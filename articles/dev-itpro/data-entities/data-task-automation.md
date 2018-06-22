---
title: "データ タスクの自動化"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータ タスク自動化を使用して、各種のデータ タスクを簡単に繰り返し、各タスクの結果を検証する方法について説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform update 16
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 8e79030522bd5046964ed50f2bdf627efbe3b11f
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="data-task-automation"></a><span data-ttu-id="f3a31-103">データ タスクの自動化</span><span class="sxs-lookup"><span data-stu-id="f3a31-103">Data task automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f3a31-104">Microsoft Dynamics 365 for Finance and Operations のデータ タスク自動化は、各種のデータ タスクを簡単に繰り返し、各タスクの結果を検証を可能にします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-104">Data task automation in Microsoft Dynamics 365 for Finance and Operations lets you easily repeat many types of data tasks and validate the outcome of each task.</span></span> <span data-ttu-id="f3a31-105">データ タスクの自動化は、実装フェーズにあるプロジェクトで非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="f3a31-105">Data task automation is very useful for projects that are in the implementation phase.</span></span> <span data-ttu-id="f3a31-106">たとえば、データ プロジェクトの作成およびコンフィギュレーションを自動化することができます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-106">For example, you can automate the creation and configuration of data projects.</span></span> <span data-ttu-id="f3a31-107">また、デモ データおよび高品質の構成データ、およびデータ移行に関連する他のタスクなどの、インポート/エクスポート オペレーションの実行を構成およびトリガーすることができます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-107">You can also configure and trigger the execution of import/export operations, such as the setup of demo data and golden configuration data, and other tasks that are related to data migration.</span></span> <span data-ttu-id="f3a31-108">また、タスクの結果の検証を使用して、データ エンティティの自動テストを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-108">You can also create automated testing of data entities by using task outcome validation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3a31-109">現時点では、オンプレミス環境ではデータ タスクの自動化はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f3a31-109">Data task automation isn't currently supported for on-premises environments.</span></span>

<span data-ttu-id="f3a31-110">データ タスクの自動化のために次の方法をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-110">We recommend the following approach for data task automation.</span></span>

1. <span data-ttu-id="f3a31-111">自動化の恩恵を受けるデータ関連のタスクを特定する。</span><span class="sxs-lookup"><span data-stu-id="f3a31-111">Identify the data-related tasks that will benefit from automation.</span></span>

    <span data-ttu-id="f3a31-112">実装チームは自分たちの構成管理計画とデータ移行計画をレビューして、自動化のための潜在的なデータ タスクを識別すること、またデータ エンティティのテスト ケースも識別することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-112">We recommend that implementation teams review their configuration management plan and data migration plan to identify potential data tasks for automation, and also to identify data entity test cases.</span></span>

2. <span data-ttu-id="f3a31-113">タスクを定義します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-113">Define tasks.</span></span>

    <span data-ttu-id="f3a31-114">タスクは、XML マニフェストで定義されます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-114">Tasks are defined in an XML manifest.</span></span> <span data-ttu-id="f3a31-115">アプリケーション ライフ サイクルの管理 (ALM) 戦略では、構成管理の一部としてソース管理下のマニフェストを保持することができます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-115">You can keep your manifest under source control as part of configuration management in your application lifecycle management (ALM) strategy.</span></span>

3. <span data-ttu-id="f3a31-116">Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリでのデータ タスクの自動化に関連するデータ パッケージを配置します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-116">Put the data packages that are related to data task automation in the Shared asset library of Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="f3a31-117">また、必要に応じて特定の LCS プロジェクトを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-117">You can also use a specific LCS project as you require.</span></span>

    <span data-ttu-id="f3a31-118">データ タスク自動化マネージャは、LCS プロジェクトに関連するサンドボックスまたは実稼動環境からパッケージを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-118">Data task automation manager can consume packages from any sandbox and/or production environment that is related to the LCS project.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="f3a31-119">Finance and Operations のデータ タスク自動化マネージャーを実行するユーザー アカウントは、LCS およびデータ パッケージのマニフェストで参照される LCS プロジェクトにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-119">The user account that runs Data task automation manager in Finance and Operations must have access to LCS and to the LCS project that is referenced in the manifest for data packages.</span></span>
    > - <span data-ttu-id="f3a31-120">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合アプリケーション プログラミング インターフェイス (API) を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-120">Although data task automation can be run in any environment in the cloud, we strongly recommend that you not run any import/export tasks that use integration application programming interfaces (APIs) in a production environment.</span></span> <span data-ttu-id="f3a31-121">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-121">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

