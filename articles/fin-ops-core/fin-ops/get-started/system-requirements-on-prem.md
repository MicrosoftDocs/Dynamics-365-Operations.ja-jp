---
title: オンプレミス配置のシステム要件
description: このトピックでは、オンプレミス配置のシステム要件を一覧表示します。
author: PeterRFriis
manager: AnnBe
ms.date: 01/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: perahlff
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: b2c99f7c0ab8528b377f15e09228fe63b6d60162
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077646"
---
# <a name="system-requirements-for-on-premises-deployments"></a><span data-ttu-id="025b1-103">オンプレミス配置のシステム要件</span><span class="sxs-lookup"><span data-stu-id="025b1-103">System requirements for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="025b1-104">このトピックは、現在のバージョンの Microsoft Dynamics 365 Finance + Operations (オンプレミス) 配置のシステム要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="025b1-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 Finance + Operations (on-premises) deployments.</span></span> <span data-ttu-id="025b1-105">インストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証します。</span><span class="sxs-lookup"><span data-stu-id="025b1-105">Before you install, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="025b1-106">Azure を含む、任意のパブリック クラウド インフラストラクチャでサポートされていない、Dynamics 365 Finance + Operations (オンプレミス) 配置。</span><span class="sxs-lookup"><span data-stu-id="025b1-106">Dynamics 365 Finance + Operations (on-premises) deployments are not supported on any public cloud infrastructure, including Azure.</span></span>

## <a name="network-requirements"></a><span data-ttu-id="025b1-107">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="025b1-107">Network requirements</span></span>

<span data-ttu-id="025b1-108">Dynamics 365 Finance + Operations (オンプレミス) は、インターネット プロトコル バージョン 4 (IPv4) またはインターネット プロトコル バージョン 6 (IPv6) を使用するネットワークで処理できます。</span><span class="sxs-lookup"><span data-stu-id="025b1-108">Dynamics 365 Finance + Operations (on-premises) can work on networks that use Internet Protocol Version 4 (IPv4) or Internet Protocol Version 6 (IPv6).</span></span> <span data-ttu-id="025b1-109">システムを計画して次のガイドラインを使用するには、ネットワーク環境を検討してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-109">Consider the network environment when you plan your system, and use the following guidelines.</span></span>

### <a name="network-response-time"></a><span data-ttu-id="025b1-110">ネットワークの応答時間</span><span class="sxs-lookup"><span data-stu-id="025b1-110">Network response time</span></span>

<span data-ttu-id="025b1-111">次の表では、Web ブラウザーと Application Object Server (AOS) の間の接続およびオンプレミス システムでの AOS とデータベースの間の接続のネットワークの最小要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="025b1-111">The following table lists the minimum network requirements for the connection between the web browser and Application Object Server (AOS), and for the connection between AOS and the database in an on-premises system.</span></span>

| <span data-ttu-id="025b1-112">先頭値</span><span class="sxs-lookup"><span data-stu-id="025b1-112">Value</span></span>     | <span data-ttu-id="025b1-113">Web ブラウザから AOS へ</span><span class="sxs-lookup"><span data-stu-id="025b1-113">Web browser to AOS</span></span>                      | <span data-ttu-id="025b1-114">AOS からデータベースへ</span><span class="sxs-lookup"><span data-stu-id="025b1-114">AOS to database</span></span>                                                                            |
|-----------|-----------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="025b1-115">帯域幅</span><span class="sxs-lookup"><span data-stu-id="025b1-115">Bandwidth</span></span> | <span data-ttu-id="025b1-116">ユーザーあたり毎秒 50 キロバイト (KBps)</span><span class="sxs-lookup"><span data-stu-id="025b1-116">50 kilobytes per second (KBps) per user</span></span> | <span data-ttu-id="025b1-117">毎秒 100 メガバイト (MBps)</span><span class="sxs-lookup"><span data-stu-id="025b1-117">100 megabytes per second (MBps)</span></span>                                                            |
| <span data-ttu-id="025b1-118">待機時間</span><span class="sxs-lookup"><span data-stu-id="025b1-118">Latency</span></span>   | <span data-ttu-id="025b1-119">250 ～ 300 ミリ秒 (ms) 未満</span><span class="sxs-lookup"><span data-stu-id="025b1-119">Less than 250–300 milliseconds (ms)</span></span>     | <span data-ttu-id="025b1-120">1 ミリ秒 (ローカル エリア ネットワーク \[LAN\] のみ) 未満。</span><span class="sxs-lookup"><span data-stu-id="025b1-120">Less than 1 ms (local area network \[LAN\] only).</span></span> <span data-ttu-id="025b1-121">AOS およびデータベースは、同一配置である必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-121">AOS and the database must be co-located.</span></span> |

- <span data-ttu-id="025b1-122">Finance + Operations は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="025b1-122">Finance + Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="025b1-123">この待機時間は、ブラウザー クライアントから Finance + Operations をホストするデータ センターまでの待機時間のことです。</span><span class="sxs-lookup"><span data-stu-id="025b1-123">This latency is the latency from a browser client to the datacenter that hosts Finance + Operations.</span></span>
- <span data-ttu-id="025b1-124">帯域幅の要件は、シナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="025b1-124">Bandwidth requirements depend on your scenario.</span></span> <span data-ttu-id="025b1-125">一般的なシナリオでは、ブラウザーおよびサーバーの間に 50 KBps 以上の帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="025b1-125">Typical scenarios require a bandwidth of more than 50 KBps between the browser and the server.</span></span> <span data-ttu-id="025b1-126">ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、より高い帯域幅を勧めます。</span><span class="sxs-lookup"><span data-stu-id="025b1-126">However, we recommend higher bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span> <span data-ttu-id="025b1-127">特定の帯域幅の量は、用途によって異なります。</span><span class="sxs-lookup"><span data-stu-id="025b1-127">The specific amount of bandwidth depends on use.</span></span>

<span data-ttu-id="025b1-128">AOS および Microsoft SQL Server データベースが異なるデータセンターにある配置はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="025b1-128">Deployments where AOS and the Microsoft SQL Server database are in different datacenters aren't supported.</span></span> <span data-ttu-id="025b1-129">AOS および SQL Server データベースは、同一配置である必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-129">AOS and the SQL Server database must be co-located.</span></span>

<span data-ttu-id="025b1-130">一般に、Finance + Operations は、ブラウザーからサーバーへのラウンド トリップを減らすために最適化されます。</span><span class="sxs-lookup"><span data-stu-id="025b1-130">In general, Finance + Operations is optimized to reduce browser-to-server round trips.</span></span> <span data-ttu-id="025b1-131">ブラウザー クライアントからデータセンターへのラウンド トリップの数は各ユーザーの操作ごとに 0 または 1 であり、全伝送データは圧縮されます。</span><span class="sxs-lookup"><span data-stu-id="025b1-131">The number of round trips from a browser client to the datacenter is either zero or one for each user interaction, and the payload is compressed.</span></span>

