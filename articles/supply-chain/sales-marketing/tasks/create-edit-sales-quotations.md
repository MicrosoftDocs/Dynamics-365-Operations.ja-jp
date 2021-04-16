---
title: 販売見積の作成および編集
description: この手順は、販売見積を作成および更新する方法を示します。
author: omulvad
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable, CustQuotationConfirmationJournal, CustQuotationJournal, CustSalesLines, SalesQuotationCopying, SalesQuotationDeleteQuotations, SalesQuotationListPagePreviewPane, SalesQuotationTypeGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51e80cf500181601cf6e0d2910b91c429c404f01
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836449"
---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="8da17-103">販売見積の作成および編集</span><span class="sxs-lookup"><span data-stu-id="8da17-103">Create and edit sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8da17-104">この手順は、販売見積を作成および更新する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8da17-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="8da17-105">この手順は、独自のデータで、またはデモ データの会社 USMF のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="8da17-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="8da17-106">販売見積の作成</span><span class="sxs-lookup"><span data-stu-id="8da17-106">Create a sales quotation</span></span>
1. <span data-ttu-id="8da17-107">**ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > 販売見積 > すべての見積** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8da17-107">Go to **Navigation pane > Modules > Sales and marketing > Sales quotations > All quotations**.</span></span>
2. <span data-ttu-id="8da17-108">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-108">Click **New**.</span></span>
3. <span data-ttu-id="8da17-109">**勘定タイプ** フィールドで、「見込顧客」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8da17-109">In the **Account type** field, select 'Prospect'.</span></span>
4. <span data-ttu-id="8da17-110">**見込顧客** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8da17-110">In the **Prospect** field, enter or select a value.</span></span>
5. <span data-ttu-id="8da17-111">**一般** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="8da17-111">Expand the **General** section.</span></span> <span data-ttu-id="8da17-112">販売とマーケティング領域から見積書を作成する選択をしたため、タイプは自動的に「販売見積」に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8da17-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to 'Sales quotation'.</span></span> <span data-ttu-id="8da17-113">プロジェクトの見積書を作成するには、**プロジェクト管理および会計** モジュールからアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8da17-113">To create a quotation for a project you must access it from the **Project management and accounting** module.</span></span>
6. <span data-ttu-id="8da17-114">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-114">Click **OK**.</span></span> <span data-ttu-id="8da17-115">見積明細行のフィールドおよびアクションは、販売注文明細行のフィールドおよびアクションに非常に似ています。</span><span class="sxs-lookup"><span data-stu-id="8da17-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="8da17-116">販売注文と同様に、見積は特定の品目に対して作成できます。品目番号がわかっていないか、見積の作成時に存在しない場合、見積は販売カテゴリに対して作成できます。</span><span class="sxs-lookup"><span data-stu-id="8da17-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>     
7. <span data-ttu-id="8da17-117">**品目** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8da17-117">In the **Item** field, enter or select a value.</span></span>
8. <span data-ttu-id="8da17-118">**サイト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8da17-118">In the **Site** field, type a value.</span></span>
9. <span data-ttu-id="8da17-119">**数量** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8da17-119">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="8da17-120">明細行で選択した品目の有効な売買契約が存在する場合、適用できる価格と割引は見積明細行に自動的にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8da17-120">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="8da17-121">[単価] フィールドに値が含まれていることを確認します。割引の値も入力できます。</span><span class="sxs-lookup"><span data-stu-id="8da17-121">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span> 
10. <span data-ttu-id="8da17-122">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-122">Click **Save**.</span></span>
11. <span data-ttu-id="8da17-123">**アクション ウィンドウ** で、**販売見積** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-123">On the **Action Pane**, click **Sales quotation**.</span></span>
12. <span data-ttu-id="8da17-124">**合計** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-124">Click **Totals**.</span></span>
13. <span data-ttu-id="8da17-125">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-125">Click **OK**.</span></span>
14. <span data-ttu-id="8da17-126">販売見積明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="8da17-126">Select the sales quotation line.</span></span>
15. <span data-ttu-id="8da17-127">**アクション ウィンドウ** で、**見積書** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-127">On the **Action Pane**, click **Quotation**.</span></span>
16. <span data-ttu-id="8da17-128">**価格シミュレーション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-128">Click **Price simulation**.</span></span>
    - <span data-ttu-id="8da17-129">**価格シミュレーションの実行** ページでは、目的の単価、割引金額、割引率、合計金額、利益または利益率に基づいての見積の予測売上または収益性の調整を実験できます。</span><span class="sxs-lookup"><span data-stu-id="8da17-129">In the **Run price simulation** page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span> <span data-ttu-id="8da17-130">目標数値に問題がなければ、見積明細行に提案を適用し、価格関連フィールドがそれに応じて更新されます。</span><span class="sxs-lookup"><span data-stu-id="8da17-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    - <span data-ttu-id="8da17-131">思い通りの価格シミュレーションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8da17-131">You can create as many price simulations as you wish.</span></span> <span data-ttu-id="8da17-132">**新規** をクリックすると、現在の見積明細行の価格条件がページにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8da17-132">When you click **New**, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="8da17-133">いずれかの価格関連フィールドの値をターゲット値に変更できます。</span><span class="sxs-lookup"><span data-stu-id="8da17-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="8da17-134">1 つのフィールドの変更により、他のすべてのフィールドの再計算が発生します。</span><span class="sxs-lookup"><span data-stu-id="8da17-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="8da17-135">販売の利益幅と利益率をシステムが計算するためには、製品の単位コストが明らかになっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8da17-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="8da17-136">[シミュレーション価格] タブを使用して、見積合計上にある元の価格、提案された変更およびその効果の詳細表示をします。</span><span class="sxs-lookup"><span data-stu-id="8da17-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span> <span data-ttu-id="8da17-137">一般に、新しい金額を設定するシミュレーションが見積明細行に適用されると、システムは [単価] フィールドに新しい値を再計算して入力します。</span><span class="sxs-lookup"><span data-stu-id="8da17-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="8da17-138">シミュレーションが新しい利益幅と新しい利益率に基づく場合は、[正味金額] フィールドのみが更新され、[単価] は空白になります。</span><span class="sxs-lookup"><span data-stu-id="8da17-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="8da17-139">どちらの場合も、シミュレーション前の見積明細行に含まれていた割引は削除されます。</span><span class="sxs-lookup"><span data-stu-id="8da17-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>
