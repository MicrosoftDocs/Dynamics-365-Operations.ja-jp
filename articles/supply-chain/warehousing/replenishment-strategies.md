---
title: 補充戦略
description: このトピックでは、補充戦略に関する情報を提供し、[補充戦略] フィールドを使用して補充の実行方法を選択する方法について説明します。
author: mirzaab
manager: tfehr
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: a66d48c6636f9f2012c92945868728d8430c1cbe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256042"
---
# <a name="replenishment-strategies"></a><span data-ttu-id="756b4-103">補充戦略</span><span class="sxs-lookup"><span data-stu-id="756b4-103">Replenishment strategies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="756b4-104">**補充テンプレート** ページで定義されているテンプレートには、補充の実行方法を選択できる、ウェーブ需要補充テンプレートの行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="756b4-104">The templates that are defined on the **Replenishment templates** page include wave demand replenishment template lines that let you select how replenishment is done.</span></span> <span data-ttu-id="756b4-105">各行に **補充戦略** フィールドが含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="756b4-105">Each line now includes a **Replenishment strategy** field.</span></span>

<span data-ttu-id="756b4-106">*ウェーブ需要数量* 戦略は、既定の戦略です。</span><span class="sxs-lookup"><span data-stu-id="756b4-106">The *Wave demand quantity* strategy is the default strategy.</span></span> <span data-ttu-id="756b4-107">**補充戦略** フィールドの導入前に使用されていた補充戦略です。</span><span class="sxs-lookup"><span data-stu-id="756b4-107">It's the replenishment strategy that was used before the introduction of the **Replenishment strategy** field.</span></span> <span data-ttu-id="756b4-108">補充場所ディレクティブを使用して補充可能な場所を検索します。</span><span class="sxs-lookup"><span data-stu-id="756b4-108">It uses the replenishment location directives to find locations that can be replenished.</span></span> <span data-ttu-id="756b4-109">次に、需要がカバーされるまでこれらの場所を補充します。</span><span class="sxs-lookup"><span data-stu-id="756b4-109">It then replenishes those locations until the demand is covered.</span></span>

<span data-ttu-id="756b4-110">*場所の最大キャパシティ* 戦略には、いくつかの新しい機能が導入されています。</span><span class="sxs-lookup"><span data-stu-id="756b4-110">The *Maximum location capacity* strategy introduces some new functionality.</span></span> <span data-ttu-id="756b4-111">この戦略では、*ウェーブ需要数量* 戦略と同様に、補充場所ディレクティブを使用して補充可能な場所を検索し、需要がカバーされるまでこれらの場所を補充ます。</span><span class="sxs-lookup"><span data-stu-id="756b4-111">Like the *Wave demand quantity* strategy, this strategy uses the replenishment location directives to find locations that can be replenished, and then it replenishes those locations until the demand is covered.</span></span> <span data-ttu-id="756b4-112">これは、保管場所の在庫上限により定義されているとおり、補充されたすべての場所が最大キャパシティまで補充されるという点で、*ウェーブ需要数量* 戦略とは異なります。</span><span class="sxs-lookup"><span data-stu-id="756b4-112">It differs from the *Wave demand quantity* strategy in that all the replenished locations are replenished to their maximum capacity, as defined by the location stocking limits.</span></span> <span data-ttu-id="756b4-113">*場所の最大キャパシティ* 戦略では、補充される場所を満たすために、要求された数量に加えていくつかの追加数量を取り込む作業を作成しようとします。</span><span class="sxs-lookup"><span data-stu-id="756b4-113">The *Maximum location capacity* strategy tries to create work to bring in the requested quantity, plus some extra quantity, to fill the locations that are being replenished.</span></span> <span data-ttu-id="756b4-114">ただし、場合によっては失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="756b4-114">However, in some cases, that attempt might fail.</span></span> <span data-ttu-id="756b4-115">たとえば、バルク場所には、追加数量をカバーするのに十分な在庫がない場合があります。</span><span class="sxs-lookup"><span data-stu-id="756b4-115">For example, the bulk locations might not have enough inventory to cover the extra quantity.</span></span> <span data-ttu-id="756b4-116">このような場合、システムによって障害が検出され、回復が試行されます。</span><span class="sxs-lookup"><span data-stu-id="756b4-116">In these cases, the system detects the failure and tries to recover.</span></span>

