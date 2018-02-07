---
title: "フォーミュラ デザイナー"
description: "このトピックでは、ツリー ビューでフォーミュラ デザイナーを使用して式の分析および管理する方法について説明します。"
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: d9b61e545067db592545d5fbce7b4315c51a8bf8
ms.contentlocale: ja-jp
ms.lasthandoff: 02/07/2018

---

# <a name="formula-designer"></a><span data-ttu-id="d3162-103">フォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="d3162-103">Formula designer</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d3162-104">このトピックでは、ツリー ビューでフォーミュラ デザイナーを使用して式の分析および管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d3162-104">This topic explains how to use the formula designer to analyze and maintain formulas in a tree view.</span></span>

<span data-ttu-id="d3162-105">[**リリース済製品**] ページから [**フォーミュラ デザイナー**] ページを開くと、左ウィンドウのツリーはリリース済製品に対する連産品および材料の階層の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="d3162-105">When you open the **Formula designer** page from the **Released products** page, the tree in the left pane shows the list of co-products and the hierarchy of ingredients for the released product.</span></span> <span data-ttu-id="d3162-106">構造は、選択した品目およびその材料、品目の既定の注文サイト、および実際の日付で有効また承認済であるフォーミュラの階層から派生します。</span><span class="sxs-lookup"><span data-stu-id="d3162-106">The structure is derived from the hierarchy of formulas that are active and approved for the selected item and its ingredients, the default order site of the item, and the actual date.</span></span>

<span data-ttu-id="d3162-107">[**設定**] をクリックして、さまざまなコンフィギュレーションの選択や、ツリーの行に表示する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="d3162-107">Click **Setup** to select different configurations and specify what information appears on the lines of the tree.</span></span>

<span data-ttu-id="d3162-108">ビューの最初の選択内容を変更するには、**[フィルター]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3162-108">Click **Filter** to change the initial selection in the view.</span></span> <span data-ttu-id="d3162-109">表示原則を [**選択済/有効**] または [**選択済**] に設定すると、ビューで使用する個々のフォーミュラまたは工順バージョンを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-109">If you set the display principle to **Selected/Active** or **Selected**, you can select individual formula or route versions to use in the view.</span></span> <span data-ttu-id="d3162-110">[フォーミュラ デザイナー] で表示または管理する、未承認で有効でないフォーミュラ バージョンを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-110">You can select non-approved and non-active formula versions to show or maintain in the formula designer.</span></span>  

> [!NOTE]
> <span data-ttu-id="d3162-111">[**部品表**] リスト ページから [**フォーミュラ デザイナー**] ページを開くと、工順情報が表示されません。</span><span class="sxs-lookup"><span data-stu-id="d3162-111">If you open the **Formula designer** page from the **Bills of materials** list page, it doesn't show route information.</span></span> <span data-ttu-id="d3162-112">現時点では、フォーミュラまたは工順バージョンの選択は、[フォーミュラ デザイナー] のすべてのインスタンスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d3162-112">Currently, the selection of a formula or route version applies to all instances of the formula designer.</span></span>  

<span data-ttu-id="d3162-113">次のセクションでは、[BOM デザイナー] で使用できる機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d3162-113">The following sections describe the functionality that is available in the BOM designer.</span></span>

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a><span data-ttu-id="d3162-114">[フォーミュラ デザイナー] を使用して、フォーミュラ構造を分析します</span><span class="sxs-lookup"><span data-stu-id="d3162-114">Analyze a formula structure by using the formula designer</span></span>
<span data-ttu-id="d3162-115">[フォーミュラ デザイナー] には 2 つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="d3162-115">The formula designer has two sections:</span></span>