4. <span data-ttu-id="f3a31-122">データ タスクを実行し、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-122">Run the data tasks, and then review the outcomes.</span></span>

    <span data-ttu-id="f3a31-123">データ タスク自動化マネージャは、各タスクの成功または失敗の結果を提供します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-123">Data task automation manager provides the success or failure outcome for each task.</span></span> <span data-ttu-id="f3a31-124">また、タスクが失敗した理由に関する見解も提供します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-124">It also provides insights into the reason why a task failed.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="f3a31-125">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合 API を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-125">Although data task automation can be run in any environments in the cloud, we recommend that you not run any import/export tasks that use integration APIs in a production environment.</span></span> <span data-ttu-id="f3a31-126">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-126">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

<span data-ttu-id="f3a31-127">次のビデオは、Data Task Automation Manager の初期リリースを紹介する TechTalk の 55 分です。</span><span class="sxs-lookup"><span data-stu-id="f3a31-127">The following video is a 55-minute TechTalk that walks you through an early release of Data task automation manager.</span></span>

> [!Video https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4]

## <a name="task-manifest"></a><span data-ttu-id="f3a31-128">タスク マニフェスト</span><span class="sxs-lookup"><span data-stu-id="f3a31-128">Task manifest</span></span>
<span data-ttu-id="f3a31-129">タスクは、XML マニフェストで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-129">A task must be defined in an XML manifest.</span></span> <span data-ttu-id="f3a31-130">このセクションでは、マニフェストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-130">This section describes the manifest.</span></span> <span data-ttu-id="f3a31-131">マニフェストを名前付けしデザインする方法の指針については、このトピックの後半の、「マニフェストのデザインに対するベスト プラクティス」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3a31-131">For guidance about how to name and design the manifest, see the "Best practices for manifest design" section later in this topic.</span></span>

### <a name="manifest-root"></a><span data-ttu-id="f3a31-132">マニフェスト ルート</span><span class="sxs-lookup"><span data-stu-id="f3a31-132">Manifest root</span></span>
<span data-ttu-id="f3a31-133">**\<TestManifest\>** 要素は、マニフェストのルートです。</span><span class="sxs-lookup"><span data-stu-id="f3a31-133">The **\<TestManifest\>** element is the root of the manifest.</span></span> <span data-ttu-id="f3a31-134">その他のすべての要素はこの要素の子です。</span><span class="sxs-lookup"><span data-stu-id="f3a31-134">All other elements are children of this element.</span></span>

```
<?xml version='1.0' encoding='utf-8'?>
<TestManifest name='Data management demo data set up'>
    <SharedSetup />
        <JobDefinition ID='ImportJobDefinition_1' />
        <EntitySetup ID='Generic' />
    </SharedSetup>
    <TestGroup />
</TestManifest>
```

### <a name="shared-setup"></a><span data-ttu-id="f3a31-135">共有された設定</span><span class="sxs-lookup"><span data-stu-id="f3a31-135">Shared setup</span></span>
<span data-ttu-id="f3a31-136">**共有セットアップ** セクションは、全般的なタスクのパラメーターとマニフェスト内のすべてのタスクの動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-136">The **Shared setup** section defines general task parameters and behaviors for all tasks in the manifest.</span></span>

### <a name="data-files"></a><span data-ttu-id="f3a31-137">データ ファイル</span><span class="sxs-lookup"><span data-stu-id="f3a31-137">Data files</span></span>
<span data-ttu-id="f3a31-138">**\<DataFile\>** 要素は、マニフェスト内のタスクが使用するデータ パッケージとデータ ファイルを定義します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-138">**\<DataFile\>** elements define the data packages and data files that the tasks in the manifest will use.</span></span> <span data-ttu-id="f3a31-139">データ ファイルは、LCS プロジェクトの LCS アセット ライブラリまたは共有アセット ライブラリのいずれかになければなりません。</span><span class="sxs-lookup"><span data-stu-id="f3a31-139">The data files must be either in the LCS asset library of your LCS project or in the Shared asset library.</span></span>

