---
title: シリーズ登録
description: このトピックでは、プロセス自動化フレームワークでシリーズを作成する方法について説明します。
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
ms.openlocfilehash: 15aab9e43ad74883ad9b4539fceef77f8b0b3dfb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751349"
---
# <a name="series-registration"></a><span data-ttu-id="1c39c-103">シリーズ登録</span><span class="sxs-lookup"><span data-stu-id="1c39c-103">Series registration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c39c-104">すべてのプロセスには、*シリーズ* が必要です。</span><span class="sxs-lookup"><span data-stu-id="1c39c-104">Every process must have a *series*.</span></span> <span data-ttu-id="1c39c-105">プロセス自動化のシリーズの概念は、Microsoft Outlook でのミーティング シリーズの概念に似ています。</span><span class="sxs-lookup"><span data-stu-id="1c39c-105">The concept of a series in process automation resembles the concept of a meeting series in Microsoft Outlook.</span></span> <span data-ttu-id="1c39c-106">ただし、プロセス自動化のシリーズは、一連のスケジュールされたプロセスの実行です。</span><span class="sxs-lookup"><span data-stu-id="1c39c-106">However, a series in process automation is a series of scheduled runs of a process.</span></span> <span data-ttu-id="1c39c-107">ほとんどのスケジュールされたプロセス タイプでは、ユーザーがユーザー インターフェイス (UI) にシリーズを作成し、シリーズ登録を実装する必要がありません。</span><span class="sxs-lookup"><span data-stu-id="1c39c-107">For most scheduled process types, users create the series in the user interface (UI), and series registration never has to be implemented.</span></span> <span data-ttu-id="1c39c-108">ただし、実装中のプロセスが一連のスケジュールである場合は、このタスクを省略できます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-108">However, if the process that is being implemented is a schedule series, you can skip this task.</span></span>

<span data-ttu-id="1c39c-109">バックグラウンド プロセスは、ユーザー操作を許可しない内部プロセスとなる傾向があるため、通常シリーズ登録を使用してコードを介してシリーズを作成します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-109">Background processes typically create a series via code, by using series registration, because background processes tend to be "under the hood" processes that don't allow for user interaction.</span></span> <span data-ttu-id="1c39c-110">コードを介してシリーズを作成するには、**ProcessScheduleISeriesRegistration** インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-110">To create a series via code, you implement the **ProcessScheduleISeriesRegistration** interface.</span></span> <span data-ttu-id="1c39c-111">このインターフェイスには、**ProcessScheduleSeriesRegistrationItem** のインスタンスを返す単一のメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="1c39c-111">This interface contains a single method that returns an instance of **ProcessScheduleSeriesRegistrationItem**.</span></span>

<span data-ttu-id="1c39c-112">プロセス自動化フレームワークは、システム管理者が既定のポーリング間隔とバックグラウンド プロセスの単位を変更できるようにします。</span><span class="sxs-lookup"><span data-stu-id="1c39c-112">The process automation framework lets system admins change the default polling interval and unit for background processes.</span></span>

<span data-ttu-id="1c39c-113">ここでは、プロセス自動化フレームワークのテストに使用するテスト シリーズの例を示します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-113">Here is an example of a test series that is used to test the process automation framework.</span></span>

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

## <a name="processscheduleseriesregistrationitem-class"></a><span data-ttu-id="1c39c-114">ProcessScheduleSeriesRegistrationItem クラス</span><span class="sxs-lookup"><span data-stu-id="1c39c-114">ProcessScheduleSeriesRegistrationItem class</span></span>

