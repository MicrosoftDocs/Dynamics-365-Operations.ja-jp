---
title: 製品推奨事項の概要
description: このトピックは、製品推奨事項に関する一般情報を提供します。 製品推奨事項により、顧客は必要な製品や元々購入する予定ではなかった製品も簡単かつ迅速に見つけることができます。
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770050"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="5cda6-104">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="5cda6-104">Product recommendations overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5cda6-105">Microsoft Dynamics 365 Commerce を使用して、E コマース Web サイトおよび販売時点管理 (POS) デバイスで製品推奨事項を表示できます。</span><span class="sxs-lookup"><span data-stu-id="5cda6-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="5cda6-106">製品推奨事項とは、顧客が興味を持っている可能性がある品目です。</span><span class="sxs-lookup"><span data-stu-id="5cda6-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="5cda6-107">推奨事項は、オンライン ストアおよび従来型店舗における他の顧客の購入傾向に基づいています。</span><span class="sxs-lookup"><span data-stu-id="5cda6-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="5cda6-108">製品の推奨事項により、顧客は自分に役立つ製品を簡単かつ迅速に見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="5cda6-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="5cda6-109">クロスセルおよびアップセルは、顧客が元々購入する予定ではなかった製品を見つけるためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="5cda6-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="5cda6-110">製品の検出のために推奨事項を使用した場合、より多くの変換の機会を作り出して販売収益を増やし、また顧客満足度と定着の強化することもできます。</span><span class="sxs-lookup"><span data-stu-id="5cda6-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="5cda6-111">コマースにおいて、製品推奨事項は、Microsoft の推奨機械学習マシンの学習技術により大規模に強化されています。</span><span class="sxs-lookup"><span data-stu-id="5cda6-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="5cda6-112">シナリオ</span><span class="sxs-lookup"><span data-stu-id="5cda6-112">Scenarios</span></span>

<span data-ttu-id="5cda6-113">製品推奨事項は、次のシナリオで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="5cda6-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="5cda6-114">**E コマースの参照またはランディング ページの店舗ページにおいて:** 顧客または店舗スタッフが店舗ページにアクセスする場合、推奨エンジンは、**新規**、**ベストセラー**、および**トレンド** リストの製品を提案することができます。</span><span class="sxs-lookup"><span data-stu-id="5cda6-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="5cda6-115">**製品の詳細ページにおいて:** 顧客または店舗スタッフが**製品の詳細**ページにアクセスした場合、推奨エンジンは購入される可能性がある追加の品目を提案します。</span><span class="sxs-lookup"><span data-stu-id="5cda6-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="5cda6-116">これらの品目は、**人気製品**リストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5cda6-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="5cda6-117">**トランザクション ページまたはチェックアウト ページにおいて:** 推奨エンジンは、買い物カゴ内の品目のリスト全体に基づいて提案します。</span><span class="sxs-lookup"><span data-stu-id="5cda6-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="5cda6-118">これらの項目は、**よく一緒に購入される製品**リストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5cda6-118">These items appear in the **Frequently bought together** list.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="5cda6-119">推奨サービス</span><span class="sxs-lookup"><span data-stu-id="5cda6-119">Recommendation service</span></span>

<span data-ttu-id="5cda6-120">製品推奨事項は、次のように推奨機械学習マシンの学習技術を使用します。</span><span class="sxs-lookup"><span data-stu-id="5cda6-120">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="5cda6-121">推奨サービスが必要とする形式のデータは、コマース運用データベースから抽出され、エンティティ ストアに送信されます。</span><span class="sxs-lookup"><span data-stu-id="5cda6-121">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="5cda6-122">推奨サービスはデータを使用して、**人気製品**、**よく一緒に購入される製品**、**新規**、**ベストセラー**、および**トレンド** リストに対する推奨モデルをトレーニングします。</span><span class="sxs-lookup"><span data-stu-id="5cda6-122">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5cda6-123">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5cda6-123">Additional resources</span></span>

[<span data-ttu-id="5cda6-124">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="5cda6-124">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="5cda6-125">Curated 製品推奨事項リストの作成</span><span class="sxs-lookup"><span data-stu-id="5cda6-125">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="5cda6-126">AI-ML ベースの製品推奨事項結果の管理</span><span class="sxs-lookup"><span data-stu-id="5cda6-126">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="5cda6-127">ページへの製品推奨リストの追加</span><span class="sxs-lookup"><span data-stu-id="5cda6-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
