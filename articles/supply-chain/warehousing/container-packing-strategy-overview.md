---
title: コンテナー梱包計画
description: このトピックでは、コンテナー梱包計画間の違いについて説明し、その例を示します。
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292764"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="66425-103">コンテナー梱包計画</span><span class="sxs-lookup"><span data-stu-id="66425-103">Container packing strategies</span></span>

<span data-ttu-id="66425-104">*コンテナー梱包計画* は、コンテナー間で品目配賦を定義するために使用できる計画です。</span><span class="sxs-lookup"><span data-stu-id="66425-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="66425-105">このトピックでは、*オープンのコンテナーすべてに梱包* 計画と *現在のコンテナーにのみ梱包* 計画の違いについて説明します。</span><span class="sxs-lookup"><span data-stu-id="66425-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="66425-106">**オープンのコンテナーすべてに梱包** – システムは、コンテナー詰めのサイクル中に既に作成されたすべてのオープン コンテナーを確認し、品目がそのうちの 1 つに適合することを確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="66425-107">梱包中に、システムは各品目をチェックして以前に作成されたコンテナーのいずれかに適合するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="66425-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="66425-108">品目が既存のコンテナーに適合しない場合は、システムにより新しいコンテナーが作成され、注文全体の梱包が終了するまで続行されます。</span><span class="sxs-lookup"><span data-stu-id="66425-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="66425-109">たとえば、*n* 注文済品目はコンテナー詰めを必要とします。</span><span class="sxs-lookup"><span data-stu-id="66425-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="66425-110">最悪の場合、システムが既存のコンテナーに適合しない品目を処理するたびに、(\[(*n* – 1) × (*n* + 1)\] ÷ 2) の合計のチェックを実行し、品目が既存のコンテナーに適合するかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="66425-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="66425-111">**現在のコンテナーにのみ梱包** – システムにより、最後に作成されたコンテナーのみをチェックして品目がそれに適合するかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66425-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="66425-112">梱包中に、システムは各品目をチェックして最後に作成されたコンテナーに適合するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="66425-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="66425-113">品目がそのコンテナーに適合しない場合は、システムにより新しいコンテナーが作成され、注文全体の梱包が終了するまで続行されます。</span><span class="sxs-lookup"><span data-stu-id="66425-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="66425-114">たとえば、*n* 注文済品目はコンテナー詰めを必要とします。</span><span class="sxs-lookup"><span data-stu-id="66425-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="66425-115">最悪の場合、システムは (*n* – 1) の合計のチェックを実行し、品目がコンテナーに適合するかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="66425-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="66425-116">コンテナー梱包計画のフローの例</span><span class="sxs-lookup"><span data-stu-id="66425-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="66425-117">コンテナー詰めに対して次の項目を設定します。</span><span class="sxs-lookup"><span data-stu-id="66425-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="66425-118">項目</span><span class="sxs-lookup"><span data-stu-id="66425-118">Item</span></span> | <span data-ttu-id="66425-119">現物分析コード (幅 × 奥行き × 高さ)</span><span class="sxs-lookup"><span data-stu-id="66425-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="66425-120">太さ</span><span class="sxs-lookup"><span data-stu-id="66425-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="66425-121">HDMI ケーブル 6'</span><span class="sxs-lookup"><span data-stu-id="66425-121">HDMI Cable 6'</span></span> | <span data-ttu-id="66425-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="66425-122">1 × 1 × 1</span></span> | <span data-ttu-id="66425-123">1</span><span class="sxs-lookup"><span data-stu-id="66425-123">1</span></span> |
| <span data-ttu-id="66425-124">HDMI ケーブル 12'</span><span class="sxs-lookup"><span data-stu-id="66425-124">HDMI Cable 12'</span></span> | <span data-ttu-id="66425-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="66425-125">2 × 1 × 1</span></span> | <span data-ttu-id="66425-126">1</span><span class="sxs-lookup"><span data-stu-id="66425-126">1</span></span> |
| <span data-ttu-id="66425-127">HDMI ケーブル 18'</span><span class="sxs-lookup"><span data-stu-id="66425-127">HDMI Cable 18'</span></span> | <span data-ttu-id="66425-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="66425-128">3 × 1 × 1</span></span> | <span data-ttu-id="66425-129">2</span><span class="sxs-lookup"><span data-stu-id="66425-129">2</span></span> |

