---
title: ユーザー受け入れテストの作成と自動化
description: このトピックでは、タスク ガイドと BPM を 使用して承認テスト スイートを作成および実行することに関する情報を提供します。
author: jorisdg
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 32030c50551ebf4cc6619f692c91f76071b2c799
ms.sourcegitcommit: 990dd96d1dcd462928aa0029ff84a8185198e5de
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2020
ms.locfileid: "3287837"
---
# <a name="create-and-automate-user-acceptance-tests"></a><span data-ttu-id="332fc-103">ユーザー受け入れテストの作成と自動化</span><span class="sxs-lookup"><span data-stu-id="332fc-103">Create and automate user acceptance tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="332fc-104">タスク レコーダーおよびビジネス プロセス モデラー (BPM) を使用して、ユーザー承認テスト ライブラリを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="332fc-104">You can use Task recorder and Business process modeler (BPM) to create user acceptance test libraries.</span></span> <span data-ttu-id="332fc-105">タスク レコーダーは、テスト ケースを記録し、BPM を使用して業務プロセス別に整理する強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="332fc-105">Task recorder is a powerful tool to record test cases and organize them by business process using BPM.</span></span> <span data-ttu-id="332fc-106">Microsoft パートナーは、BPM を使用して LCS および LCS ソリューション経由で顧客にテスト ライブラリを配布することができます。</span><span class="sxs-lookup"><span data-stu-id="332fc-106">As a Microsoft partner you can use BPM to distribute test libraries to your customers via LCS and LCS solutions.</span></span> <span data-ttu-id="332fc-107">顧客の場合、BPM を使用し、さまざまなプロジェクトおよびチーム間でテスト ライブラリを作成して配布します。</span><span class="sxs-lookup"><span data-stu-id="332fc-107">If you are a customer, use BPM to author and distribute test libraries across different projects and team.</span></span>

