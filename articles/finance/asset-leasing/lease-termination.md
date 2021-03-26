---
title: リース終了提案
description: このトピックでは、解約に向けたリースの提案方法について解説します。
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 144559b14878a44afd8a77648bb5ce1d3ba17832
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131294"
---
# <a name="propose-a-lease-for-termination"></a><span data-ttu-id="abeaf-103">解約に向けたリースの提案</span><span class="sxs-lookup"><span data-stu-id="abeaf-103">Propose a lease for termination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abeaf-104">リースが早期に終了した場合、資産リースでは終了の仕訳入力をしてリース負債、使用権 (ROU) 資産、減価償却累計額の損金処理を記録し、損益を帳簿に記録できます。</span><span class="sxs-lookup"><span data-stu-id="abeaf-104">If a lease is terminated early, Asset leasing can record a termination journal entry to write off the lease liability, right-of-use (ROU) asset, and accumulated depreciation, and book a gain or loss.</span></span> <span data-ttu-id="abeaf-105">早期終了プロセスによりリースが終了し、関連付けられているリース帳簿が終了します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-105">The early termination process terminates a lease and its associated lease books.</span></span> <span data-ttu-id="abeaf-106">個々のリース帳簿は終了しません。</span><span class="sxs-lookup"><span data-stu-id="abeaf-106">It doesn't terminate individual lease books.</span></span> <span data-ttu-id="abeaf-107">このトピックでは、終了に向けたリースの提案、リース終了仕訳エントリを処理する機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-107">This topic describes the functionality that lets you propose a lease for termination and process the lease termination journal entry.</span></span>

<span data-ttu-id="abeaf-108">リースで繰延支払として分類され、固定資産に関連付けされていない場合は、次の終了仕訳入力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="abeaf-108">If a lease isn't classified as a deferred rent treatment lease and isn't associated with a fixed asset, Asset leasing produces the following termination journal entry.</span></span>

| <span data-ttu-id="abeaf-109">取引</span><span class="sxs-lookup"><span data-stu-id="abeaf-109">Transaction</span></span>                           | <span data-ttu-id="abeaf-110">借方 (Dr.)</span><span class="sxs-lookup"><span data-stu-id="abeaf-110">Debit (Dr.)</span></span> | <span data-ttu-id="abeaf-111">貸方 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="abeaf-111">Credit (Cr.)</span></span> |
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="abeaf-112">借方 : リース負債</span><span class="sxs-lookup"><span data-stu-id="abeaf-112">Dr. Lease liability</span></span>                   | <span data-ttu-id="abeaf-113">X</span><span class="sxs-lookup"><span data-stu-id="abeaf-113">X</span></span>           |              |
| <span data-ttu-id="abeaf-114">借方 : 減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="abeaf-114">Dr. Accumulated depreciation</span></span>          | <span data-ttu-id="abeaf-115">X</span><span class="sxs-lookup"><span data-stu-id="abeaf-115">X</span></span>           |              |
| <span data-ttu-id="abeaf-116">貸方 : リース変更に伴う利益/損失</span><span class="sxs-lookup"><span data-stu-id="abeaf-116">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="abeaf-117">X</span><span class="sxs-lookup"><span data-stu-id="abeaf-117">X</span></span>           |              |
| <span data-ttu-id="abeaf-118">貸方 : リース資産</span><span class="sxs-lookup"><span data-stu-id="abeaf-118">Cr. Lease asset</span></span>                       |             | <span data-ttu-id="abeaf-119">X</span><span class="sxs-lookup"><span data-stu-id="abeaf-119">X</span></span>            |
| <span data-ttu-id="abeaf-120">貸方 : リース変更に伴う利益/損失</span><span class="sxs-lookup"><span data-stu-id="abeaf-120">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="abeaf-121">X</span><span class="sxs-lookup"><span data-stu-id="abeaf-121">X</span></span>            |

<span data-ttu-id="abeaf-122">リース帳が繰延繰延賃料に分類されている場合は、ここに示すように、終了前の繰延繰延賃料の残高を損益計算書に計上します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-122">If the lease book is classified as a deferred rent book, the entry writes off the balance of the deferred rent before the termination to the gain or loss account, as shown here.</span></span>

