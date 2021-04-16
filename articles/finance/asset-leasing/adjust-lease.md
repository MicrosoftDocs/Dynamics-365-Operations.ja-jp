---
title: リースの調整
description: このトピックでは、リースを調整する方法について説明します。 リースの条件が変更された場合、リースが拡張された場合、またはその他の状況が変化した場合は、調整が必要になることがあります。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1dce99e9fb553cce8de9cefc7e01c8755e9d2090
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825774"
---
# <a name="adjust-leases"></a><span data-ttu-id="ec457-104">リースの調整</span><span class="sxs-lookup"><span data-stu-id="ec457-104">Adjust leases</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ec457-105">このトピックでは、リースを調整する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ec457-105">The topic explains how to adjust a lease.</span></span> <span data-ttu-id="ec457-106">リースの条件が変更された場合、リースが拡張された場合、またはその他の状況が変化した場合は、調整が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="ec457-106">Adjustment might be required if the lease terms are modified, the lease is extended, or other circumstances change.</span></span> <span data-ttu-id="ec457-107">資産リースは、リースの変更に関する Accounting Standards Codification Topic 842 (ASC 842) および International Financial Reporting Standard 16 (IFRS 16) のガイダンスに準拠しています。</span><span class="sxs-lookup"><span data-stu-id="ec457-107">Asset leasing complies with the guidance that Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16) provide about lease modifications.</span></span> <span data-ttu-id="ec457-108">ASC 842-20-15-1 では、リースの変更を、リースの範囲や対価に変更を生じさせる契約条件の変更と定義しています。</span><span class="sxs-lookup"><span data-stu-id="ec457-108">ASC 842-20-15-1 defines a lease modification as any change to the terms and conditions of a contract that causes a change in the scope of, or the consideration for, a lease.</span></span> <span data-ttu-id="ec457-109">IFRS 16 の パラグラフ 39 では、 賃借人はリース支払の変動を反映するようにリース負債を再評価する必要があることが示されています。</span><span class="sxs-lookup"><span data-stu-id="ec457-109">Paragraph 39 of IFRS 16 states that a lessee must revalue the lease liability so that it reflects changes to the lease payments.</span></span>

<span data-ttu-id="ec457-110">ASC 842 または IFRS 16 に準拠している組織については、リースは、将来のリース支払 (PVFMLP) の現在価値の変化を反映して再測定されます。</span><span class="sxs-lookup"><span data-stu-id="ec457-110">For organizations that adhere to ASC 842 or IFRS 16, a lease is remeasured to reflect a change in the present value of the future minimum lease payments (PVFMLP).</span></span> <span data-ttu-id="ec457-111">PVFMLP が増加した場合、作成される仕訳入力は、使用権 (ROU) 資産勘定の借方と、新規 PVFMLP と前の PVFMLP の差額に対するリース負債勘定の貸方になります。</span><span class="sxs-lookup"><span data-stu-id="ec457-111">If the PVFMLP increases, the journal entry that is created will be a debit to the right-of-use (ROU) asset account and a credit to the lease liability account for the difference between the new PVFMLP and the previous PVFMLP.</span></span> <span data-ttu-id="ec457-112">PVFMLP が減少した場合、仕訳入力はリース負債勘定の借方になり、使用権資産勘定に対する貸方となります。</span><span class="sxs-lookup"><span data-stu-id="ec457-112">If the PVFMLP decreases, the journal entry will be a debit to the lease liability account and a credit to the ROU asset account for the difference.</span></span>

<span data-ttu-id="ec457-113">調整で使用権資産の数が0 (ゼロ) を超えると、**リース転記勘定** ページで指定されている [リース変更の転記] 勘定の貸方に転記され ます。</span><span class="sxs-lookup"><span data-stu-id="ec457-113">If the adjustment decreases the ROU asset past 0 (zero), the remainder will be credited to the gain on lease modification posting account that is specified on the **Lease posting accounts** page.</span></span> <span data-ttu-id="ec457-114">このシステムでは、これら取引や、分類変更、初期直接原価、リースインセンティブ、前払い、リース変更に伴う解体費用などの調整項目を会計処理しています。</span><span class="sxs-lookup"><span data-stu-id="ec457-114">The system accounts for these transactions and other adjustment entries, such as classification changes, initial direct costs, lease incentives, prepayments, and dismantling costs that arise from lease modifications.</span></span>

