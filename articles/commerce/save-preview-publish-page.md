---
title: ページの保存、プレビュー、および公開
description: このトピックでは、Microsoft Dynamics 365 Commerce でページの保存、プレビュー、公開を行う方法について説明します。
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
ms.openlocfilehash: f1eff0edeb630628057bd0a90e2dadc4857600f1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791826"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="17a62-103">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="17a62-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17a62-104">このトピックでは、Microsoft Dynamics 365 Commerce でページの保存、プレビュー、公開を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="17a62-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="17a62-105">ページの保存</span><span class="sxs-lookup"><span data-stu-id="17a62-105">Save a page</span></span>

<span data-ttu-id="17a62-106">ページを保存するには、自分自身にチェックアウトして、ページ エディターで開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="17a62-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="17a62-107">ページをチェックするには、コマンド バーで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-107">To check out a page, select **Edit** on the command bar.</span></span> <span data-ttu-id="17a62-108">ページの修正後、ページをすぐに保存して、変更が確実に保存されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17a62-108">After you've finished editing a page, you should immediately save it to ensure that your changes are stored.</span></span>

<span data-ttu-id="17a62-109">ページを保存すると、その変更は自分にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="17a62-109">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="17a62-110">保存操作は主に、ページをチェックインする準備ができていない間に変更を保存することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="17a62-110">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="17a62-111">ページの修正が完了したら、チェックインして他のユーザーに表示されるようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="17a62-111">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="17a62-112">その時点で、ページは修正する必要がある他のユーザーがチェックアウトすることができます。</span><span class="sxs-lookup"><span data-stu-id="17a62-112">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="17a62-113">ページのプレビュー</span><span class="sxs-lookup"><span data-stu-id="17a62-113">Preview a page</span></span>

<span data-ttu-id="17a62-114">作成ツールは、2 種類のプレビュー機能を提供します。ページ エディターの「What You See Is What You Get」 (WYSIWYG) プレビュー ウィンドウであるビジュアル ページ ビルダーと個別のプレビュー ウィンドウです。</span><span class="sxs-lookup"><span data-stu-id="17a62-114">The authoring tool offers two kinds of preview features: visual page builder, which is a "what you see is what you get" (WYSIWYG) preview pane in the page editor, and a separate preview window.</span></span>

<span data-ttu-id="17a62-115">ページ エディターの使用中は、中央のウィンドウに「What You See Is What You Get」 (WYSIWYG) プレビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="17a62-115">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="17a62-116">このプレビューは、ページを保存するたびに自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="17a62-116">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="17a62-117">コマンド バーの **更新** を選択して、手動で更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="17a62-117">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="17a62-118">プレビューでは、サイト ユーザーに表示されるようにページを表示しますが、作成ヘルパーはその上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="17a62-118">The preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="17a62-119">ページの修正が完了したら、プレビューにより顧客に表示される内容を確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="17a62-119">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="17a62-120">ページをプレビューするには、コマンド バーの **プレビュー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-120">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="17a62-121">プレビューは別のブラウザー ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="17a62-121">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="17a62-122">プレビュー ウィンドウのページは、サイト ユーザーに表示されるように表示します。</span><span class="sxs-lookup"><span data-stu-id="17a62-122">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="17a62-123">ウィンドウ サイズを変更して、応答可能なモジュールがすべてのビュー ポートに正しく表示されるようにできます。</span><span class="sxs-lookup"><span data-stu-id="17a62-123">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="17a62-124">公開されていないコンテンツをプレビューするには、認証および正しいアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="17a62-124">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="17a62-125">したがって、プレビューの URL を他のユーザーと共有する場合、そのユーザーはコンテンツにアクセスするための正しいアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="17a62-125">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="17a62-126">ページの公開</span><span class="sxs-lookup"><span data-stu-id="17a62-126">Publish a page</span></span>