```
<DataFile ID='SharedSetup' name='Demo data-7.3-100-System and Shared'  assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsHQUS' name='Demo data-7.3-200-Financials-HQUS' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPICH' name='Demo data-7.3-200-Financials-PICH' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPIFB' name='Demo data-7.3-200-Financials-PIFB' assetType='Data package' lcsProjectId=''/>
```

### <a name="data-project-definition"></a><span data-ttu-id="f3a31-140">データ プロジェクト定義</span><span class="sxs-lookup"><span data-stu-id="f3a31-140">Data project definition</span></span>
<span data-ttu-id="f3a31-141">**\<JobDefinition\>** 要素は、データ プロジェクト定義を定義します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-141">The **\<JobDefinition\>** element defines the data project definition.</span></span> <span data-ttu-id="f3a31-142">マニフェストには複数のジョブ定義があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-142">There can be more than one job definition in a manifest.</span></span>

```
<JobDefinition ID='ImportJobDefinition_1'>
    <Operation>Import</Operation>
    <SkipStaging></SkipStaging>
    <Truncate></Truncate>
    <Mode>Import async</Mode>
    <BatchFrequencyInMinutes>1</BatchFrequencyInMinutes>
    <NumberOfTimesToRunBatch >2</NumberOfTimesToRunBatch>
    <UploadFrequencyInSeconds>1</UploadFrequencyInSeconds>
    <TotalNumberOfTimesToUploadFile>1</TotalNumberOfTimesToUploadFile>
    <SupportedDataSourceType>Package</SupportedDataSourceType>
    <ProcessMessagesInOrder>No</ProcessMessagesInOrder>
    <PreventUploadWhenZeroRecords>No</PreventUploadWhenZeroRecords>
    <UseCompanyFromMessage>Yes</UseCompanyFromMessage>
    <LegalEntity>DAT</LegalEntity>
</JobDefinition>
```

### <a name="entity-setup"></a><span data-ttu-id="f3a31-143">エンティティ設定</span><span class="sxs-lookup"><span data-stu-id="f3a31-143">Entity setup</span></span>
<span data-ttu-id="f3a31-144">**エンティティ設定** セクションは、マニフェストのタスクが使用するエンティティの特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-144">The **Entity setup** section defines the characteristics of an entity that a task in the manifest will use.</span></span> <span data-ttu-id="f3a31-145">マニフェスト内のタスクによって使用されるエンティティごとに、1 つずつ複数の定義が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-145">There can be more than one definition, one for each entity that is used by the tasks in the manifest.</span></span>

```
<EntitySetup ID='Generic'>
    <Entity name='*'>
        <SourceDataFormatName>Package</SourceDataFormatName>
        <ChangeTracking></ChangeTracking>
        <PublishToBYOD></PublishToBYOD>
        <DefaultRefreshType>Full push only</DefaultRefreshType>
        <ExcelWorkSheetName></ExcelWorkSheetName>
        <SelectFields>All fields</SelectFields>
        <SetBasedProcessing></SetBasedProcessing>
        <FailBatchOnErrorForExecutionUnit>No</FailBatchOnErrorForExecutionUnit>
        <FailBatchOnErrorForLevel>No</FailBatchOnErrorForLevel>
        <FailBatchOnErrorForSequence>No</FailBatchOnErrorForSequence>
        <ParallelProcessing>
            <Threshold></Threshold>
            <TaskCount></TaskCount>
        </ParallelProcessing>
    </Entity>
</EntitySetup>
```

### <a name="test-groups"></a><span data-ttu-id="f3a31-146">テスト グループ</span><span class="sxs-lookup"><span data-stu-id="f3a31-146">Test groups</span></span>
<span data-ttu-id="f3a31-147">テスト グループは、マニフェストの関連するタスクを整理するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-147">Test groups can be used to organize related tasks in a manifest.</span></span> <span data-ttu-id="f3a31-148">マニフェストには複数のテスト グループがあります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-148">There can be more than one test group in a manifest.</span></span>

