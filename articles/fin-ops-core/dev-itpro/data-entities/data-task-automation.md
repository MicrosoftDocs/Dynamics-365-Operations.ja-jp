---
title: データ タスクの自動化
description: このトピックでは、Finance and Operations におけるデータ タスクの自動化により、さまざまな種類のデータ タスクを簡単に繰り返し、各タスクの結果を検証する方法を説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform update 16
ms.openlocfilehash: ccfef0da2ebaf932c0e6ca70f8d47c9d53abc1d6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191540"
---
# <a name="data-task-automation"></a><span data-ttu-id="efee9-103">データ タスクの自動化</span><span class="sxs-lookup"><span data-stu-id="efee9-103">Data task automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="efee9-104">データ タスクの自動化により、さまざまな種類のデータ タスクを簡単に繰り返し、各タスクの結果を検証することができます。</span><span class="sxs-lookup"><span data-stu-id="efee9-104">Data task automation lets you easily repeat many types of data tasks and validate the outcome of each task.</span></span> <span data-ttu-id="efee9-105">データ タスクの自動化は、実装フェーズにあるプロジェクトで非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="efee9-105">Data task automation is very useful for projects that are in the implementation phase.</span></span> <span data-ttu-id="efee9-106">たとえば、データ プロジェクトの作成およびコンフィギュレーションを自動化することができます。</span><span class="sxs-lookup"><span data-stu-id="efee9-106">For example, you can automate the creation and configuration of data projects.</span></span> <span data-ttu-id="efee9-107">また、デモ データおよび高品質の構成データ、およびデータ移行に関連する他のタスクなどの、インポート/エクスポート オペレーションの実行を構成およびトリガーすることができます。</span><span class="sxs-lookup"><span data-stu-id="efee9-107">You can also configure and trigger the execution of import/export operations, such as the setup of demo data and golden configuration data, and other tasks that are related to data migration.</span></span> <span data-ttu-id="efee9-108">また、タスクの結果の検証を使用して、データ エンティティの自動テストを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="efee9-108">You can also create automated testing of data entities by using task outcome validation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="efee9-109">現時点では、オンプレミス環境ではデータ タスクの自動化はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="efee9-109">Data task automation isn't currently supported for on-premises environments.</span></span>

> <span data-ttu-id="efee9-110">データタスクの自動化を実行するユーザーは、アプリケーションの環境および LCS プロジェクトと同じテナントに存在するユーザーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-110">The user who executes data task automation must be in the same tenant as the application environment and LCS project.</span></span>

<span data-ttu-id="efee9-111">データ タスクの自動化のために次の方法をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="efee9-111">We recommend the following approach for data task automation.</span></span>

1. <span data-ttu-id="efee9-112">自動化の恩恵を受けるデータ関連のタスクを特定する。</span><span class="sxs-lookup"><span data-stu-id="efee9-112">Identify the data-related tasks that will benefit from automation.</span></span>

    <span data-ttu-id="efee9-113">実装チームは自分たちの構成管理計画とデータ移行計画をレビューして、自動化のための潜在的なデータ タスクを識別すること、またデータ エンティティのテスト ケースも識別することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="efee9-113">We recommend that implementation teams review their configuration management plan and data migration plan to identify potential data tasks for automation, and also to identify data entity test cases.</span></span>

2. <span data-ttu-id="efee9-114">タスクを定義します。</span><span class="sxs-lookup"><span data-stu-id="efee9-114">Define tasks.</span></span>

    <span data-ttu-id="efee9-115">タスクは、XML マニフェストで定義されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-115">Tasks are defined in an XML manifest.</span></span> <span data-ttu-id="efee9-116">アプリケーション ライフ サイクルの管理 (ALM) 戦略では、構成管理の一部としてソース管理下のマニフェストを保持することができます。</span><span class="sxs-lookup"><span data-stu-id="efee9-116">You can keep your manifest under source control as part of configuration management in your application lifecycle management (ALM) strategy.</span></span>

3. <span data-ttu-id="efee9-117">Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリに、データ タスクの自動化に関連するデータ パッケージを配置します。</span><span class="sxs-lookup"><span data-stu-id="efee9-117">Put the data packages that are related to data task automation in the Shared asset library of Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="efee9-118">また、必要に応じて特定の LCS プロジェクトを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="efee9-118">You can also use a specific LCS project as you require.</span></span>

    <span data-ttu-id="efee9-119">データ タスク自動化マネージャは、LCS プロジェクトに関連するサンドボックスまたは実稼動環境からパッケージを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="efee9-119">Data task automation manager can consume packages from any sandbox and/or production environment that is related to the LCS project.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="efee9-120">データ タスク自動化マネージャーを実行するユーザー アカウントは、LCS およびデータ パッケージのマニフェストで参照される LCS プロジェクトにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-120">The user account that runs Data task automation manager must have access to LCS and to the LCS project that is referenced in the manifest for data packages.</span></span>
    > - <span data-ttu-id="efee9-121">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合アプリケーション プログラミング インターフェイス (API) を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="efee9-121">Although data task automation can be run in any environment in the cloud, we strongly recommend that you not run any import/export tasks that use integration application programming interfaces (APIs) in a production environment.</span></span> <span data-ttu-id="efee9-122">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-122">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

4. <span data-ttu-id="efee9-123">データ タスクを実行し、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="efee9-123">Run the data tasks, and then review the outcomes.</span></span>

    <span data-ttu-id="efee9-124">データ タスク自動化マネージャは、各タスクの成功または失敗の結果を提供します。</span><span class="sxs-lookup"><span data-stu-id="efee9-124">Data task automation manager provides the success or failure outcome for each task.</span></span> <span data-ttu-id="efee9-125">また、タスクが失敗した理由に関する見解も提供します。</span><span class="sxs-lookup"><span data-stu-id="efee9-125">It also provides insights into the reason why a task failed.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="efee9-126">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合 API を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="efee9-126">Although data task automation can be run in any environments in the cloud, we recommend that you not run any import/export tasks that use integration APIs in a production environment.</span></span> <span data-ttu-id="efee9-127">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-127">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

<span data-ttu-id="efee9-128">次のビデオは、Data Task Automation Manager の初期リリースを紹介する TechTalk の 55 分です。[タスク自動化フレームワーク](https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4)。</span><span class="sxs-lookup"><span data-stu-id="efee9-128">The following video is a 55-minute TechTalk that walks you through an early release of Data task automation manager: [Task automation framework](https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4).</span></span>

## <a name="task-manifest"></a><span data-ttu-id="efee9-129">タスク マニフェスト</span><span class="sxs-lookup"><span data-stu-id="efee9-129">Task manifest</span></span>
<span data-ttu-id="efee9-130">タスクは、XML マニフェストで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-130">A task must be defined in an XML manifest.</span></span> <span data-ttu-id="efee9-131">このセクションでは、マニフェストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="efee9-131">This section describes the manifest.</span></span> <span data-ttu-id="efee9-132">マニフェストを名前付けしデザインする方法の指針については、このトピックの後半の、「マニフェストのデザインに対するベスト プラクティス」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="efee9-132">For guidance about how to name and design the manifest, see the "Best practices for manifest design" section later in this topic.</span></span>

### <a name="manifest-root"></a><span data-ttu-id="efee9-133">マニフェスト ルート</span><span class="sxs-lookup"><span data-stu-id="efee9-133">Manifest root</span></span>
<span data-ttu-id="efee9-134">**\<TestManifest\>** 要素は、マニフェストのルートです。</span><span class="sxs-lookup"><span data-stu-id="efee9-134">The **\<TestManifest\>** element is the root of the manifest.</span></span> <span data-ttu-id="efee9-135">その他のすべての要素はこの要素の子です。</span><span class="sxs-lookup"><span data-stu-id="efee9-135">All other elements are children of this element.</span></span>

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

