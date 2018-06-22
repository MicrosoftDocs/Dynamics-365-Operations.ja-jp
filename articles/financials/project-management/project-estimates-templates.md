---
title: "Project Service Automation からプロジェクト見積を直接 Finance and Operations のプロジェクト予測に同期します"
description: "このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へプロジェクト時間見積およびプロジェクト経費見積を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: ja-jp
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a><span data-ttu-id="8917d-103">Project Service Automation からプロジェクト見積を直接 Finance and Operations のプロジェクト予測に同期します</span><span class="sxs-lookup"><span data-stu-id="8917d-103">Synchronize project estimates from Project Service Automation directly to project forecasts in Finance and Operations</span></span>

<span data-ttu-id="8917d-104">このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へプロジェクト時間見積およびプロジェクト経費見積を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8917d-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="8917d-105">プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="8917d-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="8917d-106">Project Service Automation から Finance and Operations のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="8917d-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="8917d-107">Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="8917d-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="8917d-108">データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト時間見積およびプロジェクト経費見積に関するデータ フローを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8917d-108">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="8917d-109">次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8917d-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="8917d-110">[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="8917d-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="8917d-111">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="8917d-111">Templates and tasks</span></span>

<span data-ttu-id="8917d-112">使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="8917d-112">To access the available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="8917d-113">次のテンプレートおよび基本的なタスクはプロジェクト時間見積を Project Service Automation から Finance and Operations へ同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8917d-113">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

-  <span data-ttu-id="8917d-114">**データ統合でのテンプレートの名前:** プロジェクト時間見積 (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="8917d-114">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>

-  <span data-ttu-id="8917d-115">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="8917d-115">**Name of the tasks in the project:**</span></span> 
    - <span data-ttu-id="8917d-116">トランザクション リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="8917d-116">Transaction relationships</span></span> 
    - <span data-ttu-id="8917d-117">経費見積</span><span class="sxs-lookup"><span data-stu-id="8917d-117">Expense estimates</span></span>

## <a name="entity-set"></a><span data-ttu-id="8917d-118">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="8917d-118">Entity set</span></span>

| <span data-ttu-id="8917d-119">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8917d-119">Project Service Automation</span></span>      | <span data-ttu-id="8917d-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8917d-120">Finance and Operations</span></span>                          |
|---------------------------------|-------------------------------------------------|
| <span data-ttu-id="8917d-121">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="8917d-121">Project tasks</span></span>                   | <span data-ttu-id="8917d-122">プロジェクト時間見積の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="8917d-122">Integration entity for project hour estimates</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="8917d-123">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="8917d-123">Entity flow</span></span>

<span data-ttu-id="8917d-124">プロジェクト時間見積は Project Service Automation で管理され、プロジェクト時間見積として Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="8917d-124">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

## <a name="preconditions"></a><span data-ttu-id="8917d-125">事前条件</span><span class="sxs-lookup"><span data-stu-id="8917d-125">Preconditions</span></span>

<span data-ttu-id="8917d-126">プロジェクト時間見積の同期を行う前に、プロジェクト、プロジェクト タスク、およびプロジェクトの経費トランザクション カテゴリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-126">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="8917d-127">Power Query</span><span class="sxs-lookup"><span data-stu-id="8917d-127">Power Query</span></span>

<span data-ttu-id="8917d-128">プロジェクト時間見積もりテンプレートで Microsoft Power Query を使用して、以下を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-128">You must use Microsoft Power Query in the project hour estimates template to:</span></span>
- <span data-ttu-id="8917d-129">統合が、新しい時間予測を作成するときに使用される**予測モデル ID** を設定します。</span><span class="sxs-lookup"><span data-stu-id="8917d-129">Set the **Forecast model ID** that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="8917d-130">時間予測への統合に失敗するタスク内のリソース特定のレコードを除外します</span><span class="sxs-lookup"><span data-stu-id="8917d-130">Filter out any resource specific records within the task that will fail the integration into hour forecasts</span></span>
- <span data-ttu-id="8917d-131">空のトランザクション カテゴリ行を除外します。</span><span class="sxs-lookup"><span data-stu-id="8917d-131">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="8917d-132">これを行わないと、時間予測が正しくない場合があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-132">Failure to do this may result in incorrect hour forecasts.</span></span>

### <a name="forecast-model-id"></a><span data-ttu-id="8917d-133">予測モデル ID</span><span class="sxs-lookup"><span data-stu-id="8917d-133">Forecast model ID</span></span>
<span data-ttu-id="8917d-134">テンプレートの既定の予測モデル ID を更新するには、**マップ**矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="8917d-134">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="8917d-135">高度なクエリおよびフィルタリングを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="8917d-135">Select to open the Advanced Query and Filtering.</span></span>
- <span data-ttu-id="8917d-136">既定の Microsoft Project 時間見積 (Project Service Automation から Finance and Operations) テンプレートを使用している場合は、**適用されたステップ**セクションで**挿入された条件**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8917d-136">If you are using the default Microsoft Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the **Applied Steps** section.</span></span> <span data-ttu-id="8917d-137">**機能**入力で、**O_forecast** を統合して使用する**予測モデル ID** の名前に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-137">In the **Function** entry, replace **O_forecast** with the name of the **Forecast model ID** that should be used with the integration.</span></span> <span data-ttu-id="8917d-138">既定のテンプレートは、デモ データから予測モデル ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="8917d-138">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="8917d-139">新しいテンプレートを作成する場合は、この列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-139">If you are creating a new template, you must add this column.</span></span> <span data-ttu-id="8917d-140">**条件付き列の追加**を選択し、列に ModelID などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="8917d-140">Select **Add Conditional Column** and give the column a name, such as ModelID.</span></span> <span data-ttu-id="8917d-141">プロジェクト タスクが null でない場合は列の条件を入力し、次に<enter the forecast model ID>を行います。その他 null を表します。</span><span class="sxs-lookup"><span data-stu-id="8917d-141">Enter the condition for the column where if Project task is not null, then<enter the forecast model ID>; else null.</span></span>

### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="8917d-142">リソースの特定のレコードを除外します</span><span class="sxs-lookup"><span data-stu-id="8917d-142">Filter out resource specific records</span></span>
<span data-ttu-id="8917d-143">プロジェクト時間見積 (Project Service Automation から Finance and Operations) テンプレートは、リソースの特定のレコードを削除する既定のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="8917d-143">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource specific records.</span></span> <span data-ttu-id="8917d-144">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-144">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="8917d-145">高度なクエリおよびフィルタリング フォームでは、**msdyn_islinetask** 列にフィルターを選択し **False** レコードのみを含めます。</span><span class="sxs-lookup"><span data-stu-id="8917d-145">In the Advanced Query and Filtering form, select to filter on the column **msdyn_islinetask** to only include **False** records.</span></span>

### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="8917d-146">空のトランザクション カテゴリ行を除外します</span><span class="sxs-lookup"><span data-stu-id="8917d-146">Filter out empty transaction category rows</span></span>
<span data-ttu-id="8917d-147">空のトランザクション カテゴリの行を削除するフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-147">You must add a filter to remove any rows with empty transaction categories.</span></span> <span data-ttu-id="8917d-148">これは、既定のテンプレートを使用している場合でも、独自のテンプレートを作成している場合でも必要です。</span><span class="sxs-lookup"><span data-stu-id="8917d-148">This is needed regardless if you are using the default template or creating your own template.</span></span> <span data-ttu-id="8917d-149">このフィルタは、Project Service Automation からの要約行を削除し、Finance and Operations の時間予測が正しくない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-149">This filter will remove any summary rows coming from Project Service Automation that could cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="8917d-150">高度なクエリおよびフィルタリング フォームで、**msdyn_transactioncategory_value** 列の null レコードを除外するように選択します。</span><span class="sxs-lookup"><span data-stu-id="8917d-150">In the Advanced Query and Filtering form, select to filter out the null records in the column **msdyn_transactioncategory_value**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8917d-151">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="8917d-151">Template mapping in Data integration</span></span>

<span data-ttu-id="8917d-152">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="8917d-152">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="8917d-153">マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="8917d-153">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="8917d-154">[![テンプレートのマッピング](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="8917d-154">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

<span data-ttu-id="8917d-155">次のテンプレートおよび基本的なタスクはプロジェクト経費見積を Project Service Automation から Finance and Operations へ同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8917d-155">The following template and underlying task is used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

-  <span data-ttu-id="8917d-156">**データ統合でのテンプレートの名前:** プロジェクト経費見積 (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="8917d-156">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
-  <span data-ttu-id="8917d-157">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="8917d-157">**Name of the tasks in the project:**</span></span> 
     - <span data-ttu-id="8917d-158">トランザクション リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="8917d-158">Transaction relationships</span></span> 
     - <span data-ttu-id="8917d-159">経費見積</span><span class="sxs-lookup"><span data-stu-id="8917d-159">Expense estimates</span></span>

## <a name="entity-set"></a><span data-ttu-id="8917d-160">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="8917d-160">Entity set</span></span>

| <span data-ttu-id="8917d-161">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8917d-161">Project Service Automation</span></span>      | <span data-ttu-id="8917d-162">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8917d-162">Finance and Operations</span></span>                                     |
|---------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8917d-163">トランザクション接続</span><span class="sxs-lookup"><span data-stu-id="8917d-163">Transaction Connections</span></span>         | <span data-ttu-id="8917d-164">プロジェクト トランザクション リレーションシップの統合エンティティ。</span><span class="sxs-lookup"><span data-stu-id="8917d-164">Integration entity for project transaction relationships.</span></span>   |
| <span data-ttu-id="8917d-165">見積行</span><span class="sxs-lookup"><span data-stu-id="8917d-165">Estimate Lines</span></span>                  | <span data-ttu-id="8917d-166">プロジェクト経費見積の統合エンティティ。</span><span class="sxs-lookup"><span data-stu-id="8917d-166">Integration entity for project expense estimates.</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="8917d-167">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="8917d-167">Entity flow</span></span>

<span data-ttu-id="8917d-168">プロジェクト経費見積は Project Service Automation で管理され、プロジェクト経費見積として Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="8917d-168">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8917d-169">前提条件</span><span class="sxs-lookup"><span data-stu-id="8917d-169">Prerequisites</span></span>

<span data-ttu-id="8917d-170">プロジェクト経費見積の同期を行う前に、プロジェクト、プロジェクト タスクおよびプロジェクト経費トランザクション カテゴリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-170">Before synchronization of project expense estimates can occur, you must synchronize Projects, Project tasks and Project expense transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="8917d-171">Power Query</span><span class="sxs-lookup"><span data-stu-id="8917d-171">Power Query</span></span>

<span data-ttu-id="8917d-172">プロジェクト経費見積テンプレートの Microsoft Power Query を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-172">You must use Microsoft Power Query in the project expense estimates template to:</span></span>
- <span data-ttu-id="8917d-173">経費見積行レコードのみを含めるようにフィルターをする</span><span class="sxs-lookup"><span data-stu-id="8917d-173">Filter to include only expense estimate line records</span></span>
- <span data-ttu-id="8917d-174">統合が、新しい時間予測を作成するときに使用される**予測モデル ID** を設定します。</span><span class="sxs-lookup"><span data-stu-id="8917d-174">Set the **Forecast model ID** that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="8917d-175">請求タイプを変換する。</span><span class="sxs-lookup"><span data-stu-id="8917d-175">Transform the billing types.</span></span>
- <span data-ttu-id="8917d-176">トランザクション タイプを変換する。</span><span class="sxs-lookup"><span data-stu-id="8917d-176">Transform the transaction types.</span></span>

### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="8917d-177">経費見積行のみを含めるようにフィルターをする</span><span class="sxs-lookup"><span data-stu-id="8917d-177">Filter to include only expense estimate lines</span></span>
<span data-ttu-id="8917d-178">プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートには、統合に経費明細行のみを含めるための既定のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="8917d-178">The Project expense estimates (PSA to Fin and Ops) template has a default filter to only include expense lines in the integration.</span></span> <span data-ttu-id="8917d-179">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-179">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="8917d-180">トランザクション リレーションシップのタスクを選択し**マップ**矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8917d-180">Select the Transaction relationships task and click the **Map** arrow.</span></span> <span data-ttu-id="8917d-181">**高度なクエリとフィルター処理**を選択。</span><span class="sxs-lookup"><span data-stu-id="8917d-181">Select **Advanced Query and filtering**.</span></span> <span data-ttu-id="8917d-182">**msdyn_estimateline** のみを含む **msdyn_transactiontype1** 列のフィルター。</span><span class="sxs-lookup"><span data-stu-id="8917d-182">Filter the **msdyn_transactiontype1** column to include only **msdyn_estimateline**.</span></span>

### <a name="forecast-model-id"></a><span data-ttu-id="8917d-183">予測モデル ID</span><span class="sxs-lookup"><span data-stu-id="8917d-183">Forecast model ID</span></span>
<span data-ttu-id="8917d-184">テンプレートの既定の予測モデル ID を更新するには、経費見積タスクで、**マップ**矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="8917d-184">To update the default forecast model ID in the template, for the Expense estimates task, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="8917d-185">高度なクエリおよびフィルタリングを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="8917d-185">Select to open the Advanced Query and Filtering.</span></span>
- <span data-ttu-id="8917d-186">既定の Microsoft Project 経費見積 (Project Service Automation から Finance and Operations) テンプレートを使用している場合は、**適用されたステップ** セクションで最初の**挿入された条件**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8917d-186">If you are using the default Microsoft Project expense estimates (PSA to Fin and Ops) template, select the first **Inserted Condition** in the **Applied Steps** section.</span></span> <span data-ttu-id="8917d-187">**機能**入力で、**O_forecast** を統合して使用する**予測モデル ID** の名前に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-187">In the **Function** entry, replace **O_forecast** with the name of the **Forecast model ID** that should be used with the integration.</span></span> <span data-ttu-id="8917d-188">既定のテンプレートは、デモ データから予測モデル ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="8917d-188">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="8917d-189">新しいテンプレートを作成する場合は、この列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-189">If you are creating a new template, you must add this column.</span></span> <span data-ttu-id="8917d-190">**条件付き列の追加**を選択し、列に ModelID などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="8917d-190">Select **Add Conditional Column** and give the column a name, such as ModelID.</span></span> <span data-ttu-id="8917d-191">見積明細行 ID が null でない場合は、<予測モデル ID を入力> の列の条件を入力します。その他は null を表します。</span><span class="sxs-lookup"><span data-stu-id="8917d-191">Enter the condition for the column where if Estimate line ID is not null, then < enter the forecast model ID >; else null.</span></span>

### <a name="transform-the-billing-types"></a><span data-ttu-id="8917d-192">請求タイプを変換する</span><span class="sxs-lookup"><span data-stu-id="8917d-192">Transform the billing types</span></span>
<span data-ttu-id="8917d-193">プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートは、統合中に Project Service Automation から受け取った請求タイプを変換するための条件付き列が追加されます。</span><span class="sxs-lookup"><span data-stu-id="8917d-193">The Project expense estimates (PSA to Fin and Ops) template has a conditional column added to transform the billing types received from Project Service Automation during the integration.</span></span>
- <span data-ttu-id="8917d-194">独自のテンプレートを作成する場合は、この条件付き列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-194">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="8917d-195">高度なクエリおよびフィルタリング フォームで、**条件付き列の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8917d-195">In the Advanced Query and Filtering form, select **Add Conditional Column**.</span></span> <span data-ttu-id="8917d-196">列に、「BillingType」などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="8917d-196">Give the column a name, such as "BillingType".</span></span> <span data-ttu-id="8917d-197">入力する条件は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8917d-197">The condition to enter is as follows:</span></span>

    <span data-ttu-id="8917d-198">**msdyn_billingtype** = 192350000 の場合は、**NonChargeable** それ以外の場合は **msdyn_billingtype** = 192350001、**Chargeable** ならば **msdyn_billingtype** = 192350002、**Complimentary** 以外は **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="8917d-198">If **msdyn_billingtype** = 192350000, then **NonChargeable** else if **msdyn_billingtype** = 192350001, then **Chargeable** else if **msdyn_billingtype** = 192350002, then **Complimentary** else **NotAvailable**</span></span>

### <a name="transform-the-transaction-types"></a><span data-ttu-id="8917d-199">トランザクション タイプを変換する</span><span class="sxs-lookup"><span data-stu-id="8917d-199">Transform the transaction types</span></span>
<span data-ttu-id="8917d-200">プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートは、統合中に Project Service Automation から受け取ったトランザクション タイプを変換するための条件付き列が追加されます。</span><span class="sxs-lookup"><span data-stu-id="8917d-200">The Project expense estimates (PSA to Fin and Ops) template has a conditional column added to transform the transaction types received from Project Service Automation during the integration.</span></span>
- <span data-ttu-id="8917d-201">独自のテンプレートを作成する場合は、この条件付き列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8917d-201">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="8917d-202">高度なクエリおよびフィルタリング フォームで、**条件付き列の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8917d-202">In the Advanced Query and Filtering form, select **Add Conditional Column**.</span></span> <span data-ttu-id="8917d-203">列に、「TransactionType」などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="8917d-203">Give the column a name, such as "TransactionType".</span></span> <span data-ttu-id="8917d-204">入力する条件は次のとおりです。**msdyn_transactiontypecode** = 192350000 の場合、次に**原価**他に **msdyn_transactiontypecode** = 192350005、それから**販売**他 **null**</span><span class="sxs-lookup"><span data-stu-id="8917d-204">The condition to enter is as follows: If **msdyn_transactiontypecode** = 192350000, then **Cost** else if **msdyn_transactiontypecode** = 192350005, then **Sales** else **null**</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8917d-205">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="8917d-205">Template mapping in Data integration</span></span>

<span data-ttu-id="8917d-206">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="8917d-206">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="8917d-207">マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="8917d-207">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="8917d-208">[![テンプレートのマッピング](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="8917d-208">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="8917d-209">[![テンプレートのマッピング](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="8917d-209">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>




