---
title: Regression Suite Automation Tool (RSAT) を使用したテスト ケースの実行
description: このトピックでは、Azure DevOps からのテスト ケースの読み込み、自動化ファイルの生成、テストパラメータの変更、テストの実行、結果の調査、および Azure DevOps への作業内容の保存方法について説明します。
author: robadawy
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 605b257caa7332f3ec5e725e8a7b4978e7808bcd
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680444"
---
# <a name="use-the-regression-suite-automation-tool-rsat"></a><span data-ttu-id="6321d-103">Regression Suite Automation Tool (RSAT) の使用</span><span class="sxs-lookup"><span data-stu-id="6321d-103">Use the Regression suite automation tool (RSAT)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6321d-104">このトピックでは、Azure DevOps からのテスト ケースの読み込み、自動化ファイルの生成、テストパラメータの変更、結果の実行と調査、および Azure DevOps への作業内容の保存方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6321d-104">This topic explains how to load test cases from Azure DevOps, generate automation files, modify test parameters, run and investigate results, and save your work back to Azure DevOps.</span></span>

## <a name="load-test-cases-and-create-automation-files"></a><span data-ttu-id="6321d-105">テスト ケースの読み込みと自動化ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="6321d-105">Load test cases and create automation files</span></span>
<span data-ttu-id="6321d-106">Azure DevOpsで、**ロード** を選択して、テスト ケースおよびテスト ケースの自動化ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6321d-106">In Azure DevOps, select **Load** to download test cases and test case automation files.</span></span> <span data-ttu-id="6321d-107">**設定** ダイアログ ボックスで指定されたテスト計画に属するすべてのテスト ケースがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="6321d-107">All test cases belonging to the test plan specified in the **Settings** dialog box are downloaded.</span></span>
 
![テスト ケースの読み込み](media/load-test-cases.png)

<span data-ttu-id="6321d-109">テスト ケースは、共通のテスト計画に基づいてテスト スイートごとに編成されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-109">Test cases are organized by test suites under a common test plan.</span></span> <span data-ttu-id="6321d-110">これらは、Azure DevOpsプロジェクトで作成したテスト スイートです。</span><span class="sxs-lookup"><span data-stu-id="6321d-110">These are test suites you created in your Azure DevOps project.</span></span> <span data-ttu-id="6321d-111">このツールを使用すると、一度に1つのテスト スイートを操作できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-111">Using this tool, you can work with one test suite at a time.</span></span>

<span data-ttu-id="6321d-112">ツールでテスト ケースの読み込みに失敗したときは、Azure DevOpsのテスト計画が適切に作成されていること、また、目的のテスト スイートおよびテスト ケースが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6321d-112">If the tool fails to load any test case, verify that your test plan in Azure DevOps is properly created and contains the desired test suites and test cases.</span></span>

<span data-ttu-id="6321d-113">このテスト計画を初めて読み込むとき、**パラメーター ファイル** の列が空白になります。</span><span class="sxs-lookup"><span data-stu-id="6321d-113">If this is the first time you load this test plan, the **Parameters File** column will be blank.</span></span> <span data-ttu-id="6321d-114">テスト ケースのテスト自動化ファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6321d-114">You will need to create test automation files for your test cases.</span></span> <span data-ttu-id="6321d-115">テスト自動化ファイルの構成要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6321d-115">Test automation files consist of:</span></span>

+ <span data-ttu-id="6321d-116">テスト パラメーター ファイル (Microsoft Excel ファイルにテスト ケース パラメーターが含まれています)</span><span class="sxs-lookup"><span data-stu-id="6321d-116">Test parameter files (Microsoft Excel files contain test case parameters)</span></span>
+ <span data-ttu-id="6321d-117">テストを実行するために必要なその他のバイナリ ファイルおよび XML ファイル。</span><span class="sxs-lookup"><span data-stu-id="6321d-117">Other binary and XML files needed to execute the tests.</span></span>

<span data-ttu-id="6321d-118">**新規** を選択すると、テスト自動化ファイルが作業ディレクトリに生成されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-118">When you select **New**, test automation files are generated in your working directory.</span></span> <span data-ttu-id="6321d-119">Excel テスト パラメーター ファイルが **パラメーター ファイル** の下のグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-119">The Excel test parameter files will appear on the grid under **Parameters File**.</span></span>

