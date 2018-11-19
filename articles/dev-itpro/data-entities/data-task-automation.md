---
title: "データ タスクの自動化"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータ タスク自動化を使用して、各種のデータ タスクを簡単に繰り返し、各タスクの結果を検証する方法について説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 11/02/2018
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
ms.sourcegitcommit: 8b9b80b0e7d3d6b66f241e24e58dd9b91a55b975
ms.openlocfilehash: 27c5192da2eca78f026bd5f19e279732675f148a
ms.contentlocale: ja-jp
ms.lasthandoff: 11/02/2018

---

# <a name="data-task-automation"></a><span data-ttu-id="956d6-103">データ タスクの自動化</span><span class="sxs-lookup"><span data-stu-id="956d6-103">Data task automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="956d6-104">Microsoft Dynamics 365 for Finance and Operations のデータ タスク自動化は、各種のデータ タスクを簡単に繰り返し、各タスクの結果を検証を可能にします。</span><span class="sxs-lookup"><span data-stu-id="956d6-104">Data task automation in Microsoft Dynamics 365 for Finance and Operations lets you easily repeat many types of data tasks and validate the outcome of each task.</span></span> <span data-ttu-id="956d6-105">データ タスクの自動化は、実装フェーズにあるプロジェクトで非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="956d6-105">Data task automation is very useful for projects that are in the implementation phase.</span></span> <span data-ttu-id="956d6-106">たとえば、データ プロジェクトの作成およびコンフィギュレーションを自動化することができます。</span><span class="sxs-lookup"><span data-stu-id="956d6-106">For example, you can automate the creation and configuration of data projects.</span></span> <span data-ttu-id="956d6-107">また、デモ データおよび高品質の構成データ、およびデータ移行に関連する他のタスクなどの、インポート/エクスポート オペレーションの実行を構成およびトリガーすることができます。</span><span class="sxs-lookup"><span data-stu-id="956d6-107">You can also configure and trigger the execution of import/export operations, such as the setup of demo data and golden configuration data, and other tasks that are related to data migration.</span></span> <span data-ttu-id="956d6-108">また、タスクの結果の検証を使用して、データ エンティティの自動テストを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="956d6-108">You can also create automated testing of data entities by using task outcome validation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="956d6-109">現時点では、オンプレミス環境ではデータ タスクの自動化はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="956d6-109">Data task automation isn't currently supported for on-premises environments.</span></span>

<span data-ttu-id="956d6-110">データ タスクの自動化のために次の方法をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="956d6-110">We recommend the following approach for data task automation.</span></span>

1. <span data-ttu-id="956d6-111">自動化の恩恵を受けるデータ関連のタスクを特定する。</span><span class="sxs-lookup"><span data-stu-id="956d6-111">Identify the data-related tasks that will benefit from automation.</span></span>

    <span data-ttu-id="956d6-112">実装チームは自分たちの構成管理計画とデータ移行計画をレビューして、自動化のための潜在的なデータ タスクを識別すること、またデータ エンティティのテスト ケースも識別することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="956d6-112">We recommend that implementation teams review their configuration management plan and data migration plan to identify potential data tasks for automation, and also to identify data entity test cases.</span></span>

2. <span data-ttu-id="956d6-113">タスクを定義します。</span><span class="sxs-lookup"><span data-stu-id="956d6-113">Define tasks.</span></span>

    <span data-ttu-id="956d6-114">タスクは、XML マニフェストで定義されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-114">Tasks are defined in an XML manifest.</span></span> <span data-ttu-id="956d6-115">アプリケーション ライフ サイクルの管理 (ALM) 戦略では、構成管理の一部としてソース管理下のマニフェストを保持することができます。</span><span class="sxs-lookup"><span data-stu-id="956d6-115">You can keep your manifest under source control as part of configuration management in your application lifecycle management (ALM) strategy.</span></span>

3. <span data-ttu-id="956d6-116">Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリでのデータ タスクの自動化に関連するデータ パッケージを配置します。</span><span class="sxs-lookup"><span data-stu-id="956d6-116">Put the data packages that are related to data task automation in the Shared asset library of Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="956d6-117">また、必要に応じて特定の LCS プロジェクトを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="956d6-117">You can also use a specific LCS project as you require.</span></span>

    <span data-ttu-id="956d6-118">データ タスク自動化マネージャは、LCS プロジェクトに関連するサンドボックスまたは実稼動環境からパッケージを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="956d6-118">Data task automation manager can consume packages from any sandbox and/or production environment that is related to the LCS project.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="956d6-119">Finance and Operations のデータ タスク自動化マネージャーを実行するユーザー アカウントは、LCS およびデータ パッケージのマニフェストで参照される LCS プロジェクトにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-119">The user account that runs Data task automation manager in Finance and Operations must have access to LCS and to the LCS project that is referenced in the manifest for data packages.</span></span>
    > - <span data-ttu-id="956d6-120">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合アプリケーション プログラミング インターフェイス (API) を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="956d6-120">Although data task automation can be run in any environment in the cloud, we strongly recommend that you not run any import/export tasks that use integration application programming interfaces (APIs) in a production environment.</span></span> <span data-ttu-id="956d6-121">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-121">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

4. <span data-ttu-id="956d6-122">データ タスクを実行し、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="956d6-122">Run the data tasks, and then review the outcomes.</span></span>

    <span data-ttu-id="956d6-123">データ タスク自動化マネージャは、各タスクの成功または失敗の結果を提供します。</span><span class="sxs-lookup"><span data-stu-id="956d6-123">Data task automation manager provides the success or failure outcome for each task.</span></span> <span data-ttu-id="956d6-124">また、タスクが失敗した理由に関する見解も提供します。</span><span class="sxs-lookup"><span data-stu-id="956d6-124">It also provides insights into the reason why a task failed.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="956d6-125">データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合 API を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。</span><span class="sxs-lookup"><span data-stu-id="956d6-125">Although data task automation can be run in any environments in the cloud, we recommend that you not run any import/export tasks that use integration APIs in a production environment.</span></span> <span data-ttu-id="956d6-126">統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-126">Data task automation that involves integration APIs should be used only for automated testing.</span></span>

<span data-ttu-id="956d6-127">次のビデオは、Data Task Automation Manager の初期リリースを紹介する TechTalk の 55 分です。[タスク自動化フレームワーク](https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4)。</span><span class="sxs-lookup"><span data-stu-id="956d6-127">The following video is a 55-minute TechTalk that walks you through an early release of Data task automation manager: [Task automation framework](https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4).</span></span>

## <a name="task-manifest"></a><span data-ttu-id="956d6-128">タスク マニフェスト</span><span class="sxs-lookup"><span data-stu-id="956d6-128">Task manifest</span></span>
<span data-ttu-id="956d6-129">タスクは、XML マニフェストで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-129">A task must be defined in an XML manifest.</span></span> <span data-ttu-id="956d6-130">このセクションでは、マニフェストについて説明します。</span><span class="sxs-lookup"><span data-stu-id="956d6-130">This section describes the manifest.</span></span> <span data-ttu-id="956d6-131">マニフェストを名前付けしデザインする方法の指針については、このトピックの後半の、「マニフェストのデザインに対するベスト プラクティス」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="956d6-131">For guidance about how to name and design the manifest, see the "Best practices for manifest design" section later in this topic.</span></span>

### <a name="manifest-root"></a><span data-ttu-id="956d6-132">マニフェスト ルート</span><span class="sxs-lookup"><span data-stu-id="956d6-132">Manifest root</span></span>
<span data-ttu-id="956d6-133">**\<TestManifest\>** 要素は、マニフェストのルートです。</span><span class="sxs-lookup"><span data-stu-id="956d6-133">The **\<TestManifest\>** element is the root of the manifest.</span></span> <span data-ttu-id="956d6-134">その他のすべての要素はこの要素の子です。</span><span class="sxs-lookup"><span data-stu-id="956d6-134">All other elements are children of this element.</span></span>

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