<span data-ttu-id="66425-130">梱包に使用される次のボックスも設定します。</span><span class="sxs-lookup"><span data-stu-id="66425-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="66425-131">コンテナー</span><span class="sxs-lookup"><span data-stu-id="66425-131">Container</span></span> | <span data-ttu-id="66425-132">現物分析コード (長さ × 幅 × 高さ)</span><span class="sxs-lookup"><span data-stu-id="66425-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="66425-133">太さ</span><span class="sxs-lookup"><span data-stu-id="66425-133">Weight</span></span> | <span data-ttu-id="66425-134">量</span><span class="sxs-lookup"><span data-stu-id="66425-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="66425-135">中規模なボックス</span><span class="sxs-lookup"><span data-stu-id="66425-135">Medium Box</span></span> | <span data-ttu-id="66425-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="66425-136">6 × 3 × 2</span></span> | <span data-ttu-id="66425-137">10</span><span class="sxs-lookup"><span data-stu-id="66425-137">10</span></span> | <span data-ttu-id="66425-138">100</span><span class="sxs-lookup"><span data-stu-id="66425-138">100</span></span> |

<span data-ttu-id="66425-139">最後に、次の製品と数量を含む注文を設定します。</span><span class="sxs-lookup"><span data-stu-id="66425-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="66425-140">販売注文明細行</span><span class="sxs-lookup"><span data-stu-id="66425-140">Sales order line</span></span> | <span data-ttu-id="66425-141">件数</span><span class="sxs-lookup"><span data-stu-id="66425-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="66425-142">HDMI ケーブル 12'</span><span class="sxs-lookup"><span data-stu-id="66425-142">HDMI Cable 12'</span></span> | <span data-ttu-id="66425-143">9</span><span class="sxs-lookup"><span data-stu-id="66425-143">9</span></span> |
| <span data-ttu-id="66425-144">HDMI ケーブル 18'</span><span class="sxs-lookup"><span data-stu-id="66425-144">HDMI Cable 18'</span></span> | <span data-ttu-id="66425-145">8</span><span class="sxs-lookup"><span data-stu-id="66425-145">8</span></span> |
| <span data-ttu-id="66425-146">HDMI ケーブル 6'</span><span class="sxs-lookup"><span data-stu-id="66425-146">HDMI Cable 6'</span></span> | <span data-ttu-id="66425-147">13</span><span class="sxs-lookup"><span data-stu-id="66425-147">13</span></span> |

