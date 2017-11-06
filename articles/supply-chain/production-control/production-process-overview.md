---
title: "生産プロセスの概要"
description: "この記事では、生産プロセスの概要を示します。 製造オーダー、バッチ オーダー、およびかんばんのオーダーの作成から財務期間の決算までのさまざまなステージについて説明します。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgProdStatusListPage, JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19832
ms.assetid: 0e83c7ea-feba-4ed6-8717-8b48a3b8804a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e50e64057d19d0e1fbf5645c2abc31fbd19ea43a
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="production-process-overview"></a><span data-ttu-id="34657-104">生産プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="34657-104">Production process overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="34657-105">この記事では、生産プロセスの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="34657-105">This article gives an overview of the production processes.</span></span> <span data-ttu-id="34657-106">製造オーダー、バッチ オーダー、およびかんばんのオーダーの作成から財務期間の決算までのさまざまなステージについて説明します。</span><span class="sxs-lookup"><span data-stu-id="34657-106">It describes the various stages of production orders, batch orders, and kanbans, from order creation to closing of the financial period.</span></span> 

<span data-ttu-id="34657-107">製品の生産 (生産ライフ サイクルとも呼ばれるプロセス) は、品目の製造に必要な手順に従って行われます。</span><span class="sxs-lookup"><span data-stu-id="34657-107">The production of products, a process that is also known as the production life cycle, follows specific steps that are required to complete the manufacture of an item.</span></span> <span data-ttu-id="34657-108">ライフ サイクルは、製造オーダー、バッチ オーダー、またはかんばんの作成で始まります。</span><span class="sxs-lookup"><span data-stu-id="34657-108">The life cycle begins with the creation of the production order, batch order, or kanban.</span></span> <span data-ttu-id="34657-109">完成した、顧客への提供または別の生産フェーズへの準備が整っている製品により終了します。</span><span class="sxs-lookup"><span data-stu-id="34657-109">It ends with a finished, manufactured item that is ready for either a customer or another phase of production.</span></span> <span data-ttu-id="34657-110">ライフ サイクルの各ステップでプロセスを実行するにはさまざまな情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="34657-110">Each step in the life cycle requires different kinds of information to complete the process.</span></span> <span data-ttu-id="34657-111">各ステップが完了すると、製造オーダー、バッチ オーダー、かんばんでの生産状態に変化が生じます。</span><span class="sxs-lookup"><span data-stu-id="34657-111">As each step is completed, the production order, batch order, or kanban shows a change in the production status.</span></span> <span data-ttu-id="34657-112">さまざまな製品タイプごとに、異なる製造プロセスが要求されます。</span><span class="sxs-lookup"><span data-stu-id="34657-112">Different types of products require different manufacturing processes.</span></span>  

<span data-ttu-id="34657-113">[**生産管理**] モジュールは、他のモジュールにリンクされています。たとえば [**製品情報管理**]、[**在庫管理**]、[**総勘定元帳**]、[**倉庫管理**]、[**プロジェクト会計**]、および [**組織管理**] などです。</span><span class="sxs-lookup"><span data-stu-id="34657-113">The **Production control** module is linked to other modules, such as **Product information management**, **Inventory management**, **General ledger**, **Warehouse management**, **Project accounting**, and **Organization administration**.</span></span> <span data-ttu-id="34657-114">この統合では、完成品目の製造に必要な情報フローをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="34657-114">This integration supports the information flow that is required to complete the manufacturing of a finished item.</span></span>  

<span data-ttu-id="34657-115">生産プロセスは、通常、特定の生産プロセスに対して選択された原価計算と在庫評価方法からの影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="34657-115">The production process is typically influenced by the cost accounting and inventory valuation methods that are chosen for a specific production process.</span></span> <span data-ttu-id="34657-116">Finance and Operations は、実績原価 (先入れ先出し \[FIFO\]、後入れ先出し \[LIFO\]、移動平均、および周期加重平均) と標準原価方法の両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="34657-116">Finance and Operations supports both actual cost (first in, first out \[FIFO\]; last in, first out \[LIFO\]; moving average; and periodic weighted average) and standard cost methods.</span></span> <span data-ttu-id="34657-117">リーン生産は、一括引き落とし原価計算原則に基づいて実行されます。</span><span class="sxs-lookup"><span data-stu-id="34657-117">Lean manufacturing is implemented based on the backflush costing principle.</span></span>  

