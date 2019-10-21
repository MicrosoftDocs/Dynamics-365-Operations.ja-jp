---
title: Retail Cloud POS 用のレコーダーおよRegression Suite Automation Tool のテスト
description: このトピックでは、POS テスト レコーダーと Regression Suite Automation Tool (RSAT) を使用して、ユーザー受け入れテスト (UAT) を自動化する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 10/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-08-2019
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 6eb379396a68a907a0880e630ee99fd9480cf01c
ms.sourcegitcommit: 7b74425637ddcf02087f1d391755e5cb8ce25949
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/05/2019
ms.locfileid: "2559202"
---
# <a name="test-recorder-and-regression-suite-automation-tool-for-retail-cloud-pos"></a><span data-ttu-id="1355c-103">Retail Cloud POS 用のレコーダーおよRegression Suite Automation Tool のテスト</span><span class="sxs-lookup"><span data-stu-id="1355c-103">Test recorder and Regression suite automation tool for Retail Cloud POS</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1355c-104">このトピックでは、Retail Cloud POS の新しいテスト レコーダー ツールを使用して、ユーザー受け入れテスト (UAT) とユーザー インターフェイス (UI) テストのビジネス シナリオを記録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1355c-104">This topic explains how to use the new test recorder tool in Retail Cloud POS to record business scenarios for user acceptance testing (UAT) and user interface (UI) testing.</span></span> <span data-ttu-id="1355c-105">また、Regression Suite Automation Tool (RSAT) を使用してテストの検証を自動化する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="1355c-105">It also explains how to automate test validation by using the Regression suite automation tool (RSAT).</span></span> <span data-ttu-id="1355c-106">RSAT では、Microsoft Azure DevOps のテスト スイートを使用してテスト ケースをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1355c-106">RSAT uses the Microsoft Azure DevOps test suite to download test cases.</span></span> <span data-ttu-id="1355c-107">次に、テストの実行ステータスと共に、結果が Azure DevOps に報告されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-107">It then reports the results, together with the test execution status, back to Azure DevOps.</span></span> <span data-ttu-id="1355c-108">テスト ケースは、Azure DevOps で手動で作成するか、または Microsoft Dynamics Lifecycle Services (LCS) の ビジネス プロセス モデラー (BPM) ツール から Azure DevOps に同期してから、RSAT に同期することができます。</span><span class="sxs-lookup"><span data-stu-id="1355c-108">The test cases can be manually created in Azure DevOps, or they can be synced from the Business process modeler (BPM) tool in Microsoft Dynamics Lifecycle Services (LCS) to Azure DevOps and then to RSAT.</span></span>

<span data-ttu-id="1355c-109">このトピックは、Dynamics 365 Retail および Dynamics 365 Finance バージョン 10.0.5 (2019 年 10 月) 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-109">This topic applies to Dynamics 365 Retail and Dynamics 365 Finance version 10.0.5 (October 2019) and later.</span></span>

> [!NOTE]
> <span data-ttu-id="1355c-110">テスト レコーダーは、Google Chrome Web ブラウザーを使用している場合にのみ、Retail Cloud POS でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="1355c-110">The test recorder is supported in Retail Cloud POS only when the Google Chrome web browser is used.</span></span> <span data-ttu-id="1355c-111">その他の Web ブラウザーおよびデバイス タイプのサポートは、今後追加されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-111">Support for other web browsers and device types will be added later.</span></span>

## <a name="test-recorder"></a><span data-ttu-id="1355c-112">テスト レコーダー</span><span class="sxs-lookup"><span data-stu-id="1355c-112">Test recorder</span></span>

<span data-ttu-id="1355c-113">POS のテスト レコーダーは、UAT の時間とコストを大幅に削減するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1355c-113">The test recorder in POS helps significantly reduce the time and cost of UAT.</span></span> <span data-ttu-id="1355c-114">通常、UAT は、Microsoft アプリケーションの更新が適用される前に、またはカスタム コードと構成がユーザーの Retail POS 生産環境に適用される前に必要になります。</span><span class="sxs-lookup"><span data-stu-id="1355c-114">UAT is typically required before a Microsoft application update is applied, or before custom code and configurations are applied to your Retail POS production environments.</span></span>

<span data-ttu-id="1355c-115">テスト レコーダーは、クライアントのユーザー アクションを記録でき、ドキュメント オブジェクト モデル (DOM) 内のすべてのコントロールおよびすべての要素に対する正確な忠実度を提供します。</span><span class="sxs-lookup"><span data-stu-id="1355c-115">The test recorder can record user actions in the client, and it provides exact fidelity for all controls and for all elements in the Document Object Model (DOM).</span></span> <span data-ttu-id="1355c-116">POS で、テスト レコーダーは、発生したイベントを該当するユーザー アクションに関するすべての関連情報と共にキャプチャして、リアルタイムで保存します。</span><span class="sxs-lookup"><span data-stu-id="1355c-116">In POS, the test recorder captures an event that has occurred and stores it, together with all relevant information about the corresponding user action, in real time.</span></span> <span data-ttu-id="1355c-117">テスト レコーダーは、この情報からユーザー アクションのタイプ (ボタンのクリック、値の入力、ナビゲーションなど) と、ユーザー アクションに関連するデータ (入力データの値とタイプ、ビュー コンテキスト、レコード コンテキストなど) をキャプチャできます。</span><span class="sxs-lookup"><span data-stu-id="1355c-117">From this information, the test recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to that user action (such as the value and type of input data, the view context, or the record context).</span></span> <span data-ttu-id="1355c-118">ただし、パスワード情報はキャプチャされません。</span><span class="sxs-lookup"><span data-stu-id="1355c-118">However, password information isn't captured.</span></span> <span data-ttu-id="1355c-119">記録セッション中は、テスト レコーダーによってすべてのレコーダー情報がメモリに保持されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-119">During a recording session, the test recorder persists all the recorder information in memory.</span></span> <span data-ttu-id="1355c-120">その後、記録セッションの終了時に、必要な詳細を含む出力ファイルが生成されます。これにより、RSATを使用してユーザーが実行したときと同じようにアクションを再生できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-120">Then, at the end of the recording session, it generates an output file that includes enough detail so that RSAT can be used later to play back the actions just as the user performed them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1355c-121">テスト レコーダーは、POS ユーザーのパスワードを除く、記録セッション中に入力されたすべてのデータをキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="1355c-121">The test recorder captures all the data that is entered during a recording session except POS user passwords.</span></span> <span data-ttu-id="1355c-122">個人を特定できる情報 (PII)、シークレット、機密性の高いデータ、またはユーザー固有のデータは記録しないでください。</span><span class="sxs-lookup"><span data-stu-id="1355c-122">Don't record any personally identifiable information (PII), secrets, sensitive data, or user-specific data.</span></span> <span data-ttu-id="1355c-123">記録セッション中に入力されたデータはすべて、Recording.xml ファイルに格納されます。その他のユーザーは、LCS および Azure DevOps、variables.xlsx および Recording .xml ファイルの中と、再生中にそのデータを参照できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-123">All data that is entered during a recording session is stored in the Recording.xml file, and other users can see it in LCS and Azure DevOps, in the variables.xlsx and Recording.xml files, and during playback.</span></span>

## <a name="regression-suite-automation-tool"></a><span data-ttu-id="1355c-124">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="1355c-124">Regression suite automation tool</span></span>

<span data-ttu-id="1355c-125">RSAT を使用すると、機能 パワーユーザーは Retail POS でテストケースを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="1355c-125">RSAT lets functional power users run test cases in Retail POS.</span></span> <span data-ttu-id="1355c-126">その後、Azure DevOps のテストの実行結果は、レポートおよび調査のために更新されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-126">It then updates the test execution results in Azure DevOps for reporting and investigation purposes.</span></span>

