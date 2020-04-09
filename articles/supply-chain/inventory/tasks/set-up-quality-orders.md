---
title: 品質指示の設定
description: この手順では、受け取る在庫を着荷登録の直後に検査する必要のある品質管理プロセスを有効にする方法を示します。
author: perlynne
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9760aeb823730581aa1f02db1574e6f5eccd1f75
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145643"
---
# <a name="set-up-quality-orders"></a><span data-ttu-id="cf490-103">品質指示の設定</span><span class="sxs-lookup"><span data-stu-id="cf490-103">Set up quality orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf490-104">この手順では、受け取る在庫を着荷登録の直後に検査する必要のある品質管理プロセスを有効にする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cf490-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="cf490-105">手順は品質マネージャーによって通常実行されます。</span><span class="sxs-lookup"><span data-stu-id="cf490-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="cf490-106">プロセスには、サンプルになる品目を定義するために使用する品質グループの作成、および品目に対して実行するテストをグループ化するテスト グループが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cf490-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="cf490-107">USMF デモ データ会社でこのガイドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="cf490-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="cf490-108">品質管理の有効化</span><span class="sxs-lookup"><span data-stu-id="cf490-108">Enable quality management</span></span>
1. <span data-ttu-id="cf490-109">**ナビゲーション ウィンドウ > モジュール > 在庫管理 > 設定 > 在庫および倉庫管理パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf490-109">Go to **Navigation pane > Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="cf490-110">**品質管理**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-110">Click the **Quality management** tab.</span></span>
3. <span data-ttu-id="cf490-111">**品質管理を使用するオプション**を「はい」に設定します。</span><span class="sxs-lookup"><span data-stu-id="cf490-111">Set the **Use quality management option** to 'Yes'.</span></span>
4. <span data-ttu-id="cf490-112">**レポートの設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-112">Click **Report setup**.</span></span> <span data-ttu-id="cf490-113">USMF では、品質管理のレポート設定が既に定義されます。</span><span class="sxs-lookup"><span data-stu-id="cf490-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="cf490-114">これが行われていなかった場合は、異なるレポート タイプに対して新しい行をここで追加し、各レポートに使用するドキュメントのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-114">If this wasn't done, you'd add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="cf490-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf490-115">Close the page.</span></span>
6. <span data-ttu-id="cf490-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf490-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="cf490-117">テストの作成</span><span class="sxs-lookup"><span data-stu-id="cf490-117">Create a test</span></span>
1. <span data-ttu-id="cf490-118">**在庫管理 > 設定 > 品質管理 > テスト**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf490-118">Go to **Inventory management > Setup > Quality control > Tests**.</span></span>
2. <span data-ttu-id="cf490-119">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-119">Click **New**.</span></span>
3. <span data-ttu-id="cf490-120">**テスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-120">In the **Test** field, type a value.</span></span>
4. <span data-ttu-id="cf490-121">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-121">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="cf490-122">**タイプ**フィールドで「オプション」を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-122">In the **Type** field, select 'Option'.</span></span> <span data-ttu-id="cf490-123">この例では、定義済の値に基づいてテスト結果を割り当てることが可能になる [オプション] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="cf490-124">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-124">Click **Save**.</span></span>
7. <span data-ttu-id="cf490-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf490-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="cf490-126">結果を記録する方法を定義するテスト変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="cf490-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="cf490-127">**在庫管理 > 設定 > 品質管理 > テスト変数**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf490-127">Go to **Inventory management > Setup > Quality control > Test variables**.</span></span>
2. <span data-ttu-id="cf490-128">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-128">Click **New**.</span></span>
3. <span data-ttu-id="cf490-129">**変数**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-129">In the **Variable** field, type a value.</span></span>
4. <span data-ttu-id="cf490-130">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-130">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="cf490-131">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-131">Click **Save**.</span></span>
6. <span data-ttu-id="cf490-132">**結果**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-132">Click **Outcomes**.</span></span>
7. <span data-ttu-id="cf490-133">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-133">Click **New**.</span></span>
8. <span data-ttu-id="cf490-134">**結果**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-134">In the **Outcome** field, type a value.</span></span>
9. <span data-ttu-id="cf490-135">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-135">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="cf490-136">**結果ステータス**フィールドで、「パス」を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-136">In the **Outcome status** field, select 'Pass'.</span></span>
11. <span data-ttu-id="cf490-137">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-137">Click **Save**.</span></span>
12. <span data-ttu-id="cf490-138">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-138">Click **New**.</span></span>
13. <span data-ttu-id="cf490-139">**結果**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-139">In the **Outcome** field, type a value.</span></span>
14. <span data-ttu-id="cf490-140">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-140">In the **Description** field, type a value.</span></span>
15. <span data-ttu-id="cf490-141">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-141">Click **Save**.</span></span>
16. <span data-ttu-id="cf490-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf490-142">Close the page.</span></span>
17. <span data-ttu-id="cf490-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf490-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="cf490-144">品目サンプリングの設定</span><span class="sxs-lookup"><span data-stu-id="cf490-144">Set up item sampling</span></span>
1. <span data-ttu-id="cf490-145">**在庫管理 > 設定 > 品質管理 > 品目サンプリング**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf490-145">Go to **Inventory management > Setup > Quality control > Item sampling**.</span></span>
2. <span data-ttu-id="cf490-146">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-146">Click **New**.</span></span>
3. <span data-ttu-id="cf490-147">**品目サンプリング** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-147">In the **Item sampling** field, type a value.</span></span>
4. <span data-ttu-id="cf490-148">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-148">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="cf490-149">**値**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-149">In the **Value** field, enter a number.</span></span> <span data-ttu-id="cf490-150">この値は、隣のフィールドで選択された数量の仕様に関連します。</span><span class="sxs-lookup"><span data-stu-id="cf490-150">This value relates to the Quantity specification that's selected in the adjacent field.</span></span>  
6. <span data-ttu-id="cf490-151">**プロセス** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="cf490-151">Expand or collapse the **Process** section.</span></span>
7. <span data-ttu-id="cf490-152">**完全ブロック** チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="cf490-152">Select or clear the **Full blocking** check box.</span></span> <span data-ttu-id="cf490-153">このオプションを選択した場合、テストに失敗すると、全部または注文明細行の数量はブロックされます。</span><span class="sxs-lookup"><span data-stu-id="cf490-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="cf490-154">これを選択しない場合は、品質指示の品目のみがブロックされます。</span><span class="sxs-lookup"><span data-stu-id="cf490-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="cf490-155">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-155">Click **Save**.</span></span>
9. <span data-ttu-id="cf490-156">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf490-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="cf490-157">品質グループの作成</span><span class="sxs-lookup"><span data-stu-id="cf490-157">Create a quality group</span></span>
1. <span data-ttu-id="cf490-158">**在庫管理 > 設定 > 品質管理 > 品質グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf490-158">Go to **Inventory management > Setup > Quality control > Quality groups**.</span></span>
2. <span data-ttu-id="cf490-159">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-159">Click **New**.</span></span>
3. <span data-ttu-id="cf490-160">**品質グループ** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-160">In the **Quality group** field, type a value.</span></span> <span data-ttu-id="cf490-161">グループにどのタイプの品目が含まれているかを識別しやすい記述名を使用します (サンプリングの基準)。</span><span class="sxs-lookup"><span data-stu-id="cf490-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="cf490-162">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-162">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="cf490-163">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-163">Click **Save**.</span></span>
6. <span data-ttu-id="cf490-164">**品目の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-164">Click **Add items**.</span></span>
7. <span data-ttu-id="cf490-165">**品目番号**行を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-165">Select the **Item number** row.</span></span> <span data-ttu-id="cf490-166">この例では品目番号に基づいフィルタ処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="cf490-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="cf490-167">**基準**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-167">In the **Criteria** field, type a value.</span></span> <span data-ttu-id="cf490-168">たとえば、「T\*」と入力し、T で始まる品目番号にフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="cf490-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="cf490-169">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-169">Click **OK**.</span></span>
10. <span data-ttu-id="cf490-170">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-170">Click **OK**.</span></span>
11. <span data-ttu-id="cf490-171">**品目品質グループ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-171">Click **Item quality groups**.</span></span>
12. <span data-ttu-id="cf490-172">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf490-172">Close the page.</span></span>
13. <span data-ttu-id="cf490-173">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf490-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="cf490-174">テスト グループの作成</span><span class="sxs-lookup"><span data-stu-id="cf490-174">Create a test group</span></span>
1. <span data-ttu-id="cf490-175">**在庫管理 > 設定 > 品質管理 > テスト グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf490-175">Go to **Inventory management > Setup > Quality control > Test groups**.</span></span>
2. <span data-ttu-id="cf490-176">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-176">Click **New**.</span></span>
3. <span data-ttu-id="cf490-177">**テスト グループ** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-177">In the **Test group** field, type a value.</span></span> <span data-ttu-id="cf490-178">どのようなテストが実行され、どの品質グループにテストを関連付ける必要があるかを覚えるのに役立つ名前を**テスト グループ**に指定します。</span><span class="sxs-lookup"><span data-stu-id="cf490-178">Give the **Test group** a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="cf490-179">たとえば、これは "T" で開始する項目を選択する品質グループと一緒に使用され、"T 品目テスト" と呼ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="cf490-179">For example, it it's to be used with a quality group that selects items starting with "T", you could call it "T-item tests".</span></span>  
4. <span data-ttu-id="cf490-180">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-180">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="cf490-181">**品目サンプリング** フィールドで、以前に作成した品目サンプリング行を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-181">In the **Item sampling** field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="cf490-182">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cf490-183">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-183">Click **Add**.</span></span>
8. <span data-ttu-id="cf490-184">**順序番号**フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf490-184">In the **Sequence number** field, enter a number.</span></span>
9. <span data-ttu-id="cf490-185">**テスト** フィールドで、先ほど作成したテストを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-185">In the **Test** field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="cf490-186">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="cf490-187">**テスト** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-187">Click the **Test** tab.</span></span>
12. <span data-ttu-id="cf490-188">**変数**フィールドで、以前に成したテストを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-188">In the **Variable** field, select the test variable that you created before</span></span>
13. <span data-ttu-id="cf490-189">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="cf490-190">**既定の結果**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cf490-190">In the **Default outcome** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="cf490-191">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="cf490-192">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-192">Click **Save**.</span></span>
17. <span data-ttu-id="cf490-193">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf490-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="cf490-194">品質指示の作成時に定義する</span><span class="sxs-lookup"><span data-stu-id="cf490-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="cf490-195">**在庫管理 > 設定 > 品質管理 > 品質関連**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf490-195">Go to **Inventory management > Setup > Quality control > Quality associations**.</span></span>
2. <span data-ttu-id="cf490-196">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-196">Click **New**.</span></span>
3. <span data-ttu-id="cf490-197">**参照タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-197">In the **Reference type** field, select an option.</span></span>
4. <span data-ttu-id="cf490-198">**品目コード** フィールドで「グループ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-198">In the **Item code** field, select 'Group'.</span></span> <span data-ttu-id="cf490-199">この例では、"グループ" を選択し、以前に作成した品質グループを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf490-199">In this example, we'll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="cf490-200">手動で品目を指定するためには、これを「テーブル」と設定することもでき、または品質指示にすべての品目を追加するには「すべて」を選択できます。</span><span class="sxs-lookup"><span data-stu-id="cf490-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="cf490-201">**品目コード** フィールドで、以前に作成した品質グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-201">In the **Item** field, select the quality group that you created before.</span></span> <span data-ttu-id="cf490-202">品目フィールドで指定できるオプションは品目コードの設定内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="cf490-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="cf490-203">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cf490-204">[プロセス] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="cf490-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="cf490-205">**イベント タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-205">In the **Event type** field, select an option.</span></span> <span data-ttu-id="cf490-206">これはテストを発生させるイベントです。</span><span class="sxs-lookup"><span data-stu-id="cf490-206">This is the event that triggers the test.</span></span> <span data-ttu-id="cf490-207">ここで使用可能なオプションは参照タイプ フィールドで選択したプロセスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="cf490-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="cf490-208">**実行**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-208">In the **Execution** field, select an option.</span></span>
10. <span data-ttu-id="cf490-209">**品質指示プロセス** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="cf490-209">Expand or collapse the **Quality order process** section.</span></span>
11. <span data-ttu-id="cf490-210">**イベント ブロッキング** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cf490-210">In the **Event blocking** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="cf490-211">このフィールドには、品質指示がまだ開いている場合に、ブロックできるプロセスの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf490-211">This field shows the list of processes that it's possible to block if the quality order is still open.</span></span> <span data-ttu-id="cf490-212">オプションは、イベント タイプ フィールドの選択内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="cf490-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="cf490-213">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-213">In the list, click the link in the selected row.</span></span> <span data-ttu-id="cf490-214">これは、以前に選択した値によって異なってきます。</span><span class="sxs-lookup"><span data-stu-id="cf490-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="cf490-215">未処理の品質指示を伝票明細行にリンクさせている間に次のプロセスをブロックする必要がある場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="cf490-216">**詳細**セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="cf490-216">Expand or collapse the **Specifications** section.</span></span>
14. <span data-ttu-id="cf490-217">**テスト グループ** フィールドで、以前に作成したテスト グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-217">In the **Test group** field, select the test group that you created before.</span></span>
15. <span data-ttu-id="cf490-218">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cf490-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="cf490-219">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf490-219">Click **Save**.</span></span>
17. <span data-ttu-id="cf490-220">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf490-220">Close the page.</span></span>

