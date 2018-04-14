---
title: "予算作成の概要"
description: "Microsoft Dynamics 365 for Finance and Operations の財務機能を使用するほとんどすべての会社は、実績対予算のレポートを作成できなければなりません。 この記事では、Finance and Operations 予算で作成したり、サード パーティ製プログラムから読み込むために必要な最低限のコンフィギュレーションを説明します。"
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ddfc7093ae2fb246f66486787e225f5b4c34ba1b
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="budgeting-overview"></a><span data-ttu-id="12e83-104">予算作成の概要</span><span class="sxs-lookup"><span data-stu-id="12e83-104">Budgeting overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="12e83-105">Microsoft Dynamics 365 for Finance and Operations の財務機能を使用するほとんどすべての会社は、実績対予算のレポートを作成できなければなりません。</span><span class="sxs-lookup"><span data-stu-id="12e83-105">Almost every company that uses Financials functionality in Microsoft Dynamics 365 for Finance and Operations will have to be able to create reports of budget vs. actuals.</span></span> <span data-ttu-id="12e83-106">この記事では、Finance and Operations 予算で作成したり、サード パーティ製プログラムから読み込むために必要な最低限のコンフィギュレーションを説明します。</span><span class="sxs-lookup"><span data-stu-id="12e83-106">This article explains the minimum configuration that is required in order to create budgets in Finance and Operations or load them from a third-party program.</span></span>

<a name="overview"></a><span data-ttu-id="12e83-107">概要</span><span class="sxs-lookup"><span data-stu-id="12e83-107">Overview</span></span>
--------

<span data-ttu-id="12e83-108">法人の承認済の予算は、*予算登録エントリ*として知られるドキュメントで管理されます。</span><span class="sxs-lookup"><span data-stu-id="12e83-108">The approved budget for a legal entity is maintained in a document that is known as a *budget register entry*.</span></span> <span data-ttu-id="12e83-109">予算登録エントリのドキュメント明細行は、*予算勘定*エントリとして知られ、承認済の予算の財務分析コード情報、日付、および金額が含まれます。</span><span class="sxs-lookup"><span data-stu-id="12e83-109">The lines in a budget register entry document are known as *budget account* entries, and contain financial dimension information, dates, and the amounts of the approved budget.</span></span> <span data-ttu-id="12e83-110">予算登録エントリのドキュメントは、予算金額の元帳の実際の金額を比較した基本的な財務レポートや照会のページに統合されます。</span><span class="sxs-lookup"><span data-stu-id="12e83-110">The budget register entry document is integrated with basic financial reports and inquiry pages where ledger actual amounts are compared to budget amounts.</span></span> 

<span data-ttu-id="12e83-111">Finance and Operations の予算登録エントリを作成するための方法は複数あります。</span><span class="sxs-lookup"><span data-stu-id="12e83-111">There are multiple methods for creating budget register entries in Finance and Operations:</span></span>

-   <span data-ttu-id="12e83-112">**予算登録エントリ**ページで、ドキュメント情報を手動で入力します。</span><span class="sxs-lookup"><span data-stu-id="12e83-112">Manually enter the document information on the **Budget register entries** page.</span></span>
-   <span data-ttu-id="12e83-113">**予算登録エントリ**ページの、**Excel で開く**ボタンをクリックして開くことができる Microsoft Excel テンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="12e83-113">Use the Microsoft Excel template that you can open by clicking the **Open in Excel** button on the **Budget register entries** page.</span></span>
-   <span data-ttu-id="12e83-114">予算登録エントリをインポートする場合、データ管理の**予算勘定項目**データ エンティティを使用します。</span><span class="sxs-lookup"><span data-stu-id="12e83-114">Use the **Budget Account Entries** data entity in Data management to import budget register entries.</span></span> <span data-ttu-id="12e83-115">システムに多くの予算勘定項目をインポートする必要がある場合、この方法を使用し、**セット ベース****処理**パラメーターを有効にすることを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e83-115">You should consider using this method and turning on the **Set based** **processing **parameter when you must import many budget account entries into the system.</span></span>
-   <span data-ttu-id="12e83-116">会社が予算データの準備に予算計画機能を使用する場合、**予算登録エントリの生成**定期処理を使用できます。</span><span class="sxs-lookup"><span data-stu-id="12e83-116">If the company uses Budget planning functionality to prepare budget data, you can use the **Generate budget register entry** periodic process.</span></span>

