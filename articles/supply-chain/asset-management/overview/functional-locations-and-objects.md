---
title: 機能的な場所と資産
description: このトピックでは、資産管理の機能的な場所と資産について説明します。 資産管理は、Dynamics 365 Supply Chain Management の資産およびメンテナンス ジョブを管理するための高度なモジュールです。
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3a42d36fd137aa780886276a4235f1b8f3a3680
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653350"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="6c8b8-104">機能的な場所と資産</span><span class="sxs-lookup"><span data-stu-id="6c8b8-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6c8b8-105">このトピックでは、資産管理の機能的な場所と資産について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="6c8b8-106">資産管理は、Dynamics 365 Supply Chain Management の資産およびメンテナンス ジョブを管理するための高度なモジュールです。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="6c8b8-107">概要</span><span class="sxs-lookup"><span data-stu-id="6c8b8-107">Overview</span></span>

<span data-ttu-id="6c8b8-108">資産管理は、Finance and Operations アプリでいくつかのモジュールとシームレスに統合されています。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="6c8b8-109">次の図は、他のモジュールとのインターフェイスを示しています。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-109">The following illustration shows the interfaces with other modules.</span></span>

![他のモジュールとの資産管理インターフェイスを示す図](media/01-overview-image.png)

<span data-ttu-id="6c8b8-111">資産管理を使用すると、社内のさまざまな種類の設備の管理とサービスに関連するすべてのタスクを効率的に管理および実行できます。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="6c8b8-112">この設備には、機械、生産施設、および車両が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="6c8b8-113">資産管理は、さまざまな業界にわたるソリューションもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="6c8b8-114">次の図は、資産管理で対象となる主な機能の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![資産管理の主要機能を示す図](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="6c8b8-116">機能の場所と資産</span><span class="sxs-lookup"><span data-stu-id="6c8b8-116">Functional locations and assets</span></span>

<span data-ttu-id="6c8b8-117">機能的な場所は、場所にある資産を管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="6c8b8-118">この管理には、機能的な場所の資産原価の追跡が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="6c8b8-119">機能的な場所は階層構造で、場所はサブの場所を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="6c8b8-120">機能的な場所の構造は静的です。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-120">The structure of functional locations is static.</span></span> <span data-ttu-id="6c8b8-121">つまり、場所を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-121">In other words, locations can't change place.</span></span> <span data-ttu-id="6c8b8-122">資産は機能的な場所に導入でき、必要に応じて、後で他の機能的な場所に導入することができます。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="6c8b8-123">資産原価は、常に資産の場所に従います。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="6c8b8-124">つまり、新しい機能的な場所に資産を導入すると、その資産は新しい機能的な場所に関連する財務分析コードを自動的に使用します。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="6c8b8-125">したがって、資産原価は、常に資産が現在導入されている機能的な場所に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="6c8b8-126">財務分析コードのこの自動処理は、会社が機能的な場所に関するプロジェクト管理とレポートを行う際に、コストの完全な追跡をするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="6c8b8-127">機能的な場所の階層を構築する方法は、内部設備の管理や顧客設備の管理に関する会社の要件によって異なります。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="6c8b8-128">次の図は、地理的な場所に基づく機能的な場所の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![地理的な場所に基づく機能上の場所を示す図](media/03-overview-image.png)

<span data-ttu-id="6c8b8-130">次の図は、顧客に基づく機能的な場所の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6c8b8-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![顧客に基づく機能上の場所を示す図](media/04-overview-image.png)
