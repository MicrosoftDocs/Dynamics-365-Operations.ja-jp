---
title: データ タスクの自動化
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations でのデータ タスクの自動化により、さまざまな種類のデータ タスクを簡単に繰り返し、各タスクの結果を検証する方法を説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform update 16
ms.openlocfilehash: dc29c6cd1a8320461635b6b3f732a3d7519c14e0
ms.sourcegitcommit: 0ee991a48e271debbe1e0a9932ca8af0162d2275
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2019
ms.locfileid: "898664"
---
# <a name="data-task-automation"></a><span data-ttu-id="2a342-103">データ タスクの自動化</span><span class="sxs-lookup"><span data-stu-id="2a342-103">Data task automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2a342-104">Microsoft Dynamics 365 for Finance and Operations のデータ タスクの自動化により、さまざまな種類のデータ タスクを簡単に繰り返し、各タスクの結果を検証することができます。</span><span class="sxs-lookup"><span data-stu-id="2a342-104">Data task automation in Microsoft Dynamics 365 for Finance and Operations lets you easily repeat many types of data tasks and validate the outcome of each task.</span></span> <span data-ttu-id="2a342-105">データ タスクの自動化は、実装フェーズにあるプロジェクトで非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="2a342-105">Data task automation is very useful for projects that are in the implementation phase.</span></span> <span data-ttu-id="2a342-106">たとえば、データ プロジェクトの作成およびコンフィギュレーションを自動化することができます。</span><span class="sxs-lookup"><span data-stu-id="2a342-106">For example, you can automate the creation and configuration of data projects.</span></span> <span data-ttu-id="2a342-107">また、デモ データおよび高品質の構成データ、およびデータ移行に関連する他のタスクなどの、インポート/エクスポート オペレーションの実行を構成およびトリガーすることができます。</span><span class="sxs-lookup"><span data-stu-id="2a342-107">You can also configure and trigger the execution of import/export operations, such as the setup of demo data and golden configuration data, and other tasks that are related to data migration.</span></span> <span data-ttu-id="2a342-108">また、タスクの結果の検証を使用して、データ エンティティの自動テストを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="2a342-108">You can also create automated testing of data entities by using task outcome validation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a342-109">現時点では、オンプレミス環境ではデータ タスクの自動化はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2a342-109">Data task automation isn't currently supported for on-premises environments.</span></span>

<span data-ttu-id="2a342-110">データ タスクの自動化のために次の方法をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2a342-110">We recommend the following approach for data task automation.</span></span>

1. <span data-ttu-id="2a342-111">自動化の恩恵を受けるデータ関連のタスクを特定する。</span><span class="sxs-lookup"><span data-stu-id="2a342-111">Identify the data-related tasks that will benefit from automation.</span></span>

    <span data-ttu-id="2a342-112">実装チームは自分たちの構成管理計画とデータ移行計画をレビューして、自動化のための潜在的なデータ タスクを識別すること、またデータ エンティティのテスト ケースも識別することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2a342-112">We recommend that implementation teams review their configuration management plan and data migration plan to identify potential data tasks for automation, and also to identify data entity test cases.</span></span>

2. <span data-ttu-id="2a342-113">タスクを定義します。</span><span class="sxs-lookup"><span data-stu-id="2a342-113">Define tasks.</span></span>

    <span data-ttu-id="2a342-114">タスクは、XML マニフェストで定義されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-114">Tasks are defined in an XML manifest.</span></span> <span data-ttu-id="2a342-115">アプリケーション ライフ サイクルの管理 (ALM) 戦略では、構成管理の一部としてソース管理下のマニフェストを保持することができます。</span><span class="sxs-lookup"><span data-stu-id="2a342-115">You can keep your manifest under source control as part of configuration management in your application lifecycle management (ALM) strategy.</span></span>

3. <span data-ttu-id="2a342-116">Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリに、データ タスクの自動化に関連するデータ パッケージを配置します。</span><span class="sxs-lookup"><span data-stu-id="2a342-116">Put the data packages that are related to data task automation in the Shared asset library of Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="2a342-117">また、必要に応じて特定の LCS プロジェクトを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="2a342-117">You can also use a specific LCS project as you require.</span></span>

    <span data-ttu-id="2a342-118">データ タスク自動化マネージャは、LCS プロジェクトに関連するサンドボックスまたは実稼動環境からパッケージを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2a342-118">Data task automation manager can consume packages from any sandbox and/or production environment that is related to the LCS project.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="2a342-119">Finance and Operations のデータ タスク自動化マネージャーを実行するユーザー アカウントは、LCS およびデータ パッケージのマニフェストで参照される LCS プロジェクトにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-119">The user account that runs Data task automation manager in Finance and Operations must have access to LCS and to the LCS project that is referenced in the manifest for data packages.</span></span>
    > - <span data-ttu-id="2a342-120">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合アプリケーション プログラミング インターフェイス (API) を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="2a342-120">Although data task automation can be run in any environment in the cloud, we strongly recommend that you not run any import/export tasks that use integration application programming interfaces (APIs) in a production environment.</span></span> <span data-ttu-id="2a342-121">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-121">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

4. <span data-ttu-id="2a342-122">データ タスクを実行し、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="2a342-122">Run the data tasks, and then review the outcomes.</span></span>

    <span data-ttu-id="2a342-123">データ タスク自動化マネージャは、各タスクの成功または失敗の結果を提供します。</span><span class="sxs-lookup"><span data-stu-id="2a342-123">Data task automation manager provides the success or failure outcome for each task.</span></span> <span data-ttu-id="2a342-124">また、タスクが失敗した理由に関する見解も提供します。</span><span class="sxs-lookup"><span data-stu-id="2a342-124">It also provides insights into the reason why a task failed.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2a342-125">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合 API を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="2a342-125">Although data task automation can be run in any environments in the cloud, we recommend that you not run any import/export tasks that use integration APIs in a production environment.</span></span> <span data-ttu-id="2a342-126">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-126">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

<span data-ttu-id="2a342-127">次のビデオは、Data Task Automation Manager の初期リリースを紹介する TechTalk の 55 分です。[タスク自動化フレームワーク](https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4)。</span><span class="sxs-lookup"><span data-stu-id="2a342-127">The following video is a 55-minute TechTalk that walks you through an early release of Data task automation manager: [Task automation framework](https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4).</span></span>

## <a name="task-manifest"></a><span data-ttu-id="2a342-128">タスク マニフェスト</span><span class="sxs-lookup"><span data-stu-id="2a342-128">Task manifest</span></span>
<span data-ttu-id="2a342-129">タスクは、XML マニフェストで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-129">A task must be defined in an XML manifest.</span></span> <span data-ttu-id="2a342-130">このセクションでは、マニフェストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2a342-130">This section describes the manifest.</span></span> <span data-ttu-id="2a342-131">マニフェストを名前付けしデザインする方法の指針については、このトピックの後半の、「マニフェストのデザインに対するベスト プラクティス」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a342-131">For guidance about how to name and design the manifest, see the "Best practices for manifest design" section later in this topic.</span></span>

### <a name="manifest-root"></a><span data-ttu-id="2a342-132">マニフェスト ルート</span><span class="sxs-lookup"><span data-stu-id="2a342-132">Manifest root</span></span>
<span data-ttu-id="2a342-133">**\<TestManifest\>** 要素は、マニフェストのルートです。</span><span class="sxs-lookup"><span data-stu-id="2a342-133">The **\<TestManifest\>** element is the root of the manifest.</span></span> <span data-ttu-id="2a342-134">その他のすべての要素はこの要素の子です。</span><span class="sxs-lookup"><span data-stu-id="2a342-134">All other elements are children of this element.</span></span>

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