<span data-ttu-id="ec457-115">リース調整トランザクションに関する具体的なガイダンスについては、IFRS 16 および ASC 842 を参照することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ec457-115">For specific guidance about lease adjustment transactions, we recommend that you see IFRS 16 and ASC 842.</span></span>

## <a name="lease-adjustment-wizard"></a><span data-ttu-id="ec457-116">リース調整ウィザード</span><span class="sxs-lookup"><span data-stu-id="ec457-116">Lease adjustment wizard</span></span>

<span data-ttu-id="ec457-117">リースを調整するには、以下の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="ec457-117">To adjust a lease, complete the following steps.</span></span> <span data-ttu-id="ec457-118">変更されたデータは、**リース調整** ウィザードから転記した後に、リース スケジュールを更新します。</span><span class="sxs-lookup"><span data-stu-id="ec457-118">The modified data will update lease schedules after you post from the **Lease adjustment** wizard.</span></span> <span data-ttu-id="ec457-119">いつでも作業を保存してウィザード閉じ、後で作業を再開できます。</span><span class="sxs-lookup"><span data-stu-id="ec457-119">You can save your work and close the wizard at any time, and then come back later to resume your work.</span></span>

<span data-ttu-id="ec457-120">リース概要から **リース調整** ウィザードを開くには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ec457-120">To open the **Lease adjustment** wizard from the lease summary, follow these steps.</span></span>

1. <span data-ttu-id="ec457-121">**資産リース \> リース \> リース概要** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ec457-121">Go to **Asset leasing \> Leases \> Lease summary**.</span></span> 
2. <span data-ttu-id="ec457-122">調整するリースを選択してから **調整ウィザード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-122">Select the lease to adjust, and then select **Adjustment wizard**.</span></span>
3. <span data-ttu-id="ec457-123">ウィザードのプロンプトに従って、必要な変更を入力します。</span><span class="sxs-lookup"><span data-stu-id="ec457-123">Follow the prompts in the wizard to enter the required changes.</span></span>

<span data-ttu-id="ec457-124">既に進行中を調整するために **リース調整** ページから **リース調整** ウィザードを開くには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ec457-124">To open the **Lease adjustment** wizard from the **Lease adjustments** page, for an adjustment that is already in progress, follow these steps.</span></span>