17. <span data-ttu-id="8da17-140">**アクション ウィンドウ** で、**見積書** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-140">On the **Action Pane**, click **Quotation**.</span></span>
18. <span data-ttu-id="8da17-141">**見積の送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-141">Click **Send quotation**.</span></span>
19. <span data-ttu-id="8da17-142">**見積書の印刷** フィールドで、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8da17-142">Select 'Yes' in the **Print quotation** field.</span></span>
20. <span data-ttu-id="8da17-143">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-143">Click **OK**.</span></span> <span data-ttu-id="8da17-144">レポートが生成するのに、数分かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="8da17-144">The report may take a minute to generate.</span></span> <span data-ttu-id="8da17-145">完了するまでページを閉じないでください。</span><span class="sxs-lookup"><span data-stu-id="8da17-145">Don't close the page until it does so.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="8da17-146">販売見積の更新</span><span class="sxs-lookup"><span data-stu-id="8da17-146">Update a sales quotation</span></span>
1. <span data-ttu-id="8da17-147">**ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > 販売見積 > すべての見積** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8da17-147">Go to **Navigation pane > Modules > Sales and marketing > Sales quotations > All quotations**.</span></span>
2. <span data-ttu-id="8da17-148">**アクション ウィンドウ** で、**フォローアップ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-148">On the **Action Pane**, click **Follow up**.</span></span>
3. <span data-ttu-id="8da17-149">**顧客に変更** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-149">Click **Convert to customer**.</span></span>
4. <span data-ttu-id="8da17-150">**顧客口座** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8da17-150">In the **Customer account** field, type a value.</span></span>
5. <span data-ttu-id="8da17-151">**小切手** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-151">Click **Check**.</span></span> <span data-ttu-id="8da17-152">入力した勘定番号が使用可能であるというメッセージの表示を確認します。</span><span class="sxs-lookup"><span data-stu-id="8da17-152">Make sure you see a message that the account number you typed in is free to use.</span></span>  
6. <span data-ttu-id="8da17-153">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-153">Click **OK**.</span></span> <span data-ttu-id="8da17-154">システムは、見積の見込顧客用の新しい顧客 ID を作成しています。</span><span class="sxs-lookup"><span data-stu-id="8da17-154">The system has now created a new customer account for the prospect on the quotation.</span></span>  
7. <span data-ttu-id="8da17-155">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8da17-155">Close the page.</span></span>
8. <span data-ttu-id="8da17-156">**アクション ウィンドウ** で、**フォローアップ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-156">On the **Action Pane**, click **Follow up**.</span></span>
9. <span data-ttu-id="8da17-157">**確定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-157">Click **Confirm**.</span></span>
10. <span data-ttu-id="8da17-158">**理由** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8da17-158">In the **Reason** field, enter or select a value.</span></span>
11. <span data-ttu-id="8da17-159">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-159">Click **OK**.</span></span>
12. <span data-ttu-id="8da17-160">**アクション ウィンドウ** で、**一般** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-160">On the **Action Pane**, click **General**.</span></span>
13. <span data-ttu-id="8da17-161">**販売注文** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8da17-161">Click **Sales orders**.</span></span>
14. <span data-ttu-id="8da17-162">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8da17-162">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]