| <span data-ttu-id="2a342-135">要素</span><span class="sxs-lookup"><span data-stu-id="2a342-135">Element</span></span>          | <span data-ttu-id="2a342-136">要素の基数</span><span class="sxs-lookup"><span data-stu-id="2a342-136">Element Cardinality</span></span> | <span data-ttu-id="2a342-137">属性</span><span class="sxs-lookup"><span data-stu-id="2a342-137">Attributes</span></span> | <span data-ttu-id="2a342-138">属性の説明</span><span class="sxs-lookup"><span data-stu-id="2a342-138">Attribute description</span></span>                                     |
|------------------|---------------------|------------|-----------------------------------------------------------|
| <span data-ttu-id="2a342-139">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="2a342-139">\<TestManifest\></span></span> | <span data-ttu-id="2a342-140">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-140">1..1</span></span>                | <span data-ttu-id="2a342-141">名前</span><span class="sxs-lookup"><span data-stu-id="2a342-141">name</span></span>       | <span data-ttu-id="2a342-142">*名前*はマニフェストの目的を識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2a342-142">The *name* helps to identify the purpose of the manifest.</span></span> |

### <a name="shared-setup"></a><span data-ttu-id="2a342-143">共有された設定</span><span class="sxs-lookup"><span data-stu-id="2a342-143">Shared setup</span></span>
<span data-ttu-id="2a342-144">**共有セットアップ** セクションは、全般的なタスクのパラメーターとマニフェスト内のすべてのタスクの動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="2a342-144">The **Shared setup** section defines general task parameters and behaviors for all tasks in the manifest.</span></span>

| <span data-ttu-id="2a342-145">親要素</span><span class="sxs-lookup"><span data-stu-id="2a342-145">Parent element</span></span>   | <span data-ttu-id="2a342-146">要素</span><span class="sxs-lookup"><span data-stu-id="2a342-146">Element</span></span>         | <span data-ttu-id="2a342-147">要素の基数</span><span class="sxs-lookup"><span data-stu-id="2a342-147">Element Cardinality</span></span> | <span data-ttu-id="2a342-148">属性</span><span class="sxs-lookup"><span data-stu-id="2a342-148">Attributes</span></span> | <span data-ttu-id="2a342-149">属性の説明</span><span class="sxs-lookup"><span data-stu-id="2a342-149">Attribute description</span></span>            |
|------------------|-----------------|---------------------|------------|----------------------------------|
| <span data-ttu-id="2a342-150">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="2a342-150">\<TestManifest\></span></span> | <span data-ttu-id="2a342-151">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="2a342-151">\<SharedSetup\></span></span> | <span data-ttu-id="2a342-152">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-152">1..1</span></span>                | \-         | <span data-ttu-id="2a342-153">この要素には属性はありません。</span><span class="sxs-lookup"><span data-stu-id="2a342-153">This element takes no attributes.</span></span> |

### <a name="data-files"></a><span data-ttu-id="2a342-154">データ ファイル</span><span class="sxs-lookup"><span data-stu-id="2a342-154">Data files</span></span>
<span data-ttu-id="2a342-155">**\<DataFile\>** 要素は、マニフェスト内のタスクが使用するデータ パッケージとデータ ファイルを定義します。</span><span class="sxs-lookup"><span data-stu-id="2a342-155">**\<DataFile\>** elements define the data packages and data files that the tasks in the manifest will use.</span></span> <span data-ttu-id="2a342-156">データ ファイルは、LCS プロジェクトの LCS アセット ライブラリまたは共有アセット ライブラリのいずれかになければなりません。</span><span class="sxs-lookup"><span data-stu-id="2a342-156">The data files must be either in the LCS asset library of your LCS project or in the Shared asset library.</span></span>

```
<DataFile ID='SharedSetup' name='Demo data-7.3-100-System and Shared'  assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsHQUS' name='Demo data-7.3-200-Financials-HQUS' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPICH' name='Demo data-7.3-200-Financials-PICH' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPIFB' name='Demo data-7.3-200-Financials-PIFB' assetType='Data package' lcsProjectId=''/>
```

| <span data-ttu-id="2a342-157">親要素</span><span class="sxs-lookup"><span data-stu-id="2a342-157">Parent element</span></span>  | <span data-ttu-id="2a342-158">要素</span><span class="sxs-lookup"><span data-stu-id="2a342-158">Element</span></span>      | <span data-ttu-id="2a342-159">要素の基数</span><span class="sxs-lookup"><span data-stu-id="2a342-159">Element Cardinality</span></span> | <span data-ttu-id="2a342-160">属性</span><span class="sxs-lookup"><span data-stu-id="2a342-160">Attributes</span></span>   | <span data-ttu-id="2a342-161">属性の説明</span><span class="sxs-lookup"><span data-stu-id="2a342-161">Attribute description</span></span> |
|-----------------|--------------|---------------------|--------------|-----------------------|
| <span data-ttu-id="2a342-162">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="2a342-162">\<SharedSetup\></span></span> | <span data-ttu-id="2a342-163">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="2a342-163">\<DataFile\></span></span> | <span data-ttu-id="2a342-164">1..n</span><span class="sxs-lookup"><span data-stu-id="2a342-164">1..n</span></span>                | \-           | \- |
|                 | <span data-ttu-id="2a342-165">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="2a342-165">\<DataFile\></span></span> | \-                  | <span data-ttu-id="2a342-166">ID</span><span class="sxs-lookup"><span data-stu-id="2a342-166">ID</span></span>           | |
|                 | <span data-ttu-id="2a342-167">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="2a342-167">\<DataFile\></span></span> | \-                  | <span data-ttu-id="2a342-168">名前</span><span class="sxs-lookup"><span data-stu-id="2a342-168">name</span></span>         | <span data-ttu-id="2a342-169">データ ファイルを表す資産の名前。</span><span class="sxs-lookup"><span data-stu-id="2a342-169">Name of the asset that represents the data file.</span></span> |
|                 | <span data-ttu-id="2a342-170">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="2a342-170">\<DataFile\></span></span> | \-                  | <span data-ttu-id="2a342-171">assetType</span><span class="sxs-lookup"><span data-stu-id="2a342-171">assetType</span></span>    | <span data-ttu-id="2a342-172">データ ファイルを格納する LCS 資産ライブラリでの資産タイプ。</span><span class="sxs-lookup"><span data-stu-id="2a342-172">The asset type in LCS asset library that stores the data file.</span></span> <span data-ttu-id="2a342-173">これは、LCS アセット ライブラリで示されたように、アセット タイプの名前です。</span><span class="sxs-lookup"><span data-stu-id="2a342-173">This is the asset type name as shown in LCS asset library.</span></span> |
|                 | <span data-ttu-id="2a342-174">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="2a342-174">\<DataFile\></span></span> | \-                  | <span data-ttu-id="2a342-175">lcsProjectId</span><span class="sxs-lookup"><span data-stu-id="2a342-175">lcsProjectId</span></span> | <span data-ttu-id="2a342-176">その資産ライブラリで LCS プロジェクトにはデータ ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="2a342-176">The LCS project that has the data file in its asset library.</span></span> <span data-ttu-id="2a342-177">プロジェクト ID が " として指定されている場合は、共有アセット ライブラリを示します。</span><span class="sxs-lookup"><span data-stu-id="2a342-177">If the project ID is specified as '' then, it indicates the Shared asset library.</span></span> |

### <a name="data-project-definition"></a><span data-ttu-id="2a342-178">データ プロジェクト定義</span><span class="sxs-lookup"><span data-stu-id="2a342-178">Data project definition</span></span>
<span data-ttu-id="2a342-179">**\<JobDefinition\>** 要素は、データ プロジェクト定義を定義します。</span><span class="sxs-lookup"><span data-stu-id="2a342-179">The **\<JobDefinition\>** element defines the data project definition.</span></span> <span data-ttu-id="2a342-180">マニフェストには複数のジョブ定義があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-180">There can be more than one job definition in a manifest.</span></span>

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