![読み込まれたテスト ケースの一覧](media/rsat-test-cases.png)
 
<span data-ttu-id="6321d-121">また、パラメーター ファイルを上書きせずに、**テスト実行ファイル** だけを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="6321d-121">You can also generate **test execution files** only, without overwriting your parameter files.</span></span> <span data-ttu-id="6321d-122">**新規 \> 実行ファイルの生成** を選択して、実行ファイルのみを再生成し、Excel ファイルは影響を受けないままにします。</span><span class="sxs-lookup"><span data-stu-id="6321d-122">Select **New \> Generate Execution Files** to regenerate only execution files and leave Excel files unaffected.</span></span> 

<span data-ttu-id="6321d-123">ツールの新しいバージョンをインストールするとき、および記録ファイルを変更または読み込むときに、テスト実行ファイルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6321d-123">You must generate test execution files when you install a new version of the tool, and when you modify or load a recording file.</span></span> <span data-ttu-id="6321d-124">このようにして、実行ファイルを更新するだけでなく、テスト パラメーター ファイルも保持できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-124">In this way, you update your execution files but also preserve the test parameter files.</span></span>

![テスト実行ファイルのみのメニュー項目を生成する](media/generate-execution-files.png)

## <a name="modify-test-parameters"></a><span data-ttu-id="6321d-126">テスト パラメーターの変更</span><span class="sxs-lookup"><span data-stu-id="6321d-126">Modify test parameters</span></span>

<span data-ttu-id="6321d-127">ここでは、Excel ファイルを変更して、テストの実行に使用する入力および検証のパラメータを指定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6321d-127">This section describes how to modify Excel files to specify input and validation parameters for your test run.</span></span> <span data-ttu-id="6321d-128">変更する 1 つ以上のテスト ケースを選択し、ツール バーで Microsoft Excel 記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="6321d-128">Select one or more test cases to modify, and then select the Microsoft Excel symbol on the toolbar.</span></span> <span data-ttu-id="6321d-129">選択したテスト ケースごとに Excel ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="6321d-129">An Excel window is opened for each test case that you selected.</span></span> <span data-ttu-id="6321d-130">または、作業ディレクトリから直接 Excel ファイルを開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="6321d-130">Alternatively, you can open the Excel files directly from the working directory.</span></span> 

<span data-ttu-id="6321d-131">**一般** タブに加えて、Excel パラメーター ファイルには、テスト ケースがアクセスするすべてのフォームのデータ タブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6321d-131">In addition to the **General** tab, the Excel parameter file contains a data tab for every form that the test case visits.</span></span>

<span data-ttu-id="6321d-132">編集する必要のあるフォーム (Excel タブ) を選択し、変更するパラメーター値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6321d-132">Select the desired form (Excel tab) that you want to edit and identify the parameter values that you want to change.</span></span> <span data-ttu-id="6321d-133">値は、コントロール名によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-133">Values are identified by their control name.</span></span> <span data-ttu-id="6321d-134">どのコントロールが正しいかわからない場合は、アプリケーションでフォームを開き、値を変更するコントロールを右クリックして、**フォーム情報** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6321d-134">If you are not sure which control is correct, open the form in the application, right-click the control whose value you want to change, and select **form information**.</span></span>

<span data-ttu-id="6321d-135">編集が完了したら Excel ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="6321d-135">Save the Excel files when you are done making edits.</span></span>

