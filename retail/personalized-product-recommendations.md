---
title: "カスタマイズされた製品の推奨事項の概要"
description: "Dynamics 365 for Retail では、POS (営業拠点) デバイスに製品の推奨事項を表示することができます。 推奨事項は、顧客の購買履歴、欲しい物のリストの品目、他の顧客がオンラインや従来型の店舗で購入した品目に基づいた興味を持ちそうな品目のことです。 大規模カタログの小売業者には、製品の発見に役立つ推奨事項があります。 製品の推奨事項は、顧客の関心と購買習慣を対象とした製品を展示することで、アップセルおよびクロスセルを行う小売業者を支援し、顧客維持を強化することができます。 Dynamics 365 for Retail では、認知サービスと Microsoft Azure 機械学習によって、小売りと製品の推奨が強化されます。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: a3a3b5e87a797c29c13b180c248d1782805c4c31
ms.contentlocale: ja-jp
ms.lasthandoff: 06/29/2017


---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="e928a-107">カスタマイズされた製品の推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="e928a-107">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="e928a-108">Dynamics 365 for Retail では、POS (営業拠点) デバイスに製品の推奨事項を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="e928a-108">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="e928a-109">推奨事項は、顧客の購買履歴、欲しい物のリストの品目、他の顧客がオンラインや従来型の店舗で購入した品目に基づいた興味を持ちそうな品目のことです。</span><span class="sxs-lookup"><span data-stu-id="e928a-109">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="e928a-110">大規模カタログの小売業者には、製品の発見に役立つ推奨事項があります。</span><span class="sxs-lookup"><span data-stu-id="e928a-110">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="e928a-111">製品の推奨事項は、顧客の関心と購買習慣を対象とした製品を展示することで、アップセルおよびクロスセルを行う小売業者を支援し、顧客維持を強化することができます。</span><span class="sxs-lookup"><span data-stu-id="e928a-111">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="e928a-112">Dynamics 365 for Retail では、認知サービスと Microsoft Azure 機械学習によって、小売りと製品の推奨が強化されます。</span><span class="sxs-lookup"><span data-stu-id="e928a-112">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>

<a name="scenarios"></a><span data-ttu-id="e928a-113">シナリオ</span><span class="sxs-lookup"><span data-stu-id="e928a-113">Scenarios</span></span>
---------

<span data-ttu-id="e928a-114">製品推奨事項は、以下の POS シナリオで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="e928a-114">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="e928a-115">これらは、Cloud POS または Modern POS (MPOS) で利用できます。</span><span class="sxs-lookup"><span data-stu-id="e928a-115">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="e928a-116">[**製品の詳細**] ページ:</span><span class="sxs-lookup"><span data-stu-id="e928a-116">On the **Product details** page:</span></span>

-   <span data-ttu-id="e928a-117">店舗スタッフが、異なるチャネル間で以前のトランザクションを調べるときに、[**製品の詳細**] ページを参照する場合、推薦エンジンは、一緒に購入される可能性が高い追加アイテムを提案します。</span><span class="sxs-lookup"><span data-stu-id="e928a-117">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="e928a-118">店舗スタッフが顧客をトランザクションに追加し、[**製品の詳細**] を参照する場合、推奨エンジンは、顧客の取引履歴を使用してパーソナライズされた推奨事項を提供します。</span><span class="sxs-lookup"><span data-stu-id="e928a-118">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="e928a-119">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="e928a-119">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="e928a-120">[**トランザクション**] ページ:</span><span class="sxs-lookup"><span data-stu-id="e928a-120">On the **Transaction** page:</span></span>

-   <span data-ttu-id="e928a-121">推薦エンジンは、バスケット内のアイテムの全リストに基づいて品目を提案します。</span><span class="sxs-lookup"><span data-stu-id="e928a-121">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="e928a-122">店舗スタッフが顧客をトランザクションに追加する場合、推奨エンジンは、顧客のトランザクション履歴とバスケット内の品目のリストを使用して個人的な推奨を提供します。</span><span class="sxs-lookup"><span data-stu-id="e928a-122">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