| <span data-ttu-id="2a342-181">親要素</span><span class="sxs-lookup"><span data-stu-id="2a342-181">Parent element</span></span>    | <span data-ttu-id="2a342-182">要素</span><span class="sxs-lookup"><span data-stu-id="2a342-182">Element</span></span>                          | <span data-ttu-id="2a342-183">要素の基数</span><span class="sxs-lookup"><span data-stu-id="2a342-183">Element cardinality</span></span> | <span data-ttu-id="2a342-184">属性</span><span class="sxs-lookup"><span data-stu-id="2a342-184">Attribute</span></span> | <span data-ttu-id="2a342-185">説明</span><span class="sxs-lookup"><span data-stu-id="2a342-185">Description</span></span> |
|-------------------|----------------------------------|---------------------|-----------|-------------|
| <span data-ttu-id="2a342-186">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="2a342-186">\<SharedSetup\></span></span>   | <span data-ttu-id="2a342-187">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="2a342-187">\<JobDefinition\></span></span>                | <span data-ttu-id="2a342-188">1..n</span><span class="sxs-lookup"><span data-stu-id="2a342-188">1..n</span></span>                | <span data-ttu-id="2a342-189">ID</span><span class="sxs-lookup"><span data-stu-id="2a342-189">ID</span></span>        | <span data-ttu-id="2a342-190">タスクでジョブ定義 ID を使用してデータ プロジェクトで使用する定義を参照できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-190">The job definition ID is used in the tasks to reference the definition to be used for the data project.</span></span> |
| <span data-ttu-id="2a342-191">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="2a342-191">\<JobDefinition\></span></span> | <span data-ttu-id="2a342-192">[\<操作\>]</span><span class="sxs-lookup"><span data-stu-id="2a342-192">\<Operation\></span></span>                    | <span data-ttu-id="2a342-193">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-193">1..1</span></span>                | \-        | <span data-ttu-id="2a342-194">実行される操作は、次の値によって指定されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-194">The operation to be performed is specified by the following values:</span></span> <br> <span data-ttu-id="2a342-195">- インポート</span><span class="sxs-lookup"><span data-stu-id="2a342-195">- Import</span></span> <br> <span data-ttu-id="2a342-196">- エクスポート</span><span class="sxs-lookup"><span data-stu-id="2a342-196">- Export</span></span> |
|                   | <span data-ttu-id="2a342-197">\<切り詰め\></span><span class="sxs-lookup"><span data-stu-id="2a342-197">\<Truncate\></span></span>                     | <span data-ttu-id="2a342-198">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-198">1..1</span></span>                | \-        | <span data-ttu-id="2a342-199">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-199">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="2a342-200">これは操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-200">This is applicable only when operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="2a342-201">\<モード\></span><span class="sxs-lookup"><span data-stu-id="2a342-201">\<Mode\></span></span>                         | <span data-ttu-id="2a342-202">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-202">1..1</span></span>                | \-        | <span data-ttu-id="2a342-203">モードでは、操作を実行する必要があるメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="2a342-203">The mode specifies the method using which the operation must be performed.</span></span> <span data-ttu-id="2a342-204">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2a342-204">The possible values are:</span></span><br><span data-ttu-id="2a342-205">- 非同期インポート</span><span class="sxs-lookup"><span data-stu-id="2a342-205">- Import async</span></span> <br><span data-ttu-id="2a342-206">- 非同期エクスポート</span><span class="sxs-lookup"><span data-stu-id="2a342-206">- Export async</span></span> <br><span data-ttu-id="2a342-207">- 定期的に実行するバッチ: エンキュー API を使用します。</span><span class="sxs-lookup"><span data-stu-id="2a342-207">- Recurring batch: This uses the enqueue API.</span></span> <span data-ttu-id="2a342-208">デキュー API には現在対応していません。</span><span class="sxs-lookup"><span data-stu-id="2a342-208">Dequeue API is not supported yet.</span></span> <span data-ttu-id="2a342-209">パッケージAPIは、エクスポートとインポートの両方に対応しています。</span><span class="sxs-lookup"><span data-stu-id="2a342-209">Package API supports both export and import.</span></span>|
|                   | <span data-ttu-id="2a342-210">\<ConfigurationOnly\></span><span class="sxs-lookup"><span data-stu-id="2a342-210">\<ConfigurationOnly\></span></span>            | <span data-ttu-id="2a342-211">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-211">1..1</span></span>                | \-        | <span data-ttu-id="2a342-212">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-212">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="2a342-213">タスクがデータ プロジェクトをコンフィギュレーションするのみで、指定された操作を実行しない場合は、はいに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-213">This must be set to Yes if the task is only to configure the data project but not to perform the specified operation.</span></span> |
|                   | <span data-ttu-id="2a342-214">\<BatchFrequencyInMinutes\></span><span class="sxs-lookup"><span data-stu-id="2a342-214">\<BatchFrequencyInMinutes\></span></span>      | <span data-ttu-id="2a342-215">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-215">1..1</span></span>                | \-        | <span data-ttu-id="2a342-216">バッチがスケジュール設定される頻度を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a342-216">This specifies the frequency in which the batch must be scheduled.</span></span> <span data-ttu-id="2a342-217">これはモードが*定期実行されるバッチ*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-217">This is applicable only when mode is set to *recurring batch*.</span></span> |
|                   | <span data-ttu-id="2a342-218">\<NumberOfTimesToRunBatch\></span><span class="sxs-lookup"><span data-stu-id="2a342-218">\<NumberOfTimesToRunBatch\></span></span>      | <span data-ttu-id="2a342-219">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-219">1..1</span></span>                | \-        | <span data-ttu-id="2a342-220">これは、スケジュールされているバッチを実行する回数の制限を設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-220">This is used to set a limit to how many times the scheduled batch should run.</span></span> <span data-ttu-id="2a342-221">これはモードが*定期実行されるバッチ*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-221">This is applicable only when mode is set to *recurring batch*.</span></span> |
|                   | <span data-ttu-id="2a342-222">\<UploadFrequencyInSeconds\></span><span class="sxs-lookup"><span data-stu-id="2a342-222">\<UploadFrequencyInSeconds\></span></span>     | <span data-ttu-id="2a342-223">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-223">1..1</span></span>                | \-        | <span data-ttu-id="2a342-224">これは、インポートする定期バッチ ジョブにファイルをアップロードする頻度を制御するために使用します。</span><span class="sxs-lookup"><span data-stu-id="2a342-224">This is used to control the rate at which a file is uploaded to the recurring batch job for import.</span></span> <span data-ttu-id="2a342-225">これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-225">This must be used only for automated testing of recurring integrations in non-production environments.</span></span> <span data-ttu-id="2a342-226">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-226">This is applicable only when mode is set to *recurring batch* and operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="2a342-227">\<TotalNumberOfTimesToUpload\></span><span class="sxs-lookup"><span data-stu-id="2a342-227">\<TotalNumberOfTimesToUpload\></span></span>   | <span data-ttu-id="2a342-228">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-228">1..1</span></span>                |           | <span data-ttu-id="2a342-229">これはファイルを繰り返しバッチにアップロードする総回数を制御します。</span><span class="sxs-lookup"><span data-stu-id="2a342-229">This controls the total number of times the file should be uploaded to the recurring batch.</span></span> <span data-ttu-id="2a342-230">これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-230">This must be used only for automated testing of recurring integrations in non-production environments.</span></span> <span data-ttu-id="2a342-231">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-231">This is applicable only when mode is set to *recurring batch* and operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="2a342-232">\<SupportedDataSoureType\></span><span class="sxs-lookup"><span data-stu-id="2a342-232">\<SupportedDataSoureType\></span></span>       | <span data-ttu-id="2a342-233">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-233">1..1</span></span>                |           | <span data-ttu-id="2a342-234">ファイルが定期的なバッチまたはパッケージに送信中であるかどうかを指定するために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-234">This must be used to specify if a file is being sent to the recurring batch or a package.</span></span> <span data-ttu-id="2a342-235">これはモードが「定期実行されるバッチ」に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-235">This is only applicable when mode is set to 'recurring batch'.</span></span> |
|                   | <span data-ttu-id="2a342-236">\<ProcessMessagesInOrder\></span><span class="sxs-lookup"><span data-stu-id="2a342-236">\<ProcessMessagesInOrder\></span></span>       | <span data-ttu-id="2a342-237">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-237">1..1</span></span>                |           | <span data-ttu-id="2a342-238">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-238">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="2a342-239">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-239">This is applicable only when mode is set to *recurring batch* and operation is *Import*.</span></span> |
|                   | <span data-ttu-id="2a342-240">\<PreventUploadWhenZeroRecords\></span><span class="sxs-lookup"><span data-stu-id="2a342-240">\<PreventUploadWhenZeroRecords\></span></span> | <span data-ttu-id="2a342-241">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-241">1..1</span></span>                |           | <span data-ttu-id="2a342-242">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-242">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="2a342-243">これはモードが*定期実行されるバッチ*に設定されており、操作が*エクスポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-243">This is applicable only when mode is set to *recurring batch* and operation is *Export*.</span></span> |
|                   | <span data-ttu-id="2a342-244">\<UseCompanyFromMessage\></span><span class="sxs-lookup"><span data-stu-id="2a342-244">\<UseCompanyFromMessage\></span></span>        | <span data-ttu-id="2a342-245">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-245">1..1</span></span>                |           | <span data-ttu-id="2a342-246">これははい、またはいいえに設定できるブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-246">This is a Boolean field which can be set to Yes or No.</span></span> <span data-ttu-id="2a342-247">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-247">This is applicable only when mode is set to *recurring batch* and operation is *Import*.</span></span> |
|                   | <span data-ttu-id="2a342-248">\<LegalEntity\></span><span class="sxs-lookup"><span data-stu-id="2a342-248">\<LegalEntity\></span></span>                  | <span data-ttu-id="2a342-249">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-249">1..1</span></span>                |           | <span data-ttu-id="2a342-250">これをは、インポート/エクスポート ジョブを実行する必要がある法人を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-250">This is used to specify the legal entity in which the import/export job must be executed.</span></span> |
|                   | <span data-ttu-id="2a342-251">\<ConfigurationOnly\></span><span class="sxs-lookup"><span data-stu-id="2a342-251">\<ConfigurationOnly\></span></span>            | <span data-ttu-id="2a342-252">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-252">1..1</span></span>                |           | <span data-ttu-id="2a342-253">これを使用して、データのプロジェクトおよび構成する定期的なスケジュールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-253">This is used to create data projects and recurring schedules to be configured.</span></span> <span data-ttu-id="2a342-254">インポートまたはエクスポートの操作は実行されません。</span><span class="sxs-lookup"><span data-stu-id="2a342-254">The operation of import or export will not be executed.</span></span> <span data-ttu-id="2a342-255">ただし、データ プロジェクトを正しく設定するには、操作とモードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-255">However, it is required to specify the operation and mode for the data project to be configured correctly.</span></span> <span data-ttu-id="2a342-256">これは、はいまたはいいえを取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-256">This is a Boolean field which takes Yes or No.</span></span> |
|                   | <span data-ttu-id="2a342-257">\<PackageAPIExecute\></span><span class="sxs-lookup"><span data-stu-id="2a342-257">\<PackageAPIExecute\></span></span>            | <span data-ttu-id="2a342-258">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-258">1..1</span></span>                |           | <span data-ttu-id="2a342-259">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a342-259">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="2a342-260">これは、"true" または "false" を取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-260">This is a Boolean field which takes 'true' or 'false'.</span></span> |
|                   | <span data-ttu-id="2a342-261">\<PackageAPIOverwrite\></span><span class="sxs-lookup"><span data-stu-id="2a342-261">\<PackageAPIOverwrite\></span></span>            | <span data-ttu-id="2a342-262">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-262">1..1</span></span>                |           | <span data-ttu-id="2a342-263">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a342-263">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="2a342-264">これは、"true" または "false" を取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-264">This is a Boolean field which takes 'true' or 'false'.</span></span> |
|                   | <span data-ttu-id="2a342-265">\<PackageAPIReexecute\></span><span class="sxs-lookup"><span data-stu-id="2a342-265">\<PackageAPIReexecute\></span></span>            | <span data-ttu-id="2a342-266">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-266">1..1</span></span>                |           | <span data-ttu-id="2a342-267">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a342-267">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="2a342-268">これは、"true" または "false" を取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-268">This is a Boolean field which takes 'true' or 'false'.</span></span> |
|                   | <span data-ttu-id="2a342-269">\<DefinitionGroupID\></span><span class="sxs-lookup"><span data-stu-id="2a342-269">\<DefinitionGroupID\></span></span>            | <span data-ttu-id="2a342-270">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-270">1..1</span></span>                |           | <span data-ttu-id="2a342-271">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a342-271">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="2a342-272">これは文字列フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-272">This is a string field.</span></span> |
|                   | <span data-ttu-id="2a342-273">\<PackageName\></span><span class="sxs-lookup"><span data-stu-id="2a342-273">\<PackageName\></span></span>            | <span data-ttu-id="2a342-274">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-274">1..1</span></span>                |           | <span data-ttu-id="2a342-275">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a342-275">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="2a342-276">これは文字列フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-276">This is a string field.</span></span> |

