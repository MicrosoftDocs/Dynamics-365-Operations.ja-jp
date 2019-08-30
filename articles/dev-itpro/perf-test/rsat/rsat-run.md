---
title: Regression Suite Automation Tool テスト ケースの実行
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
ms.openlocfilehash: 8a759691e098408b9373156f0066ffe74a007688
ms.sourcegitcommit: f79f2249d7557e578d7d3c4d6ea83682df7362d5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/14/2019
ms.locfileid: "1874852"
---
# <a name="run-regression-suite-automation-tool-test-cases"></a><span data-ttu-id="6a0b7-103">Regression Suite Automation Tool テスト ケースの実行</span><span class="sxs-lookup"><span data-stu-id="6a0b7-103">Run Regression suite automation tool test cases</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a0b7-104">このトピックでは、Azure DevOps からのテスト ケースの読み込み、自動化ファイルの生成、テストパラメータの変更、テストの実行、結果の調査、および Azure DevOps への作業内容の保存方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-104">This topic explains how to load test cases from Azure DevOps, generate automation files, modify test parameters, run tests, investigate results, and save your work back to Azure DevOps.</span></span>

## <a name="load-test-cases-and-create-automation-files"></a><span data-ttu-id="6a0b7-105">テスト ケースの読み込みと自動化ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="6a0b7-105">Load test cases and create automation files</span></span>
<span data-ttu-id="6a0b7-106">Azure DevOpsで、**ロード** を選択して、テスト ケースおよびテスト ケースの自動化ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-106">In Azure DevOps, select **Load** to download test cases and test case automation files.</span></span> <span data-ttu-id="6a0b7-107">**設定**ダイアログ ボックスで指定されたテスト計画に属するすべてのテスト ケースがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-107">All test cases belonging to the test plan specified in the **Settings** dialog box are downloaded.</span></span>
 
![テスト ケースの読み込み](media/load-test-cases.png)

<span data-ttu-id="6a0b7-109">テスト ケースは、共通のテスト計画に基づいてテスト スイートごとに編成されます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-109">Test cases are organized by test suites under a common test plan.</span></span> <span data-ttu-id="6a0b7-110">これらは、Azure DevOpsプロジェクトで作成したテスト スイートです。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-110">These are test suites you created in your Azure DevOps project.</span></span> <span data-ttu-id="6a0b7-111">このツールを使用すると、一度に1つのテスト スイートを操作できます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-111">Using this tool, you can work with one test suite at a time.</span></span>

<span data-ttu-id="6a0b7-112">ツールでテスト ケースの読み込みに失敗したときは、Azure DevOpsのテスト計画が適切に作成されていること、また、目的のテスト スイートおよびテスト ケースが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-112">If the tool fails to load any test case, verify that your test plan in Azure DevOps is properly created and contains the desired test suites and test cases.</span></span>

<span data-ttu-id="6a0b7-113">このテスト計画を初めて読み込むとき、**パラメーター ファイル**の列が空白になります。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-113">If this is the first time you load this test plan, the **Parameters File** column will be blank.</span></span> <span data-ttu-id="6a0b7-114">テスト ケースのテスト自動化ファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-114">You will need to create test automation files for your test cases.</span></span> <span data-ttu-id="6a0b7-115">テスト自動化ファイルの構成要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-115">Test automation files consist of:</span></span>

+ <span data-ttu-id="6a0b7-116">テスト パラメーター ファイル (Microsoft Excel ファイルにテスト ケース パラメーターが含まれています)</span><span class="sxs-lookup"><span data-stu-id="6a0b7-116">Test parameter files (Microsoft Excel files contain test case parameters)</span></span>
+ <span data-ttu-id="6a0b7-117">テストを実行するために必要なその他のバイナリ ファイルおよび XML ファイル。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-117">Other binary and XML files needed to execute the tests.</span></span>

<span data-ttu-id="6a0b7-118">**新規**を選択すると、テスト自動化ファイルが作業ディレクトリに生成されます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-118">When you select **New**, test automation files are generated in your working directory.</span></span> <span data-ttu-id="6a0b7-119">Excel テスト パラメーター ファイルが**パラメーター ファイル**の下のグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-119">The Excel test parameter files will appear on the grid under **Parameters File**.</span></span>

![読み込まれたテスト ケースの一覧](media/rsat-test-cases.png)
 