| <span data-ttu-id="956d6-135">要素</span><span class="sxs-lookup"><span data-stu-id="956d6-135">Element</span></span>          | <span data-ttu-id="956d6-136">要素の基数</span><span class="sxs-lookup"><span data-stu-id="956d6-136">Element Cardinality</span></span> | <span data-ttu-id="956d6-137">属性</span><span class="sxs-lookup"><span data-stu-id="956d6-137">Attributes</span></span> | <span data-ttu-id="956d6-138">属性の説明</span><span class="sxs-lookup"><span data-stu-id="956d6-138">Attribute description</span></span>                                     |
|------------------|---------------------|------------|-----------------------------------------------------------|
| <span data-ttu-id="956d6-139">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="956d6-139">\<TestManifest\></span></span> | <span data-ttu-id="956d6-140">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-140">1..1</span></span>                | <span data-ttu-id="956d6-141">名前</span><span class="sxs-lookup"><span data-stu-id="956d6-141">name</span></span>       | <span data-ttu-id="956d6-142">*名前*はマニフェストの目的を識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="956d6-142">The *name* helps to identify the purpose of the manifest.</span></span> |

### <a name="shared-setup"></a><span data-ttu-id="956d6-143">共有された設定</span><span class="sxs-lookup"><span data-stu-id="956d6-143">Shared setup</span></span>
<span data-ttu-id="956d6-144">**共有セットアップ** セクションは、全般的なタスクのパラメーターとマニフェスト内のすべてのタスクの動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="956d6-144">The **Shared setup** section defines general task parameters and behaviors for all tasks in the manifest.</span></span>

| <span data-ttu-id="956d6-145">親要素</span><span class="sxs-lookup"><span data-stu-id="956d6-145">Parent element</span></span>   | <span data-ttu-id="956d6-146">要素</span><span class="sxs-lookup"><span data-stu-id="956d6-146">Element</span></span>         | <span data-ttu-id="956d6-147">要素の基数</span><span class="sxs-lookup"><span data-stu-id="956d6-147">Element Cardinality</span></span> | <span data-ttu-id="956d6-148">属性</span><span class="sxs-lookup"><span data-stu-id="956d6-148">Attributes</span></span> | <span data-ttu-id="956d6-149">属性の説明</span><span class="sxs-lookup"><span data-stu-id="956d6-149">Attribute description</span></span>            |
|------------------|-----------------|---------------------|------------|----------------------------------|
| <span data-ttu-id="956d6-150">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="956d6-150">\<TestManifest\></span></span> | <span data-ttu-id="956d6-151">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="956d6-151">\<SharedSetup\></span></span> | <span data-ttu-id="956d6-152">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-152">1..1</span></span>                | \-         | <span data-ttu-id="956d6-153">この要素には属性はありません。</span><span class="sxs-lookup"><span data-stu-id="956d6-153">This element takes no attributes.</span></span> |

### <a name="data-files"></a><span data-ttu-id="956d6-154">データ ファイル</span><span class="sxs-lookup"><span data-stu-id="956d6-154">Data files</span></span>
<span data-ttu-id="956d6-155">**\<DataFile\>** 要素は、マニフェスト内のタスクが使用するデータ パッケージとデータ ファイルを定義します。</span><span class="sxs-lookup"><span data-stu-id="956d6-155">**\<DataFile\>** elements define the data packages and data files that the tasks in the manifest will use.</span></span> <span data-ttu-id="956d6-156">データ ファイルは、LCS プロジェクトの LCS アセット ライブラリまたは共有アセット ライブラリのいずれかになければなりません。</span><span class="sxs-lookup"><span data-stu-id="956d6-156">The data files must be either in the LCS asset library of your LCS project or in the Shared asset library.</span></span>

```
<DataFile ID='SharedSetup' name='Demo data-7.3-100-System and Shared'  assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsHQUS' name='Demo data-7.3-200-Financials-HQUS' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPICH' name='Demo data-7.3-200-Financials-PICH' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPIFB' name='Demo data-7.3-200-Financials-PIFB' assetType='Data package' lcsProjectId=''/>
```

| <span data-ttu-id="956d6-157">親要素</span><span class="sxs-lookup"><span data-stu-id="956d6-157">Parent element</span></span>  | <span data-ttu-id="956d6-158">要素</span><span class="sxs-lookup"><span data-stu-id="956d6-158">Element</span></span>      | <span data-ttu-id="956d6-159">要素の基数</span><span class="sxs-lookup"><span data-stu-id="956d6-159">Element Cardinality</span></span> | <span data-ttu-id="956d6-160">属性</span><span class="sxs-lookup"><span data-stu-id="956d6-160">Attributes</span></span>   | <span data-ttu-id="956d6-161">属性の説明</span><span class="sxs-lookup"><span data-stu-id="956d6-161">Attribute description</span></span> |
|-----------------|--------------|---------------------|--------------|-----------------------|
| <span data-ttu-id="956d6-162">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="956d6-162">\<SharedSetup\></span></span> | <span data-ttu-id="956d6-163">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="956d6-163">\<DataFile\></span></span> | <span data-ttu-id="956d6-164">1..n</span><span class="sxs-lookup"><span data-stu-id="956d6-164">1..n</span></span>                | \-           | \- |
|                 | <span data-ttu-id="956d6-165">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="956d6-165">\<DataFile\></span></span> | \-                  | <span data-ttu-id="956d6-166">ID</span><span class="sxs-lookup"><span data-stu-id="956d6-166">ID</span></span>           | |
|                 | <span data-ttu-id="956d6-167">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="956d6-167">\<DataFile\></span></span> | \-                  | <span data-ttu-id="956d6-168">名前</span><span class="sxs-lookup"><span data-stu-id="956d6-168">name</span></span>         | <span data-ttu-id="956d6-169">データ ファイルを表す資産の名前。</span><span class="sxs-lookup"><span data-stu-id="956d6-169">Name of the asset that represents the data file.</span></span> |
|                 | <span data-ttu-id="956d6-170">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="956d6-170">\<DataFile\></span></span> | \-                  | <span data-ttu-id="956d6-171">assetType</span><span class="sxs-lookup"><span data-stu-id="956d6-171">assetType</span></span>    | <span data-ttu-id="956d6-172">データ ファイルを格納する LCS 資産ライブラリでの資産タイプ。</span><span class="sxs-lookup"><span data-stu-id="956d6-172">The asset type in LCS asset library that stores the data file.</span></span> <span data-ttu-id="956d6-173">これは、LCS アセット ライブラリで示されたように、アセット タイプの名前です。</span><span class="sxs-lookup"><span data-stu-id="956d6-173">This is the asset type name as shown in LCS asset library.</span></span> |
|                 | <span data-ttu-id="956d6-174">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="956d6-174">\<DataFile\></span></span> | \-                  | <span data-ttu-id="956d6-175">lcsProjectId</span><span class="sxs-lookup"><span data-stu-id="956d6-175">lcsProjectId</span></span> | <span data-ttu-id="956d6-176">その資産ライブラリで LCS プロジェクトにはデータ ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="956d6-176">The LCS project that has the data file in its asset library.</span></span> <span data-ttu-id="956d6-177">プロジェクト ID が " として指定されている場合は、共有アセット ライブラリを示します。</span><span class="sxs-lookup"><span data-stu-id="956d6-177">If the project ID is specified as '' then, it indicates the Shared asset library.</span></span> |

