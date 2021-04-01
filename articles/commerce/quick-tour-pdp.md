---
title: 製品詳細ページの概要
description: このトピックでは、Microsoft Dynamics 365 Commerce の製品詳細ページ (PDP) の概要を示します。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 020c2a72515eb112adb33c6b58e3a5084339d040
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243840"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="b85c5-103">製品詳細ページの概要</span><span class="sxs-lookup"><span data-stu-id="b85c5-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b85c5-104">このトピックでは、Microsoft Dynamics 365 Commerce の製品詳細ページ (PDP) の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="b85c5-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b85c5-105">概要</span><span class="sxs-lookup"><span data-stu-id="b85c5-105">Overview</span></span>

<span data-ttu-id="b85c5-106">PDP は、製品に関する詳細情報を提供し、顧客がサイズ、スタイル、および色などの製品オプションを選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b85c5-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="b85c5-107">PDP は顧客が購入決定をするために必要なすべての製品情報を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b85c5-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="b85c5-108">次の図は、PDP の例を示します。</span><span class="sxs-lookup"><span data-stu-id="b85c5-108">The following illustration shows an example of a PDP.</span></span>

![製品の詳細ページの例](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="b85c5-110">ヘッダーとフッター モジュール</span><span class="sxs-lookup"><span data-stu-id="b85c5-110">Header and footer modules</span></span>

<span data-ttu-id="b85c5-111">PDP の上部には、小売業者が顧客に参照させたいすべての製品カテゴリおよび他のページを表示するヘッダーがあります。</span><span class="sxs-lookup"><span data-stu-id="b85c5-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="b85c5-112">ページの下部には、顧客が興味を持つさまざまなトピックへのクイック リンクを含むフッターがあります。</span><span class="sxs-lookup"><span data-stu-id="b85c5-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="b85c5-113">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="b85c5-113">Buy box module</span></span>

<span data-ttu-id="b85c5-114">PDP の最も重要なモジュールは購入ボックス モジュールで、ページの主なセクションの最初の項目として表示されます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="b85c5-115">購入ボックス モジュールは、製品名、製品説明、製品価格、製品画像、製品評価などの重要な製品情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="b85c5-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="b85c5-116">購入ボックス モジュールにより、顧客は製品オプション (たとえば、サイズ、スタイル、および色) を選択して、製品を買い物カゴに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="b85c5-117">また、顧客が製品をオンラインで購入し、店舗で受取ることもできます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="b85c5-118">オンライン購入店舗受取りのモジュールは、Bing Maps のアプリケーション プログラミング インターフェイス (API) との統合を使用して、最寄りの店舗、または顧客が指定した別の場所の店舗を検索します。</span><span class="sxs-lookup"><span data-stu-id="b85c5-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="b85c5-119">購入ボックス モジュールには製品 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="b85c5-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="b85c5-120">この ID は、ページ コンテキストから派生します。</span><span class="sxs-lookup"><span data-stu-id="b85c5-120">This ID is derived from the page context.</span></span> <span data-ttu-id="b85c5-121">購入ボックス モジュールがページ コンテキストに製品 ID が含まれていないページに追加される場合、情報は正しく表示されません。</span><span class="sxs-lookup"><span data-stu-id="b85c5-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="b85c5-122">製品仕様のモジュール</span><span class="sxs-lookup"><span data-stu-id="b85c5-122">Product specifications module</span></span>

<span data-ttu-id="b85c5-123">製品仕様モジュールは、製品に関する追加情報を表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="b85c5-124">これらの詳細は、コマースの製品属性から取得されます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="b85c5-125">製品仕様モジュールは、**表示** プロパティが **はい** に設定されているすべての属性を表示します。</span><span class="sxs-lookup"><span data-stu-id="b85c5-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="b85c5-126">製品属性を取得するには、製品 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="b85c5-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="b85c5-127">推奨モジュール</span><span class="sxs-lookup"><span data-stu-id="b85c5-127">Recommendations module</span></span>

<span data-ttu-id="b85c5-128">推奨モジュールは、PDP で重要なモジュールです。</span><span class="sxs-lookup"><span data-stu-id="b85c5-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="b85c5-129">顧客が製品を参照している間、正しい製品を見つけて購買することができるように、より多くの製品オプションを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b85c5-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="b85c5-130">推奨事項により、顧客は関連するコンテンツを簡単に見つけて、ショッピングを継続することができます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="b85c5-131">異なるタイプの推奨項目リストが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="b85c5-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="b85c5-132">**人気製品** リストは機械学習に基づいています。</span><span class="sxs-lookup"><span data-stu-id="b85c5-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="b85c5-133">他の顧客のトランザクション履歴を使用して、推奨事項を提供します。</span><span class="sxs-lookup"><span data-stu-id="b85c5-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="b85c5-134">このリストは推奨項目サービスによって生成され、「この製品を購入した顧客はこちらも購入しました」リストに似ています。</span><span class="sxs-lookup"><span data-stu-id="b85c5-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="b85c5-135">このリストを生成するには、製品 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="b85c5-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="b85c5-136">**関連** リストは、コマースの製品についてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="b85c5-137">たとえば、茶色のレザーの旅行用ハンドバッグの場合、レザー製または旅行目的のためにデザインされた、さらに多くのハンドバッグを関連リストにコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="b85c5-138">**アクセサリ** および **類似製品** など他のタイプの関連リストも、コマースでコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="b85c5-139">このリストを生成するには、製品 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="b85c5-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="b85c5-140">したがって、ページ コンテキストに製品 ID が含まれていないホーム ページに追加すると、リストは空になります。</span><span class="sxs-lookup"><span data-stu-id="b85c5-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="b85c5-141">**トレンド**、**ベスト セラー**、および **新規** など、アルゴリズムによって生成された推奨項目リストは PDP 上で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="b85c5-142">これらのリストは、PDP 上の製品に直接関連していないことがありますが、顧客が興味を持つ可能性がある製品を検索するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="b85c5-143">これらのタイプのリストには、製品 ID は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="b85c5-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="b85c5-144">これらは、サイト間でのショッピング パターンに基づいて生成される一般的なリストです。</span><span class="sxs-lookup"><span data-stu-id="b85c5-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="b85c5-145">編集リストは、手動で精選されたリストです。</span><span class="sxs-lookup"><span data-stu-id="b85c5-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="b85c5-146">たとえば、小売業者は、紹介する製品のリストを手動で精選することがあります。</span><span class="sxs-lookup"><span data-stu-id="b85c5-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="b85c5-147">評価とレビュー モジュール</span><span class="sxs-lookup"><span data-stu-id="b85c5-147">Ratings and reviews modules</span></span>

<span data-ttu-id="b85c5-148">レビューを表示および追加するのに、次の 3 つのモジュールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="b85c5-149">**レビュー** – このモジュール リストは、他の顧客によって提供された評価とレビューを表示します。</span><span class="sxs-lookup"><span data-stu-id="b85c5-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="b85c5-150">顧客は、レビューの並べ替えやフィルター処理ができます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="b85c5-151">また、このモジュールでは、顧客がレビューを気に入るか気に入らないか、問題を報告することもできます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="b85c5-152">**レビュー書き込み** – このモジュールでは、製品の独自のレビューを書き込めます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="b85c5-153">**評価ヒストグラム** – このモジュールには製品の評価傾向を示すヒストグラムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="b85c5-154">詳細については、[評価とレビューの概要](ratings-reviews-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b85c5-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="b85c5-155">マーケティング モジュール</span><span class="sxs-lookup"><span data-stu-id="b85c5-155">Marketing modules</span></span>

<span data-ttu-id="b85c5-156">マーケティング コンテンツが特定の製品固有のものである場合、すべてのマーケティング モジュールを PDP に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="b85c5-157">ページを「拡充」することにより、マーケティング モジュールを PDP に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b85c5-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="b85c5-158">詳細については、[製品ページの拡充](enrich-product-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b85c5-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b85c5-159">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b85c5-159">Additional resources</span></span>

[<span data-ttu-id="b85c5-160">ホーム ページの概要</span><span class="sxs-lookup"><span data-stu-id="b85c5-160">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="b85c5-161">買い物カゴとチェックアウト ページの概要</span><span class="sxs-lookup"><span data-stu-id="b85c5-161">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="b85c5-162">アカウント管理ページの概要</span><span class="sxs-lookup"><span data-stu-id="b85c5-162">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="b85c5-163">製品の詳細ページの拡充</span><span class="sxs-lookup"><span data-stu-id="b85c5-163">Enrich a product details page</span></span>](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]