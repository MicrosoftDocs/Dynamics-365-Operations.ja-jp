---
title: Regression Suite Automation Tool ベスト プラクティス
description: このトピックでは、Regression Suite Automation Tool (RSAT)/タスクレコーダーを使用して、クライアントの機能を記録する方法について説明します。
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
ms.openlocfilehash: c7dcafed51fbd841df91728e1e9aa801c4716b44
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570538"
---
# <a name="regression-suite-automation-tool-best-practices"></a><span data-ttu-id="e5f9e-103">Regression Suite Automation Tool ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="e5f9e-103">Regression suite automation tool best practices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5f9e-104">このトピックでは、Regression Suite Automation Tool (RSAT)/タスクレコーダーを使用して、クライアントの機能を記録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-104">This topic describes how to use the Regression suite automation tool (RSAT)/Task recorder to record client functions.</span></span>

## <a name="authoring-test-cases-using-the-task-recorder"></a><span data-ttu-id="e5f9e-105">タスクレコーダーを使用したテストケースの作成</span><span class="sxs-lookup"><span data-stu-id="e5f9e-105">Authoring test cases using the Task recorder</span></span>

1. <span data-ttu-id="e5f9e-106">すべての記録が、メイン ダッシュボードから開始していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-106">Make sure all your recordings start on the main dashboard.</span></span>
2. <span data-ttu-id="e5f9e-107">個々の記録を短くし、販売注文の作成など、１人のユーザーが実行するビジネス タスクに集中します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-107">Keep individual recordings short and focus on a business task performed by one user, like creating a sales order.</span></span> <span data-ttu-id="e5f9e-108">これにより、テストケースの保守性と再利用性が簡略化されます。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-108">This simplifies maintainability and reusability of test cases.</span></span>
3. <span data-ttu-id="e5f9e-109">Chart コントロール はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-109">Chart controls are not supported.</span></span> <span data-ttu-id="e5f9e-110">チャートに関連するタスク記録アクションは、テストケースの再生中にRSATによって無視されます。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-110">Any task recording actions related to charts will be ignored by RSAT during test case playback.</span></span>
4. <span data-ttu-id="e5f9e-111">記録を作成する場合は、タブが既に開かれている場合でも、必ずタブヘッダーを選択してください。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-111">When creating a recording make sure to select a tab header even if the tab is already open.</span></span> <span data-ttu-id="e5f9e-112">たとえば、別のタブに切り替えてから、必要なタブを再度選択して、そのタブのコントロールを使用する前にアクティブにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-112">For example, you can switch to another tab and then select the needed tab again to activate it before using a control on it.</span></span> <span data-ttu-id="e5f9e-113">これにより、テストケースの再生中に記録の信頼性を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-113">This will make your recording more reliable during test case playback.</span></span>
5. <span data-ttu-id="e5f9e-114">RSATでは、タスク レコーダーで認識されないテスト ステップを再生することはできません。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-114">RSAT cannot play back any test step that is not recognized by the task recorder.</span></span> <span data-ttu-id="e5f9e-115">たとえば、テストケースの再生中にローカル ディスクからファイルをアップロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-115">For example, you cannot upload a file from the local disk during play back of a test case.</span></span>
6. <span data-ttu-id="e5f9e-116">RSATでは、 **ページ更新** ステップを再生できません。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-116">RSAT cannot play back a **page refresh** step.</span></span> <span data-ttu-id="e5f9e-117">テストの記録中にページを更新しないでください。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-117">Avoid refreshing a page while recording your test.</span></span>

## <a name="using-the-regression-suite-automation-tool"></a><span data-ttu-id="e5f9e-118">Regression Suite Automation Tool を使用する</span><span class="sxs-lookup"><span data-stu-id="e5f9e-118">Using the Regression suite automation tool</span></span> 

