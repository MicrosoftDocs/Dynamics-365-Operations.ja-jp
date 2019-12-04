---
title: 品質管理の概要
description: このトピックでは、Dynamics 365 Supply Chain Management で品質管理を使用してサプライ チェーン内の製品の品質を向上させる方法について説明します。
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2d51c659d9d06f075458359d81de978e7a6d14b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814401"
---
# <a name="quality-management-overview"></a><span data-ttu-id="7a35d-103">品質管理の概要</span><span class="sxs-lookup"><span data-stu-id="7a35d-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a35d-104">このトピックでは、Dynamics 365 Supply Chain Management で品質管理を使用してサプライ チェーン内の製品の品質を向上させる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="7a35d-105">品質管理で、不適合製品を処理する際に原産地に関係なく応答時間を管理することができます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="7a35d-106">診断タイプは修正レポートにリンクされているため、Supply Chain Management では、問題を修正して再発を防ぐためのタスクをスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="7a35d-107">不適合を管理するための機能に加えて、品質管理には、問題タイプ (内部の問題も含む) で問題を追跡し、短期または長期でソリューションを識別する機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a35d-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="7a35d-108">主要業績評価指標 (KPI) に関する統計で、以前の不適合問題の履歴と修正に使用されたソリューションを分析できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="7a35d-109">履歴データを使用して、以前の品質尺度の有効性を確認し、今後使用する適切な尺度を決定することができます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="7a35d-110">品質関連を設定すると、Supply Chain Management でさまざまな業務プロセス、イベントおよび条件の品質指示を生成できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="7a35d-111">品質アソシエーションは、特定の品目、特定の品目のグループ、またはすべての品目をカバーできます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="7a35d-112">品質管理の使用例</span><span class="sxs-lookup"><span data-stu-id="7a35d-112">Examples of the use of quality management</span></span>
<span data-ttu-id="7a35d-113">品質管理は柔軟で、サプライ チェーン工程の特定のレベルの要件を満たすさまざまな方法で実行できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="7a35d-114">次の例では、これらの機能で可能な使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="7a35d-115">(特定の仕入先からの発注書の倉庫の登録の際に) 事前に定義された基準に基づいて品質テスト プロセスを自動的に開始します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="7a35d-116">未承認の在庫が使用されないように検査中の在庫をブロックします (発注書数量の完全なブロック)。</span><span class="sxs-lookup"><span data-stu-id="7a35d-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="7a35d-117">検査しなければならない現在の現物在庫の数量を定義するために、品質関連の一部として品目サンプリングを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="7a35d-118">サンプリングは、固定数量または割合に基づいて設定できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="7a35d-119">部分的な入庫の品質指示を作成します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="7a35d-120">注文に対して現物入庫した数量の基準となる品質指示を作成するには、**品目サンプリング**フォームの**更新済数量別**チェック ボックスをオンにします</span><span class="sxs-lookup"><span data-stu-id="7a35d-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="7a35d-121">最小、最大とターゲットのテスト値を含むテスト タイプを作成し、事前に定義された検証結果がある定性試験と定量試験を実行します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="7a35d-122">品質の測定許容を制御する許容可能な品質レベル (AQL) を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="7a35d-123">テスト領域およびテスト機器といった検査の工程で必要とするリソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="7a35d-124">品質アソシエーションの使用</span><span class="sxs-lookup"><span data-stu-id="7a35d-124">Working with quality associations</span></span>
<span data-ttu-id="7a35d-125">品質関連を使用する業務プロセスは、発注書、販売注文、または製造オーダーなどさまざまな元伝票に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="7a35d-126">それぞれの品質関連レコードでは、生成された品質指示に適用される一連のテスト、AQL、およびサンプリング計画が定義されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="7a35d-127">業務プロセスの各バリエーションごとに品質関連レコードを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="7a35d-128">たとえば、購買注文製品受領書が更新されるときに、品質指示を生成する品質関連を設定できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="7a35d-129">実施計画の設定に応じて、未処理の品質指示がある場合、発生プロセス自体や、発注書の請求などの次のプロセスをブロックすることができます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="7a35d-130">**注記:** 未処理の品質指示がある間は、在庫数量が発行されないように自動的にブロックされます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="7a35d-131">**品目サンプリング** ページの**完全ブロック**設定に応じて、発注書上の数量か、元伝票明細行の数量のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="7a35d-132">指定された業務プロセスに対して、品質関連レコードにより、品質指示が生成されるイベントおよび条件が識別されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="7a35d-133">条件はサイトまたは法人の固有のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="7a35d-134">破壊試験を伴う品質指示は、イベントに必要な手持ち在庫が存在する場合にのみ生成できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="7a35d-135">次の例は、業務プロセスの各変動に対して、品質アソシエーション レコードがどのように定義されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="7a35d-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="7a35d-136">次の表の例は、品質関連レコードによって定義されるイベントと条件の観点から要約されています。</span><span class="sxs-lookup"><span data-stu-id="7a35d-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="7a35d-137">参照タイプ</span><span class="sxs-lookup"><span data-stu-id="7a35d-137">Reference type</span></span></th>
<th><span data-ttu-id="7a35d-138">イベント タイプ</span><span class="sxs-lookup"><span data-stu-id="7a35d-138">Event type</span></span></th>
<th><span data-ttu-id="7a35d-139">実行</span><span class="sxs-lookup"><span data-stu-id="7a35d-139">Execution</span></span></th>
<th><span data-ttu-id="7a35d-140">イベント ブロック</span><span class="sxs-lookup"><span data-stu-id="7a35d-140">Event blocking</span></span></th>
<th><span data-ttu-id="7a35d-141">ドキュメントの参照</span><span class="sxs-lookup"><span data-stu-id="7a35d-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="7a35d-142">棚卸資産</span><span class="sxs-lookup"><span data-stu-id="7a35d-142">Inventory</span></span></td>
<td><span data-ttu-id="7a35d-143">適用できません</span><span class="sxs-lookup"><span data-stu-id="7a35d-143">Not applicable</span></span></td>
<td><span data-ttu-id="7a35d-144">適用できません</span><span class="sxs-lookup"><span data-stu-id="7a35d-144">Not applicable</span></span></td>
<td><span data-ttu-id="7a35d-145">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-145">None</span></span></td>
<td><span data-ttu-id="7a35d-146">すべて</span><span class="sxs-lookup"><span data-stu-id="7a35d-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="7a35d-147">販売注文</span><span class="sxs-lookup"><span data-stu-id="7a35d-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="7a35d-148">ピッキング プロセスがスケジュールされます</span><span class="sxs-lookup"><span data-stu-id="7a35d-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="7a35d-149">以前</span><span class="sxs-lookup"><span data-stu-id="7a35d-149">Before</span></span></td>
<td><span data-ttu-id="7a35d-150">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="7a35d-151">固有 ID、グループ、またはすべてのみ。</span><span class="sxs-lookup"><span data-stu-id="7a35d-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-152">ピッキング プロセス</span><span class="sxs-lookup"><span data-stu-id="7a35d-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-153">梱包明細</span><span class="sxs-lookup"><span data-stu-id="7a35d-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-154">請求書</span><span class="sxs-lookup"><span data-stu-id="7a35d-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7a35d-155">梱包明細</span><span class="sxs-lookup"><span data-stu-id="7a35d-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="7a35d-156">以前</span><span class="sxs-lookup"><span data-stu-id="7a35d-156">Before</span></span></td>
<td><span data-ttu-id="7a35d-157">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-158">梱包明細</span><span class="sxs-lookup"><span data-stu-id="7a35d-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-159">請求書</span><span class="sxs-lookup"><span data-stu-id="7a35d-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="7a35d-160">購買</span><span class="sxs-lookup"><span data-stu-id="7a35d-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="7a35d-161">入庫リスト</span><span class="sxs-lookup"><span data-stu-id="7a35d-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="7a35d-162">以前</span><span class="sxs-lookup"><span data-stu-id="7a35d-162">Before</span></span></td>
<td><span data-ttu-id="7a35d-163">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-164">入庫リスト</span><span class="sxs-lookup"><span data-stu-id="7a35d-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-165">製品受領書</span><span class="sxs-lookup"><span data-stu-id="7a35d-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-166">請求書</span><span class="sxs-lookup"><span data-stu-id="7a35d-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7a35d-167">以後</span><span class="sxs-lookup"><span data-stu-id="7a35d-167">After</span></span></td>
<td><span data-ttu-id="7a35d-168">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-169">製品受領書</span><span class="sxs-lookup"><span data-stu-id="7a35d-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-170">請求書</span><span class="sxs-lookup"><span data-stu-id="7a35d-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7a35d-171">登録</span><span class="sxs-lookup"><span data-stu-id="7a35d-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="7a35d-172">適用できません</span><span class="sxs-lookup"><span data-stu-id="7a35d-172">Not applicable</span></span></td>
<td><span data-ttu-id="7a35d-173">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-174">製品受領書</span><span class="sxs-lookup"><span data-stu-id="7a35d-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-175">請求書</span><span class="sxs-lookup"><span data-stu-id="7a35d-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="7a35d-176">製品受領書</span><span class="sxs-lookup"><span data-stu-id="7a35d-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="7a35d-177">以前</span><span class="sxs-lookup"><span data-stu-id="7a35d-177">Before</span></span></td>
<td><span data-ttu-id="7a35d-178">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-179">製品受領書</span><span class="sxs-lookup"><span data-stu-id="7a35d-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-180">請求書</span><span class="sxs-lookup"><span data-stu-id="7a35d-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7a35d-181">以後</span><span class="sxs-lookup"><span data-stu-id="7a35d-181">After</span></span></td>
<td><span data-ttu-id="7a35d-182">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-183">請求書</span><span class="sxs-lookup"><span data-stu-id="7a35d-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="7a35d-184">運用</span><span class="sxs-lookup"><span data-stu-id="7a35d-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="7a35d-185">登録</span><span class="sxs-lookup"><span data-stu-id="7a35d-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="7a35d-186">適用できません</span><span class="sxs-lookup"><span data-stu-id="7a35d-186">Not applicable</span></span></td>
<td><span data-ttu-id="7a35d-187">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="7a35d-188">すべて</span><span class="sxs-lookup"><span data-stu-id="7a35d-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-189">完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-190">終了日</span><span class="sxs-lookup"><span data-stu-id="7a35d-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="7a35d-191">完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="7a35d-192">以前</span><span class="sxs-lookup"><span data-stu-id="7a35d-192">Before</span></span></td>
<td><span data-ttu-id="7a35d-193">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-194">完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-195">終了日</span><span class="sxs-lookup"><span data-stu-id="7a35d-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7a35d-196">以後</span><span class="sxs-lookup"><span data-stu-id="7a35d-196">After</span></span></td>
<td><span data-ttu-id="7a35d-197">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-198">終了日</span><span class="sxs-lookup"><span data-stu-id="7a35d-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="7a35d-199">検査</span><span class="sxs-lookup"><span data-stu-id="7a35d-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="7a35d-200">完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="7a35d-201">以前</span><span class="sxs-lookup"><span data-stu-id="7a35d-201">Before</span></span></td>
<td><span data-ttu-id="7a35d-202">完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-203">終了日</span><span class="sxs-lookup"><span data-stu-id="7a35d-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-204">以後</span><span class="sxs-lookup"><span data-stu-id="7a35d-204">After</span></span></td>
<td><span data-ttu-id="7a35d-205">終了日</span><span class="sxs-lookup"><span data-stu-id="7a35d-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-206">終了日</span><span class="sxs-lookup"><span data-stu-id="7a35d-206">End</span></span></td>
<td><span data-ttu-id="7a35d-207">以前</span><span class="sxs-lookup"><span data-stu-id="7a35d-207">Before</span></span></td>
<td><span data-ttu-id="7a35d-208">終了日</span><span class="sxs-lookup"><span data-stu-id="7a35d-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7a35d-209">工順工程</span><span class="sxs-lookup"><span data-stu-id="7a35d-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="7a35d-210">完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="7a35d-211">以前</span><span class="sxs-lookup"><span data-stu-id="7a35d-211">Before</span></span></td>
<td><span data-ttu-id="7a35d-212">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="7a35d-213">固有 ID、グループ、またはすべて、およびリソース固有、グループ、またはすべて</span><span class="sxs-lookup"><span data-stu-id="7a35d-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-214">完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-215">以後</span><span class="sxs-lookup"><span data-stu-id="7a35d-215">After</span></span></td>
<td><span data-ttu-id="7a35d-216">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7a35d-217">連産品の生産</span><span class="sxs-lookup"><span data-stu-id="7a35d-217">Co-product production</span></span></td>
<td><span data-ttu-id="7a35d-218">登録</span><span class="sxs-lookup"><span data-stu-id="7a35d-218">Registration</span></span></td>
<td><span data-ttu-id="7a35d-219">適用できません</span><span class="sxs-lookup"><span data-stu-id="7a35d-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7a35d-220">なし</span><span class="sxs-lookup"><span data-stu-id="7a35d-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="7a35d-221">すべて</span><span class="sxs-lookup"><span data-stu-id="7a35d-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7a35d-222">完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-222">Report as finished</span></span></td>
<td><span data-ttu-id="7a35d-223">以前</span><span class="sxs-lookup"><span data-stu-id="7a35d-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-224">以後</span><span class="sxs-lookup"><span data-stu-id="7a35d-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a35d-225">次の表に、品質指示をプロセスの特定のタイプに対して生成する方法の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="7a35d-226">プロセスのタイプ</span><span class="sxs-lookup"><span data-stu-id="7a35d-226">Type of process</span></span></th>
<th><span data-ttu-id="7a35d-227">品質指示を自動的に生成できる場合</span><span class="sxs-lookup"><span data-stu-id="7a35d-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="7a35d-228">破壊試験が必要な場合に品質指示を生成できる場合</span><span class="sxs-lookup"><span data-stu-id="7a35d-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="7a35d-229">条件の情報</span><span class="sxs-lookup"><span data-stu-id="7a35d-229">Condition information</span></span></th>
<th><span data-ttu-id="7a35d-230">手動生成情報</span><span class="sxs-lookup"><span data-stu-id="7a35d-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="7a35d-231">発注書</span><span class="sxs-lookup"><span data-stu-id="7a35d-231">Purchase order</span></span></td>
<td><span data-ttu-id="7a35d-232">受領した材料の受領書リストまたは製品受領書の転記前または転記後</span><span class="sxs-lookup"><span data-stu-id="7a35d-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="7a35d-233">材料は破壊試験に利用できる必要があるために、受領した材料の製品受領書が転記された後</span><span class="sxs-lookup"><span data-stu-id="7a35d-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="7a35d-234">品質指示の要求は、特定のサイト、品目、仕入先、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="7a35d-235">発注書を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-236">検査指示</span><span class="sxs-lookup"><span data-stu-id="7a35d-236">Quarantine order</span></span></td>
<td><span data-ttu-id="7a35d-237">検査指示が完了済みまたは終了と報告される前または後</span><span class="sxs-lookup"><span data-stu-id="7a35d-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="7a35d-238">破壊試験を必要とする品質指示は生成することができません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="7a35d-239">検査指示機能が、破壊される材料の破棄を扱うと仮定します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="7a35d-240">品質指示の要求は、特定のサイト、品目、仕入先、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="7a35d-241">検査指示を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-242">販売注文</span><span class="sxs-lookup"><span data-stu-id="7a35d-242">Sales order</span></span></td>
<td><span data-ttu-id="7a35d-243">出荷する品目のスケジュールされたピッキング プロセスまたは梱包明細を更新する前</span><span class="sxs-lookup"><span data-stu-id="7a35d-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="7a35d-244">任意のステップ</span><span class="sxs-lookup"><span data-stu-id="7a35d-244">At any step</span></span></td>
<td><span data-ttu-id="7a35d-245">品質指示の要求は、特定のサイト、品目、顧客、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="7a35d-246">販売注文を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-247">製造オーダー</span><span class="sxs-lookup"><span data-stu-id="7a35d-247">Production order</span></span></td>
<td><span data-ttu-id="7a35d-248">製造オーダーの完了済数量の報告前または後</span><span class="sxs-lookup"><span data-stu-id="7a35d-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="7a35d-249">製造オーダーの完了済数量の報告後</span><span class="sxs-lookup"><span data-stu-id="7a35d-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="7a35d-250">品質指示の要求は、特定のサイト、品目、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="7a35d-251">製造オーダーを参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-252">工順工程を持つ製造オーダー</span><span class="sxs-lookup"><span data-stu-id="7a35d-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="7a35d-253">操作のレポート終了前または後</span><span class="sxs-lookup"><span data-stu-id="7a35d-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="7a35d-254">最後の操作のレポート生産終了後</span><span class="sxs-lookup"><span data-stu-id="7a35d-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="7a35d-255">品質指示の要求は、特定のサイト、品目、運営リソース、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="7a35d-256">工順工程を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質関連レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-257">棚卸資産</span><span class="sxs-lookup"><span data-stu-id="7a35d-257">Inventory</span></span></td>
<td><span data-ttu-id="7a35d-258">在庫仕訳帳のトランザクションまたは移動オーダー トランザクションに対して、品質指示を自動的に生成することはできません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="7a35d-259">品質指示は、品目の在庫数量に対して手動で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="7a35d-260">現物手持在庫は必須です。</span><span class="sxs-lookup"><span data-stu-id="7a35d-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="7a35d-261">品質指示の自動生成の例</span><span class="sxs-lookup"><span data-stu-id="7a35d-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="7a35d-262">購買</span><span class="sxs-lookup"><span data-stu-id="7a35d-262">Purchasing</span></span>

