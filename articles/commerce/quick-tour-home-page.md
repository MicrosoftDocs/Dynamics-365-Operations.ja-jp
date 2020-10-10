---
title: ホーム ページの概要
description: このトピックでは、Microsoft Dynamics 365 Commerce のホーム ページの概要を提供します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 3ebc8b4ebd3720815cdaaab708fbfdd8302cbea1
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817757"
---
# <a name="home-page-overview"></a><span data-ttu-id="0598d-103">ホーム ページの概要</span><span class="sxs-lookup"><span data-stu-id="0598d-103">Home page overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0598d-104">このトピックでは、Microsoft Dynamics 365 Commerce のホーム ページの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="0598d-104">This topic provides an overview of the home page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0598d-105">概要</span><span class="sxs-lookup"><span data-stu-id="0598d-105">Overview</span></span>

<span data-ttu-id="0598d-106">ホーム ページは、買い物客が E コマース サイトにアクセスした場合に移動する既定のページです。</span><span class="sxs-lookup"><span data-stu-id="0598d-106">The home page is the default page that shoppers go to when they visit an e-Commerce site.</span></span> <span data-ttu-id="0598d-107">通常、このページは、マーケティング モジュールの組み合わせを使用して、製品およびプロモーションを示します。</span><span class="sxs-lookup"><span data-stu-id="0598d-107">Typically, this page showcases products and promotions by using a combination of marketing modules.</span></span> <span data-ttu-id="0598d-108">ホーム ページは、買い物客を関連付けるために、豊かな画像とテキストが必要です。</span><span class="sxs-lookup"><span data-stu-id="0598d-108">The home page should be rich with images and text to keep shoppers engaged.</span></span>

<span data-ttu-id="0598d-109">以下の図は、モジュール ライブラリおよび 「Fabrikam」 のテーマを使用してビルドされたホーム ページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="0598d-109">The following illustration shows an example of a home page that was built by using the module library and the "Fabrikam" theme.</span></span>

![ホーム ページの例](./media/Homepage2.PNG)

<span data-ttu-id="0598d-111">ホーム ページの上部には、小売業者が顧客に参照させたいすべての製品カテゴリおよび他のページを表示するヘッダーがあります。</span><span class="sxs-lookup"><span data-stu-id="0598d-111">The top of the home page has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="0598d-112">ホーム ページの下部には、顧客が興味を持つさまざまなトピックへのクイック リンクを含むフッターがあります。</span><span class="sxs-lookup"><span data-stu-id="0598d-112">The bottom of the home page has a footer that contains quick links to various topics that might interest customers.</span></span>

<span data-ttu-id="0598d-113">ホーム ページの主なセクションは、さまざまな Dynamics 365 Commerce モジュールを使用して、製品、カテゴリ、またはプロモーションを強調することができます。</span><span class="sxs-lookup"><span data-stu-id="0598d-113">The main section of the home page can highlight products, categories, or promotions by using various Dynamics 365 Commerce modules:</span></span>

- <span data-ttu-id="0598d-114">**ヒーロー** – 通常、主なセクションの最初の項目には、店舗の新しい製品およびプロモーションを強調する 1 つ以上の「ヒーロー」画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0598d-114">**Hero** – Typically, the first item at the top of the main section shows one or more "hero" images that highlight new products and promotions in the store.</span></span> <span data-ttu-id="0598d-115">ヒーロー画像が複数ある場合、ユーザーが参照できるようにカルーセル モジュール内でホストされます。</span><span class="sxs-lookup"><span data-stu-id="0598d-115">If there are multiple hero images, they are hosted in a carousel module so that users can browse them.</span></span>

    <span data-ttu-id="0598d-116">以下の図は、主なセクションの最初の項目が "新着" と呼ばれるコンテンツ ブロック モジュールのヒーロー レイアウトであるホーム ページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="0598d-116">The following illustration shows an example of a home page where the first item in the main section is a hero layout of a content block module that is named "New Arrival."</span></span>

    ![ヒーロー モジュールの例](./media/Hero.PNG)

