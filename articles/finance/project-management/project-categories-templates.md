---
title: Finance and Operations および Project Service Automation でプロジェクト経費カテゴリを同期させる
description: このトピックでは、Microsoft Dynamics 365 Finance および Dynamics 365 Project Service Automation でプロジェクトの経費カテゴリを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 7b0b3721c3b0755218c834d2bf77ec976be3bdcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770315"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="b0e2c-103">Finance and Operations および Project Service Automation でプロジェクト経費カテゴリを同期させる</span><span class="sxs-lookup"><span data-stu-id="b0e2c-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b0e2c-104">このトピックでは、Dynamics 365 Finance および Dynamics 365 Project Service Automation でプロジェクトの経費カテゴリを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="b0e2c-105">プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、バージョン 8.0 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="b0e2c-106">実績の統合は、バージョン 8.0.1 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="b0e2c-107">Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="b0e2c-108">勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="b0e2c-109">Project Service Automation および Finance のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="b0e2c-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="b0e2c-110">Project Service Automation と Finance の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="b0e2c-111">データ統合機能で利用できる統合テンプレートを使用すると、Finance および Project Service Automation 間のプロジェクト経費トランザクションのカテゴリに関するデータ フローが有効になります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="b0e2c-112">プロジェクト経費カテゴリが Finance で習得されている場合、統合フローは最初に Finance から Project Service Automation になります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="b0e2c-113">Project Service Automation から Finance への同期を通してプロジェクトの経費カテゴリの統合 ID が更新されます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b0e2c-114">プロジェクト経費カテゴリが Project Service Automation で習得されている場合、統合フローは最初に Project Service Automation から Finance になります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="b0e2c-115">プロジェクト カテゴリは Project Service Automation から同期する前に、Finance で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="b0e2c-116">Finance から Project Service Automation へ同期すると、Project Service Automation から Finance へ再度戻ります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="b0e2c-117">これにより、カテゴリがリンクされていると重複が作成されないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="b0e2c-118">通常、プロジェクトの経費カテゴリは Finance で習得されます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="b0e2c-119">ただし、習得されていない場合、または Project Service Automation で経費カテゴリが既に作成されている場合は、プロジェクト経費トランザクション カテゴリ (Project Service Automation から Finance and Operations) テンプレートを使用して最初に同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="b0e2c-120">次にプロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation) テンプレートを使用して同期します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="b0e2c-121">それから Project Service Automation から Finance にもう一度同期を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="b0e2c-122">Project Service Automation から最初に同期する場合は、同期を実行する前に Finance で次の要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="b0e2c-123">Project Service Automation で設定されるプロジェクト カテゴリに一致する共有カテゴリが存在し、それは**プロジェクト**および**経費**の両方に対して有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="b0e2c-124">統合する必要がある Finance の各法人に対して、次のプロジェクト カテゴリが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="b0e2c-125">**プロジェクト カテゴリ**が存在します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="b0e2c-126">**経費での使用**が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="b0e2c-127">**仕訳帳で有効**が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="b0e2c-128">**トランザクション タイプ**を**経費**に設定します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="b0e2c-129">次の図は、データが Project Service Automation と Finance との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="b0e2c-130">[![Project Service Automation と Finance の統合のデータ フロー](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b0e2c-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="b0e2c-131">Finance から Project Service Automation へのプロジェクト経費カテゴリの同期</span><span class="sxs-lookup"><span data-stu-id="b0e2c-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="b0e2c-132">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="b0e2c-132">Template and task</span></span>

<span data-ttu-id="b0e2c-133">テンプレートにアクセスするには、Microsoft Power Apps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b0e2c-134">次のテンプレートおよび基本的なタスクはプロジェクト経費カテゴリを Finance から Project Service Automation へ同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="b0e2c-135">**データ統合でのテンプレートの名前:** プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation)</span><span class="sxs-lookup"><span data-stu-id="b0e2c-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="b0e2c-136">**プロジェクトのタスクの名前:** Project Service Automation にカテゴリを同期</span><span class="sxs-lookup"><span data-stu-id="b0e2c-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="b0e2c-137">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="b0e2c-137">Entity set</span></span>

