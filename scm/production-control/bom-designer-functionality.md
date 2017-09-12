---
title: "BOM デザイナーの機能"
description: "この記事は、 [BOM デザイナ] ページを使用して、部品表 (BOM) のツリー構造の設計および操作をする方法について説明します。 [設定] をクリックすると、さまざまなコンフィギュレーションの選択や、ツリーの行に表示する情報の指定ができます。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesigner
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 011e8220e155a5202b7b0a18bbfa9581826645d0
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="bom-designer-functionality"></a><span data-ttu-id="2781f-104">BOM デザイナーの機能</span><span class="sxs-lookup"><span data-stu-id="2781f-104">BOM designer functionality</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2781f-105">この記事は、 [BOM デザイナ] ページを使用して、部品表 (BOM) のツリー構造の設計および操作をする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2781f-105">This article describes how you can use the BOM designer page to design and work with tree structures for bills of materials (BOMs).</span></span> <span data-ttu-id="2781f-106">[設定] をクリックすると、さまざまなコンフィギュレーションの選択や、ツリーの行に表示する情報の指定ができます。</span><span class="sxs-lookup"><span data-stu-id="2781f-106">You can click Setup to select different configurations and specify what information appears on the lines of the tree.</span></span>

<span data-ttu-id="2781f-107">**[リリースされた製品]** ページから **[BOM デザイナー]** ページを開くと、選択した品目、品目の既定の注文サイト、および実際の日付で有効、承認済である部品表 (BOMs) の階層が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2781f-107">When you open the **BOM designer** page from the **Released products** page, it displays the hierarchy of bills of materials (BOMs) that are active and approved for the selected item, the default order site of the item, and the actual date.</span></span>  

<span data-ttu-id="2781f-108">ビューの最初の選択内容を変更するには、**[フィルター]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2781f-108">Click **Filter** to change the initial selection in the view.</span></span> <span data-ttu-id="2781f-109">表示原則を **[選択済/有効] または [選択済]** に設定することで、ビューで使用する個々の BOM または工順バージョンを選択できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-109">By setting the display principle to **Selected/Active or Selected**, you can select individual BOM or route versions to use in the view.</span></span> <span data-ttu-id="2781f-110">[BOM デザイナー] で、表示または管理する未承認で有効でない BOM バージョンを選択できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-110">You can select non-approved and non-active BOM versions to show or maintain in the BOM designer.</span></span>  

<span data-ttu-id="2781f-111">**メモ:** BOM デザイナーを [**部品表**] リスト ページから開くと、工順情報が表示されません。</span><span class="sxs-lookup"><span data-stu-id="2781f-111">**Note:** If you open the BOM designer from the **Bills of materials** list page, it doesn't display route information.</span></span> <span data-ttu-id="2781f-112">現在のところ、BOM または工順バージョンの選択は BOM および工順バージョンのプロパティで、[BOM デザイナー]のすべてのインスタンスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="2781f-112">Currently, the selection of a BOM or route version is a property of the BOM and route version, and applies to all instances of the BOM designer.</span></span>  

<span data-ttu-id="2781f-113">次のセクションでは、[BOM デザイナー] のさまざまなタブで使用できる機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="2781f-113">The following sections describe the functionality that is available on the various tabs of the BOM designer.</span></span>

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a><span data-ttu-id="2781f-114">[BOM デザイナー] を使用して BOM 構造を分析</span><span class="sxs-lookup"><span data-stu-id="2781f-114">Analyzing a BOM structure by using the BOM designer</span></span>
<span data-ttu-id="2781f-115">[BOM デザイナー] には 2 つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="2781f-115">The BOM designer has two sections:</span></span>

