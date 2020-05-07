---
title: 新しいサイト ページの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce に新しいサイト ページを追加する方法について説明します。
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: b0f1e290526c25aa6e6300c65e24044a325bee53
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269961"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="90232-103">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="90232-103">Add a new site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="90232-104">このトピックでは、Microsoft Dynamics 365 Commerce に新しいサイト ページを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="90232-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="90232-105">概要</span><span class="sxs-lookup"><span data-stu-id="90232-105">Overview</span></span>

<span data-ttu-id="90232-106">サイトのテンプレートとフラグメントを作成したら、次はそれらを使用するページの作成を開始します。</span><span class="sxs-lookup"><span data-stu-id="90232-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="90232-107">作業を開始するには、テンプレートまたはレイアウト、ページ名、およびページの URL を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90232-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="90232-108">テンプレートまたはレイアウト</span><span class="sxs-lookup"><span data-stu-id="90232-108">Template or layout</span></span>

<span data-ttu-id="90232-109">新しいページには、テンプレートまたはレイアウトのいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="90232-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="90232-110">詳細については、[テンプレートおよびレイアウト](templates-layouts-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="90232-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="90232-111">ページ名</span><span class="sxs-lookup"><span data-stu-id="90232-111">Page name</span></span>

<span data-ttu-id="90232-112">ページ名は、ページに対して一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="90232-112">The page name must be unique to your page.</span></span> <span data-ttu-id="90232-113">見つけやすく、他の人がページの目的を理解できるように、説明的なものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="90232-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="90232-114">ページ名は後で変更できないので、注意して選択してください。</span><span class="sxs-lookup"><span data-stu-id="90232-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="90232-115">ページ URL</span><span class="sxs-lookup"><span data-stu-id="90232-115">Page URL</span></span>

<span data-ttu-id="90232-116">新しいページの URL を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="90232-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="90232-117">ページを作成するときに、完全な URL を形成するために使用される文字列を入力できます。</span><span class="sxs-lookup"><span data-stu-id="90232-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="90232-118">この文字列は相対 URL または URL スラッグとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="90232-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="90232-119">次に、URL スラッグに基づいて完全な URL が生成され、新しいページが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="90232-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="90232-120">ページを公開する前に URL スラッグを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="90232-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="90232-121">詳細については、[ページ URL の作成](create-page-URL.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="90232-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="90232-122">Dynamics 365 Commerce は、URL とコンテンツを切り離します。</span><span class="sxs-lookup"><span data-stu-id="90232-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="90232-123">つまり、URL に関連付けられていないページを作成し、ページに関連付けられていない URL を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="90232-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="90232-124">したがって、URL のコンテンツ スワップを実行でき、ダウンタイムを必要とせず、リダイレクトの管理が容易になります。</span><span class="sxs-lookup"><span data-stu-id="90232-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="90232-125">新しいページの追加</span><span class="sxs-lookup"><span data-stu-id="90232-125">Add a new page</span></span>

<span data-ttu-id="90232-126">サイトに新しいサイト ページを追加するには、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="90232-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="90232-127">**サイト**で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="90232-128">**新しいページ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-128">Select **New Page**.</span></span>
1. <span data-ttu-id="90232-129">**新しいページ** ダイアログ ボックスでテンプレートを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="90232-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="90232-130">**ページ名**フィールドに、ページの名前 (**新しいページ**など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="90232-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="90232-131">**URL** フィールドに、URL を完了するための文字列 (URL スラグ) を入力します (**mynewpage** など)。</span><span class="sxs-lookup"><span data-stu-id="90232-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="90232-132">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-132">Select **OK**.</span></span> <span data-ttu-id="90232-133">ページ エディターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="90232-133">The page editor appears.</span></span> <span data-ttu-id="90232-134">選択したテンプレートに基づいて、ヘッダーとフッターがページに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="90232-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="90232-135">ページ アウトラインで**メイン** スロットを選択し、省略記号ボタン (**...**) を選択してから、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="90232-136">**コンテナー** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="90232-137">**流動的なコンテナー**の省略ボタンを選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="90232-138">**コンテンツ リッチ ブロック**を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="90232-139">**コンテンツ リッチ ブロック**を選択してから省略ボタンを選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="90232-140">**コンテンツ リッチ ブロック項目**を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="90232-141">右側のプロパティ ウィンドウで、**段落**を選択し、フィールドに**テスト テキスト**を入力します。</span><span class="sxs-lookup"><span data-stu-id="90232-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="90232-142">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="90232-143">**コメント** フィールドで、**追加済の新しいページ**と入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="90232-144">**プレビュー**を選択して、ページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="90232-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="90232-145">完了したら、プレビュー タブを閉じて、作成ツールに戻ります。</span><span class="sxs-lookup"><span data-stu-id="90232-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="90232-146">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-146">Select **Publish**.</span></span>
1. <span data-ttu-id="90232-147">ナビゲーション パス (階層リンク) で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="90232-148">左のナビゲーション ウィンドウで、**URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="90232-149">一覧で URL (**mynewpage**) を検索し、選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="90232-150">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90232-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90232-151">追加リソース</span><span class="sxs-lookup"><span data-stu-id="90232-151">Additional resources</span></span>

[<span data-ttu-id="90232-152">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="90232-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="90232-153">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="90232-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="90232-154">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="90232-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="90232-155">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="90232-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="90232-156">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="90232-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="90232-157">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="90232-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="90232-158">ページ コンテンツ アクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="90232-158">Verify page content accessibility</span></span>](verify-accessibility.md)
