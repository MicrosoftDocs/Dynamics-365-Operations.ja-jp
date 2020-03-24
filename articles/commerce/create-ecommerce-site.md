---
title: E コマース サイトの作成
description: このトピックでは、Dynamics 365 Commerce サイト ビルダーで 新しい E コマース サイトを作成するために必要な手順と情報について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096777"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="a6a5d-103">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="a6a5d-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a6a5d-104">このトピックでは、Dynamics 365 Commerce サイト ビルダーで 新しい E コマース サイトを作成するために必要な手順と情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="a6a5d-105">E コマース サイトの開発を開始する前には、最初にサイト ビルダーで新しいサイトを開設する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="a6a5d-106">E コマース サイトの開発を開始するには、最初にサイト作成環境で新しいサイトを開設する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="a6a5d-107">新しいサイトを作成する前に、少なくとも 1 つのオンライン ストアをコマースで作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="a6a5d-108">サイトの設定</span><span class="sxs-lookup"><span data-stu-id="a6a5d-108">Set up your site</span></span>

<span data-ttu-id="a6a5d-109">サイトを設定するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="a6a5d-110">サイト ビルダーの環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-110">Open the site builder environment.</span></span> <span data-ttu-id="a6a5d-111">コマースの環境機能ページには、Microsoft Lifecycle Services (LCS) のサイト ビルダーへのリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="a6a5d-112">サイト作成環境のホームページで、**新しいサイト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="a6a5d-113">**新しいサイト** ダイアログ ボックスで、次の情報を入力してください。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="a6a5d-114">フィールド</span><span class="sxs-lookup"><span data-stu-id="a6a5d-114">Field</span></span>                               | <span data-ttu-id="a6a5d-115">説明</span><span class="sxs-lookup"><span data-stu-id="a6a5d-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="a6a5d-116">サイト名</span><span class="sxs-lookup"><span data-stu-id="a6a5d-116">Site name</span></span>                           | <span data-ttu-id="a6a5d-117">サイト作成環境で、サイトに使用する表示名を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="a6a5d-118">この名前は、作成環境でのみ表示され、顧客には表示されません。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="a6a5d-119">サイト管理者のセキュリティ グループ</span><span class="sxs-lookup"><span data-stu-id="a6a5d-119">Site administrator's security group</span></span> | <span data-ttu-id="a6a5d-120">このサイトで管理者ロールを持つユーザーを管理する Microsoft Azure Active Directory (Azure AD) セキュリティ グループを指定します。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="a6a5d-121">既定のチャネル (作業単位番号)</span><span class="sxs-lookup"><span data-stu-id="a6a5d-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="a6a5d-122">このサイトが Web ストア フロントとして使用されるオンライン ストアを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="a6a5d-123">E コマース サイトで複数のオンライン ストアをサポートする場合は、サイトを設定した後で、**サイトの設定**でストアをサイトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="a6a5d-124">既定の言語</span><span class="sxs-lookup"><span data-stu-id="a6a5d-124">Default language</span></span>                            | <span data-ttu-id="a6a5d-125">このオンライン ストアおよびマーケットの既定の言語を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="a6a5d-126">オンライン ストアは複数の言語をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-126">An online store can support multiple languages.</span></span> <span data-ttu-id="a6a5d-127">このオンライン ストアまたは別のオンライン ストアに対して、複数の言語をサポートする場合は、サイトを設定した後に、**サイトの設定**で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="a6a5d-128">ドメイン</span><span class="sxs-lookup"><span data-stu-id="a6a5d-128">Domain</span></span>                              | <span data-ttu-id="a6a5d-129">このオンライン ストアでドメインとして使用されるドメイン名を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="a6a5d-130">LCS でドメインをコンフィグレーションしていない場合は、このフィールドを空白のままにしておくことができます。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="a6a5d-131">ドメインを LCS でコンフィグレーションしたら、**サイトの設定**でそのドメインをオンライン ストアに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="a6a5d-132">パス</span><span class="sxs-lookup"><span data-stu-id="a6a5d-132">Path</span></span>                              | <span data-ttu-id="a6a5d-133">サイトが、特定のドメイン名に対して複数の言語をサポートしている場合は、パス フィールドを使用して、そのドメインと言語の組み合わせに固有のサイト URL を作成します。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="a6a5d-134">**既定の言語**フィールドに指定した言語のみ、このドメインに対してサポートされる場合、またはサイトを他の言語にローカライズした後も、その言語を既定の言語として使用する場合は、このフィールドを空白のままにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="a6a5d-135">サイトが作成されると、**製品**タブを選択することにより、そのサイトがオンライン ストアに関連付けられていることを確認できます。そこでは、オンライン ストアに割り当てられた製品の品揃えが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="a6a5d-136">ページの左上にあるドロップダウン メニューを使用して、割り当てられた製品にカテゴリ別にアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a6a5d-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6a5d-137">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a6a5d-137">Additional resources</span></span>

[<span data-ttu-id="a6a5d-138">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a6a5d-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a6a5d-139">新しい E コマース サイトの配置</span><span class="sxs-lookup"><span data-stu-id="a6a5d-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a6a5d-140">オンライン ストア チャネルのセットアップ</span><span class="sxs-lookup"><span data-stu-id="a6a5d-140">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="a6a5d-141">チャンネルとオンライン サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="a6a5d-141">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a6a5d-142">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="a6a5d-142">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a6a5d-143">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="a6a5d-143">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a6a5d-144">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="a6a5d-144">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a6a5d-145">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="a6a5d-145">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a6a5d-146">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a6a5d-146">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a6a5d-147">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="a6a5d-147">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a6a5d-148">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="a6a5d-148">Enable location-based store detection</span></span>](enable-store-detection.md)
