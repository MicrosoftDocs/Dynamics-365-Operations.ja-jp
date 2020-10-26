---
title: Azure ExpressRoute と Finance and Operations アプリ
description: 顧客は、 Finance and Operations アプリで Microsoft Azure ExpressRoute を使用して、オンプレミス インフラストラクチャに接続することができます。 このトピックでは、ExpressRoute を使い始めるのに必要な情報を提供します。
author: PeterRFriis
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 260954
ms.assetid: 5dccb418-b489-4777-aa5e-2a0b03b4f2b0
ms.search.region: Global
ms.author: perahlff
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e694aca206d26a1789a43cff4edee6267eb60633
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893391"
---
# <a name="azure-expressroute-and-finance-and-operations-apps"></a><span data-ttu-id="7448b-104">Azure ExpressRoute と Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="7448b-104">Azure ExpressRoute and Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7448b-105">顧客は、 Finance and Operations アプリで Microsoft Azure ExpressRoute を使用して、オンプレミス インフラストラクチャに接続することができます。</span><span class="sxs-lookup"><span data-stu-id="7448b-105">Customers can use Microsoft Azure ExpressRoute with Finance and Operations apps to connect to their on-premises infrastructure.</span></span> <span data-ttu-id="7448b-106">このトピックでは、ExpressRoute を使い始めるのに必要な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="7448b-106">This topic provides the information that you need to get started with ExpressRoute.</span></span>

<a name="overview"></a><span data-ttu-id="7448b-107">概要</span><span class="sxs-lookup"><span data-stu-id="7448b-107">Overview</span></span>
--------

<span data-ttu-id="7448b-108">Microsoft Azure ExpressRoute で、Azure データ センターとオンプレミスの場所の間に、専用で、すぐに使用できる、信頼性の高い、低待機時間の接続を作成できます。</span><span class="sxs-lookup"><span data-stu-id="7448b-108">Microsoft Azure ExpressRoute lets you create dedicated, readily available, highly reliable, low latency connections between Azure datacenters and your on-premises locations.</span></span> <span data-ttu-id="7448b-109">ExpressRoute 回線は顧客のオンプレミス ネットワークと接続プロバイダーを通じた Microsoft クラウド サービスでの論理接続です。</span><span class="sxs-lookup"><span data-stu-id="7448b-109">An ExpressRoute circuit is a logical connection between a customer’s on-premises network and Microsoft cloud services through a connectivity provider.</span></span> <span data-ttu-id="7448b-110">ExpressRoute は、 Finance and Operations とは別に構成されています。</span><span class="sxs-lookup"><span data-stu-id="7448b-110">ExpressRoute is configured separately from Finance and Operations apps.</span></span> <span data-ttu-id="7448b-111">実装に ExpressRoute 回路を使用するには、ネットワーク サービス プロバイダーに直接問い合わせる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7448b-111">To get an ExpressRoute circuit for your implementation, you must contact a network service provider directly.</span></span> <span data-ttu-id="7448b-112">ExpressRoute が構成された後、Finance and Operations アプリに接続することに加えて、顧客は Microsoft 365 などの様々なアプリケーションや、仮想マシンへの接続や仮想ネットワークに配置されたクラウド サービスなどの対応している Azure サービスに接続できます。</span><span class="sxs-lookup"><span data-stu-id="7448b-112">After ExpressRoute is configured, in addition to connecting to Finance and Operations apps, customers can connect to a variety of applications such as Microsoft 365 and supported Azure services, such as connecting to virtual machines and cloud services deployed in virtual networks.</span></span> <span data-ttu-id="7448b-113">サポートされているその他のサービスの詳細については、[[ExpressRoute FAQ](/azure/expressroute/expressroute-faqs)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7448b-113">To learn more about additional supported services, see [ExpressRoute FAQ](/azure/expressroute/expressroute-faqs).</span></span> <span data-ttu-id="7448b-114">ExpressRoute 回線を購入する前に、次のことを理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7448b-114">Before purchasing an ExpressRoute circuit, you will need to know the following:</span></span>

-   <span data-ttu-id="7448b-115">Finance and Operations アプリが配置されているデータ センター。</span><span class="sxs-lookup"><span data-stu-id="7448b-115">The datacenter that your Finance and Operations apps are located in.</span></span>
-   <span data-ttu-id="7448b-116">接続元となるリージョン。</span><span class="sxs-lookup"><span data-stu-id="7448b-116">The region where you will be connecting from.</span></span>

<span data-ttu-id="7448b-117">この情報は、ExpressRoute の標準または割増給与提供が必要かどうかを判別するために必要です。</span><span class="sxs-lookup"><span data-stu-id="7448b-117">This information is necessary to determine whether a standard or premium offering of ExpressRoute is required.</span></span>

## <a name="resources-for-getting-started"></a><span data-ttu-id="7448b-118">概要リソース</span><span class="sxs-lookup"><span data-stu-id="7448b-118">Resources for getting started</span></span>
-   [<span data-ttu-id="7448b-119">ExpressRoute サービス ページ</span><span class="sxs-lookup"><span data-stu-id="7448b-119">ExpressRoute service page</span></span>](https://azure.microsoft.com/services/expressroute/)
-   [<span data-ttu-id="7448b-120">ExpressRoute 技術の概要</span><span class="sxs-lookup"><span data-stu-id="7448b-120">ExpressRoute technical overview</span></span>](https://azure.microsoft.com/documentation/articles/expressroute-introduction/)
-   [<span data-ttu-id="7448b-121">ExpressRoute パートナーおよびピアリング場所</span><span class="sxs-lookup"><span data-stu-id="7448b-121">ExpressRoute partners and peering locations</span></span>](https://azure.microsoft.com/documentation/articles/expressroute-locations/)
-   [<span data-ttu-id="7448b-122">ExpressRoute の価格決定</span><span class="sxs-lookup"><span data-stu-id="7448b-122">ExpressRoute pricing</span></span>](https://azure.microsoft.com/pricing/details/expressroute/)




