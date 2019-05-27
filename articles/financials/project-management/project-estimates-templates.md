---
title: プロジェクト見積を Project Service Automation から Finance and Operations に直接同期します
description: このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations にプロジェクト時間見積およびプロジェクト経費見積を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556555"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a6ba2-103">プロジェクト見積を Project Service Automation から Finance and Operations に直接同期します</span><span class="sxs-lookup"><span data-stu-id="a6ba2-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a6ba2-104">このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations にプロジェクト時間見積およびプロジェクト経費見積を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="a6ba2-105">プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="a6ba2-106">実績の統合は、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0.1 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="a6ba2-107">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="a6ba2-108">勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a6ba2-109">Project Service Automation から Finance and Operations のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="a6ba2-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="a6ba2-110">Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="a6ba2-111">データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト時間見積およびプロジェクト経費見積に関するデータ フローを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-111">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="a6ba2-112">次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="a6ba2-113">[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a6ba2-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="a6ba2-114">プロジェクト時間見積</span><span class="sxs-lookup"><span data-stu-id="a6ba2-114">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="a6ba2-115">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="a6ba2-115">Template and tasks</span></span>

<span data-ttu-id="a6ba2-116">使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-116">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a6ba2-117">次のテンプレートおよび基本的なタスクはプロジェクト時間見積を Project Service Automation から Finance and Operations へ同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-117">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="a6ba2-118">**データ統合でのテンプレートの名前:** プロジェクト時間見積 (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a6ba2-118">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a6ba2-119">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="a6ba2-119">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="a6ba2-120">トランザクション リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="a6ba2-120">Transaction relationships</span></span>
    - <span data-ttu-id="a6ba2-121">経費見積</span><span class="sxs-lookup"><span data-stu-id="a6ba2-121">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="a6ba2-122">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="a6ba2-122">Entity set</span></span>

| <span data-ttu-id="a6ba2-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a6ba2-123">Project Service Automation</span></span> | <span data-ttu-id="a6ba2-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6ba2-124">Finance and Operations</span></span>                        |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="a6ba2-125">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="a6ba2-125">Project tasks</span></span>              | <span data-ttu-id="a6ba2-126">プロジェクト時間見積の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="a6ba2-126">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="a6ba2-127">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="a6ba2-127">Entity flow</span></span>

<span data-ttu-id="a6ba2-128">プロジェクト時間見積は Project Service Automation で管理され、プロジェクト時間見積として Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-128">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a6ba2-129">前提条件</span><span class="sxs-lookup"><span data-stu-id="a6ba2-129">Prerequisites</span></span>

<span data-ttu-id="a6ba2-130">プロジェクト時間見積の同期を行う前に、プロジェクト、プロジェクト タスク、およびプロジェクトの経費トランザクション カテゴリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-130">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a6ba2-131">Power Query</span><span class="sxs-lookup"><span data-stu-id="a6ba2-131">Power Query</span></span>

<span data-ttu-id="a6ba2-132">プロジェクト時間見積テンプレートで、Microsoft Power Query for Excel を使用してこれらのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-132">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="a6ba2-133">統合が新しい時間予測を作成するときに使用される、既定の予測モデル ID を設定します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-133">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="a6ba2-134">時間予測への統合に失敗するタスク内のリソース特定のレコードを除外します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-134">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="a6ba2-135">空のトランザクション カテゴリ行を除外します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-135">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="a6ba2-136">このタスクを完了しないと、時間予測が正しくない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-136">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="a6ba2-137">既定の予測モデル ID の設定</span><span class="sxs-lookup"><span data-stu-id="a6ba2-137">Set the default forecast model ID</span></span>

<span data-ttu-id="a6ba2-138">テンプレートの既定の予測モデル ID を更新するには、**マップ**矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-138">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a6ba2-139">次に**高度なクエリおよびフィルタリング**リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-139">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="a6ba2-140">既定のプロジェクト時間見積 (Project Service Automation から Finance and Operations) テンプレートを使用している場合は、**適用されたステップ**のリストで**挿入された条件**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-140">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="a6ba2-141">**機能**入力で、**O\_forecast**を統合で使用される予測モデル ID の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-141">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="a6ba2-142">既定のテンプレートは、デモ データから予測モデル ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-142">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="a6ba2-143">新しいテンプレートを作成する場合は、この列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-143">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="a6ba2-144">Power Query で、**条件付き列の追加**を選択し、新しい列に **ModelID** などの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-144">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="a6ba2-145">プロジェクト タスクが null でない場合は、列の条件を入力し \<予測モデル ID を入力\>します。その他は null を表します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-145">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="a6ba2-146">リソースの特定のレコードを除外します</span><span class="sxs-lookup"><span data-stu-id="a6ba2-146">Filter out resource-specific records</span></span>