| <span data-ttu-id="efee9-136">要素</span><span class="sxs-lookup"><span data-stu-id="efee9-136">Element</span></span>          | <span data-ttu-id="efee9-137">要素の基数</span><span class="sxs-lookup"><span data-stu-id="efee9-137">Element Cardinality</span></span> | <span data-ttu-id="efee9-138">属性</span><span class="sxs-lookup"><span data-stu-id="efee9-138">Attributes</span></span> | <span data-ttu-id="efee9-139">属性の説明</span><span class="sxs-lookup"><span data-stu-id="efee9-139">Attribute description</span></span>                                     |
|------------------|---------------------|------------|-----------------------------------------------------------|
| <span data-ttu-id="efee9-140">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="efee9-140">\<TestManifest\></span></span> | <span data-ttu-id="efee9-141">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-141">1..1</span></span>                | <span data-ttu-id="efee9-142">名前</span><span class="sxs-lookup"><span data-stu-id="efee9-142">name</span></span>       | <span data-ttu-id="efee9-143">*名前*はマニフェストの目的を識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="efee9-143">The *name* helps to identify the purpose of the manifest.</span></span> |

### <a name="shared-setup"></a><span data-ttu-id="efee9-144">共有された設定</span><span class="sxs-lookup"><span data-stu-id="efee9-144">Shared setup</span></span>
<span data-ttu-id="efee9-145">**共有セットアップ** セクションは、全般的なタスクのパラメーターとマニフェスト内のすべてのタスクの動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="efee9-145">The **Shared setup** section defines general task parameters and behaviors for all tasks in the manifest.</span></span>

| <span data-ttu-id="efee9-146">親要素</span><span class="sxs-lookup"><span data-stu-id="efee9-146">Parent element</span></span>   | <span data-ttu-id="efee9-147">要素</span><span class="sxs-lookup"><span data-stu-id="efee9-147">Element</span></span>         | <span data-ttu-id="efee9-148">要素の基数</span><span class="sxs-lookup"><span data-stu-id="efee9-148">Element Cardinality</span></span> | <span data-ttu-id="efee9-149">属性</span><span class="sxs-lookup"><span data-stu-id="efee9-149">Attributes</span></span> | <span data-ttu-id="efee9-150">属性の説明</span><span class="sxs-lookup"><span data-stu-id="efee9-150">Attribute description</span></span>            |
|------------------|-----------------|---------------------|------------|----------------------------------|
| <span data-ttu-id="efee9-151">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="efee9-151">\<TestManifest\></span></span> | <span data-ttu-id="efee9-152">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="efee9-152">\<SharedSetup\></span></span> | <span data-ttu-id="efee9-153">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-153">1..1</span></span>                | \-         | <span data-ttu-id="efee9-154">この要素には属性はありません。</span><span class="sxs-lookup"><span data-stu-id="efee9-154">This element takes no attributes.</span></span> |

### <a name="data-files"></a><span data-ttu-id="efee9-155">データ ファイル</span><span class="sxs-lookup"><span data-stu-id="efee9-155">Data files</span></span>
<span data-ttu-id="efee9-156">**\<DataFile\>** 要素は、マニフェスト内のタスクが使用するデータ パッケージとデータ ファイルを定義します。</span><span class="sxs-lookup"><span data-stu-id="efee9-156">**\<DataFile\>** elements define the data packages and data files that the tasks in the manifest will use.</span></span> <span data-ttu-id="efee9-157">データ ファイルは、LCS プロジェクトの LCS アセット ライブラリまたは共有アセット ライブラリのいずれかになければなりません。</span><span class="sxs-lookup"><span data-stu-id="efee9-157">The data files must be either in the LCS asset library of your LCS project or in the Shared asset library.</span></span>

```
<DataFile ID='SharedSetup' name='Demo data-7.3-100-System and Shared'  assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsHQUS' name='Demo data-7.3-200-Financials-HQUS' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPICH' name='Demo data-7.3-200-Financials-PICH' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPIFB' name='Demo data-7.3-200-Financials-PIFB' assetType='Data package' lcsProjectId=''/>
```

| <span data-ttu-id="efee9-158">親要素</span><span class="sxs-lookup"><span data-stu-id="efee9-158">Parent element</span></span>  | <span data-ttu-id="efee9-159">要素</span><span class="sxs-lookup"><span data-stu-id="efee9-159">Element</span></span>      | <span data-ttu-id="efee9-160">要素の基数</span><span class="sxs-lookup"><span data-stu-id="efee9-160">Element Cardinality</span></span> | <span data-ttu-id="efee9-161">属性</span><span class="sxs-lookup"><span data-stu-id="efee9-161">Attributes</span></span>   | <span data-ttu-id="efee9-162">属性の説明</span><span class="sxs-lookup"><span data-stu-id="efee9-162">Attribute description</span></span> |
|-----------------|--------------|---------------------|--------------|-----------------------|
| <span data-ttu-id="efee9-163">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="efee9-163">\<SharedSetup\></span></span> | <span data-ttu-id="efee9-164">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="efee9-164">\<DataFile\></span></span> | <span data-ttu-id="efee9-165">1..n</span><span class="sxs-lookup"><span data-stu-id="efee9-165">1..n</span></span>                | \-           | \- |
|                 | <span data-ttu-id="efee9-166">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="efee9-166">\<DataFile\></span></span> | \-                  | <span data-ttu-id="efee9-167">ID</span><span class="sxs-lookup"><span data-stu-id="efee9-167">ID</span></span>           | |
|                 | <span data-ttu-id="efee9-168">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="efee9-168">\<DataFile\></span></span> | \-                  | <span data-ttu-id="efee9-169">名前</span><span class="sxs-lookup"><span data-stu-id="efee9-169">name</span></span>         | <span data-ttu-id="efee9-170">データ ファイルを表す資産の名前。</span><span class="sxs-lookup"><span data-stu-id="efee9-170">Name of the asset that represents the data file.</span></span> |
|                 | <span data-ttu-id="efee9-171">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="efee9-171">\<DataFile\></span></span> | \-                  | <span data-ttu-id="efee9-172">assetType</span><span class="sxs-lookup"><span data-stu-id="efee9-172">assetType</span></span>    | <span data-ttu-id="efee9-173">データ ファイルを格納する LCS 資産ライブラリでの資産タイプ。</span><span class="sxs-lookup"><span data-stu-id="efee9-173">The asset type in LCS asset library that stores the data file.</span></span> <span data-ttu-id="efee9-174">これは、LCS アセット ライブラリで示されたように、アセット タイプの名前です。</span><span class="sxs-lookup"><span data-stu-id="efee9-174">This is the asset type name as shown in LCS asset library.</span></span> |
|                 | <span data-ttu-id="efee9-175">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="efee9-175">\<DataFile\></span></span> | \-                  | <span data-ttu-id="efee9-176">lcsProjectId</span><span class="sxs-lookup"><span data-stu-id="efee9-176">lcsProjectId</span></span> | <span data-ttu-id="efee9-177">その資産ライブラリで LCS プロジェクトにはデータ ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="efee9-177">The LCS project that has the data file in its asset library.</span></span> <span data-ttu-id="efee9-178">プロジェクト ID が " として指定されている場合は、共有アセット ライブラリを示します。</span><span class="sxs-lookup"><span data-stu-id="efee9-178">If the project ID is specified as '' then, it indicates the Shared asset library.</span></span> |

### <a name="data-project-definition"></a><span data-ttu-id="efee9-179">データ プロジェクト定義</span><span class="sxs-lookup"><span data-stu-id="efee9-179">Data project definition</span></span>
<span data-ttu-id="efee9-180">**\<JobDefinition\>** 要素は、データ プロジェクト定義を定義します。</span><span class="sxs-lookup"><span data-stu-id="efee9-180">The **\<JobDefinition\>** element defines the data project definition.</span></span> <span data-ttu-id="efee9-181">マニフェストには複数のジョブ定義があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-181">There can be more than one job definition in a manifest.</span></span>