1.  <span data-ttu-id="ec457-125">**リース \> リース \> リース調整** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ec457-125">Go to **Lease \> Leases \> Lease adjustments**.</span></span>
2.  <span data-ttu-id="ec457-126">調整ステータスが **進行中** のリースを選択してから **調整ウィザード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-126">Select a lease that has an adjustment status of **In progress**, and then select **Adjustment wizard**.</span></span>
3.  <span data-ttu-id="ec457-127">**変更の開始日** フィールドと **転記の日付** フィールドに、適切な日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="ec457-127">In the **Modification start date** and **Posting date** fields, enter the appropriate dates.</span></span>
4.  <span data-ttu-id="ec457-128">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-128">Select **Next**.</span></span>

    <span data-ttu-id="ec457-129">リースが **リース調整** ページに追加されたので、リースに関する新しい情報を入力できます。</span><span class="sxs-lookup"><span data-stu-id="ec457-129">The lease is now added to the **Lease adjustments** page, where you can enter the new information about it.</span></span>

    <span data-ttu-id="ec457-130">リースが調整された後は、使用権考慮フィールドが適用されます。</span><span class="sxs-lookup"><span data-stu-id="ec457-130">After the lease has been adjusted, the right-of-use considerations fields apply to it.</span></span> <span data-ttu-id="ec457-131">リースの初期直接原価、リースインセンティブ、前払、または解体費用の原価が、変更されたリースに関連付けられていない場合は、対応するのフィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="ec457-131">If no initial direct costs, lease incentives, prepayments, or dismantling costs are associated with the modified lease, leave the corresponding fields blank.</span></span> <span data-ttu-id="ec457-132">元の金額は、更新されたリースには適用されません。</span><span class="sxs-lookup"><span data-stu-id="ec457-132">The original amounts won't apply to the updated lease.</span></span> 

    <span data-ttu-id="ec457-133">たとえば、賃貸人は、リース拡張に同意する $1,000インセンティブを提供します。</span><span class="sxs-lookup"><span data-stu-id="ec457-133">For example, a lessor provides a $1,000 incentive for agreeing to a lease extension.</span></span> <span data-ttu-id="ec457-134">拡張を考慮してリースを調整する場合は、**調整によって得たリース インセンティブ** フィールドに **1,000** と入力します。</span><span class="sxs-lookup"><span data-stu-id="ec457-134">In this case, when you adjust the lease to account for the extension, enter **1,000** in the **Lease incentives arising from adjustment** field.</span></span>

    <span data-ttu-id="ec457-135">これで、**変更の開始日** フィールドの支払スケジュール明細行に、その月以降の月のすべての支払が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ec457-135">The payment schedule lines now show all payments from the month, and later months, in the **Modification start date** field.</span></span> <span data-ttu-id="ec457-136">変更は予想なので、変更を開始する前に支払スケジュール明細行を開始できません。</span><span class="sxs-lookup"><span data-stu-id="ec457-136">Because modifications are prospective, payment schedule lines can't start before the modification starts.</span></span> <span data-ttu-id="ec457-137">変更の開始日前の支払スケジュール明細行を表示するには、**リース バージョン履歴** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="ec457-137">To view payment schedule lines from before the modification start date, go to the **Lease version history** page.</span></span>

8.  <span data-ttu-id="ec457-138">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-138">Select **Next**.</span></span>

    <span data-ttu-id="ec457-139">次のページには、変更前のリース負債の繰越価格や、変更後の新しい予定リース負債など、予定リース調整に関する重要な詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ec457-139">The next page shows key details about the expected lease adjustment, such as the carrying values of the lease liability before the modification and the new expected lease liability after the modification.</span></span> <span data-ttu-id="ec457-140">このページには、予定リース調整の仕訳入力のプレビューも表示されます。</span><span class="sxs-lookup"><span data-stu-id="ec457-140">The page also shows a preview of the journal entry for the expected lease adjustment.</span></span>

9.  <span data-ttu-id="ec457-141">リース調整ワークフローが有効で調整がまだ承認されていない場合は、**ワークフローに送信** を選択してリース調整をワークフロー システムに送信します。</span><span class="sxs-lookup"><span data-stu-id="ec457-141">Select **Submit to workflow** to submit the lease adjustment to the workflow system if the lease adjustment workflow is active and the adjustment hasn't yet been approved.</span></span> <span data-ttu-id="ec457-142">リース調整ワークフローの使用方法の詳細については、[リース調整ワークフローの使用](use-create-lease-wrkflw.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec457-142">For more information about how to use the lease adjustment workflow, see [Use lease adjustments workflows](use-create-lease-wrkflw.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec457-143">調整概要および調整仕訳入力が最初に計算されたので、この時点でシステムが調整変数を再計算し、リースに対してトランザクションが転記されていないかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ec457-143">At this point, the system recalculates the adjustment variables to verify that no transactions have been posted against the lease since the adjustment overview and adjustment journal entry were first calculated.</span></span> <span data-ttu-id="ec457-144">値が変更された場合は、調整概要グリッドが更新され、リース調整をワークフロー システムに再送信する前に情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="ec457-144">If any values change, the adjustment overview grid is updated, and you can review the information before you resubmit the lease adjustments to the workflow system.</span></span>

