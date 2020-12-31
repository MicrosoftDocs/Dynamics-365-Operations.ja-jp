---
title: シリーズ登録
description: このトピックでは、プロセス自動化フレームワークでシリーズを作成する方法について説明します。
author: RyanCCarlson2
manager: AnnBe
ms.date: 09/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-09-10
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34c5b90c97959d090f30d757ffa98a033be3b305
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679226"
---
# <a name="series-registration"></a>シリーズ登録

[!include [banner](../includes/banner.md)]

すべてのプロセスには、*シリーズ* が必要です。 プロセス自動化のシリーズの概念は、Microsoft Outlook でのミーティング シリーズの概念に似ています。 ただし、プロセス自動化のシリーズは、一連のスケジュールされたプロセスの実行です。 ほとんどのスケジュールされたプロセス タイプでは、ユーザーがユーザー インターフェイス (UI) にシリーズを作成し、シリーズ登録を実装する必要がありません。 ただし、実装中のプロセスが一連のスケジュールである場合は、このタスクを省略できます。

バックグラウンド プロセスは、ユーザー操作を許可しない内部プロセスとなる傾向があるため、通常シリーズ登録を使用してコードを介してシリーズを作成します。 コードを介してシリーズを作成するには、**ProcessScheduleISeriesRegistration** インターフェイスを実装します。 このインターフェイスには、**ProcessScheduleSeriesRegistrationItem** のインスタンスを返す単一のメソッドがあります。

プロセス自動化フレームワークは、システム管理者が既定のポーリング間隔とバックグラウンド プロセスの単位を変更できるようにします。

ここでは、プロセス自動化フレームワークのテストに使用するテスト シリーズの例を示します。

```xpp
using System.ComponentModel.Composition;
// Implements the ProcessScheduleISeriesRegistration to register the vendor invoice batch posting task 'Series' with the Process Automation.
[Export(identifierStr(Dynamics.AX.Application.ProcessScheduleISeriesRegistration))]
[ExportMetadata(classStr(ProcessScheduleISeriesRegistration), classStr(VendInvoicePostProcessScheduleSeriesRegistration))]
internal final class VendInvoicePostProcessScheduleSeriesRegistration implements ProcessScheduleISeriesRegistration
{

    [Hookable(false)]
    public ProcessScheduleSeriesRegistrationItem
    getProcessScheduleSeriesRegistrationItem()
    {
        ProcessScheduleSeriesRegistrationItem
        processScheduleSeriesRegistrationItem =
        ProcessScheduleSeriesRegistrationItem::construct();
        processScheduleSeriesRegistrationItem.parmDescription("@AccountsPayable:VendInvoicePostTaskFeatureSummary");
        processScheduleSeriesRegistrationItem.parmOwnerId(curUserId());
        processScheduleSeriesRegistrationItem.parmProcessScheduleSeriesPatternList(this.getSeriesPatternList());
        processScheduleSeriesRegistrationItem.parmSeriesName("@AccountsPayable:VendInvoicePostTaskFeatureLabel");
        processScheduleSeriesRegistrationItem.parmTypeName(VendInvoicePostTaskConstants::VendorInvoiceBatchPosting);
        return processScheduleSeriesRegistrationItem;
        }

    private List getSeriesPatternList()
    {
        ProcessScheduleSeriesPatternItem processScheduleSeriesPatternItem =
        ProcessScheduleSeriesPatternItem::construct();
        processScheduleSeriesPatternItem.parmUnit(ProcessScheduleUnit::Minute);
        processScheduleSeriesPatternItem.parmPollingInterval(VendParameters::pollingIntervalMinutes());
        List list = new List(Types::Class);
        list.addEnd(processScheduleSeriesPatternItem);
        return list;
    }
}
```

## <a name="processscheduleseriesregistrationitem-class"></a>ProcessScheduleSeriesRegistrationItem クラス

| メソッド | 説明 |
|---|---|
| `public ProcessScheduleTypeName parmTypeName(ProcessScheduleTypeName _typeName = typeName)` | タイプの名前。 |
| `public ProcessScheduleSeriesName parmSeriesName(ProcessScheduleSeriesName _SeriesName = seriesName)` | シリーズの名前。 名前からシリーズの目的がよく理解できるように、説明的なものにしてください。 |
| `public Description parmDescription(Description _description = description)` | シリーズの説明。 |
| `public UserGroupId parmOwnerId(UserGroupId _ownerId = ownerId)` | シリーズ所有者のユーザー ID。 |
| `public List parmProcessScheduleSeriesPatternList(List _seriesPatternList = seriesPatternList)` | シリーズのパターン一覧。 現時点では、各シリーズには 1 つのパターンしかサポートされていません。 ただし、この制限は将来変更される可能性があります。 **ProcessScheduleSeriesPatternItem** クラスのインスタンスを、リストに挿入します。 |