| <span data-ttu-id="abeaf-123">取引</span><span class="sxs-lookup"><span data-stu-id="abeaf-123">Transaction</span></span>                           | <span data-ttu-id="abeaf-124">借方 (Dr.)</span><span class="sxs-lookup"><span data-stu-id="abeaf-124">Debit (Dr.)</span></span> | <span data-ttu-id="abeaf-125">貸方 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="abeaf-125">Credit (Cr.)</span></span> | 
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="abeaf-126">借方 : 繰延賃料</span><span class="sxs-lookup"><span data-stu-id="abeaf-126">Dr. Deferred rent</span></span>                     | <span data-ttu-id="abeaf-127">X</span><span class="sxs-lookup"><span data-stu-id="abeaf-127">X</span></span>           |              |
| <span data-ttu-id="abeaf-128">貸方 : リース変更に伴う利益/損失</span><span class="sxs-lookup"><span data-stu-id="abeaf-128">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="abeaf-129">X</span><span class="sxs-lookup"><span data-stu-id="abeaf-129">X</span></span>            |
| <span data-ttu-id="abeaf-130">貸方 : 繰延賃料</span><span class="sxs-lookup"><span data-stu-id="abeaf-130">Cr. Deferred rent</span></span>                     |             | <span data-ttu-id="abeaf-131">X</span><span class="sxs-lookup"><span data-stu-id="abeaf-131">X</span></span>            |
| <span data-ttu-id="abeaf-132">貸方 : リース変更に伴う利益/損失</span><span class="sxs-lookup"><span data-stu-id="abeaf-132">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="abeaf-133">X</span><span class="sxs-lookup"><span data-stu-id="abeaf-133">X</span></span>           |              |

<span data-ttu-id="abeaf-134">リース帳帳が固定資産に関連付けられている場合、ROU資産は固定資産の勘定に設定されます。</span><span class="sxs-lookup"><span data-stu-id="abeaf-134">If the lease book is connected to a fixed asset, the ROU asset is accounted for in Fixed assets.</span></span> <span data-ttu-id="abeaf-135">この会計には、早期終了の会計処理が含まれています。</span><span class="sxs-lookup"><span data-stu-id="abeaf-135">This accounting includes the accounting for early terminations.</span></span> <span data-ttu-id="abeaf-136">資産のリースは、リース負債の損金処理するために以下の仕訳入力を作成します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-136">Asset leasing produces the following journal entry to write off the lease liability.</span></span>

| <span data-ttu-id="abeaf-137">取引</span><span class="sxs-lookup"><span data-stu-id="abeaf-137">Transaction</span></span>                           | <span data-ttu-id="abeaf-138">借方 (Dr.)</span><span class="sxs-lookup"><span data-stu-id="abeaf-138">Debit (Dr.)</span></span> | <span data-ttu-id="abeaf-139">貸方 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="abeaf-139">Credit (Cr.)</span></span> |
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="abeaf-140">借方 : リース負債</span><span class="sxs-lookup"><span data-stu-id="abeaf-140">Dr. Lease liability</span></span>                   | <span data-ttu-id="abeaf-141">X</span><span class="sxs-lookup"><span data-stu-id="abeaf-141">X</span></span>           |              |
| <span data-ttu-id="abeaf-142">貸方 : リース変更に伴う利益/損失</span><span class="sxs-lookup"><span data-stu-id="abeaf-142">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="abeaf-143">X</span><span class="sxs-lookup"><span data-stu-id="abeaf-143">X</span></span>            |

