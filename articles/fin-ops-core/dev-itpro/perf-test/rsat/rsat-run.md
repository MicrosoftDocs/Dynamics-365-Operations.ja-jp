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
ms.search.scope: Operations
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 441fc125b602fb023f8b167ef0ce5566803345de
ms.sourcegitcommit: 5d31d3e5f8549b761360c338bc2a1d9506c15999
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030039"
---
# <a name="run-test-cases-by-using-the-regression-suite-automation-tool-rsat"></a><span data-ttu-id="477ba-103">Regression Suite Automation Tool (RSAT) を使用したテスト ケースの実行</span><span class="sxs-lookup"><span data-stu-id="477ba-103">Run test cases by using the Regression suite automation tool (RSAT)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="477ba-104">このトピックでは、Azure DevOps からのテスト ケースの読み込み、自動化ファイルの生成、テストパラメータの変更、テストの実行、結果の調査、および Azure DevOps への作業内容の保存方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="477ba-104">This topic explains how to load test cases from Azure DevOps, generate automation files, modify test parameters, run tests, investigate results, and save your work back to Azure DevOps.</span></span>

## <a name="load-test-cases-and-create-automation-files"></a><span data-ttu-id="477ba-105">テスト ケースの読み込みと自動化ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="477ba-105">Load test cases and create automation files</span></span>
<span data-ttu-id="477ba-106">Azure DevOpsで、**ロード** を選択して、テスト ケースおよびテスト ケースの自動化ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="477ba-106">In Azure DevOps, select **Load** to download test cases and test case automation files.</span></span> <span data-ttu-id="477ba-107">**設定**ダイアログ ボックスで指定されたテスト計画に属するすべてのテスト ケースがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="477ba-107">All test cases belonging to the test plan specified in the **Settings** dialog box are downloaded.</span></span>
 
![テスト ケースの読み込み](media/load-test-cases.png)

<span data-ttu-id="477ba-109">テスト ケースは、共通のテスト計画に基づいてテスト スイートごとに編成されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-109">Test cases are organized by test suites under a common test plan.</span></span> <span data-ttu-id="477ba-110">これらは、Azure DevOpsプロジェクトで作成したテスト スイートです。</span><span class="sxs-lookup"><span data-stu-id="477ba-110">These are test suites you created in your Azure DevOps project.</span></span> <span data-ttu-id="477ba-111">このツールを使用すると、一度に1つのテスト スイートを操作できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-111">Using this tool, you can work with one test suite at a time.</span></span>

<span data-ttu-id="477ba-112">ツールでテスト ケースの読み込みに失敗したときは、Azure DevOpsのテスト計画が適切に作成されていること、また、目的のテスト スイートおよびテスト ケースが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="477ba-112">If the tool fails to load any test case, verify that your test plan in Azure DevOps is properly created and contains the desired test suites and test cases.</span></span>

<span data-ttu-id="477ba-113">このテスト計画を初めて読み込むとき、**パラメーター ファイル**の列が空白になります。</span><span class="sxs-lookup"><span data-stu-id="477ba-113">If this is the first time you load this test plan, the **Parameters File** column will be blank.</span></span> <span data-ttu-id="477ba-114">テスト ケースのテスト自動化ファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-114">You will need to create test automation files for your test cases.</span></span> <span data-ttu-id="477ba-115">テスト自動化ファイルの構成要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="477ba-115">Test automation files consist of:</span></span>

+ <span data-ttu-id="477ba-116">テスト パラメーター ファイル (Microsoft Excel ファイルにテスト ケース パラメーターが含まれています)</span><span class="sxs-lookup"><span data-stu-id="477ba-116">Test parameter files (Microsoft Excel files contain test case parameters)</span></span>
+ <span data-ttu-id="477ba-117">テストを実行するために必要なその他のバイナリ ファイルおよび XML ファイル。</span><span class="sxs-lookup"><span data-stu-id="477ba-117">Other binary and XML files needed to execute the tests.</span></span>

