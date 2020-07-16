---
title: FormListControl クラス
description: このトピックでは、FormListControl クラスについて説明します。
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
ms.openlocfilehash: b81ba8891d59eca89781f5d650b48289ea74af53
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502936"
---
# <a name="class-formlistcontrol"></a><span data-ttu-id="50dbc-103">クラス FormListControl</span><span class="sxs-lookup"><span data-stu-id="50dbc-103">Class FormListControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormListControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="50dbc-104">備考</span><span class="sxs-lookup"><span data-stu-id="50dbc-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="50dbc-105">例</span><span class="sxs-lookup"><span data-stu-id="50dbc-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="50dbc-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="50dbc-106">Methods</span></span>

| <span data-ttu-id="50dbc-107">方法</span><span class="sxs-lookup"><span data-stu-id="50dbc-107">Method</span></span>                                                                                                      | <span data-ttu-id="50dbc-108">説明</span><span class="sxs-lookup"><span data-stu-id="50dbc-108">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50dbc-109">public int add(str Text, \[int image\], \[int index\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-109">public int add(str Text, \[int image\], \[int index\])</span></span>                                                      |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-110">public boolean addColumn(int Idx, FormListColumn Column)</span><span class="sxs-lookup"><span data-stu-id="50dbc-110">public boolean addColumn(int Idx, FormListColumn Column)</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-111">public int addItem(FormListItem item)</span><span class="sxs-lookup"><span data-stu-id="50dbc-111">public int addItem(FormListItem item)</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-112">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-112">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="50dbc-113">コントロールが他のコントロールと揃っているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-113">Determines whether the control is aligned with other controls.</span></span>                                                                                                          |
| <span data-ttu-id="50dbc-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="50dbc-115">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-115">Determines whether the user can modify the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="50dbc-116">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="50dbc-116">public boolean allowSysSetup()</span></span>                                                                              | <span data-ttu-id="50dbc-117">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-117">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>                                                                                     |
| <span data-ttu-id="50dbc-118">public boolean arrangeItem(FormListArrange ArrangeMethod)</span><span class="sxs-lookup"><span data-stu-id="50dbc-118">public boolean arrangeItem(FormListArrange ArrangeMethod)</span></span>                                                   |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-119">public boolean autoArrange(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-119">public boolean autoArrange(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-120">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-120">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="50dbc-121">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-121">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                                                      |
| <span data-ttu-id="50dbc-122">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-122">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="50dbc-123">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-123">Gets or sets the background color of the control.</span></span>                                                                                                                       |
| <span data-ttu-id="50dbc-124">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-124">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="50dbc-125">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-125">Determines whether the control background can be transparent.</span></span>                                                                                                           |
| <span data-ttu-id="50dbc-126">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="50dbc-126">public int beginDrag(int x, int y)</span></span>                                                                          | <span data-ttu-id="50dbc-127">ユーザーがフォーム リスト コントロールまたはフォーム リスト コントロールのアイテムの移動を開始するときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-127">Identifies when the user starts to move a form list control or an item in a form list control.</span></span>                                                                          |
| <span data-ttu-id="50dbc-128">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-128">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="50dbc-129">コントロール内のテキストに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-129">Gets or sets the font weight that is used fort text in the control.</span></span>                                                                                                     |
| <span data-ttu-id="50dbc-130">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-130">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="50dbc-131">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-131">Gets or sets the style of the borderline of the control.</span></span>                                                                                                                |
| <span data-ttu-id="50dbc-132">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="50dbc-132">public container calcControlSize(int chars, int lines)</span></span>                                                      | <span data-ttu-id="50dbc-133">文字数と明細行数に基づいて、フォームのリスト コントロールに使用されるフォント サイズを計算します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-133">Calculates the font size that is used for a form list control, based on the number of characters and the number of lines.</span></span>                                               |
| <span data-ttu-id="50dbc-134">public boolean canScroll(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-134">public boolean canScroll(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-135">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-135">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="50dbc-136">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-136">Gets or sets the character set of the font.</span></span>                                                                                                                             |
| <span data-ttu-id="50dbc-137">public boolean checkBox(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-137">public boolean checkBox(\[boolean value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-138">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-138">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="50dbc-139">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-139">Gets or sets the color scheme of the control.</span></span>                                                                                                                           |
| <span data-ttu-id="50dbc-140">public boolean columnHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-140">public boolean columnHeader(\[boolean value\])</span></span>                                                              | <span data-ttu-id="50dbc-141">フォーム リスト コントロールに列ヘッダーが含まれるかどうかを示すブール値データ型値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-141">Sets or gets a Boolean data type value that indicates whether a form list control has a column header.</span></span>                                                                  |
| <span data-ttu-id="50dbc-142">public boolean columnHeaderButton(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-142">public boolean columnHeaderButton(\[boolean value\])</span></span>                                                        | <span data-ttu-id="50dbc-143">フォーム リスト コントロールに列ヘッダー ボタンが含まれるかどうかを示すブール値データ型値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-143">Sets or gets a Boolean data type value that indicates whether a form list control has a column header button.</span></span>                                                           |
| <span data-ttu-id="50dbc-144">public boolean columnImages(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-144">public boolean columnImages(\[boolean value\])</span></span>                                                              | <span data-ttu-id="50dbc-145">フォーム リスト コントロールに列イメージが含まれるかどうかを示すブール値データ型値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-145">Sets or gets a Boolean data type value that indicates whether a form list control has column images.</span></span>                                                                    |
| <span data-ttu-id="50dbc-146">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-146">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="50dbc-147">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-147">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                                                     |
| <span data-ttu-id="50dbc-148">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="50dbc-148">public List configurationKeyEx()</span></span>                                                                            | <span data-ttu-id="50dbc-149">フォーム リスト コントロールのために有効化されたコンフィギュレーション キーの ID を含むリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-149">Retrieves a list that contains the IDs of configuration keys that are activated for a form list control.</span></span>                                                                |
| <span data-ttu-id="50dbc-150">public int copyItem(int Item, int InsertAt)</span><span class="sxs-lookup"><span data-stu-id="50dbc-150">public int copyItem(int Item, int InsertAt)</span></span>                                                                 | <span data-ttu-id="50dbc-151">指定した項目をフォーム リスト コントロールにコピーします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-151">Copies a specified item in a form list control.</span></span>                                                                                                                         |
| <span data-ttu-id="50dbc-152">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-152">public str countryRegionCodes(\[str value\])</span></span>                                                                | <span data-ttu-id="50dbc-153">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-153">Gets or sets the comma-separated list of country/region codes for the control.</span></span>                                                                                          |
| <span data-ttu-id="50dbc-154">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-154">public str dataRelationPath(\[str value\])</span></span>                                                                  | <span data-ttu-id="50dbc-155">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-155">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>                                           |
| <span data-ttu-id="50dbc-156">public boolean delete(int Idx)</span><span class="sxs-lookup"><span data-stu-id="50dbc-156">public boolean delete(int Idx)</span></span>                                                                              | <span data-ttu-id="50dbc-157">フォーム リスト コントロールから指定した項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-157">Deletes a specified item from a form list control.</span></span>                                                                                                                      |
| <span data-ttu-id="50dbc-158">public boolean deleteAll()</span><span class="sxs-lookup"><span data-stu-id="50dbc-158">public boolean deleteAll()</span></span>                                                                                  | <span data-ttu-id="50dbc-159">フォーム リスト コントロールからすべての項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-159">Deletes all the items from a form list control.</span></span>                                                                                                                         |
| <span data-ttu-id="50dbc-160">public boolean deleteColumn(int Idx)</span><span class="sxs-lookup"><span data-stu-id="50dbc-160">public boolean deleteColumn(int Idx)</span></span>                                                                        | <span data-ttu-id="50dbc-161">フォーム リスト コントロールの指定した列を削除します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-161">Deletes a specified column in a form list control.</span></span>                                                                                                                      |
| <span data-ttu-id="50dbc-162">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-162">public int displayTarget(\[int value\])</span></span>                                                                     | <span data-ttu-id="50dbc-163">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-163">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span> |
| <span data-ttu-id="50dbc-164">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-164">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="50dbc-165">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-165">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                                                       |
| <span data-ttu-id="50dbc-166">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="50dbc-166">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                           | <span data-ttu-id="50dbc-167">ユーザーがフォーム リスト コントロールの境界内のアイテムにオブジェクトをドラッグするときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-167">Identifies when a user drags an object over an item within the bounds of a form list control.</span></span>                                                                           |
| <span data-ttu-id="50dbc-168">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="50dbc-168">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                               | <span data-ttu-id="50dbc-169">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-169">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>                                                                        |
| <span data-ttu-id="50dbc-170">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="50dbc-170">public str dragText()</span></span>                                                                                       | <span data-ttu-id="50dbc-171">フォーム リスト コントロールでユーザーが項目をドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-171">Retrieves the text that is displayed when a user drags an item in a form list control.</span></span>                                                                                  |
| <span data-ttu-id="50dbc-172">public boolean editLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-172">public boolean editLabels(\[boolean value\])</span></span>                                                                | <span data-ttu-id="50dbc-173">ユーザーがフォーム リスト コントロールで項目名を変更できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-173">Indicates whether users can modify item names in a form list control.</span></span>                                                                                                   |
| <span data-ttu-id="50dbc-174">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-174">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="50dbc-175">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-175">Determines whether to enable or disable the object.</span></span>                                                                                                                     |
| <span data-ttu-id="50dbc-176">public int ensureVisible(int Idx)</span><span class="sxs-lookup"><span data-stu-id="50dbc-176">public int ensureVisible(int Idx)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-177">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-177">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="50dbc-178">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-178">Gets or sets the name of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="50dbc-179">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-179">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="50dbc-180">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-180">Gets or sets the size of the font for the control to use.</span></span>                                                                                                               |
| <span data-ttu-id="50dbc-181">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-181">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="50dbc-182">コントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-182">Gets or sets the text color for the control.</span></span>                                                                                                                            |
| <span data-ttu-id="50dbc-183">public FormListColumn getColumn(int Idx)</span><span class="sxs-lookup"><span data-stu-id="50dbc-183">public FormListColumn getColumn(int Idx)</span></span>                                                                    | <span data-ttu-id="50dbc-184">フォーム リスト コントロール内の指定された列の FormListColumn オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-184">Retrieves a FormListColumn object for a specified column in a form list control.</span></span>                                                                                        |
| <span data-ttu-id="50dbc-185">public int getColumnCount()</span><span class="sxs-lookup"><span data-stu-id="50dbc-185">public int getColumnCount()</span></span>                                                                                 | <span data-ttu-id="50dbc-186">フォーム リスト コントロール内の列の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-186">Retrieves the number of columns in a form list control.</span></span>                                                                                                                 |
| <span data-ttu-id="50dbc-187">public int getColumnWidth(int Idx)</span><span class="sxs-lookup"><span data-stu-id="50dbc-187">public int getColumnWidth(int Idx)</span></span>                                                                          | <span data-ttu-id="50dbc-188">フォーム リスト コントロール内の列の幅を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-188">Retrieves the width of a column in a form list control.</span></span>                                                                                                                 |
| <span data-ttu-id="50dbc-189">public int getCount()</span><span class="sxs-lookup"><span data-stu-id="50dbc-189">public int getCount()</span></span>                                                                                       | <span data-ttu-id="50dbc-190">フォーム リスト コントロールに含まれる項目の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-190">Retrieves the number of items that are contained in a form list control.</span></span>                                                                                                |
| <span data-ttu-id="50dbc-191">public int getCountPerPage()</span><span class="sxs-lookup"><span data-stu-id="50dbc-191">public int getCountPerPage()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-192">public Imagelist getImagelist(\[boolean GetLarge\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-192">public Imagelist getImagelist(\[boolean GetLarge\])</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-193">public FormListItem getItem(int Idx, \[int SubItem\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-193">public FormListItem getItem(int Idx, \[int SubItem\])</span></span>                                                       | <span data-ttu-id="50dbc-194">フォーム リスト コントロール内の項目の FormListItem オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-194">Retrieves a FormListItem object for an item in a form list control.</span></span>                                                                                                     |
| <span data-ttu-id="50dbc-195">public container getItemPos(int Item)</span><span class="sxs-lookup"><span data-stu-id="50dbc-195">public container getItemPos(int Item)</span></span>                                                                       | <span data-ttu-id="50dbc-196">フォーム リスト コントロール内の項目の位置を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-196">Retrieves the position of an item in a form list control.</span></span>                                                                                                               |
| <span data-ttu-id="50dbc-197">public int getNextItem(FormListNext nextType, \[int startIdx\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-197">public int getNextItem(FormListNext nextType, \[int startIdx\])</span></span>                                             | <span data-ttu-id="50dbc-198">フォーム リスト コントロール内の次の項目の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-198">Retrieves the number of the next item in a form list control.</span></span>                                                                                                           |
| <span data-ttu-id="50dbc-199">public int getSelectedCount()</span><span class="sxs-lookup"><span data-stu-id="50dbc-199">public int getSelectedCount()</span></span>                                                                               | <span data-ttu-id="50dbc-200">フォーム リスト コントロールで選択されている項目の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-200">Retrieves the number of items that are selected in a form list control.</span></span>                                                                                                 |
| <span data-ttu-id="50dbc-201">public int getStringWidth(str Text)</span><span class="sxs-lookup"><span data-stu-id="50dbc-201">public int getStringWidth(str Text)</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-202">public int getTopIndex()</span><span class="sxs-lookup"><span data-stu-id="50dbc-202">public int getTopIndex()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-203">public boolean gridLines(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-203">public boolean gridLines(\[boolean value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-204">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-204">public boolean hasChanged(\[boolean val\])</span></span>                                                                  | <span data-ttu-id="50dbc-205">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-205">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>                                                                                |
| <span data-ttu-id="50dbc-206">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="50dbc-206">public boolean hasUserSetting()</span></span>                                                                             | <span data-ttu-id="50dbc-207">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-207">Indicates whether the control has custom user settings.</span></span>                                                                                                                 |
| <span data-ttu-id="50dbc-208">public boolean headerdragdrop(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-208">public boolean headerdragdrop(\[boolean value\])</span></span>                                                            |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-209">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-209">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="50dbc-210">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-210">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="50dbc-211">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-211">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="50dbc-212">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-212">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                                          |
| <span data-ttu-id="50dbc-213">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-213">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="50dbc-214">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-214">Gets or sets the height of the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="50dbc-215">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="50dbc-215">public str helpField()</span></span>                                                                                      | <span data-ttu-id="50dbc-216">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-216">Retrieves the Help text for the control.</span></span>                                                                                                                                |
| <span data-ttu-id="50dbc-217">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-217">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="50dbc-218">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-218">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                                                |
| <span data-ttu-id="50dbc-219">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-219">public str hierarchyParent(\[str value\])</span></span>                                                                   | <span data-ttu-id="50dbc-220">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-220">Gets or sets the HierarchyParent property value of the control.</span></span>                                                                                                         |
| <span data-ttu-id="50dbc-221">public container hitTest(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="50dbc-221">public container hitTest(int x, int y)</span></span>                                                                      |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-222">public container hitTestSubItem(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="50dbc-222">public container hitTestSubItem(int x, int y)</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-223">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="50dbc-223">public int hWnd()</span></span>                                                                                           | <span data-ttu-id="50dbc-224">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-224">Retrieves the Windows handle for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="50dbc-225">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="50dbc-225">public boolean isContainer()</span></span>                                                                                |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-226">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="50dbc-226">public boolean isDisplayed()</span></span>                                                                                | <span data-ttu-id="50dbc-227">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-227">Retrieves a value that indicates whether the control is displayed.</span></span>                                                                                                      |
| <span data-ttu-id="50dbc-228">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="50dbc-228">public boolean isRestricted()</span></span>                                                                               | <span data-ttu-id="50dbc-229">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-229">Retrieves a value that indicates whether the control is restricted.</span></span>                                                                                                     |
| <span data-ttu-id="50dbc-230">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="50dbc-230">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                    | <span data-ttu-id="50dbc-231">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-231">Gets a value that indicates whether the control allows for the specified level of customization.</span></span>                                                                        |
| <span data-ttu-id="50dbc-232">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-232">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-233">public int itemAlign(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-233">public int itemAlign(\[int value\])</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-234">public boolean itemChanging(int Idx, AnyType Data)</span><span class="sxs-lookup"><span data-stu-id="50dbc-234">public boolean itemChanging(int Idx, AnyType Data)</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-235">public boolean keyDown(int vKey, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="50dbc-235">public boolean keyDown(int vKey, boolean Ctrl, boolean Shift)</span></span>                                               |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-236">public boolean leave()</span><span class="sxs-lookup"><span data-stu-id="50dbc-236">public boolean leave()</span></span>                                                                                      | <span data-ttu-id="50dbc-237">ユーザーがフォーム リスト コントロールからフォーカスを移動したら識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-237">Identifies when a user moves focus away from a form list control.</span></span>                                                                                                       |
| <span data-ttu-id="50dbc-238">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-238">public int left(int value, \[int mode\])</span></span>                                                                    | <span data-ttu-id="50dbc-239">フォーム リスト コントロールの水平位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-239">Sets or returns the horizontal position of a form list control in pixels, and specifies how the position is calculated.</span></span>                                                 |
| <span data-ttu-id="50dbc-240">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-240">public int leftMode(\[int value\])</span></span>                                                                          | <span data-ttu-id="50dbc-241">フォーム リスト コントロールの水平位置を計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-241">Sets or returns a value that indicates how the horizontal position of a form list control is calculated.</span></span>                                                                |
| <span data-ttu-id="50dbc-242">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-242">public int leftValue(\[int value\])</span></span>                                                                         | <span data-ttu-id="50dbc-243">フォーム リスト コントロールの水平位置をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-243">Sets or returns the horizontal position of a form list control in pixels.</span></span>                                                                                               |
| <span data-ttu-id="50dbc-244">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-244">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                             | <span data-ttu-id="50dbc-245">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-245">Marks or unmarks the control as a user-added control.</span></span>                                                                                                                   |
| <span data-ttu-id="50dbc-246">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="50dbc-246">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                             | <span data-ttu-id="50dbc-247">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-247">Is called when the control is double-clicked by the user.</span></span>                                                                                                               |
| <span data-ttu-id="50dbc-248">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="50dbc-248">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="50dbc-249">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-249">Is called when the user clicks the mouse button over the control.</span></span>                                                                                                       |
| <span data-ttu-id="50dbc-250">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="50dbc-250">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                 | <span data-ttu-id="50dbc-251">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-251">Is called when the user moves the mouse pointer over the control.</span></span>                                                                                                       |
| <span data-ttu-id="50dbc-252">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="50dbc-252">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                   | <span data-ttu-id="50dbc-253">ユーザーがマウスの左ボタンが押すときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-253">Identifies when a user presses the left mouse button.</span></span>                                                                                                                   |
| <span data-ttu-id="50dbc-254">public int moveItem(int Item, int InsertAt)</span><span class="sxs-lookup"><span data-stu-id="50dbc-254">public int moveItem(int Item, int InsertAt)</span></span>                                                                 | <span data-ttu-id="50dbc-255">指定した項目をフォーム リスト コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-255">Moves a specified item in a form list control.</span></span>                                                                                                                          |
| <span data-ttu-id="50dbc-256">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-256">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="50dbc-257">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-257">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>                                 |
| <span data-ttu-id="50dbc-258">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-258">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-259">public boolean oneClickActivate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-259">public boolean oneClickActivate(\[boolean value\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-260">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="50dbc-260">public container SysObsoleteAttribute()</span></span>                                                                     |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-261">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="50dbc-261">public FormControl parentControl()</span></span>                                                                          | <span data-ttu-id="50dbc-262">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-262">Retrieves the parent control for the control.</span></span>                                                                                                                           |
| <span data-ttu-id="50dbc-263">public boolean redrawItems(int idxFirst, int idxLast)</span><span class="sxs-lookup"><span data-stu-id="50dbc-263">public boolean redrawItems(int idxFirst, int idxLast)</span></span>                                                       | <span data-ttu-id="50dbc-264">フォーム リスト コントロール内の広範囲の項目を更新します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-264">Updates a range of items in a form list control.</span></span>                                                                                                                        |
| <span data-ttu-id="50dbc-265">public boolean rowSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-265">public boolean rowSelect(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="50dbc-266">行をクリックしたときにフォーム リスト コントロールの行が選択されているかどうかを示すブール値データ型値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-266">Sets or gets a Boolean data type value that indicates whether a row in a form list control is selected when the row is clicked.</span></span>                                         |
| <span data-ttu-id="50dbc-267">public boolean scroll(int dx, int dy)</span><span class="sxs-lookup"><span data-stu-id="50dbc-267">public boolean scroll(int dx, int dy)</span></span>                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-268">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-268">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   | <span data-ttu-id="50dbc-269">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-269">Sets or returns the ID of the security key for the control.</span></span>                                                                                                             |
| <span data-ttu-id="50dbc-270">public boolean selectionChanging(int Idx, AnyType Data)</span><span class="sxs-lookup"><span data-stu-id="50dbc-270">public boolean selectionChanging(int Idx, AnyType Data)</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-271">public boolean setColumn(int Idx, FormListColumn Column)</span><span class="sxs-lookup"><span data-stu-id="50dbc-271">public boolean setColumn(int Idx, FormListColumn Column)</span></span>                                                    |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-272">public boolean setColumnWidth(int Idx, int Width)</span><span class="sxs-lookup"><span data-stu-id="50dbc-272">public boolean setColumnWidth(int Idx, int Width)</span></span>                                                           | <span data-ttu-id="50dbc-273">フォーム リスト コントロール内の列の幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-273">Specifies the width of a column in a form list control.</span></span>                                                                                                                 |
| <span data-ttu-id="50dbc-274">public boolean setItem(FormListItem item)</span><span class="sxs-lookup"><span data-stu-id="50dbc-274">public boolean setItem(FormListItem item)</span></span>                                                                   | <span data-ttu-id="50dbc-275">フォーム リスト コントロールに項目が含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-275">Indicates whether an item is contained in a form list control.</span></span>                                                                                                          |
| <span data-ttu-id="50dbc-276">public Imagelist setStateImagelist(Imagelist imageList)</span><span class="sxs-lookup"><span data-stu-id="50dbc-276">public Imagelist setStateImagelist(Imagelist imageList)</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-277">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="50dbc-277">public int showContextMenu(int menuHandle)</span></span>                                                                  | <span data-ttu-id="50dbc-278">ショートカット メニューがいつ表示されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-278">Identifies when a shortcut menu appears.</span></span>                                                                                                                                |
| <span data-ttu-id="50dbc-279">public boolean showSelAlways(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-279">public boolean showSelAlways(\[boolean value\])</span></span>                                                             |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-280">public boolean singleSelection(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-280">public boolean singleSelection(\[boolean value\])</span></span>                                                           | <span data-ttu-id="50dbc-281">フォーム リスト コントロールで複数の項目を選択できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-281">Indicates whether multiple items can be selected in a form list control.</span></span>                                                                                                |
| <span data-ttu-id="50dbc-282">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-282">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="50dbc-283">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-283">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>                                         |
| <span data-ttu-id="50dbc-284">public int sort(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-284">public int sort(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-285">public boolean sortTextItems(\[int column\], \[boolean ascending\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-285">public boolean sortTextItems(\[int column\], \[boolean ascending\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-286">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="50dbc-286">public str toolTip()</span></span>                                                                                        | <span data-ttu-id="50dbc-287">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-287">Retrieves the tooltip text for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="50dbc-288">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-288">public int top(int value, \[int mode\])</span></span>                                                                     | <span data-ttu-id="50dbc-289">フォーム リスト コントロールの垂直位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-289">Sets or returns the vertical position of a form list control in pixels, and specifies how the position is calculated.</span></span>                                                   |
| <span data-ttu-id="50dbc-290">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-290">public int topMode(\[int value\])</span></span>                                                                           | <span data-ttu-id="50dbc-291">フォーム リスト コントロールの垂直位置を計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-291">Sets or returns a value that indicates how the vertical position for a form list control is calculated.</span></span>                                                                 |
| <span data-ttu-id="50dbc-292">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-292">public int topValue(\[int value\])</span></span>                                                                          | <span data-ttu-id="50dbc-293">フォーム リスト コントロールの垂直位置をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-293">Sets or returns the vertical position of a form list control in pixels.</span></span>                                                                                                 |
| <span data-ttu-id="50dbc-294">public boolean trackSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-294">public boolean trackSelect(\[boolean value\])</span></span>                                                               |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-295">public boolean twoClickActivate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-295">public boolean twoClickActivate(\[boolean value\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-296">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-296">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-297">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-297">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="50dbc-298">コントロール内のテキストの下線プロパティの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-298">Sets or returns the value of the underline property for the text in the control.</span></span>                                                                                        |
| <span data-ttu-id="50dbc-299">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="50dbc-299">public boolean SysObsoleteAttribute(container data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-300">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-300">public int userData(\[int value\])</span></span>                                                                          | <span data-ttu-id="50dbc-301">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-301">Gets or sets the user data for the control.</span></span>                                                                                                                             |
| <span data-ttu-id="50dbc-302">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-302">public int userDataItem(\[int value\])</span></span>                                                                      | <span data-ttu-id="50dbc-303">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-303">Gets or sets the user data item for the control.</span></span>                                                                                                                        |
| <span data-ttu-id="50dbc-304">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-304">public int userDataItems(\[int value\])</span></span>                                                                     | <span data-ttu-id="50dbc-305">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-305">Gets or sets the number of user data items for the control.</span></span>                                                                                                             |
| <span data-ttu-id="50dbc-306">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-306">public int userDisable(\[int value\])</span></span>                                                                       | <span data-ttu-id="50dbc-307">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-307">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>                                                                                     |
| <span data-ttu-id="50dbc-308">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-308">public int userHeight(\[int value\])</span></span>                                                                        | <span data-ttu-id="50dbc-309">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-309">Gets or sets the custom user height for the control.</span></span>                                                                                                                    |
| <span data-ttu-id="50dbc-310">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-310">public int userHide(\[int value\])</span></span>                                                                          | <span data-ttu-id="50dbc-311">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-311">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>                                                                                      |
| <span data-ttu-id="50dbc-312">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-312">public int userOrgContainer(\[int value\])</span></span>                                                                  | <span data-ttu-id="50dbc-313">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-313">Gets or sets the organization container for the control.</span></span>                                                                                                                |
| <span data-ttu-id="50dbc-314">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-314">public int userOrgSibling(\[int value\])</span></span>                                                                    | <span data-ttu-id="50dbc-315">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-315">Gets or sets the organization sibling for the control.</span></span>                                                                                                                  |
| <span data-ttu-id="50dbc-316">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-316">public str userPromptText(\[str value\])</span></span>                                                                    | <span data-ttu-id="50dbc-317">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-317">Gets or sets the user label text for the control.</span></span>                                                                                                                       |
| <span data-ttu-id="50dbc-318">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-318">public int userSecurityLevel(\[int value\])</span></span>                                                                 | <span data-ttu-id="50dbc-319">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-319">Gets or sets the user security level for the control.</span></span>                                                                                                                   |
| <span data-ttu-id="50dbc-320">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-320">public int userSkip(\[int value\])</span></span>                                                                          | <span data-ttu-id="50dbc-321">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-321">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>                    |
| <span data-ttu-id="50dbc-322">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-322">public int userWidth(\[int value\])</span></span>                                                                         | <span data-ttu-id="50dbc-323">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-323">Sets or returns the width of the control in pixels, as specified by the user.</span></span>                                                                                           |
| <span data-ttu-id="50dbc-324">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-324">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                | <span data-ttu-id="50dbc-325">ピクセルでフォーム リスト コントロールの上と下のスペースの量を設定または取得し、スペースを計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-325">Sets or gets the amount of space above and below a form list control in pixels, and specifies how the space is calculated.</span></span>                                              |
| <span data-ttu-id="50dbc-326">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-326">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      | <span data-ttu-id="50dbc-327">フォーム リスト コントロールの上と下のスペースを計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-327">Sets or returns a value that indicates how the space above and below a form list control is calculated.</span></span>                                                                 |
| <span data-ttu-id="50dbc-328">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-328">public int verticalSpacingValue(\[int value\])</span></span>                                                              | <span data-ttu-id="50dbc-329">ピクセルでフォーム リスト コントロールの上と下のスペースの量を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-329">Sets or returns the amount of space above and below a form list control in pixels.</span></span>                                                                                      |
| <span data-ttu-id="50dbc-330">public int viewType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-330">public int viewType(\[int value\])</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-331">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-331">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="50dbc-332">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-332">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="50dbc-333">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-333">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="50dbc-334">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-334">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="50dbc-335">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-335">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="50dbc-336">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-336">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                                          |
| <span data-ttu-id="50dbc-337">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-337">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="50dbc-338">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-338">Gets or sets the width of the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="50dbc-339">public void selectionChanged(int Idx, AnyType Data)</span><span class="sxs-lookup"><span data-stu-id="50dbc-339">public void selectionChanged(int Idx, AnyType Data)</span></span>                                                         |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-340">public void activateItem(int Idx)</span><span class="sxs-lookup"><span data-stu-id="50dbc-340">public void activateItem(int Idx)</span></span>                                                                           |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-341">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="50dbc-341">public void inputSearch(str searchStr)</span></span>                                                                      | <span data-ttu-id="50dbc-342">指定されたテキスト文字列の検索開始日を示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-342">Identifies when the search begins for a specified text string.</span></span>                                                                                                          |
| <span data-ttu-id="50dbc-343">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="50dbc-343">public void displayControl()</span></span>                                                                                | <span data-ttu-id="50dbc-344">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-344">Displays the control.</span></span>                                                                                                                                                   |
| <span data-ttu-id="50dbc-345">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-345">private void OnLeaving(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                  |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-346">public void update(\[int idx\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-346">public void update(\[int idx\])</span></span>                                                                             | <span data-ttu-id="50dbc-347">コントロールを更新します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-347">Updates the control.</span></span>                                                                                                                                                    |
| <span data-ttu-id="50dbc-348">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="50dbc-348">public void endDrag()</span></span>                                                                                       | <span data-ttu-id="50dbc-349">ユーザーがフォーム リスト コントロールの移動を終了した日を示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-349">Identifies when the user has finished moving a form list control.</span></span>                                                                                                       |
| <span data-ttu-id="50dbc-350">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="50dbc-350">public void mouseLeave()</span></span>                                                                                    | <span data-ttu-id="50dbc-351">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-351">Indicates that the mouse pointer has left the control.</span></span>                                                                                                                  |
| <span data-ttu-id="50dbc-352">public void setImagelist(Imagelist imageList, \[boolean SetLarge\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-352">public void setImagelist(Imagelist imageList, \[boolean SetLarge\])</span></span>                                         |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-353">public void copy()</span><span class="sxs-lookup"><span data-stu-id="50dbc-353">public void copy()</span></span>                                                                                          | <span data-ttu-id="50dbc-354">ユーザーがコピー操作を実行するときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-354">Identifies when a user performs a copy operation.</span></span>                                                                                                                       |
| <span data-ttu-id="50dbc-355">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="50dbc-355">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       | <span data-ttu-id="50dbc-356">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-356">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>                                                                    |
| <span data-ttu-id="50dbc-357">public void itemCopy(int Idx, int newIdx)</span><span class="sxs-lookup"><span data-stu-id="50dbc-357">public void itemCopy(int Idx, int newIdx)</span></span>                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-358">public void cut()</span><span class="sxs-lookup"><span data-stu-id="50dbc-358">public void cut()</span></span>                                                                                           | <span data-ttu-id="50dbc-359">ユーザーがカット操作を実行するときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-359">Identifies when the user performs a cut operation.</span></span>                                                                                                                      |
| <span data-ttu-id="50dbc-360">public void itemMoved(int Idx, int newIdx)</span><span class="sxs-lookup"><span data-stu-id="50dbc-360">public void itemMoved(int Idx, int newIdx)</span></span>                                                                  |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-361">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-361">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-362">public void paste()</span><span class="sxs-lookup"><span data-stu-id="50dbc-362">public void paste()</span></span>                                                                                         | <span data-ttu-id="50dbc-363">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-363">Pastes the contents of the clipboard into the control.</span></span>                                                                                                                  |
| <span data-ttu-id="50dbc-364">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="50dbc-364">public void lostFocus()</span></span>                                                                                     | <span data-ttu-id="50dbc-365">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-365">Indicates that the control has lost focus.</span></span>                                                                                                                              |
| <span data-ttu-id="50dbc-366">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-366">private void OnSelectionChanged(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                         |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-367">public void hotTrackItem(int Idx)</span><span class="sxs-lookup"><span data-stu-id="50dbc-367">public void hotTrackItem(int Idx)</span></span>                                                                           | <span data-ttu-id="50dbc-368">ユーザーがマウス ポインターをフォーム リスト コントロール上に移動するときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-368">Identifies when a user moves the mouse pointer over a form list control.</span></span>                                                                                                |
| <span data-ttu-id="50dbc-369">public void setCount(int count)</span><span class="sxs-lookup"><span data-stu-id="50dbc-369">public void setCount(int count)</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-370">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="50dbc-370">public void dragLeave()</span></span>                                                                                     | <span data-ttu-id="50dbc-371">ユーザーがフォーム リスト コントロールの境界からオブジェクトをドラッグするときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-371">Identifies when a user drags an object out of the bounds of a form list control.</span></span>                                                                                        |
| <span data-ttu-id="50dbc-372">public void itemDeleted(int Idx, AnyType Data)</span><span class="sxs-lookup"><span data-stu-id="50dbc-372">public void itemDeleted(int Idx, AnyType Data)</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-373">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="50dbc-373">public void prefColumnSize(int width, int height)</span></span>                                                           | <span data-ttu-id="50dbc-374">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-374">Specifies the preferred column width and height for the form control.</span></span>                                                                                                   |
| <span data-ttu-id="50dbc-375">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-375">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                 |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-376">public void setText(int Idx, str Text, \[int SubItem\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-376">public void setText(int Idx, str Text, \[int SubItem\])</span></span>                                                     |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-377">public void itemChanged(int Idx, AnyType Data)</span><span class="sxs-lookup"><span data-stu-id="50dbc-377">public void itemChanged(int Idx, AnyType Data)</span></span>                                                              |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-378">public void doubleClick()</span><span class="sxs-lookup"><span data-stu-id="50dbc-378">public void doubleClick()</span></span>                                                                                   | <span data-ttu-id="50dbc-379">ユーザーがフォーム内のリスト コントロールのアイテムをダブルクリックするときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-379">Identifies when a user double-clicks an item in a form list control.</span></span>                                                                                                    |
| <span data-ttu-id="50dbc-380">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="50dbc-380">public void resetUserSetting()</span></span>                                                                              | <span data-ttu-id="50dbc-381">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-381">Resets the user settings for the control.</span></span>                                                                                                                               |
| <span data-ttu-id="50dbc-382">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="50dbc-382">public void setFocus()</span></span>                                                                                      | <span data-ttu-id="50dbc-383">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-383">Sets the focus on the control.</span></span>                                                                                                                                          |
| <span data-ttu-id="50dbc-384">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="50dbc-384">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                               | <span data-ttu-id="50dbc-385">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-385">Is called when the user moves the mouse pointer into the control area.</span></span>                                                                                                  |
| <span data-ttu-id="50dbc-386">public void allItemsDeleted()</span><span class="sxs-lookup"><span data-stu-id="50dbc-386">public void allItemsDeleted()</span></span>                                                                               | <span data-ttu-id="50dbc-387">フォーム リスト コントロール内のすべてのアイテムが削除される日を示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-387">Identifies when all the items in a form list control are deleted.</span></span>                                                                                                       |
| <span data-ttu-id="50dbc-388">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="50dbc-388">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   | <span data-ttu-id="50dbc-389">ユーザーがフォーム リスト コントロールまたはフォーム リスト コントロールのアイテムを新しい位置にドロップするときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-389">Identifies when a user drops a form list control or an item in a form list control into a new position.</span></span>                                                                 |
| <span data-ttu-id="50dbc-390">public void columnClicked(int Column)</span><span class="sxs-lookup"><span data-stu-id="50dbc-390">public void columnClicked(int Column)</span></span>                                                                       | <span data-ttu-id="50dbc-391">ユーザーがフォーム内のリスト ビュー コントロールの列をクリックするときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-391">Identifies when a user clicks a column in a list view control in a form.</span></span>                                                                                                |
| <span data-ttu-id="50dbc-392">public void getStateImagelist()</span><span class="sxs-lookup"><span data-stu-id="50dbc-392">public void getStateImagelist()</span></span>                                                                             |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-393">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-393">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-394">public void setItemPos(int Item, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="50dbc-394">public void setItemPos(int Item, int x, int y)</span></span>                                                              | <span data-ttu-id="50dbc-395">フォーム リスト コントロール内の項目の位置を設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-395">Sets the position of an item in a form list control.</span></span>                                                                                                                    |
| <span data-ttu-id="50dbc-396">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="50dbc-396">public void gotFocus()</span></span>                                                                                      | <span data-ttu-id="50dbc-397">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-397">Indicates that the control has received focus.</span></span>                                                                                                                          |
| <span data-ttu-id="50dbc-398">public void enter()</span><span class="sxs-lookup"><span data-stu-id="50dbc-398">public void enter()</span></span>                                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-399">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="50dbc-399">private void OnEnter(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                    |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-400">public void context()</span><span class="sxs-lookup"><span data-stu-id="50dbc-400">public void context()</span></span>                                                                                       | <span data-ttu-id="50dbc-401">ユーザーがショートカット メニューをフォーム リスト コントロールで開くときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-401">Identifies when the user opens a shortcut menu in a form list control.</span></span>                                                                                                  |
| <span data-ttu-id="50dbc-402">public void beginEditLabel(int Idx)</span><span class="sxs-lookup"><span data-stu-id="50dbc-402">public void beginEditLabel(int Idx)</span></span>                                                                         |                                                                                                                                                                         |
| <span data-ttu-id="50dbc-403">public void itemInserted(int Idx, AnyType Data)</span><span class="sxs-lookup"><span data-stu-id="50dbc-403">public void itemInserted(int Idx, AnyType Data)</span></span>                                                             |                                                                                                                                                                         |

## <a name="method-add"></a><span data-ttu-id="50dbc-404">メソッド add</span><span class="sxs-lookup"><span data-stu-id="50dbc-404">Method add</span></span>

```xpp
public int add(str Text, [int image], [int index])
```

### <a name="parameters---add"></a><span data-ttu-id="50dbc-405">パラメーター - add</span><span class="sxs-lookup"><span data-stu-id="50dbc-405">Parameters - add</span></span>

<span data-ttu-id="50dbc-406">テキスト</span><span class="sxs-lookup"><span data-stu-id="50dbc-406">Text</span></span>  

<!-- -->

<span data-ttu-id="50dbc-407">画像</span><span class="sxs-lookup"><span data-stu-id="50dbc-407">image</span></span>  

<!-- -->

<span data-ttu-id="50dbc-408">指数</span><span class="sxs-lookup"><span data-stu-id="50dbc-408">index</span></span>  

### <a name="return-value---add"></a><span data-ttu-id="50dbc-409">戻り値 - add</span><span class="sxs-lookup"><span data-stu-id="50dbc-409">Return Value - add</span></span>

## <a name="method-addcolumn"></a><span data-ttu-id="50dbc-410">メソッド addColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-410">Method addColumn</span></span>

```xpp
public boolean addColumn(int Idx, FormListColumn Column)
```

### <a name="parameters---addcolumn"></a><span data-ttu-id="50dbc-411">パラメーター - addColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-411">Parameters - addColumn</span></span>

<span data-ttu-id="50dbc-412">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-412">Idx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-413">円柱</span><span class="sxs-lookup"><span data-stu-id="50dbc-413">Column</span></span>  

### <a name="return-value---addcolumn"></a><span data-ttu-id="50dbc-414">戻り値 - addColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-414">Return Value - addColumn</span></span>

## <a name="method-additem"></a><span data-ttu-id="50dbc-415">メソッド addItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-415">Method addItem</span></span>

```xpp
public int addItem(FormListItem item)
```

### <a name="parameters---additem"></a><span data-ttu-id="50dbc-416">パラメーター - addItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-416">Parameters - addItem</span></span>

<span data-ttu-id="50dbc-417">品目</span><span class="sxs-lookup"><span data-stu-id="50dbc-417">item</span></span>  

### <a name="return-value---additem"></a><span data-ttu-id="50dbc-418">戻り値 - addItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-418">Return Value - addItem</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="50dbc-419">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="50dbc-419">Method alignControl</span></span>

<span data-ttu-id="50dbc-420">コントロールが他のコントロールと揃っているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-420">Determines whether the control is aligned with other controls.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="50dbc-421">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="50dbc-421">Parameters - alignControl</span></span>

<span data-ttu-id="50dbc-422">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-422">value</span></span>  
<span data-ttu-id="50dbc-423">フォーム リスト コントロールが他のコントロールと一致しているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-423">A Boolean value that indicates whether a form list control is aligned with other controls.</span></span>

### <a name="return-value---aligncontrol"></a><span data-ttu-id="50dbc-424">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="50dbc-424">Return Value - alignControl</span></span>

<span data-ttu-id="50dbc-425">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-425">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="50dbc-426">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="50dbc-426">Remarks - alignControl</span></span>

<span data-ttu-id="50dbc-427">コントロールの左上隅は、最も長いラベルに基づいて配置されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-427">The upper-left corner of the control is aligned based on the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="50dbc-428">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="50dbc-428">Method allowEdit</span></span>

<span data-ttu-id="50dbc-429">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-429">Determines whether the user can modify the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="50dbc-430">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="50dbc-430">Parameters - allowEdit</span></span>

<span data-ttu-id="50dbc-431">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-431">value</span></span>  
<span data-ttu-id="50dbc-432">データを変更できるかどうかを示すブール値データ型。</span><span class="sxs-lookup"><span data-stu-id="50dbc-432">A Boolean data type that indicates whether data can be modified.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="50dbc-433">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="50dbc-433">Return Value - allowEdit</span></span>

<span data-ttu-id="50dbc-434">コントロールを変更することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-434">true if the control can be modified; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="50dbc-435">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="50dbc-435">Remarks - allowEdit</span></span>

<span data-ttu-id="50dbc-436">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-436">If this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="50dbc-437">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="50dbc-437">Method allowSysSetup</span></span>

<span data-ttu-id="50dbc-438">SysSetup フォームにコントロールを表示するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-438">Retrieves a value that indicates whether the control is shown in the SysSetup form.</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="50dbc-439">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="50dbc-439">Return Value - allowSysSetup</span></span>

<span data-ttu-id="50dbc-440">コントロールが SysSetup フォームに表示される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-440">true if the control is shown in the SysSetup form; otherwise, false.</span></span>

## <a name="method-arrangeitem"></a><span data-ttu-id="50dbc-441">メソッド arrangeItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-441">Method arrangeItem</span></span>

```xpp
public boolean arrangeItem(FormListArrange ArrangeMethod)
```

### <a name="parameters---arrangeitem"></a><span data-ttu-id="50dbc-442">パラメーター - arrangeItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-442">Parameters - arrangeItem</span></span>

<span data-ttu-id="50dbc-443">ArrangeMethod</span><span class="sxs-lookup"><span data-stu-id="50dbc-443">ArrangeMethod</span></span>  

### <a name="return-value---arrangeitem"></a><span data-ttu-id="50dbc-444">戻り値 - arrangeItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-444">Return Value - arrangeItem</span></span>

## <a name="method-autoarrange"></a><span data-ttu-id="50dbc-445">メソッド autoArrange</span><span class="sxs-lookup"><span data-stu-id="50dbc-445">Method autoArrange</span></span>

```xpp
public boolean autoArrange([boolean value])
```

### <a name="parameters---autoarrange"></a><span data-ttu-id="50dbc-446">パラメーター - autoArrange</span><span class="sxs-lookup"><span data-stu-id="50dbc-446">Parameters - autoArrange</span></span>

<span data-ttu-id="50dbc-447">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-447">value</span></span>  

### <a name="return-value---autoarrange"></a><span data-ttu-id="50dbc-448">戻り値 - autoArrange</span><span class="sxs-lookup"><span data-stu-id="50dbc-448">Return Value - autoArrange</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="50dbc-449">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="50dbc-449">Method autoDeclaration</span></span>

<span data-ttu-id="50dbc-450">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-450">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="50dbc-451">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="50dbc-451">Parameters - autoDeclaration</span></span>

<span data-ttu-id="50dbc-452">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-452">value</span></span>  
<span data-ttu-id="50dbc-453">システムがフォーム リスト コントロールと同じ名前の変数を宣言できるかどうかを示すブール データ型。</span><span class="sxs-lookup"><span data-stu-id="50dbc-453">A Boolean data type that indicates whether the system can declare a variable of the same name as a form list control.</span></span>

### <a name="return-value---autodeclaration"></a><span data-ttu-id="50dbc-454">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="50dbc-454">Return Value - autoDeclaration</span></span>

<span data-ttu-id="50dbc-455">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-455">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="50dbc-456">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="50dbc-456">Remarks - autoDeclaration</span></span>

<span data-ttu-id="50dbc-457">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-457">Controls cannot have identical names.</span></span>

### <a name="examples---autodeclaration"></a><span data-ttu-id="50dbc-458">例 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="50dbc-458">Examples - autoDeclaration</span></span>

<span data-ttu-id="50dbc-459">次の例は、システムがフォーム リスト コントロールと同じ名前を持つ変数を宣言できることを指定する autoDeclaration メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-459">The following example shows a call to the autoDeclaration method that specifies that the system can declare a variable that has the same name as a form list control.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.autoDeclaration(true); 
}
```

## <a name="method-backgroundcolor"></a><span data-ttu-id="50dbc-460">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="50dbc-460">Method backgroundColor</span></span>

<span data-ttu-id="50dbc-461">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-461">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="50dbc-462">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="50dbc-462">Parameters - backgroundColor</span></span>

<span data-ttu-id="50dbc-463">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-463">value</span></span>  
<span data-ttu-id="50dbc-464">背景色を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-464">An Integer data type that specifies the background color.</span></span>

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="50dbc-465">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="50dbc-465">Return Value - backgroundColor</span></span>

<span data-ttu-id="50dbc-466">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-466">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="50dbc-467">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="50dbc-467">Remarks - backgroundColor</span></span>

<span data-ttu-id="50dbc-468">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-468">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="50dbc-469">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-469">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="50dbc-470">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-470">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="50dbc-471">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-471">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="50dbc-472">上位バイトは 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-472">The high-order byte must be 0 (zero).</span></span>
-   <span data-ttu-id="50dbc-473">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-473">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="50dbc-474">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="50dbc-474">Method backStyle</span></span>

<span data-ttu-id="50dbc-475">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-475">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="50dbc-476">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="50dbc-476">Parameters - backStyle</span></span>

<span data-ttu-id="50dbc-477">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-477">value</span></span>  
<span data-ttu-id="50dbc-478">背景スタイルを示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-478">An Integer data type that indicates the background style.</span></span>

### <a name="return-value---backstyle"></a><span data-ttu-id="50dbc-479">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="50dbc-479">Return Value - backStyle</span></span>

<span data-ttu-id="50dbc-480">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-480">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="50dbc-481">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="50dbc-481">Method beginDrag</span></span>

<span data-ttu-id="50dbc-482">ユーザーがフォーム リスト コントロールまたはフォーム リスト コントロールのアイテムの移動を開始するときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-482">Identifies when the user starts to move a form list control or an item in a form list control.</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="50dbc-483">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="50dbc-483">Parameters - beginDrag</span></span>

<span data-ttu-id="50dbc-484">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-484">x</span></span>  
<span data-ttu-id="50dbc-485">移動イベントのための y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-485">An Integer data type that indicates the y-coordinate for the move event.</span></span>

<!-- -->

<span data-ttu-id="50dbc-486">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-486">y</span></span>  
<span data-ttu-id="50dbc-487">移動イベントのための y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-487">An Integer data type that indicates the y-coordinate for the move event.</span></span>

### <a name="return-value---begindrag"></a><span data-ttu-id="50dbc-488">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="50dbc-488">Return Value - beginDrag</span></span>

<span data-ttu-id="50dbc-489">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-489">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---begindrag"></a><span data-ttu-id="50dbc-490">備考 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="50dbc-490">Remarks - beginDrag</span></span>

<span data-ttu-id="50dbc-491">リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [beginDrag] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-491">To override this method on a list view control, right-click the Methods node below the control, point to Override Method, and then click beginDrag.</span></span> <span data-ttu-id="50dbc-492">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-492">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-bold"></a><span data-ttu-id="50dbc-493">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="50dbc-493">Method bold</span></span>

<span data-ttu-id="50dbc-494">コントロール内のテキストに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-494">Gets or sets the font weight that is used fort text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="50dbc-495">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="50dbc-495">Parameters - bold</span></span>

<span data-ttu-id="50dbc-496">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-496">value</span></span>  
<span data-ttu-id="50dbc-497">フォントの太さを指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-497">An Integer data type that specifies the font weight.</span></span>

### <a name="return-value---bold"></a><span data-ttu-id="50dbc-498">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="50dbc-498">Return Value - bold</span></span>

<span data-ttu-id="50dbc-499">0 (ゼロ) から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-499">An integer value between 0 (zero) and 9, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="50dbc-500">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="50dbc-500">Remarks - bold</span></span>

<span data-ttu-id="50dbc-501">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-501">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="50dbc-502">0 � 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-502">0 � Use the default font weight.</span></span>
-   <span data-ttu-id="50dbc-503">1 � シン。</span><span class="sxs-lookup"><span data-stu-id="50dbc-503">1 � Thin.</span></span>
-   <span data-ttu-id="50dbc-504">2 � エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="50dbc-504">2 � Extra-light.</span></span>
-   <span data-ttu-id="50dbc-505">3 � ライト。</span><span class="sxs-lookup"><span data-stu-id="50dbc-505">3 � Light.</span></span>
-   <span data-ttu-id="50dbc-506">4 � 標準。</span><span class="sxs-lookup"><span data-stu-id="50dbc-506">4 � Normal.</span></span>
-   <span data-ttu-id="50dbc-507">5 � 中。</span><span class="sxs-lookup"><span data-stu-id="50dbc-507">5 � Medium.</span></span>
-   <span data-ttu-id="50dbc-508">6 � セミボールド。</span><span class="sxs-lookup"><span data-stu-id="50dbc-508">6 � Semibold.</span></span>
-   <span data-ttu-id="50dbc-509">7 � 太字。</span><span class="sxs-lookup"><span data-stu-id="50dbc-509">7 � Bold.</span></span>
-   <span data-ttu-id="50dbc-510">8 � 極太。</span><span class="sxs-lookup"><span data-stu-id="50dbc-510">8 � Extra-bold.</span></span>
-   <span data-ttu-id="50dbc-511">9 � ヘビー。</span><span class="sxs-lookup"><span data-stu-id="50dbc-511">9 � Heavy.</span></span>

### <a name="examples---bold"></a><span data-ttu-id="50dbc-512">例 - bold</span><span class="sxs-lookup"><span data-stu-id="50dbc-512">Examples - bold</span></span>

<span data-ttu-id="50dbc-513">次の例は、フォントの重量を、重いことを示す、9 に設定する太字のメソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-513">The following example shows a call to the bold method to set the font weight to 9, which indicates heavy.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    int boldLevel; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    boldLevel = formListControl.bold(9); 
}
```

## <a name="method-border"></a><span data-ttu-id="50dbc-514">メソッド border</span><span class="sxs-lookup"><span data-stu-id="50dbc-514">Method border</span></span>

<span data-ttu-id="50dbc-515">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-515">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="50dbc-516">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="50dbc-516">Parameters - border</span></span>

<span data-ttu-id="50dbc-517">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-517">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="50dbc-518">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="50dbc-518">Return Value - border</span></span>

<span data-ttu-id="50dbc-519">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-519">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="50dbc-520">備考 - border</span><span class="sxs-lookup"><span data-stu-id="50dbc-520">Remarks - border</span></span>

<span data-ttu-id="50dbc-521">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-521">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="50dbc-522">先頭値</span><span class="sxs-lookup"><span data-stu-id="50dbc-522">Value</span></span> | <span data-ttu-id="50dbc-523">説明</span><span class="sxs-lookup"><span data-stu-id="50dbc-523">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="50dbc-524">0</span><span class="sxs-lookup"><span data-stu-id="50dbc-524">0</span></span>     | <span data-ttu-id="50dbc-525">自動</span><span class="sxs-lookup"><span data-stu-id="50dbc-525">Auto</span></span>        |
| <span data-ttu-id="50dbc-526">1</span><span class="sxs-lookup"><span data-stu-id="50dbc-526">1</span></span>     | <span data-ttu-id="50dbc-527">3D</span><span class="sxs-lookup"><span data-stu-id="50dbc-527">3D</span></span>          |
| <span data-ttu-id="50dbc-528">2</span><span class="sxs-lookup"><span data-stu-id="50dbc-528">2</span></span>     | <span data-ttu-id="50dbc-529">単一明細行</span><span class="sxs-lookup"><span data-stu-id="50dbc-529">Single line</span></span> |
| <span data-ttu-id="50dbc-530">3</span><span class="sxs-lookup"><span data-stu-id="50dbc-530">3</span></span>     | <span data-ttu-id="50dbc-531">均一</span><span class="sxs-lookup"><span data-stu-id="50dbc-531">Flat</span></span>        |
| <span data-ttu-id="50dbc-532">4</span><span class="sxs-lookup"><span data-stu-id="50dbc-532">4</span></span>     | <span data-ttu-id="50dbc-533">None</span><span class="sxs-lookup"><span data-stu-id="50dbc-533">None</span></span>        |

## <a name="method-calccontrolsize"></a><span data-ttu-id="50dbc-534">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="50dbc-534">Method calcControlSize</span></span>

<span data-ttu-id="50dbc-535">文字数と明細行数に基づいて、フォームのリスト コントロールに使用されるフォント サイズを計算します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-535">Calculates the font size that is used for a form list control, based on the number of characters and the number of lines.</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="50dbc-536">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="50dbc-536">Parameters - calcControlSize</span></span>

<span data-ttu-id="50dbc-537">chars</span><span class="sxs-lookup"><span data-stu-id="50dbc-537">chars</span></span>  
<span data-ttu-id="50dbc-538">行数を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-538">An Integer data type that specifies the number of lines.</span></span>

<!-- -->

<span data-ttu-id="50dbc-539">明細行</span><span class="sxs-lookup"><span data-stu-id="50dbc-539">lines</span></span>  
<span data-ttu-id="50dbc-540">行数を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-540">An Integer data type that specifies the number of lines.</span></span>

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="50dbc-541">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="50dbc-541">Return Value - calcControlSize</span></span>

<span data-ttu-id="50dbc-542">フォーム リスト コントロールのサイズを指定するコンテナー データ型値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-542">A Container data type value that specifies the size of a form list control.</span></span>

## <a name="method-canscroll"></a><span data-ttu-id="50dbc-543">メソッド canScroll</span><span class="sxs-lookup"><span data-stu-id="50dbc-543">Method canScroll</span></span>

```xpp
public boolean canScroll([boolean value])
```

### <a name="parameters---canscroll"></a><span data-ttu-id="50dbc-544">パラメーター - canScroll</span><span class="sxs-lookup"><span data-stu-id="50dbc-544">Parameters - canScroll</span></span>

<span data-ttu-id="50dbc-545">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-545">value</span></span>  

### <a name="return-value---canscroll"></a><span data-ttu-id="50dbc-546">戻り値 - canScroll</span><span class="sxs-lookup"><span data-stu-id="50dbc-546">Return Value - canScroll</span></span>

## <a name="method-characterset"></a><span data-ttu-id="50dbc-547">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="50dbc-547">Method characterSet</span></span>

<span data-ttu-id="50dbc-548">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-548">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="50dbc-549">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="50dbc-549">Parameters - characterSet</span></span>

<span data-ttu-id="50dbc-550">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-550">value</span></span>  
<span data-ttu-id="50dbc-551">テキスト フォントの文字セットを指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-551">An Integer data type that specifies the character set for the text font.</span></span>

### <a name="return-value---characterset"></a><span data-ttu-id="50dbc-552">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="50dbc-552">Return Value - characterSet</span></span>

<span data-ttu-id="50dbc-553">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-553">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="50dbc-554">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="50dbc-554">Remarks - characterSet</span></span>

<span data-ttu-id="50dbc-555">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-555">The values for the integer that is returned indicate the character set, according to the following table.</span></span>

| <span data-ttu-id="50dbc-556">先頭値</span><span class="sxs-lookup"><span data-stu-id="50dbc-556">Value</span></span> | <span data-ttu-id="50dbc-557">説明</span><span class="sxs-lookup"><span data-stu-id="50dbc-557">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="50dbc-558">0</span><span class="sxs-lookup"><span data-stu-id="50dbc-558">0</span></span>     | <span data-ttu-id="50dbc-559">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-559">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="50dbc-560">1</span><span class="sxs-lookup"><span data-stu-id="50dbc-560">1</span></span>     | <span data-ttu-id="50dbc-561">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-561">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="50dbc-562">2</span><span class="sxs-lookup"><span data-stu-id="50dbc-562">2</span></span>     | <span data-ttu-id="50dbc-563">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-563">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="50dbc-564">77</span><span class="sxs-lookup"><span data-stu-id="50dbc-564">77</span></span>    | <span data-ttu-id="50dbc-565">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-565">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="50dbc-566">128</span><span class="sxs-lookup"><span data-stu-id="50dbc-566">128</span></span>   | <span data-ttu-id="50dbc-567">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-567">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="50dbc-568">129</span><span class="sxs-lookup"><span data-stu-id="50dbc-568">129</span></span>   | <span data-ttu-id="50dbc-569">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-569">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="50dbc-570">134</span><span class="sxs-lookup"><span data-stu-id="50dbc-570">134</span></span>   | <span data-ttu-id="50dbc-571">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-571">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="50dbc-572">136</span><span class="sxs-lookup"><span data-stu-id="50dbc-572">136</span></span>   | <span data-ttu-id="50dbc-573">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-573">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="50dbc-574">161</span><span class="sxs-lookup"><span data-stu-id="50dbc-574">161</span></span>   | <span data-ttu-id="50dbc-575">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-575">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="50dbc-576">162</span><span class="sxs-lookup"><span data-stu-id="50dbc-576">162</span></span>   | <span data-ttu-id="50dbc-577">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-577">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="50dbc-578">163</span><span class="sxs-lookup"><span data-stu-id="50dbc-578">163</span></span>   | <span data-ttu-id="50dbc-579">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-579">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="50dbc-580">186</span><span class="sxs-lookup"><span data-stu-id="50dbc-580">186</span></span>   | <span data-ttu-id="50dbc-581">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-581">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="50dbc-582">204</span><span class="sxs-lookup"><span data-stu-id="50dbc-582">204</span></span>   | <span data-ttu-id="50dbc-583">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-583">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="50dbc-584">238</span><span class="sxs-lookup"><span data-stu-id="50dbc-584">238</span></span>   | <span data-ttu-id="50dbc-585">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-585">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="50dbc-586">255</span><span class="sxs-lookup"><span data-stu-id="50dbc-586">255</span></span>   | <span data-ttu-id="50dbc-587">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-587">OEM\_CHARSET</span></span>         |

<span data-ttu-id="50dbc-588">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-588">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="50dbc-589">金額</span><span class="sxs-lookup"><span data-stu-id="50dbc-589">Value</span></span> | <span data-ttu-id="50dbc-590">説明</span><span class="sxs-lookup"><span data-stu-id="50dbc-590">Description</span></span>    |
|-------|----------------|
| <span data-ttu-id="50dbc-591">130</span><span class="sxs-lookup"><span data-stu-id="50dbc-591">130</span></span>   | <span data-ttu-id="50dbc-592">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-592">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="50dbc-593">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-593">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="50dbc-594">先頭値</span><span class="sxs-lookup"><span data-stu-id="50dbc-594">Value</span></span> | <span data-ttu-id="50dbc-595">説明</span><span class="sxs-lookup"><span data-stu-id="50dbc-595">Description</span></span>     |
|-------|-----------------|
| <span data-ttu-id="50dbc-596">177</span><span class="sxs-lookup"><span data-stu-id="50dbc-596">177</span></span>   | <span data-ttu-id="50dbc-597">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-597">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="50dbc-598">178</span><span class="sxs-lookup"><span data-stu-id="50dbc-598">178</span></span>   | <span data-ttu-id="50dbc-599">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-599">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="50dbc-600">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-600">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="50dbc-601">値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-601">Value.</span></span> | <span data-ttu-id="50dbc-602">説明。</span><span class="sxs-lookup"><span data-stu-id="50dbc-602">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="50dbc-603">222</span><span class="sxs-lookup"><span data-stu-id="50dbc-603">222</span></span>    | <span data-ttu-id="50dbc-604">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="50dbc-604">THAI\_CHARSET</span></span> |

<span data-ttu-id="50dbc-605">既定の文字セットは、現在のシステム ロケールに基づいて設定されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-605">The default character set is set based on the current system locale.</span></span> <span data-ttu-id="50dbc-606">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-606">For example, if the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="50dbc-607">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-607">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-checkbox"></a><span data-ttu-id="50dbc-608">メソッド checkBox</span><span class="sxs-lookup"><span data-stu-id="50dbc-608">Method checkBox</span></span>

```xpp
public boolean checkBox([boolean value])
```

### <a name="parameters---checkbox"></a><span data-ttu-id="50dbc-609">パラメーター - checkBox</span><span class="sxs-lookup"><span data-stu-id="50dbc-609">Parameters - checkBox</span></span>

<span data-ttu-id="50dbc-610">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-610">value</span></span>  

### <a name="return-value---checkbox"></a><span data-ttu-id="50dbc-611">戻り値- checkBox</span><span class="sxs-lookup"><span data-stu-id="50dbc-611">Return Value - checkBox</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="50dbc-612">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="50dbc-612">Method colorScheme</span></span>

<span data-ttu-id="50dbc-613">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-613">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="50dbc-614">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="50dbc-614">Parameters - colorScheme</span></span>

<span data-ttu-id="50dbc-615">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-615">value</span></span>  
<span data-ttu-id="50dbc-616">フォーム リスト コントロールのカラー パレットを指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-616">An Integer data type that specifies the color palette for a form list control.</span></span>

### <a name="return-value---colorscheme"></a><span data-ttu-id="50dbc-617">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="50dbc-617">Return Value - colorScheme</span></span>

<span data-ttu-id="50dbc-618">0 (ゼロ) から 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-618">An integer between 0 (zero) and 2, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="50dbc-619">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="50dbc-619">Remarks - colorScheme</span></span>

<span data-ttu-id="50dbc-620">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-620">The color scheme is defined according to the following table.</span></span>

| <span data-ttu-id="50dbc-621">先頭値</span><span class="sxs-lookup"><span data-stu-id="50dbc-621">Value</span></span> | <span data-ttu-id="50dbc-622">スタイル</span><span class="sxs-lookup"><span data-stu-id="50dbc-622">Style</span></span>                 |
|-------|-----------------------|
| <span data-ttu-id="50dbc-623">0</span><span class="sxs-lookup"><span data-stu-id="50dbc-623">0</span></span>     | <span data-ttu-id="50dbc-624">既定</span><span class="sxs-lookup"><span data-stu-id="50dbc-624">Default</span></span>               |
| <span data-ttu-id="50dbc-625">1</span><span class="sxs-lookup"><span data-stu-id="50dbc-625">1</span></span>     | <span data-ttu-id="50dbc-626">Windows パレット</span><span class="sxs-lookup"><span data-stu-id="50dbc-626">The Windows palette</span></span>   |
| <span data-ttu-id="50dbc-627">2</span><span class="sxs-lookup"><span data-stu-id="50dbc-627">2</span></span>     | <span data-ttu-id="50dbc-628">真の配色</span><span class="sxs-lookup"><span data-stu-id="50dbc-628">The true-color scheme</span></span> |

## <a name="method-columnheader"></a><span data-ttu-id="50dbc-629">メソッド columnHeader</span><span class="sxs-lookup"><span data-stu-id="50dbc-629">Method columnHeader</span></span>

<span data-ttu-id="50dbc-630">フォーム リスト コントロールに列ヘッダーが含まれるかどうかを示すブール値データ型値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-630">Sets or gets a Boolean data type value that indicates whether a form list control has a column header.</span></span>

```xpp
public boolean columnHeader([boolean value])
```

### <a name="parameters---columnheader"></a><span data-ttu-id="50dbc-631">パラメーター - columnHeader</span><span class="sxs-lookup"><span data-stu-id="50dbc-631">Parameters - columnHeader</span></span>

<span data-ttu-id="50dbc-632">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-632">value</span></span>  
<span data-ttu-id="50dbc-633">フォーム リスト コントロールに列ヘッダーが含まれるかどうかを示すブール値データ型。</span><span class="sxs-lookup"><span data-stu-id="50dbc-633">A Boolean data type that indicates whether a form list control has a column header.</span></span>

### <a name="return-value---columnheader"></a><span data-ttu-id="50dbc-634">戻り値 - columnHeader</span><span class="sxs-lookup"><span data-stu-id="50dbc-634">Return Value - columnHeader</span></span>

<span data-ttu-id="50dbc-635">コントロールに列ヘッダーがある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-635">true if the control has a column header; otherwise, false.</span></span>

### <a name="remarks---columnheader"></a><span data-ttu-id="50dbc-636">備考 - columnHeader</span><span class="sxs-lookup"><span data-stu-id="50dbc-636">Remarks - columnHeader</span></span>

<span data-ttu-id="50dbc-637">フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-637">To display columns in a form list control, call the FormListControl.viewType method, and then pass the FormListViewType::Report enumeration value.</span></span> <span data-ttu-id="50dbc-638">フォームに列を追加する前に、columnHeader メソッドを呼び出す必要があります。それ以外の場合、列はフォーム リスト コントロールに表示されません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-638">You must call the columnHeader method before you add a column to the form; otherwise, the column does not appear in the form list control.</span></span>

### <a name="examples---columnheader"></a><span data-ttu-id="50dbc-639">例 - columnHeader</span><span class="sxs-lookup"><span data-stu-id="50dbc-639">Examples - columnHeader</span></span>

<span data-ttu-id="50dbc-640">次の例は、フォーム リスト コントロールに列ヘッダーがないことを示す columnHeader メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-640">The following example shows a call to the columnHeader method to indicate that the form list control does not have a column header.</span></span> <span data-ttu-id="50dbc-641">FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-641">The FormListControl.addColumn method adds the column to the form list control.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    boolean columnHeader; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    columnHeader = formListControl.columnHeader(false); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
}
```

## <a name="method-columnheaderbutton"></a><span data-ttu-id="50dbc-642">メソッド columnHeaderButton</span><span class="sxs-lookup"><span data-stu-id="50dbc-642">Method columnHeaderButton</span></span>

<span data-ttu-id="50dbc-643">フォーム リスト コントロールに列ヘッダー ボタンが含まれるかどうかを示すブール値データ型値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-643">Sets or gets a Boolean data type value that indicates whether a form list control has a column header button.</span></span>

```xpp
public boolean columnHeaderButton([boolean value])
```

### <a name="parameters---columnheaderbutton"></a><span data-ttu-id="50dbc-644">パラメーター - columnHeaderButton</span><span class="sxs-lookup"><span data-stu-id="50dbc-644">Parameters - columnHeaderButton</span></span>

<span data-ttu-id="50dbc-645">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-645">value</span></span>  
<span data-ttu-id="50dbc-646">フォーム リスト コントロールに列ヘッダー ボタンが含まれるかどうかを示すブール値データ型。</span><span class="sxs-lookup"><span data-stu-id="50dbc-646">A Boolean data type that indicates whether a form list control has a column header button.</span></span>

### <a name="return-value---columnheaderbutton"></a><span data-ttu-id="50dbc-647">戻り値 - columnHeaderButton</span><span class="sxs-lookup"><span data-stu-id="50dbc-647">Return Value - columnHeaderButton</span></span>

<span data-ttu-id="50dbc-648">コントロールに列ヘッダー ボタンがある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-648">true if the control has a column header button; otherwise, false.</span></span>

### <a name="remarks---columnheaderbutton"></a><span data-ttu-id="50dbc-649">備考 - columnHeaderButton</span><span class="sxs-lookup"><span data-stu-id="50dbc-649">Remarks - columnHeaderButton</span></span>

<span data-ttu-id="50dbc-650">フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-650">To display columns in a form list control, call the FormListControl.viewType method, and then pass the FormListViewType::Report enumeration value.</span></span> <span data-ttu-id="50dbc-651">フォームに列を追加する前に、columnHeaderButton メソッドを呼び出す必要があります。それ以外の場合、列はフォーム リスト コントロールに表示されません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-651">You must call the columnHeaderButton method before you add a column to the form; otherwise, the column does not appear in the form list control.</span></span>

### <a name="examples---columnheaderbutton"></a><span data-ttu-id="50dbc-652">例 - columnHeaderButton</span><span class="sxs-lookup"><span data-stu-id="50dbc-652">Examples - columnHeaderButton</span></span>

<span data-ttu-id="50dbc-653">次の例は、フォーム リスト コントロールに列ヘッダー ボタンがあることを示す columnHeaderButton メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-653">The following example shows a call to the columnHeaderButton method to indicate that the form list control has a column header button.</span></span> <span data-ttu-id="50dbc-654">FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-654">The FormListControl.addColumn method adds the column to the form list control.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    boolean columnHeaderBtn; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    columnHeaderBtn = formListControl.columnHeaderButton(true); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
}
```

## <a name="method-columnimages"></a><span data-ttu-id="50dbc-655">メソッド columnImages</span><span class="sxs-lookup"><span data-stu-id="50dbc-655">Method columnImages</span></span>

<span data-ttu-id="50dbc-656">フォーム リスト コントロールに列イメージが含まれるかどうかを示すブール値データ型値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-656">Sets or gets a Boolean data type value that indicates whether a form list control has column images.</span></span>

```xpp
public boolean columnImages([boolean value])
```

### <a name="parameters---columnimages"></a><span data-ttu-id="50dbc-657">パラメーター - columnImages</span><span class="sxs-lookup"><span data-stu-id="50dbc-657">Parameters - columnImages</span></span>

<span data-ttu-id="50dbc-658">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-658">value</span></span>  
<span data-ttu-id="50dbc-659">フォーム リスト コントロールに列の画像が含まれるかどうかを示すブール値データ型。</span><span class="sxs-lookup"><span data-stu-id="50dbc-659">A Boolean data type that indicates whether a form list control has column images.</span></span>

### <a name="return-value---columnimages"></a><span data-ttu-id="50dbc-660">戻り値 - columnImages</span><span class="sxs-lookup"><span data-stu-id="50dbc-660">Return Value - columnImages</span></span>

<span data-ttu-id="50dbc-661">フォーム リスト コントロールに列イメージがある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-661">true if the form list control has column images; otherwise, false.</span></span>

### <a name="remarks---columnimages"></a><span data-ttu-id="50dbc-662">備考 - columnImages</span><span class="sxs-lookup"><span data-stu-id="50dbc-662">Remarks - columnImages</span></span>

<span data-ttu-id="50dbc-663">フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-663">To display columns in a form list control, call the FormListControl.viewType method, and then pass the FormListViewType::Report enumeration value.</span></span>

### <a name="examples---columnimages"></a><span data-ttu-id="50dbc-664">例 - columnImages</span><span class="sxs-lookup"><span data-stu-id="50dbc-664">Examples - columnImages</span></span>

<span data-ttu-id="50dbc-665">次の例は、フォーム リスト コントロールに列イメージがあることを示す columnImages メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-665">The following example shows a call to the columnImages method to indicate that the form list control has column images.</span></span> <span data-ttu-id="50dbc-666">FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-666">The FormListControl.addColumn method adds the column to the form list control.</span></span>


```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    formListControl.columnImages(true); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
}
```

## <a name="method-configurationkey"></a><span data-ttu-id="50dbc-667">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="50dbc-667">Method configurationKey</span></span>

<span data-ttu-id="50dbc-668">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-668">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="50dbc-669">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="50dbc-669">Parameters - configurationKey</span></span>

<span data-ttu-id="50dbc-670">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-670">value</span></span>  
<span data-ttu-id="50dbc-671">コンフィギュレーション キーの ID を特定する configurationKeyId システム データ型。</span><span class="sxs-lookup"><span data-stu-id="50dbc-671">A configurationKeyId system data type that specifies the configuration key ID.</span></span>

### <a name="return-value---configurationkey"></a><span data-ttu-id="50dbc-672">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="50dbc-672">Return Value - configurationKey</span></span>

<span data-ttu-id="50dbc-673">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="50dbc-673">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="50dbc-674">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="50dbc-674">Remarks - configurationKey</span></span>

<span data-ttu-id="50dbc-675">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-675">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="50dbc-676">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-676">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="examples---configurationkey"></a><span data-ttu-id="50dbc-677">例 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="50dbc-677">Examples - configurationKey</span></span>

<span data-ttu-id="50dbc-678">次の例は、フォーム リスト コントロールに銀行コンフィギュレーション キーを割り当てる configurationKey メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-678">The following example shows a call to the configurationKey method to assign the Bank configuration key to the form list control.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    configurationKeyId ID; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run time-form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    ID = formListControl.configurationKey(configurationKeyNum(Bank)); 
}
```

## <a name="method-configurationkeyex"></a><span data-ttu-id="50dbc-679">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="50dbc-679">Method configurationKeyEx</span></span>

<span data-ttu-id="50dbc-680">フォーム リスト コントロールのために有効化されたコンフィギュレーション キーの ID を含むリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-680">Retrieves a list that contains the IDs of configuration keys that are activated for a form list control.</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="50dbc-681">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="50dbc-681">Return Value - configurationKeyEx</span></span>

<span data-ttu-id="50dbc-682">フォーム リスト コントロールのために有効化されたコンフィギュレーション キーの ID を含むリスト オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="50dbc-682">A List object that contains the IDs of configuration keys that are activated for a form list control.</span></span>

### <a name="remarks---configurationkeyex"></a><span data-ttu-id="50dbc-683">備考 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="50dbc-683">Remarks - configurationKeyEx</span></span>

<span data-ttu-id="50dbc-684">コントロールがデータソースにバインドされている場合、取得された構成キー ID のリストには、テーブルとフィールドの構成キー ID も含まれます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-684">If the control is bound to a data source, the retrieved list of configuration key IDs also includes the configuration key ID for the table and field.</span></span> <span data-ttu-id="50dbc-685">さらに、取得したリストには、拡張データ型に適用される任意のコンフィギュレーション キー ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-685">In addition, the retrieved list contains any configuration key IDs that are applied to the extended data type.</span></span> <span data-ttu-id="50dbc-686">リストに重複 ID は含まれません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-686">The list does not contain duplicate IDs.</span></span>

### <a name="examples---configurationkeyex"></a><span data-ttu-id="50dbc-687">例 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="50dbc-687">Examples - configurationKeyEx</span></span>

<span data-ttu-id="50dbc-688">次の例は、configurationKeyEx メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-688">The following example shows a call to the configurationKeyEx method.</span></span> <span data-ttu-id="50dbc-689">ListEnumerator オブジェクトを使用すると、一覧全体の要素上を移動できます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-689">The ListEnumerator object is used to traverse the elements throughout a list.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    configurationKeyId ID; 
    List list; 
    ListEnumerator enum; 
    DictConfigurationKey dck; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    ID = formListControl.configurationKey(configurationKeyNum(Bank)); 
    list = formListControl.configurationKeyEx(); 
    if (0 != list.elements()) 
    { 
        enum = list.getEnumerator(); 
        while (enum.moveNext()) 
        { 
            dck = new DictConfigurationKey(enum.current()); 
            if (dck) 
            { 
                print strfmt("Configuration Key ID: %1" 
                  + "Configuration Key Name: %2",enum.current(),dck.name()); 
                pause; 
            } 
        } 
    } 
}
```

## <a name="method-copyitem"></a><span data-ttu-id="50dbc-690">メソッド copyItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-690">Method copyItem</span></span>

<span data-ttu-id="50dbc-691">指定した項目をフォーム リスト コントロールにコピーします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-691">Copies a specified item in a form list control.</span></span>

```xpp
public int copyItem(int Item, int InsertAt)
```

### <a name="parameters---copyitem"></a><span data-ttu-id="50dbc-692">パラメーター - copyItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-692">Parameters - copyItem</span></span>

<span data-ttu-id="50dbc-693">項目</span><span class="sxs-lookup"><span data-stu-id="50dbc-693">Item</span></span>  
<span data-ttu-id="50dbc-694">品目がコピーされるリスト内の位置を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-694">An Integer data type that specifies the position in the list that the item is copied to.</span></span>

<!-- -->

<span data-ttu-id="50dbc-695">InsertAt</span><span class="sxs-lookup"><span data-stu-id="50dbc-695">InsertAt</span></span>  
<span data-ttu-id="50dbc-696">品目がコピーされるリスト内の位置を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-696">An Integer data type that specifies the position in the list that the item is copied to.</span></span>

### <a name="return-value---copyitem"></a><span data-ttu-id="50dbc-697">戻り値 - copyItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-697">Return Value - copyItem</span></span>

<span data-ttu-id="50dbc-698">品目がコピーされるリスト内の位置を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-698">An Integer data type that specifies the position in the list that the item is copied to.</span></span>

### <a name="remarks---copyitem"></a><span data-ttu-id="50dbc-699">備考 - copyItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-699">Remarks - copyItem</span></span>

<span data-ttu-id="50dbc-700">フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-700">To display columns in a form list control, call the FormListControl.viewType method, and then pass the FormListViewType::Report enumeration value.</span></span>

### <a name="examples---copyitem"></a><span data-ttu-id="50dbc-701">例 - copyItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-701">Examples - copyItem</span></span>

<span data-ttu-id="50dbc-702">次の例は、フォーム リスト コントロールの 10 番目の位置にアイテムをコピーする copyItem メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-702">The following example shows a call to the copyItem method to copy an item to the tenth position in the form list control.</span></span> <span data-ttu-id="50dbc-703">FormListControl.getCount メソッドは、コントロール内の項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-703">The FormListControl.getCount method returns the number of items in the control.</span></span> <span data-ttu-id="50dbc-704">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-704">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-705">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-705">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
   } 
    formListControl.getCount(); 
    formListControl.copyItem(2,10); 
}
```

## <a name="method-countryregioncodes"></a><span data-ttu-id="50dbc-706">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="50dbc-706">Method countryRegionCodes</span></span>

<span data-ttu-id="50dbc-707">コントロールの国/地域コードのコンマ区切りのリストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-707">Gets or sets the comma-separated list of country/region codes for the control.</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="50dbc-708">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="50dbc-708">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="50dbc-709">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-709">value</span></span>  
<span data-ttu-id="50dbc-710">設定する国/地域コードを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-710">The string that contains the country/region codes to set; optional.</span></span>

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="50dbc-711">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="50dbc-711">Return Value - countryRegionCodes</span></span>

<span data-ttu-id="50dbc-712">コントロールの国/地域コードのコンマ区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="50dbc-712">The comma-separated list of country/region codes for the control.</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="50dbc-713">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="50dbc-713">Method dataRelationPath</span></span>

<span data-ttu-id="50dbc-714">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-714">Gets or sets the period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="50dbc-715">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="50dbc-715">Parameters - dataRelationPath</span></span>

<span data-ttu-id="50dbc-716">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-716">value</span></span>  
<span data-ttu-id="50dbc-717">ピリオドで区切られたリレーションのリストを含む文字列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-717">The string that contains the period-delimited list of relations; optional.</span></span>

### <a name="return-value---datarelationpath"></a><span data-ttu-id="50dbc-718">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="50dbc-718">Return Value - dataRelationPath</span></span>

<span data-ttu-id="50dbc-719">DataField オブジェクトのフィールド バインディングを相対的なテーブルにリンクするリレーションのピリオドで区切られた一覧。</span><span class="sxs-lookup"><span data-stu-id="50dbc-719">The period-delimited list of relations that links the field binding of the DataField object to a relative table.</span></span>

### <a name="remarks---datarelationpath"></a><span data-ttu-id="50dbc-720">備考 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="50dbc-720">Remarks - dataRelationPath</span></span>

<span data-ttu-id="50dbc-721">このメソッドは、参照グループ コントロールによって使用され、どの関係が使用される置換フィールドを生成するかを正確に追跡します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-721">This method is used by the reference group control to track exactly which relations produce the replacement field that is used.</span></span> <span data-ttu-id="50dbc-722">参照グループ コントロールを有効にして、そこに含まれるコントロールに一貫したバインディングを行います。</span><span class="sxs-lookup"><span data-stu-id="50dbc-722">It enables the reference group control to bind consistently to the controls that it contains.</span></span>

## <a name="method-delete"></a><span data-ttu-id="50dbc-723">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="50dbc-723">Method delete</span></span>

<span data-ttu-id="50dbc-724">フォーム リスト コントロールから指定した項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-724">Deletes a specified item from a form list control.</span></span>

```xpp
public boolean delete(int Idx)
```

### <a name="parameters---delete"></a><span data-ttu-id="50dbc-725">パラメーター - delete</span><span class="sxs-lookup"><span data-stu-id="50dbc-725">Parameters - delete</span></span>

<span data-ttu-id="50dbc-726">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-726">Idx</span></span>  
<span data-ttu-id="50dbc-727">削除される項目の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="50dbc-727">The zero-based index for the item that is being deleted.</span></span>

### <a name="return-value---delete"></a><span data-ttu-id="50dbc-728">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="50dbc-728">Return Value - delete</span></span>

<span data-ttu-id="50dbc-729">項目が削除された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-729">true if the item is deleted; otherwise, false.</span></span>

### <a name="examples---delete"></a><span data-ttu-id="50dbc-730">例 - delete</span><span class="sxs-lookup"><span data-stu-id="50dbc-730">Examples - delete</span></span>

<span data-ttu-id="50dbc-731">次の例は、フォーム リスト コントロールから項目を削除する delete メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-731">The following example shows a call to the delete method to delete an item from the form list control.</span></span> <span data-ttu-id="50dbc-732">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-732">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-733">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-733">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    boolean itemDel; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    // Delete an item. 
    itemDel = formListControl.delete(2); 
}
```

## <a name="method-deleteall"></a><span data-ttu-id="50dbc-734">メソッド deleteAll</span><span class="sxs-lookup"><span data-stu-id="50dbc-734">Method deleteAll</span></span>

<span data-ttu-id="50dbc-735">フォーム リスト コントロールからすべての項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-735">Deletes all the items from a form list control.</span></span>

```xpp
public boolean deleteAll()
```

### <a name="return-value---deleteall"></a><span data-ttu-id="50dbc-736">戻り値 - deleteAll</span><span class="sxs-lookup"><span data-stu-id="50dbc-736">Return Value - deleteAll</span></span>

<span data-ttu-id="50dbc-737">すべての項目が削除された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-737">true if all the items are deleted; otherwise, false.</span></span>

### <a name="examples---deleteall"></a><span data-ttu-id="50dbc-738">例 - deleteAll</span><span class="sxs-lookup"><span data-stu-id="50dbc-738">Examples - deleteAll</span></span>

<span data-ttu-id="50dbc-739">次の例は、フォーム リスト コントロールからすべての項目を削除する deleteAll メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-739">The following example shows a call to the deleteAll method to delete all the items from the form list control.</span></span> <span data-ttu-id="50dbc-740">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-740">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-741">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-741">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    boolean itemsDel; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    // Delete all items. 
    itemsDel = formListControl.deleteAll(); 
}
```

## <a name="method-deletecolumn"></a><span data-ttu-id="50dbc-742">メソッド deleteColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-742">Method deleteColumn</span></span>

<span data-ttu-id="50dbc-743">フォーム リスト コントロールの指定した列を削除します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-743">Deletes a specified column in a form list control.</span></span>

```xpp
public boolean deleteColumn(int Idx)
```

### <a name="parameters---deletecolumn"></a><span data-ttu-id="50dbc-744">パラメーター - deleteColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-744">Parameters - deleteColumn</span></span>

<span data-ttu-id="50dbc-745">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-745">Idx</span></span>  
<span data-ttu-id="50dbc-746">フォーム リスト コントロール内で列を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-746">An Integer data type that specifies a column in a form list control.</span></span>

### <a name="return-value---deletecolumn"></a><span data-ttu-id="50dbc-747">戻り値 - deleteColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-747">Return Value - deleteColumn</span></span>

<span data-ttu-id="50dbc-748">列が削除された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-748">true if the column is deleted; otherwise, false.</span></span>

### <a name="examples---deletecolumn"></a><span data-ttu-id="50dbc-749">例 - deleteColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-749">Examples - deleteColumn</span></span>

<span data-ttu-id="50dbc-750">次の例は、フォーム リスト コントロールから第 1 列を削除する deleteColumn メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-750">The following example shows a call to the deleteColumn method to delete the first column in the form list control.</span></span> <span data-ttu-id="50dbc-751">FormListControl.addColumn メソッドは、2 列をフォーム リスト コントロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-751">The FormListControl.addColumn method adds two columns to the form list control.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    boolean columnDel; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add columns to the form list control. 
    formListControl.addColumn(0, new FormListColumn("Column1",1,120)); 
    formListControl.addColumn(1, new FormListColumn("Column2",2,120)); 
    // Delete a column. 
    columnDel = formListControl.deleteColumn(0); 
}
```

## <a name="method-displaytarget"></a><span data-ttu-id="50dbc-752">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="50dbc-752">Method displayTarget</span></span>

<span data-ttu-id="50dbc-753">クライアント、または Finance and Operations のエンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-753">Gets or sets the value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="50dbc-754">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="50dbc-754">Parameters - displayTarget</span></span>

<span data-ttu-id="50dbc-755">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-755">value</span></span>  
<span data-ttu-id="50dbc-756">コントロールが表示される場所を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-756">The integer value that indicates where the control is displayed; optional.</span></span>

### <a name="return-value---displaytarget"></a><span data-ttu-id="50dbc-757">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="50dbc-757">Return Value - displayTarget</span></span>

<span data-ttu-id="50dbc-758">クライアント、エンタープライズ ポータル、またはその両方でコントロールが表示されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-758">The value that indicates whether the control is displayed in the client, in Enterprise Portal, or in both.</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="50dbc-759">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="50dbc-759">Method dragDrop</span></span>

<span data-ttu-id="50dbc-760">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-760">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="50dbc-761">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="50dbc-761">Parameters - dragDrop</span></span>

<span data-ttu-id="50dbc-762">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-762">value</span></span>  
<span data-ttu-id="50dbc-763">ドラッグ アンド ドロップの動作が有効かどうかを示す整数です (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-763">An Integer that indicates whether drag-and-drop behavior is enabled; optional.</span></span>

### <a name="return-value---dragdrop"></a><span data-ttu-id="50dbc-764">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="50dbc-764">Return Value - dragDrop</span></span>

<span data-ttu-id="50dbc-765">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-765">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

### <a name="remarks---dragdrop"></a><span data-ttu-id="50dbc-766">備考 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="50dbc-766">Remarks - dragDrop</span></span>

<span data-ttu-id="50dbc-767">dragLeave、dragOver、および dragOverEx を使用して、ビヘイビアーを指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-767">Use the dragLeave, the dragOver, and the dragOverEx to specify the behavior.</span></span>

## <a name="method-dragover"></a><span data-ttu-id="50dbc-768">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="50dbc-768">Method dragOver</span></span>

<span data-ttu-id="50dbc-769">ユーザーがフォーム リスト コントロールの境界内のアイテムにオブジェクトをドラッグするときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-769">Identifies when a user drags an object over an item within the bounds of a form list control.</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="50dbc-770">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="50dbc-770">Parameters - dragOver</span></span>

<span data-ttu-id="50dbc-771">dragSource</span><span class="sxs-lookup"><span data-stu-id="50dbc-771">dragSource</span></span>  
<span data-ttu-id="50dbc-772">オブジェクトの位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-772">An Integer data type that indicates the y-coordinate of the object's position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-773">dragMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-773">dragMode</span></span>  
<span data-ttu-id="50dbc-774">オブジェクトの位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-774">An Integer data type that indicates the y-coordinate of the object's position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-775">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-775">x</span></span>  
<span data-ttu-id="50dbc-776">オブジェクトの位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-776">An Integer data type that indicates the y-coordinate of the object's position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-777">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-777">y</span></span>  
<span data-ttu-id="50dbc-778">オブジェクトの位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-778">An Integer data type that indicates the y-coordinate of the object's position.</span></span>

### <a name="return-value---dragover"></a><span data-ttu-id="50dbc-779">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="50dbc-779">Return Value - dragOver</span></span>

<span data-ttu-id="50dbc-780">オブジェクトが移動、コピー、または指定された位置に移動されていないかどうかを示す FormDrag システム列挙値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-780">A FormDrag system enumeration value that specifies whether the object is moved, copied, or not moved to a specified position.</span></span>

### <a name="remarks---dragover"></a><span data-ttu-id="50dbc-781">備考 - dragOver</span><span class="sxs-lookup"><span data-stu-id="50dbc-781">Remarks - dragOver</span></span>

<span data-ttu-id="50dbc-782">このメソッドは、DragDrop プロパティがコントロールの手動に設定されていて、beginDrag イベントがすでに開始されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-782">This method is called only if the DragDrop property is set to Manual for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="50dbc-783">イベントの詳細については、beginDrag を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-783">For more information about the event, see beginDrag.</span></span> <span data-ttu-id="50dbc-784">リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [dragOver] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-784">To override this method on a list view control, right-click the Methods node below the control, point to Override Method, and then click dragOver.</span></span> <span data-ttu-id="50dbc-785">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-785">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="50dbc-786">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="50dbc-786">Method dragOverEx</span></span>

<span data-ttu-id="50dbc-787">マウス ドラッグ操作が現在のコントロールで行われることを示すために、dragOverEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-787">Raises the dragOverEx event to indicate that a mouse drag operation is over the current control.</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="50dbc-788">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="50dbc-788">Parameters - dragOverEx</span></span>

<span data-ttu-id="50dbc-789">dragSource</span><span class="sxs-lookup"><span data-stu-id="50dbc-789">dragSource</span></span>  
<span data-ttu-id="50dbc-790">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-790">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-791">dragMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-791">dragMode</span></span>  
<span data-ttu-id="50dbc-792">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-792">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-793">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-793">x</span></span>  
<span data-ttu-id="50dbc-794">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-794">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-795">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-795">y</span></span>  
<span data-ttu-id="50dbc-796">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-796">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

### <a name="return-value---dragoverex"></a><span data-ttu-id="50dbc-797">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="50dbc-797">Return Value - dragOverEx</span></span>

<span data-ttu-id="50dbc-798">ドラッグ モードを示す FormDrag 列挙値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-798">A FormDrag enumeration value that indicates the mode of dragging.</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="50dbc-799">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="50dbc-799">Method dragText</span></span>

<span data-ttu-id="50dbc-800">フォーム リスト コントロールでユーザーが項目をドラッグしたときに表示されるテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-800">Retrieves the text that is displayed when a user drags an item in a form list control.</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="50dbc-801">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="50dbc-801">Return Value - dragText</span></span>

<span data-ttu-id="50dbc-802">ユーザーがフォーム リスト コントロールをドラッグするときに表示されるテキストを指定する文字列データ型値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-802">A String data type value that specifies the text that is displayed when a user drags a form list control.</span></span>

### <a name="remarks---dragtext"></a><span data-ttu-id="50dbc-803">備考 - dragText</span><span class="sxs-lookup"><span data-stu-id="50dbc-803">Remarks - dragText</span></span>

<span data-ttu-id="50dbc-804">リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [dragText] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-804">To override this method on a list view control, right-click the Methods node below the control, point to Override Method, and then click dragText.</span></span> <span data-ttu-id="50dbc-805">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-805">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-editlabels"></a><span data-ttu-id="50dbc-806">メソッド editLabels</span><span class="sxs-lookup"><span data-stu-id="50dbc-806">Method editLabels</span></span>

<span data-ttu-id="50dbc-807">ユーザーがフォーム リスト コントロールで項目名を変更できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-807">Indicates whether users can modify item names in a form list control.</span></span>

```xpp
public boolean editLabels([boolean value])
```

### <a name="parameters---editlabels"></a><span data-ttu-id="50dbc-808">パラメーター - editLabels</span><span class="sxs-lookup"><span data-stu-id="50dbc-808">Parameters - editLabels</span></span>

<span data-ttu-id="50dbc-809">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-809">value</span></span>  
<span data-ttu-id="50dbc-810">ユーザーがフォーム リスト コントロール内の項目名を変更できるかどうかを指定するブール値データ型。</span><span class="sxs-lookup"><span data-stu-id="50dbc-810">A Boolean data type that specifies whether users can modify item names in a form list control.</span></span>

### <a name="return-value---editlabels"></a><span data-ttu-id="50dbc-811">戻り値 - editLabels</span><span class="sxs-lookup"><span data-stu-id="50dbc-811">Return Value - editLabels</span></span>

<span data-ttu-id="50dbc-812">ユーザーが項目名を変更することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-812">true if users can modify item names; otherwise, false.</span></span>

### <a name="remarks---editlabels"></a><span data-ttu-id="50dbc-813">備考 - editLabels</span><span class="sxs-lookup"><span data-stu-id="50dbc-813">Remarks - editLabels</span></span>

<span data-ttu-id="50dbc-814">フォーム リスト コントロールに列を追加する前に、editLabels メソッドを呼び出す必要があります。それ以外の場合、列はコントロールに表示されません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-814">You must call the editLabels method before you add columns to a form list control; otherwise, the columns do not appear in the control.</span></span>

### <a name="examples---editlabels"></a><span data-ttu-id="50dbc-815">例 - editLabels</span><span class="sxs-lookup"><span data-stu-id="50dbc-815">Examples - editLabels</span></span>

<span data-ttu-id="50dbc-816">次の例は、ユーザーがフォーム リスト コントロール内の項目名を変更できるようにする editLabels メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-816">The following example shows a call to the editLabels method to enable users to modify item names in the form list control.</span></span> <span data-ttu-id="50dbc-817">DictField.label メソッドは、フォーム リスト コントロールへの品目として追加される指定のテーブル フィールドのラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-817">The DictField.label method returns a label for a specified table field that is added as an item to the form list control.</span></span> <span data-ttu-id="50dbc-818">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-818">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-819">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-819">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    DictField dictField; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    formListControl.editLabels(true); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1",1,120)); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
        dictField = new DictField(77,1); 
        formListItem = new FormListItem(dictField.label()); 
        item = formListControl.addItem(formListItem); 
    } 
}
```

## <a name="method-enabled"></a><span data-ttu-id="50dbc-820">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="50dbc-820">Method enabled</span></span>

<span data-ttu-id="50dbc-821">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-821">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="50dbc-822">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="50dbc-822">Parameters - enabled</span></span>

<span data-ttu-id="50dbc-823">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-823">value</span></span>  
<span data-ttu-id="50dbc-824">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-824">A Boolean value that specifies whether the control is enabled; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="50dbc-825">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="50dbc-825">Return Value - enabled</span></span>

<span data-ttu-id="50dbc-826">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-826">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="50dbc-827">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="50dbc-827">Remarks - enabled</span></span>

<span data-ttu-id="50dbc-828">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-828">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="50dbc-829">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-829">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="50dbc-830">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-830">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-ensurevisible"></a><span data-ttu-id="50dbc-831">メソッド ensureVisible</span><span class="sxs-lookup"><span data-stu-id="50dbc-831">Method ensureVisible</span></span>

```xpp
public int ensureVisible(int Idx)
```

### <a name="parameters---ensurevisible"></a><span data-ttu-id="50dbc-832">パラメーター - ensureVisible</span><span class="sxs-lookup"><span data-stu-id="50dbc-832">Parameters - ensureVisible</span></span>

<span data-ttu-id="50dbc-833">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-833">Idx</span></span>  

### <a name="return-value---ensurevisible"></a><span data-ttu-id="50dbc-834">戻り値 - ensureVisible</span><span class="sxs-lookup"><span data-stu-id="50dbc-834">Return Value - ensureVisible</span></span>

## <a name="method-font"></a><span data-ttu-id="50dbc-835">メソッド font</span><span class="sxs-lookup"><span data-stu-id="50dbc-835">Method font</span></span>

<span data-ttu-id="50dbc-836">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-836">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="50dbc-837">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="50dbc-837">Parameters - font</span></span>

<span data-ttu-id="50dbc-838">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-838">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="50dbc-839">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="50dbc-839">Return Value - font</span></span>

<span data-ttu-id="50dbc-840">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="50dbc-840">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="50dbc-841">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="50dbc-841">Method fontSize</span></span>

<span data-ttu-id="50dbc-842">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-842">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="50dbc-843">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="50dbc-843">Parameters - fontSize</span></span>

<span data-ttu-id="50dbc-844">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-844">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="50dbc-845">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="50dbc-845">Return Value - fontSize</span></span>

<span data-ttu-id="50dbc-846">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="50dbc-846">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="50dbc-847">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="50dbc-847">Method foregroundColor</span></span>

<span data-ttu-id="50dbc-848">コントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-848">Gets or sets the text color for the control.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="50dbc-849">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="50dbc-849">Parameters - foregroundColor</span></span>

<span data-ttu-id="50dbc-850">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-850">value</span></span>  
<span data-ttu-id="50dbc-851">前景色を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-851">An Integer data type that specifies the foreground color.</span></span>

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="50dbc-852">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="50dbc-852">Return Value - foregroundColor</span></span>

<span data-ttu-id="50dbc-853">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-853">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="50dbc-854">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="50dbc-854">Remarks - foregroundColor</span></span>

<span data-ttu-id="50dbc-855">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-855">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="50dbc-856">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-856">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="50dbc-857">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-857">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="50dbc-858">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-858">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="50dbc-859">上位バイトは 0 (ゼロ) でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-859">The high-order byte must be 0 (zero).</span></span>
-   <span data-ttu-id="50dbc-860">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-860">The maximum value for a single byte is 255.</span></span>

### <a name="examples---foregroundcolor"></a><span data-ttu-id="50dbc-861">例 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="50dbc-861">Examples - foregroundColor</span></span>

<span data-ttu-id="50dbc-862">次の例は、前景色をデスクトップ上のメニュー テキストの色に設定する foregroundColor メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-862">The following example shows a call to the foregroundColor method to set the foreground color to the color of the menu text on the desktop.</span></span> <span data-ttu-id="50dbc-863">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-863">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-864">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-864">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.foregroundColor(WindowsPalette::MenuText); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
}
```

## <a name="method-getcolumn"></a><span data-ttu-id="50dbc-865">メソッド getColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-865">Method getColumn</span></span>

<span data-ttu-id="50dbc-866">フォーム リスト コントロール内の指定された列の FormListColumn オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-866">Retrieves a FormListColumn object for a specified column in a form list control.</span></span>

```xpp
public FormListColumn getColumn(int Idx)
```

### <a name="parameters---getcolumn"></a><span data-ttu-id="50dbc-867">パラメーター - getColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-867">Parameters - getColumn</span></span>

<span data-ttu-id="50dbc-868">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-868">Idx</span></span>  
<span data-ttu-id="50dbc-869">フォーム リスト コントロール内で列を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-869">An Integer data type that specifies a column in a form list control.</span></span>

### <a name="return-value---getcolumn"></a><span data-ttu-id="50dbc-870">戻り値 - getColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-870">Return Value - getColumn</span></span>

<span data-ttu-id="50dbc-871">フォーム リスト コントロール内の指定された列の FormListColumn オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="50dbc-871">A FormListColumn object for a specified column in a form list control.</span></span>

### <a name="remarks---getcolumn"></a><span data-ttu-id="50dbc-872">備考 - getColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-872">Remarks - getColumn</span></span>

<span data-ttu-id="50dbc-873">フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-873">To display columns in a form list control, call the FormListControl.viewType method, and then pass the FormListViewType::Report enumeration value.</span></span>

### <a name="examples---getcolumn"></a><span data-ttu-id="50dbc-874">例 - getColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-874">Examples - getColumn</span></span>

<span data-ttu-id="50dbc-875">次の例は、フォーム リスト コントロール内の列の FormListColumn オブジェクトを返す getColumn メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-875">The following example shows a call to the getColumn method to return a FormListColumn object for the column in the form list control.</span></span> <span data-ttu-id="50dbc-876">FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-876">The FormListControl.addColumn method adds the column to the form list control.</span></span>


```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    str columnName; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control, 
    // and then set the column width. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    formListColumn = formListControl.getColumn(0); 
    columnName = formListColumn.toString(); 
}
```

## <a name="method-getcolumncount"></a><span data-ttu-id="50dbc-877">メソッド getColumnCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-877">Method getColumnCount</span></span>

<span data-ttu-id="50dbc-878">フォーム リスト コントロール内の列の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-878">Retrieves the number of columns in a form list control.</span></span>

```xpp
public int getColumnCount()
```

### <a name="return-value---getcolumncount"></a><span data-ttu-id="50dbc-879">戻り値 - getColumnCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-879">Return Value - getColumnCount</span></span>

<span data-ttu-id="50dbc-880">フォーム リスト コントロールの列数を指定する整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-880">An Integer data type value that specifies the number of columns in a form list control.</span></span>

### <a name="remarks---getcolumncount"></a><span data-ttu-id="50dbc-881">備考 - getColumnCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-881">Remarks - getColumnCount</span></span>

<span data-ttu-id="50dbc-882">フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-882">To display columns in a form list control, call the FormListControl.viewType method and then pass the FormListViewType::Report enumeration value.</span></span>

### <a name="examples---getcolumncount"></a><span data-ttu-id="50dbc-883">例 - getColumnCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-883">Examples - getColumnCount</span></span>

<span data-ttu-id="50dbc-884">次の例は、フォーム リスト コントロールの列数を返す getColumnCount メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-884">The following example shows a call to the getColumnCount method to return the number of columns in the form list control.</span></span> <span data-ttu-id="50dbc-885">FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-885">The FormListControl.addColumn method adds the column to the form list control.</span></span>


```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    int columnCnt; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    columnCnt = formListControl.getColumnCount(); 
}
```

## <a name="method-getcolumnwidth"></a><span data-ttu-id="50dbc-886">メソッド getColumnWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-886">Method getColumnWidth</span></span>

<span data-ttu-id="50dbc-887">フォーム リスト コントロール内の列の幅を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-887">Retrieves the width of a column in a form list control.</span></span>

```xpp
public int getColumnWidth(int Idx)
```

### <a name="parameters---getcolumnwidth"></a><span data-ttu-id="50dbc-888">パラメーター - getColumnWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-888">Parameters - getColumnWidth</span></span>

<span data-ttu-id="50dbc-889">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-889">Idx</span></span>  
<span data-ttu-id="50dbc-890">フォーム リスト コントロール内で列を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-890">An Integer data type that specifies a column in a form list control.</span></span>

### <a name="return-value---getcolumnwidth"></a><span data-ttu-id="50dbc-891">戻り値 - getColumnWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-891">Return Value - getColumnWidth</span></span>

<span data-ttu-id="50dbc-892">フォーム リスト コントロール内で列幅を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-892">An Integer data type that specifies the width of a column in a form list control.</span></span>

### <a name="remarks---getcolumnwidth"></a><span data-ttu-id="50dbc-893">備考 - getColumnWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-893">Remarks - getColumnWidth</span></span>

<span data-ttu-id="50dbc-894">フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-894">To display columns in a form list control, call the FormListControl.viewType method, and then pass the FormListViewType::Report enumeration value.</span></span>

### <a name="examples---getcolumnwidth"></a><span data-ttu-id="50dbc-895">例 - getColumnWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-895">Examples - getColumnWidth</span></span>

<span data-ttu-id="50dbc-896">次の例は、フォーム リスト コントロール内の列の幅を返す getColumnWidth メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-896">The following example shows a call to the getColumnWidth method to return the width of a column in the form list control.</span></span> <span data-ttu-id="50dbc-897">FormListControl.setColumnWidth メソッドは、列の幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-897">The FormListControl.setColumnWidth method specifies the column width.</span></span> <span data-ttu-id="50dbc-898">FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-898">The FormListControl.addColumn method adds the column to the form list control.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    int width; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control, 
    // and then set the column width. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    formListControl.setColumnWidth(0,100); 
    width = formListControl.getColumnWidth(0); 
}
```

## <a name="method-getcount"></a><span data-ttu-id="50dbc-899">メソッド getCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-899">Method getCount</span></span>

<span data-ttu-id="50dbc-900">フォーム リスト コントロールに含まれる項目の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-900">Retrieves the number of items that are contained in a form list control.</span></span>

```xpp
public int getCount()
```

### <a name="return-value---getcount"></a><span data-ttu-id="50dbc-901">戻り値 - getCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-901">Return Value - getCount</span></span>

<span data-ttu-id="50dbc-902">フォーム リスト コントロールに含まれている品目数を指定する整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-902">An Integer data type value that specifies the number of items that are contained in a form list control.</span></span>

### <a name="examples---getcount"></a><span data-ttu-id="50dbc-903">例 - getCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-903">Examples - getCount</span></span>

<span data-ttu-id="50dbc-904">次の例は、getCount メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-904">The following example shows a call to the getCount method.</span></span> <span data-ttu-id="50dbc-905">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-905">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-906">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-906">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    numItems = formListControl.getCount(); 
}
```

## <a name="method-getcountperpage"></a><span data-ttu-id="50dbc-907">メソッド getCountPerPage</span><span class="sxs-lookup"><span data-stu-id="50dbc-907">Method getCountPerPage</span></span>

```xpp
public int getCountPerPage()
```

### <a name="return-value---getcountperpage"></a><span data-ttu-id="50dbc-908">戻り値 - getCountPerPage</span><span class="sxs-lookup"><span data-stu-id="50dbc-908">Return Value - getCountPerPage</span></span>

## <a name="method-getimagelist"></a><span data-ttu-id="50dbc-909">メソッド getImagelist</span><span class="sxs-lookup"><span data-stu-id="50dbc-909">Method getImagelist</span></span>

```xpp
public Imagelist getImagelist([boolean GetLarge])
```

### <a name="parameters---getimagelist"></a><span data-ttu-id="50dbc-910">パラメーター - getImagelist</span><span class="sxs-lookup"><span data-stu-id="50dbc-910">Parameters - getImagelist</span></span>

<span data-ttu-id="50dbc-911">GetLarge</span><span class="sxs-lookup"><span data-stu-id="50dbc-911">GetLarge</span></span>  

### <a name="return-value---getimagelist"></a><span data-ttu-id="50dbc-912">戻り値 - getImagelist</span><span class="sxs-lookup"><span data-stu-id="50dbc-912">Return Value - getImagelist</span></span>

## <a name="method-getitem"></a><span data-ttu-id="50dbc-913">メソッド getItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-913">Method getItem</span></span>

<span data-ttu-id="50dbc-914">フォーム リスト コントロール内の項目の FormListItem オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-914">Retrieves a FormListItem object for an item in a form list control.</span></span>

```xpp
public FormListItem getItem(int Idx, [int SubItem])
```

### <a name="parameters---getitem"></a><span data-ttu-id="50dbc-915">パラメーター - getItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-915">Parameters - getItem</span></span>

<span data-ttu-id="50dbc-916">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-916">Idx</span></span>  
<span data-ttu-id="50dbc-917">フォーム リスト コントロール内でサブ項目を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-917">An Integer data type that specifies a sub-item in a form list control.</span></span>

<!-- -->

<span data-ttu-id="50dbc-918">SubItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-918">SubItem</span></span>  
<span data-ttu-id="50dbc-919">フォーム リスト コントロール内でサブ項目を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-919">An Integer data type that specifies a sub-item in a form list control.</span></span>

### <a name="return-value---getitem"></a><span data-ttu-id="50dbc-920">戻り値 - getItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-920">Return Value - getItem</span></span>

<span data-ttu-id="50dbc-921">フォーム リスト コントロール内の項目の FormListItem オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="50dbc-921">A FormListItem object for an item in a form list control.</span></span>

### <a name="examples---getitem"></a><span data-ttu-id="50dbc-922">例 - getItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-922">Examples - getItem</span></span>

<span data-ttu-id="50dbc-923">次の例は、フォーム リスト コントロール内の各項目の列の FormListItem オブジェクトを返す getItem メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-923">The following example shows a call to the getItem method to return a FormListItem object for each item in the form list control.</span></span> <span data-ttu-id="50dbc-924">FormListItem.toString メソッドは、各項目のテキスト文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-924">The FormListItem.toString method returns a text string for each item.</span></span> <span data-ttu-id="50dbc-925">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-925">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-926">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-926">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    boolean columnadd; 
    str string; 
    str itemTxt; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add an item to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
            "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
        formListItem = formListControl.getItem(item); 
        itemTxt = formListItem.toString(); 
    } 
}
```

## <a name="method-getitempos"></a><span data-ttu-id="50dbc-927">メソッド getItemPos</span><span class="sxs-lookup"><span data-stu-id="50dbc-927">Method getItemPos</span></span>

<span data-ttu-id="50dbc-928">フォーム リスト コントロール内の項目の位置を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-928">Retrieves the position of an item in a form list control.</span></span>

```xpp
public container getItemPos(int Item)
```

### <a name="parameters---getitempos"></a><span data-ttu-id="50dbc-929">パラメーター - getItemPos</span><span class="sxs-lookup"><span data-stu-id="50dbc-929">Parameters - getItemPos</span></span>

<span data-ttu-id="50dbc-930">項目</span><span class="sxs-lookup"><span data-stu-id="50dbc-930">Item</span></span>  
<span data-ttu-id="50dbc-931">フォーム リスト コントロール内の項目を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-931">An Integer data type that specifies an item in a form list control.</span></span>

### <a name="return-value---getitempos"></a><span data-ttu-id="50dbc-932">戻り値 - getItemPos</span><span class="sxs-lookup"><span data-stu-id="50dbc-932">Return Value - getItemPos</span></span>

<span data-ttu-id="50dbc-933">フォーム リスト コントロールの項目の位置を含むコンテナー データ型。</span><span class="sxs-lookup"><span data-stu-id="50dbc-933">A Container data type that contains the position of an item in a form list control.</span></span> <span data-ttu-id="50dbc-934">項目の位置は、x 座標と y 座標によって指定されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-934">The position of an item is specified by an x-coordinate and a y-coordinate.</span></span>

### <a name="remarks---getitempos"></a><span data-ttu-id="50dbc-935">備考 - getItemPos</span><span class="sxs-lookup"><span data-stu-id="50dbc-935">Remarks - getItemPos</span></span>

<span data-ttu-id="50dbc-936">コンテナから項目を抽出するには conPeek 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-936">Use the conPeek function to extract an item from a container.</span></span>

### <a name="examples---getitempos"></a><span data-ttu-id="50dbc-937">例 - getItemPos</span><span class="sxs-lookup"><span data-stu-id="50dbc-937">Examples - getItemPos</span></span>

<span data-ttu-id="50dbc-938">次の例は、フォーム リスト コントロール内の各項目の位置を返す getItemPos メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-938">The following example shows a call to the getItemPos method to return the position of each item in the form list control.</span></span> <span data-ttu-id="50dbc-939">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-939">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-940">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-940">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    boolean columnadd; 
    str string; 
    container conAccountNum; 
    container itemPos; 
    CustTable custTable; 
    int numAccounts; 
    int numItems; 
    int i; 
    int x; 
    int item; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add an item to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
        itemPos = formListControl.getItemPos(item); 
        numItems = conlen(itemPos); 
        for(x = 1; x<= numItems; x++) 
        { 
            print conpeek(itemPos,x); 
            pause; 
        } 
    } 
}
```

## <a name="method-getnextitem"></a><span data-ttu-id="50dbc-941">メソッド getNextItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-941">Method getNextItem</span></span>

<span data-ttu-id="50dbc-942">フォーム リスト コントロール内の次の項目の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-942">Retrieves the number of the next item in a form list control.</span></span>

```xpp
public int getNextItem(FormListNext nextType, [int startIdx])
```

### <a name="parameters---getnextitem"></a><span data-ttu-id="50dbc-943">パラメーター - getNextItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-943">Parameters - getNextItem</span></span>

<span data-ttu-id="50dbc-944">nextType</span><span class="sxs-lookup"><span data-stu-id="50dbc-944">nextType</span></span>  
<span data-ttu-id="50dbc-945">次の項目の前にある項目を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-945">An Integer data type that specifies the item that is before the next item.</span></span>

<!-- -->

<span data-ttu-id="50dbc-946">startIdx</span><span class="sxs-lookup"><span data-stu-id="50dbc-946">startIdx</span></span>  
<span data-ttu-id="50dbc-947">次の項目の前にある項目を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-947">An Integer data type that specifies the item that is before the next item.</span></span>

### <a name="return-value---getnextitem"></a><span data-ttu-id="50dbc-948">戻り値 - getNextItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-948">Return Value - getNextItem</span></span>

<span data-ttu-id="50dbc-949">フォーム リスト コントロールでどの項目が次の品目であるかを示す整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-949">An Integer data type value that indicates which item is the next item in a form list control.</span></span>

### <a name="examples---getnextitem"></a><span data-ttu-id="50dbc-950">例 - getNextItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-950">Examples - getNextItem</span></span>

<span data-ttu-id="50dbc-951">次の例は、フォーム リスト コントロールの次の項目数を取得する getNextItem メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-951">The following example shows a call to the getNextItem method to retrieve the number of the next item in the form list control.</span></span> <span data-ttu-id="50dbc-952">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-952">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-953">変数内の品目は、フォーム リスト コントロールの一覧の管理に追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-953">The items in the variable are added to the form list control.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    boolean columnadd; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(77); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = new FormRun(Args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add an item to the form list control. 
    while select custTable 
       where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        formListControl.addItem(formListItem); 
    } 
    item = formListControl.getNextItem(FormListNext::ToRight); 
}
```

## <a name="method-getselectedcount"></a><span data-ttu-id="50dbc-954">メソッド getSelectedCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-954">Method getSelectedCount</span></span>

<span data-ttu-id="50dbc-955">フォーム リスト コントロールで選択されている項目の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-955">Retrieves the number of items that are selected in a form list control.</span></span>

```xpp
public int getSelectedCount()
```

### <a name="return-value---getselectedcount"></a><span data-ttu-id="50dbc-956">戻り値 - getSelectedCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-956">Return Value - getSelectedCount</span></span>

<span data-ttu-id="50dbc-957">フォーム リスト コントロールで選択されている品目の数を示す整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-957">An Integer data type value that indicates the number of items that are selected in a form list control.</span></span>

### <a name="examples---getselectedcount"></a><span data-ttu-id="50dbc-958">例 - getSelectedCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-958">Examples - getSelectedCount</span></span>

<span data-ttu-id="50dbc-959">次の例は、フォーム リスト コントロールの選択した項目数を返す getSelectedCount メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-959">The following example shows a call to the getSelectedCount method to return the number of items that are selected in the form list control.</span></span> <span data-ttu-id="50dbc-960">FormListControl.singleSelection メソッドは、複数の項目を選択するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-960">The FormListControl.singleSelection method indicates whether multiple items can be selected.</span></span> <span data-ttu-id="50dbc-961">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-961">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-962">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-962">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    int numItemsSel; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    formListControl.singleSelection(false); 
    // Add columns to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1",1,120)); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    numItemsSel = formListControl.getSelectedCount(); 
}
```

## <a name="method-getstringwidth"></a><span data-ttu-id="50dbc-963">メソッド getStringWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-963">Method getStringWidth</span></span>

```xpp
public int getStringWidth(str Text)
```

### <a name="parameters---getstringwidth"></a><span data-ttu-id="50dbc-964">パラメーター - getStringWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-964">Parameters - getStringWidth</span></span>

<span data-ttu-id="50dbc-965">テキスト</span><span class="sxs-lookup"><span data-stu-id="50dbc-965">Text</span></span>  

### <a name="return-value---getstringwidth"></a><span data-ttu-id="50dbc-966">戻り値 - getStringWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-966">Return Value - getStringWidth</span></span>

## <a name="method-gettopindex"></a><span data-ttu-id="50dbc-967">メソッド getTopIndex</span><span class="sxs-lookup"><span data-stu-id="50dbc-967">Method getTopIndex</span></span>

```xpp
public int getTopIndex()
```

### <a name="return-value---gettopindex"></a><span data-ttu-id="50dbc-968">戻り値 - getTopIndex</span><span class="sxs-lookup"><span data-stu-id="50dbc-968">Return Value - getTopIndex</span></span>

## <a name="method-gridlines"></a><span data-ttu-id="50dbc-969">メソッド gridLines</span><span class="sxs-lookup"><span data-stu-id="50dbc-969">Method gridLines</span></span>

```xpp
public boolean gridLines([boolean value])
```

### <a name="parameters---gridlines"></a><span data-ttu-id="50dbc-970">パラメーター - gridLines</span><span class="sxs-lookup"><span data-stu-id="50dbc-970">Parameters - gridLines</span></span>

<span data-ttu-id="50dbc-971">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-971">value</span></span>  

### <a name="return-value---gridlines"></a><span data-ttu-id="50dbc-972">戻り値 - gridLines</span><span class="sxs-lookup"><span data-stu-id="50dbc-972">Return Value - gridLines</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="50dbc-973">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="50dbc-973">Method hasChanged</span></span>

<span data-ttu-id="50dbc-974">コントロールの内容が変更されたかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-974">Sets or returns a value that indicates whether the contents of the control have changed.</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="50dbc-975">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="50dbc-975">Parameters - hasChanged</span></span>

<span data-ttu-id="50dbc-976">val</span><span class="sxs-lookup"><span data-stu-id="50dbc-976">val</span></span>  
<span data-ttu-id="50dbc-977">コントロールの hasChanged 値として割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-977">The value to assign as the hasChanged value for the control; optional.</span></span>

### <a name="return-value---haschanged"></a><span data-ttu-id="50dbc-978">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="50dbc-978">Return Value - hasChanged</span></span>

<span data-ttu-id="50dbc-979">コントロールの内容が変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-979">true if the contents of the control have changed; otherwise, false.</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="50dbc-980">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="50dbc-980">Method hasUserSetting</span></span>

<span data-ttu-id="50dbc-981">コントロールにカスタム ユーザー設定があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-981">Indicates whether the control has custom user settings.</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="50dbc-982">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="50dbc-982">Return Value - hasUserSetting</span></span>

<span data-ttu-id="50dbc-983">コントロールにカスタム ユーザー設定がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-983">true if the control has custom user settings; otherwise, false.</span></span>

## <a name="method-headerdragdrop"></a><span data-ttu-id="50dbc-984">メソッド headerdragdrop</span><span class="sxs-lookup"><span data-stu-id="50dbc-984">Method headerdragdrop</span></span>

```xpp
public boolean headerdragdrop([boolean value])
```

### <a name="parameters---headerdragdrop"></a><span data-ttu-id="50dbc-985">パラメーター - headerdragdrop</span><span class="sxs-lookup"><span data-stu-id="50dbc-985">Parameters - headerdragdrop</span></span>

<span data-ttu-id="50dbc-986">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-986">value</span></span>  

### <a name="return-value---headerdragdrop"></a><span data-ttu-id="50dbc-987">戻り値 - headerdragdrop</span><span class="sxs-lookup"><span data-stu-id="50dbc-987">Return Value - headerdragdrop</span></span>

## <a name="method-height"></a><span data-ttu-id="50dbc-988">メソッド height</span><span class="sxs-lookup"><span data-stu-id="50dbc-988">Method height</span></span>

<span data-ttu-id="50dbc-989">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-989">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="50dbc-990">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="50dbc-990">Parameters - height</span></span>

<span data-ttu-id="50dbc-991">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-991">value</span></span>  
<span data-ttu-id="50dbc-992">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-992">An integer that indicates how the height is calculated; optional.</span></span> <span data-ttu-id="50dbc-993">これは、次のいずれかの値になります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-993">This can be one of the following values:</span></span>

<!-- -->

<span data-ttu-id="50dbc-994">モード</span><span class="sxs-lookup"><span data-stu-id="50dbc-994">mode</span></span>  
<span data-ttu-id="50dbc-995">高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-995">An integer that indicates how the height is calculated; optional.</span></span> <span data-ttu-id="50dbc-996">これは、次のいずれかの値になります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-996">This can be one of the following values:</span></span>

### <a name="return-value---height"></a><span data-ttu-id="50dbc-997">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="50dbc-997">Return Value - height</span></span>

<span data-ttu-id="50dbc-998">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="50dbc-998">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="50dbc-999">備考 - height</span><span class="sxs-lookup"><span data-stu-id="50dbc-999">Remarks - height</span></span>

<span data-ttu-id="50dbc-1000">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1000">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="50dbc-1001">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1001">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="50dbc-1002">モード</span><span class="sxs-lookup"><span data-stu-id="50dbc-1002">Mode</span></span>              | <span data-ttu-id="50dbc-1003">高さの計算</span><span class="sxs-lookup"><span data-stu-id="50dbc-1003">Height calculation</span></span>                                                                         |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="50dbc-1004">-1 � 正確</span><span class="sxs-lookup"><span data-stu-id="50dbc-1004">-1 � Exact</span></span>        | <span data-ttu-id="50dbc-1005">ピクセル単位のコントロールの正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1005">The exact height of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="50dbc-1006">0 � 自動</span><span class="sxs-lookup"><span data-stu-id="50dbc-1006">0 � Auto</span></span>          | <span data-ttu-id="50dbc-1007">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1007">The height of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="50dbc-1008">1 � 列の高さ</span><span class="sxs-lookup"><span data-stu-id="50dbc-1008">1 � Column height</span></span> | <span data-ttu-id="50dbc-1009">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1009">The layout of the form determines the height of the control.</span></span>                               |

<span data-ttu-id="50dbc-1010">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1010">The height and the height calculation mode can be set separately.</span></span>

### <a name="examples---height"></a><span data-ttu-id="50dbc-1011">例 - height</span><span class="sxs-lookup"><span data-stu-id="50dbc-1011">Examples - height</span></span>

<span data-ttu-id="50dbc-1012">次の例は、コントロールの高さを 120 ピクセルに設定する height メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1012">The following example shows a call to the height method to the set the height of the control to 120 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form, and then specifiy the control height. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.height(120,-1); 
}
```

## <a name="method-heightmode"></a><span data-ttu-id="50dbc-1013">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1013">Method heightMode</span></span>

<span data-ttu-id="50dbc-1014">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1014">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="50dbc-1015">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1015">Parameters - heightMode</span></span>

<span data-ttu-id="50dbc-1016">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1016">value</span></span>  
<span data-ttu-id="50dbc-1017">コントロールの高さの計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1017">An integer that indicates how the height of the control is calculated; optional.</span></span> <span data-ttu-id="50dbc-1018">この値は、 Exact モードの場合は -1、Auto モードの場合は 0、Column height 幅の場合は 1 になります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1018">This value can be -1 for Exact mode, 0 for Auto mode, or 1 for Column height width.</span></span>

### <a name="return-value---heightmode"></a><span data-ttu-id="50dbc-1019">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1019">Return Value - heightMode</span></span>

<span data-ttu-id="50dbc-1020">高さ計算モード。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1020">The height calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="50dbc-1021">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1021">Remarks - heightMode</span></span>

<span data-ttu-id="50dbc-1022">次の表に従って高さを計算します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1022">Calculate the height according to the following table.</span></span>

| <span data-ttu-id="50dbc-1023">モード</span><span class="sxs-lookup"><span data-stu-id="50dbc-1023">Mode</span></span>          | <span data-ttu-id="50dbc-1024">高さの計算</span><span class="sxs-lookup"><span data-stu-id="50dbc-1024">Height calculation</span></span>                                                                         |
|---------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="50dbc-1025">正確</span><span class="sxs-lookup"><span data-stu-id="50dbc-1025">Exact</span></span>         | <span data-ttu-id="50dbc-1026">ピクセル単位のコントロールの正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1026">The exact height of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="50dbc-1027">自動</span><span class="sxs-lookup"><span data-stu-id="50dbc-1027">Auto</span></span>          | <span data-ttu-id="50dbc-1028">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1028">The height of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="50dbc-1029">1 列の高さ</span><span class="sxs-lookup"><span data-stu-id="50dbc-1029">Column height</span></span> | <span data-ttu-id="50dbc-1030">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1030">The layout of the form determines the height of the control.</span></span>                               |

<span data-ttu-id="50dbc-1031">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1031">The height of the control might change when the calculation mode is set to Auto or Column height.</span></span>

### <a name="examples---heightmode"></a><span data-ttu-id="50dbc-1032">例 - heightMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1032">Examples - heightMode</span></span>

<span data-ttu-id="50dbc-1033">次の例は、正確なピクセル値に基づいてコントロールの高さを調整する heightMode メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1033">The following example shows a call to the heightMode method to adjust the height of the control, based on an exact pixel value.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form, and then specifiy the control height. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.heightMode(-1); 
    formListControl.heightValue(120); 
}
```

## <a name="method-heightvalue"></a><span data-ttu-id="50dbc-1034">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1034">Method heightValue</span></span>

<span data-ttu-id="50dbc-1035">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1035">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="50dbc-1036">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1036">Parameters - heightValue</span></span>

<span data-ttu-id="50dbc-1037">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1037">value</span></span>  
<span data-ttu-id="50dbc-1038">高さをピクセル単位で指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1038">An Integer data type that specifies the height in pixels.</span></span>

### <a name="return-value---heightvalue"></a><span data-ttu-id="50dbc-1039">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1039">Return Value - heightValue</span></span>

<span data-ttu-id="50dbc-1040">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1040">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="50dbc-1041">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1041">Remarks - heightValue</span></span>

<span data-ttu-id="50dbc-1042">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1042">The height of the control is not changed unless the Exact height calculation mode is used.</span></span>

### <a name="examples---heightvalue"></a><span data-ttu-id="50dbc-1043">例 - heightValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1043">Examples - heightValue</span></span>

<span data-ttu-id="50dbc-1044">次の例は、高さを 120 ピクセルに設定する heightValue メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1044">The following example shows a call to the heightValue method that sets the height to 120 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form, and then specifiy the control height. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.heightMode(-1); 
    formListControl.heightValue(120); 
}
```

## <a name="method-helpfield"></a><span data-ttu-id="50dbc-1045">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="50dbc-1045">Method helpField</span></span>

<span data-ttu-id="50dbc-1046">コントロールのヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1046">Retrieves the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="50dbc-1047">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="50dbc-1047">Return Value - helpField</span></span>

<span data-ttu-id="50dbc-1048">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1048">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="remarks---helpfield"></a><span data-ttu-id="50dbc-1049">備考 - helpField</span><span class="sxs-lookup"><span data-stu-id="50dbc-1049">Remarks - helpField</span></span>

<span data-ttu-id="50dbc-1050">helpField メソッドを使用してヘルプテキストの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1050">The helpField method cannot be used to set the value of the Help text.</span></span> <span data-ttu-id="50dbc-1051">ヘルプ テキストの値を設定するには、helpText メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1051">Use the helpText method to set the value of the Help text.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="50dbc-1052">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="50dbc-1052">Method helpText</span></span>

<span data-ttu-id="50dbc-1053">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1053">Gets or sets the Help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="50dbc-1054">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="50dbc-1054">Parameters - helpText</span></span>

<span data-ttu-id="50dbc-1055">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1055">value</span></span>  
<span data-ttu-id="50dbc-1056">コントロールのヘルプ テキストとして割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1056">The value that is assigned as the Help text for the control.</span></span>

### <a name="return-value---helptext"></a><span data-ttu-id="50dbc-1057">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="50dbc-1057">Return Value - helpText</span></span>

<span data-ttu-id="50dbc-1058">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1058">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="50dbc-1059">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="50dbc-1059">Remarks - helpText</span></span>

<span data-ttu-id="50dbc-1060">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1060">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="50dbc-1061">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1061">The Help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="50dbc-1062">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="50dbc-1062">Method hierarchyParent</span></span>

<span data-ttu-id="50dbc-1063">コントロールの HierarchyParent プロパティ値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1063">Gets or sets the HierarchyParent property value of the control.</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="50dbc-1064">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="50dbc-1064">Parameters - hierarchyParent</span></span>

<span data-ttu-id="50dbc-1065">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1065">value</span></span>  
<span data-ttu-id="50dbc-1066">コントロールの HierarchyParent プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1066">The value to assign to the HierarchyParent property of the control.</span></span>

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="50dbc-1067">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="50dbc-1067">Return Value - hierarchyParent</span></span>

<span data-ttu-id="50dbc-1068">コントロールの HierarchyParent プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1068">The HierarchyParent property value of the control.</span></span>

## <a name="method-hittest"></a><span data-ttu-id="50dbc-1069">メソッド hitTest</span><span class="sxs-lookup"><span data-stu-id="50dbc-1069">Method hitTest</span></span>

```xpp
public container hitTest(int x, int y)
```

### <a name="parameters---hittest"></a><span data-ttu-id="50dbc-1070">パラメーター - hitTest</span><span class="sxs-lookup"><span data-stu-id="50dbc-1070">Parameters - hitTest</span></span>

<span data-ttu-id="50dbc-1071">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-1071">x</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1072">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-1072">y</span></span>  

### <a name="return-value---hittest"></a><span data-ttu-id="50dbc-1073">戻り値 - hitTest</span><span class="sxs-lookup"><span data-stu-id="50dbc-1073">Return Value - hitTest</span></span>

## <a name="method-hittestsubitem"></a><span data-ttu-id="50dbc-1074">メソッド hitTestSubItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1074">Method hitTestSubItem</span></span>

```xpp
public container hitTestSubItem(int x, int y)
```

### <a name="parameters---hittestsubitem"></a><span data-ttu-id="50dbc-1075">パラメーター - hitTestSubItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1075">Parameters - hitTestSubItem</span></span>

<span data-ttu-id="50dbc-1076">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-1076">x</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1077">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-1077">y</span></span>  

### <a name="return-value---hittestsubitem"></a><span data-ttu-id="50dbc-1078">戻り値 - hitTestSubItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1078">Return Value - hitTestSubItem</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="50dbc-1079">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="50dbc-1079">Method hWnd</span></span>

<span data-ttu-id="50dbc-1080">コントロールの Windows ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1080">Retrieves the Windows handle for the control.</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="50dbc-1081">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="50dbc-1081">Return Value - hWnd</span></span>

<span data-ttu-id="50dbc-1082">ハンドラーコントロールのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1082">The handle for the control.</span></span>

### <a name="remarks---hwnd"></a><span data-ttu-id="50dbc-1083">備考 - hWnd</span><span class="sxs-lookup"><span data-stu-id="50dbc-1083">Remarks - hWnd</span></span>

<span data-ttu-id="50dbc-1084">この処理は、Windows API で使用できます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1084">The handle can be used with the Windows API.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="50dbc-1085">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="50dbc-1085">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="50dbc-1086">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="50dbc-1086">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="50dbc-1087">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="50dbc-1087">Method isDisplayed</span></span>

<span data-ttu-id="50dbc-1088">コントロールが表示されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1088">Retrieves a value that indicates whether the control is displayed.</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="50dbc-1089">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="50dbc-1089">Return Value - isDisplayed</span></span>

<span data-ttu-id="50dbc-1090">コントロールが表示される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1090">true if the control is displayed; otherwise, false.</span></span>

### <a name="remarks---isdisplayed"></a><span data-ttu-id="50dbc-1091">備考 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="50dbc-1091">Remarks - isDisplayed</span></span>

<span data-ttu-id="50dbc-1092">コントロールの表示の状態を変更するには、表示されているメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1092">To modify the visible state of the control, call the visible method.</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="50dbc-1093">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="50dbc-1093">Method isRestricted</span></span>

<span data-ttu-id="50dbc-1094">コントロールが制限されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1094">Retrieves a value that indicates whether the control is restricted.</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="50dbc-1095">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="50dbc-1095">Return Value - isRestricted</span></span>

<span data-ttu-id="50dbc-1096">コントロールが制限される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1096">true if the control is restricted; otherwise, false.</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="50dbc-1097">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="50dbc-1097">Method isUserSetupEnabled</span></span>

<span data-ttu-id="50dbc-1098">コントロールが、特定のレベルのカスタマイズを許可するかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1098">Gets a value that indicates whether the control allows for the specified level of customization.</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="50dbc-1099">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="50dbc-1099">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="50dbc-1100">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="50dbc-1100">neededSetupRights</span></span>  
<span data-ttu-id="50dbc-1101">コントロールに対して照会されるカスタマイズのレベルを指定する FormAllowUserSetup 列挙値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1101">A FormAllowUserSetup enumeration value that specifies the level of customization that is being queried for the control.</span></span>

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="50dbc-1102">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="50dbc-1102">Return Value - isUserSetupEnabled</span></span>

<span data-ttu-id="50dbc-1103">neededSetupRights パラメーターで指定されたカスタマイズのレベルがコントロール、デザイン、および親コンテナーで許可される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1103">true if the control, design, and parent containers allow for the level of customization that is specified by the neededSetupRights parameter; otherwise, false.</span></span>

### <a name="remarks---isusersetupenabled"></a><span data-ttu-id="50dbc-1104">備考 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="50dbc-1104">Remarks - isUserSetupEnabled</span></span>

<span data-ttu-id="50dbc-1105">「true」を返すこのメソッドについては、デザインの AllowUserSetup プロパティとすべての親コンテナが、neededSetupRights パラメータで指定されたアクセスレベルを許可している必要があります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1105">For this method to return true, the AllowUserSetup property for the design and all parent containers must allow for the level of access that is specified by the neededSetupRights parameter.</span></span> <span data-ttu-id="50dbc-1106">次のテーブルでは、neededSetupRights パラメーターの値について説明します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1106">The following table describes the values for the neededSetupRights parameter.</span></span>

|                                  |                                                                                                                                  |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50dbc-1107">FormAllowUserSetup::No 0</span><span class="sxs-lookup"><span data-stu-id="50dbc-1107">FormAllowUserSetup::No 0</span></span>         | <span data-ttu-id="50dbc-1108">コントロールに対する変更は加えられません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1108">No changes can be made to the control.</span></span> <span data-ttu-id="50dbc-1109">この値が neededSetupRights パラメーターに対して設定されている場合、メソッドは常に true を返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1109">If this value is set for the neededSetupRights parameter, the method always returns true.</span></span> |
| <span data-ttu-id="50dbc-1110">FormAllowUserSetup::Restricted 1</span><span class="sxs-lookup"><span data-stu-id="50dbc-1110">FormAllowUserSetup::Restricted 1</span></span> | <span data-ttu-id="50dbc-1111">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1111">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="50dbc-1112">ユーザーがコントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1112">The user cannot move the control.</span></span>   |
| <span data-ttu-id="50dbc-1113">FormAllowUserSetup::Yes 2</span><span class="sxs-lookup"><span data-stu-id="50dbc-1113">FormAllowUserSetup::Yes 2</span></span>        | <span data-ttu-id="50dbc-1114">ユーザーはコントロールの、編集可能、表示、スキップ、ラベル、幅の各プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1114">The user can change the editable, visible, skip, label, and width properties of the control.</span></span> <span data-ttu-id="50dbc-1115">ユーザーはコントロールを移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1115">The user can also move the control.</span></span> |

### <a name="examples---isusersetupenabled"></a><span data-ttu-id="50dbc-1116">例 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="50dbc-1116">Examples - isUserSetupEnabled</span></span>

<span data-ttu-id="50dbc-1117">次の例は、コントロールのユーザー設定権限を決定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1117">The following example shows how to determine the user setup rights for a control.</span></span>

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

## <a name="method-italic"></a><span data-ttu-id="50dbc-1118">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="50dbc-1118">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="50dbc-1119">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="50dbc-1119">Parameters - italic</span></span>

<span data-ttu-id="50dbc-1120">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1120">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="50dbc-1121">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="50dbc-1121">Return Value - italic</span></span>

## <a name="method-itemalign"></a><span data-ttu-id="50dbc-1122">メソッド itemAlign</span><span class="sxs-lookup"><span data-stu-id="50dbc-1122">Method itemAlign</span></span>

```xpp
public int itemAlign([int value])
```

### <a name="parameters---itemalign"></a><span data-ttu-id="50dbc-1123">パラメーター - itemAlign</span><span class="sxs-lookup"><span data-stu-id="50dbc-1123">Parameters - itemAlign</span></span>

<span data-ttu-id="50dbc-1124">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1124">value</span></span>  

### <a name="return-value---itemalign"></a><span data-ttu-id="50dbc-1125">戻り値 - itemAlign</span><span class="sxs-lookup"><span data-stu-id="50dbc-1125">Return Value - itemAlign</span></span>

## <a name="method-itemchanging"></a><span data-ttu-id="50dbc-1126">メソッド itemChanging</span><span class="sxs-lookup"><span data-stu-id="50dbc-1126">Method itemChanging</span></span>

```xpp
public boolean itemChanging(int Idx, AnyType Data)
```

### <a name="parameters---itemchanging"></a><span data-ttu-id="50dbc-1127">パラメーター - itemChanging</span><span class="sxs-lookup"><span data-stu-id="50dbc-1127">Parameters - itemChanging</span></span>

<span data-ttu-id="50dbc-1128">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1128">Idx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1129">データ</span><span class="sxs-lookup"><span data-stu-id="50dbc-1129">Data</span></span>  

### <a name="return-value---itemchanging"></a><span data-ttu-id="50dbc-1130">戻り値 - itemChanging</span><span class="sxs-lookup"><span data-stu-id="50dbc-1130">Return Value - itemChanging</span></span>

## <a name="method-keydown"></a><span data-ttu-id="50dbc-1131">メソッド keyDown</span><span class="sxs-lookup"><span data-stu-id="50dbc-1131">Method keyDown</span></span>

```xpp
public boolean keyDown(int vKey, boolean Ctrl, boolean Shift)
```

### <a name="parameters---keydown"></a><span data-ttu-id="50dbc-1132">パラメーター - keyDown</span><span class="sxs-lookup"><span data-stu-id="50dbc-1132">Parameters - keyDown</span></span>

<span data-ttu-id="50dbc-1133">vKey</span><span class="sxs-lookup"><span data-stu-id="50dbc-1133">vKey</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1134">Ctrl</span><span class="sxs-lookup"><span data-stu-id="50dbc-1134">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1135">Shift</span><span class="sxs-lookup"><span data-stu-id="50dbc-1135">Shift</span></span>  

### <a name="return-value---keydown"></a><span data-ttu-id="50dbc-1136">戻り値 - keyDown</span><span class="sxs-lookup"><span data-stu-id="50dbc-1136">Return Value - keyDown</span></span>

## <a name="method-leave"></a><span data-ttu-id="50dbc-1137">メソッド leave</span><span class="sxs-lookup"><span data-stu-id="50dbc-1137">Method leave</span></span>

<span data-ttu-id="50dbc-1138">ユーザーがフォーム リスト コントロールからフォーカスを移動したら識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1138">Identifies when a user moves focus away from a form list control.</span></span>

```xpp
public boolean leave()
```

### <a name="return-value---leave"></a><span data-ttu-id="50dbc-1139">戻り値 - leave</span><span class="sxs-lookup"><span data-stu-id="50dbc-1139">Return Value - leave</span></span>

<span data-ttu-id="50dbc-1140">フォーカスがコントロールから移動された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1140">true if focus is moved away from the control; otherwise, false.</span></span>

### <a name="remarks---leave"></a><span data-ttu-id="50dbc-1141">備考 - leave</span><span class="sxs-lookup"><span data-stu-id="50dbc-1141">Remarks - leave</span></span>

<span data-ttu-id="50dbc-1142">フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[leave] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1142">To override this method in a form list control, right-click the Methods node below the control, point to Override Method, and then click leave.</span></span> <span data-ttu-id="50dbc-1143">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1143">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-left"></a><span data-ttu-id="50dbc-1144">メソッド left</span><span class="sxs-lookup"><span data-stu-id="50dbc-1144">Method left</span></span>

<span data-ttu-id="50dbc-1145">フォーム リスト コントロールの水平位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1145">Sets or returns the horizontal position of a form list control in pixels, and specifies how the position is calculated.</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="50dbc-1146">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="50dbc-1146">Parameters - left</span></span>

<span data-ttu-id="50dbc-1147">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1147">value</span></span>  
<span data-ttu-id="50dbc-1148">位置の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1148">An integer that indicates how the position is calculated; optional.</span></span> <span data-ttu-id="50dbc-1149">これは、次のいずれかの値になります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1149">This can be one of the following values:</span></span>

<!-- -->

<span data-ttu-id="50dbc-1150">モード</span><span class="sxs-lookup"><span data-stu-id="50dbc-1150">mode</span></span>  
<span data-ttu-id="50dbc-1151">位置の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1151">An integer that indicates how the position is calculated; optional.</span></span> <span data-ttu-id="50dbc-1152">これは、次のいずれかの値になります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1152">This can be one of the following values:</span></span>

### <a name="return-value---left"></a><span data-ttu-id="50dbc-1153">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="50dbc-1153">Return Value - left</span></span>

<span data-ttu-id="50dbc-1154">フォーム リスト コントロールの水平位置をピクセル単位で示す整数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1154">An integer that indicates the horizontal position of a form list control in pixels.</span></span>

### <a name="examples---left"></a><span data-ttu-id="50dbc-1155">例 - left</span><span class="sxs-lookup"><span data-stu-id="50dbc-1155">Examples - left</span></span>

<span data-ttu-id="50dbc-1156">次の例は、水平方向の位置を 50 ピクセルに設定する left メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1156">The following example shows a call to the left method that sets the horizontal position to 50 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.left(50,-1); 
}
```

## <a name="method-leftmode"></a><span data-ttu-id="50dbc-1157">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1157">Method leftMode</span></span>

<span data-ttu-id="50dbc-1158">フォーム リスト コントロールの水平位置を計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1158">Sets or returns a value that indicates how the horizontal position of a form list control is calculated.</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="50dbc-1159">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1159">Parameters - leftMode</span></span>

<span data-ttu-id="50dbc-1160">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1160">value</span></span>  
<span data-ttu-id="50dbc-1161">水平位置の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1161">An integer that indicates how the horizontal position is calculated; optional.</span></span>

### <a name="return-value---leftmode"></a><span data-ttu-id="50dbc-1162">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1162">Return Value - leftMode</span></span>

<span data-ttu-id="50dbc-1163">水平位置の計算方法を示す整数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1163">An integer that indicates how the horizontal position is calculated.</span></span> <span data-ttu-id="50dbc-1164">戻り値は、-1 または FormLeft 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1164">The return value can be -1 or a FormLeft enumeration value.</span></span>

### <a name="remarks---leftmode"></a><span data-ttu-id="50dbc-1165">備考 - leftMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1165">Remarks - leftMode</span></span>

<span data-ttu-id="50dbc-1166">value パラメーターと戻り値は、水平位置の計算方法を指定する整数値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1166">The value parameter and the return value are integer values that specify how the horizontal position is calculated.</span></span> <span data-ttu-id="50dbc-1167">この値は、正確なピクセル値の場合は -1、FormLeft 列挙値の場合は -1 のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1167">This value can be either -1 for an exact pixel value or a FormLeft enumeration value.</span></span> <span data-ttu-id="50dbc-1168">詳細については、「FormLeft 列挙」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1168">For more information, see FormLeft Enumeration.</span></span>

### <a name="examples---leftmode"></a><span data-ttu-id="50dbc-1169">例 - leftMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1169">Examples - leftMode</span></span>

<span data-ttu-id="50dbc-1170">次の例は、正確なピクセル値に基づいて、フォーム リスト コントロールの水平方向位置を計算する leftMode メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1170">The following example shows a call to the leftMode method that calculates the horizontal position of a form list control, based on an exact pixel value.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form.  
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.leftMode(-1); 
    formListControl.leftValue(100); 
}
```

## <a name="method-leftvalue"></a><span data-ttu-id="50dbc-1171">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1171">Method leftValue</span></span>

<span data-ttu-id="50dbc-1172">フォーム リスト コントロールの水平位置をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1172">Sets or returns the horizontal position of a form list control in pixels.</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="50dbc-1173">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1173">Parameters - leftValue</span></span>

<span data-ttu-id="50dbc-1174">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1174">value</span></span>  
<span data-ttu-id="50dbc-1175">水平位置をピクセル単位で示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1175">An integer that indicates the horizontal position in pixels; optional.</span></span>

### <a name="return-value---leftvalue"></a><span data-ttu-id="50dbc-1176">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1176">Return Value - leftValue</span></span>

<span data-ttu-id="50dbc-1177">水平位置をピクセル単位で示す整数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1177">An integer that indicates the horizontal position in pixels.</span></span>

### <a name="remarks---leftvalue"></a><span data-ttu-id="50dbc-1178">備考 - leftValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1178">Remarks - leftValue</span></span>

<span data-ttu-id="50dbc-1179">正確なピクセル値に左モードが設定されていない限り、水平位置は変更されません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1179">The horizontal position is not changed unless the left mode is set for an exact pixel value.</span></span> <span data-ttu-id="50dbc-1180">詳細については、「leftMode」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1180">For more information, see leftMode.</span></span>

### <a name="examples---leftvalue"></a><span data-ttu-id="50dbc-1181">例 - leftValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1181">Examples - leftValue</span></span>

<span data-ttu-id="50dbc-1182">次の例は、水平方向の位置を 100 ピクセルに設定する leftValue メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1182">The following example shows a call to the leftValue method that sets the horizontal position to 100 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form, and then specifiy the control height. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.leftMode(-1); 
    formListControl.leftValue(100); 
}
```

## <a name="method-markasuseradd"></a><span data-ttu-id="50dbc-1183">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="50dbc-1183">Method markAsUserAdd</span></span>

<span data-ttu-id="50dbc-1184">ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1184">Marks or unmarks the control as a user-added control.</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="50dbc-1185">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="50dbc-1185">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="50dbc-1186">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1186">value</span></span>  
<span data-ttu-id="50dbc-1187">ユーザーが追加したコントロールとして、コントロールをマークする必要があるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1187">The Boolean value that indicates whether the control should be marked as a user-added control.</span></span>

### <a name="return-value---markasuseradd"></a><span data-ttu-id="50dbc-1188">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="50dbc-1188">Return Value - markAsUserAdd</span></span>

<span data-ttu-id="50dbc-1189">コントロールがユーザーにより追加されたコントロールとしてマークされていた場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1189">true if the control was marked as a user-added control; otherwise, false.</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="50dbc-1190">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="50dbc-1190">Method mouseDblClick</span></span>

<span data-ttu-id="50dbc-1191">コントロールがユーザーにダブルクリックされると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1191">Is called when the control is double-clicked by the user.</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="50dbc-1192">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="50dbc-1192">Parameters - mouseDblClick</span></span>

<span data-ttu-id="50dbc-1193">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-1193">x</span></span>  
<span data-ttu-id="50dbc-1194">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1194">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1195">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-1195">y</span></span>  
<span data-ttu-id="50dbc-1196">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1196">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1197">ボタン</span><span class="sxs-lookup"><span data-stu-id="50dbc-1197">button</span></span>  
<span data-ttu-id="50dbc-1198">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1198">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1199">Ctrl</span><span class="sxs-lookup"><span data-stu-id="50dbc-1199">Ctrl</span></span>  
<span data-ttu-id="50dbc-1200">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1200">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1201">シフト</span><span class="sxs-lookup"><span data-stu-id="50dbc-1201">Shift</span></span>  
<span data-ttu-id="50dbc-1202">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1202">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedblclick"></a><span data-ttu-id="50dbc-1203">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="50dbc-1203">Return Value - mouseDblClick</span></span>

<span data-ttu-id="50dbc-1204">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1204">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedblclick"></a><span data-ttu-id="50dbc-1205">備考 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="50dbc-1205">Remarks - mouseDblClick</span></span>

<span data-ttu-id="50dbc-1206">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1206">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="50dbc-1207">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="50dbc-1207">Method mouseDown</span></span>

<span data-ttu-id="50dbc-1208">ユーザーがコントロール上でマウス ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1208">Is called when the user clicks the mouse button over the control.</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="50dbc-1209">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="50dbc-1209">Parameters - mouseDown</span></span>

<span data-ttu-id="50dbc-1210">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-1210">x</span></span>  
<span data-ttu-id="50dbc-1211">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1211">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1212">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-1212">y</span></span>  
<span data-ttu-id="50dbc-1213">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1213">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1214">ボタン</span><span class="sxs-lookup"><span data-stu-id="50dbc-1214">button</span></span>  
<span data-ttu-id="50dbc-1215">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1215">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1216">Ctrl</span><span class="sxs-lookup"><span data-stu-id="50dbc-1216">Ctrl</span></span>  
<span data-ttu-id="50dbc-1217">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1217">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1218">シフト</span><span class="sxs-lookup"><span data-stu-id="50dbc-1218">Shift</span></span>  
<span data-ttu-id="50dbc-1219">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1219">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousedown"></a><span data-ttu-id="50dbc-1220">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="50dbc-1220">Return Value - mouseDown</span></span>

<span data-ttu-id="50dbc-1221">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1221">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousedown"></a><span data-ttu-id="50dbc-1222">備考 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="50dbc-1222">Remarks - mouseDown</span></span>

<span data-ttu-id="50dbc-1223">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1223">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span> <span data-ttu-id="50dbc-1224">このイベントは、コントロールのラベルに値が指定され、コントロールの ShowLabel プロパティが [はい] に設定されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1224">This event is called only if a value is specified for the label of the control and the ShowLabel property of the control is set to Yes.</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="50dbc-1225">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="50dbc-1225">Method mouseMove</span></span>

<span data-ttu-id="50dbc-1226">ユーザーがマウス ポインターをコントロール上に移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1226">Is called when the user moves the mouse pointer over the control.</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="50dbc-1227">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="50dbc-1227">Parameters - mouseMove</span></span>

<span data-ttu-id="50dbc-1228">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-1228">x</span></span>  
<span data-ttu-id="50dbc-1229">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1229">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1230">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-1230">y</span></span>  
<span data-ttu-id="50dbc-1231">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1231">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1232">ボタン</span><span class="sxs-lookup"><span data-stu-id="50dbc-1232">button</span></span>  
<span data-ttu-id="50dbc-1233">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1233">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1234">Ctrl</span><span class="sxs-lookup"><span data-stu-id="50dbc-1234">Ctrl</span></span>  
<span data-ttu-id="50dbc-1235">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1235">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1236">シフト</span><span class="sxs-lookup"><span data-stu-id="50dbc-1236">Shift</span></span>  
<span data-ttu-id="50dbc-1237">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1237">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mousemove"></a><span data-ttu-id="50dbc-1238">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="50dbc-1238">Return Value - mouseMove</span></span>

<span data-ttu-id="50dbc-1239">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1239">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mousemove"></a><span data-ttu-id="50dbc-1240">備考 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="50dbc-1240">Remarks - mouseMove</span></span>

<span data-ttu-id="50dbc-1241">通常、このメソッドがオーバーライドされると、super メソッドの呼び出しからの戻り値が返されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1241">Typically, when this method is overridden, the return value from a call to the super method is returned.</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="50dbc-1242">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="50dbc-1242">Method mouseUp</span></span>

<span data-ttu-id="50dbc-1243">ユーザーがマウスの左ボタンが押すときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1243">Identifies when a user presses the left mouse button.</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="50dbc-1244">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="50dbc-1244">Parameters - mouseUp</span></span>

<span data-ttu-id="50dbc-1245">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-1245">x</span></span>  
<span data-ttu-id="50dbc-1246">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1246">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1247">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-1247">y</span></span>  
<span data-ttu-id="50dbc-1248">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1248">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1249">ボタン</span><span class="sxs-lookup"><span data-stu-id="50dbc-1249">button</span></span>  
<span data-ttu-id="50dbc-1250">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1250">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1251">Ctrl</span><span class="sxs-lookup"><span data-stu-id="50dbc-1251">Ctrl</span></span>  
<span data-ttu-id="50dbc-1252">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1252">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1253">シフト</span><span class="sxs-lookup"><span data-stu-id="50dbc-1253">Shift</span></span>  
<span data-ttu-id="50dbc-1254">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1254">A Boolean value that indicates whether the SHIFT key is down.</span></span>

### <a name="return-value---mouseup"></a><span data-ttu-id="50dbc-1255">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="50dbc-1255">Return Value - mouseUp</span></span>

<span data-ttu-id="50dbc-1256">イベントが処理された場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1256">0 (zero) if the event has been handled.</span></span>

### <a name="remarks---mouseup"></a><span data-ttu-id="50dbc-1257">備考 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="50dbc-1257">Remarks - mouseUp</span></span>

<span data-ttu-id="50dbc-1258">フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[mouseUp] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1258">To override this method in a form list control, right-click the Methods node below the control, point to Override Method, and then click mouseUp.</span></span> <span data-ttu-id="50dbc-1259">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1259">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-moveitem"></a><span data-ttu-id="50dbc-1260">メソッド moveItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1260">Method moveItem</span></span>

<span data-ttu-id="50dbc-1261">指定した項目をフォーム リスト コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1261">Moves a specified item in a form list control.</span></span>

```xpp
public int moveItem(int Item, int InsertAt)
```

### <a name="parameters---moveitem"></a><span data-ttu-id="50dbc-1262">パラメーター - moveItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1262">Parameters - moveItem</span></span>

<span data-ttu-id="50dbc-1263">項目</span><span class="sxs-lookup"><span data-stu-id="50dbc-1263">Item</span></span>  
<span data-ttu-id="50dbc-1264">品目が移動されるリスト内の位置を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1264">An Integer data type that specifies the position in the list that the item is moved to.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1265">InsertAt</span><span class="sxs-lookup"><span data-stu-id="50dbc-1265">InsertAt</span></span>  
<span data-ttu-id="50dbc-1266">品目が移動されるリスト内の位置を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1266">An Integer data type that specifies the position in the list that the item is moved to.</span></span>

### <a name="return-value---moveitem"></a><span data-ttu-id="50dbc-1267">戻り値 - moveItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1267">Return Value - moveItem</span></span>

<span data-ttu-id="50dbc-1268">品目が移動されるリスト内の位置を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1268">An Integer data type that specifies the position in the list that the item is moved to.</span></span>

### <a name="examples---moveitem"></a><span data-ttu-id="50dbc-1269">例 - moveItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1269">Examples - moveItem</span></span>

<span data-ttu-id="50dbc-1270">次の例は、フォーム リスト コントロールの 10 番目の位置にアイテムを移動する moveItem メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1270">The following example shows a call to the moveItem method to move an item to the tenth position in the form list control.</span></span> <span data-ttu-id="50dbc-1271">FormListControl.getCount メソッドは、コントロール内の項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1271">The FormListControl.getCount method returns the number of items in the control.</span></span> <span data-ttu-id="50dbc-1272">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1272">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-1273">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1273">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(77); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = new FormRun(Args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add columns to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Account Numbers",1,120)); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
            "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    formListControl.getCount(); 
    formListControl.moveItem(2,10); 
}
```

## <a name="method-name"></a><span data-ttu-id="50dbc-1274">メソッド名</span><span class="sxs-lookup"><span data-stu-id="50dbc-1274">Method name</span></span>

<span data-ttu-id="50dbc-1275">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1275">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="50dbc-1276">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="50dbc-1276">Parameters - name</span></span>

<span data-ttu-id="50dbc-1277">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1277">value</span></span>  
<span data-ttu-id="50dbc-1278">コントロールに割り当てる名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1278">The name to assign to the control; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="50dbc-1279">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="50dbc-1279">Return Value - name</span></span>

<span data-ttu-id="50dbc-1280">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1280">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="50dbc-1281">備考 - name</span><span class="sxs-lookup"><span data-stu-id="50dbc-1281">Remarks - name</span></span>

<span data-ttu-id="50dbc-1282">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1282">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="50dbc-1283">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1283">It must start with a letter.</span></span>
-   <span data-ttu-id="50dbc-1284">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1284">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="50dbc-1285">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1285">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="50dbc-1286">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1286">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="50dbc-1287">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1287">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="50dbc-1288">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="50dbc-1288">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="50dbc-1289">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="50dbc-1289">Parameters - neededPermission</span></span>

<span data-ttu-id="50dbc-1290">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1290">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="50dbc-1291">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="50dbc-1291">Return Value - neededPermission</span></span>

## <a name="method-oneclickactivate"></a><span data-ttu-id="50dbc-1292">メソッド oneClickActivate</span><span class="sxs-lookup"><span data-stu-id="50dbc-1292">Method oneClickActivate</span></span>

```xpp
public boolean oneClickActivate([boolean value])
```

### <a name="parameters---oneclickactivate"></a><span data-ttu-id="50dbc-1293">パラメーター - oneClickActivate</span><span class="sxs-lookup"><span data-stu-id="50dbc-1293">Parameters - oneClickActivate</span></span>

<span data-ttu-id="50dbc-1294">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1294">value</span></span>  

### <a name="return-value---oneclickactivate"></a><span data-ttu-id="50dbc-1295">戻り値 - oneClickActivate</span><span class="sxs-lookup"><span data-stu-id="50dbc-1295">Return Value - oneClickActivate</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="50dbc-1296">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="50dbc-1296">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="50dbc-1297">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="50dbc-1297">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="50dbc-1298">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="50dbc-1298">Method parentControl</span></span>

<span data-ttu-id="50dbc-1299">コントロールの親コントロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1299">Retrieves the parent control for the control.</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="50dbc-1300">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="50dbc-1300">Return Value - parentControl</span></span>

<span data-ttu-id="50dbc-1301">コントロールの親コントロール。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1301">The parent control for the control.</span></span>

## <a name="method-redrawitems"></a><span data-ttu-id="50dbc-1302">メソッド redrawItems</span><span class="sxs-lookup"><span data-stu-id="50dbc-1302">Method redrawItems</span></span>

<span data-ttu-id="50dbc-1303">フォーム リスト コントロール内の広範囲の項目を更新します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1303">Updates a range of items in a form list control.</span></span>

```xpp
public boolean redrawItems(int idxFirst, int idxLast)
```

### <a name="parameters---redrawitems"></a><span data-ttu-id="50dbc-1304">パラメーター - redrawItems</span><span class="sxs-lookup"><span data-stu-id="50dbc-1304">Parameters - redrawItems</span></span>

<span data-ttu-id="50dbc-1305">idxFirst</span><span class="sxs-lookup"><span data-stu-id="50dbc-1305">idxFirst</span></span>  
<span data-ttu-id="50dbc-1306">範囲内の最後の項目のゼロベースのインデックスを指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1306">An Integer data type that specifies the zero-based index for the last item in the range.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1307">idxLast</span><span class="sxs-lookup"><span data-stu-id="50dbc-1307">idxLast</span></span>  
<span data-ttu-id="50dbc-1308">範囲内の最後の項目のゼロベースのインデックスを指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1308">An Integer data type that specifies the zero-based index for the last item in the range.</span></span>

### <a name="return-value---redrawitems"></a><span data-ttu-id="50dbc-1309">戻り値 - redrawItems</span><span class="sxs-lookup"><span data-stu-id="50dbc-1309">Return Value - redrawItems</span></span>

<span data-ttu-id="50dbc-1310">項目が更新された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1310">true if the items are updated; otherwise, false.</span></span>

### <a name="examples---redrawitems"></a><span data-ttu-id="50dbc-1311">例 - redrawItems</span><span class="sxs-lookup"><span data-stu-id="50dbc-1311">Examples - redrawItems</span></span>

<span data-ttu-id="50dbc-1312">次の例は、フォーム リスト コントロール内の項目の範囲を更新する redrawItems メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1312">The following example shows a call to the redrawItems method to update a range of items in the form list control.</span></span> <span data-ttu-id="50dbc-1313">FormListControl.moveItem メソッドは、指定された項目を移動します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1313">The FormListControl.moveItem method moves a specified item.</span></span> <span data-ttu-id="50dbc-1314">FormListControl.getCount メソッドは、コントロール内の項目の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1314">The FormListControl.getCount method retrieves the number of items in the control.</span></span> <span data-ttu-id="50dbc-1315">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1315">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-1316">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1316">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    str string; 
    container conAccountNum; 
    DictTable dictTable; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(77); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = new FormRun(Args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add columns to form list control. 
    formListControl.addColumn(1, new FormListColumn("Account Numbers",1,120)); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= "4000" 
            && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
    formListControl.getCount(); 
    formListControl.moveItem(2,10); 
    formListControl.redrawItems(0,20); 
}
```

## <a name="method-rowselect"></a><span data-ttu-id="50dbc-1317">メソッド rowSelect</span><span class="sxs-lookup"><span data-stu-id="50dbc-1317">Method rowSelect</span></span>

<span data-ttu-id="50dbc-1318">行をクリックしたときにフォーム リスト コントロールの行が選択されているかどうかを示すブール値データ型値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1318">Sets or gets a Boolean data type value that indicates whether a row in a form list control is selected when the row is clicked.</span></span>

```xpp
public boolean rowSelect([boolean value])
```

### <a name="parameters---rowselect"></a><span data-ttu-id="50dbc-1319">パラメーター - rowSelect</span><span class="sxs-lookup"><span data-stu-id="50dbc-1319">Parameters - rowSelect</span></span>

<span data-ttu-id="50dbc-1320">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1320">value</span></span>  
<span data-ttu-id="50dbc-1321">行をクリックしたときにフォーム リスト コントロールの行が選択されているかどうかを示すブール値データ型。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1321">A Boolean data type that indicates whether a row in a form list control is selected when the row is clicked.</span></span>

### <a name="return-value---rowselect"></a><span data-ttu-id="50dbc-1322">戻り値 - rowSelect</span><span class="sxs-lookup"><span data-stu-id="50dbc-1322">Return Value - rowSelect</span></span>

<span data-ttu-id="50dbc-1323">フォーム リスト コントロール内の行が選択されている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1323">true if the row in a form list control is selected; otherwise, false.</span></span>

### <a name="examples---rowselect"></a><span data-ttu-id="50dbc-1324">例 - rowSelect</span><span class="sxs-lookup"><span data-stu-id="50dbc-1324">Examples - rowSelect</span></span>

<span data-ttu-id="50dbc-1325">次の例は、行がクリックされたときにフォーム リスト コントロール内の行が選択されるように指定する、rowSelect メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1325">The following example shows a call to the rowSelect method to specify that a row in the form list control is selected when the row is clicked.</span></span> <span data-ttu-id="50dbc-1326">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1326">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-1327">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1327">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span> <span data-ttu-id="50dbc-1328">列は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1328">The columns are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn1; 
    FormListColumn formListColumn2; 
    FormListColumn formListColumn; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    formListControl.rowSelect(true); 
    // Add columns to the form list control. 
    formListControl.addColumn(1, new FormListColumn("Column1",1,120)); 
    formListControl.addColumn(2, new FormListColumn("Column2",2,120)); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    }}
```

## <a name="method-scroll"></a><span data-ttu-id="50dbc-1329">メソッド scroll</span><span class="sxs-lookup"><span data-stu-id="50dbc-1329">Method scroll</span></span>

```xpp
public boolean scroll(int dx, int dy)
```

### <a name="parameters---scroll"></a><span data-ttu-id="50dbc-1330">パラメーター - scroll</span><span class="sxs-lookup"><span data-stu-id="50dbc-1330">Parameters - scroll</span></span>

<span data-ttu-id="50dbc-1331">dx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1331">dx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1332">dy</span><span class="sxs-lookup"><span data-stu-id="50dbc-1332">dy</span></span>  

### <a name="return-value---scroll"></a><span data-ttu-id="50dbc-1333">戻り値 - scroll</span><span class="sxs-lookup"><span data-stu-id="50dbc-1333">Return Value - scroll</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="50dbc-1334">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="50dbc-1334">Method securityKey</span></span>

<span data-ttu-id="50dbc-1335">コントロールのセキュリティ キーの ID を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1335">Sets or returns the ID of the security key for the control.</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="50dbc-1336">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="50dbc-1336">Parameters - securityKey</span></span>

<span data-ttu-id="50dbc-1337">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1337">value</span></span>  
<span data-ttu-id="50dbc-1338">コントロールに割り当てるセキュリティ キーの ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1338">The ID of the security key to assign to the control; optional.</span></span>

### <a name="return-value---securitykey"></a><span data-ttu-id="50dbc-1339">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="50dbc-1339">Return Value - securityKey</span></span>

<span data-ttu-id="50dbc-1340">コントロールのセキュリティ キーの ID。コントロールにセキュリティ キーが割り当てられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1340">The ID of the security key for the control; 0 (zero) if no security key is assigned to the control.</span></span>

## <a name="method-selectionchanging"></a><span data-ttu-id="50dbc-1341">メソッド selectionChanging</span><span class="sxs-lookup"><span data-stu-id="50dbc-1341">Method selectionChanging</span></span>

```xpp
public boolean selectionChanging(int Idx, AnyType Data)
```

### <a name="parameters---selectionchanging"></a><span data-ttu-id="50dbc-1342">パラメーター - selectionChanging</span><span class="sxs-lookup"><span data-stu-id="50dbc-1342">Parameters - selectionChanging</span></span>

<span data-ttu-id="50dbc-1343">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1343">Idx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1344">データ</span><span class="sxs-lookup"><span data-stu-id="50dbc-1344">Data</span></span>  

### <a name="return-value---selectionchanging"></a><span data-ttu-id="50dbc-1345">戻り値 - selectionChanging</span><span class="sxs-lookup"><span data-stu-id="50dbc-1345">Return Value - selectionChanging</span></span>

## <a name="method-setcolumn"></a><span data-ttu-id="50dbc-1346">メソッド setColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-1346">Method setColumn</span></span>

```xpp
public boolean setColumn(int Idx, FormListColumn Column)
```

### <a name="parameters---setcolumn"></a><span data-ttu-id="50dbc-1347">パラメーター - setColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-1347">Parameters - setColumn</span></span>

<span data-ttu-id="50dbc-1348">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1348">Idx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1349">円柱</span><span class="sxs-lookup"><span data-stu-id="50dbc-1349">Column</span></span>  

### <a name="return-value---setcolumn"></a><span data-ttu-id="50dbc-1350">戻り値 - setColumn</span><span class="sxs-lookup"><span data-stu-id="50dbc-1350">Return Value - setColumn</span></span>

## <a name="method-setcolumnwidth"></a><span data-ttu-id="50dbc-1351">メソッド setColumnWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-1351">Method setColumnWidth</span></span>

<span data-ttu-id="50dbc-1352">フォーム リスト コントロール内の列の幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1352">Specifies the width of a column in a form list control.</span></span>

```xpp
public boolean setColumnWidth(int Idx, int Width)
```

### <a name="parameters---setcolumnwidth"></a><span data-ttu-id="50dbc-1353">パラメーター - setColumnWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-1353">Parameters - setColumnWidth</span></span>

<span data-ttu-id="50dbc-1354">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1354">Idx</span></span>  
<span data-ttu-id="50dbc-1355">フォーム リスト コントロール内で列の幅を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1355">An Integer data type that specifies the width of the column in a form list control.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1356">幅</span><span class="sxs-lookup"><span data-stu-id="50dbc-1356">Width</span></span>  
<span data-ttu-id="50dbc-1357">フォーム リスト コントロール内で列の幅を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1357">An Integer data type that specifies the width of the column in a form list control.</span></span>

### <a name="return-value---setcolumnwidth"></a><span data-ttu-id="50dbc-1358">戻り値 - setColumnWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-1358">Return Value - setColumnWidth</span></span>

<span data-ttu-id="50dbc-1359">幅がセットされている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1359">true if the width is set; otherwise, false.</span></span>

### <a name="remarks---setcolumnwidth"></a><span data-ttu-id="50dbc-1360">備考 - setColumnWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-1360">Remarks - setColumnWidth</span></span>

<span data-ttu-id="50dbc-1361">フォーム リスト コントロールに列を表示するには、FormListControl.viewType メソッドを呼び出して、FormListViewType::Report 列挙値を渡します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1361">To display columns in a form list control, call the FormListControl.viewType method, and then pass the FormListViewType::Report enumeration value.</span></span>

### <a name="examples---setcolumnwidth"></a><span data-ttu-id="50dbc-1362">例 - setColumnWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-1362">Examples - setColumnWidth</span></span>

<span data-ttu-id="50dbc-1363">次の例は、フォーム リスト コントロール内の列の幅を指定する setColumnWidth メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1363">The following example shows a call to the setColumnWidth method to specify the width of the column in the form list control.</span></span> <span data-ttu-id="50dbc-1364">FormListControl.addColumn メソッドは、列をフォーム リスト コントロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1364">The FormListControl.addColumn method adds the column to the form list control.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::Report); 
    formListControl.height(120); 
    formListControl.widthMode(FormWidth::ColumnWidth); 
    // Add a column to the form list control, and then set the column width. 
    formListControl.addColumn(1, new FormListColumn("Column1")); 
    formListControl.setColumnWidth(0,100); 
}
```

## <a name="method-setitem"></a><span data-ttu-id="50dbc-1365">メソッド setItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1365">Method setItem</span></span>

<span data-ttu-id="50dbc-1366">フォーム リスト コントロールに項目が含まれているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1366">Indicates whether an item is contained in a form list control.</span></span>

```xpp
public boolean setItem(FormListItem item)
```

### <a name="parameters---setitem"></a><span data-ttu-id="50dbc-1367">パラメーター - setItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1367">Parameters - setItem</span></span>

<span data-ttu-id="50dbc-1368">品目</span><span class="sxs-lookup"><span data-stu-id="50dbc-1368">item</span></span>  
<span data-ttu-id="50dbc-1369">フォーム リスト コントロール内の項目の FormListItem オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1369">A FormListItem object for an item in a form list control.</span></span>

### <a name="return-value---setitem"></a><span data-ttu-id="50dbc-1370">戻り値 - setItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1370">Return Value - setItem</span></span>

<span data-ttu-id="50dbc-1371">フォーム リスト コントロールに項目が含まれている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1371">true if an item is contained in a form list control; otherwise, false.</span></span>

### <a name="examples---setitem"></a><span data-ttu-id="50dbc-1372">例 - setItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1372">Examples - setItem</span></span>

<span data-ttu-id="50dbc-1373">次の例は、各項目がフォーム リスト コントロールに含まれているかどうかを判断する setItem メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1373">The following example shows a call to the setItem method to determine whether each item is contained in the form list control.</span></span> <span data-ttu-id="50dbc-1374">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1374">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-1375">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1375">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    boolean itemSet; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
            "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
        itemSet = formListControl.setItem(formListItem); 
    } 
}
```

## <a name="method-setstateimagelist"></a><span data-ttu-id="50dbc-1376">メソッド setStateImagelist</span><span class="sxs-lookup"><span data-stu-id="50dbc-1376">Method setStateImagelist</span></span>

```xpp
public Imagelist setStateImagelist(Imagelist imageList)
```

### <a name="parameters---setstateimagelist"></a><span data-ttu-id="50dbc-1377">パラメーター - setStateImagelist</span><span class="sxs-lookup"><span data-stu-id="50dbc-1377">Parameters - setStateImagelist</span></span>

<span data-ttu-id="50dbc-1378">imageList</span><span class="sxs-lookup"><span data-stu-id="50dbc-1378">imageList</span></span>  

### <a name="return-value---setstateimagelist"></a><span data-ttu-id="50dbc-1379">戻り値 - setStateImagelist</span><span class="sxs-lookup"><span data-stu-id="50dbc-1379">Return Value - setStateImagelist</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="50dbc-1380">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="50dbc-1380">Method showContextMenu</span></span>

<span data-ttu-id="50dbc-1381">ショートカット メニューがいつ表示されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1381">Identifies when a shortcut menu appears.</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="50dbc-1382">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="50dbc-1382">Parameters - showContextMenu</span></span>

<span data-ttu-id="50dbc-1383">menuHandle</span><span class="sxs-lookup"><span data-stu-id="50dbc-1383">menuHandle</span></span>  
<span data-ttu-id="50dbc-1384">メニュー ハンドルを指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1384">An Integer data type that specifies the menu handle.</span></span>

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="50dbc-1385">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="50dbc-1385">Return Value - showContextMenu</span></span>

<span data-ttu-id="50dbc-1386">メニュー ハンドルを指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1386">An Integer data type that specifies the menu handle.</span></span>

### <a name="remarks---showcontextmenu"></a><span data-ttu-id="50dbc-1387">備考 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="50dbc-1387">Remarks - showContextMenu</span></span>

<span data-ttu-id="50dbc-1388">リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [showContextMenu] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1388">To override this method on a list view control, right-click the Methods node below the control, point to Override Method, and then click showContextMenu.</span></span> <span data-ttu-id="50dbc-1389">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1389">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-showselalways"></a><span data-ttu-id="50dbc-1390">メソッド showSelAlways</span><span class="sxs-lookup"><span data-stu-id="50dbc-1390">Method showSelAlways</span></span>

```xpp
public boolean showSelAlways([boolean value])
```

### <a name="parameters---showselalways"></a><span data-ttu-id="50dbc-1391">パラメーター - showSelAlways</span><span class="sxs-lookup"><span data-stu-id="50dbc-1391">Parameters - showSelAlways</span></span>

<span data-ttu-id="50dbc-1392">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1392">value</span></span>  

### <a name="return-value---showselalways"></a><span data-ttu-id="50dbc-1393">戻り値 - showSelAlways</span><span class="sxs-lookup"><span data-stu-id="50dbc-1393">Return Value - showSelAlways</span></span>

## <a name="method-singleselection"></a><span data-ttu-id="50dbc-1394">メソッド singleSelection</span><span class="sxs-lookup"><span data-stu-id="50dbc-1394">Method singleSelection</span></span>

<span data-ttu-id="50dbc-1395">フォーム リスト コントロールで複数の項目を選択できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1395">Indicates whether multiple items can be selected in a form list control.</span></span>

```xpp
public boolean singleSelection([boolean value])
```

### <a name="parameters---singleselection"></a><span data-ttu-id="50dbc-1396">パラメーター - singleSelection</span><span class="sxs-lookup"><span data-stu-id="50dbc-1396">Parameters - singleSelection</span></span>

<span data-ttu-id="50dbc-1397">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1397">value</span></span>  
<span data-ttu-id="50dbc-1398">フォーム リスト コントロールで複数の項目を選択できるかどうかを示すブール値データ型。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1398">A Boolean data type that indicates whether multiple items can be selected in a form list control.</span></span>

### <a name="return-value---singleselection"></a><span data-ttu-id="50dbc-1399">戻り値 - singleSelection</span><span class="sxs-lookup"><span data-stu-id="50dbc-1399">Return Value - singleSelection</span></span>

<span data-ttu-id="50dbc-1400">複数の項目を選択することができない場合 true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1400">true if multiple items cannot be selected; otherwise, false.</span></span>

### <a name="remarks---singleselection"></a><span data-ttu-id="50dbc-1401">備考 - singleSelection</span><span class="sxs-lookup"><span data-stu-id="50dbc-1401">Remarks - singleSelection</span></span>

<span data-ttu-id="50dbc-1402">フォームのリスト コントロールにアイテムを追加する前に、singleSelection メソッドを呼び出します。 それ以外の場合は、項目はコントロールに表示されません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1402">Call the singleSelection method before you add items to a form list control; otherwise, the items do not appear in the control.</span></span>

### <a name="examples---singleselection"></a><span data-ttu-id="50dbc-1403">例 - singleSelection</span><span class="sxs-lookup"><span data-stu-id="50dbc-1403">Examples - singleSelection</span></span>

<span data-ttu-id="50dbc-1404">次の例は、複数の項目を選択できるように指定するための singleSelection メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1404">The following example shows a call to the singleSelection method to specify that multiple items can be selected.</span></span> <span data-ttu-id="50dbc-1405">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1405">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-1406">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1406">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void testFormListControl(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    FormListColumn formListColumn1; 
    FormListColumn formListColumn2; 
    FormListColumn formListColumn; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    int numItems; 
    boolean columnAdd; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.viewType(FormListViewType::List); 
    formListControl.height(120); 
    formListControl.singleSelection(false); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
            "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
    } 
}
```

