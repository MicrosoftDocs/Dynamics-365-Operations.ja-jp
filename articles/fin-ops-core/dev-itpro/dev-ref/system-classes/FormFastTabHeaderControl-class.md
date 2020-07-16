---
title: FormFastTabHeaderControl クラス
description: このトピックでは、FormFastTabHeaderControl クラスについて説明します。
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
ms.openlocfilehash: 78400c369629cb0f1cb98fc0c7b92c67b11142c4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502944"
---
# <a name="class-formfasttabheadercontrol"></a><span data-ttu-id="3d9e8-103">クラス FormFastTabHeaderControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-103">Class FormFastTabHeaderControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormFastTabHeaderControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="3d9e8-104">備考</span><span class="sxs-lookup"><span data-stu-id="3d9e8-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3d9e8-105">例</span><span class="sxs-lookup"><span data-stu-id="3d9e8-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3d9e8-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3d9e8-106">Methods</span></span>

| <span data-ttu-id="3d9e8-107">方法</span><span class="sxs-lookup"><span data-stu-id="3d9e8-107">Method</span></span>                                                                                                              | <span data-ttu-id="3d9e8-108">説明</span><span class="sxs-lookup"><span data-stu-id="3d9e8-108">Description</span></span>                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d9e8-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-112">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-112">public boolean alignChild(\[boolean value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-113">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-113">public boolean alignChildren(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-114">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-114">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="3d9e8-115">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-115">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="3d9e8-116">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-116">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="3d9e8-117">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-117">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="3d9e8-118">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-118">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="3d9e8-119">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-119">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="3d9e8-120">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-120">public int allowUserSetup(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-121">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-121">public int arrangeGuide(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-122">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-122">public int arrangeMethod(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-123">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-123">public int arrangeWhen(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-124">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-124">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="3d9e8-125">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-125">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="3d9e8-126">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-126">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="3d9e8-127">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-127">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="3d9e8-128">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-128">public int backStyle(\[int value\])</span></span>                                                                                 | <span data-ttu-id="3d9e8-129">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-129">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="3d9e8-130">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-130">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="3d9e8-131">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-131">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="3d9e8-132">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-132">public int bold(\[int value\])</span></span>                                                                                      | <span data-ttu-id="3d9e8-133">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-133">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="3d9e8-134">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-134">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-135">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-135">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-136">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-136">public int bottomMarginValue(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-137">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-137">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="3d9e8-138">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-138">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="3d9e8-139">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-139">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-140">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-140">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-141">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-141">public str caption(\[str value\])</span></span>                                                                                   | <span data-ttu-id="3d9e8-142">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-142">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="3d9e8-143">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-143">public int characterSet(\[int value\])</span></span>                                                                              | <span data-ttu-id="3d9e8-144">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-144">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="3d9e8-145">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-145">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="3d9e8-146">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-146">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="3d9e8-147">public int columns(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-147">public int columns(\[int value\], \[AutoMode mode\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-148">public AutoMode columnsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-148">public AutoMode columnsMode(\[AutoMode mode\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-149">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-149">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-150">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-150">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-151">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-151">public int columnspaceValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-152">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-152">public int columnsValue(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-153">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-153">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="3d9e8-154">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-154">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="3d9e8-155">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-155">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="3d9e8-156">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-156">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="3d9e8-157">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-157">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-158">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-158">public int controlCount()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-159">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-159">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-160">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-160">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="3d9e8-161">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-161">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="3d9e8-162">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-162">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-163">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-163">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="3d9e8-164">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-164">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="3d9e8-165">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-165">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="3d9e8-166">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-166">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="3d9e8-167">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-167">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="3d9e8-168">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-168">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="3d9e8-169">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-169">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="3d9e8-170">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-170">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="3d9e8-171">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-171">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="3d9e8-172">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-172">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="3d9e8-173">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-173">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="3d9e8-174">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-174">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="3d9e8-175">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-175">public str dragText()</span></span>                                                                                               | <span data-ttu-id="3d9e8-176">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-176">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="3d9e8-177">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-177">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="3d9e8-178">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-178">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="3d9e8-179">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-179">public str font(\[str value\])</span></span>                                                                                      | <span data-ttu-id="3d9e8-180">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-180">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="3d9e8-181">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-181">public int fontSize(\[int value\])</span></span>                                                                                  | <span data-ttu-id="3d9e8-182">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-182">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="3d9e8-183">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-183">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="3d9e8-184">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-184">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="3d9e8-185">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-185">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="3d9e8-186">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-186">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="3d9e8-187">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-187">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="3d9e8-188">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-188">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="3d9e8-189">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-189">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="3d9e8-190">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-190">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="3d9e8-191">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-191">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="3d9e8-192">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-192">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="3d9e8-193">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-193">public str helpField()</span></span>                                                                                              | <span data-ttu-id="3d9e8-194">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-194">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="3d9e8-195">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-195">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="3d9e8-196">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-196">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="3d9e8-197">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-197">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-198">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-198">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="3d9e8-199">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-199">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="3d9e8-200">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-200">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="3d9e8-201">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-201">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="3d9e8-202">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-202">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-203">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-203">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="3d9e8-204">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-204">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="3d9e8-205">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-205">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="3d9e8-206">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-206">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="3d9e8-207">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-207">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="3d9e8-208">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-208">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="3d9e8-209">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-209">public boolean italic(\[boolean value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-210">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-210">public boolean leave()</span></span>                                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-211">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-211">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="3d9e8-212">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-212">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="3d9e8-213">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-213">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-214">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-214">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-215">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-215">public int leftMarginValue(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-216">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-216">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="3d9e8-217">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-217">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="3d9e8-218">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-218">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="3d9e8-219">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-219">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="3d9e8-220">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-220">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="3d9e8-221">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-221">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="3d9e8-222">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-222">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="3d9e8-223">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-223">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="3d9e8-224">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-224">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="3d9e8-225">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-225">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="3d9e8-226">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-226">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="3d9e8-227">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-227">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="3d9e8-228">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-228">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="3d9e8-229">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-229">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="3d9e8-230">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-230">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-231">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-231">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="3d9e8-232">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-232">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="3d9e8-233">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-233">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-234">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-234">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-235">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-235">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="3d9e8-236">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-236">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="3d9e8-237">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-237">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-238">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-238">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-239">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-239">public int rightMarginValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-240">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-240">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="3d9e8-241">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-241">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="3d9e8-242">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-242">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="3d9e8-243">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-243">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="3d9e8-244">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-244">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="3d9e8-245">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-245">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="3d9e8-246">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-246">public int sort(\[SortOrder sortDirection\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-247">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-247">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="3d9e8-248">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-248">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="3d9e8-249">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-249">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="3d9e8-250">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-250">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="3d9e8-251">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-251">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-252">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-252">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-253">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-253">public int topMarginValue(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-254">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-254">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="3d9e8-255">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-255">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="3d9e8-256">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-256">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="3d9e8-257">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-257">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="3d9e8-258">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-258">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-259">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-259">public boolean underline(\[boolean value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-260">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-260">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-261">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-261">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="3d9e8-262">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-262">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="3d9e8-263">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-263">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="3d9e8-264">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-264">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="3d9e8-265">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-265">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="3d9e8-266">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-266">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="3d9e8-267">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-267">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="3d9e8-268">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-268">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="3d9e8-269">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-269">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="3d9e8-270">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-270">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="3d9e8-271">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-271">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="3d9e8-272">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-272">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="3d9e8-273">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-273">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="3d9e8-274">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-274">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="3d9e8-275">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-275">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="3d9e8-276">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-276">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="3d9e8-277">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-277">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="3d9e8-278">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-278">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="3d9e8-279">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-279">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="3d9e8-280">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-280">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="3d9e8-281">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-281">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="3d9e8-282">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-282">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="3d9e8-283">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-283">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="3d9e8-284">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-284">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="3d9e8-285">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-285">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-286">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-286">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="3d9e8-287">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-287">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="3d9e8-288">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-288">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="3d9e8-289">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-289">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="3d9e8-290">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-290">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="3d9e8-291">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-291">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="3d9e8-292">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-292">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="3d9e8-293">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-293">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="3d9e8-294">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-294">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="3d9e8-295">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-295">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="3d9e8-296">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-296">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="3d9e8-297">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-297">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="3d9e8-298">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-298">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="3d9e8-299">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-299">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="3d9e8-300">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-300">public void filter(\[str filterStr\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-301">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-301">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                          |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-302">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-302">public void jumpRef()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-303">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-303">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-304">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-304">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="3d9e8-305">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-305">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="3d9e8-306">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-306">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-307">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-307">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="3d9e8-308">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-308">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="3d9e8-309">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-309">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="3d9e8-310">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-310">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="3d9e8-311">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-311">public void arrange()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-312">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-312">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="3d9e8-313">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-313">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="3d9e8-314">public void paste()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-314">public void paste()</span></span>                                                                                                 | <span data-ttu-id="3d9e8-315">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-315">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="3d9e8-316">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-316">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="3d9e8-317">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-317">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="3d9e8-318">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-318">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="3d9e8-319">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-319">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="3d9e8-320">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-320">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-321">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-321">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="3d9e8-322">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-322">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="3d9e8-323">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-323">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="3d9e8-324">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-324">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="3d9e8-325">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-325">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="3d9e8-326">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-326">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="3d9e8-327">public void copy()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-327">public void copy()</span></span>                                                                                                  | <span data-ttu-id="3d9e8-328">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-328">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="3d9e8-329">public void enter()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-329">public void enter()</span></span>                                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-330">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="3d9e8-330">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="3d9e8-331">public void context()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-331">public void context()</span></span>                                                                                               | <span data-ttu-id="3d9e8-332">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-332">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="3d9e8-333">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-333">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="3d9e8-334">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-334">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="3d9e8-335">public void cut()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-335">public void cut()</span></span>                                                                                                   | <span data-ttu-id="3d9e8-336">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-336">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="3d9e8-337">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-337">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="3d9e8-338">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-338">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="3d9e8-339">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="3d9e8-339">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="3d9e8-340">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-340">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="3d9e8-341">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="3d9e8-341">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="3d9e8-342">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-342">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |

## <a name="method-addcontrol"></a><span data-ttu-id="3d9e8-343">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-343">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="3d9e8-344">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-344">Parameters - addControl</span></span>

<span data-ttu-id="3d9e8-345">controlType</span><span class="sxs-lookup"><span data-stu-id="3d9e8-345">controlType</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-346">controlName</span><span class="sxs-lookup"><span data-stu-id="3d9e8-346">controlName</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-347">insertAfter</span><span class="sxs-lookup"><span data-stu-id="3d9e8-347">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="3d9e8-348">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-348">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="3d9e8-349">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="3d9e8-349">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="3d9e8-350">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="3d9e8-350">Parameters - addControlEx</span></span>

<span data-ttu-id="3d9e8-351">controlClass</span><span class="sxs-lookup"><span data-stu-id="3d9e8-351">controlClass</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-352">controlName</span><span class="sxs-lookup"><span data-stu-id="3d9e8-352">controlName</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-353">insertAfter</span><span class="sxs-lookup"><span data-stu-id="3d9e8-353">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="3d9e8-354">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="3d9e8-354">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="3d9e8-355">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-355">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="3d9e8-356">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-356">Parameters - addDataField</span></span>

<span data-ttu-id="3d9e8-357">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="3d9e8-357">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-358">fieldId</span><span class="sxs-lookup"><span data-stu-id="3d9e8-358">fieldId</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-359">insertAfter</span><span class="sxs-lookup"><span data-stu-id="3d9e8-359">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-360">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="3d9e8-360">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="3d9e8-361">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-361">Return Value - addDataField</span></span>

## <a name="method-alignchild"></a><span data-ttu-id="3d9e8-362">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="3d9e8-362">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="3d9e8-363">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="3d9e8-363">Parameters - alignChild</span></span>

<span data-ttu-id="3d9e8-364">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-364">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="3d9e8-365">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="3d9e8-365">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="3d9e8-366">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="3d9e8-366">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="3d9e8-367">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="3d9e8-367">Parameters - alignChildren</span></span>

<span data-ttu-id="3d9e8-368">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-368">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="3d9e8-369">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="3d9e8-369">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="3d9e8-370">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-370">Method alignControl</span></span>

<span data-ttu-id="3d9e8-371">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-371">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="3d9e8-372">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-372">Parameters - alignControl</span></span>

<span data-ttu-id="3d9e8-373">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-373">value</span></span>  
<span data-ttu-id="3d9e8-374">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-374">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="3d9e8-375">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-375">Return Value - alignControl</span></span>

<span data-ttu-id="3d9e8-376">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-376">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="3d9e8-377">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-377">Remarks - alignControl</span></span>

<span data-ttu-id="3d9e8-378">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-378">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="3d9e8-379">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="3d9e8-379">Method allowEdit</span></span>

<span data-ttu-id="3d9e8-380">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-380">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="3d9e8-381">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="3d9e8-381">Parameters - allowEdit</span></span>

<span data-ttu-id="3d9e8-382">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-382">value</span></span>  
<span data-ttu-id="3d9e8-383">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-383">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="3d9e8-384">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="3d9e8-384">Return Value - allowEdit</span></span>

<span data-ttu-id="3d9e8-385">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-385">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="3d9e8-386">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="3d9e8-386">Remarks - allowEdit</span></span>

<span data-ttu-id="3d9e8-387">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-387">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="3d9e8-388">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="3d9e8-388">Method allowSysSetup</span></span>

<span data-ttu-id="3d9e8-389">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-389">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="3d9e8-390">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="3d9e8-390">Return Value - allowSysSetup</span></span>

<span data-ttu-id="3d9e8-391">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-391">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="3d9e8-392">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="3d9e8-392">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="3d9e8-393">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="3d9e8-393">Parameters - allowUserSetup</span></span>

<span data-ttu-id="3d9e8-394">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-394">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="3d9e8-395">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="3d9e8-395">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="3d9e8-396">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="3d9e8-396">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="3d9e8-397">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="3d9e8-397">Parameters - arrangeGuide</span></span>

<span data-ttu-id="3d9e8-398">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-398">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="3d9e8-399">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="3d9e8-399">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="3d9e8-400">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="3d9e8-400">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="3d9e8-401">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="3d9e8-401">Parameters - arrangeMethod</span></span>

<span data-ttu-id="3d9e8-402">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-402">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="3d9e8-403">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="3d9e8-403">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="3d9e8-404">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="3d9e8-404">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="3d9e8-405">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="3d9e8-405">Parameters - arrangeWhen</span></span>

<span data-ttu-id="3d9e8-406">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-406">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="3d9e8-407">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="3d9e8-407">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="3d9e8-408">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3d9e8-408">Method autoDeclaration</span></span>

<span data-ttu-id="3d9e8-409">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-409">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="3d9e8-410">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3d9e8-410">Parameters - autoDeclaration</span></span>

<span data-ttu-id="3d9e8-411">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-411">value</span></span>  
<span data-ttu-id="3d9e8-412">プロパティを設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-412">The value to which to set the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="3d9e8-413">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3d9e8-413">Return Value - autoDeclaration</span></span>

<span data-ttu-id="3d9e8-414">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-414">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="3d9e8-415">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="3d9e8-415">Remarks - autoDeclaration</span></span>

<span data-ttu-id="3d9e8-416">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-416">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="3d9e8-417">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3d9e8-417">Method backgroundColor</span></span>

<span data-ttu-id="3d9e8-418">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-418">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="3d9e8-419">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3d9e8-419">Parameters - backgroundColor</span></span>

<span data-ttu-id="3d9e8-420">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-420">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="3d9e8-421">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3d9e8-421">Return Value - backgroundColor</span></span>

<span data-ttu-id="3d9e8-422">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-422">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="3d9e8-423">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3d9e8-423">Remarks - backgroundColor</span></span>

<span data-ttu-id="3d9e8-424">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-424">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="3d9e8-425">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-425">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="3d9e8-426">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-426">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="3d9e8-427">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-427">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="3d9e8-428">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-428">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="3d9e8-429">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-429">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="3d9e8-430">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="3d9e8-430">Method backStyle</span></span>

<span data-ttu-id="3d9e8-431">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-431">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="3d9e8-432">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="3d9e8-432">Parameters - backStyle</span></span>

<span data-ttu-id="3d9e8-433">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-433">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="3d9e8-434">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="3d9e8-434">Return Value - backStyle</span></span>

<span data-ttu-id="3d9e8-435">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-435">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="3d9e8-436">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="3d9e8-436">Method beginDrag</span></span>

<span data-ttu-id="3d9e8-437">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-437">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="3d9e8-438">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="3d9e8-438">Parameters - beginDrag</span></span>

<span data-ttu-id="3d9e8-439">x</span><span class="sxs-lookup"><span data-stu-id="3d9e8-439">x</span></span>  
<span data-ttu-id="3d9e8-440">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-440">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="3d9e8-441">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-441">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-442">y</span><span class="sxs-lookup"><span data-stu-id="3d9e8-442">y</span></span>  
<span data-ttu-id="3d9e8-443">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-443">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="3d9e8-444">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-444">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="3d9e8-445">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="3d9e8-445">Return Value - beginDrag</span></span>

<span data-ttu-id="3d9e8-446">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-446">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="3d9e8-447">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="3d9e8-447">Remarks - beginDrag</span></span>

<span data-ttu-id="3d9e8-448">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-448">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="3d9e8-449">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-449">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="3d9e8-450">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="3d9e8-450">Method bold</span></span>

<span data-ttu-id="3d9e8-451">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-451">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="3d9e8-452">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="3d9e8-452">Parameters - bold</span></span>

<span data-ttu-id="3d9e8-453">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-453">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="3d9e8-454">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="3d9e8-454">Return Value - bold</span></span>

<span data-ttu-id="3d9e8-455">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-455">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="3d9e8-456">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="3d9e8-456">Remarks - bold</span></span>

<span data-ttu-id="3d9e8-457">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-457">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="3d9e8-458">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-458">0 Use the default font weight.</span></span>
-   <span data-ttu-id="3d9e8-459">1 シン。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-459">1 Thin.</span></span>
-   <span data-ttu-id="3d9e8-460">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-460">2 Extra-light.</span></span>
-   <span data-ttu-id="3d9e8-461">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-461">3 Light.</span></span>
-   <span data-ttu-id="3d9e8-462">4 標準。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-462">4 Normal.</span></span>
-   <span data-ttu-id="3d9e8-463">5 中。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-463">5 Medium.</span></span>
-   <span data-ttu-id="3d9e8-464">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-464">6 Semibold.</span></span>
-   <span data-ttu-id="3d9e8-465">7 太字。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-465">7 Bold.</span></span>
-   <span data-ttu-id="3d9e8-466">8 極太。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-466">8 Extra-bold.</span></span>
-   <span data-ttu-id="3d9e8-467">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-467">9 Heavy.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="3d9e8-468">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-468">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="3d9e8-469">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-469">Parameters - bottomMargin</span></span>

<span data-ttu-id="3d9e8-470">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-470">value</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-471">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-471">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="3d9e8-472">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-472">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="3d9e8-473">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-473">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="3d9e8-474">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-474">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="3d9e8-475">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-475">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="3d9e8-476">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-476">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="3d9e8-477">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-477">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="3d9e8-478">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-478">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="3d9e8-479">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-479">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="3d9e8-480">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-480">Return Value - bottomMarginValue</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="3d9e8-481">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="3d9e8-481">Method calcControlSize</span></span>

<span data-ttu-id="3d9e8-482">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-482">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="3d9e8-483">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="3d9e8-483">Parameters - calcControlSize</span></span>

<span data-ttu-id="3d9e8-484">chars</span><span class="sxs-lookup"><span data-stu-id="3d9e8-484">chars</span></span>  
<span data-ttu-id="3d9e8-485">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-485">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-486">明細行</span><span class="sxs-lookup"><span data-stu-id="3d9e8-486">lines</span></span>  
<span data-ttu-id="3d9e8-487">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-487">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="3d9e8-488">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="3d9e8-488">Return Value - calcControlSize</span></span>

<span data-ttu-id="3d9e8-489">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-489">The container that holds the width and height.</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="3d9e8-490">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-490">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="3d9e8-491">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-491">Parameters - canAddDataField</span></span>

<span data-ttu-id="3d9e8-492">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="3d9e8-492">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-493">fieldId</span><span class="sxs-lookup"><span data-stu-id="3d9e8-493">fieldId</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-494">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="3d9e8-494">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="3d9e8-495">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-495">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="3d9e8-496">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="3d9e8-496">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="3d9e8-497">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="3d9e8-497">Parameters - canContain</span></span>

<span data-ttu-id="3d9e8-498">control</span><span class="sxs-lookup"><span data-stu-id="3d9e8-498">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="3d9e8-499">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="3d9e8-499">Return Value - canContain</span></span>

## <a name="method-caption"></a><span data-ttu-id="3d9e8-500">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="3d9e8-500">Method caption</span></span>

<span data-ttu-id="3d9e8-501">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-501">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="3d9e8-502">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="3d9e8-502">Parameters - caption</span></span>

<span data-ttu-id="3d9e8-503">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-503">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="3d9e8-504">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="3d9e8-504">Return Value - caption</span></span>

<span data-ttu-id="3d9e8-505">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-505">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="3d9e8-506">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="3d9e8-506">Method characterSet</span></span>

<span data-ttu-id="3d9e8-507">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-507">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="3d9e8-508">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="3d9e8-508">Parameters - characterSet</span></span>

<span data-ttu-id="3d9e8-509">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-509">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="3d9e8-510">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="3d9e8-510">Return Value - characterSet</span></span>

<span data-ttu-id="3d9e8-511">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-511">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="3d9e8-512">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="3d9e8-512">Remarks - characterSet</span></span>

<span data-ttu-id="3d9e8-513">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-513">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="3d9e8-514">値です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-514">Value.</span></span> | <span data-ttu-id="3d9e8-515">説明。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-515">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="3d9e8-516">0</span><span class="sxs-lookup"><span data-stu-id="3d9e8-516">0</span></span>      | <span data-ttu-id="3d9e8-517">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-517">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="3d9e8-518">1</span><span class="sxs-lookup"><span data-stu-id="3d9e8-518">1</span></span>      | <span data-ttu-id="3d9e8-519">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-519">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="3d9e8-520">2</span><span class="sxs-lookup"><span data-stu-id="3d9e8-520">2</span></span>      | <span data-ttu-id="3d9e8-521">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-521">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="3d9e8-522">77</span><span class="sxs-lookup"><span data-stu-id="3d9e8-522">77</span></span>     | <span data-ttu-id="3d9e8-523">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-523">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="3d9e8-524">128</span><span class="sxs-lookup"><span data-stu-id="3d9e8-524">128</span></span>    | <span data-ttu-id="3d9e8-525">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-525">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="3d9e8-526">129</span><span class="sxs-lookup"><span data-stu-id="3d9e8-526">129</span></span>    | <span data-ttu-id="3d9e8-527">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-527">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="3d9e8-528">134</span><span class="sxs-lookup"><span data-stu-id="3d9e8-528">134</span></span>    | <span data-ttu-id="3d9e8-529">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-529">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="3d9e8-530">136</span><span class="sxs-lookup"><span data-stu-id="3d9e8-530">136</span></span>    | <span data-ttu-id="3d9e8-531">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-531">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="3d9e8-532">161</span><span class="sxs-lookup"><span data-stu-id="3d9e8-532">161</span></span>    | <span data-ttu-id="3d9e8-533">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-533">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="3d9e8-534">162</span><span class="sxs-lookup"><span data-stu-id="3d9e8-534">162</span></span>    | <span data-ttu-id="3d9e8-535">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-535">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="3d9e8-536">163</span><span class="sxs-lookup"><span data-stu-id="3d9e8-536">163</span></span>    | <span data-ttu-id="3d9e8-537">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-537">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="3d9e8-538">186</span><span class="sxs-lookup"><span data-stu-id="3d9e8-538">186</span></span>    | <span data-ttu-id="3d9e8-539">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-539">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="3d9e8-540">204</span><span class="sxs-lookup"><span data-stu-id="3d9e8-540">204</span></span>    | <span data-ttu-id="3d9e8-541">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-541">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="3d9e8-542">238</span><span class="sxs-lookup"><span data-stu-id="3d9e8-542">238</span></span>    | <span data-ttu-id="3d9e8-543">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-543">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="3d9e8-544">255</span><span class="sxs-lookup"><span data-stu-id="3d9e8-544">255</span></span>    | <span data-ttu-id="3d9e8-545">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-545">OEM\_CHARSET</span></span>         |

<span data-ttu-id="3d9e8-546">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-546">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="3d9e8-547">値です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-547">Value.</span></span> | <span data-ttu-id="3d9e8-548">説明。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-548">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="3d9e8-549">130</span><span class="sxs-lookup"><span data-stu-id="3d9e8-549">130</span></span>    | <span data-ttu-id="3d9e8-550">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-550">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="3d9e8-551">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-551">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="3d9e8-552">値です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-552">Value.</span></span> | <span data-ttu-id="3d9e8-553">説明。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-553">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="3d9e8-554">177</span><span class="sxs-lookup"><span data-stu-id="3d9e8-554">177</span></span>    | <span data-ttu-id="3d9e8-555">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-555">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="3d9e8-556">178</span><span class="sxs-lookup"><span data-stu-id="3d9e8-556">178</span></span>    | <span data-ttu-id="3d9e8-557">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-557">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="3d9e8-558">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-558">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="3d9e8-559">値です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-559">Value.</span></span> | <span data-ttu-id="3d9e8-560">説明。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-560">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="3d9e8-561">222</span><span class="sxs-lookup"><span data-stu-id="3d9e8-561">222</span></span>    | <span data-ttu-id="3d9e8-562">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="3d9e8-562">THAI\_CHARSET</span></span> |

<span data-ttu-id="3d9e8-563">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-563">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="3d9e8-564">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-564">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="3d9e8-565">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-565">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="3d9e8-566">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="3d9e8-566">Method colorScheme</span></span>

<span data-ttu-id="3d9e8-567">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-567">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="3d9e8-568">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="3d9e8-568">Parameters - colorScheme</span></span>

<span data-ttu-id="3d9e8-569">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-569">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="3d9e8-570">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="3d9e8-570">Return Value - colorScheme</span></span>

<span data-ttu-id="3d9e8-571">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-571">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="3d9e8-572">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="3d9e8-572">Remarks - colorScheme</span></span>

<span data-ttu-id="3d9e8-573">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-573">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="3d9e8-574">値です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-574">Value.</span></span> | <span data-ttu-id="3d9e8-575">スタイル。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-575">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="3d9e8-576">0</span><span class="sxs-lookup"><span data-stu-id="3d9e8-576">0</span></span>      | <span data-ttu-id="3d9e8-577">既定。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-577">Default.</span></span>               |
| <span data-ttu-id="3d9e8-578">1</span><span class="sxs-lookup"><span data-stu-id="3d9e8-578">1</span></span>      | <span data-ttu-id="3d9e8-579">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-579">The Windows palette.</span></span>   |
| <span data-ttu-id="3d9e8-580">2</span><span class="sxs-lookup"><span data-stu-id="3d9e8-580">2</span></span>      | <span data-ttu-id="3d9e8-581">真の配色。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-581">The true-color scheme.</span></span> |

## <a name="method-columns"></a><span data-ttu-id="3d9e8-582">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="3d9e8-582">Method columns</span></span>

```xpp
public int columns([int value], [AutoMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="3d9e8-583">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="3d9e8-583">Parameters - columns</span></span>

<span data-ttu-id="3d9e8-584">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-584">value</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-585">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-585">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="3d9e8-586">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="3d9e8-586">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="3d9e8-587">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-587">Method columnsMode</span></span>

```xpp
public AutoMode columnsMode([AutoMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="3d9e8-588">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-588">Parameters - columnsMode</span></span>

<span data-ttu-id="3d9e8-589">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-589">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="3d9e8-590">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-590">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="3d9e8-591">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="3d9e8-591">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="3d9e8-592">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="3d9e8-592">Parameters - columnspace</span></span>

<span data-ttu-id="3d9e8-593">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-593">value</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-594">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-594">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="3d9e8-595">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="3d9e8-595">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="3d9e8-596">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-596">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="3d9e8-597">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-597">Parameters - columnspaceMode</span></span>

<span data-ttu-id="3d9e8-598">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-598">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="3d9e8-599">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-599">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="3d9e8-600">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-600">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="3d9e8-601">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-601">Parameters - columnspaceValue</span></span>

<span data-ttu-id="3d9e8-602">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-602">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="3d9e8-603">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-603">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="3d9e8-604">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-604">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="3d9e8-605">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-605">Parameters - columnsValue</span></span>

<span data-ttu-id="3d9e8-606">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-606">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="3d9e8-607">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-607">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="3d9e8-608">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="3d9e8-608">Method configurationKey</span></span>

<span data-ttu-id="3d9e8-609">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-609">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="3d9e8-610">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="3d9e8-610">Parameters - configurationKey</span></span>

<span data-ttu-id="3d9e8-611">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-611">value</span></span>  
<span data-ttu-id="3d9e8-612">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-612">The ID of the configuration key being assigned to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="3d9e8-613">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="3d9e8-613">Return Value - configurationKey</span></span>

<span data-ttu-id="3d9e8-614">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-614">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="3d9e8-615">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="3d9e8-615">Remarks - configurationKey</span></span>

<span data-ttu-id="3d9e8-616">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-616">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="3d9e8-617">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-617">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="3d9e8-618">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="3d9e8-618">Method configurationKeyEx</span></span>

<span data-ttu-id="3d9e8-619">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-619">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="3d9e8-620">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="3d9e8-620">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="3d9e8-621">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-621">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="3d9e8-622">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="3d9e8-622">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="3d9e8-623">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-623">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="3d9e8-624">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-624">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="3d9e8-625">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-625">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-contains"></a><span data-ttu-id="3d9e8-626">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="3d9e8-626">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="3d9e8-627">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="3d9e8-627">Parameters - contains</span></span>

<span data-ttu-id="3d9e8-628">control</span><span class="sxs-lookup"><span data-stu-id="3d9e8-628">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="3d9e8-629">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="3d9e8-629">Return Value - contains</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="3d9e8-630">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="3d9e8-630">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="3d9e8-631">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="3d9e8-631">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="3d9e8-632">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="3d9e8-632">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="3d9e8-633">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="3d9e8-633">Parameters - controlNum</span></span>

<span data-ttu-id="3d9e8-634">controlNo</span><span class="sxs-lookup"><span data-stu-id="3d9e8-634">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="3d9e8-635">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="3d9e8-635">Return Value - controlNum</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="3d9e8-636">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3d9e8-636">Method countryRegionCodes</span></span>

<span data-ttu-id="3d9e8-637">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-637">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="3d9e8-638">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3d9e8-638">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="3d9e8-639">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-639">value</span></span>  
<span data-ttu-id="3d9e8-640">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-640">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="3d9e8-641">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3d9e8-641">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="3d9e8-642">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-642">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="3d9e8-643">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-643">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="3d9e8-644">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-644">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="3d9e8-645">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-645">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="3d9e8-646">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-646">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="3d9e8-647">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="3d9e8-647">Method dataRelationPath</span></span>

<span data-ttu-id="3d9e8-648">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-648">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="3d9e8-649">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="3d9e8-649">Parameters - dataRelationPath</span></span>

<span data-ttu-id="3d9e8-650">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-650">value</span></span>  
<span data-ttu-id="3d9e8-651">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-651">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="3d9e8-652">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="3d9e8-652">Return Value - dataRelationPath</span></span>

<span data-ttu-id="3d9e8-653">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-653">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="3d9e8-654">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="3d9e8-654">Remarks - dataRelationPath</span></span>

<span data-ttu-id="3d9e8-655">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-655">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="3d9e8-656">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-656">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="3d9e8-657">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="3d9e8-657">Method dataSource</span></span>

<span data-ttu-id="3d9e8-658">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-658">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="3d9e8-659">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="3d9e8-659">Parameters - dataSource</span></span>

<span data-ttu-id="3d9e8-660">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-660">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="3d9e8-661">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="3d9e8-661">Return Value - dataSource</span></span>

<span data-ttu-id="3d9e8-662">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-662">The identifier of the data source to be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="3d9e8-663">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="3d9e8-663">Method displayTarget</span></span>

<span data-ttu-id="3d9e8-664">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-664">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="3d9e8-665">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="3d9e8-665">Parameters - displayTarget</span></span>

<span data-ttu-id="3d9e8-666">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-666">value</span></span>  
<span data-ttu-id="3d9e8-667">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-667">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="3d9e8-668">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="3d9e8-668">Return Value - displayTarget</span></span>

<span data-ttu-id="3d9e8-669">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-669">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="3d9e8-670">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="3d9e8-670">Method dragDrop</span></span>

<span data-ttu-id="3d9e8-671">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-671">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="3d9e8-672">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="3d9e8-672">Parameters - dragDrop</span></span>

<span data-ttu-id="3d9e8-673">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-673">value</span></span>  
<span data-ttu-id="3d9e8-674">ドラッグ アンド ドロップ動作が有効になっているかどうかを示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-674">An Integer data type that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="3d9e8-675">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="3d9e8-675">Return Value - dragDrop</span></span>

<span data-ttu-id="3d9e8-676">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-676">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="3d9e8-677">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="3d9e8-677">Remarks - dragDrop</span></span>

<span data-ttu-id="3d9e8-678">dragLeave、dragOver、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-678">Use the dragLeave, dragOver, and dragOverEx methods to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="3d9e8-679">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="3d9e8-679">Method dragOver</span></span>

<span data-ttu-id="3d9e8-680">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-680">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="3d9e8-681">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="3d9e8-681">Parameters - dragOver</span></span>

<span data-ttu-id="3d9e8-682">dragSource</span><span class="sxs-lookup"><span data-stu-id="3d9e8-682">dragSource</span></span>  
<span data-ttu-id="3d9e8-683">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-683">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-684">dragMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-684">dragMode</span></span>  
<span data-ttu-id="3d9e8-685">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-685">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-686">x</span><span class="sxs-lookup"><span data-stu-id="3d9e8-686">x</span></span>  
<span data-ttu-id="3d9e8-687">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-687">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-688">y</span><span class="sxs-lookup"><span data-stu-id="3d9e8-688">y</span></span>  
<span data-ttu-id="3d9e8-689">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-689">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="3d9e8-690">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="3d9e8-690">Return Value - dragOver</span></span>

<span data-ttu-id="3d9e8-691">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-691">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="3d9e8-692">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="3d9e8-692">Method dragOverEx</span></span>

<span data-ttu-id="3d9e8-693">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-693">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="3d9e8-694">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="3d9e8-694">Parameters - dragOverEx</span></span>

<span data-ttu-id="3d9e8-695">dragSource</span><span class="sxs-lookup"><span data-stu-id="3d9e8-695">dragSource</span></span>  
<span data-ttu-id="3d9e8-696">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-696">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-697">dragMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-697">dragMode</span></span>  
<span data-ttu-id="3d9e8-698">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-698">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-699">x</span><span class="sxs-lookup"><span data-stu-id="3d9e8-699">x</span></span>  
<span data-ttu-id="3d9e8-700">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-700">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-701">y</span><span class="sxs-lookup"><span data-stu-id="3d9e8-701">y</span></span>  
<span data-ttu-id="3d9e8-702">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-702">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="3d9e8-703">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="3d9e8-703">Return Value - dragOverEx</span></span>

<span data-ttu-id="3d9e8-704">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-704">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="3d9e8-705">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="3d9e8-705">Method dragText</span></span>

<span data-ttu-id="3d9e8-706">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-706">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="3d9e8-707">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="3d9e8-707">Return Value - dragText</span></span>

<span data-ttu-id="3d9e8-708">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-708">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="3d9e8-709">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="3d9e8-709">Method enabled</span></span>

<span data-ttu-id="3d9e8-710">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-710">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="3d9e8-711">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="3d9e8-711">Parameters - enabled</span></span>

<span data-ttu-id="3d9e8-712">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-712">value</span></span>  
<span data-ttu-id="3d9e8-713">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-713">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="3d9e8-714">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="3d9e8-714">Return Value - enabled</span></span>

<span data-ttu-id="3d9e8-715">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-715">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="3d9e8-716">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="3d9e8-716">Remarks - enabled</span></span>

<span data-ttu-id="3d9e8-717">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-717">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="3d9e8-718">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-718">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="3d9e8-719">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-719">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="3d9e8-720">メソッド font</span><span class="sxs-lookup"><span data-stu-id="3d9e8-720">Method font</span></span>

<span data-ttu-id="3d9e8-721">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-721">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="3d9e8-722">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="3d9e8-722">Parameters - font</span></span>

<span data-ttu-id="3d9e8-723">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-723">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="3d9e8-724">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="3d9e8-724">Return Value - font</span></span>

<span data-ttu-id="3d9e8-725">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-725">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="3d9e8-726">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="3d9e8-726">Method fontSize</span></span>

<span data-ttu-id="3d9e8-727">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-727">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="3d9e8-728">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="3d9e8-728">Parameters - fontSize</span></span>

<span data-ttu-id="3d9e8-729">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-729">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="3d9e8-730">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="3d9e8-730">Return Value - fontSize</span></span>

<span data-ttu-id="3d9e8-731">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-731">The height of the font in points.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="3d9e8-732">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="3d9e8-732">Method hasChanged</span></span>

<span data-ttu-id="3d9e8-733">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-733">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="3d9e8-734">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="3d9e8-734">Parameters - hasChanged</span></span>

<span data-ttu-id="3d9e8-735">val</span><span class="sxs-lookup"><span data-stu-id="3d9e8-735">val</span></span>  
<span data-ttu-id="3d9e8-736">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-736">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="3d9e8-737">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="3d9e8-737">Return Value - hasChanged</span></span>

<span data-ttu-id="3d9e8-738">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-738">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="3d9e8-739">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="3d9e8-739">Method hasUserSetting</span></span>

<span data-ttu-id="3d9e8-740">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-740">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="3d9e8-741">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="3d9e8-741">Return Value - hasUserSetting</span></span>

<span data-ttu-id="3d9e8-742">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-742">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="3d9e8-743">メソッド height</span><span class="sxs-lookup"><span data-stu-id="3d9e8-743">Method height</span></span>

<span data-ttu-id="3d9e8-744">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-744">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="3d9e8-745">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="3d9e8-745">Parameters - height</span></span>

<span data-ttu-id="3d9e8-746">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-746">value</span></span>  
<span data-ttu-id="3d9e8-747">高さの計算方法を示す整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-747">An integer data type that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-748">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-748">mode</span></span>  
<span data-ttu-id="3d9e8-749">高さの計算方法を示す整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-749">An integer data type that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="3d9e8-750">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="3d9e8-750">Return Value - height</span></span>

<span data-ttu-id="3d9e8-751">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-751">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="3d9e8-752">備考 - height</span><span class="sxs-lookup"><span data-stu-id="3d9e8-752">Remarks - height</span></span>

<span data-ttu-id="3d9e8-753">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-753">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="3d9e8-754">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="3d9e8-754">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="3d9e8-755">モード。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-755">Mode.</span></span>            | <span data-ttu-id="3d9e8-756">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-756">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d9e8-757">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-757">-1 Exact.</span></span>        | <span data-ttu-id="3d9e8-758">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-758">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3d9e8-759">0 自動。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-759">0 Auto.</span></span>          | <span data-ttu-id="3d9e8-760">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-760">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3d9e8-761">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-761">1 Column height.</span></span> | <span data-ttu-id="3d9e8-762">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-762">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="3d9e8-763">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-763">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="3d9e8-764">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-764">Method heightMode</span></span>

<span data-ttu-id="3d9e8-765">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-765">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="3d9e8-766">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-766">Parameters - heightMode</span></span>

<span data-ttu-id="3d9e8-767">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-767">value</span></span>  
<span data-ttu-id="3d9e8-768">コントロールの高さの計算方法を示す整数データ型値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-768">An integer data type value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="3d9e8-769">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-769">Return Value - heightMode</span></span>

<span data-ttu-id="3d9e8-770">計算モード。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-770">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="3d9e8-771">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-771">Remarks - heightMode</span></span>

<span data-ttu-id="3d9e8-772">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="3d9e8-772">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="3d9e8-773">モード。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-773">Mode.</span></span>          | <span data-ttu-id="3d9e8-774">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-774">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d9e8-775">正確。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-775">Exact.</span></span>         | <span data-ttu-id="3d9e8-776">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-776">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3d9e8-777">自動。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-777">Auto.</span></span>          | <span data-ttu-id="3d9e8-778">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-778">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3d9e8-779">列の高さ</span><span class="sxs-lookup"><span data-stu-id="3d9e8-779">Column height.</span></span> | <span data-ttu-id="3d9e8-780">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-780">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="3d9e8-781">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-781">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="3d9e8-782">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-782">Method heightValue</span></span>

<span data-ttu-id="3d9e8-783">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-783">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="3d9e8-784">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-784">Parameters - heightValue</span></span>

<span data-ttu-id="3d9e8-785">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-785">value</span></span>  
<span data-ttu-id="3d9e8-786">高さをピクセル単位で指定する整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-786">An integer data type that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="3d9e8-787">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-787">Return Value - heightValue</span></span>

<span data-ttu-id="3d9e8-788">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-788">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="3d9e8-789">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-789">Remarks - heightValue</span></span>

<span data-ttu-id="3d9e8-790">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-790">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="3d9e8-791">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-791">Method helpField</span></span>

<span data-ttu-id="3d9e8-792">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-792">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="3d9e8-793">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-793">Return Value - helpField</span></span>

<span data-ttu-id="3d9e8-794">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-794">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="3d9e8-795">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="3d9e8-795">Remarks - helpField</span></span>

<span data-ttu-id="3d9e8-796">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-796">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="3d9e8-797">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-797">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="3d9e8-798">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="3d9e8-798">Method helpText</span></span>

<span data-ttu-id="3d9e8-799">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-799">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="3d9e8-800">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="3d9e8-800">Parameters - helpText</span></span>

<span data-ttu-id="3d9e8-801">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-801">value</span></span>  
<span data-ttu-id="3d9e8-802">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-802">The value that is assigned as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="3d9e8-803">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="3d9e8-803">Return Value - helpText</span></span>

<span data-ttu-id="3d9e8-804">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-804">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="3d9e8-805">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="3d9e8-805">Remarks - helpText</span></span>

<span data-ttu-id="3d9e8-806">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-806">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="3d9e8-807">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-807">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="3d9e8-808">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="3d9e8-808">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="3d9e8-809">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="3d9e8-809">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="3d9e8-810">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-810">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="3d9e8-811">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="3d9e8-811">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="3d9e8-812">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="3d9e8-812">Method hierarchyParent</span></span>

<span data-ttu-id="3d9e8-813">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-813">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="3d9e8-814">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="3d9e8-814">Parameters - hierarchyParent</span></span>

<span data-ttu-id="3d9e8-815">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-815">value</span></span>  
<span data-ttu-id="3d9e8-816">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-816">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="3d9e8-817">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="3d9e8-817">Return Value - hierarchyParent</span></span>

<span data-ttu-id="3d9e8-818">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-818">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="3d9e8-819">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="3d9e8-819">Method hWnd</span></span>

<span data-ttu-id="3d9e8-820">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-820">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="3d9e8-821">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="3d9e8-821">Return Value - hWnd</span></span>

<span data-ttu-id="3d9e8-822">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-822">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="3d9e8-823">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="3d9e8-823">Remarks - hWnd</span></span>

<span data-ttu-id="3d9e8-824">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-824">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="3d9e8-825">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="3d9e8-825">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="3d9e8-826">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="3d9e8-826">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="3d9e8-827">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="3d9e8-827">Method isDisplayed</span></span>

<span data-ttu-id="3d9e8-828">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-828">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="3d9e8-829">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="3d9e8-829">Return Value - isDisplayed</span></span>

<span data-ttu-id="3d9e8-830">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-830">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="3d9e8-831">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="3d9e8-831">Remarks - isDisplayed</span></span>

<span data-ttu-id="3d9e8-832">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-832">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="3d9e8-833">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="3d9e8-833">Method isRestricted</span></span>

<span data-ttu-id="3d9e8-834">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-834">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="3d9e8-835">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="3d9e8-835">Return Value - isRestricted</span></span>

<span data-ttu-id="3d9e8-836">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-836">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="3d9e8-837">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="3d9e8-837">Method isUserSetupEnabled</span></span>

<span data-ttu-id="3d9e8-838">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-838">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="3d9e8-839">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="3d9e8-839">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="3d9e8-840">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="3d9e8-840">neededSetupRights</span></span>  
<span data-ttu-id="3d9e8-841">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-841">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="3d9e8-842">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="3d9e8-842">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="3d9e8-843">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-843">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="3d9e8-844">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="3d9e8-844">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="3d9e8-845">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-845">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d9e8-846">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="3d9e8-846">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="3d9e8-847">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-847">No changes can be made to the control.</span></span> <span data-ttu-id="3d9e8-848">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-848">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="3d9e8-849">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="3d9e8-849">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="3d9e8-850">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-850">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="3d9e8-851">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-851">The user cannot move the control.</span></span>   |
| <span data-ttu-id="3d9e8-852">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="3d9e8-852">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="3d9e8-853">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-853">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="3d9e8-854">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-854">The user can also move the control.</span></span> |

<span data-ttu-id="3d9e8-855">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-855">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-italic"></a><span data-ttu-id="3d9e8-856">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="3d9e8-856">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="3d9e8-857">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="3d9e8-857">Parameters - italic</span></span>

<span data-ttu-id="3d9e8-858">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-858">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="3d9e8-859">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="3d9e8-859">Return Value - italic</span></span>

## <a name="method-leave"></a><span data-ttu-id="3d9e8-860">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="3d9e8-860">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="3d9e8-861">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="3d9e8-861">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="3d9e8-862">メソッド left</span><span class="sxs-lookup"><span data-stu-id="3d9e8-862">Method left</span></span>

<span data-ttu-id="3d9e8-863">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-863">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="3d9e8-864">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="3d9e8-864">Parameters - left</span></span>

<span data-ttu-id="3d9e8-865">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-865">value</span></span>  
<span data-ttu-id="3d9e8-866">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-866">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-867">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-867">mode</span></span>  
<span data-ttu-id="3d9e8-868">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-868">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="3d9e8-869">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="3d9e8-869">Return Value - left</span></span>

<span data-ttu-id="3d9e8-870">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-870">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="3d9e8-871">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-871">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="3d9e8-872">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-872">Parameters - leftMargin</span></span>

<span data-ttu-id="3d9e8-873">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-873">value</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-874">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-874">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="3d9e8-875">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-875">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="3d9e8-876">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-876">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="3d9e8-877">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-877">Parameters - leftMarginMode</span></span>

<span data-ttu-id="3d9e8-878">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-878">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="3d9e8-879">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-879">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="3d9e8-880">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-880">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="3d9e8-881">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-881">Parameters - leftMarginValue</span></span>

<span data-ttu-id="3d9e8-882">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-882">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="3d9e8-883">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-883">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="3d9e8-884">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-884">Method leftMode</span></span>

<span data-ttu-id="3d9e8-885">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-885">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="3d9e8-886">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-886">Parameters - leftMode</span></span>

<span data-ttu-id="3d9e8-887">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-887">value</span></span>  
<span data-ttu-id="3d9e8-888">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-888">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="3d9e8-889">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-889">Return Value - leftMode</span></span>

<span data-ttu-id="3d9e8-890">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-890">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="3d9e8-891">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-891">Method leftValue</span></span>

<span data-ttu-id="3d9e8-892">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-892">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="3d9e8-893">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-893">Parameters - leftValue</span></span>

<span data-ttu-id="3d9e8-894">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-894">value</span></span>  
<span data-ttu-id="3d9e8-895">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-895">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="3d9e8-896">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-896">Return Value - leftValue</span></span>

<span data-ttu-id="3d9e8-897">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-897">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="3d9e8-898">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="3d9e8-898">Method markAsUserAdd</span></span>

<span data-ttu-id="3d9e8-899">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-899">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="3d9e8-900">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="3d9e8-900">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="3d9e8-901">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-901">value</span></span>  
<span data-ttu-id="3d9e8-902">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-902">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="3d9e8-903">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="3d9e8-903">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="3d9e8-904">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-904">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="3d9e8-905">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="3d9e8-905">Method mouseDblClick</span></span>

<span data-ttu-id="3d9e8-906">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-906">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="3d9e8-907">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="3d9e8-907">Parameters - mouseDblClick</span></span>

<span data-ttu-id="3d9e8-908">x</span><span class="sxs-lookup"><span data-stu-id="3d9e8-908">x</span></span>  
<span data-ttu-id="3d9e8-909">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-909">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-910">y</span><span class="sxs-lookup"><span data-stu-id="3d9e8-910">y</span></span>  
<span data-ttu-id="3d9e8-911">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-911">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-912">ボタン</span><span class="sxs-lookup"><span data-stu-id="3d9e8-912">button</span></span>  
<span data-ttu-id="3d9e8-913">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-913">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-914">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-914">Ctrl</span></span>  
<span data-ttu-id="3d9e8-915">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-915">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-916">シフト</span><span class="sxs-lookup"><span data-stu-id="3d9e8-916">Shift</span></span>  
<span data-ttu-id="3d9e8-917">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-917">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="3d9e8-918">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="3d9e8-918">Return Value - mouseDblClick</span></span>

<span data-ttu-id="3d9e8-919">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-919">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="3d9e8-920">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="3d9e8-920">Remarks - mouseDblClick</span></span>

<span data-ttu-id="3d9e8-921">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-921">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="3d9e8-922">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="3d9e8-922">Method mouseDown</span></span>

<span data-ttu-id="3d9e8-923">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-923">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="3d9e8-924">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="3d9e8-924">Parameters - mouseDown</span></span>

<span data-ttu-id="3d9e8-925">x</span><span class="sxs-lookup"><span data-stu-id="3d9e8-925">x</span></span>  
<span data-ttu-id="3d9e8-926">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-926">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-927">y</span><span class="sxs-lookup"><span data-stu-id="3d9e8-927">y</span></span>  
<span data-ttu-id="3d9e8-928">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-928">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-929">ボタン</span><span class="sxs-lookup"><span data-stu-id="3d9e8-929">button</span></span>  
<span data-ttu-id="3d9e8-930">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-930">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-931">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-931">Ctrl</span></span>  
<span data-ttu-id="3d9e8-932">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-932">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-933">シフト</span><span class="sxs-lookup"><span data-stu-id="3d9e8-933">Shift</span></span>  
<span data-ttu-id="3d9e8-934">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-934">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="3d9e8-935">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="3d9e8-935">Return Value - mouseDown</span></span>

<span data-ttu-id="3d9e8-936">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-936">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="3d9e8-937">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="3d9e8-937">Remarks - mouseDown</span></span>

<span data-ttu-id="3d9e8-938">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-938">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="3d9e8-939">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-939">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="3d9e8-940">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="3d9e8-940">Method mouseMove</span></span>

<span data-ttu-id="3d9e8-941">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-941">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="3d9e8-942">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="3d9e8-942">Parameters - mouseMove</span></span>

<span data-ttu-id="3d9e8-943">x</span><span class="sxs-lookup"><span data-stu-id="3d9e8-943">x</span></span>  
<span data-ttu-id="3d9e8-944">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-944">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-945">y</span><span class="sxs-lookup"><span data-stu-id="3d9e8-945">y</span></span>  
<span data-ttu-id="3d9e8-946">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-946">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-947">ボタン</span><span class="sxs-lookup"><span data-stu-id="3d9e8-947">button</span></span>  
<span data-ttu-id="3d9e8-948">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-948">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-949">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-949">Ctrl</span></span>  
<span data-ttu-id="3d9e8-950">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-950">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-951">シフト</span><span class="sxs-lookup"><span data-stu-id="3d9e8-951">Shift</span></span>  
<span data-ttu-id="3d9e8-952">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-952">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="3d9e8-953">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="3d9e8-953">Return Value - mouseMove</span></span>

<span data-ttu-id="3d9e8-954">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-954">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="3d9e8-955">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="3d9e8-955">Remarks - mouseMove</span></span>

<span data-ttu-id="3d9e8-956">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-956">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="3d9e8-957">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="3d9e8-957">Method mouseUp</span></span>

<span data-ttu-id="3d9e8-958">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-958">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="3d9e8-959">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="3d9e8-959">Parameters - mouseUp</span></span>

<span data-ttu-id="3d9e8-960">x</span><span class="sxs-lookup"><span data-stu-id="3d9e8-960">x</span></span>  
<span data-ttu-id="3d9e8-961">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-961">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-962">y</span><span class="sxs-lookup"><span data-stu-id="3d9e8-962">y</span></span>  
<span data-ttu-id="3d9e8-963">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-963">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-964">ボタン</span><span class="sxs-lookup"><span data-stu-id="3d9e8-964">button</span></span>  
<span data-ttu-id="3d9e8-965">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-965">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-966">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-966">Ctrl</span></span>  
<span data-ttu-id="3d9e8-967">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-967">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-968">シフト</span><span class="sxs-lookup"><span data-stu-id="3d9e8-968">Shift</span></span>  
<span data-ttu-id="3d9e8-969">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-969">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="3d9e8-970">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="3d9e8-970">Return Value - mouseUp</span></span>

<span data-ttu-id="3d9e8-971">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-971">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="3d9e8-972">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="3d9e8-972">Remarks - mouseUp</span></span>

<span data-ttu-id="3d9e8-973">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-973">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="3d9e8-974">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-974">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="3d9e8-975">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-975">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="3d9e8-976">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-976">Parameters - moveControl</span></span>

<span data-ttu-id="3d9e8-977">controlId</span><span class="sxs-lookup"><span data-stu-id="3d9e8-977">controlId</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-978">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="3d9e8-978">insertAfterId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="3d9e8-979">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-979">Return Value - moveControl</span></span>

## <a name="method-name"></a><span data-ttu-id="3d9e8-980">メソッド名</span><span class="sxs-lookup"><span data-stu-id="3d9e8-980">Method name</span></span>

<span data-ttu-id="3d9e8-981">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-981">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="3d9e8-982">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="3d9e8-982">Parameters - name</span></span>

<span data-ttu-id="3d9e8-983">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-983">value</span></span>  
<span data-ttu-id="3d9e8-984">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-984">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="3d9e8-985">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="3d9e8-985">Return Value - name</span></span>

<span data-ttu-id="3d9e8-986">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-986">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="3d9e8-987">備考 - name</span><span class="sxs-lookup"><span data-stu-id="3d9e8-987">Remarks - name</span></span>

<span data-ttu-id="3d9e8-988">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-988">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="3d9e8-989">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-989">It must begin with a letter.</span></span>
-   <span data-ttu-id="3d9e8-990">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-990">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="3d9e8-991">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-991">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="3d9e8-992">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-992">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="3d9e8-993">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-993">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="3d9e8-994">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="3d9e8-994">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="3d9e8-995">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="3d9e8-995">Parameters - neededPermission</span></span>

<span data-ttu-id="3d9e8-996">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-996">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="3d9e8-997">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="3d9e8-997">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="3d9e8-998">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="3d9e8-998">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="3d9e8-999">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="3d9e8-999">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="3d9e8-1000">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1000">Method parentControl</span></span>

<span data-ttu-id="3d9e8-1001">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1001">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="3d9e8-1002">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1002">Return Value - parentControl</span></span>

<span data-ttu-id="3d9e8-1003">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1003">The parent control for the control.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="3d9e8-1004">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1004">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="3d9e8-1005">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1005">Parameters - rightMargin</span></span>

<span data-ttu-id="3d9e8-1006">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1006">value</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-1007">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1007">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="3d9e8-1008">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1008">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="3d9e8-1009">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1009">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="3d9e8-1010">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1010">Parameters - rightMarginMode</span></span>

<span data-ttu-id="3d9e8-1011">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1011">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="3d9e8-1012">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1012">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="3d9e8-1013">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1013">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="3d9e8-1014">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1014">Parameters - rightMarginValue</span></span>

<span data-ttu-id="3d9e8-1015">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1015">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="3d9e8-1016">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1016">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="3d9e8-1017">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1017">Method securityKey</span></span>

<span data-ttu-id="3d9e8-1018">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1018">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="3d9e8-1019">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1019">Parameters - securityKey</span></span>

<span data-ttu-id="3d9e8-1020">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1020">value</span></span>  
<span data-ttu-id="3d9e8-1021">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1021">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="3d9e8-1022">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1022">Return Value - securityKey</span></span>

<span data-ttu-id="3d9e8-1023">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1023">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="3d9e8-1024">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1024">Method showContextMenu</span></span>

<span data-ttu-id="3d9e8-1025">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1025">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="3d9e8-1026">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1026">Parameters - showContextMenu</span></span>

<span data-ttu-id="3d9e8-1027">menuHandle</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1027">menuHandle</span></span>  
<span data-ttu-id="3d9e8-1028">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1028">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="3d9e8-1029">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1029">Return Value - showContextMenu</span></span>

<span data-ttu-id="3d9e8-1030">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1030">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="3d9e8-1031">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1031">Method skip</span></span>

<span data-ttu-id="3d9e8-1032">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1032">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="3d9e8-1033">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1033">Parameters - skip</span></span>

<span data-ttu-id="3d9e8-1034">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1034">value</span></span>  
<span data-ttu-id="3d9e8-1035">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1035">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="3d9e8-1036">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1036">Return Value - skip</span></span>

<span data-ttu-id="3d9e8-1037">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1037">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="3d9e8-1038">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1038">Remarks - skip</span></span>

<span data-ttu-id="3d9e8-1039">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1039">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="3d9e8-1040">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1040">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="3d9e8-1041">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1041">Parameters - sort</span></span>

<span data-ttu-id="3d9e8-1042">sortDirection</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1042">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="3d9e8-1043">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1043">Return Value - sort</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="3d9e8-1044">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1044">Method toolTip</span></span>

<span data-ttu-id="3d9e8-1045">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1045">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="3d9e8-1046">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1046">Return Value - toolTip</span></span>

<span data-ttu-id="3d9e8-1047">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1047">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="3d9e8-1048">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1048">Remarks - toolTip</span></span>

<span data-ttu-id="3d9e8-1049">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1049">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="3d9e8-1050">メソッド top</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1050">Method top</span></span>

<span data-ttu-id="3d9e8-1051">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1051">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="3d9e8-1052">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1052">Parameters - top</span></span>

<span data-ttu-id="3d9e8-1053">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1053">value</span></span>  
<span data-ttu-id="3d9e8-1054">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1054">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1055">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1055">mode</span></span>  
<span data-ttu-id="3d9e8-1056">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1056">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="3d9e8-1057">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1057">Return Value - top</span></span>

<span data-ttu-id="3d9e8-1058">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1058">The vertical position of the control in the form.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="3d9e8-1059">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1059">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="3d9e8-1060">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1060">Parameters - topMargin</span></span>

<span data-ttu-id="3d9e8-1061">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1061">value</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-1062">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1062">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="3d9e8-1063">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1063">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="3d9e8-1064">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1064">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="3d9e8-1065">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1065">Parameters - topMarginMode</span></span>

<span data-ttu-id="3d9e8-1066">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1066">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="3d9e8-1067">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1067">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="3d9e8-1068">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1068">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="3d9e8-1069">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1069">Parameters - topMarginValue</span></span>

<span data-ttu-id="3d9e8-1070">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1070">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="3d9e8-1071">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1071">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="3d9e8-1072">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1072">Method topMode</span></span>

<span data-ttu-id="3d9e8-1073">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1073">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="3d9e8-1074">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1074">Parameters - topMode</span></span>

<span data-ttu-id="3d9e8-1075">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1075">value</span></span>  
<span data-ttu-id="3d9e8-1076">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1076">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="3d9e8-1077">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1077">Return Value - topMode</span></span>

<span data-ttu-id="3d9e8-1078">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1078">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="3d9e8-1079">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1079">Method topValue</span></span>

<span data-ttu-id="3d9e8-1080">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1080">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="3d9e8-1081">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1081">Parameters - topValue</span></span>

<span data-ttu-id="3d9e8-1082">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1082">value</span></span>  
<span data-ttu-id="3d9e8-1083">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1083">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="3d9e8-1084">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1084">Return Value - topValue</span></span>

<span data-ttu-id="3d9e8-1085">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1085">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="3d9e8-1086">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1086">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="3d9e8-1087">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1087">Parameters - type</span></span>

<span data-ttu-id="3d9e8-1088">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1088">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="3d9e8-1089">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1089">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="3d9e8-1090">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1090">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="3d9e8-1091">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1091">Parameters - underline</span></span>

<span data-ttu-id="3d9e8-1092">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1092">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="3d9e8-1093">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1093">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="3d9e8-1094">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1094">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="3d9e8-1095">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1095">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="3d9e8-1096">データ</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1096">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="3d9e8-1097">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1097">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="3d9e8-1098">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1098">Method userData</span></span>

<span data-ttu-id="3d9e8-1099">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1099">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="3d9e8-1100">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1100">Parameters - userData</span></span>

<span data-ttu-id="3d9e8-1101">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1101">value</span></span>  
<span data-ttu-id="3d9e8-1102">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1102">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="3d9e8-1103">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1103">Return Value - userData</span></span>

<span data-ttu-id="3d9e8-1104">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1104">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="3d9e8-1105">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1105">Method userDataItem</span></span>

<span data-ttu-id="3d9e8-1106">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1106">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="3d9e8-1107">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1107">Parameters - userDataItem</span></span>

<span data-ttu-id="3d9e8-1108">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1108">value</span></span>  
<span data-ttu-id="3d9e8-1109">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1109">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="3d9e8-1110">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1110">Return Value - userDataItem</span></span>

<span data-ttu-id="3d9e8-1111">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1111">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="3d9e8-1112">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1112">Method userDataItems</span></span>

<span data-ttu-id="3d9e8-1113">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1113">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="3d9e8-1114">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1114">Parameters - userDataItems</span></span>

<span data-ttu-id="3d9e8-1115">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1115">value</span></span>  
<span data-ttu-id="3d9e8-1116">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1116">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="3d9e8-1117">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1117">Return Value - userDataItems</span></span>

<span data-ttu-id="3d9e8-1118">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1118">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="3d9e8-1119">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1119">Method userDisable</span></span>

<span data-ttu-id="3d9e8-1120">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1120">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="3d9e8-1121">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1121">Parameters - userDisable</span></span>

<span data-ttu-id="3d9e8-1122">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1122">value</span></span>  
<span data-ttu-id="3d9e8-1123">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1123">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="3d9e8-1124">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1124">Return Value - userDisable</span></span>

<span data-ttu-id="3d9e8-1125">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1125">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="3d9e8-1126">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1126">Method userHeight</span></span>

<span data-ttu-id="3d9e8-1127">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1127">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="3d9e8-1128">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1128">Parameters - userHeight</span></span>

<span data-ttu-id="3d9e8-1129">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1129">value</span></span>  
<span data-ttu-id="3d9e8-1130">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1130">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="3d9e8-1131">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1131">Return Value - userHeight</span></span>

<span data-ttu-id="3d9e8-1132">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1132">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="3d9e8-1133">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1133">Method userHide</span></span>

<span data-ttu-id="3d9e8-1134">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1134">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="3d9e8-1135">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1135">Parameters - userHide</span></span>

<span data-ttu-id="3d9e8-1136">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1136">value</span></span>  
<span data-ttu-id="3d9e8-1137">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1137">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="3d9e8-1138">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1138">Return Value - userHide</span></span>

<span data-ttu-id="3d9e8-1139">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1139">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="3d9e8-1140">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1140">Remarks - userHide</span></span>

<span data-ttu-id="3d9e8-1141">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1141">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="3d9e8-1142">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1142">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="3d9e8-1143">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1143">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="3d9e8-1144">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1144">Method userOrgContainer</span></span>

<span data-ttu-id="3d9e8-1145">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1145">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="3d9e8-1146">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1146">Parameters - userOrgContainer</span></span>

<span data-ttu-id="3d9e8-1147">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1147">value</span></span>  
<span data-ttu-id="3d9e8-1148">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1148">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="3d9e8-1149">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1149">Return Value - userOrgContainer</span></span>

<span data-ttu-id="3d9e8-1150">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1150">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="3d9e8-1151">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1151">Method userOrgSibling</span></span>

<span data-ttu-id="3d9e8-1152">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1152">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="3d9e8-1153">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1153">Parameters - userOrgSibling</span></span>

<span data-ttu-id="3d9e8-1154">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1154">value</span></span>  
<span data-ttu-id="3d9e8-1155">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1155">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="3d9e8-1156">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1156">Return Value - userOrgSibling</span></span>

<span data-ttu-id="3d9e8-1157">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1157">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="3d9e8-1158">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1158">Method userPromptText</span></span>

<span data-ttu-id="3d9e8-1159">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1159">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="3d9e8-1160">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1160">Parameters - userPromptText</span></span>

<span data-ttu-id="3d9e8-1161">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1161">value</span></span>  
<span data-ttu-id="3d9e8-1162">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1162">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="3d9e8-1163">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1163">Return Value - userPromptText</span></span>

<span data-ttu-id="3d9e8-1164">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1164">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="3d9e8-1165">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1165">Method userSecurityLevel</span></span>

<span data-ttu-id="3d9e8-1166">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1166">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="3d9e8-1167">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1167">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="3d9e8-1168">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1168">value</span></span>  
<span data-ttu-id="3d9e8-1169">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1169">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="3d9e8-1170">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1170">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="3d9e8-1171">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1171">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="3d9e8-1172">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1172">Method userSkip</span></span>

<span data-ttu-id="3d9e8-1173">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1173">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="3d9e8-1174">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1174">Parameters - userSkip</span></span>

<span data-ttu-id="3d9e8-1175">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1175">value</span></span>  
<span data-ttu-id="3d9e8-1176">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1176">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="3d9e8-1177">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1177">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="3d9e8-1178">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1178">Return Value - userSkip</span></span>

<span data-ttu-id="3d9e8-1179">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1179">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="3d9e8-1180">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1180">Method userWidth</span></span>

<span data-ttu-id="3d9e8-1181">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1181">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="3d9e8-1182">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1182">Parameters - userWidth</span></span>

<span data-ttu-id="3d9e8-1183">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1183">value</span></span>  
<span data-ttu-id="3d9e8-1184">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1184">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="3d9e8-1185">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1185">Return Value - userWidth</span></span>

<span data-ttu-id="3d9e8-1186">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1186">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="3d9e8-1187">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1187">Remarks - userWidth</span></span>

<span data-ttu-id="3d9e8-1188">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1188">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="3d9e8-1189">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1189">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="3d9e8-1190">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1190">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="3d9e8-1191">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1191">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="3d9e8-1192">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1192">Parameters - useUserLayout</span></span>

<span data-ttu-id="3d9e8-1193">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1193">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="3d9e8-1194">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1194">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="3d9e8-1195">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1195">Method verticalSpacing</span></span>

<span data-ttu-id="3d9e8-1196">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1196">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="3d9e8-1197">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1197">Parameters - verticalSpacing</span></span>

<span data-ttu-id="3d9e8-1198">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1198">value</span></span>  
<span data-ttu-id="3d9e8-1199">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1199">An integer value that indicates the AutoMode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1200">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1200">mode</span></span>  
<span data-ttu-id="3d9e8-1201">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1201">An integer value that indicates the AutoMode for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="3d9e8-1202">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1202">Return Value - verticalSpacing</span></span>

<span data-ttu-id="3d9e8-1203">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1203">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="3d9e8-1204">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1204">Method verticalSpacingMode</span></span>

<span data-ttu-id="3d9e8-1205">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1205">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="3d9e8-1206">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1206">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="3d9e8-1207">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1207">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="3d9e8-1208">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1208">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="3d9e8-1209">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1209">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="3d9e8-1210">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1210">Method verticalSpacingValue</span></span>

<span data-ttu-id="3d9e8-1211">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1211">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="3d9e8-1212">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1212">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="3d9e8-1213">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1213">value</span></span>  
<span data-ttu-id="3d9e8-1214">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1214">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="3d9e8-1215">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1215">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="3d9e8-1216">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1216">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="3d9e8-1217">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1217">Method visible</span></span>

<span data-ttu-id="3d9e8-1218">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1218">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="3d9e8-1219">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1219">Parameters - visible</span></span>

<span data-ttu-id="3d9e8-1220">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1220">value</span></span>  
<span data-ttu-id="3d9e8-1221">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1221">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="3d9e8-1222">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1222">Return Value - visible</span></span>

<span data-ttu-id="3d9e8-1223">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1223">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="3d9e8-1224">メソッド width</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1224">Method width</span></span>

<span data-ttu-id="3d9e8-1225">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1225">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="3d9e8-1226">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1226">Parameters - width</span></span>

<span data-ttu-id="3d9e8-1227">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1227">value</span></span>  
<span data-ttu-id="3d9e8-1228">幅の計算方法を示す整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1228">An integer data type that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1229">モード</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1229">mode</span></span>  
<span data-ttu-id="3d9e8-1230">幅の計算方法を示す整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1230">An integer data type that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="3d9e8-1231">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1231">Return Value - width</span></span>

<span data-ttu-id="3d9e8-1232">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1232">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="3d9e8-1233">備考 - width</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1233">Remarks - width</span></span>

<span data-ttu-id="3d9e8-1234">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1234">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="3d9e8-1235">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1235">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="3d9e8-1236">モード。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1236">Mode.</span></span>           | <span data-ttu-id="3d9e8-1237">幅計算。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1237">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d9e8-1238">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1238">-1 Exact.</span></span>       | <span data-ttu-id="3d9e8-1239">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1239">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3d9e8-1240">0 自動。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1240">0 Auto.</span></span>         | <span data-ttu-id="3d9e8-1241">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1241">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3d9e8-1242">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1242">1 Column width.</span></span> | <span data-ttu-id="3d9e8-1243">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1243">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="3d9e8-1244">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1244">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="3d9e8-1245">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1245">Method widthMode</span></span>

<span data-ttu-id="3d9e8-1246">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1246">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="3d9e8-1247">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1247">Parameters - widthMode</span></span>

<span data-ttu-id="3d9e8-1248">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1248">value</span></span>  
<span data-ttu-id="3d9e8-1249">コントロールの幅の計算方法を示す整数データ型値。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1249">An integer data type value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="3d9e8-1250">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1250">Return Value - widthMode</span></span>

<span data-ttu-id="3d9e8-1251">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1251">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="3d9e8-1252">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1252">Remarks - widthMode</span></span>

<span data-ttu-id="3d9e8-1253">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1253">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="3d9e8-1254">モード。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1254">Mode.</span></span>         | <span data-ttu-id="3d9e8-1255">幅計算。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1255">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d9e8-1256">正確。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1256">Exact.</span></span>        | <span data-ttu-id="3d9e8-1257">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1257">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="3d9e8-1258">自動。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1258">Auto.</span></span>         | <span data-ttu-id="3d9e8-1259">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1259">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="3d9e8-1260">列の幅。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1260">Column width.</span></span> | <span data-ttu-id="3d9e8-1261">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1261">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="3d9e8-1262">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1262">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="3d9e8-1263">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1263">Method widthValue</span></span>

<span data-ttu-id="3d9e8-1264">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1264">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="3d9e8-1265">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1265">Parameters - widthValue</span></span>

<span data-ttu-id="3d9e8-1266">値</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1266">value</span></span>  
<span data-ttu-id="3d9e8-1267">幅をピクセル単位で指定する整数データ型。オプション。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1267">An integer data type that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="3d9e8-1268">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1268">Return Value - widthValue</span></span>

<span data-ttu-id="3d9e8-1269">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1269">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="3d9e8-1270">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1270">Remarks - widthValue</span></span>

<span data-ttu-id="3d9e8-1271">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1271">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-filter"></a><span data-ttu-id="3d9e8-1272">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1272">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="3d9e8-1273">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1273">Parameters - filter</span></span>

<span data-ttu-id="3d9e8-1274">filterStr</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1274">filterStr</span></span>  

## <a name="method-onleaving"></a><span data-ttu-id="3d9e8-1275">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1275">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="3d9e8-1276">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1276">Parameters - OnLeaving</span></span>

<span data-ttu-id="3d9e8-1277">sender</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1277">sender</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-1278">e</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1278">e</span></span>  

## <a name="method-jumpref"></a><span data-ttu-id="3d9e8-1279">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1279">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="3d9e8-1280">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1280">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="3d9e8-1281">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1281">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="3d9e8-1282">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1282">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-1283">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1283">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-1284">overrideObject</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1284">overrideObject</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="3d9e8-1285">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1285">Method gotFocus</span></span>

<span data-ttu-id="3d9e8-1286">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1286">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="3d9e8-1287">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1287">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="3d9e8-1288">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1288">Parameters - OnGotFocus</span></span>

<span data-ttu-id="3d9e8-1289">sender</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1289">sender</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-1290">e</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1290">e</span></span>  

## <a name="method-setfocus"></a><span data-ttu-id="3d9e8-1291">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1291">Method setFocus</span></span>

<span data-ttu-id="3d9e8-1292">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1292">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-mouseenter"></a><span data-ttu-id="3d9e8-1293">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1293">Method mouseEnter</span></span>

<span data-ttu-id="3d9e8-1294">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1294">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="3d9e8-1295">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1295">Parameters - mouseEnter</span></span>

<span data-ttu-id="3d9e8-1296">x</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1296">x</span></span>  
<span data-ttu-id="3d9e8-1297">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1297">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1298">y</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1298">y</span></span>  
<span data-ttu-id="3d9e8-1299">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1299">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1300">ボタン</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1300">button</span></span>  
<span data-ttu-id="3d9e8-1301">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1301">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1302">Ctrl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1302">Ctrl</span></span>  
<span data-ttu-id="3d9e8-1303">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1303">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1304">シフト</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1304">Shift</span></span>  
<span data-ttu-id="3d9e8-1305">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1305">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-arrange"></a><span data-ttu-id="3d9e8-1306">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1306">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-enddrag"></a><span data-ttu-id="3d9e8-1307">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1307">Method endDrag</span></span>

<span data-ttu-id="3d9e8-1308">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1308">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="3d9e8-1309">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1309">Remarks - endDrag</span></span>

<span data-ttu-id="3d9e8-1310">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1310">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="3d9e8-1311">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1311">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-paste"></a><span data-ttu-id="3d9e8-1312">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1312">Method paste</span></span>

<span data-ttu-id="3d9e8-1313">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1313">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-drop"></a><span data-ttu-id="3d9e8-1314">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1314">Method drop</span></span>

<span data-ttu-id="3d9e8-1315">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1315">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="3d9e8-1316">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1316">Parameters - drop</span></span>

<span data-ttu-id="3d9e8-1317">dragSource</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1317">dragSource</span></span>  
<span data-ttu-id="3d9e8-1318">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1318">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1319">dragMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1319">dragMode</span></span>  
<span data-ttu-id="3d9e8-1320">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1320">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1321">x</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1321">x</span></span>  
<span data-ttu-id="3d9e8-1322">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1322">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1323">y</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1323">y</span></span>  
<span data-ttu-id="3d9e8-1324">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1324">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="3d9e8-1325">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1325">Method resetUserSetting</span></span>

<span data-ttu-id="3d9e8-1326">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1326">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="3d9e8-1327">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1327">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="3d9e8-1328">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1328">Parameters - OnLostFocus</span></span>

<span data-ttu-id="3d9e8-1329">sender</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1329">sender</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-1330">e</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1330">e</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="3d9e8-1331">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1331">Method mouseLeave</span></span>

<span data-ttu-id="3d9e8-1332">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1332">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-dropex"></a><span data-ttu-id="3d9e8-1333">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1333">Method dropEx</span></span>

<span data-ttu-id="3d9e8-1334">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1334">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="3d9e8-1335">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1335">Parameters - dropEx</span></span>

<span data-ttu-id="3d9e8-1336">dragSource</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1336">dragSource</span></span>  
<span data-ttu-id="3d9e8-1337">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1337">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1338">dragMode</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1338">dragMode</span></span>  
<span data-ttu-id="3d9e8-1339">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1339">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1340">x</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1340">x</span></span>  
<span data-ttu-id="3d9e8-1341">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1341">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1342">y</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1342">y</span></span>  
<span data-ttu-id="3d9e8-1343">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1343">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-prefcolumnsize"></a><span data-ttu-id="3d9e8-1344">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1344">Method prefColumnSize</span></span>

<span data-ttu-id="3d9e8-1345">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1345">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="3d9e8-1346">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1346">Parameters - prefColumnSize</span></span>

<span data-ttu-id="3d9e8-1347">width</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1347">width</span></span>  
<span data-ttu-id="3d9e8-1348">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1348">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="3d9e8-1349">height</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1349">height</span></span>  
<span data-ttu-id="3d9e8-1350">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1350">The preferred height of the control.</span></span>

## <a name="method-copy"></a><span data-ttu-id="3d9e8-1351">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1351">Method copy</span></span>

<span data-ttu-id="3d9e8-1352">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1352">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-enter"></a><span data-ttu-id="3d9e8-1353">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1353">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-onenter"></a><span data-ttu-id="3d9e8-1354">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1354">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="3d9e8-1355">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1355">Parameters - OnEnter</span></span>

<span data-ttu-id="3d9e8-1356">sender</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1356">sender</span></span>  

<!-- -->

<span data-ttu-id="3d9e8-1357">e</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1357">e</span></span>  

## <a name="method-context"></a><span data-ttu-id="3d9e8-1358">メソッド context</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1358">Method context</span></span>

<span data-ttu-id="3d9e8-1359">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1359">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="3d9e8-1360">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1360">Method displayControl</span></span>

<span data-ttu-id="3d9e8-1361">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1361">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-cut"></a><span data-ttu-id="3d9e8-1362">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1362">Method cut</span></span>

<span data-ttu-id="3d9e8-1363">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1363">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-lostfocus"></a><span data-ttu-id="3d9e8-1364">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1364">Method lostFocus</span></span>

<span data-ttu-id="3d9e8-1365">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1365">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-dragleave"></a><span data-ttu-id="3d9e8-1366">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1366">Method dragLeave</span></span>

<span data-ttu-id="3d9e8-1367">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1367">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-inputsearch"></a><span data-ttu-id="3d9e8-1368">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1368">Method inputSearch</span></span>

<span data-ttu-id="3d9e8-1369">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1369">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="3d9e8-1370">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1370">Parameters - inputSearch</span></span>

<span data-ttu-id="3d9e8-1371">searchStr</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1371">searchStr</span></span>  
<span data-ttu-id="3d9e8-1372">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3d9e8-1372">The string value to use to filter data; optional.</span></span>



