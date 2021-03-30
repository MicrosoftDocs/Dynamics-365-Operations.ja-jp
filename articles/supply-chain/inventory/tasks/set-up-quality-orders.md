---
title: 品質指示の設定
description: この手順では、受け取る在庫を着荷登録の直後に検査する必要のある品質管理プロセスを有効にする方法を示します。
author: perlynne
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351b2ce6b5678976fa8c46908c16dbadbbe23e97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244306"
---
# <a name="set-up-quality-orders"></a><span data-ttu-id="e0df6-103">品質指示の設定</span><span class="sxs-lookup"><span data-stu-id="e0df6-103">Set up quality orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0df6-104">この手順では、受け取る在庫を着荷登録の直後に検査する必要のある品質管理プロセスを有効にする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="e0df6-105">手順は品質マネージャーによって通常実行されます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="e0df6-106">プロセスには、サンプルになる品目を定義するために使用する品質グループの作成、および品目に対して実行するテストをグループ化するテスト グループが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="e0df6-107">USMF デモ データ会社でこのガイドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="e0df6-108">品質管理の有効化</span><span class="sxs-lookup"><span data-stu-id="e0df6-108">Enable quality management</span></span>
1. <span data-ttu-id="e0df6-109">**ナビゲーション ウィンドウ > モジュール > 在庫管理 > 設定 > 在庫および倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-109">Go to **Navigation pane > Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="e0df6-110">**品質管理** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-110">Click the **Quality management** tab.</span></span>
3. <span data-ttu-id="e0df6-111">**品質管理を使用するオプション** を「はい」に設定します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-111">Set the **Use quality management option** to 'Yes'.</span></span>
4. <span data-ttu-id="e0df6-112">**レポートの設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-112">Click **Report setup**.</span></span> <span data-ttu-id="e0df6-113">USMF では、品質管理のレポート設定が既に定義されます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="e0df6-114">これが行われていなかった場合は、異なるレポート タイプに対して新しい行をここで追加し、各レポートに使用するドキュメントのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-114">If this wasn't done, you'd add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="e0df6-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-115">Close the page.</span></span>
6. <span data-ttu-id="e0df6-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="e0df6-117">テストの作成</span><span class="sxs-lookup"><span data-stu-id="e0df6-117">Create a test</span></span>
1. <span data-ttu-id="e0df6-118">**在庫管理 > 設定 > 品質管理 > テスト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-118">Go to **Inventory management > Setup > Quality control > Tests**.</span></span>
2. <span data-ttu-id="e0df6-119">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-119">Click **New**.</span></span>
3. <span data-ttu-id="e0df6-120">**テスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-120">In the **Test** field, type a value.</span></span>
4. <span data-ttu-id="e0df6-121">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-121">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="e0df6-122">**タイプ** フィールドで「オプション」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-122">In the **Type** field, select 'Option'.</span></span> <span data-ttu-id="e0df6-123">この例では、定義済の値に基づいてテスト結果を割り当てることが可能になる [オプション] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="e0df6-124">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-124">Click **Save**.</span></span>
7. <span data-ttu-id="e0df6-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="e0df6-126">結果を記録する方法を定義するテスト変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="e0df6-127">**在庫管理 > 設定 > 品質管理 > テスト変数** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-127">Go to **Inventory management > Setup > Quality control > Test variables**.</span></span>
2. <span data-ttu-id="e0df6-128">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-128">Click **New**.</span></span>
3. <span data-ttu-id="e0df6-129">**変数** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-129">In the **Variable** field, type a value.</span></span>
4. <span data-ttu-id="e0df6-130">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-130">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="e0df6-131">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-131">Click **Save**.</span></span>
6. <span data-ttu-id="e0df6-132">**結果** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-132">Click **Outcomes**.</span></span>
7. <span data-ttu-id="e0df6-133">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-133">Click **New**.</span></span>
8. <span data-ttu-id="e0df6-134">**結果** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-134">In the **Outcome** field, type a value.</span></span>
9. <span data-ttu-id="e0df6-135">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-135">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="e0df6-136">**結果ステータス** フィールドで、「パス」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-136">In the **Outcome status** field, select 'Pass'.</span></span>
11. <span data-ttu-id="e0df6-137">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-137">Click **Save**.</span></span>
12. <span data-ttu-id="e0df6-138">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-138">Click **New**.</span></span>
13. <span data-ttu-id="e0df6-139">**結果** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-139">In the **Outcome** field, type a value.</span></span>
14. <span data-ttu-id="e0df6-140">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-140">In the **Description** field, type a value.</span></span>
15. <span data-ttu-id="e0df6-141">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-141">Click **Save**.</span></span>
16. <span data-ttu-id="e0df6-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-142">Close the page.</span></span>
17. <span data-ttu-id="e0df6-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="e0df6-144">品目サンプリングの設定</span><span class="sxs-lookup"><span data-stu-id="e0df6-144">Set up item sampling</span></span>
1. <span data-ttu-id="e0df6-145">**在庫管理 > 設定 > 品質管理 > 品目サンプリング** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-145">Go to **Inventory management > Setup > Quality control > Item sampling**.</span></span>
2. <span data-ttu-id="e0df6-146">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-146">Click **New**.</span></span>
3. <span data-ttu-id="e0df6-147">**品目サンプリング** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-147">In the **Item sampling** field, type a value.</span></span>
4. <span data-ttu-id="e0df6-148">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-148">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="e0df6-149">**値** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-149">In the **Value** field, enter a number.</span></span> <span data-ttu-id="e0df6-150">この値は、隣のフィールドで選択された数量の仕様に関連します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-150">This value relates to the Quantity specification that's selected in the adjacent field.</span></span>  
6. <span data-ttu-id="e0df6-151">**プロセス** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-151">Expand or collapse the **Process** section.</span></span>
7. <span data-ttu-id="e0df6-152">**完全ブロック** チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-152">Select or clear the **Full blocking** check box.</span></span> <span data-ttu-id="e0df6-153">このオプションを選択した場合、テストに失敗すると、全部または注文明細行の数量はブロックされます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="e0df6-154">これを選択しない場合は、品質指示の品目のみがブロックされます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="e0df6-155">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-155">Click **Save**.</span></span>
9. <span data-ttu-id="e0df6-156">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-156">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="e0df6-157">*倉庫プロセスの品質管理* 機能により、その他の品目のサンプリング機能が追加されます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-157">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="e0df6-158">これにより、*品目サンプリング スコープ* の概念と、完全なライセンス プレートを数量指定として定義する機能が追加されます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-158">It adds a concept of *item sampling scope* and the ability to define a full license plate as the quantity specification.</span></span> <span data-ttu-id="e0df6-159">この機能を有効にした場合、詳細については [倉庫プロセスの品質管理](../quality-management-for-warehouses-processes.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0df6-159">If you have enabled this feature, then see [Quality management for warehouse processes](../quality-management-for-warehouses-processes.md) for details.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="e0df6-160">品質グループの作成</span><span class="sxs-lookup"><span data-stu-id="e0df6-160">Create a quality group</span></span>
1. <span data-ttu-id="e0df6-161">**在庫管理 > 設定 > 品質管理 > 品質グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-161">Go to **Inventory management > Setup > Quality control > Quality groups**.</span></span>
2. <span data-ttu-id="e0df6-162">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-162">Click **New**.</span></span>
3. <span data-ttu-id="e0df6-163">**品質グループ** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-163">In the **Quality group** field, type a value.</span></span> <span data-ttu-id="e0df6-164">グループにどのタイプの品目が含まれているかを識別しやすい記述名を使用します (サンプリングの基準)。</span><span class="sxs-lookup"><span data-stu-id="e0df6-164">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="e0df6-165">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-165">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="e0df6-166">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-166">Click **Save**.</span></span>
6. <span data-ttu-id="e0df6-167">**品目の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-167">Click **Add items**.</span></span>
7. <span data-ttu-id="e0df6-168">**品目番号** 行を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-168">Select the **Item number** row.</span></span> <span data-ttu-id="e0df6-169">この例では品目番号に基づいフィルタ処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-169">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="e0df6-170">**基準** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-170">In the **Criteria** field, type a value.</span></span> <span data-ttu-id="e0df6-171">たとえば、「T\*」と入力し、T で始まる品目番号にフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-171">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="e0df6-172">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-172">Click **OK**.</span></span>
10. <span data-ttu-id="e0df6-173">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-173">Click **OK**.</span></span>
11. <span data-ttu-id="e0df6-174">**品目品質グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-174">Click **Item quality groups**.</span></span>
12. <span data-ttu-id="e0df6-175">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-175">Close the page.</span></span>
13. <span data-ttu-id="e0df6-176">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-176">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="e0df6-177">テスト グループの作成</span><span class="sxs-lookup"><span data-stu-id="e0df6-177">Create a test group</span></span>
1. <span data-ttu-id="e0df6-178">**在庫管理 > 設定 > 品質管理 > テスト グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-178">Go to **Inventory management > Setup > Quality control > Test groups**.</span></span>
2. <span data-ttu-id="e0df6-179">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-179">Click **New**.</span></span>
3. <span data-ttu-id="e0df6-180">**テスト グループ** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-180">In the **Test group** field, type a value.</span></span> <span data-ttu-id="e0df6-181">どのようなテストが実行され、どの品質グループにテストを関連付ける必要があるかを覚えるのに役立つ名前を **テスト グループ** に指定します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-181">Give the **Test group** a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="e0df6-182">たとえば、これは "T" で開始する項目を選択する品質グループと一緒に使用され、"T 品目テスト" と呼ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-182">For example, it it's to be used with a quality group that selects items starting with "T", you could call it "T-item tests".</span></span>  
4. <span data-ttu-id="e0df6-183">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-183">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="e0df6-184">**品目サンプリング** フィールドで、以前に作成した品目サンプリング行を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-184">In the **Item sampling** field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="e0df6-185">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-185">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e0df6-186">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-186">Click **Add**.</span></span>
8. <span data-ttu-id="e0df6-187">**順序番号** フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-187">In the **Sequence number** field, enter a number.</span></span>
9. <span data-ttu-id="e0df6-188">**テスト** フィールドで、先ほど作成したテストを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-188">In the **Test** field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="e0df6-189">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-189">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="e0df6-190">**テスト** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-190">Click the **Test** tab.</span></span>
12. <span data-ttu-id="e0df6-191">**変数** フィールドで、以前に成したテストを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-191">In the **Variable** field, select the test variable that you created before</span></span>
13. <span data-ttu-id="e0df6-192">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-192">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="e0df6-193">**既定の結果** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-193">In the **Default outcome** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="e0df6-194">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-194">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="e0df6-195">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-195">Click **Save**.</span></span>
17. <span data-ttu-id="e0df6-196">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-196">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="e0df6-197">品質指示の作成時に定義する</span><span class="sxs-lookup"><span data-stu-id="e0df6-197">Define when quality orders will be created</span></span>
1. <span data-ttu-id="e0df6-198">**在庫管理 > 設定 > 品質管理 > 品質関連** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-198">Go to **Inventory management > Setup > Quality control > Quality associations**.</span></span>
2. <span data-ttu-id="e0df6-199">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-199">Click **New**.</span></span>
3. <span data-ttu-id="e0df6-200">**参照タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-200">In the **Reference type** field, select an option.</span></span>
4. <span data-ttu-id="e0df6-201">**品目コード** フィールドで「グループ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-201">In the **Item code** field, select 'Group'.</span></span> <span data-ttu-id="e0df6-202">この例では、"グループ" を選択し、以前に作成した品質グループを使用します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-202">In this example, we'll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="e0df6-203">手動で品目を指定するためには、これを「テーブル」と設定することもでき、または品質指示にすべての品目を追加するには「すべて」を選択できます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-203">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="e0df6-204">**品目コード** フィールドで、以前に作成した品質グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-204">In the **Item** field, select the quality group that you created before.</span></span> <span data-ttu-id="e0df6-205">品目フィールドで指定できるオプションは品目コードの設定内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e0df6-205">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="e0df6-206">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e0df6-207">[プロセス] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-207">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="e0df6-208">**イベント タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-208">In the **Event type** field, select an option.</span></span> <span data-ttu-id="e0df6-209">これはテストを発生させるイベントです。</span><span class="sxs-lookup"><span data-stu-id="e0df6-209">This is the event that triggers the test.</span></span> <span data-ttu-id="e0df6-210">ここで使用可能なオプションは参照タイプ フィールドで選択したプロセスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e0df6-210">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="e0df6-211">**実行** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-211">In the **Execution** field, select an option.</span></span>
10. <span data-ttu-id="e0df6-212">**品質指示プロセス** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-212">Expand or collapse the **Quality order process** section.</span></span>
11. <span data-ttu-id="e0df6-213">**イベント ブロッキング** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-213">In the **Event blocking** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="e0df6-214">このフィールドには、品質指示がまだ開いている場合に、ブロックできるプロセスの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-214">This field shows the list of processes that it's possible to block if the quality order is still open.</span></span> <span data-ttu-id="e0df6-215">オプションは、イベント タイプ フィールドの選択内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e0df6-215">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="e0df6-216">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-216">In the list, click the link in the selected row.</span></span> <span data-ttu-id="e0df6-217">これは、以前に選択した値によって異なってきます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-217">This will be depending on the previous selected values.</span></span> <span data-ttu-id="e0df6-218">未処理の品質指示を伝票明細行にリンクさせている間に次のプロセスをブロックする必要がある場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-218">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="e0df6-219">**詳細** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-219">Expand or collapse the **Specifications** section.</span></span>
14. <span data-ttu-id="e0df6-220">**テスト グループ** フィールドで、以前に作成したテスト グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-220">In the **Test group** field, select the test group that you created before.</span></span>
15. <span data-ttu-id="e0df6-221">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-221">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="e0df6-222">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0df6-222">Click **Save**.</span></span>
17. <span data-ttu-id="e0df6-223">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-223">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="e0df6-224">*倉庫プロセスの品質管理* 機能では、品質関連の設定のその他の追加オプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="e0df6-224">The *Quality management for warehouse processes* feature provides additional options for setting up quality associations.</span></span> <span data-ttu-id="e0df6-225">これは新しい条件 (**適用可能な倉庫タイプ**) と新しい設定 (**品質処理ポリシー**) が追加されます。</span><span class="sxs-lookup"><span data-stu-id="e0df6-225">It adds a new condition (**Applicable warehouse type**) and a new setting (**Quality processing policy**).</span></span> <span data-ttu-id="e0df6-226">この機能を有効にした場合、詳細については [倉庫プロセスの品質管理](../quality-management-for-warehouses-processes.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0df6-226">If you have enabled this feature, then see [Quality management for warehouse processes](../quality-management-for-warehouses-processes.md) for details.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]