1. <span data-ttu-id="e5f9e-119">ツールを初めて開いたときに、 **設定** を選択し、必要なすべての設定が揃っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-119">Upon opening the tool for the first time, select **Settings** and ensure that you have all the needed settings.</span></span> 
2. <span data-ttu-id="e5f9e-120">ツールの新しいバージョンをインストールする前に、旧バージョンを終了して、アンインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-120">Before installing a new version of the tool, it is recommended to close and uninstall the previous version.</span></span> 
3. <span data-ttu-id="e5f9e-121">ツールの新しいバージョンをインストールするときに、 **すべて** のテストの実行ファイルを再生成します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-121">When you install a new version of the tool, regenerate **all** test execution files.</span></span>
 
    ![実行ファイル メニュー項目を生成する](media/generate-execution-files.png)

    <span data-ttu-id="e5f9e-123">パラメータ ファイルの新しい形式で使用できる新しい機能を利用する場合を除いて、 Microsoft Excel パラメータ ファイルを再生成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-123">It is not necessary to regenerate Microsoft Excel parameter files unless you want to take advantage of new features available in a newer format of parameter files.</span></span>

4. <span data-ttu-id="e5f9e-124">固有値を必要とするテスト パラメーター、たとえば、 **製品受領書** フォームの製品受領書番号や **仕入先請求書** フォームの請求書番号などの場合は、 **RandBetween (a, b)** Excel 関数を使用して、テスト ケースが実行されるたびに一意の番号を生成します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-124">For test parameters that need a unique value, for example, the product receipt number in the **Product Receipt** form or the invoice number in the **Vendor Invoice** form, use the **RandBetween(a,b)** Excel function to generate a unique number every time the test case is executed.</span></span>
5. <span data-ttu-id="e5f9e-125">Excel の既定値は、タスクの記録から取得されます。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-125">The default values in Excel come from the task recording.</span></span> <span data-ttu-id="e5f9e-126">保管分析コードや追跡用分析コードなどの **参照グループ** コントロールでは、たとえば、 **SiteWH** の代わりに **2** のように、値の代わりにルックアップのキーを格納します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-126">For **Reference Group** controls such as storage dimensions or tracking dimensions, it stores the key of the lookup instead of the value, for example, **2** instead of **SiteWH**.</span></span> <span data-ttu-id="e5f9e-127">Excelでこれらのフィールドを実際の値で更新して、テストの堅牢性と変更に対する耐性を高めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-127">We recommend that you update these fields with the actual value in Excel so that the test is more robust and resilient to changes.</span></span>
6. <span data-ttu-id="e5f9e-128">RSAT を実行する前に、環境の**言語**および**日付、時刻、数字の形式**の設定に対して同じロケールを設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-128">It is recommended to set the same locale for **Language** and **Date ,time, and number format** settings of your environment prior to running RSAT.</span></span> <span data-ttu-id="e5f9e-129">これらの値に不整合があると、検証エラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-129">If these values are inconsistent, it may result in validation errors.</span></span>  

  
   ![ロケール、日付、時刻、数字の形式を設定する](media/locale.png)

<span data-ttu-id="e5f9e-131">次に、一般的な使用順序を示します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-131">The following are typical usage sequences.</span></span>

<span data-ttu-id="e5f9e-132">**順序 A: 読み込み > 新規 > 編集 > 実行 > アップロード**</span><span class="sxs-lookup"><span data-stu-id="e5f9e-132">**Sequence A: Load > New > Edit > Run > Upload**</span></span>

1. <span data-ttu-id="e5f9e-133">**読み込み** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-133">Select **Load**.</span></span>
2. <span data-ttu-id="e5f9e-134">テスト ケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-134">Select a test cases.</span></span>
3. <span data-ttu-id="e5f9e-135">パラメーター ファイルがないテスト ケースがある場合は、 **新規** を選択して生成します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-135">If some test cases have no parameter file, select **New** to generate them.</span></span> 
4. <span data-ttu-id="e5f9e-136">オプション: Excel ファイルを編集して、異なるパラメーターでテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-136">Optional: Edit Excel file to run tests with different parameters.</span></span>
5. <span data-ttu-id="e5f9e-137">**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-137">Select **Run**.</span></span>
6. <span data-ttu-id="e5f9e-138">オプション: 実行が正常に終了したら、 **アップロード** を選択して、生成されたすべての自動化ファイル (Excel テスト パラメーター ファイルを含む) を Azure DevOps にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-138">Optional: After a successful run, select **Upload** to upload all generated automation files (including Excel test parameter files) to Azure DevOps.</span></span> 

