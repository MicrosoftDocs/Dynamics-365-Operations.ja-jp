---
title: ユーザー インターフェイスのカスタマイズ
description: このトピックでは、プロセス自動化フレームワークを使用して、ユーザー インターフェースをカスタマイズする方法について説明します。
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
ms.openlocfilehash: 2a0b296e7e4926604edc488e4610bdcbdcd876cd
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679220"
---
# <a name="customize-the-user-interface"></a>ユーザー インターフェイスのカスタマイズ

[!include [banner](../includes/banner.md)]

プロセス自動化フレームワークは、一部のユーザー インターフェース (UI) のカスタマイズをサポートしています。 フレーム ワークがすべての既定値を提供しているので、このトピックの大部分は省略可能です。 唯一の例外は、**ProcessScheduleSeries** フォームです。 特定の製品区分に対して **ProcessScheduleSeries** フォームを表示する場合、、フレーム ワークがその製品区分に固有のデータを表示できるように、カスタマイズする必要があります。

## <a name="weekly-calendar-view"></a>週ごとのカレンダー表示

### <a name="processscheduleibuildoccurrencecard-interface"></a>ProcessScheduleIBuildOccurrenceCard のインターフェース

**ProcessScheduleIBuildOccurrenceCard** のインターフェースを使用すると、週ごとのカレンダー表示のオカレンス カードの概観をカスタマイズできます。 インターフェイスには、**スケジュール**、**待機**、**実行**、**成功**、**失敗**、および **無効** の各ステータスに対応する静的メソッドがあります。 ステータス値ごとにカスタマイズされたオカレンス カードを作成できます。 これらの各メソッドは、**ProcessScheduleOccurrenceCard** のインスタンスを返します。

プロセス自動化フレームワークでは、**ProcessScheduleOccurrenceCardBuilder** クラスの既定の実装が提供されます。 このクラスから継承して、必要に応じて機能を上書きします。 次に、特定のタイプの **SysPlugin** を介して派生クラスを登録します。 登録プロセスは、フレームワーク ドキュメントに含まれる多くのプラグインのプロセスに似ています。

**ProcessScheduleOccurrenceCardBuilderContract** のインスタンスが各メソッドに渡され、そのオカレンスに関する情報を取得するために使用できます。 派生クラスでは、**ProcessScheduleOccurrenceCard** インスタンスを返す各静的メソッドの既定の実装を呼び出し、必要な変更を加えて、それを返すことができます。

### <a name="processscheduleoccurrencecard-class"></a>ProcessScheduleOccurrenceCard クラス

**ProcessScheduleOccurrenceCard** クラスを使用すると、カレンダー表示に表示されるオカレンス カードの外観をカスタマイズできます。 最初の 2 行はプロセス自動化フレームワークによって制御されており、変更することはできません。 次の図では、サブヘッダーは **完了した** フェーズで、ステータス メッセージは **完了** という言葉の背景が青色であることを示しています。

![ステータスと時間を表示する既定のオカレンス カード](media/uptake-schedule.png)

| メソッド | 説明 |
|---|---|
| `public str parmSubHeader(str _subHeader = cardSubHeader)` | 前の図に示されているオカレンス カードの 3 行目であるサブヘッダー。 |
| `public str parmStatusMessage(str _statusMessage = statusMessage)` | プロセスのステータスを表し、色付きの背景を持つステータス メッセージ。 |
| `public ProcessExecutionOccurrenceCardStatusColor parmStatusColor(ProcessExecutionOccurrenceCardStatusColor _statusColor = statusColor)` | ステータス メッセージの背景の色。 |

### <a name="processscheduleishowoccurrencecalendarview-interface"></a>ProcessScheduleIShowOccurrenceCalendarView インターフェイス

**ProcessScheduleIShowOccurrenceCalendarView** インターフェースは、週単位のカレンダー表示を表示するフォームで実装する必要があります。 **ProcessScheduleSeries** フォームは、このインターフェイスを実装するフォームの一例です。