### <a name="data-project-definition"></a><span data-ttu-id="956d6-178">データ プロジェクト定義</span><span class="sxs-lookup"><span data-stu-id="956d6-178">Data project definition</span></span>
<span data-ttu-id="956d6-179">**\<JobDefinition\>** 要素は、データ プロジェクト定義を定義します。</span><span class="sxs-lookup"><span data-stu-id="956d6-179">The **\<JobDefinition\>** element defines the data project definition.</span></span> <span data-ttu-id="956d6-180">マニフェストには複数のジョブ定義があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-180">There can be more than one job definition in a manifest.</span></span>

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

| <span data-ttu-id="956d6-181">親要素</span><span class="sxs-lookup"><span data-stu-id="956d6-181">Parent element</span></span>    | <span data-ttu-id="956d6-182">要素</span><span class="sxs-lookup"><span data-stu-id="956d6-182">Element</span></span>                          | <span data-ttu-id="956d6-183">要素の基数</span><span class="sxs-lookup"><span data-stu-id="956d6-183">Element cardinality</span></span> | <span data-ttu-id="956d6-184">属性</span><span class="sxs-lookup"><span data-stu-id="956d6-184">Attribute</span></span> | <span data-ttu-id="956d6-185">説明</span><span class="sxs-lookup"><span data-stu-id="956d6-185">Description</span></span> |
|-------------------|----------------------------------|---------------------|-----------|-------------|
| <span data-ttu-id="956d6-186">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="956d6-186">\<SharedSetup\></span></span>   | <span data-ttu-id="956d6-187">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="956d6-187">\<JobDefinition\></span></span>                | <span data-ttu-id="956d6-188">1..n</span><span class="sxs-lookup"><span data-stu-id="956d6-188">1..n</span></span>                | <span data-ttu-id="956d6-189">ID</span><span class="sxs-lookup"><span data-stu-id="956d6-189">ID</span></span>        | <span data-ttu-id="956d6-190">タスクでジョブ定義 ID を使用してデータ プロジェクトで使用する定義を参照できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-190">The job definition ID is used in the tasks to reference the definition to be used for the data project.</span></span> |
| <span data-ttu-id="956d6-191">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="956d6-191">\<JobDefinition\></span></span> | <span data-ttu-id="956d6-192">[\<操作\>]</span><span class="sxs-lookup"><span data-stu-id="956d6-192">\<Operation\></span></span>                    | <span data-ttu-id="956d6-193">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-193">1..1</span></span>                | \-        | <span data-ttu-id="956d6-194">実行される操作は、次の値によって指定されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-194">The operation to be performed is specified by the following values:</span></span> <br> <span data-ttu-id="956d6-195">- インポート</span><span class="sxs-lookup"><span data-stu-id="956d6-195">- Import</span></span> <br> <span data-ttu-id="956d6-196">- エクスポート</span><span class="sxs-lookup"><span data-stu-id="956d6-196">- Export</span></span> |
|                   | <span data-ttu-id="956d6-197">\<切り詰め\></span><span class="sxs-lookup"><span data-stu-id="956d6-197">\<Truncate\></span></span>                     | <span data-ttu-id="956d6-198">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-198">1..1</span></span>                | \-        | <span data-ttu-id="956d6-199">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-199">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="956d6-200">これは操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-200">This is applicable only when operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="956d6-201">\<モード\></span><span class="sxs-lookup"><span data-stu-id="956d6-201">\<Mode\></span></span>                         | <span data-ttu-id="956d6-202">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-202">1..1</span></span>                | \-        | <span data-ttu-id="956d6-203">モードでは、操作を実行する必要があるメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="956d6-203">The mode specifies the method using which the operation must be performed.</span></span> <span data-ttu-id="956d6-204">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="956d6-204">The possible values are:</span></span><br><span data-ttu-id="956d6-205">- 非同期インポート</span><span class="sxs-lookup"><span data-stu-id="956d6-205">- Import async</span></span> <br><span data-ttu-id="956d6-206">- 非同期エクスポート</span><span class="sxs-lookup"><span data-stu-id="956d6-206">- Export async</span></span> <br><span data-ttu-id="956d6-207">- 定期的なバッチ: これは、エンキュー/デキュー API を使用します。</span><span class="sxs-lookup"><span data-stu-id="956d6-207">- Recurring batch: This uses the enqueue/dequeue API’s.</span></span>|
|                   | <span data-ttu-id="956d6-208">\<ConfigurationOnly\></span><span class="sxs-lookup"><span data-stu-id="956d6-208">\<ConfigurationOnly\></span></span>            | <span data-ttu-id="956d6-209">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-209">1..1</span></span>                | \-        | <span data-ttu-id="956d6-210">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-210">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="956d6-211">タスクがデータ プロジェクトをコンフィギュレーションするのみで、指定された操作を実行しない場合は、はいに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-211">This must be set to Yes if the task is only to configure the data project but not to perform the specified operation.</span></span> |
|                   | <span data-ttu-id="956d6-212">\<BatchFrequencyInMinutes\></span><span class="sxs-lookup"><span data-stu-id="956d6-212">\<BatchFrequencyInMinutes\></span></span>      | <span data-ttu-id="956d6-213">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-213">1..1</span></span>                | \-        | <span data-ttu-id="956d6-214">バッチがスケジュール設定される頻度を指定します。</span><span class="sxs-lookup"><span data-stu-id="956d6-214">This specifies the frequency in which the batch must be scheduled.</span></span> <span data-ttu-id="956d6-215">これはモードが*定期実行されるバッチ*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-215">This is applicable only when mode is set to *recurring batch*.</span></span> |
|                   | <span data-ttu-id="956d6-216">\<NumberOfTimesToRunBatch\></span><span class="sxs-lookup"><span data-stu-id="956d6-216">\<NumberOfTimesToRunBatch\></span></span>      | <span data-ttu-id="956d6-217">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-217">1..1</span></span>                | \-        | <span data-ttu-id="956d6-218">これは、スケジュールされているバッチを実行する回数の制限を設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-218">This is used to set a limit to how many times the scheduled batch should run.</span></span> <span data-ttu-id="956d6-219">これはモードが*定期実行されるバッチ*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-219">This is applicable only when mode is set to *recurring batch*.</span></span> |
|                   | <span data-ttu-id="956d6-220">\<UploadFrequencyInSeconds\></span><span class="sxs-lookup"><span data-stu-id="956d6-220">\<UploadFrequencyInSeconds\></span></span>     | <span data-ttu-id="956d6-221">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-221">1..1</span></span>                | \-        | <span data-ttu-id="956d6-222">これは、インポートする定期バッチ ジョブにファイルをアップロードする頻度を制御するために使用します。</span><span class="sxs-lookup"><span data-stu-id="956d6-222">This is used to control the rate at which a file is uploaded to the recurring batch job for import.</span></span> <span data-ttu-id="956d6-223">これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-223">This must be used only for automated testing of recurring integrations in non-production environments.</span></span> <span data-ttu-id="956d6-224">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-224">This is applicable only when mode is set to *recurring batch* and operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="956d6-225">\<TotalNumberOfTimesToUpload\></span><span class="sxs-lookup"><span data-stu-id="956d6-225">\<TotalNumberOfTimesToUpload\></span></span>   | <span data-ttu-id="956d6-226">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-226">1..1</span></span>                |           | <span data-ttu-id="956d6-227">これはファイルを繰り返しバッチにアップロードする総回数を制御します。</span><span class="sxs-lookup"><span data-stu-id="956d6-227">This controls the total number of times the file should be uploaded to the recurring batch.</span></span> <span data-ttu-id="956d6-228">これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-228">This must be used only for automated testing of recurring integrations in non-production environments.</span></span> <span data-ttu-id="956d6-229">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-229">This is applicable only when mode is set to *recurring batch* and operation is set to *Import*.</span></span> |
|                   | <span data-ttu-id="956d6-230">\<SupportedDataSoureType\></span><span class="sxs-lookup"><span data-stu-id="956d6-230">\<SupportedDataSoureType\></span></span>       | <span data-ttu-id="956d6-231">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-231">1..1</span></span>                |           | <span data-ttu-id="956d6-232">ファイルが定期的なバッチまたはパッケージに送信中であるかどうかを指定するために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-232">This must be used to specify if a file is being sent to the recurring batch or a package.</span></span> <span data-ttu-id="956d6-233">これはモードが「定期実行されるバッチ」に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-233">This is only applicable when mode is set to 'recurring batch'.</span></span> |
|                   | <span data-ttu-id="956d6-234">\<ProcessMessagesInOrder\></span><span class="sxs-lookup"><span data-stu-id="956d6-234">\<ProcessMessagesInOrder\></span></span>       | <span data-ttu-id="956d6-235">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-235">1..1</span></span>                |           | <span data-ttu-id="956d6-236">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-236">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="956d6-237">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-237">This is applicable only when mode is set to *recurring batch* and operation is *Import*.</span></span> |
|                   | <span data-ttu-id="956d6-238">\<PreventUploadWhenZeroRecords\></span><span class="sxs-lookup"><span data-stu-id="956d6-238">\<PreventUploadWhenZeroRecords\></span></span> | <span data-ttu-id="956d6-239">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-239">1..1</span></span>                |           | <span data-ttu-id="956d6-240">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-240">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="956d6-241">これはモードが*定期実行されるバッチ*に設定されており、操作が*エクスポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-241">This is applicable only when mode is set to *recurring batch* and operation is *Export*.</span></span> |
|                   | <span data-ttu-id="956d6-242">\<UseCompanyFromMessage\></span><span class="sxs-lookup"><span data-stu-id="956d6-242">\<UseCompanyFromMessage\></span></span>        | <span data-ttu-id="956d6-243">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-243">1..1</span></span>                |           | <span data-ttu-id="956d6-244">これははい、またはいいえに設定できるブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-244">This is a Boolean field which can be set to Yes or No.</span></span> <span data-ttu-id="956d6-245">これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*の場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-245">This is applicable only when mode is set to *recurring batch* and operation is *Import*.</span></span> |
|                   | <span data-ttu-id="956d6-246">\<LegalEntity\></span><span class="sxs-lookup"><span data-stu-id="956d6-246">\<LegalEntity\></span></span>                  | <span data-ttu-id="956d6-247">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-247">1..1</span></span>                |           | <span data-ttu-id="956d6-248">これをは、インポート/エクスポート ジョブを実行する必要がある法人を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-248">This is used to specify the legal entity in which the import/export job must be executed.</span></span> |
|                   | <span data-ttu-id="956d6-249">\<ConfigurationOnly\></span><span class="sxs-lookup"><span data-stu-id="956d6-249">\<ConfigurationOnly\></span></span>            | <span data-ttu-id="956d6-250">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-250">1..1</span></span>                |           | <span data-ttu-id="956d6-251">これを使用して、データのプロジェクトおよび構成する定期的なスケジュールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-251">This is used to create data projects and recurring schedules to be configured.</span></span> <span data-ttu-id="956d6-252">インポートまたはエクスポートの操作は実行されません。</span><span class="sxs-lookup"><span data-stu-id="956d6-252">The operation of import or export will not be executed.</span></span> <span data-ttu-id="956d6-253">ただし、データ プロジェクトを正しく設定するには、操作とモードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-253">However, it is required to specify the operation and mode for the data project to be configured correctly.</span></span> <span data-ttu-id="956d6-254">これは、はいまたはいいえを取るブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-254">This is a Boolean field which takes Yes or No.</span></span> |

