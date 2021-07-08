---
title: ヘッドレス コマースのアーキテクチャ
description: このトピックでは、ヘッドレス コマースのアーキテクチャについて説明します。
author: mugunthanm
ms.date: 06/20/2017
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: f150089f9e3b1a664c959867d46ba3c4b1f075e5
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271115"
---
# <a name="headless-commerce-architecture"></a><span data-ttu-id="90b59-103">ヘッドレス コマースのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="90b59-103">Headless commerce architecture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90b59-104">このトピックでは、ヘッドレス コマース (Commerce Scale Unit とも呼ばれる) のアーキテクチャについて説明します。</span><span class="sxs-lookup"><span data-stu-id="90b59-104">This topic describes the architecture of the headless commerce (also known as Commerce Scale Unit).</span></span> <span data-ttu-id="90b59-105">ヘッドレス コマースは、拡張可能で、カスタマイズされたフリクションフリーなコマース エクスペリエンス、および統合され最適化されたバック オフィス操作を可能にする API 駆動型のフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="90b59-105">The headless commerce is an API-driven framework that enables extensible, personalized, friction-free commerce experiences, and integrated, optimized back-office operations.</span></span>

![Commerce Scale Unit アーキテクチャ](./media/CSU.PNG)

## <a name="omnichannel-solution-provided-by-the-headless-commerce"></a><span data-ttu-id="90b59-107">ヘッドレス コマースが提供するオムニチャネル ソリューション</span><span class="sxs-lookup"><span data-stu-id="90b59-107">Omnichannel solution provided by the headless commerce</span></span>

<span data-ttu-id="90b59-108">ヘッドレス コマースのコマース API は Microsoft Dynamics 365 Commerce によって使用され (バックオフィス、ストア内、コール センター、および e コマース)、完全なオムニチャネル ソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="90b59-108">The commerce APIs of the headless commerce are consumed by Microsoft Dynamics 365 Commerce (back-office, in-store, call center, and e-commerce) and provide a complete omnichannel solution.</span></span> <span data-ttu-id="90b59-109">API は、サード パーティのアプリケーションおよび Microsoft Power Platform コネクタで使用できます。</span><span class="sxs-lookup"><span data-stu-id="90b59-109">The APIs can be consumed by third-party applications and Microsoft Power Platform connectors.</span></span>

![Commerce Scale Unit のプラットフォームの統合](./media/CSUConsumer.PNG)

## <a name="components"></a><span data-ttu-id="90b59-111">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="90b59-111">Components</span></span>

<span data-ttu-id="90b59-112">ヘッドレス コマースには、次のコンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="90b59-112">The headless commerce contains these components:</span></span>

+ <span data-ttu-id="90b59-113">コンシューマー API</span><span class="sxs-lookup"><span data-stu-id="90b59-113">Consumer APIs</span></span>
+ <span data-ttu-id="90b59-114">Commerce Runtime (CRT)</span><span class="sxs-lookup"><span data-stu-id="90b59-114">Commerce runtime (CRT)</span></span>
+ <span data-ttu-id="90b59-115">チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="90b59-115">Channel database</span></span>

### <a name="consumer-apis"></a><span data-ttu-id="90b59-116">コンシューマー API</span><span class="sxs-lookup"><span data-stu-id="90b59-116">Consumer APIs</span></span>

<span data-ttu-id="90b59-117">ヘッドレス コマースでは、Dynamics 365 Commerce 用の Open Data Protocol (OData) API と使用できるサード パーティ アプリが公開されます。</span><span class="sxs-lookup"><span data-stu-id="90b59-117">The headless commerce exposes Open Data Protocol (OData) APIs for Dynamics 365 Commerce and third-party applications to consume.</span></span> <span data-ttu-id="90b59-118">API レイヤーは、ASP.NET コアを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="90b59-118">The API layer is built by using ASP.NET Core.</span></span> <span data-ttu-id="90b59-119">クライアントが API を使用できるように異なった認証オプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="90b59-119">It provides different authentication options so that the clients can consume the APIs.</span></span> <span data-ttu-id="90b59-120">API は、ビジネス ロジックを公開するラッパーです。</span><span class="sxs-lookup"><span data-stu-id="90b59-120">The APIs are a wrapper that exposes the business logic.</span></span> <span data-ttu-id="90b59-121">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="90b59-121">For more information, see the following topics:</span></span>