<span data-ttu-id="34657-118">原価計算方法の選択は、生産プロセス中の材料およびリソースの消費に関する報告の要件も定義します。</span><span class="sxs-lookup"><span data-stu-id="34657-118">The choice of the cost measurement methods also defines the requirements for reporting about material and resource consumption during the production process.</span></span> <span data-ttu-id="34657-119">通常、実績原価法ではジョブ レベルの正確なレポートが必要で、周期原価計算法ではより粗い粒度の材料およびリソースの消費報告でも可能です。</span><span class="sxs-lookup"><span data-stu-id="34657-119">Typically, actual cost methods require accurate reporting on the job level, whereas periodic costing methods allow for less granular reporting of material and resource consumption.</span></span>

## <a name="mixed-mode-manufacturing"></a><span data-ttu-id="34657-120">混合モード製造</span><span class="sxs-lookup"><span data-stu-id="34657-120">Mixed mode manufacturing</span></span>
<span data-ttu-id="34657-121">さまざまな製品と生産のトポロジーで、さまざまな注文タイプの適用が要求されます。</span><span class="sxs-lookup"><span data-stu-id="34657-121">Different products and production topologies require the application of different order types.</span></span> <span data-ttu-id="34657-122">Finance and Operations では、混合モードで、さまざまな注文タイプに対応します。</span><span class="sxs-lookup"><span data-stu-id="34657-122">Finance and Operations can apply the various order types in a mixed mode.</span></span> <span data-ttu-id="34657-123">つまり、すべての注文タイプが、1 つの製品を製造するエンド ツー エンドのプロセス中に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="34657-123">In other words, all order types can occur during the end-to-end process of producing one finished product.</span></span>

-   <span data-ttu-id="34657-124">**製造オーダー** – これは、古典的な注文タイプで、特定の製品または製品バリアントを、数量と日付を指定して製造します。</span><span class="sxs-lookup"><span data-stu-id="34657-124">**Production order** – This is the classic order type to produce a specific product or product variant in a given quantity on a specific date.</span></span> <span data-ttu-id="34657-125">製造オーダーは、部品表 (BOM) と工順に基づきます。</span><span class="sxs-lookup"><span data-stu-id="34657-125">Production orders are based on bills of materials (BOMs) and routes.</span></span>
-   <span data-ttu-id="34657-126">**バッチ オーダー** – この注文タイプは、プロセス産業と個別プロセスに使用します。そこでは、式に基づいた生産変換が行われるか、主要製品に加えてまたは代わりとして連産品と副産物が最終製品になります。</span><span class="sxs-lookup"><span data-stu-id="34657-126">**Batch order** – This order type is used for process industries and discrete processes where the manufacturing conversion is based on a formula, or where co-products and by-products can be end products, either in addition to or instead of the main product.</span></span> <span data-ttu-id="34657-127">バッチ オーダーが**式**タイプの BOM および工順を使用します。</span><span class="sxs-lookup"><span data-stu-id="34657-127">Batch orders use **Formula** type BOMs and routes.</span></span>
-   <span data-ttu-id="34657-128">**かんばん** – かんばんは、生産フロー、かんばんルール、BOM に基づいた反復的なリーン生産プロセスへの通知として使用します。</span><span class="sxs-lookup"><span data-stu-id="34657-128">**Kanban** – Kanbans are used to signal repetitive lean manufacturing processes that are based on production flows, kanban rules, and BOMs.</span></span>
-   <span data-ttu-id="34657-129">**プロジェクト** – 製造プロジェクトは、製品とサービスを、特定のスケジュールと予算に結び付けます。</span><span class="sxs-lookup"><span data-stu-id="34657-129">**Project** – A manufacturing project combines products and services with a given schedule and budget.</span></span> <span data-ttu-id="34657-130">プロジェクトの製造の部分は、他のどの注文タイプでも提供できます。</span><span class="sxs-lookup"><span data-stu-id="34657-130">The manufacturing part of a project can be delivered through any of the other order types.</span></span>

