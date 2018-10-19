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
ms.sourcegitcommit: 033c9bdfce0840e1af1c63708905aec6829bbe90
ms.openlocfilehash: 24c4b554ef06af25ab35df103ec805b4302b5799
ms.contentlocale: ja-jp
ms.lasthandoff: 09/13/2018

---

# <a name="data-task-automation"></a><span data-ttu-id="c9023-103">データ タスクの自動化</span><span class="sxs-lookup"><span data-stu-id="c9023-103">Data task automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c9023-104">Microsoft Dynamics 365 for Finance and Operations のデータ タスク自動化は、各種のデータ タスクを簡単に繰り返し、各タスクの結果を検証を可能にします。</span><span class="sxs-lookup"><span data-stu-id="c9023-104">Data task automation in Microsoft Dynamics 365 for Finance and Operations lets you easily repeat many types of data tasks and validate the outcome of each task.</span></span> <span data-ttu-id="c9023-105">データ タスクの自動化は、実装フェーズにあるプロジェクトで非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="c9023-105">Data task automation is very useful for projects that are in the implementation phase.</span></span> <span data-ttu-id="c9023-106">たとえば、データ プロジェクトの作成およびコンフィギュレーションを自動化することができます。</span><span class="sxs-lookup"><span data-stu-id="c9023-106">For example, you can automate the creation and configuration of data projects.</span></span> <span data-ttu-id="c9023-107">また、デモ データおよび高品質の構成データ、およびデータ移行に関連する他のタスクなどの、インポート/エクスポート オペレーションの実行を構成およびトリガーすることができます。</span><span class="sxs-lookup"><span data-stu-id="c9023-107">You can also configure and trigger the execution of import/export operations, such as the setup of demo data and golden configuration data, and other tasks that are related to data migration.</span></span> <span data-ttu-id="c9023-108">また、タスクの結果の検証を使用して、データ エンティティの自動テストを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="c9023-108">You can also create automated testing of data entities by using task outcome validation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9023-109">現時点では、オンプレミス環境ではデータ タスクの自動化はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c9023-109">Data task automation isn't currently supported for on-premises environments.</span></span>

<span data-ttu-id="c9023-110">データ タスクの自動化のために次の方法をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c9023-110">We recommend the following approach for data task automation.</span></span>

1. <span data-ttu-id="c9023-111">自動化の恩恵を受けるデータ関連のタスクを特定する。</span><span class="sxs-lookup"><span data-stu-id="c9023-111">Identify the data-related tasks that will benefit from automation.</span></span>

    <span data-ttu-id="c9023-112">実装チームは自分たちの構成管理計画とデータ移行計画をレビューして、自動化のための潜在的なデータ タスクを識別すること、またデータ エンティティのテスト ケースも識別することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c9023-112">We recommend that implementation teams review their configuration management plan and data migration plan to identify potential data tasks for automation, and also to identify data entity test cases.</span></span>

2. <span data-ttu-id="c9023-113">タスクを定義します。</span><span class="sxs-lookup"><span data-stu-id="c9023-113">Define tasks.</span></span>

    <span data-ttu-id="c9023-114">タスクは、XML マニフェストで定義されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-114">Tasks are defined in an XML manifest.</span></span> <span data-ttu-id="c9023-115">アプリケーション ライフ サイクルの管理 (ALM) 戦略では、構成管理の一部としてソース管理下のマニフェストを保持することができます。</span><span class="sxs-lookup"><span data-stu-id="c9023-115">You can keep your manifest under source control as part of configuration management in your application lifecycle management (ALM) strategy.</span></span>

3. <span data-ttu-id="c9023-116">Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリでのデータ タスクの自動化に関連するデータ パッケージを配置します。</span><span class="sxs-lookup"><span data-stu-id="c9023-116">Put the data packages that are related to data task automation in the Shared asset library of Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="c9023-117">また、必要に応じて特定の LCS プロジェクトを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="c9023-117">You can also use a specific LCS project as you require.</span></span>

    <span data-ttu-id="c9023-118">データ タスク自動化マネージャは、LCS プロジェクトに関連するサンドボックスまたは実稼動環境からパッケージを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c9023-118">Data task automation manager can consume packages from any sandbox and/or production environment that is related to the LCS project.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="c9023-119">Finance and Operations のデータ タスク自動化マネージャーを実行するユーザー アカウントは、LCS およびデータ パッケージのマニフェストで参照される LCS プロジェクトにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-119">The user account that runs Data task automation manager in Finance and Operations must have access to LCS and to the LCS project that is referenced in the manifest for data packages.</span></span>
    > - <span data-ttu-id="c9023-120">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合アプリケーション プログラミング インターフェイス (API) を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="c9023-120">Although data task automation can be run in any environment in the cloud, we strongly recommend that you not run any import/export tasks that use integration application programming interfaces (APIs) in a production environment.</span></span> <span data-ttu-id="c9023-121">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-121">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

4. <span data-ttu-id="c9023-122">データ タスクを実行し、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="c9023-122">Run the data tasks, and then review the outcomes.</span></span>

    <span data-ttu-id="c9023-123">データ タスク自動化マネージャは、各タスクの成功または失敗の結果を提供します。</span><span class="sxs-lookup"><span data-stu-id="c9023-123">Data task automation manager provides the success or failure outcome for each task.</span></span> <span data-ttu-id="c9023-124">また、タスクが失敗した理由に関する見解も提供します。</span><span class="sxs-lookup"><span data-stu-id="c9023-124">It also provides insights into the reason why a task failed.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c9023-125">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合 API を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="c9023-125">Although data task automation can be run in any environments in the cloud, we recommend that you not run any import/export tasks that use integration APIs in a production environment.</span></span> <span data-ttu-id="c9023-126">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-126">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

<span data-ttu-id="c9023-127">次のビデオは、Data Task Automation Manager の初期リリースを紹介する TechTalk の 55 分です。[タスク自動化フレームワーク](https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4)。</span><span class="sxs-lookup"><span data-stu-id="c9023-127">The following video is a 55-minute TechTalk that walks you through an early release of Data task automation manager: [Task automation framework](https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4).</span></span>

## <a name="task-manifest"></a><span data-ttu-id="c9023-128">タスク マニフェスト</span><span class="sxs-lookup"><span data-stu-id="c9023-128">Task manifest</span></span>
<span data-ttu-id="c9023-129">タスクは、XML マニフェストで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-129">A task must be defined in an XML manifest.</span></span> <span data-ttu-id="c9023-130">このセクションでは、マニフェストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c9023-130">This section describes the manifest.</span></span> <span data-ttu-id="c9023-131">マニフェストを名前付けしデザインする方法の指針については、このトピックの後半の、「マニフェストのデザインに対するベスト プラクティス」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9023-131">For guidance about how to name and design the manifest, see the "Best practices for manifest design" section later in this topic.</span></span>

### <a name="manifest-root"></a><span data-ttu-id="c9023-132">マニフェスト ルート</span><span class="sxs-lookup"><span data-stu-id="c9023-132">Manifest root</span></span>
<span data-ttu-id="c9023-133">**\<TestManifest\>** 要素は、マニフェストのルートです。</span><span class="sxs-lookup"><span data-stu-id="c9023-133">The **\<TestManifest\>** element is the root of the manifest.</span></span> <span data-ttu-id="c9023-134">その他のすべての要素はこの要素の子です。</span><span class="sxs-lookup"><span data-stu-id="c9023-134">All other elements are children of this element.</span></span>

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

