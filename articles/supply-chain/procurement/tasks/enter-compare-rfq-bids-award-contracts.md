---
title: RFQ 入札価格の入力、比較、および契約の授与
description: この手順は、見積依頼 (RFQ) への返信を入力したり、入札の記録や比較をしたり、また仕入先の 1 つに契約を授与する方法を示します。
author: mkirknel
manager: AnnBe
ms.date: 02/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45ddab03810b331bcd8965f6a2ba699ffb138910
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1533355"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="7aa67-103">RFQ 入札価格の入力、比較、および契約の授与</span><span class="sxs-lookup"><span data-stu-id="7aa67-103">Enter and compare RFQ bids, and award contracts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7aa67-104">この手順は、見積依頼 (RFQ) への返信を入力したり、受領した入札の記録や比較をしたり、また入札を送信してきた仕入先の 1 つに契約を授与する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-104">This procedure shows how to enter replies to a request for quotation (RFQ), score and compare bids that you receive, and then award the contract to one of the vendors who submitted bids.</span></span> <span data-ttu-id="7aa67-105">デモ データの会社 **USMF** でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-105">You can use this procedure in the **USMF** demo data company.</span></span>

<span data-ttu-id="7aa67-106">この手順を開始する前に、少なくとも 2 つの仕入先に送信された、2 つの明細行から成る RFQ が必要になります。</span><span class="sxs-lookup"><span data-stu-id="7aa67-106">Before you start this procedure, you must have an RFQ that has two lines, and that has been sent to at least two vendors.</span></span> <span data-ttu-id="7aa67-107">この RFQ を作成するには[見積依頼の作成](create-request-quotation.md)の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-107">To create this RFQ, complete the [Create a request for quotation](create-request-quotation.md) procedure.</span></span> <span data-ttu-id="7aa67-108">この手順を完了する前に、スコア基準も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7aa67-108">Scoring criteria must also be set up before you can complete this procedure.</span></span>

<span data-ttu-id="7aa67-109">仕入先または調達担当者のいずれかとして入札を入力できます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-109">You can enter the bid as either a vendor or a procurement professional.</span></span> <span data-ttu-id="7aa67-110">詳細については、「[仕入先コラボレーションの設定と管理](../set-up-maintain-vendor-collaboration.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7aa67-110">For more information, see [Set up and maintain vendor collaboration](../set-up-maintain-vendor-collaboration.md).</span></span>

## <a name="enter-a-reply-as-a-vendor"></a><span data-ttu-id="7aa67-111">仕入先として返信を入力する</span><span class="sxs-lookup"><span data-stu-id="7aa67-111">Enter a reply as a vendor</span></span>

