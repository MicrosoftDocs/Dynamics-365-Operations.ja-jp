---
title: "製造オーダーの原価分析"
description: "この記事は、完了した製造オーダーおよび現在の製造オーダーに対して実行できる原価分析について説明します。 [価格計算] ページまたは [原価見積] レポートを使用して、見積原価および実際原価を分析できます。 コンポーネント品目、工順工程、および間接原価ごとに見積原価と実績原価 (および数量) についての情報を表示できます。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 703070ae85f504cf204244b2197732dc6849abd6
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="production-order-cost-analysis"></a><span data-ttu-id="e1f8b-105">製造オーダーの原価分析</span><span class="sxs-lookup"><span data-stu-id="e1f8b-105">Production order cost analysis</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e1f8b-106">この記事は、完了した製造オーダーおよび現在の製造オーダーに対して実行できる原価分析について説明します。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-106">This article provides information about the cost analysis that you can do for completed and current production orders.</span></span> <span data-ttu-id="e1f8b-107">[価格計算] ページまたは [原価見積] レポートを使用して、見積原価および実際原価を分析できます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-107">You can analyze the estimated costs and actual costs by using the Price calculation page or the Cost estimates and costings report.</span></span> <span data-ttu-id="e1f8b-108">コンポーネント品目、工順工程、および間接原価ごとに見積原価と実績原価 (および数量) についての情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-108">You can view information about the estimated and actual costs (and quantity) for each component item, the routing operation, and the indirect cost.</span></span>

<span data-ttu-id="e1f8b-109">製造オーダーの実績原価は、報告済の材料消費と工順工程に基づきます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-109">The actual costs for a production order are based on the reported consumption of material and routing operations.</span></span> <span data-ttu-id="e1f8b-110">報告済の材料消費、工順工程、および間接原価についての詳細トランザクションには、製造オーダーの [**生産の転記**] ページでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-110">You can access detailed transactions about the reported consumption of material, routing operations, and indirect costs for a production order on the **Production posting** page.</span></span>

## <a name="variance-analysis-for-a-completed-production-order"></a><span data-ttu-id="e1f8b-111">完了した発注書の差異分析</span><span class="sxs-lookup"><span data-stu-id="e1f8b-111">Variance analysis for a completed production order</span></span>
<span data-ttu-id="e1f8b-112">差異は、報告された生産活動と、生産品目の標準原価計算の比較を反映します。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-112">The variances reflect a comparison of the reported production activities and the calculation of standard costs for the production item.</span></span> <span data-ttu-id="e1f8b-113">差異は、製造オーダーの見積原価との比較を反映しません。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-113">The variances don't reflect a comparison to the production order's estimated costs.</span></span> <span data-ttu-id="e1f8b-114">報告された生産活動には、材料の消費と工順工程 (および関連する間接原価)、および完了済として報告された数量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-114">The production activities that are reported include the consumption of material and routing operations, together with the associated indirect costs, and the quantity that is reported as finished.</span></span> <span data-ttu-id="e1f8b-115">次の 4 種類の差異が計算されます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-115">The following four types of variance are calculated:</span></span>

-   <span data-ttu-id="e1f8b-116">ロット サイズの差異</span><span class="sxs-lookup"><span data-stu-id="e1f8b-116">Lot size variance</span></span>
-   <span data-ttu-id="e1f8b-117">生産数量の差異</span><span class="sxs-lookup"><span data-stu-id="e1f8b-117">Production quantity variance</span></span>
-   <span data-ttu-id="e1f8b-118">生産価格差異</span><span class="sxs-lookup"><span data-stu-id="e1f8b-118">Production price variance</span></span>
-   <span data-ttu-id="e1f8b-119">生産代替の差異</span><span class="sxs-lookup"><span data-stu-id="e1f8b-119">Production substitution variance</span></span>

<span data-ttu-id="e1f8b-120">次の図に、製造オーダーの終了時の品目の原価レコード内の製造オーダーの実績原価と算出原価の差異を説明する 4 つの差異を示します。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-120">The following diagram shows the four variances that account for the difference between a production order's actual costs and the calculated costs within the item's cost record when the production order is ended.</span></span> 

![完了した製造オーダーの差異を説明する差異](./media/control.jpg) 

<span data-ttu-id="e1f8b-122">**差異** ページまたは **製造差異** レポートを使用して製造差異を分析できます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-122">You can analyze the production variances by using the **Variance** page or the **Production variance** report.</span></span> <span data-ttu-id="e1f8b-123">表示オプションを使用して、品目および運営リソース別または原価グループ別の詳細な差異を表示します。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-123">Use the display options to view detailed variances by item and operations resource, or by cost group.</span></span> <span data-ttu-id="e1f8b-124">在庫パラメータ内の原価内訳ポリシーは、差異が原価グループ別に追跡されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-124">The policy for cost breakdown in the inventory parameters determines whether the variances are tracked by cost group.</span></span> <span data-ttu-id="e1f8b-125">また、[**単一**]、[**複数**]、および [**合計**] 表示オプションを使用して、要約された差異を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-125">You can also use the **single**, **multi**, and **total** display options to view summarized variances.</span></span> <span data-ttu-id="e1f8b-126">詳細な差異に関する情報は、各差異のソースを理解するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-126">The information about detailed variances can help you understand the source of each variance.</span></span> <span data-ttu-id="e1f8b-127">製造オーダーが終了する前に差異を予期するには、[**原価見積**] レポートで提供される詳細情報を分析します。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-127">To predict variances before you end a production order, analyze the detailed information that is provided on the **Cost estimates and costings** report.</span></span>

