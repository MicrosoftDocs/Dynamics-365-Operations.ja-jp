---
title: 使用権資産の減損
description: このトピックでは、Accounting Standards Codification Topic 842 (ASC 842) オペレーティング リースの減損を記録し、資産減価償却スケジュールを調整する機能について説明します。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3b648075a681fb01720149aac4f479dccf963489
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229529"
---
# <a name="impair-right-of-use-assets"></a><span data-ttu-id="dc1a9-103">使用権資産の減損</span><span class="sxs-lookup"><span data-stu-id="dc1a9-103">Impair right-of-use assets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc1a9-104">使用権 (ROU) 資産のキャリー額を回収できない場合は、資産が不足していないかどうかをテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-104">If a right-of-use (ROU) asset's carrying amount isn't recoverable, you might have to test whether the asset is impaired.</span></span> <span data-ttu-id="dc1a9-105">資産が損なわれていると判断した場合は、資産リースによって減損を記録し、それに応じて減価償却スケジュールを調整することができます。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-105">If you determine that the asset is impaired, Asset leasing can record the impairment and adjust the depreciation schedule accordingly.</span></span> <span data-ttu-id="dc1a9-106">このトピックでは、Accounting Standards Codification Topic 842 (ASC 842) オペレーティング リースの減損を記録し、減価償却スケジュールを調整する機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-106">This topic describes the functionality that records the impairment and adjusts the depreciation schedule of an Accounting Standards Codification Topic 842 (ASC 842) operating lease.</span></span> <span data-ttu-id="dc1a9-107">Financial Reporting Standard 16 (IFRS 16) リースにも同じ方法が適用されます。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-107">The same method also applies to International Financial Reporting Standard 16 (IFRS 16) leases.</span></span>

<span data-ttu-id="dc1a9-108">使用権資産の残余残高は、残りの期間の数のために定額法で償却され、リースが IFRS 16 でのファイナンス リースとして分類されているか、ASC 842 のオペレーティングリースであるかどうかにかかわらず、償却されます。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-108">The remaining balance of the ROU asset will be amortized on a straight-line basis for the number of periods that remain, regardless of whether the lease was classified as a finance lease under IFRS 16 or an operating lease under ASC 842.</span></span>

## <a name="impair-an-rou-asset"></a><span data-ttu-id="dc1a9-109">使用権資産の減損</span><span class="sxs-lookup"><span data-stu-id="dc1a9-109">Impair an ROU asset</span></span>

1. <span data-ttu-id="dc1a9-110">減損されたリースに移動し、**書籍** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-110">Go to the impaired lease, and select **Books**.</span></span>
2. <span data-ttu-id="dc1a9-111">アクション ペインで、**減損** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-111">On the Action Pane, select **Impairment**.</span></span>
3. <span data-ttu-id="dc1a9-112">表示されるダイアログボックスの **減損損失** フィールドに、資産減損の量を入力します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-112">In the dialog box that appears, in the **Impairment amount** field, enter the amount of the asset impairment.</span></span> <span data-ttu-id="dc1a9-113">使用権資産を減らすには、正の値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-113">To decrease the ROU asset, you should enter a positive value.</span></span>
4. <span data-ttu-id="dc1a9-114">**トランザクションの日付** フィールドに、減損エントリを転記する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-114">In the **Transaction date** field, enter the date when the impairment entry should be posted.</span></span>
5. <span data-ttu-id="dc1a9-115">**残りの期間** フィールドに、償却する残りの月数を入力します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-115">In the **Periods remaining** field, enter the remaining number of months to amortize.</span></span>
6. <span data-ttu-id="dc1a9-116">障減損経費仕訳入力をシステムで自動的に転記する場合は、**転記** パラメータをオンにします。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-116">Turn on the **Post** parameter if you want the system to automatically post the impairment expense journal entry.</span></span> <span data-ttu-id="dc1a9-117">このパラメーターをオフのままにした場合は、エントリが作成されますが、転記は行われません。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-117">If you leave this parameter turned off, the system creates the entry but doesn't post it.</span></span> <span data-ttu-id="dc1a9-118">その後、**資産のリース仕訳帳** ページからエントリを転記できます。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-118">You can then post the entry from the **Asset lease journals** page.</span></span>
7. <span data-ttu-id="dc1a9-119">入力または転記の前に提示されたエントリを表示するには、**転記前にプレビューする** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-119">Set the **Preview before posting** option to **Yes** to view the proposed entry before it's created or posted.</span></span>
8. <span data-ttu-id="dc1a9-120">**帳簿の終了** オプションを **はい** に設定すると、リース帳簿が閉じます。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-120">Set the **Close book** option to **Yes** to close the lease book.</span></span> <span data-ttu-id="dc1a9-121">このアクションを元に戻すことはできません。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-121">You can't undo this action.</span></span> <span data-ttu-id="dc1a9-122">終了したリースに対してエントリを転記することはできず、終了したリースを調整することもできません。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-122">Entries can't be posted against closed leases, and closed leases can't be adjusted.</span></span>
9. <span data-ttu-id="dc1a9-123">**OK** を選択すると、減損エントリが作成または転記されます。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-123">Select **OK** to create or post the impairment entry.</span></span>
10. <span data-ttu-id="dc1a9-124">減損資産の減価償却スケジュールを表示するには、そのリース帳簿の資産減価償却スケジュールを開きます。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-124">To view the impaired asset depreciation schedule, open the asset depreciation schedule for that lease book.</span></span> <span data-ttu-id="dc1a9-125">これで、**残りの期間** フィールドに入力した月数で資産が定額法で償却されます。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-125">The asset will now be depreciated on a straight-line basis over the number of months that you entered in the **Periods remaining** field.</span></span>
11. <span data-ttu-id="dc1a9-126">減損経費仕訳入力を表示するには、減損したリース帳簿のアクション ペインで、**固定資産のリース仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-126">To view the impairment expense journal entry, select **Asset leasing journal** on the Action Pane of the impaired lease book.</span></span> <span data-ttu-id="dc1a9-127">システムによって、減損の経費転記勘定の借方に転記される仕訳入力と、リース資産の転記勘定が作成されます。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-127">The system creates a journal entry that debits the impairment expense posting account and credits the lease asset posting account.</span></span>
12. <span data-ttu-id="dc1a9-128">使用権資産の新しいキャリー額を表示するには、リース帳簿のアクション ペインで **資産トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-128">To view the new carrying value of the ROU asset, select **Asset transactions** on the Action Pane of the lease book.</span></span>

