---
title: Regression Suite Automation Tool (RSAT) を使用したテスト ケースの実行
description: このトピックでは、Azure DevOps からのテスト ケースの読み込み、テストの実行、および作業内容を Azure DevOps に保存する方法について説明します。
author: FrankDahl
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a1dcd380d73ba383348d204f9e533284050cef7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745181"
---
# <a name="use-the-regression-suite-automation-tool-rsat"></a><span data-ttu-id="72356-103">Regression Suite Automation Tool (RSAT) の使用</span><span class="sxs-lookup"><span data-stu-id="72356-103">Use the Regression suite automation tool (RSAT)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72356-104">このトピックでは、Azure DevOps からのテスト ケースの読み込み、自動化ファイルの生成、テストパラメータの変更、結果の実行と調査、および Azure DevOps への作業内容の保存方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="72356-104">This topic explains how to load test cases from Azure DevOps, generate automation files, modify test parameters, run and investigate results, and save your work back to Azure DevOps.</span></span>

## <a name="load-test-cases-and-create-automation-files"></a><span data-ttu-id="72356-105">テスト ケースの読み込みと自動化ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="72356-105">Load test cases and create automation files</span></span>

<span data-ttu-id="72356-106">RSAT で、**テスト計画** タブを選択し、**読み込み** を選択して、テスト ケースとテスト ケース自動化ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="72356-106">In RSAT, select the **Test Plans** tab and then select **Load** to download test cases and test case automation files.</span></span> <span data-ttu-id="72356-107">**設定** タブで指定されたテスト計画に属する全てのテスト ケース (および対応する添付ファイル) は、ローカルの作業ディレクトリにダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="72356-107">All test cases (and their corresponding attachments) belonging to the test plan specified in the **Settings** tab are downloaded to the local working directory.</span></span>

![テスト ケースの読み込み](media/load-test-cases.png)

<span data-ttu-id="72356-109">テスト ケースは、共通のテスト計画に基づいてテスト スイートごとに編成されます。</span><span class="sxs-lookup"><span data-stu-id="72356-109">Test cases are organized by test suites under a common test plan.</span></span> <span data-ttu-id="72356-110">これらは、Azure DevOpsプロジェクトで作成したテスト スイートです。</span><span class="sxs-lookup"><span data-stu-id="72356-110">These are test suites you created in your Azure DevOps project.</span></span> <span data-ttu-id="72356-111">このツールを使用すると、一度に1つのテスト スイートを操作できます。</span><span class="sxs-lookup"><span data-stu-id="72356-111">Using this tool, you can work with one test suite at a time.</span></span>

<span data-ttu-id="72356-112">ツールでテスト ケースの読み込みに失敗したときは、Azure DevOpsのテスト計画が適切に作成されていること、また、目的のテスト スイートおよびテスト ケースが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="72356-112">If the tool fails to load any test case, verify that your test plan in Azure DevOps is properly created and contains the desired test suites and test cases.</span></span>

<span data-ttu-id="72356-113">このテスト計画を初めて使用する場合は、**パラメーター ファイル** 列が空白になります。</span><span class="sxs-lookup"><span data-stu-id="72356-113">If this is the first time you are using this test plan, the **Parameters File** column will be blank.</span></span> <span data-ttu-id="72356-114">テスト ケース用のテスト自動化ファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72356-114">You must create test automation files for your test cases.</span></span>

<span data-ttu-id="72356-115">テスト ケースでは、正常に実行するために次の添付ファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="72356-115">A test case requires the following attachments for successful execution:</span></span>

+ <span data-ttu-id="72356-116">**記録ファイル**: Finance and Operations タスク レコーダーによって作成された記録ファイルです。</span><span class="sxs-lookup"><span data-stu-id="72356-116">A **recording file**: This is the recording file created by the Finance and Operations Task recorder.</span></span> <span data-ttu-id="72356-117">これにより、テスト ケースのステップが定義されます。</span><span class="sxs-lookup"><span data-stu-id="72356-117">It defines the steps of your test case.</span></span> <span data-ttu-id="72356-118">通常は **recording.xml** という名前ですが、Azure DevOps のテスト ケースのタイトルと一致するように名前を付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="72356-118">It is typically named **recording.xml** or but you can also name it to match the test case title in Azure DevOps.</span></span> <span data-ttu-id="72356-119">Azure DevOps のテスト ケースに添付され、テスト ケースのローカル作業ディレクトリの **添付** フォルダーにダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="72356-119">It is attached to the test case in Azure DevOps and downloaded into the **attachment** folder of the local working directory of the test case.</span></span>
+ <span data-ttu-id="72356-120">**テスト自動化ファイル** は、構成可能なテスト ケース パラメーターを含む **テスト パラメーター ファイル** (Microsoft Excel ファイル) と **テスト実行ファイル** で構成されます。これらのファイルは、テスト記録の自動実行を可能にするために RSAT によって生成されます。</span><span class="sxs-lookup"><span data-stu-id="72356-120">**Test automation files** consisting of **a test parameter file** (Microsoft Excel file) containing configurable test case parameters and **test execution files**: These files are generated by RSAT to enable automated execution of the test recording.</span></span> <span data-ttu-id="72356-121">ファイル名には **_Base.cs**、**_Base.xml**、および **_Base.dll** などの接尾語が使用されます。</span><span class="sxs-lookup"><span data-stu-id="72356-121">Filenames are suffixed by **_Base.cs**, **_Base.xml**, and **_Base.dll**.</span></span>

