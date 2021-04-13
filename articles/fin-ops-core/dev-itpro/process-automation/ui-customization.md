---
title: ユーザー インターフェイスのカスタマイズ
description: このトピックでは、プロセス自動化フレームワークを使用して、ユーザー インターフェースをカスタマイズする方法について説明します。
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
ms.openlocfilehash: d2196d902aa90be3a9ffd5de9870919e42980008
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751346"
---
# <a name="customize-the-user-interface"></a><span data-ttu-id="17689-103">ユーザー インターフェイスのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="17689-103">Customize the user interface</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17689-104">プロセス自動化フレームワークは、一部のユーザー インターフェース (UI) のカスタマイズをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="17689-104">The process automation framework supports some customizations of the user interface (UI).</span></span> <span data-ttu-id="17689-105">フレーム ワークがすべての既定値を提供しているので、このトピックの大部分は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="17689-105">Most of this topic is optional, because the framework provides default values for everything.</span></span> <span data-ttu-id="17689-106">唯一の例外は、**ProcessScheduleSeries** フォームです。</span><span class="sxs-lookup"><span data-stu-id="17689-106">The only exception is the **ProcessScheduleSeries** form.</span></span> <span data-ttu-id="17689-107">特定の製品区分に対して **ProcessScheduleSeries** フォームを表示する場合、、フレーム ワークがその製品区分に固有のデータを表示できるように、カスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17689-107">If you intend to show the **ProcessScheduleSeries** form for a specific product area, customizations are required so that the framework can show data that is specific to that product area.</span></span>

## <a name="weekly-calendar-view"></a><span data-ttu-id="17689-108">週ごとのカレンダー表示</span><span class="sxs-lookup"><span data-stu-id="17689-108">Weekly calendar view</span></span>

### <a name="processscheduleibuildoccurrencecard-interface"></a><span data-ttu-id="17689-109">ProcessScheduleIBuildOccurrenceCard のインターフェース</span><span class="sxs-lookup"><span data-stu-id="17689-109">ProcessScheduleIBuildOccurrenceCard interface</span></span>

<span data-ttu-id="17689-110">**ProcessScheduleIBuildOccurrenceCard** のインターフェースを使用すると、週ごとのカレンダー表示のオカレンス カードの概観をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="17689-110">The **ProcessScheduleIBuildOccurrenceCard** interface lets you customize the appearance of occurrence cards in the weekly calendar view.</span></span> <span data-ttu-id="17689-111">インターフェイスには、**スケジュール**、**待機**、**実行**、**成功**、**失敗**、および **無効** の各ステータスに対応する静的メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="17689-111">There is a static method on the interface for each status of an occurrence: **Scheduled**, **Waiting**, **Running**, **Successful**, **Failed**, and **Disabled**.</span></span> <span data-ttu-id="17689-112">ステータス値ごとにカスタマイズされたオカレンス カードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="17689-112">You can create a customized occurrence card for each status value.</span></span> <span data-ttu-id="17689-113">これらの各メソッドは、**ProcessScheduleOccurrenceCard** のインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="17689-113">Each of these methods returns an instance of **ProcessScheduleOccurrenceCard**.</span></span>

<span data-ttu-id="17689-114">プロセス自動化フレームワークでは、**ProcessScheduleOccurrenceCardBuilder** クラスの既定の実装が提供されます。</span><span class="sxs-lookup"><span data-stu-id="17689-114">The process automation framework provides a default implementation in the **ProcessScheduleOccurrenceCardBuilder** class.</span></span> <span data-ttu-id="17689-115">このクラスから継承して、必要に応じて機能を上書きします。</span><span class="sxs-lookup"><span data-stu-id="17689-115">You inherit from this class and override the functionality as you require.</span></span> <span data-ttu-id="17689-116">次に、特定のタイプの **SysPlugin** を介して派生クラスを登録します。</span><span class="sxs-lookup"><span data-stu-id="17689-116">You then register your derived class via the **SysPlugin** for your specific type.</span></span> <span data-ttu-id="17689-117">登録プロセスは、フレームワーク ドキュメントに含まれる多くのプラグインのプロセスに似ています。</span><span class="sxs-lookup"><span data-stu-id="17689-117">The registration process resembles the process for many of the plug-ins in the framework documentation.</span></span>