## <a name="example-of-rou-asset-impairment"></a><span data-ttu-id="dc1a9-129">使用権資産減損の例</span><span class="sxs-lookup"><span data-stu-id="dc1a9-129">Example of ROU asset impairment</span></span>

<span data-ttu-id="dc1a9-130">この例では、リースは特殊な資産ではないので、所有権を移転したり、賃借人に購入を許可したりすることはありません。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-130">For this example, the lease is a non-specialized asset that doesn't transfer ownership or grant the lessee the option to purchase.</span></span>

### <a name="setup"></a><span data-ttu-id="dc1a9-131">段取り</span><span class="sxs-lookup"><span data-stu-id="dc1a9-131">Setup</span></span>

<span data-ttu-id="dc1a9-132">以下の表は、この例で使用したリースの、**一般** と **支払スケジュール明細行** タブに設定されている値を示しています。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-132">The following tables show the values that are set on the **General** and **Payment schedule lines** tabs for the lease that is used in this example.</span></span>

<span data-ttu-id="dc1a9-133">**全般タブ**</span><span class="sxs-lookup"><span data-stu-id="dc1a9-133">**General tab**</span></span>

| <span data-ttu-id="dc1a9-134">フィールド</span><span class="sxs-lookup"><span data-stu-id="dc1a9-134">Field</span></span>                      | <span data-ttu-id="dc1a9-135">先頭値</span><span class="sxs-lookup"><span data-stu-id="dc1a9-135">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="dc1a9-136">資産の公正価値</span><span class="sxs-lookup"><span data-stu-id="dc1a9-136">Fair value of the asset</span></span>    | <span data-ttu-id="dc1a9-137">600,000</span><span class="sxs-lookup"><span data-stu-id="dc1a9-137">600,000</span></span>          |
| <span data-ttu-id="dc1a9-138">追加借入利子率</span><span class="sxs-lookup"><span data-stu-id="dc1a9-138">Incremental borrowing rate</span></span> | <span data-ttu-id="dc1a9-139">7%</span><span class="sxs-lookup"><span data-stu-id="dc1a9-139">7%</span></span>               |
| <span data-ttu-id="dc1a9-140">複合間隔</span><span class="sxs-lookup"><span data-stu-id="dc1a9-140">Compounding interval</span></span>       | <span data-ttu-id="dc1a9-141">毎年</span><span class="sxs-lookup"><span data-stu-id="dc1a9-141">Annually</span></span>         |
| <span data-ttu-id="dc1a9-142">資産の耐用年数 (月単位)</span><span class="sxs-lookup"><span data-stu-id="dc1a9-142">Asset useful life (months)</span></span> | <span data-ttu-id="dc1a9-143">600</span><span class="sxs-lookup"><span data-stu-id="dc1a9-143">600</span></span>              |
| <span data-ttu-id="dc1a9-144">定期支払のタイプ</span><span class="sxs-lookup"><span data-stu-id="dc1a9-144">Annuity type</span></span>               | <span data-ttu-id="dc1a9-145">通常の定期支払</span><span class="sxs-lookup"><span data-stu-id="dc1a9-145">Ordinary annuity</span></span> |
| <span data-ttu-id="dc1a9-146">開始日</span><span class="sxs-lookup"><span data-stu-id="dc1a9-146">Commencement date</span></span>          | <span data-ttu-id="dc1a9-147">2019 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="dc1a9-147">01/01/2019</span></span>       |

