---
title: クラウドを利用した検索の概要
description: このトピックでは、Microsoft Dynamics 365 Commerce でのクラウドを利用した検索の概要を示します。
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 015f308640117b1354868c9f37e4b8df9cac6f2a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697201"
---
# <a name="cloud-powered-search-overview"></a><span data-ttu-id="c3bdf-103">クラウドを利用した検索の概要</span><span class="sxs-lookup"><span data-stu-id="c3bdf-103">Cloud-powered search overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c3bdf-104">このトピックでは、Microsoft Dynamics 365 Commerce でのクラウドを利用した検索の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-104">This topic gives an overview of cloud-powered search in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c3bdf-105">概要</span><span class="sxs-lookup"><span data-stu-id="c3bdf-105">Overview</span></span>

<span data-ttu-id="c3bdf-106">製品の発見可能性は、カテゴリの閲覧、検索、およびフィルタリングにより、顧客が迅速かつ簡単に製品を見つけられることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-106">Product discoverability helps guarantee that customers can quickly and easily find products by browsing categories, searching, and filtering.</span></span> <span data-ttu-id="c3bdf-107">小売業者は、製品の検出を、すべての小売チャンネルでの顧客とのやり取りにおける主要なツールと考えています。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-107">Retailers consider product discovery a primary tool for customer interaction across all retail channels.</span></span>

<span data-ttu-id="c3bdf-108">顧客は、Web 検索エンジン、洗練された E コマース Web サイト、ソーシャル アプリ、検索用語の入力時に表示される自動提案、ファセット ナビゲーション、および強調表示のほぼ瞬時の応答時間に慣れています。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-108">Customers are accustomed to the nearly instantaneous response times of web search engines, sophisticated e-Commerce websites, social apps, automatic suggestions that appear as they type search terms, faceted navigation, and highlighting.</span></span> <span data-ttu-id="c3bdf-109">探している製品を、ある E コマース ストアで十分な速さで見つけることができなければ、顧客は別の E コマース ストアへ移動してしまいます。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-109">If customers can't find the product that they are looking for quickly enough in one e-Commerce store, they won't hesitate to go to a different e-Commerce store.</span></span>

<span data-ttu-id="c3bdf-110">Dynamics 365 Commerce のクラウドを利用した製品の発見可能性により、小売業者は、E コマース チャネルと販売時点管理 (POS) チャネルの両方で、すべてのチャネルにおける消費者の保持とコンバージョンを向上させ続けることができます。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-110">The cloud-powered product discoverability in Dynamics 365 Commerce helps retailers continue to increase consumer retention and conversion rates across all channels, both e-Commerce channels and point of sale (POS) channels.</span></span>

<span data-ttu-id="c3bdf-111">Dynamics 365 Commerce 検索エクスペリエンスの機能が改善され、小売業者は製品の発見可能性を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-111">The Dynamics 365 Commerce search experience has improved capabilities to help retailers achieve better product discoverability.</span></span> <span data-ttu-id="c3bdf-112">同時に、これらの機能は、E コマースのトラフィックに必要なスケーラビリティとパフォーマンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-112">At the same time, these capabilities deliver the scalability and performance that are required for e-Commerce traffic.</span></span>

## <a name="browse-and-search"></a><span data-ttu-id="c3bdf-113">参照と検索</span><span class="sxs-lookup"><span data-stu-id="c3bdf-113">Browse and search</span></span>

<span data-ttu-id="c3bdf-114">製品の発見は主に、情報の取得とコンテンツ ナビゲーションの検索機能に依存するため、検索の関連性とパフォーマンスはオムニチャネル エクスペリエンスの重要な要素です。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-114">Search relevance and performance are key factors in the omnichannel experience, because product discovery relies primarily on search functionality for information retrieval and content navigation.</span></span> <span data-ttu-id="c3bdf-115">効果的かつ効率的な参照と検索のエクスペリエンスによって、コンバージョンが増える場合があります。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-115">An effective and efficient browse and search experience helps increase conversion.</span></span>

