---
title: 予算計画
description: このラボの目的は、予算計画領域で、Microsoft Dynamics 365 Finance 機能の更新のガイドされたビューを提供することです。 このラボの目的は、予算計画モジュールのクイック コンフィギュレーションの例、およびこのコンフィギュレーションを使用してどのように予算計画が達成されるかのショーケースを示すことです。
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a59ff16555bfcb55d2f21c09675e7ae0637bca8f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188605"
---
# <a name="budget-planning"></a><span data-ttu-id="c852f-104">予算計画</span><span class="sxs-lookup"><span data-stu-id="c852f-104">Budget planning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c852f-105">このラボの目的は、予算計画領域で、Microsoft Dynamics 365 Finance 機能の更新のガイドされたビューを提供することです。</span><span class="sxs-lookup"><span data-stu-id="c852f-105">The objective of this lab is to provide a guided view of Microsoft Dynamics 365 Finance functionality updates in Budget planning area.</span></span> <span data-ttu-id="c852f-106">このラボの目的は、予算計画モジュールのクイック コンフィギュレーションの例、およびこのコンフィギュレーションを使用してどのように予算計画が達成されるかのショーケースを示すことです。</span><span class="sxs-lookup"><span data-stu-id="c852f-106">The intent of this lab is to illustrate a quick configuration example of budget planning module and showcase how budget planning can be accomplished using this configuration.</span></span>  <span data-ttu-id="c852f-107">この実習では、次の業務プロセスまたはタスクに特に焦点を合わせます。</span><span class="sxs-lookup"><span data-stu-id="c852f-107">This lab will focus specifically on the following business processes or tasks:</span></span>
- <span data-ttu-id="c852f-108">予算計画のための組織階層の作成およびユーザー セキュリティの構成</span><span class="sxs-lookup"><span data-stu-id="c852f-108">Creating organizational hierarchy for budget planning and configuring user security</span></span>
- <span data-ttu-id="c852f-109">予算計画シナリオ、予算計画の列、レイアウトおよび Excel テンプレートの定義</span><span class="sxs-lookup"><span data-stu-id="c852f-109">Defining budget plan scenarios, budget plan columns, layouts and Excel templates</span></span>
- <span data-ttu-id="c852f-110">予算計画プロセスの作成および有効化</span><span class="sxs-lookup"><span data-stu-id="c852f-110">Creating and activating budget planning process</span></span>
- <span data-ttu-id="c852f-111">総勘定元帳からの実績読み込みによる予算計画ドキュメントの作成</span><span class="sxs-lookup"><span data-stu-id="c852f-111">Creating budget plan document by pulling in actuals from General ledger</span></span>
- <span data-ttu-id="c852f-112">配賦を使用した予算計画ドキュメント データの調整</span><span class="sxs-lookup"><span data-stu-id="c852f-112">Using allocations to adjust budget plan document data</span></span>
- <span data-ttu-id="c852f-113">Excel での予算計画ドキュメント データの編集</span><span class="sxs-lookup"><span data-stu-id="c852f-113">Editing budget plan document data in Excel</span></span> 

<a name="prerequisites"></a><span data-ttu-id="c852f-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="c852f-114">Prerequisites</span></span> 
------------------

<span data-ttu-id="c852f-115">このチュートリアルでは、Contoso のデモ データ環境を使用する Microsoft Dynamics 365 Finance にアクセスする必要があり、インスタンスの管理者としてプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="c852f-115">For this tutorial, you’ll need to access the Microsoft Dynamics 365 Finance environment with Contoso demo data, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="c852f-116">このラボにおいてプライベート ブラウザー モードを使用しないでください - 必要に応じてブラウザーの他のどのアカウントからもサインアウトし、管理者認証情報を使用してサインインしてください。</span><span class="sxs-lookup"><span data-stu-id="c852f-116">Do not use In Private browser mode for this lab - sign out from any other account in the browser if needed and sign in with administrator credentials.</span></span> <span data-ttu-id="c852f-117">サインインする時には、「サインインしたままにする」チェック ボックスをオンにする**必要**があります。</span><span class="sxs-lookup"><span data-stu-id="c852f-117">When signing in, you **MUST** check the “Keep me signed in” checkbox.</span></span> <span data-ttu-id="c852f-118">これは、Excel のアプリが現在必要な永続する Cookie を作成します。</span><span class="sxs-lookup"><span data-stu-id="c852f-118">This creates a persistent cookie that the Excel App currently needs.</span></span> <span data-ttu-id="c852f-119">IE 以外のブラウザーを使用してアプリケーションにサインインする場合、Excel のアプリでサインインするように求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c852f-119">If you sign in to the application using a browser other than IE, then you’ll be prompted to sign in within the Excel App.</span></span> <span data-ttu-id="c852f-120">Excel のアプリで「サインイン」をクリックすると、IE のポップアップ ウィンドウが開きます。「サインインしたままにする」チェック ボックスをオンにする**必要**があります。</span><span class="sxs-lookup"><span data-stu-id="c852f-120">When you click “Sign in” in the Excel App, an IE popup window will open and when signing in you **MUST** check the “Keep me signed in” check box.</span></span> <span data-ttu-id="c852f-121">Excel のアプリで「サインイン」をクリックしても何も表示されない場合、IE の Cookie キャッシュを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c852f-121">If clicking “Sign in” in the Excel App doesn’t appear to do anything then you should clear the IE cookie cache.</span></span>

## <a name="scenario-overview"></a><span data-ttu-id="c852f-122">**シナリオの概要**</span><span class="sxs-lookup"><span data-stu-id="c852f-122">**Scenario overview**</span></span>
<span data-ttu-id="c852f-123">ジュリアは、ドイツ (DEMF) の Contoso Entertainment Systems の財務マネージャーとして勤務しています。</span><span class="sxs-lookup"><span data-stu-id="c852f-123">Julia works as a finance manager in Contoso Entertainment Systems in Germany (DEMF).</span></span> <span data-ttu-id="c852f-124">FY2016 が近づき、翌年の会社の予算を設定する業務を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="c852f-124">As FY2016 approaches, she needs to work on setting up the company’s budget for the upcoming year.</span></span> <span data-ttu-id="c852f-125">予算の設定は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="c852f-125">Budget preparation looks as follows:</span></span>

