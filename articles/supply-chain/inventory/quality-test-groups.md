---
title: 品質管理テスト グループ
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質指示で複数のテストに使用できるようテスト グループを作成する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 020a610e6a7e4d4b35ceb176d542bae32503a615
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021759"
---
# <a name="quality-management-test-groups"></a><span data-ttu-id="fe963-103">品質管理テスト グループ</span><span class="sxs-lookup"><span data-stu-id="fe963-103">Quality management test groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe963-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質指示で複数のテストに使用できるようテスト グループを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fe963-104">This topic describes how to create test groups, so that multiple tests can be used with quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="fe963-105">テスト グループと、それらに割り当てられる個別のテストを設定、編集、および表示するには、この **テスト グループ** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="fe963-105">You use the **Test groups** page to set up, edit, and view test groups and the individual tests that are assigned to them.</span></span> <span data-ttu-id="fe963-106">ページの上部パーツにはテスト グループが表示され、下部パーツには選択したテスト グループに割り当てられるテストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-106">The upper part of the page shows the test groups, and the lower part shows the tests that are assigned to a selected test group.</span></span>

<span data-ttu-id="fe963-107">テスト グループには、サンプリング計画、許容可能な品質レベル (AQL)、破壊試験の要件などの複数のポリシーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="fe963-107">You assign several policies to a test group, such as a sampling plan, an acceptable quality level (AQL), and the requirement for destructive testing.</span></span> <span data-ttu-id="fe963-108">そして、個別のテストをテスト グループに割り当てるときは、順序、ドキュメント、有効期間などの追加情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="fe963-108">Then, when you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="fe963-109">定量試験の場合、定義する情報には許容測定値も含まれます。</span><span class="sxs-lookup"><span data-stu-id="fe963-109">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="fe963-110">定性試験の場合、情報にはテスト変数と既定の結果が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fe963-110">For a qualitative test, the information includes the test variable and default outcome.</span></span>

<span data-ttu-id="fe963-111">品質指示に割り当てるテスト グループは、指定された品目に対して実行する必要がある既定のテストのセットを定義します。</span><span class="sxs-lookup"><span data-stu-id="fe963-111">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="fe963-112">ただし、品質指示のテストは、追加、削除、または変更できます。</span><span class="sxs-lookup"><span data-stu-id="fe963-112">However, you can add, delete, or change tests for the quality order.</span></span> <span data-ttu-id="fe963-113">テスト結果のレポートは、品質指示に対するそれぞれのテストに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-113">Test results are reported for each test on a quality order.</span></span>

<span data-ttu-id="fe963-114">テスト グループを定義する場合、必要に応じて品目サンプリングを指定できます。</span><span class="sxs-lookup"><span data-stu-id="fe963-114">When you define a test group, you can optionally specify an item sampling.</span></span> <span data-ttu-id="fe963-115">品目サンプリングは、テストする必要がある製品の量を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-115">Item samplings are used to define the amount of the product that must be tested.</span></span> <span data-ttu-id="fe963-116">詳細については、[品質管理の品目サンプリング](quality-item-sampling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe963-116">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span> <span data-ttu-id="fe963-117">テスト グループのテストが破壊試験であるかどうかを示す場合も指定できます。</span><span class="sxs-lookup"><span data-stu-id="fe963-117">You can also indicate whether the tests in a test group are destructive.</span></span> <span data-ttu-id="fe963-118">破壊試験では、品目サンプリングが破棄され、数量が手持在庫から削除されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-118">In a destructive test, the item sampling is destroyed, and the quantity is removed from the on-hand inventory.</span></span>

## <a name="example-of-a-test-group"></a><span data-ttu-id="fe963-119">テストグループの例</span><span class="sxs-lookup"><span data-stu-id="fe963-119">Example of a test group</span></span>

