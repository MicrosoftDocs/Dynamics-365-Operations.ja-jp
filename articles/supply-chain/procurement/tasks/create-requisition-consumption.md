---
title: 消費要求の作成
description: この手順では、要求作成のプロセスを説明します。
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81ca3966cf7dae88468ccf107b52b8c3d7b323d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "366561"
---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="1bcf8-103">消費要求の作成</span><span class="sxs-lookup"><span data-stu-id="1bcf8-103">Create a requisition for consumption</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1bcf8-104">この手順では、要求作成のプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="1bcf8-105">調達カタログで製品を検索するさまざまな方法と、カタログに存在しない製品を追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-105">It shows you different ways to search for products in your procurement catalog and how to add a product that isn’t in your catalog.</span></span> <span data-ttu-id="1bcf8-106">この手順を開始する前に、[消費] を要求の既定のタイプとして設定した購買ポリシーがある必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="1bcf8-107">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="1bcf8-108">この手順は、ユーザー プロファイルが作業者として設定されているユーザーのみ実施できます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="1bcf8-109">通常、このタスクを実施するのは、従業員です。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="1bcf8-110">従業員の採用セキュリティ ロールにより、タスクを実行することができます。または、USMF を使用する場合に、アリシアとしてログインできます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="1bcf8-111">新しい要求の作成</span><span class="sxs-lookup"><span data-stu-id="1bcf8-111">Create a new requisition</span></span>
1. <span data-ttu-id="1bcf8-112">[調達] > [購買要求] > [自分自身が作成した購買要求] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="1bcf8-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-113">Click New.</span></span>
3. <span data-ttu-id="1bcf8-114">[名前] フィールドに、要求の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="1bcf8-115">[要求日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="1bcf8-116">既定では、要求日と会計日が購買要求明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="1bcf8-117">日付は、明細行レベルで変更できます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-117">They can be changed at the line level.</span></span> <span data-ttu-id="1bcf8-118">要求日は、要求する配送日です。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="1bcf8-119">[会計日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="1bcf8-120">転記日は、一般会計に会計入力を記録し、予算資金が使用可能かどうかを検証する日付です。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="1bcf8-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-121">Click OK.</span></span>
7. <span data-ttu-id="1bcf8-122">[理由] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1bcf8-123">選択した業務の妥当性の理由は、既定で、購買要求明細行に対して表示されますが、明細行レベルで変更できます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="1bcf8-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="1bcf8-125">理由を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-125">Select the reason</span></span>
10. <span data-ttu-id="1bcf8-126">[詳細] フィールドで、要求のより詳しい妥当性を入力します</span><span class="sxs-lookup"><span data-stu-id="1bcf8-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="1bcf8-127">要求への行の追加</span><span class="sxs-lookup"><span data-stu-id="1bcf8-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="1bcf8-128">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-128">Click Add line.</span></span>
    * <span data-ttu-id="1bcf8-129">購買要求に明細行を追加するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="1bcf8-130">製品番号が既にわかっている場合、または製品カタログに存在しない製品を要求していることが既にわかっている場合は、[行の追加] で明細行を直接追加できます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalog, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="1bcf8-131">別の方法として、検索やフィルター処理を使用して製品カタログで品目を見つけることができる [製品の追加] を使う方法があります。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalog.</span></span>    
2. <span data-ttu-id="1bcf8-132">作成した行をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="1bcf8-133">要求者は、要求を指定した作業者です。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="1bcf8-134">既定では、請求を準備する担当者は、それを要求した作業者です。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="1bcf8-135">別の作業者に代わって要求明細行を準備するためのアクセス許可を得る必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="1bcf8-136">このようなアクセス許可がある場合、他の作業者がこのルックアップに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="1bcf8-137">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1bcf8-138">選択できる品目は、購買組織のカテゴリ アクセス ポリシーおよび調達カタログによって制限されます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-138">The items that are available for you to choose are limited by the category access policy and the procurement catalog for the buying legal entity.</span></span>   
4. <span data-ttu-id="1bcf8-139">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="1bcf8-140">要求へ製品をさらに追加</span><span class="sxs-lookup"><span data-stu-id="1bcf8-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="1bcf8-141">[製品の追加]をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-141">Click Add products.</span></span>
    * <span data-ttu-id="1bcf8-142">これは、製品カタログで製品を検索できるオプションです。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-142">This is the option where you can search for products in the product catalog.</span></span>    
2. <span data-ttu-id="1bcf8-143">[調達カテゴリ ノードの検索] フィールドで、探しているカテゴリの名前の最初の部分を入力し、[入力] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="1bcf8-144">たとえば、「comput」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-144">For example, type comput.</span></span>  
3. <span data-ttu-id="1bcf8-145">[InvokeDefaultButton] ショートカットを使用します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="1bcf8-146">選択されているカタログの製品リストをフィルター処理するためには [フィルター] 使用します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="1bcf8-147">要求に追加する製品カードを選択します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="1bcf8-148">[明細行に追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-148">Click Add to lines.</span></span>
7. <span data-ttu-id="1bcf8-149">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="1bcf8-150">[調達カテゴリ ノードの検索] フィールドで、探しているカテゴリの名前の最初の部分を入力し、[入力] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="1bcf8-151">たとえば、「High」(蛍光ペン) と入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="1bcf8-152">[InvokeDefaultButton] ショートカットを使用します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="1bcf8-153">[リストに記載されていない製品を明細行に追加] をクリックして、調達カタログに記載されていない製品を追加します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalog.</span></span>
11. <span data-ttu-id="1bcf8-154">[製品名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="1bcf8-155">[単位] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="1bcf8-156">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-156">Click OK.</span></span>
14. <span data-ttu-id="1bcf8-157">[品目の説明] フィールドに、製品の説明を追加します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="1bcf8-158">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="1bcf8-159">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="1bcf8-160">([仕入先勘定] フィールドで選択する) 特定の仕入先の価格がわかっている場合は、その価格を入力できます</span><span class="sxs-lookup"><span data-stu-id="1bcf8-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="1bcf8-161">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1bcf8-162">このフィールドで使用できる仕入先は、購買ポリシー、および現在の調達カテゴリに関する仕入先の状態に依存します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="1bcf8-163">ここで仕入先を選択する代わりに、[仕入先の提案] ボタンをクリックできます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="1bcf8-164">リストで、使用する仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="1bcf8-165">[外部品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="1bcf8-166">これは、仕入先によりわかる製品の参照番号です。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="1bcf8-167">たとえば、これは、仕入先固有のカタログの製品の品目番号にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-167">For example, this could be the item number of the product in the vendor's own catalog.</span></span>  
20. <span data-ttu-id="1bcf8-168">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="1bcf8-169">金額の配分</span><span class="sxs-lookup"><span data-stu-id="1bcf8-169">Distribute amounts</span></span>
1. <span data-ttu-id="1bcf8-170">[財務] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-170">Click Financials.</span></span>
2. <span data-ttu-id="1bcf8-171">[金額の配分] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="1bcf8-172">このプロセスは、2 つの勘定間の最初の行の原価を配分する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="1bcf8-173">これは、要求のレビュー後にも実行できます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="1bcf8-174">[分割] をクリックして、新しい配分ラインを作成します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="1bcf8-175">[勘定科目] フィールドで、原価の一部を取得する最初の原価部門を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-175">In the Ledger account field select the first cost center that should take part of the cost.</span></span>
5. <span data-ttu-id="1bcf8-176">他の配分ラインを選択します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="1bcf8-177">[勘定科目] フィールドで、他の原価部門を指定します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-177">In the Ledger account field specify the other cost center.</span></span>
7. <span data-ttu-id="1bcf8-178">[均等な配分] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="1bcf8-179">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="1bcf8-180">行の詳細の表示</span><span class="sxs-lookup"><span data-stu-id="1bcf8-180">View line details</span></span>
1. <span data-ttu-id="1bcf8-181">[明細行の詳細] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="1bcf8-182">要求の送信</span><span class="sxs-lookup"><span data-stu-id="1bcf8-182">Submit the requisition</span></span>
1. <span data-ttu-id="1bcf8-183">[ワークフロー] をクリックすると、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="1bcf8-184">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-184">Click Submit.</span></span>
3. <span data-ttu-id="1bcf8-185">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-185">Close the page.</span></span>
4. <span data-ttu-id="1bcf8-186">[コメント] フィールドで、要求の承認者のメモを入力します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="1bcf8-187">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-187">Click Submit.</span></span>
6. <span data-ttu-id="1bcf8-188">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-188">Close the page.</span></span>
7. <span data-ttu-id="1bcf8-189">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="1bcf8-189">Refresh the page.</span></span>

