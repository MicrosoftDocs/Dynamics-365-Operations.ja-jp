--- 
title: "倉庫なしの販売注文の出荷"
description: "このガイドでは、製品が顧客に出荷されたときに販売注文を更新する方法を示します。"
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1d4d43ca62901ecd2280f21dfbeee9cb70ec600e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/11/2018

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="68f57-103">倉庫なしの販売注文の出荷</span><span class="sxs-lookup"><span data-stu-id="68f57-103">Ship sales orders without warehousing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="68f57-104">このガイドでは、製品が顧客に出荷されたときに販売注文を更新する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="68f57-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="68f57-105">このガイドは、倉庫管理 (基本的または詳細な倉庫管理) 用に設定されていないフルフィルメント フローに適用可能です。そのため、出荷前に製品のピッキングを登録する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="68f57-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="68f57-106">この手順は、独自のデータで、またはデモ データの会社 USMF のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="68f57-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="68f57-107">どちらの場合も、このタスクを開始する前に、1 より大きな数量で在庫品目の販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="68f57-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="68f57-108">転記エラーを回避するには、注文で選択したサイトと倉庫の製品の手持数量が注文数量をカバーするのか、確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68f57-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="68f57-109">注文の [梱包明細] の転記</span><span class="sxs-lookup"><span data-stu-id="68f57-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="68f57-110">[販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="68f57-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="68f57-111">一覧で、このタスクに対して作成した注文を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="68f57-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="68f57-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="68f57-113">[アクション] ペインで、[ピッキングと梱包] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="68f57-114">[梱包明細の転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="68f57-115">[パラメーター] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="68f57-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="68f57-116">[数量] フィールドで、「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="68f57-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="68f57-117">他のオプションには、[すぐに出荷する] および [ピッキング済] があります。</span><span class="sxs-lookup"><span data-stu-id="68f57-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="68f57-118">注文明細行が一部出荷済で、注文明細行の [すぐに出荷する] フィールドに数量が含まれる場合は、[すぐに出荷する] を選択します。</span><span class="sxs-lookup"><span data-stu-id="68f57-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="68f57-119">組織のフルフィルメント フローに、ピッキング リストで管理また登録されている別のプロセスとしてピッキングが含まれている場合、[ピッキング済] を選択します。</span><span class="sxs-lookup"><span data-stu-id="68f57-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="68f57-120">[転記] オプションが、[はい] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="68f57-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="68f57-121">[梱包明細の印刷] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="68f57-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="68f57-122">[概要] タブには、この転記で生成される梱包明細の一覧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="68f57-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="68f57-123">個々の注文を出荷する場合、通常 1 つの梱包明細があります。</span><span class="sxs-lookup"><span data-stu-id="68f57-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="68f57-124">ただし、その注文明細行を複数のサイトから出荷する場合、転記は自動的に適切な数のドキュメントに分割されます。</span><span class="sxs-lookup"><span data-stu-id="68f57-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="68f57-125">これは、変更できない必須の条件です。</span><span class="sxs-lookup"><span data-stu-id="68f57-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="68f57-126">同様に、注文明細行が異なる配送先住所に出荷される場合、転記も複数のドキュメントに分割され、出荷ポリシーは分割を必要とするように設定されます。</span><span class="sxs-lookup"><span data-stu-id="68f57-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="68f57-127">[明細行] タブで、出荷する行の注文明細行の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="68f57-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="68f57-128">[更新] フィールドに、元の数量より小さい数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="68f57-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="68f57-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-129">Click OK.</span></span>
12. <span data-ttu-id="68f57-130">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-130">Click Yes.</span></span>
13. <span data-ttu-id="68f57-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="68f57-131">Close the page.</span></span>
14. <span data-ttu-id="68f57-132">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="68f57-133">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-133">Click Change view.</span></span>
16. <span data-ttu-id="68f57-134">[ヘッダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-134">Click Header view.</span></span>
    * <span data-ttu-id="68f57-135">注文の明細行がすべて出荷すると、注文のステータスが [未処理] から [出荷済] に変更されます。</span><span class="sxs-lookup"><span data-stu-id="68f57-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="68f57-136">この例では、注文明細行が部分的に出荷されています。</span><span class="sxs-lookup"><span data-stu-id="68f57-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="68f57-137">そのため、注文の状態は [Open] のままです。</span><span class="sxs-lookup"><span data-stu-id="68f57-137">This is why the the order status remains Open.</span></span>     
    * <span data-ttu-id="68f57-138">ドキュメントのステータス フィールドは、注文明細行の少なくとも 1 つが出荷されたので、[梱包明細] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="68f57-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="68f57-139">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="68f57-140">[明細行の数量] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-140">Click Line quantity.</span></span>
19. <span data-ttu-id="68f57-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="68f57-141">Close the page.</span></span>
20. <span data-ttu-id="68f57-142">アクション ウィンドウで、[ピッキングと梱包] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="68f57-143">[梱包明細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68f57-143">Click Packing slip.</span></span>
    * <span data-ttu-id="68f57-144">[梱包明細仕訳帳] ページには、注文に対して生成されたすべての梱包明細ドキュメントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="68f57-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="68f57-145">各ドキュメントの詳細を確認および印刷することもできます。</span><span class="sxs-lookup"><span data-stu-id="68f57-145">You can review details of each document and print them, if you wish.</span></span>  


