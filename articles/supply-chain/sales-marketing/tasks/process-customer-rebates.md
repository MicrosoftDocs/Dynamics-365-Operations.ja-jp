--- 
title: "顧客リベートの生成および処理"
description: "この手順は、要求の生成から売掛金勘定への見越計上として顧客リベートを渡すまでの、顧客リベートの処理方法を示します。"
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsRebateAgreement, SalesTableListPage, SalesCreateOrder, SalesTable, MCRPriceHistory, SalesEditLines,  PdsRebateTableListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: d22d4527ee08c2b5251077cfde352b56b9e0e19f
ms.contentlocale: ja-jp
ms.lasthandoff: 09/11/2018

---
# <a name="generate-and-process-customer-rebates"></a><span data-ttu-id="aa7b4-103">顧客リベートの生成および処理</span><span class="sxs-lookup"><span data-stu-id="aa7b4-103">Generate and process customer rebates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa7b4-104">この手順は、要求の生成から売掛金勘定への見越計上として顧客リベートを渡すまでの、顧客リベートの処理方法を示します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-104">This procedure demonstrates how to process customer rebates from claim generation to the point of passing them as accruals to Accounts receivable.</span></span> <span data-ttu-id="aa7b4-105">ここでは、リベート明細行のさまざまな条件が、顧客に貸方転記される最終金額にどのように影響するかについて説明する特定の例を示します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-105">It walks you through a specific example to explain how the various conditions on the rebate lines affect the final amounts that will be credited to the customer.</span></span> <span data-ttu-id="aa7b4-106">ガイドを開始する前に、USMF のデモ データ会社を使用して、次のタスクを実行する必要があります。(1) [売掛金勘定パラメーター] ページに移動し、[価格] タブと [価格の詳細] タブを展開し、[価格の詳細の有効化] オプションが [はい] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-106">You need to use the USMF demo data company, and carry out the following tasks before you start the guide: (1) Go to the Accounts receivable parameters page, and expand the Prices tab and then the Price details tab, and check that the Enable price details option is set to Yes.</span></span> <span data-ttu-id="aa7b4-107">(2) [リベート契約] ページに移動し、顧客リベート契約 USMF-000001 を選択します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-107">(2) Go to the Rebate agreements page and select the customer rebate agreement: USMF-000001.</span></span> <span data-ttu-id="aa7b4-108">[ワークフローの承認状態] フィールドが [承認済] に設定されていない場合、アクション ウィンドウで [検証] をクリックして承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-108">If the Workflow approval status field is not set to Approved, you need click Validation on the Action pane to approve it.</span></span>


## <a name="review-a-customer-rebate-agreement"></a><span data-ttu-id="aa7b4-109">顧客リベート契約の確認</span><span class="sxs-lookup"><span data-stu-id="aa7b4-109">Review a customer rebate agreement</span></span>
1. <span data-ttu-id="aa7b4-110">[販売とマーケティング] > [顧客リベート] > [リベート契約] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-110">Go to Sales and marketing > Customer rebates > Rebate agreements.</span></span>
    * <span data-ttu-id="aa7b4-111">次のいくつかの手順では、契約 USMF-000001 の条件を確認します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-111">The next few steps look at the conditions of agreement USMF-000001.</span></span> <span data-ttu-id="aa7b4-112">これにより、顧客貸方の値が手順の後のほうでどのように計算されるかが理解しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-112">This makes it easier to understand how the customer credit values are calculated later in the procedure.</span></span>  
    * <span data-ttu-id="aa7b4-113">契約は顧客ごとです。この例では、顧客 US-009 です。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-113">The agreement is for an individual customer, in this example customer US-009.</span></span>  
    * <span data-ttu-id="aa7b4-114">リベートは、顧客が特定の製品を購入するときに、その顧客に付与されます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-114">Rebates are given to the customer when they purchase a specific product.</span></span> <span data-ttu-id="aa7b4-115">この場合、製品は、品目番号 T0020 をもちます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-115">In this case, the product has item number T0020.</span></span>   
    * <span data-ttu-id="aa7b4-116">リベート金額が見積られている顧客の販売実績は、週単位で累計されます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-116">The customer's sales performance, against which the rebate amounts are estimated, is to be accumulated on a weekly basis.</span></span>  
    * <span data-ttu-id="aa7b4-117">[取得元の価格] の設定は総計なので、見積もられた要求に基づく注文明細行金額は、行割引によって減らされることはありません。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-117">The setting for “Price taken from” is Gross, which means that line's sales amount on which basis the claim is estimated is not reduced by the line discount.</span></span>  
    * <span data-ttu-id="aa7b4-118">[リベート改行タイプ] フィールドにはリベートの計算方法が表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-118">The Rebate line break type field shows the method for calculating rebates.</span></span> <span data-ttu-id="aa7b4-119">この場合、リベートが見積もられた売上目標が、[数量] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-119">In this case, the sales target against which the rebates are to be estimated is set to Quantity.</span></span>   
    * <span data-ttu-id="aa7b4-120">契約の行には、リベート金額タイプ、実際のリベート値、しきい値を指定します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-120">The agreement's lines specify the rebate amount type, the actual rebate value, and the thresholds.</span></span> <span data-ttu-id="aa7b4-121">この例では、製品の週購買が 1 ～ 50 単位内に含まれる場合、販売された単位ごとに 20 USD のリベートが顧客に適用されます。また、50 単位を超えて購入した場合、販売された単位ごとに 40 USD のリベートが顧客に適用されます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-121">In this example, the customer will qualify for a rebate of 20 USD per unit sold, if their weekly purchases of the product fall within 1 to 50 units; and a rebate of 40 USD per unit sold, if they purchase above 50 units.</span></span>  