-   <span data-ttu-id="2781f-116">BOM 構造のツリー ビュー。</span><span class="sxs-lookup"><span data-stu-id="2781f-116">The tree view of the BOM structure.</span></span>
-   <span data-ttu-id="2781f-117">選択したデータの詳細を示す詳細セクション。</span><span class="sxs-lookup"><span data-stu-id="2781f-117">The details section, which shows details of the selected data.</span></span> <span data-ttu-id="2781f-118">ツリー ビューのノードを選択すると、詳細セクションのクイック タブがそのノードに基づいて更新されます。</span><span class="sxs-lookup"><span data-stu-id="2781f-118">When you select a node in the tree view, the FastTabs in the details section are updated based on that node:</span></span>
    -   <span data-ttu-id="2781f-119">**[BOM明細行の詳細]** – ツリー ビューで選択した BOM 明細行の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="2781f-119">**BOM line details** – Shows the details of the BOM line that is selected in the tree view.</span></span>
    -   <span data-ttu-id="2781f-120">**[品目データ]** – 選択したノードで使用されるメインの品目または品目の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="2781f-120">**Item data** – Shows the details of the main item or the item that is used in the selected node.</span></span> <span data-ttu-id="2781f-121">選択した品目を管理するには、**[リリースされた製品の編集]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2781f-121">You can click **Edit released product** to maintain the selected item.</span></span>
    -   <span data-ttu-id="2781f-122">**[BOM]** – 選択したノードに関連付けられる BOM のヘッダーを表示します。</span><span class="sxs-lookup"><span data-stu-id="2781f-122">**BOM** – Shows the header of the BOM that is related to the selected node.</span></span>
    -   <span data-ttu-id="2781f-123">**[Route]** – 選択したノードに関連付けられる Route のヘッダーを表示します。</span><span class="sxs-lookup"><span data-stu-id="2781f-123">**Route** – Shows the header of the route that is related to the selected node.</span></span>
    -   <span data-ttu-id="2781f-124">**工順工程** –は、工順の工程のプレビューを表示します。</span><span class="sxs-lookup"><span data-stu-id="2781f-124">**Route operations** – Shows a preview of the operations for the route.</span></span> <span data-ttu-id="2781f-125">特定の工程に割り当てられる BOM 明細行が選択されている場合、工程は **[工程のコンフィギュレーションの準備]** としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="2781f-125">When a BOM line that is assigned to a specific operation is selected, the operation is marked as **Component needed at operations**.</span></span>