<span data-ttu-id="abeaf-144">ROU資産の正しい処分方法については、[固定資産の仕損としての処分](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="abeaf-144">For information about the correct way to dispose of an ROU asset, see [Dispose of a fixed asset as scrap](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).</span></span>

## <a name="propose-a-lease-for-termination"></a><span data-ttu-id="abeaf-145">解約に向けたリースの提案</span><span class="sxs-lookup"><span data-stu-id="abeaf-145">Propose a lease for termination</span></span>

1. <span data-ttu-id="abeaf-146">終了する必要があるリースに移動し、アクション ウィンドウで **終了提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-146">Go to the lease that must be terminated, and then, on the Action Pane, select **Termination proposal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="abeaf-147">帳帳に対して未転記の仕訳帳エントリがある場合は、**終了提案** ボタンは使用できません。</span><span class="sxs-lookup"><span data-stu-id="abeaf-147">The **Termination proposal** button is unavailable if there are any unposted journal entries against any book.</span></span> <span data-ttu-id="abeaf-148">リースを終了する前に、リースに対して作成された仕訳帳エントリを転記、または削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abeaf-148">Before you can terminate the lease, you must post or delete any journal entries that have been created against the lease.</span></span>

2. <span data-ttu-id="abeaf-149">表示されるダイアログ ボックスで、終了仕訳帳エントリの **有効日** フィールドと **転記日** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-149">In the dialog box that appears, set the **Effective date** and **Posting date** fields for the termination journal entry.</span></span>
3. <span data-ttu-id="abeaf-150">リースの終了を提案するには、**終了提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-150">Select **Termination proposal** to propose the lease for termination.</span></span>
4. <span data-ttu-id="abeaf-151">リース終了仕訳帳エントリを自動的に転記するには、 **リースの終了の転記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-151">Select **Post lease termination** to automatically post the lease termination journal entry.</span></span>
5. <span data-ttu-id="abeaf-152">**リースの終了** ページで、終了について提案したリースのリース ID を選択して、終了明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-152">On the **Lease terminations** page, select the lease ID of the lease that you proposed for termination to view the termination lines.</span></span> <span data-ttu-id="abeaf-153">終了明細行には、ROU資産、リース負債、減価償却累計額、繰延賃料 (該当する場合)、リース終了時に認識する必要がある損益の帳簿価額を示しています。</span><span class="sxs-lookup"><span data-stu-id="abeaf-153">The termination lines show the carrying values of the ROU asset, lease liability, accumulated depreciation, deferred rent (if applicable), and gain or loss that must be recognized on the termination of the lease.</span></span>

<span data-ttu-id="abeaf-154">以上でリースを終了する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="abeaf-154">The lease is now ready for termination.</span></span> <span data-ttu-id="abeaf-155">リース帳に対する **終了状態** フィールドの値が **終了準備完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="abeaf-155">The value of the **Termination status** field for the lease book is changed to **Ready for termination**.</span></span> <span data-ttu-id="abeaf-156">この時点では、リースに対する仕訳入力の転記や、仕訳入力の調整や変更はできません。</span><span class="sxs-lookup"><span data-stu-id="abeaf-156">At this point, you can no longer post journal entries against the lease, or adjust or impair it.</span></span> 

## <a name="process-leases-that-are-ready-for-termination"></a><span data-ttu-id="abeaf-157">終了の準備が整ったリースを処理する</span><span class="sxs-lookup"><span data-stu-id="abeaf-157">Process leases that are ready for termination</span></span>

<span data-ttu-id="abeaf-158">終了の準備ができたリースを処理し、終了の仕訳入力を転記するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="abeaf-158">To process leases that are ready for termination and post the termination journal entry, follow these steps.</span></span>

1. <span data-ttu-id="abeaf-159">**リースの終了** ページで、処理対象のリースを選択し、 **終了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-159">On the **Lease terminations** page, select the lease to process, and then select **Terminate**.</span></span>
2. <span data-ttu-id="abeaf-160">表示されるダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-160">In the dialog box that appears, select **OK**.</span></span>

<span data-ttu-id="abeaf-161">システムが終了の仕訳入力を転記します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-161">The system posts the termination journal entry.</span></span> <span data-ttu-id="abeaf-162">リース帳の **リース状態** フィールドが **終了** に、**終了提案の状態** フィールドが **完了** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="abeaf-162">The **Lease status** field for the lease book is set to **Terminated**, and the **Termination proposal status** field is set to **Completed**.</span></span>

## <a name="reverse-a-lease-termination"></a><span data-ttu-id="abeaf-163">リース終了の取消</span><span class="sxs-lookup"><span data-stu-id="abeaf-163">Reverse a lease termination</span></span>

<span data-ttu-id="abeaf-164">リース終了仕訳エントリを取消して、終了したリースを開くには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="abeaf-164">To reverse a lease termination journal entry and open a terminated lease, follow this step.</span></span>

- <span data-ttu-id="abeaf-165">**リースの終了** ページで、終了したリースを選択し、 **終了の取消** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-165">On the **Lease terminations** page, select the terminated lease to reverse, and then select **Reverse termination**.</span></span>

<span data-ttu-id="abeaf-166">システムが終了の仕訳入力を取消します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-166">The system reverses the termination journal entry.</span></span> <span data-ttu-id="abeaf-167">リース帳の **リース状態** フィールドが **オープン** に設定 されます。</span><span class="sxs-lookup"><span data-stu-id="abeaf-167">The **Lease status** field for the lease book is set to **Open**.</span></span> <span data-ttu-id="abeaf-168">リースが、**リースの終了** ページに表示されなくなるので、もう一度提案することができます。</span><span class="sxs-lookup"><span data-stu-id="abeaf-168">The lease no longer appears on the **Lease terminations** page and can be proposed again for termination.</span></span>

## <a name="example-of-a-lease-termination"></a><span data-ttu-id="abeaf-169">リースの終了の例</span><span class="sxs-lookup"><span data-stu-id="abeaf-169">Example of a lease termination</span></span>

<span data-ttu-id="abeaf-170">この例では、リースは非専門資産と関連付けられており、資産の所有権を移管したり、賃借人に購入の選択肢を与えたりするものではありません。</span><span class="sxs-lookup"><span data-stu-id="abeaf-170">For this example, the lease is associated with a non-specialized asset, and it doesn't transfer ownership of the asset or grant the lessee the option to purchase the asset.</span></span>

### <a name="setup"></a><span data-ttu-id="abeaf-171">段取り</span><span class="sxs-lookup"><span data-stu-id="abeaf-171">Setup</span></span>

<span data-ttu-id="abeaf-172">以下の表は、この例で使用したリースの、**一般** と **支払スケジュール明細行** タブに設定されている値を示しています。</span><span class="sxs-lookup"><span data-stu-id="abeaf-172">The following tables show the values that are set on the **General** and **Payment schedule lines** tabs for the lease that is used in this example.</span></span>

<span data-ttu-id="abeaf-173">**全般タブ**</span><span class="sxs-lookup"><span data-stu-id="abeaf-173">**General tab**</span></span>

| <span data-ttu-id="abeaf-174">フィールド</span><span class="sxs-lookup"><span data-stu-id="abeaf-174">Field</span></span>                      | <span data-ttu-id="abeaf-175">先頭値</span><span class="sxs-lookup"><span data-stu-id="abeaf-175">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="abeaf-176">資産の公正価値</span><span class="sxs-lookup"><span data-stu-id="abeaf-176">Fair value of the asset</span></span>    | <span data-ttu-id="abeaf-177">600,000</span><span class="sxs-lookup"><span data-stu-id="abeaf-177">600,000</span></span>          |
| <span data-ttu-id="abeaf-178">通貨</span><span class="sxs-lookup"><span data-stu-id="abeaf-178">Currency</span></span>                   | <span data-ttu-id="abeaf-179">USD</span><span class="sxs-lookup"><span data-stu-id="abeaf-179">USD</span></span>              |
| <span data-ttu-id="abeaf-180">初期直接原価</span><span class="sxs-lookup"><span data-stu-id="abeaf-180">Initial direct costs</span></span>       | <span data-ttu-id="abeaf-181">1.000</span><span class="sxs-lookup"><span data-stu-id="abeaf-181">1,000</span></span>            |
| <span data-ttu-id="abeaf-182">追加借入利子率</span><span class="sxs-lookup"><span data-stu-id="abeaf-182">Incremental borrowing rate</span></span> | <span data-ttu-id="abeaf-183">7%</span><span class="sxs-lookup"><span data-stu-id="abeaf-183">7%</span></span>               |
| <span data-ttu-id="abeaf-184">複合間隔</span><span class="sxs-lookup"><span data-stu-id="abeaf-184">Compounding interval</span></span>       | <span data-ttu-id="abeaf-185">毎年</span><span class="sxs-lookup"><span data-stu-id="abeaf-185">Annually</span></span>         |
| <span data-ttu-id="abeaf-186">資産の耐用年数 (月単位)</span><span class="sxs-lookup"><span data-stu-id="abeaf-186">Asset useful life (months)</span></span> | <span data-ttu-id="abeaf-187">600</span><span class="sxs-lookup"><span data-stu-id="abeaf-187">600</span></span>              |
| <span data-ttu-id="abeaf-188">定期支払のタイプ</span><span class="sxs-lookup"><span data-stu-id="abeaf-188">Annuity type</span></span>               | <span data-ttu-id="abeaf-189">通常の定期支払</span><span class="sxs-lookup"><span data-stu-id="abeaf-189">Ordinary annuity</span></span> |
| <span data-ttu-id="abeaf-190">開始日</span><span class="sxs-lookup"><span data-stu-id="abeaf-190">Commencement date</span></span>          | <span data-ttu-id="abeaf-191">2019 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="abeaf-191">1/1/2019</span></span>         |

<span data-ttu-id="abeaf-192">**支払スケジュール明細行タブ**</span><span class="sxs-lookup"><span data-stu-id="abeaf-192">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="abeaf-193">フィールド</span><span class="sxs-lookup"><span data-stu-id="abeaf-193">Field</span></span>             | <span data-ttu-id="abeaf-194">先頭値</span><span class="sxs-lookup"><span data-stu-id="abeaf-194">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="abeaf-195">開始日</span><span class="sxs-lookup"><span data-stu-id="abeaf-195">Start date</span></span>        | <span data-ttu-id="abeaf-196">2019 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="abeaf-196">1/1/2019</span></span>   |
| <span data-ttu-id="abeaf-197">間隔</span><span class="sxs-lookup"><span data-stu-id="abeaf-197">Period interval</span></span>   | <span data-ttu-id="abeaf-198">月 1 回</span><span class="sxs-lookup"><span data-stu-id="abeaf-198">Monthly</span></span>    |
| <span data-ttu-id="abeaf-199">期間</span><span class="sxs-lookup"><span data-stu-id="abeaf-199">Periods</span></span>           | <span data-ttu-id="abeaf-200">120</span><span class="sxs-lookup"><span data-stu-id="abeaf-200">120</span></span>        |
| <span data-ttu-id="abeaf-201">終了日</span><span class="sxs-lookup"><span data-stu-id="abeaf-201">End date</span></span>          | <span data-ttu-id="abeaf-202">2028 年 12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="abeaf-202">12/31/2028</span></span> |
| <span data-ttu-id="abeaf-203">支払頻度</span><span class="sxs-lookup"><span data-stu-id="abeaf-203">Payment frequency</span></span> | <span data-ttu-id="abeaf-204">毎年</span><span class="sxs-lookup"><span data-stu-id="abeaf-204">Annually</span></span>   |
| <span data-ttu-id="abeaf-205">支払額</span><span class="sxs-lookup"><span data-stu-id="abeaf-205">Payment amount</span></span>    | <span data-ttu-id="abeaf-206">10,000</span><span class="sxs-lookup"><span data-stu-id="abeaf-206">10,000</span></span>     |

### <a name="steps-for-terminating-the-lease"></a><span data-ttu-id="abeaf-207">リース終了の手順</span><span class="sxs-lookup"><span data-stu-id="abeaf-207">Steps for terminating the lease</span></span>

1. <span data-ttu-id="abeaf-208">このトピックで既に説明したようにリースを作成した後、リース帳簿に移動し、支払スケジュールを確認します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-208">After you create the lease as described earlier in this topic, go to the lease book, and confirm the payment schedule.</span></span> <span data-ttu-id="abeaf-209">次に、初期認識仕訳入力を転記します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-209">Then post the initial recognition journal entry.</span></span> <span data-ttu-id="abeaf-210">当初の使用権資産は $71,235.81、リース負債は $70,235.81 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="abeaf-210">The initial ROU asset is $71,235.81, and lease liability should be $70,235.81.</span></span> <span data-ttu-id="abeaf-211">この例では、リースは ASC 842 (会計基準のコード化 842) の下ではオペレーティング リースとして分類されています。</span><span class="sxs-lookup"><span data-stu-id="abeaf-211">For this example, the lease was classified as an operating lease under Accounting Standards Codification Topic 842 (ASC 842).</span></span>
2. <span data-ttu-id="abeaf-212">バッチ仕訳プロセスを 3 回実行して、リース支払、支払い利息、および減価償却費に対する 3 年間の通過をシミュレーションします。</span><span class="sxs-lookup"><span data-stu-id="abeaf-212">Run the batch journal process three times to simulate the passage of three years for the lease payments, interest expenses, and depreciation expenses.</span></span>
3. <span data-ttu-id="abeaf-213">3 つのバッチジョブすべての実行完了後は、リース帳簿に戻り、負債 テーブルと資産トランザクション テーブルを開いて、使用権資産とリース負債の現在の帳簿価額を表示します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-213">After you've finished running all three batch jobs, go back to the lease book, and open the Liability and Asset transactions tables to view the current carrying value of the ROU asset and lease liability.</span></span> <span data-ttu-id="abeaf-214">3年後には、負債の価値は約 $-53,893.00、資産の価値は約 $54,593.00 となります。</span><span class="sxs-lookup"><span data-stu-id="abeaf-214">After three years, the value of the liability should be approximately $-53,893.00, and the value of the asset should be approximately $54,593.00.</span></span>

    <span data-ttu-id="abeaf-215">3年が経過すると、事業者と賃貸人が相互に合意して賃貸借契約を終了します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-215">After the three years have passed, the business and lessor mutually agree to terminate the lease.</span></span> <span data-ttu-id="abeaf-216">したがって、リースを終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="abeaf-216">Therefore, you must now terminate the lease.</span></span>

4. <span data-ttu-id="abeaf-217">終了する必要があるリースに移動し、アクション ウィンドウで **終了提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-217">Go to the lease that must be terminated, and then, on the Action Pane, select **Termination proposal**.</span></span> 
5. <span data-ttu-id="abeaf-218">表示されるダイアログ ボックスの **有効日** および **転記日** フィールドに **2021/1/1** と入力します 。</span><span class="sxs-lookup"><span data-stu-id="abeaf-218">In the dialog box that appears, in the **Effective date** and **Posting date** field, enter **1/1/2021**.</span></span>
6. <span data-ttu-id="abeaf-219">リースの終了を提案するには、**終了提案** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-219">Select **Termination proposal** to propose the lease for termination.</span></span>

    <span data-ttu-id="abeaf-220">**リースの終了** ページが表示され、終了するリースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="abeaf-220">The **Lease terminations** page appears and shows the lease that will be terminated.</span></span>

7. <span data-ttu-id="abeaf-221">終了明細行を表示するには、終了を提案したリースのリースIDを選択します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-221">To view the termination lines, select the lease ID of the lease that you proposed for termination.</span></span> <span data-ttu-id="abeaf-222">終了明細行には、リースの残高残高の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="abeaf-222">The termination lines show the carrying values of the lease.</span></span> <span data-ttu-id="abeaf-223">次の表に、これらの値の例を示します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-223">The following table shows what these values should be for this example.</span></span> 

    | <span data-ttu-id="abeaf-224">フィールド</span><span class="sxs-lookup"><span data-stu-id="abeaf-224">Field</span></span>                                                 | <span data-ttu-id="abeaf-225">先頭値</span><span class="sxs-lookup"><span data-stu-id="abeaf-225">Value</span></span>      |
    |-------------------------------------------------------|------------|
    | <span data-ttu-id="abeaf-226">取引を行った通貨での負債残高</span><span class="sxs-lookup"><span data-stu-id="abeaf-226">Carrying balance of liability in transaction currency</span></span> | <span data-ttu-id="abeaf-227">$53,892.89</span><span class="sxs-lookup"><span data-stu-id="abeaf-227">$53,892.89</span></span> |
    | <span data-ttu-id="abeaf-228">取引を行った通貨での使用権資産</span><span class="sxs-lookup"><span data-stu-id="abeaf-228">Right-of-use asset in transaction currency</span></span>            | <span data-ttu-id="abeaf-229">$71,235.81</span><span class="sxs-lookup"><span data-stu-id="abeaf-229">$71,235.81</span></span> |
    | <span data-ttu-id="abeaf-230">取引を行った通貨での減価償却の累計</span><span class="sxs-lookup"><span data-stu-id="abeaf-230">Accumulated depreciation in transaction currency</span></span>      | <span data-ttu-id="abeaf-231">$16,642.92</span><span class="sxs-lookup"><span data-stu-id="abeaf-231">$16,642.92</span></span> |
    | <span data-ttu-id="abeaf-232">取引を行った通貨での損益</span><span class="sxs-lookup"><span data-stu-id="abeaf-232">Gain (loss) in transaction currency</span></span>                   | <span data-ttu-id="abeaf-233">$-700.00</span><span class="sxs-lookup"><span data-stu-id="abeaf-233">$-700.00</span></span>   |

8. <span data-ttu-id="abeaf-234">終了の仕訳入力を転記するには、**リースの終了** ページで該当のロースを選択し、**終了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-234">To post the termination journal entry, select the lease on the **Lease terminations** page, and then select **Terminate**.</span></span>
9. <span data-ttu-id="abeaf-235">表示されるダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-235">In the dialog box that appears, select **OK**.</span></span>
10. <span data-ttu-id="abeaf-236">作成、転記された終了の仕訳入力を表示するには、リース帳の資産のリース仕訳に移動します。</span><span class="sxs-lookup"><span data-stu-id="abeaf-236">To view the termination journal entry that has been created and posted, go to the asset's leasing journal in the lease book.</span></span> <span data-ttu-id="abeaf-237">次の表は、この入力がこの例ではどのように見えるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="abeaf-237">The following table shows what this entry should look like for this example.</span></span>

    | <span data-ttu-id="abeaf-238">取引</span><span class="sxs-lookup"><span data-stu-id="abeaf-238">Transaction</span></span>                           | <span data-ttu-id="abeaf-239">借方 (Dr.)</span><span class="sxs-lookup"><span data-stu-id="abeaf-239">Debit (Dr.)</span></span> | <span data-ttu-id="abeaf-240">貸方 (Cr.)</span><span class="sxs-lookup"><span data-stu-id="abeaf-240">Credit (Cr.)</span></span> |
    |---------------------------------------|-------------|--------------|
    | <span data-ttu-id="abeaf-241">借方 : リース負債</span><span class="sxs-lookup"><span data-stu-id="abeaf-241">Dr. Lease liability</span></span>                   | <span data-ttu-id="abeaf-242">53,892.89</span><span class="sxs-lookup"><span data-stu-id="abeaf-242">53,892.89</span></span>   |              |
    | <span data-ttu-id="abeaf-243">Dr. 減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="abeaf-243">Dr. Accumulated depreciation</span></span>          | <span data-ttu-id="abeaf-244">16,642.92</span><span class="sxs-lookup"><span data-stu-id="abeaf-244">16,642.92</span></span>   |              |
    | <span data-ttu-id="abeaf-245">貸方 : リース変更に伴う利益/損失</span><span class="sxs-lookup"><span data-stu-id="abeaf-245">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="abeaf-246">700.00</span><span class="sxs-lookup"><span data-stu-id="abeaf-246">700.00</span></span>      |              |
    | <span data-ttu-id="abeaf-247">貸方 : リース資産</span><span class="sxs-lookup"><span data-stu-id="abeaf-247">Cr. Lease asset</span></span>                       |             | <span data-ttu-id="abeaf-248">71,235.81</span><span class="sxs-lookup"><span data-stu-id="abeaf-248">71,235.81</span></span>    |

11. <span data-ttu-id="abeaf-249">使用権資産とリース負債が0 (ゼロ) となる終了の正味効果を見るには、負債と資産の取引表を開きます。</span><span class="sxs-lookup"><span data-stu-id="abeaf-249">To view the net effect of the termination, where the ROU asset and lease liability will be 0 (zero), open the Liability and Asset transactions tables.</span></span>

<span data-ttu-id="abeaf-250">リースの状態が、**終了** となります。</span><span class="sxs-lookup"><span data-stu-id="abeaf-250">The lease status should now be **Terminated**.</span></span> <span data-ttu-id="abeaf-251">終了が取り消されていない限り、このリースに対して追加の仕訳入力は転記されません。</span><span class="sxs-lookup"><span data-stu-id="abeaf-251">No additional journal entries will be posted against this lease unless the termination is reversed.</span></span>