<span data-ttu-id="756b4-117">*ウェーブ需要数量* 戦略よりも *場所の最大キャパシティ* 戦略が適している状況の一例として、ピーク時があります。</span><span class="sxs-lookup"><span data-stu-id="756b4-117">Peak season is one example of a situation where the *Maximum location capacity* strategy is preferable to the *Wave demand quantity* strategy.</span></span> <span data-ttu-id="756b4-118">ピーク時には、一部の品目が大容量で販売されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="756b4-118">During peak season, some items might be selling at high volume.</span></span> <span data-ttu-id="756b4-119">したがって、関連するピッキング場所をできる限り予防的に補充して、補充に対して作成される作業 ID の数を減らすことが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="756b4-119">Therefore, you might want to proactively replenish the relevant picking locations as much as possible, to reduce the number of work IDs that are created for replenishment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="756b4-120">*場所の最大キャパシティ* 戦略を最大限に活用するには、関連する場所の在庫上限を再定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="756b4-120">To take full advantage of the *Maximum location capacity* strategy, you must redefine the stocking limits for the relevant locations.</span></span> <span data-ttu-id="756b4-121">それ以外の場合、この戦略は、*ウェーブ需要数量* 戦略と同じように機能します。</span><span class="sxs-lookup"><span data-stu-id="756b4-121">Otherwise, this strategy works just like the *Wave demand quantity* strategy.</span></span>

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a><span data-ttu-id="756b4-122">[在庫上限に基づき最大まで補充] 機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="756b4-122">Turn on the Replenish to max based on stocking limits feature</span></span>

<span data-ttu-id="756b4-123">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="756b4-123">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="756b4-124">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、この機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="756b4-124">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of this feature and turn it on if it's required.</span></span> <span data-ttu-id="756b4-125">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="756b4-125">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="756b4-126">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="756b4-126">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="756b4-127">**機能名:** *在庫上限に基づき最大まで補充*</span><span class="sxs-lookup"><span data-stu-id="756b4-127">**Feature name:** *Replenish to max based on stocking limits*</span></span>

## <a name="set-up-replenishment-strategies"></a><span data-ttu-id="756b4-128">補充戦略のセットアップ</span><span class="sxs-lookup"><span data-stu-id="756b4-128">Set up replenishment strategies</span></span>

<span data-ttu-id="756b4-129">テンプレートにアクセスするには、**倉庫管理 \> 設定 \> 補充 \> 補充テンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="756b4-129">To access the templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span> <span data-ttu-id="756b4-130">**概要** セクションで、**補充タイプ** フィールドが *ウェーブ需要* に設定されているウェーブ補充テンプレートを選択または作成します。</span><span class="sxs-lookup"><span data-stu-id="756b4-130">In the **Overview** section, select or create a wave demand replenishment template where the **Replenishment type** field is set to *Wave demand*.</span></span> <span data-ttu-id="756b4-131">次に、**補充テンプレートの詳細** セクションで補充テンプレート明細行を設定します。</span><span class="sxs-lookup"><span data-stu-id="756b4-131">Then set up the replenishment template lines in the **Replenishment template details** section.</span></span> <span data-ttu-id="756b4-132">各明細行の **補充戦略** フィールドで、使用する補充方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="756b4-132">For each line, in the **Replenishment strategy** field, select the replenishment strategy that you want to use.</span></span>

<span data-ttu-id="756b4-133">![補充テンプレート ページ](media/ReplenTempWaveDmdMaxLocCap.png "補充テンプレート ページ")</span><span class="sxs-lookup"><span data-stu-id="756b4-133">![Replenishment templates page](media/ReplenTempWaveDmdMaxLocCap.png "Replenishment templates page")</span></span>

