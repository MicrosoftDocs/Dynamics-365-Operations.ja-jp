---
title: 予算作成用のホーム ページ
description: このトピックでは、Microsoft Dynamics 365 Finance の予算作成機能コンポーネント、予算作成ツール、およびレポート機能の概要を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/09/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a910aa7f54905f305ed69e9dd9eea0909e5558d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528548"
---
# <a name="budgeting-home-page"></a><span data-ttu-id="b247a-103">予算作成用のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="b247a-103">Budgeting home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b247a-104">このトピックでは、予算作成機能コンポーネント、予算作成ツール、およびレポート機能の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="b247a-104">This topic provides an overview of the budgeting functionality components, budgeting tools, and reporting capabilities.</span></span> 

<a name="components-of-budgeting-functionality"></a><span data-ttu-id="b247a-105">予算作成機能のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="b247a-105">Components of budgeting functionality</span></span>
-------------------------------------

<span data-ttu-id="b247a-106">通常、会社のリソース予定サイクルは、計画、予算作成、予測活動で構成されます。</span><span class="sxs-lookup"><span data-stu-id="b247a-106">The resource planning cycle for a company typically consists of planning, budgeting, and forecasting activities.</span></span>

<span data-ttu-id="b247a-107">[![予算作成機能コンポーネント](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)</span><span class="sxs-lookup"><span data-stu-id="b247a-107">[![Budgeting functionality components](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)</span></span>

<span data-ttu-id="b247a-108">長期戦略的計画と年間予算計画の両方のプロセスは、予算計画ドキュメント経由でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b247a-108">The processes for both long-term strategic planning and annual budget planning are supported through a budget plan document.</span></span> <span data-ttu-id="b247a-109">予算計画ドキュメントは、Microsoft Excel と密に統合されています。</span><span class="sxs-lookup"><span data-stu-id="b247a-109">Budget plan documents are tightly integrated with Microsoft Excel.</span></span> <span data-ttu-id="b247a-110">ユーザーは、無制限な金額と定量的なシナリオを構成することができ、予算作成の組織階層も定義してトップダウンとボトムアップの両方の予算作成方法をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="b247a-110">Users can configure unlimited monetary and quantitative scenarios, and can also define a budgeting organizational hierarchy to both support top-down and bottom-up budgeting methods.</span></span> <span data-ttu-id="b247a-111">予算をアプリケーションで設定し、承認した後、予算計画を予算登録エントリに変換します。</span><span class="sxs-lookup"><span data-stu-id="b247a-111">After a budget is established and approved in the application, you convert the budget plan to a budget register entry.</span></span> <span data-ttu-id="b247a-112">予算登録エントリは、予算を管理し、予算コード経由で追跡できる金額を維持するためのツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="b247a-112">Budget register entries provide tools for maintaining the budget and for keeping amounts traceable through budget codes.</span></span> <span data-ttu-id="b247a-113">予算登録エントリでは、元の予算の変更、転送の実行、予算金額の前年度からの繰り越しができます。</span><span class="sxs-lookup"><span data-stu-id="b247a-113">Budget register entries let you revise original budgets, perform transfers, and carry forward budget amounts from the previous year.</span></span> <span data-ttu-id="b247a-114">決定した予算に基づいて、会社は予算管理を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b247a-114">Based on the established budget, a company can enable budget control.</span></span> <span data-ttu-id="b247a-115">管理レベルは、組織の文化と組織の成熟度レベルに依存します。</span><span class="sxs-lookup"><span data-stu-id="b247a-115">The level of control depends on the organizational culture and the organization's level of maturity.</span></span> <span data-ttu-id="b247a-116">成熟度レベルの低い組織は、予算が目標を満たしていない場合、予算を "現状のまま" とし、プロアクティブよりリアクティブです。</span><span class="sxs-lookup"><span data-stu-id="b247a-116">Organizations that have low maturity might leave the budget “as is” and might be more reactive than proactive if a budget doesn't meet expectations.</span></span> <span data-ttu-id="b247a-117">組織によっては、予算財源が使用できない場合に、ユーザーが購入することを妨げる予算管理ポリシーを有効にすることもあります。</span><span class="sxs-lookup"><span data-stu-id="b247a-117">Other organizations might enable budget control policies that prevent users from purchasing if budget funds aren't available.</span></span>

<span data-ttu-id="b247a-118">最後に、非常に成熟した組織は、従業員が組織の目標について教育されている組織文化を確立し、「出張の代わりにオンライン ミーティングを検討する」ようなポリシーを通じてこれらの目標に従う可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b247a-118">Finally, very mature organizations might establish an organizational culture where employees are educated about organizational targets and follow those targets through policies such as “Consider online meeting instead of a travel.”</span></span> <span data-ttu-id="b247a-119">アプリケーションには、会社の管理がハード コントロール (予算を超過する転記ができません) またはソフト コントロール (ユーザーが利用可能な予算資源を超えると警告されますが、続行方法を決めることができます) のいずれかを選択できる予算管理フレームワークが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b247a-119">The application includes a budget control framework that lets the company's management select either hard control (which prevents postings that would go over the budget) or soft control (where users are warned that they will exceed the available budget funds but can decide for themselves how to proceed).</span></span> <span data-ttu-id="b247a-120">最後に、ローリング予測を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b247a-120">Finally, you can use rolling forecasts.</span></span> <span data-ttu-id="b247a-121">ローリング予測は、予算対実績の定期的な比較であり、会社が予算との比較においてどの程度効果的に運営されているかを定義するために使用します。</span><span class="sxs-lookup"><span data-stu-id="b247a-121">A rolling forecast is a regular comparison of budget to actuals and is used to define how well the company operates against the budget.</span></span> <span data-ttu-id="b247a-122">ローリング予測はトレンドの特定にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="b247a-122">A rolling forecast is also used to identify trends.</span></span> <span data-ttu-id="b247a-123">Finance and Operations では、ローリング予測は、最初の計画活動として予算計画ドキュメント経由でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b247a-123">In Finance and Operations, rolling forecasts are supported, through a budget plan document, as initial planning activities.</span></span> <span data-ttu-id="b247a-124">ローリング予測は、次回の予算サイクルの計画と並列して実行できます。</span><span class="sxs-lookup"><span data-stu-id="b247a-124">Rolling forecasts can be done in parallel with the planning for the upcoming budget cycle.</span></span>

-   [<span data-ttu-id="b247a-125">予算作成の概要</span><span class="sxs-lookup"><span data-stu-id="b247a-125">Budgeting overview</span></span>](basic-budgeting-overview-configuration.md)
-   [<span data-ttu-id="b247a-126">予算管理の概要</span><span class="sxs-lookup"><span data-stu-id="b247a-126">Budget control overview</span></span>](budget-control-overview-configuration.md)
-   [<span data-ttu-id="b247a-127">予算計画の概要</span><span class="sxs-lookup"><span data-stu-id="b247a-127">Budget planning overview</span></span>](budget-planning-overview-configuration.md)
-   [<span data-ttu-id="b247a-128">職位予測</span><span class="sxs-lookup"><span data-stu-id="b247a-128">Position forecasting</span></span>](position-forecasting.md)
-   [<span data-ttu-id="b247a-129">予算計画妥当性ドキュメント</span><span class="sxs-lookup"><span data-stu-id="b247a-129">Budget planning justification documents</span></span>](budget-planning-justification-docs.md)
-   [<span data-ttu-id="b247a-130">Excel の予算計画テンプレート</span><span class="sxs-lookup"><span data-stu-id="b247a-130">Budget planning templates for Excel</span></span>](budget-planning-excel-templates.md)

## <a name="budgeting-tools"></a><span data-ttu-id="b247a-131">予算作成ツール</span><span class="sxs-lookup"><span data-stu-id="b247a-131">Budgeting tools</span></span>
<span data-ttu-id="b247a-132">[![予算作成ツール](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg)</span><span class="sxs-lookup"><span data-stu-id="b247a-132">[![Budgeting tools](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg)</span></span> 

<span data-ttu-id="b247a-133">追加の計画機能および予算作成機能は使用可能で、元帳予算に統合されます。</span><span class="sxs-lookup"><span data-stu-id="b247a-133">Additional planning and budgeting capabilities are available and are integrated with ledger budgets.</span></span>

-   <span data-ttu-id="b247a-134">**要員予算** – 従業員の予算作成は、職位、報酬グループなどの詳細な予算原価コンポーネント計画を含みます。</span><span class="sxs-lookup"><span data-stu-id="b247a-134">**Workforce budgets** – Workforce budgeting includes detailed budget cost component planning for positions, compensation groups, and so on.</span></span>
-   <span data-ttu-id="b247a-135">**固定資産予算** – 固定資産情報に基づいて、計画済み減価償却を計算し、固定資産に関連する他の計画済みトランザクションを記録できます。</span><span class="sxs-lookup"><span data-stu-id="b247a-135">**Fixed assets budgets** – Based on fixed asset information, you can calculate planned depreciation and record other planned transactions that are related to fixed assets.</span></span>
-   <span data-ttu-id="b247a-136">**プロジェクト予算** プロジェクト モジュールで、詳細なプロジェクト予測を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b247a-136">**Project budgets** – In the projects module, you can create detailed project forecasts.</span></span> <span data-ttu-id="b247a-137">プロジェクトの予測には、予定時間、経費、および品目に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b247a-137">The projects forecasts will include details about the planned hours, expenses, fees, and items.</span></span>
-   <span data-ttu-id="b247a-138">**需要予測** – トランザクション履歴データに基づき、将来の在庫需要の見積、需要予測の作成ができます。</span><span class="sxs-lookup"><span data-stu-id="b247a-138">**Demand forecasting** – Based on historical transaction data, you can estimate future inventory demand and create demand forecasts.</span></span>

<span data-ttu-id="b247a-139">予算計画に他のモジュールから計画データを移動する方法についての情報は、[他のモジュールとの予算計画の統合](budget-planning-integration-other-modules.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b247a-139">For information about how to bring planning data from other modules into budget plans, see [Budget planning integration with other modules](budget-planning-integration-other-modules.md).</span></span>

## <a name="user-interface-and-reporting-capabilities"></a><span data-ttu-id="b247a-140">ユーザー インターフェイスとレポート機能</span><span class="sxs-lookup"><span data-stu-id="b247a-140">User interface and reporting capabilities</span></span>
<span data-ttu-id="b247a-141">ユーザーは直接クライアントで (コンフィギュレーション可能な予算計画ドキュメント ページを使用することにより)、または Excel を使用して、予算計画を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b247a-141">Users can create budget plans either directly in the client (by using a configurable budget plan document page) or through Excel.</span></span> <span data-ttu-id="b247a-142">Excel は、いくつかの追加機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="b247a-142">Excel provides several additional capabilities.</span></span> <span data-ttu-id="b247a-143">たとえば、予算計画のソースとして外部データを使用し、カスタム計算を実行し、Microsoft PivotTable やグラフを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b247a-143">For example, you can use external data as a source for a budget plan, do custom calculations, and use Microsoft PivotTable and charts.</span></span> <span data-ttu-id="b247a-144">予算計画プロセスの変数のほとんどは、コンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="b247a-144">Most of the variables in the budget planning process can be configured.</span></span> 

<span data-ttu-id="b247a-145">たとえば、予算作成者、予算作成する対象、プロセスの概要を定義できます。</span><span class="sxs-lookup"><span data-stu-id="b247a-145">For example, you can define who does budgeting, what is budgeted, and what the process looks like.</span></span> <span data-ttu-id="b247a-146">予算計画には Excel を使用できますが、アプリケーションでは、まったくの単一のソースとして保持され、予算管理の問題を防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b247a-146">Although you can use Excel for budget planning, the application is kept as a single source of truth and helps prevent budget control issues.</span></span> <span data-ttu-id="b247a-147">定期処理プロセスは、予算作成の初期データを予算計画に移動するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b247a-147">Periodic processes can be used to bring initial data for budgeting into the budget plan.</span></span> <span data-ttu-id="b247a-148">アプリケーションでは、予算作成データを表示および分析できる一連の標準的なレポートの照会ページを提供します。</span><span class="sxs-lookup"><span data-stu-id="b247a-148">For reporting, the application offers a set of standard inquiry pages that let you view and analyze budgeting data.</span></span> <span data-ttu-id="b247a-149">予算計画データは、[Financial Reporting](../general-ledger/financial-reporting-getting-started.md) を使用してアクセスでき、別の予算計画シナリオは、財務諸表で列として表示できます。</span><span class="sxs-lookup"><span data-stu-id="b247a-149">Budget plan data can be accessed through [Financial reporting](../general-ledger/financial-reporting-getting-started.md), and separate budget plan scenarios can be displayed as columns on the Financial report.</span></span>






