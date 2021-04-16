---
title: マイナス在庫日数および動的マイナス在庫日数
description: このトピックでは、マイナス在庫日数および動的マイナス在庫日数に関する情報、およびこれらを使用してビジネスを支援する方法について説明します。
author: t-benebo
ms.date: 06/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 184f0f22d4587b25b02ca3d425ab26a6f8ab23f6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836617"
---
# <a name="negative-days-and-dynamic-negative-days"></a><span data-ttu-id="c3d79-103">マイナス在庫日数および動的マイナス在庫日数</span><span class="sxs-lookup"><span data-stu-id="c3d79-103">Negative days and dynamic negative days</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3d79-104">このトピックでは、マイナス在庫日数および動的マイナス在庫日数に関する情報、およびこれらを使用してビジネスを支援する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-104">This topic provides information about negative days and dynamic negative days, and how you can use them to help your business.</span></span> <span data-ttu-id="c3d79-105">*マイナス在庫日数タイム フェンス* は、マイナス在庫がある場合に、新しい補充を注文するまでに待機する日数を表します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-105">The *negative days time fence* represents the number of days that you're willing to wait before you order new replenishment when you have negative inventory.</span></span>

<span data-ttu-id="c3d79-106">このトピックでは、次の情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-106">In this topic, you will learn the following information:</span></span>

- <span data-ttu-id="c3d79-107">計画オーダーが作成される方法</span><span class="sxs-lookup"><span data-stu-id="c3d79-107">How planned orders are created</span></span>
- <span data-ttu-id="c3d79-108">マイナス在庫日数タイム フェンスと品目のリード タイムとの相関関係</span><span class="sxs-lookup"><span data-stu-id="c3d79-108">The correlation between the negative days time fence and the item's lead time</span></span>
- <span data-ttu-id="c3d79-109">動的マイナス在庫日数タイムフェンスの計算方法と、品目のリード タイムを計算に含める方法</span><span class="sxs-lookup"><span data-stu-id="c3d79-109">How the dynamic negative days time fence is calculated, and how the item's lead time is factored into the calculation</span></span>
- <span data-ttu-id="c3d79-110">マイナス在庫日数に関連する [原材料の必要量の計画 (MRP) (マスター プラン) の実行時間を改善するための提案](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx) を解釈する方法</span><span class="sxs-lookup"><span data-stu-id="c3d79-110">How to interpret the [suggestions for improving the running time for material requirements planning (MRP) (master planning)](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx) that are related to negative days</span></span>

<span data-ttu-id="c3d79-111">このトピックでは、この情報を理解するのに役立つ 3 つの仮想シナリオを使用します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-111">This topic uses three hypothetical scenarios to help you understand this information.</span></span> <span data-ttu-id="c3d79-112">シナリオ間の違いは、品目のリード タイム期間の前、最中、または後のどの時点で需要が発生するかという点です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-112">The difference between the scenarios is the point at which you get demand: before, during, or after the item's lead time period.</span></span>

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a><span data-ttu-id="c3d79-113">シナリオ 1: 品目のリード タイム期間よりも前に需要が発生する場合</span><span class="sxs-lookup"><span data-stu-id="c3d79-113">Scenario 1: You get demand before the item's lead time period</span></span>

<span data-ttu-id="c3d79-114">需要は、品目のリード タイムの比較的早い時点、またはリード タイム期間が始まる直前に発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-114">You might get demand either relatively early in your item's lead time or just before the lead time period begins.</span></span> <span data-ttu-id="c3d79-115">このシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-115">Here is an example of this scenario:</span></span>

- <span data-ttu-id="c3d79-116">DemoProduct 品目には、6 日間の購買リード タイムがあります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-116">The DemoProduct item has a six-day purchase lead time.</span></span>
- <span data-ttu-id="c3d79-117">0 日目 (1 月 1 日) の時点では、DemoProduct 品目の在庫レベルは 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-117">On day zero (January 1), the inventory level for the DemoProduct item is 0 (zero).</span></span>
- <span data-ttu-id="c3d79-118">0 日目 (1 月 1 日) に、DemoProduct 品目の数量 10 の販売注文を取得します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-118">On day zero (January 1), you get a sales order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="c3d79-119">7 日目 (1 月 7 日) には、DemoProduct 項目の数量 10 に対応する既存の発注書があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-119">On day seven (January 7), there is an existing purchase order for a quantity of 10 of the DemoProduct item.</span></span>

<span data-ttu-id="c3d79-120">次の図は、このシナリオのグラフィカル表示を示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-120">The following illustration shows a graphical view of this scenario.</span></span>