> [!WARNING]
> <span data-ttu-id="025b1-132">ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="025b1-132">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="025b1-133">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="025b1-133">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="025b1-134">特定のケースでのパフォーマンスの最良の指標として、非実稼働環境に対する実時間シミュレーションを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="025b1-134">We recommend that you use a real-life simulation against a non-production environment as the best gauge of performance for your specific case.</span></span>

### <a name="lan-environments"></a><span data-ttu-id="025b1-135">LAN 環境</span><span class="sxs-lookup"><span data-stu-id="025b1-135">LAN environments</span></span>

<span data-ttu-id="025b1-136">LAN 環境において、Microsoft Windows Server の Microsoft Remote Desktop は、Finance + Operations に接続する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="025b1-136">In LAN environments, Microsoft Remote Desktop in Microsoft Windows Server isn't required in order to connect to Finance + Operations.</span></span> <span data-ttu-id="025b1-137">ただし、Remote Desktop では、サーバーの配置を構成する仮想マシン (VMs) 上でのサービス操作に必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-137">However, Remote Desktop might be required for servicing operations on the virtual machines (VMs) that make up the server deployments.</span></span>

### <a name="wan-environments"></a><span data-ttu-id="025b1-138">WAN 環境</span><span class="sxs-lookup"><span data-stu-id="025b1-138">WAN environments</span></span>

<span data-ttu-id="025b1-139">広域ネットワーク (WAN) 環境において、Windows Server の Remote Desktop は、Finance + Operations に接続する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="025b1-139">In wide area network (WAN) environments, Remote Desktop in Windows Server isn't required in order to connect to Finance + Operations.</span></span>

### <a name="internet-connectivity-requirements"></a><span data-ttu-id="025b1-140">インターネット接続要件</span><span class="sxs-lookup"><span data-stu-id="025b1-140">Internet connectivity requirements</span></span>

<span data-ttu-id="025b1-141">Finance + Operations は、ユーザー ワークステーションからインターネットに接続する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="025b1-141">Finance + Operations doesn't require internet connectivity from user workstations.</span></span> <span data-ttu-id="025b1-142">ただし、一部の機能はインターネットに接続されていないと、利用できません。</span><span class="sxs-lookup"><span data-stu-id="025b1-142">However, some features won't be available if there is no internet connectivity.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="025b1-143"><strong>ブラウザー クライアント</strong></span><span class="sxs-lookup"><span data-stu-id="025b1-143"><strong>Browser client</strong></span></span></td>
<td><span data-ttu-id="025b1-144">インターネットに接続されていないイントラネット シナリオは、オンプレミス配置オプションの設計ポイントです。</span><span class="sxs-lookup"><span data-stu-id="025b1-144">An intranet scenario without internet connectivity is a design point for the on-premises deployment option.</span></span> <span data-ttu-id="025b1-145">Microsoft Dynamics Lifecycle Services (LCS) のヘルプおよびタスク ガイド ライブラリなどのクラウド サービスを必要とする一部の機能は、利用できません。</span><span class="sxs-lookup"><span data-stu-id="025b1-145">Some features that require cloud services won't be available, such as Help and Task guide libraries in Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="025b1-146"><strong>サーバー</strong></span><span class="sxs-lookup"><span data-stu-id="025b1-146"><strong>Server</strong></span></span></td>
<td><span data-ttu-id="025b1-147">AOS または Microsoft Azure Service Fabric 層は、LCS と通信できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-147">The AOS or Microsoft Azure Service Fabric tier must be able to communicate with LCS.</span></span> <span data-ttu-id="025b1-148">オンプレミス ブラウザーベースのクライアントには、インターネットへのアクセスは不要です。</span><span class="sxs-lookup"><span data-stu-id="025b1-148">The on-premises browser-based client doesn't require internet access.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="025b1-149"><strong>テレメトリ</strong></span><span class="sxs-lookup"><span data-stu-id="025b1-149"><strong>Telemetry</strong></span></span></td>
<td><span data-ttu-id="025b1-150">接続に長時間の障害があると、テレメトリ データが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-150">Telemetry data might be lost if there are long interruptions in connectivity.</span></span> <span data-ttu-id="025b1-151">LCS への接続の中断は、オンプレミスのアプリケーション機能に影響しません。</span><span class="sxs-lookup"><span data-stu-id="025b1-151">Interruptions in connectivity to LCS don't affect the on-premises application functionality.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="025b1-152"><strong>LCS</strong></span><span class="sxs-lookup"><span data-stu-id="025b1-152"><strong>LCS</strong></span></span></td>
<td><span data-ttu-id="025b1-153">配置、コードの配置、およびサービス操作には、LCS への接続が必要です。</span><span class="sxs-lookup"><span data-stu-id="025b1-153">Connectivity to LCS is required for deployment, code deployment, and servicing operations.</span></span></td>
</tr>
</tbody>
</table>

## <a name="telemetry-data-transfer-to-the-cloud"></a><span data-ttu-id="025b1-154">クラウドへのテレメトリ データの転送</span><span class="sxs-lookup"><span data-stu-id="025b1-154">Telemetry data transfer to the cloud</span></span>

<span data-ttu-id="025b1-155">ほとんどのテレメトリ データはローカルに保存され、Microsoft Windows のイベント ビューアーを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="025b1-155">Most telemetry data is stored locally and can be accessed by using Event Viewer in Microsoft Windows.</span></span> <span data-ttu-id="025b1-156">テレメトリ イベントの小さなサブセットは、診断のためにクラウド内の Microsoft テレメトリ パイプラインに転送されます。</span><span class="sxs-lookup"><span data-stu-id="025b1-156">A small subset of telemetry events is transferred to the Microsoft telemetry pipeline in the cloud for diagnostics.</span></span> <span data-ttu-id="025b1-157">顧客データおよびユーザー識別可能なデータは、Microsoft に送信されたテレメトリ データの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="025b1-157">Customer data and user-identifiable data aren't part of the telemetry data that is sent to Microsoft.</span></span> <span data-ttu-id="025b1-158">VM 名は、LCS ポータルからの環境管理および診断を支援するために、Microsoft へ送信されます。</span><span class="sxs-lookup"><span data-stu-id="025b1-158">VM names are sent to Microsoft to help with environment management and diagnostics from the LCS portal.</span></span>

## <a name="domain-requirements"></a><span data-ttu-id="025b1-159">ドメイン要件</span><span class="sxs-lookup"><span data-stu-id="025b1-159">Domain requirements</span></span>

<span data-ttu-id="025b1-160">Finance + Operations をインストールする場合は、次のドメイン要件を検討してください:</span><span class="sxs-lookup"><span data-stu-id="025b1-160">Consider the following domain requirements when you install Finance + Operations:</span></span>