```
<TestGroup name='Set up Financials'>
    <TestCase Title='Import shared set up data package' ID='3933885' RepeatCount='1' TraceParser='off' TimeOut='20'>
        <DataFile RefID='SharedSetup' />
        <JobDefinition RefID='ImportJobDefinition_1' />
        <EntitySetup RefID='Generic' />
    </TestCase>
    
    <TestCase Title='Import financials for HQUS' ID='3933886' RepeatCount='1' TraceParser='off' TimeOut='20'>
        <DataFile RefID='FinancialsHQUS' />
        <JobDefinition RefID='ImportJobDefinition_1'>
            <LegalEntity>HQUS</LegalEntity>
        </JobDefinition>
        <EntitySetup RefID='Generic' />
    </TestCase>

    <TestCase Title='Import financials for PICH' ID='3933887' RepeatCount='1' TraceParser='off' TimeOut='20'>
        <DataFile RefID='FinancialsPICH' />
        <JobDefinition RefID='ImportJobDefinition_1'>
            <LegalEntity>PICH</LegalEntity>
        </JobDefinition>
        <EntitySetup RefID='Generic' />
    </TestCase>

    <TestCase Title='Import financials for PIFB' ID='3933888' RepeatCount='1' TraceParser='off' TimeOut='20'>
        <DataFile RefID='FinancialsPIFB' />
        <JobDefinition RefID='ImportJobDefinition_1'>
            <LegalEntity>PIFB</LegalEntity>
        </JobDefinition>
        <EntitySetup RefID='Generic' />
    </TestCase>
</TestGroup>
```

## <a name="best-practices-for-manifest-design"></a><span data-ttu-id="f3a31-149">マニフェスト デザインのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="f3a31-149">Best practices for manifest design</span></span>
<span data-ttu-id="f3a31-150">さまざまな方法でマニフェストを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-150">You can define a manifest in many ways.</span></span> <span data-ttu-id="f3a31-151">マニフェストをデザインするときに考慮する必要があるいくつかのポインターを次に示します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-151">Here are a few pointers that you should consider when you design a manifest.</span></span>

### <a name="granularity"></a><span data-ttu-id="f3a31-152">粒度</span><span class="sxs-lookup"><span data-stu-id="f3a31-152">Granularity</span></span>
<span data-ttu-id="f3a31-153">機能的な意思決定としてマニフェストの粒度を判断することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-153">We recommend that you determine the granularity of your manifest as a functional decision.</span></span> <span data-ttu-id="f3a31-154">チームは、複数のマニフェストを管理するか、または単一のマニフェストの変更を管理するかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-154">Your team must decide whether it wants to manage many manifests or manage changes in a single manifest.</span></span>

- <span data-ttu-id="f3a31-155">チームが論理的に必要と考える数のマニフェストを使って開始します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-155">Start with as many manifests as your team thinks you logically need.</span></span> <span data-ttu-id="f3a31-156">後で、チームが実際にマニフェストの実行を開始すると、予想より少ないマニフェストを使用しており、それらを結合したいと考える場合があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-156">Later, when the team actually starts to run the manifests, it might find that it uses fewer manifests than it expected, and it might want to merge them.</span></span> <span data-ttu-id="f3a31-157">この場合、マニフェストをマージすることができます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-157">In this case, you can merge manifests.</span></span>
- <span data-ttu-id="f3a31-158">職務の分離を検討する。</span><span class="sxs-lookup"><span data-stu-id="f3a31-158">Consider separation of duties.</span></span> <span data-ttu-id="f3a31-159">たとえば、デモ データの設定に対して 1 つのマニフェスト、環境の高品質の構成の設定に対して別のマニフェストがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-159">For example, you might have one manifest for the setup of demo data and another manifest for the setup of the golden configuration for your environment.</span></span> <span data-ttu-id="f3a31-160">この方法で、チーム メンバーが使用する予定のマニフェストのみを使用することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-160">In this way, you can make sure that team members use only the manifests that they are supposed to use.</span></span>
- <span data-ttu-id="f3a31-161">LCS へのユーザー アクセスについて考慮してください。</span><span class="sxs-lookup"><span data-stu-id="f3a31-161">Consider user access to LCS.</span></span> <span data-ttu-id="f3a31-162">たとえば、大きなおよびグローバルに配分された実装チームは、Finance and Operations の複数のインスタンスまたは複数の LCS プロジェクトを持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-162">For example, larger and globally distributed implementation teams might have multiple instances of Finance and Operations or multiple LCS projects.</span></span>

