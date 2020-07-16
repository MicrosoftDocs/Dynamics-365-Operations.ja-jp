---
title: FormTreeControl クラス
description: このトピックでは、FormTreeControl クラスについて説明します。
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
ms.openlocfilehash: a1d3eb39f31d1de510102f890114cfe20698ab51
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502619"
---
# <a name="class-formtreecontrol"></a><span data-ttu-id="5ec08-103">クラス FormTreeControl</span><span class="sxs-lookup"><span data-stu-id="5ec08-103">Class FormTreeControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormTreeControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="5ec08-104">備考</span><span class="sxs-lookup"><span data-stu-id="5ec08-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="5ec08-105">例</span><span class="sxs-lookup"><span data-stu-id="5ec08-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="5ec08-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="5ec08-106">Methods</span></span>

| <span data-ttu-id="5ec08-107">方法</span><span class="sxs-lookup"><span data-stu-id="5ec08-107">Method</span></span>                                                                                                      | <span data-ttu-id="5ec08-108">説明</span><span class="sxs-lookup"><span data-stu-id="5ec08-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec08-109">public int add(int parent, int insertAfter, str Text, \[int image\], \[int children\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-109">public int add(int parent, int insertAfter, str Text, \[int image\], \[int children\])</span></span>                      |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-110">public int addItem(int parent, int insertAfter, FormTreeItem item)</span><span class="sxs-lookup"><span data-stu-id="5ec08-110">public int addItem(int parent, int insertAfter, FormTreeItem item)</span></span>                                          |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="5ec08-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-112">Determines whether to align the control.</span></span>                                                                                                                                |
| <span data-ttu-id="5ec08-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="5ec08-114">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-114">Determines whether the user can modify the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="5ec08-115">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="5ec08-115">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="5ec08-116">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-116">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="5ec08-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="5ec08-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="5ec08-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="5ec08-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-120">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="5ec08-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="5ec08-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-122">Determines whether the control background can be transparent.</span></span>                                                                                                          |
| <span data-ttu-id="5ec08-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="5ec08-123">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="5ec08-124">ユーザーがフォーム ツリー コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-124">Is called when the user starts to drag a form tree control.</span></span>                                                                                                             |
| <span data-ttu-id="5ec08-125">public boolean beginLabelEdit(int Idx, str text, AnyType data)</span><span class="sxs-lookup"><span data-stu-id="5ec08-125">public boolean beginLabelEdit(int Idx, str text, AnyType data)</span></span>                                              |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-126">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-126">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="5ec08-127">コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-127">Gets or sets the font weight that is used to display text in the control.</span></span>                                                                                               |
| <span data-ttu-id="5ec08-128">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-128">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="5ec08-129">コントロールの境界のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-129">Gets or sets the style of the border for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="5ec08-130">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="5ec08-130">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="5ec08-131">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-131">Retrieves the size of the control.</span></span>                                                                                                                                      |
| <span data-ttu-id="5ec08-132">public boolean canScroll(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-132">public boolean canScroll(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-133">public boolean cascadeSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-133">public boolean cascadeSelect(\[boolean value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-134">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-134">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="5ec08-135">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-135">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="5ec08-136">public boolean checkBox(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-136">public boolean checkBox(\[boolean value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-137">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-137">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="5ec08-138">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-138">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="5ec08-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-139">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="5ec08-140">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-140">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="5ec08-141">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="5ec08-141">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="5ec08-142">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-142">Returns a list that contains the IDs of configuration keys that are in effect for the control.</span></span>                                                                          |
| <span data-ttu-id="5ec08-143">public int copyItem(int Idx, int newParent, \[int insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-143">public int copyItem(int Idx, int newParent, \[int insertAfter\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-144">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-144">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="5ec08-145">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-145">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="5ec08-146">public Imagelist createDragImagelist()</span><span class="sxs-lookup"><span data-stu-id="5ec08-146">public Imagelist createDragImagelist()</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-147">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-147">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="5ec08-148">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-148">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="5ec08-149">public boolean delete(int Idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-149">public boolean delete(int Idx)</span></span>                                                                              | <span data-ttu-id="5ec08-150">フォーム ツリー コントロールから指定した項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-150">Deletes the specified item from the form tree control.</span></span>                                                                                                                  |
| <span data-ttu-id="5ec08-151">public boolean deleteAll()</span><span class="sxs-lookup"><span data-stu-id="5ec08-151">public boolean deleteAll()</span></span>                                                                                  | <span data-ttu-id="5ec08-152">フォーム ツリー コントロールからすべての項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-152">Deletes all items from the form tree control.</span></span>                                                                                                                           |
| <span data-ttu-id="5ec08-153">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-153">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="5ec08-154">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-154">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="5ec08-155">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-155">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="5ec08-156">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-156">Determines whether drag-and-drop operations are enabled or disabled for the control.</span></span>                                                                                    |
| <span data-ttu-id="5ec08-157">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="5ec08-157">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="5ec08-158">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-158">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>                                                                          |
| <span data-ttu-id="5ec08-159">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="5ec08-159">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="5ec08-160">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-160">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="5ec08-161">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="5ec08-161">public str dragText()</span></span>                                                                                       | <span data-ttu-id="5ec08-162">フォーム ツリー コントロールをドラッグしたときに表示されるテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-162">Returns the text that is displayed when the form tree control is dragged.</span></span>                                                                                               |
| <span data-ttu-id="5ec08-163">public boolean editLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-163">public boolean editLabels(\[boolean value\])</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-164">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-164">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="5ec08-165">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-165">Determines whether the object is enabled or disabled.</span></span>                                                                                                                   |
| <span data-ttu-id="5ec08-166">public int expand(int Idx, \[FormTreeExpand action\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-166">public int expand(int Idx, \[FormTreeExpand action\])</span></span>                                                       |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-167">public boolean expanding(int Idx, FormTreeExpand action, AnyType data)</span><span class="sxs-lookup"><span data-stu-id="5ec08-167">public boolean expanding(int Idx, FormTreeExpand action, AnyType data)</span></span>                                      |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-168">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-168">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="5ec08-169">コントロール内のテキストに使用されるフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-169">Gets or sets the name of the font that is used for the text in the control.</span></span>                                                                                             |
| <span data-ttu-id="5ec08-170">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-170">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="5ec08-171">コントロール内のテキストに使用されるフォント サイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-171">Gets or sets the font size that is used for the text in the control.</span></span>                                                                                                    |
| <span data-ttu-id="5ec08-172">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-172">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="5ec08-173">コントロール内のテキストに使用される色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-173">Gets or sets the color that is used for the text in the control.</span></span>                                                                                                        |
| <span data-ttu-id="5ec08-174">public int getChild(int Idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-174">public int getChild(int Idx)</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-175">public int getFirstSelected()</span><span class="sxs-lookup"><span data-stu-id="5ec08-175">public int getFirstSelected()</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-176">public int getFirstVisible()</span><span class="sxs-lookup"><span data-stu-id="5ec08-176">public int getFirstVisible()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-177">public Imagelist getImagelist()</span><span class="sxs-lookup"><span data-stu-id="5ec08-177">public Imagelist getImagelist()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-178">public FormTreeItem getItem(int Idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-178">public FormTreeItem getItem(int Idx)</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-179">public int getNextSelected(int idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-179">public int getNextSelected(int idx)</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-180">public int getNextSibling(int Idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-180">public int getNextSibling(int Idx)</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-181">public int getNextVisible(int Idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-181">public int getNextVisible(int Idx)</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-182">public int getParent(int Idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-182">public int getParent(int Idx)</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-183">public int getPrevSelected(int idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-183">public int getPrevSelected(int idx)</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-184">public int getPrevSibling(int Idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-184">public int getPrevSibling(int Idx)</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-185">public int getPrevVisible(int Idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-185">public int getPrevVisible(int Idx)</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-186">public int getRoot()</span><span class="sxs-lookup"><span data-stu-id="5ec08-186">public int getRoot()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-187">public int getSelectedCount()</span><span class="sxs-lookup"><span data-stu-id="5ec08-187">public int getSelectedCount()</span></span>                                                                               |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-188">public int getSelection()</span><span class="sxs-lookup"><span data-stu-id="5ec08-188">public int getSelection()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-189">public Imagelist getStateImagelist()</span><span class="sxs-lookup"><span data-stu-id="5ec08-189">public Imagelist getStateImagelist()</span></span>                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-190">public int getVisibleCount()</span><span class="sxs-lookup"><span data-stu-id="5ec08-190">public int getVisibleCount()</span></span>                                                                                | <span data-ttu-id="5ec08-191">ツリー コントロール内の表示されている項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-191">Returns the number of visible items in the tree control.</span></span>                                                                                                                |
| <span data-ttu-id="5ec08-192">public boolean hasButtons(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-192">public boolean hasButtons(\[boolean value\])</span></span>                                                                | <span data-ttu-id="5ec08-193">ツリー コントロールが展開/折り畳みボタンを表示するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-193">Returns a value that indicates whether the tree control uses expand/collapse buttons.</span></span>                                                                                   |
| <span data-ttu-id="5ec08-194">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-194">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="5ec08-195">ツリー コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-195">Sets or returns a value that indicates whether the contents of the tree control have changed.</span></span>                                                                           |
| <span data-ttu-id="5ec08-196">public boolean hasLines(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-196">public boolean hasLines(\[boolean value\])</span></span>                                                                  | <span data-ttu-id="5ec08-197">ツリー コントロールがツリー コネクタ明細行を表示するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-197">Returns a value that indicates whether the tree control displays tree connector lines.</span></span>                                                                                  |
| <span data-ttu-id="5ec08-198">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="5ec08-198">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="5ec08-199">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-199">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="5ec08-200">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-200">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="5ec08-201">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-201">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="5ec08-202">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-202">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="5ec08-203">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-203">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="5ec08-204">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-204">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="5ec08-205">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-205">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="5ec08-206">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="5ec08-206">public str helpField()</span></span>                                                                                      | <span data-ttu-id="5ec08-207">コントロールのヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-207">Returns the Help text for the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="5ec08-208">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-208">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="5ec08-209">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-209">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>                                                         |
| <span data-ttu-id="5ec08-210">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-210">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="5ec08-211">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-211">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="5ec08-212">public container hitTest(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="5ec08-212">public container hitTest(int x, int y)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-213">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="5ec08-213">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="5ec08-214">コントロールの Windows ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-214">Returns the Windows handle for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="5ec08-215">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="5ec08-215">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="5ec08-216">コントロールがコンテナーかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-216">Returns a value that indicates whether the control is a container.</span></span>                                                                                                      |
| <span data-ttu-id="5ec08-217">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="5ec08-217">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="5ec08-218">コントロールが表示されるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-218">Returns a value that indicates whether the control is displayed.</span></span>                                                                                                        |
| <span data-ttu-id="5ec08-219">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="5ec08-219">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="5ec08-220">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-220">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="5ec08-221">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="5ec08-221">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="5ec08-222">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-222">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                   |
| <span data-ttu-id="5ec08-223">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-223">public boolean italic(\[boolean value\])</span></span>                                                                    | <span data-ttu-id="5ec08-224">コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-224">Sets or returns a value that indicates whether the text in the control is italic.</span></span>                                                                                       |
| <span data-ttu-id="5ec08-225">public boolean keyDown(int vKey, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="5ec08-225">public boolean keyDown(int vKey, boolean Ctrl, boolean Shift)</span></span>                                               |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-226">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="5ec08-226">public boolean leave()</span></span>                                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-227">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-227">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="5ec08-228">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-228">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="5ec08-229">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-229">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="5ec08-230">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-230">Sets the horizontal arrange mode for the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="5ec08-231">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-231">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="5ec08-232">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-232">Gets or sets the horizontal position of the control in the form.</span></span>                                                                                                        |
| <span data-ttu-id="5ec08-233">public boolean linesAtRoot(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-233">public boolean linesAtRoot(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-234">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-234">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="5ec08-235">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="5ec08-235">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="5ec08-236">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="5ec08-236">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="5ec08-237">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-237">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="5ec08-238">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="5ec08-238">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="5ec08-239">ユーザーがマウス ポインターがコントロール上にある状態でクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-239">Is called when the user clicks while the mouse pointer is over the control.</span></span>                                                                                             |
| <span data-ttu-id="5ec08-240">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="5ec08-240">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="5ec08-241">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-241">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="5ec08-242">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="5ec08-242">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="5ec08-243">マウス ポインターがコントロール上にある状態で、ユーザーがマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-243">Is called when the user releases the mouse button while the mouse pointer is over the control.</span></span>                                                                          |
| <span data-ttu-id="5ec08-244">public int moveItem(int Idx, int newParent, \[int insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-244">public int moveItem(int Idx, int newParent, \[int insertAfter\])</span></span>                                            |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-245">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-245">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="5ec08-246">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-246">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                               |
| <span data-ttu-id="5ec08-247">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-247">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-248">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="5ec08-248">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-249">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="5ec08-249">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="5ec08-250">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-250">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="5ec08-251">public boolean rowSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-251">public boolean rowSelect(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-252">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-252">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="5ec08-253">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-253">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="5ec08-254">public int select(int Idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-254">public int select(int Idx)</span></span>                                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-255">public int selectEx(int Idx, boolean setSelection)</span><span class="sxs-lookup"><span data-stu-id="5ec08-255">public int selectEx(int Idx, boolean setSelection)</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-256">public boolean selectionChanging(FormTreeItem OldItem, FormTreeItem NewItem, FormTreeSelect how)</span><span class="sxs-lookup"><span data-stu-id="5ec08-256">public boolean selectionChanging(FormTreeItem OldItem, FormTreeItem NewItem, FormTreeSelect how)</span></span>            |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-257">public int selectItems(int fromIdx, int toIdx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-257">public int selectItems(int fromIdx, int toIdx)</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-258">public int selectSetFirstVisible(int Idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-258">public int selectSetFirstVisible(int Idx)</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-259">public boolean setInsertMark(int Idx, boolean After)</span><span class="sxs-lookup"><span data-stu-id="5ec08-259">public boolean setInsertMark(int Idx, boolean After)</span></span>                                                        |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-260">public boolean setItem(FormTreeItem item)</span><span class="sxs-lookup"><span data-stu-id="5ec08-260">public boolean setItem(FormTreeItem item)</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-261">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="5ec08-261">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="5ec08-262">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-262">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="5ec08-263">public boolean showSelAlways(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-263">public boolean showSelAlways(\[boolean value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-264">public boolean singleSelection(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-264">public boolean singleSelection(\[boolean value\])</span></span>                                                           |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-265">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-265">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="5ec08-266">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-266">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="5ec08-267">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="5ec08-267">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="5ec08-268">コントロールのツールヒント テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-268">Returns the tooltip text for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="5ec08-269">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-269">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="5ec08-270">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-270">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="5ec08-271">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-271">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="5ec08-272">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-272">Sets the vertical arrange mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="5ec08-273">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-273">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="5ec08-274">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-274">Gets or sets the vertical position of the control in the form.</span></span>                                                                                                          |
| <span data-ttu-id="5ec08-275">public boolean trackSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-275">public boolean trackSelect(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-276">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-276">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-277">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-277">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-278">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="5ec08-278">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-279">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-279">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="5ec08-280">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-280">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="5ec08-281">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-281">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="5ec08-282">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-282">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="5ec08-283">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-283">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="5ec08-284">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-284">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="5ec08-285">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-285">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="5ec08-286">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-286">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="5ec08-287">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-287">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="5ec08-288">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-288">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="5ec08-289">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-289">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="5ec08-290">フォーム ツリー コントロールがユーザーから非表示になっているかどうかを示す値を返すか設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-290">Returns or sets the value that indicates whether the form tree control is hidden from the user.</span></span>                                                                         |
| <span data-ttu-id="5ec08-291">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-291">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="5ec08-292">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-292">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="5ec08-293">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-293">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="5ec08-294">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-294">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="5ec08-295">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-295">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="5ec08-296">コントロールのユーザー プロンプト テキストを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-296">Sets or retrieves the user prompt text for the control.</span></span>                                                                                                                 |
| <span data-ttu-id="5ec08-297">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-297">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="5ec08-298">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-298">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="5ec08-299">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-299">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="5ec08-300">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-300">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="5ec08-301">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-301">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="5ec08-302">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-302">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="5ec08-303">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-303">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="5ec08-304">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-304">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="5ec08-305">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-305">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="5ec08-306">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-306">Sets the vertical spacing mode for the control in the form.</span></span>                                                                                                             |
| <span data-ttu-id="5ec08-307">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-307">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="5ec08-308">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-308">Gets or sets the vertical spacing of the control in the form.</span></span>                                                                                                           |
| <span data-ttu-id="5ec08-309">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-309">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="5ec08-310">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-310">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="5ec08-311">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-311">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="5ec08-312">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-312">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="5ec08-313">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-313">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="5ec08-314">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-314">Gets or sets the calculation mode for the width of the control.</span></span>                                                                                                         |
| <span data-ttu-id="5ec08-315">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-315">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="5ec08-316">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-316">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="5ec08-317">public void checkedStateChanged(int Idx, FormTreeCheckedState newState)</span><span class="sxs-lookup"><span data-stu-id="5ec08-317">public void checkedStateChanged(int Idx, FormTreeCheckedState newState)</span></span>                                     |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-318">public void endLabelEdit(int Idx, str text, AnyType data)</span><span class="sxs-lookup"><span data-stu-id="5ec08-318">public void endLabelEdit(int Idx, str text, AnyType data)</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-319">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="5ec08-319">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="5ec08-320">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-320">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>                                                                      |
| <span data-ttu-id="5ec08-321">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="5ec08-321">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="5ec08-322">ユーザーがマウス ポインターをコントロールに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-322">Is called when the user moves the mouse pointer into the control.</span></span>                                                                                                       |
| <span data-ttu-id="5ec08-323">private void OnExpanding(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-323">private void OnExpanding(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-324">public void cut()</span><span class="sxs-lookup"><span data-stu-id="5ec08-324">public void cut()</span></span>                                                                                           | <span data-ttu-id="5ec08-325">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="5ec08-325">Cuts the contents of the control.</span></span>                                                                                                                                       |
| <span data-ttu-id="5ec08-326">public void paste()</span><span class="sxs-lookup"><span data-stu-id="5ec08-326">public void paste()</span></span>                                                                                         | <span data-ttu-id="5ec08-327">フォーム ツリー コントロールをフォームに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-327">Pastes the form tree control in the form.</span></span>                                                                                                                               |
| <span data-ttu-id="5ec08-328">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="5ec08-328">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="5ec08-329">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="5ec08-329">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="5ec08-330">public void itemMoved(int OldIdx, int NewIdx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-330">public void itemMoved(int OldIdx, int NewIdx)</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-331">public void expanded(int Idx, FormTreeExpand action, AnyType data)</span><span class="sxs-lookup"><span data-stu-id="5ec08-331">public void expanded(int Idx, FormTreeExpand action, AnyType data)</span></span>                                          |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-332">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="5ec08-332">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="5ec08-333">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-333">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="5ec08-334">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-334">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                         |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-335">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-335">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-336">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="5ec08-336">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="5ec08-337">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-337">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="5ec08-338">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="5ec08-338">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="5ec08-339">ユーザーがマウス ポインターをコントロールから移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-339">Is called when the user moves the mouse pointer out of the control.</span></span>                                                                                                     |
| <span data-ttu-id="5ec08-340">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="5ec08-340">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="5ec08-341">ユーザーがフォーム ツリー コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-341">Is called when the user has finished dragging a form tree control.</span></span>                                                                                                      |
| <span data-ttu-id="5ec08-342">public void context()</span><span class="sxs-lookup"><span data-stu-id="5ec08-342">public void context()</span></span>                                                                                       | <span data-ttu-id="5ec08-343">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-343">Shows the shortcut menu for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="5ec08-344">public void itemCopy(int OldIdx, int NewIdx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-344">public void itemCopy(int OldIdx, int NewIdx)</span></span>                                                                |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-345">public void enter()</span><span class="sxs-lookup"><span data-stu-id="5ec08-345">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-346">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="5ec08-346">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="5ec08-347">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-347">Performs data filtering for the control, based on the specified string.</span></span>                                                                                                 |
| <span data-ttu-id="5ec08-348">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="5ec08-348">public void displayControl()</span></span>                                                                                | <span data-ttu-id="5ec08-349">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-349">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="5ec08-350">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="5ec08-350">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="5ec08-351">フォーム ツリー コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-351">Specifies the preferred column width and height for the form tree control.</span></span>                                                                                              |
| <span data-ttu-id="5ec08-352">public void setImagelist(Imagelist imageList)</span><span class="sxs-lookup"><span data-stu-id="5ec08-352">public void setImagelist(Imagelist imageList)</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-353">private void OnExpanded(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-353">private void OnExpanded(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-354">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="5ec08-354">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="5ec08-355">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-355">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>                                                                        |
| <span data-ttu-id="5ec08-356">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="5ec08-356">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="5ec08-357">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-357">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="5ec08-358">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-358">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-359">public void itemDeleted(int Idx, AnyType data)</span><span class="sxs-lookup"><span data-stu-id="5ec08-359">public void itemDeleted(int Idx, AnyType data)</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-360">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="5ec08-360">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="5ec08-361">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-361">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="5ec08-362">public void setStateImagelist(Imagelist imageList)</span><span class="sxs-lookup"><span data-stu-id="5ec08-362">public void setStateImagelist(Imagelist imageList)</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-363">public void endEditLabel(boolean cancel)</span><span class="sxs-lookup"><span data-stu-id="5ec08-363">public void endEditLabel(boolean cancel)</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-364">public void copy()</span><span class="sxs-lookup"><span data-stu-id="5ec08-364">public void copy()</span></span>                                                                                          | <span data-ttu-id="5ec08-365">フォーム ツリー コントロールをコピーします。</span><span class="sxs-lookup"><span data-stu-id="5ec08-365">Copies the form tree control.</span></span>                                                                                                                                           |
| <span data-ttu-id="5ec08-366">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-366">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-367">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-367">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-368">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="5ec08-368">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="5ec08-369">public void selectionChanged(FormTreeItem OldItem, FormTreeItem NewItem, FormTreeSelect how)</span><span class="sxs-lookup"><span data-stu-id="5ec08-369">public void selectionChanged(FormTreeItem OldItem, FormTreeItem NewItem, FormTreeSelect how)</span></span>                | <span data-ttu-id="5ec08-370">ユーザーがフォーム ツリー コントロールで選択した項目を変更したことを示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-370">Indicates that the user has changed the selected item in the form tree control.</span></span>                                                                                         |
| <span data-ttu-id="5ec08-371">public void beginEditLabel(int Idx)</span><span class="sxs-lookup"><span data-stu-id="5ec08-371">public void beginEditLabel(int Idx)</span></span>                                                                         |                                                                                                                                                                         |

## <a name="method-add"></a><span data-ttu-id="5ec08-372">メソッド add</span><span class="sxs-lookup"><span data-stu-id="5ec08-372">Method add</span></span>

```xpp
public int add(int parent, int insertAfter, str Text, [int image], [int children])
```

### <a name="parameters---add"></a><span data-ttu-id="5ec08-373">パラメーター - add</span><span class="sxs-lookup"><span data-stu-id="5ec08-373">Parameters - add</span></span>

<span data-ttu-id="5ec08-374">parent</span><span class="sxs-lookup"><span data-stu-id="5ec08-374">parent</span></span>  

<!-- -->

<span data-ttu-id="5ec08-375">insertAfter</span><span class="sxs-lookup"><span data-stu-id="5ec08-375">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="5ec08-376">テキスト</span><span class="sxs-lookup"><span data-stu-id="5ec08-376">Text</span></span>  

<!-- -->

<span data-ttu-id="5ec08-377">画像</span><span class="sxs-lookup"><span data-stu-id="5ec08-377">image</span></span>  

<!-- -->

<span data-ttu-id="5ec08-378">children</span><span class="sxs-lookup"><span data-stu-id="5ec08-378">children</span></span>  

### <a name="return-value---add"></a><span data-ttu-id="5ec08-379">戻り値 - add</span><span class="sxs-lookup"><span data-stu-id="5ec08-379">Return Value - add</span></span>

## <a name="method-additem"></a><span data-ttu-id="5ec08-380">メソッド addItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-380">Method addItem</span></span>

```xpp
public int addItem(int parent, int insertAfter, FormTreeItem item)
```

### <a name="parameters---additem"></a><span data-ttu-id="5ec08-381">パラメーター - addItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-381">Parameters - addItem</span></span>

<span data-ttu-id="5ec08-382">parent</span><span class="sxs-lookup"><span data-stu-id="5ec08-382">parent</span></span>  

<!-- -->

<span data-ttu-id="5ec08-383">insertAfter</span><span class="sxs-lookup"><span data-stu-id="5ec08-383">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="5ec08-384">品目</span><span class="sxs-lookup"><span data-stu-id="5ec08-384">item</span></span>  

### <a name="return-value---additem"></a><span data-ttu-id="5ec08-385">戻り値 - addItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-385">Return Value - addItem</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="5ec08-386">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="5ec08-386">Method alignControl</span></span>

<span data-ttu-id="5ec08-387">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-387">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="5ec08-388">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="5ec08-388">Parameters - alignControl</span></span>

<span data-ttu-id="5ec08-389">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-389">value</span></span>  
<span data-ttu-id="5ec08-390">プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-390">The new value for the property; optional.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="5ec08-391">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="5ec08-391">Return Value - alignControl</span></span>

<span data-ttu-id="5ec08-392">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-392">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="5ec08-393">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="5ec08-393">Remarks - alignControl</span></span>

<span data-ttu-id="5ec08-394">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-394">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="5ec08-395">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="5ec08-395">Method allowEdit</span></span>

<span data-ttu-id="5ec08-396">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-396">Determines whether the user can modify the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="5ec08-397">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="5ec08-397">Parameters - allowEdit</span></span>

<span data-ttu-id="5ec08-398">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-398">value</span></span>  
<span data-ttu-id="5ec08-399">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-399">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="5ec08-400">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="5ec08-400">Return Value - allowEdit</span></span>

<span data-ttu-id="5ec08-401">コントロールを変更することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-401">true if the control can be modified; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="5ec08-402">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="5ec08-402">Remarks - allowEdit</span></span>

<span data-ttu-id="5ec08-403">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-403">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

### <a name="examples---allowedit"></a><span data-ttu-id="5ec08-404">例 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="5ec08-404">Examples - allowEdit</span></span>

<span data-ttu-id="5ec08-405">次の例は、allowEdit プロパティの値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-405">The following example shows how to return and set the value of the allowEdit property.</span></span>

```xpp
// Return the value. 
info (strfmt("allowEdit: %1", this.allowEdit())); 
// Set the value. 
this.allowEdit(false);
```

## <a name="method-allowsyssetup"></a><span data-ttu-id="5ec08-406">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="5ec08-406">Method allowSysSetup</span></span>

<span data-ttu-id="5ec08-407">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-407">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="5ec08-408">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="5ec08-408">Return Value - allowSysSetup</span></span>

<span data-ttu-id="5ec08-409">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-409">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="5ec08-410">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="5ec08-410">Method autoDeclaration</span></span>

<span data-ttu-id="5ec08-411">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-411">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="5ec08-412">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="5ec08-412">Parameters - autoDeclaration</span></span>

<span data-ttu-id="5ec08-413">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-413">value</span></span>  
<span data-ttu-id="5ec08-414">autoDeclaration プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-414">The value to assign to the autoDeclaration property.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="5ec08-415">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="5ec08-415">Return Value - autoDeclaration</span></span>

<span data-ttu-id="5ec08-416">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-416">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="5ec08-417">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="5ec08-417">Remarks - autoDeclaration</span></span>

<span data-ttu-id="5ec08-418">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-418">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="5ec08-419">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="5ec08-419">Method backgroundColor</span></span>

<span data-ttu-id="5ec08-420">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-420">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="5ec08-421">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="5ec08-421">Parameters - backgroundColor</span></span>

<span data-ttu-id="5ec08-422">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-422">value</span></span>  
<span data-ttu-id="5ec08-423">コントロールの背景色として割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-423">The value to assign as the background color of the control.</span></span>

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="5ec08-424">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="5ec08-424">Return Value - backgroundColor</span></span>

<span data-ttu-id="5ec08-425">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="5ec08-425">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="5ec08-426">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="5ec08-426">Remarks - backgroundColor</span></span>

<span data-ttu-id="5ec08-427">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-427">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="5ec08-428">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-428">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="5ec08-429">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-429">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="5ec08-430">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-430">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="5ec08-431">上位バイトは 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-431">The high-order byte must be 0 (zero).</span></span>
-   <span data-ttu-id="5ec08-432">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-432">The maximum value for a single byte is 255.</span></span>

### <a name="examples---backgroundcolor"></a><span data-ttu-id="5ec08-433">例 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="5ec08-433">Examples - backgroundColor</span></span>

<span data-ttu-id="5ec08-434">次の例は、コントロールの背景色を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-434">The following example shows how to return and set the background color for a control.</span></span>

```xpp
// Retrieve the existing background color. 
info (strfmt("Background color: %1", this.backgroundColor())); 
// Set the background color. 
this.backgroundColor(WindowsPalette::DarkShadow3D);
```

## <a name="method-backstyle"></a><span data-ttu-id="5ec08-435">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="5ec08-435">Method backStyle</span></span>

<span data-ttu-id="5ec08-436">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-436">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="5ec08-437">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="5ec08-437">Parameters - backStyle</span></span>

<span data-ttu-id="5ec08-438">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-438">value</span></span>  
<span data-ttu-id="5ec08-439">コントロールの背景スタイルとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-439">The value to assign as the background style of the control.</span></span>

### <a name="return-value---backstyle"></a><span data-ttu-id="5ec08-440">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="5ec08-440">Return Value - backStyle</span></span>

<span data-ttu-id="5ec08-441">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-441">1 if the control background can be transparent; otherwise, 0.</span></span>

### <a name="examples---backstyle"></a><span data-ttu-id="5ec08-442">例 - backStyle</span><span class="sxs-lookup"><span data-stu-id="5ec08-442">Examples - backStyle</span></span>

<span data-ttu-id="5ec08-443">次の例は、背景スタイルを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-443">The following example shows how to return and set the background style.</span></span>

```xpp
// Return the background style. 
info (strfmt("Background style: %1", this.backStyle())); 
// Set the background style. 
this.backStyle(FormBackStyle::Transparent);
```

## <a name="method-begindrag"></a><span data-ttu-id="5ec08-444">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="5ec08-444">Method beginDrag</span></span>

<span data-ttu-id="5ec08-445">ユーザーがフォーム ツリー コントロールのドラッグを始めると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-445">Is called when the user starts to drag a form tree control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="5ec08-446">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="5ec08-446">Parameters - beginDrag</span></span>

<span data-ttu-id="5ec08-447">x</span><span class="sxs-lookup"><span data-stu-id="5ec08-447">x</span></span>  
<span data-ttu-id="5ec08-448">マウス ポインターの y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-448">An Integer data type that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="5ec08-449">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-449">The coordinate is relative to the upper-left corner of the control.</span></span>

<!-- -->

<span data-ttu-id="5ec08-450">y</span><span class="sxs-lookup"><span data-stu-id="5ec08-450">y</span></span>  
<span data-ttu-id="5ec08-451">マウス ポインターの y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-451">An Integer data type that indicates the y-coordinate of the mouse pointer.</span></span> <span data-ttu-id="5ec08-452">座標はコントロールの左上隅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-452">The coordinate is relative to the upper-left corner of the control.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="5ec08-453">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="5ec08-453">Return Value - beginDrag</span></span>

<span data-ttu-id="5ec08-454">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-454">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="5ec08-455">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="5ec08-455">Remarks - beginDrag</span></span>

<span data-ttu-id="5ec08-456">このイベントは、コントロールの DragDrop プロパティが有効でない限り発生しません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-456">This event is not raised unless the DragDrop property is enabled for the control.</span></span> <span data-ttu-id="5ec08-457">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-457">To drag a control, the user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="examples---begindrag"></a><span data-ttu-id="5ec08-458">例 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="5ec08-458">Examples - beginDrag</span></span>

<span data-ttu-id="5ec08-459">次の例では、ユーザーがフォーム ツリー コントロールのドラッグを開始したときに、Infolog の x 座標と y 座標を表示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-459">The following example displays the x-coordinates and y-coordinates in the Infolog when the user starts to drag the form tree control.</span></span>

```xpp
public int beginDrag(int _x, int _y) 
{ 
    int ret; 
    info(strfmt("beginDrag (x, y) : (%1, %2)", _x, _y)); 
    ret = super(_x, _y); 
    return ret; 
}
```

## <a name="method-beginlabeledit"></a><span data-ttu-id="5ec08-460">メソッド beginLabelEdit</span><span class="sxs-lookup"><span data-stu-id="5ec08-460">Method beginLabelEdit</span></span>

```xpp
public boolean beginLabelEdit(int Idx, str text, AnyType data)
```

### <a name="parameters---beginlabeledit"></a><span data-ttu-id="5ec08-461">パラメーター - beginLabelEdit</span><span class="sxs-lookup"><span data-stu-id="5ec08-461">Parameters - beginLabelEdit</span></span>

<span data-ttu-id="5ec08-462">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-462">Idx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-463">テキスト</span><span class="sxs-lookup"><span data-stu-id="5ec08-463">text</span></span>  

<!-- -->

<span data-ttu-id="5ec08-464">データ</span><span class="sxs-lookup"><span data-stu-id="5ec08-464">data</span></span>  

### <a name="return-value---beginlabeledit"></a><span data-ttu-id="5ec08-465">戻り値 - beginLabelEdit</span><span class="sxs-lookup"><span data-stu-id="5ec08-465">Return Value - beginLabelEdit</span></span>

## <a name="method-bold"></a><span data-ttu-id="5ec08-466">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="5ec08-466">Method bold</span></span>

<span data-ttu-id="5ec08-467">コントロール内のテキストを表示するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-467">Gets or sets the font weight that is used to display text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="5ec08-468">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="5ec08-468">Parameters - bold</span></span>

<span data-ttu-id="5ec08-469">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-469">value</span></span>  
<span data-ttu-id="5ec08-470">コントロールのボールド設定に割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-470">The value to assign to the bold setting for the control.</span></span>

### <a name="return-value---bold"></a><span data-ttu-id="5ec08-471">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="5ec08-471">Return Value - bold</span></span>

<span data-ttu-id="5ec08-472">0 (ゼロ) から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-472">An integer value between 0 (zero) and 9, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="5ec08-473">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="5ec08-473">Remarks - bold</span></span>

<span data-ttu-id="5ec08-474">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-474">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="5ec08-475">0 � 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-475">0 � Use the default font weight.</span></span>
-   <span data-ttu-id="5ec08-476">1 � シン。</span><span class="sxs-lookup"><span data-stu-id="5ec08-476">1 � Thin.</span></span>
-   <span data-ttu-id="5ec08-477">2 � エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="5ec08-477">2 � Extra-light.</span></span>
-   <span data-ttu-id="5ec08-478">3 � ライト。</span><span class="sxs-lookup"><span data-stu-id="5ec08-478">3 � Light.</span></span>
-   <span data-ttu-id="5ec08-479">4 � 標準。</span><span class="sxs-lookup"><span data-stu-id="5ec08-479">4 � Normal.</span></span>
-   <span data-ttu-id="5ec08-480">5 � 中。</span><span class="sxs-lookup"><span data-stu-id="5ec08-480">5 � Medium.</span></span>
-   <span data-ttu-id="5ec08-481">6 � セミボールド。</span><span class="sxs-lookup"><span data-stu-id="5ec08-481">6 � Semibold.</span></span>
-   <span data-ttu-id="5ec08-482">7 � 太字。</span><span class="sxs-lookup"><span data-stu-id="5ec08-482">7 � Bold.</span></span>
-   <span data-ttu-id="5ec08-483">8 � 極太。</span><span class="sxs-lookup"><span data-stu-id="5ec08-483">8 � Extra-bold.</span></span>
-   <span data-ttu-id="5ec08-484">9 � ヘビー。</span><span class="sxs-lookup"><span data-stu-id="5ec08-484">9 � Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="5ec08-485">メソッド border</span><span class="sxs-lookup"><span data-stu-id="5ec08-485">Method border</span></span>

<span data-ttu-id="5ec08-486">コントロールの境界のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-486">Gets or sets the style of the border for the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="5ec08-487">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="5ec08-487">Parameters - border</span></span>

<span data-ttu-id="5ec08-488">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-488">value</span></span>  
<span data-ttu-id="5ec08-489">コントロールの境界スタイルとして割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-489">The value to assign as the border style for the control; optional.</span></span>

### <a name="return-value---border"></a><span data-ttu-id="5ec08-490">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="5ec08-490">Return Value - border</span></span>

<span data-ttu-id="5ec08-491">0 (ゼロ) から 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="5ec08-491">An integer between 0 (zero) and 4, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="5ec08-492">備考 - border</span><span class="sxs-lookup"><span data-stu-id="5ec08-492">Remarks - border</span></span>

<span data-ttu-id="5ec08-493">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-493">The integer that is returned contains the style of the border for the control as follows.</span></span>

| <span data-ttu-id="5ec08-494">先頭値</span><span class="sxs-lookup"><span data-stu-id="5ec08-494">Value</span></span> | <span data-ttu-id="5ec08-495">説明</span><span class="sxs-lookup"><span data-stu-id="5ec08-495">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="5ec08-496">0</span><span class="sxs-lookup"><span data-stu-id="5ec08-496">0</span></span>     | <span data-ttu-id="5ec08-497">自動</span><span class="sxs-lookup"><span data-stu-id="5ec08-497">Auto</span></span>        |
| <span data-ttu-id="5ec08-498">1</span><span class="sxs-lookup"><span data-stu-id="5ec08-498">1</span></span>     | <span data-ttu-id="5ec08-499">3D</span><span class="sxs-lookup"><span data-stu-id="5ec08-499">3D</span></span>          |
| <span data-ttu-id="5ec08-500">2</span><span class="sxs-lookup"><span data-stu-id="5ec08-500">2</span></span>     | <span data-ttu-id="5ec08-501">1 行</span><span class="sxs-lookup"><span data-stu-id="5ec08-501">Single line</span></span> |
| <span data-ttu-id="5ec08-502">3</span><span class="sxs-lookup"><span data-stu-id="5ec08-502">3</span></span>     | <span data-ttu-id="5ec08-503">集合住宅</span><span class="sxs-lookup"><span data-stu-id="5ec08-503">Flat</span></span>        |
| <span data-ttu-id="5ec08-504">4</span><span class="sxs-lookup"><span data-stu-id="5ec08-504">4</span></span>     | <span data-ttu-id="5ec08-505">None</span><span class="sxs-lookup"><span data-stu-id="5ec08-505">None</span></span>        |

### <a name="examples---border"></a><span data-ttu-id="5ec08-506">例 - border</span><span class="sxs-lookup"><span data-stu-id="5ec08-506">Examples - border</span></span>

<span data-ttu-id="5ec08-507">次の例は、コントロールの境界線のスタイルを取得および設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-507">The following example shows how to retrieve and set the border style for a control.</span></span>

```xpp
// Retrieve the border style. 
info (strfmt("border: %1", this.border())); 
// Set the border style. 
this.border(2);
```

## <a name="method-calccontrolsize"></a><span data-ttu-id="5ec08-508">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="5ec08-508">Method calcControlSize</span></span>

<span data-ttu-id="5ec08-509">コントロールのサイズを取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-509">Retrieves the size of the control.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="5ec08-510">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="5ec08-510">Parameters - calcControlSize</span></span>

<span data-ttu-id="5ec08-511">chars</span><span class="sxs-lookup"><span data-stu-id="5ec08-511">chars</span></span>  
<span data-ttu-id="5ec08-512">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="5ec08-512">The number of lines to use to determine the height.</span></span>

<!-- -->

<span data-ttu-id="5ec08-513">明細行</span><span class="sxs-lookup"><span data-stu-id="5ec08-513">lines</span></span>  
<span data-ttu-id="5ec08-514">高さを決定するために使用する行数。</span><span class="sxs-lookup"><span data-stu-id="5ec08-514">The number of lines to use to determine the height.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="5ec08-515">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="5ec08-515">Return Value - calcControlSize</span></span>

<span data-ttu-id="5ec08-516">幅と高さを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="5ec08-516">The container that holds the width and height.</span></span>

## <a name="method-canscroll"></a><span data-ttu-id="5ec08-517">メソッド canScroll</span><span class="sxs-lookup"><span data-stu-id="5ec08-517">Method canScroll</span></span>

```xpp
public boolean canScroll([boolean value])
```

### <a name="parameters---canscroll"></a><span data-ttu-id="5ec08-518">パラメーター - canScroll</span><span class="sxs-lookup"><span data-stu-id="5ec08-518">Parameters - canScroll</span></span>

<span data-ttu-id="5ec08-519">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-519">value</span></span>  

### <a name="return-value---canscroll"></a><span data-ttu-id="5ec08-520">戻り値 - canScroll</span><span class="sxs-lookup"><span data-stu-id="5ec08-520">Return Value - canScroll</span></span>

## <a name="method-cascadeselect"></a><span data-ttu-id="5ec08-521">メソッド cascadeSelect</span><span class="sxs-lookup"><span data-stu-id="5ec08-521">Method cascadeSelect</span></span>

```xpp
public boolean cascadeSelect([boolean value])
```

### <a name="parameters---cascadeselect"></a><span data-ttu-id="5ec08-522">パラメーター - cascadeSelect</span><span class="sxs-lookup"><span data-stu-id="5ec08-522">Parameters - cascadeSelect</span></span>

<span data-ttu-id="5ec08-523">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-523">value</span></span>  

### <a name="return-value---cascadeselect"></a><span data-ttu-id="5ec08-524">戻り値 - cascadeSelect</span><span class="sxs-lookup"><span data-stu-id="5ec08-524">Return Value - cascadeSelect</span></span>

## <a name="method-characterset"></a><span data-ttu-id="5ec08-525">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="5ec08-525">Method characterSet</span></span>

<span data-ttu-id="5ec08-526">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-526">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="5ec08-527">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="5ec08-527">Parameters - characterSet</span></span>

<span data-ttu-id="5ec08-528">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-528">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="5ec08-529">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="5ec08-529">Return Value - characterSet</span></span>

<span data-ttu-id="5ec08-530">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-530">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="5ec08-531">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="5ec08-531">Remarks - characterSet</span></span>

<span data-ttu-id="5ec08-532">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-532">The values for the integer that is returned indicate the character set according to the following table.</span></span>

| <span data-ttu-id="5ec08-533">先頭値</span><span class="sxs-lookup"><span data-stu-id="5ec08-533">Value</span></span> | <span data-ttu-id="5ec08-534">説明</span><span class="sxs-lookup"><span data-stu-id="5ec08-534">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="5ec08-535">0</span><span class="sxs-lookup"><span data-stu-id="5ec08-535">0</span></span>     | <span data-ttu-id="5ec08-536">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-536">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="5ec08-537">1</span><span class="sxs-lookup"><span data-stu-id="5ec08-537">1</span></span>     | <span data-ttu-id="5ec08-538">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-538">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="5ec08-539">2</span><span class="sxs-lookup"><span data-stu-id="5ec08-539">2</span></span>     | <span data-ttu-id="5ec08-540">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-540">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="5ec08-541">77</span><span class="sxs-lookup"><span data-stu-id="5ec08-541">77</span></span>    | <span data-ttu-id="5ec08-542">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-542">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="5ec08-543">128</span><span class="sxs-lookup"><span data-stu-id="5ec08-543">128</span></span>   | <span data-ttu-id="5ec08-544">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-544">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="5ec08-545">129</span><span class="sxs-lookup"><span data-stu-id="5ec08-545">129</span></span>   | <span data-ttu-id="5ec08-546">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-546">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="5ec08-547">134</span><span class="sxs-lookup"><span data-stu-id="5ec08-547">134</span></span>   | <span data-ttu-id="5ec08-548">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-548">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="5ec08-549">136</span><span class="sxs-lookup"><span data-stu-id="5ec08-549">136</span></span>   | <span data-ttu-id="5ec08-550">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-550">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="5ec08-551">161</span><span class="sxs-lookup"><span data-stu-id="5ec08-551">161</span></span>   | <span data-ttu-id="5ec08-552">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-552">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="5ec08-553">162</span><span class="sxs-lookup"><span data-stu-id="5ec08-553">162</span></span>   | <span data-ttu-id="5ec08-554">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-554">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="5ec08-555">163</span><span class="sxs-lookup"><span data-stu-id="5ec08-555">163</span></span>   | <span data-ttu-id="5ec08-556">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-556">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="5ec08-557">186</span><span class="sxs-lookup"><span data-stu-id="5ec08-557">186</span></span>   | <span data-ttu-id="5ec08-558">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-558">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="5ec08-559">204</span><span class="sxs-lookup"><span data-stu-id="5ec08-559">204</span></span>   | <span data-ttu-id="5ec08-560">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-560">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="5ec08-561">238</span><span class="sxs-lookup"><span data-stu-id="5ec08-561">238</span></span>   | <span data-ttu-id="5ec08-562">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-562">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="5ec08-563">255</span><span class="sxs-lookup"><span data-stu-id="5ec08-563">255</span></span>   | <span data-ttu-id="5ec08-564">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-564">OEM\_CHARSET</span></span>         |

<span data-ttu-id="5ec08-565">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-565">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="5ec08-566">金額</span><span class="sxs-lookup"><span data-stu-id="5ec08-566">Value</span></span> | <span data-ttu-id="5ec08-567">説明</span><span class="sxs-lookup"><span data-stu-id="5ec08-567">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="5ec08-568">130</span><span class="sxs-lookup"><span data-stu-id="5ec08-568">130</span></span>   | <span data-ttu-id="5ec08-569">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-569">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="5ec08-570">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-570">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="5ec08-571">先頭値</span><span class="sxs-lookup"><span data-stu-id="5ec08-571">Value</span></span> | <span data-ttu-id="5ec08-572">説明</span><span class="sxs-lookup"><span data-stu-id="5ec08-572">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="5ec08-573">177</span><span class="sxs-lookup"><span data-stu-id="5ec08-573">177</span></span>   | <span data-ttu-id="5ec08-574">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-574">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="5ec08-575">178</span><span class="sxs-lookup"><span data-stu-id="5ec08-575">178</span></span>   | <span data-ttu-id="5ec08-576">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-576">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="5ec08-577">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-577">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="5ec08-578">先頭値</span><span class="sxs-lookup"><span data-stu-id="5ec08-578">Value</span></span> | <span data-ttu-id="5ec08-579">説明</span><span class="sxs-lookup"><span data-stu-id="5ec08-579">Description</span></span>   |
|-------|---------------|
| <span data-ttu-id="5ec08-580">222</span><span class="sxs-lookup"><span data-stu-id="5ec08-580">222</span></span>   | <span data-ttu-id="5ec08-581">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="5ec08-581">THAI\_CHARSET</span></span> |

<span data-ttu-id="5ec08-582">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-582">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="5ec08-583">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-583">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="5ec08-584">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ec08-584">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-checkbox"></a><span data-ttu-id="5ec08-585">メソッド checkBox</span><span class="sxs-lookup"><span data-stu-id="5ec08-585">Method checkBox</span></span>

```xpp
public boolean checkBox([boolean value])
```

### <a name="parameters---checkbox"></a><span data-ttu-id="5ec08-586">パラメーター - checkBox</span><span class="sxs-lookup"><span data-stu-id="5ec08-586">Parameters - checkBox</span></span>

<span data-ttu-id="5ec08-587">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-587">value</span></span>  

### <a name="return-value---checkbox"></a><span data-ttu-id="5ec08-588">戻り値- checkBox</span><span class="sxs-lookup"><span data-stu-id="5ec08-588">Return Value - checkBox</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="5ec08-589">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="5ec08-589">Method colorScheme</span></span>

<span data-ttu-id="5ec08-590">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-590">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="5ec08-591">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="5ec08-591">Parameters - colorScheme</span></span>

<span data-ttu-id="5ec08-592">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-592">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="5ec08-593">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="5ec08-593">Return Value - colorScheme</span></span>

<span data-ttu-id="5ec08-594">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="5ec08-594">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="5ec08-595">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="5ec08-595">Remarks - colorScheme</span></span>

<span data-ttu-id="5ec08-596">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-596">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="5ec08-597">先頭値</span><span class="sxs-lookup"><span data-stu-id="5ec08-597">Value</span></span> | <span data-ttu-id="5ec08-598">スタイル</span><span class="sxs-lookup"><span data-stu-id="5ec08-598">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="5ec08-599">0</span><span class="sxs-lookup"><span data-stu-id="5ec08-599">0</span></span>     | <span data-ttu-id="5ec08-600">既定</span><span class="sxs-lookup"><span data-stu-id="5ec08-600">Default</span></span>               |
| <span data-ttu-id="5ec08-601">1</span><span class="sxs-lookup"><span data-stu-id="5ec08-601">1</span></span>     | <span data-ttu-id="5ec08-602">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="5ec08-602">The Windows palette</span></span>   |
| <span data-ttu-id="5ec08-603">2</span><span class="sxs-lookup"><span data-stu-id="5ec08-603">2</span></span>     | <span data-ttu-id="5ec08-604">真の配色</span><span class="sxs-lookup"><span data-stu-id="5ec08-604">The true-color scheme</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="5ec08-605">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="5ec08-605">Method configurationKey</span></span>

<span data-ttu-id="5ec08-606">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-606">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="5ec08-607">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="5ec08-607">Parameters - configurationKey</span></span>

<span data-ttu-id="5ec08-608">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-608">value</span></span>  
<span data-ttu-id="5ec08-609">コントロールに割り当てるコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="5ec08-609">The ID of the configuration key to assign to the control.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="5ec08-610">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="5ec08-610">Return Value - configurationKey</span></span>

<span data-ttu-id="5ec08-611">コントロールに割り当てられるコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="5ec08-611">The ID of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="5ec08-612">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="5ec08-612">Remarks - configurationKey</span></span>

<span data-ttu-id="5ec08-613">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-613">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="5ec08-614">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-614">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="examples---configurationkey"></a><span data-ttu-id="5ec08-615">例 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="5ec08-615">Examples - configurationKey</span></span>

<span data-ttu-id="5ec08-616">次の例は、コントロールのコンフィギュレーション キーを設定して取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-616">The following example shows how to set and retrieve the configuration key for a control.</span></span>

```xpp
DictConfigurationKey dck; 
configurationKeyId cki; 
// objCtrl previously assigned. 
// Assign a configuration key to the control. 
objCtrl.configurationKey(configurationkeynum(BankDeposit)); 
// Retrieve the configuration key ID from the control. 
cki = objCtrl.configurationKey(); 
if (cki != 0) 
{ 
    dck = new DictConfigurationKey(cki); 
    if (dck) 
    { 
    print strfmt("Configuration Key ID: %1 Configuration Key Name: %2", 
                  cki, 
                  dck.name()); 
    } 
}
```

## <a name="method-configurationkeyex"></a><span data-ttu-id="5ec08-617">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-617">Method configurationKeyEx</span></span>

<span data-ttu-id="5ec08-618">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-618">Returns a list that contains the IDs of configuration keys that are in effect for the control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="5ec08-619">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-619">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="5ec08-620">コントロールが有効になっているコンフィギュレーション キーの ID を含む一覧。</span><span class="sxs-lookup"><span data-stu-id="5ec08-620">A list that contains the IDs of configuration keys that are in effect for the control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="5ec08-621">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-621">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="5ec08-622">コントロールがデータソースにバインドされている場合、返された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-622">If the control is bound to a data source, the returned list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="5ec08-623">また、返されたリストには、プロパティ、拡張データ型、または enumType メソッドに適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-623">The returned list also contains any configuration key IDs that are applied to the properties, extended data type, or enumType methods.</span></span> <span data-ttu-id="5ec08-624">リストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-624">The list does not contain duplicate IDs.</span></span>

### <a name="examples---configurationkeyex"></a><span data-ttu-id="5ec08-625">例 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-625">Examples - configurationKeyEx</span></span>

<span data-ttu-id="5ec08-626">次の例は、コントロールのコンフィギュレーション キー ID を取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-626">The following example shows how to retrieve the configuration key IDs for a control.</span></span>

```xpp
DictConfigurationKey dck; 
configurationKeyId cki; 
List list; 
ListEnumerator enum;
// objCtrl previously assigned. 
list = objCtrl.configurationKeyEx(); 
if (0 != list.elements()) 
{ 
    enum = list.getEnumerator(); 
    while (enum.moveNext()) 
    { 
       dck = new DictConfigurationKey(enum.current()); 
       if (dck) 
       { 
        print strfmt("Configuration Key ID: %1 Configuration Key Name: %2", 
                     enum.current(), 
                     dck.name() ); 
       } 
    } 
}
```

## <a name="method-copyitem"></a><span data-ttu-id="5ec08-627">メソッド copyItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-627">Method copyItem</span></span>

```xpp
public int copyItem(int Idx, int newParent, [int insertAfter])
```

### <a name="parameters---copyitem"></a><span data-ttu-id="5ec08-628">パラメーター - copyItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-628">Parameters - copyItem</span></span>

<span data-ttu-id="5ec08-629">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-629">Idx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-630">newParent</span><span class="sxs-lookup"><span data-stu-id="5ec08-630">newParent</span></span>  

<!-- -->

<span data-ttu-id="5ec08-631">insertAfter</span><span class="sxs-lookup"><span data-stu-id="5ec08-631">insertAfter</span></span>  

### <a name="return-value---copyitem"></a><span data-ttu-id="5ec08-632">戻り値 - copyItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-632">Return Value - copyItem</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="5ec08-633">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="5ec08-633">Method countryRegionCodes</span></span>

<span data-ttu-id="5ec08-634">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-634">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="5ec08-635">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="5ec08-635">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="5ec08-636">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-636">value</span></span>  
<span data-ttu-id="5ec08-637">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-637">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="5ec08-638">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="5ec08-638">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="5ec08-639">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="5ec08-639">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-createdragimagelist"></a><span data-ttu-id="5ec08-640">メソッド createDragImagelist</span><span class="sxs-lookup"><span data-stu-id="5ec08-640">Method createDragImagelist</span></span>

```xpp
public Imagelist createDragImagelist()
```

### <a name="return-value---createdragimagelist"></a><span data-ttu-id="5ec08-641">戻り値 - createDragImagelist</span><span class="sxs-lookup"><span data-stu-id="5ec08-641">Return Value - createDragImagelist</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="5ec08-642">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="5ec08-642">Method dataRelationPath</span></span>

<span data-ttu-id="5ec08-643">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-643">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="5ec08-644">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="5ec08-644">Parameters - dataRelationPath</span></span>

<span data-ttu-id="5ec08-645">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-645">value</span></span>  
<span data-ttu-id="5ec08-646">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-646">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="5ec08-647">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="5ec08-647">Return Value - dataRelationPath</span></span>

<span data-ttu-id="5ec08-648">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="5ec08-648">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="5ec08-649">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="5ec08-649">Remarks - dataRelationPath</span></span>

<span data-ttu-id="5ec08-650">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-650">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="5ec08-651">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="5ec08-651">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-delete"></a><span data-ttu-id="5ec08-652">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="5ec08-652">Method delete</span></span>

<span data-ttu-id="5ec08-653">フォーム ツリー コントロールから指定した項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-653">Deletes the specified item from the form tree control.</span></span>

```xpp
public boolean delete(int Idx)
```

### <a name="parameters---delete"></a><span data-ttu-id="5ec08-654">パラメーター - delete</span><span class="sxs-lookup"><span data-stu-id="5ec08-654">Parameters - delete</span></span>

<span data-ttu-id="5ec08-655">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-655">Idx</span></span>  
<span data-ttu-id="5ec08-656">削除する項目のゼロベース インデックスを指定する整数。</span><span class="sxs-lookup"><span data-stu-id="5ec08-656">An integer that specifies the zero-based index of the item to delete.</span></span>

### <a name="return-value---delete"></a><span data-ttu-id="5ec08-657">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="5ec08-657">Return Value - delete</span></span>

<span data-ttu-id="5ec08-658">項目が正常に削除された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-658">true if the item was successfully deleted; otherwise, false.</span></span>

### <a name="examples---delete"></a><span data-ttu-id="5ec08-659">例 - delete</span><span class="sxs-lookup"><span data-stu-id="5ec08-659">Examples - delete</span></span>

<span data-ttu-id="5ec08-660">次の例は、フォーム ツリー コントロールの最初の項目を削除する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-660">The following example shows how to delete the first item in the form tree control.</span></span>

```xpp
// The ftc variable was a previously allocated  
// FormTreeControl variable. 
boolean bDelete; 
bDelete = ftc.delete(0);
```

## <a name="method-deleteall"></a><span data-ttu-id="5ec08-661">メソッド deleteAll</span><span class="sxs-lookup"><span data-stu-id="5ec08-661">Method deleteAll</span></span>

<span data-ttu-id="5ec08-662">フォーム ツリー コントロールからすべての項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-662">Deletes all items from the form tree control.</span></span>

```xpp
public boolean deleteAll()
```

### <a name="return-value---deleteall"></a><span data-ttu-id="5ec08-663">戻り値 - deleteAll</span><span class="sxs-lookup"><span data-stu-id="5ec08-663">Return Value - deleteAll</span></span>

<span data-ttu-id="5ec08-664">すべての項目が正常に削除された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-664">true if all items were successfully deleted; otherwise, false.</span></span>

### <a name="examples---deleteall"></a><span data-ttu-id="5ec08-665">例 - deleteAll</span><span class="sxs-lookup"><span data-stu-id="5ec08-665">Examples - deleteAll</span></span>

<span data-ttu-id="5ec08-666">次の例は、フォーム ツリー コントロールからすべての項目を削除する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-666">The following example shows how to delete all items from a form tree control.</span></span>

```xpp
// The ftc variable was a previously allocated 
// FormTreeControl variable. 
boolean bDelete; 
bDelete = ftc.deleteAll();
```

## <a name="method-displaytarget"></a><span data-ttu-id="5ec08-667">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="5ec08-667">Method displayTarget</span></span>

<span data-ttu-id="5ec08-668">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-668">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="5ec08-669">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="5ec08-669">Parameters - displayTarget</span></span>

<span data-ttu-id="5ec08-670">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-670">value</span></span>  
<span data-ttu-id="5ec08-671">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-671">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="5ec08-672">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="5ec08-672">Return Value - displayTarget</span></span>

<span data-ttu-id="5ec08-673">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-673">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="5ec08-674">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="5ec08-674">Method dragDrop</span></span>

<span data-ttu-id="5ec08-675">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-675">Determines whether drag-and-drop operations are enabled or disabled for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="5ec08-676">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="5ec08-676">Parameters - dragDrop</span></span>

<span data-ttu-id="5ec08-677">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-677">value</span></span>  
<span data-ttu-id="5ec08-678">ドラッグ アンド ドロップ動作が有効になっているかどうかを示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-678">An Integer data type that indicates whether drag-and-drop behavior is enabled.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="5ec08-679">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="5ec08-679">Return Value - dragDrop</span></span>

<span data-ttu-id="5ec08-680">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-680">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="examples---dragdrop"></a><span data-ttu-id="5ec08-681">例 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="5ec08-681">Examples - dragDrop</span></span>

<span data-ttu-id="5ec08-682">次の例は、ドラッグ アンド ドロップの動作が有効かどうかを示す値を返すか、設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-682">The following example shows how to return or set the value that indicates whether drag-and-drop behavior is enabled.</span></span>

```xpp
boolean dDragDrop; 
// The ctrl variable was previously assigned  
// as a FormTreeControl value. 
// Retrieve the drag�and�drop-enabled value. 
dDragDrop = ctrl.dragDrop(); 
// Set the drag�and�drop-enabled value. 
ctrl.dragDrop(true);
```

## <a name="method-dragover"></a><span data-ttu-id="5ec08-683">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="5ec08-683">Method dragOver</span></span>

<span data-ttu-id="5ec08-684">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOver イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-684">Raises the dragOver event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="5ec08-685">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="5ec08-685">Parameters - dragOver</span></span>

<span data-ttu-id="5ec08-686">dragSource</span><span class="sxs-lookup"><span data-stu-id="5ec08-686">dragSource</span></span>  
<span data-ttu-id="5ec08-687">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-687">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-688">dragMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-688">dragMode</span></span>  
<span data-ttu-id="5ec08-689">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-689">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-690">x</span><span class="sxs-lookup"><span data-stu-id="5ec08-690">x</span></span>  
<span data-ttu-id="5ec08-691">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-691">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-692">y</span><span class="sxs-lookup"><span data-stu-id="5ec08-692">y</span></span>  
<span data-ttu-id="5ec08-693">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-693">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="5ec08-694">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="5ec08-694">Return Value - dragOver</span></span>

<span data-ttu-id="5ec08-695">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-695">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="5ec08-696">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-696">Method dragOverEx</span></span>

<span data-ttu-id="5ec08-697">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-697">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="5ec08-698">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-698">Parameters - dragOverEx</span></span>

<span data-ttu-id="5ec08-699">dragSource</span><span class="sxs-lookup"><span data-stu-id="5ec08-699">dragSource</span></span>  
<span data-ttu-id="5ec08-700">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-700">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-701">dragMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-701">dragMode</span></span>  
<span data-ttu-id="5ec08-702">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-702">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-703">x</span><span class="sxs-lookup"><span data-stu-id="5ec08-703">x</span></span>  
<span data-ttu-id="5ec08-704">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-704">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-705">y</span><span class="sxs-lookup"><span data-stu-id="5ec08-705">y</span></span>  
<span data-ttu-id="5ec08-706">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-706">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="5ec08-707">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-707">Return Value - dragOverEx</span></span>

<span data-ttu-id="5ec08-708">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-708">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="5ec08-709">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="5ec08-709">Method dragText</span></span>

<span data-ttu-id="5ec08-710">フォーム ツリー コントロールをドラッグしたときに表示されるテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-710">Returns the text that is displayed when the form tree control is dragged.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="5ec08-711">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="5ec08-711">Return Value - dragText</span></span>

<span data-ttu-id="5ec08-712">ツリー コントロールをドラッグしたときに表示されるテキスト。ツリー コントロールがドラッグされたときに表示するテキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="5ec08-712">The text that is displayed when the tree control is dragged; an empty string if there is no text to display when the tree control is dragged.</span></span>

## <a name="method-editlabels"></a><span data-ttu-id="5ec08-713">メソッド editLabels</span><span class="sxs-lookup"><span data-stu-id="5ec08-713">Method editLabels</span></span>

```xpp
public boolean editLabels([boolean value])
```

### <a name="parameters---editlabels"></a><span data-ttu-id="5ec08-714">パラメーター - editLabels</span><span class="sxs-lookup"><span data-stu-id="5ec08-714">Parameters - editLabels</span></span>

<span data-ttu-id="5ec08-715">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-715">value</span></span>  

### <a name="return-value---editlabels"></a><span data-ttu-id="5ec08-716">戻り値 - editLabels</span><span class="sxs-lookup"><span data-stu-id="5ec08-716">Return Value - editLabels</span></span>

## <a name="method-enabled"></a><span data-ttu-id="5ec08-717">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="5ec08-717">Method enabled</span></span>

<span data-ttu-id="5ec08-718">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-718">Determines whether the object is enabled or disabled.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="5ec08-719">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="5ec08-719">Parameters - enabled</span></span>

<span data-ttu-id="5ec08-720">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-720">value</span></span>  
<span data-ttu-id="5ec08-721">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-721">A Boolean value that specifies whether the control is enabled.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="5ec08-722">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="5ec08-722">Return Value - enabled</span></span>

<span data-ttu-id="5ec08-723">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-723">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="5ec08-724">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="5ec08-724">Remarks - enabled</span></span>

<span data-ttu-id="5ec08-725">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-725">The enabled property lets you enable or disable controls at run time.</span></span> <span data-ttu-id="5ec08-726">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-726">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="5ec08-727">また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-727">You can also disable a control that is used only for display purposes, such as an error message that provides read-only information.</span></span>

### <a name="examples---enabled"></a><span data-ttu-id="5ec08-728">例 - enabled</span><span class="sxs-lookup"><span data-stu-id="5ec08-728">Examples - enabled</span></span>

<span data-ttu-id="5ec08-729">次の例は、コントロールの有効なプロパティを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-729">The following example shows how to return and set the enabled property for a control.</span></span>

```xpp
// Return the value of the enabled property. 
info(strfmt("enabled: %1",this.enabled())); 
// Set the enabled property. 
this.enabled(false);
```

## <a name="method-expand"></a><span data-ttu-id="5ec08-730">メソッド expand</span><span class="sxs-lookup"><span data-stu-id="5ec08-730">Method expand</span></span>

```xpp
public int expand(int Idx, [FormTreeExpand action])
```

### <a name="parameters---expand"></a><span data-ttu-id="5ec08-731">パラメーター - expand</span><span class="sxs-lookup"><span data-stu-id="5ec08-731">Parameters - expand</span></span>

<span data-ttu-id="5ec08-732">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-732">Idx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-733">アクション</span><span class="sxs-lookup"><span data-stu-id="5ec08-733">action</span></span>  

### <a name="return-value---expand"></a><span data-ttu-id="5ec08-734">戻り値 - expand</span><span class="sxs-lookup"><span data-stu-id="5ec08-734">Return Value - expand</span></span>

## <a name="method-expanding"></a><span data-ttu-id="5ec08-735">メソッド expanding</span><span class="sxs-lookup"><span data-stu-id="5ec08-735">Method expanding</span></span>

```xpp
public boolean expanding(int Idx, FormTreeExpand action, AnyType data)
```

### <a name="parameters---expanding"></a><span data-ttu-id="5ec08-736">パラメーター - expanding</span><span class="sxs-lookup"><span data-stu-id="5ec08-736">Parameters - expanding</span></span>

<span data-ttu-id="5ec08-737">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-737">Idx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-738">アクション</span><span class="sxs-lookup"><span data-stu-id="5ec08-738">action</span></span>  

<!-- -->

<span data-ttu-id="5ec08-739">データ</span><span class="sxs-lookup"><span data-stu-id="5ec08-739">data</span></span>  

### <a name="return-value---expanding"></a><span data-ttu-id="5ec08-740">戻り値 - expanding</span><span class="sxs-lookup"><span data-stu-id="5ec08-740">Return Value - expanding</span></span>

## <a name="method-font"></a><span data-ttu-id="5ec08-741">戻り値 - expand</span><span class="sxs-lookup"><span data-stu-id="5ec08-741">Method font</span></span>

<span data-ttu-id="5ec08-742">コントロール内のテキストに使用されるフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-742">Gets or sets the name of the font that is used for the text in the control.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="5ec08-743">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="5ec08-743">Parameters - font</span></span>

<span data-ttu-id="5ec08-744">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-744">value</span></span>  
<span data-ttu-id="5ec08-745">フォーム ツリー コントロールのテキストに使用するフォントを示す文字列値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-745">A string value that indicates the font to use for the text in a form tree control.</span></span>

### <a name="return-value---font"></a><span data-ttu-id="5ec08-746">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="5ec08-746">Return Value - font</span></span>

<span data-ttu-id="5ec08-747">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="5ec08-747">The name of the font to use, such as Tahoma or Verdana.</span></span>

### <a name="examples---font"></a><span data-ttu-id="5ec08-748">例 - font</span><span class="sxs-lookup"><span data-stu-id="5ec08-748">Examples - font</span></span>

<span data-ttu-id="5ec08-749">次の例は、フォーム ツリー コントロールのフォントを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-749">The following example shows how to return and set the font for a form tree control.</span></span>

```xpp
str strFont; 
// The ctrl variable was previously assigned  
// as a form tree control variable. 
// Retrieve the font. 
strFont = ctrl.font(); 
// Set the font. 
ctrl.font("Times New Roman");
```

## <a name="method-fontsize"></a><span data-ttu-id="5ec08-750">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="5ec08-750">Method fontSize</span></span>

<span data-ttu-id="5ec08-751">コントロール内のテキストに使用されるフォント サイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-751">Gets or sets the font size that is used for the text in the control.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="5ec08-752">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="5ec08-752">Parameters - fontSize</span></span>

<span data-ttu-id="5ec08-753">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-753">value</span></span>  
<span data-ttu-id="5ec08-754">フォーム ツリー コントロール内のテキストのフォント サイズ、ポイントを示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-754">An Integer data type that indicates the font size, in points, for the text in a form tree control.</span></span>

### <a name="return-value---fontsize"></a><span data-ttu-id="5ec08-755">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="5ec08-755">Return Value - fontSize</span></span>

<span data-ttu-id="5ec08-756">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="5ec08-756">The height of the font in points.</span></span>

### <a name="examples---fontsize"></a><span data-ttu-id="5ec08-757">例 - fontSize</span><span class="sxs-lookup"><span data-stu-id="5ec08-757">Examples - fontSize</span></span>

<span data-ttu-id="5ec08-758">次の例は、コントロールのフォント サイズを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-758">The following example shows how to return and set the font size for a control.</span></span>

```xpp
int nSize; 
// The ctrl variable was previously assigned  
// as a form tree control. 
// Retrieve the font size. 
nSize = ctrl.fontSize(); 
// Set the font size. 
ctrl.fontSize(16);
```

## <a name="method-foregroundcolor"></a><span data-ttu-id="5ec08-759">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="5ec08-759">Method foregroundColor</span></span>

<span data-ttu-id="5ec08-760">コントロール内のテキストに使用される色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-760">Gets or sets the color that is used for the text in the control.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="5ec08-761">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="5ec08-761">Parameters - foregroundColor</span></span>

<span data-ttu-id="5ec08-762">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-762">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="5ec08-763">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="5ec08-763">Return Value - foregroundColor</span></span>

<span data-ttu-id="5ec08-764">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="5ec08-764">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="5ec08-765">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="5ec08-765">Remarks - foregroundColor</span></span>

<span data-ttu-id="5ec08-766">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-766">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="5ec08-767">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-767">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="5ec08-768">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-768">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="5ec08-769">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-769">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="5ec08-770">上位バイトは 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-770">The high-order byte must be 0 (zero).</span></span>
-   <span data-ttu-id="5ec08-771">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-771">The maximum value for a single byte is 255.</span></span>

## <a name="method-getchild"></a><span data-ttu-id="5ec08-772">メソッド getChild</span><span class="sxs-lookup"><span data-stu-id="5ec08-772">Method getChild</span></span>

```xpp
public int getChild(int Idx)
```

### <a name="parameters---getchild"></a><span data-ttu-id="5ec08-773">パラメーター - getChild</span><span class="sxs-lookup"><span data-stu-id="5ec08-773">Parameters - getChild</span></span>

<span data-ttu-id="5ec08-774">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-774">Idx</span></span>  

### <a name="return-value---getchild"></a><span data-ttu-id="5ec08-775">戻り値 - getChild</span><span class="sxs-lookup"><span data-stu-id="5ec08-775">Return Value - getChild</span></span>

## <a name="method-getfirstselected"></a><span data-ttu-id="5ec08-776">メソッド getFirstSelected</span><span class="sxs-lookup"><span data-stu-id="5ec08-776">Method getFirstSelected</span></span>

```xpp
public int getFirstSelected()
```

### <a name="return-value---getfirstselected"></a><span data-ttu-id="5ec08-777">戻り値 - getFirstSelected</span><span class="sxs-lookup"><span data-stu-id="5ec08-777">Return Value - getFirstSelected</span></span>

## <a name="method-getfirstvisible"></a><span data-ttu-id="5ec08-778">メソッド getFirstVisible</span><span class="sxs-lookup"><span data-stu-id="5ec08-778">Method getFirstVisible</span></span>

```xpp
public int getFirstVisible()
```

### <a name="return-value---getfirstvisible"></a><span data-ttu-id="5ec08-779">戻り値 - getFirstVisible</span><span class="sxs-lookup"><span data-stu-id="5ec08-779">Return Value - getFirstVisible</span></span>

## <a name="method-getimagelist"></a><span data-ttu-id="5ec08-780">メソッド getImagelist</span><span class="sxs-lookup"><span data-stu-id="5ec08-780">Method getImagelist</span></span>

```xpp
public Imagelist getImagelist()
```

### <a name="return-value---getimagelist"></a><span data-ttu-id="5ec08-781">戻り値 - getImagelist</span><span class="sxs-lookup"><span data-stu-id="5ec08-781">Return Value - getImagelist</span></span>

## <a name="method-getitem"></a><span data-ttu-id="5ec08-782">メソッド getItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-782">Method getItem</span></span>

```xpp
public FormTreeItem getItem(int Idx)
```

### <a name="parameters---getitem"></a><span data-ttu-id="5ec08-783">パラメーター - getItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-783">Parameters - getItem</span></span>

<span data-ttu-id="5ec08-784">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-784">Idx</span></span>  

### <a name="return-value---getitem"></a><span data-ttu-id="5ec08-785">戻り値 - getItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-785">Return Value - getItem</span></span>

## <a name="method-getnextselected"></a><span data-ttu-id="5ec08-786">メソッド getNextSelected</span><span class="sxs-lookup"><span data-stu-id="5ec08-786">Method getNextSelected</span></span>

```xpp
public int getNextSelected(int idx)
```

### <a name="parameters---getnextselected"></a><span data-ttu-id="5ec08-787">パラメーター - getNextSelected</span><span class="sxs-lookup"><span data-stu-id="5ec08-787">Parameters - getNextSelected</span></span>

<span data-ttu-id="5ec08-788">idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-788">idx</span></span>  

### <a name="return-value---getnextselected"></a><span data-ttu-id="5ec08-789">戻り値 - getNextSelected</span><span class="sxs-lookup"><span data-stu-id="5ec08-789">Return Value - getNextSelected</span></span>

## <a name="method-getnextsibling"></a><span data-ttu-id="5ec08-790">メソッド getNextSibling</span><span class="sxs-lookup"><span data-stu-id="5ec08-790">Method getNextSibling</span></span>

```xpp
public int getNextSibling(int Idx)
```

### <a name="parameters---getnextsibling"></a><span data-ttu-id="5ec08-791">パラメーター - getNextSibling</span><span class="sxs-lookup"><span data-stu-id="5ec08-791">Parameters - getNextSibling</span></span>

<span data-ttu-id="5ec08-792">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-792">Idx</span></span>  

### <a name="return-value---getnextsibling"></a><span data-ttu-id="5ec08-793">戻り値 - getNextSibling</span><span class="sxs-lookup"><span data-stu-id="5ec08-793">Return Value - getNextSibling</span></span>

## <a name="method-getnextvisible"></a><span data-ttu-id="5ec08-794">メソッド getNextVisible</span><span class="sxs-lookup"><span data-stu-id="5ec08-794">Method getNextVisible</span></span>

```xpp
public int getNextVisible(int Idx)
```

### <a name="parameters---getnextvisible"></a><span data-ttu-id="5ec08-795">パラメーター - getNextVisible</span><span class="sxs-lookup"><span data-stu-id="5ec08-795">Parameters - getNextVisible</span></span>

<span data-ttu-id="5ec08-796">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-796">Idx</span></span>  

### <a name="return-value---getnextvisible"></a><span data-ttu-id="5ec08-797">戻り値 - getNextVisible</span><span class="sxs-lookup"><span data-stu-id="5ec08-797">Return Value - getNextVisible</span></span>

## <a name="method-getparent"></a><span data-ttu-id="5ec08-798">メソッド getParent</span><span class="sxs-lookup"><span data-stu-id="5ec08-798">Method getParent</span></span>

```xpp
public int getParent(int Idx)
```

### <a name="parameters---getparent"></a><span data-ttu-id="5ec08-799">パラメーター - getParent</span><span class="sxs-lookup"><span data-stu-id="5ec08-799">Parameters - getParent</span></span>

<span data-ttu-id="5ec08-800">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-800">Idx</span></span>  

### <a name="return-value---getparent"></a><span data-ttu-id="5ec08-801">戻り値 - getParent</span><span class="sxs-lookup"><span data-stu-id="5ec08-801">Return Value - getParent</span></span>

## <a name="method-getprevselected"></a><span data-ttu-id="5ec08-802">メソッド getPrevSelected</span><span class="sxs-lookup"><span data-stu-id="5ec08-802">Method getPrevSelected</span></span>

```xpp
public int getPrevSelected(int idx)
```

### <a name="parameters---getprevselected"></a><span data-ttu-id="5ec08-803">パラメーター - getPrevSelected</span><span class="sxs-lookup"><span data-stu-id="5ec08-803">Parameters - getPrevSelected</span></span>

<span data-ttu-id="5ec08-804">idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-804">idx</span></span>  

### <a name="return-value---getprevselected"></a><span data-ttu-id="5ec08-805">戻り値 - getPrevSelected</span><span class="sxs-lookup"><span data-stu-id="5ec08-805">Return Value - getPrevSelected</span></span>

## <a name="method-getprevsibling"></a><span data-ttu-id="5ec08-806">メソッド getPrevSibling</span><span class="sxs-lookup"><span data-stu-id="5ec08-806">Method getPrevSibling</span></span>

```xpp
public int getPrevSibling(int Idx)
```

### <a name="parameters---getprevsibling"></a><span data-ttu-id="5ec08-807">パラメーター - getPrevSibling</span><span class="sxs-lookup"><span data-stu-id="5ec08-807">Parameters - getPrevSibling</span></span>

<span data-ttu-id="5ec08-808">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-808">Idx</span></span>  

### <a name="return-value---getprevsibling"></a><span data-ttu-id="5ec08-809">戻り値 - getPrevSibling</span><span class="sxs-lookup"><span data-stu-id="5ec08-809">Return Value - getPrevSibling</span></span>

## <a name="method-getprevvisible"></a><span data-ttu-id="5ec08-810">メソッド getPrevVisible</span><span class="sxs-lookup"><span data-stu-id="5ec08-810">Method getPrevVisible</span></span>

```xpp
public int getPrevVisible(int Idx)
```

### <a name="parameters---getprevvisible"></a><span data-ttu-id="5ec08-811">パラメーター - getPrevVisible</span><span class="sxs-lookup"><span data-stu-id="5ec08-811">Parameters - getPrevVisible</span></span>

<span data-ttu-id="5ec08-812">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-812">Idx</span></span>  

### <a name="return-value---getprevvisible"></a><span data-ttu-id="5ec08-813">戻り値 - getPrevVisible</span><span class="sxs-lookup"><span data-stu-id="5ec08-813">Return Value - getPrevVisible</span></span>

## <a name="method-getroot"></a><span data-ttu-id="5ec08-814">メソッド getRoot</span><span class="sxs-lookup"><span data-stu-id="5ec08-814">Method getRoot</span></span>

```xpp
public int getRoot()
```

### <a name="return-value---getroot"></a><span data-ttu-id="5ec08-815">戻り値 - getRoot</span><span class="sxs-lookup"><span data-stu-id="5ec08-815">Return Value - getRoot</span></span>

## <a name="method-getselectedcount"></a><span data-ttu-id="5ec08-816">メソッド getSelectedCount</span><span class="sxs-lookup"><span data-stu-id="5ec08-816">Method getSelectedCount</span></span>

```xpp
public int getSelectedCount()
```

### <a name="return-value---getselectedcount"></a><span data-ttu-id="5ec08-817">戻り値 - getSelectedCount</span><span class="sxs-lookup"><span data-stu-id="5ec08-817">Return Value - getSelectedCount</span></span>

## <a name="method-getselection"></a><span data-ttu-id="5ec08-818">メソッド getSelection</span><span class="sxs-lookup"><span data-stu-id="5ec08-818">Method getSelection</span></span>

```xpp
public int getSelection()
```

### <a name="return-value---getselection"></a><span data-ttu-id="5ec08-819">戻り値 - getSelection</span><span class="sxs-lookup"><span data-stu-id="5ec08-819">Return Value - getSelection</span></span>

## <a name="method-getstateimagelist"></a><span data-ttu-id="5ec08-820">メソッド getStateImagelist</span><span class="sxs-lookup"><span data-stu-id="5ec08-820">Method getStateImagelist</span></span>

```xpp
public Imagelist getStateImagelist()
```

### <a name="return-value---getstateimagelist"></a><span data-ttu-id="5ec08-821">戻り値 - getStateImagelist</span><span class="sxs-lookup"><span data-stu-id="5ec08-821">Return Value - getStateImagelist</span></span>

## <a name="method-getvisiblecount"></a><span data-ttu-id="5ec08-822">メソッド getVisibleCount</span><span class="sxs-lookup"><span data-stu-id="5ec08-822">Method getVisibleCount</span></span>

<span data-ttu-id="5ec08-823">ツリー コントロール内の表示されている項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-823">Returns the number of visible items in the tree control.</span></span>

```xpp
public int getVisibleCount()
```

### <a name="return-value---getvisiblecount"></a><span data-ttu-id="5ec08-824">戻り値 - getVisibleCount</span><span class="sxs-lookup"><span data-stu-id="5ec08-824">Return Value - getVisibleCount</span></span>

<span data-ttu-id="5ec08-825">ツリー コントロール内の表示されている項目の数。</span><span class="sxs-lookup"><span data-stu-id="5ec08-825">The number of visible items in the tree control.</span></span>

### <a name="examples---getvisiblecount"></a><span data-ttu-id="5ec08-826">例 - getVisibleCount</span><span class="sxs-lookup"><span data-stu-id="5ec08-826">Examples - getVisibleCount</span></span>

<span data-ttu-id="5ec08-827">次の例は、ツリー コントロール内の表示される項目の数を取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-827">The following example shows how to retrieve the number of visible items in the tree control.</span></span>

```xpp
int nCount; 
nCount = this.getVisibleCount(); 
info (strfmt("getVisibleCount: %1", int2str(nCount)));
```

## <a name="method-hasbuttons"></a><span data-ttu-id="5ec08-828">メソッド hasButtons</span><span class="sxs-lookup"><span data-stu-id="5ec08-828">Method hasButtons</span></span>

<span data-ttu-id="5ec08-829">ツリー コントロールが展開/折り畳みボタンを表示するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-829">Returns a value that indicates whether the tree control uses expand/collapse buttons.</span></span>

```xpp
public boolean hasButtons([boolean value])
```

### <a name="parameters---hasbuttons"></a><span data-ttu-id="5ec08-830">パラメーター - hasButtons</span><span class="sxs-lookup"><span data-stu-id="5ec08-830">Parameters - hasButtons</span></span>

<span data-ttu-id="5ec08-831">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-831">value</span></span>  

### <a name="return-value---hasbuttons"></a><span data-ttu-id="5ec08-832">戻り値 - hasButtons</span><span class="sxs-lookup"><span data-stu-id="5ec08-832">Return Value - hasButtons</span></span>

<span data-ttu-id="5ec08-833">ツリー コントロールが展開/折りたたみボタンを使用する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-833">true if the tree control uses expand/collapse buttons; otherwise, false.</span></span>

### <a name="examples---hasbuttons"></a><span data-ttu-id="5ec08-834">例 - hasButtons</span><span class="sxs-lookup"><span data-stu-id="5ec08-834">Examples - hasButtons</span></span>

<span data-ttu-id="5ec08-835">次の例は、ツリー コントロールが展開/折りたたみボタンを使用するかどうかを示す値を取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-835">The following example shows how to retrieve the value that indicates whether the tree control uses expand/collapse buttons.</span></span>

```xpp
boolean bHasButtons; 
// Retrieve the value. 
bHasButtons = this.hasButtons(); 
info (strfmt("hasButtons: %1",bHasButtons)); 
// Set the value. 
this.hasButtons(false);
```

## <a name="method-haschanged"></a><span data-ttu-id="5ec08-836">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="5ec08-836">Method hasChanged</span></span>

<span data-ttu-id="5ec08-837">ツリー コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-837">Sets or returns a value that indicates whether the contents of the tree control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="5ec08-838">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="5ec08-838">Parameters - hasChanged</span></span>

<span data-ttu-id="5ec08-839">val</span><span class="sxs-lookup"><span data-stu-id="5ec08-839">val</span></span>  
<span data-ttu-id="5ec08-840">ツリー コントロールの hasChanged 値として割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-840">The value to assign as the hasChanged value for the tree control.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="5ec08-841">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="5ec08-841">Return Value - hasChanged</span></span>

<span data-ttu-id="5ec08-842">ツリー コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-842">true if the contents of the tree control have changed; otherwise, false.</span></span>

### <a name="examples---haschanged"></a><span data-ttu-id="5ec08-843">例 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="5ec08-843">Examples - hasChanged</span></span>

<span data-ttu-id="5ec08-844">次の例は、ツリー コントロールの内容が変更されたかどうかを示す値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-844">The following example shows how to return and set the value that indicates whether the contents of the tree control have changed.</span></span>

```xpp
boolean bHasChanged; 
// The ctrl variable was previously assigned 
// as a FormTreeControl variable. 
// Retrieve the hasChanged value. 
bHasChanged = ctrl.hasChanged(); 
// Modify the hasChanged value. 
ctrl.hasChanged(true);
```

## <a name="method-haslines"></a><span data-ttu-id="5ec08-845">メソッド hasLines</span><span class="sxs-lookup"><span data-stu-id="5ec08-845">Method hasLines</span></span>

<span data-ttu-id="5ec08-846">ツリー コントロールがツリー コネクタ明細行を表示するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-846">Returns a value that indicates whether the tree control displays tree connector lines.</span></span>

```xpp
public boolean hasLines([boolean value])
```

### <a name="parameters---haslines"></a><span data-ttu-id="5ec08-847">パラメーター - hasLines</span><span class="sxs-lookup"><span data-stu-id="5ec08-847">Parameters - hasLines</span></span>

<span data-ttu-id="5ec08-848">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-848">value</span></span>  

### <a name="return-value---haslines"></a><span data-ttu-id="5ec08-849">戻り値 - hasLines</span><span class="sxs-lookup"><span data-stu-id="5ec08-849">Return Value - hasLines</span></span>

<span data-ttu-id="5ec08-850">ツリー コントロールにツリー コネクタ行が表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-850">true if the tree control displays tree connector lines; otherwise, false.</span></span>

### <a name="examples---haslines"></a><span data-ttu-id="5ec08-851">例 - hasLines</span><span class="sxs-lookup"><span data-stu-id="5ec08-851">Examples - hasLines</span></span>

<span data-ttu-id="5ec08-852">次の例は、ツリー コントロールがツリー コネクタ ラインを表示するかどうかを示す値を取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-852">The following example shows how to retrieve the value that indicates whether the tree control displays tree connector lines.</span></span>

```xpp
boolean bHasLines; 
// Retrieve the value. 
bHasLines = this.hasLines(); 
info (strfmt("hasLines: %1", bHasLines)); 
// Set the value. 
this.hasLines(false);
```

## <a name="method-hasusersetting"></a><span data-ttu-id="5ec08-853">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="5ec08-853">Method hasUserSetting</span></span>

<span data-ttu-id="5ec08-854">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-854">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="5ec08-855">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="5ec08-855">Return Value - hasUserSetting</span></span>

<span data-ttu-id="5ec08-856">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-856">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-height"></a><span data-ttu-id="5ec08-857">メソッド height</span><span class="sxs-lookup"><span data-stu-id="5ec08-857">Method height</span></span>

<span data-ttu-id="5ec08-858">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-858">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="5ec08-859">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="5ec08-859">Parameters - height</span></span>

<span data-ttu-id="5ec08-860">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-860">value</span></span>  
<span data-ttu-id="5ec08-861">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="5ec08-861">An Integer data type that indicates how the height is calculated; optional.</span></span> <span data-ttu-id="5ec08-862">これは、次のいずれかの値になります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-862">This can be one of the following values:</span></span>

<!-- -->

<span data-ttu-id="5ec08-863">モード</span><span class="sxs-lookup"><span data-stu-id="5ec08-863">mode</span></span>  
<span data-ttu-id="5ec08-864">高さの計算方法を示す整数データ型です。オプションです。</span><span class="sxs-lookup"><span data-stu-id="5ec08-864">An Integer data type that indicates how the height is calculated; optional.</span></span> <span data-ttu-id="5ec08-865">これは、次のいずれかの値になります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-865">This can be one of the following values:</span></span>

### <a name="return-value---height"></a><span data-ttu-id="5ec08-866">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="5ec08-866">Return Value - height</span></span>

<span data-ttu-id="5ec08-867">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="5ec08-867">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="5ec08-868">備考 - height</span><span class="sxs-lookup"><span data-stu-id="5ec08-868">Remarks - height</span></span>

<span data-ttu-id="5ec08-869">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-869">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="5ec08-870">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-870">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="5ec08-871">モード</span><span class="sxs-lookup"><span data-stu-id="5ec08-871">Mode</span></span>              | <span data-ttu-id="5ec08-872">高さの計算</span><span class="sxs-lookup"><span data-stu-id="5ec08-872">Height calculation</span></span>                                                                         |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec08-873">-1 � 正確</span><span class="sxs-lookup"><span data-stu-id="5ec08-873">-1 � Exact</span></span>        | <span data-ttu-id="5ec08-874">ピクセル単位のコントロールの正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-874">The exact height of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="5ec08-875">0 � 自動</span><span class="sxs-lookup"><span data-stu-id="5ec08-875">0 � Auto</span></span>          | <span data-ttu-id="5ec08-876">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-876">The height of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="5ec08-877">1 � 列の高さ</span><span class="sxs-lookup"><span data-stu-id="5ec08-877">1 � Column height</span></span> | <span data-ttu-id="5ec08-878">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-878">The layout of the form determines the height of the control.</span></span>                               |

<span data-ttu-id="5ec08-879">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-879">The height and the height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="5ec08-880">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-880">Method heightMode</span></span>

<span data-ttu-id="5ec08-881">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-881">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="5ec08-882">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-882">Parameters - heightMode</span></span>

<span data-ttu-id="5ec08-883">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-883">value</span></span>  
<span data-ttu-id="5ec08-884">コントロールの高さの計算方法を示す整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-884">An Integer data type value that indicates how the height of the control is calculated.</span></span> <span data-ttu-id="5ec08-885">この値は、 Exact モードの場合は -1、Auto モードの場合は 0、Column height モードの場合は 1 になります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-885">This value can be -1 for Exact mode, 0 for Auto mode, or 1 for Column height mode.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="5ec08-886">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-886">Return Value - heightMode</span></span>

<span data-ttu-id="5ec08-887">高さ計算モード。</span><span class="sxs-lookup"><span data-stu-id="5ec08-887">The height calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="5ec08-888">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-888">Remarks - heightMode</span></span>

<span data-ttu-id="5ec08-889">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-889">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="5ec08-890">モード</span><span class="sxs-lookup"><span data-stu-id="5ec08-890">Mode</span></span>          | <span data-ttu-id="5ec08-891">高さの計算</span><span class="sxs-lookup"><span data-stu-id="5ec08-891">Height calculation</span></span>                                                                         |
|---------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec08-892">正確</span><span class="sxs-lookup"><span data-stu-id="5ec08-892">Exact</span></span>         | <span data-ttu-id="5ec08-893">ピクセル単位のコントロールの正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-893">The exact height of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="5ec08-894">自動</span><span class="sxs-lookup"><span data-stu-id="5ec08-894">Auto</span></span>          | <span data-ttu-id="5ec08-895">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-895">The height of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="5ec08-896">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="5ec08-896">Column height</span></span> | <span data-ttu-id="5ec08-897">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-897">The layout of the form determines the height of the control.</span></span>                               |

<span data-ttu-id="5ec08-898">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-898">The height of the control might change when the calculation mode is set to Auto or Column height.</span></span>

### <a name="examples---heightmode"></a><span data-ttu-id="5ec08-899">例 - heightMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-899">Examples - heightMode</span></span>

<span data-ttu-id="5ec08-900">次の例は、ツリー コントロールの高さ計算モードを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-900">The following example shows how to return and set the height calculation mode for a form tree control.</span></span>

```xpp
int nHeightMode; 
; 
// The ctrl variable was previously assigned 
// as a form tree control variable. 
// Retrieve the height mode. 
nHeightMode = ctrl.HeightMode(); 
// Set the height mode. 
ctrl.heightMode(-1); 
// Set the height. 
ctrl.heightValue(160);
```

## <a name="method-heightvalue"></a><span data-ttu-id="5ec08-901">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-901">Method heightValue</span></span>

<span data-ttu-id="5ec08-902">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-902">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="5ec08-903">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-903">Parameters - heightValue</span></span>

<span data-ttu-id="5ec08-904">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-904">value</span></span>  
<span data-ttu-id="5ec08-905">高さをピクセル単位で指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-905">An Integer data type that specifies the height in pixels.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="5ec08-906">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-906">Return Value - heightValue</span></span>

<span data-ttu-id="5ec08-907">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="5ec08-907">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="5ec08-908">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-908">Remarks - heightValue</span></span>

<span data-ttu-id="5ec08-909">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-909">The height of the control is not changed unless the Exact height calculation mode is used.</span></span>

### <a name="examples---heightvalue"></a><span data-ttu-id="5ec08-910">例 - heightValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-910">Examples - heightValue</span></span>

<span data-ttu-id="5ec08-911">次の例は、フォーム ツリー コントロールの高さの値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-911">The following example shows how to return and set the height value of a form tree control.</span></span>

```xpp
int nHeightValue; 
// The ctrl variable was previously assigned 
// as a form tree control variable. 
// Retrieve the height value. 
nHeightValue = ctrl.heightValue(); 
// Set the height value. 
ctrl.heightMode(-1); 
ctrl.heightValue(160);
```

## <a name="method-helpfield"></a><span data-ttu-id="5ec08-912">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="5ec08-912">Method helpField</span></span>

<span data-ttu-id="5ec08-913">コントロールのヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-913">Returns the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="5ec08-914">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="5ec08-914">Return Value - helpField</span></span>

<span data-ttu-id="5ec08-915">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="5ec08-915">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="5ec08-916">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="5ec08-916">Remarks - helpField</span></span>

<span data-ttu-id="5ec08-917">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-917">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="5ec08-918">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-918">Use the helpText method to set the value of the Help text.</span></span>

### <a name="examples---helpfield"></a><span data-ttu-id="5ec08-919">例 - helpField</span><span class="sxs-lookup"><span data-stu-id="5ec08-919">Examples - helpField</span></span>

<span data-ttu-id="5ec08-920">次の例は、helpField メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-920">The following example shows how to use the helpField method.</span></span>

```xpp
str strHelp; 
strHelp = this.helpField();
```

## <a name="method-helptext"></a><span data-ttu-id="5ec08-921">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="5ec08-921">Method helpText</span></span>

<span data-ttu-id="5ec08-922">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-922">Gets or sets the Help text that is displayed at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="5ec08-923">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="5ec08-923">Parameters - helpText</span></span>

<span data-ttu-id="5ec08-924">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-924">value</span></span>  
<span data-ttu-id="5ec08-925">コントロールのヘルプ テキストとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-925">The value to assign as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="5ec08-926">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="5ec08-926">Return Value - helpText</span></span>

<span data-ttu-id="5ec08-927">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="5ec08-927">The string that is displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="5ec08-928">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="5ec08-928">Remarks - helpText</span></span>

<span data-ttu-id="5ec08-929">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-929">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="5ec08-930">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-930">The Help text must not exceed 250 characters.</span></span>

### <a name="examples---helptext"></a><span data-ttu-id="5ec08-931">例 - helpText</span><span class="sxs-lookup"><span data-stu-id="5ec08-931">Examples - helpText</span></span>

<span data-ttu-id="5ec08-932">次の例は、コントロールのヘルプ テキストを設定して返す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-932">The following example shows how to set and return the Help text for a control.</span></span>

```xpp
// objCtrl previously assigned to a control 
// Retrieve existing Help text. 
print objCtrl.helpText(); 
// Specify new Help text. 
objCtrl.helpText("My new Help text");
```

## <a name="method-hierarchyparent"></a><span data-ttu-id="5ec08-933">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="5ec08-933">Method hierarchyParent</span></span>

<span data-ttu-id="5ec08-934">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-934">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="5ec08-935">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="5ec08-935">Parameters - hierarchyParent</span></span>

<span data-ttu-id="5ec08-936">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-936">value</span></span>  
<span data-ttu-id="5ec08-937">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-937">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="5ec08-938">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="5ec08-938">Return Value - hierarchyParent</span></span>

<span data-ttu-id="5ec08-939">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-939">The HierarchyParent property value of the control.</span></span>

## <a name="method-hittest"></a><span data-ttu-id="5ec08-940">メソッド hitTest</span><span class="sxs-lookup"><span data-stu-id="5ec08-940">Method hitTest</span></span>

```xpp
public container hitTest(int x, int y)
```

### <a name="parameters---hittest"></a><span data-ttu-id="5ec08-941">パラメーター - hitTest</span><span class="sxs-lookup"><span data-stu-id="5ec08-941">Parameters - hitTest</span></span>

<span data-ttu-id="5ec08-942">x</span><span class="sxs-lookup"><span data-stu-id="5ec08-942">x</span></span>  

<!-- -->

<span data-ttu-id="5ec08-943">y</span><span class="sxs-lookup"><span data-stu-id="5ec08-943">y</span></span>  

### <a name="return-value---hittest"></a><span data-ttu-id="5ec08-944">戻り値 - hitTest</span><span class="sxs-lookup"><span data-stu-id="5ec08-944">Return Value - hitTest</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="5ec08-945">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="5ec08-945">Method hWnd</span></span>

<span data-ttu-id="5ec08-946">コントロールの Windows ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-946">Returns the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="5ec08-947">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="5ec08-947">Return Value - hWnd</span></span>

<span data-ttu-id="5ec08-948">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="5ec08-948">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="5ec08-949">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="5ec08-949">Remarks - hWnd</span></span>

<span data-ttu-id="5ec08-950">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-950">The handle can be used with the Windows API.</span></span>

### <a name="examples---hwnd"></a><span data-ttu-id="5ec08-951">例 - hWnd</span><span class="sxs-lookup"><span data-stu-id="5ec08-951">Examples - hWnd</span></span>

<span data-ttu-id="5ec08-952">次の例は、コントロールの Windows ハンドルを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-952">The following example shows how to retrieve the Windows handle for a control.</span></span>

```xpp
int h; 
h = this.hWnd(); 
info (strfmt("hWnd: %1", h));
```

## <a name="method-iscontainer"></a><span data-ttu-id="5ec08-953">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="5ec08-953">Method isContainer</span></span>

<span data-ttu-id="5ec08-954">コントロールがコンテナーかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-954">Returns a value that indicates whether the control is a container.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="5ec08-955">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="5ec08-955">Return Value - isContainer</span></span>

<span data-ttu-id="5ec08-956">コントロールがコンテナーである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-956">true if the control is a container; otherwise false.</span></span>

### <a name="examples---iscontainer"></a><span data-ttu-id="5ec08-957">例 - isContainer</span><span class="sxs-lookup"><span data-stu-id="5ec08-957">Examples - isContainer</span></span>

<span data-ttu-id="5ec08-958">次の例は、コントロールがコンテナーであるかどうかを判断する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-958">The following example shows how to determine whether a control is a container.</span></span>

```xpp
info(strfmt("IsContainer: %1", this.isContainer()));
```

## <a name="method-isdisplayed"></a><span data-ttu-id="5ec08-959">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="5ec08-959">Method isDisplayed</span></span>

<span data-ttu-id="5ec08-960">コントロールが表示されるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-960">Returns a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="5ec08-961">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="5ec08-961">Return Value - isDisplayed</span></span>

<span data-ttu-id="5ec08-962">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-962">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="5ec08-963">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="5ec08-963">Remarks - isDisplayed</span></span>

<span data-ttu-id="5ec08-964">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-964">To modify the visible state of the control, call the visible method.</span></span>

### <a name="examples---isdisplayed"></a><span data-ttu-id="5ec08-965">例 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="5ec08-965">Examples - isDisplayed</span></span>

<span data-ttu-id="5ec08-966">次の例は、コントロールが可視かどうかを判断する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-966">The following example shows how to determine whether a control is visible.</span></span>

```xpp
info(strfmt("isDisplayed: %1", this.isDisplayed()));
```

## <a name="method-isrestricted"></a><span data-ttu-id="5ec08-967">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="5ec08-967">Method isRestricted</span></span>

<span data-ttu-id="5ec08-968">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-968">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="5ec08-969">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="5ec08-969">Return Value - isRestricted</span></span>

<span data-ttu-id="5ec08-970">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-970">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="5ec08-971">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="5ec08-971">Method isUserSetupEnabled</span></span>

<span data-ttu-id="5ec08-972">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-972">Retrieves a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="5ec08-973">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="5ec08-973">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="5ec08-974">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="5ec08-974">neededSetupRights</span></span>  
<span data-ttu-id="5ec08-975">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-975">A value from the FormAllowUserSetup enumeration that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="5ec08-976">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="5ec08-976">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="5ec08-977">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-977">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span> <span data-ttu-id="5ec08-978">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-978">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="5ec08-979">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="5ec08-979">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="5ec08-980">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-980">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec08-981">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="5ec08-981">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="5ec08-982">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-982">No changes can be made to the control.</span></span> <span data-ttu-id="5ec08-983">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-983">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="5ec08-984">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="5ec08-984">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="5ec08-985">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-985">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="5ec08-986">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-986">The user cannot move the control.</span></span>   |
| <span data-ttu-id="5ec08-987">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="5ec08-987">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="5ec08-988">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-988">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="5ec08-989">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-989">The user can also move the control.</span></span> |

### <a name="examples---isusersetupenabled"></a><span data-ttu-id="5ec08-990">例 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="5ec08-990">Examples - isUserSetupEnabled</span></span>

<span data-ttu-id="5ec08-991">次の例は、コントロールのユーザー設定権限を決定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-991">The following example shows how to determine the user setup rights for a control.</span></span>

```xpp
FormAllowUserSetup formAllowUserSetup = FormAllowUserSetup::No; 
switch (true) 
{ 
    case this.isUserSetupEnabled(FormAllowUserSetup::Yes): 
        formAllowUserSetup = FormAllowUserSetup::Yes; 
        break; 
    case this.isUserSetupEnabled(FormAllowUserSetup::Restricted): 
        formAllowUserSetup = FormAllowUserSetup::Restricted; 
        break; 
    case this.isUserSetupEnabled(FormAllowUserSetup::No): 
       formAllowUserSetup = FormAllowUserSetup::No; 
        break; 
} 
info (strfmt("formAllowUserSetup: %1", formAllowUserSetup));
```

## <a name="method-italic"></a><span data-ttu-id="5ec08-992">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="5ec08-992">Method italic</span></span>

<span data-ttu-id="5ec08-993">コントロールのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-993">Sets or returns a value that indicates whether the text in the control is italic.</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="5ec08-994">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="5ec08-994">Parameters - italic</span></span>

<span data-ttu-id="5ec08-995">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-995">value</span></span>  
<span data-ttu-id="5ec08-996">コントロールのイタリック設定に割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-996">The value to assign to the italic setting for the control.</span></span>

### <a name="return-value---italic"></a><span data-ttu-id="5ec08-997">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="5ec08-997">Return Value - italic</span></span>

<span data-ttu-id="5ec08-998">コントロール内のテキストが斜体である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-998">true if the text in the control is italic; otherwise, false.</span></span>

## <a name="method-keydown"></a><span data-ttu-id="5ec08-999">メソッド keyDown</span><span class="sxs-lookup"><span data-stu-id="5ec08-999">Method keyDown</span></span>

```xpp
public boolean keyDown(int vKey, boolean Ctrl, boolean Shift)
```

### <a name="parameters---keydown"></a><span data-ttu-id="5ec08-1000">パラメーター - keyDown</span><span class="sxs-lookup"><span data-stu-id="5ec08-1000">Parameters - keyDown</span></span>

<span data-ttu-id="5ec08-1001">vKey</span><span class="sxs-lookup"><span data-stu-id="5ec08-1001">vKey</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1002">Ctrl</span><span class="sxs-lookup"><span data-stu-id="5ec08-1002">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1003">Shift</span><span class="sxs-lookup"><span data-stu-id="5ec08-1003">Shift</span></span>  

### <a name="return-value---keydown"></a><span data-ttu-id="5ec08-1004">戻り値 - keyDown</span><span class="sxs-lookup"><span data-stu-id="5ec08-1004">Return Value - keyDown</span></span>

## <a name="method-leave"></a><span data-ttu-id="5ec08-1005">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="5ec08-1005">Method leave</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="5ec08-1006">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="5ec08-1006">Return Value - leave</span></span>

## <a name="method-left"></a><span data-ttu-id="5ec08-1007">メソッド left</span><span class="sxs-lookup"><span data-stu-id="5ec08-1007">Method left</span></span>

<span data-ttu-id="5ec08-1008">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1008">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="5ec08-1009">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="5ec08-1009">Parameters - left</span></span>

<span data-ttu-id="5ec08-1010">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1010">value</span></span>  
<span data-ttu-id="5ec08-1011">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1011">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1012">モード</span><span class="sxs-lookup"><span data-stu-id="5ec08-1012">mode</span></span>  
<span data-ttu-id="5ec08-1013">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1013">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---left"></a><span data-ttu-id="5ec08-1014">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="5ec08-1014">Return Value - left</span></span>

<span data-ttu-id="5ec08-1015">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1015">The horizontal position of the control in the form.</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="5ec08-1016">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1016">Method leftMode</span></span>

<span data-ttu-id="5ec08-1017">フォームのコントロールの水平配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1017">Sets the horizontal arrange mode for the control in the form.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="5ec08-1018">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1018">Parameters - leftMode</span></span>

<span data-ttu-id="5ec08-1019">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1019">value</span></span>  
<span data-ttu-id="5ec08-1020">コントロールの水平配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1020">An integer value that indicates the horizontal arrange mode for the control; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="5ec08-1021">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1021">Return Value - leftMode</span></span>

<span data-ttu-id="5ec08-1022">フォームのコントロールの水平配置モード。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1022">The horizontal arrange mode for the control in the form.</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="5ec08-1023">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1023">Method leftValue</span></span>

<span data-ttu-id="5ec08-1024">フォームのコントロールの水平位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1024">Gets or sets the horizontal position of the control in the form.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="5ec08-1025">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1025">Parameters - leftValue</span></span>

<span data-ttu-id="5ec08-1026">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1026">value</span></span>  
<span data-ttu-id="5ec08-1027">コントロールの水平位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1027">An integer value that indicates the horizontal position of the control; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="5ec08-1028">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1028">Return Value - leftValue</span></span>

<span data-ttu-id="5ec08-1029">フォーム内のコントロールの水平位置。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1029">The horizontal position of the control in the form.</span></span>

## <a name="method-linesatroot"></a><span data-ttu-id="5ec08-1030">メソッド linesAtRoot</span><span class="sxs-lookup"><span data-stu-id="5ec08-1030">Method linesAtRoot</span></span>

```xpp
public boolean linesAtRoot([boolean value])
```

### <a name="parameters---linesatroot"></a><span data-ttu-id="5ec08-1031">パラメーター - linesAtRoot</span><span class="sxs-lookup"><span data-stu-id="5ec08-1031">Parameters - linesAtRoot</span></span>

<span data-ttu-id="5ec08-1032">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1032">value</span></span>  

### <a name="return-value---linesatroot"></a><span data-ttu-id="5ec08-1033">戻り値 - linesAtRoot</span><span class="sxs-lookup"><span data-stu-id="5ec08-1033">Return Value - linesAtRoot</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="5ec08-1034">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="5ec08-1034">Method markAsUserAdd</span></span>

<span data-ttu-id="5ec08-1035">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1035">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="5ec08-1036">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="5ec08-1036">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="5ec08-1037">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1037">value</span></span>  
<span data-ttu-id="5ec08-1038">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1038">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="5ec08-1039">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="5ec08-1039">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="5ec08-1040">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1040">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="5ec08-1041">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="5ec08-1041">Method mouseDblClick</span></span>

<span data-ttu-id="5ec08-1042">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1042">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="5ec08-1043">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="5ec08-1043">Parameters - mouseDblClick</span></span>

<span data-ttu-id="5ec08-1044">x</span><span class="sxs-lookup"><span data-stu-id="5ec08-1044">x</span></span>  
<span data-ttu-id="5ec08-1045">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1045">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1046">y</span><span class="sxs-lookup"><span data-stu-id="5ec08-1046">y</span></span>  
<span data-ttu-id="5ec08-1047">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1047">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1048">ボタン</span><span class="sxs-lookup"><span data-stu-id="5ec08-1048">button</span></span>  
<span data-ttu-id="5ec08-1049">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1049">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1050">Ctrl</span><span class="sxs-lookup"><span data-stu-id="5ec08-1050">Ctrl</span></span>  
<span data-ttu-id="5ec08-1051">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1051">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1052">シフト</span><span class="sxs-lookup"><span data-stu-id="5ec08-1052">Shift</span></span>  
<span data-ttu-id="5ec08-1053">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1053">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="5ec08-1054">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="5ec08-1054">Return Value - mouseDblClick</span></span>

<span data-ttu-id="5ec08-1055">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1055">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="5ec08-1056">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="5ec08-1056">Remarks - mouseDblClick</span></span>

<span data-ttu-id="5ec08-1057">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1057">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="examples---mousedblclick"></a><span data-ttu-id="5ec08-1058">例 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="5ec08-1058">Examples - mouseDblClick</span></span>

<span data-ttu-id="5ec08-1059">次の例は、Infolog に mouseDblClick イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1059">The following example shows how to display the parameters of a mouseDblClick event in the Infolog.</span></span>

```xpp
public int mouseDblClick(int x,  
                         int y,  
                         int button, 
                         boolean Ctrl, 
                         boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mousedown"></a><span data-ttu-id="5ec08-1060">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="5ec08-1060">Method mouseDown</span></span>

<span data-ttu-id="5ec08-1061">ユーザーがマウス ポインターがコントロール上にある状態でクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1061">Is called when the user clicks while the mouse pointer is over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="5ec08-1062">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="5ec08-1062">Parameters - mouseDown</span></span>

<span data-ttu-id="5ec08-1063">x</span><span class="sxs-lookup"><span data-stu-id="5ec08-1063">x</span></span>  
<span data-ttu-id="5ec08-1064">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1064">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1065">y</span><span class="sxs-lookup"><span data-stu-id="5ec08-1065">y</span></span>  
<span data-ttu-id="5ec08-1066">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1066">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1067">ボタン</span><span class="sxs-lookup"><span data-stu-id="5ec08-1067">button</span></span>  
<span data-ttu-id="5ec08-1068">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1068">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1069">Ctrl</span><span class="sxs-lookup"><span data-stu-id="5ec08-1069">Ctrl</span></span>  
<span data-ttu-id="5ec08-1070">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1070">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1071">シフト</span><span class="sxs-lookup"><span data-stu-id="5ec08-1071">Shift</span></span>  
<span data-ttu-id="5ec08-1072">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1072">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="5ec08-1073">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="5ec08-1073">Return Value - mouseDown</span></span>

<span data-ttu-id="5ec08-1074">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1074">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="5ec08-1075">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="5ec08-1075">Remarks - mouseDown</span></span>

<span data-ttu-id="5ec08-1076">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1076">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="5ec08-1077">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1077">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="examples---mousedown"></a><span data-ttu-id="5ec08-1078">例 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="5ec08-1078">Examples - mouseDown</span></span>

<span data-ttu-id="5ec08-1079">次の例は、Infolog に mouseDown イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1079">The following example shows how to display the parameters of a mouseDown event in the Infolog.</span></span>

```xpp
public int mouseDown(int x,  
                              int y,  
                              int button, 
                              boolean Ctrl, 
                              boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mousemove"></a><span data-ttu-id="5ec08-1080">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="5ec08-1080">Method mouseMove</span></span>

<span data-ttu-id="5ec08-1081">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1081">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="5ec08-1082">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="5ec08-1082">Parameters - mouseMove</span></span>

<span data-ttu-id="5ec08-1083">x</span><span class="sxs-lookup"><span data-stu-id="5ec08-1083">x</span></span>  
<span data-ttu-id="5ec08-1084">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1084">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1085">y</span><span class="sxs-lookup"><span data-stu-id="5ec08-1085">y</span></span>  
<span data-ttu-id="5ec08-1086">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1086">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1087">ボタン</span><span class="sxs-lookup"><span data-stu-id="5ec08-1087">button</span></span>  
<span data-ttu-id="5ec08-1088">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1088">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1089">Ctrl</span><span class="sxs-lookup"><span data-stu-id="5ec08-1089">Ctrl</span></span>  
<span data-ttu-id="5ec08-1090">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1090">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1091">シフト</span><span class="sxs-lookup"><span data-stu-id="5ec08-1091">Shift</span></span>  
<span data-ttu-id="5ec08-1092">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1092">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="5ec08-1093">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="5ec08-1093">Return Value - mouseMove</span></span>

<span data-ttu-id="5ec08-1094">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1094">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="5ec08-1095">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="5ec08-1095">Remarks - mouseMove</span></span>

<span data-ttu-id="5ec08-1096">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1096">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

### <a name="examples---mousemove"></a><span data-ttu-id="5ec08-1097">例 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="5ec08-1097">Examples - mouseMove</span></span>

<span data-ttu-id="5ec08-1098">次の例は、Infolog に mouseMove イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1098">The following example shows how to display the parameters of a mouseMove event in the Infolog.</span></span>

```xpp
public int mouseMove(int x,  
                     int y,  
                     int button, 
                     boolean Ctrl, 
                     boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-mouseup"></a><span data-ttu-id="5ec08-1099">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="5ec08-1099">Method mouseUp</span></span>

<span data-ttu-id="5ec08-1100">マウス ポインターがコントロール上にある状態で、ユーザーがマウス ボタンを放すと呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1100">Is called when the user releases the mouse button while the mouse pointer is over the control.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="5ec08-1101">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="5ec08-1101">Parameters - mouseUp</span></span>

<span data-ttu-id="5ec08-1102">x</span><span class="sxs-lookup"><span data-stu-id="5ec08-1102">x</span></span>  
<span data-ttu-id="5ec08-1103">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1103">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1104">y</span><span class="sxs-lookup"><span data-stu-id="5ec08-1104">y</span></span>  
<span data-ttu-id="5ec08-1105">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1105">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1106">ボタン</span><span class="sxs-lookup"><span data-stu-id="5ec08-1106">button</span></span>  
<span data-ttu-id="5ec08-1107">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1107">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1108">Ctrl</span><span class="sxs-lookup"><span data-stu-id="5ec08-1108">Ctrl</span></span>  
<span data-ttu-id="5ec08-1109">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1109">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1110">シフト</span><span class="sxs-lookup"><span data-stu-id="5ec08-1110">Shift</span></span>  
<span data-ttu-id="5ec08-1111">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1111">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="5ec08-1112">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="5ec08-1112">Return Value - mouseUp</span></span>

<span data-ttu-id="5ec08-1113">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1113">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="5ec08-1114">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="5ec08-1114">Remarks - mouseUp</span></span>

<span data-ttu-id="5ec08-1115">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1115">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="5ec08-1116">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1116">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

### <a name="examples---mouseup"></a><span data-ttu-id="5ec08-1117">例 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="5ec08-1117">Examples - mouseUp</span></span>

<span data-ttu-id="5ec08-1118">次の例は、Infolog に mouseUp イベントのパラメーターを表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1118">The following example shows how to display the parameters of a mouseUp event in the Infolog.</span></span>

```xpp
public int mouseUp(int x,  
                   int y,  
                   int button, 
                   boolean Ctrl, 
                   boolean Shift) 
{ 
    int ret; 
    if (Shift) 
    { 
        info( "Shift set" ); 
    } 
    if (Ctrl) 
    { 
        info( "Ctrl set"); 
    } 
    info (strfmt("x, y: %1 %2 button: %3", x, y, button)); 
    ret = super(x, y, button, Ctrl, Shift); 
    info (strfmt("ret: %1", ret)); 
    return ret; 
}
```

## <a name="method-moveitem"></a><span data-ttu-id="5ec08-1119">メソッド moveItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1119">Method moveItem</span></span>

```xpp
public int moveItem(int Idx, int newParent, [int insertAfter])
```

### <a name="parameters---moveitem"></a><span data-ttu-id="5ec08-1120">パラメーター - moveItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1120">Parameters - moveItem</span></span>

<span data-ttu-id="5ec08-1121">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1121">Idx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1122">newParent</span><span class="sxs-lookup"><span data-stu-id="5ec08-1122">newParent</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1123">insertAfter</span><span class="sxs-lookup"><span data-stu-id="5ec08-1123">insertAfter</span></span>  

### <a name="return-value---moveitem"></a><span data-ttu-id="5ec08-1124">戻り値 - moveItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1124">Return Value - moveItem</span></span>

## <a name="method-name"></a><span data-ttu-id="5ec08-1125">メソッド名</span><span class="sxs-lookup"><span data-stu-id="5ec08-1125">Method name</span></span>

<span data-ttu-id="5ec08-1126">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1126">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="5ec08-1127">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="5ec08-1127">Parameters - name</span></span>

<span data-ttu-id="5ec08-1128">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1128">value</span></span>  
<span data-ttu-id="5ec08-1129">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1129">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="5ec08-1130">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="5ec08-1130">Return Value - name</span></span>

<span data-ttu-id="5ec08-1131">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1131">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="5ec08-1132">備考 - name</span><span class="sxs-lookup"><span data-stu-id="5ec08-1132">Remarks - name</span></span>

<span data-ttu-id="5ec08-1133">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1133">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="5ec08-1134">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1134">Begins with a letter.</span></span>
-   <span data-ttu-id="5ec08-1135">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1135">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="5ec08-1136">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1136">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="5ec08-1137">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1137">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="5ec08-1138">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1138">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="5ec08-1139">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="5ec08-1139">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="5ec08-1140">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="5ec08-1140">Parameters - neededPermission</span></span>

<span data-ttu-id="5ec08-1141">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1141">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="5ec08-1142">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="5ec08-1142">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5ec08-1143">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5ec08-1143">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="5ec08-1144">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5ec08-1144">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="5ec08-1145">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="5ec08-1145">Method parentControl</span></span>

<span data-ttu-id="5ec08-1146">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1146">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="5ec08-1147">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="5ec08-1147">Return Value - parentControl</span></span>

<span data-ttu-id="5ec08-1148">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1148">The parent control for the control.</span></span>

## <a name="method-rowselect"></a><span data-ttu-id="5ec08-1149">メソッド rowSelect</span><span class="sxs-lookup"><span data-stu-id="5ec08-1149">Method rowSelect</span></span>

```xpp
public boolean rowSelect([boolean value])
```

### <a name="parameters---rowselect"></a><span data-ttu-id="5ec08-1150">パラメーター - rowSelect</span><span class="sxs-lookup"><span data-stu-id="5ec08-1150">Parameters - rowSelect</span></span>

<span data-ttu-id="5ec08-1151">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1151">value</span></span>  

### <a name="return-value---rowselect"></a><span data-ttu-id="5ec08-1152">戻り値 - rowSelect</span><span class="sxs-lookup"><span data-stu-id="5ec08-1152">Return Value - rowSelect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="5ec08-1153">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="5ec08-1153">Method securityKey</span></span>

<span data-ttu-id="5ec08-1154">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1154">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="5ec08-1155">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="5ec08-1155">Parameters - securityKey</span></span>

<span data-ttu-id="5ec08-1156">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1156">value</span></span>  
<span data-ttu-id="5ec08-1157">コントロールに割り当てるセキュリティ キーの ID。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1157">The ID of the security key to assign to the control.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="5ec08-1158">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="5ec08-1158">Return Value - securityKey</span></span>

<span data-ttu-id="5ec08-1159">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1159">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

### <a name="examples---securitykey"></a><span data-ttu-id="5ec08-1160">例 - securityKey</span><span class="sxs-lookup"><span data-stu-id="5ec08-1160">Examples - securityKey</span></span>

<span data-ttu-id="5ec08-1161">次の例では、コントロールのセキュリティ キー IDを取得して割り当てる方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1161">The following example shows how to retrieve and assign a security key ID for a control.</span></span>

```xpp
DictSecurityKey dsk; 
securityKeyId ski; 
// objCtrl previously assigned. 
// Assign a security key ID to the control. 
objCtrl.securityKey(securitykeynum(AdminDaily)); 
// Retrieve the security key ID from the control. 
ski = objCtrl.securityKey(); 
if (ski != 0) 
{ 
    dsk = new DictSecurityKey(ski); 
    if (dsk) 
    { 
        print strfmt("Security Key ID: %1 Security Key Name: %2", 
                     ski, 
                     dsk.name()); 
    } 
}
```

## <a name="method-select"></a><span data-ttu-id="5ec08-1162">メソッド select</span><span class="sxs-lookup"><span data-stu-id="5ec08-1162">Method select</span></span>

```xpp
public int select(int Idx)
```

### <a name="parameters---select"></a><span data-ttu-id="5ec08-1163">パラメーター - select</span><span class="sxs-lookup"><span data-stu-id="5ec08-1163">Parameters - select</span></span>

<span data-ttu-id="5ec08-1164">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1164">Idx</span></span>  

### <a name="return-value---select"></a><span data-ttu-id="5ec08-1165">戻り値 - select</span><span class="sxs-lookup"><span data-stu-id="5ec08-1165">Return Value - select</span></span>

## <a name="method-selectex"></a><span data-ttu-id="5ec08-1166">メソッド selectEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1166">Method selectEx</span></span>

```xpp
public int selectEx(int Idx, boolean setSelection)
```

### <a name="parameters---selectex"></a><span data-ttu-id="5ec08-1167">パラメーター - selectEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1167">Parameters - selectEx</span></span>

<span data-ttu-id="5ec08-1168">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1168">Idx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1169">setSelection</span><span class="sxs-lookup"><span data-stu-id="5ec08-1169">setSelection</span></span>  

### <a name="return-value---selectex"></a><span data-ttu-id="5ec08-1170">戻り値 - selectEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1170">Return Value - selectEx</span></span>

## <a name="method-selectionchanging"></a><span data-ttu-id="5ec08-1171">メソッド selectionChanging</span><span class="sxs-lookup"><span data-stu-id="5ec08-1171">Method selectionChanging</span></span>

```xpp
public boolean selectionChanging(FormTreeItem OldItem, FormTreeItem NewItem, FormTreeSelect how)
```

### <a name="parameters---selectionchanging"></a><span data-ttu-id="5ec08-1172">パラメーター - selectionChanging</span><span class="sxs-lookup"><span data-stu-id="5ec08-1172">Parameters - selectionChanging</span></span>

<span data-ttu-id="5ec08-1173">OldItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1173">OldItem</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1174">NewItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1174">NewItem</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1175">how</span><span class="sxs-lookup"><span data-stu-id="5ec08-1175">how</span></span>  

### <a name="return-value---selectionchanging"></a><span data-ttu-id="5ec08-1176">戻り値 - selectionChanging</span><span class="sxs-lookup"><span data-stu-id="5ec08-1176">Return Value - selectionChanging</span></span>

## <a name="method-selectitems"></a><span data-ttu-id="5ec08-1177">メソッド selectItems</span><span class="sxs-lookup"><span data-stu-id="5ec08-1177">Method selectItems</span></span>

```xpp
public int selectItems(int fromIdx, int toIdx)
```

### <a name="parameters---selectitems"></a><span data-ttu-id="5ec08-1178">パラメーター - selectItems</span><span class="sxs-lookup"><span data-stu-id="5ec08-1178">Parameters - selectItems</span></span>

<span data-ttu-id="5ec08-1179">fromIdx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1179">fromIdx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1180">toIdx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1180">toIdx</span></span>  

### <a name="return-value---selectitems"></a><span data-ttu-id="5ec08-1181">戻り値 - selectItems</span><span class="sxs-lookup"><span data-stu-id="5ec08-1181">Return Value - selectItems</span></span>

## <a name="method-selectsetfirstvisible"></a><span data-ttu-id="5ec08-1182">メソッド selectSetFirstVisible</span><span class="sxs-lookup"><span data-stu-id="5ec08-1182">Method selectSetFirstVisible</span></span>

```xpp
public int selectSetFirstVisible(int Idx)
```

### <a name="parameters---selectsetfirstvisible"></a><span data-ttu-id="5ec08-1183">パラメーター - selectSetFirstVisible</span><span class="sxs-lookup"><span data-stu-id="5ec08-1183">Parameters - selectSetFirstVisible</span></span>

<span data-ttu-id="5ec08-1184">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1184">Idx</span></span>  

### <a name="return-value---selectsetfirstvisible"></a><span data-ttu-id="5ec08-1185">戻り値 - selectSetFirstVisible</span><span class="sxs-lookup"><span data-stu-id="5ec08-1185">Return Value - selectSetFirstVisible</span></span>

## <a name="method-setinsertmark"></a><span data-ttu-id="5ec08-1186">メソッド setInsertMark</span><span class="sxs-lookup"><span data-stu-id="5ec08-1186">Method setInsertMark</span></span>

```xpp
public boolean setInsertMark(int Idx, boolean After)
```

### <a name="parameters---setinsertmark"></a><span data-ttu-id="5ec08-1187">パラメーター - setInsertMark</span><span class="sxs-lookup"><span data-stu-id="5ec08-1187">Parameters - setInsertMark</span></span>

<span data-ttu-id="5ec08-1188">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1188">Idx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1189">変更後</span><span class="sxs-lookup"><span data-stu-id="5ec08-1189">After</span></span>  

### <a name="return-value---setinsertmark"></a><span data-ttu-id="5ec08-1190">戻り値 - setInsertMark</span><span class="sxs-lookup"><span data-stu-id="5ec08-1190">Return Value - setInsertMark</span></span>

## <a name="method-setitem"></a><span data-ttu-id="5ec08-1191">メソッド setItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1191">Method setItem</span></span>

```xpp
public boolean setItem(FormTreeItem item)
```

### <a name="parameters---setitem"></a><span data-ttu-id="5ec08-1192">パラメーター - setItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1192">Parameters - setItem</span></span>

<span data-ttu-id="5ec08-1193">品目</span><span class="sxs-lookup"><span data-stu-id="5ec08-1193">item</span></span>  

### <a name="return-value---setitem"></a><span data-ttu-id="5ec08-1194">戻り値 - setItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1194">Return Value - setItem</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="5ec08-1195">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="5ec08-1195">Method showContextMenu</span></span>

<span data-ttu-id="5ec08-1196">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1196">Shows the shortcut menu for the control.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="5ec08-1197">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="5ec08-1197">Parameters - showContextMenu</span></span>

<span data-ttu-id="5ec08-1198">menuHandle</span><span class="sxs-lookup"><span data-stu-id="5ec08-1198">menuHandle</span></span>  
<span data-ttu-id="5ec08-1199">表示するメニューの ID。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1199">The ID of the menu to show.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="5ec08-1200">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="5ec08-1200">Return Value - showContextMenu</span></span>

<span data-ttu-id="5ec08-1201">通話が成功したかどうかを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1201">An integer value that indicates whether the call succeeded.</span></span>

## <a name="method-showselalways"></a><span data-ttu-id="5ec08-1202">メソッド showSelAlways</span><span class="sxs-lookup"><span data-stu-id="5ec08-1202">Method showSelAlways</span></span>

```xpp
public boolean showSelAlways([boolean value])
```

### <a name="parameters---showselalways"></a><span data-ttu-id="5ec08-1203">パラメーター - showSelAlways</span><span class="sxs-lookup"><span data-stu-id="5ec08-1203">Parameters - showSelAlways</span></span>

<span data-ttu-id="5ec08-1204">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1204">value</span></span>  

### <a name="return-value---showselalways"></a><span data-ttu-id="5ec08-1205">戻り値 - showSelAlways</span><span class="sxs-lookup"><span data-stu-id="5ec08-1205">Return Value - showSelAlways</span></span>

## <a name="method-singleselection"></a><span data-ttu-id="5ec08-1206">メソッド singleSelection</span><span class="sxs-lookup"><span data-stu-id="5ec08-1206">Method singleSelection</span></span>

```xpp
public boolean singleSelection([boolean value])
```

### <a name="parameters---singleselection"></a><span data-ttu-id="5ec08-1207">パラメーター - singleSelection</span><span class="sxs-lookup"><span data-stu-id="5ec08-1207">Parameters - singleSelection</span></span>

<span data-ttu-id="5ec08-1208">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1208">value</span></span>  

### <a name="return-value---singleselection"></a><span data-ttu-id="5ec08-1209">戻り値 - singleSelection</span><span class="sxs-lookup"><span data-stu-id="5ec08-1209">Return Value - singleSelection</span></span>

## <a name="method-skip"></a><span data-ttu-id="5ec08-1210">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1210">Method skip</span></span>

<span data-ttu-id="5ec08-1211">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1211">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="5ec08-1212">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1212">Parameters - skip</span></span>

<span data-ttu-id="5ec08-1213">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1213">value</span></span>  
<span data-ttu-id="5ec08-1214">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1214">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="5ec08-1215">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1215">Return Value - skip</span></span>

<span data-ttu-id="5ec08-1216">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1216">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="5ec08-1217">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1217">Remarks - skip</span></span>

<span data-ttu-id="5ec08-1218">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1218">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span>

### <a name="examples---skip"></a><span data-ttu-id="5ec08-1219">例 - skip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1219">Examples - skip</span></span>

<span data-ttu-id="5ec08-1220">以下は、コントロールのスキップ プロパティを返す方法と設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1220">The following shows how to return and set the skip property of a control.</span></span>

```xpp
// Return the value of the skip property. 
info(strfmt("skip: %1", this.skip())); 
// Set the value of the skip property. 
this.skip(true);
```

## <a name="method-tooltip"></a><span data-ttu-id="5ec08-1221">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1221">Method toolTip</span></span>

<span data-ttu-id="5ec08-1222">コントロールのツールヒント テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1222">Returns the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="5ec08-1223">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1223">Return Value - toolTip</span></span>

<span data-ttu-id="5ec08-1224">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1224">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="5ec08-1225">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1225">Remarks - toolTip</span></span>

<span data-ttu-id="5ec08-1226">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1226">The method can be overridden to provide a value to the toolTip method.</span></span>

### <a name="examples---tooltip"></a><span data-ttu-id="5ec08-1227">例 - toolTip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1227">Examples - toolTip</span></span>

<span data-ttu-id="5ec08-1228">次の例は、toolTip メソッドを上書きする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1228">The following example shows how to override the toolTip method.</span></span>

```xpp
str toolTip() 
{ 
    return "Account numbers of customers eligible for discount"; 
}
```

## <a name="method-top"></a><span data-ttu-id="5ec08-1229">メソッド top</span><span class="sxs-lookup"><span data-stu-id="5ec08-1229">Method top</span></span>

<span data-ttu-id="5ec08-1230">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1230">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="5ec08-1231">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="5ec08-1231">Parameters - top</span></span>

<span data-ttu-id="5ec08-1232">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1232">value</span></span>  
<span data-ttu-id="5ec08-1233">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1233">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1234">モード</span><span class="sxs-lookup"><span data-stu-id="5ec08-1234">mode</span></span>  
<span data-ttu-id="5ec08-1235">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1235">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---top"></a><span data-ttu-id="5ec08-1236">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="5ec08-1236">Return Value - top</span></span>

<span data-ttu-id="5ec08-1237">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1237">The vertical position of the control in the form.</span></span>

## <a name="method-topmode"></a><span data-ttu-id="5ec08-1238">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1238">Method topMode</span></span>

<span data-ttu-id="5ec08-1239">フォームのコントロールの垂直配置モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1239">Sets the vertical arrange mode for the control in the form.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="5ec08-1240">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1240">Parameters - topMode</span></span>

<span data-ttu-id="5ec08-1241">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1241">value</span></span>  
<span data-ttu-id="5ec08-1242">コントロールの垂直配置モードを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1242">An integer value that indicates the vertical arrange mode for the control; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="5ec08-1243">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1243">Return Value - topMode</span></span>

<span data-ttu-id="5ec08-1244">フォームのコントロールの垂直配置モード。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1244">The vertical arrange mode for the control in the form.</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="5ec08-1245">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1245">Method topValue</span></span>

<span data-ttu-id="5ec08-1246">フォームのコントロールの垂直位置を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1246">Gets or sets the vertical position of the control in the form.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="5ec08-1247">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1247">Parameters - topValue</span></span>

<span data-ttu-id="5ec08-1248">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1248">value</span></span>  
<span data-ttu-id="5ec08-1249">コントロールの垂直位置を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1249">An integer value that indicates the vertical position of the control; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="5ec08-1250">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1250">Return Value - topValue</span></span>

<span data-ttu-id="5ec08-1251">フォーム内のコントロールの垂直位置。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1251">The vertical position of the control in the form.</span></span>

## <a name="method-trackselect"></a><span data-ttu-id="5ec08-1252">メソッド trackSelect</span><span class="sxs-lookup"><span data-stu-id="5ec08-1252">Method trackSelect</span></span>

```xpp
public boolean trackSelect([boolean value])
```

### <a name="parameters---trackselect"></a><span data-ttu-id="5ec08-1253">パラメーター - trackSelect</span><span class="sxs-lookup"><span data-stu-id="5ec08-1253">Parameters - trackSelect</span></span>

<span data-ttu-id="5ec08-1254">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1254">value</span></span>  

### <a name="return-value---trackselect"></a><span data-ttu-id="5ec08-1255">戻り値 - trackSelect</span><span class="sxs-lookup"><span data-stu-id="5ec08-1255">Return Value - trackSelect</span></span>

## <a name="method-type"></a><span data-ttu-id="5ec08-1256">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="5ec08-1256">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="5ec08-1257">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="5ec08-1257">Parameters - type</span></span>

<span data-ttu-id="5ec08-1258">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1258">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="5ec08-1259">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="5ec08-1259">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="5ec08-1260">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="5ec08-1260">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="5ec08-1261">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="5ec08-1261">Parameters - underline</span></span>

<span data-ttu-id="5ec08-1262">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1262">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="5ec08-1263">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="5ec08-1263">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="5ec08-1264">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5ec08-1264">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="5ec08-1265">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5ec08-1265">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="5ec08-1266">データ</span><span class="sxs-lookup"><span data-stu-id="5ec08-1266">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="5ec08-1267">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="5ec08-1267">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="5ec08-1268">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="5ec08-1268">Method userData</span></span>

<span data-ttu-id="5ec08-1269">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1269">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="5ec08-1270">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="5ec08-1270">Parameters - userData</span></span>

<span data-ttu-id="5ec08-1271">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1271">value</span></span>  
<span data-ttu-id="5ec08-1272">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1272">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="5ec08-1273">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="5ec08-1273">Return Value - userData</span></span>

<span data-ttu-id="5ec08-1274">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1274">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="5ec08-1275">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1275">Method userDataItem</span></span>

<span data-ttu-id="5ec08-1276">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1276">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="5ec08-1277">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1277">Parameters - userDataItem</span></span>

<span data-ttu-id="5ec08-1278">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1278">value</span></span>  
<span data-ttu-id="5ec08-1279">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1279">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="5ec08-1280">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1280">Return Value - userDataItem</span></span>

<span data-ttu-id="5ec08-1281">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1281">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="5ec08-1282">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="5ec08-1282">Method userDataItems</span></span>

<span data-ttu-id="5ec08-1283">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1283">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="5ec08-1284">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="5ec08-1284">Parameters - userDataItems</span></span>

<span data-ttu-id="5ec08-1285">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1285">value</span></span>  
<span data-ttu-id="5ec08-1286">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1286">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="5ec08-1287">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="5ec08-1287">Return Value - userDataItems</span></span>

<span data-ttu-id="5ec08-1288">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1288">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="5ec08-1289">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="5ec08-1289">Method userDisable</span></span>

<span data-ttu-id="5ec08-1290">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1290">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="5ec08-1291">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="5ec08-1291">Parameters - userDisable</span></span>

<span data-ttu-id="5ec08-1292">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1292">value</span></span>  
<span data-ttu-id="5ec08-1293">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1293">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="5ec08-1294">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="5ec08-1294">Return Value - userDisable</span></span>

<span data-ttu-id="5ec08-1295">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1295">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="5ec08-1296">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="5ec08-1296">Method userHeight</span></span>

<span data-ttu-id="5ec08-1297">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1297">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="5ec08-1298">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="5ec08-1298">Parameters - userHeight</span></span>

<span data-ttu-id="5ec08-1299">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1299">value</span></span>  
<span data-ttu-id="5ec08-1300">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1300">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="5ec08-1301">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="5ec08-1301">Return Value - userHeight</span></span>

<span data-ttu-id="5ec08-1302">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1302">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="5ec08-1303">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="5ec08-1303">Method userHide</span></span>

<span data-ttu-id="5ec08-1304">フォーム ツリー コントロールがユーザーから非表示になっているかどうかを示す値を返すか設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1304">Returns or sets the value that indicates whether the form tree control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="5ec08-1305">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="5ec08-1305">Parameters - userHide</span></span>

<span data-ttu-id="5ec08-1306">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1306">value</span></span>  
<span data-ttu-id="5ec08-1307">フォーム ツリー コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1307">The value that indicates whether the form tree control is hidden from the user.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="5ec08-1308">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="5ec08-1308">Return Value - userHide</span></span>

<span data-ttu-id="5ec08-1309">ツリー コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1309">1 if the tree control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="5ec08-1310">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="5ec08-1310">Remarks - userHide</span></span>

<span data-ttu-id="5ec08-1311">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1311">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="5ec08-1312">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1312">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="5ec08-1313">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1313">This method lets you programmatically determine and set the value.</span></span>

### <a name="examples---userhide"></a><span data-ttu-id="5ec08-1314">例 - userHide</span><span class="sxs-lookup"><span data-stu-id="5ec08-1314">Examples - userHide</span></span>

<span data-ttu-id="5ec08-1315">次の例は、フォーム ツリー コントロールがユーザーから隠されているかどうかを指定する値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1315">The following example shows how to return and set the value that specifies whether the form tree control is hidden from the user.</span></span>

```xpp
int nUserHide; 
// The ctrl variable was previously assigned  
// as a form tree control variable. 
// Retrieve the userHide value. 
nUserHide = ctrl.userHide(); 
// Set the userHide value. 
ctrl.userHide(1);
```

## <a name="method-userorgcontainer"></a><span data-ttu-id="5ec08-1316">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="5ec08-1316">Method userOrgContainer</span></span>

<span data-ttu-id="5ec08-1317">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1317">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="5ec08-1318">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="5ec08-1318">Parameters - userOrgContainer</span></span>

<span data-ttu-id="5ec08-1319">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1319">value</span></span>  
<span data-ttu-id="5ec08-1320">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1320">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="5ec08-1321">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="5ec08-1321">Return Value - userOrgContainer</span></span>

<span data-ttu-id="5ec08-1322">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1322">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="5ec08-1323">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="5ec08-1323">Method userOrgSibling</span></span>

<span data-ttu-id="5ec08-1324">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1324">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="5ec08-1325">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="5ec08-1325">Parameters - userOrgSibling</span></span>

<span data-ttu-id="5ec08-1326">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1326">value</span></span>  
<span data-ttu-id="5ec08-1327">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1327">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="5ec08-1328">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="5ec08-1328">Return Value - userOrgSibling</span></span>

<span data-ttu-id="5ec08-1329">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1329">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="5ec08-1330">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="5ec08-1330">Method userPromptText</span></span>

<span data-ttu-id="5ec08-1331">コントロールのユーザー プロンプト テキストを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1331">Sets or retrieves the user prompt text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="5ec08-1332">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="5ec08-1332">Parameters - userPromptText</span></span>

<span data-ttu-id="5ec08-1333">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1333">value</span></span>  
<span data-ttu-id="5ec08-1334">コントロールのユーザー プロンプト テキストとして割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1334">The value to assign as the user prompt text for the control.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="5ec08-1335">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="5ec08-1335">Return Value - userPromptText</span></span>

<span data-ttu-id="5ec08-1336">コントロールのユーザー プロンプト テキスト。コントロールにユーザー プロンプト テキストが割り当てられていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1336">The user prompt text for the control; an empty string if no user prompt text is assigned to the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="5ec08-1337">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5ec08-1337">Method userSecurityLevel</span></span>

<span data-ttu-id="5ec08-1338">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1338">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="5ec08-1339">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5ec08-1339">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="5ec08-1340">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1340">value</span></span>  
<span data-ttu-id="5ec08-1341">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1341">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="5ec08-1342">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5ec08-1342">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="5ec08-1343">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1343">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="5ec08-1344">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1344">Method userSkip</span></span>

<span data-ttu-id="5ec08-1345">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1345">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="5ec08-1346">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1346">Parameters - userSkip</span></span>

<span data-ttu-id="5ec08-1347">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1347">value</span></span>  
<span data-ttu-id="5ec08-1348">userSkip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1348">The value to assign to the userSkip property.</span></span> <span data-ttu-id="5ec08-1349">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合の値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1349">The value is 1 if the user setting to skip the control is in effect; otherwise, the value is 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="5ec08-1350">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1350">Return Value - userSkip</span></span>

<span data-ttu-id="5ec08-1351">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1351">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="examples---userskip"></a><span data-ttu-id="5ec08-1352">例 - userSkip</span><span class="sxs-lookup"><span data-stu-id="5ec08-1352">Examples - userSkip</span></span>

<span data-ttu-id="5ec08-1353">次の例は、userSkip プロパティを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1353">The following example shows how to return and set the userSkip property.</span></span>

```xpp
int nUserSkip 
// The ctrl variable was previously assigned 
// as a FormTreeControl value. 
// Return the userSkip property. 
nUserSkip = ctrl.userSkip(); 
// Set the userSkip property. 
ctrl.userSkip(1);
```

## <a name="method-userwidth"></a><span data-ttu-id="5ec08-1354">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="5ec08-1354">Method userWidth</span></span>

<span data-ttu-id="5ec08-1355">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1355">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="5ec08-1356">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="5ec08-1356">Parameters - userWidth</span></span>

<span data-ttu-id="5ec08-1357">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1357">value</span></span>  
<span data-ttu-id="5ec08-1358">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1358">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="5ec08-1359">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="5ec08-1359">Return Value - userWidth</span></span>

<span data-ttu-id="5ec08-1360">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1360">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="5ec08-1361">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="5ec08-1361">Remarks - userWidth</span></span>

<span data-ttu-id="5ec08-1362">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1362">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="5ec08-1363">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1363">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="5ec08-1364">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1364">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

### <a name="examples---userwidth"></a><span data-ttu-id="5ec08-1365">例 - userWidth</span><span class="sxs-lookup"><span data-stu-id="5ec08-1365">Examples - userWidth</span></span>

<span data-ttu-id="5ec08-1366">次の例は、フォーム ツリー コントロールのユーザーの幅を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1366">The following example shows how to return and set the user width of a form tree control.</span></span>

```xpp
int nWidth; 
// The ctrl variable was previously defined 
// as a FormTreeControl value. 
// Return the width. 
nWidth = ctrl.userWidth(); 
// Specify the width. 
ctrl.userWidth(90);  // 15 characters * 6 pixels == 90
```

## <a name="method-verticalspacing"></a><span data-ttu-id="5ec08-1367">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="5ec08-1367">Method verticalSpacing</span></span>

<span data-ttu-id="5ec08-1368">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1368">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="5ec08-1369">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="5ec08-1369">Parameters - verticalSpacing</span></span>

<span data-ttu-id="5ec08-1370">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1370">value</span></span>  
<span data-ttu-id="5ec08-1371">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1371">An integer value that indicates the AutoMode value for the control; optional.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1372">モード</span><span class="sxs-lookup"><span data-stu-id="5ec08-1372">mode</span></span>  
<span data-ttu-id="5ec08-1373">コントロールの AutoMode 値を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1373">An integer value that indicates the AutoMode value for the control; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="5ec08-1374">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="5ec08-1374">Return Value - verticalSpacing</span></span>

<span data-ttu-id="5ec08-1375">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1375">The vertical spacing of the control in the form.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="5ec08-1376">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1376">Method verticalSpacingMode</span></span>

<span data-ttu-id="5ec08-1377">フォームのコントロールの垂直スペーシング モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1377">Sets the vertical spacing mode for the control in the form.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="5ec08-1378">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1378">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="5ec08-1379">モード</span><span class="sxs-lookup"><span data-stu-id="5ec08-1379">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="5ec08-1380">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1380">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="5ec08-1381">フォームのコントロールの垂直スペーシング モード。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1381">The vertical spacing mode for the control in the form.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="5ec08-1382">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1382">Method verticalSpacingValue</span></span>

<span data-ttu-id="5ec08-1383">フォームのコントロールの上下の間隔を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1383">Gets or sets the vertical spacing of the control in the form.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="5ec08-1384">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1384">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="5ec08-1385">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1385">value</span></span>  
<span data-ttu-id="5ec08-1386">コントロールの上下の間隔を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1386">An integer value that indicates the vertical spacing of the control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="5ec08-1387">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1387">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="5ec08-1388">フォームのコントロールの垂直スペーシング。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1388">The vertical spacing of the control in the form.</span></span>

## <a name="method-visible"></a><span data-ttu-id="5ec08-1389">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="5ec08-1389">Method visible</span></span>

<span data-ttu-id="5ec08-1390">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1390">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="5ec08-1391">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="5ec08-1391">Parameters - visible</span></span>

<span data-ttu-id="5ec08-1392">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1392">value</span></span>  
<span data-ttu-id="5ec08-1393">コントロールの可視化設定に割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1393">The value to assign to the visibility setting for the control.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="5ec08-1394">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="5ec08-1394">Return Value - visible</span></span>

<span data-ttu-id="5ec08-1395">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1395">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="5ec08-1396">メソッド width</span><span class="sxs-lookup"><span data-stu-id="5ec08-1396">Method width</span></span>

<span data-ttu-id="5ec08-1397">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1397">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="5ec08-1398">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="5ec08-1398">Parameters - width</span></span>

<span data-ttu-id="5ec08-1399">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1399">value</span></span>  
<span data-ttu-id="5ec08-1400">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1400">An integer that indicates how the width is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1401">モード</span><span class="sxs-lookup"><span data-stu-id="5ec08-1401">mode</span></span>  
<span data-ttu-id="5ec08-1402">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1402">An integer that indicates how the width is calculated; optional.</span></span>

### <a name="return-value---width"></a><span data-ttu-id="5ec08-1403">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="5ec08-1403">Return Value - width</span></span>

<span data-ttu-id="5ec08-1404">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1404">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="5ec08-1405">備考 - width</span><span class="sxs-lookup"><span data-stu-id="5ec08-1405">Remarks - width</span></span>

<span data-ttu-id="5ec08-1406">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1406">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="5ec08-1407">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1407">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="5ec08-1408">モード</span><span class="sxs-lookup"><span data-stu-id="5ec08-1408">Mode</span></span>             | <span data-ttu-id="5ec08-1409">幅計算</span><span class="sxs-lookup"><span data-stu-id="5ec08-1409">Width calculation</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec08-1410">-1 � 正確</span><span class="sxs-lookup"><span data-stu-id="5ec08-1410">-1 � Exact</span></span>       | <span data-ttu-id="5ec08-1411">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1411">The exact width of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="5ec08-1412">0 � 自動</span><span class="sxs-lookup"><span data-stu-id="5ec08-1412">0 � Auto</span></span>         | <span data-ttu-id="5ec08-1413">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1413">The width of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="5ec08-1414">1 � 列の幅</span><span class="sxs-lookup"><span data-stu-id="5ec08-1414">1 � Column width</span></span> | <span data-ttu-id="5ec08-1415">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1415">The layout of the form determines the width of the control.</span></span>                               |

<span data-ttu-id="5ec08-1416">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1416">The width and the width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="5ec08-1417">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1417">Method widthMode</span></span>

<span data-ttu-id="5ec08-1418">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1418">Gets or sets the calculation mode for the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="5ec08-1419">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1419">Parameters - widthMode</span></span>

<span data-ttu-id="5ec08-1420">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1420">value</span></span>  
<span data-ttu-id="5ec08-1421">コントロールの幅の計算方法を示す整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1421">An Integer data type value that indicates how control width is calculated.</span></span> <span data-ttu-id="5ec08-1422">この値は、 Exact モードの場合は -1、Auto モードの場合は 0、Column width モードの場合は 1 になります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1422">This value can be -1 for Exact mode, 0 for Auto mode, or 1 for Column width mode.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="5ec08-1423">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1423">Return Value - widthMode</span></span>

<span data-ttu-id="5ec08-1424">現在の幅の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1424">An integer value that indicates the current width calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="5ec08-1425">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1425">Remarks - widthMode</span></span>

<span data-ttu-id="5ec08-1426">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1426">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="5ec08-1427">モード</span><span class="sxs-lookup"><span data-stu-id="5ec08-1427">Mode</span></span>         | <span data-ttu-id="5ec08-1428">幅計算</span><span class="sxs-lookup"><span data-stu-id="5ec08-1428">Width calculation</span></span>                                                                         |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec08-1429">正確</span><span class="sxs-lookup"><span data-stu-id="5ec08-1429">Exact</span></span>        | <span data-ttu-id="5ec08-1430">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1430">The exact width of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="5ec08-1431">自動</span><span class="sxs-lookup"><span data-stu-id="5ec08-1431">Auto</span></span>         | <span data-ttu-id="5ec08-1432">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1432">The width of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="5ec08-1433">列の幅</span><span class="sxs-lookup"><span data-stu-id="5ec08-1433">Column width</span></span> | <span data-ttu-id="5ec08-1434">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1434">The layout of the form determines the width of the control.</span></span>                               |

<span data-ttu-id="5ec08-1435">計算モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1435">The width of the control might change when the calculation mode is set to Auto or Column width.</span></span>

### <a name="examples---widthmode"></a><span data-ttu-id="5ec08-1436">例 - widthMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1436">Examples - widthMode</span></span>

<span data-ttu-id="5ec08-1437">次の例は、フォーム ツリー コントロールの幅計算モードを返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1437">The following example shows how to return and set the width calculation mode for a form tree control.</span></span>

```xpp
int nWidthMode; 
// The ctrl variable was previously assigned 
// as a form tree control value. 
// Retrieve the width mode. 
nWidthMode = ctrl.widthMode (); 
// Set the width mode. 
ctrl.widthMode(-1); 
// Set the width. 
ctrl.widthValue(180);
```

## <a name="method-widthvalue"></a><span data-ttu-id="5ec08-1438">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1438">Method widthValue</span></span>

<span data-ttu-id="5ec08-1439">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1439">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="5ec08-1440">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1440">Parameters - widthValue</span></span>

<span data-ttu-id="5ec08-1441">値</span><span class="sxs-lookup"><span data-stu-id="5ec08-1441">value</span></span>  
<span data-ttu-id="5ec08-1442">幅をピクセル単位で指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1442">An Integer data type that specifies the width in pixels.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="5ec08-1443">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1443">Return Value - widthValue</span></span>

<span data-ttu-id="5ec08-1444">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1444">The width of the control in pixels.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="5ec08-1445">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1445">Remarks - widthValue</span></span>

<span data-ttu-id="5ec08-1446">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1446">To change the width of the control, use the Exact width calculation mode.</span></span>

### <a name="examples---widthvalue"></a><span data-ttu-id="5ec08-1447">例 - widthValue</span><span class="sxs-lookup"><span data-stu-id="5ec08-1447">Examples - widthValue</span></span>

<span data-ttu-id="5ec08-1448">次の例は、フォーム ツリー コントロールの幅の値を返して設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1448">The following example shows how to return and set the width value of a form tree control.</span></span>

```xpp
int nWidthValue; 
// The ctrl variable was previously assigned 
// as a form tree control value. 
// Retrieve the width value. 
nWidthValue = ctrl.widthValue(); 
// Set the width value. 
ctrl.widthMode(-1); 
ctrl.widthValue(160);
```

## <a name="method-checkedstatechanged"></a><span data-ttu-id="5ec08-1449">メソッド checkedStateChanged</span><span class="sxs-lookup"><span data-stu-id="5ec08-1449">Method checkedStateChanged</span></span>

```xpp
public void checkedStateChanged(int Idx, FormTreeCheckedState newState)
```

### <a name="parameters---checkedstatechanged"></a><span data-ttu-id="5ec08-1450">パラメーター - checkedStateChanged</span><span class="sxs-lookup"><span data-stu-id="5ec08-1450">Parameters - checkedStateChanged</span></span>

<span data-ttu-id="5ec08-1451">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1451">Idx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1452">newState</span><span class="sxs-lookup"><span data-stu-id="5ec08-1452">newState</span></span>  

## <a name="method-endlabeledit"></a><span data-ttu-id="5ec08-1453">メソッド endLabelEdit</span><span class="sxs-lookup"><span data-stu-id="5ec08-1453">Method endLabelEdit</span></span>

```xpp
public void endLabelEdit(int Idx, str text, AnyType data)
```

### <a name="parameters---endlabeledit"></a><span data-ttu-id="5ec08-1454">パラメーター - endLabelEdit</span><span class="sxs-lookup"><span data-stu-id="5ec08-1454">Parameters - endLabelEdit</span></span>

<span data-ttu-id="5ec08-1455">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1455">Idx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1456">テキスト</span><span class="sxs-lookup"><span data-stu-id="5ec08-1456">text</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1457">データ</span><span class="sxs-lookup"><span data-stu-id="5ec08-1457">data</span></span>  

## <a name="method-drop"></a><span data-ttu-id="5ec08-1458">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="5ec08-1458">Method drop</span></span>

<span data-ttu-id="5ec08-1459">ドロップ操作が現在のコントロールで実行されていることを示すために、drop イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1459">Raises the drop event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="5ec08-1460">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="5ec08-1460">Parameters - drop</span></span>

<span data-ttu-id="5ec08-1461">dragSource</span><span class="sxs-lookup"><span data-stu-id="5ec08-1461">dragSource</span></span>  
<span data-ttu-id="5ec08-1462">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1462">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1463">dragMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1463">dragMode</span></span>  
<span data-ttu-id="5ec08-1464">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1464">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1465">x</span><span class="sxs-lookup"><span data-stu-id="5ec08-1465">x</span></span>  
<span data-ttu-id="5ec08-1466">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1466">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1467">y</span><span class="sxs-lookup"><span data-stu-id="5ec08-1467">y</span></span>  
<span data-ttu-id="5ec08-1468">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1468">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-mouseenter"></a><span data-ttu-id="5ec08-1469">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="5ec08-1469">Method mouseEnter</span></span>

<span data-ttu-id="5ec08-1470">ユーザーがマウス ポインターをコントロールに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1470">Is called when the user moves the mouse pointer into the control.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="5ec08-1471">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="5ec08-1471">Parameters - mouseEnter</span></span>

<span data-ttu-id="5ec08-1472">x</span><span class="sxs-lookup"><span data-stu-id="5ec08-1472">x</span></span>  
<span data-ttu-id="5ec08-1473">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1473">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1474">y</span><span class="sxs-lookup"><span data-stu-id="5ec08-1474">y</span></span>  
<span data-ttu-id="5ec08-1475">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1475">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1476">ボタン</span><span class="sxs-lookup"><span data-stu-id="5ec08-1476">button</span></span>  
<span data-ttu-id="5ec08-1477">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1477">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1478">Ctrl</span><span class="sxs-lookup"><span data-stu-id="5ec08-1478">Ctrl</span></span>  
<span data-ttu-id="5ec08-1479">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1479">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1480">シフト</span><span class="sxs-lookup"><span data-stu-id="5ec08-1480">Shift</span></span>  
<span data-ttu-id="5ec08-1481">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1481">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="remarks---mouseenter"></a><span data-ttu-id="5ec08-1482">備考 - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="5ec08-1482">Remarks - mouseEnter</span></span>

<span data-ttu-id="5ec08-1483">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1483">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-onexpanding"></a><span data-ttu-id="5ec08-1484">メソッド OnExpanding</span><span class="sxs-lookup"><span data-stu-id="5ec08-1484">Method OnExpanding</span></span>

```xpp
private void OnExpanding([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onexpanding"></a><span data-ttu-id="5ec08-1485">パラメーター - OnExpanding</span><span class="sxs-lookup"><span data-stu-id="5ec08-1485">Parameters - OnExpanding</span></span>

<span data-ttu-id="5ec08-1486">sender</span><span class="sxs-lookup"><span data-stu-id="5ec08-1486">sender</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1487">e</span><span class="sxs-lookup"><span data-stu-id="5ec08-1487">e</span></span>  

## <a name="method-cut"></a><span data-ttu-id="5ec08-1488">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="5ec08-1488">Method cut</span></span>

<span data-ttu-id="5ec08-1489">コントロールのコンテンツを切り取りします。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1489">Cuts the contents of the control.</span></span>

```xpp
public void cut()
```

## <a name="method-paste"></a><span data-ttu-id="5ec08-1490">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="5ec08-1490">Method paste</span></span>

<span data-ttu-id="5ec08-1491">フォーム ツリー コントロールをフォームに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1491">Pastes the form tree control in the form.</span></span>

```xpp
public void paste()
```

## <a name="method-resetusersetting"></a><span data-ttu-id="5ec08-1492">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="5ec08-1492">Method resetUserSetting</span></span>

<span data-ttu-id="5ec08-1493">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1493">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-itemmoved"></a><span data-ttu-id="5ec08-1494">メソッド itemMoved</span><span class="sxs-lookup"><span data-stu-id="5ec08-1494">Method itemMoved</span></span>

```xpp
public void itemMoved(int OldIdx, int NewIdx)
```

### <a name="parameters---itemmoved"></a><span data-ttu-id="5ec08-1495">パラメーター - itemMoved</span><span class="sxs-lookup"><span data-stu-id="5ec08-1495">Parameters - itemMoved</span></span>

<span data-ttu-id="5ec08-1496">OldIdx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1496">OldIdx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1497">NewIdx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1497">NewIdx</span></span>  

## <a name="method-expanded"></a><span data-ttu-id="5ec08-1498">パラメーター - expand</span><span class="sxs-lookup"><span data-stu-id="5ec08-1498">Method expanded</span></span>

```xpp
public void expanded(int Idx, FormTreeExpand action, AnyType data)
```

### <a name="parameters---expanded"></a><span data-ttu-id="5ec08-1499">パラメーター - expanded</span><span class="sxs-lookup"><span data-stu-id="5ec08-1499">Parameters - expanded</span></span>

<span data-ttu-id="5ec08-1500">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1500">Idx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1501">アクション</span><span class="sxs-lookup"><span data-stu-id="5ec08-1501">action</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1502">データ</span><span class="sxs-lookup"><span data-stu-id="5ec08-1502">data</span></span>  

## <a name="method-setfocus"></a><span data-ttu-id="5ec08-1503">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="5ec08-1503">Method setFocus</span></span>

<span data-ttu-id="5ec08-1504">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1504">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-onselectionchanged"></a><span data-ttu-id="5ec08-1505">メソッド OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="5ec08-1505">Method OnSelectionChanged</span></span>

```xpp
private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanged"></a><span data-ttu-id="5ec08-1506">パラメーター - OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="5ec08-1506">Parameters - OnSelectionChanged</span></span>

<span data-ttu-id="5ec08-1507">sender</span><span class="sxs-lookup"><span data-stu-id="5ec08-1507">sender</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1508">e</span><span class="sxs-lookup"><span data-stu-id="5ec08-1508">e</span></span>  

## <a name="method-onlostfocus"></a><span data-ttu-id="5ec08-1509">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="5ec08-1509">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="5ec08-1510">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="5ec08-1510">Parameters - OnLostFocus</span></span>

<span data-ttu-id="5ec08-1511">sender</span><span class="sxs-lookup"><span data-stu-id="5ec08-1511">sender</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1512">e</span><span class="sxs-lookup"><span data-stu-id="5ec08-1512">e</span></span>  

## <a name="method-dropex"></a><span data-ttu-id="5ec08-1513">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1513">Method dropEx</span></span>

<span data-ttu-id="5ec08-1514">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1514">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="5ec08-1515">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1515">Parameters - dropEx</span></span>

<span data-ttu-id="5ec08-1516">dragSource</span><span class="sxs-lookup"><span data-stu-id="5ec08-1516">dragSource</span></span>  
<span data-ttu-id="5ec08-1517">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1517">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1518">dragMode</span><span class="sxs-lookup"><span data-stu-id="5ec08-1518">dragMode</span></span>  
<span data-ttu-id="5ec08-1519">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1519">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1520">x</span><span class="sxs-lookup"><span data-stu-id="5ec08-1520">x</span></span>  
<span data-ttu-id="5ec08-1521">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1521">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1522">y</span><span class="sxs-lookup"><span data-stu-id="5ec08-1522">y</span></span>  
<span data-ttu-id="5ec08-1523">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1523">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-mouseleave"></a><span data-ttu-id="5ec08-1524">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="5ec08-1524">Method mouseLeave</span></span>

<span data-ttu-id="5ec08-1525">ユーザーがマウス ポインターをコントロールから移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1525">Is called when the user moves the mouse pointer out of the control.</span></span>

```xpp
public void mouseLeave()
```

### <a name="examples---mouseleave"></a><span data-ttu-id="5ec08-1526">例 - mouseLeave</span><span class="sxs-lookup"><span data-stu-id="5ec08-1526">Examples - mouseLeave</span></span>

<span data-ttu-id="5ec08-1527">次の例では、マウス ポインタがコントロール エリアを離れるときに情報ログに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1527">The following example writes to the Infolog when the mouse pointer leaves the control area.</span></span>

```xpp
public void mouseLeave() 
{ 
    info (strfmt("The mouse has left the %1 control.", this.name()) ); 
    super(); 
}
```

## <a name="method-enddrag"></a><span data-ttu-id="5ec08-1528">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="5ec08-1528">Method endDrag</span></span>

<span data-ttu-id="5ec08-1529">ユーザーがフォーム ツリー コントロールのドラッグを終了すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1529">Is called when the user has finished dragging a form tree control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="5ec08-1530">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="5ec08-1530">Remarks - endDrag</span></span>

<span data-ttu-id="5ec08-1531">DragDrop プロパティがコントロールで有効で、beginDrag イベントがすでに開始されていない限り、このイベントは発生しません。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1531">This event is not raised unless the DragDrop property is enabled for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="5ec08-1532">コントロールをドラッグするには、コントロール領域内でマウス ボタンを押した後、マウス ポインターを移動します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1532">To drag a control, the user presses the mouse button in the control area and then moves the mouse pointer.</span></span>

### <a name="examples---enddrag"></a><span data-ttu-id="5ec08-1533">例 - endDrag</span><span class="sxs-lookup"><span data-stu-id="5ec08-1533">Examples - endDrag</span></span>

<span data-ttu-id="5ec08-1534">次の例では、ユーザーがツリー コントロールのドラッグを終了したときに、Infolog にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1534">The following example displays a message in the Infolog when the user has finished dragging the form tree control.</span></span>

```xpp
public void endDrag() 
{ 
    info("EndDrag completed"); 
    super(); 
}
```

## <a name="method-context"></a><span data-ttu-id="5ec08-1535">メソッド context</span><span class="sxs-lookup"><span data-stu-id="5ec08-1535">Method context</span></span>

<span data-ttu-id="5ec08-1536">コントロールのショートカット メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1536">Shows the shortcut menu for the control.</span></span>

```xpp
public void context()
```

## <a name="method-itemcopy"></a><span data-ttu-id="5ec08-1537">メソッド itemCopy</span><span class="sxs-lookup"><span data-stu-id="5ec08-1537">Method itemCopy</span></span>

```xpp
public void itemCopy(int OldIdx, int NewIdx)
```

### <a name="parameters---itemcopy"></a><span data-ttu-id="5ec08-1538">パラメーター - itemCopy</span><span class="sxs-lookup"><span data-stu-id="5ec08-1538">Parameters - itemCopy</span></span>

<span data-ttu-id="5ec08-1539">OldIdx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1539">OldIdx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1540">NewIdx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1540">NewIdx</span></span>  

## <a name="method-enter"></a><span data-ttu-id="5ec08-1541">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="5ec08-1541">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-inputsearch"></a><span data-ttu-id="5ec08-1542">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="5ec08-1542">Method inputSearch</span></span>

<span data-ttu-id="5ec08-1543">指定した文字列を基に、コントロールのデータ フィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1543">Performs data filtering for the control, based on the specified string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="5ec08-1544">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="5ec08-1544">Parameters - inputSearch</span></span>

<span data-ttu-id="5ec08-1545">searchStr</span><span class="sxs-lookup"><span data-stu-id="5ec08-1545">searchStr</span></span>  
<span data-ttu-id="5ec08-1546">データのフィルタリングに使用する文字列値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1546">The string value to use to filter data; optional.</span></span>

## <a name="method-displaycontrol"></a><span data-ttu-id="5ec08-1547">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="5ec08-1547">Method displayControl</span></span>

<span data-ttu-id="5ec08-1548">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1548">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-prefcolumnsize"></a><span data-ttu-id="5ec08-1549">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="5ec08-1549">Method prefColumnSize</span></span>

<span data-ttu-id="5ec08-1550">フォーム ツリー コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1550">Specifies the preferred column width and height for the form tree control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="5ec08-1551">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="5ec08-1551">Parameters - prefColumnSize</span></span>

<span data-ttu-id="5ec08-1552">width</span><span class="sxs-lookup"><span data-stu-id="5ec08-1552">width</span></span>  
<span data-ttu-id="5ec08-1553">コントロールの適切な高さはピクセルで測定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1553">The preferred height of the control measures in pixels.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1554">height</span><span class="sxs-lookup"><span data-stu-id="5ec08-1554">height</span></span>  
<span data-ttu-id="5ec08-1555">コントロールの適切な高さはピクセルで測定します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1555">The preferred height of the control measures in pixels.</span></span>

### <a name="examples---prefcolumnsize"></a><span data-ttu-id="5ec08-1556">例 - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="5ec08-1556">Examples - prefColumnSize</span></span>

<span data-ttu-id="5ec08-1557">次の例は、ツリー コントロールの優先幅と高さを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1557">The following example shows how to set the preferred width and height of a form tree control.</span></span>

```xpp
// The nWidth and nHeight variables were previously assigned 
// as int variables. 
// The ctrl variable was previously assigned 
// as a FormTreeControl value. 
ctrl.prefColumnSize( nWidth, nHeight);
```

## <a name="method-setimagelist"></a><span data-ttu-id="5ec08-1558">メソッド setImagelist</span><span class="sxs-lookup"><span data-stu-id="5ec08-1558">Method setImagelist</span></span>

```xpp
public void setImagelist(Imagelist imageList)
```

### <a name="parameters---setimagelist"></a><span data-ttu-id="5ec08-1559">パラメーター - setImagelist</span><span class="sxs-lookup"><span data-stu-id="5ec08-1559">Parameters - setImagelist</span></span>

<span data-ttu-id="5ec08-1560">imageList</span><span class="sxs-lookup"><span data-stu-id="5ec08-1560">imageList</span></span>  

## <a name="method-onexpanded"></a><span data-ttu-id="5ec08-1561">メソッド OnExpanded</span><span class="sxs-lookup"><span data-stu-id="5ec08-1561">Method OnExpanded</span></span>

```xpp
private void OnExpanded([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onexpanded"></a><span data-ttu-id="5ec08-1562">パラメーター - OnExpanded</span><span class="sxs-lookup"><span data-stu-id="5ec08-1562">Parameters - OnExpanded</span></span>

<span data-ttu-id="5ec08-1563">sender</span><span class="sxs-lookup"><span data-stu-id="5ec08-1563">sender</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1564">e</span><span class="sxs-lookup"><span data-stu-id="5ec08-1564">e</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="5ec08-1565">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="5ec08-1565">Method dragLeave</span></span>

<span data-ttu-id="5ec08-1566">マウス ドラッグ操作が現在のコントロールを離れることを示すために、dragLeave イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1566">Raises the dragLeave event to indicate that a mouse drag operation has left the current control.</span></span>

```xpp
public void dragLeave()
```

## <a name="method-lostfocus"></a><span data-ttu-id="5ec08-1567">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="5ec08-1567">Method lostFocus</span></span>

<span data-ttu-id="5ec08-1568">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1568">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-onenter"></a><span data-ttu-id="5ec08-1569">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="5ec08-1569">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="5ec08-1570">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="5ec08-1570">Parameters - OnEnter</span></span>

<span data-ttu-id="5ec08-1571">sender</span><span class="sxs-lookup"><span data-stu-id="5ec08-1571">sender</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1572">e</span><span class="sxs-lookup"><span data-stu-id="5ec08-1572">e</span></span>  

## <a name="method-itemdeleted"></a><span data-ttu-id="5ec08-1573">メソッド itemDeleted</span><span class="sxs-lookup"><span data-stu-id="5ec08-1573">Method itemDeleted</span></span>

```xpp
public void itemDeleted(int Idx, AnyType data)
```

### <a name="parameters---itemdeleted"></a><span data-ttu-id="5ec08-1574">パラメーター - itemDeleted</span><span class="sxs-lookup"><span data-stu-id="5ec08-1574">Parameters - itemDeleted</span></span>

<span data-ttu-id="5ec08-1575">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1575">Idx</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1576">データ</span><span class="sxs-lookup"><span data-stu-id="5ec08-1576">data</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="5ec08-1577">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="5ec08-1577">Method gotFocus</span></span>

<span data-ttu-id="5ec08-1578">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1578">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-setstateimagelist"></a><span data-ttu-id="5ec08-1579">メソッド setStateImagelist</span><span class="sxs-lookup"><span data-stu-id="5ec08-1579">Method setStateImagelist</span></span>

```xpp
public void setStateImagelist(Imagelist imageList)
```

### <a name="parameters---setstateimagelist"></a><span data-ttu-id="5ec08-1580">パラメーター - setStateImagelist</span><span class="sxs-lookup"><span data-stu-id="5ec08-1580">Parameters - setStateImagelist</span></span>

<span data-ttu-id="5ec08-1581">imageList</span><span class="sxs-lookup"><span data-stu-id="5ec08-1581">imageList</span></span>  

## <a name="method-endeditlabel"></a><span data-ttu-id="5ec08-1582">メソッド endEditLabel</span><span class="sxs-lookup"><span data-stu-id="5ec08-1582">Method endEditLabel</span></span>

```xpp
public void endEditLabel(boolean cancel)
```

### <a name="parameters---endeditlabel"></a><span data-ttu-id="5ec08-1583">パラメーター - endEditLabel</span><span class="sxs-lookup"><span data-stu-id="5ec08-1583">Parameters - endEditLabel</span></span>

<span data-ttu-id="5ec08-1584">キャンセル</span><span class="sxs-lookup"><span data-stu-id="5ec08-1584">cancel</span></span>  

## <a name="method-copy"></a><span data-ttu-id="5ec08-1585">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="5ec08-1585">Method copy</span></span>

<span data-ttu-id="5ec08-1586">フォーム ツリー コントロールをコピーします。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1586">Copies the form tree control.</span></span>

```xpp
public void copy()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="5ec08-1587">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="5ec08-1587">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="5ec08-1588">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="5ec08-1588">Parameters - OnGotFocus</span></span>

<span data-ttu-id="5ec08-1589">sender</span><span class="sxs-lookup"><span data-stu-id="5ec08-1589">sender</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1590">e</span><span class="sxs-lookup"><span data-stu-id="5ec08-1590">e</span></span>  

## <a name="method-registeroverridemethod"></a><span data-ttu-id="5ec08-1591">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="5ec08-1591">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="5ec08-1592">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="5ec08-1592">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="5ec08-1593">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="5ec08-1593">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1594">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="5ec08-1594">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1595">overrideObject</span><span class="sxs-lookup"><span data-stu-id="5ec08-1595">overrideObject</span></span>  

## <a name="method-onleaving"></a><span data-ttu-id="5ec08-1596">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="5ec08-1596">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="5ec08-1597">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="5ec08-1597">Parameters - OnLeaving</span></span>

<span data-ttu-id="5ec08-1598">sender</span><span class="sxs-lookup"><span data-stu-id="5ec08-1598">sender</span></span>  

<!-- -->

<span data-ttu-id="5ec08-1599">e</span><span class="sxs-lookup"><span data-stu-id="5ec08-1599">e</span></span>  

## <a name="method-selectionchanged"></a><span data-ttu-id="5ec08-1600">メソッド selectionChanged</span><span class="sxs-lookup"><span data-stu-id="5ec08-1600">Method selectionChanged</span></span>

<span data-ttu-id="5ec08-1601">ユーザーがフォーム ツリー コントロールで選択した項目を変更したことを示します。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1601">Indicates that the user has changed the selected item in the form tree control.</span></span>

```xpp
public void selectionChanged(FormTreeItem OldItem, FormTreeItem NewItem, FormTreeSelect how)
```

### <a name="parameters---selectionchanged"></a><span data-ttu-id="5ec08-1602">パラメーター - selectionChanged</span><span class="sxs-lookup"><span data-stu-id="5ec08-1602">Parameters - selectionChanged</span></span>

<span data-ttu-id="5ec08-1603">OldItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1603">OldItem</span></span>  
<span data-ttu-id="5ec08-1604">\_NewItem パラメーターで指定された項目がどのように選択されたかを示す値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1604">The value that indicates how the item that is specified by the \_NewItem parameter was selected.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1605">NewItem</span><span class="sxs-lookup"><span data-stu-id="5ec08-1605">NewItem</span></span>  
<span data-ttu-id="5ec08-1606">\_NewItem パラメーターで指定された項目がどのように選択されたかを示す値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1606">The value that indicates how the item that is specified by the \_NewItem parameter was selected.</span></span>

<!-- -->

<span data-ttu-id="5ec08-1607">how</span><span class="sxs-lookup"><span data-stu-id="5ec08-1607">how</span></span>  
<span data-ttu-id="5ec08-1608">\_NewItem パラメーターで指定された項目がどのように選択されたかを示す値。</span><span class="sxs-lookup"><span data-stu-id="5ec08-1608">The value that indicates how the item that is specified by the \_NewItem parameter was selected.</span></span>

## <a name="method-begineditlabel"></a><span data-ttu-id="5ec08-1609">メソッド beginEditLabel</span><span class="sxs-lookup"><span data-stu-id="5ec08-1609">Method beginEditLabel</span></span>

```xpp
public void beginEditLabel(int Idx)
```

### <a name="parameters---begineditlabel"></a><span data-ttu-id="5ec08-1610">パラメーター - beginEditLabel</span><span class="sxs-lookup"><span data-stu-id="5ec08-1610">Parameters - beginEditLabel</span></span>

<span data-ttu-id="5ec08-1611">Idx</span><span class="sxs-lookup"><span data-stu-id="5ec08-1611">Idx</span></span>  