<span data-ttu-id="66425-148">次の表では、*オープンのコンテナーすべてに梱包* 計画を使用する場合と *現在のコンテナーにのみ梱包* 計画を使用する場合にコンテナー詰めがどのように機能するかを要約します。</span><span class="sxs-lookup"><span data-stu-id="66425-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="66425-149">すべてのオープン コンテナーに梱包</span><span class="sxs-lookup"><span data-stu-id="66425-149">Pack into all open containers</span></span> | <span data-ttu-id="66425-150">現在のコンテナーに梱包</span><span class="sxs-lookup"><span data-stu-id="66425-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="66425-151">HDMI ケーブル 12':</span><span class="sxs-lookup"><span data-stu-id="66425-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="66425-152">新規コンテナー、CONT0001 を作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="66425-153">9 個をコンテナー CONT0001 に配置します。</span><span class="sxs-lookup"><span data-stu-id="66425-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="66425-154">HDMI ケーブル 12':</span><span class="sxs-lookup"><span data-stu-id="66425-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="66425-155">新規コンテナー、CONT0001 を作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="66425-156">9 個をコンテナー CONT0001 に配置します。</span><span class="sxs-lookup"><span data-stu-id="66425-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="66425-157">HDMI ケーブル 18':</span><span class="sxs-lookup"><span data-stu-id="66425-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="66425-158">品目がコンテナー CONT0001 に適合するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="66425-159">新規コンテナー、CONT0002 を作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="66425-160">5 個をコンテナー CONT0002 に配置します。</span><span class="sxs-lookup"><span data-stu-id="66425-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="66425-161">新規コンテナー、CONT0003 を作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="66425-162">3 個をコンテナー CONT0003 に配置します。</span><span class="sxs-lookup"><span data-stu-id="66425-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="66425-163">HDMI ケーブル 18':</span><span class="sxs-lookup"><span data-stu-id="66425-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="66425-164">品目がコンテナー CONT0001 に適合するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="66425-165">新規コンテナー、CONT0002 を作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="66425-166">5 個をコンテナー CONT0002 に配置します。</span><span class="sxs-lookup"><span data-stu-id="66425-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="66425-167">新規コンテナー、CONT0003 を作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="66425-168">3 個をコンテナー CONT0003 に配置します。</span><span class="sxs-lookup"><span data-stu-id="66425-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="66425-169">HDMI ケーブル 6':</span><span class="sxs-lookup"><span data-stu-id="66425-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="66425-170">品目がコンテナー CONT0001 に適合するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="66425-171">1 個をコンテナー CONT0001 に配置します。</span><span class="sxs-lookup"><span data-stu-id="66425-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="66425-172">品目がコンテナー CONT0002 に適合するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="66425-173">品目がコンテナー CONT0003 に適合するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="66425-174">4 個をコンテナー CONT0003 に配置します。</span><span class="sxs-lookup"><span data-stu-id="66425-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="66425-175">新規コンテナー、CONT0004 を作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="66425-176">8 個をコンテナー CONT0004 に配置します。</span><span class="sxs-lookup"><span data-stu-id="66425-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="66425-177">HDMI ケーブル 6':</span><span class="sxs-lookup"><span data-stu-id="66425-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="66425-178">品目がコンテナー CONT0003 に適合するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="66425-179">4 個をコンテナー CONT0003 に配置します。</span><span class="sxs-lookup"><span data-stu-id="66425-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="66425-180">新規コンテナー、CONT0004 を作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="66425-181">9 個をコンテナー CONT0004 に配置します。</span><span class="sxs-lookup"><span data-stu-id="66425-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="66425-182">シナリオ例: コンテナーごとの単一の注文の梱包</span><span class="sxs-lookup"><span data-stu-id="66425-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="66425-183">このセクションでは、複数の注文を 1 つの出荷に連結するためにシステムが設定されているシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="66425-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="66425-184">したがって、複数の製品を含むすべての注文が独自のコンテナーに梱包されるのを確認するために、販売注文からコンテナー詰めが行われます。</span><span class="sxs-lookup"><span data-stu-id="66425-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="66425-185">この機能を使用すると、各コンテナーに 1 つの販売注文のみを梱包する必要があるシナリオを処理できるため、物流センターは小売店舗間で完全なコンテナーをクロスドッキングすることができます。</span><span class="sxs-lookup"><span data-stu-id="66425-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="66425-186">小売シナリオ (小売店舗ごとの注文およびクロスドッキング用の物流センターへの出荷) に加えて、この技術は、リーン サプライ チェーン (Just-In-Time 生産ラインごとの販売注文) でも一般的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="66425-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="66425-187">このシナリオでは、コンテナー詰めの *現在のコンテナーにのみ梱包* 計画を使用して、梱包中に評価されるコンテナーの数を減少する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="66425-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="66425-188">必要条件</span><span class="sxs-lookup"><span data-stu-id="66425-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="66425-189">システムで出荷連結機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="66425-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="66425-190">このシナリオでは、*出荷連結* 機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="66425-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="66425-191">この機能をシステムで使用できない場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用してオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="66425-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="66425-192">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="66425-192">Make demo data available</span></span>

<span data-ttu-id="66425-193">このシナリオでは、Microsoft Dynamics 365 Supply Chain Management に用意されている標準のデモ データに含まれる値とレコードを参照します。</span><span class="sxs-lookup"><span data-stu-id="66425-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="66425-194">ここで提供されている値を使用するには、デモデータがインストールされている環境で作業し、開始する前に法人を **usmf** に設定します。</span><span class="sxs-lookup"><span data-stu-id="66425-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="66425-195">コンテナー タイプの検査または作成</span><span class="sxs-lookup"><span data-stu-id="66425-195">Inspect or create container types</span></span>

