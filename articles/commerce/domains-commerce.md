---
title: Dynamics 365 Commerce のドメイン
description: このトピックでは、Microsoft Dynamics 365 Commerce でのドメインの処理方法について説明します。
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: bafa49cc570ddf7e0ff9c3dcb1b6902fb341b790
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225792"
---
# <a name="domains-in-dynamics-365-commerce"></a><span data-ttu-id="74158-103">Dynamics 365 Commerce のドメイン</span><span class="sxs-lookup"><span data-stu-id="74158-103">Domains in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="74158-104">このトピックでは、Microsoft Dynamics 365 Commerce でのドメインの処理方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="74158-104">This topic describes how domains are handled in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="74158-105">ドメインは Web ブラウザーで Dynamics 365 Commerce サイトに移動するために使用される Web アドレスです。</span><span class="sxs-lookup"><span data-stu-id="74158-105">Domains are web addresses used to navigate to Dynamics 365 Commerce sites in a web browser.</span></span> <span data-ttu-id="74158-106">選択したドメイン ネーム サーバー (DNS) プロバイダーを使用して、ドメインの管理を制御します。</span><span class="sxs-lookup"><span data-stu-id="74158-106">You control management of your domain with a chosen Domain Name Server (DNS) provider.</span></span> <span data-ttu-id="74158-107">ドメインは、Dynamics 365 Commerce サイト ビルダー全体で参照され、公開時のサイトへのアクセス方法を調整します。</span><span class="sxs-lookup"><span data-stu-id="74158-107">Domains are referenced throughout Dynamics 365 Commerce site builder to coordinate how a site will be accessed when published.</span></span> <span data-ttu-id="74158-108">このトピックでは、Commerce サイトの開発と立ち上げのライフサイクルを通じてドメインがどのように処理および参照されるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="74158-108">This topic reviews how domains are handled and referenced throughout the lifecycle of the Commerce site development and launch.</span></span>

## <a name="provisioning-and-supported-host-names"></a><span data-ttu-id="74158-109">プロビジョニングおよびサポートされているホスト名</span><span class="sxs-lookup"><span data-stu-id="74158-109">Provisioning and supported host names</span></span>

<span data-ttu-id="74158-110">[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) で e コマース環境をプロビジョニングする場合 、e コマース プロビジョニング画面の **サポートされているホスト名** ボックスを使用して、展開された Commerce 環境に関連付けられるドメインを入力します。</span><span class="sxs-lookup"><span data-stu-id="74158-110">When provisioning an e-commerce environment in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), the **Supported host names** box on the e-commerce provisioning screen is used to enter domains that will be associated with the deployed Commerce environment.</span></span> <span data-ttu-id="74158-111">これらのドメインは、e コマース Web サイトがホストされる顧客向けドメイン ネーム サーバー (DNS) 名になります。</span><span class="sxs-lookup"><span data-stu-id="74158-111">These domains will be the customer-facing Domain Name Server (DNS) names where e-commerce websites will be hosted.</span></span> <span data-ttu-id="74158-112">この段階でドメインを入力しても、ドメインのトラフィックを Dynamics 365 Commerce に振り向けることはありません。</span><span class="sxs-lookup"><span data-stu-id="74158-112">Entering a domain at this stage does not start diverting traffic for the domain to Dynamics 365 Commerce.</span></span> <span data-ttu-id="74158-113">ドメインのトラフィックは、ドメインで Commerce エンドポイントを使用するように DNS CNAME レコードが更新された場合にのみ、Commerce エンドポイントにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="74158-113">Traffic for a domain will only be routed to the Commerce endpoint when the DNS CNAME record is updated to use the Commerce endpoint with the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="74158-114">複数のドメインをセミコロンで区切ることによって、**サポートされているホスト名** ボックスに入力できます。</span><span class="sxs-lookup"><span data-stu-id="74158-114">Multiple domains can be entered into the **Supported host names** box by separating them with semi-colons.</span></span>

<span data-ttu-id="74158-115">次の図は、**サポートされているホスト名** ボックスが強調表示された LCS E コマース プロビジョニング画面を示しています。</span><span class="sxs-lookup"><span data-stu-id="74158-115">The following illustration shows the LCS e-commerce provisioning screen with the **Supported host names** box highlighted.</span></span> 

