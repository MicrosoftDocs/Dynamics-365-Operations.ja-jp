---
title: "プロジェクト実績を、Project Service Automation から Finance and Operations へ転記する統合仕訳帳に、直接同期させます。"
description: "このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へ直接プロジェクト実績を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: ja-jp
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a><span data-ttu-id="8a19e-103">プロジェクト実績を、Project Service Automation から Finance and Operations へ転記する統合仕訳帳に、直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-103">Synchronize project actuals from Project Service Automation directly to the project integration journal for posting in Finance and Operations</span></span>

<span data-ttu-id="8a19e-104">このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へ直接プロジェクト実績を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-104">This topic describes the templates and underlying tasks that are used to synchronize project actuals directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="8a19e-105">テンプレートは、Project Service Automation から Finance and Operations のステージング テーブルへ、トランザクションを同期します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-105">The template syncs transactions from Project Service Automation into a staging table in Finance and Operations.</span></span> <span data-ttu-id="8a19e-106">同期が完了した後、統合仕訳帳にステージング テーブルからインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-106">After synchronization is complete, you must import from the staging table to the integration journal.</span></span>

> [!NOTE]
> <span data-ttu-id="8a19e-107">プロジェクト実績の統合は、Dynamics 365 for Finance and Operations バージョン 8.01 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="8a19e-107">Project actuals integration is available in Dynamics 365 for Finance and Operations version 8.01.</span></span>