<span data-ttu-id="66425-196">コンテナー タイプを検査したり、必要に応じて新しいコンテナー タイプを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="66425-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="66425-197">**Warehouse Management** \> **設定** \> **コンテナー** \> **コンテナー タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="66425-198">次の各コンテナー タイプがデモ データで利用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="66425-199">必要に応じてコンテナー タイプを編集または作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="66425-200">コンテナー タイプ 1:</span><span class="sxs-lookup"><span data-stu-id="66425-200">Container type 1:</span></span>

        - <span data-ttu-id="66425-201">**コンテナー タイプ コード:** *ボックス - 大*</span><span class="sxs-lookup"><span data-stu-id="66425-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="66425-202">**説明:** *大型ボックス*</span><span class="sxs-lookup"><span data-stu-id="66425-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="66425-203">**最大正味重量:** *100*</span><span class="sxs-lookup"><span data-stu-id="66425-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="66425-204">**容積:** *400*</span><span class="sxs-lookup"><span data-stu-id="66425-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="66425-205">**期間:** *4*</span><span class="sxs-lookup"><span data-stu-id="66425-205">**Length:** *4*</span></span>
        - <span data-ttu-id="66425-206">**幅:** *10*</span><span class="sxs-lookup"><span data-stu-id="66425-206">**Width:** *10*</span></span>
        - <span data-ttu-id="66425-207">**高さ:** *10*</span><span class="sxs-lookup"><span data-stu-id="66425-207">**Height:** *10*</span></span>

    - <span data-ttu-id="66425-208">コンテナー タイプ 2:</span><span class="sxs-lookup"><span data-stu-id="66425-208">Container type 2:</span></span>

        - <span data-ttu-id="66425-209">**コンテナー タイプ コード:** *ボックス - 中*</span><span class="sxs-lookup"><span data-stu-id="66425-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="66425-210">**説明:** *中型ボックス*</span><span class="sxs-lookup"><span data-stu-id="66425-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="66425-211">**最大正味重量:** *50*</span><span class="sxs-lookup"><span data-stu-id="66425-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="66425-212">**容積:** *200*</span><span class="sxs-lookup"><span data-stu-id="66425-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="66425-213">**期間:** *2*</span><span class="sxs-lookup"><span data-stu-id="66425-213">**Length:** *2*</span></span>
        - <span data-ttu-id="66425-214">**幅:** *10*</span><span class="sxs-lookup"><span data-stu-id="66425-214">**Width:** *10*</span></span>
        - <span data-ttu-id="66425-215">**高さ:** *10*</span><span class="sxs-lookup"><span data-stu-id="66425-215">**Height:** *10*</span></span>

    - <span data-ttu-id="66425-216">コンテナー タイプ 3:</span><span class="sxs-lookup"><span data-stu-id="66425-216">Container type 3:</span></span>

        - <span data-ttu-id="66425-217">**コンテナー タイプ コード:** *ボックス - 小*</span><span class="sxs-lookup"><span data-stu-id="66425-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="66425-218">**説明:** *小型ボックス*</span><span class="sxs-lookup"><span data-stu-id="66425-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="66425-219">**最大正味重量:** *20*</span><span class="sxs-lookup"><span data-stu-id="66425-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="66425-220">**容積:** *100*</span><span class="sxs-lookup"><span data-stu-id="66425-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="66425-221">**期間:** *1*</span><span class="sxs-lookup"><span data-stu-id="66425-221">**Length:** *1*</span></span>
        - <span data-ttu-id="66425-222">**幅:** *10*</span><span class="sxs-lookup"><span data-stu-id="66425-222">**Width:** *10*</span></span>
        - <span data-ttu-id="66425-223">**高さ:** *10*</span><span class="sxs-lookup"><span data-stu-id="66425-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="66425-224">コンテナー グループの検査または作成</span><span class="sxs-lookup"><span data-stu-id="66425-224">Inspect or create container groups</span></span>

