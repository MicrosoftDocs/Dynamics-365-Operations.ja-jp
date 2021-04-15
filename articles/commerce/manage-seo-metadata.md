---
title: SEO メタデータの管理
description: このトピックでは、Microsoft Dynamics 365 Commerce の検索エンジン最適化 (SEO) メタデータを管理する方法について説明します。
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794214"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="61b86-103">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="61b86-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="61b86-104">このトピックでは、Microsoft Dynamics 365 Commerce の検索エンジン最適化 (SEO) メタデータを管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="61b86-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="61b86-105">サイトの SEO メタデータは、サイト マップとページ メタデータを使用して管理できます。</span><span class="sxs-lookup"><span data-stu-id="61b86-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="61b86-106">サイト マップ</span><span class="sxs-lookup"><span data-stu-id="61b86-106">Site maps</span></span>

<span data-ttu-id="61b86-107">サイト マップは、Web サイト上のページにて、XML 形式の機械可読リストです。</span><span class="sxs-lookup"><span data-stu-id="61b86-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="61b86-108">検索エンジンによって使用されることを目的としており、サイトからの優れた検索結果を提供することができます。</span><span class="sxs-lookup"><span data-stu-id="61b86-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="61b86-109">サイトマップは、手動により検索エンジンで取得するか、または robots.txt ファイルに発行されます。</span><span class="sxs-lookup"><span data-stu-id="61b86-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="61b86-110">Dynamics 365 Commerce はサイトマップの自動生成をサポートします。</span><span class="sxs-lookup"><span data-stu-id="61b86-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="61b86-111">ページが発行および未発行の場合は、サイト マップが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="61b86-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="61b86-112">サイト マップの生成を有効化</span><span class="sxs-lookup"><span data-stu-id="61b86-112">Turn on site map generation</span></span>

1. <span data-ttu-id="61b86-113">オーサリング ツールにログインします。</span><span class="sxs-lookup"><span data-stu-id="61b86-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="61b86-114">**サイト** で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="61b86-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="61b86-115">左のナビゲーション ウィンドウで、**サイト管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61b86-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="61b86-116">**サイト マップの有効化** オプションがオンになっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="61b86-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="61b86-117">メタデータのページ</span><span class="sxs-lookup"><span data-stu-id="61b86-117">Page metadata</span></span>

<span data-ttu-id="61b86-118">Dynamics 365 Commerce では、個々のページの SEO メタデータを管理できます。</span><span class="sxs-lookup"><span data-stu-id="61b86-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="61b86-119">ページ コンテナーの **SEO プロパティ** セクションで、この情報を表示および変更できます。</span><span class="sxs-lookup"><span data-stu-id="61b86-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="61b86-120">次の SEO メタデータのプロパティがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="61b86-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="61b86-121">肩書き</span><span class="sxs-lookup"><span data-stu-id="61b86-121">Title</span></span>
- <span data-ttu-id="61b86-122">説明</span><span class="sxs-lookup"><span data-stu-id="61b86-122">Description</span></span>
- <span data-ttu-id="61b86-123">SEO キーワード</span><span class="sxs-lookup"><span data-stu-id="61b86-123">SEO keywords</span></span>
- <span data-ttu-id="61b86-124">Aria ラベル</span><span class="sxs-lookup"><span data-stu-id="61b86-124">Aria labels</span></span>
- <span data-ttu-id="61b86-125">noindex</span><span class="sxs-lookup"><span data-stu-id="61b86-125">noindex</span></span>
- <span data-ttu-id="61b86-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="61b86-126">nofollow</span></span>
- <span data-ttu-id="61b86-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="61b86-127">noarchive</span></span>
- <span data-ttu-id="61b86-128">nocache</span><span class="sxs-lookup"><span data-stu-id="61b86-128">nocache</span></span>
- <span data-ttu-id="61b86-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="61b86-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="61b86-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="61b86-130">nosnippet</span></span>
- <span data-ttu-id="61b86-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="61b86-131">noImageIndex</span></span>
- <span data-ttu-id="61b86-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="61b86-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="61b86-133">ページ メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="61b86-133">Modify page metadata</span></span>

<span data-ttu-id="61b86-134">ページ メタデータを変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="61b86-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="61b86-135">**サイト** で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="61b86-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="61b86-136">左のナビゲーション ウィンドウで、**ページ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61b86-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="61b86-137">ホーム ページを選択して、ページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="61b86-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="61b86-138">コマンド バーで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61b86-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="61b86-139">右側のプロパティ ウィンドウで、**既定のメタタグ** を展開します。</span><span class="sxs-lookup"><span data-stu-id="61b86-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="61b86-140">新しいメタタグを追加するには、**追加** を選択して、フィールドにタグを入力します。</span><span class="sxs-lookup"><span data-stu-id="61b86-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="61b86-141">既存のメタタグを削除するには、その右側にあるごみ箱記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="61b86-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="61b86-142">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61b86-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="61b86-143">**コメント** フィールドで、**メタタグの更新** と入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61b86-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="61b86-144">**プレビュー** を選択して、ページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="61b86-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="61b86-145">完了したら、プレビュー タブを閉じて、作成ツールに戻ります。</span><span class="sxs-lookup"><span data-stu-id="61b86-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="61b86-146">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61b86-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61b86-147">追加リソース</span><span class="sxs-lookup"><span data-stu-id="61b86-147">Additional resources</span></span>

[<span data-ttu-id="61b86-148">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="61b86-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="61b86-149">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="61b86-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="61b86-150">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="61b86-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="61b86-151">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="61b86-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="61b86-152">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="61b86-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="61b86-153">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="61b86-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="61b86-154">ページ コンテンツのアクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="61b86-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="61b86-155">URL のパラメーターに基いて動的な電子商取引ページを作成する</span><span class="sxs-lookup"><span data-stu-id="61b86-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
