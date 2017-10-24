--- 
title: "RFQ 入札価格の入力と比較および契約の授与"
description: "この手順は、RFQ への返信を入力したり、入札の記録や比較をしたり、また仕入先の 1 つに入札を付与する方法を示します。"
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="7d6e4-103">RFQ 入札価格の入力と比較および契約の授与</span><span class="sxs-lookup"><span data-stu-id="7d6e4-103">Enter and compare RFQ bids and award contracts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d6e4-104">この手順は、RFQ への返信を入力したり、入札の記録や比較をしたり、また仕入先の 1 つに入札を付与する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="7d6e4-105">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="7d6e4-106">開始する前に、少なくとも 2 つの仕入先に送信された、2 つの明細行から成る RFQ が必要になります。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="7d6e4-107">「見積依頼の作成」手順を前提条件として実行しながら、これを作成できます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="7d6e4-108">この手順を実行する前に、スコア基準を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="7d6e4-109">仕入先からの返信を入力します</span><span class="sxs-lookup"><span data-stu-id="7d6e4-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="7d6e4-110">[調達] > [見積依頼] > [すべての見積依頼] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="7d6e4-111">[送信済] ステータスがある RFQ を選択し、[見積依頼] のケース番号にあるリンクをクリックして下さい。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="7d6e4-112">RFQ は、少なくとも 2 箇所の仕入先に送付される必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="7d6e4-113">仕入先の一覧に移動するには、[ヘッダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="7d6e4-114">RFQ で回答を入力してほしい仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="7d6e4-115">[入力] をクリックして回答します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-115">Click Enter reply.</span></span>
6. <span data-ttu-id="7d6e4-116">[アクション ペイン] で、[返信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="7d6e4-117">[データのコピー] をクリックして返信します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="7d6e4-118">このアクションは、例えば RFQ ケースから RFQ 返信への数量、のように選択されたデータをコピーします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="7d6e4-119">またはこのアクションをスキップし、返信を編集する際に手動ですべての回答フィールドに記入することもできます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="7d6e4-120">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-120">Click Edit.</span></span>
9. <span data-ttu-id="7d6e4-121">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="7d6e4-122">他の見積明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="7d6e4-123">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="7d6e4-124">入札を記録します</span><span class="sxs-lookup"><span data-stu-id="7d6e4-124">Score the bid</span></span>
1. <span data-ttu-id="7d6e4-125">入札のスコアに移動するには、[ヘッダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="7d6e4-126">[入札スコア] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="7d6e4-127">[スコア] フィールドで、いずれかのスコア基準の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="7d6e4-128">いずれかのスコア基準をポイントすると、ツールチップがスコア付けすべき範囲を表示します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="7d6e4-129">このデモで基準のどこにでも 1 ~ 5 の番号を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="7d6e4-130">別のスコア基準を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="7d6e4-131">[スコア] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="7d6e4-132">[アンケート] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="7d6e4-133">RFQ ケースで仕入先に送信されたアンケートがある場合は、アンケート セクションにそれらの回答を入力できます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="7d6e4-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="7d6e4-135">別の仕入先の返信を入力します</span><span class="sxs-lookup"><span data-stu-id="7d6e4-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="7d6e4-136">すでに返信を入力した仕入先をオフにしてから、次の仕入先の行を選択することによって、新たな仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="7d6e4-137">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7d6e4-138">[入力] をクリックして回答します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-138">Click Enter reply.</span></span>
4. <span data-ttu-id="7d6e4-139">[データのコピー] をクリックして返信します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="7d6e4-140">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-140">Click Edit.</span></span>
6. <span data-ttu-id="7d6e4-141">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="7d6e4-142">他の見積明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="7d6e4-143">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="7d6e4-144">2 番目の入札を記録します</span><span class="sxs-lookup"><span data-stu-id="7d6e4-144">Score the second bid</span></span>
1. <span data-ttu-id="7d6e4-145">入札スコアに移動するには、[ヘッダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="7d6e4-146">[スコア] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="7d6e4-147">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7d6e4-148">[スコア] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="7d6e4-149">回答を比較します</span><span class="sxs-lookup"><span data-stu-id="7d6e4-149">Compare the replies</span></span>
1. <span data-ttu-id="7d6e4-150">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="7d6e4-151">[回答の比較] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-151">Click Compare replies.</span></span>
3. <span data-ttu-id="7d6e4-152">[ランク] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="7d6e4-153">このページはヘッダーと明細行によって入札を、さらにヘッダー レベル上で合計スコアを表示します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="7d6e4-154">グリッドで並び替えをすることによって、類似する行が隣同士になり行を比較することができます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="7d6e4-155">その情報には、次の点も含まれます。数量: 仕入先が見積もった数量。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="7d6e4-156">これは RFQ で指定された数量と一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="7d6e4-157">正味金額: 明細行の品目に対する割引を差し引いた後の仕入先の見積価格。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="7d6e4-158">誤差: 入札ヘッダーまたは明細行の配送日と、RFQ ヘッダーまたは RFQ 明細行で要求した配送日との日数差。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="7d6e4-159">それぞれの入札ごとに、ランクを入力できます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="7d6e4-160">ランク付けする他の入札のヘッダー行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="7d6e4-161">[ランク] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="7d6e4-162">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="7d6e4-163">入札を却下します</span><span class="sxs-lookup"><span data-stu-id="7d6e4-163">Reject a bid</span></span>
1. <span data-ttu-id="7d6e4-164">却下する入札のヘッダー行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="7d6e4-165">一度に 1 回の入札または 1 回の入札での明細行を承認、否認、あるいは返却ができるのみです。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="7d6e4-166">[マーク] のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="7d6e4-167">入札のヘッダーの [マーク] チェック ボックスをオンにした場合、すべての明細行もマークされます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="7d6e4-168">さらに入札内の明細行のサブセットをマークして、これらを拒否または承認することもできます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="7d6e4-169">RFQ の一部の明細行には一つの仕入先入札を承認し、それから他の RFQ 明細行は別の仕入先へ付与することは可能ですが、その際この 2 つのステップを一度に 1 回の入札で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="7d6e4-170">代替明細行がある場合は、元の入札明細行または代替明細行のいずれかを承認でき、両方を承認することはできません。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="7d6e4-171">[却下] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-171">Click Reject.</span></span>
4. <span data-ttu-id="7d6e4-172">[パラメーター] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="7d6e4-173">[却下理由] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="7d6e4-174">否認理由は、返信に保存されます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="7d6e4-175">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-175">Click OK.</span></span>
7. <span data-ttu-id="7d6e4-176">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-176">Click OK.</span></span>
8. <span data-ttu-id="7d6e4-177">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-177">Close the page.</span></span>
9. <span data-ttu-id="7d6e4-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-178">Close the page.</span></span>
10. <span data-ttu-id="7d6e4-179">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="7d6e4-180">入札を承認します</span><span class="sxs-lookup"><span data-stu-id="7d6e4-180">Accept a bid</span></span>
1. <span data-ttu-id="7d6e4-181">承認したい入札を選択し、[見積依頼] フィールドのリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="7d6e4-182">[アクション ペイン] で、[返信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="7d6e4-183">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-183">Click Accept.</span></span>
    * <span data-ttu-id="7d6e4-184">他のものでなく特定の明細行をマークした場合、承認アクションはマークした明細行だけを含みます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="7d6e4-185">もし入札のすべての明細行を承認したい場合は、明細行をマークする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="7d6e4-186">[パラメーター] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="7d6e4-187">これによって、入札を承認する理由を記録することができます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="7d6e4-188">その理由は入札に保存されます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="7d6e4-189">[承認理由] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="7d6e4-190">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-190">Click OK.</span></span>
7. <span data-ttu-id="7d6e4-191">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-191">Click OK.</span></span>
    * <span data-ttu-id="7d6e4-192">[OK] をクリックすると、RFQ 承認に含まれる明細行に基づいて発注書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="7d6e4-193">処理 (承認、否認、または返品) されていない他の入札がある場合は、残余入札を拒否するようシステムから要求されます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="7d6e4-194">生成された発注書を表示します</span><span class="sxs-lookup"><span data-stu-id="7d6e4-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="7d6e4-195">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="7d6e4-196">[発注書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-196">Click Purchase order.</span></span>
    * <span data-ttu-id="7d6e4-197">ここで、入札を承認したときに生成された発注書が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="7d6e4-198">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-198">Close the page.</span></span>
4. <span data-ttu-id="7d6e4-199">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-199">Close the page.</span></span>
5. <span data-ttu-id="7d6e4-200">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-200">Close the page.</span></span>
6. <span data-ttu-id="7d6e4-201">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d6e4-201">Close the page.</span></span>