## <a name="selecting-a-bom-and-route"></a><span data-ttu-id="2781f-126">BOM と工順の選択</span><span class="sxs-lookup"><span data-stu-id="2781f-126">Selecting a BOM and route</span></span>
<span data-ttu-id="2781f-127">BOM および工順に適用されるフィルタは、[BOM デザイナー] のヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2781f-127">The filter that is applied for the BOM and route is displayed in the header of the BOM designer.</span></span> <span data-ttu-id="2781f-128">**[フィルタ]** ダイアログ ボックスを使用してフィルタを変更できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-128">You can change the filter by using the **Filter** dialog box.</span></span> <span data-ttu-id="2781f-129">次の表は、このダイアログ ボックスのフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="2781f-129">The following table describes the fields in this dialog box.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2781f-130">フィールド</span><span class="sxs-lookup"><span data-stu-id="2781f-130">Field</span></span></th>
<th><span data-ttu-id="2781f-131">説明</span><span class="sxs-lookup"><span data-stu-id="2781f-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2781f-132">製品分析コード</span><span class="sxs-lookup"><span data-stu-id="2781f-132">Product dimensions</span></span></td>
<td><span data-ttu-id="2781f-133">選択した完成品が製品マスターの場合、主要な選択の有効な製品分析コードを定義できます。<strong>メモ:</strong> 製品マスターではない製品の [BOM デザイナー] を開くと、製品分析コードは <strong>[フィルタ]</strong> ダイアログ ボックスで選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="2781f-133">If the selected finished product is a product master, you can define the active product dimensions for the main selection.<strong>Note:</strong> If you open the BOM designer for a product that isn't a product master, no product dimensions can be selected in the <strong>Filter</strong> dialog box.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2781f-134">サービス拠点</span><span class="sxs-lookup"><span data-stu-id="2781f-134">Site</span></span></td>
<td><span data-ttu-id="2781f-135">BOM ツリーが表示されるサイトを変更します。</span><span class="sxs-lookup"><span data-stu-id="2781f-135">Change the site that the BOM tree is displayed for.</span></span> <span data-ttu-id="2781f-136">既定のサイトは、完成品目の既定の在庫サイトです。</span><span class="sxs-lookup"><span data-stu-id="2781f-136">The default site is the default inventory site of the finished item.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2781f-137">表示原則</span><span class="sxs-lookup"><span data-stu-id="2781f-137">Display principle</span></span></td>
<td><span data-ttu-id="2781f-138">現在の BOM 構造と現在の工順に適用されるバージョン表示原則を選択します。</span><span class="sxs-lookup"><span data-stu-id="2781f-138">Select the version display principle that applies to the current BOM structure and the current route:</span></span>
<ul>
<li><span data-ttu-id="2781f-139">表示原則が <strong>[有効] または [選択済/有効]</strong> に設定されている場合、この日付の有効な BOM または工順のバージョンが検出されます。</span><span class="sxs-lookup"><span data-stu-id="2781f-139">When the principle is set to <strong>Active or Selected/Active</strong>, the valid BOM or route version for this date is found.</span></span></li>
<li><span data-ttu-id="2781f-140">原則が <strong>[選択済/有効] または [選択済]</strong> に設定されている場合、[<strong>BOM</strong>] &gt; [<strong>BOM バージョン</strong>] または [<strong>工順</strong>] &gt; [<strong>工順バージョン</strong>] をクリックして BOM バージョンまたは工順バージョンを選択できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-140">When the principle is set to <strong>Selected/Active or Selected</strong>, you can select a BOM version or route version by clicking <strong>BOM</strong> &gt; <strong>BOM versions</strong> or <strong>Route</strong> &gt; <strong>Route versions</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2781f-141">バージョン日付</span><span class="sxs-lookup"><span data-stu-id="2781f-141">Version date</span></span></td>
<td><span data-ttu-id="2781f-142">BOM および工順のバージョン日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="2781f-142">Enter the version date for the BOM and route.</span></span> <span data-ttu-id="2781f-143">このバージョンは、特定の日付 (BOM バージョン設定におけるバージョン日付) に使用される BOM バージョンを識別します。</span><span class="sxs-lookup"><span data-stu-id="2781f-143">The version identifies which BOM version is used on a specific date, as determined by the version dates in the BOM version setup.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2781f-144">開始数量</span><span class="sxs-lookup"><span data-stu-id="2781f-144">From quantity</span></span></td>
<td><span data-ttu-id="2781f-145">数量から固有を選択してバージョンをフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="2781f-145">Filter the versions by selecting a specific from quantity.</span></span> <span data-ttu-id="2781f-146">値を設定すると、別の BOM および工順バージョンが選択されることがあります。</span><span class="sxs-lookup"><span data-stu-id="2781f-146">If you set a value, different BOM and route versions might be selected.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2781f-147">有効のみを表示</span><span class="sxs-lookup"><span data-stu-id="2781f-147">Show valid only</span></span></td>
<td><span data-ttu-id="2781f-148">このチェック ボックスを選択すると、有効な日付を持つ BOM 明細行のみがツリー構造に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2781f-148">When you select the check box, the tree structure shows only BOM lines that have valid dates.</span></span> <span data-ttu-id="2781f-149">BOM 明細行を右クリックまたはダブルクリックして [<strong>BOM 明細行の編集</strong>] ページを開くと、その BOM 明細行の有効期間を確認できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-149">Right-click or double-click a BOM line to open the <strong>Edit BOM line</strong> page, where you can see the validity dates for that BOM line.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2781f-150">[BOM デザイナー] を使用して 1 つ以上のファントムのレベルで構成される BOM を確認または編集すると、上位品目と関連付けられる工順は通常、BOM 階層全体に及びます。</span><span class="sxs-lookup"><span data-stu-id="2781f-150">When you use the BOM designer to review or edit BOMs that consist of one or more levels of phantoms, the route that is associated with the top item typically spans the complete BOM hierarchy.</span></span> <span data-ttu-id="2781f-151">概要を簡略化するために、[**表示**] &gt; [**工順のロック**] をクリックして表示に含まれるトップレベルの工順をロックできます。</span><span class="sxs-lookup"><span data-stu-id="2781f-151">To simplify the overview, you can lock the top-level route in the display by clicking **View** &gt; **Lock route**.</span></span> <span data-ttu-id="2781f-152">工順のロックを解除するには、[**表示**] &gt; [**工順のロック解除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2781f-152">To unlock the route, click **View** &gt; **Unlock route**.</span></span>

