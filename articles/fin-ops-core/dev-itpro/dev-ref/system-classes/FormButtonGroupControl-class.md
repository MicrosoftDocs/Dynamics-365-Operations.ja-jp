---
title: FormButtonGroupControl クラス
description: このトピックでは、FormButtonGroupControl クラスについて説明します。
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
ms.openlocfilehash: d7daac4fee42022e25b98714a186db2e3ed41fd9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502954"
---
# <a name="class-formbuttongroupcontrol"></a><span data-ttu-id="08cf0-103">クラス FormButtonGroupControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-103">Class FormButtonGroupControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormButtonGroupControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="08cf0-104">備考</span><span class="sxs-lookup"><span data-stu-id="08cf0-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="08cf0-105">例</span><span class="sxs-lookup"><span data-stu-id="08cf0-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="08cf0-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="08cf0-106">Methods</span></span>

| <span data-ttu-id="08cf0-107">方法</span><span class="sxs-lookup"><span data-stu-id="08cf0-107">Method</span></span>                                                                                                              | <span data-ttu-id="08cf0-108">説明</span><span class="sxs-lookup"><span data-stu-id="08cf0-108">Description</span></span>                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08cf0-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-112">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-112">public boolean alignChild(\[boolean value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-113">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-113">public boolean alignChildren(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-114">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-114">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="08cf0-115">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-115">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="08cf0-116">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-116">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="08cf0-117">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-117">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="08cf0-118">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="08cf0-118">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="08cf0-119">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-119">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="08cf0-120">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-120">public int allowUserSetup(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-121">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-121">public int arrangeGuide(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-122">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-122">public int arrangeMethod(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-123">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-123">public int arrangeWhen(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-124">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-124">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="08cf0-125">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-125">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="08cf0-126">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-126">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="08cf0-127">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-127">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="08cf0-128">public Image backgroundImage(\[Image image\], \[int drawMode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-128">public Image backgroundImage(\[Image image\], \[int drawMode\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-129">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-129">public int backStyle(\[int value\])</span></span>                                                                                 | <span data-ttu-id="08cf0-130">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-130">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="08cf0-131">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="08cf0-131">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="08cf0-132">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-132">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="08cf0-133">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-133">public int bold(\[int value\])</span></span>                                                                                      | <span data-ttu-id="08cf0-134">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-134">Gets or sets the weight of font used to output text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="08cf0-135">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-135">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-136">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-136">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-137">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-137">public int bottomMarginValue(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-138">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="08cf0-138">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="08cf0-139">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-139">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="08cf0-140">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-140">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-141">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="08cf0-141">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-142">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-142">public str caption(\[str value\])</span></span>                                                                                   | <span data-ttu-id="08cf0-143">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-143">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="08cf0-144">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-144">public int characterSet(\[int value\])</span></span>                                                                              | <span data-ttu-id="08cf0-145">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-145">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="08cf0-146">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-146">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="08cf0-147">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-147">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="08cf0-148">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-148">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-149">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-149">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-150">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-150">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-151">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-151">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-152">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-152">public int columnspaceValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-153">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-153">public int columnsValue(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-154">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-154">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="08cf0-155">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-155">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="08cf0-156">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="08cf0-156">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="08cf0-157">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-157">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="08cf0-158">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="08cf0-158">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-159">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="08cf0-159">public int controlCount()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-160">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="08cf0-160">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-161">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-161">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="08cf0-162">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-162">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="08cf0-163">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-163">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-164">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-164">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="08cf0-165">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-165">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="08cf0-166">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-166">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="08cf0-167">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-167">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="08cf0-168">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-168">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="08cf0-169">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-169">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="08cf0-170">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-170">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="08cf0-171">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-171">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="08cf0-172">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="08cf0-172">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="08cf0-173">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-173">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="08cf0-174">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="08cf0-174">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="08cf0-175">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-175">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="08cf0-176">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="08cf0-176">public str dragText()</span></span>                                                                                               | <span data-ttu-id="08cf0-177">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-177">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="08cf0-178">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-178">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="08cf0-179">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-179">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="08cf0-180">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-180">public str font(\[str value\])</span></span>                                                                                      | <span data-ttu-id="08cf0-181">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-181">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="08cf0-182">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-182">public int fontSize(\[int value\])</span></span>                                                                                  | <span data-ttu-id="08cf0-183">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-183">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="08cf0-184">public int framePosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-184">public int framePosition(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-185">public int frameType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-185">public int frameType(\[int value\])</span></span>                                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-186">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-186">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="08cf0-187">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-187">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="08cf0-188">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="08cf0-188">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="08cf0-189">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-189">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="08cf0-190">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-190">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="08cf0-191">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-191">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="08cf0-192">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-192">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="08cf0-193">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-193">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="08cf0-194">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-194">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="08cf0-195">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-195">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="08cf0-196">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="08cf0-196">public str helpField()</span></span>                                                                                              | <span data-ttu-id="08cf0-197">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-197">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="08cf0-198">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-198">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="08cf0-199">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-199">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="08cf0-200">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-200">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-201">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-201">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="08cf0-202">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-202">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="08cf0-203">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="08cf0-203">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="08cf0-204">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-204">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="08cf0-205">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="08cf0-205">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-206">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="08cf0-206">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="08cf0-207">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-207">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="08cf0-208">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="08cf0-208">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="08cf0-209">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-209">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="08cf0-210">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="08cf0-210">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="08cf0-211">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-211">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="08cf0-212">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-212">public boolean italic(\[boolean value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-213">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-213">public str keyTip(\[str value\])</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-214">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-214">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="08cf0-215">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-215">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="08cf0-216">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-216">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-217">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-217">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-218">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-218">public int leftMarginValue(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-219">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-219">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="08cf0-220">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-220">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="08cf0-221">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-221">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="08cf0-222">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-222">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="08cf0-223">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-223">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="08cf0-224">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="08cf0-224">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="08cf0-225">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="08cf0-225">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="08cf0-226">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-226">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="08cf0-227">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="08cf0-227">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="08cf0-228">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-228">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="08cf0-229">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="08cf0-229">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="08cf0-230">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-230">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="08cf0-231">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="08cf0-231">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="08cf0-232">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-232">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="08cf0-233">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-233">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-234">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-234">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="08cf0-235">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-235">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="08cf0-236">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-236">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-237">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="08cf0-237">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-238">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="08cf0-238">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="08cf0-239">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-239">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="08cf0-240">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-240">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-241">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-241">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-242">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-242">public int rightMarginValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-243">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-243">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="08cf0-244">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-244">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="08cf0-245">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="08cf0-245">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="08cf0-246">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-246">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="08cf0-247">public boolean sizeHeight(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-247">public boolean sizeHeight(\[boolean value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-248">public boolean sizeWidth(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-248">public boolean sizeWidth(\[boolean value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-249">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-249">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="08cf0-250">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-250">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="08cf0-251">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-251">public int sort(\[SortOrder sortDirection\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-252">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-252">public int style(\[int value\])</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-253">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="08cf0-253">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="08cf0-254">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-254">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="08cf0-255">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-255">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="08cf0-256">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-256">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="08cf0-257">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-257">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-258">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-258">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-259">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-259">public int topMarginValue(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-260">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-260">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="08cf0-261">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-261">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="08cf0-262">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-262">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="08cf0-263">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-263">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="08cf0-264">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-264">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-265">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-265">public boolean underline(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="08cf0-266">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-266">Sets or returns the underline property for the text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="08cf0-267">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="08cf0-267">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-268">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-268">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="08cf0-269">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-269">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="08cf0-270">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-270">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="08cf0-271">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-271">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="08cf0-272">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-272">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="08cf0-273">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-273">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="08cf0-274">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-274">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="08cf0-275">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-275">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="08cf0-276">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-276">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="08cf0-277">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-277">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="08cf0-278">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-278">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="08cf0-279">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-279">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="08cf0-280">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-280">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="08cf0-281">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-281">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="08cf0-282">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-282">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="08cf0-283">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-283">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="08cf0-284">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-284">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="08cf0-285">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-285">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="08cf0-286">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-286">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="08cf0-287">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-287">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="08cf0-288">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-288">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="08cf0-289">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-289">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls on the form.</span></span>                    |
| <span data-ttu-id="08cf0-290">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-290">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="08cf0-291">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-291">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="08cf0-292">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-292">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-293">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-293">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="08cf0-294">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-294">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="08cf0-295">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-295">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="08cf0-296">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-296">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="08cf0-297">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-297">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="08cf0-298">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-298">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="08cf0-299">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-299">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="08cf0-300">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-300">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="08cf0-301">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-301">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="08cf0-302">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-302">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="08cf0-303">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-303">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="08cf0-304">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-304">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="08cf0-305">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-305">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="08cf0-306">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-306">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="08cf0-307">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="08cf0-307">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="08cf0-308">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="08cf0-308">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="08cf0-309">public void cut()</span><span class="sxs-lookup"><span data-stu-id="08cf0-309">public void cut()</span></span>                                                                                                   | <span data-ttu-id="08cf0-310">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="08cf0-310">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="08cf0-311">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-311">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-312">public void copy()</span><span class="sxs-lookup"><span data-stu-id="08cf0-312">public void copy()</span></span>                                                                                                  | <span data-ttu-id="08cf0-313">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="08cf0-313">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="08cf0-314">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="08cf0-314">public void arrange()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-315">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="08cf0-315">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="08cf0-316">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-316">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="08cf0-317">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="08cf0-317">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="08cf0-318">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-318">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="08cf0-319">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="08cf0-319">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="08cf0-320">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-320">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="08cf0-321">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="08cf0-321">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="08cf0-322">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-322">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="08cf0-323">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="08cf0-323">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="08cf0-324">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-324">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="08cf0-325">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="08cf0-325">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="08cf0-326">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-326">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="08cf0-327">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="08cf0-327">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="08cf0-328">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-328">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="08cf0-329">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="08cf0-329">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="08cf0-330">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-330">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="08cf0-331">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-331">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-332">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="08cf0-332">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="08cf0-333">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-333">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="08cf0-334">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-334">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-335">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="08cf0-335">public void jumpRef()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-336">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="08cf0-336">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="08cf0-337">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-337">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="08cf0-338">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="08cf0-338">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="08cf0-339">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-339">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="08cf0-340">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="08cf0-340">public void filter(\[str filterStr\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="08cf0-341">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="08cf0-341">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="08cf0-342">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-342">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="08cf0-343">public void paste()</span><span class="sxs-lookup"><span data-stu-id="08cf0-343">public void paste()</span></span>                                                                                                 | <span data-ttu-id="08cf0-344">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-344">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="08cf0-345">public void context()</span><span class="sxs-lookup"><span data-stu-id="08cf0-345">public void context()</span></span>                                                                                               | <span data-ttu-id="08cf0-346">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-346">Shows the shortcut menu for the control.</span></span>                                                                                                                                |

## <a name="method-addcontrol"></a><span data-ttu-id="08cf0-347">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-347">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="08cf0-348">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-348">Parameters - addControl</span></span>

<span data-ttu-id="08cf0-349">controlType</span><span class="sxs-lookup"><span data-stu-id="08cf0-349">controlType</span></span>  

<!-- -->

<span data-ttu-id="08cf0-350">controlName</span><span class="sxs-lookup"><span data-stu-id="08cf0-350">controlName</span></span>  

<!-- -->

<span data-ttu-id="08cf0-351">insertAfter</span><span class="sxs-lookup"><span data-stu-id="08cf0-351">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="08cf0-352">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-352">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="08cf0-353">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="08cf0-353">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="08cf0-354">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="08cf0-354">Parameters - addControlEx</span></span>

<span data-ttu-id="08cf0-355">controlClass</span><span class="sxs-lookup"><span data-stu-id="08cf0-355">controlClass</span></span>  

<!-- -->

<span data-ttu-id="08cf0-356">controlName</span><span class="sxs-lookup"><span data-stu-id="08cf0-356">controlName</span></span>  

<!-- -->

<span data-ttu-id="08cf0-357">insertAfter</span><span class="sxs-lookup"><span data-stu-id="08cf0-357">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="08cf0-358">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="08cf0-358">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="08cf0-359">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="08cf0-359">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="08cf0-360">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="08cf0-360">Parameters - addDataField</span></span>

<span data-ttu-id="08cf0-361">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="08cf0-361">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="08cf0-362">fieldId</span><span class="sxs-lookup"><span data-stu-id="08cf0-362">fieldId</span></span>  

<!-- -->

<span data-ttu-id="08cf0-363">insertAfter</span><span class="sxs-lookup"><span data-stu-id="08cf0-363">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="08cf0-364">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="08cf0-364">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="08cf0-365">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="08cf0-365">Return Value - addDataField</span></span>

## <a name="method-alignchild"></a><span data-ttu-id="08cf0-366">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="08cf0-366">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="08cf0-367">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="08cf0-367">Parameters - alignChild</span></span>

<span data-ttu-id="08cf0-368">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-368">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="08cf0-369">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="08cf0-369">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="08cf0-370">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="08cf0-370">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="08cf0-371">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="08cf0-371">Parameters - alignChildren</span></span>

<span data-ttu-id="08cf0-372">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-372">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="08cf0-373">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="08cf0-373">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="08cf0-374">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-374">Method alignControl</span></span>

<span data-ttu-id="08cf0-375">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-375">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="08cf0-376">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-376">Parameters - alignControl</span></span>

<span data-ttu-id="08cf0-377">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-377">value</span></span>  
<span data-ttu-id="08cf0-378">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-378">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="08cf0-379">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-379">Return Value - alignControl</span></span>

<span data-ttu-id="08cf0-380">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-380">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="08cf0-381">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-381">Remarks - alignControl</span></span>

<span data-ttu-id="08cf0-382">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-382">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="08cf0-383">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="08cf0-383">Method allowEdit</span></span>

<span data-ttu-id="08cf0-384">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-384">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="08cf0-385">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="08cf0-385">Parameters - allowEdit</span></span>

<span data-ttu-id="08cf0-386">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-386">value</span></span>  
<span data-ttu-id="08cf0-387">allowEdit プロパティに割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-387">The value to be assigned to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="08cf0-388">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="08cf0-388">Return Value - allowEdit</span></span>

<span data-ttu-id="08cf0-389">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-389">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="08cf0-390">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="08cf0-390">Remarks - allowEdit</span></span>

<span data-ttu-id="08cf0-391">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="08cf0-391">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="08cf0-392">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="08cf0-392">Method allowSysSetup</span></span>

<span data-ttu-id="08cf0-393">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-393">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="08cf0-394">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="08cf0-394">Return Value - allowSysSetup</span></span>

<span data-ttu-id="08cf0-395">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-395">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="08cf0-396">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="08cf0-396">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="08cf0-397">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="08cf0-397">Parameters - allowUserSetup</span></span>

<span data-ttu-id="08cf0-398">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-398">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="08cf0-399">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="08cf0-399">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="08cf0-400">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="08cf0-400">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="08cf0-401">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="08cf0-401">Parameters - arrangeGuide</span></span>

<span data-ttu-id="08cf0-402">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-402">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="08cf0-403">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="08cf0-403">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="08cf0-404">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="08cf0-404">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="08cf0-405">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="08cf0-405">Parameters - arrangeMethod</span></span>

<span data-ttu-id="08cf0-406">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-406">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="08cf0-407">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="08cf0-407">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="08cf0-408">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="08cf0-408">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="08cf0-409">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="08cf0-409">Parameters - arrangeWhen</span></span>

<span data-ttu-id="08cf0-410">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-410">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="08cf0-411">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="08cf0-411">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="08cf0-412">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="08cf0-412">Method autoDeclaration</span></span>

<span data-ttu-id="08cf0-413">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-413">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="08cf0-414">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="08cf0-414">Parameters - autoDeclaration</span></span>

<span data-ttu-id="08cf0-415">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-415">value</span></span>  
<span data-ttu-id="08cf0-416">指定されている場合、プロパティはこの値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-416">The property is set to this value, if supplied.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="08cf0-417">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="08cf0-417">Return Value - autoDeclaration</span></span>

<span data-ttu-id="08cf0-418">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-418">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="08cf0-419">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="08cf0-419">Remarks - autoDeclaration</span></span>

<span data-ttu-id="08cf0-420">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-420">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="08cf0-421">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="08cf0-421">Method backgroundColor</span></span>

<span data-ttu-id="08cf0-422">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-422">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="08cf0-423">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="08cf0-423">Parameters - backgroundColor</span></span>

<span data-ttu-id="08cf0-424">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-424">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="08cf0-425">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="08cf0-425">Return Value - backgroundColor</span></span>

<span data-ttu-id="08cf0-426">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="08cf0-426">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="08cf0-427">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="08cf0-427">Remarks - backgroundColor</span></span>

<span data-ttu-id="08cf0-428">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-428">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="08cf0-429">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="08cf0-429">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="08cf0-430">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="08cf0-430">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="08cf0-431">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="08cf0-431">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="08cf0-432">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-432">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="08cf0-433">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-433">The maximum value for a single byte is 255.</span></span>

## <a name="method-backgroundimage"></a><span data-ttu-id="08cf0-434">メソッド backgroundImage</span><span class="sxs-lookup"><span data-stu-id="08cf0-434">Method backgroundImage</span></span>

```xpp
public Image backgroundImage([Image image], [int drawMode])
```

### <a name="parameters---backgroundimage"></a><span data-ttu-id="08cf0-435">パラメーター - backgroundImage</span><span class="sxs-lookup"><span data-stu-id="08cf0-435">Parameters - backgroundImage</span></span>

<span data-ttu-id="08cf0-436">画像</span><span class="sxs-lookup"><span data-stu-id="08cf0-436">image</span></span>  

<!-- -->

<span data-ttu-id="08cf0-437">drawMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-437">drawMode</span></span>  

### <a name="return-value---backgroundimage"></a><span data-ttu-id="08cf0-438">戻り値 - backgroundImage</span><span class="sxs-lookup"><span data-stu-id="08cf0-438">Return Value - backgroundImage</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="08cf0-439">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="08cf0-439">Method backStyle</span></span>

<span data-ttu-id="08cf0-440">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-440">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="08cf0-441">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="08cf0-441">Parameters - backStyle</span></span>

<span data-ttu-id="08cf0-442">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-442">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="08cf0-443">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="08cf0-443">Return Value - backStyle</span></span>

<span data-ttu-id="08cf0-444">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-444">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="08cf0-445">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="08cf0-445">Method beginDrag</span></span>

<span data-ttu-id="08cf0-446">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-446">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="08cf0-447">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="08cf0-447">Parameters - beginDrag</span></span>

<span data-ttu-id="08cf0-448">x</span><span class="sxs-lookup"><span data-stu-id="08cf0-448">x</span></span>  
<span data-ttu-id="08cf0-449">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-449">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="08cf0-450">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="08cf0-450">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="08cf0-451">y</span><span class="sxs-lookup"><span data-stu-id="08cf0-451">y</span></span>  
<span data-ttu-id="08cf0-452">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-452">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="08cf0-453">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="08cf0-453">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="08cf0-454">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="08cf0-454">Return Value - beginDrag</span></span>

<span data-ttu-id="08cf0-455">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-455">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="08cf0-456">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="08cf0-456">Remarks - beginDrag</span></span>

<span data-ttu-id="08cf0-457">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-457">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="08cf0-458">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-458">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bold"></a><span data-ttu-id="08cf0-459">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="08cf0-459">Method bold</span></span>

<span data-ttu-id="08cf0-460">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-460">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="08cf0-461">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="08cf0-461">Parameters - bold</span></span>

<span data-ttu-id="08cf0-462">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-462">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="08cf0-463">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="08cf0-463">Return Value - bold</span></span>

<span data-ttu-id="08cf0-464">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-464">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="08cf0-465">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="08cf0-465">Remarks - bold</span></span>

<span data-ttu-id="08cf0-466">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-466">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="08cf0-467">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-467">0 Use the default font weight.</span></span>
-   <span data-ttu-id="08cf0-468">1 シン。</span><span class="sxs-lookup"><span data-stu-id="08cf0-468">1 Thin.</span></span>
-   <span data-ttu-id="08cf0-469">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="08cf0-469">2 Extra-light.</span></span>
-   <span data-ttu-id="08cf0-470">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="08cf0-470">3 Light.</span></span>
-   <span data-ttu-id="08cf0-471">4 標準。</span><span class="sxs-lookup"><span data-stu-id="08cf0-471">4 Normal.</span></span>
-   <span data-ttu-id="08cf0-472">5 中。</span><span class="sxs-lookup"><span data-stu-id="08cf0-472">5 Medium.</span></span>
-   <span data-ttu-id="08cf0-473">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="08cf0-473">6 Semibold.</span></span>
-   <span data-ttu-id="08cf0-474">7 太字。</span><span class="sxs-lookup"><span data-stu-id="08cf0-474">7 Bold.</span></span>
-   <span data-ttu-id="08cf0-475">8 極太。</span><span class="sxs-lookup"><span data-stu-id="08cf0-475">8 Extra-bold.</span></span>
-   <span data-ttu-id="08cf0-476">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="08cf0-476">9 Heavy.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="08cf0-477">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-477">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="08cf0-478">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-478">Parameters - bottomMargin</span></span>

<span data-ttu-id="08cf0-479">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-479">value</span></span>  

<!-- -->

<span data-ttu-id="08cf0-480">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-480">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="08cf0-481">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-481">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="08cf0-482">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-482">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="08cf0-483">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-483">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="08cf0-484">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-484">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="08cf0-485">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-485">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="08cf0-486">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-486">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="08cf0-487">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-487">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="08cf0-488">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-488">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="08cf0-489">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-489">Return Value - bottomMarginValue</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="08cf0-490">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="08cf0-490">Method calcControlSize</span></span>

<span data-ttu-id="08cf0-491">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-491">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="08cf0-492">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="08cf0-492">Parameters - calcControlSize</span></span>

<span data-ttu-id="08cf0-493">chars</span><span class="sxs-lookup"><span data-stu-id="08cf0-493">chars</span></span>  
<span data-ttu-id="08cf0-494">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="08cf0-494">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="08cf0-495">明細行</span><span class="sxs-lookup"><span data-stu-id="08cf0-495">lines</span></span>  
<span data-ttu-id="08cf0-496">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="08cf0-496">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="08cf0-497">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="08cf0-497">Return Value - calcControlSize</span></span>

<span data-ttu-id="08cf0-498">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="08cf0-498">The container that holds the width and height.</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="08cf0-499">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="08cf0-499">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="08cf0-500">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="08cf0-500">Parameters - canAddDataField</span></span>

<span data-ttu-id="08cf0-501">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="08cf0-501">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="08cf0-502">fieldId</span><span class="sxs-lookup"><span data-stu-id="08cf0-502">fieldId</span></span>  

<!-- -->

<span data-ttu-id="08cf0-503">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="08cf0-503">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="08cf0-504">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="08cf0-504">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="08cf0-505">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="08cf0-505">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="08cf0-506">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="08cf0-506">Parameters - canContain</span></span>

<span data-ttu-id="08cf0-507">control</span><span class="sxs-lookup"><span data-stu-id="08cf0-507">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="08cf0-508">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="08cf0-508">Return Value - canContain</span></span>

## <a name="method-caption"></a><span data-ttu-id="08cf0-509">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="08cf0-509">Method caption</span></span>

<span data-ttu-id="08cf0-510">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-510">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="08cf0-511">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="08cf0-511">Parameters - caption</span></span>

<span data-ttu-id="08cf0-512">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-512">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="08cf0-513">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="08cf0-513">Return Value - caption</span></span>

<span data-ttu-id="08cf0-514">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="08cf0-514">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="08cf0-515">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="08cf0-515">Method characterSet</span></span>

<span data-ttu-id="08cf0-516">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-516">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="08cf0-517">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="08cf0-517">Parameters - characterSet</span></span>

<span data-ttu-id="08cf0-518">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-518">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="08cf0-519">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="08cf0-519">Return Value - characterSet</span></span>

<span data-ttu-id="08cf0-520">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-520">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="08cf0-521">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="08cf0-521">Remarks - characterSet</span></span>

<span data-ttu-id="08cf0-522">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-522">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="08cf0-523">値です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-523">Value.</span></span> | <span data-ttu-id="08cf0-524">説明。</span><span class="sxs-lookup"><span data-stu-id="08cf0-524">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="08cf0-525">0</span><span class="sxs-lookup"><span data-stu-id="08cf0-525">0</span></span>      | <span data-ttu-id="08cf0-526">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-526">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="08cf0-527">1</span><span class="sxs-lookup"><span data-stu-id="08cf0-527">1</span></span>      | <span data-ttu-id="08cf0-528">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-528">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="08cf0-529">2</span><span class="sxs-lookup"><span data-stu-id="08cf0-529">2</span></span>      | <span data-ttu-id="08cf0-530">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-530">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="08cf0-531">77</span><span class="sxs-lookup"><span data-stu-id="08cf0-531">77</span></span>     | <span data-ttu-id="08cf0-532">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-532">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="08cf0-533">128</span><span class="sxs-lookup"><span data-stu-id="08cf0-533">128</span></span>    | <span data-ttu-id="08cf0-534">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-534">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="08cf0-535">129</span><span class="sxs-lookup"><span data-stu-id="08cf0-535">129</span></span>    | <span data-ttu-id="08cf0-536">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-536">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="08cf0-537">134</span><span class="sxs-lookup"><span data-stu-id="08cf0-537">134</span></span>    | <span data-ttu-id="08cf0-538">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-538">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="08cf0-539">136</span><span class="sxs-lookup"><span data-stu-id="08cf0-539">136</span></span>    | <span data-ttu-id="08cf0-540">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-540">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="08cf0-541">161</span><span class="sxs-lookup"><span data-stu-id="08cf0-541">161</span></span>    | <span data-ttu-id="08cf0-542">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-542">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="08cf0-543">162</span><span class="sxs-lookup"><span data-stu-id="08cf0-543">162</span></span>    | <span data-ttu-id="08cf0-544">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-544">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="08cf0-545">163</span><span class="sxs-lookup"><span data-stu-id="08cf0-545">163</span></span>    | <span data-ttu-id="08cf0-546">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-546">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="08cf0-547">186</span><span class="sxs-lookup"><span data-stu-id="08cf0-547">186</span></span>    | <span data-ttu-id="08cf0-548">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-548">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="08cf0-549">204</span><span class="sxs-lookup"><span data-stu-id="08cf0-549">204</span></span>    | <span data-ttu-id="08cf0-550">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-550">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="08cf0-551">238</span><span class="sxs-lookup"><span data-stu-id="08cf0-551">238</span></span>    | <span data-ttu-id="08cf0-552">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-552">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="08cf0-553">255</span><span class="sxs-lookup"><span data-stu-id="08cf0-553">255</span></span>    | <span data-ttu-id="08cf0-554">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-554">OEM\_CHARSET</span></span>         |

<span data-ttu-id="08cf0-555">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-555">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="08cf0-556">値です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-556">Value.</span></span> | <span data-ttu-id="08cf0-557">説明。</span><span class="sxs-lookup"><span data-stu-id="08cf0-557">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="08cf0-558">130</span><span class="sxs-lookup"><span data-stu-id="08cf0-558">130</span></span>    | <span data-ttu-id="08cf0-559">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-559">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="08cf0-560">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-560">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="08cf0-561">値です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-561">Value.</span></span> | <span data-ttu-id="08cf0-562">説明。</span><span class="sxs-lookup"><span data-stu-id="08cf0-562">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="08cf0-563">177</span><span class="sxs-lookup"><span data-stu-id="08cf0-563">177</span></span>    | <span data-ttu-id="08cf0-564">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-564">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="08cf0-565">178</span><span class="sxs-lookup"><span data-stu-id="08cf0-565">178</span></span>    | <span data-ttu-id="08cf0-566">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-566">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="08cf0-567">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-567">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="08cf0-568">値です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-568">Value.</span></span> | <span data-ttu-id="08cf0-569">説明。</span><span class="sxs-lookup"><span data-stu-id="08cf0-569">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="08cf0-570">222</span><span class="sxs-lookup"><span data-stu-id="08cf0-570">222</span></span>    | <span data-ttu-id="08cf0-571">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="08cf0-571">THAI\_CHARSET</span></span> |

<span data-ttu-id="08cf0-572">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-572">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="08cf0-573">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-573">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="08cf0-574">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08cf0-574">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="08cf0-575">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="08cf0-575">Method colorScheme</span></span>

<span data-ttu-id="08cf0-576">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-576">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="08cf0-577">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="08cf0-577">Parameters - colorScheme</span></span>

<span data-ttu-id="08cf0-578">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-578">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="08cf0-579">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="08cf0-579">Return Value - colorScheme</span></span>

<span data-ttu-id="08cf0-580">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="08cf0-580">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="08cf0-581">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="08cf0-581">Remarks - colorScheme</span></span>

<span data-ttu-id="08cf0-582">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-582">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="08cf0-583">値です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-583">Value.</span></span> | <span data-ttu-id="08cf0-584">スタイル。</span><span class="sxs-lookup"><span data-stu-id="08cf0-584">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="08cf0-585">0</span><span class="sxs-lookup"><span data-stu-id="08cf0-585">0</span></span>      | <span data-ttu-id="08cf0-586">既定。</span><span class="sxs-lookup"><span data-stu-id="08cf0-586">Default.</span></span>                       |
| <span data-ttu-id="08cf0-587">1</span><span class="sxs-lookup"><span data-stu-id="08cf0-587">1</span></span>      | <span data-ttu-id="08cf0-588">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="08cf0-588">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="08cf0-589">2</span><span class="sxs-lookup"><span data-stu-id="08cf0-589">2</span></span>      | <span data-ttu-id="08cf0-590">真の配色。</span><span class="sxs-lookup"><span data-stu-id="08cf0-590">The true-color scheme.</span></span>         |

## <a name="method-columns"></a><span data-ttu-id="08cf0-591">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="08cf0-591">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="08cf0-592">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="08cf0-592">Parameters - columns</span></span>

<span data-ttu-id="08cf0-593">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-593">value</span></span>  

<!-- -->

<span data-ttu-id="08cf0-594">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-594">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="08cf0-595">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="08cf0-595">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="08cf0-596">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-596">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="08cf0-597">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-597">Parameters - columnsMode</span></span>

<span data-ttu-id="08cf0-598">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-598">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="08cf0-599">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-599">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="08cf0-600">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="08cf0-600">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="08cf0-601">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="08cf0-601">Parameters - columnspace</span></span>

<span data-ttu-id="08cf0-602">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-602">value</span></span>  

<!-- -->

<span data-ttu-id="08cf0-603">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-603">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="08cf0-604">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="08cf0-604">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="08cf0-605">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-605">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="08cf0-606">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-606">Parameters - columnspaceMode</span></span>

<span data-ttu-id="08cf0-607">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-607">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="08cf0-608">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-608">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="08cf0-609">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-609">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="08cf0-610">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-610">Parameters - columnspaceValue</span></span>

<span data-ttu-id="08cf0-611">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-611">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="08cf0-612">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-612">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="08cf0-613">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-613">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="08cf0-614">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-614">Parameters - columnsValue</span></span>

<span data-ttu-id="08cf0-615">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-615">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="08cf0-616">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-616">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="08cf0-617">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="08cf0-617">Method configurationKey</span></span>

<span data-ttu-id="08cf0-618">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-618">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="08cf0-619">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="08cf0-619">Parameters - configurationKey</span></span>

<span data-ttu-id="08cf0-620">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-620">value</span></span>  
<span data-ttu-id="08cf0-621">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-621">The ID of the configuration key that is being assigned to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="08cf0-622">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="08cf0-622">Return Value - configurationKey</span></span>

<span data-ttu-id="08cf0-623">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="08cf0-623">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="08cf0-624">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="08cf0-624">Remarks - configurationKey</span></span>

<span data-ttu-id="08cf0-625">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-625">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="08cf0-626">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-626">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="08cf0-627">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="08cf0-627">Method configurationKeyEx</span></span>

<span data-ttu-id="08cf0-628">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-628">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="08cf0-629">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="08cf0-629">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="08cf0-630">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="08cf0-630">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="08cf0-631">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="08cf0-631">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="08cf0-632">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-632">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="08cf0-633">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-633">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="08cf0-634">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-634">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-contains"></a><span data-ttu-id="08cf0-635">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="08cf0-635">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="08cf0-636">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="08cf0-636">Parameters - contains</span></span>

<span data-ttu-id="08cf0-637">control</span><span class="sxs-lookup"><span data-stu-id="08cf0-637">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="08cf0-638">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="08cf0-638">Return Value - contains</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="08cf0-639">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="08cf0-639">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="08cf0-640">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="08cf0-640">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="08cf0-641">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="08cf0-641">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="08cf0-642">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="08cf0-642">Parameters - controlNum</span></span>

<span data-ttu-id="08cf0-643">controlNo</span><span class="sxs-lookup"><span data-stu-id="08cf0-643">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="08cf0-644">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="08cf0-644">Return Value - controlNum</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="08cf0-645">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="08cf0-645">Method countryRegionCodes</span></span>

<span data-ttu-id="08cf0-646">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-646">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="08cf0-647">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="08cf0-647">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="08cf0-648">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-648">value</span></span>  
<span data-ttu-id="08cf0-649">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-649">The string that contains the country region/codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="08cf0-650">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="08cf0-650">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="08cf0-651">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="08cf0-651">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="08cf0-652">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="08cf0-652">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="08cf0-653">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="08cf0-653">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="08cf0-654">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-654">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="08cf0-655">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="08cf0-655">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="08cf0-656">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="08cf0-656">Method dataRelationPath</span></span>

<span data-ttu-id="08cf0-657">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-657">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="08cf0-658">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="08cf0-658">Parameters - dataRelationPath</span></span>

<span data-ttu-id="08cf0-659">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-659">value</span></span>  
<span data-ttu-id="08cf0-660">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-660">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="08cf0-661">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="08cf0-661">Return Value - dataRelationPath</span></span>

<span data-ttu-id="08cf0-662">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="08cf0-662">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="08cf0-663">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="08cf0-663">Remarks - dataRelationPath</span></span>

<span data-ttu-id="08cf0-664">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-664">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="08cf0-665">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="08cf0-665">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="08cf0-666">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="08cf0-666">Method dataSource</span></span>

<span data-ttu-id="08cf0-667">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-667">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="08cf0-668">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="08cf0-668">Parameters - dataSource</span></span>

<span data-ttu-id="08cf0-669">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-669">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="08cf0-670">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="08cf0-670">Return Value - dataSource</span></span>

<span data-ttu-id="08cf0-671">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="08cf0-671">The identifier of the data source to be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="08cf0-672">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="08cf0-672">Method displayTarget</span></span>

<span data-ttu-id="08cf0-673">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-673">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="08cf0-674">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="08cf0-674">Parameters - displayTarget</span></span>

<span data-ttu-id="08cf0-675">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-675">value</span></span>  
<span data-ttu-id="08cf0-676">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-676">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="08cf0-677">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="08cf0-677">Return Value - displayTarget</span></span>

<span data-ttu-id="08cf0-678">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-678">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="08cf0-679">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="08cf0-679">Method dragDrop</span></span>

<span data-ttu-id="08cf0-680">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-680">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="08cf0-681">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="08cf0-681">Parameters - dragDrop</span></span>

<span data-ttu-id="08cf0-682">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-682">value</span></span>  
<span data-ttu-id="08cf0-683">ドラッグ アンド ドロップの動作が有効かどうかを示す整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-683">An Integer data type that indicates whether the drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="08cf0-684">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="08cf0-684">Return Value - dragDrop</span></span>

<span data-ttu-id="08cf0-685">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-685">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="08cf0-686">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="08cf0-686">Remarks - dragDrop</span></span>

<span data-ttu-id="08cf0-687">FormControl::dragLeave、FormControl::dragOver、および FormControl::dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-687">Use the FormControl::dragLeave, FormControl::dragOver, and FormControl::dragOverEx methods to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="08cf0-688">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="08cf0-688">Method dragOver</span></span>

<span data-ttu-id="08cf0-689">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-689">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="08cf0-690">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="08cf0-690">Parameters - dragOver</span></span>

<span data-ttu-id="08cf0-691">dragSource</span><span class="sxs-lookup"><span data-stu-id="08cf0-691">dragSource</span></span>  
<span data-ttu-id="08cf0-692">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-692">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-693">dragMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-693">dragMode</span></span>  
<span data-ttu-id="08cf0-694">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-694">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-695">x</span><span class="sxs-lookup"><span data-stu-id="08cf0-695">x</span></span>  
<span data-ttu-id="08cf0-696">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-696">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-697">y</span><span class="sxs-lookup"><span data-stu-id="08cf0-697">y</span></span>  
<span data-ttu-id="08cf0-698">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-698">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="08cf0-699">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="08cf0-699">Return Value - dragOver</span></span>

<span data-ttu-id="08cf0-700">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-700">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="08cf0-701">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="08cf0-701">Method dragOverEx</span></span>

<span data-ttu-id="08cf0-702">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-702">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="08cf0-703">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="08cf0-703">Parameters - dragOverEx</span></span>

<span data-ttu-id="08cf0-704">dragSource</span><span class="sxs-lookup"><span data-stu-id="08cf0-704">dragSource</span></span>  
<span data-ttu-id="08cf0-705">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-705">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-706">dragMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-706">dragMode</span></span>  
<span data-ttu-id="08cf0-707">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-707">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-708">x</span><span class="sxs-lookup"><span data-stu-id="08cf0-708">x</span></span>  
<span data-ttu-id="08cf0-709">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-709">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-710">y</span><span class="sxs-lookup"><span data-stu-id="08cf0-710">y</span></span>  
<span data-ttu-id="08cf0-711">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-711">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="08cf0-712">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="08cf0-712">Return Value - dragOverEx</span></span>

<span data-ttu-id="08cf0-713">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-713">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="08cf0-714">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="08cf0-714">Method dragText</span></span>

<span data-ttu-id="08cf0-715">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-715">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="08cf0-716">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="08cf0-716">Return Value - dragText</span></span>

<span data-ttu-id="08cf0-717">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="08cf0-717">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="08cf0-718">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="08cf0-718">Method enabled</span></span>

<span data-ttu-id="08cf0-719">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-719">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="08cf0-720">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="08cf0-720">Parameters - enabled</span></span>

<span data-ttu-id="08cf0-721">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-721">value</span></span>  
<span data-ttu-id="08cf0-722">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-722">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="08cf0-723">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="08cf0-723">Return Value - enabled</span></span>

<span data-ttu-id="08cf0-724">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-724">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="08cf0-725">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="08cf0-725">Remarks - enabled</span></span>

<span data-ttu-id="08cf0-726">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-726">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="08cf0-727">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-727">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="08cf0-728">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-728">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="08cf0-729">メソッド font</span><span class="sxs-lookup"><span data-stu-id="08cf0-729">Method font</span></span>

<span data-ttu-id="08cf0-730">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-730">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="08cf0-731">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="08cf0-731">Parameters - font</span></span>

<span data-ttu-id="08cf0-732">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-732">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="08cf0-733">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="08cf0-733">Return Value - font</span></span>

<span data-ttu-id="08cf0-734">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="08cf0-734">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="08cf0-735">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="08cf0-735">Method fontSize</span></span>

<span data-ttu-id="08cf0-736">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-736">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="08cf0-737">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="08cf0-737">Parameters - fontSize</span></span>

<span data-ttu-id="08cf0-738">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-738">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="08cf0-739">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="08cf0-739">Return Value - fontSize</span></span>

<span data-ttu-id="08cf0-740">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="08cf0-740">The height of the font in points.</span></span>

## <a name="method-frameposition"></a><span data-ttu-id="08cf0-741">メソッド framePosition</span><span class="sxs-lookup"><span data-stu-id="08cf0-741">Method framePosition</span></span>

```xpp
public int framePosition([int value])
```

### <a name="parameters---frameposition"></a><span data-ttu-id="08cf0-742">パラメーター - framePosition</span><span class="sxs-lookup"><span data-stu-id="08cf0-742">Parameters - framePosition</span></span>

<span data-ttu-id="08cf0-743">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-743">value</span></span>  

### <a name="return-value---frameposition"></a><span data-ttu-id="08cf0-744">戻り値 - framePosition</span><span class="sxs-lookup"><span data-stu-id="08cf0-744">Return Value - framePosition</span></span>

## <a name="method-frametype"></a><span data-ttu-id="08cf0-745">メソッド frameType</span><span class="sxs-lookup"><span data-stu-id="08cf0-745">Method frameType</span></span>

```xpp
public int frameType([int value])
```

### <a name="parameters---frametype"></a><span data-ttu-id="08cf0-746">パラメーター - frameType</span><span class="sxs-lookup"><span data-stu-id="08cf0-746">Parameters - frameType</span></span>

<span data-ttu-id="08cf0-747">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-747">value</span></span>  

### <a name="return-value---frametype"></a><span data-ttu-id="08cf0-748">戻り値 - frameType</span><span class="sxs-lookup"><span data-stu-id="08cf0-748">Return Value - frameType</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="08cf0-749">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="08cf0-749">Method hasChanged</span></span>

<span data-ttu-id="08cf0-750">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-750">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="08cf0-751">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="08cf0-751">Parameters - hasChanged</span></span>

<span data-ttu-id="08cf0-752">val</span><span class="sxs-lookup"><span data-stu-id="08cf0-752">val</span></span>  
<span data-ttu-id="08cf0-753">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-753">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="08cf0-754">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="08cf0-754">Return Value - hasChanged</span></span>

<span data-ttu-id="08cf0-755">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-755">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="08cf0-756">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="08cf0-756">Method hasUserSetting</span></span>

<span data-ttu-id="08cf0-757">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-757">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="08cf0-758">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="08cf0-758">Return Value - hasUserSetting</span></span>

<span data-ttu-id="08cf0-759">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-759">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="08cf0-760">メソッド height</span><span class="sxs-lookup"><span data-stu-id="08cf0-760">Method height</span></span>

<span data-ttu-id="08cf0-761">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-761">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="08cf0-762">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="08cf0-762">Parameters - height</span></span>

<span data-ttu-id="08cf0-763">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-763">value</span></span>  
<span data-ttu-id="08cf0-764">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="08cf0-764">An Integer data type that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="08cf0-765">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-765">mode</span></span>  
<span data-ttu-id="08cf0-766">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="08cf0-766">An Integer data type that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="08cf0-767">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="08cf0-767">Return Value - height</span></span>

<span data-ttu-id="08cf0-768">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="08cf0-768">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="08cf0-769">備考 - height</span><span class="sxs-lookup"><span data-stu-id="08cf0-769">Remarks - height</span></span>

<span data-ttu-id="08cf0-770">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-770">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="08cf0-771">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="08cf0-771">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="08cf0-772">モード。</span><span class="sxs-lookup"><span data-stu-id="08cf0-772">Mode.</span></span>            | <span data-ttu-id="08cf0-773">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="08cf0-773">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="08cf0-774">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="08cf0-774">-1 Exact.</span></span>        | <span data-ttu-id="08cf0-775">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-775">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="08cf0-776">0 自動。</span><span class="sxs-lookup"><span data-stu-id="08cf0-776">0 Auto.</span></span>          | <span data-ttu-id="08cf0-777">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-777">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="08cf0-778">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="08cf0-778">1 Column height.</span></span> | <span data-ttu-id="08cf0-779">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="08cf0-779">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="08cf0-780">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-780">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="08cf0-781">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-781">Method heightMode</span></span>

<span data-ttu-id="08cf0-782">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-782">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="08cf0-783">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-783">Parameters - heightMode</span></span>

<span data-ttu-id="08cf0-784">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-784">value</span></span>  
<span data-ttu-id="08cf0-785">コントロールの高さの計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-785">An Integer data type value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="08cf0-786">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-786">Return Value - heightMode</span></span>

<span data-ttu-id="08cf0-787">計算モード。</span><span class="sxs-lookup"><span data-stu-id="08cf0-787">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="08cf0-788">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-788">Remarks - heightMode</span></span>

<span data-ttu-id="08cf0-789">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="08cf0-789">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="08cf0-790">モード。</span><span class="sxs-lookup"><span data-stu-id="08cf0-790">Mode.</span></span>          | <span data-ttu-id="08cf0-791">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="08cf0-791">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="08cf0-792">正確。</span><span class="sxs-lookup"><span data-stu-id="08cf0-792">Exact.</span></span>         | <span data-ttu-id="08cf0-793">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-793">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="08cf0-794">自動。</span><span class="sxs-lookup"><span data-stu-id="08cf0-794">Auto.</span></span>          | <span data-ttu-id="08cf0-795">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-795">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="08cf0-796">列の高さ</span><span class="sxs-lookup"><span data-stu-id="08cf0-796">Column height.</span></span> | <span data-ttu-id="08cf0-797">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="08cf0-797">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="08cf0-798">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="08cf0-798">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="08cf0-799">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-799">Method heightValue</span></span>

<span data-ttu-id="08cf0-800">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-800">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="08cf0-801">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-801">Parameters - heightValue</span></span>

<span data-ttu-id="08cf0-802">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-802">value</span></span>  
<span data-ttu-id="08cf0-803">高さをピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-803">An Integer data type that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="08cf0-804">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-804">Return Value - heightValue</span></span>

<span data-ttu-id="08cf0-805">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="08cf0-805">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="08cf0-806">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-806">Remarks - heightValue</span></span>

<span data-ttu-id="08cf0-807">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-807">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="08cf0-808">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="08cf0-808">Method helpField</span></span>

<span data-ttu-id="08cf0-809">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-809">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="08cf0-810">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="08cf0-810">Return Value - helpField</span></span>

<span data-ttu-id="08cf0-811">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="08cf0-811">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="08cf0-812">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="08cf0-812">Remarks - helpField</span></span>

<span data-ttu-id="08cf0-813">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-813">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="08cf0-814">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-814">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="08cf0-815">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="08cf0-815">Method helpText</span></span>

<span data-ttu-id="08cf0-816">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-816">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="08cf0-817">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="08cf0-817">Parameters - helpText</span></span>

<span data-ttu-id="08cf0-818">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-818">value</span></span>  
<span data-ttu-id="08cf0-819">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-819">The value that is assigned as the help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="08cf0-820">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="08cf0-820">Return Value - helpText</span></span>

<span data-ttu-id="08cf0-821">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="08cf0-821">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="08cf0-822">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="08cf0-822">Remarks - helpText</span></span>

<span data-ttu-id="08cf0-823">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-823">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="08cf0-824">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-824">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="08cf0-825">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="08cf0-825">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="08cf0-826">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="08cf0-826">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="08cf0-827">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-827">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="08cf0-828">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="08cf0-828">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="08cf0-829">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="08cf0-829">Method hierarchyParent</span></span>

<span data-ttu-id="08cf0-830">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-830">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="08cf0-831">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="08cf0-831">Parameters - hierarchyParent</span></span>

<span data-ttu-id="08cf0-832">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-832">value</span></span>  
<span data-ttu-id="08cf0-833">コントロールの HierarchyParent 値として割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-833">The value to assign as the HierarchyParent value of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="08cf0-834">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="08cf0-834">Return Value - hierarchyParent</span></span>

<span data-ttu-id="08cf0-835">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-835">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="08cf0-836">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="08cf0-836">Method hWnd</span></span>

<span data-ttu-id="08cf0-837">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-837">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="08cf0-838">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="08cf0-838">Return Value - hWnd</span></span>

<span data-ttu-id="08cf0-839">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="08cf0-839">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="08cf0-840">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="08cf0-840">Remarks - hWnd</span></span>

<span data-ttu-id="08cf0-841">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-841">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="08cf0-842">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="08cf0-842">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="08cf0-843">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="08cf0-843">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="08cf0-844">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="08cf0-844">Method isDisplayed</span></span>

<span data-ttu-id="08cf0-845">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-845">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="08cf0-846">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="08cf0-846">Return Value - isDisplayed</span></span>

<span data-ttu-id="08cf0-847">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-847">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="08cf0-848">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="08cf0-848">Remarks - isDisplayed</span></span>

<span data-ttu-id="08cf0-849">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-849">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="08cf0-850">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="08cf0-850">Method isRestricted</span></span>

<span data-ttu-id="08cf0-851">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-851">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="08cf0-852">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="08cf0-852">Return Value - isRestricted</span></span>

<span data-ttu-id="08cf0-853">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-853">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="08cf0-854">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="08cf0-854">Method isUserSetupEnabled</span></span>

<span data-ttu-id="08cf0-855">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-855">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="08cf0-856">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="08cf0-856">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="08cf0-857">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="08cf0-857">neededSetupRights</span></span>  
<span data-ttu-id="08cf0-858">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-858">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="08cf0-859">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="08cf0-859">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="08cf0-860">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-860">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="08cf0-861">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="08cf0-861">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="08cf0-862">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-862">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08cf0-863">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="08cf0-863">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="08cf0-864">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-864">No changes can be made to the control.</span></span> <span data-ttu-id="08cf0-865">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-865">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="08cf0-866">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="08cf0-866">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="08cf0-867">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-867">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="08cf0-868">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-868">The user cannot move the control.</span></span>   |
| <span data-ttu-id="08cf0-869">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="08cf0-869">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="08cf0-870">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-870">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="08cf0-871">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-871">The user can also move the control.</span></span> |

<span data-ttu-id="08cf0-872">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="08cf0-872">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-italic"></a><span data-ttu-id="08cf0-873">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="08cf0-873">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="08cf0-874">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="08cf0-874">Parameters - italic</span></span>

<span data-ttu-id="08cf0-875">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-875">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="08cf0-876">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="08cf0-876">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="08cf0-877">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="08cf0-877">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="08cf0-878">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="08cf0-878">Parameters - keyTip</span></span>

<span data-ttu-id="08cf0-879">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-879">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="08cf0-880">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="08cf0-880">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="08cf0-881">メソッド left</span><span class="sxs-lookup"><span data-stu-id="08cf0-881">Method left</span></span>

<span data-ttu-id="08cf0-882">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-882">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="08cf0-883">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="08cf0-883">Parameters - left</span></span>

<span data-ttu-id="08cf0-884">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-884">value</span></span>  
<span data-ttu-id="08cf0-885">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-885">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="08cf0-886">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-886">mode</span></span>  
<span data-ttu-id="08cf0-887">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-887">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="08cf0-888">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="08cf0-888">Return Value - left</span></span>

<span data-ttu-id="08cf0-889">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="08cf0-889">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="08cf0-890">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-890">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="08cf0-891">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-891">Parameters - leftMargin</span></span>

<span data-ttu-id="08cf0-892">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-892">value</span></span>  

<!-- -->

<span data-ttu-id="08cf0-893">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-893">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="08cf0-894">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-894">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="08cf0-895">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-895">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="08cf0-896">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-896">Parameters - leftMarginMode</span></span>

<span data-ttu-id="08cf0-897">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-897">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="08cf0-898">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-898">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="08cf0-899">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-899">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="08cf0-900">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-900">Parameters - leftMarginValue</span></span>

<span data-ttu-id="08cf0-901">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-901">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="08cf0-902">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-902">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="08cf0-903">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-903">Method leftMode</span></span>

<span data-ttu-id="08cf0-904">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-904">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="08cf0-905">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-905">Parameters - leftMode</span></span>

<span data-ttu-id="08cf0-906">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-906">value</span></span>  
<span data-ttu-id="08cf0-907">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-907">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="08cf0-908">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-908">Return Value - leftMode</span></span>

<span data-ttu-id="08cf0-909">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="08cf0-909">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="08cf0-910">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-910">Method leftValue</span></span>

<span data-ttu-id="08cf0-911">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-911">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="08cf0-912">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-912">Parameters - leftValue</span></span>

<span data-ttu-id="08cf0-913">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-913">value</span></span>  
<span data-ttu-id="08cf0-914">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-914">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="08cf0-915">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-915">Return Value - leftValue</span></span>

<span data-ttu-id="08cf0-916">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="08cf0-916">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="08cf0-917">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="08cf0-917">Method markAsUserAdd</span></span>

<span data-ttu-id="08cf0-918">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="08cf0-918">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="08cf0-919">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="08cf0-919">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="08cf0-920">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-920">value</span></span>  
<span data-ttu-id="08cf0-921">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-921">A Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="08cf0-922">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="08cf0-922">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="08cf0-923">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-923">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="08cf0-924">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="08cf0-924">Method mouseDblClick</span></span>

<span data-ttu-id="08cf0-925">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-925">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="08cf0-926">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="08cf0-926">Parameters - mouseDblClick</span></span>

<span data-ttu-id="08cf0-927">x</span><span class="sxs-lookup"><span data-stu-id="08cf0-927">x</span></span>  
<span data-ttu-id="08cf0-928">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-928">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-929">y</span><span class="sxs-lookup"><span data-stu-id="08cf0-929">y</span></span>  
<span data-ttu-id="08cf0-930">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-930">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-931">ボタン</span><span class="sxs-lookup"><span data-stu-id="08cf0-931">button</span></span>  
<span data-ttu-id="08cf0-932">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-932">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-933">Ctrl</span><span class="sxs-lookup"><span data-stu-id="08cf0-933">Ctrl</span></span>  
<span data-ttu-id="08cf0-934">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-934">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-935">シフト</span><span class="sxs-lookup"><span data-stu-id="08cf0-935">Shift</span></span>  
<span data-ttu-id="08cf0-936">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-936">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="08cf0-937">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="08cf0-937">Return Value - mouseDblClick</span></span>

<span data-ttu-id="08cf0-938">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-938">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="08cf0-939">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="08cf0-939">Remarks - mouseDblClick</span></span>

<span data-ttu-id="08cf0-940">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-940">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="08cf0-941">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="08cf0-941">Method mouseDown</span></span>

<span data-ttu-id="08cf0-942">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-942">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="08cf0-943">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="08cf0-943">Parameters - mouseDown</span></span>

<span data-ttu-id="08cf0-944">x</span><span class="sxs-lookup"><span data-stu-id="08cf0-944">x</span></span>  
<span data-ttu-id="08cf0-945">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-945">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-946">y</span><span class="sxs-lookup"><span data-stu-id="08cf0-946">y</span></span>  
<span data-ttu-id="08cf0-947">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-947">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-948">ボタン</span><span class="sxs-lookup"><span data-stu-id="08cf0-948">button</span></span>  
<span data-ttu-id="08cf0-949">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-949">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-950">Ctrl</span><span class="sxs-lookup"><span data-stu-id="08cf0-950">Ctrl</span></span>  
<span data-ttu-id="08cf0-951">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-951">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-952">シフト</span><span class="sxs-lookup"><span data-stu-id="08cf0-952">Shift</span></span>  
<span data-ttu-id="08cf0-953">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-953">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="08cf0-954">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="08cf0-954">Return Value - mouseDown</span></span>

<span data-ttu-id="08cf0-955">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-955">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="08cf0-956">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="08cf0-956">Remarks - mouseDown</span></span>

<span data-ttu-id="08cf0-957">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-957">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="08cf0-958">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-958">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="08cf0-959">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="08cf0-959">Method mouseMove</span></span>

<span data-ttu-id="08cf0-960">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-960">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="08cf0-961">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="08cf0-961">Parameters - mouseMove</span></span>

<span data-ttu-id="08cf0-962">x</span><span class="sxs-lookup"><span data-stu-id="08cf0-962">x</span></span>  
<span data-ttu-id="08cf0-963">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-963">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-964">y</span><span class="sxs-lookup"><span data-stu-id="08cf0-964">y</span></span>  
<span data-ttu-id="08cf0-965">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-965">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-966">ボタン</span><span class="sxs-lookup"><span data-stu-id="08cf0-966">button</span></span>  
<span data-ttu-id="08cf0-967">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-967">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-968">Ctrl</span><span class="sxs-lookup"><span data-stu-id="08cf0-968">Ctrl</span></span>  
<span data-ttu-id="08cf0-969">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-969">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-970">シフト</span><span class="sxs-lookup"><span data-stu-id="08cf0-970">Shift</span></span>  
<span data-ttu-id="08cf0-971">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-971">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="08cf0-972">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="08cf0-972">Return Value - mouseMove</span></span>

<span data-ttu-id="08cf0-973">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-973">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="08cf0-974">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="08cf0-974">Remarks - mouseMove</span></span>

<span data-ttu-id="08cf0-975">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-975">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="08cf0-976">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="08cf0-976">Method mouseUp</span></span>

<span data-ttu-id="08cf0-977">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-977">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="08cf0-978">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="08cf0-978">Parameters - mouseUp</span></span>

<span data-ttu-id="08cf0-979">x</span><span class="sxs-lookup"><span data-stu-id="08cf0-979">x</span></span>  
<span data-ttu-id="08cf0-980">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-980">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-981">y</span><span class="sxs-lookup"><span data-stu-id="08cf0-981">y</span></span>  
<span data-ttu-id="08cf0-982">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-982">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-983">ボタン</span><span class="sxs-lookup"><span data-stu-id="08cf0-983">button</span></span>  
<span data-ttu-id="08cf0-984">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-984">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-985">Ctrl</span><span class="sxs-lookup"><span data-stu-id="08cf0-985">Ctrl</span></span>  
<span data-ttu-id="08cf0-986">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-986">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-987">シフト</span><span class="sxs-lookup"><span data-stu-id="08cf0-987">Shift</span></span>  
<span data-ttu-id="08cf0-988">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-988">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="08cf0-989">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="08cf0-989">Return Value - mouseUp</span></span>

<span data-ttu-id="08cf0-990">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-990">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="08cf0-991">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="08cf0-991">Remarks - mouseUp</span></span>

<span data-ttu-id="08cf0-992">通常、このメソッドがオーバーライドされると、super への呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-992">Typically, when this method is overridden, the return value from a call to super is returned.</span></span> <span data-ttu-id="08cf0-993">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-993">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="08cf0-994">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-994">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="08cf0-995">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-995">Parameters - moveControl</span></span>

<span data-ttu-id="08cf0-996">controlId</span><span class="sxs-lookup"><span data-stu-id="08cf0-996">controlId</span></span>  

<!-- -->

<span data-ttu-id="08cf0-997">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="08cf0-997">insertAfterId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="08cf0-998">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-998">Return Value - moveControl</span></span>

## <a name="method-name"></a><span data-ttu-id="08cf0-999">メソッド名</span><span class="sxs-lookup"><span data-stu-id="08cf0-999">Method name</span></span>

<span data-ttu-id="08cf0-1000">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1000">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="08cf0-1001">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="08cf0-1001">Parameters - name</span></span>

<span data-ttu-id="08cf0-1002">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1002">value</span></span>  
<span data-ttu-id="08cf0-1003">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1003">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="08cf0-1004">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="08cf0-1004">Return Value - name</span></span>

<span data-ttu-id="08cf0-1005">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1005">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="08cf0-1006">備考 - name</span><span class="sxs-lookup"><span data-stu-id="08cf0-1006">Remarks - name</span></span>

<span data-ttu-id="08cf0-1007">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1007">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="08cf0-1008">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1008">It must start with a letter.</span></span>
-   <span data-ttu-id="08cf0-1009">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1009">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="08cf0-1010">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1010">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="08cf0-1011">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1011">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="08cf0-1012">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1012">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="08cf0-1013">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="08cf0-1013">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="08cf0-1014">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="08cf0-1014">Parameters - neededPermission</span></span>

<span data-ttu-id="08cf0-1015">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1015">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="08cf0-1016">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="08cf0-1016">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="08cf0-1017">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="08cf0-1017">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="08cf0-1018">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="08cf0-1018">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="08cf0-1019">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-1019">Method parentControl</span></span>

<span data-ttu-id="08cf0-1020">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1020">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="08cf0-1021">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-1021">Return Value - parentControl</span></span>

<span data-ttu-id="08cf0-1022">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1022">The parent control for the control.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="08cf0-1023">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-1023">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="08cf0-1024">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-1024">Parameters - rightMargin</span></span>

<span data-ttu-id="08cf0-1025">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1025">value</span></span>  

<!-- -->

<span data-ttu-id="08cf0-1026">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-1026">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="08cf0-1027">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-1027">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="08cf0-1028">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1028">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="08cf0-1029">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1029">Parameters - rightMarginMode</span></span>

<span data-ttu-id="08cf0-1030">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-1030">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="08cf0-1031">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1031">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="08cf0-1032">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1032">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="08cf0-1033">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1033">Parameters - rightMarginValue</span></span>

<span data-ttu-id="08cf0-1034">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1034">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="08cf0-1035">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1035">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="08cf0-1036">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="08cf0-1036">Method securityKey</span></span>

<span data-ttu-id="08cf0-1037">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1037">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="08cf0-1038">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="08cf0-1038">Parameters - securityKey</span></span>

<span data-ttu-id="08cf0-1039">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1039">value</span></span>  
<span data-ttu-id="08cf0-1040">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1040">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="08cf0-1041">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="08cf0-1041">Return Value - securityKey</span></span>

<span data-ttu-id="08cf0-1042">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1042">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="08cf0-1043">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="08cf0-1043">Method showContextMenu</span></span>

<span data-ttu-id="08cf0-1044">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1044">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="08cf0-1045">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="08cf0-1045">Parameters - showContextMenu</span></span>

<span data-ttu-id="08cf0-1046">menuHandle</span><span class="sxs-lookup"><span data-stu-id="08cf0-1046">menuHandle</span></span>  
<span data-ttu-id="08cf0-1047">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1047">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="08cf0-1048">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="08cf0-1048">Return Value - showContextMenu</span></span>

<span data-ttu-id="08cf0-1049">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1049">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-sizeheight"></a><span data-ttu-id="08cf0-1050">メソッド sizeHeight</span><span class="sxs-lookup"><span data-stu-id="08cf0-1050">Method sizeHeight</span></span>

```xpp
public boolean sizeHeight([boolean value])
```

### <a name="parameters---sizeheight"></a><span data-ttu-id="08cf0-1051">パラメーター - sizeHeight</span><span class="sxs-lookup"><span data-stu-id="08cf0-1051">Parameters - sizeHeight</span></span>

<span data-ttu-id="08cf0-1052">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1052">value</span></span>  

### <a name="return-value---sizeheight"></a><span data-ttu-id="08cf0-1053">戻り値 - sizeHeight</span><span class="sxs-lookup"><span data-stu-id="08cf0-1053">Return Value - sizeHeight</span></span>

## <a name="method-sizewidth"></a><span data-ttu-id="08cf0-1054">メソッド sizeWidth</span><span class="sxs-lookup"><span data-stu-id="08cf0-1054">Method sizeWidth</span></span>

```xpp
public boolean sizeWidth([boolean value])
```

### <a name="parameters---sizewidth"></a><span data-ttu-id="08cf0-1055">パラメーター - sizeWidth</span><span class="sxs-lookup"><span data-stu-id="08cf0-1055">Parameters - sizeWidth</span></span>

<span data-ttu-id="08cf0-1056">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1056">value</span></span>  

### <a name="return-value---sizewidth"></a><span data-ttu-id="08cf0-1057">戻り値 - sizeWidth</span><span class="sxs-lookup"><span data-stu-id="08cf0-1057">Return Value - sizeWidth</span></span>

## <a name="method-skip"></a><span data-ttu-id="08cf0-1058">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="08cf0-1058">Method skip</span></span>

<span data-ttu-id="08cf0-1059">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1059">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="08cf0-1060">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="08cf0-1060">Parameters - skip</span></span>

<span data-ttu-id="08cf0-1061">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1061">value</span></span>  
<span data-ttu-id="08cf0-1062">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1062">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="08cf0-1063">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="08cf0-1063">Return Value - skip</span></span>

<span data-ttu-id="08cf0-1064">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1064">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-sort"></a><span data-ttu-id="08cf0-1065">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="08cf0-1065">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="08cf0-1066">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="08cf0-1066">Parameters - sort</span></span>

<span data-ttu-id="08cf0-1067">sortDirection</span><span class="sxs-lookup"><span data-stu-id="08cf0-1067">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="08cf0-1068">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="08cf0-1068">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="08cf0-1069">メソッド style</span><span class="sxs-lookup"><span data-stu-id="08cf0-1069">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="08cf0-1070">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="08cf0-1070">Parameters - style</span></span>

<span data-ttu-id="08cf0-1071">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1071">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="08cf0-1072">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="08cf0-1072">Return Value - style</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="08cf0-1073">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="08cf0-1073">Method toolTip</span></span>

<span data-ttu-id="08cf0-1074">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1074">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="08cf0-1075">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="08cf0-1075">Return Value - toolTip</span></span>

<span data-ttu-id="08cf0-1076">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1076">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="08cf0-1077">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="08cf0-1077">Remarks - toolTip</span></span>

<span data-ttu-id="08cf0-1078">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1078">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="08cf0-1079">メソッド top</span><span class="sxs-lookup"><span data-stu-id="08cf0-1079">Method top</span></span>

<span data-ttu-id="08cf0-1080">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1080">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="08cf0-1081">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="08cf0-1081">Parameters - top</span></span>

<span data-ttu-id="08cf0-1082">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1082">value</span></span>  
<span data-ttu-id="08cf0-1083">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1083">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1084">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-1084">mode</span></span>  
<span data-ttu-id="08cf0-1085">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1085">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="08cf0-1086">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="08cf0-1086">Return Value - top</span></span>

<span data-ttu-id="08cf0-1087">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1087">The vertical position of the control in the form.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="08cf0-1088">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-1088">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="08cf0-1089">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-1089">Parameters - topMargin</span></span>

<span data-ttu-id="08cf0-1090">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1090">value</span></span>  

<!-- -->

<span data-ttu-id="08cf0-1091">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-1091">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="08cf0-1092">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="08cf0-1092">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="08cf0-1093">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1093">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="08cf0-1094">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1094">Parameters - topMarginMode</span></span>

<span data-ttu-id="08cf0-1095">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-1095">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="08cf0-1096">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1096">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="08cf0-1097">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1097">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="08cf0-1098">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1098">Parameters - topMarginValue</span></span>

<span data-ttu-id="08cf0-1099">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1099">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="08cf0-1100">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1100">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="08cf0-1101">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1101">Method topMode</span></span>

<span data-ttu-id="08cf0-1102">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1102">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="08cf0-1103">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1103">Parameters - topMode</span></span>

<span data-ttu-id="08cf0-1104">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1104">value</span></span>  
<span data-ttu-id="08cf0-1105">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1105">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="08cf0-1106">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1106">Return Value - topMode</span></span>

<span data-ttu-id="08cf0-1107">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1107">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="08cf0-1108">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1108">Method topValue</span></span>

<span data-ttu-id="08cf0-1109">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1109">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="08cf0-1110">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1110">Parameters - topValue</span></span>

<span data-ttu-id="08cf0-1111">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1111">value</span></span>  
<span data-ttu-id="08cf0-1112">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1112">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="08cf0-1113">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1113">Return Value - topValue</span></span>

<span data-ttu-id="08cf0-1114">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1114">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="08cf0-1115">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="08cf0-1115">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="08cf0-1116">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="08cf0-1116">Parameters - type</span></span>

<span data-ttu-id="08cf0-1117">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1117">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="08cf0-1118">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="08cf0-1118">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="08cf0-1119">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="08cf0-1119">Method underline</span></span>

<span data-ttu-id="08cf0-1120">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1120">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="08cf0-1121">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="08cf0-1121">Parameters - underline</span></span>

<span data-ttu-id="08cf0-1122">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1122">value</span></span>  
<span data-ttu-id="08cf0-1123">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1123">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="08cf0-1124">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="08cf0-1124">Return Value - underline</span></span>

<span data-ttu-id="08cf0-1125">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1125">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="08cf0-1126">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="08cf0-1126">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="08cf0-1127">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="08cf0-1127">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="08cf0-1128">データ</span><span class="sxs-lookup"><span data-stu-id="08cf0-1128">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="08cf0-1129">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="08cf0-1129">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="08cf0-1130">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="08cf0-1130">Method userData</span></span>

<span data-ttu-id="08cf0-1131">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1131">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="08cf0-1132">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="08cf0-1132">Parameters - userData</span></span>

<span data-ttu-id="08cf0-1133">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1133">value</span></span>  
<span data-ttu-id="08cf0-1134">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1134">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="08cf0-1135">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="08cf0-1135">Return Value - userData</span></span>

<span data-ttu-id="08cf0-1136">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1136">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="08cf0-1137">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="08cf0-1137">Method userDataItem</span></span>

<span data-ttu-id="08cf0-1138">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1138">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="08cf0-1139">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="08cf0-1139">Parameters - userDataItem</span></span>

<span data-ttu-id="08cf0-1140">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1140">value</span></span>  
<span data-ttu-id="08cf0-1141">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1141">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="08cf0-1142">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="08cf0-1142">Return Value - userDataItem</span></span>

<span data-ttu-id="08cf0-1143">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1143">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="08cf0-1144">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="08cf0-1144">Method userDataItems</span></span>

<span data-ttu-id="08cf0-1145">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1145">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="08cf0-1146">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="08cf0-1146">Parameters - userDataItems</span></span>

<span data-ttu-id="08cf0-1147">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1147">value</span></span>  
<span data-ttu-id="08cf0-1148">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1148">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="08cf0-1149">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="08cf0-1149">Return Value - userDataItems</span></span>

<span data-ttu-id="08cf0-1150">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1150">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="08cf0-1151">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="08cf0-1151">Method userDisable</span></span>

<span data-ttu-id="08cf0-1152">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1152">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="08cf0-1153">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="08cf0-1153">Parameters - userDisable</span></span>

<span data-ttu-id="08cf0-1154">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1154">value</span></span>  
<span data-ttu-id="08cf0-1155">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1155">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="08cf0-1156">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="08cf0-1156">Return Value - userDisable</span></span>

<span data-ttu-id="08cf0-1157">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1157">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="08cf0-1158">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="08cf0-1158">Method userHeight</span></span>

<span data-ttu-id="08cf0-1159">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1159">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="08cf0-1160">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="08cf0-1160">Parameters - userHeight</span></span>

<span data-ttu-id="08cf0-1161">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1161">value</span></span>  
<span data-ttu-id="08cf0-1162">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1162">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="08cf0-1163">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="08cf0-1163">Return Value - userHeight</span></span>

<span data-ttu-id="08cf0-1164">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1164">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="08cf0-1165">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="08cf0-1165">Method userHide</span></span>

<span data-ttu-id="08cf0-1166">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1166">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="08cf0-1167">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="08cf0-1167">Parameters - userHide</span></span>

<span data-ttu-id="08cf0-1168">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1168">value</span></span>  
<span data-ttu-id="08cf0-1169">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1169">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="08cf0-1170">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="08cf0-1170">Return Value - userHide</span></span>

<span data-ttu-id="08cf0-1171">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1171">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="08cf0-1172">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="08cf0-1172">Remarks - userHide</span></span>

<span data-ttu-id="08cf0-1173">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1173">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="08cf0-1174">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1174">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="08cf0-1175">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1175">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="08cf0-1176">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="08cf0-1176">Method userOrgContainer</span></span>

<span data-ttu-id="08cf0-1177">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1177">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="08cf0-1178">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="08cf0-1178">Parameters - userOrgContainer</span></span>

<span data-ttu-id="08cf0-1179">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1179">value</span></span>  
<span data-ttu-id="08cf0-1180">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1180">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="08cf0-1181">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="08cf0-1181">Return Value - userOrgContainer</span></span>

<span data-ttu-id="08cf0-1182">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1182">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="08cf0-1183">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="08cf0-1183">Method userOrgSibling</span></span>

<span data-ttu-id="08cf0-1184">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1184">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="08cf0-1185">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="08cf0-1185">Parameters - userOrgSibling</span></span>

<span data-ttu-id="08cf0-1186">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1186">value</span></span>  
<span data-ttu-id="08cf0-1187">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1187">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="08cf0-1188">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="08cf0-1188">Return Value - userOrgSibling</span></span>

<span data-ttu-id="08cf0-1189">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1189">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="08cf0-1190">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="08cf0-1190">Method userPromptText</span></span>

<span data-ttu-id="08cf0-1191">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1191">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="08cf0-1192">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="08cf0-1192">Parameters - userPromptText</span></span>

<span data-ttu-id="08cf0-1193">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1193">value</span></span>  
<span data-ttu-id="08cf0-1194">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1194">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="08cf0-1195">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="08cf0-1195">Return Value - userPromptText</span></span>

<span data-ttu-id="08cf0-1196">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1196">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="08cf0-1197">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="08cf0-1197">Method userSecurityLevel</span></span>

<span data-ttu-id="08cf0-1198">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1198">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="08cf0-1199">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="08cf0-1199">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="08cf0-1200">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1200">value</span></span>  
<span data-ttu-id="08cf0-1201">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1201">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="08cf0-1202">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="08cf0-1202">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="08cf0-1203">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1203">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="08cf0-1204">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="08cf0-1204">Method userSkip</span></span>

<span data-ttu-id="08cf0-1205">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1205">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls on the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="08cf0-1206">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="08cf0-1206">Parameters - userSkip</span></span>

<span data-ttu-id="08cf0-1207">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1207">value</span></span>  
<span data-ttu-id="08cf0-1208">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1208">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="08cf0-1209">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1209">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="08cf0-1210">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="08cf0-1210">Return Value - userSkip</span></span>

<span data-ttu-id="08cf0-1211">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1211">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="08cf0-1212">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="08cf0-1212">Method userWidth</span></span>

<span data-ttu-id="08cf0-1213">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1213">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="08cf0-1214">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="08cf0-1214">Parameters - userWidth</span></span>

<span data-ttu-id="08cf0-1215">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1215">value</span></span>  
<span data-ttu-id="08cf0-1216">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1216">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="08cf0-1217">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="08cf0-1217">Return Value - userWidth</span></span>

<span data-ttu-id="08cf0-1218">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1218">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="08cf0-1219">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="08cf0-1219">Remarks - userWidth</span></span>

<span data-ttu-id="08cf0-1220">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1220">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="08cf0-1221">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1221">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="08cf0-1222">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1222">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="08cf0-1223">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="08cf0-1223">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="08cf0-1224">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="08cf0-1224">Parameters - useUserLayout</span></span>

<span data-ttu-id="08cf0-1225">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1225">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="08cf0-1226">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="08cf0-1226">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="08cf0-1227">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="08cf0-1227">Method verticalSpacing</span></span>

<span data-ttu-id="08cf0-1228">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1228">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="08cf0-1229">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="08cf0-1229">Parameters - verticalSpacing</span></span>

<span data-ttu-id="08cf0-1230">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1230">value</span></span>  
<span data-ttu-id="08cf0-1231">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1231">An integer value that indicates the AutoMode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1232">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-1232">mode</span></span>  
<span data-ttu-id="08cf0-1233">コントロールの AutoMode を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1233">An integer value that indicates the AutoMode for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="08cf0-1234">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="08cf0-1234">Return Value - verticalSpacing</span></span>

<span data-ttu-id="08cf0-1235">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1235">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="08cf0-1236">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1236">Method verticalSpacingMode</span></span>

<span data-ttu-id="08cf0-1237">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1237">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="08cf0-1238">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1238">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="08cf0-1239">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-1239">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="08cf0-1240">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1240">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="08cf0-1241">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1241">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="08cf0-1242">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1242">Method verticalSpacingValue</span></span>

<span data-ttu-id="08cf0-1243">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1243">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="08cf0-1244">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1244">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="08cf0-1245">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1245">value</span></span>  
<span data-ttu-id="08cf0-1246">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1246">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="08cf0-1247">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1247">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="08cf0-1248">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1248">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="08cf0-1249">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="08cf0-1249">Method visible</span></span>

<span data-ttu-id="08cf0-1250">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1250">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="08cf0-1251">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="08cf0-1251">Parameters - visible</span></span>

<span data-ttu-id="08cf0-1252">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1252">value</span></span>  
<span data-ttu-id="08cf0-1253">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1253">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="08cf0-1254">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="08cf0-1254">Return Value - visible</span></span>

<span data-ttu-id="08cf0-1255">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1255">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="08cf0-1256">メソッド width</span><span class="sxs-lookup"><span data-stu-id="08cf0-1256">Method width</span></span>

<span data-ttu-id="08cf0-1257">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1257">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="08cf0-1258">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="08cf0-1258">Parameters - width</span></span>

<span data-ttu-id="08cf0-1259">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1259">value</span></span>  
<span data-ttu-id="08cf0-1260">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1260">An Integer data type that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1261">モード</span><span class="sxs-lookup"><span data-stu-id="08cf0-1261">mode</span></span>  
<span data-ttu-id="08cf0-1262">幅の計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1262">An Integer data type that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="08cf0-1263">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="08cf0-1263">Return Value - width</span></span>

<span data-ttu-id="08cf0-1264">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1264">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="08cf0-1265">備考 - width</span><span class="sxs-lookup"><span data-stu-id="08cf0-1265">Remarks - width</span></span>

<span data-ttu-id="08cf0-1266">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1266">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="08cf0-1267">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="08cf0-1267">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="08cf0-1268">モード。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1268">Mode.</span></span>           | <span data-ttu-id="08cf0-1269">幅計算。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1269">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08cf0-1270">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1270">-1 Exact.</span></span>       | <span data-ttu-id="08cf0-1271">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1271">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="08cf0-1272">0 自動。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1272">0 Auto.</span></span>         | <span data-ttu-id="08cf0-1273">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1273">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="08cf0-1274">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1274">1 Column width.</span></span> | <span data-ttu-id="08cf0-1275">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1275">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="08cf0-1276">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1276">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="08cf0-1277">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1277">Method widthMode</span></span>

<span data-ttu-id="08cf0-1278">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1278">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="08cf0-1279">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1279">Parameters - widthMode</span></span>

<span data-ttu-id="08cf0-1280">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1280">value</span></span>  
<span data-ttu-id="08cf0-1281">コントロールの幅の計算方法を示す整数データ型値です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1281">An Integer data type value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="08cf0-1282">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1282">Return Value - widthMode</span></span>

<span data-ttu-id="08cf0-1283">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1283">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="08cf0-1284">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1284">Remarks - widthMode</span></span>

<span data-ttu-id="08cf0-1285">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="08cf0-1285">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="08cf0-1286">モード。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1286">Mode.</span></span>         | <span data-ttu-id="08cf0-1287">幅計算。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1287">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08cf0-1288">正確。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1288">Exact.</span></span>        | <span data-ttu-id="08cf0-1289">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1289">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="08cf0-1290">自動。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1290">Auto.</span></span>         | <span data-ttu-id="08cf0-1291">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1291">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="08cf0-1292">列の幅。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1292">Column width.</span></span> | <span data-ttu-id="08cf0-1293">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1293">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="08cf0-1294">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1294">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="08cf0-1295">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1295">Method widthValue</span></span>

<span data-ttu-id="08cf0-1296">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1296">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="08cf0-1297">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1297">Parameters - widthValue</span></span>

<span data-ttu-id="08cf0-1298">値</span><span class="sxs-lookup"><span data-stu-id="08cf0-1298">value</span></span>  
<span data-ttu-id="08cf0-1299">幅をピクセル単位で指定する整数データ型です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1299">An Integer data type that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="08cf0-1300">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1300">Return Value - widthValue</span></span>

<span data-ttu-id="08cf0-1301">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1301">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="08cf0-1302">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="08cf0-1302">Remarks - widthValue</span></span>

<span data-ttu-id="08cf0-1303">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1303">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="08cf0-1304">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="08cf0-1304">Method resetUserSetting</span></span>

<span data-ttu-id="08cf0-1305">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1305">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-cut"></a><span data-ttu-id="08cf0-1306">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="08cf0-1306">Method cut</span></span>

<span data-ttu-id="08cf0-1307">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1307">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="08cf0-1308">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="08cf0-1308">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="08cf0-1309">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="08cf0-1309">Parameters - OnGotFocus</span></span>

<span data-ttu-id="08cf0-1310">sender</span><span class="sxs-lookup"><span data-stu-id="08cf0-1310">sender</span></span>  

<!-- -->

<span data-ttu-id="08cf0-1311">e</span><span class="sxs-lookup"><span data-stu-id="08cf0-1311">e</span></span>  

## <a name="method-copy"></a><span data-ttu-id="08cf0-1312">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="08cf0-1312">Method copy</span></span>

<span data-ttu-id="08cf0-1313">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1313">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-arrange"></a><span data-ttu-id="08cf0-1314">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="08cf0-1314">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-dragleave"></a><span data-ttu-id="08cf0-1315">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="08cf0-1315">Method dragLeave</span></span>

<span data-ttu-id="08cf0-1316">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1316">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-mouseleave"></a><span data-ttu-id="08cf0-1317">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="08cf0-1317">Method mouseLeave</span></span>

<span data-ttu-id="08cf0-1318">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1318">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="08cf0-1319">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="08cf0-1319">Method displayControl</span></span>

<span data-ttu-id="08cf0-1320">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1320">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="08cf0-1321">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="08cf0-1321">Method prefColumnSize</span></span>

<span data-ttu-id="08cf0-1322">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1322">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="08cf0-1323">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="08cf0-1323">Parameters - prefColumnSize</span></span>

<span data-ttu-id="08cf0-1324">width</span><span class="sxs-lookup"><span data-stu-id="08cf0-1324">width</span></span>  
<span data-ttu-id="08cf0-1325">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1325">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1326">height</span><span class="sxs-lookup"><span data-stu-id="08cf0-1326">height</span></span>  
<span data-ttu-id="08cf0-1327">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1327">The preferred height of the control.</span></span>

## <a name="method-lostfocus"></a><span data-ttu-id="08cf0-1328">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="08cf0-1328">Method lostFocus</span></span>

<span data-ttu-id="08cf0-1329">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1329">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-drop"></a><span data-ttu-id="08cf0-1330">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="08cf0-1330">Method drop</span></span>

<span data-ttu-id="08cf0-1331">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1331">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="08cf0-1332">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="08cf0-1332">Parameters - drop</span></span>

<span data-ttu-id="08cf0-1333">dragSource</span><span class="sxs-lookup"><span data-stu-id="08cf0-1333">dragSource</span></span>  
<span data-ttu-id="08cf0-1334">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1334">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1335">dragMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1335">dragMode</span></span>  
<span data-ttu-id="08cf0-1336">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1336">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1337">x</span><span class="sxs-lookup"><span data-stu-id="08cf0-1337">x</span></span>  
<span data-ttu-id="08cf0-1338">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1338">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1339">y</span><span class="sxs-lookup"><span data-stu-id="08cf0-1339">y</span></span>  
<span data-ttu-id="08cf0-1340">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1340">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-enddrag"></a><span data-ttu-id="08cf0-1341">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="08cf0-1341">Method endDrag</span></span>

<span data-ttu-id="08cf0-1342">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1342">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="08cf0-1343">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="08cf0-1343">Remarks - endDrag</span></span>

<span data-ttu-id="08cf0-1344">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1344">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="08cf0-1345">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1345">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-inputsearch"></a><span data-ttu-id="08cf0-1346">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="08cf0-1346">Method inputSearch</span></span>

<span data-ttu-id="08cf0-1347">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1347">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="08cf0-1348">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="08cf0-1348">Parameters - inputSearch</span></span>

<span data-ttu-id="08cf0-1349">searchStr</span><span class="sxs-lookup"><span data-stu-id="08cf0-1349">searchStr</span></span>  
<span data-ttu-id="08cf0-1350">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1350">The string value to use to filter data; optional.</span></span>

## <a name="method-onlostfocus"></a><span data-ttu-id="08cf0-1351">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="08cf0-1351">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="08cf0-1352">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="08cf0-1352">Parameters - OnLostFocus</span></span>

<span data-ttu-id="08cf0-1353">sender</span><span class="sxs-lookup"><span data-stu-id="08cf0-1353">sender</span></span>  

<!-- -->

<span data-ttu-id="08cf0-1354">e</span><span class="sxs-lookup"><span data-stu-id="08cf0-1354">e</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="08cf0-1355">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="08cf0-1355">Method gotFocus</span></span>

<span data-ttu-id="08cf0-1356">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1356">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="08cf0-1357">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="08cf0-1357">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="08cf0-1358">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="08cf0-1358">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="08cf0-1359">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="08cf0-1359">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="08cf0-1360">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="08cf0-1360">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="08cf0-1361">overrideObject</span><span class="sxs-lookup"><span data-stu-id="08cf0-1361">overrideObject</span></span>  

## <a name="method-jumpref"></a><span data-ttu-id="08cf0-1362">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="08cf0-1362">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-mouseenter"></a><span data-ttu-id="08cf0-1363">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="08cf0-1363">Method mouseEnter</span></span>

<span data-ttu-id="08cf0-1364">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1364">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="08cf0-1365">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="08cf0-1365">Parameters - mouseEnter</span></span>

<span data-ttu-id="08cf0-1366">x</span><span class="sxs-lookup"><span data-stu-id="08cf0-1366">x</span></span>  
<span data-ttu-id="08cf0-1367">Shift キーが押されている場合は、ブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1367">A Boolean value of true if the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1368">y</span><span class="sxs-lookup"><span data-stu-id="08cf0-1368">y</span></span>  
<span data-ttu-id="08cf0-1369">Shift キーが押されている場合は、ブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1369">A Boolean value of true if the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1370">ボタン</span><span class="sxs-lookup"><span data-stu-id="08cf0-1370">button</span></span>  
<span data-ttu-id="08cf0-1371">Shift キーが押されている場合は、ブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1371">A Boolean value of true if the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1372">Ctrl</span><span class="sxs-lookup"><span data-stu-id="08cf0-1372">Ctrl</span></span>  
<span data-ttu-id="08cf0-1373">Shift キーが押されている場合は、ブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1373">A Boolean value of true if the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1374">シフト</span><span class="sxs-lookup"><span data-stu-id="08cf0-1374">Shift</span></span>  
<span data-ttu-id="08cf0-1375">Shift キーが押されている場合は、ブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1375">A Boolean value of true if the SHIFT key is down.</span></span>

## <a name="method-setfocus"></a><span data-ttu-id="08cf0-1376">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="08cf0-1376">Method setFocus</span></span>

<span data-ttu-id="08cf0-1377">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1377">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-filter"></a><span data-ttu-id="08cf0-1378">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="08cf0-1378">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="08cf0-1379">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="08cf0-1379">Parameters - filter</span></span>

<span data-ttu-id="08cf0-1380">filterStr</span><span class="sxs-lookup"><span data-stu-id="08cf0-1380">filterStr</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="08cf0-1381">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="08cf0-1381">Method dropEx</span></span>

<span data-ttu-id="08cf0-1382">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1382">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="08cf0-1383">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="08cf0-1383">Parameters - dropEx</span></span>

<span data-ttu-id="08cf0-1384">dragSource</span><span class="sxs-lookup"><span data-stu-id="08cf0-1384">dragSource</span></span>  
<span data-ttu-id="08cf0-1385">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1385">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1386">dragMode</span><span class="sxs-lookup"><span data-stu-id="08cf0-1386">dragMode</span></span>  
<span data-ttu-id="08cf0-1387">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1387">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1388">x</span><span class="sxs-lookup"><span data-stu-id="08cf0-1388">x</span></span>  
<span data-ttu-id="08cf0-1389">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1389">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="08cf0-1390">y</span><span class="sxs-lookup"><span data-stu-id="08cf0-1390">y</span></span>  
<span data-ttu-id="08cf0-1391">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1391">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-paste"></a><span data-ttu-id="08cf0-1392">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="08cf0-1392">Method paste</span></span>

<span data-ttu-id="08cf0-1393">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1393">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-context"></a><span data-ttu-id="08cf0-1394">メソッド context</span><span class="sxs-lookup"><span data-stu-id="08cf0-1394">Method context</span></span>

<span data-ttu-id="08cf0-1395">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="08cf0-1395">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