### <a name="entity-setup"></a><span data-ttu-id="2a342-277">エンティティ設定</span><span class="sxs-lookup"><span data-stu-id="2a342-277">Entity setup</span></span>
<span data-ttu-id="2a342-278">**エンティティ設定** セクションは、マニフェストのタスクが使用するエンティティの特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="2a342-278">The **Entity setup** section defines the characteristics of an entity that a task in the manifest will use.</span></span> <span data-ttu-id="2a342-279">マニフェスト内のタスクによって使用されるエンティティごとに、1 つずつ複数の定義が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-279">There can be more than one definition, one for each entity that is used by the tasks in the manifest.</span></span>

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

| <span data-ttu-id="2a342-280">親要素</span><span class="sxs-lookup"><span data-stu-id="2a342-280">Parent element</span></span>         | <span data-ttu-id="2a342-281">要素</span><span class="sxs-lookup"><span data-stu-id="2a342-281">Element</span></span>                              | <span data-ttu-id="2a342-282">要素の基数</span><span class="sxs-lookup"><span data-stu-id="2a342-282">Element cardinality</span></span> | <span data-ttu-id="2a342-283">属性</span><span class="sxs-lookup"><span data-stu-id="2a342-283">Attribute</span></span>         | <span data-ttu-id="2a342-284">説明</span><span class="sxs-lookup"><span data-stu-id="2a342-284">Description</span></span> |
|------------------------|--------------------------------------|---------------------|-------------------|-------------|
| <span data-ttu-id="2a342-285">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="2a342-285">\<SharedSetup\></span></span>        | <span data-ttu-id="2a342-286">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="2a342-286">\<EntitySetup\></span></span>                      | <span data-ttu-id="2a342-287">1..n</span><span class="sxs-lookup"><span data-stu-id="2a342-287">1..n</span></span>                | <span data-ttu-id="2a342-288">ID</span><span class="sxs-lookup"><span data-stu-id="2a342-288">ID</span></span>                | <span data-ttu-id="2a342-289">タスクが使用するエンティティ定義を参照するために使用される ID。</span><span class="sxs-lookup"><span data-stu-id="2a342-289">An identification that will be used by tasks to reference an entity definition to be used.</span></span> |
| <span data-ttu-id="2a342-290">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="2a342-290">\<EntitySetup\></span></span>        | <span data-ttu-id="2a342-291">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="2a342-291">\<Entity\></span></span>                           | <span data-ttu-id="2a342-292">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-292">1..1</span></span>                | <span data-ttu-id="2a342-293">名前</span><span class="sxs-lookup"><span data-stu-id="2a342-293">name</span></span>              | <span data-ttu-id="2a342-294">エンティティ要素は、エンティティの名前で識別されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-294">The entity element is identified by the entity's name.</span></span> <span data-ttu-id="2a342-295">ただし、簡単なマニフェスト定義を容易にするために、この要素は \* ワイルド カードとしてもサポートしています。これは、すべてのエンティティがタスクで使用されていることを意味しています。</span><span class="sxs-lookup"><span data-stu-id="2a342-295">However, to facilitate easy manifest definition, this element also supports \* as a wild card which will mean all entities being used in a task.</span></span> <span data-ttu-id="2a342-296">これは、タスク内の何百ものエンティティを持つデータ パッケージを使用する場合に非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="2a342-296">This comes in very handy when using data packages with hundreds of entities in a task.</span></span> |
| <span data-ttu-id="2a342-297">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="2a342-297">\<Entity\></span></span>             | <span data-ttu-id="2a342-298">\<SourceDataFormatName\></span><span class="sxs-lookup"><span data-stu-id="2a342-298">\<SourceDataFormatName\></span></span>             | <span data-ttu-id="2a342-299">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-299">1..1</span></span>                | \-                | <span data-ttu-id="2a342-300">これはエンティティに使用されるファイル形式です。</span><span class="sxs-lookup"><span data-stu-id="2a342-300">This is the file format to be used for the entity.</span></span> |
|                        | <span data-ttu-id="2a342-301">\<ChangeTracking\></span><span class="sxs-lookup"><span data-stu-id="2a342-301">\<ChangeTracking\></span></span>                   | <span data-ttu-id="2a342-302">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-302">1..1</span></span>                | \-                | <span data-ttu-id="2a342-303">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-303">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="2a342-304">エンティティ全体で変更追跡を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="2a342-304">It enables or disables change tracking on the entire entity.</span></span> |
|                        | <span data-ttu-id="2a342-305">\<PublishToBYOD\></span><span class="sxs-lookup"><span data-stu-id="2a342-305">\<PublishToBYOD\></span></span>                    | <span data-ttu-id="2a342-306">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-306">1..1</span></span>                | \-                | <span data-ttu-id="2a342-307">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-307">This is a Boolean field with possible values of Yes or No.</span></span> |
|                        | <span data-ttu-id="2a342-308">\<DefaultRefreshType\></span><span class="sxs-lookup"><span data-stu-id="2a342-308">\<DefaultRefreshType\></span></span>               | <span data-ttu-id="2a342-309">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-309">1..1</span></span>                | \-                | <span data-ttu-id="2a342-310">これにより、エンティティの既定の更新頻度が設定されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-310">This sets the default refresh rate on the entity.</span></span> <span data-ttu-id="2a342-311">使用可能な値は*増分プッシュのみ*または*フル プッシュ*です。</span><span class="sxs-lookup"><span data-stu-id="2a342-311">The possible values are *Incremental push only* or *Full push*.</span></span> |
|                        | <span data-ttu-id="2a342-312">\<ExcelWorkSheetName\></span><span class="sxs-lookup"><span data-stu-id="2a342-312">\<ExcelWorkSheetName\></span></span>               | <span data-ttu-id="2a342-313">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-313">1..1</span></span>                | \-                | <span data-ttu-id="2a342-314">これはエンティティに使用するワークシートを指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-314">This is used to specify the worksheet to be used for the entity.</span></span> |
|                        | <span data-ttu-id="2a342-315">\<SelectFields\></span><span class="sxs-lookup"><span data-stu-id="2a342-315">\<SelectFields\></span></span>                     | <span data-ttu-id="2a342-316">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-316">1..1</span></span>                | \-                | <span data-ttu-id="2a342-317">これは、エクスポート操作のテンプレートに含まれるフィールドを指定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-317">This can be used to specify the fields to be included in the template for an export operation.</span></span> |
|                        | <span data-ttu-id="2a342-318">\<SetBasedProcessing\></span><span class="sxs-lookup"><span data-stu-id="2a342-318">\<SetBasedProcessing\></span></span>               | <span data-ttu-id="2a342-319">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-319">1..1</span></span>                | \-                | <span data-ttu-id="2a342-320">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-320">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="2a342-321">エンティティのセット ベースのプロセスを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-321">It is used to enable or disable set based processing on an entity.</span></span> |
|                        | <span data-ttu-id="2a342-322">\<FailBatchOnErrorForExecutionUnit\></span><span class="sxs-lookup"><span data-stu-id="2a342-322">\<FailBatchOnErrorForExecutionUnit\></span></span> | <span data-ttu-id="2a342-323">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-323">1..1</span></span>                | \-                | <span data-ttu-id="2a342-324">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-324">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="2a342-325">エンティティの実行単位レベルでエラーを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-325">It is used to enable or disable failure at execution unit level on an entity.</span></span> |
|                        | <span data-ttu-id="2a342-326">\<FailBatchOnErrorForLevel\></span><span class="sxs-lookup"><span data-stu-id="2a342-326">\<FailBatchOnErrorForLevel\></span></span>         | <span data-ttu-id="2a342-327">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-327">1..1</span></span>                | \-                | <span data-ttu-id="2a342-328">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-328">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="2a342-329">エンティティの実行レベルでエラーを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-329">It is used to enable or disable failure at execution level on an entity.</span></span> |
|                        | <span data-ttu-id="2a342-330">\<DisableEntity\></span><span class="sxs-lookup"><span data-stu-id="2a342-330">\<DisableEntity\></span></span>                    | <span data-ttu-id="2a342-331">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-331">1..1</span></span>                | \-                | <span data-ttu-id="2a342-332">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-332">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="2a342-333">データ プロジェクトでエンティティを有効化または無効化するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-333">It is used to enable or disable an entity in a data project.</span></span> |
|                        | <span data-ttu-id="2a342-334">\<SkipStaging\></span><span class="sxs-lookup"><span data-stu-id="2a342-334">\<SkipStaging\></span></span>                      | <span data-ttu-id="2a342-335">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-335">1..1</span></span>                | \-                | <span data-ttu-id="2a342-336">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-336">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="2a342-337">エクスポート中にエンティティのステージング テーブルをスキップするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-337">It is used to skip staging table for an entity during exports.</span></span> |
|                        | <span data-ttu-id="2a342-338">\<ParallelProcessing\></span><span class="sxs-lookup"><span data-stu-id="2a342-338">\<ParallelProcessing\></span></span>               | <span data-ttu-id="2a342-339">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-339">1..1</span></span>                | \-                | <span data-ttu-id="2a342-340">これは、エンティティに対して設定された並列処理を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-340">This is used to define the parallel processing set up for an entity.</span></span> <span data-ttu-id="2a342-341">タスクの始まりで既に終了する場合、タスクはこれらの設定を削除し、その実行の終わりに作成された設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="2a342-341">The task will delete these settings if already exits at the beginning of the task and it will delete the created settings at the end of its execution.</span></span> |
| <span data-ttu-id="2a342-342">\<ParallelProcessing\></span><span class="sxs-lookup"><span data-stu-id="2a342-342">\<ParallelProcessing\></span></span> | <span data-ttu-id="2a342-343">\<しきい値\></span><span class="sxs-lookup"><span data-stu-id="2a342-343">\<Threshold\></span></span>                        | <span data-ttu-id="2a342-344">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-344">1..1</span></span>                | \-                | <span data-ttu-id="2a342-345">並列処理のルールのしきい値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a342-345">This specifies the threshold for the parallel processing rule.</span></span> |
|                        | <span data-ttu-id="2a342-346">\<TaskCount\></span><span class="sxs-lookup"><span data-stu-id="2a342-346">\<TaskCount\></span></span>                        | <span data-ttu-id="2a342-347">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-347">1..1</span></span>                | \-                | <span data-ttu-id="2a342-348">これは、並列処理に使用される並列タスクの数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-348">This is used to specify the number of parallel tasks to be used for parallel processing.</span></span> |
| <span data-ttu-id="2a342-349">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="2a342-349">\<Entity\></span></span>             | <span data-ttu-id="2a342-350">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="2a342-350">\<MappingDetail\></span></span>                    | <span data-ttu-id="2a342-351">0..n</span><span class="sxs-lookup"><span data-stu-id="2a342-351">0..n</span></span>                | \-                | <span data-ttu-id="2a342-352">*自動生成*、*自動既定値*およびエンティティのマッピングで他の設定を構成できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-352">Allows to configure the *auto generate*, *auto default* and other settings on the mapping for an entity.</span></span> |
|                        | <span data-ttu-id="2a342-353">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="2a342-353">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="2a342-354">StagingFieldName</span><span class="sxs-lookup"><span data-stu-id="2a342-354">StagingFieldName</span></span>  | <span data-ttu-id="2a342-355">この属性は、設定を指定するエンティティ列を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-355">This attribute is used to identify the entity column for which the settings are to be specified.</span></span> |
|                        | <span data-ttu-id="2a342-356">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="2a342-356">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="2a342-357">AutoGenerate</span><span class="sxs-lookup"><span data-stu-id="2a342-357">AutoGenerate</span></span>      | <span data-ttu-id="2a342-358">これは、自動生成オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-358">This is a Boolean field with possible values of Yes or No for enabling/disabling auto generate option.</span></span> |
|                        | <span data-ttu-id="2a342-359">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="2a342-359">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="2a342-360">AutoDefault</span><span class="sxs-lookup"><span data-stu-id="2a342-360">AutoDefault</span></span>       | <span data-ttu-id="2a342-361">これは、自動既定オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-361">This is a Boolean field with possible values of Yes or No for enabling/disabling auto default option.</span></span> |
|                        | <span data-ttu-id="2a342-362">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="2a342-362">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="2a342-363">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2a342-363">DefaultValue</span></span>      | <span data-ttu-id="2a342-364">これは、自動既定設定が有効な場合に使用される既定値です。</span><span class="sxs-lookup"><span data-stu-id="2a342-364">This is the default value to be used if auto defaulting is enabled.</span></span> |
|                        | <span data-ttu-id="2a342-365">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="2a342-365">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="2a342-366">IgnoreBlankValues</span><span class="sxs-lookup"><span data-stu-id="2a342-366">IgnoreBlankValues</span></span> | <span data-ttu-id="2a342-367">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-367">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |
|                        | <span data-ttu-id="2a342-368">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="2a342-368">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="2a342-369">TextQualifier</span><span class="sxs-lookup"><span data-stu-id="2a342-369">TextQualifier</span></span>     | <span data-ttu-id="2a342-370">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-370">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |
|                        | <span data-ttu-id="2a342-371">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="2a342-371">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="2a342-372">UseEnumLabel</span><span class="sxs-lookup"><span data-stu-id="2a342-372">UseEnumLabel</span></span>      | <span data-ttu-id="2a342-373">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="2a342-373">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |

