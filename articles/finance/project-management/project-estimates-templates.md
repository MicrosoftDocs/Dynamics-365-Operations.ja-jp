---
title: プロジェクト見積を Project Service Automation から Finance and Operations に直接同期します
description: このトピックでは、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Finance にプロジェクト時間見積およびプロジェクト経費見積を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770292"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="e45fc-103">プロジェクト見積を Project Service Automation から Finance and Operations に直接同期します</span><span class="sxs-lookup"><span data-stu-id="e45fc-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e45fc-104">このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance にプロジェクト時間見積およびプロジェクト経費見積を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="e45fc-105">プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、バージョン 8.0 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="e45fc-106">実績の統合は、バージョン 8.0.1 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="e45fc-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="e45fc-107">Project Service Automation から Finance のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="e45fc-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="e45fc-108">Project Service Automation の Finance への統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="e45fc-109">データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance へのプロジェクト時間見積およびプロジェクト経費見積に関するデータ フローを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e45fc-110">次の図は、データが Project Service Automation と Finance との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e45fc-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="e45fc-111">[![Project Service Automation と Finance の統合のデータ フロー](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="e45fc-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="e45fc-112">プロジェクト時間見積</span><span class="sxs-lookup"><span data-stu-id="e45fc-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="e45fc-113">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="e45fc-113">Template and tasks</span></span>

<span data-ttu-id="e45fc-114">使用可能なテンプレートにアクセスするには、Microsoft Power Apps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e45fc-115">次のテンプレートおよび基本的なタスクはプロジェクト時間見積を Project Service Automation から Finance へ同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="e45fc-116">**データ統合でのテンプレートの名前:** プロジェクト時間見積 (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="e45fc-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="e45fc-117">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="e45fc-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="e45fc-118">トランザクション リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="e45fc-118">Transaction relationships</span></span>
    - <span data-ttu-id="e45fc-119">経費見積</span><span class="sxs-lookup"><span data-stu-id="e45fc-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="e45fc-120">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="e45fc-120">Entity set</span></span>

| <span data-ttu-id="e45fc-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e45fc-121">Project Service Automation</span></span> | <span data-ttu-id="e45fc-122">財務</span><span class="sxs-lookup"><span data-stu-id="e45fc-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="e45fc-123">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="e45fc-123">Project tasks</span></span>              | <span data-ttu-id="e45fc-124">プロジェクト時間見積の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="e45fc-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="e45fc-125">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="e45fc-125">Entity flow</span></span>

<span data-ttu-id="e45fc-126">プロジェクト時間見積は Project Service Automation で管理され、プロジェクト時間見積として Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e45fc-127">必要条件</span><span class="sxs-lookup"><span data-stu-id="e45fc-127">Prerequisites</span></span>

<span data-ttu-id="e45fc-128">プロジェクト時間見積の同期を行う前に、プロジェクト、プロジェクト タスク、およびプロジェクトの経費トランザクション カテゴリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="e45fc-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="e45fc-129">Power Query</span></span>

<span data-ttu-id="e45fc-130">プロジェクト時間見積テンプレートで、Microsoft Power Query for Excel を使用してこれらのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="e45fc-131">統合が新しい時間予測を作成するときに使用される、既定の予測モデル ID を設定します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="e45fc-132">時間予測への統合に失敗するタスク内のリソース特定のレコードを除外します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="e45fc-133">空のトランザクション カテゴリ行を除外します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="e45fc-134">このタスクを完了しないと、時間予測が正しくない場合があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="e45fc-135">既定の予測モデル ID の設定</span><span class="sxs-lookup"><span data-stu-id="e45fc-135">Set the default forecast model ID</span></span>

<span data-ttu-id="e45fc-136">テンプレートの既定の予測モデル ID を更新するには、**マップ**矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="e45fc-137">次に**高度なクエリおよびフィルタリング**リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="e45fc-138">既定のプロジェクト時間見積 (Project Service Automation から Finance and Operations) テンプレートを使用している場合は、**適用されたステップ**のリストで**挿入された条件**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="e45fc-139">**機能**入力で、**O\_forecast**を統合で使用される予測モデル ID の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="e45fc-140">既定のテンプレートは、デモ データから予測モデル ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="e45fc-141">新しいテンプレートを作成する場合は、この列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="e45fc-142">Power Query で、**条件付き列の追加**を選択し、新しい列に **ModelID** などの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="e45fc-143">プロジェクト タスクが null でない場合は、列の条件を入力し \<予測モデル ID を入力\>します。その他は null を表します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="e45fc-144">リソースの特定のレコードを除外します</span><span class="sxs-lookup"><span data-stu-id="e45fc-144">Filter out resource-specific records</span></span>

<span data-ttu-id="e45fc-145">プロジェクト時間見積 (Project Service Automation から Finance and Operations) テンプレートは、リソースの特定のレコードを削除する既定のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="e45fc-146">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="e45fc-147">**高度なクエリおよびフィルタリング**リンクを選択して、**msdyn\_islinetask** 列をフィルタリングし **False** レコードのみを含めます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="e45fc-148">空のトランザクション カテゴリ行を除外します</span><span class="sxs-lookup"><span data-stu-id="e45fc-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="e45fc-149">空のトランザクション カテゴリがある行を削除するためのフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="e45fc-150">このタスクは、既定のテンプレートを使用している、または独自のテンプレートを作成しているかどうかに関係なく必要です。</span><span class="sxs-lookup"><span data-stu-id="e45fc-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="e45fc-151">このフィルタは、Finance の時間予測が不正確になる可能性がある Project Service Automation からの要約行を削除します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="e45fc-152">**高度なクエリおよびフィルタリング**リンクを選択し、**msdyn\_transactioncategory\_value** 列の null レコードを除外します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e45fc-153">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="e45fc-153">Template mapping in Data integration</span></span>

<span data-ttu-id="e45fc-154">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="e45fc-155">マッピングは、Project Service Automation から Finance に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e45fc-156">[![テンプレートのマッピング](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e45fc-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="e45fc-157">プロジェクト経費見積</span><span class="sxs-lookup"><span data-stu-id="e45fc-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="e45fc-158">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="e45fc-158">Template and tasks</span></span>

<span data-ttu-id="e45fc-159">次のテンプレートおよび基本的なタスクはプロジェクト経費見積を Project Service Automation から Finance へ同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="e45fc-160">**データ統合でのテンプレートの名前:** プロジェクト経費見積 (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="e45fc-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="e45fc-161">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="e45fc-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="e45fc-162">トランザクション リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="e45fc-162">Transaction relationships</span></span> 
    - <span data-ttu-id="e45fc-163">経費見積</span><span class="sxs-lookup"><span data-stu-id="e45fc-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="e45fc-164">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="e45fc-164">Entity set</span></span>

| <span data-ttu-id="e45fc-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e45fc-165">Project Service Automation</span></span> | <span data-ttu-id="e45fc-166">財務</span><span class="sxs-lookup"><span data-stu-id="e45fc-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="e45fc-167">トランザクション接続</span><span class="sxs-lookup"><span data-stu-id="e45fc-167">Transaction Connections</span></span>    | <span data-ttu-id="e45fc-168">プロジェクト トランザクション リレーションシップに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="e45fc-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="e45fc-169">見積行</span><span class="sxs-lookup"><span data-stu-id="e45fc-169">Estimate Lines</span></span>             | <span data-ttu-id="e45fc-170">プロジェクト経費見積に対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="e45fc-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="e45fc-171">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="e45fc-171">Entity flow</span></span>

<span data-ttu-id="e45fc-172">プロジェクト経費見積は Project Service Automation で管理され、プロジェクト経費見積として Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e45fc-173">必要条件</span><span class="sxs-lookup"><span data-stu-id="e45fc-173">Prerequisites</span></span>

<span data-ttu-id="e45fc-174">プロジェクト経費見積の同期を行う前に、プロジェクト、プロジェクト タスクおよびプロジェクト経費トランザクション カテゴリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="e45fc-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="e45fc-175">Power Query</span></span>

<span data-ttu-id="e45fc-176">プロジェクト経費見積テンプレートで、Power Query を使用して以下のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="e45fc-177">経費見積行レコードのみを含めるようにフィルタリングします。</span><span class="sxs-lookup"><span data-stu-id="e45fc-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="e45fc-178">統合が新しい時間予測を作成するときに使用される、既定の予測モデル ID を設定します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="e45fc-179">請求タイプを変換する。</span><span class="sxs-lookup"><span data-stu-id="e45fc-179">Transform the billing types.</span></span>
- <span data-ttu-id="e45fc-180">トランザクション タイプを変換する。</span><span class="sxs-lookup"><span data-stu-id="e45fc-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="e45fc-181">経費見積行のみを含めるようにフィルターをする</span><span class="sxs-lookup"><span data-stu-id="e45fc-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="e45fc-182">プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートには、統合に経費明細行のみを含む既定のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="e45fc-183">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="e45fc-184">**トランザクション リレーションシップ**タスクを選択し、次に**マップ**矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="e45fc-185">**高度なクエリおよびフィルタリング**リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="e45fc-186">**msdyn\_transactiontype1** 列をフィルタリングして、**msdyn\_estimateline** のみを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="e45fc-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="e45fc-187">既定の予測モデル ID の設定</span><span class="sxs-lookup"><span data-stu-id="e45fc-187">Set the default forecast model ID</span></span>

<span data-ttu-id="e45fc-188">テンプレートの既定の予測モデル ID を更新するには、**経費見積**タスクを選択し、**マップ**矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="e45fc-189">**高度なクエリおよびフィルタリング**リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="e45fc-190">既定のプロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートを使用している場合、Power Query で、**適用されたステップ**セクションから最初の**挿入された条件**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="e45fc-191">**機能**入力で、**O\_forecast**を統合で使用される予測モデル ID の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="e45fc-192">既定のテンプレートは、デモ データから予測モデル ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="e45fc-193">新しいテンプレートを作成する場合は、この列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="e45fc-194">Power Query で、**条件付き列の追加**を選択し、新しい列に **ModelID** などの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="e45fc-195">見積明細行 ID が null でない場合は、列の条件を入力し、\<予測モデル ID を入力\>します。その他は null を表します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="e45fc-196">請求タイプを変換する</span><span class="sxs-lookup"><span data-stu-id="e45fc-196">Transform the billing types</span></span>

<span data-ttu-id="e45fc-197">プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートは、統合中に Project Service Automation から受け取った請求タイプを変換するのに使用する条件付き列を含みます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="e45fc-198">独自のテンプレートを作成する場合は、この条件付き列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="e45fc-199">**高度なクエリおよびフィルタリング**リンクを選択し、**条件付き列の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="e45fc-200">新しい列に、**BillingType** などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="e45fc-201">次の条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-201">Then enter the following condition:</span></span>

<span data-ttu-id="e45fc-202">**msdyn\_billingtype** = 192350000 の場合、**NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="e45fc-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="e45fc-203">**msdyn\_billingtype** = 192350001 の場合は、**Chargeable**</span><span class="sxs-lookup"><span data-stu-id="e45fc-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="e45fc-204">**msdyn\_billingtype** = 192350002 の場合は、**Complimentary**</span><span class="sxs-lookup"><span data-stu-id="e45fc-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="e45fc-205">それ以外の場合は **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="e45fc-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="e45fc-206">トランザクション タイプを変換する</span><span class="sxs-lookup"><span data-stu-id="e45fc-206">Transform the transaction types</span></span>

<span data-ttu-id="e45fc-207">プロジェクト経費見積 (Project Service Automation から Finance and Operations) テンプレートは、統合中に Project Service Automation から受け取ったトランザクション タイプを変換するのに使用する条件付き列を含みます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="e45fc-208">独自のテンプレートを作成する場合は、この条件付き列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e45fc-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="e45fc-209">**高度なクエリおよびフィルタリング**リンクを選択し、**条件付き列の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="e45fc-210">新しい列に、**TransactionType** などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="e45fc-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="e45fc-211">次の条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-211">Then enter the following condition:</span></span>

<span data-ttu-id="e45fc-212">**msdyn\_transactiontypecode** = 192350000 の場合、**原価**</span><span class="sxs-lookup"><span data-stu-id="e45fc-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="e45fc-213">**msdyn\_transactiontypecode** = 192350005 の場合は、**販売**</span><span class="sxs-lookup"><span data-stu-id="e45fc-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="e45fc-214">それ以外の場合は **null**</span><span class="sxs-lookup"><span data-stu-id="e45fc-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e45fc-215">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="e45fc-215">Template mapping in Data integration</span></span>

<span data-ttu-id="e45fc-216">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="e45fc-217">マッピングは、Project Service Automation から Finance に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="e45fc-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e45fc-218">[![テンプレートのマッピング](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e45fc-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="e45fc-219">[![テンプレートのマッピング](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e45fc-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