<span data-ttu-id="66425-225">コンテナー グループを検査したり、必要に応じて新しいコンテナー グループを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="66425-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="66425-226">**倉庫管理** \> **設定** \> **コンテナー** \> **コンテナー グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="66425-227">次のコンテナー グループがデモ データで利用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="66425-228">利用できない場合は、**新規** を選択して作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="66425-229">**コンテナー グループ ID:** *ボックス*</span><span class="sxs-lookup"><span data-stu-id="66425-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="66425-230">**説明:** *ボックス サイズ*</span><span class="sxs-lookup"><span data-stu-id="66425-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="66425-231">*ボックス* コンテナー グループの **詳細** クイックタブで、次の明細行が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="66425-232">存在しない場合は、**新規** を選択して追加します。</span><span class="sxs-lookup"><span data-stu-id="66425-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="66425-233">明細行 1:</span><span class="sxs-lookup"><span data-stu-id="66425-233">Line 1:</span></span>

        - <span data-ttu-id="66425-234">**シーケンス番号:** *1*</span><span class="sxs-lookup"><span data-stu-id="66425-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="66425-235">**コンテナー タイプ:** *ボックス-大*</span><span class="sxs-lookup"><span data-stu-id="66425-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="66425-236">**コンテナー使用率の割合:** *100*</span><span class="sxs-lookup"><span data-stu-id="66425-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="66425-237">明細行 2:</span><span class="sxs-lookup"><span data-stu-id="66425-237">Line 2:</span></span>

        - <span data-ttu-id="66425-238">**シーケンス番号:** *2*</span><span class="sxs-lookup"><span data-stu-id="66425-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="66425-239">**コンテナー タイプ:** *ボックス - 中*</span><span class="sxs-lookup"><span data-stu-id="66425-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="66425-240">**コンテナー使用率の割合:** *100*</span><span class="sxs-lookup"><span data-stu-id="66425-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="66425-241">明細行 3:</span><span class="sxs-lookup"><span data-stu-id="66425-241">Line 3:</span></span>

        - <span data-ttu-id="66425-242">**シーケンス番号:** *3*</span><span class="sxs-lookup"><span data-stu-id="66425-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="66425-243">**コンテナー タイプ:** *ボックス - 小*</span><span class="sxs-lookup"><span data-stu-id="66425-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="66425-244">**コンテナー使用率の割合:** *100*</span><span class="sxs-lookup"><span data-stu-id="66425-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="66425-245">新しいコンテナー構築テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="66425-245">Create a new container build template</span></span>

<span data-ttu-id="66425-246">新しいコンテナー構築テンプレートを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="66425-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="66425-247">**倉庫管理** \> **設定** \> **コンテナー** \> **コンテナー構築テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="66425-248">**新規** を選択して、次の設定を持つコンテナー構築テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="66425-249">**シーケンス番号:** *1*</span><span class="sxs-lookup"><span data-stu-id="66425-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="66425-250">**コンテナー テンプレート ID:** *ボックス*</span><span class="sxs-lookup"><span data-stu-id="66425-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="66425-251">**コンテナー グループ ID:** *ボックス*</span><span class="sxs-lookup"><span data-stu-id="66425-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="66425-252">**基準クエリ タイプ:** *販売配賦ライン*</span><span class="sxs-lookup"><span data-stu-id="66425-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="66425-253">**ウェーブ ステップ コード:** *234*</span><span class="sxs-lookup"><span data-stu-id="66425-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="66425-254">**分割ピッキングを許可する:** *はい*</span><span class="sxs-lookup"><span data-stu-id="66425-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="66425-255">**コンテナー梱包計画:** *現在のコンテナーにのみ梱包*</span><span class="sxs-lookup"><span data-stu-id="66425-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="66425-256">**ディレクティブ出荷単位ごとの梱包:** *いいえ*</span><span class="sxs-lookup"><span data-stu-id="66425-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="66425-257">新しいテンプレートの行がまだ選択されている間に、アクション ウィンドウで **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="66425-258">標準のクエリ エディター ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="66425-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="66425-259">**並べ替え** タブで、**追加** を選択して次の設定を持つ行を追加します。</span><span class="sxs-lookup"><span data-stu-id="66425-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="66425-260">**テーブル:** *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="66425-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="66425-261">**派生テーブル:** *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="66425-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="66425-262">**フィールド:** *注文番号*</span><span class="sxs-lookup"><span data-stu-id="66425-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="66425-263">**検索の方法:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="66425-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="66425-264">その他すべてのオープン コンテナーのサイクル オーバーを回避し、1 つのコンテナーを一度にチェックしてプロセスを高速化するには、注文番号による並べ替えに加えて *現在のコンテナーにのみ梱包* 計画を使用します。</span><span class="sxs-lookup"><span data-stu-id="66425-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="66425-265">この組み合わせは、作業テンプレートのワーク ブレイクのように機能します。</span><span class="sxs-lookup"><span data-stu-id="66425-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="66425-266">**OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="66425-267">新しいテンプレートの行がまだ選択されている間に、アクション ウィンドウで **コンテナー混合の制約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="66425-268">1 つの注文の品目を 1 つのコンテナーに入れる制約を追加します。</span><span class="sxs-lookup"><span data-stu-id="66425-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="66425-269">他の注文からの品目は別のコンテナーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="66425-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="66425-270">**新規** を選択して、次の設定を持つ混合の制約を作成します。</span><span class="sxs-lookup"><span data-stu-id="66425-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="66425-271">**テーブル:** *販売注文*</span><span class="sxs-lookup"><span data-stu-id="66425-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="66425-272">**フィールドの選択:** *SalesId* (フィールドはグリッドに *販売注文* として表示されます。)</span><span class="sxs-lookup"><span data-stu-id="66425-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="66425-273">**OK** を選択して制約を追加します。</span><span class="sxs-lookup"><span data-stu-id="66425-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="66425-274">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="66425-275">コンテナー詰めのウェーブ テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="66425-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="66425-276">ウェーブ テンプレートを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="66425-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="66425-277">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="66425-278">一覧 ウィンドウで、**ウェーブ テンプレート タイプ** フィールドを *出荷* に設定します。</span><span class="sxs-lookup"><span data-stu-id="66425-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="66425-279">一覧で **63 コンテナー詰め** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="66425-280">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="66425-281">**メソッド** クイックタブの **選択したメソッド** 列で、次の行を確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="66425-282">**メソッド名:** *コンテナー詰め*</span><span class="sxs-lookup"><span data-stu-id="66425-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="66425-283">**名前:** *コンテナー詰め*</span><span class="sxs-lookup"><span data-stu-id="66425-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="66425-284">明細行の **ウェーブ ステップ コード** フィールドを *234* に設定します。</span><span class="sxs-lookup"><span data-stu-id="66425-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="66425-285">作業テンプレートを設定する</span><span class="sxs-lookup"><span data-stu-id="66425-285">Set up a work template</span></span>

