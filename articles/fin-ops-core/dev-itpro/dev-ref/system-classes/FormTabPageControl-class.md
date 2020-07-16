---
title: FormTabPageControl クラス
description: このトピックでは、FormTabPageControl クラスについて説明します。
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
ms.openlocfilehash: c23203b0bdf940baed30cc4de325d69c4b05e505
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502618"
---
# <a name="class-formtabpagecontrol"></a><span data-ttu-id="2759a-103">クラス FormTabPageControl</span><span class="sxs-lookup"><span data-stu-id="2759a-103">Class FormTabPageControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormTabPageControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="2759a-104">備考</span><span class="sxs-lookup"><span data-stu-id="2759a-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="2759a-105">例</span><span class="sxs-lookup"><span data-stu-id="2759a-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="2759a-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="2759a-106">Methods</span></span>

| <span data-ttu-id="2759a-107">方法</span><span class="sxs-lookup"><span data-stu-id="2759a-107">Method</span></span>                                                                                                              | <span data-ttu-id="2759a-108">説明</span><span class="sxs-lookup"><span data-stu-id="2759a-108">Description</span></span>                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2759a-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="2759a-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                                                                                                                         |
| <span data-ttu-id="2759a-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="2759a-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                                                                                                                         |
| <span data-ttu-id="2759a-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="2759a-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="2759a-112">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-112">public boolean alignChild(\[boolean value\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="2759a-113">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-113">public boolean alignChildren(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="2759a-114">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-114">public boolean alignControl(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="2759a-115">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-115">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="2759a-116">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-116">public boolean allowEdit(\[boolean value\])</span></span>                                                                         | <span data-ttu-id="2759a-117">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-117">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="2759a-118">public boolean allowPageDeactivate()</span><span class="sxs-lookup"><span data-stu-id="2759a-118">public boolean allowPageDeactivate()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="2759a-119">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="2759a-119">public boolean allowSysSetup()</span></span>                                                                                      | <span data-ttu-id="2759a-120">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-120">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="2759a-121">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-121">public int allowUserSetup(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="2759a-122">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-122">public int arrangeGuide(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="2759a-123">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-123">public int arrangeMethod(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="2759a-124">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-124">public int arrangeWhen(\[int value\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="2759a-125">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-125">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="2759a-126">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-126">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="2759a-127">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-127">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="2759a-128">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-128">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="2759a-129">public Image backgroundImage(\[Image image\], \[int drawMode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-129">public Image backgroundImage(\[Image image\], \[int drawMode\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="2759a-130">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-130">public int backStyle(\[int value\])</span></span>                                                                                 | <span data-ttu-id="2759a-131">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-131">Determines whether the control background can be transparent.</span></span>                                                                                                           |
| <span data-ttu-id="2759a-132">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="2759a-132">public int beginDrag(int x, int y)</span></span>                                                                                  | <span data-ttu-id="2759a-133">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-133">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="2759a-134">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-134">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="2759a-135">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-135">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="2759a-136">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-136">public int bottomMarginValue(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="2759a-137">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="2759a-137">public container calcControlSize(int chars, int lines)</span></span>                                                              | <span data-ttu-id="2759a-138">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-138">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="2759a-139">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="2759a-139">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="2759a-140">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="2759a-140">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="2759a-141">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-141">public str caption(\[str value\])</span></span>                                                                                   | <span data-ttu-id="2759a-142">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-142">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="2759a-143">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-143">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="2759a-144">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-144">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="2759a-145">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-145">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="2759a-146">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-146">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="2759a-147">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-147">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="2759a-148">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-148">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="2759a-149">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-149">public int columnspaceValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="2759a-150">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-150">public int columnsValue(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="2759a-151">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-151">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            | <span data-ttu-id="2759a-152">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-152">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="2759a-153">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="2759a-153">public List configurationKeyEx()</span></span>                                                                                    | <span data-ttu-id="2759a-154">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-154">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="2759a-155">public int containerScrollHorizontalOffset(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-155">public int containerScrollHorizontalOffset(\[int value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="2759a-156">public int containerScrollVerticalOffset(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-156">public int containerScrollVerticalOffset(\[int value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="2759a-157">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="2759a-157">public boolean contains(FormControl control)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="2759a-158">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="2759a-158">public int controlCount()</span></span>                                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="2759a-159">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="2759a-159">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="2759a-160">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-160">public str countryRegionCodes(\[str value\])</span></span>                                                                        | <span data-ttu-id="2759a-161">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-161">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="2759a-162">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-162">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="2759a-163">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-163">public str dataRelationPath(\[str value\])</span></span>                                                                          | <span data-ttu-id="2759a-164">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-164">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="2759a-165">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-165">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="2759a-166">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-166">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                                                |
| <span data-ttu-id="2759a-167">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-167">public int displayTarget(\[int value\])</span></span>                                                                             | <span data-ttu-id="2759a-168">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-168">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="2759a-169">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-169">public int dragDrop(\[int value\])</span></span>                                                                                  | <span data-ttu-id="2759a-170">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-170">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="2759a-171">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="2759a-171">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="2759a-172">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2759a-172">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="2759a-173">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="2759a-173">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="2759a-174">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2759a-174">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="2759a-175">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="2759a-175">public str dragText()</span></span>                                                                                               | <span data-ttu-id="2759a-176">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-176">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="2759a-177">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-177">public boolean enabled(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="2759a-178">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-178">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="2759a-179">public int fastTabExpanded(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-179">public int fastTabExpanded(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="2759a-180">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="2759a-180">public boolean hasChanged(\[boolean val\])</span></span>                                                                          | <span data-ttu-id="2759a-181">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-181">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="2759a-182">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="2759a-182">public boolean hasUserSetting()</span></span>                                                                                     | <span data-ttu-id="2759a-183">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-183">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="2759a-184">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-184">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="2759a-185">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-185">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="2759a-186">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-186">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="2759a-187">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-187">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="2759a-188">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-188">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="2759a-189">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-189">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="2759a-190">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="2759a-190">public str helpField()</span></span>                                                                                              | <span data-ttu-id="2759a-191">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-191">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="2759a-192">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-192">public str helpText(\[str value\])</span></span>                                                                                  | <span data-ttu-id="2759a-193">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-193">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="2759a-194">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-194">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="2759a-195">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-195">public str hierarchyParent(\[str value\])</span></span>                                                                           | <span data-ttu-id="2759a-196">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-196">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="2759a-197">public boolean horizontalScrollBarVisible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-197">public boolean horizontalScrollBarVisible(\[boolean value\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="2759a-198">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="2759a-198">public int hWnd()</span></span>                                                                                                   | <span data-ttu-id="2759a-199">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-199">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="2759a-200">public boolean isActivePage()</span><span class="sxs-lookup"><span data-stu-id="2759a-200">public boolean isActivePage()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="2759a-201">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="2759a-201">public boolean isContainer()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="2759a-202">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="2759a-202">public boolean isDisplayed()</span></span>                                                                                        | <span data-ttu-id="2759a-203">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-203">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="2759a-204">public boolean isExpanded()</span><span class="sxs-lookup"><span data-stu-id="2759a-204">public boolean isExpanded()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="2759a-205">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="2759a-205">public boolean isRestricted()</span></span>                                                                                       | <span data-ttu-id="2759a-206">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-206">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="2759a-207">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="2759a-207">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            | <span data-ttu-id="2759a-208">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-208">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="2759a-209">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-209">public int left(int value, \[int mode\])</span></span>                                                                            | <span data-ttu-id="2759a-210">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-210">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="2759a-211">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-211">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="2759a-212">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-212">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="2759a-213">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-213">public int leftMarginValue(\[int value\])</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="2759a-214">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-214">public int leftMode(\[int value\])</span></span>                                                                                  | <span data-ttu-id="2759a-215">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-215">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="2759a-216">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-216">public int leftValue(\[int value\])</span></span>                                                                                 | <span data-ttu-id="2759a-217">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-217">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="2759a-218">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-218">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     | <span data-ttu-id="2759a-219">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="2759a-219">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="2759a-220">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="2759a-220">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     | <span data-ttu-id="2759a-221">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-221">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="2759a-222">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="2759a-222">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="2759a-223">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-223">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="2759a-224">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="2759a-224">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         | <span data-ttu-id="2759a-225">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-225">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="2759a-226">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="2759a-226">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           | <span data-ttu-id="2759a-227">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-227">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="2759a-228">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="2759a-228">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="2759a-229">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-229">public str name(\[str value\])</span></span>                                                                                      | <span data-ttu-id="2759a-230">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-230">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                               |
| <span data-ttu-id="2759a-231">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-231">public int neededPermission(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="2759a-232">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="2759a-232">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="2759a-233">public int panelStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-233">public int panelStyle(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="2759a-234">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="2759a-234">public FormControl parentControl()</span></span>                                                                                  | <span data-ttu-id="2759a-235">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-235">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="2759a-236">public str parentPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-236">public str parentPage(\[str value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="2759a-237">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-237">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="2759a-238">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-238">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="2759a-239">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-239">public int rightMarginValue(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="2759a-240">public int scrollbars(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-240">public int scrollbars(\[int value\])</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="2759a-241">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-241">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           | <span data-ttu-id="2759a-242">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-242">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="2759a-243">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="2759a-243">public int showContextMenu(int menuHandle)</span></span>                                                                          | <span data-ttu-id="2759a-244">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-244">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="2759a-245">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-245">public boolean skip(\[boolean value\])</span></span>                                                                              | <span data-ttu-id="2759a-246">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-246">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="2759a-247">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="2759a-247">public int sort(\[SortOrder sortDirection\])</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="2759a-248">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-248">public int style(\[int value\])</span></span>                                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="2759a-249">public int tabAppearance(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-249">public int tabAppearance(\[int value\])</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="2759a-250">public boolean tabAutoChange(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-250">public boolean tabAutoChange(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="2759a-251">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="2759a-251">public str toolTip()</span></span>                                                                                                | <span data-ttu-id="2759a-252">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-252">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="2759a-253">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-253">public int top(int value, \[int mode\])</span></span>                                                                             | <span data-ttu-id="2759a-254">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-254">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="2759a-255">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-255">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="2759a-256">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-256">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="2759a-257">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-257">public int topMarginValue(\[int value\])</span></span>                                                                            |                                                                                                                                                                         |
| <span data-ttu-id="2759a-258">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-258">public int topMode(\[int value\])</span></span>                                                                                   | <span data-ttu-id="2759a-259">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-259">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="2759a-260">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-260">public int topValue(\[int value\])</span></span>                                                                                  | <span data-ttu-id="2759a-261">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-261">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="2759a-262">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-262">public int type(\[int value\])</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="2759a-263">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="2759a-263">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="2759a-264">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-264">public int userData(\[int value\])</span></span>                                                                                  | <span data-ttu-id="2759a-265">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-265">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="2759a-266">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-266">public int userDataItem(\[int value\])</span></span>                                                                              | <span data-ttu-id="2759a-267">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-267">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="2759a-268">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-268">public int userDataItems(\[int value\])</span></span>                                                                             | <span data-ttu-id="2759a-269">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-269">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="2759a-270">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-270">public int userDisable(\[int value\])</span></span>                                                                               | <span data-ttu-id="2759a-271">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-271">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="2759a-272">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-272">public int userHeight(\[int value\])</span></span>                                                                                | <span data-ttu-id="2759a-273">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-273">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="2759a-274">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-274">public int userHide(\[int value\])</span></span>                                                                                  | <span data-ttu-id="2759a-275">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-275">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="2759a-276">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-276">public int userOrgContainer(\[int value\])</span></span>                                                                          | <span data-ttu-id="2759a-277">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-277">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="2759a-278">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-278">public int userOrgSibling(\[int value\])</span></span>                                                                            | <span data-ttu-id="2759a-279">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-279">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="2759a-280">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-280">public str userPromptText(\[str value\])</span></span>                                                                            | <span data-ttu-id="2759a-281">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-281">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="2759a-282">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-282">public int userSecurityLevel(\[int value\])</span></span>                                                                         | <span data-ttu-id="2759a-283">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-283">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="2759a-284">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-284">public int userSkip(\[int value\])</span></span>                                                                                  | <span data-ttu-id="2759a-285">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-285">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="2759a-286">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-286">public int userWidth(\[int value\])</span></span>                                                                                 | <span data-ttu-id="2759a-287">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-287">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="2759a-288">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-288">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="2759a-289">public boolean verticalScrollBarVisible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-289">public boolean verticalScrollBarVisible(\[boolean value\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="2759a-290">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-290">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        | <span data-ttu-id="2759a-291">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-291">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="2759a-292">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-292">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              | <span data-ttu-id="2759a-293">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-293">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="2759a-294">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-294">public int verticalSpacingValue(\[int value\])</span></span>                                                                      | <span data-ttu-id="2759a-295">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-295">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="2759a-296">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-296">public int viewEditMode(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="2759a-297">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-297">public boolean visible(\[boolean value\])</span></span>                                                                           | <span data-ttu-id="2759a-298">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-298">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="2759a-299">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2759a-299">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="2759a-300">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-300">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="2759a-301">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-301">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="2759a-302">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-302">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="2759a-303">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2759a-303">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="2759a-304">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-304">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="2759a-305">public void pageActivated()</span><span class="sxs-lookup"><span data-stu-id="2759a-305">public void pageActivated()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="2759a-306">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="2759a-306">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="2759a-307">public void collapse()</span><span class="sxs-lookup"><span data-stu-id="2759a-307">public void collapse()</span></span>                                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="2759a-308">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="2759a-308">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |                                                                                                                                                                         |
| <span data-ttu-id="2759a-309">private void OnExpanding(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="2759a-309">private void OnExpanding(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |                                                                                                                                                                         |
| <span data-ttu-id="2759a-310">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="2759a-310">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           | <span data-ttu-id="2759a-311">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2759a-311">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="2759a-312">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="2759a-312">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       | <span data-ttu-id="2759a-313">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-313">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="2759a-314">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="2759a-314">public void jumpRef()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="2759a-315">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="2759a-315">public void endDrag()</span></span>                                                                                               | <span data-ttu-id="2759a-316">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-316">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |
| <span data-ttu-id="2759a-317">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="2759a-317">public void filter(\[str filterStr\])</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="2759a-318">public void paste()</span><span class="sxs-lookup"><span data-stu-id="2759a-318">public void paste()</span></span>                                                                                                 | <span data-ttu-id="2759a-319">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2759a-319">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="2759a-320">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="2759a-320">public void setFocus()</span></span>                                                                                              | <span data-ttu-id="2759a-321">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-321">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="2759a-322">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="2759a-322">public void resetUserSetting()</span></span>                                                                                      | <span data-ttu-id="2759a-323">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="2759a-323">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="2759a-324">private void OnExpanded(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="2759a-324">private void OnExpanded(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="2759a-325">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="2759a-325">public void mouseLeave()</span></span>                                                                                            | <span data-ttu-id="2759a-326">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-326">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="2759a-327">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="2759a-327">public void arrange()</span></span>                                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="2759a-328">private void OnPageActivated(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="2759a-328">private void OnPageActivated(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="2759a-329">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="2759a-329">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               | <span data-ttu-id="2759a-330">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2759a-330">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="2759a-331">public void expand()</span><span class="sxs-lookup"><span data-stu-id="2759a-331">public void expand()</span></span>                                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="2759a-332">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="2759a-332">public void gotFocus()</span></span>                                                                                              | <span data-ttu-id="2759a-333">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-333">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="2759a-334">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="2759a-334">public void prefColumnSize(int width, int height)</span></span>                                                                   | <span data-ttu-id="2759a-335">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-335">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="2759a-336">public void copy()</span><span class="sxs-lookup"><span data-stu-id="2759a-336">public void copy()</span></span>                                                                                                  | <span data-ttu-id="2759a-337">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="2759a-337">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="2759a-338">public void activatePage()</span><span class="sxs-lookup"><span data-stu-id="2759a-338">public void activatePage()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="2759a-339">public void context()</span><span class="sxs-lookup"><span data-stu-id="2759a-339">public void context()</span></span>                                                                                               | <span data-ttu-id="2759a-340">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-340">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="2759a-341">public void cut()</span><span class="sxs-lookup"><span data-stu-id="2759a-341">public void cut()</span></span>                                                                                                   | <span data-ttu-id="2759a-342">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="2759a-342">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="2759a-343">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="2759a-343">public void lostFocus()</span></span>                                                                                             | <span data-ttu-id="2759a-344">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-344">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="2759a-345">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="2759a-345">public void displayControl()</span></span>                                                                                        | <span data-ttu-id="2759a-346">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-346">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="2759a-347">private void OnAllowPageDeactivate(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="2759a-347">private void OnAllowPageDeactivate(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                              |                                                                                                                                                                         |
| <span data-ttu-id="2759a-348">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="2759a-348">public void inputSearch(str searchStr)</span></span>                                                                              | <span data-ttu-id="2759a-349">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="2759a-349">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="2759a-350">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="2759a-350">public void dragLeave()</span></span>                                                                                             | <span data-ttu-id="2759a-351">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2759a-351">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="2759a-352">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="2759a-352">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |                                                                                                                                                                         |

## <a name="method-addcontrol"></a><span data-ttu-id="2759a-353">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="2759a-353">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="2759a-354">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="2759a-354">Parameters - addControl</span></span>

<span data-ttu-id="2759a-355">controlType</span><span class="sxs-lookup"><span data-stu-id="2759a-355">controlType</span></span>  

<!-- -->

<span data-ttu-id="2759a-356">controlName</span><span class="sxs-lookup"><span data-stu-id="2759a-356">controlName</span></span>  

<!-- -->

<span data-ttu-id="2759a-357">insertAfter</span><span class="sxs-lookup"><span data-stu-id="2759a-357">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="2759a-358">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="2759a-358">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="2759a-359">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="2759a-359">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="2759a-360">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="2759a-360">Parameters - addControlEx</span></span>

<span data-ttu-id="2759a-361">controlClass</span><span class="sxs-lookup"><span data-stu-id="2759a-361">controlClass</span></span>  

<!-- -->

<span data-ttu-id="2759a-362">controlName</span><span class="sxs-lookup"><span data-stu-id="2759a-362">controlName</span></span>  

<!-- -->

<span data-ttu-id="2759a-363">insertAfter</span><span class="sxs-lookup"><span data-stu-id="2759a-363">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="2759a-364">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="2759a-364">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="2759a-365">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="2759a-365">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="2759a-366">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="2759a-366">Parameters - addDataField</span></span>

<span data-ttu-id="2759a-367">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="2759a-367">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="2759a-368">fieldId</span><span class="sxs-lookup"><span data-stu-id="2759a-368">fieldId</span></span>  

<!-- -->

<span data-ttu-id="2759a-369">insertAfter</span><span class="sxs-lookup"><span data-stu-id="2759a-369">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="2759a-370">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="2759a-370">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="2759a-371">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="2759a-371">Return Value - addDataField</span></span>

## <a name="method-alignchild"></a><span data-ttu-id="2759a-372">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="2759a-372">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="2759a-373">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="2759a-373">Parameters - alignChild</span></span>

<span data-ttu-id="2759a-374">値</span><span class="sxs-lookup"><span data-stu-id="2759a-374">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="2759a-375">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="2759a-375">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="2759a-376">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="2759a-376">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="2759a-377">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="2759a-377">Parameters - alignChildren</span></span>

<span data-ttu-id="2759a-378">値</span><span class="sxs-lookup"><span data-stu-id="2759a-378">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="2759a-379">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="2759a-379">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="2759a-380">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="2759a-380">Method alignControl</span></span>

<span data-ttu-id="2759a-381">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-381">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="2759a-382">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="2759a-382">Parameters - alignControl</span></span>

<span data-ttu-id="2759a-383">値</span><span class="sxs-lookup"><span data-stu-id="2759a-383">value</span></span>  
<span data-ttu-id="2759a-384">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-384">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="2759a-385">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="2759a-385">Return Value - alignControl</span></span>

<span data-ttu-id="2759a-386">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="2759a-386">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="2759a-387">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="2759a-387">Remarks - alignControl</span></span>

<span data-ttu-id="2759a-388">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-388">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="2759a-389">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="2759a-389">Method allowEdit</span></span>

<span data-ttu-id="2759a-390">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-390">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="2759a-391">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2759a-391">Parameters - allowEdit</span></span>

<span data-ttu-id="2759a-392">値</span><span class="sxs-lookup"><span data-stu-id="2759a-392">value</span></span>  
<span data-ttu-id="2759a-393">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="2759a-393">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="2759a-394">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2759a-394">Return Value - allowEdit</span></span>

<span data-ttu-id="2759a-395">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2759a-395">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="2759a-396">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2759a-396">Remarks - allowEdit</span></span>

<span data-ttu-id="2759a-397">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="2759a-397">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowpagedeactivate"></a><span data-ttu-id="2759a-398">メソッド allowPageDeactivate</span><span class="sxs-lookup"><span data-stu-id="2759a-398">Method allowPageDeactivate</span></span>

```xpp
public boolean allowPageDeactivate()
```

### <a name="return-value---allowpagedeactivate"></a><span data-ttu-id="2759a-399">戻り値 - allowPageDeactivate</span><span class="sxs-lookup"><span data-stu-id="2759a-399">Return Value - allowPageDeactivate</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="2759a-400">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="2759a-400">Method allowSysSetup</span></span>

<span data-ttu-id="2759a-401">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-401">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="2759a-402">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="2759a-402">Return Value - allowSysSetup</span></span>

<span data-ttu-id="2759a-403">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2759a-403">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="2759a-404">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="2759a-404">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="2759a-405">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="2759a-405">Parameters - allowUserSetup</span></span>

<span data-ttu-id="2759a-406">値</span><span class="sxs-lookup"><span data-stu-id="2759a-406">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="2759a-407">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="2759a-407">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="2759a-408">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="2759a-408">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="2759a-409">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="2759a-409">Parameters - arrangeGuide</span></span>

<span data-ttu-id="2759a-410">値</span><span class="sxs-lookup"><span data-stu-id="2759a-410">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="2759a-411">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="2759a-411">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="2759a-412">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="2759a-412">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="2759a-413">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="2759a-413">Parameters - arrangeMethod</span></span>

<span data-ttu-id="2759a-414">値</span><span class="sxs-lookup"><span data-stu-id="2759a-414">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="2759a-415">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="2759a-415">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="2759a-416">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="2759a-416">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="2759a-417">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="2759a-417">Parameters - arrangeWhen</span></span>

<span data-ttu-id="2759a-418">値</span><span class="sxs-lookup"><span data-stu-id="2759a-418">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="2759a-419">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="2759a-419">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="2759a-420">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2759a-420">Method autoDeclaration</span></span>

<span data-ttu-id="2759a-421">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-421">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="2759a-422">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2759a-422">Parameters - autoDeclaration</span></span>

<span data-ttu-id="2759a-423">値</span><span class="sxs-lookup"><span data-stu-id="2759a-423">value</span></span>  
<span data-ttu-id="2759a-424">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-424">The new value of the property; optional</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="2759a-425">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2759a-425">Return Value - autoDeclaration</span></span>

<span data-ttu-id="2759a-426">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2759a-426">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="2759a-427">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2759a-427">Remarks - autoDeclaration</span></span>

<span data-ttu-id="2759a-428">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="2759a-428">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="2759a-429">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2759a-429">Method backgroundColor</span></span>

<span data-ttu-id="2759a-430">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-430">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="2759a-431">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2759a-431">Parameters - backgroundColor</span></span>

<span data-ttu-id="2759a-432">値</span><span class="sxs-lookup"><span data-stu-id="2759a-432">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="2759a-433">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2759a-433">Return Value - backgroundColor</span></span>

<span data-ttu-id="2759a-434">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="2759a-434">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="2759a-435">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2759a-435">Remarks - backgroundColor</span></span>

<span data-ttu-id="2759a-436">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2759a-436">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="2759a-437">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2759a-437">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="2759a-438">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="2759a-438">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="2759a-439">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="2759a-439">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="2759a-440">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2759a-440">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="2759a-441">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="2759a-441">The maximum value for a single byte is 255.</span></span>

## <a name="method-backgroundimage"></a><span data-ttu-id="2759a-442">メソッド backgroundImage</span><span class="sxs-lookup"><span data-stu-id="2759a-442">Method backgroundImage</span></span>

```xpp
public Image backgroundImage([Image image], [int drawMode])
```

### <a name="parameters---backgroundimage"></a><span data-ttu-id="2759a-443">パラメーター - backgroundImage</span><span class="sxs-lookup"><span data-stu-id="2759a-443">Parameters - backgroundImage</span></span>

<span data-ttu-id="2759a-444">画像</span><span class="sxs-lookup"><span data-stu-id="2759a-444">image</span></span>  

<!-- -->

<span data-ttu-id="2759a-445">drawMode</span><span class="sxs-lookup"><span data-stu-id="2759a-445">drawMode</span></span>  

### <a name="return-value---backgroundimage"></a><span data-ttu-id="2759a-446">戻り値 - backgroundImage</span><span class="sxs-lookup"><span data-stu-id="2759a-446">Return Value - backgroundImage</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="2759a-447">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="2759a-447">Method backStyle</span></span>

<span data-ttu-id="2759a-448">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-448">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="2759a-449">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="2759a-449">Parameters - backStyle</span></span>

<span data-ttu-id="2759a-450">値</span><span class="sxs-lookup"><span data-stu-id="2759a-450">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="2759a-451">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="2759a-451">Return Value - backStyle</span></span>

<span data-ttu-id="2759a-452">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="2759a-452">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="2759a-453">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="2759a-453">Method beginDrag</span></span>

<span data-ttu-id="2759a-454">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-454">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="2759a-455">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="2759a-455">Parameters - beginDrag</span></span>

<span data-ttu-id="2759a-456">x</span><span class="sxs-lookup"><span data-stu-id="2759a-456">x</span></span>  
<span data-ttu-id="2759a-457">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-457">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="2759a-458">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="2759a-458">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="2759a-459">y</span><span class="sxs-lookup"><span data-stu-id="2759a-459">y</span></span>  
<span data-ttu-id="2759a-460">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-460">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="2759a-461">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="2759a-461">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="2759a-462">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="2759a-462">Return Value - beginDrag</span></span>

<span data-ttu-id="2759a-463">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2759a-463">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="2759a-464">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="2759a-464">Remarks - beginDrag</span></span>

<span data-ttu-id="2759a-465">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="2759a-465">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="2759a-466">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="2759a-466">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="2759a-467">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-467">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="2759a-468">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-468">Parameters - bottomMargin</span></span>

<span data-ttu-id="2759a-469">値</span><span class="sxs-lookup"><span data-stu-id="2759a-469">value</span></span>  

<!-- -->

<span data-ttu-id="2759a-470">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-470">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="2759a-471">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-471">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="2759a-472">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-472">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="2759a-473">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-473">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="2759a-474">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-474">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="2759a-475">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-475">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="2759a-476">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-476">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="2759a-477">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-477">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="2759a-478">値</span><span class="sxs-lookup"><span data-stu-id="2759a-478">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="2759a-479">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-479">Return Value - bottomMarginValue</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="2759a-480">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="2759a-480">Method calcControlSize</span></span>

<span data-ttu-id="2759a-481">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-481">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="2759a-482">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="2759a-482">Parameters - calcControlSize</span></span>

<span data-ttu-id="2759a-483">chars</span><span class="sxs-lookup"><span data-stu-id="2759a-483">chars</span></span>  
<span data-ttu-id="2759a-484">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="2759a-484">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="2759a-485">明細行</span><span class="sxs-lookup"><span data-stu-id="2759a-485">lines</span></span>  
<span data-ttu-id="2759a-486">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="2759a-486">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="2759a-487">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="2759a-487">Return Value - calcControlSize</span></span>

<span data-ttu-id="2759a-488">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="2759a-488">The container that holds the width and height.</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="2759a-489">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="2759a-489">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="2759a-490">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="2759a-490">Parameters - canAddDataField</span></span>

<span data-ttu-id="2759a-491">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="2759a-491">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="2759a-492">fieldId</span><span class="sxs-lookup"><span data-stu-id="2759a-492">fieldId</span></span>  

<!-- -->

<span data-ttu-id="2759a-493">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="2759a-493">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="2759a-494">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="2759a-494">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="2759a-495">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="2759a-495">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="2759a-496">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="2759a-496">Parameters - canContain</span></span>

<span data-ttu-id="2759a-497">control</span><span class="sxs-lookup"><span data-stu-id="2759a-497">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="2759a-498">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="2759a-498">Return Value - canContain</span></span>

## <a name="method-caption"></a><span data-ttu-id="2759a-499">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="2759a-499">Method caption</span></span>

<span data-ttu-id="2759a-500">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-500">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="2759a-501">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="2759a-501">Parameters - caption</span></span>

<span data-ttu-id="2759a-502">値</span><span class="sxs-lookup"><span data-stu-id="2759a-502">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="2759a-503">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="2759a-503">Return Value - caption</span></span>

<span data-ttu-id="2759a-504">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="2759a-504">The string that is used as the caption of the control.</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="2759a-505">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="2759a-505">Method colorScheme</span></span>

<span data-ttu-id="2759a-506">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-506">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="2759a-507">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="2759a-507">Parameters - colorScheme</span></span>

<span data-ttu-id="2759a-508">値</span><span class="sxs-lookup"><span data-stu-id="2759a-508">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="2759a-509">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="2759a-509">Return Value - colorScheme</span></span>

<span data-ttu-id="2759a-510">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="2759a-510">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="2759a-511">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="2759a-511">Remarks - colorScheme</span></span>

<span data-ttu-id="2759a-512">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-512">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="2759a-513">金額</span><span class="sxs-lookup"><span data-stu-id="2759a-513">Value</span></span> | <span data-ttu-id="2759a-514">スタイル</span><span class="sxs-lookup"><span data-stu-id="2759a-514">Style</span></span>                        |
|-------|------------------------------|
| <span data-ttu-id="2759a-515">0</span><span class="sxs-lookup"><span data-stu-id="2759a-515">0</span></span>     | <span data-ttu-id="2759a-516">既定</span><span class="sxs-lookup"><span data-stu-id="2759a-516">Default</span></span>                      |
| <span data-ttu-id="2759a-517">1</span><span class="sxs-lookup"><span data-stu-id="2759a-517">1</span></span>     | <span data-ttu-id="2759a-518">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="2759a-518">The Microsoft Windows palette</span></span> |
| <span data-ttu-id="2759a-519">2</span><span class="sxs-lookup"><span data-stu-id="2759a-519">2</span></span>     | <span data-ttu-id="2759a-520">真の配色</span><span class="sxs-lookup"><span data-stu-id="2759a-520">The true-color scheme</span></span>        |

## <a name="method-columns"></a><span data-ttu-id="2759a-521">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="2759a-521">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="2759a-522">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="2759a-522">Parameters - columns</span></span>

<span data-ttu-id="2759a-523">値</span><span class="sxs-lookup"><span data-stu-id="2759a-523">value</span></span>  

<!-- -->

<span data-ttu-id="2759a-524">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-524">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="2759a-525">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="2759a-525">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="2759a-526">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="2759a-526">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="2759a-527">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="2759a-527">Parameters - columnsMode</span></span>

<span data-ttu-id="2759a-528">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-528">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="2759a-529">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="2759a-529">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="2759a-530">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="2759a-530">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="2759a-531">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="2759a-531">Parameters - columnspace</span></span>

<span data-ttu-id="2759a-532">値</span><span class="sxs-lookup"><span data-stu-id="2759a-532">value</span></span>  

<!-- -->

<span data-ttu-id="2759a-533">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-533">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="2759a-534">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="2759a-534">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="2759a-535">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="2759a-535">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="2759a-536">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="2759a-536">Parameters - columnspaceMode</span></span>

<span data-ttu-id="2759a-537">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-537">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="2759a-538">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="2759a-538">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="2759a-539">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="2759a-539">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="2759a-540">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="2759a-540">Parameters - columnspaceValue</span></span>

<span data-ttu-id="2759a-541">値</span><span class="sxs-lookup"><span data-stu-id="2759a-541">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="2759a-542">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="2759a-542">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="2759a-543">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="2759a-543">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="2759a-544">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="2759a-544">Parameters - columnsValue</span></span>

<span data-ttu-id="2759a-545">値</span><span class="sxs-lookup"><span data-stu-id="2759a-545">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="2759a-546">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="2759a-546">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="2759a-547">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="2759a-547">Method configurationKey</span></span>

<span data-ttu-id="2759a-548">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-548">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="2759a-549">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2759a-549">Parameters - configurationKey</span></span>

<span data-ttu-id="2759a-550">値</span><span class="sxs-lookup"><span data-stu-id="2759a-550">value</span></span>  
<span data-ttu-id="2759a-551">コントロールに割り当てるコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-551">The ID of the configuration key to assign to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="2759a-552">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2759a-552">Return Value - configurationKey</span></span>

<span data-ttu-id="2759a-553">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="2759a-553">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="2759a-554">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2759a-554">Remarks - configurationKey</span></span>

<span data-ttu-id="2759a-555">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-555">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="2759a-556">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="2759a-556">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="2759a-557">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="2759a-557">Method configurationKeyEx</span></span>

<span data-ttu-id="2759a-558">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-558">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="2759a-559">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="2759a-559">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="2759a-560">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="2759a-560">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="2759a-561">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="2759a-561">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="2759a-562">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="2759a-562">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="2759a-563">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="2759a-563">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="2759a-564">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2759a-564">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-containerscrollhorizontaloffset"></a><span data-ttu-id="2759a-565">メソッド containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="2759a-565">Method containerScrollHorizontalOffset</span></span>

```xpp
public int containerScrollHorizontalOffset([int value])
```

### <a name="parameters---containerscrollhorizontaloffset"></a><span data-ttu-id="2759a-566">パラメーター - containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="2759a-566">Parameters - containerScrollHorizontalOffset</span></span>

<span data-ttu-id="2759a-567">値</span><span class="sxs-lookup"><span data-stu-id="2759a-567">value</span></span>  

### <a name="return-value---containerscrollhorizontaloffset"></a><span data-ttu-id="2759a-568">戻り値 - containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="2759a-568">Return Value - containerScrollHorizontalOffset</span></span>

## <a name="method-containerscrollverticaloffset"></a><span data-ttu-id="2759a-569">メソッド containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="2759a-569">Method containerScrollVerticalOffset</span></span>

```xpp
public int containerScrollVerticalOffset([int value])
```

### <a name="parameters---containerscrollverticaloffset"></a><span data-ttu-id="2759a-570">パラメーター - containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="2759a-570">Parameters - containerScrollVerticalOffset</span></span>

<span data-ttu-id="2759a-571">値</span><span class="sxs-lookup"><span data-stu-id="2759a-571">value</span></span>  

### <a name="return-value---containerscrollverticaloffset"></a><span data-ttu-id="2759a-572">戻り値 - containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="2759a-572">Return Value - containerScrollVerticalOffset</span></span>

## <a name="method-contains"></a><span data-ttu-id="2759a-573">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="2759a-573">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="2759a-574">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="2759a-574">Parameters - contains</span></span>

<span data-ttu-id="2759a-575">control</span><span class="sxs-lookup"><span data-stu-id="2759a-575">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="2759a-576">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="2759a-576">Return Value - contains</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="2759a-577">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="2759a-577">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="2759a-578">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="2759a-578">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="2759a-579">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="2759a-579">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="2759a-580">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="2759a-580">Parameters - controlNum</span></span>

<span data-ttu-id="2759a-581">controlNo</span><span class="sxs-lookup"><span data-stu-id="2759a-581">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="2759a-582">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="2759a-582">Return Value - controlNum</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="2759a-583">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2759a-583">Method countryRegionCodes</span></span>

<span data-ttu-id="2759a-584">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-584">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="2759a-585">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2759a-585">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="2759a-586">値</span><span class="sxs-lookup"><span data-stu-id="2759a-586">value</span></span>  
<span data-ttu-id="2759a-587">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-587">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="2759a-588">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2759a-588">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="2759a-589">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="2759a-589">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="2759a-590">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="2759a-590">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="2759a-591">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="2759a-591">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="2759a-592">値</span><span class="sxs-lookup"><span data-stu-id="2759a-592">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="2759a-593">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="2759a-593">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="2759a-594">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2759a-594">Method dataRelationPath</span></span>

<span data-ttu-id="2759a-595">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-595">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="2759a-596">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2759a-596">Parameters - dataRelationPath</span></span>

<span data-ttu-id="2759a-597">値</span><span class="sxs-lookup"><span data-stu-id="2759a-597">value</span></span>  
<span data-ttu-id="2759a-598">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-598">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="2759a-599">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2759a-599">Return Value - dataRelationPath</span></span>

<span data-ttu-id="2759a-600">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="2759a-600">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="2759a-601">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2759a-601">Remarks - dataRelationPath</span></span>

<span data-ttu-id="2759a-602">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="2759a-602">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="2759a-603">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="2759a-603">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="2759a-604">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="2759a-604">Method dataSource</span></span>

<span data-ttu-id="2759a-605">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-605">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="2759a-606">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="2759a-606">Parameters - dataSource</span></span>

<span data-ttu-id="2759a-607">値</span><span class="sxs-lookup"><span data-stu-id="2759a-607">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="2759a-608">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="2759a-608">Return Value - dataSource</span></span>

<span data-ttu-id="2759a-609">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="2759a-609">The identifier of the data source that will be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="2759a-610">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="2759a-610">Method displayTarget</span></span>

<span data-ttu-id="2759a-611">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-611">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="2759a-612">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="2759a-612">Parameters - displayTarget</span></span>

<span data-ttu-id="2759a-613">値</span><span class="sxs-lookup"><span data-stu-id="2759a-613">value</span></span>  
<span data-ttu-id="2759a-614">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-614">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="2759a-615">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="2759a-615">Return Value - displayTarget</span></span>

<span data-ttu-id="2759a-616">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="2759a-616">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="2759a-617">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="2759a-617">Method dragDrop</span></span>

<span data-ttu-id="2759a-618">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-618">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="2759a-619">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="2759a-619">Parameters - dragDrop</span></span>

<span data-ttu-id="2759a-620">値</span><span class="sxs-lookup"><span data-stu-id="2759a-620">value</span></span>  
<span data-ttu-id="2759a-621">ドラッグ アンド ドロップの動作を有効にするかどうかを示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-621">An integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="2759a-622">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="2759a-622">Return Value - dragDrop</span></span>

<span data-ttu-id="2759a-623">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="2759a-623">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="2759a-624">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="2759a-624">Remarks - dragDrop</span></span>

<span data-ttu-id="2759a-625">dragLeave メソッド、dragOver メソッド、および dragOverEx メソッドを使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-625">Use the dragLeave Method, the dragOver Method, and the dragOverEx Method to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="2759a-626">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="2759a-626">Method dragOver</span></span>

<span data-ttu-id="2759a-627">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2759a-627">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="2759a-628">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="2759a-628">Parameters - dragOver</span></span>

<span data-ttu-id="2759a-629">dragSource</span><span class="sxs-lookup"><span data-stu-id="2759a-629">dragSource</span></span>  
<span data-ttu-id="2759a-630">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-630">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-631">dragMode</span><span class="sxs-lookup"><span data-stu-id="2759a-631">dragMode</span></span>  
<span data-ttu-id="2759a-632">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-632">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-633">x</span><span class="sxs-lookup"><span data-stu-id="2759a-633">x</span></span>  
<span data-ttu-id="2759a-634">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-634">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-635">y</span><span class="sxs-lookup"><span data-stu-id="2759a-635">y</span></span>  
<span data-ttu-id="2759a-636">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-636">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="2759a-637">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="2759a-637">Return Value - dragOver</span></span>

<span data-ttu-id="2759a-638">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="2759a-638">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="2759a-639">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="2759a-639">Method dragOverEx</span></span>

<span data-ttu-id="2759a-640">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2759a-640">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="2759a-641">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="2759a-641">Parameters - dragOverEx</span></span>

<span data-ttu-id="2759a-642">dragSource</span><span class="sxs-lookup"><span data-stu-id="2759a-642">dragSource</span></span>  
<span data-ttu-id="2759a-643">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-643">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-644">dragMode</span><span class="sxs-lookup"><span data-stu-id="2759a-644">dragMode</span></span>  
<span data-ttu-id="2759a-645">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-645">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-646">x</span><span class="sxs-lookup"><span data-stu-id="2759a-646">x</span></span>  
<span data-ttu-id="2759a-647">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-647">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-648">y</span><span class="sxs-lookup"><span data-stu-id="2759a-648">y</span></span>  
<span data-ttu-id="2759a-649">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-649">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="2759a-650">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="2759a-650">Return Value - dragOverEx</span></span>

<span data-ttu-id="2759a-651">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="2759a-651">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="2759a-652">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="2759a-652">Method dragText</span></span>

<span data-ttu-id="2759a-653">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-653">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="2759a-654">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="2759a-654">Return Value - dragText</span></span>

<span data-ttu-id="2759a-655">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="2759a-655">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="2759a-656">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="2759a-656">Method enabled</span></span>

<span data-ttu-id="2759a-657">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-657">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="2759a-658">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="2759a-658">Parameters - enabled</span></span>

<span data-ttu-id="2759a-659">値</span><span class="sxs-lookup"><span data-stu-id="2759a-659">value</span></span>  
<span data-ttu-id="2759a-660">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-660">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="2759a-661">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="2759a-661">Return Value - enabled</span></span>

<span data-ttu-id="2759a-662">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2759a-662">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="2759a-663">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="2759a-663">Remarks - enabled</span></span>

<span data-ttu-id="2759a-664">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="2759a-664">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="2759a-665">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2759a-665">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="2759a-666">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="2759a-666">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-fasttabexpanded"></a><span data-ttu-id="2759a-667">メソッド fastTabExpanded</span><span class="sxs-lookup"><span data-stu-id="2759a-667">Method fastTabExpanded</span></span>

```xpp
public int fastTabExpanded([int value])
```

### <a name="parameters---fasttabexpanded"></a><span data-ttu-id="2759a-668">パラメーター - fastTabExpanded</span><span class="sxs-lookup"><span data-stu-id="2759a-668">Parameters - fastTabExpanded</span></span>

<span data-ttu-id="2759a-669">値</span><span class="sxs-lookup"><span data-stu-id="2759a-669">value</span></span>  

### <a name="return-value---fasttabexpanded"></a><span data-ttu-id="2759a-670">戻り値 - fastTabExpanded</span><span class="sxs-lookup"><span data-stu-id="2759a-670">Return Value - fastTabExpanded</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="2759a-671">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="2759a-671">Method hasChanged</span></span>

<span data-ttu-id="2759a-672">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-672">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="2759a-673">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="2759a-673">Parameters - hasChanged</span></span>

<span data-ttu-id="2759a-674">val</span><span class="sxs-lookup"><span data-stu-id="2759a-674">val</span></span>  
<span data-ttu-id="2759a-675">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-675">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="2759a-676">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="2759a-676">Return Value - hasChanged</span></span>

<span data-ttu-id="2759a-677">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2759a-677">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="2759a-678">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="2759a-678">Method hasUserSetting</span></span>

<span data-ttu-id="2759a-679">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-679">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="2759a-680">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="2759a-680">Return Value - hasUserSetting</span></span>

<span data-ttu-id="2759a-681">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2759a-681">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="2759a-682">メソッド height</span><span class="sxs-lookup"><span data-stu-id="2759a-682">Method height</span></span>

<span data-ttu-id="2759a-683">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-683">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="2759a-684">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="2759a-684">Parameters - height</span></span>

<span data-ttu-id="2759a-685">値</span><span class="sxs-lookup"><span data-stu-id="2759a-685">value</span></span>  
<span data-ttu-id="2759a-686">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-686">An integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="2759a-687">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-687">mode</span></span>  
<span data-ttu-id="2759a-688">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-688">An integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="2759a-689">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="2759a-689">Return Value - height</span></span>

<span data-ttu-id="2759a-690">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="2759a-690">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="2759a-691">備考 - height</span><span class="sxs-lookup"><span data-stu-id="2759a-691">Remarks - height</span></span>

<span data-ttu-id="2759a-692">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-692">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="2759a-693">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="2759a-693">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="2759a-694">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-694">Mode</span></span>            | <span data-ttu-id="2759a-695">高さの計算</span><span class="sxs-lookup"><span data-stu-id="2759a-695">Height calculation</span></span>                                                                        |
|-----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2759a-696">-1 正確</span><span class="sxs-lookup"><span data-stu-id="2759a-696">-1 Exact</span></span>        | <span data-ttu-id="2759a-697">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-697">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2759a-698">0 自動</span><span class="sxs-lookup"><span data-stu-id="2759a-698">0 Auto</span></span>          | <span data-ttu-id="2759a-699">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-699">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2759a-700">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="2759a-700">1 Column height</span></span> | <span data-ttu-id="2759a-701">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="2759a-701">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="2759a-702">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2759a-702">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="2759a-703">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="2759a-703">Method heightMode</span></span>

<span data-ttu-id="2759a-704">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-704">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="2759a-705">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="2759a-705">Parameters - heightMode</span></span>

<span data-ttu-id="2759a-706">値</span><span class="sxs-lookup"><span data-stu-id="2759a-706">value</span></span>  
<span data-ttu-id="2759a-707">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-707">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="2759a-708">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="2759a-708">Return Value - heightMode</span></span>

<span data-ttu-id="2759a-709">計算モード。</span><span class="sxs-lookup"><span data-stu-id="2759a-709">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="2759a-710">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="2759a-710">Remarks - heightMode</span></span>

<span data-ttu-id="2759a-711">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="2759a-711">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="2759a-712">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-712">Mode</span></span>          | <span data-ttu-id="2759a-713">高さの計算</span><span class="sxs-lookup"><span data-stu-id="2759a-713">Height calculation</span></span>                                                                        |
|---------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2759a-714">正確</span><span class="sxs-lookup"><span data-stu-id="2759a-714">Exact</span></span>         | <span data-ttu-id="2759a-715">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-715">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2759a-716">自動</span><span class="sxs-lookup"><span data-stu-id="2759a-716">Auto</span></span>          | <span data-ttu-id="2759a-717">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-717">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2759a-718">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="2759a-718">Column height</span></span> | <span data-ttu-id="2759a-719">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="2759a-719">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="2759a-720">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="2759a-720">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="2759a-721">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="2759a-721">Method heightValue</span></span>

<span data-ttu-id="2759a-722">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-722">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="2759a-723">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="2759a-723">Parameters - heightValue</span></span>

<span data-ttu-id="2759a-724">値</span><span class="sxs-lookup"><span data-stu-id="2759a-724">value</span></span>  
<span data-ttu-id="2759a-725">高さをピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-725">An integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="2759a-726">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="2759a-726">Return Value - heightValue</span></span>

<span data-ttu-id="2759a-727">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="2759a-727">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="2759a-728">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="2759a-728">Remarks - heightValue</span></span>

<span data-ttu-id="2759a-729">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="2759a-729">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="2759a-730">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="2759a-730">Method helpField</span></span>

<span data-ttu-id="2759a-731">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-731">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="2759a-732">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="2759a-732">Return Value - helpField</span></span>

<span data-ttu-id="2759a-733">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="2759a-733">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="2759a-734">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="2759a-734">Remarks - helpField</span></span>

<span data-ttu-id="2759a-735">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="2759a-735">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="2759a-736">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2759a-736">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="2759a-737">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="2759a-737">Method helpText</span></span>

<span data-ttu-id="2759a-738">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-738">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="2759a-739">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="2759a-739">Parameters - helpText</span></span>

<span data-ttu-id="2759a-740">値</span><span class="sxs-lookup"><span data-stu-id="2759a-740">value</span></span>  
<span data-ttu-id="2759a-741">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="2759a-741">The value that is assigned as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="2759a-742">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="2759a-742">Return Value - helpText</span></span>

<span data-ttu-id="2759a-743">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="2759a-743">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="2759a-744">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="2759a-744">Remarks - helpText</span></span>

<span data-ttu-id="2759a-745">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-745">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="2759a-746">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="2759a-746">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="2759a-747">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="2759a-747">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="2759a-748">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="2759a-748">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="2759a-749">値</span><span class="sxs-lookup"><span data-stu-id="2759a-749">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="2759a-750">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="2759a-750">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="2759a-751">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2759a-751">Method hierarchyParent</span></span>

<span data-ttu-id="2759a-752">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-752">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="2759a-753">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2759a-753">Parameters - hierarchyParent</span></span>

<span data-ttu-id="2759a-754">値</span><span class="sxs-lookup"><span data-stu-id="2759a-754">value</span></span>  
<span data-ttu-id="2759a-755">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="2759a-755">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="2759a-756">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2759a-756">Return Value - hierarchyParent</span></span>

<span data-ttu-id="2759a-757">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="2759a-757">The HierarchyParent property value of the control.</span></span>

## <a name="method-horizontalscrollbarvisible"></a><span data-ttu-id="2759a-758">メソッド horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="2759a-758">Method horizontalScrollBarVisible</span></span>

```xpp
public boolean horizontalScrollBarVisible([boolean value])
```

### <a name="parameters---horizontalscrollbarvisible"></a><span data-ttu-id="2759a-759">パラメーター - horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="2759a-759">Parameters - horizontalScrollBarVisible</span></span>

<span data-ttu-id="2759a-760">値</span><span class="sxs-lookup"><span data-stu-id="2759a-760">value</span></span>  

### <a name="return-value---horizontalscrollbarvisible"></a><span data-ttu-id="2759a-761">戻り値 - horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="2759a-761">Return Value - horizontalScrollBarVisible</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="2759a-762">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="2759a-762">Method hWnd</span></span>

<span data-ttu-id="2759a-763">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-763">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="2759a-764">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="2759a-764">Return Value - hWnd</span></span>

<span data-ttu-id="2759a-765">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="2759a-765">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="2759a-766">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="2759a-766">Remarks - hWnd</span></span>

<span data-ttu-id="2759a-767">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="2759a-767">The handle can be used with the Windows API.</span></span>

## <a name="method-isactivepage"></a><span data-ttu-id="2759a-768">メソッド isActivePage</span><span class="sxs-lookup"><span data-stu-id="2759a-768">Method isActivePage</span></span>

```xpp
public boolean isActivePage()
```

### <a name="return-value---isactivepage"></a><span data-ttu-id="2759a-769">戻り値 - isActivePage</span><span class="sxs-lookup"><span data-stu-id="2759a-769">Return Value - isActivePage</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="2759a-770">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="2759a-770">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="2759a-771">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="2759a-771">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="2759a-772">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="2759a-772">Method isDisplayed</span></span>

<span data-ttu-id="2759a-773">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-773">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="2759a-774">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="2759a-774">Return Value - isDisplayed</span></span>

<span data-ttu-id="2759a-775">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="2759a-775">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="2759a-776">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="2759a-776">Remarks - isDisplayed</span></span>

<span data-ttu-id="2759a-777">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2759a-777">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isexpanded"></a><span data-ttu-id="2759a-778">メソッド isExpanded</span><span class="sxs-lookup"><span data-stu-id="2759a-778">Method isExpanded</span></span>

```xpp
public boolean isExpanded()
```

### <a name="return-value---isexpanded"></a><span data-ttu-id="2759a-779">戻り値 - isExpanded</span><span class="sxs-lookup"><span data-stu-id="2759a-779">Return Value - isExpanded</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="2759a-780">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="2759a-780">Method isRestricted</span></span>

<span data-ttu-id="2759a-781">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-781">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="2759a-782">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="2759a-782">Return Value - isRestricted</span></span>

<span data-ttu-id="2759a-783">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="2759a-783">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="2759a-784">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="2759a-784">Method isUserSetupEnabled</span></span>

<span data-ttu-id="2759a-785">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-785">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="2759a-786">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="2759a-786">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="2759a-787">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="2759a-787">neededSetupRights</span></span>  
<span data-ttu-id="2759a-788">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="2759a-788">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="2759a-789">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="2759a-789">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="2759a-790">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2759a-790">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="2759a-791">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="2759a-791">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="2759a-792">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="2759a-792">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2759a-793">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="2759a-793">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="2759a-794">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="2759a-794">No changes can be made to the control.</span></span> <span data-ttu-id="2759a-795">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-795">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="2759a-796">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="2759a-796">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="2759a-797">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="2759a-797">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="2759a-798">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="2759a-798">The user cannot move the control.</span></span>   |
| <span data-ttu-id="2759a-799">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="2759a-799">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="2759a-800">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="2759a-800">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="2759a-801">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="2759a-801">The user can also move the control.</span></span> |

<span data-ttu-id="2759a-802">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="2759a-802">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-left"></a><span data-ttu-id="2759a-803">メソッド left</span><span class="sxs-lookup"><span data-stu-id="2759a-803">Method left</span></span>

<span data-ttu-id="2759a-804">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-804">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="2759a-805">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="2759a-805">Parameters - left</span></span>

<span data-ttu-id="2759a-806">値</span><span class="sxs-lookup"><span data-stu-id="2759a-806">value</span></span>  
<span data-ttu-id="2759a-807">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-807">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="2759a-808">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-808">mode</span></span>  
<span data-ttu-id="2759a-809">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-809">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="2759a-810">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="2759a-810">Return Value - left</span></span>

<span data-ttu-id="2759a-811">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="2759a-811">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="2759a-812">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-812">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="2759a-813">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-813">Parameters - leftMargin</span></span>

<span data-ttu-id="2759a-814">値</span><span class="sxs-lookup"><span data-stu-id="2759a-814">value</span></span>  

<!-- -->

<span data-ttu-id="2759a-815">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-815">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="2759a-816">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-816">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="2759a-817">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-817">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="2759a-818">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-818">Parameters - leftMarginMode</span></span>

<span data-ttu-id="2759a-819">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-819">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="2759a-820">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-820">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="2759a-821">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-821">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="2759a-822">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-822">Parameters - leftMarginValue</span></span>

<span data-ttu-id="2759a-823">値</span><span class="sxs-lookup"><span data-stu-id="2759a-823">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="2759a-824">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-824">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="2759a-825">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="2759a-825">Method leftMode</span></span>

<span data-ttu-id="2759a-826">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-826">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="2759a-827">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="2759a-827">Parameters - leftMode</span></span>

<span data-ttu-id="2759a-828">値</span><span class="sxs-lookup"><span data-stu-id="2759a-828">value</span></span>  
<span data-ttu-id="2759a-829">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-829">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="2759a-830">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="2759a-830">Return Value - leftMode</span></span>

<span data-ttu-id="2759a-831">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="2759a-831">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="2759a-832">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="2759a-832">Method leftValue</span></span>

<span data-ttu-id="2759a-833">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-833">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="2759a-834">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="2759a-834">Parameters - leftValue</span></span>

<span data-ttu-id="2759a-835">値</span><span class="sxs-lookup"><span data-stu-id="2759a-835">value</span></span>  
<span data-ttu-id="2759a-836">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-836">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="2759a-837">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="2759a-837">Return Value - leftValue</span></span>

<span data-ttu-id="2759a-838">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="2759a-838">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="2759a-839">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="2759a-839">Method markAsUserAdd</span></span>

<span data-ttu-id="2759a-840">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="2759a-840">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="2759a-841">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="2759a-841">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="2759a-842">値</span><span class="sxs-lookup"><span data-stu-id="2759a-842">value</span></span>  
<span data-ttu-id="2759a-843">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-843">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="2759a-844">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="2759a-844">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="2759a-845">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2759a-845">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="2759a-846">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="2759a-846">Method mouseDblClick</span></span>

<span data-ttu-id="2759a-847">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-847">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="2759a-848">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="2759a-848">Parameters - mouseDblClick</span></span>

<span data-ttu-id="2759a-849">x</span><span class="sxs-lookup"><span data-stu-id="2759a-849">x</span></span>  
<span data-ttu-id="2759a-850">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-850">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-851">y</span><span class="sxs-lookup"><span data-stu-id="2759a-851">y</span></span>  
<span data-ttu-id="2759a-852">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-852">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-853">ボタン</span><span class="sxs-lookup"><span data-stu-id="2759a-853">button</span></span>  
<span data-ttu-id="2759a-854">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-854">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-855">Ctrl</span><span class="sxs-lookup"><span data-stu-id="2759a-855">Ctrl</span></span>  
<span data-ttu-id="2759a-856">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-856">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-857">シフト</span><span class="sxs-lookup"><span data-stu-id="2759a-857">Shift</span></span>  
<span data-ttu-id="2759a-858">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-858">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="2759a-859">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="2759a-859">Return Value - mouseDblClick</span></span>

<span data-ttu-id="2759a-860">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2759a-860">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="2759a-861">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="2759a-861">Remarks - mouseDblClick</span></span>

<span data-ttu-id="2759a-862">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-862">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="2759a-863">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="2759a-863">Method mouseDown</span></span>

<span data-ttu-id="2759a-864">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-864">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="2759a-865">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="2759a-865">Parameters - mouseDown</span></span>

<span data-ttu-id="2759a-866">x</span><span class="sxs-lookup"><span data-stu-id="2759a-866">x</span></span>  
<span data-ttu-id="2759a-867">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-867">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-868">y</span><span class="sxs-lookup"><span data-stu-id="2759a-868">y</span></span>  
<span data-ttu-id="2759a-869">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-869">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-870">ボタン</span><span class="sxs-lookup"><span data-stu-id="2759a-870">button</span></span>  
<span data-ttu-id="2759a-871">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-871">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-872">Ctrl</span><span class="sxs-lookup"><span data-stu-id="2759a-872">Ctrl</span></span>  
<span data-ttu-id="2759a-873">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-873">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-874">シフト</span><span class="sxs-lookup"><span data-stu-id="2759a-874">Shift</span></span>  
<span data-ttu-id="2759a-875">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-875">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="2759a-876">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="2759a-876">Return Value - mouseDown</span></span>

<span data-ttu-id="2759a-877">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2759a-877">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="2759a-878">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="2759a-878">Remarks - mouseDown</span></span>

<span data-ttu-id="2759a-879">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-879">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="2759a-880">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-880">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="2759a-881">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="2759a-881">Method mouseMove</span></span>

<span data-ttu-id="2759a-882">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-882">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="2759a-883">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="2759a-883">Parameters - mouseMove</span></span>

<span data-ttu-id="2759a-884">x</span><span class="sxs-lookup"><span data-stu-id="2759a-884">x</span></span>  
<span data-ttu-id="2759a-885">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-885">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-886">y</span><span class="sxs-lookup"><span data-stu-id="2759a-886">y</span></span>  
<span data-ttu-id="2759a-887">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-887">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-888">ボタン</span><span class="sxs-lookup"><span data-stu-id="2759a-888">button</span></span>  
<span data-ttu-id="2759a-889">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-889">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-890">Ctrl</span><span class="sxs-lookup"><span data-stu-id="2759a-890">Ctrl</span></span>  
<span data-ttu-id="2759a-891">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-891">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-892">シフト</span><span class="sxs-lookup"><span data-stu-id="2759a-892">Shift</span></span>  
<span data-ttu-id="2759a-893">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-893">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="2759a-894">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="2759a-894">Return Value - mouseMove</span></span>

<span data-ttu-id="2759a-895">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2759a-895">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="2759a-896">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="2759a-896">Remarks - mouseMove</span></span>

<span data-ttu-id="2759a-897">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-897">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="2759a-898">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="2759a-898">Method mouseUp</span></span>

<span data-ttu-id="2759a-899">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-899">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="2759a-900">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="2759a-900">Parameters - mouseUp</span></span>

<span data-ttu-id="2759a-901">x</span><span class="sxs-lookup"><span data-stu-id="2759a-901">x</span></span>  
<span data-ttu-id="2759a-902">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-902">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-903">y</span><span class="sxs-lookup"><span data-stu-id="2759a-903">y</span></span>  
<span data-ttu-id="2759a-904">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-904">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-905">ボタン</span><span class="sxs-lookup"><span data-stu-id="2759a-905">button</span></span>  
<span data-ttu-id="2759a-906">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-906">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-907">Ctrl</span><span class="sxs-lookup"><span data-stu-id="2759a-907">Ctrl</span></span>  
<span data-ttu-id="2759a-908">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-908">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-909">シフト</span><span class="sxs-lookup"><span data-stu-id="2759a-909">Shift</span></span>  
<span data-ttu-id="2759a-910">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-910">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="2759a-911">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="2759a-911">Return Value - mouseUp</span></span>

<span data-ttu-id="2759a-912">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2759a-912">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="2759a-913">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="2759a-913">Remarks - mouseUp</span></span>

<span data-ttu-id="2759a-914">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-914">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="2759a-915">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-915">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="2759a-916">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="2759a-916">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="2759a-917">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="2759a-917">Parameters - moveControl</span></span>

<span data-ttu-id="2759a-918">controlId</span><span class="sxs-lookup"><span data-stu-id="2759a-918">controlId</span></span>  

<!-- -->

<span data-ttu-id="2759a-919">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="2759a-919">insertAfterId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="2759a-920">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="2759a-920">Return Value - moveControl</span></span>

## <a name="method-name"></a><span data-ttu-id="2759a-921">メソッド名</span><span class="sxs-lookup"><span data-stu-id="2759a-921">Method name</span></span>

<span data-ttu-id="2759a-922">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-922">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="2759a-923">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="2759a-923">Parameters - name</span></span>

<span data-ttu-id="2759a-924">値</span><span class="sxs-lookup"><span data-stu-id="2759a-924">value</span></span>  
<span data-ttu-id="2759a-925">コントロールに割り当てられた名前。</span><span class="sxs-lookup"><span data-stu-id="2759a-925">The name assigned to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="2759a-926">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="2759a-926">Return Value - name</span></span>

<span data-ttu-id="2759a-927">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="2759a-927">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="2759a-928">備考 - name</span><span class="sxs-lookup"><span data-stu-id="2759a-928">Remarks - name</span></span>

<span data-ttu-id="2759a-929">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2759a-929">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="2759a-930">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="2759a-930">Begins with a letter.</span></span>
-   <span data-ttu-id="2759a-931">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="2759a-931">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="2759a-932">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2759a-932">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="2759a-933">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="2759a-933">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="2759a-934">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="2759a-934">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="2759a-935">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="2759a-935">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="2759a-936">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="2759a-936">Parameters - neededPermission</span></span>

<span data-ttu-id="2759a-937">値</span><span class="sxs-lookup"><span data-stu-id="2759a-937">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="2759a-938">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="2759a-938">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="2759a-939">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="2759a-939">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="2759a-940">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="2759a-940">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-panelstyle"></a><span data-ttu-id="2759a-941">メソッド panelStyle</span><span class="sxs-lookup"><span data-stu-id="2759a-941">Method panelStyle</span></span>

```xpp
public int panelStyle([int value])
```

### <a name="parameters---panelstyle"></a><span data-ttu-id="2759a-942">パラメーター - panelStyle</span><span class="sxs-lookup"><span data-stu-id="2759a-942">Parameters - panelStyle</span></span>

<span data-ttu-id="2759a-943">値</span><span class="sxs-lookup"><span data-stu-id="2759a-943">value</span></span>  

### <a name="return-value---panelstyle"></a><span data-ttu-id="2759a-944">戻り値 - panelStyle</span><span class="sxs-lookup"><span data-stu-id="2759a-944">Return Value - panelStyle</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="2759a-945">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="2759a-945">Method parentControl</span></span>

<span data-ttu-id="2759a-946">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-946">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="2759a-947">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="2759a-947">Return Value - parentControl</span></span>

<span data-ttu-id="2759a-948">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="2759a-948">The parent control for the control.</span></span>

## <a name="method-parentpage"></a><span data-ttu-id="2759a-949">メソッド parentPage</span><span class="sxs-lookup"><span data-stu-id="2759a-949">Method parentPage</span></span>

```xpp
public str parentPage([str value])
```

### <a name="parameters---parentpage"></a><span data-ttu-id="2759a-950">パラメーター - parentPage</span><span class="sxs-lookup"><span data-stu-id="2759a-950">Parameters - parentPage</span></span>

<span data-ttu-id="2759a-951">値</span><span class="sxs-lookup"><span data-stu-id="2759a-951">value</span></span>  

### <a name="return-value---parentpage"></a><span data-ttu-id="2759a-952">戻り値 - parentPage</span><span class="sxs-lookup"><span data-stu-id="2759a-952">Return Value - parentPage</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="2759a-953">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-953">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="2759a-954">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-954">Parameters - rightMargin</span></span>

<span data-ttu-id="2759a-955">値</span><span class="sxs-lookup"><span data-stu-id="2759a-955">value</span></span>  

<!-- -->

<span data-ttu-id="2759a-956">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-956">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="2759a-957">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-957">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="2759a-958">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-958">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="2759a-959">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-959">Parameters - rightMarginMode</span></span>

<span data-ttu-id="2759a-960">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-960">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="2759a-961">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-961">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="2759a-962">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-962">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="2759a-963">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-963">Parameters - rightMarginValue</span></span>

<span data-ttu-id="2759a-964">値</span><span class="sxs-lookup"><span data-stu-id="2759a-964">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="2759a-965">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-965">Return Value - rightMarginValue</span></span>

## <a name="method-scrollbars"></a><span data-ttu-id="2759a-966">メソッド scrollbars</span><span class="sxs-lookup"><span data-stu-id="2759a-966">Method scrollbars</span></span>

```xpp
public int scrollbars([int value])
```

### <a name="parameters---scrollbars"></a><span data-ttu-id="2759a-967">パラメーター - scrollbars</span><span class="sxs-lookup"><span data-stu-id="2759a-967">Parameters - scrollbars</span></span>

<span data-ttu-id="2759a-968">値</span><span class="sxs-lookup"><span data-stu-id="2759a-968">value</span></span>  

### <a name="return-value---scrollbars"></a><span data-ttu-id="2759a-969">戻り値 - scrollbars</span><span class="sxs-lookup"><span data-stu-id="2759a-969">Return Value - scrollbars</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="2759a-970">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="2759a-970">Method securityKey</span></span>

<span data-ttu-id="2759a-971">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-971">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="2759a-972">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="2759a-972">Parameters - securityKey</span></span>

<span data-ttu-id="2759a-973">値</span><span class="sxs-lookup"><span data-stu-id="2759a-973">value</span></span>  
<span data-ttu-id="2759a-974">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-974">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="2759a-975">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="2759a-975">Return Value - securityKey</span></span>

<span data-ttu-id="2759a-976">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="2759a-976">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="2759a-977">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="2759a-977">Method showContextMenu</span></span>

<span data-ttu-id="2759a-978">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-978">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="2759a-979">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="2759a-979">Parameters - showContextMenu</span></span>

<span data-ttu-id="2759a-980">menuHandle</span><span class="sxs-lookup"><span data-stu-id="2759a-980">menuHandle</span></span>  
<span data-ttu-id="2759a-981">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="2759a-981">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="2759a-982">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="2759a-982">Return Value - showContextMenu</span></span>

<span data-ttu-id="2759a-983">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-983">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="2759a-984">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="2759a-984">Method skip</span></span>

<span data-ttu-id="2759a-985">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-985">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="2759a-986">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="2759a-986">Parameters - skip</span></span>

<span data-ttu-id="2759a-987">値</span><span class="sxs-lookup"><span data-stu-id="2759a-987">value</span></span>  
<span data-ttu-id="2759a-988">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-988">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="2759a-989">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="2759a-989">Return Value - skip</span></span>

<span data-ttu-id="2759a-990">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2759a-990">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="2759a-991">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="2759a-991">Remarks - skip</span></span>

<span data-ttu-id="2759a-992">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="2759a-992">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="2759a-993">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="2759a-993">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="2759a-994">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="2759a-994">Parameters - sort</span></span>

<span data-ttu-id="2759a-995">sortDirection</span><span class="sxs-lookup"><span data-stu-id="2759a-995">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="2759a-996">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="2759a-996">Return Value - sort</span></span>

## <a name="method-style"></a><span data-ttu-id="2759a-997">メソッド style</span><span class="sxs-lookup"><span data-stu-id="2759a-997">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="2759a-998">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="2759a-998">Parameters - style</span></span>

<span data-ttu-id="2759a-999">値</span><span class="sxs-lookup"><span data-stu-id="2759a-999">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="2759a-1000">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="2759a-1000">Return Value - style</span></span>

## <a name="method-tabappearance"></a><span data-ttu-id="2759a-1001">メソッド tabAppearance</span><span class="sxs-lookup"><span data-stu-id="2759a-1001">Method tabAppearance</span></span>

```xpp
public int tabAppearance([int value])
```

### <a name="parameters---tabappearance"></a><span data-ttu-id="2759a-1002">パラメーター - tabAppearance</span><span class="sxs-lookup"><span data-stu-id="2759a-1002">Parameters - tabAppearance</span></span>

<span data-ttu-id="2759a-1003">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1003">value</span></span>  

### <a name="return-value---tabappearance"></a><span data-ttu-id="2759a-1004">戻り値 - tabAppearance</span><span class="sxs-lookup"><span data-stu-id="2759a-1004">Return Value - tabAppearance</span></span>

## <a name="method-tabautochange"></a><span data-ttu-id="2759a-1005">メソッド tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="2759a-1005">Method tabAutoChange</span></span>

```xpp
public boolean tabAutoChange([boolean value])
```

### <a name="parameters---tabautochange"></a><span data-ttu-id="2759a-1006">パラメーター - tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="2759a-1006">Parameters - tabAutoChange</span></span>

<span data-ttu-id="2759a-1007">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1007">value</span></span>  

### <a name="return-value---tabautochange"></a><span data-ttu-id="2759a-1008">戻り値 - tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="2759a-1008">Return Value - tabAutoChange</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="2759a-1009">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="2759a-1009">Method toolTip</span></span>

<span data-ttu-id="2759a-1010">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1010">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="2759a-1011">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="2759a-1011">Return Value - toolTip</span></span>

<span data-ttu-id="2759a-1012">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="2759a-1012">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="2759a-1013">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="2759a-1013">Remarks - toolTip</span></span>

<span data-ttu-id="2759a-1014">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1014">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="2759a-1015">メソッド top</span><span class="sxs-lookup"><span data-stu-id="2759a-1015">Method top</span></span>

<span data-ttu-id="2759a-1016">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1016">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="2759a-1017">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="2759a-1017">Parameters - top</span></span>

<span data-ttu-id="2759a-1018">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1018">value</span></span>  
<span data-ttu-id="2759a-1019">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1019">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="2759a-1020">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-1020">mode</span></span>  
<span data-ttu-id="2759a-1021">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1021">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="2759a-1022">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="2759a-1022">Return Value - top</span></span>

<span data-ttu-id="2759a-1023">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="2759a-1023">The vertical position of the control in the form.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="2759a-1024">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-1024">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="2759a-1025">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-1025">Parameters - topMargin</span></span>

<span data-ttu-id="2759a-1026">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1026">value</span></span>  

<!-- -->

<span data-ttu-id="2759a-1027">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-1027">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="2759a-1028">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="2759a-1028">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="2759a-1029">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1029">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="2759a-1030">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1030">Parameters - topMarginMode</span></span>

<span data-ttu-id="2759a-1031">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-1031">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="2759a-1032">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1032">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="2759a-1033">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1033">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="2759a-1034">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1034">Parameters - topMarginValue</span></span>

<span data-ttu-id="2759a-1035">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1035">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="2759a-1036">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1036">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="2759a-1037">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1037">Method topMode</span></span>

<span data-ttu-id="2759a-1038">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1038">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="2759a-1039">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1039">Parameters - topMode</span></span>

<span data-ttu-id="2759a-1040">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1040">value</span></span>  
<span data-ttu-id="2759a-1041">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1041">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="2759a-1042">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1042">Return Value - topMode</span></span>

<span data-ttu-id="2759a-1043">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="2759a-1043">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="2759a-1044">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1044">Method topValue</span></span>

<span data-ttu-id="2759a-1045">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1045">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="2759a-1046">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1046">Parameters - topValue</span></span>

<span data-ttu-id="2759a-1047">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1047">value</span></span>  
<span data-ttu-id="2759a-1048">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1048">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="2759a-1049">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1049">Return Value - topValue</span></span>

<span data-ttu-id="2759a-1050">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="2759a-1050">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="2759a-1051">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="2759a-1051">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="2759a-1052">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="2759a-1052">Parameters - type</span></span>

<span data-ttu-id="2759a-1053">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1053">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="2759a-1054">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="2759a-1054">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="2759a-1055">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="2759a-1055">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="2759a-1056">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="2759a-1056">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="2759a-1057">データ</span><span class="sxs-lookup"><span data-stu-id="2759a-1057">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="2759a-1058">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="2759a-1058">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="2759a-1059">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="2759a-1059">Method userData</span></span>

<span data-ttu-id="2759a-1060">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1060">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="2759a-1061">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="2759a-1061">Parameters - userData</span></span>

<span data-ttu-id="2759a-1062">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1062">value</span></span>  
<span data-ttu-id="2759a-1063">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1063">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="2759a-1064">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="2759a-1064">Return Value - userData</span></span>

<span data-ttu-id="2759a-1065">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="2759a-1065">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="2759a-1066">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="2759a-1066">Method userDataItem</span></span>

<span data-ttu-id="2759a-1067">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1067">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="2759a-1068">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="2759a-1068">Parameters - userDataItem</span></span>

<span data-ttu-id="2759a-1069">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1069">value</span></span>  
<span data-ttu-id="2759a-1070">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1070">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="2759a-1071">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="2759a-1071">Return Value - userDataItem</span></span>

<span data-ttu-id="2759a-1072">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="2759a-1072">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="2759a-1073">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="2759a-1073">Method userDataItems</span></span>

<span data-ttu-id="2759a-1074">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1074">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="2759a-1075">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="2759a-1075">Parameters - userDataItems</span></span>

<span data-ttu-id="2759a-1076">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1076">value</span></span>  
<span data-ttu-id="2759a-1077">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1077">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="2759a-1078">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="2759a-1078">Return Value - userDataItems</span></span>

<span data-ttu-id="2759a-1079">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="2759a-1079">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="2759a-1080">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="2759a-1080">Method userDisable</span></span>

<span data-ttu-id="2759a-1081">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1081">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="2759a-1082">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="2759a-1082">Parameters - userDisable</span></span>

<span data-ttu-id="2759a-1083">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1083">value</span></span>  
<span data-ttu-id="2759a-1084">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1084">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="2759a-1085">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="2759a-1085">Return Value - userDisable</span></span>

<span data-ttu-id="2759a-1086">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="2759a-1086">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="2759a-1087">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="2759a-1087">Method userHeight</span></span>

<span data-ttu-id="2759a-1088">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1088">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="2759a-1089">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="2759a-1089">Parameters - userHeight</span></span>

<span data-ttu-id="2759a-1090">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1090">value</span></span>  
<span data-ttu-id="2759a-1091">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1091">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="2759a-1092">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="2759a-1092">Return Value - userHeight</span></span>

<span data-ttu-id="2759a-1093">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="2759a-1093">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="2759a-1094">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="2759a-1094">Method userHide</span></span>

<span data-ttu-id="2759a-1095">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1095">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="2759a-1096">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="2759a-1096">Parameters - userHide</span></span>

<span data-ttu-id="2759a-1097">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1097">value</span></span>  
<span data-ttu-id="2759a-1098">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1098">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="2759a-1099">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="2759a-1099">Return Value - userHide</span></span>

<span data-ttu-id="2759a-1100">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="2759a-1100">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="2759a-1101">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="2759a-1101">Remarks - userHide</span></span>

<span data-ttu-id="2759a-1102">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1102">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="2759a-1103">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1103">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="2759a-1104">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1104">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="2759a-1105">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="2759a-1105">Method userOrgContainer</span></span>

<span data-ttu-id="2759a-1106">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1106">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="2759a-1107">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="2759a-1107">Parameters - userOrgContainer</span></span>

<span data-ttu-id="2759a-1108">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1108">value</span></span>  
<span data-ttu-id="2759a-1109">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1109">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="2759a-1110">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="2759a-1110">Return Value - userOrgContainer</span></span>

<span data-ttu-id="2759a-1111">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="2759a-1111">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="2759a-1112">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="2759a-1112">Method userOrgSibling</span></span>

<span data-ttu-id="2759a-1113">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1113">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="2759a-1114">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="2759a-1114">Parameters - userOrgSibling</span></span>

<span data-ttu-id="2759a-1115">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1115">value</span></span>  
<span data-ttu-id="2759a-1116">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1116">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="2759a-1117">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="2759a-1117">Return Value - userOrgSibling</span></span>

<span data-ttu-id="2759a-1118">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="2759a-1118">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="2759a-1119">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="2759a-1119">Method userPromptText</span></span>

<span data-ttu-id="2759a-1120">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1120">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="2759a-1121">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="2759a-1121">Parameters - userPromptText</span></span>

<span data-ttu-id="2759a-1122">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1122">value</span></span>  
<span data-ttu-id="2759a-1123">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1123">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="2759a-1124">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="2759a-1124">Return Value - userPromptText</span></span>

<span data-ttu-id="2759a-1125">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="2759a-1125">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="2759a-1126">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="2759a-1126">Method userSecurityLevel</span></span>

<span data-ttu-id="2759a-1127">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1127">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="2759a-1128">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="2759a-1128">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="2759a-1129">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1129">value</span></span>  
<span data-ttu-id="2759a-1130">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1130">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="2759a-1131">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="2759a-1131">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="2759a-1132">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="2759a-1132">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="2759a-1133">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="2759a-1133">Method userSkip</span></span>

<span data-ttu-id="2759a-1134">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1134">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="2759a-1135">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="2759a-1135">Parameters - userSkip</span></span>

<span data-ttu-id="2759a-1136">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1136">value</span></span>  
<span data-ttu-id="2759a-1137">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1137">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="2759a-1138">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="2759a-1138">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="2759a-1139">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="2759a-1139">Return Value - userSkip</span></span>

<span data-ttu-id="2759a-1140">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="2759a-1140">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="2759a-1141">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="2759a-1141">Method userWidth</span></span>

<span data-ttu-id="2759a-1142">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1142">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="2759a-1143">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="2759a-1143">Parameters - userWidth</span></span>

<span data-ttu-id="2759a-1144">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1144">value</span></span>  
<span data-ttu-id="2759a-1145">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1145">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="2759a-1146">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="2759a-1146">Return Value - userWidth</span></span>

<span data-ttu-id="2759a-1147">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1147">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="2759a-1148">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="2759a-1148">Remarks - userWidth</span></span>

<span data-ttu-id="2759a-1149">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1149">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="2759a-1150">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="2759a-1150">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="2759a-1151">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1151">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="2759a-1152">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="2759a-1152">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="2759a-1153">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="2759a-1153">Parameters - useUserLayout</span></span>

<span data-ttu-id="2759a-1154">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1154">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="2759a-1155">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="2759a-1155">Return Value - useUserLayout</span></span>

## <a name="method-verticalscrollbarvisible"></a><span data-ttu-id="2759a-1156">メソッド verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="2759a-1156">Method verticalScrollBarVisible</span></span>

```xpp
public boolean verticalScrollBarVisible([boolean value])
```

### <a name="parameters---verticalscrollbarvisible"></a><span data-ttu-id="2759a-1157">パラメーター - verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="2759a-1157">Parameters - verticalScrollBarVisible</span></span>

<span data-ttu-id="2759a-1158">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1158">value</span></span>  

### <a name="return-value---verticalscrollbarvisible"></a><span data-ttu-id="2759a-1159">戻り値 - verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="2759a-1159">Return Value - verticalScrollBarVisible</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="2759a-1160">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2759a-1160">Method verticalSpacing</span></span>

<span data-ttu-id="2759a-1161">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1161">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="2759a-1162">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2759a-1162">Parameters - verticalSpacing</span></span>

<span data-ttu-id="2759a-1163">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1163">value</span></span>  
<span data-ttu-id="2759a-1164">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1164">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="2759a-1165">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-1165">mode</span></span>  
<span data-ttu-id="2759a-1166">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1166">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="2759a-1167">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2759a-1167">Return Value - verticalSpacing</span></span>

<span data-ttu-id="2759a-1168">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="2759a-1168">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="2759a-1169">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1169">Method verticalSpacingMode</span></span>

<span data-ttu-id="2759a-1170">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1170">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="2759a-1171">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1171">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="2759a-1172">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-1172">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="2759a-1173">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1173">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="2759a-1174">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="2759a-1174">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="2759a-1175">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1175">Method verticalSpacingValue</span></span>

<span data-ttu-id="2759a-1176">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1176">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="2759a-1177">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1177">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="2759a-1178">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1178">value</span></span>  
<span data-ttu-id="2759a-1179">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1179">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="2759a-1180">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1180">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="2759a-1181">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="2759a-1181">The vertical spacing of the control in the form.</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="2759a-1182">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1182">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="2759a-1183">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1183">Parameters - viewEditMode</span></span>

<span data-ttu-id="2759a-1184">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1184">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="2759a-1185">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1185">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="2759a-1186">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="2759a-1186">Method visible</span></span>

<span data-ttu-id="2759a-1187">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1187">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="2759a-1188">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="2759a-1188">Parameters - visible</span></span>

<span data-ttu-id="2759a-1189">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1189">value</span></span>  
<span data-ttu-id="2759a-1190">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1190">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="2759a-1191">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="2759a-1191">Return Value - visible</span></span>

<span data-ttu-id="2759a-1192">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="2759a-1192">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="2759a-1193">メソッド width</span><span class="sxs-lookup"><span data-stu-id="2759a-1193">Method width</span></span>

<span data-ttu-id="2759a-1194">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1194">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="2759a-1195">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="2759a-1195">Parameters - width</span></span>

<span data-ttu-id="2759a-1196">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1196">value</span></span>  
<span data-ttu-id="2759a-1197">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1197">An integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="2759a-1198">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-1198">mode</span></span>  
<span data-ttu-id="2759a-1199">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1199">An integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="2759a-1200">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="2759a-1200">Return Value - width</span></span>

<span data-ttu-id="2759a-1201">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="2759a-1201">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="2759a-1202">備考 - width</span><span class="sxs-lookup"><span data-stu-id="2759a-1202">Remarks - width</span></span>

<span data-ttu-id="2759a-1203">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1203">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="2759a-1204">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1204">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="2759a-1205">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-1205">Mode</span></span>           | <span data-ttu-id="2759a-1206">幅計算</span><span class="sxs-lookup"><span data-stu-id="2759a-1206">Width calculation</span></span>                                                                        |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2759a-1207">-1 正確</span><span class="sxs-lookup"><span data-stu-id="2759a-1207">-1 Exact</span></span>       | <span data-ttu-id="2759a-1208">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1208">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2759a-1209">0 自動</span><span class="sxs-lookup"><span data-stu-id="2759a-1209">0 Auto</span></span>         | <span data-ttu-id="2759a-1210">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1210">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2759a-1211">1 列の幅</span><span class="sxs-lookup"><span data-stu-id="2759a-1211">1 Column width</span></span> | <span data-ttu-id="2759a-1212">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="2759a-1212">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="2759a-1213">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1213">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="2759a-1214">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1214">Method widthMode</span></span>

<span data-ttu-id="2759a-1215">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1215">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="2759a-1216">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1216">Parameters - widthMode</span></span>

<span data-ttu-id="2759a-1217">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1217">value</span></span>  
<span data-ttu-id="2759a-1218">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1218">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="2759a-1219">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1219">Return Value - widthMode</span></span>

<span data-ttu-id="2759a-1220">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1220">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="2759a-1221">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1221">Remarks - widthMode</span></span>

<span data-ttu-id="2759a-1222">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1222">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="2759a-1223">モード</span><span class="sxs-lookup"><span data-stu-id="2759a-1223">Mode</span></span>         | <span data-ttu-id="2759a-1224">幅計算</span><span class="sxs-lookup"><span data-stu-id="2759a-1224">Width calculation</span></span>                                                                        |
|--------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2759a-1225">正確</span><span class="sxs-lookup"><span data-stu-id="2759a-1225">Exact</span></span>        | <span data-ttu-id="2759a-1226">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1226">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2759a-1227">自動</span><span class="sxs-lookup"><span data-stu-id="2759a-1227">Auto</span></span>         | <span data-ttu-id="2759a-1228">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1228">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2759a-1229">列の幅</span><span class="sxs-lookup"><span data-stu-id="2759a-1229">Column width</span></span> | <span data-ttu-id="2759a-1230">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="2759a-1230">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="2759a-1231">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="2759a-1231">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="2759a-1232">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1232">Method widthValue</span></span>

<span data-ttu-id="2759a-1233">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1233">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="2759a-1234">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1234">Parameters - widthValue</span></span>

<span data-ttu-id="2759a-1235">値</span><span class="sxs-lookup"><span data-stu-id="2759a-1235">value</span></span>  
<span data-ttu-id="2759a-1236">幅をピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="2759a-1236">An integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="2759a-1237">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1237">Return Value - widthValue</span></span>

<span data-ttu-id="2759a-1238">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="2759a-1238">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="2759a-1239">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="2759a-1239">Remarks - widthValue</span></span>

<span data-ttu-id="2759a-1240">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1240">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-pageactivated"></a><span data-ttu-id="2759a-1241">メソッド pageActivated</span><span class="sxs-lookup"><span data-stu-id="2759a-1241">Method pageActivated</span></span>

```xpp
public void pageActivated()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="2759a-1242">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="2759a-1242">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="2759a-1243">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="2759a-1243">Parameters - OnLostFocus</span></span>

<span data-ttu-id="2759a-1244">sender</span><span class="sxs-lookup"><span data-stu-id="2759a-1244">sender</span></span>  

<!-- -->

<span data-ttu-id="2759a-1245">e</span><span class="sxs-lookup"><span data-stu-id="2759a-1245">e</span></span>  

## <a name="method-collapse"></a><span data-ttu-id="2759a-1246">メソッド collapse</span><span class="sxs-lookup"><span data-stu-id="2759a-1246">Method collapse</span></span>

```xpp
public void collapse()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="2759a-1247">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="2759a-1247">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="2759a-1248">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="2759a-1248">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="2759a-1249">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="2759a-1249">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="2759a-1250">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="2759a-1250">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="2759a-1251">overrideObject</span><span class="sxs-lookup"><span data-stu-id="2759a-1251">overrideObject</span></span>  

## <a name="method-onexpanding"></a><span data-ttu-id="2759a-1252">メソッド OnExpanding</span><span class="sxs-lookup"><span data-stu-id="2759a-1252">Method OnExpanding</span></span>

```xpp
private void OnExpanding([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onexpanding"></a><span data-ttu-id="2759a-1253">パラメーター - OnExpanding</span><span class="sxs-lookup"><span data-stu-id="2759a-1253">Parameters - OnExpanding</span></span>

<span data-ttu-id="2759a-1254">sender</span><span class="sxs-lookup"><span data-stu-id="2759a-1254">sender</span></span>  

<!-- -->

<span data-ttu-id="2759a-1255">e</span><span class="sxs-lookup"><span data-stu-id="2759a-1255">e</span></span>  

## <a name="method-drop"></a><span data-ttu-id="2759a-1256">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="2759a-1256">Method drop</span></span>

<span data-ttu-id="2759a-1257">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1257">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="2759a-1258">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="2759a-1258">Parameters - drop</span></span>

<span data-ttu-id="2759a-1259">dragSource</span><span class="sxs-lookup"><span data-stu-id="2759a-1259">dragSource</span></span>  
<span data-ttu-id="2759a-1260">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1260">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-1261">dragMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1261">dragMode</span></span>  
<span data-ttu-id="2759a-1262">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1262">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-1263">x</span><span class="sxs-lookup"><span data-stu-id="2759a-1263">x</span></span>  
<span data-ttu-id="2759a-1264">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1264">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-1265">y</span><span class="sxs-lookup"><span data-stu-id="2759a-1265">y</span></span>  
<span data-ttu-id="2759a-1266">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1266">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="2759a-1267">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="2759a-1267">Method mouseEnter</span></span>

<span data-ttu-id="2759a-1268">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1268">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="2759a-1269">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="2759a-1269">Parameters - mouseEnter</span></span>

<span data-ttu-id="2759a-1270">x</span><span class="sxs-lookup"><span data-stu-id="2759a-1270">x</span></span>  
<span data-ttu-id="2759a-1271">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1271">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-1272">y</span><span class="sxs-lookup"><span data-stu-id="2759a-1272">y</span></span>  
<span data-ttu-id="2759a-1273">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1273">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-1274">ボタン</span><span class="sxs-lookup"><span data-stu-id="2759a-1274">button</span></span>  
<span data-ttu-id="2759a-1275">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1275">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-1276">Ctrl</span><span class="sxs-lookup"><span data-stu-id="2759a-1276">Ctrl</span></span>  
<span data-ttu-id="2759a-1277">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1277">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="2759a-1278">シフト</span><span class="sxs-lookup"><span data-stu-id="2759a-1278">Shift</span></span>  
<span data-ttu-id="2759a-1279">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1279">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-jumpref"></a><span data-ttu-id="2759a-1280">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="2759a-1280">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-enddrag"></a><span data-ttu-id="2759a-1281">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="2759a-1281">Method endDrag</span></span>

<span data-ttu-id="2759a-1282">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1282">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="2759a-1283">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="2759a-1283">Remarks - endDrag</span></span>

<span data-ttu-id="2759a-1284">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="2759a-1284">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="2759a-1285">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1285">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-filter"></a><span data-ttu-id="2759a-1286">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="2759a-1286">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="2759a-1287">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="2759a-1287">Parameters - filter</span></span>

<span data-ttu-id="2759a-1288">filterStr</span><span class="sxs-lookup"><span data-stu-id="2759a-1288">filterStr</span></span>  

## <a name="method-paste"></a><span data-ttu-id="2759a-1289">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="2759a-1289">Method paste</span></span>

<span data-ttu-id="2759a-1290">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1290">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-setfocus"></a><span data-ttu-id="2759a-1291">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="2759a-1291">Method setFocus</span></span>

<span data-ttu-id="2759a-1292">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1292">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="2759a-1293">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="2759a-1293">Method resetUserSetting</span></span>

<span data-ttu-id="2759a-1294">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="2759a-1294">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-onexpanded"></a><span data-ttu-id="2759a-1295">メソッド OnExpanded</span><span class="sxs-lookup"><span data-stu-id="2759a-1295">Method OnExpanded</span></span>

```xpp
private void OnExpanded([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onexpanded"></a><span data-ttu-id="2759a-1296">パラメーター - OnExpanded</span><span class="sxs-lookup"><span data-stu-id="2759a-1296">Parameters - OnExpanded</span></span>

<span data-ttu-id="2759a-1297">sender</span><span class="sxs-lookup"><span data-stu-id="2759a-1297">sender</span></span>  

<!-- -->

<span data-ttu-id="2759a-1298">e</span><span class="sxs-lookup"><span data-stu-id="2759a-1298">e</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="2759a-1299">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="2759a-1299">Method mouseLeave</span></span>

<span data-ttu-id="2759a-1300">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1300">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-arrange"></a><span data-ttu-id="2759a-1301">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="2759a-1301">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-onpageactivated"></a><span data-ttu-id="2759a-1302">メソッド OnPageActivated</span><span class="sxs-lookup"><span data-stu-id="2759a-1302">Method OnPageActivated</span></span>

```xpp
private void OnPageActivated([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onpageactivated"></a><span data-ttu-id="2759a-1303">パラメーター - OnPageActivated</span><span class="sxs-lookup"><span data-stu-id="2759a-1303">Parameters - OnPageActivated</span></span>

<span data-ttu-id="2759a-1304">sender</span><span class="sxs-lookup"><span data-stu-id="2759a-1304">sender</span></span>  

<!-- -->

<span data-ttu-id="2759a-1305">e</span><span class="sxs-lookup"><span data-stu-id="2759a-1305">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="2759a-1306">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="2759a-1306">Method dropEx</span></span>

<span data-ttu-id="2759a-1307">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1307">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="2759a-1308">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="2759a-1308">Parameters - dropEx</span></span>

<span data-ttu-id="2759a-1309">dragSource</span><span class="sxs-lookup"><span data-stu-id="2759a-1309">dragSource</span></span>  
<span data-ttu-id="2759a-1310">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1310">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-1311">dragMode</span><span class="sxs-lookup"><span data-stu-id="2759a-1311">dragMode</span></span>  
<span data-ttu-id="2759a-1312">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1312">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-1313">x</span><span class="sxs-lookup"><span data-stu-id="2759a-1313">x</span></span>  
<span data-ttu-id="2759a-1314">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1314">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="2759a-1315">y</span><span class="sxs-lookup"><span data-stu-id="2759a-1315">y</span></span>  
<span data-ttu-id="2759a-1316">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2759a-1316">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-expand"></a><span data-ttu-id="2759a-1317">メソッド expand</span><span class="sxs-lookup"><span data-stu-id="2759a-1317">Method expand</span></span>

```xpp
public void expand()
```

## <a name="method-gotfocus"></a><span data-ttu-id="2759a-1318">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="2759a-1318">Method gotFocus</span></span>

<span data-ttu-id="2759a-1319">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1319">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="2759a-1320">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="2759a-1320">Method prefColumnSize</span></span>

<span data-ttu-id="2759a-1321">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1321">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="2759a-1322">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="2759a-1322">Parameters - prefColumnSize</span></span>

<span data-ttu-id="2759a-1323">width</span><span class="sxs-lookup"><span data-stu-id="2759a-1323">width</span></span>  
<span data-ttu-id="2759a-1324">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="2759a-1324">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="2759a-1325">height</span><span class="sxs-lookup"><span data-stu-id="2759a-1325">height</span></span>  
<span data-ttu-id="2759a-1326">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="2759a-1326">The preferred height of the control.</span></span>

## <a name="method-copy"></a><span data-ttu-id="2759a-1327">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="2759a-1327">Method copy</span></span>

<span data-ttu-id="2759a-1328">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="2759a-1328">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-activatepage"></a><span data-ttu-id="2759a-1329">メソッド activatePage</span><span class="sxs-lookup"><span data-stu-id="2759a-1329">Method activatePage</span></span>

```xpp
public void activatePage()
```

## <a name="method-context"></a><span data-ttu-id="2759a-1330">メソッド context</span><span class="sxs-lookup"><span data-stu-id="2759a-1330">Method context</span></span>

<span data-ttu-id="2759a-1331">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1331">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-cut"></a><span data-ttu-id="2759a-1332">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="2759a-1332">Method cut</span></span>

<span data-ttu-id="2759a-1333">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="2759a-1333">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-lostfocus"></a><span data-ttu-id="2759a-1334">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="2759a-1334">Method lostFocus</span></span>

<span data-ttu-id="2759a-1335">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1335">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-displaycontrol"></a><span data-ttu-id="2759a-1336">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="2759a-1336">Method displayControl</span></span>

<span data-ttu-id="2759a-1337">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1337">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-onallowpagedeactivate"></a><span data-ttu-id="2759a-1338">メソッド OnAllowPageDeactivate</span><span class="sxs-lookup"><span data-stu-id="2759a-1338">Method OnAllowPageDeactivate</span></span>

```xpp
private void OnAllowPageDeactivate([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onallowpagedeactivate"></a><span data-ttu-id="2759a-1339">パラメーター - OnAllowPageDeactivate</span><span class="sxs-lookup"><span data-stu-id="2759a-1339">Parameters - OnAllowPageDeactivate</span></span>

<span data-ttu-id="2759a-1340">sender</span><span class="sxs-lookup"><span data-stu-id="2759a-1340">sender</span></span>  

<!-- -->

<span data-ttu-id="2759a-1341">e</span><span class="sxs-lookup"><span data-stu-id="2759a-1341">e</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="2759a-1342">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="2759a-1342">Method inputSearch</span></span>

<span data-ttu-id="2759a-1343">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="2759a-1343">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="2759a-1344">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="2759a-1344">Parameters - inputSearch</span></span>

<span data-ttu-id="2759a-1345">searchStr</span><span class="sxs-lookup"><span data-stu-id="2759a-1345">searchStr</span></span>  
<span data-ttu-id="2759a-1346">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="2759a-1346">The string value to use to filter data; optional.</span></span>

## <a name="method-dragleave"></a><span data-ttu-id="2759a-1347">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="2759a-1347">Method dragLeave</span></span>

<span data-ttu-id="2759a-1348">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="2759a-1348">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="2759a-1349">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="2759a-1349">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="2759a-1350">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="2759a-1350">Parameters - OnGotFocus</span></span>

<span data-ttu-id="2759a-1351">sender</span><span class="sxs-lookup"><span data-stu-id="2759a-1351">sender</span></span>  

<!-- -->

<span data-ttu-id="2759a-1352">e</span><span class="sxs-lookup"><span data-stu-id="2759a-1352">e</span></span>  