## <a name="adding-and-editing-boms-and-bom-lines"></a><span data-ttu-id="2781f-153">BOM および BOM 明細行を追加および編集</span><span class="sxs-lookup"><span data-stu-id="2781f-153">Adding and editing BOMs and BOM lines</span></span>
<span data-ttu-id="2781f-154">BOM 明細行または BOM を編集するには、[**BOM 明細行**] または [**BOM**] 機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="2781f-154">Use the **BOM lines** or **BOM** functions to modify the BOM lines or BOM.</span></span> <span data-ttu-id="2781f-155">ツリー内のノードを選択すると、使用可能な機能がノード タイプによって決まります。</span><span class="sxs-lookup"><span data-stu-id="2781f-155">When you select a node in the tree, the type of the node determines that functions that are available.</span></span>

| <span data-ttu-id="2781f-156">職務</span><span class="sxs-lookup"><span data-stu-id="2781f-156">Function</span></span>                            | <span data-ttu-id="2781f-157">説明</span><span class="sxs-lookup"><span data-stu-id="2781f-157">Description</span></span>                                                                                               | <span data-ttu-id="2781f-158">ノード タイプや条件</span><span class="sxs-lookup"><span data-stu-id="2781f-158">Node type and conditions</span></span>                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2781f-159">[BOM 明細行] &gt; [編集]</span><span class="sxs-lookup"><span data-stu-id="2781f-159">BOM lines &gt; Edit</span></span>                 | <span data-ttu-id="2781f-160">BOM 明細行の属性を編集できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="2781f-160">Open a dialog box where you can edit the BOM line attributes.</span></span>                                             | <span data-ttu-id="2781f-161">この機能は、BOM 明細行ノードが選択されている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-161">This function is available when a BOM line node is selected.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="2781f-162">[BOM 明細行] &gt; [削除]</span><span class="sxs-lookup"><span data-stu-id="2781f-162">BOM lines &gt; Delete</span></span>               | <span data-ttu-id="2781f-163">選択された BOM から BOM 明細行を削除</span><span class="sxs-lookup"><span data-stu-id="2781f-163">Delete a BOM line from the selected BOM.</span></span>                                                                  | <span data-ttu-id="2781f-164">この機能は、BOM 明細行ノードが選択されている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-164">This function is available when a BOM line node is selected, and the BOM isn't locked for editing.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="2781f-165">[BOM 明細行] &gt; [行の前に追加]</span><span class="sxs-lookup"><span data-stu-id="2781f-165">BOM lines &gt; Add before line</span></span>      | <span data-ttu-id="2781f-166">選択した BOM 明細行の前に含める製品バリアントを選択できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="2781f-166">Open a dialog box where you can select a product variant to include before the selected BOM line.</span></span>         | <span data-ttu-id="2781f-167">この機能は、BOM 明細行ノードが選択されている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-167">This function is available when a BOM line node is selected.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="2781f-168">[BOM 明細行] &gt; [コンポーネント BOM に追加]</span><span class="sxs-lookup"><span data-stu-id="2781f-168">BOM lines &gt; Add to component BOM</span></span> | <span data-ttu-id="2781f-169">選択した BOM の最後に含める製品バリアントを選択できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="2781f-169">Open a dialog box where you can select a product variant to include at the end of the selected BOM.</span></span>       | <span data-ttu-id="2781f-170">この機能は、選択されているノードに選択された BOM がある場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-170">This function is available when the node that is selected has a selected BOM.</span></span> <span data-ttu-id="2781f-171">この機能を使用できない場合は、選択した品目バリアントに BOM バージョンが存在しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="2781f-171">If this function isn't available, a BOM version might be missing for the selected item variant.</span></span> <span data-ttu-id="2781f-172">この場合、選択したノードの欠落しているバージョンを作成するには [**BOM**] &gt; [**バージョンの作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2781f-172">In this case, you can click **BOM** &gt; **Create version** to create the missing version for the selected node.</span></span> |
| <span data-ttu-id="2781f-173">[BOM 明細行] &gt; [行の後に追加]</span><span class="sxs-lookup"><span data-stu-id="2781f-173">BOM lines &gt; Add after line</span></span>       | <span data-ttu-id="2781f-174">選択した BOM 明細行の後に含める製品バリアントを選択できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="2781f-174">Open a dialog box where you can select a product variant to include after the selected BOM line.</span></span>          | <span data-ttu-id="2781f-175">この機能は、BOM 明細行ノードが選択されている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-175">This function is available when a BOM line node is selected.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="2781f-176">[BOM] &gt; [バージョンの作成]</span><span class="sxs-lookup"><span data-stu-id="2781f-176">BOM &gt; Create version</span></span>             | <span data-ttu-id="2781f-177">選択したノードの製品バリアントのBOMまたはBOMバージョンを作成します。</span><span class="sxs-lookup"><span data-stu-id="2781f-177">Create a new BOM version or BOM for the product variant of the selected node.</span></span>                             | <span data-ttu-id="2781f-178">この機能は、選択した BOM 明細行ノードが生産タイプが [**BOM**] または [**フォーミュラ**] である品目にリンクされている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-178">This function is available when the BOM line node that is selected is linked to an item that has a production type of **BOM** or **Formula**.</span></span>                                                                                                                                                  |
| <span data-ttu-id="2781f-179">[BOM] &gt; [計算]</span><span class="sxs-lookup"><span data-stu-id="2781f-179">BOM &gt; Calculation</span></span>                | <span data-ttu-id="2781f-180">選択した製品バリアントの原価または販売価格の計算を実行できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="2781f-180">Open a dialog box where you can run the cost or sales price calculation for the selected product variant.</span></span> | <span data-ttu-id="2781f-181">この機能は、選択されているノードが BOM バージョンに関連付けらている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-181">This function is available when the node that is selected is related to a BOM version.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="2781f-182">[BOM] &gt; [確認]</span><span class="sxs-lookup"><span data-stu-id="2781f-182">BOM &gt; Check</span></span>                      | <span data-ttu-id="2781f-183">選択したBOMを検証し、確認します。</span><span class="sxs-lookup"><span data-stu-id="2781f-183">Validate and check the selected BOM.</span></span>                                                                      | <span data-ttu-id="2781f-184">この機能は、選択されているノードが BOM バージョンに関連付けらている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2781f-184">This function is available when the node that is selected is related to a BOM version.</span></span>                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a><span data-ttu-id="2781f-185">ツリー ビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2781f-185">Configuring the tree view</span></span>
<span data-ttu-id="2781f-186">[**設定**] をクリックすると、[BOM デザイナー] のツリー ビューに表示される情報をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="2781f-186">Click **Setup** to customize the information that is shown in the tree view of the BOM designer.</span></span>