| メソッド | 説明 |
|---|---|
| `ProcessScheduleOccurrenceCalendarViewContract getProcessScheduleOccurrenceCalendarViewContract()` | 表示するタイプを決定するために、毎週の表示で使用する契約を返します。 |
| `void refreshAfterChangeToCalendarView()` | この値は、週単位のビューからのコールバックです。 この値は、週ごとのカレンダー 表示が変更されたために親フォームを更新する必要があることを示します。 |

### <a name="processscheduleoccurrencecalendarviewcontract-class"></a>ProcessScheduleOccurrenceCalendarViewContract クラス

**ProcessScheduleOccurrenceCalendarViewContract** クラスを使用して、週ごとのカレンダー表示に表示するシリーズを制限します。 例については、アプリケーション オブジェクト ツリー (AOT) の **ProcessScheduleSeries.getProcessScheduleOccurrenceCalendarViewcontract** を参照してください。

| メソッド | 説明 |
|---|---|
| `public static ProcessScheduleOccurrenceCalendarViewContract construct()` | 単一から多数のタイプのオカレンスを表示することを意図している場合は、このコンストラクターを使用します。 |
| `internal static ProcessScheduleOccurrenceCalendarViewContract newFromScheduleSeries(ProcessScheduleSeries _scheduleSeries)` | 単一のシリーズのオカレンスを表示することを意図している場合は、このコンストラクターを使用します。 |
| `public void AddScheduleType(ProcessScheduleTypeName _scheduleTypeName)` | 1つのシリーズしかを表示していない場合は、この値を使用して、表示するタイプを追加します。 |

### <a name="processscheduleoccurrencecalendarviewrenderer-class"></a>ProcessScheduleOccurrenceCalendarViewRenderer クラス

**ProcessScheduleOccurrenceCalendarViewRenderer** クラスを使用して、週ごとのカレンダー表示を既存のフォームに表示します。 フォーム パーツが作成され、正しく初期化されます。 このクラスの例は、**ProcessScheduleSeries** フォームで使用されます。

| メソッド | 説明 |
|---|---|
| `public static ProcessScheduleICalendarView renderCalendarViewInFormControl(FormGroupControl _containingGroupControl)` | このメソッドは、指定されたフォーム グループ コントロールの週ごとのカレンダー表示をレンダリングします。 |

### <a name="render-interfaces"></a>インターフェースのレンダリング

さまざまなインターフェイスを使用して、カレンダー表示で発生プロセスを表示する方法をカスタマイズできます。 プロセスが保持できる状態ごとに、次のようなインターフェイスが用意されています。

- ProcessScheduleIRenderDisabledOccurrenceCard
- ProcessScheduleIRenderFailedOccurrenceCard
- ProcessScheduleIRenderRunningOccurrenceCard
- ProcessScheduleIRenderScheduledOccurrenceCard
- ProcessScheduleIRenderSuccessfulOccurrenceCard
- ProcessScheduleIRenderWaitingOccurrenceCard

これらのインターフェイスはすべて同じパターンに従います。 **ProcessScheduleOccurrenceCardRendering** のインスタンスがそれらに送信されます。 このインスタンスは、オカレンス カードの表示方法を制御するために使用されます。

例については、AOTの **CustVendPaymProposalAutomationOccurrenceCardRenderer** クラスを参照してください。

### <a name="processscheduleoccurrencecardrendering-class"></a>ProcessScheduleOccurrenceCardRendering クラス