<span data-ttu-id="1355c-127">RSAT には、テストの失敗を調査するためのオプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="1355c-127">RSAT provides options for investigating test failures.</span></span> <span data-ttu-id="1355c-128">さらに、テスト パラメーターをテスト ステップから切り離して、Microsoft Excel ファイルにパラメーターを格納します。</span><span class="sxs-lookup"><span data-stu-id="1355c-128">It also decouples the test parameters from test steps and stores the parameters in Microsoft Excel files.</span></span> <span data-ttu-id="1355c-129">この方法により、テスト パラメーター値が簡単に編集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="1355c-129">In that way, the values of test parameters can easily be edited.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1355c-130">必要条件</span><span class="sxs-lookup"><span data-stu-id="1355c-130">Prerequisites</span></span>

+ <span data-ttu-id="1355c-131">Retail POS 環境が必要です。</span><span class="sxs-lookup"><span data-stu-id="1355c-131">You must have a Retail POS environment.</span></span>
+ <span data-ttu-id="1355c-132">テスト環境では、バイナリ更新プログラム 10.0.5 以降を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-132">Your test environment must be running binary update 10.0.5 or later.</span></span>
+ <span data-ttu-id="1355c-133">RSAT は、Web ブラウザーを介してテスト環境にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-133">RSAT must have access to your test environment via a web browser.</span></span>
+ <span data-ttu-id="1355c-134">テスト パラメーターを作成および編集するには、Excel をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-134">You must have Excel installed to generate and edit test parameters.</span></span>
+ <span data-ttu-id="1355c-135">テスト ケース、テスト計画、およびテストケースの結果を保存および管理するには、 Azure DevOps プロジェクトが必要です。</span><span class="sxs-lookup"><span data-stu-id="1355c-135">You must have an Azure DevOps project to store and manage your test cases, test plans, and test case results.</span></span>

## <a name="enable-test-recording-in-the-retail-pos-application"></a><span data-ttu-id="1355c-136">Retail POS アプリケーションでのテスト記録の有効化</span><span class="sxs-lookup"><span data-stu-id="1355c-136">Enable test recording in the Retail POS application</span></span>

<span data-ttu-id="1355c-137">Retail POS で記録のテスト機能を有効にするには、Retail Headquarters で次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1355c-137">To turn on the test recording functionality in Retail POS, follow these steps in Retail headquarters.</span></span>

1. <span data-ttu-id="1355c-138"> **小売** &gt; **チャネル設定** &gt; **POS 設定** &gt; **レジスター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1355c-138">Go to **Retail** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="1355c-139">テスト記録機能を有効にする必要があるレジスターを選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-139">Select the register where the test recording functionality should be turned on.</span></span>
3. <span data-ttu-id="1355c-140">**登録** タブの **全般** クイック タブで、**タスクとテスト レコーダーの有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1355c-140">On the **Register** tab, on the **General** FastTab, set the **Enable task and test recorder** option to **Yes**.</span></span>
4. <span data-ttu-id="1355c-141">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-141">Select **Save**.</span></span>
5. <span data-ttu-id="1355c-142">**小売** &gt; **小売 IT** &gt; **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1355c-142">Go to **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="1355c-143">**1090 レジスター** ジョブを選択し、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-143">Select the **Registers (1090)** job, and then select **Run now**.</span></span>

## <a name="controlling-the-test-recorder"></a><span data-ttu-id="1355c-144">テスト レコーダーの制御</span><span class="sxs-lookup"><span data-stu-id="1355c-144">Controlling the test recorder</span></span>

### <a name="open-the-test-recorder"></a><span data-ttu-id="1355c-145">テスト レコーダーを開く</span><span class="sxs-lookup"><span data-stu-id="1355c-145">Open the test recorder</span></span>

<span data-ttu-id="1355c-146">テスト レコーダーを開くには、Retail Cloud POS にログインしてから、**設定**ページの**タスクとテスト レコーダー**セクションで、**テスト レコーダーを開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-146">To open the test recorder, sign in to Retail Cloud POS, and then, on the **Settings** page, in the **Task and Test recorders** section, select **Open test recorder**.</span></span>