### <a name="inheritance"></a><span data-ttu-id="f3a31-163">継承</span><span class="sxs-lookup"><span data-stu-id="f3a31-163">Inheritance</span></span>
<span data-ttu-id="f3a31-164">マニフェスト スキーマは、マニフェスト内のすべてのタスクに適用される共通要素の継承をサポートします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-164">The manifest schema supports inheritance of common elements that will apply to all tasks in the manifest.</span></span> <span data-ttu-id="f3a31-165">タスクは、共通の要素を上書きして一意の動作を定義できます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-165">A task can override a common element to define a unique behavior.</span></span> <span data-ttu-id="f3a31-166">**共通設定** セクションの目的は、構成要素の繰り返しを最小限に抑えて、可能な限り要素を再利用することです。</span><span class="sxs-lookup"><span data-stu-id="f3a31-166">The purpose of the **Shared setup** section is to minimize repetition of configuration elements, so that elements are reused as much as possible.</span></span> <span data-ttu-id="f3a31-167">目標は、メンテナンスと可読性を向上させるために、マニフェストを簡潔かつ清潔に保つことです。</span><span class="sxs-lookup"><span data-stu-id="f3a31-167">The goal is to keep the manifest concise and clean, to improve maintenance and readability.</span></span>

### <a name="source-control"></a><span data-ttu-id="f3a31-168">ソース管理</span><span class="sxs-lookup"><span data-stu-id="f3a31-168">Source control</span></span>
<span data-ttu-id="f3a31-169">実装チームのすべてのメンバーが使用する必要があるマニフェストは、アプリケーション オブジェクト ツリー (AOT) 内のソース コントロールに格納されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-169">Manifests that must be used by all the members of an implementation team should be stored in source control in the Application Object Tree (AOT).</span></span> <span data-ttu-id="f3a31-170">この方法は、ソース管理の利点を提供するだけでなく、プロセスがすべてのユーザーに一貫した方法で配布またはマニフェストを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-170">This approach not only provides the benefits of source control, but also enables a process to distribute or make manifests available to all users in a consistent manner.</span></span> <span data-ttu-id="f3a31-171">また、この方法では、マニフェストを構成に使用する場合、データ管理に関連するデータ プロジェクトの構成管理も可能です。</span><span class="sxs-lookup"><span data-stu-id="f3a31-171">This approach also enables configuration management for data projects that are related to data management, if manifests are used for configuration.</span></span>

### <a name="number-of-job-definitions-and-entity-definitions"></a><span data-ttu-id="f3a31-172">ジョブ定義とエンティティ定義の数</span><span class="sxs-lookup"><span data-stu-id="f3a31-172">Number of job definitions and entity definitions</span></span>
<span data-ttu-id="f3a31-173">使用ケースのほとんどの場合、マニフェストで 1 つのジョブ定義で十分であるのは、継承がタスク レベルでの動作を変更するために使用できるからです。</span><span class="sxs-lookup"><span data-stu-id="f3a31-173">For most of the use cases, one job definition in a manifest should be enough, because inheritance can be used to change the behavior at the task level.</span></span> <span data-ttu-id="f3a31-174">この原則は、エンティティの定義にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-174">This principle also applies to entity definitions.</span></span>