### <a name="test-groups"></a><span data-ttu-id="2a342-374">テスト グループ</span><span class="sxs-lookup"><span data-stu-id="2a342-374">Test groups</span></span>
<span data-ttu-id="2a342-375">テスト グループは、マニフェストの関連するタスクを整理するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-375">Test groups can be used to organize related tasks in a manifest.</span></span> <span data-ttu-id="2a342-376">マニフェストには複数のテスト グループがあります。</span><span class="sxs-lookup"><span data-stu-id="2a342-376">There can be more than one test group in a manifest.</span></span>

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

| <span data-ttu-id="2a342-377">親要素</span><span class="sxs-lookup"><span data-stu-id="2a342-377">Parent element</span></span>   | <span data-ttu-id="2a342-378">要素</span><span class="sxs-lookup"><span data-stu-id="2a342-378">Element</span></span>           | <span data-ttu-id="2a342-379">要素の基数</span><span class="sxs-lookup"><span data-stu-id="2a342-379">Element Cardinality</span></span> | <span data-ttu-id="2a342-380">属性</span><span class="sxs-lookup"><span data-stu-id="2a342-380">Attributes</span></span>  | <span data-ttu-id="2a342-381">説明</span><span class="sxs-lookup"><span data-stu-id="2a342-381">Description</span></span> |
|------------------|-------------------|---------------------|-------------|-------------|
| <span data-ttu-id="2a342-382">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="2a342-382">\<TestManifest\></span></span> | <span data-ttu-id="2a342-383">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="2a342-383">\<TestGroup\></span></span>     | <span data-ttu-id="2a342-384">1..n</span><span class="sxs-lookup"><span data-stu-id="2a342-384">1..n</span></span>                | \-          | \- |
|                  | <span data-ttu-id="2a342-385">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="2a342-385">\<TestGroup\></span></span>     | <span data-ttu-id="2a342-386">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-386">1..1</span></span>                | <span data-ttu-id="2a342-387">氏名</span><span class="sxs-lookup"><span data-stu-id="2a342-387">Name</span></span>        | <span data-ttu-id="2a342-388">これは、グループの機能上の理由を特定するための名前です。</span><span class="sxs-lookup"><span data-stu-id="2a342-388">This is the name for the group to identify its functional reason.</span></span> |
| <span data-ttu-id="2a342-389">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="2a342-389">\<TestGroup\></span></span>    | <span data-ttu-id="2a342-390">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="2a342-390">\<TestCase\></span></span>      | <span data-ttu-id="2a342-391">1..n</span><span class="sxs-lookup"><span data-stu-id="2a342-391">1..n</span></span>                | \-          | <span data-ttu-id="2a342-392">タスクは、この要素で定義されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-392">The task is defined in this element.</span></span> <span data-ttu-id="2a342-393">タスクでは、タスク パラメータおよびタスク動作を継承する共有設定を参照できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-393">The task can refer to the shared set up to inherit task parameters and task behavior.</span></span> <span data-ttu-id="2a342-394">タスクでは、パラメータと動作もそのレベルで上書きできるため、マニフェストの管理を単純にできます。</span><span class="sxs-lookup"><span data-stu-id="2a342-394">The task can also override parameters and behavior at its level thus making the management of the manifest simple.</span></span> |
|                  | <span data-ttu-id="2a342-395">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="2a342-395">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="2a342-396">肩書き</span><span class="sxs-lookup"><span data-stu-id="2a342-396">Title</span></span>       | <span data-ttu-id="2a342-397">これはタスクのタイトルです。</span><span class="sxs-lookup"><span data-stu-id="2a342-397">This is the title for the task.</span></span> |
|                  | <span data-ttu-id="2a342-398">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="2a342-398">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="2a342-399">ID</span><span class="sxs-lookup"><span data-stu-id="2a342-399">ID</span></span>          | <span data-ttu-id="2a342-400">これはタスクの ID です。</span><span class="sxs-lookup"><span data-stu-id="2a342-400">This is the ID for the task.</span></span> <span data-ttu-id="2a342-401">これは英数字で、最大文字数制限は 10 です。</span><span class="sxs-lookup"><span data-stu-id="2a342-401">This can be alphanumeric with a max character limit of 10.</span></span> |
|                  | <span data-ttu-id="2a342-402">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="2a342-402">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="2a342-403">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="2a342-403">RepeatCount</span></span> | <span data-ttu-id="2a342-404">これは、将来の機能のプレース ホルダーです。</span><span class="sxs-lookup"><span data-stu-id="2a342-404">This is a placeholder for a future functionality.</span></span> <span data-ttu-id="2a342-405">ただし、これは値 *1* で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-405">However, this must be specified with a value of *1*.</span></span> |
|                  | <span data-ttu-id="2a342-406">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="2a342-406">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="2a342-407">TraceParser</span><span class="sxs-lookup"><span data-stu-id="2a342-407">TraceParser</span></span> | <span data-ttu-id="2a342-408">これは、将来の機能のプレース ホルダーです。</span><span class="sxs-lookup"><span data-stu-id="2a342-408">This is a placeholder for a future functionality.</span></span> <span data-ttu-id="2a342-409">ただし、これは値*オフ*で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-409">However, this must be specified with a value *off*.</span></span> |
|                  | <span data-ttu-id="2a342-410">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="2a342-410">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="2a342-411">タイムアウト</span><span class="sxs-lookup"><span data-stu-id="2a342-411">Timeout</span></span>     | <span data-ttu-id="2a342-412">これは、タスク自動化マネージャーによってタスクがモニターされる最大期間です。</span><span class="sxs-lookup"><span data-stu-id="2a342-412">This is the maximum duration a task will be monitored by the task automation manager.</span></span> <span data-ttu-id="2a342-413">指定したタイムアウトを超えてタスクがまだアクティブな場合、マネージャーはマニフェスト内の次のタスクに進みます。</span><span class="sxs-lookup"><span data-stu-id="2a342-413">If the task is still active beyond the timeout specified, the manager will proceed to the next task in the manifest.</span></span> |
| <span data-ttu-id="2a342-414">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="2a342-414">\<TestCase\></span></span>     | <span data-ttu-id="2a342-415">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="2a342-415">\<DataFile\></span></span>      | <span data-ttu-id="2a342-416">1..n</span><span class="sxs-lookup"><span data-stu-id="2a342-416">1..n</span></span>                | \-          | <span data-ttu-id="2a342-417">この要素は、タスクで使用されるファイル、またはデータのプロジェクトを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-417">This element is used to define the file or data package to be used by the task.</span></span> <span data-ttu-id="2a342-418">これは、既に宣言されたファイル、またはマニフェストの共有セクションのデータ パッケージを参照できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-418">This can reference to an already declared file or a data package in the shared section of the manifest.</span></span> <span data-ttu-id="2a342-419">タスクでは、反復バッチ インポート シナリオでのみ指定された複数のデータ ファイルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2a342-419">A task can have more than one data file specified for recurring batch import scenarios only.</span></span> <span data-ttu-id="2a342-420">他のシナリオでは、1 つ以上のファイルが指定されていても、最初のファイルがタスクによって使用されるファイルです。</span><span class="sxs-lookup"><span data-stu-id="2a342-420">For other scenarios, even if more than one files are specified, the first file is what will be used by the task.</span></span> |
|                  | <span data-ttu-id="2a342-421">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="2a342-421">\<JobDefinition\></span></span> | <span data-ttu-id="2a342-422">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-422">1..1</span></span>                | \-          | <span data-ttu-id="2a342-423">この要素は、タスクで使用されるデータのプロジェクトを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-423">This element is used to define the data project to be used by the task.</span></span> <span data-ttu-id="2a342-424">これは、共有セクション内のすでに宣言されているマニフェストのジョブ定義を参照できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-424">This can reference to an already declared job definition in the shared section of the manifest.</span></span> <span data-ttu-id="2a342-425">タスクでは、共有設定で定義されている値よりも新しい値にジョブ定義の要素を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="2a342-425">The task can override elements of job definition to a new value than what is defined in the shared set up.</span></span> |
|                  | <span data-ttu-id="2a342-426">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="2a342-426">\<EntitySetup\></span></span>   | <span data-ttu-id="2a342-427">1..1</span><span class="sxs-lookup"><span data-stu-id="2a342-427">1..1</span></span>                | \-          | <span data-ttu-id="2a342-428">この要素は、タスクで使用されるエンティティのエンティティ セットアップを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-428">This element is used to define the entity set up for entities used by the task.</span></span> <span data-ttu-id="2a342-429">これは、マニフェストの共有のセクションで既に宣言されたエンティティ セットアップを参照できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-429">This can reference to an already declared entity set up in the shared section of the manifest.</span></span> <span data-ttu-id="2a342-430">タスクでは、共有設定で定義されている値よりも新しい値にエンティティ設定の要素を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="2a342-430">The task can override elements of entity setup to a new value than what is defined in the shared set up.</span></span> |