<span data-ttu-id="66425-286">作業テンプレートを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="66425-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="66425-287">**倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="66425-288">**作業指示書タイプ** フィールドを *販売注文* に設定します。</span><span class="sxs-lookup"><span data-stu-id="66425-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="66425-289">**概要** グリッドで、コンテナーごとの単一の注文の梱包で使用する作業テンプレートを検索および選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="66425-290">このシナリオでは **63 ピッキングからコンテナー** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="66425-291">アクション ウィンドウで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="66425-292">標準のクエリ エディター ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="66425-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="66425-293">**並べ替え** タブで、次の明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="66425-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="66425-294">明細行 1:</span><span class="sxs-lookup"><span data-stu-id="66425-294">Line 1:</span></span>

        - <span data-ttu-id="66425-295">**テーブル:** *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="66425-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="66425-296">**派生テーブル:** *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="66425-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="66425-297">**フィールド:** *出荷 ID*</span><span class="sxs-lookup"><span data-stu-id="66425-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="66425-298">**検索の方法:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="66425-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="66425-299">明細行 2:</span><span class="sxs-lookup"><span data-stu-id="66425-299">Line 2:</span></span>

        - <span data-ttu-id="66425-300">**テーブル:** *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="66425-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="66425-301">**派生テーブル:** *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="66425-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="66425-302">**フィールド:** *注文番号*</span><span class="sxs-lookup"><span data-stu-id="66425-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="66425-303">**検索の方法:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="66425-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="66425-304">明細行 3:</span><span class="sxs-lookup"><span data-stu-id="66425-304">Line 3:</span></span>

        - <span data-ttu-id="66425-305">**テーブル:** *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="66425-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="66425-306">**派生テーブル:** *一時的な作業トランザクション*</span><span class="sxs-lookup"><span data-stu-id="66425-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="66425-307">**フィールド:** *コンテナー ID*</span><span class="sxs-lookup"><span data-stu-id="66425-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="66425-308">**検索の方法:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="66425-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="66425-309">**OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="66425-310">次のメッセージが表示されます: "グループはリセットされますが、続行しますか?"</span><span class="sxs-lookup"><span data-stu-id="66425-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="66425-311">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="66425-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="66425-312">While the **63 ピッキングからコンテナー** テンプレートがまだ選択されている間に、アクション ウィンドウで **作業ヘッダーの分割** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="66425-313">次に、作業を分割する設定を適用して、注文の各コンテナーが 1 つの作業指示書にリンクされるようにします。</span><span class="sxs-lookup"><span data-stu-id="66425-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="66425-314">**作業ヘッダーの分割** ページ (**出荷 ID**、**注文番号**、**コンテナー ID**) で各行の **このフィールドでグループ化する** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="66425-315">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="66425-316">出荷連結ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="66425-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="66425-317">出荷連結ポリシーを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="66425-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="66425-318">**倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="66425-319">一覧ウィンドウで、**ポリシー タイプ** フィールドを *販売注文* に設定します。</span><span class="sxs-lookup"><span data-stu-id="66425-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="66425-320">一覧で、**既定** ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="66425-321">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="66425-322">**連結フィールド** クイックタブの **選択したフィールド** の一覧で、**フィールド名** フィールドが *注文番号* に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="66425-323">**削除** ボタンの ![左矢印](media/backward-button.png) を選択して、フィールドを **残りのフィールド** 一覧に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="66425-324">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="66425-325">製品の現物分析コードの設定</span><span class="sxs-lookup"><span data-stu-id="66425-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="66425-326">このシナリオで使用される製品の現物分析コードを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="66425-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="66425-327">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="66425-328">**品目番号** フィールドが *A0001* に設定されている製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="66425-329">アクション ペインの **在庫の管理** タブの **倉庫** グループで、**現物分析コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="66425-330">**現物分析コード** ページのグリッドには次の明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="66425-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="66425-331">**ユニット:** *pcs*</span><span class="sxs-lookup"><span data-stu-id="66425-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="66425-332">**総重量:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="66425-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="66425-333">**幅:** *2.00*</span><span class="sxs-lookup"><span data-stu-id="66425-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="66425-334">**奥行き:** *2.00*</span><span class="sxs-lookup"><span data-stu-id="66425-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="66425-335">**高さ:** *4.00*</span><span class="sxs-lookup"><span data-stu-id="66425-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="66425-336">**容積:** *16.00*</span><span class="sxs-lookup"><span data-stu-id="66425-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="66425-337">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-337">Close the page.</span></span>