<span data-ttu-id="fe963-120">ある製造会社では、品質ガイドラインのバリエーションごとにテスト グループを定義します。</span><span class="sxs-lookup"><span data-stu-id="fe963-120">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="fe963-121">さまざまなテスト グループは、サンプリング計画、まとめて実行する必要があるテストのセット、AQL、およびその他の要因における違いを反映します。</span><span class="sxs-lookup"><span data-stu-id="fe963-121">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="fe963-122">定量試験の場合、許容測定値にも違いがあります。</span><span class="sxs-lookup"><span data-stu-id="fe963-122">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="fe963-123">品質ガイドラインを適用するには、会社は **品質関連** ページで品質指示を自動的に生成するために使用される各ルールにテスト グループを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe963-123">To enforce its quality guidelines, the company assigns a test group to each rule that is used to automatically generate quality orders on the **Quality associations** page.</span></span> <span data-ttu-id="fe963-124">また、手動で作成された品質指示にテスト グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="fe963-124">It also assigns a test group to quality orders that are manually created.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="fe963-125">テスト グループの作成</span><span class="sxs-lookup"><span data-stu-id="fe963-125">Create a test group</span></span>

<span data-ttu-id="fe963-126">テストグループを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fe963-126">To create a test group, follow these steps.</span></span>

1. <span data-ttu-id="fe963-127">**在庫管理 \> 設定 \> 品質テスト \> テスト グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fe963-127">Go to **Inventory management \> Setup \> Quality control \> Test groups**.</span></span>
1. <span data-ttu-id="fe963-128">アクション ペインで **新規** を選択して、ページ上部のグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="fe963-128">On the Action Pane, select **New** to add a row to the grid in the upper part of the page.</span></span> <span data-ttu-id="fe963-129">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="fe963-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="fe963-130">**テスト グループ** – テスト グループの固有の ID または名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="fe963-130">**Test group** – Enter a unique ID or name for the test group.</span></span>
    - <span data-ttu-id="fe963-131">**説明** – テスト グループの詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="fe963-131">**Description** – Enter a detailed description of the test group.</span></span>
    - <span data-ttu-id="fe963-132">**許容可能な品質レベル** – 合格と見なされるテストのグループに合格する必要があるテスト結果の合計割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="fe963-132">**Acceptable quality level** – Enter the total percentage of test results that must pass for the group of tests to be considered passed.</span></span>
    - <span data-ttu-id="fe963-133">**品目サンプリング** – 品目サンプリングを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-133">**Item sampling** – Select an item sampling.</span></span> <span data-ttu-id="fe963-134">詳細については、[品質管理の品目サンプリング](quality-item-sampling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe963-134">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>
    - <span data-ttu-id="fe963-135">**破壊試験** – テストされた品目を破壊するテスト グループの場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="fe963-135">**Destructive** – Select this check box to indicate that the test group will destroy the items that are tested.</span></span>