- <span data-ttu-id="025b1-161">Finance + Operations コンポーネントをホストする VM は、Active Directory ドメインに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-161">VMs that host Finance + Operations components must belong to an Active Directory domain.</span></span> <span data-ttu-id="025b1-162">Active Directory Domain Services (AD DS) は、ネイティブ モードで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-162">Active Directory Domain Services (AD DS) must be configured in native mode.</span></span>
- <span data-ttu-id="025b1-163">Finance + Operations コンポーネントを実行する VM は、相互にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-163">VMs that run Finance + Operations components must have access to each other.</span></span> <span data-ttu-id="025b1-164">このアクセスは、AD DS で構成されています。</span><span class="sxs-lookup"><span data-stu-id="025b1-164">This access is configured in AD DS.</span></span>
- <span data-ttu-id="025b1-165">ドメイン コントローラは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-165">The domain controller must be Microsoft Windows Server 2012 R2 or later, and the domain functional level must be 2012 R2 or more.</span></span>

### <a name="full-2-way-trust"></a><span data-ttu-id="025b1-166">双方向の完全な信頼</span><span class="sxs-lookup"><span data-stu-id="025b1-166">Full 2-way trust</span></span>
<span data-ttu-id="025b1-167">Windows Server 2008 R2 ドメイン機能レベル (DFL) 上の会社のドメイン コントローラーと互換性を保つために、Windows Server 2008 R2 DFL ユーザー ドメインと Windows Server 2012 R2 DFL Finance + Operations サービス ドメインの間の双方向の完全な信頼は、プラットフォーム更新 33 以降でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="025b1-167">For compatibility with corporate domain controllers on Windows Server 2008 R2 domain functional level (DFL), a full 2-way trust between the Windows Server 2008 R2 DFL user domain and the Windows Server 2012 R2 DFL Finance + Operations service domain is supported in Platform update 33 and later.</span></span>

<span data-ttu-id="025b1-168">つまり、Finance + Operations (オンプレミス) アプリケーションのユーザーは、Windows Server 2008 R2 DFL メインから取得され、Finance + Operations (オンプレミス) インフラストラクチャとサービスをホストするリソースとサービス アカウントは Windows Server 2012 R2 DFL ドメインから取得されます。</span><span class="sxs-lookup"><span data-stu-id="025b1-168">This means that users of the Finance + Operations (on-premises) application will come from the Windows Server 2008 R2 DFL domain, and the resources and service accounts hosting the Finance + Operations (on-premises) infrastructure and services will come from the Windows Server 2012 R2 DFL domain.</span></span>

<span data-ttu-id="025b1-169">双方向の完全な信頼の設定の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="025b1-169">Examples for a full 2-way trust setup could be.</span></span>

<img src="./media/2WayTrust.png" width="700" hspace="50" alt="Examples of supported full 2-way trust between DFL versions"/>

#### <a name="known-limitations-with-using-the-full-2-way-trust-setup"></a><span data-ttu-id="025b1-170">双方向の完全な信頼設定を使用した場合の既知の制限</span><span class="sxs-lookup"><span data-stu-id="025b1-170">Known limitations with using the full 2-way trust setup</span></span>
* <span data-ttu-id="025b1-171">Windows Server 2008 R2 ユーザー ドメインからのセキュリティ グループのインポートはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="025b1-171">Import of security groups from the Windows Server 2008 R2 user domain is not supported.</span></span>

## <a name="hardware-requirements"></a><span data-ttu-id="025b1-172">ハードウェア要件</span><span class="sxs-lookup"><span data-stu-id="025b1-172">Hardware requirements</span></span>

<span data-ttu-id="025b1-173">このセクションでは、Finance + Operations の実行に必要なハードウェアについて説明します。</span><span class="sxs-lookup"><span data-stu-id="025b1-173">This section describes the hardware that is required in order to run Finance + Operations.</span></span>

<span data-ttu-id="025b1-174">システム構成、データ合成、および使用する機能に基づいて、実際のハードウェア要件は異なります。</span><span class="sxs-lookup"><span data-stu-id="025b1-174">The actual hardware requirements vary, based on the system configuration, the data composition, and the features that you decide to use.</span></span> <span data-ttu-id="025b1-175">適切なハードウェア選択に影響を与えるいくつかの要因を、以下に示します。</span><span class="sxs-lookup"><span data-stu-id="025b1-175">Here are some of the factors that can affect the choice of appropriate hardware:</span></span>

- <span data-ttu-id="025b1-176">時間あたりのトランザクション数</span><span class="sxs-lookup"><span data-stu-id="025b1-176">The number of transactions per hour</span></span>
- <span data-ttu-id="025b1-177">同時ユーザー数</span><span class="sxs-lookup"><span data-stu-id="025b1-177">The number of concurrent users</span></span>

## <a name="minimum-infrastructure-requirements"></a><span data-ttu-id="025b1-178">最小限のインフラストラクチャ要件</span><span class="sxs-lookup"><span data-stu-id="025b1-178">Minimum infrastructure requirements</span></span>

<span data-ttu-id="025b1-179">Finance + Operations では、Service Fabric を使用して、AOS、バッチ、データ管理、Management reporter、および環境オーケストレータ サービスをホストします。</span><span class="sxs-lookup"><span data-stu-id="025b1-179">Finance + Operations uses Service Fabric to host the AOS, Batch, Data management, Management reporter, and Environment orchestrator services.</span></span>

<span data-ttu-id="025b1-180">SQL Server は、生産用として少なくとも 2 つのノードを持つ高可用性 HADRON の設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="025b1-180">SQL Server must have a high-availability HADRON setup that has at least two nodes for production use.</span></span>

<span data-ttu-id="025b1-181">次の図は、Service Fabric クラスターのノードの最小推奨数を示しています。</span><span class="sxs-lookup"><span data-stu-id="025b1-181">The following illustration shows the minimum number of nodes that is recommended for your Service Fabric cluster.</span></span>

<span data-ttu-id="025b1-182">[![Service Fabric クラスターの推奨されるノード数](./media/Minimum-infrastructure-Jan2017.png)](./media/Minimum-infrastructure-Jan2017.png)</span><span class="sxs-lookup"><span data-stu-id="025b1-182">[![Recommended number of nodes for the Service Fabric cluster](./media/Minimum-infrastructure-Jan2017.png)](./media/Minimum-infrastructure-Jan2017.png)</span></span>

## <a name="processor-and-ram-requirements"></a><span data-ttu-id="025b1-183">プロセッサおよび RAM 要件</span><span class="sxs-lookup"><span data-stu-id="025b1-183">Processor and RAM requirements</span></span>