<span data-ttu-id="6a0b7-121">パラメーター ファイルを上書きせずに、バイナリ ファイルおよび XML ファイルのみを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-121">You can also generate binary and XML files only without overwriting your parameter files.</span></span> <span data-ttu-id="6a0b7-122">サブメニューの **新規 > 実行ファイルを生成する**を使用すると、実行ファイルのみが再生成され、Excel ファイルは影響を受けないままになります。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-122">Use submenu **New > Generate Execution Files** to only regenerate execution files and leave Excel files unaffected.</span></span> <span data-ttu-id="6a0b7-123">これは、通常、ツールの新しいバージョンをインストールするときに、テスト パラメーター ファイルを保持したまま実行ファイルを更新できるようにする場合に使用される方法です。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-123">This is typical when you install a new version of the tool, you can update your execution files while preserving the test parameter files.</span></span>

![テスト実行ファイルのみのメニュー項目を生成する](media/generate-execution-files.png)

## <a name="modify-test-parameters"></a><span data-ttu-id="6a0b7-125">テスト パラメーターの変更</span><span class="sxs-lookup"><span data-stu-id="6a0b7-125">Modify test parameters</span></span>

<span data-ttu-id="6a0b7-126">ここでは、Excel ファイルを変更して、テストの実行に使用する入力および検証のパラメータを指定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-126">This section describes how to modify Excel files to specify input and validation parameters for your test run.</span></span> <span data-ttu-id="6a0b7-127">変更する 1 つ以上のテスト ケースを選択し、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-127">Select one or more test cases you want to modify and select **Edit**.</span></span> <span data-ttu-id="6a0b7-128">これにより、選択したテスト ケースごとに Excel ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-128">This will open an Excel window for each selected test case.</span></span> <span data-ttu-id="6a0b7-129">または、作業ディレクトリから直接 Excel ファイルを開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-129">Alternatively, you can open the Excel files directly from the working directory.</span></span> 

<span data-ttu-id="6a0b7-130">**一般** タブに加えて、Excel ファイルには、テスト ケースがアクセスするすべての Finance and Operations フォームのデータ タブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-130">In addition to the **General** tab, the Excel file contains a data tab for every Finance and Operations form that the test case visits.</span></span>

<span data-ttu-id="6a0b7-131">編集する必要のあるフォーム (Excel タブ) を選択し、変更するパラメーター値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-131">Select the desired form (Excel tab) that you want to edit and identify the parameter values that you want to change.</span></span> <span data-ttu-id="6a0b7-132">値は、コントロール名によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-132">Values are identified by their control name.</span></span> <span data-ttu-id="6a0b7-133">正しいコントロールがわからない場合は、Finance and Operations でフォームを開き、値を変更するコントロールを右クリックし、**フォーム情報**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-133">If you are not sure which control is correct, open the form in Finance and Operations, right-click the control whose value you want to change, and select **form information**.</span></span>

<span data-ttu-id="6a0b7-134">編集が完了したら Excel ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-134">Save the Excel files when you are done making edits.</span></span>

### <a name="run-a-test-as-a-specific-user"></a><span data-ttu-id="6a0b7-135">特定のユーザーとしてテストを実行する</span><span class="sxs-lookup"><span data-stu-id="6a0b7-135">Run a test as a specific user</span></span>
<span data-ttu-id="6a0b7-136">既定では、テストは、管理者ロールを使用して Finance and Operations で実行されます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-136">By default, tests are executed in Finance and Operations using the admin role.</span></span> <span data-ttu-id="6a0b7-137">特定のセキュリティ ロールとしてテストを実行する場合は、Excel パラメーター ファイルの **一般** タブの **テストユーザー** パラメーターで、Finance and Operations の電子メール アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-137">If you want to run the test as a specific security role, specify the email address of a Finance and Operations user under the **Test User** parameter in the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="6a0b7-138">**テスト ユーザー**は、接続している Finance and Operations 環境の有効なユーザーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-138">The **Test User** must be a valid user of the Finance and Operations environments you are connecting to.</span></span> <span data-ttu-id="6a0b7-139">テストは、特定のユーザーが属しているセキュリティ ロールの下で実行されます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-139">The test will run under the security roles that the specific user belongs to.</span></span> <span data-ttu-id="6a0b7-140">この機能を機能させるには、バージョン 1.200 またはそれ以降のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-140">You need version 1.200 or newer for this feature to be functional.</span></span>

