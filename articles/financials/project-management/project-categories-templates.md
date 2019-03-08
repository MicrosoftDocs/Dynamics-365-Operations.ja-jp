---
title: Finance and Operations および Project Service Automation でプロジェクト経費カテゴリを同期させる
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations および Microsoft Dynamics 365 for Project Service Automation でプロジェクトの経費カテゴリを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "347839"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="59a08-103">Finance and Operations および Project Service Automation でプロジェクト経費カテゴリを同期させる</span><span class="sxs-lookup"><span data-stu-id="59a08-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="59a08-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations および Microsoft Dynamics 365 for Project Service Automation でプロジェクトの経費カテゴリを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="59a08-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="59a08-105">プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="59a08-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="59a08-106">実績の統合は、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0.1 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="59a08-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="59a08-107">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="59a08-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="59a08-108">勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="59a08-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="59a08-109">Project Service Automation および Finance and Operations のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="59a08-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="59a08-110">Project Service Automation および Finance and Operations 統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="59a08-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="59a08-111">データ統合機能で利用できる統合テンプレートを使用すると、Finance and Operations および Project Service Automation 間のプロジェクト経費トランザクションのカテゴリに関するデータ フローが有効になります。</span><span class="sxs-lookup"><span data-stu-id="59a08-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="59a08-112">プロジェクト経費カテゴリが Finance and Operations で習得されている場合、統合フローは最初に Finance and Operations から Project Service Automation になります。</span><span class="sxs-lookup"><span data-stu-id="59a08-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="59a08-113">Project Service Automation から Finance and Operations への同期を通してプロジェクトの経費カテゴリの統合 ID が更新されます。</span><span class="sxs-lookup"><span data-stu-id="59a08-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="59a08-114">プロジェクト経費カテゴリが Project Service Automation で習得されている場合、統合フローは最初に Project Service Automation から Finance and Operations になります。</span><span class="sxs-lookup"><span data-stu-id="59a08-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="59a08-115">プロジェクト カテゴリは Project Service Automation から同期する前に、Finance and Operations で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a08-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="59a08-116">Finance and Operations から Project Service Automation へ同期すると、Project Service Automation から Finance and Operations へ再度戻ります。</span><span class="sxs-lookup"><span data-stu-id="59a08-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="59a08-117">これにより、カテゴリがリンクされていると重複が作成されないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="59a08-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="59a08-118">通常、プロジェクトの経費カテゴリは Finance and Operations で習得されます。</span><span class="sxs-lookup"><span data-stu-id="59a08-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="59a08-119">ただし、Finance and Operations でマスターされていない場合、または Project Service Automation で経費カテゴリが既に作成されている場合は、プロジェクト経費トランザクション カテゴリ (Project Service Automation から Finance and Operations) を使用して最初に同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a08-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="59a08-120">次にプロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation) テンプレートを使用して同期します。</span><span class="sxs-lookup"><span data-stu-id="59a08-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="59a08-121">それから Project Service Automation から Finance and Operations にもう一度同期を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a08-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="59a08-122">Project Service Automation から最初に同期する場合は、同期を実行する前に Finance and Operations で次の要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a08-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="59a08-123">Project Service Automation で設定されるプロジェクト カテゴリに一致する共有カテゴリが存在し、それは**プロジェクト**および**経費**の両方に対して有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a08-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="59a08-124">統合する必要がある Finance and Operations の各法人に対して、次のプロジェクト カテゴリが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a08-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="59a08-125">**プロジェクト カテゴリ**が存在します。</span><span class="sxs-lookup"><span data-stu-id="59a08-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="59a08-126">**経費での使用**が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="59a08-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="59a08-127">**仕訳帳で有効**が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="59a08-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="59a08-128">**トランザクション タイプ**を**経費**に設定します。</span><span class="sxs-lookup"><span data-stu-id="59a08-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="59a08-129">次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="59a08-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="59a08-130">[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="59a08-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="59a08-131">Finance and Operations から Project Service Automation へのプロジェクト経費カテゴリの同期</span><span class="sxs-lookup"><span data-stu-id="59a08-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="59a08-132">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="59a08-132">Template and task</span></span>

<span data-ttu-id="59a08-133">テンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="59a08-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="59a08-134">次のテンプレートおよび基本的なタスクはプロジェクト経費カテゴリを Finance and Operations から Project Service Automation へ同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="59a08-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="59a08-135">**データ統合でのテンプレートの名前:** プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation)</span><span class="sxs-lookup"><span data-stu-id="59a08-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="59a08-136">**プロジェクトのタスクの名前:** Project Service Automation にカテゴリを同期</span><span class="sxs-lookup"><span data-stu-id="59a08-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="59a08-137">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="59a08-137">Entity set</span></span>