<span data-ttu-id="17689-118">**ProcessScheduleOccurrenceCardBuilderContract** のインスタンスが各メソッドに渡され、そのオカレンスに関する情報を取得するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="17689-118">An instance of **ProcessScheduleOccurrenceCardBuilderContract** is passed into each of the methods and can be used to retrieve information about the occurrence.</span></span> <span data-ttu-id="17689-119">派生クラスでは、**ProcessScheduleOccurrenceCard** インスタンスを返す各静的メソッドの既定の実装を呼び出し、必要な変更を加えて、それを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="17689-119">The derived class can invoke the default implementation for each static method that returns the **ProcessScheduleOccurrenceCard** instance, modify whatever is required, and return it.</span></span>

### <a name="processscheduleoccurrencecard-class"></a><span data-ttu-id="17689-120">ProcessScheduleOccurrenceCard クラス</span><span class="sxs-lookup"><span data-stu-id="17689-120">ProcessScheduleOccurrenceCard class</span></span>

<span data-ttu-id="17689-121">**ProcessScheduleOccurrenceCard** クラスを使用すると、カレンダー表示に表示されるオカレンス カードの外観をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="17689-121">The **ProcessScheduleOccurrenceCard** class lets you customize the appearance of an occurrence card that is shown in the calendar view.</span></span> <span data-ttu-id="17689-122">最初の 2 行はプロセス自動化フレームワークによって制御されており、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="17689-122">The first two lines are controlled by the process automation framework and can't be modified.</span></span> <span data-ttu-id="17689-123">次の図では、サブヘッダーは **完了した** フェーズで、ステータス メッセージは **完了** という言葉の背景が青色であることを示しています。</span><span class="sxs-lookup"><span data-stu-id="17689-123">In the following illustration, the subheader is the **Completed at** phrase, and the status message is the word **Completed** that has a blue background.</span></span>

![ステータスと時間を表示する既定のオカレンス カード](media/uptake-schedule.png)

| <span data-ttu-id="17689-125">メソッド</span><span class="sxs-lookup"><span data-stu-id="17689-125">Method</span></span> | <span data-ttu-id="17689-126">説明</span><span class="sxs-lookup"><span data-stu-id="17689-126">Description</span></span> |
|---|---|
| `public str parmSubHeader(str _subHeader = cardSubHeader)` | <span data-ttu-id="17689-127">前の図に示されているオカレンス カードの 3 行目であるサブヘッダー。</span><span class="sxs-lookup"><span data-stu-id="17689-127">The subheader, which is the third line of the occurrence card that is shown in the previous illustration.</span></span> |
| `public str parmStatusMessage(str _statusMessage = statusMessage)` | <span data-ttu-id="17689-128">プロセスのステータスを表し、色付きの背景を持つステータス メッセージ。</span><span class="sxs-lookup"><span data-stu-id="17689-128">The status message, which represents the status of the process and has a colored background.</span></span> |
| `public ProcessExecutionOccurrenceCardStatusColor parmStatusColor(ProcessExecutionOccurrenceCardStatusColor _statusColor = statusColor)` | <span data-ttu-id="17689-129">ステータス メッセージの背景の色。</span><span class="sxs-lookup"><span data-stu-id="17689-129">The color of the background for the status message.</span></span> |

### <a name="processscheduleishowoccurrencecalendarview-interface"></a><span data-ttu-id="17689-130">ProcessScheduleIShowOccurrenceCalendarView インターフェイス</span><span class="sxs-lookup"><span data-stu-id="17689-130">ProcessScheduleIShowOccurrenceCalendarView interface</span></span>

<span data-ttu-id="17689-131">**ProcessScheduleIShowOccurrenceCalendarView** インターフェースは、週単位のカレンダー表示を表示するフォームで実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17689-131">The **ProcessScheduleIShowOccurrenceCalendarView** interface must be implemented by forms that will show the weekly calendar view.</span></span> <span data-ttu-id="17689-132">**ProcessScheduleSeries** フォームは、このインターフェイスを実装するフォームの一例です。</span><span class="sxs-lookup"><span data-stu-id="17689-132">The **ProcessScheduleSeries** form is an example of a form that implements this interface.</span></span>