![テスト ユーザー列](media/run-specific-user.png)
 
### <a name="run-a-test-in-the-context-of-a-specific-company"></a><span data-ttu-id="6a0b7-142">特定の会社のコンテキストでテストを実行する</span><span class="sxs-lookup"><span data-stu-id="6a0b7-142">Run a test in the context of a specific company</span></span>
<span data-ttu-id="6a0b7-143">Excel パラメーター ファイルの **一般** タブでは、Finance and Operations 法人 (会社) の名前を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-143">The **General** tab of the Excel parameter file also allows you to specify the name of a Finance and Operations legal entity (Company).</span></span> <span data-ttu-id="6a0b7-144">この会社のコンテキスト内でテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-144">The test will run in the context of this company.</span></span> <span data-ttu-id="6a0b7-145">既定の会社を、ツールの **設定** ダイアログ ボックスで指定できます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-145">You can specify your default company in the **Settings** dialog box of the tool.</span></span>

### <a name="infolog-and-message-validation"></a><span data-ttu-id="6a0b7-146">情報ログおよびメッセージの検証</span><span class="sxs-lookup"><span data-stu-id="6a0b7-146">Infolog and message validation</span></span>
<span data-ttu-id="6a0b7-147">バージョン1.200 またはそれ以降のバージョンを使用して生成される Excel パラメーター ファイルには、 **messagevalidation** のタブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-147">Excel parameter files that are generated using version 1.200 or newer contain a **MessageValidation** tab.</span></span>

<span data-ttu-id="6a0b7-148">このタブには、**メッセージを検証**するためのメッセージを入力できます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-148">You can enter messages in this tab under **Message Validation**.</span></span> <span data-ttu-id="6a0b7-149">テスト ケースの実行が完了した後、ここで指定されたメッセージが Finance and Operations の情報ログに表示されるかどうかが検証されます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-149">After a test case completes execution, it validates that the messages specified here appear in the Finance and Operations Infolog.</span></span> <span data-ttu-id="6a0b7-150">これらのメッセージが見つからない場合、テスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-150">The test case will fail if these messages are not found.</span></span>

<span data-ttu-id="6a0b7-151">予想されるエラー メッセージを含むすべてのメッセージを特定できます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-151">You can specify any expected messages including error messages that are expected.</span></span> <span data-ttu-id="6a0b7-152">予期されたエラーが発生して、このセクション内に存在している場合、このテストは失敗しません。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-152">If an expected error occurred, but exists in this section, the test will not fail.</span></span>
 
![メッセージ検証の例](media/message-validation.png)


## <a name="run"></a><span data-ttu-id="6a0b7-154">実行</span><span class="sxs-lookup"><span data-stu-id="6a0b7-154">Run</span></span>
<span data-ttu-id="6a0b7-155">**実行**を選択して、選択済みのテストケースを実行します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-155">Select **Run** to execute the selected test cases.</span></span> <span data-ttu-id="6a0b7-156">既存の自動化ファイルを用いるテスト ケースのみを実行できます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-156">Only test cases with existing automation files can be run.</span></span> <span data-ttu-id="6a0b7-157">このツールでは、Finance and Operations が開き、Excel に入力したデータを使用して、これらのテストが実行されます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-157">The tool will open Finance and Operations and execute these tests with the data you entered in Excel.</span></span>

<span data-ttu-id="6a0b7-158">上下矢印ボタンを使用して、テスト ケースを実行する順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-158">You can modify the order in which test cases are executed using the up and down arrow buttons.</span></span>

### <a name="pause-prior-to-a-test-case-run"></a><span data-ttu-id="6a0b7-159">テスト ケース実行前の一時停止</span><span class="sxs-lookup"><span data-stu-id="6a0b7-159">Pause prior to a test case run</span></span> 
<span data-ttu-id="6a0b7-160">テスト ケース実行開始前に、一時停止を追加できます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-160">You can add a pause before a test case starts execution.</span></span> <span data-ttu-id="6a0b7-161">一時停止する場合は、Excel パラメーター ファイルの**一般**タブの**一時停止 (秒)** セルを更新します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-161">If you want to pause, update the cell **Pause (seconds)** on the **General** tab of the Excel parameters file.</span></span>

