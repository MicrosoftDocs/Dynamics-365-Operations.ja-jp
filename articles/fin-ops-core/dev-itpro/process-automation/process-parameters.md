---
title: プロセス パラメーター
description: このトピックでは、プロセス自動化フレームワークでカスタム パラメーターを実装する方法について説明します。
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
ms.openlocfilehash: 0a403cf72cc84adcd33fea92fc602f77f3c7ea2e
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866122"
---
# <a name="process-parameters"></a><span data-ttu-id="8caf1-103">プロセス パラメーター</span><span class="sxs-lookup"><span data-stu-id="8caf1-103">Process parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8caf1-104">ほとんどの場合、プロセスには、そのプロセスに固有のカスタム パラメーターを格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8caf1-104">In most cases, a process must store custom parameters that are specific to its processes.</span></span> <span data-ttu-id="8caf1-105">たとえば、あるプロセスが日付範囲または顧客番号を必要とする場合があります。</span><span class="sxs-lookup"><span data-stu-id="8caf1-105">For example, a process might require a date range or a customer number.</span></span> <span data-ttu-id="8caf1-106">これらのパラメーターを表示および格納するには、独自のユーザー インターフェイス (UI) とカスタム テーブルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8caf1-106">You must create your own user interface (UI) and custom tables to show and store these parameters.</span></span> <span data-ttu-id="8caf1-107">タイプにパラメーターがない場合は、このタスクを省略できます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-107">If a type doesn't have any parameters, you can skip this task.</span></span>

<span data-ttu-id="8caf1-108">ユーザーが UI でシリーズを作成すると、**シリーズの作成** ウィザードが複数のフォーム パーツをホストします。各フォームには、関連するパラメーター セットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8caf1-108">When a user creates a series in the UI, the **Create series** wizard hosts multiple form parts, each of which contains a related set of parameters.</span></span> <span data-ttu-id="8caf1-109">プロセスのフォーム パーツには、ユーザーがパラメーターを入力するために使用する UI が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8caf1-109">The form parts for the process contain the UI that the user uses to enter the parameters.</span></span> <span data-ttu-id="8caf1-110">これらのフォーム パーツは、プロセスの開発者によって作成され、タイプ登録を通じて提供されます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-110">These form parts are built by the developer of the process and provided through type registration.</span></span> <span data-ttu-id="8caf1-111">フォーム パーツは、カスタム パラメーターを初期化、検証、および書き込みできるインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="8caf1-111">A form part implements interfaces that let you initialize, validate, and write the custom parameters.</span></span>

<span data-ttu-id="8caf1-112">カスタム パラメーター テーブルには、通常、次の 2 つのタイプのレコードがあります。</span><span class="sxs-lookup"><span data-stu-id="8caf1-112">The custom parameter tables typically have two types of records:</span></span>

- <span data-ttu-id="8caf1-113">すべての発生のテンプレートとして機能するシリーズにバインドされるテンプレート レコード。</span><span class="sxs-lookup"><span data-stu-id="8caf1-113">A template record that is bound to the series that serves as a template for all occurrences.</span></span>
- <span data-ttu-id="8caf1-114">発生に固有のレコード。その発生の実行時に使用されるパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-114">A record that is specific to an occurrence and contains the parameters that will be used when that occurrence runs.</span></span> <span data-ttu-id="8caf1-115">ユーザーは、必要に応じて、各発生に対してパラメーターを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-115">Users can override the parameters for each occurrence as they require.</span></span>

<span data-ttu-id="8caf1-116">パラメーター テーブルには通常、**ProcessScheduleSeries** テーブルへのひとつの外部キー (**RecId**) と、**ProcessScheduleOccurrence** テーブルへの別の外部キー (**RecId**) があります。</span><span class="sxs-lookup"><span data-stu-id="8caf1-116">Parameter tables typically have one foreign key (**RecId**) to the **ProcessScheduleSeries** table and another foreign key (**RecId**) to the **ProcessScheduleOccurrence** table.</span></span> <span data-ttu-id="8caf1-117">テンプレート レコードには、シリーズ外部キーがありますが、発生への外部キーはありません。</span><span class="sxs-lookup"><span data-stu-id="8caf1-117">The template record has a series foreign key, but it doesn't have a foreign key to the occurrence.</span></span> <span data-ttu-id="8caf1-118">他のすべてのレコードには、両方の外部キーがあります。</span><span class="sxs-lookup"><span data-stu-id="8caf1-118">All other records have both foreign keys.</span></span>