## <a name="validations"></a><span data-ttu-id="f3a31-175">検証</span><span class="sxs-lookup"><span data-stu-id="f3a31-175">Validations</span></span>
<span data-ttu-id="f3a31-176">データ タスク自動化マネージャは、タスクの設定に基づいて検証を実行します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-176">Data task automation manager performs validations, based on the setup of a task.</span></span> <span data-ttu-id="f3a31-177">タスクが失敗した場合は、タスクの完了後に、検証を表示することによって、エラーの原因をすばやく確認できます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-177">If a task fails, you can quickly determine the reason for the failure by viewing the validations after the task is completed.</span></span> <span data-ttu-id="f3a31-178">データ タスク自動化マネージャーが提供する情報のレベルは、初期検出を容易にするために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="f3a31-178">The level of information that Data task automation manager provides is optimized to facilitate initial discovery.</span></span> <span data-ttu-id="f3a31-179">詳細な調査のためには、対応するデータ プロジェクトおよびその実行の詳細を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-179">For detailed investigation, you must look at the corresponding data project and its execution details.</span></span>

<span data-ttu-id="f3a31-180">現在、次のデータ検証がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f3a31-180">The following data validations are currently supported:</span></span>

- <span data-ttu-id="f3a31-181">**ジョブ ステータス** – この検証は、ジョブが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-181">**Job status** – This validation checks whether the job was successful.</span></span>
- <span data-ttu-id="f3a31-182">**バッチ ステータス** - この検証は、バッチが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-182">**Batch status** – This validation checks whether the batch was successful.</span></span>
- <span data-ttu-id="f3a31-183">**メッセージ状態** – テストが統合に関するものである場合、メッセージの状態が検証されます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-183">**Message status** – If the test is about integrations, the message status is validated.</span></span>
- <span data-ttu-id="f3a31-184">**切り捨て** – 切り捨てが有効になっている場合は、この検証が切り捨てが発生したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-184">**Truncation** – If truncation is enabled, this validation checks whether truncation occurred.</span></span>
- <span data-ttu-id="f3a31-185">**ステージングのスキップ** – **ステージングのスキップ** がテストで有効になっている場合、ステージングがスキップされたかどうかをこの検証でチェックします。</span><span class="sxs-lookup"><span data-stu-id="f3a31-185">**Skip staging** – If **Skip staging** is enabled on a test, this validation checks whether staging was skipped.</span></span>

## <a name="example-1-configuration-management-for-data-projects"></a><span data-ttu-id="f3a31-186">例 1: データ プロジェクトの構成管理</span><span class="sxs-lookup"><span data-stu-id="f3a31-186">Example 1: Configuration management for data projects</span></span>
<span data-ttu-id="f3a31-187">**\<ConfigurationOnly\>** 要素は、データ プロジェクトおよび定期的なスケジュールの構成タスクを作成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-187">The **\<ConfigurationOnly\>** element can be used to create configuration tasks for data projects and recurring schedules.</span></span>

<span data-ttu-id="f3a31-188">この最初の例は、定期的なスケジュールを持たないデータ プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="f3a31-188">This first example configures a data project that doesn't have a recurring schedule.</span></span> <span data-ttu-id="f3a31-189">2 番目の例には、定期的なスケジュールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3a31-189">The second example includes a recurring schedule.</span></span> <span data-ttu-id="f3a31-190">違いは、**\<Operation\>** 要素の値です。</span><span class="sxs-lookup"><span data-stu-id="f3a31-190">The difference is the value of the **\<Operation\>** element.</span></span> <span data-ttu-id="f3a31-191">構成タスクのマニフェストは、ソース コントロール下にも保管する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3a31-191">Manifests for configuration tasks should also be kept under source control.</span></span>

