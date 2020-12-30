---
title: 既定のカテゴリ ランディング ページと検索結果ページの概要
description: このトピックでは、Dynamics 365 Commerce での既定のカテゴリ ランディング ページと検索結果ページの概要を提供します。
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
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
ms.openlocfilehash: e85449c10fa4a768a144ce423a77bd1fc2c94352
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413719"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a><span data-ttu-id="f6d14-103">既定のカテゴリ ランディング ページと検索結果ページの概要</span><span class="sxs-lookup"><span data-stu-id="f6d14-103">Default category landing page and search results page overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f6d14-104">このトピックでは、Microsoft Dynamics 365 Commerce E コマースでの既定のカテゴリ ランディング ページと検索結果ページの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="f6d14-104">This topic provides an overview of the default category landing page and search results page in Microsoft Dynamics 365 Commerce e-Commerce.</span></span>

## <a name="default-category-landing-page"></a><span data-ttu-id="f6d14-105">既定のカテゴリ ランディング ページ</span><span class="sxs-lookup"><span data-stu-id="f6d14-105">Default category landing page</span></span>

<span data-ttu-id="f6d14-106">既定のカテゴリ ランディング ページは、Web サイトのユーザーがナビゲーション階層でカテゴリを選択したときに、通常表示されるページです。</span><span class="sxs-lookup"><span data-stu-id="f6d14-106">The default category landing page is the page that website users typically are taken to when they select a category in the navigation hierarchy.</span></span> <span data-ttu-id="f6d14-107">カテゴリ ページを使用すると、参照したり、分類された製品を並べ替えたり、絞り込んだりすることができます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-107">The category page lets you browse, and you can also sort and refine the categorized products.</span></span>

![既定のカテゴリ ランディング ページ](./media/SimpleCategoryLandingDressCategory.png)

<span data-ttu-id="f6d14-109">ページの上部には、販売促進マネージャーがカテゴリ化したすべての製品カテゴリおよび他のページを表示するヘッダーがあります。</span><span class="sxs-lookup"><span data-stu-id="f6d14-109">At the top of the page is a header that shows all the product categories and other pages that the merchandising manager has categorized.</span></span> <span data-ttu-id="f6d14-110">コンフィギュレーションはチャネル ナビゲーション階層のコンフィギュレーションの一部として実行されます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-110">Configuration is done as part of the configuration of the channel navigation hierarchy.</span></span> <span data-ttu-id="f6d14-111">ページの下部には、買い物客が興味を持つ可能性のあるさまざまなトピックへのクイック リンクを含むフッターがあります。</span><span class="sxs-lookup"><span data-stu-id="f6d14-111">At the bottom of the page is a footer that includes quick links to various topics that a shopper might be interested in.</span></span>

<span data-ttu-id="f6d14-112">カテゴリには、次のコンポーネントが不可欠です。</span><span class="sxs-lookup"><span data-stu-id="f6d14-112">The following components are essential for a category:</span></span>

- <span data-ttu-id="f6d14-113">**製品配置タイル** は、ナビゲーション階層のコンフィギュレーションの一部として、販売促進マネージャーによってカテゴリで定義された製品を示します。</span><span class="sxs-lookup"><span data-stu-id="f6d14-113">**Product placement tiles** show the products that the merchandising manager has defined in a category as part of the configuration of the navigation hierarchy.</span></span>
- <span data-ttu-id="f6d14-114">**絞り込み条件と選択肢の概要** は、カウントを提供し、品目の絞り込みに使用できるフィルターです。</span><span class="sxs-lookup"><span data-stu-id="f6d14-114">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="f6d14-115">販売促進マネージャーは、チャネル カテゴリおよび製品属性に関連するメタデータのコンフィギュレーションの一部として、これらをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="f6d14-115">The merchandising manager configures them as part of the configuration of the metadata related to channel categories and product attributes.</span></span>
- <span data-ttu-id="f6d14-116">**並べ替えのオプション** は、Web サイトの訪問者が製品を並べ替えるために使用します。</span><span class="sxs-lookup"><span data-stu-id="f6d14-116">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="f6d14-117">既定では、次の並べ替えのオプションを利用できます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-117">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="f6d14-118">価格 – 低から高</span><span class="sxs-lookup"><span data-stu-id="f6d14-118">Price – low to high</span></span>
    - <span data-ttu-id="f6d14-119">価格 – 高から低</span><span class="sxs-lookup"><span data-stu-id="f6d14-119">Price – high to low</span></span>
    - <span data-ttu-id="f6d14-120">製品名 – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="f6d14-120">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="f6d14-121">製品名 – \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="f6d14-121">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="f6d14-122">評価 – 低から高</span><span class="sxs-lookup"><span data-stu-id="f6d14-122">Ratings – low to high</span></span>
    - <span data-ttu-id="f6d14-123">評価 – 高から低</span><span class="sxs-lookup"><span data-stu-id="f6d14-123">Ratings – high to low</span></span>