| <span data-ttu-id="17689-133">メソッド</span><span class="sxs-lookup"><span data-stu-id="17689-133">Method</span></span> | <span data-ttu-id="17689-134">説明</span><span class="sxs-lookup"><span data-stu-id="17689-134">Description</span></span> |
|---|---|
| `ProcessScheduleOccurrenceCalendarViewContract getProcessScheduleOccurrenceCalendarViewContract()` | <span data-ttu-id="17689-135">表示するタイプを決定するために、毎週の表示で使用する契約を返します。</span><span class="sxs-lookup"><span data-stu-id="17689-135">Return the contract that the weekly view will use to determine which types should be shown.</span></span> |
| `void refreshAfterChangeToCalendarView()` | <span data-ttu-id="17689-136">この値は、週単位のビューからのコールバックです。</span><span class="sxs-lookup"><span data-stu-id="17689-136">This value is a callback from the weekly view.</span></span> <span data-ttu-id="17689-137">この値は、週ごとのカレンダー 表示が変更されたために親フォームを更新する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="17689-137">It indicates that the parent form should be refreshed because of changes in the weekly calendar view.</span></span> |

### <a name="processscheduleoccurrencecalendarviewcontract-class"></a><span data-ttu-id="17689-138">ProcessScheduleOccurrenceCalendarViewContract クラス</span><span class="sxs-lookup"><span data-stu-id="17689-138">ProcessScheduleOccurrenceCalendarViewContract class</span></span>

<span data-ttu-id="17689-139">**ProcessScheduleOccurrenceCalendarViewContract** クラスを使用して、週ごとのカレンダー表示に表示するシリーズを制限します。</span><span class="sxs-lookup"><span data-stu-id="17689-139">Use the **ProcessScheduleOccurrenceCalendarViewContract** class to limit the series that the weekly calendar view should show.</span></span> <span data-ttu-id="17689-140">例については、アプリケーション オブジェクト ツリー (AOT) の **ProcessScheduleSeries.getProcessScheduleOccurrenceCalendarViewcontract** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17689-140">For an example, see **ProcessScheduleSeries.getProcessScheduleOccurrenceCalendarViewcontract** in the Application Object Tree (AOT).</span></span>

| <span data-ttu-id="17689-141">メソッド</span><span class="sxs-lookup"><span data-stu-id="17689-141">Method</span></span> | <span data-ttu-id="17689-142">説明</span><span class="sxs-lookup"><span data-stu-id="17689-142">Description</span></span> |
|---|---|
| `public static ProcessScheduleOccurrenceCalendarViewContract construct()` | <span data-ttu-id="17689-143">単一から多数のタイプのオカレンスを表示することを意図している場合は、このコンストラクターを使用します。</span><span class="sxs-lookup"><span data-stu-id="17689-143">Use this constructor if the intention is to show occurrences for one to many types.</span></span> |
| `internal static ProcessScheduleOccurrenceCalendarViewContract newFromScheduleSeries(ProcessScheduleSeries _scheduleSeries)` | <span data-ttu-id="17689-144">単一のシリーズのオカレンスを表示することを意図している場合は、このコンストラクターを使用します。</span><span class="sxs-lookup"><span data-stu-id="17689-144">Use this constructor if the intention is to show occurrences for a single series.</span></span> |
| `public void AddScheduleType(ProcessScheduleTypeName _scheduleTypeName)` | <span data-ttu-id="17689-145">1つのシリーズしかを表示していない場合は、この値を使用して、表示するタイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="17689-145">If you aren't showing just one series, use this value to add the types that should be shown.</span></span> |

### <a name="processscheduleoccurrencecalendarviewrenderer-class"></a><span data-ttu-id="17689-146">ProcessScheduleOccurrenceCalendarViewRenderer クラス</span><span class="sxs-lookup"><span data-stu-id="17689-146">ProcessScheduleOccurrenceCalendarViewRenderer class</span></span>