## <a name="investigate-results"></a><span data-ttu-id="6a0b7-162">結果の調査</span><span class="sxs-lookup"><span data-stu-id="6a0b7-162">Investigate results</span></span>
<span data-ttu-id="6a0b7-163">すべてのテスト ケースの実行が完了すると、**合格** または **不合格** が **結果** 列に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-163">When all test cases complete execution, **Pass** or **Fail** will be populated in the **Result** column.</span></span> <span data-ttu-id="6a0b7-164">結果をクリックすると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-164">You can click on the result to see error messages.</span></span>

<span data-ttu-id="6a0b7-165">Azure DevOps で入手できる追加の調査詳細。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-165">Additional investigation details are available in Azure DevOps.</span></span> <span data-ttu-id="6a0b7-166">この情報を表示するには Azure DevOps プロジェクトページから、**テスト > 実行** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-166">To view this information, from your Azure DevOps project page, go to **Test > Runs**.</span></span>

![テスト結果](media/test-results.png)

<span data-ttu-id="6a0b7-168">目的のテストの実行を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-168">Select the desired test run.</span></span> <span data-ttu-id="6a0b7-169">その実行中に実行されたすべてのテストの結果が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-169">It will include the results of all tests that were executed during that run.</span></span>
 
![結果の円グラフ](media/outcome-pie-chart.png)

![各テストの結果](media/pass-fail.png)

<span data-ttu-id="6a0b7-172">失敗したテスト結果を開いて、**ErrorMessage** セクションでエラーに関する情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-172">You can open a failed test result and review the **ErrorMessage** section for information about the failure.</span></span>
 
![エラー メッセージの情報](media/error-message.png)

<span data-ttu-id="6a0b7-174">すべてのエラー メッセージは、**C:\Users\$YourUserName\AppData\Roaming\regressionTool\errormsg-<TestCaseId>.txt** でローカルでも利用可能です。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-174">All error messages are also available locally under **C:\Users\$YourUserName\AppData\Roaming\regressionTool\errormsg-<TestCaseId>.txt**.</span></span>

### <a name="test-response-times"></a><span data-ttu-id="6a0b7-175">応答時間のテスト</span><span class="sxs-lookup"><span data-stu-id="6a0b7-175">Test response times</span></span>
<span data-ttu-id="6a0b7-176">実行ログに加えて、テスト ケースの期間もテスト結果で確認できます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-176">In addition to execution logs, the duration of a test case is also available in the test result.</span></span>
 
![テスト ケースの期間](media/test-duration.png)

<span data-ttu-id="6a0b7-178">テスト結果に添付されている **BaseTime.xml** ファイルを開くことにより、テスト ケースの各ステップの応答時間を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-178">You can also review the response time of each step of the test case by opening the **BaseTime.xml** file attached to the test result.</span></span>
 
![応答時間ファイル](media/response-time.png)

<span data-ttu-id="6a0b7-180">応答時間を機能させるには、バージョン 1.200 またはそれ以降のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-180">You need version 1.200 or newer for response times to be available.</span></span>

## <a name="save-your-work"></a><span data-ttu-id="6a0b7-181">作業を保存</span><span class="sxs-lookup"><span data-stu-id="6a0b7-181">Save your work</span></span>
<span data-ttu-id="6a0b7-182">作業内容を保存するには、**アップロード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-182">To preserve your work, select **Upload**.</span></span> <span data-ttu-id="6a0b7-183">これにより、選択したテスト ケースに関するテストの自動化ファイル (Excel テストパラメータ ファイルを含む) を、 Azure DevOps にアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-183">This will upload test automation files, including Excel test parameter files, of all selected test cases to Azure DevOps for future use.</span></span>
<span data-ttu-id="6a0b7-184">テスト自動化ファイルを Azure DevOps にアップロードした後は、次に Regression Suite Automation Tool を使用するときに、テストの実行ファイルを生成したり Excel パラメーター ファイルを編集したりすることなく、別のコンピューターからでも簡単に **読み込み**、**実行**できます。</span><span class="sxs-lookup"><span data-stu-id="6a0b7-184">After test automation files are uploaded to Azure DevOps, the next time you use the Regression suite automation tool, even from a different computer, you can simply use **Load** and then **Run**, without generating test execution files or editing Excel parameter files.</span></span>
