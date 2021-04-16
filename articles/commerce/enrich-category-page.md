---
title: カテゴリ ランディング ページの拡充
description: このトピックでは、Dynamics 365 Commerce のカテゴリ ページの拡充について説明します。
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5e18439fc0e91619cade33b83b87be0d5c4d1040
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799014"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="8703c-103">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="8703c-103">Enrich a category landing page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8703c-104">このトピックでは、Dynamics 365 Commerce のカテゴリ ページの拡充について説明します。</span><span class="sxs-lookup"><span data-stu-id="8703c-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8703c-105">コマースは、カテゴリ データを表示するときに使用される既定のカテゴリのランディング ページを提供します。</span><span class="sxs-lookup"><span data-stu-id="8703c-105">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="8703c-106">既定のカテゴリ ページには、絞り込み条件、分類された製品の配置、並べ替えオプション、選択の概要、ページネーション コントロールなどの必須要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8703c-106">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="8703c-107">ただし、既定のカテゴリ ページを使用する代わりに、コンテンツがより多く、より具体的な要素を持つ「拡充された」カテゴリのランディング ページを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="8703c-107">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="8703c-108">一般的な拡充には、カテゴリ固有のマーケティング コンテンツをカテゴリ ページに追加することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8703c-108">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="8703c-109">このコンテンツには、クロスセルを目的としたカテゴリ間の製品配置、編集リスト、画像、ビデオ、およびその他のテキストが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="8703c-109">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="8703c-110">既定のカテゴリ ページを変更するか、特定のカテゴリに対して別のカテゴリ ページを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="8703c-110">You can either modify the default category page or define a different category page for a specific category.</span></span>

![拡充されたカテゴリ ランディング ページ](./media/CategoryLandingPages.png)

<span data-ttu-id="8703c-112">Commerce のサイト ビルダーの **製品** ページには、サイトに割り当てられているチャネルのカテゴリの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8703c-112">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="8703c-113">**拡充** ステータスがカテゴリ ページに選択されている場合は、そのカテゴリ ページは拡充されています。</span><span class="sxs-lookup"><span data-stu-id="8703c-113">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="8703c-114">それ以外の場合、カテゴリには既定のカテゴリ ページとコンテンツが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8703c-114">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="8703c-115">カテゴリ名を選択して、カテゴリの拡充カテゴリ ページと非拡充カテゴリ ページの両方をプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="8703c-115">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="8703c-116">カテゴリ ページを拡充するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="8703c-116">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="8703c-117">**製品** ページで、カテゴリ ページを拡充するカテゴリの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="8703c-117">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="8703c-118">選択したカテゴリの既定のカテゴリのページが、ページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="8703c-118">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="8703c-119">**カテゴリ ページの拡充** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8703c-119">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="8703c-120">拡充したカテゴリ ページのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="8703c-120">Select a template for the enriched category page.</span></span> <span data-ttu-id="8703c-121">マイナーな変更のみを行う場合は、既定のカテゴリ ページを選択できます。</span><span class="sxs-lookup"><span data-stu-id="8703c-121">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="8703c-122">または、特定のカテゴリ ページ テンプレートを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="8703c-122">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="8703c-123">テンプレートを選択すると、ページ エディターが開き、選択したテンプレートを使用して、選択したカテゴリの新しいカテゴリ ページが作成されます。</span><span class="sxs-lookup"><span data-stu-id="8703c-123">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="8703c-124">ページはチェックアウトされ、変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="8703c-124">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="8703c-125">カテゴリ仕様データを使用するモジュールは、選択したカテゴリのデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="8703c-125">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="8703c-126">選択するテンプレートの設定によって、実行できる変更が決まります。</span><span class="sxs-lookup"><span data-stu-id="8703c-126">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8703c-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8703c-127">Additional resources</span></span>

[<span data-ttu-id="8703c-128">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="8703c-128">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="8703c-129">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="8703c-129">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="8703c-130">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="8703c-130">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="8703c-131">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="8703c-131">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="8703c-132">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="8703c-132">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="8703c-133">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="8703c-133">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="8703c-134">ページ コンテンツのアクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="8703c-134">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="8703c-135">URL のパラメーターに基いて動的な電子商取引ページを作成する</span><span class="sxs-lookup"><span data-stu-id="8703c-135">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
