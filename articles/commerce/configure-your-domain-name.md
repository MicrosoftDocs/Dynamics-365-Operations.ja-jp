---
title: ドメイン名のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 E コマース サイトのドメイン名をコンフィギュレーションする方法について説明します。
author: psimolin
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2ad9ca3aee21301ef6d830d7b29982a45cd53f60
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096823"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="6876b-103">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6876b-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6876b-104">このトピックでは、Microsoft Dynamics 365 E コマース サイトのドメイン名をコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6876b-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="6876b-105">E-コマースの初期化中にドメインを追加する</span><span class="sxs-lookup"><span data-stu-id="6876b-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="6876b-106">ドメインを E コマース環境に関連付けるには、[新しい E コマース サイトの配置](deploy-ecommerce-site.md) に記載され E コマースを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6876b-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="6876b-107">初期化中、E コマース環境のプロビジョニングに使用する情報を提供するように求められます。</span><span class="sxs-lookup"><span data-stu-id="6876b-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="6876b-108">**サポートされるホスト名**フィールドに、この環境で使用する予定のすべてのドメインを追加します。</span><span class="sxs-lookup"><span data-stu-id="6876b-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="6876b-109">複数のドメインはセミコロンで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="6876b-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="6876b-110">この方法で、全ての必要な E コーマース コンポーネントでドメインがコンフィギュレーションされ、それらは、コンテンツ配信ネットワーク (CDN) または Web サーバーからのトラフィックを切り替えて、それを E コマース フロント エンドにポイントする際に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6876b-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="6876b-111">E-コマースの初期化後にドメインを追加する</span><span class="sxs-lookup"><span data-stu-id="6876b-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="6876b-112">E コマースの初期化後に新しいドメインを E コマース環境に関連付けるには、サービス要求を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6876b-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6876b-113">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6876b-113">Additional resources</span></span>

[<span data-ttu-id="6876b-114">新しい E コマース サイトの配置</span><span class="sxs-lookup"><span data-stu-id="6876b-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6876b-115">オンライン ストア チャネルのセットアップ</span><span class="sxs-lookup"><span data-stu-id="6876b-115">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="6876b-116">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="6876b-116">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="6876b-117">チャンネルとオンライン サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="6876b-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6876b-118">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="6876b-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="6876b-119">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="6876b-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="6876b-120">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="6876b-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="6876b-121">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="6876b-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6876b-122">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6876b-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="6876b-123">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="6876b-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6876b-124">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="6876b-124">Enable location-based store detection</span></span>](enable-store-detection.md)
