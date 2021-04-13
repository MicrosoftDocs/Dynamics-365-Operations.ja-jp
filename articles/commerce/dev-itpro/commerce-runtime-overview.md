---
title: Commerce Runtime (CRT) のアーキテクチャおよびコンフィギュレーション
description: この記事では、Commerce Runtime (CRT) のアーキテクチャと構成に関する情報を提供します。
author: AamirAllaq
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 218654
ms.assetid: ac422f7e-bc71-4b42-b8c1-4702c6c18421
ms.search.region: Global
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 35d00d59f961c1eef2f148da433a72ba34016a19
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795679"
---
# <a name="commerce-runtime-crt-architecture-and-configuration"></a><span data-ttu-id="02333-103">Commerce Runtime (CRT) のアーキテクチャおよびコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="02333-103">Commerce runtime (CRT) architecture and configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02333-104">この記事では、Commerce Runtime (CRT) のアーキテクチャと構成に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="02333-104">This article provides information about the architecture and configuration of Commerce Runtime (CRT).</span></span> <span data-ttu-id="02333-105">CRT は、ビジネス ロジックをカプセル化するポータブル .NET ライブラリの集合です。</span><span class="sxs-lookup"><span data-stu-id="02333-105">The CRT is a collection of portable .NET libraries that encapsulate business logic.</span></span> <span data-ttu-id="02333-106">コマース チャネルのエンジンとして機能します。</span><span class="sxs-lookup"><span data-stu-id="02333-106">It serves as the engine for the commerce channel.</span></span> 

## <a name="commerce-runtime-architecture"></a><span data-ttu-id="02333-107">Commerce Runtime アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="02333-107">Commerce Runtime architecture</span></span>

<span data-ttu-id="02333-108">次の図は、Microsoft Dynamics 365 Commerce Runtime (CRT) のコンポーネントを示しています。</span><span class="sxs-lookup"><span data-stu-id="02333-108">The following diagram shows the components of the Microsoft Dynamics 365 Commerce Runtime (CRT).</span></span> 

<span data-ttu-id="02333-109">[![Commerce Runtime コンポーネント](./media/crt-architecture-1024x793.jpg)](./media/crt-architecture.jpg)</span><span class="sxs-lookup"><span data-stu-id="02333-109">[![Commerce Runtime components](./media/crt-architecture-1024x793.jpg)](./media/crt-architecture.jpg)</span></span>

### <a name="data-access"></a><span data-ttu-id="02333-110">データ アクセス</span><span class="sxs-lookup"><span data-stu-id="02333-110">Data access</span></span>

<span data-ttu-id="02333-111">データベースの上は、データ アクセス レイヤーです。</span><span class="sxs-lookup"><span data-stu-id="02333-111">On top of the database is a data access layer.</span></span> <span data-ttu-id="02333-112">データ アクセス レイヤーでは、生データがメモリ内のオブジェクトに変換されます。</span><span class="sxs-lookup"><span data-stu-id="02333-112">In the data access layer, raw data is translated into objects in memory.</span></span> <span data-ttu-id="02333-113">たとえば、オブジェクトは、製品である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="02333-113">For example, an object might be a product.</span></span> <span data-ttu-id="02333-114">製品は、価格や色などの属性を持ちます。</span><span class="sxs-lookup"><span data-stu-id="02333-114">Products have attributes, such as price and color.</span></span> <span data-ttu-id="02333-115">データ アクセス レイヤーには、オブジェクトを操作するための機能があります。</span><span class="sxs-lookup"><span data-stu-id="02333-115">The data access layer has functions that you can use to manipulate the objects.</span></span> <span data-ttu-id="02333-116">ストアド プロシージャは、サービスとワークフローで使用できるデータ エンティティにデータベースからデータのパケットを渡します。</span><span class="sxs-lookup"><span data-stu-id="02333-116">Stored procedures pass packets of data from the database to data entities that can be used in services and workflows.</span></span> <span data-ttu-id="02333-117">データのパケットを更新して、コマースに追加する新しいフィールドを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="02333-117">You can update the packets of data to include new fields that you add in Commerce.</span></span>

### <a name="services"></a><span data-ttu-id="02333-118">サービス</span><span class="sxs-lookup"><span data-stu-id="02333-118">Services</span></span>

