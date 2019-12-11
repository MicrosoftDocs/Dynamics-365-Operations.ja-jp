---
title: 製品詳細ページの概要
description: このトピックでは、Microsoft Dynamics 365 Commerce の製品詳細ページ (PDP) の概要を示します。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697868"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="681ab-103">製品詳細ページの概要</span><span class="sxs-lookup"><span data-stu-id="681ab-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="681ab-104">このトピックでは、Microsoft Dynamics 365 Commerce の製品詳細ページ (PDP) の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="681ab-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="681ab-105">概要</span><span class="sxs-lookup"><span data-stu-id="681ab-105">Overview</span></span>

<span data-ttu-id="681ab-106">PDP は、製品に関する詳細情報を提供し、顧客がサイズ、スタイル、および色などの製品オプションを選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="681ab-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="681ab-107">PDP は顧客が購入決定をするために必要なすべての製品情報を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="681ab-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="681ab-108">次の図は、PDP の例を示します。</span><span class="sxs-lookup"><span data-stu-id="681ab-108">The following illustration shows an example of a PDP.</span></span>

![製品の詳細ページの例](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="681ab-110">ヘッダーとフッター モジュール</span><span class="sxs-lookup"><span data-stu-id="681ab-110">Header and footer modules</span></span>

<span data-ttu-id="681ab-111">PDP の上部には、小売業者が顧客に参照させたいすべての製品カテゴリおよび他のページを表示するヘッダーがあります。</span><span class="sxs-lookup"><span data-stu-id="681ab-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="681ab-112">ページの下部には、顧客が興味を持つさまざまなトピックへのクイック リンクを含むフッターがあります。</span><span class="sxs-lookup"><span data-stu-id="681ab-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="681ab-113">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="681ab-113">Buy box module</span></span>

<span data-ttu-id="681ab-114">PDP で最も重要なモジュールは、購入ボックス モジュールです。</span><span class="sxs-lookup"><span data-stu-id="681ab-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="681ab-115">したがって、これはページのメイン セクションの最初の項目です。</span><span class="sxs-lookup"><span data-stu-id="681ab-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="681ab-116">購入ボックス モジュールは、製品に関する最も重要な情報を含む複数のモジュールをホストするコンテナ モジュールです。</span><span class="sxs-lookup"><span data-stu-id="681ab-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="681ab-117">この情報には、製品名、製品の画像、説明、価格、および製品の評価が含まれます。</span><span class="sxs-lookup"><span data-stu-id="681ab-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="681ab-118">購入ボックス モジュールにより、顧客は製品オプション (たとえば、サイズ、スタイル、および色) を選択して、製品を買い物カゴに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="681ab-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="681ab-119">また、顧客が製品をオンラインで購入し、店舗で受取ることもできます。</span><span class="sxs-lookup"><span data-stu-id="681ab-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="681ab-120">オンライン購入店舗受取りのモジュールは、Bing Maps のアプリケーション プログラミング インターフェイス (API) との統合を使用して、最寄りの店舗、または顧客が指定した別の場所の店舗を検索します。</span><span class="sxs-lookup"><span data-stu-id="681ab-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="681ab-121">購入ボックス モジュールには製品 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="681ab-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="681ab-122">この ID は、ページ コンテキストから派生します。</span><span class="sxs-lookup"><span data-stu-id="681ab-122">This ID is derived from the page context.</span></span> <span data-ttu-id="681ab-123">購入ボックス モジュールがページ コンテキストに製品 ID が含まれていないページに追加される場合、情報は正しく表示されません。</span><span class="sxs-lookup"><span data-stu-id="681ab-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="681ab-124">製品仕様のモジュール</span><span class="sxs-lookup"><span data-stu-id="681ab-124">Product specifications module</span></span>

<span data-ttu-id="681ab-125">製品仕様モジュールは、製品に関する追加情報を表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="681ab-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="681ab-126">これらの詳細は、Dynamics 365 Retail の製品属性から取得されます。</span><span class="sxs-lookup"><span data-stu-id="681ab-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="681ab-127">製品仕様モジュールは、**表示**プロパティが**はい**に設定されているすべての属性を表示します。</span><span class="sxs-lookup"><span data-stu-id="681ab-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="681ab-128">製品属性を取得するには、製品 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="681ab-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="681ab-129">推奨モジュール</span><span class="sxs-lookup"><span data-stu-id="681ab-129">Recommendations module</span></span>

<span data-ttu-id="681ab-130">推奨モジュールは、PDP で重要なモジュールです。</span><span class="sxs-lookup"><span data-stu-id="681ab-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="681ab-131">顧客が製品を参照している間、正しい製品を見つけて購買することができるように、より多くの製品オプションを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="681ab-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="681ab-132">推奨事項により、顧客は関連するコンテンツを簡単に見つけて、ショッピングを継続することができます。</span><span class="sxs-lookup"><span data-stu-id="681ab-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="681ab-133">異なるタイプの推奨項目リストが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="681ab-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="681ab-134">**人気製品**リストは機械学習に基づいています。</span><span class="sxs-lookup"><span data-stu-id="681ab-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="681ab-135">他の顧客のトランザクション履歴を使用して、推奨事項を提供します。</span><span class="sxs-lookup"><span data-stu-id="681ab-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="681ab-136">このリストは推奨項目サービスによって生成され、「この製品を購入した顧客はこちらも購入しました」リストに似ています。</span><span class="sxs-lookup"><span data-stu-id="681ab-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="681ab-137">このリストを生成するには、製品 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="681ab-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="681ab-138">**関連**リストは、Retail の製品についてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="681ab-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="681ab-139">たとえば、茶色のレザーの旅行用ハンドバッグの場合、レザー製または旅行目的のためにデザインされた、さらに多くのハンドバッグを関連リストにコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="681ab-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="681ab-140">**アクセサリ**および**類似製品**などの、他のタイプの関連リストも Retail でコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="681ab-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="681ab-141">このリストを生成するには、製品 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="681ab-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="681ab-142">したがって、ページ コンテキストに製品 ID が含まれていないホーム ページに追加すると、リストは空になります。</span><span class="sxs-lookup"><span data-stu-id="681ab-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="681ab-143">**トレンド**、**ベスト セラー**、および**新規**など、アルゴリズムによって生成された推奨項目リストは PDP 上で使用できます。</span><span class="sxs-lookup"><span data-stu-id="681ab-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="681ab-144">これらのリストは、PDP 上の製品に直接関連していないことがありますが、顧客が興味を持つ可能性がある製品を検索するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="681ab-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="681ab-145">これらのタイプのリストには、製品 ID は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="681ab-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="681ab-146">これらは、サイト間でのショッピング パターンに基づいて生成される一般的なリストです。</span><span class="sxs-lookup"><span data-stu-id="681ab-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="681ab-147">編集リストは、手動で精選されたリストです。</span><span class="sxs-lookup"><span data-stu-id="681ab-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="681ab-148">たとえば、小売業者は、紹介する製品のリストを手動で精選することがあります。</span><span class="sxs-lookup"><span data-stu-id="681ab-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="681ab-149">評価とレビュー モジュール</span><span class="sxs-lookup"><span data-stu-id="681ab-149">Ratings and reviews module</span></span>

<span data-ttu-id="681ab-150">評価とレビュー モジュールは、他の顧客によって提供された評価とレビューを表示します。</span><span class="sxs-lookup"><span data-stu-id="681ab-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="681ab-151">また、顧客が製品のレビューを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="681ab-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="681ab-152">また、製品の評価の傾向を示すヒストグラムも含まれます。</span><span class="sxs-lookup"><span data-stu-id="681ab-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="681ab-153">詳細については、[評価とレビューの概要](ratings-reviews-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="681ab-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="681ab-154">マーケティング モジュール</span><span class="sxs-lookup"><span data-stu-id="681ab-154">Marketing modules</span></span>

<span data-ttu-id="681ab-155">マーケティング コンテンツが特定の製品固有のものである場合、すべてのマーケティング モジュールを PDP に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="681ab-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="681ab-156">ページを「拡充」することにより、マーケティング モジュールを PDP に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="681ab-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="681ab-157">追加リソース</span><span class="sxs-lookup"><span data-stu-id="681ab-157">Additional resources</span></span>

[<span data-ttu-id="681ab-158">ホーム ページの概要</span><span class="sxs-lookup"><span data-stu-id="681ab-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="681ab-159">既定のカテゴリ ランディング ページと検索結果ページの概要</span><span class="sxs-lookup"><span data-stu-id="681ab-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="681ab-160">買い物カゴとチェック アウト ページの概要</span><span class="sxs-lookup"><span data-stu-id="681ab-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="681ab-161">アカウント管理ページの概要</span><span class="sxs-lookup"><span data-stu-id="681ab-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
