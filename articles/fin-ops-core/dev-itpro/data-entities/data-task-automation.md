---
title: データ タスクの自動化
description: このトピックでは、データ タスクの自動化により、さまざまな種類のデータ タスクを簡単に繰り返し、各タスクの結果を検証する方法について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform update 16
ms.openlocfilehash: 066f685fc861f49e8ea4ac580c919b0a60adba29
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130045"
---
# <a name="data-task-automation"></a><span data-ttu-id="de205-103">データ タスクの自動化</span><span class="sxs-lookup"><span data-stu-id="de205-103">Data task automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="de205-104">データ タスクの自動化により、さまざまな種類のデータ タスクを簡単に繰り返し、各タスクの結果を検証することができます。</span><span class="sxs-lookup"><span data-stu-id="de205-104">Data task automation lets you easily repeat many types of data tasks and validate the outcome of each task.</span></span> <span data-ttu-id="de205-105">データ タスクの自動化は、実装フェーズにあるプロジェクトで非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="de205-105">Data task automation is very useful for projects that are in the implementation phase.</span></span> <span data-ttu-id="de205-106">たとえば、データ プロジェクトの作成およびコンフィギュレーションを自動化することができます。</span><span class="sxs-lookup"><span data-stu-id="de205-106">For example, you can automate the creation and configuration of data projects.</span></span> <span data-ttu-id="de205-107">また、デモ データおよび高品質の構成データ、およびデータ移行に関連する他のタスクなどの、インポート/エクスポート オペレーションの実行を構成およびトリガーすることができます。</span><span class="sxs-lookup"><span data-stu-id="de205-107">You can also configure and trigger the execution of import/export operations, such as the setup of demo data and golden configuration data, and other tasks that are related to data migration.</span></span> <span data-ttu-id="de205-108">また、タスクの結果の検証を使用して、データ エンティティの自動テストを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="de205-108">You can also create automated testing of data entities by using task outcome validation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de205-109">現時点では、オンプレミス環境ではデータ タスクの自動化はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="de205-109">Data task automation isn't currently supported for on-premises environments.</span></span>
> <span data-ttu-id="de205-110">データタスクの自動化を実行するユーザーは、アプリケーションの環境および LCS プロジェクトと同じテナントに存在するユーザーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-110">The user who executes data task automation must be in the same tenant as the application environment and LCS project.</span></span>

<span data-ttu-id="de205-111">データ タスクの自動化のために次の方法をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="de205-111">We recommend the following approach for data task automation.</span></span>

1. <span data-ttu-id="de205-112">自動化の恩恵を受けるデータ関連のタスクを特定する。</span><span class="sxs-lookup"><span data-stu-id="de205-112">Identify the data-related tasks that will benefit from automation.</span></span>

    <span data-ttu-id="de205-113">実装チームは自分たちの構成管理計画とデータ移行計画をレビューして、自動化のための潜在的なデータ タスクを識別すること、またデータ エンティティのテスト ケースも識別することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="de205-113">We recommend that implementation teams review their configuration management plan and data migration plan to identify potential data tasks for automation, and also to identify data entity test cases.</span></span>

2. <span data-ttu-id="de205-114">タスクを定義します。</span><span class="sxs-lookup"><span data-stu-id="de205-114">Define tasks.</span></span>

    <span data-ttu-id="de205-115">タスクは、XML マニフェストで定義されます。</span><span class="sxs-lookup"><span data-stu-id="de205-115">Tasks are defined in an XML manifest.</span></span> <span data-ttu-id="de205-116">アプリケーション ライフ サイクルの管理 (ALM) 戦略では、構成管理の一部としてソース管理下のマニフェストを保持することができます。</span><span class="sxs-lookup"><span data-stu-id="de205-116">You can keep your manifest under source control as part of configuration management in your application lifecycle management (ALM) strategy.</span></span>

3. <span data-ttu-id="de205-117">Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリに、データ タスクの自動化に関連するデータ パッケージを配置します。</span><span class="sxs-lookup"><span data-stu-id="de205-117">Put the data packages that are related to data task automation in the Shared asset library of Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="de205-118">また、必要に応じて特定の LCS プロジェクトを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="de205-118">You can also use a specific LCS project as you require.</span></span>

    <span data-ttu-id="de205-119">データ タスク自動化マネージャは、LCS プロジェクトに関連するサンドボックスまたは実稼動環境からパッケージを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="de205-119">Data task automation manager can consume packages from any sandbox and/or production environment that is related to the LCS project.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="de205-120">データ タスク自動化マネージャーを実行するユーザー アカウントは、LCS およびデータ パッケージのマニフェストで参照される LCS プロジェクトにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-120">The user account that runs Data task automation manager must have access to LCS and to the LCS project that is referenced in the manifest for data packages.</span></span>
    > - <span data-ttu-id="de205-121">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合アプリケーション プログラミング インターフェイス (API) を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="de205-121">Although data task automation can be run in any environment in the cloud, we strongly recommend that you not run any import/export tasks that use integration application programming interfaces (APIs) in a production environment.</span></span> <span data-ttu-id="de205-122">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-122">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

4. <span data-ttu-id="de205-123">データ タスクを実行し、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="de205-123">Run the data tasks, and then review the outcomes.</span></span>

    <span data-ttu-id="de205-124">データ タスク自動化マネージャは、各タスクの成功または失敗の結果を提供します。</span><span class="sxs-lookup"><span data-stu-id="de205-124">Data task automation manager provides the success or failure outcome for each task.</span></span> <span data-ttu-id="de205-125">また、タスクが失敗した理由に関する見解も提供します。</span><span class="sxs-lookup"><span data-stu-id="de205-125">It also provides insights into the reason why a task failed.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="de205-126">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合 API を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="de205-126">Although data task automation can be run in any environments in the cloud, we recommend that you not run any import/export tasks that use integration APIs in a production environment.</span></span> <span data-ttu-id="de205-127">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-127">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

<span data-ttu-id="de205-128">次のビデオは、Data Task Automation Manager の初期リリースを紹介する TechTalk の 55 分です。[タスク自動化フレームワーク](https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4)。</span><span class="sxs-lookup"><span data-stu-id="de205-128">The following video is a 55-minute TechTalk that walks you through an early release of Data task automation manager: [Task automation framework](https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4).</span></span>

## <a name="task-manifest"></a><span data-ttu-id="de205-129">タスク マニフェスト</span><span class="sxs-lookup"><span data-stu-id="de205-129">Task manifest</span></span>
<span data-ttu-id="de205-130">タスクは、XML マニフェストで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-130">A task must be defined in an XML manifest.</span></span> <span data-ttu-id="de205-131">このセクションでは、マニフェストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="de205-131">This section describes the manifest.</span></span> <span data-ttu-id="de205-132">マニフェストを名前付けしデザインする方法の指針については、このトピックの後半の、「マニフェストのデザインに対するベスト プラクティス」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de205-132">For guidance about how to name and design the manifest, see the "Best practices for manifest design" section later in this topic.</span></span>

