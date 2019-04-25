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
# <a name="data-task-automation"></a>データ タスクの自動化

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations のデータ タスクの自動化により、さまざまな種類のデータ タスクを簡単に繰り返し、各タスクの結果を検証することができます。 データ タスクの自動化は、実装フェーズにあるプロジェクトで非常に便利です。 たとえば、データ プロジェクトの作成およびコンフィギュレーションを自動化することができます。 また、デモ データおよび高品質の構成データ、およびデータ移行に関連する他のタスクなどの、インポート/エクスポート オペレーションの実行を構成およびトリガーすることができます。 また、タスクの結果の検証を使用して、データ エンティティの自動テストを作成することもできます。

> [!IMPORTANT]
> 現時点では、オンプレミス環境ではデータ タスクの自動化はサポートされていません。

データ タスクの自動化のために次の方法をお勧めします。

1. 自動化の恩恵を受けるデータ関連のタスクを特定する。

    実装チームは自分たちの構成管理計画とデータ移行計画をレビューして、自動化のための潜在的なデータ タスクを識別すること、またデータ エンティティのテスト ケースも識別することをお勧めします。

2. タスクを定義します。

    タスクは、XML マニフェストで定義されます。 アプリケーション ライフ サイクルの管理 (ALM) 戦略では、構成管理の一部としてソース管理下のマニフェストを保持することができます。

3. Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリに、データ タスクの自動化に関連するデータ パッケージを配置します。 また、必要に応じて特定の LCS プロジェクトを使用することもできます。

    データ タスク自動化マネージャは、LCS プロジェクトに関連するサンドボックスまたは実稼動環境からパッケージを使用することができます。

    > [!IMPORTANT]
    > - Finance and Operations のデータ タスク自動化マネージャーを実行するユーザー アカウントは、LCS およびデータ パッケージのマニフェストで参照される LCS プロジェクトにアクセスできる必要があります。
    > - データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合アプリケーション プログラミング インターフェイス (API) を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。 統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。

4. データ タスクを実行し、結果を確認します。

    データ タスク自動化マネージャは、各タスクの成功または失敗の結果を提供します。 また、タスクが失敗した理由に関する見解も提供します。

    > [!IMPORTANT]
    > データ タスクの自動化はクラウドのすべての環境で実行できますが、実稼動環境の統合 API を使用してすべてのインポート/エクスポート タスクを実行しないことを強くお勧めいたします。 統合 API を含むデータ タスクの自動化は、自動テストにのみ使用する必要があります。

