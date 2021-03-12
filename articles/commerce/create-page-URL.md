---
title: ページ URL の作成
description: このトピックでは、サイトにページ URL を作成するための基本的な概念と手順について説明します。
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 062a49df93e442dbe402ac9a78244c966958aaa2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965256"
---
# <a name="create-a-page-url"></a><span data-ttu-id="ecf22-103">ページ URL の作成</span><span class="sxs-lookup"><span data-stu-id="ecf22-103">Create a page URL</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ecf22-104">このトピックでは、サイトにページ URL を作成するための基本的な概念と手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

## <a name="overview"></a><span data-ttu-id="ecf22-105">概要</span><span class="sxs-lookup"><span data-stu-id="ecf22-105">Overview</span></span>

<span data-ttu-id="ecf22-106">サイト上のページを指す URL の全体または絶対 URL は、個別のパーツで構成されます。</span><span class="sxs-lookup"><span data-stu-id="ecf22-106">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="ecf22-107">たとえば、URL `https://www.contoso.com/en-us/contactus` は次の部分から構成されます。</span><span class="sxs-lookup"><span data-stu-id="ecf22-107">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="ecf22-108">`https://www.contoso.com` – HTTP プロトコルとサイトのドメイン。</span><span class="sxs-lookup"><span data-stu-id="ecf22-108">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="ecf22-109">`/en-us` – サイトの言語パス。</span><span class="sxs-lookup"><span data-stu-id="ecf22-109">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="ecf22-110">`/contactus` – **お問い合わせ** ページの相対 URL。</span><span class="sxs-lookup"><span data-stu-id="ecf22-110">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="ecf22-111">相対 URL は URL *スラッグ* とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="ecf22-111">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="ecf22-112">サイトのドメインとオプションの言語パスは、サイトの設定時に確立します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-112">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="ecf22-113">サイトの設定のオンライン ストア ページで、サイトにドメインと言語のパスを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ecf22-113">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="ecf22-114">ページの URL スラグは、サイト作成環境では独立した項目となっています。</span><span class="sxs-lookup"><span data-stu-id="ecf22-114">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="ecf22-115">ページ URLは、URL スラグを表す名前と、サイトまたは外部サイトのページへのポインターの 2 つの部分で構成されます。</span><span class="sxs-lookup"><span data-stu-id="ecf22-115">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="ecf22-116">ページ URLは、サイトまたは外部サイトの別のページへリダイレクトするようにコンフィギュレーションすることもできます。</span><span class="sxs-lookup"><span data-stu-id="ecf22-116">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="ecf22-117">ページ URL の作成</span><span class="sxs-lookup"><span data-stu-id="ecf22-117">Create a page URL</span></span>

<span data-ttu-id="ecf22-118">ページ URL を作成するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="ecf22-118">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="ecf22-119">ページ作成時に自動作成する</span><span class="sxs-lookup"><span data-stu-id="ecf22-119">Automatically, when you create a page</span></span>
- <span data-ttu-id="ecf22-120">**URL** ページから手動で作成する</span><span class="sxs-lookup"><span data-stu-id="ecf22-120">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="ecf22-121">ページ作成時にページ URL を作成する</span><span class="sxs-lookup"><span data-stu-id="ecf22-121">Create a page URL when you create a page</span></span>

<span data-ttu-id="ecf22-122">新しいページを作成するときに **URL** フィールドに名前を指定すると、そのページを指すページ URL が **URL** ページ上に自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ecf22-122">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="ecf22-123">URL とそのリンク先のページを公開すると、サイト ユーザー (顧客) は、その URL に関連付けられているページにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="ecf22-123">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="ecf22-124">リンク先のページを公開せずに URL を発行した場合、サイト ユーザーがページにアクセスしようとすると、404 エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ecf22-124">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="ecf22-125">ページを指す URL を公開せずに発行した場合、URL を使用してページにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ecf22-125">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="ecf22-126">ページ URL を手動で作成する</span><span class="sxs-lookup"><span data-stu-id="ecf22-126">Manually create a page URL</span></span>