<span data-ttu-id="7a35d-263">購買で、**品質関連**ページで**イベント タイプ** フィールドを**製品受領書**に、**実行**フィールドを**変更後**に設定すると、次のような結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="7a35d-264">**更新済数量別**オプションが**はい**に設定されると、品目サンプリングの入庫済数量と設定に基づいて、発注書に対するすべての入荷の品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="7a35d-265">発注書に対する数量が入荷されるたびに、新しく入荷した数量に基づいて新しい品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="7a35d-266">**更新済数量別**オプションが**いいえ**に設定されると、入庫済数量に基づいて、発注書に対する最初の入荷の品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="7a35d-267">さらに、追跡用分析コードに応じて、残余数量に基づく 1 つ以上の品質指示が作成されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="7a35d-268">発注書に対するそれ以降の入荷の品質指示は生成されません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="7a35d-269">品質仕様</span><span class="sxs-lookup"><span data-stu-id="7a35d-269">Quality specification</span></span></th>
<th><span data-ttu-id="7a35d-270">更新済数量別</span><span class="sxs-lookup"><span data-stu-id="7a35d-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="7a35d-271">追跡用分析コード別</span><span class="sxs-lookup"><span data-stu-id="7a35d-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="7a35d-272">結果</span><span class="sxs-lookup"><span data-stu-id="7a35d-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="7a35d-273">割合: 10%</span><span class="sxs-lookup"><span data-stu-id="7a35d-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="7a35d-274">はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="7a35d-275">バッチ番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-275">Batch number: No</span></span></p>
<p><span data-ttu-id="7a35d-276">シリアル番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="7a35d-277">注文数量: 100</span><span class="sxs-lookup"><span data-stu-id="7a35d-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="7a35d-278">30 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="7a35d-279">3 (30 の 10%) に対する品質指示 #1</span><span class="sxs-lookup"><span data-stu-id="7a35d-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7a35d-280">70 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="7a35d-281">7 (この場合は 70 に相当する残余注文数量の 10%) に対する品質指示 #2</span><span class="sxs-lookup"><span data-stu-id="7a35d-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-282">固定数量: 1</span><span class="sxs-lookup"><span data-stu-id="7a35d-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="7a35d-283">いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-283">No</span></span></td>
<td>
<p><span data-ttu-id="7a35d-284">バッチ番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-284">Batch number: No</span></span></p>
<p><span data-ttu-id="7a35d-285">シリアル番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="7a35d-286">注文数量: 100</span><span class="sxs-lookup"><span data-stu-id="7a35d-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="7a35d-287">30 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="7a35d-288">1 (完了済として最初にレポートされる数量、つまり固定値 1) に対して品質指示 #1 が作成されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="7a35d-289">残余数量に対しては、これ以上の品質指示は作成されません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7a35d-290">10 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="7a35d-291">品質指示は作成されません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7a35d-292">60 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="7a35d-293">品質指示は作成されません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-294">固定数量: 1</span><span class="sxs-lookup"><span data-stu-id="7a35d-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="7a35d-295">はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="7a35d-296">バッチ番号: はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="7a35d-297">シリアル番号: はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="7a35d-298">注文数量: 10</span><span class="sxs-lookup"><span data-stu-id="7a35d-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="7a35d-299">3 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="7a35d-300">バッチ #b1、シリアル #s1 の 1 に対する品質指示 #1</span><span class="sxs-lookup"><span data-stu-id="7a35d-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="7a35d-301">バッチ #b2、シリアル #s2 の 1 に対する品質指示 #2</span><span class="sxs-lookup"><span data-stu-id="7a35d-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="7a35d-302">バッチ #b3、シリアル #s3 の 1 に対する品質指示 #3</span><span class="sxs-lookup"><span data-stu-id="7a35d-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7a35d-303">2 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="7a35d-304">バッチ #b4、シリアル #s4 の 1 に対する品質指示 #4</span><span class="sxs-lookup"><span data-stu-id="7a35d-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="7a35d-305">バッチ #b5、シリアル #s5 の 1 に対する品質指示 #5</span><span class="sxs-lookup"><span data-stu-id="7a35d-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="7a35d-306"><strong>注記:</strong> バッチは再利用できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-307">固定数量: 2</span><span class="sxs-lookup"><span data-stu-id="7a35d-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="7a35d-308">いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-308">No</span></span></td>
<td>
<p><span data-ttu-id="7a35d-309">バッチ番号: はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="7a35d-310">シリアル番号: はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="7a35d-311">注文数量: 10</span><span class="sxs-lookup"><span data-stu-id="7a35d-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="7a35d-312">4 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="7a35d-313">バッチ #b1、シリアル #s1 の 1 に対する品質指示 #1。</span><span class="sxs-lookup"><span data-stu-id="7a35d-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="7a35d-314">バッチ #b2、シリアル #s2 の 1 に対する品質指示 #2。</span><span class="sxs-lookup"><span data-stu-id="7a35d-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="7a35d-315">バッチ #b3、シリアル #s3 の 1 に対する品質指示 #3。</span><span class="sxs-lookup"><span data-stu-id="7a35d-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="7a35d-316">バッチ #b4、シリアル #s4 の 1 に対する品質指示 #4。</span><span class="sxs-lookup"><span data-stu-id="7a35d-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="7a35d-317">残余数量に対しては、これ以上の品質指示は作成されません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7a35d-318">6 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="7a35d-319">品質指示は作成されません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="7a35d-320">生産</span><span class="sxs-lookup"><span data-stu-id="7a35d-320">Production</span></span>