10. <span data-ttu-id="ec457-145">ワークフローが有効でない場合、またはリース調整が承認されている場合は、**完了** を選択して変更を処理し、調整仕訳入力を転記します。</span><span class="sxs-lookup"><span data-stu-id="ec457-145">If a workflow isn't active, or if the lease adjustment has been approved, select **Finish** to process the changes and post the adjustment journal entry.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="ec457-146">調整概要および調整仕訳入力が最初に計算されたので、この時点でシステムが調整変数を再計算し、リースに対してトランザクションが転記されていないかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ec457-146">At this point, the system recalculates the adjustment variables to verify that no transactions have been posted against the lease since the adjustment overview and adjustment journal entry were first calculated.</span></span> <span data-ttu-id="ec457-147">値が変更すると調整概要グリッドが更新され、**完了** を選択する前に変更を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ec457-147">If any values change, the adjustment overview grid is updated, and you can review the changes before you select **Finish**.</span></span> <span data-ttu-id="ec457-148">ワークフローが有効でリース調整が承認されている場合は、調整概要を変更すると、承認状態が **送信しませんでした** に戻ります。</span><span class="sxs-lookup"><span data-stu-id="ec457-148">If the workflow is active and the lease adjustment has been approved, any changes to the adjustment overview will cause the approval status to be set back to **Not submitted**.</span></span> <span data-ttu-id="ec457-149">この場合は、リース調整をワークフロー システムに再送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec457-149">In this case, you should resubmit the lease adjustment to the workflow system.</span></span>

    <span data-ttu-id="ec457-150">**リース調整** ページで、調整状態が **完了** に設定されました。</span><span class="sxs-lookup"><span data-stu-id="ec457-150">On the **Lease adjustments** page, the adjustment status is now set to **Completed**.</span></span>

    <span data-ttu-id="ec457-151">**リース調整** ページでは、引き続き **調整概要** および **調整入力のプレビュー** FastTabs を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ec457-151">On the **Lease adjustments** page, you can still view the **Adjustment overview** and **Adjustment entry preview** FastTabs.</span></span> <span data-ttu-id="ec457-152">リースの詳細と日付に関する情報は、そのリースのバージョン履歴に表示されます。</span><span class="sxs-lookup"><span data-stu-id="ec457-152">The lease details and date information are shown in the version history of that lease.</span></span>

    <span data-ttu-id="ec457-153">更新した情報を使用して、新しいリース バージョンと新しいスケジュール セットが作成されました。</span><span class="sxs-lookup"><span data-stu-id="ec457-153">A new lease version and a new set of schedules are now created by using the modified information.</span></span> 

13. <span data-ttu-id="ec457-154">新しいスケジュールを表示するには、リースに移動し、**帳簿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-154">To view the new schedules, go to the lease, and then select **Books**.</span></span>
14. <span data-ttu-id="ec457-155">新しく生成された支払スケジュールを表示するには、**支払スケジュール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-155">To view the newly generated payment schedule, select **Payment schedule**.</span></span>
15. <span data-ttu-id="ec457-156">新しい情報から生成された新しいリース負債の償却スケジュールを表示するには、**支払スケジュール** ページを閉じ、**負債償却スケジュール** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="ec457-156">To view the new lease liability amortization schedule that is generated from the new information, close the **Payment schedule** page, and open the **Liability amortization schedule** page.</span></span>
16. <span data-ttu-id="ec457-157">新たに生成された資産の減価償却スケジュールを表示するには、**帳簿の詳細** ページから **資産減価償却スケジュール**  ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="ec457-157">To view the newly generated asset depreciation schedule, open the **Asset depreciation schedule** page from the **Book details** page.</span></span>
17. <span data-ttu-id="ec457-158">調整仕訳入力を表示するには、**仕訳帳 \> 資産リース仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-158">To view the adjustment journal entry, select **Journals \> Asset leasing journal**.</span></span>

## <a name="cancel-a-lease-adjustment"></a><span data-ttu-id="ec457-159">リース調整のキャンセル</span><span class="sxs-lookup"><span data-stu-id="ec457-159">Cancel a lease adjustment</span></span>

<span data-ttu-id="ec457-160">進行中のリース調整を削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ec457-160">To delete a lease adjustment that is in progress, follow these steps.</span></span>

