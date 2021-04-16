---
title: 製造品目の標準原価を管理するための準備
description: このトピックでは、製造品目の原価の管理を準備するステップについて説明します。
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6944782ac236a3f414b1cadfb12b0f0d8c1115b9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821516"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="3460b-103">製造品目の標準原価を管理するための準備</span><span class="sxs-lookup"><span data-stu-id="3460b-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3460b-104">このトピックでは、製造品目の原価の管理を準備するステップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3460b-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="3460b-105">製造品目のステップは、購入品目のステップからわずかに異なっています。</span><span class="sxs-lookup"><span data-stu-id="3460b-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="3460b-106">製造品目に割り当てられているポリシーは、親製造品目の原価計算に影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3460b-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="3460b-107">製造品目の原価の管理を準備するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3460b-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="3460b-108">製造品目に品目モデル グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3460b-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="3460b-109">品目モデル グループは、標準原価が使用されることを示します。</span><span class="sxs-lookup"><span data-stu-id="3460b-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="3460b-110">製造品目に品目グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3460b-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="3460b-111">品目グループには、製造品目に適用する勘定科目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3460b-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="3460b-112">標準原価在庫モデルを持つ製造品目の勘定科目には、複数の製造差異、原価変更差額、および在庫原価再評価が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3460b-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="3460b-113">品目に在庫単位を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3460b-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="3460b-114">品目の原価は、常に品目の在庫単位で表現されます。</span><span class="sxs-lookup"><span data-stu-id="3460b-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="3460b-115">原価グループは、品目を購入品目として扱わない場合、製造品目に割り当てないでください。</span><span class="sxs-lookup"><span data-stu-id="3460b-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="3460b-116">部品表 (BOM) 計算グループを製造品目に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3460b-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="3460b-117">品目の BOM 計算グループは、適用する警告条件を定義します。</span><span class="sxs-lookup"><span data-stu-id="3460b-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="3460b-118">これにより、BOM 計算が行われた時に、計算エラーの考えられる原因についての警告メッセージが生成されるようになります。</span><span class="sxs-lookup"><span data-stu-id="3460b-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="3460b-119">たとえば、有効な BOM または工順が存在しないときに、警告メッセージでそれを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="3460b-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="3460b-120">BOM 計算グループには、製造品目をいつ購入品目として扱うかを示す展開停止ポリシーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3460b-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="3460b-121">製造品目に固定費がある場合は、標準注文数量を製造品目に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3460b-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="3460b-122">標準注文数量は、固定費を償却する際の会計ロット サイズです。</span><span class="sxs-lookup"><span data-stu-id="3460b-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="3460b-123">固定費には、工順操作での設定回数および BOM の固定コンポーネントの数量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3460b-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="3460b-124">製造品目の BOM を定義します。</span><span class="sxs-lookup"><span data-stu-id="3460b-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="3460b-125">1 つまたは複数の BOM バージョンを、1 つの製造品目に対して定義できます。</span><span class="sxs-lookup"><span data-stu-id="3460b-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="3460b-126">必要なバージョンが承認済みで有効と指定され、そのバージョンに適切な有効日が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3460b-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="3460b-127">BOM バージョンは、会社全体またはサイト固有のどちらでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="3460b-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="3460b-128">製造品目の工順を定義します。</span><span class="sxs-lookup"><span data-stu-id="3460b-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="3460b-129">1 つまたは複数の工順バージョンを、1 つの製造品目に対して定義できます。</span><span class="sxs-lookup"><span data-stu-id="3460b-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="3460b-130">必要なバージョンが承認済みで有効と指定され、そのバージョンに適切な有効日が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3460b-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="3460b-131">工順バージョンは、サイト固有である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3460b-131">The route version must be site-specific.</span></span>

<span data-ttu-id="3460b-132">原価計算のために工順情報を使用したい場合は、追加の準備手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="3460b-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="3460b-133">たとえば、工順操作には正確で完全な原価カテゴリを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3460b-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="3460b-134">関連トピック</span><span class="sxs-lookup"><span data-stu-id="3460b-134">Related topics</span></span>
--------

[<span data-ttu-id="3460b-135">製造品目の固定費の償却</span><span class="sxs-lookup"><span data-stu-id="3460b-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="3460b-136">生産または調達する製品を設定する</span><span class="sxs-lookup"><span data-stu-id="3460b-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]