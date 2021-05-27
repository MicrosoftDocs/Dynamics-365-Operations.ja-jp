---
title: 品質関連
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質関連を使用して、販売、購買、および生産プロセスに関連する品質指示を自動的に生成する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c6fab1b89b7e58d9e443c27da03a6b13afcc9c6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022327"
---
# <a name="quality-associations"></a><span data-ttu-id="ca9eb-103">品質関連</span><span class="sxs-lookup"><span data-stu-id="ca9eb-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca9eb-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質関連を使用して、販売、購買、および生産プロセスに関連する品質指示を自動的に生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="ca9eb-105">品質関連は、生成された品質指示に対する次のすべての情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="ca9eb-106">トランザクション イベント</span><span class="sxs-lookup"><span data-stu-id="ca9eb-106">The transaction event</span></span>
- <span data-ttu-id="ca9eb-107">品目に実行する必要がある一連のテスト</span><span class="sxs-lookup"><span data-stu-id="ca9eb-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="ca9eb-108">許容可能な品質レベル (AQL)</span><span class="sxs-lookup"><span data-stu-id="ca9eb-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="ca9eb-109">サンプリング計画</span><span class="sxs-lookup"><span data-stu-id="ca9eb-109">The sampling plan</span></span>

<span data-ttu-id="ca9eb-110">品質指示の自動生成を必要とする業務プロセスの各バリエーションごとに品質アソシエーションを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="ca9eb-111">たとえば、品質指示は、発注書、検査指示、販売注文、および製造オーダーの業務プロセスで生成することができます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="ca9eb-112">品質アソシエーションの使用</span><span class="sxs-lookup"><span data-stu-id="ca9eb-112">Working with quality associations</span></span>