```
<?xml version='1.0' encoding='utf-8'?>
<TestManifest name='Data management demo data set up'>
    <SharedSetup>
        <DataFile ID='SharedSetup' name='Demo data-7.3-100-System and Shared'  assetType='Data package' lcsProjectId=''/>
        <DataFile ID='FinancialsHQUS' name='Demo data-7.3-200-Financials-HQUS' assetType='Data package' lcsProjectId=''/>
        <DataFile ID='FinancialsPICH' name='Demo data-7.3-200-Financials-PICH' assetType='Data package' lcsProjectId=''/>
        <DataFile ID='FinancialsPIFB' name='Demo data-7.3-200-Financials-PIFB' assetType='Data package' lcsProjectId=''/>

        <JobDefinition ID='ImportJobDefinition_1'>
            <ConfigurationOnly>Yes</ConfigurationOnly>
            <Operation>Import</Operation>
            <SkipStaging>No</SkipStaging>
            <Truncate>No</Truncate>
            <Mode>Import async</Mode>
            <BatchFrequencyInMinutes>1</BatchFrequencyInMinutes>
            <NumberOfTimesToRunBatch >2</NumberOfTimesToRunBatch>
            <UploadFrequencyInSeconds>1</UploadFrequencyInSeconds>
            <TotalNumberOfTimesToUploadFile>1</TotalNumberOfTimesToUploadFile>
            <SupportedDataSourceType>Package</SupportedDataSourceType>
            <ProcessMessagesInOrder>No</ProcessMessagesInOrder>
            <PreventUploadWhenZeroRecords>No</PreventUploadWhenZeroRecords>
            <UseCompanyFromMessage>Yes</UseCompanyFromMessage>
            <LegalEntity>DAT</LegalEntity>
        </JobDefinition>

        <EntitySetup ID='Generic'>
            <Entity name='*'>
                <SourceDataFormatName>Package</SourceDataFormatName>
                <ChangeTracking>No</ChangeTracking>
                <PublishToBYOD>No</PublishToBYOD>
                <DefaultRefreshType>Full push only</DefaultRefreshType>
                <ExcelWorkSheetName></ExcelWorkSheetName>
                <SelectFields>All fields</SelectFields>
                <SetBasedProcessing>No</SetBasedProcessing>
                <FailBatchOnErrorForExecutionUnit>No</FailBatchOnErrorForExecutionUnit>
                <FailBatchOnErrorForLevel>No</FailBatchOnErrorForLevel>
                <FailBatchOnErrorForSequence>No</FailBatchOnErrorForSequence>
                <ParallelProcessing>
                    <Threshold></Threshold>
                    <TaskCount></TaskCount>
                </ParallelProcessing>
            </Entity>
        </EntitySetup>
    </SharedSetup>

    <TestGroup name='Set up import jobs for Financials'>
        <TestCase Title='Set up import job for shared set up data package' ID='3933885' RepeatCount='1' TraceParser='off' TimeOut='20'>
            <DataFile RefID='SharedSetup' />
            <JobDefinition RefID='ImportJobDefinition_1' />
            <EntitySetup RefID='Generic' />
        </TestCase>

        <TestCase Title='Set up import job for financials HQUS' ID='3933886' RepeatCount='1' TraceParser='off' TimeOut='20'>
            <DataFile RefID='FinancialsHQUS' />
                <JobDefinition RefID='ImportJobDefinition_1'>
                    <LegalEntity>HQUS</LegalEntity>
                </JobDefinition>
                <EntitySetup RefID='Generic' />
        </TestCase>

        <TestCase Title='Set up import job for financials PICH' ID='3933887' RepeatCount='1' TraceParser='off' TimeOut='20'>
            <DataFile RefID='FinancialsPICH' />
                <JobDefinition RefID='ImportJobDefinition_1'>
                    <LegalEntity>PICH</LegalEntity>
                </JobDefinition>
                <EntitySetup RefID='Generic' />
        </TestCase>

        <TestCase Title='Set up import job for financials PIFB' ID='3933888' RepeatCount='1' TraceParser='off' TimeOut='20'>
            <DataFile RefID='FinancialsPIFB' />
                <JobDefinition RefID='ImportJobDefinition_1'>
                    <LegalEntity>PIFB</LegalEntity>
                </JobDefinition>
                <EntitySetup RefID='Generic' />
        </TestCase>
    </TestGroup>
</TestManifest>
```

## <a name="example-2-automated-setup-of-demo-data"></a><span data-ttu-id="f3a31-192">例 2: デモ データの自動設定</span><span class="sxs-lookup"><span data-stu-id="f3a31-192">Example 2: Automated setup of demo data</span></span>
<span data-ttu-id="f3a31-193">次のマニフェストは、デモ データ パッケージが共有アセット ライブラリに格納されている場合の 3 つの法人のデモ データの設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="f3a31-193">The following manifest shows the setup of demo data for three legal entities when the demo data packages are stored in the Shared asset library.</span></span>

