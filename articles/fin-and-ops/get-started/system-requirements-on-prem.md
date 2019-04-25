---
title: オンプレミス配置のシステム要件
description: このトピックは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations におけるオンプレミス展開のシステム要件を一覧表示します。
author: kfend
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 0e72bf2af7019e7328bad495bb18004090efc12c
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "858965"
---
# <a name="system-requirements-for-on-premises-deployments"></a><span data-ttu-id="92640-103">オンプレミス配置のシステム要件</span><span class="sxs-lookup"><span data-stu-id="92640-103">System requirements for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92640-104">このトピックは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations におけるオンプレミス展開のシステム要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="92640-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations for on-premises deployments.</span></span> <span data-ttu-id="92640-105">Finance and Operations をインストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証します。</span><span class="sxs-lookup"><span data-stu-id="92640-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92640-106">Azure を含む、任意のパブリック クラウド インフラストラクチャでサポートされていない、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置。</span><span class="sxs-lookup"><span data-stu-id="92640-106">On-premises deployments of Microsoft Dynamics 365 for Finance and Operations are not supported on any public cloud infrastructure, including Azure.</span></span>

## <a name="network-requirements"></a><span data-ttu-id="92640-107">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="92640-107">Network requirements</span></span>

<span data-ttu-id="92640-108">Microsoft Dynamics 365 for Finance and Operations (オンプレミス) は、インターネット プロトコル バージョン 4 (IPv4) またはインターネット プロトコル バージョン 6 (IPv6) を使用するネットワークで処理できます。</span><span class="sxs-lookup"><span data-stu-id="92640-108">Microsoft Dynamics 365 for Finance and Operations (on-premises) can work on networks that use Internet Protocol Version 4 (IPv4) or Internet Protocol Version 6 (IPv6).</span></span> <span data-ttu-id="92640-109">システムを計画して次のガイドラインを使用するには、ネットワーク環境を検討してください。</span><span class="sxs-lookup"><span data-stu-id="92640-109">Consider the network environment when you plan your system, and use the following guidelines.</span></span>

### <a name="network-response-time"></a><span data-ttu-id="92640-110">ネットワークの応答時間</span><span class="sxs-lookup"><span data-stu-id="92640-110">Network response time</span></span>

<span data-ttu-id="92640-111">次の表では、Web ブラウザーと Application Object Server (AOS) の間の接続およびオンプレミス システムでの AOS とデータベースの間の接続のネットワークの最小要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="92640-111">The following table lists the minimum network requirements for the connection between the web browser and Application Object Server (AOS), and for the connection between AOS and the database in an on-premises system.</span></span>

| <span data-ttu-id="92640-112">先頭値</span><span class="sxs-lookup"><span data-stu-id="92640-112">Value</span></span>     | <span data-ttu-id="92640-113">Web ブラウザから AOS へ</span><span class="sxs-lookup"><span data-stu-id="92640-113">Web browser to AOS</span></span>                      | <span data-ttu-id="92640-114">AOS からデータベースへ</span><span class="sxs-lookup"><span data-stu-id="92640-114">AOS to database</span></span>                                                                            |
|-----------|-----------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="92640-115">帯域幅</span><span class="sxs-lookup"><span data-stu-id="92640-115">Bandwidth</span></span> | <span data-ttu-id="92640-116">ユーザーあたり毎秒 50 キロバイト (KBps)</span><span class="sxs-lookup"><span data-stu-id="92640-116">50 kilobytes per second (KBps) per user</span></span> | <span data-ttu-id="92640-117">毎秒 100 メガバイト (MBps)</span><span class="sxs-lookup"><span data-stu-id="92640-117">100 megabytes per second (MBps)</span></span>                                                            |
| <span data-ttu-id="92640-118">待機時間</span><span class="sxs-lookup"><span data-stu-id="92640-118">Latency</span></span>   | <span data-ttu-id="92640-119">250 ～ 300 ミリ秒 (ms) 未満</span><span class="sxs-lookup"><span data-stu-id="92640-119">Less than 250–300 milliseconds (ms)</span></span>     | <span data-ttu-id="92640-120">1 ミリ秒 (ローカル エリア ネットワーク \[LAN\] のみ) 未満。</span><span class="sxs-lookup"><span data-stu-id="92640-120">Less than 1 ms (local area network \[LAN\] only).</span></span> <span data-ttu-id="92640-121">AOS およびデータベースは、同一配置である必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-121">AOS and the database must be co-located.</span></span> |

- <span data-ttu-id="92640-122">Finance and Operations (オンプレミス) は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="92640-122">Finance and Operations (on-premises) is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="92640-123">この待機時間は、ブラウザー クライアントから Finance and Operations をホストするデータ センターまでの待機時間のことです。</span><span class="sxs-lookup"><span data-stu-id="92640-123">This latency is the latency from a browser client to the datacenter that hosts Finance and Operations.</span></span>
- <span data-ttu-id="92640-124">Finance and Operations (オンプレミス) の帯域幅の要件はシナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="92640-124">Bandwidth requirements for Finance and Operations (on-premises) depend on your scenario.</span></span> <span data-ttu-id="92640-125">一般的なシナリオでは、ブラウザーおよび Finance and Operations サーバーの間に 1 秒あたり 50 KBps 以上の帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="92640-125">Typical scenarios require a bandwidth of more than 50 KBps between the browser and the Finance and Operations server.</span></span> <span data-ttu-id="92640-126">ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、より高い帯域幅を勧めます。</span><span class="sxs-lookup"><span data-stu-id="92640-126">However, we recommend higher bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span> <span data-ttu-id="92640-127">特定の帯域幅の量は、用途によって異なります。</span><span class="sxs-lookup"><span data-stu-id="92640-127">The specific amount of bandwidth depends on use.</span></span>

<span data-ttu-id="92640-128">AOS および Microsoft SQL Server データベースが異なるデータセンターにある配置はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="92640-128">Deployments where AOS and the Microsoft SQL Server database are in different datacenters aren't supported.</span></span> <span data-ttu-id="92640-129">AOS および SQL Server データベースは、同一配置である必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-129">AOS and the SQL Server database must be co-located.</span></span>