<span data-ttu-id="17689-147">**ProcessScheduleOccurrenceCalendarViewRenderer** クラスを使用して、週ごとのカレンダー表示を既存のフォームに表示します。</span><span class="sxs-lookup"><span data-stu-id="17689-147">Use the **ProcessScheduleOccurrenceCalendarViewRenderer** class to render the weekly calendar view in an existing form.</span></span> <span data-ttu-id="17689-148">フォーム パーツが作成され、正しく初期化されます。</span><span class="sxs-lookup"><span data-stu-id="17689-148">A form part will be created and correctly initialized.</span></span> <span data-ttu-id="17689-149">このクラスの例は、**ProcessScheduleSeries** フォームで使用されます。</span><span class="sxs-lookup"><span data-stu-id="17689-149">An example of this class is used in the **ProcessScheduleSeries** form.</span></span>

| <span data-ttu-id="17689-150">メソッド</span><span class="sxs-lookup"><span data-stu-id="17689-150">Method</span></span> | <span data-ttu-id="17689-151">説明</span><span class="sxs-lookup"><span data-stu-id="17689-151">Description</span></span> |
|---|---|
| `public static ProcessScheduleICalendarView renderCalendarViewInFormControl(FormGroupControl _containingGroupControl)` | <span data-ttu-id="17689-152">このメソッドは、指定されたフォーム グループ コントロールの週ごとのカレンダー表示をレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="17689-152">This method renders the weekly calendar view in the specified form group control.</span></span> |

### <a name="render-interfaces"></a><span data-ttu-id="17689-153">インターフェースのレンダリング</span><span class="sxs-lookup"><span data-stu-id="17689-153">Render interfaces</span></span>

<span data-ttu-id="17689-154">さまざまなインターフェイスを使用して、カレンダー表示で発生プロセスを表示する方法をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="17689-154">Several interfaces enable customization of the way that occurrence processes are rendered in the calendar view.</span></span> <span data-ttu-id="17689-155">プロセスが保持できる状態ごとに、次のようなインターフェイスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="17689-155">There is one interface for each status that a process can have:</span></span>

- <span data-ttu-id="17689-156">ProcessScheduleIRenderDisabledOccurrenceCard</span><span class="sxs-lookup"><span data-stu-id="17689-156">ProcessScheduleIRenderDisabledOccurrenceCard</span></span>
- <span data-ttu-id="17689-157">ProcessScheduleIRenderFailedOccurrenceCard</span><span class="sxs-lookup"><span data-stu-id="17689-157">ProcessScheduleIRenderFailedOccurrenceCard</span></span>
- <span data-ttu-id="17689-158">ProcessScheduleIRenderRunningOccurrenceCard</span><span class="sxs-lookup"><span data-stu-id="17689-158">ProcessScheduleIRenderRunningOccurrenceCard</span></span>
- <span data-ttu-id="17689-159">ProcessScheduleIRenderScheduledOccurrenceCard</span><span class="sxs-lookup"><span data-stu-id="17689-159">ProcessScheduleIRenderScheduledOccurrenceCard</span></span>
- <span data-ttu-id="17689-160">ProcessScheduleIRenderSuccessfulOccurrenceCard</span><span class="sxs-lookup"><span data-stu-id="17689-160">ProcessScheduleIRenderSuccessfulOccurrenceCard</span></span>
- <span data-ttu-id="17689-161">ProcessScheduleIRenderWaitingOccurrenceCard</span><span class="sxs-lookup"><span data-stu-id="17689-161">ProcessScheduleIRenderWaitingOccurrenceCard</span></span>

<span data-ttu-id="17689-162">これらのインターフェイスはすべて同じパターンに従います。</span><span class="sxs-lookup"><span data-stu-id="17689-162">All these interfaces follow the same pattern.</span></span> <span data-ttu-id="17689-163">**ProcessScheduleOccurrenceCardRendering** のインスタンスがそれらに送信されます。</span><span class="sxs-lookup"><span data-stu-id="17689-163">An instance of **ProcessScheduleOccurrenceCardRendering** is sent to them.</span></span> <span data-ttu-id="17689-164">このインスタンスは、オカレンス カードの表示方法を制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="17689-164">That instance is used to control how the occurrence card is rendered.</span></span>

