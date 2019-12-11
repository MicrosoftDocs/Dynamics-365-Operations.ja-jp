---
title: ページの保存、プレビュー、および公開
description: このトピックでは、Microsoft Dynamics 365 Commerce でページの保存、プレビュー、公開を行う方法について説明します。
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
ms.openlocfilehash: 8c1b82b1b8423c63d442ee581ed0cc8789ee63fd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697891"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="3fa16-103">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="3fa16-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3fa16-104">このトピックでは、Microsoft Dynamics 365 Commerce でページの保存、プレビュー、公開を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="3fa16-105">ページの保存</span><span class="sxs-lookup"><span data-stu-id="3fa16-105">Save a page</span></span>

<span data-ttu-id="3fa16-106">ページを保存するには、自分自身にチェックアウトして、ページ エディターで開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fa16-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="3fa16-107">修正後、ページをすぐに保存して、変更が確実に保存されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fa16-107">You should save a page immediately after you modify it, to help guarantee that your changes are stored.</span></span>

<span data-ttu-id="3fa16-108">ページを保存すると、その変更は自分にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-108">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="3fa16-109">保存操作は主に、ページをチェックインする準備ができていない間に変更を保存することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="3fa16-109">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="3fa16-110">ページの修正が完了したら、チェックインして他のユーザーに表示されるようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3fa16-110">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="3fa16-111">その時点で、ページは修正する必要がある他のユーザーがチェックアウトすることができます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-111">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="3fa16-112">ページのプレビュー</span><span class="sxs-lookup"><span data-stu-id="3fa16-112">Preview a page</span></span>

<span data-ttu-id="3fa16-113">作成ツールは 2 種類のプレビュー機能を提供します。ページ エディターの「What You See Is What You Get」 (WYSIWYG) プレビュー ウィンドウおよび別のプレビュー ウィンドウです。</span><span class="sxs-lookup"><span data-stu-id="3fa16-113">The authoring tool offers two kinds of preview features: a "what you see is what you get" (WYSIWYG) preview pane in the page editor and a separate preview window.</span></span>

<span data-ttu-id="3fa16-114">ページ エディターの使用中は、中央のウィンドウに「What You See Is What You Get」 (WYSIWYG) プレビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-114">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="3fa16-115">このプレビューは、ページを保存するたびに自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-115">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="3fa16-116">コマンド バーの**更新**を選択して、手動で更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-116">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="3fa16-117">WYSIWYG プレビューは、サイト ユーザーに表示されるようにページを表示しますが、作成ヘルパーはその上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-117">The WYSIWYG preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="3fa16-118">ページの修正が完了したら、プレビューにより顧客に表示される内容を確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3fa16-118">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="3fa16-119">ページをプレビューするには、コマンド バーの**プレビュー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-119">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="3fa16-120">プレビューは別のブラウザー ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-120">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="3fa16-121">プレビュー ウィンドウのページは、サイト ユーザーに表示されるように表示します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-121">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="3fa16-122">ウィンドウ サイズを変更して、応答可能なモジュールがすべてのビュー ポートに正しく表示されるようにできます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-122">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="3fa16-123">公開されていないコンテンツをプレビューするには、認証および正しいアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="3fa16-123">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="3fa16-124">したがって、プレビューの URL を他のユーザーと共有する場合、そのユーザーはコンテンツにアクセスするための正しいアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fa16-124">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="3fa16-125">ページの公開</span><span class="sxs-lookup"><span data-stu-id="3fa16-125">Publish a page</span></span>

<span data-ttu-id="3fa16-126">ページの準備ができたら、次の手順は公開し、外部ユーザーがコンテンツを表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="3fa16-126">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="3fa16-127">ページを公開する前に、チェックインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fa16-127">Before you can publish a page, you must check it in.</span></span>

<span data-ttu-id="3fa16-128">ページ インスペクターまたはページ エディターのいずれかで、ページの公開および非公開を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-128">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="3fa16-129">ページ インスペクターにより、ページのリストを表示し、一括操作ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="3fa16-129">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="3fa16-130">ページ エディターを使用し、開かれている 1 つのページだけを公開または非公開にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-130">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="3fa16-131">ページ インスペクターから 1 つ以上のページを公開するには、ページを選択し、チェックインされていることを確認してから、コマンド バーの**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-131">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="3fa16-132">ページが公開され、作成ツールで操作に関する通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="3fa16-132">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="3fa16-133">ページ エディターから 1 つのページを公開する場合、手順は同じです。</span><span class="sxs-lookup"><span data-stu-id="3fa16-133">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="3fa16-134">ページがページ エディターで開いている間、ページがチェックインされていることを確認してから、コマンド バーの**公開**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fa16-134">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="3fa16-135">ページが公開され、操作に関する通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="3fa16-135">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="3fa16-136">ページを公開する場合、ページのコンテンツのみが公開されます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-136">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="3fa16-137">URL を関連付けた後にのみ、ユーザーはページに移動して、表示することができます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-137">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="3fa16-138">URL は個別に公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fa16-138">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3fa16-139">ページを公開する前に、ページが参照する画像またはフラグメントを公開しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fa16-139">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="3fa16-140">ホーム ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="3fa16-140">Save, preview, and publish a home page</span></span>

<span data-ttu-id="3fa16-141">ホーム ページの保存、プレビュー、および公開を行うには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-141">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="3fa16-142">**サイト**で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-142">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="3fa16-143">左のナビゲーション ウィンドウで、**ページ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-143">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="3fa16-144">ホーム ページを検索、選択して、ページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="3fa16-144">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="3fa16-145">**チェックアウト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-145">Select **Check Out**.</span></span>
1. <span data-ttu-id="3fa16-146">必要に応じてページを修正します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-146">Modify the page as you require.</span></span>
1. <span data-ttu-id="3fa16-147">**保存**を選択してから、**チェックイン**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-147">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="3fa16-148">**コメント** フィールドに、行った変更に関するメモを入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-148">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="3fa16-149">**プレビュー**を選択して、ページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="3fa16-149">Select **Preview** to preview your page.</span></span> <span data-ttu-id="3fa16-150">完了したら、プレビュー タブを閉じて、作成ツールに戻ります。</span><span class="sxs-lookup"><span data-stu-id="3fa16-150">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="3fa16-151">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-151">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="3fa16-152">URL の公開</span><span class="sxs-lookup"><span data-stu-id="3fa16-152">Publish a URL</span></span>

<span data-ttu-id="3fa16-153">URL を公開するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3fa16-153">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="3fa16-154">**サイト**で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-154">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="3fa16-155">左のナビゲーション ウィンドウで、**URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-155">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="3fa16-156">公開する URL を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-156">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="3fa16-157">コマンド バーで、**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fa16-157">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3fa16-158">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3fa16-158">Additional resources</span></span>

[<span data-ttu-id="3fa16-159">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="3fa16-159">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="3fa16-160">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="3fa16-160">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="3fa16-161">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="3fa16-161">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="3fa16-162">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="3fa16-162">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="3fa16-163">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="3fa16-163">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="3fa16-164">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="3fa16-164">Enrich a category landing page</span></span>](enrich-category-page.md)