## <a name="method-skip"></a><span data-ttu-id="50dbc-1407">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="50dbc-1407">Method skip</span></span>

<span data-ttu-id="50dbc-1408">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1408">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="50dbc-1409">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="50dbc-1409">Parameters - skip</span></span>

<span data-ttu-id="50dbc-1410">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1410">value</span></span>  
<span data-ttu-id="50dbc-1411">コントロールのスキップ プロパティに割り当てるブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1411">A Boolean value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="50dbc-1412">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="50dbc-1412">Return Value - skip</span></span>

<span data-ttu-id="50dbc-1413">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1413">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-sort"></a><span data-ttu-id="50dbc-1414">メソッド sort</span><span class="sxs-lookup"><span data-stu-id="50dbc-1414">Method sort</span></span>

```xpp
public int sort([int value])
```

### <a name="parameters---sort"></a><span data-ttu-id="50dbc-1415">パラメーター - sort</span><span class="sxs-lookup"><span data-stu-id="50dbc-1415">Parameters - sort</span></span>

<span data-ttu-id="50dbc-1416">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1416">value</span></span>  

### <a name="return-value---sort"></a><span data-ttu-id="50dbc-1417">戻り値 - sort</span><span class="sxs-lookup"><span data-stu-id="50dbc-1417">Return Value - sort</span></span>

