---
title: オンライン チャネルと E コマース サイトの関連付け
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトを 1 つ以上のオンライン ストアにバインドする方法について説明します。
author: stuharg
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: bicyclingfool
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62d3c168967bd680b3ded56e627730324f2a5ec6
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945585"
---
# <a name="associate-an-e-commerce-site-with-an-online-channel"></a><span data-ttu-id="20528-103">オンライン チャネルと E コマース サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="20528-103">Associate an e-Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="20528-104">このトピックでは、Microsoft Dynamics 365 Commerce サイトを 1 つ以上のオンライン ストアにバインドする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="20528-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="20528-105">Microsoft Dynamics Lifecycle Services (LCS) ポータルを使用して E コマースを準備したら、最初の E コマース Web サイトを確立する準備が整います。</span><span class="sxs-lookup"><span data-stu-id="20528-105">After you've provisioned e-Commerce by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-Commerce website.</span></span> <span data-ttu-id="20528-106">サイトの初期作成の一環として、サイトを以前に作成されたオンライン ストアに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="20528-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="20528-107">この手順により、サイトがオンライン チャネルにバインドされ、そのサイトには、ナビゲーション階層、製品、カテゴリ、価格、配送オプション、およびオンライン ストアで定義したその他すべてが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20528-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="20528-108">新しいサイトを確立し、そのサイトをオンライン ストアに関連付けるには、LCS でサイト作成環境のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="20528-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="20528-109">その後、サイト作成環境のページで、**新しいサイト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="20528-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="20528-110">**新しいサイト** ダイアログ ボックスでは、サイトに関する基本情報をいくつか入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20528-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="20528-111">入力する必要がある情報の詳しい説明については、[新しい E コマース サイトの作成](create-ecommerce-site.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20528-111">For a complete explanation of the information that you must provide, see [Create a new e-Commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="20528-112">サイトが作成されると、**製品**タブを選択することにより、そのサイトがオンライン ストアに関連付けられていることを確認できます。そこでは、オンライン ストアに割り当てられた製品の品揃えが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20528-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="20528-113">ページの左上にあるドロップダウン フィールドを使用して、割り当てられた製品にカテゴリ別にアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="20528-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20528-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="20528-114">Additional resources</span></span>

[<span data-ttu-id="20528-115">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="20528-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="20528-116">新しい E コマース サイトの配置</span><span class="sxs-lookup"><span data-stu-id="20528-116">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="20528-117">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="20528-117">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="20528-118">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="20528-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="20528-119">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="20528-119">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="20528-120">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="20528-120">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="20528-121">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="20528-121">Enable location-based store detection</span></span>](enable-store-detection.md)