<span data-ttu-id="e5f9e-139">**順序 B: 読み込み > 編集 > 実行 > アップロード**</span><span class="sxs-lookup"><span data-stu-id="e5f9e-139">**Sequence B: Load > Edit > Run > Upload**</span></span>

1. <span data-ttu-id="e5f9e-140">**読み込み** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-140">Select **Load**.</span></span> <span data-ttu-id="e5f9e-141">すべてのパラメーター ファイルが既に存在する場合、 **新規** を選択して再生成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-141">If all parameter files already exist, you do not need to select **New** to regenerate them.</span></span>
2. <span data-ttu-id="e5f9e-142">オプション: Excel ファイルを編集して、異なるパラメーターでテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-142">Optional: Edit Excel file to run tests with different parameters.</span></span>
3. <span data-ttu-id="e5f9e-143">**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-143">Select **Run**.</span></span>
4. <span data-ttu-id="e5f9e-144">オプション: 実行が正常に終了したら、 **アップロード** を選択して、生成されたすべての自動化ファイル (Excel テスト パラメーター ファイルを含む) を Azure DevOps にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-144">Optional: After a successful run, select **Upload** to upload all generated automation files (including Excel test parameter files) to Azure DevOps.</span></span> 

<span data-ttu-id="e5f9e-145">**順序 C: 読み込み > 新規 (すべてのテスト ケース用) > 実行 > アップロード**</span><span class="sxs-lookup"><span data-stu-id="e5f9e-145">**Sequence C: Load > New (for all test cases) > Run > Upload**</span></span>

<span data-ttu-id="e5f9e-146">この手順は、ツールの新しいバージョンをインストールした後にお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-146">This sequence is recommended after installing a new version of the tool.</span></span> 

1. <span data-ttu-id="e5f9e-147">**読み込み** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-147">Select **Load**.</span></span> 
2. <span data-ttu-id="e5f9e-148">テスト計画内のすべてのテスト ケースを選択し、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-148">Select all test cases in the test plan and select **New**.</span></span>
3. <span data-ttu-id="e5f9e-149">Excel パラメーター ファイルを編集します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-149">Edit Excel parameter files.</span></span>
4. <span data-ttu-id="e5f9e-150">**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-150">Select **Run**.</span></span>
5. <span data-ttu-id="e5f9e-151">正常に実行されたら、 **アップロード** を選択して、 Azure DevOps にすべての生成されたテスト コンポーネントをにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-151">After a successful run, select **Upload** to upload all generated test artifacts to Azure DevOps.</span></span> 

## <a name="how-to-modify-a-task-recording"></a><span data-ttu-id="e5f9e-152">タスクの記録を変更する方法</span><span class="sxs-lookup"><span data-stu-id="e5f9e-152">How to modify a Task recording</span></span>

<span data-ttu-id="e5f9e-153">既存のタスク記録を変更する場合は、これらのベストプラクティスに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-153">If you want to modify an existing task recording, note these best practices.</span></span> 

<span data-ttu-id="e5f9e-154">Web クライアントで、タスク レコーダー ウィンドウを開き、**記録の編集**オプションを使用して記録の編集を開始します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-154">In the web client, open the Task recorder pane and start editing the recording using the **Edit Recording** option.</span></span>

![記録の編集オプション](media/edit-recording.png)
  
<span data-ttu-id="e5f9e-156">編集が終了したら、記録を保存またはダウンロードしてからクライアントで再生し、すべての手順が正常に動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-156">When you finish editing, save or download the recording, then play it back in the client and verify that all the steps work correctly.</span></span>

![記録の再生オプション](media/playback-recording.png)
 
<span data-ttu-id="e5f9e-158">編集した記録を再生した後、保存します。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-158">After playing back an edited recording, save it.</span></span> <span data-ttu-id="e5f9e-159">これで、RSATで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e5f9e-159">It is then ready to be used by RSAT.</span></span>