- <span data-ttu-id="f6d14-124">**ページネーション** を使用すると、Web サイトの訪問者は、カテゴリ化された製品結果のあるページから別のページに移動できます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-124">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="f6d14-125">**合計数** には、カテゴリで定義されている製品の合計数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-125">**Total count** provides the total number of products that are defined in a category.</span></span>

## <a name="enrich-a-category-landing-page"></a><span data-ttu-id="f6d14-126">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="f6d14-126">Enrich a category landing page</span></span>

<span data-ttu-id="f6d14-127">カテゴリ ランディング ページに、特定のカテゴリに合わせたよりカスタマイズされた経験が必要な場合は、そのカテゴリのカテゴリ ランディング ページを「拡充」できます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-127">If you want a category landing page to have a more tailored experience for a specific category, you can "enrich" the category landing page for that category.</span></span> <span data-ttu-id="f6d14-128">たとえば、マーケティング ビデオおよびいくつかのカテゴリのストーリーテリングを追加して、買い物客の注意を引くことができます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-128">For example, you can add a marketing video and some category storytelling to get the shopper's attention.</span></span> <span data-ttu-id="f6d14-129">詳細については、[カテゴリ ランディング ページの拡充](enrich-category-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6d14-129">For more information, see [Enrich a category landing page](enrich-category-page.md).</span></span>