-   <span data-ttu-id="d3162-116">フォーミュラ 構造のツリー ビュー。</span><span class="sxs-lookup"><span data-stu-id="d3162-116">The tree view of the formula structure.</span></span>
-   <span data-ttu-id="d3162-117">選択したデータの詳細を示す詳細セクション。</span><span class="sxs-lookup"><span data-stu-id="d3162-117">The details section, which shows details of the selected data.</span></span> <span data-ttu-id="d3162-118">ツリー ビューのノードを選択すると、詳細セクションのクイック タブがそのノードに基づいて更新されます。</span><span class="sxs-lookup"><span data-stu-id="d3162-118">When you select a node in the tree view, the FastTabs in the details section are updated based on that node:</span></span>
    -   <span data-ttu-id="d3162-119">[**フォーミュラ明細行の詳細**] – ツリー ビューで選択したフォーミュラ明細行の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="d3162-119">**Formula line details** – View the details of the formula line that is selected in the tree view.</span></span>
    -   <span data-ttu-id="d3162-120">[**品目データ**] – 選択したノードで使用されるメインの品目または品目の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="d3162-120">**Item data** – View the details of the main item or the item that is used in the selected node.</span></span> <span data-ttu-id="d3162-121">選択した品目を管理するには、**[リリースされた製品の編集]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3162-121">You can click **Edit released product** to maintain the selected item.</span></span>
    -   <span data-ttu-id="d3162-122">[**フォーミュラ**] – 選択したノードに関連付けられるフォーミュラのヘッダーを表示します。</span><span class="sxs-lookup"><span data-stu-id="d3162-122">**Formula** – View the header of the formula that is related to the selected node.</span></span>
    -   <span data-ttu-id="d3162-123">[**Route**] – 選択したノードに関連付けられる Route のヘッダーを表示します。</span><span class="sxs-lookup"><span data-stu-id="d3162-123">**Route** – View the header of the route that is related to the selected node.</span></span>
    -   <span data-ttu-id="d3162-124">[**工順工程**] –は、工順の工程のプレビューを表示します。</span><span class="sxs-lookup"><span data-stu-id="d3162-124">**Route operations** – View a preview of the operations for the route.</span></span> <span data-ttu-id="d3162-125">特定の工程に割り当てられる部品表 (BOM) 明細行が選択されている場合、工程は [**工程のコンフィギュレーションの準備**] としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="d3162-125">When a bill of materials (BOM) line that is assigned to a specific operation is selected, the operation is marked as **Component needed at operations**.</span></span>