<span data-ttu-id="8caf1-119">これらのパラメーターを維持するために使用されるインタフェースは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8caf1-119">The following interfaces are used to maintain these parameters.</span></span>

## <a name="processscheduleparametersiinitialize-interface"></a><span data-ttu-id="8caf1-120">ProcessScheduleParametersIInitialize インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8caf1-120">ProcessScheduleParametersIInitialize interface</span></span>

<span data-ttu-id="8caf1-121">**ProcessScheduleParametersIInitialize** インターフェイスを使用すると、ユーザーがプロセス自動化フレームワークの UI を操作するときにパラメーターを初期化できます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-121">The **ProcessScheduleParametersIInitialize** interface lets you initialize parameters when the user interacts with the UI of the process automation framework.</span></span> <span data-ttu-id="8caf1-122">プロセス固有のパラメーターを表示するウィザード用に作成されたフォーム パーツは、このインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="8caf1-122">The form part that is built for the wizard that shows process-specific parameters implements this interface.</span></span>

## <a name="processscheduleparametersivalidate-interface"></a><span data-ttu-id="8caf1-123">ProcessScheduleParametersIValidate インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8caf1-123">ProcessScheduleParametersIValidate interface</span></span>

<span data-ttu-id="8caf1-124">**ProcessScheduleParametersIValidate** インターフェイスを使用すると、ユーザーがフォーム パーツに入力したパラメーターを検証できます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-124">The **ProcessScheduleParametersIValidate** interface lets you validate the parameters that the user enters in the form part.</span></span>

## <a name="processscheduleparametersiwrite-interface"></a><span data-ttu-id="8caf1-125">ProcessScheduleParametersIWrite インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8caf1-125">ProcessScheduleParametersIWrite interface</span></span>

<span data-ttu-id="8caf1-126">**ProcessScheduleParametersIWrite** インターフェイスを使用すると、パラメーターをカスタム パラメーター テーブルに書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-126">The **ProcessScheduleParametersIWrite** interface lets you write the parameters to their custom parameter tables.</span></span>

## <a name="example"></a><span data-ttu-id="8caf1-127">例</span><span class="sxs-lookup"><span data-stu-id="8caf1-127">Example</span></span>

<span data-ttu-id="8caf1-128">次の例では、上記の 3 つのインターフェイスがサンプルのテスト プロセスで使用されています。</span><span class="sxs-lookup"><span data-stu-id="8caf1-128">In the following example, the three interfaces that were just described are used for a sample test process.</span></span> <span data-ttu-id="8caf1-129">この例では、フォーム パーツに *メッセージ* と呼ばれる 1 つの文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8caf1-129">In this example, the form part contains a single string that is known as a *message*.</span></span>

