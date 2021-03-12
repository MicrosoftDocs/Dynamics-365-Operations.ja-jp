---
title: 製品推奨事項の概要
description: このトピックは、製品推奨事項に関する一般情報を提供します。 製品推奨事項により、顧客は必要な製品や元々購入する予定ではなかった製品も簡単かつ迅速に見つけることができます。
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1769af6663a040c699449eb53841b3f72ab433e5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972371"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="30364-104">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="30364-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="30364-105">Microsoft Dynamics 365 Commerce を使用して、E コマース Web サイトおよび販売時点管理 (POS) デバイスで製品推奨事項を表示できます。</span><span class="sxs-lookup"><span data-stu-id="30364-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="30364-106">製品推奨事項とは、顧客が興味を持っている可能性がある品目です。</span><span class="sxs-lookup"><span data-stu-id="30364-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="30364-107">推奨事項は、オンライン ストアおよび従来型店舗における他の顧客の購入傾向に基づいています。</span><span class="sxs-lookup"><span data-stu-id="30364-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="30364-108">製品の推奨事項により、顧客は自分に役立つ製品を簡単かつ迅速に見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="30364-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="30364-109">クロスセルおよびアップセルは、顧客が元々購入する予定ではなかった製品を見つけるためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="30364-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="30364-110">製品の検出を強化するために推奨事項を使用した場合、より多くの変換の機会を作り出して販売収益を増やし、また顧客満足度と定着を増幅させることもできます。</span><span class="sxs-lookup"><span data-stu-id="30364-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="30364-111">E コマースにおいて、製品推奨事項は、Microsoft の推奨機械学習マシンの学習技術により大規模に強化されています。</span><span class="sxs-lookup"><span data-stu-id="30364-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="30364-112">推奨サービス</span><span class="sxs-lookup"><span data-stu-id="30364-112">Recommendation service</span></span>

<span data-ttu-id="30364-113">製品推奨事項サービスは、次の方法で人為的知能と機械学習 (AI-ML) テクノロジを利用します。</span><span class="sxs-lookup"><span data-stu-id="30364-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="30364-114">推奨サービスが必要とする形式のデータは、コマース運用データベースから抽出され、Azure Data Lake Storage かエンティティ ストアに送信されます。</span><span class="sxs-lookup"><span data-stu-id="30364-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="30364-115">推奨サービスは保存済データを使用して、**人気製品**、**よく一緒に購入される製品**、**新規**、**ベストセラー**、および **トレンド** リストに対する推奨モデルをトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="30364-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="30364-116">シナリオ</span><span class="sxs-lookup"><span data-stu-id="30364-116">Scenarios</span></span>

<span data-ttu-id="30364-117">製品推奨事項は、次のシナリオで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="30364-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="30364-118">**E コマースの参照またはランディング ページの店舗ページにおいて:** 顧客または店舗スタッフが店舗ページにアクセスする場合、推奨エンジンは、**新規**、**ベストセラー**、および **トレンド** リストの製品を提案することができます。</span><span class="sxs-lookup"><span data-stu-id="30364-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="30364-119">**製品の詳細ページにおいて:** 顧客または店舗スタッフが **製品の詳細** ページにアクセスした場合、推奨エンジンは購入される可能性がある追加の品目を提案します。</span><span class="sxs-lookup"><span data-stu-id="30364-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="30364-120">これらの品目は、**人気製品** リストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="30364-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="30364-121">**トランザクション ページまたはチェックアウト ページにおいて:** 推奨エンジンは、買い物カゴ内の品目のリスト全体に基づいて提案します。</span><span class="sxs-lookup"><span data-stu-id="30364-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="30364-122">これらの項目は、**よく一緒に購入される製品** リストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="30364-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="30364-123">**パーソナライズされた推奨事項:** マーチャンダイザーは、既存のリストシナリオをその顧客に基づいてパーソナライズできる新しい機能に加えて、サインインしたユーザーにパーソナライズされた **おすすめ** リストを提供できます。</span><span class="sxs-lookup"><span data-stu-id="30364-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="30364-124">詳細については、[カスタマイズされた推奨事項を有効にする。](personalized-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30364-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="30364-125">製品推奨事項のタイプ</span><span class="sxs-lookup"><span data-stu-id="30364-125">Types of product recommendations</span></span>