## <a name="select-a-formula-and-route"></a><span data-ttu-id="d3162-126">フォーミュラおよび工順を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3162-126">Select a formula and route</span></span>
<span data-ttu-id="d3162-127">フォーミュラおよび工順に適用されるフィルタは、[フォーミュラ デザイナー] のヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3162-127">The filter that is applied for the formula and route is shown in the header of the formula designer.</span></span> <span data-ttu-id="d3162-128">**[フィルタ]** ダイアログ ボックスを使用してフィルタを変更できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-128">You can change the filter by using the **Filter** dialog box.</span></span> <span data-ttu-id="d3162-129">次の表は、このダイアログ ボックスのフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="d3162-129">The following table describes the fields in this dialog box.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d3162-130">フィールド</span><span class="sxs-lookup"><span data-stu-id="d3162-130">Field</span></span></th>
<th><span data-ttu-id="d3162-131">説明</span><span class="sxs-lookup"><span data-stu-id="d3162-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3162-132">製品分析コード</span><span class="sxs-lookup"><span data-stu-id="d3162-132">Product dimensions</span></span></td>
<td><span data-ttu-id="d3162-133">選択された完成品が製品マスターの場合、主要な選択に対する有効な製品分析コードを定義できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-133">If the selected finished product is a product master, you can define the active product dimensions for the main selection.</span></span> <span data-ttu-id="d3162-134">製品マスターではない製品の [フォーミュラ デザイナー] を開いた場合は、[<strong>フィルター</strong>] ダイアログ ボックスで製品分析コードを選択できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d3162-134">Note that if you open the formula designer for a product that isn't a product master, no product dimensions can be selected in the <strong>Filter</strong> dialog box.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3162-135">サイト</span><span class="sxs-lookup"><span data-stu-id="d3162-135">Site</span></span></td>
<td><span data-ttu-id="d3162-136">材料ツリーが表示されるサイトを変更します。</span><span class="sxs-lookup"><span data-stu-id="d3162-136">Change the site that the ingredient tree is shown for.</span></span> <span data-ttu-id="d3162-137">既定のサイトは、完成品目の既定の在庫サイトです。</span><span class="sxs-lookup"><span data-stu-id="d3162-137">The default site is the default inventory site of the finished item.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3162-138">表示原則</span><span class="sxs-lookup"><span data-stu-id="d3162-138">Display principle</span></span></td>
<td><p><span data-ttu-id="d3162-139">現在の式構造と現在の工順に適用されるバージョン表示原則を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3162-139">Select the version display principle that applies to the current formula structure and the current route:</span></span></p>
<ul>
<li><span data-ttu-id="d3162-140">原則が [<strong>有効</strong>] または [<strong>選択済/有効</strong>] に設定されている場合は、この日付の有効な式または工順のバージョンが検出されます。</span><span class="sxs-lookup"><span data-stu-id="d3162-140">When the principle is set to <strong>Active</strong> or <strong>Selected/Active</strong>, the valid formula or route version for this date is found.</span></span></li>
<li><span data-ttu-id="d3162-141">原則が [<strong>選択済/有効</strong>] または [<strong>選択済</strong>] に設定されている場合、[<strong>フォーミュラ</strong>] &gt; [<strong>フォーミュラ バージョン</strong>] または [<strong>工順</strong>] &gt; [<strong>工順バージョン</strong>] をクリックしてフォーミュラ バージョンまたは工順バージョンを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-141">When the principle is set to <strong>Selected/Active</strong> or <strong>Selected</strong>, you can select a formula version or route version by clicking <strong>Formula</strong> &gt; <strong>Formula versions</strong> or <strong>Route</strong> &gt; <strong>Route versions</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3162-142">バージョン日付</span><span class="sxs-lookup"><span data-stu-id="d3162-142">Version date</span></span></td>
<td><span data-ttu-id="d3162-143">式および工順のバージョン日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3162-143">Enter the version date for the formula and route.</span></span> <span data-ttu-id="d3162-144">このバージョンは、式バージョン設定におけるバージョン日付に基づく、特定の日付で使用される式バージョンを識別します。</span><span class="sxs-lookup"><span data-stu-id="d3162-144">The version identifies which formula version is used on a specific date, based on the version dates in the formula version setup.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3162-145">開始数量</span><span class="sxs-lookup"><span data-stu-id="d3162-145">From quantity</span></span></td>
<td><span data-ttu-id="d3162-146">固有の「開始」数量を選択してバージョンをフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="d3162-146">Filter the versions by selecting a specific "from" quantity.</span></span> <span data-ttu-id="d3162-147">値を設定すると、別のフォーミュラおよび工順バージョンが選択されることがあります。</span><span class="sxs-lookup"><span data-stu-id="d3162-147">If you set a value, different formula and route versions might be selected.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3162-148">有効のみを表示</span><span class="sxs-lookup"><span data-stu-id="d3162-148">Show valid only</span></span></td>
<td><span data-ttu-id="d3162-149">このチェック ボックスを選択すると、有効な日付を持つフォーミュラ明細行のみがツリー構造に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3162-149">When you select the check box, the tree structure shows only formula lines that have valid dates.</span></span> <span data-ttu-id="d3162-150">フォーミュラ明細行を右クリックまたはダブルクリックして [<strong>フォーミュラ明細行の編集</strong>] ページを開くと、そのフォーミュラ明細行の有効期間を確認できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-150">Right-click or double-click a formula line to open the <strong>Edit formula line</strong> page, where you can see the validity dates for that formula line.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3162-151">[フォーミュラ デザイナー] を使用して 1 つ以上のファントムのレベルで構成されるフォーミュラを確認または編集すると、上位品目と関連付けられる工順は通常、フォーミュラ階層全体に及びます。</span><span class="sxs-lookup"><span data-stu-id="d3162-151">When you use the formula designer to review or edit formulas that consist of one or more levels of phantoms, the route that is associated with the top item typically spans the complete formula hierarchy.</span></span> <span data-ttu-id="d3162-152">概要を簡略化するために、[**表示**] &gt; [**工順のロック**] をクリックして表示に含まれるトップレベルの工順をロックできます。</span><span class="sxs-lookup"><span data-stu-id="d3162-152">To simplify the overview, you can lock the top-level route in the display by clicking **View** &gt; **Lock route**.</span></span> <span data-ttu-id="d3162-153">工順のロックを解除するには、[**表示**] &gt; [**工順のロック解除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3162-153">To unlock the route, click **View** &gt; **Unlock route**.</span></span>