- <span data-ttu-id="0598d-118">**機能** – 画像とテキストの組み合わせを使用して製品またはプロモーションをマーケティングするために、コンテンツ ブロック モジュールの機能レイアウトが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0598d-118">**Feature** – A feature layout of a content block module is used to market products or promotions by using a combination of images and text.</span></span> <span data-ttu-id="0598d-119">機能レイアウトは個別に使用することができ、またカルーセル モジュールでホストすることもできます。</span><span class="sxs-lookup"><span data-stu-id="0598d-119">Features layouts can be used independently, or they can be hosted in a carousel module.</span></span>

    <span data-ttu-id="0598d-120">以下の図は、ホーム ページ内におけるコンテンツ ブロック モジュールの機能レイアウトの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0598d-120">The following illustration shows an example of feature layout of a content block module on a home page.</span></span>

    ![機能モジュールの例](./media/Feature.PNG)

- <span data-ttu-id="0598d-122">**タイル** – コンテンツ ブロック モジュールのタイル レイアウトは、複数行レイアウトの画像とテキストの組み合わせを使用して、複数の製品または製品カテゴリを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0598d-122">**Tile** – A tile layout of a content block module is used to showcase multiple products or category of products by using a combination of images and text in a multicolumn layout.</span></span> <span data-ttu-id="0598d-123">このトピックの前の部分で示したホーム ページの図において、タイル レイアウトは、**女性店員**、**男性店員**、および**店舗のアクセサリ**項目の 3 列のレンダリングで使用されています。</span><span class="sxs-lookup"><span data-stu-id="0598d-123">In the illustration of a home page that appears earlier in this topic, a tile  layout is used for the three-column rendering of the **Shop Women**, **Shop Men**, and **Shop Accessories** items.</span></span>
- <span data-ttu-id="0598d-124">**ビデオ プレーヤー** – ビデオ プレーヤー モジュールを使用して、ホーム ページにビデオ コンテンツを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0598d-124">**Video player** – A video player module can be used to showcase video content on the home page.</span></span> <span data-ttu-id="0598d-125">このトピックの前の部分で示したホーム ページの図には、ビデオ プレーヤー モジュールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0598d-125">The illustration of a home page that appears earlier in this topic includes a video player module.</span></span>
- <span data-ttu-id="0598d-126">**テキスト ブロック** – コンテンツ リッチ ブロック モジュールを使用して、1 列または複数列のレイアウトのホーム ページにテキスト コンテンツを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0598d-126">**Text block** – A content rich block module can be used to present text content on the home page in a single-column or multicolumn layout.</span></span>
- <span data-ttu-id="0598d-127">**製品の推奨事項** – 製品推奨モジュールを使用して、ホーム ページの**新規**、**トレンド**、および**ベスト セラー**などのリストを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0598d-127">**Product recommendations** – Product recommendations modules are used to show lists, such as **New**, **Trending**, and **Best Selling** on the home page.</span></span> <span data-ttu-id="0598d-128">これらの一覧は、ショッピングのトレンドに基づき、アルゴリズムにより生成、または手動で精選された製品を表示します。</span><span class="sxs-lookup"><span data-stu-id="0598d-128">These lists showcase products based on shopping trends, and they can be algorithmically generated or manually curated.</span></span> <span data-ttu-id="0598d-129">顧客が上位製品を見つけて、買い物を継続するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0598d-129">They help customers quickly discover top products and then continue to shop.</span></span>

    <span data-ttu-id="0598d-130">以下の図は、ホーム ページ内における製品推奨モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0598d-130">The following illustration shows an example of product recommendations modules on a home page.</span></span>

    ![製品推奨モジュールの例](./media/Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="0598d-132">ここに一覧表示されているすべてのモジュールは、すべてのサイト ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="0598d-132">All the modules that are listed here can be used on any site page.</span></span> <span data-ttu-id="0598d-133">ただし、顧客がサイトで最初に対話するページなので、ホーム ページ上での配置は重要です。</span><span class="sxs-lookup"><span data-stu-id="0598d-133">However, their placement on the home page is important because that page is where customers first interact with your site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0598d-134">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0598d-134">Additional resources</span></span>

[<span data-ttu-id="0598d-135">製品詳細ページの概要</span><span class="sxs-lookup"><span data-stu-id="0598d-135">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="0598d-136">買い物カゴとチェックアウト ページの概要</span><span class="sxs-lookup"><span data-stu-id="0598d-136">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="0598d-137">アカウント管理ページの概要</span><span class="sxs-lookup"><span data-stu-id="0598d-137">Account management pages overview</span></span>](quick-tour-account-management.md)
