--- 
title: "新しい売買契約の作成"
description: "この手順は、特定の顧客と合意した新しい製品販売価格を登録する売買契約の作成方法を示します。"
author: omulvad
manager: AnnBe
ms.date: 11/16/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f7df0a91948a494465fbd55af99757e3890357ce
ms.openlocfilehash: e132cd20437b7929e81fcaa123d70bb57fb320c8
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="cc0ce-103">新しい売買契約の作成</span><span class="sxs-lookup"><span data-stu-id="cc0ce-103">Create a new trade agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc0ce-104">この手順は、特定の顧客と合意した新しい製品販売価格を登録する売買契約の作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="cc0ce-105">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="cc0ce-106">独自のデータを使用する場合は、このガイドの開始する前に、「価格 (販売)」に既定の取引関係が設定されている売買契約仕訳帳名が存在することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="cc0ce-107">新しい売買契約仕訳帳の作成と転記</span><span class="sxs-lookup"><span data-stu-id="cc0ce-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="cc0ce-108">[販売とマーケティング] > [価格と割引] > [売買契約仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="cc0ce-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-109">Click New.</span></span>
3. <span data-ttu-id="cc0ce-110">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cc0ce-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cc0ce-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cc0ce-113">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-113">Click Lines.</span></span>
7. <span data-ttu-id="cc0ce-114">[アカウント コード] フィールドで、[テーブル] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="cc0ce-115">この例では、特定の顧客の価格を更新しており、これはテーブルの選択が必要であることを意味しています。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="cc0ce-116">製品の表示価格を更新する場合は、すべての顧客に対して有効な新しい価格をすべて選択します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="cc0ce-117">異なる顧客の区分間の価格を区別する場合は、[グループ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="cc0ce-118">[グループ] を選択するには、[顧客の価格グループ] を設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="cc0ce-119">[勘定の選択] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="cc0ce-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="cc0ce-121">[品目コード] フィールドで、[テーブル] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="cc0ce-122">「価格 (販売)」タイプの売買契約を入力する場合は、[品目コード] フィールドで [テーブル] のみを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="cc0ce-123">これは、価格が絶対値であり、すべての製品または製品のグループで同じにすることができないためです。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="cc0ce-124">[品目関係] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="cc0ce-125">リストで、契約に含める製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="cc0ce-126">選択した製品をメモします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="cc0ce-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="cc0ce-128">[ソース] フィールドに、最小数量入力します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="cc0ce-129">新しい価格を利用する前に、顧客が最小数量を注文する必要がある場合、ここでその数量を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="cc0ce-130">契約の価格が有効ではない最大数量を指定するには、[ターゲット フィールド] に値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="cc0ce-131">複数の数量の区分に基づいて価格と割引を提供する場合、[ソース] と [ターゲット] フィールドそれぞれに最小数量と最大数量のペアとして各数量の区分を指定します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="cc0ce-132">[通貨金額] フィールドに価格を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="cc0ce-133">[開始日] フィールドに、この契約が有効になる日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="cc0ce-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-134">Click Save.</span></span>
18. <span data-ttu-id="cc0ce-135">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-135">Click Validate.</span></span>
19. <span data-ttu-id="cc0ce-136">[選択した明細行の検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="cc0ce-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-137">Click OK.</span></span>
21. <span data-ttu-id="cc0ce-138">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-138">Click Post.</span></span>
22. <span data-ttu-id="cc0ce-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="cc0ce-140">製品に関連する売買契約の表示</span><span class="sxs-lookup"><span data-stu-id="cc0ce-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="cc0ce-141">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="cc0ce-142">リストで、更新した価格の製品を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="cc0ce-143">[アクション] ペインで [販売] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="cc0ce-144">[売買契約の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="cc0ce-145">作成した価格の売買契約の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="cc0ce-146">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cc0ce-146">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc0ce-147">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="cc0ce-147">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="cc0ce-148">コミュニティのブログ</span><span class="sxs-lookup"><span data-stu-id="cc0ce-148">Community blogs</span></span>
- [<span data-ttu-id="cc0ce-149">Dynamics 365 for Finance and Operations での販売価格</span><span class="sxs-lookup"><span data-stu-id="cc0ce-149">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)

