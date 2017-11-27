---
title: "標準原価換算の前提条件"
description: "このトピックでは、標準コスト換算を実行する前に実行するタスクについて説明します。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 65844bd78363dc6638b16b3fd4ca163a3fde6a23
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="prerequisites-for-a-standard-cost-conversion"></a><span data-ttu-id="70715-103">標準原価換算の前提条件</span><span class="sxs-lookup"><span data-stu-id="70715-103">Prerequisites for a standard cost conversion</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="70715-104">このトピックでは、標準コスト換算を実行する前に実行するタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="70715-104">This topic discusses tasks to perform before you run a standard cost conversion.</span></span> 

<span data-ttu-id="70715-105">標準原価換算を実行する前に、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="70715-105">Before you run a standard cost conversion, follow these steps:</span></span>

1.  <span data-ttu-id="70715-106">標準原価用の**品目モデル グループ**を定義します。</span><span class="sxs-lookup"><span data-stu-id="70715-106">Define an **item model group** for standard costs.</span></span> <span data-ttu-id="70715-107">[品目モデル グループ] ページを使用して、標準原価在庫モデルを持つ品目モデル グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="70715-107">Use the Item model groups page to create an item model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="70715-108">標準コスト換算の設定時に、変換する品目にこの品目モデル グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="70715-108">When setting up a standard cost conversion, you assign this item model group to the items that are being converted.</span></span>
2.  <span data-ttu-id="70715-109">各品目に**原価グループ**を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="70715-109">Assign a **cost group** to each item.</span></span>
    -   <span data-ttu-id="70715-110">購入品目に割り当てられたコスト グループは、標準コストに関連する勘定科目を割り当てるための基準として使用できます。</span><span class="sxs-lookup"><span data-stu-id="70715-110">The cost group that is assigned to a purchased item can act as the basis for assigning ledger accounts that are related to standard costs.</span></span> <span data-ttu-id="70715-111">これには購買価格差異への勘定科目の割り当てが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="70715-111">This can include assigning ledger accounts for purchase price variances.</span></span> <span data-ttu-id="70715-112">製造環境では、購入コンポーネントに割り当てられた原価グループは、製造品目の算出原価における原価区分の基準にもなります。</span><span class="sxs-lookup"><span data-stu-id="70715-112">In a manufacturing environment, the cost group that is assigned to purchased components also provides cost segmentation in the calculated costs of a manufactured item.</span></span>
    -   <span data-ttu-id="70715-113">製造品目に割り当てられた原価グループは、標準原価に関連する勘定科目を割り当てるための基準として使用できます (製造差異に勘定科目を割り当てるときなど)。</span><span class="sxs-lookup"><span data-stu-id="70715-113">The cost group that is assigned to a manufactured item can act as the basis for assigning ledger accounts that are related to standard costs, such as assigning ledger accounts for production variances.</span></span>