1. <span data-ttu-id="66425-338">**品目番号** フィールドが *A0002* に設定されている製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="66425-339">アクション ペインの **在庫の管理** タブの **倉庫** グループで、**現物分析コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="66425-340">**現物分析コード** ページのグリッドには次の明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="66425-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="66425-341">**ユニット:** *pcs*</span><span class="sxs-lookup"><span data-stu-id="66425-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="66425-342">**総重量:** *4.00*</span><span class="sxs-lookup"><span data-stu-id="66425-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="66425-343">**幅:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="66425-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="66425-344">**奥行き:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="66425-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="66425-345">**高さ:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="66425-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="66425-346">**容積:** *9.00*</span><span class="sxs-lookup"><span data-stu-id="66425-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="66425-347">販売注文の作成 1</span><span class="sxs-lookup"><span data-stu-id="66425-347">Create sales order 1</span></span>

<span data-ttu-id="66425-348">販売注文を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="66425-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="66425-349">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="66425-350">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="66425-351">新しい販売注文を作成するためのダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="66425-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="66425-352">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="66425-352">Set the following values:</span></span>

    - <span data-ttu-id="66425-353">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="66425-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="66425-354">**倉庫:** *63*</span><span class="sxs-lookup"><span data-stu-id="66425-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="66425-355">**OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="66425-356">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="66425-356">The new sales order is opened.</span></span> <span data-ttu-id="66425-357">**販売注文明細行** クイックタブで、次の販売明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="66425-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="66425-358">明細行 1:</span><span class="sxs-lookup"><span data-stu-id="66425-358">Line 1:</span></span>

        - <span data-ttu-id="66425-359">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="66425-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="66425-360">**数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="66425-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="66425-361">明細行 2:</span><span class="sxs-lookup"><span data-stu-id="66425-361">Line 2:</span></span>

        - <span data-ttu-id="66425-362">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="66425-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="66425-363">**数量:** *2*</span><span class="sxs-lookup"><span data-stu-id="66425-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="66425-364">最初の明細行を選択し、**在庫 \> 予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="66425-365">**予約** ページで、**ロットの予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="66425-366">その後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-366">Then close the page.</span></span>