<span data-ttu-id="477ba-118">**新規**を選択すると、テスト自動化ファイルが作業ディレクトリに生成されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-118">When you select **New**, test automation files are generated in your working directory.</span></span> <span data-ttu-id="477ba-119">Excel テスト パラメーター ファイルが**パラメーター ファイル**の下のグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-119">The Excel test parameter files will appear on the grid under **Parameters File**.</span></span>

![読み込まれたテスト ケースの一覧](media/rsat-test-cases.png)
 
<span data-ttu-id="477ba-121">また、パラメーター ファイルを上書きせずに、**テスト実行ファイル**だけを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="477ba-121">You can also generate **test execution files** only, without overwriting your parameter files.</span></span> <span data-ttu-id="477ba-122">**新規 \> 実行ファイルの生成**を選択して、実行ファイルのみを再生成し、Excel ファイルは影響を受けないままにします。</span><span class="sxs-lookup"><span data-stu-id="477ba-122">Select **New \> Generate Execution Files** to regenerate only execution files and leave Excel files unaffected.</span></span> 

<span data-ttu-id="477ba-123">ツールの新しいバージョンをインストールするとき、および記録ファイルを変更または読み込むときに、テスト実行ファイルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-123">You must generate test execution files when you install a new version of the tool, and when you modify or load a recording file.</span></span> <span data-ttu-id="477ba-124">このようにして、実行ファイルを更新するだけでなく、テスト パラメーター ファイルも保持できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-124">In this way, you update your execution files but also preserve the test parameter files.</span></span>

![テスト実行ファイルのみのメニュー項目を生成する](media/generate-execution-files.png)

## <a name="modify-test-parameters"></a><span data-ttu-id="477ba-126">テスト パラメーターの変更</span><span class="sxs-lookup"><span data-stu-id="477ba-126">Modify test parameters</span></span>

<span data-ttu-id="477ba-127">ここでは、Excel ファイルを変更して、テストの実行に使用する入力および検証のパラメータを指定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="477ba-127">This section describes how to modify Excel files to specify input and validation parameters for your test run.</span></span> <span data-ttu-id="477ba-128">変更する 1 つ以上のテスト ケースを選択し、ツール バーで Microsoft Excel 記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="477ba-128">Select one or more test cases to modify, and then select the Microsoft Excel symbol on the toolbar.</span></span> <span data-ttu-id="477ba-129">選択したテスト ケースごとに Excel ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="477ba-129">An Excel window is opened for each test case that you selected.</span></span> <span data-ttu-id="477ba-130">または、作業ディレクトリから直接 Excel ファイルを開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="477ba-130">Alternatively, you can open the Excel files directly from the working directory.</span></span> 

<span data-ttu-id="477ba-131">**一般**タブに加えて、Excel パラメーター ファイルには、テスト ケースがアクセスするすべてのフォームのデータ タブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="477ba-131">In addition to the **General** tab, the Excel parameter file contains a data tab for every form that the test case visits.</span></span>

<span data-ttu-id="477ba-132">編集する必要のあるフォーム (Excel タブ) を選択し、変更するパラメーター値を指定します。</span><span class="sxs-lookup"><span data-stu-id="477ba-132">Select the desired form (Excel tab) that you want to edit and identify the parameter values that you want to change.</span></span> <span data-ttu-id="477ba-133">値は、コントロール名によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-133">Values are identified by their control name.</span></span> <span data-ttu-id="477ba-134">どのコントロールが正しいかわからない場合は、アプリケーションでフォームを開き、値を変更するコントロールを右クリックして、**フォーム情報**を選択します。</span><span class="sxs-lookup"><span data-stu-id="477ba-134">If you are not sure which control is correct, open the form in the application, right-click the control whose value you want to change, and select **form information**.</span></span>

<span data-ttu-id="477ba-135">編集が完了したら Excel ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="477ba-135">Save the Excel files when you are done making edits.</span></span>