1. <span data-ttu-id="7aa67-112">ダッシュボードで、**仕入先の入札**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-112">On the dashboard, select **Vendor bidding**.</span></span>
2. <span data-ttu-id="7aa67-113">**新しい入札の招待**の一覧で、送信したばかりの RFQ を見つけます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-113">In the **New bid invitations** list, find an RFQ that was just sent.</span></span> <span data-ttu-id="7aa67-114">RFQ を選択して、要求された内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-114">Select the RFQ to review what was requested.</span></span>
3. <span data-ttu-id="7aa67-115">追加された添付ファイルを確認するには、**RQF 添付ファイル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-115">Select **RFQ attachments** to review any attachments that have been added.</span></span>
4. <span data-ttu-id="7aa67-116">フィールドを編集できるようにするには、**入札**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-116">Select **Bid** to make the fields editable.</span></span> <span data-ttu-id="7aa67-117">**入札進捗状況**フィールドが**仕入先が更新中**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-117">Notice that the **Bid progress** field is set to **Vendor is updating**.</span></span>
5. <span data-ttu-id="7aa67-118">ヘッダーと明細行で、入札返信から値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-118">On the header and lines, enter the values from the bid reply.</span></span>
6. <span data-ttu-id="7aa67-119">入札に添付ファイルを追加する必要がある場合、**入札の添付ファイル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-119">If any attachments should be added to the bid, select **Bid attachments**.</span></span>
7. <span data-ttu-id="7aa67-120">ドキュメントが必要かどうかを表示するには、**入札ガイダンス項目**クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-120">Select the **Bidding guiding items** FastTab to view whether any documents are required.</span></span>
8. <span data-ttu-id="7aa67-121">RFQ が修正されたかどうかを確認するには、**修正**クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-121">Select the **Amendments** FastTab to view whether the RFQ has been amended.</span></span>
9. <span data-ttu-id="7aa67-122">**アンケート** クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-122">Select the **Questionnaire** FastTab.</span></span> <span data-ttu-id="7aa67-123">ここに表示されるアンケートには、回答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7aa67-123">Any questionnaires that appear here must be answered.</span></span>
10. <span data-ttu-id="7aa67-124">明細行に関する追加情報を確認するには、**明細行の詳細**クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-124">Select the **Line details** FastTab to view extended information about the line.</span></span>
11. <span data-ttu-id="7aa67-125">元の RFQ 値に入力された値をリセットする必要がある場合にのみ、**RFQ からのリセット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-125">Select **Reset from RFQ** only if you must reset the values that have been entered to the original RFQ values.</span></span>
12. <span data-ttu-id="7aa67-126">有効期限が過ぎていない限り、入札価格はいつでも保存することができ、後で追加処理を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-126">You can save the bid at any time and do additional processing later, provided that the expiration date and time haven't passed.</span></span> <span data-ttu-id="7aa67-127">この場合、**仕入先の入札**ワークスペースの**進行中の入札**一覧で入札を検索できます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-127">In this case, you can find the bid in the **Bids in progress** list in the **Vendor bidding** workspace.</span></span>
13. <span data-ttu-id="7aa67-128">入札の送信準備ができたら、**送信**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-128">When the bid is ready to be sent, select **Submit**.</span></span> <span data-ttu-id="7aa67-129">入札したくない場合は、**辞退**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-129">If you don't want to bid, select **Decline**.</span></span>

    <span data-ttu-id="7aa67-130">送信された入札は、**仕入先の入札**ワークスペースの**送信済みの入札**一覧で確認できます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-130">Submitted bids are available in the **Submitted bids** list in the **Vendor bidding** workspace.</span></span>

14. <span data-ttu-id="7aa67-131">入札を送信した後は、有効期限の日時より前であればいつでも取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-131">After the bid is submitted, you can recall it at any time before the expiration date and time.</span></span> <span data-ttu-id="7aa67-132">入札を取り消す場合、入札は送信済として処理されないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7aa67-132">Note that when a bid is recalled, it isn't treated as submitted.</span></span>

    <span data-ttu-id="7aa67-133">調達部門によって入札が承認または却下されると、**仕入先入札**ワークスペースの、**落札済の入札**または**失注した入札**の一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-133">When the bid is accepted or rejected by the procurement department, it appears in either the **Awarded bids** or **Lost bids** list in the **Vendor bidding** workspace.</span></span>

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a><span data-ttu-id="7aa67-134">調達担当者として仕入先からの返信を入力する</span><span class="sxs-lookup"><span data-stu-id="7aa67-134">Enter a reply from a vendor as a procurement professional</span></span>

