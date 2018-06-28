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

# <a name="data-task-automation"></a>データ タスクの自動化

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations のデータ タスク自動化は、各種のデータ タスクを簡単に繰り返し、各タスクの結果を検証を可能にします。 データ タスクの自動化は、実装フェーズにあるプロジェクトで非常に便利です。 たとえば、データ プロジェクトの作成およびコンフィギュレーションを自動化することができます。 また、デモ データおよび高品質の構成データ、およびデータ移行に関連する他のタスクなどの、インポート/エクスポート オペレーションの実行を構成およびトリガーすることができます。 また、タスクの結果の検証を使用して、データ エンティティの自動テストを作成することもできます。

> [!IMPORTANT]
> 現時点では、オンプレミス環境ではデータ タスクの自動化はサポートされていません。

データ タスクの自動化のために次の方法をお勧めします。

1. 自動化の恩恵を受けるデータ関連のタスクを特定する。

    実装チームは自分たちの構成管理計画とデータ移行計画をレビューして、自動化のための潜在的なデータ タスクを識別すること、またデータ エンティティのテスト ケースも識別することをお勧めします。

2. タスクを定義します。

    タスクは、XML マニフェストで定義されます。 アプリケーション ライフ サイクルの管理 (ALM) 戦略では、構成管理の一部としてソース管理下のマニフェストを保持することができます。

3. Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリでのデータ タスクの自動化に関連するデータ パッケージを配置します。 また、必要に応じて特定の LCS プロジェクトを使用することもできます。

    データ タスク自動化マネージャは、LCS プロジェクトに関連するサンドボックスまたは実稼動環境からパッケージを使用することができます。

    > [!IMPORTANT]
    > - Finance and Operations のデータ タスク自動化マネージャーを実行するユーザー アカウントは、LCS およびデータ パッケージのマニフェストで参照される LCS プロジェクトにアクセスできる必要があります。
    > - データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合アプリケーション プログラミング インターフェイス (API) を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。 統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。

4. データ タスクを実行し、結果を確認します。

    データ タスク自動化マネージャは、各タスクの成功または失敗の結果を提供します。 また、タスクが失敗した理由に関する見解も提供します。

    > [!IMPORTANT]
    > データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合 API を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。 統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。

次のビデオは、Data Task Automation Manager の初期リリースを紹介する TechTalk の 55 分です。

> [!Video https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4]

## <a name="task-manifest"></a>タスク マニフェスト
タスクは、XML マニフェストで定義する必要があります。 このセクションでは、マニフェストについて説明します。 マニフェストを名前付けしデザインする方法の指針については、このトピックの後半の、「マニフェストのデザインに対するベスト プラクティス」セクションを参照してください。

### <a name="manifest-root"></a>マニフェスト ルート
**\<TestManifest\>** 要素は、マニフェストのルートです。 その他のすべての要素はこの要素の子です。

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

### <a name="shared-setup"></a>共有された設定
**共有セットアップ** セクションは、全般的なタスクのパラメーターとマニフェスト内のすべてのタスクの動作を定義します。

### <a name="data-files"></a>データ ファイル
**\<DataFile\>** 要素は、マニフェスト内のタスクが使用するデータ パッケージとデータ ファイルを定義します。 データ ファイルは、LCS プロジェクトの LCS アセット ライブラリまたは共有アセット ライブラリのいずれかになければなりません。

```
<DataFile ID='SharedSetup' name='Demo data-7.3-100-System and Shared'  assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsHQUS' name='Demo data-7.3-200-Financials-HQUS' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPICH' name='Demo data-7.3-200-Financials-PICH' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPIFB' name='Demo data-7.3-200-Financials-PIFB' assetType='Data package' lcsProjectId=''/>
```

### <a name="data-project-definition"></a>データ プロジェクト定義
**\<JobDefinition\>** 要素は、データ プロジェクト定義を定義します。 マニフェストには複数のジョブ定義があります。

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

### <a name="entity-setup"></a>エンティティ設定
**エンティティ設定** セクションは、マニフェストのタスクが使用するエンティティの特性を定義します。 マニフェスト内のタスクによって使用されるエンティティごとに、1 つずつ複数の定義が存在する可能性があります。

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

### <a name="test-groups"></a>テスト グループ
テスト グループは、マニフェストの関連するタスクを整理するために使用できます。 マニフェストには複数のテスト グループがあります。

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