## <a name="method-sorttextitems"></a><span data-ttu-id="50dbc-1418">メソッド sortTextItems</span><span class="sxs-lookup"><span data-stu-id="50dbc-1418">Method sortTextItems</span></span>

```xpp
public boolean sortTextItems([int column], [boolean ascending])
```

### <a name="parameters---sorttextitems"></a><span data-ttu-id="50dbc-1419">パラメーター - sortTextItems</span><span class="sxs-lookup"><span data-stu-id="50dbc-1419">Parameters - sortTextItems</span></span>

<span data-ttu-id="50dbc-1420">column</span><span class="sxs-lookup"><span data-stu-id="50dbc-1420">column</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1421">ascending</span><span class="sxs-lookup"><span data-stu-id="50dbc-1421">ascending</span></span>  

### <a name="return-value---sorttextitems"></a><span data-ttu-id="50dbc-1422">戻り値 - sortTextItems</span><span class="sxs-lookup"><span data-stu-id="50dbc-1422">Return Value - sortTextItems</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="50dbc-1423">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="50dbc-1423">Method toolTip</span></span>

<span data-ttu-id="50dbc-1424">コントロールのツール ヒント テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1424">Retrieves the tooltip text for the control.</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="50dbc-1425">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="50dbc-1425">Return Value - toolTip</span></span>