1.  <span data-ttu-id="c852f-126">ジュリアは予算を作成する開始点として前年度の実績を使用します。</span><span class="sxs-lookup"><span data-stu-id="c852f-126">Julia uses previous year actuals amounts as a starting point to create the budget.</span></span>
2.  <span data-ttu-id="c852f-127">前年度の実績に基づいて、翌年の 12 か月間の見積を作成します</span><span class="sxs-lookup"><span data-stu-id="c852f-127">Based on the previous year actuals, she creates estimates for 12 months in the upcoming year</span></span>
3.  <span data-ttu-id="c852f-128">ジュリアは、CFO と予算を確認します。</span><span class="sxs-lookup"><span data-stu-id="c852f-128">Julia reviews the budget with CFO.</span></span> <span data-ttu-id="c852f-129">これらが終了した後に、予算計画に必要な調整を行い、予算の設定を確定します。</span><span class="sxs-lookup"><span data-stu-id="c852f-129">Once done she makes necessary adjustments for the budget plan and finalizes budget preparation.</span></span>

<span data-ttu-id="c852f-130">このシナリオの予算計画コンフィギュレーションのスキーマは次のようになります:</span><span class="sxs-lookup"><span data-stu-id="c852f-130">Budget planning configuration schema for the scenario looks as follows:</span></span>

![予算計画のコンフィギュレーション スキーマ](./media/screenshot1-300x152.png)

<span data-ttu-id="c852f-132">ジュリアは、予算を設定するために、Excel の次のテンプレートを使用します:</span><span class="sxs-lookup"><span data-stu-id="c852f-132">Julia uses the following Excel template to prepare the budget:</span></span>