## <a name="best-practices-for-manifest-design"></a>マニフェスト デザインのためのベスト プラクティス
さまざまな方法でマニフェストを定義することができます。 マニフェストをデザインするときに考慮する必要があるいくつかのポインターを次に示します。

### <a name="granularity"></a>粒度
機能的な意思決定としてマニフェストの粒度を判断することをお勧めします。 チームは、複数のマニフェストを管理するか、または単一のマニフェストの変更を管理するかを決定する必要があります。

- チームが論理的に必要と考える数のマニフェストを使って開始します。 後で、チームが実際にマニフェストの実行を開始すると、予想より少ないマニフェストを使用しており、それらを結合したいと考える場合があります。 この場合、マニフェストをマージすることができます。
- 職務の分離を検討する。 たとえば、デモ データの設定に対して 1 つのマニフェスト、環境の高品質の構成の設定に対して別のマニフェストがある場合があります。 この方法で、チーム メンバーが使用する予定のマニフェストのみを使用することを確認できます。
- LCS へのユーザー アクセスについて考慮してください。 たとえば、大きなおよびグローバルに配分された実装チームは、Finance and Operations の複数のインスタンスまたは複数の LCS プロジェクトを持っている可能性があります。

### <a name="inheritance"></a>継承
マニフェスト スキーマは、マニフェスト内のすべてのタスクに適用される共通要素の継承をサポートします。 タスクは、共通の要素を上書きして一意の動作を定義できます。 **共通設定** セクションの目的は、構成要素の繰り返しを最小限に抑えて、可能な限り要素を再利用することです。 目標は、メンテナンスと可読性を向上させるために、マニフェストを簡潔かつ清潔に保つことです。

### <a name="source-control"></a>ソース管理
実装チームのすべてのメンバーが使用する必要があるマニフェストは、アプリケーション オブジェクト ツリー (AOT) 内のソース コントロールに格納されている必要があります。 この方法は、ソース管理の利点を提供するだけでなく、プロセスがすべてのユーザーに一貫した方法で配布またはマニフェストを提供できるようにします。 また、この方法では、マニフェストを構成に使用する場合、データ管理に関連するデータ プロジェクトの構成管理も可能です。

### <a name="number-of-job-definitions-and-entity-definitions"></a>ジョブ定義とエンティティ定義の数
使用ケースのほとんどの場合、マニフェストで 1 つのジョブ定義で十分であるのは、継承がタスク レベルでの動作を変更するために使用できるからです。 この原則は、エンティティの定義にも適用されます。

## <a name="validations"></a>検証
データ タスク自動化マネージャは、タスクの設定に基づいて検証を実行します。 タスクが失敗した場合は、タスクの完了後に、検証を表示することによって、エラーの原因をすばやく確認できます。 データ タスク自動化マネージャーが提供する情報のレベルは、初期検出を容易にするために最適化されています。 詳細な調査のためには、対応するデータ プロジェクトおよびその実行の詳細を確認する必要があります。

現在、次のデータ検証がサポートされています。

- **ジョブ ステータス** – この検証は、ジョブが成功したかどうかをチェックします。
- **バッチ ステータス** - この検証は、バッチが成功したかどうかをチェックします。
- **メッセージ状態** – テストが統合に関するものである場合、メッセージの状態が検証されます。
- **切り捨て** – 切り捨てが有効になっている場合は、この検証が切り捨てが発生したかどうかをチェックします。
- **ステージングのスキップ** – **ステージングのスキップ** がテストで有効になっている場合、ステージングがスキップされたかどうかをこの検証でチェックします。

## <a name="example-1-configuration-management-for-data-projects"></a>例 1: データ プロジェクトの構成管理
**\<ConfigurationOnly\>** 要素は、データ プロジェクトおよび定期的なスケジュールの構成タスクを作成するために使用できます。

この最初の例は、定期的なスケジュールを持たないデータ プロジェクトを設定します。 2 番目の例には、定期的なスケジュールが含まれます。 違いは、**\<Operation\>** 要素の値です。 構成タスクのマニフェストは、ソース コントロール下にも保管する必要があります。

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

## <a name="example-2-automated-setup-of-demo-data"></a>例 2: デモ データの自動設定
次のマニフェストは、デモ データ パッケージが共有アセット ライブラリに格納されている場合の 3 つの法人のデモ データの設定を示しています。

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