<span data-ttu-id="30364-126">次の表では、小売業者が [製品収集モジュール](product-collection-module-overview.md) を介して Dynamics 365 Commerce ソリューションで実装可能なさまざまなタイプの自動化製品推奨事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="30364-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="30364-127">サイトの作成者がこのオプションを選択している場合、小売業者はサインインしたユーザーに対してパーソナライズされた結果を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="30364-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="30364-128">製品収集モジュール</span><span class="sxs-lookup"><span data-stu-id="30364-128">Product collection module</span></span>  | <span data-ttu-id="30364-129">種類</span><span class="sxs-lookup"><span data-stu-id="30364-129">Type</span></span> | <span data-ttu-id="30364-130">説明</span><span class="sxs-lookup"><span data-stu-id="30364-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="30364-131">新規</span><span class="sxs-lookup"><span data-stu-id="30364-131">New</span></span>                        | <span data-ttu-id="30364-132">アルゴリズム</span><span class="sxs-lookup"><span data-stu-id="30364-132">Algorithmic</span></span> | <span data-ttu-id="30364-133">このモジュールは、チャネルおよびカタログに対して最近類別された最新の製品のリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="30364-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="30364-134">ベストセラー</span><span class="sxs-lookup"><span data-stu-id="30364-134">Best selling</span></span>               | <span data-ttu-id="30364-135">アルゴリズム</span><span class="sxs-lookup"><span data-stu-id="30364-135">Algorithmic</span></span> | <span data-ttu-id="30364-136">このモジュールは、最大販売注文数でランク付けされている製品のリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="30364-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="30364-137">トレンド</span><span class="sxs-lookup"><span data-stu-id="30364-137">Trending</span></span>                   | <span data-ttu-id="30364-138">アルゴリズム</span><span class="sxs-lookup"><span data-stu-id="30364-138">Algorithmic</span></span> | <span data-ttu-id="30364-139">このモジュールは、指定期間において業績が最上位で、最大販売注文数でランク付けされている製品のリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="30364-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="30364-140">よく一緒に購入される品目</span><span class="sxs-lookup"><span data-stu-id="30364-140">Frequently bought together</span></span> | <span data-ttu-id="30364-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="30364-141">AI-ML</span></span> | <span data-ttu-id="30364-142">このモジュールは、最も消費者の現在の買い物カゴのコンテンツと共に購入される製品の一覧を推奨します。</span><span class="sxs-lookup"><span data-stu-id="30364-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="30364-143">その他のお勧め</span><span class="sxs-lookup"><span data-stu-id="30364-143">People also like</span></span>           | <span data-ttu-id="30364-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="30364-144">AI-ML</span></span> | <span data-ttu-id="30364-145">このモジュールは、消費者の購入パターンに基づき、指定されたシード製品に対する製品を推奨します。</span><span class="sxs-lookup"><span data-stu-id="30364-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="30364-146">おすすめ</span><span class="sxs-lookup"><span data-stu-id="30364-146">Picks for you</span></span>              | <span data-ttu-id="30364-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="30364-147">AI-ML</span></span> | <span data-ttu-id="30364-148">このモジュールは、サインインしたユーザーの購入パターンに基づいてパーソナライズされた製品の一覧を推奨します。</span><span class="sxs-lookup"><span data-stu-id="30364-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="30364-149">ゲスト ユーザーの場合、このリストは折りたたまれています。</span><span class="sxs-lookup"><span data-stu-id="30364-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="30364-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="30364-150">Additional resources</span></span>

[<span data-ttu-id="30364-151">Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する</span><span class="sxs-lookup"><span data-stu-id="30364-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="30364-152">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="30364-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="30364-153">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="30364-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="30364-154">カスタマイズされた推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="30364-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="30364-155">"類似したルックを買う" 推奨を有効にする</span><span class="sxs-lookup"><span data-stu-id="30364-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="30364-156">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="30364-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="30364-157">トランザクション画面への推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="30364-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="30364-158">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="30364-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="30364-159">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="30364-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="30364-160">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="30364-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="30364-161">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="30364-161">Product recommendations FAQ</span></span>](faq-recommendations.md)