### <a name="run-a-test-as-a-specific-user"></a><span data-ttu-id="477ba-136">特定のユーザーとしてテストを実行する</span><span class="sxs-lookup"><span data-stu-id="477ba-136">Run a test as a specific user</span></span>
<span data-ttu-id="477ba-137">既定では、テストは管理者ロールを使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-137">By default, tests are executed using the admin role.</span></span> <span data-ttu-id="477ba-138">特定のセキュリティ ロールとしてテストを実行する場合は、Excel パラメーター ファイルの**一般**タブにある**テスト ユーザー** パラメーターでユーザーの電子メール アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="477ba-138">If you want to run the test as a specific security role, specify the email address of a user under the **Test User** parameter in the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="477ba-139">**テスト ユーザー**は、接続している環境の有効なユーザーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="477ba-139">The **Test User** must be a valid user of the environments you are connecting to.</span></span> <span data-ttu-id="477ba-140">テストは、特定のユーザーが属しているセキュリティ ロールの下で実行されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-140">The test will run under the security roles that the specific user belongs to.</span></span> <span data-ttu-id="477ba-141">この機能を機能させるには、バージョン 1.200 またはそれ以降のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="477ba-141">You need version 1.200 or newer for this feature to be functional.</span></span>

![Excel パラメーター ファイルの一般タブ](media/rsat-excel-general-tab.png)
 
### <a name="run-a-test-in-the-context-of-a-specific-company"></a><span data-ttu-id="477ba-143">特定の会社のコンテキストでテストを実行する</span><span class="sxs-lookup"><span data-stu-id="477ba-143">Run a test in the context of a specific company</span></span>
<span data-ttu-id="477ba-144">Excel パラメーター ファイルの**一般**タブでは、法人 (会社) の名前を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="477ba-144">The **General** tab of the Excel parameter file also allows you to specify the name of a legal entity (Company).</span></span> <span data-ttu-id="477ba-145">この会社のコンテキスト内でテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="477ba-145">The test will run in the context of this company.</span></span> <span data-ttu-id="477ba-146">既定の会社を、ツールの **設定** ダイアログ ボックスで指定できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-146">You can specify your default company in the **Settings** dialog box of the tool.</span></span>

### <a name="other-notable-test-case-execution-settings"></a><span data-ttu-id="477ba-147">その他の重要なテスト ケースの実行の設定</span><span class="sxs-lookup"><span data-stu-id="477ba-147">Other notable test case execution settings</span></span>

<span data-ttu-id="477ba-148">**情報ログの警告メッセージで失敗**</span><span class="sxs-lookup"><span data-stu-id="477ba-148">**Fail on warning message in the Infolog**</span></span>

<span data-ttu-id="477ba-149">既定では、エラーが発生した場合または検証ステップが失敗した場合に、テスト ケースが失敗します。</span><span class="sxs-lookup"><span data-stu-id="477ba-149">By default, test cases fail when an error occurs or a validation step fails.</span></span> <span data-ttu-id="477ba-150">警告メッセージへの応答でもテスト ケースが失敗するようにする場合は、Excel パラメーター ファイルの**一般**タブで、**情報ログの警告メッセージで失敗**オプションを **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="477ba-150">If you want a test case to fail in response to a warning message too, set the **Fail on warning message in the Infolog** option to **True** on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="477ba-151">この設定は、たとえば、テスト ケースで重複する顧客を追加する場合などに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="477ba-151">This setting is useful if, for example, a test case adds a duplicate customer.</span></span> <span data-ttu-id="477ba-152">既定の設定は **False** です。</span><span class="sxs-lookup"><span data-stu-id="477ba-152">The default setting is **False**.</span></span>

<span data-ttu-id="477ba-153">**失敗時にテスト スイートの実行を中止する**</span><span class="sxs-lookup"><span data-stu-id="477ba-153">**Abort test suite execution on failure**</span></span>