1. <span data-ttu-id="7aa67-135">仕入先の入札を編集するためのアクセス許可が設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7aa67-135">Make sure that the permission to edit vendor bids is set up.</span></span> <span data-ttu-id="7aa67-136">**調達 \> セットアップ \> 調達パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-136">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span> <span data-ttu-id="7aa67-137">**見積依頼**タブで、**購買担当者は仕入先入札を編集可能**のオプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-137">On the **Request for quotations** tab, set the **Purchaser can edit vendors bid** option to **Yes**.</span></span>
2. <span data-ttu-id="7aa67-138">**調達 \> 見積依頼 \> すべての見積依頼**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-138">Go to **Procurement and sourcing \> Requests for quotations \> All requests for quotations**.</span></span>
3. <span data-ttu-id="7aa67-139">ステータスが**送信済**の RFQ を選択し、次に**見積依頼ケース** フィールドでリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-139">Select an RFQ that has a status of **Sent**, and then select the link in the **Request for quotation case** field.</span></span>
4. <span data-ttu-id="7aa67-140">**返信を管理する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-140">Select **Manage replies**.</span></span> <span data-ttu-id="7aa67-141">表示されるページには、入札に招待された各仕入先の RFQ が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-141">The page that appears shows an RFQ for each vendor that was invited to bid.</span></span>
5. <span data-ttu-id="7aa67-142">未返信の RFQ を選択してください。</span><span class="sxs-lookup"><span data-stu-id="7aa67-142">Select an RFQ that hasn't been replied to.</span></span> <span data-ttu-id="7aa67-143">(**返信進捗状況**フィールドは、**開始されていません**に設定する必要があります。)</span><span class="sxs-lookup"><span data-stu-id="7aa67-143">(The **Reply progress** field should be set to **Not started**.)</span></span>
6. <span data-ttu-id="7aa67-144">**編集 \> RFQ 返信の編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-144">Select **Edit \> Edit RFQ reply**.</span></span>

    <span data-ttu-id="7aa67-145">**RFQ 返信**ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-145">The **RFQ reply** page appears.</span></span> <span data-ttu-id="7aa67-146">調達担当者として、仕入先の代わって返信を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-146">As a procurement professional, you can now enter the reply on behalf of the vendor.</span></span> <span data-ttu-id="7aa67-147">**入札進捗状況**フィールドが、**購買担当者が更新中**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-147">Notice that the **Bid progress** field is set to **Purchaser is updating**.</span></span>

7. <span data-ttu-id="7aa67-148">入札データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-148">Enter the bid data.</span></span> <span data-ttu-id="7aa67-149">完了したら、**送信**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-149">When you've finished, select **Submit**.</span></span>

## <a name="score-the-bids"></a><span data-ttu-id="7aa67-150">入札を記録する</span><span class="sxs-lookup"><span data-stu-id="7aa67-150">Score the bids</span></span>

1. <span data-ttu-id="7aa67-151">**すべての見積依頼**のページで、返信を記録したい RFQ ケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-151">On the **All requests for quotations** page, select the RFQ case that you want to score replies for.</span></span>
2. <span data-ttu-id="7aa67-152">**返信を管理する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-152">Select **Manage replies**.</span></span>
3. <span data-ttu-id="7aa67-153">記録する返信を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-153">Select the reply to score.</span></span>
4. <span data-ttu-id="7aa67-154">入札のスコアを表示できるように、**ヘッダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-154">Select **Header** so that you can view the scoring for the bid.</span></span>
5. <span data-ttu-id="7aa67-155">**入札スコア** クイック タブで、スコア基準のいずれかについて、**スコア** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-155">On the **Bid scoring** FastTab, enter a number in the **Score** field for one of the scoring criteria.</span></span>

    <span data-ttu-id="7aa67-156">スコア基準をポイントすると、ツールチップがスコア付けすべき範囲を表示します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-156">If you hover over a scoring criterion, a tooltip shows the range that the score must be within.</span></span> <span data-ttu-id="7aa67-157">このデモで、スコア基準のどこにでも 1 ~ 5 の数字を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-157">In this demo, you can enter a number between 1 and 5 for any of the scoring criteria.</span></span>

6. <span data-ttu-id="7aa67-158">他のスコア基準に対して、手順 5 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-158">Repeat step 5 for another scoring criterion.</span></span>
7. <span data-ttu-id="7aa67-159">RFQ ケースで仕入先に送信されたアンケートがある場合は、**アンケート** クイック タブに仕入先の回答を入力できます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-159">If the RFQ case has a questionnaire that was sent to the vendors, you can enter the vendor responses on the **Questionnaires** FastTab.</span></span>
8. <span data-ttu-id="7aa67-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-160">Close the page.</span></span>
9. <span data-ttu-id="7aa67-161">その他の入札すべてについて、手順 1 ~ 8 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-161">Repeat steps 1 through 8 for all the other bids.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="7aa67-162">回答を比較します</span><span class="sxs-lookup"><span data-stu-id="7aa67-162">Compare the replies</span></span>