1. <span data-ttu-id="fe963-136">新しい行を選択しながら、ページの上部にある **一般** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-136">While the new row is still selected, select the **General** tab in the upper part of the page.</span></span> <span data-ttu-id="fe963-137">**概要** タブで選択したテスト グループの設定の一部がここで繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-137">Some of the settings for the test group that is selected on the **Overview** tab are repeated here.</span></span> <span data-ttu-id="fe963-138">さらに、グループに次のフィールドを設定できます。</span><span class="sxs-lookup"><span data-stu-id="fe963-138">In addition, you can set the following fields for the group:</span></span>

    - <span data-ttu-id="fe963-139">**在庫バッチ属性の更新** – このオプションを *はい* に設定すると、ページ下部にあるテスト グループに追加された新しい各テストが、自動的に *はい* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-139">**Update inventory batch attribute** – When you set this option to *Yes* here, it will automatically be set to *Yes* for every new test that is added to the test group in the lower part of the page.</span></span>
    - <span data-ttu-id="fe963-140">**バッチ廃棄の更新** – このオプションを *はい* に設定すると、テスト中の品目がバッチ管理されている場合は、**失敗した品質指示のバッチ廃棄** フィールドまたは **合格した品質指示バッチ廃棄** フィールドで選択した値でバッチ廃棄が自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-140">**Update batch disposition** – When you set this option to *Yes*, if the item that is being tested is batch controlled, the batch disposition will automatically be updated with the value that is selected in the **Failed quality order batch disposition** or **Passed quality order batch disposition** field.</span></span>
    - <span data-ttu-id="fe963-141">**失敗した品質指示バッチ廃棄** – このテスト グループを含む品質指示が AQL を満たしておらず失敗した場合に割り当てるバッチ廃棄コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-141">**Failed quality order batch disposition** – Select the batch disposition code that should be assigned when a quality order that includes this test group fails because it doesn't meet the AQL.</span></span>
    - <span data-ttu-id="fe963-142">**合格した品質指示バッチ廃棄** – このテスト グループを含む品質指示が AQL を満たして合格した場合に割り当てるバッチ廃棄コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-142">**Passed quality order batch disposition** – Select the batch disposition code that should be assigned when a quality order that includes this test group passes because it meets the AQL.</span></span>
    - <span data-ttu-id="fe963-143">**在庫ステータスの更新** – このオプションを *はい* に設定すると、テスト中の品目の保管分析コード グループで **在庫ステータス** が有効になっている場合は、**失敗した品質指示のステータス** または **合格した品質指示のステータス** フィールドで選択されているステータスに自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-143">**Update inventory status** – When you set this option to *Yes*, if **Inventory status** is enabled on the storage dimension group for the item that is being tested, the status will automatically be updated with the status that is selected in the **Failed quality order status** or **Passed quality order status** field.</span></span>
    - <span data-ttu-id="fe963-144">**失敗した品質指示ステータス** – このテスト グループを含む品質指示が AQL を満たしておらず失敗した場合に品目に割り当てる在庫ステータスを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-144">**Failed quality order status** – Select the inventory status that should be assigned to the item when a quality order that includes this test group fails because it doesn't meet the AQL.</span></span>
    - <span data-ttu-id="fe963-145">**成功した品質指示ステータス** – このテスト グループを含む品質指示が AQL を満たし成功した場合に品目に割り当てる在庫ステータスを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-145">**Passed quality order status** – Select the inventory status that should be assigned to the item when a quality order that includes this test group passes because it meets the AQL.</span></span>

## <a name="add-a-qualitative-test-to-a-test-group"></a><span data-ttu-id="fe963-146">テスト グループへの定性試験の追加</span><span class="sxs-lookup"><span data-stu-id="fe963-146">Add a qualitative test to a test group</span></span>

<span data-ttu-id="fe963-147">テスト グループに定性試験を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fe963-147">To add a qualitative test to a test group, follow these steps.</span></span>

