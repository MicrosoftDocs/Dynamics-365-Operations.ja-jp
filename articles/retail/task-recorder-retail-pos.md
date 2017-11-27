---
title: "POS のタスク レコーダーとヘルプ"
description: "このトピックでは、Retail Modern POS およびクラウド POS のタスク レコーダーを使用する方法を説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a527136f77b65ef5a43576291e38cb168dbbd322
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="task-recorder-and-help-for-pos"></a><span data-ttu-id="b4df3-103">POS のタスク レコーダーとヘルプ</span><span class="sxs-lookup"><span data-stu-id="b4df3-103">Task recorder and Help for POS</span></span>

<span data-ttu-id="b4df3-104">このトピックでは、Retail Modern POS およびクラウド POS のタスク レコーダーを使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="b4df3-105">概要</span><span class="sxs-lookup"><span data-stu-id="b4df3-105">Overview</span></span>
--------

<span data-ttu-id="b4df3-106">Retail Modern POS またはクラウド POS のタスク レコーダーは、高い応答性に焦点を当てて構築された新しいソリューションです。</span><span class="sxs-lookup"><span data-stu-id="b4df3-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="b4df3-107">業務プロセスを記録する消費者向けに、拡張性とシームレスな統合のための柔軟なアプリケーション プログラミング インターフェイス (API) を提供します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="b4df3-108">さらに、Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) で業務プロセス モデル (BPM) ツールと統合されたタスク レコーダーが公開されました。</span><span class="sxs-lookup"><span data-stu-id="b4df3-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="b4df3-109">そのため、ユーザーは、引き続き記録からリッチな業務プロセス ダイアグラムを作成してアプリケーションを分析、設計できます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="b4df3-110">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="b4df3-110">Architecture</span></span>
<span data-ttu-id="b4df3-111">タスク レコーダーは、正確な再現性でクライアントでのユーザー アクションを記録できます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="b4df3-112">各コントロールが計測され、ユーザー アクションの実行についてタスク レコーダーに通知されます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="b4df3-113">コントロールは、イベントが発生したことをタスク レコーダーを通知し、該当するユーザー アクションに関するすべての関連情報をリアルタイムで渡します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="b4df3-114">タスク レコーダーは、この情報からユーザー アクションのタイプ (ボタンのクリック、値の入力、ナビゲーションなど) と、ユーザー アクションに関連するデータ (入力データの値とタイプ、フォーム コンテキスト、レコード コンテキストなど) をキャプチャできます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="b4df3-115">タスク レコーダーは、記録の再生で、記録されたアクションをユーザーが実行したとおりに実行できることを保証するために役立つ十分な詳細とともに、情報を保持します </span><span class="sxs-lookup"><span data-stu-id="b4df3-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="b4df3-116">(再生機能はまだ Retail Modern POS またはクラウド POS で実装されていません)。</span><span class="sxs-lookup"><span data-stu-id="b4df3-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="b4df3-117">基本コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b4df3-117">Basic configuration</span></span>
<span data-ttu-id="b4df3-118">POS でタスク記録を有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b4df3-118">To enable task recording in POS, follow these steps.</span></span>