### <a name="entity-setup"></a><span data-ttu-id="956d6-255">エンティティ設定</span><span class="sxs-lookup"><span data-stu-id="956d6-255">Entity setup</span></span>
<span data-ttu-id="956d6-256">**エンティティ設定** セクションは、マニフェストのタスクが使用するエンティティの特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="956d6-256">The **Entity setup** section defines the characteristics of an entity that a task in the manifest will use.</span></span> <span data-ttu-id="956d6-257">マニフェスト内のタスクによって使用されるエンティティごとに、1 つずつ複数の定義が存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-257">There can be more than one definition, one for each entity that is used by the tasks in the manifest.</span></span>

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

| <span data-ttu-id="956d6-258">親要素</span><span class="sxs-lookup"><span data-stu-id="956d6-258">Parent element</span></span>         | <span data-ttu-id="956d6-259">要素</span><span class="sxs-lookup"><span data-stu-id="956d6-259">Element</span></span>                              | <span data-ttu-id="956d6-260">要素の基数</span><span class="sxs-lookup"><span data-stu-id="956d6-260">Element cardinality</span></span> | <span data-ttu-id="956d6-261">属性</span><span class="sxs-lookup"><span data-stu-id="956d6-261">Attribute</span></span>         | <span data-ttu-id="956d6-262">説明</span><span class="sxs-lookup"><span data-stu-id="956d6-262">Description</span></span> |
|------------------------|--------------------------------------|---------------------|-------------------|-------------|
| <span data-ttu-id="956d6-263">\<SharedSetup\></span><span class="sxs-lookup"><span data-stu-id="956d6-263">\<SharedSetup\></span></span>        | <span data-ttu-id="956d6-264">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="956d6-264">\<EntitySetup\></span></span>                      | <span data-ttu-id="956d6-265">1..n</span><span class="sxs-lookup"><span data-stu-id="956d6-265">1..n</span></span>                | <span data-ttu-id="956d6-266">ID</span><span class="sxs-lookup"><span data-stu-id="956d6-266">ID</span></span>                | <span data-ttu-id="956d6-267">タスクが使用するエンティティ定義を参照するために使用される ID。</span><span class="sxs-lookup"><span data-stu-id="956d6-267">An identification that will be used by tasks to reference an entity definition to be used.</span></span> |
| <span data-ttu-id="956d6-268">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="956d6-268">\<EntitySetup\></span></span>        | <span data-ttu-id="956d6-269">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="956d6-269">\<Entity\></span></span>                           | <span data-ttu-id="956d6-270">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-270">1..1</span></span>                | <span data-ttu-id="956d6-271">名前</span><span class="sxs-lookup"><span data-stu-id="956d6-271">name</span></span>              | <span data-ttu-id="956d6-272">エンティティ要素は、エンティティの名前で識別されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-272">The entity element is identified by the entity's name.</span></span> <span data-ttu-id="956d6-273">ただし、簡単なマニフェスト定義を容易にするために、この要素は \* ワイルド カードとしてもサポートしています。これは、すべてのエンティティがタスクで使用されていることを意味しています。</span><span class="sxs-lookup"><span data-stu-id="956d6-273">However, to facilitate easy manifest definition, this element also supports \* as a wild card which will mean all entities being used in a task.</span></span> <span data-ttu-id="956d6-274">これは、タスク内の何百ものエンティティを持つデータ パッケージを使用する場合に非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="956d6-274">This comes in very handy when using data packages with hundreds of entities in a task.</span></span> |
| <span data-ttu-id="956d6-275">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="956d6-275">\<Entity\></span></span>             | <span data-ttu-id="956d6-276">\<SourceDataFormatName\></span><span class="sxs-lookup"><span data-stu-id="956d6-276">\<SourceDataFormatName\></span></span>             | <span data-ttu-id="956d6-277">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-277">1..1</span></span>                | \-                | <span data-ttu-id="956d6-278">これはエンティティに使用されるファイル形式です。</span><span class="sxs-lookup"><span data-stu-id="956d6-278">This is the file format to be used for the entity.</span></span> |
|                        | <span data-ttu-id="956d6-279">\<ChangeTracking\></span><span class="sxs-lookup"><span data-stu-id="956d6-279">\<ChangeTracking\></span></span>                   | <span data-ttu-id="956d6-280">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-280">1..1</span></span>                | \-                | <span data-ttu-id="956d6-281">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-281">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="956d6-282">エンティティ全体で変更追跡を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="956d6-282">It enables or disables change tracking on the entire entity.</span></span> |
|                        | <span data-ttu-id="956d6-283">\<PublishToBYOD\></span><span class="sxs-lookup"><span data-stu-id="956d6-283">\<PublishToBYOD\></span></span>                    | <span data-ttu-id="956d6-284">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-284">1..1</span></span>                | \-                | <span data-ttu-id="956d6-285">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-285">This is a Boolean field with possible values of Yes or No.</span></span> |
|                        | <span data-ttu-id="956d6-286">\<DefaultRefreshType\></span><span class="sxs-lookup"><span data-stu-id="956d6-286">\<DefaultRefreshType\></span></span>               | <span data-ttu-id="956d6-287">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-287">1..1</span></span>                | \-                | <span data-ttu-id="956d6-288">これにより、エンティティの既定の更新頻度が設定されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-288">This sets the default refresh rate on the entity.</span></span> <span data-ttu-id="956d6-289">使用可能な値は*増分プッシュのみ*または*フル プッシュ*です。</span><span class="sxs-lookup"><span data-stu-id="956d6-289">The possible values are *Incremental push only* or *Full push*.</span></span> |
|                        | <span data-ttu-id="956d6-290">\<ExcelWorkSheetName\></span><span class="sxs-lookup"><span data-stu-id="956d6-290">\<ExcelWorkSheetName\></span></span>               | <span data-ttu-id="956d6-291">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-291">1..1</span></span>                | \-                | <span data-ttu-id="956d6-292">これはエンティティに使用するワークシートを指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-292">This is used to specify the worksheet to be used for the entity.</span></span> |
|                        | <span data-ttu-id="956d6-293">\<SelectFields\></span><span class="sxs-lookup"><span data-stu-id="956d6-293">\<SelectFields\></span></span>                     | <span data-ttu-id="956d6-294">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-294">1..1</span></span>                | \-                | <span data-ttu-id="956d6-295">これは、エクスポート操作のテンプレートに含まれるフィールドを指定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-295">This can be used to specify the fields to be included in the template for an export operation.</span></span> |
|                        | <span data-ttu-id="956d6-296">\<SetBasedProcessing\></span><span class="sxs-lookup"><span data-stu-id="956d6-296">\<SetBasedProcessing\></span></span>               | <span data-ttu-id="956d6-297">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-297">1..1</span></span>                | \-                | <span data-ttu-id="956d6-298">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-298">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="956d6-299">エンティティのセット ベースのプロセスを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-299">It is used to enable or disable set based processing on an entity.</span></span> |
|                        | <span data-ttu-id="956d6-300">\<FailBatchOnErrorForExecutionUnit\></span><span class="sxs-lookup"><span data-stu-id="956d6-300">\<FailBatchOnErrorForExecutionUnit\></span></span> | <span data-ttu-id="956d6-301">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-301">1..1</span></span>                | \-                | <span data-ttu-id="956d6-302">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-302">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="956d6-303">エンティティの実行単位レベルでエラーを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-303">It is used to enable or disable failure at execution unit level on an entity.</span></span> |
|                        | <span data-ttu-id="956d6-304">\<FailBatchOnErrorForLevel\></span><span class="sxs-lookup"><span data-stu-id="956d6-304">\<FailBatchOnErrorForLevel\></span></span>         | <span data-ttu-id="956d6-305">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-305">1..1</span></span>                | \-                | <span data-ttu-id="956d6-306">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-306">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="956d6-307">エンティティの実行レベルでエラーを有効または無効にするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-307">It is used to enable or disable failure at execution level on an entity.</span></span> |
|                        | <span data-ttu-id="956d6-308">\<DisableEntity\></span><span class="sxs-lookup"><span data-stu-id="956d6-308">\<DisableEntity\></span></span>                    | <span data-ttu-id="956d6-309">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-309">1..1</span></span>                | \-                | <span data-ttu-id="956d6-310">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-310">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="956d6-311">データ プロジェクトでエンティティを有効化または無効化するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-311">It is used to enable or disable an entity in a data project.</span></span> |
|                        | <span data-ttu-id="956d6-312">\<SkipStaging\></span><span class="sxs-lookup"><span data-stu-id="956d6-312">\<SkipStaging\></span></span>                      | <span data-ttu-id="956d6-313">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-313">1..1</span></span>                | \-                | <span data-ttu-id="956d6-314">これは、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-314">This is a Boolean field with possible values of Yes or No.</span></span> <span data-ttu-id="956d6-315">エクスポート中にエンティティのステージング テーブルをスキップするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-315">It is used to skip staging table for an entity during exports.</span></span> |
|                        | <span data-ttu-id="956d6-316">\<ParallelProcessing\></span><span class="sxs-lookup"><span data-stu-id="956d6-316">\<ParallelProcessing\></span></span>               | <span data-ttu-id="956d6-317">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-317">1..1</span></span>                | \-                | <span data-ttu-id="956d6-318">これは、エンティティに対して設定された並列処理を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-318">This is used to define the parallel processing set up for an entity.</span></span> <span data-ttu-id="956d6-319">タスクの始まりで既に終了する場合、タスクはこれらの設定を削除し、その実行の終わりに作成された設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="956d6-319">The task will delete these settings if already exits at the beginning of the task and it will delete the created settings at the end of its execution.</span></span> |
| <span data-ttu-id="956d6-320">\<ParallelProcessing\></span><span class="sxs-lookup"><span data-stu-id="956d6-320">\<ParallelProcessing\></span></span> | <span data-ttu-id="956d6-321">\<しきい値\></span><span class="sxs-lookup"><span data-stu-id="956d6-321">\<Threshold\></span></span>                        | <span data-ttu-id="956d6-322">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-322">1..1</span></span>                | \-                | <span data-ttu-id="956d6-323">並列処理のルールのしきい値を指定します。</span><span class="sxs-lookup"><span data-stu-id="956d6-323">This specifies the threshold for the parallel processing rule.</span></span> |
|                        | <span data-ttu-id="956d6-324">\<TaskCount\></span><span class="sxs-lookup"><span data-stu-id="956d6-324">\<TaskCount\></span></span>                        | <span data-ttu-id="956d6-325">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-325">1..1</span></span>                | \-                | <span data-ttu-id="956d6-326">これは、並列処理に使用される並列タスクの数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-326">This is used to specify the number of parallel tasks to be used for parallel processing.</span></span> |
| <span data-ttu-id="956d6-327">\<エンティティ\></span><span class="sxs-lookup"><span data-stu-id="956d6-327">\<Entity\></span></span>             | <span data-ttu-id="956d6-328">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="956d6-328">\<MappingDetail\></span></span>                    | <span data-ttu-id="956d6-329">0..n</span><span class="sxs-lookup"><span data-stu-id="956d6-329">0..n</span></span>                | \-                | <span data-ttu-id="956d6-330">*自動生成*、*自動既定値*およびエンティティのマッピングで他の設定を構成できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-330">Allows to configure the *auto generate*, *auto default* and other settings on the mapping for an entity.</span></span> |
|                        | <span data-ttu-id="956d6-331">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="956d6-331">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="956d6-332">StagingFieldName</span><span class="sxs-lookup"><span data-stu-id="956d6-332">StagingFieldName</span></span>  | <span data-ttu-id="956d6-333">この属性は、設定を指定するエンティティ列を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-333">This attribute is used to identify the entity column for which the settings are to be specified.</span></span> |
|                        | <span data-ttu-id="956d6-334">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="956d6-334">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="956d6-335">AutoGenerate</span><span class="sxs-lookup"><span data-stu-id="956d6-335">AutoGenerate</span></span>      | <span data-ttu-id="956d6-336">これは、自動生成オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-336">This is a Boolean field with possible values of Yes or No for enabling/disabling auto generate option.</span></span> |
|                        | <span data-ttu-id="956d6-337">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="956d6-337">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="956d6-338">AutoDefault</span><span class="sxs-lookup"><span data-stu-id="956d6-338">AutoDefault</span></span>       | <span data-ttu-id="956d6-339">これは、自動既定オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-339">This is a Boolean field with possible values of Yes or No for enabling/disabling auto default option.</span></span> |
|                        | <span data-ttu-id="956d6-340">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="956d6-340">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="956d6-341">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="956d6-341">DefaultValue</span></span>      | <span data-ttu-id="956d6-342">これは、自動既定設定が有効な場合に使用される既定値です。</span><span class="sxs-lookup"><span data-stu-id="956d6-342">This is the default value to be used if auto defaulting is enabled.</span></span> |
|                        | <span data-ttu-id="956d6-343">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="956d6-343">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="956d6-344">IgnoreBlankValues</span><span class="sxs-lookup"><span data-stu-id="956d6-344">IgnoreBlankValues</span></span> | <span data-ttu-id="956d6-345">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-345">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |
|                        | <span data-ttu-id="956d6-346">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="956d6-346">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="956d6-347">TextQualifier</span><span class="sxs-lookup"><span data-stu-id="956d6-347">TextQualifier</span></span>     | <span data-ttu-id="956d6-348">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-348">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |
|                        | <span data-ttu-id="956d6-349">\<MappingDetail\></span><span class="sxs-lookup"><span data-stu-id="956d6-349">\<MappingDetail\></span></span>                    | \-                  | <span data-ttu-id="956d6-350">UseEnumLabel</span><span class="sxs-lookup"><span data-stu-id="956d6-350">UseEnumLabel</span></span>      | <span data-ttu-id="956d6-351">これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="956d6-351">This is a Boolean field with possible values of Yes or No for enabling/disabling this option.</span></span> |

