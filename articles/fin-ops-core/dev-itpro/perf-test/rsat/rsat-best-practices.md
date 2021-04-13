---
title: Regression Suite Automation Tool ベスト プラクティス
description: このトピックでは、Regression Suite Automation Tool (RSAT)/タスクレコーダーを使用して、クライアントの機能を記録する方法について説明します。
author: FrankDahl
ms.date: 08/01/2019
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
ms.openlocfilehash: c7b65c0c10b706839b25493680baad8d0c8cdf09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752684"
---
# <a name="regression-suite-automation-tool-best-practices"></a><span data-ttu-id="0c490-103">Regression Suite Automation Tool ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="0c490-103">Regression suite automation tool best practices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c490-104">このトピックでは、Regression Suite Automation Tool (RSAT) およびタスク レコーダーのベスト プラクティスと一般的な使用例について説明します。</span><span class="sxs-lookup"><span data-stu-id="0c490-104">This topic describes best practices and common use cases of the Regression suite automation tool (RSAT) and Task recorder.</span></span>

## <a name="author-test-cases-using-the-task-recorder"></a><span data-ttu-id="0c490-105">タスク レコーダーを使用したテスト ケースの作成</span><span class="sxs-lookup"><span data-stu-id="0c490-105">Author test cases using the Task recorder</span></span>

<span data-ttu-id="0c490-106">RSAT のタスク記録を作成する場合は、次の方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="0c490-106">When you author task recordings for RSAT, follow these practices:</span></span>

1. <span data-ttu-id="0c490-107">すべての記録が、メイン ダッシュボードから開始していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0c490-107">Make sure all your recordings start on the main dashboard.</span></span>
2. <span data-ttu-id="0c490-108">個々の記録を短くし、販売注文の作成など、１人のユーザーが実行するビジネス タスクに集中します。</span><span class="sxs-lookup"><span data-stu-id="0c490-108">Keep individual recordings short and focus on a business task performed by one user, like creating a sales order.</span></span> <span data-ttu-id="0c490-109">これにより、テストケースの保守性と再利用性が簡略化されます。</span><span class="sxs-lookup"><span data-stu-id="0c490-109">This simplifies maintainability and reusability of test cases.</span></span>
3. <span data-ttu-id="0c490-110">Chart コントロール はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0c490-110">Chart controls are not supported.</span></span> <span data-ttu-id="0c490-111">チャートに関連するタスク記録アクションは、テストケースの再生中にRSATによって無視されます。</span><span class="sxs-lookup"><span data-stu-id="0c490-111">Any task recording actions related to charts will be ignored by RSAT during test case playback.</span></span>
4. <span data-ttu-id="0c490-112">記録を作成する場合、タブが既に開かれている場合でも、必ずタブ ヘッダーを選択してください。</span><span class="sxs-lookup"><span data-stu-id="0c490-112">When creating a recording, make sure to select a tab header even if the tab is already open.</span></span> <span data-ttu-id="0c490-113">たとえば、別のタブに切り替えてから、必要なタブを再度選択して、そのタブのコントロールを使用する前にアクティブにすることができます。</span><span class="sxs-lookup"><span data-stu-id="0c490-113">For example, you can switch to another tab and then select the needed tab again to activate it before using a control on it.</span></span> <span data-ttu-id="0c490-114">これにより、テストケースの再生中に記録の信頼性を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="0c490-114">This will make your recording more reliable during test case playback.</span></span>
5. <span data-ttu-id="0c490-115">RSATでは、タスク レコーダーで認識されないテスト ステップを再生することはできません。</span><span class="sxs-lookup"><span data-stu-id="0c490-115">RSAT cannot play back any test step that is not recognized by the task recorder.</span></span> <span data-ttu-id="0c490-116">たとえば、テストケースの再生中にローカル ディスクからファイルをアップロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="0c490-116">For example, you cannot upload a file from the local disk during play back of a test case.</span></span>
6. <span data-ttu-id="0c490-117">RSATでは、 **ページ更新** ステップを再生できません。</span><span class="sxs-lookup"><span data-stu-id="0c490-117">RSAT cannot play back a **page refresh** step.</span></span> <span data-ttu-id="0c490-118">テストの記録中にページを更新しないでください。</span><span class="sxs-lookup"><span data-stu-id="0c490-118">Avoid refreshing a page while recording your test.</span></span>