```xpp
[Form]
public class ProcessScheduleSampleUptakeFirstFormPart
extends ProcessScheduleParametersFormPart
implements ProcessScheduleParametersIWrite, ProcessScheduleParametersIValidate, ProcessScheduleParametersIInitialize
{

    private ProcessScheduleSchedulingContract schedulingContract;

    public void setSchedulingContract(ProcessScheduleSchedulingContract _schedulingContract)
    {
        schedulingContract = _schedulingContract;
    }

    public void initializeForSeriesCreate()
    {
        str text = strFmt("@ProcessAutomationFramework:ProcessScheduleSeriesTestTypeInitSeriesCreate", curExt());
        ProcessScheduleSampleUptakeParameters_Message.text(text);
    }

    public void initializeForSeriesUpdate()
    {
        ProcessScheduleSampleUptakeParameters parameters =
            ProcessScheduleSampleUptakeParameters::findForProcessScheduleSeries(schedulingContract.processScheduleSeries, true);
        ProcessScheduleSampleUptakeParameters_Message.text(parameters.Message);
    }

    public void initializeForOccurrenceCreate()
    {
        str text = strFmt("@ProcessAutomationFramework:ProcessScheduleSeriesTestTypeInitOccurrenceCreate", curExt());
        ProcessScheduleSampleUptakeParameters_Message.text(text);
    }

    public void initializeForOccurrenceUpdate()
    {
        ProcessScheduleSampleUptakeParameters parameters =
            ProcessScheduleSampleUptakeParameters::findForProcessScheduleOccurrence(schedulingContract.processScheduleOccurrence);
        ProcessScheduleSampleUptakeParameters_Message.text(parameters.Message);
    }

    public void createScheduleSeries(ProcessScheduleSchedulingContract
    _schedulingContract)
    {
        ProcessScheduleSampleUptakeParameters sampleParameters;
        sampleParameters.Message = ProcessScheduleSampleUptakeParameters_Message.valueStr();
        sampleParameters.ProcessScheduleSeries = _schedulingContract.processScheduleSeries.RecId;
        sampleParameters.insert();
    }

    public void updateScheduleSeries(ProcessScheduleSchedulingContract
    _schedulingContract)
    {
        ProcessScheduleSampleUptakeParameters parameters =
            ProcessScheduleSampleUptakeParameters::findForProcessScheduleSeries(_schedulingContract.processScheduleSeries, true);

        if (parameters)
        {
            ttsbegin;
            parameters.Message = ProcessScheduleSampleUptakeParameters_Message.valueStr();
            parameters.update();
            ttscommit;
        }
    }

    public void createScheduledOccurrence(ProcessScheduleSchedulingContract _schedulingContract)
    {
        ProcessScheduleSampleUptakeParameters occurrenceParameters;
        occurrenceParameters.ProcessScheduleOccurrence = _schedulingContract.processScheduleOccurrence.RecId;
        occurrenceParameters.Message = ProcessScheduleSampleUptakeParameters_Message.valueStr();
        occurrenceParameters.insert();
    }

    public void updateScheduledOccurrence(ProcessScheduleSchedulingContract
    _schedulingContract)
    {
        ProcessScheduleSampleUptakeParameters parameters =
            ProcessScheduleSampleUptakeParameters::findForProcessScheduleOccurrence(_schedulingContract.processScheduleOccurrence,
            true);

        ttsbegin;

        parameters.ProcessScheduleSeries = _schedulingContract.processScheduleSeries.RecId;
        parameters.ProcessScheduleOccurrence = _schedulingContract.processScheduleOccurrence.RecId;
        parameters.Message = ProcessScheduleSampleUptakeParameters_Message.valueStr();

        if (parameters.RecId != 0)
        {
            parameters.update();
        }
        else
        {
            parameters.insert();
        }

        ttscommit;
    }

    public boolean validate()
    {
      boolean isValid = true;
      if (ProcessScheduleSampleUptakeParameters_Message.valueStr() == '')
      {
          isValid = checkFailed("@ProcessAutomationFramework:ProcessScheduleSeriesTestTypeMessageWarning");
      }
      return isValid;
    }
}
```

## <a name="processscheduleideleteoccurrence-interface"></a><span data-ttu-id="8caf1-130">ProcessScheduleIDeleteOccurrence インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8caf1-130">ProcessScheduleIDeleteOccurrence interface</span></span>

<span data-ttu-id="8caf1-131">ユーザーまたはシステムが発生を削除したことを示すイベントを受け取るための **ProcessScheduleIDeleteOccurrence** インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="8caf1-131">Implement the **ProcessScheduleIDeleteOccurrence** interface to receive an event that indicates that a user or the system has deleted occurrences.</span></span> <span data-ttu-id="8caf1-132">その発生に関連付けられているパラメーターを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8caf1-132">The parameters that are related to that occurrence should be deleted.</span></span>

<span data-ttu-id="8caf1-133">このインターフェイスは、特定のタイプの **SysPlugIn** を介して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-133">This interface is invoked via **SysPlugIn** for a specific type.</span></span> <span data-ttu-id="8caf1-134">タイプを登録したときに作成されたタイプ名を使用します。</span><span class="sxs-lookup"><span data-stu-id="8caf1-134">Use the type name that was created when the type was registered.</span></span>