<span data-ttu-id="756b4-134">**補充戦略** 列がグリッドに表示されない場合、**補充テンプレートの詳細** セクションで、この機能が有効になっていることと、選択した補充テンプレートで補充タイプとして *ウェーブ需要* が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="756b4-134">If the **Replenishment strategy** column doesn't appear in the grid in the **Replenishment template details** section, make sure that the feature has been turned on, and that the selected replenishment template has a replenishment type of *Wave demand*.</span></span>

> [!NOTE]
> <span data-ttu-id="756b4-135">*ウェーブ需要数量* 戦略は、既定の戦略です。</span><span class="sxs-lookup"><span data-stu-id="756b4-135">The *Wave demand quantity* strategy is the default strategy.</span></span> <span data-ttu-id="756b4-136">したがって、代わりに、*場所の最大キャパシティ* 戦略を使用する補充テンプレート行を更新するだけで済みます。</span><span class="sxs-lookup"><span data-stu-id="756b4-136">Therefore, you just have to update the replenishment template lines where you want to use the *Maximum location capacity* strategy instead.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="756b4-137">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="756b4-137">Example scenarios</span></span>

### <a name="example-1"></a><span data-ttu-id="756b4-138">例 1</span><span class="sxs-lookup"><span data-stu-id="756b4-138">Example 1</span></span>

<span data-ttu-id="756b4-139">この例では、補充テンプレート明細行が 1 つしかない補充テンプレートは 1 つしかありません。</span><span class="sxs-lookup"><span data-stu-id="756b4-139">For this example, there is only one replenishment template that has only one replenishment template line.</span></span>

<span data-ttu-id="756b4-140">品目 A0001 130 個 に対する販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="756b4-140">You create a sales order for 130 pieces (pcs) of item A0001.</span></span> <span data-ttu-id="756b4-141">倉庫に注文をリリースする前に、次の方法で倉庫が設定されます。</span><span class="sxs-lookup"><span data-stu-id="756b4-141">Before you release the order to the warehouse, the warehouse is set up in the following way:</span></span>

- <span data-ttu-id="756b4-142">バルク場所は 1 つのみであり、利用可能な手持在庫が 500 個あります。</span><span class="sxs-lookup"><span data-stu-id="756b4-142">There is only one bulk location, and it has 500 pcs of available on-hand inventory.</span></span>
- <span data-ttu-id="756b4-143">3 つのピッキング場所があり、それぞれの在庫上限は 100 個になっています。</span><span class="sxs-lookup"><span data-stu-id="756b4-143">There are three pick locations, each of which has a stocking limit of 100 pcs.</span></span> <span data-ttu-id="756b4-144">(在庫上限は、*場所の最大キャパシティ* 戦略では必須である点に留意してください)。</span><span class="sxs-lookup"><span data-stu-id="756b4-144">(Remember that stocking limits are required for the *Maximum location capacity* strategy.)</span></span>
- <span data-ttu-id="756b4-145">補充のプット場所は、販売ピッキングの場所と同じです。</span><span class="sxs-lookup"><span data-stu-id="756b4-145">The replenishment put locations are the same as the sales pick locations.</span></span>
- <span data-ttu-id="756b4-146">補充単位はボックス (1 ボックス = 20 個) です。</span><span class="sxs-lookup"><span data-stu-id="756b4-146">The replenishment unit is a box (1 box = 20 pcs).</span></span>

<span data-ttu-id="756b4-147">注文の時点では、販売ピックの場所で次の在庫が手持在庫になります。</span><span class="sxs-lookup"><span data-stu-id="756b4-147">At the time of the order, the following inventory is on hand at the sales pick locations:</span></span>

- <span data-ttu-id="756b4-148">**Pick-001:** 20 個 (1 ボックス)</span><span class="sxs-lookup"><span data-stu-id="756b4-148">**Pick-001:** 20 pcs (1 box)</span></span>
- <span data-ttu-id="756b4-149">**Pick-002:** 0 個</span><span class="sxs-lookup"><span data-stu-id="756b4-149">**Pick-002:** 0 pcs</span></span>
- <span data-ttu-id="756b4-150">**Pick-003:** 0 個</span><span class="sxs-lookup"><span data-stu-id="756b4-150">**Pick-003:** 0 pcs</span></span>