## <a name="best-practices-when-using-the-regression-suite-automation-tool"></a><span data-ttu-id="0c490-119">Regression Suite Automation Tool の使用時のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="0c490-119">Best practices when using the Regression suite automation tool</span></span>

1. <span data-ttu-id="0c490-120">ツールを初めて開いたときに、 **設定** を選択し、必要なすべての設定が揃っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0c490-120">Upon opening the tool for the first time, select **Settings** and ensure that you have all the needed settings.</span></span>
2. <span data-ttu-id="0c490-121">ツールの新しいバージョンをインストールする前に、旧バージョンを終了して、アンインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0c490-121">Before installing a new version of the tool, it is recommended to close and uninstall the previous version.</span></span>
3. <span data-ttu-id="0c490-122">ツールの新しいバージョンをインストールするときに、 **すべて** のテストの実行ファイルを再生成します。</span><span class="sxs-lookup"><span data-stu-id="0c490-122">When you install a new version of the tool, regenerate **all** test execution files.</span></span>

    ![実行ファイル メニュー項目を生成する](media/generate-execution-files.png)

    <span data-ttu-id="0c490-124">パラメータ ファイルの新しい形式で使用できる新しい機能を利用する場合を除いて、 Microsoft Excel パラメータ ファイルを再生成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0c490-124">It is not necessary to regenerate Microsoft Excel parameter files unless you want to take advantage of new features available in a newer format of parameter files.</span></span>

4. <span data-ttu-id="0c490-125">固有値を必要とするテスト パラメーター、たとえば、 **製品受領書** フォームの製品受領書番号や **仕入先請求書** フォームの請求書番号などの場合は、 **RandBetween (a, b)** Excel 関数を使用して、テスト ケースが実行されるたびに一意の番号を生成します。</span><span class="sxs-lookup"><span data-stu-id="0c490-125">For test parameters that need a unique value, for example, the product receipt number in the **Product Receipt** form or the invoice number in the **Vendor Invoice** form, use the **RandBetween(a,b)** Excel function to generate a unique number every time the test case is executed.</span></span>
5. <span data-ttu-id="0c490-126">Excel の既定値は、タスクの記録から取得されます。</span><span class="sxs-lookup"><span data-stu-id="0c490-126">The default values in Excel come from the task recording.</span></span> <span data-ttu-id="0c490-127">保管分析コードや追跡用分析コードなどの **参照グループ** コントロールでは、たとえば、 **SiteWH** の代わりに **2** のように、値の代わりにルックアップのキーを格納します。</span><span class="sxs-lookup"><span data-stu-id="0c490-127">For **Reference Group** controls such as storage dimensions or tracking dimensions, it stores the key of the lookup instead of the value, for example, **2** instead of **SiteWH**.</span></span> <span data-ttu-id="0c490-128">Excelでこれらのフィールドを実際の値で更新して、テストの堅牢性と変更に対する耐性を高めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0c490-128">We recommend that you update these fields with the actual value in Excel so that the test is more robust and resilient to changes.</span></span>
6. <span data-ttu-id="0c490-129">RSAT を実行する前に、環境の **言語** および **日付、時刻、数字の形式** の設定に対して同じロケールを設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0c490-129">It is recommended to set the same locale for **Language** and **Date, time, and number format** settings of your environment prior to running RSAT.</span></span> <span data-ttu-id="0c490-130">これらの値に不整合があると、検証エラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0c490-130">If these values are inconsistent, it may result in validation errors.</span></span>

    ![ロケール、日付、時刻、数字の形式を設定する](media/locale.png)