| <span data-ttu-id="1c39c-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="1c39c-115">Method</span></span> | <span data-ttu-id="1c39c-116">説明</span><span class="sxs-lookup"><span data-stu-id="1c39c-116">Description</span></span> |
|---|---|
| `public ProcessScheduleTypeName parmTypeName(ProcessScheduleTypeName _typeName = typeName)` | <span data-ttu-id="1c39c-117">タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="1c39c-117">The name of the type.</span></span> |
| `public ProcessScheduleSeriesName parmSeriesName(ProcessScheduleSeriesName _SeriesName = seriesName)` | <span data-ttu-id="1c39c-118">シリーズの名前。</span><span class="sxs-lookup"><span data-stu-id="1c39c-118">The name of the series.</span></span> <span data-ttu-id="1c39c-119">名前からシリーズの目的がよく理解できるように、説明的なものにしてください。</span><span class="sxs-lookup"><span data-stu-id="1c39c-119">Be descriptive, so that the purpose of the series is clear from the name.</span></span> |
| `public Description parmDescription(Description _description = description)` | <span data-ttu-id="1c39c-120">シリーズの説明。</span><span class="sxs-lookup"><span data-stu-id="1c39c-120">The description of the series.</span></span> |
| `public UserGroupId parmOwnerId(UserGroupId _ownerId = ownerId)` | <span data-ttu-id="1c39c-121">シリーズ所有者のユーザー ID。</span><span class="sxs-lookup"><span data-stu-id="1c39c-121">The user ID of the owner of the series.</span></span> |
| `public List parmProcessScheduleSeriesPatternList(List _seriesPatternList = seriesPatternList)` | <span data-ttu-id="1c39c-122">シリーズのパターン一覧。</span><span class="sxs-lookup"><span data-stu-id="1c39c-122">The list of patterns for the series.</span></span> <span data-ttu-id="1c39c-123">現時点では、各シリーズには 1 つのパターンしかサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1c39c-123">Currently, only one pattern per series is supported.</span></span> <span data-ttu-id="1c39c-124">ただし、この制限は将来変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1c39c-124">However, this limitation might change in the future.</span></span> <span data-ttu-id="1c39c-125">**ProcessScheduleSeriesPatternItem** クラスのインスタンスを、リストに挿入します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-125">Insert an instance of the **ProcessScheduleSeriesPatternItem** class into the list.</span></span> |

## <a name="processscheduleseriespatternitem-class"></a><span data-ttu-id="1c39c-126">ProcessScheduleSeriesPatternItem クラス</span><span class="sxs-lookup"><span data-stu-id="1c39c-126">ProcessScheduleSeriesPatternItem class</span></span>

<span data-ttu-id="1c39c-127">パターンをコンフィギュレーションすると、該当するフィールドが単位に基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-127">When the pattern is configured, applicable fields are determined based on the unit.</span></span> <span data-ttu-id="1c39c-128">次の表に定義されているすべてのメソッドが、すべての単位で機能するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="1c39c-128">Not all methods that are defined in the following table work for all units.</span></span> <span data-ttu-id="1c39c-129">単位に適用されるメソッドは、このセクションの後の表で定義します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-129">The methods that apply to units are defined in the tables later in this section.</span></span> <span data-ttu-id="1c39c-130">他の組み合わせは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-130">Other combinations will be ignored.</span></span> <span data-ttu-id="1c39c-131">ポーリングされたプロセスの場合は、単位とポーリング間隔のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-131">For polled processes, only the unit and the polling interval are used.</span></span> <span data-ttu-id="1c39c-132">他のフィールドは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-132">Other fields are ignored.</span></span>