<span data-ttu-id="8caf1-135">セットベースの削除を実行できるように、Microsoft Azure SQL データベースの一時テーブルが渡されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8caf1-135">Note that a Microsoft Azure SQL Database temp table is passed in so that you can do set-based deletes.</span></span>

```xpp
using System.ComponentModel.Composition;

// The VendPaymProposalAutomationOccurrenceDeleteProvider class is designed to handle
// deleting the appropriate VendPaymProposalAutomationCriteria records when ProcessScheduleOccurrence records are deleted.
[ExportMetadata(extendedTypeStr(ProcessScheduleTypeName), 'VendPaymProposalAutomation')]
[Export(identifierStr(Dynamics.AX.Application.ProcessScheduleIDeleteOccurrence))]
internal final class VendPaymProposalAutomationOccurrenceDeleteProvider
implements ProcessScheduleIDeleteOccurrence
{
    private ProcessScheduleSeriesOccurrenceTmp occurrencesExplodedTmp;

    [Wrappable(false)]
    public void deleteOccurrences(ProcessScheduleSeriesOccurrenceTmp _occurrencesExplodedTmp)
    {
        this.initialize(_occurrencesExplodedTmp);
        this.deleteVendPaymProposalAutomationCriteria();
    }

    private void initialize(ProcessScheduleSeriesOccurrenceTmp _occurrencesExplodedTmp)
    {
        occurrencesExplodedTmp.linkPhysicalTableInstance(_occurrencesExplodedTmp);
    }

    private void deleteVendPaymProposalAutomationCriteria()
    {
        VendPaymProposalAutomationCriteria automationCriteria;
        automationCriteria.skipDeleteActions(true);
        automationCriteria.skipDataMethods(true);
        automationCriteria.skipAosValidation(true);
        automationCriteria.skipDatabaseLog(true);
        automationCriteria.skipEvents(true);

        delete_from automationCriteria
            exists join occurrencesExplodedTmp
            where automationCriteria.ProcessScheduleOccurrence == occurrencesExplodedTmp.ProcessScheduleOccurrence;
    }
}
```

## <a name="processscheduleideleteseries-interface"></a><span data-ttu-id="8caf1-136">ProcessScheduleIDeleteSeries インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8caf1-136">ProcessScheduleIDeleteSeries interface</span></span>

<span data-ttu-id="8caf1-137">**ProcessScheduleIDeleteSeries** は、**ProcessScheduleIDeleteOccurrence** に似ています。</span><span class="sxs-lookup"><span data-stu-id="8caf1-137">The **ProcessScheduleIDeleteSeries** interface resembles **ProcessScheduleIDeleteOccurrence**.</span></span> <span data-ttu-id="8caf1-138">このイベントは、シリーズが削除されるたびに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-138">The event is invoked whenever a series is deleted.</span></span> <span data-ttu-id="8caf1-139">すべての発生に関して、パラメーター レコードをすべて削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8caf1-139">You should delete all parameter records for all occurrences.</span></span> <span data-ttu-id="8caf1-140">これらのレコードには、シリーズ テンプレート レコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8caf1-140">These records include the series template record.</span></span>

<span data-ttu-id="8caf1-141">セットベースの削除を実行できるように、SQL データベースの一時テーブルが渡されます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-141">A SQL Database temp table is passed in so that you can do set-based deletes.</span></span>

```xpp
using System.ComponentModel.Composition;

// The VendPaymProposalAutomationSeriesDeleteProvider class is designed to handle
// deleting the appropriate VendPaymProposalAutomationCriteria records when ProcessScheduleSeries records are deleted.
[ExportMetadata(extendedTypeStr(ProcessScheduleTypeName), 'VendPaymProposalAutomation')]
[Export(identifierStr(Dynamics.AX.Application.ProcessScheduleIDeleteSeries))]
internal final class VendPaymProposalAutomationSeriesDeleteProvider
implements ProcessScheduleIDeleteSeries
{

    [Wrappable(false)]
    public void deleteSeries(RefRecId _seriesRecId)
    {
        this.deleteVendPaymProposalAutomationCriteria(_seriesRecId);
    }

    private void deleteVendPaymProposalAutomationCriteria(RefRecId _seriesRecId)
    {
        VendPaymProposalAutomationCriteria automationCriteria;
        automationCriteria.skipDeleteActions(true);
        automationCriteria.skipDataMethods(true);
        automationCriteria.skipAosValidation(true);
        automationCriteria.skipDatabaseLog(true);
        automationCriteria.skipEvents(true);

        delete_from automationCriteria
            where automationCriteria.ProcessScheduleSeries == _seriesRecId;
    }
}
```