### <a name="test-groups"></a><span data-ttu-id="956d6-352">テスト グループ</span><span class="sxs-lookup"><span data-stu-id="956d6-352">Test groups</span></span>
<span data-ttu-id="956d6-353">テスト グループは、マニフェストの関連するタスクを整理するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-353">Test groups can be used to organize related tasks in a manifest.</span></span> <span data-ttu-id="956d6-354">マニフェストには複数のテスト グループがあります。</span><span class="sxs-lookup"><span data-stu-id="956d6-354">There can be more than one test group in a manifest.</span></span>

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

| <span data-ttu-id="956d6-355">親要素</span><span class="sxs-lookup"><span data-stu-id="956d6-355">Parent element</span></span>   | <span data-ttu-id="956d6-356">要素</span><span class="sxs-lookup"><span data-stu-id="956d6-356">Element</span></span>           | <span data-ttu-id="956d6-357">要素の基数</span><span class="sxs-lookup"><span data-stu-id="956d6-357">Element Cardinality</span></span> | <span data-ttu-id="956d6-358">属性</span><span class="sxs-lookup"><span data-stu-id="956d6-358">Attributes</span></span>  | <span data-ttu-id="956d6-359">説明</span><span class="sxs-lookup"><span data-stu-id="956d6-359">Description</span></span> |
|------------------|-------------------|---------------------|-------------|-------------|
| <span data-ttu-id="956d6-360">\<TestManifest\></span><span class="sxs-lookup"><span data-stu-id="956d6-360">\<TestManifest\></span></span> | <span data-ttu-id="956d6-361">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="956d6-361">\<TestGroup\></span></span>     | <span data-ttu-id="956d6-362">1..n</span><span class="sxs-lookup"><span data-stu-id="956d6-362">1..n</span></span>                | \-          | \- |
|                  | <span data-ttu-id="956d6-363">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="956d6-363">\<TestGroup\></span></span>     | <span data-ttu-id="956d6-364">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-364">1..1</span></span>                | <span data-ttu-id="956d6-365">氏名</span><span class="sxs-lookup"><span data-stu-id="956d6-365">Name</span></span>        | <span data-ttu-id="956d6-366">これは、グループの機能上の理由を特定するための名前です。</span><span class="sxs-lookup"><span data-stu-id="956d6-366">This is the name for the group to identify its functional reason.</span></span> |
| <span data-ttu-id="956d6-367">\<TestGroup\></span><span class="sxs-lookup"><span data-stu-id="956d6-367">\<TestGroup\></span></span>    | <span data-ttu-id="956d6-368">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="956d6-368">\<TestCase\></span></span>      | <span data-ttu-id="956d6-369">1..n</span><span class="sxs-lookup"><span data-stu-id="956d6-369">1..n</span></span>                | \-          | <span data-ttu-id="956d6-370">タスクは、この要素で定義されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-370">The task is defined in this element.</span></span> <span data-ttu-id="956d6-371">タスクでは、タスク パラメータおよびタスク動作を継承する共有設定を参照できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-371">The task can refer to the shared set up to inherit task parameters and task behavior.</span></span> <span data-ttu-id="956d6-372">タスクでは、パラメータと動作もそのレベルで上書きできるため、マニフェストの管理を単純にできます。</span><span class="sxs-lookup"><span data-stu-id="956d6-372">The task can also override parameters and behavior at its level thus making the management of the manifest simple.</span></span> |
|                  | <span data-ttu-id="956d6-373">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="956d6-373">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="956d6-374">肩書き</span><span class="sxs-lookup"><span data-stu-id="956d6-374">Title</span></span>       | <span data-ttu-id="956d6-375">これはタスクのタイトルです。</span><span class="sxs-lookup"><span data-stu-id="956d6-375">This is the title for the task.</span></span> |
|                  | <span data-ttu-id="956d6-376">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="956d6-376">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="956d6-377">ID</span><span class="sxs-lookup"><span data-stu-id="956d6-377">ID</span></span>          | <span data-ttu-id="956d6-378">これはタスクの ID です。</span><span class="sxs-lookup"><span data-stu-id="956d6-378">This is the ID for the task.</span></span> <span data-ttu-id="956d6-379">これは英数字で、最大文字数制限は 10 です。</span><span class="sxs-lookup"><span data-stu-id="956d6-379">This can be alphanumeric with a max character limit of 10.</span></span> |
|                  | <span data-ttu-id="956d6-380">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="956d6-380">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="956d6-381">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="956d6-381">RepeatCount</span></span> | <span data-ttu-id="956d6-382">これは、将来の機能のプレース ホルダーです。</span><span class="sxs-lookup"><span data-stu-id="956d6-382">This is a placeholder for a future functionality.</span></span> <span data-ttu-id="956d6-383">ただし、これは値 *1* で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-383">However, this must be specified with a value of *1*.</span></span> |
|                  | <span data-ttu-id="956d6-384">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="956d6-384">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="956d6-385">TraceParser</span><span class="sxs-lookup"><span data-stu-id="956d6-385">TraceParser</span></span> | <span data-ttu-id="956d6-386">これは、将来の機能のプレース ホルダーです。</span><span class="sxs-lookup"><span data-stu-id="956d6-386">This is a placeholder for a future functionality.</span></span> <span data-ttu-id="956d6-387">ただし、これは値*オフ*で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-387">However, this must be specified with a value *off*.</span></span> |
|                  | <span data-ttu-id="956d6-388">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="956d6-388">\<TestCase\></span></span>      | \-                  | <span data-ttu-id="956d6-389">タイムアウト</span><span class="sxs-lookup"><span data-stu-id="956d6-389">Timeout</span></span>     | <span data-ttu-id="956d6-390">これは、タスク自動化マネージャーによってタスクがモニターされる最大期間です。</span><span class="sxs-lookup"><span data-stu-id="956d6-390">This is the maximum duration a task will be monitored by the task automation manager.</span></span> <span data-ttu-id="956d6-391">指定したタイムアウトを超えてタスクがまだアクティブな場合、マネージャーはマニフェスト内の次のタスクに進みます。</span><span class="sxs-lookup"><span data-stu-id="956d6-391">If the task is still active beyond the timeout specified, the manager will proceed to the next task in the manifest.</span></span> |
| <span data-ttu-id="956d6-392">\<TestCase\></span><span class="sxs-lookup"><span data-stu-id="956d6-392">\<TestCase\></span></span>     | <span data-ttu-id="956d6-393">\<DataFile\></span><span class="sxs-lookup"><span data-stu-id="956d6-393">\<DataFile\></span></span>      | <span data-ttu-id="956d6-394">1..n</span><span class="sxs-lookup"><span data-stu-id="956d6-394">1..n</span></span>                | \-          | <span data-ttu-id="956d6-395">この要素は、タスクで使用されるファイル、またはデータのプロジェクトを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-395">This element is used to define the file or data package to be used by the task.</span></span> <span data-ttu-id="956d6-396">これは、既に宣言されたファイル、またはマニフェストの共有セクションのデータ パッケージを参照できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-396">This can reference to an already declared file or a data package in the shared section of the manifest.</span></span> <span data-ttu-id="956d6-397">タスクでは、反復バッチ インポート シナリオでのみ指定された複数のデータ ファイルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="956d6-397">A task can have more than one data file specified for recurring batch import scenarios only.</span></span> <span data-ttu-id="956d6-398">他のシナリオでは、1 つ以上のファイルが指定されていても、最初のファイルがタスクによって使用されるファイルです。</span><span class="sxs-lookup"><span data-stu-id="956d6-398">For other scenarios, even if more than one files are specified, the first file is what will be used by the task.</span></span> |
|                  | <span data-ttu-id="956d6-399">\<JobDefinition\></span><span class="sxs-lookup"><span data-stu-id="956d6-399">\<JobDefinition\></span></span> | <span data-ttu-id="956d6-400">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-400">1..1</span></span>                | \-          | <span data-ttu-id="956d6-401">この要素は、タスクで使用されるデータのプロジェクトを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-401">This element is used to define the data project to be used by the task.</span></span> <span data-ttu-id="956d6-402">これは、共有セクション内のすでに宣言されているマニフェストのジョブ定義を参照できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-402">This can reference to an already declared job definition in the shared section of the manifest.</span></span> <span data-ttu-id="956d6-403">タスクでは、共有設定で定義されている値よりも新しい値にジョブ定義の要素を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="956d6-403">The task can override elements of job definition to a new value than what is defined in the shared set up.</span></span> |
|                  | <span data-ttu-id="956d6-404">\<EntitySetup\></span><span class="sxs-lookup"><span data-stu-id="956d6-404">\<EntitySetup\></span></span>   | <span data-ttu-id="956d6-405">1..1</span><span class="sxs-lookup"><span data-stu-id="956d6-405">1..1</span></span>                | \-          | <span data-ttu-id="956d6-406">この要素は、タスクで使用されるエンティティのエンティティ セットアップを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-406">This element is used to define the entity set up for entities used by the task.</span></span> <span data-ttu-id="956d6-407">これは、マニフェストの共有のセクションで既に宣言されたエンティティ セットアップを参照できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-407">This can reference to an already declared entity set up in the shared section of the manifest.</span></span> <span data-ttu-id="956d6-408">タスクでは、共有設定で定義されている値よりも新しい値にエンティティ設定の要素を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="956d6-408">The task can override elements of entity setup to a new value than what is defined in the shared set up.</span></span> |