1. <span data-ttu-id="fe963-148">**在庫管理 \> 設定 \> 品質テスト \> テスト グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fe963-148">Go to **Inventory management \> Setup \> Quality control \> Test groups**.</span></span>
1. <span data-ttu-id="fe963-149">ページの上部にある **概要** タブで、テストを追加するテスト グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-149">On the **Overview** tab in the upper part of the page, select the test group that you want to add a test to.</span></span>
1. <span data-ttu-id="fe963-150">ページの下部の **概要** タブで、ツールバーの **追加** を選択して、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="fe963-150">In the lower part of the page, on the **Overview** tab, select **Add** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="fe963-151">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="fe963-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="fe963-152">**順序番号** – テストの実行順序を指定する整数を入力します。</span><span class="sxs-lookup"><span data-stu-id="fe963-152">**Sequence number** – Enter an integer to specify the order that the tests should be performed in.</span></span> <span data-ttu-id="fe963-153">小さい順序番号のテストは、順序番号が大きいテストの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-153">Tests that have smaller sequence numbers will be run before tests that have larger sequence numbers.</span></span>

        > [!NOTE]
        > <span data-ttu-id="fe963-154">順序番号間には間隔を残すことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fe963-154">We recommend that you leave a gap between sequence numbers.</span></span> <span data-ttu-id="fe963-155">たとえば、最初のテストでは **順序番号** フィールドを *10* に設定し、追加のテストごとに値を 10 ずつ増分します。</span><span class="sxs-lookup"><span data-stu-id="fe963-155">For example, set the **Sequence number** field to *10* for your first test, and then increment the value by 10 for each additional test.</span></span> <span data-ttu-id="fe963-156">この方法で、目的の順序に合わせるために行を削除および再作成することなく後から新しいテストを追加できます。</span><span class="sxs-lookup"><span data-stu-id="fe963-156">In this way, you can add new tests later without having to delete and re-create the lines to put them in the desired order.</span></span>

    - <span data-ttu-id="fe963-157">**テスト** – 実行するテストを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-157">**Test** – Select the test that you want to perform.</span></span> <span data-ttu-id="fe963-158">定性試験の場合は、**タイプ** フィールドが *オプション* に設定されているテストを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-158">For a qualitative test, select a test where the **Type** field is set to *Option*.</span></span>
    - <span data-ttu-id="fe963-159">**開始** – テストが有効となる最初の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-159">**Effective** – Select the first date when the test is valid.</span></span> <span data-ttu-id="fe963-160">このフィールドを空白のままにした場合、制限はありません。</span><span class="sxs-lookup"><span data-stu-id="fe963-160">If you leave this field blank, there is no limit.</span></span>
    - <span data-ttu-id="fe963-161">**終了** – テストが有効となる最後の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-161">**Expiration** – Select the last date when the test is valid.</span></span> <span data-ttu-id="fe963-162">このフィールドを空白のままにした場合、または *なし* に設定した場合、制限はありません。</span><span class="sxs-lookup"><span data-stu-id="fe963-162">If you leave this field blank or set it to *Never*, there is no limit.</span></span>
    - <span data-ttu-id="fe963-163">**テスト値の決定** – 同じテストについて複数の結果が記録された場合に、AQL を決定する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-163">**Test value determination** – Select how an AQL should be determined when multiple results are recorded for the same test.</span></span> <span data-ttu-id="fe963-164">定性試験では、*手動* のみを選択できます。</span><span class="sxs-lookup"><span data-stu-id="fe963-164">For a qualitative test, only *Manual* can be selected.</span></span> <span data-ttu-id="fe963-165">その他の値 (*平均*、*最小*、または *最大*) のいずれかを選択した場合、テスト グループを保存するときにエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-165">If you select one of the other values (*Average*, *Minimum*, or *Maximum*), you will receive an error message when you save the test group.</span></span>
    - <span data-ttu-id="fe963-166">**属性** – バッチ属性のテスト結果を記録する場合は、ここで属性を選択し、**在庫バッチ属性の更新** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="fe963-166">**Attribute** – If you want to record test results on a batch attribute, select the attribute here, and select the **Update inventory batch attribute** check box.</span></span>
    - <span data-ttu-id="fe963-167">**在庫バッチ属性の更新** – **属性** フィールドで選択されているバッチ属性のテスト結果を記録する場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="fe963-167">**Update inventory batch attribute** – Select this check box to record test results for the batch attribute that is selected in the **Attribute** field.</span></span>

1. <span data-ttu-id="fe963-168">ページの下部で、**一般** タブを選択します。**概要** タブで選択したテストの設定の一部がここで繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-168">In the lower part of the page, select the **General** tab. Some of the settings for the test that is selected on the **Overview** tab are repeated here.</span></span> <span data-ttu-id="fe963-169">さらに、テストに次のフィールドを設定できます。</span><span class="sxs-lookup"><span data-stu-id="fe963-169">In addition, you can set the following fields for the test:</span></span>

    - <span data-ttu-id="fe963-170">**分析証明レポート** – テスト結果を分析証明 (CoA) に印刷する必要がある場合は、このオプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="fe963-170">**Certificate of analysis report** – Set this option to *Yes* to indicate that the test results should be printed on the certificate of analysis (CoA).</span></span> <span data-ttu-id="fe963-171">このレポートは品質指示から生成できます。</span><span class="sxs-lookup"><span data-stu-id="fe963-171">This report can be generated from the quality order.</span></span>
    - <span data-ttu-id="fe963-172">**失敗に対するアクション** – *承認* または *不合格* のどちらかを選択して、そのテストの AQL が満たされていない場合にテストを合格にするか不合格にするかを指定します。</span><span class="sxs-lookup"><span data-stu-id="fe963-172">**Action on failure** – Select either *Accept* or *Fail* to indicate whether the test should pass or fail if the AQL for it isn't met.</span></span>
    - <span data-ttu-id="fe963-173">**許容可能な品質レベル** – 合格と見なされるテストに合格する必要があるテスト結果の合計割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="fe963-173">**Acceptable quality level** – Enter the total percentage of test results that must pass for the test to be considered passed.</span></span>