<span data-ttu-id="17689-165">例については、AOTの **CustVendPaymProposalAutomationOccurrenceCardRenderer** クラスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="17689-165">For an example, see the **CustVendPaymProposalAutomationOccurrenceCardRenderer** class in the AOT.</span></span>

### <a name="processscheduleoccurrencecardrendering-class"></a><span data-ttu-id="17689-166">ProcessScheduleOccurrenceCardRendering クラス</span><span class="sxs-lookup"><span data-stu-id="17689-166">ProcessScheduleOccurrenceCardRendering class</span></span>

| <span data-ttu-id="17689-167">メソッド</span><span class="sxs-lookup"><span data-stu-id="17689-167">Method</span></span> | <span data-ttu-id="17689-168">説明</span><span class="sxs-lookup"><span data-stu-id="17689-168">Description</span></span> |
|---|---|
| `public ProcessScheduleOccurrence getOccurrenceBeingRendered()` | <span data-ttu-id="17689-169">このメソッドは、オカレンス カードに表示されているオカレンスを返します。</span><span class="sxs-lookup"><span data-stu-id="17689-169">This method returns the occurrence that is being rendered on the occurrence card.</span></span> |
| `public ProcessExecutionExecutingInformation getOccurrenceExecutionInformation()` | <span data-ttu-id="17689-170">このメソッドは、発生したオカレンスの実行情報を返します。</span><span class="sxs-lookup"><span data-stu-id="17689-170">This method returns the running information for the occurrence.</span></span> <span data-ttu-id="17689-171">通常、この情報には、バッチ ジョブ、開始時刻、および終了時刻の結果が含まれます。</span><span class="sxs-lookup"><span data-stu-id="17689-171">This information typically includes the results of the batch job, the start time, and the end time.</span></span> |
| `public void makeCardSubHeaderInvisible()` | <span data-ttu-id="17689-172">このメソッドによって、カードのサブヘッダーが非表示になります。</span><span class="sxs-lookup"><span data-stu-id="17689-172">This method makes the card's subheader invisible.</span></span> <span data-ttu-id="17689-173">このトピックの前の図と下の内容を参照して、どの行がサブヘッダーであるかを決定してください。</span><span class="sxs-lookup"><span data-stu-id="17689-173">See the illustration earlier in this topic and the content below it to determine which line is the subheader.</span></span> |
| `public void makeCardButtonsInvisible()` | <span data-ttu-id="17689-174">このメソッドは、オカレンス カードの **無効化** および **編集** ボタンを非表示にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="17689-174">This method specifies whether the **Disable** and **Edit** buttons on the occurrence card are invisible.</span></span> |
| `public void setColumnsOnOccurrenceCardDetailGroup(int _numberOfColumns)` | <span data-ttu-id="17689-175">この方法を使用すると、オカレンス カードの列の数をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="17689-175">This method enables the number of columns on the occurrence card to be customized.</span></span> <span data-ttu-id="17689-176">既定では、2 つの列があります。</span><span class="sxs-lookup"><span data-stu-id="17689-176">By default, there are two columns.</span></span> |
| `public FormButtonControl addButtonControl(FormControlName _buttonControlName)` | <span data-ttu-id="17689-177">このメソッドを使用すると、新しいボタンをオカレンス カードに追加できます。</span><span class="sxs-lookup"><span data-stu-id="17689-177">This method enables a new button to be added to the occurrence card.</span></span> |
| `public FormStaticTextControl addStaticTextControl(FormControlName _staticTextControlName)` | <span data-ttu-id="17689-178">このメソッドを使用すると、静的テキスト コントロールをオカレンス カードに追加できます。</span><span class="sxs-lookup"><span data-stu-id="17689-178">This method enables a static text control to be added to the occurrence card.</span></span> |
| `public FormStringControl addStringControl(FormControlName _stringControlName, LabelId _stringControlLabel)` | <span data-ttu-id="17689-179">このメソッドは、オカレンス カードに文字列コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="17689-179">This method adds a string control to the occurrence card.</span></span> |