## <a name="best-practices-for-manifest-design"></a><span data-ttu-id="956d6-409">マニフェスト デザインのためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="956d6-409">Best practices for manifest design</span></span>
<span data-ttu-id="956d6-410">さまざまな方法でマニフェストを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="956d6-410">You can define a manifest in many ways.</span></span> <span data-ttu-id="956d6-411">マニフェストをデザインするときに考慮する必要があるいくつかのポインターを次に示します。</span><span class="sxs-lookup"><span data-stu-id="956d6-411">Here are a few pointers that you should consider when you design a manifest.</span></span>

### <a name="granularity"></a><span data-ttu-id="956d6-412">粒度</span><span class="sxs-lookup"><span data-stu-id="956d6-412">Granularity</span></span>
<span data-ttu-id="956d6-413">機能的な意思決定としてマニフェストの粒度を判断することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="956d6-413">We recommend that you determine the granularity of your manifest as a functional decision.</span></span> <span data-ttu-id="956d6-414">チームは、複数のマニフェストを管理するか、または単一のマニフェストの変更を管理するかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-414">Your team must decide whether it wants to manage many manifests or manage changes in a single manifest.</span></span>

- <span data-ttu-id="956d6-415">チームが論理的に必要と考える数のマニフェストを使って開始します。</span><span class="sxs-lookup"><span data-stu-id="956d6-415">Start with as many manifests as your team thinks you logically need.</span></span> <span data-ttu-id="956d6-416">後で、チームが実際にマニフェストの実行を開始すると、予想より少ないマニフェストを使用しており、それらを結合したいと考える場合があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-416">Later, when the team actually starts to run the manifests, it might find that it uses fewer manifests than it expected, and it might want to merge them.</span></span> <span data-ttu-id="956d6-417">この場合、マニフェストをマージすることができます。</span><span class="sxs-lookup"><span data-stu-id="956d6-417">In this case, you can merge manifests.</span></span>
- <span data-ttu-id="956d6-418">職務の分離を検討する。</span><span class="sxs-lookup"><span data-stu-id="956d6-418">Consider separation of duties.</span></span> <span data-ttu-id="956d6-419">たとえば、デモ データの設定に対して 1 つのマニフェスト、環境の高品質の構成の設定に対して別のマニフェストがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-419">For example, you might have one manifest for the setup of demo data and another manifest for the setup of the golden configuration for your environment.</span></span> <span data-ttu-id="956d6-420">この方法で、チーム メンバーが使用する予定のマニフェストのみを使用することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-420">In this way, you can make sure that team members use only the manifests that they are supposed to use.</span></span>
- <span data-ttu-id="956d6-421">LCS へのユーザー アクセスについて考慮してください。</span><span class="sxs-lookup"><span data-stu-id="956d6-421">Consider user access to LCS.</span></span> <span data-ttu-id="956d6-422">たとえば、大きなおよびグローバルに配分された実装チームは、Finance and Operations の複数のインスタンスまたは複数の LCS プロジェクトを持っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-422">For example, larger and globally distributed implementation teams might have multiple instances of Finance and Operations or multiple LCS projects.</span></span>