1. <span data-ttu-id="fe963-174">ページの下部にある **テスト** タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="fe963-174">In the lower part of the page, on the **Test** tab, set the following fields:</span></span>

    - <span data-ttu-id="fe963-175">**変数** – 定性試験を記録するテスト変数を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-175">**Variable** – Select the test variable to record the qualitative test results for.</span></span>
    - <span data-ttu-id="fe963-176">**既定の結果** – テスト結果を記録する既定の結果を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-176">**Default outcome** – Select the default outcome that should be recorded for the test results.</span></span>
    - <span data-ttu-id="fe963-177">**テスト機器** – テストに使用するデバイスを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-177">**Test instrument** – Select the device that should be used for the test.</span></span> <span data-ttu-id="fe963-178">テスト機器が定義されている場合は、テスト グループ内のテストに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-178">If a test instrument is defined, it's automatically entered for the test in the test group.</span></span>

1. <span data-ttu-id="fe963-179">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fe963-179">Close the page.</span></span>

## <a name="add-a-quantitative-test-to-a-test-group"></a><span data-ttu-id="fe963-180">テスト グループへの定量試験の追加</span><span class="sxs-lookup"><span data-stu-id="fe963-180">Add a quantitative test to a test group</span></span>

<span data-ttu-id="fe963-181">テスト グループに定量試験を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fe963-181">To add a quantitative test to a test group, follow these steps.</span></span>

