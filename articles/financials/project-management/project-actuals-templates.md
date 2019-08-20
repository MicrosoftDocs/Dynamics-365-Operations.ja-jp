---
title: プロジェクト実績を、Project Service Automation から Finance and Operations へ転記する統合仕訳帳に、直接同期させます。
description: このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations にプロジェクト実績を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。
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
ms.openlocfilehash: 3b6427d7eede8fe35fcd86928c3d5b8507876e2e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846078"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a><span data-ttu-id="94b15-103">プロジェクト実績を、Project Service Automation から Finance and Operations へ転記する統合仕訳帳に、直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="94b15-103">Synchronize project actuals directly from Project Service Automation to the project integration journal for posting in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="94b15-104">このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations にプロジェクト実績を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="94b15-104">This topic describes the templates and underlying tasks that are used to synchronize project actuals directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="94b15-105">テンプレートは、Project Service Automation から Finance and Operations のステージング テーブルへ、トランザクションを同期します。</span><span class="sxs-lookup"><span data-stu-id="94b15-105">The template synchronizes transactions from Project Service Automation into a staging table in Finance and Operations.</span></span> <span data-ttu-id="94b15-106">同期が完了した後、ステージング テーブルから統合仕訳帳にデータをインポートするよう**指定する**必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b15-106">After synchronization is completed, you **must** import the data from the staging table into the integration journal.</span></span>

> [!NOTE]
> - <span data-ttu-id="94b15-107">プロジェクト実績の統合は、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0.1 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="94b15-107">Project actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="94b15-108">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="94b15-108">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="94b15-109">勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="94b15-109">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="94b15-110">Finance and Operations 7.3.0 を使用し、Project Service Automation から手数料トランザクションを挿入する場合は、プロジェクト請求書にそれらの手数料を含めるために KB 4345320 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b15-110">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="94b15-111">Project Service Automation で時間や経費のトランザクションに対する消費税金額を入力する場合は、Project Service Automation 更新プログラム 7 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b15-111">If you're entering sales tax amounts on time or expense transactions in Project Service Automation, you must install Project Service Automation Update 7.</span></span> <span data-ttu-id="94b15-112">それ以外の場合は、税の実績は関連付けられている時間または経費の実績にリンクされず、Finance and Operations に同期されません。</span><span class="sxs-lookup"><span data-stu-id="94b15-112">Otherwise, the tax actuals won't be linked to the associated time or expense actuals, and they won't be synchronized to Finance and Operations.</span></span> <span data-ttu-id="94b15-113">詳細については、サポートにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="94b15-113">For more information, contact Support.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="94b15-114">Project Service Automation から Finance and Operations のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="94b15-114">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="94b15-115">Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="94b15-115">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="94b15-116">データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト実績に関するデータ フローを有効にします。</span><span class="sxs-lookup"><span data-stu-id="94b15-116">The integration templates that are available with the Data integration feature enable the flow of data about project actuals from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="94b15-117">次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="94b15-117">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="94b15-118">[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span><span class="sxs-lookup"><span data-stu-id="94b15-118">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span></span>

## <a name="project-actuals-from-project-service-automation"></a><span data-ttu-id="94b15-119">Project Service Automation からのプロジェクト実績</span><span class="sxs-lookup"><span data-stu-id="94b15-119">Project actuals from Project Service Automation</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="94b15-120">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="94b15-120">Template and tasks</span></span>

