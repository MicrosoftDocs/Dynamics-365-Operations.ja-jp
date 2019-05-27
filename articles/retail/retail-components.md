---
title: Retail のコンポーネント
description: このトピックは、Microsoft Dynamics 365 for Retail を構成するさまざまなコンポーネントについて説明します。
author: sericks007
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailITWorkspace
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 221954
ms.assetid: 8fe1b080-00d4-41ae-b047-10da160877ab
ms.search.region: Global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2261f17ad380c71ed0e1ce43ddbc8db9d5f3b793
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537072"
---
# <a name="retail-components"></a><span data-ttu-id="77b93-103">Retail のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="77b93-103">Retail components</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="77b93-104">このトピックは、Microsoft Dynamics 365 for Retail を構成するさまざまなコンポーネントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="77b93-104">This topic describes the various components that make up Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="77b93-105">Dynamics 365 for Retail は、中規模市場および大規模小売業者に、オンラインと従来型のストアのサポートを含む完全な本社および販売時点管理 (POS) ソリューションを提供します.</span><span class="sxs-lookup"><span data-stu-id="77b93-105">Dynamics 365 for Retail provides mid-market and large retailers with a complete head office and point of sale (POS) solution that includes support for online and brick-and-mortar stores.</span></span> <span data-ttu-id="77b93-106">小売業者が財務収益を高め、サービスを向上させ、成長を管理して、顧客に到達し、効率面を合理化できます。</span><span class="sxs-lookup"><span data-stu-id="77b93-106">It can help retailers increase financial returns, improve service, manage growth, reach customers, and streamline efficiencies.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="77b93-107">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="77b93-107">Component</span></span></th>
<th><span data-ttu-id="77b93-108">職務</span><span class="sxs-lookup"><span data-stu-id="77b93-108">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="77b93-109">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="77b93-109">Retail headquarters</span></span></td>
<td><span data-ttu-id="77b93-110">Dynamics 365 for Retail 用小売用バックオフィスを使用すると、一連の店舗を 1 つの企業として管理することができます。</span><span class="sxs-lookup"><span data-stu-id="77b93-110">Retail headquarters for Dynamics 365 for Retail can be used to manage a chain of stores as one enterprise.</span></span> <span data-ttu-id="77b93-111">これは、日々の業務を管理し、チェーンの全店舗の販売情報を追跡します。</span><span class="sxs-lookup"><span data-stu-id="77b93-111">It controls daily operations and tracks sales information for every store in the chain.</span></span> <span data-ttu-id="77b93-112">小売用スケジューラは、Dynamics 365 for Retail と店舗間の通信を調整します。</span><span class="sxs-lookup"><span data-stu-id="77b93-112">Retail Scheduler coordinates communication between Dynamics 365 for Retail and the stores.</span></span> <span data-ttu-id="77b93-113">小売用バックオフィスは、POS 、または必要なデータを受信して転送できるオンライン店舗システムで使用できます。</span><span class="sxs-lookup"><span data-stu-id="77b93-113">Retail headquarters can be used with any POS or online store system that can receive and transmit the required data.</span></span>
<blockquote>[!IMPORTANT] <span data-ttu-id="77b93-114">Dynamics 365 for Retail のカスタム POS またはオンライン ストア ソリューションの構築は、広範な計画、開発、およびテストが必要な複雑な作業です。</span><span class="sxs-lookup"><span data-stu-id="77b93-114">Building a custom POS or online store solution for Dynamics 365 for Retail is a complex task that requires extensive planning, development, and testing.</span></span></blockquote>
</td>
</tr>
<tr>
<td><span data-ttu-id="77b93-115">Retail POS</span><span class="sxs-lookup"><span data-stu-id="77b93-115">Retail POS</span></span></td>
<td><span data-ttu-id="77b93-116">Dynamics 365 for Retail では POS エクスペリエンスの 2 種類のイベントがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="77b93-116">Dynamics 365 for Retail supports two types of POS experience:</span></span>
<ul>
<li><span data-ttu-id="77b93-117"><strong>クラウド POS</strong> はブラウザベースの POS で、モバイルデバイスで使用できます。</span><span class="sxs-lookup"><span data-stu-id="77b93-117"><strong>Cloud POS</strong> is a browser-based POS that can be used on mobile devices.</span></span></li>
<li><span data-ttu-id="77b93-118"><strong>Retail Modern POS</strong> (MPOS) は、PC、タブレット、電話などのクライアントで、販売トランザクション、顧客注文、日常業務を処理し、在庫管理を実行するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="77b93-118"><strong>Retail Modern POS</strong> (MPOS) can be used on clients such as PCs, tablets, and phones to process sales transactions, customer orders, and daily operations, and to perform inventory management.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="77b93-119">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="77b93-119">Retail Server</span></span></td>
<td><span data-ttu-id="77b93-120">Retail サーバーは、従業員と顧客の両方が情報にアクセスし、Retail POS クライアントとオンライン店舗の両方を使用してタスクを実行できるようにする、OData Web API を提供します。</span><span class="sxs-lookup"><span data-stu-id="77b93-120">Retail Server provides an OData web API that lets both employees and customers access information and perform tasks by using both Retail POS clients and the online store.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="77b93-121">ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="77b93-121">Hardware Station</span></span></td>
<td><span data-ttu-id="77b93-122">Retail Hardware Station には、Retail POS クライアントと、プリンター、キャッシュ ドロワー、支払いデバイスなどの周辺基金が Retail Server と通信できるようにするサービスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="77b93-122">Retail Hardware Station provides services that enable Retail POS clients, and peripherals such as printers, cash drawers, and payment devices to communicate with Retail Server.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="77b93-123">Retail Store Scale Unit</span><span class="sxs-lookup"><span data-stu-id="77b93-123">Retail Store Scale Unit</span></span></td>
<td><span data-ttu-id="77b93-124">Retail Store Scale Unit は、バック オフィスまたは本社 (HQ) への常時インターネット接続がない店舗で製品の販売をサポートする一連の機能です。</span><span class="sxs-lookup"><span data-stu-id="77b93-124">Retail Store Scale Unit is a set of features that supports selling products in a store that does not have constant Internet connectivity to a back office or headquarters (HQ).</span></span> <span data-ttu-id="77b93-125">Store スケール ユニットは、店舗内の工程専用に設計されており、バック オフィスに接続していない場合でもターミナル間トランザクションおよびシフト操作が可能になります。</span><span class="sxs-lookup"><span data-stu-id="77b93-125">The Store Scale Unit is designed specifically for in-store operation, and enables cross terminal transactions and shift operations even when you are not connected to the back office.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="77b93-126">Retail Cloud Scale Unit</span><span class="sxs-lookup"><span data-stu-id="77b93-126">Retail Cloud Scale Unit</span></span></td>
<td><span data-ttu-id="77b93-127">Retail Cloud Scale Unit は、店頭または電子商取引において小売チャンネルの操作 (販売時点情報管理など) を可能にする一連のコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="77b93-127">Retail Cloud Scale Unit is a set of components that enables Retail channel operations (such as point of sale operations) in a store or e-Commerce operation.</span></span> <span data-ttu-id="77b93-128">Retail Cloud Scale Unit には小売サーバー、小売チャンネル データベース、およびクラウドPOSが含まれます。</span><span class="sxs-lookup"><span data-stu-id="77b93-128">Retail Cloud Scale Unit includes Retail Server, Retail channel database, and Cloud POS.</span></span> <span data-ttu-id="77b93-129">Retail Cloud Scale Unit はMicrosoftによって提供、管理されています。</span><span class="sxs-lookup"><span data-stu-id="77b93-129">Retail Cloud Scale Unit is hosted and managed by Microsoft.</span></span> <span data-ttu-id="77b93-130">Retail Cloud Scale Unit はクラウド ホスト型小売サーバー、小売チャンネルのデータベース、およびクラウドPOSなどの旧製品の改良版です。</span><span class="sxs-lookup"><span data-stu-id="77b93-130">Retail Cloud Scale Unit supersedes the previous iteration of cloud-hosted Retail Server, Retail channel database, and Cloud POS.</span></span></td>
<tr>
<td><span data-ttu-id="77b93-131">Commerce Runtime</span><span class="sxs-lookup"><span data-stu-id="77b93-131">Commerce runtime</span></span></td>
<td><span data-ttu-id="77b93-132">Commerce Runtime (CRT) は、さまざまなチャネル全体にビジネス ロジックをサポートするコア エンジンとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="77b93-132">Commerce runtime (CRT) serves as the core engine that supports the business logic across the various channels.</span></span> <span data-ttu-id="77b93-133">Commerce Runtime には、データ アクセス レイヤー、サービス レイヤー、ワークフロー レイヤーおよびアプリケーション プログラミング インターフェイス (API) レイヤーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="77b93-133">Commerce runtime contains a data access layer, services layer, workflow layer, and an application programming interface (API) layer.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="77b93-134">チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="77b93-134">Channel database</span></span></td>
<td><span data-ttu-id="77b93-135">チャンネル データベースは、オンライン ストアや従来型店舗など、1 つ以上の小売チャンネルの小売データを保持します。</span><span class="sxs-lookup"><span data-stu-id="77b93-135">A channel database holds Retail data for one or more retail channels, such as online stores or brick-and-mortar stores.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="77b93-136">E コマース プラットフォーム SDK</span><span class="sxs-lookup"><span data-stu-id="77b93-136">e-Commerce platform SDK</span></span></td>
<td><span data-ttu-id="77b93-137">包括的な E コマース プラットフォームにより、プラットフォームのオムニチャネル サービスを利用できるフロントエンドのオンライン ストアにプラグインできます。</span><span class="sxs-lookup"><span data-stu-id="77b93-137">The comprehensive e-Commerce platform lets you plug in a front-end online store that can take advantage of the omni-channel services of the platform.</span></span> <span data-ttu-id="77b93-138">ソフトウェア開発キット (SDK) は、プラットフォームをいかに活用できるかを示すサンプル オンライン ストアで構成されています。</span><span class="sxs-lookup"><span data-stu-id="77b93-138">The software development kit (SDK) also consists of a sample online store that demonstrates how you can take advantage of the platform.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="77b93-139">Retail SDK</span><span class="sxs-lookup"><span data-stu-id="77b93-139">Retail SDK</span></span></td>
<td><span data-ttu-id="77b93-140">Retail SDK には、サンプル ソース コードと、Retail システムをカスタマイズするために使用できるテンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="77b93-140">The Retail SDK contains sample source code and templates that you can use to customize the Retail system.</span></span></td>
</tr>
</tbody>
</table>

![SystemArchitecture](./media/Dynamics-365-for-Retail-System-Architecture.PNG)
