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
# <a name="process-parameters"></a>プロセス パラメーター

[!include [banner](../includes/banner.md)]

ほとんどの場合、プロセスには、そのプロセスに固有のカスタム パラメーターを格納する必要があります。 たとえば、あるプロセスが日付範囲または顧客番号を必要とする場合があります。 これらのパラメーターを表示および格納するには、独自のユーザー インターフェイス (UI) とカスタム テーブルを作成する必要があります。 タイプにパラメーターがない場合は、このタスクを省略できます。

ユーザーが UI でシリーズを作成すると、**シリーズの作成** ウィザードが複数のフォーム パーツをホストします。各フォームには、関連するパラメーター セットが含まれています。 プロセスのフォーム パーツには、ユーザーがパラメーターを入力するために使用する UI が含まれています。 これらのフォーム パーツは、プロセスの開発者によって作成され、タイプ登録を通じて提供されます。 フォーム パーツは、カスタム パラメーターを初期化、検証、および書き込みできるインターフェイスを実装します。

カスタム パラメーター テーブルには、通常、次の 2 つのタイプのレコードがあります。

- すべての発生のテンプレートとして機能するシリーズにバインドされるテンプレート レコード。
- 発生に固有のレコード。その発生の実行時に使用されるパラメーターが含まれます。 ユーザーは、必要に応じて、各発生に対してパラメーターを上書きできます。

パラメーター テーブルには通常、**ProcessScheduleSeries** テーブルへのひとつの外部キー (**RecId**) と、**ProcessScheduleOccurrence** テーブルへの別の外部キー (**RecId**) があります。 テンプレート レコードには、シリーズ外部キーがありますが、発生への外部キーはありません。 他のすべてのレコードには、両方の外部キーがあります。

これらのパラメーターを維持するために使用されるインタフェースは次のとおりです。

## <a name="processscheduleparametersiinitialize-interface"></a>ProcessScheduleParametersIInitialize インターフェイス

**ProcessScheduleParametersIInitialize** インターフェイスを使用すると、ユーザーがプロセス自動化フレームワークの UI を操作するときにパラメーターを初期化できます。 プロセス固有のパラメーターを表示するウィザード用に作成されたフォーム パーツは、このインターフェイスを実装します。

## <a name="processscheduleparametersivalidate-interface"></a>ProcessScheduleParametersIValidate インターフェイス

**ProcessScheduleParametersIValidate** インターフェイスを使用すると、ユーザーがフォーム パーツに入力したパラメーターを検証できます。

## <a name="processscheduleparametersiwrite-interface"></a>ProcessScheduleParametersIWrite インターフェイス

**ProcessScheduleParametersIWrite** インターフェイスを使用すると、パラメーターをカスタム パラメーター テーブルに書き込むことができます。

## <a name="example"></a>例

次の例では、上記の 3 つのインターフェイスがサンプルのテスト プロセスで使用されています。 この例では、フォーム パーツに *メッセージ* と呼ばれる 1 つの文字列が含まれています。

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

## <a name="processscheduleideleteoccurrence-interface"></a>ProcessScheduleIDeleteOccurrence インターフェイス

ユーザーまたはシステムが発生を削除したことを示すイベントを受け取るための **ProcessScheduleIDeleteOccurrence** インターフェイスを実装します。 その発生に関連付けられているパラメーターを削除する必要があります。

このインターフェイスは、特定のタイプの **SysPlugIn** を介して呼び出されます。 タイプを登録したときに作成されたタイプ名を使用します。

セットベースの削除を実行できるように、Microsoft Azure SQL データベースの一時テーブルが渡されることに注意してください。

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

## <a name="processscheduleideleteseries-interface"></a>ProcessScheduleIDeleteSeries インターフェイス

**ProcessScheduleIDeleteSeries** は、**ProcessScheduleIDeleteOccurrence** に似ています。 このイベントは、シリーズが削除されるたびに呼び出されます。 すべての発生に関して、パラメーター レコードをすべて削除する必要があります。 これらのレコードには、シリーズ テンプレート レコードが含まれています。

セットベースの削除を実行できるように、SQL データベースの一時テーブルが渡されます。

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

## <a name="processscheduleiexplodeoccurrences-interface"></a>ProcessScheduleIExplodeOccurrences インターフェイス

ユーザーが UI を通じて新しいシリーズを作成すると、すべての将来の発生が生成されます。 したがって、シリーズが毎日実行される場合は、プロセス自動化フレームワークによって毎日発生が作成されます。 このアクションは、*シリーズの生成* と呼ばれます。 **ProcessScheduleIExplodeOccurrences** イベントは、シリーズが生成されたときに発生します。 パラメーター テーブル内の各発生にパラメーター レコードを作成するには、シリーズ テンプレート レコードをテンプレートとして使用する必要があります。

最適なパフォーマンスを得るためのパラメーター レコードを作成するために、SQL データベースの一時テーブルが渡されます。

次の例では、パラメーター テーブルに **Type** という名前の 1 つのパラメーターが格納されています。 このパラメーターはプロセス自動化フレームワーク タイプとは関連していませんが、キャッシュ フロー予測に固有です。

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