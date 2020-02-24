---
title: SEO メタデータの管理
description: このトピックでは、Microsoft Dynamics 365 Commerce の検索エンジン最適化 (SEO) メタデータを管理する方法について説明します。
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
ms.openlocfilehash: 1e7da7bf5c473746413e92babfa943f546b7724d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003467"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="3bdbd-103">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="3bdbd-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3bdbd-104">このトピックでは、Microsoft Dynamics 365 Commerce の検索エンジン最適化 (SEO) メタデータを管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3bdbd-105">概要</span><span class="sxs-lookup"><span data-stu-id="3bdbd-105">Overview</span></span>

<span data-ttu-id="3bdbd-106">サイトの SEO メタデータは、サイト マップとページ メタデータを使用して管理できます。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="3bdbd-107">サイト マップ</span><span class="sxs-lookup"><span data-stu-id="3bdbd-107">Site maps</span></span>

<span data-ttu-id="3bdbd-108">サイト マップは、Web サイト上のページにて、XML 形式の機械可読リストです。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="3bdbd-109">検索エンジンによって使用されることを目的としており、サイトからの優れた検索結果を提供することができます。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="3bdbd-110">サイトマップは、手動により検索エンジンで取得するか、または robots.txt ファイルに発行されます。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="3bdbd-111">Dynamics 365 Commerce はサイトマップの自動生成をサポートします。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="3bdbd-112">ページが発行および未発行の場合は、サイト マップが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="3bdbd-113">サイト マップの生成を有効化</span><span class="sxs-lookup"><span data-stu-id="3bdbd-113">Turn on site map generation</span></span>

1. <span data-ttu-id="3bdbd-114">オーサリング ツールにログインします。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="3bdbd-115">**サイト**で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="3bdbd-116">左のナビゲーション ウィンドウで、**サイト管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="3bdbd-117">**サイト マップの有効化**オプションがオンになっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="3bdbd-118">メタデータのページ</span><span class="sxs-lookup"><span data-stu-id="3bdbd-118">Page metadata</span></span>

<span data-ttu-id="3bdbd-119">Dynamics 365 Commerce では、個々のページの SEO メタデータを管理できます。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="3bdbd-120">ページ コンテナーの **SEO プロパティ**セクションで、この情報を表示および変更できます。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="3bdbd-121">次の SEO メタデータのプロパティがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="3bdbd-122">肩書き</span><span class="sxs-lookup"><span data-stu-id="3bdbd-122">Title</span></span>
- <span data-ttu-id="3bdbd-123">説明</span><span class="sxs-lookup"><span data-stu-id="3bdbd-123">Description</span></span>
- <span data-ttu-id="3bdbd-124">SEO キーワード</span><span class="sxs-lookup"><span data-stu-id="3bdbd-124">SEO keywords</span></span>
- <span data-ttu-id="3bdbd-125">Aria ラベル</span><span class="sxs-lookup"><span data-stu-id="3bdbd-125">Aria labels</span></span>
- <span data-ttu-id="3bdbd-126">noindex</span><span class="sxs-lookup"><span data-stu-id="3bdbd-126">noindex</span></span>
- <span data-ttu-id="3bdbd-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="3bdbd-127">nofollow</span></span>
- <span data-ttu-id="3bdbd-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="3bdbd-128">noarchive</span></span>
- <span data-ttu-id="3bdbd-129">nocache</span><span class="sxs-lookup"><span data-stu-id="3bdbd-129">nocache</span></span>
- <span data-ttu-id="3bdbd-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="3bdbd-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="3bdbd-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="3bdbd-131">nosnippet</span></span>
- <span data-ttu-id="3bdbd-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="3bdbd-132">noImageIndex</span></span>
- <span data-ttu-id="3bdbd-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="3bdbd-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="3bdbd-134">ページ メタデータの変更</span><span class="sxs-lookup"><span data-stu-id="3bdbd-134">Modify page metadata</span></span>

<span data-ttu-id="3bdbd-135">ページ メタデータを変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="3bdbd-136">**サイト**で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="3bdbd-137">左のナビゲーション ウィンドウで、**ページ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="3bdbd-138">ホーム ページを選択して、ページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="3bdbd-139">アクション ウィンドウで、**チェック アウト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="3bdbd-140">右側のプロパティ ウィンドウで、**既定のメタタグ**を展開します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="3bdbd-141">新しいメタタグを追加するには、**追加**を選択して、フィールドにタグを入力します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="3bdbd-142">既存のメタタグを削除するには、その右側にあるごみ箱記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="3bdbd-143">**保存**を選択してから、**チェックイン**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="3bdbd-144">**コメント**フィールドで、**メタタグの更新**と入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="3bdbd-145">**プレビュー**を選択して、ページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="3bdbd-146">完了したら、プレビュー タブを閉じて、作成ツールに戻ります。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="3bdbd-147">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bdbd-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3bdbd-148">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3bdbd-148">Additional resources</span></span>

[<span data-ttu-id="3bdbd-149">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="3bdbd-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="3bdbd-150">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="3bdbd-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="3bdbd-151">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="3bdbd-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="3bdbd-152">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="3bdbd-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="3bdbd-153">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="3bdbd-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="3bdbd-154">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="3bdbd-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="3bdbd-155">ページ コンテンツ アクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="3bdbd-155">Verify page content accessibility</span></span>](verify-accessibility.md)