<span data-ttu-id="72356-122">**新規** を選択すると、テスト自動化ファイルが作業ディレクトリに生成されます。</span><span class="sxs-lookup"><span data-stu-id="72356-122">When you select **New**, test automation files are generated in your working directory.</span></span> <span data-ttu-id="72356-123">Excel テスト パラメーター ファイルが **パラメーター ファイル** の下のグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="72356-123">The Excel test parameter files will appear on the grid under **Parameters File**.</span></span>

![読み込まれたテスト ケースの一覧](media/rsat-test-cases.png)

<span data-ttu-id="72356-125">また、パラメーター ファイルを上書きせずに、**テスト実行ファイル** だけを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="72356-125">You can also generate **test execution files** only, without overwriting your parameter files.</span></span> <span data-ttu-id="72356-126">**新規 \> 実行ファイルの生成** を選択して、実行ファイルのみを再生成し、Excel ファイルは影響を受けないままにします。</span><span class="sxs-lookup"><span data-stu-id="72356-126">Select **New \> Generate Execution Files** to regenerate only execution files and leave Excel files unaffected.</span></span>

<span data-ttu-id="72356-127">ツールの新しいバージョンをインストールするとき、および新しいバージョンの記録ファイルを変更または読み込むときに、テスト実行ファイルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72356-127">You must generate test execution files when you install a new version of the tool, and when you modify or load a new version of the recording file.</span></span> <span data-ttu-id="72356-128">このようにして、実行ファイルを更新するだけでなく、テスト パラメーター ファイルも保持できます。</span><span class="sxs-lookup"><span data-stu-id="72356-128">In this way, you update your execution files but also preserve the test parameter files.</span></span>

![テスト実行ファイルのみのメニュー項目を生成する](media/generate-execution-files.png)

## <a name="modify-test-parameters"></a><span data-ttu-id="72356-130">テスト パラメーターの変更</span><span class="sxs-lookup"><span data-stu-id="72356-130">Modify test parameters</span></span>