<span data-ttu-id="dc1a9-148">**支払スケジュール明細行タブ**</span><span class="sxs-lookup"><span data-stu-id="dc1a9-148">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="dc1a9-149">フィールド</span><span class="sxs-lookup"><span data-stu-id="dc1a9-149">Field</span></span>             | <span data-ttu-id="dc1a9-150">先頭値</span><span class="sxs-lookup"><span data-stu-id="dc1a9-150">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="dc1a9-151">開始日</span><span class="sxs-lookup"><span data-stu-id="dc1a9-151">Start date</span></span>        | <span data-ttu-id="dc1a9-152">2019 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="dc1a9-152">1/1/2019</span></span>   |
| <span data-ttu-id="dc1a9-153">間隔</span><span class="sxs-lookup"><span data-stu-id="dc1a9-153">Period interval</span></span>   | <span data-ttu-id="dc1a9-154">月 1 回</span><span class="sxs-lookup"><span data-stu-id="dc1a9-154">Monthly</span></span>    |
| <span data-ttu-id="dc1a9-155">期間</span><span class="sxs-lookup"><span data-stu-id="dc1a9-155">Periods</span></span>           | <span data-ttu-id="dc1a9-156">120</span><span class="sxs-lookup"><span data-stu-id="dc1a9-156">120</span></span>        |
| <span data-ttu-id="dc1a9-157">終了日</span><span class="sxs-lookup"><span data-stu-id="dc1a9-157">End date</span></span>          | <span data-ttu-id="dc1a9-158">2028 年 12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="dc1a9-158">12/31/2028</span></span> |
| <span data-ttu-id="dc1a9-159">支払頻度</span><span class="sxs-lookup"><span data-stu-id="dc1a9-159">Payment frequency</span></span> | <span data-ttu-id="dc1a9-160">毎年</span><span class="sxs-lookup"><span data-stu-id="dc1a9-160">Annually</span></span>   |
| <span data-ttu-id="dc1a9-161">支払額</span><span class="sxs-lookup"><span data-stu-id="dc1a9-161">Payment amount</span></span>    | <span data-ttu-id="dc1a9-162">10,000</span><span class="sxs-lookup"><span data-stu-id="dc1a9-162">10,000</span></span>     |

### <a name="steps"></a><span data-ttu-id="dc1a9-163">ステップ</span><span class="sxs-lookup"><span data-stu-id="dc1a9-163">Steps</span></span>

1. <span data-ttu-id="dc1a9-164">このトピックで既に説明したようにリースを作成した後、リース帳簿に移動し、支払スケジュールを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-164">After you create the lease as described earlier in this topic, go to the lease book, and confirm the payment schedule.</span></span> <span data-ttu-id="dc1a9-165">次に、初期認識仕訳入力を転記します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-165">Then post the initial recognition journal entry.</span></span> <span data-ttu-id="dc1a9-166">初期の使用権資産とリース負債は $70,235.81 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-166">The initial ROU asset and lease liability should be $70,235.81.</span></span> <span data-ttu-id="dc1a9-167">この例では、リースは ASC 842 の下ではオペレーティング リースとして分類されていました。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-167">For this example, the lease was classified as an operating lease under ASC 842.</span></span>
2. <span data-ttu-id="dc1a9-168">バッチ仕訳プロセスを 3 回実行して、リース支払、支払い利息、および減価償却費に対する 3 年間の通過をシミュレーションします。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-168">Run the batch journal process three times to simulate the passage of three years for the lease payments, interest expenses, and depreciation expenses.</span></span>
3. <span data-ttu-id="dc1a9-169">3 つのバッチジョブすべての実行が完了したら、リース帳簿に戻り、負債 テーブルと資産トランザクション テーブルを開いて、使用権資産とリース負債の現在のキャリー金額を表示します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-169">After you've finished running all three batch jobs, go back to the lease book, and open the liability and asset transactions tables to view the current carrying value of the ROU asset and lease liability.</span></span> <span data-ttu-id="dc1a9-170">3 年後、負債の値は約 $-53,893.00となり、資産の値はおよそ $53,893.00である必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-170">After three years, the value of the liability should be approximately $-53,893.00, and the value of the asset should be approximately $53,893.00.</span></span> 

    <span data-ttu-id="dc1a9-171">3 年間を通じて、業務における減損テストが行われ、使用権資産に $35,000 の減損があると判断されます。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-171">After three years, the business does impairment tests and determines that the ROU asset has an impairment of $35,000.</span></span> <span data-ttu-id="dc1a9-172">ここで、この減損を記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-172">You must now record this impairment.</span></span>
    