### <a name="run-a-test-as-a-specific-user"></a><span data-ttu-id="6321d-136">特定のユーザーとしてテストを実行する</span><span class="sxs-lookup"><span data-stu-id="6321d-136">Run a test as a specific user</span></span>
<span data-ttu-id="6321d-137">既定では、テストは管理者ロールを使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-137">By default, tests are executed using the admin role.</span></span> <span data-ttu-id="6321d-138">特定のセキュリティ ロールとしてテストを実行する場合は、Excel パラメーター ファイルの **一般** タブにある **テスト ユーザー** パラメーターでユーザーの電子メール アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="6321d-138">If you want to run the test as a specific security role, specify the email address of a user under the **Test User** parameter in the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="6321d-139">**テスト ユーザー** は、接続している環境の有効なユーザーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6321d-139">The **Test User** must be a valid user of the environments you are connecting to.</span></span> <span data-ttu-id="6321d-140">テストは、特定のユーザーが属しているセキュリティ ロールの下で実行されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-140">The test will run under the security roles that the specific user belongs to.</span></span> <span data-ttu-id="6321d-141">この機能を機能させるには、バージョン 1.200 またはそれ以降のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="6321d-141">You need version 1.200 or newer for this feature to be functional.</span></span>

![Excel パラメーター ファイルの一般タブ](media/rsat-excel-general-tab.png)
 
### <a name="run-a-test-in-the-context-of-a-specific-company"></a><span data-ttu-id="6321d-143">特定の会社のコンテキストでテストを実行する</span><span class="sxs-lookup"><span data-stu-id="6321d-143">Run a test in the context of a specific company</span></span>
<span data-ttu-id="6321d-144">Excel パラメーター ファイルの **一般** タブでは、法人 (会社) の名前を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="6321d-144">The **General** tab of the Excel parameter file also allows you to specify the name of a legal entity (Company).</span></span> <span data-ttu-id="6321d-145">この会社のコンテキスト内でテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="6321d-145">The test will run in the context of this company.</span></span> <span data-ttu-id="6321d-146">既定の会社を、ツールの **設定** ダイアログ ボックスで指定できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-146">You can specify your default company in the **Settings** dialog box of the tool.</span></span>

### <a name="other-notable-test-case-execution-settings"></a><span data-ttu-id="6321d-147">その他の重要なテスト ケースの実行の設定</span><span class="sxs-lookup"><span data-stu-id="6321d-147">Other notable test case execution settings</span></span>

<span data-ttu-id="6321d-148">**情報ログの警告メッセージで失敗**</span><span class="sxs-lookup"><span data-stu-id="6321d-148">**Fail on warning message in the Infolog**</span></span>

<span data-ttu-id="6321d-149">既定では、エラーが発生した場合または検証ステップが失敗した場合に、テスト ケースが失敗します。</span><span class="sxs-lookup"><span data-stu-id="6321d-149">By default, test cases fail when an error occurs or a validation step fails.</span></span> <span data-ttu-id="6321d-150">警告メッセージへの応答でもテスト ケースが失敗するようにする場合は、Excel パラメーター ファイルの **一般** タブで、**情報ログの警告メッセージで失敗** オプションを **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6321d-150">If you want a test case to fail in response to a warning message too, set the **Fail on warning message in the Infolog** option to **True** on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="6321d-151">この設定は、たとえば、テスト ケースで重複する顧客を追加する場合などに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6321d-151">This setting is useful if, for example, a test case adds a duplicate customer.</span></span> <span data-ttu-id="6321d-152">既定の設定は **False** です。</span><span class="sxs-lookup"><span data-stu-id="6321d-152">The default setting is **False**.</span></span>

<span data-ttu-id="6321d-153">**失敗時にテスト スイートの実行を中止する**</span><span class="sxs-lookup"><span data-stu-id="6321d-153">**Abort test suite execution on failure**</span></span>

<span data-ttu-id="6321d-154">**失敗時にテスト スイートの実行を中止する** オプションを **True** に設定した場合、テスト ケースが失敗すると、テスト スイートの実行は中止されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-154">If you set the **Abort test suite execution on failure** option to **True**, execution of the test suite is aborted if the test case fails.</span></span> <span data-ttu-id="6321d-155">残りのすべてのテスト ケースのステータスは **未実行** になります。</span><span class="sxs-lookup"><span data-stu-id="6321d-155">All the remaining test cases will have a status of **Not Executed**.</span></span> <span data-ttu-id="6321d-156">既定の設定は **False** です。</span><span class="sxs-lookup"><span data-stu-id="6321d-156">The default setting is **False**.</span></span>

