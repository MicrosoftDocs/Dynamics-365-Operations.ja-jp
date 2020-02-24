---
title: カテゴリ ランディング ページの拡充
description: このトピックでは、Dynamics 365 Commerce のカテゴリ ページの拡充について説明します。
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
ms.openlocfilehash: 71348efba9fc1374b9e6599eb23f198d3851036e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003053"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="d1fc2-103">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="d1fc2-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d1fc2-104">このトピックでは、Dynamics 365 Commerce のカテゴリ ページの拡充について説明します。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d1fc2-105">概要</span><span class="sxs-lookup"><span data-stu-id="d1fc2-105">Overview</span></span>

<span data-ttu-id="d1fc2-106">コマースは、カテゴリ データを表示するときに使用される既定のカテゴリのランディング ページを提供します。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="d1fc2-107">既定のカテゴリ ページには、絞り込み条件、分類された製品の配置、並べ替えオプション、選択の概要、ページネーション コントロールなどの必須要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="d1fc2-108">ただし、既定のカテゴリ ページを使用する代わりに、コンテンツがより多く、より具体的な要素を持つ「拡充された」カテゴリのランディング ページを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="d1fc2-109">一般的な拡充には、カテゴリ固有のマーケティング コンテンツをカテゴリ ページに追加することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="d1fc2-110">このコンテンツには、クロスセルを目的としたカテゴリ間の製品配置、編集リスト、画像、ビデオ、およびその他のテキストが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="d1fc2-111">既定のカテゴリ ページを変更するか、特定のカテゴリに対して別のカテゴリ ページを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![拡充されたカテゴリ ランディング ページ](./media/CategoryLandingPages.png)

<span data-ttu-id="d1fc2-113">オーサリング ツールの**製品**ページには、サイトに割り当てられているチャネルのカテゴリの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-113">In the authoring tool, the **Product** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="d1fc2-114">**拡充**ステータスがカテゴリ ページに選択されている場合は、そのカテゴリ ページは拡充されています。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="d1fc2-115">それ以外の場合、カテゴリには既定のカテゴリ ページとコンテンツが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="d1fc2-116">カテゴリ名を選択して、カテゴリの拡充カテゴリ ページと非拡充カテゴリ ページの両方をプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="d1fc2-117">カテゴリ ページを拡充するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="d1fc2-118">**製品**ページで、カテゴリ ページを拡充するカテゴリの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-118">On the **Products** page, select the name of the category that you want to enrich the category page for.</span></span> <span data-ttu-id="d1fc2-119">選択したカテゴリの既定のカテゴリのページが、ページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="d1fc2-120">**カテゴリ ページの拡充**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="d1fc2-121">拡充したカテゴリ ページのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="d1fc2-122">マイナーな変更のみを行う場合は、既定のカテゴリ ページを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="d1fc2-123">または、特定のカテゴリ ページ テンプレートを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="d1fc2-124">テンプレートを選択すると、ページ エディターが開き、選択したテンプレートを使用して、選択したカテゴリの新しいカテゴリ ページが作成されます。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="d1fc2-125">ページはチェックアウトされ、変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="d1fc2-126">カテゴリ仕様データを使用するモジュールは、選択したカテゴリのデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-126">Modules that use category specification data use the data from your selected category.</span></span>
>
> <span data-ttu-id="d1fc2-127">選択するテンプレートの設定によって、実行できる変更が決まります。</span><span class="sxs-lookup"><span data-stu-id="d1fc2-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1fc2-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d1fc2-128">Additional resources</span></span>

[<span data-ttu-id="d1fc2-129">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="d1fc2-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="d1fc2-130">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="d1fc2-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="d1fc2-131">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="d1fc2-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="d1fc2-132">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="d1fc2-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="d1fc2-133">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="d1fc2-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="d1fc2-134">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="d1fc2-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="d1fc2-135">ページ コンテンツ アクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="d1fc2-135">Verify page content accessibility</span></span>](verify-accessibility.md)