<span data-ttu-id="477ba-154">**失敗時にテスト スイートの実行を中止する**オプションを **True** に設定した場合、テスト ケースが失敗すると、テスト スイートの実行は中止されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-154">If you set the **Abort test suite execution on failure** option to **True**, execution of the test suite is aborted if the test case fails.</span></span> <span data-ttu-id="477ba-155">残りのすべてのテスト ケースのステータスは**未実行**になります。</span><span class="sxs-lookup"><span data-stu-id="477ba-155">All the remaining test cases will have a status of **Not Executed**.</span></span> <span data-ttu-id="477ba-156">既定の設定は **False** です。</span><span class="sxs-lookup"><span data-stu-id="477ba-156">The default setting is **False**.</span></span>

<span data-ttu-id="477ba-157">**ステップ間の一時停止**</span><span class="sxs-lookup"><span data-stu-id="477ba-157">**Pause between steps**</span></span>

<span data-ttu-id="477ba-158">テスト ステップ間で一時停止する秒数。</span><span class="sxs-lookup"><span data-stu-id="477ba-158">The number of seconds to pause between test steps.</span></span> <span data-ttu-id="477ba-159">既定値は **0** (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="477ba-159">The default value is **0** (zero).</span></span>

### <a name="infolog-and-message-validation"></a><span data-ttu-id="477ba-160">情報ログおよびメッセージの検証</span><span class="sxs-lookup"><span data-stu-id="477ba-160">Infolog and message validation</span></span>
<span data-ttu-id="477ba-161">バージョン1.200 またはそれ以降のバージョンを使用して生成される Excel パラメーター ファイルには、 **messagevalidation** のタブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="477ba-161">Excel parameter files that are generated using version 1.200 or newer contain a **MessageValidation** tab.</span></span>

<span data-ttu-id="477ba-162">このタブには、**メッセージを検証**するためのメッセージを入力できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-162">You can enter messages in this tab under **Message Validation**.</span></span> <span data-ttu-id="477ba-163">テスト ケースが実行を完了した後、ここで指定されたメッセージが情報ログに表示されることを検証します。</span><span class="sxs-lookup"><span data-stu-id="477ba-163">After a test case completes execution, it validates that the messages specified here appear in the Infolog.</span></span> <span data-ttu-id="477ba-164">これらのメッセージが見つからない場合、テスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="477ba-164">The test case will fail if these messages are not found.</span></span>

<span data-ttu-id="477ba-165">予想されるエラー メッセージを含むすべてのメッセージを特定できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-165">You can specify any expected messages including error messages that are expected.</span></span> <span data-ttu-id="477ba-166">予期されたエラーが発生して、このセクション内に存在している場合、このテストは失敗しません。</span><span class="sxs-lookup"><span data-stu-id="477ba-166">If an expected error occurred, but exists in this section, the test will not fail.</span></span>
 
![メッセージ検証の例](media/message-validation.png)


## <a name="run"></a><span data-ttu-id="477ba-168">実行</span><span class="sxs-lookup"><span data-stu-id="477ba-168">Run</span></span>
<span data-ttu-id="477ba-169">**実行**を選択して、選択済みのテストケースを実行します。</span><span class="sxs-lookup"><span data-stu-id="477ba-169">Select **Run** to execute the selected test cases.</span></span> <span data-ttu-id="477ba-170">既存の自動化ファイルを用いるテスト ケースのみを実行できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-170">Only test cases with existing automation files can be run.</span></span> <span data-ttu-id="477ba-171">ツールでは、Excel に入力されたデータを使用して、これらのテストが開かれ実行されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-171">The tool will open and execute these tests with the data you entered in Excel.</span></span>

<span data-ttu-id="477ba-172">上下矢印ボタンを使用して、テスト ケースを実行する順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-172">You can modify the order in which test cases are executed using the up and down arrow buttons.</span></span>

### <a name="pause-prior-to-a-test-case-run"></a><span data-ttu-id="477ba-173">テスト ケース実行前の一時停止</span><span class="sxs-lookup"><span data-stu-id="477ba-173">Pause prior to a test case run</span></span> 
<span data-ttu-id="477ba-174">テスト ケース実行開始前に、一時停止を追加できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-174">You can add a pause before a test case starts execution.</span></span> <span data-ttu-id="477ba-175">一時停止する場合は、Excel パラメーター ファイルの**一般**タブの**一時停止 (秒)** セルを更新します。</span><span class="sxs-lookup"><span data-stu-id="477ba-175">If you want to pause, update the cell **Pause (seconds)** on the **General** tab of the Excel parameters file.</span></span>

## <a name="investigate-results"></a><span data-ttu-id="477ba-176">結果の調査</span><span class="sxs-lookup"><span data-stu-id="477ba-176">Investigate results</span></span>
<span data-ttu-id="477ba-177">すべてのテスト ケースの実行が完了すると、**合格** または **不合格** が **結果** 列に設定されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-177">When all test cases complete execution, **Pass** or **Fail** will be populated in the **Result** column.</span></span> <span data-ttu-id="477ba-178">結果をクリックすると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-178">You can click on the result to see error messages.</span></span>

<span data-ttu-id="477ba-179">Azure DevOps で入手できる追加の調査詳細。</span><span class="sxs-lookup"><span data-stu-id="477ba-179">Additional investigation details are available in Azure DevOps.</span></span> <span data-ttu-id="477ba-180">この情報を表示するには Azure DevOps プロジェクトページから、**テスト > 実行** に移動します。</span><span class="sxs-lookup"><span data-stu-id="477ba-180">To view this information, from your Azure DevOps project page, go to **Test > Runs**.</span></span>

![テスト結果](media/test-results.png)

<span data-ttu-id="477ba-182">目的のテストの実行を選択します。</span><span class="sxs-lookup"><span data-stu-id="477ba-182">Select the desired test run.</span></span> <span data-ttu-id="477ba-183">その実行中に実行されたすべてのテストの結果が含まれます。</span><span class="sxs-lookup"><span data-stu-id="477ba-183">It will include the results of all tests that were executed during that run.</span></span>
 
![結果の円グラフ](media/outcome-pie-chart.png)

![各テストの結果](media/pass-fail.png)

<span data-ttu-id="477ba-186">失敗したテスト結果を開いて、**ErrorMessage** セクションでエラーに関する情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-186">You can open a failed test result and review the **ErrorMessage** section for information about the failure.</span></span>
 
![エラー メッセージの情報](media/error-message.png)

<span data-ttu-id="477ba-188">すべてのエラー メッセージは、**C:\Users\$YourUserName\AppData\Roaming\regressionTool\errormsg-<TestCaseId>.txt** でローカルでも利用可能です。</span><span class="sxs-lookup"><span data-stu-id="477ba-188">All error messages are also available locally under **C:\Users\$YourUserName\AppData\Roaming\regressionTool\errormsg-<TestCaseId>.txt**.</span></span>

### <a name="test-response-times"></a><span data-ttu-id="477ba-189">応答時間のテスト</span><span class="sxs-lookup"><span data-stu-id="477ba-189">Test response times</span></span>
<span data-ttu-id="477ba-190">実行ログに加えて、テスト ケースの期間もテスト結果で確認できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-190">In addition to execution logs, the duration of a test case is also available in the test result.</span></span>
 
![テスト ケースの期間](media/test-duration.png)

<span data-ttu-id="477ba-192">テスト結果に添付されている **BaseTime.xml** ファイルを開くことにより、テスト ケースの各ステップの応答時間を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="477ba-192">You can also review the response time of each step of the test case by opening the **BaseTime.xml** file attached to the test result.</span></span>
 
![応答時間ファイル](media/response-time.png)

<span data-ttu-id="477ba-194">応答時間を機能させるには、バージョン 1.200 またはそれ以降のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="477ba-194">You need version 1.200 or newer for response times to be available.</span></span>

## <a name="save-your-work"></a><span data-ttu-id="477ba-195">作業を保存</span><span class="sxs-lookup"><span data-stu-id="477ba-195">Save your work</span></span>
<span data-ttu-id="477ba-196">作業内容を保存するには、**アップロード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="477ba-196">To preserve your work, select **Upload**.</span></span> <span data-ttu-id="477ba-197">これにより、選択したテスト ケースに関するテストの自動化ファイル (Excel テストパラメータ ファイルを含む) を、 Azure DevOps にアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="477ba-197">This will upload test automation files, including Excel test parameter files, of all selected test cases to Azure DevOps for future use.</span></span>
<span data-ttu-id="477ba-198">テスト自動化ファイルを Azure DevOps にアップロードした後は、次に Regression Suite Automation Tool を使用するときに、テストの実行ファイルを生成したり Excel パラメーター ファイルを編集したりすることなく、別のコンピューターからでも簡単に **読み込み**、**実行**できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-198">After test automation files are uploaded to Azure DevOps, the next time you use the Regression suite automation tool, even from a different computer, you can simply use **Load** and then **Run**, without generating test execution files or editing Excel parameter files.</span></span>

## <a name="process-compliance"></a><span data-ttu-id="477ba-199">コンプライアンスのプロセス</span><span class="sxs-lookup"><span data-stu-id="477ba-199">Process compliance</span></span>
<span data-ttu-id="477ba-200">RSAT には、テスト ケースの準備状況を管理する機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="477ba-200">RSAT provides capabilities for managing the readiness of test cases.</span></span> <span data-ttu-id="477ba-201">また、テストの実行のためのサインオフ プロセスも用意されています。</span><span class="sxs-lookup"><span data-stu-id="477ba-201">It also provides a sign-off process for test runs.</span></span>

![コンプライアンス ファイルのプロセス](media/rsat-process-compliance-settings.png)

### <a name="enforce-test-case-readiness"></a><span data-ttu-id="477ba-203">テスト ケースの準備完了を適用する</span><span class="sxs-lookup"><span data-stu-id="477ba-203">Enforce test case readiness</span></span>

<span data-ttu-id="477ba-204">Azure DevOps で **準備完了**のステータスがない限り、テスト ケースが実行されないように設定できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-204">You can set up the test case so that it isn't run unless it has a status of **Ready** in Azure DevOps.</span></span> <span data-ttu-id="477ba-205">**設定**ダイアログ ボックスの**プロセス** タブで、**テスト ケースの準備完了を適用**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="477ba-205">In the **Settings** dialog box, on the **Process** tab, select the **Enforce test case readiness** check box.</span></span> <span data-ttu-id="477ba-206">既定では、このチェック ボックスはオフになっています。</span><span class="sxs-lookup"><span data-stu-id="477ba-206">By default, the check box is cleared.</span></span>

### <a name="signoffs"></a><span data-ttu-id="477ba-207">サインオフ</span><span class="sxs-lookup"><span data-stu-id="477ba-207">Signoffs</span></span>

<span data-ttu-id="477ba-208">テストの実行が完了すると、RSAT によって Azure DevOps にサインオフ作業項目が作成されます。</span><span class="sxs-lookup"><span data-stu-id="477ba-208">When your test run is completed, RSAT can create sign-off work items in Azure DevOps.</span></span> <span data-ttu-id="477ba-209">**設定**ダイアログ ボックスの**プロセス** タブで、**サインオフ タスク** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="477ba-209">In the **Settings** dialog box, on the **Process** tab, select the **Sign-off tasks** check box.</span></span> <span data-ttu-id="477ba-210">次に、サインオフする各ユーザーに対して作成する作業項目のタイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="477ba-210">Then set the type of work item that should be created for each person who signs off.</span></span> <span data-ttu-id="477ba-211">サインオフに **機能**、**IT マネージャー**および**チーム マネージャー** ロールを選択し、適切な電子メールアドレスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="477ba-211">You can select **Functional**, **IT Manager** and **Team Manager** roles for sign-offs, and then specify appropriate email addresses.</span></span> <span data-ttu-id="477ba-212">その後、作業項目は Azure DevOps で作成され、承認のために所有者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="477ba-212">Work items will then be created in Azure DevOps and assigned to owners for approval.</span></span>

