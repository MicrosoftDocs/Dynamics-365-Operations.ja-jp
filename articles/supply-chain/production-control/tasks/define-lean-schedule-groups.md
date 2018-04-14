--- 
title: "リーン スケジュール グループの定義"
description: "リーン スケジュール グループは、かんばんスケジューリングの製品をグループ化して区別するために定義されます。"
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 50435f858524013c3b0e67939bd29ab18b4272b0
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="bba7c-103">リーン スケジュール グループの定義</span><span class="sxs-lookup"><span data-stu-id="bba7c-103">Define lean schedule groups</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bba7c-104">リーン スケジュール グループは、かんばんスケジューリングの製品をグループ化して区別するために定義されます。</span><span class="sxs-lookup"><span data-stu-id="bba7c-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="bba7c-105">グループ化は、会社ごとの一般的な関連として、または作業セル特定としてできます。</span><span class="sxs-lookup"><span data-stu-id="bba7c-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="bba7c-106">各グループには、かんばんスケジューリング リストページでの視覚的表示のため、割り当てられた色コードがあります。</span><span class="sxs-lookup"><span data-stu-id="bba7c-106">Each group has a color code assigned for visual indication in the kanban scheduling list page.</span></span> <span data-ttu-id="bba7c-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="bba7c-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="bba7c-108">リーン スケジューリング グループの定義</span><span class="sxs-lookup"><span data-stu-id="bba7c-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="bba7c-109">[製品情報管理] > [リーン生産] > [リーン スケジュール グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="bba7c-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="bba7c-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bba7c-110">Click New.</span></span>
3. <span data-ttu-id="bba7c-111">[スケジュール グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bba7c-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="bba7c-112">スケジュール グループは、グローバル グループとして、または作業セルを固有に定義できます。</span><span class="sxs-lookup"><span data-stu-id="bba7c-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="bba7c-113">この単純な例では、グローバル グループを定義し、作業セルは空白になります。</span><span class="sxs-lookup"><span data-stu-id="bba7c-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="bba7c-114">このグループの設定は、特定のスケジュール グループがないすべての作業セルに適用されます。</span><span class="sxs-lookup"><span data-stu-id="bba7c-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="bba7c-115">色セレクションから色を選択します。</span><span class="sxs-lookup"><span data-stu-id="bba7c-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="bba7c-116">かんばんスケジュールのリスト ページまたはかんばんプロセス ボードのジョブを強調表示するため、色が使用されます。</span><span class="sxs-lookup"><span data-stu-id="bba7c-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="bba7c-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="bba7c-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="bba7c-118">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bba7c-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="bba7c-119">製品の関連付け</span><span class="sxs-lookup"><span data-stu-id="bba7c-119">Associate product</span></span>
1. <span data-ttu-id="bba7c-120">特定の製品を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="bba7c-120">Associate a specific product</span></span>
    * <span data-ttu-id="bba7c-121">製品をリーン スケジュール グループに関連付けるには、特定の製品として(商品関係タイプ = 品目) または、品目配賦キーの一部として(商品関係タイプ = グループ) のいずれか 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="bba7c-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="bba7c-122">[商品関係タイプ] フィールドで、品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="bba7c-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="bba7c-123">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bba7c-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="bba7c-124">[スループットの比率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bba7c-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="bba7c-125">既定のスループットの比率は 1 です。つまり、関連する製品は、生産フローのプロセス活動で指定されたのと同じ能力を消費することを意味します。</span><span class="sxs-lookup"><span data-stu-id="bba7c-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activities of the production flows.</span></span> <span data-ttu-id="bba7c-126">スループットの比率 > 1 はより高いリソース消費を定義し、スループットの比率 < 1 はより低いリソース消費を定義します。</span><span class="sxs-lookup"><span data-stu-id="bba7c-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="bba7c-127">この比率は原価計算とかんばん作業消費の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="bba7c-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="bba7c-128">品目配賦キーの関連付け</span><span class="sxs-lookup"><span data-stu-id="bba7c-128">Associate item allocation key</span></span>
1. <span data-ttu-id="bba7c-129">品目配賦キーの関連付け</span><span class="sxs-lookup"><span data-stu-id="bba7c-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="bba7c-130">[品目関係タイプ] グループを使用して、品目配賦キーにアソシエーションを追加します。</span><span class="sxs-lookup"><span data-stu-id="bba7c-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="bba7c-131">このプロセスには、データで定義された予測の品目配賦キーが必要なことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="bba7c-131">Note that for this process, you need a forecast item allocation key defined in your data.</span></span>  
2. <span data-ttu-id="bba7c-132">[商品関係タイプ] フィールドで、グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="bba7c-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="bba7c-133">[品目配賦キー] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bba7c-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bba7c-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bba7c-134">In the list, click the link in the selected row.</span></span>