<span data-ttu-id="50dbc-1426">コントロールのツールヒント テキスト。コントロールにツールヒント テキストが定義されていない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1426">The tooltip text for the control; an empty string if no tooltip text has been defined for the control.</span></span>

### <a name="remarks---tooltip"></a><span data-ttu-id="50dbc-1427">備考 - toolTip</span><span class="sxs-lookup"><span data-stu-id="50dbc-1427">Remarks - toolTip</span></span>

<span data-ttu-id="50dbc-1428">メソッドを上書きして、toolTip メソッドに値を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1428">The method might be overridden to provide a value to the toolTip method.</span></span>

## <a name="method-top"></a><span data-ttu-id="50dbc-1429">メソッド top</span><span class="sxs-lookup"><span data-stu-id="50dbc-1429">Method top</span></span>

<span data-ttu-id="50dbc-1430">フォーム リスト コントロールの垂直位置をピクセル単位で設定するか返し、位置を計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1430">Sets or returns the vertical position of a form list control in pixels, and specifies how the position is calculated.</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="50dbc-1431">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="50dbc-1431">Parameters - top</span></span>

<span data-ttu-id="50dbc-1432">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1432">value</span></span>  
<span data-ttu-id="50dbc-1433">垂直位置の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1433">An integer that indicates how the vertical position is calculated; optional.</span></span> <span data-ttu-id="50dbc-1434">このパラメーターは、次のいずれかの値にすることができます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1434">This parameter can be one of the following values:</span></span>

