---
title: コマース コンポーネント
description: このトピックは、Dynamics 365 Commerce を構成するさまざまなコンポーネントについて説明します。
author: sericks007
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailITWorkspace
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 221954
ms.assetid: 8fe1b080-00d4-41ae-b047-10da160877ab
ms.search.region: Global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b5104413686418c2999f618f833714f351d48b12
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004619"
---
# <a name="commerce-components"></a><span data-ttu-id="8dc5e-103">コマース コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8dc5e-103">Commerce components</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8dc5e-104">このトピックは、Dynamics 365 Commerce を構成するさまざまなコンポーネントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-104">This topic describes the various components that make up Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8dc5e-105">コマースは、中規模市場および大規模小売業者に、オンラインと従来型のストアのサポートを含む完全な本社および販売時点管理 (POS) ソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-105">Commerce provides mid-market and large retailers with a complete head office and point of sale (POS) solution that includes support for online and brick-and-mortar stores.</span></span> <span data-ttu-id="8dc5e-106">小売業者が財務収益を高め、サービスを向上させ、成長を管理して、顧客に到達し、効率面を合理化できます。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-106">It can help retailers increase financial returns, improve service, manage growth, reach customers, and streamline efficiencies.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8dc5e-107">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8dc5e-107">Component</span></span></th>
<th><span data-ttu-id="8dc5e-108">職務</span><span class="sxs-lookup"><span data-stu-id="8dc5e-108">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8dc5e-109">バックオフィス</span><span class="sxs-lookup"><span data-stu-id="8dc5e-109">Headquarters</span></span></td>
<td><span data-ttu-id="8dc5e-110">コマース用バックオフィスを使用すると、一連の店舗を 1 つの企業として管理することができます。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-110">Headquarters for Commerce can be used to manage a chain of stores as one enterprise.</span></span> <span data-ttu-id="8dc5e-111">これは、日々の業務を管理し、チェーンの全店舗の販売情報を追跡します。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-111">It controls daily operations and tracks sales information for every store in the chain.</span></span> <span data-ttu-id="8dc5e-112">コマース スケジューラは、コマースと店舗間の通信を調整します。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-112">Commerce Scheduler coordinates communication between Commerce and the stores.</span></span> <span data-ttu-id="8dc5e-113">バックオフィスは、POS、または必要なデータを受信して転送できるオンライン店舗システムで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-113">Headquarters can be used with any POS or online store system that can receive and transmit the required data.</span></span>
<p><span data-ttu-id="8dc5e-114"><strong>重要:</strong> コマースにおいて、カスタム POS またはオンライン ストア ソリューションの構築を行うには、広範囲にわたる計画、開発、およびテストなどの複雑な作業が必要となります。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-114"><strong>Important:</strong> Building a custom POS or online store solution for Commerce is a complex task that requires extensive planning, development, and testing.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="8dc5e-115">販売時点管理 (POS)</span><span class="sxs-lookup"><span data-stu-id="8dc5e-115">Point of sale (POS)</span></span></td>
<td><span data-ttu-id="8dc5e-116">コマースでは POS エクスペリエンスの 2 種類のイベントがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-116">Commerce supports two types of POS experience:</span></span>
<ul>
<li><span data-ttu-id="8dc5e-117"><strong>クラウド POS</strong> はブラウザベースの POS で、モバイルデバイスで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-117"><strong>Cloud POS</strong> is a browser-based POS that can be used on mobile devices.</span></span></li>
<li><span data-ttu-id="8dc5e-118"><strong>Modern POS</strong> (MPOS) は、PC、タブレット、電話などのクライアントで、販売トランザクション、顧客注文、日常業務を処理し、在庫管理を実行するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-118"><strong>Modern POS</strong> (MPOS) can be used on clients such as PCs, tablets, and phones to process sales transactions, customer orders, and daily operations, and to perform inventory management.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="8dc5e-119">コマース スケール ユニット</span><span class="sxs-lookup"><span data-stu-id="8dc5e-119">Commerce Scale Unit</span></span></td>
<td><span data-ttu-id="8dc5e-120">Commerce Scale Unit は、従業員と顧客の両方が情報にアクセスし、Retail POS クライアントとオンライン店舗の両方を使用してタスクを実行できるようにする、OData Web API を提供します。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-120">Commerce Scale Unit provides an OData web API that lets both employees and customers access information and perform tasks by using both Retail POS clients and the online store.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8dc5e-121">ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="8dc5e-121">Hardware Station</span></span></td>
<td><span data-ttu-id="8dc5e-122">Retail Hardware Station には、Retail POS クライアントと、プリンター、キャッシュ ドロワー、支払いデバイスなどの周辺基金が Commerce Scale Unit と通信できるようにするサービスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-122">Retail Hardware Station provides services that enable Retail POS clients, and peripherals such as printers, cash drawers, and payment devices to communicate with Commerce Scale Unit.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8dc5e-123">Retail Store Scale Unit</span><span class="sxs-lookup"><span data-stu-id="8dc5e-123">Retail Store Scale Unit</span></span></td>
<td><span data-ttu-id="8dc5e-124">Retail Store Scale Unit は、バック オフィスまたは本社 (HQ) への常時インターネット接続がない店舗で製品の販売をサポートする一連の機能です。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-124">Retail Store Scale Unit is a set of features that supports selling products in a store that does not have constant Internet connectivity to a back office or headquarters (HQ).</span></span> <span data-ttu-id="8dc5e-125">Store スケール ユニットは、店舗内の工程専用に設計されており、バック オフィスに接続していない場合でもターミナル間トランザクションおよびシフト操作が可能になります。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-125">The Store Scale Unit is designed specifically for in-store operation, and enables cross terminal transactions and shift operations even when you are not connected to the back office.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8dc5e-126">Retail Cloud Scale Unit</span><span class="sxs-lookup"><span data-stu-id="8dc5e-126">Retail Cloud Scale Unit</span></span></td>
<td><span data-ttu-id="8dc5e-127">Retail Cloud Scale Unit は、店頭または電子商取引においてコマース チャンネルの操作 (販売時点情報管理など) を可能にする一連のコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-127">Retail Cloud Scale Unit is a set of components that enables Commerce channel operations (such as point of sale operations) in a store or e-Commerce operation.</span></span> <span data-ttu-id="8dc5e-128">Retail Cloud Scale Unit には小売サーバー、コマース チャンネル データベース、および Cloud POS が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-128">Retail Cloud Scale Unit includes Retail Server, Commerce channel database, and Cloud POS.</span></span> <span data-ttu-id="8dc5e-129">Retail Cloud Scale Unit はMicrosoftによって提供、管理されています。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-129">Retail Cloud Scale Unit is hosted and managed by Microsoft.</span></span> <span data-ttu-id="8dc5e-130">Retail Cloud Scale Unit はクラウド ホスト型小売サーバー、コマース チャンネルのデータベース、および Cloud POS などの旧製品の改良版です。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-130">Retail Cloud Scale Unit supersedes the previous iteration of cloud-hosted Retail Server, Commerce channel database, and Cloud POS.</span></span></td>
<tr>
<td><span data-ttu-id="8dc5e-131">Commerce Runtime</span><span class="sxs-lookup"><span data-stu-id="8dc5e-131">Commerce runtime</span></span></td>
<td><span data-ttu-id="8dc5e-132">Commerce Runtime (CRT) は、さまざまなチャネル全体にビジネス ロジックをサポートするコア エンジンとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-132">Commerce runtime (CRT) serves as the core engine that supports the business logic across the various channels.</span></span> <span data-ttu-id="8dc5e-133">Commerce Runtime には、データ アクセス レイヤー、サービス レイヤー、ワークフロー レイヤーおよびアプリケーション プログラミング インターフェイス (API) レイヤーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-133">Commerce runtime contains a data access layer, services layer, workflow layer, and an application programming interface (API) layer.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8dc5e-134">チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="8dc5e-134">Channel database</span></span></td>
<td><span data-ttu-id="8dc5e-135">チャネル データベースは、オンライン ストアや従来型店舗など、1 つ以上のコマース チャネルのチャネル データを保持します。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-135">A channel database holds Channel data for one or more commerce channels, such as online stores or brick-and-mortar stores.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8dc5e-136">E コマース プラットフォーム SDK</span><span class="sxs-lookup"><span data-stu-id="8dc5e-136">e-Commerce platform SDK</span></span></td>
<td><span data-ttu-id="8dc5e-137">包括的な E コマース プラットフォームにより、プラットフォームのオムニチャネル サービスを利用できるフロントエンドのオンライン ストアにプラグインできます。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-137">The comprehensive e-Commerce platform lets you plug in a front-end online store that can take advantage of the omni-channel services of the platform.</span></span> <span data-ttu-id="8dc5e-138">ソフトウェア開発キット (SDK) は、プラットフォームをいかに活用できるかを示すサンプル オンライン ストアで構成されています。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-138">The software development kit (SDK) also consists of a sample online store that demonstrates how you can take advantage of the platform.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8dc5e-139">Retail SDK</span><span class="sxs-lookup"><span data-stu-id="8dc5e-139">Retail SDK</span></span></td>
<td><span data-ttu-id="8dc5e-140">Retail SDK には、サンプル ソース コードと、コマース システムをカスタマイズするために使用できるテンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8dc5e-140">The Retail SDK contains sample source code and templates that you can use to customize the Commerce system.</span></span></td>
</tr>
</tbody>
</table>

![システム アーキテクチャ](./media/Dynamics-365-for-Retail-System-Architecture.png)
