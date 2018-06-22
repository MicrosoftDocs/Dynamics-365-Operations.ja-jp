---
title: "タスク ガイドと BPM を使用して承認テスト スイートを作成する"
description: "このトピックでは、タスク ガイドと BOMを 使用して受け入れテスト スイートを作成する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 03/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 13301
ms.assetid: 
ms.search.region: Global
ms.author: ntecklu
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: ab8d54d8493d4fe208168b5f4be169905cb6fa12
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="create-an-acceptance-test-suite-using-task-guides-and-bpm"></a><span data-ttu-id="bb634-103">タスク ガイドと BPM を使用して承認テスト スイートを作成する</span><span class="sxs-lookup"><span data-stu-id="bb634-103">Create an acceptance test suite using Task guides and BPM</span></span>

<span data-ttu-id="bb634-104">タスク ガイドおよびビジネス プロセス モデラー (BPM) を使用して、ユーザー承認テスト計画を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="bb634-104">You can use Task guides and Business process modeler (BPM) to create a user acceptance test plan.</span></span> <span data-ttu-id="bb634-105">業務プロセスごとに承認テストを整理してから BPM を Visual Studio Team Services (VSTS) に同期し、テストの実行と結果を管理することができます。</span><span class="sxs-lookup"><span data-stu-id="bb634-105">You can organize your acceptance tests by business processes and then synchronize BPM to Visual Studio Team Services (VSTS) to manage test execution and results.</span></span> <span data-ttu-id="bb634-106">このトピックでは、手動テストまたは自動テストに使用する受入れテスト スイートを作成するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bb634-106">This topic walks through the process of creating an acceptance test suite to be used for manual or automatic testing.</span></span>

## <a name="create-a-bpm-library"></a><span data-ttu-id="bb634-107">BPM ライブラリの作成</span><span class="sxs-lookup"><span data-stu-id="bb634-107">Create a BPM library</span></span>