### <a name="inheritance"></a><span data-ttu-id="956d6-423">継承</span><span class="sxs-lookup"><span data-stu-id="956d6-423">Inheritance</span></span>
<span data-ttu-id="956d6-424">マニフェスト スキーマは、マニフェスト内のすべてのタスクに適用される共通要素の継承をサポートします。</span><span class="sxs-lookup"><span data-stu-id="956d6-424">The manifest schema supports inheritance of common elements that will apply to all tasks in the manifest.</span></span> <span data-ttu-id="956d6-425">タスクは、共通の要素を上書きして一意の動作を定義できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-425">A task can override a common element to define a unique behavior.</span></span> <span data-ttu-id="956d6-426">**共通設定** セクションの目的は、構成要素の繰り返しを最小限に抑えて、可能な限り要素を再利用することです。</span><span class="sxs-lookup"><span data-stu-id="956d6-426">The purpose of the **Shared setup** section is to minimize repetition of configuration elements, so that elements are reused as much as possible.</span></span> <span data-ttu-id="956d6-427">目標は、メンテナンスと可読性を向上させるために、マニフェストを簡潔かつ清潔に保つことです。</span><span class="sxs-lookup"><span data-stu-id="956d6-427">The goal is to keep the manifest concise and clean, to improve maintenance and readability.</span></span>