<span data-ttu-id="92640-130">一般に、Finance and Operations は、ブラウザーからサーバーへのラウンド トリップを減らすために最適化されます。</span><span class="sxs-lookup"><span data-stu-id="92640-130">In general, Finance and Operations is optimized to reduce browser-to-server round trips.</span></span> <span data-ttu-id="92640-131">ブラウザー クライアントからデータセンターへのラウンド トリップの数は各ユーザーの操作ごとに 0 または 1 であり、全伝送データは圧縮されます。</span><span class="sxs-lookup"><span data-stu-id="92640-131">The number of round trips from a browser client to the datacenter is either zero or one for each user interaction, and the payload is compressed.</span></span>

> [!WARNING]
> <span data-ttu-id="92640-132">ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="92640-132">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="92640-133">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="92640-133">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="92640-134">特定のケースでのパフォーマンスの最良の指標として、Finance and Operations 以外の環境に対する実時間シミュレーションを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="92640-134">We recommend that you use a real-life simulation against a non-production environment of Finance and Operations as the best gauge of performance for your specific case.</span></span>

### <a name="lan-environments"></a><span data-ttu-id="92640-135">LAN 環境</span><span class="sxs-lookup"><span data-stu-id="92640-135">LAN environments</span></span>

<span data-ttu-id="92640-136">LAN 環境において、Microsoft Windows Server の Microsoft Remote Desktop は、Finance and Operations に接続する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="92640-136">In LAN environments, Microsoft Remote Desktop in Microsoft Windows Server isn't required in order to connect to Finance and Operations.</span></span> <span data-ttu-id="92640-137">ただし、Remote Desktop では、サーバーの配置を構成する仮想マシン (VMs) 上でのサービス操作に必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="92640-137">However, Remote Desktop might be required for servicing operations on the virtual machines (VMs) that make up the server deployments.</span></span>

### <a name="wan-environments"></a><span data-ttu-id="92640-138">WAN 環境</span><span class="sxs-lookup"><span data-stu-id="92640-138">WAN environments</span></span>

<span data-ttu-id="92640-139">広域ネットワーク (WAN) 環境において、Windows Server の Remote Desktop は、Finance and Operations に接続する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="92640-139">In wide area network (WAN) environments, Remote Desktop in Windows Server isn't required in order to connect to Finance and Operations.</span></span>

### <a name="internet-connectivity-requirements"></a><span data-ttu-id="92640-140">インターネット接続要件</span><span class="sxs-lookup"><span data-stu-id="92640-140">Internet connectivity requirements</span></span>

<span data-ttu-id="92640-141">Finance and Operations (オンプレミス) は、ユーザー ワークステーションからインターネットに接続する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="92640-141">Finance and Operations (on-premises) doesn't require internet connectivity from user workstations.</span></span> <span data-ttu-id="92640-142">ただし、一部の機能はインターネットに接続されていないと、利用できません。</span><span class="sxs-lookup"><span data-stu-id="92640-142">However, some features won't be available if there is no internet connectivity.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="92640-143"><strong>ブラウザー クライアント</strong></span><span class="sxs-lookup"><span data-stu-id="92640-143"><strong>Browser client</strong></span></span></td>
<td><span data-ttu-id="92640-144">インターネットに接続されていないイントラネット シナリオは、オンプレミス配置オプションの設計ポイントです。</span><span class="sxs-lookup"><span data-stu-id="92640-144">An intranet scenario without internet connectivity is a design point for the on-premises deployment option.</span></span> <span data-ttu-id="92640-145">Microsoft Dynamics Lifecycle Services (LCS) のヘルプおよびタスク ガイド ライブラリなどのクラウド サービスを必要とする一部の機能は、利用できません。</span><span class="sxs-lookup"><span data-stu-id="92640-145">Some features that require cloud services won't be available, such as Help and Task guide libraries in Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92640-146"><strong>サーバー</strong></span><span class="sxs-lookup"><span data-stu-id="92640-146"><strong>Server</strong></span></span></td>
<td><span data-ttu-id="92640-147">AOS または Microsoft Azure Service Fabric 層は、LCS と通信できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-147">The AOS or Microsoft Azure Service Fabric tier must be able to communicate with LCS.</span></span> <span data-ttu-id="92640-148">オンプレミス ブラウザーベースのクライアントには、インターネットへのアクセスは不要です。</span><span class="sxs-lookup"><span data-stu-id="92640-148">The on-premises browser-based client doesn't require internet access.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92640-149"><strong>テレメトリ</strong></span><span class="sxs-lookup"><span data-stu-id="92640-149"><strong>Telemetry</strong></span></span></td>
<td><span data-ttu-id="92640-150">接続に長時間の障害があると、テレメトリ データが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="92640-150">Telemetry data might be lost if there are long interruptions in connectivity.</span></span> <span data-ttu-id="92640-151">LCS への接続の中断は、オンプレミスのアプリケーション機能に影響しません。</span><span class="sxs-lookup"><span data-stu-id="92640-151">Interruptions in connectivity to LCS don't affect the on-premises application functionality.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92640-152"><strong>LCS</strong></span><span class="sxs-lookup"><span data-stu-id="92640-152"><strong>LCS</strong></span></span></td>
<td><span data-ttu-id="92640-153">配置、コードの配置、およびサービス操作には、LCS への接続が必要です。</span><span class="sxs-lookup"><span data-stu-id="92640-153">Connectivity to LCS is required for deployment, code deployment, and servicing operations.</span></span></td>
</tr>
</tbody>
</table>

## <a name="telemetry-data-transfer-to-the-cloud"></a><span data-ttu-id="92640-154">クラウドへのテレメトリ データの転送</span><span class="sxs-lookup"><span data-stu-id="92640-154">Telemetry data transfer to the cloud</span></span>

<span data-ttu-id="92640-155">ほとんどのテレメトリ データはローカルに保存され、Microsoft Windows のイベント ビューアーを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="92640-155">Most telemetry data is stored locally and can be accessed by using Event Viewer in Microsoft Windows.</span></span> <span data-ttu-id="92640-156">テレメトリ イベントの小さなサブセットは、診断のためにクラウド内の Microsoft テレメトリ パイプラインに転送されます。</span><span class="sxs-lookup"><span data-stu-id="92640-156">A small subset of telemetry events is transferred to the Microsoft telemetry pipeline in the cloud for diagnostics.</span></span> <span data-ttu-id="92640-157">顧客データおよびユーザー識別可能なデータは、Microsoft に送信されたテレメトリ データの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="92640-157">Customer data and user-identifiable data aren't part of the telemetry data that is sent to Microsoft.</span></span> <span data-ttu-id="92640-158">VM 名は、LCS ポータルからの環境管理および診断を支援するために、Microsoft へ送信されます。</span><span class="sxs-lookup"><span data-stu-id="92640-158">VM names are sent to Microsoft to help with environment management and diagnostics from the LCS portal.</span></span>

