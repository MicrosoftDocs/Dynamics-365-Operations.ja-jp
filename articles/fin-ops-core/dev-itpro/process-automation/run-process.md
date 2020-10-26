---
title: プロセスの実行
description: このトピックでは、プロセス自動化フレームワークでプロセスを実行する方法について説明します。
author: RyanCCarlson2
manager: AnnBe
ms.date: 09/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-09-10
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e2404f28582dd4b7a7938b2f34e305aeeb67323
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885344"
---
# <a name="run-processes"></a><span data-ttu-id="b5274-103">プロセスの実行</span><span class="sxs-lookup"><span data-stu-id="b5274-103">Run processes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5274-104">プロセス自動化フレームワークで実行するには、プロセスに **ProcessAutomationTask** インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5274-104">To run in the process automation framework, a process must implement the **ProcessAutomationTask** interface.</span></span> <span data-ttu-id="b5274-105">フレームワークは、このインターフェイスを使用して **ProcessScheduleWorkItem** のインスタンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b5274-105">The framework uses this interface to provide an instance of **ProcessScheduleWorkItem**.</span></span> <span data-ttu-id="b5274-106">このインスタンスには、シリーズ、実行中の発生 (該当する場合)、および実行 ID に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5274-106">That instance contains information about the series, the occurrence that is being run (if applicable), and the execution ID.</span></span> <span data-ttu-id="b5274-107">実行する必要があるバッチ タスクを作成し、そのタスクをフレームワークに提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5274-107">You must create the batch task that has to be run, and you must provide the task to the framework.</span></span> <span data-ttu-id="b5274-108">その後、フレームワークは提供されるバッチ ヘッダーとタスクを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5274-108">The framework then creates the batch header and the tasks that are provided.</span></span>

<span data-ttu-id="b5274-109">ポーリングされたプロセスは頻繁に実行される可能性があるため、発生はありません。頻繁に実行されることにより、追跡するよりもはるかに多くの発生が作成されます。代わりに、一意の実行 ID を使用して、ポーリングされたプロセスのすべての実行を追跡します。</span><span class="sxs-lookup"><span data-stu-id="b5274-109">Polled processes don't have occurrences, because they might be run frequently, and those frequent runs will create many more occurrences than you want to track. Instead, you use a unique execution ID to track every run of a polled process.</span></span> <span data-ttu-id="b5274-110">実行 ID は、スケジュールされたプロセスにも割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b5274-110">An execution ID is also assigned to scheduled processes.</span></span>

<span data-ttu-id="b5274-111">**getListOfWorkToBePerformed** メソッドは、実行する必要のある作業があるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b5274-111">The **getListOfWorkToBePerformed** method determines whether there is work that must be done.</span></span> <span data-ttu-id="b5274-112">作業がある場合、このメソッドは **SysOperationServiceController** から継承されたバッチ対応クラスを返します。</span><span class="sxs-lookup"><span data-stu-id="b5274-112">If there is, the method returns a list of batch-enabled classes that inherit from **SysOperationServiceController**.</span></span> <span data-ttu-id="b5274-113">このメソッドは、ポーリング プロセスのコンテキスト内で実行されるため、効率的かつ高速である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5274-113">This method must be efficient and fast, because it's run in the context of the polling process.</span></span> <span data-ttu-id="b5274-114">したがって、このメソッドでは、作業を実行する必要があるかどうかを確認し、実行する必要がある作業に対してバッチ タスクを作成する以外の作業は、行わないでください。</span><span class="sxs-lookup"><span data-stu-id="b5274-114">Therefore, you should not do any work in this method except check whether work must be done and create batch tasks for any work that must be done.</span></span> <span data-ttu-id="b5274-115">空のリストは作業を行う必要がないことを示しているため、メソッドが空のリストを返しても問題はありません。</span><span class="sxs-lookup"><span data-stu-id="b5274-115">It's OK if the method returns an empty list, because an empty list indicates that no work must be done.</span></span> <span data-ttu-id="b5274-116">この場合、プロセス自動化フレームワークはバッチ処理を作成しません。</span><span class="sxs-lookup"><span data-stu-id="b5274-116">In this case, the process automation framework doesn't create any batch processes.</span></span>

<span data-ttu-id="b5274-117">プロセス自動化フレームワークでは、並列処理を実行し、複数のバッチ タスクを必要とするプロセスの一覧をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b5274-117">The process automation framework supports a list for those processes that do parallel processing and that want multiple batch tasks.</span></span> <span data-ttu-id="b5274-118">実行中のプロセスが **RunBaseBatch** を実装する古いプロセスである場合は、リストから返されることはありません。</span><span class="sxs-lookup"><span data-stu-id="b5274-118">If the process that is being run is an older process that implements **RunBaseBatch**, it can't be returned through the list.</span></span> <span data-ttu-id="b5274-119">この場合、2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="b5274-119">In this case, you have two options:</span></span>