<span data-ttu-id="332fc-108">BPM は Azure DevOps (旧 Visual Studio Team Services) と同期することができるので、Azure DevOps プロジェクトでテスト ケース (テスト ステップを含む) を自動的に作成できます。</span><span class="sxs-lookup"><span data-stu-id="332fc-108">Because BPM can be synchronized with Azure DevOps (formerly known as Visual Studio Team Services), you can automatically create test cases (including test steps) in your Azure DevOps project.</span></span> <span data-ttu-id="332fc-109">その後、Azure DevOps は、対象となるテスト計画およびテスト スイートを作成して、テストの実行を管理し、結果を調査できるテスト構成およびテスト管理ツールとして動作できます。</span><span class="sxs-lookup"><span data-stu-id="332fc-109">Azure DevOps can then serve as your test configuration and test management tool where you can create targeted test plans and test suites, manage the execution of tests and investigate results.</span></span> <span data-ttu-id="332fc-110">Azure DevOps を使用したテストの詳細については、[テスト計画、テスト スイート、テスト ケースとは?](https://docs.microsoft.com/azure/devops/test/create-a-test-plan?view=azure-devops#what-are-test-plans-test-suites-and-test-cases) を参照してください</span><span class="sxs-lookup"><span data-stu-id="332fc-110">For more information about testing with Azure DevOps, see [What are test plans, test suites, and test cases?](https://docs.microsoft.com/azure/devops/test/create-a-test-plan?view=azure-devops#what-are-test-plans-test-suites-and-test-cases)</span></span>

<span data-ttu-id="332fc-111">このトピックでは、手動テストまたは自動テストに使用する承認テスト スイートを作成および実行するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="332fc-111">This topic walks through the process of creating and executing acceptance test suites to be used for manual or automated testing.</span></span>

## <a name="create-a-scenario-acceptance-testing-bpm-library"></a><span data-ttu-id="332fc-112">シナリオ承認テスト BPM ライブラリの作成</span><span class="sxs-lookup"><span data-stu-id="332fc-112">Create a Scenario Acceptance Testing BPM library</span></span>
<span data-ttu-id="332fc-113">BPM は、業務プロセスおよびユーザー タスクの階層を記述する優れた LCS ツールです。</span><span class="sxs-lookup"><span data-stu-id="332fc-113">BPM is a great LCS tool to describe a hierarchy of business processes and user tasks.</span></span> <span data-ttu-id="332fc-114">LCS では Microsoft パートナーおよび顧客がアセット ライブラリ経由で LCS プロジェクト間の BPM ライブラリを作成し配布することもできます。</span><span class="sxs-lookup"><span data-stu-id="332fc-114">LCS also allows Microsoft partners and customers to author and distribute BPM libraries across LCS projects via the Asset library.</span></span> <span data-ttu-id="332fc-115">このセクションでは、承認テスト ライブラリを定義する BPM を活用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="332fc-115">This section describes how to take advantage of BPM to define your acceptance test library.</span></span>

### <a name="create-a-bpm-library"></a><span data-ttu-id="332fc-116">BPM ライブラリの作成</span><span class="sxs-lookup"><span data-stu-id="332fc-116">Create a BPM library</span></span>
<span data-ttu-id="332fc-117">ビジネス プロセス モデラー (BPM) ライブラリを作成するにはいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="332fc-117">There are several ways to create a Business process modeler (BPM) library.</span></span> <span data-ttu-id="332fc-118">BPM でライブラリを作成する方法の詳細については、[BPM ライブラリの作成、編集、および参照](creating-editing-browsing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332fc-118">For more information about how to create libraries in BPM, see [Create, edit, and browse Business process modeler (BPM) libraries](creating-editing-browsing.md).</span></span>

<span data-ttu-id="332fc-119">説明目的で、このトピックでは、経費精算書の作成および注文要求の承認などの一般的な業務プロセスを含むライブラリを使用します。</span><span class="sxs-lookup"><span data-stu-id="332fc-119">For illustration purposes, this topic uses a library that contains common business processes, such as create an expense report and approve order requests.</span></span> <span data-ttu-id="332fc-120">Excel インポート機能を使用してライブラリを作成しました。</span><span class="sxs-lookup"><span data-stu-id="332fc-120">The library was created by using the Excel import functionality.</span></span>  

<span data-ttu-id="332fc-121">![Excel からインポート](./media/import-from-excel.PNG "Excel からインポート")</span><span class="sxs-lookup"><span data-stu-id="332fc-121">![Import from Excel](./media/import-from-excel.PNG "Import from Excel")</span></span>

### <a name="record-test-cases-and-save-to-bpm"></a><span data-ttu-id="332fc-122">テスト ケースを記録して BPM に保存</span><span class="sxs-lookup"><span data-stu-id="332fc-122">Record test cases and save to BPM</span></span> 

<span data-ttu-id="332fc-123">BPMライブラリを作成した後は、タスク レコーダーを使用してテスト ケースを作成し、それから BPM にそのケースをアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="332fc-123">After you have created a BPM library, you'll need to use Task recorder to create your test cases and then upload the cases to BPM.</span></span> <span data-ttu-id="332fc-124">これを行うにはいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="332fc-124">There are several ways to do this.</span></span> 

<span data-ttu-id="332fc-125">既に必要なタスク記録 (テスト ケース) が付属されている BPM ライブラリを使用している場合、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="332fc-125">If you're using a BPM library that already has all of the necessary task recordings (test cases) attached, you can skip this step.</span></span> <span data-ttu-id="332fc-126">それ以外の場合、新しいタスク記録を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="332fc-126">Otherwise, follow the instructions below to create new task recordings.</span></span>

#### <a name="create-and-save-a-new-task-recording"></a><span data-ttu-id="332fc-127">新しいタスク記録を作成して保存する</span><span class="sxs-lookup"><span data-stu-id="332fc-127">Create and save a new task recording</span></span>
1. <span data-ttu-id="332fc-128">クライアントを開いて、サインインします。</span><span class="sxs-lookup"><span data-stu-id="332fc-128">Open the client and sign in.</span></span> 
2. <span data-ttu-id="332fc-129">記録中に使用する会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="332fc-129">Select the company that you want to use while recording.</span></span>
3. <span data-ttu-id="332fc-130">**設定** > **タスク レコーダー**に移動します。</span><span class="sxs-lookup"><span data-stu-id="332fc-130">Go to **Settings** > **Task recorder**.</span></span>

    <span data-ttu-id="332fc-131">![タスク レコーダーの選択](./media/select_task_recorder.PNG "タスク レコーダーの選択。")。</span><span class="sxs-lookup"><span data-stu-id="332fc-131">![Select Task recorder](./media/select_task_recorder.PNG "Select Task recorder")</span></span>

4. <span data-ttu-id="332fc-132">**新しい記録の作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="332fc-132">Click **Create a new recording**.</span></span>
5. <span data-ttu-id="332fc-133">コンフィギュレーション名を入力し、**開始**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="332fc-133">Enter a name for the recording, and then click **Start**.</span></span> <span data-ttu-id="332fc-134">記録は、**開始** をクリックすると開始されます。</span><span class="sxs-lookup"><span data-stu-id="332fc-134">Recording begins the moment that you click **Start**.</span></span>
6. <span data-ttu-id="332fc-135">記録が完了したら、タスク レコーダー ウィンドウで、**停止** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="332fc-135">When the recording is complete, in the Task recorder pane, click **Stop**.</span></span>
7. <span data-ttu-id="332fc-136">添付された BPM にタスク記録を保存するには、**Lifecycle Services に保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="332fc-136">To save the task recording to an attached BPM, click **Save to Lifecycle Services**.</span></span>

    <span data-ttu-id="332fc-137">![タスク レコーダー オプション](./media/task_recorder_options.PNG "タスク レコーダー オプション")</span><span class="sxs-lookup"><span data-stu-id="332fc-137">![Task recorder options](./media/task_recorder_options.PNG "Task recorder options")</span></span>

8. <span data-ttu-id="332fc-138">記録を保存するライブラリを選択し、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="332fc-138">Select the library that you want to save the recording to, and then click **Save**.</span></span> <span data-ttu-id="332fc-139">それ以外の場合、**ディスクに保存** を選択し、次のセクション「BPM に AXTR ファイルをアップロードする」の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="332fc-139">Otherwise, select **Save to Disk** and follow the steps in the next section, "Upload an AXTR file to BPM."</span></span>

 >[!NOTE]
 > <span data-ttu-id="332fc-140">自動化ツールを使用して、テストの有効な実行を有効にするには、タスク記録がすべてアプリケーションの主要なダッシュボードで開始することを確認します。</span><span class="sxs-lookup"><span data-stu-id="332fc-140">To enable the effective execution of your tests using automation tools, make sure all of your task recordings start on the main dashboard of your application.</span></span>
 > <span data-ttu-id="332fc-141">複数のユーザーによって実行されるエンド ツー エンド プロセスの場合、ユーザー固有のタスクにタスク記録を分割することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="332fc-141">For end-to-end processes that are performed by more than one user, we recommend that you divide your task recordings into user-specific tasks.</span></span> <span data-ttu-id="332fc-142">これにより、テスト ケースの保守作業を簡素化され、セキュリティ ロールのコンテキストでテスト ケースを実行することができます。これはベスト プラクティスです。</span><span class="sxs-lookup"><span data-stu-id="332fc-142">This simplifies the maintenance of test cases and allows you to execute test cases in the context of security roles, which is a best a practice.</span></span> 

#### <a name="upload-an-axtr-file-to-bpm"></a><span data-ttu-id="332fc-143">BPM に AXTR ファイルをアップロード</span><span class="sxs-lookup"><span data-stu-id="332fc-143">Upload an AXTR file to BPM</span></span>
<span data-ttu-id="332fc-144">ディスクに記録 (AXTR ファイル) を保存した場合、以下の手順に従って BPM にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="332fc-144">If you have saved your recordings (AXTR files) to disk, follow these steps to upload them to BPM.</span></span>

1. <span data-ttu-id="332fc-145">Lifecycle Services (LCS) で、プロジェクトの**業務プロセス ライブラリ** ページで、タスク記録をアップロードするライブラリを選択します。</span><span class="sxs-lookup"><span data-stu-id="332fc-145">In Lifecycle Services (LCS), in your project, on the **Business process libraries** page, select the library to upload the task recording to.</span></span>
2. <span data-ttu-id="332fc-146">**作成と編集**をクリックして、明細行内で、タスク記録をアップロードするプロセスを特定し選択します。</span><span class="sxs-lookup"><span data-stu-id="332fc-146">Click **Author and edit** and in the lines, locate and select the process to upload the task recording to.</span></span>
3. <span data-ttu-id="332fc-147">右ウィンドウで**アップロード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="332fc-147">In the right pane, click **Upload**.</span></span> 

    <span data-ttu-id="332fc-148">![AXTR 1 のアップロード:](./media/upload_axtr_1.PNG "AXTR 1 のアップロード:")</span><span class="sxs-lookup"><span data-stu-id="332fc-148">![Upload AXTR 1](./media/upload_axtr_1.PNG "Upload AXTR 1")</span></span>

4. <span data-ttu-id="332fc-149">**参照**をクリックして、アップロードするファイルを検索して選択し、次に**アップロード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="332fc-149">Click **Browse** to find and select the file to upload, and then click **Upload**.</span></span>

    <span data-ttu-id="332fc-150">![AXTR 2 のアップロード:](./media/upload_axtr_2.PNG "AXTR 2 のアップロード:")</span><span class="sxs-lookup"><span data-stu-id="332fc-150">![Upload AXTR 2](./media/upload_axtr_2.PNG "Upload AXTR 2")</span></span>

#### <a name="save-an-existing-task-recording-to-bpm"></a><span data-ttu-id="332fc-151">既存のタスク記録を BPM を保存</span><span class="sxs-lookup"><span data-stu-id="332fc-151">Save an existing task recording to BPM</span></span>
1. <span data-ttu-id="332fc-152">既存のタスクの記録を添付するには、クライアントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="332fc-152">To attach an existing task recording, sign in to the client.</span></span>
2. <span data-ttu-id="332fc-153">**設定** > **タスク レコーダー**に移動します。</span><span class="sxs-lookup"><span data-stu-id="332fc-153">Go to **Settings** > **Task recorder**.</span></span>
3. <span data-ttu-id="332fc-154">**タスクの記録を編集** を選択し、LCS に直接を保存するか、AXTR にダウンロードしてから BPM にアップグレードすることによって、そのファイルを添付します。</span><span class="sxs-lookup"><span data-stu-id="332fc-154">Select **Edit Task Recording** and attach the file by either saving directly to LCS or downloading the AXTR and then uploading to BPM.</span></span>

### <a name="guidelines-for-recording-test-cases"></a><span data-ttu-id="332fc-155">テスト ケースを記録するためのガイドライン</span><span class="sxs-lookup"><span data-stu-id="332fc-155">Guidelines for recording test cases</span></span>

<span data-ttu-id="332fc-156">テスト ケースを作成して記録するとき、特にテストの実行を自動化する予定がある場合は、次のガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="332fc-156">Follow these guidelines when authoring and recording your test cases, especially if you are planning to automate test execution.</span></span>
<span data-ttu-id="332fc-157">ここで説明されているプロセスおよびツールは、業務プロセスの受け入れテストに適用されます。</span><span class="sxs-lookup"><span data-stu-id="332fc-157">The process and tools described in this article apply to business process acceptance tests.</span></span> <span data-ttu-id="332fc-158">通常の開発者によって所有されているコンポーネントおよび単体テストを交換するためではありません。</span><span class="sxs-lookup"><span data-stu-id="332fc-158">They are not meant to replace component and unit testing that is typically owned by developers.</span></span>

- <span data-ttu-id="332fc-159">組み合わせるとエンド ツー エンド プロセス全体をカバーする限られた数のテスト ケースを作成します。</span><span class="sxs-lookup"><span data-stu-id="332fc-159">Author a limited number of test cases that, when combined, cover complete end-to-end processes.</span></span>
- <span data-ttu-id="332fc-160">カスタマイズされている業務プロセスに焦点を当てててください。</span><span class="sxs-lookup"><span data-stu-id="332fc-160">Focus on business processes that have been customized.</span></span>
- <span data-ttu-id="332fc-161">個々のテスト ケース (記録) は、通常は 1 人のユーザーによって実行される、1 つか 2 つの業務のみを対象としてください。</span><span class="sxs-lookup"><span data-stu-id="332fc-161">An individual test case (recording) should cover one or two business tasks only, typically executed by one person.</span></span> <span data-ttu-id="332fc-162">これにより、タスク記録メンテナンスが簡略化されます。</span><span class="sxs-lookup"><span data-stu-id="332fc-162">This simplifies task recording maintenance.</span></span> <span data-ttu-id="332fc-163">1 つの大きなタスクの記録に「調達から支払」や「注文から現金」などの包括的なエンド ツー エンド ビジネス プロセスを組み合わせることはしないでください。</span><span class="sxs-lookup"><span data-stu-id="332fc-163">Do not combine a complete end-to-end business process such as "Procure to Pay" or "Order to Cash" into one large task recording.</span></span> <span data-ttu-id="332fc-164">たとえば、RFQ > 発注書 > 製品受領書 > 仕入先請求書 > 仕入先支払を 1 つのテスト ケースとするのではなく、3 つか 4 つのテスト ケースにプロセスを分割します。</span><span class="sxs-lookup"><span data-stu-id="332fc-164">For example, instead of having RFQ > Purchase Order > Product Receipt > Vendor Invoice > Vendor Payment as one test case, divide the process into three or four test cases.</span></span> <span data-ttu-id="332fc-165">これらのテストを後で順序指定テスト スイートに組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="332fc-165">You will have the opportunity to combine these tests into an ordered test suite later.</span></span>
- <span data-ttu-id="332fc-166">テスト ケースでは、少なくとも 1 つの検証が必要です。</span><span class="sxs-lookup"><span data-stu-id="332fc-166">A test case should have at least one validation.</span></span> <span data-ttu-id="332fc-167">その他のフィールドの影響をカバーする重要なフィールドを検証するには、このようにしてください。</span><span class="sxs-lookup"><span data-stu-id="332fc-167">Try to validate critical fields that cover the impact of other fields.</span></span> <span data-ttu-id="332fc-168">例: 売上または発注書の合計が単位価格/数量/割引/税金をカバーするかの検証など。</span><span class="sxs-lookup"><span data-stu-id="332fc-168">For example: Validation of totals on sales or purchase orders cover the unit price/quantity/discount/tax ...etc.</span></span>
- <span data-ttu-id="332fc-169">テスト ケースのレポートを印刷しないようにします。</span><span class="sxs-lookup"><span data-stu-id="332fc-169">Avoid printing a report in a test case.</span></span> <span data-ttu-id="332fc-170">テスト ケースでレポートを印刷する必要がある場合は、画面で選択してください。</span><span class="sxs-lookup"><span data-stu-id="332fc-170">If a test case needs to print a report, it should be selected on screen.</span></span>
- <span data-ttu-id="332fc-171">テスト ケースの 80% 以上は、トランザクションや元伝票にしてください。</span><span class="sxs-lookup"><span data-stu-id="332fc-171">80+% of test cases should be of transactions or source documents.</span></span> <span data-ttu-id="332fc-172">マスタ データは、テスト ケースの最大 20% に限定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="332fc-172">Master data should be limited to up to 20% of test cases only.</span></span>

## <a name="synchronize-and-configure-your-test-plan-in-azure-devops"></a><span data-ttu-id="332fc-173">Azure DevOps でテスト計画の同期およびコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="332fc-173">Synchronize and configure your test plan in Azure DevOps</span></span>

<span data-ttu-id="332fc-174">引受テスト ライブラリは、開始点です。</span><span class="sxs-lookup"><span data-stu-id="332fc-174">An acceptance test library is your starting point.</span></span> <span data-ttu-id="332fc-175">通常、業務プロセス別に分類されている特定のアプリケーションのすべてのテスト ケース (タスク記録) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="332fc-175">It typically contains all test cases (task recordings) of a particular application organized by business process.</span></span> <span data-ttu-id="332fc-176">特定のテスト パスの間、通常はすべてのテスト ケースを実行する必要があるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="332fc-176">During a particular test pass, you usually do not need to execute all test cases.</span></span> <span data-ttu-id="332fc-177">選択したテスト ケースが実装のフェーズまたは更新の性質に依存している場合、実稼働環境に適用するよう計画します。</span><span class="sxs-lookup"><span data-stu-id="332fc-177">What test cases you select depends on the phase of your implementation or the nature of the update you are planning to apply to your production environment.</span></span> <span data-ttu-id="332fc-178">Azure DevOps を使用すると、テスト計画およびテスト スイートでテスト ケースを整理できます。</span><span class="sxs-lookup"><span data-stu-id="332fc-178">Azure DevOps enables you to organize your test cases in test plans and test suites.</span></span> <span data-ttu-id="332fc-179">テスト計画には、1 つまたは複数のテストスイート (テスト ライブラリのサブセット) が含まれています。テスト ケースは、1 つ以上のテスト スイートに属することができます。</span><span class="sxs-lookup"><span data-stu-id="332fc-179">A test plan contains one or more test suites (A subset of your test library); test cases can belong to more than one test suite.</span></span>

<span data-ttu-id="332fc-180">承認テスト BPM ライブラリを一度選択すると、Azure DevOps と同期してテスト計画およびテスト スイートを作成します。</span><span class="sxs-lookup"><span data-stu-id="332fc-180">Once you have selected your acceptance testing BPM library, synchronize it with Azure DevOps and create your test plan and test suites.</span></span>

### <a name="sync-with-azure-devops"></a><span data-ttu-id="332fc-181">Azure DevOps との同期</span><span class="sxs-lookup"><span data-stu-id="332fc-181">Sync with Azure DevOps</span></span>
<span data-ttu-id="332fc-182">Azure DevOps プロジェクトと BPM ライブラリを同期します。</span><span class="sxs-lookup"><span data-stu-id="332fc-182">Synchronize your BPM library with your Azure DevOps project.</span></span> <span data-ttu-id="332fc-183">詳細については、[BPM ライブラリの Azure DevOps との同期について](synchronize-bpm-vsts.md#configure-your-lcs-project-to-connect-to-azure-devops) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332fc-183">For more information, see [Synchronize BPM libraries with Azure DevOps](synchronize-bpm-vsts.md#configure-your-lcs-project-to-connect-to-azure-devops).</span></span> 

<span data-ttu-id="332fc-184">コンフィギュレーションが完了した後、Azure DevOps プロジェクトと BPM ライブラリを同期します。</span><span class="sxs-lookup"><span data-stu-id="332fc-184">After configuration is complete, synchronize the BPM library with a Azure DevOps project.</span></span>
1. <span data-ttu-id="332fc-185">**業務プロセス ライブラリ**ページで、同期するライブラリのタイルの省略記号ボタン (...) を選択し、**Azure DevOps 同期**を選択します。</span><span class="sxs-lookup"><span data-stu-id="332fc-185">On the **Business process libraries** page, on the tile for the library that you want to synchronize, select the ellipsis button (…), and then select **Azure DevOps sync**.</span></span>

    <span data-ttu-id="332fc-186">![VSTS Sync1](./media/vsts_sync_1.png "VSTS Sync1")</span><span class="sxs-lookup"><span data-stu-id="332fc-186">![VSTS Sync1](./media/vsts_sync_1.png "VSTS Sync1")</span></span>

    <span data-ttu-id="332fc-187">また、BPM ライブラリ内のツールバーから Azure DevOps 同期を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="332fc-187">You can also start Azure DevOps synchronization from the toolbar in a BPM library.</span></span> <span data-ttu-id="332fc-188">省略記号ボタン (...) を選択し、**Azure DevOps の同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="332fc-188">Select the ellipsis button (…), and then select **Azure DevOps sync**.</span></span>

    <span data-ttu-id="332fc-189">![VSTS Sync2](./media/vsts_sync_2.png "VSTS Sync2")</span><span class="sxs-lookup"><span data-stu-id="332fc-189">![VSTS Sync2](./media/vsts_sync_2.png "VSTS Sync2")</span></span>

2. <span data-ttu-id="332fc-190">Azure DevOps の同期が完了した後、省略記号ボタン (…) を選択し、**テスト ケースの同期**を選択します。</span><span class="sxs-lookup"><span data-stu-id="332fc-190">After Azure DevOps synchronization is complete, select the ellipsis button (…), and then select **Sync test cases**.</span></span>

    <span data-ttu-id="332fc-191">![テスト ケースの同期](./media/sync_test_case.PNG "テスト ケースの同期")</span><span class="sxs-lookup"><span data-stu-id="332fc-191">![Sync test cases](./media/sync_test_case.PNG "Sync test cases")</span></span>

3. <span data-ttu-id="332fc-192">このステップが完了したら、タスク記録は Azure DevOps のテスト ケースになり、**要件** タブの下にリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="332fc-192">When this step is complete, your task recordings will become test cases in Azure DevOps and a link will appear under the **Requirements** tab.</span></span> 

    <span data-ttu-id="332fc-193">![テスト ケースの表示](./media/view_test_case.PNG "テスト ケースの表示")</span><span class="sxs-lookup"><span data-stu-id="332fc-193">![View test case](./media/view_test_case.PNG "View test case")</span></span>


<span data-ttu-id="332fc-194">テスト ステップに加えて、タスクを記録する XML ファイルが Azure DevOps テスト ケースに付属します。</span><span class="sxs-lookup"><span data-stu-id="332fc-194">In addition to the test steps, the task recording XML file is attached to the Azure DevOps test case.</span></span> <span data-ttu-id="332fc-195">テストの実行を自動化する場合、このファイルを必要とします。</span><span class="sxs-lookup"><span data-stu-id="332fc-195">This file will be needed if you want to automate test execution.</span></span> 

### <a name="create-a-test-suite-in-azure-devops"></a><span data-ttu-id="332fc-196">Azure DevOps でテスト スイートを作成する</span><span class="sxs-lookup"><span data-stu-id="332fc-196">Create a test suite in Azure DevOps</span></span>
<span data-ttu-id="332fc-197">次に、Azure DevOps でテスト計画とスイートを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="332fc-197">Next, you will need to create a test plan and test suite in Azure DevOps.</span></span> <span data-ttu-id="332fc-198">これにより、テスト ケースの順序指定テストを実行できるので、結果の管理、調査、追跡が容易になります。</span><span class="sxs-lookup"><span data-stu-id="332fc-198">This will allow you to execute an ordered suite of test cases and easily manage, investigate, and track the results.</span></span> 

1. <span data-ttu-id="332fc-199">Azure DevOps にログインし、テストするプロジェクトとテスト計画を選択します。</span><span class="sxs-lookup"><span data-stu-id="332fc-199">Sign in to Azure DevOps and select the project and test plan that you want to test in.</span></span> 
2. <span data-ttu-id="332fc-200">ツール バーで、**テスト** > **テスト計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="332fc-200">On the toolbar, select **Test** > **Test Plans**.</span></span>
3. <span data-ttu-id="332fc-201">左ウィンドウで、**+** を選択してから、**静的スイート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="332fc-201">In the left pane, select **+**, and then select **Static suite**.</span></span> 
4. <span data-ttu-id="332fc-202">スイート名を入力します。</span><span class="sxs-lookup"><span data-stu-id="332fc-202">Enter a name for the suite.</span></span>
5. <span data-ttu-id="332fc-203">**既存の追加**をクリックし、**LCS:Test Cases** タグを照会します。</span><span class="sxs-lookup"><span data-stu-id="332fc-203">Click **Add existing** and query the tag **LCS:Test Cases**.</span></span>
6. <span data-ttu-id="332fc-204">**実行** > **テスト ケースの追加**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="332fc-204">Click **Run** > **Add test cases**.</span></span>

    <span data-ttu-id="332fc-205">![テスト ケースの追加](./media/add_test_cases.PNG "テスト ケースの追加")</span><span class="sxs-lookup"><span data-stu-id="332fc-205">![Add test cases](./media/add_test_cases.PNG "Add test cases")</span></span>
 
7. <span data-ttu-id="332fc-206">詳細と関連付けられている XML ファイルを表示するには、テスト ケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="332fc-206">Select the test case to view details and the attached XML file.</span></span>   

    <span data-ttu-id="332fc-207">![テスト ケースの詳細](./media/test_case_details.PNG "テスト ケースの詳細")</span><span class="sxs-lookup"><span data-stu-id="332fc-207">![Test case details](./media/test_case_details.PNG "Test case details")</span></span>

 >[!NOTE]
 > <span data-ttu-id="332fc-208">この例は、すべてのテスト ケースが追加された 1 つの包括的受入れテスト スイートを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="332fc-208">This example shows how to create one comprehensive acceptance test suite with all test cases added.</span></span> <span data-ttu-id="332fc-209">代わりに、同じテスト計画下にさまざまなテスト スイートを作成し、カスタム クエリを使用してテスト スイートに特定のテスト ケースを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="332fc-209">Instead, you should create various test suites under the same test plan and then use custom queries to add specific test cases to a test suite.</span></span> <span data-ttu-id="332fc-210">テスト ケースは、1 つ以上のテスト スイートに属することができます。</span><span class="sxs-lookup"><span data-stu-id="332fc-210">A test case can belong to more than one test suite.</span></span>

## <a name="execute-your-tests"></a><span data-ttu-id="332fc-211">テストを実行します。</span><span class="sxs-lookup"><span data-stu-id="332fc-211">Execute your tests</span></span>

### <a name="run-manual-test-cases"></a><span data-ttu-id="332fc-212">手動テスト ケースを実行</span><span class="sxs-lookup"><span data-stu-id="332fc-212">Run manual test cases</span></span>
<span data-ttu-id="332fc-213">テスト スイートがある場合、サンドボックスおよびテスト環境で アプリケーションが更新された後、回帰テストを使用する準備ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="332fc-213">After you have a test suite, you are ready to use it for regression testing after updates have been made to your application in a sandbox or test environment.</span></span> <span data-ttu-id="332fc-214">テスト スイートで手動でテスト ケースを実行、またはテスト スイートの一部であるタスク記録を再生し、Azure DevOps を使用してテスト ケースを成功または失敗としてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="332fc-214">You can run the test cases in your test suite manually or play the task recordings that are part of the test suite and use Azure DevOps to mark the test cases as passed or failed.</span></span>

<span data-ttu-id="332fc-215">![マーク済み VSTS テスト](./media/vsts_test_marked.png "マーク済み VSTS テスト")</span><span class="sxs-lookup"><span data-stu-id="332fc-215">![VSTS test marked](./media/vsts_test_marked.png "VSTS test marked")</span></span>

<span data-ttu-id="332fc-216">Azure DevOps は、**テスト ランナー** というツールを提供して、手動テスト ケースの実行も管理します。</span><span class="sxs-lookup"><span data-stu-id="332fc-216">Azure DevOps also provides a tool, **Test Runner**, to manage manual test case execution.</span></span> <span data-ttu-id="332fc-217">テスト ランナーの使用の詳細については、[手動テストの実行](https://docs.microsoft.com/vsts/manual-test/getting-started/run-manual-tests) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332fc-217">For more information about using Test Runner, see [Run manual tests](https://docs.microsoft.com/vsts/manual-test/getting-started/run-manual-tests).</span></span>

<span data-ttu-id="332fc-218">Azure DevOps はテストだけでなく、結果の管理と軽減策のための豊富な管理機能セットを提供するので、VSTS の活用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="332fc-218">We recommend that you take advantage of Azure DevOps as it provides a rich set of management features not only for testing, but result management and mitigation.</span></span>

### <a name="run-automated-test-cases"></a><span data-ttu-id="332fc-219">自動テスト ケースを実行</span><span class="sxs-lookup"><span data-stu-id="332fc-219">Run automated test cases</span></span>

<span data-ttu-id="332fc-220">Finance and Operations のプラットフォームは、タスク記録に基づいてテスト ケースを作成し、Azure DevOps を使用してそれらのテスト ケースの自動実行を管理するためのツールを開発者を提供します。</span><span class="sxs-lookup"><span data-stu-id="332fc-220">The platform for Finance and Operations provides developers with tools to author test cases based on task recordings and use Azure DevOps to manage the automated execution of these test cases.</span></span> 

<span data-ttu-id="332fc-221">開発者は、**ビルドおよびテスト**環境のビルドおよびテスト自動化機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="332fc-221">Developers can use the build and test automation capabilities of **build and test** environments.</span></span> <span data-ttu-id="332fc-222">詳細については、[継続的な配信ホーム ページ](../dev-tools/continuous-delivery-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332fc-222">For details, see the [Continuous delivery home page](../dev-tools/continuous-delivery-home-page.md).</span></span>

<span data-ttu-id="332fc-223">機能パワー ユーザーは、**Regression Suite Automation Tool** を使ってテスト ケースの実行を自動化できます。</span><span class="sxs-lookup"><span data-stu-id="332fc-223">Functional power users can automate the execution of their test cases using the **Regression suite automation tool**.</span></span> <span data-ttu-id="332fc-224">詳細について[ツールのダウンロード](https://www.microsoft.com/download/details.aspx?id=57357)と[Regression Suite Automation Tool](../perf-test/rsat/rsat-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332fc-224">For more information, [download the tool](https://www.microsoft.com/download/details.aspx?id=57357) and read the [Regression suite automation tool](../perf-test/rsat/rsat-overview.md).</span></span>

<span data-ttu-id="332fc-225">Regression Suite Automation Tool の詳細については、次の情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332fc-225">To learn more about using the Regression suite automation tool, see the following:</span></span>

- [<span data-ttu-id="332fc-226">第 1 部: Regression Suite Automation Tool -- バックグラウンド & セットアップ</span><span class="sxs-lookup"><span data-stu-id="332fc-226">PART 1: Regression Suite Automation Tool -- Background & Setup</span></span>](https://infopedia.eventbuilder.com/event?eventid=j5m3w4&source=Dynamics_365_for_Operations_-_FastTrack_Tech_Talks)
- [<span data-ttu-id="332fc-227">- 第 2 部: Regression Suite Automation Tool -- ライフサイクル デモのテスト</span><span class="sxs-lookup"><span data-stu-id="332fc-227">PART 2: Regression Suite Automation Tool -- Testing Lifecycle Demo</span></span>](https://infopedia.eventbuilder.com/event?eventid=r5j6c1&source=Dynamics_365_for_Operations_-_FastTrack_Tech_Talks)
- [<span data-ttu-id="332fc-228">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="332fc-228">Regression suite automation tool</span></span>](../perf-test/rsat/rsat-overview.md)
 
<span data-ttu-id="332fc-229">ハンズ オン ラボについては、[Regression Suite Automation Tool のチュートリアルを使用する](../../fin-ops/get-started/hol-use-regression-suite-automation-tool.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332fc-229">For a hands-on lab experience, see [Use the Regression suite automation tool tutorial](../../fin-ops/get-started/hol-use-regression-suite-automation-tool.md).</span></span>

#### <a name="investigate-test-runs"></a><span data-ttu-id="332fc-230">テストの実行を調査します</span><span class="sxs-lookup"><span data-stu-id="332fc-230">Investigate test runs</span></span>
<span data-ttu-id="332fc-231">自動実行が完了したら、Azure DevOps ツール バーで**テスト > 実行** (または **テスト計画 > 実行**) を選択し、テストの実行を調査すします。</span><span class="sxs-lookup"><span data-stu-id="332fc-231">Once an automated run is complete, on the Azure DevOps toolbar, select **Test > Runs** (or **Test Plans > Runs**) to investigate your test run.</span></span> <span data-ttu-id="332fc-232">テスト ケース失敗およびエラーを調査するために必要なテスト実行を選択します。</span><span class="sxs-lookup"><span data-stu-id="332fc-232">Select the desired test run to investigate test case failures and errors.</span></span> <span data-ttu-id="332fc-233">Azure DevOps のテスト スイートにアクセスして、テスト ケースに関連する最新の結果を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="332fc-233">You can also go to your test suite in Azure DevOps to see the latest results associated with your test cases.</span></span>
<span data-ttu-id="332fc-234">Azure DevOps のテストおよびテスト管理の詳細については、[Azure DevOps ドキュメント](https://docs.microsoft.com/azure/devops)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="332fc-234">For more information on testing and test management in Azure DevOps, see the [Azure DevOps documentation](https://docs.microsoft.com/azure/devops).</span></span>