## <a name="manufacturing-principles"></a><span data-ttu-id="34657-131">製造原則</span><span class="sxs-lookup"><span data-stu-id="34657-131">Manufacturing principles</span></span>
<span data-ttu-id="34657-132">特定の製品および関連市場に最もふさわしい製造原則を選択するには、製造および物流を考慮し、出荷のリード タイムに関する顧客の期待を考える必要があります。</span><span class="sxs-lookup"><span data-stu-id="34657-132">To select the manufacturing principle that best applies to a particular product and related market, you must consider the requirements of production and logistics, and also customer expectations about delivery lead times.</span></span>

-   <span data-ttu-id="34657-133">**製造から在庫** – これは、予測または最小在庫補充に基づいて、製造した製品を在庫にする古典的な製造原則です。(最小在庫補充は予測または消費履歴に基づいて計算されます)</span><span class="sxs-lookup"><span data-stu-id="34657-133">**Make to stock** – This is the classic manufacturing principle, where products are produced for stock, based on forecast or minimum stock refill (the latter is typically calculated based on forecast or historic consumption).</span></span>
-   <span data-ttu-id="34657-134">**受注生産** – 標準製品を、注文により生産または注文により完成させます。</span><span class="sxs-lookup"><span data-stu-id="34657-134">**Make to order** – Standard products are made to order or finished to order.</span></span> <span data-ttu-id="34657-135">生産開始前の段取りは「製造から在庫」の原則で行われる場合がありますが、バリュー チェーンで費用のかかる手順またはバリアントを作成する手順は、販売注文や移動オーダーが引き金となります。</span><span class="sxs-lookup"><span data-stu-id="34657-135">Although pre-production might be done by using the Make to stock principle, expensive steps of the value chain, or steps that create variants, are triggered by a sales order or transfer order.</span></span>
-   <span data-ttu-id="34657-136">**注文により構成** – 受注生産の原則では、バリュー チェーンの最終工程は受注による生産です。</span><span class="sxs-lookup"><span data-stu-id="34657-136">**Configure to order** – As for the Make to order principle, the final operations of the value chain are made to order.</span></span> <span data-ttu-id="34657-137">生産される実際の製品バリアントは事前定義がありませんが、販売製品のコンフィギュレーション モデルに基づいて注文入力時に作成されます。</span><span class="sxs-lookup"><span data-stu-id="34657-137">The actual product variant that is produced isn't predefined but is created at the time of order entry, based on the configuration model of the sales product.</span></span> <span data-ttu-id="34657-138">「注文により構成」の原則では、特定の製品ラインに対して一定レベルの統一プロセスが求められます。</span><span class="sxs-lookup"><span data-stu-id="34657-138">The Configure to order principle requires a certain level of process unification for a given product line.</span></span>
-   <span data-ttu-id="34657-139">**個別受注生産** – 個別受注生産プロセスは、プロジェクトとも呼ばれ、通常は設計フェーズから開始します。</span><span class="sxs-lookup"><span data-stu-id="34657-139">**Engineer to order** – Engineer to order processes are typically adressed by a project and usually start with the engineering phase.</span></span> <span data-ttu-id="34657-140">設計フェーズ中に、注文を満たすような実際の製品が、設計され記述されます。</span><span class="sxs-lookup"><span data-stu-id="34657-140">During the engineering phase, the actual products that are required fulfill the order are designed and described.</span></span> <span data-ttu-id="34657-141">その後、製品の製造のために製造オーダー、バッチ オーダー、かんばんを作成できます。</span><span class="sxs-lookup"><span data-stu-id="34657-141">Production orders, batch orders, or kanbans can then be created to produce the products.</span></span>