```
<JobDefinition ID='ImportJobDefinition_1'>
    <Operation>Import</Operation>
    <ConfigurationOnly>No</ConfigurationOnly>
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
    <PackageAPIExecute>true</PackageAPIExecute>
    <PackageAPIOverwrite>false</PackageAPIOverwrite>
    <PackageAPIReexecute>false</PackageAPIReexecute>
    <DefinitionGroupID>TestExport</DefinitionGroupID>
    <PackageName>TestExportPackage</PackageName>
</JobDefinition>
```

| <span data-ttu-id="efee9-182">親要素</span><span class="sxs-lookup"><span data-stu-id="efee9-182">Parent element</span></span>    | <span data-ttu-id="efee9-183">要素</span><span class="sxs-lookup"><span data-stu-id="efee9-183">Element</span></span>                          | <span data-ttu-id="efee9-184">要素の基数</span><span class="sxs-lookup"><span data-stu-id="efee9-184">Element cardinality</span></span> | <span data-ttu-id="efee9-185">属性</span><span class="sxs-lookup"><span data-stu-id="efee9-185">Attribute</span></span> | <span data-ttu-id="efee9-186">説明</span><span class="sxs-lookup"><span data-stu-id="efee9-186">Description</span></span> |
|-------------------|----------------------------------|---------------------|-----------|-------------|
| <span data-ttu-id="efee9-187">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="efee9-187">\<SharedSetup\></span></span>   | <span data-ttu-id="efee9-188">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="efee9-188">\<JobDefinition\></span></span>                | <span data-ttu-id="efee9-189">1..n</span><span class="sxs-lookup"><span data-stu-id="efee9-189">1..n</span></span>                | <span data-ttu-id="efee9-190">ID</span><span class="sxs-lookup"><span data-stu-id="efee9-190">ID</span></span>        | <span data-ttu-id="efee9-191">タスクでジョブ定義 ID を使用してデータ プロジェクトで使用する定義を参照できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-191">The job definition ID is used in the tasks to reference the definition to be used for the data project.</span></span> |
| <span data-ttu-id="efee9-192">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="efee9-192">\<JobDefinition\></span></span> | <span data-ttu-id="efee9-193">[\<操作\>]</span><span class="sxs-lookup"><span data-stu-id="efee9-193">\<Operation\></span></span>                    | <span data-ttu-id="efee9-194">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-194">1..1</span></span>                | \-        | <span data-ttu-id="efee9-195">実行される操作は、次の値によって指定されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-195">The operation to be performed is specified by the following values:</span></span> <br> <span data-ttu-id="efee9-196">- インポート</span><span class="sxs-lookup"><span data-stu-id="efee9-196">- Import</span></span> <br> <span data-ttu-id="efee9-197">- エクスポート</span><span class="sxs-lookup"><span data-stu-id="efee9-197">- Export</span></span> |
|                   | <span data-ttu-id="efee9-198">\<切り詰め\></span><span class="sxs-lookup"><span data-stu-id="efee9-198">\<Truncate\></span></span>                     | <span data-ttu-id="efee9-199">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-199">1..1</span></span>                | \-        | <span data-ttu-id="efee9-200">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-200">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="efee9-201">これは操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-201">This is applicable only when operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="efee9-202">\<モード\></span><span class="sxs-lookup"><span data-stu-id="efee9-202">\<Mode\></span></span>                         | <span data-ttu-id="efee9-203">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-203">1..1</span></span>                | \-        | <span data-ttu-id="efee9-204">モードでは、操作を実行する必要があるメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="efee9-204">The mode specifies the method using which the operation must be performed.</span></span> <span data-ttu-id="efee9-205">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="efee9-205">The possible values are:</span></span><br><span data-ttu-id="efee9-206">- 非同期インポート</span><span class="sxs-lookup"><span data-stu-id="efee9-206">- Import async</span></span> <br><span data-ttu-id="efee9-207">- 非同期エクスポート</span><span class="sxs-lookup"><span data-stu-id="efee9-207">- Export async</span></span> <br><span data-ttu-id="efee9-208">- 定期的に実行するバッチ: エンキュー API を使用します。</span><span class="sxs-lookup"><span data-stu-id="efee9-208">- Recurring batch: This uses the enqueue API.</span></span> <span data-ttu-id="efee9-209">デキュー API には現在対応していません。</span><span class="sxs-lookup"><span data-stu-id="efee9-209">Dequeue API is not supported yet.</span></span> <span data-ttu-id="efee9-210">パッケージAPIは、エクスポートとインポートの両方に対応しています。</span><span class="sxs-lookup"><span data-stu-id="efee9-210">Package API supports both export and import.</span></span>|
|                   | <span data-ttu-id="efee9-211">\<ConfigurationOnly\></span><span class="sxs-lookup"><span data-stu-id="efee9-211">\<ConfigurationOnly\></span></span>            | <span data-ttu-id="efee9-212">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-212">1..1</span></span>                | \-        | <span data-ttu-id="efee9-213">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-213">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="efee9-214">タスクがデータ プロジェクトをコンフィギュレーションするのみで、指定された操作を実行しない場合は、はいに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-214">This must be set to Yes if the task is only to configure the data project but not to perform the specified operation.</span></span> |
|                   | <span data-ttu-id="efee9-215">\<BatchFrequencyInMinutes\></span><span class="sxs-lookup"><span data-stu-id="efee9-215">\<BatchFrequencyInMinutes\></span></span>      | <span data-ttu-id="efee9-216">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-216">1..1</span></span>                | \-        | <span data-ttu-id="efee9-217">バッチがスケジュール設定される頻度を指定します。</span><span class="sxs-lookup"><span data-stu-id="efee9-217">This specifies the frequency in which the batch must be scheduled.</span></span> <span data-ttu-id="efee9-218">これはモードが*定期実行されるバッチ*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-218">This is applicable only when mode is set to *recurring batch*.</span></span> |
|                   | <span data-ttu-id="efee9-219">\<NumberOfTimesToRunBatch\></span><span class="sxs-lookup"><span data-stu-id="efee9-219">\<NumberOfTimesToRunBatch\></span></span>      | <span data-ttu-id="efee9-220">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-220">1..1</span></span>                | \-        | <span data-ttu-id="efee9-221">これは、スケジュールされているバッチを実行する回数の制限を設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-221">This is used to set a limit to how many times the scheduled batch should run.</span></span> <span data-ttu-id="efee9-222">これはモードが*定期実行されるバッチ*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-222">This is applicable only when mode is set to *recurring batch*.</span></span> |
|                   | <span data-ttu-id="efee9-223">\<UploadFrequencyInSeconds\></span><span class="sxs-lookup"><span data-stu-id="efee9-223">\<UploadFrequencyInSeconds\></span></span>     | <span data-ttu-id="efee9-224">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-224">1..1</span></span>                | \-        | <span data-ttu-id="efee9-225">これは、インポートする定期バッチ ジョブにファイルをアップロードする頻度を制御するために使用します。</span><span class="sxs-lookup"><span data-stu-id="efee9-225">This is used to control the rate at which a file is uploaded to the recurring batch job for import.</span></span> <span data-ttu-id="efee9-226">これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-226">This must be used only for automated testing of recurring integrations in non-production environments.</span></span> <span data-ttu-id="efee9-227">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-227">This is applicable only when mode is set to *recurring batch* and operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="efee9-228">\<TotalNumberOfTimesToUpload\></span><span class="sxs-lookup"><span data-stu-id="efee9-228">\<TotalNumberOfTimesToUpload\></span></span>   | <span data-ttu-id="efee9-229">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-229">1..1</span></span>                |           | <span data-ttu-id="efee9-230">これはファイルを繰り返しバッチにアップロードする総回数を制御します。</span><span class="sxs-lookup"><span data-stu-id="efee9-230">This controls the total number of times the file should be uploaded to the recurring batch.</span></span> <span data-ttu-id="efee9-231">これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-231">This must be used only for automated testing of recurring integrations in non-production environments.</span></span> <span data-ttu-id="efee9-232">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-232">This is applicable only when mode is set to *recurring batch* and operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="efee9-233">\<SupportedDataSoureType\></span><span class="sxs-lookup"><span data-stu-id="efee9-233">\<SupportedDataSoureType\></span></span>       | <span data-ttu-id="efee9-234">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-234">1..1</span></span>                |           | <span data-ttu-id="efee9-235">ファイルが定期的なバッチまたはパッケージに送信中であるかどうかを指定するために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-235">This must be used to specify if a file is being sent to the recurring batch or a package.</span></span> <span data-ttu-id="efee9-236">これはモードが「定期実行されるバッチ」に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-236">This is only applicable when mode is set to 'recurring batch'.</span></span> |
|                   | <span data-ttu-id="efee9-237">\<ProcessMessagesInOrder\></span><span class="sxs-lookup"><span data-stu-id="efee9-237">\<ProcessMessagesInOrder\></span></span>       | <span data-ttu-id="efee9-238">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-238">1..1</span></span>                |           | <span data-ttu-id="efee9-239">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-239">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="efee9-240">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-240">This is applicable only when mode is set to *recurring batch* and operation is *Import*.</span></span> |
|                   | <span data-ttu-id="efee9-241">\<PreventUploadWhenZeroRecords\></span><span class="sxs-lookup"><span data-stu-id="efee9-241">\<PreventUploadWhenZeroRecords\></span></span> | <span data-ttu-id="efee9-242">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-242">1..1</span></span>                |           | <span data-ttu-id="efee9-243">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-243">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="efee9-244">これはモードが*定期実行されるバッチ*に設定されており、操作が*エクスポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-244">This is applicable only when mode is set to *recurring batch* and operation is *Export*.</span></span> |
|                   | <span data-ttu-id="efee9-245">\<UseCompanyFromMessage\></span><span class="sxs-lookup"><span data-stu-id="efee9-245">\<UseCompanyFromMessage\></span></span>        | <span data-ttu-id="efee9-246">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-246">1..1</span></span>                |           | <span data-ttu-id="efee9-247">これははい、またはいいえに設定できるブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-247">This is a Boolean field which can be set to Yes or No.</span></span> <span data-ttu-id="efee9-248">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-248">This is applicable only when mode is set to *recurring batch* and operation is *Import*.</span></span> |
|                   | <span data-ttu-id="efee9-249">\<LegalEntity\></span><span class="sxs-lookup"><span data-stu-id="efee9-249">\<LegalEntity\></span></span>                  | <span data-ttu-id="efee9-250">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-250">1..1</span></span>                |           | <span data-ttu-id="efee9-251">これをは、インポート/エクスポート ジョブを実行する必要がある法人を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-251">This is used to specify the legal entity in which the import/export job must be executed.</span></span> |
|                   | <span data-ttu-id="efee9-252">\<PackageAPIExecute\></span><span class="sxs-lookup"><span data-stu-id="efee9-252">\<PackageAPIExecute\></span></span>            | <span data-ttu-id="efee9-253">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-253">1..1</span></span>                |           | <span data-ttu-id="efee9-254">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="efee9-254">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="efee9-255">これは、"true" または "false" を取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-255">This is a Boolean field which takes 'true' or 'false'.</span></span> |
|                   | <span data-ttu-id="efee9-256">\<PackageAPIOverwrite\></span><span class="sxs-lookup"><span data-stu-id="efee9-256">\<PackageAPIOverwrite\></span></span>            | <span data-ttu-id="efee9-257">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-257">1..1</span></span>                |           | <span data-ttu-id="efee9-258">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="efee9-258">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="efee9-259">これは、"true" または "false" を取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-259">This is a Boolean field which takes 'true' or 'false'.</span></span> |
|                   | <span data-ttu-id="efee9-260">\<PackageAPIReexecute\></span><span class="sxs-lookup"><span data-stu-id="efee9-260">\<PackageAPIReexecute\></span></span>            | <span data-ttu-id="efee9-261">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-261">1..1</span></span>                |           | <span data-ttu-id="efee9-262">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="efee9-262">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="efee9-263">これは、"true" または "false" を取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-263">This is a Boolean field which takes 'true' or 'false'.</span></span> |
|                   | <span data-ttu-id="efee9-264">\<DefinitionGroupID\></span><span class="sxs-lookup"><span data-stu-id="efee9-264">\<DefinitionGroupID\></span></span>            | <span data-ttu-id="efee9-265">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-265">1..1</span></span>                |           | <span data-ttu-id="efee9-266">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="efee9-266">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="efee9-267">これは文字列フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-267">This is a string field.</span></span> |
|                   | <span data-ttu-id="efee9-268">\<PackageName\></span><span class="sxs-lookup"><span data-stu-id="efee9-268">\<PackageName\></span></span>            | <span data-ttu-id="efee9-269">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-269">1..1</span></span>                |           | <span data-ttu-id="efee9-270">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="efee9-270">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="efee9-271">これは文字列フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-271">This is a string field.</span></span> |