| <span data-ttu-id="b0e2c-138">財務</span><span class="sxs-lookup"><span data-stu-id="b0e2c-138">Finance</span></span>                           | <span data-ttu-id="b0e2c-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b0e2c-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="b0e2c-140">カテゴリに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="b0e2c-140">Integration entity for categories</span></span> | <span data-ttu-id="b0e2c-141">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="b0e2c-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="b0e2c-142">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="b0e2c-142">Entity flow</span></span>

<span data-ttu-id="b0e2c-143">プロジェクト経費カテゴリは Finance で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="b0e2c-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="b0e2c-144">Power Query</span></span>

<span data-ttu-id="b0e2c-145">Project Service Automation から同期する時に、Microsoft Power Query for Excel を使用してトランザクション カテゴリの請求タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="b0e2c-146">プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation) テンプレートは、既定の列とマッピングを提供します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="b0e2c-147">独自のテンプレートを作成する場合は、Power Query に条件付き列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="b0e2c-148">以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-148">Follow these steps.</span></span>

1. <span data-ttu-id="b0e2c-149">プロジェクト経費トランザクション カテゴリ (Finance and Operations から Project Service Automation) テンプレートで、プロジェクト経費カテゴリ タスクのマッピングを開くには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="b0e2c-150">**高度なクエリおよびフィルタリング**リンクをクリックして、Power Query を開きます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="b0e2c-151">**条件付き列の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="b0e2c-152">新しい列に、**BillingType** などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="b0e2c-153">次の条件を入力します。**CATEGORYID が NULL に等しくない場合は 19235001、それ以外の場合は NULL** です。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="b0e2c-154">列の **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="b0e2c-155">マッピング ページでこの新しい列をマップしてください。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="b0e2c-156">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="b0e2c-157">マッピングは、Finance から Project Service Automation に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="b0e2c-158">[![テンプレートのマッピング](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b0e2c-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="b0e2c-159">Project Service Automation から Finance へのプロジェクト経費カテゴリの同期</span><span class="sxs-lookup"><span data-stu-id="b0e2c-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="b0e2c-160">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="b0e2c-160">Template and task</span></span>

<span data-ttu-id="b0e2c-161">次のテンプレートおよび基本的なタスクはプロジェクト経費カテゴリを Project Service Automation から Finance へ同期するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="b0e2c-162">**データ統合でのテンプレートの名前:** プロジェクト経費トランザクション カテゴリ (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="b0e2c-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="b0e2c-163">**プロジェクトのタスクの名前:** Finance and Operations にカテゴリを同期</span><span class="sxs-lookup"><span data-stu-id="b0e2c-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="b0e2c-164">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="b0e2c-164">Entity set</span></span>

| <span data-ttu-id="b0e2c-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b0e2c-165">Project Service Automation</span></span> | <span data-ttu-id="b0e2c-166">財務</span><span class="sxs-lookup"><span data-stu-id="b0e2c-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="b0e2c-167">トランザクション カテゴリ</span><span class="sxs-lookup"><span data-stu-id="b0e2c-167">Transaction categories</span></span>     | <span data-ttu-id="b0e2c-168">カテゴリに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="b0e2c-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="b0e2c-169">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="b0e2c-169">Entity flow</span></span>

<span data-ttu-id="b0e2c-170">プロジェクト経費カテゴリは Finance で管理され、トランザクション カテゴリとして Project Service Automation に同期されます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="b0e2c-171">Finance に同期すると、Project Service Automation からの統合 ID により Finance のプロジェクト カテゴリが更新されます。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b0e2c-172">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="b0e2c-172">Template mapping in Data integration</span></span>

<span data-ttu-id="b0e2c-173">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="b0e2c-174">マッピングは、Project Service Automation から Finance に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="b0e2c-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b0e2c-175">[![テンプレートのマッピング](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b0e2c-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