次のビデオは、Data Task Automation Manager の初期リリースを紹介する TechTalk の 55 分です。[タスク自動化フレームワーク](https://academylive.blob.core.windows.net/media/PAL/TechTalks-EnterpriseEdition/TaskAutomationFrameworkForDataManagement-DYN447PAL2.mp4)。

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

| 要素          | 要素の基数 | 属性 | 属性の説明                                     |
|------------------|---------------------|------------|-----------------------------------------------------------|
| \<TestManifest\> | 1..1                | 名前       | *名前*はマニフェストの目的を識別するのに役立ちます。 |

### <a name="shared-setup"></a>共有された設定
**共有セットアップ** セクションは、全般的なタスクのパラメーターとマニフェスト内のすべてのタスクの動作を定義します。

| 親要素   | 要素         | 要素の基数 | 属性 | 属性の説明            |
|------------------|-----------------|---------------------|------------|----------------------------------|
| \<TestManifest\> | \<SharedSetup\> | 1..1                | \-         | この要素には属性はありません。 |

### <a name="data-files"></a>データ ファイル
**\<DataFile\>** 要素は、マニフェスト内のタスクが使用するデータ パッケージとデータ ファイルを定義します。 データ ファイルは、LCS プロジェクトの LCS アセット ライブラリまたは共有アセット ライブラリのいずれかになければなりません。

```
<DataFile ID='SharedSetup' name='Demo data-7.3-100-System and Shared'  assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsHQUS' name='Demo data-7.3-200-Financials-HQUS' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPICH' name='Demo data-7.3-200-Financials-PICH' assetType='Data package' lcsProjectId=''/>
<DataFile ID='FinancialsPIFB' name='Demo data-7.3-200-Financials-PIFB' assetType='Data package' lcsProjectId=''/>
```

| 親要素  | 要素      | 要素の基数 | 属性   | 属性の説明 |
|-----------------|--------------|---------------------|--------------|-----------------------|
| \<SharedSetup\> | \<DataFile\> | 1..n                | \-           | \- |
|                 | \<DataFile\> | \-                  | ID           | |
|                 | \<DataFile\> | \-                  | 名前         | データ ファイルを表す資産の名前。 |
|                 | \<DataFile\> | \-                  | assetType    | データ ファイルを格納する LCS 資産ライブラリでの資産タイプ。 これは、LCS アセット ライブラリで示されたように、アセット タイプの名前です。 |
|                 | \<DataFile\> | \-                  | lcsProjectId | その資産ライブラリで LCS プロジェクトにはデータ ファイルがあります。 プロジェクト ID が " として指定されている場合は、共有アセット ライブラリを示します。 |

### <a name="data-project-definition"></a>データ プロジェクト定義
**\<JobDefinition\>** 要素は、データ プロジェクト定義を定義します。 マニフェストには複数のジョブ定義があります。

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

| 親要素    | 要素                          | 要素の基数 | 属性 | 説明 |
|-------------------|----------------------------------|---------------------|-----------|-------------|
| \<SharedSetup\>   | \<JobDefinition\>                | 1..n                | ID        | タスクでジョブ定義 ID を使用してデータ プロジェクトで使用する定義を参照できます。 |
| \<JobDefinition\> | [\<操作\>]                    | 1..1                | \-        | 実行される操作は、次の値によって指定されます。 <br> - インポート <br> - エクスポート |
|                   | \<切り詰め\>                     | 1..1                | \-        | これは、はいまたはいいえの値を持つブール値フィールドです。 これは操作が*インポート*に設定されている場合にのみ適用されます。 |
|                   | \<モード\>                         | 1..1                | \-        | モードでは、操作を実行する必要があるメソッドを指定します。 使用可能な値は次のとおりです。<br>- 非同期インポート <br>- 非同期エクスポート <br>- 定期的に実行するバッチ: エンキュー API を使用します。 デキュー API には現在対応していません。 パッケージAPIは、エクスポートとインポートの両方に対応しています。|
|                   | \<ConfigurationOnly\>            | 1..1                | \-        | これは、はいまたはいいえの値を持つブール値フィールドです。 タスクがデータ プロジェクトをコンフィギュレーションするのみで、指定された操作を実行しない場合は、はいに設定する必要があります。 |
|                   | \<BatchFrequencyInMinutes\>      | 1..1                | \-        | バッチがスケジュール設定される頻度を指定します。 これはモードが*定期実行されるバッチ*に設定されている場合にのみ適用されます。 |
|                   | \<NumberOfTimesToRunBatch\>      | 1..1                | \-        | これは、スケジュールされているバッチを実行する回数の制限を設定するために使用されます。 これはモードが*定期実行されるバッチ*に設定されている場合にのみ適用されます。 |
|                   | \<UploadFrequencyInSeconds\>     | 1..1                | \-        | これは、インポートする定期バッチ ジョブにファイルをアップロードする頻度を制御するために使用します。 これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。 これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*に設定されている場合にのみ適用されます。 |
|                   | \<TotalNumberOfTimesToUpload\>   | 1..1                |           | これはファイルを繰り返しバッチにアップロードする総回数を制御します。 これは、非実稼働環境での定期的な統合の自動テストに対してのみ使用する必要があります。 これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*に設定されている場合にのみ適用されます。 |
|                   | \<SupportedDataSoureType\>       | 1..1                |           | ファイルが定期的なバッチまたはパッケージに送信中であるかどうかを指定するために使用する必要があります。 これはモードが「定期実行されるバッチ」に設定されている場合にのみ適用されます。 |
|                   | \<ProcessMessagesInOrder\>       | 1..1                |           | これは、はいまたはいいえの値を持つブール値フィールドです。 これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*の場合にのみ適用されます。 |
|                   | \<PreventUploadWhenZeroRecords\> | 1..1                |           | これは、はいまたはいいえの値を持つブール値フィールドです。 これはモードが*定期実行されるバッチ*に設定されており、操作が*エクスポート*の場合にのみ適用されます。 |
|                   | \<UseCompanyFromMessage\>        | 1..1                |           | これははい、またはいいえに設定できるブール値フィールドです。 これはモードが*定期実行されるバッチ*に設定されており、操作が*インポート*の場合にのみ適用されます。 |
|                   | \<LegalEntity\>                  | 1..1                |           | これをは、インポート/エクスポート ジョブを実行する必要がある法人を指定するために使用されます。 |
|                   | \<ConfigurationOnly\>            | 1..1                |           | これを使用して、データのプロジェクトおよび構成する定期的なスケジュールを作成できます。 インポートまたはエクスポートの操作は実行されません。 ただし、データ プロジェクトを正しく設定するには、操作とモードを指定する必要があります。 これは、はいまたはいいえを取るブール値フィールドです。 |
|                   | \<PackageAPIExecute\>            | 1..1                |           | このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。 これは、"true" または "false" を取るブール値フィールドです。 |
|                   | \<PackageAPIOverwrite\>            | 1..1                |           | このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。 これは、"true" または "false" を取るブール値フィールドです。 |
|                   | \<PackageAPIReexecute\>            | 1..1                |           | このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。 これは、"true" または "false" を取るブール値フィールドです。 |
|                   | \<DefinitionGroupID\>            | 1..1                |           | このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。 これは文字列フィールドです。 |
|                   | \<PackageName\>            | 1..1                |           | このパラメーターを理解するためにパッケージ API ドキュメントを参照してください。 これは文字列フィールドです。 |

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

| 親要素         | 要素                              | 要素の基数 | 属性         | 説明 |
|------------------------|--------------------------------------|---------------------|-------------------|-------------|
| \<SharedSetup\>        | \<EntitySetup\>                      | 1..n                | ID                | タスクが使用するエンティティ定義を参照するために使用される ID。 |
| \<EntitySetup\>        | \<エンティティ\>                           | 1..1                | 名前              | エンティティ要素は、エンティティの名前で識別されます。 ただし、簡単なマニフェスト定義を容易にするために、この要素は \* ワイルド カードとしてもサポートしています。これは、すべてのエンティティがタスクで使用されていることを意味しています。 これは、タスク内の何百ものエンティティを持つデータ パッケージを使用する場合に非常に便利です。 |
| \<エンティティ\>             | \<SourceDataFormatName\>             | 1..1                | \-                | これはエンティティに使用されるファイル形式です。 |
|                        | \<ChangeTracking\>                   | 1..1                | \-                | これは、はいまたはいいえの値を持つブール値フィールドです。 エンティティ全体で変更追跡を有効または無効にします。 |
|                        | \<PublishToBYOD\>                    | 1..1                | \-                | これは、はいまたはいいえの値を持つブール値フィールドです。 |
|                        | \<DefaultRefreshType\>               | 1..1                | \-                | これにより、エンティティの既定の更新頻度が設定されます。 使用可能な値は*増分プッシュのみ*または*フル プッシュ*です。 |
|                        | \<ExcelWorkSheetName\>               | 1..1                | \-                | これはエンティティに使用するワークシートを指定するために使用されます。 |
|                        | \<SelectFields\>                     | 1..1                | \-                | これは、エクスポート操作のテンプレートに含まれるフィールドを指定するために使用できます。 |
|                        | \<SetBasedProcessing\>               | 1..1                | \-                | これは、はいまたはいいえの値を持つブール値フィールドです。 エンティティのセット ベースのプロセスを有効または無効にするのに使用されます。 |
|                        | \<FailBatchOnErrorForExecutionUnit\> | 1..1                | \-                | これは、はいまたはいいえの値を持つブール値フィールドです。 エンティティの実行単位レベルでエラーを有効または無効にするのに使用されます。 |
|                        | \<FailBatchOnErrorForLevel\>         | 1..1                | \-                | これは、はいまたはいいえの値を持つブール値フィールドです。 エンティティの実行レベルでエラーを有効または無効にするのに使用されます。 |
|                        | \<DisableEntity\>                    | 1..1                | \-                | これは、はいまたはいいえの値を持つブール値フィールドです。 データ プロジェクトでエンティティを有効化または無効化するのに使用されます。 |
|                        | \<SkipStaging\>                      | 1..1                | \-                | これは、はいまたはいいえの値を持つブール値フィールドです。 エクスポート中にエンティティのステージング テーブルをスキップするのに使用されます。 |
|                        | \<ParallelProcessing\>               | 1..1                | \-                | これは、エンティティに対して設定された並列処理を定義するために使用されます。 タスクの始まりで既に終了する場合、タスクはこれらの設定を削除し、その実行の終わりに作成された設定を削除します。 |
| \<ParallelProcessing\> | \<しきい値\>                        | 1..1                | \-                | 並列処理のルールのしきい値を指定します。 |
|                        | \<TaskCount\>                        | 1..1                | \-                | これは、並列処理に使用される並列タスクの数を指定するために使用されます。 |
| \<エンティティ\>             | \<MappingDetail\>                    | 0..n                | \-                | *自動生成*、*自動既定値*およびエンティティのマッピングで他の設定を構成できます。 |
|                        | \<MappingDetail\>                    | \-                  | StagingFieldName  | この属性は、設定を指定するエンティティ列を識別するために使用されます。 |
|                        | \<MappingDetail\>                    | \-                  | AutoGenerate      | これは、自動生成オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。 |
|                        | \<MappingDetail\>                    | \-                  | AutoDefault       | これは、自動既定オプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。 |
|                        | \<MappingDetail\>                    | \-                  | DefaultValue      | これは、自動既定設定が有効な場合に使用される既定値です。 |
|                        | \<MappingDetail\>                    | \-                  | IgnoreBlankValues | これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。 |
|                        | \<MappingDetail\>                    | \-                  | TextQualifier     | これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。 |
|                        | \<MappingDetail\>                    | \-                  | UseEnumLabel      | これは、このオプションを有効または無効にするための、はいまたはいいえの値を持つブール値フィールドです。 |

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

| 親要素   | 要素           | 要素の基数 | 属性  | 説明 |
|------------------|-------------------|---------------------|-------------|-------------|
| \<TestManifest\> | \<TestGroup\>     | 1..n                | \-          | \- |
|                  | \<TestGroup\>     | 1..1                | 氏名        | これは、グループの機能上の理由を特定するための名前です。 |
| \<TestGroup\>    | \<TestCase\>      | 1..n                | \-          | タスクは、この要素で定義されます。 タスクでは、タスク パラメータおよびタスク動作を継承する共有設定を参照できます。 タスクでは、パラメータと動作もそのレベルで上書きできるため、マニフェストの管理を単純にできます。 |
|                  | \<TestCase\>      | \-                  | 肩書き       | これはタスクのタイトルです。 |
|                  | \<TestCase\>      | \-                  | ID          | これはタスクの ID です。 これは英数字で、最大文字数制限は 10 です。 |
|                  | \<TestCase\>      | \-                  | RepeatCount | これは、将来の機能のプレース ホルダーです。 ただし、これは値 *1* で指定する必要があります。 |
|                  | \<TestCase\>      | \-                  | TraceParser | これは、将来の機能のプレース ホルダーです。 ただし、これは値*オフ*で指定する必要があります。 |
|                  | \<TestCase\>      | \-                  | タイムアウト     | これは、タスク自動化マネージャーによってタスクがモニターされる最大期間です。 指定したタイムアウトを超えてタスクがまだアクティブな場合、マネージャーはマニフェスト内の次のタスクに進みます。 |
| \<TestCase\>     | \<DataFile\>      | 1..n                | \-          | この要素は、タスクで使用されるファイル、またはデータのプロジェクトを定義するために使用されます。 これは、既に宣言されたファイル、またはマニフェストの共有セクションのデータ パッケージを参照できます。 タスクでは、反復バッチ インポート シナリオでのみ指定された複数のデータ ファイルを使用することができます。 他のシナリオでは、1 つ以上のファイルが指定されていても、最初のファイルがタスクによって使用されるファイルです。 |
|                  | \<JobDefinition\> | 1..1                | \-          | この要素は、タスクで使用されるデータのプロジェクトを定義するために使用されます。 これは、共有セクション内のすでに宣言されているマニフェストのジョブ定義を参照できます。 タスクでは、共有設定で定義されている値よりも新しい値にジョブ定義の要素を上書きできます。 |
|                  | \<EntitySetup\>   | 1..1                | \-          | この要素は、タスクで使用されるエンティティのエンティティ セットアップを定義するために使用されます。 これは、マニフェストの共有のセクションで既に宣言されたエンティティ セットアップを参照できます。 タスクでは、共有設定で定義されている値よりも新しい値にエンティティ設定の要素を上書きできます。 |

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