## <a name="cost-analysis-for-current-production-orders"></a><span data-ttu-id="e1f8b-128">現在の製造オーダーに対する原価分析</span><span class="sxs-lookup"><span data-stu-id="e1f8b-128">Cost analysis for current production orders</span></span>
<span data-ttu-id="e1f8b-129">残りの 1 つのトランザクション タイプは、完了報告済品目を表します。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-129">Separate reports provide information about each type of transaction.</span></span> <span data-ttu-id="e1f8b-130">これらのレポートを使用して、報告済の生産活動の原価を分析できます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-130">Use these reports to analyze costs for reported production activities.</span></span> <span data-ttu-id="e1f8b-131">ステータスが [**開始済**] または [**完了報告済**] である現在の製造オーダーに関する情報のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-131">Information is displayed only for current production orders that have a status of **Started** or **Reported as finished**.</span></span>

-   <span data-ttu-id="e1f8b-132">**仕掛材料** − このレポートには、指定したトランザクション日付の時点で現在の製造オーダーに対して報告済のピッキング リスト トランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-132">**Materials in process** − This report lists the picking list transactions that are reported against the current production orders as of a specified transaction date.</span></span> <span data-ttu-id="e1f8b-133">このレポートには払い出されたコンポーネントの数量と原価金額がトランザクションごとに示されます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-133">The report indicates the quantity of a component that was issued and the cost amount for each transaction.</span></span> <span data-ttu-id="e1f8b-134">単一のコンポーネント品目の選択基準を使用します。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-134">Use the selection criteria for a single component item.</span></span> <span data-ttu-id="e1f8b-135">たとえば、適用される製造オーダーに対するそのコンポーネントの払出数量についての情報を出力できます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-135">For example, you can print information about the component’s issued quantity against applicable production orders.</span></span> <span data-ttu-id="e1f8b-136">払い出された数量は親品目の完了報告済数量によって更新されることはありません。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-136">The issued quantity isn't updated by the quantities that are reported as finished for the parent item.</span></span> <span data-ttu-id="e1f8b-137">したがって、仕掛原材料の実数量が多く表される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-137">Therefore, the actual quantity of raw materials in process might be overstated.</span></span>
-   <span data-ttu-id="e1f8b-138">**仕掛品** − このレポートには、指定したトランザクション日付の時点で現在の製造オーダーに対して報告済の工順トランザクション (または、ジョブ トランザクション) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-138">**Work in process** − This report lists route transactions (or job transactions) that are reported against the current production orders as of a specified transaction date.</span></span> <span data-ttu-id="e1f8b-139">このレポートは、トランザクションごとの報告済の時間、金額および数量 (適正数量と不良数量の両方) を示します。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-139">The report indicates the hours, amount, and quantity (both good quantity and error quantity) that are reported for each transaction.</span></span> <span data-ttu-id="e1f8b-140">また、工程番号、工程 ID、運営リソースなどの情報も含まれます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-140">It also includes information such as the operation number, operation ID, and operations resource.</span></span> <span data-ttu-id="e1f8b-141">また、レポートには、製造オーダーに対するすべてのトランザクションの合計時間と金額、および完了報告された数量も表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-141">Additionally, this report shows the total time and amount for all transactions against the production order, and the quantity that is reported as finished.</span></span>
-   <span data-ttu-id="e1f8b-142">[**処理中の間接原価**] − このレポートには、製造オーダーに対して発生した間接原価が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-142">**Indirect costs in process** − This report lists the indirect costs that have been incurred against production orders.</span></span> <span data-ttu-id="e1f8b-143">このデータは、指定したトランザクション日付の時点で報告済の工順工程およびコンポーネントに基づきます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-143">This data is based on reported consumption of routing operations and components as of a specified transaction date.</span></span> <span data-ttu-id="e1f8b-144">このレポートには間接原価のタイプ (割増金またはレート)、間接原価の原価計算表コード、および各トランザクションの原価金額が示されます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-144">The report indicates the type of indirect cost (surcharge or rate), the costing sheet code for the indirect cost, and the cost amount for each transaction.</span></span> <span data-ttu-id="e1f8b-145">このレポートには、間接原価を生成した工順カードまたはピッキング リストのトランザクションについての情報は示されません。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-145">This report doesn't provide information about the route card or pick list transaction that generated the indirect cost.</span></span>
-   <span data-ttu-id="e1f8b-146">[**処理中生産の原価計算**] − このレポートには、指定したトランザクション日付の時点での製造オーダーに対する材料消費、工順工程、および間接原価の組み合わせが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-146">**In process production costing** − This report lists the combined consumption of material, routing operations, and indirect cost against the production orders as of a specified transaction date.</span></span>
-   <span data-ttu-id="e1f8b-147">[**仕掛完成品目**] − このレポートには、指定したトランザクション日付の時点での、現在の製造オーダーと完了報告済トランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1f8b-147">**Finished items in process** − This report lists current production orders and the report-as-finished transactions as of a specified transaction date.</span></span>


<a name="see-also"></a><span data-ttu-id="e1f8b-148">参照</span><span class="sxs-lookup"><span data-stu-id="e1f8b-148">See also</span></span>
--------

[<span data-ttu-id="e1f8b-149">製造差異の一般的な発生源</span><span class="sxs-lookup"><span data-stu-id="e1f8b-149">Common sources of production variances</span></span>](common-sources-of-production-variances.md)