| <span data-ttu-id="59a08-138">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="59a08-138">Finance and Operations</span></span>            | <span data-ttu-id="59a08-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="59a08-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="59a08-140">カテゴリに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="59a08-140">Integration entity for categories</span></span> | <span data-ttu-id="59a08-141">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="59a08-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="59a08-142">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="59a08-142">Entity flow</span></span>

<span data-ttu-id="59a08-143">プロジェクト経費カテゴリは Finance and Operations で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。</span><span class="sxs-lookup"><span data-stu-id="59a08-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="59a08-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="59a08-144">Power Query</span></span>

<span data-ttu-id="59a08-145">Project Service Automation から同期する時に、Microsoft Power Query for Excel を使用してトランザクション カテゴリの請求タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a08-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="59a08-146">プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation) テンプレートは、既定の列とマッピングを提供します。</span><span class="sxs-lookup"><span data-stu-id="59a08-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="59a08-147">独自のテンプレートを作成する場合は、Power Query に条件付き列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a08-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="59a08-148">以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="59a08-148">Follow these steps.</span></span>

1. <span data-ttu-id="59a08-149">プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation) テンプレートで、プロジェクト経費カテゴリ タスクのマッピングを開くには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59a08-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="59a08-150">**高度なクエリおよびフィルタリング**リンクをクリックして、Power Query を開きます。</span><span class="sxs-lookup"><span data-stu-id="59a08-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="59a08-151">**条件付き列の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="59a08-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="59a08-152">新しい列に、**BillingType** などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="59a08-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="59a08-153">次の条件を入力します。**CATEGORYID が NULL に等しくない場合は 19235001、それ以外の場合は NULL** です。</span><span class="sxs-lookup"><span data-stu-id="59a08-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="59a08-154">列の **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59a08-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="59a08-155">マッピング ページでこの新しい列をマップしてください。</span><span class="sxs-lookup"><span data-stu-id="59a08-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="59a08-156">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="59a08-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="59a08-157">マッピングは、Finance and Operations から Project Service Automation に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="59a08-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="59a08-158">[![テンプレートのマッピング](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="59a08-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="59a08-159">Project Service Automation から Finance and Operations へのプロジェクト経費カテゴリの同期</span><span class="sxs-lookup"><span data-stu-id="59a08-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="59a08-160">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="59a08-160">Template and task</span></span>

<span data-ttu-id="59a08-161">次のテンプレートおよび基本的なタスクは、プロジェクト経費カテゴリを Project Service Automation から Finance and Operations へ同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="59a08-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="59a08-162">**データ統合でのテンプレートの名前:** プロジェクト経費トランザクション カテゴリ (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="59a08-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="59a08-163">**プロジェクトのタスクの名前:** Finance and Operations にカテゴリを同期</span><span class="sxs-lookup"><span data-stu-id="59a08-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="59a08-164">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="59a08-164">Entity set</span></span>

| <span data-ttu-id="59a08-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="59a08-165">Project Service Automation</span></span> | <span data-ttu-id="59a08-166">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="59a08-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="59a08-167">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="59a08-167">Transaction categories</span></span>     | <span data-ttu-id="59a08-168">カテゴリに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="59a08-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="59a08-169">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="59a08-169">Entity flow</span></span>

<span data-ttu-id="59a08-170">プロジェクト経費カテゴリは Finance and Operations で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。</span><span class="sxs-lookup"><span data-stu-id="59a08-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="59a08-171">Finance and Operations に同期すると、Project Service Automation からの統合 ID により Finance and Operations のプロジェクト カテゴリが更新されます。</span><span class="sxs-lookup"><span data-stu-id="59a08-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="59a08-172">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="59a08-172">Template mapping in Data integration</span></span>

<span data-ttu-id="59a08-173">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="59a08-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="59a08-174">マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="59a08-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="59a08-175">[![テンプレートのマッピング](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="59a08-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