## <a name="manage-local-recording-files"></a><span data-ttu-id="0c490-132">ローカル記録ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="0c490-132">Manage local recording files</span></span>

<span data-ttu-id="0c490-133">RSATは、Azure DevOpsを使用して、テスト記録ファイル (タスク記録とも呼ばれます) を保存および管理します。</span><span class="sxs-lookup"><span data-stu-id="0c490-133">RSAT relies on Azure DevOps to store and manage test recording files (also known as task recordings).</span></span> <span data-ttu-id="0c490-134">RSAT が Azure DevOps からテスト計画を読み込むと、関連付けられたファイルがローカル コンピューターの現在の **作業ディレクトリ** にダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="0c490-134">When RSAT loads a test plan from Azure DevOps, associated files are downloaded to the current **working directory** on your local computer.</span></span> <span data-ttu-id="0c490-135">(この作業ディレクトリは、RSAT の設定で定義されています。)</span><span class="sxs-lookup"><span data-stu-id="0c490-135">(This working directory is defined in RSAT settings.)</span></span>

<span data-ttu-id="0c490-136">バージョン 1.200.42264.6 以降では、ローカルの記録ファイルの管理が容易になります。</span><span class="sxs-lookup"><span data-stu-id="0c490-136">In version 1.200.42264.6 and later, it's easier to manage local recording files.</span></span> <span data-ttu-id="0c490-137">ビジネス プロセス モデラー (BPM) または Azure DevOps を介さずに、タスク レコーダーで変更を行ってから RSAT を使用して変更をテストできます。</span><span class="sxs-lookup"><span data-stu-id="0c490-137">You can make changes in Task recorder and then use RSAT to test them, without having to go through the Business process modeler (BPM) or Azure DevOps.</span></span> <span data-ttu-id="0c490-138">タスク レコーダーを使用する場合は、記録の作成または変更を終えた後で、開発者の記録として直接ローカル ディスクに保存することができます。</span><span class="sxs-lookup"><span data-stu-id="0c490-138">When you use Task recorder, after you've finished authoring or modifying a recording, you can save it directly to your local disk as a developer recording.</span></span>

![開発者の記録としてタスク記録を保存する](media/rsat-save-as-developer-recording.png)

<span data-ttu-id="0c490-140">テスト ケースに関連付けられている作業ディレクトリの下に記録ファイルを配置します。</span><span class="sxs-lookup"><span data-stu-id="0c490-140">Put the recording file under the working directory that is associated with the test case.</span></span> <span data-ttu-id="0c490-141">たとえば、構成された作業ディレクトリが `C:\Users\<username>\Documents\RSAT` である場合、テスト ケース 1234 の記録ファイルを `C:\Users\<username>\Documents\RSAT\1234\attachments` の下に配置します。</span><span class="sxs-lookup"><span data-stu-id="0c490-141">For example, if your configured working directory is `C:\Users\<username>\Documents\RSAT`, put the recording file for test case 1234 under `C:\Users\<username>\Documents\RSAT\1234\attachments`.</span></span> <span data-ttu-id="0c490-142">開発者の記録ファイルには、**Recording.xml** という名前を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c490-142">You must name the developer recording file **Recording.xml**.</span></span> <span data-ttu-id="0c490-143">または、記録ファイル **-テスト ケース タイトル-.xml** という名前を付けることもできます。**-テスト ケース タイトル-** は Azure DevOps のテスト ケースのタイトルです。</span><span class="sxs-lookup"><span data-stu-id="0c490-143">Alternatively, you can name the recording file **-Test Case Title-.xml**, where **-Test Case Title-** is the title of the test case in Azure DevOps.</span></span>

<span data-ttu-id="0c490-144">次の図は、作業ディレクトリのフォルダー構造の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0c490-144">The following illustration shows an example of a working directory folder structure.</span></span> <span data-ttu-id="0c490-145">フォルダー記号をクリックして、RSAT から直接ディレクトリを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="0c490-145">You can open the directory directly from RSAT by clicking the folder symbol.</span></span>