<span data-ttu-id="a6ba2-147">プロジェクト時間見積 (Project Service Automation から Finance and Operations) テンプレートは、リソースの特定のレコードを削除する既定のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-147">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="a6ba2-148">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-148">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="a6ba2-149">**高度なクエリおよびフィルタリング**リンクを選択して、**msdyn\_islinetask** 列をフィルタリングし **False** レコードのみを含めます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-149">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="a6ba2-150">空のトランザクション カテゴリ行を除外します</span><span class="sxs-lookup"><span data-stu-id="a6ba2-150">Filter out empty transaction category rows</span></span>

<span data-ttu-id="a6ba2-151">空のトランザクション カテゴリがある行を削除するためのフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-151">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="a6ba2-152">このタスクは、既定のテンプレートを使用している、または独自のテンプレートを作成しているかどうかに関係なく必要です。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-152">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="a6ba2-153">このフィルタは、Project Service Automation からの要約行を削除し、Finance and Operations の時間予測が正しくない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-153">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="a6ba2-154">**高度なクエリおよびフィルタリング**リンクを選択し、**msdyn\_transactioncategory\_value** 列の null レコードを除外します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-154">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a6ba2-155">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="a6ba2-155">Template mapping in Data integration</span></span>

<span data-ttu-id="a6ba2-156">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="a6ba2-157">マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-157">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="a6ba2-158">[![テンプレートのマッピング](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a6ba2-158">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="a6ba2-159">プロジェクト経費見積</span><span class="sxs-lookup"><span data-stu-id="a6ba2-159">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="a6ba2-160">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="a6ba2-160">Template and tasks</span></span>

<span data-ttu-id="a6ba2-161">次のテンプレートおよび基本的なタスクはプロジェクト経費見積を Project Service Automation から Finance and Operations へ同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-161">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="a6ba2-162">**データ統合でのテンプレートの名前:** プロジェクト経費見積 (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a6ba2-162">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a6ba2-163">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="a6ba2-163">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="a6ba2-164">トランザクション リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="a6ba2-164">Transaction relationships</span></span> 
    - <span data-ttu-id="a6ba2-165">経費見積</span><span class="sxs-lookup"><span data-stu-id="a6ba2-165">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="a6ba2-166">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="a6ba2-166">Entity set</span></span>

| <span data-ttu-id="a6ba2-167">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a6ba2-167">Project Service Automation</span></span> | <span data-ttu-id="a6ba2-168">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6ba2-168">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="a6ba2-169">トランザクション接続</span><span class="sxs-lookup"><span data-stu-id="a6ba2-169">Transaction Connections</span></span>    | <span data-ttu-id="a6ba2-170">プロジェクト トランザクション リレーションシップに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="a6ba2-170">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="a6ba2-171">見積行</span><span class="sxs-lookup"><span data-stu-id="a6ba2-171">Estimate Lines</span></span>             | <span data-ttu-id="a6ba2-172">プロジェクト経費見積に対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="a6ba2-172">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="a6ba2-173">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="a6ba2-173">Entity flow</span></span>

<span data-ttu-id="a6ba2-174">プロジェクト経費見積は Project Service Automation で管理され、プロジェクト経費見積として Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-174">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a6ba2-175">前提条件</span><span class="sxs-lookup"><span data-stu-id="a6ba2-175">Prerequisites</span></span>

<span data-ttu-id="a6ba2-176">プロジェクト経費見積の同期を行う前に、プロジェクト、プロジェクト タスクおよびプロジェクト経費トランザクション カテゴリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-176">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a6ba2-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="a6ba2-177">Power Query</span></span>