## <a name="series-list-page"></a><span data-ttu-id="17689-180">リスト ページのシリーズ</span><span class="sxs-lookup"><span data-stu-id="17689-180">Series list page</span></span>

### <a name="processscheduleiseriesformcontroller-interface"></a><span data-ttu-id="17689-181">ProcessScheduleISeriesFormController インターフェイス</span><span class="sxs-lookup"><span data-stu-id="17689-181">ProcessScheduleISeriesFormController interface</span></span>

<span data-ttu-id="17689-182">**シリーズ** リスト ページでは、**ProcessScheduleISeriesFormController** コントローラーを使用して、**ProcessScheduleSeries** リスト ページに表示するタイプのシリーズを決定します。</span><span class="sxs-lookup"><span data-stu-id="17689-182">The **Series** list page uses the **ProcessScheduleISeriesFormController** controller to determine which types series will be shown for on the **ProcessScheduleSeries** list page.</span></span> <span data-ttu-id="17689-183">このクラスは **SysPlugin** クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="17689-183">This class uses the **SysPlugIn** class.</span></span> <span data-ttu-id="17689-184">**ProcessScheduleSeries** フォームを開くために使用するメニュー項目は、指定されたプラグインを呼び出すためのキーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="17689-184">The menu item that you use to open the **ProcessScheduleSeries** form is used as the key to invoke the specified plug-in.</span></span> <span data-ttu-id="17689-185">このキーを使用すると、このフォームを使用して、表示するタイプをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="17689-185">This key enables each use of this form to customize which types are shown.</span></span>

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

### <a name="processscheduleseriesformcontract-class"></a><span data-ttu-id="17689-186">ProcessScheduleSeriesFormContract クラス</span><span class="sxs-lookup"><span data-stu-id="17689-186">ProcessScheduleSeriesFormContract class</span></span>

<span data-ttu-id="17689-187">**ProcessScheduleSeriesFormContract** クラスは、シリーズ リスト ページで **ProcessScheduleType** の表示を決定するために使用される契約です。</span><span class="sxs-lookup"><span data-stu-id="17689-187">The **ProcessScheduleSeriesFormContract** class is a contract that the series list page uses to determine which **ProcessScheduleType** is shown on it.</span></span> <span data-ttu-id="17689-188">このクラスは、ワークスペースで、そのワークスペースに関連付けられている特定のタイプについてのみシリーズを表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="17689-188">This class can be used in a workspace to show series only for specific types that are related to that workspace.</span></span>

| <span data-ttu-id="17689-189">メソッド</span><span class="sxs-lookup"><span data-stu-id="17689-189">Method</span></span> | <span data-ttu-id="17689-190">説明</span><span class="sxs-lookup"><span data-stu-id="17689-190">Description</span></span> |
|---|---|
| `public void addScheduledScheduleType(ProcessScheduleTypeName _scheduleTypeName)` | <span data-ttu-id="17689-191">特定のスケジュールされたタイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="17689-191">Add a specific scheduled type.</span></span> |
| `public void addPolledScheduleType(ProcessScheduleTypeName _scheduleTypeName)` | <span data-ttu-id="17689-192">特定のポーリングされたタイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="17689-192">Add a specific polled type.</span></span> |

## <a name="results-and-messages"></a><span data-ttu-id="17689-193">結果とメッセージ</span><span class="sxs-lookup"><span data-stu-id="17689-193">Results and messages</span></span>

### <a name="processexecutioniresultscontroller-interface"></a><span data-ttu-id="17689-194">ProcessExecutionIResultsController インターフェイス</span><span class="sxs-lookup"><span data-stu-id="17689-194">ProcessExecutionIResultsController interface</span></span>