## <a name="domain-requirements"></a><span data-ttu-id="92640-159">ドメイン要件</span><span class="sxs-lookup"><span data-stu-id="92640-159">Domain requirements</span></span>

<span data-ttu-id="92640-160">Finance and Operations (オンプレミス) をインストールする場合は、次のドメイン要件を検討してください:</span><span class="sxs-lookup"><span data-stu-id="92640-160">Consider the following domain requirements when you install Finance and Operations (on-premises):</span></span>

- <span data-ttu-id="92640-161">Finance and Operations (オンプレミス) コンポーネントをホストする VMs は、Active Directory ドメインに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-161">VMs that host Finance and Operations (on-premises) components must belong to an Active Directory domain.</span></span> <span data-ttu-id="92640-162">Active Directory ドメイン サービス (AD DS) は、ネイティブ モードで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-162">Active Directory Domain Services (AD DS) must be configured in native mode.</span></span>
- <span data-ttu-id="92640-163">Finance and Operations (オンプレミス) コンポーネントを実行する VMs は、相互にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-163">VMs that run Finance and Operations (on-premises) components must have access to each other.</span></span> <span data-ttu-id="92640-164">このアクセスは、AD DS で設定されています。</span><span class="sxs-lookup"><span data-stu-id="92640-164">This access is configured in AD DS.</span></span>
- <span data-ttu-id="92640-165">ドメイン コントローラは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-165">The domain controller must be Microsoft Windows Server 2012 R2 or later, and the domain functional level must be 2012 R2 or more.</span></span>

## <a name="hardware-requirements"></a><span data-ttu-id="92640-166">ハードウェア要件</span><span class="sxs-lookup"><span data-stu-id="92640-166">Hardware requirements</span></span>

<span data-ttu-id="92640-167">このセクションでは、Finance and Operations (オンプレミス) の実行に必要なハードウェアについて説明します。</span><span class="sxs-lookup"><span data-stu-id="92640-167">This section describes the hardware that is required in order to run Finance and Operations (on-premises).</span></span>

<span data-ttu-id="92640-168">システム構成、データ合成、および使用するアプリケーションと機能に基づいて、実際のハードウェア要件は異なります。</span><span class="sxs-lookup"><span data-stu-id="92640-168">The actual hardware requirements vary, based on the system configuration, the data composition, and the applications and features that you decide to use.</span></span> <span data-ttu-id="92640-169">Finance and Operations (オンプレミス) のための適切なハードウェア選択に影響を与えるいくつかの要因を、以下に示します。</span><span class="sxs-lookup"><span data-stu-id="92640-169">Here are some of the factors that can affect the choice of appropriate hardware for Finance and Operations (on-premises):</span></span>

- <span data-ttu-id="92640-170">時間あたりのトランザクション数</span><span class="sxs-lookup"><span data-stu-id="92640-170">The number of transactions per hour</span></span>
- <span data-ttu-id="92640-171">同時ユーザー数</span><span class="sxs-lookup"><span data-stu-id="92640-171">The number of concurrent users</span></span>

## <a name="minimum-infrastructure-requirements"></a><span data-ttu-id="92640-172">最小限のインフラストラクチャ要件</span><span class="sxs-lookup"><span data-stu-id="92640-172">Minimum infrastructure requirements</span></span>

<span data-ttu-id="92640-173">Finance and Operations (オンプレミス) では、Service Fabric を使用して、AOS、バッチ、データ管理、Management reporter、および環境オーケストレータ サービスをホストします。</span><span class="sxs-lookup"><span data-stu-id="92640-173">Finance and Operations (on-premises) uses Service Fabric to host the AOS, Batch, Data management, Management reporter, and Environment orchestrator services.</span></span>

<span data-ttu-id="92640-174">SQL Server は、生産用として少なくとも 2 つのノードを持つ高可用性 HADRON の設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="92640-174">SQL Server must have a high-availability HADRON setup that has at least two nodes for production use.</span></span>

<span data-ttu-id="92640-175">次の図は、Service Fabric クラスターのノードの最小推奨数を示しています。</span><span class="sxs-lookup"><span data-stu-id="92640-175">The following illustration shows the minimum number of nodes that is recommended for your Service Fabric cluster.</span></span>

<span data-ttu-id="92640-176">[![Service Fabric クラスターの推奨されるノード数](./media/Minimum-infrastructure-Jan2017.png)](./media/Minimum-infrastructure-Jan2017.png)</span><span class="sxs-lookup"><span data-stu-id="92640-176">[![Recommended number of nodes for the Service Fabric cluster](./media/Minimum-infrastructure-Jan2017.png)](./media/Minimum-infrastructure-Jan2017.png)</span></span>

## <a name="processor-and-ram-requirements"></a><span data-ttu-id="92640-177">プロセッサおよび RAM 要件</span><span class="sxs-lookup"><span data-stu-id="92640-177">Processor and RAM requirements</span></span>

<span data-ttu-id="92640-178">次の表では、この配置オプションを実行するために必要な役割ごとに求められるプロセッサの数およびランダムアクセス メモリ (RAM) の量を示します。</span><span class="sxs-lookup"><span data-stu-id="92640-178">The following tables list the number of processors and the amount of random-access memory (RAM) that are required for each role that is required in order to run this deployment option.</span></span> <span data-ttu-id="92640-179">詳細については、[Service Fabric クラスターの計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) の Service Fabric スタンドアロン クラスターに推奨する最小要件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-179">For more information, see the recommended minimum requirements for a Service Fabric standalone cluster in [Plan and prepare your Service Fabric cluster](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

> [!NOTE]
> <span data-ttu-id="92640-180">その他の Microsoft ソフトウェアが同じコンピューターにインストールされている場合、システムはそのソフトウェアのハードウェア要件も満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-180">If other Microsoft software is installed on the same computer, the system must also comply with the hardware requirements for that software.</span></span> <span data-ttu-id="92640-181">他のサーバー アプリケーションが AOS と同じコンピューターにインストールされている場合、これらのサーバー アプリケーションを 1 ギガバイト (GB) の RAM に制限することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="92640-181">If other server applications are installed on the same computer as AOS, we recommend that you limit those server applications 1 gigabyte (GB) of RAM.</span></span>