![拡充されたカテゴリ ランディング ページ](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a><span data-ttu-id="f6d14-131">自動提案および検索結果ページ</span><span class="sxs-lookup"><span data-stu-id="f6d14-131">Auto-suggest and search results pages</span></span>

<span data-ttu-id="f6d14-132">Web サイトのユーザーは、ナビゲーション階層からカテゴリに移動するか、検索フィールドに検索用語を入力することによってサイトを探索できます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-132">Website users can explore a site either by going to a category from the navigation hierarchy or by entering a search term in the search field.</span></span>

<span data-ttu-id="f6d14-133">ユーザーが検索フィールドに入力し始めるとすぐに、検索語を提案する没入型の自動提案機能が使用できます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-133">As soon as users start to type in the search field, they experience the immersive auto-suggest functionality that suggests search terms.</span></span>

<span data-ttu-id="f6d14-134">次に、表示される可能性のある提案のタイプをいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="f6d14-134">Here are some of the types of suggestions that might be shown:</span></span>

- <span data-ttu-id="f6d14-135">**キーワード** は、チャンネルに類別されたすべての製品の中から品目を検索するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-135">**Keywords** are used to find items across all products that are assorted to the channel.</span></span>
- <span data-ttu-id="f6d14-136">**製品** は、製品の詳細ページへの直接リンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="f6d14-136">**Products** provide direct links to the product details page.</span></span>
- <span data-ttu-id="f6d14-137">**スコープ カテゴリ検索候補** は、さまざまなカテゴリを一覧表示し、ユーザーが特定のカテゴリのキーワードを検索できるようにします。</span><span class="sxs-lookup"><span data-stu-id="f6d14-137">**Scoped category search suggestions** list various categories and let users search for the keyword in a specific category.</span></span>

![没入型の自動提案](./media/ImmersiveAutoSuggestUX.png)

<span data-ttu-id="f6d14-139">ユーザーがキーワードまたはスコープ カテゴリ検索候補のいずれかを選択した場合、または、入力した検索語句に対する提案がない場合は、検索結果ページにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-139">When users select one of the keyword or scoped category search suggestions, or when there are no suggestions for the search term that they enter, they are redirected to a search results page.</span></span> <span data-ttu-id="f6d14-140">ユーザーは、検索結果の一覧を参照、並べ替え、および絞り込んで、目的の品目を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-140">The users can then browse, sort, and refine the list of search results to find the desired item.</span></span>

![検索のランディング](./media/SearchLanding.png)

<span data-ttu-id="f6d14-142">検索結果ページには、次のコンポーネントが不可欠です。</span><span class="sxs-lookup"><span data-stu-id="f6d14-142">The following components are essential for a search results page:</span></span>

- <span data-ttu-id="f6d14-143">**製品配置タイル** は、ユーザーの検索用の製品を示します。</span><span class="sxs-lookup"><span data-stu-id="f6d14-143">**Product placement tiles** show the products for the user's search.</span></span> <span data-ttu-id="f6d14-144">既定では、これらのタイルは、ユーザー検索のクラウドベースの検索関連性スコアで並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-144">By default, these tiles are sorted by the cloud-powered search relevancy score for the user search.</span></span>
- <span data-ttu-id="f6d14-145">**絞り込み条件と選択肢の概要** は、カウントを提供し、品目の絞り込みに使用できるフィルターです。</span><span class="sxs-lookup"><span data-stu-id="f6d14-145">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="f6d14-146">販売促進マネージャーは、「チャネル カテゴリおよび製品属性」メタデータのコンフィギュレーションの一部として、これらをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="f6d14-146">The merchandising manager configures them as part of the configuration of the "channel categories and product attributes" metadata.</span></span>
- <span data-ttu-id="f6d14-147">**並べ替えのオプション** は、Web サイトの訪問者が製品を並べ替えるために使用します。</span><span class="sxs-lookup"><span data-stu-id="f6d14-147">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="f6d14-148">既定では、次の並べ替えのオプションを利用できます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-148">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="f6d14-149">価格 – 低から高</span><span class="sxs-lookup"><span data-stu-id="f6d14-149">Price – low to high</span></span>
    - <span data-ttu-id="f6d14-150">価格 – 高から低</span><span class="sxs-lookup"><span data-stu-id="f6d14-150">Price – high to low</span></span>
    - <span data-ttu-id="f6d14-151">製品名 – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="f6d14-151">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="f6d14-152">製品名 – \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="f6d14-152">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="f6d14-153">評価 – 低から高</span><span class="sxs-lookup"><span data-stu-id="f6d14-153">Ratings – low to high</span></span>
    - <span data-ttu-id="f6d14-154">評価 – 高から低</span><span class="sxs-lookup"><span data-stu-id="f6d14-154">Ratings – high to low</span></span>
    - <span data-ttu-id="f6d14-155">既定</span><span class="sxs-lookup"><span data-stu-id="f6d14-155">Default</span></span>

- <span data-ttu-id="f6d14-156">**ページネーション** を使用すると、Web サイトの訪問者は、カテゴリ化された製品結果のあるページから別のページに移動できます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-156">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="f6d14-157">**合計数** には、カテゴリで定義され、検索基準に合致する製品の合計数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-157">**Total count** provides the total number of products that are defined in a category and that match the search criteria.</span></span>

>[!NOTE]
><span data-ttu-id="f6d14-158">これらのクラウドを利用した検索機能は、バージョン 10.0.8 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="f6d14-158">These cloud-powered search capabilities are available starting in version 10.0.8.</span></span> <span data-ttu-id="f6d14-159">**コマース パラメーター > コンフィギュレーション パラメーター** で、「ProductSearch.UseAzureSearch が "true" に設定」されたエントリがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f6d14-159">Ensure that under **Commerce Parameters > Configuration Parameters** there is an entry for "ProductSearch.UseAzureSearch set to 'true'".</span></span> 
<span data-ttu-id="f6d14-160">![クラウドを利用した検索のためのコンフィギュレーション パラメーター](./media/CloudPoweredSearchConfigurationParameters.png)</span><span class="sxs-lookup"><span data-stu-id="f6d14-160">![Configuration parameters for cloud-powered search](./media/CloudPoweredSearchConfigurationParameters.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6d14-161">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f6d14-161">Additional resources</span></span>

[<span data-ttu-id="f6d14-162">クラウドを利用した検索の概要</span><span class="sxs-lookup"><span data-stu-id="f6d14-162">Cloud-powered search overview</span></span>](cloud-powered-search-overview.md)

[<span data-ttu-id="f6d14-163">ホーム ページの概要</span><span class="sxs-lookup"><span data-stu-id="f6d14-163">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="f6d14-164">製品詳細ページの概要</span><span class="sxs-lookup"><span data-stu-id="f6d14-164">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="f6d14-165">買い物カゴとチェックアウト ページの概要</span><span class="sxs-lookup"><span data-stu-id="f6d14-165">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="f6d14-166">アカウント管理ページの概要</span><span class="sxs-lookup"><span data-stu-id="f6d14-166">Account management pages overview</span></span>](quick-tour-account-management.md)

