---
title: 予算計画データの配賦
description: このトピックは、Microsoft Dynamics 365 Finance で利用できる配賦方法と、その使用方法ついて説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8bcfb4d3720d03ce84024766a66ccfc546767ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772079"
---
# <a name="budget-planning-data-allocation"></a><span data-ttu-id="5d194-103">予算計画データの配賦</span><span class="sxs-lookup"><span data-stu-id="5d194-103">Budget planning data allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d194-104">この記事は、Microsoft Dynamics 365 Finance で利用できる配賦方法と、その使用方法ついて説明します。</span><span class="sxs-lookup"><span data-stu-id="5d194-104">This article describes the allocation methods that are available in Microsoft Dynamics 365 Finance and how they can be used.</span></span>  

<span data-ttu-id="5d194-105">予想金額を正確に描くさまざまな方法で予算計画のデータを配分できます。</span><span class="sxs-lookup"><span data-stu-id="5d194-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="5d194-106">配賦方法</span><span class="sxs-lookup"><span data-stu-id="5d194-106">Allocation methods</span></span>
<span data-ttu-id="5d194-107">3 つの配賦方法 (複数の期間に割り当て、分析コードへの配賦、および元帳配賦ルールの使用) で、同じ予算計画明細行に基づく予算計画明細行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="5d194-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="5d194-108">3 つの他の方法 (集計、配分、および予算計画からのコピー) で、他の予算計画での予算計画明細行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="5d194-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="5d194-109">すべての 6 つの配賦方法では、ターゲット シナリオを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d194-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="5d194-110">ターゲット シナリオは、ソース シナリオと同じ場合も異なる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="5d194-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="5d194-111">また、新しい明細行を予算計画に追加するか、予算計画の現在の明細行を置き換えるか指定できます。</span><span class="sxs-lookup"><span data-stu-id="5d194-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="5d194-112">[![配賦方法を複数の期間に割り当てる](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**複数の期間に割り当て** – 期間割り当てカテゴリを使用して、ソース予算計画シナリオの予算計画明細行を、ターゲット シナリオの期間全域に配賦します。</span><span class="sxs-lookup"><span data-stu-id="5d194-112">[![Allocate across Periods allocation method](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="5d194-113">当初起票額は、期間割り当てカテゴリで定義された割合と日付に基づいて、ターゲット シナリオの複数の明細行に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="5d194-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="5d194-114">[![分析コード配賦方法への配賦](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**分析コードへの配賦** – 選択した予算配賦条件で定義された割合および財務分析コードに基づいて、ソース予算計画シナリオからターゲット シナリオの 1 つ以上の明細行に予算計画明細行を配賦します。</span><span class="sxs-lookup"><span data-stu-id="5d194-114">[![Allocate to Dimensions allocation method](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="5d194-115">![集計チャート](./media/aggregatechart-300x230.png)
**集計** – 関連付けられた (子) 予算計画のソース予算計画シナリオから、親予算計画のターゲット シナリオに予算計画明細行を集計します。</span><span class="sxs-lookup"><span data-stu-id="5d194-115">![Aggregate chart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="5d194-116">この方法で、上位レベルで統合されるように組織の下位レベルで準備した予算金額が有効になります。</span><span class="sxs-lookup"><span data-stu-id="5d194-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="5d194-117">[![配分チャート](./media/distributechart-300x230.png)](./media/distributechart.png)
**配分** – 関連付けられた計画の組織単位の財務分析コードに基づいて、親予算計画のソース予算計画シナリオから、関連付けられた (子) 予算計画のターゲット シナリオに予算計画明細行を配分します。</span><span class="sxs-lookup"><span data-stu-id="5d194-117">[![Distribute chart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="5d194-118">この方法で、さらなるローカライズ レビューのために分配されるよう組織の上位レベルで準備した予算金額が有効になります。</span><span class="sxs-lookup"><span data-stu-id="5d194-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="5d194-119">[![元帳配賦ルール](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**元帳配賦ルールの使用** – 選択された元帳配賦ルールに基づいて、ソース予算計画シナリオからターゲット シナリオに予算計画明細行を分配します。</span><span class="sxs-lookup"><span data-stu-id="5d194-119">[![Ledger allocation rules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="5d194-120">[![予算計画からのコピー](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**予算計画からのコピー** – 配分配賦の方法のように、関連する予算計画の明細行に基づいて、ターゲットに予算計画明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="5d194-120">[![Copy from budget plan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="5d194-121">ただし、この方法の場合、ソース予算計画は親である必要はありませんが、予算計画階層の上位になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5d194-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="5d194-122">この配賦方法は、結合された金額をさらに上位レベルで予算とする場合に役立ち、詳細な確認と調整を行うには組織の下位レベルに転送させると、上位レベルの承認を受けられます。</span><span class="sxs-lookup"><span data-stu-id="5d194-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="5d194-123">予算計画の配賦方法を使用</span><span class="sxs-lookup"><span data-stu-id="5d194-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="5d194-124">予算計画ページで配賦を実行するには、配賦する明細行を選択し、**予算の配賦**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d194-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="5d194-125">[![予算配賦ボタン](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="5d194-125">[![Allocate budget button](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="5d194-126">次に、配賦方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d194-126">Next, select an allocation method.</span></span> <span data-ttu-id="5d194-127">残りのフィールドが選択した方法に基づいて設定されます。</span><span class="sxs-lookup"><span data-stu-id="5d194-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="5d194-128">これらのフィールドでは、予算計画データのソースとターゲット、および目標金額が作成される際に指定した係数をソースに掛けられる、バルク調整を簡単にするためのオプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5d194-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="5d194-129">**計画への追加**オプションも設定できます。</span><span class="sxs-lookup"><span data-stu-id="5d194-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="5d194-130">**いいえ**を選択して既存の予算計画明細行を置き換えるか、**はい**を選択して既存の予算計画明細行をそのままにし、配賦済金額の新しい明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="5d194-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="5d194-131">ワークフロー中の配賦の自動化</span><span class="sxs-lookup"><span data-stu-id="5d194-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="5d194-132">1 つの強力な機能を使用して、予算計画のワークフローの一部として配賦を自動的に実行できます。</span><span class="sxs-lookup"><span data-stu-id="5d194-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="5d194-133">予算計画はそのワークフローで進行するため、指定した予算計画ステージで自動化タスクで配賦を開始できます。</span><span class="sxs-lookup"><span data-stu-id="5d194-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="5d194-134">自動配賦を設定するには、最初に**予算計画のコンフィギュレーション** ページで配賦スケジュールを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d194-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="5d194-135">配賦スケジュールでは、自動配賦を実行する際に使用される配賦方法、およびさまざまな配賦オプションの値を定義します (説明は前のセクションを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="5d194-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="5d194-136">次に、**予算計画のコンフィギュレーション** ページでステージ配賦を作成します。</span><span class="sxs-lookup"><span data-stu-id="5d194-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="5d194-137">ステージ配賦は、予算計画のワークフローおよびステージに配賦スケジュールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="5d194-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="5d194-138">最後に、目的のワークフロー ステージで予算計画ステージ配賦の自動化タスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="5d194-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="5d194-139">次の例では、2 つの予算計画ステージ配賦 (赤に示されています) がワークフローに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="5d194-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="5d194-140">[![予算計画ステージ配賦](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="5d194-140">[![Budget planning stage allocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>



