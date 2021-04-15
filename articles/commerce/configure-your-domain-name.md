---
title: ドメイン名のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 E コマース サイトのドメイン名をコンフィギュレーションする方法について説明します。
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796054"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="aea3a-103">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="aea3a-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="aea3a-104">このトピックでは、Microsoft Dynamics 365 E コマース サイトのドメイン名をコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aea3a-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="aea3a-105">eコマースの初期化中にドメインを追加する</span><span class="sxs-lookup"><span data-stu-id="aea3a-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="aea3a-106">ドメインを Dynamics 365 Commerce e コマース環境に関連付けるには、[新しい e コマース テナントのデプロイ](deploy-ecommerce-site.md).に記載されている通り、e コマースを初期化します。</span><span class="sxs-lookup"><span data-stu-id="aea3a-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="aea3a-107">初期化中、e コマース環境のプロビジョニングに使用する情報を提供するように求められます。</span><span class="sxs-lookup"><span data-stu-id="aea3a-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="aea3a-108">**サポートされるホスト名** フィールドに、この環境で使用する予定のすべてのドメインを追加します。</span><span class="sxs-lookup"><span data-stu-id="aea3a-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="aea3a-109">複数のドメインはセミコロンで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="aea3a-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="aea3a-110">この方法で、全ての必要な e コーマース コンポーネントでドメインがコンフィギュレーションされ、それらは、コンテンツ配信ネットワーク (CDN) または Web サーバーからのトラフィックを切り替え、それを e コマース フロント エンドにポイントする際に使用する準備が整います。</span><span class="sxs-lookup"><span data-stu-id="aea3a-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="aea3a-111">e-コマースの初期化後にドメインを追加する</span><span class="sxs-lookup"><span data-stu-id="aea3a-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="aea3a-112">e コマースの初期化後に新しいドメインを e コマース環境に関連付けるには、サービス要求を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aea3a-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aea3a-113">追加リソース</span><span class="sxs-lookup"><span data-stu-id="aea3a-113">Additional resources</span></span>

[<span data-ttu-id="aea3a-114">新しい eコマース テナントのデプロイ</span><span class="sxs-lookup"><span data-stu-id="aea3a-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="aea3a-115">eコマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="aea3a-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="aea3a-116">オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="aea3a-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="aea3a-117">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="aea3a-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="aea3a-118">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="aea3a-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="aea3a-119">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="aea3a-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="aea3a-120">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="aea3a-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="aea3a-121">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="aea3a-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="aea3a-122">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="aea3a-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="aea3a-123">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="aea3a-123">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]