![**サポートされているホスト名** ボックスが強調表示された LCS E コマース プロビジョニング画面](./media/Domains_ProvisioningeCommerceScreen.png)

<span data-ttu-id="74158-117">プロビジョニングが既に行われている場合は、サービス要求を作成して環境にドメインを追加できます。</span><span class="sxs-lookup"><span data-stu-id="74158-117">You can create a service request to add additional domains to an environment if provisioning has already occurred.</span></span> <span data-ttu-id="74158-118">LCS でサービス要求を作成するには、環境内で **サポート \> サポートの問題** に移動し、**インシデントの送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74158-118">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

## <a name="commerce-generated-urls"></a><span data-ttu-id="74158-119">Commerce 生成の URL</span><span class="sxs-lookup"><span data-stu-id="74158-119">Commerce-generated URLs</span></span>

<span data-ttu-id="74158-120">Dynamics 365 Commerce e コマース環境をプロビジョニングする際、Commerce は環境の作業用アドレスとなる URL を生成します。</span><span class="sxs-lookup"><span data-stu-id="74158-120">When provisioning a Dynamics 365 Commerce e-commerce environment, Commerce will generate a URL that will be the working address for the environment.</span></span> <span data-ttu-id="74158-121">この URL は、環境のプロビジョニング後に、LCS に表示されている e コマース サイトのリンクで参照されます。</span><span class="sxs-lookup"><span data-stu-id="74158-121">This URL is referenced in the e-commerce site link shown in LCS after the environment is provisioned.</span></span> <span data-ttu-id="74158-122">Commerce 生成の URL は、`https://<e-commerce tenant name>.commerce.dynamics.com` の形式で、e コマース テナント名は、Commerce 環境に対して LCS に入力された名前です。</span><span class="sxs-lookup"><span data-stu-id="74158-122">A Commerce-generated URL is in the format `https://<e-commerce tenant name>.commerce.dynamics.com`, where the e-commerce tenant name is the name entered in LCS for the Commerce environment.</span></span>

<span data-ttu-id="74158-123">サンドボックス環境では、実稼働環境サイトのホスト名を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="74158-123">You can use production site host names in a sandbox environment as well.</span></span> <span data-ttu-id="74158-124">このオプションは、サンドボックス環境から実稼働環境にサイトをコピーする場合に最も適しています。</span><span class="sxs-lookup"><span data-stu-id="74158-124">This option is ideal when you will be copying a site from a sandbox environment to production.</span></span>

## <a name="site-setup"></a><span data-ttu-id="74158-125">サイトの設定</span><span class="sxs-lookup"><span data-stu-id="74158-125">Site setup</span></span>

<span data-ttu-id="74158-126">e コマース環境のプロビジョニング後、サイトを作業用 URL に関連付けるように、サイトを Commerce サイト ビルダーで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74158-126">After your e-commerce environment is provisioned, you must set up your site in Commerce site builder to associate your site to the working URL.</span></span>

<span data-ttu-id="74158-127">サイト ビルダーで初めてサイトを設定すると、**サイトの設定** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="74158-127">When you first set up a site in site builder, the **Setup your Site** dialog box will appear.</span></span>

<span data-ttu-id="74158-128">次の図は、サイト ビルダーで初めてサイトにアクセスするときの、"default" という名前のサイトの **サイトの設定** ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="74158-128">The following illustration shows the **Setup your Site** dialog box for a site named "default" when you access the site for the first time in site builder.</span></span>

![**サイトの設定** ダイアログ ボックス](./media/Domains_SetupyoursiteScreen.png)

<span data-ttu-id="74158-130">**ドメインの選択** ボックスを使用すると、LCS でサイトに用意されている、サポートされているホスト名の 1 つをサイト ビルダーでサイトに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="74158-130">The **Select a domain** box allows you to associate one of the supported host names provided for your site in LCS to your site in site builder.</span></span>

