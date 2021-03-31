---
title: サービス作業の概要
description: サービス作業は、サービス注文で実行される作業を記述するために使用されます。 この情報は、技術者と顧客の両方が参照できます。
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dfeddcf754ccaf1f5fb5d3f20ca771145c5f2a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223317"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="2da6f-104">サービス作業の概要</span><span class="sxs-lookup"><span data-stu-id="2da6f-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2da6f-105">サービス作業は、サービス注文で実行される作業を記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2da6f-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="2da6f-106">この情報は、技術者と顧客の両方が参照できます。</span><span class="sxs-lookup"><span data-stu-id="2da6f-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="2da6f-107">サービス作業は、**サービス作業** ページで作成し、サービス作業関係を作成することで特定のサービス合意またはサービス注文に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="2da6f-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="2da6f-108">サービス タスク リレーションをするたびに、以下を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="2da6f-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="2da6f-109">作業に関する社内ノート。技術者にとって重要な、作業に関する詳細な技術的要求事項などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2da6f-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="2da6f-110">顧客が参照できる社外ノート。</span><span class="sxs-lookup"><span data-stu-id="2da6f-110">External notes that the customer can see.</span></span> <span data-ttu-id="2da6f-111">顧客とサービス会社の契約に従って遂行されるタスクに関する、あまり専門的でない説明などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2da6f-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="2da6f-112">サービス タスクとサービス注文またはサービス契約の間にサービス タスク リレーションを設定すると、現在のサービス注文またはサービス契約にサービス注文明細行またはサービス契約行を作成するときに、このサービス タスクを指定できるようになります。</span><span class="sxs-lookup"><span data-stu-id="2da6f-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="2da6f-113">サービス契約からサービス注文を生成するときに、各サービス契約行に割り当てられたサービスタスクを使用して、サービス注文明細行をサービス注文へとグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="2da6f-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="2da6f-114">サービス作業の作成</span><span class="sxs-lookup"><span data-stu-id="2da6f-114">Create a service task</span></span>

1. <span data-ttu-id="2da6f-115">**サービス管理** \> **設定** \> **サービス作業** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2da6f-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="2da6f-116">新しい行を作成します。</span><span class="sxs-lookup"><span data-stu-id="2da6f-116">Create a new line.</span></span>
3. <span data-ttu-id="2da6f-117">サービス ID と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2da6f-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="2da6f-118">例</span><span class="sxs-lookup"><span data-stu-id="2da6f-118">Example</span></span>

<span data-ttu-id="2da6f-119">ある技術者が、顧客のサイトでギアボックス (サービス対象 GB-1234) に対して 2 つのジョブを遂行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2da6f-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="2da6f-120">顧客に対してサービス契約が作成され、2 つのジョブに複数のトランザクションが関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="2da6f-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="2da6f-121">このサービス契約および 2 つのジョブのサービス契約を次に示します。</span><span class="sxs-lookup"><span data-stu-id="2da6f-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="2da6f-122">サービス契約</span><span class="sxs-lookup"><span data-stu-id="2da6f-122">Service agreement</span></span>

| <span data-ttu-id="2da6f-123">Project</span><span class="sxs-lookup"><span data-stu-id="2da6f-123">Project</span></span> | <span data-ttu-id="2da6f-124">サービス契約</span><span class="sxs-lookup"><span data-stu-id="2da6f-124">Service agreement</span></span> | <span data-ttu-id="2da6f-125">説明</span><span class="sxs-lookup"><span data-stu-id="2da6f-125">Description</span></span>                                  | <span data-ttu-id="2da6f-126">グループ化</span><span class="sxs-lookup"><span data-stu-id="2da6f-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="2da6f-127">9012</span><span class="sxs-lookup"><span data-stu-id="2da6f-127">9012</span></span>    | <span data-ttu-id="2da6f-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="2da6f-128">000008\_001</span></span>       | <span data-ttu-id="2da6f-129">点検と定期交換 - GB-1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="2da6f-130">割増給与</span><span class="sxs-lookup"><span data-stu-id="2da6f-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="2da6f-131">サービス契約項目</span><span class="sxs-lookup"><span data-stu-id="2da6f-131">Service agreement lines</span></span>

