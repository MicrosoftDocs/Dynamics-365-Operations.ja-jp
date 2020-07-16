---
title: FormFilterPaneControl クラス
description: このトピックでは、FormFilterPaneControl クラスについて説明します。
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
ms.openlocfilehash: 09191578c74f0222c015b32e1835d8bf9c07e71c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502940"
---
# <a name="class-formfilterpanecontrol"></a><span data-ttu-id="7393c-103">クラス FormFilterPaneControl</span><span class="sxs-lookup"><span data-stu-id="7393c-103">Class FormFilterPaneControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormFilterPaneControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="7393c-104">備考</span><span class="sxs-lookup"><span data-stu-id="7393c-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="7393c-105">例</span><span class="sxs-lookup"><span data-stu-id="7393c-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="7393c-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="7393c-106">Methods</span></span>

| <span data-ttu-id="7393c-107">方法</span><span class="sxs-lookup"><span data-stu-id="7393c-107">Method</span></span>                                                                                                      | <span data-ttu-id="7393c-108">説明</span><span class="sxs-lookup"><span data-stu-id="7393c-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7393c-109">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-109">public boolean alignChild(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7393c-110">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-110">public boolean alignChildren(\[boolean value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="7393c-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="7393c-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-112">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7393c-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="7393c-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-114">Determines whether the user can change the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="7393c-115">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="7393c-115">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="7393c-116">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-116">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="7393c-117">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-117">public int allowUserSetup(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7393c-118">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-118">public int arrangeGuide(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7393c-119">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-119">public int arrangeMethod(\[int value\])</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="7393c-120">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-120">public int arrangeWhen(\[int value\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7393c-121">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-121">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="7393c-122">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-122">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="7393c-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7393c-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="7393c-124">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-124">Is called when the user starts to drag a form control.</span></span>                                                                                                                  |
| <span data-ttu-id="7393c-125">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-125">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="7393c-126">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-126">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="7393c-127">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-127">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7393c-128">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="7393c-128">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="7393c-129">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-129">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="7393c-130">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-130">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="7393c-131">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-131">Gets or set the caption of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="7393c-132">public int columns(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-132">public int columns(\[int value\], \[AutoMode mode\])</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="7393c-133">public AutoMode columnsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-133">public AutoMode columnsMode(\[AutoMode mode\])</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="7393c-134">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-134">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7393c-135">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-135">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="7393c-136">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-136">public int columnspaceValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="7393c-137">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-137">public int columnsValue(\[int value\])</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7393c-138">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-138">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="7393c-139">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-139">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="7393c-140">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="7393c-140">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="7393c-141">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-141">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                        |
| <span data-ttu-id="7393c-142">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-142">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="7393c-143">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-143">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="7393c-144">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-144">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                                                         |
| <span data-ttu-id="7393c-145">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-145">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="7393c-146">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-146">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="7393c-147">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-147">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="7393c-148">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-148">Gets or sets a data source to be used by the control or the form.</span></span>                                                                                                       |
| <span data-ttu-id="7393c-149">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-149">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="7393c-150">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-150">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="7393c-151">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-151">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="7393c-152">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-152">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="7393c-153">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7393c-153">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="7393c-154">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7393c-154">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="7393c-155">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7393c-155">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="7393c-156">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7393c-156">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="7393c-157">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="7393c-157">public str dragText()</span></span>                                                                                       | <span data-ttu-id="7393c-158">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-158">Retrieves the text that is displayed when the form control is dragged.</span></span>                                                                                                  |
| <span data-ttu-id="7393c-159">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-159">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="7393c-160">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-160">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="7393c-161">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="7393c-161">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="7393c-162">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-162">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="7393c-163">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="7393c-163">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="7393c-164">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-164">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="7393c-165">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-165">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="7393c-166">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-166">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="7393c-167">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-167">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="7393c-168">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-168">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="7393c-169">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-169">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="7393c-170">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-170">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="7393c-171">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="7393c-171">public str helpField()</span></span>                                                                                      | <span data-ttu-id="7393c-172">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-172">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7393c-173">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-173">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="7393c-174">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-174">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="7393c-175">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-175">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="7393c-176">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-176">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="7393c-177">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-177">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="7393c-178">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="7393c-178">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="7393c-179">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-179">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="7393c-180">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="7393c-180">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7393c-181">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="7393c-181">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="7393c-182">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-182">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="7393c-183">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="7393c-183">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="7393c-184">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-184">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="7393c-185">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="7393c-185">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="7393c-186">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-186">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="7393c-187">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="7393c-187">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7393c-188">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-188">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="7393c-189">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-189">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="7393c-190">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-190">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="7393c-191">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-191">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="7393c-192">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-192">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="7393c-193">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-193">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="7393c-194">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-194">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="7393c-195">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-195">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="7393c-196">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-196">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="7393c-197">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-197">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="7393c-198">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="7393c-198">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="7393c-199">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7393c-199">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="7393c-200">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-200">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="7393c-201">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7393c-201">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="7393c-202">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-202">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="7393c-203">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7393c-203">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="7393c-204">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-204">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="7393c-205">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7393c-205">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="7393c-206">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-206">Is called when the user releases the mouse button over the control area.</span></span>                                                                                                |
| <span data-ttu-id="7393c-207">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-207">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="7393c-208">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-208">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>                                 |
| <span data-ttu-id="7393c-209">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-209">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="7393c-210">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="7393c-210">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="7393c-211">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="7393c-211">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="7393c-212">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-212">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="7393c-213">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-213">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7393c-214">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-214">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="7393c-215">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-215">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="7393c-216">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-216">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="7393c-217">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-217">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="7393c-218">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="7393c-218">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="7393c-219">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-219">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7393c-220">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-220">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="7393c-221">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-221">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="7393c-222">public int sort(\[SortOrder sortDirection\])</span><span class="sxs-lookup"><span data-stu-id="7393c-222">public int sort(\[SortOrder sortDirection\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="7393c-223">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="7393c-223">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="7393c-224">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-224">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="7393c-225">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-225">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="7393c-226">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-226">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="7393c-227">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-227">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="7393c-228">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-228">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="7393c-229">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-229">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="7393c-230">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-230">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="7393c-231">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-231">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="7393c-232">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-232">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="7393c-233">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-233">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="7393c-234">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-234">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="7393c-235">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="7393c-235">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="7393c-236">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-236">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="7393c-237">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-237">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="7393c-238">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-238">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="7393c-239">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-239">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="7393c-240">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-240">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="7393c-241">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-241">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="7393c-242">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-242">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="7393c-243">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-243">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="7393c-244">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-244">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="7393c-245">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-245">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="7393c-246">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-246">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="7393c-247">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-247">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="7393c-248">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-248">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="7393c-249">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-249">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="7393c-250">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-250">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="7393c-251">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-251">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="7393c-252">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-252">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="7393c-253">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-253">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="7393c-254">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-254">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="7393c-255">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-255">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="7393c-256">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-256">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="7393c-257">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-257">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="7393c-258">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-258">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="7393c-259">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-259">Sets or returns the width of the control in pixels.</span></span>                                                                                                                     |
| <span data-ttu-id="7393c-260">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-260">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="7393c-261">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-261">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="7393c-262">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-262">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="7393c-263">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-263">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="7393c-264">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-264">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="7393c-265">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-265">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="7393c-266">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-266">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="7393c-267">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-267">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="7393c-268">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="7393c-268">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="7393c-269">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-269">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="7393c-270">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-270">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="7393c-271">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-271">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="7393c-272">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7393c-272">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="7393c-273">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-273">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="7393c-274">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7393c-274">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="7393c-275">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="7393c-275">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="7393c-276">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-276">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="7393c-277">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7393c-277">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="7393c-278">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7393c-278">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="7393c-279">public void paste()</span><span class="sxs-lookup"><span data-stu-id="7393c-279">public void paste()</span></span>                                                                                         | <span data-ttu-id="7393c-280">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7393c-280">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="7393c-281">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="7393c-281">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="7393c-282">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-282">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="7393c-283">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7393c-283">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="7393c-284">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="7393c-284">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="7393c-285">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-285">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="7393c-286">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="7393c-286">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="7393c-287">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-287">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="7393c-288">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="7393c-288">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="7393c-289">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7393c-289">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="7393c-290">public void enter()</span><span class="sxs-lookup"><span data-stu-id="7393c-290">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="7393c-291">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="7393c-291">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="7393c-292">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7393c-292">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="7393c-293">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="7393c-293">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="7393c-294">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-294">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="7393c-295">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="7393c-295">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7393c-296">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7393c-296">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="7393c-297">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="7393c-297">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="7393c-298">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="7393c-298">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="7393c-299">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-299">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="7393c-300">public void cut()</span><span class="sxs-lookup"><span data-stu-id="7393c-300">public void cut()</span></span>                                                                                           | <span data-ttu-id="7393c-301">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="7393c-301">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="7393c-302">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="7393c-302">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="7393c-303">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="7393c-303">public void displayControl()</span></span>                                                                                | <span data-ttu-id="7393c-304">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-304">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="7393c-305">public void copy()</span><span class="sxs-lookup"><span data-stu-id="7393c-305">public void copy()</span></span>                                                                                          | <span data-ttu-id="7393c-306">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7393c-306">Copies the contents of the control to the clipboard.</span></span>                                                                                                                    |
| <span data-ttu-id="7393c-307">public void context()</span><span class="sxs-lookup"><span data-stu-id="7393c-307">public void context()</span></span>                                                                                       | <span data-ttu-id="7393c-308">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-308">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="7393c-309">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="7393c-309">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="7393c-310">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="7393c-310">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="7393c-311">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="7393c-311">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="7393c-312">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="7393c-312">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="7393c-313">public void filter(\[str filterStr\])</span><span class="sxs-lookup"><span data-stu-id="7393c-313">public void filter(\[str filterStr\])</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="7393c-314">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="7393c-314">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="7393c-315">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-315">Is called when the user has finished dragging a form control.</span></span>                                                                                                           |

## <a name="method-alignchild"></a><span data-ttu-id="7393c-316">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="7393c-316">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="7393c-317">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="7393c-317">Parameters - alignChild</span></span>

<span data-ttu-id="7393c-318">値</span><span class="sxs-lookup"><span data-stu-id="7393c-318">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="7393c-319">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="7393c-319">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="7393c-320">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="7393c-320">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="7393c-321">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="7393c-321">Parameters - alignChildren</span></span>

<span data-ttu-id="7393c-322">値</span><span class="sxs-lookup"><span data-stu-id="7393c-322">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="7393c-323">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="7393c-323">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="7393c-324">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="7393c-324">Method alignControl</span></span>

<span data-ttu-id="7393c-325">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-325">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="7393c-326">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="7393c-326">Parameters - alignControl</span></span>

<span data-ttu-id="7393c-327">値</span><span class="sxs-lookup"><span data-stu-id="7393c-327">value</span></span>  
<span data-ttu-id="7393c-328">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-328">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="7393c-329">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="7393c-329">Return Value - alignControl</span></span>

<span data-ttu-id="7393c-330">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7393c-330">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="7393c-331">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="7393c-331">Remarks - alignControl</span></span>

<span data-ttu-id="7393c-332">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-332">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="7393c-333">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="7393c-333">Method allowEdit</span></span>

<span data-ttu-id="7393c-334">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-334">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="7393c-335">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="7393c-335">Parameters - allowEdit</span></span>

<span data-ttu-id="7393c-336">値</span><span class="sxs-lookup"><span data-stu-id="7393c-336">value</span></span>  
<span data-ttu-id="7393c-337">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="7393c-337">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="7393c-338">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="7393c-338">Return Value - allowEdit</span></span>

<span data-ttu-id="7393c-339">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7393c-339">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="7393c-340">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="7393c-340">Remarks - allowEdit</span></span>

<span data-ttu-id="7393c-341">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="7393c-341">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="7393c-342">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="7393c-342">Method allowSysSetup</span></span>

<span data-ttu-id="7393c-343">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-343">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="7393c-344">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="7393c-344">Return Value - allowSysSetup</span></span>

<span data-ttu-id="7393c-345">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7393c-345">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="7393c-346">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="7393c-346">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="7393c-347">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="7393c-347">Parameters - allowUserSetup</span></span>

<span data-ttu-id="7393c-348">値</span><span class="sxs-lookup"><span data-stu-id="7393c-348">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="7393c-349">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="7393c-349">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="7393c-350">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="7393c-350">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="7393c-351">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="7393c-351">Parameters - arrangeGuide</span></span>

<span data-ttu-id="7393c-352">値</span><span class="sxs-lookup"><span data-stu-id="7393c-352">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="7393c-353">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="7393c-353">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="7393c-354">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="7393c-354">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="7393c-355">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="7393c-355">Parameters - arrangeMethod</span></span>

<span data-ttu-id="7393c-356">値</span><span class="sxs-lookup"><span data-stu-id="7393c-356">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="7393c-357">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="7393c-357">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="7393c-358">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="7393c-358">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="7393c-359">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="7393c-359">Parameters - arrangeWhen</span></span>

<span data-ttu-id="7393c-360">値</span><span class="sxs-lookup"><span data-stu-id="7393c-360">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="7393c-361">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="7393c-361">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="7393c-362">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7393c-362">Method autoDeclaration</span></span>

<span data-ttu-id="7393c-363">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-363">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="7393c-364">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7393c-364">Parameters - autoDeclaration</span></span>

<span data-ttu-id="7393c-365">値</span><span class="sxs-lookup"><span data-stu-id="7393c-365">value</span></span>  
<span data-ttu-id="7393c-366">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-366">The new value for the property; optional.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="7393c-367">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7393c-367">Return Value - autoDeclaration</span></span>

<span data-ttu-id="7393c-368">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7393c-368">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="7393c-369">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7393c-369">Remarks - autoDeclaration</span></span>

<span data-ttu-id="7393c-370">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="7393c-370">Controls cannot have identical names.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="7393c-371">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="7393c-371">Method beginDrag</span></span>

<span data-ttu-id="7393c-372">ユーザーがフォーム コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-372">Is called when the user starts to drag a form control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="7393c-373">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="7393c-373">Parameters - beginDrag</span></span>

<span data-ttu-id="7393c-374">x</span><span class="sxs-lookup"><span data-stu-id="7393c-374">x</span></span>  
<span data-ttu-id="7393c-375">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-375">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="7393c-376">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="7393c-376">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="7393c-377">y</span><span class="sxs-lookup"><span data-stu-id="7393c-377">y</span></span>  
<span data-ttu-id="7393c-378">マウス ポインターの y 座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-378">An integer value that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="7393c-379">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="7393c-379">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="7393c-380">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="7393c-380">Return Value - beginDrag</span></span>

<span data-ttu-id="7393c-381">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7393c-381">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="7393c-382">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="7393c-382">Remarks - beginDrag</span></span>

<span data-ttu-id="7393c-383">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="7393c-383">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="7393c-384">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="7393c-384">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="7393c-385">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-385">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="7393c-386">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-386">Parameters - bottomMargin</span></span>

<span data-ttu-id="7393c-387">値</span><span class="sxs-lookup"><span data-stu-id="7393c-387">value</span></span>  

<!-- -->

<span data-ttu-id="7393c-388">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-388">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="7393c-389">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-389">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="7393c-390">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-390">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="7393c-391">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-391">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="7393c-392">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-392">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="7393c-393">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-393">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="7393c-394">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-394">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="7393c-395">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-395">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="7393c-396">値</span><span class="sxs-lookup"><span data-stu-id="7393c-396">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="7393c-397">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-397">Return Value - bottomMarginValue</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="7393c-398">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="7393c-398">Method calcControlSize</span></span>

<span data-ttu-id="7393c-399">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-399">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="7393c-400">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="7393c-400">Parameters - calcControlSize</span></span>

<span data-ttu-id="7393c-401">chars</span><span class="sxs-lookup"><span data-stu-id="7393c-401">chars</span></span>  
<span data-ttu-id="7393c-402">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="7393c-402">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="7393c-403">明細行</span><span class="sxs-lookup"><span data-stu-id="7393c-403">lines</span></span>  
<span data-ttu-id="7393c-404">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="7393c-404">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="7393c-405">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="7393c-405">Return Value - calcControlSize</span></span>

<span data-ttu-id="7393c-406">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="7393c-406">The container that holds the width and height.</span></span>

## <a name="method-caption"></a><span data-ttu-id="7393c-407">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="7393c-407">Method caption</span></span>

<span data-ttu-id="7393c-408">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-408">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="7393c-409">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="7393c-409">Parameters - caption</span></span>

<span data-ttu-id="7393c-410">値</span><span class="sxs-lookup"><span data-stu-id="7393c-410">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="7393c-411">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="7393c-411">Return Value - caption</span></span>

<span data-ttu-id="7393c-412">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="7393c-412">The string that is used as the caption of the control.</span></span>

## <a name="method-columns"></a><span data-ttu-id="7393c-413">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="7393c-413">Method columns</span></span>

```xpp
public int columns([int value], [AutoMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="7393c-414">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="7393c-414">Parameters - columns</span></span>

<span data-ttu-id="7393c-415">値</span><span class="sxs-lookup"><span data-stu-id="7393c-415">value</span></span>  

<!-- -->

<span data-ttu-id="7393c-416">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-416">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="7393c-417">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="7393c-417">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="7393c-418">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="7393c-418">Method columnsMode</span></span>

```xpp
public AutoMode columnsMode([AutoMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="7393c-419">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="7393c-419">Parameters - columnsMode</span></span>

<span data-ttu-id="7393c-420">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-420">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="7393c-421">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="7393c-421">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="7393c-422">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="7393c-422">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="7393c-423">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="7393c-423">Parameters - columnspace</span></span>

<span data-ttu-id="7393c-424">値</span><span class="sxs-lookup"><span data-stu-id="7393c-424">value</span></span>  

<!-- -->

<span data-ttu-id="7393c-425">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-425">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="7393c-426">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="7393c-426">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="7393c-427">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="7393c-427">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="7393c-428">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="7393c-428">Parameters - columnspaceMode</span></span>

<span data-ttu-id="7393c-429">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-429">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="7393c-430">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="7393c-430">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="7393c-431">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="7393c-431">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="7393c-432">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="7393c-432">Parameters - columnspaceValue</span></span>

<span data-ttu-id="7393c-433">値</span><span class="sxs-lookup"><span data-stu-id="7393c-433">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="7393c-434">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="7393c-434">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="7393c-435">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="7393c-435">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="7393c-436">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="7393c-436">Parameters - columnsValue</span></span>

<span data-ttu-id="7393c-437">値</span><span class="sxs-lookup"><span data-stu-id="7393c-437">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="7393c-438">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="7393c-438">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="7393c-439">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="7393c-439">Method configurationKey</span></span>

<span data-ttu-id="7393c-440">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-440">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="7393c-441">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7393c-441">Parameters - configurationKey</span></span>

<span data-ttu-id="7393c-442">値</span><span class="sxs-lookup"><span data-stu-id="7393c-442">value</span></span>  
<span data-ttu-id="7393c-443">コントロールに割り当てられているコンフィギュレーション キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-443">The ID of the configuration key being assigned to the control; optional.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="7393c-444">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7393c-444">Return Value - configurationKey</span></span>

<span data-ttu-id="7393c-445">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="7393c-445">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="7393c-446">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7393c-446">Remarks - configurationKey</span></span>

<span data-ttu-id="7393c-447">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-447">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="7393c-448">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="7393c-448">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="7393c-449">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="7393c-449">Method configurationKeyEx</span></span>

<span data-ttu-id="7393c-450">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-450">Retrieves a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="7393c-451">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="7393c-451">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="7393c-452">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="7393c-452">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="7393c-453">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="7393c-453">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="7393c-454">返されるリストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="7393c-454">The returned list does not contain duplicate IDs.</span></span> <span data-ttu-id="7393c-455">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="7393c-455">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="7393c-456">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7393c-456">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="7393c-457">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="7393c-457">Method countryRegionCodes</span></span>

<span data-ttu-id="7393c-458">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-458">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="7393c-459">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="7393c-459">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="7393c-460">値</span><span class="sxs-lookup"><span data-stu-id="7393c-460">value</span></span>  
<span data-ttu-id="7393c-461">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-461">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="7393c-462">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="7393c-462">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="7393c-463">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="7393c-463">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="7393c-464">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="7393c-464">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="7393c-465">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="7393c-465">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="7393c-466">値</span><span class="sxs-lookup"><span data-stu-id="7393c-466">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="7393c-467">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="7393c-467">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="7393c-468">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7393c-468">Method dataRelationPath</span></span>

<span data-ttu-id="7393c-469">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-469">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="7393c-470">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7393c-470">Parameters - dataRelationPath</span></span>

<span data-ttu-id="7393c-471">値</span><span class="sxs-lookup"><span data-stu-id="7393c-471">value</span></span>  
<span data-ttu-id="7393c-472">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-472">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="7393c-473">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7393c-473">Return Value - dataRelationPath</span></span>

<span data-ttu-id="7393c-474">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="7393c-474">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="7393c-475">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="7393c-475">Remarks - dataRelationPath</span></span>

<span data-ttu-id="7393c-476">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="7393c-476">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="7393c-477">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="7393c-477">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="7393c-478">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="7393c-478">Method dataSource</span></span>

<span data-ttu-id="7393c-479">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-479">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="7393c-480">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="7393c-480">Parameters - dataSource</span></span>

<span data-ttu-id="7393c-481">値</span><span class="sxs-lookup"><span data-stu-id="7393c-481">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="7393c-482">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="7393c-482">Return Value - dataSource</span></span>

<span data-ttu-id="7393c-483">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="7393c-483">The identifier of the data source to be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="7393c-484">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="7393c-484">Method displayTarget</span></span>

<span data-ttu-id="7393c-485">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-485">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="7393c-486">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="7393c-486">Parameters - displayTarget</span></span>

<span data-ttu-id="7393c-487">値</span><span class="sxs-lookup"><span data-stu-id="7393c-487">value</span></span>  
<span data-ttu-id="7393c-488">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-488">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="7393c-489">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="7393c-489">Return Value - displayTarget</span></span>

<span data-ttu-id="7393c-490">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="7393c-490">The value that indicates whether the control is displayed in the  client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="7393c-491">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="7393c-491">Method dragDrop</span></span>

<span data-ttu-id="7393c-492">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-492">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="7393c-493">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="7393c-493">Parameters - dragDrop</span></span>

<span data-ttu-id="7393c-494">値</span><span class="sxs-lookup"><span data-stu-id="7393c-494">value</span></span>  
<span data-ttu-id="7393c-495">ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-495">An Integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="7393c-496">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="7393c-496">Return Value - dragDrop</span></span>

<span data-ttu-id="7393c-497">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="7393c-497">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="7393c-498">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="7393c-498">Remarks - dragDrop</span></span>

<span data-ttu-id="7393c-499">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-499">Use the dragLeave , the dragOver, and the dragOverEx to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="7393c-500">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="7393c-500">Method dragOver</span></span>

<span data-ttu-id="7393c-501">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7393c-501">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="7393c-502">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="7393c-502">Parameters - dragOver</span></span>

<span data-ttu-id="7393c-503">dragSource</span><span class="sxs-lookup"><span data-stu-id="7393c-503">dragSource</span></span>  
<span data-ttu-id="7393c-504">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-504">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-505">dragMode</span><span class="sxs-lookup"><span data-stu-id="7393c-505">dragMode</span></span>  
<span data-ttu-id="7393c-506">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-506">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-507">x</span><span class="sxs-lookup"><span data-stu-id="7393c-507">x</span></span>  
<span data-ttu-id="7393c-508">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-508">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-509">y</span><span class="sxs-lookup"><span data-stu-id="7393c-509">y</span></span>  
<span data-ttu-id="7393c-510">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-510">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="7393c-511">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="7393c-511">Return Value - dragOver</span></span>

<span data-ttu-id="7393c-512">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="7393c-512">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="7393c-513">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="7393c-513">Method dragOverEx</span></span>

<span data-ttu-id="7393c-514">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7393c-514">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="7393c-515">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="7393c-515">Parameters - dragOverEx</span></span>

<span data-ttu-id="7393c-516">dragSource</span><span class="sxs-lookup"><span data-stu-id="7393c-516">dragSource</span></span>  
<span data-ttu-id="7393c-517">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-517">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-518">dragMode</span><span class="sxs-lookup"><span data-stu-id="7393c-518">dragMode</span></span>  
<span data-ttu-id="7393c-519">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-519">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-520">x</span><span class="sxs-lookup"><span data-stu-id="7393c-520">x</span></span>  
<span data-ttu-id="7393c-521">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-521">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-522">y</span><span class="sxs-lookup"><span data-stu-id="7393c-522">y</span></span>  
<span data-ttu-id="7393c-523">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-523">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="7393c-524">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="7393c-524">Return Value - dragOverEx</span></span>

<span data-ttu-id="7393c-525">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="7393c-525">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="7393c-526">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="7393c-526">Method dragText</span></span>

<span data-ttu-id="7393c-527">フォーム コントロールをドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-527">Retrieves the text that is displayed when the form control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="7393c-528">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="7393c-528">Return Value - dragText</span></span>

<span data-ttu-id="7393c-529">コントロールをドラッグしたときに表示されるテキスト。コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="7393c-529">The text that is displayed when the control is dragged; an empty string if there is no text to display when the control is dragged.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="7393c-530">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="7393c-530">Method enabled</span></span>

<span data-ttu-id="7393c-531">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-531">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="7393c-532">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="7393c-532">Parameters - enabled</span></span>

<span data-ttu-id="7393c-533">値</span><span class="sxs-lookup"><span data-stu-id="7393c-533">value</span></span>  
<span data-ttu-id="7393c-534">コントロールが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-534">A Boolean value that indicates whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="7393c-535">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="7393c-535">Return Value - enabled</span></span>

<span data-ttu-id="7393c-536">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7393c-536">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="7393c-537">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="7393c-537">Remarks - enabled</span></span>

<span data-ttu-id="7393c-538">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="7393c-538">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="7393c-539">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7393c-539">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="7393c-540">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="7393c-540">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="7393c-541">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="7393c-541">Method hasChanged</span></span>

<span data-ttu-id="7393c-542">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-542">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="7393c-543">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="7393c-543">Parameters - hasChanged</span></span>

<span data-ttu-id="7393c-544">val</span><span class="sxs-lookup"><span data-stu-id="7393c-544">val</span></span>  
<span data-ttu-id="7393c-545">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-545">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="7393c-546">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="7393c-546">Return Value - hasChanged</span></span>

<span data-ttu-id="7393c-547">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7393c-547">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="7393c-548">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="7393c-548">Method hasUserSetting</span></span>

<span data-ttu-id="7393c-549">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-549">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="7393c-550">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="7393c-550">Return Value - hasUserSetting</span></span>

<span data-ttu-id="7393c-551">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7393c-551">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="7393c-552">メソッド height</span><span class="sxs-lookup"><span data-stu-id="7393c-552">Method height</span></span>

<span data-ttu-id="7393c-553">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-553">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="7393c-554">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="7393c-554">Parameters - height</span></span>

<span data-ttu-id="7393c-555">値</span><span class="sxs-lookup"><span data-stu-id="7393c-555">value</span></span>  
<span data-ttu-id="7393c-556">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-556">An Integer that indicates how the height is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="7393c-557">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-557">mode</span></span>  
<span data-ttu-id="7393c-558">高さの計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-558">An Integer that indicates how the height is calculated; optional.</span></span>

### <a name="return-value---height"></a><span data-ttu-id="7393c-559">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="7393c-559">Return Value - height</span></span>

<span data-ttu-id="7393c-560">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="7393c-560">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="7393c-561">備考 - height</span><span class="sxs-lookup"><span data-stu-id="7393c-561">Remarks - height</span></span>

<span data-ttu-id="7393c-562">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-562">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="7393c-563">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="7393c-563">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="7393c-564">モード。</span><span class="sxs-lookup"><span data-stu-id="7393c-564">Mode.</span></span>            | <span data-ttu-id="7393c-565">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="7393c-565">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7393c-566">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="7393c-566">-1 Exact.</span></span>        | <span data-ttu-id="7393c-567">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-567">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7393c-568">0 自動。</span><span class="sxs-lookup"><span data-stu-id="7393c-568">0 Auto.</span></span>          | <span data-ttu-id="7393c-569">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-569">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7393c-570">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="7393c-570">1 Column height.</span></span> | <span data-ttu-id="7393c-571">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="7393c-571">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="7393c-572">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7393c-572">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="7393c-573">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="7393c-573">Method heightMode</span></span>

<span data-ttu-id="7393c-574">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-574">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="7393c-575">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="7393c-575">Parameters - heightMode</span></span>

<span data-ttu-id="7393c-576">値</span><span class="sxs-lookup"><span data-stu-id="7393c-576">value</span></span>  
<span data-ttu-id="7393c-577">コントロールの高さの計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-577">An integer value that indicates how control height is calculated; optional.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="7393c-578">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="7393c-578">Return Value - heightMode</span></span>

<span data-ttu-id="7393c-579">計算モード。</span><span class="sxs-lookup"><span data-stu-id="7393c-579">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="7393c-580">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="7393c-580">Remarks - heightMode</span></span>

<span data-ttu-id="7393c-581">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="7393c-581">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="7393c-582">モード。</span><span class="sxs-lookup"><span data-stu-id="7393c-582">Mode.</span></span>          | <span data-ttu-id="7393c-583">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="7393c-583">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7393c-584">正確。</span><span class="sxs-lookup"><span data-stu-id="7393c-584">Exact.</span></span>         | <span data-ttu-id="7393c-585">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-585">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7393c-586">自動。</span><span class="sxs-lookup"><span data-stu-id="7393c-586">Auto.</span></span>          | <span data-ttu-id="7393c-587">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-587">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7393c-588">列の高さ</span><span class="sxs-lookup"><span data-stu-id="7393c-588">Column height.</span></span> | <span data-ttu-id="7393c-589">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="7393c-589">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="7393c-590">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="7393c-590">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="7393c-591">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="7393c-591">Method heightValue</span></span>

<span data-ttu-id="7393c-592">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-592">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="7393c-593">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="7393c-593">Parameters - heightValue</span></span>

<span data-ttu-id="7393c-594">値</span><span class="sxs-lookup"><span data-stu-id="7393c-594">value</span></span>  
<span data-ttu-id="7393c-595">高さをピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-595">An Integer that specifies the height in pixels; optional.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="7393c-596">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="7393c-596">Return Value - heightValue</span></span>

<span data-ttu-id="7393c-597">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="7393c-597">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="7393c-598">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="7393c-598">Remarks - heightValue</span></span>

<span data-ttu-id="7393c-599">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="7393c-599">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="7393c-600">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="7393c-600">Method helpField</span></span>

<span data-ttu-id="7393c-601">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-601">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="7393c-602">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="7393c-602">Return Value - helpField</span></span>

<span data-ttu-id="7393c-603">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="7393c-603">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="7393c-604">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="7393c-604">Remarks - helpField</span></span>

<span data-ttu-id="7393c-605">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="7393c-605">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="7393c-606">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="7393c-606">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="7393c-607">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7393c-607">Method helpText</span></span>

<span data-ttu-id="7393c-608">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-608">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="7393c-609">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="7393c-609">Parameters - helpText</span></span>

<span data-ttu-id="7393c-610">値</span><span class="sxs-lookup"><span data-stu-id="7393c-610">value</span></span>  
<span data-ttu-id="7393c-611">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="7393c-611">The value that is assigned as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="7393c-612">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="7393c-612">Return Value - helpText</span></span>

<span data-ttu-id="7393c-613">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7393c-613">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="7393c-614">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="7393c-614">Remarks - helpText</span></span>

<span data-ttu-id="7393c-615">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-615">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="7393c-616">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="7393c-616">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="7393c-617">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="7393c-617">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="7393c-618">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="7393c-618">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="7393c-619">値</span><span class="sxs-lookup"><span data-stu-id="7393c-619">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="7393c-620">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="7393c-620">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="7393c-621">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="7393c-621">Method hierarchyParent</span></span>

<span data-ttu-id="7393c-622">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-622">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="7393c-623">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="7393c-623">Parameters - hierarchyParent</span></span>

<span data-ttu-id="7393c-624">値</span><span class="sxs-lookup"><span data-stu-id="7393c-624">value</span></span>  
<span data-ttu-id="7393c-625">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="7393c-625">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="7393c-626">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="7393c-626">Return Value - hierarchyParent</span></span>

<span data-ttu-id="7393c-627">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="7393c-627">The HierarchyParent property value of the control.</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="7393c-628">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="7393c-628">Method hWnd</span></span>

<span data-ttu-id="7393c-629">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-629">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="7393c-630">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="7393c-630">Return Value - hWnd</span></span>

<span data-ttu-id="7393c-631">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="7393c-631">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="7393c-632">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="7393c-632">Remarks - hWnd</span></span>

<span data-ttu-id="7393c-633">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="7393c-633">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="7393c-634">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="7393c-634">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="7393c-635">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="7393c-635">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="7393c-636">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="7393c-636">Method isDisplayed</span></span>

<span data-ttu-id="7393c-637">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-637">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="7393c-638">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="7393c-638">Return Value - isDisplayed</span></span>

<span data-ttu-id="7393c-639">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7393c-639">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="7393c-640">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="7393c-640">Remarks - isDisplayed</span></span>

<span data-ttu-id="7393c-641">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7393c-641">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="7393c-642">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="7393c-642">Method isRestricted</span></span>

<span data-ttu-id="7393c-643">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-643">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="7393c-644">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="7393c-644">Return Value - isRestricted</span></span>

<span data-ttu-id="7393c-645">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7393c-645">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="7393c-646">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7393c-646">Method isUserSetupEnabled</span></span>

<span data-ttu-id="7393c-647">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-647">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="7393c-648">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7393c-648">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="7393c-649">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="7393c-649">neededSetupRights</span></span>  
<span data-ttu-id="7393c-650">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="7393c-650">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="7393c-651">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7393c-651">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="7393c-652">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7393c-652">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="7393c-653">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="7393c-653">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="7393c-654">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="7393c-654">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7393c-655">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="7393c-655">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="7393c-656">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="7393c-656">No changes can be made to the control.</span></span> <span data-ttu-id="7393c-657">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-657">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="7393c-658">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="7393c-658">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="7393c-659">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="7393c-659">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="7393c-660">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="7393c-660">The user cannot move the control.</span></span>   |
| <span data-ttu-id="7393c-661">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="7393c-661">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="7393c-662">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="7393c-662">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="7393c-663">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="7393c-663">The user can also move the control.</span></span> |

<span data-ttu-id="7393c-664">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="7393c-664">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

## <a name="method-leave"></a><span data-ttu-id="7393c-665">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="7393c-665">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="7393c-666">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="7393c-666">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="7393c-667">メソッド left</span><span class="sxs-lookup"><span data-stu-id="7393c-667">Method left</span></span>

<span data-ttu-id="7393c-668">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-668">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="7393c-669">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="7393c-669">Parameters - left</span></span>

<span data-ttu-id="7393c-670">値</span><span class="sxs-lookup"><span data-stu-id="7393c-670">value</span></span>  
<span data-ttu-id="7393c-671">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-671">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="7393c-672">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-672">mode</span></span>  
<span data-ttu-id="7393c-673">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-673">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="7393c-674">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="7393c-674">Return Value - left</span></span>

<span data-ttu-id="7393c-675">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="7393c-675">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="7393c-676">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-676">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="7393c-677">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-677">Parameters - leftMargin</span></span>

<span data-ttu-id="7393c-678">値</span><span class="sxs-lookup"><span data-stu-id="7393c-678">value</span></span>  

<!-- -->

<span data-ttu-id="7393c-679">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-679">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="7393c-680">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-680">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="7393c-681">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-681">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="7393c-682">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-682">Parameters - leftMarginMode</span></span>

<span data-ttu-id="7393c-683">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-683">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="7393c-684">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-684">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="7393c-685">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-685">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="7393c-686">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-686">Parameters - leftMarginValue</span></span>

<span data-ttu-id="7393c-687">値</span><span class="sxs-lookup"><span data-stu-id="7393c-687">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="7393c-688">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-688">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="7393c-689">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="7393c-689">Method leftMode</span></span>

<span data-ttu-id="7393c-690">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-690">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="7393c-691">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="7393c-691">Parameters - leftMode</span></span>

<span data-ttu-id="7393c-692">値</span><span class="sxs-lookup"><span data-stu-id="7393c-692">value</span></span>  
<span data-ttu-id="7393c-693">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-693">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="7393c-694">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="7393c-694">Return Value - leftMode</span></span>

<span data-ttu-id="7393c-695">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="7393c-695">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="7393c-696">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="7393c-696">Method leftValue</span></span>

<span data-ttu-id="7393c-697">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-697">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="7393c-698">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="7393c-698">Parameters - leftValue</span></span>

<span data-ttu-id="7393c-699">値</span><span class="sxs-lookup"><span data-stu-id="7393c-699">value</span></span>  
<span data-ttu-id="7393c-700">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-700">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="7393c-701">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="7393c-701">Return Value - leftValue</span></span>

<span data-ttu-id="7393c-702">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="7393c-702">The horizontal position of the control in the form.</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="7393c-703">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="7393c-703">Method markAsUserAdd</span></span>

<span data-ttu-id="7393c-704">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="7393c-704">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="7393c-705">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="7393c-705">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="7393c-706">値</span><span class="sxs-lookup"><span data-stu-id="7393c-706">value</span></span>  
<span data-ttu-id="7393c-707">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-707">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="7393c-708">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="7393c-708">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="7393c-709">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7393c-709">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="7393c-710">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7393c-710">Method mouseDblClick</span></span>

<span data-ttu-id="7393c-711">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-711">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="7393c-712">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7393c-712">Parameters - mouseDblClick</span></span>

<span data-ttu-id="7393c-713">x</span><span class="sxs-lookup"><span data-stu-id="7393c-713">x</span></span>  
<span data-ttu-id="7393c-714">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-714">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-715">y</span><span class="sxs-lookup"><span data-stu-id="7393c-715">y</span></span>  
<span data-ttu-id="7393c-716">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-716">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-717">ボタン</span><span class="sxs-lookup"><span data-stu-id="7393c-717">button</span></span>  
<span data-ttu-id="7393c-718">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-718">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-719">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7393c-719">Ctrl</span></span>  
<span data-ttu-id="7393c-720">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-720">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-721">シフト</span><span class="sxs-lookup"><span data-stu-id="7393c-721">Shift</span></span>  
<span data-ttu-id="7393c-722">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-722">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="7393c-723">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7393c-723">Return Value - mouseDblClick</span></span>

<span data-ttu-id="7393c-724">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7393c-724">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="7393c-725">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="7393c-725">Remarks - mouseDblClick</span></span>

<span data-ttu-id="7393c-726">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-726">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="7393c-727">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="7393c-727">Method mouseDown</span></span>

<span data-ttu-id="7393c-728">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-728">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="7393c-729">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="7393c-729">Parameters - mouseDown</span></span>

<span data-ttu-id="7393c-730">x</span><span class="sxs-lookup"><span data-stu-id="7393c-730">x</span></span>  
<span data-ttu-id="7393c-731">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-731">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-732">y</span><span class="sxs-lookup"><span data-stu-id="7393c-732">y</span></span>  
<span data-ttu-id="7393c-733">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-733">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-734">ボタン</span><span class="sxs-lookup"><span data-stu-id="7393c-734">button</span></span>  
<span data-ttu-id="7393c-735">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-735">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-736">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7393c-736">Ctrl</span></span>  
<span data-ttu-id="7393c-737">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-737">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-738">シフト</span><span class="sxs-lookup"><span data-stu-id="7393c-738">Shift</span></span>  
<span data-ttu-id="7393c-739">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-739">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="7393c-740">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="7393c-740">Return Value - mouseDown</span></span>

<span data-ttu-id="7393c-741">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7393c-741">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="7393c-742">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="7393c-742">Remarks - mouseDown</span></span>

<span data-ttu-id="7393c-743">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-743">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="7393c-744">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-744">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="7393c-745">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="7393c-745">Method mouseMove</span></span>

<span data-ttu-id="7393c-746">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-746">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="7393c-747">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="7393c-747">Parameters - mouseMove</span></span>

<span data-ttu-id="7393c-748">x</span><span class="sxs-lookup"><span data-stu-id="7393c-748">x</span></span>  
<span data-ttu-id="7393c-749">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-749">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-750">y</span><span class="sxs-lookup"><span data-stu-id="7393c-750">y</span></span>  
<span data-ttu-id="7393c-751">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-751">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-752">ボタン</span><span class="sxs-lookup"><span data-stu-id="7393c-752">button</span></span>  
<span data-ttu-id="7393c-753">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-753">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-754">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7393c-754">Ctrl</span></span>  
<span data-ttu-id="7393c-755">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-755">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-756">シフト</span><span class="sxs-lookup"><span data-stu-id="7393c-756">Shift</span></span>  
<span data-ttu-id="7393c-757">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-757">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="7393c-758">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="7393c-758">Return Value - mouseMove</span></span>

<span data-ttu-id="7393c-759">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7393c-759">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="7393c-760">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="7393c-760">Remarks - mouseMove</span></span>

<span data-ttu-id="7393c-761">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-761">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="7393c-762">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="7393c-762">Method mouseUp</span></span>

<span data-ttu-id="7393c-763">ユーザーがコントロール エリア上でマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-763">Is called when the user releases the mouse button over the control area.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="7393c-764">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="7393c-764">Parameters - mouseUp</span></span>

<span data-ttu-id="7393c-765">x</span><span class="sxs-lookup"><span data-stu-id="7393c-765">x</span></span>  
<span data-ttu-id="7393c-766">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-766">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-767">y</span><span class="sxs-lookup"><span data-stu-id="7393c-767">y</span></span>  
<span data-ttu-id="7393c-768">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-768">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-769">ボタン</span><span class="sxs-lookup"><span data-stu-id="7393c-769">button</span></span>  
<span data-ttu-id="7393c-770">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-770">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-771">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7393c-771">Ctrl</span></span>  
<span data-ttu-id="7393c-772">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-772">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-773">シフト</span><span class="sxs-lookup"><span data-stu-id="7393c-773">Shift</span></span>  
<span data-ttu-id="7393c-774">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-774">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="7393c-775">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="7393c-775">Return Value - mouseUp</span></span>

<span data-ttu-id="7393c-776">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7393c-776">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="7393c-777">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="7393c-777">Remarks - mouseUp</span></span>

<span data-ttu-id="7393c-778">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-778">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="7393c-779">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-779">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-name"></a><span data-ttu-id="7393c-780">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7393c-780">Method name</span></span>

<span data-ttu-id="7393c-781">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-781">Gets or sets the name that is used in code to identify a form, report, table, query, or other  application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="7393c-782">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="7393c-782">Parameters - name</span></span>

<span data-ttu-id="7393c-783">値</span><span class="sxs-lookup"><span data-stu-id="7393c-783">value</span></span>  
<span data-ttu-id="7393c-784">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="7393c-784">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="7393c-785">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="7393c-785">Return Value - name</span></span>

<span data-ttu-id="7393c-786">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7393c-786">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="7393c-787">備考 - name</span><span class="sxs-lookup"><span data-stu-id="7393c-787">Remarks - name</span></span>

<span data-ttu-id="7393c-788">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7393c-788">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7393c-789">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7393c-789">It must begin with a letter.</span></span>
-   <span data-ttu-id="7393c-790">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7393c-790">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="7393c-791">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7393c-791">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="7393c-792">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7393c-792">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7393c-793">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7393c-793">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="7393c-794">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="7393c-794">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="7393c-795">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="7393c-795">Parameters - neededPermission</span></span>

<span data-ttu-id="7393c-796">値</span><span class="sxs-lookup"><span data-stu-id="7393c-796">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="7393c-797">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="7393c-797">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="7393c-798">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7393c-798">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="7393c-799">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7393c-799">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="7393c-800">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="7393c-800">Method parentControl</span></span>

<span data-ttu-id="7393c-801">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-801">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="7393c-802">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="7393c-802">Return Value - parentControl</span></span>

<span data-ttu-id="7393c-803">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="7393c-803">The parent control for the control.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="7393c-804">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-804">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="7393c-805">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-805">Parameters - rightMargin</span></span>

<span data-ttu-id="7393c-806">値</span><span class="sxs-lookup"><span data-stu-id="7393c-806">value</span></span>  

<!-- -->

<span data-ttu-id="7393c-807">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-807">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="7393c-808">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-808">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="7393c-809">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-809">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="7393c-810">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-810">Parameters - rightMarginMode</span></span>

<span data-ttu-id="7393c-811">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-811">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="7393c-812">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-812">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="7393c-813">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-813">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="7393c-814">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-814">Parameters - rightMarginValue</span></span>

<span data-ttu-id="7393c-815">値</span><span class="sxs-lookup"><span data-stu-id="7393c-815">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="7393c-816">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-816">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="7393c-817">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="7393c-817">Method securityKey</span></span>

<span data-ttu-id="7393c-818">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-818">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="7393c-819">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="7393c-819">Parameters - securityKey</span></span>

<span data-ttu-id="7393c-820">値</span><span class="sxs-lookup"><span data-stu-id="7393c-820">value</span></span>  
<span data-ttu-id="7393c-821">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-821">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="7393c-822">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="7393c-822">Return Value - securityKey</span></span>

<span data-ttu-id="7393c-823">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="7393c-823">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="7393c-824">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="7393c-824">Method showContextMenu</span></span>

<span data-ttu-id="7393c-825">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-825">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="7393c-826">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="7393c-826">Parameters - showContextMenu</span></span>

<span data-ttu-id="7393c-827">menuHandle</span><span class="sxs-lookup"><span data-stu-id="7393c-827">menuHandle</span></span>  
<span data-ttu-id="7393c-828">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="7393c-828">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="7393c-829">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="7393c-829">Return Value - showContextMenu</span></span>

<span data-ttu-id="7393c-830">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-830">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-skip"></a><span data-ttu-id="7393c-831">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="7393c-831">Method skip</span></span>

<span data-ttu-id="7393c-832">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-832">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="7393c-833">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="7393c-833">Parameters - skip</span></span>

<span data-ttu-id="7393c-834">値</span><span class="sxs-lookup"><span data-stu-id="7393c-834">value</span></span>  
<span data-ttu-id="7393c-835">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-835">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="7393c-836">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="7393c-836">Return Value - skip</span></span>

<span data-ttu-id="7393c-837">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7393c-837">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="7393c-838">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="7393c-838">Remarks - skip</span></span>

<span data-ttu-id="7393c-839">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="7393c-839">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

## <a name="method-sort"></a><span data-ttu-id="7393c-840">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="7393c-840">Method sort</span></span>

```xpp
public int sort([SortOrder sortDirection])
```

### <a name="parameters---sort"></a><span data-ttu-id="7393c-841">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="7393c-841">Parameters - sort</span></span>

<span data-ttu-id="7393c-842">sortDirection</span><span class="sxs-lookup"><span data-stu-id="7393c-842">sortDirection</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="7393c-843">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="7393c-843">Return Value - sort</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="7393c-844">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="7393c-844">Method toolTip</span></span>

<span data-ttu-id="7393c-845">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="7393c-845">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="7393c-846">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="7393c-846">Return Value - toolTip</span></span>

<span data-ttu-id="7393c-847">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="7393c-847">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="7393c-848">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="7393c-848">Remarks - toolTip</span></span>

<span data-ttu-id="7393c-849">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="7393c-849">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="7393c-850">メソッド top</span><span class="sxs-lookup"><span data-stu-id="7393c-850">Method top</span></span>

<span data-ttu-id="7393c-851">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-851">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="7393c-852">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="7393c-852">Parameters - top</span></span>

<span data-ttu-id="7393c-853">値</span><span class="sxs-lookup"><span data-stu-id="7393c-853">value</span></span>  
<span data-ttu-id="7393c-854">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-854">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="7393c-855">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-855">mode</span></span>  
<span data-ttu-id="7393c-856">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-856">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="7393c-857">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="7393c-857">Return Value - top</span></span>

<span data-ttu-id="7393c-858">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="7393c-858">The vertical position of the control in the form.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="7393c-859">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-859">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="7393c-860">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-860">Parameters - topMargin</span></span>

<span data-ttu-id="7393c-861">値</span><span class="sxs-lookup"><span data-stu-id="7393c-861">value</span></span>  

<!-- -->

<span data-ttu-id="7393c-862">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-862">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="7393c-863">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="7393c-863">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="7393c-864">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-864">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="7393c-865">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-865">Parameters - topMarginMode</span></span>

<span data-ttu-id="7393c-866">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-866">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="7393c-867">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="7393c-867">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="7393c-868">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-868">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="7393c-869">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-869">Parameters - topMarginValue</span></span>

<span data-ttu-id="7393c-870">値</span><span class="sxs-lookup"><span data-stu-id="7393c-870">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="7393c-871">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="7393c-871">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="7393c-872">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="7393c-872">Method topMode</span></span>

<span data-ttu-id="7393c-873">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-873">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="7393c-874">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="7393c-874">Parameters - topMode</span></span>

<span data-ttu-id="7393c-875">値</span><span class="sxs-lookup"><span data-stu-id="7393c-875">value</span></span>  
<span data-ttu-id="7393c-876">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-876">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="7393c-877">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="7393c-877">Return Value - topMode</span></span>

<span data-ttu-id="7393c-878">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="7393c-878">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="7393c-879">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="7393c-879">Method topValue</span></span>

<span data-ttu-id="7393c-880">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-880">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="7393c-881">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="7393c-881">Parameters - topValue</span></span>

<span data-ttu-id="7393c-882">値</span><span class="sxs-lookup"><span data-stu-id="7393c-882">value</span></span>  
<span data-ttu-id="7393c-883">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-883">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="7393c-884">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="7393c-884">Return Value - topValue</span></span>

<span data-ttu-id="7393c-885">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="7393c-885">The vertical position of the control in the form.</span></span>

## <a name="method-type"></a><span data-ttu-id="7393c-886">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="7393c-886">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="7393c-887">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="7393c-887">Parameters - type</span></span>

<span data-ttu-id="7393c-888">値</span><span class="sxs-lookup"><span data-stu-id="7393c-888">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="7393c-889">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="7393c-889">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="7393c-890">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7393c-890">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="7393c-891">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7393c-891">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="7393c-892">データ</span><span class="sxs-lookup"><span data-stu-id="7393c-892">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="7393c-893">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="7393c-893">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="7393c-894">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="7393c-894">Method userData</span></span>

<span data-ttu-id="7393c-895">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-895">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="7393c-896">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="7393c-896">Parameters - userData</span></span>

<span data-ttu-id="7393c-897">値</span><span class="sxs-lookup"><span data-stu-id="7393c-897">value</span></span>  
<span data-ttu-id="7393c-898">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-898">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="7393c-899">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="7393c-899">Return Value - userData</span></span>

<span data-ttu-id="7393c-900">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="7393c-900">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="7393c-901">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="7393c-901">Method userDataItem</span></span>

<span data-ttu-id="7393c-902">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-902">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="7393c-903">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="7393c-903">Parameters - userDataItem</span></span>

<span data-ttu-id="7393c-904">値</span><span class="sxs-lookup"><span data-stu-id="7393c-904">value</span></span>  
<span data-ttu-id="7393c-905">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-905">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="7393c-906">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="7393c-906">Return Value - userDataItem</span></span>

<span data-ttu-id="7393c-907">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="7393c-907">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="7393c-908">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="7393c-908">Method userDataItems</span></span>

<span data-ttu-id="7393c-909">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-909">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="7393c-910">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="7393c-910">Parameters - userDataItems</span></span>

<span data-ttu-id="7393c-911">値</span><span class="sxs-lookup"><span data-stu-id="7393c-911">value</span></span>  
<span data-ttu-id="7393c-912">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-912">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="7393c-913">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="7393c-913">Return Value - userDataItems</span></span>

<span data-ttu-id="7393c-914">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="7393c-914">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="7393c-915">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="7393c-915">Method userDisable</span></span>

<span data-ttu-id="7393c-916">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-916">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="7393c-917">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="7393c-917">Parameters - userDisable</span></span>

<span data-ttu-id="7393c-918">値</span><span class="sxs-lookup"><span data-stu-id="7393c-918">value</span></span>  
<span data-ttu-id="7393c-919">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-919">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="7393c-920">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="7393c-920">Return Value - userDisable</span></span>

<span data-ttu-id="7393c-921">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="7393c-921">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="7393c-922">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="7393c-922">Method userHeight</span></span>

<span data-ttu-id="7393c-923">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-923">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="7393c-924">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="7393c-924">Parameters - userHeight</span></span>

<span data-ttu-id="7393c-925">値</span><span class="sxs-lookup"><span data-stu-id="7393c-925">value</span></span>  
<span data-ttu-id="7393c-926">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-926">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="7393c-927">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="7393c-927">Return Value - userHeight</span></span>

<span data-ttu-id="7393c-928">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="7393c-928">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="7393c-929">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="7393c-929">Method userHide</span></span>

<span data-ttu-id="7393c-930">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-930">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="7393c-931">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="7393c-931">Parameters - userHide</span></span>

<span data-ttu-id="7393c-932">値</span><span class="sxs-lookup"><span data-stu-id="7393c-932">value</span></span>  
<span data-ttu-id="7393c-933">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-933">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="7393c-934">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="7393c-934">Return Value - userHide</span></span>

<span data-ttu-id="7393c-935">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="7393c-935">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="7393c-936">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="7393c-936">Remarks - userHide</span></span>

<span data-ttu-id="7393c-937">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-937">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="7393c-938">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="7393c-938">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="7393c-939">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="7393c-939">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="7393c-940">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="7393c-940">Method userOrgContainer</span></span>

<span data-ttu-id="7393c-941">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-941">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="7393c-942">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="7393c-942">Parameters - userOrgContainer</span></span>

<span data-ttu-id="7393c-943">値</span><span class="sxs-lookup"><span data-stu-id="7393c-943">value</span></span>  
<span data-ttu-id="7393c-944">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-944">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="7393c-945">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="7393c-945">Return Value - userOrgContainer</span></span>

<span data-ttu-id="7393c-946">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="7393c-946">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="7393c-947">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="7393c-947">Method userOrgSibling</span></span>

<span data-ttu-id="7393c-948">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-948">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="7393c-949">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="7393c-949">Parameters - userOrgSibling</span></span>

<span data-ttu-id="7393c-950">値</span><span class="sxs-lookup"><span data-stu-id="7393c-950">value</span></span>  
<span data-ttu-id="7393c-951">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-951">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="7393c-952">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="7393c-952">Return Value - userOrgSibling</span></span>

<span data-ttu-id="7393c-953">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="7393c-953">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="7393c-954">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="7393c-954">Method userPromptText</span></span>

<span data-ttu-id="7393c-955">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-955">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="7393c-956">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="7393c-956">Parameters - userPromptText</span></span>

<span data-ttu-id="7393c-957">値</span><span class="sxs-lookup"><span data-stu-id="7393c-957">value</span></span>  
<span data-ttu-id="7393c-958">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-958">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="7393c-959">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="7393c-959">Return Value - userPromptText</span></span>

<span data-ttu-id="7393c-960">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="7393c-960">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="7393c-961">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="7393c-961">Method userSecurityLevel</span></span>

<span data-ttu-id="7393c-962">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-962">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="7393c-963">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="7393c-963">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="7393c-964">値</span><span class="sxs-lookup"><span data-stu-id="7393c-964">value</span></span>  
<span data-ttu-id="7393c-965">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-965">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="7393c-966">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="7393c-966">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="7393c-967">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="7393c-967">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="7393c-968">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="7393c-968">Method userSkip</span></span>

<span data-ttu-id="7393c-969">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-969">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="7393c-970">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="7393c-970">Parameters - userSkip</span></span>

<span data-ttu-id="7393c-971">値</span><span class="sxs-lookup"><span data-stu-id="7393c-971">value</span></span>  
<span data-ttu-id="7393c-972">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-972">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="7393c-973">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="7393c-973">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="7393c-974">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="7393c-974">Return Value - userSkip</span></span>

<span data-ttu-id="7393c-975">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="7393c-975">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="7393c-976">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="7393c-976">Method userWidth</span></span>

<span data-ttu-id="7393c-977">ピクセル単位でコントロールの幅を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-977">Sets or returns the width of the control in pixels.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="7393c-978">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="7393c-978">Parameters - userWidth</span></span>

<span data-ttu-id="7393c-979">値</span><span class="sxs-lookup"><span data-stu-id="7393c-979">value</span></span>  
<span data-ttu-id="7393c-980">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-980">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="7393c-981">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="7393c-981">Return Value - userWidth</span></span>

<span data-ttu-id="7393c-982">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="7393c-982">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="7393c-983">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="7393c-983">Remarks - userWidth</span></span>

<span data-ttu-id="7393c-984">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-984">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="7393c-985">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="7393c-985">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="7393c-986">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="7393c-986">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="7393c-987">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="7393c-987">Method verticalSpacing</span></span>

<span data-ttu-id="7393c-988">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-988">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="7393c-989">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="7393c-989">Parameters - verticalSpacing</span></span>

<span data-ttu-id="7393c-990">値</span><span class="sxs-lookup"><span data-stu-id="7393c-990">value</span></span>  
<span data-ttu-id="7393c-991">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-991">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="7393c-992">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-992">mode</span></span>  
<span data-ttu-id="7393c-993">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-993">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="7393c-994">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="7393c-994">Return Value - verticalSpacing</span></span>

<span data-ttu-id="7393c-995">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="7393c-995">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="7393c-996">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="7393c-996">Method verticalSpacingMode</span></span>

<span data-ttu-id="7393c-997">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-997">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="7393c-998">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="7393c-998">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="7393c-999">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-999">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="7393c-1000">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="7393c-1000">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="7393c-1001">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="7393c-1001">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="7393c-1002">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="7393c-1002">Method verticalSpacingValue</span></span>

<span data-ttu-id="7393c-1003">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1003">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="7393c-1004">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="7393c-1004">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="7393c-1005">値</span><span class="sxs-lookup"><span data-stu-id="7393c-1005">value</span></span>  
<span data-ttu-id="7393c-1006">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-1006">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="7393c-1007">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="7393c-1007">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="7393c-1008">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="7393c-1008">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="7393c-1009">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="7393c-1009">Method visible</span></span>

<span data-ttu-id="7393c-1010">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1010">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="7393c-1011">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="7393c-1011">Parameters - visible</span></span>

<span data-ttu-id="7393c-1012">値</span><span class="sxs-lookup"><span data-stu-id="7393c-1012">value</span></span>  
<span data-ttu-id="7393c-1013">コントロールの可視化設定に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-1013">The value to assign to the visibility setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="7393c-1014">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="7393c-1014">Return Value - visible</span></span>

<span data-ttu-id="7393c-1015">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7393c-1015">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="7393c-1016">メソッド width</span><span class="sxs-lookup"><span data-stu-id="7393c-1016">Method width</span></span>

<span data-ttu-id="7393c-1017">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1017">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="7393c-1018">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="7393c-1018">Parameters - width</span></span>

<span data-ttu-id="7393c-1019">値</span><span class="sxs-lookup"><span data-stu-id="7393c-1019">value</span></span>  
<span data-ttu-id="7393c-1020">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-1020">An Integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="7393c-1021">モード</span><span class="sxs-lookup"><span data-stu-id="7393c-1021">mode</span></span>  
<span data-ttu-id="7393c-1022">幅の計算方法を示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-1022">An Integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="7393c-1023">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="7393c-1023">Return Value - width</span></span>

<span data-ttu-id="7393c-1024">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="7393c-1024">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="7393c-1025">備考 - width</span><span class="sxs-lookup"><span data-stu-id="7393c-1025">Remarks - width</span></span>

<span data-ttu-id="7393c-1026">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1026">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="7393c-1027">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="7393c-1027">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="7393c-1028">モード。</span><span class="sxs-lookup"><span data-stu-id="7393c-1028">Mode.</span></span>           | <span data-ttu-id="7393c-1029">幅計算。</span><span class="sxs-lookup"><span data-stu-id="7393c-1029">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7393c-1030">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="7393c-1030">-1 Exact.</span></span>       | <span data-ttu-id="7393c-1031">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1031">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7393c-1032">0 自動。</span><span class="sxs-lookup"><span data-stu-id="7393c-1032">0 Auto.</span></span>         | <span data-ttu-id="7393c-1033">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1033">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7393c-1034">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="7393c-1034">1 Column width.</span></span> | <span data-ttu-id="7393c-1035">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="7393c-1035">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="7393c-1036">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1036">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="7393c-1037">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="7393c-1037">Method widthMode</span></span>

<span data-ttu-id="7393c-1038">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1038">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="7393c-1039">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="7393c-1039">Parameters - widthMode</span></span>

<span data-ttu-id="7393c-1040">値</span><span class="sxs-lookup"><span data-stu-id="7393c-1040">value</span></span>  
<span data-ttu-id="7393c-1041">コントロール幅の計算方法を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="7393c-1041">An integer value that indicates how control width is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="7393c-1042">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="7393c-1042">Return Value - widthMode</span></span>

<span data-ttu-id="7393c-1043">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1043">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="7393c-1044">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="7393c-1044">Remarks - widthMode</span></span>

<span data-ttu-id="7393c-1045">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="7393c-1045">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="7393c-1046">モード。</span><span class="sxs-lookup"><span data-stu-id="7393c-1046">Mode.</span></span>         | <span data-ttu-id="7393c-1047">幅計算。</span><span class="sxs-lookup"><span data-stu-id="7393c-1047">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7393c-1048">正確。</span><span class="sxs-lookup"><span data-stu-id="7393c-1048">Exact.</span></span>        | <span data-ttu-id="7393c-1049">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1049">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7393c-1050">自動。</span><span class="sxs-lookup"><span data-stu-id="7393c-1050">Auto.</span></span>         | <span data-ttu-id="7393c-1051">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1051">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7393c-1052">列の幅。</span><span class="sxs-lookup"><span data-stu-id="7393c-1052">Column width.</span></span> | <span data-ttu-id="7393c-1053">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="7393c-1053">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="7393c-1054">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="7393c-1054">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="7393c-1055">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="7393c-1055">Method widthValue</span></span>

<span data-ttu-id="7393c-1056">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1056">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="7393c-1057">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="7393c-1057">Parameters - widthValue</span></span>

<span data-ttu-id="7393c-1058">値</span><span class="sxs-lookup"><span data-stu-id="7393c-1058">value</span></span>  
<span data-ttu-id="7393c-1059">幅をピクセル単位で指定する整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-1059">An Integer that specifies the width in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="7393c-1060">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="7393c-1060">Return Value - widthValue</span></span>

<span data-ttu-id="7393c-1061">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="7393c-1061">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="7393c-1062">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="7393c-1062">Remarks - widthValue</span></span>

<span data-ttu-id="7393c-1063">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1063">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-onenter"></a><span data-ttu-id="7393c-1064">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="7393c-1064">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="7393c-1065">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="7393c-1065">Parameters - OnEnter</span></span>

<span data-ttu-id="7393c-1066">sender</span><span class="sxs-lookup"><span data-stu-id="7393c-1066">sender</span></span>  

<!-- -->

<span data-ttu-id="7393c-1067">e</span><span class="sxs-lookup"><span data-stu-id="7393c-1067">e</span></span>  

## <a name="method-lostfocus"></a><span data-ttu-id="7393c-1068">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="7393c-1068">Method lostFocus</span></span>

<span data-ttu-id="7393c-1069">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1069">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-drop"></a><span data-ttu-id="7393c-1070">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="7393c-1070">Method drop</span></span>

<span data-ttu-id="7393c-1071">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1071">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="7393c-1072">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="7393c-1072">Parameters - drop</span></span>

<span data-ttu-id="7393c-1073">dragSource</span><span class="sxs-lookup"><span data-stu-id="7393c-1073">dragSource</span></span>  
<span data-ttu-id="7393c-1074">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1074">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-1075">dragMode</span><span class="sxs-lookup"><span data-stu-id="7393c-1075">dragMode</span></span>  
<span data-ttu-id="7393c-1076">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1076">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-1077">x</span><span class="sxs-lookup"><span data-stu-id="7393c-1077">x</span></span>  
<span data-ttu-id="7393c-1078">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1078">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-1079">y</span><span class="sxs-lookup"><span data-stu-id="7393c-1079">y</span></span>  
<span data-ttu-id="7393c-1080">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1080">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-paste"></a><span data-ttu-id="7393c-1081">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="7393c-1081">Method paste</span></span>

<span data-ttu-id="7393c-1082">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1082">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-setfocus"></a><span data-ttu-id="7393c-1083">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="7393c-1083">Method setFocus</span></span>

<span data-ttu-id="7393c-1084">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1084">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-onleaving"></a><span data-ttu-id="7393c-1085">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="7393c-1085">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="7393c-1086">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="7393c-1086">Parameters - OnLeaving</span></span>

<span data-ttu-id="7393c-1087">sender</span><span class="sxs-lookup"><span data-stu-id="7393c-1087">sender</span></span>  

<!-- -->

<span data-ttu-id="7393c-1088">e</span><span class="sxs-lookup"><span data-stu-id="7393c-1088">e</span></span>  

## <a name="method-mouseleave"></a><span data-ttu-id="7393c-1089">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="7393c-1089">Method mouseLeave</span></span>

<span data-ttu-id="7393c-1090">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1090">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-gotfocus"></a><span data-ttu-id="7393c-1091">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="7393c-1091">Method gotFocus</span></span>

<span data-ttu-id="7393c-1092">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1092">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-dragleave"></a><span data-ttu-id="7393c-1093">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="7393c-1093">Method dragLeave</span></span>

<span data-ttu-id="7393c-1094">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1094">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-enter"></a><span data-ttu-id="7393c-1095">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="7393c-1095">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-dropex"></a><span data-ttu-id="7393c-1096">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="7393c-1096">Method dropEx</span></span>

<span data-ttu-id="7393c-1097">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1097">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="7393c-1098">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="7393c-1098">Parameters - dropEx</span></span>

<span data-ttu-id="7393c-1099">dragSource</span><span class="sxs-lookup"><span data-stu-id="7393c-1099">dragSource</span></span>  
<span data-ttu-id="7393c-1100">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1100">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-1101">dragMode</span><span class="sxs-lookup"><span data-stu-id="7393c-1101">dragMode</span></span>  
<span data-ttu-id="7393c-1102">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1102">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-1103">x</span><span class="sxs-lookup"><span data-stu-id="7393c-1103">x</span></span>  
<span data-ttu-id="7393c-1104">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1104">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="7393c-1105">y</span><span class="sxs-lookup"><span data-stu-id="7393c-1105">y</span></span>  
<span data-ttu-id="7393c-1106">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1106">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="7393c-1107">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="7393c-1107">Method mouseEnter</span></span>

<span data-ttu-id="7393c-1108">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1108">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="7393c-1109">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="7393c-1109">Parameters - mouseEnter</span></span>

<span data-ttu-id="7393c-1110">x</span><span class="sxs-lookup"><span data-stu-id="7393c-1110">x</span></span>  
<span data-ttu-id="7393c-1111">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1111">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-1112">y</span><span class="sxs-lookup"><span data-stu-id="7393c-1112">y</span></span>  
<span data-ttu-id="7393c-1113">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1113">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-1114">ボタン</span><span class="sxs-lookup"><span data-stu-id="7393c-1114">button</span></span>  
<span data-ttu-id="7393c-1115">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1115">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-1116">Ctrl</span><span class="sxs-lookup"><span data-stu-id="7393c-1116">Ctrl</span></span>  
<span data-ttu-id="7393c-1117">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1117">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="7393c-1118">シフト</span><span class="sxs-lookup"><span data-stu-id="7393c-1118">Shift</span></span>  
<span data-ttu-id="7393c-1119">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7393c-1119">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-jumpref"></a><span data-ttu-id="7393c-1120">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="7393c-1120">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="7393c-1121">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="7393c-1121">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="7393c-1122">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="7393c-1122">Parameters - OnLostFocus</span></span>

<span data-ttu-id="7393c-1123">sender</span><span class="sxs-lookup"><span data-stu-id="7393c-1123">sender</span></span>  

<!-- -->

<span data-ttu-id="7393c-1124">e</span><span class="sxs-lookup"><span data-stu-id="7393c-1124">e</span></span>  

## <a name="method-ongotfocus"></a><span data-ttu-id="7393c-1125">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="7393c-1125">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="7393c-1126">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="7393c-1126">Parameters - OnGotFocus</span></span>

<span data-ttu-id="7393c-1127">sender</span><span class="sxs-lookup"><span data-stu-id="7393c-1127">sender</span></span>  

<!-- -->

<span data-ttu-id="7393c-1128">e</span><span class="sxs-lookup"><span data-stu-id="7393c-1128">e</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="7393c-1129">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="7393c-1129">Method prefColumnSize</span></span>

<span data-ttu-id="7393c-1130">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1130">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="7393c-1131">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="7393c-1131">Parameters - prefColumnSize</span></span>

<span data-ttu-id="7393c-1132">width</span><span class="sxs-lookup"><span data-stu-id="7393c-1132">width</span></span>  
<span data-ttu-id="7393c-1133">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="7393c-1133">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="7393c-1134">height</span><span class="sxs-lookup"><span data-stu-id="7393c-1134">height</span></span>  
<span data-ttu-id="7393c-1135">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="7393c-1135">The preferred height of the control.</span></span>

## <a name="method-cut"></a><span data-ttu-id="7393c-1136">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="7393c-1136">Method cut</span></span>

<span data-ttu-id="7393c-1137">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="7393c-1137">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="7393c-1138">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="7393c-1138">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="7393c-1139">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="7393c-1139">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="7393c-1140">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="7393c-1140">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="7393c-1141">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="7393c-1141">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="7393c-1142">overrideObject</span><span class="sxs-lookup"><span data-stu-id="7393c-1142">overrideObject</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="7393c-1143">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="7393c-1143">Method displayControl</span></span>

<span data-ttu-id="7393c-1144">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1144">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-copy"></a><span data-ttu-id="7393c-1145">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="7393c-1145">Method copy</span></span>

<span data-ttu-id="7393c-1146">コントロールの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7393c-1146">Copies the contents of the control to the clipboard.</span></span>

```xpp
public void copy()
```

## <a name="method-context"></a><span data-ttu-id="7393c-1147">メソッド context</span><span class="sxs-lookup"><span data-stu-id="7393c-1147">Method context</span></span>

<span data-ttu-id="7393c-1148">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1148">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="7393c-1149">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="7393c-1149">Method resetUserSetting</span></span>

<span data-ttu-id="7393c-1150">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="7393c-1150">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-inputsearch"></a><span data-ttu-id="7393c-1151">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="7393c-1151">Method inputSearch</span></span>

<span data-ttu-id="7393c-1152">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1152">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="7393c-1153">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="7393c-1153">Parameters - inputSearch</span></span>

<span data-ttu-id="7393c-1154">searchStr</span><span class="sxs-lookup"><span data-stu-id="7393c-1154">searchStr</span></span>  
<span data-ttu-id="7393c-1155">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="7393c-1155">The string value to use to filter data; optional.</span></span>

## <a name="method-filter"></a><span data-ttu-id="7393c-1156">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="7393c-1156">Method filter</span></span>

```xpp
public void filter([str filterStr])
```

### <a name="parameters---filter"></a><span data-ttu-id="7393c-1157">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="7393c-1157">Parameters - filter</span></span>

<span data-ttu-id="7393c-1158">filterStr</span><span class="sxs-lookup"><span data-stu-id="7393c-1158">filterStr</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="7393c-1159">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="7393c-1159">Method endDrag</span></span>

<span data-ttu-id="7393c-1160">ユーザーがフォーム コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7393c-1160">Is called when the user has finished dragging a form control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="7393c-1161">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="7393c-1161">Remarks - endDrag</span></span>

<span data-ttu-id="7393c-1162">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="7393c-1162">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="7393c-1163">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="7393c-1163">To drag a control, a user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