| <span data-ttu-id="c9023-135">要素</span><span class="sxs-lookup"><span data-stu-id="c9023-135">Element</span></span>          | <span data-ttu-id="c9023-136">要素の基数</span><span class="sxs-lookup"><span data-stu-id="c9023-136">Element Cardinality</span></span> | <span data-ttu-id="c9023-137">属性</span><span class="sxs-lookup"><span data-stu-id="c9023-137">Attributes</span></span> | <span data-ttu-id="c9023-138">属性の説明</span><span class="sxs-lookup"><span data-stu-id="c9023-138">Attribute description</span></span>                                     |
|------------------|---------------------|------------|-----------------------------------------------------------|
| <span data-ttu-id="c9023-139">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="c9023-139">\<TestManifest\></span></span> | <span data-ttu-id="c9023-140">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-140">1..1</span></span>                | <span data-ttu-id="c9023-141">名前</span><span class="sxs-lookup"><span data-stu-id="c9023-141">name</span></span>       | <span data-ttu-id="c9023-142">*名前*はマニフェストの目的を識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c9023-142">The *name* helps to identify the purpose of the manifest.</span></span> |

### <a name="shared-setup"></a><span data-ttu-id="c9023-143">共有された設定</span><span class="sxs-lookup"><span data-stu-id="c9023-143">Shared setup</span></span>
<span data-ttu-id="c9023-144">**共有セットアップ** セクションは、全般的なタスクのパラメーターとマニフェスト内のすべてのタスクの動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="c9023-144">The **Shared setup** section defines general task parameters and behaviors for all tasks in the manifest.</span></span>

| <span data-ttu-id="c9023-145">親要素</span><span class="sxs-lookup"><span data-stu-id="c9023-145">Parent element</span></span>   | <span data-ttu-id="c9023-146">要素</span><span class="sxs-lookup"><span data-stu-id="c9023-146">Element</span></span>         | <span data-ttu-id="c9023-147">要素の基数</span><span class="sxs-lookup"><span data-stu-id="c9023-147">Element Cardinality</span></span> | <span data-ttu-id="c9023-148">属性</span><span class="sxs-lookup"><span data-stu-id="c9023-148">Attributes</span></span> | <span data-ttu-id="c9023-149">属性の説明</span><span class="sxs-lookup"><span data-stu-id="c9023-149">Attribute description</span></span>            |
|------------------|-----------------|---------------------|------------|----------------------------------|
| <span data-ttu-id="c9023-150">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="c9023-150">\<TestManifest\></span></span> | <span data-ttu-id="c9023-151">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="c9023-151">\<SharedSetup\></span></span> | <span data-ttu-id="c9023-152">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-152">1..1</span></span>                | \-         | <span data-ttu-id="c9023-153">この要素には属性はありません</span><span class="sxs-lookup"><span data-stu-id="c9023-153">This element takes no attributes</span></span> |

### <a name="data-files"></a><span data-ttu-id="c9023-154">データ ファイル</span><span class="sxs-lookup"><span data-stu-id="c9023-154">Data files</span></span>
<span data-ttu-id="c9023-155">**\<DataFile\>** 要素は、マニフェスト内のタスクが使用するデータ パッケージとデータ ファイルを定義します。</span><span class="sxs-lookup"><span data-stu-id="c9023-155">**\<DataFile\>** elements define the data packages and data files that the tasks in the manifest will use.</span></span> <span data-ttu-id="c9023-156">データ ファイルは、LCS プロジェクトの LCS アセット ライブラリまたは共有アセット ライブラリのいずれかになければなりません。</span><span class="sxs-lookup"><span data-stu-id="c9023-156">The data files must be either in the LCS asset library of your LCS project or in the Shared asset library.</span></span>

```
<DataFile ID='SharedSetup' name='Demo data-7.3-100-System and Shared'  assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsHQUS' name='Demo data-7.3-200-Financials-HQUS' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPICH' name='Demo data-7.3-200-Financials-PICH' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPIFB' name='Demo data-7.3-200-Financials-PIFB' assetType='Data package' lcsProjectId=''/>
```

| <span data-ttu-id="c9023-157">親要素</span><span class="sxs-lookup"><span data-stu-id="c9023-157">Parent element</span></span>  | <span data-ttu-id="c9023-158">要素</span><span class="sxs-lookup"><span data-stu-id="c9023-158">Element</span></span>      | <span data-ttu-id="c9023-159">要素の基数</span><span class="sxs-lookup"><span data-stu-id="c9023-159">Element Cardinality</span></span> | <span data-ttu-id="c9023-160">属性</span><span class="sxs-lookup"><span data-stu-id="c9023-160">Attributes</span></span>   | <span data-ttu-id="c9023-161">属性の説明</span><span class="sxs-lookup"><span data-stu-id="c9023-161">Attribute description</span></span> |
|-----------------|--------------|---------------------|--------------|-----------------------|
| <span data-ttu-id="c9023-162">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="c9023-162">\<SharedSetup\></span></span> | <span data-ttu-id="c9023-163">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="c9023-163">\<DataFile\></span></span> | <span data-ttu-id="c9023-164">1..n</span><span class="sxs-lookup"><span data-stu-id="c9023-164">1..n</span></span>                | \-           | \- |
|                 | <span data-ttu-id="c9023-165">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="c9023-165">\<DataFile\></span></span> | \-                  | <span data-ttu-id="c9023-166">ID</span><span class="sxs-lookup"><span data-stu-id="c9023-166">ID</span></span>           | |
|                 | <span data-ttu-id="c9023-167">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="c9023-167">\<DataFile\></span></span> | \-                  | <span data-ttu-id="c9023-168">名前</span><span class="sxs-lookup"><span data-stu-id="c9023-168">name</span></span>         | <span data-ttu-id="c9023-169">データ ファイルを表す資産の名前</span><span class="sxs-lookup"><span data-stu-id="c9023-169">Name of the asset that represents the data file</span></span> |
|                 | <span data-ttu-id="c9023-170">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="c9023-170">\<DataFile\></span></span> | \-                  | <span data-ttu-id="c9023-171">assetType</span><span class="sxs-lookup"><span data-stu-id="c9023-171">assetType</span></span>    | <span data-ttu-id="c9023-172">データ ファイルを格納する LCS 資産ライブラリでの資産タイプ。</span><span class="sxs-lookup"><span data-stu-id="c9023-172">The asset type in LCS asset library that stores the data file.</span></span> <span data-ttu-id="c9023-173">これは、LCS アセット ライブラリで示されたように、アセット タイプの名前です。</span><span class="sxs-lookup"><span data-stu-id="c9023-173">This is the asset type name as shown in LCS asset library.</span></span> |
|                 | <span data-ttu-id="c9023-174">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="c9023-174">\<DataFile\></span></span> | \-                  | <span data-ttu-id="c9023-175">lcsProjectId</span><span class="sxs-lookup"><span data-stu-id="c9023-175">lcsProjectId</span></span> | <span data-ttu-id="c9023-176">その資産ライブラリで LCS プロジェクトにはデータ ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="c9023-176">The LCS project that has the data file in its asset library.</span></span> <span data-ttu-id="c9023-177">プロジェクト ID が " として指定されている場合は、共有アセット ライブラリを示します。</span><span class="sxs-lookup"><span data-stu-id="c9023-177">If the project ID is specified as '' then, it indicates the Shared asset library.</span></span> |

