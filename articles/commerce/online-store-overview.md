---
title: 電子商取引サイトの概要
description: このトピックでは、Microsoft Dynamics 365 Commerce における電子商取引サイトのサポートの概要について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ae220e98acbda99255beefea598d973dbaa22368
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997550"
---
# <a name="e-commerce-site-overview"></a><span data-ttu-id="c7893-103">eコマース サイトの概要</span><span class="sxs-lookup"><span data-stu-id="c7893-103">E-commerce site overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c7893-104">このトピックでは、Microsoft Dynamics 365 Commerce における電子商取引サイトのサポートの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="c7893-104">This topic provides an overview of the support for e-commerce sites in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="c7893-105">これには、Dynamics 365 Commerce で電子商取引オンライン ストアが初期化および管理される方法に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7893-105">It includes information about how e-commerce online stores are initialized and managed in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c7893-106">また、オンラインストア、および電子商取引サイトの設定と構成の方法に関する詳細情報へのリンクも提供します。</span><span class="sxs-lookup"><span data-stu-id="c7893-106">It also provides links to more information about online stores, and about how to set up and configure an e-commerce site.</span></span> <span data-ttu-id="c7893-107">このトピックでは、多くの基本的な概念について説明しますが、生産的な電子商取引サイトの設定に必要なものすべてについては説明しません。</span><span class="sxs-lookup"><span data-stu-id="c7893-107">Although this topic covers many of the basics, it doesn't cover everything that is required to set up a production e-commerce site.</span></span> <span data-ttu-id="c7893-108">詳細なトピックについては、Dynamics 365 Commerce ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7893-108">More advanced topics can be found in the Dynamics 365 Commerce documentation.</span></span>

## <a name="online-store-channel"></a><span data-ttu-id="c7893-109">オンライン ストア チャネル</span><span class="sxs-lookup"><span data-stu-id="c7893-109">Online store channel</span></span>

<span data-ttu-id="c7893-110">Dynamics 365 Commerce で新しいサイトを構築する前に、少なくとも 1 つのオンライン ストア チャネルを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7893-110">Before you can build your site in Dynamics 365 Commerce, at least one online store channel must be set up.</span></span> <span data-ttu-id="c7893-111">詳細については、[オンライン チャンネルの設定](channel-setup-online.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7893-111">For more information, see [Set up an online channel](channel-setup-online.md).</span></span> 

<span data-ttu-id="c7893-112">Dynamics 365 Commerce では、オンライン ストア チャネルを使用して、製品、価格決定、言語、支払方法、出荷方法、補充センターなど、顧客が利用できるオンライン エクスペリエンスの側面を確立します。</span><span class="sxs-lookup"><span data-stu-id="c7893-112">In Dynamics 365 Commerce, you use an online store channel to establish the products, pricing, languages, payment methods, delivery modes, fulfillment centers, and other aspects of the online experience that should be available to your customers.</span></span>