<!-- -->

<span data-ttu-id="50dbc-1435">モード</span><span class="sxs-lookup"><span data-stu-id="50dbc-1435">mode</span></span>  
<span data-ttu-id="50dbc-1436">垂直位置の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1436">An integer that indicates how the vertical position is calculated; optional.</span></span> <span data-ttu-id="50dbc-1437">このパラメーターは、次のいずれかの値にすることができます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1437">This parameter can be one of the following values:</span></span>

### <a name="return-value---top"></a><span data-ttu-id="50dbc-1438">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="50dbc-1438">Return Value - top</span></span>

<span data-ttu-id="50dbc-1439">フォーム リスト コントロールの垂直位置をピクセル単位で示す整数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1439">An integer that indicates the vertical position of a form list control in pixels.</span></span>

### <a name="examples---top"></a><span data-ttu-id="50dbc-1440">例 - top</span><span class="sxs-lookup"><span data-stu-id="50dbc-1440">Examples - top</span></span>

<span data-ttu-id="50dbc-1441">次の例は、垂直位置を 50 ピクセルに設定する top メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1441">The following example shows a call to the top method to set the vertical position to 50 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.top(50,-1); 
}
```

## <a name="method-topmode"></a><span data-ttu-id="50dbc-1442">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1442">Method topMode</span></span>

<span data-ttu-id="50dbc-1443">フォーム リスト コントロールの垂直位置を計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1443">Sets or returns a value that indicates how the vertical position for a form list control is calculated.</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="50dbc-1444">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1444">Parameters - topMode</span></span>

<span data-ttu-id="50dbc-1445">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1445">value</span></span>  
<span data-ttu-id="50dbc-1446">垂直位置の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1446">An integer that indicates how the vertical position is calculated; optional.</span></span>

### <a name="return-value---topmode"></a><span data-ttu-id="50dbc-1447">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1447">Return Value - topMode</span></span>

<span data-ttu-id="50dbc-1448">垂直位置の計算方法を示す整数データ型値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1448">An Integer data type value that indicates how the vertical position is calculated.</span></span> <span data-ttu-id="50dbc-1449">戻り値は、-1 または FormTop 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1449">The return value can be -1 or a FormTop enumeration value.</span></span>

### <a name="remarks---topmode"></a><span data-ttu-id="50dbc-1450">備考 - topMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1450">Remarks - topMode</span></span>

<span data-ttu-id="50dbc-1451">value パラメーターと戻り値は、正確なピクセル値の場合は -1、FormTop 列挙値または -1 のいずれかの整数値です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1451">The value parameter and return value are integer values that can be either -1 for an exact pixel value or a FormTop enumeration value.</span></span> <span data-ttu-id="50dbc-1452">詳細については、「FormTop 列挙」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1452">For more information, see FormTop Enumeration.</span></span>

### <a name="examples---topmode"></a><span data-ttu-id="50dbc-1453">例 - topMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1453">Examples - topMode</span></span>

<span data-ttu-id="50dbc-1454">次の例は、正確なピクセル値に基づいて垂直位置を計算する topMode メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1454">The following example shows a call to the topMode method that calculates the vertical position based on an exact pixel value.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.topMode(-1); 
    formListControl.topValue(50); 
}
```