```
<?xml version='1.0' encoding='utf-8'?>
<TestManifest name='Data management demo data set up'>
    <SharedSetup>
        <DataFile ID='SharedSetup' name='Demo data-7.3-100-System and Shared'  assetType='Data package' lcsProjectId=''/>
        <DataFile ID='FinancialsHQUS' name='Demo data-7.3-200-Financials-HQUS' assetType='Data package' lcsProjectId=''/>
        <DataFile ID='FinancialsPICH' name='Demo data-7.3-200-Financials-PICH' assetType='Data package' lcsProjectId=''/>
        <DataFile ID='FinancialsPIFB' name='Demo data-7.3-200-Financials-PIFB' assetType='Data package' lcsProjectId=''/>

        <JobDefinition ID='ImportJobDefinition_1'>
                <Operation>Import</Operation>
                <SkipStaging></SkipStaging>
                <Truncate></Truncate>
                <Mode>Import async</Mode>
                <BatchFrequencyInMinutes>1</BatchFrequencyInMinutes>
                <NumberOfTimesToRunBatch >2</NumberOfTimesToRunBatch>
                <UploadFrequencyInSeconds>1</UploadFrequencyInSeconds>
                <TotalNumberOfTimesToUploadFile>1</TotalNumberOfTimesToUploadFile>
                <SupportedDataSourceType>Package</SupportedDataSourceType>
                <ProcessMessagesInOrder>No</ProcessMessagesInOrder>
                <PreventUploadWhenZeroRecords>No</PreventUploadWhenZeroRecords>
                <UseCompanyFromMessage>Yes</UseCompanyFromMessage>
                <LegalEntity>DAT</LegalEntity>
        </JobDefinition>

        <EntitySetup ID='Generic'>
            <Entity name='*'>
                <SourceDataFormatName>Package</SourceDataFormatName>
                <ChangeTracking></ChangeTracking>
                <PublishToBYOD></PublishToBYOD>
                <DefaultRefreshType>Full push only</DefaultRefreshType>
                <ExcelWorkSheetName></ExcelWorkSheetName>
                <SelectFields>All fields</SelectFields>
                <SetBasedProcessing></SetBasedProcessing>
                <FailBatchOnErrorForExecutionUnit>No</FailBatchOnErrorForExecutionUnit>
                <FailBatchOnErrorForLevel>No</FailBatchOnErrorForLevel>
                <FailBatchOnErrorForSequence>No</FailBatchOnErrorForSequence>
                <ParallelProcessing>
                    <Threshold></Threshold>
                    <TaskCount></TaskCount>
                </ParallelProcessing>
            </Entity>
        </EntitySetup>
    </SharedSetup>

    <TestGroup name='Set up Financials'>
        <TestCase Title='Import shared set up data package' ID='3933885' RepeatCount='1' TraceParser='off' TimeOut='20'>
            <DataFile RefID='SharedSetup' />
            <JobDefinition RefID='ImportJobDefinition_1' />
            <EntitySetup RefID='Generic' />
        </TestCase>

        <TestCase Title='Import financials for HQUS' ID='3933886' RepeatCount='1' TraceParser='off' TimeOut='20'>
            <DataFile RefID='FinancialsHQUS' />
            <JobDefinition RefID='ImportJobDefinition_1'>
                <LegalEntity>HQUS</LegalEntity>
            </JobDefinition>
            <EntitySetup RefID='Generic' />
        </TestCase>

        <TestCase Title='Import financials for PICH' ID='3933887' RepeatCount='1' TraceParser='off' TimeOut='20'>
            <DataFile RefID='FinancialsPICH' />
            <JobDefinition RefID='ImportJobDefinition_1'>
                <LegalEntity>PICH</LegalEntity>
            </JobDefinition>
            <EntitySetup RefID='Generic' />
        </TestCase>

        <TestCase Title='Import financials for PIFB' ID='3933888' RepeatCount='1' TraceParser='off' TimeOut='20'>
            <DataFile RefID='FinancialsPIFB' />
            <JobDefinition RefID='ImportJobDefinition_1'>
                <LegalEntity>PIFB</LegalEntity>
            </JobDefinition>
            <EntitySetup RefID='Generic' />
        </TestCase>
    </TestGroup>
</TestManifest>
```