3.  <span data-ttu-id="70715-114">製造品目に固定費がある場合は、**標準注文数量**を製造品目に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="70715-114">Assign a **standard order quantity** to a manufactured item when it has constant costs.</span></span> <span data-ttu-id="70715-115">製造品目の標準注文数量は、固定費の償却、または比例配分の会計ロット サイズの役目をします。</span><span class="sxs-lookup"><span data-stu-id="70715-115">The standard order quantity for a manufactured item acts as an accounting lot size for amortizing, or prorating, constant costs.</span></span> <span data-ttu-id="70715-116">これには、工順操作での設定回数や部品表 (BOM) の固定コンポーネントの数量が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="70715-116">These can include setup times in routing operations or a constant component quantity in a bill of material (BOM).</span></span>
4.  <span data-ttu-id="70715-117">標準原価 (特に再評価差異) に関連する**総勘定元帳勘定**を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="70715-117">Assign **general ledger accounts** that are related to standard costs, especially the revaluation variance.</span></span> <span data-ttu-id="70715-118">標準コストに関連する総勘定元帳の勘定を割り当てるために、[**転記**] ページ (**在庫管理**&gt;**設定**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="70715-118">Use the **Posting** page (**Inventory management** &gt; **Setup**) to assign general ledger accounts that are related to standard costs.</span></span> <span data-ttu-id="70715-119">標準原価換算プロセスのためには、少なくともすべての品目および原価グループの再評価差異に対して勘定を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="70715-119">As a minimum for the standard cost conversion process, you must assign the account for the revaluation variance for all items and all cost groups.</span></span> <span data-ttu-id="70715-120">**勘定科目表**ページを使用して、標準原価に必要な総勘定元帳を定義します。</span><span class="sxs-lookup"><span data-stu-id="70715-120">Use the **Chart of accounts** page to define the general ledger accounts that will be needed for standard costs.</span></span> <span data-ttu-id="70715-121">**トランザクションの組み合わせ**ページを使用して、品目転記ルールを定義する前に、(テーブル、グループ、およびすべてに対する) 原価関係を有効にします。</span><span class="sxs-lookup"><span data-stu-id="70715-121">Use the **Transaction combinations** page to enable cost relations (for tables, groups, and all) before you define the item posting rules.</span></span>
5.  <span data-ttu-id="70715-122">標準原価に関連する在庫パラメータを定義します。</span><span class="sxs-lookup"><span data-stu-id="70715-122">Define the inventory parameters that are related to standard costs.</span></span> <span data-ttu-id="70715-123">**在庫および倉庫管理パラメーター** ページの**番号順序**タブを使用して、再評価伝票に番号順序を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="70715-123">Use the **Number sequences** tab on the **Inventory and warehouse management parameters** page to assign a number sequence to revaluation vouchers.</span></span> <span data-ttu-id="70715-124">再評価伝票は、標準コスト換算によって品目の在庫金額が変更されると生成されます。</span><span class="sxs-lookup"><span data-stu-id="70715-124">A revaluation voucher is generated when the standard cost conversion creates a change of an item's inventory value.</span></span> <span data-ttu-id="70715-125">**在庫および倉庫管理パラメーター** ページを使用して、[原価管理] パラメーター (**在庫会計**タブ) を定義して、2 つのパラメーターが標準原価に関連するように定義します。</span><span class="sxs-lookup"><span data-stu-id="70715-125">Use the **Inventory and warehouse management parameters** page to define Cost Control parameters (on the **Inventory accounting** tab) to define two parameters that are related to standard costs.</span></span>
    -   <span data-ttu-id="70715-126">**原価内訳**フィールドを使用して、[なし] または [補助元帳] を選択します。</span><span class="sxs-lookup"><span data-stu-id="70715-126">Use the **Cost breakdown** field to select No or Sub ledger.</span></span> <span data-ttu-id="70715-127">[補助元帳] の選択は、有効な原価内訳とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="70715-127">The selection of Sub ledger is termed an active cost breakdown.</span></span> <span data-ttu-id="70715-128">有効なコスト内訳は、標準コスト品目の複数レベルの製品構成全体で、コスト グループ セグメントを計算、保持、および表示するためにとても重要です。</span><span class="sxs-lookup"><span data-stu-id="70715-128">An active cost breakdown is very important for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="70715-129">コスト内訳が有効な場合、単一レベル、複数レベル、または合計形式で以下のレポートおよび分析ができます。</span><span class="sxs-lookup"><span data-stu-id="70715-129">When the cost breakdown is active, you can report and analyze the following in a single level, multi-level, or total format:</span></span>
        1.  <span data-ttu-id="70715-130">在庫</span><span class="sxs-lookup"><span data-stu-id="70715-130">Inventory</span></span>
        2.  <span data-ttu-id="70715-131">仕掛品 (WIP)</span><span class="sxs-lookup"><span data-stu-id="70715-131">Work in process (WIP)</span></span>
        3.  <span data-ttu-id="70715-132">コスト グループごとの売却済商品の原価 (COGS)</span><span class="sxs-lookup"><span data-stu-id="70715-132">Cost of goods sold (COGS) per cost group</span></span>

        <span data-ttu-id="70715-133">有効なコスト内訳は、製造品目のコストを有効にすると、品目のコスト レコードの中にコスト グループ セグメントが保存されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="70715-133">An active cost breakdown means that if you enable a manufactured item's cost, the result will be stored in the cost group segmentation in the item's cost record.</span></span> <span data-ttu-id="70715-134">**原価内訳**フィールドに値を入力しない場合、標準コスト品目のための原価グループ区分は維持されません。</span><span class="sxs-lookup"><span data-stu-id="70715-134">If you put no value in the **Cost breakdown** field, the cost group segmentation will not be maintained for standard cost items.</span></span> <span data-ttu-id="70715-135">つまり、製造された品目の標準原価は、原価グループ セグメントを持たない単一の金額として計算および管理され、製造後のコンポーネントの原価貢献度が、単一の金額に集計されます。</span><span class="sxs-lookup"><span data-stu-id="70715-135">That is, a manufactured item's standard cost will be calculated and maintained as a single amount without cost group segmentation, and the cost contributions of manufactured components will be aggregated into the single amount.</span></span>
    -   <span data-ttu-id="70715-136">**標準に対する差異**フィールドを使用して、集計または原価グループ別を選択します。</span><span class="sxs-lookup"><span data-stu-id="70715-136">Use the **Variances to standard** field to select summarized or per cost group.</span></span> <span data-ttu-id="70715-137">コスト グループごとに選択すると、コスト グループにより購買価格差異と製造差異を識別できます。</span><span class="sxs-lookup"><span data-stu-id="70715-137">The selection of per cost group enables you to identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="70715-138">これにより、製造差異 (ロット サイズ、数量、価格、および代替差異) の 4 種類が識別できるようになります。</span><span class="sxs-lookup"><span data-stu-id="70715-138">This also enables you to identify the four types of production variances (the lot size, quantity, price, and substitution variances).</span></span> <span data-ttu-id="70715-139">集計を選択すると、コスト グループ別の差異と、4 種類の製造差異が区別できなくなります。</span><span class="sxs-lookup"><span data-stu-id="70715-139">If you select summarized, you cannot identify variances by cost group, and you cannot identify the four types of production variances.</span></span> <span data-ttu-id="70715-140">確認できるのは、集計された製造差異だけとなります。</span><span class="sxs-lookup"><span data-stu-id="70715-140">You can only view a summarized production variance.</span></span> <span data-ttu-id="70715-141">標準に対する差異に関するポリシーは、コスト内訳ポリシーから独立しています。</span><span class="sxs-lookup"><span data-stu-id="70715-141">The policy about variance to standard is independent of the cost breakdown policy.</span></span> <span data-ttu-id="70715-142">つまり、原価計算ポリシーを選択しなくても、原価グループ別の差異を選択することで、原価グループ別の製造差異を把握できます。</span><span class="sxs-lookup"><span data-stu-id="70715-142">That is, you can select a cost breakdown policy of none, and select variances per cost group, so that production variances by cost group will still be captured.</span></span>






