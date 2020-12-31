---
title: Regression Suite Automation Tool チュートリアルの使用
description: このトピックでは、Regression Suite Automation Tool (RSAT) の使用方法について説明します。 さまざまな機能について説明し、高度なスクリプトを使用した例を示します。
author: robinarh
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 798717b276e68949a9425350720bf683a37d6fb5
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692993"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="83911-104">Regression Suite Automation Tool のチュートリアル</span><span class="sxs-lookup"><span data-stu-id="83911-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="83911-105">インターネット ブラウザーのツールを使用して、このページを PDF 形式でダウンロードして保存します。</span><span class="sxs-lookup"><span data-stu-id="83911-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="83911-106">このチュートリアルでは、デモの割り当て、戦略と重要な学習ポイントの説明を含む Regression Suite Automation Tool (RSAT) の高度な機能をいくつかを説明します。</span><span class="sxs-lookup"><span data-stu-id="83911-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span> 

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="83911-107">RSAT とタスク レコーダーの注目すべき機能</span><span class="sxs-lookup"><span data-stu-id="83911-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="83911-108">フィールド値を検証する</span><span class="sxs-lookup"><span data-stu-id="83911-108">Validate a field value</span></span>

<span data-ttu-id="83911-109">RSAT を使用すると、予測値を検証するためにテスト ケース内に検証ステップを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="83911-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="83911-110">この機能の詳細については、[予測値の検証](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83911-110">For information about this feature, see the article [Validate expected values](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span></span>

<span data-ttu-id="83911-111">次の例は、この機能を使用して、手持在庫が 0 (ゼロ) よりも大きいかどうかを検証する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="83911-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="83911-112">**USMF** 会社のデモデータで、次の手順を含むタスク記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="83911-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="83911-113">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="83911-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="83911-114">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="83911-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="83911-115">たとえば、**1000** という値で **品目番号** フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="83911-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="83911-116">**手持在庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83911-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="83911-117">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="83911-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="83911-118">たとえば、**1** という値で **サイト** フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="83911-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="83911-119">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="83911-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="83911-120">**引当可能合計数** フィールドの値が、**411.0000000000000000** であることを検証します。</span><span class="sxs-lookup"><span data-stu-id="83911-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="83911-121">タスクの記録を保存し、Azure Devops のテスト ケースに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="83911-121">Save the task recording and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="83911-122">テスト ケースをテスト計画に追加し、テスト ケースを RSAT に読み込みます。</span><span class="sxs-lookup"><span data-stu-id="83911-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="83911-123">Excel パラメーター ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="83911-123">Open the Excel parameter file.</span></span> <span data-ttu-id="83911-124">**手持ち在庫品目** タブに、**演算子** フィールドを含む **手持ち在庫品目検証** セクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83911-124">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![演算子フィールド](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="83911-126">手持在庫が常に 0 より大きいかどうかを検証するには、**値** フィールドの値を **411** から **0** に、および **演算子** フィールドの値を等号 (**=**) から大なり記号 (**\>**) に変更します。</span><span class="sxs-lookup"><span data-stu-id="83911-126">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![値と演算子フィールドの値が変更されました](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="83911-128">Excel パラメーター ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="83911-128">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="83911-129">**アップロード** を選択し、Excel パラメーター ファイルに加えた変更を Azure DevOps に保存します。</span><span class="sxs-lookup"><span data-stu-id="83911-129">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="83911-130">これで、指定した在庫品目の **引当可能合計数** フィールド値が0 ( ゼロ ) よりも大きい場合、実際の手持在庫値に関係なくテストが合格となります。</span><span class="sxs-lookup"><span data-stu-id="83911-130">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="83911-131">保存された変数とテスト ケースの連鎖</span><span class="sxs-lookup"><span data-stu-id="83911-131">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="83911-132">RSAT の主要な機能の 1 つとして、テスト ケースの連鎖、つまり、変数を他のテストに渡すテストの機能、があります。</span><span class="sxs-lookup"><span data-stu-id="83911-132">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="83911-133">詳細については、[テスト ケースの連鎖への変数のコピー](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83911-133">For more information, see the article [Copy variables to chain test cases](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="83911-134">派生テスト ケース</span><span class="sxs-lookup"><span data-stu-id="83911-134">Derived test case</span></span>

<span data-ttu-id="83911-135">RSAT を使用すると、複数のテスト ケースで同じタスク レコードを使用して、タスクを異なるデータ構成で実行できます。</span><span class="sxs-lookup"><span data-stu-id="83911-135">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="83911-136">詳細については、[派生テスト ケース](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83911-136">See the article [Derived test cases](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="83911-137">通知とメッセージの検証</span><span class="sxs-lookup"><span data-stu-id="83911-137">Validate notifications and messages</span></span>

<span data-ttu-id="83911-138">この機能は、アクションが実行されたかどうかを検証するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="83911-138">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="83911-139">たとえば、製造オーダーが作成、見積り、開始された時に、アプリは製造オーダーが開始されたことを通知する "生産 – 開始" メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="83911-139">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![生産 – 開始通知](./media/use_rsa_tool_05.png)

<span data-ttu-id="83911-141">RSAT を使用してこのメッセージを検証するには、該当する記録の Excel パラメーター ファイルにある **メッセージ検証** タブにメッセージ テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="83911-141">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![メッセージ検証タブ](./media/use_rsa_tool_06.png)

<span data-ttu-id="83911-143">テスト ケースを実行すると、Excel パラメーター ファイル内のメッセージが、表示されるメッセージと比較されます。</span><span class="sxs-lookup"><span data-stu-id="83911-143">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="83911-144">メッセージが一致しない場合、テストケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="83911-144">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="83911-145">Excel パラメーター ファイルの **メッセージ検証** タブには、複数のメッセージを入力できます。</span><span class="sxs-lookup"><span data-stu-id="83911-145">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="83911-146">メッセージは、情報メッセージではなく、エラーまたは警告メッセージである場合もあります。</span><span class="sxs-lookup"><span data-stu-id="83911-146">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="83911-147">スナップショット</span><span class="sxs-lookup"><span data-stu-id="83911-147">Snapshot</span></span>

<span data-ttu-id="83911-148">この機能は、タスク記録中に実行された手順のスクリーンショットを撮ります。</span><span class="sxs-lookup"><span data-stu-id="83911-148">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="83911-149">これは、監査やデバッグの目的で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="83911-149">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="83911-150">この機能を使用するには、RSAT のインストール フォルダー (たとえば、**C:\\Program Files (x86)\\Regression Suite Automation Tool**) にある **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ファイルを開き、次の要素の値を **False** から **True** に変更します。</span><span class="sxs-lookup"><span data-stu-id="83911-150">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="83911-151">テスト ケースを実行すると、RSAT は、作業ディレクトリ内のテスト ケースの再生フォルダにあるステップのスナップショット (画像) を生成します。</span><span class="sxs-lookup"><span data-stu-id="83911-151">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="83911-152">古いバージョンの RSAT を使用している場合、画像は **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** に保存され、実行される各テスト ケースに対して個別のフォルダが作成されます。</span><span class="sxs-lookup"><span data-stu-id="83911-152">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="83911-153">割り当て</span><span class="sxs-lookup"><span data-stu-id="83911-153">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="83911-154">シナリオ</span><span class="sxs-lookup"><span data-stu-id="83911-154">Scenario</span></span>

1. <span data-ttu-id="83911-155">製品デザイナーが新しくリリースされた製品を作成します。</span><span class="sxs-lookup"><span data-stu-id="83911-155">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="83911-156">生産マネージャは、在庫レベルを 2 個にするために製造オーダーを開始します。</span><span class="sxs-lookup"><span data-stu-id="83911-156">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="83911-157">製造は、製造オーダーを開始および終了し、手持在庫数量が 2 個であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="83911-157">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="83911-158">販売チームは、新しい製品 4 個 の注文を受けます。</span><span class="sxs-lookup"><span data-stu-id="83911-158">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="83911-159">したがって、販売チームは動的計画を使って正味必要量を更新します。</span><span class="sxs-lookup"><span data-stu-id="83911-159">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="83911-160">追加の利用可能容量がないので、既定の注文ポリシーは "作成ではなく購入" に設定されます。</span><span class="sxs-lookup"><span data-stu-id="83911-160">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="83911-161">したがって、計画発注書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="83911-161">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="83911-162">購入者は、仕入先を追加し、計画発注書を確定してから、発注書を確認します。</span><span class="sxs-lookup"><span data-stu-id="83911-162">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="83911-163">購入した商品が店舗に到着すると、店舗オペレーターが関連する発注書を検索して商品を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="83911-163">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="83911-164">注文が完了したため、販売注文に対して商品をピッキングおよび梱包することができます。</span><span class="sxs-lookup"><span data-stu-id="83911-164">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="83911-165">財務は、仕入請求書および売上請求書に転記します。</span><span class="sxs-lookup"><span data-stu-id="83911-165">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="83911-166">次の図は、このシナリオのフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="83911-166">The following illustration shows the flow for this scenario.</span></span>

![デモ シナリオのフロー](./media/use_rsa_tool_14.png)

<span data-ttu-id="83911-168">次の図は、LCS ビジネス プロセス モデラーでのこのシナリオの業務プロセスの階層を示しています。</span><span class="sxs-lookup"><span data-stu-id="83911-168">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![デモ シナリオの業務プロセス](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="83911-170">戦略 – キー学習</span><span class="sxs-lookup"><span data-stu-id="83911-170">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="83911-171">データ</span><span class="sxs-lookup"><span data-stu-id="83911-171">Data</span></span>

- <span data-ttu-id="83911-172">代表的なデータボリューム (生産のコピー/高品質の構成データと移行されたデータ) があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="83911-172">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="83911-173">タスク レコーダーを介して新しいデータを生成する場合は、既存の名前と競合しないテスト名 (例えば、**RSATxxx** などの接頭語を使用するなど) を作成します。</span><span class="sxs-lookup"><span data-stu-id="83911-173">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="83911-174">Azure ポイントインタイム復元を使用して、第 1 層環境以外でテストを再実行します。</span><span class="sxs-lookup"><span data-stu-id="83911-174">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="83911-175">Excel 関数の **RANDOM** や **NOW** を使用して、独自の組み合わせを生成することはできますが、その作業量は大幅に多くなります。</span><span class="sxs-lookup"><span data-stu-id="83911-175">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="83911-176">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="83911-176">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="83911-177">タスク レコーダー</span><span class="sxs-lookup"><span data-stu-id="83911-177">Task recorder</span></span>

- <span data-ttu-id="83911-178">記録を開始する前にシナリオを定義します。</span><span class="sxs-lookup"><span data-stu-id="83911-178">Define scenarios before you start recording.</span></span> <span data-ttu-id="83911-179">適切に管理されたプロジェクトには、事前定義済みのテスト シナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="83911-179">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="83911-180">テスト ケースを構築するには、それらのテスト シナリオの結果がどの程度予測可能かを考慮します。</span><span class="sxs-lookup"><span data-stu-id="83911-180">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="83911-181">異なるロールによって実行される場合、または待機時間がある場合、または次のステップの前に外部イベントがある場合に、記録を分割します。</span><span class="sxs-lookup"><span data-stu-id="83911-181">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="83911-182">リストから値を選択することは避けてください。</span><span class="sxs-lookup"><span data-stu-id="83911-182">Avoid selecting values in lists.</span></span> <span data-ttu-id="83911-183">代わりに、**FIFO**、**AudioRM**、**SiteWH** などのテキスト形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="83911-183">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="83911-184">リスト内で選択した場合は、値自体ではなく、リスト内の値の位置が記録されます。</span><span class="sxs-lookup"><span data-stu-id="83911-184">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="83911-185">このリストに品目を追加すると、値の位置が変わる場合があります。</span><span class="sxs-lookup"><span data-stu-id="83911-185">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="83911-186">したがって、記録では別のパラメーターが使用され、その他のシナリオが影響を受ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="83911-186">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="83911-187">マルチ ユーザーの動作について考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="83911-187">Think about multi-user behavior.</span></span> <span data-ttu-id="83911-188">たとえば、新しく作成された販売注文が常に自動的に選択されるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="83911-188">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="83911-189">代わりに、常にフィルターを使用して正しい注文を見つけます。</span><span class="sxs-lookup"><span data-stu-id="83911-189">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="83911-190">連鎖したテスト ケースで使用できるように、タスク レコーダーのコピー機能を使用して、新しく作成された製品の名前を保存します。</span><span class="sxs-lookup"><span data-stu-id="83911-190">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="83911-191">タスク レコーダーの検証機能を使用して、ステップが正常に実行されたことを確認するチェックポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="83911-191">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="83911-192">RSAT</span><span class="sxs-lookup"><span data-stu-id="83911-192">RSAT</span></span>

- <span data-ttu-id="83911-193">別の会社でテストを実行するには、Excel パラメーター ファイルの **一般** タブで会社を変更します。</span><span class="sxs-lookup"><span data-stu-id="83911-193">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="83911-194">設定およびデータが、新しく選択した会社で使用可能であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="83911-194">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="83911-195">テスト ユーザーは、Excel パラメーター ファイルの **一般** タブで変更できます。</span><span class="sxs-lookup"><span data-stu-id="83911-195">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="83911-196">テスト ケースを実行するユーザーの電子メール ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="83911-196">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="83911-197">この方法で、指定したユーザーのセキュリティ アクセス許可を使用し、テスト ケースを実行できます。</span><span class="sxs-lookup"><span data-stu-id="83911-197">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="83911-198">テストが開始されるまで待機するには、Excel パラメーター ファイルの **一般** タブで一時停止を定義します。</span><span class="sxs-lookup"><span data-stu-id="83911-198">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="83911-199">この一時停止は、バッチ ジョブで使用できます (たとえば、次のステップを実行する前にワークフローを実行する必要がある場合など)。</span><span class="sxs-lookup"><span data-stu-id="83911-199">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="83911-200">高度なスクリプト</span><span class="sxs-lookup"><span data-stu-id="83911-200">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="83911-201">CLI</span><span class="sxs-lookup"><span data-stu-id="83911-201">CLI</span></span>

<span data-ttu-id="83911-202">RSAT は、**コマンド プロンプト** または **PowerShell** ウィンドウから呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="83911-202">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="83911-203">**TestRoot** 環境変数が RSAT インストール パスに設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="83911-203">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="83911-204">(Microsoft Windows の **コントロール パネル** を開き、**システムとセキュリティ\>システム\>高度なシステム設定** を選択し、**環境変数** を選択します。)</span><span class="sxs-lookup"><span data-stu-id="83911-204">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="83911-205">**コマンド プロンプト** または **PowerShell** ウィンドウを管理者として開きます。</span><span class="sxs-lookup"><span data-stu-id="83911-205">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="83911-206">RSAT インストール ディレクトリに移動します。</span><span class="sxs-lookup"><span data-stu-id="83911-206">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="83911-207">すべてのコマンドのリスト</span><span class="sxs-lookup"><span data-stu-id="83911-207">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="83911-208">?</span><span class="sxs-lookup"><span data-stu-id="83911-208">?</span></span> 
<span data-ttu-id="83911-209">使用可能なすべてのコマンドとそのパラメーターに関するヘルプを表示します。</span><span class="sxs-lookup"><span data-stu-id="83911-209">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="83911-210">オプションのパラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-210">Optional parameters</span></span>

**``command``**


<span data-ttu-id="83911-211">ここで、``[command]`` は以下で指定されたコマンドの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="83911-211">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="83911-212">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="83911-212">about</span></span>
<span data-ttu-id="83911-213">現在のバージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="83911-213">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="83911-214">cls</span><span class="sxs-lookup"><span data-stu-id="83911-214">cls</span></span>
<span data-ttu-id="83911-215">画面をクリアします。</span><span class="sxs-lookup"><span data-stu-id="83911-215">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="83911-216">ダウンロード</span><span class="sxs-lookup"><span data-stu-id="83911-216">download</span></span>
<span data-ttu-id="83911-217">指定したテスト ケースの添付ファイルを出力ディレクトリにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="83911-217">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="83911-218">``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。</span><span class="sxs-lookup"><span data-stu-id="83911-218">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="83911-219">最初の列の値を **test_case_id** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="83911-219">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-220">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-220">Required parameters</span></span>
<span data-ttu-id="83911-221">**``test_case_id``** テスト ケース ID を表します。</span><span class="sxs-lookup"><span data-stu-id="83911-221">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="83911-222">**``output_dir``** 出力ディレクトリを表します。</span><span class="sxs-lookup"><span data-stu-id="83911-222">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="83911-223">このディレクトリが存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="83911-223">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="83911-224">例</span><span class="sxs-lookup"><span data-stu-id="83911-224">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="83911-225">編集</span><span class="sxs-lookup"><span data-stu-id="83911-225">edit</span></span>
<span data-ttu-id="83911-226">Excel プログラムでパラメーター ファイルを開いて編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="83911-226">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-227">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-227">Required parameters</span></span>
<span data-ttu-id="83911-228">**``excel_file``** 既存の Excel ファイルへの完全なパスが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="83911-228">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="83911-229">例</span><span class="sxs-lookup"><span data-stu-id="83911-229">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="83911-230">作成</span><span class="sxs-lookup"><span data-stu-id="83911-230">generate</span></span>
<span data-ttu-id="83911-231">指定されたテスト ケースのテスト実行およびパラメーター ファイルを出力ディレクトリに生成します。</span><span class="sxs-lookup"><span data-stu-id="83911-231">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="83911-232">``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。</span><span class="sxs-lookup"><span data-stu-id="83911-232">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="83911-233">最初の列の値を **test_case_id** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="83911-233">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-234">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-234">Required parameters</span></span>
<span data-ttu-id="83911-235">**``test_case_id``** テスト ケース ID を表します。</span><span class="sxs-lookup"><span data-stu-id="83911-235">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="83911-236">**``output_dir``** 出力ディレクトリを表します。</span><span class="sxs-lookup"><span data-stu-id="83911-236">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="83911-237">このディレクトリが存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="83911-237">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="83911-238">例</span><span class="sxs-lookup"><span data-stu-id="83911-238">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="83911-239">generatederived</span><span class="sxs-lookup"><span data-stu-id="83911-239">generatederived</span></span>
<span data-ttu-id="83911-240">指定されたテスト ケースから派生する新しいテスト ケースを生成します。</span><span class="sxs-lookup"><span data-stu-id="83911-240">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="83911-241">``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。</span><span class="sxs-lookup"><span data-stu-id="83911-241">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="83911-242">最初の列の値を **test_case_id** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="83911-242">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-243">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-243">Required parameters</span></span>
<span data-ttu-id="83911-244">**``parent_test_case_id``** 親テスト ケース ID を表します。</span><span class="sxs-lookup"><span data-stu-id="83911-244">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="83911-245">**``test_plan_id``** テスト計画 ID を表します。</span><span class="sxs-lookup"><span data-stu-id="83911-245">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="83911-246">**``test_suite_id``** テスト スイート ID を表します。</span><span class="sxs-lookup"><span data-stu-id="83911-246">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="83911-247">例</span><span class="sxs-lookup"><span data-stu-id="83911-247">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="83911-248">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="83911-248">generatetestonly</span></span>
<span data-ttu-id="83911-249">指定されたテスト ケースのテスト実行ファイルのみを出力ディレクトリに生成します。</span><span class="sxs-lookup"><span data-stu-id="83911-249">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="83911-250">``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。</span><span class="sxs-lookup"><span data-stu-id="83911-250">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="83911-251">最初の列の値を **test_case_id** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="83911-251">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-252">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-252">Required parameters</span></span>
<span data-ttu-id="83911-253">**``test_case_id``** テスト ケース ID を表します。</span><span class="sxs-lookup"><span data-stu-id="83911-253">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="83911-254">**``output_dir``** 出力ディレクトリを表します。</span><span class="sxs-lookup"><span data-stu-id="83911-254">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="83911-255">このディレクトリが存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="83911-255">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="83911-256">例</span><span class="sxs-lookup"><span data-stu-id="83911-256">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="83911-257">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="83911-257">generatetestsuite</span></span>
<span data-ttu-id="83911-258">指定されたスイートのすべてのテスト ケースを出力ディレクトリに生成します。</span><span class="sxs-lookup"><span data-stu-id="83911-258">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="83911-259">``listtestsuitenames`` コマンドを使用すると、使用可能なすべてのテスト スイートを取得できます。</span><span class="sxs-lookup"><span data-stu-id="83911-259">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="83911-260">最初の列の値を **test_suite_name** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="83911-260">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-261">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-261">Required parameters</span></span>
<span data-ttu-id="83911-262">**``test_suite_name``** テスト スイートの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="83911-262">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="83911-263">**``output_dir``** 出力ディレクトリを表します。</span><span class="sxs-lookup"><span data-stu-id="83911-263">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="83911-264">このディレクトリが存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="83911-264">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="83911-265">例</span><span class="sxs-lookup"><span data-stu-id="83911-265">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="83911-266">ヘルプ</span><span class="sxs-lookup"><span data-stu-id="83911-266">help</span></span>
<span data-ttu-id="83911-267">[?](#section) と同一</span><span class="sxs-lookup"><span data-stu-id="83911-267">Identical to the [?](#section)</span></span> <span data-ttu-id="83911-268">command</span><span class="sxs-lookup"><span data-stu-id="83911-268">command</span></span>


#### <a name="list"></a><span data-ttu-id="83911-269">リスト</span><span class="sxs-lookup"><span data-stu-id="83911-269">list</span></span>
<span data-ttu-id="83911-270">使用可能なすべてのテスト ケースを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="83911-270">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="83911-271">listtestplans</span><span class="sxs-lookup"><span data-stu-id="83911-271">listtestplans</span></span>
<span data-ttu-id="83911-272">使用可能なすべてのテスト計画を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="83911-272">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="83911-273">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="83911-273">listtestsuite</span></span>
<span data-ttu-id="83911-274">指定されたテスト スイートのテスト ケースを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="83911-274">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="83911-275">``listtestsuitenames`` コマンドを使用すると、使用可能なすべてのテスト スイートを取得できます。</span><span class="sxs-lookup"><span data-stu-id="83911-275">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="83911-276">最初の列の値を **suite_name** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="83911-276">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-277">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-277">Required parameters</span></span>
<span data-ttu-id="83911-278">**``suite_name``** 目的のスイートの名前。</span><span class="sxs-lookup"><span data-stu-id="83911-278">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="83911-279">例</span><span class="sxs-lookup"><span data-stu-id="83911-279">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="83911-280">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="83911-280">listtestsuitenames</span></span>
<span data-ttu-id="83911-281">使用可能なすべてのテスト スイートを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="83911-281">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="83911-282">playback</span><span class="sxs-lookup"><span data-stu-id="83911-282">playback</span></span>
<span data-ttu-id="83911-283">Excel ファイルを使用してテスト ケースを再生します。</span><span class="sxs-lookup"><span data-stu-id="83911-283">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-284">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-284">Required parameters</span></span>
<span data-ttu-id="83911-285">**``excel_file``** Excel ファイルへの完全なパス。</span><span class="sxs-lookup"><span data-stu-id="83911-285">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="83911-286">ファイルが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83911-286">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="83911-287">例</span><span class="sxs-lookup"><span data-stu-id="83911-287">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="83911-288">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="83911-288">playbackbyid</span></span>
<span data-ttu-id="83911-289">同時に複数のテスト ケースを再生します。</span><span class="sxs-lookup"><span data-stu-id="83911-289">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="83911-290">``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。</span><span class="sxs-lookup"><span data-stu-id="83911-290">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="83911-291">最初の列の値を **test_case_id** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="83911-291">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-292">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-292">Required parameters</span></span>
<span data-ttu-id="83911-293">**``test_case_id1``** 既存のテスト ケースの ID。</span><span class="sxs-lookup"><span data-stu-id="83911-293">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="83911-294">**``test_case_id2``** 既存のテスト ケースの ID。</span><span class="sxs-lookup"><span data-stu-id="83911-294">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="83911-295">**``test_case_idN``** 既存のテスト ケースの ID。</span><span class="sxs-lookup"><span data-stu-id="83911-295">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="83911-296">例</span><span class="sxs-lookup"><span data-stu-id="83911-296">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="83911-297">playbackmany</span><span class="sxs-lookup"><span data-stu-id="83911-297">playbackmany</span></span>
<span data-ttu-id="83911-298">Excel ファイルを使用して、同時に多数のテスト ケースを再生します。</span><span class="sxs-lookup"><span data-stu-id="83911-298">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-299">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-299">Required parameters</span></span>
<span data-ttu-id="83911-300">**``excel_file1``** Excel ファイルへの完全なパス。</span><span class="sxs-lookup"><span data-stu-id="83911-300">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="83911-301">ファイルが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83911-301">File must exist.</span></span>  
<span data-ttu-id="83911-302">**``excel_file2``** Excel ファイルへの完全なパス。</span><span class="sxs-lookup"><span data-stu-id="83911-302">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="83911-303">ファイルが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83911-303">File must exist.</span></span>  
<span data-ttu-id="83911-304">**``excel_fileN``** Excel ファイルへの完全なパス。</span><span class="sxs-lookup"><span data-stu-id="83911-304">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="83911-305">ファイルが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83911-305">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="83911-306">例</span><span class="sxs-lookup"><span data-stu-id="83911-306">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="83911-307">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="83911-307">playbacksuite</span></span>
<span data-ttu-id="83911-308">指定されたテスト スイートからすべてのテスト ケースを再生します。</span><span class="sxs-lookup"><span data-stu-id="83911-308">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="83911-309">``listtestsuitenames`` コマンドを使用すると、使用可能なすべてのテスト スイートを取得できます。</span><span class="sxs-lookup"><span data-stu-id="83911-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="83911-310">最初の列の値を **suite_name** パラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="83911-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-311">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-311">Required parameters</span></span>
<span data-ttu-id="83911-312">**``suite_name``** 目的のスイートの名前。</span><span class="sxs-lookup"><span data-stu-id="83911-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="83911-313">例</span><span class="sxs-lookup"><span data-stu-id="83911-313">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="83911-314">quit</span><span class="sxs-lookup"><span data-stu-id="83911-314">quit</span></span>
<span data-ttu-id="83911-315">アプリケーションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="83911-315">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="83911-316">アップロード</span><span class="sxs-lookup"><span data-stu-id="83911-316">upload</span></span>
<span data-ttu-id="83911-317">指定されたテスト スイートまたはテスト ケースに属するすべてのファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="83911-317">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="83911-318">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-318">Required parameters</span></span>
<span data-ttu-id="83911-319">**``suite_name``** 指定されたテスト スイートに属するすべてのファイルがアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="83911-319">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="83911-320">**``testcase_id``** 指定されたテスト ケースに属するすべてのファイルがアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="83911-320">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="83911-321">例</span><span class="sxs-lookup"><span data-stu-id="83911-321">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="83911-322">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="83911-322">uploadrecording</span></span>
<span data-ttu-id="83911-323">指定されたテスト ケースに属する記録ファイルのみをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="83911-323">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="83911-324">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="83911-324">Required parameters</span></span>
<span data-ttu-id="83911-325">**``testcase_id``** 指定されたテスト ケースに属する記録ファイルがアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="83911-325">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="83911-326">例</span><span class="sxs-lookup"><span data-stu-id="83911-326">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="83911-327">使用</span><span class="sxs-lookup"><span data-stu-id="83911-327">usage</span></span>
<span data-ttu-id="83911-328">このアプリケーションを呼び出す 2 つの方法を示します。1 つは既定の設定ファイルを使用する方法、もう 1 つは設定ファイルを提供する方法です。</span><span class="sxs-lookup"><span data-stu-id="83911-328">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="83911-329">Windows PowerShell の例</span><span class="sxs-lookup"><span data-stu-id="83911-329">Windows PowerShell examples</span></span>

[!IMPORTANT] <span data-ttu-id="83911-330">次のサンプル スクリプトは、説明のためのもので Microsoft ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="83911-330">The example scripts below are provided AS IS for illustration purposes and are not supported by Microsoft.</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="83911-331">ループでのテスト ケースの実行</span><span class="sxs-lookup"><span data-stu-id="83911-331">Run a test case in a loop</span></span>

<span data-ttu-id="83911-332">新しい顧客を作成するテスト スクリプトがあります。</span><span class="sxs-lookup"><span data-stu-id="83911-332">You have a test script that creates a new customer.</span></span> <span data-ttu-id="83911-333">このテスト ケースは、スクリプトを使用し、各繰り返しを実行する前に次のデータをランダム化することによってループで実行できます。</span><span class="sxs-lookup"><span data-stu-id="83911-333">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="83911-334">顧客 ID</span><span class="sxs-lookup"><span data-stu-id="83911-334">Customer ID</span></span>
- <span data-ttu-id="83911-335">顧客名</span><span class="sxs-lookup"><span data-stu-id="83911-335">Customer name</span></span>
- <span data-ttu-id="83911-336">顧客の住所</span><span class="sxs-lookup"><span data-stu-id="83911-336">Customer address</span></span>

<span data-ttu-id="83911-337">顧客 ID は、*ATCUS\<number\>* の形式で、\<number\>は **000000001** と **999999999** の間の値にします。</span><span class="sxs-lookup"><span data-stu-id="83911-337">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="83911-338">次の例は、1 つのパラメーター、**開始** を使用して、使用される最初の番号を定義します。</span><span class="sxs-lookup"><span data-stu-id="83911-338">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="83911-339">2 番目のパラメーター **nr** を使用して、作成する必要がある顧客数を定義します。</span><span class="sxs-lookup"><span data-stu-id="83911-339">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="83911-340">繰り返しごとに、Excel パラメーター ファイル内のパラメーターが UpdateCustomer 関数を使用して変更されます。</span><span class="sxs-lookup"><span data-stu-id="83911-340">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="83911-341">次に、RSAT コマンドラインは RunTestCase 関数内で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="83911-341">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="83911-342">管理者モードで Microsoft Windows PowerShell Integrated Scripting Environment (ISE) を開き、**Untitled1.ps1** という名前のウィンドウに次のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="83911-342">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="83911-343">Microsoft Dynamics 365 のデータに依存するスクリプトを実行する</span><span class="sxs-lookup"><span data-stu-id="83911-343">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="83911-344">次の例は、オープン データ プロトコル (OData) 呼び出しを使用して、発注書のオーダー状態を検索します。</span><span class="sxs-lookup"><span data-stu-id="83911-344">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="83911-345">ステータスが **請求済** ではない場合、たとえば、請求書を転記する RSAT のテスト ケースを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="83911-345">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