<span data-ttu-id="7a35d-321">生産で、**品質関連**ページで**イベント タイプ** フィールドを**完了レポート**に、**実行**フィールドを**変更後**に設定すると、次のような結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="7a35d-322">**更新済数量別**オプションが**はい**に設定されると、品目サンプリングの各完了済数量と設定に基づいて品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="7a35d-323">製造オーダーに対する数量が完了済としてレポートされるたびに、新しい完了済数量に基づいて新しい品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="7a35d-324">この生成ロジックは、購買と一致しています。</span><span class="sxs-lookup"><span data-stu-id="7a35d-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="7a35d-325">**更新済数量別**オプションが**いいえ**に設定されると、完了済数量に基づいて、数量が完成済と最初に報告されたときの品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="7a35d-326">さらに、品目サンプリングの追跡用分析コードに応じて、残余数量に基づく 1 つ以上の品質指示が作成されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="7a35d-327">それ以降の完了済数量に対して品質指示は生成されません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="7a35d-328">品質仕様</span><span class="sxs-lookup"><span data-stu-id="7a35d-328">Quality specification</span></span></th>
<th><span data-ttu-id="7a35d-329">更新済数量別</span><span class="sxs-lookup"><span data-stu-id="7a35d-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="7a35d-330">追跡用分析コード別</span><span class="sxs-lookup"><span data-stu-id="7a35d-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="7a35d-331">結果</span><span class="sxs-lookup"><span data-stu-id="7a35d-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="7a35d-332">割合: 10%</span><span class="sxs-lookup"><span data-stu-id="7a35d-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="7a35d-333">はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="7a35d-334">バッチ番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-334">Batch number: No</span></span></p>
<p><span data-ttu-id="7a35d-335">シリアル番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="7a35d-336">注文数量: 100</span><span class="sxs-lookup"><span data-stu-id="7a35d-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="7a35d-337">30 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="7a35d-338">3 (30 の 10%) に対する品質指示 #1</span><span class="sxs-lookup"><span data-stu-id="7a35d-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7a35d-339">70 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="7a35d-340">7 (この場合は 70 に相当する残余注文数量の 10%) に対する品質指示 #2</span><span class="sxs-lookup"><span data-stu-id="7a35d-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-341">固定数量: 1</span><span class="sxs-lookup"><span data-stu-id="7a35d-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="7a35d-342">いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-342">No</span></span></td>
<td>
<p><span data-ttu-id="7a35d-343">バッチ番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-343">Batch number: No</span></span></p>
<p><span data-ttu-id="7a35d-344">シリアル番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="7a35d-345">注文数量: 100</span><span class="sxs-lookup"><span data-stu-id="7a35d-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="7a35d-346">30 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="7a35d-347">1 (完了済として最初にレポートされる数量、つまり固定値 1) に対する品質指示 #1。</span><span class="sxs-lookup"><span data-stu-id="7a35d-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="7a35d-348">1 (まだ固定値 1 の残余数量) に対する品質指示 #2。</span><span class="sxs-lookup"><span data-stu-id="7a35d-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7a35d-349">10 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="7a35d-350">品質指示は作成されません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7a35d-351">60 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="7a35d-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="7a35d-352">品質指示は作成されません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-353">固定数量: 1</span><span class="sxs-lookup"><span data-stu-id="7a35d-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="7a35d-354">はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="7a35d-355">バッチ番号: はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="7a35d-356">シリアル番号: はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="7a35d-357">注文数量: 10</span><span class="sxs-lookup"><span data-stu-id="7a35d-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="7a35d-358">3 に対する完了レポート: #b1、#s1 に対する 1; #b2、#s2 に対する 1; および #b3、#s3 に対する 1</span><span class="sxs-lookup"><span data-stu-id="7a35d-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="7a35d-359">バッチ #b1、シリアル #s1 の 1 に対する品質指示 #1</span><span class="sxs-lookup"><span data-stu-id="7a35d-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="7a35d-360">バッチ #b2、シリアル #s2 の 1 に対する品質指示 #2</span><span class="sxs-lookup"><span data-stu-id="7a35d-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="7a35d-361">バッチ #b3、シリアル #s3 の 1 に対する品質指示 #3</span><span class="sxs-lookup"><span data-stu-id="7a35d-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7a35d-362">2 に対する完了レポート: #b4、#s4 に対する 1; および #b5、#s5 に対する1</span><span class="sxs-lookup"><span data-stu-id="7a35d-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="7a35d-363">バッチ #b4、シリアル #s4 の 1 に対する品質指示 #4</span><span class="sxs-lookup"><span data-stu-id="7a35d-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="7a35d-364">バッチ #b5、シリアル #s5 の 1 に対する品質指示 #5</span><span class="sxs-lookup"><span data-stu-id="7a35d-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="7a35d-365"><strong>注記:</strong> バッチは再利用できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="7a35d-366">固定数量: 2</span><span class="sxs-lookup"><span data-stu-id="7a35d-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="7a35d-367">いいえ</span><span class="sxs-lookup"><span data-stu-id="7a35d-367">No</span></span></td>
<td>
<p><span data-ttu-id="7a35d-368">バッチ番号: はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="7a35d-369">シリアル番号: はい</span><span class="sxs-lookup"><span data-stu-id="7a35d-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="7a35d-370">注文数量: 10</span><span class="sxs-lookup"><span data-stu-id="7a35d-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="7a35d-371">4 に対する完了レポート: #b1、#s1 に対する 1; #b2、#s2 に対する 1; #b3、#s3 に対する 1; および #b4、#s4 に対する 1</span><span class="sxs-lookup"><span data-stu-id="7a35d-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="7a35d-372">バッチ #b1、シリアル #s1 の 1 に対する品質指示 #1</span><span class="sxs-lookup"><span data-stu-id="7a35d-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="7a35d-373">バッチ #b2、シリアル #s2 の 1 に対する品質指示 #2</span><span class="sxs-lookup"><span data-stu-id="7a35d-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="7a35d-374">バッチ #b3、シリアル #s3 の 1 に対する品質指示 #3</span><span class="sxs-lookup"><span data-stu-id="7a35d-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="7a35d-375">バッチ #b4、シリアル #s4 の 1 に対する品質指示 #4</span><span class="sxs-lookup"><span data-stu-id="7a35d-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="7a35d-376">バッチ番号およびシリアル番号への参照がない、2 に対する品質指示 #5</span><span class="sxs-lookup"><span data-stu-id="7a35d-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="7a35d-377">6 に対する完了レポート: #b5、#s5 に対する 1; #b6、#s6 に対する 1; #b7、#s7 に対する 1; #b8、#s8 に対する 1; #b9, #s9 に対する 1; および #b10, #s10 に対する 1</span><span class="sxs-lookup"><span data-stu-id="7a35d-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="7a35d-378">品質指示は作成されません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="7a35d-379">品質管理ページ</span><span class="sxs-lookup"><span data-stu-id="7a35d-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a35d-380">ページ</span><span class="sxs-lookup"><span data-stu-id="7a35d-380">Page</span></span></th>
<th><span data-ttu-id="7a35d-381">説明</span><span class="sxs-lookup"><span data-stu-id="7a35d-381">Description</span></span></th>
<th><span data-ttu-id="7a35d-382">例</span><span class="sxs-lookup"><span data-stu-id="7a35d-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a35d-383">品質関連</span><span class="sxs-lookup"><span data-stu-id="7a35d-383">Quality associations</span></span></td>
<td><span data-ttu-id="7a35d-384">この記事の前のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a35d-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="7a35d-385">品質関連は、生成された品質指示に対する次のすべての情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="7a35d-386">トランザクション イベント</span><span class="sxs-lookup"><span data-stu-id="7a35d-386">The transaction event</span></span></li>
<li><span data-ttu-id="7a35d-387">品目に実行する必要がある一連のテスト</span><span class="sxs-lookup"><span data-stu-id="7a35d-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="7a35d-388">AQL</span><span class="sxs-lookup"><span data-stu-id="7a35d-388">The AQL</span></span></li>
<li><span data-ttu-id="7a35d-389">サンプリング計画</span><span class="sxs-lookup"><span data-stu-id="7a35d-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="7a35d-390">品質指示の自動生成を必要とする業務プロセスの各バリエーションごとに品質アソシエーションを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="7a35d-391">たとえば、品質指示は、発注書、検査指示、販売注文、および製造オーダーの業務プロセスで生成することができます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a35d-392">テスト</span><span class="sxs-lookup"><span data-stu-id="7a35d-392">Tests</span></span></td>
<td><span data-ttu-id="7a35d-393">このページを使用して、製品が品質仕様を満たすかどうかを決定する個別のテストを定義して表示できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="7a35d-394">テスト グループに 1 つ以上の個別のテストを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="7a35d-395">この場合、許容測定値などのテスト固有の情報も指定します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="7a35d-396">測定値は、定量試験に使用され、テスト変数は、定性試験に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="7a35d-397">定量試験には、<strong>整数</strong>または<strong>分数</strong>のテスト タイプがあり、指定された測定単位もあります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="7a35d-398">品質仕様とテスト結果が数字で示されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="7a35d-399">定性試験では、テスト タイプを <strong>オプション</strong> として定義します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="7a35d-400">定性試験では、測定されるテスト変数と列挙されたオプションに関する追加情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="7a35d-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="7a35d-401">品質仕様とテスト結果が結果に応じて示されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="7a35d-402">ある製造会社では、購入した材料に対して 2 種類のテストを行います。材料品質に関する定量試験と、梱包破損に関する定性試験です。</span><span class="sxs-lookup"><span data-stu-id="7a35d-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="7a35d-403">定性試験に関して、テスト変数 (破損した梱包) とその結果を識別する追加情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="7a35d-404"><strong>テスト グループ</strong> ページを使用して、これら 2 つのテストを 1 つのテスト グループに割り当て、テスト固有の情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="7a35d-405">2 つのテストの結果をレポートできるよう、テスト グループを品質指示に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a35d-406">テスト グループ</span><span class="sxs-lookup"><span data-stu-id="7a35d-406">Test groups</span></span></td>
<td><span data-ttu-id="7a35d-407">テスト グループと、テスト グループに割り当てられる個別のテストを設定、編集、および表示するには、このページを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="7a35d-408">上部ウィンドウにはテスト グループが表示され、下部ウィンドウには選択したテスト グループに割り当てられるテストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="7a35d-409">テスト グループには、サンプリング計画、AQL、破壊試験の要件などの複数のポリシーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="7a35d-410">個別のテストをテスト グループに割り当てるときは、順序、ドキュメント、有効期間などの追加情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="7a35d-411">定量試験の場合、定義する情報には許容測定値も含まれます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="7a35d-412">定性試験の場合、情報にはテスト変数と既定の結果が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="7a35d-413">品質指示に割り当てるテスト グループは、指定された品目に対して実行する必要がある既定のテストのセットを定義します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="7a35d-414">ただし、品質指示のテストは、追加、削除、または変更できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="7a35d-415">テスト結果のレポートは、品質指示に対するそれぞれのテストに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="7a35d-416">ある製造会社では、品質ガイドラインのバリエーションごとにテスト グループを定義します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="7a35d-417">さまざまなテスト グループは、サンプリング計画、まとめて実行する必要があるテストのセット、AQL、およびその他の要因における違いを反映します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="7a35d-418">定量試験の場合、許容測定値にも違いがあります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="7a35d-419">品質ガイドラインを適用するために、この会社では、<strong>品質関連</strong>ページで各ルールにテスト グループを割り当てて品質指示を自動的に生成し、また手動で作成された品質指示にテスト グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a35d-420">品目品質グループ</span><span class="sxs-lookup"><span data-stu-id="7a35d-420">Item quality groups</span></span></td>
<td><span data-ttu-id="7a35d-421">品質グループに割り当てられる品目、または品目に割り当てられる品質グループを、設定、編集、および表示するには、このページを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="7a35d-422">品質グループとは、複数の品目に共通するテスト要件です。</span><span class="sxs-lookup"><span data-stu-id="7a35d-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="7a35d-423"><strong>テスト グループ</strong> ページのテスト要件を定義した後、品質指示を自動生成するルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="7a35d-424">プロセスを簡略化するために、個別の品目のルールは定義しません。</span><span class="sxs-lookup"><span data-stu-id="7a35d-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="7a35d-425">代わりに、<strong>品質関連</strong>ページを使用して品質グループのルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="7a35d-426">選択した品質グループの<strong>品目品質グループ</strong> ページを使用して、そのグループに関連品目を割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="7a35d-427">選択した品目の<strong>品目品質グループ</strong> ページを使用して、その品目に関連品質グループを割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="7a35d-428">ある製造会社で、受入検査に同じテスト要件があるさまざまな原材料を購入しています。</span><span class="sxs-lookup"><span data-stu-id="7a35d-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="7a35d-429">その会社では、品質グループを定義し、そのグループに原材料と関連付けた品目番号を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="7a35d-430">後で、同じテスト要件がある新しいタイプの原材料を購入します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="7a35d-431">新しい材料の新しいテスト要件を設定せずに、既存の品質グループに新しい材料の品目番号を追加します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="7a35d-432">また、この製造会社では、同じ製造テスト要件の品目を製造し、同じ要件で出荷前テストを実行して品目を出荷しています。</span><span class="sxs-lookup"><span data-stu-id="7a35d-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="7a35d-433">この会社は、さらに 2 つの品質グループを定義し、各グループに関連品目番号を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a35d-434">テスト変数</span><span class="sxs-lookup"><span data-stu-id="7a35d-434">Test variables</span></span></td>
<td><span data-ttu-id="7a35d-435">定性試験に関連付けられている変数を定義または表示するには、このページを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="7a35d-436">各変数には、選択できるオプションを表す列挙された結果を定義します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="7a35d-437"><strong>テスト</strong> ページでテストを定義します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="7a35d-438">定性試験では、テスト タイプを <strong>オプション</strong> に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="7a35d-439"><strong>テスト グループ</strong> ページを使用して個別のテストにテスト変数を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="7a35d-440">クッキーを製造しているある製造会社では、完成した製品の検査テストを採用しています。</span><span class="sxs-lookup"><span data-stu-id="7a35d-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="7a35d-441">この検査テストには、複数の変数があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-441">This inspection test has several variables.</span></span> <span data-ttu-id="7a35d-442">1 つ目の変数は味で、この変数に対して発生する可能性がある結果は、良および不良です。</span><span class="sxs-lookup"><span data-stu-id="7a35d-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="7a35d-443">2 つ目の変数は色で、発生する可能性がある結果は、濃すぎる、薄すぎる、および適正です。</span><span class="sxs-lookup"><span data-stu-id="7a35d-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a35d-444">テスト変数の結果</span><span class="sxs-lookup"><span data-stu-id="7a35d-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="7a35d-445">定性試験に関連付けられているテスト変数について、発生する可能性があるテスト結果を設定、編集、および表示するには、このページを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="7a35d-446">それぞれの結果について、<strong>合格</strong>または<strong>不合格</strong>のステータスを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7a35d-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="7a35d-447"><strong>テスト</strong> ページで定義した各定性試験に対する変数とその結果を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="7a35d-448">(定性試験の場合、テスト タイプは、<strong>テスト</strong> ページで <strong>オプション</strong> に設定されます)。個々の定性試験にテスト変数と既定の結果を割り当てるには、<strong>テスト グループ</strong> ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="7a35d-449">クッキーを製造しているある製造会社では、完成した製品の検査テストを採用しています。</span><span class="sxs-lookup"><span data-stu-id="7a35d-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="7a35d-450">この検査テストには、複数の変数があります。</span><span class="sxs-lookup"><span data-stu-id="7a35d-450">This inspection test has of several variables.</span></span> <span data-ttu-id="7a35d-451">1 つ目の変数は味で、この変数に対して発生する可能性がある結果は、良および不良です。</span><span class="sxs-lookup"><span data-stu-id="7a35d-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="7a35d-452">2 つ目の変数は色で、発生する可能性がある結果は、濃すぎる、薄すぎる、および適正です。</span><span class="sxs-lookup"><span data-stu-id="7a35d-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="7a35d-453">それぞれの結果に<strong>合格</strong>または<strong>不合格</strong>のステータスが割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="7a35d-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="7a35d-454">各変数の検査テスト時に、検査官はいずれかの結果を選択することによってテスト結果を報告します。</span><span class="sxs-lookup"><span data-stu-id="7a35d-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="7a35d-455">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7a35d-455">Additional resources</span></span>
--------

[<span data-ttu-id="7a35d-456">品質管理プロセス</span><span class="sxs-lookup"><span data-stu-id="7a35d-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="7a35d-457">不適合管理</span><span class="sxs-lookup"><span data-stu-id="7a35d-457">Nonconformance management</span></span>](enable-nonconformance-management.md)