| メソッド | 説明 |
|---|---|
| `public ProcessScheduleOccurrence getOccurrenceBeingRendered()` | このメソッドは、オカレンス カードに表示されているオカレンスを返します。 |
| `public ProcessExecutionExecutingInformation getOccurrenceExecutionInformation()` | このメソッドは、発生したオカレンスの実行情報を返します。 通常、この情報には、バッチ ジョブ、開始時刻、および終了時刻の結果が含まれます。 |
| `public void makeCardSubHeaderInvisible()` | このメソッドによって、カードのサブヘッダーが非表示になります。 このトピックの前の図と下の内容を参照して、どの行がサブヘッダーであるかを決定してください。 |
| `public void makeCardButtonsInvisible()` | このメソッドは、オカレンス カードの **無効化** および **編集** ボタンを非表示にするかどうかを指定します。 |
| `public void setColumnsOnOccurrenceCardDetailGroup(int _numberOfColumns)` | この方法を使用すると、オカレンス カードの列の数をカスタマイズできます。 既定では、2 つの列があります。 |
| `public FormButtonControl addButtonControl(FormControlName _buttonControlName)` | このメソッドを使用すると、新しいボタンをオカレンス カードに追加できます。 |
| `public FormStaticTextControl addStaticTextControl(FormControlName _staticTextControlName)` | このメソッドを使用すると、静的テキスト コントロールをオカレンス カードに追加できます。 |
| `public FormStringControl addStringControl(FormControlName _stringControlName, LabelId _stringControlLabel)` | このメソッドは、オカレンス カードに文字列コントロールを追加します。 |

## <a name="series-list-page"></a>リスト ページのシリーズ

### <a name="processscheduleiseriesformcontroller-interface"></a>ProcessScheduleISeriesFormController インターフェイス

**シリーズ** リスト ページでは、**ProcessScheduleISeriesFormController** コントローラーを使用して、**ProcessScheduleSeries** リスト ページに表示するタイプのシリーズを決定します。 このクラスは **SysPlugin** クラスを使用します。 **ProcessScheduleSeries** フォームを開くために使用するメニュー項目は、指定されたプラグインを呼び出すためのキーとして使用されます。 このキーを使用すると、このフォームを使用して、表示するタイプをカスタマイズできます。

```xpp
// Implementation of the ProcessScheduleISeriesFormController for the admin view of the process schedule Series form.
// This implementation will show series for all process types, both scheduled and polled, on the Series form.
[Export(identifierStr(Dynamics.AX.Application.ProcessScheduleISeriesFormController))]
[ExportMetadata(classStr(ProcessScheduleISeriesFormController), menuItemDisplayStr(ProcessScheduleSeriesAdmin))]
internal class ProcessScheduleSeriesFormAdminController implements ProcessScheduleISeriesFormController
{
    [Hookable(false)]
    public ProcessScheduleSeriesFormContract getSeriesFormContract()
    {
        return ProcessScheduleSeriesFormContract::newForAllScheduleTypes();
    }
}
```

### <a name="processscheduleseriesformcontract-class"></a>ProcessScheduleSeriesFormContract クラス

**ProcessScheduleSeriesFormContract** クラスは、シリーズ リスト ページで **ProcessScheduleType** の表示を決定するために使用される契約です。 このクラスは、ワークスペースで、そのワークスペースに関連付けられている特定のタイプについてのみシリーズを表示するために使用できます。

| メソッド | 説明 |
|---|---|
| `public void addScheduledScheduleType(ProcessScheduleTypeName _scheduleTypeName)` | 特定のスケジュールされたタイプを追加します。 |
| `public void addPolledScheduleType(ProcessScheduleTypeName _scheduleTypeName)` | 特定のポーリングされたタイプを追加します。 |

## <a name="results-and-messages"></a>結果とメッセージ

### <a name="processexecutioniresultscontroller-interface"></a>ProcessExecutionIResultsController インターフェイス

**ProcessExecutionIResultsController** インターフェイスを使用すると、プロセスに従って結果ダイアログ ボックスをカスタマイズできます。 これにより、結果グリッドで **ヘッダー** フィールドの列ヘッダー ラベルを設定して、ヘッダー列の値をハイパーリンクにすることができます。 このインターフェイスは、プラグインであるクラスによって実装する必要があります。 サンプル プラグインを次に示します。

