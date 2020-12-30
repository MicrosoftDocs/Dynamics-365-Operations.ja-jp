---
title: e コマース サイトの作成
description: このトピックでは、Dynamics 365 Commerce サイト ビルダーで新しい e コマース サイトを作成するために必要な手順と情報について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
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
ms.openlocfilehash: 7d552f29fd8f52b512a7c21b36b0a814cac50646
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517187"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="c333f-103">e コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="c333f-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c333f-104">このトピックでは、Dynamics 365 Commerce サイト ビルダーで新しい e コマース サイトを作成するために必要な手順と情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="c333f-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="c333f-105">Dynamics 365 Commerce 機能のライセンスを取得すると、サイト ビルダーには、独自のサイトの基礎として使用できるスターター サイトがプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="c333f-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="c333f-106">ただし、最初から開始する場合、または 2 つめのサイトを作成する場合は、サイト作成環境で新しいサイトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c333f-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="c333f-107">サイトの設定</span><span class="sxs-lookup"><span data-stu-id="c333f-107">Set up your site</span></span>

<span data-ttu-id="c333f-108">サイトを設定するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c333f-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="c333f-109">サイト ビルダーの環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="c333f-109">Open the site builder environment.</span></span> <span data-ttu-id="c333f-110">コマースの環境機能ページには、Microsoft Lifecycle Services (LCS) のサイト ビルダーへのリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c333f-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="c333f-111">サイト作成環境のホームページで、**新しいサイト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c333f-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="c333f-112">**新しいサイト** ダイアログ ボックスで、次の情報を入力してください。</span><span class="sxs-lookup"><span data-stu-id="c333f-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="c333f-113">フィールド</span><span class="sxs-lookup"><span data-stu-id="c333f-113">Field</span></span>                               | <span data-ttu-id="c333f-114">説明</span><span class="sxs-lookup"><span data-stu-id="c333f-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="c333f-115">サイト名</span><span class="sxs-lookup"><span data-stu-id="c333f-115">Site name</span></span>                           | <span data-ttu-id="c333f-116">サイト作成環境で、サイトに使用する表示名を入力します。</span><span class="sxs-lookup"><span data-stu-id="c333f-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="c333f-117">この名前は、作成環境でのみ表示され、顧客には表示されません。</span><span class="sxs-lookup"><span data-stu-id="c333f-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="c333f-118">サイト管理者のセキュリティ グループ</span><span class="sxs-lookup"><span data-stu-id="c333f-118">Site administrator's security group</span></span> | <span data-ttu-id="c333f-119">このサイトで管理者ロールを持つユーザーを管理する Microsoft Azure Active Directory (Azure AD) セキュリティ グループを指定します。</span><span class="sxs-lookup"><span data-stu-id="c333f-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="c333f-120">既定のチャネル (作業単位番号)</span><span class="sxs-lookup"><span data-stu-id="c333f-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="c333f-121">このサイトが Web ストア フロントとして使用されるオンライン ストアを選択します。</span><span class="sxs-lookup"><span data-stu-id="c333f-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="c333f-122">e コマース サイトで複数のオンライン ストアをサポートする場合は、サイトを設定した後で、**サイトの設定** でストアをサイトに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="c333f-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="c333f-123">既定の言語</span><span class="sxs-lookup"><span data-stu-id="c333f-123">Default language</span></span>                            | <span data-ttu-id="c333f-124">このオンライン ストアおよびマーケットの既定の言語を指定します。</span><span class="sxs-lookup"><span data-stu-id="c333f-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="c333f-125">オンライン ストアは複数の言語をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="c333f-125">An online store can support multiple languages.</span></span> <span data-ttu-id="c333f-126">このオンライン ストアまたは別のオンライン ストアに対して、複数の言語をサポートする場合は、サイトを設定した後に、**サイトの設定** で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="c333f-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="c333f-127">ドメイン</span><span class="sxs-lookup"><span data-stu-id="c333f-127">Domain</span></span>                              | <span data-ttu-id="c333f-128">このオンライン ストアでドメインとして使用されるドメイン名を選択します。</span><span class="sxs-lookup"><span data-stu-id="c333f-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="c333f-129">LCS でドメインをコンフィグレーションしていない場合は、このフィールドを空白のままにしておくことができます。</span><span class="sxs-lookup"><span data-stu-id="c333f-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="c333f-130">ドメインを LCS でコンフィグレーションしたら、**サイトの設定** でそのドメインをオンライン ストアに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c333f-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="c333f-131">パス</span><span class="sxs-lookup"><span data-stu-id="c333f-131">Path</span></span>                              | <span data-ttu-id="c333f-132">サイトが、特定のドメイン名に対して複数の言語をサポートしている場合は、パス フィールドを使用して、そのドメインと言語の組み合わせに固有のサイト URL を作成します。</span><span class="sxs-lookup"><span data-stu-id="c333f-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="c333f-133">**既定の言語** フィールドに指定した言語のみ、このドメインに対してサポートされる場合、またはサイトを他の言語にローカライズした後も、その言語を既定の言語として使用する場合は、このフィールドを空白のままにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c333f-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="c333f-134">サイトが作成されると、**製品** タブを選択することにより、そのサイトがオンライン ストアに関連付けられていることを確認できます。そこでは、オンライン ストアに割り当てられた製品の品揃えが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c333f-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="c333f-135">ページの左上にあるドロップダウン メニューを使用して、割り当てられた製品にカテゴリ別にアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c333f-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c333f-136">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c333f-136">Additional resources</span></span>

[<span data-ttu-id="c333f-137">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c333f-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="c333f-138">新しい eコマース テナントのデプロイ</span><span class="sxs-lookup"><span data-stu-id="c333f-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="c333f-139">オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="c333f-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="c333f-140">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="c333f-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="c333f-141">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="c333f-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="c333f-142">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="c333f-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="c333f-143">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="c333f-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="c333f-144">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c333f-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="c333f-145">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="c333f-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="c333f-146">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="c333f-146">Enable location-based store detection</span></span>](enable-store-detection.md)