<span data-ttu-id="025b1-184">次の表では、この配置オプションを実行するために必要な役割ごとに求められるプロセッサの数およびランダムアクセス メモリ (RAM) の量を示します。</span><span class="sxs-lookup"><span data-stu-id="025b1-184">The following tables list the number of processors and the amount of random-access memory (RAM) that are required for each role that is required in order to run this deployment option.</span></span> <span data-ttu-id="025b1-185">詳細については、[Service Fabric クラスターの計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) の Service Fabric スタンドアロン クラスターに推奨する最小要件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-185">For more information, see the recommended minimum requirements for a Service Fabric standalone cluster in [Plan and prepare your Service Fabric cluster](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

> [!NOTE]
> <span data-ttu-id="025b1-186">その他の Microsoft ソフトウェアが同じコンピューターにインストールされている場合、システムはそのソフトウェアのハードウェア要件も満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-186">If other Microsoft software is installed on the same computer, the system must also comply with the hardware requirements for that software.</span></span> <span data-ttu-id="025b1-187">他のサーバー アプリケーションが AOS と同じコンピューターにインストールされている場合、これらのサーバー アプリケーションを RAM の 1 ギガバイト (GB) に制限することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="025b1-187">If other server applications are installed on the same computer as AOS, we recommend that you limit those server applications 1 gigabyte (GB) of RAM.</span></span>

<span data-ttu-id="025b1-188">**ロールおよびトポロジ タイプのサイズ変更**</span><span class="sxs-lookup"><span data-stu-id="025b1-188">**Sizing by role and topology type**</span></span>

| <span data-ttu-id="025b1-189">トポロジ</span><span class="sxs-lookup"><span data-stu-id="025b1-189">Topology</span></span>   | <span data-ttu-id="025b1-190">役割 (ノード タイプ)</span><span class="sxs-lookup"><span data-stu-id="025b1-190">Role (node type)</span></span>              | <span data-ttu-id="025b1-191">推奨されるプロセッサ コア</span><span class="sxs-lookup"><span data-stu-id="025b1-191">Recommended processor cores</span></span> | <span data-ttu-id="025b1-192">推奨メモリ (GB)</span><span class="sxs-lookup"><span data-stu-id="025b1-192">Recommended memory (GB)</span></span> |
|------------|-------------------------------|-----------------------------|-------------------------|
| <span data-ttu-id="025b1-193">生産</span><span class="sxs-lookup"><span data-stu-id="025b1-193">Production</span></span> | <span data-ttu-id="025b1-194">AOS,データ管理、バッチ</span><span class="sxs-lookup"><span data-stu-id="025b1-194">AOS, Data management, Batch</span></span>   | <span data-ttu-id="025b1-195">8</span><span class="sxs-lookup"><span data-stu-id="025b1-195">8</span></span>                           | <span data-ttu-id="025b1-196">24</span><span class="sxs-lookup"><span data-stu-id="025b1-196">24</span></span>                      |
|            | <span data-ttu-id="025b1-197">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="025b1-197">Management Reporter</span></span>           | <span data-ttu-id="025b1-198">4</span><span class="sxs-lookup"><span data-stu-id="025b1-198">4</span></span>                           | <span data-ttu-id="025b1-199">16</span><span class="sxs-lookup"><span data-stu-id="025b1-199">16</span></span>                      |
|            | <span data-ttu-id="025b1-200">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="025b1-200">SQL Server Reporting Services</span></span> | <span data-ttu-id="025b1-201">4</span><span class="sxs-lookup"><span data-stu-id="025b1-201">4</span></span>                           | <span data-ttu-id="025b1-202">16</span><span class="sxs-lookup"><span data-stu-id="025b1-202">16</span></span>                      |
|            | <span data-ttu-id="025b1-203">オーケストレータ</span><span class="sxs-lookup"><span data-stu-id="025b1-203">Orchestrator</span></span>                  | <span data-ttu-id="025b1-204">4</span><span class="sxs-lookup"><span data-stu-id="025b1-204">4</span></span>                           | <span data-ttu-id="025b1-205">16</span><span class="sxs-lookup"><span data-stu-id="025b1-205">16</span></span>                      |
|            | <span data-ttu-id="025b1-206">SQL Server</span><span class="sxs-lookup"><span data-stu-id="025b1-206">SQL Server</span></span>                    | <span data-ttu-id="025b1-207">8</span><span class="sxs-lookup"><span data-stu-id="025b1-207">8</span></span>                           | <span data-ttu-id="025b1-208">32</span><span class="sxs-lookup"><span data-stu-id="025b1-208">32</span></span>                      |
| <span data-ttu-id="025b1-209">サンドボックス</span><span class="sxs-lookup"><span data-stu-id="025b1-209">Sandbox</span></span>    | <span data-ttu-id="025b1-210">AOS,データ管理、バッチ</span><span class="sxs-lookup"><span data-stu-id="025b1-210">AOS, Data management, Batch</span></span>   | <span data-ttu-id="025b1-211">4</span><span class="sxs-lookup"><span data-stu-id="025b1-211">4</span></span>                           | <span data-ttu-id="025b1-212">24</span><span class="sxs-lookup"><span data-stu-id="025b1-212">24</span></span>                      |
|            | <span data-ttu-id="025b1-213">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="025b1-213">Management Reporter</span></span>           | <span data-ttu-id="025b1-214">4</span><span class="sxs-lookup"><span data-stu-id="025b1-214">4</span></span>                           | <span data-ttu-id="025b1-215">16</span><span class="sxs-lookup"><span data-stu-id="025b1-215">16</span></span>                      |
|            | <span data-ttu-id="025b1-216">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="025b1-216">SQL Server Reporting Services</span></span> | <span data-ttu-id="025b1-217">4</span><span class="sxs-lookup"><span data-stu-id="025b1-217">4</span></span>                           | <span data-ttu-id="025b1-218">16</span><span class="sxs-lookup"><span data-stu-id="025b1-218">16</span></span>                      |
|            | <span data-ttu-id="025b1-219">オーケストレータ</span><span class="sxs-lookup"><span data-stu-id="025b1-219">Orchestrator</span></span>                  | <span data-ttu-id="025b1-220">4</span><span class="sxs-lookup"><span data-stu-id="025b1-220">4</span></span>                           | <span data-ttu-id="025b1-221">16</span><span class="sxs-lookup"><span data-stu-id="025b1-221">16</span></span>                      |
|            | <span data-ttu-id="025b1-222">SQL Server</span><span class="sxs-lookup"><span data-stu-id="025b1-222">SQL Server</span></span>                    | <span data-ttu-id="025b1-223">8</span><span class="sxs-lookup"><span data-stu-id="025b1-223">8</span></span>                           | <span data-ttu-id="025b1-224">32</span><span class="sxs-lookup"><span data-stu-id="025b1-224">32</span></span>                      |

<span data-ttu-id="025b1-225">**生産およびサンド ボックス配置用の最小サイズ設定の見積**</span><span class="sxs-lookup"><span data-stu-id="025b1-225">**Minimum sizing estimates for production and sandbox deployments**</span></span>