## <a name="overview-of-the-production-life-cycle"></a><span data-ttu-id="34657-142">生産ライフ サイクルの概要</span><span class="sxs-lookup"><span data-stu-id="34657-142">Overview of the production life cycle</span></span>
<span data-ttu-id="34657-143">生産ライフ サイクルの中の次の手順は、混合モード製造のすべての注文タイプに対して実行できます。</span><span class="sxs-lookup"><span data-stu-id="34657-143">The following steps in the production life cycle can occur for all order types of mixed mode manufacturing.</span></span> <span data-ttu-id="34657-144">ただし、すべてが明確な注文ステータスを代表しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="34657-144">However, not all of them are represented as an explicit order status.</span></span>

1.  <span data-ttu-id="34657-145">**作成済** – 製造オーダー、バッチ オーダー、かんばんを手動で作成することができます。また、さまざまな要求通知に基づいてそれらを生成するようにシステムを構成できます。</span><span class="sxs-lookup"><span data-stu-id="34657-145">**Created** – You can create a production order, batch order, or kanban manually, or you can configure the system to generate them based on various demand signals.</span></span> <span data-ttu-id="34657-146">マスター プランは、計画オーダーの確定して製造オーダー、バッチ オーダー、またはかんばんを作成します。</span><span class="sxs-lookup"><span data-stu-id="34657-146">Master planning creates production orders, batch orders, or kanbans by firming planned orders.</span></span> <span data-ttu-id="34657-147">他の要求信号とは、他の製造オーダーやかんばんからの、販売注文やペギングされた供給の信号です。</span><span class="sxs-lookup"><span data-stu-id="34657-147">Other demand signals are sales orders or pegged supply signals from other production orders or kanbans.</span></span> <span data-ttu-id="34657-148">固定数量かんばんの場合、要求信号は、かんばんが空として登録されるときに生成されます。</span><span class="sxs-lookup"><span data-stu-id="34657-148">For fixed-quantity kanbans, demand signals are generated when kanbans are registered as empty.</span></span>
2.  <span data-ttu-id="34657-149">**見積済** – 材料とリソースの消費の見積を計算できます。</span><span class="sxs-lookup"><span data-stu-id="34657-149">**Estimated** – You can calculate estimates for material and resource consumption.</span></span> <span data-ttu-id="34657-150">見積では、原材料の在庫トランザクションが**注文中**ステータスで生成されます 。</span><span class="sxs-lookup"><span data-stu-id="34657-150">The estimation generates inventory transactions for raw materials that have a status of **On order**.</span></span> <span data-ttu-id="34657-151">製造オーダーまたはバッチ オーダーが推定されると、主要製品、副産物、および副産物の受領書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="34657-151">The receipts for main products, co-products, and by-products are generate when production orders or batch orders are estimated.</span></span> <span data-ttu-id="34657-152">BOM に [**ペギングされた供給**] タイプの明細行がある場合、材料の発注書や外注された工程のサービスの発注書が生成され、製造オーダーやバッチ オーダーにペギングされます。</span><span class="sxs-lookup"><span data-stu-id="34657-152">If the BOM contains lines of the **Pegged supply** type, purchase orders for materials or subcontracted operation services are generated and pegged to the production order or batch order.</span></span> <span data-ttu-id="34657-153">品目や注文は、製造オーダーの引当の方針に従って引当され、完成品の価格はパラメータ設定に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="34657-153">Items or orders are reserved according to the reservation strategy of the production order, and the price of the finished goods is calculated based on parameter settings.</span></span>
3.  <span data-ttu-id="34657-154">**スケジュール済** – 工程、個別のジョブ、またはその両方に基づいて、生産のスケジュールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="34657-154">**Scheduled** – You can schedule production based on operations, individual jobs, or both.</span></span>
    -   <span data-ttu-id="34657-155">**工程のスケジューリング** – このスケジューリング方法は、大まかな長期の計画に使用します。</span><span class="sxs-lookup"><span data-stu-id="34657-155">**Operations scheduling** – This scheduling method provides a rough, long-term plan.</span></span> <span data-ttu-id="34657-156">この方法を使用すると、製造オーダーに開始日と終了日を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="34657-156">By using this method, you can assign start and end dates to production orders.</span></span> <span data-ttu-id="34657-157">製造オーダーが工順工程に関連付けられている場合は、原価センター グループに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="34657-157">If the production orders are attached to route operations, you can assign them to cost center groups.</span></span>
    -   <span data-ttu-id="34657-158">**ジョブのスケジューリング** – このスケジューリング方法は、詳細な計画に使用します。</span><span class="sxs-lookup"><span data-stu-id="34657-158">**Job scheduling** – This scheduling method provides a detailed plan.</span></span> <span data-ttu-id="34657-159">各工程は、特定の日付、時刻、および運営リソースが割り当てられた個々のジョブに細分します。</span><span class="sxs-lookup"><span data-stu-id="34657-159">Each operation is broken down into individual jobs that have specific dates, times, and assigned operations resources.</span></span> <span data-ttu-id="34657-160">有限能力を使用する場合は、使用可能な能力に基づいてジョブは運営リソースに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="34657-160">If finite capacity is used, jobs are assigned to operations resources based on availability.</span></span> <span data-ttu-id="34657-161">スケジュールは、ガント チャートで表示および変更できます。</span><span class="sxs-lookup"><span data-stu-id="34657-161">You can view and change the schedule in a Gantt chart.</span></span>
    -   <span data-ttu-id="34657-162">**かんばんスケジュール** – かんばん作業は、かんばんスケジュール ボードでスケジュールされるか、かんばんルールの自動計画の構成に基づいて自動的にスケジューリングされます。</span><span class="sxs-lookup"><span data-stu-id="34657-162">**Kanban schedule** – Kanban jobs are scheduled on the kanban schedule board or automatically scheduled based on the automatic planning configuration of the kanban rules.</span></span>