### <a name="manifest-root"></a><span data-ttu-id="de205-133">マニフェスト ルート</span><span class="sxs-lookup"><span data-stu-id="de205-133">Manifest root</span></span>
<span data-ttu-id="de205-134">**\<TestManifest\>** 要素は、マニフェストのルートです。</span><span class="sxs-lookup"><span data-stu-id="de205-134">The **\<TestManifest\>** element is the root of the manifest.</span></span> <span data-ttu-id="de205-135">その他のすべての要素はこの要素の子です。</span><span class="sxs-lookup"><span data-stu-id="de205-135">All other elements are children of this element.</span></span>

```xml
<?xml version='1.0' encoding='utf-8'?>
<TestManifest name='Data management demo data set up'>
    <SharedSetup />
        <JobDefinition ID='ImportJobDefinition_1' />
        <EntitySetup ID='Generic' />
    </SharedSetup>
    <TestGroup />
</TestManifest>
```

| <span data-ttu-id="de205-136">要素</span><span class="sxs-lookup"><span data-stu-id="de205-136">Element</span></span>          | <span data-ttu-id="de205-137">要素の基数</span><span class="sxs-lookup"><span data-stu-id="de205-137">Element Cardinality</span></span> | <span data-ttu-id="de205-138">属性</span><span class="sxs-lookup"><span data-stu-id="de205-138">Attributes</span></span> | <span data-ttu-id="de205-139">属性の説明</span><span class="sxs-lookup"><span data-stu-id="de205-139">Attribute description</span></span>                                     |
|------------------|---------------------|------------|-----------------------------------------------------------|
| \<TestManifest\> | <span data-ttu-id="de205-140">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-140">1..1</span></span>                | <span data-ttu-id="de205-141">名前</span><span class="sxs-lookup"><span data-stu-id="de205-141">name</span></span>       | <span data-ttu-id="de205-142">*名前* はマニフェストの目的を識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="de205-142">The *name* helps to identify the purpose of the manifest.</span></span> |

### <a name="shared-setup"></a><span data-ttu-id="de205-143">共有された設定</span><span class="sxs-lookup"><span data-stu-id="de205-143">Shared setup</span></span>
<span data-ttu-id="de205-144">**共有セットアップ** セクションは、全般的なタスクのパラメーターとマニフェスト内のすべてのタスクの動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="de205-144">The **Shared setup** section defines general task parameters and behaviors for all tasks in the manifest.</span></span>

| <span data-ttu-id="de205-145">親要素</span><span class="sxs-lookup"><span data-stu-id="de205-145">Parent element</span></span>   | <span data-ttu-id="de205-146">要素</span><span class="sxs-lookup"><span data-stu-id="de205-146">Element</span></span>         | <span data-ttu-id="de205-147">要素の基数</span><span class="sxs-lookup"><span data-stu-id="de205-147">Element Cardinality</span></span> | <span data-ttu-id="de205-148">属性</span><span class="sxs-lookup"><span data-stu-id="de205-148">Attributes</span></span> | <span data-ttu-id="de205-149">属性の説明</span><span class="sxs-lookup"><span data-stu-id="de205-149">Attribute description</span></span>            |
|------------------|-----------------|---------------------|------------|----------------------------------|
| \<TestManifest\> | \<SharedSetup\> | <span data-ttu-id="de205-150">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-150">1..1</span></span>                | \-         | <span data-ttu-id="de205-151">この要素には属性はありません。</span><span class="sxs-lookup"><span data-stu-id="de205-151">This element takes no attributes.</span></span> |

### <a name="data-files"></a><span data-ttu-id="de205-152">データ ファイル</span><span class="sxs-lookup"><span data-stu-id="de205-152">Data files</span></span>
<span data-ttu-id="de205-153">**\<DataFile\>** 要素は、マニフェスト内のタスクが使用するデータ パッケージおよびデータ ファイルを定義します。</span><span class="sxs-lookup"><span data-stu-id="de205-153">**\<DataFile\>** elements define the data packages and data files that the tasks in the manifest will use.</span></span> <span data-ttu-id="de205-154">データ ファイルは、LCS プロジェクトの LCS アセット ライブラリまたは共有アセット ライブラリのいずれかになければなりません。</span><span class="sxs-lookup"><span data-stu-id="de205-154">The data files must be either in the LCS asset library of your LCS project or in the Shared asset library.</span></span>

```xml
<DataFile ID='SharedSetup' name='Demo data-7.3-100-System and Shared'  assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsHQUS' name='Demo data-7.3-200-Financials-HQUS' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPICH' name='Demo data-7.3-200-Financials-PICH' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPIFB' name='Demo data-7.3-200-Financials-PIFB' assetType='Data package' lcsProjectId=''/>
```

| <span data-ttu-id="de205-155">親要素</span><span class="sxs-lookup"><span data-stu-id="de205-155">Parent element</span></span>  | <span data-ttu-id="de205-156">要素</span><span class="sxs-lookup"><span data-stu-id="de205-156">Element</span></span>      | <span data-ttu-id="de205-157">要素の基数</span><span class="sxs-lookup"><span data-stu-id="de205-157">Element Cardinality</span></span> | <span data-ttu-id="de205-158">属性</span><span class="sxs-lookup"><span data-stu-id="de205-158">Attributes</span></span>   | <span data-ttu-id="de205-159">属性の説明</span><span class="sxs-lookup"><span data-stu-id="de205-159">Attribute description</span></span> |
|-----------------|--------------|---------------------|--------------|-----------------------|
| \<SharedSetup\> | \<DataFile\> | <span data-ttu-id="de205-160">1..n</span><span class="sxs-lookup"><span data-stu-id="de205-160">1..n</span></span>                | \-           | \- |
|                 | \<DataFile\> | \-                  | <span data-ttu-id="de205-161">ID</span><span class="sxs-lookup"><span data-stu-id="de205-161">ID</span></span>           | |
|                 | \<DataFile\> | \-                  | <span data-ttu-id="de205-162">名前</span><span class="sxs-lookup"><span data-stu-id="de205-162">name</span></span>         | <span data-ttu-id="de205-163">データ ファイルを表す資産の名前。</span><span class="sxs-lookup"><span data-stu-id="de205-163">Name of the asset that represents the data file.</span></span> |
|                 | \<DataFile\> | \-                  | <span data-ttu-id="de205-164">assetType</span><span class="sxs-lookup"><span data-stu-id="de205-164">assetType</span></span>    | <span data-ttu-id="de205-165">データ ファイルを格納する LCS 資産ライブラリでの資産タイプ。</span><span class="sxs-lookup"><span data-stu-id="de205-165">The asset type in LCS asset library that stores the data file.</span></span> <span data-ttu-id="de205-166">これは、LCS アセット ライブラリで示されたように、アセット タイプの名前です。</span><span class="sxs-lookup"><span data-stu-id="de205-166">This is the asset type name as shown in LCS asset library.</span></span> |
|                 | \<DataFile\> | \-                  | <span data-ttu-id="de205-167">lcsProjectId</span><span class="sxs-lookup"><span data-stu-id="de205-167">lcsProjectId</span></span> | <span data-ttu-id="de205-168">その資産ライブラリで LCS プロジェクトにはデータ ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="de205-168">The LCS project that has the data file in its asset library.</span></span> <span data-ttu-id="de205-169">プロジェクト ID が " として指定されている場合は、共有アセット ライブラリを示します。</span><span class="sxs-lookup"><span data-stu-id="de205-169">If the project ID is specified as '' then, it indicates the Shared asset library.</span></span> |

