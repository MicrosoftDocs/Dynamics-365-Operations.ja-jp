---
title: "Project Service Automation からプロジェクトの経費カテゴリを同期する"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations および Dynamics 365 for Project Service Automation のプロジェクト経費カテゴリを同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: ja-jp
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="e6a30-103">Finance and Operations および Project Service Automation でプロジェクト経費カテゴリを同期させる</span><span class="sxs-lookup"><span data-stu-id="e6a30-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="e6a30-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations および Dynamics 365 for Project Service Automation のプロジェクト経費カテゴリを同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e6a30-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="e6a30-105">プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="e6a30-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="e6a30-106">Project Service Automation および Finance and Operations のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="e6a30-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="e6a30-107">Project Service Automation および Finance and Operations 統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="e6a30-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="e6a30-108">データ統合機能で利用できる統合テンプレートを使用すると、Finance and Operations および Project Service Automation 間のプロジェクト経費トランザクションのカテゴリに関するデータ フローが有効になります。</span><span class="sxs-lookup"><span data-stu-id="e6a30-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="e6a30-109">プロジェクト経費カテゴリが Finance and Operations で習得されている場合、統合フローは最初に Finance and Operations から Project Service Automation へ、次に Project Service Automation から Finance and Operations へ同期することにより、プロジェクト経費カテゴリ統合 ID を更新します。</span><span class="sxs-lookup"><span data-stu-id="e6a30-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="e6a30-110">プロジェクト経費カテゴリが Project Service Automation で習得されている場合、統合フローは最初に Project Service Automation から Finance and Operations になります。</span><span class="sxs-lookup"><span data-stu-id="e6a30-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="e6a30-111">プロジェクト カテゴリは Project Service Automation から同期する前に、Finance and Operations で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6a30-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="e6a30-112">Finance and Operations から Project Service Automation へ同期すると、Project Service Automation から Finance and Operations へ再度戻ります。</span><span class="sxs-lookup"><span data-stu-id="e6a30-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="e6a30-113">これにより、カテゴリはリンクされ重複は作成されません。</span><span class="sxs-lookup"><span data-stu-id="e6a30-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="e6a30-114">通常、プロジェクトの経費カテゴリは Finance and Operations で習得されます。</span><span class="sxs-lookup"><span data-stu-id="e6a30-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="e6a30-115">ユーザーの状況と同じでない場合、または既に Project Service Automation で作成された経費カテゴリがある場合は、まずプロジェクト経費トランザクション カテゴリ (PSA から Finance and Operations) を使用して同期し、次にプロジェクト経費トランザクション カテゴリ (Finance and Operations から PSA) を使用して同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6a30-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="e6a30-116">再び Project Service Automation から Finance and Operations に同期を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6a30-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="e6a30-117">Project Service Automation から最初に同期している場合、プロジェクト カテゴリは Finance and Operations および Project Service Automation トランザクション カテゴリと同期させる必要があるプロジェクト カテゴリを**仕訳帳で有効**に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6a30-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="e6a30-118">次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e6a30-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="e6a30-119">[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="e6a30-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="e6a30-120">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="e6a30-120">Templates and tasks</span></span>

<span data-ttu-id="e6a30-121">使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6a30-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e6a30-122">次のテンプレートおよび基本的なタスクはプロジェクト経費カテゴリを Finance and Operations から Project Service Automation へ同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e6a30-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="e6a30-123">**データ統合でのテンプレートの名前:** プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation)</span><span class="sxs-lookup"><span data-stu-id="e6a30-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="e6a30-124">**プロジェクトのタスクの名前:** Project Service Automation にカテゴリを同期</span><span class="sxs-lookup"><span data-stu-id="e6a30-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="e6a30-125">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="e6a30-125">Entity set</span></span>

| <span data-ttu-id="e6a30-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e6a30-126">Finance and Operations</span></span>               | <span data-ttu-id="e6a30-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e6a30-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="e6a30-128">カテゴリに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="e6a30-128">Integration entity for categories</span></span>    | <span data-ttu-id="e6a30-129">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="e6a30-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="e6a30-130">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="e6a30-130">Entity flow</span></span>

<span data-ttu-id="e6a30-131">プロジェクト経費カテゴリは Finance and Operations で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。</span><span class="sxs-lookup"><span data-stu-id="e6a30-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="e6a30-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="e6a30-132">Power Query</span></span>

<span data-ttu-id="e6a30-133">Microsoft Power Query を使用して、Project Service Automation から同期する時に、トランザクション カテゴリの請求タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6a30-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="e6a30-134">プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation) テンプレートは、既定の列と既に提示しているマッピングを持っています。</span><span class="sxs-lookup"><span data-stu-id="e6a30-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="e6a30-135">独自のテンプレートを作成する場合は、Power Query に条件付き列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6a30-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="e6a30-136">プロジェクト経費カテゴリのタスクのマッピング内から高度なクエリおよびフィルタリング フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="e6a30-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="e6a30-137">**条件付き列の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6a30-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="e6a30-138">新しい列に、BillingType などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="e6a30-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="e6a30-139">次の条件を入力します。**CATEGORYID が NULL に等しくない場合は 19235001、それ以外の場合は NULL** です。</span><span class="sxs-lookup"><span data-stu-id="e6a30-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="e6a30-140">列の **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6a30-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="e6a30-141">マッピング ページにこの新しい列をマップしてください。</span><span class="sxs-lookup"><span data-stu-id="e6a30-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="e6a30-142">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="e6a30-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="e6a30-143">マッピングは、Finance and Operations から Project Service Automation に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="e6a30-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="e6a30-144">[![テンプレートのマッピング](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e6a30-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="e6a30-145">次のテンプレートおよび基本的なタスクはプロジェクト経費カテゴリを Project Service Automation から Finance and Operations へ同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e6a30-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="e6a30-146">-**データ統合のテンプレートの名前:** プロジェクト経費トランザクション カテゴリ (Project Service Automation から Finance and Operations) - **プロジェクトのタスクの名前:** Finance and Operations へカテゴリの同期</span><span class="sxs-lookup"><span data-stu-id="e6a30-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="e6a30-147">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="e6a30-147">Entity set</span></span>

| <span data-ttu-id="e6a30-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e6a30-148">Project Service Automation</span></span>      | <span data-ttu-id="e6a30-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e6a30-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="e6a30-150">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="e6a30-150">Transaction categories</span></span>          | <span data-ttu-id="e6a30-151">カテゴリに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="e6a30-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="e6a30-152">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="e6a30-152">Entity flow</span></span>

<span data-ttu-id="e6a30-153">プロジェクト経費カテゴリは Finance and Operations で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。</span><span class="sxs-lookup"><span data-stu-id="e6a30-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="e6a30-154">Finance and Operations に同期すると、Project Service Automation から Finance and Operations プロジェクト カテゴリの統合 ID に更新されます。</span><span class="sxs-lookup"><span data-stu-id="e6a30-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="e6a30-155">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="e6a30-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="e6a30-156">マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="e6a30-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="e6a30-157">[![テンプレートのマッピング](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e6a30-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