## <a name="method-topvalue"></a><span data-ttu-id="50dbc-1455">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1455">Method topValue</span></span>

<span data-ttu-id="50dbc-1456">フォーム リスト コントロールの垂直位置をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1456">Sets or returns the vertical position of a form list control in pixels.</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="50dbc-1457">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1457">Parameters - topValue</span></span>

<span data-ttu-id="50dbc-1458">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1458">value</span></span>  
<span data-ttu-id="50dbc-1459">垂直位置を指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1459">An integer that specifies the vertical position; optional.</span></span>

### <a name="return-value---topvalue"></a><span data-ttu-id="50dbc-1460">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1460">Return Value - topValue</span></span>

<span data-ttu-id="50dbc-1461">フォーム リスト コントロールの垂直位置を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1461">An integer that specifies the vertical position of a form list control.</span></span>

### <a name="remarks---topvalue"></a><span data-ttu-id="50dbc-1462">備考 - topValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1462">Remarks - topValue</span></span>

<span data-ttu-id="50dbc-1463">正確なピクセル値に上部モードが設定されていない限り、垂直位置は変更されません。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1463">The vertical position is not changed unless the top mode is set for an exact pixel value.</span></span> <span data-ttu-id="50dbc-1464">詳細については、「topMode」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1464">For more information, see topMode.</span></span>