<span data-ttu-id="c852f-133">[![Excel テンプレート](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-133">[![Excel template](./media/screenshot2-1024x352.png)](./media/screenshot2.png)</span></span>

## <a name="exercise-1-configuration"></a><span data-ttu-id="c852f-134">練習 1: コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c852f-134">Exercise 1: Configuration</span></span>

### <a name="task-1-create-organizational-hierarchy"></a><span data-ttu-id="c852f-135">**タスク 1: 組織階層の作成**</span><span class="sxs-lookup"><span data-stu-id="c852f-135">**Task 1: Create organizational hierarchy**</span></span>
<span data-ttu-id="c852f-136">すべての予算作成プロセスが財務部門で発生すると、ジュリアは、財務部門のみから構成される非常に単純な組織階層を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c852f-136">As all the budgeting process happens in the Finance department, therefore Julia needs to create a very simple organizational hierarchy – consisting of Finance department only.</span></span> <span data-ttu-id="c852f-137">1.1。</span><span class="sxs-lookup"><span data-stu-id="c852f-137">1.1.</span></span> <span data-ttu-id="c852f-138">組織階層 ([組織の管理] &gt; [組織] &gt; [組織階層]) の順に移動し、[新規] ボタンをクリックします</span><span class="sxs-lookup"><span data-stu-id="c852f-138">Navigate to Organization hierarchies (Organization administration &gt; Organizations &gt; Organization hierarchies) and click New button</span></span>

![組織階層](./media/screenshot3.png) 

<span data-ttu-id="c852f-140">1.2。</span><span class="sxs-lookup"><span data-stu-id="c852f-140">1.2.</span></span> <span data-ttu-id="c852f-141">組織階層の名前を入力し、[目的の割り当て] ボタンをクリックします</span><span class="sxs-lookup"><span data-stu-id="c852f-141">Type the name for the organizational hierarchy and click button Assign purpose</span></span>

<span data-ttu-id="c852f-142">[![名前](./media/screenshot4.png)](./media/screenshot4.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-142">[![Name](./media/screenshot4.png)](./media/screenshot4.png)</span></span> 

<span data-ttu-id="c852f-143">1.3。</span><span class="sxs-lookup"><span data-stu-id="c852f-143">1.3.</span></span> <span data-ttu-id="c852f-144">[予算計画目的] を選択し、[追加] ボタンをクリックし、新しく作成された組織階層を割り当てます:</span><span class="sxs-lookup"><span data-stu-id="c852f-144">Select Budget planning purpose, click button Add and assign newly created organizational hierarchy:</span></span> 

<span data-ttu-id="c852f-145">[![目的の割り当て](./media/screenshot5.png)](./media/screenshot5.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-145">[![Assign purpose](./media/screenshot5.png)](./media/screenshot5.png)</span></span>

<span data-ttu-id="c852f-146">1.4。</span><span class="sxs-lookup"><span data-stu-id="c852f-146">1.4.</span></span> <span data-ttu-id="c852f-147">セキュリティの組織のために上記の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="c852f-147">Repeat the step above for Security organizational purpose.</span></span> <span data-ttu-id="c852f-148">終了した際にフォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c852f-148">Close the form when done.</span></span>

<span data-ttu-id="c852f-149">[![セキュリティ組織](./media/screenshot6.png)](./media/screenshot6.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-149">[![Security org](./media/screenshot6.png)](./media/screenshot6.png)</span></span>

<span data-ttu-id="c852f-150">1.5。</span><span class="sxs-lookup"><span data-stu-id="c852f-150">1.5.</span></span> <span data-ttu-id="c852f-151">[組織階層] フォームで [表示] のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c852f-151">In the Organizational Hierarchies form click button View.</span></span> <span data-ttu-id="c852f-152">[階層構造デザイナー] の [編集] をクリックし、[挿入] のボタンをクリックして階層を作成します。</span><span class="sxs-lookup"><span data-stu-id="c852f-152">Click Edit in the Hierarchy designer and create a hierarchy by clicking button Insert.</span></span>

<span data-ttu-id="c852f-153">[![挿入](./media/screenshot7.png)](./media/screenshot7.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-153">[![Insert](./media/screenshot7.png)](./media/screenshot7.png)</span></span> 

<span data-ttu-id="c852f-154">1.6。</span><span class="sxs-lookup"><span data-stu-id="c852f-154">1.6.</span></span> <span data-ttu-id="c852f-155">予算の階層の [財務部門] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c852f-155">Select Finance department for the budgeting hierarchy.</span></span> 

<span data-ttu-id="c852f-156">[![財務](./media/screenshot8.png)](./media/screenshot8.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-156">[![Finance](./media/screenshot8.png)](./media/screenshot8.png)</span></span>

<span data-ttu-id="c852f-157">1.7。</span><span class="sxs-lookup"><span data-stu-id="c852f-157">1.7.</span></span> <span data-ttu-id="c852f-158">終了後、[公開] および [終了] のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c852f-158">When done, click button Publish and Close.</span></span> <span data-ttu-id="c852f-159">階層の発行の有効日として [2015 年 1 月 1 日] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c852f-159">Select 1/1/2015 as effective date for hierarchy publishing.</span></span>

<span data-ttu-id="c852f-160">[![有効日](./media/screenshot9.png)](./media/screenshot9.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-160">[![Effective date](./media/screenshot9.png)](./media/screenshot9.png)</span></span>

### <a name="task-2-configure-user-security"></a><span data-ttu-id="c852f-161">タスク 2: ユーザーのセキュリティのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c852f-161">Task 2: Configure user security</span></span>
<span data-ttu-id="c852f-162">予算計画は、予算計画のデータへのアクセスを構成する際に特別なセキュリティ ポリシーを使用します。</span><span class="sxs-lookup"><span data-stu-id="c852f-162">Budget planning uses special security policies to configure access to budget plans data.</span></span> <span data-ttu-id="c852f-163">ジュリアは、自分自身に対して、財務予算計画へのアクセス権を与える必要があります。</span><span class="sxs-lookup"><span data-stu-id="c852f-163">Julia needs to give access to Finance budget plans for herself.</span></span> 

<span data-ttu-id="c852f-164">2.1。</span><span class="sxs-lookup"><span data-stu-id="c852f-164">2.1.</span></span> <span data-ttu-id="c852f-165">DEMF の法人のコンテキストに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="c852f-165">Switch to DEMF legal entity context.</span></span> 


<span data-ttu-id="c852f-166">2.2.</span><span class="sxs-lookup"><span data-stu-id="c852f-166">2.2.</span></span> <span data-ttu-id="c852f-167">[予算作成] &gt; [設定] &gt; [予算計画] &gt; [予算計画のコンフィギュレーション] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c852f-167">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="c852f-168">パラメータータブで、セキュリティ モデルの値を、セキュリティの組織に基づいて設定します</span><span class="sxs-lookup"><span data-stu-id="c852f-168">In Parameters tab, set the Security model value to Based on security organizations</span></span> 

<span data-ttu-id="c852f-169">[![パラメータ](./media/screenshot11.png)](./media/screenshot11.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-169">[![Parameters](./media/screenshot11.png)](./media/screenshot11.png)</span></span> 

<span data-ttu-id="c852f-170">2.3.</span><span class="sxs-lookup"><span data-stu-id="c852f-170">2.3.</span></span> <span data-ttu-id="c852f-171">[システム管理] &gt; [ユーザー] &gt; [ユーザー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c852f-171">Navigate to System administration &gt; Users &gt; Users.</span></span> <span data-ttu-id="c852f-172">管理者 (ジュリア ファンダーバーク) の予算マネージャーのロールをユーザーに付与します。</span><span class="sxs-lookup"><span data-stu-id="c852f-172">Give user Admin (Julia Funderburk) Budget manager role.</span></span> 

<span data-ttu-id="c852f-173">[![予算マネージャー](./media/screenshot12.png)](./media/screenshot12.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-173">[![Budget manager](./media/screenshot12.png)](./media/screenshot12.png)</span></span> 

<span data-ttu-id="c852f-174">2.4.</span><span class="sxs-lookup"><span data-stu-id="c852f-174">2.4.</span></span> <span data-ttu-id="c852f-175">ユーザー ロールを選択し、組織の割り当てをクリックします</span><span class="sxs-lookup"><span data-stu-id="c852f-175">Pick user role and click Assign organizations</span></span> 

<span data-ttu-id="c852f-176">[![組織の割り当て](./media/screenshot13.png)](./media/screenshot13.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-176">[![Assign org](./media/screenshot13.png)](./media/screenshot13.png)</span></span>

<span data-ttu-id="c852f-177">2.5.</span><span class="sxs-lookup"><span data-stu-id="c852f-177">2.5.</span></span> <span data-ttu-id="c852f-178">「特定の組織にアクセス許可を付与」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c852f-178">Select “Grant access to specific organizations”.</span></span> <span data-ttu-id="c852f-179">最初の手順で作成した [組織階層] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c852f-179">Pick Organizational hierarchy created in the first step.</span></span> <span data-ttu-id="c852f-180">財務のノードを選択し、子を含むアクセス許可のボタンをクリックします</span><span class="sxs-lookup"><span data-stu-id="c852f-180">Pick Finance node and click Grant with children button</span></span> 

<span data-ttu-id="c852f-181">***重要!***</span><span class="sxs-lookup"><span data-stu-id="c852f-181">***Important!***</span></span> <span data-ttu-id="c852f-182">*– このタスクを実行する際には、DEMF の法人のコンテキストにいることを確認してください。組織のセキュリティは、法人のエンティティごとに適用されるからです*</span><span class="sxs-lookup"><span data-stu-id="c852f-182">*Make sure you are in DEMF legal entity context when performing this task, as Organizational security is applied per legal entity*</span></span> 

### <a name="task-3-create-scenarios"></a><span data-ttu-id="c852f-183">タスク 3: シナリオの作成</span><span class="sxs-lookup"><span data-stu-id="c852f-183">Task 3: Create scenarios</span></span>
<span data-ttu-id="c852f-184">3.1。</span><span class="sxs-lookup"><span data-stu-id="c852f-184">3.1.</span></span> <span data-ttu-id="c852f-185">[予算作成] &gt; [設定] &gt; [予算計画] &gt; [予算計画のコンフィギュレーション] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c852f-185">Navigate to Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="c852f-186">シナリオのページで、このラボでさらに使用するシナリオに注意してください: 前年度の実績と予算。</span><span class="sxs-lookup"><span data-stu-id="c852f-186">In the Scenarios page note the scenarios we are going to use further in this lab: Previous year actuals and Budgeted.</span></span> 

<span data-ttu-id="c852f-187">*注: 必要であれば、この練習用の新しいシナリオを作成し、それらを代わりに使用します。*</span><span class="sxs-lookup"><span data-stu-id="c852f-187">*Note: You can create new scenarios for this exercise if desired and use those instead.*</span></span> 

<span data-ttu-id="c852f-188">[![新しいシナリオ](./media/screenshot15.png)](./media/screenshot15.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-188">[![New scenarios](./media/screenshot15.png)](./media/screenshot15.png)</span></span> 

<span data-ttu-id="c852f-189">*注: ジュリアは予算計画に正式な承認プロセスを使用していないため、ワークフロー、ステージおよびこの実習でのワークフロー ステージの設定を省き、既存の自動的に承認する設定を使用します。このワークフロー コンフィギュレーションについては付録を参照してください。*</span><span class="sxs-lookup"><span data-stu-id="c852f-189">*Note: as Julia is not using formal approval process for budget preparation, we will skip Workflows, Stages and Workflow stages setup in this lab and will use existing setup for Auto – approve workflow. See appendix for this workflow configuration.*</span></span>

### <a name="task-4-create-budget-plan-columns"></a><span data-ttu-id="c852f-190">タスク 4: 予算計画の列の作成</span><span class="sxs-lookup"><span data-stu-id="c852f-190">Task 4: Create budget plan columns</span></span>
<span data-ttu-id="c852f-191">予算計画の列は、予算計画のドキュメント レイアウトに使用できる金銭情報または数量に基づく列です。</span><span class="sxs-lookup"><span data-stu-id="c852f-191">Budget plan columns are either Monetary or quantity based columns that can be used in budget plan document layout.</span></span> <span data-ttu-id="c852f-192">上記の例では、"前年度" の実績を表す列、および会計年度の各月を表す 12 の列を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c852f-192">In our example we need to create a column for Previous year actuals and 12 columns to represent each month in a budgeted year.</span></span> <span data-ttu-id="c852f-193">列は単純に [追加] ボタンをクリックして値を入力するか、または "データ エンティティ" を使用して作成します。</span><span class="sxs-lookup"><span data-stu-id="c852f-193">Columns can be created either by simply clicking Add button and filling in the values, or with a help of Data entity.</span></span> <span data-ttu-id="c852f-194">このラボでは、値を入力するために "データ エンティティ" を使用します。</span><span class="sxs-lookup"><span data-stu-id="c852f-194">In this lab we will use Data entity to fill in the values.</span></span> 

<span data-ttu-id="c852f-195">4.1。</span><span class="sxs-lookup"><span data-stu-id="c852f-195">4.1.</span></span> <span data-ttu-id="c852f-196">[予算作成] &gt; [設定] &gt; [予算計画] &gt; [予算計画のコンフィギュレーション] で "列" ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="c852f-196">In Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration open Columns page.</span></span> <span data-ttu-id="c852f-197">フォームの右上隅にある Office ボタンをクリックして、列 (フィルター処理なし) を選択します</span><span class="sxs-lookup"><span data-stu-id="c852f-197">Click Office button on the top right corner of the form and pick Columns (unfiltered)</span></span> 

<span data-ttu-id="c852f-198">[![列のフィルターなし](./media/screenshot16.png)](./media/screenshot16.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-198">[![Columns unfiltered](./media/screenshot16.png)](./media/screenshot16.png)</span></span> 

<span data-ttu-id="c852f-199">4.2.</span><span class="sxs-lookup"><span data-stu-id="c852f-199">4.2.</span></span> <span data-ttu-id="c852f-200">システムは、値を入力するために使用する Excel ブックを開きます。</span><span class="sxs-lookup"><span data-stu-id="c852f-200">System will open Excel workbook to be used for filling in the values.</span></span> <span data-ttu-id="c852f-201">メッセージが表示されたら、編集機能を有効にする、次いでこのアプリを信頼するをクリックします</span><span class="sxs-lookup"><span data-stu-id="c852f-201">If prompted, click Enable Editing and Trust this app</span></span> 

<span data-ttu-id="c852f-202">[![編集機能を有効にする](./media/screenshot18.png)](./media/screenshot18.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-202">[![Enable editing](./media/screenshot18.png)](./media/screenshot18.png)</span></span> 

<span data-ttu-id="c852f-203">[![このアプリを信頼する](./media/screenshot17.png)](./media/screenshot17.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-203">[![Trust this app](./media/screenshot17.png)](./media/screenshot17.png)</span></span>

<span data-ttu-id="c852f-204">4.3.</span><span class="sxs-lookup"><span data-stu-id="c852f-204">4.3.</span></span> <span data-ttu-id="c852f-205">値を入力するために、より多くの列が必要です。</span><span class="sxs-lookup"><span data-stu-id="c852f-205">We will need more columns to fill the values in.</span></span> <span data-ttu-id="c852f-206">右側のウィンドウでデザインをクリックして、グリッドに列を追加します:</span><span class="sxs-lookup"><span data-stu-id="c852f-206">Click Design on the right side pane to add the columns to the grid:</span></span> 

<span data-ttu-id="c852f-207">[![デザイン](./media/screenshot19.png)](./media/screenshot19.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-207">[![Design](./media/screenshot19.png)](./media/screenshot19.png)</span></span> 

<span data-ttu-id="c852f-208">4.4.</span><span class="sxs-lookup"><span data-stu-id="c852f-208">4.4.</span></span> <span data-ttu-id="c852f-209">PlanColumns の横にある小さい鉛筆のボタンをクリックして、グリッドに追加する利用可能な列を表示します</span><span class="sxs-lookup"><span data-stu-id="c852f-209">Click little pencil button next to PlanColumns to see available columns to add to the grid</span></span> 

<span data-ttu-id="c852f-210">[![編集](./media/screenshot20.png)](./media/screenshot20.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-210">[![Edit](./media/screenshot20.png)](./media/screenshot20.png)</span></span> 

<span data-ttu-id="c852f-211">4.5.</span><span class="sxs-lookup"><span data-stu-id="c852f-211">4.5.</span></span> <span data-ttu-id="c852f-212">使用可能な各フィールドをダブルクックし、それらを選択したフィールドに追加し、更新をクリックします</span><span class="sxs-lookup"><span data-stu-id="c852f-212">Double click on each available field to add them to Selected fields and click Update</span></span> 

![更新](./media/screenshot21.png)<span data-ttu-id="c852f-214">](./media/screenshot21.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-214">](./media/screenshot21.png)</span></span> 

<span data-ttu-id="c852f-215">4.6.</span><span class="sxs-lookup"><span data-stu-id="c852f-215">4.6.</span></span> <span data-ttu-id="c852f-216">Excel の表に作成する必要があるすべての列を追加します。</span><span class="sxs-lookup"><span data-stu-id="c852f-216">In Excel table add all the columns that need to be created.</span></span> <span data-ttu-id="c852f-217">Excel のオートフィル機能を使用して、明細行をすばやく追加します。</span><span class="sxs-lookup"><span data-stu-id="c852f-217">Use AutoFill feature in Excel to add the lines quickly.</span></span> <span data-ttu-id="c852f-218">テーブルの一部として明細行が追加されたことを確認します (上下スクロールを使用する場合、グリッドの上部で列のヘッダーを表示できます)</span><span class="sxs-lookup"><span data-stu-id="c852f-218">Make sure the lines are added as a part of the table (when using vertical scroll, you should be able to see column headers on the top of the grid)</span></span> 

<span data-ttu-id="c852f-219">[![オートフィル](./media/screenshot22.png)](./media/screenshot22.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-219">[![Autofill](./media/screenshot22.png)](./media/screenshot22.png)</span></span> 

<span data-ttu-id="c852f-220">4.7.</span><span class="sxs-lookup"><span data-stu-id="c852f-220">4.7.</span></span> <span data-ttu-id="c852f-221">アプリケーションに戻り、ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="c852f-221">Return to the application and refresh the page.</span></span> <span data-ttu-id="c852f-222">公開された値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c852f-222">Published values will appear.</span></span> 

<span data-ttu-id="c852f-223">[![更新反映](./media/screenshot23.png)](./media/screenshot23.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-223">[![Refresh](./media/screenshot23.png)](./media/screenshot23.png)</span></span>

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a><span data-ttu-id="c852f-224">タスク 5: 予算計画のドキュメント レイアウトおよびテンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="c852f-224">Task 5: Create budget plan document layouts and templates</span></span>
<span data-ttu-id="c852f-225">レイアウトは、ユーザーが予算計画のドキュメントを開いたときに、予算計画ドキュメントの行グリッドが、どのように表示されるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="c852f-225">Layout defines how budget plan document lines grid is going to look like when user opens budget plan document.</span></span> <span data-ttu-id="c852f-226">さまざまな角度で同じデータを表示するように予算計画のドキュメントのレイアウトを切り替えることもできます。</span><span class="sxs-lookup"><span data-stu-id="c852f-226">It is also possible to switch the layout for budget plan document to see the same data in different angles.</span></span> <span data-ttu-id="c852f-227">ここでは、ジュリアが予算計画のドキュメントで使用するために定義した列があるため、ジュリアは、予算データ (このラボのシナリオの概要セクションを参照) を作成するために使用する Excel の表に似た、予算計画のドキュメント レイアウトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c852f-227">Now, as she’s got columns defined to be used with our budget plan document, Julia needs to create a budget plan document layout, that would look similar to the Excel table she uses to create budget data (see section Scenario overview in this lab)</span></span> 

<span data-ttu-id="c852f-228">5.1.</span><span class="sxs-lookup"><span data-stu-id="c852f-228">5.1.</span></span> <span data-ttu-id="c852f-229">[予算作成] &gt; [設定] &gt; [予算計画] &gt; [予算計画のコンフィギュレーション] で "レイアウト" ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="c852f-229">In Budgeting&gt;Setup &gt; Budget planning &gt; Budget planning configuration open Layouts page.</span></span> <span data-ttu-id="c852f-230">月間の予算入力のために新しいレイアウトを作成します。</span><span class="sxs-lookup"><span data-stu-id="c852f-230">Create a new layout for Monthly budget entry:</span></span>

-   <span data-ttu-id="c852f-231">レイアウトに主勘定と業務単位を含めるために、MA+BU の分析コード セットを選択します。</span><span class="sxs-lookup"><span data-stu-id="c852f-231">Pick MA+BU dimension set to include Main accounts and Business units to the layout.</span></span>
-   <span data-ttu-id="c852f-232">[要素] セクションの前の手順で作成された、すべての予算計画の列を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="c852f-232">List all budget plan columns created in the previous step in the Elements section.</span></span> <span data-ttu-id="c852f-233">前年度の実績を除くすべてを編集可能にします。</span><span class="sxs-lookup"><span data-stu-id="c852f-233">Make all but Previous year actuals editable.</span></span>
-   <span data-ttu-id="c852f-234">どの財務分析コードをグリッドの説明に表示するかを選択するには、[説明] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c852f-234">Click Descriptions button to select which financial dimensions should display Descriptions in the grid.</span></span>

<span data-ttu-id="c852f-235">[![説明](./media/screenshot24.png)](./media/screenshot24.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-235">[![Descriptions](./media/screenshot24.png)](./media/screenshot24.png)</span></span> 

<span data-ttu-id="c852f-236">予算計画レイアウト定義に基づいて、予算データを編集する代替方法として Excel テンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c852f-236">Based on the budget plan layout definition we can create an Excel template to be used as an alternative way to edit Budget data.</span></span> <span data-ttu-id="c852f-237">Excel テンプレートは、予算計画のレイアウト定義と一致している必要があるために、Excel テンプレートの生成後に予算計画のレイアウトは編集できません。したがって、すべてのレイアウトのコンポーネントが定義された後に、このタスクは実行される必要があります。</span><span class="sxs-lookup"><span data-stu-id="c852f-237">As Excel template has to match budget plan layout definition, you won’t be able to edit budget plan layout after generating Excel template, therefore this task should be done after all layout components are defined.</span></span> 

<span data-ttu-id="c852f-238">5.2。</span><span class="sxs-lookup"><span data-stu-id="c852f-238">5.2.</span></span> <span data-ttu-id="c852f-239">5.1 ステップで作成されたレイアウトを表示するには、</span><span class="sxs-lookup"><span data-stu-id="c852f-239">For the layout created in the 5.1.</span></span> <span data-ttu-id="c852f-240">[テンプレート] &gt; [生成] の順にボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c852f-240">step, click button Template &gt; Generate.</span></span> <span data-ttu-id="c852f-241">警告メッセージを確認します。</span><span class="sxs-lookup"><span data-stu-id="c852f-241">Confirm the warning message.</span></span> <span data-ttu-id="c852f-242">テンプレートを表示するには、[テンプレート] &gt; [ビュー] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="c852f-242">To view the template, click Template &gt; View.</span></span> 

<span data-ttu-id="c852f-243">*注: 名前を付けて保存を選択し、編集できるようにテンプレートを保存する場所を選択してください。ユーザーが、保存しないでダイアログで開くを選択した場合、ファイルへの変更は、ファイルを閉じたときに残りません。* 
[![テンプレート ビュー](./media/screenshot25.png)](./media/screenshot25.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-243">*Note: Make sure to select “Save as” and select the place where template should be stored in order to edit it. If user selects “Open” in the dialog without saving, the changes done to the file will not be retained when the file is closed.* 
[![Template view](./media/screenshot25.png)](./media/screenshot25.png)</span></span> 

<span data-ttu-id="c852f-244">5.3.</span><span class="sxs-lookup"><span data-stu-id="c852f-244">5.3.</span></span> <span data-ttu-id="c852f-245">&lt; オプションのステップ&gt; Excel テンプレートを変更して、フォーミュラの合計、ヘッダー フィールド、書式などの追加により、より使いやすくすることができます。変更を保存し、レイアウト &gt; アップロードの順にクリックして、予算計画レイアウトにファイルをアップロードします[![アップロード](./media/screenshot26.png)](./media/screenshot26.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-245">&lt; Optional step&gt; Modify Excel template to make it look more user friendly – add total formulas, header fields, formatting, etc. Save the changes and upload the file to budget plan layout by clicking Layout &gt; Upload [![Upload](./media/screenshot26.png)](./media/screenshot26.png)</span></span>

### <a name="task-6-create-a-budget-planning-process"></a><span data-ttu-id="c852f-246">タスク 6: 予算計画プロセスの作成</span><span class="sxs-lookup"><span data-stu-id="c852f-246">Task 6: Create a budget planning process</span></span>
<span data-ttu-id="c852f-247">ジュリアは、新たな予算計画を開始するために、上記のすべての設定を組み合わせて、新しい予算計画プロセスを作成して有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c852f-247">Julia needs to create and activate a new budget planning process combining all the setup above to start entering budget plans.</span></span> <span data-ttu-id="c852f-248">予算計画プロセスは、どの予算作成の組織、ワークフロー、レイアウトおよびテンプレートが予算計画の作成に使用されるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="c852f-248">Budget planning process defines what budgeting organizations, workflow, layouts and templates will be used for creating budget plans.</span></span> 

<span data-ttu-id="c852f-249">6.1。</span><span class="sxs-lookup"><span data-stu-id="c852f-249">6.1.</span></span> <span data-ttu-id="c852f-250">[予算作成] &gt; [設定] &gt; [予算計画] &gt; [予算計画プロセス] の順に移動し、新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="c852f-250">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning process and create a new record.</span></span>

-   <span data-ttu-id="c852f-251">予算計画プロセス - DEMF FY2016 予算作成</span><span class="sxs-lookup"><span data-stu-id="c852f-251">Budget planning process – DEMF budgeting FY2016</span></span>
-   <span data-ttu-id="c852f-252">予算サイクル – FY2016</span><span class="sxs-lookup"><span data-stu-id="c852f-252">Budget cycle – FY2016</span></span>
-   <span data-ttu-id="c852f-253">元帳 – DEMF</span><span class="sxs-lookup"><span data-stu-id="c852f-253">Ledger – DEMF</span></span>
-   <span data-ttu-id="c852f-254">既定の勘定構造 – 製造損益</span><span class="sxs-lookup"><span data-stu-id="c852f-254">Default account structure – Manufacturing P&L</span></span>
-   <span data-ttu-id="c852f-255">組織階層 - ラボの最初に作成した階層の選択</span><span class="sxs-lookup"><span data-stu-id="c852f-255">Organization hierarchy – pick the hierarchy created in the beginning of the lab</span></span>
-   <span data-ttu-id="c852f-256">予算計画のワークフロー - 自動割り当て - 財務部門のワークフローの承認</span><span class="sxs-lookup"><span data-stu-id="c852f-256">Budget planning workflow – assign Auto – Approve workflow for Finance department</span></span>
-   <span data-ttu-id="c852f-257">予算計画のステージ ルールとテンプレートでは、各ワークフローの "予算" 計画ステージが、明細行の "追加" および明細行の "変更" が許可された場合に選択されるか、またどの "レイアウト" が既定で使用されるかが選択されます。</span><span class="sxs-lookup"><span data-stu-id="c852f-257">In budget planning stage rules and templates, for each workflow Budget planning stage pick if Adding lines and Modifying lines is allowed and what Layout should be used by default</span></span>

<span data-ttu-id="c852f-258">*注: 追加のドキュメント レイアウトを作成し、それらを [代替レイアウト] ボタンをクリックして、予算計画のワークフロー ステージで使用できるように割り当てることができます。*</span><span class="sxs-lookup"><span data-stu-id="c852f-258">*Note: You can create additional document layouts and assign them to be available in budget planning workflow stage by clicking Alternate layouts button.*</span></span> 

<span data-ttu-id="c852f-259">[![代替レイアウト](./media/screenshot27.png)](./media/screenshot27.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-259">[![Alternate layouts](./media/screenshot27.png)](./media/screenshot27.png)</span></span> 

<span data-ttu-id="c852f-260">6.2.</span><span class="sxs-lookup"><span data-stu-id="c852f-260">6.2.</span></span> <span data-ttu-id="c852f-261">アクション &gt; 有効化を選択して、この予算計画ワークフローを有効化します</span><span class="sxs-lookup"><span data-stu-id="c852f-261">Select Actions &gt; Activate to activate this budget planning workflow</span></span> 

<span data-ttu-id="c852f-262">[![有効化する](./media/screenshot28.png)](./media/screenshot28.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-262">[![Activate](./media/screenshot28.png)](./media/screenshot28.png)</span></span>

## <a name="exercise-2-process-simulation"></a><span data-ttu-id="c852f-263">練習 2: プロセスのシミュレーション</span><span class="sxs-lookup"><span data-stu-id="c852f-263">Exercise 2: Process simulation</span></span>

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a><span data-ttu-id="c852f-264">タスク 7: 総勘定元帳から予算計画の初期データを生成する</span><span class="sxs-lookup"><span data-stu-id="c852f-264">Task 7: Generate initial data for budget plan from General ledger</span></span>
<span data-ttu-id="c852f-265">7.1。</span><span class="sxs-lookup"><span data-stu-id="c852f-265">7.1.</span></span> <span data-ttu-id="c852f-266">[予算作成] &gt; [定期処理] &gt; [一般会計から予算計画を生成] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c852f-266">Navigate to Budgeting &gt; Periodic &gt; Generate budget plan from General ledger.</span></span> <span data-ttu-id="c852f-267">定期的なプロセス パラメーターを入力し、[生成] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c852f-267">Fill in the periodic process parameters and click button Generate.</span></span> 

<span data-ttu-id="c852f-268">[![生成](./media/screenshot29.png)](./media/screenshot29.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-268">[![Generate](./media/screenshot29.png)](./media/screenshot29.png)</span></span> 

<span data-ttu-id="c852f-269">7.2.</span><span class="sxs-lookup"><span data-stu-id="c852f-269">7.2.</span></span> <span data-ttu-id="c852f-270">[予算作成] &gt; [予算計画] の順に移動し、[プロセスの生成] で作成された予算計画を見つけます。</span><span class="sxs-lookup"><span data-stu-id="c852f-270">Navigate to Budgeting &gt; Budget plans to find a budget plan created by Generate process.</span></span> 

<span data-ttu-id="c852f-271">[![予算計画](./media/screenshot30.png)](./media/screenshot30.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-271">[![Budget plan](./media/screenshot30.png)](./media/screenshot30.png)</span></span> 

<span data-ttu-id="c852f-272">7.3.</span><span class="sxs-lookup"><span data-stu-id="c852f-272">7.3.</span></span> <span data-ttu-id="c852f-273">[文書番号] のハイパーリンクをクリックしてドキュメントの詳細を開きます。</span><span class="sxs-lookup"><span data-stu-id="c852f-273">Open document details by clicking on Document number hyperlink.</span></span> <span data-ttu-id="c852f-274">予算計画は、このラボで作成されたレイアウトで定義されたように表示されます</span><span class="sxs-lookup"><span data-stu-id="c852f-274">Budget plan is displayed as defined in the layout created during this lab</span></span> 

<span data-ttu-id="c852f-275">[![予算計画表示](./media/screenshot31.png)](./media/screenshot31.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-275">[![Budget plan display](./media/screenshot31.png)](./media/screenshot31.png)</span></span>

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a><span data-ttu-id="c852f-276">タスク 8: 前年度の実績に基づく今年度の予算の作成</span><span class="sxs-lookup"><span data-stu-id="c852f-276">Task 8: Create current year budget based on previous year actuals</span></span>
<span data-ttu-id="c852f-277">配賦方法を予算計画で使用できます。これにより、1 つのシナリオから別のシナリオに予算計画を簡単にコピーする、それらを複数の期間に分割する、または分析コードに配賦することができます。</span><span class="sxs-lookup"><span data-stu-id="c852f-277">Allocation methods can be used in budget plan to easily copy information for budget plans from one scenario to another/ spread them across periods/ allocate to dimensions.</span></span> <span data-ttu-id="c852f-278">前年度の実績からの今年度の予算を作成するために配賦を使用します。</span><span class="sxs-lookup"><span data-stu-id="c852f-278">We will use allocations to create current year budget from previous year actuals.</span></span> 

<span data-ttu-id="c852f-279">8.1。</span><span class="sxs-lookup"><span data-stu-id="c852f-279">8.1.</span></span> <span data-ttu-id="c852f-280">予算計画ドキュメント グリッドのすべての行を選択し、予算の配賦ボタンをクリックします</span><span class="sxs-lookup"><span data-stu-id="c852f-280">Pick all lines in the budget plan document grid and click button allocate budget</span></span> 

<span data-ttu-id="c852f-281">[![すべての行](./media/screenshot32.png)](./media/screenshot32.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-281">[![All lines](./media/screenshot32.png)](./media/screenshot32.png)</span></span> 

<span data-ttu-id="c852f-282">8.2.</span><span class="sxs-lookup"><span data-stu-id="c852f-282">8.2.</span></span> <span data-ttu-id="c852f-283">配賦方法、期間キー、ソース シナリオとターゲット シナリオを選択し、[配賦] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c852f-283">Select allocation method, Period key, Source and destination scenarios and click Allocate</span></span> 

<span data-ttu-id="c852f-284">[![配賦](./media/screenshot33.png)](./media/screenshot33.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-284">[![Allocate](./media/screenshot33.png)](./media/screenshot33.png)</span></span>

<span data-ttu-id="c852f-285">前年の実績金額が今年度の予算にコピーされ、[販売曲線期間] キーを使用して、それらを複数の期間に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c852f-285">The previous year actual amounts will be copied to current year budget and allocate them across periods using Sales curve period key.</span></span> 

<span data-ttu-id="c852f-286">[![販売曲線](./media/screenshot34.png)](./media/screenshot34.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-286">[![Sales curve](./media/screenshot34.png)](./media/screenshot34.png)</span></span>

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a><span data-ttu-id="c852f-287">タスク 9: 予算計画ドキュメントを Excel を使用して調整し、ドキュメントを確定する</span><span class="sxs-lookup"><span data-stu-id="c852f-287">Task 9: Adjust budget plan document using Excel and finalize the document</span></span>
<span data-ttu-id="c852f-288">9.1。</span><span class="sxs-lookup"><span data-stu-id="c852f-288">9.1.</span></span> <span data-ttu-id="c852f-289">[ボタン ワークシート] をクリックして、Excel でドキュメントの内容を開きます</span><span class="sxs-lookup"><span data-stu-id="c852f-289">Click Button worksheet to open document contents in Excel</span></span>

<span data-ttu-id="c852f-290">[![Excel](./media/screenshot35.png)](./media/screenshot35.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-290">[![Excel](./media/screenshot35.png)](./media/screenshot35.png)</span></span>

<span data-ttu-id="c852f-291">9.2。</span><span class="sxs-lookup"><span data-stu-id="c852f-291">9.2.</span></span> <span data-ttu-id="c852f-292">Excel ブックを開いて、予算計画ドキュメントで番号を調整し、[公開] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c852f-292">When Excel workbook opens, adjust the numbers in budget plan document and click button Publish.</span></span>

<span data-ttu-id="c852f-293">[![パブリッシュ](./media/screenshot36.png)](./media/screenshot36.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-293">[![Publish](./media/screenshot36.png)](./media/screenshot36.png)</span></span>

<span data-ttu-id="c852f-294">9.3。</span><span class="sxs-lookup"><span data-stu-id="c852f-294">9.3.</span></span> <span data-ttu-id="c852f-295">予算計画ドキュメントに戻ります。</span><span class="sxs-lookup"><span data-stu-id="c852f-295">Return to budget plan document.</span></span> <span data-ttu-id="c852f-296">[ワークフロー] &gt; [提出] の順にクリックして、ドキュメントを自動承認します。</span><span class="sxs-lookup"><span data-stu-id="c852f-296">Click Workflow &gt; Submit to Auto-approve the document</span></span>

<span data-ttu-id="c852f-297">[![自動承認](./media/screenshot37.png)](./media/screenshot37.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-297">[![Auto-approve](./media/screenshot37.png)](./media/screenshot37.png)</span></span> 

<span data-ttu-id="c852f-298">ワークフローが完了すると、予算計画ドキュメント ステージは [承認済] に変更します。</span><span class="sxs-lookup"><span data-stu-id="c852f-298">Once workflow completes, budget plan document stage changes to Approved.</span></span> <span data-ttu-id="c852f-299">[![承認済](./media/screenshot38.png)](./media/screenshot38.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-299">[![Approved](./media/screenshot38.png)](./media/screenshot38.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="c852f-300">付録</span><span class="sxs-lookup"><span data-stu-id="c852f-300">Appendix</span></span>

### <a name="auto-approve-workflow-configuration"></a><span data-ttu-id="c852f-301">自動承認ワークフロー コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c852f-301">Auto-Approve workflow configuration</span></span>

<span data-ttu-id="c852f-302">A.</span><span class="sxs-lookup"><span data-stu-id="c852f-302">A.</span></span> <span data-ttu-id="c852f-303">[予算作成] &gt; [設定] &gt; [予算計画] &gt; [予算作成ワークフロー] 予算計画ワークフローのテンプレートを使用して新しいワークフローを作成します:</span><span class="sxs-lookup"><span data-stu-id="c852f-303">Budgeting &gt; Setup &gt; Budget planning &gt; Budgeting workflows Create a new workflow using template Budget planning workflows:</span></span>

<span data-ttu-id="c852f-304">[![新しいワークフローの作成](./media/screenshot39.png)](./media/screenshot39.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-304">[![Create a new workflow](./media/screenshot39.png)](./media/screenshot39.png)</span></span>

<span data-ttu-id="c852f-305">このワークフローは、予算計画のステージ移行という 1 つのタスクだけを含みます。</span><span class="sxs-lookup"><span data-stu-id="c852f-305">This workflow will contain only one task – Stage transition budget plan</span></span> 

<span data-ttu-id="c852f-306">[![予算計画のステージ移行](./media/screenshot40.png)](./media/screenshot40.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-306">[![Stage transition budget plan](./media/screenshot40.png)](./media/screenshot40.png)</span></span> 

<span data-ttu-id="c852f-307">保存してワークフローを有効化します。</span><span class="sxs-lookup"><span data-stu-id="c852f-307">Save and activate the workflow.</span></span> 

<span data-ttu-id="c852f-308">B.</span><span class="sxs-lookup"><span data-stu-id="c852f-308">B.</span></span> <span data-ttu-id="c852f-309">[予算作成] &gt; [設定] &gt; [予算計画] &gt; [予算計画のコンフィギュレーション] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c852f-309">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="c852f-310">[ステージ] タブで、[初期] および [送信済] という、2 つのステージを作成します。</span><span class="sxs-lookup"><span data-stu-id="c852f-310">In Stages tab create 2 stages – Initial and Submitted</span></span> 

<span data-ttu-id="c852f-311">[![初期および送信済](./media/screenshot41.png)](./media/screenshot41.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-311">[![Initial and submitted](./media/screenshot41.png)](./media/screenshot41.png)</span></span>

<span data-ttu-id="c852f-312">C.</span><span class="sxs-lookup"><span data-stu-id="c852f-312">C.</span></span> <span data-ttu-id="c852f-313">[予算作成] &gt; [設定] &gt; [予算計画] &gt; [予算計画のコンフィギュレーション] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c852f-313">Navigate to Budgeting &gt; Setup &gt; Budget planning &gt; Budget planning configuration.</span></span> <span data-ttu-id="c852f-314">[ワークフロー ステージ] タブで、[初期] および [送信済] というステージと共に、A ステップで作成された [自動承認] ワークフローを関連付けます</span><span class="sxs-lookup"><span data-stu-id="c852f-314">In Workflow Stages tab Associate the workflow Auto – approve created in A step with the stages Initial and Submitted</span></span> 

<span data-ttu-id="c852f-315">[![予算作成および予算計画](./media/screenshot42.png)](./media/screenshot42.png)</span><span class="sxs-lookup"><span data-stu-id="c852f-315">[![Budgeting and budget planning](./media/screenshot42.png)](./media/screenshot42.png)</span></span>  