1. <span data-ttu-id="7aa67-163">アクション ペインの**一般**タブで、**回答の比較**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-163">On the Action Pane, on the **General** tab, select **Compare replies**.</span></span>
2. <span data-ttu-id="7aa67-164">**ランク** フィールドに数字を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-164">In the **Rank** field, enter a number.</span></span>

    <span data-ttu-id="7aa67-165">このページはヘッダーと明細行の情報によって入札を、さらにヘッダー レベル上で合計スコアを表示します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-165">This page shows the bids, together with the header and line information, and also the total score at the header level.</span></span> <span data-ttu-id="7aa67-166">グリッドを並び替えをすることによって、類似する行が隣同士になり行を比較することができます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-166">You can compare the lines by sorting the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="7aa67-167">次の情報も含まれます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-167">The following information is also included:</span></span>

    - <span data-ttu-id="7aa67-168">**数量** – 仕入先が見積もりした数量。</span><span class="sxs-lookup"><span data-stu-id="7aa67-168">**Quantity** – The quantity that the vendor quoted.</span></span> <span data-ttu-id="7aa67-169">この数量は RFQ で指定された数量と一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="7aa67-169">This quantity might not equal the quantity that is specified in the RFQ.</span></span>
    - <span data-ttu-id="7aa67-170">**正味金額** – 仕入先が明細行の品目について見積もりした価格から、割引を差し引いたもの。</span><span class="sxs-lookup"><span data-stu-id="7aa67-170">**Net amount** – The price that the vendor quoted for the items on the line, minus any discounts.</span></span>
    - <span data-ttu-id="7aa67-171">**誤差** – 入札ヘッダーまたは明細行の配送日と、RFQ ヘッダーまたは RFQ 明細行で要求した配送日との日数差。</span><span class="sxs-lookup"><span data-stu-id="7aa67-171">**Deviation** – The number of days by which the delivery date on the bid header or line differs from the requested delivery date on the RFQ header or line.</span></span> <span data-ttu-id="7aa67-172">それぞれの入札ごとに、ランクを入力できます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-172">You can enter a rank for each bid.</span></span>

3. <span data-ttu-id="7aa67-173">ランク付けする他の入札のヘッダー行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-173">Select the header line for the other bid that you want to rank.</span></span>
4. <span data-ttu-id="7aa67-174">**ランク** フィールドに数字を入力します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-174">In the **Rank** field, enter a number.</span></span>
5. <span data-ttu-id="7aa67-175">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-175">Select **Save**.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="7aa67-176">入札を却下します</span><span class="sxs-lookup"><span data-stu-id="7aa67-176">Reject a bid</span></span>

1. <span data-ttu-id="7aa67-177">却下する入札のヘッダー行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-177">Select the header line for the bid that you want to reject.</span></span>

    <span data-ttu-id="7aa67-178">一度に 1 つの入札または 1 つの入札のみの明細行を承認、却下、あるいは返却することができます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-178">You can accept, reject, or return only one bid or the lines on only one bid at a time.</span></span>

2. <span data-ttu-id="7aa67-179">**マーク** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-179">Select the **Mark** check box.</span></span>

    <span data-ttu-id="7aa67-180">入札のヘッダーの**マーク** チェック ボックスを選択すると、すべての明細行もマークされます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-180">If you select the **Mark** check box on the header of the bid, all the lines are also marked.</span></span> <span data-ttu-id="7aa67-181">入札の明細行の一部のみを却下または承認するには、それらの明細行だけをマークします。</span><span class="sxs-lookup"><span data-stu-id="7aa67-181">To reject or accept only some of the lines on the bid, you can mark just those lines.</span></span> <span data-ttu-id="7aa67-182">また、RFQ の一部の明細行の 1 つのベンダー入札を承認し、他の RFQ 明細行は別のベンダーに付与できます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-182">Additionally, you can accept one vendor's bid for some lines of an RFQ and then award other RFQ lines to a different vendor.</span></span> <span data-ttu-id="7aa67-183">ただし、一度に 1 回ずつ入札する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7aa67-183">However, you must do one bid at a time.</span></span>

    <span data-ttu-id="7aa67-184">代替明細行がある場合は、元の入札明細行または代替明細行のいずれかを承認でき、両方を承認することはできません。</span><span class="sxs-lookup"><span data-stu-id="7aa67-184">If alternate lines are present, you can accept either the original bid line or its alternate, but not both.</span></span>