<span data-ttu-id="94b15-121">使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="94b15-121">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="94b15-122">次のテンプレートおよび基本的なタスクは、Project Service Automation から Finance and Operations プロジェクト実績を同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="94b15-122">The following template and underlying tasks are used to synchronize project actuals from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="94b15-123">**データ統合でのテンプレートの名前:** プロジェクト実績 (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="94b15-123">**Name of the template in Data integration:** Project actuals (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="94b15-124">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="94b15-124">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="94b15-125">実績</span><span class="sxs-lookup"><span data-stu-id="94b15-125">Actuals</span></span>
    - <span data-ttu-id="94b15-126">トランザクション接続</span><span class="sxs-lookup"><span data-stu-id="94b15-126">TransactionConnections</span></span>

### <a name="entity-set"></a><span data-ttu-id="94b15-127">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="94b15-127">Entity set</span></span>

| <span data-ttu-id="94b15-128">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="94b15-128">Project Service Automation</span></span> | <span data-ttu-id="94b15-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="94b15-129">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="94b15-130">実績</span><span class="sxs-lookup"><span data-stu-id="94b15-130">Actuals</span></span>                    | <span data-ttu-id="94b15-131">プロジェクト実績の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="94b15-131">Integration entity for project actuals</span></span>                   |
| <span data-ttu-id="94b15-132">トランザクション接続</span><span class="sxs-lookup"><span data-stu-id="94b15-132">Transaction Connections</span></span>    | <span data-ttu-id="94b15-133">プロジェクト トランザクション リレーションシップに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="94b15-133">Integration entity for project transaction relationships</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="94b15-134">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="94b15-134">Entity flow</span></span>

<span data-ttu-id="94b15-135">プロジェクト実績は Project Service Automation で管理され、Finance and Operations のプロジェクトの統合仕訳帳に同期されます。</span><span class="sxs-lookup"><span data-stu-id="94b15-135">Project actuals are managed in Project Service Automation, and they are synchronized to the project integration journal in Finance and Operations.</span></span> <span data-ttu-id="94b15-136">既定の財務分析コードと転記設定に基づいて、会計が適用されます。</span><span class="sxs-lookup"><span data-stu-id="94b15-136">The accounting will be applied based on default financial dimensions and the posting setup.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="94b15-137">前提条件</span><span class="sxs-lookup"><span data-stu-id="94b15-137">Prerequisites</span></span>

<span data-ttu-id="94b15-138">実績の同期を行う前に、Project Service Automation 統合パラメーターを設定し、プロジェクト、プロジェクト タスク、およびプロジェクトの経費トランザクションのカテゴリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b15-138">Before synchronization of actuals can occur, you must configure the Project Service Automation integration parameters and synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="94b15-139">Power Query</span><span class="sxs-lookup"><span data-stu-id="94b15-139">Power Query</span></span>

<span data-ttu-id="94b15-140">プロジェクト実績テンプレートで、Microsoft Power Query for Excel を使用してこれらのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b15-140">In the project actuals template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="94b15-141">Project Service Automation のトランザクション タイプを、Finance and Operations の正しいトランザクション タイプに変換します。</span><span class="sxs-lookup"><span data-stu-id="94b15-141">Transform the transaction type in Project Service Automation to the correct transaction type in Finance and Operations.</span></span> <span data-ttu-id="94b15-142">プロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートでは、既にこの変換を定義しています。</span><span class="sxs-lookup"><span data-stu-id="94b15-142">This transformation is already defined in the Project actuals (PSA to Fin and Ops) template.</span></span>
- <span data-ttu-id="94b15-143">Project Service Automation の請求タイプを、Finance and Operations の正しい請求タイプに変換します。</span><span class="sxs-lookup"><span data-stu-id="94b15-143">Transform the billing type in Project Service Automation to the correct billing type in Finance and Operations.</span></span> <span data-ttu-id="94b15-144">プロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートでは、既にこの変換を定義しています。</span><span class="sxs-lookup"><span data-stu-id="94b15-144">This transformation is already defined in the Project actuals (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="94b15-145">すると、請求タイプは **Project Service Automation の統合パラメーター**ページのコンフィギュレーションに基づいて、明細行プロパティにマップされます。</span><span class="sxs-lookup"><span data-stu-id="94b15-145">The billing type is then mapped to the line property, based on the configuration on the **Project Service Automation integration parameters** page.</span></span>
- <span data-ttu-id="94b15-146">このテンプレートと同期する必要のある、特定の組織単位のリソースにフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="94b15-146">Filter to specific resource organizational units that must be synchronized with this template.</span></span>
- <span data-ttu-id="94b15-147">会社間時間または会社間経費の実績を Finance and Operations に同期させると、Finance and Operations で契約組織単位を、正しい法人に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b15-147">If intercompany time or intercompany expense actuals will be synchronized to Finance and Operations, you must transform the contract organizational unit to the correct legal entity in Finance and Operations.</span></span> <span data-ttu-id="94b15-148">プロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートでは、条件付き列がデモ データに基づいて定義されます。</span><span class="sxs-lookup"><span data-stu-id="94b15-148">In the Project actuals (PSA to Fin and Ops) template, a conditional column is defined based on demo data.</span></span> <span data-ttu-id="94b15-149">正しい法人に最後に挿入された条件付き列を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b15-149">You must update the last inserted conditional column to the correct legal entities.</span></span> <span data-ttu-id="94b15-150">それ以外の場合は、統合エラーが発生し、あるいは無効な実績トランザクションが Finance and Operations にインポートされることがあります。</span><span class="sxs-lookup"><span data-stu-id="94b15-150">Otherwise, either an integration error might occur, or incorrect actual transactions might be imported into Finance and Operations.</span></span>
- <span data-ttu-id="94b15-151">会社間時間または会社間経費の実績が Finance and operations と同期されない場合、最後に挿入した条件付き列をテンプレートから削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b15-151">If intercompany time or intercompany expense actuals won't be synchronized to Finance and operations, you must delete the last inserted conditional column from your template.</span></span> <span data-ttu-id="94b15-152">それ以外の場合は、統合エラーが発生し、あるいは無効な実績トランザクションが Finance and Operations にインポートされることがあります。</span><span class="sxs-lookup"><span data-stu-id="94b15-152">Otherwise, either an integration error might occur, or incorrect actual transactions might be imported into Finance and Operations.</span></span>

#### <a name="contract-organizational-unit"></a><span data-ttu-id="94b15-153">契約組織単位</span><span class="sxs-lookup"><span data-stu-id="94b15-153">Contract organizational unit</span></span>
<span data-ttu-id="94b15-154">テンプレートの挿入された条件付き列を更新するには、**マップ**矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="94b15-154">To update the inserted conditional column in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="94b15-155">**高度なクエリおよびフィルタリング**リンクを選択して Power Query を開きます。</span><span class="sxs-lookup"><span data-stu-id="94b15-155">Select the **Advanced Query and Filtering** link to open Power Query.</span></span>

- <span data-ttu-id="94b15-156">既定のプロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートを使用している場合、Power Query で、**適用されたステップ**セクションから最後の**挿入された条件**を選択します。</span><span class="sxs-lookup"><span data-stu-id="94b15-156">If you're using the default Project actuals (PSA to Fin and Ops) template, in Power Query, select the last **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="94b15-157">**機能**入力で、**USSI** を統合で使用する必要がある法人の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="94b15-157">In the **Function** entry, replace **USSI** with the name of the legal entity that should be used with the integration.</span></span> <span data-ttu-id="94b15-158">必要に応じて**関数**入力に追加条件を追加し、**USMF** から正しい法人へ**他の**条件を更新します。</span><span class="sxs-lookup"><span data-stu-id="94b15-158">Add additional conditions to the **Function** entry as you require, and update the **else** condition from **USMF** to the correct legal entity.</span></span>
- <span data-ttu-id="94b15-159">新しいテンプレートを作成する場合、会社間時間および会社間経費をサポートするために列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b15-159">If you're creating a new template, you must add the column to support intercompany time and expenses.</span></span> <span data-ttu-id="94b15-160">**条件付き列の追加**を選択し、列に **LegalEntity** などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="94b15-160">Select **Add Conditional Column**, and enter a name for the column, such as **LegalEntity**.</span></span> <span data-ttu-id="94b15-161">**msdyn\_contractorganizationalunitid.msdyn\_name** が \<組織単位\>である場合は列の条件を入力してから、 \<法人を入力\>します。その他 null を表します。</span><span class="sxs-lookup"><span data-stu-id="94b15-161">Enter a condition for the column, where, if **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, then \<enter the legal entity\>; else null.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="94b15-162">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="94b15-162">Template mapping in Data integration</span></span>

<span data-ttu-id="94b15-163">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="94b15-163">The following illustrations show an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="94b15-164">マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="94b15-164">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="94b15-165">[![テンプレートのマッピング](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="94b15-165">[![Template mapping](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span></span>

<span data-ttu-id="94b15-166">[![テンプレートのマッピング](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span><span class="sxs-lookup"><span data-stu-id="94b15-166">[![Template mapping](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span></span>

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a><span data-ttu-id="94b15-167">Project Service Automation から統合後のステージング テーブルからのインポート</span><span class="sxs-lookup"><span data-stu-id="94b15-167">Import from staging table after integration from Project Service Automation</span></span>

<span data-ttu-id="94b15-168">ステージング テーブルの定期処理からのインポートは、Project Service Automation から Finance and Operations への実績の同期後に実行される必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b15-168">The Import from staging table periodic process must be run after the synchronization of actuals from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="94b15-169">この処理では、プロジェクト トランザクションがステージング テーブルから Project Service Automation 統合仕訳帳にインポートされ、会計が適用され、インポートされたトランザクションが転記されます。</span><span class="sxs-lookup"><span data-stu-id="94b15-169">This process will import the project transactions from the staging table into the Project Service Automation integration journal, where the accounting is applied and the imported transactions can be posted.</span></span> <span data-ttu-id="94b15-170">この処理はバッチ モードで実行し、必要に応じて繰り返し実行されるバッチとして設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="94b15-170">We recommend that you run this process in batch mode and optionally can be set up to run as a recurring batch.</span></span>

## <a name="update-actuals-from-finance-and-operations"></a><span data-ttu-id="94b15-171">Finance and Operations からの実績の更新</span><span class="sxs-lookup"><span data-stu-id="94b15-171">Update actuals from Finance and Operations</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="94b15-172">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="94b15-172">Template and tasks</span></span>

<span data-ttu-id="94b15-173">次のテンプレートおよび基本的なタスクは Finance and Operations から Project Service Automation へ伝票番号とプロジェクト実績に転記した消費税を同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="94b15-173">The following template and underlying tasks are used to synchronize the voucher number and sales taxes for posted project transactions from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="94b15-174">**データ統合でのテンプレートの名前:** プロジェクト実績の更新 (Finance and Operations から Project Service Automation)</span><span class="sxs-lookup"><span data-stu-id="94b15-174">**Name of the template in Data integration:** Project actuals update (Fin Ops to PSA)</span></span>
- <span data-ttu-id="94b15-175">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="94b15-175">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="94b15-176">実績</span><span class="sxs-lookup"><span data-stu-id="94b15-176">Actuals</span></span> 
    - <span data-ttu-id="94b15-177">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="94b15-177">TransactionConnections</span></span>

### <a name="entity-set"></a><span data-ttu-id="94b15-178">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="94b15-178">Entity set</span></span>

| <span data-ttu-id="94b15-179">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="94b15-179">Finance and Operations</span></span>                                   | <span data-ttu-id="94b15-180">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="94b15-180">Project Service Automation</span></span> |
|----------------------------------------------------------|----------------------------|
| <span data-ttu-id="94b15-181">プロジェクト実績の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="94b15-181">Integration entity for project actuals</span></span>                   | <span data-ttu-id="94b15-182">実績</span><span class="sxs-lookup"><span data-stu-id="94b15-182">Actuals</span></span>                    |
| <span data-ttu-id="94b15-183">プロジェクト トランザクション リレーションシップに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="94b15-183">Integration entity for project transaction relationships</span></span> | <span data-ttu-id="94b15-184">Transaction Connections</span><span class="sxs-lookup"><span data-stu-id="94b15-184">Transaction Connections</span></span>    |

### <a name="entity-flow"></a><span data-ttu-id="94b15-185">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="94b15-185">Entity flow</span></span>

<span data-ttu-id="94b15-186">プロジェクト実績は Project Service Automation で管理され、Finance and Operations のプロジェクトの統合仕訳帳に同期されます。</span><span class="sxs-lookup"><span data-stu-id="94b15-186">Project actuals are managed in Project Service Automation, and they are synchronized to the project integration journal in Finance and Operations.</span></span> <span data-ttu-id="94b15-187">Finance and Operations に実績が転記された後、Finance and Operations からの伝票番号によって、Project Service Automation で更新されます。</span><span class="sxs-lookup"><span data-stu-id="94b15-187">After actuals are posted in Finance and Operations, they are updated in Project Service Automation with the voucher number from Finance and Operations.</span></span> <span data-ttu-id="94b15-188">Finance and Operations で消費税が追加された場合、Project Service Automation で新しい税実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="94b15-188">If sales taxes were added in Finance and Operations, new tax actuals are created in Project Service Automation.</span></span>

### <a name="power-query"></a><span data-ttu-id="94b15-189">Power Query</span><span class="sxs-lookup"><span data-stu-id="94b15-189">Power Query</span></span>

<span data-ttu-id="94b15-190">プロジェクト実績更新テンプレートで、Power Query を使用してこれらのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94b15-190">In the project actuals update template, you must use Power Query to complete these tasks:</span></span>

- <span data-ttu-id="94b15-191">Finance and Operations のトランザクション タイプを、Project Service Automation の正しいトランザクション タイプに変換します。</span><span class="sxs-lookup"><span data-stu-id="94b15-191">Transform the transaction type in Finance and Operations to the correct transaction type in Project Service Automation.</span></span> <span data-ttu-id="94b15-192">プロジェクト実績の更新 (Finance and Operations から Project Service Automation) テンプレートでは、既にこの変換を定義しています。</span><span class="sxs-lookup"><span data-stu-id="94b15-192">This transformation is already defined in the Project actuals update (Fin Ops to PSA) template.</span></span>
- <span data-ttu-id="94b15-193">Finance and Operations の請求タイプを、Project Service Automation の正しい請求タイプに変換します。</span><span class="sxs-lookup"><span data-stu-id="94b15-193">Transform the billing type in Finance and Operations to the correct billing type in Project Service Automation.</span></span> <span data-ttu-id="94b15-194">プロジェクト実績の更新 (Finance and Operations から Project Service Automation) テンプレートでは、既にこの変換を定義しています。</span><span class="sxs-lookup"><span data-stu-id="94b15-194">This transformation is already defined in the Project actuals update (Fin Ops to PSA) template.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="94b15-195">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="94b15-195">Template mapping in Data integration</span></span>

<span data-ttu-id="94b15-196">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="94b15-196">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="94b15-197">マッピングは、Finance and Operations から Project Service Automation に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="94b15-197">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="94b15-198">[![テンプレートのマッピング](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="94b15-198">[![Template mapping](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span></span>

<span data-ttu-id="94b15-199">[![テンプレートのマッピング](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span><span class="sxs-lookup"><span data-stu-id="94b15-199">[![Template mapping](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span></span>