| <span data-ttu-id="025b1-226">トポロジ</span><span class="sxs-lookup"><span data-stu-id="025b1-226">Topology</span></span>                                        | <span data-ttu-id="025b1-227">役割</span><span class="sxs-lookup"><span data-stu-id="025b1-227">Role</span></span>                          | <span data-ttu-id="025b1-228">インスタンスの数</span><span class="sxs-lookup"><span data-stu-id="025b1-228">Number of instances</span></span> |
|-------------------------------------------------|-------------------------------|---------------------|
| <span data-ttu-id="025b1-229">生産</span><span class="sxs-lookup"><span data-stu-id="025b1-229">Production</span></span>                                      | <span data-ttu-id="025b1-230">AOS (データ管理、バッチ)</span><span class="sxs-lookup"><span data-stu-id="025b1-230">AOS (Data management, Batch)</span></span>  | <span data-ttu-id="025b1-231">3</span><span class="sxs-lookup"><span data-stu-id="025b1-231">3</span></span>                   |
|                                                 | <span data-ttu-id="025b1-232">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="025b1-232">Management Reporter</span></span>           | <span data-ttu-id="025b1-233">2</span><span class="sxs-lookup"><span data-stu-id="025b1-233">2</span></span>                   |
|                                                 | <span data-ttu-id="025b1-234">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="025b1-234">SQL Server Reporting Services</span></span> | <span data-ttu-id="025b1-235">1</span><span class="sxs-lookup"><span data-stu-id="025b1-235">1</span></span>                   |
|                                                 | <span data-ttu-id="025b1-236">オーケストレータ\*\*</span><span class="sxs-lookup"><span data-stu-id="025b1-236">Orchestrator\*\*</span></span>              | <span data-ttu-id="025b1-237">3</span><span class="sxs-lookup"><span data-stu-id="025b1-237">3</span></span>                   |
|                                                 | <span data-ttu-id="025b1-238">SQL Server</span><span class="sxs-lookup"><span data-stu-id="025b1-238">SQL Server</span></span>                    | <span data-ttu-id="025b1-239">2</span><span class="sxs-lookup"><span data-stu-id="025b1-239">2</span></span>                   |
| <span data-ttu-id="025b1-240">サンドボックス</span><span class="sxs-lookup"><span data-stu-id="025b1-240">Sandbox</span></span>                                         | <span data-ttu-id="025b1-241">AOS,データ管理、バッチ</span><span class="sxs-lookup"><span data-stu-id="025b1-241">AOS, Data management, Batch</span></span>   | <span data-ttu-id="025b1-242">2</span><span class="sxs-lookup"><span data-stu-id="025b1-242">2</span></span>                   |
|                                                 | <span data-ttu-id="025b1-243">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="025b1-243">Management Reporter</span></span>           | <span data-ttu-id="025b1-244">1</span><span class="sxs-lookup"><span data-stu-id="025b1-244">1</span></span>                   |
|                                                 | <span data-ttu-id="025b1-245">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="025b1-245">SQL Server Reporting Services</span></span> | <span data-ttu-id="025b1-246">1</span><span class="sxs-lookup"><span data-stu-id="025b1-246">1</span></span>                   |
|                                                 | <span data-ttu-id="025b1-247">オーケストレータ</span><span class="sxs-lookup"><span data-stu-id="025b1-247">Orchestrator</span></span>                  | <span data-ttu-id="025b1-248">3</span><span class="sxs-lookup"><span data-stu-id="025b1-248">3</span></span>                   |
|                                                 | <span data-ttu-id="025b1-249">SQL Server</span><span class="sxs-lookup"><span data-stu-id="025b1-249">SQL Server</span></span>                    | <span data-ttu-id="025b1-250">1</span><span class="sxs-lookup"><span data-stu-id="025b1-250">1</span></span>                   |
| <span data-ttu-id="025b1-251">*生産とサンドボックス集計の概要ー*</span><span class="sxs-lookup"><span data-stu-id="025b1-251">*Summary for production and sandbox topologies*</span></span> |                               | <span data-ttu-id="025b1-252">*19*</span><span class="sxs-lookup"><span data-stu-id="025b1-252">*19*</span></span>                |

<span data-ttu-id="025b1-253">\*この表の数字は、プレビュー顧客によって検証されており、顧客からのフィードバックに基づいて調整されるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="025b1-253">\* The numbers in this table are being validated by our preview customers and might be adjusted based on the feedback from those customers.</span></span>

<span data-ttu-id="025b1-254">\*\* オーケストレータはプライマリ ノード タイプとして指定され、また Service Fabric サービスの実行にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="025b1-254">\*\* Orchestrator is designated as the primary node type and will also be used to run the Service Fabric services.</span></span>

<span data-ttu-id="025b1-255">**バック エンド SQL Server と AD DS の初期推定値**</span><span class="sxs-lookup"><span data-stu-id="025b1-255">**Initial estimates for the back-end SQL Server and AD DS**</span></span>