<span data-ttu-id="92640-182">**ロールおよびトポロジ タイプのサイズ変更**</span><span class="sxs-lookup"><span data-stu-id="92640-182">**Sizing by role and topology type**</span></span>

| <span data-ttu-id="92640-183">トポロジ</span><span class="sxs-lookup"><span data-stu-id="92640-183">Topology</span></span>   | <span data-ttu-id="92640-184">役割 (ノード タイプ)</span><span class="sxs-lookup"><span data-stu-id="92640-184">Role (node type)</span></span>              | <span data-ttu-id="92640-185">推奨されるプロセッサ コア</span><span class="sxs-lookup"><span data-stu-id="92640-185">Recommended processor cores</span></span> | <span data-ttu-id="92640-186">推奨メモリ (GB)</span><span class="sxs-lookup"><span data-stu-id="92640-186">Recommended memory (GB)</span></span> |
|------------|-------------------------------|-----------------------------|-------------------------|
| <span data-ttu-id="92640-187">生産</span><span class="sxs-lookup"><span data-stu-id="92640-187">Production</span></span> | <span data-ttu-id="92640-188">AOS,データ管理、バッチ</span><span class="sxs-lookup"><span data-stu-id="92640-188">AOS, Data management, Batch</span></span>   | <span data-ttu-id="92640-189">8</span><span class="sxs-lookup"><span data-stu-id="92640-189">8</span></span>                           | <span data-ttu-id="92640-190">24</span><span class="sxs-lookup"><span data-stu-id="92640-190">24</span></span>                      |
|            | <span data-ttu-id="92640-191">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="92640-191">Management Reporter</span></span>           | <span data-ttu-id="92640-192">4</span><span class="sxs-lookup"><span data-stu-id="92640-192">4</span></span>                           | <span data-ttu-id="92640-193">16</span><span class="sxs-lookup"><span data-stu-id="92640-193">16</span></span>                      |
|            | <span data-ttu-id="92640-194">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="92640-194">SQL Server Reporting Services</span></span> | <span data-ttu-id="92640-195">4</span><span class="sxs-lookup"><span data-stu-id="92640-195">4</span></span>                           | <span data-ttu-id="92640-196">16</span><span class="sxs-lookup"><span data-stu-id="92640-196">16</span></span>                      |
|            | <span data-ttu-id="92640-197">オーケストレータ</span><span class="sxs-lookup"><span data-stu-id="92640-197">Orchestrator</span></span>                  | <span data-ttu-id="92640-198">4</span><span class="sxs-lookup"><span data-stu-id="92640-198">4</span></span>                           | <span data-ttu-id="92640-199">16</span><span class="sxs-lookup"><span data-stu-id="92640-199">16</span></span>                      |
|            | <span data-ttu-id="92640-200">SQL Server</span><span class="sxs-lookup"><span data-stu-id="92640-200">SQL Server</span></span>                    | <span data-ttu-id="92640-201">8</span><span class="sxs-lookup"><span data-stu-id="92640-201">8</span></span>                           | <span data-ttu-id="92640-202">32</span><span class="sxs-lookup"><span data-stu-id="92640-202">32</span></span>                      |
| <span data-ttu-id="92640-203">サンドボックス</span><span class="sxs-lookup"><span data-stu-id="92640-203">Sandbox</span></span>    | <span data-ttu-id="92640-204">AOS,データ管理、バッチ</span><span class="sxs-lookup"><span data-stu-id="92640-204">AOS, Data management, Batch</span></span>   | <span data-ttu-id="92640-205">4</span><span class="sxs-lookup"><span data-stu-id="92640-205">4</span></span>                           | <span data-ttu-id="92640-206">24</span><span class="sxs-lookup"><span data-stu-id="92640-206">24</span></span>                      |
|            | <span data-ttu-id="92640-207">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="92640-207">Management Reporter</span></span>           | <span data-ttu-id="92640-208">4</span><span class="sxs-lookup"><span data-stu-id="92640-208">4</span></span>                           | <span data-ttu-id="92640-209">16</span><span class="sxs-lookup"><span data-stu-id="92640-209">16</span></span>                      |
|            | <span data-ttu-id="92640-210">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="92640-210">SQL Server Reporting Services</span></span> | <span data-ttu-id="92640-211">4</span><span class="sxs-lookup"><span data-stu-id="92640-211">4</span></span>                           | <span data-ttu-id="92640-212">16</span><span class="sxs-lookup"><span data-stu-id="92640-212">16</span></span>                      |
|            | <span data-ttu-id="92640-213">オーケストレータ</span><span class="sxs-lookup"><span data-stu-id="92640-213">Orchestrator</span></span>                  | <span data-ttu-id="92640-214">4</span><span class="sxs-lookup"><span data-stu-id="92640-214">4</span></span>                           | <span data-ttu-id="92640-215">16</span><span class="sxs-lookup"><span data-stu-id="92640-215">16</span></span>                      |
|            | <span data-ttu-id="92640-216">SQL Server</span><span class="sxs-lookup"><span data-stu-id="92640-216">SQL Server</span></span>                    | <span data-ttu-id="92640-217">8</span><span class="sxs-lookup"><span data-stu-id="92640-217">8</span></span>                           | <span data-ttu-id="92640-218">32</span><span class="sxs-lookup"><span data-stu-id="92640-218">32</span></span>                      |

<span data-ttu-id="92640-219">**生産およびサンド ボックス配置用の最小サイズ設定の見積**</span><span class="sxs-lookup"><span data-stu-id="92640-219">**Minimum sizing estimates for production and sandbox deployments**</span></span>