### <a name="entity-setup"></a><span data-ttu-id="efee9-272">エンティティ設定</span><span class="sxs-lookup"><span data-stu-id="efee9-272">Entity setup</span></span>
<span data-ttu-id="efee9-273">**エンティティ設定** セクションは、マニフェストのタスクが使用するエンティティの特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="efee9-273">The **Entity setup** section defines the characteristics of an entity that a task in the manifest will use.</span></span> <span data-ttu-id="efee9-274">マニフェスト内のタスクによって使用されるエンティティごとに、1 つずつ複数の定義が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-274">There can be more than one definition, one for each entity that is used by the tasks in the manifest.</span></span>

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
        <DisableEntity>No</DisableEntity>
        <SkipStaging>Yes</SkipStaging>
        <ParallelProcessing>
            <Threshold></Threshold>
            <TaskCount></TaskCount>
        </ParallelProcessing>
        <MappingDetail StagingFieldName='RoundingRulePrices' AutoGenerate='Yes' AutoDefault='No' DefaultValue='' IgnoreBlankValues='No' TextQualifier='No' UseEnumLabel='No'/>
        </Entity>
</EntitySetup>
```

| <span data-ttu-id="efee9-275">親要素</span><span class="sxs-lookup"><span data-stu-id="efee9-275">Parent element</span></span>         | <span data-ttu-id="efee9-276">要素</span><span class="sxs-lookup"><span data-stu-id="efee9-276">Element</span></span>                              | <span data-ttu-id="efee9-277">要素の基数</span><span class="sxs-lookup"><span data-stu-id="efee9-277">Element cardinality</span></span> | <span data-ttu-id="efee9-278">属性</span><span class="sxs-lookup"><span data-stu-id="efee9-278">Attribute</span></span>         | <span data-ttu-id="efee9-279">説明</span><span class="sxs-lookup"><span data-stu-id="efee9-279">Description</span></span> |
|------------------------|--------------------------------------|---------------------|-------------------|-------------|
| <span data-ttu-id="efee9-280">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="efee9-280">\<SharedSetup\></span></span>        | <span data-ttu-id="efee9-281">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="efee9-281">\<EntitySetup\></span></span>                      | <span data-ttu-id="efee9-282">1..n</span><span class="sxs-lookup"><span data-stu-id="efee9-282">1..n</span></span>                | <span data-ttu-id="efee9-283">ID</span><span class="sxs-lookup"><span data-stu-id="efee9-283">ID</span></span>                | <span data-ttu-id="efee9-284">タスクが使用するエンティティ定義を参照するために使用される ID。</span><span class="sxs-lookup"><span data-stu-id="efee9-284">An identification that will be used by tasks to reference an entity definition to be used.</span></span> |
| <span data-ttu-id="efee9-285">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="efee9-285">\<EntitySetup\></span></span>        | <span data-ttu-id="efee9-286">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="efee9-286">\<Entity\></span></span>                           | <span data-ttu-id="efee9-287">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-287">1..1</span></span>                | <span data-ttu-id="efee9-288">名前</span><span class="sxs-lookup"><span data-stu-id="efee9-288">name</span></span>              | <span data-ttu-id="efee9-289">エンティティ要素は、エンティティの名前で識別されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-289">The entity element is identified by the entity's name.</span></span> <span data-ttu-id="efee9-290">ただし、簡単なマニフェスト定義を容易にするために、この要素は \* ワイルド カードとしてもサポートしています。これは、すべてのエンティティがタスクで使用されていることを意味しています。</span><span class="sxs-lookup"><span data-stu-id="efee9-290">However, to facilitate easy manifest definition, this element also supports \* as a wild card which will mean all entities being used in a task.</span></span> <span data-ttu-id="efee9-291">これは、タスク内の何百ものエンティティを持つデータ パッケージを使用する場合に非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="efee9-291">This comes in very handy when using data packages with hundreds of entities in a task.</span></span> |
| <span data-ttu-id="efee9-292">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="efee9-292">\<Entity\></span></span>             | <span data-ttu-id="efee9-293">\<SourceDataFormatName\></span><span class="sxs-lookup"><span data-stu-id="efee9-293">\<SourceDataFormatName\></span></span>             | <span data-ttu-id="efee9-294">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-294">1..1</span></span>                | \-                | <span data-ttu-id="efee9-295">これはエンティティに使用されるファイル形式です。</span><span class="sxs-lookup"><span data-stu-id="efee9-295">This is the file format to be used for the entity.</span></span> |
|                        | <span data-ttu-id="efee9-296">\<ChangeTracking\></span><span class="sxs-lookup"><span data-stu-id="efee9-296">\<ChangeTracking\></span></span>                   | <span data-ttu-id="efee9-297">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-297">1..1</span></span>                | \-                | <span data-ttu-id="efee9-298">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-298">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="efee9-299">エンティティ全体で変更追跡を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="efee9-299">It enables or disables change tracking on the entire entity.</span></span> |
|                        | <span data-ttu-id="efee9-300">\<PublishToBYOD\></span><span class="sxs-lookup"><span data-stu-id="efee9-300">\<PublishToBYOD\></span></span>                    | <span data-ttu-id="efee9-301">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-301">1..1</span></span>                | \-                | <span data-ttu-id="efee9-302">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-302">This is a Boolean field with possible values of Yes or No.</span></span> |
|                        | <span data-ttu-id="efee9-303">\<DefaultRefreshType\></span><span class="sxs-lookup"><span data-stu-id="efee9-303">\<DefaultRefreshType\></span></span>               | <span data-ttu-id="efee9-304">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-304">1..1</span></span>                | \-                | <span data-ttu-id="efee9-305">これにより、エンティティの既定の更新頻度が設定されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-305">This sets the default refresh rate on the entity.</span></span> <span data-ttu-id="efee9-306">使用可能な値は*増分プッシュのみ*または*フル プッシュ*です。</span><span class="sxs-lookup"><span data-stu-id="efee9-306">The possible values are *Incremental push only* or *Full push*.</span></span> |
|                        | <span data-ttu-id="efee9-307">\<ExcelWorkSheetName\></span><span class="sxs-lookup"><span data-stu-id="efee9-307">\<ExcelWorkSheetName\></span></span>               | <span data-ttu-id="efee9-308">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-308">1..1</span></span>                | \-                | <span data-ttu-id="efee9-309">これはエンティティに使用するワークシートを指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-309">This is used to specify the worksheet to be used for the entity.</span></span> |
|                        | <span data-ttu-id="efee9-310">\<SelectFields\></span><span class="sxs-lookup"><span data-stu-id="efee9-310">\<SelectFields\></span></span>                     | <span data-ttu-id="efee9-311">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-311">1..1</span></span>                | \-                | <span data-ttu-id="efee9-312">これは、エクスポート操作のテンプレートに含まれるフィールドを指定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-312">This can be used to specify the fields to be included in the template for an export operation.</span></span> |
|                        | <span data-ttu-id="efee9-313">\<SetBasedProcessing\></span><span class="sxs-lookup"><span data-stu-id="efee9-313">\<SetBasedProcessing\></span></span>               | <span data-ttu-id="efee9-314">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-314">1..1</span></span>                | \-                | <span data-ttu-id="efee9-315">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-315">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="efee9-316">エンティティのセット ベースのプロセスを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-316">It is used to enable or disable set based processing on an entity.</span></span> |
|                        | <span data-ttu-id="efee9-317">\<FailBatchOnErrorForExecutionUnit\></span><span class="sxs-lookup"><span data-stu-id="efee9-317">\<FailBatchOnErrorForExecutionUnit\></span></span> | <span data-ttu-id="efee9-318">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-318">1..1</span></span>                | \-                | <span data-ttu-id="efee9-319">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-319">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="efee9-320">エンティティの実行単位レベルでエラーを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-320">It is used to enable or disable failure at execution unit level on an entity.</span></span> |
|                        | <span data-ttu-id="efee9-321">\<FailBatchOnErrorForLevel\></span><span class="sxs-lookup"><span data-stu-id="efee9-321">\<FailBatchOnErrorForLevel\></span></span>         | <span data-ttu-id="efee9-322">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-322">1..1</span></span>                | \-                | <span data-ttu-id="efee9-323">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-323">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="efee9-324">エンティティの実行レベルでエラーを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-324">It is used to enable or disable failure at execution level on an entity.</span></span> |
|                        | <span data-ttu-id="efee9-325">\<DisableEntity\></span><span class="sxs-lookup"><span data-stu-id="efee9-325">\<DisableEntity\></span></span>                    | <span data-ttu-id="efee9-326">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-326">1..1</span></span>                | \-                | <span data-ttu-id="efee9-327">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-327">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="efee9-328">データ プロジェクトでエンティティを有効化または無効化するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-328">It is used to enable or disable an entity in a data project.</span></span> |
|                        | <span data-ttu-id="efee9-329">\<SkipStaging\></span><span class="sxs-lookup"><span data-stu-id="efee9-329">\<SkipStaging\></span></span>                      | <span data-ttu-id="efee9-330">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-330">1..1</span></span>                | \-                | <span data-ttu-id="efee9-331">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-331">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="efee9-332">エクスポート中にエンティティのステージング テーブルをスキップするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-332">It is used to skip staging table for an entity during exports.</span></span> |
|                        | <span data-ttu-id="efee9-333">\<ParallelProcessing\></span><span class="sxs-lookup"><span data-stu-id="efee9-333">\<ParallelProcessing\></span></span>               | <span data-ttu-id="efee9-334">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-334">1..1</span></span>                | \-                | <span data-ttu-id="efee9-335">これは、エンティティに対して設定された並列処理を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-335">This is used to define the parallel processing set up for an entity.</span></span> <span data-ttu-id="efee9-336">タスクの始まりで既に終了する場合、タスクはこれらの設定を削除し、その実行の終わりに作成された設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="efee9-336">The task will delete these settings if already exits at the beginning of the task and it will delete the created settings at the end of its execution.</span></span> |
| <span data-ttu-id="efee9-337">\<ParallelProcessing\></span><span class="sxs-lookup"><span data-stu-id="efee9-337">\<ParallelProcessing\></span></span> | <span data-ttu-id="efee9-338">\<しきい値\></span><span class="sxs-lookup"><span data-stu-id="efee9-338">\<Threshold\></span></span>                        | <span data-ttu-id="efee9-339">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-339">1..1</span></span>                | \-                | <span data-ttu-id="efee9-340">並列処理のルールのしきい値を指定します。</span><span class="sxs-lookup"><span data-stu-id="efee9-340">This specifies the threshold for the parallel processing rule.</span></span> |
|                        | <span data-ttu-id="efee9-341">\<TaskCount\></span><span class="sxs-lookup"><span data-stu-id="efee9-341">\<TaskCount\></span></span>                        | <span data-ttu-id="efee9-342">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-342">1..1</span></span>                | \-                | <span data-ttu-id="efee9-343">これは、並列処理に使用される並列タスクの数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-343">This is used to specify the number of parallel tasks to be used for parallel processing.</span></span> |
| <span data-ttu-id="efee9-344">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="efee9-344">\<Entity\></span></span>             | <span data-ttu-id="efee9-345">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="efee9-345">\<MappingDetail\></span></span>                    | <span data-ttu-id="efee9-346">0..n</span><span class="sxs-lookup"><span data-stu-id="efee9-346">0..n</span></span>                | \-                | <span data-ttu-id="efee9-347">*自動生成*、*自動既定値*およびエンティティのマッピングで他の設定を構成できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-347">Allows to configure the *auto generate*, *auto default* and other settings on the mapping for an entity.</span></span> |
|                        | <span data-ttu-id="efee9-348">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="efee9-348">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="efee9-349">StagingFieldName</span><span class="sxs-lookup"><span data-stu-id="efee9-349">StagingFieldName</span></span>  | <span data-ttu-id="efee9-350">この属性は、設定を指定するエンティティ列を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-350">This attribute is used to identify the entity column for which the settings are to be specified.</span></span> |
|                        | <span data-ttu-id="efee9-351">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="efee9-351">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="efee9-352">AutoGenerate</span><span class="sxs-lookup"><span data-stu-id="efee9-352">AutoGenerate</span></span>      | <span data-ttu-id="efee9-353">これは、自動生成オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-353">This is a Boolean field with possible values of Yes or No for enabling/disabling auto generate option.</span></span> |
|                        | <span data-ttu-id="efee9-354">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="efee9-354">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="efee9-355">AutoDefault</span><span class="sxs-lookup"><span data-stu-id="efee9-355">AutoDefault</span></span>       | <span data-ttu-id="efee9-356">これは、自動既定オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-356">This is a Boolean field with possible values of Yes or No for enabling/disabling auto default option.</span></span> |
|                        | <span data-ttu-id="efee9-357">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="efee9-357">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="efee9-358">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="efee9-358">DefaultValue</span></span>      | <span data-ttu-id="efee9-359">これは、自動既定設定が有効な場合に使用される既定値です。</span><span class="sxs-lookup"><span data-stu-id="efee9-359">This is the default value to be used if auto defaulting is enabled.</span></span> |
|                        | <span data-ttu-id="efee9-360">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="efee9-360">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="efee9-361">IgnoreBlankValues</span><span class="sxs-lookup"><span data-stu-id="efee9-361">IgnoreBlankValues</span></span> | <span data-ttu-id="efee9-362">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-362">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |
|                        | <span data-ttu-id="efee9-363">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="efee9-363">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="efee9-364">TextQualifier</span><span class="sxs-lookup"><span data-stu-id="efee9-364">TextQualifier</span></span>     | <span data-ttu-id="efee9-365">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-365">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |
|                        | <span data-ttu-id="efee9-366">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="efee9-366">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="efee9-367">UseEnumLabel</span><span class="sxs-lookup"><span data-stu-id="efee9-367">UseEnumLabel</span></span>      | <span data-ttu-id="efee9-368">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="efee9-368">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |

### <a name="test-groups"></a><span data-ttu-id="efee9-369">テスト グループ</span><span class="sxs-lookup"><span data-stu-id="efee9-369">Test groups</span></span>
<span data-ttu-id="efee9-370">テスト グループは、マニフェストの関連するタスクを整理するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-370">Test groups can be used to organize related tasks in a manifest.</span></span> <span data-ttu-id="efee9-371">マニフェストには複数のテスト グループがあります。</span><span class="sxs-lookup"><span data-stu-id="efee9-371">There can be more than one test group in a manifest.</span></span>

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

| <span data-ttu-id="efee9-372">親要素</span><span class="sxs-lookup"><span data-stu-id="efee9-372">Parent element</span></span>   | <span data-ttu-id="efee9-373">要素</span><span class="sxs-lookup"><span data-stu-id="efee9-373">Element</span></span>           | <span data-ttu-id="efee9-374">要素の基数</span><span class="sxs-lookup"><span data-stu-id="efee9-374">Element Cardinality</span></span> | <span data-ttu-id="efee9-375">属性</span><span class="sxs-lookup"><span data-stu-id="efee9-375">Attributes</span></span>  | <span data-ttu-id="efee9-376">説明</span><span class="sxs-lookup"><span data-stu-id="efee9-376">Description</span></span> |
|------------------|-------------------|---------------------|-------------|-------------|
| <span data-ttu-id="efee9-377">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="efee9-377">\<TestManifest\></span></span> | <span data-ttu-id="efee9-378">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="efee9-378">\<TestGroup\></span></span>     | <span data-ttu-id="efee9-379">1..n</span><span class="sxs-lookup"><span data-stu-id="efee9-379">1..n</span></span>                | \-          | \- |
|                  | <span data-ttu-id="efee9-380">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="efee9-380">\<TestGroup\></span></span>     | <span data-ttu-id="efee9-381">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-381">1..1</span></span>                | <span data-ttu-id="efee9-382">氏名</span><span class="sxs-lookup"><span data-stu-id="efee9-382">Name</span></span>        | <span data-ttu-id="efee9-383">これは、グループの機能上の理由を特定するための名前です。</span><span class="sxs-lookup"><span data-stu-id="efee9-383">This is the name for the group to identify its functional reason.</span></span> |
| <span data-ttu-id="efee9-384">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="efee9-384">\<TestGroup\></span></span>    | <span data-ttu-id="efee9-385">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="efee9-385">\<TestCase\></span></span>      | <span data-ttu-id="efee9-386">1..n</span><span class="sxs-lookup"><span data-stu-id="efee9-386">1..n</span></span>                | \-          | <span data-ttu-id="efee9-387">タスクは、この要素で定義されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-387">The task is defined in this element.</span></span> <span data-ttu-id="efee9-388">タスクでは、タスク パラメータおよびタスク動作を継承する共有設定を参照できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-388">The task can refer to the shared set up to inherit task parameters and task behavior.</span></span> <span data-ttu-id="efee9-389">タスクでは、パラメータと動作もそのレベルで上書きできるため、マニフェストの管理を単純にできます。</span><span class="sxs-lookup"><span data-stu-id="efee9-389">The task can also override parameters and behavior at its level thus making the management of the manifest simple.</span></span> |
|                  | <span data-ttu-id="efee9-390">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="efee9-390">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="efee9-391">肩書き</span><span class="sxs-lookup"><span data-stu-id="efee9-391">Title</span></span>       | <span data-ttu-id="efee9-392">これはタスクのタイトルです。</span><span class="sxs-lookup"><span data-stu-id="efee9-392">This is the title for the task.</span></span> |
|                  | <span data-ttu-id="efee9-393">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="efee9-393">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="efee9-394">ID</span><span class="sxs-lookup"><span data-stu-id="efee9-394">ID</span></span>          | <span data-ttu-id="efee9-395">これはタスクの ID です。</span><span class="sxs-lookup"><span data-stu-id="efee9-395">This is the ID for the task.</span></span> <span data-ttu-id="efee9-396">これは英数字で、最大文字数制限は 10 です。</span><span class="sxs-lookup"><span data-stu-id="efee9-396">This can be alphanumeric with a max character limit of 10.</span></span> |
|                  | <span data-ttu-id="efee9-397">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="efee9-397">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="efee9-398">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="efee9-398">RepeatCount</span></span> | <span data-ttu-id="efee9-399">これは、将来の機能のプレース ホルダーです。</span><span class="sxs-lookup"><span data-stu-id="efee9-399">This is a placeholder for a future functionality.</span></span> <span data-ttu-id="efee9-400">ただし、これは値 *1* で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-400">However, this must be specified with a value of *1*.</span></span> |
|                  | <span data-ttu-id="efee9-401">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="efee9-401">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="efee9-402">TraceParser</span><span class="sxs-lookup"><span data-stu-id="efee9-402">TraceParser</span></span> | <span data-ttu-id="efee9-403">これは、将来の機能のプレース ホルダーです。</span><span class="sxs-lookup"><span data-stu-id="efee9-403">This is a placeholder for a future functionality.</span></span> <span data-ttu-id="efee9-404">ただし、これは値*オフ*で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-404">However, this must be specified with a value *off*.</span></span> |
|                  | <span data-ttu-id="efee9-405">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="efee9-405">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="efee9-406">タイムアウト</span><span class="sxs-lookup"><span data-stu-id="efee9-406">Timeout</span></span>     | <span data-ttu-id="efee9-407">これは、タスク自動化マネージャーによってタスクがモニターされる最大期間です。</span><span class="sxs-lookup"><span data-stu-id="efee9-407">This is the maximum duration a task will be monitored by the task automation manager.</span></span> <span data-ttu-id="efee9-408">指定したタイムアウトを超えてタスクがまだアクティブな場合、マネージャーはマニフェスト内の次のタスクに進みます。</span><span class="sxs-lookup"><span data-stu-id="efee9-408">If the task is still active beyond the timeout specified, the manager will proceed to the next task in the manifest.</span></span> |
| <span data-ttu-id="efee9-409">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="efee9-409">\<TestCase\></span></span>     | <span data-ttu-id="efee9-410">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="efee9-410">\<DataFile\></span></span>      | <span data-ttu-id="efee9-411">1..n</span><span class="sxs-lookup"><span data-stu-id="efee9-411">1..n</span></span>                | \-          | <span data-ttu-id="efee9-412">この要素は、タスクで使用されるファイル、またはデータのプロジェクトを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-412">This element is used to define the file or data package to be used by the task.</span></span> <span data-ttu-id="efee9-413">これは、既に宣言されたファイル、またはマニフェストの共有セクションのデータ パッケージを参照できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-413">This can reference to an already declared file or a data package in the shared section of the manifest.</span></span> <span data-ttu-id="efee9-414">タスクでは、反復バッチ インポート シナリオでのみ指定された複数のデータ ファイルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="efee9-414">A task can have more than one data file specified for recurring batch import scenarios only.</span></span> <span data-ttu-id="efee9-415">他のシナリオでは、1 つ以上のファイルが指定されていても、最初のファイルがタスクによって使用されるファイルです。</span><span class="sxs-lookup"><span data-stu-id="efee9-415">For other scenarios, even if more than one files are specified, the first file is what will be used by the task.</span></span> |
|                  | <span data-ttu-id="efee9-416">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="efee9-416">\<JobDefinition\></span></span> | <span data-ttu-id="efee9-417">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-417">1..1</span></span>                | \-          | <span data-ttu-id="efee9-418">この要素は、タスクで使用されるデータのプロジェクトを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-418">This element is used to define the data project to be used by the task.</span></span> <span data-ttu-id="efee9-419">これは、共有セクション内のすでに宣言されているマニフェストのジョブ定義を参照できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-419">This can reference to an already declared job definition in the shared section of the manifest.</span></span> <span data-ttu-id="efee9-420">タスクでは、共有設定で定義されている値よりも新しい値にジョブ定義の要素を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="efee9-420">The task can override elements of job definition to a new value than what is defined in the shared set up.</span></span> |
|                  | <span data-ttu-id="efee9-421">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="efee9-421">\<EntitySetup\></span></span>   | <span data-ttu-id="efee9-422">1..1</span><span class="sxs-lookup"><span data-stu-id="efee9-422">1..1</span></span>                | \-          | <span data-ttu-id="efee9-423">この要素は、タスクで使用されるエンティティのエンティティ セットアップを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-423">This element is used to define the entity set up for entities used by the task.</span></span> <span data-ttu-id="efee9-424">これは、マニフェストの共有のセクションで既に宣言されたエンティティ セットアップを参照できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-424">This can reference to an already declared entity set up in the shared section of the manifest.</span></span> <span data-ttu-id="efee9-425">タスクでは、共有設定で定義されている値よりも新しい値にエンティティ設定の要素を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="efee9-425">The task can override elements of entity setup to a new value than what is defined in the shared set up.</span></span> |

## <a name="best-practices-for-manifest-design"></a><span data-ttu-id="efee9-426">マニフェスト デザインのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="efee9-426">Best practices for manifest design</span></span>
<span data-ttu-id="efee9-427">さまざまな方法でマニフェストを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="efee9-427">You can define a manifest in many ways.</span></span> <span data-ttu-id="efee9-428">マニフェストをデザインするときに考慮する必要があるいくつかのポインターを次に示します。</span><span class="sxs-lookup"><span data-stu-id="efee9-428">Here are a few pointers that you should consider when you design a manifest.</span></span>

### <a name="granularity"></a><span data-ttu-id="efee9-429">粒度</span><span class="sxs-lookup"><span data-stu-id="efee9-429">Granularity</span></span>
<span data-ttu-id="efee9-430">機能的な意思決定としてマニフェストの粒度を判断することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="efee9-430">We recommend that you determine the granularity of your manifest as a functional decision.</span></span> <span data-ttu-id="efee9-431">チームは、複数のマニフェストを管理するか、または単一のマニフェストの変更を管理するかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-431">Your team must decide whether it wants to manage many manifests or manage changes in a single manifest.</span></span>

- <span data-ttu-id="efee9-432">チームが論理的に必要と考える数のマニフェストを使って開始します。</span><span class="sxs-lookup"><span data-stu-id="efee9-432">Start with as many manifests as your team thinks you logically need.</span></span> <span data-ttu-id="efee9-433">後で、チームが実際にマニフェストの実行を開始すると、予想より少ないマニフェストを使用しており、それらを結合したいと考える場合があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-433">Later, when the team actually starts to run the manifests, it might find that it uses fewer manifests than it expected, and it might want to merge them.</span></span> <span data-ttu-id="efee9-434">この場合、マニフェストをマージすることができます。</span><span class="sxs-lookup"><span data-stu-id="efee9-434">In this case, you can merge manifests.</span></span>
- <span data-ttu-id="efee9-435">職務の分離を検討する。</span><span class="sxs-lookup"><span data-stu-id="efee9-435">Consider separation of duties.</span></span> <span data-ttu-id="efee9-436">たとえば、デモ データの設定に対して 1 つのマニフェスト、環境の高品質の構成の設定に対して別のマニフェストがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-436">For example, you might have one manifest for the setup of demo data and another manifest for the setup of the golden configuration for your environment.</span></span> <span data-ttu-id="efee9-437">この方法で、チーム メンバーが使用する予定のマニフェストのみを使用することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-437">In this way, you can make sure that team members use only the manifests that they are supposed to use.</span></span>
- <span data-ttu-id="efee9-438">LCS へのユーザー アクセスについて考慮してください。</span><span class="sxs-lookup"><span data-stu-id="efee9-438">Consider user access to LCS.</span></span> <span data-ttu-id="efee9-439">たとえば、大きなおよびグローバルに配分された実装チームは、アプリケーションの複数のインスタンスまたは複数の LCS プロジェクトを持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-439">For example, larger and globally distributed implementation teams might have multiple instances of the application or multiple LCS projects.</span></span>

### <a name="inheritance"></a><span data-ttu-id="efee9-440">継承</span><span class="sxs-lookup"><span data-stu-id="efee9-440">Inheritance</span></span>
<span data-ttu-id="efee9-441">マニフェスト スキーマは、マニフェスト内のすべてのタスクに適用される共通要素の継承をサポートします。</span><span class="sxs-lookup"><span data-stu-id="efee9-441">The manifest schema supports inheritance of common elements that will apply to all tasks in the manifest.</span></span> <span data-ttu-id="efee9-442">タスクは、共通の要素を上書きして一意の動作を定義できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-442">A task can override a common element to define a unique behavior.</span></span> <span data-ttu-id="efee9-443">**共通設定** セクションの目的は、構成要素の繰り返しを最小限に抑えて、可能な限り要素を再利用することです。</span><span class="sxs-lookup"><span data-stu-id="efee9-443">The purpose of the **Shared setup** section is to minimize repetition of configuration elements, so that elements are reused as much as possible.</span></span> <span data-ttu-id="efee9-444">目標は、メンテナンスと可読性を向上させるために、マニフェストを簡潔かつ清潔に保つことです。</span><span class="sxs-lookup"><span data-stu-id="efee9-444">The goal is to keep the manifest concise and clean, to improve maintenance and readability.</span></span>

### <a name="source-control"></a><span data-ttu-id="efee9-445">ソース管理</span><span class="sxs-lookup"><span data-stu-id="efee9-445">Source control</span></span>
<span data-ttu-id="efee9-446">実装チームのすべてのメンバーが使用する必要があるマニフェストは、アプリケーション オブジェクト ツリー (AOT) 内のソース コントロールに格納されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-446">Manifests that must be used by all the members of an implementation team should be stored in source control in the Application Object Tree (AOT).</span></span> <span data-ttu-id="efee9-447">この方法は、ソース管理の利点を提供するだけでなく、プロセスがすべてのユーザーに一貫した方法で配布またはマニフェストを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="efee9-447">This approach not only provides the benefits of source control, but also enables a process to distribute or make manifests available to all users in a consistent manner.</span></span> <span data-ttu-id="efee9-448">また、この方法では、マニフェストを構成に使用する場合、データ管理に関連するデータ プロジェクトの構成管理も可能です。</span><span class="sxs-lookup"><span data-stu-id="efee9-448">This approach also enables configuration management for data projects that are related to data management, if manifests are used for configuration.</span></span>

### <a name="number-of-job-definitions-and-entity-definitions"></a><span data-ttu-id="efee9-449">ジョブ定義とエンティティ定義の数</span><span class="sxs-lookup"><span data-stu-id="efee9-449">Number of job definitions and entity definitions</span></span>
<span data-ttu-id="efee9-450">使用ケースのほとんどの場合、マニフェストで 1 つのジョブ定義で十分であるのは、継承がタスク レベルでの動作を変更するために使用できるからです。</span><span class="sxs-lookup"><span data-stu-id="efee9-450">For most of the use cases, one job definition in a manifest should be enough, because inheritance can be used to change the behavior at the task level.</span></span> <span data-ttu-id="efee9-451">この原則は、エンティティの定義にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-451">This principle also applies to entity definitions.</span></span>

## <a name="validations"></a><span data-ttu-id="efee9-452">検証</span><span class="sxs-lookup"><span data-stu-id="efee9-452">Validations</span></span>
<span data-ttu-id="efee9-453">データ タスク自動化マネージャは、タスクの設定に基づいて検証を実行します。</span><span class="sxs-lookup"><span data-stu-id="efee9-453">Data task automation manager performs validations, based on the setup of a task.</span></span> <span data-ttu-id="efee9-454">タスクが失敗した場合は、タスクの完了後に、検証を表示することによって、エラーの原因をすばやく確認できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-454">If a task fails, you can quickly determine the reason for the failure by viewing the validations after the task is completed.</span></span> <span data-ttu-id="efee9-455">データ タスク自動化マネージャーが提供する情報のレベルは、初期検出を容易にするために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="efee9-455">The level of information that Data task automation manager provides is optimized to facilitate initial discovery.</span></span> <span data-ttu-id="efee9-456">詳細な調査のためには、対応するデータ プロジェクトおよびその実行の詳細を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-456">For detailed investigation, you must look at the corresponding data project and its execution details.</span></span>

<span data-ttu-id="efee9-457">現在、次のデータ検証がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="efee9-457">The following data validations are currently supported:</span></span>

- <span data-ttu-id="efee9-458">**ジョブ ステータス** – この検証は、ジョブが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="efee9-458">**Job status** – This validation checks whether the job was successful.</span></span>
- <span data-ttu-id="efee9-459">**バッチ ステータス** - この検証は、バッチが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="efee9-459">**Batch status** – This validation checks whether the batch was successful.</span></span>
- <span data-ttu-id="efee9-460">**メッセージ状態** – テストが統合に関するものである場合、メッセージの状態が検証されます。</span><span class="sxs-lookup"><span data-stu-id="efee9-460">**Message status** – If the test is about integrations, the message status is validated.</span></span>
- <span data-ttu-id="efee9-461">**切り捨て** – 切り捨てが有効になっている場合は、この検証が切り捨てが発生したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="efee9-461">**Truncation** – If truncation is enabled, this validation checks whether truncation occurred.</span></span>
- <span data-ttu-id="efee9-462">**ステージングのスキップ** – **ステージングのスキップ** がテストで有効になっている場合、ステージングがスキップされたかどうかをこの検証でチェックします。</span><span class="sxs-lookup"><span data-stu-id="efee9-462">**Skip staging** – If **Skip staging** is enabled on a test, this validation checks whether staging was skipped.</span></span>

## <a name="example-1-configuration-management-for-data-projects"></a><span data-ttu-id="efee9-463">例 1: データ プロジェクトの構成管理</span><span class="sxs-lookup"><span data-stu-id="efee9-463">Example 1: Configuration management for data projects</span></span>
<span data-ttu-id="efee9-464">**\<ConfigurationOnly\>** 要素は、データ プロジェクトおよび定期的なスケジュールの構成タスクを作成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="efee9-464">The **\<ConfigurationOnly\>** element can be used to create configuration tasks for data projects and recurring schedules.</span></span>

<span data-ttu-id="efee9-465">この最初の例は、定期的なスケジュールを持たないデータ プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="efee9-465">This first example configures a data project that doesn't have a recurring schedule.</span></span> <span data-ttu-id="efee9-466">2 番目の例には、定期的なスケジュールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="efee9-466">The second example includes a recurring schedule.</span></span> <span data-ttu-id="efee9-467">違いは、**\<Operation\>** 要素の値です。</span><span class="sxs-lookup"><span data-stu-id="efee9-467">The difference is the value of the **\<Operation\>** element.</span></span> <span data-ttu-id="efee9-468">構成タスクのマニフェストは、ソース コントロール下にも保管する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efee9-468">Manifests for configuration tasks should also be kept under source control.</span></span>

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

## <a name="example-2-automated-setup-of-demo-data"></a><span data-ttu-id="efee9-469">例 2: デモ データの自動設定</span><span class="sxs-lookup"><span data-stu-id="efee9-469">Example 2: Automated setup of demo data</span></span>
<span data-ttu-id="efee9-470">次のマニフェストは、デモ データ パッケージが共有アセット ライブラリに格納されている場合の 3 つの法人のデモ データの設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="efee9-470">The following manifest shows the setup of demo data for three legal entities when the demo data packages are stored in the Shared asset library.</span></span>

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