![作業ディレクトリの例](media/rsat-working-directory-example.png)

<span data-ttu-id="0c490-147">各テスト ケースには独自のフォルダーがあり、テスト ケースの ID に基づいた名前が付けられています。</span><span class="sxs-lookup"><span data-stu-id="0c490-147">Each test case has its own folder, which is named after the ID of the test case.</span></span> <span data-ttu-id="0c490-148">テスト ケースの添付ファイル (記録ファイル、自動化ファイル、および Excel パラメーター ファイル) は、添付ファイル フォルダーにダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="0c490-148">Test case attachments (recording files, automation files, and Excel parameter files) are downloaded into an attachments folder.</span></span> <span data-ttu-id="0c490-149">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="0c490-149">Here is an example.</span></span>

![テスト ケースの添付ファイル](media/rsat-test-case-attachments.png)

<span data-ttu-id="0c490-151">GeneratorLogs ディレクトリには、ログ ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0c490-151">The generatorLogs directory contains log files.</span></span> <span data-ttu-id="0c490-152">ユーザーが変更できるファイルは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="0c490-152">It doesn't contain any files that users can modify.</span></span> <span data-ttu-id="0c490-153">RSAT サポートからログ ファイルの提供を明示的に求められない限り、このディレクトリは無視できます。</span><span class="sxs-lookup"><span data-stu-id="0c490-153">You can ignore this directory unless RSAT support explicitly asks you to provide log files from it.</span></span>

### <a name="commit-a-recording-file-to-azure-devops"></a><span data-ttu-id="0c490-154">記録ファイルを Azure DevOps にコミットする</span><span class="sxs-lookup"><span data-stu-id="0c490-154">Commit a recording file to Azure DevOps</span></span>

<span data-ttu-id="0c490-155">記録がテストされ確定されたら、RSAT を使用してアップロードし、Azure DevOps にコミットします。</span><span class="sxs-lookup"><span data-stu-id="0c490-155">After a recording has been tested and finalized, use RSAT to upload it and commit it to Azure DevOps.</span></span> <span data-ttu-id="0c490-156">アップロード ボタンには 2 つのオプションがあります。 **自動化ファイルのアップロード** および **記録ファイルのアップロード** です。</span><span class="sxs-lookup"><span data-stu-id="0c490-156">The upload button has two options: **Upload automation files** and **Upload recording file**.</span></span> <span data-ttu-id="0c490-157">2 番目のオプションでは、記録ファイルのみが Azure DevOps にアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="0c490-157">The second option uploads only your recording file to Azure DevOps.</span></span>

> [!NOTE]
> <span data-ttu-id="0c490-158">1.200.37255.0 よりも前のバージョンの RSAT を使用していて、最新バージョンにアップグレードする場合は、Azure DevOps からテスト ケースを再読み込みして、適切なディレクトリにダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c490-158">If you're using a version of RSAT that is earlier than 1.200.37255.0, and you upgrade to the latest version, you must reload your test cases from Azure DevOps to download them into the correct directory.</span></span> <span data-ttu-id="0c490-159">それ以外の場合は、RSAT が失敗し、「ファイルが見つかりません」というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0c490-159">Otherwise, RSAT will fail, and you will receive a "File not found" error.</span></span>
>
> <span data-ttu-id="0c490-160">複数の DevOps プロジェクトで作業している場合は、プロジェクトごとに別の作業ディレクトリを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0c490-160">If you're working across several DevOps projects, we recommend that you use a different working directory for each project.</span></span> <span data-ttu-id="0c490-161">そうしないと、複数のプロジェクトの添付ファイルが同じディレクトリ構造に混在してしまう可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0c490-161">Otherwise, attachment files from multiple projects can become commingled in the same directory structure.</span></span>