<span data-ttu-id="756b4-151">最初、補充方法は、*ウェーブ需要数量* に設定されています。</span><span class="sxs-lookup"><span data-stu-id="756b4-151">Initially, the replenishment strategy is set to *Wave demand quantity*.</span></span>

<span data-ttu-id="756b4-152">倉庫への販売注文をリリースした後、ウェーブに対してウェーブ処理を実行すると、次の補充作業を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="756b4-152">After you release the sales order to the warehouse, and wave processing runs for the wave, you get the following replenishment work:</span></span>

- <span data-ttu-id="756b4-153">**補充作業 1:** バルク場所から 4 つのボックスをピックし、それを場所 pick-001 にプットします。</span><span class="sxs-lookup"><span data-stu-id="756b4-153">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
- <span data-ttu-id="756b4-154">**補充作業 2:** バルク場所から 2 つのボックスをピックし、それを場所 pick-002 にプットします。</span><span class="sxs-lookup"><span data-stu-id="756b4-154">**Replenishment work 2:** Pick 2 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="756b4-155">2 つの補充作業 ID を取得する必要があるのは、2 つの在庫場所を補充する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="756b4-155">You get two replenishment work IDs because you must replenish two locations, and multi-puts aren't supported.</span></span>

<span data-ttu-id="756b4-156">代わりに補充戦略を *場所の最大キャパシティ* に設定した場合、次の補充作業が行われます。</span><span class="sxs-lookup"><span data-stu-id="756b4-156">If you set the replenishment strategy to *Maximum location capacity* instead, you get the following replenishment work:</span></span>

- <span data-ttu-id="756b4-157">**補充作業 1:** バルク場所から 4 つのボックスをピックし、それを場所 pick-001 にプットします。</span><span class="sxs-lookup"><span data-stu-id="756b4-157">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
- <span data-ttu-id="756b4-158">**補充作業 2:** バルク場所から 5 つのボックスをピックし、それを場所 pick-002 にプットします。</span><span class="sxs-lookup"><span data-stu-id="756b4-158">**Replenishment work 2:** Pick 5 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="756b4-159">[![例 1](media/ReplenTemp_example_1.png "例 1")](media/ReplenTemp_example_1_large.png)</span><span class="sxs-lookup"><span data-stu-id="756b4-159">[![Example 1](media/ReplenTemp_example_1.png "Example 1")](media/ReplenTemp_example_1_large.png)</span></span>

### <a name="example-2"></a><span data-ttu-id="756b4-160">例 2</span><span class="sxs-lookup"><span data-stu-id="756b4-160">Example 2</span></span>

<span data-ttu-id="756b4-161">この例では、バルク場所に追加数量を処理するための在庫が不足している場合を示します。</span><span class="sxs-lookup"><span data-stu-id="756b4-161">This example shows what happens when the bulk location doesn't have enough inventory to cover the extra quantity.</span></span> <span data-ttu-id="756b4-162">この例では、例 1 と同じシナリオが使用されますが、バルク場所には 160 個 (8 ボックス) あります。</span><span class="sxs-lookup"><span data-stu-id="756b4-162">It uses the same scenario as example 1, but the bulk location has 160 pcs (8 boxes).</span></span>

<span data-ttu-id="756b4-163">*ウェーブ需要数量* 戦略では、例 1 に示すのと同じ作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="756b4-163">The *Wave demand quantity* strategy creates the same work that it did in example 1.</span></span>

<span data-ttu-id="756b4-164">ただし、*場所の最大キャパシティ* 戦略では、例 1 のように作業 ID を作成しようとするため、失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="756b4-164">However, because the *Maximum location capacity* strategy tries to create the work IDs as it did in example 1, it might fail.</span></span> <span data-ttu-id="756b4-165">その時点で、システムによって回復が試行されます。</span><span class="sxs-lookup"><span data-stu-id="756b4-165">At that point, the system tries to recover.</span></span>