1.  <span data-ttu-id="ec457-161">**リース \> リース \> リース調整** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ec457-161">Go to **Lease \> Leases \> Lease adjustments**.</span></span>
2.  <span data-ttu-id="ec457-162">キャンセルする進行中のリース調整を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-162">Select that in-progress lease adjustment to cancel.</span></span>
3.  <span data-ttu-id="ec457-163">**調整をキャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-163">Select **Cancel adjustment**.</span></span> 
4.  <span data-ttu-id="ec457-164">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-164">Select **OK**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="ec457-165">**リース調整** ウィザードで **キャンセル** を選択した場合、ウィザードで完了した最新の変更をロールバックしますが、進行中の調整は削除されません。</span><span class="sxs-lookup"><span data-stu-id="ec457-165">If you select **Cancel** in the **Lease adjustment** wizard, you roll back the most recent change that you completed in the wizard, but you don't remove an adjustment that is in progress.</span></span>

## <a name="use-the-lease-adjustment-workflow"></a><span data-ttu-id="ec457-166">リース調整ワークフローの使用</span><span class="sxs-lookup"><span data-stu-id="ec457-166">Use the lease adjustment workflow</span></span>

<span data-ttu-id="ec457-167">ここでは、リース調整ワークフローの使い方について説明します。</span><span class="sxs-lookup"><span data-stu-id="ec457-167">This section explains how to use the lease adjustment workflow.</span></span> <span data-ttu-id="ec457-168">リース調整ワークフローを使用すると、一連の承認段階に従い、リース調整が最終段階になる前に承認する特定のユーザーに割り当てるので、リース調整を一貫した方法で管理できます。</span><span class="sxs-lookup"><span data-stu-id="ec457-168">The lease adjustment workflow helps you manage lease adjustments in a consistent manner by providing a set of approval steps and assigning them to specific users who approve a lease adjustment before it becomes final.</span></span> <span data-ttu-id="ec457-169">ワークフローでリース調整が承認された後に、**リース調整** ウィザードを使用してリース調整を完了できます。</span><span class="sxs-lookup"><span data-stu-id="ec457-169">After the lease adjustment is approved in the workflow, you can use the **Lease adjustment** wizard to complete the lease adjustment.</span></span>

1.  <span data-ttu-id="ec457-170">承認のためにリース調整を送信するには、**リース \> リース \> リース調整** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ec457-170">To submit a lease adjustment for approval, go to **Lease \> Leases \> Lease adjustments**.</span></span>
2.  <span data-ttu-id="ec457-171">リース調整のリース ID を選択してから **調整ウィザード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-171">Select the lease ID of the lease adjustment, and then select **Adjustment wizard**.</span></span>
3.  <span data-ttu-id="ec457-172">ウィザードの最後のページで、**承認のために送信する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-172">On the last page of the wizard, select **Submit for approval**.</span></span>
4.  <span data-ttu-id="ec457-173">調整に関するコメントを入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-173">Enter a comment about the adjustment, and then select **OK**.</span></span>

    <span data-ttu-id="ec457-174">ワークフローの状態が **保留中の承認** に変わり、ウィザードにあるすべてのフィールドが編集用にロックされます。</span><span class="sxs-lookup"><span data-stu-id="ec457-174">The workflow status is changed to **Pending approval**, and all the fields in the wizard are locked for editing.</span></span>

5.  <span data-ttu-id="ec457-175">リース調整を承認するには、**リース \> リース \> リース調整** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ec457-175">To approve the lease adjustment, go to **Lease \> Leases \> Lease adjustments**.</span></span>
6.  <span data-ttu-id="ec457-176">リース調整のリース ID を選択して、**調整概要** および **調整入力のプレビュー** FastTabs を表示します。</span><span class="sxs-lookup"><span data-stu-id="ec457-176">Select the lease ID of the lease adjustment, and review the **Adjustment overview** and **Adjustment entry preview** FastTabs.</span></span>
7.  <span data-ttu-id="ec457-177">**ワークフロー \> 承認済** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-177">Select **Workflow \> Approved**.</span></span>

    <span data-ttu-id="ec457-178">**リース調整** ページで、ワークフロー状態が **承認済** に設定されました。</span><span class="sxs-lookup"><span data-stu-id="ec457-178">On the **Lease adjustments** page, the workflow status is now set to **Approved**.</span></span> <span data-ttu-id="ec457-179">この時点で、リース調整を調整仕訳入力から転記できるようになります。</span><span class="sxs-lookup"><span data-stu-id="ec457-179">At this point, the lease adjustment is ready to be posted through the adjustment journal entry.</span></span>