<span data-ttu-id="a6ba2-178">プロジェクト経費見積テンプレートで、Power Query を使用して以下のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-178">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="a6ba2-179">経費見積行レコードのみを含めるようにフィルタリングします。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-179">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="a6ba2-180">統合が新しい時間予測を作成するときに使用される、既定の予測モデル ID を設定します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-180">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="a6ba2-181">請求タイプを変換する。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-181">Transform the billing types.</span></span>
- <span data-ttu-id="a6ba2-182">トランザクション タイプを変換する。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-182">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="a6ba2-183">経費見積行のみを含めるようにフィルターをする</span><span class="sxs-lookup"><span data-stu-id="a6ba2-183">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="a6ba2-184">プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートには、統合に経費明細行のみを含む既定のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-184">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="a6ba2-185">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-185">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="a6ba2-186">**トランザクション リレーションシップ**タスクを選択し、次に**マップ**矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-186">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a6ba2-187">**高度なクエリおよびフィルタリング**リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-187">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="a6ba2-188">**msdyn\_transactiontype1** 列をフィルタリングして、**msdyn\_estimateline** のみを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-188">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="a6ba2-189">既定の予測モデル ID の設定</span><span class="sxs-lookup"><span data-stu-id="a6ba2-189">Set the default forecast model ID</span></span>

<span data-ttu-id="a6ba2-190">テンプレートの既定の予測モデル ID を更新するには、**経費見積**タスクを選択し、**マップ**矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-190">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a6ba2-191">**高度なクエリおよびフィルタリング**リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-191">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="a6ba2-192">既定のプロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートを使用している場合、Power Query で、**適用されたステップ**セクションから最初の**挿入された条件**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-192">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="a6ba2-193">**機能**入力で、**O\_forecast**を統合で使用される予測モデル ID の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-193">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="a6ba2-194">既定のテンプレートは、デモ データから予測モデル ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-194">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="a6ba2-195">新しいテンプレートを作成する場合は、この列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-195">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="a6ba2-196">Power Query で、**条件付き列の追加**を選択し、新しい列に **ModelID** などの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-196">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="a6ba2-197">見積明細行 ID が null でない場合は、列の条件を入力し、\<予測モデル ID を入力\>します。その他は null を表します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-197">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="a6ba2-198">請求タイプを変換する</span><span class="sxs-lookup"><span data-stu-id="a6ba2-198">Transform the billing types</span></span>

<span data-ttu-id="a6ba2-199">プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートは、統合中に Project Service Automation から受け取った請求タイプを変換するのに使用する条件付き列を含みます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-199">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="a6ba2-200">独自のテンプレートを作成する場合は、この条件付き列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-200">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="a6ba2-201">**高度なクエリおよびフィルタリング**リンクを選択し、**条件付き列の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-201">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="a6ba2-202">新しい列に、**BillingType** などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-202">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="a6ba2-203">次の条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-203">Then enter the following condition:</span></span>

<span data-ttu-id="a6ba2-204">**msdyn\_billingtype** = 192350000 の場合、**NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="a6ba2-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="a6ba2-205">**msdyn\_billingtype** = 192350001 の場合は、**Chargeable**</span><span class="sxs-lookup"><span data-stu-id="a6ba2-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="a6ba2-206">**msdyn\_billingtype** = 192350002 の場合は、**Complimentary**</span><span class="sxs-lookup"><span data-stu-id="a6ba2-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="a6ba2-207">それ以外の場合は **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="a6ba2-207">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="a6ba2-208">トランザクション タイプを変換する</span><span class="sxs-lookup"><span data-stu-id="a6ba2-208">Transform the transaction types</span></span>

<span data-ttu-id="a6ba2-209">プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートは、統合中に Project Service Automation から受け取ったトランザクション タイプを変換するのに使用する条件付き列を含みます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-209">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="a6ba2-210">独自のテンプレートを作成する場合は、この条件付き列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-210">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="a6ba2-211">**高度なクエリおよびフィルタリング**リンクを選択し、**条件付き列の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-211">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="a6ba2-212">新しい列に、**TransactionType** などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-212">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="a6ba2-213">次の条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-213">Then enter the following condition:</span></span>

<span data-ttu-id="a6ba2-214">**msdyn\_transactiontypecode** = 192350000 の場合、**原価**</span><span class="sxs-lookup"><span data-stu-id="a6ba2-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="a6ba2-215">**msdyn\_transactiontypecode** = 192350005 の場合は、**販売**</span><span class="sxs-lookup"><span data-stu-id="a6ba2-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="a6ba2-216">それ以外の場合は **null**</span><span class="sxs-lookup"><span data-stu-id="a6ba2-216">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a6ba2-217">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="a6ba2-217">Template mapping in Data integration</span></span>

<span data-ttu-id="a6ba2-218">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-218">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="a6ba2-219">マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="a6ba2-219">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="a6ba2-220">[![テンプレートのマッピング](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a6ba2-220">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="a6ba2-221">[![テンプレートのマッピング](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a6ba2-221">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