```xpp
using System.ComponentModel.Composition;

[Export(identifierStr(Dynamics.AX.Application.ProcessExecutionIResultsController))]
[ExportMetadata(classStr(ProcessExecutionIResultsController), 'TestScheduledType')]
public final class ProcessExecutionSampleUptakeExecutionResultsController implements ProcessExecutionIResultsController
{
    [Hookable(false)]
    public ProcessExecutionResultsDialogContract getResultsDialogContract()
    {
        ProcessExecutionResultsDialogContract contract = ProcessExecutionResultsDialogContract::construct();
        contract.parmSourceLinkHeaderLabel('Sample Header');
        contract.parmShouldSourceLinkHeaderBeLinkToSourceLinkDetails(true);
        return contract;
    }

    [Hookable(false)]
    public void openSourceLinkDetails(RefTableId _refTableId, RefRecId
    _refRecId)
    {
        if (_refTableId == tableNum(SystemParameters))
        {
            Args args = new Args();
            MenuFunction systemParametersMenuFunction = new MenuFunction(menuItemDisplayStr(SystemParameters), MenuItemType::Display);
            systemParametersMenuFunction.run(args);
        }
    }
}
```

| メソッド | 説明 |
|---|---|
| `ProcessExecutionResultsDialogContract getResultsDialogContract()` | **ProcessExecutionResultsDialogContract** のインスタンスを返します。 |
| `void openSourceLinkDetails(RefTableId _refTableId, RefRecId _refRecId)` | 渡されたレコードを表示できる適切なメニュー項目を開くロジックを実装します。 |

### <a name="processexecutionresultsdialogcontract-class"></a>ProcessExecutionResultsDialogContract クラス

**ProcessExecutionResultsDialogContract** クラスを使用すると、ヘッダー列ラベルをカスタマイズして、ヘッダー列のデータをハイパーリンクとして表示するかどうかを指定できます。

| メソッド | 説明 |
|---|---|
| `public static ProcessExecutionResultsDialogContract newForSourceLinkHeader(LabelId _sourceLinkHeaderLabel, boolean _shouldSourceLinkHeaderBeLinkToSourceLinkDetails)` | ヘッダー列ラベルとして使用するテキストを指定します。 また、ヘッダー列の値をハイパーリンクとして表示するかどうかを示すブール値を提供します。 |
| `public LabelId parmExecutionResultsDialogCaption(LabelId _executionResultsDialogCaption = executionResultsDialogCaption)` | このメソッドは、結果ダイアログ ボックスのキャプションを設定します。 |

### <a name="processexecutionmessagelogdialog-class"></a>ProcessExecutionMessageLogDialog クラス

**ProcessExecutionMessageLogDialog** インターフェイスを使用すると、メッセージ ログを移行元ドメインの内容のコンテキストで開くことができます。 たとえば、転記済仕入先請求書ページからメッセージ ログを開いて、プロセス自動化フレームワークに対して有効になっているプロセスによって仕入先請求書が転記されている間にログに記録されたメッセージを表示することができます。 この例では、転記済仕入先請求書ページで **ProcessExecutionMessageLogDialog** インターフェースを実装する必要があります。 このインターフェイスを使用することにより、独自のプライベート結果/メッセージング サブシステムを作成する必要はありません。

| メソッド | 説明 |
|---|---|
| `ProcessExecutionMessageLogContract getContractForMessageLog()` | このメソッドは、**ProcessExecutionMessageLogContract** のインスタンスを返します。 |

### <a name="processexecutionmessagelogcontract-class"></a>ProcessExecutionMessageLogContract クラス

**ProcessExecutionMessageLogContract** 契約を使用すると、メッセージ ログを移行元ドメインの特定の項目に制限できます。 **ProcessExecutionSourceLink** テーブルには、**RefRecId** および **RefTableId** 値が契約によって送られる値と一致しているレコードが必要です。

| メソッド | 説明 |
|---|---|
| `public static ProcessExecutionMessageLogContract newForSourceRecord(ProcessScheduleTypeName _typeName, RefTableId _refTableId, RefRecId _refRecId, guid _executionId = emptyGuid())` | このメソッドは、指定された型名、**RefTableld** 値、および **RefRecld** 値を使用して契約を初期化します。 **ProcessExecutionSourceLink** テーブルには一致するレコ―ドが存在している必要があります。 バックグラウンド プロセスには、複数の実行 ID が割り当てられます。 したがって、実行 ID の省略可能なパラメーターをバックグラウンド処理用に提供する必要があります。 詳細については、[タイプ登録](type-registration.md) を参照してください。 |