<span data-ttu-id="74158-131">**パス** ボックスは空白のままにするか、作業 URL に反映される追加のパス文字列を追加できます。</span><span class="sxs-lookup"><span data-stu-id="74158-131">The **Path** box can be left blank, or an additional path string can be added that will be reflected in your working URL.</span></span> <span data-ttu-id="74158-132">**パス** ボックスを空白のままにすると、Commerce 生成のベース URL が、サイト ビルダーで設定されているサイトに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="74158-132">Leaving the **Path** box blank associates the base Commerce-generated URL with the site being set up in site builder.</span></span> <span data-ttu-id="74158-133">パスは、サイト/ドメインのペアごとに一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="74158-133">Paths must be unique for each site/domain pair.</span></span> <span data-ttu-id="74158-134">選択したサイトおよびドメイン内では、環境内の 1 つのサイトのみが空白のパスを使用するか、一意のパス文字列に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="74158-134">Within the site and domain selected, only one site in the environment can use the blank path or be associated with a unique path string.</span></span> <span data-ttu-id="74158-135">サイトのセットアップ時に **パス** フィールドに追加された文字列は、Web ブラウザーでサイトにアクセスするために使用される Commerce 生成のベース URL のサブパスになります。</span><span class="sxs-lookup"><span data-stu-id="74158-135">Any string added to the **Path** field during site setup will become a subpath of the base Commerce-generated URL used to access the site in a web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="74158-136">パスは、サイト ビルダーの **サイトの設定 \> チャネル** コンフィギュレーション セクションでチャネルを追加するときに、**一致パス** とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="74158-136">The path is also known as the **Match path** when adding a channel in the **Site Settings \> Channels** configuration section of site builder.</span></span>

<span data-ttu-id="74158-137">たとえば、"xyz" という名前の e コマース テナントでサイト ビルダーに "fabrikam" というサイトがあり、空白のパスでサイトを設定した場合、次の Commerce 生成のベース URL に直接アクセスすることによって、Web ブラウザーで公開サイトのコンテンツにアクセスします:</span><span class="sxs-lookup"><span data-stu-id="74158-137">For example, if you have a site in site builder called "fabrikam" in an e-commerce tenant named "xyz," and if you set up the site with a blank path, then you would access the published site content in a web browser by going directly to the base Commerce-generated URL:</span></span>

`https://xyz.commerce.dynamics.com`

<span data-ttu-id="74158-138">また、この同じサイトのセットアップ時に "fabrikam" のパスを追加した場合は、次の URL を使用して、Web ブラウザーで公開サイトのコンテンツにアクセスします:</span><span class="sxs-lookup"><span data-stu-id="74158-138">Alternately, if you had added a path of "fabrikam" during this same site's setup, you would access the published site content in a web browser using the following URL:</span></span>

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a><span data-ttu-id="74158-139">ページと URL</span><span class="sxs-lookup"><span data-stu-id="74158-139">Pages and URLs</span></span>

<span data-ttu-id="74158-140">サイトがパスで設定されると、サイト ビルダーのページに関連付けられているすべての URL が、サイトの作業 URL (Commerce 生成の URL または Commerce 生成の URLとパス) に基づいてビルドされます。</span><span class="sxs-lookup"><span data-stu-id="74158-140">After your site is set up with a path, all URLs associated with pages in site builder will build on the working URL (the Commerce-generated URL, or the Commerce-generated URL plus the path) for the site.</span></span> <span data-ttu-id="74158-141">**新しい URL** ダイアログ ボックスの一覧からページを選択し、そのページの URL パスを入力することによって、サイト ビルダー (**URL /> + 新規**) で新しい URL を作成すると、その URL が選択したページに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="74158-141">Creating a new URL in site builder (**URLS /> +New**) by selecting a page from the list in the **New URL** dialog box and entering the URL path for that page will associate that URL with the selected page.</span></span> <span data-ttu-id="74158-142">URL パス値は、そのページにアクセスするためにサイトの作業 URL に追加され、サイト ビルダーの **URL** ページの URL リストで `./<URL path>` のラベルが付けられます。</span><span class="sxs-lookup"><span data-stu-id="74158-142">The URL path value then appends to the site's working URL to access the page, and is labeled as `./<URL path>` in the URL list of the **URLs** page in site builder.</span></span>

<span data-ttu-id="74158-143">次の図は、URL パスの例が強調表示されたサイト ビルダーの **新しい URL** ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="74158-143">The following illustration shows the **New URL** dialog box in site builder with an example URL path highlighted.</span></span> 

