---
title: "Azure ExpressRoute と Finance and Operations"
description: "顧客は、Finance and Operations でMicrosoft Azure ExpressRoute を使用して、社内のインフラストラクチャに接続することができます。 このトピックでは、ExpressRoute を使い始めるのに必要な情報を提供します。"
author: sarvanisathish
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 260954
ms.assetid: 5dccb418-b489-4777-aa5e-2a0b03b4f2b0
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 00725f31244c8daa1e3cb16e7c5c4373735c70fd
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="azure-expressroute-and-finance-and-operations"></a><span data-ttu-id="0ff5c-104">Azure ExpressRoute と Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0ff5c-104">Azure ExpressRoute and Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ff5c-105">顧客は、Finance and Operations でMicrosoft Azure ExpressRoute を使用して、社内のインフラストラクチャに接続することができます。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-105">Customers can use Microsoft Azure ExpressRoute with Finance and Operations to connect to their on-premises infrastructure.</span></span> <span data-ttu-id="0ff5c-106">このトピックでは、ExpressRoute を使い始めるのに必要な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-106">This topic provides the information that you need to get started with ExpressRoute.</span></span>

<a name="overview"></a><span data-ttu-id="0ff5c-107">概要</span><span class="sxs-lookup"><span data-stu-id="0ff5c-107">Overview</span></span>
--------

<span data-ttu-id="0ff5c-108">Microsoft Azure ExpressRoute で、Azure データ センターとオンプレミスの場所の間に、プライベートですぐに使用できる、信頼性の高い低待機時間の接続を作成できます。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-108">Microsoft Azure ExpressRoute lets you create private, readily available, highly reliable, low latency connections between Azure datacenters and your on-premises locations.</span></span> <span data-ttu-id="0ff5c-109">ExpressRoute 回線は顧客のオンプレミス ネットワークと接続プロバイダーを通じた Microsoft クラウド サービスでの論理接続です。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-109">An ExpressRoute circuit is a logical connection between a customer’s on-premises network and Microsoft cloud services through a connectivity provider.</span></span> <span data-ttu-id="0ff5c-110">ExpressRoute は、Microsoft Dynamics 365 for Finance and Operations とは個別に構成されています。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-110">ExpressRoute is configured separately from Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="0ff5c-111">実装に ExpressRoute 回路を使用するには、ネットワーク サービス プロバイダーに直接問い合わせる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-111">To get an ExpressRoute circuit for your implementation, you must contact a network service provider directly.</span></span> <span data-ttu-id="0ff5c-112">ExpressRoute がコンフィギュレーションされた後、Finance and Operations に接続することに加えて、顧客は Office 365 などの様々なアプリケーションや、仮想マシンへの接続および仮想ネットワークに配置されたクラウド サービスなどのサポートされている Azure サービスに接続できます。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-112">After ExpressRoute is configured, in addition to connecting to Finance and Operations, customers can connect to a variety of applications such as Office 365 and supported Azure services, such as connecting to virtual machines and cloud services deployed in virtual networks.</span></span> <span data-ttu-id="0ff5c-113">サポートされているその他のサービスの詳細については、[[ExpressRoute FAQ](/azure/expressroute/expressroute-faqs)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-113">To learn more about additional supported services, see [ExpressRoute FAQ](/azure/expressroute/expressroute-faqs).</span></span> <span data-ttu-id="0ff5c-114">Finance and Operations の ExpressRoute 回線を購入する前に、次のことを理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-114">Before purchasing an ExpressRoute circuit for Finance and Operations, you will need to know the following:</span></span>

-   <span data-ttu-id="0ff5c-115">Finance and Operations インスタンスが配置されているデータセンター。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-115">The datacenter that your Finance and Operations instance is located in.</span></span>
-   <span data-ttu-id="0ff5c-116">接続元となるリージョン。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-116">The region where you will be connecting from.</span></span>

<span data-ttu-id="0ff5c-117">この情報は、ExpressRoute の標準または割増給与提供が必要かどうかを判別するために必要です。</span><span class="sxs-lookup"><span data-stu-id="0ff5c-117">This information is necessary to determine whether a standard or premium offering of ExpressRoute is required.</span></span>

## <a name="resources-for-getting-started"></a><span data-ttu-id="0ff5c-118">概要リソース</span><span class="sxs-lookup"><span data-stu-id="0ff5c-118">Resources for getting started</span></span>
-   [<span data-ttu-id="0ff5c-119">ExpressRoute サービス ページ</span><span class="sxs-lookup"><span data-stu-id="0ff5c-119">ExpressRoute service page</span></span>](https://azure.microsoft.com/en-us/services/expressroute/)
-   [<span data-ttu-id="0ff5c-120">ExpressRoute 技術の概要</span><span class="sxs-lookup"><span data-stu-id="0ff5c-120">ExpressRoute technical overview</span></span>](https://azure.microsoft.com/en-us/documentation/articles/expressroute-introduction/)
-   [<span data-ttu-id="0ff5c-121">ExpressRoute パートナーおよびピアリング場所</span><span class="sxs-lookup"><span data-stu-id="0ff5c-121">ExpressRoute partners and peering locations</span></span>](https://azure.microsoft.com/en-us/documentation/articles/expressroute-locations/)
-   [<span data-ttu-id="0ff5c-122">ExpressRoute の価格決定</span><span class="sxs-lookup"><span data-stu-id="0ff5c-122">ExpressRoute pricing</span></span>](https://azure.microsoft.com/en-us/pricing/details/expressroute/)