8.  <span data-ttu-id="ec457-180">引き続きリース調整を処理して調整エントリを転記するには、**リース \> リース \> リース調整** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ec457-180">To continue to process the lease adjustment and post the adjustment entry, go to **Lease \> Leases \> Lease adjustments**.</span></span>
9.  <span data-ttu-id="ec457-181">リース調整のリース ID を選択してから **調整ウィザード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-181">Select the lease ID of the lease adjustment, and then select **Adjustment wizard**.</span></span>
10. <span data-ttu-id="ec457-182">ウィザードの最後のページになるまで **次へ** を選択してから、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-182">Select **Next** until you reach the last page of the wizard, and then select **Finish**.</span></span>

<span data-ttu-id="ec457-183">システムでリースの繰越価格が再計算され、承認された調整変数が最新の状態かを確認します。</span><span class="sxs-lookup"><span data-stu-id="ec457-183">The system recalculates the carrying values of the lease to ensure that the adjustment variables that were approved are current.</span></span> <span data-ttu-id="ec457-184">変更がある場合、承認状態が **下書き** に戻り、リース調整をワークフロー システムに再送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec457-184">If there are any changes, the approval status is set back to **Draft**, and you should resubmit the lease adjustment to the workflow system.</span></span>

## <a name="view-lease-versions"></a><span data-ttu-id="ec457-185">リース バージョンの表示</span><span class="sxs-lookup"><span data-stu-id="ec457-185">View lease versions</span></span>

<span data-ttu-id="ec457-186">リースが調整されている場合は、異なるバージョンを表示できます。</span><span class="sxs-lookup"><span data-stu-id="ec457-186">If a lease has been adjusted, you can view the different versions of it.</span></span> <span data-ttu-id="ec457-187">履歴スケジュールと過去のリースの詳細を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="ec457-187">You can also view the historical schedules and past lease details.</span></span>

1. <span data-ttu-id="ec457-188">**リースの概要** ページで、コピーするリースを選択し、[アクション] ウィンドウで **リースのバージョン履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-188">On the **Lease summary** page, select the lease, and then, on the Action Pane, select **Lease version history**.</span></span>

    <span data-ttu-id="ec457-189">選択したリースが調整されている場合、**リースのバージョン履歴** ページには、異なるバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ec457-189">If the selected lease has been adjusted, the **Lease version history** page shows the different versions.</span></span> <span data-ttu-id="ec457-190">元のリースには **1** というラベルが付けられ、後続のバージョンに連番が付番されます。</span><span class="sxs-lookup"><span data-stu-id="ec457-190">The original lease is labeled **1**, and subsequent versions have ascending numerical order.</span></span>

    <span data-ttu-id="ec457-191">選択したリース バージョンに対して、財務分析コード、契約の詳細、場所、および支払スケジュール明細行を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ec457-191">For a selected lease version, you can view the financial dimensions, contract details, location, and payment schedule lines.</span></span>

2. <span data-ttu-id="ec457-192">履歴スケジュールを表示するには、**リースの概要** ページで変更したリースを開き 、目的の帳簿を選択して、アクション ウィンドウで **帳簿バージョン履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-192">To view historical schedules, open the modified lease from the **Lease summary** page, select the desired book, and then, on the Action Pane, select **Book version history**.</span></span>
3. <span data-ttu-id="ec457-193">**帳簿バージョン** ページで、バージョンと表示するスケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="ec457-193">On the **Book version** page, select a version and a schedule to view.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]