| <span data-ttu-id="1c39c-133">メソッド</span><span class="sxs-lookup"><span data-stu-id="1c39c-133">Method</span></span> | <span data-ttu-id="1c39c-134">説明</span><span class="sxs-lookup"><span data-stu-id="1c39c-134">Description</span></span> |
|---|---|
| `public ProcessScheduleUnit parmUnit(ProcessScheduleUnit _unit = unit)` | <span data-ttu-id="1c39c-135">シリーズが実行される時間の単位。</span><span class="sxs-lookup"><span data-stu-id="1c39c-135">The unit of time that the series runs in.</span></span> <span data-ttu-id="1c39c-136">単位には、分または時間を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-136">The unit can be minutes or hours.</span></span> |
| `public ProcessScheduleInterval parmPollingInterval(ProcessScheduleInterval _pollingInterval = pollingInterval)` | <span data-ttu-id="1c39c-137">ポーリングされたプロセスの場合、この値は単位と共に整数になり、プロセスの実行頻度を定義します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-137">For polled processes, this value is an integer that, together with the unit, defines how often the process runs.</span></span> |
| `public ProcessScheduleDateTime parmStartDate(ProcessScheduleDateTime _startDate = startDate)` | <span data-ttu-id="1c39c-138">シリーズの開始日。</span><span class="sxs-lookup"><span data-stu-id="1c39c-138">The start date of the series.</span></span> <span data-ttu-id="1c39c-139">時刻は、[空の時刻](../dev-ref/xpp-variables-data-types.md#null-values-for-data-types)に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c39c-139">The time should be set to the [empty time](../dev-ref/xpp-variables-data-types.md#null-values-for-data-types).</span></span> |
| `public ProcessScheduleDateTime parmEndDate(ProcessScheduleDateTime _endDate = endDate)` | <span data-ttu-id="1c39c-140">シリーズの終了日。</span><span class="sxs-lookup"><span data-stu-id="1c39c-140">The end date of the series.</span></span> <span data-ttu-id="1c39c-141">時刻は、[空の時刻](../dev-ref/xpp-variables-data-types.md#null-values-for-data-types)に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c39c-141">The time should be set to the [empty time](../dev-ref/xpp-variables-data-types.md#null-values-for-data-types).</span></span> |
| `public ProcessScheduleDateTime parmTime(ProcessScheduleDateTime _time = time)` | <span data-ttu-id="1c39c-142">シリーズを実行する時刻。</span><span class="sxs-lookup"><span data-stu-id="1c39c-142">The time when the series should run.</span></span> <span data-ttu-id="1c39c-143">日付は、[空の日付](../dev-ref/xpp-variables-data-types.md#null-values-for-data-types)に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c39c-143">The date should be set to the [empty date](../dev-ref/xpp-variables-data-types.md#null-values-for-data-types).</span></span> |

### <a name="methods-that-are-applicable-to-the-week-unit"></a><span data-ttu-id="1c39c-144">週単位に適用できるメソッド</span><span class="sxs-lookup"><span data-stu-id="1c39c-144">Methods that are applicable to the week unit</span></span>

| <span data-ttu-id="1c39c-145">メソッド</span><span class="sxs-lookup"><span data-stu-id="1c39c-145">Method</span></span> | <span data-ttu-id="1c39c-146">説明</span><span class="sxs-lookup"><span data-stu-id="1c39c-146">Description</span></span> |
|---|---|
| `public NoYes parmOnSunday(NoYes _onSunday = onSunday)` | <span data-ttu-id="1c39c-147">曜日に対して適切なメソッドを選択して、プロセスを実行する曜日。</span><span class="sxs-lookup"><span data-stu-id="1c39c-147">The days of the week that you want the process to run on by selecting the appropriate methods for the day of the week.</span></span> <span data-ttu-id="1c39c-148">たとえば、**parmOnMonday()** では、月曜日にジョブが実行されます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-148">For example, **parmOnMonday()** will run the job on a Monday.</span></span> |

### <a name="methods-that-are-applicable-to-the-day-unit"></a><span data-ttu-id="1c39c-149">日単位に適用できるメソッド</span><span class="sxs-lookup"><span data-stu-id="1c39c-149">Methods that are applicable to the day unit</span></span>

| <span data-ttu-id="1c39c-150">メソッド</span><span class="sxs-lookup"><span data-stu-id="1c39c-150">Method</span></span> | <span data-ttu-id="1c39c-151">説明</span><span class="sxs-lookup"><span data-stu-id="1c39c-151">Description</span></span> |
|---|---|
| `public NoYes parmDoesRepeatEveryNumberOfDays(NoYes _doesRepeatEveryNumberOfDays = doesRepeatEveryNumberOfDays)` | <span data-ttu-id="1c39c-152">プロセスを *X* 日ごとに実行するかどうかを示し ます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-152">Indicates whether the process should run every *X* number of days.</span></span> |
| `public int parmDailyRepeatInterval(int _dailyRepeatInterval = dailyRepeatInterval)` | <span data-ttu-id="1c39c-153">日数を示します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-153">Indicates the number of days.</span></span> |
| `public NoYes parmDoesRepeatEveryWeekDay(NoYes _doesRepeatEveryWeekDay = doesRepeatEveryWeekDay)` | <span data-ttu-id="1c39c-154">プロセスを平日に実行するかどうかを示し ます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-154">Indicates whether the process should run every weekday.</span></span> |

### <a name="methods-that-are-applicable-to-the-month-unit"></a><span data-ttu-id="1c39c-155">月単位に適用できるメソッド</span><span class="sxs-lookup"><span data-stu-id="1c39c-155">Methods that are applicable to the month unit</span></span>

| <span data-ttu-id="1c39c-156">メソッド</span><span class="sxs-lookup"><span data-stu-id="1c39c-156">Method</span></span> | <span data-ttu-id="1c39c-157">説明</span><span class="sxs-lookup"><span data-stu-id="1c39c-157">Description</span></span> |
|---|---|
| `public NoYes parmDoesRepeatOnDayOfMonth(NoYes _doesRepeatOnDayOfMonth = doesRepeatOnDayOfMonth)` | <span data-ttu-id="1c39c-158">このプロセスは、毎月特定の日に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c39c-158">The process should run on a specific day of every month.</span></span> |
| `public Day parmMonthlyRepeatDayOfMonth(Day _monthlyRepeatDayOfMonth = monthlyRepeatDayOfMonth)` | <span data-ttu-id="1c39c-159">プロセスを実行する月の日付。</span><span class="sxs-lookup"><span data-stu-id="1c39c-159">The day of month when the process should run.</span></span> |

### <a name="modifying-background-processes"></a><span data-ttu-id="1c39c-160">バックグラウンド プロセスの変更</span><span class="sxs-lookup"><span data-stu-id="1c39c-160">Modifying background processes</span></span>

<span data-ttu-id="1c39c-161">システム管理者は、プロセス自動化フレームワークのポーリング間隔と単位を変更できます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-161">System admins can modify the polling interval and unit in the process automation framework.</span></span> <span data-ttu-id="1c39c-162">ただし、現在存在する多くのバックグラウンド プロセスは、これらの変更を管理するように構築された固有の UI を備えています。</span><span class="sxs-lookup"><span data-stu-id="1c39c-162">However, many background processes that currently exist have their own specific UI that is built to manage these changes.</span></span> <span data-ttu-id="1c39c-163">Microsoft は、次の API を介して、これらの値をプログラムで変更する方法を提供しています。</span><span class="sxs-lookup"><span data-stu-id="1c39c-163">Microsoft provides a way to programmatically modify these values via the following APIs.</span></span>

| <span data-ttu-id="1c39c-164">メソッド</span><span class="sxs-lookup"><span data-stu-id="1c39c-164">Method</span></span> | <span data-ttu-id="1c39c-165">説明</span><span class="sxs-lookup"><span data-stu-id="1c39c-165">Description</span></span> |
|---|---|
| `public static ProcessScheduleSeriesPollingDetails getPollingDetailsForSeries(ProcessScheduleTypeName _typeName, ProcessScheduleSeriesName _seriesName)` | <span data-ttu-id="1c39c-166">ポーリング プロセスのポーリング間隔、単位、および次のスケジュールされた日時を取得します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-166">Gets the polling interval, the unit, and the next scheduled date/time for a polled process.</span></span> |
| `public static void setPollingDetailsForSeries(ProcessScheduleTypeName _typeName, ProcessScheduleSeriesName _seriesName, ProcessScheduleSeriesPollingDetails _pollingDetails)` | <span data-ttu-id="1c39c-167">ポーリング プロセスのポーリング間隔、単位、および次のスケジュールされた日時の変更を有効にします。</span><span class="sxs-lookup"><span data-stu-id="1c39c-167">Enables changes to the polling interval, the unit, and the next scheduled date/time for a polled process.</span></span> |

## <a name="validating-background-process-settings"></a><span data-ttu-id="1c39c-168">バックグラウンド プロセスの設定の検証</span><span class="sxs-lookup"><span data-stu-id="1c39c-168">Validating background process settings</span></span>

<span data-ttu-id="1c39c-169">バージョン 10.0.13では、プロセス自動化フレームワークによって、システム管理者は **バックグラウンド プロセスの編集** セクションを介してバックグラウンド プロセス設定を変更でき ます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-169">In version 10.0.13, the process automation framework lets system admins modify background process settings via the **Edit background process** section.</span></span> <span data-ttu-id="1c39c-170">一部のバックグラウンド プロセスでは、実行頻度が制限されます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-170">Some background processes have restrictions on the frequency of their runs.</span></span> <span data-ttu-id="1c39c-171">Microsoft は、バックグラウンド プロセスが実装できるインターフェイスを導入しました。</span><span class="sxs-lookup"><span data-stu-id="1c39c-171">Microsoft has introduced an interface that a background process can implement.</span></span> <span data-ttu-id="1c39c-172">このインターフェイスが呼び出されると、バックグラウンド プロセスを使用して、単位とポーリング間隔が許容範囲内にあることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-172">When this interface is invoked, it enables the background process to ensure that the unit and polling interval are within their allowed range.</span></span>

<span data-ttu-id="1c39c-173">次の例では、このプロセスが毎分または毎時間ごとに実行されないようにします。</span><span class="sxs-lookup"><span data-stu-id="1c39c-173">The following example prevents this process from ever being run every minute or every hour.</span></span> <span data-ttu-id="1c39c-174">このプロセスは 1 日に 1 回実行できます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-174">The process can run a maximum of one time per day.</span></span> <span data-ttu-id="1c39c-175">ただし、プロセスは、より頻繁に実行する必要があるような方法でルールを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-175">However, a process can implement the rules in such a way that more frequent runs are required.</span></span>

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

## <a name="processscheduleiseriesvalidatebackgrounddialog-interface"></a><span data-ttu-id="1c39c-176">ProcessScheduleISeriesValidateBackgroundDialog インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1c39c-176">ProcessScheduleISeriesValidateBackgroundDialog interface</span></span>

<span data-ttu-id="1c39c-177">**ProcessScheduleISeriesValidateBackgroundDialog** インターフェイスを使用すると、ユーザーが **ProcessScheduleSeriesBackgroundDialog** を介してバックグラウンド設定を編集するときに、バックグラウンド プロセスでユーザー入力を検証できます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-177">The **ProcessScheduleISeriesValidateBackgroundDialog** interface enables background processes to validate user input when users edit background settings via **ProcessScheduleSeriesBackgroundDialog**.</span></span>

| <span data-ttu-id="1c39c-178">メソッド</span><span class="sxs-lookup"><span data-stu-id="1c39c-178">Method</span></span> | <span data-ttu-id="1c39c-179">説明</span><span class="sxs-lookup"><span data-stu-id="1c39c-179">Description</span></span> |
|---|---|
| `boolean validateBackgroundProcessParameters(ProcessScheduleSeriesBackgroundValidationParameters _validationParameters)` | <span data-ttu-id="1c39c-180">プロセスに対して設定されている検証ルールを実装します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-180">Implements any validation rules that you have for the process.</span></span> |

## <a name="processscheduleseriesbackgroundvalidationparameters-class"></a><span data-ttu-id="1c39c-181">ProcessScheduleSeriesBackgroundValidationParameters クラス</span><span class="sxs-lookup"><span data-stu-id="1c39c-181">ProcessScheduleSeriesBackgroundValidationParameters class</span></span>

<span data-ttu-id="1c39c-182">**ProcessScheduleSeriesBackgroundValidationParameters** クラスには、編集中のバックグラウンド プロセスに対して検証された検証パラメーターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c39c-182">The **ProcessScheduleSeriesBackgroundValidationParameters** class contains the validation parameters that are validated for the background processes that are being edited.</span></span>

| <span data-ttu-id="1c39c-183">メソッド</span><span class="sxs-lookup"><span data-stu-id="1c39c-183">Method</span></span> | <span data-ttu-id="1c39c-184">説明</span><span class="sxs-lookup"><span data-stu-id="1c39c-184">Description</span></span> |
|---|---|
| `public UserId parmOwnerId(UserId _ownerId = ownerId)` | <span data-ttu-id="1c39c-185">プロセスの所有者。</span><span class="sxs-lookup"><span data-stu-id="1c39c-185">The owner of the process.</span></span> <span data-ttu-id="1c39c-186">バッチジョブは、このユーザーのコンテキストで作成されるので、バッチジョブの作成時に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-186">It will be used when batch jobs are created, because batch jobs will be created under this user's context.</span></span> |
| `public ProcessScheduleUnit parmUnit(ProcessScheduleUnit _unit = unit)` | <span data-ttu-id="1c39c-187">時間の単位。</span><span class="sxs-lookup"><span data-stu-id="1c39c-187">The unit of time.</span></span> |
| `public ProcessScheduleInterval parmPollingInterval(ProcessScheduleInterval _pollingInterval = pollingInterval)` | <span data-ttu-id="1c39c-188">ポーリング間隔。</span><span class="sxs-lookup"><span data-stu-id="1c39c-188">The polling interval.</span></span> <span data-ttu-id="1c39c-189">この値は、プロセスを実行する時間の単位 (**parmUnit()** で示される) を定義します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-189">It defines the number of units of time (as specified by **parmUnit()**) that the process should be run.</span></span> |
| `public ProcessScheduleDateTime parmPolledNextScheduledDateTime(ProcessScheduleDateTime _polledNextScheduledDateTime = polledNextScheduledDateTime)` | <span data-ttu-id="1c39c-190">次に協定世界時 (UTC) で予定されているプロセスの実行。</span><span class="sxs-lookup"><span data-stu-id="1c39c-190">The next scheduled run of the process in Coordinated Universal Time (UTC).</span></span> |
| `public ProcessScheduleDateTime parmSleepFromTime(ProcessScheduleDateTime _polledSleepFromTime = polledSleepFromTime)` | <span data-ttu-id="1c39c-191">スリープを開始するタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-191">Specifies when the sleep should start.</span></span> <span data-ttu-id="1c39c-192">プロセス自動化フレームワークによって、システム管理者はプロセスを一定時間スリープ状態にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-192">The process automation framework lets system admins put a process to sleep for a time range.</span></span> <span data-ttu-id="1c39c-193">**parmPolledNextScheduleDateTime()** の設定に関係なく、この時間範囲中にプロセスが実行されることはありません。</span><span class="sxs-lookup"><span data-stu-id="1c39c-193">The process isn't run during this time range, regardless of the setting of **parmPolledNextScheduleDateTime()**.</span></span> <span data-ttu-id="1c39c-194">この時間範囲は最大 16 時間であり、日付をまたぐことができます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-194">This time range is a maximum of 16 hours and can span the date boundary.</span></span> |
| `public ProcessScheduleDateTime parmSleepToTime(ProcessScheduleDateTime _polledSleepToTime = polledSleepToTime)` | <span data-ttu-id="1c39c-195">スリープを終了するタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="1c39c-195">Specifies when the sleep should end.</span></span> <span data-ttu-id="1c39c-196">プロセス自動化フレームワークによって、システム管理者はプロセスを一定時間スリープ状態にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-196">The process automation framework lets system admins put a process to sleep for a time range.</span></span> <span data-ttu-id="1c39c-197">**parmPolledNextScheduleDateTime()** の設定に関係なく、この時間範囲中にプロセスが実行されることはありません。</span><span class="sxs-lookup"><span data-stu-id="1c39c-197">The process isn't run during this time range, regardless of the setting of **parmPolledNextScheduleDateTime()**.</span></span> <span data-ttu-id="1c39c-198">この時間範囲は最大 16 時間であり、日付をまたぐことができます。</span><span class="sxs-lookup"><span data-stu-id="1c39c-198">This time range is a maximum of 16 hours and can span the date boundary.</span></span>  |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]