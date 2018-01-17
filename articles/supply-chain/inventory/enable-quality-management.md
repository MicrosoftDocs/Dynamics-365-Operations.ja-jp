---
title: "品質管理の概要"
description: "このトピックは、Microsoft Dynamics 365 for Finance and Operations で品質管理を使用してサプライ チェーン内の製品の品質を向上させる方法について説明します。"
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 517ec53695ccf46f57bc1f379036d635c4fea24f
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="quality-management-overview"></a><span data-ttu-id="b6062-103">品質管理の概要</span><span class="sxs-lookup"><span data-stu-id="b6062-103">Quality management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b6062-104">このトピックは、Microsoft Dynamics 365 for Finance and Operations で品質管理を使用してサプライ チェーン内の製品の品質を向上させる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b6062-104">This topic describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="b6062-105">品質管理で、不適合製品を処理する際に原産地に関係なく応答時間を管理することができます。</span><span class="sxs-lookup"><span data-stu-id="b6062-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="b6062-106">診断タイプは修正レポートにリンクされているため、Microsoft Dynamics 365 for Finance および Operations では、問題を修正して再発を防ぐためのタスクをスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="b6062-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="b6062-107">不適合を管理するための機能に加えて、品質管理には、問題タイプ (内部の問題も含む) で問題を追跡し、短期または長期でソリューションを識別する機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b6062-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="b6062-108">主要業績評価指標 (KPI) に関する統計で、以前の不適合問題の履歴と修正に使用されたソリューションを分析できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="b6062-109">履歴データを使用して、以前の品質尺度の有効性を確認し、今後使用する適切な尺度を決定することができます。</span><span class="sxs-lookup"><span data-stu-id="b6062-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="b6062-110">品質関連を設定すると、Finance および Operations でさまざまな業務プロセス、イベントおよび条件の品質指示を生成できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="b6062-111">品質アソシエーションは、特定の品目、特定の品目のグループ、またはすべての品目をカバーできます。</span><span class="sxs-lookup"><span data-stu-id="b6062-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="b6062-112">品質管理の使用例</span><span class="sxs-lookup"><span data-stu-id="b6062-112">Examples of the use of quality management</span></span>
<span data-ttu-id="b6062-113">品質管理は柔軟で、サプライ チェーン工程の特定のレベルの要件を満たすさまざまな方法で実行できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="b6062-114">次の例では、これらの機能で可能な使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b6062-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="b6062-115">(特定の仕入先からの発注書の倉庫の登録の際に) 事前に定義された基準に基づいて品質テスト プロセスを自動的に開始します。</span><span class="sxs-lookup"><span data-stu-id="b6062-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="b6062-116">未承認の在庫が使用されないように検査中の在庫をブロックします (発注書数量の完全なブロック)。</span><span class="sxs-lookup"><span data-stu-id="b6062-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="b6062-117">検査しなければならない現在の現物在庫の数量を定義するために、品質関連の一部として品目サンプリングを使用します。</span><span class="sxs-lookup"><span data-stu-id="b6062-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="b6062-118">サンプリングは、固定数量または割合に基づいて設定できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="b6062-119">部分的な入庫の品質指示を作成します。</span><span class="sxs-lookup"><span data-stu-id="b6062-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="b6062-120">注文に対して現物入庫した数量の基準となる品質指示を作成するには、[品目サンプリング] フォームの [更新済数量別] チェック ボックスをオンにします</span><span class="sxs-lookup"><span data-stu-id="b6062-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="b6062-121">最小、最大とターゲットのテスト値を含むテスト タイプを作成し、事前に定義された検証結果がある定性試験と定量試験を実行します。</span><span class="sxs-lookup"><span data-stu-id="b6062-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="b6062-122">品質の測定許容を制御する許容可能な品質レベル (AQL) を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6062-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="b6062-123">テスト領域およびテスト機器といった検査の工程で必要とするリソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="b6062-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="b6062-124">品質アソシエーションの使用</span><span class="sxs-lookup"><span data-stu-id="b6062-124">Working with quality associations</span></span>
<span data-ttu-id="b6062-125">品質関連を使用する業務プロセスは、発注書、販売注文、または製造オーダーなどさまざまな元伝票に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b6062-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="b6062-126">それぞれの品質関連レコードでは、生成された品質指示に適用される一連のテスト、AQL、およびサンプリング計画が定義されます。</span><span class="sxs-lookup"><span data-stu-id="b6062-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="b6062-127">業務プロセスの各バリエーションごとに品質関連レコードを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="b6062-128">たとえば、購買注文製品受領書が更新されるときに、品質指示を生成する品質関連を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="b6062-129">実施計画の設定に応じて、未処理の品質指示がある場合、発生プロセス自体や、発注書の請求などの次のプロセスをブロックすることができます。</span><span class="sxs-lookup"><span data-stu-id="b6062-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="b6062-130">**注記:** 未処理の品質指示がある間は、在庫数量が発行されないように自動的にブロックされます。</span><span class="sxs-lookup"><span data-stu-id="b6062-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="b6062-131">**品目サンプリング** ページの [完全ブロック] 設定に応じて、発注書上の数量か、元伝票明細行の数量のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="b6062-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="b6062-132">指定された業務プロセスに対して、品質関連レコードにより、品質指示が生成されるイベントおよび条件が識別されます。</span><span class="sxs-lookup"><span data-stu-id="b6062-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="b6062-133">条件はサイトまたは法人の固有のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b6062-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="b6062-134">破壊試験を伴う品質指示は、イベントに必要な手持ち在庫が存在する場合にのみ生成できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="b6062-135">次の例は、業務プロセスの各変動に対して、品質アソシエーション レコードがどのように定義されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="b6062-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="b6062-136">次の表の例は、品質関連レコードによって定義されるイベントと条件の観点から要約されています。</span><span class="sxs-lookup"><span data-stu-id="b6062-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="b6062-137">参照タイプ</span><span class="sxs-lookup"><span data-stu-id="b6062-137">Reference type</span></span></th>
<th><span data-ttu-id="b6062-138">イベント タイプ</span><span class="sxs-lookup"><span data-stu-id="b6062-138">Event type</span></span></th>
<th><span data-ttu-id="b6062-139">実行</span><span class="sxs-lookup"><span data-stu-id="b6062-139">Execution</span></span></th>
<th><span data-ttu-id="b6062-140">イベント ブロック</span><span class="sxs-lookup"><span data-stu-id="b6062-140">Event blocking</span></span></th>
<th><span data-ttu-id="b6062-141">ドキュメントの参照</span><span class="sxs-lookup"><span data-stu-id="b6062-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b6062-142">棚卸資産</span><span class="sxs-lookup"><span data-stu-id="b6062-142">Inventory</span></span></td>
<td><span data-ttu-id="b6062-143">適用できません</span><span class="sxs-lookup"><span data-stu-id="b6062-143">Not applicable</span></span></td>
<td><span data-ttu-id="b6062-144">適用できません</span><span class="sxs-lookup"><span data-stu-id="b6062-144">Not applicable</span></span></td>
<td><span data-ttu-id="b6062-145">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-145">None</span></span></td>
<td><span data-ttu-id="b6062-146">すべて</span><span class="sxs-lookup"><span data-stu-id="b6062-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="b6062-147">販売注文</span><span class="sxs-lookup"><span data-stu-id="b6062-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="b6062-148">ピッキング プロセスがスケジュールされます</span><span class="sxs-lookup"><span data-stu-id="b6062-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="b6062-149">以前</span><span class="sxs-lookup"><span data-stu-id="b6062-149">Before</span></span></td>
<td><span data-ttu-id="b6062-150">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="b6062-151">固有 ID、グループ、またはすべてのみ。</span><span class="sxs-lookup"><span data-stu-id="b6062-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-152">ピッキング プロセス</span><span class="sxs-lookup"><span data-stu-id="b6062-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-153">梱包明細</span><span class="sxs-lookup"><span data-stu-id="b6062-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-154">請求書</span><span class="sxs-lookup"><span data-stu-id="b6062-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b6062-155">梱包明細</span><span class="sxs-lookup"><span data-stu-id="b6062-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="b6062-156">以前</span><span class="sxs-lookup"><span data-stu-id="b6062-156">Before</span></span></td>
<td><span data-ttu-id="b6062-157">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-158">梱包明細</span><span class="sxs-lookup"><span data-stu-id="b6062-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-159">請求書</span><span class="sxs-lookup"><span data-stu-id="b6062-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="b6062-160">購買</span><span class="sxs-lookup"><span data-stu-id="b6062-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="b6062-161">入庫リスト</span><span class="sxs-lookup"><span data-stu-id="b6062-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="b6062-162">以前</span><span class="sxs-lookup"><span data-stu-id="b6062-162">Before</span></span></td>
<td><span data-ttu-id="b6062-163">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-164">入庫リスト</span><span class="sxs-lookup"><span data-stu-id="b6062-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-165">製品受領書</span><span class="sxs-lookup"><span data-stu-id="b6062-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-166">請求書</span><span class="sxs-lookup"><span data-stu-id="b6062-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b6062-167">以後</span><span class="sxs-lookup"><span data-stu-id="b6062-167">After</span></span></td>
<td><span data-ttu-id="b6062-168">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-169">製品受領書</span><span class="sxs-lookup"><span data-stu-id="b6062-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-170">請求書</span><span class="sxs-lookup"><span data-stu-id="b6062-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b6062-171">登録</span><span class="sxs-lookup"><span data-stu-id="b6062-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="b6062-172">適用できません</span><span class="sxs-lookup"><span data-stu-id="b6062-172">Not applicable</span></span></td>
<td><span data-ttu-id="b6062-173">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-174">製品受領書</span><span class="sxs-lookup"><span data-stu-id="b6062-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-175">請求書</span><span class="sxs-lookup"><span data-stu-id="b6062-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b6062-176">製品受領書</span><span class="sxs-lookup"><span data-stu-id="b6062-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="b6062-177">以前</span><span class="sxs-lookup"><span data-stu-id="b6062-177">Before</span></span></td>
<td><span data-ttu-id="b6062-178">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-179">製品受領書</span><span class="sxs-lookup"><span data-stu-id="b6062-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-180">請求書</span><span class="sxs-lookup"><span data-stu-id="b6062-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b6062-181">以後</span><span class="sxs-lookup"><span data-stu-id="b6062-181">After</span></span></td>
<td><span data-ttu-id="b6062-182">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-183">請求書</span><span class="sxs-lookup"><span data-stu-id="b6062-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="b6062-184">運用</span><span class="sxs-lookup"><span data-stu-id="b6062-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="b6062-185">登録</span><span class="sxs-lookup"><span data-stu-id="b6062-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="b6062-186">適用できません</span><span class="sxs-lookup"><span data-stu-id="b6062-186">Not applicable</span></span></td>
<td><span data-ttu-id="b6062-187">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="b6062-188">すべて</span><span class="sxs-lookup"><span data-stu-id="b6062-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-189">完了レポート</span><span class="sxs-lookup"><span data-stu-id="b6062-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-190">終了日</span><span class="sxs-lookup"><span data-stu-id="b6062-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b6062-191">完了レポート</span><span class="sxs-lookup"><span data-stu-id="b6062-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="b6062-192">以前</span><span class="sxs-lookup"><span data-stu-id="b6062-192">Before</span></span></td>
<td><span data-ttu-id="b6062-193">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-194">完了レポート</span><span class="sxs-lookup"><span data-stu-id="b6062-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-195">終了日</span><span class="sxs-lookup"><span data-stu-id="b6062-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b6062-196">以後</span><span class="sxs-lookup"><span data-stu-id="b6062-196">After</span></span></td>
<td><span data-ttu-id="b6062-197">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-198">終了日</span><span class="sxs-lookup"><span data-stu-id="b6062-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="b6062-199">検査</span><span class="sxs-lookup"><span data-stu-id="b6062-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="b6062-200">完了レポート</span><span class="sxs-lookup"><span data-stu-id="b6062-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="b6062-201">以前</span><span class="sxs-lookup"><span data-stu-id="b6062-201">Before</span></span></td>
<td><span data-ttu-id="b6062-202">完了レポート</span><span class="sxs-lookup"><span data-stu-id="b6062-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-203">終了日</span><span class="sxs-lookup"><span data-stu-id="b6062-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-204">以後</span><span class="sxs-lookup"><span data-stu-id="b6062-204">After</span></span></td>
<td><span data-ttu-id="b6062-205">終了日</span><span class="sxs-lookup"><span data-stu-id="b6062-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-206">終了日</span><span class="sxs-lookup"><span data-stu-id="b6062-206">End</span></span></td>
<td><span data-ttu-id="b6062-207">以前</span><span class="sxs-lookup"><span data-stu-id="b6062-207">Before</span></span></td>
<td><span data-ttu-id="b6062-208">終了日</span><span class="sxs-lookup"><span data-stu-id="b6062-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b6062-209">工順工程</span><span class="sxs-lookup"><span data-stu-id="b6062-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="b6062-210">完了レポート</span><span class="sxs-lookup"><span data-stu-id="b6062-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="b6062-211">以前</span><span class="sxs-lookup"><span data-stu-id="b6062-211">Before</span></span></td>
<td><span data-ttu-id="b6062-212">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="b6062-213">固有 ID、グループ、またはすべて、およびリソース固有、グループ、またはすべて</span><span class="sxs-lookup"><span data-stu-id="b6062-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-214">完了レポート</span><span class="sxs-lookup"><span data-stu-id="b6062-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-215">以後</span><span class="sxs-lookup"><span data-stu-id="b6062-215">After</span></span></td>
<td><span data-ttu-id="b6062-216">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b6062-217">連産品の生産</span><span class="sxs-lookup"><span data-stu-id="b6062-217">Co-product production</span></span></td>
<td><span data-ttu-id="b6062-218">登録</span><span class="sxs-lookup"><span data-stu-id="b6062-218">Registration</span></span></td>
<td><span data-ttu-id="b6062-219">適用できません</span><span class="sxs-lookup"><span data-stu-id="b6062-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b6062-220">なし</span><span class="sxs-lookup"><span data-stu-id="b6062-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="b6062-221">すべて</span><span class="sxs-lookup"><span data-stu-id="b6062-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b6062-222">完了レポート</span><span class="sxs-lookup"><span data-stu-id="b6062-222">Report as finished</span></span></td>
<td><span data-ttu-id="b6062-223">以前</span><span class="sxs-lookup"><span data-stu-id="b6062-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-224">以後</span><span class="sxs-lookup"><span data-stu-id="b6062-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6062-225">次の表に、品質指示をプロセスの特定のタイプに対して生成する方法の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="b6062-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="b6062-226">プロセスのタイプ</span><span class="sxs-lookup"><span data-stu-id="b6062-226">Type of process</span></span></th>
<th><span data-ttu-id="b6062-227">品質指示を自動的に生成できる場合</span><span class="sxs-lookup"><span data-stu-id="b6062-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="b6062-228">破壊試験が必要な場合に品質指示を生成できる場合</span><span class="sxs-lookup"><span data-stu-id="b6062-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="b6062-229">条件の情報</span><span class="sxs-lookup"><span data-stu-id="b6062-229">Condition information</span></span></th>
<th><span data-ttu-id="b6062-230">手動生成情報</span><span class="sxs-lookup"><span data-stu-id="b6062-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b6062-231">発注書</span><span class="sxs-lookup"><span data-stu-id="b6062-231">Purchase order</span></span></td>
<td><span data-ttu-id="b6062-232">受領した材料の受領書リストまたは製品受領書の転記前または転記後</span><span class="sxs-lookup"><span data-stu-id="b6062-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="b6062-233">材料は破壊試験に利用できる必要があるために、受領した材料の製品受領書が転記された後</span><span class="sxs-lookup"><span data-stu-id="b6062-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="b6062-234">品質指示の要求は、特定のサイト、品目、仕入先、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b6062-235">発注書を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-236">検査指示</span><span class="sxs-lookup"><span data-stu-id="b6062-236">Quarantine order</span></span></td>
<td><span data-ttu-id="b6062-237">検査指示が完了済みまたは終了と報告される前または後</span><span class="sxs-lookup"><span data-stu-id="b6062-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="b6062-238">破壊試験を必要とする品質指示は生成することができません。</span><span class="sxs-lookup"><span data-stu-id="b6062-238">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="b6062-239">検査指示機能が、破壊される材料の破棄を扱うと仮定します。</span><span class="sxs-lookup"><span data-stu-id="b6062-239">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="b6062-240">品質指示の要求は、特定のサイト、品目、仕入先、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b6062-241">検査指示を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-242">販売注文</span><span class="sxs-lookup"><span data-stu-id="b6062-242">Sales order</span></span></td>
<td><span data-ttu-id="b6062-243">出荷する品目のスケジュールされたピッキング プロセスまたは梱包明細を更新する前</span><span class="sxs-lookup"><span data-stu-id="b6062-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="b6062-244">任意のステップ</span><span class="sxs-lookup"><span data-stu-id="b6062-244">At any step</span></span></td>
<td><span data-ttu-id="b6062-245">品質指示の要求は、特定のサイト、品目、顧客、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b6062-246">販売注文を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-247">製造オーダー</span><span class="sxs-lookup"><span data-stu-id="b6062-247">Production order</span></span></td>
<td><span data-ttu-id="b6062-248">製造オーダーの完了済数量の報告前または後</span><span class="sxs-lookup"><span data-stu-id="b6062-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="b6062-249">製造オーダーの完了済数量の報告後</span><span class="sxs-lookup"><span data-stu-id="b6062-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="b6062-250">品質指示の要求は、特定のサイト、品目、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b6062-251">製造オーダーを参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-252">工順工程を持つ製造オーダー</span><span class="sxs-lookup"><span data-stu-id="b6062-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="b6062-253">操作のレポート終了前または後</span><span class="sxs-lookup"><span data-stu-id="b6062-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="b6062-254">最後の操作のレポート生産終了後</span><span class="sxs-lookup"><span data-stu-id="b6062-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="b6062-255">品質指示の要求は、特定のサイト、品目、運営リソース、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b6062-256">工順工程を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質関連レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6062-257">棚卸資産</span><span class="sxs-lookup"><span data-stu-id="b6062-257">Inventory</span></span></td>
<td><span data-ttu-id="b6062-258">在庫仕訳帳のトランザクションまたは移動オーダー トランザクションに対して、品質指示を自動的に生成することはできません。</span><span class="sxs-lookup"><span data-stu-id="b6062-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="b6062-259">品質指示は、品目の在庫数量に対して手動で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-259">A quality order must be created manually for an item's inventory quantity.</span></span> <span data-ttu-id="b6062-260">現物手持在庫は必須です。</span><span class="sxs-lookup"><span data-stu-id="b6062-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="b6062-261">品質管理ページ</span><span class="sxs-lookup"><span data-stu-id="b6062-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6062-262">ページ</span><span class="sxs-lookup"><span data-stu-id="b6062-262">Page</span></span></th>
<th><span data-ttu-id="b6062-263">説明</span><span class="sxs-lookup"><span data-stu-id="b6062-263">Description</span></span></th>
<th><span data-ttu-id="b6062-264">例</span><span class="sxs-lookup"><span data-stu-id="b6062-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6062-265">品質関連</span><span class="sxs-lookup"><span data-stu-id="b6062-265">Quality associations</span></span></td>
<td><span data-ttu-id="b6062-266">この記事の前のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6062-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="b6062-267">品質関連は、生成された品質指示に対する次のすべての情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="b6062-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="b6062-268">トランザクション イベント</span><span class="sxs-lookup"><span data-stu-id="b6062-268">The transaction event</span></span></li>
<li><span data-ttu-id="b6062-269">品目に実行する必要がある一連のテスト</span><span class="sxs-lookup"><span data-stu-id="b6062-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="b6062-270">AQL</span><span class="sxs-lookup"><span data-stu-id="b6062-270">The AQL</span></span></li>
<li><span data-ttu-id="b6062-271">サンプリング計画</span><span class="sxs-lookup"><span data-stu-id="b6062-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="b6062-272">品質指示の自動生成を必要とする業務プロセスの各バリエーションごとに品質アソシエーションを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-272">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="b6062-273">たとえば、品質指示は、発注書、検査指示、販売注文、および製造オーダーの業務プロセスで生成することができます。</span><span class="sxs-lookup"><span data-stu-id="b6062-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6062-274">テスト</span><span class="sxs-lookup"><span data-stu-id="b6062-274">Tests</span></span></td>
<td><span data-ttu-id="b6062-275">このページを使用して、製品が品質仕様を満たすかどうかを決定する個別のテストを定義して表示できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="b6062-276">テスト グループに 1 つ以上の個別のテストを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b6062-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="b6062-277">この場合、許容測定値などのテスト固有の情報も指定します。</span><span class="sxs-lookup"><span data-stu-id="b6062-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="b6062-278">測定値は、定量試験に使用され、テスト変数は、定性試験に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6062-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="b6062-279">定量試験には、<strong>整数</strong>または<strong>分数</strong>のテスト タイプがあり、指定された測定単位もあります。</span><span class="sxs-lookup"><span data-stu-id="b6062-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="b6062-280">品質仕様とテスト結果が数字で示されます。</span><span class="sxs-lookup"><span data-stu-id="b6062-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="b6062-281">定性試験では、テスト タイプを [<strong>オプション</strong>] として定義します。</span><span class="sxs-lookup"><span data-stu-id="b6062-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="b6062-282">定性試験では、測定されるテスト変数と列挙されたオプションに関する追加情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="b6062-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="b6062-283">品質仕様とテスト結果が結果に応じて示されます。</span><span class="sxs-lookup"><span data-stu-id="b6062-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="b6062-284">ある製造会社では、購入した材料に対して 2 種類のテストを行います。材料品質に関する定量試験と、梱包破損に関する定性試験です。</span><span class="sxs-lookup"><span data-stu-id="b6062-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="b6062-285">定性試験に関して、テスト変数 (破損した梱包) とその結果を識別する追加情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="b6062-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="b6062-286"><strong>テスト グループ</strong> ページを使用して、これら 2 つのテストを 1 つのテスト グループに割り当て、テスト固有の情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6062-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="b6062-287">2 つのテストの結果をレポートできるよう、テスト グループを品質指示に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b6062-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6062-288">テスト グループ</span><span class="sxs-lookup"><span data-stu-id="b6062-288">Test groups</span></span></td>
<td><span data-ttu-id="b6062-289">テスト グループと、テスト グループに割り当てられる個別のテストを設定、編集、および表示するには、このページを使用します。</span><span class="sxs-lookup"><span data-stu-id="b6062-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="b6062-290">上部ウィンドウにはテスト グループが表示され、下部ウィンドウには選択したテスト グループに割り当てられるテストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b6062-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="b6062-291">テスト グループには、サンプリング計画、AQL、破壊試験の要件などの複数のポリシーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b6062-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="b6062-292">個別のテストをテスト グループに割り当てるときは、順序、ドキュメント、有効期間などの追加情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="b6062-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="b6062-293">定量試験の場合、定義する情報には許容測定値も含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6062-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="b6062-294">定性試験の場合、情報にはテスト変数と既定の結果が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6062-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="b6062-295">品質指示に割り当てるテスト グループは、指定された品目に対して実行する必要がある既定のテストのセットを定義します。</span><span class="sxs-lookup"><span data-stu-id="b6062-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="b6062-296">ただし、品質指示のテストは、追加、削除、または変更できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="b6062-297">テスト結果のレポートは、品質指示に対するそれぞれのテストに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="b6062-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="b6062-298">ある製造会社では、品質ガイドラインのバリエーションごとにテスト グループを定義します。</span><span class="sxs-lookup"><span data-stu-id="b6062-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="b6062-299">さまざまなテスト グループは、サンプリング計画、まとめて実行する必要があるテストのセット、AQL、およびその他の要因における違いを反映します。</span><span class="sxs-lookup"><span data-stu-id="b6062-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="b6062-300">定量試験の場合、許容測定値にも違いがあります。</span><span class="sxs-lookup"><span data-stu-id="b6062-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="b6062-301">品質ガイドラインを適用するために、この会社では、<strong>品質関連</strong>ページで各ルールにテスト グループを割り当てて品質指示を自動的に生成し、また手動で作成された品質指示にテスト グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b6062-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6062-302">品目品質グループ</span><span class="sxs-lookup"><span data-stu-id="b6062-302">Item quality groups</span></span></td>
<td><span data-ttu-id="b6062-303">品質グループに割り当てられる品目、または品目に割り当てられる品質グループを、設定、編集、および表示するには、このページを使用します。</span><span class="sxs-lookup"><span data-stu-id="b6062-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="b6062-304">品質グループとは、複数の品目に共通するテスト要件です。</span><span class="sxs-lookup"><span data-stu-id="b6062-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="b6062-305"><strong>テスト グループ</strong> ページのテスト要件を定義した後、品質指示を自動生成するルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="b6062-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="b6062-306">プロセスを簡略化するために、個別の品目のルールを定義しません。</span><span class="sxs-lookup"><span data-stu-id="b6062-306">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="b6062-307">代わりに、<strong>品質関連</strong>ページを使用して品質グループのルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="b6062-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="b6062-308">選択した品質グループの<strong>品目品質グループ</strong> ページを使用して、そのグループに関連品目を割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="b6062-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="b6062-309">選択した品目の<strong>品目品質グループ</strong> ページを使用して、その品目に関連品質グループを割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="b6062-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="b6062-310">ある製造会社で、受入検査に同じテスト要件があるさまざまな原材料を購入しています。</span><span class="sxs-lookup"><span data-stu-id="b6062-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="b6062-311">その会社では、品質グループを定義し、そのグループに原材料と関連付けた品目番号を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b6062-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="b6062-312">後で、同じテスト要件がある新しいタイプの原材料を購入します。</span><span class="sxs-lookup"><span data-stu-id="b6062-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="b6062-313">新しい材料の新しいテスト要件を設定せずに、既存の品質グループに新しい材料の品目番号を追加します。</span><span class="sxs-lookup"><span data-stu-id="b6062-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="b6062-314">また、この製造会社では、同じ製造テスト要件の品目を製造し、同じ要件で出荷前テストを実行して品目を出荷しています。</span><span class="sxs-lookup"><span data-stu-id="b6062-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="b6062-315">この会社は、さらに 2 つの品質グループを定義し、各グループに関連品目番号を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b6062-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6062-316">テスト変数</span><span class="sxs-lookup"><span data-stu-id="b6062-316">Test variables</span></span></td>
<td><span data-ttu-id="b6062-317">定性試験に関連付けられている変数を定義または表示するには、このページを使用します。</span><span class="sxs-lookup"><span data-stu-id="b6062-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="b6062-318">各変数には、選択できるオプションを表す列挙された結果を定義します。</span><span class="sxs-lookup"><span data-stu-id="b6062-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="b6062-319"><strong>テスト</strong> ページでテストを定義します。</span><span class="sxs-lookup"><span data-stu-id="b6062-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="b6062-320">定性試験では、テスト タイプを [<strong>オプション</strong>] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="b6062-321"><strong>テスト グループ</strong> ページを使用して個別のテストにテスト変数を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b6062-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="b6062-322">クッキーを製造しているある製造会社では、完成した製品の検査テストを採用しています。</span><span class="sxs-lookup"><span data-stu-id="b6062-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="b6062-323">この検査テストには、複数の変数があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-323">This inspection test has several variables.</span></span> <span data-ttu-id="b6062-324">1 つ目の変数は味で、この変数に対して発生する可能性がある結果は、良および不良です。</span><span class="sxs-lookup"><span data-stu-id="b6062-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="b6062-325">2 つ目の変数は色で、発生する可能性がある結果は、濃すぎる、薄すぎる、および適正です。</span><span class="sxs-lookup"><span data-stu-id="b6062-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6062-326">テスト変数の結果</span><span class="sxs-lookup"><span data-stu-id="b6062-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="b6062-327">定性試験に関連付けられているテスト変数について、発生する可能性があるテスト結果を設定、編集、および表示するには、このページを使用します。</span><span class="sxs-lookup"><span data-stu-id="b6062-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="b6062-328">それぞれの結果について、<strong>合格</strong>または<strong>不合格</strong>のステータスを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b6062-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="b6062-329"><strong>テスト</strong> ページで定義した各定性試験に対する変数とその結果を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="b6062-330">(定性試験の場合、テスト タイプは、<strong>テスト</strong> ページで [<strong>オプション</strong>] に設定されます)。個々の定性試験にテスト変数と既定の結果を割り当てるには、<strong>テスト グループ</strong> ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="b6062-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="b6062-331">クッキーを製造しているある製造会社では、完成した製品の検査テストを採用しています。</span><span class="sxs-lookup"><span data-stu-id="b6062-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="b6062-332">この検査テストには、複数の変数があります。</span><span class="sxs-lookup"><span data-stu-id="b6062-332">This inspection test has of several variables.</span></span> <span data-ttu-id="b6062-333">1 つ目の変数は味で、この変数に対して発生する可能性がある結果は、良および不良です。</span><span class="sxs-lookup"><span data-stu-id="b6062-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="b6062-334">2 つ目の変数は色で、発生する可能性がある結果は、濃すぎる、薄すぎる、および適正です。</span><span class="sxs-lookup"><span data-stu-id="b6062-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="b6062-335">それぞれの結果に<strong>合格</strong>または<strong>不合格</strong>のステータスが割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="b6062-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="b6062-336">各変数の検査テスト時に、検査官はいずれかの結果を選択することによってテスト結果を報告します。</span><span class="sxs-lookup"><span data-stu-id="b6062-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="b6062-337">参照</span><span class="sxs-lookup"><span data-stu-id="b6062-337">See also</span></span>
--------

[<span data-ttu-id="b6062-338">品質管理プロセス</span><span class="sxs-lookup"><span data-stu-id="b6062-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="b6062-339">不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="b6062-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)