> [!NOTE]
> <span data-ttu-id="8a19e-108">Project Service Automation で時間や経費のトランザクションに対する消費税金額を入力する場合は、Project Service Automation の更新プログラム 7 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-108">If you are entering sales tax amounts on time or expense transactions in Project Service Automation, you must install the Project Service Automation Update 7.</span></span> <span data-ttu-id="8a19e-109">この更新プログラムがインストールされていない場合、税の実績は関連付けられている時間または経費の実績にリンクされず、Finance and Operations に同期されません。</span><span class="sxs-lookup"><span data-stu-id="8a19e-109">If this update is not installed, the tax actuals will not be linked to the associated time or expense actuals and will not be synced to Finance and Operations.</span></span> <span data-ttu-id="8a19e-110">詳細については、サポートにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="8a19e-110">Contact Support for more information.</span></span>


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="8a19e-111">Project Service Automation から Finance and Operations のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="8a19e-111">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="8a19e-112">Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-112">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="8a19e-113">データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト実績に関するデータ フローを有効にします。</span><span class="sxs-lookup"><span data-stu-id="8a19e-113">The integration templates that are available with the Data integration feature enable the flow of data about project actuals from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="8a19e-114">次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8a19e-114">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="8a19e-115">[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span><span class="sxs-lookup"><span data-stu-id="8a19e-115">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="8a19e-116">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="8a19e-116">Templates and tasks</span></span>

<span data-ttu-id="8a19e-117">使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-117">To access the available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="8a19e-118">次のテンプレートおよび基本的なタスクは、Project Service Automation から Finance and Operations プロジェクト実績を同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-118">The following template and underlying tasks are used to synchronize project actuals from Project Service Automation to Finance and Operations:</span></span>

-  <span data-ttu-id="8a19e-119">**データ統合でのテンプレートの名前:** プロジェクト実績 (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="8a19e-119">**Name of the template in Data integration:** Project actuals (PSA to Fin and Ops)</span></span>

-  <span data-ttu-id="8a19e-120">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="8a19e-120">**Name of the tasks in the project:**</span></span> 
    - <span data-ttu-id="8a19e-121">実績</span><span class="sxs-lookup"><span data-stu-id="8a19e-121">Actuals</span></span> 
    - <span data-ttu-id="8a19e-122">トランザクション接続</span><span class="sxs-lookup"><span data-stu-id="8a19e-122">TransactionConnections</span></span>

## <a name="entity-set"></a><span data-ttu-id="8a19e-123">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="8a19e-123">Entity set</span></span>

| <span data-ttu-id="8a19e-124">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8a19e-124">Project Service Automation</span></span>      | <span data-ttu-id="8a19e-125">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8a19e-125">Finance and Operations</span></span>                                      |
|---------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="8a19e-126">実績</span><span class="sxs-lookup"><span data-stu-id="8a19e-126">Actuals</span></span>                         | <span data-ttu-id="8a19e-127">プロジェクト実績の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="8a19e-127">Integration entity for project actuals</span></span>                      |
| <span data-ttu-id="8a19e-128">トランザクション接続</span><span class="sxs-lookup"><span data-stu-id="8a19e-128">Transaction Connections</span></span>         | <span data-ttu-id="8a19e-129">プロジェクト トランザクション リレーションシップに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="8a19e-129">Integration entity for project transaction relationships</span></span>    |

## <a name="entity-flow"></a><span data-ttu-id="8a19e-130">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="8a19e-130">Entity flow</span></span>

<span data-ttu-id="8a19e-131">プロジェクト実績は Project Service Automation で管理され、プロジェクトの統合仕訳帳に対する Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-131">Project actuals are managed in Project Service Automation, and they are synchronized to Finance and Operations to the project ingetration journal.</span></span> <span data-ttu-id="8a19e-132">既定の財務分析コードと転記設定に基づいて、会計が適用されます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-132">The accounting will be applied based on default financial dimensions and posting setup.</span></span>

## <a name="preconditions"></a><span data-ttu-id="8a19e-133">事前条件</span><span class="sxs-lookup"><span data-stu-id="8a19e-133">Preconditions</span></span>

<span data-ttu-id="8a19e-134">実績の同期を行う前に、Project Service Automation 統合パラメーターを設定し、プロジェクト、プロジェクト タスク、およびプロジェクトの経費トランザクションのカテゴリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-134">Before synchronization of actuals can occur, you must configure the Project Service Automation integration parameters and synchronize projects, project tasks, and project expense transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="8a19e-135">Power Query</span><span class="sxs-lookup"><span data-stu-id="8a19e-135">Power Query</span></span>

<span data-ttu-id="8a19e-136">プロジェクト実績テンプレートで Microsoft Power Query を使用して、以下を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-136">You must use Microsoft Power Query in the project actuals template to:</span></span>
- <span data-ttu-id="8a19e-137">Project Service Automation **トランザクション タイプ**を、Finance and Operations の正しい**トランザクション タイプ**に変換します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-137">Transform the Project Service Automation **transaction type** to the correct **transaction type** in Finance and Operations.</span></span> <span data-ttu-id="8a19e-138">プロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートは、既にこの変換を定義しています。</span><span class="sxs-lookup"><span data-stu-id="8a19e-138">The Project actuals (PSA to Fin and Ops) template already has this transformation defined.</span></span>
- <span data-ttu-id="8a19e-139">Project Service Automation **請求タイプ**を、Finance and Operations の正しい**請求タイプ**に変換します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-139">Transform the Project Service Automation **billing type** to the correct **billing type** in Finance and Operations.</span></span> <span data-ttu-id="8a19e-140">プロジェクト実績 (Project Service Automation から Finance and Operations) テンプレートは、既にこの変換を定義しています。</span><span class="sxs-lookup"><span data-stu-id="8a19e-140">The Project actuals (PSA to Fin and Ops) template already has this transformation defined.</span></span> <span data-ttu-id="8a19e-141">すると、請求タイプは Dynamics 365 for Project Service Automation 統合パラメーター フォームのコンフィギュレーションに基づいて、**明細行プロパティ**にマップされます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-141">The billing type is then mapped to the **line property** based on the configuration in the Dynamics 365 for Project Service Automation integration parameters form.</span></span>
- <span data-ttu-id="8a19e-142">このテンプレートと同期する必要のある、特定の**組織単位のリソース**にフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-142">Filter to specific **Resource organizational units** that are to be synced with this template.</span></span>
- <span data-ttu-id="8a19e-143">**会社間時間または会社間経費の実績**を Finance and Operations に同期させると、Finance and Operations で**契約組織単位**を、正しい**法人**に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-143">If **intercompany time or intercompany expense actuals** will be synced to Finance and Operations, you must transform the **contract organizational unit** to the correct **legal entity** in Finance and Operations.</span></span> <span data-ttu-id="8a19e-144">プロジェクト実績 (Project Service Automation から Finance and Operations) には、デモ データに基づいて定義された条件付き列があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-144">The Project actuals (PSA to Fin and Ops) template has a conditional column defined based on demo data.</span></span> <span data-ttu-id="8a19e-145">正しい法人に最後に挿入された条件付き列を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-145">You must update the last inserted condition column to the correct legal entities.</span></span> <span data-ttu-id="8a19e-146">これに失敗すると、統合エラーあるいは Finance and Operations にインポートされた無効な実績トランザクションが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-146">Failure to do this may result in either an integration error or incorrect actual transactions imported into Finance and Operations.</span></span>
- <span data-ttu-id="8a19e-147">**会社間時間または会社間経費の実績**が Finance and operations と同期されない場合、最後に挿入した条件付き列をテンプレートから削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-147">If **intercompany time or intercompany expense actuals** will not be synced to Finance and operations, you must delete the last inserted condition column from your template.</span></span> <span data-ttu-id="8a19e-148">これに失敗すると、統合エラーあるいは Finance and Operations にインポートされた無効な実績トランザクションが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-148">Failure to do this may result in either an integration error or incorrect actual transactions imported into Finance and Operations.</span></span>

### <a name="contract-organizational-unit"></a><span data-ttu-id="8a19e-149">契約組織単位</span><span class="sxs-lookup"><span data-stu-id="8a19e-149">Contract Organizational Unit</span></span>
<span data-ttu-id="8a19e-150">テンプレートの挿入された条件付き列を更新するには、**マップ**矢印をクリックしてマッピングを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-150">To update the inserted condition column in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="8a19e-151">高度なクエリおよびフィルタリングを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-151">Select to open the Advanced Query and Filtering.</span></span>
- <span data-ttu-id="8a19e-152">既定の Microsoft Project 実績 (Project Service Automation から Finance and Operations) テンプレートを使用している場合、**適用されたステップ**セクションで**挿入された条件**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-152">If you are using the default Microsoft Project actuals (PSA to Fin and Ops) template, select the lasat **Inserted Condition** in the **Applied Steps** section.</span></span> <span data-ttu-id="8a19e-153">**機能**入力で、**USSI** を統合して使用する**法人**の名前に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-153">In the **Function** entry, replace **USSI** with the name of the **Legal entity** that should be used with the integration.</span></span> <span data-ttu-id="8a19e-154">**関数**入力に必要な追加条件を追加し、**USMF** から正しい**法人**へ、**他の**条件を更新します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-154">Add additional conditions as needed to the **Function** entry and update the **else** condition from **USMF** to the correct **Legal entity**.</span></span>
- <span data-ttu-id="8a19e-155">新しいテンプレートを作成する場合、会社間時間および会社間経費をサポートするためにこの列を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-155">If you are creating a new template, you must add this column to support intercompany time and expenses.</span></span> <span data-ttu-id="8a19e-156">**条件付き列の追加**を選択し、列に LegalEntity などの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-156">Select **Add Conditional Column** and give the column a name, such as LegalEntity.</span></span> <span data-ttu-id="8a19e-157">msdyn_contractorganizationalunitid.msdyn_name が <organizational unit> である場合は列の条件を入力し、次に <enter the Legal entity> を行います。その他は null を表します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-157">Enter the condition for the column where if msdyn_contractorganizationalunitid.msdyn_name is <organizational unit>, then <enter the Legal entity>; else null.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8a19e-158">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="8a19e-158">Template mapping in Data integration</span></span>

<span data-ttu-id="8a19e-159">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-159">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="8a19e-160">マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-160">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="8a19e-161">[![テンプレートのマッピング](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="8a19e-161">[![Template mapping](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span></span>

<span data-ttu-id="8a19e-162">[![テンプレートのマッピング](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span><span class="sxs-lookup"><span data-stu-id="8a19e-162">[![Template mapping](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span></span>

## <a name="import-from-staging-table"></a><span data-ttu-id="8a19e-163">ステージング テーブルからインポートする</span><span class="sxs-lookup"><span data-stu-id="8a19e-163">Import from staging table</span></span>

<span data-ttu-id="8a19e-164">ステージング テーブルの定期処理からのインポートは、Project Service Automation から Finance and Operations への実績の同期後に実行される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-164">The Import from staging table perioidic process must be run after the sychronization of actuals from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="8a19e-165">この処理では、プロジェクト トランザクションがステージング テーブルから Project Service Automation 統合仕訳帳にインポートされ、会計が適用され、インポートされたトランザクションが転記されます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-165">This process will import the project transactions from the staging table into the Project Service Automation integration journal, where the accounting is applied and the imported transactions can be posted.</span></span> <span data-ttu-id="8a19e-166">この処理はバッチ モードで実行し、必要に応じて繰り返し実行されるバッチとして設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8a19e-166">It is recommended that you run this process in batch mode and optionally can be set up to run as a recurring batch.</span></span>

## <a name="update-actuals"></a><span data-ttu-id="8a19e-167">実績の更新</span><span class="sxs-lookup"><span data-stu-id="8a19e-167">Update Actuals</span></span>

<span data-ttu-id="8a19e-168">次のテンプレートおよび基本的なタスクは Finance and Operations から Project Service Automation へ伝票番号とプロジェクト実績に転記した消費税を同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-168">The following template and underlying tasks are used to synchronize the voucher number and sales taxes for posted project transactions from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="8a19e-169">**データ統合でのテンプレートの名前:** プロジェクト実績の更新 (Finance and Operations から Project Service Automation)</span><span class="sxs-lookup"><span data-stu-id="8a19e-169">**Name of the template in Data integration:** Project actuals update (Fin Ops to PSA)</span></span>
-  <span data-ttu-id="8a19e-170">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="8a19e-170">**Name of the tasks in the project:**</span></span> 
     - <span data-ttu-id="8a19e-171">実績</span><span class="sxs-lookup"><span data-stu-id="8a19e-171">Actuals</span></span> 
     - <span data-ttu-id="8a19e-172">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="8a19e-172">TransactionConnections</span></span>

## <a name="entity-set"></a><span data-ttu-id="8a19e-173">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="8a19e-173">Entity set</span></span>

| <span data-ttu-id="8a19e-174">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8a19e-174">Finance and Operations</span></span>                                         | <span data-ttu-id="8a19e-175">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8a19e-175">Project Service Automation</span></span>        |
|----------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="8a19e-176">プロジェクト実績の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="8a19e-176">Integration entity for project actuals</span></span>                         | <span data-ttu-id="8a19e-177">実績</span><span class="sxs-lookup"><span data-stu-id="8a19e-177">Actuals</span></span>                           |
| <span data-ttu-id="8a19e-178">プロジェクト トランザクション リレーションシップに対する統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="8a19e-178">Integration entity for project transaction relationships</span></span>       | <span data-ttu-id="8a19e-179">Transaction Connections</span><span class="sxs-lookup"><span data-stu-id="8a19e-179">Transaction Connections</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="8a19e-180">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="8a19e-180">Entity flow</span></span>

<span data-ttu-id="8a19e-181">プロジェクト実績は Project Service Automation で管理され、プロジェクトの統合仕訳帳に対する Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-181">Project actuals are managed in Project Service Automation, and they are synchronized to Finance and Operations to the project integration journal.</span></span> <span data-ttu-id="8a19e-182">Finance and Operations に転記されると、Finance and Operations からの伝票番号によって、実績は Project Service Automation で更新されます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-182">Once posted in Finance and Operations, actuals are updated in Project Service Automation with the voucher number from Finance and Operations.</span></span> <span data-ttu-id="8a19e-183">Finance and Operations で消費税が追加された場合、PRoject Service Automation で新しい税実績が作成されます。</span><span class="sxs-lookup"><span data-stu-id="8a19e-183">If sales taxes were added in Finance and Operations, new tax actuals will be created in PRoject Service Automation.</span></span>

## <a name="power-query"></a><span data-ttu-id="8a19e-184">Power Query</span><span class="sxs-lookup"><span data-stu-id="8a19e-184">Power Query</span></span>

<span data-ttu-id="8a19e-185">プロジェクト実績更新テンプレートで Microsoft Power Query を使用して、以下を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a19e-185">You must use Microsoft Power Query in the project actuals update template to:</span></span>
- <span data-ttu-id="8a19e-186">Finance and Operations **トランザクション タイプ**を、Project Service Automation の正しい**トランザクション タイプ**に変換します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-186">Transform the Finance and Operations **transaction type** to the correct **transaction type** in Project Service Automation.</span></span> <span data-ttu-id="8a19e-187">プロジェクト実績更新 (Finance and Operations から Project Service Automation) テンプレートは、既にこの変換を定義しています。</span><span class="sxs-lookup"><span data-stu-id="8a19e-187">The Project actuals update (Fin Ops to PSA) template already has this transformation defined.</span></span>
- <span data-ttu-id="8a19e-188">Finance and Operations **請求タイプ**を、Project Service Automation の正しい**請求タイプ**に変換します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-188">Transform the Finance and Operations **billing type** to the correct **billing type** in Project Service Automation.</span></span> <span data-ttu-id="8a19e-189">プロジェクト実績更新 (Finance and Operations から Project Service Automation) テンプレートは、既にこの変換を定義しています。</span><span class="sxs-lookup"><span data-stu-id="8a19e-189">The Project actuals update (Fin Ops to PSA) template already has this transformation defined.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8a19e-190">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="8a19e-190">Template mapping in Data integration</span></span>

<span data-ttu-id="8a19e-191">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-191">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="8a19e-192">マッピングは、Finance and Operations から Project Service Automation に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="8a19e-192">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="8a19e-193">[![テンプレートのマッピング](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="8a19e-193">[![Template mapping](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span></span>

<span data-ttu-id="8a19e-194">[![テンプレートのマッピング](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span><span class="sxs-lookup"><span data-stu-id="8a19e-194">[![Template mapping](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span></span>