1. <span data-ttu-id="fe963-182">**在庫管理 \> 設定 \> 品質テスト \> テスト グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fe963-182">Go to **Inventory management \> Setup \> Quality control \> Test groups**.</span></span>
1. <span data-ttu-id="fe963-183">ページの上部にある **概要** タブで、テストを追加するテスト グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-183">On the **Overview** tab in the upper part of the page, select the test group that you want to add a test to.</span></span>
1. <span data-ttu-id="fe963-184">ページの下部の **概要** タブで、ツールバーの **追加** を選択して、グリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="fe963-184">In the lower part of the page, on the **Overview** tab, select **Add** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="fe963-185">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="fe963-185">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="fe963-186">**順序番号** – テストの実行順序を指定する整数を入力します。</span><span class="sxs-lookup"><span data-stu-id="fe963-186">**Sequence number** – Enter an integer to specify the order that the tests should be performed in.</span></span> <span data-ttu-id="fe963-187">小さい順序番号のテストは、順序番号が大きいテストの前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-187">Tests that have smaller sequence numbers will be run before tests that have larger sequence numbers.</span></span>

        > [!NOTE]
        > <span data-ttu-id="fe963-188">順序番号間には間隔を残すことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fe963-188">We recommend that you leave a gap between sequence numbers.</span></span> <span data-ttu-id="fe963-189">たとえば、最初のテストでは **順序番号** フィールドを *10* に設定し、追加のテストごとに値を 10 ずつ増分します。</span><span class="sxs-lookup"><span data-stu-id="fe963-189">For example, set the **Sequence number** field to *10* for your first test, and then increment the value by 10 for each additional test.</span></span> <span data-ttu-id="fe963-190">この方法で、目的の順序に合わせるために行を削除および再作成することなく後から新しいテストを追加できます。</span><span class="sxs-lookup"><span data-stu-id="fe963-190">In this way, you can add new tests later without having to delete and re-create the lines to put them in the desired order.</span></span>

    - <span data-ttu-id="fe963-191">**テスト** – 実行するテストを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-191">**Test** – Select the test that you want to perform.</span></span> <span data-ttu-id="fe963-192">定量試験の場合は、**タイプ** フィールドが *分数* または *整数* に設定されているテストを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-192">For a quantitative test, select a test where the **Type** field is set to *Fraction* or *Integer*.</span></span>
    - <span data-ttu-id="fe963-193">**開始** – テストが有効となる最初の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-193">**Effective** – Select the first date when the test is valid.</span></span> <span data-ttu-id="fe963-194">このフィールドを空白のままにした場合、制限はありません。</span><span class="sxs-lookup"><span data-stu-id="fe963-194">If you leave this field blank, there is no limit.</span></span>
    - <span data-ttu-id="fe963-195">**終了** – テストが有効となる最後の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-195">**Expiration** – Select the last date when the test is valid.</span></span> <span data-ttu-id="fe963-196">このフィールドを空白のままにした場合、または *なし* に設定した場合、制限はありません。</span><span class="sxs-lookup"><span data-stu-id="fe963-196">If you leave this field blank or set it to *Never*, there is no limit.</span></span>
    - <span data-ttu-id="fe963-197">**テスト値の決定** – 同じテストについて複数の結果が記録された場合に、AQL を決定する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-197">**Test value determination** – Select how an AQL should be determined when multiple results are recorded for the same test.</span></span> <span data-ttu-id="fe963-198">利用できるオプションには、*平均*、*最小*、*最大*、および *手動* があります。</span><span class="sxs-lookup"><span data-stu-id="fe963-198">The available options are *Average*, *Minimum*, *Maximum*, and *Manual*.</span></span>
    - <span data-ttu-id="fe963-199">**属性** – バッチ属性のテスト結果を記録する場合は、ここで属性を選択し、**在庫バッチ属性の更新** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="fe963-199">**Attribute** – If you want to record test results on a batch attribute, select the attribute here, and select the **Update inventory batch attribute** check box.</span></span>
    - <span data-ttu-id="fe963-200">**在庫バッチ属性の更新** – **属性** フィールドで選択されているバッチ属性のテスト結果を記録する場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="fe963-200">**Update inventory batch attribute** – Select this check box to record test results for the batch attribute that is selected in the **Attribute** field.</span></span>

1. <span data-ttu-id="fe963-201">ページの下部で、**一般** タブを選択します。**概要** タブで選択したテストの設定の一部がここで繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-201">In the lower part of the page, select the **General** tab. Some of the settings for the test that is selected on the **Overview** tab are repeated here.</span></span> <span data-ttu-id="fe963-202">さらに、テストに次のフィールドを設定できます。</span><span class="sxs-lookup"><span data-stu-id="fe963-202">In addition, you can set the following fields for the test:</span></span>

    - <span data-ttu-id="fe963-203">**分析証明レポート** – テスト結果を分析証明 (CoA) に印刷する必要がある場合は、このオプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="fe963-203">**Certificate of analysis report** – Set this option to *Yes* to indicate that the test results should be printed on the CoA.</span></span> <span data-ttu-id="fe963-204">このレポートは品質指示から生成できます。</span><span class="sxs-lookup"><span data-stu-id="fe963-204">This report can be generated from the quality order.</span></span>
    - <span data-ttu-id="fe963-205">**失敗に対するアクション** – *承認* または *不合格* のどちらかを選択して、そのテストの AQL が満たされていない場合にテストを合格にするか不合格にするかを指定します。</span><span class="sxs-lookup"><span data-stu-id="fe963-205">**Action on failure** – Select either *Accept* or *Fail* to indicate whether the test should pass or fail if the AQL for it isn't met.</span></span>
    - <span data-ttu-id="fe963-206">**許容可能な品質レベル** – 合格と見なされるテストに合格する必要があるテスト結果の合計割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="fe963-206">**Acceptable quality level** – Enter the total percentage of test results that must pass for the test to be considered passed.</span></span>