<span data-ttu-id="756b4-166">補充ピッキングの保管場所ディレクティブの **分割を許可する** オプションの設定に応じて、次の 2 つの結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="756b4-166">Depending on the setting of the **Allow split** option on the location directives for replenishment picking, two outcomes are possible:</span></span>

- <span data-ttu-id="756b4-167">**分割を許可** オプションが *はい* に設定されている場合は、次の補充作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="756b4-167">If the **Allow split** option is set to *Yes*, the following replenishment work is created:</span></span>

    - <span data-ttu-id="756b4-168">**補充作業 1:** バルク場所から 4 つのボックスをピックし、それを場所 pick-001 にプットします。</span><span class="sxs-lookup"><span data-stu-id="756b4-168">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
    - <span data-ttu-id="756b4-169">**補充作業 2:** バルク場所から 4 つのボックスをピックし、それを場所 pick-002 にプットします。</span><span class="sxs-lookup"><span data-stu-id="756b4-169">**Replenishment work 2:** Pick 4 boxes from the bulk location, and put them in location pick-002.</span></span>

- <span data-ttu-id="756b4-170">**分割を許可** オプションが *いいえ* に設定されている場合は、次の補充作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="756b4-170">If the **Allow split** option is set to *No*, the following replenishment work is created:</span></span>

    - <span data-ttu-id="756b4-171">**補充作業 1:** バルク場所から 4 つのボックスをピックし、それを場所 pick-001 にプットします。</span><span class="sxs-lookup"><span data-stu-id="756b4-171">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
    - <span data-ttu-id="756b4-172">**補充作業 2:** バルク場所から 2 つのボックスをピックし、それを場所 pick-002 にプットします。</span><span class="sxs-lookup"><span data-stu-id="756b4-172">**Replenishment work 2:** Pick 2 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="756b4-173">結果は、作業を作成するときに使用できる情報によって異なります。</span><span class="sxs-lookup"><span data-stu-id="756b4-173">The outcomes differ because of the information that is available when you create the work.</span></span> <span data-ttu-id="756b4-174">補充ピッキングの場所ディレクティブで **分割を許可** が *はい* に設定されている場合、160 個を検索できたことがわかります。</span><span class="sxs-lookup"><span data-stu-id="756b4-174">When the **Allow split** is set to *Yes* on the location directives for replenishment picking, you know that you managed to find 160 pcs.</span></span> <span data-ttu-id="756b4-175">したがって、その数量に対して作業を作成できます。</span><span class="sxs-lookup"><span data-stu-id="756b4-175">Therefore, you can create work for that quantity.</span></span> <span data-ttu-id="756b4-176">ただし、**分割を許可** オプションが *いいえ* に設定されている場合、160 個の存在についてはわかりません。</span><span class="sxs-lookup"><span data-stu-id="756b4-176">However, when the **Allow split** option is set to *No*, you don't know about the existence of the 160 pcs.</span></span> <span data-ttu-id="756b4-177">補充することに決めた追加数量が 3 ボックスの場合、その追加の数量をドロップして元の数量を再度試します。</span><span class="sxs-lookup"><span data-stu-id="756b4-177">Because the extra quantity that you decided to replenish was 3 boxes, you drop that extra quantity and try the original quantity again.</span></span>

<span data-ttu-id="756b4-178">[![例 2](media/ReplenTemp_example_2.png "例 2")](media/ReplenTemp_example_2_large.png)</span><span class="sxs-lookup"><span data-stu-id="756b4-178">[![Example 2](media/ReplenTemp_example_2.png "Example 2")](media/ReplenTemp_example_2_large.png)</span></span>

<span data-ttu-id="756b4-179">したがって、補充された場所に対して最大数量を取得するには、補充ピッキングの保管場所ディレクティブで **分割を許可** オプションを *はい* に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="756b4-179">Therefore, to get the maximum quantity to the replenished locations, you should set the **Allow split** option to *Yes* on the location directives for replenishment picking.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]