<span data-ttu-id="17a62-127">ページの準備ができたら、次の手順は公開し、外部ユーザーがコンテンツを表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="17a62-127">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="17a62-128">ページを公開する前に、まず、コマンドバーの **編集の完了** を選択して、ページをチェックインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17a62-128">Before you can publish a page, you must check it in by selecting **Finish editing** on the command bar.</span></span>

<span data-ttu-id="17a62-129">ページ インスペクターまたはページ エディターのいずれかで、ページの公開および非公開を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="17a62-129">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="17a62-130">ページ インスペクターにより、ページのリストを表示し、一括操作ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="17a62-130">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="17a62-131">ページ エディターを使用し、開かれている 1 つのページだけを公開または非公開にすることができます。</span><span class="sxs-lookup"><span data-stu-id="17a62-131">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="17a62-132">ページ インスペクターから 1 つ以上のページを公開するには、ページを選択し、チェックインされていることを確認してから、コマンド バーの **公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-132">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="17a62-133">ページが公開され、作成ツールで操作に関する通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="17a62-133">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="17a62-134">ページ エディターから 1 つのページを公開する場合、手順は同じです。</span><span class="sxs-lookup"><span data-stu-id="17a62-134">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="17a62-135">ページがページ エディターで開いている間、ページがチェックインされていることを確認してから、コマンド バーの **公開** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17a62-135">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="17a62-136">ページが公開され、操作に関する通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="17a62-136">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="17a62-137">ページを公開する場合、ページのコンテンツのみが公開されます。</span><span class="sxs-lookup"><span data-stu-id="17a62-137">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="17a62-138">URL を関連付けた後にのみ、ユーザーはページに移動して、表示することができます。</span><span class="sxs-lookup"><span data-stu-id="17a62-138">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="17a62-139">URL は個別に公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17a62-139">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17a62-140">ページを公開する前に、ページが参照する画像またはフラグメントを公開しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="17a62-140">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="17a62-141">ホーム ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="17a62-141">Save, preview, and publish a home page</span></span>

<span data-ttu-id="17a62-142">ホーム ページの保存、プレビュー、および公開を行うには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="17a62-142">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="17a62-143">**サイト** で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-143">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="17a62-144">左のナビゲーション ウィンドウで、**ページ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-144">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="17a62-145">ホーム ページを検索、選択して、ページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="17a62-145">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="17a62-146">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-146">Select **Edit**.</span></span>
1. <span data-ttu-id="17a62-147">必要に応じてページを修正します。</span><span class="sxs-lookup"><span data-stu-id="17a62-147">Modify the page as you require.</span></span>
1. <span data-ttu-id="17a62-148">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-148">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="17a62-149">**コメント** フィールドに、行った変更に関するメモを入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-149">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="17a62-150">**プレビュー** を選択して、ページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="17a62-150">Select **Preview** to preview your page.</span></span> <span data-ttu-id="17a62-151">完了したら、プレビュー タブを閉じて、作成ツールに戻ります。</span><span class="sxs-lookup"><span data-stu-id="17a62-151">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="17a62-152">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-152">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="17a62-153">URL の公開</span><span class="sxs-lookup"><span data-stu-id="17a62-153">Publish a URL</span></span>

<span data-ttu-id="17a62-154">URL を公開するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="17a62-154">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="17a62-155">**サイト** で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-155">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="17a62-156">左のナビゲーション ウィンドウで、**URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-156">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="17a62-157">公開する URL を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-157">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="17a62-158">コマンド バーで、**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17a62-158">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17a62-159">追加リソース</span><span class="sxs-lookup"><span data-stu-id="17a62-159">Additional resources</span></span>

[<span data-ttu-id="17a62-160">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="17a62-160">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="17a62-161">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="17a62-161">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="17a62-162">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="17a62-162">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="17a62-163">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="17a62-163">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="17a62-164">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="17a62-164">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="17a62-165">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="17a62-165">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="17a62-166">ページ コンテンツのアクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="17a62-166">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="17a62-167">URL のパラメーターに基いて動的な電子商取引ページを作成する</span><span class="sxs-lookup"><span data-stu-id="17a62-167">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]