## <a name="best-practices-for-manifest-design"></a><span data-ttu-id="2a342-431">マニフェスト デザインのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="2a342-431">Best practices for manifest design</span></span>
<span data-ttu-id="2a342-432">さまざまな方法でマニフェストを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="2a342-432">You can define a manifest in many ways.</span></span> <span data-ttu-id="2a342-433">マニフェストをデザインするときに考慮する必要があるいくつかのポインターを次に示します。</span><span class="sxs-lookup"><span data-stu-id="2a342-433">Here are a few pointers that you should consider when you design a manifest.</span></span>

### <a name="granularity"></a><span data-ttu-id="2a342-434">粒度</span><span class="sxs-lookup"><span data-stu-id="2a342-434">Granularity</span></span>
<span data-ttu-id="2a342-435">機能的な意思決定としてマニフェストの粒度を判断することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2a342-435">We recommend that you determine the granularity of your manifest as a functional decision.</span></span> <span data-ttu-id="2a342-436">チームは、複数のマニフェストを管理するか、または単一のマニフェストの変更を管理するかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-436">Your team must decide whether it wants to manage many manifests or manage changes in a single manifest.</span></span>

- <span data-ttu-id="2a342-437">チームが論理的に必要と考える数のマニフェストを使って開始します。</span><span class="sxs-lookup"><span data-stu-id="2a342-437">Start with as many manifests as your team thinks you logically need.</span></span> <span data-ttu-id="2a342-438">後で、チームが実際にマニフェストの実行を開始すると、予想より少ないマニフェストを使用しており、それらを結合したいと考える場合があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-438">Later, when the team actually starts to run the manifests, it might find that it uses fewer manifests than it expected, and it might want to merge them.</span></span> <span data-ttu-id="2a342-439">この場合、マニフェストをマージすることができます。</span><span class="sxs-lookup"><span data-stu-id="2a342-439">In this case, you can merge manifests.</span></span>
- <span data-ttu-id="2a342-440">職務の分離を検討する。</span><span class="sxs-lookup"><span data-stu-id="2a342-440">Consider separation of duties.</span></span> <span data-ttu-id="2a342-441">たとえば、デモ データの設定に対して 1 つのマニフェスト、環境の高品質の構成の設定に対して別のマニフェストがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-441">For example, you might have one manifest for the setup of demo data and another manifest for the setup of the golden configuration for your environment.</span></span> <span data-ttu-id="2a342-442">この方法で、チーム メンバーが使用する予定のマニフェストのみを使用することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-442">In this way, you can make sure that team members use only the manifests that they are supposed to use.</span></span>
- <span data-ttu-id="2a342-443">LCS へのユーザー アクセスについて考慮してください。</span><span class="sxs-lookup"><span data-stu-id="2a342-443">Consider user access to LCS.</span></span> <span data-ttu-id="2a342-444">たとえば、大きなおよびグローバルに配分された実装チームは、Finance and Operations の複数のインスタンスまたは複数の LCS プロジェクトを持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-444">For example, larger and globally distributed implementation teams might have multiple instances of Finance and Operations or multiple LCS projects.</span></span>

