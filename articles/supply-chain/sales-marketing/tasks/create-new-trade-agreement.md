---
title: 新しい売買契約の作成
description: この手順は、特定の顧客と合意した新しい製品販売価格を登録する売買契約の作成方法を示します。
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9aa46f959c35c209791457aa697ab829264b3275
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211954"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="68ce1-103">新しい売買契約の作成</span><span class="sxs-lookup"><span data-stu-id="68ce1-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="68ce1-104">この手順は、特定の顧客と合意した新しい製品販売価格を登録する売買契約の作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="68ce1-105">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="68ce1-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="68ce1-106">独自のデータを使用する場合は、このガイドの開始する前に、"価格 (販売)" に既定の取引関係が設定されている売買契約仕訳帳名が存在することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68ce1-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="68ce1-107">新しい売買契約仕訳帳の作成と転記</span><span class="sxs-lookup"><span data-stu-id="68ce1-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="68ce1-108">**ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > 価格と割引 > 売買契約仕訳帳**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="68ce1-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68ce1-109">Click **New**.</span></span>
3. <span data-ttu-id="68ce1-110">**名前**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="68ce1-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="68ce1-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="68ce1-112">**アクション ウィンドウ**で、**明細行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68ce1-112">On **Action pane**, click **Lines**.</span></span>
6. <span data-ttu-id="68ce1-113">**アカウント コード** フィールドで、「テーブル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="68ce1-114">この例では、特定の顧客の価格を更新しており、これはテーブルの選択が必要であることを意味しています。</span><span class="sxs-lookup"><span data-stu-id="68ce1-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="68ce1-115">製品の表示価格を更新する場合は、新しい価格がすべての顧客に対して有効になるように、「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="68ce1-116">異なる顧客の区分間の価格を区別する場合は、[グループ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="68ce1-117">[グループ] を選択するには、[顧客の価格グループ] を設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="68ce1-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="68ce1-118">**勘定の選択**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="68ce1-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="68ce1-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="68ce1-120">**品目コード** フィールドで、「テーブル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="68ce1-121">「価格 (販売)」タイプの売買契約を入力する場合は、**品目コード** フィールドで「テーブル」のみを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68ce1-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="68ce1-122">これは、価格が絶対値であり、すべての製品または製品のグループで同じにすることができないためです。</span><span class="sxs-lookup"><span data-stu-id="68ce1-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="68ce1-123">**品目関係**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="68ce1-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="68ce1-124">リストで、契約に含める製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="68ce1-125">選択した製品をメモします。</span><span class="sxs-lookup"><span data-stu-id="68ce1-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="68ce1-126">**ソース** フィールドに、最小数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="68ce1-127">新しい価格を利用する前に、顧客が最小数量を注文する必要がある場合、ここでその数量を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68ce1-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="68ce1-128">契約の価格が有効にならない最大数量を指定するには、**ターゲット** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="68ce1-129">複数の数量区分に基づいて価格と割引を提供する場合、**ソース**と**ターゲット** フィールドそれぞれに最小数量と最大数量のペアとして各数量の区分を指定します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="68ce1-130">**通貨金額フィールド**に価格を入力します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="68ce1-131">**詳細**セクションの**開始日**フィールドに、この契約が有効になる日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="68ce1-132">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68ce1-132">Click **Save**.</span></span>
16. <span data-ttu-id="68ce1-133">**検証**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68ce1-133">Click **Validate**.</span></span>
17. <span data-ttu-id="68ce1-134">**選択した明細行の検証**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68ce1-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="68ce1-135">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68ce1-135">Click **OK**.</span></span>
19. <span data-ttu-id="68ce1-136">**転記** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68ce1-136">Click **Post**.</span></span>
20. <span data-ttu-id="68ce1-137">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68ce1-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="68ce1-138">製品に関連する売買契約の表示</span><span class="sxs-lookup"><span data-stu-id="68ce1-138">View trade agreements for a product</span></span>
1. <span data-ttu-id="68ce1-139">**ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 製品 > リリース済製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="68ce1-140">リストで、更新した価格の製品を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="68ce1-141">**アクション ウィンドウ**で、**販売**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68ce1-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="68ce1-142">**売買契約の表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68ce1-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="68ce1-143">作成した価格の売買契約の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="68ce1-143">Review the details of the price trade agreement you have just created.</span></span>    

5. <span data-ttu-id="68ce1-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="68ce1-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68ce1-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="68ce1-145">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="68ce1-146">コミュニティのブログ</span><span class="sxs-lookup"><span data-stu-id="68ce1-146">Community blogs</span></span>
- [<span data-ttu-id="68ce1-147">Dynamics 365 for Finance and Operations での販売価格</span><span class="sxs-lookup"><span data-stu-id="68ce1-147">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