## <a name="add-and-edit-formulas-and-formula-lines"></a><span data-ttu-id="d3162-154">フォーミュラとフォーミュラ明細行の追加および編集</span><span class="sxs-lookup"><span data-stu-id="d3162-154">Add and edit formulas and formula lines</span></span>
<span data-ttu-id="d3162-155">フォーミュラ明細行またはフォーミュラを編集するには、[**BOM 明細行**] または [**フォーミュラ**] 機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="d3162-155">Use the **BOM lines** or **Formula** functions to modify the formula lines or formula.</span></span> <span data-ttu-id="d3162-156">ツリー内のノードを選択すると、使用可能な機能がノード タイプによって決まります。</span><span class="sxs-lookup"><span data-stu-id="d3162-156">When you select a node in the tree, the type of the node determines the functions that are available.</span></span>

| <span data-ttu-id="d3162-157">職務</span><span class="sxs-lookup"><span data-stu-id="d3162-157">Function</span></span>                            | <span data-ttu-id="d3162-158">説明</span><span class="sxs-lookup"><span data-stu-id="d3162-158">Description</span></span>                                                                                               | <span data-ttu-id="d3162-159">ノード タイプや条件</span><span class="sxs-lookup"><span data-stu-id="d3162-159">Node type and conditions</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| <span data-ttu-id="d3162-160">[BOM 明細行] &gt; [編集]</span><span class="sxs-lookup"><span data-stu-id="d3162-160">BOM lines &gt; Edit</span></span>                 | <span data-ttu-id="d3162-161">フォーミュラ明細行の属性を編集できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3162-161">Open a dialog box where you can edit the formula line attributes.</span></span>                                         | <span data-ttu-id="d3162-162">この機能は、フォーミュラ明細行ノードが選択されている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-162">This function is available when a formula line node is selected.</span></span> |
| <span data-ttu-id="d3162-163">[BOM 明細行] &gt; [削除]</span><span class="sxs-lookup"><span data-stu-id="d3162-163">BOM lines &gt; Delete</span></span>               | <span data-ttu-id="d3162-164">選択したフォーミュラのフォーミュラ明細行を削除します。</span><span class="sxs-lookup"><span data-stu-id="d3162-164">Delete a formula line from the selected formula.</span></span>                                                          | <span data-ttu-id="d3162-165">この機能は、フォーミュラ明細行ノードが選択され、フォーミュラが編集用にロックされていない場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-165">This function is available when a formula line node is selected, and the formula isn't locked for editing.</span></span> |
| <span data-ttu-id="d3162-166">[BOM 明細行] &gt; [行の前に追加]</span><span class="sxs-lookup"><span data-stu-id="d3162-166">BOM lines &gt; Add before line</span></span>      | <span data-ttu-id="d3162-167">選択したフォーミュラ明細行の前に含める製品バリアントを選択できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3162-167">Open a dialog box where you can select a product variant to include before the selected formula line.</span></span>     | <span data-ttu-id="d3162-168">この機能は、フォーミュラ明細行ノードが選択されている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-168">This function is available when a formula line node is selected.</span></span> |
| <span data-ttu-id="d3162-169">[BOM 明細行] &gt; [コンポーネント BOM に追加]</span><span class="sxs-lookup"><span data-stu-id="d3162-169">BOM lines &gt; Add to component BOM</span></span> | <span data-ttu-id="d3162-170">選択したフォーミュラの最後に含める製品バリアントを選択できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3162-170">Open a dialog box where you can select a product variant to include at the end of the selected formula.</span></span>   | <span data-ttu-id="d3162-171">この機能は、選択されているノードに選択されたフォーミュラがある場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-171">This function is available when the node that is selected has a selected formula.</span></span> <span data-ttu-id="d3162-172">この機能を使用できない場合は、選択した品目バリアントにフォーミュラ バージョンが存在しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3162-172">If this function isn't available, a formula version might be missing for the selected item variant.</span></span> <span data-ttu-id="d3162-173">この場合、選択したノードの欠落しているバージョンを作成するには [**フォーミュラ**] &gt; [**バージョンの作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3162-173">In this case, you can click **Formula** &gt; **Create version** to create the missing version for the selected node.</span></span> |
| <span data-ttu-id="d3162-174">[BOM 明細行] &gt; [行の後に追加]</span><span class="sxs-lookup"><span data-stu-id="d3162-174">BOM lines &gt; Add after line</span></span>       | <span data-ttu-id="d3162-175">選択したフォーミュラ明細行の後ろに含める製品バリアントを選択できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3162-175">Open a dialog box where you can select a product variant to include after the selected formula line.</span></span>      | <span data-ttu-id="d3162-176">この機能は、フォーミュラ明細行ノードが選択されている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-176">This function is available when a formula line node is selected.</span></span> |
| <span data-ttu-id="d3162-177">[フォーミュラ] &gt; [バージョンの作成]</span><span class="sxs-lookup"><span data-stu-id="d3162-177">Formula &gt; Create version</span></span>         | <span data-ttu-id="d3162-178">選択したノードの製品バリアントの新しいフォーミュラ バージョンまたはフォーミュラを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3162-178">Create a new formula version or formula for the product variant of the selected node.</span></span>                     | <span data-ttu-id="d3162-179">この機能は、選択したフォーミュラ明細行ノードが、生産タイプが [**BOM**] または [**フォーミュラ**] である品目にリンクされている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-179">This function is available when the formula line node that is selected is linked to an item that has a production type of **BOM** or **Formula**.</span></span> |
| <span data-ttu-id="d3162-180">[フォーミュラ] &gt; [計算]</span><span class="sxs-lookup"><span data-stu-id="d3162-180">Formula &gt; Calculation</span></span>            | <span data-ttu-id="d3162-181">選択した製品バリアントの原価または販売価格の計算を実行できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3162-181">Open a dialog box where you can run the cost or sales price calculation for the selected product variant.</span></span> | <span data-ttu-id="d3162-182">この機能は、選択されているノードがフォーミュラ バージョンに関連付けらている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-182">This function is available when the node that is selected is related to a formula version.</span></span> |
| <span data-ttu-id="d3162-183">[フォーミュラ] &gt; [確認]</span><span class="sxs-lookup"><span data-stu-id="d3162-183">Formula &gt; Check</span></span>                  | <span data-ttu-id="d3162-184">選択したフォーミュラを検証し、確認します。</span><span class="sxs-lookup"><span data-stu-id="d3162-184">Validate and check the selected formula.</span></span>                                                                  | <span data-ttu-id="d3162-185">この機能は、選択されているノードがフォーミュラ バージョンに関連付けらている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3162-185">This function is available when the node that is selected is related to a formula version.</span></span> |

