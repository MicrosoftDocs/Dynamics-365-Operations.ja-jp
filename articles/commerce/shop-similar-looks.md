---
title: "\"類似したルックを買う\" 推奨を有効にする"
description: このトピックでは、Microsoft Dynamics 365 Commerce での "類似したスタイルを探す" 推奨製品を有効にする方法について説明します。
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2e57965a1073982a7b6c34b79dbf6e5b90d7ee30
ms.sourcegitcommit: 15c68822f4d412bfc609be31b3702f18c81ea0bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2020
ms.locfileid: "3666311"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="4a86e-103">"類似したルックを買う" 推奨を有効にする</span><span class="sxs-lookup"><span data-stu-id="4a86e-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4a86e-104">このトピックでは、Microsoft Dynamics 365 Commerce での "類似したスタイルを探す" 推奨製品を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4a86e-105">概要</span><span class="sxs-lookup"><span data-stu-id="4a86e-105">Overview</span></span>

<span data-ttu-id="4a86e-106">Dynamics 365 Commerce の "類似したスタイルを探す" 推奨機能は、人工知能と機械学習 (AI-ML) の機能を使用して、顧客に対して視覚的に類似した製品の推奨を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="4a86e-107">Commerce におけるすべての小売チャンネルについて、"類似したスタイルを探す" 推奨を提供することによって、小売業者は顧客が欲しいものを簡単に見つけられるようにすることで、顧客満足度を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="4a86e-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="4a86e-108">"類似したスタイルを探す" 推奨の機能は、シード製品バリアントの製品画像を使用して、小売業者の製品カタログで視覚的に類似した製品を見つけて推奨します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="4a86e-109">"同様のスタイルを探す" 推奨事項は、販売時点管理 (POS) と電子商取引の両方の経験で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="4a86e-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="4a86e-110">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="4a86e-110">Example scenarios</span></span>

- <span data-ttu-id="4a86e-111">顧客はブラック ストライプのセーターを閲覧し、類似した赤色のセーターの推奨を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="4a86e-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="4a86e-112">顧客は、最初に表示された製品の代わりに推奨された製品を選択し、類似した赤色の製品の推奨を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="4a86e-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="4a86e-113">"類似のスタイルを探す" 推奨事項を使用する顧客は、顧客が購入しようと思っている指輪とおそろいのイヤリングを見つけます。</span><span class="sxs-lookup"><span data-stu-id="4a86e-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="4a86e-114">Commerce 本社の "類似したスタイルを探す" 推奨を有効にする</span><span class="sxs-lookup"><span data-stu-id="4a86e-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="4a86e-115">製品の推奨は、ストレージを Azure Data Lake Gen2 に移行した Commerce 顧客に対してのみサポートしています。</span><span class="sxs-lookup"><span data-stu-id="4a86e-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4a86e-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="4a86e-116">Prerequisites</span></span>