2. <span data-ttu-id="aa7b4-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-122">Close the page.</span></span>

## <a name="generate-rebate-claims"></a><span data-ttu-id="aa7b4-123">リベート請求の作成</span><span class="sxs-lookup"><span data-stu-id="aa7b4-123">Generate rebate claims</span></span>
1. <span data-ttu-id="aa7b4-124">[販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-124">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="aa7b4-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-125">Click New.</span></span>
    * <span data-ttu-id="aa7b4-126">リベート要求の生成方法を再現するために、次のタスクでは、リベートのための質問で製品と数量が顧客を特定する販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-126">To mimic the way in which rebate claims would be generated, the next task is to create a sales order, where the product and quantity will qualify the customer in question for a rebate.</span></span>  
3. <span data-ttu-id="aa7b4-127">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-127">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="aa7b4-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-128">Click OK.</span></span>
5. <span data-ttu-id="aa7b4-129">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-129">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="aa7b4-130">数量を '40' に設定します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-130">Set Quantity to '40'.</span></span>
7. <span data-ttu-id="aa7b4-131">[販売注文明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-131">Click Sales order line.</span></span>
8. <span data-ttu-id="aa7b4-132">[価格の詳細]をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-132">Click Price details.</span></span>
    * <span data-ttu-id="aa7b4-133">このオプションが表示されない場合は、ガイドを開始する前に [価格の詳細の有効化] オプションを設定していなかったためです。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-133">If you don’t see this option, it’s because you didn’t set the Enable price details option to Yes before you started the guide.</span></span>  
9. <span data-ttu-id="aa7b4-134">[リベート] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-134">Expand the Rebates section.</span></span>
    * <span data-ttu-id="aa7b4-135">[リベート] タブには、現在の注文明細行に適用でき、見積済リベート金額を示すリベート契約がすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-135">The Rebates tab lists all the rebate agreements that are applicable to the current order line and shows the estimated rebate amount.</span></span> <span data-ttu-id="aa7b4-136">表示された金額が、将来のリベート要求を示しているにすぎないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-136">Note that the displayed amounts are only indications of what future rebate claims may be.</span></span> <span data-ttu-id="aa7b4-137">実際のリベート金額は、次の内容によって異なる可能性があります: 定期的なリベート契約で顧客によって達成された合計売上高、顧客が数量の全部または一部を返品たかどうか、適用できる販売注文が請求されたかどうか。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-137">The actual rebate amounts may be different depending on: the total sales volume achieved by the customer under a periodic rebate agreement; whether the customer had returned all or partial quantities; and whether the applicable sales order was invoiced.</span></span>  
10. <span data-ttu-id="aa7b4-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-138">Close the page.</span></span>
11. <span data-ttu-id="aa7b4-139">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-139">Click Add line.</span></span>
12. <span data-ttu-id="aa7b4-140">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-140">In the Item number field, enter or select a value.</span></span>
13. <span data-ttu-id="aa7b4-141">数量を '60' に設定します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-141">Set Quantity to '60'.</span></span>
14. <span data-ttu-id="aa7b4-142">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-142">Click Save.</span></span>
15. <span data-ttu-id="aa7b4-143">アクション ウィンドウで、[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-143">On the Action Pane, click Invoice.</span></span>
16. <span data-ttu-id="aa7b4-144">[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-144">Click Invoice.</span></span>
17. <span data-ttu-id="aa7b4-145">[パラメーター] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-145">Expand the Parameters section.</span></span>
18. <span data-ttu-id="aa7b4-146">[数量] フィールドで、「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-146">In the Quantity field, select 'All'.</span></span>
19. <span data-ttu-id="aa7b4-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-147">Click OK.</span></span>
20. <span data-ttu-id="aa7b4-148">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-148">Click OK.</span></span>

## <a name="process-rebate-claims"></a><span data-ttu-id="aa7b4-149">リベート要求の処理</span><span class="sxs-lookup"><span data-stu-id="aa7b4-149">Process rebate claims</span></span>
1. <span data-ttu-id="aa7b4-150">[販売とマーケティング] > [顧客リベート] > [リベート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-150">Go to Sales and marketing > Customer rebates > Rebates.</span></span>
    * <span data-ttu-id="aa7b4-151">[リベート] ページは、リベート要求の確認、承認、処理を行うワークベンチとして機能します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-151">The Rebates page acts a workbench in which you can review, approve, and process rebate claims.</span></span> <span data-ttu-id="aa7b4-152">リベート契約 USMF-000001 の対象となる顧客 US-009 の販売注文が請求された結果として作成された要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-152">You’ll now process the claims that were created as a result of invoicing a sales order for customer US-009, who is the subject of the rebate agreement USMF-000001.</span></span>   
    * <span data-ttu-id="aa7b4-153">最初の行は、製品 T0020 の 40 単位の販売に基づいて、単位ごとに 20 USD として計算された 800 USD のリベート要求を表します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-153">The first line represents a rebate claim for 800 USD, which is based on the sales of 40 units of product T0020, calculated at 20 USD per unit.</span></span> <span data-ttu-id="aa7b4-154">これは、リベート契約の最初の数量区分の条件と一致します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-154">This matches the conditions of the first quantity break in the rebate agreement.</span></span>  
    * <span data-ttu-id="aa7b4-155">2 番目の要求は、2,400 USD です。これは、製品 T0020 の 60 単位の販売に基づいています。また、契約の 2 番目の数量区分により、1 単位 40 USD として計算されました。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-155">The second claim is for 2,400 USD, which is based on the sales of 60 units of product T0020, calculated at 40 USD per unit, as per the second quantity break in the agreement.</span></span>  
    * <span data-ttu-id="aa7b4-156">両方の要求は、「計算対象」の状態です。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-156">Both claims are in the “To be calculated” state.</span></span> <span data-ttu-id="aa7b4-157">これは、定期的に顧客の販売実績を追跡する契約に関連付けられ、対応する期間内の合計売上高の勘定を再計算する必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-157">This means that they are associated with an agreement that tracks the customer's sales performance on periodic basis and that they have to be re-calculated to account for the total sales volume within the respective period.</span></span>   
2. <span data-ttu-id="aa7b4-158">[累計] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-158">Click Cumulate.</span></span>
3. <span data-ttu-id="aa7b4-159">[顧客] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-159">In the Customer field, enter or select a value.</span></span>
4. <span data-ttu-id="aa7b4-160">[開始日] フィールドで、今日の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-160">In the Start date field, select today's date.</span></span>
5. <span data-ttu-id="aa7b4-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-161">Click OK.</span></span>
    * <span data-ttu-id="aa7b4-162">累計機能を実行した結果、見積要求の金額は、関連する期間の顧客の合計売上高が最初のリベートが生成されたときより高いため、勘定が調整されています。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-162">As a result of running the Cumulate function, the estimated claim amount has now been adjusted to account for the fact that the customer's total sales volume in the relevant period is higher than when the first rebate was generated.</span></span> <span data-ttu-id="aa7b4-163">つまり、購買合計数量が 100 単位に達したため、顧客は、単位ごとに 40 USD (契約の2 番目の数量区分により)、または合計リベート金額の 400 USD を利用できます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-163">More specifically, because the total purchased quantity has reached 100 units, the customer now qualifies for 40 USD per unit (as per the agreement's second quantity break), or 400 USD of total rebate amount.</span></span> <span data-ttu-id="aa7b4-164">差額は、800 USD 追加という新しい要求「調整」として記録されます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-164">The difference is recorded as a new claim "adjustment" for the additional 800 USD.</span></span> <span data-ttu-id="aa7b4-165">累積的な更新プログラムに含まれているリベート要求の状態は、計算済に設定されます。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-165">The status of the rebate claims that were included in the Cumulate update are now set to Calculated.</span></span>   
6. <span data-ttu-id="aa7b4-166">リストで、すべての行をマークします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-166">In the list, mark all rows.</span></span>
7. <span data-ttu-id="aa7b4-167">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-167">Click Approve.</span></span>
8. <span data-ttu-id="aa7b4-168">[プロセス] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-168">Click Process.</span></span>
9. <span data-ttu-id="aa7b4-169">[顧客] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-169">In the Customer field, enter or select a value.</span></span>
10. <span data-ttu-id="aa7b4-170">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-170">Click OK.</span></span>
    * <span data-ttu-id="aa7b4-171">メッセージは、リベートが正常に処理されたことを示し、要求の状態は [マーク] に変更されました。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-171">A message shows that the rebate was processed successfully, and the status of the claims has been changed to Mark.</span></span> <span data-ttu-id="aa7b4-172">これは、リベート見越計上仕訳帳の結果が転記されたことを意味します。a) 要求は、控除として一時顧客残高に転送されました。b) リベート見越計上勘定は、顧客に対する将来の負債を表すために貸方に転記されました。c) リベート経費勘定は、販売に関連して発生した費用を承認するため借方に転記されました。</span><span class="sxs-lookup"><span data-stu-id="aa7b4-172">This means that as a result of a Rebate accrual journal being posted: a) the claims have now been transferred to the temporary customer balance as deductions; b) the Rebate accrual account has been credited to represent the future liability towards the customer; and c) the Rebate expense account has been debited, in recognition of the cost incurred in connection with the sales.</span></span>   


