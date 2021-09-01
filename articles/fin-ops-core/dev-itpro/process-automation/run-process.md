---
title: プロセスの実行
description: このトピックでは、プロセス自動化フレームワークでプロセスを実行する方法について説明します。
author: RyanCCarlson2
ms.date: 09/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-09-10
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3da334f41da45ea3cfdc7fa95ebec5c26208dc64c865c5d367df7cce5741918
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765070"
---
# <a name="run-processes"></a>プロセスの実行

[!include [banner](../includes/banner.md)]

プロセス自動化フレームワークで実行するには、プロセスに **ProcessAutomationTask** インターフェイスを実装する必要があります。 フレームワークは、このインターフェイスを使用して **ProcessScheduleWorkItem** のインスタンスを提供します。 このインスタンスには、シリーズ、実行中の発生 (該当する場合)、および実行 ID に関する情報が含まれています。 実行する必要があるバッチ タスクを作成し、そのタスクをフレームワークに提供する必要があります。 その後、フレームワークは提供されるバッチ ヘッダーとタスクを作成します。

ポーリングされたプロセスは頻繁に実行される可能性があるため、発生はありません。頻繁に実行されることにより、追跡するよりもはるかに多くの発生が作成されます。代わりに、一意の実行 ID を使用して、ポーリングされたプロセスのすべての実行を追跡します。 実行 ID は、スケジュールされたプロセスにも割り当てられます。

**getListOfWorkToBePerformed** メソッドは、実行する必要のある作業があるかどうかを決定します。 作業がある場合、このメソッドは **SysOperationServiceController** から継承されたバッチ対応クラスを返します。 このメソッドは、ポーリング プロセスのコンテキスト内で実行されるため、効率的かつ高速である必要があります。 したがって、このメソッドでは、作業を実行する必要があるかどうかを確認し、実行する必要がある作業に対してバッチ タスクを作成する以外の作業は、行わないでください。 空のリストは作業を行う必要がないことを示しているため、メソッドが空のリストを返しても問題はありません。 この場合、プロセス自動化フレームワークはバッチ処理を作成しません。

プロセス自動化フレームワークでは、並列処理を実行し、複数のバッチ タスクを必要とするプロセスの一覧をサポートしています。 実行中のプロセスが **RunBaseBatch** を実装する古いプロセスである場合は、リストから返されることはありません。 この場合、2 つのオプションがあります。

- プロセスを **SysOperationServiceController** に変換します。 詳細については、[SysOperations フレームワーク](/dynamicsax-2012/developer/sysoperation-framework-overview)を参照してください。 該当する場合は、このオプションを使用することをお勧めします。
- **SysOperationServiceController** から継承された新しいクラスを使用して、レガシ **RunBaseBatch** クラスをラップします。 例については、アプリケーション オブジェクト ツリー (AOT) の **LedgerCovTotalProcessAutomationProcessor** を参照してください。

次の例は、**ProcessAutomationTask** インターフェイスの実装を示しています。

```xpp
using System.ComponentModel.Composition;

// The test class to test the process automation task engine.
[ExportMetadataAttribute(classStr(ProcessAutomationTask), classStr(ProcessAutomationTaskTestImplementation))]
[ExportAttribute(identifierStr('Microsoft.Dynamics.AX.Application.ProcessAutomationTask'))]
internal final class ProcessAutomationTaskTestImplementation extends ProcessAutomationTask
{

    protected boolean isProcessAutomationEnabledForThisTask()
    {
        return true;
    }

    protected List getListOfWorkToBePerformed()
    {
        ProcessScheduleWorkItem scheduleWorkItemToExecute = this.parmProcessScheduleWorkItem();
        List taskList = new List(Types::Class);
        ProcessAutomationTestProcess testProcess = ProcessAutomationTestProcess::construct(scheduleWorkItemToExecute);
        taskList.addEnd(testProcess);
        return taskList;
    }

    // Gets and sets the batch job caption that will be used by the batch job scheduled to run this process.
    // Returns the batch caption that will be used for the batch job that will perform the task.
    protected BatchCaption batchJobCaption()
    {
        return "@ProcessAutomationFramework:ProcessScheduleExplodeProcessLabel";
    }
}
```