### <a name="data-project-definition"></a><span data-ttu-id="de205-170">データ プロジェクト定義</span><span class="sxs-lookup"><span data-stu-id="de205-170">Data project definition</span></span>
<span data-ttu-id="de205-171">**\<JobDefinition\>** 要素は、データ プロジェクト定義を定義します。</span><span class="sxs-lookup"><span data-stu-id="de205-171">The **\<JobDefinition\>** element defines the data project definition.</span></span> <span data-ttu-id="de205-172">マニフェストには複数のジョブ定義があります。</span><span class="sxs-lookup"><span data-stu-id="de205-172">There can be more than one job definition in a manifest.</span></span>

```xml
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

| <span data-ttu-id="de205-173">親要素</span><span class="sxs-lookup"><span data-stu-id="de205-173">Parent element</span></span>    | <span data-ttu-id="de205-174">要素</span><span class="sxs-lookup"><span data-stu-id="de205-174">Element</span></span>                          | <span data-ttu-id="de205-175">要素の基数</span><span class="sxs-lookup"><span data-stu-id="de205-175">Element cardinality</span></span> | <span data-ttu-id="de205-176">属性</span><span class="sxs-lookup"><span data-stu-id="de205-176">Attribute</span></span> | <span data-ttu-id="de205-177">説明</span><span class="sxs-lookup"><span data-stu-id="de205-177">Description</span></span> |
|-------------------|----------------------------------|---------------------|-----------|-------------|
| \<SharedSetup\>   | \<JobDefinition\>                | <span data-ttu-id="de205-178">1..n</span><span class="sxs-lookup"><span data-stu-id="de205-178">1..n</span></span>                | <span data-ttu-id="de205-179">ID</span><span class="sxs-lookup"><span data-stu-id="de205-179">ID</span></span>        | <span data-ttu-id="de205-180">タスクでジョブ定義 ID を使用してデータ プロジェクトで使用する定義を参照できます。</span><span class="sxs-lookup"><span data-stu-id="de205-180">The job definition ID is used in the tasks to reference the definition to be used for the data project.</span></span> |
| \<JobDefinition\> | \<Operation\>                    | <span data-ttu-id="de205-181">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-181">1..1</span></span>                | \-        | <span data-ttu-id="de205-182">実行される操作は、次の値によって指定されます。</span><span class="sxs-lookup"><span data-stu-id="de205-182">The operation to be performed is specified by the following values:</span></span> <br> <span data-ttu-id="de205-183">- インポート</span><span class="sxs-lookup"><span data-stu-id="de205-183">- Import</span></span> <br> <span data-ttu-id="de205-184">- エクスポート</span><span class="sxs-lookup"><span data-stu-id="de205-184">- Export</span></span> |
|                   | \<Truncate\>                     | <span data-ttu-id="de205-185">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-185">1..1</span></span>                | \-        | <span data-ttu-id="de205-186">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-186">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="de205-187">これは操作が *インポート* に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-187">This is applicable only when operation is set to *Import*.</span></span> |
|                   | \<Mode\>                         | <span data-ttu-id="de205-188">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-188">1..1</span></span>                | \-        | <span data-ttu-id="de205-189">モードでは、操作を実行する必要があるメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="de205-189">The mode specifies the method using which the operation must be performed.</span></span> <span data-ttu-id="de205-190">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="de205-190">The possible values are:</span></span><br><span data-ttu-id="de205-191">- 非同期インポート</span><span class="sxs-lookup"><span data-stu-id="de205-191">- Import async</span></span> <br><span data-ttu-id="de205-192">- 非同期エクスポート</span><span class="sxs-lookup"><span data-stu-id="de205-192">- Export async</span></span> <br><span data-ttu-id="de205-193">- 定期的に実行するバッチ: エンキュー API を使用します。</span><span class="sxs-lookup"><span data-stu-id="de205-193">- Recurring batch: This uses the enqueue API.</span></span> <span data-ttu-id="de205-194">デキュー API には現在対応していません。</span><span class="sxs-lookup"><span data-stu-id="de205-194">Dequeue API is not supported yet.</span></span> <span data-ttu-id="de205-195">パッケージAPIは、エクスポートとインポートの両方に対応しています。</span><span class="sxs-lookup"><span data-stu-id="de205-195">Package API supports both export and import.</span></span>|
|                   | \<ConfigurationOnly\>            | <span data-ttu-id="de205-196">0..1</span><span class="sxs-lookup"><span data-stu-id="de205-196">0..1</span></span>                | \-        | <span data-ttu-id="de205-197">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-197">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="de205-198">タスクがデータ プロジェクトをコンフィギュレーションするのみで、指定された操作を実行しない場合は、はいに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-198">This must be set to Yes if the task is only to configure the data project but not to perform the specified operation.</span></span> |
|                   | \<BatchFrequencyInMinutes\>      | <span data-ttu-id="de205-199">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-199">1..1</span></span>                | \-        | <span data-ttu-id="de205-200">バッチがスケジュール設定される頻度を指定します。</span><span class="sxs-lookup"><span data-stu-id="de205-200">This specifies the frequency in which the batch must be scheduled.</span></span> <span data-ttu-id="de205-201">これはモードが *定期実行されるバッチ* に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-201">This is applicable only when mode is set to *recurring batch*.</span></span> |
|                   | \<NumberOfTimesToRunBatch\>      | <span data-ttu-id="de205-202">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-202">1..1</span></span>                | \-        | <span data-ttu-id="de205-203">これは、スケジュールされているバッチを実行する回数の制限を設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-203">This is used to set a limit to how many times the scheduled batch should run.</span></span> <span data-ttu-id="de205-204">これはモードが *定期実行されるバッチ* に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-204">This is applicable only when mode is set to *recurring batch*.</span></span> |
|                   | \<UploadFrequencyInSeconds\>     | <span data-ttu-id="de205-205">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-205">1..1</span></span>                | \-        | <span data-ttu-id="de205-206">これは、インポートする定期バッチ ジョブにファイルをアップロードする頻度を制御するために使用します。</span><span class="sxs-lookup"><span data-stu-id="de205-206">This is used to control the rate at which a file is uploaded to the recurring batch job for import.</span></span> <span data-ttu-id="de205-207">これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-207">This must be used only for automated testing of recurring integrations in non-production environments.</span></span> <span data-ttu-id="de205-208">これはモードが *定期実行されるバッチ* に設定されており、操作が *インポート* に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-208">This is applicable only when mode is set to *recurring batch* and operation is set to *Import*.</span></span> |
|                   | \<TotalNumberOfTimesToUpload\>   | <span data-ttu-id="de205-209">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-209">1..1</span></span>                |           | <span data-ttu-id="de205-210">これはファイルを繰り返しバッチにアップロードする総回数を制御します。</span><span class="sxs-lookup"><span data-stu-id="de205-210">This controls the total number of times the file should be uploaded to the recurring batch.</span></span> <span data-ttu-id="de205-211">これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-211">This must be used only for automated testing of recurring integrations in non-production environments.</span></span> <span data-ttu-id="de205-212">これはモードが *定期実行されるバッチ* に設定されており、操作が *インポート* に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-212">This is applicable only when mode is set to *recurring batch* and operation is set to *Import*.</span></span> |
|                   | \<SupportedDataSoureType\>       | <span data-ttu-id="de205-213">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-213">1..1</span></span>                |           | <span data-ttu-id="de205-214">ファイルが定期的なバッチまたはパッケージに送信中であるかどうかを指定するために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-214">This must be used to specify if a file is being sent to the recurring batch or a package.</span></span> <span data-ttu-id="de205-215">これはモードが「定期実行されるバッチ」に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-215">This is only applicable when mode is set to 'recurring batch'.</span></span> |
|                   | \<ProcessMessagesInOrder\>       | <span data-ttu-id="de205-216">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-216">1..1</span></span>                |           | <span data-ttu-id="de205-217">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-217">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="de205-218">これはモードが *定期実行されるバッチ* に設定されており、操作が *インポート* の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-218">This is applicable only when mode is set to *recurring batch* and operation is *Import*.</span></span> |
|                   | \<PreventUploadWhenZeroRecords\> | <span data-ttu-id="de205-219">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-219">1..1</span></span>                |           | <span data-ttu-id="de205-220">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-220">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="de205-221">これはモードが *定期実行されるバッチ* に設定されており、操作が *エクスポート* の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-221">This is applicable only when mode is set to *recurring batch* and operation is *Export*.</span></span> |
|                   | \<UseCompanyFromMessage\>        | <span data-ttu-id="de205-222">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-222">1..1</span></span>                |           | <span data-ttu-id="de205-223">これははい、またはいいえに設定できるブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-223">This is a Boolean field which can be set to Yes or No.</span></span> <span data-ttu-id="de205-224">これはモードが *定期実行されるバッチ* に設定されており、操作が *インポート* の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-224">This is applicable only when mode is set to *recurring batch* and operation is *Import*.</span></span> |
|                   | \<LegalEntity\>                  | <span data-ttu-id="de205-225">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-225">1..1</span></span>                |           | <span data-ttu-id="de205-226">これをは、インポート/エクスポート ジョブを実行する必要がある法人を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-226">This is used to specify the legal entity in which the import/export job must be executed.</span></span> |
|                   | \<PackageAPIExecute\>            | <span data-ttu-id="de205-227">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-227">1..1</span></span>                |           | <span data-ttu-id="de205-228">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de205-228">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="de205-229">これは、"true" または "false" を取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-229">This is a Boolean field which takes 'true' or 'false'.</span></span> |
|                   | \<PackageAPIOverwrite\>            | <span data-ttu-id="de205-230">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-230">1..1</span></span>                |           | <span data-ttu-id="de205-231">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de205-231">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="de205-232">これは、"true" または "false" を取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-232">This is a Boolean field which takes 'true' or 'false'.</span></span> |
|                   | \<PackageAPIReexecute\>            | <span data-ttu-id="de205-233">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-233">1..1</span></span>                |           | <span data-ttu-id="de205-234">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de205-234">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="de205-235">これは、"true" または "false" を取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-235">This is a Boolean field which takes 'true' or 'false'.</span></span> |
|                   | \<DefinitionGroupID\>            | <span data-ttu-id="de205-236">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-236">1..1</span></span>                |           | <span data-ttu-id="de205-237">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de205-237">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="de205-238">これは文字列フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-238">This is a string field.</span></span> |
|                   | \<PackageName\>            | <span data-ttu-id="de205-239">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-239">1..1</span></span>                |           | <span data-ttu-id="de205-240">このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de205-240">Refer to package API documentation to understand this parameter.</span></span> <span data-ttu-id="de205-241">これは文字列フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-241">This is a string field.</span></span> |

### <a name="entity-setup"></a><span data-ttu-id="de205-242">エンティティ設定</span><span class="sxs-lookup"><span data-stu-id="de205-242">Entity setup</span></span>
<span data-ttu-id="de205-243">**エンティティ設定** セクションは、マニフェストのタスクが使用するエンティティの特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="de205-243">The **Entity setup** section defines the characteristics of an entity that a task in the manifest will use.</span></span> <span data-ttu-id="de205-244">マニフェスト内のタスクによって使用されるエンティティごとに、1 つずつ複数の定義が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="de205-244">There can be more than one definition, one for each entity that is used by the tasks in the manifest.</span></span>

```xml
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

