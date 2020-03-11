---
title: Regression Suite Automation Tool チュートリアルの使用
description: このトピックでは、Regression Suite Automation Tool (RSAT) の使用方法について説明します。 さまざまな機能について説明し、高度なスクリプトを使用した例を示します。
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070823"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="5439b-104">Regression Suite Automation Tool チュートリアルの使用</span><span class="sxs-lookup"><span data-stu-id="5439b-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="5439b-105">インターネット ブラウザーのツールを使用して、このページを PDF 形式でダウンロードして保存します。</span><span class="sxs-lookup"><span data-stu-id="5439b-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="5439b-106">このチュートリアルでは、デモの割り当て、戦略と重要な学習ポイントの説明を含む Regression Suite Automation Tool (RSAT) の高度な機能をいくつかを説明します。</span><span class="sxs-lookup"><span data-stu-id="5439b-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="5439b-107">RSAT/タスクレコーダーの機能</span><span class="sxs-lookup"><span data-stu-id="5439b-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="5439b-108">フィールド値を検証する</span><span class="sxs-lookup"><span data-stu-id="5439b-108">Validate a field value</span></span>

<span data-ttu-id="5439b-109">この機能の詳細については、[検証機能を持つ新しいタスク記録を作成する](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5439b-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="5439b-110">保存された変数</span><span class="sxs-lookup"><span data-stu-id="5439b-110">Saved variable</span></span>

<span data-ttu-id="5439b-111">この機能の詳細については、[既存のタスク記録を変更して保存された変数を作成する](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5439b-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="5439b-112">派生テスト ケース</span><span class="sxs-lookup"><span data-stu-id="5439b-112">Derived test case</span></span>

1. <span data-ttu-id="5439b-113">Regression Suite Automation Tool (RSAT) を開き、[Regression Suite Automation Tool チュートリアルのセットアップおよびインストール](./hol-set-up-regression-suite-automation-tool.md) で作成した両方のテストケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="5439b-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="5439b-114">**新規 \> 派生テストケースの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5439b-114">Select **New \> Create derived test case**.</span></span>

    ![新しいメニューで、派生テスト ケース コマンドを作成する](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="5439b-116">現在のテスト スイートで選択した各テスト ケースに対して派生テスト ケースが作成され、各派生テスト ケースに Excel パラメーター ファイルの独自のコピーがあることを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="5439b-117">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5439b-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5439b-118">派生テスト ケースを実行すると、親テスト ケースと独自の Excel パラメーター ファイルのタスク記録が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="5439b-119">この方法で、複数のタスク記録を管理することなく、異なるパラメーターを使用して同じテストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="5439b-120">派生テスト ケースは、親テスト ケースと同じテスト スイートの一部である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5439b-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![メッセージ ボックス](./media/use_rsa_tool_02.png)

    <span data-ttu-id="5439b-122">さらに 2 つの派生テスト ケースが作成され、**派生?** チェック ボックスがオンになっています。</span><span class="sxs-lookup"><span data-stu-id="5439b-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![派生テスト ケースが作成されました](./media/use_rsa_tool_03.png)

    <span data-ttu-id="5439b-124">派生テスト ケースは、自動的に Azure DevOps に作成されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="5439b-125">これは、特別なキーワード **RSAT: DerivedTestSteps** でタグ付けされた**新しい製品の作成**テスト ケースの子品目です。</span><span class="sxs-lookup"><span data-stu-id="5439b-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="5439b-126">これらのテスト ケースは、Azure DevOps テスト計画にも自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![RSAT: DerivedTestSteps キーワード](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="5439b-128">何らかの理由で、派生したテスト ケースが正しい順序になっていない場合は Azure DevOps に移動し、RSAT が適切な順序で実行できるように、テスト スイート内のテスト ケース順序を変更します。</span><span class="sxs-lookup"><span data-stu-id="5439b-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="5439b-129">派生テスト ケースを選択し、**編集**を選択して対応する Excel パラメーター ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="5439b-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="5439b-130">これらの Excel パラメーター ファイルは、親ファイルを編集したときと同じ方法で編集します。</span><span class="sxs-lookup"><span data-stu-id="5439b-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="5439b-131">つまり、製品 ID が自動的に生成されるように設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5439b-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="5439b-132">また、保存された変数が関連するフィールドにコピーされていることも確認します。</span><span class="sxs-lookup"><span data-stu-id="5439b-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="5439b-133">両方の Excel パラメーター ファイルの**一般**タブで、**会社**フィールドの値を **USSI** に更新して、派生テスト ケースが親テスト ケースとは別の法人に対して実行されるようにします。</span><span class="sxs-lookup"><span data-stu-id="5439b-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="5439b-134">特定のユーザー (または特定のユーザーに関連付けられているロール) に対してテスト ケースを実行するには、**テスト ユーザー** フィールドの値を更新します。</span><span class="sxs-lookup"><span data-stu-id="5439b-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="5439b-135">**実行**を選択し、USMF 法人と USSI 法人の両方で製品が作成されていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="5439b-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="5439b-136">通知の検証</span><span class="sxs-lookup"><span data-stu-id="5439b-136">Validate notifications</span></span>

<span data-ttu-id="5439b-137">この機能は、アクションが実行されたかどうかを検証するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="5439b-138">たとえば、製造オーダーが作成、見積り、開始された時に、アプリは製造オーダーが開始されたことを通知する "生産 – 開始" メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="5439b-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![生産 – 開始通知](./media/use_rsa_tool_05.png)

<span data-ttu-id="5439b-140">RSAT を使用してこのメッセージを検証するには、該当する記録の Excel パラメーター ファイルにある**メッセージ検証**タブにメッセージ テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="5439b-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![メッセージ検証タブ](./media/use_rsa_tool_06.png)

<span data-ttu-id="5439b-142">テスト ケースを実行すると、Excel パラメーター ファイル内のメッセージが、表示されるメッセージと比較されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="5439b-143">メッセージが一致しない場合、テストケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="5439b-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="5439b-144">Excel パラメーター ファイルの**メッセージ検証**タブには、複数のメッセージを入力できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="5439b-145">メッセージは、情報メッセージではなく、エラーまたは警告メッセージである場合もあります。</span><span class="sxs-lookup"><span data-stu-id="5439b-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="5439b-146">演算子を使用して値を検証する</span><span class="sxs-lookup"><span data-stu-id="5439b-146">Validate values by using operators</span></span>

<span data-ttu-id="5439b-147">RSAT の以前のバージョンでは、予測値がコントロール値と等しい場合にのみ値を検証できました。</span><span class="sxs-lookup"><span data-stu-id="5439b-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="5439b-148">この新しい機能を使用すると、変数が指定された値と等しくない、指定された値より小さい、またはそれを超えていることを検証できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="5439b-149">この機能を使用するには、RSAT のインストールホルダー (たとえば、**C:\\Program Files (x86)\\Regression Suite Automation Tool**) にある **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ファイルを開き、次の要素の値を **False** から **True** に変更します。</span><span class="sxs-lookup"><span data-stu-id="5439b-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="5439b-150">Excel パラメーター ファイルで、新しい**演算子**フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5439b-151">古いバージョンの RSAT を使用している場合は、新しい Excel パラメーター ファイルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![演算子フィールド](./media/use_rsa_tool_07.png)

<span data-ttu-id="5439b-153">次の例は、この機能を使用して、手持在庫が 0 (ゼロ) よりも大きいかどうかを検証する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5439b-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="5439b-154">**USMF** 会社のデモデータで、次の手順を含むタスク記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="5439b-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="5439b-155">**製品管理情報 \> 製品 \> リリースされた製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5439b-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="5439b-156">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="5439b-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5439b-157">たとえば、**1000** という値で**品目番号**フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="5439b-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="5439b-158">**手持在庫**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5439b-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="5439b-159">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="5439b-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5439b-160">たとえば、**1** という値で**サイト** フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="5439b-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="5439b-161">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="5439b-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="5439b-162">**引当可能合計数**フィールドの値が、**411.0000000000000000** であることを検証します。</span><span class="sxs-lookup"><span data-stu-id="5439b-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="5439b-163">タスク記録を LCS の BPM ライブラリに保存し、Azure DevOps に同期させます。</span><span class="sxs-lookup"><span data-stu-id="5439b-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="5439b-164">テスト ケースをテスト計画に追加し、テスト ケースを RSAT に読み込みます。</span><span class="sxs-lookup"><span data-stu-id="5439b-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="5439b-165">Excel パラメーター ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="5439b-165">Open the Excel parameter file.</span></span> <span data-ttu-id="5439b-166">**手持ち在庫品目**タブに、**演算子**フィールドを含む**手持ち在庫品目検証**セクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![演算子フィールド](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="5439b-168">手持在庫が常に 0 より大きいかどうかを検証するには、**値**フィールドの値を **411** から **0** に、および**演算子**フィールドの値を等号 (**=**) から大なり記号 (**\>**) に変更します。</span><span class="sxs-lookup"><span data-stu-id="5439b-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![値と演算子フィールドの値が変更されました](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="5439b-170">Excel パラメーター ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="5439b-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="5439b-171">**アップロード**を選択し、Excel パラメーター ファイルに加えた変更を Azure DevOps に保存します。</span><span class="sxs-lookup"><span data-stu-id="5439b-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="5439b-172">これで、指定した在庫品目の**引当可能合計数**フィールド値が0 ( ゼロ ) よりも大きい場合、実際の手持在庫値に関係なくテストが合格となります。</span><span class="sxs-lookup"><span data-stu-id="5439b-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="5439b-173">ジェネレーター ログ</span><span class="sxs-lookup"><span data-stu-id="5439b-173">Generator logs</span></span>

<span data-ttu-id="5439b-174">この機能は、実行されたテスト ケースのログを含むフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="5439b-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="5439b-175">この機能を使用するには、RSAT のインストールホルダー (たとえば、**C:\\Program Files (x86)\\Regression Suite Automation Tool**) にある **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ファイルを開き、次の要素の値を **False** から **True** に変更します。</span><span class="sxs-lookup"><span data-stu-id="5439b-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="5439b-176">テスト ケースが実行されると、**C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**でログファイルを検索できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![ジェネレーター ログ フォルダー](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="5439b-178">構成ファイルの値を変更する前に既存のテスト ケースがあった場合、新しいテスト実行ファイルを生成するまで、そのテスト ケースに対するログは生成されません。</span><span class="sxs-lookup"><span data-stu-id="5439b-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![新しいメニューにテキスト実行ファイルのみのコマンドを生成します。](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="5439b-180">スナップショット</span><span class="sxs-lookup"><span data-stu-id="5439b-180">Snapshot</span></span>

<span data-ttu-id="5439b-181">この機能は、タスク記録中に実行された手順のスクリーンショットを撮ります。</span><span class="sxs-lookup"><span data-stu-id="5439b-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="5439b-182">この機能を使用するには、RSAT のインストール フォルダー (たとえば、**C:\\Program Files (x86)\\Regression Suite Automation Tool**) にある **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ファイルを開き、次の要素の値を **False** から **True** に変更します。</span><span class="sxs-lookup"><span data-stu-id="5439b-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="5439b-183">**C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** では、実行される各テスト ケースに対して個別のフォルダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![テスト ケースのスナップショット フォルダー](./media/use_rsa_tool_12.png)

<span data-ttu-id="5439b-185">これらの各フォルダー内で、テスト ケースの実行中に実行された手順のスナップショットを検索できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![スナップショット ファイル](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="5439b-187">割り当て</span><span class="sxs-lookup"><span data-stu-id="5439b-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="5439b-188">シナリオ</span><span class="sxs-lookup"><span data-stu-id="5439b-188">Scenario</span></span>

1. <span data-ttu-id="5439b-189">製品デザイナーが新しくリリースされた製品を作成します。</span><span class="sxs-lookup"><span data-stu-id="5439b-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="5439b-190">生産マネージャは、在庫レベルを 2 個にするために製造オーダーを開始します。</span><span class="sxs-lookup"><span data-stu-id="5439b-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="5439b-191">製造は、製造オーダーを開始および終了し、手持在庫数量が 2 個であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5439b-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="5439b-192">販売チームは、新しい製品 4 個 の注文を受けます。</span><span class="sxs-lookup"><span data-stu-id="5439b-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="5439b-193">したがって、販売チームは動的計画を使って正味必要量を更新します。</span><span class="sxs-lookup"><span data-stu-id="5439b-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="5439b-194">追加の利用可能容量がないので、既定の注文ポリシーは "作成ではなく購入" に設定されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="5439b-195">したがって、計画発注書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="5439b-196">購入者は、仕入先を追加し、計画発注書を確定してから、発注書を確認します。</span><span class="sxs-lookup"><span data-stu-id="5439b-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="5439b-197">購入した商品が店舗に到着すると、店舗オペレーターが関連する発注書を検索して商品を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="5439b-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="5439b-198">注文が完了したため、販売注文に対して商品をピッキングおよび梱包することができます。</span><span class="sxs-lookup"><span data-stu-id="5439b-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="5439b-199">財務は、仕入請求書および売上請求書に転記します。</span><span class="sxs-lookup"><span data-stu-id="5439b-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="5439b-200">次の図は、このシナリオのフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="5439b-200">The following illustration shows the flow for this scenario.</span></span>

![デモ シナリオのフロー](./media/use_rsa_tool_14.png)

<span data-ttu-id="5439b-202">次の図は、RSAT のこのシナリオの業務プロセスを示しています。</span><span class="sxs-lookup"><span data-stu-id="5439b-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![デモ シナリオの業務プロセス](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="5439b-204">戦略 – キー学習</span><span class="sxs-lookup"><span data-stu-id="5439b-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="5439b-205">データ</span><span class="sxs-lookup"><span data-stu-id="5439b-205">Data</span></span>

- <span data-ttu-id="5439b-206">代表的なデータボリューム (生産のコピー/高品質の構成データと移行されたデータ) があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5439b-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="5439b-207">タスク レコーダーを介して新しいデータを生成する場合は、既存の名前と競合しないテスト名 (例えば、**RSATxxx** などの接頭語を使用するなど) を作成します。</span><span class="sxs-lookup"><span data-stu-id="5439b-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="5439b-208">Azure ポイントインタイム復元を使用して、第 1 層環境以外でテストを再実行します。</span><span class="sxs-lookup"><span data-stu-id="5439b-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="5439b-209">Excel 関数の **RANDOM** や **NOW** を使用して、独自の組み合わせを生成することはできますが、その作業量は大幅に多くなります。</span><span class="sxs-lookup"><span data-stu-id="5439b-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="5439b-210">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="5439b-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="5439b-211">タスク レコーダー</span><span class="sxs-lookup"><span data-stu-id="5439b-211">Task recorder</span></span>

- <span data-ttu-id="5439b-212">記録を開始する前にシナリオを定義します。</span><span class="sxs-lookup"><span data-stu-id="5439b-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="5439b-213">適切に管理されたプロジェクトには、事前定義済みのテスト シナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="5439b-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="5439b-214">テスト ケースを構築するには、それらのテスト シナリオの結果がどの程度予測可能かを考慮します。</span><span class="sxs-lookup"><span data-stu-id="5439b-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="5439b-215">異なるロールによって実行される場合、または待機時間がある場合、または次のステップの前に外部イベントがある場合に、記録を分割します。</span><span class="sxs-lookup"><span data-stu-id="5439b-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="5439b-216">リストから値を選択することは避けてください。</span><span class="sxs-lookup"><span data-stu-id="5439b-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="5439b-217">代わりに、**FIFO**、**AudioRM**、**SiteWH** などのテキスト形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="5439b-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="5439b-218">リスト内で選択した場合は、値自体ではなく、リスト内の値の位置が記録されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="5439b-219">このリストに品目を追加すると、値の位置が変わる場合があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="5439b-220">したがって、記録では別のパラメーターが使用され、その他のシナリオが影響を受ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="5439b-221">マルチ ユーザーの動作について考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="5439b-221">Think about multi-user behavior.</span></span> <span data-ttu-id="5439b-222">たとえば、新しく作成された販売注文が常に自動的に選択されるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="5439b-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="5439b-223">代わりに、常にフィルターを使用して正しい注文を見つけます。</span><span class="sxs-lookup"><span data-stu-id="5439b-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="5439b-224">連鎖したテスト ケースで使用できるように、タスク レコーダーのコピー機能を使用して、新しく作成された製品の名前を保存します。</span><span class="sxs-lookup"><span data-stu-id="5439b-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="5439b-225">タスク レコーダーの検証機能を使用して、ステップが正常に実行されたことを確認するチェックポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="5439b-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="5439b-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="5439b-226">RSAT</span></span>

- <span data-ttu-id="5439b-227">別の会社でテストを実行するには、Excel パラメーター ファイルの**一般**タブで会社を変更します。</span><span class="sxs-lookup"><span data-stu-id="5439b-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="5439b-228">設定およびデータが、新しく選択した会社で使用可能であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5439b-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="5439b-229">テスト ユーザーは、Excel パラメーター ファイルの**一般**タブで変更できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="5439b-230">テスト ケースを実行するユーザーの電子メール ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="5439b-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="5439b-231">この方法で、指定したユーザーのセキュリティ アクセス許可を使用し、テスト ケースを実行できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="5439b-232">テストが開始されるまで待機するには、Excel パラメーター ファイルの**一般**タブで一時停止を定義します。</span><span class="sxs-lookup"><span data-stu-id="5439b-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="5439b-233">この一時停止は、バッチ ジョブで使用できます (たとえば、次のステップを実行する前にワークフローを実行する必要がある場合など)。</span><span class="sxs-lookup"><span data-stu-id="5439b-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="5439b-234">高度なスクリプト</span><span class="sxs-lookup"><span data-stu-id="5439b-234">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="5439b-235">CLI</span><span class="sxs-lookup"><span data-stu-id="5439b-235">CLI</span></span>

<span data-ttu-id="5439b-236">RSAT は、**コマンド プロンプト**または **PowerShell** ウィンドウから呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="5439b-236">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="5439b-237">**TestRoot** 環境変数が RSAT インストール パスに設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5439b-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="5439b-238">(Microsoft Windows の**コントロール パネル**を開き、**システムとセキュリティ\>システム\>高度なシステム設定**を選択し、**環境変数**を選択します。)</span><span class="sxs-lookup"><span data-stu-id="5439b-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="5439b-239">**コマンド プロンプト**または **PowerShell** ウィンドウを管理者として開きます。</span><span class="sxs-lookup"><span data-stu-id="5439b-239">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="5439b-240">RSAT インストール ディレクトリに移動します。</span><span class="sxs-lookup"><span data-stu-id="5439b-240">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="5439b-241">すべてのコマンドのリスト</span><span class="sxs-lookup"><span data-stu-id="5439b-241">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="5439b-242">?</span><span class="sxs-lookup"><span data-stu-id="5439b-242">?</span></span> 
<span data-ttu-id="5439b-243">使用可能なすべてのコマンドとそのパラメーターに関するヘルプを表示します。</span><span class="sxs-lookup"><span data-stu-id="5439b-243">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="5439b-244">オプションのパラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-244">Optional parameters</span></span>

**``command``**


<span data-ttu-id="5439b-245">ここで、``[command]`` は以下で指定されたコマンドの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="5439b-245">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="5439b-246">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="5439b-246">about</span></span>
<span data-ttu-id="5439b-247">現在のバージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="5439b-247">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="5439b-248">cls</span><span class="sxs-lookup"><span data-stu-id="5439b-248">cls</span></span>
<span data-ttu-id="5439b-249">画面をクリアします。</span><span class="sxs-lookup"><span data-stu-id="5439b-249">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="5439b-250">ダウンロード</span><span class="sxs-lookup"><span data-stu-id="5439b-250">download</span></span>
<span data-ttu-id="5439b-251">指定したテスト ケースの添付ファイルを出力ディレクトリにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="5439b-251">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="5439b-252">``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-252">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="5439b-253">最初の列の値を **test_case_id** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="5439b-253">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-254">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-254">Required parameters</span></span>
<span data-ttu-id="5439b-255">**``test_case_id``** テスト ケース ID を表します。</span><span class="sxs-lookup"><span data-stu-id="5439b-255">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="5439b-256">**``output_dir``** 出力ディレクトリを表します。</span><span class="sxs-lookup"><span data-stu-id="5439b-256">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="5439b-257">このディレクトリが存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-257">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="5439b-258">例</span><span class="sxs-lookup"><span data-stu-id="5439b-258">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="5439b-259">編集</span><span class="sxs-lookup"><span data-stu-id="5439b-259">edit</span></span>
<span data-ttu-id="5439b-260">Excel プログラムでパラメーター ファイルを開いて編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5439b-260">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-261">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-261">Required parameters</span></span>
<span data-ttu-id="5439b-262">**``excel_file``** 既存の Excel ファイルへの完全なパスが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-262">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="5439b-263">例</span><span class="sxs-lookup"><span data-stu-id="5439b-263">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="5439b-264">作成</span><span class="sxs-lookup"><span data-stu-id="5439b-264">generate</span></span>
<span data-ttu-id="5439b-265">指定されたテスト ケースのテスト実行およびパラメーター ファイルを出力ディレクトリに生成します。</span><span class="sxs-lookup"><span data-stu-id="5439b-265">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="5439b-266">``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-266">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="5439b-267">最初の列の値を **test_case_id** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="5439b-267">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-268">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-268">Required parameters</span></span>
<span data-ttu-id="5439b-269">**``test_case_id``** テスト ケース ID を表します。</span><span class="sxs-lookup"><span data-stu-id="5439b-269">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="5439b-270">**``output_dir``** 出力ディレクトリを表します。</span><span class="sxs-lookup"><span data-stu-id="5439b-270">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="5439b-271">このディレクトリが存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-271">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="5439b-272">例</span><span class="sxs-lookup"><span data-stu-id="5439b-272">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="5439b-273">generatederived</span><span class="sxs-lookup"><span data-stu-id="5439b-273">generatederived</span></span>
<span data-ttu-id="5439b-274">指定されたテスト ケースから派生する新しいテスト ケースを生成します。</span><span class="sxs-lookup"><span data-stu-id="5439b-274">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="5439b-275">``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-275">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="5439b-276">最初の列の値を **test_case_id** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="5439b-276">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-277">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-277">Required parameters</span></span>
<span data-ttu-id="5439b-278">**``parent_test_case_id``** 親テスト ケース ID を表します。</span><span class="sxs-lookup"><span data-stu-id="5439b-278">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="5439b-279">**``test_plan_id``** テスト計画 ID を表します。</span><span class="sxs-lookup"><span data-stu-id="5439b-279">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="5439b-280">**``test_suite_id``** テスト スイート ID を表します。</span><span class="sxs-lookup"><span data-stu-id="5439b-280">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="5439b-281">例</span><span class="sxs-lookup"><span data-stu-id="5439b-281">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="5439b-282">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="5439b-282">generatetestonly</span></span>
<span data-ttu-id="5439b-283">指定されたテスト ケースのテスト実行ファイルのみを出力ディレクトリに生成します。</span><span class="sxs-lookup"><span data-stu-id="5439b-283">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="5439b-284">``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-284">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="5439b-285">最初の列の値を **test_case_id** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="5439b-285">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-286">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-286">Required parameters</span></span>
<span data-ttu-id="5439b-287">**``test_case_id``** テスト ケース ID を表します。</span><span class="sxs-lookup"><span data-stu-id="5439b-287">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="5439b-288">**``output_dir``** 出力ディレクトリを表します。</span><span class="sxs-lookup"><span data-stu-id="5439b-288">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="5439b-289">このディレクトリが存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-289">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="5439b-290">例</span><span class="sxs-lookup"><span data-stu-id="5439b-290">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="5439b-291">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="5439b-291">generatetestsuite</span></span>
<span data-ttu-id="5439b-292">指定されたスイートのすべてのテスト ケースを出力ディレクトリに生成します。</span><span class="sxs-lookup"><span data-stu-id="5439b-292">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="5439b-293">``listtestsuitenames`` コマンドを使用すると、使用可能なすべてのテスト スイートを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-293">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="5439b-294">最初の列の値を **test_suite_name** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="5439b-294">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-295">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-295">Required parameters</span></span>
<span data-ttu-id="5439b-296">**``test_suite_name``** テスト スイートの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="5439b-296">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="5439b-297">**``output_dir``** 出力ディレクトリを表します。</span><span class="sxs-lookup"><span data-stu-id="5439b-297">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="5439b-298">このディレクトリが存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-298">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="5439b-299">例</span><span class="sxs-lookup"><span data-stu-id="5439b-299">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="5439b-300">ヘルプ</span><span class="sxs-lookup"><span data-stu-id="5439b-300">help</span></span>
<span data-ttu-id="5439b-301">[?](####?) と同一</span><span class="sxs-lookup"><span data-stu-id="5439b-301">Identical to the [?](####?)</span></span> <span data-ttu-id="5439b-302">command</span><span class="sxs-lookup"><span data-stu-id="5439b-302">command</span></span>


#### <a name="list"></a><span data-ttu-id="5439b-303">リスト</span><span class="sxs-lookup"><span data-stu-id="5439b-303">list</span></span>
<span data-ttu-id="5439b-304">使用可能なすべてのテスト ケースを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="5439b-304">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="5439b-305">listtestplans</span><span class="sxs-lookup"><span data-stu-id="5439b-305">listtestplans</span></span>
<span data-ttu-id="5439b-306">使用可能なすべてのテスト計画を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="5439b-306">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="5439b-307">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="5439b-307">listtestsuite</span></span>
<span data-ttu-id="5439b-308">指定されたテスト スイートのテスト ケースを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="5439b-308">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="5439b-309">``listtestsuitenames`` コマンドを使用すると、使用可能なすべてのテスト スイートを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="5439b-310">最初の列の値を **suite_name** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="5439b-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-311">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-311">Required parameters</span></span>
<span data-ttu-id="5439b-312">**``suite_name``** 目的のスイートの名前。</span><span class="sxs-lookup"><span data-stu-id="5439b-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="5439b-313">例</span><span class="sxs-lookup"><span data-stu-id="5439b-313">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="5439b-314">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="5439b-314">listtestsuitenames</span></span>
<span data-ttu-id="5439b-315">使用可能なすべてのテスト スイートを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="5439b-315">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="5439b-316">playback</span><span class="sxs-lookup"><span data-stu-id="5439b-316">playback</span></span>
<span data-ttu-id="5439b-317">Excel ファイルを使用してテスト ケースを再生します。</span><span class="sxs-lookup"><span data-stu-id="5439b-317">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-318">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-318">Required parameters</span></span>
<span data-ttu-id="5439b-319">**``excel_file``** Excel ファイルへの完全なパス。</span><span class="sxs-lookup"><span data-stu-id="5439b-319">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="5439b-320">ファイルが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-320">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="5439b-321">例</span><span class="sxs-lookup"><span data-stu-id="5439b-321">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="5439b-322">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="5439b-322">playbackbyid</span></span>
<span data-ttu-id="5439b-323">同時に複数のテスト ケースを再生します。</span><span class="sxs-lookup"><span data-stu-id="5439b-323">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="5439b-324">``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-324">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="5439b-325">最初の列の値を **test_case_id** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="5439b-325">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-326">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-326">Required parameters</span></span>
<span data-ttu-id="5439b-327">**``test_case_id1``** 既存のテスト ケースの ID。</span><span class="sxs-lookup"><span data-stu-id="5439b-327">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="5439b-328">**``test_case_id2``** 既存のテスト ケースの ID。</span><span class="sxs-lookup"><span data-stu-id="5439b-328">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="5439b-329">**``test_case_idN``** 既存のテスト ケースの ID。</span><span class="sxs-lookup"><span data-stu-id="5439b-329">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="5439b-330">例</span><span class="sxs-lookup"><span data-stu-id="5439b-330">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="5439b-331">playbackmany</span><span class="sxs-lookup"><span data-stu-id="5439b-331">playbackmany</span></span>
<span data-ttu-id="5439b-332">Excel ファイルを使用して、同時に多数のテスト ケースを再生します。</span><span class="sxs-lookup"><span data-stu-id="5439b-332">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-333">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-333">Required parameters</span></span>
<span data-ttu-id="5439b-334">**``excel_file1``** Excel ファイルへの完全なパス。</span><span class="sxs-lookup"><span data-stu-id="5439b-334">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="5439b-335">ファイルが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-335">File must exist.</span></span>  
<span data-ttu-id="5439b-336">**``excel_file2``** Excel ファイルへの完全なパス。</span><span class="sxs-lookup"><span data-stu-id="5439b-336">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="5439b-337">ファイルが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-337">File must exist.</span></span>  
<span data-ttu-id="5439b-338">**``excel_fileN``** Excel ファイルへの完全なパス。</span><span class="sxs-lookup"><span data-stu-id="5439b-338">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="5439b-339">ファイルが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5439b-339">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="5439b-340">例</span><span class="sxs-lookup"><span data-stu-id="5439b-340">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="5439b-341">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="5439b-341">playbacksuite</span></span>
<span data-ttu-id="5439b-342">指定されたテスト スイートからすべてのテスト ケースを再生します。</span><span class="sxs-lookup"><span data-stu-id="5439b-342">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="5439b-343">``listtestsuitenames`` コマンドを使用すると、使用可能なすべてのテスト スイートを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-343">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="5439b-344">最初の列の値を **suite_name** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="5439b-344">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-345">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-345">Required parameters</span></span>
<span data-ttu-id="5439b-346">**``suite_name``** 目的のスイートの名前。</span><span class="sxs-lookup"><span data-stu-id="5439b-346">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="5439b-347">例</span><span class="sxs-lookup"><span data-stu-id="5439b-347">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="5439b-348">quit</span><span class="sxs-lookup"><span data-stu-id="5439b-348">quit</span></span>
<span data-ttu-id="5439b-349">アプリケーションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5439b-349">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="5439b-350">アップロード</span><span class="sxs-lookup"><span data-stu-id="5439b-350">upload</span></span>
<span data-ttu-id="5439b-351">指定されたテスト スイートまたはテスト ケースに属するすべてのファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="5439b-351">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="5439b-352">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-352">Required parameters</span></span>
<span data-ttu-id="5439b-353">**``suite_name``** 指定されたテスト スイートに属するすべてのファイルがアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="5439b-353">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="5439b-354">**``testcase_id``** 指定されたテスト ケースに属するすべてのファイルがアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="5439b-354">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="5439b-355">例</span><span class="sxs-lookup"><span data-stu-id="5439b-355">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="5439b-356">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="5439b-356">uploadrecording</span></span>
<span data-ttu-id="5439b-357">指定されたテスト ケースに属する記録ファイルのみをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="5439b-357">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="5439b-358">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="5439b-358">Required parameters</span></span>
<span data-ttu-id="5439b-359">**``testcase_id``** 指定されたテスト ケースに属する記録ファイルがアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="5439b-359">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="5439b-360">例</span><span class="sxs-lookup"><span data-stu-id="5439b-360">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="5439b-361">使用</span><span class="sxs-lookup"><span data-stu-id="5439b-361">usage</span></span>
<span data-ttu-id="5439b-362">このアプリケーションを呼び出す 2 つの方法を示します。1 つは既定の設定ファイルを使用する方法、もう 1 つは設定ファイルを提供する方法です。</span><span class="sxs-lookup"><span data-stu-id="5439b-362">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="5439b-363">Windows PowerShell の例</span><span class="sxs-lookup"><span data-stu-id="5439b-363">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="5439b-364">ループでのテスト ケースの実行</span><span class="sxs-lookup"><span data-stu-id="5439b-364">Run a test case in a loop</span></span>

<span data-ttu-id="5439b-365">新しい顧客を作成するテスト スクリプトがあります。</span><span class="sxs-lookup"><span data-stu-id="5439b-365">You have a test script that creates a new customer.</span></span> <span data-ttu-id="5439b-366">このテスト ケースは、スクリプトを使用し、各繰り返しを実行する前に次のデータをランダム化することによってループで実行できます。</span><span class="sxs-lookup"><span data-stu-id="5439b-366">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="5439b-367">顧客 ID</span><span class="sxs-lookup"><span data-stu-id="5439b-367">Customer ID</span></span>
- <span data-ttu-id="5439b-368">顧客名</span><span class="sxs-lookup"><span data-stu-id="5439b-368">Customer name</span></span>
- <span data-ttu-id="5439b-369">顧客の住所</span><span class="sxs-lookup"><span data-stu-id="5439b-369">Customer address</span></span>

<span data-ttu-id="5439b-370">顧客 ID は、*ATCUS\<番号\>* の形式で、\<番号\>は **000000001** と **999999999** の間の値にします。</span><span class="sxs-lookup"><span data-stu-id="5439b-370">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="5439b-371">次の例は、1 つのパラメーター、**開始**を使用して、使用される最初の番号を定義します。</span><span class="sxs-lookup"><span data-stu-id="5439b-371">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="5439b-372">2 番目のパラメーター **nr** を使用して、作成する必要がある顧客数を定義します。</span><span class="sxs-lookup"><span data-stu-id="5439b-372">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="5439b-373">繰り返しごとに、Excel パラメーター ファイル内のパラメーターが UpdateCustomer 関数を使用して変更されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-373">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="5439b-374">次に、RSAT コマンドラインは RunTestCase 関数内で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5439b-374">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="5439b-375">管理者モードで Microsoft Windows PowerShell Integrated Scripting Environment (ISE) を開き、**Untitled1.ps1** という名前のウィンドウに次のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="5439b-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="5439b-376">Microsoft Dynamics 365 のデータに依存するスクリプトを実行する</span><span class="sxs-lookup"><span data-stu-id="5439b-376">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="5439b-377">次の例は、オープン データ プロトコル (OData) 呼び出しを使用して、発注書のオーダー状態を検索します。</span><span class="sxs-lookup"><span data-stu-id="5439b-377">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="5439b-378">ステータスが**請求済**ではない場合、たとえば、請求書を転記する RSAT のテスト ケースを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="5439b-378">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