### <a name="data-project-definition"></a><span data-ttu-id="c9023-178">データ プロジェクト定義</span><span class="sxs-lookup"><span data-stu-id="c9023-178">Data project definition</span></span>
<span data-ttu-id="c9023-179">**\<JobDefinition\>** 要素は、データ プロジェクト定義を定義します。</span><span class="sxs-lookup"><span data-stu-id="c9023-179">The **\<JobDefinition\>** element defines the data project definition.</span></span> <span data-ttu-id="c9023-180">マニフェストには複数のジョブ定義があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-180">There can be more than one job definition in a manifest.</span></span>

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
</JobDefinition>
```

| <span data-ttu-id="c9023-181">親要素</span><span class="sxs-lookup"><span data-stu-id="c9023-181">Parent element</span></span>    | <span data-ttu-id="c9023-182">要素</span><span class="sxs-lookup"><span data-stu-id="c9023-182">Element</span></span>                          | <span data-ttu-id="c9023-183">要素の基数</span><span class="sxs-lookup"><span data-stu-id="c9023-183">Element cardinality</span></span> | <span data-ttu-id="c9023-184">属性</span><span class="sxs-lookup"><span data-stu-id="c9023-184">Attribute</span></span> | <span data-ttu-id="c9023-185">説明</span><span class="sxs-lookup"><span data-stu-id="c9023-185">Description</span></span> |
|-------------------|----------------------------------|---------------------|-----------|-------------|
| <span data-ttu-id="c9023-186">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="c9023-186">\<SharedSetup\></span></span>   | <span data-ttu-id="c9023-187">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="c9023-187">\<JobDefinition\></span></span>                | <span data-ttu-id="c9023-188">1..n</span><span class="sxs-lookup"><span data-stu-id="c9023-188">1..n</span></span>                | <span data-ttu-id="c9023-189">ID</span><span class="sxs-lookup"><span data-stu-id="c9023-189">ID</span></span>        | <span data-ttu-id="c9023-190">タスクでジョブ定義 ID を使用してデータ プロジェクトで使用する定義を参照できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-190">The job definition ID is used in the tasks to reference the definition to be used for the data project.</span></span> |
| <span data-ttu-id="c9023-191">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="c9023-191">\<JobDefinition\></span></span> | <span data-ttu-id="c9023-192">[\<操作\>]</span><span class="sxs-lookup"><span data-stu-id="c9023-192">\<Operation\></span></span>                    | <span data-ttu-id="c9023-193">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-193">1..1</span></span>                | \-        | <span data-ttu-id="c9023-194">実行される操作は、次の値によって指定されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-194">The operation to be performed is specified by the following values.</span></span> |
|                   | <span data-ttu-id="c9023-195">\<切り詰め\></span><span class="sxs-lookup"><span data-stu-id="c9023-195">\<Truncate\></span></span>                     | <span data-ttu-id="c9023-196">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-196">1..1</span></span>                | \-        | <span data-ttu-id="c9023-197">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-197">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="c9023-198">これは操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-198">This is applicable only when operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="c9023-199">\<モード\></span><span class="sxs-lookup"><span data-stu-id="c9023-199">\<Mode\></span></span>                         | <span data-ttu-id="c9023-200">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-200">1..1</span></span>                | \-        | <span data-ttu-id="c9023-201">モードでは、操作を実行する必要があるメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="c9023-201">The mode specifies the method using which the operation must be performed.</span></span> <span data-ttu-id="c9023-202">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c9023-202">The possible values are:</span></span> |
|                   | <span data-ttu-id="c9023-203">\<ConfigurationOnly\></span><span class="sxs-lookup"><span data-stu-id="c9023-203">\<ConfigurationOnly\></span></span>            | <span data-ttu-id="c9023-204">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-204">1..1</span></span>                | \-        | <span data-ttu-id="c9023-205">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-205">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="c9023-206">タスクがデータ プロジェクトをコンフィギュレーションするのみで、指定された操作を実行しない場合は、はいに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-206">This must be set to Yes if the task is only to configure the data project but not to perform the specified operation.</span></span> |
|                   | <span data-ttu-id="c9023-207">\<BatchFrequencyInMinutes\></span><span class="sxs-lookup"><span data-stu-id="c9023-207">\<BatchFrequencyInMinutes\></span></span>      | <span data-ttu-id="c9023-208">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-208">1..1</span></span>                | \-        | <span data-ttu-id="c9023-209">バッチがスケジュール設定される頻度を指定します。</span><span class="sxs-lookup"><span data-stu-id="c9023-209">This specifies the frequency in which the batch must be scheduled.</span></span> <span data-ttu-id="c9023-210">これはモードが*定期実行されるバッチ*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-210">This is applicable only when mode is set to *recurring batch*.</span></span> |
|                   | <span data-ttu-id="c9023-211">\<NumberOfTimesToRunBatch\></span><span class="sxs-lookup"><span data-stu-id="c9023-211">\<NumberOfTimesToRunBatch\></span></span>      | <span data-ttu-id="c9023-212">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-212">1..1</span></span>                | \-        | <span data-ttu-id="c9023-213">これは、スケジュールされているバッチを実行する回数の制限を設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-213">This is used to set a limit to how many times the scheduled batch should run.</span></span> <span data-ttu-id="c9023-214">これはモードが*定期実行されるバッチ*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-214">This is applicable only when mode is set to *recurring batch*.</span></span> |
|                   | <span data-ttu-id="c9023-215">\<UploadFrequencyInSeconds\></span><span class="sxs-lookup"><span data-stu-id="c9023-215">\<UploadFrequencyInSeconds\></span></span>     | <span data-ttu-id="c9023-216">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-216">1..1</span></span>                | \-        | <span data-ttu-id="c9023-217">これは、インポートする定期バッチ ジョブにファイルをアップロードする頻度を制御するために使用します。</span><span class="sxs-lookup"><span data-stu-id="c9023-217">This is used to control the rate at which a file is uploaded to the recurring batch job for import.</span></span> <span data-ttu-id="c9023-218">これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-218">This must be used only for automated testing of recurring integrations in non-production environments.</span></span> <span data-ttu-id="c9023-219">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-219">This is applicable only when mode is set to *recurring batch* and operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="c9023-220">\<TotalNumberOfTimesToUpload\></span><span class="sxs-lookup"><span data-stu-id="c9023-220">\<TotalNumberOfTimesToUpload\></span></span>   | <span data-ttu-id="c9023-221">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-221">1..1</span></span>                |           | <span data-ttu-id="c9023-222">これはファイルを繰り返しバッチにアップロードする総回数を制御します。</span><span class="sxs-lookup"><span data-stu-id="c9023-222">This controls the total number of times the file should be uploaded to the recurring batch.</span></span> <span data-ttu-id="c9023-223">これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-223">This must be used only for automated testing of recurring integrations in non-production environments.</span></span> <span data-ttu-id="c9023-224">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-224">This is applicable only when mode is set to *recurring batch* and operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="c9023-225">\<SupportedDataSoureType\></span><span class="sxs-lookup"><span data-stu-id="c9023-225">\<SupportedDataSoureType\></span></span>       | <span data-ttu-id="c9023-226">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-226">1..1</span></span>                |           | <span data-ttu-id="c9023-227">ファイルが定期的なバッチまたはパッケージに送信中であるかどうかを指定するために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-227">This must be used to specify if a file is being sent to the recurring batch or a package.</span></span> <span data-ttu-id="c9023-228">これはモードが「定期実行されるバッチ」に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-228">This is only applicable when mode is set to 'recurring batch'.</span></span> |
|                   | <span data-ttu-id="c9023-229">\<ProcessMessagesInOrder\></span><span class="sxs-lookup"><span data-stu-id="c9023-229">\<ProcessMessagesInOrder\></span></span>       | <span data-ttu-id="c9023-230">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-230">1..1</span></span>                |           | <span data-ttu-id="c9023-231">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-231">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="c9023-232">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-232">This is applicable only when mode is set to *recurring batch* and operation is *Import*.</span></span> |
|                   | <span data-ttu-id="c9023-233">\<PreventUploadWhenZeroRecords\></span><span class="sxs-lookup"><span data-stu-id="c9023-233">\<PreventUploadWhenZeroRecords\></span></span> | <span data-ttu-id="c9023-234">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-234">1..1</span></span>                |           | <span data-ttu-id="c9023-235">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-235">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="c9023-236">これはモードが*定期実行されるバッチ*に設定されており、操作が*エクスポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-236">This is applicable only when mode is set to *recurring batch* and operation is *Export*.</span></span> |
|                   | <span data-ttu-id="c9023-237">\<UseCompanyFromMessage\></span><span class="sxs-lookup"><span data-stu-id="c9023-237">\<UseCompanyFromMessage\></span></span>        | <span data-ttu-id="c9023-238">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-238">1..1</span></span>                |           | <span data-ttu-id="c9023-239">これははい、またはいいえに設定できるブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-239">This is a Boolean field which can be set to Yes or No.</span></span> <span data-ttu-id="c9023-240">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-240">This is applicable only when mode is set to *recurring batch* and operation is *Import*.</span></span> |
|                   | <span data-ttu-id="c9023-241">\<LegalEntity\></span><span class="sxs-lookup"><span data-stu-id="c9023-241">\<LegalEntity\></span></span>                  | <span data-ttu-id="c9023-242">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-242">1..1</span></span>                |           | <span data-ttu-id="c9023-243">これをは、インポート/エクスポート ジョブを実行する必要がある法人を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-243">This is used to specify the legal entity in which the import/export job must be executed.</span></span> |
|                   | <span data-ttu-id="c9023-244">\<ConfigurationOnly\></span><span class="sxs-lookup"><span data-stu-id="c9023-244">\<ConfigurationOnly\></span></span>            | <span data-ttu-id="c9023-245">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-245">1..1</span></span>                |           | <span data-ttu-id="c9023-246">これを使用して、データのプロジェクトおよび構成する定期的なスケジュールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-246">This is used to create data projects and recurring schedules to be configured.</span></span> <span data-ttu-id="c9023-247">インポートまたはエクスポートの操作は実行されません。</span><span class="sxs-lookup"><span data-stu-id="c9023-247">The operation of import or export will not be executed.</span></span> <span data-ttu-id="c9023-248">ただし、データ プロジェクトを正しく設定するには、操作とモードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-248">However, it is required to specify the operation and mode for the data project to be configured correctly.</span></span> <span data-ttu-id="c9023-249">これは、はいまたはいいえを取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-249">This is a Boolean field which takes Yes or No.</span></span> |

### <a name="entity-setup"></a><span data-ttu-id="c9023-250">エンティティ設定</span><span class="sxs-lookup"><span data-stu-id="c9023-250">Entity setup</span></span>
<span data-ttu-id="c9023-251">**エンティティ設定** セクションは、マニフェストのタスクが使用するエンティティの特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="c9023-251">The **Entity setup** section defines the characteristics of an entity that a task in the manifest will use.</span></span> <span data-ttu-id="c9023-252">マニフェスト内のタスクによって使用されるエンティティごとに、1 つずつ複数の定義が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-252">There can be more than one definition, one for each entity that is used by the tasks in the manifest.</span></span>

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

| <span data-ttu-id="c9023-253">親要素</span><span class="sxs-lookup"><span data-stu-id="c9023-253">Parent element</span></span>         | <span data-ttu-id="c9023-254">要素</span><span class="sxs-lookup"><span data-stu-id="c9023-254">Element</span></span>                              | <span data-ttu-id="c9023-255">要素の基数</span><span class="sxs-lookup"><span data-stu-id="c9023-255">Element cardinality</span></span> | <span data-ttu-id="c9023-256">属性</span><span class="sxs-lookup"><span data-stu-id="c9023-256">Attribute</span></span>         | <span data-ttu-id="c9023-257">説明</span><span class="sxs-lookup"><span data-stu-id="c9023-257">Description</span></span> |
|------------------------|--------------------------------------|---------------------|-------------------|-------------|
| <span data-ttu-id="c9023-258">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="c9023-258">\<SharedSetup\></span></span>        | <span data-ttu-id="c9023-259">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="c9023-259">\<EntitySetup\></span></span>                      | <span data-ttu-id="c9023-260">1..n</span><span class="sxs-lookup"><span data-stu-id="c9023-260">1..n</span></span>                | <span data-ttu-id="c9023-261">ID</span><span class="sxs-lookup"><span data-stu-id="c9023-261">ID</span></span>                | <span data-ttu-id="c9023-262">タスクが使用するエンティティ定義を参照するために使用される ID。</span><span class="sxs-lookup"><span data-stu-id="c9023-262">An identification that will be used by tasks to reference an entity definition to be used.</span></span> |
| <span data-ttu-id="c9023-263">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="c9023-263">\<EntitySetup\></span></span>        | <span data-ttu-id="c9023-264">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="c9023-264">\<Entity\></span></span>                           | <span data-ttu-id="c9023-265">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-265">1..1</span></span>                | <span data-ttu-id="c9023-266">名前</span><span class="sxs-lookup"><span data-stu-id="c9023-266">name</span></span>              | <span data-ttu-id="c9023-267">エンティティ要素は、エンティティの名前で識別されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-267">The entity element is identified by the entity's name.</span></span> <span data-ttu-id="c9023-268">ただし、簡単なマニフェスト定義を容易にするために、この要素は \* ワイルド カードとしてもサポートしています。これは、すべてのエンティティがタスクで使用されていることを意味しています。</span><span class="sxs-lookup"><span data-stu-id="c9023-268">However, to facilitate easy manifest definition, this element also supports \* as a wild card which will mean all entities being used in a task.</span></span> <span data-ttu-id="c9023-269">これは、タスク内の何百ものエンティティを持つデータ パッケージを使用する場合に非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="c9023-269">This comes in very handy when using data packages with hundreds of entities in a task.</span></span> |
| <span data-ttu-id="c9023-270">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="c9023-270">\<Entity\></span></span>             | <span data-ttu-id="c9023-271">\<SourceDataFormatName\></span><span class="sxs-lookup"><span data-stu-id="c9023-271">\<SourceDataFormatName\></span></span>             | <span data-ttu-id="c9023-272">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-272">1..1</span></span>                | \-                | <span data-ttu-id="c9023-273">これはエンティティに使用されるファイル形式です。</span><span class="sxs-lookup"><span data-stu-id="c9023-273">This is the file format to be used for the entity.</span></span> |
|                        | <span data-ttu-id="c9023-274">\<ChangeTracking\></span><span class="sxs-lookup"><span data-stu-id="c9023-274">\<ChangeTracking\></span></span>                   | <span data-ttu-id="c9023-275">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-275">1..1</span></span>                | \-                | <span data-ttu-id="c9023-276">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-276">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="c9023-277">エンティティ全体で変更追跡を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="c9023-277">It enables or disables change tracking on the entire entity.</span></span> |
|                        | <span data-ttu-id="c9023-278">\<PublishToBYOD\></span><span class="sxs-lookup"><span data-stu-id="c9023-278">\<PublishToBYOD\></span></span>                    | <span data-ttu-id="c9023-279">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-279">1..1</span></span>                | \-                | <span data-ttu-id="c9023-280">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-280">This is a Boolean field with possible values of Yes or No.</span></span> |
|                        | <span data-ttu-id="c9023-281">\<DefaultRefreshType\></span><span class="sxs-lookup"><span data-stu-id="c9023-281">\<DefaultRefreshType\></span></span>               | <span data-ttu-id="c9023-282">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-282">1..1</span></span>                | \-                | <span data-ttu-id="c9023-283">これにより、エンティティの既定の更新頻度が設定されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-283">This sets the default refresh rate on the entity.</span></span> <span data-ttu-id="c9023-284">使用可能な値は*増分プッシュのみ*または*フル プッシュ*です。</span><span class="sxs-lookup"><span data-stu-id="c9023-284">The possible values are *Incremental push only* or *Full push*.</span></span> |
|                        | <span data-ttu-id="c9023-285">\<ExcelWorkSheetName\></span><span class="sxs-lookup"><span data-stu-id="c9023-285">\<ExcelWorkSheetName\></span></span>               | <span data-ttu-id="c9023-286">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-286">1..1</span></span>                | \-                | <span data-ttu-id="c9023-287">これはエンティティに使用するワークシートを指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-287">This is used to specify the worksheet to be used for the entity.</span></span> |
|                        | <span data-ttu-id="c9023-288">\<SelectFields\></span><span class="sxs-lookup"><span data-stu-id="c9023-288">\<SelectFields\></span></span>                     | <span data-ttu-id="c9023-289">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-289">1..1</span></span>                | \-                | <span data-ttu-id="c9023-290">これは、エクスポート操作のテンプレートに含まれるフィールドを指定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-290">This can be used to specify the fields to be included in the template for an export operation.</span></span> |
|                        | <span data-ttu-id="c9023-291">\<SetBasedProcessing\></span><span class="sxs-lookup"><span data-stu-id="c9023-291">\<SetBasedProcessing\></span></span>               | <span data-ttu-id="c9023-292">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-292">1..1</span></span>                | \-                | <span data-ttu-id="c9023-293">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-293">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="c9023-294">エンティティのセット ベースのプロセスを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-294">It is used to enable or disable set based processing on an entity.</span></span> |
|                        | <span data-ttu-id="c9023-295">\<FailBatchOnErrorForExecutionUnit\></span><span class="sxs-lookup"><span data-stu-id="c9023-295">\<FailBatchOnErrorForExecutionUnit\></span></span> | <span data-ttu-id="c9023-296">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-296">1..1</span></span>                | \-                | <span data-ttu-id="c9023-297">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-297">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="c9023-298">エンティティの実行単位レベルでエラーを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-298">It is used to enable or disable failure at execution unit level on an entity.</span></span> |
|                        | <span data-ttu-id="c9023-299">\<FailBatchOnErrorForLevel\></span><span class="sxs-lookup"><span data-stu-id="c9023-299">\<FailBatchOnErrorForLevel\></span></span>         | <span data-ttu-id="c9023-300">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-300">1..1</span></span>                | \-                | <span data-ttu-id="c9023-301">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-301">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="c9023-302">エンティティの実行レベルでエラーを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-302">It is used to enable or disable failure at execution level on an entity.</span></span> |
|                        | <span data-ttu-id="c9023-303">\<DisableEntity\></span><span class="sxs-lookup"><span data-stu-id="c9023-303">\<DisableEntity\></span></span>                    | <span data-ttu-id="c9023-304">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-304">1..1</span></span>                | \-                | <span data-ttu-id="c9023-305">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-305">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="c9023-306">データ プロジェクトでエンティティを有効化または無効化するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-306">It is used to enable or disable an entity in a data project.</span></span> |
|                        | <span data-ttu-id="c9023-307">\<SkipStaging\></span><span class="sxs-lookup"><span data-stu-id="c9023-307">\<SkipStaging\></span></span>                      | <span data-ttu-id="c9023-308">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-308">1..1</span></span>                | \-                | <span data-ttu-id="c9023-309">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-309">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="c9023-310">エクスポート中にエンティティのステージング テーブルをスキップするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-310">It is used to skip staging table for an entity during exports.</span></span> |
|                        | <span data-ttu-id="c9023-311">\<ParallelProcessing\></span><span class="sxs-lookup"><span data-stu-id="c9023-311">\<ParallelProcessing\></span></span>               | <span data-ttu-id="c9023-312">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-312">1..1</span></span>                | \-                | <span data-ttu-id="c9023-313">これは、エンティティに対して設定された並列処理を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-313">This is used to define the parallel processing set up for an entity.</span></span> <span data-ttu-id="c9023-314">タスクの始まりで既に終了する場合、タスクはこれらの設定を削除し、その実行の終わりに作成された設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="c9023-314">The task will delete these settings if already exits at the beginning of the task and it will delete the created settings at the end of its execution.</span></span> |
| <span data-ttu-id="c9023-315">\<ParallelProcessing\></span><span class="sxs-lookup"><span data-stu-id="c9023-315">\<ParallelProcessing\></span></span> | <span data-ttu-id="c9023-316">\<しきい値\></span><span class="sxs-lookup"><span data-stu-id="c9023-316">\<Threshold\></span></span>                        | <span data-ttu-id="c9023-317">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-317">1..1</span></span>                | \-                | <span data-ttu-id="c9023-318">並列処理のルールのしきい値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c9023-318">This specifies the threshold for the parallel processing rule.</span></span> |
|                        | <span data-ttu-id="c9023-319">\<TaskCount\></span><span class="sxs-lookup"><span data-stu-id="c9023-319">\<TaskCount\></span></span>                        | <span data-ttu-id="c9023-320">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-320">1..1</span></span>                | \-                | <span data-ttu-id="c9023-321">これは、並列処理に使用される並列タスクの数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-321">This is used to specify the number of parallel tasks to be used for parallel processing.</span></span> |
| <span data-ttu-id="c9023-322">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="c9023-322">\<Entity\></span></span>             | <span data-ttu-id="c9023-323">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="c9023-323">\<MappingDetail\></span></span>                    | <span data-ttu-id="c9023-324">0..n</span><span class="sxs-lookup"><span data-stu-id="c9023-324">0..n</span></span>                | \-                | <span data-ttu-id="c9023-325">*自動生成*、*自動既定値*およびエンティティのマッピングで他の設定を構成できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-325">Allows to configure the *auto generate*, *auto default* and other settings on the mapping for an entity.</span></span> |
|                        | <span data-ttu-id="c9023-326">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="c9023-326">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="c9023-327">StagingFieldName</span><span class="sxs-lookup"><span data-stu-id="c9023-327">StagingFieldName</span></span>  | <span data-ttu-id="c9023-328">この属性は、設定を指定するエンティティ列を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-328">This attribute is used to identify the entity column for which the settings are to be specified.</span></span> |
|                        | <span data-ttu-id="c9023-329">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="c9023-329">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="c9023-330">AutoGenerate</span><span class="sxs-lookup"><span data-stu-id="c9023-330">AutoGenerate</span></span>      | <span data-ttu-id="c9023-331">これは、自動生成オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-331">This is a Boolean field with possible values of Yes or No for enabling/disabling auto generate option.</span></span> |
|                        | <span data-ttu-id="c9023-332">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="c9023-332">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="c9023-333">AutoDefault</span><span class="sxs-lookup"><span data-stu-id="c9023-333">AutoDefault</span></span>       | <span data-ttu-id="c9023-334">これは、自動既定オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-334">This is a Boolean field with possible values of Yes or No for enabling/disabling auto default option.</span></span> |
|                        | <span data-ttu-id="c9023-335">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="c9023-335">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="c9023-336">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c9023-336">DefaultValue</span></span>      | <span data-ttu-id="c9023-337">これは、自動既定設定が有効な場合に使用される既定値です。</span><span class="sxs-lookup"><span data-stu-id="c9023-337">This is the default value to be used if auto defaulting is enabled.</span></span> |
|                        | <span data-ttu-id="c9023-338">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="c9023-338">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="c9023-339">IgnoreBlankValues</span><span class="sxs-lookup"><span data-stu-id="c9023-339">IgnoreBlankValues</span></span> | <span data-ttu-id="c9023-340">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-340">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |
|                        | <span data-ttu-id="c9023-341">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="c9023-341">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="c9023-342">TextQualifier</span><span class="sxs-lookup"><span data-stu-id="c9023-342">TextQualifier</span></span>     | <span data-ttu-id="c9023-343">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-343">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |
|                        | <span data-ttu-id="c9023-344">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="c9023-344">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="c9023-345">UseEnumLabel</span><span class="sxs-lookup"><span data-stu-id="c9023-345">UseEnumLabel</span></span>      | <span data-ttu-id="c9023-346">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c9023-346">ThThis is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |

### <a name="test-groups"></a><span data-ttu-id="c9023-347">テスト グループ</span><span class="sxs-lookup"><span data-stu-id="c9023-347">Test groups</span></span>
<span data-ttu-id="c9023-348">テスト グループは、マニフェストの関連するタスクを整理するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-348">Test groups can be used to organize related tasks in a manifest.</span></span> <span data-ttu-id="c9023-349">マニフェストには複数のテスト グループがあります。</span><span class="sxs-lookup"><span data-stu-id="c9023-349">There can be more than one test group in a manifest.</span></span>

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

| <span data-ttu-id="c9023-350">親要素</span><span class="sxs-lookup"><span data-stu-id="c9023-350">Parent element</span></span>   | <span data-ttu-id="c9023-351">要素</span><span class="sxs-lookup"><span data-stu-id="c9023-351">Element</span></span>           | <span data-ttu-id="c9023-352">要素の基数</span><span class="sxs-lookup"><span data-stu-id="c9023-352">Element Cardinality</span></span> | <span data-ttu-id="c9023-353">属性</span><span class="sxs-lookup"><span data-stu-id="c9023-353">Attributes</span></span>  | <span data-ttu-id="c9023-354">説明</span><span class="sxs-lookup"><span data-stu-id="c9023-354">Description</span></span> |
|------------------|-------------------|---------------------|-------------|-------------|
| <span data-ttu-id="c9023-355">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="c9023-355">\<TestManifest\></span></span> | <span data-ttu-id="c9023-356">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="c9023-356">\<TestGroup\></span></span>     | <span data-ttu-id="c9023-357">1..n</span><span class="sxs-lookup"><span data-stu-id="c9023-357">1..n</span></span>                | \-          | \- |
|                  | <span data-ttu-id="c9023-358">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="c9023-358">\<TestGroup\></span></span>     | <span data-ttu-id="c9023-359">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-359">1..1</span></span>                | <span data-ttu-id="c9023-360">氏名</span><span class="sxs-lookup"><span data-stu-id="c9023-360">Name</span></span>        | <span data-ttu-id="c9023-361">これは、グループの機能上の理由を特定するための名前です。</span><span class="sxs-lookup"><span data-stu-id="c9023-361">This is the name for the group to identify its functional reason.</span></span> |
| <span data-ttu-id="c9023-362">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="c9023-362">\<TestGroup\></span></span>    | <span data-ttu-id="c9023-363">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="c9023-363">\<TestCase\></span></span>      | <span data-ttu-id="c9023-364">1..n</span><span class="sxs-lookup"><span data-stu-id="c9023-364">1..n</span></span>                | \-          | <span data-ttu-id="c9023-365">タスクは、この要素で定義されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-365">The task is defined in this element.</span></span> <span data-ttu-id="c9023-366">タスクでは、タスク パラメータおよびタスク動作を継承する共有設定を参照できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-366">The task can refer to the shared set up to inherit task parameters and task behavior.</span></span> <span data-ttu-id="c9023-367">タスクでは、パラメータと動作もそのレベルで上書きできるため、マニフェストの管理を単純にできます。</span><span class="sxs-lookup"><span data-stu-id="c9023-367">The task can also override parameters and behavior at its level thus making the management of the manifest simple.</span></span> |
|                  | <span data-ttu-id="c9023-368">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="c9023-368">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="c9023-369">肩書き</span><span class="sxs-lookup"><span data-stu-id="c9023-369">Title</span></span>       | <span data-ttu-id="c9023-370">これはタスクのタイトルです。</span><span class="sxs-lookup"><span data-stu-id="c9023-370">This is the title for the task.</span></span> |
|                  | <span data-ttu-id="c9023-371">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="c9023-371">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="c9023-372">ID</span><span class="sxs-lookup"><span data-stu-id="c9023-372">ID</span></span>          | <span data-ttu-id="c9023-373">これはタスクの ID です。</span><span class="sxs-lookup"><span data-stu-id="c9023-373">This is the ID for the task.</span></span> <span data-ttu-id="c9023-374">これは英数字で、最大文字数制限は 10 です。</span><span class="sxs-lookup"><span data-stu-id="c9023-374">This can be alphanumeric with a max character limit of 10.</span></span> |
|                  | <span data-ttu-id="c9023-375">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="c9023-375">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="c9023-376">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="c9023-376">RepeatCount</span></span> | <span data-ttu-id="c9023-377">これは、将来の機能のプレース ホルダーです。</span><span class="sxs-lookup"><span data-stu-id="c9023-377">This is a placeholder for a future functionality.</span></span> <span data-ttu-id="c9023-378">ただし、これは値 *1* で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-378">However, this must be specified with a value of *1*.</span></span> |
|                  | <span data-ttu-id="c9023-379">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="c9023-379">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="c9023-380">TraceParser</span><span class="sxs-lookup"><span data-stu-id="c9023-380">TraceParser</span></span> | <span data-ttu-id="c9023-381">これは、将来の機能のプレース ホルダーです。</span><span class="sxs-lookup"><span data-stu-id="c9023-381">This is a placeholder for a future functionality.</span></span> <span data-ttu-id="c9023-382">ただし、これは値*オフ*で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-382">However, this must be specified with a value *off*.</span></span> |
|                  | <span data-ttu-id="c9023-383">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="c9023-383">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="c9023-384">タイムアウト</span><span class="sxs-lookup"><span data-stu-id="c9023-384">Timeout</span></span>     | <span data-ttu-id="c9023-385">これは、タスク自動化マネージャーによってタスクがモニターされる最大期間です。</span><span class="sxs-lookup"><span data-stu-id="c9023-385">This is the maximum duration a task will be monitored by the task automation manager.</span></span> <span data-ttu-id="c9023-386">指定したタイムアウトを超えてタスクがまだアクティブな場合、マネージャーはマニフェスト内の次のタスクに進みます。</span><span class="sxs-lookup"><span data-stu-id="c9023-386">If the task is still active beyond the timeout specified, the manager will proceed to the next task in the manifest.</span></span> |
| <span data-ttu-id="c9023-387">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="c9023-387">\<TestCase\></span></span>     | <span data-ttu-id="c9023-388">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="c9023-388">\<DataFile\></span></span>      | <span data-ttu-id="c9023-389">1..n</span><span class="sxs-lookup"><span data-stu-id="c9023-389">1..n</span></span>                | \-          | <span data-ttu-id="c9023-390">この要素は、タスクで使用されるファイル、またはデータのプロジェクトを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-390">This element is used to define the file or data package to be used by the task.</span></span> <span data-ttu-id="c9023-391">これは、既に宣言されたファイル、またはマニフェストの共有セクションのデータ パッケージを参照できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-391">This can reference to an already declared file or a data package in the shared section of the manifest.</span></span> <span data-ttu-id="c9023-392">タスクでは、反復バッチ インポート シナリオでのみ指定された複数のデータ ファイルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c9023-392">A task can have more than one data file specified for recurring batch import scenarios only.</span></span> <span data-ttu-id="c9023-393">他のシナリオでは、1 つ以上のファイルが指定されていても、最初のファイルがタスクによって使用されるファイルです。</span><span class="sxs-lookup"><span data-stu-id="c9023-393">For other scenarios, even if more than one files are specified, the first file is what will be used by the task.</span></span> |
|                  | <span data-ttu-id="c9023-394">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="c9023-394">\<JobDefinition\></span></span> | <span data-ttu-id="c9023-395">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-395">1..1</span></span>                | \-          | <span data-ttu-id="c9023-396">この要素は、タスクで使用されるデータのプロジェクトを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-396">This element is used to define the data project to be used by the task.</span></span> <span data-ttu-id="c9023-397">これは、共有セクション内のすでに宣言されているマニフェストのジョブ定義を参照できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-397">This can reference to an already declared job definition in the shared section of the manifest.</span></span> <span data-ttu-id="c9023-398">タスクでは、共有設定で定義されている値よりも新しい値にジョブ定義の要素を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="c9023-398">The task can override elements of job definition to a new value than what is defined in the shared set up.</span></span> |
|                  | <span data-ttu-id="c9023-399">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="c9023-399">\<EntitySetup\></span></span>   | <span data-ttu-id="c9023-400">1..1</span><span class="sxs-lookup"><span data-stu-id="c9023-400">1..1</span></span>                | \-          | <span data-ttu-id="c9023-401">この要素は、タスクで使用されるエンティティのエンティティ セットアップを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-401">This element is used to define the entity set up for entities used by the task.</span></span> <span data-ttu-id="c9023-402">これは、マニフェストの共有のセクションで既に宣言されたエンティティ セットアップを参照できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-402">This can reference to an already declared entity set up in the shared section of the manifest.</span></span> <span data-ttu-id="c9023-403">タスクでは、共有設定で定義されている値よりも新しい値にエンティティ設定の要素を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="c9023-403">The task can override elements of entity setup to a new value than what is defined in the shared set up.</span></span> |

## <a name="best-practices-for-manifest-design"></a><span data-ttu-id="c9023-404">マニフェスト デザインのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="c9023-404">Best practices for manifest design</span></span>
<span data-ttu-id="c9023-405">さまざまな方法でマニフェストを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="c9023-405">You can define a manifest in many ways.</span></span> <span data-ttu-id="c9023-406">マニフェストをデザインするときに考慮する必要があるいくつかのポインターを次に示します。</span><span class="sxs-lookup"><span data-stu-id="c9023-406">Here are a few pointers that you should consider when you design a manifest.</span></span>

### <a name="granularity"></a><span data-ttu-id="c9023-407">粒度</span><span class="sxs-lookup"><span data-stu-id="c9023-407">Granularity</span></span>
<span data-ttu-id="c9023-408">機能的な意思決定としてマニフェストの粒度を判断することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c9023-408">We recommend that you determine the granularity of your manifest as a functional decision.</span></span> <span data-ttu-id="c9023-409">チームは、複数のマニフェストを管理するか、または単一のマニフェストの変更を管理するかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-409">Your team must decide whether it wants to manage many manifests or manage changes in a single manifest.</span></span>

- <span data-ttu-id="c9023-410">チームが論理的に必要と考える数のマニフェストを使って開始します。</span><span class="sxs-lookup"><span data-stu-id="c9023-410">Start with as many manifests as your team thinks you logically need.</span></span> <span data-ttu-id="c9023-411">後で、チームが実際にマニフェストの実行を開始すると、予想より少ないマニフェストを使用しており、それらを結合したいと考える場合があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-411">Later, when the team actually starts to run the manifests, it might find that it uses fewer manifests than it expected, and it might want to merge them.</span></span> <span data-ttu-id="c9023-412">この場合、マニフェストをマージすることができます。</span><span class="sxs-lookup"><span data-stu-id="c9023-412">In this case, you can merge manifests.</span></span>
- <span data-ttu-id="c9023-413">職務の分離を検討する。</span><span class="sxs-lookup"><span data-stu-id="c9023-413">Consider separation of duties.</span></span> <span data-ttu-id="c9023-414">たとえば、デモ データの設定に対して 1 つのマニフェスト、環境の高品質の構成の設定に対して別のマニフェストがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-414">For example, you might have one manifest for the setup of demo data and another manifest for the setup of the golden configuration for your environment.</span></span> <span data-ttu-id="c9023-415">この方法で、チーム メンバーが使用する予定のマニフェストのみを使用することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-415">In this way, you can make sure that team members use only the manifests that they are supposed to use.</span></span>
- <span data-ttu-id="c9023-416">LCS へのユーザー アクセスについて考慮してください。</span><span class="sxs-lookup"><span data-stu-id="c9023-416">Consider user access to LCS.</span></span> <span data-ttu-id="c9023-417">たとえば、大きなおよびグローバルに配分された実装チームは、Finance and Operations の複数のインスタンスまたは複数の LCS プロジェクトを持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-417">For example, larger and globally distributed implementation teams might have multiple instances of Finance and Operations or multiple LCS projects.</span></span>

### <a name="inheritance"></a><span data-ttu-id="c9023-418">継承</span><span class="sxs-lookup"><span data-stu-id="c9023-418">Inheritance</span></span>
<span data-ttu-id="c9023-419">マニフェスト スキーマは、マニフェスト内のすべてのタスクに適用される共通要素の継承をサポートします。</span><span class="sxs-lookup"><span data-stu-id="c9023-419">The manifest schema supports inheritance of common elements that will apply to all tasks in the manifest.</span></span> <span data-ttu-id="c9023-420">タスクは、共通の要素を上書きして一意の動作を定義できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-420">A task can override a common element to define a unique behavior.</span></span> <span data-ttu-id="c9023-421">**共通設定** セクションの目的は、構成要素の繰り返しを最小限に抑えて、可能な限り要素を再利用することです。</span><span class="sxs-lookup"><span data-stu-id="c9023-421">The purpose of the **Shared setup** section is to minimize repetition of configuration elements, so that elements are reused as much as possible.</span></span> <span data-ttu-id="c9023-422">目標は、メンテナンスと可読性を向上させるために、マニフェストを簡潔かつ清潔に保つことです。</span><span class="sxs-lookup"><span data-stu-id="c9023-422">The goal is to keep the manifest concise and clean, to improve maintenance and readability.</span></span>

### <a name="source-control"></a><span data-ttu-id="c9023-423">ソース管理</span><span class="sxs-lookup"><span data-stu-id="c9023-423">Source control</span></span>
<span data-ttu-id="c9023-424">実装チームのすべてのメンバーが使用する必要があるマニフェストは、アプリケーション オブジェクト ツリー (AOT) 内のソース コントロールに格納されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-424">Manifests that must be used by all the members of an implementation team should be stored in source control in the Application Object Tree (AOT).</span></span> <span data-ttu-id="c9023-425">この方法は、ソース管理の利点を提供するだけでなく、プロセスがすべてのユーザーに一貫した方法で配布またはマニフェストを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c9023-425">This approach not only provides the benefits of source control, but also enables a process to distribute or make manifests available to all users in a consistent manner.</span></span> <span data-ttu-id="c9023-426">また、この方法では、マニフェストを構成に使用する場合、データ管理に関連するデータ プロジェクトの構成管理も可能です。</span><span class="sxs-lookup"><span data-stu-id="c9023-426">This approach also enables configuration management for data projects that are related to data management, if manifests are used for configuration.</span></span>

### <a name="number-of-job-definitions-and-entity-definitions"></a><span data-ttu-id="c9023-427">ジョブ定義とエンティティ定義の数</span><span class="sxs-lookup"><span data-stu-id="c9023-427">Number of job definitions and entity definitions</span></span>
<span data-ttu-id="c9023-428">使用ケースのほとんどの場合、マニフェストで 1 つのジョブ定義で十分であるのは、継承がタスク レベルでの動作を変更するために使用できるからです。</span><span class="sxs-lookup"><span data-stu-id="c9023-428">For most of the use cases, one job definition in a manifest should be enough, because inheritance can be used to change the behavior at the task level.</span></span> <span data-ttu-id="c9023-429">この原則は、エンティティの定義にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-429">This principle also applies to entity definitions.</span></span>

## <a name="validations"></a><span data-ttu-id="c9023-430">検証</span><span class="sxs-lookup"><span data-stu-id="c9023-430">Validations</span></span>
<span data-ttu-id="c9023-431">データ タスク自動化マネージャは、タスクの設定に基づいて検証を実行します。</span><span class="sxs-lookup"><span data-stu-id="c9023-431">Data task automation manager performs validations, based on the setup of a task.</span></span> <span data-ttu-id="c9023-432">タスクが失敗した場合は、タスクの完了後に、検証を表示することによって、エラーの原因をすばやく確認できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-432">If a task fails, you can quickly determine the reason for the failure by viewing the validations after the task is completed.</span></span> <span data-ttu-id="c9023-433">データ タスク自動化マネージャーが提供する情報のレベルは、初期検出を容易にするために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="c9023-433">The level of information that Data task automation manager provides is optimized to facilitate initial discovery.</span></span> <span data-ttu-id="c9023-434">詳細な調査のためには、対応するデータ プロジェクトおよびその実行の詳細を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-434">For detailed investigation, you must look at the corresponding data project and its execution details.</span></span>

<span data-ttu-id="c9023-435">現在、次のデータ検証がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c9023-435">The following data validations are currently supported:</span></span>

- <span data-ttu-id="c9023-436">**ジョブ ステータス** – この検証は、ジョブが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="c9023-436">**Job status** – This validation checks whether the job was successful.</span></span>
- <span data-ttu-id="c9023-437">**バッチ ステータス** - この検証は、バッチが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="c9023-437">**Batch status** – This validation checks whether the batch was successful.</span></span>
- <span data-ttu-id="c9023-438">**メッセージ状態** – テストが統合に関するものである場合、メッセージの状態が検証されます。</span><span class="sxs-lookup"><span data-stu-id="c9023-438">**Message status** – If the test is about integrations, the message status is validated.</span></span>
- <span data-ttu-id="c9023-439">**切り捨て** – 切り捨てが有効になっている場合は、この検証が切り捨てが発生したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="c9023-439">**Truncation** – If truncation is enabled, this validation checks whether truncation occurred.</span></span>
- <span data-ttu-id="c9023-440">**ステージングのスキップ** – **ステージングのスキップ** がテストで有効になっている場合、ステージングがスキップされたかどうかをこの検証でチェックします。</span><span class="sxs-lookup"><span data-stu-id="c9023-440">**Skip staging** – If **Skip staging** is enabled on a test, this validation checks whether staging was skipped.</span></span>

## <a name="example-1-configuration-management-for-data-projects"></a><span data-ttu-id="c9023-441">例 1: データ プロジェクトの構成管理</span><span class="sxs-lookup"><span data-stu-id="c9023-441">Example 1: Configuration management for data projects</span></span>
<span data-ttu-id="c9023-442">**\<ConfigurationOnly\>** 要素は、データ プロジェクトおよび定期的なスケジュールの構成タスクを作成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c9023-442">The **\<ConfigurationOnly\>** element can be used to create configuration tasks for data projects and recurring schedules.</span></span>

<span data-ttu-id="c9023-443">この最初の例は、定期的なスケジュールを持たないデータ プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="c9023-443">This first example configures a data project that doesn't have a recurring schedule.</span></span> <span data-ttu-id="c9023-444">2 番目の例には、定期的なスケジュールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c9023-444">The second example includes a recurring schedule.</span></span> <span data-ttu-id="c9023-445">違いは、**\<Operation\>** 要素の値です。</span><span class="sxs-lookup"><span data-stu-id="c9023-445">The difference is the value of the **\<Operation\>** element.</span></span> <span data-ttu-id="c9023-446">構成タスクのマニフェストは、ソース コントロール下にも保管する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9023-446">Manifests for configuration tasks should also be kept under source control.</span></span>

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

## <a name="example-2-automated-setup-of-demo-data"></a><span data-ttu-id="c9023-447">例 2: デモ データの自動設定</span><span class="sxs-lookup"><span data-stu-id="c9023-447">Example 2: Automated setup of demo data</span></span>
<span data-ttu-id="c9023-448">次のマニフェストは、デモ データ パッケージが共有アセット ライブラリに格納されている場合の 3 つの法人のデモ データの設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="c9023-448">The following manifest shows the setup of demo data for three legal entities when the demo data packages are stored in the Shared asset library.</span></span>

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