## <a name="processscheduleiexplodeoccurrences-interface"></a><span data-ttu-id="8caf1-142">ProcessScheduleIExplodeOccurrences インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8caf1-142">ProcessScheduleIExplodeOccurrences interface</span></span>

<span data-ttu-id="8caf1-143">ユーザーが UI を通じて新しいシリーズを作成すると、すべての将来の発生が生成されます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-143">When a user creates a new series through the UI, all the future occurrences are generated.</span></span> <span data-ttu-id="8caf1-144">したがって、シリーズが毎日実行される場合は、プロセス自動化フレームワークによって毎日発生が作成されます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-144">Therefore, if the series runs every day, the process automation framework creates an occurrence for every day.</span></span> <span data-ttu-id="8caf1-145">このアクションは、*シリーズの生成* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-145">This action is known as *generating the series*.</span></span> <span data-ttu-id="8caf1-146">**ProcessScheduleIExplodeOccurrences** イベントは、シリーズが生成されたときに発生します。</span><span class="sxs-lookup"><span data-stu-id="8caf1-146">The **ProcessScheduleIExplodeOccurrences** event is fired when the series is generated.</span></span> <span data-ttu-id="8caf1-147">パラメーター テーブル内の各発生にパラメーター レコードを作成するには、シリーズ テンプレート レコードをテンプレートとして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8caf1-147">The series template record should be used as a template to create parameter records for each occurrence in the parameter tables.</span></span>

<span data-ttu-id="8caf1-148">最適なパフォーマンスを得るためのパラメーター レコードを作成するために、SQL データベースの一時テーブルが渡されます。</span><span class="sxs-lookup"><span data-stu-id="8caf1-148">A SQL Database temp table is passed in so that you can do set-based creation of parameter records for optimal performance.</span></span>

<span data-ttu-id="8caf1-149">次の例では、パラメーター テーブルに **Type** という名前の 1 つのパラメーターが格納されています。</span><span class="sxs-lookup"><span data-stu-id="8caf1-149">In the following example, a parameter table stores a single parameter that is named **Type**.</span></span> <span data-ttu-id="8caf1-150">このパラメーターはプロセス自動化フレームワーク タイプとは関連していませんが、キャッシュ フロー予測に固有です。</span><span class="sxs-lookup"><span data-stu-id="8caf1-150">This parameter isn't related to the process automation framework type but is specific to cash flow forecasting.</span></span>

```xpp
using System.ComponentModel.Composition;

// Provider for cash flow forecast automation generate occurrences.
[Export(identifierStr(Dynamics.AX.Application.ProcessScheduleIExplodeOccurrences))]
[ExportMetadata(extendedTypeStr(ProcessScheduleTypeName), 'LedgerCovTotalProcessAutomation')]
internal final class LedgerCovTotalProcessAutomationExplodeOccurrencesProvider
implements ProcessScheduleIExplodeOccurrences
{
    private void new()
    {
    }

    [Wrappable(false)]
    public void explodeOccurrences(ProcessScheduleSeriesOccurrenceTmp _occurrencesExplodedTmp)
    {
        LedgerCovTotalProcessAutomationSchedulingParameters parameters;
        LedgerCovTotalProcessAutomationSchedulingParameters
        parametersSeriesRecord;

        insert_recordset parameters
        (
            Type,
            ProcessScheduleSeries,
            ProcessScheduleOccurrence
        )

        select Type, ProcessScheduleSeries from parametersSeriesRecord
            where parametersSeriesRecord.ProcessScheduleOccurrence == 0
            join ProcessScheduleOccurrence from _occurrencesExplodedTmp
            where _occurrencesExplodedTmp.ProcessScheduleSeries == parametersSeriesRecord.ProcessScheduleSeries
                && _occurrencesExplodedTmp.TypeName == LedgerCovTotalProcessAutomationConstants::RegisteredTypeName;
    }
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]