<span data-ttu-id="72356-131">ここでは、Excel ファイルを変更して、テストの実行に使用する入力および検証のパラメータを指定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="72356-131">This section describes how to modify Excel files to specify input and validation parameters for your test run.</span></span> <span data-ttu-id="72356-132">変更する 1 つ以上のテスト ケースを選択し、ツール バーで **パラメーター** ボタン (Microsoft Excel 記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="72356-132">Select one or more test cases to modify, and then select the **Parameters** button (Microsoft Excel symbol) on the toolbar.</span></span> <span data-ttu-id="72356-133">選択したテスト ケースごとに Excel ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="72356-133">An Excel window opens for each test case that you selected.</span></span> <span data-ttu-id="72356-134">または、作業ディレクトリから直接 Excel ファイルを開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="72356-134">Alternatively, you can open the Excel files directly from the working directory.</span></span>

<span data-ttu-id="72356-135">**一般** タブに加えて、Excel パラメーター ファイルには **MessageValidation** タブおよび **TestCaseSteps** タブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="72356-135">In addition to the **General** tab, the Excel parameter file contains a **MessageValidation** tab and a **TestCaseSteps** tab.</span></span>

<span data-ttu-id="72356-136">**TestCaseSteps** タブを選択して、テスト ケースの入力パラメーターおよび検証パラメーターを構成します。</span><span class="sxs-lookup"><span data-stu-id="72356-136">Select the **TestCaseSteps** tab to configure input and validation parameters of your test case.</span></span> <span data-ttu-id="72356-137">入力パラメーターおよび検証パラメーターは、対応するテスト ケース ステップの横に配置され、テスト作成者はコンテキストと簡単なエクスペリエンスを得ることができます。</span><span class="sxs-lookup"><span data-stu-id="72356-137">Input and validation parameters are placed directly next to their corresponding test case step, enabling test authors with context and a simple experience.</span></span> <span data-ttu-id="72356-138">パラメーターを変更すると、テスト ケースのどのステップに影響を与えているかが明確になります。</span><span class="sxs-lookup"><span data-stu-id="72356-138">When you modify parameters, it is clear what steps of the test case you are affecting.</span></span> <span data-ttu-id="72356-139">コンテキスト内の値または式を入力できます。</span><span class="sxs-lookup"><span data-stu-id="72356-139">You can enter values or formulas in context.</span></span> <span data-ttu-id="72356-140">カラー コーディングにより、入力パラメーターと検証ステップが区別されます。</span><span class="sxs-lookup"><span data-stu-id="72356-140">Color coding differentiates input parameters from validation steps.</span></span>

![テスト ケース ステップ](media/test-case-steps.PNG)

<span data-ttu-id="72356-142">テスト ケースの記録中にコピーされた再利用可能な変数も、テスト ケース ステップのコンテキストで表示されます。</span><span class="sxs-lookup"><span data-stu-id="72356-142">Reusable variables that are copied while recording the test case are also shown in context of the test case step.</span></span> <span data-ttu-id="72356-143">変数を簡単に検索してコピーし、次のステップや式で使用できます。</span><span class="sxs-lookup"><span data-stu-id="72356-143">You can easily locate a variable and copy it to use in subsequent steps and formulas.</span></span> <span data-ttu-id="72356-144">詳細については、[変数をコピーしてテスト ケースに連鎖させる方法](rsat-chain-test-cases.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72356-144">For more information, see [Copy variables to chain test cases](rsat-chain-test-cases.md).</span></span>

![テスト ケース ステップ変数](media/test-case-steps-rsat-var.png)

<span data-ttu-id="72356-146">編集が完了したら Excel ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="72356-146">Save the Excel files when you are done making edits.</span></span>

### <a name="run-a-test-as-a-specific-user"></a><span data-ttu-id="72356-147">特定のユーザーとしてテストを実行する</span><span class="sxs-lookup"><span data-stu-id="72356-147">Run a test as a specific user</span></span>

<span data-ttu-id="72356-148">既定では、テストは管理者ロールを使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="72356-148">By default, tests are executed using the admin role.</span></span> <span data-ttu-id="72356-149">特定のセキュリティ ロールとしてテストを実行する場合は、Excel パラメーター ファイルの **一般** タブにある **テスト ユーザー** パラメーターでユーザーの電子メール アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="72356-149">If you want to run the test as a specific security role, specify the email address of a user under the **Test User** parameter in the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="72356-150">**テスト ユーザー** は、接続している環境の有効なユーザーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="72356-150">The **Test User** must be a valid user of the environments you are connecting to.</span></span> <span data-ttu-id="72356-151">テストは、特定のユーザーが属しているセキュリティ ロールの下で実行されます。</span><span class="sxs-lookup"><span data-stu-id="72356-151">The test will run under the security roles that the specific user belongs to.</span></span> <span data-ttu-id="72356-152">この機能を機能させるには、バージョン 1.200 またはそれ以降のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="72356-152">You need version 1.200 or newer for this feature to be functional.</span></span>

![Excel パラメーター ファイルの一般タブ](media/rsat-excel-general-tab.png)

### <a name="run-a-test-in-the-context-of-a-specific-company"></a><span data-ttu-id="72356-154">特定の会社のコンテキストでテストを実行する</span><span class="sxs-lookup"><span data-stu-id="72356-154">Run a test in the context of a specific company</span></span>

<span data-ttu-id="72356-155">Excel パラメーター ファイルの **一般** タブでは、法人 (会社) の名前を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="72356-155">The **General** tab of the Excel parameter file also allows you to specify the name of a legal entity (Company).</span></span> <span data-ttu-id="72356-156">この会社のコンテキスト内でテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="72356-156">The test will run in the context of this company.</span></span> <span data-ttu-id="72356-157">既定の会社を、ツールの **設定** ダイアログ ボックスで指定できます。</span><span class="sxs-lookup"><span data-stu-id="72356-157">You can specify your default company in the **Settings** dialog box of the tool.</span></span>

### <a name="pause-after-a-specific-test-step"></a><span data-ttu-id="72356-158">特定のテスト ステップの後で一時停止する</span><span class="sxs-lookup"><span data-stu-id="72356-158">Pause after a specific test step</span></span>

<span data-ttu-id="72356-159">特定のテスト ステップ間に一時停止を挿入できます。</span><span class="sxs-lookup"><span data-stu-id="72356-159">You can insert a pause between specific test steps.</span></span> <span data-ttu-id="72356-160">Excel パラメーター ファイルの **TestCaseSteps** タブに移動し、テスト ステップの一時停止列に値 (秒) を挿入します。</span><span class="sxs-lookup"><span data-stu-id="72356-160">Navigate to the **TestCaseSteps** tab of the Excel parameters file and insert a value (in seconds) in the pause column of a test step.</span></span> <span data-ttu-id="72356-161">これにより、テスト ステップの完了後、テスト ケースの実行が一時停止されます。</span><span class="sxs-lookup"><span data-stu-id="72356-161">This will pause test cases execution after the test step is completed.</span></span>

![顧客 ID フィールドに対する一時停止設定](media/Pause-after-specific-step.png)

<span data-ttu-id="72356-163">**一時停止** 列が表示されない場合、Excel パラメーター ファイルの古いバージョンを使用し、再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72356-163">If you don’t see the **Pause** column, you are using an older version of the Excel parameters file and need to regenerate it.</span></span> <span data-ttu-id="72356-164">目的のテスト ケースを選択し、**新規 > テスト実行とパラメーター ファイルの生成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="72356-164">Select the desired test case, then go to **New > Generate Test Execution and Parameter Files**.</span></span> <span data-ttu-id="72356-165">パラメーター ファイルに対して行った編集が上書きされる可能性があるため、既存の Excel ファイルを先にバックアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="72356-165">This may override edits you have made to the parameters file, so you should back up the existing Excel file first.</span></span>

### <a name="other-notable-test-case-execution-settings"></a><span data-ttu-id="72356-166">その他の重要なテスト ケースの実行の設定</span><span class="sxs-lookup"><span data-stu-id="72356-166">Other notable test case execution settings</span></span>

<span data-ttu-id="72356-167">次の設定が役立つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="72356-167">You may find the following settings useful.</span></span> <span data-ttu-id="72356-168">これらは、Excel パラメーター ファイルの **一般** タブで使用できます。</span><span class="sxs-lookup"><span data-stu-id="72356-168">They are available on the **General** tab of the Excel parameter file.</span></span>

+ <span data-ttu-id="72356-169">**情報ログの警告メッセージで失敗**: 既定では、エラーが発生、または検証ステップが失敗した場合、テスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="72356-169">**Fail on warning message in the Infolog**: By default, test cases fail when an error occurs or a validation step fails.</span></span> <span data-ttu-id="72356-170">警告メッセージに応じてテスト ケースも失敗させたい場合は、**情報ログの警告メッセージで失敗** オプションを **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="72356-170">If you also want a test case to fail in response to a warning message, set the **Fail on warning message in the Infolog** option to **True** .</span></span> <span data-ttu-id="72356-171">これは、たとえば、テスト ケースで重複する顧客レコードを追加する場合などに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="72356-171">This is useful, for example, if a test case adds a duplicate customer record.</span></span> <span data-ttu-id="72356-172">既定の設定は **False** です。</span><span class="sxs-lookup"><span data-stu-id="72356-172">The default setting is **False**.</span></span>
+ <span data-ttu-id="72356-173">**失敗時にテスト スイートの実行を中止する**: **失敗時にテスト スイートの実行を中止する** オプションを **True** に設定した場合、テスト ケースが失敗すると、テスト スイートの実行は中止されます。</span><span class="sxs-lookup"><span data-stu-id="72356-173">**Abort test suite execution on failure**: If you set the **Abort test suite execution on failure** option to **True**, execution of the test suite is aborted if the test case fails.</span></span> <span data-ttu-id="72356-174">残りのすべてのテスト ケースのステータスは **未実行** になります。</span><span class="sxs-lookup"><span data-stu-id="72356-174">All the remaining test cases will have a status of **Not Executed**.</span></span> <span data-ttu-id="72356-175">既定の設定は **False** です。</span><span class="sxs-lookup"><span data-stu-id="72356-175">The default setting is **False**.</span></span>
+ <span data-ttu-id="72356-176">**ステップ間の一時停止**: テスト ステップ間で一時停止する秒数。</span><span class="sxs-lookup"><span data-stu-id="72356-176">**Pause between steps**: The number of seconds to pause between test steps.</span></span> <span data-ttu-id="72356-177">これは、すべてのテスト ステップに影響します。</span><span class="sxs-lookup"><span data-stu-id="72356-177">This will affect every test step.</span></span> <span data-ttu-id="72356-178">既定値は **0** (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="72356-178">The default value is **0** (zero).</span></span>

### <a name="infolog-and-message-validation"></a><span data-ttu-id="72356-179">情報ログおよびメッセージの検証</span><span class="sxs-lookup"><span data-stu-id="72356-179">Infolog and message validation</span></span>

<span data-ttu-id="72356-180">バージョン1.200 またはそれ以降のバージョンを使用して生成される Excel パラメーター ファイルには、 **messagevalidation** のタブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="72356-180">Excel parameter files that are generated using version 1.200 or newer contain a **MessageValidation** tab.</span></span>

<span data-ttu-id="72356-181">このタブには、**メッセージを検証** するためのメッセージを入力できます。</span><span class="sxs-lookup"><span data-stu-id="72356-181">You can enter messages in this tab under **Message Validation**.</span></span> <span data-ttu-id="72356-182">テスト ケースが実行を完了した後、ここで指定されたメッセージが情報ログに表示されることを検証します。</span><span class="sxs-lookup"><span data-stu-id="72356-182">After a test case completes execution, it validates that the messages specified here appear in the Infolog.</span></span> <span data-ttu-id="72356-183">これらのメッセージが見つからない場合、テスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="72356-183">The test case will fail if these messages are not found.</span></span>

<span data-ttu-id="72356-184">エラー メッセージを含む、予期されるメッセージを指定できます。</span><span class="sxs-lookup"><span data-stu-id="72356-184">You can specify any expected messages including error messages.</span></span> <span data-ttu-id="72356-185">このセクションで指定されたメッセージは、実行中に情報ログで検出されていない限り、テスト ケースが失敗する原因になります。</span><span class="sxs-lookup"><span data-stu-id="72356-185">Any message specified in this section will cause a test case to fail unless it is found in the Infolog during execution.</span></span> <span data-ttu-id="72356-186">**Equals** と **Contains** の 2 つの演算子を使用できます。</span><span class="sxs-lookup"><span data-stu-id="72356-186">Two operators are available: **Equals** and **Contains**.</span></span> <span data-ttu-id="72356-187">**Equals** を使用する場合、RSAT は情報ログ内のすべてのメッセージと文字列比較を実行し、完全なメッセージが見つからない場合は検証に失敗します。</span><span class="sxs-lookup"><span data-stu-id="72356-187">If you use **Equals**, then RSAT performs a string comparison with all messages in the Infolog and fails validation if the full message is not found.</span></span> <span data-ttu-id="72356-188">**Contains** を使用する場合、RSAT は情報ログの少なくとも 1 つのメッセージに指定した文字列が含まれていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="72356-188">If you use **Contains**, then RSAT will validate that at least one message in the Infolog contains the string you specify.</span></span>

![メッセージ検証の例](media/message-validation.png)

<span data-ttu-id="72356-190">文字列比較で大文字と小文字を区別するかどうかは、**設定** タブの **オプション** ページで構成できます。</span><span class="sxs-lookup"><span data-stu-id="72356-190">You can configure whether string comparison is case sensitive or not in the **Optional** page of the **Settings** tab.</span></span>

## <a name="run"></a><span data-ttu-id="72356-191">実行</span><span class="sxs-lookup"><span data-stu-id="72356-191">Run</span></span>

<span data-ttu-id="72356-192">**実行** を選択して、選択済みのテストケースを実行します。</span><span class="sxs-lookup"><span data-stu-id="72356-192">Select **Run** to execute the selected test cases.</span></span> <span data-ttu-id="72356-193">既存の自動化ファイルを用いるテスト ケースのみを実行できます。</span><span class="sxs-lookup"><span data-stu-id="72356-193">Only test cases with existing automation files can be run.</span></span> <span data-ttu-id="72356-194">ツールでは、Excel に入力されたデータを使用して、これらのテストが開かれ実行されます。</span><span class="sxs-lookup"><span data-stu-id="72356-194">The tool will open and execute these tests with the data you entered in Excel.</span></span>

<span data-ttu-id="72356-195">上下矢印ボタンを使用して、テスト ケースを実行する順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="72356-195">You can modify the order in which test cases are executed using the up and down arrow buttons.</span></span>

### <a name="pause-prior-to-a-test-case-run"></a><span data-ttu-id="72356-196">テスト ケース実行前の一時停止</span><span class="sxs-lookup"><span data-stu-id="72356-196">Pause prior to a test case run</span></span>

<span data-ttu-id="72356-197">テスト ケース実行開始前に、一時停止を追加できます。</span><span class="sxs-lookup"><span data-stu-id="72356-197">You can add a pause before a test case starts execution.</span></span> <span data-ttu-id="72356-198">一時停止する場合は、目的のテスト ケースの Excel パラメーター ファイルの **一般** タブで、セル **一時停止 (秒)** を更新します。</span><span class="sxs-lookup"><span data-stu-id="72356-198">If you want to pause, update the cell **Pause (seconds)** on the **General** tab of the Excel parameters file of the desired test case.</span></span>

### <a name="stop-a-run"></a><span data-ttu-id="72356-199">実行の停止</span><span class="sxs-lookup"><span data-stu-id="72356-199">Stop a run</span></span>

<span data-ttu-id="72356-200">テストの実行が進行中の場合は、ツールバーの **停止** ボタンを選択して実行をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="72356-200">When a test run is in progress, you can select the **Stop** button on the toolbar to cancel the run.</span></span> <span data-ttu-id="72356-201">現在実行中のテスト ケースが完了した後で実行が停止します。</span><span class="sxs-lookup"><span data-stu-id="72356-201">Execution stops after the currently running test case completes.</span></span> <span data-ttu-id="72356-202">残りのテスト ケースは、Azure DevOps で **未実行** とマークされます。</span><span class="sxs-lookup"><span data-stu-id="72356-202">The remaining test cases will be marked as **Not Executed** in Azure DevOps.</span></span>

### <a name="validate-readiness-of-test-automation-files"></a><span data-ttu-id="72356-203">テスト自動化ファイルの準備状況の検証</span><span class="sxs-lookup"><span data-stu-id="72356-203">Validate readiness of test automation files</span></span>

<span data-ttu-id="72356-204">必要に応じて、テスト ケースの実行準備が整っているかどうかを検証する設定を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="72356-204">Optionally, you can turn on a setting that validates whether your test cases are ready for execution.</span></span> <span data-ttu-id="72356-205">この設定により、レコーディングおよびテスト自動化ファイルの有効性に関連する不明なエラーが防止されます。</span><span class="sxs-lookup"><span data-stu-id="72356-205">This setting prevents unknown errors related to the validity of recordings and test automation files.</span></span> <span data-ttu-id="72356-206">このオプションは、RSAT バージョン 1.210 で使用できます。</span><span class="sxs-lookup"><span data-stu-id="72356-206">This option is available as of RSAT version 1.210.</span></span> <span data-ttu-id="72356-207">これを有効にするには、**設定** タブを選択し、**オプション** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="72356-207">You can enable this by selecting the **Settings** tab and then selecting the **Optional** tab.</span></span>

![ローカル ファイル検証ルールを有効にする設定](media/enable-local-file-validation-rules.png)

<span data-ttu-id="72356-209">有効にすると、バックグラウンド プロセスによって、各テスト ケースの次の項目が継続的に検証されます。</span><span class="sxs-lookup"><span data-stu-id="72356-209">When enabled, a background process continuously validates the following for each test case.</span></span>

+ <span data-ttu-id="72356-210">ローカルの作業ディレクトリが存在します。</span><span class="sxs-lookup"><span data-stu-id="72356-210">The local working directory exists.</span></span>
+ <span data-ttu-id="72356-211">Excel パラメーター ファイルが存在します。</span><span class="sxs-lookup"><span data-stu-id="72356-211">The Excel parameter file exists.</span></span>
+ <span data-ttu-id="72356-212">実行に必要なテスト自動化ファイル (バイナリ ファイルまたは Xml ファイル) が存在します。</span><span class="sxs-lookup"><span data-stu-id="72356-212">Test automation files (binary and Xml files) needed for execution exist.</span></span>
+ <span data-ttu-id="72356-213">テスト自動化ファイルは、RSAT の現在のバージョンと互換性があります。</span><span class="sxs-lookup"><span data-stu-id="72356-213">Test automation files are compatible with current version of RSAT.</span></span> <span data-ttu-id="72356-214">新しいバージョンの RSAT をインストールするときに、テスト自動化ファイルを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72356-214">You must regenerate test automation files when you install a new version of RSAT.</span></span>
+ <span data-ttu-id="72356-215">Excel パラメーター ファイルに指定されたテスト ケース ID は、Azure DevOps のテスト ケース ID と一致します。</span><span class="sxs-lookup"><span data-stu-id="72356-215">Test case ID specified in the Excel parameter file matches the test cases ID in Azure DevOps.</span></span>

<span data-ttu-id="72356-216">グリッドの有効な列は、検証プロセスの結果を示します。</span><span class="sxs-lookup"><span data-stu-id="72356-216">The Valid column in the grid indicates the result of the validation process.</span></span> <span data-ttu-id="72356-217">検証が失敗した場合は、**有効** 列の **X** をクリックすると、エラーと推奨されるアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72356-217">If validation fails, click on the **X** in the **Valid** column to view the error and recommended action.</span></span>

![有効な列グリッド](media/enable-local-file-validation-rules-2.png)

## <a name="investigate-results"></a><span data-ttu-id="72356-219">結果の調査</span><span class="sxs-lookup"><span data-stu-id="72356-219">Investigate results</span></span>

<span data-ttu-id="72356-220">すべてのテスト ケースの実行が完了すると、**合格** または **不合格** が **結果** 列に設定されます。</span><span class="sxs-lookup"><span data-stu-id="72356-220">When all test cases complete execution, **Pass** or **Fail** will be populated in the **Result** column.</span></span> <span data-ttu-id="72356-221">結果をクリックすると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72356-221">You can click on the result to see error messages.</span></span>

<span data-ttu-id="72356-222">Azure DevOps で入手できる追加の調査詳細。</span><span class="sxs-lookup"><span data-stu-id="72356-222">Additional investigation details are available in Azure DevOps.</span></span> <span data-ttu-id="72356-223">この情報を表示するには Azure DevOps プロジェクトページから、**テスト > 実行** に移動します。</span><span class="sxs-lookup"><span data-stu-id="72356-223">To view this information, from your Azure DevOps project page, go to **Test > Runs**.</span></span>

![テスト結果](media/test-results.png)

<span data-ttu-id="72356-225">目的のテストの実行を選択します。</span><span class="sxs-lookup"><span data-stu-id="72356-225">Select the desired test run.</span></span> <span data-ttu-id="72356-226">その実行中に実行されたすべてのテストの結果が含まれます。</span><span class="sxs-lookup"><span data-stu-id="72356-226">It will include the results of all tests that were executed during that run.</span></span>

![結果の円グラフ](media/outcome-pie-chart.png)

![各テストの結果](media/pass-fail.png)

<span data-ttu-id="72356-229">失敗したテスト結果を開いて、**ErrorMessage** セクションでエラーに関する情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="72356-229">You can open a failed test result and review the **ErrorMessage** section for information about the failure.</span></span>

![エラー メッセージの情報](media/error-message.png)

<span data-ttu-id="72356-231">すべてのエラー メッセージは、**C:\Users\$YourUserName\AppData\Roaming\regressionTool\errormsg-<TestCaseId>.txt** でローカルでも利用可能です。</span><span class="sxs-lookup"><span data-stu-id="72356-231">All error messages are also available locally under **C:\Users\$YourUserName\AppData\Roaming\regressionTool\errormsg-<TestCaseId>.txt**.</span></span>

### <a name="test-response-times"></a><span data-ttu-id="72356-232">応答時間のテスト</span><span class="sxs-lookup"><span data-stu-id="72356-232">Test response times</span></span>

<span data-ttu-id="72356-233">実行ログに加えて、テスト ケースの期間もテスト結果で確認できます。</span><span class="sxs-lookup"><span data-stu-id="72356-233">In addition to execution logs, the duration of a test case is also available in the test result.</span></span>

![テスト ケースの期間](media/test-duration.png)

<span data-ttu-id="72356-235">テスト結果に添付されている **BaseTime.xml** ファイルを開くことにより、テスト ケースの各ステップの応答時間を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="72356-235">You can also review the response time of each step of the test case by opening the **BaseTime.xml** file attached to the test result.</span></span>

![応答時間ファイル](media/response-time.png)

<span data-ttu-id="72356-237">応答時間を機能させるには、バージョン 1.200 またはそれ以降のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="72356-237">You need version 1.200 or newer for response times to be available.</span></span>

## <a name="upload-to-azure-devops-to-commit-your-work"></a><span data-ttu-id="72356-238">Azure DevOps にアップロードして作業をコミットします。</span><span class="sxs-lookup"><span data-stu-id="72356-238">Upload to Azure DevOps to commit your work</span></span>

<span data-ttu-id="72356-239">Azure DevOps に作業をコミットするには、**アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72356-239">To commit your work to Azure DevOps, select **Upload**.</span></span> <span data-ttu-id="72356-240">これにより、選択したテスト ケースの記録およびテストの自動化ファイル (Excel テスト パラメーター ファイルを含む) が、将来の使用のために Azure DevOps にアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="72356-240">This uploads recordings and test automation files, including Excel test parameter files, of all selected test cases to Azure DevOps for future use.</span></span> <span data-ttu-id="72356-241">テスト自動化ファイルを Azure DevOps にアップロードした後は、次に Regression Suite Automation Tool を使用するときに、テストの実行ファイルを生成したり Excel パラメーター ファイルを編集したりすることなく、別のコンピューターからでも簡単に **読み込み**、**実行** できます。</span><span class="sxs-lookup"><span data-stu-id="72356-241">After test automation files are uploaded to Azure DevOps, the next time you use the Regression suite automation tool, even from a different computer, you can simply use **Load** and then **Run**, without generating test execution files or editing Excel parameter files.</span></span>

<span data-ttu-id="72356-242">アップロード メニューには、レコーディング ファイル (タスクの記録) のみをアップロードするためのオプションも用意されています。</span><span class="sxs-lookup"><span data-stu-id="72356-242">In the upload menu, you also have the option to upload recording files (Task recordings) only.</span></span>

<span data-ttu-id="72356-243">選択するテスト ケースがわからない場合に、(前回の読み込み以降の) すべての変更を Azure DevOps にコミットするには、アップロード メニューで **すべての変更されたオートメーション ファイルをアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72356-243">If you are unsure what test cases to select, and you want to commit all changes (since last load) to Azure DevOps, select **Upload all modified automation files** in the upload menu.</span></span>

## <a name="process-compliance"></a><span data-ttu-id="72356-244">コンプライアンスのプロセス</span><span class="sxs-lookup"><span data-stu-id="72356-244">Process compliance</span></span>

<span data-ttu-id="72356-245">RSAT には、テスト ケースの準備状況を管理する機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="72356-245">RSAT provides capabilities for managing the readiness of test cases.</span></span> <span data-ttu-id="72356-246">また、テストの実行のためのサインオフ プロセスも用意されています。</span><span class="sxs-lookup"><span data-stu-id="72356-246">It also provides a sign-off process for test runs.</span></span> <span data-ttu-id="72356-247">これは、設定の **プロセス** タブでコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="72356-247">This is configurable in the **Process** tab under Settings.</span></span>

![コンプライアンス ファイルのプロセス](media/rsat-process-compliance-settings.png)

### <a name="enforce-test-case-readiness"></a><span data-ttu-id="72356-249">テスト ケースの準備完了を適用する</span><span class="sxs-lookup"><span data-stu-id="72356-249">Enforce test case readiness</span></span>

<span data-ttu-id="72356-250">Azure DevOps で **準備完了** のステータスがない限り、テスト ケースが実行されないように設定できます。</span><span class="sxs-lookup"><span data-stu-id="72356-250">You can set up the test case so that it isn't run unless it has a status of **Ready** in Azure DevOps.</span></span> <span data-ttu-id="72356-251">**テスト ケースの準備完了を適用する** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="72356-251">Select the **Enforce test case readiness** check box.</span></span> <span data-ttu-id="72356-252">既定では、このチェック ボックスはオフになっています。</span><span class="sxs-lookup"><span data-stu-id="72356-252">By default, the check box is cleared.</span></span>

### <a name="signoffs"></a><span data-ttu-id="72356-253">サインオフ</span><span class="sxs-lookup"><span data-stu-id="72356-253">Signoffs</span></span>

<span data-ttu-id="72356-254">テストの実行が完了すると、RSAT によって Azure DevOps にサインオフ作業項目が作成されます。</span><span class="sxs-lookup"><span data-stu-id="72356-254">When your test run is complete, RSAT can create sign-off work items in Azure DevOps.</span></span> <span data-ttu-id="72356-255">**サインオフ タスク** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="72356-255">Select the **Sign-off tasks** check box.</span></span> <span data-ttu-id="72356-256">次に、サインオフする各ユーザーに対して作成する作業項目のタイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="72356-256">Then set the type of work item that should be created for each person who signs off.</span></span> <span data-ttu-id="72356-257">サインオフには、**機能**、**IT マネージャー**、または **チーム マネージャー** ロールを選択してから、適切な電子メール アドレスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="72356-257">You can select the **Functional**, **IT Manager**, or **Team Manager** role for sign-offs, and then specify appropriate email addresses.</span></span> <span data-ttu-id="72356-258">その後、作業項目は Azure DevOps で作成され、承認のために所有者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="72356-258">Work items will then be created in Azure DevOps and assigned to owners for approval.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]