| <span data-ttu-id="92640-220">トポロジ</span><span class="sxs-lookup"><span data-stu-id="92640-220">Topology</span></span>                                        | <span data-ttu-id="92640-221">役割</span><span class="sxs-lookup"><span data-stu-id="92640-221">Role</span></span>                          | <span data-ttu-id="92640-222">インスタンスの数</span><span class="sxs-lookup"><span data-stu-id="92640-222">Number of instances</span></span> |
|-------------------------------------------------|-------------------------------|---------------------|
| <span data-ttu-id="92640-223">生産</span><span class="sxs-lookup"><span data-stu-id="92640-223">Production</span></span>                                      | <span data-ttu-id="92640-224">AOS (データ管理、バッチ)</span><span class="sxs-lookup"><span data-stu-id="92640-224">AOS (Data management, Batch)</span></span>  | <span data-ttu-id="92640-225">3</span><span class="sxs-lookup"><span data-stu-id="92640-225">3</span></span>                   |
|                                                 | <span data-ttu-id="92640-226">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="92640-226">Management Reporter</span></span>           | <span data-ttu-id="92640-227">2</span><span class="sxs-lookup"><span data-stu-id="92640-227">2</span></span>                   |
|                                                 | <span data-ttu-id="92640-228">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="92640-228">SQL Server Reporting Services</span></span> | <span data-ttu-id="92640-229">1</span><span class="sxs-lookup"><span data-stu-id="92640-229">1</span></span>                   |
|                                                 | <span data-ttu-id="92640-230">オーケストレータ\*\*</span><span class="sxs-lookup"><span data-stu-id="92640-230">Orchestrator\*\*</span></span>              | <span data-ttu-id="92640-231">3</span><span class="sxs-lookup"><span data-stu-id="92640-231">3</span></span>                   |
|                                                 | <span data-ttu-id="92640-232">SQL Server</span><span class="sxs-lookup"><span data-stu-id="92640-232">SQL Server</span></span>                    | <span data-ttu-id="92640-233">2</span><span class="sxs-lookup"><span data-stu-id="92640-233">2</span></span>                   |
| <span data-ttu-id="92640-234">サンドボックス</span><span class="sxs-lookup"><span data-stu-id="92640-234">Sandbox</span></span>                                         | <span data-ttu-id="92640-235">AOS,データ管理、バッチ</span><span class="sxs-lookup"><span data-stu-id="92640-235">AOS, Data management, Batch</span></span>   | <span data-ttu-id="92640-236">2</span><span class="sxs-lookup"><span data-stu-id="92640-236">2</span></span>                   |
|                                                 | <span data-ttu-id="92640-237">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="92640-237">Management Reporter</span></span>           | <span data-ttu-id="92640-238">1</span><span class="sxs-lookup"><span data-stu-id="92640-238">1</span></span>                   |
|                                                 | <span data-ttu-id="92640-239">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="92640-239">SQL Server Reporting Services</span></span> | <span data-ttu-id="92640-240">1</span><span class="sxs-lookup"><span data-stu-id="92640-240">1</span></span>                   |
|                                                 | <span data-ttu-id="92640-241">オーケストレータ</span><span class="sxs-lookup"><span data-stu-id="92640-241">Orchestrator</span></span>                  | <span data-ttu-id="92640-242">3</span><span class="sxs-lookup"><span data-stu-id="92640-242">3</span></span>                   |
|                                                 | <span data-ttu-id="92640-243">SQL Server</span><span class="sxs-lookup"><span data-stu-id="92640-243">SQL Server</span></span>                    | <span data-ttu-id="92640-244">1</span><span class="sxs-lookup"><span data-stu-id="92640-244">1</span></span>                   |
| <span data-ttu-id="92640-245">*生産とサンドボックス集計の概要ー*</span><span class="sxs-lookup"><span data-stu-id="92640-245">*Summary for production and sandbox topologies*</span></span> |                               | <span data-ttu-id="92640-246">*19*</span><span class="sxs-lookup"><span data-stu-id="92640-246">*19*</span></span>                |

<span data-ttu-id="92640-247">\*この表の数字は、プレビュー顧客によって検証されており、顧客からのフィードバックに基づいて調整されるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="92640-247">\* The numbers in this table are being validated by our preview customers and might be adjusted based on the feedback from those customers.</span></span>

<span data-ttu-id="92640-248">\*\* オーケストレータはプライマリ ノード タイプとして指定され、また Service Fabric サービスの実行にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="92640-248">\*\* Orchestrator is designated as the primary node type and will also be used to run the Service Fabric services.</span></span>

<span data-ttu-id="92640-249">**バック エンド SQL Server と AD DS の初期推定値**</span><span class="sxs-lookup"><span data-stu-id="92640-249">**Initial estimates for the back-end SQL Server and AD DS**</span></span>