### <a name="examples---topvalue"></a><span data-ttu-id="50dbc-1465">例 - topValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1465">Examples - topValue</span></span>

<span data-ttu-id="50dbc-1466">次の例は、垂直位置を 50 ピクセルに設定する topValue メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1466">The following example shows a call to the topValue method that sets the vertical position to 50 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.topMode(-1); 
    formListControl.topValue(50); 
}
```

## <a name="method-trackselect"></a><span data-ttu-id="50dbc-1467">メソッド trackSelect</span><span class="sxs-lookup"><span data-stu-id="50dbc-1467">Method trackSelect</span></span>

```xpp
public boolean trackSelect([boolean value])
```

### <a name="parameters---trackselect"></a><span data-ttu-id="50dbc-1468">パラメーター - trackSelect</span><span class="sxs-lookup"><span data-stu-id="50dbc-1468">Parameters - trackSelect</span></span>

<span data-ttu-id="50dbc-1469">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1469">value</span></span>  

### <a name="return-value---trackselect"></a><span data-ttu-id="50dbc-1470">戻り値 - trackSelect</span><span class="sxs-lookup"><span data-stu-id="50dbc-1470">Return Value - trackSelect</span></span>

## <a name="method-twoclickactivate"></a><span data-ttu-id="50dbc-1471">メソッド twoClickActivate</span><span class="sxs-lookup"><span data-stu-id="50dbc-1471">Method twoClickActivate</span></span>

```xpp
public boolean twoClickActivate([boolean value])
```

### <a name="parameters---twoclickactivate"></a><span data-ttu-id="50dbc-1472">パラメーター - twoClickActivate</span><span class="sxs-lookup"><span data-stu-id="50dbc-1472">Parameters - twoClickActivate</span></span>

<span data-ttu-id="50dbc-1473">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1473">value</span></span>  

### <a name="return-value---twoclickactivate"></a><span data-ttu-id="50dbc-1474">戻り値 - twoClickActivate</span><span class="sxs-lookup"><span data-stu-id="50dbc-1474">Return Value - twoClickActivate</span></span>

## <a name="method-type"></a><span data-ttu-id="50dbc-1475">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="50dbc-1475">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="50dbc-1476">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="50dbc-1476">Parameters - type</span></span>

<span data-ttu-id="50dbc-1477">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1477">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="50dbc-1478">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="50dbc-1478">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="50dbc-1479">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="50dbc-1479">Method underline</span></span>

<span data-ttu-id="50dbc-1480">コントロール内のテキストの下線プロパティの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1480">Sets or returns the value of the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="50dbc-1481">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="50dbc-1481">Parameters - underline</span></span>

<span data-ttu-id="50dbc-1482">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1482">value</span></span>  
<span data-ttu-id="50dbc-1483">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1483">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="50dbc-1484">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="50dbc-1484">Return Value - underline</span></span>

<span data-ttu-id="50dbc-1485">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1485">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="50dbc-1486">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="50dbc-1486">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="50dbc-1487">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="50dbc-1487">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="50dbc-1488">データ</span><span class="sxs-lookup"><span data-stu-id="50dbc-1488">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="50dbc-1489">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="50dbc-1489">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="50dbc-1490">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="50dbc-1490">Method userData</span></span>

<span data-ttu-id="50dbc-1491">コントロールのユーザー データを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1491">Gets or sets the user data for the control.</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="50dbc-1492">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="50dbc-1492">Parameters - userData</span></span>

<span data-ttu-id="50dbc-1493">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1493">value</span></span>  
<span data-ttu-id="50dbc-1494">コントロールのユーザー データを示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1494">An integer value that indicates the user data for the control; optional.</span></span>

### <a name="return-value---userdata"></a><span data-ttu-id="50dbc-1495">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="50dbc-1495">Return Value - userData</span></span>

<span data-ttu-id="50dbc-1496">コントロールのユーザー データ。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1496">The user data for the control.</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="50dbc-1497">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1497">Method userDataItem</span></span>

<span data-ttu-id="50dbc-1498">コントロールのユーザー データ品目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1498">Gets or sets the user data item for the control.</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="50dbc-1499">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1499">Parameters - userDataItem</span></span>

<span data-ttu-id="50dbc-1500">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1500">value</span></span>  
<span data-ttu-id="50dbc-1501">コントロールのユーザー データ項目を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1501">An integer value that indicates the user data item for the control; optional.</span></span>

### <a name="return-value---userdataitem"></a><span data-ttu-id="50dbc-1502">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1502">Return Value - userDataItem</span></span>

<span data-ttu-id="50dbc-1503">コントロールのユーザー データ アイテム。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1503">The user data item for the control.</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="50dbc-1504">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="50dbc-1504">Method userDataItems</span></span>

<span data-ttu-id="50dbc-1505">コントロールのユーザー データ項目の数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1505">Gets or sets the number of user data items for the control.</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="50dbc-1506">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="50dbc-1506">Parameters - userDataItems</span></span>

<span data-ttu-id="50dbc-1507">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1507">value</span></span>  
<span data-ttu-id="50dbc-1508">コントロールのユーザー データ項目の数を示す整数値。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1508">An integer value that indicates the number of user data items for the control; optional.</span></span>

### <a name="return-value---userdataitems"></a><span data-ttu-id="50dbc-1509">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="50dbc-1509">Return Value - userDataItems</span></span>

<span data-ttu-id="50dbc-1510">コントロールのユーザー データ項目の数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1510">The number of user data items for the control.</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="50dbc-1511">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="50dbc-1511">Method userDisable</span></span>

<span data-ttu-id="50dbc-1512">ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1512">Gets or sets the value that indicates whether the control is disabled for the user.</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="50dbc-1513">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="50dbc-1513">Parameters - userDisable</span></span>

<span data-ttu-id="50dbc-1514">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1514">value</span></span>  
<span data-ttu-id="50dbc-1515">ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1515">The value that indicates whether the control is disabled for the user; optional.</span></span>

### <a name="return-value---userdisable"></a><span data-ttu-id="50dbc-1516">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="50dbc-1516">Return Value - userDisable</span></span>

<span data-ttu-id="50dbc-1517">ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1517">1 if the control is disabled for the user; otherwise, 0.</span></span>

## <a name="method-userheight"></a><span data-ttu-id="50dbc-1518">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="50dbc-1518">Method userHeight</span></span>

<span data-ttu-id="50dbc-1519">コントロールのカスタム ユーザーの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1519">Gets or sets the custom user height for the control.</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="50dbc-1520">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="50dbc-1520">Parameters - userHeight</span></span>

<span data-ttu-id="50dbc-1521">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1521">value</span></span>  
<span data-ttu-id="50dbc-1522">コントロールのユーザーの高さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1522">The user height for the control; optional.</span></span>

### <a name="return-value---userheight"></a><span data-ttu-id="50dbc-1523">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="50dbc-1523">Return Value - userHeight</span></span>

<span data-ttu-id="50dbc-1524">コントロールのカスタム ユーザーの高さ。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1524">The custom user height for the control.</span></span>

## <a name="method-userhide"></a><span data-ttu-id="50dbc-1525">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="50dbc-1525">Method userHide</span></span>

<span data-ttu-id="50dbc-1526">コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1526">Gets or sets the value that indicates whether the control is hidden from the user.</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="50dbc-1527">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="50dbc-1527">Parameters - userHide</span></span>

<span data-ttu-id="50dbc-1528">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1528">value</span></span>  
<span data-ttu-id="50dbc-1529">コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1529">The value that indicates whether the control is hidden from the user; optional.</span></span>

### <a name="return-value---userhide"></a><span data-ttu-id="50dbc-1530">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="50dbc-1530">Return Value - userHide</span></span>

<span data-ttu-id="50dbc-1531">コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1531">1 if the control is hidden from the user; otherwise, 0.</span></span>

### <a name="remarks---userhide"></a><span data-ttu-id="50dbc-1532">備考 - userHide</span><span class="sxs-lookup"><span data-stu-id="50dbc-1532">Remarks - userHide</span></span>

<span data-ttu-id="50dbc-1533">ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1533">The user specifies whether a control is hidden by right-clicking the control when it is viewable or by right-clicking another control when the original control is hidden.</span></span> <span data-ttu-id="50dbc-1534">右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1534">A right-click opens a menu that can be used to hide or display the control.</span></span> <span data-ttu-id="50dbc-1535">このメソッドを使用すると、プログラムによって値を決定して設定できます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1535">This method lets you programmatically determine and set the value.</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="50dbc-1536">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="50dbc-1536">Method userOrgContainer</span></span>

<span data-ttu-id="50dbc-1537">コントロールの組織コンテナを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1537">Gets or sets the organization container for the control.</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="50dbc-1538">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="50dbc-1538">Parameters - userOrgContainer</span></span>

<span data-ttu-id="50dbc-1539">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1539">value</span></span>  
<span data-ttu-id="50dbc-1540">コントロールに設定する組織コンテナー (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1540">The organization container to set for the control; optional.</span></span>

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="50dbc-1541">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="50dbc-1541">Return Value - userOrgContainer</span></span>

<span data-ttu-id="50dbc-1542">コントロールの組織コンテナー。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1542">The organization container for the control.</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="50dbc-1543">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="50dbc-1543">Method userOrgSibling</span></span>

<span data-ttu-id="50dbc-1544">コントロールの組織兄弟を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1544">Gets or sets the organization sibling for the control.</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="50dbc-1545">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="50dbc-1545">Parameters - userOrgSibling</span></span>

<span data-ttu-id="50dbc-1546">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1546">value</span></span>  
<span data-ttu-id="50dbc-1547">コントロールに設定する組織の兄弟 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1547">The organization sibling to set for the control; optional.</span></span>

### <a name="return-value---userorgsibling"></a><span data-ttu-id="50dbc-1548">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="50dbc-1548">Return Value - userOrgSibling</span></span>

<span data-ttu-id="50dbc-1549">コントロールの組織の兄弟。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1549">The organization sibling for the control.</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="50dbc-1550">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="50dbc-1550">Method userPromptText</span></span>

<span data-ttu-id="50dbc-1551">コントロールのユーザーラベル テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1551">Gets or sets the user label text for the control.</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="50dbc-1552">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="50dbc-1552">Parameters - userPromptText</span></span>

<span data-ttu-id="50dbc-1553">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1553">value</span></span>  
<span data-ttu-id="50dbc-1554">コントロールに設定するユーザー ラベルのテキスト (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1554">The user label text to set for the control; optional.</span></span>

### <a name="return-value---userprompttext"></a><span data-ttu-id="50dbc-1555">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="50dbc-1555">Return Value - userPromptText</span></span>

<span data-ttu-id="50dbc-1556">コントロールのユーザーラベル テキスト。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1556">The user label text for the control.</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="50dbc-1557">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="50dbc-1557">Method userSecurityLevel</span></span>

<span data-ttu-id="50dbc-1558">コントロールのユーザー セキュリティ レベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1558">Gets or sets the user security level for the control.</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="50dbc-1559">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="50dbc-1559">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="50dbc-1560">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1560">value</span></span>  
<span data-ttu-id="50dbc-1561">コントロールに設定するユーザー セキュリティ レベル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1561">The user security level to set for the control; optional.</span></span>

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="50dbc-1562">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="50dbc-1562">Return Value - userSecurityLevel</span></span>

<span data-ttu-id="50dbc-1563">コントロールのユーザー セキュリティ レベル。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1563">The user security level for the control.</span></span>

## <a name="method-userskip"></a><span data-ttu-id="50dbc-1564">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="50dbc-1564">Method userSkip</span></span>

<span data-ttu-id="50dbc-1565">ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1565">Sets or returns the value that indicates whether the form control is skipped when the user presses the TAB key to navigate the controls in the form.</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="50dbc-1566">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="50dbc-1566">Parameters - userSkip</span></span>

<span data-ttu-id="50dbc-1567">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1567">value</span></span>  
<span data-ttu-id="50dbc-1568">userSkip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1568">The value to assign to the userSkip property; optional.</span></span> <span data-ttu-id="50dbc-1569">コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1569">The value is 1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

### <a name="return-value---userskip"></a><span data-ttu-id="50dbc-1570">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="50dbc-1570">Return Value - userSkip</span></span>

<span data-ttu-id="50dbc-1571">コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1571">1 if the user setting to skip the control is in effect; otherwise, 0.</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="50dbc-1572">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-1572">Method userWidth</span></span>

<span data-ttu-id="50dbc-1573">ユーザーによって指定されたコントロールの幅をピクセル単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1573">Sets or returns the width of the control in pixels, as specified by the user.</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="50dbc-1574">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-1574">Parameters - userWidth</span></span>

<span data-ttu-id="50dbc-1575">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1575">value</span></span>  
<span data-ttu-id="50dbc-1576">コントロールの幅として使用するピクセル数 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1576">The number of pixels to use as the width of the control; optional.</span></span>

### <a name="return-value---userwidth"></a><span data-ttu-id="50dbc-1577">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-1577">Return Value - userWidth</span></span>

<span data-ttu-id="50dbc-1578">ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1578">The number of pixels that the user specified as the width of the control; 0 (zero) if the user did not specify a character width.</span></span>

### <a name="remarks---userwidth"></a><span data-ttu-id="50dbc-1579">備考 - userWidth</span><span class="sxs-lookup"><span data-stu-id="50dbc-1579">Remarks - userWidth</span></span>

<span data-ttu-id="50dbc-1580">userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1580">The userWidth method returns the width in pixels, based on six times the number of characters.</span></span> <span data-ttu-id="50dbc-1581">たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1581">For example, if the user has specified 30 characters as the width of the control, the return value is 6 \* 30 = 180.</span></span> <span data-ttu-id="50dbc-1582">コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1582">To specify the width of the control in characters, users can right-click the control to open the setup form where the character specification is made.</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="50dbc-1583">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="50dbc-1583">Method verticalSpacing</span></span>

<span data-ttu-id="50dbc-1584">ピクセルでフォーム リスト コントロールの上と下のスペースの量を設定または取得し、スペースを計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1584">Sets or gets the amount of space above and below a form list control in pixels, and specifies how the space is calculated.</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="50dbc-1585">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="50dbc-1585">Parameters - verticalSpacing</span></span>

<span data-ttu-id="50dbc-1586">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1586">value</span></span>  
<span data-ttu-id="50dbc-1587">領域の計算方法を示す AutoMode システムの列挙値、オプションです。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1587">An AutoMode system enumeration value that indicates how the space is calculated; optional.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1588">モード</span><span class="sxs-lookup"><span data-stu-id="50dbc-1588">mode</span></span>  
<span data-ttu-id="50dbc-1589">領域の計算方法を示す AutoMode システムの列挙値、オプションです。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1589">An AutoMode system enumeration value that indicates how the space is calculated; optional.</span></span>

### <a name="return-value---verticalspacing"></a><span data-ttu-id="50dbc-1590">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="50dbc-1590">Return Value - verticalSpacing</span></span>

<span data-ttu-id="50dbc-1591">コントロールの上と下のスペースの量を示す整数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1591">An integer that indicates the amount of space above and below a control.</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="50dbc-1592">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1592">Method verticalSpacingMode</span></span>

<span data-ttu-id="50dbc-1593">フォーム リスト コントロールの上と下のスペースを計算する方法を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1593">Sets or returns a value that indicates how the space above and below a form list control is calculated.</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="50dbc-1594">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1594">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="50dbc-1595">モード</span><span class="sxs-lookup"><span data-stu-id="50dbc-1595">mode</span></span>  
<span data-ttu-id="50dbc-1596">領域の計算方法を示す AutoMode システムの列挙値、オプションです。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1596">An AutoMode system enumeration value that indicates how the space is calculated; optional.</span></span>

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="50dbc-1597">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1597">Return Value - verticalSpacingMode</span></span>

<span data-ttu-id="50dbc-1598">スペースがフォント サイズなどの他のフォーム設定に基づいて自動的に調整される場合は自動です。そうでなければ、固定です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1598">Auto if the space is automatically adjusted based on other form settings, such as the font size; otherwise, Fixed.</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="50dbc-1599">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1599">Method verticalSpacingValue</span></span>

<span data-ttu-id="50dbc-1600">ピクセルでフォーム リスト コントロールの上と下のスペースの量を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1600">Sets or returns the amount of space above and below a form list control in pixels.</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="50dbc-1601">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1601">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="50dbc-1602">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1602">value</span></span>  
<span data-ttu-id="50dbc-1603">コントロールの上と下のスペースの量を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1603">An integer that indicates the amount of space above and below a control; optional.</span></span>

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="50dbc-1604">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1604">Return Value - verticalSpacingValue</span></span>

<span data-ttu-id="50dbc-1605">コントロールの上と下のスペースの量を示す整数。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1605">An integer that indicates the amount of space above and below a control.</span></span>

## <a name="method-viewtype"></a><span data-ttu-id="50dbc-1606">メソッド viewType</span><span class="sxs-lookup"><span data-stu-id="50dbc-1606">Method viewType</span></span>

```xpp
public int viewType([int value])
```

### <a name="parameters---viewtype"></a><span data-ttu-id="50dbc-1607">パラメーター - viewType</span><span class="sxs-lookup"><span data-stu-id="50dbc-1607">Parameters - viewType</span></span>

<span data-ttu-id="50dbc-1608">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1608">value</span></span>  

### <a name="return-value---viewtype"></a><span data-ttu-id="50dbc-1609">戻り値 - viewType</span><span class="sxs-lookup"><span data-stu-id="50dbc-1609">Return Value - viewType</span></span>

## <a name="method-visible"></a><span data-ttu-id="50dbc-1610">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="50dbc-1610">Method visible</span></span>

<span data-ttu-id="50dbc-1611">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1611">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="50dbc-1612">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="50dbc-1612">Parameters - visible</span></span>

<span data-ttu-id="50dbc-1613">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1613">value</span></span>  
<span data-ttu-id="50dbc-1614">コントロールの表示設定に割り当てられる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1614">The value to be assigned to the visible setting for the control; optional.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="50dbc-1615">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="50dbc-1615">Return Value - visible</span></span>

<span data-ttu-id="50dbc-1616">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1616">true if the control is visible; otherwise, false.</span></span>

## <a name="method-width"></a><span data-ttu-id="50dbc-1617">メソッド width</span><span class="sxs-lookup"><span data-stu-id="50dbc-1617">Method width</span></span>

<span data-ttu-id="50dbc-1618">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1618">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="50dbc-1619">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="50dbc-1619">Parameters - width</span></span>

<span data-ttu-id="50dbc-1620">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1620">value</span></span>  
<span data-ttu-id="50dbc-1621">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1621">An integer that indicates how the width is calculated; optional.</span></span> <span data-ttu-id="50dbc-1622">このパラメーターは、次のいずれかの値にすることができます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1622">This parameter can be one of the following values:</span></span>

<!-- -->

<span data-ttu-id="50dbc-1623">モード</span><span class="sxs-lookup"><span data-stu-id="50dbc-1623">mode</span></span>  
<span data-ttu-id="50dbc-1624">幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1624">An integer that indicates how the width is calculated; optional.</span></span> <span data-ttu-id="50dbc-1625">このパラメーターは、次のいずれかの値にすることができます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1625">This parameter can be one of the following values:</span></span>

### <a name="return-value---width"></a><span data-ttu-id="50dbc-1626">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="50dbc-1626">Return Value - width</span></span>

<span data-ttu-id="50dbc-1627">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1627">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="50dbc-1628">備考 - width</span><span class="sxs-lookup"><span data-stu-id="50dbc-1628">Remarks - width</span></span>

<span data-ttu-id="50dbc-1629">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1629">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="50dbc-1630">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1630">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="50dbc-1631">モード</span><span class="sxs-lookup"><span data-stu-id="50dbc-1631">Mode</span></span>             | <span data-ttu-id="50dbc-1632">幅計算</span><span class="sxs-lookup"><span data-stu-id="50dbc-1632">Width calculation</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="50dbc-1633">-1 � 正確</span><span class="sxs-lookup"><span data-stu-id="50dbc-1633">-1 � Exact</span></span>       | <span data-ttu-id="50dbc-1634">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1634">The exact width of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="50dbc-1635">0 � 自動</span><span class="sxs-lookup"><span data-stu-id="50dbc-1635">0 � Auto</span></span>         | <span data-ttu-id="50dbc-1636">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1636">The width of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="50dbc-1637">1 � 列の幅</span><span class="sxs-lookup"><span data-stu-id="50dbc-1637">1 � Column width</span></span> | <span data-ttu-id="50dbc-1638">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1638">The layout of the form determines the width of the control.</span></span>                               |

<span data-ttu-id="50dbc-1639">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1639">The width and the width calculation mode can be set separately.</span></span>

### <a name="examples---width"></a><span data-ttu-id="50dbc-1640">例 - width</span><span class="sxs-lookup"><span data-stu-id="50dbc-1640">Examples - width</span></span>

<span data-ttu-id="50dbc-1641">次の例は、コントロールの幅を 120 ピクセルに設定する width メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1641">The following example shows a call to the width method to set the width of the control to 120 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.width(120,-1); 
}
```

## <a name="method-widthmode"></a><span data-ttu-id="50dbc-1642">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1642">Method widthMode</span></span>

<span data-ttu-id="50dbc-1643">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1643">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="50dbc-1644">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1644">Parameters - widthMode</span></span>

<span data-ttu-id="50dbc-1645">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1645">value</span></span>  
<span data-ttu-id="50dbc-1646">コントロールの幅の計算方法を示す整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1646">An integer that indicates how the width of the control is calculated; optional.</span></span>

### <a name="return-value---widthmode"></a><span data-ttu-id="50dbc-1647">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1647">Return Value - widthMode</span></span>

<span data-ttu-id="50dbc-1648">現在の幅の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1648">An integer value that indicates the current width calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="50dbc-1649">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1649">Remarks - widthMode</span></span>

<span data-ttu-id="50dbc-1650">次の表に従って幅を計算します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1650">Calculate the width according to the following table.</span></span>

| <span data-ttu-id="50dbc-1651">モード</span><span class="sxs-lookup"><span data-stu-id="50dbc-1651">Mode</span></span>         | <span data-ttu-id="50dbc-1652">幅計算</span><span class="sxs-lookup"><span data-stu-id="50dbc-1652">Width calculation</span></span>                                                                         |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="50dbc-1653">正確</span><span class="sxs-lookup"><span data-stu-id="50dbc-1653">Exact</span></span>        | <span data-ttu-id="50dbc-1654">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1654">The exact width of the control in pixels is used.</span></span>                                         |
| <span data-ttu-id="50dbc-1655">自動</span><span class="sxs-lookup"><span data-stu-id="50dbc-1655">Auto</span></span>         | <span data-ttu-id="50dbc-1656">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1656">The width of the control is calculated automatically, and the value parameter is ignored.</span></span> |
| <span data-ttu-id="50dbc-1657">列の幅</span><span class="sxs-lookup"><span data-stu-id="50dbc-1657">Column width</span></span> | <span data-ttu-id="50dbc-1658">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1658">The layout of the form determines the width of the control.</span></span>                               |

<span data-ttu-id="50dbc-1659">計算モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1659">The width of the control might change when the calculation mode is set to Auto or Column width.</span></span>

### <a name="examples---widthmode"></a><span data-ttu-id="50dbc-1660">例 - widthMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1660">Examples - widthMode</span></span>

