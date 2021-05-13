---
title: オンプレミス環境の設定と配置 (Platform update 41 以降)
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) プラットフォーム更新プログラム 41 以降を計画、設定、展開する方法について説明します。
author: faix
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: Platform update 41
ms.openlocfilehash: 59c2bc3786a9bb701d98c4e324a6fd2fc419d394
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924415"
---
# <a name="set-up-and-deploy-on-premises-environments-platform-update-41-and-later"></a><span data-ttu-id="b094f-103">オンプレミス環境の設定と配置 (Platform update 41 以降)</span><span class="sxs-lookup"><span data-stu-id="b094f-103">Set up and deploy on-premises environments (Platform update 41 and later)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b094f-104">このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) プラットフォーム更新プログラム 41 以降を計画、設定、展開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b094f-104">This topic explains how to plan, set up, and deploy Microsoft Dynamics 365 Finance + Operations (on-premises) with Platform update 41 and later.</span></span> <span data-ttu-id="b094f-105">プラットフォーム更新プログラム 41 はバージョン 10.0.17 で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="b094f-105">Platform update 41 is available with version 10.0.17.</span></span>

<span data-ttu-id="b094f-106">[ローカル ビジネス データ Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13595809&view=all) が利用可能です。</span><span class="sxs-lookup"><span data-stu-id="b094f-106">The [Local Business Data Yammer group](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13595809&view=all) is available.</span></span> <span data-ttu-id="b094f-107">そこでは、オンプレミス展開に関する質問またはフィードバックをすべて投稿できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-107">There, you can post any questions or feedback that you have about the on-premises deployment.</span></span>

## <a name="finance--operations-components"></a><span data-ttu-id="b094f-108">Finance + Operations のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="b094f-108">Finance + Operations components</span></span>

<span data-ttu-id="b094f-109">Finance + Operations アプリケーションは、次の 3 つの主要なコンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="b094f-109">The Finance + Operations application consists of three main components:</span></span>

- <span data-ttu-id="b094f-110">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="b094f-110">Application Object Server (AOS)</span></span>
- <span data-ttu-id="b094f-111">ビジネス インテリジェンス (BI)</span><span class="sxs-lookup"><span data-stu-id="b094f-111">Business Intelligence (BI)</span></span>
- <span data-ttu-id="b094f-112">財務レポート/管理レポーター</span><span class="sxs-lookup"><span data-stu-id="b094f-112">Financial Reporting/Management Reporter</span></span>

<span data-ttu-id="b094f-113">これらのコンポーネントは、次のシステム ソフトウェアによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b094f-113">These components depend on the following system software:</span></span>

- <span data-ttu-id="b094f-114">Microsoft Windows Server 2016 (英語オペレーティング システムのインストールのみがサポートされます。)</span><span class="sxs-lookup"><span data-stu-id="b094f-114">Microsoft Windows Server 2016 (Only English-language operating system installations are supported.)</span></span>
- <span data-ttu-id="b094f-115">Microsoft SQL Server 2016 SP2</span><span class="sxs-lookup"><span data-stu-id="b094f-115">Microsoft SQL Server 2016 SP2</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b094f-116">フルテキスト検索を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-116">Full-Text Search must be enabled.</span></span>

- <span data-ttu-id="b094f-117">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="b094f-117">SQL Server Reporting Services (SSRS)</span></span>

    <span data-ttu-id="b094f-118">SSRS は BI 仮想マシン (VM) に展開されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-118">SSRS is deployed on BI virtual machines (VMs).</span></span> <span data-ttu-id="b094f-119">SSRS ノードには、ローカルで実行されているデータベース エンジン インスタンスも必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-119">The SSRS nodes should also have a Database Engine instance that is running locally.</span></span>

- <span data-ttu-id="b094f-120">SQL Server Integration Services (SSIS)</span><span class="sxs-lookup"><span data-stu-id="b094f-120">SQL Server Integration Services (SSIS)</span></span>

    <span data-ttu-id="b094f-121">SSIS は AOS VM に展開されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-121">SSIS is deployed on AOS VMs.</span></span>