<span data-ttu-id="02333-119">データ アクセス レイヤーの上は、サービス レイヤーです。</span><span class="sxs-lookup"><span data-stu-id="02333-119">On top of the data access layer is a services layer.</span></span> <span data-ttu-id="02333-120">リアルタイム データのクエリを処理します。</span><span class="sxs-lookup"><span data-stu-id="02333-120">Services query for real-time data.</span></span> <span data-ttu-id="02333-121">これらのサービスを使用して、既存の機能をカスタマイズしたり、新しい機能を含む独自のサービスを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="02333-121">You can use these services to customize existing functionality, or you can add your own services that include new functionality.</span></span>

### <a name="workflows"></a><span data-ttu-id="02333-122">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="02333-122">Workflows</span></span>

<span data-ttu-id="02333-123">サービス レイヤーの上は、ワークフロー レイヤーです。</span><span class="sxs-lookup"><span data-stu-id="02333-123">On top of the services layer is the workflow layer.</span></span> <span data-ttu-id="02333-124">ワークフローは、業務プロセスを定義するサービスとビジネス ロジックの集合です。</span><span class="sxs-lookup"><span data-stu-id="02333-124">A workflow is a collection of services and business logic that, together, define business processes.</span></span> <span data-ttu-id="02333-125">たとえば、顧客がカートに品目を追加すると、価格の取得、検証の実行、在庫数量の確認、出荷費用の計算、税計算、および割引計算をするためワークフローを使用できます。</span><span class="sxs-lookup"><span data-stu-id="02333-125">For example, when a customer adds an item to the cart, you can use a workflow to get the price, perform validation, check the inventory quantity, calculate shipping charges, calculate tax, and calculate discounts.</span></span> <span data-ttu-id="02333-126">コマースに含まれているワークフローを使用することも、新しいワークフローを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="02333-126">You can use the workflows that are included in Commerce, or you can create new workflows.</span></span> <span data-ttu-id="02333-127">ワークフローを使用して、業務プロセスの一部としてサードパーティ製システムに接続することもできます。</span><span class="sxs-lookup"><span data-stu-id="02333-127">You can even use a workflow to connect to a third-party system as part of your business processes.</span></span>

### <a name="api"></a><span data-ttu-id="02333-128">API</span><span class="sxs-lookup"><span data-stu-id="02333-128">API</span></span>

<span data-ttu-id="02333-129">ワークフロー レイヤーーの上は、アプリケーション プログラミング インターフェイス (API) レイヤーです。</span><span class="sxs-lookup"><span data-stu-id="02333-129">On top of the workflow layer is the application programming interface (API) layer.</span></span> <span data-ttu-id="02333-130">項目に関する情報の取得、価格の計算、配送料の計算、および発注などのタスクのために API を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="02333-130">You can use the API for tasks such as getting information about items, calculating prices, calculating shipping charges, and placing orders.</span></span> <span data-ttu-id="02333-131">業務プロセスに合わせて API を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="02333-131">You can extend the API to fit your business processes.</span></span>

## <a name="commerce-runtime-configuration"></a><span data-ttu-id="02333-132">Commerce Runtime のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="02333-132">Commerce Runtime configuration</span></span>

<span data-ttu-id="02333-133">サービスは、CRT コンフィギュレーション ファイルのタイプとして列挙されます。</span><span class="sxs-lookup"><span data-stu-id="02333-133">Services are enumerated as types in the CRT configuration file.</span></span> <span data-ttu-id="02333-134">タイプを CRT 構成ファイルに追加して、どのサービスが CRT に読み込まれるかコントロールすることができます。</span><span class="sxs-lookup"><span data-stu-id="02333-134">You can add types in the CRT configuration file to control which services are loaded in the CRT.</span></span> <span data-ttu-id="02333-135">コンフィギュレーション ファイルに一覧表示された順序でサービスが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="02333-135">Services are loaded in the order in which they are listed in the configuration file.</span></span> <span data-ttu-id="02333-136">すべての既定サービスは自動的に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="02333-136">All the default services are loaded automatically.</span></span> <span data-ttu-id="02333-137">ただし、既定のサービスのいずれかの上に新しいサービスを追加する場合、新しいサービスは既定のサービスに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="02333-137">However, if you add a new service above one of the default services, the new service replaces the default service.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