![サイト ビルダーの **新しい URL** ダイアログ ボックス](./media/Domains_PageSetup2a.png)

<span data-ttu-id="74158-145">次の図は、URL の例が一覧で強調表示されたサイト ビルダーの **URL** ページを示しています。</span><span class="sxs-lookup"><span data-stu-id="74158-145">The following illustration shows the **URLs** page in site builder with an example URL highlighted in the list.</span></span>

![ポリシー フローでのユーザー フロー オプションの実行](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a><span data-ttu-id="74158-147">サイト ビルダーのドメイン</span><span class="sxs-lookup"><span data-stu-id="74158-147">Domains in site builder</span></span>

<span data-ttu-id="74158-148">サポートされているホスト名の値は、サイトの設定時にドメインとして関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="74158-148">The supported host names values are available to be associated as a domain when setting up a site.</span></span> <span data-ttu-id="74158-149">サポートされているホスト名の値をドメインとして選択すると、サイト ビルダー全体で参照されている選択されたドメインが表示されます。</span><span class="sxs-lookup"><span data-stu-id="74158-149">When selecting a supported host name value as the domain, you will see the chosen domain referenced throughout site builder.</span></span> <span data-ttu-id="74158-150">このドメインは、Commerce 環境内の参照にすぎず、そのドメインのライブ トラフィックはまだ Dynamics 365 Commerce に転送されません。</span><span class="sxs-lookup"><span data-stu-id="74158-150">This domain is only a reference within the Commerce environment, live traffic for that domain will not yet be forwarded to Dynamics 365 Commerce.</span></span>

<span data-ttu-id="74158-151">サイト ビルダーでサイトを操作するときに、2 つの異なるドメインで 2 つのサイトを設定している場合、**?domain=** 属性を作業 URL に追加して、ブラウザーで公開サイトのコンテンツにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="74158-151">When working with sites in site builder, if you have two sites set up with two different domains, you can append the **?domain=** attribute to your working URL to access the published site content in a browser.</span></span>

<span data-ttu-id="74158-152">たとえば、環境 "xyz" がプロビジョニングされ、サイト ビルダーに 2 つのサイトが作成されて、1 つはドメイン `www.fabrikam.com` で、もう 1 つはドメイン `www.constoso.com` に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="74158-152">For example, environment "xyz" has been provisioned, and two sites have been created and associated in site builder: one with the domain `www.fabrikam.com` and the other with the domain `www.constoso.com`.</span></span> <span data-ttu-id="74158-153">各サイトは空白のパスを使用して設定されました。</span><span class="sxs-lookup"><span data-stu-id="74158-153">Each site was set up using a blank path.</span></span> <span data-ttu-id="74158-154">この 2 つのサイトは、**?domain=** 属性を使用して、次のように Web ブラウザーでアクセスできます:</span><span class="sxs-lookup"><span data-stu-id="74158-154">These two sites could then be accessed in a web browser as follows using the **?domain=** attribute:</span></span>
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

<span data-ttu-id="74158-155">複数のドメインが提供されている環境でドメインのクエリ文字列が指定されていない場合、Commerce は提供された最初のドメインを使用します。</span><span class="sxs-lookup"><span data-stu-id="74158-155">When a domain query string is not given in an environment with multiple domains provided, Commerce uses the first domain you provided.</span></span> <span data-ttu-id="74158-156">たとえば、サイトの設定中に最初にパス "fabrikam" が提供された場合、その URL `https://xyz.commerce.dynamics.com` を使用して、`www.fabrikam.com` の公開サイトのコンテンツ サイトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="74158-156">For example, if the path "fabrikam" was provided first during site setup, the URL `https://xyz.commerce.dynamics.com` could be used to access the published site content site for `www.fabrikam.com`.</span></span>

## <a name="traffic-forwarding-in-production"></a><span data-ttu-id="74158-157">実稼働環境でのトラフィックの転送</span><span class="sxs-lookup"><span data-stu-id="74158-157">Traffic forwarding in production</span></span>

<span data-ttu-id="74158-158">Commerce.dynamics.com エンドポイント自体でドメインのクエリ文字列パラメータを使用して、複数のドメインをシミュレートできます。</span><span class="sxs-lookup"><span data-stu-id="74158-158">You can simulate multiple domains using domain query string parameters on the commerce.dynamics.com endpoint itself.</span></span> <span data-ttu-id="74158-159">ただし、実稼働環境で稼働させる必要がある場合は、カスタム ドメインのトラフィックを `<e-commerce tenant name>.commerce.dynamics.com` エンドポイントに転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74158-159">But when you need to go live in production, you must forward the traffic for your custom domain to the `<e-commerce tenant name>.commerce.dynamics.com` endpoint.</span></span>

<span data-ttu-id="74158-160">`<e-commerce tenant name>.commerce.dynamics.com` エンドポイントは、カスタム ドメイン Secure Sockets Layer (SSL) をサポートしていないため、フロント ドア サービスまたはコンテンツ配信ネットワーク (CDN) を使用してカスタム ドメインを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74158-160">The `<e-commerce tenant name>.commerce.dynamics.com` endpoint does not support custom domain Secure Sockets Layers (SSLs), so you must set up custom domains using a front door service or content delivery network (CDN).</span></span> 

<span data-ttu-id="74158-161">フロント ドア サービスまたは CDN を使用してカスタム ドメインを設定するには、次の 2 つのオプションがあります:</span><span class="sxs-lookup"><span data-stu-id="74158-161">To set up custom domains using a front door service or CDN, you have two options:</span></span>

- <span data-ttu-id="74158-162">Azure Front Door ようなフロント ドア サービスを設定して、フロント エンド トラフィックを処理し、Commerce 環境に接続します。</span><span class="sxs-lookup"><span data-stu-id="74158-162">Set up a front door service like Azure Front Door to handle front-end traffic and connect to your Commerce environment.</span></span> <span data-ttu-id="74158-163">これにより、ドメインと証明書の管理をより詳細に制御し、よりきめ細かなセキュリティ ポリシーを提供できます。</span><span class="sxs-lookup"><span data-stu-id="74158-163">This provides greater control over domain and certificate management and more granular security policies.</span></span>
- <span data-ttu-id="74158-164">Commerce 提供の Azure Front Door インスタンスを使用します。</span><span class="sxs-lookup"><span data-stu-id="74158-164">Use the Commerce-supplied Azure Front Door instance.</span></span> <span data-ttu-id="74158-165">これには、ドメイン検証と実稼動環境ドメインの SSL 証明書を取得するために、Dynamics 365 Commerce チームとの調整が必要です。</span><span class="sxs-lookup"><span data-stu-id="74158-165">This requires coordinating action with the Dynamics 365 Commerce team for domain verification and obtaining SSL certificates for your production domain.</span></span>

<span data-ttu-id="74158-166">CDN サービスを直接設定する方法の詳細については、[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74158-166">For information about how to set up a CDN service directly, see [Add support for a content delivery network (CDN)](add-cdn-support.md).</span></span>

<span data-ttu-id="74158-167">Commerce 提供の Azure Front Door インスタンスを使用するには、Commerce オンボード チームから CDN 設定支援のサービス要求を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74158-167">To use the Commerce-supplied Azure Front Door instance, you must create a service request for CDN setup assistance from the Commerce onboarding team.</span></span> 

- <span data-ttu-id="74158-168">会社名、実稼動環境ドメイン、環境 ID、および実稼動環境の e コマース テナント名を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74158-168">You will need to provide your company name, the production domain, environment ID, and production e-commerce tenant name.</span></span> 
- <span data-ttu-id="74158-169">これが既存のドメイン (現在アクティブなサイトに使用されている) か、新しいドメインであるかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74158-169">You will need to confirm if this is an existing domain (used for a currently active site) or a new domain.</span></span> 
- <span data-ttu-id="74158-170">新しいドメインの場合、ドメイン検証と SSL 証明書は 1 つのステップで実行できます。</span><span class="sxs-lookup"><span data-stu-id="74158-170">For a new domain, the domain verification and SSL certificate can be achieved in a single step.</span></span> 
- <span data-ttu-id="74158-171">既存の Web サイトに提供するドメインの場合、ドメイン検証と SSL 証明書を確立するために必要ないくつかのステップ プロセスがあります。</span><span class="sxs-lookup"><span data-stu-id="74158-171">For a domain serving an existing website, there is a multistep process required to establish the domain verification and SSL certificate.</span></span> <span data-ttu-id="74158-172">このプロセスには、複数の連続したステップが含まれているため、ドメインが稼働するために 7 営業日のサービス レベル契約 (SLA) があります。</span><span class="sxs-lookup"><span data-stu-id="74158-172">This process has a 7-working-day service level agreement (SLA) for a domain to go live, because it includes multiple sequential steps.</span></span>

<span data-ttu-id="74158-173">LCS でサービス要求を作成するには、環境内で **サポート \> サポートの問題** に移動し、**インシデントの送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74158-173">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

> [!NOTE]
> <span data-ttu-id="74158-174">SSL を使用したカスタム ドメインは、実稼働環境でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="74158-174">Custom domains with SSL are only supported on production environments.</span></span> <span data-ttu-id="74158-175">サンドボックスやユーザー受け入れテスト (UAT) などの非実稼働環境の場合、Commerce 生成の URL を使用して、Web ブラウザーで公開されたコンテンツにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="74158-175">For non-production environments such as sandbox and user acceptance testing (UAT), use the Commerce-generated URL to access published content in a web browser.</span></span>

## <a name="ssl-certificate-process"></a><span data-ttu-id="74158-176">SSL 証明書プロセス</span><span class="sxs-lookup"><span data-stu-id="74158-176">SSL certificate process</span></span>

<span data-ttu-id="74158-177">サービス要求が提出されると、Commerce チームは次の手順をユーザーと調整します。</span><span class="sxs-lookup"><span data-stu-id="74158-177">When a service request is filed, the Commerce team will coordinate the following steps with you.</span></span>

<span data-ttu-id="74158-178">新しいドメインの場合:</span><span class="sxs-lookup"><span data-stu-id="74158-178">For new domains:</span></span>
- <span data-ttu-id="74158-179">Commerce チームは Azure Front Door インスタンス (Commerce ホスト) を設定します。</span><span class="sxs-lookup"><span data-stu-id="74158-179">The Commerce team will set up the Azure Front Door instance (Commerce-hosted).</span></span>
- <span data-ttu-id="74158-180">その後、Commerce チームは、カスタム ドメインをポイントする CNAME レコードを提供します。</span><span class="sxs-lookup"><span data-stu-id="74158-180">The Commerce team will then provide the CNAME record to point your custom domain.</span></span>
- <span data-ttu-id="74158-181">CNAME レコードが更新されると、Commerce ホストの Azure Front Door インスタンスは、ドメインの所有権を確認して SSL 証明書を取得できるようになります。</span><span class="sxs-lookup"><span data-stu-id="74158-181">After the CNAME record is updated, the Commerce-hosted Azure Front Door instance will be able to verify the domain ownership and get the SSL certificate.</span></span>

<span data-ttu-id="74158-182">既存/アクティブ ドメインの場合:</span><span class="sxs-lookup"><span data-stu-id="74158-182">For existing/active domains:</span></span>
- <span data-ttu-id="74158-183">Commerce チームは、ドメイン DNS プロバイダーに提供する `afdverify.<custom-domain>` CNAME レコードを追加するように指示します。</span><span class="sxs-lookup"><span data-stu-id="74158-183">The Commerce team will instruct you to add an `afdverify.<custom-domain>` CNAME record to provide to your domain DNS provider.</span></span>
- <span data-ttu-id="74158-184">完了すると、Commerce チームは、ドメインを Azure Front Door インスタンスに追加し、ドメインの DNS に追加する追加の DNS TXT レコードを提供します。</span><span class="sxs-lookup"><span data-stu-id="74158-184">When complete, the Commerce team will add the domain to the Azure Front Door instance and provide additional DNS TXT records to be added to the DNS for the domain.</span></span>
- <span data-ttu-id="74158-185">TXT レコードが完了すると、Commerce チームは、SSL 証明書を設定するドメインに対して Azure Front Door の更新を完了します。</span><span class="sxs-lookup"><span data-stu-id="74158-185">After the TXT records are completed, the Commerce team will complete the Azure Front Door updates for the domain that will set up the SSL certificate.</span></span>

## <a name="apex-domains"></a><span data-ttu-id="74158-186">Apex ドメイン</span><span class="sxs-lookup"><span data-stu-id="74158-186">Apex domains</span></span>

<span data-ttu-id="74158-187">Commerce 提供の Azure Front Door インスタンスは、apex ドメイン (サブドメインを含まないルート ドメイン) をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="74158-187">The Commerce-supplied Azure Front Door instance does not support apex domains (root domains that do not contain subdomains).</span></span> <span data-ttu-id="74158-188">Apex ドメインは解決するために IP アドレスを必要とし、Commerce Azure Front Door インスタンスは仮想エンドポイントでのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="74158-188">Apex domains require an IP address to resolve, and the Commerce Azure Front Door instance exists with virtual endpoints only.</span></span> <span data-ttu-id="74158-189">Apex ドメインを使用するには、次の 2 つのオプションがあります:</span><span class="sxs-lookup"><span data-stu-id="74158-189">To use an apex domain, you have two options:</span></span>

- <span data-ttu-id="74158-190">**オプション 1** - DNS プロバイダーを使用して、apex ドメインを "www" ドメインにリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="74158-190">**Option 1** - Use your DNS provider to redirect the apex domain to a "www" domain.</span></span> <span data-ttu-id="74158-191">たとえば、fabrikam.com は `www.fabrikam.com` にリダイレクトし、`www.fabrikam.com` は、Commerce ホストの Azure Front Door インスタンスをポイントする CNAME レコードです。</span><span class="sxs-lookup"><span data-stu-id="74158-191">For example, fabrikam.com redirects to `www.fabrikam.com` where `www.fabrikam.com` is the CNAME record that points to the Commerce-hosted Azure Front Door instance.</span></span>

- <span data-ttu-id="74158-192">**オプション 2** - ご自分で CDN/フロント ドア インスタンスを設定して、apex ドメインをホストします。</span><span class="sxs-lookup"><span data-stu-id="74158-192">**Option 2** - Set up a CDN/front door instance on your own to host the apex domain.</span></span>

> [!NOTE]
> <span data-ttu-id="74158-193">Azure Front Door を使用している場合は、同じサブスクリプションで Azure DNS も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74158-193">If you are using Azure Front Door, you must also set up an Azure DNS in the same subscription.</span></span> <span data-ttu-id="74158-194">Azure DNS でホストされている apex ドメインは、Azure Front Door をエイリアス レコードとしてポイントできます。</span><span class="sxs-lookup"><span data-stu-id="74158-194">The apex domain hosted on Azure DNS can point to your Azure Front Door as an alias record.</span></span> <span data-ttu-id="74158-195">Apex ドメインは常に IP アドレスをポイントする必要があるため、これが唯一の回避策です。</span><span class="sxs-lookup"><span data-stu-id="74158-195">This is the only work around, as apex domains must always point to an IP address.</span></span>

  ## <a name="additional-resources"></a><span data-ttu-id="74158-196">追加リソース</span><span class="sxs-lookup"><span data-stu-id="74158-196">Additional resources</span></span>

  [<span data-ttu-id="74158-197">新しい eコマース テナントのデプロイ</span><span class="sxs-lookup"><span data-stu-id="74158-197">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

  [<span data-ttu-id="74158-198">オンライン ストア チャネルのセットアップ</span><span class="sxs-lookup"><span data-stu-id="74158-198">Set up an online store channel</span></span>](online-stores.md)

  [<span data-ttu-id="74158-199">eコマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="74158-199">Create an e-commerce site</span></span>](create-ecommerce-site.md)

  [<span data-ttu-id="74158-200">オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="74158-200">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

  [<span data-ttu-id="74158-201">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="74158-201">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

  [<span data-ttu-id="74158-202">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="74158-202">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

  [<span data-ttu-id="74158-203">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="74158-203">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

  [<span data-ttu-id="74158-204">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="74158-204">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

  [<span data-ttu-id="74158-205">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="74158-205">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

  [<span data-ttu-id="74158-206">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="74158-206">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

  [<span data-ttu-id="74158-207">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="74158-207">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]