<span data-ttu-id="c3bdf-116">次の図は、一般的な参照と検索の機能の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-116">The following illustration shows an example of typical browse and search functionality.</span></span>

![検索のランディング ページ](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a><span data-ttu-id="c3bdf-118">ファセットナビゲーションと選択の概要</span><span class="sxs-lookup"><span data-stu-id="c3bdf-118">Faceted navigation and choice summary</span></span> 

<span data-ttu-id="c3bdf-119">ファセット ナビゲーションを使用すると、用語セット内の用語にリンクされた絞り込み条件をフィルタ処理することにより、顧客はコンテンツを簡単に参照できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-119">Faceted navigation helps customers more easily browse for content by letting them filter on refiners that are linked to terms in a term set.</span></span> <span data-ttu-id="c3bdf-120">顧客が絞り込み条件を選択して適用すると、選択肢の概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-120">After a customer has selected and applied refiners, a summary of the choices is shown.</span></span> 

<span data-ttu-id="c3bdf-121">ファセット ナビゲーションを使用することで、追加のページを作成することなく、用語セット内の用語ごとに異なる絞り込み条件をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-121">By using faceted navigation, you can configure different refiners for different terms in a term set, without having to create additional pages.</span></span> 

<span data-ttu-id="c3bdf-122">次の図は、ファセット ナビゲーションが検索で使用されている例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-122">The following illustration shows an example where faceted navigation is used in a search.</span></span>

![選択の概要](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a><span data-ttu-id="c3bdf-124">没入型の自動提案</span><span class="sxs-lookup"><span data-stu-id="c3bdf-124">Immersive autosuggest</span></span>

<span data-ttu-id="c3bdf-125">現在の自動提案機能では、一致するキーワードの検索をトリガーするキーワードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-125">Current autosuggest functionality just shows keywords that trigger a search for the matching keyword.</span></span> <span data-ttu-id="c3bdf-126">Dynamics 365 Commerce の新しい機能拡張により、ユーザーは入力を完了する前に製品へのリンクを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-126">Because of new enhancements in Dynamics 365 Commerce, customers can often discover links to products before they have finished typing.</span></span>

<span data-ttu-id="c3bdf-127">Dynamics 365 Commerce では、さまざまなカテゴリでのキーワード照合の機能もサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-127">Dynamics 365 Commerce also supports functionality for keyword matches in various categories.</span></span> <span data-ttu-id="c3bdf-128">この機能により、顧客はカテゴリ全体で一致するキーワードの数を確認し、他のカテゴリのキーワードの検索をトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-128">This functionality lets customers see the number of matching keywords across categories and trigger a search for a keyword in other categories.</span></span>

<span data-ttu-id="c3bdf-129">次の図は、没入型の自動提案が使用されている例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-129">The following illustration shows an example where immersive autosuggest is being used.</span></span>

![没入型の自動提案](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a><span data-ttu-id="c3bdf-131">並べ替え</span><span class="sxs-lookup"><span data-stu-id="c3bdf-131">Sort</span></span>

<span data-ttu-id="c3bdf-132">Dynamics 365 Commerce の強化された並べ替えにより、顧客は検索結果を並べ替え、検索、参照し、価格、製品名、製品番号などの基準で検索結果を絞り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-132">Enhanced sorting in Dynamics 365 Commerce lets customers sort, search, and browse search results, and refine them by criteria such as price, product name, and product number.</span></span> <span data-ttu-id="c3bdf-133">顧客は、製品が新しいか、売れ筋か、または最近追加されたかに基づいて、結果を並べ替えることもできます。</span><span class="sxs-lookup"><span data-stu-id="c3bdf-133">Customers can also sort results based on whether a product is new, top-selling, or recently added.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3bdf-134">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c3bdf-134">Additional resources</span></span>

[<span data-ttu-id="c3bdf-135">既定のカテゴリ ランディング ページと検索結果ページ</span><span class="sxs-lookup"><span data-stu-id="c3bdf-135">Default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="c3bdf-136">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="c3bdf-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)