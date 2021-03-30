---
title: Dynamics 365 Commerce サイトとオンライン チャネルの関連付け
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトを 1 つ以上のオンライン ストアにバインドする方法について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb39b54e45e387067720dcbc5d9ccffbf8bf08b4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211525"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="083ef-103">Dynamics 365 Commerce サイトとオンライン チャネルの関連付け</span><span class="sxs-lookup"><span data-stu-id="083ef-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="083ef-104">このトピックでは、Microsoft Dynamics 365 Commerce サイトを 1 つ以上のオンライン ストアにバインドする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="083ef-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="083ef-105">Microsoft Dynamics Lifecycle Services (LCS) ポータルを使用して自分の Dynamics 365 Commerce E コマース環境をプロビジョニングしたら、最初の E コマース Web サイトを確立する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="083ef-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="083ef-106">サイトの初期作成の一環として、サイトを以前に作成されたオンライン ストアに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="083ef-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="083ef-107">この手順により、サイトがオンライン チャネルにバインドされ、そのサイトには、ナビゲーション階層、製品、カテゴリ、価格、配送オプション、およびオンライン ストアで定義したその他すべてが表示されます。</span><span class="sxs-lookup"><span data-stu-id="083ef-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="083ef-108">新しいサイトを確立し、そのサイトをオンライン ストアに関連付けるには、LCS でサイト作成環境のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="083ef-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="083ef-109">その後、サイト作成環境のページで、**新しいサイト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="083ef-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="083ef-110">**新しいサイト** ダイアログ ボックスでは、サイトに関する基本情報をいくつか入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="083ef-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="083ef-111">入力する必要がある情報の詳しい説明については、[新しい E コマース サイトの作成](create-ecommerce-site.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="083ef-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="083ef-112">サイトが作成されると、**製品** タブを選択することにより、そのサイトがオンライン ストアに関連付けられていることを確認できます。そこでは、オンライン ストアに割り当てられた製品の品揃えが表示されます。</span><span class="sxs-lookup"><span data-stu-id="083ef-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="083ef-113">ページの左上にあるドロップダウン フィールドを使用して、割り当てられた製品にカテゴリ別にアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="083ef-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="083ef-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="083ef-114">Additional resources</span></span>

[<span data-ttu-id="083ef-115">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="083ef-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="083ef-116">新しい eコマース テナントのデプロイ</span><span class="sxs-lookup"><span data-stu-id="083ef-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="083ef-117">eコマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="083ef-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="083ef-118">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="083ef-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="083ef-119">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="083ef-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="083ef-120">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="083ef-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="083ef-121">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="083ef-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="083ef-122">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="083ef-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="083ef-123">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="083ef-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="083ef-124">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="083ef-124">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]