- <span data-ttu-id="b5274-120">プロセスを **SysOperationServiceController** に変換します。</span><span class="sxs-lookup"><span data-stu-id="b5274-120">Convert the process to **SysOperationServiceController**.</span></span> <span data-ttu-id="b5274-121">詳細については、[SysOperations フレームワーク](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5274-121">For more information, see [SysOperations Framework](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview).</span></span> <span data-ttu-id="b5274-122">該当する場合は、このオプションを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5274-122">This option is recommended, if it's feasible.</span></span>
- <span data-ttu-id="b5274-123">**SysOperationServiceController** から継承された新しいクラスを使用して、レガシ **RunBaseBatch** クラスをラップします。</span><span class="sxs-lookup"><span data-stu-id="b5274-123">Wrap the legacy **RunBaseBatch** class with a new class that inherits from **SysOperationServiceController**.</span></span> <span data-ttu-id="b5274-124">例については、アプリケーション オブジェクト ツリー (AOT) の **LedgerCovTotalProcessAutomationProcessor** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5274-124">For an example, see **LedgerCovTotalProcessAutomationProcessor** in the Application Object Tree (AOT).</span></span>

<span data-ttu-id="b5274-125">次の例は、**ProcessAutomationTask** インターフェイスの実装を示しています。</span><span class="sxs-lookup"><span data-stu-id="b5274-125">The following example shows an implementation of the **ProcessAutomationTask** interface.</span></span>

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

## <a name="processscheduleworkitem-class"></a><span data-ttu-id="b5274-126">ProcessScheduleWorkItem クラス</span><span class="sxs-lookup"><span data-stu-id="b5274-126">ProcessScheduleWorkItem class</span></span>

<span data-ttu-id="b5274-127">**ProcessScheduleWorkItem** クラスにはさまざまな情報が含まれており、実行する必要があるプロセスを表すように設計されています。</span><span class="sxs-lookup"><span data-stu-id="b5274-127">The **ProcessScheduleWorkItem** class has many pieces of information and is designed to represent a process that must be run.</span></span>

| <span data-ttu-id="b5274-128">メソッド</span><span class="sxs-lookup"><span data-stu-id="b5274-128">Method</span></span> | <span data-ttu-id="b5274-129">説明</span><span class="sxs-lookup"><span data-stu-id="b5274-129">Description</span></span> |
|---|---|
| `public ProcessExecutionId parmExecutionId(ProcessExecutionId _executionId = executionId)` | <span data-ttu-id="b5274-130">実行 ID は、エラーをログに記録するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5274-130">The execution ID is used to log errors.</span></span> <span data-ttu-id="b5274-131">ポーリング プロセスは、実行されるたびに新しい一意の実行 ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="b5274-131">A polled process gets a new, unique execution ID every time that it's run.</span></span> <span data-ttu-id="b5274-132">スケジュールされたプロセスは、発生ごとに 1 回だけ実行されるため、各発生には 1 つの実行 ID しかありません。</span><span class="sxs-lookup"><span data-stu-id="b5274-132">Because scheduled processes are only ever run one time for each occurrence, each occurrence only ever has one execution ID.</span></span> |
| `public RefRecId parmProcessScheduleOccurrenceRecId(RefRecId _scheduleOccurrenceRecId = scheduleOccurrenceRecId)` | <span data-ttu-id="b5274-133">実行中の発生。</span><span class="sxs-lookup"><span data-stu-id="b5274-133">The occurrence that is being run.</span></span> <span data-ttu-id="b5274-134">この方法を使用して、パラメーター テーブルの発生に固有のパラメーター情報を参照します。</span><span class="sxs-lookup"><span data-stu-id="b5274-134">Use this method to reference occurrence-specific parameter information in parameter tables.</span></span> <span data-ttu-id="b5274-135">ポーリングされたプロセスには、発生に対する **RecId** 値はありません。</span><span class="sxs-lookup"><span data-stu-id="b5274-135">Polled processes don't have a **RecId** value for an occurrence.</span></span> |
| `public RefRecId parmProcessScheduleSeriesPatternRecId(RefRecId _scheduleSeriesPatternRecId = scheduleSeriesPatternRecId)` | <span data-ttu-id="b5274-136">プロセスが関連付けられているシリーズ パターン。</span><span class="sxs-lookup"><span data-stu-id="b5274-136">The series pattern that the process is associated with.</span></span> <span data-ttu-id="b5274-137">現在、シリーズは 1 つのパターンしか持つことができません。</span><span class="sxs-lookup"><span data-stu-id="b5274-137">Currently, series can have only one pattern.</span></span> <span data-ttu-id="b5274-138">通常、すべてのパラメーター レコードには、このパターンへの外部キーがあります。</span><span class="sxs-lookup"><span data-stu-id="b5274-138">All parameter records typically have a foreign key to this pattern.</span></span> |
| `public ProcessScheduleProcessType parmProcessScheduleType(ProcessScheduleProcessType _scheduleType = scheduleType)` | <span data-ttu-id="b5274-139">プロセスのスケジュール タイプ: ポーリングまたはスケジュール済。</span><span class="sxs-lookup"><span data-stu-id="b5274-139">The schedule type of the process: polled or scheduled.</span></span> |
| `public ProcessScheduleTypeName parmProcessScheduleTypeName(ProcessScheduleTypeName _scheduleTypeName = scheduleTypeName)` | <span data-ttu-id="b5274-140">**VendPaymentProposal** など、プロセスとシリーズが関連付けられているタイプ名。</span><span class="sxs-lookup"><span data-stu-id="b5274-140">The type name that the process and series are associated with, such as **VendPaymentProposal**.</span></span> <span data-ttu-id="b5274-141">この名前は内部の開発者名であり、ユーザーには表示されません。</span><span class="sxs-lookup"><span data-stu-id="b5274-141">This name is an internal developer name and isn't shown to the user.</span></span> |
| `public List parmLegalEntityList(List _legalEntityList = legalEntityList)` | <span data-ttu-id="b5274-142">プロセスが実行される法人の一覧。</span><span class="sxs-lookup"><span data-stu-id="b5274-142">The list of legal entities that the process will be run against.</span></span> <span data-ttu-id="b5274-143">プロセスがグローバル プロセスの場合、このリストは **null** になります。</span><span class="sxs-lookup"><span data-stu-id="b5274-143">If the process is a global process, this list will be **null**.</span></span> <span data-ttu-id="b5274-144">プロセスが 1 つの会社に対して実行される場合、この一覧には 1 つの会社が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5274-144">If the process is run against a single company, this list will contain a single company.</span></span> <span data-ttu-id="b5274-145">現在、複数の会社はサポートされていませんが、将来サポートされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b5274-145">Multiple companies aren't currently supported, but they might be supported in the future.</span></span> |
| `public Name getName()` | <span data-ttu-id="b5274-146">発生名を返します。</span><span class="sxs-lookup"><span data-stu-id="b5274-146">Returns the occurrence name.</span></span> <span data-ttu-id="b5274-147">タイプをポーリングする場合、このメソッドはシリーズ名を返します。</span><span class="sxs-lookup"><span data-stu-id="b5274-147">If a type is polled, this method returns the series name.</span></span> |
| `public ProcessScheduleSeriesName parmSeriesName(ProcessScheduleSeriesName _seriesName = seriesName)` | <span data-ttu-id="b5274-148">シリーズの名前。</span><span class="sxs-lookup"><span data-stu-id="b5274-148">The name of the series.</span></span> |
| `public Name parmOccurrenceName(Name _occurrenceName = occurrenceName)` | <span data-ttu-id="b5274-149">発生名。</span><span class="sxs-lookup"><span data-stu-id="b5274-149">The occurrence name.</span></span> <span data-ttu-id="b5274-150">プロセスがポーリング プロセスの場合、値は空になります。</span><span class="sxs-lookup"><span data-stu-id="b5274-150">If the process is a polled process, the value will be empty.</span></span> |
| `public List parmTaskList(List _taskList = taskList)` | <span data-ttu-id="b5274-151">プロセス自動化フレームワークによってバッチに追加されるバッチ タスクのリスト。</span><span class="sxs-lookup"><span data-stu-id="b5274-151">The list of batch tasks that the process automation framework should add to the batch.</span></span> <span data-ttu-id="b5274-152">このリストが **null** の場合は、実行必要な作業はなく、バッチでは何も作成されません。</span><span class="sxs-lookup"><span data-stu-id="b5274-152">If this list is **null**, it's assumed that no work must be done, and nothing will be created in a batch.</span></span> |
| `public ProcessScheduleDateTime parmScheduledDateTime(ProcessScheduleDateTime _scheduledDateTime = scheduledDateTime)` | <span data-ttu-id="b5274-153">プロセスの実行がスケジュールされている日時。</span><span class="sxs-lookup"><span data-stu-id="b5274-153">The date and time when the process was scheduled to run.</span></span> <span data-ttu-id="b5274-154">この日時は、実際にプロセスが実行されたときの日時とは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5274-154">This date and time might differ from the actual date and time when the process runs.</span></span> |
| `public UserGroupId parmOwnerId(UserGroupId _ownerId = ownerId)` | <span data-ttu-id="b5274-155">実行中の発生の所有者。</span><span class="sxs-lookup"><span data-stu-id="b5274-155">The owner of the occurrence that is being run.</span></span> |
| `public void initializeFromScheduleWorkItem(ProcessScheduleWorkItem _item)` | <span data-ttu-id="b5274-156">別のインスタンスから **ProcessScheduleWorkItem** のインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b5274-156">Initializes an instance of **ProcessScheduleWorkItem** from another instance.</span></span> |