## <a name="processscheduleworkitem-class"></a>ProcessScheduleWorkItem クラス

**ProcessScheduleWorkItem** クラスにはさまざまな情報が含まれており、実行する必要があるプロセスを表すように設計されています。

| メソッド | 説明 |
|---|---|
| `public ProcessExecutionId parmExecutionId(ProcessExecutionId _executionId = executionId)` | 実行 ID は、エラーをログに記録するために使用されます。 ポーリング プロセスは、実行されるたびに新しい一意の実行 ID を取得します。 スケジュールされたプロセスは、発生ごとに 1 回だけ実行されるため、各発生には 1 つの実行 ID しかありません。 |
| `public RefRecId parmProcessScheduleOccurrenceRecId(RefRecId _scheduleOccurrenceRecId = scheduleOccurrenceRecId)` | 実行中の発生。 この方法を使用して、パラメーター テーブルの発生に固有のパラメーター情報を参照します。 ポーリングされたプロセスには、発生に対する **RecId** 値はありません。 |
| `public RefRecId parmProcessScheduleSeriesPatternRecId(RefRecId _scheduleSeriesPatternRecId = scheduleSeriesPatternRecId)` | プロセスが関連付けられているシリーズ パターン。 現在、シリーズは 1 つのパターンしか持つことができません。 通常、すべてのパラメーター レコードには、このパターンへの外部キーがあります。 |
| `public ProcessScheduleProcessType parmProcessScheduleType(ProcessScheduleProcessType _scheduleType = scheduleType)` | プロセスのスケジュール タイプ: ポーリングまたはスケジュール済。 |
| `public ProcessScheduleTypeName parmProcessScheduleTypeName(ProcessScheduleTypeName _scheduleTypeName = scheduleTypeName)` | **VendPaymentProposal** など、プロセスとシリーズが関連付けられているタイプ名。 この名前は内部の開発者名であり、ユーザーには表示されません。 |
| `public List parmLegalEntityList(List _legalEntityList = legalEntityList)` | プロセスが実行される法人の一覧。 プロセスがグローバル プロセスの場合、このリストは **null** になります。 プロセスが 1 つの会社に対して実行される場合、この一覧には 1 つの会社が含まれます。 現在、複数の会社はサポートされていませんが、将来サポートされる可能性があります。 |
| `public Name getName()` | 発生名を返します。 タイプをポーリングする場合、このメソッドはシリーズ名を返します。 |
| `public ProcessScheduleSeriesName parmSeriesName(ProcessScheduleSeriesName _seriesName = seriesName)` | シリーズの名前。 |
| `public Name parmOccurrenceName(Name _occurrenceName = occurrenceName)` | 発生名。 プロセスがポーリング プロセスの場合、値は空になります。 |
| `public List parmTaskList(List _taskList = taskList)` | プロセス自動化フレームワークによってバッチに追加されるバッチ タスクのリスト。 このリストが **null** の場合は、実行必要な作業はなく、バッチでは何も作成されません。 |
| `public ProcessScheduleDateTime parmScheduledDateTime(ProcessScheduleDateTime _scheduledDateTime = scheduledDateTime)` | プロセスの実行がスケジュールされている日時。 この日時は、実際にプロセスが実行されたときの日時とは異なる場合があります。 |
| `public UserGroupId parmOwnerId(UserGroupId _ownerId = ownerId)` | 実行中の発生の所有者。 |
| `public void initializeFromScheduleWorkItem(ProcessScheduleWorkItem _item)` | 別のインスタンスから **ProcessScheduleWorkItem** のインスタンスを初期化します。 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]