<span data-ttu-id="c7893-113">Dynamics 365 Commerce の使用を開始する前に、設定する必要があるオンライン ストア チャネルは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="c7893-113">Only one online store channel has to be set up before you can get started with Dynamics 365 Commerce.</span></span> <span data-ttu-id="c7893-114">ただし、1 つの電子商取引サイトは、複数のオンライン ストアにオンライン エクスペリエンスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="c7893-114">However, a single e-commerce site can provide the online experience for multiple online stores.</span></span> <span data-ttu-id="c7893-115">たとえば、異なる地理的地域をサポートするように複数のオンライン ストアが設定されている場合、単一の電子商取引ページ セットを使用して、各ストアで定義されている固有のエクスペリエンスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="c7893-115">For example, if multiple online stores are set up to support different geographical regions, a single set of e-commerce pages can be used to provide the unique experiences that are defined by each store.</span></span> <span data-ttu-id="c7893-116">複数のオンライン ストアをサポートするようにサイトを構成する方法の詳細については、[チャンネルとオンライン サイトの関連付け](associate-site-online-store.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7893-116">For more information about how to configure a site to support multiple online stores, see [Associate an online site with a channel](associate-site-online-store.md).</span></span>

<span data-ttu-id="c7893-117">オンライン ストアが設定されると、オンライン ストアフロントとして機能する Dynamics 365 Commerce サイトに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="c7893-117">After an online store is set up, it can be associated with the Dynamics 365 Commerce site that will serve as your online storefront.</span></span> <span data-ttu-id="c7893-118">オンライン ストアとその設定方法の詳細については、[オンライン ストアの設定](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7893-118">For more information about online stores and how to set them up, see [Set up online stores](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores).</span></span>

## <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="c7893-119">新しい eコマース テナントのデプロイ</span><span class="sxs-lookup"><span data-stu-id="c7893-119">Deploy a new e-commerce tenant</span></span>

<span data-ttu-id="c7893-120">電子商取引サイトの初期化中に、ドメイン名の入力を求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c7893-120">During initialization of an e-commerce site, you're prompted for a domain name.</span></span> <span data-ttu-id="c7893-121">Commerce のドメインの詳細については、[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)[Dynamics 365 Commerce のドメイン](domains-commerce.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7893-121">For more information about domains in Commerce, see [Configure your domain name](configure-your-domain-name.md) and [Domains in Dynamics 365 Commerce](domains-commerce.md).</span></span> <span data-ttu-id="c7893-122">[Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) を使用して新しい電子商取引のテナントを配置するには、[新しい電子商取引テナントの配置](deploy-ecommerce-site.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7893-122">To deploy a new e-commerce tenant by using [Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), follow the steps in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="c7893-123">電子商取引のテナントが LCS で設定された後に、Commerce サイト ビルダーへのリンクが提供されます。</span><span class="sxs-lookup"><span data-stu-id="c7893-123">After your e-commerce tenant is set up in LCS, a link to Commerce site builder will be provided.</span></span> <span data-ttu-id="c7893-124">その後、Commerce サイト ビルダーを使用して、電子商取引サイトを初期化および構成することができます。</span><span class="sxs-lookup"><span data-stu-id="c7893-124">You can then use Commerce site builder to initialize and configure your e-commerce sites.</span></span>

## <a name="initialize-your-e-commerce-site"></a><span data-ttu-id="c7893-125">電子商取引サイトの初期化</span><span class="sxs-lookup"><span data-stu-id="c7893-125">Initialize your e-commerce site</span></span>

<span data-ttu-id="c7893-126">LC から Commerce サイト ビルダーを起動すると、**サイト** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c7893-126">When you start Commerce site builder from LCS, the **Sites** page appears.</span></span> <span data-ttu-id="c7893-127">このページには、次の図の例に示すように、**既定** と **fabrikam** の 2 つの事前構成されたサイトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7893-127">This page includes two preconfigured sites, **default** and **fabrikam**, as shown in the example in the following illustration.</span></span>

![Commerce サイト ビルダーのサイト ページ](media/e-commerce-site-01.png)

<span data-ttu-id="c7893-129">これらのサイトのいずれかを選択すると、ドメイン名、既定のオンライン チャンネル、選択したチャンネルでサポートされている言語、およびパスを選択するように求められます。</span><span class="sxs-lookup"><span data-stu-id="c7893-129">When you select one of these sites, you're prompted to select a domain name, a default online store channel, a supported language for the selected channel, and a path.</span></span> <span data-ttu-id="c7893-130">1 つのチャネルだけを使用する場合は、パスを空白のままにしておくことができます。</span><span class="sxs-lookup"><span data-stu-id="c7893-130">If only one channel is used, you can leave the path blank.</span></span> <span data-ttu-id="c7893-131">後で、オンラインの店舗のチャネルまたは言語を Commerce サイト ビルダーで構成できます。</span><span class="sxs-lookup"><span data-stu-id="c7893-131">More online store channels or languages can be configured later in Commerce site builder.</span></span> <span data-ttu-id="c7893-132">追加のチャネルまたは言語ごとに、固有のパスが必要です。</span><span class="sxs-lookup"><span data-stu-id="c7893-132">Each additional channel or language will require a unique path.</span></span> <span data-ttu-id="c7893-133">たとえば、1 つのサイトに関連付けられている 2 つのオンライン チャネルがあり、そのサイトのドメイン名は `www.fabrikam.com` であるとします。</span><span class="sxs-lookup"><span data-stu-id="c7893-133">For example, you have two online channels that are associated with a single site, and the domain name for the site is `www.fabrikam.com`.</span></span> <span data-ttu-id="c7893-134">この場合、1つのチャネルのパスをパスのない既定値 (`https://www.fabrikam.com`) にすることができ、2 番目のチャネルを **site2** などの新しいパスに設定できます。URL は `https://www.fabrikam.com/site2` になります。</span><span class="sxs-lookup"><span data-stu-id="c7893-134">In this case, the path for one channel can be the default value that has no path (`https://www.fabrikam.com`), and the second channel can be set to a new path, such as **site2**, that will have the URL `https://www.fabrikam.com/site2`.</span></span> <span data-ttu-id="c7893-135">次の図は、Commerce サイト ビルダーのサイトの初期化ダイアログ ボックスの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c7893-135">The following illustration shows an example of a site initialization dialog box in Commerce site builder.</span></span>

![Commerce サイト ビルダーのサイトの初期化ダイアログ ボックス](media/e-commerce-site-02.png)

<span data-ttu-id="c7893-137">**サイト** ページには、**新しいサイト** ボタンも含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7893-137">The **Sites** page also includes a **New site** button.</span></span> <span data-ttu-id="c7893-138">このボタンを選択したときに表示されるダイアログ ボックスは、サイトの初期化ダイアログ ボックスに似ていますが、新しいサイトを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c7893-138">The dialog box that appears when you select this button resembles the site initialization dialog box, but it's used to create a new site.</span></span> <span data-ttu-id="c7893-139">新しいサイトは空白になっています。</span><span class="sxs-lookup"><span data-stu-id="c7893-139">New sites are blank.</span></span> <span data-ttu-id="c7893-140">これには、**既定の** サイトと **fabrikam** サイトに用意されている既定のテンプレート、フラグメント、ページ、およびイメージは含まれません。</span><span class="sxs-lookup"><span data-stu-id="c7893-140">They don't include the same default templates, fragments, pages, and images that are provided with the **default** and **fabrikam** sites.</span></span> <span data-ttu-id="c7893-141">ただし、必要に応じて、サポート チケットを開いて、新しい空のサイトに既定のコンテンツのコピーを追加するように要求することができます。</span><span class="sxs-lookup"><span data-stu-id="c7893-141">However, as you require, you can open a support ticket to request that a copy of the default content be added to a new blank site.</span></span> <span data-ttu-id="c7893-142">詳細については、[E コマース サイトの作成](create-ecommerce-site.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7893-142">For more information, see [Create an e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="c7893-143">新しいサイトが初期化されると、Commerce サイト ビルダーの **ホーム** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c7893-143">After a new site is initialized, the Commerce site builder **Home** page appears.</span></span> <span data-ttu-id="c7893-144">このページには、次の図の例に示すように、一般的なアクションとガイダンスのコンテンツへのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7893-144">This page includes links to common actions and guidance content, as shown in the example in the following illustration.</span></span>

![Commerce サイト ビルダーのホーム ページにあるリンク](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a><span data-ttu-id="c7893-146">オンライン ストア チャネルの変更、または電子商取引サイトへのオンライン ストア チャネルの追加</span><span class="sxs-lookup"><span data-stu-id="c7893-146">Modify online store channels or add online store channels to an e-commerce site</span></span>

<span data-ttu-id="c7893-147">電子商取引サイトを作成した後、そのサイトに関連付けられているチャネルを変更するには、[電子商取引サイトをオンライン チャネルに関連付ける](associate-site-online-store.md)の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="c7893-147">After an e-commerce site is created, you can change the channel that it's associated with by following the steps in [Associate an e-commerce site with an online channel](associate-site-online-store.md).</span></span> <span data-ttu-id="c7893-148">次の図の例は、**チャネル** ページ (**サイト設定 \> チャンネル**) でチャンネルの作業単位番号 (OUN) を変更する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c7893-148">The example in the following illustration shows how a channel operating unit number (OUN) can be changed on the **Channels** page (**Site settings \> Channels**).</span></span> <span data-ttu-id="c7893-149">変更が完了したら、**保存して発行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7893-149">After you've finished making a change, be sure to select **Save and publish**.</span></span> <span data-ttu-id="c7893-150">これにより、変更が確実に発行されます。</span><span class="sxs-lookup"><span data-stu-id="c7893-150">In this way, you ensure that the change is published.</span></span>

![Commerce サイト ビルダーのチャネル ページ](media/e-commerce-site-04.png)

<span data-ttu-id="c7893-152">新しいチャネルを追加するには、**チャンネルの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7893-152">You can add new channels by selecting **Add a channel**.</span></span> <span data-ttu-id="c7893-153">チャネルに新しい言語を追加するには、チャネルを選択し、表示されるチャネル ダイアログ ボックスで **ロケールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7893-153">To add new languages to a channel, select the channel, and then select **Add a locale** in the channel dialog box that appears.</span></span> <span data-ttu-id="c7893-154">ダイアログ ボックスにロケールを表示するには、あらかじめロケールを設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7893-154">Before locales can appear in the dialog box, they must be preconfigured for the online store channel in Commerce headquarters.</span></span>

![Commerce サイト ビルダーのチャネル ダイアログ ボックス](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a><span data-ttu-id="c7893-156">Azure B2C テナントの設定</span><span class="sxs-lookup"><span data-stu-id="c7893-156">Set up an Azure B2C tenant</span></span>

<span data-ttu-id="c7893-157">Dynamics 365 Commerce は Azure Active Directory (Azure AD) 企業と顧客間 (B2C) を使用して、ユーザーの資格情報と認証フローをサポートします。</span><span class="sxs-lookup"><span data-stu-id="c7893-157">Dynamics 365 Commerce uses Azure Active Directory (Azure AD) business-to-consumer (B2C) to support user credential and authentication flows.</span></span> <span data-ttu-id="c7893-158">Azure B2C テナントの設定方法の詳細については、[Commerce での B2C テナントの設定](set-up-b2c-tenant.md)、[ユーザーのサインインに対するカスタム ページの設定](custom-pages-user-logins.md)、[Commerce 環境での複数の B2C テナントのコンフィギュレーション](configure-multi-b2c-tenants.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7893-158">For information about how to set up your Azure B2C tenant, see [Set up a B2C tenant in Commerce](set-up-b2c-tenant.md), [Set up custom pages for user sign-ins](custom-pages-user-logins.md), and [Configure multiple B2C tenants in a Commerce environment](configure-multi-b2c-tenants.md).</span></span>

## <a name="overview-of-the-default-site-pages"></a><span data-ttu-id="c7893-159">既定のサイト ページの概要</span><span class="sxs-lookup"><span data-stu-id="c7893-159">Overview of the default site pages</span></span>

<span data-ttu-id="c7893-160">**既定の** サイトと **fabrikam** のサイトには、開始するのに役立つコンフィギュレーション済みテンプレート、フラグメント、およびページが用意されています。</span><span class="sxs-lookup"><span data-stu-id="c7893-160">The **default** and **fabrikam** sites include preconfigured templates, fragments, and pages to help you get started.</span></span> <span data-ttu-id="c7893-161">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7893-161">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c7893-162">ホーム ページの概要</span><span class="sxs-lookup"><span data-stu-id="c7893-162">Home page overview</span></span>](quick-tour-home-page.md)
- [<span data-ttu-id="c7893-163">製品詳細ページの概要</span><span class="sxs-lookup"><span data-stu-id="c7893-163">Product details page overview</span></span>](quick-tour-pdp.md)
- [<span data-ttu-id="c7893-164">買い物カゴとチェック アウト ページの概要</span><span class="sxs-lookup"><span data-stu-id="c7893-164">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)
- [<span data-ttu-id="c7893-165">アカウント管理ページの概要</span><span class="sxs-lookup"><span data-stu-id="c7893-165">Account management pages overview</span></span>](quick-tour-account-management.md)

## <a name="manage-site-settings"></a><span data-ttu-id="c7893-166">サイト設定の管理</span><span class="sxs-lookup"><span data-stu-id="c7893-166">Manage site settings</span></span>

<span data-ttu-id="c7893-167">サイト設定を管理する方法については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7893-167">For information about how to manage your site settings, see the following topics:</span></span>

- [<span data-ttu-id="c7893-168">E コマース ユーザーとロールの管理</span><span class="sxs-lookup"><span data-stu-id="c7893-168">Manage e-commerce users and roles</span></span>](manage-ecommerce-users-roles.md)
- [<span data-ttu-id="c7893-169">サイトにおける検索エンジンの最適化 (SEO) の考慮事項</span><span class="sxs-lookup"><span data-stu-id="c7893-169">Search engine optimization (SEO) considerations for your site</span></span>](/search-engine-optimization-considerations.md)
- [<span data-ttu-id="c7893-170">コンテンツ セキュリティ ポリシー (CSP) の管理</span><span class="sxs-lookup"><span data-stu-id="c7893-170">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
- [<span data-ttu-id="c7893-171">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="c7893-171">Select a site theme</span></span>](select-site-theme.md)

## <a name="manage-site-content"></a><span data-ttu-id="c7893-172">サイト コンテンツの管理</span><span class="sxs-lookup"><span data-stu-id="c7893-172">Manage site content</span></span>

<span data-ttu-id="c7893-173">サイトのコンテンツを管理する方法については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7893-173">For information about how to manage site content, see the following topics:</span></span>

- [<span data-ttu-id="c7893-174">ページ モデルの用語集</span><span class="sxs-lookup"><span data-stu-id="c7893-174">Page model glossary</span></span>](page-elements-overview.md)
- [<span data-ttu-id="c7893-175">ドキュメントの状態とライフサイクル</span><span class="sxs-lookup"><span data-stu-id="c7893-175">Document states and lifecycle</span></span>](document-states-overview.md)
- [<span data-ttu-id="c7893-176">テンプレートとレイアウト</span><span class="sxs-lookup"><span data-stu-id="c7893-176">Templates and layout</span></span>](templates-layouts-overview.md)
- [<span data-ttu-id="c7893-177">フラグメントで動作</span><span class="sxs-lookup"><span data-stu-id="c7893-177">Work with fragments</span></span>](work-with-fragments.md)
- [<span data-ttu-id="c7893-178">モジュールで動作</span><span class="sxs-lookup"><span data-stu-id="c7893-178">Work with modules</span></span>](work-with-modules.md)
- [<span data-ttu-id="c7893-179">デジタル資産管理の概要</span><span class="sxs-lookup"><span data-stu-id="c7893-179">Digital asset management overview</span></span>](dam-overview.md)
- [<span data-ttu-id="c7893-180">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="c7893-180">Module library overview</span></span>](starter-kit-overview.md)

## <a name="additional-resources"></a><span data-ttu-id="c7893-181">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c7893-181">Additional resources</span></span>

[<span data-ttu-id="c7893-182">eコマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="c7893-182">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="c7893-183">新しい E コマース サイトの配置</span><span class="sxs-lookup"><span data-stu-id="c7893-183">Deploy a new e-commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="c7893-184">チャンネルとオンライン サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="c7893-184">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="c7893-185">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c7893-185">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="c7893-186">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="c7893-186">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="c7893-187">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="c7893-187">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="c7893-188">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="c7893-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