<span data-ttu-id="1355c-147">[![タスクおよびテスト レコーダー](./media/CreateTest.png)](./media/CreateTest.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-147">[![Task and Test recorders](./media/CreateTest.png)](./media/CreateTest.png)</span></span>

### <a name="stop-a-recording-session"></a><span data-ttu-id="1355c-148">記録セッションの停止</span><span class="sxs-lookup"><span data-stu-id="1355c-148">Stop a recording session</span></span>

<span data-ttu-id="1355c-149">記録セッションを終了するには、**停止**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-149">To end a recording session, select **Stop**.</span></span> <span data-ttu-id="1355c-150">終了後に記録セッションを再起動することはできません。</span><span class="sxs-lookup"><span data-stu-id="1355c-150">Note that you can't restart a recording session after you end it.</span></span> <span data-ttu-id="1355c-151">そのため、記録セッションが完了したことを確認してから終了してください。</span><span class="sxs-lookup"><span data-stu-id="1355c-151">Therefore, make sure that the recording session is completed before you end it.</span></span>

<span data-ttu-id="1355c-152">[![停止](./media/Stop.png)](./media/Stop.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-152">[![Stop](./media/Stop.png)](./media/Stop.png)</span></span>

### <a name="pause-a-recording-session"></a><span data-ttu-id="1355c-153">記録セッションの一時停止</span><span class="sxs-lookup"><span data-stu-id="1355c-153">Pause a recording session</span></span>

<span data-ttu-id="1355c-154">記録セッションを一時的に停止 (一時停止) するには、**一時停止**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-154">To temporarily stop (pause) a recording session, select **Pause**.</span></span> <span data-ttu-id="1355c-155">**一時停止** を選択した後で実行するステップは記録されません。</span><span class="sxs-lookup"><span data-stu-id="1355c-155">Steps that you perform after you select **Pause** aren't recorded.</span></span>

<span data-ttu-id="1355c-156">[![一時停止](./media/Pause.png)](./media/Pause.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-156">[![Pause](./media/Pause.png)](./media/Pause.png)</span></span>

### <a name="continue-a-recording-session"></a><span data-ttu-id="1355c-157">記録セッションの続行</span><span class="sxs-lookup"><span data-stu-id="1355c-157">Continue a recording session</span></span>

<span data-ttu-id="1355c-158">一時停止後に記録セッションを再開するには、**記録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-158">To resume a recording session after you've paused it, select **Recording**.</span></span>

<span data-ttu-id="1355c-159">[![レコード](./media/Recording.png)](./media/Recording.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-159">[![Recording](./media/Recording.png)](./media/Recording.png)</span></span>

### <a name="start-and-end-a-task"></a><span data-ttu-id="1355c-160">タスクの開始と終了</span><span class="sxs-lookup"><span data-stu-id="1355c-160">Start and end a task</span></span>

<span data-ttu-id="1355c-161">手順を整理するために、ステップをグループ化してタスクにまとめることができます。</span><span class="sxs-lookup"><span data-stu-id="1355c-161">To help organize your procedures, you can group steps together into tasks.</span></span> <span data-ttu-id="1355c-162">グループ化されたステップの開始と終了を指定するには、**タスクの開始**と**タスクの終了**ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="1355c-162">To specify the beginning and end of a set of grouped steps, use the **Start task** and **End task** buttons.</span></span> <span data-ttu-id="1355c-163">**タスクの開始**を選択して「タスクの開始」ステップを追加し、グループに含めるステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="1355c-163">Select **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="1355c-164">グループのステップの実行を終了したら、**タスクの終了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-164">After you've finished performing the steps for the group, select **End task**.</span></span> 

<span data-ttu-id="1355c-165">タスクはその他のタスク内で入れ子にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1355c-165">Tasks can be nested inside other tasks.</span></span> <span data-ttu-id="1355c-166">この方法を使用すると、非常に長く複雑な業務プロセスをさらに上手に整理できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-166">In this way, you can better organize very long and complex business processes.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="1355c-167">[![タスク](./media/StartTask.png)](./media/Recording.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-167">[![Task](./media/StartTask.png)](./media/Recording.png)</span></span>

### <a name="add-a-new-task"></a><span data-ttu-id="1355c-168">新しいタスクの追加</span><span class="sxs-lookup"><span data-stu-id="1355c-168">Add a new task</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="1355c-169">[![新しいタスク](./media/NewTask.png)](./media/NewTask.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-169">[![New task](./media/NewTask.png)](./media/NewTask.png)</span></span>

### <a name="add-an-annotation"></a><span data-ttu-id="1355c-170">注釈の追加</span><span class="sxs-lookup"><span data-stu-id="1355c-170">Add an annotation</span></span>

<span data-ttu-id="1355c-171">注釈は、記録でステップに追加するテキストです。</span><span class="sxs-lookup"><span data-stu-id="1355c-171">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="1355c-172">たとえば、注釈を使用して、詳細なコンテキストや指示をユーザーに与えることができます。</span><span class="sxs-lookup"><span data-stu-id="1355c-172">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="1355c-173">ステップの右側にある **編集** ボタン (鉛筆のアイコン) を選択して、任意のステップに注釈を追加できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-173">You can add an annotation to any step by selecting the **Edit** button (pencil symbol) to the right of the step.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="1355c-174">[![注釈](./media/Annotation.png)](./media/Annotation.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-174">[![Annotation](./media/Annotation.png)](./media/Annotation.png)</span></span>

### <a name="add-text-and-notes"></a><span data-ttu-id="1355c-175">テキストとメモの追加</span><span class="sxs-lookup"><span data-stu-id="1355c-175">Add text and notes</span></span>

<span data-ttu-id="1355c-176">注釈ダイアログ ボックスの**テキスト**および**メモ**フィールドを使用して、タスク ガイドのステップに関連付けるテキストを追加できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-176">You can use the **Text** and **Notes** fields in the annotation dialog box to add text that should be associated with a step in a task guide.</span></span>

+ <span data-ttu-id="1355c-177">**テキスト** – このフィールドに入力するテキストは、テスト ステップにあるステップのテキストの*上*に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-177">**Text** – Text that you enter in this field appears *above* the step text in the test steps.</span></span>
+ <span data-ttu-id="1355c-178">**メモ** – このフィールドに入力するテキストは、LCS のステップのテキストの*下*に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-178">**Notes** – Text that you enter in this field appears *below* the step text in the LCS.</span></span>

### <a name="change-input-values"></a><span data-ttu-id="1355c-179">入力値の変更</span><span class="sxs-lookup"><span data-stu-id="1355c-179">Change input values</span></span>

<span data-ttu-id="1355c-180">記録セッション中に入力されたユーザー入力値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-180">You can change user input values that are entered during a recording session.</span></span> <span data-ttu-id="1355c-181">たとえば、記録セッション中に製品 0005 を追加した場合、既定では、製品 ID は Recording.xml ファイルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-181">For example, if you added product 0005 during the recording session, the product ID is stored by default in the Recording.xml file.</span></span> <span data-ttu-id="1355c-182">別の製品 ID を指定する場合は、ここで値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-182">If you want to specify a different product ID, you can change the value here.</span></span> <span data-ttu-id="1355c-183">この値は、ユーザー入力がある場合のみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-183">The value will be shown only if there is user input.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="1355c-184">[![値と注釈の編集](./media/EditAnnotation.png)](./media/EditAnnotation.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-184">[![Edit a value and an annotation](./media/EditAnnotation.png)](./media/EditAnnotation.png)</span></span>

### <a name="hide-the-test-recorder-pane"></a><span data-ttu-id="1355c-185">テスト レコーダー ウィンドウの非表示</span><span class="sxs-lookup"><span data-stu-id="1355c-185">Hide the test recorder pane</span></span>

<span data-ttu-id="1355c-186">記録セッション中にテスト レコーダー ウィンドウの非表示と表示を切り替えるには、折りたたみボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-186">To hide and show the test recorder pane during a recording session, select the collapse button.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="1355c-187">[![折りたたみボタン](./media/Hide.png)](./media/Hide.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-187">[![Collapse button](./media/Hide.png)](./media/Hide.png)</span></span>

### <a name="test-recorder-floater-control"></a><span data-ttu-id="1355c-188">テスト レコーダーのフローター コントロール</span><span class="sxs-lookup"><span data-stu-id="1355c-188">Test recorder floater control</span></span>

<span data-ttu-id="1355c-189">テスト レコーダーのフローター コントロールは、記録セッション中にテスト レコーダー ウィンドウが非表示になっている場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1355c-189">The test recorder floater control is useful when the test recorder pane is hidden during a recording session.</span></span> <span data-ttu-id="1355c-190">テスト レコーダー ウィンドウは、エラーのないダイアログ ボックスや POS ビューの一部をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="1355c-190">The test recorder pane overrides non-error dialog boxes and/or part of the POS view.</span></span> <span data-ttu-id="1355c-191">したがって、ダイアログ ボックスで検証を追加したり、コントロールを選択したりするために、ウィンドウを非表示にすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-191">Therefore, you must sometimes hide the pane to add validation in the dialog boxes or select controls.</span></span> <span data-ttu-id="1355c-192">テスト レコーダー ウィンドウが非表示になっていても、テスト記録機能にアクセスする必要がある場合 (たとえば、検証モードをオンにしたり、記録セッションを一時停止または続行する必要がある場合)、このフローター コントロールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-192">If the test recorder pane is hidden, but you must still be able to access test recording functionality (for example, you must turn on validation mode, or pause or continue the recording session), you can use this floater control.</span></span>

<span data-ttu-id="1355c-193">[![フローター制御](./media/Floatter.png)](./media/Floatter.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-193">[![Floater control](./media/Floatter.png)](./media/Floatter.png)</span></span>

<span data-ttu-id="1355c-194">次のセクションでは、フローター コントロール上のコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1355c-194">The following sections describe the controls on the floater control.</span></span>

#### <a name="move-control"></a><span data-ttu-id="1355c-195">移動コントロール</span><span class="sxs-lookup"><span data-stu-id="1355c-195">Move control</span></span>

<span data-ttu-id="1355c-196">移動コントロールを使用すると、POS アプリ内の フローター コントロールを移動できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-196">The move control lets you move the floater control within the POS app.</span></span>

#### <a name="validation-mode"></a><span data-ttu-id="1355c-197">検証モード</span><span class="sxs-lookup"><span data-stu-id="1355c-197">Validation mode</span></span>

<span data-ttu-id="1355c-198">検証モードをオンにすると、記録セッションは一時停止します。</span><span class="sxs-lookup"><span data-stu-id="1355c-198">When you turn on validation mode, the recording session is paused.</span></span> <span data-ttu-id="1355c-199">記録セッションを続行するには、検証モードをオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-199">To continue the recording session, you must turn off validation mode.</span></span>

#### <a name="pause"></a><span data-ttu-id="1355c-200">一時停止</span><span class="sxs-lookup"><span data-stu-id="1355c-200">Pause</span></span>

<span data-ttu-id="1355c-201">記録セッションを一時的に中止 (一時停止) して操作を続行するには、**一時停止**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-201">To temporarily stop (pause) the recording session and continue the operation, select the **Pause** button.</span></span> <span data-ttu-id="1355c-202">**一時停止** を選択した後で実行するステップは記録されません。</span><span class="sxs-lookup"><span data-stu-id="1355c-202">Steps that you perform after you select **Pause** aren't recorded.</span></span>

#### <a name="recording"></a><span data-ttu-id="1355c-203">レコード</span><span class="sxs-lookup"><span data-stu-id="1355c-203">Recording</span></span>

<span data-ttu-id="1355c-204">一時停止後に記録セッションを再開するには、**記録**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-204">To resume the recording session after you've paused it, select **Recording**.</span></span>

## <a name="record-a-test-case-in-retail-pos"></a><span data-ttu-id="1355c-205">Retail POS でのテスト ケースの記録</span><span class="sxs-lookup"><span data-stu-id="1355c-205">Record a test case in Retail POS</span></span>

### <a name="create-a-recording"></a><span data-ttu-id="1355c-206">記録の作成</span><span class="sxs-lookup"><span data-stu-id="1355c-206">Create a recording</span></span>

<span data-ttu-id="1355c-207">次の手順に従い、テスト レコーダーを使用して新しい記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="1355c-207">Follow these steps to create a new recording by using the test recorder:</span></span>

1. <span data-ttu-id="1355c-208">Retail Cloud POS を開き、サインインします。</span><span class="sxs-lookup"><span data-stu-id="1355c-208">Open Retail Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="1355c-209">**設定**ページの**タスクとテスト レコーダー**セクションで、**テスト レコーダーを開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-209">On the **Settings** page, in the **Task and Test recorders** section, select **Open test recorder**.</span></span>

    <span data-ttu-id="1355c-210">[![タスクおよびテスト レコーダー](./media/CreateTest.png)](./media/CreateTest.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-210">[![Task and Test recorders](./media/CreateTest.png)](./media/CreateTest.png)</span></span>

3. <span data-ttu-id="1355c-211">**新しい記録の作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-211">Select **Create a new recording**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="1355c-212">[![新しい記録の作成](./media/NewTest.png)](./media/Newtest.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-212">[![Create a new recording](./media/NewTest.png)](./media/Newtest.png)</span></span>

4. <span data-ttu-id="1355c-213">記録の名前と説明を入力し、**開始**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-213">Enter a name and description for the recording, and then select **Start**.</span></span>

    <span data-ttu-id="1355c-214">テスト レコーダーが記録モードに入り、記録セッションが開始されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-214">The test recorder enters recording mode, and the recording session begins.</span></span> <span data-ttu-id="1355c-215">テスト レコーダー ウィンドウには、記録セッションに関連付けられている情報とコントロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-215">The test recorder pane shows information and controls that are related to the recording session.</span></span>

5. <span data-ttu-id="1355c-216">Retail POS UI で、目的のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="1355c-216">Perform the actions that you want to perform in the Retail POS UI.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="1355c-217">[![テスト レコーダーのステップ](./media/Steps.png)](./media/Steps.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-217">[![Test recorder steps](./media/Steps.png)](./media/Steps.png)</span></span>

### <a name="validation-mode"></a><span data-ttu-id="1355c-218">検証モード</span><span class="sxs-lookup"><span data-stu-id="1355c-218">Validation mode</span></span>

<span data-ttu-id="1355c-219">記録セッション中に検証モードを使用すると、ユーザーはテストの実行中に値を検証できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-219">When you use validation mode during a recording session, users can then validate values during test execution.</span></span> <span data-ttu-id="1355c-220">たとえば、ラベル テキストまたはエラー メッセージを検証する場合や、品目価格または税金が正しく計算されているかどうかを検証する場合に、検証モード機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-220">For example, you can use the validation mode feature if you want to validate label text or an error message, or if you want to validate that the item price or tax is calculated correctly.</span></span> <span data-ttu-id="1355c-221">記録セッション中に検証モードをオンにするには、**検証モードの有効化**オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="1355c-221">To turn on validation mode during a recording session, use the **Enable validation mode** option.</span></span>

1. <span data-ttu-id="1355c-222">**検証モードの有効化**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="1355c-222">Set the **Enable validation mode** option to **Yes**.</span></span>
2. <span data-ttu-id="1355c-223">検証ステップを追加するには、POS の値またはテキストを選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-223">Select values or text in the POS to add a validation step.</span></span> <span data-ttu-id="1355c-224">パスワード、機密データ、またはテスト レコーダーがフィールド値を取得できないフィールドに対して、検証は行われません。</span><span class="sxs-lookup"><span data-stu-id="1355c-224">No validation is done for passwords, sensitive data, or fields where the test recorder can't get the field values.</span></span> <span data-ttu-id="1355c-225">テストの実行中、再生エンジンは値が同じかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="1355c-225">During test execution, the playback engine determines whether the value is same.</span></span> <span data-ttu-id="1355c-226">検証の結果に応じて、テスト ケースは合格または不合格のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="1355c-226">The test case then either passes or fails, depending on the result of the validation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1355c-227">検証モードがオンになっている場合、テスト レコーダーは一時停止状態になります。</span><span class="sxs-lookup"><span data-stu-id="1355c-227">While validation mode is turned on, the test recorder will be in a paused state.</span></span> <span data-ttu-id="1355c-228">検証ステップが追加されるのみとなります。POS は検証ステップの追加以外のユーザー アクションには応答しません。</span><span class="sxs-lookup"><span data-stu-id="1355c-228">It will just add validations steps, and POS won't respond to any user actions except the addition of validation steps.</span></span> <span data-ttu-id="1355c-229">たとえば、検証モードでは、異なる POS ビューを開いたり、POS 機能を使用したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1355c-229">For example, in validation mode, you can't open a different POS view or use any POS functionality.</span></span> <span data-ttu-id="1355c-230">記録セッションを続行するには、**検証モードの有効化**オプションを**いいえ**に設定して、検証モードをオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-230">To continue the recording session, you must turn off validation mode by setting the **Enable validation mode** option to **No**.</span></span>

    <span data-ttu-id="1355c-231">[![テスト レコーダーの検証](./media/Validation.png)](./media/Validation.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-231">[![Test recorder validation](./media/Validation.png)](./media/Validation.png)</span></span>

3. <span data-ttu-id="1355c-232">記録セッションを終了するには、**停止**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-232">To end the recording session, select **Stop**.</span></span>

### <a name="download-options"></a><span data-ttu-id="1355c-233">ダウンロード オプション</span><span class="sxs-lookup"><span data-stu-id="1355c-233">Download options</span></span>

<span data-ttu-id="1355c-234">記録セッションを終了した後、**このPC に保存**を選択することにより、記録をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="1355c-234">After you end a recording session, you can download the recording by selecting **Save to this PC**.</span></span>

<span data-ttu-id="1355c-235">[![テスト レコーダーの出力ファイルの保存](./media/Save.png)](./media/Save.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-235">[![Save test recorder output file](./media/Save.png)](./media/Save.png)</span></span>

<span data-ttu-id="1355c-236">Recording.xml ファイルは、ローカル ファイル システムに保存されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-236">The Recording.xml file is saved to the local file system.</span></span> <span data-ttu-id="1355c-237">このファイルは、手動で LCS または Azure DevOps にアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-237">You must manually upload this file to LCS or Azure DevOps.</span></span> <span data-ttu-id="1355c-238">その後、ファイル システムから削除するか、セキュリティで保護する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-238">You must then either delete it from the file system or secure it.</span></span>

## <a name="install-rsat"></a><span data-ttu-id="1355c-239">RSAT をインストールする</span><span class="sxs-lookup"><span data-stu-id="1355c-239">Install RSAT</span></span>

<span data-ttu-id="1355c-240">RSAT の Microsoft Windows インストーラー (MSI) パッケージ ファイルを [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357) からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1355c-240">Download the Microsoft Windows Installer (MSI) package file for RSAT from [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="1355c-241">MSI ファイルをダブルクリックして、実行します。</span><span class="sxs-lookup"><span data-stu-id="1355c-241">Double-click the MSI file to run it.</span></span> <span data-ttu-id="1355c-242">RSAT をインストールした後、Selenium と Web ブラウザーのドライバーをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-242">After you install RSAT, you must install drivers for Selenium and the web browser.</span></span> 

> [!NOTE]
> <span data-ttu-id="1355c-243">テストを実行する前に Azure DevOps を設定する必要があります。また、必要な全般設定およびその他の RSAT で必要な設定を完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-243">Before you run the test, you must set up Azure DevOps, and you must complete the required general settings and other required settings in RSAT.</span></span> <span data-ttu-id="1355c-244">詳細な手順については、「[Regression Suite Automation Tool のインストールおよびコンフィギュレーション](../../dev-itpro/perf-test/rsat/rsat-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1355c-244">For detailed steps, see [Regression suite automation tool installation and configuration](../../dev-itpro/perf-test/rsat/rsat-overview.md).</span></span>

<span data-ttu-id="1355c-245">次の手順では、Retail POS のテスト ケースを実行するために必要なコンフィギュレーションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1355c-245">The following procedure describes the configuration that is required to run the Retail POS test cases.</span></span>

<span data-ttu-id="1355c-246">POS RSAT のプレビュー バージョンを使用している場合、RSAT のインストール後に、Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config 構成ファイルに次の設定を追加します。</span><span class="sxs-lookup"><span data-stu-id="1355c-246">If you are using the preview version of POS RSAT, after the installation of RSAT, add the following setting in the Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config configuration file.</span></span> <span data-ttu-id="1355c-247">このファイルは、メインの RSAT インストール フォルダ (通常は C:\Program Files (x86)\Regression Suite Automation Tool) にあります。</span><span class="sxs-lookup"><span data-stu-id="1355c-247">This file is located in main RSAT installation folder (usually C:\Program Files (x86)\Regression Suite Automation Tool).</span></span>

```Xml
<add key="RetailPos" value="true" />
```

<span data-ttu-id="1355c-248">この設定を使用しない場合、**RSAT の設定**タブに Retail POS タブは表示されません。</span><span class="sxs-lookup"><span data-stu-id="1355c-248">If this setting is not used, Retail POS tab will not be shown on the **RSAT Settings** tab.</span></span>

### <a name="configure-the-retail-pos-settings"></a><span data-ttu-id="1355c-249">Retail POS 設定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="1355c-249">Configure the Retail POS settings</span></span>

1. <span data-ttu-id="1355c-250">デスクトップから RSAT を開きます。</span><span class="sxs-lookup"><span data-stu-id="1355c-250">Open RSAT from your desktop.</span></span>
2. <span data-ttu-id="1355c-251">右上にある**設定**ボタンを選択して、RSAT をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="1355c-251">Select the **Settings** button in the upper right to configure RSAT.</span></span>
3. <span data-ttu-id="1355c-252">**設定**ダイアログ ボックスの **Retail POS** タブの**再生環境**タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="1355c-252">In the **Settings** dialog box, on the **Retail POS** tab, on the **Playback environment** tab, set the following fields:</span></span>

    + <span data-ttu-id="1355c-253">**Cloud POS URL** – テストを実行する Retail Cloud POS 環境の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="1355c-253">**Cloud POS URL** – Enter the URL of the Retail Cloud POS environment where you want to run the test.</span></span>
    + <span data-ttu-id="1355c-254">**Retail サーバー URL** – デバイスがまだ有効化されていない場合にデバイスの有効化に使用する、Retail サーバー URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="1355c-254">**Retail server URL** – Enter the Retail Server URL that should be used for device activation, if the device hasn't already been activated.</span></span>
    + <span data-ttu-id="1355c-255">**AAD ユーザー電子メール** - デバイスの有効化に使用する Azure Active Directory (Azure AD) ユーザーの電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="1355c-255">**AAD user email** – Enter the email address of the Azure Active Directory (Azure AD) user that should be used for device activation.</span></span> <span data-ttu-id="1355c-256">Azure AD ユーザーは、デバイスを有効にするアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-256">The Azure AD user must have permission to activate the device.</span></span>
    + <span data-ttu-id="1355c-257">**AAD パスワード** - デバイスの有効化に使用する Azure AD ユーザーのパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="1355c-257">**AAD password** – Enter the password of the Azure AD user that should be used for device activation.</span></span>
    + <span data-ttu-id="1355c-258">**店舗** - テストを実行する店舗 (小売チャネル) の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="1355c-258">**Store** – Enter the ID of the store (retail channel) where the test should be run.</span></span>
    + <span data-ttu-id="1355c-259">**デバイス** - テストを実行するデバイスの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="1355c-259">**Device** – Enter the ID of the device where the test should be run.</span></span>
    + <span data-ttu-id="1355c-260">**既定の待機時間** - いずれの要素も見つからなかった場合に、テスト ケースが失敗するまでの待機時間を秒単位で入力します。</span><span class="sxs-lookup"><span data-stu-id="1355c-260">**Default wait time** – Enter the wait time, in seconds, before the test case fails if any element isn't found.</span></span> <span data-ttu-id="1355c-261">テストの実行中、再生エンジンは、この既定の待機時間が経過するまで検索要素の検索を試行し続けます。</span><span class="sxs-lookup"><span data-stu-id="1355c-261">During test execution, the playback engine keeps trying to find the find element until this default wait time has passed.</span></span> <span data-ttu-id="1355c-262">その後、テスト ケースに失敗し、記録されていた要素が見つからなかったか、再生用に読み込まれなかったことを通知します。</span><span class="sxs-lookup"><span data-stu-id="1355c-262">It then fails the test case and notifies you that the element that was recorded wasn't found or loaded for playback.</span></span>

    <span data-ttu-id="1355c-263">[![再生環境](./media/Setting.png)](./media/Setting.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-263">[![Playback environment](./media/Setting.png)](./media/Setting.png)</span></span>

5. <span data-ttu-id="1355c-264">**POS ログイン資格情報**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-264">Select the **POS login credentials** tab.</span></span>

    <span data-ttu-id="1355c-265">記録セッション中、テスト レコーダーは POS からのユーザー名のみをキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="1355c-265">During a recording session, the test recorder captures only the user name from the POS.</span></span> <span data-ttu-id="1355c-266">パスワードは保存されません。</span><span class="sxs-lookup"><span data-stu-id="1355c-266">It doesn't store any password.</span></span> <span data-ttu-id="1355c-267">ただし、テストを実行するには、POS へのサインインに使用するユーザー名とパスワードの両方が必要です。</span><span class="sxs-lookup"><span data-stu-id="1355c-267">However, to run the test, you must have both the user name and the password that are used to sign in to POS.</span></span> <span data-ttu-id="1355c-268">このタブは POS のユーザー名とパスワードを取得して、パスワード情報が記録ファイルの外部に安全に保管されるようにします。</span><span class="sxs-lookup"><span data-stu-id="1355c-268">This tab captures the POS user name and password, so that the password information is securely stored outside the recording file.</span></span> <span data-ttu-id="1355c-269">テストの実行時に、ユーザー ID は、RSAT で入力されたものと同じユーザー ID にマップされ、パスワードが取得されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-269">During test execution, the user ID is then mapped to the same user ID that is entered in RSAT, and the password is retrieved.</span></span>
    
    <span data-ttu-id="1355c-270">したがって、**POS ログイン資格情報**タブでは、記録セッション中に使用されたすべてのユーザー名とパスワードの情報を入力して、テストの実行中にパスワードを取得できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-270">Therefore, on the **POS login credentials** tab, you must enter all the user name and password information that was used during the recording session, so that the password can be retrieved during test execution.</span></span> <span data-ttu-id="1355c-271">入力しない場合、テストの実行は失敗し、サインインの詳細が見つからなかったことが通知されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-271">Otherwise, test execution will fail, and you will be notified that sign-in details weren't found.</span></span>

    <span data-ttu-id="1355c-272">[![POS ログインの資格情報](./media/PosLogin.png)](./media/PosLogin.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-272">[![POS login credentials](./media/PosLogin.png)](./media/PosLogin.png)</span></span>

6. <span data-ttu-id="1355c-273">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-273">Select **New**.</span></span>

    <span data-ttu-id="1355c-274">[![POS ユーザー](./media/EditPosUser.png)](./media/EditPosUser.png)</span><span class="sxs-lookup"><span data-stu-id="1355c-274">[![POS user](./media/EditPosUser.png)](./media/EditPosUser.png)</span></span>

7. <span data-ttu-id="1355c-275">**ユーザー名**フィールドに、POS へのサインイン用のユーザー名を入力します。</span><span class="sxs-lookup"><span data-stu-id="1355c-275">In the **Username** field, enter the user name for sign-in to POS.</span></span>
8. <span data-ttu-id="1355c-276">**パスワード**フィールドに、POS へのサインイン用のパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="1355c-276">In the **Password** field, enter the password for sign-in to POS.</span></span>
9. <span data-ttu-id="1355c-277">手順 6～8 を繰り返して、POS にサインインするための他のユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="1355c-277">Repeat steps 6 through 8 to enter other user names and passwords for sign-in to POS.</span></span>
10. <span data-ttu-id="1355c-278">一連の POS サインイン資格情報を編集するには、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-278">To edit a set of POS sign-in credentials, select **Edit**.</span></span>
11. <span data-ttu-id="1355c-279">一連の POS サインイン資格情報を削除するには、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-279">To delete a set of POS sign-in credentials, select **Delete**.</span></span>

## <a name="run-tests"></a><span data-ttu-id="1355c-280">テストの実行</span><span class="sxs-lookup"><span data-stu-id="1355c-280">Run tests</span></span>

<span data-ttu-id="1355c-281">このセクションでは、Azure DevOps からのテスト ケースの読み込み、自動化ファイルの生成、テスト パラメーターの変更、テストの実行、結果の調査、Azure DevOps への作業の保存方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1355c-281">This section explains how to load test cases from Azure DevOps, generate automation files, modify test parameters, run tests, investigate results, and save your work back to Azure DevOps.</span></span>

> [!NOTE]
> <span data-ttu-id="1355c-282">Azure DevOps およびテスト ケースの設定の詳細については、「[Regression Suite Automation Tool のインストールおよびコンフィギュレーション](../../dev-itpro/perf-test/rsat/rsat-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1355c-282">For detailed information about how to set up Azure DevOps and test cases, see [Regression suite automation tool installation and configuration](../../dev-itpro/perf-test/rsat/rsat-overview.md).</span></span> <span data-ttu-id="1355c-283">テストの実行を開始する前に、この設定を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-283">You must complete that setup before you start to run tests.</span></span>

### <a name="load-test-cases-and-create-parameter-files"></a><span data-ttu-id="1355c-284">テスト ケースの読み込みとパラメーター ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="1355c-284">Load test cases and create parameter files</span></span>

<span data-ttu-id="1355c-285">RSAT で、**読み込み**を選択して、テスト ケースとテスト ケース自動化ファイルを Azure DevOps からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1355c-285">In RSAT, select **Load** to download test cases and test case automation files from Azure DevOps.</span></span> <span data-ttu-id="1355c-286">**設定**ダイアログ ボックスで指定されたテスト計画に属する、すべてのテスト ケースがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="1355c-286">All test cases that belong to the test plan that is specified in the **Settings** dialog box are downloaded.</span></span>

![貨物](./media/RSATLoad.png)

<span data-ttu-id="1355c-288">テスト ケースは、共通のテスト計画の下にあるテスト スイート別にまとめられています。</span><span class="sxs-lookup"><span data-stu-id="1355c-288">Test cases are organized by test suite under a common test plan.</span></span> <span data-ttu-id="1355c-289">テスト スイートは、Azure DevOps プロジェクトで作成したテスト スイートです。</span><span class="sxs-lookup"><span data-stu-id="1355c-289">The test suites are the test suites that you created in your Azure DevOps project.</span></span> <span data-ttu-id="1355c-290">RSAT を使用することにより、一度に 1 つのテスト スイートを操作できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-290">By using RSAT, you can work with one test suite at a time.</span></span> <span data-ttu-id="1355c-291">RSAT でテスト ケースを読み込むことができない場合は、Azure DevOps でテスト計画が正しく作成されていること、および必要なテスト スイートとテスト ケースが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1355c-291">If RSAT can't load any test case, verify that your test plan was correctly created in Azure DevOps, and that it contains the required test suites and test cases.</span></span>

<span data-ttu-id="1355c-292">テスト計画を初めて読み込む場合、グリッドの**パラメーター ファイル**列は空白です。テスト ケースのテスト自動化パラメーター ファイルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-292">If you're loading the test plan for the first time, the **Parameters File** column in the grid is blank, and you must generate test automation parameter files for your test cases.</span></span>

<span data-ttu-id="1355c-293">テストを実行するには、次のテスト自動化ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="1355c-293">To run the tests, generate the following test automation files:</span></span>

- <span data-ttu-id="1355c-294">テスト パラメーター ファイル (テスト ケース パラメーターを含む Excel ファイル)</span><span class="sxs-lookup"><span data-stu-id="1355c-294">Test parameter files (Excel files that contain test case parameters)</span></span>
- <span data-ttu-id="1355c-295">テストの実行に必要な XML ファイル</span><span class="sxs-lookup"><span data-stu-id="1355c-295">XML files that are required to run the tests</span></span>

<span data-ttu-id="1355c-296">**新規**を選択すると、テスト自動化ファイルが作業ディレクトリに生成されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-296">When you select **New**, test automation files are generated in your working directory.</span></span> <span data-ttu-id="1355c-297">Excel テスト パラメーター ファイルは、グリッドの**パラメーター ファイル**列に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-297">The Excel test parameter files appear in the **Parameters File** column in the grid.</span></span>

![パラメーター ファイル列のテスト パラメーター ファイル](./media/RSATParameter.png)

<span data-ttu-id="1355c-299">小売テストの記録ファイルの場合、**テストの実行ファイルのみを生成**オプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="1355c-299">For the retail test recording files, the **Generate Test Execution files only** option is unavailable.</span></span> <span data-ttu-id="1355c-300">Retail Cloud POS では、Selenium web を直接使用して再生を実行するため、追加のスクリプト ファイルを生成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1355c-300">Because Retail Cloud POS uses the Selenium web directly to do the playback, no additional script file must be generated.</span></span>

![利用不可のテスト実行ファイルのみ生成オプション](./media/RSATNewOption.png)

### <a name="modify-test-parameters-and-validation-values"></a><span data-ttu-id="1355c-302">テスト パラメーターおよび検証値の変更</span><span class="sxs-lookup"><span data-stu-id="1355c-302">Modify test parameters and validation values</span></span>

<span data-ttu-id="1355c-303">このセクションでは、テスト実行の入力パラメーターと検証パラメーターを指定して Excel ファイルを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1355c-303">This section explains how to modify Excel files by specifying input and validation parameters for your test run.</span></span>

<span data-ttu-id="1355c-304">RSAT で、変更する 1 つ以上のテスト ケースを選択してから、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-304">In RSAT, select one or more test cases to modify, and then select **Edit**.</span></span> <span data-ttu-id="1355c-305">選択したテスト ケースごとに Excel ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="1355c-305">An Excel window is opened for each test case that you selected.</span></span> <span data-ttu-id="1355c-306">または、作業ディレクトリから直接 Excel ファイルを開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="1355c-306">Alternatively, you can open the Excel files directly from the working directory.</span></span>

<span data-ttu-id="1355c-307">Excel ファイルには、**概要**タブに加えて、生成されたすべての変数の詳細を示す**変数**タブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1355c-307">In addition to a **Summary** tab, the Excel file includes a **Variables** tab that has the details of all the variables that were generated.</span></span> <span data-ttu-id="1355c-308">Retail POS は、記録セッション中に入力されたすべての入力値に対して、変数を自動的に生成します。</span><span class="sxs-lookup"><span data-stu-id="1355c-308">Retail POS automatically generates variables for all the input values that are entered during a recording session.</span></span> <span data-ttu-id="1355c-309">変数を個別に生成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1355c-309">You don't have to generate the variables separately.</span></span> <span data-ttu-id="1355c-310">各変数には、一意の変数 ID があります。この ID は、テスト実行の 1 つのインスタンスで別のテスト ケースに順番に渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="1355c-310">Each variable has a unique variable ID that you can pass, in order, to different test cases in a single instance of test execution.</span></span> <span data-ttu-id="1355c-311">**変数**タブのすべての変数は、記録セッション中に入力された順序で表示されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-311">All the variables on the **Variables** tab appear in the order that they were entered in during the recording session.</span></span>

### <a name="validate-expected-values"></a><span data-ttu-id="1355c-312">予測値の検証</span><span class="sxs-lookup"><span data-stu-id="1355c-312">Validate expected values</span></span>

<span data-ttu-id="1355c-313">予想される値の検証は、テスト ケースの重要な要素です。</span><span class="sxs-lookup"><span data-stu-id="1355c-313">Validation of expected values is an important component of a test case.</span></span> <span data-ttu-id="1355c-314">テスト ケースを作成するときに、検証モードでテスト レコーダーを使用して検証パラメーターを定義できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-314">When you create your test cases, you can define validation parameters by using the test recorder in validation mode.</span></span>

<span data-ttu-id="1355c-315">記録セッション中に、検証モードをオンにします。</span><span class="sxs-lookup"><span data-stu-id="1355c-315">During the recording session, turn on validation mode.</span></span> <span data-ttu-id="1355c-316">次に、テスト レコーダーが記録している間に、検証する必要があるフィールドをすべて選択します。</span><span class="sxs-lookup"><span data-stu-id="1355c-316">Then, while the test recorder is recording, select all the fields that must be validated.</span></span> <span data-ttu-id="1355c-317">このアクションが RSAT で使用できる検証ステップになります。</span><span class="sxs-lookup"><span data-stu-id="1355c-317">This action becomes a validation step that you can use with RSAT.</span></span> <span data-ttu-id="1355c-318">検証値は、入力された順に、Excel ファイルの**変数**タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-318">The validation values will appear, in the order that they were entered in, on the **Variables** tab in the Excel file.</span></span> <span data-ttu-id="1355c-319">その後、テストの実行前に Excel ファイルの値を変更し、テストの実行中に新しい値を使用してデータの入力および検証を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1355c-319">You can then modify the values in the Excel file before test execution, and the new values will be used for data entry and validation during test execution.</span></span>

![値の編集](./media/RSATExcel.png)

### <a name="run"></a><span data-ttu-id="1355c-321">実行</span><span class="sxs-lookup"><span data-stu-id="1355c-321">Run</span></span>

<span data-ttu-id="1355c-322">RSAT で、**実行**を選択して、選択したテスト ケースを実行します。</span><span class="sxs-lookup"><span data-stu-id="1355c-322">In RSAT, select **Run** to run the selected test cases.</span></span> <span data-ttu-id="1355c-323">自動化ファイルが生成されたテスト ケースのみ実行できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-323">You can run only test cases that automation files have been generated for.</span></span> <span data-ttu-id="1355c-324">RSAT は Retail POS を開き、Excel に入力されたデータを使用してテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="1355c-324">RSAT opens Retail POS and runs the tests by using the data that is entered in Excel.</span></span> <span data-ttu-id="1355c-325">テストの実行後、RSAT の**結果**列、および Azure DevOps で結果が更新されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-325">After the test run, the results are updated in the **Result** column in RSAT, and also in Azure DevOps.</span></span>

<span data-ttu-id="1355c-326">テスト ケースが実行される順序を変更するには、上向き矢印ボタンと下向き矢印ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="1355c-326">To change the order that test cases are run in, use the up arrow and down arrow buttons.</span></span>

### <a name="investigate-results"></a><span data-ttu-id="1355c-327">結果の調査</span><span class="sxs-lookup"><span data-stu-id="1355c-327">Investigate results</span></span>

<span data-ttu-id="1355c-328">テスト ケースの実行が完了すると、RSAT の**結果**列に合格または不合格のステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-328">After test cases have finished running, the pass or fail status appears in the **Result** column in RSAT.</span></span> <span data-ttu-id="1355c-329">**結果**列を選択して、エラー メッセージを表示できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-329">You can select the **Result** column to view the error messages.</span></span> <span data-ttu-id="1355c-330">詳細は Azure DevOps にあります。この詳細を使用して結果を調査できます。</span><span class="sxs-lookup"><span data-stu-id="1355c-330">More details are available in Azure DevOps, and you can use them to investigate the results.</span></span> <span data-ttu-id="1355c-331">Azure DevOps プロジェクト ページで、**テスト \> 実行**に移動します。</span><span class="sxs-lookup"><span data-stu-id="1355c-331">From your Azure DevOps project page, go to **Test \> Runs**.</span></span>

<span data-ttu-id="1355c-332">すべてのエラー メッセージは、C:\\Users\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg\<TestCaseId\>.txt でローカルでも利用可能です。</span><span class="sxs-lookup"><span data-stu-id="1355c-332">All error messages are also available locally at C:\\Users\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg\<TestCaseId\>.txt.</span></span>

## <a name="system-and-metadata-files"></a><span data-ttu-id="1355c-333">システムおよびメタデータ ファイル</span><span class="sxs-lookup"><span data-stu-id="1355c-333">System and metadata files</span></span>

<span data-ttu-id="1355c-334">次の表に、記録セッション、テストの実行、および再生時に生成されるファイルを示します。</span><span class="sxs-lookup"><span data-stu-id="1355c-334">The following table shows the files that are generated during recording sessions, test execution, and playback.</span></span>

| <span data-ttu-id="1355c-335">ファイル名</span><span class="sxs-lookup"><span data-stu-id="1355c-335">File name</span></span>      | <span data-ttu-id="1355c-336">説明</span><span class="sxs-lookup"><span data-stu-id="1355c-336">Description</span></span> | <span data-ttu-id="1355c-337">ファイル生成フロー</span><span class="sxs-lookup"><span data-stu-id="1355c-337">File generation flow</span></span> | <span data-ttu-id="1355c-338">ファイル保存フロー</span><span class="sxs-lookup"><span data-stu-id="1355c-338">File save flow</span></span> |
|----------------|-------------|----------------------|----------------|
| <span data-ttu-id="1355c-339">Recording.xml</span><span class="sxs-lookup"><span data-stu-id="1355c-339">Recording.xml</span></span>  | <span data-ttu-id="1355c-340">このファイルには、記録の再生に必要なすべてのステップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1355c-340">This file contains all the steps that are required to play back a recording.</span></span> <span data-ttu-id="1355c-341">記録の各ステップのすべてのユーザー固有の値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1355c-341">It includes all user-specific values for each step in the recording.</span></span> | <span data-ttu-id="1355c-342">ユーザーがテスト ケースを記録し、Azure DevOps にアップロードすると、RSAT で使用できるようにファイルが生成されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-342">The file is generated by the user when that user records a test case and uploads it to Azure DevOps so that it can be used by RSAT.</span></span> | <span data-ttu-id="1355c-343">このファイルは、テスト ケースが RSAT に読み込まれたときにディスクに保存されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-343">The file is saved to disk when the test case is loaded into RSAT.</span></span> |
| <span data-ttu-id="1355c-344">Variables.xml</span><span class="sxs-lookup"><span data-stu-id="1355c-344">Variables.xml</span></span>  | <span data-ttu-id="1355c-345">このファイルには、記録ファイルで使用されているすべての変数の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1355c-345">This file contains the values for all the variables that are used in the recording file.</span></span> <span data-ttu-id="1355c-346">再生ツールによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-346">It's used by the playback tool.</span></span> | <span data-ttu-id="1355c-347">このファイルは、ユーザーが RSAT で**新規 \> テスト実行とパラメーター ファイルの生成**を選択したときに生成されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-347">The file is generated when the user selects **New \> Generate Test Execution and Parameter files** in RSAT.</span></span> | <span data-ttu-id="1355c-348">このファイルは、ユーザーが**新規 \> テスト実行とパラメーター ファイルの生成**を選択したときに保存されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-348">The file is saved when the user selects **New \> Generate Test Execution and Parameter files**.</span></span> |
| <span data-ttu-id="1355c-349">Variables.xlsx</span><span class="sxs-lookup"><span data-stu-id="1355c-349">Variables.xlsx</span></span> | <span data-ttu-id="1355c-350">このファイルには、記録ファイルで使用されているすべての変数の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1355c-350">This file contains the values for all the variables that are used in the recording file.</span></span> <span data-ttu-id="1355c-351">このファイルはユーザーが変更でき、再生ツールによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-351">It can be modified by the user and is used by the playback tool.</span></span> | <span data-ttu-id="1355c-352">このファイルは、ユーザーが RSAT で**新規 \> テスト実行とパラメーター ファイルの生成**を選択したときに生成されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-352">The file is generated when the user selects **New \> Generate Test Execution and Parameter files** in RSAT.</span></span> | <span data-ttu-id="1355c-353">このファイルは、ユーザーが**新規 \> テスト実行とパラメーター ファイルの生成**を選択したときに保存されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-353">The file is saved when the user selects **New \> Generate Test Execution and Parameter files**.</span></span> |
| <span data-ttu-id="1355c-354">OutputLog.txt</span><span class="sxs-lookup"><span data-stu-id="1355c-354">OutputLog.txt</span></span>  | <span data-ttu-id="1355c-355">このファイルには、再生プロセスの実行のログが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1355c-355">This file contains a log of execution of the playback process.</span></span> <span data-ttu-id="1355c-356">このファイルには、実行された各ステップの説明が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1355c-356">It includes a description of each step that was run.</span></span> <span data-ttu-id="1355c-357">例外が含まれている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="1355c-357">It might also include an exception.</span></span> <span data-ttu-id="1355c-358">例外によっては、Recording.xml ファイルに利用可能なデータが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-358">Depending on the exception, it might contain data that is available in the Recording.xml file.</span></span> | <span data-ttu-id="1355c-359">このファイルは、テスト ケースが正常に再生されたかどうかに関係なく、RSAT の再生ツールの実行が完了した後に生成されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-359">The file is generated after the playback tool in RSAT has finished running, regardless of whether the test case was successfully played back.</span></span> | <span data-ttu-id="1355c-360">このファイルは、テスト ケースが再生されるときに保存されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-360">The file is saved when a test case is played back.</span></span> |
| <span data-ttu-id="1355c-361">Time.xml</span><span class="sxs-lookup"><span data-stu-id="1355c-361">Time.xml</span></span>       | <span data-ttu-id="1355c-362">このファイルには、ステップの一覧、ユーザーによって編集された各ステップの説明、および各ステップの実行に必要な時間が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1355c-362">This file contains the list of steps, the user-edited description of each step, and the amount of time that the execution of each step required.</span></span> | <span data-ttu-id="1355c-363">このファイルは、テスト ケースが正常に再生された場合にのみ、RSAT の再生ツールの実行が完了した後に生成されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-363">The file is generated after the playback tool in RSAT has finished running, but only if the test case was successfully played back.</span></span> | <span data-ttu-id="1355c-364">テスト ケースが正常に再生されると、このファイルが保存されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-364">The file is saved when a test case is successfully played back.</span></span> |
| <span data-ttu-id="1355c-365">Out.xml</span><span class="sxs-lookup"><span data-stu-id="1355c-365">Out.xml</span></span>        | <span data-ttu-id="1355c-366">このファイルには、記録ファイルで使用されているすべての変数の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1355c-366">This file contains the values for all the variables that are used in the recording file.</span></span> <span data-ttu-id="1355c-367">このファイルは、Variables.xlsx ファイルから更新された値を各変数に対して使用します。</span><span class="sxs-lookup"><span data-stu-id="1355c-367">For each variable, this file uses the updated value from the Variables.xlsx file.</span></span> <span data-ttu-id="1355c-368">再生ツールはこのファイルを使用して、他のテスト ケースの変数に依存するテスト ケースをサポートします。</span><span class="sxs-lookup"><span data-stu-id="1355c-368">The playback tool uses this file to support test cases that depend on variables from other test cases.</span></span> | <span data-ttu-id="1355c-369">このファイルは、テスト ケースが正常に再生されたかどうかに関係なく、RSAT の再生ツールの実行が完了した後に生成されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-369">The file is generated after the playback tool in RSAT has finished running, regardless of whether the test case was successfully played back.</span></span> | <span data-ttu-id="1355c-370">このファイルは、テスト ケースが再生されるときに保存されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-370">The file is saved when a test case is played back.</span></span> |
| <span data-ttu-id="1355c-371">In.xml</span><span class="sxs-lookup"><span data-stu-id="1355c-371">In.xml</span></span>         | <span data-ttu-id="1355c-372">このファイルには、現在のテスト ケースの前に実行されたすべてのテスト ケースの記録ファイルで使用される、すべての変数の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1355c-372">This file contains the values for all the variables that are used in the recording file of every test case that was run before the current test case.</span></span> <span data-ttu-id="1355c-373">このファイルは、各 Variables.xlsx ファイルから更新された値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1355c-373">It uses the updated values from each Variables.xlsx file.</span></span> <span data-ttu-id="1355c-374">再生ツールはこのファイルを使用して、他のテスト ケースの変数に依存するテスト ケースをサポートします。</span><span class="sxs-lookup"><span data-stu-id="1355c-374">The playback tool uses this file to support test cases that depend on variables from other test cases.</span></span> | <span data-ttu-id="1355c-375">複数のテスト ケースが実行されている場合、このファイルは、RSAT の再生ツールが実行される前に生成されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-375">The file is generated before the playback tool in RSAT is run, when multiple test cases are run.</span></span> | <span data-ttu-id="1355c-376">ファイルは、前のテスト ケースの実行が完了し、新しいテスト ケースが実行される前に保存されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-376">The file is saved when the previous test case has finished running and before a new test case is run.</span></span> |

<span data-ttu-id="1355c-377">これらのファイルは、手動で削除し、必要に応じて保護する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-377">You must manually delete these files and secure them as you require.</span></span> <span data-ttu-id="1355c-378">これらのファイルはすべて、RSAT の作業ディレクトリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="1355c-378">All these files are stored in the RSAT working directory.</span></span>

## <a name="best-practices"></a><span data-ttu-id="1355c-379">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="1355c-379">Best practices</span></span>

### <a name="creating-test-cases-by-using-the-test-recorder"></a><span data-ttu-id="1355c-380">テスト レコーダーを使用したテスト ケースの作成</span><span class="sxs-lookup"><span data-stu-id="1355c-380">Creating test cases by using the test recorder</span></span>

+ <span data-ttu-id="1355c-381">すべての記録が、POS のログイン画面から開始されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1355c-381">Make sure that all your recordings start from the POS log-in screen.</span></span>
+ <span data-ttu-id="1355c-382">個々の記録を簡潔にし、1 人のユーザーが実行するビジネス タスク (販売トランザクションの作成など) に注目します。</span><span class="sxs-lookup"><span data-stu-id="1355c-382">Keep individual recordings short, and focus on a business task that is performed by one user, such as the creation a sale transaction.</span></span> <span data-ttu-id="1355c-383">この方法を使用すると、テスト ケースの管理と再利用が容易になります。</span><span class="sxs-lookup"><span data-stu-id="1355c-383">This approach makes it easier to maintain and reuse test cases.</span></span>
+ <span data-ttu-id="1355c-384">機密情報を含むシナリオは記録しないでください。</span><span class="sxs-lookup"><span data-stu-id="1355c-384">Don't record any scenario that includes secrets.</span></span>
+ <span data-ttu-id="1355c-385">記録と再生は同じ画面レイアウトで実行し、同じ解像度で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1355c-385">Recording and playback must be done in the same screen layout and at the same resolution.</span></span> <span data-ttu-id="1355c-386">記録と再生が異なるレイアウトで行われ、解像度が異なる場合、再生は失敗します。</span><span class="sxs-lookup"><span data-stu-id="1355c-386">If recording and playback are done in different layouts and at different resolutions, playback will fail.</span></span>
+ <span data-ttu-id="1355c-387">記録の再生中に POS ユーザー名を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="1355c-387">You can't change the POS user name during playback of a recording.</span></span> <span data-ttu-id="1355c-388">記録を作成する場合は、後で再生するときに使用するのと同じユーザー名を常に使用します。</span><span class="sxs-lookup"><span data-stu-id="1355c-388">When you make a recording, always use the same user name that will be used later for playback.</span></span>
+ <span data-ttu-id="1355c-389">POS 有効化フローの記録はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1355c-389">Recording the POS activation flow is not supported.</span></span>
+ <span data-ttu-id="1355c-390">キー操作の記録のパフォーマンスは遅くなる可能性があります。すべてのイベントが正しくキャプチャされるように、記録中はゆっくり入力してください。</span><span class="sxs-lookup"><span data-stu-id="1355c-390">Keystroke recording performance may be slow, so type slowly while recording so that all the events are captured property.</span></span>
+ <span data-ttu-id="1355c-391">現在、周辺機器のエミュレーションはサポートされていません。キーボード ウェッジ ベースのデバイスを使用してください。</span><span class="sxs-lookup"><span data-stu-id="1355c-391">Peripheral emulation is currently not supported, use a keyboard wedge-based device.</span></span>
+ <span data-ttu-id="1355c-392">複数のキー プレス イベントが記録される可能性があるため、記録中にキーを押したままにしないでください。</span><span class="sxs-lookup"><span data-stu-id="1355c-392">Don’t hold a key down during recording, as this could record multiple key press events.</span></span>