<span data-ttu-id="ecf22-127">新しいページを作成する場合は、ページ URL の指定は必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="ecf22-127">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="ecf22-128">URL フィールドを空白のままにすると、ページはリンクされていない状態で作成されます。</span><span class="sxs-lookup"><span data-stu-id="ecf22-128">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="ecf22-129">この場合、ページが公開されていても、顧客はそれにアクセスすることができません。</span><span class="sxs-lookup"><span data-stu-id="ecf22-129">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="ecf22-130">ページにアクセスできるようにするには、URL を手動で作成してページにリンクする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf22-130">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="ecf22-131">ページ URL を手動で作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-131">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="ecf22-132">**URL** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-132">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="ecf22-133">URL と関連付けるサイトのページを選択します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-133">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="ecf22-134">URL スラッグを入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ecf22-134">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="ecf22-135">この時点で、URL はドラフト状態になっています。</span><span class="sxs-lookup"><span data-stu-id="ecf22-135">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="ecf22-136">サイト ユーザーが関連ページにアクセスできるようにするには、これを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf22-136">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="ecf22-137">ページ URL の更新</span><span class="sxs-lookup"><span data-stu-id="ecf22-137">Update a page URL</span></span>

<span data-ttu-id="ecf22-138">ページ URL のターゲット ページを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-138">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="ecf22-139">**URL** ページで、更新する URL を選択します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-139">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="ecf22-140">右側のプロパティ ウィンドウで、ターゲット ページ フィールドの横にある省略記号ボタン (**...**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-140">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="ecf22-141">ダイアログ ボックスで別のページを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ecf22-141">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="ecf22-142">URL を保存して公開します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-142">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="ecf22-143">ページ URL のリダイレクト</span><span class="sxs-lookup"><span data-stu-id="ecf22-143">Redirect a page URL</span></span>

<span data-ttu-id="ecf22-144">場合によっては、顧客が特定の URL を要求したときに別のページが表示されるようにしたいことがあります。</span><span class="sxs-lookup"><span data-stu-id="ecf22-144">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="ecf22-145">このような場合は、ページ URL が指すページを変更するのが最善で簡単な方法です。</span><span class="sxs-lookup"><span data-stu-id="ecf22-145">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="ecf22-146">ただし、正当な理由で、HTTP 301 または 3023 リダイレクトを使用して、URL に対する要求を別の URL にリダイレクトする場合もあります。</span><span class="sxs-lookup"><span data-stu-id="ecf22-146">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="ecf22-147">URL を別の URL にリダイレクトするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ecf22-147">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="ecf22-148">**URL** ページで、更新する URL を選択します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-148">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="ecf22-149">右のプロパティ ウィンドウで、**リダイレクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-149">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="ecf22-150">リダイレクトのリンク先を選択します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-150">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="ecf22-151">サイトの別のページをポイントするには、**内部 URL** を選択し、省略記号ボタン (**...**) をクリックし、リダイレクト先の URL を選択します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-151">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="ecf22-152">外部サイトのページをポイントするには、**外部 URL** を選択し、そのページの完全な URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-152">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="ecf22-153">必ずプロトコルを含めてください。</span><span class="sxs-lookup"><span data-stu-id="ecf22-153">Be sure to include the protocol.</span></span> <span data-ttu-id="ecf22-154">たとえば、「`https://domain.com/new/page`」を入力します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-154">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="ecf22-155">URL が既に内部 URL にリダイレクトされている場合は、外部 URL を入力する前に **選択解除** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecf22-155">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="ecf22-156">リダイレクト タイプの選択</span><span class="sxs-lookup"><span data-stu-id="ecf22-156">Select a redirect type:</span></span>

    - <span data-ttu-id="ecf22-157">**恒久的リダイレクト (301)** – コンテンツが恒久的に移動して、前の URL に戻らないことがわかっている場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-157">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="ecf22-158">検索エンジンは、リダイレクトする URL の検索エンジン最適化 (SEO) 値を、リダイレクト先の URL に割り当て、レコードを更新して新しい URL を表示します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-158">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="ecf22-159">**一時リダイレクト (302)** – 検索エンジンを更新せずにトラフィックをリダイレクトするには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-159">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="ecf22-160">この方法は、通常、コンテンツを前の URL にすぐに戻す場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ecf22-160">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="ecf22-161">リダイレクトを実装する準備ができたら、URL を保存して公開します。</span><span class="sxs-lookup"><span data-stu-id="ecf22-161">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ecf22-162">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ecf22-162">Additional resources</span></span>

[<span data-ttu-id="ecf22-163">サイト ナビゲーションのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="ecf22-163">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="ecf22-164">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="ecf22-164">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="ecf22-165">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ecf22-165">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="ecf22-166">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="ecf22-166">Add languages to your site</span></span>](add-languages-to-site.md)