### <a name="source-control"></a><span data-ttu-id="956d6-428">ソース管理</span><span class="sxs-lookup"><span data-stu-id="956d6-428">Source control</span></span>
<span data-ttu-id="956d6-429">実装チームのすべてのメンバーが使用する必要があるマニフェストは、アプリケーション オブジェクト ツリー (AOT) 内のソース コントロールに格納されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-429">Manifests that must be used by all the members of an implementation team should be stored in source control in the Application Object Tree (AOT).</span></span> <span data-ttu-id="956d6-430">この方法は、ソース管理の利点を提供するだけでなく、プロセスがすべてのユーザーに一貫した方法で配布またはマニフェストを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="956d6-430">This approach not only provides the benefits of source control, but also enables a process to distribute or make manifests available to all users in a consistent manner.</span></span> <span data-ttu-id="956d6-431">また、この方法では、マニフェストを構成に使用する場合、データ管理に関連するデータ プロジェクトの構成管理も可能です。</span><span class="sxs-lookup"><span data-stu-id="956d6-431">This approach also enables configuration management for data projects that are related to data management, if manifests are used for configuration.</span></span>

### <a name="number-of-job-definitions-and-entity-definitions"></a><span data-ttu-id="956d6-432">ジョブ定義とエンティティ定義の数</span><span class="sxs-lookup"><span data-stu-id="956d6-432">Number of job definitions and entity definitions</span></span>
<span data-ttu-id="956d6-433">使用ケースのほとんどの場合、マニフェストで 1 つのジョブ定義で十分であるのは、継承がタスク レベルでの動作を変更するために使用できるからです。</span><span class="sxs-lookup"><span data-stu-id="956d6-433">For most of the use cases, one job definition in a manifest should be enough, because inheritance can be used to change the behavior at the task level.</span></span> <span data-ttu-id="956d6-434">この原則は、エンティティの定義にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-434">This principle also applies to entity definitions.</span></span>

## <a name="validations"></a><span data-ttu-id="956d6-435">検証</span><span class="sxs-lookup"><span data-stu-id="956d6-435">Validations</span></span>
<span data-ttu-id="956d6-436">データ タスク自動化マネージャは、タスクの設定に基づいて検証を実行します。</span><span class="sxs-lookup"><span data-stu-id="956d6-436">Data task automation manager performs validations, based on the setup of a task.</span></span> <span data-ttu-id="956d6-437">タスクが失敗した場合は、タスクの完了後に、検証を表示することによって、エラーの原因をすばやく確認できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-437">If a task fails, you can quickly determine the reason for the failure by viewing the validations after the task is completed.</span></span> <span data-ttu-id="956d6-438">データ タスク自動化マネージャーが提供する情報のレベルは、初期検出を容易にするために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="956d6-438">The level of information that Data task automation manager provides is optimized to facilitate initial discovery.</span></span> <span data-ttu-id="956d6-439">詳細な調査のためには、対応するデータ プロジェクトおよびその実行の詳細を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-439">For detailed investigation, you must look at the corresponding data project and its execution details.</span></span>

<span data-ttu-id="956d6-440">現在、次のデータ検証がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="956d6-440">The following data validations are currently supported:</span></span>

- <span data-ttu-id="956d6-441">**ジョブ ステータス** – この検証は、ジョブが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="956d6-441">**Job status** – This validation checks whether the job was successful.</span></span>
- <span data-ttu-id="956d6-442">**バッチ ステータス** - この検証は、バッチが成功したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="956d6-442">**Batch status** – This validation checks whether the batch was successful.</span></span>
- <span data-ttu-id="956d6-443">**メッセージ状態** – テストが統合に関するものである場合、メッセージの状態が検証されます。</span><span class="sxs-lookup"><span data-stu-id="956d6-443">**Message status** – If the test is about integrations, the message status is validated.</span></span>
- <span data-ttu-id="956d6-444">**切り捨て** – 切り捨てが有効になっている場合は、この検証が切り捨てが発生したかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="956d6-444">**Truncation** – If truncation is enabled, this validation checks whether truncation occurred.</span></span>
- <span data-ttu-id="956d6-445">**ステージングのスキップ** – **ステージングのスキップ** がテストで有効になっている場合、ステージングがスキップされたかどうかをこの検証でチェックします。</span><span class="sxs-lookup"><span data-stu-id="956d6-445">**Skip staging** – If **Skip staging** is enabled on a test, this validation checks whether staging was skipped.</span></span>

## <a name="example-1-configuration-management-for-data-projects"></a><span data-ttu-id="956d6-446">例 1: データ プロジェクトの構成管理</span><span class="sxs-lookup"><span data-stu-id="956d6-446">Example 1: Configuration management for data projects</span></span>
<span data-ttu-id="956d6-447">**\<ConfigurationOnly\>** 要素は、データ プロジェクトおよび定期的なスケジュールの構成タスクを作成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="956d6-447">The **\<ConfigurationOnly\>** element can be used to create configuration tasks for data projects and recurring schedules.</span></span>

<span data-ttu-id="956d6-448">この最初の例は、定期的なスケジュールを持たないデータ プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="956d6-448">This first example configures a data project that doesn't have a recurring schedule.</span></span> <span data-ttu-id="956d6-449">2 番目の例には、定期的なスケジュールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="956d6-449">The second example includes a recurring schedule.</span></span> <span data-ttu-id="956d6-450">違いは、**\<Operation\>** 要素の値です。</span><span class="sxs-lookup"><span data-stu-id="956d6-450">The difference is the value of the **\<Operation\>** element.</span></span> <span data-ttu-id="956d6-451">構成タスクのマニフェストは、ソース コントロール下にも保管する必要があります。</span><span class="sxs-lookup"><span data-stu-id="956d6-451">Manifests for configuration tasks should also be kept under source control.</span></span>

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

## <a name="example-2-automated-setup-of-demo-data"></a><span data-ttu-id="956d6-452">例 2: デモ データの自動設定</span><span class="sxs-lookup"><span data-stu-id="956d6-452">Example 2: Automated setup of demo data</span></span>
<span data-ttu-id="956d6-453">次のマニフェストは、デモ データ パッケージが共有アセット ライブラリに格納されている場合の 3 つの法人のデモ データの設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="956d6-453">The following manifest shows the setup of demo data for three legal entities when the demo data packages are stored in the Shared asset library.</span></span>

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