<table>
<thead>
<tr>
<th></th>
<th><span data-ttu-id="92640-250">役割</span><span class="sxs-lookup"><span data-stu-id="92640-250">Role</span></span></th>
<th><span data-ttu-id="92640-251">VMs/ インスタンス</span><span class="sxs-lookup"><span data-stu-id="92640-251">VMs/instances</span></span></th>
<th><span data-ttu-id="92640-252">コア</span><span class="sxs-lookup"><span data-stu-id="92640-252">Cores</span></span></th>
<th><span data-ttu-id="92640-253">コア合計</span><span class="sxs-lookup"><span data-stu-id="92640-253">Total cores</span></span></th>
<th><span data-ttu-id="92640-254">インスタンス 16 GB あたりのメモリー</span><span class="sxs-lookup"><span data-stu-id="92640-254">Memory per instance (GB)</span></span></th>
<th><span data-ttu-id="92640-255">メモリー合計 (GB)</span><span class="sxs-lookup"><span data-stu-id="92640-255">Total memory (GB)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><span data-ttu-id="92640-256"><strong>共有インフラストラクチャ</strong></span><span class="sxs-lookup"><span data-stu-id="92640-256"><strong>Shared infrastructure</strong></span></span></td>
<td><span data-ttu-id="92640-257">SQL Server\*</span><span class="sxs-lookup"><span data-stu-id="92640-257">SQL Server\*</span></span></td>
<td><span data-ttu-id="92640-258">2</span><span class="sxs-lookup"><span data-stu-id="92640-258">2</span></span></td>
<td><span data-ttu-id="92640-259">8</span><span class="sxs-lookup"><span data-stu-id="92640-259">8</span></span></td>
<td><span data-ttu-id="92640-260">16</span><span class="sxs-lookup"><span data-stu-id="92640-260">16</span></span></td>
<td><span data-ttu-id="92640-261">32</span><span class="sxs-lookup"><span data-stu-id="92640-261">32</span></span></td>
<td><span data-ttu-id="92640-262">64</span><span class="sxs-lookup"><span data-stu-id="92640-262">64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92640-263">ファイル サーバー / ストレージ エリア ネットワーク / 高可用性ストレージ</span><span class="sxs-lookup"><span data-stu-id="92640-263">File server/Storage area network/Highly available storage</span></span></td>
<td colspan="5"><span data-ttu-id="92640-264">バック エンド記憶域は、ランタイム ストレージ エリア ネットワーク (SAN) のソリッド ステート ドライブ (SSDs) に基づく必用があります。</span><span class="sxs-lookup"><span data-stu-id="92640-264">The back-end storage must be based on solid-state drives (SSDs) on a runtime storage area network (SAN).</span></span>
<p><span data-ttu-id="92640-265">1 秒あたりのサイズと入力 / 出力オペレーション (IOPS) スループットは、ワークロードのサイズに基づきます。</span><span class="sxs-lookup"><span data-stu-id="92640-265">Size and input/output operations per second (IOPS) throughput is based on the size of the workload.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="92640-266">Active Directory</span><span class="sxs-lookup"><span data-stu-id="92640-266">Active Directory</span></span></td>
<td><span data-ttu-id="92640-267">3</span><span class="sxs-lookup"><span data-stu-id="92640-267">3</span></span></td>
<td><span data-ttu-id="92640-268">4</span><span class="sxs-lookup"><span data-stu-id="92640-268">4</span></span></td>
<td><span data-ttu-id="92640-269">12</span><span class="sxs-lookup"><span data-stu-id="92640-269">12</span></span></td>
<td><span data-ttu-id="92640-270">16</span><span class="sxs-lookup"><span data-stu-id="92640-270">16</span></span></td>
<td><span data-ttu-id="92640-271">48</span><span class="sxs-lookup"><span data-stu-id="92640-271">48</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92640-272"><em>共有インフラストラクチャの概要</em></span><span class="sxs-lookup"><span data-stu-id="92640-272"><em>Summary for shared infrastructure</em></span></span></td>
<td></td>
<td><span data-ttu-id="92640-273"><em>5</em></span><span class="sxs-lookup"><span data-stu-id="92640-273"><em>5</em></span></span></td>
<td></td>
<td><span data-ttu-id="92640-274"><em>28</em></span><span class="sxs-lookup"><span data-stu-id="92640-274"><em>28</em></span></span></td>
<td></td>
<td><span data-ttu-id="92640-275"><em>112</em></span><span class="sxs-lookup"><span data-stu-id="92640-275"><em>112</em></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="92640-276">\*SQL Server サイズは、ワークロードに大きく依存します。</span><span class="sxs-lookup"><span data-stu-id="92640-276">\* SQL Server sizes are highly dependent on workloads.</span></span> <span data-ttu-id="92640-277">詳細については、[オンプレミス環境のハードウェアのサイズ変更](hardware-sizing-on-premises-environments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-277">For more information, see [Hardware sizing for on-premises environments](hardware-sizing-on-premises-environments.md).</span></span> <span data-ttu-id="92640-278">サンド ボックスと生産環境の 個別 SQL Server 機械を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-278">Separate SQL Server machines for sandbox and production environments must be used.</span></span> <span data-ttu-id="92640-279">ただし、すべてのサンド ボックス環境で、SQL Server を共有できます。</span><span class="sxs-lookup"><span data-stu-id="92640-279">However, SQL Server can be shared in all sandbox environments.</span></span>

## <a name="storage"></a><span data-ttu-id="92640-280">保管</span><span class="sxs-lookup"><span data-stu-id="92640-280">Storage</span></span>

- <span data-ttu-id="92640-281">**AOS** - Finance and Operations (オンプレミス) を使用して、サーバー メッセージ ブロック (SMB) 3.0 共有に構造化されていないデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="92640-281">**AOS** – Finance and Operations (on-premises) uses a Server Message Block (SMB) 3.0 share to store unstructured data.</span></span> <span data-ttu-id="92640-282">詳細については、[Windows Server 2016 の Storage Spaces Direct](/windows-server/storage/storage-spaces/storage-spaces-direct-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-282">For more information, see [Storage Spaces Direct in Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).</span></span>
- <span data-ttu-id="92640-283">**SQL** – 次のオプションは実行可能です。</span><span class="sxs-lookup"><span data-stu-id="92640-283">**SQL** – The following options are viable:</span></span>

    - <span data-ttu-id="92640-284">高可用性 SSD 設定</span><span class="sxs-lookup"><span data-stu-id="92640-284">A highly available SSD setup</span></span>
    - <span data-ttu-id="92640-285">オンライン トランザクション 処理 (OLTP) スループットに対して最適化された SAN</span><span class="sxs-lookup"><span data-stu-id="92640-285">A SAN that is optimized for online transaction processing (OLTP) throughputs</span></span>
    - <span data-ttu-id="92640-286">高パフォーマンス直接接続ストレージ (DAS)</span><span class="sxs-lookup"><span data-stu-id="92640-286">High-performance direct-attached storage (DAS)</span></span>

- <span data-ttu-id="92640-287">**SQL サーバーとデータの管理 IOPS** – データ管理と SQL Server の両方のストレージには、少なくとも 1 秒あたり 2,000 IOPS が必要です。</span><span class="sxs-lookup"><span data-stu-id="92640-287">**SQL Server and data management IOPS** – The storage for both data management and SQL Server should have at least 2,000 IOPS.</span></span> <span data-ttu-id="92640-288">生産 IOPS はさまざまな要因に依存します。</span><span class="sxs-lookup"><span data-stu-id="92640-288">Production IOPS depends on many factors.</span></span> <span data-ttu-id="92640-289">詳細については、[オンプレミス環境のハードウェアのサイズ変更](hardware-sizing-on-premises-environments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-289">For more information, see [Hardware sizing for on-premises environments](hardware-sizing-on-premises-environments.md).</span></span>
- <span data-ttu-id="92640-290">**VM IOPS** – 各 VM は少なくともt 100 書き込み IOPS が必要です。</span><span class="sxs-lookup"><span data-stu-id="92640-290">**VM IOPS** – Each VM should have at least 100 write IOPS.</span></span>

## <a name="virtual-host-requirements"></a><span data-ttu-id="92640-291">仮想ホストの要件</span><span class="sxs-lookup"><span data-stu-id="92640-291">Virtual host requirements</span></span>

<span data-ttu-id="92640-292">Finance and Operations (オンプレミス) 環境の仮想ホストを設定する場合は、[Service Fabric クラスターの計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) と [Service Fabric クラスターの説明](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description) のガイドラインを参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-292">When you set up the virtual hosts for a Finance and Operations (on-premises) environment, see the guidelines in [Plan and prepare your Service Fabric cluster](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) and [Describing a service fabric cluster](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description).</span></span> <span data-ttu-id="92640-293">各仮想ホストには、サイズ変更されているインフラストラクチャ用のコアが十分にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-293">Each virtual host should have enough cores for the infrastructure that is being sized.</span></span> <span data-ttu-id="92640-294">SQL Server が物理ハードウェア上に存在し、その他のすべてが仮想化されている場合は、複数の高度な構成が可能です。</span><span class="sxs-lookup"><span data-stu-id="92640-294">Multiple advanced configurations are possible, where SQL Server resides on physical hardware but everything else is virtualized.</span></span> <span data-ttu-id="92640-295">SQL Server が仮想化されている場合、ディスク サブシステムは高速 SAN または同等のものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-295">If SQL Server is virtualized, the disk subsystem should be a fast SAN or the equivalent.</span></span> <span data-ttu-id="92640-296">いずれの場合も、仮想ホストの基本設定が高可用性および重複であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="92640-296">In all cases, make sure that the basic setup of the virtual host is highly available and redundant.</span></span> <span data-ttu-id="92640-297">いずれの場合も、仮想化を使用する場合は、VM スナップショットを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="92640-297">In all cases, when virtualization is used, no VM snapshots should be taken.</span></span>

<span data-ttu-id="92640-298">Finance and Operations には、非 Microsoft 仮想化プラットフォーム (具体的には VMWare) での操作に関する Microsoft の標準サポート ポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="92640-298">Finance and Operations falls under Microsoft's standard support policy regarding operation on non-Microsoft virtualization platforms – specifically VMWare.</span></span> <span data-ttu-id="92640-299">詳細については、[Microsoft ソフトウェアのサポート ポリシー](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-299">For more information, read [Support policy for Microsoft software](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw).</span></span> <span data-ttu-id="92640-300">つまり、この環境では製品をサポートしますが、問題の調査を依頼された場合、仮想化プラットフォームのない状態または Microsoft 仮想化プラットフォームで問題を再現するようまずお客様に依頼する場合があります。</span><span class="sxs-lookup"><span data-stu-id="92640-300">In short, we support our products in this environment, but if we are asked to investigate an issue, we may ask the customer to first reproduce the problem without the virtualization platform or on the Microsoft virtualization platform.</span></span>

## <a name="software-requirements-for-all-server-computers"></a><span data-ttu-id="92640-301">すべてのサーバー コンピュータのソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="92640-301">Software requirements for all server computers</span></span>

<span data-ttu-id="92640-302">Finance and Operations (オンプレミス) コンポーネントをインストールする前に、次のソフトウェアがコンピュータに存在している必要があります:</span><span class="sxs-lookup"><span data-stu-id="92640-302">The following software must be present on a computer before any Finance and Operations (on-premises) components can be installed:</span></span>

- <span data-ttu-id="92640-303">Microsoft .NET Framework バージョン 4.5.1 またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="92640-303">The Microsoft .NET Framework version 4.5.1 or later</span></span>
- <span data-ttu-id="92640-304">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="92640-304">Service Fabric</span></span>

<span data-ttu-id="92640-305">詳細については、[Service Fabric クラスターの計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-305">For more information, see [Plan and prepare your Service Fabric cluster](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

## <a name="supported-server-operating-systems"></a><span data-ttu-id="92640-306">サポートされるサーバー オペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="92640-306">Supported server operating systems</span></span>

<span data-ttu-id="92640-307">次の表では、Finance and Operations コンポーネントでサポートされているサーバー オペレーティング システムを示します。</span><span class="sxs-lookup"><span data-stu-id="92640-307">The following table lists the server operating systems that are supported for Finance and Operations components.</span></span>

| <span data-ttu-id="92640-308">オペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="92640-308">Operating system</span></span>                                     | <span data-ttu-id="92640-309">摘要</span><span class="sxs-lookup"><span data-stu-id="92640-309">Notes</span></span> |
|------------------------------------------------------|-------|
| <span data-ttu-id="92640-310">Microsoft Windows Server 2016 Datacenter または Standard</span><span class="sxs-lookup"><span data-stu-id="92640-310">Microsoft Windows Server 2016 Datacenter or Standard</span></span> | <span data-ttu-id="92640-311">これらの要件は、AOS をホストするデータベースおよび Service Fabric クラスターに対するものです。</span><span class="sxs-lookup"><span data-stu-id="92640-311">These requirements are for the database and the Service Fabric cluster that hosts AOS.</span></span><p><span data-ttu-id="92640-312">en-US OS インストールのみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="92640-312">Only en-US OS installations are supported.</span></span></p> |

## <a name="software-requirements-for-database-servers"></a><span data-ttu-id="92640-313">データベース サーバーのソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="92640-313">Software requirements for database servers</span></span>

- <span data-ttu-id="92640-314">64 ビット バージョンの SQL Server 2016 のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="92640-314">Only 64-bit versions of SQL Server 2016 are supported.</span></span>
- <span data-ttu-id="92640-315">サーバーおよびデータベースの照合順序では、**SQL\_Latin1\_General\_CP1\_CI\_AS** のみ有効です。</span><span class="sxs-lookup"><span data-stu-id="92640-315">Only **SQL\_Latin1\_General\_CP1\_CI\_AS** is valid for the server and database collation.</span></span>
- <span data-ttu-id="92640-316">実稼動環境では、使用している SQL Server のバージョンの最新の累積的な更新プログラム (CU) をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="92640-316">In a production environment, we recommend that you install the latest cumulative update (CU) for the version of SQL Server that you're using.</span></span>
- <span data-ttu-id="92640-317">Finance and Operations (オンプレミス) では、大文字小文字を区別しない、アクセントを区別する、カナを区別する、および幅を区別しない Unicode 照合順序をサポートします。</span><span class="sxs-lookup"><span data-stu-id="92640-317">Finance and Operations (on-premises) supports Unicode collations that are case-insensitive, accent-sensitive, kana-sensitive, and width-insensitive.</span></span> <span data-ttu-id="92640-318">照合順序は、AOS インスタンスを実行しているコンピュータの Windows ロケールと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-318">The collation must match the Windows locale of the computers that are running AOS instances.</span></span> <span data-ttu-id="92640-319">新しいインストールを設定する場合は、SQL Server 照合の代わりに Windows 照合を選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="92640-319">If you're setting up a new installation, we recommend that you select a Windows collation instead of a SQL Server collation.</span></span> <span data-ttu-id="92640-320">SQL Server データベースの照合順序を選択する方法の詳細については、「[SQL Server に関するドキュメント](/sql/sql-server/sql-server-technical-documentation)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-320">For more information about how to select a collation for a SQL Server database, see the [SQL Server documentation](/sql/sql-server/sql-server-technical-documentation).</span></span>

<span data-ttu-id="92640-321">次の表では、Finance and Operations データベースでサポートされている SQL Server バージョンを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="92640-321">The following table lists the SQL Server versions that are supported for the Finance and Operations databases.</span></span> <span data-ttu-id="92640-322">詳細については、「[SQL Server](https://www.microsoft.com/sql-server/sql-server-2016) の最小ハードウェア要件」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-322">For more information, see the minimum hardware requirements for [SQL Server](https://www.microsoft.com/sql-server/sql-server-2016).</span></span>

| <span data-ttu-id="92640-323">必要量</span><span class="sxs-lookup"><span data-stu-id="92640-323">Requirement</span></span>                                                      | <span data-ttu-id="92640-324">摘要</span><span class="sxs-lookup"><span data-stu-id="92640-324">Notes</span></span> |
|------------------------------------------------------------------|-------|
| <span data-ttu-id="92640-325">Microsoft SQL Server2016 Standard Edition または Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="92640-325">Microsoft SQL Server 2016 Standard Edition or Enterprise Edition</span></span> | <span data-ttu-id="92640-326">SQL Server 2016 のハードウェア要件については、「[SQL Server 2016 インストール用のハードウェアおよびソフトウェア要件](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-326">For the hardware requirements for SQL Server 2016, see [Hardware and Software Requirements for Installing SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server).</span></span> |

## <a name="software-requirements-for-application-object-server-aos"></a><span data-ttu-id="92640-327">Application Object Server (AOS) のソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="92640-327">Software requirements for Application Object Server (AOS)</span></span>

- <span data-ttu-id="92640-328">SQL Server Integration Services (SSIS)</span><span class="sxs-lookup"><span data-stu-id="92640-328">SQL Server Integration Services (SSIS)</span></span>

## <a name="software-requirements-for-reporting-server-bi"></a><span data-ttu-id="92640-329">レポート サーバー (BI) のソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="92640-329">Software requirements for Reporting Server (BI)</span></span>

- <span data-ttu-id="92640-330">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="92640-330">SQL Server Reporting Services (SSRS)</span></span>

## <a name="software-requirements-for-client-computers"></a><span data-ttu-id="92640-331">クライアント コンピュータのソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="92640-331">Software requirements for client computers</span></span>

<span data-ttu-id="92640-332">Finance and Operations Web アプリケーションは、HTML 5.0 に準拠している Web ブラウザーを備えた任意のデバイス上で実行できます。</span><span class="sxs-lookup"><span data-stu-id="92640-332">The Finance and Operations web application can run on any device that has an HTML 5.0–compliant web browser.</span></span> <span data-ttu-id="92640-333">Microsoft が確認した特定のデバイス / ブラウザーの組み合わせは、次の通りです。</span><span class="sxs-lookup"><span data-stu-id="92640-333">Here are some of the specific device/browser combinations that Microsoft has confirmed:</span></span>

- <span data-ttu-id="92640-334">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="92640-334">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
- <span data-ttu-id="92640-335">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="92640-335">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
- <span data-ttu-id="92640-336">Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="92640-336">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
- <span data-ttu-id="92640-337">Mac OS X 10.10 (Yosemite)、10.11 (El Capitan)、または 10.12 (Sierra)、または Apple iPad の Apple Safari (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="92640-337">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

## <a name="software-requirements-for-active-directory-federation-services"></a><span data-ttu-id="92640-338">Active Directory フェデレーション サービスのソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="92640-338">Software requirements for Active Directory Federation Services</span></span>

<span data-ttu-id="92640-339">Windows Server 2016 の Active Directory Federation Services (AD FS) は必要です。</span><span class="sxs-lookup"><span data-stu-id="92640-339">Active Directory Federation Services (AD FS) on Windows Server 2016 is required.</span></span>

<span data-ttu-id="92640-340">ドメイン コントローラは、Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-340">The domain controller must be Windows Server 2012 R2 or later, and the domain functional level must be 2012 R2 or more.</span></span> <span data-ttu-id="92640-341">ドメイン機能レベルの詳細については、次のページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-341">For more information about domain functional levels, see the following pages:</span></span>

- <span data-ttu-id="92640-342">[Active Directory 機能レベルとは](https://technet.microsoft.com/library/cc787290(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="92640-342">[What Are Active Directory Functional Levels](https://technet.microsoft.com/library/cc787290(v=ws.10).aspx)</span></span>
- <span data-ttu-id="92640-343">[Active Directory ドメイン サービス機能のレベルを理解する](https://technet.microsoft.com/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="92640-343">[Understanding Active Directory Domain Services Functional Levels](https://technet.microsoft.com/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="92640-344">サポートされる Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="92640-344">Supported Microsoft Office applications</span></span>

<span data-ttu-id="92640-345">次の Microsoft Office アプリケーションは、Finance and Operations のクラウドおよびオンプレミス配置でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="92640-345">The following Microsoft Office applications are supported in the cloud and on-premises deployments of Finance and Operations:</span></span>

- <span data-ttu-id="92640-346">Microsoft Excel と Microsoft Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-346">To run the Microsoft Excel and Microsoft Word add-ins, you must have Microsoft Office 2016 for Windows installed.</span></span> <span data-ttu-id="92640-347">バージョン要求の詳細については、[Office 統合トラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92640-347">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
- <span data-ttu-id="92640-348">Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="92640-348">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="hardware-and-software-requirements-for-retail-components"></a><span data-ttu-id="92640-349">小売コンポーネントのハードウェアおよびソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="92640-349">Hardware and software requirements for Retail components</span></span>

<span data-ttu-id="92640-350">現在、Finance and Operations (オンプレミス) は Retail コンポーネントを含んでいません。</span><span class="sxs-lookup"><span data-stu-id="92640-350">Currently, Finance and Operations (on-premises) doesn't include the Retail components.</span></span>