- <span data-ttu-id="b094f-122">SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="b094f-122">SQL Server Management Studio</span></span>
- <span data-ttu-id="b094f-123">スタンドアロン Microsoft Azure Service Fabric 7.2 以降</span><span class="sxs-lookup"><span data-stu-id="b094f-123">Standalone Microsoft Azure Service Fabric 7.2 or later</span></span>
- <span data-ttu-id="b094f-124">Microsoft Windows PowerShell 5.0 以降</span><span class="sxs-lookup"><span data-stu-id="b094f-124">Microsoft Windows PowerShell 5.0 or later</span></span>
- <span data-ttu-id="b094f-125">Windows Server 2016 での Active Directory Federation Services (AD FS)</span><span class="sxs-lookup"><span data-stu-id="b094f-125">Active Directory Federation Services (AD FS) on Windows Server 2016</span></span>
- <span data-ttu-id="b094f-126">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="b094f-126">Domain controller</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b094f-127">ドメイン コントローラーは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-127">The domain controller must be Microsoft Windows Server 2012 R2 or later, and it must have a domain functional level of 2012 R2 or more.</span></span> <span data-ttu-id="b094f-128">ドメイン機能レベルの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-128">For more information about domain functional levels, see the following topics:</span></span>
    >
    > - <span data-ttu-id="b094f-129">[Active Directory 機能レベルとは?](/previous-versions/windows/it-pro/windows-server-2003/cc787290(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b094f-129">[What Are Active Directory Functional Levels?](/previous-versions/windows/it-pro/windows-server-2003/cc787290(v=ws.10))</span></span>
    > - <span data-ttu-id="b094f-130">[Active Directory Domain Services (AD DS) 機能のレベルを理解する](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b094f-130">[Understanding Active Directory Domain Services (AD DS) Functional Levels](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))</span></span>
    > - [<span data-ttu-id="b094f-131">双方向の完全な信頼</span><span class="sxs-lookup"><span data-stu-id="b094f-131">Full 2-way trust</span></span>](../../fin-ops/get-started/system-requirements-on-prem.md#full-2-way-trust)

- <span data-ttu-id="b094f-132">次はオプションですが **非常に** 推奨されています: Windows Server 2016 の Active Directory Certificate Services (AD CS)</span><span class="sxs-lookup"><span data-stu-id="b094f-132">Optional but **highly** recommended: Active Directory Certificate Services (AD CS) on Windows Server 2016</span></span>

## <a name="lcs"></a><span data-ttu-id="b094f-133">LCS</span><span class="sxs-lookup"><span data-stu-id="b094f-133">LCS</span></span>

<span data-ttu-id="b094f-134">Finance + Operations のビットは、Microsoft Dynamics Lifecycle Services (LCS) を通じて配布されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-134">Finance + Operations bits are distributed through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b094f-135">配置する前に、[エンタープライズ契約](https://www.microsoft.com/Licensing/licensing-programs/enterprise.aspx) チャンネルを通じてライセンス キーを購入し、LCS でオンプレミス プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="b094f-135">Before you can deploy, you must purchase license keys through the [Enterprise Agreements](https://www.microsoft.com/Licensing/licensing-programs/enterprise.aspx) channel and set up an on-premises project in LCS.</span></span> <span data-ttu-id="b094f-136">LCS からのみ配置を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="b094f-136">Deployments can be initiated only through LCS.</span></span> <span data-ttu-id="b094f-137">LCS でオンプレミス プロジェクトを設定する方法の詳細については、[Lifecycle Services (LCS) でのオンプレミス プロジェクトの設定](../lifecycle-services/lbd-create-lcs-on-prem-project.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-137">For more information about how to set up on-premises projects in LCS, see [Set up on-premises projects in Lifecycle Services (LCS)](../lifecycle-services/lbd-create-lcs-on-prem-project.md).</span></span>

## <a name="authentication"></a><span data-ttu-id="b094f-138">認証</span><span class="sxs-lookup"><span data-stu-id="b094f-138">Authentication</span></span>

<span data-ttu-id="b094f-139">オンプレミス アプリケーションは AD FS で動作します。</span><span class="sxs-lookup"><span data-stu-id="b094f-139">The on-premises application works with AD FS.</span></span> <span data-ttu-id="b094f-140">LCS と対話するには、Azure Active Directory (Azure AD) も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-140">To interact with LCS, you must also configure Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="b094f-141">展開を完了し、LCS ローカル エージェントを構成するには、Azure AD が必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-141">To complete the deployment and configure the LCS local agent, you must have Azure AD.</span></span> <span data-ttu-id="b094f-142">Azure AD テナントがまだない場合は、Azure AD が提供するオプションのいずれかを使用して無料のものを取得できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-142">If you don't already have an Azure AD tenant, you can get one for free by using one of the options that Azure AD provides.</span></span> <span data-ttu-id="b094f-143">詳細については、[クイックスタート: テナントの設定](/azure/active-directory/develop/active-directory-howto-tenant)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-143">For more information, see [Quickstart: Set up a tenant](/azure/active-directory/develop/active-directory-howto-tenant).</span></span>

## <a name="standalone-service-fabric"></a><span data-ttu-id="b094f-144">Standalone Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b094f-144">Standalone Service Fabric</span></span>

<span data-ttu-id="b094f-145">Finance + Operations は スタンドアロン Service Fabric を使用します。</span><span class="sxs-lookup"><span data-stu-id="b094f-145">Finance + Operations uses standalone Service Fabric.</span></span> <span data-ttu-id="b094f-146">詳細については、[Service Fabric ドキュメント](/azure/service-fabric/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-146">For more information, see the [Service Fabric documentation](/azure/service-fabric/).</span></span>

<span data-ttu-id="b094f-147">Finance + Operations の設定では、Service Fabric 内に一連のアプリケーションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b094f-147">Setup of Finance + Operations will deploy a set of applications inside Service Fabric.</span></span> <span data-ttu-id="b094f-148">展開中に、クラスター内の各ノードは、次のいずれかのノード タイプを持つように構成されることにより定義されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-148">During deployment, each node in the cluster will be defined through configuration so that it has one of the following node types:</span></span>

- <span data-ttu-id="b094f-149">**AOSNodeType** – このタイプのノードは、AOS (ビジネス ロジック) をホストします。</span><span class="sxs-lookup"><span data-stu-id="b094f-149">**AOSNodeType** – Nodes of this type host AOS (business logic).</span></span>
- <span data-ttu-id="b094f-150">**OrchestratorType** – このノード タイプのノードは Service Fabric のプライマリ ノードとして機能し、展開およびサービスロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="b094f-150">**OrchestratorType** – Nodes of this node type work as Service Fabric Primary nodes, and host deployment and servicing logic.</span></span>
- <span data-ttu-id="b094f-151">**ReportServerType** – このタイプのノードは、SSRS およびレポート ロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="b094f-151">**ReportServerType** – Nodes of this type host SSRS and reporting logic.</span></span>
- <span data-ttu-id="b094f-152">**MRType** – このタイプのノードは Management Reporter ロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="b094f-152">**MRType** – Nodes of this type host Management Reporter logic.</span></span>

## <a name="infrastructure"></a><span data-ttu-id="b094f-153">インフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="b094f-153">Infrastructure</span></span>

<span data-ttu-id="b094f-154">Finance + Operations には、非 Microsoft 仮想化プラットフォーム (特に VMWare) での操作に関する Microsoft の標準サポート ポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-154">Finance + Operations falls under the standard Microsoft support policy about operation on non-Microsoft virtualization platforms, specifically VMware.</span></span> <span data-ttu-id="b094f-155">詳細については、[Microsoft 以外のハードウェア仮想化ソフトウェアで実行される Microsoft ソフトウェアのサポート ポリシー](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-155">For more information, see [Support policy for Microsoft software that runs on non-Microsoft hardware virtualization software](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw).</span></span> <span data-ttu-id="b094f-156">要するに、Microsoft はこの環境で製品をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b094f-156">In short, Microsoft supports its products in this environment.</span></span> <span data-ttu-id="b094f-157">ただし、Microsoft が問題の調査を依頼された場合、仮想化プラットフォームのない状態または Microsoft 仮想化プラットフォームで問題を再現するようまず顧客に依頼する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-157">However, if Microsoft is asked to investigate an issue, we might first ask the customer to reproduce the issue without the virtualization platform or on the Microsoft virtualization platform.</span></span>

<span data-ttu-id="b094f-158">VMware を使用している場合は、次の Web ページに記載されている修正プログラムを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-158">If you're using VMware, you must implement the fixes that are documented on the following webpages:</span></span>

- [<span data-ttu-id="b094f-159">仮想マシンをハードウェア バージョン 11 にアップグレード後、ネットワーク依存ワークロードのパフォーマンスが低下する (2129176)</span><span class="sxs-lookup"><span data-stu-id="b094f-159">After upgrading a virtual machine to hardware version 11, network dependent workloads experience performance degradation (2129176)</span></span>](https://kb.vmware.com/s/article/2129176)
- [<span data-ttu-id="b094f-160">vmxnet3 仮想アダプターのいくつかの問題</span><span class="sxs-lookup"><span data-stu-id="b094f-160">Several issues with vmxnet3 virtual adapter</span></span>](https://vinfrastructure.it/2016/05/several-issues-vmxnet3-virtual-adapter)

 > [!WARNING]
 > <span data-ttu-id="b094f-161">Dynamics 365 Finance + Operations (オンプレミス) は、Microsoft Azure クラウド サービス を含む、任意のパブリック クラウド インフラストラクチャではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b094f-161">Dynamics 365 Finance + Operations (on-premises) is not supported on any public cloud infrastructure, including Microsoft Azure Cloud services.</span></span> <span data-ttu-id="b094f-162">ただし、[Microsoft Azure スタック ハブ](https://azure.microsoft.com/en-us/products/azure-stack/hub/) での実行はサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b094f-162">However, it is supported to run on [Microsoft Azure Stack Hub](https://azure.microsoft.com/en-us/products/azure-stack/hub/).</span></span>

<span data-ttu-id="b094f-163">ハードウェア構成には、次のコンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b094f-163">The hardware configuration includes the following components:</span></span>

- <span data-ttu-id="b094f-164">Windows Server 2016 VM に基づく スタンドアロン Service Fabric Cluster</span><span class="sxs-lookup"><span data-stu-id="b094f-164">A standalone Service Fabric cluster that is based on Windows Server 2016 VMs</span></span>
- <span data-ttu-id="b094f-165">SQL Server (Clustered SQL と Always-On の両方がサポートされます。)</span><span class="sxs-lookup"><span data-stu-id="b094f-165">SQL Server (Both Clustered SQL and Always-On are supported.)</span></span>
- <span data-ttu-id="b094f-166">認証のための AD FS</span><span class="sxs-lookup"><span data-stu-id="b094f-166">AD FS for authentication</span></span>
- <span data-ttu-id="b094f-167">ストレージ用の Server Message Block (SMB) バージョン 3 のファイル共有</span><span class="sxs-lookup"><span data-stu-id="b094f-167">Server Message Block (SMB) version 3 file share for storage</span></span>
- <span data-ttu-id="b094f-168">オプション: Microsoft Office Server 2017</span><span class="sxs-lookup"><span data-stu-id="b094f-168">Optional: Microsoft Office Server 2017</span></span>

<span data-ttu-id="b094f-169">詳細については、[オンプレミス展開のシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-169">For more information, see [System requirements for on-premises deployments](../../fin-ops/get-started/system-requirements-on-prem.md).</span></span>

### <a name="hardware-layout"></a><span data-ttu-id="b094f-170">ハードウェア レイアウト</span><span class="sxs-lookup"><span data-stu-id="b094f-170">Hardware layout</span></span>

<span data-ttu-id="b094f-171">[オンプレミス環境のハードウェア サイジング要件](../../fin-ops/get-started/hardware-sizing-on-premises-environments.md) で推奨されるサイジングに基づいて、インフラストラクチャと Service Fabric Cluster を計画します。</span><span class="sxs-lookup"><span data-stu-id="b094f-171">Plan your infrastructure and Service Fabric cluster, based on the recommended sizing in [Hardware sizing requirements for on-premises environments](../../fin-ops/get-started/hardware-sizing-on-premises-environments.md).</span></span> <span data-ttu-id="b094f-172">Service Fabric クラスターを計画する方法の詳細については、[Service Fabric のスタンドアロン クラスター展開の計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-172">For more information about how to plan the Service Fabric cluster, see [Plan and prepare your Service Fabric standalone cluster deployment](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

<span data-ttu-id="b094f-173">次のテーブルは、ハードウェア レイアウトの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="b094f-173">The following table shows an example of a hardware layout.</span></span> <span data-ttu-id="b094f-174">この例は、設定を示すためにこのトピック全体で使用されています。</span><span class="sxs-lookup"><span data-stu-id="b094f-174">This example is used throughout this topic to demonstrate the setup.</span></span> <span data-ttu-id="b094f-175">設定が完了すると、次の手順で指定されているマシン名と IP アドレスを、ご使用の環境のマシンの名前と IP アドレスに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-175">When you complete the setup, you will have to replace the machine names and IP addresses that are provided in the following instructions with the names and IP addresses for the machines in your environment.</span></span>

> [!NOTE]
> <span data-ttu-id="b094f-176">Service Fabric クラスターのプライマリ ノードには、少なくとも 3 つのノードが必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-176">The Primary node of the Service Fabric cluster must have at least three nodes.</span></span> <span data-ttu-id="b094f-177">この例では **OrchestratorType** を主要なノード タイプとして指定します。</span><span class="sxs-lookup"><span data-stu-id="b094f-177">In this example, **OrchestratorType** is designated as the Primary node type.</span></span> <span data-ttu-id="b094f-178">3 つ以上の VM を持つノード タイプがある場合、クラスターの信頼性を高めるために、そのノードタイプをプライマリ (シード) ノード タイプにすることを検討します。</span><span class="sxs-lookup"><span data-stu-id="b094f-178">If you have a node type that has more than three VMs, consider making that node type your Primary (Seed) node type to help increase the reliability of the cluster.</span></span> 

| <span data-ttu-id="b094f-179">マシンの目的</span><span class="sxs-lookup"><span data-stu-id="b094f-179">Machine purpose</span></span>          | <span data-ttu-id="b094f-180">Service Fabric ノード タイプ</span><span class="sxs-lookup"><span data-stu-id="b094f-180">Service Fabric node type</span></span> | <span data-ttu-id="b094f-181">コンピューター名</span><span class="sxs-lookup"><span data-stu-id="b094f-181">Machine name</span></span>    | <span data-ttu-id="b094f-182">IP アドレス</span><span class="sxs-lookup"><span data-stu-id="b094f-182">IP address</span></span>    |
|--------------------------|--------------------------|-----------------|---------------|
| <span data-ttu-id="b094f-183">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="b094f-183">Domain controller</span></span>        |                          | <span data-ttu-id="b094f-184">DAX7SQLAODC1</span><span class="sxs-lookup"><span data-stu-id="b094f-184">DAX7SQLAODC1</span></span>    | <span data-ttu-id="b094f-185">10.179.108.2</span><span class="sxs-lookup"><span data-stu-id="b094f-185">10.179.108.2</span></span>  |
| <span data-ttu-id="b094f-186">AD FS</span><span class="sxs-lookup"><span data-stu-id="b094f-186">AD FS</span></span>                    |                          | <span data-ttu-id="b094f-187">DAX7SQLAOADFS1</span><span class="sxs-lookup"><span data-stu-id="b094f-187">DAX7SQLAOADFS1</span></span>  | <span data-ttu-id="b094f-188">10.179.108.3</span><span class="sxs-lookup"><span data-stu-id="b094f-188">10.179.108.3</span></span>  |
| <span data-ttu-id="b094f-189">ファイル サーバー</span><span class="sxs-lookup"><span data-stu-id="b094f-189">File server</span></span>              |                          | <span data-ttu-id="b094f-190">DAX7SQLAOFILE1</span><span class="sxs-lookup"><span data-stu-id="b094f-190">DAX7SQLAOFILE1</span></span>  | <span data-ttu-id="b094f-191">10.179.108.4</span><span class="sxs-lookup"><span data-stu-id="b094f-191">10.179.108.4</span></span>  |
| <span data-ttu-id="b094f-192">SQL Always-On クラスター</span><span class="sxs-lookup"><span data-stu-id="b094f-192">SQL Always-On cluster</span></span>    |                          | <span data-ttu-id="b094f-193">DAX7SQLAOSQLA01</span><span class="sxs-lookup"><span data-stu-id="b094f-193">DAX7SQLAOSQLA01</span></span> | <span data-ttu-id="b094f-194">10.179.108.5</span><span class="sxs-lookup"><span data-stu-id="b094f-194">10.179.108.5</span></span>  |
|                          |                          | <span data-ttu-id="b094f-195">DAX7SQLAOSQLA02</span><span class="sxs-lookup"><span data-stu-id="b094f-195">DAX7SQLAOSQLA02</span></span> | <span data-ttu-id="b094f-196">10.179.108.6</span><span class="sxs-lookup"><span data-stu-id="b094f-196">10.179.108.6</span></span>  |
|                          |                          | <span data-ttu-id="b094f-197">DAX7SQLAOSQLA</span><span class="sxs-lookup"><span data-stu-id="b094f-197">DAX7SQLAOSQLA</span></span>   | <span data-ttu-id="b094f-198">10.179.108.9</span><span class="sxs-lookup"><span data-stu-id="b094f-198">10.179.108.9</span></span>  |
| <span data-ttu-id="b094f-199">クライアント</span><span class="sxs-lookup"><span data-stu-id="b094f-199">Client</span></span>                   |                          | <span data-ttu-id="b094f-200">SQLAOCLIENT1</span><span class="sxs-lookup"><span data-stu-id="b094f-200">SQLAOCLIENT1</span></span>    | <span data-ttu-id="b094f-201">10.179.108.11</span><span class="sxs-lookup"><span data-stu-id="b094f-201">10.179.108.11</span></span> |
| <span data-ttu-id="b094f-202">AOS 1</span><span class="sxs-lookup"><span data-stu-id="b094f-202">AOS 1</span></span>                    | <span data-ttu-id="b094f-203">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="b094f-203">AOSNodeType</span></span>              | <span data-ttu-id="b094f-204">SQLAOSF1AOS1</span><span class="sxs-lookup"><span data-stu-id="b094f-204">SQLAOSF1AOS1</span></span>    | <span data-ttu-id="b094f-205">10.179.108.12</span><span class="sxs-lookup"><span data-stu-id="b094f-205">10.179.108.12</span></span> |
| <span data-ttu-id="b094f-206">AOS 2</span><span class="sxs-lookup"><span data-stu-id="b094f-206">AOS 2</span></span>                    | <span data-ttu-id="b094f-207">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="b094f-207">AOSNodeType</span></span>              | <span data-ttu-id="b094f-208">SQLAOSF1AOS2</span><span class="sxs-lookup"><span data-stu-id="b094f-208">SQLAOSF1AOS2</span></span>    | <span data-ttu-id="b094f-209">10.179.108.13</span><span class="sxs-lookup"><span data-stu-id="b094f-209">10.179.108.13</span></span> |
| <span data-ttu-id="b094f-210">AOS 3</span><span class="sxs-lookup"><span data-stu-id="b094f-210">AOS 3</span></span>                    | <span data-ttu-id="b094f-211">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="b094f-211">AOSNodeType</span></span>              | <span data-ttu-id="b094f-212">SQLAOSF1AOS3</span><span class="sxs-lookup"><span data-stu-id="b094f-212">SQLAOSF1AOS3</span></span>    | <span data-ttu-id="b094f-213">10.179.108.14</span><span class="sxs-lookup"><span data-stu-id="b094f-213">10.179.108.14</span></span> |
| <span data-ttu-id="b094f-214">オーケストレータ 1</span><span class="sxs-lookup"><span data-stu-id="b094f-214">Orchestrator 1</span></span>           | <span data-ttu-id="b094f-215">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="b094f-215">OrchestratorType</span></span>         | <span data-ttu-id="b094f-216">SQLAOSF1ORCH1</span><span class="sxs-lookup"><span data-stu-id="b094f-216">SQLAOSF1ORCH1</span></span>   | <span data-ttu-id="b094f-217">10.179.108.21</span><span class="sxs-lookup"><span data-stu-id="b094f-217">10.179.108.21</span></span> |
| <span data-ttu-id="b094f-218">オーケストレータ 2</span><span class="sxs-lookup"><span data-stu-id="b094f-218">Orchestrator 2</span></span>           | <span data-ttu-id="b094f-219">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="b094f-219">OrchestratorType</span></span>         | <span data-ttu-id="b094f-220">SQLAOSF1ORCH2</span><span class="sxs-lookup"><span data-stu-id="b094f-220">SQLAOSF1ORCH2</span></span>   | <span data-ttu-id="b094f-221">10.179.108.22</span><span class="sxs-lookup"><span data-stu-id="b094f-221">10.179.108.22</span></span> |
| <span data-ttu-id="b094f-222">オーケストレータ 3</span><span class="sxs-lookup"><span data-stu-id="b094f-222">Orchestrator 3</span></span>           | <span data-ttu-id="b094f-223">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="b094f-223">OrchestratorType</span></span>         | <span data-ttu-id="b094f-224">SQLAOSF1ORCH3</span><span class="sxs-lookup"><span data-stu-id="b094f-224">SQLAOSF1ORCH3</span></span>   | <span data-ttu-id="b094f-225">10.179.108.23</span><span class="sxs-lookup"><span data-stu-id="b094f-225">10.179.108.23</span></span> |
| <span data-ttu-id="b094f-226">Management Reporter ノード</span><span class="sxs-lookup"><span data-stu-id="b094f-226">Management Reporter node</span></span> | <span data-ttu-id="b094f-227">MRType</span><span class="sxs-lookup"><span data-stu-id="b094f-227">MRType</span></span>                   | <span data-ttu-id="b094f-228">SQLAOSMR1</span><span class="sxs-lookup"><span data-stu-id="b094f-228">SQLAOSMR1</span></span>       | <span data-ttu-id="b094f-229">10.179.108.31</span><span class="sxs-lookup"><span data-stu-id="b094f-229">10.179.108.31</span></span> |
| <span data-ttu-id="b094f-230">SSRS ノード 1</span><span class="sxs-lookup"><span data-stu-id="b094f-230">SSRS node 1</span></span>              | <span data-ttu-id="b094f-231">ReportServerType</span><span class="sxs-lookup"><span data-stu-id="b094f-231">ReportServerType</span></span>         | <span data-ttu-id="b094f-232">SQLAOSFBI1</span><span class="sxs-lookup"><span data-stu-id="b094f-232">SQLAOSFBI1</span></span>      | <span data-ttu-id="b094f-233">10.179.108.41</span><span class="sxs-lookup"><span data-stu-id="b094f-233">10.179.108.41</span></span> |

<span data-ttu-id="b094f-234">次の表に、バッチ実行と対話型セッションが専用ノードで実行されるハードウェア レイアウトの例を示します。</span><span class="sxs-lookup"><span data-stu-id="b094f-234">The following table shows an example of a hardware layout where batch execution and interactive sessions are run in dedicated nodes.</span></span> <span data-ttu-id="b094f-235">詳細については、[オンプレミス配置でのバッチのみおよび対話型のみの AOS ノードのコンフィギュレーション](./onprem-batchonly.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-235">For more information, see [Configure batch-only and interactive-only AOS nodes in on-premises deployments](./onprem-batchonly.md).</span></span>

| <span data-ttu-id="b094f-236">マシンの目的</span><span class="sxs-lookup"><span data-stu-id="b094f-236">Machine purpose</span></span>          | <span data-ttu-id="b094f-237">Service Fabric ノード タイプ</span><span class="sxs-lookup"><span data-stu-id="b094f-237">Service Fabric node type</span></span>   | <span data-ttu-id="b094f-238">コンピューター名</span><span class="sxs-lookup"><span data-stu-id="b094f-238">Machine name</span></span>    | <span data-ttu-id="b094f-239">IP アドレス</span><span class="sxs-lookup"><span data-stu-id="b094f-239">IP address</span></span>    |
|--------------------------|----------------------------|-----------------|---------------|
| <span data-ttu-id="b094f-240">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="b094f-240">Domain controller</span></span>        |                            | <span data-ttu-id="b094f-241">DAX7SQLAODC1</span><span class="sxs-lookup"><span data-stu-id="b094f-241">DAX7SQLAODC1</span></span>    | <span data-ttu-id="b094f-242">10.179.108.2</span><span class="sxs-lookup"><span data-stu-id="b094f-242">10.179.108.2</span></span>  |
| <span data-ttu-id="b094f-243">AD FS</span><span class="sxs-lookup"><span data-stu-id="b094f-243">AD FS</span></span>                    |                            | <span data-ttu-id="b094f-244">DAX7SQLAOADFS1</span><span class="sxs-lookup"><span data-stu-id="b094f-244">DAX7SQLAOADFS1</span></span>  | <span data-ttu-id="b094f-245">10.179.108.3</span><span class="sxs-lookup"><span data-stu-id="b094f-245">10.179.108.3</span></span>  |
| <span data-ttu-id="b094f-246">ファイル サーバー</span><span class="sxs-lookup"><span data-stu-id="b094f-246">File server</span></span>              |                            | <span data-ttu-id="b094f-247">DAX7SQLAOFILE1</span><span class="sxs-lookup"><span data-stu-id="b094f-247">DAX7SQLAOFILE1</span></span>  | <span data-ttu-id="b094f-248">10.179.108.4</span><span class="sxs-lookup"><span data-stu-id="b094f-248">10.179.108.4</span></span>  |
| <span data-ttu-id="b094f-249">SQL Always-On クラスター</span><span class="sxs-lookup"><span data-stu-id="b094f-249">SQL Always-On cluster</span></span>    |                            | <span data-ttu-id="b094f-250">DAX7SQLAOSQLA01</span><span class="sxs-lookup"><span data-stu-id="b094f-250">DAX7SQLAOSQLA01</span></span> | <span data-ttu-id="b094f-251">10.179.108.5</span><span class="sxs-lookup"><span data-stu-id="b094f-251">10.179.108.5</span></span>  |
|                          |                            | <span data-ttu-id="b094f-252">DAX7SQLAOSQLA02</span><span class="sxs-lookup"><span data-stu-id="b094f-252">DAX7SQLAOSQLA02</span></span> | <span data-ttu-id="b094f-253">10.179.108.6</span><span class="sxs-lookup"><span data-stu-id="b094f-253">10.179.108.6</span></span>  |
|                          |                            | <span data-ttu-id="b094f-254">DAX7SQLAOSQLA</span><span class="sxs-lookup"><span data-stu-id="b094f-254">DAX7SQLAOSQLA</span></span>   | <span data-ttu-id="b094f-255">10.179.108.9</span><span class="sxs-lookup"><span data-stu-id="b094f-255">10.179.108.9</span></span>  |
| <span data-ttu-id="b094f-256">クライアント</span><span class="sxs-lookup"><span data-stu-id="b094f-256">Client</span></span>                   |                            | <span data-ttu-id="b094f-257">SQLAOCLIENT1</span><span class="sxs-lookup"><span data-stu-id="b094f-257">SQLAOCLIENT1</span></span>    | <span data-ttu-id="b094f-258">10.179.108.11</span><span class="sxs-lookup"><span data-stu-id="b094f-258">10.179.108.11</span></span> |
| <span data-ttu-id="b094f-259">AOS 1</span><span class="sxs-lookup"><span data-stu-id="b094f-259">AOS 1</span></span>                    | <span data-ttu-id="b094f-260">BatchOnlyAOSNodeType</span><span class="sxs-lookup"><span data-stu-id="b094f-260">BatchOnlyAOSNodeType</span></span>       | <span data-ttu-id="b094f-261">SQLAOSF1AOS1</span><span class="sxs-lookup"><span data-stu-id="b094f-261">SQLAOSF1AOS1</span></span>    | <span data-ttu-id="b094f-262">10.179.108.12</span><span class="sxs-lookup"><span data-stu-id="b094f-262">10.179.108.12</span></span> |
| <span data-ttu-id="b094f-263">AOS 2</span><span class="sxs-lookup"><span data-stu-id="b094f-263">AOS 2</span></span>                    | <span data-ttu-id="b094f-264">BatchOnlyAOSNodeType</span><span class="sxs-lookup"><span data-stu-id="b094f-264">BatchOnlyAOSNodeType</span></span>       | <span data-ttu-id="b094f-265">SQLAOSF1AOS2</span><span class="sxs-lookup"><span data-stu-id="b094f-265">SQLAOSF1AOS2</span></span>    | <span data-ttu-id="b094f-266">10.179.108.13</span><span class="sxs-lookup"><span data-stu-id="b094f-266">10.179.108.13</span></span> |
| <span data-ttu-id="b094f-267">AOS 3</span><span class="sxs-lookup"><span data-stu-id="b094f-267">AOS 3</span></span>                    | <span data-ttu-id="b094f-268">BatchOnlyAOSNodeType</span><span class="sxs-lookup"><span data-stu-id="b094f-268">BatchOnlyAOSNodeType</span></span>       | <span data-ttu-id="b094f-269">SQLAOSF1AOS3</span><span class="sxs-lookup"><span data-stu-id="b094f-269">SQLAOSF1AOS3</span></span>    | <span data-ttu-id="b094f-270">10.179.108.14</span><span class="sxs-lookup"><span data-stu-id="b094f-270">10.179.108.14</span></span> |
| <span data-ttu-id="b094f-271">AOS 4</span><span class="sxs-lookup"><span data-stu-id="b094f-271">AOS 4</span></span>                    | <span data-ttu-id="b094f-272">InteractiveOnlyAOSNodeType</span><span class="sxs-lookup"><span data-stu-id="b094f-272">InteractiveOnlyAOSNodeType</span></span> | <span data-ttu-id="b094f-273">SQLAOSF1AOS4</span><span class="sxs-lookup"><span data-stu-id="b094f-273">SQLAOSF1AOS4</span></span>    | <span data-ttu-id="b094f-274">10.179.108.15</span><span class="sxs-lookup"><span data-stu-id="b094f-274">10.179.108.15</span></span> |
| <span data-ttu-id="b094f-275">AOS 5</span><span class="sxs-lookup"><span data-stu-id="b094f-275">AOS 5</span></span>                    | <span data-ttu-id="b094f-276">InteractiveOnlyAOSNodeType</span><span class="sxs-lookup"><span data-stu-id="b094f-276">InteractiveOnlyAOSNodeType</span></span> | <span data-ttu-id="b094f-277">SQLAOSF1AOS5</span><span class="sxs-lookup"><span data-stu-id="b094f-277">SQLAOSF1AOS5</span></span>    | <span data-ttu-id="b094f-278">10.179.108.16</span><span class="sxs-lookup"><span data-stu-id="b094f-278">10.179.108.16</span></span> |
| <span data-ttu-id="b094f-279">AOS 6</span><span class="sxs-lookup"><span data-stu-id="b094f-279">AOS 6</span></span>                    | <span data-ttu-id="b094f-280">InteractiveOnlyAOSNodeType</span><span class="sxs-lookup"><span data-stu-id="b094f-280">InteractiveOnlyAOSNodeType</span></span> | <span data-ttu-id="b094f-281">SQLAOSF1AOS6</span><span class="sxs-lookup"><span data-stu-id="b094f-281">SQLAOSF1AOS6</span></span>    | <span data-ttu-id="b094f-282">10.179.108.17</span><span class="sxs-lookup"><span data-stu-id="b094f-282">10.179.108.17</span></span> |
| <span data-ttu-id="b094f-283">オーケストレータ 1</span><span class="sxs-lookup"><span data-stu-id="b094f-283">Orchestrator 1</span></span>           | <span data-ttu-id="b094f-284">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="b094f-284">OrchestratorType</span></span>           | <span data-ttu-id="b094f-285">SQLAOSF1ORCH1</span><span class="sxs-lookup"><span data-stu-id="b094f-285">SQLAOSF1ORCH1</span></span>   | <span data-ttu-id="b094f-286">10.179.108.21</span><span class="sxs-lookup"><span data-stu-id="b094f-286">10.179.108.21</span></span> |
| <span data-ttu-id="b094f-287">オーケストレータ 2</span><span class="sxs-lookup"><span data-stu-id="b094f-287">Orchestrator 2</span></span>           | <span data-ttu-id="b094f-288">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="b094f-288">OrchestratorType</span></span>           | <span data-ttu-id="b094f-289">SQLAOSF1ORCH2</span><span class="sxs-lookup"><span data-stu-id="b094f-289">SQLAOSF1ORCH2</span></span>   | <span data-ttu-id="b094f-290">10.179.108.22</span><span class="sxs-lookup"><span data-stu-id="b094f-290">10.179.108.22</span></span> |
| <span data-ttu-id="b094f-291">オーケストレータ 3</span><span class="sxs-lookup"><span data-stu-id="b094f-291">Orchestrator 3</span></span>           | <span data-ttu-id="b094f-292">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="b094f-292">OrchestratorType</span></span>           | <span data-ttu-id="b094f-293">SQLAOSF1ORCH3</span><span class="sxs-lookup"><span data-stu-id="b094f-293">SQLAOSF1ORCH3</span></span>   | <span data-ttu-id="b094f-294">10.179.108.23</span><span class="sxs-lookup"><span data-stu-id="b094f-294">10.179.108.23</span></span> |
| <span data-ttu-id="b094f-295">Management Reporter ノード</span><span class="sxs-lookup"><span data-stu-id="b094f-295">Management Reporter node</span></span> | <span data-ttu-id="b094f-296">MRType</span><span class="sxs-lookup"><span data-stu-id="b094f-296">MRType</span></span>                     | <span data-ttu-id="b094f-297">SQLAOSMR1</span><span class="sxs-lookup"><span data-stu-id="b094f-297">SQLAOSMR1</span></span>       | <span data-ttu-id="b094f-298">10.179.108.31</span><span class="sxs-lookup"><span data-stu-id="b094f-298">10.179.108.31</span></span> |
| <span data-ttu-id="b094f-299">SSRS ノード 1</span><span class="sxs-lookup"><span data-stu-id="b094f-299">SSRS node 1</span></span>              | <span data-ttu-id="b094f-300">ReportServerType</span><span class="sxs-lookup"><span data-stu-id="b094f-300">ReportServerType</span></span>           | <span data-ttu-id="b094f-301">SQLAOSFBI1</span><span class="sxs-lookup"><span data-stu-id="b094f-301">SQLAOSFBI1</span></span>      | <span data-ttu-id="b094f-302">10.179.108.41</span><span class="sxs-lookup"><span data-stu-id="b094f-302">10.179.108.41</span></span> |

## <a name="overview-of-the-setup-process"></a><span data-ttu-id="b094f-303">設定プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="b094f-303">Overview of the setup process</span></span>

<span data-ttu-id="b094f-304">Finance + Operations のインフラストラクチャを設定するには、以下の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-304">You must complete the following steps to set up the infrastructure for Finance + Operations.</span></span> <span data-ttu-id="b094f-305">開始する前にすべての手順を読むと、セットアップを計画しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="b094f-305">By reading all the steps before you begin, you can more easily plan your setup.</span></span>

1. [<span data-ttu-id="b094f-306">ドメイン名と DNS ゾーンの計画</span><span class="sxs-lookup"><span data-stu-id="b094f-306">Plan your domain name and DNS zones</span></span>](#plandomain)
1. [<span data-ttu-id="b094f-307">証明書の計画と取得</span><span class="sxs-lookup"><span data-stu-id="b094f-307">Plan and acquire your certificates</span></span>](#plancert)
1. [<span data-ttu-id="b094f-308">ユーザーとサービス アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="b094f-308">Plan your users and service accounts</span></span>](#plansvcacct)
1. [<span data-ttu-id="b094f-309">DNS ゾーンの作成と A レコードの追加</span><span class="sxs-lookup"><span data-stu-id="b094f-309">Create DNS zones, and add A records</span></span>](#createdns)
1. [<span data-ttu-id="b094f-310">VM のドメインへの参加</span><span class="sxs-lookup"><span data-stu-id="b094f-310">Join VMs to the domain</span></span>](#joindomain)
1. [<span data-ttu-id="b094f-311">LCS からセットアップ スクリプトのダウンロード</span><span class="sxs-lookup"><span data-stu-id="b094f-311">Download setup scripts from LCS</span></span>](#downloadscripts)
1. [<span data-ttu-id="b094f-312">コンフィギュレーションの記述</span><span class="sxs-lookup"><span data-stu-id="b094f-312">Describe your configuration</span></span>](#describeconfig)
1. [<span data-ttu-id="b094f-313">証明書の構成</span><span class="sxs-lookup"><span data-stu-id="b094f-313">Configure certificates</span></span>](#configurecert)
1. [<span data-ttu-id="b094f-314">VMs を設定する</span><span class="sxs-lookup"><span data-stu-id="b094f-314">Set up VMs</span></span>](#setupvms)
1. [<span data-ttu-id="b094f-315">スタンドアロン Service Fabric クラスターの設定</span><span class="sxs-lookup"><span data-stu-id="b094f-315">Set up a standalone Service Fabric cluster</span></span>](#setupsfcluster)
1. [<span data-ttu-id="b094f-316">テナント用 LCS 接続の構成</span><span class="sxs-lookup"><span data-stu-id="b094f-316">Configure LCS connectivity for the tenant</span></span>](#configurelcs)
1. [<span data-ttu-id="b094f-317">ファイル ストレージの設定</span><span class="sxs-lookup"><span data-stu-id="b094f-317">Set up file storage</span></span>](#setupfile)
1. [<span data-ttu-id="b094f-318">SQL Server の設定</span><span class="sxs-lookup"><span data-stu-id="b094f-318">Set up SQL Server</span></span>](#setupsql)
1. [<span data-ttu-id="b094f-319">データベースを構成する</span><span class="sxs-lookup"><span data-stu-id="b094f-319">Configure the databases</span></span>](#configuredb)
1. [<span data-ttu-id="b094f-320">資格情報の暗号化</span><span class="sxs-lookup"><span data-stu-id="b094f-320">Encrypt credentials</span></span>](#encryptcred)
1. [<span data-ttu-id="b094f-321">SSIS を設定する</span><span class="sxs-lookup"><span data-stu-id="b094f-321">Set up SSIS</span></span>](#setupssis)
1. [<span data-ttu-id="b094f-322">SSRS を設定する</span><span class="sxs-lookup"><span data-stu-id="b094f-322">Set up SSRS</span></span>](#setupssrs)
1. [<span data-ttu-id="b094f-323">AD FS のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b094f-323">Configure AD FS</span></span>](#configureadfs)
1. [<span data-ttu-id="b094f-324">コネクタを構成し、オンプレミスのローカル エージェントをインストールする</span><span class="sxs-lookup"><span data-stu-id="b094f-324">Configure a connector, and install an on-premises local agent</span></span>](#configureconnector)
1. [<span data-ttu-id="b094f-325">リモート処理が使用されたら、CredSSP を終了処理する</span><span class="sxs-lookup"><span data-stu-id="b094f-325">Tear down CredSSP, if remoting was used</span></span>](#teardowncredssp)
1. [<span data-ttu-id="b094f-326">LCS から Finance + Operations 環境を配置する</span><span class="sxs-lookup"><span data-stu-id="b094f-326">Deploy your Finance + Operations environment from LCS</span></span>](#deploy)
1. [<span data-ttu-id="b094f-327">Finance + Operations 環境への接続</span><span class="sxs-lookup"><span data-stu-id="b094f-327">Connect to your Finance + Operations environment</span></span>](#connect)

## <a name="setup"></a><span data-ttu-id="b094f-328">段取り</span><span class="sxs-lookup"><span data-stu-id="b094f-328">Setup</span></span>

### <a name="prerequisites"></a><span data-ttu-id="b094f-329">必要条件</span><span class="sxs-lookup"><span data-stu-id="b094f-329">Prerequisites</span></span>

<span data-ttu-id="b094f-330">セットアップを開始する前に、次の前提条件が満たされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-330">Before you start the setup, the following prerequisites must be in place.</span></span> <span data-ttu-id="b094f-331">これらの前提条件の設定は、このドキュメントの範囲外です。</span><span class="sxs-lookup"><span data-stu-id="b094f-331">The setup of these prerequisites is out of the scope of this document.</span></span>

- <span data-ttu-id="b094f-332">Active Directory Domain Services (AD DS) は、ネットワークにインストールして構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-332">Active Directory Domain Services (AD DS) must be installed and configured in your network.</span></span>
- <span data-ttu-id="b094f-333">AD FS は、展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-333">AD FS must be deployed.</span></span>
- <span data-ttu-id="b094f-334">SQL Server 2016 SP2 は SSRS コンピューターにインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-334">SQL Server 2016 SP2 must be installed on the SSRS machines.</span></span>
- <span data-ttu-id="b094f-335">SQL Server Reporting Services 2016 は、SSRS コンピューターに **ネイティブ** モードでインストールされる (コンフィギュレーションはされない) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-335">SQL Server Reporting Services 2016 must be installed (but not configured) in **Native** mode on the SSRS machines.</span></span>
- <span data-ttu-id="b094f-336">オプション: AD CS がネットワークにインストールおよびコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="b094f-336">Optional: AD CS is installed and configured in your network.</span></span>

<span data-ttu-id="b094f-337">次の表は、LCS からダウンロードされたインフラストラクチャ セットアップ スクリプトによって VM にインストールされる必須ソフトウェアを示します。</span><span class="sxs-lookup"><span data-stu-id="b094f-337">The following table shows the prerequisite software that is installed on the VMs by the infrastructure setup scripts that are downloaded from LCS.</span></span>

| <span data-ttu-id="b094f-338">ノード タイプ</span><span class="sxs-lookup"><span data-stu-id="b094f-338">Node type</span></span> | <span data-ttu-id="b094f-339">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b094f-339">Component</span></span> | <span data-ttu-id="b094f-340">細目</span><span class="sxs-lookup"><span data-stu-id="b094f-340">Details</span></span> |
|-----------|-----------|---------|
| <span data-ttu-id="b094f-341">AOS</span><span class="sxs-lookup"><span data-stu-id="b094f-341">AOS</span></span>       | <span data-ttu-id="b094f-342">SNAC – ODBC ドライバー 13</span><span class="sxs-lookup"><span data-stu-id="b094f-342">SNAC – ODBC driver 13</span></span> | <https://docs.microsoft.com/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows#131> |
| <span data-ttu-id="b094f-343">AOS</span><span class="sxs-lookup"><span data-stu-id="b094f-343">AOS</span></span>       | <span data-ttu-id="b094f-344">SNAC – ODBC ドライバー 17.5.x</span><span class="sxs-lookup"><span data-stu-id="b094f-344">SNAC – ODBC driver 17.5.x</span></span> | <p><span data-ttu-id="b094f-345">このドライバーは、プラットフォーム更新プログラム 15 以上にアップグレードするために必要です</span><span class="sxs-lookup"><span data-stu-id="b094f-345">This driver is required for upgrade to Platform update 15 or higher</span></span></p><p><https://docs.microsoft.com/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows?view=sql-server-ver15#1752&preserve-view=true></p> |
| <span data-ttu-id="b094f-346">AOS</span><span class="sxs-lookup"><span data-stu-id="b094f-346">AOS</span></span>       | <span data-ttu-id="b094f-347">Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-347">The Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="b094f-348">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="b094f-348">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="b094f-349">AOS</span><span class="sxs-lookup"><span data-stu-id="b094f-349">AOS</span></span>       | <span data-ttu-id="b094f-350">Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-350">The Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="b094f-351">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="b094f-351">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="b094f-352">AOS</span><span class="sxs-lookup"><span data-stu-id="b094f-352">AOS</span></span>       | <span data-ttu-id="b094f-353">Microsoft .NET Framework version 4.7.2 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-353">The Microsoft .NET Framework version 4.7.2 (CLR 4.0)</span></span> | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| <span data-ttu-id="b094f-354">AOS</span><span class="sxs-lookup"><span data-stu-id="b094f-354">AOS</span></span>       | <span data-ttu-id="b094f-355">Microsoft Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="b094f-355">Microsoft Internet Information Services (IIS)</span></span> | <span data-ttu-id="b094f-356">**Windows の機能:** WAS、WAS-Process-Model、WAS-NET-Environment、WAS-Config-APIs、Web-Server、Web-WebServer、Web-Security、Web-Filtering、Web-App-Dev、Web-Net-Ext、Web-Mgmt-Tools、Web-Mgmt-Console</span><span class="sxs-lookup"><span data-stu-id="b094f-356">**Windows features:** WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs, Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console</span></span> |
| <span data-ttu-id="b094f-357">AOS</span><span class="sxs-lookup"><span data-stu-id="b094f-357">AOS</span></span>       | <span data-ttu-id="b094f-358">SQL Server Management Studio 17.9.1</span><span class="sxs-lookup"><span data-stu-id="b094f-358">SQL Server Management Studio 17.9.1</span></span> | <https://go.microsoft.com/fwlink/?linkid=854085> |
| <span data-ttu-id="b094f-359">AOS</span><span class="sxs-lookup"><span data-stu-id="b094f-359">AOS</span></span>       | <span data-ttu-id="b094f-360">Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="b094f-360">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</span></span> | <https://support.microsoft.com/help/3179560> |
| <span data-ttu-id="b094f-361">AOS</span><span class="sxs-lookup"><span data-stu-id="b094f-361">AOS</span></span>       | <span data-ttu-id="b094f-362">Microsoft Visual Studio 2017 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="b094f-362">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2017</span></span> | <span data-ttu-id="b094f-363"><https://lcs.dynamics.com/V2/SharedAssetLibrary>に移動して、資産タイプとして **モデル** を選択して、**VC++ 17 再配布可能ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-363">Go to <https://lcs.dynamics.com/V2/SharedAssetLibrary>, select **Model** as the asset type, and then select **VC++ 17 Redistributables**.</span></span> |
| <span data-ttu-id="b094f-364">AOS</span><span class="sxs-lookup"><span data-stu-id="b094f-364">AOS</span></span>       | <span data-ttu-id="b094f-365">Microsoft Access データベース エンジン 2010 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="b094f-365">Microsoft Access Database Engine 2010 Redistributable</span></span> | <https://www.microsoft.com/download/details.aspx?id=13255> |
| <span data-ttu-id="b094f-366">BI</span><span class="sxs-lookup"><span data-stu-id="b094f-366">BI</span></span>        | <span data-ttu-id="b094f-367">.NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-367">The .NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="b094f-368">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="b094f-368">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="b094f-369">BI</span><span class="sxs-lookup"><span data-stu-id="b094f-369">BI</span></span>        | <span data-ttu-id="b094f-370">.NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-370">The .NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="b094f-371">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="b094f-371">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="b094f-372">BI</span><span class="sxs-lookup"><span data-stu-id="b094f-372">BI</span></span>        | <span data-ttu-id="b094f-373">.NET Framework version 4.7.2 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-373">The .NET Framework version 4.7.2 (CLR 4.0)</span></span> | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| <span data-ttu-id="b094f-374">BI</span><span class="sxs-lookup"><span data-stu-id="b094f-374">BI</span></span>        | <span data-ttu-id="b094f-375">SQL Server Management Studio 17.9.1</span><span class="sxs-lookup"><span data-stu-id="b094f-375">SQL Server Management Studio 17.9.1</span></span> | <https://go.microsoft.com/fwlink/?linkid=854085> |
| <span data-ttu-id="b094f-376">MR</span><span class="sxs-lookup"><span data-stu-id="b094f-376">MR</span></span>        | <span data-ttu-id="b094f-377">.NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-377">The .NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="b094f-378">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="b094f-378">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="b094f-379">MR</span><span class="sxs-lookup"><span data-stu-id="b094f-379">MR</span></span>        | <span data-ttu-id="b094f-380">.NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-380">The .NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="b094f-381">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="b094f-381">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="b094f-382">MR</span><span class="sxs-lookup"><span data-stu-id="b094f-382">MR</span></span>        | <span data-ttu-id="b094f-383">.NET Framework version 4.7.2 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-383">The .NET Framework version 4.7.2 (CLR 4.0)</span></span> | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| <span data-ttu-id="b094f-384">MR</span><span class="sxs-lookup"><span data-stu-id="b094f-384">MR</span></span>        | <span data-ttu-id="b094f-385">Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="b094f-385">Visual C++ Redistributable Packages for Visual Studio 2013</span></span> | <https://support.microsoft.com/help/3179560> |
| <span data-ttu-id="b094f-386">ORCH</span><span class="sxs-lookup"><span data-stu-id="b094f-386">ORCH</span></span>      | <span data-ttu-id="b094f-387">Microsoft .NET Framework version 4.0–4.8 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-387">The Microsoft .NET Framework version 4.0–4.8 (CLR 4.0)</span></span> | <https://dotnet.microsoft.com/download/thank-you/net48-offline> |

### <a name="step-1-plan-your-domain-name-and-dns-zones"></a><a name="plandomain"></a><span data-ttu-id="b094f-388">手順 1、</span><span class="sxs-lookup"><span data-stu-id="b094f-388">Step 1.</span></span> <span data-ttu-id="b094f-389">ドメイン名と DNS ゾーンの計画</span><span class="sxs-lookup"><span data-stu-id="b094f-389">Plan your domain name and DNS zones</span></span>

<span data-ttu-id="b094f-390">AOS のプロダクション インストールには、公的に登録されたドメイン名を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b094f-390">We recommend that you use a publicly registered domain name for your production installation of AOS.</span></span> <span data-ttu-id="b094f-391">このようにして、外部アクセスが必要な場合は、ネットワークの外部からインストールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b094f-391">In that way, the installation can be accessed outside the network, if outside access is required.</span></span>

<span data-ttu-id="b094f-392">たとえば、会社のドメインが contoso.com の場合、Finance + Operations は d365ffo.onprem.contoso.com であり、ホスト名は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="b094f-392">For example, if your company's domain is contoso.com, your zone for Finance + Operations might be d365ffo.onprem.contoso.com, and the host names might be as follows:</span></span>

- <span data-ttu-id="b094f-393">AOS の機械の場合 ax.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-393">ax.d365ffo.onprem.contoso.com for AOS machines</span></span>
- <span data-ttu-id="b094f-394">Service Fabric クラスターの場合 sf.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-394">sf.d365ffo.onprem.contoso.com for the Service Fabric cluster</span></span>

### <a name="step-2-plan-and-acquire-your-certificates"></a><a name="plancert"></a><span data-ttu-id="b094f-395">手順 2、</span><span class="sxs-lookup"><span data-stu-id="b094f-395">Step 2.</span></span> <span data-ttu-id="b094f-396">証明書の計画と取得</span><span class="sxs-lookup"><span data-stu-id="b094f-396">Plan and acquire your certificates</span></span>

<span data-ttu-id="b094f-397">Service Fabric Cluster と展開されているすべてのアプリケーションを保護するには、Secure Sockets Layer (SSL) 証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-397">Secure Sockets Layer (SSL) certificates are required to secure a Service Fabric cluster and all the applications that are deployed.</span></span> <span data-ttu-id="b094f-398">プロダクションとサンドボックスのワークロードについては、[DigiCert](https://www.digicert.com/ssl-certificate/)、[Comodo](https://ssl.comodo.com/)、[Symantec](https://www.websecurity.symantec.com/ssl-certificate)、[GoDaddy](https://www.godaddy.com/web-security/ssl-certificate)、または [GlobalSign](https://www.globalsign.com/en/ssl/) などの認証局から証明書を取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b094f-398">For your production and sandbox workloads, we recommend that you acquire certificates from a certificate authority (CA) such as [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate), or [GlobalSign](https://www.globalsign.com/en/ssl/).</span></span> <span data-ttu-id="b094f-399">ドメインが [AD CS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772393(v=ws.10)) で設定されている場合は、Microsoft セットアップ スクリプトを使用してテンプレートと証明書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-399">If your domain is set up with [AD CS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772393(v=ws.10)), you can use the Microsoft setup scripts to create the templates and certificates.</span></span> <span data-ttu-id="b094f-400">証明書ごとに、プライベート キーが作成されたキーの交換を含める必要があり、個人情報交換 (.pfx) ファイルにエクスポート可能な必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-400">Each certificate must contain a private key that was created for key exchange, and it must be exportable to a Personal Information Exchange (.pfx) file.</span></span>

<span data-ttu-id="b094f-401">自己署名証明書は、テスト目的でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-401">Self-signed certificates can be used only for testing purposes.</span></span> <span data-ttu-id="b094f-402">便宜上、LCS で提供されるセットアップ スクリプトには、自己署名証明書を生成およびエクスポートするスクリプトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b094f-402">For the sake of convenience, the setup scripts that are provided in LCS include scripts that generate and export self-signed certificates.</span></span> <span data-ttu-id="b094f-403">自己署名スクリプトを使用している場合は、このトピックの後の手順で作成スクリプトを実行するように指示されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-403">If you're using self-signed scripts, you will be instructed to run the creation scripts during later steps in this topic.</span></span> <span data-ttu-id="b094f-404">前述の通り、これらの証明書はテスト目的でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-404">As has been mentioned, these certificates can be used only for testing purposes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b094f-405">Microsoft は、AD CS による自動証明書の作成をサポートして、セットアップ スクリプトによる自己署名証明書の生成のサポートを終了する予定です。</span><span class="sxs-lookup"><span data-stu-id="b094f-405">Microsoft plans to discontinue support for the generation of self-signed certificates through the setup scripts, in favor of automatic certificate creation through AD CS.</span></span>

<span data-ttu-id="b094f-406">証明書の推奨設定を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b094f-406">Here are the recommended settings for certificates:</span></span>

- <span data-ttu-id="b094f-407">**署名アルゴリズム:** sha256RSA</span><span class="sxs-lookup"><span data-stu-id="b094f-407">**Signature algorithm:** sha256RSA</span></span>
- <span data-ttu-id="b094f-408">**署名ハッシュ アルゴリズム:** sha256</span><span class="sxs-lookup"><span data-stu-id="b094f-408">**Signature hash algorithm:** sha256</span></span>
- <span data-ttu-id="b094f-409">**公開キー:** RSA (2048 ビット)</span><span class="sxs-lookup"><span data-stu-id="b094f-409">**Public key:** RSA (2048 bits)</span></span>
- <span data-ttu-id="b094f-410">**Thumbprint アルゴリズム:** sha1</span><span class="sxs-lookup"><span data-stu-id="b094f-410">**Thumbprint algorithm:** sha1</span></span>

| <span data-ttu-id="b094f-411">目的</span><span class="sxs-lookup"><span data-stu-id="b094f-411">Purpose</span></span>                                      | <span data-ttu-id="b094f-412">説明</span><span class="sxs-lookup"><span data-stu-id="b094f-412">Explanation</span></span> | <span data-ttu-id="b094f-413">追加条件</span><span class="sxs-lookup"><span data-stu-id="b094f-413">Additional requirements</span></span> |
|----------------------------------------------|-------------|-------------------------|
| <span data-ttu-id="b094f-414">SQL Server SSL 証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-414">SQL Server SSL certificate</span></span>                   | <span data-ttu-id="b094f-415">この証明書は、ネットワーク上の SQL Server インスタンスとクライアント アプリケーションの間で転送されるデータを暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-415">This certificate is used to encrypt data that is transmitted across a network between an instance of SQL Server and a client application.</span></span> | <p><span data-ttu-id="b094f-416">証明書の場合、ドメイン名は SQL Server のインスタンスまたはリスナーの完全修飾ドメイン名 (FQDN) と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-416">The domain name of the certificate should match the fully qualified domain name (FQDN) of the SQL Server instance or listener.</span></span> <span data-ttu-id="b094f-417">たとえば、SQL のリスナーが DAX7SQLAOSQLA のコンピューターにホストされている場合、証明書のドメイン ネーム システム (DNS) 名は、DAX7SQLAOSQLA.contoso.com です。</span><span class="sxs-lookup"><span data-stu-id="b094f-417">For example, if the SQL listener is hosted on machine DAX7SQLAOSQLA, the certificate's Domain Name System (DNS) name is DAX7SQLAOSQLA.contoso.com.</span></span></p><ul><li><span data-ttu-id="b094f-418">**共通名 (CN):** DAX7SQLAOSQLA.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-418">**Common name (CN):** DAX7SQLAOSQLA.contoso.com</span></span></li><li><span data-ttu-id="b094f-419">**DNS 名:** DAX7SQLAOSQLA.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-419">**DNS name:** DAX7SQLAOSQLA.contoso.com</span></span></li></ul> |
| <span data-ttu-id="b094f-420">Service Fabric Server 証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-420">Service Fabric Server certificate</span></span>            | <span data-ttu-id="b094f-421">この証明書を使用して、Service Fabric ノード間のノードからノードの通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="b094f-421">This certificate is used to help secure the node-to-node communication between the Service Fabric nodes.</span></span> <span data-ttu-id="b094f-422">これはクラスターに接続するクライアントに提示されるサーバー証明書としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-422">It's also used as the server certificate that is presented to the client that connects to the cluster.</span></span> | <p><span data-ttu-id="b094f-423">この証明書については、\*.contoso.com などのドメイン用ワイルドカード SSL 証明書を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="b094f-423">For this certificate, you can also use the wildcard SSL certificate for your domain, such as \*.contoso.com.</span></span> <span data-ttu-id="b094f-424">(詳細については、このテーブルに続くテキストを参照してください。) それ以外の場合は、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b094f-424">(For more information, see the text that follows this table.) Otherwise, use the following values:</span></span></p><ul><li><span data-ttu-id="b094f-425">**CN:** sf.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-425">**CN:** sf.d365ffo.onprem.contoso.com</span></span></li><li><span data-ttu-id="b094f-426">**DNS 名:** sf.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-426">**DNS name:** sf.d365ffo.onprem.contoso.com</span></span></li></ul> |
| <span data-ttu-id="b094f-427">Service Fabric Client 証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-427">Service Fabric Client certificate</span></span>            | <span data-ttu-id="b094f-428">クライアントはこの証明書を使用して Service Fabric cluster を表示および管理します。</span><span class="sxs-lookup"><span data-stu-id="b094f-428">Clients use this certificate to view and manage the Service Fabric cluster.</span></span> | <ul><li><span data-ttu-id="b094f-429">**CN:** client.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-429">**CN:** client.d365ffo.onprem.contoso.com</span></span></li><li><span data-ttu-id="b094f-430">**DNS 名:** client.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-430">**DNS name:** client.d365ffo.onprem.contoso.com</span></span></li></ul> |
| <span data-ttu-id="b094f-431">暗号化証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-431">Encipherment certificate</span></span>                     | <span data-ttu-id="b094f-432">この証明書は、SQL Server パスワードとユーザー アカウントのパスワードなどの重要な情報を暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-432">This certificate is used to encrypt sensitive information such as the SQL Server password and user account passwords.</span></span> | <p><span data-ttu-id="b094f-433">証明書は、**Microsoft Enhanced Cryptographic Provider v1.0** プロバイダーを使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-433">The certificate must be created by using the **Microsoft Enhanced Cryptographic Provider v1.0** provider.</span></span></p><p><span data-ttu-id="b094f-434">証明書キーの使用にはデータ暗号化 (10) が含まれている必要があり、サーバー認証またはクライアント認証は含めないでください。</span><span class="sxs-lookup"><span data-stu-id="b094f-434">The certificate key usage must include Data Encipherment (10), and should not include server authentication or client authentication.</span></span></p><p><span data-ttu-id="b094f-435">詳細については、[Service Fabric アプリケーションでの機密情報の管理](/azure/service-fabric/service-fabric-application-secret-management) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-435">For more information, see [Managing secrets in Service Fabric applications](/azure/service-fabric/service-fabric-application-secret-management).</span></span></p><ul><li><span data-ttu-id="b094f-436">**CN:** axdataenciphermentcert</span><span class="sxs-lookup"><span data-stu-id="b094f-436">**CN:** axdataenciphermentcert</span></span></li><li><span data-ttu-id="b094f-437">**DNS 名:** axdataenciphermentcert</span><span class="sxs-lookup"><span data-stu-id="b094f-437">**DNS name:** axdataenciphermentcert</span></span></li></ul> |
| <span data-ttu-id="b094f-438">AOS SSL 証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-438">AOS SSL certificate</span></span>                          | <p><span data-ttu-id="b094f-439">この証明書は、AOS Web サイトに接続するクライアントに提示されるサーバー証明書として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-439">This certificate is used as the server certificate that is presented to the client for the AOS website.</span></span> <span data-ttu-id="b094f-440">また、WCF (Windows Communication Foundation) / SOAP (Simple Object Access Protocol) 証明書を有効にするためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-440">It's also used to enable Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP) certificates.</span></span></p> | <p><span data-ttu-id="b094f-441">Service Fabric サーバー証明書として使用したのと同じワイルドカード SSL 証明書を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-441">You can use the same wildcard SSL certificate that you used as the Service Fabric server certificate.</span></span> <span data-ttu-id="b094f-442">それ以外の場合は、次の値を使用します:</span><span class="sxs-lookup"><span data-stu-id="b094f-442">Otherwise, use the following values:</span></span></p><ul><li><span data-ttu-id="b094f-443">**CN:** ax.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-443">**CN:** ax.d365ffo.onprem.contoso.com</span></span></li><li><span data-ttu-id="b094f-444">**DNS 名:** ax.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-444">**DNS name:** ax.d365ffo.onprem.contoso.com</span></span></li></ul> |
| <span data-ttu-id="b094f-445">セッション認証証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-445">Session Authentication certificate</span></span>           | <span data-ttu-id="b094f-446">AOS はこの証明書を使用してユーザーのセッション情報を保護します。</span><span class="sxs-lookup"><span data-stu-id="b094f-446">AOS uses this certificate to help secure a user's session information.</span></span> | <p><span data-ttu-id="b094f-447">この証明書は、LCS からの展開時に使用されるファイル共有証明書です。</span><span class="sxs-lookup"><span data-stu-id="b094f-447">This certificate is also the File Share certificate that will be used at the time of deployment from LCS.</span></span></p><ul><li><span data-ttu-id="b094f-448">**CN:** SessionAuthentication</span><span class="sxs-lookup"><span data-stu-id="b094f-448">**CN:** SessionAuthentication</span></span></li><li><span data-ttu-id="b094f-449">**DNS 名:** SessionAuthentication</span><span class="sxs-lookup"><span data-stu-id="b094f-449">**DNS name:** SessionAuthentication</span></span> </li></ul> |
| <span data-ttu-id="b094f-450">データの暗号化証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-450">Data Encryption certificate</span></span>                  | <span data-ttu-id="b094f-451">AOS はこの証明書を使用して機密情報を暗号化します。</span><span class="sxs-lookup"><span data-stu-id="b094f-451">AOS uses this certificate to encrypt sensitive information.</span></span> | <p><span data-ttu-id="b094f-452">この証明書は、**Microsoft Enhanced RSA and AES Cryptographic Provider** プロバイダーを使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-452">This certificate must be created by using the **Microsoft Enhanced RSA and AES Cryptographic Provider** provider.</span></span></p><ul><li><span data-ttu-id="b094f-453">**CN:** DataEncryption</span><span class="sxs-lookup"><span data-stu-id="b094f-453">**CN:** DataEncryption</span></span></li><li><span data-ttu-id="b094f-454">**DNS 名:** DataEncryption</span><span class="sxs-lookup"><span data-stu-id="b094f-454">**DNS name:** DataEncryption</span></span></li></ul> |
| <span data-ttu-id="b094f-455">データ署名の証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-455">Data Signing certificate</span></span>                     | <span data-ttu-id="b094f-456">AOS はこの証明書を使用して機密情報を暗号化します。</span><span class="sxs-lookup"><span data-stu-id="b094f-456">AOS uses this certificate to encrypt sensitive information.</span></span> | <p><span data-ttu-id="b094f-457">この証明書はデータ暗号化証明書とは別のもので、**Microsoft Enhanced RSA and AES Cryptographic Provider** プロバイダーを使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-457">This certificate is separate from the Data Encryption certificate and must be created by using the **Microsoft Enhanced RSA and AES Cryptographic Provider** provider.</span></span></p><ul><li><span data-ttu-id="b094f-458">**CN:** DataSigning</span><span class="sxs-lookup"><span data-stu-id="b094f-458">**CN:** DataSigning</span></span></li><li><span data-ttu-id="b094f-459">**DNS 名:** DataSigning</span><span class="sxs-lookup"><span data-stu-id="b094f-459">**DNS name:** DataSigning</span></span></li></ul> |
| <span data-ttu-id="b094f-460">Financial Reporting クライアント証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-460">Financial Reporting Client certificate</span></span>       | <span data-ttu-id="b094f-461">この証明書を使用して、Financial Reporting サービスと AOS 間の通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="b094f-461">This certificate is used to help secure the communication between the Financial Reporting services and AOS.</span></span> | <ul><li><span data-ttu-id="b094f-462">**CN:** FinancialReporting</span><span class="sxs-lookup"><span data-stu-id="b094f-462">**CN:** FinancialReporting</span></span></li><li><span data-ttu-id="b094f-463">**DNS 名:** FinancialReporting</span><span class="sxs-lookup"><span data-stu-id="b094f-463">**DNS name:** FinancialReporting</span></span></li></ul> |
| <span data-ttu-id="b094f-464">報告証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-464">Reporting certificate</span></span>                        | <span data-ttu-id="b094f-465">この証明書を使用して、SSRS と AOS 間の通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="b094f-465">This certificate is used to help secure the communication between SSRS and AOS.</span></span>| <p><span data-ttu-id="b094f-466">**重要:** Financial Reporting クライアント証明書を再利用 **しない** でください。</span><span class="sxs-lookup"><span data-stu-id="b094f-466">**Important:** Do **not** reuse the Financial Reporting Client certificate.</span></span></p><ul><li><span data-ttu-id="b094f-467">**CN:** ReportingService</span><span class="sxs-lookup"><span data-stu-id="b094f-467">**CN:** ReportingService</span></span></li><li><span data-ttu-id="b094f-468">**DNS 名:** ReportingService</span><span class="sxs-lookup"><span data-stu-id="b094f-468">**DNS name:** ReportingService</span></span></li></ul> |
| <span data-ttu-id="b094f-469">SSRS Web サーバー証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-469">SSRS Web Server certificate</span></span>                  | <span data-ttu-id="b094f-470">この証明書は、SSRS Web サーバーに接続するクライアント (AOS) に提示されるサーバー証明書として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-470">This certificate is used as the server certificate that is presented to the client (AOS) for the SSRS web server.</span></span> | <p><span data-ttu-id="b094f-471">証明書のドメイン名は SSRS ノードの SSRN と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-471">The domain name of the certificate should match the FQDN of the SSRS node.</span></span></p><ul><li><span data-ttu-id="b094f-472">**CN:** BI1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-472">**CN:** BI1.contoso.com</span></span></li><li><span data-ttu-id="b094f-473">**DNS 名:** BI1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-473">**DNS name:** BI1.contoso.com</span></span></li></ul>
| <span data-ttu-id="b094f-474">オンプレミス ローカル エージェント証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-474">On-Premises local agent certificate</span></span>           | <p><span data-ttu-id="b094f-475">この証明書は、オンプレミスと LCS でホストされているローカル エージェント間の通信を保護するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b094f-475">This certificate is used to help secure the communication between a local agent that is hosted on-premises and on LCS.</span></span> <span data-ttu-id="b094f-476">これにより、Azure AD テナントに代わってローカル エージェントが動作し、LCS と通信して展開を編成および監視することができます。</span><span class="sxs-lookup"><span data-stu-id="b094f-476">It enables the local agent to act on behalf of your Azure AD tenant, and to communicate with LCS to orchestrate and monitor deployments.</span></span></p><p><span data-ttu-id="b094f-477">**注記:** テナントにはオンプレミス ローカル エージェント証明書が 1 つだけ必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-477">**Note:** Only one on-premises local agent certificate is required for a tenant.</span></span></p> | <ul><li><span data-ttu-id="b094f-478">**CN:** OnPremLocalAgent</span><span class="sxs-lookup"><span data-stu-id="b094f-478">**CN:** OnPremLocalAgent</span></span></li><li><span data-ttu-id="b094f-479">**DNS 名:** OnPremLocalAgent</span><span class="sxs-lookup"><span data-stu-id="b094f-479">**DNS name:** OnPremLocalAgent</span></span></li></ul> |

<span data-ttu-id="b094f-480">ドメインのワイルドカード SSL 証明書を使用して、Service Fabric サーバー証明書と AOS SSL 証明書を結合できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-480">You can use the wildcard SSL certificate for your domain to combine the Service Fabric Server certificate and the AOS SSL certificate.</span></span>

<span data-ttu-id="b094f-481">以下は、AOS SSL 証明書と組み合わせた Service Fabric サーバー証明書の例です。</span><span class="sxs-lookup"><span data-stu-id="b094f-481">Here is an example of a Service Fabric Server certificate that is combined with an AOS SSL certificate.</span></span>

#### <a name="subject-name"></a><span data-ttu-id="b094f-482">件名</span><span class="sxs-lookup"><span data-stu-id="b094f-482">Subject name</span></span>

```Text
CN = *.d365ffo.onprem.contoso.com
```

#### <a name="subject-alternative-names"></a><span data-ttu-id="b094f-483">件名の代替名</span><span class="sxs-lookup"><span data-stu-id="b094f-483">Subject alternative names</span></span>

```Text
DNS Name=ax.d365ffo.onprem.contoso.com
DNS Name=sf.d365ffo.onprem.contoso.com
DNS Name=*.d365ffo.onprem.contoso.com
```

> [!IMPORTANT]
> <span data-ttu-id="b094f-484">ワイルドカード証明書を使用して、発行先となるドメインの最初のレベル サブドメインのみをセキュリティ保護できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-484">You can use the wildcard certificate to help secure only the first-level subdomain of the domain that it's issued to.</span></span> <span data-ttu-id="b094f-485">したがって、\*.onprem.contoso.com の証明書は ax.d365ffo.onprem.contoso.com では無効になります。</span><span class="sxs-lookup"><span data-stu-id="b094f-485">Therefore, a certificate for \*.onprem.contoso.com won't be valid for ax.d365ffo.onprem.contoso.com.</span></span>

### <a name="step-3-plan-your-users-and-service-accounts"></a><a name="plansvcacct"></a><span data-ttu-id="b094f-486">手順 3、</span><span class="sxs-lookup"><span data-stu-id="b094f-486">Step 3.</span></span> <span data-ttu-id="b094f-487">ユーザーとサービス アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="b094f-487">Plan your users and service accounts</span></span>

<span data-ttu-id="b094f-488">Finance + Operations を機能させるために、いくつかのユーザー アカウントまたはサービス アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-488">You must create several user or service accounts for Finance + Operations to work.</span></span> <span data-ttu-id="b094f-489">サービス アカウントの管理グループ (gMSAs)、ドメイン アカウント、および SQL アカウントの組み合わせを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-489">You must create a combination of group managed service accounts (gMSAs), domain accounts, and SQL accounts.</span></span> <span data-ttu-id="b094f-490">次の表は、このトピックで使用されるユーザー アカウント、その目的、および名前の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="b094f-490">The following table shows the user accounts, their purpose, and example names that will be used in this topic.</span></span>

| <span data-ttu-id="b094f-491">ユーザー アカウント</span><span class="sxs-lookup"><span data-stu-id="b094f-491">User account</span></span>                                            | <span data-ttu-id="b094f-492">種類</span><span class="sxs-lookup"><span data-stu-id="b094f-492">Type</span></span> | <span data-ttu-id="b094f-493">目的</span><span class="sxs-lookup"><span data-stu-id="b094f-493">Purpose</span></span> | <span data-ttu-id="b094f-494">ユーザー名</span><span class="sxs-lookup"><span data-stu-id="b094f-494">User name</span></span> |
|---------------------------------------------------------|------|---------|-----------|
| <span data-ttu-id="b094f-495">財務レポート アプリケーション サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="b094f-495">Financial Reporting Application Service Account</span></span>         | <span data-ttu-id="b094f-496">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-496">gMSA</span></span> | | <span data-ttu-id="b094f-497">Contoso\\svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="b094f-497">Contoso\\svc-FRAS$</span></span> |
| <span data-ttu-id="b094f-498">財務レポート プロセス サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="b094f-498">Financial Reporting Process Service Account</span></span>             | <span data-ttu-id="b094f-499">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-499">gMSA</span></span> | | <span data-ttu-id="b094f-500">Contoso\\svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="b094f-500">Contoso\\svc-FRPS$</span></span> |
| <span data-ttu-id="b094f-501">財務レポート クリック ワンス デザイナー サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="b094f-501">Financial Reporting Click Once Designer Service Account</span></span> | <span data-ttu-id="b094f-502">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-502">gMSA</span></span> | | <span data-ttu-id="b094f-503">Contoso\\svc-FRCO$</span><span class="sxs-lookup"><span data-stu-id="b094f-503">Contoso\\svc-FRCO$</span></span> |
| <span data-ttu-id="b094f-504">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="b094f-504">AOS Service Account</span></span>                                     | <span data-ttu-id="b094f-505">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-505">gMSA</span></span> | <span data-ttu-id="b094f-506">将来校正するためにこのユーザーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-506">You should create this user for future proofing.</span></span> <span data-ttu-id="b094f-507">Microsoft は今後のリリースで、AOS を gMSA と連携させる予定です。</span><span class="sxs-lookup"><span data-stu-id="b094f-507">Microsoft plans to enable AOS to work with the gMSA in upcoming releases.</span></span> <span data-ttu-id="b094f-508">このユーザーを設定時に作成することで、gMSA へのシームレスな移行を確実にすることができます。\*</span><span class="sxs-lookup"><span data-stu-id="b094f-508">By creating this user at the time of setup, you help to ensure a seamless transition to the gMSA.\*</span></span> | <span data-ttu-id="b094f-509">Contoso\\svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="b094f-509">Contoso\\svc-AXSF$</span></span> |
| <span data-ttu-id="b094f-510">SSRS ブートストラッパー サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="b094f-510">SSRS bootstrapper Service Account</span></span>                       | <span data-ttu-id="b094f-511">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-511">gMSA</span></span> | <span data-ttu-id="b094f-512">レポート サービス ブートストラッパーは、このアカウントを使用して SSRS サービスをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b094f-512">The reporting service bootstrapper uses this account to configure the SSRS service.</span></span> | <span data-ttu-id="b094f-513">Contoso\\svc-ReportSvc$</span><span class="sxs-lookup"><span data-stu-id="b094f-513">Contoso\\svc-ReportSvc$</span></span> |
| <span data-ttu-id="b094f-514">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="b094f-514">AOS Service Account</span></span>                                     | <span data-ttu-id="b094f-515">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="b094f-515">Domain account</span></span> | <span data-ttu-id="b094f-516">AOS は、一般提供 (GA) リリースでこのユーザーを使用します。\*</span><span class="sxs-lookup"><span data-stu-id="b094f-516">AOS uses this user in the general availability (GA) release.\*</span></span> | <span data-ttu-id="b094f-517">Contoso\\ AXServiceUser</span><span class="sxs-lookup"><span data-stu-id="b094f-517">Contoso\\AXServiceUser</span></span> |
| <span data-ttu-id="b094f-518">AOS SQL DB 管理者ユーザー</span><span class="sxs-lookup"><span data-stu-id="b094f-518">AOS SQL DB Admin user</span></span>                                   | <span data-ttu-id="b094f-519">SQL ユーザー</span><span class="sxs-lookup"><span data-stu-id="b094f-519">SQL user</span></span> | <span data-ttu-id="b094f-520">Finance + Operations は、このユーザーを使用して SQL\*\* を認証します。</span><span class="sxs-lookup"><span data-stu-id="b094f-520">Finance + Operations uses this user to authenticate with SQL\*\*.</span></span> <span data-ttu-id="b094f-521">このユーザーは、今後のリリース \*\*\* で gMSA ユーザーにも置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="b094f-521">This user will also be replaced by the gMSA user in upcoming releases\*\*\*.</span></span> | <span data-ttu-id="b094f-522">AXDBAdmin</span><span class="sxs-lookup"><span data-stu-id="b094f-522">AXDBAdmin</span></span> |
| <span data-ttu-id="b094f-523">ローカル配置エージェント サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="b094f-523">Local Deployment Agent Service Account</span></span>                  | <span data-ttu-id="b094f-524">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-524">gMSA</span></span> | <span data-ttu-id="b094f-525">ローカル エージェントはこのアカウントを使用して、さまざまなノードでの展開を調整します。</span><span class="sxs-lookup"><span data-stu-id="b094f-525">The local agent uses this account to orchestrate the deployment on various nodes.</span></span> | <span data-ttu-id="b094f-526">Contoso\\ Svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="b094f-526">Contoso\\Svc-LocalAgent$</span></span> |

<span data-ttu-id="b094f-527">\* これらのアカウントでは、地域の設定を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="b094f-527">\* These accounts should not have their regional settings changed.</span></span> <span data-ttu-id="b094f-528">既定の EN-US リージョン設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-528">They should have the default EN-US region settings.</span></span> 

<span data-ttu-id="b094f-529">\*\* SQL ユーザーのパスワードに特殊文字が含まれている場合、展開中に問題が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-529">\*\* If the password of the SQL user contains special characters, you might encounter issues during deployment.</span></span>

<span data-ttu-id="b094f-530">\*\*\* SQL 認証で使用する SQL ユーザ名とパスワードは暗号化されてファイル共有に保存されているため、安全性が確保されています。</span><span class="sxs-lookup"><span data-stu-id="b094f-530">\*\*\* The SQL user name and password for SQL authentication are secured because they are encrypted and stored in the file share.</span></span>

### <a name="step-4-create-dns-zones-and-add-a-records"></a><a name="createdns"></a><span data-ttu-id="b094f-531">手順 4、</span><span class="sxs-lookup"><span data-stu-id="b094f-531">Step 4.</span></span> <span data-ttu-id="b094f-532">DNS ゾーンの作成と A レコードの追加</span><span class="sxs-lookup"><span data-stu-id="b094f-532">Create DNS zones and add A records</span></span>

<span data-ttu-id="b094f-533">DNS は AD DS と統合されており、ネットワーク内のリソースを整理、管理、検索することができます。</span><span class="sxs-lookup"><span data-stu-id="b094f-533">DNS is integrated with AD DS, and lets you organize, manage, and find resources in a network.</span></span> <span data-ttu-id="b094f-534">次の手順では、AOS ホスト名と Service Fabric Cluster の DNS 前方参照ゾーンと A レコードを作成する手順を示します。</span><span class="sxs-lookup"><span data-stu-id="b094f-534">The following procedures show how to create a DNS forward lookup zone and A records for the AOS host name and Service Fabric cluster.</span></span> <span data-ttu-id="b094f-535">この例では、DNS ゾーン名は d365ffo.onprem.contoso.com で、A レコード/ホスト名は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b094f-535">In this example, the DNS zone name is d365ffo.onprem.contoso.com, and the A records/host names are as follows:</span></span>

- <span data-ttu-id="b094f-536">AOS の機械の場合 **ax**.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-536">**ax**.d365ffo.onprem.contoso.com for AOS machines</span></span>
- <span data-ttu-id="b094f-537">Service Fabric クラスターの場合 **sf**.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b094f-537">**sf**.d365ffo.onprem.contoso.com for the Service Fabric cluster</span></span>

#### <a name="add-a-dns-zone"></a><span data-ttu-id="b094f-538">DNS ゾーンの追加</span><span class="sxs-lookup"><span data-stu-id="b094f-538">Add a DNS zone</span></span>

1. <span data-ttu-id="b094f-539">ドメイン コントローラー コンピューターにサインインして、**スタート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-539">Sign in to the domain controller machine, select **Start**.</span></span> <span data-ttu-id="b094f-540">次に、**dnsmgmt.msc** を入力し **dnsmgmt (DNS)** アプリケーションを選択して、DNS マネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="b094f-540">Then open DNS Manager by entering **dnsmgmt.msc** and selecting the **dnsmgmt (DNS)** application.</span></span>
2. <span data-ttu-id="b094f-541">コンソール ツリーでドメイン コントローラー名を右クリックし、**新しいゾーン** \> **次へ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-541">Right-click the domain controller name in the console tree, and then select **New Zone** \> **Next**.</span></span>
3. <span data-ttu-id="b094f-542">**プライマリ ゾーン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-542">Select **Primary Zone**.</span></span>
4. <span data-ttu-id="b094f-543">**Active Directory にゾーンを保存 (DNS サーバーが書き込み可能なドメイン コントローラーの場合にのみ使用可能)** のチェック ボックスが選択されたままの状態で、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-543">Leave the **Store the zone in Active Directory (available only if the DNS Server is a writeable domain controller** check box selected, and then select **Next**.</span></span>
5. <span data-ttu-id="b094f-544">**このドメインのドメイン コントローラーで実行されているすべての DNS サーバーに対して : Contoso.com** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-544">Select **To all DNS Servers running on Domain Controllers in this domain: Contoso.com**, and then select **Next**.</span></span>
6. <span data-ttu-id="b094f-545">**前方参照ゾーン** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-545">Select **Forward Lookup Zone**, and then select **Next**.</span></span>
7. <span data-ttu-id="b094f-546">設定するゾーン名を入力し、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b094f-546">Enter the zone name for your setup, and then select **Next**.</span></span> <span data-ttu-id="b094f-547">たとえば、**d365ffo.onprem.contoso.com** と入力します。</span><span class="sxs-lookup"><span data-stu-id="b094f-547">For example, enter **d365ffo.onprem.contoso.com**.</span></span>
8. <span data-ttu-id="b094f-548">**動的更新を許可しない** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-548">Select **Do not allow dynamic updates**, and then select **Next**.</span></span>
9. <span data-ttu-id="b094f-549">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-549">Select **Finish**.</span></span>

#### <a name="set-up-an-a-record-for-aos"></a><span data-ttu-id="b094f-550">AOS の A レコードを設定する</span><span class="sxs-lookup"><span data-stu-id="b094f-550">Set up an A record for AOS</span></span>

<span data-ttu-id="b094f-551">新しい DNS ゾーンで、**AOSNodeType** タイプの Service Fabric cluster ノード **ごと** に、ax.d365ffo.onprem.contoso.com という名前の A レコードを 1 つ作成します。</span><span class="sxs-lookup"><span data-stu-id="b094f-551">In the new DNS zone, for **each** Service Fabric cluster node of the **AOSNodeType** type, create one A record that is named ax.d365ffo.onprem.contoso.com.</span></span> <span data-ttu-id="b094f-552">他のノード タイプの A レコードは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="b094f-552">Don't create A records for the other node types.</span></span>

1. <span data-ttu-id="b094f-553">DNS マネージャーの **前方参照ゾーン** フォルダーで、新しく作成したゾーンを検索します。</span><span class="sxs-lookup"><span data-stu-id="b094f-553">Find the newly created zone under the **Forward Lookup Zones** folder in DNS Manager.</span></span>
2. <span data-ttu-id="b094f-554">新しいゾーンを選択したまま (または右クリック) にしてから、**新しいホスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-554">Select and hold (or right-click) the new zone, and then select **New Host**.</span></span>
3. <span data-ttu-id="b094f-555">Service Fabric ノードの 名前および IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="b094f-555">Enter the name and IP address of the Service Fabric node.</span></span> <span data-ttu-id="b094f-556">(たとえば、**ax** を名前として、**10.179.108.12** を IP アドレスとして入力します。) 次に **ホストの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-556">(For example, enter **ax** as the name and **10.179.108.12** as the IP address.) Then select **Add Host**.</span></span>
4. <span data-ttu-id="b094f-557">両方のチェック ボックスをオフのままにします。</span><span class="sxs-lookup"><span data-stu-id="b094f-557">Leave both check boxes cleared.</span></span>
5. <span data-ttu-id="b094f-558">追加の AOS ノードごとに手順 1 から 4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b094f-558">Repeat steps 1 through 4 for each additional AOS node.</span></span>

#### <a name="set-up-an-a-record-for-the-orchestrator"></a><span data-ttu-id="b094f-559">Orchestrator の A レコードを設定する</span><span class="sxs-lookup"><span data-stu-id="b094f-559">Set up an A record for the orchestrator</span></span>

<span data-ttu-id="b094f-560">新しい DNS ゾーンで、**OrchestratorType** タイプの Service Fabric Cluster **ごと** に、sf.d365ffo.onprem.contoso.com という名前の A レコードを 1 つ作成します。</span><span class="sxs-lookup"><span data-stu-id="b094f-560">In the new DNS zone, for **each** Service Fabric cluster node of the **OrchestratorType** type, create an A record that is named sf.d365ffo.onprem.contoso.com.</span></span> <span data-ttu-id="b094f-561">他のノード タイプの A レコードは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="b094f-561">Don't create A records for the other node types.</span></span>

1. <span data-ttu-id="b094f-562">新しいゾーンを選択したまま (または右クリック) にしてから、**新しいホスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-562">Select and hold (or right-click) the new zone, and then select **New Host**.</span></span>
2. <span data-ttu-id="b094f-563">Service Fabric ノードの 名前および IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="b094f-563">Enter the name and IP address of the Service Fabric node.</span></span> <span data-ttu-id="b094f-564">(たとえば、**sf** を名前として、**10.179.108.15** を IP アドレスとして入力します。) 次に **ホストの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-564">(For example, enter **sf** as the name and **10.179.108.15** as the IP address.) Then select **Add Host**.</span></span>
3. <span data-ttu-id="b094f-565">両方のチェック ボックスをオフのままにします。</span><span class="sxs-lookup"><span data-stu-id="b094f-565">Leave both check boxes cleared.</span></span>
4. <span data-ttu-id="b094f-566">追加のオーケストレーター ノードごとに手順 1 から 3 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b094f-566">Repeat steps 1 through 3 for each additional orchestrator node.</span></span>

### <a name="step-5-join-vms-to-the-domain"></a><a name="joindomain"></a><span data-ttu-id="b094f-567">手順 5、</span><span class="sxs-lookup"><span data-stu-id="b094f-567">Step 5.</span></span> <span data-ttu-id="b094f-568">VM のドメインへの参加</span><span class="sxs-lookup"><span data-stu-id="b094f-568">Join VMs to the domain</span></span>

<span data-ttu-id="b094f-569">各 VM をドメインに参加させるには、[コンピューターをドメインに参加させる](/windows-server/identity/ad-fs/deployment/join-a-computer-to-a-domain)の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="b094f-569">Join each VM to the domain by completing the steps in [Join a Computer to a Domain](/windows-server/identity/ad-fs/deployment/join-a-computer-to-a-domain).</span></span> <span data-ttu-id="b094f-570">または、次の Windows PowerShell スクリプトを使用します。</span><span class="sxs-lookup"><span data-stu-id="b094f-570">Alternatively, use the following Windows PowerShell script.</span></span>

```powershell
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
```

> [!IMPORTANT]
> <span data-ttu-id="b094f-571">ドメインにそれらを結合させた後、VM を再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-571">You must restart the VMs after you join them to the domain.</span></span>

### <a name="step-6-download-setup-scripts-from-lcs"></a><a name="downloadscripts"></a><span data-ttu-id="b094f-572">手順 6、</span><span class="sxs-lookup"><span data-stu-id="b094f-572">Step 6.</span></span> <span data-ttu-id="b094f-573">LCS からセットアップ スクリプトのダウンロード</span><span class="sxs-lookup"><span data-stu-id="b094f-573">Download setup scripts from LCS</span></span>

<span data-ttu-id="b094f-574">Microsoft ではセットアップ エクスペリエンスを向上させるためのスクリプトをいくつか紹介してきました。</span><span class="sxs-lookup"><span data-stu-id="b094f-574">Microsoft has provided several scripts to help improve the setup experience.</span></span> <span data-ttu-id="b094f-575">LCS からセットアップ スクリプトをダウンロードするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b094f-575">Follow these steps to download the setup scripts from LCS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b094f-576">スクリプトは、オンプレミス インフラストラクチャと同じドメイン内のコンピューターから実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-576">The scripts must be run from a computer that is in the same domain as the on-premises infrastructure.</span></span>

1. <span data-ttu-id="b094f-577">[LCS](https://lcs.dynamics.com/v2) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="b094f-577">Sign in to [LCS](https://lcs.dynamics.com/v2).</span></span>
2. <span data-ttu-id="b094f-578">ダッシュボードで、**共有アセット ライブラリ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-578">On the dashboard, select the **Shared asset library** tile.</span></span>
3. <span data-ttu-id="b094f-579">**モデル** を資産タイプとして選択してから、グリッドで、**Dynamics 365 for Operations オンプレミス - 展開スクリプト** の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-579">Select **Model** as the asset type, and then, in the grid, select the row for **Dynamics 365 for Operations on-premises - Deployment scripts**.</span></span>
4. <span data-ttu-id="b094f-580">**バージョン** を選択し、スクリプトの zip ファイルの最新版をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b094f-580">Select **Versions**, and download the latest version of the zip file for the scripts.</span></span>
5. <span data-ttu-id="b094f-581">zip ファイルをダウンロードした後、ファイルを選択したまま (または右クリック) にしてから、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-581">After the zip file is downloaded, select and hold (or right-click) it, and then select **Properties**.</span></span> <span data-ttu-id="b094f-582">**プロパティ** ダイアログ ボックスで、**ブロック解除** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-582">In the **Properties** dialog box, select the **Unblock** check box.</span></span>
6. <span data-ttu-id="b094f-583">zip ファイルをスクリプトの実行に使用するコンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="b094f-583">Copy the zip file to the machine that will be used to run the scripts.</span></span>
7. <span data-ttu-id="b094f-584">**infrastructure** という名前のフォルダーにファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="b094f-584">Unzip the files into a folder that is named **infrastructure**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b094f-585">このフォルダーの ConfigTemplate.xml ファイルにすべての編集を加えるよう確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-585">Make sure that all edits are made to the ConfigTemplate.xml file in this folder.</span></span>

### <a name="step-7-describe-your-configuration"></a><a name="describeconfig"></a><span data-ttu-id="b094f-586">手順 7、</span><span class="sxs-lookup"><span data-stu-id="b094f-586">Step 7.</span></span> <span data-ttu-id="b094f-587">コンフィギュレーションの記述</span><span class="sxs-lookup"><span data-stu-id="b094f-587">Describe your configuration</span></span>

<span data-ttu-id="b094f-588">インフラストラクチャのセットアップ スクリプトは、次のコンフィギュレーション ファイルを使用して設定を実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-588">The infrastructure setup scripts use the following configuration files to drive the setup:</span></span>

- <span data-ttu-id="b094f-589">infrastructure\\ConfigTemplate.xml</span><span class="sxs-lookup"><span data-stu-id="b094f-589">infrastructure\\ConfigTemplate.xml</span></span>
- <span data-ttu-id="b094f-590">infrastructure\\D365FO-OP\\NodeTopologyDefinition.xml</span><span class="sxs-lookup"><span data-stu-id="b094f-590">infrastructure\\D365FO-OP\\NodeTopologyDefinition.xml</span></span>
- <span data-ttu-id="b094f-591">infrastructure\\D365FO-OP\\DatabaseTopologyDefinition.xml</span><span class="sxs-lookup"><span data-stu-id="b094f-591">infrastructure\\D365FO-OP\\DatabaseTopologyDefinition.xml</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b094f-592">セットアップ スクリプトの正常に機能するように、環境のセットアップに基づいて、これらのコンフィギュレーション ファイルを適切なコンピュータ名、IP アドレス、サービス アカウント、およびドメインで更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-592">To ensure that the setup scripts work correctly, you must update these configuration files with the correct computer names, IP addresses, service accounts, and domain, based on the setup of your environment.</span></span>

<span data-ttu-id="b094f-593">infrastructure\\ConfigTemplate.xml コンフィギュレーション ファイルでは、次の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="b094f-593">The infrastructure\\ConfigTemplate.xml configuration file describes the following details:</span></span>

- <span data-ttu-id="b094f-594">アプリケーションが機能するために必要なサービス アカウント</span><span class="sxs-lookup"><span data-stu-id="b094f-594">The service accounts that are required for the application to work</span></span>
- <span data-ttu-id="b094f-595">通信を保護するために必要な証明書</span><span class="sxs-lookup"><span data-stu-id="b094f-595">The certificates that are required to help secure communications</span></span>
- <span data-ttu-id="b094f-596">データベース コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b094f-596">The database configuration</span></span>
- <span data-ttu-id="b094f-597">Service Fabric Cluster コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b094f-597">The Service Fabric cluster configuration</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b094f-598">Service Fabric cluster をコンフィギュレーションする際に、主要なノード タイプ (**OrchestratorType**) の 3 つのフォールト ドメインがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-598">When you configure the Service Fabric cluster, make sure that there are three fault domains for the Primary node type (**OrchestratorType**).</span></span> <span data-ttu-id="b094f-599">また、1 台のコンピューターに展開できるノードのタイプは 1 つだけになるようにします。</span><span class="sxs-lookup"><span data-stu-id="b094f-599">Also make sure that no more than one type of node is deployed on a single machine.</span></span>

<span data-ttu-id="b094f-600">Service Fabric ノード タイプごとに、infrastructure\\D365FO-OP\\NodeTopologyDefinition.xml コンフィギュレーション ファイルでは、次の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="b094f-600">For each Service Fabric node type, the infrastructure\\D365FO-OP\\NodeTopologyDefinition.xml configuration file describes the following details:</span></span>

- <span data-ttu-id="b094f-601">各ノード タイプとアプリケーション、ドメインとサービス アカウント、および証明書間のマッピング</span><span class="sxs-lookup"><span data-stu-id="b094f-601">The mapping between each node type and the application, domain and service accounts, and certificates</span></span>
- <span data-ttu-id="b094f-602">ユーザー アカウント制御 (UAC) が有効であるかどうか</span><span class="sxs-lookup"><span data-stu-id="b094f-602">Whether User Account Control (UAC) is enabled</span></span>
- <span data-ttu-id="b094f-603">Windows の機能とシステム ソフトウェアの前提条件</span><span class="sxs-lookup"><span data-stu-id="b094f-603">The prerequisites for Windows features and system software</span></span>
- <span data-ttu-id="b094f-604">厳密な名前の検証を有効にするかどうか</span><span class="sxs-lookup"><span data-stu-id="b094f-604">Whether strong name validation should be enabled</span></span>
- <span data-ttu-id="b094f-605">開くファイアウォール ポートの一覧</span><span class="sxs-lookup"><span data-stu-id="b094f-605">The list of firewall ports that should be opened</span></span>
- <span data-ttu-id="b094f-606">アカウントがコンピューターに必要とするアクセス許可</span><span class="sxs-lookup"><span data-stu-id="b094f-606">Which permissions an account requires for a machine</span></span>

<span data-ttu-id="b094f-607">データベースごとに、infrastructure\\D365FO-OP\\DatabaseTopologyDefinition.xml コンフィギュレーション ファイルでは、次の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="b094f-607">For each database, the infrastructure\\D365FO-OP\\DatabaseTopologyDefinition.xml configuration file describes the following details:</span></span>

- <span data-ttu-id="b094f-608">データベース設定</span><span class="sxs-lookup"><span data-stu-id="b094f-608">The database settings</span></span>
- <span data-ttu-id="b094f-609">ユーザーとロールの間のマッピング</span><span class="sxs-lookup"><span data-stu-id="b094f-609">The mappings between users and roles</span></span>

#### <a name="create-gmsa-and-domain-user-accounts"></a><span data-ttu-id="b094f-610">gMSA およびドメイン ユーザー アカウントを作成する</span><span class="sxs-lookup"><span data-stu-id="b094f-610">Create gMSA and domain user accounts</span></span>

1. <span data-ttu-id="b094f-611">**インフラストラクチャ** フォルダーに展開したインフラストラクチャ スクリプトがあるコンピューターに移動します。</span><span class="sxs-lookup"><span data-stu-id="b094f-611">Go to the machine that has the unzipped infrastructure scripts in the **infrastructure** folder.</span></span>
1. <span data-ttu-id="b094f-612">**インフラストラクチャ** フォルダーをドメイン コントローラー マシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="b094f-612">Copy the **infrastructure** folder to the domain controller machine.</span></span>
1. <span data-ttu-id="b094f-613">管理者特権モードで Windows PowerShell を開き、ディレクトリを **infrastructure** フォルダーに変更して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-613">Open Windows PowerShell in elevated mode, change the directory to the **infrastructure** folder, and run the following commands.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b094f-614">これらのコマンドでは、AxServiceUser ドメイン ユーザーを作成しません。</span><span class="sxs-lookup"><span data-stu-id="b094f-614">These commands don't create an AxServiceUser domain user for you.</span></span> <span data-ttu-id="b094f-615">ユーザーが作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-615">You must create it yourself.</span></span>

    ```powershell
    Import-Module .\D365FO-OP\D365FO-OP.psd1
    New-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

1. <span data-ttu-id="b094f-616">アカウントまたはコンピューターを変更する必要がある場合は、元の **インフラストラクチャ** フォルダーの **ConfigTemplate.xml** ファイルを更新し、このコンピューターにコピーしてから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-616">If you must make changes to accounts or machines, update the **ConfigTemplate.xml** file in the original **infrastructure** folder, copy it to this machine, and then run the following command.</span></span>

    ```powershell
    Update-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="step-8-configure-certificates"></a><a name="configurecert"></a><span data-ttu-id="b094f-617">手順 8、</span><span class="sxs-lookup"><span data-stu-id="b094f-617">Step 8.</span></span> <span data-ttu-id="b094f-618">証明書の構成</span><span class="sxs-lookup"><span data-stu-id="b094f-618">Configure certificates</span></span>

1. <span data-ttu-id="b094f-619">最初に **インフラストラクチャ** フォルダーを展開したコンピューターに移動します。</span><span class="sxs-lookup"><span data-stu-id="b094f-619">Go to the machine that you originally unzipped the **infrastructure** folder to.</span></span>
2. <span data-ttu-id="b094f-620">証明書を生成します。</span><span class="sxs-lookup"><span data-stu-id="b094f-620">Generate certificates:</span></span>

    1. <span data-ttu-id="b094f-621">証明書を生成する必要がある場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-621">If you must generate certificates, run the following commands.</span></span> <span data-ttu-id="b094f-622">これらのコマンドは AD CS で証明書テンプレートを作成し、テンプレートから証明書を生成して、コンピューターの **CurrentUser\\My** 証明書ストアに格納してから、XML ファイルのサムプリントを更新します。</span><span class="sxs-lookup"><span data-stu-id="b094f-622">These commands create the certificate templates in AD CS, generate the certificates from the templates, put the certificates in the **CurrentUser\\My** certificate store on the machine, and update the thumbprints in the XML file.</span></span>

        ```powershell
        # If you must create self-signed certs, set the generateSelfSignedCert attribute to true.
        #.\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

        .\New-ADCSCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -CreateTemplates
        .\New-ADCSCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        ```

        > [!NOTE]
        > <span data-ttu-id="b094f-623">これらのコマンドは、ドメイン コントローラー コンピューター、または Windows Server を実行していてリモート サーバー管理ツール (KMT) がインストールされているコンピューターで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-623">You must run these commands on a domain controller machine, or on a machine that is running Windows Server and that has Remote Server Administration Tools (RSAT) installed.</span></span>

    1. <span data-ttu-id="b094f-624">証明書を再利用する必要があるため、証明書を生成する必要がない場合は、**generateADCSCert** タグを **false** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b094f-624">If you must reuse any certificates and therefore don't have to generate certificates for them, set the **generateADCSCert** tag to **false**.</span></span>

3. <span data-ttu-id="b094f-625">以前に生成されている SSL 証明書を使用している場合は、証明書生成をスキップし、**ConfigTemplate.xml** ファイルのサムプリントを更新します。</span><span class="sxs-lookup"><span data-stu-id="b094f-625">If you're using SSL certificates that were previously generated, skip certificate generation, update the thumbprints in the **ConfigTemplate.xml** file.</span></span> <span data-ttu-id="b094f-626">証明書は **CurrentUser\\My** 証明書ストアにインストールする必要があり、その秘密キーはエクスポート可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b094f-626">The certificates must be installed in the **CurrentUser\\My** certificate store, and their private keys must be exportable.</span></span>

    > [!WARNING]
    > <span data-ttu-id="b094f-627">特定するのが難しい先頭の印刷不可能な特殊文字があるため、証明書管理ツール (certlm.msc) を使用してサムプリントをコピーしないでください。</span><span class="sxs-lookup"><span data-stu-id="b094f-627">Because of a leading non-printable special character, the presence of which is difficult to determine, the Certificate Manager tool (certlm.msc) should not be used to copy thumbprints.</span></span> <span data-ttu-id="b094f-628">印刷できない特殊文字がある場合、次のエラー メッセージが表示されます: 「X509 証明書が無効です」</span><span class="sxs-lookup"><span data-stu-id="b094f-628">If the non-printable special character is present, you will receive the following error message: "X509 certificate not valid."</span></span> <span data-ttu-id="b094f-629">サムプリントを取得するには、Windows PowerShell コマンドの結果を参照するか、Windows PowerShell で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-629">To retrieve the thumbprints, see the results from Windows PowerShell commands, or run the following commands in Windows PowerShell.</span></span>
    >
    > ```powershell
    > dir cert:\CurrentUser\My
    > dir cert:\LocalMachine\My
    > dir cert:\LocalMachine\Root
    > ```

4. <span data-ttu-id="b094f-630">各証明書の **ProtectTo** タグで、Active Directory ユーザーまたはグループのセミコロンで区切られた一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="b094f-630">In the **ProtectTo** tag for each certificate, specify a semicolon-separated list of Active Directory users or groups.</span></span> <span data-ttu-id="b094f-631">**ProtectTo** タグで指定されたユーザーとグループのみに、スクリプトを使用してエクスポートされる証明書をインポートするアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-631">Only users and groups that are specified in the **ProtectTo** tag will have the permissions to import the certificates that are exported by using the scripts.</span></span> <span data-ttu-id="b094f-632">エクスポートした証明書を保護するため、スクリプトではパスワードがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b094f-632">The scripts don't support passwords to help protect the exported certificates.</span></span>
5. <span data-ttu-id="b094f-633">証明書を .pfx ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="b094f-633">Export the certificates into .pfx files.</span></span> <span data-ttu-id="b094f-634">エクスポート プロセスの一環として、次のコマンドは、証明書に正しい暗号化プロバイダが設定されているかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="b094f-634">As part of the export process, the following command will check that the correct cryptographic provider is set for your certificates.</span></span> 

    ```powershell
    # Exports .pfx files into a directory VMs\<VMName>. All the certs will be written to the infrastructure\Certs folder.
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="step-9-set-up-vms"></a><a name="setupvms"></a><span data-ttu-id="b094f-635">手順 9、</span><span class="sxs-lookup"><span data-stu-id="b094f-635">Step 9.</span></span> <span data-ttu-id="b094f-636">VMs を設定する</span><span class="sxs-lookup"><span data-stu-id="b094f-636">Set up VMs</span></span>

1. <span data-ttu-id="b094f-637">次のコマンドを実行して、各 VM で実行する必要があるスクリプトをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="b094f-637">Run the following command to export the scripts that must be run on each VM.</span></span>

    ```powershell
    # Exports the script files to be executed on each VM into a directory VMs\<VMName>.
    .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. <span data-ttu-id="b094f-638">次の Microsoft Windows Installers (MSI) を全ての VM でアクセス可能なファイル共有にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b094f-638">Download the following Microsoft Windows Installers (MSIs) into a file share that is accessible by all VMs.</span></span>

    | <span data-ttu-id="b094f-639">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b094f-639">Component</span></span> | <span data-ttu-id="b094f-640">リンクのダウンロード</span><span class="sxs-lookup"><span data-stu-id="b094f-640">Download link</span></span> | <span data-ttu-id="b094f-641">必要なファイル名</span><span class="sxs-lookup"><span data-stu-id="b094f-641">Expected file name</span></span> |
    |-----------|---------------|--------------------|
    | <span data-ttu-id="b094f-642">SNAC – ODBC ドライバー 13</span><span class="sxs-lookup"><span data-stu-id="b094f-642">SNAC – ODBC driver 13</span></span> | <https://docs.microsoft.com/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows#131> | <span data-ttu-id="b094f-643">Msodbcsql .msi</span><span class="sxs-lookup"><span data-stu-id="b094f-643">msodbcsql.msi</span></span> |
    | <span data-ttu-id="b094f-644">SNAC – ODBC ドライバー 17.5.x</span><span class="sxs-lookup"><span data-stu-id="b094f-644">SNAC – ODBC driver 17.5.x</span></span> | <https://docs.microsoft.com/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows?view=sql-server-ver15#1752&preserve-view=true> | <span data-ttu-id="b094f-645">msodbcsql\_17.msi</span><span class="sxs-lookup"><span data-stu-id="b094f-645">msodbcsql\_17.msi</span></span> |
    | <span data-ttu-id="b094f-646">SQL Server Management Studio 17.9.1</span><span class="sxs-lookup"><span data-stu-id="b094f-646">SQL Server Management Studio 17.9.1</span></span> | <https://docs.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms> | <span data-ttu-id="b094f-647">SSMS-Setup-\*.exe</span><span class="sxs-lookup"><span data-stu-id="b094f-647">SSMS-Setup-\*.exe</span></span> |
    | <span data-ttu-id="b094f-648">Microsoft Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="b094f-648">Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</span></span> | <https://support.microsoft.com/help/3179560> | <span data-ttu-id="b094f-649">vcredist\_x64.exe</span><span class="sxs-lookup"><span data-stu-id="b094f-649">vcredist\_x64.exe</span></span> |
    | <span data-ttu-id="b094f-650">Microsoft Visual Studio 2017 用 Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="b094f-650">Visual C++ Redistributable Packages for Microsoft Visual Studio 2017</span></span> | <span data-ttu-id="b094f-651"><https://lcs.dynamics.com/V2/SharedAssetLibrary>に移動して、資産タイプとして **モデル** を選択して、**VC++ 17 再配布可能ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-651">Go to <https://lcs.dynamics.com/V2/SharedAssetLibrary>, select **Model** as the asset type, and then select **VC++ 17 Redistributables**.</span></span> | <span data-ttu-id="b094f-652">vc\_redist.x64\_14\_16\_27024.exe</span><span class="sxs-lookup"><span data-stu-id="b094f-652">vc\_redist.x64\_14\_16\_27024.exe</span></span> |
    | <span data-ttu-id="b094f-653">Access データベース エンジン 2010 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="b094f-653">Access Database Engine 2010 Redistributable</span></span> | <https://www.microsoft.com/download/details.aspx?id=13255> | <span data-ttu-id="b094f-654">AccessDatabaseEngine\_x64.exe</span><span class="sxs-lookup"><span data-stu-id="b094f-654">AccessDatabaseEngine\_x64.exe</span></span> |
    | <span data-ttu-id="b094f-655">.NET Framework version 4.8 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-655">The .NET Framework version 4.8 (CLR 4.0)</span></span> | <https://dotnet.microsoft.com/download/thank-you/net48-offline> | <span data-ttu-id="b094f-656">ndp48-x86-x64-allos-enu.exe</span><span class="sxs-lookup"><span data-stu-id="b094f-656">ndp48-x86-x64-allos-enu.exe</span></span> |
    | <span data-ttu-id="b094f-657">.NET Framework version 4.7.2 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="b094f-657">The .NET Framework version 4.7.2 (CLR 4.0)</span></span> | <https://dotnet.microsoft.com/download/thank-you/net472-offline> | <span data-ttu-id="b094f-658">ndp472-x86-x64-allos-enu.exe</span><span class="sxs-lookup"><span data-stu-id="b094f-658">ndp472-x86-x64-allos-enu.exe</span></span> |

> [!IMPORTANT]
> - <span data-ttu-id="b094f-659">Management Studio の設定が、対象となるコンピューターのオペレーティング システムと同じ言語であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-659">Make sure that the Management Studio setup is in the same language as the operating system of the target machine.</span></span>
> - <span data-ttu-id="b094f-660">前の表の "必要なファイル名" 列に指定されている名前がインストーラ ファイルに設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-660">Make sure that the installer files have the names that are specified in the "Expected file name" column of the preceding table.</span></span> <span data-ttu-id="b094f-661">予期した名前がないファイルの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="b094f-661">Rename any files that don't have the expected name.</span></span> <span data-ttu-id="b094f-662">そうしないと、Configure-PreReq.ps1 スクリプトの実行時にエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b094f-662">Otherwise, you will encounter errors when you run the Configure-PreReqs.ps1 script.</span></span>
> - <span data-ttu-id="b094f-663">VC++ 17 再配布可能ファイル をダウンロードする場合、実行可能ファイルが zip ファイル内に含まれます。</span><span class="sxs-lookup"><span data-stu-id="b094f-663">When you download VC++ 17 Redistributables, the executable file is inside the zip file.</span></span>

<span data-ttu-id="b094f-664">次に、各 VM についてこれらのステップに従うか、または単一のコンピューターからリモート処理を使用します。</span><span class="sxs-lookup"><span data-stu-id="b094f-664">Next, follow these steps for each VM, or use remoting from a single machine.</span></span>

> [!NOTE]
> - <span data-ttu-id="b094f-665">次の手順では、複数の VM での実行が必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-665">The following procedure requires execution on multiple VMs.</span></span> <span data-ttu-id="b094f-666">ただし、プロセスを簡略化するために、提供されるリモート処理スクリプトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-666">However, to simplify the process, you can use the remoting scripts that are provided.</span></span> <span data-ttu-id="b094f-667">これらのスクリプトを使用すると、**.\\Export-Scripts.ps1** コマンドの実行に使用されるのと同じコンピューターなど、単一のコンピューターから必要なスクリプトを実行できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-667">These scripts let you run the required scripts from a single machine, such as the same machine that is used to run the **.\\Export-Scripts.ps1** command.</span></span> <span data-ttu-id="b094f-668">リモート処理スクリプトが利用可能な場合、Windows PowerShell セクションの **\# If Remoting** コメントの後に宣言されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-668">When the remoting scripts are available, they are declared after a **\# If Remoting** comment in the Windows PowerShell sections.</span></span> <span data-ttu-id="b094f-669">リモート処理スクリプトを使用する場合、セクション内の残りのスクリプトを実行する必要がない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-669">If you use the remoting scripts, you might not have to run the remaining scripts in a section.</span></span> <span data-ttu-id="b094f-670">この場合は、セクション テキストを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-670">In these cases, see the section text.</span></span>
> - <span data-ttu-id="b094f-671">リモート処理では [WinRM](/windows/win32/winrm/portal) を使用します。</span><span class="sxs-lookup"><span data-stu-id="b094f-671">Remoting uses [WinRM](/windows/win32/winrm/portal).</span></span> <span data-ttu-id="b094f-672">場合によっては、[CredSSP](/windows/win32/secauthn/credential-security-support-provider) を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-672">In some cases, it requires that [CredSSP](/windows/win32/secauthn/credential-security-support-provider) be enabled.</span></span> <span data-ttu-id="b094f-673">リモート処理モジュールでは、実行ごとに CredSSP を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="b094f-673">The remoting module enables and disables CredSSP on an execution-by-execution basis.</span></span> <span data-ttu-id="b094f-674">使用しない場合は、CredSSP を無効にすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b094f-674">We recommend that you disable CredSSP enabled when it isn't used.</span></span> <span data-ttu-id="b094f-675">そうしないと、資格情報の盗難リスクが伴います。</span><span class="sxs-lookup"><span data-stu-id="b094f-675">Otherwise, there is a risk of credential theft.</span></span> <span data-ttu-id="b094f-676">設定が完了したら、このトピック後半の[手順 20、リモート処理が使用されたら、CredSSP を終了処理する](#teardowncredssp)セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-676">When you've completed the setup, see the [Step 20. Tear down CredSSP, if remoting was used](#teardowncredssp) section later in this topic.</span></span>

1. <span data-ttu-id="b094f-677">各 **infrastructure\\VMs\\\<VMName\>** フォルダーの内容を、対応する VM にコピーします。</span><span class="sxs-lookup"><span data-stu-id="b094f-677">Copy the contents of each **infrastructure\\VMs\\\<VMName\>** folder to the corresponding VM.</span></span> <span data-ttu-id="b094f-678">(リモート処理スクリプトを使用している場合は、コンテンツが自動的に対象の VM にコピーされます。) 続いて、次のコマンドを管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-678">(If the remoting scripts are used, they will automatically copy the contents to the target VMs.) Then run the following command as an administrator.</span></span>

    ```powershell
    # Install prereq software on the VMs.

    # If remoting, execute
    # .\Configure-PreReqs-AllVMs.ps1 -MSIFilePath <share folder path of the MSIs> -ConfigurationFilePath .\ConfigTemplate.xml

    .\Configure-PreReqs.ps1 -MSIFilePath <path of the MSIs>
    ```

    > [!IMPORTANT]
    > - <span data-ttu-id="b094f-679">再起動するように求められるたびにコンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="b094f-679">Each time that you're prompted, restart the machine.</span></span> <span data-ttu-id="b094f-680">すべての前提条件がインストールされるまでは、各再起動後に **.\\Configure-PreReqs.ps1** コマンドを必ず再実行してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-680">Make sure that you rerun the **.\\Configure-PreReqs.ps1** command after each restart, until all the prerequisites are installed.</span></span> <span data-ttu-id="b094f-681">リモート処理の場合、すべてのコンピューターがオンラインに戻ったときに AllVM スクリプトを再実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-681">In the case of remoting, rerun the AllVMs script when all the machines are back online.</span></span>
    > - <span data-ttu-id="b094f-682">リモート処理スクリプトを使用する場合は、現在のユーザーが MSI が配置されているファイル共有フォルダーにアクセスできることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-682">If you use the remoting scripts, make sure that the current user has access to the file share folder where the MSIs are located.</span></span> <span data-ttu-id="b094f-683">さらに、ユーザーが **AOSNodeType**、**MRType**、**ReportServerType** タイプのコンピューターにアクセスしていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-683">Also make sure that no user is accessing machines of the **AOSNodeType**, **MRType**, and **ReportServerType** types.</span></span> <span data-ttu-id="b094f-684">そうしないと、ユーザーがログインしている理由によって、リモート処理スクリプトがコンピューターの再起動に失敗します。</span><span class="sxs-lookup"><span data-stu-id="b094f-684">Otherwise, the remoting scripts will fail to restart the machines, because users are signed in to them.</span></span>

2. <span data-ttu-id="b094f-685">次のコマンドを実行して VM 設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="b094f-685">Run the following command to complete the VM setup.</span></span>

    ```powershell
    # If remoting, execute
    # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    .\Complete-PreReqs.ps1
    ```

3. <span data-ttu-id="b094f-686">次のコマンドを実行して VM 設定を検証します。</span><span class="sxs-lookup"><span data-stu-id="b094f-686">Run the following command to validate the VM setup.</span></span>

    ```powershell
    # If Remoting, execute
    # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    .\Test-D365FOConfiguration.ps1 
    ```

> [!IMPORTANT]
> <span data-ttu-id="b094f-687">リモート処理を使用していた場合は、設定の完了後にクリーンアップ手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-687">If you used remoting, be sure to run the cleanup steps after the setup is completed.</span></span> <span data-ttu-id="b094f-688">手順については、[手順 20、リモート処理が使用されたら、CredSSP を終了処理する](#teardowncredssp)セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-688">For instructions, see the [Step 20. Tear down CredSSP, if remoting was used](#teardowncredssp) section.</span></span>

### <a name="step-10-set-up-a-standalone-service-fabric-cluster"></a><a name="setupsfcluster"></a><span data-ttu-id="b094f-689">手順 10、</span><span class="sxs-lookup"><span data-stu-id="b094f-689">Step 10.</span></span> <span data-ttu-id="b094f-690">スタンドアロン Service Fabric クラスターの設定</span><span class="sxs-lookup"><span data-stu-id="b094f-690">Set up a standalone Service Fabric cluster</span></span>

1. <span data-ttu-id="b094f-691">[Service Fabric スタンドアロン インストール パッケージ](https://go.microsoft.com/fwlink/?LinkId=730690) を Service Fabric ノードのいずれかにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b094f-691">Download the [Service Fabric standalone installation package](https://go.microsoft.com/fwlink/?LinkId=730690) to one of your Service Fabric nodes.</span></span>
2. <span data-ttu-id="b094f-692">zip ファイルをダウンロードした後、ファイルを選択したまま (または右クリック) にしてから、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-692">After the zip file is downloaded, select and hold (or right-click) it, and then select **Properties**.</span></span> <span data-ttu-id="b094f-693">**プロパティ** ダイアログ ボックスで、**ブロック解除** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-693">In the **Properties** dialog box, select the **Unblock** check box.</span></span>
3. <span data-ttu-id="b094f-694">ZIP ファイルを Service Fabric クラスター内のいずれかのノードにコピーし、解凍します。</span><span class="sxs-lookup"><span data-stu-id="b094f-694">Copy the zip file to one of the nodes in the Service Fabric cluster, and unzip it.</span></span> <span data-ttu-id="b094f-695">**インフラストラクチャ** フォルダーが、このフォルダーにアクセスすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-695">Make sure that the **infrastructure** folder has access to this folder.</span></span>
3. <span data-ttu-id="b094f-696">**インフラストラクチャ** フォルダーに移動し、次のコマンドを実行して Service Fabric **ClusterConfig.json** ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="b094f-696">Go to the **infrastructure** folder, and run the following command to generate the Service Fabric **ClusterConfig.json** file.</span></span>

    ```powershell
    .\New-SFClusterConfig.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -TemplateConfig <ServiceFabricStandaloneInstallerPath>\ClusterConfig.X509.MultiMachine.json
    ```

4. <span data-ttu-id="b094f-697">環境に基づいて、クラスター コンフィギュレーションへの追加の変更が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-697">You might have to make additional modifications to your cluster configuration, based on your environment.</span></span> <span data-ttu-id="b094f-698">詳細については、[手順 1B: 複数のマシンでクラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)、[X.509 証明書を使用して Windows スタンドアロン クラスターを保護する](/azure/service-fabric/service-fabric-windows-cluster-x509-security)、および [Windows Server で実行されているスタンドアロン クラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-698">For more information, see [Step 1B: Create a multi-machine cluster](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Secure a standalone cluster on Windows using X.509 certificates](/azure/service-fabric/service-fabric-windows-cluster-x509-security), and [Create a standalone cluster running on Windows Server](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).</span></span>
5. <span data-ttu-id="b094f-699">生成された **ClusterConfig.json** ファイルを **\<ServiceFabricStandaloneInstallerPath\>** にコピーします。</span><span class="sxs-lookup"><span data-stu-id="b094f-699">Copy the **ClusterConfig.json** file that is generated to **\<ServiceFabricStandaloneInstallerPath\>**.</span></span>
6. <span data-ttu-id="b094f-700">管理者特権モードで Windows PowerShell を開き、**\<ServiceFabricStandaloneInstallerPath\>** に移動して、次のコマンドを実行して **ClusterConfig.go** ファイルをテストします。</span><span class="sxs-lookup"><span data-stu-id="b094f-700">Open Windows PowerShell in elevated mode, go to **\<ServiceFabricStandaloneInstallerPath\>**, and run the following command to test the **ClusterConfig.json** file.</span></span>

    ```powershell
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

7. <span data-ttu-id="b094f-701">テストが成功した場合は、次のコマンドを実行してクラスターを展開します。</span><span class="sxs-lookup"><span data-stu-id="b094f-701">If the test is successful, run the following command to deploy the cluster.</span></span>

    ```powershell
    # If using offline (internet-disconnected) install
    # .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json -FabricRuntimePackagePath <Path to MicrosoftAzureServiceFabric.cab download>

    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

8. <span data-ttu-id="b094f-702">クラスターが作成された後、任意のクライアント コンピューターで Service Fabric Explorer を開き、インストールを検証します。</span><span class="sxs-lookup"><span data-stu-id="b094f-702">After the cluster is created, open Service Fabric Explorer on any client machine, and validate the installation:</span></span>

    1. <span data-ttu-id="b094f-703">まだインストールされていない場合、**CurrentUser\\My** 証明書ストアで Service Fabric クライアント証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="b094f-703">Install the Service Fabric client certificate in the **CurrentUser\\My** certificate store if it isn't already installed.</span></span>
    2. <span data-ttu-id="b094f-704">Internet Explorer で、**ツール** (ギヤ記号) を選択してから、**互換性表示の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-704">In Internet Explorer, select **Tools** (the gear symbol), and then select **Compatibility View settings**.</span></span> <span data-ttu-id="b094f-705">**互換性表示でイントラネット サイトを表示する** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="b094f-705">Clear the **Display intranet sites in Compatibility View** check box.</span></span>
    3. <span data-ttu-id="b094f-706">`https://sf.d365ffo.onprem.contoso.com:19080` に移動します。**sf.d365ffo.onprem.contoso.com** は、ゾーンで指定されている Service Fabric Cluster のホスト名です。</span><span class="sxs-lookup"><span data-stu-id="b094f-706">Go to `https://sf.d365ffo.onprem.contoso.com:19080`, where **sf.d365ffo.onprem.contoso.com** is the host name of the Service Fabric cluster that is specified in the zone.</span></span> <span data-ttu-id="b094f-707">DNS 名前解決が設定されていない場合は、マシンの IP アドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="b094f-707">If DNS name resolution isn't configured, use the IP address of the machine.</span></span>
    4. <span data-ttu-id="b094f-708">クライアントの証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-708">Select the client certificate.</span></span> <span data-ttu-id="b094f-709">**Service Fabric Explorer** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-709">The **Service Fabric Explorer** page appears.</span></span>
    5. <span data-ttu-id="b094f-710">すべてのノードが緑で表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-710">Verify that all nodes appear as green.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="b094f-711">クライアント コンピューターがサーバー コンピューター (たとえば、Windows Server 2016 を実行しているコンピューター) である場合は、**Service Fabric Explorer** ページにアクセスするときに Internet Explorer のセキュリティ強化の構成をオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-711">If your client machine is a server machine (for example, a machine that is running Windows Server 2016), you must turn off the Internet Explorer Enhanced Security Configuration when you access the **Service Fabric Explorer** page.</span></span>
    > - <span data-ttu-id="b094f-712">任意のウィルス対策ソフトウェアをインストールする場合は、除外を設定してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-712">If any antivirus software is installed, make sure that you set exclusion.</span></span> <span data-ttu-id="b094f-713">[Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) ドキュメントのガイダンスに従ってください。</span><span class="sxs-lookup"><span data-stu-id="b094f-713">Follow the guidance in the [Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) documentation.</span></span>

### <a name="step-11-configure-lcs-connectivity-for-the-tenant"></a><a name="configurelcs"></a><span data-ttu-id="b094f-714">手順 11、</span><span class="sxs-lookup"><span data-stu-id="b094f-714">Step 11.</span></span> <span data-ttu-id="b094f-715">テナント用 LCS 接続の構成</span><span class="sxs-lookup"><span data-stu-id="b094f-715">Configure LCS connectivity for the tenant</span></span>

<span data-ttu-id="b094f-716">オンプレミスのローカル エージェントは、LCS を通じて Finance + Operations の展開とサービスを調整するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-716">An on-premises local agent is used to orchestrate deployment and servicing of Finance + Operations through LCS.</span></span> <span data-ttu-id="b094f-717">LCS から Finance + Operations テナントへの接続を確立するには、Azure AD テナント (たとえば、contoso.onmicrosoft.com) の代わりに動作するローカル エージェントを可能にする証明書をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-717">To establish connectivity from LCS to the Finance + Operations tenant, you must configure a certificate that enables the local agent to act on behalf on your Azure AD tenant (for example, contoso.onmicrosoft.com).</span></span>

<span data-ttu-id="b094f-718">CA から取得したオンプレミス エージェントの証明書またはスクリプトを使用して生成した自己署名証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="b094f-718">Use the on-premises agent certificate that you acquired from a CA or the self-signed certificate that you generated by using scripts.</span></span> <span data-ttu-id="b094f-719">オンプレミス エージェント証明書は、テナントごとに複数のサンドボックス環境および実稼動環境で再利用できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-719">The on-premises agent certificate can be reused across multiple sandbox and production environments per tenant.</span></span>

<span data-ttu-id="b094f-720">グローバル管理者ディレクトリの役割を持つユーザー アカウントだけが、LCS を承認するための証明書を追加できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-720">Only user accounts that have the Global Administrator directory role can add certificates to authorize LCS.</span></span> <span data-ttu-id="b094f-721">既定では、組織の Microsoft 365 にサインアップする担当者がディレクトリのグローバル管理者です。</span><span class="sxs-lookup"><span data-stu-id="b094f-721">By default, the person who signs up for Microsoft 365 for your organization is the global administrator for the directory.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="b094f-722">テナントごとに証明書を正確に **1** 回構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-722">You must configure the certificate exactly **one** time per tenant.</span></span> <span data-ttu-id="b094f-723">同じ環境のすべてのオンプレミス環境では、同じ証明書を使用して LCS に接続できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-723">All on-premises environments under the same tenant must use the same certificate to connect with LCS.</span></span>
> - <span data-ttu-id="b094f-724">サーバー コンピューター ( Windows Server 2016 を実行しているコンピューターなど) で以下のスクリプトを実行する場合は、Internet Explorer セキュリティ強化の構成を一時的にオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-724">If you run the script below on a server machine (for example, a machine that is running Windows Server 2016), you must temporarily turn off the Internet Explorer Enhanced Security Configuration.</span></span> <span data-ttu-id="b094f-725">そうしないと、Azure のサインイン ページのコンテンツがブロックされます。</span><span class="sxs-lookup"><span data-stu-id="b094f-725">Otherwise, the content on the Azure sign-in page will be blocked.</span></span>

1. <span data-ttu-id="b094f-726">顧客の [Azure ポータル](https://portal.azure.com)にサインインして、グローバル管理者ディレクトリの役割があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-726">Sign in to the customer's [Azure portal](https://portal.azure.com) to verify that you have the Global Administrator directory role.</span></span>
2. <span data-ttu-id="b094f-727">次のコマンドを **インフラストラクチャ** フォルダーから実行して、証明書が既に登録されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-727">From the **infrastructure** folder, run the following commands to determine whether the certificate is already registered.</span></span>

    ```powershell
    # If you have issues downloading the Azure PowerShell Az module, run the following:
    # [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12

    Install-Module Az
    Import-Module Az
    .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint' -Test
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="b094f-728">既に AzureRM をインストールしている場合は、Windows PowerShell 5.1 の既存の AzureRM インストールとの互換性がない可能性があるため、削除してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-728">If you previously installed AzureRM, you should remove it, because it might not be compatible with any existing AzureRM installations in Windows PowerShell 5.1.</span></span> <span data-ttu-id="b094f-729">詳細については、[Azure PowerShell を AzureRM から Az に移行する](/powershell/azure/migrate-from-azurerm-to-az)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-729">For more information, see [Migrate Azure PowerShell from AzureRM to Az](/powershell/azure/migrate-from-azurerm-to-az).</span></span>

3. <span data-ttu-id="b094f-730">証明書が登録されていないことをスクリプトが示している場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-730">If the script indicates that the certificate isn't registered, run the following command.</span></span>

    ```powershell
    .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint'
    ```

> [!NOTE]
> <span data-ttu-id="b094f-731">ログイン アカウントに関連付けられた複数のテナントがある場合、次のコマンドを実行してテナント ID をパラメーターとして渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="b094f-731">If you have multiple tenants that are associated with the login account, you can run the following command to pass the tenant ID as a parameter.</span></span> <span data-ttu-id="b094f-732">これにより、コンテキストが正しいテナントに設定されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-732">In this way, you can ensure that the context is set to the correct tenant.</span></span>
>
> ```powershell
> .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint' -TenantId 'xxxx-xxxx-xxxx-xxxx'
> ```

### <a name="step-12-set-up-file-storage"></a><a name="setupfile"></a><span data-ttu-id="b094f-733">手順 12、</span><span class="sxs-lookup"><span data-stu-id="b094f-733">Step 12.</span></span> <span data-ttu-id="b094f-734">ファイル ストレージの設定</span><span class="sxs-lookup"><span data-stu-id="b094f-734">Set up file storage</span></span>

<span data-ttu-id="b094f-735">以下の SMB 3.0 ファイル共有を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-735">You must set up the following SMB 3.0 file shares:</span></span>

- <span data-ttu-id="b094f-736">AOS にアップロードされるユーザー ドキュメントを格納するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\aos-storage)。</span><span class="sxs-lookup"><span data-stu-id="b094f-736">A file share that stores user documents that are uploaded to AOS (for example, \\\\DAX7SQLAOFILE1\\aos-storage).</span></span>
- <span data-ttu-id="b094f-737">デプロイメントを調整するための最新のビルド ファイルと構成ファイルを保存するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\agent)。</span><span class="sxs-lookup"><span data-stu-id="b094f-737">A file share that stores the latest build and configuration files to orchestrate the deployment (for example, \\\\DAX7SQLAOFILE1\\agent).</span></span>

    > [!WARNING]
    > <span data-ttu-id="b094f-738">共有に入れるファイルの最大パス長を超えないように、このファイル共有パスはできるだけ短くしておいてください。</span><span class="sxs-lookup"><span data-stu-id="b094f-738">Keep this file share path as short as possible, to avoid exceeding the maximum path length on the files that will be put in the share.</span></span>

<span data-ttu-id="b094f-739">SMB 3.0 を有効にする方法については、[SMB セキュリティの強化](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn551363(v=ws.11)#BKMK_disablesmb1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-739">For information about how to enable SMB 3.0, see [SMB Security Enhancements](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn551363(v=ws.11)#BKMK_disablesmb1).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="b094f-740">セキュリティで保護されたダイアレクト ネゴシエーションでは、SMB 2.0 または 3.0 から SMB 1.0 へのダウングレードを検出または防止できません。</span><span class="sxs-lookup"><span data-stu-id="b094f-740">Secure dialect negotiation can't detect or prevent downgrades from SMB 2.0 or 3.0 to SMB 1.0.</span></span> <span data-ttu-id="b094f-741">したがって、SMB 1.0 サーバーを無効にすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b094f-741">Therefore, we strongly recommend that you disable the SMB 1.0 server.</span></span> <span data-ttu-id="b094f-742">これにより、SMB 暗号化のすべての機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-742">In this way, you can take advantage of the full capabilities of SMB encryption.</span></span>
> - <span data-ttu-id="b094f-743">環境内の残りの部分でデータが保護されていることを保証するために、BitLocker ドライブ暗号化をすべてのコンピューターで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-743">To help ensure that your data is protected while it's at rest in your environment, you must enable BitLocker Drive Encryption on every machine.</span></span> <span data-ttu-id="b094f-744">BitLocker を有効にする方法については、[BitLocker: Windows Server 2012 以降で配置する方法](/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-744">For information about how to enable BitLocker, see [BitLocker: How to deploy on Windows Server 2012 and later](/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server).</span></span>

1. <span data-ttu-id="b094f-745">ファイル共有マシンで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-745">On the file share machine, run the following command.</span></span>

    ```powershell
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```

2. <span data-ttu-id="b094f-746">**\\\\DAX7SQLAOFILE1\\aos-storage** ファイル共有を設定します。</span><span class="sxs-lookup"><span data-stu-id="b094f-746">Set up the **\\\\DAX7SQLAOFILE1\\aos-storage** file share:</span></span>

    1. <span data-ttu-id="b094f-747">サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-747">In Server Manager, select **File and Storage Services** \> **Shares**.</span></span>
    2. <span data-ttu-id="b094f-748">**タスク** \> **新しい共有** を選択し、共有を作成します。</span><span class="sxs-lookup"><span data-stu-id="b094f-748">Select **Tasks** \> **New Share** to create a share.</span></span> <span data-ttu-id="b094f-749">新しい共有に **aos-storage** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="b094f-749">Name the new share **aos-storage**.</span></span>
    3. <span data-ttu-id="b094f-750">**共有のキャッシュを許可** を選択したままにします。</span><span class="sxs-lookup"><span data-stu-id="b094f-750">Leave **Allow caching of share** selected.</span></span>
    4. <span data-ttu-id="b094f-751">**データ アクセスを暗号化** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b094f-751">Select the **Encrypt data access** check box.</span></span>
    5. <span data-ttu-id="b094f-752">**OrchestratorType** を除いて、Service Fabric cluster 内のすべてのマシンに対して **変更** 許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="b094f-752">Grant **Modify** permissions for every machine in the Service Fabric cluster except **OrchestratorType**.</span></span>
    6. <span data-ttu-id="b094f-753">AOS ドメイン ユーザー (**contoso\\AXServiceUser**) と gMSA ユーザー (**contoso\\svc-AXSF$**) に対して、**変更** 許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="b094f-753">Grant **Modify** permissions for the user AOS domain user (**contoso\\AXServiceUser**) and the gMSA user (**contoso\\svc-AXSF$**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="b094f-754">コンピュータを追加するには、**オブジェクト タイプ** で **コンピューター** を有効にする場合があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-754">To add machines, you might have to enable **Computers** under **Object Types**.</span></span> <span data-ttu-id="b094f-755">サービス アカウントを追加するには、**オブジェクト タイプ** で **サービス アカウント** を有効にする場合があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-755">To add service accounts, you might have to enable **Service Accounts** under **Object Types**.</span></span>

3. <span data-ttu-id="b094f-756">**\\\\DAX7SQLAOFILE1\\agent** ファイル共有を設定します。</span><span class="sxs-lookup"><span data-stu-id="b094f-756">Set up the **\\\\DAX7SQLAOFILE1\\agent** file share:</span></span>

    1. <span data-ttu-id="b094f-757">サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-757">In Server Manager, select **File and Storage Services** \> **Shares**.</span></span>
    2. <span data-ttu-id="b094f-758">**タスク** \> **新しい共有** を選択し、共有を作成します。</span><span class="sxs-lookup"><span data-stu-id="b094f-758">Select **Tasks** \> **New Share** to create a share.</span></span> <span data-ttu-id="b094f-759">新しい共有に **エージェント** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="b094f-759">Name the new share **agent**.</span></span>
    3. <span data-ttu-id="b094f-760">ローカル展開エージェント (**contoso\\svc-LocalAgent$**) の gMSA ユーザーに対して **フル コントロール** の許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="b094f-760">Grant **Full-Control** permissions to the gMSA user for the local deployment agent (**contoso\\svc-LocalAgent$**).</span></span>

    ```powershell
    # Specify user names
    $AOSDomainUser = 'Contoso\AXServiceUser';
    $LocalDeploymentAgent = 'contoso\svc-LocalAgent$';

    # Specify the path
    $AosStorageFolderPath = 'D:\aos-storage';
    $AgentFolderPath = 'D:\agent';

    # Create new directory
    $AosStorageFolder = New-Item -type directory -path $AosStorageFolderPath;
    $AgentFolder = New-Item -type directory -path $AgentFolderPath;

    # Create new SMB share
    New-SmbShare –Name aos-storage -Path $AosStorageFolderPath -EncryptData $True
    New-SmbShare –Name agent -Path $AgentFolderPath

    # Set ACL for AOS storage folder
    $Acl = Get-Acl $AosStorageFolder.FullName;
    $Ar = New-Object system.security.accesscontrol.filesystemaccessrule($AOSDomainUser,'Modify','Allow');
    $Acl.SetAccessRule($Ar);
    Set-Acl $AosStorageFolder.FullName $Acl;

    # Set ACL for AgentFolder
    $Acl = Get-Acl $AgentFolder.FullName;
    $Ar = New-Object system.security.accesscontrol.filesystemaccessrule($LocalDeploymentAgent,'FullControl','Allow');
    $Acl.SetAccessRule($Ar);
    Set-Acl $AgentFolder.FullName $Acl;
    ```

### <a name="step-13-set-up-sql-server"></a><a name="setupsql"></a><span data-ttu-id="b094f-761">手順 13、</span><span class="sxs-lookup"><span data-stu-id="b094f-761">Step 13.</span></span> <span data-ttu-id="b094f-762">SQL Server の設定</span><span class="sxs-lookup"><span data-stu-id="b094f-762">Set up SQL Server</span></span>

1. <span data-ttu-id="b094f-763">SQL Server のインスタンスが 1 つでも十分なサンドボックス環境に展開する場合を除いて、高可用性を備えた SQL Server 2016 SP2 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="b094f-763">Install SQL Server 2016 SP2 with high availability, unless you're deploying in a sandbox environment, where one instance of SQL Server is sufficient.</span></span> <span data-ttu-id="b094f-764">(ただし、高可用性シナリオをテストするため、サンドボックス環境に高可用性を備えた SQL Server をインストールすることもできます。)</span><span class="sxs-lookup"><span data-stu-id="b094f-764">(Nevertheless, you might want to install SQL Server with high availability in sandbox environments to test high-availability scenarios.)</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b094f-765">[SQL Server および Windows 認証モード](/sql/database-engine/configure-windows/change-server-authentication-mode) を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-765">You must enable the [SQL Server and Windows Authentication mode](/sql/database-engine/configure-windows/change-server-authentication-mode).</span></span>

    <span data-ttu-id="b094f-766">高可用性を備えた SQL Server を、SAN (ストレージ エリア ネットワーク) を含む SQL クラスターまたは Always-On 構成のいずれかとしてインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="b094f-766">You can install SQL Server with high availability either as SQL clusters that include a Storage Area Network (SAN) or in an Always-On configuration.</span></span> <span data-ttu-id="b094f-767">データベース エンジン、SSRS、フルテキスト検索、および SQL Server 管理ツールがインストール済みであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-767">Verify that the Database Engine, SSRS, Full-Text Search, and SQL Server Management Tools are already installed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b094f-768">Always-On が [初期データ同期ページの選択 (可用性グループ ウィザードで常に使用する)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) で説明されているとおりに設定され、[セカンダリ データベースを手動で準備する](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs) の指示に従っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-768">Make sure that Always-On is set up as described in [Select Initial Data Synchronization Page (Always On Availability Group Wizards)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards), and follow the instructions in [To Prepare Secondary Databases Manually](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs).</span></span>

2. <span data-ttu-id="b094f-769">ドメイン ユーザーまたは gMSA のいずれかとして SQL サービスを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-769">Run the SQL service as either a domain user or a gMSA.</span></span>
3. <span data-ttu-id="b094f-770">Finance + Operations 向けに SQL Server を構成するために CA から SSL 証明書を取得します。</span><span class="sxs-lookup"><span data-stu-id="b094f-770">Get an SSL certificate from a CA to configure SQL Server for Finance + Operations.</span></span> <span data-ttu-id="b094f-771">テストの目的で、AD CS を通じて生成された証明書を作成して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="b094f-771">For testing purposes, you can create and use a certificate that is generated through AD CS.</span></span> <span data-ttu-id="b094f-772">次の例にあるコンピューター名とドメイン名を置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-772">You will have to replace the computer name and domain name in the following examples.</span></span>

    <span data-ttu-id="b094f-773">**Always-On SQL 可用性グループの AD CS 証明書**</span><span class="sxs-lookup"><span data-stu-id="b094f-773">**AD CS certificate for an Always-On SQL availability group**</span></span>

    <span data-ttu-id="b094f-774">Always-On 用の証明書のテストを設定する場合は、次のリモート処理スクリプトを使用します。</span><span class="sxs-lookup"><span data-stu-id="b094f-774">If you're setting up testing certificates for Always-On, use the following remoting script.</span></span> <span data-ttu-id="b094f-775">このスクリプトは、次に示す手動スクリプトと同じように機能します。</span><span class="sxs-lookup"><span data-stu-id="b094f-775">This script works like the manual script that follows.</span></span>

    ```powershell
    #If you need to create self-signed certs
    #.\New-SelfSigned-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser

    .\New-ADCS-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser
    ```

    <span data-ttu-id="b094f-776">**単一の SQL 可用性グループの AD CS 証明書**</span><span class="sxs-lookup"><span data-stu-id="b094f-776">**AD CS certificate for a single SQL availability group**</span></span>

    ```powershell
    #If you need to create self-signed certs
    #.\New-SelfSigned-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1 -ProtectTo CONTOSO\dynuser

    .\New-ADCS-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1 -ProtectTo CONTOSO\dynuser
    ```

    <span data-ttu-id="b094f-777">**SQL Server を使用した Always-On SQL 可用性グループまたは Windows Server フェールオーバー クラスタリングの手動 AD CS 手順**</span><span class="sxs-lookup"><span data-stu-id="b094f-777">**Manual AD CS steps for an Always-On SQL availability group or Windows Server Failover Clustering with SQL Server**</span></span> 

    <span data-ttu-id="b094f-778">SQL クラスターの各ノードに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-778">For each node of the SQL cluster, follow these steps.</span></span> 

    1. <span data-ttu-id="b094f-779">次の Windows PowerShell コマンドを、SQL Server Always-On レプリカごとに実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-779">Run the following Windows PowerShell command on each of the SQL Server Always-On replicas.</span></span>

        ```powershell
        #If you need to create self-signed certs
        #.\New-SelfSigned-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser -GenerateCertOnly

        .\New-ADCS-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser -GenerateCertOnly
        ```

    2. <span data-ttu-id="b094f-780">SQL サービスを実行するために使用されるアカウントに証明書のアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="b094f-780">Grant certificate permissions to the account that is used to run the SQL service:</span></span>

        1. <span data-ttu-id="b094f-781">証明書管理ツール (**certlm.msc**) を開きます。</span><span class="sxs-lookup"><span data-stu-id="b094f-781">Open the Certificate Manager tool (**certlm.msc**).</span></span>
        2. <span data-ttu-id="b094f-782">作成した証明書を選択したまま (または右クリック) してから、**タスク** \> **秘密キーの管理** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b094f-782">Select and hold (or right-click) the certificate that was created, and then select **Tasks** \> **Manage Private Keys**.</span></span>
        3. <span data-ttu-id="b094f-783">SQL Server サービス アカウントを追加し、**読み取り** アクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="b094f-783">Add the SQL Server service account, and grant it **Read** access.</span></span>

    3. <span data-ttu-id="b094f-784">SQL Server 構成マネージャーで **ForceEncryption** と新しい証明書を有効にします。</span><span class="sxs-lookup"><span data-stu-id="b094f-784">Enable **ForceEncryption** and the new certificate in SQL Server Configuration Manager:</span></span>

        1. <span data-ttu-id="b094f-785">SQL Server 構成マネージャーを開き、**SQL Server ネットワーク構成** を展開し、**\[サーバー インスタンス\] 用プロトコル** を選択したまま (または右クリック) にしてから、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-785">Open SQL Server Configuration Manager, expand **SQL Server Network Configuration**, select and hold (or right-click) **Protocols for \[server instance\]**, and then select **Properties**.</span></span>
        2. <span data-ttu-id="b094f-786">**プロトコル** ダイアログ ボックスの、**証明書** タブの、**証明書** フィールドで、目的の証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-786">In the **Properties** dialog box, on the **Certificate** tab, in the **Certificate** field, select the desired certificate.</span></span>
        3. <span data-ttu-id="b094f-787">**フラグ** タブの **ForceEncryption** ボックスで、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-787">On the **Flags** tab, in the **ForceEncryption** box, select **Yes**.</span></span>
        4. <span data-ttu-id="b094f-788">**OK** を選択して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="b094f-788">Select **OK** to save your changes.</span></span>

    4. <span data-ttu-id="b094f-789">各 SQL クラスター ノードから証明書 (.cer ファイル) をエクスポートし、各 Service Fabric ノードの信頼できるルートにインストールします。</span><span class="sxs-lookup"><span data-stu-id="b094f-789">Export the certificate (.cer file) from each SQL cluster node, and install it in the trusted root of each Service Fabric node.</span></span> <span data-ttu-id="b094f-790">Always-On クラスターには少なくとも 2 つの証明書があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-790">You will have at least two certificates for the Always-On cluster.</span></span> <span data-ttu-id="b094f-791">ただし、追加レプリカがある場合はそれ以上の証明書が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-791">However, you might have more if you have additional replicas.</span></span> 
    5. <span data-ttu-id="b094f-792">SQL サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="b094f-792">Restart the SQL service.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="b094f-793">詳細は、[Microsoft 管理コンソールを使用して SQL Server のインスタンスに対する SSL 暗号化を有効にする方法](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-793">For more information, see [How to enable SSL encryption for an instance of SQL Server by using Microsoft Management Console](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b094f-794">リモート処理を使用していた場合は、設定の完了後にクリーンアップ手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-794">If you used remoting, be sure to run the cleanup steps after the setup is completed.</span></span> <span data-ttu-id="b094f-795">手順については、[手順 20、リモート処理が使用されたら、CredSSP を終了処理する](#teardowncredssp)セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-795">For instructions, see the [Step 20. Tear down CredSSP, if remoting was used](#teardowncredssp) section.</span></span>

### <a name="step-14-configure-the-databases"></a><a name="configuredb"></a><span data-ttu-id="b094f-796">手順 14、</span><span class="sxs-lookup"><span data-stu-id="b094f-796">Step 14.</span></span> <span data-ttu-id="b094f-797">データベースを構成する</span><span class="sxs-lookup"><span data-stu-id="b094f-797">Configure the databases</span></span>

1. <span data-ttu-id="b094f-798">[LCS](https://lcs.dynamics.com/v2) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="b094f-798">Sign in to [LCS](https://lcs.dynamics.com/v2).</span></span>
2. <span data-ttu-id="b094f-799">ダッシュボードで、**共有アセット ライブラリ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-799">On the dashboard, select the **Shared asset library** tile.</span></span>
3. <span data-ttu-id="b094f-800">資産タイプとして **モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-800">Select **Model** as the asset type.</span></span> <span data-ttu-id="b094f-801">次にグリッドで、必要なリリースのデータ タイプを選択し、zip ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b094f-801">Then, in the grid, select the data type for the release that you want, and download the zip file.</span></span>

    | <span data-ttu-id="b094f-802">リリース</span><span class="sxs-lookup"><span data-stu-id="b094f-802">Release</span></span> | <span data-ttu-id="b094f-803"> データベース</span><span class="sxs-lookup"><span data-stu-id="b094f-803">Database</span></span> |
    |---------|----------|
    | <span data-ttu-id="b094f-804">オンプレミス プラットフォーム更新プログラム 41</span><span class="sxs-lookup"><span data-stu-id="b094f-804">On-premises Platform update 41</span></span> | <span data-ttu-id="b094f-805">Dynamics 365 for Operations オンプレミス、バージョン 10.0.17 デモ データ</span><span class="sxs-lookup"><span data-stu-id="b094f-805">Dynamics 365 for Operations on-premises, Version 10.0.17 Demo Data</span></span> |
    | <span data-ttu-id="b094f-806">オンプレミス プラットフォーム更新プログラム 41</span><span class="sxs-lookup"><span data-stu-id="b094f-806">On-premises Platform update 41</span></span> | <span data-ttu-id="b094f-807">Dynamics 365 for Operations オンプレミス、バージョン 10.0.17 空のデータ</span><span class="sxs-lookup"><span data-stu-id="b094f-807">Dynamics 365 for Operations on-premises, Version 10.0.17 Empty Data</span></span> |

4. <span data-ttu-id="b094f-808">zip ファイルには、単一のバックアップ (.bak) ファイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b094f-808">The zip file contains a single backup (.bak) file.</span></span> <span data-ttu-id="b094f-809">必要に応じて、ダウンロードするファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-809">Select the file to download, based on your requirements.</span></span>
5. <span data-ttu-id="b094f-810">**infrastructure\\ConfigTempate.xml** ファイルのデータベース セクションが、次の情報と共に正しく構成されているか確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-810">Make sure that the database section in the **infrastructure\\ConfigTempate.xml** file is configured correctly with the following information:</span></span>

    - <span data-ttu-id="b094f-811">データベース名。</span><span class="sxs-lookup"><span data-stu-id="b094f-811">The database name.</span></span>
    - <span data-ttu-id="b094f-812">データベース ファイルとログ設定。</span><span class="sxs-lookup"><span data-stu-id="b094f-812">The database file and log settings.</span></span> <span data-ttu-id="b094f-813">データベース設定は、指定された既定値以上にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-813">The database settings should not be lower than the default values that are specified.</span></span>
    - <span data-ttu-id="b094f-814">以前にダウンロードしたバックアップ ファイルのパス。</span><span class="sxs-lookup"><span data-stu-id="b094f-814">The path of the backup file that you downloaded earlier.</span></span> <span data-ttu-id="b094f-815">Finance + Operations データベースの既定の名前は **AXDB** です。</span><span class="sxs-lookup"><span data-stu-id="b094f-815">The default name of the Finance + Operations database is **AXDB**.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="b094f-816">SQL サービスを実行しているユーザーとスクリプトを実行しているユーザーは、バックアップ ファイルが格納されているフォルダーまたは共有に対して **読み取り** アクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-816">The user who is running the SQL service and the user who is running the scripts should have **Read** access on the folder or share where the backup file is located.</span></span>
    > - <span data-ttu-id="b094f-817">既に既存のデータベースの名前が同じである場合は、上書きされません。</span><span class="sxs-lookup"><span data-stu-id="b094f-817">If an existing database already has the same name, it won't be overwritten.</span></span>

6. <span data-ttu-id="b094f-818">**インフラストラクチャ** フォルダーを SQL Server コンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="b094f-818">Copy the **infrastructure** folder to the SQL Server machine.</span></span> <span data-ttu-id="b094f-819">次に、管理者特権モードで Windows PowerShell を開き、フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="b094f-819">Then open Windows PowerShell in elevated mode, and go to the folder.</span></span>

#### <a name="configure-the-orchestratordata-database"></a><span data-ttu-id="b094f-820">OrchestratorData データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b094f-820">Configure the OrchestratorData database</span></span>

- <span data-ttu-id="b094f-821">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-821">Run the following command.</span></span>

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

    <span data-ttu-id="b094f-822">Initialize-Database.ps1 スクリプトは、以下の処理を行います:</span><span class="sxs-lookup"><span data-stu-id="b094f-822">The Initialize-Database.ps1 script performs the following actions:</span></span>

    1. <span data-ttu-id="b094f-823">**OrchestratorData** という名前の空のデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="b094f-823">Create an empty database that is named **OrchestratorData**.</span></span> <span data-ttu-id="b094f-824">このデータベースは、オンプレミスのローカル エージェントによって配置を調整するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-824">This database is used by the on-premises local agent to orchestrate deployments.</span></span>
    1. <span data-ttu-id="b094f-825">データベースでローカル エージェント gMSA (**svc-LocalAgent$**) に **db\_owner** アクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="b094f-825">Grant **db\_owner** permissions on the database to the local agent gMSA (**svc-LocalAgent$**).</span></span>

#### <a name="configure-the-finance--operations-database"></a><span data-ttu-id="b094f-826">Finance + Operations データベースの構成</span><span class="sxs-lookup"><span data-stu-id="b094f-826">Configure the Finance + Operations database</span></span>

1. <span data-ttu-id="b094f-827">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-827">Run the following commands.</span></span>

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
    .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
    ```

    <span data-ttu-id="b094f-828">Initialize-Database.ps1 スクリプトは、以下の処理を行います:</span><span class="sxs-lookup"><span data-stu-id="b094f-828">The Initialize-Database.ps1 script performs the following actions:</span></span>

    1. <span data-ttu-id="b094f-829">指定されたバックアップ ファイルからデータベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="b094f-829">Restore the database from the specified backup file.</span></span>
    2. <span data-ttu-id="b094f-830">SQL 認証が有効になっている新しいユーザーを作成します (**axdbadmin**)。</span><span class="sxs-lookup"><span data-stu-id="b094f-830">Create a new user that SQL authentication is enabled for (**axdbadmin**).</span></span>
    3. <span data-ttu-id="b094f-831">**AXDB** データベースの次の表に基づいて、データベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="b094f-831">Map users to database roles, based on the following table for the **AXDB** database.</span></span>

        | <span data-ttu-id="b094f-832">ユーザー</span><span class="sxs-lookup"><span data-stu-id="b094f-832">User</span></span>            | <span data-ttu-id="b094f-833">種類</span><span class="sxs-lookup"><span data-stu-id="b094f-833">Type</span></span>    | <span data-ttu-id="b094f-834">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="b094f-834">Database role</span></span> |
        |-----------------|---------|---------------|
        | <span data-ttu-id="b094f-835">svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="b094f-835">svc-AXSF$</span></span>       | <span data-ttu-id="b094f-836">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-836">gMSA</span></span>    | <span data-ttu-id="b094f-837">db\_owner</span><span class="sxs-lookup"><span data-stu-id="b094f-837">db\_owner</span></span>     |
        | <span data-ttu-id="b094f-838">svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="b094f-838">svc-LocalAgent$</span></span> | <span data-ttu-id="b094f-839">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-839">gMSA</span></span>    | <span data-ttu-id="b094f-840">db\_owner</span><span class="sxs-lookup"><span data-stu-id="b094f-840">db\_owner</span></span>     |
        | <span data-ttu-id="b094f-841">svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="b094f-841">svc-FRPS$</span></span>       | <span data-ttu-id="b094f-842">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-842">gMSA</span></span>    | <span data-ttu-id="b094f-843">db\_owner</span><span class="sxs-lookup"><span data-stu-id="b094f-843">db\_owner</span></span>     |
        | <span data-ttu-id="b094f-844">svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="b094f-844">svc-FRAS$</span></span>       | <span data-ttu-id="b094f-845">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-845">gMSA</span></span>    | <span data-ttu-id="b094f-846">db\_owner</span><span class="sxs-lookup"><span data-stu-id="b094f-846">db\_owner</span></span>     |
        | <span data-ttu-id="b094f-847">axdbadmin</span><span class="sxs-lookup"><span data-stu-id="b094f-847">axdbadmin</span></span>       | <span data-ttu-id="b094f-848">SqlUser</span><span class="sxs-lookup"><span data-stu-id="b094f-848">SqlUser</span></span> | <span data-ttu-id="b094f-849">db\_owner</span><span class="sxs-lookup"><span data-stu-id="b094f-849">db\_owner</span></span>     |

    4. <span data-ttu-id="b094f-850">**TempD** データベースの次の表に基づいて、データベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="b094f-850">Map users to database roles, based on the following table for the **TempDB** database.</span></span>

        | <span data-ttu-id="b094f-851">ユーザー</span><span class="sxs-lookup"><span data-stu-id="b094f-851">User</span></span>      | <span data-ttu-id="b094f-852">種類</span><span class="sxs-lookup"><span data-stu-id="b094f-852">Type</span></span>    | <span data-ttu-id="b094f-853">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="b094f-853">Database role</span></span> |
        |-----------|---------|---------------|
        | <span data-ttu-id="b094f-854">svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="b094f-854">svc-AXSF$</span></span> | <span data-ttu-id="b094f-855">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-855">gMSA</span></span>    | <span data-ttu-id="b094f-856">db\_datareader、db\_datawriter、db\_ddladmin</span><span class="sxs-lookup"><span data-stu-id="b094f-856">db\_datareader, db\_datawriter, db\_ddladmin</span></span> |
        | <span data-ttu-id="b094f-857">axdbadmin</span><span class="sxs-lookup"><span data-stu-id="b094f-857">axdbadmin</span></span> | <span data-ttu-id="b094f-858">SqlUser</span><span class="sxs-lookup"><span data-stu-id="b094f-858">SqlUser</span></span> | <span data-ttu-id="b094f-859">db\_datareader、db\_datawriter、db\_ddladmin</span><span class="sxs-lookup"><span data-stu-id="b094f-859">db\_datareader, db\_datawriter, db\_ddladmin</span></span> |

    <span data-ttu-id="b094f-860">Configure-Database.ps1 スクリプトは、以下の処理を行います:</span><span class="sxs-lookup"><span data-stu-id="b094f-860">The Configure-Database.ps1 script performs the following actions:</span></span>

    1. <span data-ttu-id="b094f-861">**READ\_COMMITTED\_SNAPSHOT** を **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b094f-861">Set **READ\_COMMITTED\_SNAPSHOT** to **ON**.</span></span>
    2. <span data-ttu-id="b094f-862">**ALLOW\_SNAPSHOT\_ISOLATION** を **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b094f-862">Set **ALLOW\_SNAPSHOT\_ISOLATION** to **ON**.</span></span>
    3. <span data-ttu-id="b094f-863">指定したデータベースファイル と ログの設定を行います。</span><span class="sxs-lookup"><span data-stu-id="b094f-863">Set the specified database file and log settings.</span></span>
    4. <span data-ttu-id="b094f-864">**VIEW SERVER STATE** 権限を **axdbadmin** に付与します。</span><span class="sxs-lookup"><span data-stu-id="b094f-864">Grant the **VIEW SERVER STATE** permission to **axdbadmin**.</span></span>
    5. <span data-ttu-id="b094f-865">**ALTER ANY EVENT SESSION** 権限を **axdbadmin** に付与します。</span><span class="sxs-lookup"><span data-stu-id="b094f-865">Grant the **ALTER ANY EVENT SESSION** permission to **axdbadmin**.</span></span>
    6. <span data-ttu-id="b094f-866">**VIEW SERVER STATE** 権限を **\[contoso\\svc-AXSF$\]** に付与します。</span><span class="sxs-lookup"><span data-stu-id="b094f-866">Grant the **VIEW SERVER STATE** permission to **\[contoso\\svc-AXSF$\]**.</span></span>
    7. <span data-ttu-id="b094f-867">**ALTER ANY EVENT SESSION** 権限を **\[contoso\\svc-AXSF$\]** に付与します。</span><span class="sxs-lookup"><span data-stu-id="b094f-867">Grant the **ALTER ANY EVENT SESSION** permission to **\[contoso\\svc-AXSF$\]**.</span></span>

2. <span data-ttu-id="b094f-868">データベース ユーザーをリセットするには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-868">Run the following command to reset the database users.</span></span>

    ```powershell
    .\Reset-DatabaseUsers.ps1 -DatabaseServer '<FQDN of the SQL server>' -DatabaseName '<AX database name>'
    ```

#### <a name="configure-the-financial-reporting-database"></a><span data-ttu-id="b094f-869">財務レポート データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b094f-869">Configure the Financial Reporting database</span></span>

- <span data-ttu-id="b094f-870">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-870">Run the following command.</span></span>

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName MR
    ```

    <span data-ttu-id="b094f-871">Initialize-Database.ps1 スクリプトは、以下の処理を行います:</span><span class="sxs-lookup"><span data-stu-id="b094f-871">The Initialize-Database.ps1 script performs the following actions:</span></span>

    1. <span data-ttu-id="b094f-872">**FinancialReporting** という名前の空のデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="b094f-872">Create an empty database that is named **FinancialReporting**.</span></span>
    2. <span data-ttu-id="b094f-873">次の表に基づいて、データベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="b094f-873">Map the users to database roles, based on the following table.</span></span>

        | <span data-ttu-id="b094f-874">ユーザー</span><span class="sxs-lookup"><span data-stu-id="b094f-874">User</span></span>            | <span data-ttu-id="b094f-875">種類</span><span class="sxs-lookup"><span data-stu-id="b094f-875">Type</span></span> | <span data-ttu-id="b094f-876">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="b094f-876">Database role</span></span> |
        |-----------------|------|---------------|
        | <span data-ttu-id="b094f-877">svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="b094f-877">svc-LocalAgent$</span></span> | <span data-ttu-id="b094f-878">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-878">gMSA</span></span> | <span data-ttu-id="b094f-879">db\_owner</span><span class="sxs-lookup"><span data-stu-id="b094f-879">db\_owner</span></span>     |
        | <span data-ttu-id="b094f-880">svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="b094f-880">svc-FRPS$</span></span>       | <span data-ttu-id="b094f-881">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-881">gMSA</span></span> | <span data-ttu-id="b094f-882">db\_owner</span><span class="sxs-lookup"><span data-stu-id="b094f-882">db\_owner</span></span>     |
        | <span data-ttu-id="b094f-883">svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="b094f-883">svc-FRAS$</span></span>       | <span data-ttu-id="b094f-884">gMSA</span><span class="sxs-lookup"><span data-stu-id="b094f-884">gMSA</span></span> | <span data-ttu-id="b094f-885">db\_owner</span><span class="sxs-lookup"><span data-stu-id="b094f-885">db\_owner</span></span>     |

### <a name="step-15-encrypt-credentials"></a><a name="encryptcred"></a><span data-ttu-id="b094f-886">手順 15、</span><span class="sxs-lookup"><span data-stu-id="b094f-886">Step 15.</span></span> <span data-ttu-id="b094f-887">資格情報の暗号化</span><span class="sxs-lookup"><span data-stu-id="b094f-887">Encrypt credentials</span></span>

1. <span data-ttu-id="b094f-888">任意のクライアント コンピューターで、**LocalMachine\\My** 証明書ストアに暗号化証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="b094f-888">On any client machine, install the encipherment certificate in the **LocalMachine\\My** certificate store.</span></span>
2. <span data-ttu-id="b094f-889">現在のユーザーにこの証明書の秘密キーへの **読み取り** アクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="b094f-889">Grant the current user **Read** access to the private key of this certificate.</span></span>
3. <span data-ttu-id="b094f-890">次のようにして、**Credentials.json** ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b094f-890">Create the **Credentials.json** file, as shown here.</span></span>

    ```json
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - <span data-ttu-id="b094f-891">**AccountPassword** – AOS ドメインユーザー (**contoso\\axserviceuser**) の暗号化されたドメイン ユーザー パスワード。</span><span class="sxs-lookup"><span data-stu-id="b094f-891">**AccountPassword** – The encrypted domain user password for the AOS domain user (**contoso\\axserviceuser**).</span></span>
    - <span data-ttu-id="b094f-892">**SqlUser** – Finance + Operations データベース (**AXDB**) にアクセス権限が付与されている暗号化された SQL ユーザー (**axdbadmin**)</span><span class="sxs-lookup"><span data-stu-id="b094f-892">**SqlUser** – The encrypted SQL user (**axdbadmin**) that has access to the Finance + Operations database (**AXDB**)</span></span>
    - <span data-ttu-id="b094f-893">**SqlPassword** – 暗号化された SQL パスワード。</span><span class="sxs-lookup"><span data-stu-id="b094f-893">**SqlPassword** – The encrypted SQL password.</span></span>

4. <span data-ttu-id="b094f-894">.json ファイルを SMB ファイル共有: **\\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json** にコピーします。</span><span class="sxs-lookup"><span data-stu-id="b094f-894">Copy the .json file to the SMB file share: **\\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json**.</span></span>
5. <span data-ttu-id="b094f-895">暗号化された値で **Credentials.json** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="b094f-895">Update the **Credentials.json** file with encrypted values.</span></span>

    ```powershell
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | Set-Clipboard
    ```

    > [!IMPORTANT]
    > - <span data-ttu-id="b094f-896">**Invoke-ServiceFabricEncryptText** コマンドを呼び出す前に、[Microsoft Azure Service Fabric ソフトウェア開発キット (SDK)](/azure/service-fabric/service-fabric-get-started#sdk-installation-only) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-896">Before you can invoke the **Invoke-ServiceFabricEncryptText** command, you must install the [Microsoft Azure Service Fabric software development kit (SDK)](/azure/service-fabric/service-fabric-get-started#sdk-installation-only).</span></span>
    > - <span data-ttu-id="b094f-897">Service Fabric SDK をインストールした後で、次のエラー メッセージが表示されます:「Invoke-ServiceFabricEncryptText は認識されないコマンドです」</span><span class="sxs-lookup"><span data-stu-id="b094f-897">After you install the Service Fabric SDK, you might receive the following error message: "Invoke-ServiceFabricEncryptText is not recognized command."</span></span> <span data-ttu-id="b094f-898">この場合は、コンピュータを再起動し、もう一度やり直してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-898">In this case, restart the computer, and try again.</span></span>

    > [!WARNING]
    > <span data-ttu-id="b094f-899">すべての **ServiceFabricEncryptText** コマンドの起動が完了したら、Windows PowerShell の履歴を削除することを忘れないでください。</span><span class="sxs-lookup"><span data-stu-id="b094f-899">After you've finished invoking all the **Invoke-ServiceFabricEncryptText** commands, remember to delete the Windows PowerShell history.</span></span> <span data-ttu-id="b094f-900">それ以外の場合は、暗号化されていない資格情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-900">Otherwise, your non-encrypted credentials will be visible.</span></span>

### <a name="step-16-set-up-ssis"></a><a name="setupssis"></a><span data-ttu-id="b094f-901">手順 16、</span><span class="sxs-lookup"><span data-stu-id="b094f-901">Step 16.</span></span> <span data-ttu-id="b094f-902">SSIS を設定する</span><span class="sxs-lookup"><span data-stu-id="b094f-902">Set up SSIS</span></span>

<span data-ttu-id="b094f-903">データ管理と SSIS ワークロードを有効にするには、各 AOS VM に SSIS をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-903">To enable Data management and SSIS workloads, you must install SSIS on each AOS VM.</span></span> <span data-ttu-id="b094f-904">各 AOS VM で、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b094f-904">Follow these steps on each AOS VM.</span></span>

1. <span data-ttu-id="b094f-905">コンピューターに SSIS インストールへのアクセス許可があることを確認し、**SSIS セットアップ** ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="b094f-905">Verify that the machine has access to the SSIS installation, and open the **SSIS Setup** wizard.</span></span>
2. <span data-ttu-id="b094f-906">**機能の選択** ページの **機能** ウィンドウで、**Integration Services** および **SQL クライアント接続 SDK** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b094f-906">On the **Feature Selection** page, in the **Features** pane, select the **Integration Services** and **SQL Client Connectivity SDK** check boxes.</span></span>
3. <span data-ttu-id="b094f-907">セットアップを完了し、インストールが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-907">Complete the setup, and verify that the installation was successful.</span></span>

<span data-ttu-id="b094f-908">詳細については、[統合サービス (SSIS) のインストール](/sql/integration-services/install-windows/install-integration-services)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-908">For more information, see [Install Integration Services (SSIS)](/sql/integration-services/install-windows/install-integration-services).</span></span>

### <a name="step-17-set-up-ssrs"></a><a name="setupssrs"></a><span data-ttu-id="b094f-909">手順 17、</span><span class="sxs-lookup"><span data-stu-id="b094f-909">Step 17.</span></span> <span data-ttu-id="b094f-910">SSRS を設定する</span><span class="sxs-lookup"><span data-stu-id="b094f-910">Set up SSRS</span></span>

<span data-ttu-id="b094f-911">複数の SSRS ノードを構成できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-911">You can configure more than one SSRS node.</span></span> <span data-ttu-id="b094f-912">詳細については、[SSRS ノードの高可用性の構成](./onprem-SSRSHA.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-912">For more information, see [Configuring High Availability for SSRS nodes](./onprem-SSRSHA.md).</span></span>

1. <span data-ttu-id="b094f-913">開始する前に、このトピックの冒頭に記載されている[前提条件](#prerequisites)が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-913">Before you begin, make sure that the [prerequisites](#prerequisites) that are listed at the beginning of this topic are in place.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="b094f-914">SSRS のインストール時にデータベース エンジンをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-914">You must install the Database Engine when you install SSRS.</span></span>
    > - <span data-ttu-id="b094f-915">SSRS インスタンスを構成 **しない** でください。</span><span class="sxs-lookup"><span data-stu-id="b094f-915">Do **not** configure the SSRS instance.</span></span> <span data-ttu-id="b094f-916">レポート サービスは、すべてを自動的に構成されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-916">The reporting service will automatically configure everything.</span></span>

1. <span data-ttu-id="b094f-917">各 BI ノードについては、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-917">For each BI node, follow these steps:</span></span>

    1. <span data-ttu-id="b094f-918">**インフラストラクチャ** フォルダーをコピーします。</span><span class="sxs-lookup"><span data-stu-id="b094f-918">Copy the **infrastructure** folder.</span></span> <span data-ttu-id="b094f-919">次に、管理者特権モードで Windows PowerShell を開き、フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="b094f-919">Then open Windows PowerShell in elevated mode, and go to the folder.</span></span>
    1. <span data-ttu-id="b094f-920">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-920">Run the following commands.</span></span>

        ```powershell
        .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName BI
        .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName BI
        ```

        <span data-ttu-id="b094f-921">Initialize-Database.ps1 スクリプトは、gMSA を次のデータベースおよびロールにマップします。</span><span class="sxs-lookup"><span data-stu-id="b094f-921">The Initialize-Database.ps1 script maps the gMSA to the following databases and roles.</span></span>

        | <span data-ttu-id="b094f-922">ユーザー</span><span class="sxs-lookup"><span data-stu-id="b094f-922">User</span></span>           | <span data-ttu-id="b094f-923"> データベース</span><span class="sxs-lookup"><span data-stu-id="b094f-923">Database</span></span> | <span data-ttu-id="b094f-924">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="b094f-924">Database role</span></span> |
        |----------------|----------|---------------|
        | <span data-ttu-id="b094f-925">svc-ReportSvc$</span><span class="sxs-lookup"><span data-stu-id="b094f-925">svc-ReportSvc$</span></span> | <span data-ttu-id="b094f-926">マスター</span><span class="sxs-lookup"><span data-stu-id="b094f-926">master</span></span>   | <span data-ttu-id="b094f-927">db\_owner</span><span class="sxs-lookup"><span data-stu-id="b094f-927">db\_owner</span></span> |
        | <span data-ttu-id="b094f-928">svc-ReportSvc$</span><span class="sxs-lookup"><span data-stu-id="b094f-928">svc-ReportSvc$</span></span> | <span data-ttu-id="b094f-929">msdb</span><span class="sxs-lookup"><span data-stu-id="b094f-929">msdb</span></span>     | <span data-ttu-id="b094f-930">db\_datareader、db\_datawriter、db\_securityadmin</span><span class="sxs-lookup"><span data-stu-id="b094f-930">db\_datareader, db\_datawriter, db\_securityadmin</span></span> |

        <span data-ttu-id="b094f-931">Configure-Database.ps1 スクリプトは、以下のアクションを実行します:</span><span class="sxs-lookup"><span data-stu-id="b094f-931">The Configure-Database.ps1 script performs the following action:</span></span>

        - <span data-ttu-id="b094f-932">**CREATE ANY DATABASE** 権限を **\[contoso\\svc-ReportSvc$\]** に付与します。</span><span class="sxs-lookup"><span data-stu-id="b094f-932">Grant the **CREATE ANY DATABASE** permission to **\[contoso\\svc-ReportSvc$\]**.</span></span>

### <a name="step-18-configure-ad-fs"></a><a name="configureadfs"></a><span data-ttu-id="b094f-933">手順 18、</span><span class="sxs-lookup"><span data-stu-id="b094f-933">Step 18.</span></span> <span data-ttu-id="b094f-934">AD FS のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b094f-934">Configure AD FS</span></span>

<span data-ttu-id="b094f-935">この手順を完了する前に、AD FS を Windows Server 2016 に展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-935">Before you can complete this procedure, AD FS must be deployed on Windows Server 2016.</span></span> <span data-ttu-id="b094f-936">AD FS を展開する方法については、[Windows Server 2016 配置ガイドおよび 2012 R2 AD FS 配置ガイド](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-936">For information about how to deploy AD FS, see [Deployment Guide Windows Server 2016 and 2012 R2 AD FS Deployment Guide](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).</span></span>

<span data-ttu-id="b094f-937">Finance + Operations では、既定で標準のコンフィギュレーション以外の、AD FS の追加のコンフィギュレーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-937">Finance + Operations requires additional configuration of AD FS, beyond the default out-of-box configuration.</span></span> <span data-ttu-id="b094f-938">以下の Windows PowerShell コマンドを、AD FS ロール サービスがインストールされているマシン上で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-938">The following Windows PowerShell commands must be run on the machine where the AD FS role service is installed.</span></span> <span data-ttu-id="b094f-939">ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-939">The user account must have enough permissions to administer AD FS.</span></span> <span data-ttu-id="b094f-940">たとえば、ユーザーには、ドメイン管理者アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-940">For example, the user must have a domain administrator account.</span></span> <span data-ttu-id="b094f-941">複雑な AD FS シナリオでは、ドメイン管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="b094f-941">For complex AD FS scenarios, consult your domain administrator.</span></span>

1. <span data-ttu-id="b094f-942">AD FS 識別子を構成して、AD FS トークン発行者と一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="b094f-942">Configure the AD FS identifier so that it matches the AD FS token issuer.</span></span>

    <span data-ttu-id="b094f-943">このコマンドは、Finance + Operations クライアントの **ユーザー** ページ (**システム管理** \> **ユーザー** \> **ユーザー**) での **ユーザーをインポートする** オプションの使用による新しいユーザーの追加に関連しています。</span><span class="sxs-lookup"><span data-stu-id="b094f-943">This command is related to adding new users by using the **Import users** option on the **Users** page (**System administration** \> **Users** \> **Users**) in the Finance + Operations client.</span></span>

    ```PowerShell
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. <span data-ttu-id="b094f-944">混在環境用に AD FS を構成していない限り、イントラネット認証接続用に Windows 統合認証 (WIA) を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-944">You should disable Windows Integrated Authentication (WIA) for intranet authentication connections, unless you've configured AD FS for mixed environments.</span></span> <span data-ttu-id="b094f-945">WIA を AD FS で使用できるように構成する方法の詳細については、[AD FS で Windows 統合認証 (WIA) を使用するようにブラウザを構成する](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-945">For more information about how to configure WIA so that it can be used with AD FS, see [Configure browsers to use Windows Integrated Authentication (WIA) with AD FS](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).</span></span>

    <span data-ttu-id="b094f-946">このコマンドは、Finance + Operations クライアントへのサインイン時のフォーム認証の使用に関連しています。</span><span class="sxs-lookup"><span data-stu-id="b094f-946">This command is related to using forms authentication upon sign-in the Finance + Operations client.</span></span> <span data-ttu-id="b094f-947">シングル サインオンなど、他のオプションも利用できる場合がありますが、追加の設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-947">Other options, such as single sign-on, might be available but require additional setup.</span></span>

    ```powershell
    Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
    ```

3. <span data-ttu-id="b094f-948">サインインの場合、ユーザーの電子メール アドレスは許容される認証入力でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b094f-948">For sign-in, the user's email address must be acceptable authentication input.</span></span>

    <span data-ttu-id="b094f-949">このコマンドは、電子メール要求の設定に関連しています。</span><span class="sxs-lookup"><span data-stu-id="b094f-949">This command is related to setting up email claims.</span></span> <span data-ttu-id="b094f-950">変換ルールなど、他のオプションも利用できる場合がありますが、追加の設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-950">Other options, such as transformation rules, might be available but require additional setup.</span></span>

    ```powershell
    Add-Type -AssemblyName System.Net
    $fqdn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
    $domainName = $fqdn.Substring($fqdn.IndexOf('.')+1)
    Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
    ```

<span data-ttu-id="b094f-951">AD FS が認証を交換するために Finance + Operations を信頼できるようにするには、AD FS で AD FS アプリケーション グループの下にさまざまなアプリケーション エントリを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-951">Before AD FS can trust Finance + Operations for the exchange of authentication, various application entries must be registered under an AD FS application group in AD FS.</span></span> <span data-ttu-id="b094f-952">設定プロセスをスピードアップしてエラーを減らすために、Publish-ADFSApplicationGroup.ps1 スクリプトを使用して登録します。</span><span class="sxs-lookup"><span data-stu-id="b094f-952">To speed up the setup process and help reduce errors, you can use the Publish-ADFSApplicationGroup.ps1 script for registration.</span></span> <span data-ttu-id="b094f-953">このスクリプトと D365FO-OP ディレクトリを、AD FS ロール サービスがインストールされているコンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="b094f-953">Copy this script and the D365FO-OP directory to a machine where the AD FS role service is installed.</span></span> <span data-ttu-id="b094f-954">次に、AD FS を管理するための十分なアクセス許可を持つユーザー アカウントを使用してスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-954">Then run the script by using a user account that has enough permissions to administer AD FS.</span></span> <span data-ttu-id="b094f-955">(たとえば、管理者アカウントを使用します。)</span><span class="sxs-lookup"><span data-stu-id="b094f-955">(For example, use an administrator account.)</span></span>

<span data-ttu-id="b094f-956">スクリプトの使用方法の詳細については、スクリプトに記載されているドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-956">For more information about how to use the script, see the documentation that is listed in the script.</span></span> <span data-ttu-id="b094f-957">後に LCS でこの情報が必要となるため、出力に指定されているクライアント ID を書き留めておいてください。</span><span class="sxs-lookup"><span data-stu-id="b094f-957">Make a note of the client IDs that are specified in the output, because you will need this information in LCS later.</span></span> <span data-ttu-id="b094f-958">クライアント ID を失った場合は、AD FS がインストールされているコンピューターにサインインし、サーバー マネージャーを開き、**ツール** \> **AD FS 管理** \> **アプリケーション グループ** \> **Microsoft Dynamics 365 for Operations オンプレミス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b094f-958">If you lose the client IDs, sign in to the machine where AD FS is installed, open Server Manager, and go to **Tools** \> **AD FS Management** \> **Application Groups** \> **Microsoft Dynamics 365 for Operations On-premises**.</span></span> <span data-ttu-id="b094f-959">ネイティブ アプリケーションでクライアント ID を検索できます。</span><span class="sxs-lookup"><span data-stu-id="b094f-959">You can find the client IDs under the native applications.</span></span>

> [!NOTE]
> <span data-ttu-id="b094f-960">以前に構成した AD FS サーバーを別の環境で再利用する方法については、[複数の環境に同じ AD FS インスタンスを再使用する](./onprem-reuseadfs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-960">If you want to reuse your previously configured AD FS server for additional environments, see [Reuse the same AD FS instance for multiple environments](./onprem-reuseadfs.md).</span></span>

```powershell
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
```

![アプリケーション グループのプロパティ](./media/OPSetup_05_ApplicatioGroupProperties.png)

<span data-ttu-id="b094f-962">最後に、**AOSNodeType** タイプの Service Fabric ノード上の AD FS OpenID コンフィギュレーション URL にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-962">Finally, verify that you can access the AD FS OpenID configuration URL on a Service Fabric node of the **AOSNodeType** type.</span></span> <span data-ttu-id="b094f-963">このチェックを行うには、Web ブラウザーで `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` を開きます。</span><span class="sxs-lookup"><span data-stu-id="b094f-963">To do this check, try to open `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` in a web browser.</span></span> <span data-ttu-id="b094f-964">サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていません。</span><span class="sxs-lookup"><span data-stu-id="b094f-964">If you receive a message that states that the site isn't secure, you haven't added your AD FS SSL certificate to the Trusted Root Certification Authorities store.</span></span> <span data-ttu-id="b094f-965">この手順については、「AD FS 展開ガイド」で説明されています。</span><span class="sxs-lookup"><span data-stu-id="b094f-965">This step is described in the AD FS deployment guide.</span></span> <span data-ttu-id="b094f-966">リモート処理を使用している場合は、次のコマンドを実行して Service Fabric Cluster のすべてのノードに証明書をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="b094f-966">If you're using remoting, you can run the following command to install the certificate on all nodes in the Service Fabric cluster.</span></span>

```powershell
# If remoting, execute
.\Install-ADFSCert-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

<span data-ttu-id="b094f-967">URL にアクセスできる場合、JavaScript Object Notation (JSON) ファイルが返されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-967">If you can access the URL, a JavaScript Object Notation (JSON) file is returned.</span></span> <span data-ttu-id="b094f-968">このファイルには AD FS コンフィギュレーションが含まれており、AD FS URL が信頼されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="b094f-968">This file contains your AD FS configuration, and it will indicate that your AD FS URL is trusted.</span></span>

<span data-ttu-id="b094f-969">これで、インフラストラクチャの設定を完了しました。</span><span class="sxs-lookup"><span data-stu-id="b094f-969">You've now completed the setup of the infrastructure.</span></span> <span data-ttu-id="b094f-970">次のセクションでは、コネクタを設定して LCS に Finance + Operations 環境を展開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b094f-970">The following sections describe how set up your connector and deploy your Finance + Operations environment in LCS.</span></span>

### <a name="step-19-configure-a-connector-and-install-an-on-premises-local-agent"></a><a name="configureconnector"></a><span data-ttu-id="b094f-971">手順 19、</span><span class="sxs-lookup"><span data-stu-id="b094f-971">Step 19.</span></span> <span data-ttu-id="b094f-972">コネクタを構成し、オンプレミスのローカル エージェントをインストールする</span><span class="sxs-lookup"><span data-stu-id="b094f-972">Configure a connector and install an on-premises local agent</span></span>

1. <span data-ttu-id="b094f-973">[LCS](https://lcs.dynamics.com/) にサインインし、オンプレミスの実装プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="b094f-973">Sign in to [LCS](https://lcs.dynamics.com/), and open your on-premises implementation project.</span></span>
2. <span data-ttu-id="b094f-974">メニュー ボタン (ハンバーガーまたはハンバーガー ボタンと呼ばれる場合もあります) を選択してから、**プロジェクト設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-974">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Project settings**.</span></span>
3. <span data-ttu-id="b094f-975">**オンプレミス コネクタ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-975">Select **On-premises connectors**.</span></span>
4. <span data-ttu-id="b094f-976">**追加** を選択して、新しいオンプレミス コネクタを作成します。</span><span class="sxs-lookup"><span data-stu-id="b094f-976">Select **Add** to create a new on-premises connector.</span></span> 
5. <span data-ttu-id="b094f-977">**1: ホスト インフラストラクチャ設定** タブで、**エージェント インストーラーをダウンロードする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-977">On the **1: Setup host infrastructure** tab, select **Download agent installer**.</span></span>
6. <span data-ttu-id="b094f-978">zip ファイルのダウンロード後、そのファイルがブロックされていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-978">After the zip file is downloaded, verify that it's unblocked.</span></span> <span data-ttu-id="b094f-979">ファイルを選択したまま (または右クリック) にしてから、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-979">Select and hold (or right-click) the file, and then select **Properties**.</span></span> <span data-ttu-id="b094f-980">**プロパティ** ダイアログ ボックスで、**ブロック解除** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-980">In the **Properties** dialog box, select the **Unblock** check box.</span></span>
7. <span data-ttu-id="b094f-981">**OrchestratorType** タイプの Service Fabric ノードの 1 つでエージェント インストーラーを解凍します。</span><span class="sxs-lookup"><span data-stu-id="b094f-981">Unzip the agent installer on one of the Service Fabric nodes of the **OrchestratorType** type.</span></span>
8. <span data-ttu-id="b094f-982">ファイルの解凍後、LCS のオンプレミス コネクタに戻ります。</span><span class="sxs-lookup"><span data-stu-id="b094f-982">After the file is unzipped, go back to your on-premises connector in LCS.</span></span>
9. <span data-ttu-id="b094f-983">**2: エージェントのコンフィギュレーション** タブで、**コンフィギュレーションの入力** を選択し、コンフィギュレーション設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="b094f-983">On the **2: Configure agent** tab, select **Enter configuration**, and enter the configuration settings.</span></span> <span data-ttu-id="b094f-984">必要な値を取得するには、**インフラストラクチャ** フォルダーと最新のコンフィギュレーション ファイルを持つすべてのコンピューターで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-984">To get the required values, run the following command on any machine that has the **infrastructure** folder and up-to-date configuration files.</span></span>

    ```powershell
    .\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

10. <span data-ttu-id="b094f-985">コンフィギュレーションを保存してから、**コンフィギュレーションのダウンロード** を選択して **localagent-config.json** コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b094f-985">Save the configuration, and then select **Download configurations** to download the **localagent-config.json** configuration file.</span></span>
11. <span data-ttu-id="b094f-986">**localagent-config.json** ファイルを、エージェント インストーラー パッケージが展開されているコンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="b094f-986">Copy the **localagent-config.json** file to the machine where the agent installer package is located.</span></span>
12. <span data-ttu-id="b094f-987">**コマンド プロンプト** ウィンドウで、エージェント インストーラーを含むフォルダーに移動して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-987">In a **Command Prompt** window, go to the folder that contains the agent installer, and run the following command.</span></span>

    ```powershell
    LocalAgentCLI.exe Install <path of config.json>
    ```

    > [!NOTE]
    > <span data-ttu-id="b094f-988">このコマンドを実行するユーザーは、OrchestratorData データベースに対して **db\_owner** のアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-988">The user who runs this command must have **db\_owner** permissions on the OrchestratorData database.</span></span>

13. <span data-ttu-id="b094f-989">ローカル エージェントが正常にインストールされてから、LCS のオンプレミス コネクタに戻るようにします。</span><span class="sxs-lookup"><span data-stu-id="b094f-989">After the local agent is successfully installed, go back to your on-premises connector in LCS.</span></span>
14. <span data-ttu-id="b094f-990">**3: 設定の検証** タブで、**メッセージ エージェント** を選択して、ローカル エージェントへの LCS 接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="b094f-990">On the **3: Validate setup** tab, select **Message agent** to test for LCS connectivity to your local agent.</span></span> <span data-ttu-id="b094f-991">接続が正常に確立されると、下のメッセージが表示されます: 「検証が完了しました。</span><span class="sxs-lookup"><span data-stu-id="b094f-991">When a connection is successfully established, you will receive the following message: "Validation complete.</span></span> <span data-ttu-id="b094f-992">エージェントへの接続が確立されました。」</span><span class="sxs-lookup"><span data-stu-id="b094f-992">Agent connection established."</span></span>

### <a name="step-20-tear-down-credssp-if-remoting-was-used"></a><a name="teardowncredssp"></a><span data-ttu-id="b094f-993">手順 20、</span><span class="sxs-lookup"><span data-stu-id="b094f-993">Step 20.</span></span> <span data-ttu-id="b094f-994">リモート処理が使用されたら、CredSSP を終了処理する</span><span class="sxs-lookup"><span data-stu-id="b094f-994">Tear down CredSSP, if remoting was used</span></span>

<span data-ttu-id="b094f-995">セットアップ中にリモート処理スクリプトのいずれかが使用された場合は、セットアップ プロセスの中断時または完了後に、次のコマンドを実行してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-995">If you used any of the remoting scripts during setup, be sure to run the following command during breaks in the setup process, or after the setup is completed.</span></span>

```powershell
.\Disable-CredSSP-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

<span data-ttu-id="b094f-996">以前のリモート処理 Windows PowerShell ウィンドウが誤って終了し、CredSSP が有効になったままである場合、このコマンドにより、コンフィギュレーション ファイルで指定されたすべてのコンピューター上で無効にされます。</span><span class="sxs-lookup"><span data-stu-id="b094f-996">If the previous remoting Windows PowerShell window was accidentally closed, and CredSSP was left enabled, this command disables it on all the machines that are specified in the configuration file.</span></span>

### <a name="step-21-deploy-your-finance--operations-environment-from-lcs"></a><a name="deploy"></a><span data-ttu-id="b094f-997">手順 21、</span><span class="sxs-lookup"><span data-stu-id="b094f-997">Step 21.</span></span> <span data-ttu-id="b094f-998">LCS から Finance + Operations 環境を配置する</span><span class="sxs-lookup"><span data-stu-id="b094f-998">Deploy your Finance + Operations environment from LCS</span></span>

1. <span data-ttu-id="b094f-999">LCS で、オンプレミスの実装プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="b094f-999">In LCS, open your on-premises implementation project.</span></span>
2. <span data-ttu-id="b094f-1000">**環境** \> **サンドボックス** に移動し、**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1000">Go to **Environment** \> **Sandbox**, and select **Configure**.</span></span> <span data-ttu-id="b094f-1001">必要な値を取得するには、プライマリ ドメイン コントローラ VM で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1001">To get the required values, run the following command on the primary domain controller VM.</span></span> <span data-ttu-id="b094f-1002">その VM には、ADFS および DNS サーバー設定へのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="b094f-1002">That VM must have access to ADFS and the DNS server settings.</span></span>

    ```powershell
    .\Get-DeploymentSettings.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

3. <span data-ttu-id="b094f-1003">新しい展開では、環境のトポロジを選択し、展開を開始するウィザードを完了します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1003">For new deployments, select your environment topology, and then complete the wizard to start your deployment.</span></span>

    <span data-ttu-id="b094f-1004">準備フェーズ中に、LCS は環境の Service Fabric アプリケーション パッケージを組み立てます。</span><span class="sxs-lookup"><span data-stu-id="b094f-1004">During the preparation phase, LCS assembles the Service Fabric application packages for your environment.</span></span> <span data-ttu-id="b094f-1005">配置を開始するローカル エージェントにメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1005">It then sends a message to the local agent to start deployment.</span></span> <span data-ttu-id="b094f-1006">環境ステータスが **準備中** であることに注意します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1006">You should notice that the environment state is **Preparing**.</span></span>

    ![準備状態の環境](./media/Preparing2021.png)

4. <span data-ttu-id="b094f-1008">環境の詳細ページで、**完全な詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1008">Select **Full details** to open the environment details page.</span></span> <span data-ttu-id="b094f-1009">ページの右上隅には、環境ステータスが **準備中** として表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1009">Notice that the upper-right corner of the page shows the environment status as **Preparing**.</span></span>

    ![準備中ステータスを表示する環境の詳細ページ](./media/Details_Preparing2021.png)

    <span data-ttu-id="b094f-1011">ローカル エージェントは展開要求を受け取り、展開を開始し、環境の準備ができたら LCS に再度通知します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1011">The local agent picks up the deployment request, starts the deployment, and communicates back to LCS when the environment is ready.</span></span> <span data-ttu-id="b094f-1012">展開を開始すると、環境の状態が **展開中** に変わることに注意します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1012">When deployment is started, you should notice that the environment state is changed to **Deploying**.</span></span>

    ![展開状態の環境](./media/Deploying2021.png)

5. <span data-ttu-id="b094f-1014">環境の詳細ページで、**完全な詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1014">Select **Full details** to open the environment details page.</span></span> <span data-ttu-id="b094f-1015">ページの右上隅には、環境ステータスが **展開中** として表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1015">Notice that the upper-right corner of the page shows the environment status as **Deploying**.</span></span>

    ![展開中ステータスを表示する環境の詳細ページ](./media/Details_Deploying2021.png)

6. <span data-ttu-id="b094f-1017">展開に失敗すると、環境の状態が **失敗** に変更され、**再構成** ボタンが環境で使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="b094f-1017">If the deployment fails, the environment state is changed to **Failed**, and the **Reconfigure** button becomes available for the environment.</span></span> <span data-ttu-id="b094f-1018">基になる問題を修正し、**再構成** を選択して、任意のコンフィギュレーションの変更を更新してから、**展開** の再試行を選択します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1018">Fix the underlying issue, select **Reconfigure**, update any configuration changes, and then select **Deploy** to retry the deployment.</span></span>

    ![失敗状態の環境で使用する再構成ボタン](./media/Failed2021.png)

    <span data-ttu-id="b094f-1020">環境を再構成する方法の詳細については、[環境を再構成して、新しいプラットフォームまたはトポロジを採用する](../lifecycle-services/reconfigure-environment.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-1020">For information about how to reconfigure an environment, see [Reconfigure environments to take a new platform or topology](../lifecycle-services/reconfigure-environment.md).</span></span>

<span data-ttu-id="b094f-1021">次の図は、正常な展開を示します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1021">The following illustration shows a successful deployment.</span></span> <span data-ttu-id="b094f-1022">ページの右上隅には、環境ステータスが **展開済** として表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1022">Notice that the upper-right corner of the page shows the environment status as **Deployed**.</span></span>

![環境が正常に展開された](./media/Deployed2021.png)

### <a name="step-22-connect-to-your-finance--operations-environment"></a><a name="connect"></a><span data-ttu-id="b094f-1024">手順 22、</span><span class="sxs-lookup"><span data-stu-id="b094f-1024">Step 22.</span></span> <span data-ttu-id="b094f-1025">Finance + Operations 環境への接続</span><span class="sxs-lookup"><span data-stu-id="b094f-1025">Connect to your Finance + Operations environment</span></span>

- <span data-ttu-id="b094f-1026">Web ブラウザーで、`https://[yourD365FOdomain]/namespaces/AXSF` に移動します。そこでは **yourD365FOdomain** がこのトピック前半の [手順 1. ドメイン名と DNS ゾーンの計画](#plandomain)セクションで定義したドメイン名です。</span><span class="sxs-lookup"><span data-stu-id="b094f-1026">In a web browser, go to `https://[yourD365FOdomain]/namespaces/AXSF`, where **yourD365FOdomain** is the domain name that you defined in the [Step 1. Plan your domain name and DNS zones](#plandomain) section earlier in this topic.</span></span>

## <a name="known-issues"></a><span data-ttu-id="b094f-1027">既知の問題</span><span class="sxs-lookup"><span data-stu-id="b094f-1027">Known issues</span></span>

### <a name="when-you-run-the-new-d365fogmsaaccounts-cmdlet-you-receive-the-following-error-message-key-does-not-exist"></a><span data-ttu-id="b094f-1028">New-D365FOFOSAAccounts cmdlet を実行すると、次のエラー メッセージが表示されます: 「キーが存在しません」</span><span class="sxs-lookup"><span data-stu-id="b094f-1028">When you run the New-D365FOGMSAAccounts cmdlet, you receive the following error message: "Key does not exist"</span></span> 

<span data-ttu-id="b094f-1029">ドメインで gMSA パスワードを初めて作成し生成する場合は、最初にキー配分サービス KDS ルート キーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b094f-1029">If you're creating and generating gMSA passwords in your domain for the first time, you must first create the Key Distribution Services KDS Root Key.</span></span> <span data-ttu-id="b094f-1030">詳細については、[キー配分サービス KDS ルート キーの作成](/windows-server/security/group-managed-service-accounts/create-the-key-distribution-services-kds-root-key)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b094f-1030">For more information, see [Create the Key Distribution Services KDS Root Key](/windows-server/security/group-managed-service-accounts/create-the-key-distribution-services-kds-root-key).</span></span>

### <a name="when-you-run-the-remoting-script-configure-prereqs-allvms-cmdlet-you-receive-the-following-error-message-the-winrm-client-cannot-process-the-request"></a><span data-ttu-id="b094f-1031">リモート処理スクリプト Configure-Prereqs-AllVms cmdlet を実行すると、次のエラー メッセージが表示されます: 「WinRM クライアントは要求を処理できません」</span><span class="sxs-lookup"><span data-stu-id="b094f-1031">When you run the remoting script Configure-Prereqs-AllVms cmdlet, you receive the following error message: "The WinRM client cannot process the request"</span></span>

<span data-ttu-id="b094f-1032">Service Fabric Cluster のすべてのコンピューターで **新しい資格情報委任を許可する** コンピューター ポリシーを有効にするには、エラー メッセージの指示に従います。</span><span class="sxs-lookup"><span data-stu-id="b094f-1032">Follow the instructions in the error message to enable the **Allow delegation fresh credentials** computer policy on all machines of the Service Fabric cluster.</span></span>

### <a name="when-you-configure-prereqs-on-servers-of-the-mrtype-and-reportservertype-types-you-receive-the-following-error-message-install-windowsfeature-the-request-to-add-or-remove-features-on-the-specified-server-failed"></a><span data-ttu-id="b094f-1033">MRType および ReportServerType タイプのサーバーで Configure-Prereqs を実行すると次のエラー メッセージが表示されます:「Install-WindowsFeature: 指定されたサーバーへの機能の追加または削除の要求に失敗しました」</span><span class="sxs-lookup"><span data-stu-id="b094f-1033">When you Configure-Prereqs on servers of the MRType and ReportServerType types, you receive the following error message: "Install-WindowsFeature: The request to add or remove features on the specified server failed"</span></span> 

<span data-ttu-id="b094f-1034">.NET Framework version 3.5 は、**MRType** および **ReportServerType** タイプのサーバーでは必須です。</span><span class="sxs-lookup"><span data-stu-id="b094f-1034">The .NET Framework version 3.5 is required on servers of the **MRType** and **ReportServerType** types.</span></span> <span data-ttu-id="b094f-1035">ただし、既定では .NET Framework version 3.5 のソース ファイルは Windows Server 2016 インストールに含まれていません。</span><span class="sxs-lookup"><span data-stu-id="b094f-1035">However, by default, source files for the .NET Framework version 3.5 aren't included in Windows Server 2016 installations.</span></span> <span data-ttu-id="b094f-1036">このエラーを回避するには、.NET Framework Version 3.5 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="b094f-1036">To work around the error, install the .NET Framework version 3.5.</span></span> <span data-ttu-id="b094f-1037">サーバー マネージャーを使用して新機能を手動で追加する場合、**ソース** オプションを使用してソース ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1037">When you use Server Manager to manually add new features, specify the source files by using the **source** option.</span></span>

### <a name="when-you-run-the-publish-adfsapplicationgroup-cmdlet-you-receive-the-following-error-message-msis7628-scope-names-should-be-a-valid-scope-description-name-in-ad-fs-configuration"></a><span data-ttu-id="b094f-1038">Publish-ADFSApplicationGroup cmdlet を実行すると次のエラー メッセージが表示されます:「MSIS7628: スコープ名は AD FS コンフィギュレーションで有効なスコープ説明でなければなりません」</span><span class="sxs-lookup"><span data-stu-id="b094f-1038">When you run the Publish-ADFSApplicationGroup cmdlet, you receive the following error message: "MSIS7628: Scope names should be a valid Scope description name in AD FS configuration"</span></span>

<span data-ttu-id="b094f-1039">このエラーは、D365FO-OP-ADFSApplicationGroup が必要とする OpenID **allatclaims** スコープが、一部の Windows Server 2016 インストールでは表示されないために発生します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1039">This error occurs because an OpenID **allatclaims** scope that D365FO-OP-ADFSApplicationGroup requires might be missing in some Windows Server 2016 installations.</span></span> <span data-ttu-id="b094f-1040">エラーを回避するには、サーバー マネージャーを開き、**ツール** /> **AD FS の管理** /> **サービス** /> **スコープの説明** の順に移動し、**allatclaims** スコープの説明を追加します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1040">To work around the error, open Server Manager, go to **Tools** /> **AD FS Management** /> **Service** /> **Scope Descriptions**, and add the **allatclaims** scope description.</span></span>

### <a name="when-you-run-the-publish-adfsapplicationgroup-cmdlet-you-receive-the-following-error-message-admin0077-access-control-policy-does-not-exist-permit-everyone"></a><span data-ttu-id="b094f-1041">Publish-ADFSApplicationGroup cmdlet を実行すると次のエラー メッセージが表示されます:「ADMIN0077: アクセス制御ポリシーが存在しません: すべてのユーザーを許可してください」</span><span class="sxs-lookup"><span data-stu-id="b094f-1041">When you run the Publish-ADFSApplicationGroup cmdlet, you receive the following error message: "ADMIN0077: Access control policy does not exist: Permit everyone"</span></span>

<span data-ttu-id="b094f-1042">英語以外のバージョンの Windows Server 2016 と共に AD FS をインストールすると、**すべてのユーザーを許可する** アクセス許可ポリシーがローカル言語で作成されます。</span><span class="sxs-lookup"><span data-stu-id="b094f-1042">If AD FS is installed with a non-English version of Windows Server 2016, the **Permit everyone** access control policy is created in the local language.</span></span> <span data-ttu-id="b094f-1043">次の方法で cmdlet を呼び出して **AccessControlPolicyName** パラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="b094f-1043">Invoke the cmdlet in the following way to specify the **AccessControlPolicyName** parameter.</span></span>

```powershell
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com' -AccessControlPolicyName '<Permit everyone access control policy in your language>'
```

## <a name="additional-resources"></a><span data-ttu-id="b094f-1044">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b094f-1044">Additional resources</span></span>

- [<span data-ttu-id="b094f-1045">オンプレミス配置への更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="b094f-1045">Apply updates to on-premises deployments</span></span>](apply-updates-on-premises.md)
- [<span data-ttu-id="b094f-1046">オンプレミス環境の再配置</span><span class="sxs-lookup"><span data-stu-id="b094f-1046">Redeploy on-premises environments</span></span>](redeploy-on-prem.md)
- [<span data-ttu-id="b094f-1047">ドキュメント管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b094f-1047">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
- [<span data-ttu-id="b094f-1048">電子申告 (ER) コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="b094f-1048">Import Electronic reporting (ER) configurations</span></span>](../analytics/electronic-reporting-import-ger-configurations.md)
- [<span data-ttu-id="b094f-1049">オンプレミス配置でのドキュメントの生成、発行、印刷</span><span class="sxs-lookup"><span data-stu-id="b094f-1049">Document generation, publishing, and printing in on-premises deployments</span></span>](../analytics/printing-capabilities-on-premises.md)
- [<span data-ttu-id="b094f-1050">オンプレミス環境用プロキシの構成</span><span class="sxs-lookup"><span data-stu-id="b094f-1050">Configure proxies for on-premises environments</span></span>](onprem-reverseproxy.md)
- [<span data-ttu-id="b094f-1051">Finance and Operations アプリのテクニカル サポートの設定</span><span class="sxs-lookup"><span data-stu-id="b094f-1051">Set up technical support for Finance and Operations apps</span></span>](../lifecycle-services/support-experience.md)
- [<span data-ttu-id="b094f-1052">クライアント インターネット接続</span><span class="sxs-lookup"><span data-stu-id="b094f-1052">Client internet connectivity</span></span>](../user-interface/client-disconnected.md)