<span data-ttu-id="12e83-117">予算登録エントリは、予算残高が更新されると完了と見なされます。</span><span class="sxs-lookup"><span data-stu-id="12e83-117">The budget register entry is considered completed when the budget balances have been updated.</span></span> <span data-ttu-id="12e83-118">**予算登録エントリ**ページで、選択された予算登録エントリ、あるいは複数のエントリの [予算残高の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12e83-118">On the **Budget register entries** page, click **Update budget balances** for a selected budget register entry or multiple entries.</span></span> <span data-ttu-id="12e83-119">予算残高を更新した後、予算登録エントリの状態を**完了**に変更します。</span><span class="sxs-lookup"><span data-stu-id="12e83-119">After you update the budget balances, the status of the budget register entry changes to **Completed**.</span></span> <span data-ttu-id="12e83-120">完了した予算登録エントリは、編集用に再度開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="12e83-120">Completed budget register entry can't be re-opened for edits.</span></span> <span data-ttu-id="12e83-121">したがって、予算データを調整する必要がある場合、完了した予算登録エントリのデータを修正する代わりに、新しい予算登録エントリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e83-121">Therefore, if the budget data must be adjusted, you must create a new budget register entry instead of correcting data in the completed budget register entry.</span></span>

## <a name="configuration"></a><span data-ttu-id="12e83-122">構成</span><span class="sxs-lookup"><span data-stu-id="12e83-122">Configuration</span></span>
<span data-ttu-id="12e83-123">予算をコンフィギュレーションする場合、**予算作成パラメーター**ページで開始します。</span><span class="sxs-lookup"><span data-stu-id="12e83-123">When you configure budgeting, start on the **Budgeting parameters** page.</span></span> <span data-ttu-id="12e83-124">このページで、ワークスペースでの、予算登録エントリの予算仕訳帳、番号順序、および既定の動作を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e83-124">On this page, you must define the budget journal, the number sequence for budget register entries, and the default behavior in the workspaces.</span></span>

<span data-ttu-id="12e83-125">次に、予算タイプ (たとえば、転送あるいはリビジョン) に基づいて予算登録エントリの承認を制御するポリシーがある場合、**予算作成ワークフロー**ページで予算登録エントリのワークフローを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e83-125">Next, if there are policies that govern the approval of budget register entries, based on budget type (for example, transfers or revisions), you must create budget register entry workflows on the **Budgeting workflows** page.</span></span> <span data-ttu-id="12e83-126">転送がワークフロー承認なしで許可されるシナリオがある場合、これらのシナリオをサポートする予算振替ルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="12e83-126">If there are scenarios where transfers might be allowed without workflow approval, you can define budget transfer rules to support those scenarios.</span></span> 

<span data-ttu-id="12e83-127">**予算作成用の分析コード**ページで、勘定科目表に使用される分析コードに基づいて、割り当てに使用する財務分析コードを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e83-127">On the **Budgeting dimensions** page, you must select the financial dimensions that are used for budgeting, based on the dimensions that are used in the chart of accounts.</span></span> <span data-ttu-id="12e83-128">予算作成用にすべての財務分析コードまたはサブセットを選択できます。</span><span class="sxs-lookup"><span data-stu-id="12e83-128">You can select all financial dimensions or a subset of them for budgeting.</span></span>

<span data-ttu-id="12e83-129">予算すべて、または一部に対応する*予算モデル*を定義します。</span><span class="sxs-lookup"><span data-stu-id="12e83-129">Define a *budget model *that corresponds to all or some of the budgets.</span></span> <span data-ttu-id="12e83-130">すべての予算登録エントリに対して 1 つの予算モデルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="12e83-130">You can use a single budget model for all budget register entries.</span></span> <span data-ttu-id="12e83-131">また、予算分類できる予算タイプ、地理的な場所、または他の方法に基づく他のモデルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="12e83-131">Alternatively, you can create separate models that are based on the budget type, the geographical location, or some other way that a budget can be classified.</span></span> 

> [!NOTE] 
> <span data-ttu-id="12e83-132">予算管理を使用すると、特定の予算サイクル期間ごとに 1 つの予算モデルに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="12e83-132">If budget control is used, you can associate only one budget model with a specific budget cycle time span.</span></span> 

<span data-ttu-id="12e83-133">レコード、および関連するワークフローの予算トランザクションタイプを識別する*予算コード*を作成します。</span><span class="sxs-lookup"><span data-stu-id="12e83-133">Create *budget codes* that identify the type of budget transactions to record and any related workflow.</span></span> <span data-ttu-id="12e83-134">予算コードは次の予算タイプをサポートできます:</span><span class="sxs-lookup"><span data-stu-id="12e83-134">Budget codes can support the following budget types:</span></span>

-   <span data-ttu-id="12e83-135">元の予算</span><span class="sxs-lookup"><span data-stu-id="12e83-135">Original budget</span></span>
-   <span data-ttu-id="12e83-136">移動</span><span class="sxs-lookup"><span data-stu-id="12e83-136">Transfer</span></span>
-   <span data-ttu-id="12e83-137">リビジョン</span><span class="sxs-lookup"><span data-stu-id="12e83-137">Revision</span></span>
-   <span data-ttu-id="12e83-138">債務</span><span class="sxs-lookup"><span data-stu-id="12e83-138">Encumbrance</span></span>
-   <span data-ttu-id="12e83-139">事前債務</span><span class="sxs-lookup"><span data-stu-id="12e83-139">Pre-encumbrance</span></span>
-   <span data-ttu-id="12e83-140">繰越予算</span><span class="sxs-lookup"><span data-stu-id="12e83-140">Carry-forward budget</span></span>

<span data-ttu-id="12e83-141">予算コードにより、予算サイクルの過程全体で、承認済の予算の変更の監査証跡が可能になります。</span><span class="sxs-lookup"><span data-stu-id="12e83-141">Budget codes let you have an audit trail of approved budget modifications throughout the course of the budget cycle.</span></span> <span data-ttu-id="12e83-142">ワークフローが予算コードと関連付けられる場合、その予算コードを使用するすべての予算登録エントリに対して有効になるワークフローとワークフロー ステップは、予算登録エントリが**完了**ステージに達する前に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e83-142">If a workflow is associated with a budget code, the workflow will be enabled for all budget register entries that use that budget code, and workflow steps must be completed before the budget register entry can reach the **Completed** stage.</span></span>  

<span data-ttu-id="12e83-143">また、必要に応じて*予算振替ルール*を設定します。</span><span class="sxs-lookup"><span data-stu-id="12e83-143">You can also optionally set up *budget transfer rules*.</span></span> <span data-ttu-id="12e83-144">予算振替ルールを使用するには、**予算パラメーター** ページで [予算振替のルールを使用] を選択します。</span><span class="sxs-lookup"><span data-stu-id="12e83-144">To use budget transfer rules, select **Use rules for budget transfers** on the **Budget parameters** page.</span></span> <span data-ttu-id="12e83-145">予算振替ルールが使用される場合、ユーザーが**転送**タイプの予算コードを使用してドキュメントを作成すると、予算振替ルールに違反している場合に予算残高は更新されません。</span><span class="sxs-lookup"><span data-stu-id="12e83-145">When budget transfer rules are used, if a user creates a document by using a budget code of the **Transfer** type, budget balances won't be updated if the budget transfer rules are violated.</span></span> <span data-ttu-id="12e83-146">たとえば、販売の主勘定とマーケティング部門の間で転送される経費予算の予算振替ドキュメントを許可することができますが、そのタイプの予算勘定項目のワークフロー承認が付与されていない部門からの、あるいは部門への転送を禁止することもできます。</span><span class="sxs-lookup"><span data-stu-id="12e83-146">For example, you can allow budget transfer documents where the expense budget is transferred between the main accounts for the Sales and Marketing department, but can prohibit budget from being transferred from or to that department unless workflow approval has been granted for that type of budget account entry.</span></span>

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a><span data-ttu-id="12e83-147">実績対予算を追跡するワークスペースおよび照会ページの使用</span><span class="sxs-lookup"><span data-stu-id="12e83-147">Using workspaces and inquiry pages to track budget vs. actuals</span></span>
<span data-ttu-id="12e83-148">予算マネージャで、**元帳予算および予測**ワークスペースの予算の現在の状態を確認できます。</span><span class="sxs-lookup"><span data-stu-id="12e83-148">The budget manager can review the current state of a budget in the **Ledger budgets and forecasts** workspace.</span></span> <span data-ttu-id="12e83-149">**予算超過の経費**および**予算以内の収益**タブは、目標予算が実現されていない、あるいは、しきい値に近づいていない財務分析コードの組み合わせをすばやく表示します。</span><span class="sxs-lookup"><span data-stu-id="12e83-149">The **Expense over budget** and **Revenue under budget** tabs provide a quick view of the financial dimension combinations where budget targets aren't being met or are approaching the threshold.</span></span> <span data-ttu-id="12e83-150">**自分のワークスペースのコンフィギュレーション**をクリックして、これらのタブで使用される財務分析コード セットと予算しきい値の割合をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="12e83-150">You can personalize the budget threshold percentage and financial dimension sets that are used on those tabs by clicking **Configure my workspace**.</span></span> <span data-ttu-id="12e83-151">**単位マネージャ**をクリックして、これらのタブで選択した特定の財務分析コードの組み合わせを担当する作業者を表示できます。</span><span class="sxs-lookup"><span data-stu-id="12e83-151">You can click **Unit managers** to see the workers who are responsible for specific financial dimension combinations that are selected on those tabs.</span></span> <span data-ttu-id="12e83-152">たとえば、業務部門の経費の予算がしきい値を超過していることが表示される場合、この点について話し合うため、業務部門のマネージャーを簡単に検索し、連絡できます。</span><span class="sxs-lookup"><span data-stu-id="12e83-152">For example, if you see that the expense budget of the Operations department is going over the budget threshold, you can easily find and contact the Operations department manager to discuss the issue.</span></span> 

> [!NOTE] 
> <span data-ttu-id="12e83-153">**組織単位**ページの、[部門マネージャー] フィールドで、どのマネージャーが特定の財務分析コードの組み合わせをサポートするかが決まります。</span><span class="sxs-lookup"><span data-stu-id="12e83-153">The **Department manager** field on the **Organization Units** page determines which managers support specific financial dimension combinations.</span></span> <span data-ttu-id="12e83-154">タブの下部にある**詳細情報**をクリックすると、予算金額と実績金額の詳細についての**実績対予算**照会ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="12e83-154">Click **See more** at the bottom of the tab to open the **Budget vs actuals** inquiry page for more details about budget amounts versus actual amounts.</span></span> 

<span data-ttu-id="12e83-155">**実績対予算**照会ページは、予算と実績金額の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="12e83-155">The **Actual vs budget** inquiry page lets you drill into the details of the budget versus actual amounts.</span></span> <span data-ttu-id="12e83-156">照会ページの明細行を選択し、**期間残高**をクリックすると、予算と実績金額の会計年度期間の分布を表示します。</span><span class="sxs-lookup"><span data-stu-id="12e83-156">Select a line on the inquiry page, and then click **Period balances** to see budget and actual amounts spread across fiscal periods.</span></span> <span data-ttu-id="12e83-157">**予算勘定項目**ページで予算登録エントリの予算金額の詳細のドリルスルーが提供されます。</span><span class="sxs-lookup"><span data-stu-id="12e83-157">The **Budget account entries** page provides drill-through to the details of the budget amount in budget register entries.</span></span> <span data-ttu-id="12e83-158">**一般仕訳入力**ページで、計算された**実績**金額を含む元帳トランザクションが開かれます。</span><span class="sxs-lookup"><span data-stu-id="12e83-158">The **General journal entries** page opens the ledger transactions that are included in the calculated **Actuals** amount.</span></span> 

<span data-ttu-id="12e83-159">予算計画機能を使用している会社は、**元帳予算および予測**ワークスペースで、*予算予測*を作成、および使用できます。</span><span class="sxs-lookup"><span data-stu-id="12e83-159">A company that is using Budget planning functionality can create and use *budget forecasts* in the **Ledger budgets and forecasts** workspace.</span></span>