| <span data-ttu-id="de205-245">親要素</span><span class="sxs-lookup"><span data-stu-id="de205-245">Parent element</span></span>         | <span data-ttu-id="de205-246">要素</span><span class="sxs-lookup"><span data-stu-id="de205-246">Element</span></span>                              | <span data-ttu-id="de205-247">要素の基数</span><span class="sxs-lookup"><span data-stu-id="de205-247">Element cardinality</span></span> | <span data-ttu-id="de205-248">属性</span><span class="sxs-lookup"><span data-stu-id="de205-248">Attribute</span></span>         | <span data-ttu-id="de205-249">説明</span><span class="sxs-lookup"><span data-stu-id="de205-249">Description</span></span> |
|------------------------|--------------------------------------|---------------------|-------------------|-------------|
| \<SharedSetup\>        | \<EntitySetup\>                      | <span data-ttu-id="de205-250">1..n</span><span class="sxs-lookup"><span data-stu-id="de205-250">1..n</span></span>                | <span data-ttu-id="de205-251">ID</span><span class="sxs-lookup"><span data-stu-id="de205-251">ID</span></span>                | <span data-ttu-id="de205-252">タスクが使用するエンティティ定義を参照するために使用される ID。</span><span class="sxs-lookup"><span data-stu-id="de205-252">An identification that will be used by tasks to reference an entity definition to be used.</span></span> |
| \<EntitySetup\>        | \<Entity\>                           | <span data-ttu-id="de205-253">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-253">1..1</span></span>                | <span data-ttu-id="de205-254">名前</span><span class="sxs-lookup"><span data-stu-id="de205-254">name</span></span>              | <span data-ttu-id="de205-255">エンティティ要素は、エンティティの名前で識別されます。</span><span class="sxs-lookup"><span data-stu-id="de205-255">The entity element is identified by the entity's name.</span></span> <span data-ttu-id="de205-256">ただし、簡単なマニフェスト定義を容易にするために、この要素は \* ワイルド カードとしてもサポートしています。これは、すべてのエンティティがタスクで使用されていることを意味しています。</span><span class="sxs-lookup"><span data-stu-id="de205-256">However, to facilitate easy manifest definition, this element also supports \* as a wild card which will mean all entities being used in a task.</span></span> <span data-ttu-id="de205-257">これは、タスク内の何百ものエンティティを持つデータ パッケージを使用する場合に非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="de205-257">This comes in very handy when using data packages with hundreds of entities in a task.</span></span> |
| \<Entity\>             | \<SourceDataFormatName\>             | <span data-ttu-id="de205-258">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-258">1..1</span></span>                | \-                | <span data-ttu-id="de205-259">これはエンティティに使用されるファイル形式です。</span><span class="sxs-lookup"><span data-stu-id="de205-259">This is the file format to be used for the entity.</span></span> |
|                        | \<ChangeTracking\>                   | <span data-ttu-id="de205-260">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-260">1..1</span></span>                | \-                | <span data-ttu-id="de205-261">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-261">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="de205-262">エンティティ全体で変更追跡を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="de205-262">It enables or disables change tracking on the entire entity.</span></span> |
|                        | \<PublishToBYOD\>                    | <span data-ttu-id="de205-263">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-263">1..1</span></span>                | \-                | <span data-ttu-id="de205-264">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-264">This is a Boolean field with possible values of Yes or No.</span></span> |
|                        | \<DefaultRefreshType\>               | <span data-ttu-id="de205-265">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-265">1..1</span></span>                | \-                | <span data-ttu-id="de205-266">これにより、エンティティの既定の更新頻度が設定されます。</span><span class="sxs-lookup"><span data-stu-id="de205-266">This sets the default refresh rate on the entity.</span></span> <span data-ttu-id="de205-267">使用可能な値は *増分プッシュのみ* または *フル プッシュ* です。</span><span class="sxs-lookup"><span data-stu-id="de205-267">The possible values are *Incremental push only* or *Full push*.</span></span> |
|                        | \<ExcelWorkSheetName\>               | <span data-ttu-id="de205-268">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-268">1..1</span></span>                | \-                | <span data-ttu-id="de205-269">これはエンティティに使用するワークシートを指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-269">This is used to specify the worksheet to be used for the entity.</span></span> |
|                        | \<SelectFields\>                     | <span data-ttu-id="de205-270">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-270">1..1</span></span>                | \-                | <span data-ttu-id="de205-271">これは、エクスポート操作のテンプレートに含まれるフィールドを指定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="de205-271">This can be used to specify the fields to be included in the template for an export operation.</span></span> |
|                        | \<SetBasedProcessing\>               | <span data-ttu-id="de205-272">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-272">1..1</span></span>                | \-                | <span data-ttu-id="de205-273">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-273">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="de205-274">エンティティのセット ベースのプロセスを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-274">It is used to enable or disable set based processing on an entity.</span></span> |
|                        | \<FailBatchOnErrorForExecutionUnit\> | <span data-ttu-id="de205-275">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-275">1..1</span></span>                | \-                | <span data-ttu-id="de205-276">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-276">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="de205-277">エンティティの実行単位レベルでエラーを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-277">It is used to enable or disable failure at execution unit level on an entity.</span></span> |
|                        | \<FailBatchOnErrorForLevel\>         | <span data-ttu-id="de205-278">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-278">1..1</span></span>                | \-                | <span data-ttu-id="de205-279">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-279">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="de205-280">エンティティの実行レベルでエラーを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-280">It is used to enable or disable failure at execution level on an entity.</span></span> |
|                        | \<DisableEntity\>                    | <span data-ttu-id="de205-281">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-281">1..1</span></span>                | \-                | <span data-ttu-id="de205-282">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-282">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="de205-283">データ プロジェクトでエンティティを有効化または無効化するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-283">It is used to enable or disable an entity in a data project.</span></span> |
|                        | \<SkipStaging\>                      | <span data-ttu-id="de205-284">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-284">1..1</span></span>                | \-                | <span data-ttu-id="de205-285">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-285">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="de205-286">エクスポート中にエンティティのステージング テーブルをスキップするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-286">It is used to skip staging table for an entity during exports.</span></span> |
|                        | \<ParallelProcessing\>               | <span data-ttu-id="de205-287">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-287">1..1</span></span>                | \-                | <span data-ttu-id="de205-288">これは、エンティティに対して設定された並列処理を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-288">This is used to define the parallel processing set up for an entity.</span></span> <span data-ttu-id="de205-289">タスクの始まりで既に終了する場合、タスクはこれらの設定を削除し、その実行の終わりに作成された設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="de205-289">The task will delete these settings if already exits at the beginning of the task and it will delete the created settings at the end of its execution.</span></span> |
| \<ParallelProcessing\> | \<Threshold\>                        | <span data-ttu-id="de205-290">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-290">1..1</span></span>                | \-                | <span data-ttu-id="de205-291">並列処理のルールのしきい値を指定します。</span><span class="sxs-lookup"><span data-stu-id="de205-291">This specifies the threshold for the parallel processing rule.</span></span> |
|                        | \<TaskCount\>                        | <span data-ttu-id="de205-292">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-292">1..1</span></span>                | \-                | <span data-ttu-id="de205-293">これは、並列処理に使用される並列タスクの数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-293">This is used to specify the number of parallel tasks to be used for parallel processing.</span></span> |
| \<Entity\>             | \<MappingDetail\>                    | <span data-ttu-id="de205-294">0..n</span><span class="sxs-lookup"><span data-stu-id="de205-294">0..n</span></span>                | \-                | <span data-ttu-id="de205-295">*自動生成*、*自動既定値* およびエンティティのマッピングで他の設定を構成できます。</span><span class="sxs-lookup"><span data-stu-id="de205-295">Allows to configure the *auto generate*, *auto default* and other settings on the mapping for an entity.</span></span> |
|                        | \<MappingDetail\>                    | \-                  | <span data-ttu-id="de205-296">StagingFieldName</span><span class="sxs-lookup"><span data-stu-id="de205-296">StagingFieldName</span></span>  | <span data-ttu-id="de205-297">この属性は、設定を指定するエンティティ列を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-297">This attribute is used to identify the entity column for which the settings are to be specified.</span></span> |
|                        | \<MappingDetail\>                    | \-                  | <span data-ttu-id="de205-298">AutoGenerate</span><span class="sxs-lookup"><span data-stu-id="de205-298">AutoGenerate</span></span>      | <span data-ttu-id="de205-299">これは、自動生成オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-299">This is a Boolean field with possible values of Yes or No for enabling/disabling auto generate option.</span></span> |
|                        | \<MappingDetail\>                    | \-                  | <span data-ttu-id="de205-300">AutoDefault</span><span class="sxs-lookup"><span data-stu-id="de205-300">AutoDefault</span></span>       | <span data-ttu-id="de205-301">これは、自動既定オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-301">This is a Boolean field with possible values of Yes or No for enabling/disabling auto default option.</span></span> |
|                        | \<MappingDetail\>                    | \-                  | <span data-ttu-id="de205-302">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="de205-302">DefaultValue</span></span>      | <span data-ttu-id="de205-303">これは、自動既定設定が有効な場合に使用される既定値です。</span><span class="sxs-lookup"><span data-stu-id="de205-303">This is the default value to be used if auto defaulting is enabled.</span></span> |
|                        | \<MappingDetail\>                    | \-                  | <span data-ttu-id="de205-304">IgnoreBlankValues</span><span class="sxs-lookup"><span data-stu-id="de205-304">IgnoreBlankValues</span></span> | <span data-ttu-id="de205-305">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-305">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |
|                        | \<MappingDetail\>                    | \-                  | <span data-ttu-id="de205-306">TextQualifier</span><span class="sxs-lookup"><span data-stu-id="de205-306">TextQualifier</span></span>     | <span data-ttu-id="de205-307">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-307">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |
|                        | \<MappingDetail\>                    | \-                  | <span data-ttu-id="de205-308">UseEnumLabel</span><span class="sxs-lookup"><span data-stu-id="de205-308">UseEnumLabel</span></span>      | <span data-ttu-id="de205-309">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="de205-309">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |

### <a name="test-groups"></a><span data-ttu-id="de205-310">テスト グループ</span><span class="sxs-lookup"><span data-stu-id="de205-310">Test groups</span></span>
<span data-ttu-id="de205-311">テスト グループは、マニフェストの関連するタスクを整理するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="de205-311">Test groups can be used to organize related tasks in a manifest.</span></span> <span data-ttu-id="de205-312">マニフェストには複数のテスト グループがあります。</span><span class="sxs-lookup"><span data-stu-id="de205-312">There can be more than one test group in a manifest.</span></span>

```xml
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

| <span data-ttu-id="de205-313">親要素</span><span class="sxs-lookup"><span data-stu-id="de205-313">Parent element</span></span>   | <span data-ttu-id="de205-314">要素</span><span class="sxs-lookup"><span data-stu-id="de205-314">Element</span></span>           | <span data-ttu-id="de205-315">要素の基数</span><span class="sxs-lookup"><span data-stu-id="de205-315">Element Cardinality</span></span> | <span data-ttu-id="de205-316">属性</span><span class="sxs-lookup"><span data-stu-id="de205-316">Attributes</span></span>  | <span data-ttu-id="de205-317">説明</span><span class="sxs-lookup"><span data-stu-id="de205-317">Description</span></span> |
|------------------|-------------------|---------------------|-------------|-------------|
| \<TestManifest\> | \<TestGroup\>     | <span data-ttu-id="de205-318">1..n</span><span class="sxs-lookup"><span data-stu-id="de205-318">1..n</span></span>                | \-          | \- |
|                  | \<TestGroup\>     | <span data-ttu-id="de205-319">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-319">1..1</span></span>                | <span data-ttu-id="de205-320">氏名</span><span class="sxs-lookup"><span data-stu-id="de205-320">Name</span></span>        | <span data-ttu-id="de205-321">これは、グループの機能上の理由を特定するための名前です。</span><span class="sxs-lookup"><span data-stu-id="de205-321">This is the name for the group to identify its functional reason.</span></span> |
| \<TestGroup\>    | \<TestCase\>      | <span data-ttu-id="de205-322">1..n</span><span class="sxs-lookup"><span data-stu-id="de205-322">1..n</span></span>                | \-          | <span data-ttu-id="de205-323">タスクは、この要素で定義されます。</span><span class="sxs-lookup"><span data-stu-id="de205-323">The task is defined in this element.</span></span> <span data-ttu-id="de205-324">タスクでは、タスク パラメータおよびタスク動作を継承する共有設定を参照できます。</span><span class="sxs-lookup"><span data-stu-id="de205-324">The task can refer to the shared set up to inherit task parameters and task behavior.</span></span> <span data-ttu-id="de205-325">タスクでは、パラメータと動作もそのレベルで上書きできるため、マニフェストの管理を単純にできます。</span><span class="sxs-lookup"><span data-stu-id="de205-325">The task can also override parameters and behavior at its level thus making the management of the manifest simple.</span></span> |
|                  | \<TestCase\>      | \-                  | <span data-ttu-id="de205-326">肩書き</span><span class="sxs-lookup"><span data-stu-id="de205-326">Title</span></span>       | <span data-ttu-id="de205-327">これはタスクのタイトルです。</span><span class="sxs-lookup"><span data-stu-id="de205-327">This is the title for the task.</span></span> |
|                  | \<TestCase\>      | \-                  | <span data-ttu-id="de205-328">ID</span><span class="sxs-lookup"><span data-stu-id="de205-328">ID</span></span>          | <span data-ttu-id="de205-329">これはタスクの ID です。</span><span class="sxs-lookup"><span data-stu-id="de205-329">This is the ID for the task.</span></span> <span data-ttu-id="de205-330">これは英数字で、最大文字数制限は 10 です。</span><span class="sxs-lookup"><span data-stu-id="de205-330">This can be alphanumeric with a max character limit of 10.</span></span> |
|                  | \<TestCase\>      | \-                  | <span data-ttu-id="de205-331">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="de205-331">RepeatCount</span></span> | <span data-ttu-id="de205-332">これは、将来の機能のプレース ホルダーです。</span><span class="sxs-lookup"><span data-stu-id="de205-332">This is a placeholder for a future functionality.</span></span> <span data-ttu-id="de205-333">ただし、これは値 *1* で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-333">However, this must be specified with a value of *1*.</span></span> |
|                  | \<TestCase\>      | \-                  | <span data-ttu-id="de205-334">TraceParser</span><span class="sxs-lookup"><span data-stu-id="de205-334">TraceParser</span></span> | <span data-ttu-id="de205-335">これは、将来の機能のプレース ホルダーです。</span><span class="sxs-lookup"><span data-stu-id="de205-335">This is a placeholder for a future functionality.</span></span> <span data-ttu-id="de205-336">ただし、これは値 *オフ* で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-336">However, this must be specified with a value *off*.</span></span> |
|                  | \<TestCase\>      | \-                  | <span data-ttu-id="de205-337">タイムアウト</span><span class="sxs-lookup"><span data-stu-id="de205-337">Timeout</span></span>     | <span data-ttu-id="de205-338">これは、タスク自動化マネージャーによってタスクがモニターされる最大期間です。</span><span class="sxs-lookup"><span data-stu-id="de205-338">This is the maximum duration a task will be monitored by the task automation manager.</span></span> <span data-ttu-id="de205-339">指定したタイムアウトを超えてタスクがまだアクティブな場合、マネージャーはマニフェスト内の次のタスクに進みます。</span><span class="sxs-lookup"><span data-stu-id="de205-339">If the task is still active beyond the timeout specified, the manager will proceed to the next task in the manifest.</span></span> |
| \<TestCase\>     | \<DataFile\>      | <span data-ttu-id="de205-340">1..n</span><span class="sxs-lookup"><span data-stu-id="de205-340">1..n</span></span>                | \-          | <span data-ttu-id="de205-341">この要素は、タスクで使用されるファイル、またはデータのプロジェクトを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-341">This element is used to define the file or data package to be used by the task.</span></span> <span data-ttu-id="de205-342">これは、既に宣言されたファイル、またはマニフェストの共有セクションのデータ パッケージを参照できます。</span><span class="sxs-lookup"><span data-stu-id="de205-342">This can reference to an already declared file or a data package in the shared section of the manifest.</span></span> <span data-ttu-id="de205-343">タスクでは、反復バッチ インポート シナリオでのみ指定された複数のデータ ファイルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="de205-343">A task can have more than one data file specified for recurring batch import scenarios only.</span></span> <span data-ttu-id="de205-344">他のシナリオでは、1 つ以上のファイルが指定されていても、最初のファイルがタスクによって使用されるファイルです。</span><span class="sxs-lookup"><span data-stu-id="de205-344">For other scenarios, even if more than one files are specified, the first file is what will be used by the task.</span></span> |
|                  | \<JobDefinition\> | <span data-ttu-id="de205-345">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-345">1..1</span></span>                | \-          | <span data-ttu-id="de205-346">この要素は、タスクで使用されるデータのプロジェクトを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-346">This element is used to define the data project to be used by the task.</span></span> <span data-ttu-id="de205-347">これは、共有セクション内のすでに宣言されているマニフェストのジョブ定義を参照できます。</span><span class="sxs-lookup"><span data-stu-id="de205-347">This can reference to an already declared job definition in the shared section of the manifest.</span></span> <span data-ttu-id="de205-348">タスクでは、共有設定で定義されている値よりも新しい値にジョブ定義の要素を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="de205-348">The task can override elements of job definition to a new value than what is defined in the shared set up.</span></span> |
|                  | \<EntitySetup\>   | <span data-ttu-id="de205-349">1..1</span><span class="sxs-lookup"><span data-stu-id="de205-349">1..1</span></span>                | \-          | <span data-ttu-id="de205-350">この要素は、タスクで使用されるエンティティのエンティティ セットアップを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-350">This element is used to define the entity set up for entities used by the task.</span></span> <span data-ttu-id="de205-351">これは、マニフェストの共有のセクションで既に宣言されたエンティティ セットアップを参照できます。</span><span class="sxs-lookup"><span data-stu-id="de205-351">This can reference to an already declared entity set up in the shared section of the manifest.</span></span> <span data-ttu-id="de205-352">タスクでは、共有設定で定義されている値よりも新しい値にエンティティ設定の要素を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="de205-352">The task can override elements of entity setup to a new value than what is defined in the shared set up.</span></span> |

## <a name="best-practices-for-manifest-design"></a><span data-ttu-id="de205-353">マニフェスト デザインのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="de205-353">Best practices for manifest design</span></span>
<span data-ttu-id="de205-354">さまざまな方法でマニフェストを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="de205-354">You can define a manifest in many ways.</span></span> <span data-ttu-id="de205-355">マニフェストをデザインするときに考慮する必要があるいくつかのポインターを次に示します。</span><span class="sxs-lookup"><span data-stu-id="de205-355">Here are a few pointers that you should consider when you design a manifest.</span></span>

### <a name="granularity"></a><span data-ttu-id="de205-356">粒度</span><span class="sxs-lookup"><span data-stu-id="de205-356">Granularity</span></span>
<span data-ttu-id="de205-357">機能的な意思決定としてマニフェストの粒度を判断することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="de205-357">We recommend that you determine the granularity of your manifest as a functional decision.</span></span> <span data-ttu-id="de205-358">チームは、複数のマニフェストを管理するか、または単一のマニフェストの変更を管理するかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-358">Your team must decide whether it wants to manage many manifests or manage changes in a single manifest.</span></span>

- <span data-ttu-id="de205-359">チームが論理的に必要と考える数のマニフェストを使って開始します。</span><span class="sxs-lookup"><span data-stu-id="de205-359">Start with as many manifests as your team thinks you logically need.</span></span> <span data-ttu-id="de205-360">後で、チームが実際にマニフェストの実行を開始すると、予想より少ないマニフェストを使用しており、それらを結合したいと考える場合があります。</span><span class="sxs-lookup"><span data-stu-id="de205-360">Later, when the team actually starts to run the manifests, it might find that it uses fewer manifests than it expected, and it might want to merge them.</span></span> <span data-ttu-id="de205-361">この場合、マニフェストをマージすることができます。</span><span class="sxs-lookup"><span data-stu-id="de205-361">In this case, you can merge manifests.</span></span>
- <span data-ttu-id="de205-362">職務の分離を検討する。</span><span class="sxs-lookup"><span data-stu-id="de205-362">Consider separation of duties.</span></span> <span data-ttu-id="de205-363">たとえば、デモ データの設定に対して 1 つのマニフェスト、環境の高品質の構成の設定に対して別のマニフェストがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="de205-363">For example, you might have one manifest for the setup of demo data and another manifest for the setup of the golden configuration for your environment.</span></span> <span data-ttu-id="de205-364">この方法で、チーム メンバーが使用する予定のマニフェストのみを使用することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="de205-364">In this way, you can make sure that team members use only the manifests that they are supposed to use.</span></span>
- <span data-ttu-id="de205-365">LCS へのユーザー アクセスについて考慮してください。</span><span class="sxs-lookup"><span data-stu-id="de205-365">Consider user access to LCS.</span></span> <span data-ttu-id="de205-366">たとえば、大きなおよびグローバルに配分された実装チームは、アプリケーションの複数のインスタンスまたは複数の LCS プロジェクトを持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="de205-366">For example, larger and globally distributed implementation teams might have multiple instances of the application or multiple LCS projects.</span></span>

### <a name="inheritance"></a><span data-ttu-id="de205-367">継承</span><span class="sxs-lookup"><span data-stu-id="de205-367">Inheritance</span></span>
<span data-ttu-id="de205-368">マニフェスト スキーマは、マニフェスト内のすべてのタスクに適用される共通要素の継承をサポートします。</span><span class="sxs-lookup"><span data-stu-id="de205-368">The manifest schema supports inheritance of common elements that will apply to all tasks in the manifest.</span></span> <span data-ttu-id="de205-369">タスクは、共通の要素を上書きして一意の動作を定義できます。</span><span class="sxs-lookup"><span data-stu-id="de205-369">A task can override a common element to define a unique behavior.</span></span> <span data-ttu-id="de205-370">**共通設定** セクションの目的は、構成要素の繰り返しを最小限に抑えて、可能な限り要素を再利用することです。</span><span class="sxs-lookup"><span data-stu-id="de205-370">The purpose of the **Shared setup** section is to minimize repetition of configuration elements, so that elements are reused as much as possible.</span></span> <span data-ttu-id="de205-371">目標は、メンテナンスと可読性を向上させるために、マニフェストを簡潔かつ清潔に保つことです。</span><span class="sxs-lookup"><span data-stu-id="de205-371">The goal is to keep the manifest concise and clean, to improve maintenance and readability.</span></span>

### <a name="source-control"></a><span data-ttu-id="de205-372">ソース管理</span><span class="sxs-lookup"><span data-stu-id="de205-372">Source control</span></span>
<span data-ttu-id="de205-373">実装チームのすべてのメンバーが使用する必要があるマニフェストは、アプリケーション オブジェクト ツリー (AOT) 内のソース コントロールに格納されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-373">Manifests that must be used by all the members of an implementation team should be stored in source control in the Application Object Tree (AOT).</span></span> <span data-ttu-id="de205-374">この方法は、ソース管理の利点を提供するだけでなく、プロセスがすべてのユーザーに一貫した方法で配布またはマニフェストを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="de205-374">This approach not only provides the benefits of source control, but also enables a process to distribute or make manifests available to all users in a consistent manner.</span></span> <span data-ttu-id="de205-375">また、この方法では、マニフェストを構成に使用する場合、データ管理に関連するデータ プロジェクトの構成管理も可能です。</span><span class="sxs-lookup"><span data-stu-id="de205-375">This approach also enables configuration management for data projects that are related to data management, if manifests are used for configuration.</span></span>

### <a name="number-of-job-definitions-and-entity-definitions"></a><span data-ttu-id="de205-376">ジョブ定義とエンティティ定義の数</span><span class="sxs-lookup"><span data-stu-id="de205-376">Number of job definitions and entity definitions</span></span>
<span data-ttu-id="de205-377">使用ケースのほとんどの場合、マニフェストで 1 つのジョブ定義で十分であるのは、継承がタスク レベルでの動作を変更するために使用できるからです。</span><span class="sxs-lookup"><span data-stu-id="de205-377">For most of the use cases, one job definition in a manifest should be enough, because inheritance can be used to change the behavior at the task level.</span></span> <span data-ttu-id="de205-378">この原則は、エンティティの定義にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="de205-378">This principle also applies to entity definitions.</span></span>

## <a name="validations"></a><span data-ttu-id="de205-379">検証</span><span class="sxs-lookup"><span data-stu-id="de205-379">Validations</span></span>
<span data-ttu-id="de205-380">データ タスク自動化マネージャは、タスクの設定に基づいて検証を実行します。</span><span class="sxs-lookup"><span data-stu-id="de205-380">Data task automation manager performs validations, based on the setup of a task.</span></span> <span data-ttu-id="de205-381">タスクが失敗した場合は、タスクの完了後に、検証を表示することによって、エラーの原因をすばやく確認できます。</span><span class="sxs-lookup"><span data-stu-id="de205-381">If a task fails, you can quickly determine the reason for the failure by viewing the validations after the task is completed.</span></span> <span data-ttu-id="de205-382">データ タスク自動化マネージャーが提供する情報のレベルは、初期検出を容易にするために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="de205-382">The level of information that Data task automation manager provides is optimized to facilitate initial discovery.</span></span> <span data-ttu-id="de205-383">詳細な調査のためには、対応するデータ プロジェクトおよびその実行の詳細を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de205-383">For detailed investigation, you must look at the corresponding data project and its execution details.</span></span>

<span data-ttu-id="de205-384">現在、次のデータ検証がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="de205-384">The following data validations are currently supported:</span></span>

- <span data-ttu-id="de205-385">**ジョブ ステータス** – この検証は、ジョブが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="de205-385">**Job status** – This validation checks whether the job was successful.</span></span>
- <span data-ttu-id="de205-386">**バッチ ステータス** - この検証は、バッチが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="de205-386">**Batch status** – This validation checks whether the batch was successful.</span></span>
- <span data-ttu-id="de205-387">**メッセージ状態** – テストが統合に関するものである場合、メッセージの状態が検証されます。</span><span class="sxs-lookup"><span data-stu-id="de205-387">**Message status** – If the test is about integrations, the message status is validated.</span></span>
- <span data-ttu-id="de205-388">**切り捨て** – 切り捨てが有効になっている場合は、この検証が切り捨てが発生したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="de205-388">**Truncation** – If truncation is enabled, this validation checks whether truncation occurred.</span></span>
- <span data-ttu-id="de205-389">**ステージングのスキップ** – **ステージングのスキップ** がテストで有効になっている場合、ステージングがスキップされたかどうかをこの検証でチェックします。</span><span class="sxs-lookup"><span data-stu-id="de205-389">**Skip staging** – If **Skip staging** is enabled on a test, this validation checks whether staging was skipped.</span></span>

## <a name="example-1-configuration-management-for-data-projects"></a><span data-ttu-id="de205-390">例 1: データ プロジェクトの構成管理</span><span class="sxs-lookup"><span data-stu-id="de205-390">Example 1: Configuration management for data projects</span></span>
<span data-ttu-id="de205-391">**\<ConfigurationOnly\>** 要素はデータ プロジェクトに構成タスクを作成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="de205-391">The **\<ConfigurationOnly\>** element can be used to create configuration tasks for data projects.</span></span> <span data-ttu-id="de205-392">ConfigurationOnly が はい に設定されている場合は、データプロジェクトが作成されるのみで実行はされません。</span><span class="sxs-lookup"><span data-stu-id="de205-392">When ConfigurationOnly is set to Yes, the data projects are only created but not executed.</span></span> <span data-ttu-id="de205-393">これにより、環境に渡るデータプロジェクトの管理を自動でおこなうことができます。</span><span class="sxs-lookup"><span data-stu-id="de205-393">This allows for managing data projects across environments in an automated manner.</span></span>

```xml
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

## <a name="example-2-automated-setup-of-demo-data"></a><span data-ttu-id="de205-394">例 2: デモ データの自動設定</span><span class="sxs-lookup"><span data-stu-id="de205-394">Example 2: Automated setup of demo data</span></span>
<span data-ttu-id="de205-395">次のマニフェストは、デモ データ パッケージが共有アセット ライブラリに格納されている場合の 3 つの法人のデモ データの設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="de205-395">The following manifest shows the setup of demo data for three legal entities when the demo data packages are stored in the Shared asset library.</span></span> <span data-ttu-id="de205-396">以前の例とこの例との違いは、データプロジェクトを実際に実行して、デモデータを設定することです。</span><span class="sxs-lookup"><span data-stu-id="de205-396">The difference in this example from the previous example is the actual execution of the data projects to set up the demo data.</span></span> <span data-ttu-id="de205-397">これは、ConfigurationOnly オプションを使用しない、またはマニフェストの一貫性に対してこれを使うことに対して、いいえと設定することで達成されます。</span><span class="sxs-lookup"><span data-stu-id="de205-397">This is accomplished by not using the ConfigurationOnly option or setting it to No to use it for consistency of the manifest.</span></span>

```xml
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