## <a name="modify-edit-a-task-recording"></a><span data-ttu-id="0c490-162">タスクの記録の変更 (編集)</span><span class="sxs-lookup"><span data-stu-id="0c490-162">Modify (Edit) a Task recording</span></span>

<span data-ttu-id="0c490-163">既存のタスク記録を変更する場合は、これらのベストプラクティスに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0c490-163">If you want to modify an existing task recording, note these best practices.</span></span>

<span data-ttu-id="0c490-164">Web クライアントで、タスク レコーダー ウィンドウを開き、**記録の編集** オプションを使用して記録の編集を開始します。</span><span class="sxs-lookup"><span data-stu-id="0c490-164">In the web client, open the Task recorder pane and start editing the recording using the **Edit Recording** option.</span></span>

![記録の編集オプション](media/edit-recording.png)

<span data-ttu-id="0c490-166">編集が終了したら、クライアントで再生し、すべての手順が正常に動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="0c490-166">When you've finished editing the recording, play it back in the client, and verify that all the steps work correctly.</span></span> <span data-ttu-id="0c490-167">再生が必要です。</span><span class="sxs-lookup"><span data-stu-id="0c490-167">Playback is required.</span></span>

![記録の再生オプション](media/playback-recording.png)

<span data-ttu-id="0c490-169">編集した記録を再生し終わったら、保存します。</span><span class="sxs-lookup"><span data-stu-id="0c490-169">After you've finished playing back an edited recording, save it.</span></span> <span data-ttu-id="0c490-170">これで、RSAT で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0c490-170">It's then ready to be used by RSAT.</span></span>

## <a name="copy-test-cases-in-azure-devops"></a><span data-ttu-id="0c490-171">Azure DevOps でのテスト ケースのコピー </span><span class="sxs-lookup"><span data-stu-id="0c490-171">Copy test cases in Azure DevOps</span></span>

<span data-ttu-id="0c490-172">Azure DevOps でテスト スイートを作成するとき、テスト ケースとその添付ファイルが重複することがよくあります。</span><span class="sxs-lookup"><span data-stu-id="0c490-172">As you are building your test suites in Azure DevOps, it is handy and common to duplicate test cases along with their attachments.</span></span> <span data-ttu-id="0c490-173">コピーしたテスト ケースに既存の Excel パラメーター ファイルが添付されている場合、RSAT では、Excel ファイルを手動で編集することなく、それを実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="0c490-173">If a copied test case contains an existing Excel parameter file attached, RSAT cannot execute it without manual edits to the Excel file.</span></span> <span data-ttu-id="0c490-174">Excel パラメーター ファイルの **テスト ケース ID** は、Azure DevOps テスト ケース ID と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c490-174">The **Test Case ID** in the Excel parameter file must match the Azure DevOps test case ID.</span></span>
<span data-ttu-id="0c490-175">コピーされたすべての Excel パラメーター ファイルを編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c490-175">You will need to edit all copied Excel parameter files.</span></span> <span data-ttu-id="0c490-176">次の図では、Excel ファイルが Azure DevOps のテスト ケース番号 53 に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="0c490-176">In the following image, the Excel file is associated with Test Case number 53 in Azure DevOps.</span></span>

![コピーされたテスト ケースの編集](media/copy-test-cases.png)

<span data-ttu-id="0c490-178">RSAT バージョン 1.210 では、このプロセスが簡単になりました。</span><span class="sxs-lookup"><span data-stu-id="0c490-178">As of RSAT version 1.210, this process is easier.</span></span> <span data-ttu-id="0c490-179">不一致のすべての事例を自動的に修正するには、グリッドで目的のテスト ケースを選択し、**新規** メニューで **テスト ケース ID の不一致を解決** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0c490-179">To automatically fix all occurrences of a mismatch, select the desired test cases in the grid, and then select **Resolve test case ID mismatch** in the **New** menu.</span></span>

![不一致の解決](media/resolve-test-case-id-mismatch.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]