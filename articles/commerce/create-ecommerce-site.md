---
title: E コマース サイトの作成
description: このトピックでは、Dynamics 365 Commerce における新しい E コマース サイトの作成に関連する作業について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697132"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="850e7-103">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="850e7-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="850e7-104">このトピックでは、Dynamics 365 Commerce における新しい E コマース サイトの作成に関連する作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="850e7-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="850e7-105">概要</span><span class="sxs-lookup"><span data-stu-id="850e7-105">Overview</span></span>

<span data-ttu-id="850e7-106">E コマース サイトの開発を開始するには、最初にサイト作成環境で新しいサイトを開設する必要があります。</span><span class="sxs-lookup"><span data-stu-id="850e7-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="850e7-107">新しいサイトを作成する前に、少なくとも 1 つのオンライン ストアを Dynamics 365 Retail で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="850e7-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="850e7-108">サイトの設定</span><span class="sxs-lookup"><span data-stu-id="850e7-108">Set up your site</span></span>

<span data-ttu-id="850e7-109">サイトを設定するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="850e7-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="850e7-110">Microsoft Lifecycle Services (LCS) で、サイト作成環境のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="850e7-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="850e7-111">サイト作成環境のホームページで、**新しいサイト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="850e7-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="850e7-112">**新しいサイト** ダイアログ ボックスで、次の情報を入力してください。</span><span class="sxs-lookup"><span data-stu-id="850e7-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="850e7-113">フィールド</span><span class="sxs-lookup"><span data-stu-id="850e7-113">Field</span></span>                               | <span data-ttu-id="850e7-114">説明</span><span class="sxs-lookup"><span data-stu-id="850e7-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="850e7-115">サイト名</span><span class="sxs-lookup"><span data-stu-id="850e7-115">Site name</span></span>                           | <span data-ttu-id="850e7-116">サイト作成環境で、サイトに使用する表示名を入力します。</span><span class="sxs-lookup"><span data-stu-id="850e7-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="850e7-117">この名前は、作成環境でのみ表示され、顧客には表示されません。</span><span class="sxs-lookup"><span data-stu-id="850e7-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="850e7-118">サイト管理者のセキュリティ グループ</span><span class="sxs-lookup"><span data-stu-id="850e7-118">Site administrator's security group</span></span> | <span data-ttu-id="850e7-119">このサイトで管理者ロールを持つユーザーを管理する Microsoft Azure Active Directory (Azure AD) セキュリティ グループを指定します。</span><span class="sxs-lookup"><span data-stu-id="850e7-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="850e7-120">既定のチャネル (作業単位番号)</span><span class="sxs-lookup"><span data-stu-id="850e7-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="850e7-121">このサイトが Web ストア フロントとして使用されるオンライン ストアを選択します。</span><span class="sxs-lookup"><span data-stu-id="850e7-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="850e7-122">E コマース サイトで複数のオンライン ストアをサポートする場合は、サイトを設定した後で、**サイトの設定**でストアをサイトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="850e7-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="850e7-123">既定の言語</span><span class="sxs-lookup"><span data-stu-id="850e7-123">Default language</span></span>                            | <span data-ttu-id="850e7-124">このオンライン ストアおよびマーケットの既定の言語を指定します。</span><span class="sxs-lookup"><span data-stu-id="850e7-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="850e7-125">オンライン ストアは複数の言語をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="850e7-125">An online store can support multiple languages.</span></span> <span data-ttu-id="850e7-126">このオンライン ストアまたは別のオンライン ストアに対して、複数の言語をサポートする場合は、サイトを設定した後に、**サイトの設定**で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="850e7-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="850e7-127">ドメイン</span><span class="sxs-lookup"><span data-stu-id="850e7-127">Domain</span></span>                              | <span data-ttu-id="850e7-128">このオンライン ストアでドメインとして使用されるドメイン名を選択します。</span><span class="sxs-lookup"><span data-stu-id="850e7-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="850e7-129">LCS でドメインをコンフィグレーションしていない場合は、このフィールドを空白のままにしておくことができます。</span><span class="sxs-lookup"><span data-stu-id="850e7-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="850e7-130">ドメインを LCS でコンフィグレーションしたら、**サイトの設定**でそのドメインをオンライン ストアに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="850e7-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="850e7-131">パス</span><span class="sxs-lookup"><span data-stu-id="850e7-131">Path</span></span>                              | <span data-ttu-id="850e7-132">サイトが、特定のドメイン名に対して複数の言語をサポートしている場合は、パス フィールドを使用して、そのドメインと言語の組み合わせに固有のサイト URL を作成します。</span><span class="sxs-lookup"><span data-stu-id="850e7-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="850e7-133">**既定の言語**フィールドに指定した言語のみ、このドメインに対してサポートされる場合、またはサイトを他の言語にローカライズした後も、その言語を既定の言語として使用する場合は、このフィールドを空白のままにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="850e7-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="850e7-134">サイトが作成されると、**製品**タブを選択することにより、そのサイトがオンライン ストアに関連付けられていることを確認できます。そこでは、オンライン ストアに割り当てられた製品の品揃えが表示されます。</span><span class="sxs-lookup"><span data-stu-id="850e7-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="850e7-135">ページの左上にあるドロップダウン メニューを使用して、割り当てられた製品にカテゴリ別にアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="850e7-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="850e7-136">追加リソース</span><span class="sxs-lookup"><span data-stu-id="850e7-136">Additional resources</span></span>

[<span data-ttu-id="850e7-137">オンライン ストアの概要</span><span class="sxs-lookup"><span data-stu-id="850e7-137">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="850e7-138">新しい E コマース サイトの配置</span><span class="sxs-lookup"><span data-stu-id="850e7-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="850e7-139">チャンネルとオンライン サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="850e7-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="850e7-140">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="850e7-140">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="850e7-141">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="850e7-141">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="850e7-142">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="850e7-142">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="850e7-143">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="850e7-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="850e7-144">ホーム ページの概要の作成</span><span class="sxs-lookup"><span data-stu-id="850e7-144">Authoring home page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="850e7-145">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="850e7-145">Add a new site page</span></span>](add-new-page.md)