3. <span data-ttu-id="7aa67-185">**却下**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-185">Select **Reject**.</span></span>
4. <span data-ttu-id="7aa67-186">**パラメーター**を選択し、**却下理由**フィールドで、入札を却下する理由を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-186">Select **Parameters**, and then, in the **Reason reject** field, enter or select your reason for rejecting the bid.</span></span>

    <span data-ttu-id="7aa67-187">理由は返信に格納されています。</span><span class="sxs-lookup"><span data-stu-id="7aa67-187">The reason is stored in the reply.</span></span>

5. <span data-ttu-id="7aa67-188">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-188">Select **OK**.</span></span>
6. <span data-ttu-id="7aa67-189">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-189">Select **OK**.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="7aa67-190">入札を承認します</span><span class="sxs-lookup"><span data-stu-id="7aa67-190">Accept a bid</span></span>

1. <span data-ttu-id="7aa67-191">承認する入札を選択してから、**見積依頼**フィールドのリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-191">Select the bid to accept, and then select the link in the **Request for quotation** field.</span></span>

    <span data-ttu-id="7aa67-192">**見積依頼の返信の比較**ページが表示されている場合、フォーカスのある強調表示されている入札は、システムが承認アクション中に検討する入札です。</span><span class="sxs-lookup"><span data-stu-id="7aa67-192">If you're on the **Compare request for quotation replies** page, the highlighted bid that has focus is the bid that the system will consider during the Accept action.</span></span> <span data-ttu-id="7aa67-193">一度に 1 つの入札からのみ明細行を承認することができます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-193">You can accept lines from only one bid at a time.</span></span>

2. <span data-ttu-id="7aa67-194">アクション ペインで、**返信**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-194">On the Action Pane, select **Reply**.</span></span>
3. <span data-ttu-id="7aa67-195">**受け入れる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-195">Select **Accept**.</span></span>

    <span data-ttu-id="7aa67-196">特定の明細行のみをマークした場合、承認アクションにはその明細行のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-196">If you marked only specific lines, the Accept action will include only those lines.</span></span> <span data-ttu-id="7aa67-197">もし入札のすべての明細行を承認したい場合は、明細行をマークする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7aa67-197">If you want to accept all the lines on the bid, you don't have to mark the lines.</span></span>

4. <span data-ttu-id="7aa67-198">**パラメーター**を選択し、**承認理由**フィールドで、入札を承認する理由を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-198">Select **Parameters**, and then, in the **Reason accept** field, enter or select your reason for accepting the bid.</span></span>

    <span data-ttu-id="7aa67-199">理由は入札に格納されています。</span><span class="sxs-lookup"><span data-stu-id="7aa67-199">The reason is stored in the bid.</span></span>

5. <span data-ttu-id="7aa67-200">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-200">Select **OK**.</span></span>
6. <span data-ttu-id="7aa67-201">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-201">Select **OK**.</span></span>

    <span data-ttu-id="7aa67-202">**OK** をクリックすると、RFQ 承認に含まれる明細行に基づいて発注書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-202">When you select **OK**, a purchase order is generated based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="7aa67-203">処理 (承認、却下、または返品) されていない他の入札がある場合は、それらを却下するようシステムから要求されます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-203">If there are other bids that haven't been processed (accepted, rejected, or returned), the system prompts you to reject them.</span></span>

## <a name="view-the-purchase-order-that-is-generated"></a><span data-ttu-id="7aa67-204">生成された発注書を表示する</span><span class="sxs-lookup"><span data-stu-id="7aa67-204">View the purchase order that is generated</span></span>

- <span data-ttu-id="7aa67-205">アクション ペインの**一般**タブで、**発注書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7aa67-205">On the Action Pane, on the **General** tab, select **Purchase order**.</span></span>

    <span data-ttu-id="7aa67-206">表示されるページに、入札を承認したときに生成された発注書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7aa67-206">The page that appears shows the purchase order that was generated when you accepted the bid.</span></span>