4.  <span data-ttu-id="34657-163">**リリース済** – 製造オーダーやバッチ オーダーは、スケジュールが終了し、材料がピッキング可能になるか準備完了になると、リリースできます。</span><span class="sxs-lookup"><span data-stu-id="34657-163">**Released** – You can release the production order or batch order when the schedule is finished and the material is available to be picked or prepared.</span></span> <span data-ttu-id="34657-164">材料の使用可能チェックは、作業現場の監修者が、製造オーダーやバッチ オーダーの材料の在庫状態を評価するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="34657-164">The material availability check helps the shop floor supervisor assess the availabilty of material for the production orders or batch orders.</span></span> <span data-ttu-id="34657-165">製造オーダーのドキュメント (ピッキング リスト、ジョブ カード、工順カード、工順ジョブなど) を印刷することもできます。</span><span class="sxs-lookup"><span data-stu-id="34657-165">You can also print the production order documents, such as the pick lists, job card, route card, and route job.</span></span> <span data-ttu-id="34657-166">製造オーダーをリリースすると、製造オーダーのステータスが変更されて、生産を開始できることが示されます。</span><span class="sxs-lookup"><span data-stu-id="34657-166">When the production order is released, the status of the order changes to indicate that the production can begin.</span></span> <span data-ttu-id="34657-167">倉庫管理を使用する場合、製造オーダーまたはバッチ オーダーのリリースは、生産 BOM 明細行を倉庫管理にリリースします。</span><span class="sxs-lookup"><span data-stu-id="34657-167">When warehouse management is used, release of the production order or batch order releases the production BOM lines to warehouse management.</span></span> <span data-ttu-id="34657-168">その後、倉庫のウェーブと倉庫の作業が、倉庫の設定に従って生成されます。</span><span class="sxs-lookup"><span data-stu-id="34657-168">Warehouse waves and warehouse work are then generated according to the setup of the warehouse.</span></span>
5.  <span data-ttu-id="34657-169">[**準備済**] / [**ピッキング済**] – すべての材料とリソースが生産場所でステージ完了すると、生産 BOM 明細行またはかんばん明細行が [**ピッキング済**] のステータスに更新されます。</span><span class="sxs-lookup"><span data-stu-id="34657-169">**Prepared**/**Picked** – When all materials and resources have been staged at the production location, the production BOM lines or kanban lines are updated to a status of **Picked**.</span></span> <span data-ttu-id="34657-170">ペギングされた供給の注文および関連する倉庫の作業は、通常このステージで完成します。</span><span class="sxs-lookup"><span data-stu-id="34657-170">Pegged supply orders and related warehouse work are typically completed at this stage.</span></span> <span data-ttu-id="34657-171">生産の進捗状況を報告するために必要な、かんばんカードまたはジョブ カードが割り当てられ、印刷されます。</span><span class="sxs-lookup"><span data-stu-id="34657-171">The kanban cards or job cards that are required to report production progress should be assigned and printed.</span></span>
6.  <span data-ttu-id="34657-172">**開始済** – 製造オーダー、バッチ オーダー、またはかんばんの開始時に、注文に対して材料とリソースの消費を報告できます。</span><span class="sxs-lookup"><span data-stu-id="34657-172">**Started** – When a production order, batch order, or kanban is started, you can report material and resource consumption against the order.</span></span> <span data-ttu-id="34657-173">注文に割り当てられている材料とリソース消費を、注文の開始時に自動的に転記するよう、システムを構成できます。</span><span class="sxs-lookup"><span data-stu-id="34657-173">The system can be configured to automatically post the material and resource consumption that are allocated to the order when the order is started.</span></span> <span data-ttu-id="34657-174">この割り当てはプレフラッシュ、フォワード フラッシュ、またはオートコンサンプションと呼ばれています。</span><span class="sxs-lookup"><span data-stu-id="34657-174">This allocation is known as preflushing, forward flushing, or autoconsumption.</span></span> <span data-ttu-id="34657-175">追加のピッキング リスト仕訳帳を作成すると、製造オーダーまたはバッチ オーダーに、材料を手動で割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="34657-175">You can manually allocate materials to production orders or batch orders by creating additional picking list journals.</span></span> <span data-ttu-id="34657-176">また、作業や工順原価を注文に手動で割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="34657-176">You can also manually allocate labor and other route costs to the order.</span></span> <span data-ttu-id="34657-177">工程のスケジューリングを使用している場合は、工順カード仕訳帳を作成してこれらの原価を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="34657-177">If you're using operations scheduling, you can allocate these costs by creating a route card journal.</span></span> <span data-ttu-id="34657-178">ジョブのスケジューリングを使用している場合は、ジョブカード仕訳帳を作成して原価を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="34657-178">If you're using job scheduling, you can allocate the costs by creating a job card journal.</span></span> <span data-ttu-id="34657-179">製造オーダーまたはバッチ オーダーは、要求された最終数量でバッチを開始できます。</span><span class="sxs-lookup"><span data-stu-id="34657-179">Production orders or batch orders can be started in batches of the requested final quantity.</span></span> <span data-ttu-id="34657-180">製造オーダー、バッチ オーダー、またはかんばんの中で作成されたジョブは、仕訳帳、製造実行ターミナル (MES ターミナル)、またはかんばんボードを使用して個別に開始と報告ができます。</span><span class="sxs-lookup"><span data-stu-id="34657-180">Within a production order, batch order, or kanban, the jobs that are created can be started and reported separately through journals, the manufacturing execution terminal (MES Terminal), or the kanban boards.</span></span>
7.  <span data-ttu-id="34657-181">レポート進捗 / **完了**ジョブ – MES ターミナル、生産仕訳帳、かんばんボード、移動式スキャン設備を使用して、ジョブまたはリソースごとの生産の進捗状況を報告します。</span><span class="sxs-lookup"><span data-stu-id="34657-181">Report progress/**Complete** jobs – Use the MES Terminal, production journals, kanban boards, or mobile scanning capabilities to report the production progress by job or resource.</span></span> <span data-ttu-id="34657-182">材料とリソースの消費は転記され、関連するかんばん、製造オーダー、またはバッチ オーダーのステータスは**入庫済**または**完了報告済**に更新されることがあります。</span><span class="sxs-lookup"><span data-stu-id="34657-182">Material and resource consumption will be posted, and the status of the related kanbans, production orders, and batch orders might be updated to **Received** or **Reported as finished**.</span></span> <span data-ttu-id="34657-183">倉庫のプット アウェイ作業は、倉庫の構成によって作成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="34657-183">Put-away work for the warehouse might be created, depending on the warehouse configuration.</span></span>
8.  <span data-ttu-id="34657-184">**完了報告済** (製品受領書) – 製造オーダーまたはバッチ オーダーが完了済として報告されると、完了した完成品の在庫数量が更新されます。</span><span class="sxs-lookup"><span data-stu-id="34657-184">**Reported as finished** (the product receipt) – When a production order or batch order is reported as finished, the quantity of the finished goods that were completed is updated in inventory.</span></span> <span data-ttu-id="34657-185">この数量には、関連する連産品および副産物の数量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="34657-185">This quantity includes the quantity of relevant co-products and by-products.</span></span> <span data-ttu-id="34657-186">仕掛品 (WIP) 会計を使用している場合、WIP 勘定を節約し、完成品在庫を増やすため、元帳兼用仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="34657-186">If you're using work-in-process (WIP) accounting, a ledger journal is generated to reduce the WIP accounts and increase the inventory of the finished goods.</span></span> <span data-ttu-id="34657-187">製造オーダーの原価の計算時に、生産の実績原価を転記します。</span><span class="sxs-lookup"><span data-stu-id="34657-187">When the cost of a production order is calculated, the actual cost of the production is posted.</span></span> <span data-ttu-id="34657-188">生産に関連付けられた材料原価と人件費がプレフラッシュで仕訳帳に割り当てられていない場合、バックフラッシュで自動的に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="34657-188">If the material and labor costs that are associated with a production aren't already allocated in a journal or by preflushing, they can be automatically allocated through back-flushing.</span></span> <span data-ttu-id="34657-189">バックフラッシュを使用した割り当てでは、在庫トランザクションの処理後の控除が含まれます。</span><span class="sxs-lookup"><span data-stu-id="34657-189">Allocation through back-flushing involves the post-deducting of inventory transaction processes.</span></span> <span data-ttu-id="34657-190">製造オーダーが完了すると、**終了ジョブ** チェック ボックスをオンにして、残りの状態を**終了済**に変更します。</span><span class="sxs-lookup"><span data-stu-id="34657-190">If the production order is completed, select the **End job** check box to change the remaining status to **Ended**.</span></span> <span data-ttu-id="34657-191">それ以外では、生産される追加数量の報告のためにこのフィールドは空けておきます。</span><span class="sxs-lookup"><span data-stu-id="34657-191">Otherwise, leave the field empty to enable reporting of additional quantities that are produced.</span></span>
9.  <span data-ttu-id="34657-192">**品質評価** – 製品受領書は、特定の製品に対して設定されたテストのプロセスおよび品質ルールの構成によって、品質指示の作成を発生させることができます。</span><span class="sxs-lookup"><span data-stu-id="34657-192">**Quality assessment** – A product receipt can trigger the creation of quality orders, depending on the configuration of test processes and the quality rules that are established for specific products.</span></span> <span data-ttu-id="34657-193">品質指示がテストした製品の在庫状態またはバッチ属性を更新できるため、品質評価は多くの産業で必須のプロセスです。</span><span class="sxs-lookup"><span data-stu-id="34657-193">Because a quality order can update the inventory status or the batch attributes of the tested products, quality assessment is a mandatory process in many industries.</span></span>
10. <span data-ttu-id="34657-194">**プット アウェイ**および **注文による出荷** – 製品受領と品質評価の後、オプションのプット アウェイ作業では受け取った製品を誘導します。消費の次の地点、完成品の倉庫、注文による出荷の要件がある場合は出荷の領域が誘導先になります。</span><span class="sxs-lookup"><span data-stu-id="34657-194">**Put away** and **Ship to order** – After product receipt and quality assessment, optional put-away work directs the received products to the next point of consumption, to a finished goods warehouse, or to a shipment zone if there are ship-to-order requirements.</span></span>
11. <span data-ttu-id="34657-195">**終了済** – 生産を終了する前に、生産した数量に対して実績原価を計算します。</span><span class="sxs-lookup"><span data-stu-id="34657-195">**Ended** – Before production is ended, actual costs are calculated for the quantity that was produced.</span></span> <span data-ttu-id="34657-196">材料費、労務費、および間接費のすべての見積原価が取り消され、実績原価に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="34657-196">All estimated costs of material, labor, and overhead are reversed and replaced with actual costs.</span></span> <span data-ttu-id="34657-197">原価計算を実行するときに**終了済**チェック ボックスをオンにすると、製造オーダーのステータスが**終了済**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="34657-197">If you select the **End job** check box when you run the cost calculation, the production order status changes to **Ended**.</span></span> <span data-ttu-id="34657-198">これにより、完了した製造オーダーに対して原価が転記されるのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="34657-198">This status prevents any additional costs from being posted to a completed production order.</span></span>
12. <span data-ttu-id="34657-199">**期間終了** – 周期平均、バック フラッシュ原価計算、FIFO、LIFOなどいくつかの原価計算の原則は、定期的な活動によって在庫または財務期間を閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="34657-199">**Period closure** – Some cost accounting principles, such as periodic average, back-flush costing, FIFO, or LIFO, require periodic activities to close the inventory or financial period.</span></span> <span data-ttu-id="34657-200">通常、システムは、期間終了前にすべての材料消費、リソース消費、在庫と仕損の修正を報告するように試みます。</span><span class="sxs-lookup"><span data-stu-id="34657-200">Typically, the system tries to report all material and resource consumption, and also corrections of inventory and scrap, before the periods are closed.</span></span> <span data-ttu-id="34657-201">この報告は通常、在庫移動仕訳帳または調整仕訳帳を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="34657-201">This reporting is typically done by using inventory movement journals or adjustment journals.</span></span> <span data-ttu-id="34657-202">目標は、期間ごとの作業単位の経済パフォーマンスを評価することです。</span><span class="sxs-lookup"><span data-stu-id="34657-202">The goal is to assess the economic performance of operating units per period.</span></span> <span data-ttu-id="34657-203">場合によっては、複数の財務報告期間にまたがる長期の製造オーダーを使用すると、生産仕訳帳が、期間の終わりに生産の進捗状況およびリソース消費を報告するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="34657-203">In some cases, when long-running production orders are used that span the financial reporting periods, production journals are used to report the production progress and resource consumption by the end of the period.</span></span>


<a name="see-also"></a><span data-ttu-id="34657-204">参照</span><span class="sxs-lookup"><span data-stu-id="34657-204">See also</span></span>
--------

[<span data-ttu-id="34657-205">生産フィードバック</span><span class="sxs-lookup"><span data-stu-id="34657-205">Production feedback</span></span>](production-feedback.md)

[<span data-ttu-id="34657-206">製品コンフィギュレーション モデル</span><span class="sxs-lookup"><span data-stu-id="34657-206">Product configuration models</span></span>](../pim/product-configuration-models.md)

[<span data-ttu-id="34657-207">リーン生産</span><span class="sxs-lookup"><span data-stu-id="34657-207">Lean manufacturing</span></span>](lean-manufacturing-overview.md)