<span data-ttu-id="50dbc-1661">次の例は、正確なピクセル値に基づいて、コントロールの幅を計算する widthMode メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1661">The following example shows a call to the widthMode method to calculate the width of the control, based on an exact pixel value.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.widthMode(-1); 
    formListControl.widthValue(120); 
}
```

## <a name="method-widthvalue"></a><span data-ttu-id="50dbc-1662">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1662">Method widthValue</span></span>

<span data-ttu-id="50dbc-1663">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1663">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="50dbc-1664">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1664">Parameters - widthValue</span></span>

<span data-ttu-id="50dbc-1665">値</span><span class="sxs-lookup"><span data-stu-id="50dbc-1665">value</span></span>  
<span data-ttu-id="50dbc-1666">コントロールの幅をピクセル単位で指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1666">An integer that specifies the width of the control in pixels; optional.</span></span>

### <a name="return-value---widthvalue"></a><span data-ttu-id="50dbc-1667">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1667">Return Value - widthValue</span></span>

<span data-ttu-id="50dbc-1668">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1668">The width of the control in pixels.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="50dbc-1669">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1669">Remarks - widthValue</span></span>

<span data-ttu-id="50dbc-1670">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1670">To change the width of the control, use the Exact width calculation mode.</span></span>

### <a name="examples---widthvalue"></a><span data-ttu-id="50dbc-1671">例 - widthValue</span><span class="sxs-lookup"><span data-stu-id="50dbc-1671">Examples - widthValue</span></span>

<span data-ttu-id="50dbc-1672">次の例は、コントロールの幅を 120 ピクセルに設定する widthValue メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1672">The following example shows a call to the widthValue method that sets the width of the control to 120 pixels.</span></span>

```xpp
static void createForm(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    int idx4; 
    DictTable dictTable; 
    CustTable custTable; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    formListControl.widthMode(-1); 
    formListControl.widthValue(120); 
}
```

## <a name="method-selectionchanged"></a><span data-ttu-id="50dbc-1673">メソッド selectionChanged</span><span class="sxs-lookup"><span data-stu-id="50dbc-1673">Method selectionChanged</span></span>

```xpp
public void selectionChanged(int Idx, AnyType Data)
```

### <a name="parameters---selectionchanged"></a><span data-ttu-id="50dbc-1674">パラメーター - selectionChanged</span><span class="sxs-lookup"><span data-stu-id="50dbc-1674">Parameters - selectionChanged</span></span>

<span data-ttu-id="50dbc-1675">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1675">Idx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1676">データ</span><span class="sxs-lookup"><span data-stu-id="50dbc-1676">Data</span></span>  

## <a name="method-activateitem"></a><span data-ttu-id="50dbc-1677">メソッド activateItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1677">Method activateItem</span></span>

```xpp
public void activateItem(int Idx)
```

### <a name="parameters---activateitem"></a><span data-ttu-id="50dbc-1678">パラメーター - activateItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1678">Parameters - activateItem</span></span>

<span data-ttu-id="50dbc-1679">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1679">Idx</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="50dbc-1680">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="50dbc-1680">Method inputSearch</span></span>

<span data-ttu-id="50dbc-1681">指定されたテキスト文字列の検索開始日を示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1681">Identifies when the search begins for a specified text string.</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="50dbc-1682">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="50dbc-1682">Parameters - inputSearch</span></span>

<span data-ttu-id="50dbc-1683">searchStr</span><span class="sxs-lookup"><span data-stu-id="50dbc-1683">searchStr</span></span>  
<span data-ttu-id="50dbc-1684">テキスト文字列を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1684">A String data type that specifies a text string.</span></span>

### <a name="remarks---inputsearch"></a><span data-ttu-id="50dbc-1685">備考 - inputSearch</span><span class="sxs-lookup"><span data-stu-id="50dbc-1685">Remarks - inputSearch</span></span>

<span data-ttu-id="50dbc-1686">フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[inputSearch] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1686">To override this method in a form list control, right-click the Methods node below the control, point to Override Method, and then click inputSearch.</span></span> <span data-ttu-id="50dbc-1687">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1687">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-displaycontrol"></a><span data-ttu-id="50dbc-1688">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="50dbc-1688">Method displayControl</span></span>

<span data-ttu-id="50dbc-1689">コントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1689">Displays the control.</span></span>

```xpp
public void displayControl()
```

## <a name="method-onleaving"></a><span data-ttu-id="50dbc-1690">メソッド OnLeaving</span><span class="sxs-lookup"><span data-stu-id="50dbc-1690">Method OnLeaving</span></span>

```xpp
private void OnLeaving([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onleaving"></a><span data-ttu-id="50dbc-1691">パラメーター - OnLeaving</span><span class="sxs-lookup"><span data-stu-id="50dbc-1691">Parameters - OnLeaving</span></span>

<span data-ttu-id="50dbc-1692">sender</span><span class="sxs-lookup"><span data-stu-id="50dbc-1692">sender</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1693">e</span><span class="sxs-lookup"><span data-stu-id="50dbc-1693">e</span></span>  

## <a name="method-update"></a><span data-ttu-id="50dbc-1694">メソッド update</span><span class="sxs-lookup"><span data-stu-id="50dbc-1694">Method update</span></span>

<span data-ttu-id="50dbc-1695">コントロールを更新します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1695">Updates the control.</span></span>

```xpp
public void update([int idx])
```

### <a name="parameters---update"></a><span data-ttu-id="50dbc-1696">パラメーター - update</span><span class="sxs-lookup"><span data-stu-id="50dbc-1696">Parameters - update</span></span>

<span data-ttu-id="50dbc-1697">idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1697">idx</span></span>  

## <a name="method-enddrag"></a><span data-ttu-id="50dbc-1698">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="50dbc-1698">Method endDrag</span></span>

<span data-ttu-id="50dbc-1699">ユーザーがフォーム リスト コントロールの移動を終了した日を示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1699">Identifies when the user has finished moving a form list control.</span></span>

```xpp
public void endDrag()
```

### <a name="remarks---enddrag"></a><span data-ttu-id="50dbc-1700">備考 - endDrag</span><span class="sxs-lookup"><span data-stu-id="50dbc-1700">Remarks - endDrag</span></span>

<span data-ttu-id="50dbc-1701">フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[endDrag] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1701">To override this method in a form list control, right-click the Methods node below the control, point to Override Method, and then click endDrag.</span></span> <span data-ttu-id="50dbc-1702">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1702">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-mouseleave"></a><span data-ttu-id="50dbc-1703">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="50dbc-1703">Method mouseLeave</span></span>

<span data-ttu-id="50dbc-1704">マウス ポインターがコントロールを離れたことを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1704">Indicates that the mouse pointer has left the control.</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-setimagelist"></a><span data-ttu-id="50dbc-1705">メソッド setImagelist</span><span class="sxs-lookup"><span data-stu-id="50dbc-1705">Method setImagelist</span></span>

```xpp
public void setImagelist(Imagelist imageList, [boolean SetLarge])
```

### <a name="parameters---setimagelist"></a><span data-ttu-id="50dbc-1706">パラメーター - setImagelist</span><span class="sxs-lookup"><span data-stu-id="50dbc-1706">Parameters - setImagelist</span></span>

<span data-ttu-id="50dbc-1707">imageList</span><span class="sxs-lookup"><span data-stu-id="50dbc-1707">imageList</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1708">SetLarge</span><span class="sxs-lookup"><span data-stu-id="50dbc-1708">SetLarge</span></span>  

## <a name="method-copy"></a><span data-ttu-id="50dbc-1709">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="50dbc-1709">Method copy</span></span>

<span data-ttu-id="50dbc-1710">ユーザーがコピー操作を実行するときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1710">Identifies when a user performs a copy operation.</span></span>

```xpp
public void copy()
```

### <a name="remarks---copy"></a><span data-ttu-id="50dbc-1711">備考 - copy</span><span class="sxs-lookup"><span data-stu-id="50dbc-1711">Remarks - copy</span></span>

<span data-ttu-id="50dbc-1712">リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [copy] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1712">To override this method on a list view control, right-click the Methods node below the control, point to Override Method, and then click copy.</span></span> <span data-ttu-id="50dbc-1713">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1713">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-dropex"></a><span data-ttu-id="50dbc-1714">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1714">Method dropEx</span></span>

<span data-ttu-id="50dbc-1715">ドロップ操作が現在のコントロールで実行されていることを示すために、dropEx イベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1715">Raises the dropEx event to indicate that a drop operation is being performed on the current control.</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="50dbc-1716">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1716">Parameters - dropEx</span></span>

<span data-ttu-id="50dbc-1717">dragSource</span><span class="sxs-lookup"><span data-stu-id="50dbc-1717">dragSource</span></span>  
<span data-ttu-id="50dbc-1718">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1718">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1719">dragMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1719">dragMode</span></span>  
<span data-ttu-id="50dbc-1720">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1720">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1721">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-1721">x</span></span>  
<span data-ttu-id="50dbc-1722">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1722">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1723">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-1723">y</span></span>  
<span data-ttu-id="50dbc-1724">マウス位置の垂直クライアント座標を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1724">An integer value that indicates the vertical client coordinate of the mouse position.</span></span>

## <a name="method-itemcopy"></a><span data-ttu-id="50dbc-1725">メソッド itemCopy</span><span class="sxs-lookup"><span data-stu-id="50dbc-1725">Method itemCopy</span></span>

```xpp
public void itemCopy(int Idx, int newIdx)
```

### <a name="parameters---itemcopy"></a><span data-ttu-id="50dbc-1726">パラメーター - itemCopy</span><span class="sxs-lookup"><span data-stu-id="50dbc-1726">Parameters - itemCopy</span></span>

<span data-ttu-id="50dbc-1727">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1727">Idx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1728">newIdx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1728">newIdx</span></span>  

## <a name="method-cut"></a><span data-ttu-id="50dbc-1729">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="50dbc-1729">Method cut</span></span>

<span data-ttu-id="50dbc-1730">ユーザーがカット操作を実行するときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1730">Identifies when the user performs a cut operation.</span></span>

```xpp
public void cut()
```

### <a name="remarks---cut"></a><span data-ttu-id="50dbc-1731">備考 - cut</span><span class="sxs-lookup"><span data-stu-id="50dbc-1731">Remarks - cut</span></span>

<span data-ttu-id="50dbc-1732">リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [cut] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1732">To override this method on a list view control, right-click the Methods node below the control, point to Override Method, and then click cut.</span></span> <span data-ttu-id="50dbc-1733">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1733">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-itemmoved"></a><span data-ttu-id="50dbc-1734">メソッド itemMoved</span><span class="sxs-lookup"><span data-stu-id="50dbc-1734">Method itemMoved</span></span>

```xpp
public void itemMoved(int Idx, int newIdx)
```

### <a name="parameters---itemmoved"></a><span data-ttu-id="50dbc-1735">パラメーター - itemMoved</span><span class="sxs-lookup"><span data-stu-id="50dbc-1735">Parameters - itemMoved</span></span>

<span data-ttu-id="50dbc-1736">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1736">Idx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1737">newIdx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1737">newIdx</span></span>  

## <a name="method-registeroverridemethod"></a><span data-ttu-id="50dbc-1738">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="50dbc-1738">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="50dbc-1739">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="50dbc-1739">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="50dbc-1740">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="50dbc-1740">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1741">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="50dbc-1741">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1742">overrideObject</span><span class="sxs-lookup"><span data-stu-id="50dbc-1742">overrideObject</span></span>  

## <a name="method-paste"></a><span data-ttu-id="50dbc-1743">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="50dbc-1743">Method paste</span></span>

<span data-ttu-id="50dbc-1744">クリップボードの内容をコントロールに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1744">Pastes the contents of the clipboard into the control.</span></span>

```xpp
public void paste()
```

## <a name="method-lostfocus"></a><span data-ttu-id="50dbc-1745">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="50dbc-1745">Method lostFocus</span></span>

<span data-ttu-id="50dbc-1746">コントロールがフォーカスを失ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1746">Indicates that the control has lost focus.</span></span>

```xpp
public void lostFocus()
```

## <a name="method-onselectionchanged"></a><span data-ttu-id="50dbc-1747">メソッド OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="50dbc-1747">Method OnSelectionChanged</span></span>

```xpp
private void OnSelectionChanged([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onselectionchanged"></a><span data-ttu-id="50dbc-1748">パラメーター - OnSelectionChanged</span><span class="sxs-lookup"><span data-stu-id="50dbc-1748">Parameters - OnSelectionChanged</span></span>

<span data-ttu-id="50dbc-1749">sender</span><span class="sxs-lookup"><span data-stu-id="50dbc-1749">sender</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1750">e</span><span class="sxs-lookup"><span data-stu-id="50dbc-1750">e</span></span>  

## <a name="method-hottrackitem"></a><span data-ttu-id="50dbc-1751">メソッド hotTrackItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1751">Method hotTrackItem</span></span>

<span data-ttu-id="50dbc-1752">ユーザーがマウス ポインターをフォーム リスト コントロール上に移動するときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1752">Identifies when a user moves the mouse pointer over a form list control.</span></span>

```xpp
public void hotTrackItem(int Idx)
```

### <a name="parameters---hottrackitem"></a><span data-ttu-id="50dbc-1753">パラメーター - hotTrackItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1753">Parameters - hotTrackItem</span></span>

<span data-ttu-id="50dbc-1754">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1754">Idx</span></span>  
<span data-ttu-id="50dbc-1755">フォーム リスト コントロールのインデックスを指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1755">An Integer data type that specifies the index for a form list control.</span></span>

### <a name="remarks---hottrackitem"></a><span data-ttu-id="50dbc-1756">備考 - hotTrackItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1756">Remarks - hotTrackItem</span></span>

<span data-ttu-id="50dbc-1757">フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[hotTrackItem] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1757">To override this method in a form list control, right-click the Methods node below the control, point to Override Method, and then click hotTrackItem.</span></span> <span data-ttu-id="50dbc-1758">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1758">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-setcount"></a><span data-ttu-id="50dbc-1759">メソッド setCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-1759">Method setCount</span></span>

```xpp
public void setCount(int count)
```

### <a name="parameters---setcount"></a><span data-ttu-id="50dbc-1760">パラメーター - setCount</span><span class="sxs-lookup"><span data-stu-id="50dbc-1760">Parameters - setCount</span></span>

<span data-ttu-id="50dbc-1761">カウント</span><span class="sxs-lookup"><span data-stu-id="50dbc-1761">count</span></span>  

## <a name="method-dragleave"></a><span data-ttu-id="50dbc-1762">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="50dbc-1762">Method dragLeave</span></span>

<span data-ttu-id="50dbc-1763">ユーザーがフォーム リスト コントロールの境界からオブジェクトをドラッグするときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1763">Identifies when a user drags an object out of the bounds of a form list control.</span></span>

```xpp
public void dragLeave()
```

### <a name="remarks---dragleave"></a><span data-ttu-id="50dbc-1764">備考 - dragLeave</span><span class="sxs-lookup"><span data-stu-id="50dbc-1764">Remarks - dragLeave</span></span>

<span data-ttu-id="50dbc-1765">フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[dragLeave] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1765">To override this method in a form list control, right-click the Methods node below the control, point to Override Method, and then click dragLeave.</span></span> <span data-ttu-id="50dbc-1766">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1766">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-itemdeleted"></a><span data-ttu-id="50dbc-1767">メソッド itemDeleted</span><span class="sxs-lookup"><span data-stu-id="50dbc-1767">Method itemDeleted</span></span>

```xpp
public void itemDeleted(int Idx, AnyType Data)
```

### <a name="parameters---itemdeleted"></a><span data-ttu-id="50dbc-1768">パラメーター - itemDeleted</span><span class="sxs-lookup"><span data-stu-id="50dbc-1768">Parameters - itemDeleted</span></span>

<span data-ttu-id="50dbc-1769">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1769">Idx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1770">データ</span><span class="sxs-lookup"><span data-stu-id="50dbc-1770">Data</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="50dbc-1771">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="50dbc-1771">Method prefColumnSize</span></span>

<span data-ttu-id="50dbc-1772">フォーム コントロールの最適な列の幅と高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1772">Specifies the preferred column width and height for the form control.</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="50dbc-1773">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="50dbc-1773">Parameters - prefColumnSize</span></span>

<span data-ttu-id="50dbc-1774">width</span><span class="sxs-lookup"><span data-stu-id="50dbc-1774">width</span></span>  
<span data-ttu-id="50dbc-1775">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1775">The preferred height of the control.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1776">height</span><span class="sxs-lookup"><span data-stu-id="50dbc-1776">height</span></span>  
<span data-ttu-id="50dbc-1777">コントロールの適切な高さです。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1777">The preferred height of the control.</span></span>

## <a name="method-ongotfocus"></a><span data-ttu-id="50dbc-1778">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="50dbc-1778">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="50dbc-1779">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="50dbc-1779">Parameters - OnGotFocus</span></span>

<span data-ttu-id="50dbc-1780">sender</span><span class="sxs-lookup"><span data-stu-id="50dbc-1780">sender</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1781">e</span><span class="sxs-lookup"><span data-stu-id="50dbc-1781">e</span></span>  

## <a name="method-settext"></a><span data-ttu-id="50dbc-1782">メソッド setText</span><span class="sxs-lookup"><span data-stu-id="50dbc-1782">Method setText</span></span>

```xpp
public void setText(int Idx, str Text, [int SubItem])
```

### <a name="parameters---settext"></a><span data-ttu-id="50dbc-1783">パラメーター - setText</span><span class="sxs-lookup"><span data-stu-id="50dbc-1783">Parameters - setText</span></span>

<span data-ttu-id="50dbc-1784">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1784">Idx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1785">テキスト</span><span class="sxs-lookup"><span data-stu-id="50dbc-1785">Text</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1786">SubItem</span><span class="sxs-lookup"><span data-stu-id="50dbc-1786">SubItem</span></span>  

## <a name="method-itemchanged"></a><span data-ttu-id="50dbc-1787">メソッド itemChanged</span><span class="sxs-lookup"><span data-stu-id="50dbc-1787">Method itemChanged</span></span>

```xpp
public void itemChanged(int Idx, AnyType Data)
```

### <a name="parameters---itemchanged"></a><span data-ttu-id="50dbc-1788">パラメーター - itemChanged</span><span class="sxs-lookup"><span data-stu-id="50dbc-1788">Parameters - itemChanged</span></span>

<span data-ttu-id="50dbc-1789">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1789">Idx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1790">データ</span><span class="sxs-lookup"><span data-stu-id="50dbc-1790">Data</span></span>  

## <a name="method-doubleclick"></a><span data-ttu-id="50dbc-1791">メソッド doubleClick</span><span class="sxs-lookup"><span data-stu-id="50dbc-1791">Method doubleClick</span></span>

<span data-ttu-id="50dbc-1792">ユーザーがフォーム内のリスト コントロールのアイテムをダブルクリックするときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1792">Identifies when a user double-clicks an item in a form list control.</span></span>

```xpp
public void doubleClick()
```

### <a name="remarks---doubleclick"></a><span data-ttu-id="50dbc-1793">備考 - doubleClick</span><span class="sxs-lookup"><span data-stu-id="50dbc-1793">Remarks - doubleClick</span></span>

<span data-ttu-id="50dbc-1794">リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [doubleClick] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1794">To override this method on a list view control, right-click the Methods node below the control, point to Override Method, and then click doubleClick.</span></span> <span data-ttu-id="50dbc-1795">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1795">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="50dbc-1796">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="50dbc-1796">Method resetUserSetting</span></span>

<span data-ttu-id="50dbc-1797">コントロールのユーザー設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1797">Resets the user settings for the control.</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-setfocus"></a><span data-ttu-id="50dbc-1798">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="50dbc-1798">Method setFocus</span></span>

<span data-ttu-id="50dbc-1799">コントロールにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1799">Sets the focus on the control.</span></span>

```xpp
public void setFocus()
```

## <a name="method-mouseenter"></a><span data-ttu-id="50dbc-1800">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="50dbc-1800">Method mouseEnter</span></span>

<span data-ttu-id="50dbc-1801">ユーザーがマウス ポインターをコントロール エリアに移動させると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1801">Is called when the user moves the mouse pointer into the control area.</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="50dbc-1802">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="50dbc-1802">Parameters - mouseEnter</span></span>

<span data-ttu-id="50dbc-1803">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-1803">x</span></span>  
<span data-ttu-id="50dbc-1804">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1804">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1805">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-1805">y</span></span>  
<span data-ttu-id="50dbc-1806">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1806">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1807">ボタン</span><span class="sxs-lookup"><span data-stu-id="50dbc-1807">button</span></span>  
<span data-ttu-id="50dbc-1808">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1808">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1809">Ctrl</span><span class="sxs-lookup"><span data-stu-id="50dbc-1809">Ctrl</span></span>  
<span data-ttu-id="50dbc-1810">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1810">A Boolean value that indicates whether the SHIFT key is down.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1811">シフト</span><span class="sxs-lookup"><span data-stu-id="50dbc-1811">Shift</span></span>  
<span data-ttu-id="50dbc-1812">Shift キーが押されているかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1812">A Boolean value that indicates whether the SHIFT key is down.</span></span>

## <a name="method-allitemsdeleted"></a><span data-ttu-id="50dbc-1813">メソッド allItemsDeleted</span><span class="sxs-lookup"><span data-stu-id="50dbc-1813">Method allItemsDeleted</span></span>

<span data-ttu-id="50dbc-1814">フォーム リスト コントロール内のすべてのアイテムが削除される日を示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1814">Identifies when all the items in a form list control are deleted.</span></span>

```xpp
public void allItemsDeleted()
```

### <a name="remarks---allitemsdeleted"></a><span data-ttu-id="50dbc-1815">備考 - allItemsDeleted</span><span class="sxs-lookup"><span data-stu-id="50dbc-1815">Remarks - allItemsDeleted</span></span>

<span data-ttu-id="50dbc-1816">フォーム リスト コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして、[allItemsDeleted] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1816">To override this method in a form list control, right-click the Methods node below the control, point to Override Method, and then click allItemsDeleted.</span></span> <span data-ttu-id="50dbc-1817">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1817">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-drop"></a><span data-ttu-id="50dbc-1818">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="50dbc-1818">Method drop</span></span>

<span data-ttu-id="50dbc-1819">ユーザーがフォーム リスト コントロールまたはフォーム リスト コントロールのアイテムを新しい位置にドロップするときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1819">Identifies when a user drops a form list control or an item in a form list control into a new position.</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="50dbc-1820">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="50dbc-1820">Parameters - drop</span></span>

<span data-ttu-id="50dbc-1821">dragSource</span><span class="sxs-lookup"><span data-stu-id="50dbc-1821">dragSource</span></span>  
<span data-ttu-id="50dbc-1822">オブジェクトの位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1822">An Integer data type that indicates the y-coordinate of the object's position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1823">dragMode</span><span class="sxs-lookup"><span data-stu-id="50dbc-1823">dragMode</span></span>  
<span data-ttu-id="50dbc-1824">オブジェクトの位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1824">An Integer data type that indicates the y-coordinate of the object's position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1825">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-1825">x</span></span>  
<span data-ttu-id="50dbc-1826">オブジェクトの位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1826">An Integer data type that indicates the y-coordinate of the object's position.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1827">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-1827">y</span></span>  
<span data-ttu-id="50dbc-1828">オブジェクトの位置の y 座標を示す整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1828">An Integer data type that indicates the y-coordinate of the object's position.</span></span>

### <a name="remarks---drop"></a><span data-ttu-id="50dbc-1829">備考 - drop</span><span class="sxs-lookup"><span data-stu-id="50dbc-1829">Remarks - drop</span></span>

<span data-ttu-id="50dbc-1830">このメソッドは、DragDrop プロパティがコントロールの手動に設定されていて、beginDrag イベントがすでに開始されている場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1830">This method is called only if the DragDrop property is set to Manual for the control and a beginDrag event has already been started.</span></span> <span data-ttu-id="50dbc-1831">イベントの詳細については、beginDrag を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1831">For more information about the event, see beginDrag.</span></span> <span data-ttu-id="50dbc-1832">リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [drop] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1832">To override this method on a list view control, right-click the Methods node below the control, point to Override Method, and then click drop.</span></span> <span data-ttu-id="50dbc-1833">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1833">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-columnclicked"></a><span data-ttu-id="50dbc-1834">メソッド columnClicked</span><span class="sxs-lookup"><span data-stu-id="50dbc-1834">Method columnClicked</span></span>

<span data-ttu-id="50dbc-1835">ユーザーがフォーム内のリスト ビュー コントロールの列をクリックするときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1835">Identifies when a user clicks a column in a list view control in a form.</span></span>

```xpp
public void columnClicked(int Column)
```

### <a name="parameters---columnclicked"></a><span data-ttu-id="50dbc-1836">パラメーター - columnClicked</span><span class="sxs-lookup"><span data-stu-id="50dbc-1836">Parameters - columnClicked</span></span>

<span data-ttu-id="50dbc-1837">円柱</span><span class="sxs-lookup"><span data-stu-id="50dbc-1837">Column</span></span>  
<span data-ttu-id="50dbc-1838">フォーム列を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1838">An Integer data type that specifies a form column.</span></span>

### <a name="remarks---columnclicked"></a><span data-ttu-id="50dbc-1839">備考 - columnClicked</span><span class="sxs-lookup"><span data-stu-id="50dbc-1839">Remarks - columnClicked</span></span>

<span data-ttu-id="50dbc-1840">リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をクリックして [columnClicked] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1840">To override this method on a list view control, right-click the Methods node below the control, click Override Method, and then click columnClicked.</span></span> <span data-ttu-id="50dbc-1841">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1841">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-getstateimagelist"></a><span data-ttu-id="50dbc-1842">メソッド getStateImagelist</span><span class="sxs-lookup"><span data-stu-id="50dbc-1842">Method getStateImagelist</span></span>

```xpp
public void getStateImagelist()
```

## <a name="method-onlostfocus"></a><span data-ttu-id="50dbc-1843">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="50dbc-1843">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="50dbc-1844">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="50dbc-1844">Parameters - OnLostFocus</span></span>

<span data-ttu-id="50dbc-1845">sender</span><span class="sxs-lookup"><span data-stu-id="50dbc-1845">sender</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1846">e</span><span class="sxs-lookup"><span data-stu-id="50dbc-1846">e</span></span>  

## <a name="method-setitempos"></a><span data-ttu-id="50dbc-1847">メソッド setItemPos</span><span class="sxs-lookup"><span data-stu-id="50dbc-1847">Method setItemPos</span></span>

<span data-ttu-id="50dbc-1848">フォーム リスト コントロール内の項目の位置を設定します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1848">Sets the position of an item in a form list control.</span></span>

```xpp
public void setItemPos(int Item, int x, int y)
```

### <a name="parameters---setitempos"></a><span data-ttu-id="50dbc-1849">パラメーター - setItemPos</span><span class="sxs-lookup"><span data-stu-id="50dbc-1849">Parameters - setItemPos</span></span>

<span data-ttu-id="50dbc-1850">項目</span><span class="sxs-lookup"><span data-stu-id="50dbc-1850">Item</span></span>  
<span data-ttu-id="50dbc-1851">項目の位置の y 座標を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1851">An Integer data type that specifies the y-coordinate of the position of an item.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1852">x</span><span class="sxs-lookup"><span data-stu-id="50dbc-1852">x</span></span>  
<span data-ttu-id="50dbc-1853">項目の位置の y 座標を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1853">An Integer data type that specifies the y-coordinate of the position of an item.</span></span>

<!-- -->

<span data-ttu-id="50dbc-1854">y</span><span class="sxs-lookup"><span data-stu-id="50dbc-1854">y</span></span>  
<span data-ttu-id="50dbc-1855">項目の位置の y 座標を指定する整数データ型です。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1855">An Integer data type that specifies the y-coordinate of the position of an item.</span></span>

### <a name="examples---setitempos"></a><span data-ttu-id="50dbc-1856">例 - setItemPos</span><span class="sxs-lookup"><span data-stu-id="50dbc-1856">Examples - setItemPos</span></span>

<span data-ttu-id="50dbc-1857">次の例は、フォーム リスト コントロール内の各項目の位置を指定する setItemPos メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1857">The following example shows a call to the setItemPos method to specify the position of each item in the form list control.</span></span> <span data-ttu-id="50dbc-1858">while select ステートメントは、CustTable テーブルからアカウント番号を取得し、そのデータをコンテナーに格納します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1858">The while select statement retrieves account numbers from the CustTable table and then stores the data in a container.</span></span> <span data-ttu-id="50dbc-1859">変数内の項目は、FormListControl.addItem メソッドを呼び出すことによってフォーム リスト コントロールに追加されます。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1859">The items in the variable are added to the form list control by calling the FormListControl.addItem method.</span></span>

```xpp
static void createForm2(Args _args) 
{ 
    Args args; 
    Form form; 
    FormRun formRun; 
    FormBuildDesign formBuildDesign; 
    FormBuildDataSource formBuildDataSource; 
    FormBuildListControl formBuildListControl; 
    FormListControl formListControl; 
    FormListItem formListItem; 
    DictTable dictTable; 
    int idx4; 
    str string; 
    container conAccountNum; 
    CustTable custTable; 
    int numAccounts; 
    int i; 
    int item; 
    // Create the form header. 
    form = new Form(); 
    // Add data sources to the form. 
    dictTable = new DictTable(tableNum(custTable)); 
    formBuildDataSource = form.addDataSource(dictTable.name()); 
    formBuildDataSource.table(dictTable.id()); 
    // Create the form design. 
    formBuildDesign = form.addDesign("Design"); 
    formBuildDesign.caption("myForm"); 
    // Add a form list control. 
    formBuildListControl = 
 formBuildDesign.addControl(FormControlType::ListView,"List"); 
    idx4 = formBuildListControl.id(); 
    args = new Args(); 
    args.object(form); 
    // Create the run-time form. 
    formRun = classfactory.formRunClass(args); 
    formRun.run(); 
    formRun.detach(); 
    formListControl = formRun.control(idx4); 
    // Add items to the form list control. 
    while select custTable 
        where custTable.AccountNum >= 
 "4000" && custTable.AccountNum <= "4040" 
    { 
        conAccountNum += [[custTable.AccountNum]]; 
    } 
    numAccounts = conlen(conAccountNum); 
    for(i = 1; i <= numAccounts; i++) 
    { 
        string = conPeek(conAccountNum,i); 
        formListItem = new FormListItem(string); 
        item = formListControl.addItem(formListItem); 
        formListControl.setItemPos(item,1,5); 
    } 
}
```

## <a name="method-gotfocus"></a><span data-ttu-id="50dbc-1860">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="50dbc-1860">Method gotFocus</span></span>

<span data-ttu-id="50dbc-1861">コントロールがフォーカスを受信したことを示します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1861">Indicates that the control has received focus.</span></span>

```xpp
public void gotFocus()
```

## <a name="method-enter"></a><span data-ttu-id="50dbc-1862">メソッド enter</span><span class="sxs-lookup"><span data-stu-id="50dbc-1862">Method enter</span></span>

```xpp
public void enter()
```

## <a name="method-onenter"></a><span data-ttu-id="50dbc-1863">メソッド OnEnter</span><span class="sxs-lookup"><span data-stu-id="50dbc-1863">Method OnEnter</span></span>

```xpp
private void OnEnter([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onenter"></a><span data-ttu-id="50dbc-1864">パラメーター - OnEnter</span><span class="sxs-lookup"><span data-stu-id="50dbc-1864">Parameters - OnEnter</span></span>

<span data-ttu-id="50dbc-1865">sender</span><span class="sxs-lookup"><span data-stu-id="50dbc-1865">sender</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1866">e</span><span class="sxs-lookup"><span data-stu-id="50dbc-1866">e</span></span>  

## <a name="method-context"></a><span data-ttu-id="50dbc-1867">メソッド context</span><span class="sxs-lookup"><span data-stu-id="50dbc-1867">Method context</span></span>

<span data-ttu-id="50dbc-1868">ユーザーがショートカット メニューをフォーム リスト コントロールで開くときを識別します。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1868">Identifies when the user opens a shortcut menu in a form list control.</span></span>

```xpp
public void context()
```

### <a name="remarks---context"></a><span data-ttu-id="50dbc-1869">備考 - context</span><span class="sxs-lookup"><span data-stu-id="50dbc-1869">Remarks - context</span></span>

<span data-ttu-id="50dbc-1870">リスト ビュー コントロールでこのメソッドをオーバーライドするには、コントロールの下のメソッド ノードを右クリックし、[メソッドのオーバーライド] をポイントして [context] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1870">To override this method on a list view control, right-click the Methods node below the control, point to Override Method, and then click context.</span></span> <span data-ttu-id="50dbc-1871">フォームおよびコードのベスト プラクティスについては、「フォームにコードがありません」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50dbc-1871">For information about best practices for forms and code, see No Code in Forms.</span></span>

## <a name="method-begineditlabel"></a><span data-ttu-id="50dbc-1872">メソッド beginEditLabel</span><span class="sxs-lookup"><span data-stu-id="50dbc-1872">Method beginEditLabel</span></span>

```xpp
public void beginEditLabel(int Idx)
```

### <a name="parameters---begineditlabel"></a><span data-ttu-id="50dbc-1873">パラメーター - beginEditLabel</span><span class="sxs-lookup"><span data-stu-id="50dbc-1873">Parameters - beginEditLabel</span></span>

<span data-ttu-id="50dbc-1874">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1874">Idx</span></span>  

## <a name="method-iteminserted"></a><span data-ttu-id="50dbc-1875">メソッド itemInserted</span><span class="sxs-lookup"><span data-stu-id="50dbc-1875">Method itemInserted</span></span>

```xpp
public void itemInserted(int Idx, AnyType Data)
```

### <a name="parameters---iteminserted"></a><span data-ttu-id="50dbc-1876">パラメーター - itemInserted</span><span class="sxs-lookup"><span data-stu-id="50dbc-1876">Parameters - itemInserted</span></span>

<span data-ttu-id="50dbc-1877">Idx</span><span class="sxs-lookup"><span data-stu-id="50dbc-1877">Idx</span></span>  

<!-- -->

<span data-ttu-id="50dbc-1878">データ</span><span class="sxs-lookup"><span data-stu-id="50dbc-1878">Data</span></span>  