<span data-ttu-id="ca9eb-113">品質関連を使用する業務プロセスは、発注書、販売注文、または製造オーダーなどさまざまな元伝票に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="ca9eb-114">それぞれの品質関連レコードでは、生成された品質指示に適用される一連のテスト、AQL、およびサンプリング計画が定義されます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="ca9eb-115">業務プロセスの各バリエーションごとに品質関連レコードを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="ca9eb-116">たとえば、購買注文製品受領書が更新されるときに、品質指示を生成する品質関連を設定できます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="ca9eb-117">実行計画の設定によっては、未処理の品質指示がある場合、発生プロセス自体をブロックできます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="ca9eb-118">また発注書の請求など、後続のプロセスをブロックできます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="ca9eb-119">未処理の品質指示がある間は、在庫数量が発行されないように自動的にブロックされます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="ca9eb-120">**品目サンプリング** ページの **完全ブロック** フィールドの設定に応じて、発注書上の数量か、元伝票明細行の数量のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="ca9eb-121">詳細については、[品質管理の品目サンプリング](quality-item-sampling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="ca9eb-122">指定された業務プロセスに対して、品質関連レコードにより、品質指示が生成されるイベントおよび条件が識別されます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="ca9eb-123">条件はサイトまたは法人の固有のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="ca9eb-124">破壊試験を伴う品質指示は、イベントに必要な手持ち在庫が存在する場合にのみ生成できます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="ca9eb-125">品質関連を使用するには、**在庫管理 \> 設定 \> 品質管理 \> 品質関連** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="ca9eb-126">次の例は、業務プロセスの各変動に対して、品質関連レコードがどのように定義されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="ca9eb-127">次の表の例は、品質関連レコードによって定義されるイベントと条件の観点から要約されています。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ca9eb-128">参照タイプ</span><span class="sxs-lookup"><span data-stu-id="ca9eb-128">Reference type</span></span></th>
<th><span data-ttu-id="ca9eb-129">イベント タイプ</span><span class="sxs-lookup"><span data-stu-id="ca9eb-129">Event type</span></span></th>
<th><span data-ttu-id="ca9eb-130">実行</span><span class="sxs-lookup"><span data-stu-id="ca9eb-130">Execution</span></span></th>
<th><span data-ttu-id="ca9eb-131">イベント ブロック</span><span class="sxs-lookup"><span data-stu-id="ca9eb-131">Event blocking</span></span></th>
<th><span data-ttu-id="ca9eb-132">ドキュメントの参照</span><span class="sxs-lookup"><span data-stu-id="ca9eb-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ca9eb-133">棚卸資産</span><span class="sxs-lookup"><span data-stu-id="ca9eb-133">Inventory</span></span></td>
<td><span data-ttu-id="ca9eb-134">適用できません</span><span class="sxs-lookup"><span data-stu-id="ca9eb-134">Not applicable</span></span></td>
<td><span data-ttu-id="ca9eb-135">適用できません</span><span class="sxs-lookup"><span data-stu-id="ca9eb-135">Not applicable</span></span></td>
<td><span data-ttu-id="ca9eb-136">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-136">None</span></span></td>
<td><span data-ttu-id="ca9eb-137">すべて</span><span class="sxs-lookup"><span data-stu-id="ca9eb-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="ca9eb-138">販売注文</span><span class="sxs-lookup"><span data-stu-id="ca9eb-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="ca9eb-139">ピッキング プロセスがスケジュールされます</span><span class="sxs-lookup"><span data-stu-id="ca9eb-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="ca9eb-140">以前</span><span class="sxs-lookup"><span data-stu-id="ca9eb-140">Before</span></span></td>
<td><span data-ttu-id="ca9eb-141">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="ca9eb-142">固有 ID、グループ、またはすべてのみ。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-143">ピッキング プロセス</span><span class="sxs-lookup"><span data-stu-id="ca9eb-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-144">梱包明細</span><span class="sxs-lookup"><span data-stu-id="ca9eb-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-145">請求書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ca9eb-146">梱包明細</span><span class="sxs-lookup"><span data-stu-id="ca9eb-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9eb-147">以前</span><span class="sxs-lookup"><span data-stu-id="ca9eb-147">Before</span></span></td>
<td><span data-ttu-id="ca9eb-148">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-149">梱包明細</span><span class="sxs-lookup"><span data-stu-id="ca9eb-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-150">請求書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="ca9eb-151">購買</span><span class="sxs-lookup"><span data-stu-id="ca9eb-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="ca9eb-152">入庫リスト</span><span class="sxs-lookup"><span data-stu-id="ca9eb-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="ca9eb-153">以前</span><span class="sxs-lookup"><span data-stu-id="ca9eb-153">Before</span></span></td>
<td><span data-ttu-id="ca9eb-154">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-155">入庫リスト</span><span class="sxs-lookup"><span data-stu-id="ca9eb-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-156">製品受領書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-157">請求書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ca9eb-158">以後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-158">After</span></span></td>
<td><span data-ttu-id="ca9eb-159">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-160">製品受領書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-161">請求書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ca9eb-162">登録</span><span class="sxs-lookup"><span data-stu-id="ca9eb-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9eb-163">適用できません</span><span class="sxs-lookup"><span data-stu-id="ca9eb-163">Not applicable</span></span></td>
<td><span data-ttu-id="ca9eb-164">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-165">製品受領書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-166">請求書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ca9eb-167">製品受領書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9eb-168">以前</span><span class="sxs-lookup"><span data-stu-id="ca9eb-168">Before</span></span></td>
<td><span data-ttu-id="ca9eb-169">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-170">製品受領書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-171">請求書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ca9eb-172">以後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-172">After</span></span></td>
<td><span data-ttu-id="ca9eb-173">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-174">請求書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="ca9eb-175">運用</span><span class="sxs-lookup"><span data-stu-id="ca9eb-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9eb-176">登録</span><span class="sxs-lookup"><span data-stu-id="ca9eb-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9eb-177">適用できません</span><span class="sxs-lookup"><span data-stu-id="ca9eb-177">Not applicable</span></span></td>
<td><span data-ttu-id="ca9eb-178">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="ca9eb-179">すべて</span><span class="sxs-lookup"><span data-stu-id="ca9eb-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-180">完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-181">終了日</span><span class="sxs-lookup"><span data-stu-id="ca9eb-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ca9eb-182">完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9eb-183">以前</span><span class="sxs-lookup"><span data-stu-id="ca9eb-183">Before</span></span></td>
<td><span data-ttu-id="ca9eb-184">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-185">完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-186">終了日</span><span class="sxs-lookup"><span data-stu-id="ca9eb-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ca9eb-187">以後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-187">After</span></span></td>
<td><span data-ttu-id="ca9eb-188">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-189">終了日</span><span class="sxs-lookup"><span data-stu-id="ca9eb-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ca9eb-190">検査</span><span class="sxs-lookup"><span data-stu-id="ca9eb-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9eb-191">完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="ca9eb-192">以前</span><span class="sxs-lookup"><span data-stu-id="ca9eb-192">Before</span></span></td>
<td><span data-ttu-id="ca9eb-193">完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-194">終了日</span><span class="sxs-lookup"><span data-stu-id="ca9eb-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-195">以後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-195">After</span></span></td>
<td><span data-ttu-id="ca9eb-196">終了日</span><span class="sxs-lookup"><span data-stu-id="ca9eb-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-197">終了日</span><span class="sxs-lookup"><span data-stu-id="ca9eb-197">End</span></span></td>
<td><span data-ttu-id="ca9eb-198">以前</span><span class="sxs-lookup"><span data-stu-id="ca9eb-198">Before</span></span></td>
<td><span data-ttu-id="ca9eb-199">終了日</span><span class="sxs-lookup"><span data-stu-id="ca9eb-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ca9eb-200">工順工程</span><span class="sxs-lookup"><span data-stu-id="ca9eb-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9eb-201">完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="ca9eb-202">以前</span><span class="sxs-lookup"><span data-stu-id="ca9eb-202">Before</span></span></td>
<td><span data-ttu-id="ca9eb-203">None</span><span class="sxs-lookup"><span data-stu-id="ca9eb-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9eb-204">固有 ID、グループ、またはすべて、および固有リソース、グループ、またはすべて</span><span class="sxs-lookup"><span data-stu-id="ca9eb-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-205">完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-206">変更後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-206">After</span></span></td>
<td><span data-ttu-id="ca9eb-207">None</span><span class="sxs-lookup"><span data-stu-id="ca9eb-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ca9eb-208">連産品の生産</span><span class="sxs-lookup"><span data-stu-id="ca9eb-208">Co-product production</span></span></td>
<td><span data-ttu-id="ca9eb-209">登録</span><span class="sxs-lookup"><span data-stu-id="ca9eb-209">Registration</span></span></td>
<td><span data-ttu-id="ca9eb-210">適用できません</span><span class="sxs-lookup"><span data-stu-id="ca9eb-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9eb-211">None</span><span class="sxs-lookup"><span data-stu-id="ca9eb-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="ca9eb-212">All</span><span class="sxs-lookup"><span data-stu-id="ca9eb-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ca9eb-213">完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-213">Report as finished</span></span></td>
<td><span data-ttu-id="ca9eb-214">以前</span><span class="sxs-lookup"><span data-stu-id="ca9eb-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-215">変更後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ca9eb-216">*倉庫プロセスの品質管理機能* では、**イベント タイプ** フィールドが *完了報告* に、 **実行** フィールドが *後* に設定した生産用の品質指示処理と、**イベント タイプ** フィールドを *登録* に設定した購入用の品質指示処理の機能が追加されます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="ca9eb-217">詳細については、[倉庫プロセスの品質管理](quality-management-for-warehouses-processes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="ca9eb-218">次の表に、品質指示をプロセスの特定のタイプに対して生成する方法の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="ca9eb-219">プロセスのタイプ</span><span class="sxs-lookup"><span data-stu-id="ca9eb-219">Type of process</span></span></th>
<th><span data-ttu-id="ca9eb-220">品質指示を自動的に生成できる場合</span><span class="sxs-lookup"><span data-stu-id="ca9eb-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="ca9eb-221">破壊試験が必要な場合に品質指示を生成できる場合</span><span class="sxs-lookup"><span data-stu-id="ca9eb-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="ca9eb-222">条件の情報</span><span class="sxs-lookup"><span data-stu-id="ca9eb-222">Condition information</span></span></th>
<th><span data-ttu-id="ca9eb-223">手動生成情報</span><span class="sxs-lookup"><span data-stu-id="ca9eb-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ca9eb-224">発注書</span><span class="sxs-lookup"><span data-stu-id="ca9eb-224">Purchase order</span></span></td>
<td><span data-ttu-id="ca9eb-225">受領した材料の受領書リストまたは製品受領書の転記前または転記後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="ca9eb-226">材料は破壊試験に利用できる必要があるために、受領した材料の製品受領書が転記された後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="ca9eb-227">品質指示の要求は、特定のサイト、品目、仕入先、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ca9eb-228">発注書を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-229">検査指示</span><span class="sxs-lookup"><span data-stu-id="ca9eb-229">Quarantine order</span></span></td>
<td><span data-ttu-id="ca9eb-230">検査指示が完了済みまたは終了と報告される前または後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="ca9eb-231">破壊試験を必要とする品質指示は生成することができません。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="ca9eb-232">検査指示機能が、破壊される材料の破棄を扱うと仮定します。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="ca9eb-233">品質指示の要求は、特定のサイト、品目、仕入先、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ca9eb-234">検査指示を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-235">販売注文</span><span class="sxs-lookup"><span data-stu-id="ca9eb-235">Sales order</span></span></td>
<td><span data-ttu-id="ca9eb-236">出荷する品目のスケジュールされたピッキング プロセスまたは梱包明細を更新する前</span><span class="sxs-lookup"><span data-stu-id="ca9eb-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="ca9eb-237">任意のステップ</span><span class="sxs-lookup"><span data-stu-id="ca9eb-237">At any step</span></span></td>
<td><span data-ttu-id="ca9eb-238">品質指示の要求は、特定のサイト、品目、顧客、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ca9eb-239">販売注文を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-240">製造オーダー</span><span class="sxs-lookup"><span data-stu-id="ca9eb-240">Production order</span></span></td>
<td><span data-ttu-id="ca9eb-241">製造オーダーの完了済数量の報告前または後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="ca9eb-242">製造オーダーの完了済数量の報告後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="ca9eb-243">品質指示の要求は、特定のサイトや品目、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ca9eb-244">製造オーダーを参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質アソシエーション レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-245">工順工程を持つ製造オーダー</span><span class="sxs-lookup"><span data-stu-id="ca9eb-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="ca9eb-246">操作のレポート終了前または後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="ca9eb-247">最後の操作のレポート生産終了後</span><span class="sxs-lookup"><span data-stu-id="ca9eb-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="ca9eb-248">品質指示の要求は、特定のサイト、品目、運営リソース、またはこれらの条件の組み合わせを反映している場合があります。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="ca9eb-249">工順工程を参照する、手動で生成された品質指示では、テスト サンプリング計画などの、品質関連レコードの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-250">在庫</span><span class="sxs-lookup"><span data-stu-id="ca9eb-250">Inventory</span></span></td>
<td><span data-ttu-id="ca9eb-251">在庫仕訳帳のトランザクションまたは移動オーダー トランザクションに対して、品質指示を自動的に生成することはできません。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="ca9eb-252">品質指示は、品目の在庫数量に対して手動で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="ca9eb-253">現物手持在庫は必須です。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="ca9eb-254">品質指示の自動生成の例</span><span class="sxs-lookup"><span data-stu-id="ca9eb-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="ca9eb-255">購買</span><span class="sxs-lookup"><span data-stu-id="ca9eb-255">Purchasing</span></span>

<span data-ttu-id="ca9eb-256">購買で、**品質関連** ページで **イベント タイプ** フィールドを *製品受領書* に、**実行** フィールドを *変更後* に設定すると、次のような結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="ca9eb-257">**更新済数量別** オプションが *はい* に設定されると、品目サンプリングの入庫済数量と設定に基づいて、発注書に対するすべての入荷の品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="ca9eb-258">発注書に対する数量が入荷されるたびに、新しく入荷した数量に基づいて新しい品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="ca9eb-259">**更新済数量別** オプションが *いいえ* に設定されると、入庫済数量に基づいて、発注書に対する最初の入荷の品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="ca9eb-260">さらに、追跡用分析コードに応じて、残余数量に基づく 1 つ以上の品質指示が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="ca9eb-261">発注書に対するそれ以降の入荷の品質指示は生成されません。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="ca9eb-262">運用</span><span class="sxs-lookup"><span data-stu-id="ca9eb-262">Production</span></span>

<span data-ttu-id="ca9eb-263">生産で、**品質関連** ページで **イベント タイプ** フィールドを *完了レポート* に、**実行** フィールドを *変更後* に設定すると、次のような結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="ca9eb-264">**更新済数量別** オプションが *はい* に設定されると、品目サンプリングの各完了済数量と設定に基づいて品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="ca9eb-265">製造オーダーに対する数量が完了済としてレポートされるたびに、新しい完了済数量に基づいて新しい品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="ca9eb-266">この生成ロジックは、購買と一致しています。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="ca9eb-267">**更新済数量別** オプションが *いいえ* に設定されると、完了済数量に基づいて、数量が完成済と最初に報告されたときの品質指示が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="ca9eb-268">さらに、品目サンプリングの追跡用分析コードに応じて、残余数量に基づく 1 つ以上の品質指示が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="ca9eb-269">それ以降の完了済数量に対して品質指示は生成されません。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ca9eb-270">品質仕様</span><span class="sxs-lookup"><span data-stu-id="ca9eb-270">Quality specification</span></span></th>
<th><span data-ttu-id="ca9eb-271">更新済数量別</span><span class="sxs-lookup"><span data-stu-id="ca9eb-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="ca9eb-272">追跡用分析コード別</span><span class="sxs-lookup"><span data-stu-id="ca9eb-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="ca9eb-273">結果</span><span class="sxs-lookup"><span data-stu-id="ca9eb-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ca9eb-274">割合: 10%</span><span class="sxs-lookup"><span data-stu-id="ca9eb-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="ca9eb-275">はい</span><span class="sxs-lookup"><span data-stu-id="ca9eb-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="ca9eb-276">バッチ番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="ca9eb-276">Batch number: No</span></span></p>
<p><span data-ttu-id="ca9eb-277">シリアル番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="ca9eb-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="ca9eb-278">注文数量: 100</span><span class="sxs-lookup"><span data-stu-id="ca9eb-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="ca9eb-279">30 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="ca9eb-280">3 (30 の 10%) に対する品質指示 1</span><span class="sxs-lookup"><span data-stu-id="ca9eb-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9eb-281">70 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="ca9eb-282">7 (この場合は 70 に相当する残余注文数量の 10%) に対する品質指示 2</span><span class="sxs-lookup"><span data-stu-id="ca9eb-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-283">固定数量: 1</span><span class="sxs-lookup"><span data-stu-id="ca9eb-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="ca9eb-284">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-284">No</span></span></td>
<td>
<p><span data-ttu-id="ca9eb-285">バッチ番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="ca9eb-285">Batch number: No</span></span></p>
<p><span data-ttu-id="ca9eb-286">シリアル番号: いいえ</span><span class="sxs-lookup"><span data-stu-id="ca9eb-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="ca9eb-287">注文数量: 100</span><span class="sxs-lookup"><span data-stu-id="ca9eb-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="ca9eb-288">30 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="ca9eb-289">1 (完了済として最初にレポートされる数量、つまり固定値 1) に対する品質指示 1</span><span class="sxs-lookup"><span data-stu-id="ca9eb-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="ca9eb-290">1 (まだ固定値 1 の残余数量) に対する品質指示 2</span><span class="sxs-lookup"><span data-stu-id="ca9eb-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9eb-291">10 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="ca9eb-292">品質指示は作成されません。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9eb-293">60 の完了レポート</span><span class="sxs-lookup"><span data-stu-id="ca9eb-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="ca9eb-294">品質指示は作成されません。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-295">固定数量: 1</span><span class="sxs-lookup"><span data-stu-id="ca9eb-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="ca9eb-296">はい</span><span class="sxs-lookup"><span data-stu-id="ca9eb-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="ca9eb-297">バッチ番号: はい</span><span class="sxs-lookup"><span data-stu-id="ca9eb-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="ca9eb-298">シリアル番号: はい</span><span class="sxs-lookup"><span data-stu-id="ca9eb-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="ca9eb-299">注文数量: 10</span><span class="sxs-lookup"><span data-stu-id="ca9eb-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="ca9eb-300">3 の完了レポート: バッチ番号 b1、シリアル番号 s1 に対する 1; バッチ番号 b2、シリアル番号 s2 に対する 1; およびバッチ番号 b3、シリアル番号 s3 に対する 1</span><span class="sxs-lookup"><span data-stu-id="ca9eb-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="ca9eb-301">バッチ番号 b1、シリアル番号 s1 の 1 に対する品質指示 1</span><span class="sxs-lookup"><span data-stu-id="ca9eb-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="ca9eb-302">バッチ番号 b2、シリアル番号 s2 の 1 に対する品質指示 2</span><span class="sxs-lookup"><span data-stu-id="ca9eb-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="ca9eb-303">バッチ番号 b3、シリアル番号 s3 の 1 に対する品質指示 3</span><span class="sxs-lookup"><span data-stu-id="ca9eb-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9eb-304">完了レポート 2: バッチ番号 b4、シリアル番号 s4 に対する 1; およびバッチ番号 b5、シリアル番号 s5 に対する 1</span><span class="sxs-lookup"><span data-stu-id="ca9eb-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="ca9eb-305">バッチ番号 b4、シリアル番号 s4 の 1 に対する品質指示 4</span><span class="sxs-lookup"><span data-stu-id="ca9eb-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="ca9eb-306">バッチ番号 b5、シリアル番号 s5 の 1 に対する品質指示 5</span><span class="sxs-lookup"><span data-stu-id="ca9eb-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="ca9eb-307"><strong>注記:</strong> バッチは再利用できます。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="ca9eb-308">固定数量: 2</span><span class="sxs-lookup"><span data-stu-id="ca9eb-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="ca9eb-309">なし</span><span class="sxs-lookup"><span data-stu-id="ca9eb-309">No</span></span></td>
<td>
<p><span data-ttu-id="ca9eb-310">バッチ番号: はい</span><span class="sxs-lookup"><span data-stu-id="ca9eb-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="ca9eb-311">シリアル番号: はい</span><span class="sxs-lookup"><span data-stu-id="ca9eb-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="ca9eb-312">注文数量: 10</span><span class="sxs-lookup"><span data-stu-id="ca9eb-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="ca9eb-313">4 の完了レポート: バッチ番号 b1、シリアル番号 s1 に対する 1; バッチ番号 b2、シリアル番号 s2 に対する 1; バッチ番号 b3、シリアル番号 s3 に対する 1; およびバッチ番号 b4、シリアル番号 s4 に対する 1</span><span class="sxs-lookup"><span data-stu-id="ca9eb-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="ca9eb-314">バッチ番号 b1、シリアル番号 s1 の 1 に対する品質指示 1</span><span class="sxs-lookup"><span data-stu-id="ca9eb-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="ca9eb-315">バッチ番号 b2、シリアル番号 s2 の 1 に対する品質指示 2</span><span class="sxs-lookup"><span data-stu-id="ca9eb-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="ca9eb-316">バッチ番号 b3、シリアル番号 s3 の 1 に対する品質指示 3</span><span class="sxs-lookup"><span data-stu-id="ca9eb-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="ca9eb-317">バッチ番号 b4、シリアル番号 s4 の 1 に対する品質指示 4</span><span class="sxs-lookup"><span data-stu-id="ca9eb-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="ca9eb-318">バッチ番号およびシリアル番号への参照がない、2 に対する品質指示 5</span><span class="sxs-lookup"><span data-stu-id="ca9eb-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ca9eb-319">完了レポート 6: バッチ番号 b5、シリアル番号 s5 に対する 1; バッチ番号 b6、シリアル番号 s6 に対する 1; バッチ番号 b7、シリアル番号 s7 に対する 1; バッチ番号 b8、シリアル番号 s8 に対する 1; バッチ番号 b9、シリアル番号 s9 に対する 1; およびバッチ番号 b10、シリアル番号 s10 に対する 1</span><span class="sxs-lookup"><span data-stu-id="ca9eb-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="ca9eb-320">品質指示は作成されません。</span><span class="sxs-lookup"><span data-stu-id="ca9eb-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="ca9eb-321">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ca9eb-321">Additional resources</span></span>

- [<span data-ttu-id="ca9eb-322">品質管理プロセス</span><span class="sxs-lookup"><span data-stu-id="ca9eb-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="ca9eb-323">品質および不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="ca9eb-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="ca9eb-324">倉庫プロセスに対する品質管理</span><span class="sxs-lookup"><span data-stu-id="ca9eb-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