1.  <span data-ttu-id="b4df3-119"> [**小売**] &gt; [**チャネル設定**] &gt; [**POS 設定**] &gt; [**レジスター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-119">Click **Retail** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2.  <span data-ttu-id="b4df3-120">レジスターをクリックしてタスクの記録を有効にします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-120">Click the register to enable task recording on.</span></span>
3.  <span data-ttu-id="b4df3-121">[**登録**] タブの [**全般**] クイック タブで、[**タスク記録の有効化**] オプションを [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4.  <span data-ttu-id="b4df3-122">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-122">Click **Save**.</span></span>
5.  <span data-ttu-id="b4df3-123">[**小売**] &gt; [**小売 IT**] &gt; [**配送スケジュール**] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-123">Go to **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
6.  <span data-ttu-id="b4df3-124">[**1090 レジスター**] ジョブを選択し、[**今すぐ実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="b4df3-125">記録の作成</span><span class="sxs-lookup"><span data-stu-id="b4df3-125">Create a recording</span></span>
<span data-ttu-id="b4df3-126">次の手順に従い、タスク レコーダーを使用して新しい記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-126">Follow these steps to create a new recording using Task recorder.</span></span>

1.  <span data-ttu-id="b4df3-127">Retail Modern POS またはクラウド POS を起動し、サインインします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2.  <span data-ttu-id="b4df3-128">[**設定**] ページの [**タスク レコーダー**] セクションで、[**タスク レコーダーを開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="b4df3-129">[**タスク レコーダー**] ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="b4df3-130">右上隅の [**閉じる**] ボタン (**X**) をクリックして [**タスク レコーダー**] ウィンドウを閉じてから、新しい記録を開始します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="b4df3-131">ウィンドウをもう一度開くには、手順 2 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-131">To reopen the pane, repeat step 2.</span></span>
<span data-ttu-id="b4df3-132">[![[タスク レコーダー] ウィンドウ](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="b4df3-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3.  <span data-ttu-id="b4df3-133">記録の名前と説明を入力し、[**開始**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="b4df3-134">[**開始**] をクリックするとすぐに記録セッションが開始されます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-134">The recording session begins as soon as you click **Start**.</span></span>

<span data-ttu-id="b4df3-135">**注記:** 記録中に右上隅の [**閉じる**] ボタン (**X**) をクリックすると、[**タスク レコーダー**] ウィンドウが閉じられますが、記録セッションは終了されません。</span><span class="sxs-lookup"><span data-stu-id="b4df3-135">**Note:** If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="b4df3-136">[タスク レコーダー] ウィンドウを再度開くには、画面の上部にある [**ヘルプ**] ボタン (疑問符) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span> 

<span data-ttu-id="b4df3-137">[![疑問符](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="b4df3-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4.  <span data-ttu-id="b4df3-138">[**開始**] をクリックすると、タスク レコーダーは記録モードになります。</span><span class="sxs-lookup"><span data-stu-id="b4df3-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="b4df3-139">[**タスク レコーダー**] ウィンドウには、記録プロセスに関連付けられている情報とコントロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5.  <span data-ttu-id="b4df3-140">Retail Modern POS またはクラウド POS ユーザー インターフェイス (UI) で、目的のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6.  <span data-ttu-id="b4df3-141">記録セッションを終了するには、[**停止**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="b4df3-142">ダウンロード オプション</span><span class="sxs-lookup"><span data-stu-id="b4df3-142">Download options</span></span>
<span data-ttu-id="b4df3-143">記録セッションを終了すると、いくつかのオプションが表示され、記録をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span> 
<span data-ttu-id="b4df3-144">[![ダウンロード オプション](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="b4df3-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="b4df3-145">この PC に保存</span><span class="sxs-lookup"><span data-stu-id="b4df3-145">Save to this PC</span></span>

<span data-ttu-id="b4df3-146">記録パッケージを使用して、タスク ガイドの再生、記録の管理、または記録の注釈の編集を行うことができます </span><span class="sxs-lookup"><span data-stu-id="b4df3-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="b4df3-147">(この機能はまだ Retail Modern POS およびクラウド POS で実装されていません)。</span><span class="sxs-lookup"><span data-stu-id="b4df3-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="b4df3-148">Word ドキュメントとしてエクスポート</span><span class="sxs-lookup"><span data-stu-id="b4df3-148">Export as Word document</span></span>

<span data-ttu-id="b4df3-149">記録を Microsoft Word 文書として保存できます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="b4df3-150">このドキュメントには、記録されたステップとキャプチャされたスクリーンショットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="b4df3-151">開発者の記録として保存</span><span class="sxs-lookup"><span data-stu-id="b4df3-151">Save as developer recording</span></span>

<span data-ttu-id="b4df3-152">未加工の記録ファイルは、テスト コードの生成などの開発者シナリオに役立ちます </span><span class="sxs-lookup"><span data-stu-id="b4df3-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="b4df3-153">(この機能はまだ実装されていません)。</span><span class="sxs-lookup"><span data-stu-id="b4df3-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="b4df3-154">記録コントロール</span><span class="sxs-lookup"><span data-stu-id="b4df3-154">Recording controls</span></span>
### <a name="recording-controlsmediacontrolsjpgmediacontrolsjpg"></a><span data-ttu-id="b4df3-155">[![記録コントロール](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="b4df3-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="b4df3-156">停止</span><span class="sxs-lookup"><span data-stu-id="b4df3-156">Stop</span></span>

<span data-ttu-id="b4df3-157">記録セッションを終了するには、[**停止**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="b4df3-158">終了後にセッションを再起動することはできません。</span><span class="sxs-lookup"><span data-stu-id="b4df3-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="b4df3-159">そのため、記録が完了したことを確認してから終了してください。</span><span class="sxs-lookup"><span data-stu-id="b4df3-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="b4df3-160">一時停止</span><span class="sxs-lookup"><span data-stu-id="b4df3-160">Pause</span></span>

<span data-ttu-id="b4df3-161">[**一時停止**] をクリックして記録セッションを一時的に中止 (一時停止) し、操作を続行します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="b4df3-162">[**一時停止**] をクリックした後で実行するステップは記録されません。</span><span class="sxs-lookup"><span data-stu-id="b4df3-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="b4df3-163">続行</span><span class="sxs-lookup"><span data-stu-id="b4df3-163">Continue</span></span>

<span data-ttu-id="b4df3-164">一時停止後に記録セッションを再開するには、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="b4df3-165">スクリーンショットのキャプチャ</span><span class="sxs-lookup"><span data-stu-id="b4df3-165">Capture screenshots</span></span>

<span data-ttu-id="b4df3-166">タスク レコーダーは、業務プロセスを記録するときに Retail Modern POS UI のスクリーンショットをキャプチャできます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="b4df3-167">Word 文書として記録をダウンロードする場合、タスク レコーダーはスクリーンショットを使用します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-167">Task recorder uses the screenshots if you download the recording as a Word document.</span></span> <span data-ttu-id="b4df3-168">スクリーンショットのキャプチャ機能を有効にするには、[**スクリーンショットをキャプチャ**] オプションを [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-168">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes**.</span></span> 

#### <a name="note"></a><span data-ttu-id="b4df3-169">注記</span><span class="sxs-lookup"><span data-stu-id="b4df3-169">Note</span></span>
> <span data-ttu-id="b4df3-170">クラウド POS ではスクリーンショットのキャプチャ機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b4df3-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="b4df3-171">タスクの開始と終了</span><span class="sxs-lookup"><span data-stu-id="b4df3-171">Start task and End task</span></span>

<span data-ttu-id="b4df3-172">[**タスクの開始**] と [**タスクの終了******] ボタンを使用して、グループ化されたステップの開始と終了を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="b4df3-173">[**タスクの開始**] をクリックして "タスクの開始" ステップを追加し、グループに含めるステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-173">Click **Start task** to add a “Start Task” step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="b4df3-174">グループのステップの実行を終了したら、[**タスクの終了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="b4df3-175">タスクは手順を整理するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="b4df3-176">タスクはその他のタスク内で入れ子にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="b4df3-177">この方法を使用すると、非常に長く複雑な業務プロセスをさらに上手に整理できます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="b4df3-178">注釈の追加</span><span class="sxs-lookup"><span data-stu-id="b4df3-178">Adding annotations</span></span>
<span data-ttu-id="b4df3-179">注釈は、記録でステップに追加するテキストです。</span><span class="sxs-lookup"><span data-stu-id="b4df3-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="b4df3-180">たとえば、注釈を使用して、詳細なコンテキストや指示をユーザーに与えることができます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="b4df3-181">注釈はステップの前後に追加できます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="b4df3-182">ステップの右側にある [**編集**] ボタン (鉛筆のアイコン) をクリックして、任意のステップに注釈を追加できます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span> 

<span data-ttu-id="b4df3-183">[![ステップの [編集] ボタン](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="b4df3-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="b4df3-184">テキストとメモ</span><span class="sxs-lookup"><span data-stu-id="b4df3-184">Texts and notes</span></span>

<span data-ttu-id="b4df3-185">[**テキスト**] および [**メモ**] フィールドを使用して、タスク ガイドのステップに関連付けるテキストを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>
<span data-ttu-id="b4df3-186">[![[テキスト] および [メモ] フィールド](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="b4df3-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="b4df3-187">テキスト</span><span class="sxs-lookup"><span data-stu-id="b4df3-187">Text</span></span>

<span data-ttu-id="b4df3-188">[**テキスト**] フィールドに入力するテキストは、タスク ガイドのステップのテキストの*上*に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="b4df3-189">この場所は、ステップを完了する前にユーザーに読んでもらいたいテキストに適しています。</span><span class="sxs-lookup"><span data-stu-id="b4df3-189">This location is appropriate for text that you want the user to read before he or she completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="b4df3-190">摘要</span><span class="sxs-lookup"><span data-stu-id="b4df3-190">Notes</span></span>

<span data-ttu-id="b4df3-191">[**メモ**] フィールドに入力するテキストは、タスク ガイドのステップのテキストの*下*に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="b4df3-192">メモのテキストを読み取るには、ユーザーはポップアップ ウィンドウでステップのテキストを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4df3-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="b4df3-193">この場所は、ユーザーにとって役立つ可能性があるが、アクションを完了するために必要とはしない、オプションの参考資料またはその他の情報に適しています。</span><span class="sxs-lookup"><span data-stu-id="b4df3-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="b4df3-194">Retail Modern POS およびクラウド POS のヘルプ</span><span class="sxs-lookup"><span data-stu-id="b4df3-194">Help in Retail Modern POS and Cloud POS</span></span>
<span data-ttu-id="b4df3-195">独自のタスク記録をテキストとして表示するために、Retail Modern POS およびクラウド POS の [ヘルプ] ウィンドウに表示するには、タスク記録を BPM ライブラリに保存して、ヘルプ システム パラメーターを BPM ライブラリにポイントするように更新します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="b4df3-196">詳細については、「[ヘルプ システムの接続](../fin-and-ops/get-started/help-connect.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4df3-196">For more information, see [Connecting the Help system](../fin-and-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="b4df3-197">Retail Modern POS およびクラウド POS のヘルプでは、リアルタイムで LCS を検索します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="b4df3-198">Microsoft Dynamics 365 for Retail のヘルプ システムのパラメーターで選択されているすべての BPM ライブラリを検索し、関連する結果を示します。</span><span class="sxs-lookup"><span data-stu-id="b4df3-198">It searches across all the BPM libraries that are selected in the Microsoft Dynamics 365 for Retail Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="b4df3-199">[**ヘルプ**] メニューにアクセスするには、画面の上部にある [**ヘルプ**] ボタン (疑問符) をクリックし、検索ボックスにプロセス名を入力して、検索ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4df3-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span> 

<span data-ttu-id="b4df3-200">[![ヘルプ ボタン](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="b4df3-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span> 

<span data-ttu-id="b4df3-201">検索結果でタスク ガイドをクリックするときは、ヘルプ トピックとしてステップを表示するか、Word 文書にステップをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="b4df3-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span> 
#### <a name="note"></a><span data-ttu-id="b4df3-202">注記</span><span class="sxs-lookup"><span data-stu-id="b4df3-202">Note</span></span>
> <span data-ttu-id="b4df3-203">Retail Modern POS およびクラウド POS のヘルプ システムでは、使用しているフォームまたは行っている操作によるタスク ガイドは表示されません。</span><span class="sxs-lookup"><span data-stu-id="b4df3-203">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="b4df3-204">検索ボックスにプロセス名を入力して**検索**ボタンをクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4df3-204">You have to type the process name in the search box and then click **Search**.</span></span>


