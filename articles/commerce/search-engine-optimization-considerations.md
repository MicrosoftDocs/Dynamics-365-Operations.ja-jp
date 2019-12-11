---
title: サイトにおける検索エンジン最適化 (SEO) の考慮事項
description: このトピックでは、サイトの開発から運用における、検索エンジンの最適化 (SEO) の考慮事項について説明します。
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b35d0cb606e1b17a0258ea3fcb6287988d83091c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698214"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="f7dfa-103">サイトにおける検索エンジン最適化 (SEO) の考慮事項</span><span class="sxs-lookup"><span data-stu-id="f7dfa-103">Search engine optimization (SEO) considerations for your site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f7dfa-104">このトピックでは、サイトの開発から運用における、検索エンジンの最適化 (SEO) の考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="f7dfa-105">開発中のサイト</span><span class="sxs-lookup"><span data-stu-id="f7dfa-105">A site that is under development</span></span>

<span data-ttu-id="f7dfa-106">サイトが開発中の間、検索エンジンがページにインデックスを付けず、サイトの開発バージョンをキャッシュに保存しないようにするために、すべてのサイト ページに **NOINDEX** および **NOFOLLOW** メタ タグがある必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="f7dfa-107">このコンフィギュレーションを実行するには、既定のメタ タグのモジュールをサイト ページのテンプレートに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="f7dfa-108">既定のメタ タグのプロパティは、ページ エディターの SEO プロパティ セクションで使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="f7dfa-109">これらのプロパティを使用して、メタ タグを管理できます。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="f7dfa-110">サイトのソフト起動</span><span class="sxs-lookup"><span data-stu-id="f7dfa-110">Soft launch of a site</span></span>

<span data-ttu-id="f7dfa-111">「ソフト起動」中、完全な起動が行われる前は、限られた対象者またはマーケットに Web サイトが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="f7dfa-112">Web サイトのソフト起動を行う場合、**NOINDEX** メタ タグの配置を検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="f7dfa-113">この方法で、ソフト起動が確実に制限された対象者だけに限定されるようにできます。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="f7dfa-114">運用中のサイト</span><span class="sxs-lookup"><span data-stu-id="f7dfa-114">A site that is in production</span></span>

<span data-ttu-id="f7dfa-115">サイトが運用中の場合、すべてのサイト ページが正しくタグ付けされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="f7dfa-116">Microsoft Dynamics 365 Commerce は、ページに入力された情報を使用して、ページのすべての SEO 情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="f7dfa-117">カテゴリ ページの概要、リスト ページの概要、および製品ページの概要のモジュールは、この機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="f7dfa-118">検索エンジンのインデックスを最適化するために、レンダリング フレームワークは、Dynamics 365 Commerce およびモジュール固有の情報でコンフィギュレーションされた SEO プロパティからの両方の情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="f7dfa-119">運用中のサイトの場合、robots.txt ファイルによりサイト全体のインデックスを作成することができ、公開したサイト マップ ドキュメントへのリンクを含んでいる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="f7dfa-120">**サイトの設定 \> サイト マップの有効化**で、サイト マップ生成の機能をオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="f7dfa-121">内部プレビュー、制限された対象者、およびすべての対象者に対するページの SEO 設定</span><span class="sxs-lookup"><span data-stu-id="f7dfa-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="f7dfa-122">Dynamics 365 Commerce は 「What You See Is What You Get」 (WYSIWYG) 認証のプレビューをサポートしているので、作成者は情報がサイト訪問者に表示されるか心配することなく、ページ コンテンツを準備することができます。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="f7dfa-123">ページを公開する必要はあるが、エクスポージャは制限する必要がある場合、検索エンジンでインデックスが作成されないようにするために **NOINDEX** メタ タグが必要です。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="f7dfa-124">ページがすべての対象者に準備されている場合、検索エンジン インデックスの効率を最大にするために、すべての基本的な SEO メタ データが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="f7dfa-125">また、**NOLIMIT** メタ タグを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7dfa-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7dfa-126">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f7dfa-126">Additional resources</span></span>

[<span data-ttu-id="f7dfa-127">E コマース ユーザーとロールの管理</span><span class="sxs-lookup"><span data-stu-id="f7dfa-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="f7dfa-128">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="f7dfa-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="f7dfa-129">コンテンツ セキュリティ ポリシー (CSP) の管理</span><span class="sxs-lookup"><span data-stu-id="f7dfa-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