<table>
<thead>
<tr>
<th></th>
<th><span data-ttu-id="025b1-256">役割</span><span class="sxs-lookup"><span data-stu-id="025b1-256">Role</span></span></th>
<th><span data-ttu-id="025b1-257">VMs/ インスタンス</span><span class="sxs-lookup"><span data-stu-id="025b1-257">VMs/instances</span></span></th>
<th><span data-ttu-id="025b1-258">コア</span><span class="sxs-lookup"><span data-stu-id="025b1-258">Cores</span></span></th>
<th><span data-ttu-id="025b1-259">コア合計</span><span class="sxs-lookup"><span data-stu-id="025b1-259">Total cores</span></span></th>
<th><span data-ttu-id="025b1-260">インスタンス 16 GB あたりのメモリー</span><span class="sxs-lookup"><span data-stu-id="025b1-260">Memory per instance (GB)</span></span></th>
<th><span data-ttu-id="025b1-261">メモリー合計 (GB)</span><span class="sxs-lookup"><span data-stu-id="025b1-261">Total memory (GB)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><span data-ttu-id="025b1-262"><strong>共有インフラストラクチャ</strong></span><span class="sxs-lookup"><span data-stu-id="025b1-262"><strong>Shared infrastructure</strong></span></span></td>
<td><span data-ttu-id="025b1-263">SQL Server\*</span><span class="sxs-lookup"><span data-stu-id="025b1-263">SQL Server\*</span></span></td>
<td><span data-ttu-id="025b1-264">2</span><span class="sxs-lookup"><span data-stu-id="025b1-264">2</span></span></td>
<td><span data-ttu-id="025b1-265">8</span><span class="sxs-lookup"><span data-stu-id="025b1-265">8</span></span></td>
<td><span data-ttu-id="025b1-266">16</span><span class="sxs-lookup"><span data-stu-id="025b1-266">16</span></span></td>
<td><span data-ttu-id="025b1-267">32</span><span class="sxs-lookup"><span data-stu-id="025b1-267">32</span></span></td>
<td><span data-ttu-id="025b1-268">64</span><span class="sxs-lookup"><span data-stu-id="025b1-268">64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="025b1-269">ファイル サーバー / ストレージ エリア ネットワーク / 高可用性ストレージ</span><span class="sxs-lookup"><span data-stu-id="025b1-269">File server/Storage area network/Highly available storage</span></span></td>
<td colspan="5"><span data-ttu-id="025b1-270">バック エンド記憶域は、ランタイム ストレージ エリア ネットワーク (SAN) のソリッド ステート ドライブ (SSDs) に基づく必用があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-270">The back-end storage must be based on solid-state drives (SSDs) on a runtime storage area network (SAN).</span></span>
<p><span data-ttu-id="025b1-271">1 秒あたりのサイズと入力 / 出力オペレーション (IOPS) スループットは、ワークロードのサイズに基づきます。</span><span class="sxs-lookup"><span data-stu-id="025b1-271">Size and input/output operations per second (IOPS) throughput is based on the size of the workload.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="025b1-272">Active Directory</span><span class="sxs-lookup"><span data-stu-id="025b1-272">Active Directory</span></span></td>
<td><span data-ttu-id="025b1-273">3</span><span class="sxs-lookup"><span data-stu-id="025b1-273">3</span></span></td>
<td><span data-ttu-id="025b1-274">4</span><span class="sxs-lookup"><span data-stu-id="025b1-274">4</span></span></td>
<td><span data-ttu-id="025b1-275">12</span><span class="sxs-lookup"><span data-stu-id="025b1-275">12</span></span></td>
<td><span data-ttu-id="025b1-276">16</span><span class="sxs-lookup"><span data-stu-id="025b1-276">16</span></span></td>
<td><span data-ttu-id="025b1-277">48</span><span class="sxs-lookup"><span data-stu-id="025b1-277">48</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="025b1-278"><em>共有インフラストラクチャの概要</em></span><span class="sxs-lookup"><span data-stu-id="025b1-278"><em>Summary for shared infrastructure</em></span></span></td>
<td></td>
<td><span data-ttu-id="025b1-279"><em>5</em></span><span class="sxs-lookup"><span data-stu-id="025b1-279"><em>5</em></span></span></td>
<td></td>
<td><span data-ttu-id="025b1-280"><em>28</em></span><span class="sxs-lookup"><span data-stu-id="025b1-280"><em>28</em></span></span></td>
<td></td>
<td><span data-ttu-id="025b1-281"><em>112</em></span><span class="sxs-lookup"><span data-stu-id="025b1-281"><em>112</em></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="025b1-282">\*SQL Server サイズは、ワークロードに大きく依存します。</span><span class="sxs-lookup"><span data-stu-id="025b1-282">\* SQL Server sizes are highly dependent on workloads.</span></span> <span data-ttu-id="025b1-283">詳細については、[オンプレミス環境のハードウェアのサイズ変更要件](hardware-sizing-on-premises-environments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-283">For more information, see [Hardware sizing requirements for on-premises environments](hardware-sizing-on-premises-environments.md).</span></span> <span data-ttu-id="025b1-284">サンド ボックスと生産環境の 個別 SQL Server 機械を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-284">Separate SQL Server machines for sandbox and production environments must be used.</span></span> <span data-ttu-id="025b1-285">ただし、すべてのサンド ボックス環境で、SQL Server を共有できます。</span><span class="sxs-lookup"><span data-stu-id="025b1-285">However, SQL Server can be shared in all sandbox environments.</span></span>

## <a name="storage"></a><span data-ttu-id="025b1-286">保管</span><span class="sxs-lookup"><span data-stu-id="025b1-286">Storage</span></span>

- <span data-ttu-id="025b1-287">**AOS** - Finance + Operations を使用して、サーバー メッセージ ブロック (SMB) 3.0 共有に構造化されていないデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="025b1-287">**AOS** – Finance + Operations uses a Server Message Block (SMB) 3.0 share to store unstructured data.</span></span> <span data-ttu-id="025b1-288">詳細については、[Windows Server 2016 の Storage Spaces Direct](/windows-server/storage/storage-spaces/storage-spaces-direct-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-288">For more information, see [Storage Spaces Direct in Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).</span></span>
- <span data-ttu-id="025b1-289">**SQL** – 次のオプションは実行可能です。</span><span class="sxs-lookup"><span data-stu-id="025b1-289">**SQL** – The following options are viable:</span></span>

    - <span data-ttu-id="025b1-290">高可用性 SSD 設定</span><span class="sxs-lookup"><span data-stu-id="025b1-290">A highly available SSD setup</span></span>
    - <span data-ttu-id="025b1-291">オンライン トランザクション 処理 (OLTP) スループットに対して最適化された SAN</span><span class="sxs-lookup"><span data-stu-id="025b1-291">A SAN that is optimized for online transaction processing (OLTP) throughputs</span></span>
    - <span data-ttu-id="025b1-292">高パフォーマンス直接接続ストレージ (DAS)</span><span class="sxs-lookup"><span data-stu-id="025b1-292">High-performance direct-attached storage (DAS)</span></span>

- <span data-ttu-id="025b1-293">**SQL サーバーとデータの管理 IOPS** – データ管理と SQL Server の両方のストレージには、少なくとも 2,000 IOPS が必要です。</span><span class="sxs-lookup"><span data-stu-id="025b1-293">**SQL Server and data management IOPS** – The storage for both data management and SQL Server should have at least 2,000 IOPS.</span></span> <span data-ttu-id="025b1-294">生産 IOPS はさまざまな要因に依存します。</span><span class="sxs-lookup"><span data-stu-id="025b1-294">Production IOPS depends on many factors.</span></span> <span data-ttu-id="025b1-295">詳細については、[オンプレミス環境のハードウェアのサイズ変更要件](hardware-sizing-on-premises-environments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-295">For more information, see [Hardware sizing requirements for on-premises environments](hardware-sizing-on-premises-environments.md).</span></span>
- <span data-ttu-id="025b1-296">**VM IOPS** – 各 VM は少なくともt 100 書き込み IOPS が必要です。</span><span class="sxs-lookup"><span data-stu-id="025b1-296">**VM IOPS** – Each VM should have at least 100 write IOPS.</span></span>

## <a name="virtual-host-requirements"></a><span data-ttu-id="025b1-297">仮想ホストの要件</span><span class="sxs-lookup"><span data-stu-id="025b1-297">Virtual host requirements</span></span>

<span data-ttu-id="025b1-298">環境の仮想ホストを設定する場合は、[Service Fabric クラスターの計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) と [Service Fabric クラスターの説明](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description) のガイドラインを参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-298">When you set up the virtual hosts for an environment, see the guidelines in [Plan and prepare your Service Fabric cluster](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) and [Describing a service fabric cluster](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description).</span></span> <span data-ttu-id="025b1-299">各仮想ホストには、サイズ変更されているインフラストラクチャ用のコアが十分にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-299">Each virtual host should have enough cores for the infrastructure that is being sized.</span></span> <span data-ttu-id="025b1-300">SQL Server が物理ハードウェア上に存在し、その他のすべてが仮想化されている場合は、複数の高度な構成が可能です。</span><span class="sxs-lookup"><span data-stu-id="025b1-300">Multiple advanced configurations are possible, where SQL Server resides on physical hardware but everything else is virtualized.</span></span> <span data-ttu-id="025b1-301">SQL Server が仮想化されている場合、ディスク サブシステムは高速 SAN または同等のものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-301">If SQL Server is virtualized, the disk subsystem should be a fast SAN or the equivalent.</span></span> <span data-ttu-id="025b1-302">いずれの場合も、仮想ホストの基本設定が高可用性および重複であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-302">In all cases, make sure that the basic setup of the virtual host is highly available and redundant.</span></span> <span data-ttu-id="025b1-303">いずれの場合も、仮想化を使用する場合は、VM スナップショットを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="025b1-303">In all cases, when virtualization is used, no VM snapshots should be taken.</span></span>

<span data-ttu-id="025b1-304">Finance + Operations には、非 Microsoft 仮想化プラットフォーム (具体的には VMWare) での操作に関する Microsoft の標準サポート ポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="025b1-304">Finance + Operations falls under Microsoft's standard support policy regarding operation on non-Microsoft virtualization platforms – specifically VMWare.</span></span> <span data-ttu-id="025b1-305">詳細については、[Microsoft ソフトウェアのサポート ポリシー](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-305">For more information, read [Support policy for Microsoft software](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw).</span></span> <span data-ttu-id="025b1-306">つまり、この環境では製品をサポートしますが、問題の調査を依頼された場合、仮想化プラットフォームのない状態または Microsoft 仮想化プラットフォームで問題を再現するようまずお客様に依頼する場合があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-306">In short, we support our products in this environment, but if we are asked to investigate an issue, we may ask the customer to first reproduce the problem without the virtualization platform or on the Microsoft virtualization platform.</span></span>

## <a name="software-requirements-for-all-server-computers"></a><span data-ttu-id="025b1-307">すべてのサーバー コンピュータのソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="025b1-307">Software requirements for all server computers</span></span>

<span data-ttu-id="025b1-308">Finance + Operations コンポーネントをインストールする前に、次のソフトウェアがコンピュータに存在している必要があります:</span><span class="sxs-lookup"><span data-stu-id="025b1-308">The following software must be present on a computer before any Finance + Operations components can be installed:</span></span>

- <span data-ttu-id="025b1-309">Microsoft .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="025b1-309">The Microsoft .NET Framework.</span></span> <span data-ttu-id="025b1-310">バージョン情報については、[配置の設定](../../dev-itpro/deployment/setup-deploy-on-premises-pu12.md#setup)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-310">See [Deployment setup](../../dev-itpro/deployment/setup-deploy-on-premises-pu12.md#setup) for version information.</span></span>
- <span data-ttu-id="025b1-311">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="025b1-311">Service Fabric</span></span>

<span data-ttu-id="025b1-312">詳細については、[Service Fabric クラスターの計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-312">For more information, see [Plan and prepare your Service Fabric cluster](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

## <a name="supported-server-operating-systems"></a><span data-ttu-id="025b1-313">サポートされるサーバー オペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="025b1-313">Supported server operating systems</span></span>

<span data-ttu-id="025b1-314">次の表は、サポートされているサーバー オペレーティング システムの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="025b1-314">The following table lists the server operating systems that are supported.</span></span>

| <span data-ttu-id="025b1-315">オペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="025b1-315">Operating system</span></span>                                     | <span data-ttu-id="025b1-316">摘要</span><span class="sxs-lookup"><span data-stu-id="025b1-316">Notes</span></span> |
|------------------------------------------------------|-------|
| <span data-ttu-id="025b1-317">Microsoft Windows Server 2016 Datacenter または Standard</span><span class="sxs-lookup"><span data-stu-id="025b1-317">Microsoft Windows Server 2016 Datacenter or Standard</span></span> | <span data-ttu-id="025b1-318">これらの要件は、AOS をホストするデータベースおよび Service Fabric クラスターに対するものです。</span><span class="sxs-lookup"><span data-stu-id="025b1-318">These requirements are for the database and the Service Fabric cluster that hosts AOS.</span></span><p><span data-ttu-id="025b1-319">en-US OS インストールのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="025b1-319">Only en-US OS installations are supported.</span></span></p> |

## <a name="software-requirements-for-database-servers"></a><span data-ttu-id="025b1-320">データベース サーバーのソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="025b1-320">Software requirements for database servers</span></span>

- <span data-ttu-id="025b1-321">64 ビット バージョンの SQL Server 2016 のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="025b1-321">Only 64-bit versions of SQL Server 2016 are supported.</span></span>
- <span data-ttu-id="025b1-322">サーバーおよびデータベースの照合順序では、**SQL\_Latin1\_General\_CP1\_CI\_AS** のみ有効です。</span><span class="sxs-lookup"><span data-stu-id="025b1-322">Only **SQL\_Latin1\_General\_CP1\_CI\_AS** is valid for the server and database collation.</span></span> <span data-ttu-id="025b1-323">SQL Server データベースの照合順序を選択する方法の詳細については、「[SQL Server に関するドキュメント](/sql/sql-server/sql-server-technical-documentation)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-323">For more information about how to select a collation for a SQL Server database, see the [SQL Server documentation](/sql/sql-server/sql-server-technical-documentation).</span></span>
- <span data-ttu-id="025b1-324">実稼動環境では、使用している SQL Server のバージョンの最新の累積的な更新プログラム (CU) をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="025b1-324">In a production environment, we recommend that you install the latest cumulative update (CU) for the version of SQL Server that you're using.</span></span>

<span data-ttu-id="025b1-325">次の表では、データベースでサポートされている SQL Server バージョンを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="025b1-325">The following table lists the SQL Server versions that are supported for the databases.</span></span> <span data-ttu-id="025b1-326">詳細については、「[SQL Server](https://www.microsoft.com/sql-server/sql-server-2016) の最小ハードウェア要件」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-326">For more information, see the minimum hardware requirements for [SQL Server](https://www.microsoft.com/sql-server/sql-server-2016).</span></span>

| <span data-ttu-id="025b1-327">必要量</span><span class="sxs-lookup"><span data-stu-id="025b1-327">Requirement</span></span>                                                      | <span data-ttu-id="025b1-328">摘要</span><span class="sxs-lookup"><span data-stu-id="025b1-328">Notes</span></span> |
|------------------------------------------------------------------|-------|
| <span data-ttu-id="025b1-329">Microsoft SQL Server2016 Standard Edition または Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="025b1-329">Microsoft SQL Server 2016 Standard Edition or Enterprise Edition</span></span> | <span data-ttu-id="025b1-330">SQL Server 2016 のハードウェア要件については、「[SQL Server 2016 インストール用のハードウェアおよびソフトウェア要件](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-330">For the hardware requirements for SQL Server 2016, see [Hardware and Software Requirements for Installing SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server).</span></span> |

## <a name="software-requirements-for-application-object-server-aos"></a><span data-ttu-id="025b1-331">Application Object Server (AOS) のソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="025b1-331">Software requirements for Application Object Server (AOS)</span></span>

- <span data-ttu-id="025b1-332">SQL Server Integration Services (SSIS)</span><span class="sxs-lookup"><span data-stu-id="025b1-332">SQL Server Integration Services (SSIS)</span></span>

## <a name="software-requirements-for-reporting-server-bi"></a><span data-ttu-id="025b1-333">レポート サーバー (BI) のソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="025b1-333">Software requirements for Reporting Server (BI)</span></span>

- <span data-ttu-id="025b1-334">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="025b1-334">SQL Server Reporting Services (SSRS)</span></span>

## <a name="software-requirements-for-client-computers"></a><span data-ttu-id="025b1-335">クライアント コンピュータのソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="025b1-335">Software requirements for client computers</span></span>

<span data-ttu-id="025b1-336">ユーザーは、これらの一般的なブラウザの最新バージョンを使用して Finance + Operations にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="025b1-336">Users can access Finance + Operations by using the most recent versions of these popular browsers:</span></span>

- <span data-ttu-id="025b1-337">Microsoft Edge (推奨: [Chromium ベースの Edge](https://support.microsoft.com/microsoft-edge/download-the-new-microsoft-edge-based-on-chromium-0f4a3dd7-55df-60f5-739f-00010dba52cf))</span><span class="sxs-lookup"><span data-stu-id="025b1-337">Microsoft Edge (recommended: [Chromium-based Edge](https://support.microsoft.com/microsoft-edge/download-the-new-microsoft-edge-based-on-chromium-0f4a3dd7-55df-60f5-739f-00010dba52cf))</span></span>
- <span data-ttu-id="025b1-338">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="025b1-338">Google Chrome</span></span>
- <span data-ttu-id="025b1-339">Apple Safari</span><span class="sxs-lookup"><span data-stu-id="025b1-339">Apple Safari</span></span>
- <span data-ttu-id="025b1-340">Internet Explorer 11 (非推奨)</span><span class="sxs-lookup"><span data-stu-id="025b1-340">Internet Explorer 11 (deprecated, not recommended)</span></span>

> [!NOTE]
> <span data-ttu-id="025b1-341">パフォーマンスを最適化し、最適なエクスペリエンスを提供するために、最新のブラウザ、特に Microsoft Edge の最新バージョンを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="025b1-341">For optimal performance and an optimal experience, we recommend that you use the latest version of a modern browser, especially Microsoft Edge.</span></span> <span data-ttu-id="025b1-342">Internet Explorer 11 のサポートは非推奨です。</span><span class="sxs-lookup"><span data-stu-id="025b1-342">Support for Internet Explorer 11 is deprecated.</span></span> <span data-ttu-id="025b1-343">詳細については、[Internet Explorer 非推奨のお知らせ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/removed-deprecated-features-platform-updates#platform-updates-for-version-10015-of-finance-and-operations-apps)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-343">For more information, see the [Internet Explorer deprecation announcement](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/removed-deprecated-features-platform-updates#platform-updates-for-version-10015-of-finance-and-operations-apps).</span></span>

## <a name="software-requirements-for-active-directory-federation-services"></a><span data-ttu-id="025b1-344">Active Directory フェデレーション サービスのソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="025b1-344">Software requirements for Active Directory Federation Services</span></span>

<span data-ttu-id="025b1-345">Windows Server 2016 の Active Directory フェデレーション サービス (AD FS) は必要です。</span><span class="sxs-lookup"><span data-stu-id="025b1-345">Active Directory Federation Services (AD FS) on Windows Server 2016 is required.</span></span>

<span data-ttu-id="025b1-346">ドメイン コントローラは、Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-346">The domain controller must be Windows Server 2012 R2 or later, and the domain functional level must be 2012 R2 or more.</span></span> <span data-ttu-id="025b1-347">ドメイン機能レベルの詳細については、次のページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-347">For more information about domain functional levels, see the following pages:</span></span>

- <span data-ttu-id="025b1-348">[Active Directory 機能レベルとは](https://technet.microsoft.com/library/cc787290(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="025b1-348">[What Are Active Directory Functional Levels](https://technet.microsoft.com/library/cc787290(v=ws.10).aspx)</span></span>
- <span data-ttu-id="025b1-349">[Active Directory ドメイン サービス機能のレベルを理解する](https://technet.microsoft.com/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="025b1-349">[Understanding Active Directory Domain Services Functional Levels](https://technet.microsoft.com/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span></span>
- [<span data-ttu-id="025b1-350">双方向の完全な信頼</span><span class="sxs-lookup"><span data-stu-id="025b1-350">Full 2-way trust</span></span>](../../fin-ops/get-started/system-requirements-on-prem.md#full-2-way-trust)

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="025b1-351">サポートされる Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="025b1-351">Supported Microsoft Office applications</span></span>

<span data-ttu-id="025b1-352">次の Microsoft Office アプリケーションは、オンプレミス配置でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="025b1-352">The following Microsoft Office applications are supported in on-premises deployments:</span></span>

- <span data-ttu-id="025b1-353">Microsoft Excel と Microsoft Word のアドインを実行するには、Windows 用の Microsoft Office 2016 (またはそれ以降) をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-353">To run the Microsoft Excel and Microsoft Word add-ins, you must have Microsoft Office 2016 for Windows (or newer) installed.</span></span> <span data-ttu-id="025b1-354">バージョン要求の詳細については、[Office 統合に関するトラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025b1-354">For more information about version requirements, see [Troubleshoot the Office integration](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
- <span data-ttu-id="025b1-355">Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="025b1-355">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="hardware-and-software-requirements-for-commerce-components"></a><span data-ttu-id="025b1-356">コマース コンポーネントのハードウェアおよびソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="025b1-356">Hardware and software requirements for Commerce components</span></span>

<span data-ttu-id="025b1-357">現在、Finance + Operations はコマース コンポーネントを含んでいません。</span><span class="sxs-lookup"><span data-stu-id="025b1-357">Currently, Finance + Operations doesn't include the Commerce components.</span></span>