## <a name="processscheduleseriespatternitem-class"></a>ProcessScheduleSeriesPatternItem クラス

パターンをコンフィギュレーションすると、該当するフィールドが単位に基づいて決定されます。 次の表に定義されているすべてのメソッドが、すべての単位で機能するわけではありません。 単位に適用されるメソッドは、このセクションの後の表で定義します。 他の組み合わせは無視されます。 ポーリングされたプロセスの場合は、単位とポーリング間隔のみが使用されます。 他のフィールドは無視されます。

| メソッド | 説明 |
|---|---|
| `public ProcessScheduleUnit parmUnit(ProcessScheduleUnit _unit = unit)` | シリーズが実行される時間の単位。 単位には、分または時間を指定できます。 |
| `public ProcessScheduleInterval parmPollingInterval(ProcessScheduleInterval _pollingInterval = pollingInterval)` | ポーリングされたプロセスの場合、この値は単位と共に整数になり、プロセスの実行頻度を定義します。 |
| `public ProcessScheduleDateTime parmStartDate(ProcessScheduleDateTime _startDate = startDate)` | シリーズの開始日。 時刻は、[空の時刻](../dev-ref/xpp-variables-data-types.md#null-values-for-data-types)に設定する必要があります。 |
| `public ProcessScheduleDateTime parmEndDate(ProcessScheduleDateTime _endDate = endDate)` | シリーズの終了日。 時刻は、[空の時刻](../dev-ref/xpp-variables-data-types.md#null-values-for-data-types)に設定する必要があります。 |
| `public ProcessScheduleDateTime parmTime(ProcessScheduleDateTime _time = time)` | シリーズを実行する時刻。 日付は、[空の日付](../dev-ref/xpp-variables-data-types.md#null-values-for-data-types)に設定する必要があります。 |

### <a name="methods-that-are-applicable-to-the-week-unit"></a>週単位に適用できるメソッド

| メソッド | 説明 |
|---|---|
| `public NoYes parmOnSunday(NoYes _onSunday = onSunday)` | 曜日に対して適切なメソッドを選択して、プロセスを実行する曜日。 たとえば、**parmOnMonday()** では、月曜日にジョブが実行されます。 |

### <a name="methods-that-are-applicable-to-the-day-unit"></a>日単位に適用できるメソッド

| メソッド | 説明 |
|---|---|
| `public NoYes parmDoesRepeatEveryNumberOfDays(NoYes _doesRepeatEveryNumberOfDays = doesRepeatEveryNumberOfDays)` | プロセスを *X* 日ごとに実行するかどうかを示し ます。 |
| `public int parmDailyRepeatInterval(int _dailyRepeatInterval = dailyRepeatInterval)` | 日数を示します。 |
| `public NoYes parmDoesRepeatEveryWeekDay(NoYes _doesRepeatEveryWeekDay = doesRepeatEveryWeekDay)` | プロセスを平日に実行するかどうかを示し ます。 |

### <a name="methods-that-are-applicable-to-the-month-unit"></a>月単位に適用できるメソッド

| メソッド | 説明 |
|---|---|
| `public NoYes parmDoesRepeatOnDayOfMonth(NoYes _doesRepeatOnDayOfMonth = doesRepeatOnDayOfMonth)` | このプロセスは、毎月特定の日に実行する必要があります。 |
| `public Day parmMonthlyRepeatDayOfMonth(Day _monthlyRepeatDayOfMonth = monthlyRepeatDayOfMonth)` | プロセスを実行する月の日付。 |

### <a name="modifying-background-processes"></a>バックグラウンド プロセスの変更

システム管理者は、プロセス自動化フレームワークのポーリング間隔と単位を変更できます。 ただし、現在存在する多くのバックグラウンド プロセスは、これらの変更を管理するように構築された固有の UI を備えています。 Microsoft は、次の API を介して、これらの値をプログラムで変更する方法を提供しています。

| メソッド | 説明 |
|---|---|
| `public static ProcessScheduleSeriesPollingDetails getPollingDetailsForSeries(ProcessScheduleTypeName _typeName, ProcessScheduleSeriesName _seriesName)` | ポーリング プロセスのポーリング間隔、単位、および次のスケジュールされた日時を取得します。 |
| `public static void setPollingDetailsForSeries(ProcessScheduleTypeName _typeName, ProcessScheduleSeriesName _seriesName, ProcessScheduleSeriesPollingDetails _pollingDetails)` | ポーリング プロセスのポーリング間隔、単位、および次のスケジュールされた日時の変更を有効にします。 |

## <a name="validating-background-process-settings"></a>バックグラウンド プロセスの設定の検証

バージョン 10.0.13では、プロセス自動化フレームワークによって、システム管理者は **バックグラウンド プロセスの編集** セクションを介してバックグラウンド プロセス設定を変更でき ます。 一部のバックグラウンド プロセスでは、実行頻度が制限されます。 Microsoft は、バックグラウンド プロセスが実装できるインターフェイスを導入しました。 このインターフェイスが呼び出されると、バックグラウンド プロセスを使用して、単位とポーリング間隔が許容範囲内にあることを確認できます。

次の例では、このプロセスが毎分または毎時間ごとに実行されないようにします。 このプロセスは 1 日に 1 回実行できます。 ただし、プロセスは、より頻繁に実行する必要があるような方法でルールを実装することができます。

```xpp
using System.ComponentModel.Composition;

// Provider to validate background settings.
[Export(identifierStr(Dynamics.AX.Application.ProcessScheduleISeriesValidateBackgroundDialog))]
[ExportMetadata(extendedTypeStr(ProcessScheduleTypeName), 'ProcessAutomationExploder')]
internal final class ProcessScheduleExplodeAutomationBackgroundDialogValidationProvider implements ProcessScheduleISeriesValidateBackgroundDialog
{

    public boolean
    validateBackgroundProcessParameters(ProcessScheduleSeriesBackgroundValidationParameters
    _validationParameters)
    {
        ProcessScheduleUnit currentUnit = _validationParameters.parmUnit();
        if (currentUnit == ProcessScheduleUnit::Minute || currentUnit == ProcessScheduleUnit::Hour)
        {
            SysDictEnum enum = new SysDictEnum(enumNum(ProcessScheduleUnit));
            throw Error(
                strFmt("@ProcessAutomationFramework:ProcessScheduleExplodeProcessInvalidUnit",
                enum.value2Label(ProcessScheduleUnit::Minute),
                enum.value2Label(ProcessScheduleUnit::Hour)));
        }
        return true;
    }
}
```

## <a name="processscheduleiseriesvalidatebackgrounddialog-interface"></a>ProcessScheduleISeriesValidateBackgroundDialog インターフェイス

**ProcessScheduleISeriesValidateBackgroundDialog** インターフェイスを使用すると、ユーザーが **ProcessScheduleSeriesBackgroundDialog** を介してバックグラウンド設定を編集するときに、バックグラウンド プロセスでユーザー入力を検証できます。

| メソッド | 説明 |
|---|---|
| `boolean validateBackgroundProcessParameters(ProcessScheduleSeriesBackgroundValidationParameters _validationParameters)` | プロセスに対して設定されている検証ルールを実装します。 |

## <a name="processscheduleseriesbackgroundvalidationparameters-class"></a>ProcessScheduleSeriesBackgroundValidationParameters クラス

**ProcessScheduleSeriesBackgroundValidationParameters** クラスには、編集中のバックグラウンド プロセスに対して検証された検証パラメーターが含まれています。

| メソッド | 説明 |
|---|---|
| `public UserId parmOwnerId(UserId _ownerId = ownerId)` | プロセスの所有者。 バッチジョブは、このユーザーのコンテキストで作成されるので、バッチジョブの作成時に使用されます。 |
| `public ProcessScheduleUnit parmUnit(ProcessScheduleUnit _unit = unit)` | 時間の単位。 |
| `public ProcessScheduleInterval parmPollingInterval(ProcessScheduleInterval _pollingInterval = pollingInterval)` | ポーリング間隔。 この値は、プロセスを実行する時間の単位 (**parmUnit()** で示される) を定義します。 |
| `public ProcessScheduleDateTime parmPolledNextScheduledDateTime(ProcessScheduleDateTime _polledNextScheduledDateTime = polledNextScheduledDateTime)` | 次に協定世界時 (UTC) で予定されているプロセスの実行。 |
| `public ProcessScheduleDateTime parmSleepFromTime(ProcessScheduleDateTime _polledSleepFromTime = polledSleepFromTime)` | スリープを開始するタイミングを指定します。 プロセス自動化フレームワークによって、システム管理者はプロセスを一定時間スリープ状態にすることができます。 **parmPolledNextScheduleDateTime()** の設定に関係なく、この時間範囲中にプロセスが実行されることはありません。 この時間範囲は最大 16 時間であり、日付をまたぐことができます。 |
| `public ProcessScheduleDateTime parmSleepToTime(ProcessScheduleDateTime _polledSleepToTime = polledSleepToTime)` | スリープを終了するタイミングを指定します。 プロセス自動化フレームワークによって、システム管理者はプロセスを一定時間スリープ状態にすることができます。 **parmPolledNextScheduleDateTime()** の設定に関係なく、この時間範囲中にプロセスが実行されることはありません。 この時間範囲は最大 16 時間であり、日付をまたぐことができます。  |