| <span data-ttu-id="2781f-187">フィールド グループ</span><span class="sxs-lookup"><span data-stu-id="2781f-187">Field group</span></span> | <span data-ttu-id="2781f-188">説明</span><span class="sxs-lookup"><span data-stu-id="2781f-188">Description</span></span>                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2781f-189">BOM</span><span class="sxs-lookup"><span data-stu-id="2781f-189">BOM</span></span>         | <span data-ttu-id="2781f-190">ツリー構造に表示された基準を選択するには、このチェック ボックスを使用します。</span><span class="sxs-lookup"><span data-stu-id="2781f-190">Use the check boxes to select the criteria that are shown in the tree structure.</span></span> <span data-ttu-id="2781f-191">選択した基準は、[BOM デザイナー] の両方のタブの下部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2781f-191">The BOM designer displays the selected criteria at the bottom of both tabs.</span></span> |
| <span data-ttu-id="2781f-192">工順</span><span class="sxs-lookup"><span data-stu-id="2781f-192">Route</span></span>       | <span data-ttu-id="2781f-193">表示された工順の基準を選択するには、このチェック ボックスを使用します。</span><span class="sxs-lookup"><span data-stu-id="2781f-193">Use the check boxes to select the criteria that are shown for the routes.</span></span>                                                                                    |