<span data-ttu-id="17689-195">**ProcessExecutionIResultsController** インターフェイスを使用すると、プロセスに従って結果ダイアログ ボックスをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="17689-195">The **ProcessExecutionIResultsController** interface lets you customize the results dialog box according to your process.</span></span> <span data-ttu-id="17689-196">これにより、結果グリッドで **ヘッダー** フィールドの列ヘッダー ラベルを設定して、ヘッダー列の値をハイパーリンクにすることができます。</span><span class="sxs-lookup"><span data-stu-id="17689-196">It lets you set the column header label for the **Header** field in the results grid and make the value in the header column a hyperlink.</span></span> <span data-ttu-id="17689-197">このインターフェイスは、プラグインであるクラスによって実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17689-197">This interface should be implemented by a class that is a plug-in.</span></span> <span data-ttu-id="17689-198">サンプル プラグインを次に示します。</span><span class="sxs-lookup"><span data-stu-id="17689-198">Here is a sample plug-in.</span></span>

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

| <span data-ttu-id="17689-199">メソッド</span><span class="sxs-lookup"><span data-stu-id="17689-199">Method</span></span> | <span data-ttu-id="17689-200">説明</span><span class="sxs-lookup"><span data-stu-id="17689-200">Description</span></span> |
|---|---|
| `ProcessExecutionResultsDialogContract getResultsDialogContract()` | <span data-ttu-id="17689-201">**ProcessExecutionResultsDialogContract** のインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="17689-201">Return an instance of **ProcessExecutionResultsDialogContract**.</span></span> |
| `void openSourceLinkDetails(RefTableId _refTableId, RefRecId _refRecId)` | <span data-ttu-id="17689-202">渡されたレコードを表示できる適切なメニュー項目を開くロジックを実装します。</span><span class="sxs-lookup"><span data-stu-id="17689-202">Implement the logic to open the appropriate menu item that can show the record that is passed in.</span></span> |

### <a name="processexecutionresultsdialogcontract-class"></a><span data-ttu-id="17689-203">ProcessExecutionResultsDialogContract クラス</span><span class="sxs-lookup"><span data-stu-id="17689-203">ProcessExecutionResultsDialogContract class</span></span>

<span data-ttu-id="17689-204">**ProcessExecutionResultsDialogContract** クラスを使用すると、ヘッダー列ラベルをカスタマイズして、ヘッダー列のデータをハイパーリンクとして表示するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="17689-204">The **ProcessExecutionResultsDialogContract** class lets you customize the header column label and specify whether the data in the header column should be rendered as a hyperlink.</span></span>

| <span data-ttu-id="17689-205">メソッド</span><span class="sxs-lookup"><span data-stu-id="17689-205">Method</span></span> | <span data-ttu-id="17689-206">説明</span><span class="sxs-lookup"><span data-stu-id="17689-206">Description</span></span> |
|---|---|
| `public static ProcessExecutionResultsDialogContract newForSourceLinkHeader(LabelId _sourceLinkHeaderLabel, boolean _shouldSourceLinkHeaderBeLinkToSourceLinkDetails)` | <span data-ttu-id="17689-207">ヘッダー列ラベルとして使用するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="17689-207">Provide the text that should be used as a header column label.</span></span> <span data-ttu-id="17689-208">また、ヘッダー列の値をハイパーリンクとして表示するかどうかを示すブール値を提供します。</span><span class="sxs-lookup"><span data-stu-id="17689-208">Also provide a Boolean value that indicates whether the value in the header column should be rendered as a hyperlink.</span></span> |
| `public LabelId parmExecutionResultsDialogCaption(LabelId _executionResultsDialogCaption = executionResultsDialogCaption)` | <span data-ttu-id="17689-209">このメソッドは、結果ダイアログ ボックスのキャプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="17689-209">This method sets the caption for the results dialog box.</span></span> |

### <a name="processexecutionmessagelogdialog-class"></a><span data-ttu-id="17689-210">ProcessExecutionMessageLogDialog クラス</span><span class="sxs-lookup"><span data-stu-id="17689-210">ProcessExecutionMessageLogDialog class</span></span>