### <a name="inheritance"></a><span data-ttu-id="2a342-445">継承</span><span class="sxs-lookup"><span data-stu-id="2a342-445">Inheritance</span></span>
<span data-ttu-id="2a342-446">マニフェスト スキーマは、マニフェスト内のすべてのタスクに適用される共通要素の継承をサポートします。</span><span class="sxs-lookup"><span data-stu-id="2a342-446">The manifest schema supports inheritance of common elements that will apply to all tasks in the manifest.</span></span> <span data-ttu-id="2a342-447">タスクは、共通の要素を上書きして一意の動作を定義できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-447">A task can override a common element to define a unique behavior.</span></span> <span data-ttu-id="2a342-448">**共通設定** セクションの目的は、構成要素の繰り返しを最小限に抑えて、可能な限り要素を再利用することです。</span><span class="sxs-lookup"><span data-stu-id="2a342-448">The purpose of the **Shared setup** section is to minimize repetition of configuration elements, so that elements are reused as much as possible.</span></span> <span data-ttu-id="2a342-449">目標は、メンテナンスと可読性を向上させるために、マニフェストを簡潔かつ清潔に保つことです。</span><span class="sxs-lookup"><span data-stu-id="2a342-449">The goal is to keep the manifest concise and clean, to improve maintenance and readability.</span></span>