4. <span data-ttu-id="dc1a9-173">リース帳簿に移動し、アクション ペインで **減損** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-173">Go to the lease book, and then, on the Action Pane, select **Impairment**.</span></span>
5. <span data-ttu-id="dc1a9-174">**減損のパラメータ** ページで、次の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-174">On the **Impairment parameter** page, enter the following details.</span></span>

    | <span data-ttu-id="dc1a9-175">フィールド</span><span class="sxs-lookup"><span data-stu-id="dc1a9-175">Field</span></span>                  | <span data-ttu-id="dc1a9-176">先頭値</span><span class="sxs-lookup"><span data-stu-id="dc1a9-176">Value</span></span>    |
    |------------------------|----------|
    | <span data-ttu-id="dc1a9-177">減損損失額</span><span class="sxs-lookup"><span data-stu-id="dc1a9-177">Impairment amount</span></span>      | <span data-ttu-id="dc1a9-178">35,000</span><span class="sxs-lookup"><span data-stu-id="dc1a9-178">35,000</span></span>   |
    | <span data-ttu-id="dc1a9-179">トランザクション日</span><span class="sxs-lookup"><span data-stu-id="dc1a9-179">Transaction date</span></span>       | <span data-ttu-id="dc1a9-180">2022 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="dc1a9-180">1/1/2022</span></span> |
    | <span data-ttu-id="dc1a9-181">残余期間</span><span class="sxs-lookup"><span data-stu-id="dc1a9-181">Periods remaining</span></span>      | <span data-ttu-id="dc1a9-182">84</span><span class="sxs-lookup"><span data-stu-id="dc1a9-182">84</span></span>       |
    | <span data-ttu-id="dc1a9-183">転記</span><span class="sxs-lookup"><span data-stu-id="dc1a9-183">Post</span></span>                   | <span data-ttu-id="dc1a9-184">あり</span><span class="sxs-lookup"><span data-stu-id="dc1a9-184">Yes</span></span>      |
    | <span data-ttu-id="dc1a9-185">転記前のプレビュー</span><span class="sxs-lookup"><span data-stu-id="dc1a9-185">Preview before posting</span></span> | <span data-ttu-id="dc1a9-186">なし</span><span class="sxs-lookup"><span data-stu-id="dc1a9-186">No</span></span>       |
    | <span data-ttu-id="dc1a9-187">帳簿のクローズ</span><span class="sxs-lookup"><span data-stu-id="dc1a9-187">Close book</span></span>             | <span data-ttu-id="dc1a9-188">なし</span><span class="sxs-lookup"><span data-stu-id="dc1a9-188">No</span></span>       |

6. <span data-ttu-id="dc1a9-189">減損経費仕訳入力が作成され、転記されました。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-189">An impairment expense journal entry has been created and posted.</span></span> <span data-ttu-id="dc1a9-190">表示するには、資産のリース仕訳帳のリース帳簿を表示します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-190">To view it, go to the asset's leasing journal in the lease book.</span></span> <span data-ttu-id="dc1a9-191">この減損の金額が、減損経費転記勘定に借方記入され、使用権資産の転記勘定に貸方記入されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-191">Notice that the amount of the impairment was debited to the Impairment expense posting account, and the ROU asset posting account was credited.</span></span>
7. <span data-ttu-id="dc1a9-192">減損の正味効果を表示するには、[負債] テーブルと [資産トランザクション] テーブルに移動します。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-192">To view the net effect of the impairment, go to the liability and asset transactions tables.</span></span> <span data-ttu-id="dc1a9-193">減損経費は使用権資産を減少しましたが、リース負債のキャリー額が変更されていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-193">Notice that the impairment expense has decreased the ROU asset, but the carrying amount of the lease liability hasn't changed.</span></span>

<span data-ttu-id="dc1a9-194">この減損には、考慮する必要があるもう 1 つの影響があります。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-194">The impairment has one other effect that you should consider.</span></span> <span data-ttu-id="dc1a9-195">使用権資産金額はリース負債よりもはるかに少ないので、この金額は以前とは異なる減価償却を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-195">Because the ROU asset amount is now much less than the lease liability, the amount must be depreciated differently than it was before.</span></span> <span data-ttu-id="dc1a9-196">特に、この資産は、トランザクションの日付から開始され、残りの 84 か月のリースにわたって定額法で減価償却されるようになります。</span><span class="sxs-lookup"><span data-stu-id="dc1a9-196">Specifically, the asset is now depreciated in a straight-line manner throughout the remaining 84 months of the lease, beginning on the transaction date.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]