<span data-ttu-id="bb634-108">ビジネス プロセス モデラー (BPM) ライブラリを作成するにはいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="bb634-108">There are several ways to create a Business process modeler (BPM) library.</span></span> <span data-ttu-id="bb634-109">BPM でライブラリを作成する方法の詳細については、[BPM ライブラリの作成、編集、および参照](creating-editing-browsing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb634-109">For more information about how to create libraries in BPM, see [Create, edit, and browse BPM libraries](creating-editing-browsing.md).</span></span>

<span data-ttu-id="bb634-110">説明目的で、このトピックでは、経費精算書の作成および注文要求の承認などの一般的な業務プロセスを含むライブラリを使用します。</span><span class="sxs-lookup"><span data-stu-id="bb634-110">For illustration purposes, this topic uses a library that contains common business processes such as Create expense report and Approve order requests.</span></span> <span data-ttu-id="bb634-111">Excel インポート機能を使用してライブラリを作成しました。</span><span class="sxs-lookup"><span data-stu-id="bb634-111">The library was created by using the Excel import functionality.</span></span>  

<span data-ttu-id="bb634-112">![Excel からインポート](./media/import_from_excel.png.PNG "Excel からインポート")</span><span class="sxs-lookup"><span data-stu-id="bb634-112">![Import from Excel](./media/import_from_excel.png.PNG "Import from Excel")</span></span>

## <a name="record-test-cases-and-upload-to-bpm"></a><span data-ttu-id="bb634-113">テスト ケースを記録して BPM にアップロード</span><span class="sxs-lookup"><span data-stu-id="bb634-113">Record test cases and upload to BPM</span></span> 

<span data-ttu-id="bb634-114">BPMライブラリを作成した後は、タスク レコーダーを使用してテスト ケースを作成し、それから BPM にそのケースをアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb634-114">After you have created a BPM library, you'll need to use Task recorder to create your test cases and then upload the cases to BPM.</span></span> <span data-ttu-id="bb634-115">これを行うにはいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="bb634-115">There are several ways to do this.</span></span> 

<span data-ttu-id="bb634-116">既に必要なタスク記録が付属されているライブラリを使用している場合、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="bb634-116">If you're using a library that already has all of the necessary task recordings attached, you can skip this step.</span></span> <span data-ttu-id="bb634-117">それ以外の場合、クライアントで新しいタスク記録を作成して LCS に直接保存するか、AXTR ファイルをダウンロードしてから後で BPM ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="bb634-117">Otherwise, create a new task recording in the client and save it directly to LCS, or download the AXTR file and upload it to a BPM library later.</span></span> 

### <a name="create-and-save-a-new-task-recording"></a><span data-ttu-id="bb634-118">新しいタスク記録を作成して保存する</span><span class="sxs-lookup"><span data-stu-id="bb634-118">Create and save a new task recording</span></span> 
1. <span data-ttu-id="bb634-119">クライアントを開いて、サインインします。</span><span class="sxs-lookup"><span data-stu-id="bb634-119">Open the client and sign in.</span></span> 
2. <span data-ttu-id="bb634-120">記録中に使用する会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb634-120">Select the company that you want to use while recording.</span></span>
3. <span data-ttu-id="bb634-121">**設定** > **タスク レコーダー**に移動します。</span><span class="sxs-lookup"><span data-stu-id="bb634-121">Go to **Settings** > **Task recorder**.</span></span>

<span data-ttu-id="bb634-122">![タスク レコーダーの選択](./media/select_task_recorder.png.PNG "タスク レコーダーの選択")</span><span class="sxs-lookup"><span data-stu-id="bb634-122">![Select Task recorder](./media/select_task_recorder.png.PNG "Select Task recorder")</span></span>

4. <span data-ttu-id="bb634-123">**新しい記録の作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb634-123">Click **Create a new recording**.</span></span>
5. <span data-ttu-id="bb634-124">コンフィギュレーション名を入力し、**開始**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb634-124">Enter a name for the recording, and then click **Start**.</span></span> <span data-ttu-id="bb634-125">記録は、**開始** をクリックすると開始されます。</span><span class="sxs-lookup"><span data-stu-id="bb634-125">Recording begins the moment that you click **Start**.</span></span>
6. <span data-ttu-id="bb634-126">記録が完了したら、タスク レコーダー ウィンドウで、**停止** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb634-126">When the recording is complete, in the Task recorder pane, click **Stop**.</span></span>
7. <span data-ttu-id="bb634-127">添付された BPM にタスク記録を保存するには、**Lifecycle Services に保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb634-127">To save the task recording to an attached BPM, click **Save to Lifecycle Services**.</span></span>

<span data-ttu-id="bb634-128">![タスク レコーダー オプション](./media/task_recorder_options.png.PNG "タスク レコーダー オプション")</span><span class="sxs-lookup"><span data-stu-id="bb634-128">![Task recorder options](./media/task_recorder_options.png.PNG "Task recorder options")</span></span>

8. <span data-ttu-id="bb634-129">記録を保存するライブラリを選択し、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb634-129">Select the library that you want to save the recording to, and then click **Save**.</span></span> <span data-ttu-id="bb634-130">それ以外の場合、**ディスクに保存** を選択し、次のセクション「BPM に AXTR ファイルをアップロードする」の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bb634-130">Otherwise, select **Save to Disk** and follow the steps in the next section, "Upload an AXTR file to BPM."</span></span>

### <a name="upload-an-axtr-file-to-bpm"></a><span data-ttu-id="bb634-131">BPM に AXTR ファイルをアップロード</span><span class="sxs-lookup"><span data-stu-id="bb634-131">Upload an AXTR file to BPM</span></span> 

1. <span data-ttu-id="bb634-132">Lifecycle Services (LCS) で、プロジェクトの**業務プロセス ライブラリ** ページで、タスク記録をアップロードするライブラリを選択します。</span><span class="sxs-lookup"><span data-stu-id="bb634-132">In Lifecycle Services (LCS), in your project, on the **Business process libraries** page, select the library to upload the task recording to.</span></span>
2. <span data-ttu-id="bb634-133">**作成と編集**をクリックして、明細行内で、タスク記録をアップロードするプロセスを特定し選択します。</span><span class="sxs-lookup"><span data-stu-id="bb634-133">Click **Author and edit** and in the lines, locate and select the process to upload the task recording to.</span></span>
3. <span data-ttu-id="bb634-134">右ウィンドウで**アップロード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb634-134">In the right pane, click **Upload**.</span></span> 

<span data-ttu-id="bb634-135">![AXTR 1 のアップロード](./media/upload_axtr_1.png.PNG "AXTR 1 のアップロード")</span><span class="sxs-lookup"><span data-stu-id="bb634-135">![Upload AXTR 1](./media/upload_axtr_1.png.PNG "Upload AXTR 1")</span></span>

4. <span data-ttu-id="bb634-136">**参照**をクリックして、アップロードするファイルを検索して選択し、次に**アップロード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb634-136">Click **Browse** to find and select the file to upload, and then click **Upload**.</span></span>

<span data-ttu-id="bb634-137">![AXTR 2 のアップロード](./media/upload_axtr_2.png.PNG "AXTR 2 のアップロード")</span><span class="sxs-lookup"><span data-stu-id="bb634-137">![Upload AXTR 2](./media/upload_axtr_2.png.PNG "Upload AXTR 2")</span></span>

### <a name="save-an-existing-task-recording-to-bpm"></a><span data-ttu-id="bb634-138">既存のタスク記録を BPM を保存</span><span class="sxs-lookup"><span data-stu-id="bb634-138">Save an existing task recording to BPM</span></span>

1. <span data-ttu-id="bb634-139">既存のタスクの記録を添付するには、クライアントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="bb634-139">To attach an existing task recording, sign in to the client.</span></span>
2. <span data-ttu-id="bb634-140">**設定** > **タスク レコーダー**に移動します。</span><span class="sxs-lookup"><span data-stu-id="bb634-140">Go to **Settings** > **Task recorder**.</span></span>
3. <span data-ttu-id="bb634-141">**タスクの記録を編集** を選択し、LCS に直接を保存するか、AXTR にダウンロードしてから BPM にアップグレードすることによって、そのファイルを添付します。</span><span class="sxs-lookup"><span data-stu-id="bb634-141">Select **Edit Task Recording** and attach the file by either saving directly to LCS or downloading the AXTR and then uploading to BPM.</span></span>

## <a name="sync-with-vsts"></a><span data-ttu-id="bb634-142">VSTS と同期</span><span class="sxs-lookup"><span data-stu-id="bb634-142">Sync with VSTS</span></span>   

<span data-ttu-id="bb634-143">次に、VSTS プロジェクトと BPM ライブラリを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb634-143">Next, you'll need to synchronize your BPM library with your VSTS project.</span></span> <span data-ttu-id="bb634-144">詳細については、「[LCS プロジェクトのコンフィギュレーションおよび LCS に接続](synchronize-bpm-vsts.md#configure-your-lcs-project-to-connect-to-vsts)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb634-144">For more information, see [Configure your LCS project and connect to LCS](synchronize-bpm-vsts.md#configure-your-lcs-project-to-connect-to-vsts).</span></span> 

<span data-ttu-id="bb634-145">コンフィギュレーションが完了した後、VSTS プロジェクトと BPM ライブラリを同期します。</span><span class="sxs-lookup"><span data-stu-id="bb634-145">After configuration is complete, synchronize the BPM library with a VSTS project.</span></span>
1. <span data-ttu-id="bb634-146">**業務プロセス ライブラリ**ページで、同期するライブラリのタイルの省略記号ボタン (...) を選択し、**VSTS 同期**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb634-146">On the **Business process libraries** page, on the tile for the library that you want to synchronize, select the ellipsis button (…), and then select **VSTS sync**.</span></span>

<span data-ttu-id="bb634-147">![VSTS Sync1](./media/vsts_sync_1.png.png "VSTS Sync1")</span><span class="sxs-lookup"><span data-stu-id="bb634-147">![VSTS Sync1](./media/vsts_sync_1.png.png "VSTS Sync1")</span></span>

<span data-ttu-id="bb634-148">また、BPM ライブラリ内のツールバーから VSTS 同期を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="bb634-148">You can also start VSTS synchronization from the toolbar in a BPM library.</span></span> <span data-ttu-id="bb634-149">省略記号ボタン (...) を選択し、**VSTS の同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb634-149">Select the ellipsis button (…), and then select **VSTS sync**.</span></span>

<span data-ttu-id="bb634-150">![VSTS Sync2](./media/vsts_sync_2.png.png "VSTS Sync2")</span><span class="sxs-lookup"><span data-stu-id="bb634-150">![VSTS Sync2](./media/vsts_sync_2.png.png "VSTS Sync2")</span></span>

2. <span data-ttu-id="bb634-151">VSTS の同期が完了した後、省略記号ボタン (…) を選択し、**テスト ケースの同期**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb634-151">After VSTS synchronization is complete, select the ellipsis button (…), and then select **Sync test cases**.</span></span>

<span data-ttu-id="bb634-152">![テスト ケースの同期](./media/sync_test_case.png.PNG "テスト ケースの同期")</span><span class="sxs-lookup"><span data-stu-id="bb634-152">![Sync test cases](./media/sync_test_case.png.PNG "Sync test cases")</span></span>

3. <span data-ttu-id="bb634-153">このステップが完了したら、タスク記録は VSTS のテスト_ケースになり、**要件** タブの下にリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb634-153">When this step is complete, your task recordings will become test cases in VSTS and a link will appear under the **Requirements** tab.</span></span> 

<span data-ttu-id="bb634-154">![テスト ケースの表示](./media/view_test_case.png.PNG "テスト ケースの表示")</span><span class="sxs-lookup"><span data-stu-id="bb634-154">![View test case](./media/view_test_case.png.PNG "View test case")</span></span>


<span data-ttu-id="bb634-155">テスト ステップに加えて、タスクを記録する XML ファイルが VSTS テスト ケースに付属します。</span><span class="sxs-lookup"><span data-stu-id="bb634-155">In addition to the test steps, the task recording XML file is attached to the VSTS test case.</span></span> <span data-ttu-id="bb634-156">テストの実行を自動化する場合、このファイルを必要とします。</span><span class="sxs-lookup"><span data-stu-id="bb634-156">This file will be needed if you want to automate test execution.</span></span> 

## <a name="create-a-test-suite-in-vsts"></a><span data-ttu-id="bb634-157">VSTS でテスト スイートを作成する</span><span class="sxs-lookup"><span data-stu-id="bb634-157">Create a test suite in VSTS</span></span>

<span data-ttu-id="bb634-158">次に、VSTS でテスト スイートを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb634-158">Next, you will need to create a test suite in VSTS.</span></span> <span data-ttu-id="bb634-159">これにより一連のテストを実行できるので、結果の管理、調査、追跡が容易になります。</span><span class="sxs-lookup"><span data-stu-id="bb634-159">This will allow you to run a suite of tests so you can easily manage, investigate, and track the results.</span></span> 

1. <span data-ttu-id="bb634-160">VSTS にログインし、テストするプロジェクトとテスト計画を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb634-160">Sign in to VSTS and select the project and test plan that you want to test in.</span></span> 
2. <span data-ttu-id="bb634-161">ツール バーで、**テスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb634-161">On the toolbar, select **Test**.</span></span>
3. <span data-ttu-id="bb634-162">左ウィンドウで、**+** を選択してから、**静的スイート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb634-162">In the left pane, select **+**, and then select **Static suite**.</span></span> 
4. <span data-ttu-id="bb634-163">スイート名を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb634-163">Enter a name for the suite.</span></span>
5. <span data-ttu-id="bb634-164">**既存の追加**をクリックし、**LCS:Test Cases** タグを照会します。</span><span class="sxs-lookup"><span data-stu-id="bb634-164">Click **Add existing** and query the tag **LCS:Test Cases**.</span></span>
6. <span data-ttu-id="bb634-165">**実行** > **テスト ケースの追加**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb634-165">Click **Run** > **Add test cases**.</span></span>

<span data-ttu-id="bb634-166">![テスト ケースの追加](./media/add_test_cases.PNG "テスト ケースの追加")</span><span class="sxs-lookup"><span data-stu-id="bb634-166">![Add test cases](./media/add_test_cases.PNG "Add test cases")</span></span>
 
7. <span data-ttu-id="bb634-167">詳細と関連付けられている XML ファイルを表示し、作業項目を作成するには、テスト ケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="bb634-167">Select the test case to view details and the attached XML file, and to create a work item.</span></span>   

<span data-ttu-id="bb634-168">![テスト ケースの詳細](./media/test_case_details.png.PNG "テスト ケースの詳細")</span><span class="sxs-lookup"><span data-stu-id="bb634-168">![Test case details](./media/test_case_details.png.PNG "Test case details")</span></span>

 >[!NOTE]
 > <span data-ttu-id="bb634-169">この例は、すべてのテスト ケースが追加された包括的受入れテスト スイートを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bb634-169">This example shows how to create a comprehensive acceptance test suite with all test cases added.</span></span> <span data-ttu-id="bb634-170">さまざまなテスト スイートを作成して、カスタム クエリを使用し特定のテスト ケースを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="bb634-170">You can create various test suites and use custom queries to add specific test cases.</span></span> 

### <a name="run-manual-test-cases"></a><span data-ttu-id="bb634-171">手動テスト ケースを実行</span><span class="sxs-lookup"><span data-stu-id="bb634-171">Run manual test cases</span></span>

<span data-ttu-id="bb634-172">テスト スイートがある場合、サンドボックスおよびテスト環境で Dynamics 365 for Finance and Operations アプリケーションが更新された後、回帰テストを使用する準備ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="bb634-172">After you have a test suite, you are ready to use it for regression testing after updates have been made to your Dynamics 365 for Finance and Operations application in a sandbox or test environment.</span></span> <span data-ttu-id="bb634-173">テスト スイートで手動でテスト ケースを実行、またはテスト スイートの一部であるタスク記録を再生し、VSTS を使用してテスト ケースを成功または失敗としてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="bb634-173">You can run the test cases in your test suite manually or play the task recordings that are part of the test suite and use VSTS to mark the test cases as passed or failed.</span></span>

<span data-ttu-id="bb634-174">![マーク済み VSTS テスト](./media/vsts_test_marked.png.png "マーク済み VSTS テスト")</span><span class="sxs-lookup"><span data-stu-id="bb634-174">![VSTS test marked](./media/vsts_test_marked.png.png "VSTS test marked")</span></span>

<span data-ttu-id="bb634-175">VSTS は、**テスト ランナー** というツールを提供して、手動テスト ケースの実行も管理します。</span><span class="sxs-lookup"><span data-stu-id="bb634-175">VSTS also provides a tool, **Test Runner**, to manage manual test case execution.</span></span> <span data-ttu-id="bb634-176">テスト ランナーの使用の詳細については、[手動テストの実行](https://docs.microsoft.com/en-us/vsts/manual-test/getting-started/run-manual-tests) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb634-176">For more information about using Test Runner, see [Run manual tests](https://docs.microsoft.com/en-us/vsts/manual-test/getting-started/run-manual-tests).</span></span>

<span data-ttu-id="bb634-177">VSTS はテストだけでなく、結果の管理と軽減策のための豊富な管理機能セットを提供するので、VSTS の活用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bb634-177">We recommend that you take advantage of VSTS as it provides a rich set of management features not only for testing, but result management and mitigation.</span></span>

### <a name="run-automated-test-cases"></a><span data-ttu-id="bb634-178">自動テスト ケースを実行</span><span class="sxs-lookup"><span data-stu-id="bb634-178">Run automated test cases</span></span>

<span data-ttu-id="bb634-179">Dynamics 365 Unified Operations プラットフォームは、タスク記録に基づいてテスト ケースを作成し、VSTS を使用してそれらのテスト ケースの自動実行を管理するためのツールを開発者を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb634-179">The Dynamics 365 Unified Operations platform provides developers with tools to author test cases based on task recordings and use VSTS to manage the automated execution of these test cases.</span></span> <span data-ttu-id="bb634-180">テスト ケースの実行は、**ビルドおよびテスト**環境トポロジのビルドおよびテストの自動化機能の一部です。</span><span class="sxs-lookup"><span data-stu-id="bb634-180">Execution of test cases are part of the build and test automation capabilities of **build and test** environment topologies.</span></span>
<span data-ttu-id="bb634-181">詳細については、[継続的な配信ホーム ページ](../dev-tools/continuous-delivery-home-page.md) および [開発 ALM ブログ](http://blogs.msdn.microsoft.com/axdevalm/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb634-181">For details, see the [Continuous delivery home page](../dev-tools/continuous-delivery-home-page.md) and the [Dev ALM blog](http://blogs.msdn.microsoft.com/axdevalm/).</span></span>