## <a name="configuring-the-tree-view"></a><span data-ttu-id="d3162-186">ツリー ビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d3162-186">Configuring the tree view</span></span>
<span data-ttu-id="d3162-187">[**設定**] をクリックすると、[フォーミュラ デザイナー] のツリー ビューに表示される情報をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="d3162-187">Click **Setup** to customize the information that is shown in the tree view of the formula designer.</span></span>

| <span data-ttu-id="d3162-188">フィールド グループ</span><span class="sxs-lookup"><span data-stu-id="d3162-188">Field group</span></span> | <span data-ttu-id="d3162-189">説明</span><span class="sxs-lookup"><span data-stu-id="d3162-189">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="d3162-190">BOM</span><span class="sxs-lookup"><span data-stu-id="d3162-190">BOM</span></span>         | <span data-ttu-id="d3162-191">ツリー構造に表示された基準を選択するには、このチェック ボックスを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3162-191">Use the check boxes to select the criteria that are shown in the tree structure.</span></span> <span data-ttu-id="d3162-192">選択した基準は、フォーミュラ デザイナーの両方のタブの下部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3162-192">The formula designer shows the selected criteria at the bottom of both tabs.</span></span> |
| <span data-ttu-id="d3162-193">工順</span><span class="sxs-lookup"><span data-stu-id="d3162-193">Route</span></span>       | <span data-ttu-id="d3162-194">表示された工順の基準を選択するには、このチェック ボックスを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3162-194">Use the check boxes to select the criteria that are shown for the routes.</span></span> |