+ [<span data-ttu-id="90b59-122">Commerce Scale Unit の顧客およびコンシューマー API</span><span class="sxs-lookup"><span data-stu-id="90b59-122">Commerce Scale Unit customer and consumer APIs</span></span>](retail-server-customer-consumer-api.md)
+ [<span data-ttu-id="90b59-123">API の使用</span><span class="sxs-lookup"><span data-stu-id="90b59-123">Consume APIs</span></span>](consume-retail-server-api.md)
+ [<span data-ttu-id="90b59-124">カスタム API</span><span class="sxs-lookup"><span data-stu-id="90b59-124">Custom APIs</span></span>](retail-server-icontroller-extension.md)

### <a name="commerce-runtime"></a><span data-ttu-id="90b59-125">Commerce Runtime</span><span class="sxs-lookup"><span data-stu-id="90b59-125">Commerce runtime</span></span>

<span data-ttu-id="90b59-126">CRT は、コア コマース ビジネス ロジックを含むポータブル .NET ライブラリの集合です。</span><span class="sxs-lookup"><span data-stu-id="90b59-126">CRT is a collection of portable .NET libraries that contain the core commerce business logic.</span></span> <span data-ttu-id="90b59-127">コンシューマー API はクライアントに使用するビジネス ロジックを公開します。</span><span class="sxs-lookup"><span data-stu-id="90b59-127">The consumer APIs expose the business logic for clients to consume.</span></span> <span data-ttu-id="90b59-128">ビジネス ロジックを追加または変更するには、CRT をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="90b59-128">To add or modify business logic, customize CRT.</span></span> <span data-ttu-id="90b59-129">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="90b59-129">For more information, see the following topics:</span></span>

+ [<span data-ttu-id="90b59-130">Commerce Runtime (CRT) のサービス</span><span class="sxs-lookup"><span data-stu-id="90b59-130">Commerce runtime (CRT) services</span></span>](crt-services.md)
+ [<span data-ttu-id="90b59-131">CRT 拡張機能</span><span class="sxs-lookup"><span data-stu-id="90b59-131">CRT Extensions</span></span>](commerce-runtime-extensibility.md)

### <a name="channel-database"></a><span data-ttu-id="90b59-132">チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="90b59-132">Channel database</span></span>

<span data-ttu-id="90b59-133">チャネル データベースは、オンライン ストアまたは従来型の店舗などの 1 つ以上のコマース チャネルからのトランザクション データおよびマスター データを保持します。</span><span class="sxs-lookup"><span data-stu-id="90b59-133">The channel database holds transactional data and master data from one or more commerce channels, such as an online store or a brick-and-mortar store.</span></span> <span data-ttu-id="90b59-134">マスター データは Commerce Data Exchange (CDX) を使用して、Commerce 本社からチャネル データベースにプッシュ ダウンされます。</span><span class="sxs-lookup"><span data-stu-id="90b59-134">Master data is pushed down from Commerce headquarters to the channel database by using Commerce Data Exchange (CDX).</span></span> <span data-ttu-id="90b59-135">チャネル データベースに格納されたトランザクション データは、CDX を使用して Commerce 本社に引き戻されます。</span><span class="sxs-lookup"><span data-stu-id="90b59-135">Transactional data that is stored in the channel database is pulled back to Commerce headquarters by using CDX.</span></span> <span data-ttu-id="90b59-136">詳細については、[チャネル データベース拡張機能](channel-db-extensions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="90b59-136">For more information, see [Channel database extensions](channel-db-extensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