![シナリオ 1 のグラフィカル表示](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a><span data-ttu-id="c3d79-122">ケース A: マイナス在庫日数は品目のリード タイムより小さい</span><span class="sxs-lookup"><span data-stu-id="c3d79-122">Case A: Negative days are less than the item's lead time</span></span>

<span data-ttu-id="c3d79-123">マイナス在庫日数を品目のリード タイムよりも小さい値に設定すると、MRP は、マイナス在庫日数タイム フェンス内で DemoProduct 品目の入庫を検索します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-123">If you set the negative days to a number that is less than the item's lead time, MRP looks for receipts for the DemoProduct item inside the negative days time fence.</span></span> <span data-ttu-id="c3d79-124">入庫が見つからないため、MRP は新しい計画発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-124">Because it doesn't find any receipts, MRP creates a new planned purchase order.</span></span> <span data-ttu-id="c3d79-125">この計画オーダーは、すぐに 6 日 (リード タイム) 遅延します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-125">This planned order is immediately delayed by six days (the lead time).</span></span> <span data-ttu-id="c3d79-126">したがって、1 月 7 日に入庫することになります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-126">Therefore, it will arrive on January 7.</span></span> <span data-ttu-id="c3d79-127">新しい計画発注書の作成が必要でなくなったため、既存の発注書に **キャンセル** アクション メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-127">The existing purchase order gets a **Cancel** action message, because the creation of the new planned purchase order has made it redundant.</span></span>

<span data-ttu-id="c3d79-128">次の図は、このケースのスクリーンショットを示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-128">The following illustration shows a screenshot of this case.</span></span>

![シナリオ 1 のケース A スクリーンショット](./media/negative-days-2.png)

<span data-ttu-id="c3d79-130">次の図は、このケースに何が起こるかのグラフィカル表示です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-130">The following illustration shows a graphical view of what occurs in this case.</span></span>

![シナリオ 1 のケース A グラフィカル表示](./media/negative-days-3.png)

<span data-ttu-id="c3d79-132">MRP パフォーマンスとプランの違和感を考慮すると、このケースはうまく機能しません。</span><span class="sxs-lookup"><span data-stu-id="c3d79-132">If you consider MRP performance and plan nervousness, this case doesn't perform well.</span></span> <span data-ttu-id="c3d79-133">MRP は新しい計画オーダーを作成し、遅延とアクションを計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-133">MRP must create a new planned order, and must calculate delays and actions.</span></span> <span data-ttu-id="c3d79-134">これらのタスクには時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-134">These tasks are time-consuming.</span></span> <span data-ttu-id="c3d79-135">この場合、プランにはさらに 2 つのトランザクションが追加されます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-135">This case also adds two more transactions to your plan.</span></span> <span data-ttu-id="c3d79-136">一方、販売注文の遅延は 7 日ではなく、6 日だけです。</span><span class="sxs-lookup"><span data-stu-id="c3d79-136">On the other hand, the sales order is delayed by only six days, not seven days.</span></span>

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a><span data-ttu-id="c3d79-137">ケース B: マイナス在庫日数は品目のリード タイムより大きい</span><span class="sxs-lookup"><span data-stu-id="c3d79-137">Case B: Negative days are more than the item's lead time</span></span>

<span data-ttu-id="c3d79-138">MRP のパフォーマンスを向上させるために、マイナス在庫日数を品目のリード タイムよりも大きい数値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-138">To help improve MRP performance, you can set the negative days to a number that is more than the item's lead time.</span></span> <span data-ttu-id="c3d79-139">このシナリオではリード タイム内に供給を受けることができないため、この検索が理にかなっている限り、入庫を検索できます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-139">Because you can't get the supply inside the lead time in this scenario, you can search for receipts for as long as this search makes sense.</span></span> <span data-ttu-id="c3d79-140">MRP の実行時間は短くなりますが、注文に対する追加の遅延には注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-140">Although the running time for MRP will be shorter, you should watch out for additional delays to the orders.</span></span>

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a><span data-ttu-id="c3d79-141">ケース C: 品目のリード タイムのマイナス在庫日数タイム フェンスへの自動的な関連付け</span><span class="sxs-lookup"><span data-stu-id="c3d79-141">Case C: Automatically correlate the item's lead time to the negative days time fence</span></span>

<span data-ttu-id="c3d79-142">品目のリード タイムをマイナス在庫日数タイム フェンスへ自動的に関連付けるには、動的マイナス在庫日数を使用します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-142">To automatically correlate the item's lead time to the negative days time fence, use dynamic negative days.</span></span> <span data-ttu-id="c3d79-143">動的マイナス在庫日数を使用するには、**マスター プラン \> 設定 \> マスター プラン パラメーター** に移動してから、**一般** タブの **補充** セクションで、**動的マイナス在庫日数を使用する** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-143">To use dynamic negative days, go to **Master planning \> Setup \> Master planning parameters**, and then, on the **General** tab, in the **Coverage** section, set the **Use dynamic negative days** option to **Yes**.</span></span> <span data-ttu-id="c3d79-144">次に、MRP は動的マイナス在庫日数タイム フェンス内の入庫を検索します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-144">MRP then looks for receipts inside the dynamic negative days time fence.</span></span> <span data-ttu-id="c3d79-145">このタイム フェンスは次の式を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-145">This time fence is calculated by using the following formula:</span></span>

<span data-ttu-id="c3d79-146">動的マイナス在庫日数タイム フェンス = 購買のリード タイム + 動的マイナス在庫日数タイムフェンス + (現在の日付 – 要求日)</span><span class="sxs-lookup"><span data-stu-id="c3d79-146">Dynamic negative days time fence = Purchase lead time + Negative days time fence + (Current date – Requirement date)</span></span>

<span data-ttu-id="c3d79-147">(DemoProduct 品目の既定の注文タイプが **生産** または **転送** である場合、リード タイムは **在庫** リード タイムになります。)</span><span class="sxs-lookup"><span data-stu-id="c3d79-147">(If the default order type of the DemoProduct item is **Production** or **Transfer**, the lead time is the **inventory** lead time.)</span></span>

<span data-ttu-id="c3d79-148">動的マイナス在庫日数が使用される場合、MRP が入庫を検索するタイム フェンスは 6 + 2 + 0 = 8 日になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-148">When dynamic negative days are used, the time fence that MRP looks at for receipts is now 6 + 2 + 0 = 8 days.</span></span> <span data-ttu-id="c3d79-149">MRP は既存の発注書を検索して、それに対する販売注文を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-149">MRP finds the existing purchase order and pegs the sales order against it.</span></span> <span data-ttu-id="c3d79-150">新しい計画オーダーは作成されません。</span><span class="sxs-lookup"><span data-stu-id="c3d79-150">No new planned orders are created.</span></span> <span data-ttu-id="c3d79-151">したがって、MRP の実行時間は短くなります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-151">Therefore, the running time for MRP is shorter.</span></span> <span data-ttu-id="c3d79-152">次の図は、DemoProduct 品目の正味必要量を示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-152">The following illustration shows the net requirements for the DemoProduct item.</span></span>

![シナリオ 1 のケース C 正味必要量](./media/negative-days-4.png)

<span data-ttu-id="c3d79-154">次の図は、このケースに何が起こるかのグラフィカル表示です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-154">The following illustration shows a graphical view of what occurs in this case.</span></span>

![シナリオ 1 のケース C グラフィカル表示](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a><span data-ttu-id="c3d79-156">ケース D: 動的マイナス在庫日数のみを使用</span><span class="sxs-lookup"><span data-stu-id="c3d79-156">Case D: Use only dynamic negative days</span></span>

<span data-ttu-id="c3d79-157">マイナス在庫日数を **0** (ゼロ) に設定し、動的マイナス在庫日数のタイム フェンスのみを使用した場合、動的マイナス在庫日数タイム フェンスは 6 + 0 + 0 = 6 日になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-157">If you set the negative days to **0** (zero) and use only the dynamic negative days time fence, the dynamic negative days time fence is 6 + 0 + 0 = 6 days.</span></span> <span data-ttu-id="c3d79-158">この場合、このシナリオのケース A と同じ結果になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-158">In this case, the result is the same as the result in case A for this scenario.</span></span> <span data-ttu-id="c3d79-159">MRP は新しい計画オーダーを作成し、遅延とアクションを計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-159">MRP must create a new planned order, and must calculate delays and actions.</span></span> <span data-ttu-id="c3d79-160">これらの作業には時間がかかり、もどかしい場合もあります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-160">These tasks are time-consuming and can also be frustrating.</span></span> <span data-ttu-id="c3d79-161">さらに、処理対象のトランザクションがさらに 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-161">You also have two more transactions to process.</span></span> <span data-ttu-id="c3d79-162">品目が入庫に間に合うよう需要を満たすことができないので、この場合、プランに不要な煩雑さが加わります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-162">Because the demand can't be fulfilled on time for the item to arrive, this case adds unnecessary complications to your plan.</span></span>

<span data-ttu-id="c3d79-163">次の図は、このケースのスクリーンショットを示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-163">The following illustration shows a screenshot for this case.</span></span>

![シナリオ 1 のケース D スクリーンショット](./media/negative-days-6.png)

<span data-ttu-id="c3d79-165">次の図は、このケースに何が起こるかのグラフィカル表示です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-165">The following illustration shows a graphical view of what occurs in this case.</span></span>

![シナリオ 1 のケース D グラフィカル表示](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a><span data-ttu-id="c3d79-167">ケース E: 品目のリード タイムを超えるマイナス在庫日数と、動的マイナス在庫日数タイム フェンスの両方を使用する</span><span class="sxs-lookup"><span data-stu-id="c3d79-167">Case E: Use both negative days that are more than the item's lead time and the dynamic negative days time fence</span></span>

<span data-ttu-id="c3d79-168">マイナス在庫日数を品目のリード タイムより大きい数に設定した場合や、動的マイナス在庫日数のタイム フェンスも使用している場合は、動的マイナス在庫日数のタイム フェンスは 6 + 6 + 0 = 12 日になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-168">If you set the negative days to a number that is more than the item's lead time, and if you also use the dynamic negative days time fence, the dynamic negative days time fence is 6 + 6 + 0 = 12 days.</span></span> <span data-ttu-id="c3d79-169">この方法では、MRP が結果を検索する必要がある非常に長いタイム フェンスが生成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-169">This approach might produce a very long time fence that MRP must search for results in.</span></span> <span data-ttu-id="c3d79-170">マイナス在庫日数を長いタイム フェンスに設定した場合に、ケース E がどのように関連しているかについては、このトピックの [まとめ](#conclusion) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3d79-170">For information about how case E is related to a situation where you set the negative days to a long time fence, see the [Conclusion](#conclusion) section of this topic.</span></span>

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a><span data-ttu-id="c3d79-171">シナリオ 2: 品目のリード タイム期間中に需要が発生する場合</span><span class="sxs-lookup"><span data-stu-id="c3d79-171">Scenario 2: You get demand during the item's lead time period</span></span>

<span data-ttu-id="c3d79-172">品目のリード タイム中に需要が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-172">You might get demand sometime during your item's lead time.</span></span> <span data-ttu-id="c3d79-173">このシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-173">Here is an example of this scenario:</span></span>

- <span data-ttu-id="c3d79-174">DemoProduct 品目には、6 日間の購買リード タイムがあります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-174">The DemoProduct item has a six-day purchase lead time.</span></span> 
- <span data-ttu-id="c3d79-175">0 日目 (1 月 1 日) の時点では、DemoProduct 品目の在庫レベルは 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-175">On day zero (January 1), the inventory level for the DemoProduct item is 0 (zero).</span></span>
- <span data-ttu-id="c3d79-176">品目のリード タイム内である 4 日目 (1 月 5 日) に、DemoProduct 品目の数量 10 の販売注文を取得します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-176">On day four (January 5), which is inside the item's lead time, you get a sales order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="c3d79-177">7 日目 (1 月 8 日) には、DemoProduct 項目の数量 10 に対応する発注書があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-177">On day seven (January 8), there is a purchase order for a quantity of 10 of the DemoProduct item.</span></span>

<span data-ttu-id="c3d79-178">次の図は、このシナリオのグラフィカル表示を示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-178">The following illustration shows a graphical view of this scenario.</span></span>

![シナリオ 1 のグラフィカル表示](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a><span data-ttu-id="c3d79-180">ケース A: マイナス在庫日数は品目のリード タイムより小さい</span><span class="sxs-lookup"><span data-stu-id="c3d79-180">Case A: Negative days are less than the item's lead time</span></span>

<span data-ttu-id="c3d79-181">マイナス在庫日数を品目のリード タイムよりも小さい値に設定すると、MRP は、マイナス在庫日数タイム フェンス内で DemoProduct 品目の入庫を検索します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-181">If you set the negative days to a number that is less than the item's lead time, MRP looks for receipts for the DemoProduct item inside the negative days time fence.</span></span> <span data-ttu-id="c3d79-182">入庫が見つからないため、現在の日付を注文日として使用する新しい計画発注書が MRP によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-182">Because it doesn't find any receipts, MRP creates a new planned purchase order that uses the current date as the order date.</span></span> <span data-ttu-id="c3d79-183">この計画オーダーは、すぐに 6 日 (リード タイム) 遅延します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-183">This planned order is immediately delayed by six days (the lead time).</span></span> <span data-ttu-id="c3d79-184">したがって、1 月 7 日に入庫することになります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-184">Therefore, it will arrive on January 7.</span></span> <span data-ttu-id="c3d79-185">新しい計画発注書の作成が必要でなくなったため、既存の発注書に **キャンセル** アクション メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-185">The existing purchase order gets a **Cancel** action message, because the creation of the new planned purchase order has made it redundant.</span></span>

<span data-ttu-id="c3d79-186">次の図は、このケースのスクリーンショットを示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-186">The following illustration shows a screenshot for this case.</span></span>

![シナリオ 2 のケース A スクリーンショット](./media/negative-days-9.png)

<span data-ttu-id="c3d79-188">次の図は、このケースに何が起こるかのグラフィカル表示です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-188">The following illustration shows a graphical view of what occurs in this case.</span></span>

![シナリオ 2 のケース A グラフィカル表示](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a><span data-ttu-id="c3d79-190">ケース B: マイナス在庫日数は品目のリード タイムより大きい</span><span class="sxs-lookup"><span data-stu-id="c3d79-190">Case B: Negative days are more than the item's lead time</span></span>

<span data-ttu-id="c3d79-191">このケースは、シナリオ 1 のケース B に似ています。</span><span class="sxs-lookup"><span data-stu-id="c3d79-191">This case resembles case B for scenario 1.</span></span> <span data-ttu-id="c3d79-192">マイナス在庫日数を品目のリード タイムよりも大きい値に設定すると、新しい計画オーダーは取得されません。</span><span class="sxs-lookup"><span data-stu-id="c3d79-192">If you set the negative days to a number that is more than the item's lead time, you don't get a new planned order.</span></span> <span data-ttu-id="c3d79-193">販売注文は、既存の発注書に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-193">The sales order is attached to the existing purchase order.</span></span>

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a><span data-ttu-id="c3d79-194">ケース C: 品目のリード タイムのマイナス在庫日数タイム フェンスへの自動的な関連付け</span><span class="sxs-lookup"><span data-stu-id="c3d79-194">Case C: Automatically correlate the item's lead time to the negative days time fence</span></span>

<span data-ttu-id="c3d79-195">このケースは、動的マイナス在庫日数がそのケースと同様に機能するため、シナリオ 1 のケース C に似ています。</span><span class="sxs-lookup"><span data-stu-id="c3d79-195">This case resembles case C for scenario 1, because dynamic negative days work just as well as they do in that case.</span></span> <span data-ttu-id="c3d79-196">動的マイナス在庫日数のタイム フェンスは、6 + 2 – 4 = 4 日になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-196">The dynamic negative days time fence is now 6 + 2 – 4 = 4 days.</span></span> <span data-ttu-id="c3d79-197">この方法を使用した場合、MRP は既存の発注書を検索し、販売注文をその発注書に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-197">If you use this approach, MRP finds the existing purchase order and attaches the sales order to it.</span></span> <span data-ttu-id="c3d79-198">新しい計画オーダーが作成されないため、MRP の実行時間は短くなります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-198">Because no new planned orders are created, the running time for MRP is shorter.</span></span>

<span data-ttu-id="c3d79-199">次の図は、このケースのスクリーンショットを示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-199">The following illustration shows a screenshot of this case.</span></span>

![シナリオ 2 のケース C スクリーンショット](./media/negative-days-11.png)

<span data-ttu-id="c3d79-201">次の図は、このケースに何が起こるかのグラフィカル表示です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-201">The following illustration shows a graphical view of what occurs in this case.</span></span>

![シナリオ 2 のケース C グラフィカル表示](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a><span data-ttu-id="c3d79-203">ケース D: 動的マイナス在庫日数のみを使用</span><span class="sxs-lookup"><span data-stu-id="c3d79-203">Case D: Use only dynamic negative days</span></span>

<span data-ttu-id="c3d79-204">マイナス在庫日数を **0** (ゼロ) に設定し、動的マイナス在庫日数のタイム フェンスのみを使用した場合、動的マイナス在庫日数タイム フェンスは 6 + 0 – 4 = 2 日になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-204">If you set the negative days to **0** (zero) and use only the dynamic negative days time fence, the dynamic negative days time fence is now 6 + 0 – 4 = 2 days.</span></span> <span data-ttu-id="c3d79-205">この場合、このシナリオのケース A と同じ結果になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-205">In this case, the result is the same as the result in case A for this scenario.</span></span> <span data-ttu-id="c3d79-206">何が起こるかのグラフィカル表示については、このシナリオのケース A を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3d79-206">For a graphical view of what occurs, see case A for this scenario.</span></span>

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a><span data-ttu-id="c3d79-207">ケース E: 品目のリード タイムを超えるマイナス在庫日数と、動的マイナス在庫日数タイム フェンスの両方を使用する</span><span class="sxs-lookup"><span data-stu-id="c3d79-207">Case E: Use both negative days that are more than the item's lead time and the dynamic negative days time fence</span></span>

<span data-ttu-id="c3d79-208">マイナス在庫日数を品目のリード タイムより大きい数に設定した場合や、動的マイナス在庫日数のタイム フェンスも使用している場合は、動的マイナス在庫日数のタイム フェンスは 6 + 6 – 4 = 8 日になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-208">If you set the negative days to a number that is more than the item's lead time, and if you also use the dynamic negative days time fence, the dynamic negative days time fence is 6 + 6 – 4 = 8 days.</span></span> <span data-ttu-id="c3d79-209">この方法では、MRP が結果を検索する必要がある非常に長いタイム フェンスが生成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-209">This approach might produce a very long time fence that MRP must search for results in.</span></span> <span data-ttu-id="c3d79-210">マイナス在庫日数を長いタイム フェンスに設定した場合に、ケース E がどのように関連しているかについては、このトピックの [まとめ](#conclusion) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3d79-210">For information about how case E is related to a situation where you set the negative days to a long time fence, see the [Conclusion](#conclusion) section of this topic.</span></span>

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a><span data-ttu-id="c3d79-211">シナリオ 3: 品目のリード タイム期間後に需要が発生する場合</span><span class="sxs-lookup"><span data-stu-id="c3d79-211">Scenario 3: You get demand after the item's lead time period</span></span>

<span data-ttu-id="c3d79-212">品目のリード タイム期間後に需要が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-212">You might get demand after the item's lead time.</span></span> <span data-ttu-id="c3d79-213">このシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-213">Here is an example of this scenario:</span></span>

- <span data-ttu-id="c3d79-214">DemoProduct 品目には、6 日間の購買リード タイムがあります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-214">The DemoProduct item has a six-day purchase lead time.</span></span>
- <span data-ttu-id="c3d79-215">0 日目 (1 月 1 日) の時点では、DemoProduct 品目の在庫は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-215">On day zero (January 1), the inventory for the DemoProduct item is 0 (zero).</span></span>
- <span data-ttu-id="c3d79-216">品目のリード タイム外である 7 日目 (1 月 8 日) に、DemoProduct 品目の数量 10 の販売注文を取得します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-216">On day seven (January 8), which is outside the item's lead time, you get a sales order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="c3d79-217">10 日目 (1 月 11 日) には、DemoProduct 項目の数量 10 に対応する発注書があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-217">On day 10 (January 11), there is a purchase order for a quantity of 10 of the DemoProduct item.</span></span>

<span data-ttu-id="c3d79-218">次の図は、このシナリオのグラフィカル表示を示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-218">The following illustration shows a graphical view of this scenario.</span></span>

![シナリオ 3 のグラフィカル表示](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a><span data-ttu-id="c3d79-220">ケース A: マイナス在庫日数は品目のリード タイムより小さい</span><span class="sxs-lookup"><span data-stu-id="c3d79-220">Case A: Negative days are less than the item's lead time</span></span>

<span data-ttu-id="c3d79-221">マイナス在庫日数を品目のリード タイムより小さい値に設定すると、MRP は販売注文の要求日から 2 日先を検索します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-221">If you set the negative days to a number that is less than the item's lead time, MRP looks two days ahead of the sales order's requirement date.</span></span> <span data-ttu-id="c3d79-222">何も見つからないため、MRP は 1 月 2 日に新しい計画発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-222">Because it doesn't find anything, MRP creates a planned purchase order on January 2.</span></span> <span data-ttu-id="c3d79-223">この計画発注書は、販売注文の需要を満たすのにちょうど間に合うよう出荷されます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-223">This planned purchase order will be shipped just in time to fulfill the sales order demand.</span></span> <span data-ttu-id="c3d79-224">既存の発注書には、必須ではないため **キャンセル** アクション メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-224">The existing purchase order gets a **Cancel** action message, because it isn't required.</span></span>

<span data-ttu-id="c3d79-225">次の図は、このケースのスクリーンショットを示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-225">The following illustration shows a screenshot of this case.</span></span>

![シナリオ 3 のケース A スクリーンショット](./media/negative-days-14.png)

<span data-ttu-id="c3d79-227">次の図は、このケースに何が起こるかのグラフィカル表示です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-227">The following illustration shows a graphical view of what occurs in this case.</span></span>

![シナリオ 3 のケース A グラフィカル表示](./media/negative-days-15.png)

> [!NOTE]
> <span data-ttu-id="c3d79-229">前のスクリーンショットでは、発注書の要求日は 1 月 12 日です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-229">In the preceding screenshot, the purchase order requirement date is January 12.</span></span> <span data-ttu-id="c3d79-230">このスクリーンショットは 2015 年に取られたものだったため、1 月 11 日が日曜日である場合、MRP は要求日を次の稼働日である 1 月 12 日の月曜日に移動しました。</span><span class="sxs-lookup"><span data-stu-id="c3d79-230">Because that screenshot was taken in 2015, when January 11 was a Sunday, MRP moved the requirement date to the next working day, which was Monday, January 12.</span></span> <span data-ttu-id="c3d79-231">ただし、発注書の配送日は 1 月 11 日になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-231">Nevertheless, the purchase order has a delivery date of January 11.</span></span>

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a><span data-ttu-id="c3d79-232">ケース B: マイナス在庫日数は品目のリード タイムより大きい</span><span class="sxs-lookup"><span data-stu-id="c3d79-232">Case B: Negative days are more than the item's lead time</span></span>

<span data-ttu-id="c3d79-233">マイナス在庫日数を品目のリード タイムよりも大きい値に設定すると、新しい計画オーダーは取得されません。</span><span class="sxs-lookup"><span data-stu-id="c3d79-233">If you set the negative days to a number that is more than the item's lead time, you don't get a new planned order.</span></span> <span data-ttu-id="c3d79-234">販売注文は、既存の発注書に対して関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-234">The sales order is pegged against the existing purchase order.</span></span> <span data-ttu-id="c3d79-235">したがって、販売注文は遅延します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-235">Therefore, the sales order is delayed.</span></span> <span data-ttu-id="c3d79-236">計画オーダーが作成されると、販売注文を期限遵守で出荷できます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-236">If you create a planned order, you can ship the sales order on time.</span></span>

<span data-ttu-id="c3d79-237">次の図は、このケースのスクリーンショットを示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-237">The following illustration shows a screenshot of this case.</span></span>

![シナリオ 3 のケース B スクリーンショット](./media/negative-days-16.png)

<span data-ttu-id="c3d79-239">次の図は、このケースに何が起こるかのグラフィカル表示です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-239">The following illustration shows a graphical view of what occurs in this case.</span></span>

![シナリオ 3 のケース B グラフィカル表示](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a><span data-ttu-id="c3d79-241">ケース C: 品目のリード タイムのマイナス在庫日数タイム フェンスへの自動的な関連付け</span><span class="sxs-lookup"><span data-stu-id="c3d79-241">Case C: Automatically correlate the item's lead time to the negative days time fence</span></span>

<span data-ttu-id="c3d79-242">このケースは、シナリオ 1 のケース C に似ています。動的マイナス在庫日数がこのシナリオのケース B の場合と同様に機能するためです。</span><span class="sxs-lookup"><span data-stu-id="c3d79-242">This case resembles case C for scenario 1, because dynamic negative days work just as well as, if not better than, they work in case B for this scenario.</span></span>

<span data-ttu-id="c3d79-243">動的マイナス在庫日数のタイム フェンスは、6 + 2 – 7 = 1 日になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-243">The dynamic negative days time fence is 6 + 2 – 7 = 1 day.</span></span> <span data-ttu-id="c3d79-244">ただし、この場合、MRP では在庫日数リード タイムと動的マイナス在庫日数リード タイム間の最大値が考慮されるため、システムはマイナス在庫日数リード タイム (2) を考慮します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-244">However, in this case, the system still considers the negative days lead time (2), because MRP considers the maximum value between the negative days lead time and the dynamic negative days lead time.</span></span> <span data-ttu-id="c3d79-245">したがって、このケースの結果は、このシナリオのケース A と同じ結果になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-245">Therefore, the result in this case is the same as the result in case A for this scenario.</span></span>

<span data-ttu-id="c3d79-246">次の図は、このケースに何が起こるかのグラフィカル表示です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-246">The following illustration shows a graphical view of what occurs in this case.</span></span>

![シナリオ 3 のケース C グラフィカル表示](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a><span data-ttu-id="c3d79-248">ケース D: 動的マイナス在庫日数のみを使用</span><span class="sxs-lookup"><span data-stu-id="c3d79-248">Case D: Use only dynamic negative days</span></span>

<span data-ttu-id="c3d79-249">マイナス在庫日数を **0** (ゼロ) に設定し、動的マイナス在庫日数のタイム フェンスのみを使用した場合、動的マイナス在庫日数タイム フェンスは 6 + 0 – 7 = -1 日になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-249">If you set the negative days to **0** (zero) and use only the dynamic negative days time fence, the dynamic negative days time fence is now 6 + 0 – 7 = -1 day.</span></span> <span data-ttu-id="c3d79-250">この場合、マイナス在庫日数リード タイム (2) が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-250">In this case, the system still considers the negative days lead time (2).</span></span> <span data-ttu-id="c3d79-251">したがって、このケースの結果は、このシナリオのケース A と同じ結果になり、すべて同じ短所があることになります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-251">Therefore, the result in this case is the same as the result in case A for this scenario and has all the same drawbacks.</span></span> <span data-ttu-id="c3d79-252">何が起こるかのグラフィカル表示については、シナリオ 2 のケース A を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3d79-252">For a graphical view of what occurs, see case A for scenario 2.</span></span>

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a><span data-ttu-id="c3d79-253">ケース E: 品目のリード タイムを超えるマイナス在庫日数と、動的マイナス在庫日数タイム フェンスの両方を使用する</span><span class="sxs-lookup"><span data-stu-id="c3d79-253">Case E: Use both negative days that are more than the item's lead time and the dynamic negative days time fence</span></span>

<span data-ttu-id="c3d79-254">このケースは、シナリオ 1 および 2 のケース E と同じです。</span><span class="sxs-lookup"><span data-stu-id="c3d79-254">This case is the same as case E for scenarios 1 and 2.</span></span> <span data-ttu-id="c3d79-255">基本的に、同じ長所と短所があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-255">It has basically the same benefits and drawbacks.</span></span>

## <a name="conclusion"></a><span data-ttu-id="c3d79-256">まとめ</span><span class="sxs-lookup"><span data-stu-id="c3d79-256">Conclusion</span></span>

<span data-ttu-id="c3d79-257">このトピックに示す 3 つのシナリオでは、マイナス在庫日数は、補充グループの品目のリード タイムよりも大きい数に設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c3d79-257">As the three scenarios in this topic show, it's a good idea to set the negative days to a number that is more than the lead time of the items in the coverage group.</span></span> <span data-ttu-id="c3d79-258">また、動的マイナス在庫日数のみを使用し、マイナス在庫がある場合は、マイナス在庫日数を新しい補充を注文するまで待機できる日数 (つまり、需要をさらに遅延させてもよい日数) に設定します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-258">It's also a good idea to use only dynamic negative days, and to set the negative days to the number of days that you're willing to wait before you order new replenishment when you have negative inventory (in other words, the number of days that you're willing to further delay demand).</span></span> <span data-ttu-id="c3d79-259">また、同じ補充グループの品目には同じリード タイムを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-259">Additionally, items in the same coverage group should have similar lead times.</span></span>

<span data-ttu-id="c3d79-260">マイナス在庫日数を **0** (ゼロ) に設定し、動的マイナス在庫日数を使用しない場合、MRP は常に新しい計画オーダーを作成して需要を満たすようにします。</span><span class="sxs-lookup"><span data-stu-id="c3d79-260">If you set the negative days to **0** (zero) and don't use dynamic negative days, MRP always creates a new planned order to fulfill demand.</span></span> <span data-ttu-id="c3d79-261">この状況では、アクション メッセージを使用して、在庫がなくなるようにすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-261">In this situation, it's important that you work with the action messages to make sure that you don't pile up inventory.</span></span>

<span data-ttu-id="c3d79-262">マイナス在庫日数を長いタイム フェンスに設定し、アクション メッセージを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-262">You might want to set the negative days to a long time fence and then work with the action messages.</span></span> <span data-ttu-id="c3d79-263">この方法により、プランを適切に作成できますが、少し時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-263">This approach produces good planning results, but it's also a bit slower.</span></span> <span data-ttu-id="c3d79-264">アクション メッセージを分析し適用する必要があるため、分析がより困難になる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-264">It might also be more difficult to analyze, because you must analyze and apply the action messages.</span></span> <span data-ttu-id="c3d79-265">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-265">Here is an example:</span></span>

- <span data-ttu-id="c3d79-266">DemoProduct 品目には、6 日間の購買リード タイムがあります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-266">The DemoProduct item has a six-day purchase lead time.</span></span>
- <span data-ttu-id="c3d79-267">0 日目 (1 月 1 日) の時点では、DemoProduct 品目の在庫は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-267">On day zero (January 1), the inventory for the DemoProduct item is 0 (zero).</span></span>
- <span data-ttu-id="c3d79-268">0 日目 (1 月 1 日) に、DemoProduct 品目の数量 10 の販売注文を取得します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-268">On day zero (January 1), you get a sales order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="c3d79-269">10 日目 (1 月 10 日) に、DemoProduct 品目の数量 10 の販売注文を取得します。</span><span class="sxs-lookup"><span data-stu-id="c3d79-269">On day 10 (January 10), you get a sales order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="c3d79-270">12 日目 (1 月 12 日) には、DemoProduct 項目の数量 10 に対応する発注書があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-270">On day 12 (January 12), there is a purchase order for a quantity of 10 of the DemoProduct item.</span></span>
- <span data-ttu-id="c3d79-271">マイナス在庫日数は **20** に設定され、品目のリード タイムよりもかなり大きくなります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-271">Negative days are set to **20**, which is much more than the item's lead time.</span></span>

<span data-ttu-id="c3d79-272">次の図は、何が起こるかのグラフィカル表示です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-272">The following illustration shows a graphical view of what occurs.</span></span>

![例のグラフィカル レビュー](./media/negative-days-19.png)

<span data-ttu-id="c3d79-274">MRP では次の結果が生成されます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-274">MRP produces the following results.</span></span>

![結果](./media/negative-days-20.png)

<span data-ttu-id="c3d79-276">前のスクリーンショットでは、販売注文の要求日は 1 月 10 日ではなく、1 月 9 日になります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-276">In the preceding screenshot, the sales order requirement date is January 9 instead of January 10.</span></span> <span data-ttu-id="c3d79-277">このスクリーンショットは 2015 年に取られたものだったため、1 月 10 日が土曜日である場合、注文の要求日を前の稼働日である 1 月 9 日の金曜日にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-277">Because that screenshot was taken in 2015, when January 10 was a Saturday, the requirement date of the order should be the previous working day, which was Friday, January 9.</span></span>

<span data-ttu-id="c3d79-278">MRP は、最初の販売注文で要求される需要を満たす計画発注書を作成しますが、その後、計画オーダーをキャンセルするよう勧めてきます。それは既存の発注書を繰り上げて数量を増やすことができるためです。</span><span class="sxs-lookup"><span data-stu-id="c3d79-278">MRP creates a planned purchase order to fulfill the demand that is requested by the first sales order, but then it also recommends that you cancel the planned order, because you can advance the existing purchase order and increase the quantity on it.</span></span>

<span data-ttu-id="c3d79-279">結果は間違っていませんが、MRP の実行時間は長くなります。それは MRP がすべての遅延と提案を作成する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="c3d79-279">The results aren't wrong, but the running time for MRP might be longer, because MRP must create all the delays and suggestions.</span></span> <span data-ttu-id="c3d79-280">また、プランナーは MRP の結果を理解するためにより多くの時間を必要とする場合があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-280">Additionally, the planner might require more time to understand the MRP results.</span></span> <span data-ttu-id="c3d79-281">この場合、最も重要な点として、プランナーがアクション メッセージを理解して使用することが必須です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-281">Most importantly, in this case, it's essential that the planner understand and use the action messages.</span></span>

<span data-ttu-id="c3d79-282">マイナス在庫日数を品目のリード タイムに近い値に減らし、動的マイナス在庫日数を使用すると、MRP では次のような結果が生成されます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-282">If you reduce the negative days to a number that's closer to the item's lead time, and you use dynamic negative days, MRP produces the following results.</span></span>

![結果](./media/negative-days-21.png)

<span data-ttu-id="c3d79-284">MRP では、最初の販売注文に関連付けられた計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-284">MRP creates a planned order that is attached to the first sales order.</span></span> <span data-ttu-id="c3d79-285">その後、予想されるように、2 番目の販売注文は、マイナス在庫日数の設定に基づいて既存の発注書に対して関連付けされます。</span><span class="sxs-lookup"><span data-stu-id="c3d79-285">Then, as is expected, the second sales order is pegged against the existing purchase order, based on the negative days setting.</span></span> <span data-ttu-id="c3d79-286">このプランニング結果も正しく、MRP の実行時間が短くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-286">This planning result is also correct, and the running time for MRP might be shorter.</span></span> <span data-ttu-id="c3d79-287">この場合、アクション メッセージをどのように処理するかを理解しておくことは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="c3d79-287">In this case, it isn't essential that you understand and know how to work with the action messages.</span></span>

<span data-ttu-id="c3d79-288">業務に合った正しい値が確実に入力されるようにするには、機能と MRP の実行時間の両方について考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3d79-288">To help guarantee that the correct values are entered for your business, you must think in terms of both functionality and MRP running time.</span></span> <span data-ttu-id="c3d79-289">したがって、最適値を特定するには少し試行錯誤が必要です。</span><span class="sxs-lookup"><span data-stu-id="c3d79-289">Therefore, it can take a little trial and error to determine the optimal values.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3d79-290">参照</span><span class="sxs-lookup"><span data-stu-id="c3d79-290">See also</span></span>

<span data-ttu-id="c3d79-291">詳しい解説については、元の [(動的) マイナス在庫日数の詳細](https://blogs.msdn.microsoft.com/axmfg/2015/02/19/more-about-dynamic-negative-days/) ブログ投稿を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3d79-291">For more discussion, see the original [More about (dynamic) negative days](https://blogs.msdn.microsoft.com/axmfg/2015/02/19/more-about-dynamic-negative-days/) blog post.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]