<span data-ttu-id="4a86e-117">小売業者が顧客に対して "類似したスタイルを探す" 推奨を表示するには、次の 2 つの手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a86e-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="4a86e-118">Commerce 本社での [製品推奨を有効にします](enable-product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="4a86e-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="4a86e-119">メディア サーバーが HTTPS 呼び出しをサポートしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="4a86e-120">製品画像にアクセスするための推奨エンジンでは、小売業者は製品の URL を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a86e-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="4a86e-121">Commerce 本社で製品 URL を生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4a86e-122">**製品画像** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="4a86e-123">アクション ウィンドウで、**メディア テンプレートの定義** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="4a86e-124">**メディア テンプレートの定義** プロパティ ウィンドウで、**メディア URL** から **URL の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="4a86e-125">"類似のスタイルを探す" 推奨機能を有効にすると、製品推奨リストの生成プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="4a86e-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="4a86e-126">これらのリストを利用可能にし、オンラインおよび POS で表示するまでに、少なくとも 1 日必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="4a86e-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="4a86e-127">Commerce本社で"同様のスタイルを探す" 推奨機能を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4a86e-128">**機能管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="4a86e-129">使用可能な機能の一覧で、**同様のスタイルを探す** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="4a86e-130">右ウィンドウで、**有効化** を選択してサービスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="4a86e-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="4a86e-131">次の図は、Commerce本社の **機能管理** ページの **類似したスタイルを探す** 機能を示しています。</span><span class="sxs-lookup"><span data-stu-id="4a86e-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![次の図は、Commerce 本社の [機能管理] ページの [類似したスタイルを探す] 機能を示しています。](./media/enableshopsimilarlooks.png)

<span data-ttu-id="4a86e-133">上記のタスクが完了すると、POS ターミナルは、**類似した製品を探す** パネルで自動的に拡張されます。</span><span class="sxs-lookup"><span data-stu-id="4a86e-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="4a86e-134">**詳細を表示** を選択すると、POS 端末のユーザーは、さらに絞り込むことができる、専用の "類似したスタイルを探す" ページに移動できます。</span><span class="sxs-lookup"><span data-stu-id="4a86e-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="4a86e-135">"類似のスタイルを探す" 推奨機能をオフにすると、他の製品の推奨は影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="4a86e-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="4a86e-136">製品推奨の詳細については、[製品推奨の概要](product-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a86e-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="4a86e-137">Commerce サイト ビルダーを使用することで、製品の詳細ページに [類似したスタイルを探す] ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="4a86e-138">Commerce 本社の [同様のスタイルを探す] 推奨機能を有効にすると、Commerce サイトのオプションによって、小売業者は **類似したスタイルを探す** ボタンを追加して、製品詳細ページ (PDP) 上の購入ボックスに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="4a86e-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="4a86e-139">このボタンを選択した顧客は、視覚的に類似した製品を返す、専用の "類似したスタイルを探す" ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="4a86e-140">そこで、顧客はセレクターを使用して、製品をさらに詳細にフィルタ処理することができます。</span><span class="sxs-lookup"><span data-stu-id="4a86e-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="4a86e-141">Commerce サイト ビルダーを使用することで、**類似したスタイルを探す** ボタンを PDP に追加するには。</span><span class="sxs-lookup"><span data-stu-id="4a86e-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4a86e-142">購入ボックス モジュールを含む既存のサイト ビルダー ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="4a86e-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="4a86e-143">左のナビゲーション ウィンドウで、購入ボックスモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="4a86e-144">右側のナビゲーション ウィンドウで、**類似したスタイルを探すリンクを有効にする** チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4a86e-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="4a86e-145">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="4a86e-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="4a86e-146">ページの発行後に、PDP には **同様のスタイルを探す** ボタンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="4a86e-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="4a86e-147">次の図は、サイト ビルダーの PDP 例上の **類似したスタイルを探すリンクを有効にする** チェック ボックスと **類似したスタイルを探す** ボタンを示しています。</span><span class="sxs-lookup"><span data-stu-id="4a86e-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![サイト ビルダーの PDP 上で、[類似したスタイルを探すリンク] チェック ボックスと [類似したスタイルを探す] ボタンを有効化します。](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="4a86e-149">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4a86e-149">Additional resources</span></span>

[<span data-ttu-id="4a86e-150">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="4a86e-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4a86e-151">Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する</span><span class="sxs-lookup"><span data-stu-id="4a86e-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="4a86e-152">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="4a86e-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="4a86e-153">カスタマイズされた推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="4a86e-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="4a86e-154">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="4a86e-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="4a86e-155">トランザクション画面への推奨設定の追加</span><span class="sxs-lookup"><span data-stu-id="4a86e-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="4a86e-156">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="4a86e-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="4a86e-157">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="4a86e-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="4a86e-158">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="4a86e-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="4a86e-159">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="4a86e-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