| <span data-ttu-id="2da6f-132">説明</span><span class="sxs-lookup"><span data-stu-id="2da6f-132">Description</span></span>             | <span data-ttu-id="2da6f-133">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="2da6f-133">Transaction type</span></span> | <span data-ttu-id="2da6f-134">サービス対象</span><span class="sxs-lookup"><span data-stu-id="2da6f-134">Service object</span></span> | <span data-ttu-id="2da6f-135">サービス作業</span><span class="sxs-lookup"><span data-stu-id="2da6f-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="2da6f-136">点検とクリーニング</span><span class="sxs-lookup"><span data-stu-id="2da6f-136">Inspection and cleaning</span></span> | <span data-ttu-id="2da6f-137">時</span><span class="sxs-lookup"><span data-stu-id="2da6f-137">Hour</span></span>             | <span data-ttu-id="2da6f-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-138">GB-1234</span></span>        | <span data-ttu-id="2da6f-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-139">I/C - GB1234</span></span> |
| <span data-ttu-id="2da6f-140">旅行</span><span class="sxs-lookup"><span data-stu-id="2da6f-140">Travel</span></span>                  | <span data-ttu-id="2da6f-141">Expense</span><span class="sxs-lookup"><span data-stu-id="2da6f-141">Expense</span></span>          | <span data-ttu-id="2da6f-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-142">GB-1234</span></span>        | <span data-ttu-id="2da6f-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-143">I/C - GB1234</span></span> |
| <span data-ttu-id="2da6f-144">材料</span><span class="sxs-lookup"><span data-stu-id="2da6f-144">Materials</span></span>               | <span data-ttu-id="2da6f-145">項目</span><span class="sxs-lookup"><span data-stu-id="2da6f-145">Item</span></span>             | <span data-ttu-id="2da6f-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-146">GB-1234</span></span>        | <span data-ttu-id="2da6f-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-147">I/C - GB1234</span></span> |
| <span data-ttu-id="2da6f-148">定期交換</span><span class="sxs-lookup"><span data-stu-id="2da6f-148">Routine replacement</span></span>     | <span data-ttu-id="2da6f-149">時</span><span class="sxs-lookup"><span data-stu-id="2da6f-149">Hour</span></span>             | <span data-ttu-id="2da6f-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-150">GB-1234</span></span>        | <span data-ttu-id="2da6f-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-151">RR - GB1234</span></span>  |
| <span data-ttu-id="2da6f-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="2da6f-152">GR-1</span></span>                    | <span data-ttu-id="2da6f-153">項目</span><span class="sxs-lookup"><span data-stu-id="2da6f-153">Item</span></span>             | <span data-ttu-id="2da6f-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-154">GB-1234</span></span>        | <span data-ttu-id="2da6f-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-155">RR - GB1234</span></span>  |
| <span data-ttu-id="2da6f-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="2da6f-156">GR-5</span></span>                    | <span data-ttu-id="2da6f-157">項目</span><span class="sxs-lookup"><span data-stu-id="2da6f-157">Item</span></span>             | <span data-ttu-id="2da6f-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-158">GB-1234</span></span>        | <span data-ttu-id="2da6f-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-159">RR - GB1234</span></span>  |

<span data-ttu-id="2da6f-160">2 つのジョブのサービス合意項目には、2 つのサービス作業が関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="2da6f-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="2da6f-161">このサービス作業によって、各ジョブに属するトランザクションが決まります。</span><span class="sxs-lookup"><span data-stu-id="2da6f-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="2da6f-162">最初のケースでは、対象 GB-1234 の点検とクリーニングに関係するすべてのサービス契約項目が、サービス タスク I/C - GB1234 で識別されます。</span><span class="sxs-lookup"><span data-stu-id="2da6f-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="2da6f-163">2 番目のケースでは、定期交換ジョブの遂行に関係するすべてのサービス契約が、サービス契約 RR - GB1234 で識別されます。</span><span class="sxs-lookup"><span data-stu-id="2da6f-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="2da6f-164">サービス作業を特定の契約に関連付けるサービス作業関係は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2da6f-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="2da6f-165">サービス作業</span><span class="sxs-lookup"><span data-stu-id="2da6f-165">Service tasks</span></span>

| <span data-ttu-id="2da6f-166">サービス作業</span><span class="sxs-lookup"><span data-stu-id="2da6f-166">Service task</span></span> | <span data-ttu-id="2da6f-167">説明</span><span class="sxs-lookup"><span data-stu-id="2da6f-167">Description</span></span>                             | <span data-ttu-id="2da6f-168">社内ノート</span><span class="sxs-lookup"><span data-stu-id="2da6f-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="2da6f-169">社外ノート</span><span class="sxs-lookup"><span data-stu-id="2da6f-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="2da6f-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-170">I/C - GB1234</span></span> | <span data-ttu-id="2da6f-171">ギアボックス GB-1234 の点検</span><span class="sxs-lookup"><span data-stu-id="2da6f-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="2da6f-172">ギアボックス GB-1234 の目視および機械による点検とクリーニング</span><span class="sxs-lookup"><span data-stu-id="2da6f-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="2da6f-173">ギアボックスの定期点検</span><span class="sxs-lookup"><span data-stu-id="2da6f-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="2da6f-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="2da6f-174">RR - GB1234</span></span>  | <span data-ttu-id="2da6f-175">GB-1234 の部品の定期交換</span><span class="sxs-lookup"><span data-stu-id="2da6f-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="2da6f-176">GR-1 および GR-5 部品の定期サービス交換 (2002 年より前に製造されたギアボックスについては GR-2 部品も交換)</span><span class="sxs-lookup"><span data-stu-id="2da6f-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="2da6f-177">定期部品交換</span><span class="sxs-lookup"><span data-stu-id="2da6f-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="2da6f-178">サービス注文のグループ化</span><span class="sxs-lookup"><span data-stu-id="2da6f-178">Group service orders</span></span>

<span data-ttu-id="2da6f-179">サービス注文を自動的に作成するときに、サービス タスクをグループ化の基準として使用できます。</span><span class="sxs-lookup"><span data-stu-id="2da6f-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="2da6f-180">サービス注文をサービス タスクでグループ化するには、サービス契約の定義で、そのサービス契約に基づくサービス注文をグループ化する際の最初のグループ化基準としてサービス タスク ID を使用するように指定します。</span><span class="sxs-lookup"><span data-stu-id="2da6f-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="2da6f-181">**サービス作業によるグループ化**</span><span class="sxs-lookup"><span data-stu-id="2da6f-181">**Group by service task**</span></span>

1. <span data-ttu-id="2da6f-182">**サービス管理** \> **共通** \> **サービス契約** \> **サービス契約** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="2da6f-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="2da6f-183">**設定** タブの、**サービス注文の組み合わせ** フィールドで **サービス作業別** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2da6f-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]