### <a name="source-control"></a><span data-ttu-id="2a342-450">ソース管理</span><span class="sxs-lookup"><span data-stu-id="2a342-450">Source control</span></span>
<span data-ttu-id="2a342-451">実装チームのすべてのメンバーが使用する必要があるマニフェストは、アプリケーション オブジェクト ツリー (AOT) 内のソース コントロールに格納されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-451">Manifests that must be used by all the members of an implementation team should be stored in source control in the Application Object Tree (AOT).</span></span> <span data-ttu-id="2a342-452">この方法は、ソース管理の利点を提供するだけでなく、プロセスがすべてのユーザーに一貫した方法で配布またはマニフェストを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2a342-452">This approach not only provides the benefits of source control, but also enables a process to distribute or make manifests available to all users in a consistent manner.</span></span> <span data-ttu-id="2a342-453">また、この方法では、マニフェストを構成に使用する場合、データ管理に関連するデータ プロジェクトの構成管理も可能です。</span><span class="sxs-lookup"><span data-stu-id="2a342-453">This approach also enables configuration management for data projects that are related to data management, if manifests are used for configuration.</span></span>

### <a name="number-of-job-definitions-and-entity-definitions"></a><span data-ttu-id="2a342-454">ジョブ定義とエンティティ定義の数</span><span class="sxs-lookup"><span data-stu-id="2a342-454">Number of job definitions and entity definitions</span></span>
<span data-ttu-id="2a342-455">使用ケースのほとんどの場合、マニフェストで 1 つのジョブ定義で十分であるのは、継承がタスク レベルでの動作を変更するために使用できるからです。</span><span class="sxs-lookup"><span data-stu-id="2a342-455">For most of the use cases, one job definition in a manifest should be enough, because inheritance can be used to change the behavior at the task level.</span></span> <span data-ttu-id="2a342-456">この原則は、エンティティの定義にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-456">This principle also applies to entity definitions.</span></span>

## <a name="validations"></a><span data-ttu-id="2a342-457">検証</span><span class="sxs-lookup"><span data-stu-id="2a342-457">Validations</span></span>
<span data-ttu-id="2a342-458">データ タスク自動化マネージャは、タスクの設定に基づいて検証を実行します。</span><span class="sxs-lookup"><span data-stu-id="2a342-458">Data task automation manager performs validations, based on the setup of a task.</span></span> <span data-ttu-id="2a342-459">タスクが失敗した場合は、タスクの完了後に、検証を表示することによって、エラーの原因をすばやく確認できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-459">If a task fails, you can quickly determine the reason for the failure by viewing the validations after the task is completed.</span></span> <span data-ttu-id="2a342-460">データ タスク自動化マネージャーが提供する情報のレベルは、初期検出を容易にするために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="2a342-460">The level of information that Data task automation manager provides is optimized to facilitate initial discovery.</span></span> <span data-ttu-id="2a342-461">詳細な調査のためには、対応するデータ プロジェクトおよびその実行の詳細を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-461">For detailed investigation, you must look at the corresponding data project and its execution details.</span></span>

<span data-ttu-id="2a342-462">現在、次のデータ検証がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="2a342-462">The following data validations are currently supported:</span></span>

- <span data-ttu-id="2a342-463">**ジョブ ステータス** – この検証は、ジョブが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="2a342-463">**Job status** – This validation checks whether the job was successful.</span></span>
- <span data-ttu-id="2a342-464">**バッチ ステータス** - この検証は、バッチが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="2a342-464">**Batch status** – This validation checks whether the batch was successful.</span></span>
- <span data-ttu-id="2a342-465">**メッセージ状態** – テストが統合に関するものである場合、メッセージの状態が検証されます。</span><span class="sxs-lookup"><span data-stu-id="2a342-465">**Message status** – If the test is about integrations, the message status is validated.</span></span>
- <span data-ttu-id="2a342-466">**切り捨て** – 切り捨てが有効になっている場合は、この検証が切り捨てが発生したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="2a342-466">**Truncation** – If truncation is enabled, this validation checks whether truncation occurred.</span></span>
- <span data-ttu-id="2a342-467">**ステージングのスキップ** – **ステージングのスキップ** がテストで有効になっている場合、ステージングがスキップされたかどうかをこの検証でチェックします。</span><span class="sxs-lookup"><span data-stu-id="2a342-467">**Skip staging** – If **Skip staging** is enabled on a test, this validation checks whether staging was skipped.</span></span>

## <a name="example-1-configuration-management-for-data-projects"></a><span data-ttu-id="2a342-468">例 1: データ プロジェクトの構成管理</span><span class="sxs-lookup"><span data-stu-id="2a342-468">Example 1: Configuration management for data projects</span></span>
<span data-ttu-id="2a342-469">**\<ConfigurationOnly\>** 要素は、データ プロジェクトおよび定期的なスケジュールの構成タスクを作成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a342-469">The **\<ConfigurationOnly\>** element can be used to create configuration tasks for data projects and recurring schedules.</span></span>

<span data-ttu-id="2a342-470">この最初の例は、定期的なスケジュールを持たないデータ プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="2a342-470">This first example configures a data project that doesn't have a recurring schedule.</span></span> <span data-ttu-id="2a342-471">2 番目の例には、定期的なスケジュールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2a342-471">The second example includes a recurring schedule.</span></span> <span data-ttu-id="2a342-472">違いは、**\<Operation\>** 要素の値です。</span><span class="sxs-lookup"><span data-stu-id="2a342-472">The difference is the value of the **\<Operation\>** element.</span></span> <span data-ttu-id="2a342-473">構成タスクのマニフェストは、ソース コントロール下にも保管する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a342-473">Manifests for configuration tasks should also be kept under source control.</span></span>

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

## <a name="example-2-automated-setup-of-demo-data"></a><span data-ttu-id="2a342-474">例 2: デモ データの自動設定</span><span class="sxs-lookup"><span data-stu-id="2a342-474">Example 2: Automated setup of demo data</span></span>
<span data-ttu-id="2a342-475">次のマニフェストは、デモ データ パッケージが共有アセット ライブラリに格納されている場合の 3 つの法人のデモ データの設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="2a342-475">The following manifest shows the setup of demo data for three legal entities when the demo data packages are stored in the Shared asset library.</span></span>

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