1. <span data-ttu-id="fe963-207">ページの下部にある **テスト** タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="fe963-207">In the lower part of the page, on the **Test** tab, set the following fields:</span></span>

    - <span data-ttu-id="fe963-208">**標準** – テスト結果の予想される量 (整数または分数) を入力します。</span><span class="sxs-lookup"><span data-stu-id="fe963-208">**Standard** – Enter the amount (integer or fraction) that is expected for the test results.</span></span> <span data-ttu-id="fe963-209">既定では、入力した値がテスト結果に入力されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-209">The value that you enter will be entered by default in the test results.</span></span> <span data-ttu-id="fe963-210">また、**最小** フィールドと **最大** フィールドには自動的に既定値として入力されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-210">Additionally, it will automatically be entered as a default value in the **Min** and **Max** fields.</span></span>
    - <span data-ttu-id="fe963-211">**最小** – テスト結果の最小値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fe963-211">**Min** – Enter the minimum allowed value for the test results.</span></span> <span data-ttu-id="fe963-212">入力する値は、**標準** フィールドに設定されている金額よりも小さい値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe963-212">The value that you enter must be less than the amount that is set in the **Standard** field.</span></span> <span data-ttu-id="fe963-213">**最小** フィールドを更新すると、**最小許容範囲 (%)** フィールドが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-213">When you update the **Min** field, the **Min tolerance (%)** field is automatically updated.</span></span> <span data-ttu-id="fe963-214">**最小許容範囲 (%)** フィールドを更新すると、**最小** フィールドが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-214">Likewise, when you update the **Min tolerance (%)** field, the **Min** field is automatically updated.</span></span>
    - <span data-ttu-id="fe963-215">**最大** – テスト結果の最大値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fe963-215">**Max** – Enter the maximum allowed value for the test results.</span></span> <span data-ttu-id="fe963-216">入力する値は、**標準** フィールドに設定されている金額よりも大きい値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe963-216">The value that you enter must be more than the amount that is set in the **Standard** field.</span></span> <span data-ttu-id="fe963-217">**最大** フィールドを更新すると、**最大許容範囲 (%)** フィールドが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-217">When you update the **Max** field, the **Max tolerance (%)** field is automatically updated.</span></span> <span data-ttu-id="fe963-218">**最大許容範囲 (%)** フィールドを更新すると、**最大** フィールドが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-218">Likewise, when you update the **Max tolerance (%)** field, the **Max** field is automatically updated.</span></span>
    - <span data-ttu-id="fe963-219">**テスト機器** – テストに使用するデバイスを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe963-219">**Test instrument** – Select the device that should be used for the test.</span></span> <span data-ttu-id="fe963-220">テスト機器が定義されている場合は、テスト グループ内のテストに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="fe963-220">If a test instrument is defined, it's automatically entered for the test in the test group.</span></span>

1. <span data-ttu-id="fe963-221">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fe963-221">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe963-222">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fe963-222">Additional resources</span></span>

- [<span data-ttu-id="fe963-223">品質管理テスト機器</span><span class="sxs-lookup"><span data-stu-id="fe963-223">Quality management test instruments</span></span>](quality-management-processes.md)
- [<span data-ttu-id="fe963-224">品質管理テスト</span><span class="sxs-lookup"><span data-stu-id="fe963-224">Quality management tests</span></span>](quality-management-processes.md)
- [<span data-ttu-id="fe963-225">品質管理テスト変数</span><span class="sxs-lookup"><span data-stu-id="fe963-225">Quality management test variables</span></span>](quality-management-processes.md)
- [<span data-ttu-id="fe963-226">品質関連</span><span class="sxs-lookup"><span data-stu-id="fe963-226">Quality associations</span></span>](quality-management-processes.md)
- [<span data-ttu-id="fe963-227">バッチ属性 (複数)</span><span class="sxs-lookup"><span data-stu-id="fe963-227">Batch attributes</span></span>](/supply-chain/production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]