<span data-ttu-id="17689-211">**ProcessExecutionMessageLogDialog** インターフェイスを使用すると、メッセージ ログを移行元ドメインの内容のコンテキストで開くことができます。</span><span class="sxs-lookup"><span data-stu-id="17689-211">The **ProcessExecutionMessageLogDialog** interface enables the message log to be opened in the context of something from the source domain.</span></span> <span data-ttu-id="17689-212">たとえば、転記済仕入先請求書ページからメッセージ ログを開いて、プロセス自動化フレームワークに対して有効になっているプロセスによって仕入先請求書が転記されている間にログに記録されたメッセージを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="17689-212">For example, the message log can be opened from the page for a posted vendor invoice to show the messages that were logged while the vendor invoice was being posted by a process that is enabled for the process automation framework.</span></span> <span data-ttu-id="17689-213">この例では、転記済仕入先請求書ページで **ProcessExecutionMessageLogDialog** インターフェースを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17689-213">For this example, the posted vendor invoice page must implement the **ProcessExecutionMessageLogDialog** interface.</span></span> <span data-ttu-id="17689-214">このインターフェイスを使用することにより、独自のプライベート結果/メッセージング サブシステムを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="17689-214">By using this interface, you don't have to build your own private results/messaging subsystems.</span></span>

| <span data-ttu-id="17689-215">メソッド</span><span class="sxs-lookup"><span data-stu-id="17689-215">Method</span></span> | <span data-ttu-id="17689-216">説明</span><span class="sxs-lookup"><span data-stu-id="17689-216">Description</span></span> |
|---|---|
| `ProcessExecutionMessageLogContract getContractForMessageLog()` | <span data-ttu-id="17689-217">このメソッドは、**ProcessExecutionMessageLogContract** のインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="17689-217">This method returns an instance of **ProcessExecutionMessageLogContract**.</span></span> |

### <a name="processexecutionmessagelogcontract-class"></a><span data-ttu-id="17689-218">ProcessExecutionMessageLogContract クラス</span><span class="sxs-lookup"><span data-stu-id="17689-218">ProcessExecutionMessageLogContract class</span></span>

<span data-ttu-id="17689-219">**ProcessExecutionMessageLogContract** 契約を使用すると、メッセージ ログを移行元ドメインの特定の項目に制限できます。</span><span class="sxs-lookup"><span data-stu-id="17689-219">The **ProcessExecutionMessageLogContract** contract lets you limit the message log to a specific item from the source domain.</span></span> <span data-ttu-id="17689-220">**ProcessExecutionSourceLink** テーブルには、**RefRecId** および **RefTableId** 値が契約によって送られる値と一致しているレコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="17689-220">In the **ProcessExecutionSourceLink** table, there must be a record where the **RefRecId** and **RefTableId** values match the values that the contract sends.</span></span>

| <span data-ttu-id="17689-221">メソッド</span><span class="sxs-lookup"><span data-stu-id="17689-221">Method</span></span> | <span data-ttu-id="17689-222">説明</span><span class="sxs-lookup"><span data-stu-id="17689-222">Description</span></span> |
|---|---|
| `public static ProcessExecutionMessageLogContract newForSourceRecord(ProcessScheduleTypeName _typeName, RefTableId _refTableId, RefRecId _refRecId, guid _executionId = emptyGuid())` | <span data-ttu-id="17689-223">このメソッドは、指定された型名、**RefTableld** 値、および **RefRecld** 値を使用して契約を初期化します。</span><span class="sxs-lookup"><span data-stu-id="17689-223">This method initializes the contract by using the specified type name, **RefTableId** value, and **RefRecId** value.</span></span> <span data-ttu-id="17689-224">**ProcessExecutionSourceLink** テーブルには一致するレコ―ドが存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="17689-224">There should be a matching record in the **ProcessExecutionSourceLink** table.</span></span> <span data-ttu-id="17689-225">バックグラウンド プロセスには、複数の実行 ID が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="17689-225">Background processes will have multiple execution IDs.</span></span> <span data-ttu-id="17689-226">したがって、実行 ID の省略可能なパラメーターをバックグラウンド処理用に提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17689-226">Therefore, the optional parameter for the execution ID should be provided for background processes.</span></span> <span data-ttu-id="17689-227">詳細については、[タイプ登録](type-registration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17689-227">For more information, see [Type registration](type-registration.md).</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]