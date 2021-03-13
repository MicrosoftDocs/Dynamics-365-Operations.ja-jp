---
title: URL のパラメーターに基いて動的な電子商取引ページを作成する
description: このトピックでは、URL のパラメーターに基づいて動的なコンテンツを提供できる Microsoft Dynamics 365 Commerce の電子商取引ページの設定方法について説明します。
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e72b738133b396848848d167cace80fe23694334
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098635"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="c5d2e-103">URL のパラメーターに基いて動的な電子商取引ページを作成する</span><span class="sxs-lookup"><span data-stu-id="c5d2e-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c5d2e-104">このトピックでは、URL のパラメーターに基づいて動的なコンテンツを提供できる Microsoft Dynamics 365 Commerce の電子商取引ページの設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="c5d2e-105">電子商取引のページは、URL パスのセグメントに基づいて、異なるコンテンツを提供するよう構成できます。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="c5d2e-106">したがって、このページは動的ページと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="c5d2e-107">セグメントは、ページ内容を取得するパラメーターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="c5d2e-108">たとえば、**ブログ\_ビューアー** という名前のページが作成され、次の URL (`https://fabrikam.com/blog`) に関連付けられるとします。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="c5d2e-109">このページを使用すると、URL パスの最後のセグメントに基づいた異なるコンテンツを表示できます。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="c5d2e-110">たとえば、URL (`https://fabrikam.com/blog/article-1`) の最後のセグメントは **article-1** です。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="c5d2e-111">URL パスのセグメントには、動的なページを上書きするカスタム ページを関連付けすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="c5d2e-112">たとえば、**ブログ\_概要** という名前のページが作成され、次の URL (`https://fabrikam.com/blog/about-this-blog`) に関連付けられるとします。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="c5d2e-113">このURLが要求されている場合、**ブログ\_ビューワー** ページではなく、**/about-this-blog** パラメーターに関連付けられている、**ブログ\_概要** ページが返されます。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="c5d2e-114">動的なページ コンテンツをホスト、取得、表示する機能は、カスタム モジュールを使用して実装されます。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="c5d2e-115">詳細については、[オンライン チャンネルの拡張性](e-commerce-extensibility/overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="c5d2e-116">動的な電子商取引ページを設定する</span><span class="sxs-lookup"><span data-stu-id="c5d2e-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="c5d2e-117">動的な電子商取引のページを設定するには、動的なページを作成し、ベースとなる URL を作成し、動的なページへの経路を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="c5d2e-118">動的なコンテンツを提供するページの作成</span><span class="sxs-lookup"><span data-stu-id="c5d2e-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="c5d2e-119">動的なコンテンツを提供するページを作成するには[新しいサイト ページを追加する ](add-new-page.md)に記載の手順に従います 。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="c5d2e-120">作成するページには、URL パスの最後のセグメントを使用して外部データ ソースからコンテンツを取得するモジュールの実装が必要です。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="c5d2e-121">カスタム モジュール開発の詳細については、[オンライン チャンネルの機能拡張](e-commerce-extensibility/overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="c5d2e-122">動的なページのベース URL を作成する</span><span class="sxs-lookup"><span data-stu-id="c5d2e-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="c5d2e-123">Commerce サイト ビルダーで動的ページのベース URL を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c5d2e-124">**URL** に移動し、**新規 \>新規 URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="c5d2e-125">**新規 URL の作成** ダイアログ ボックスで、**内部 ページ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="c5d2e-126">**URL パス** で、動的ページのルートとして使用するパス を入力します (この例では、**/blog**) です。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="c5d2e-127">その後、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-127">Then select **Next**.</span></span>
1. <span data-ttu-id="c5d2e-128">**ページの選択** ダイアログ ボックスで、動的ページとして作成したページを選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="c5d2e-129">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="c5d2e-130">動的ページへの経路を構成する</span><span class="sxs-lookup"><span data-stu-id="c5d2e-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="c5d2e-131">Commerce サイト ビルダーで動的ページへの経路を構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c5d2e-132">**サイト 設定 \> 拡張機能** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="c5d2e-133">**パラメーター化された URL パス** で、**追加** を選択し、URL の作成時に入力した URL パス (この例では **/blog**) を入力します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="c5d2e-134">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-134">Select **Save and publish**.</span></span>

<span data-ttu-id="c5d2e-135">経路を構成した後は、パラメーター化した URL パスへのすべてのリクエストは、その URL に関連付けられているページが返されます。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="c5d2e-136">追加のセグメントが含まれるリクエストがある場合は、関連するページが返され、その区分をパラメータとして使用してページのコンテンツが取得されます。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="c5d2e-137">たとえば、`https://fabrikam.com/blog/article-1` では **ブログ\_概要** ページが返され、ページのコンテンツは **/article-1** パラメーターを使用して取得されます。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="c5d2e-138">パラメーター化された URL をカスタム ページで上書きする</span><span class="sxs-lookup"><span data-stu-id="c5d2e-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="c5d2e-139">パラメータ化された URL を Commerce サイト ビルダのカスタム ページで上書きするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c5d2e-140">**URL** に移動し、**新規 \>新規 URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="c5d2e-141">**新規 URL の作成** ダイアログ ボックスで、**内部 ページ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="c5d2e-142">**URL パス** で、上書きするセグメントを含むパスを入力します (この例では、**/blog/about-this-blog**)。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="c5d2e-143">その後、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-143">Then select **Next**.</span></span>
1. <span data-ttu-id="c5d2e-144">**ページ の選択** ダイアログ ボックスで、カスタム ページを選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="c5d2e-145">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-145">Select **Publish**.</span></span>
1. <span data-ttu-id="c5d2e-146">カスタム ページがまだ公開されていない場合は、**ページ** に移動し、カスタム ページを選択して、**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="c5d2e-147">カスタム ページが公開された後は、コンテンツをパラメータ化した動的ページではなく、カスタム ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5d2e-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5d2e-148">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c5d2e-148">Additional resources</span></span>

[<span data-ttu-id="c5d2e-149">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="c5d2e-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="c5d2e-150">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="c5d2e-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="c5d2e-151">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="c5d2e-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="c5d2e-152">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="c5d2e-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="c5d2e-153">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="c5d2e-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="c5d2e-154">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="c5d2e-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="c5d2e-155">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="c5d2e-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="c5d2e-156">ページ コンテンツのアクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="c5d2e-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="c5d2e-157">オンライン チャネルの拡張性</span><span class="sxs-lookup"><span data-stu-id="c5d2e-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)