<span data-ttu-id="6321d-157">**ステップ間の一時停止**</span><span class="sxs-lookup"><span data-stu-id="6321d-157">**Pause between steps**</span></span>

<span data-ttu-id="6321d-158">テスト ステップ間で一時停止する秒数。</span><span class="sxs-lookup"><span data-stu-id="6321d-158">The number of seconds to pause between test steps.</span></span> <span data-ttu-id="6321d-159">既定値は **0** (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="6321d-159">The default value is **0** (zero).</span></span>

### <a name="infolog-and-message-validation"></a><span data-ttu-id="6321d-160">情報ログおよびメッセージの検証</span><span class="sxs-lookup"><span data-stu-id="6321d-160">Infolog and message validation</span></span>
<span data-ttu-id="6321d-161">バージョン1.200 またはそれ以降のバージョンを使用して生成される Excel パラメーター ファイルには、 **messagevalidation** のタブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6321d-161">Excel parameter files that are generated using version 1.200 or newer contain a **MessageValidation** tab.</span></span>

<span data-ttu-id="6321d-162">このタブには、**メッセージを検証** するためのメッセージを入力できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-162">You can enter messages in this tab under **Message Validation**.</span></span> <span data-ttu-id="6321d-163">テスト ケースが実行を完了した後、ここで指定されたメッセージが情報ログに表示されることを検証します。</span><span class="sxs-lookup"><span data-stu-id="6321d-163">After a test case completes execution, it validates that the messages specified here appear in the Infolog.</span></span> <span data-ttu-id="6321d-164">これらのメッセージが見つからない場合、テスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6321d-164">The test case will fail if these messages are not found.</span></span>

<span data-ttu-id="6321d-165">予想されるエラー メッセージを含むすべてのメッセージを特定できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-165">You can specify any expected messages including error messages that are expected.</span></span> <span data-ttu-id="6321d-166">予期されたエラーが発生して、このセクション内に存在している場合、このテストは失敗しません。</span><span class="sxs-lookup"><span data-stu-id="6321d-166">If an expected error occurred, but exists in this section, the test will not fail.</span></span>
 
![メッセージ検証の例](media/message-validation.png)


## <a name="run"></a><span data-ttu-id="6321d-168">実行</span><span class="sxs-lookup"><span data-stu-id="6321d-168">Run</span></span>
<span data-ttu-id="6321d-169">**実行** を選択して、選択済みのテストケースを実行します。</span><span class="sxs-lookup"><span data-stu-id="6321d-169">Select **Run** to execute the selected test cases.</span></span> <span data-ttu-id="6321d-170">既存の自動化ファイルを用いるテスト ケースのみを実行できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-170">Only test cases with existing automation files can be run.</span></span> <span data-ttu-id="6321d-171">ツールでは、Excel に入力されたデータを使用して、これらのテストが開かれ実行されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-171">The tool will open and execute these tests with the data you entered in Excel.</span></span>

<span data-ttu-id="6321d-172">上下矢印ボタンを使用して、テスト ケースを実行する順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-172">You can modify the order in which test cases are executed using the up and down arrow buttons.</span></span>

### <a name="pause-prior-to-a-test-case-run"></a><span data-ttu-id="6321d-173">テスト ケース実行前の一時停止</span><span class="sxs-lookup"><span data-stu-id="6321d-173">Pause prior to a test case run</span></span> 
<span data-ttu-id="6321d-174">テスト ケース実行開始前に、一時停止を追加できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-174">You can add a pause before a test case starts execution.</span></span> <span data-ttu-id="6321d-175">一時停止する場合は、目的のテスト ケースの Excel パラメーター ファイルの **一般** タブで、セル **一時停止 (秒)** を更新します。</span><span class="sxs-lookup"><span data-stu-id="6321d-175">If you want to pause, update the cell **Pause (seconds)** on the **General** tab of the Excel parameters file of the desired test case.</span></span>

### <a name="stop-a-run"></a><span data-ttu-id="6321d-176">実行の停止</span><span class="sxs-lookup"><span data-stu-id="6321d-176">Stop a run</span></span>
<span data-ttu-id="6321d-177">テストの実行が進行中の場合は、**停止** ボタンをクリックして実行をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="6321d-177">When a test run is in progress, you can click the **Stop** button to cancel the run.</span></span> <span data-ttu-id="6321d-178">現在実行中のテスト ケースが完了した後で実行が停止します。</span><span class="sxs-lookup"><span data-stu-id="6321d-178">Execution stops after the currently running test case completes.</span></span> <span data-ttu-id="6321d-179">残りのテスト ケースは、Azure DevOps で **未実行** とマークされます。</span><span class="sxs-lookup"><span data-stu-id="6321d-179">The remaining test cases will be marked as **Not Executed** in Azure DevOps.</span></span>

### <a name="validate-readiness-of-test-automation-files"></a><span data-ttu-id="6321d-180">テスト自動化ファイルの準備状況の検証</span><span class="sxs-lookup"><span data-stu-id="6321d-180">Validate readiness of test automation files</span></span>
<span data-ttu-id="6321d-181">必要に応じて、テスト ケースの実行準備が整っているかどうかを検証する設定を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6321d-181">Optionally, you can turn on a setting that validates whether your test cases are ready for execution.</span></span> <span data-ttu-id="6321d-182">この設定により、レコーディングおよびテスト自動化ファイルの有効性に関連する不明なエラーが防止されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-182">This setting prevents unknown errors related to the validity of recordings and test automation files.</span></span> <span data-ttu-id="6321d-183">このオプションは、RSAT バージョン 1.210 で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-183">This option is available as of RSAT version 1.210.</span></span> <span data-ttu-id="6321d-184">この機能は、**設定** ダイアログの **オプション** タブで有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6321d-184">You can enable this feature in the **Optional** tab of the **Settings** dialog.</span></span>

![enable-local-file-validation-rules](media/enable-local-file-validation-rules.png)

<span data-ttu-id="6321d-186">有効にすると、バックグラウンド プロセスによって、各テスト ケースの次の項目が継続的に検証されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-186">When enabled, a background process continuously validates the following for each test case.</span></span>

+ <span data-ttu-id="6321d-187">ローカルの作業ディレクトリが存在します。</span><span class="sxs-lookup"><span data-stu-id="6321d-187">The local working directory exists.</span></span>
+ <span data-ttu-id="6321d-188">Excel パラメーター ファイルが存在します。</span><span class="sxs-lookup"><span data-stu-id="6321d-188">The Excel parameter file exists.</span></span>
+ <span data-ttu-id="6321d-189">実行に必要なテスト自動化ファイル (バイナリ ファイルまたは Xml ファイル) が存在します。</span><span class="sxs-lookup"><span data-stu-id="6321d-189">Test automation files (binary and Xml files) needed for execution exist.</span></span>
+ <span data-ttu-id="6321d-190">テスト自動化ファイルは、RSAT の現在のバージョンと互換性があります。</span><span class="sxs-lookup"><span data-stu-id="6321d-190">Test automation files are compatible with current version of RSAT.</span></span> <span data-ttu-id="6321d-191">新しいバージョンの RSAT をインストールするときに、テスト自動化ファイルを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6321d-191">You must regenerate test automation files when you install a new version of RSAT.</span></span>
+ <span data-ttu-id="6321d-192">Excel パラメーター ファイルに指定されたテスト ケース ID は、Azure DevOps のテスト ケース ID と一致します。</span><span class="sxs-lookup"><span data-stu-id="6321d-192">Test case ID specified in the Excel parameter file matches the test cases ID in Azure DevOps.</span></span>

<span data-ttu-id="6321d-193">グリッドの有効な列は、検証プロセスの結果を示します。</span><span class="sxs-lookup"><span data-stu-id="6321d-193">The Valid column in the grid indicates the result of the validation process.</span></span> <span data-ttu-id="6321d-194">検証が失敗した場合は、**有効** 列の **X** をクリックすると、エラーと推奨されるアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-194">If validation fails, click on the **X** in the **Valid** column to view the error and recommended action.</span></span>

![enable-local-file-validation-rules-2](media/enable-local-file-validation-rules-2.png)

## <a name="investigate-results"></a><span data-ttu-id="6321d-196">結果の調査</span><span class="sxs-lookup"><span data-stu-id="6321d-196">Investigate results</span></span>
<span data-ttu-id="6321d-197">すべてのテスト ケースの実行が完了すると、**合格** または **不合格** が **結果** 列に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-197">When all test cases complete execution, **Pass** or **Fail** will be populated in the **Result** column.</span></span> <span data-ttu-id="6321d-198">結果をクリックすると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-198">You can click on the result to see error messages.</span></span>

<span data-ttu-id="6321d-199">Azure DevOps で入手できる追加の調査詳細。</span><span class="sxs-lookup"><span data-stu-id="6321d-199">Additional investigation details are available in Azure DevOps.</span></span> <span data-ttu-id="6321d-200">この情報を表示するには Azure DevOps プロジェクトページから、**テスト > 実行** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6321d-200">To view this information, from your Azure DevOps project page, go to **Test > Runs**.</span></span>

![テスト結果](media/test-results.png)

<span data-ttu-id="6321d-202">目的のテストの実行を選択します。</span><span class="sxs-lookup"><span data-stu-id="6321d-202">Select the desired test run.</span></span> <span data-ttu-id="6321d-203">その実行中に実行されたすべてのテストの結果が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6321d-203">It will include the results of all tests that were executed during that run.</span></span>
 
![結果の円グラフ](media/outcome-pie-chart.png)

![各テストの結果](media/pass-fail.png)

<span data-ttu-id="6321d-206">失敗したテスト結果を開いて、**ErrorMessage** セクションでエラーに関する情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-206">You can open a failed test result and review the **ErrorMessage** section for information about the failure.</span></span>
 
![エラー メッセージの情報](media/error-message.png)

<span data-ttu-id="6321d-208">すべてのエラー メッセージは、**C:\Users\$YourUserName\AppData\Roaming\regressionTool\errormsg-<TestCaseId>.txt** でローカルでも利用可能です。</span><span class="sxs-lookup"><span data-stu-id="6321d-208">All error messages are also available locally under **C:\Users\$YourUserName\AppData\Roaming\regressionTool\errormsg-<TestCaseId>.txt**.</span></span>

### <a name="test-response-times"></a><span data-ttu-id="6321d-209">応答時間のテスト</span><span class="sxs-lookup"><span data-stu-id="6321d-209">Test response times</span></span>
<span data-ttu-id="6321d-210">実行ログに加えて、テスト ケースの期間もテスト結果で確認できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-210">In addition to execution logs, the duration of a test case is also available in the test result.</span></span>
 
![テスト ケースの期間](media/test-duration.png)

<span data-ttu-id="6321d-212">テスト結果に添付されている **BaseTime.xml** ファイルを開くことにより、テスト ケースの各ステップの応答時間を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="6321d-212">You can also review the response time of each step of the test case by opening the **BaseTime.xml** file attached to the test result.</span></span>
 
![応答時間ファイル](media/response-time.png)

<span data-ttu-id="6321d-214">応答時間を機能させるには、バージョン 1.200 またはそれ以降のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="6321d-214">You need version 1.200 or newer for response times to be available.</span></span>

## <a name="upload-to-azure-devops-to-commit-your-work"></a><span data-ttu-id="6321d-215">Azure DevOps にアップロードして作業をコミットします。</span><span class="sxs-lookup"><span data-stu-id="6321d-215">Upload to Azure DevOps to commit your work</span></span>
<span data-ttu-id="6321d-216">Azure DevOps に作業をコミットするには、**アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6321d-216">To commit your work to Azure DevOps, select **Upload**.</span></span> <span data-ttu-id="6321d-217">これにより、選択したテスト ケースに関するテストの自動化ファイル (Excel テストパラメータ ファイルを含む) を、 Azure DevOps にアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="6321d-217">This will upload test automation files, including Excel test parameter files, of all selected test cases to Azure DevOps for future use.</span></span> <span data-ttu-id="6321d-218">テスト自動化ファイルを Azure DevOps にアップロードした後は、次に Regression Suite Automation Tool を使用するときに、テストの実行ファイルを生成したり Excel パラメーター ファイルを編集したりすることなく、別のコンピューターからでも簡単に **読み込み**、**実行** できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-218">After test automation files are uploaded to Azure DevOps, the next time you use the Regression suite automation tool, even from a different computer, you can simply use **Load** and then **Run**, without generating test execution files or editing Excel parameter files.</span></span>

<span data-ttu-id="6321d-219">アップロード メニューには、レコーディング ファイル (タスクの記録) のみをアップロードするためのオプションも用意されています。</span><span class="sxs-lookup"><span data-stu-id="6321d-219">In the upload menu, you also have the option to upload recording files (Task recordings) only.</span></span> 

<span data-ttu-id="6321d-220">選択するテスト ケースがわからない場合に、(前回の読み込み以降の) すべての変更を Azure DevOps にコミットするには、アップロード メニューで **すべての変更されたオートメーション ファイルをアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6321d-220">If you are unsure what test cases to select, and you want to commit all changes (since last load) to Azure DevOps, select **Upload all modified automation files** in the upload menu.</span></span>

## <a name="process-compliance"></a><span data-ttu-id="6321d-221">コンプライアンスのプロセス</span><span class="sxs-lookup"><span data-stu-id="6321d-221">Process compliance</span></span>
<span data-ttu-id="6321d-222">RSAT には、テスト ケースの準備状況を管理する機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="6321d-222">RSAT provides capabilities for managing the readiness of test cases.</span></span> <span data-ttu-id="6321d-223">また、テストの実行のためのサインオフ プロセスも用意されています。</span><span class="sxs-lookup"><span data-stu-id="6321d-223">It also provides a sign-off process for test runs.</span></span>

![コンプライアンス ファイルのプロセス](media/rsat-process-compliance-settings.png)

### <a name="enforce-test-case-readiness"></a><span data-ttu-id="6321d-225">テスト ケースの準備完了を適用する</span><span class="sxs-lookup"><span data-stu-id="6321d-225">Enforce test case readiness</span></span>

<span data-ttu-id="6321d-226">Azure DevOps で **準備完了** のステータスがない限り、テスト ケースが実行されないように設定できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-226">You can set up the test case so that it isn't run unless it has a status of **Ready** in Azure DevOps.</span></span> <span data-ttu-id="6321d-227">**設定** ダイアログ ボックスの **プロセス** タブで、**テスト ケースの準備完了を適用** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="6321d-227">In the **Settings** dialog box, on the **Process** tab, select the **Enforce test case readiness** check box.</span></span> <span data-ttu-id="6321d-228">既定では、このチェック ボックスはオフになっています。</span><span class="sxs-lookup"><span data-stu-id="6321d-228">By default, the check box is cleared.</span></span>

### <a name="signoffs"></a><span data-ttu-id="6321d-229">サインオフ</span><span class="sxs-lookup"><span data-stu-id="6321d-229">Signoffs</span></span>

<span data-ttu-id="6321d-230">テストの実行が完了すると、RSAT によって Azure DevOps にサインオフ作業項目が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6321d-230">When your test run is completed, RSAT can create sign-off work items in Azure DevOps.</span></span> <span data-ttu-id="6321d-231">**設定** ダイアログ ボックスの **プロセス** タブで、**サインオフ タスク** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="6321d-231">In the **Settings** dialog box, on the **Process** tab, select the **Sign-off tasks** check box.</span></span> <span data-ttu-id="6321d-232">次に、サインオフする各ユーザーに対して作成する作業項目のタイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="6321d-232">Then set the type of work item that should be created for each person who signs off.</span></span> <span data-ttu-id="6321d-233">サインオフに **機能**、**IT マネージャー** および **チーム マネージャー** ロールを選択し、適切な電子メールアドレスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="6321d-233">You can select **Functional**, **IT Manager** and **Team Manager** roles for sign-offs, and then specify appropriate email addresses.</span></span> <span data-ttu-id="6321d-234">その後、作業項目は Azure DevOps で作成され、承認のために所有者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6321d-234">Work items will then be created in Azure DevOps and assigned to owners for approval.</span></span>

