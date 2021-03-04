---
title: Azure ExpressRoute と Finance and Operations アプリ
description: 顧客は、Microsoft Azure ExpressRoute を使用して、オンプレミス インフラストラクチャに接続できます。
author: PeterRFriis
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 260954
ms.assetid: 5dccb418-b489-4777-aa5e-2a0b03b4f2b0
ms.search.region: Global
ms.author: perahlff
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: da0af411f7770d523026a454c71930dbac974f9b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127664"
---
# <a name="azure-expressroute-and-finance-and-operations-apps"></a><span data-ttu-id="48ecd-103">Azure ExpressRoute と Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="48ecd-103">Azure ExpressRoute and Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48ecd-104">顧客は、 Finance and Operations アプリで Microsoft Azure ExpressRoute を使用して、オンプレミス インフラストラクチャに接続することができます。</span><span class="sxs-lookup"><span data-stu-id="48ecd-104">Customers can use Microsoft Azure ExpressRoute with Finance and Operations apps to connect to their on-premises infrastructure.</span></span> <span data-ttu-id="48ecd-105">このトピックでは、ExpressRoute を使い始めるのに必要な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="48ecd-105">This topic provides the information that you need to get started with ExpressRoute.</span></span>

<span data-ttu-id="48ecd-106">Microsoft Azure ExpressRoute で、Azure データ センターとオンプレミスの場所の間に、専用で、すぐに使用できる、信頼性の高い、低待機時間の接続を作成できます。</span><span class="sxs-lookup"><span data-stu-id="48ecd-106">Microsoft Azure ExpressRoute lets you create dedicated, readily available, highly reliable, low latency connections between Azure datacenters and your on-premises locations.</span></span> <span data-ttu-id="48ecd-107">ExpressRoute 回線は顧客のオンプレミス ネットワークと接続プロバイダーを通じた Microsoft クラウド サービスでの論理接続です。</span><span class="sxs-lookup"><span data-stu-id="48ecd-107">An ExpressRoute circuit is a logical connection between a customer’s on-premises network and Microsoft cloud services through a connectivity provider.</span></span> <span data-ttu-id="48ecd-108">ExpressRoute は、 Finance and Operations とは別に構成されています。</span><span class="sxs-lookup"><span data-stu-id="48ecd-108">ExpressRoute is configured separately from Finance and Operations apps.</span></span> <span data-ttu-id="48ecd-109">実装に ExpressRoute 回路を使用するには、ネットワーク サービス プロバイダーに直接問い合わせる必要があります。</span><span class="sxs-lookup"><span data-stu-id="48ecd-109">To get an ExpressRoute circuit for your implementation, you must contact a network service provider directly.</span></span> <span data-ttu-id="48ecd-110">ExpressRoute が構成された後、Finance and Operations アプリに接続することに加えて、顧客は Microsoft 365 などのアプリや、仮想マシンへの接続や仮想ネットワークに配置されたクラウド サービスなどの対応している Azure サービスに接続できます。</span><span class="sxs-lookup"><span data-stu-id="48ecd-110">After ExpressRoute is configured, in addition to connecting to Finance and Operations apps, customers can connect to apps such as Microsoft 365 and supported Azure services, such as connecting to virtual machines and cloud services deployed in virtual networks.</span></span> <span data-ttu-id="48ecd-111">サポートされているその他のサービスの詳細については、[ExpressRoute FAQ](/azure/expressroute/expressroute-faqs) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48ecd-111">To learn more about other supported services, see [ExpressRoute FAQ](/azure/expressroute/expressroute-faqs).</span></span> <span data-ttu-id="48ecd-112">ExpressRoute 回線を購入する前に、次の情報を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48ecd-112">Before purchasing an ExpressRoute circuit, you will need to know the following information:</span></span>

- <span data-ttu-id="48ecd-113">Finance and Operations アプリが配置されているデータ センター。</span><span class="sxs-lookup"><span data-stu-id="48ecd-113">The datacenter that your Finance and Operations apps are located in.</span></span>
- <span data-ttu-id="48ecd-114">接続元となるリージョン。</span><span class="sxs-lookup"><span data-stu-id="48ecd-114">The region where you will be connecting from.</span></span>

<span data-ttu-id="48ecd-115">この情報は、ExpressRoute の標準または割増給与提供が必要かどうかを判別するために必要です。</span><span class="sxs-lookup"><span data-stu-id="48ecd-115">This information is necessary to determine whether a standard or premium offering of ExpressRoute is required.</span></span>

## <a name="resources-for-getting-started"></a><span data-ttu-id="48ecd-116">概要リソース</span><span class="sxs-lookup"><span data-stu-id="48ecd-116">Resources for getting started</span></span>

- [<span data-ttu-id="48ecd-117">ExpressRoute サービス ページ</span><span class="sxs-lookup"><span data-stu-id="48ecd-117">ExpressRoute service page</span></span>](https://azure.microsoft.com/services/expressroute/)
- [<span data-ttu-id="48ecd-118">ExpressRoute 技術の概要</span><span class="sxs-lookup"><span data-stu-id="48ecd-118">ExpressRoute technical overview</span></span>](https://azure.microsoft.com/documentation/articles/expressroute-introduction/)
- [<span data-ttu-id="48ecd-119">ExpressRoute パートナーおよびピアリング場所</span><span class="sxs-lookup"><span data-stu-id="48ecd-119">ExpressRoute partners and peering locations</span></span>](https://azure.microsoft.com/documentation/articles/expressroute-locations/)
- [<span data-ttu-id="48ecd-120">ExpressRoute の価格決定</span><span class="sxs-lookup"><span data-stu-id="48ecd-120">ExpressRoute pricing</span></span>](https://azure.microsoft.com/pricing/details/expressroute/)