1. <span data-ttu-id="66425-367">2 つ目の明細行について前の 2 つの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="66425-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="66425-368">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="66425-369">販売注文の作成 2</span><span class="sxs-lookup"><span data-stu-id="66425-369">Create sales order 2</span></span>

<span data-ttu-id="66425-370">2 つ目の販売注文を作成売るには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="66425-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="66425-371">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="66425-372">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="66425-373">新しい販売注文を作成するためのダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="66425-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="66425-374">次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="66425-374">Set the following values:</span></span>

    - <span data-ttu-id="66425-375">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="66425-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="66425-376">**倉庫:** *63*</span><span class="sxs-lookup"><span data-stu-id="66425-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="66425-377">**OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="66425-378">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="66425-378">The new sales order is opened.</span></span> <span data-ttu-id="66425-379">**販売注文明細行** クイックタブで、次の販売明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="66425-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="66425-380">明細行 1:</span><span class="sxs-lookup"><span data-stu-id="66425-380">Line 1:</span></span>

        - <span data-ttu-id="66425-381">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="66425-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="66425-382">**数量:** *4*</span><span class="sxs-lookup"><span data-stu-id="66425-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="66425-383">明細行 2:</span><span class="sxs-lookup"><span data-stu-id="66425-383">Line 2:</span></span>

        - <span data-ttu-id="66425-384">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="66425-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="66425-385">**数量:** *4*</span><span class="sxs-lookup"><span data-stu-id="66425-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="66425-386">最初の明細行を選択し、**在庫 \> 予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="66425-387">**予約** ページで、**ロットの予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="66425-388">その後、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-388">Then close the page.</span></span>
1. <span data-ttu-id="66425-389">2 つ目の明細行について前の 2 つの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="66425-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="66425-390">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="66425-391">積荷の作成</span><span class="sxs-lookup"><span data-stu-id="66425-391">Create the load</span></span>

<span data-ttu-id="66425-392">このシナリオで作成した各注文に対して積荷を作成し、それを倉庫にリリースするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="66425-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="66425-393">**倉庫管理 \> 積荷 \> 積荷計画ワークベンチ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="66425-394">**販売明細行** タブで、このシナリオに対して作成した販売注文から、すべての販売注文明細行を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="66425-395">アクション ウィンドウの、**供給と需要** タブの **追加** グループで、**新しい積荷へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="66425-396">選択した注文明細行が新しい積荷に追加されます。</span><span class="sxs-lookup"><span data-stu-id="66425-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="66425-397">**積荷のテンプレート割り当て** ダイアログ ボックスの **積荷のテンプレート ID** フィールドで、*40' コンテナー* などの積荷テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="66425-398">**OK** を選択してダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66425-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="66425-399">**積荷** セクションで、作成した積荷を見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="66425-400">**リリース \> 倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="66425-401">**倉庫へのリリース** ダイアログ ボックスで、**OK** を選択し選択した積荷を倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="66425-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="66425-402">出荷とコンテナーの検証</span><span class="sxs-lookup"><span data-stu-id="66425-402">Verify the shipments and containers</span></span>

<span data-ttu-id="66425-403">次の手順では、作成された出荷を確認できます。</span><span class="sxs-lookup"><span data-stu-id="66425-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="66425-404">これを使用して、このシナリオで作成した注文を確認し、予期される結果が得られるようにします。</span><span class="sxs-lookup"><span data-stu-id="66425-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="66425-405">**倉庫管理 \> 出荷 \> すべての出荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="66425-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="66425-406">リリースした積荷に対して作成された出荷を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="66425-407">アクション ウィンドウの **輸送** タブで、**コンテナーの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="66425-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="66425-408">販売注文の品目が 2 つの異なるコンテナーにコンテナー化されているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="66425-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="66425-409">追加リソース</span><span class="sxs-lookup"><span data-stu-id="66425-409">Additional resources</span></span>

- [<span data-ttu-id="66425-410">コンテナー詰め</span><span class="sxs-lookup"><span data-stu-id="66425-410">Containerization</span></span>](wave-containerization.md)