<span data-ttu-id="e928a-123">[**注記**] [**トランザクション**] ページに推奨事項を表示するには、小売業者は Dynamics 365 for Retail の画面レイアウトを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e928a-123">**Note**  To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="e928a-124">[**推奨事項**] コントロールは、[**トランザクション**] ページにドロップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e928a-124">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="e928a-125">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="e928a-125">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="e928a-126">[**顧客の詳細**] ページ:</span><span class="sxs-lookup"><span data-stu-id="e928a-126">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="e928a-127">推薦エンジンは、ユーザ ID および顧客の希望リストの品目に基づいて、品目を提案します。</span><span class="sxs-lookup"><span data-stu-id="e928a-127">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="e928a-128">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="e928a-128">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="e928a-129">Dynamics 365 for Retail を構成して POS 推奨事項を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e928a-129">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="e928a-130">製品の推奨事項を設定するには、次の設定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e928a-130">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="e928a-131">正しい [**法人**] を選択したことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e928a-131">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="e928a-132">[**エンティティ ストア**] にナビゲートし、[**小売販売**] を選択して、[**更新**] をクリックします。これにより、運用データベースのデモ データ (またはデータ) が使用され、エンティティ ストアに転送します。</span><span class="sxs-lookup"><span data-stu-id="e928a-132">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.** **This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="e928a-133">オプション: トランザクション画面に推奨事項を表示するには、**画面レイアウト、**画面レイアウトを選択し、**画面レイアウト デザイナー**** ** を起動し、必要に応じて **レコメンデーション コントロール** を削除します。</span><span class="sxs-lookup"><span data-stu-id="e928a-133">Optional: To display recommendations on the transaction screen, go to **Screen Layout, **choose your screen layout, launch the **Screen layout designer**,** **and then drop the **recommendations control **where needed.</span></span>
4.  <span data-ttu-id="e928a-134">[**小売パラメーター**] に移動し、[**機械学習**] を選択し、[**POS 推奨事項の有効化**] で [**はい**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e928a-134">Go to **Retail parameters**, select **Machine-learning**, select **Yes **under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="e928a-135">POS に関する推奨事項を表示するには、グローバル構成ジョブ [**1110**] を実行します。</span><span class="sxs-lookup"><span data-stu-id="e928a-135">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="e928a-136">POS 画面レイアウト設計者の変更を反映するには、チャネル構成ジョブ [**1070**] を実行します。</span><span class="sxs-lookup"><span data-stu-id="e928a-136">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="e928a-137">[]() どのような仕組みですか?</span><span class="sxs-lookup"><span data-stu-id="e928a-137">[]()How does it work?</span></span>
<span data-ttu-id="e928a-138">[**エンティティ ストア**] エンティティを更新すると、次のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="e928a-138">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="e928a-139">認識サービスによって必要とされる形式のデータは、Dynamics 365 for Retail 運用データベースから抽出され、エンティティ ストアに送信されます。</span><span class="sxs-lookup"><span data-stu-id="e928a-139">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="e928a-140">このデータは、Azure Data Factory (ADF) によって ADF アクティビティの一部として Hive スクリプトを使用してデータをクレンジングするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e928a-140">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="e928a-141">クレンジングされたデータは、BLOB ストレージに保存されます。</span><span class="sxs-lookup"><span data-stu-id="e928a-141">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="e928a-142">BLOB ストレージからのデータは、Cognitive サービス API によって推奨モデルをトレーニングするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e928a-142">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="e928a-143">[**推奨事項の有効化**] をオンにして構成ジョブを実行すると、次の操作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="e928a-143">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="e928a-144">モデル資格情報と ID は API から取得され、Dynamics 365 for Retail 運用データベース、AOS 用 web.config、および小売サーバーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="e928a-144">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="e928a-145">モデルの資格情報と ID は CRT で利用できるようになっており、オンライン モードで Cloud POS と MPOS からの製品推奨事項を守ることができます。</span><span class="sxs-lookup"><span data-stu-id="e928a-145">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="e928a-146">参照</span><span class="sxs-lookup"><span data-stu-id="e928a-146">See also</span></span>
--------

[<span data-ttu-id="e928a-147">POS デバイスのトランザクション ページへのレコメンデーション コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="e928a-147">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




