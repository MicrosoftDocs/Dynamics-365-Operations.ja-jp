---
title: "オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 8 および 11)"
description: "このトピックでは、オンプレミス環境の計画、設定、および展開方法について説明します。"
author: sarvanisathish
manager: AnnBe
ms.date: 03/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3e29c8d68784bd1760bf2c94c7a906797ad4fa3c
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-and-deploy-on-premises-environments-platform-updates-8-and-11"></a><span data-ttu-id="7f24a-103">オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 8 および 11)</span><span class="sxs-lookup"><span data-stu-id="7f24a-103">Set up and deploy on-premises environments (Platform updates 8 and 11)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f24a-104">このトピックでは、展開を計画し、インフラストラクチャを設定し、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (オンプレミス)、プラットフォーム更新プログラム 8 および 11 を展開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-104">This topic describes how to plan your deployment, set up the infrastructure, and deploy Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises), Platform updates 8 and 11.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f24a-105">このトピックは、プラットフォーム更新プログラム 8 および 11 にオンプレミス環境を展開する場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-105">This topic applies only to deploying on-premises environments on Platform updates 8 and 11.</span></span> <span data-ttu-id="7f24a-106">プラットフォーム更新プログラム 12 への配置方法の詳細については、[オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12)](setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-106">For information about deploying to Platform update 12, see [Set up and deploy on premises environments (Platform update 12](setup-deploy-on-premises-pu12.md).</span></span>

## <a name="finance-and-operations-components"></a><span data-ttu-id="7f24a-107">Finance and Operations のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="7f24a-107">Finance and Operations components</span></span>

<span data-ttu-id="7f24a-108">Finance and Operations アプリケーションは、次の 3 つの主要なコンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="7f24a-108">The Finance and Operations application consists of three main components:</span></span>

- <span data-ttu-id="7f24a-109">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="7f24a-109">Application Object Server (AOS)</span></span>
- <span data-ttu-id="7f24a-110">ビジネス インテリジェンス (BI)</span><span class="sxs-lookup"><span data-stu-id="7f24a-110">Business Intelligence (BI)</span></span>
- <span data-ttu-id="7f24a-111">財務レポート/管理レポーター</span><span class="sxs-lookup"><span data-stu-id="7f24a-111">Financial Reporting/Management Reporter</span></span>

<span data-ttu-id="7f24a-112">これらのコンポーネントは、次のシステム ソフトウェアによって異なります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-112">These components depend on the following system software:</span></span>

- <span data-ttu-id="7f24a-113">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7f24a-113">Microsoft Windows Server 2016</span></span>
- <span data-ttu-id="7f24a-114">以下の特徴を有する Microsoft SQL Server 2016 SP1:</span><span class="sxs-lookup"><span data-stu-id="7f24a-114">Microsoft SQL Server 2016 SP1, which has the following features:</span></span>
  - <span data-ttu-id="7f24a-115">フルテキスト インデックス検索が有効にされている。</span><span class="sxs-lookup"><span data-stu-id="7f24a-115">Full-text index search is enabled.</span></span>
  - <span data-ttu-id="7f24a-116">SQL Server Reporting Services (SSRS) - これは BI 仮想マシンに配置されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-116">SQL Server Reporting Services (SSRS) - This is deployed on BI virtual machines.</span></span>
  - <span data-ttu-id="7f24a-117">SQL Server Integration Services (SSIS) - これは AOS 仮想マシンに配置されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-117">SQL Server Integration Services (SSIS) - This is deployed on AOS virtual machines.</span></span>

    > [!WARNING]
    > <span data-ttu-id="7f24a-118">完全なテキスト検索を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-118">Full Text Search must be enabled.</span></span>

- <span data-ttu-id="7f24a-119">SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="7f24a-119">SQL Server Management Studio</span></span>
- <span data-ttu-id="7f24a-120">Standalone Microsoft Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7f24a-120">Standalone Microsoft Azure Service Fabric</span></span>
- <span data-ttu-id="7f24a-121">Microsoft Windows PowerShell 5.0 以降</span><span class="sxs-lookup"><span data-stu-id="7f24a-121">Microsoft Windows PowerShell 5.0 or later</span></span>
- <span data-ttu-id="7f24a-122">Windows Server 2016 での Active Directory Federation Services (AD FS)</span><span class="sxs-lookup"><span data-stu-id="7f24a-122">Active Directory Federation Services (AD FS) on Windows Server 2016</span></span>
- <span data-ttu-id="7f24a-123">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="7f24a-123">Domain controller</span></span>

  > [!WARNING]
  > <span data-ttu-id="7f24a-124">ドメイン コントローラは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-124">The domain controller must be Microsoft Windows Server 2012 R2 or later and must have a domain functional level of 2012 R2 or more.</span></span>    <span data-ttu-id="7f24a-125">ドメイン機能レベルの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-125">For more information about domain functional levels, see the following topics:</span></span>
  >   - <span data-ttu-id="7f24a-126">[Active Directory 機能レベルとは](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="7f24a-126">[What Are Active Directory Functional Levels](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)</span></span>
  >   - <span data-ttu-id="7f24a-127">[Active Directory ドメイン サービス機能のレベルを理解する](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="7f24a-127">[Understanding Active Directory Domain Services Functional Levels](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="7f24a-128">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="7f24a-128">Lifecycle Services</span></span>

<span data-ttu-id="7f24a-129">Finance and Operations のビットは、Microsoft Dynamics Lifecycle Services (LCS) を通じて配布されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-129">Finance and Operations bits are distributed through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="7f24a-130">配置する前に、[エンタープライズ契約](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) チャンネルを通じてライセンス キーを購入し、LCS でオンプレミス プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-130">Before you can deploy, you must purchase license keys through the [Enterprise Agreements](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) channel and set up an on-premises project in LCS.</span></span> <span data-ttu-id="7f24a-131">LCS からのみ配置を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-131">Deployments can be initiated only through LCS.</span></span> <span data-ttu-id="7f24a-132">LCS でオンプレミス プロジェクトを設定する方法の詳細については、[Lifecycle Services でのオンプレミス プロジェクトの作成](../lifecycle-services/lbd-create-lcs-on-prem-project.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-132">For more information about how to set up on-premises projects in LCS, see [Create an on-premises project in Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).</span></span>

## <a name="authentication"></a><span data-ttu-id="7f24a-133">認証</span><span class="sxs-lookup"><span data-stu-id="7f24a-133">Authentication</span></span>

<span data-ttu-id="7f24a-134">オンプレミス アプリケーションは AD FS で動作します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-134">The on-premises application works with AD FS.</span></span> <span data-ttu-id="7f24a-135">LCS と対話するには、Azure Active Directory (AAD) も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-135">To interact with LCS, you must also configure Azure Active Directory (AAD).</span></span> <span data-ttu-id="7f24a-136">配置を完了し LCS ローカル エージェントを構成するには、AAD が必要です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-136">And, to complete the deployment and configure the LCS Local agent, you will need AAD.</span></span>

## <a name="standalone-service-fabric"></a><span data-ttu-id="7f24a-137">Standalone Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7f24a-137">Standalone Service Fabric</span></span>

<span data-ttu-id="7f24a-138">Finance and Operations は スタンドアロン Service Fabric を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-138">Finance and Operations uses standalone Service Fabric.</span></span> <span data-ttu-id="7f24a-139">詳細については、[Service Fabric ドキュメント](/azure/service-fabric/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-139">For more information, see the [Service Fabric documentation](/azure/service-fabric/).</span></span>

<span data-ttu-id="7f24a-140">Finance and Operations の設定は、Service Fabric (SF) 内に一連のアプリケーションを配置します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-140">Setup of Finance and Operations will deploy a set of applications inside Service Fabric (SF).</span></span> <span data-ttu-id="7f24a-141">展開中に、クラスター内の各ノードは、次のいずれかのノード タイプを持つように構成によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-141">During deployment, each node in the cluster will be defined via configuration to have one of the following node types:</span></span>

- <span data-ttu-id="7f24a-142">**AOSNodeType**: アプリケーション オブジェクト サーバー (ビジネス ロジック) をホストします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-142">**AOSNodeType**: Hosts the application object server (business logic).</span></span>
- <span data-ttu-id="7f24a-143">**OrchestratorType**: Service Fabric のプライマリ ノードとして機能し、配置およびサービスロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-143">**OrchestratorType**: Functions as Service Fabric primary nodes, and hosts deployment- and servicing logic.</span></span>
- <span data-ttu-id="7f24a-144">**ReportServerType**: SSRS およびレポート ロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-144">**ReportServerType**: Hosts SSRS and reporting logic.</span></span>
- <span data-ttu-id="7f24a-145">**MRType**: 管理レポート ロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-145">**MRType**: Hosts management reporting logic.</span></span>

## <a name="infrastructure"></a><span data-ttu-id="7f24a-146">インフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="7f24a-146">Infrastructure</span></span>

<span data-ttu-id="7f24a-147">Finance and Operations は、Windows Servers に基づく Hyper-V 仮想化環境で作業するよう設計されています。</span><span class="sxs-lookup"><span data-stu-id="7f24a-147">Finance and Operations is designed to work on a Hyper-V virtualized environment that is based on Windows Servers.</span></span>

 > [!WARNING]
 > <span data-ttu-id="7f24a-148">Azure を含む、任意のパブリック クラウド インフラストラクチャでサポートされていない、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置。</span><span class="sxs-lookup"><span data-stu-id="7f24a-148">On-premises deployments of Microsoft Dynamics 365 for Finance and Operations are not supported on any public cloud infrastructure, including Azure.</span></span>

<span data-ttu-id="7f24a-149">ハードウェア構成には、次のコンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-149">The hardware configuration includes the following components:</span></span>

- <span data-ttu-id="7f24a-150">Windows Server 2016 仮想マシン (VM) に基づく Standalone Service Fabric クラスター</span><span class="sxs-lookup"><span data-stu-id="7f24a-150">Standalone Service Fabric cluster that is based on Windows Server 2016 virtual machines (VMs)</span></span>
- <span data-ttu-id="7f24a-151">Microsoft SQL Server (Clustered SQL と Always-On の両方がサポートされています)</span><span class="sxs-lookup"><span data-stu-id="7f24a-151">Microsoft SQL Server (both Clustered SQL and Always-On are supported)</span></span>
- <span data-ttu-id="7f24a-152">認証のための AD FS</span><span class="sxs-lookup"><span data-stu-id="7f24a-152">AD FS for authentication</span></span>
- <span data-ttu-id="7f24a-153">ストレージ用の Server Message Block (SMB) バージョン 3 のファイル共有</span><span class="sxs-lookup"><span data-stu-id="7f24a-153">Server Message Block (SMB) version 3 file share for storage</span></span>
- <span data-ttu-id="7f24a-154">オプション: Microsoft Office Server 2017</span><span class="sxs-lookup"><span data-stu-id="7f24a-154">Optional: Microsoft Office Server 2017</span></span>

<span data-ttu-id="7f24a-155">詳細については、[システム要求](../../fin-and-ops/get-started/system-requirements-on-prem.md) およびサイジングのガイドラインを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-155">For more information, see [System requirements](../../fin-and-ops/get-started/system-requirements-on-prem.md) and Sizing guidelines.</span></span>

### <a name="hardware-layout"></a><span data-ttu-id="7f24a-156">ハードウェア レイアウト</span><span class="sxs-lookup"><span data-stu-id="7f24a-156">Hardware layout</span></span>

<span data-ttu-id="7f24a-157">[オンプレミス環境のハードウェア サイジング](../../fin-and-ops/get-started/hardware-sizing-on-premises-environments.md) で推奨されるサイジングに基づいて、インフラストラクチャと Service Fabric クラスターを計画します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-157">Plan your infrastructure and Service Fabric cluster based on the recommended sizing in [Hardware sizing for on-premises environments](../../fin-and-ops/get-started/hardware-sizing-on-premises-environments.md).</span></span> <span data-ttu-id="7f24a-158">Service Fabric クラスターを計画する方法の詳細については、[Service Fabric のスタンドアロン クラスター展開の計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-158">For more information about how to plan the Service Fabric cluster, see [Plan and prepare your Service Fabric standalone cluster deployment](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

<span data-ttu-id="7f24a-159">次のテーブルは、ハードウェア レイアウトの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7f24a-159">The following table shows an example of a hardware layout.</span></span> <span data-ttu-id="7f24a-160">この例は、設定を説明するためにこのトピック全体で使用されています。</span><span class="sxs-lookup"><span data-stu-id="7f24a-160">This example is used throughout this topic to illustrate the setup.</span></span>

> [!NOTE]
> <span data-ttu-id="7f24a-161">Service Fabric クラスターのプライマリ ノードには、少なくとも 3 つのノードが必要です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-161">The Primary node of the Service Fabric cluster must have at least three nodes.</span></span> <span data-ttu-id="7f24a-162">この例では **OrchestratorType** を主要なノード タイプとして指定します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-162">In this example, **OrchestratorType** is designated as the Primary node type.</span></span>

| <span data-ttu-id="7f24a-163">マシンの目的</span><span class="sxs-lookup"><span data-stu-id="7f24a-163">Machine purpose</span></span>          | <span data-ttu-id="7f24a-164">SF ノード タイプ</span><span class="sxs-lookup"><span data-stu-id="7f24a-164">SF Node type</span></span>     | <span data-ttu-id="7f24a-165">コンピューター名</span><span class="sxs-lookup"><span data-stu-id="7f24a-165">Machine name</span></span>    | <span data-ttu-id="7f24a-166">IP アドレス</span><span class="sxs-lookup"><span data-stu-id="7f24a-166">IP address</span></span>    |
|--------------------------|------------------|-----------------|---------------|
| <span data-ttu-id="7f24a-167">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="7f24a-167">Domain controller</span></span>        |                  | <span data-ttu-id="7f24a-168">DAX7SQLAODC1</span><span class="sxs-lookup"><span data-stu-id="7f24a-168">DAX7SQLAODC1</span></span>    | <span data-ttu-id="7f24a-169">10.179.108.2</span><span class="sxs-lookup"><span data-stu-id="7f24a-169">10.179.108.2</span></span>  |
| <span data-ttu-id="7f24a-170">AD FS</span><span class="sxs-lookup"><span data-stu-id="7f24a-170">AD FS</span></span>                    |                  | <span data-ttu-id="7f24a-171">DAX7SQLAOADFS1</span><span class="sxs-lookup"><span data-stu-id="7f24a-171">DAX7SQLAOADFS1</span></span>  | <span data-ttu-id="7f24a-172">10.179.108.3</span><span class="sxs-lookup"><span data-stu-id="7f24a-172">10.179.108.3</span></span>  |
| <span data-ttu-id="7f24a-173">ファイル サーバー</span><span class="sxs-lookup"><span data-stu-id="7f24a-173">File server</span></span>              |                  | <span data-ttu-id="7f24a-174">DAX7SQLAOFILE1</span><span class="sxs-lookup"><span data-stu-id="7f24a-174">DAX7SQLAOFILE1</span></span>  | <span data-ttu-id="7f24a-175">10.179.108.4</span><span class="sxs-lookup"><span data-stu-id="7f24a-175">10.179.108.4</span></span>  |
| <span data-ttu-id="7f24a-176">SQL Always-On クラスター</span><span class="sxs-lookup"><span data-stu-id="7f24a-176">SQL Always-On cluster</span></span>    |                  | <span data-ttu-id="7f24a-177">DAX7SQLAOSQLA01</span><span class="sxs-lookup"><span data-stu-id="7f24a-177">DAX7SQLAOSQLA01</span></span> | <span data-ttu-id="7f24a-178">10.179.108.5</span><span class="sxs-lookup"><span data-stu-id="7f24a-178">10.179.108.5</span></span>  |
|                          |                  | <span data-ttu-id="7f24a-179">DAX7SQLAOSQLA02</span><span class="sxs-lookup"><span data-stu-id="7f24a-179">DAX7SQLAOSQLA02</span></span> | <span data-ttu-id="7f24a-180">10.179.108.6</span><span class="sxs-lookup"><span data-stu-id="7f24a-180">10.179.108.6</span></span>  |
|                          |                  | <span data-ttu-id="7f24a-181">DAX7SQLAOSQLA</span><span class="sxs-lookup"><span data-stu-id="7f24a-181">DAX7SQLAOSQLA</span></span>   | <span data-ttu-id="7f24a-182">10.179.108.9</span><span class="sxs-lookup"><span data-stu-id="7f24a-182">10.179.108.9</span></span>  |
| <span data-ttu-id="7f24a-183">クライアント</span><span class="sxs-lookup"><span data-stu-id="7f24a-183">Client</span></span>                   |                  | <span data-ttu-id="7f24a-184">SQLAOCLIENT1</span><span class="sxs-lookup"><span data-stu-id="7f24a-184">SQLAOCLIENT1</span></span>    | <span data-ttu-id="7f24a-185">10.179.108.11</span><span class="sxs-lookup"><span data-stu-id="7f24a-185">10.179.108.11</span></span> |
| <span data-ttu-id="7f24a-186">AOS 1</span><span class="sxs-lookup"><span data-stu-id="7f24a-186">AOS 1</span></span>                    | <span data-ttu-id="7f24a-187">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="7f24a-187">AOSNodeType</span></span>      | <span data-ttu-id="7f24a-188">SQLAOSF1AOS1</span><span class="sxs-lookup"><span data-stu-id="7f24a-188">SQLAOSF1AOS1</span></span>    | <span data-ttu-id="7f24a-189">10.179.108.12</span><span class="sxs-lookup"><span data-stu-id="7f24a-189">10.179.108.12</span></span> |
| <span data-ttu-id="7f24a-190">AOS 2</span><span class="sxs-lookup"><span data-stu-id="7f24a-190">AOS 2</span></span>                    | <span data-ttu-id="7f24a-191">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="7f24a-191">AOSNodeType</span></span>      | <span data-ttu-id="7f24a-192">SQLAOSF1AOS2</span><span class="sxs-lookup"><span data-stu-id="7f24a-192">SQLAOSF1AOS2</span></span>    | <span data-ttu-id="7f24a-193">10.179.108.13</span><span class="sxs-lookup"><span data-stu-id="7f24a-193">10.179.108.13</span></span> |
| <span data-ttu-id="7f24a-194">AOS 3</span><span class="sxs-lookup"><span data-stu-id="7f24a-194">AOS 3</span></span>                    | <span data-ttu-id="7f24a-195">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="7f24a-195">AOSNodeType</span></span>      | <span data-ttu-id="7f24a-196">SQLAOSF1AOS3</span><span class="sxs-lookup"><span data-stu-id="7f24a-196">SQLAOSF1AOS3</span></span>    | <span data-ttu-id="7f24a-197">10.179.108.14</span><span class="sxs-lookup"><span data-stu-id="7f24a-197">10.179.108.14</span></span> |
| <span data-ttu-id="7f24a-198">オーケストレータ 1</span><span class="sxs-lookup"><span data-stu-id="7f24a-198">Orchestrator 1</span></span>           | <span data-ttu-id="7f24a-199">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="7f24a-199">OrchestratorType</span></span> | <span data-ttu-id="7f24a-200">SQLAOSF1ORCH1</span><span class="sxs-lookup"><span data-stu-id="7f24a-200">SQLAOSF1ORCH1</span></span>   | <span data-ttu-id="7f24a-201">10.179.108.15</span><span class="sxs-lookup"><span data-stu-id="7f24a-201">10.179.108.15</span></span> |
| <span data-ttu-id="7f24a-202">オーケストレータ 2</span><span class="sxs-lookup"><span data-stu-id="7f24a-202">Orchestrator 2</span></span>           | <span data-ttu-id="7f24a-203">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="7f24a-203">OrchestratorType</span></span> | <span data-ttu-id="7f24a-204">SQLAOSF1ORCH2</span><span class="sxs-lookup"><span data-stu-id="7f24a-204">SQLAOSF1ORCH2</span></span>   | <span data-ttu-id="7f24a-205">10.179.108.16</span><span class="sxs-lookup"><span data-stu-id="7f24a-205">10.179.108.16</span></span> |
| <span data-ttu-id="7f24a-206">オーケストレータ 3</span><span class="sxs-lookup"><span data-stu-id="7f24a-206">Orchestrator 3</span></span>           | <span data-ttu-id="7f24a-207">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="7f24a-207">OrchestratorType</span></span> | <span data-ttu-id="7f24a-208">SQLAOSF1ORCH3</span><span class="sxs-lookup"><span data-stu-id="7f24a-208">SQLAOSF1ORCH3</span></span>   | <span data-ttu-id="7f24a-209">10.179.108.17</span><span class="sxs-lookup"><span data-stu-id="7f24a-209">10.179.108.17</span></span> |
| <span data-ttu-id="7f24a-210">Management Reporter ノード</span><span class="sxs-lookup"><span data-stu-id="7f24a-210">Management Reporter node</span></span> | <span data-ttu-id="7f24a-211">MRType</span><span class="sxs-lookup"><span data-stu-id="7f24a-211">MRType</span></span>           | <span data-ttu-id="7f24a-212">SQLAOSMR1</span><span class="sxs-lookup"><span data-stu-id="7f24a-212">SQLAOSMR1</span></span>       | <span data-ttu-id="7f24a-213">10.179.108.18</span><span class="sxs-lookup"><span data-stu-id="7f24a-213">10.179.108.18</span></span> |
| <span data-ttu-id="7f24a-214">SSRS ノード</span><span class="sxs-lookup"><span data-stu-id="7f24a-214">SSRS node</span></span>                | <span data-ttu-id="7f24a-215">ReportServerType</span><span class="sxs-lookup"><span data-stu-id="7f24a-215">ReportServerType</span></span> | <span data-ttu-id="7f24a-216">SQLAOSFBIN1</span><span class="sxs-lookup"><span data-stu-id="7f24a-216">SQLAOSFBIN1</span></span>     | <span data-ttu-id="7f24a-217">10.179.108.10</span><span class="sxs-lookup"><span data-stu-id="7f24a-217">10.179.108.10</span></span> |

## <a name="setup"></a><span data-ttu-id="7f24a-218">段取り</span><span class="sxs-lookup"><span data-stu-id="7f24a-218">Setup</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7f24a-219">前提条件</span><span class="sxs-lookup"><span data-stu-id="7f24a-219">Prerequisites</span></span>

<span data-ttu-id="7f24a-220">セットアップを開始する前に、次の前提条件が満たされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-220">Before you start the setup, the following prerequisites must be in place.</span></span> <span data-ttu-id="7f24a-221">これらの前提条件の設定は、このドキュメントの範囲外です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-221">The setup of these prerequisites is out of scope for this document.</span></span>

- <span data-ttu-id="7f24a-222">Active Directory Domain Services (AD DS) は、ネットワークにインストールして構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-222">Active Directory Domain Services (AD DS) must be installed and configured in your network.</span></span>
- <span data-ttu-id="7f24a-223">AD FS は、展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-223">AD FS must be deployed.</span></span>
- <span data-ttu-id="7f24a-224">SQL Server 2016 SP1 は SSRS コンピューターにインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-224">SQL Server 2016 SP1 must be installed on the SSRS machines.</span></span>
- <span data-ttu-id="7f24a-225">SQL Server Reporting Services 2016 は、SSRS コンピューターに**ネイティブ** モードでインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-225">SQL Server Reporting Services 2016 must be installed in **Native** mode on the SSRS machines.</span></span>

<span data-ttu-id="7f24a-226">次の必須ソフトウェアは、LCS からダウンロードされたインフラストラクチャ セットアップ スクリプトによって VM にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-226">The following prerequisite software is installed on the VMs by the infrastructure setup scripts downloaded from LCS.</span></span>

| <span data-ttu-id="7f24a-227">ノード タイプ</span><span class="sxs-lookup"><span data-stu-id="7f24a-227">Node type</span></span> | <span data-ttu-id="7f24a-228">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="7f24a-228">Component</span></span> | <span data-ttu-id="7f24a-229">細目</span><span class="sxs-lookup"><span data-stu-id="7f24a-229">Details</span></span> |
|-----------|-----------|---------|
| <span data-ttu-id="7f24a-230">AOS</span><span class="sxs-lookup"><span data-stu-id="7f24a-230">AOS</span></span>       | <span data-ttu-id="7f24a-231">SNAC – ODBC ドライバー</span><span class="sxs-lookup"><span data-stu-id="7f24a-231">SNAC – ODBC driver</span></span> | <https://www.microsoft.com/en-us/download/details.aspx?id=53339> |
| <span data-ttu-id="7f24a-232">AOS</span><span class="sxs-lookup"><span data-stu-id="7f24a-232">AOS</span></span>       | <span data-ttu-id="7f24a-233">Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="7f24a-233">The Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="7f24a-234">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="7f24a-234">**Windows Features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="7f24a-235">AOS</span><span class="sxs-lookup"><span data-stu-id="7f24a-235">AOS</span></span>       | <span data-ttu-id="7f24a-236">Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="7f24a-236">The Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="7f24a-237">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="7f24a-237">**Windows Features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="7f24a-238">AOS</span><span class="sxs-lookup"><span data-stu-id="7f24a-238">AOS</span></span>       | <span data-ttu-id="7f24a-239">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="7f24a-239">Internet Information Services (IIS)</span></span> | <span data-ttu-id="7f24a-240">**Windows の機能:** WAS、WAS-Process-Model、WAS-NET-Environment、WAS-Config-APIs、Web-Server、Web-WebServer、Web-Security、Web-Filtering、Web-App-Dev、Web-Net-Ext、Web-Mgmt-Tools、Web-Mgmt-Console</span><span class="sxs-lookup"><span data-stu-id="7f24a-240">**Windows Features:** WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs, Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console</span></span> |
| <span data-ttu-id="7f24a-241">AOS</span><span class="sxs-lookup"><span data-stu-id="7f24a-241">AOS</span></span>       | <span data-ttu-id="7f24a-242">SQL Server Management Studio 17.2</span><span class="sxs-lookup"><span data-stu-id="7f24a-242">SQL Server Management Studio 17.2</span></span> | <https://go.microsoft.com/fwlink/?linkid=854085> |
| <span data-ttu-id="7f24a-243">AOS</span><span class="sxs-lookup"><span data-stu-id="7f24a-243">AOS</span></span>       | <span data-ttu-id="7f24a-244">Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="7f24a-244">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</span></span> | <https://support.microsoft.com/en-us/help/3179560> |
| <span data-ttu-id="7f24a-245">AOS</span><span class="sxs-lookup"><span data-stu-id="7f24a-245">AOS</span></span>       | <span data-ttu-id="7f24a-246">Microsoft Access データベース エンジン 2010 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="7f24a-246">Microsoft Access Database Engine 2010 Redistributable</span></span> | <https://www.microsoft.com/en-us/download/details.aspx?id=13255> |
| <span data-ttu-id="7f24a-247">BI</span><span class="sxs-lookup"><span data-stu-id="7f24a-247">BI</span></span>        | <span data-ttu-id="7f24a-248">.NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="7f24a-248">.NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="7f24a-249">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="7f24a-249">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="7f24a-250">BI</span><span class="sxs-lookup"><span data-stu-id="7f24a-250">BI</span></span>        | <span data-ttu-id="7f24a-251">.NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="7f24a-251">.NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="7f24a-252">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="7f24a-252">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="7f24a-253">BI</span><span class="sxs-lookup"><span data-stu-id="7f24a-253">BI</span></span>        | <span data-ttu-id="7f24a-254">SQL Server Management Studio 17.2</span><span class="sxs-lookup"><span data-stu-id="7f24a-254">SQL Server Management Studio 17.2</span></span> | <https://go.microsoft.com/fwlink/?linkid=854085> |
| <span data-ttu-id="7f24a-255">MR</span><span class="sxs-lookup"><span data-stu-id="7f24a-255">MR</span></span>        | <span data-ttu-id="7f24a-256">.NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="7f24a-256">.NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="7f24a-257">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="7f24a-257">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="7f24a-258">MR</span><span class="sxs-lookup"><span data-stu-id="7f24a-258">MR</span></span>        | <span data-ttu-id="7f24a-259">.NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="7f24a-259">.NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="7f24a-260">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="7f24a-260">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="7f24a-261">MR</span><span class="sxs-lookup"><span data-stu-id="7f24a-261">MR</span></span>        | <span data-ttu-id="7f24a-262">Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="7f24a-262">Visual C++ Redistributable Packages for Visual Studio 2013</span></span> | <https://support.microsoft.com/en-us/help/3179560> |

### <a name="overview"></a><span data-ttu-id="7f24a-263">概要</span><span class="sxs-lookup"><span data-stu-id="7f24a-263">Overview</span></span>

<span data-ttu-id="7f24a-264">Finance and Operations のインフラストラクチャを設定するには、以下の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-264">The following steps must be completed to set up the infrastructure for Finance and Operations.</span></span>

1. [<span data-ttu-id="7f24a-265">ドメイン名と DNS ゾーンの計画</span><span class="sxs-lookup"><span data-stu-id="7f24a-265">Plan your domain name and DNS zones</span></span>](#plandomain)
2. [<span data-ttu-id="7f24a-266">証明書の計画と取得</span><span class="sxs-lookup"><span data-stu-id="7f24a-266">Plan and acquire your certificates</span></span>](#plancert)
3. [<span data-ttu-id="7f24a-267">ユーザーとサービス アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="7f24a-267">Plan your users and service accounts</span></span>](#plansvcacct)
4. [<span data-ttu-id="7f24a-268">DNS ゾーンの作成と A レコードの追加</span><span class="sxs-lookup"><span data-stu-id="7f24a-268">Create DNS zones, and add A records</span></span>](#createdns)
5. [<span data-ttu-id="7f24a-269">VM のドメインへの参加</span><span class="sxs-lookup"><span data-stu-id="7f24a-269">Join VMs to the domain</span></span>](#joindomain)
6. [<span data-ttu-id="7f24a-270">LCS からセットアップ スクリプトのダウンロード</span><span class="sxs-lookup"><span data-stu-id="7f24a-270">Download setup scripts from LCS</span></span>](#downloadscripts)
7. [<span data-ttu-id="7f24a-271">コンフィギュレーションの記述</span><span class="sxs-lookup"><span data-stu-id="7f24a-271">Describe your configuration</span></span>](#describeconfig)
8. [<span data-ttu-id="7f24a-272">証明書の構成</span><span class="sxs-lookup"><span data-stu-id="7f24a-272">Configure certificates</span></span>](#configurecert)
9. [<span data-ttu-id="7f24a-273">VM を設定する</span><span class="sxs-lookup"><span data-stu-id="7f24a-273">Setup VMs</span></span>](#setupvms)
10. [<span data-ttu-id="7f24a-274">スタンドアロン Service Fabric クラスターの設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-274">Set up a standalone Service Fabric cluster</span></span>](#setupsfcluster)
11. [<span data-ttu-id="7f24a-275">テナント用 LCS 接続の構成</span><span class="sxs-lookup"><span data-stu-id="7f24a-275">Configure LCS connectivity for the tenant</span></span>](#configurelcs)
12. [<span data-ttu-id="7f24a-276">ファイル ストレージの設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-276">Set up file storage</span></span>](#setupfile)
13. [<span data-ttu-id="7f24a-277">SQL Server の設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-277">Set up SQL Server</span></span>](#setupsql)
14. [<span data-ttu-id="7f24a-278">データベースを構成する</span><span class="sxs-lookup"><span data-stu-id="7f24a-278">Configure the databases</span></span>](#configuredb)
15. [<span data-ttu-id="7f24a-279">資格情報の暗号化</span><span class="sxs-lookup"><span data-stu-id="7f24a-279">Encrypt credentials</span></span>](#encryptcred)
16. [<span data-ttu-id="7f24a-280">資産除去債務 (SSIS) の設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-280">Set up SSIS</span></span>](#setupssis)
17. [<span data-ttu-id="7f24a-281">資産除去債務 (SSRS) の設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-281">Set up SSRS</span></span>](#setupssrs)
18. [<span data-ttu-id="7f24a-282">AD FS のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f24a-282">Configure AD FS</span></span>](#configureadfs)
19. [<span data-ttu-id="7f24a-283">コネクタを構成し、オンプレミスのローカル エージェントをインストールする</span><span class="sxs-lookup"><span data-stu-id="7f24a-283">Configure a connector and install an on-premises local agent</span></span>](#configureconnector)
20. [<span data-ttu-id="7f24a-284">LCS から Finance and Operations (オンプレミス) 環境を配置する</span><span class="sxs-lookup"><span data-stu-id="7f24a-284">Deploy your Finance and Operations (on-premises) environment from LCS</span></span>](#deploy)
21. [<span data-ttu-id="7f24a-285">Finance and Operations (オンプレミス) 環境に接続する</span><span class="sxs-lookup"><span data-stu-id="7f24a-285">Connect to your Finance and Operations (on-premises) environment</span></span>](#connect)

### <a name="plandomain"></a> <span data-ttu-id="7f24a-286">1. ドメイン名と DNS ゾーンの計画</span><span class="sxs-lookup"><span data-stu-id="7f24a-286">1. Plan your domain name and DNS zones</span></span>

<span data-ttu-id="7f24a-287">AOS のプロダクション インストールには、公的に登録されたドメイン名を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-287">We recommend that you use a publicly registered domain name for your production installation of AOS.</span></span> <span data-ttu-id="7f24a-288">このようにして、外部アクセスが必要な場合は、ネットワークの外部からインストールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-288">In that way, the installation can be accessed outside the network, if outside access is required.</span></span>

<span data-ttu-id="7f24a-289">たとえば、会社のドメインが contoso.com の場合、Finance and Operations (オンプレミス) は d365ffo.onprem.contoso.com であり、ホスト名は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-289">For example, if your company's domain is contoso.com, your zone for Finance and Operations (on-premises) might be d365ffo.onprem.contoso.com, and the host names might be as follows:</span></span>

- <span data-ttu-id="7f24a-290">AOS の機械の場合 ax.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7f24a-290">ax.d365ffo.onprem.contoso.com for AOS machines</span></span>
- <span data-ttu-id="7f24a-291">Service Fabric クラスターの場合 sf.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7f24a-291">sf.d365ffo.onprem.contoso.com for the Service Fabric cluster</span></span>

### <a name="plancert"></a> <span data-ttu-id="7f24a-292">2. 証明書の計画と取得</span><span class="sxs-lookup"><span data-stu-id="7f24a-292">2. Plan and acquire your certificates</span></span>

<span data-ttu-id="7f24a-293">Service Fabric クラスターと展開されているすべてのアプリケーションを保護するには、Secure Sockets Layer (SSL) 証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-293">Secure Sockets Layer (SSL) certificates are required in order to secure a Service Fabric cluster and all the applications that are deployed.</span></span> <span data-ttu-id="7f24a-294">プロダクションとサンドボックスのワークロードについては、[DigiCert](https://www.digicert.com/ssl-certificate/)、[Comodo](https://ssl.comodo.com/)、[Symantec](https://www.websecurity.symantec.com/ssl-certificate)、[GoDaddy](https://www.godaddy.com/web-security/ssl-certificate)、または [GlobalSign](https://www.globalsign.com/en/ssl/) などの認証局から証明書を取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-294">For your production and sandbox workloads, we recommend that you acquire certificates from a certificate authority (CA) such as [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate), or [GlobalSign](https://www.globalsign.com/en/ssl/).</span></span> <span data-ttu-id="7f24a-295">ドメインが [Active Directory 証明書サービス](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS) で設定されている場合は、AD CS を介して証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-295">If your domain is set up with [Active Directory Certificate Services](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS), you can create the certificates through AD CS.</span></span> <span data-ttu-id="7f24a-296">証明書ごとに、プライベート キーが作成されたキーの交換を含める必要があり、個人情報交換 (.pfx) ファイルにエクスポート可能な必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-296">Each certificate must contain a private key that was created for key exchange, and it must be exportable to a Personal Information Exchange (.pfx) file.</span></span>

<span data-ttu-id="7f24a-297">自己署名証明書は、テスト目的でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-297">Self-signed certificates can be used only for testing purposes.</span></span> <span data-ttu-id="7f24a-298">便宜上、セットアップ スクリプトには、自己署名証明書を生成およびエクスポートするスクリプトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f24a-298">For convenience, the setup scripts include scripts that generate and export self-signed certificates.</span></span> <span data-ttu-id="7f24a-299">先に述べたように、これらの証明書はテスト目的でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-299">As we've mentioned, these certificates can be used for testing purposes only.</span></span>

| <span data-ttu-id="7f24a-300">目的</span><span class="sxs-lookup"><span data-stu-id="7f24a-300">Purpose</span></span>                                      | <span data-ttu-id="7f24a-301">説明</span><span class="sxs-lookup"><span data-stu-id="7f24a-301">Explanation</span></span> | <span data-ttu-id="7f24a-302">追加条件</span><span class="sxs-lookup"><span data-stu-id="7f24a-302">Additional requirements</span></span> |
|----------------------------------------------|-------------|-------------------------|
| <span data-ttu-id="7f24a-303">SQL Server SSL 証明書</span><span class="sxs-lookup"><span data-stu-id="7f24a-303">SQL Server SSL certificate</span></span>                   | <span data-ttu-id="7f24a-304">この証明書は、ネットワーク上の SQL Server インスタンスとクライアント アプリケーションの間で転送されるデータを暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-304">This certificate is used to encrypt data that is transmitted across a network between an instance of SQL Server and a client application.</span></span> | <span data-ttu-id="7f24a-305">証明書の場合、ドメイン名は、SQL Server のインスタンスまたはリスナーの完全修飾ドメイン名 (FQDN) と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-305">The domain name of the certificate should match the fully-qualified domain name (FQDN) of the SQL Server instance or listener.</span></span> <span data-ttu-id="7f24a-306">たとえば、SQL のリスナーが DAX7SQLAOSQLA のコンピューターにホストされている場合、証明書の DNS 名は、DAX7SQLAOSQLA.onprem.contoso.com です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-306">For example, if the SQL listener is hosted on the machine DAX7SQLAOSQLA, the certificate's DNS name is DAX7SQLAOSQLA.onprem.contoso.com.</span></span> |
| <span data-ttu-id="7f24a-307">Service Fabric Server 証明書</span><span class="sxs-lookup"><span data-stu-id="7f24a-307">Service Fabric Server certificate</span></span>            | <p><span data-ttu-id="7f24a-308">この証明書を使用して、Service Fabric ノード間のノードからノードの通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-308">This certificate is used to help secure the node-to-node communication between the Service Fabric nodes.</span></span></p> <p> <span data-ttu-id="7f24a-309">この証明書は、クラスターに接続するクライアントに提示されるサーバー証明書としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-309">This certificate is also used as the Server certificate that is presented to the client that connects to the cluster.</span></span></p> | <span data-ttu-id="7f24a-310">ドメインの SSL ワイルドカード証明書を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-310">You can use the SSL wild card certificate of your domain.</span></span> <span data-ttu-id="7f24a-311">たとえば、\*. contoso.com。**注記:** ワイルドカード証明書は、発行先となるドメインの最初のレベル サブドメインのみをセキュリティ保護できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-311">For example, \*.contoso.com. **Note:** The wild card certificate allows you to secure only the first level subdomain of the domain to which it is issued.</span></span><p><span data-ttu-id="7f24a-312">この例では、Service Fabric ドメインが sf.d365ffo.onprem.contoso.com であるため、証明書にサブジェクト代替名 (SAN) としてこれを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-312">In this example, because your service fabric domain is sf.d365ffo.onprem.contoso.com, you must include this as a Subject Alternative Name (SAN) in the certificate.</span></span> <span data-ttu-id="7f24a-313">証明機関と連携して、追加の SAN を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-313">You will need to work with your certificate authority to acquire the additional SANs.</span></span></p> |
| <span data-ttu-id="7f24a-314">Service Fabric Client 証明書</span><span class="sxs-lookup"><span data-stu-id="7f24a-314">Service Fabric Client certificate</span></span>            | <span data-ttu-id="7f24a-315">この証明書は、クライアントによって Service Fabric クラスターを表示および管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-315">This certificate is used by clients to view and manage the Service Fabric cluster.</span></span> | |
| <span data-ttu-id="7f24a-316">証明書の暗号化</span><span class="sxs-lookup"><span data-stu-id="7f24a-316">Encipherment Certificate</span></span>                     | <span data-ttu-id="7f24a-317">この証明書は、SQL Server パスワードとユーザー アカウントのパスワードなどの重要な情報を暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-317">This certificate is used to encrypt sensitive information such as the SQL Server password and user account passwords.</span></span>  | <p> <span data-ttu-id="7f24a-318">証明書は、プロバイダー **Microsoft Enhanced Cryptographic Provider v1.0** を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-318">The certificate must be created by using the provider **Microsoft Enhanced Cryptographic Provider v1.0**.</span></span> </p><p><span data-ttu-id="7f24a-319">証明書キーの使用にはデータ暗号化 (10) が含まれている必要があり、サーバー認証またはクライアント認証は含めないでください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-319">The certificate key usage must include Data Encipherment (10) and should not include Server authentication or Client authentication.</span></span></p><p><span data-ttu-id="7f24a-320">詳細については、[Service Fabric アプリケーションでの機密情報の管理](/azure/service-fabric/service-fabric-application-secret-management) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-320">For more information, see [Managing secrets in Service Fabric applications](/azure/service-fabric/service-fabric-application-secret-management).</span></span></p> |
| <span data-ttu-id="7f24a-321">AOS SSL 証明書</span><span class="sxs-lookup"><span data-stu-id="7f24a-321">AOS SSL Certificate</span></span>                          | <p><span data-ttu-id="7f24a-322">この証明書は、AOS Web サイトに接続するクライアントに提示されるサーバー証明書としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-322">This certificate is used as the Server certificate that is presented to the client for the AOS website.</span></span> <span data-ttu-id="7f24a-323">また、WCF (Windows Communication Foundation) / SOAP (Simple Object Access Protocol) 証明書を有効にするためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-323">It's also used to enable Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP) certificates.</span></span></p><p><span data-ttu-id="7f24a-324">Service Fabric サーバー証明書として使用するのと同じワイルドカード証明書を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-324">You can use the same wild card certificate that you used as the Service Fabric Server certificate.</span></span></p> | <p><span data-ttu-id="7f24a-325">この例では、ドメイン名 ax.d365ffo.onprem.contoso.com を、Service Fabric Server 証明書としてサブジェクト代替名 (SAN) に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-325">In this example, the domain name ax.d365ffo.onprem.contoso.com must be added to the Subject Alternative Name (SAN) as in the Service  Fabric Server certificate.</span></span></p> |
| <span data-ttu-id="7f24a-326">セッション認証証明書</span><span class="sxs-lookup"><span data-stu-id="7f24a-326">Session Authentication certificate</span></span>           | <span data-ttu-id="7f24a-327">この証明書は、AOS がユーザーのセッション情報を保護するために使用します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-327">This certificate is used by AOS to help secure a user's session information.</span></span> | <span data-ttu-id="7f24a-328">この証明書は、LCS からの展開時に使用されるファイル共有証明書です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-328">This certificate is also the File Share certificate that will used at the time of deployment from LCS.</span></span> |
| <span data-ttu-id="7f24a-329">データの暗号化証明書</span><span class="sxs-lookup"><span data-stu-id="7f24a-329">Data Encryption certificate</span></span> | <span data-ttu-id="7f24a-330">これらの証明書は、機密情報を暗号化するために AOS によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-330">This certificate is used by the AOS to encrypt sensitive information.</span></span>  | <span data-ttu-id="7f24a-331">これはプロバイダー **Microsoft Enhanced RSA および AES Cryptographic Provider** を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-331">This must be created using the provider **Microsoft Enhanced RSA and AES Cryptographic Provider**.</span></span> |
| <span data-ttu-id="7f24a-332">データ署名の証明書</span><span class="sxs-lookup"><span data-stu-id="7f24a-332">Data Signing certificate</span></span> | <span data-ttu-id="7f24a-333">これらの証明書は、機密情報を暗号化するために AOS によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-333">This certificate is used by AOS to encrypt sensitive information.</span></span>  | <span data-ttu-id="7f24a-334">これは、データ暗号化証明書とは別のもので、プロバイダー**Microsoft の拡張された RSA および AES 暗号化プロバイダー**を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-334">This is separate from the Data Encryption certificate and must be created using the provider **Microsoft Enhanced RSA and AES Cryptographic Provider**.</span></span> |
| <span data-ttu-id="7f24a-335">財務報告クライアント証明書</span><span class="sxs-lookup"><span data-stu-id="7f24a-335">Financial Reporting client certificate</span></span>       | <span data-ttu-id="7f24a-336">この証明書は、財務報告サービスと AOS 間の通信を保護するのに役立ちます。   この証明書を使用して、財務報告サービスと AOS 間の通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-336">This certificate is used to help secure the communication between the Financial Reporting services and the AOS.</span></span> |  |
| <span data-ttu-id="7f24a-337">報告証明書</span><span class="sxs-lookup"><span data-stu-id="7f24a-337">Reporting certificate</span></span>                        | <span data-ttu-id="7f24a-338">この証明書を使用して、SSRS と AOS 間の通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-338">This certificate is used to help secure the communication between SSRS and the AOS.</span></span>| <span data-ttu-id="7f24a-339">**財務報告クライアント証明書を再利用しないでください。**</span><span class="sxs-lookup"><span data-stu-id="7f24a-339">**Do not reuse the Financial Reporting Client certificate.**</span></span> |
| <span data-ttu-id="7f24a-340">オンプレミス ローカル エージェント証明書</span><span class="sxs-lookup"><span data-stu-id="7f24a-340">On-Premise local agent certificate</span></span>           | <p><span data-ttu-id="7f24a-341">この証明書は、オンプレミスと LCS でホストされているローカル エージェント間の通信を保護するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-341">This certificate is used to help secure the communication between a local agent that is hosted on-premises and on LCS.</span></span></p><p><span data-ttu-id="7f24a-342">この証明書を使用すると、Azure AD テナントに代わってローカル エージェントが動作し、LCS と通信して配置を編成および監視することができます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-342">This certificate enables the local agent to act on behalf of your Azure AD tenant, and to communicate with LCS to orchestrate and monitor deployments.</span></span></p><p><span data-ttu-id="7f24a-343">**注記:** テナントにはオンプレミス ローカル エージェント証明書が 1 つだけ必要です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-343">**Note:** Only 1 on-premise local agent certificate is needed for a tenant.</span></span></p>| |

<span data-ttu-id="7f24a-344">以下は、AOS SSL 証明書と組み合わせた Service Fabric Server 証明書の例です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-344">The following is an example of a Service Fabric Server certificate combined with an AOS SSL Certificate.</span></span>

#### <a name="subject-name"></a><span data-ttu-id="7f24a-345">件名</span><span class="sxs-lookup"><span data-stu-id="7f24a-345">Subject name</span></span>

```
CN = *.d365ffo.onprem.contoso.com
```

#### <a name="subject-alternative-names"></a><span data-ttu-id="7f24a-346">件名の代替名</span><span class="sxs-lookup"><span data-stu-id="7f24a-346">Subject Alternative Names</span></span>

```
DNS Name=ax.d365ffo.onprem.contoso.com
DNS Name=sf.d365ffo.onprem.contoso.com
DNS Name=*.d365ffo.onprem.contoso.com
```

### <a name="plansvcacct"></a> <span data-ttu-id="7f24a-347">3. ユーザーとサービス アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="7f24a-347">3. Plan your users and service accounts</span></span>

<span data-ttu-id="7f24a-348">Finance and Operations (オンプレミス) を機能させるために、いくつかのユーザー アカウントまたはサービス アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-348">You must create several user or service accounts for Finance and Operations (on-premises) to work.</span></span> <span data-ttu-id="7f24a-349">サービス アカウントの管理グループ (gMSAs)、ドメイン アカウント、および SQL アカウントの組み合わせを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-349">You must create a combination of group managed service accounts (gMSAs), domain accounts, and SQL accounts.</span></span> <span data-ttu-id="7f24a-350">次の表は、このトピックで使用されるユーザー アカウント、その目的、および名前の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7f24a-350">The following table shows the user accounts, their purpose, and example names that will be used in this topic.</span></span>

| <span data-ttu-id="7f24a-351">ユーザー アカウント</span><span class="sxs-lookup"><span data-stu-id="7f24a-351">User account</span></span>                                            | <span data-ttu-id="7f24a-352">種類</span><span class="sxs-lookup"><span data-stu-id="7f24a-352">Type</span></span>           | <span data-ttu-id="7f24a-353">目的</span><span class="sxs-lookup"><span data-stu-id="7f24a-353">Purpose</span></span> | <span data-ttu-id="7f24a-354">ユーザー名</span><span class="sxs-lookup"><span data-stu-id="7f24a-354">User name</span></span> |
|---------------------------------------------------------|----------------|---------|-----------|
| <span data-ttu-id="7f24a-355">財務レポート アプリケーション サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7f24a-355">Financial Reporting Application Service Account</span></span>         | <span data-ttu-id="7f24a-356">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-356">gMSA</span></span>           |         | <span data-ttu-id="7f24a-357">Contoso\\svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="7f24a-357">Contoso\\svc-FRAS$</span></span> |
| <span data-ttu-id="7f24a-358">財務レポート プロセス サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7f24a-358">Financial Reporting Process Service Account</span></span>             | <span data-ttu-id="7f24a-359">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-359">gMSA</span></span>           |         | <span data-ttu-id="7f24a-360">Contoso\\svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="7f24a-360">Contoso\\svc-FRPS$</span></span> |
| <span data-ttu-id="7f24a-361">財務レポート クリック ワンス デザイナー サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7f24a-361">Financial Reporting Click Once Designer Service Account</span></span> | <span data-ttu-id="7f24a-362">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-362">gMSA</span></span>           |         | <span data-ttu-id="7f24a-363">Contoso\\svc-FRCO$</span><span class="sxs-lookup"><span data-stu-id="7f24a-363">Contoso\\svc-FRCO$</span></span> |
| <span data-ttu-id="7f24a-364">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7f24a-364">AOS Service Account</span></span>                                     | <span data-ttu-id="7f24a-365">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-365">gMSA</span></span>           | <span data-ttu-id="7f24a-366">このユーザーは、将来校正するために作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-366">This user should be created for future-proofing.</span></span> <span data-ttu-id="7f24a-367">今後のリリースでは、AOS を gMSA と連携させる予定です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-367">We plan to enable AOS to work with the gMSA in upcoming releases.</span></span> <span data-ttu-id="7f24a-368">このユーザーを設定時に作成することで、gMSA へのシームレスな移行を確実にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-368">By creating this user at the time of setup, you will help to ensure a seamless transition to the gMSA.</span></span> | <span data-ttu-id="7f24a-369">Contoso\\svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="7f24a-369">Contoso\\svc-AXSF$</span></span> |
| <span data-ttu-id="7f24a-370">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7f24a-370">AOS Service Account</span></span>                                     | <span data-ttu-id="7f24a-371">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="7f24a-371">Domain account</span></span> | <span data-ttu-id="7f24a-372">AOS は、一般提供 (GA) リリースでこのユーザーを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-372">AOS uses this user in the general availability (GA) release.</span></span> | <span data-ttu-id="7f24a-373">Contoso\\AXServiceUser</span><span class="sxs-lookup"><span data-stu-id="7f24a-373">Contoso\\AXServiceUser</span></span> |
| <span data-ttu-id="7f24a-374">AOS SQL DB 管理者ユーザー</span><span class="sxs-lookup"><span data-stu-id="7f24a-374">AOS SQL DB Admin user</span></span>                                   | <span data-ttu-id="7f24a-375">SQL ユーザー</span><span class="sxs-lookup"><span data-stu-id="7f24a-375">SQL user</span></span>       | <span data-ttu-id="7f24a-376">Finance and Operations は、このユーザーを使用して SQL\* を認証します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-376">Finance and Operations uses this user to authenticate with SQL\*.</span></span> <span data-ttu-id="7f24a-377">このユーザーも、今後のリリースで gMSA ユーザーに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-377">This user will also be replaced by the gMSA user in upcoming releases.</span></span> | <span data-ttu-id="7f24a-378">AXDBAdmin</span><span class="sxs-lookup"><span data-stu-id="7f24a-378">AXDBAdmin</span></span> |
| <span data-ttu-id="7f24a-379">ローカル配置エージェント サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7f24a-379">Local Deployment Agent Service Account</span></span>                  | <span data-ttu-id="7f24a-380">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-380">gMSA</span></span>           | <span data-ttu-id="7f24a-381">このアカウントは、ローカル エージェントによって、さまざまなノードでの展開を調整するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-381">This account is used by the local agent to orchestrate the deployment on various nodes.</span></span> | <span data-ttu-id="7f24a-382">Contoso\\Svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="7f24a-382">Contoso\\Svc-LocalAgent$</span></span> |

<span data-ttu-id="7f24a-383">\* SQL 認証の SQL ユーザー名とパスワードは、暗号化されてファイル共有に格納されているため、保護されています。</span><span class="sxs-lookup"><span data-stu-id="7f24a-383">\* The SQL user name and password for SQL authentication are secured because they are encrypted and stored in the file share.</span></span>

### <a name="createdns"></a> <span data-ttu-id="7f24a-384">4. DNS ゾーンの作成とレコードの追加</span><span class="sxs-lookup"><span data-stu-id="7f24a-384">4. Create DNS zones and add A records</span></span>

<span data-ttu-id="7f24a-385">DNS は AD DS と統合されており、ネットワーク内のリソースを整理、管理、検索することができます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-385">DNS is integrated with AD DS, and lets you organize, manage, and find resources in a network.</span></span> <span data-ttu-id="7f24a-386">AOS ホスト名と Service Fabric クラスタの DNS 正引き検索ゾーンと A レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-386">Create a DNS forward lookup zone and A records for the AOS host name and the Service Fabric cluster.</span></span> <span data-ttu-id="7f24a-387">この設定例では、DNS ゾーン名は d365ffo.onprem.contoso.com で、A レコード/ホスト名は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7f24a-387">In this example setup, the DNS zone name is d365ffo.onprem.contoso.com, and the A records/host names are as follows:</span></span>

- <span data-ttu-id="7f24a-388">AOS の機械の場合 **ax**.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7f24a-388">**ax**.d365ffo.onprem.contoso.com for AOS machines</span></span>
- <span data-ttu-id="7f24a-389">Service Fabric クラスターの場合 **sf**.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7f24a-389">**sf**.d365ffo.onprem.contoso.com for the Service Fabric cluster</span></span>

#### <a name="add-a-dns-zone"></a><span data-ttu-id="7f24a-390">DNS ゾーンの追加</span><span class="sxs-lookup"><span data-stu-id="7f24a-390">Add a DNS zone</span></span>

<span data-ttu-id="7f24a-391">DNS ゾーンを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-391">Use the following procedure to add a DNS zone.</span></span>

1. <span data-ttu-id="7f24a-392">ドメイン コントローラー マシンにサインインし、**開始** を選択し、**dnsmgmt.msc** と入力して DNS マネージャーを起動します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-392">Sign in to the domain controller machine, select **Start**, and start DNS Manager by typing **dnsmgmt.msc**.</span></span>
2. <span data-ttu-id="7f24a-393">ドメイン コントローラー名を右クリックし、**新しいゾーン** \> **次へ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-393">Right-click the domain controller name, and then select **New Zone** \> **Next**.</span></span>
3. <span data-ttu-id="7f24a-394">**プライマリ ゾーン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-394">Select **Primary Zone**.</span></span>
4. <span data-ttu-id="7f24a-395">**Active Directory にゾーンを保存 (DNS サーバーが書き込み可能なドメイン コントローラーの場合にのみ使用可能)** のチェック ボックスが選択されたままの状態で、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-395">Leave the **Store the zone in Active Directory (available only if the DNS Server is a writeable domain controller** check box selected, and then select **Next**.</span></span>
5. <span data-ttu-id="7f24a-396">**このドメイン (Contoso.com) のドメイン コントローラーで実行されているすべての DNS サーバーに対して** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-396">Select **To all DNS Servers running on Domain Controllers in this domain: Contoso.com**, and then select **Next**.</span></span>
6. <span data-ttu-id="7f24a-397">**前方参照ゾーン** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-397">Select **Forward Lookup Zone**, and then select **Next**.</span></span>
7. <span data-ttu-id="7f24a-398">設定するゾーン名を入力し、**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-398">Enter the zone name for your setup, and then select **Next**.</span></span> <span data-ttu-id="7f24a-399">たとえば、**d365ffo.onprem.contoso.com** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-399">For example, enter **d365ffo.onprem.contoso.com**.</span></span>
8. <span data-ttu-id="7f24a-400">**動的更新を許可しない** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-400">Select **Do not allow dynamic updates**, and then select **Next**.</span></span>

#### <a name="set-up-an-a-record-for-aos"></a><span data-ttu-id="7f24a-401">AOS の A レコードを設定する</span><span class="sxs-lookup"><span data-stu-id="7f24a-401">Set up an A record for AOS</span></span>

<span data-ttu-id="7f24a-402">新しい DNS ゾーンで、**AOSNodeType** タイプの Service Fabric クラスター ノード**ごと**に、**ax.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-402">In the new DNS zone, create one A record that is named **ax.d365ffo.onprem.contoso.com** for **each** Service Fabric cluster node of the **AOSNodeType** type.</span></span> <span data-ttu-id="7f24a-403">他のノード タイプの A レコードは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-403">Don't create A records for the other node types.</span></span>

1. <span data-ttu-id="7f24a-404">新しいゾーンを右クリックして、**新しいホスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-404">Right-click the new zone, and then select **New Host**.</span></span>
2. <span data-ttu-id="7f24a-405">Service Fabric ノードの 名前および IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-405">Enter the name and IP address of the Service Fabric node.</span></span> <span data-ttu-id="7f24a-406">(たとえば、**10.179.108.12** を IP アドレスとして入力します。) **ホストの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-406">(For example, enter **10.179.108.12** as the IP address.) Select **Add Host**.</span></span>

#### <a name="set-up-an-a-record-for-the-orchestrator"></a><span data-ttu-id="7f24a-407">Orchestrator の A レコードを設定する</span><span class="sxs-lookup"><span data-stu-id="7f24a-407">Set up an A record for the orchestrator</span></span>

<span data-ttu-id="7f24a-408">新しい DNS ゾーンで、**OrchestratorType** タイプの Service Fabric クラスター ノード**ごと**に、**sf.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-408">In the new DNS zone, create an A record that is named **sf.d365ffo.onprem.contoso.com** for **each** Service Fabric cluster node of the **OrchestratorType** type.</span></span> <span data-ttu-id="7f24a-409">他のノード タイプの A レコードは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-409">Don't create A records for the other node types.</span></span>

1. <span data-ttu-id="7f24a-410">新しいゾーンを右クリックして、**新しいホスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-410">Right-click the new zone, and then select **New Host**.</span></span>
2. <span data-ttu-id="7f24a-411">Service Fabric ノードの 名前および IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-411">Enter the name and IP address of the Service Fabric node.</span></span> <span data-ttu-id="7f24a-412">(たとえば、**10.179.108.15** を IP アドレスとして入力します。) **ホストの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-412">(For example, enter **10.179.108.15** as the IP address.) Select **Add Host**.</span></span>

### <a name="joindomain"></a> <span data-ttu-id="7f24a-413">5. VM のドメインへの参加</span><span class="sxs-lookup"><span data-stu-id="7f24a-413">5. Join VMs to the domain</span></span>

<span data-ttu-id="7f24a-414">各 VM をドメインに参加させるには、[Windows Server 2016 を Active Directory ドメインに参加させる方法](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html) の各手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-414">Join each VM to the domain by completing the steps in [How to join Windows Server 2016 to an Active Directory domain](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html).</span></span> <span data-ttu-id="7f24a-415">または、次の Windows PowerShell スクリプトを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-415">Alternatively, use the following Windows PowerShell script.</span></span>

```powershell
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
```

> [!IMPORTANT]
> <span data-ttu-id="7f24a-416">ドメインにそれらを結合させた後、VM を再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-416">You must restart the VMs after you join them to the domain.</span></span>

<span data-ttu-id="7f24a-417">VM をドメインに参加させた後、ローカル管理者グループに AOS サービス アカウント **Contoso\svc-AXSF$** と **Contoso\AXServiceUser** を追加します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-417">After the VMs are joined to the domain, add the AOS Service Accounts, **Contoso\svc-AXSF$** and **Contoso\AXServiceUser** to the local administrators group.</span></span> <span data-ttu-id="7f24a-418">詳細については、「[ローカル グループへのメンバーの追加](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-418">For more information, see [Add a member to local group](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx).</span></span>

### <a name="downloadscripts"></a> <span data-ttu-id="7f24a-419">6. LCS からのセットアップ スクリプトのダウンロード</span><span class="sxs-lookup"><span data-stu-id="7f24a-419">6. Download setup scripts from LCS</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f24a-420">スクリプトは、オンプレミス インフラストラクチャと同じドメイン内のコンピューターから実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-420">The scripts must be executed from a computer in the same domain that the on-premises infrastructure is in.</span></span>

1. <span data-ttu-id="7f24a-421">[LCS](https://lcs.dynamics.com/v2) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-421">Sign in to [LCS](https://lcs.dynamics.com/v2).</span></span>
2. <span data-ttu-id="7f24a-422">ダッシュボードで、**共有アセット ライブラリ**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-422">On the dashboard, select the **Shared asset library** tile.</span></span>
3. <span data-ttu-id="7f24a-423">**モデル**タブの、グリッドで、**Dynamics 365 for Operations オンプレミス - 配置スクリプト - 最新**行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-423">On the **Model** tab, in the grid, select the **Dynamics 365 for Operations on-premises - Deployment scripts - Latest** row.</span></span>
4. <span data-ttu-id="7f24a-424">**バージョン** ボタンをクリックし、**バージョン 1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-424">Click the **Versions** button, and then select **Version 1**.</span></span>
5. <span data-ttu-id="7f24a-425">zip ファイルを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-425">Right-click the zip file, and then select **Properties**.</span></span> <span data-ttu-id="7f24a-426">ダイアログ ボックスで、**ブロック解除**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-426">In the dialog box, select the **Unblock** check box.</span></span>
6. <span data-ttu-id="7f24a-427">ZIP ファイルをスクリプトの実行に使用するマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-427">Copy the zip file to the machine that will be used to execute the scripts.</span></span>
7. <span data-ttu-id="7f24a-428">**infrastructure** という名前のフォルダーにファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-428">Unzip the files into a folder that is named **infrastructure**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f24a-429">このフォルダーの ConfigTemplate.xml にすべての編集を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-429">Ensure all edits are made to the ConfigTemplate.xml in this folder.</span></span>

### <a name="describeconfig"></a> <span data-ttu-id="7f24a-430">7. コンフィギュレーションの記述</span><span class="sxs-lookup"><span data-stu-id="7f24a-430">7. Describe your configuration</span></span>

<span data-ttu-id="7f24a-431">インフラストラクチャの設定 スクリプトは、次のコンフィギュレーション ファイルを使用して設定を実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-431">The infrastructure setup scripts use the following configuration files to drive the setup.</span></span>
- <span data-ttu-id="7f24a-432">infrastructure\ConfigTemplate.xml</span><span class="sxs-lookup"><span data-stu-id="7f24a-432">infrastructure\ConfigTemplate.xml</span></span>
- <span data-ttu-id="7f24a-433">infrastructure\D365FO-OP\NodeTopologyDefintion.xml</span><span class="sxs-lookup"><span data-stu-id="7f24a-433">infrastructure\D365FO-OP\NodeTopologyDefintion.xml</span></span>
- <span data-ttu-id="7f24a-434">infrastructure\D365FO-OP\DatabaseTopologyDefintion.xml</span><span class="sxs-lookup"><span data-stu-id="7f24a-434">infrastructure\D365FO-OP\DatabaseTopologyDefintion.xml</span></span>

<span data-ttu-id="7f24a-435">**infrastructure\ConfigTemplate.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-435">**infrastructure\ConfigTemplate.xml** describes:</span></span>
- <span data-ttu-id="7f24a-436">アプリケーションが動作するために必要なサービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7f24a-436">Service Accounts that are needed for the application to operate</span></span>
- <span data-ttu-id="7f24a-437">通信を保護するために必要な証明書</span><span class="sxs-lookup"><span data-stu-id="7f24a-437">Certificates necessary for securing communications</span></span>
- <span data-ttu-id="7f24a-438">データベース コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f24a-438">Database configuration</span></span>
- <span data-ttu-id="7f24a-439">Service Fabric クラスター構成</span><span class="sxs-lookup"><span data-stu-id="7f24a-439">Service Fabric cluster configuration</span></span>

<span data-ttu-id="7f24a-440">各 Service Fabric ノード タイプについて、**infrastructure\D365FO-OP\NodeTopologyDefinition.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-440">For each Service Fabric Node type, **infrastructure\D365FO-OP\NodeTopologyDefinition.xml** describes:</span></span>

- <span data-ttu-id="7f24a-441">各ノード タイプとアプリケーション、ドメインとサービス アカウント、および証明書間のマッピング。</span><span class="sxs-lookup"><span data-stu-id="7f24a-441">The mapping between each node type and the application, domain and service accounts, and certificates.</span></span>
- <span data-ttu-id="7f24a-442">UAC を有効にするかどうか</span><span class="sxs-lookup"><span data-stu-id="7f24a-442">Whether to enable the UAC</span></span>
- <span data-ttu-id="7f24a-443">Windows の機能とシステム ソフトウェアの前提条件</span><span class="sxs-lookup"><span data-stu-id="7f24a-443">Prerequisites for Windows features and system software</span></span>
- <span data-ttu-id="7f24a-444">厳密な名前の検証を有効にするかどうか</span><span class="sxs-lookup"><span data-stu-id="7f24a-444">Whether strong name validation should be enabled</span></span>
- <span data-ttu-id="7f24a-445">開くファイアウォール ポートのリスト</span><span class="sxs-lookup"><span data-stu-id="7f24a-445">List of firewall ports to be opened</span></span>

<span data-ttu-id="7f24a-446">各データベースについて、**infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-446">For each database, **infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml** describes:</span></span>

- <span data-ttu-id="7f24a-447">DB 設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-447">The DB settings</span></span>
- <span data-ttu-id="7f24a-448">ユーザーとロールの間のマッピング</span><span class="sxs-lookup"><span data-stu-id="7f24a-448">The mappings between users and roles</span></span>

#### <a name="create-gmsa-and-domain-user-accounts"></a><span data-ttu-id="7f24a-449">gMSA およびドメイン ユーザー アカウントを作成する</span><span class="sxs-lookup"><span data-stu-id="7f24a-449">Create gMSA and domain user accounts</span></span>

1. <span data-ttu-id="7f24a-450">**インフラストラクチャ** フォルダーに展開したインフラストラクチャ スクリプトがあるマシンに移動します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-450">Navigate to the machine that has the unzipped infrastructure scripts in the **infrastructure** folder.</span></span>
2. <span data-ttu-id="7f24a-451">**インフラストラクチャ**フォルダーをドメイン コントローラー マシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-451">Copy the **infrastructure** folder to the domain controller machine.</span></span>
3. <span data-ttu-id="7f24a-452">管理者特権モードで Windows PowerShell を起動し、ディレクトリを **infrastructure** フォルダーに変更して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-452">Start Windows PowerShell in elevated mode, change the directory to the **infrastructure** folder, and run the following commands.</span></span>

    ```powershell
    Import-Module .\D365FO-OP\D365FO-OP.psd1
    New-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

4. <span data-ttu-id="7f24a-453">アカウントまたはマシンを変更する必要がある場合は、元の **インフラストラクチャ** フォルダーの ConfigTemplate.xml ファイルを更新し、このマシンにコピーしてから次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-453">If you must make changes to accounts or machines, update the ConfigTemplate.xml file in the original **infrastructure** folder, copy it to this machine and then run the following script.</span></span>

    ```powershell
    Update-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="configurecert"></a> <span data-ttu-id="7f24a-454">8. 証明書のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f24a-454">8. Configure certificates</span></span>

1. <span data-ttu-id="7f24a-455">**インフラストラクチャ** フォルダーがあるマシンに移動します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-455">Navigate to the machine that has the **infrastructure** folder.</span></span>
2. <span data-ttu-id="7f24a-456">自己署名証明書を生成する必要がある場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-456">If you must generate self-signed certificates, run the following command.</span></span> <span data-ttu-id="7f24a-457">スクリプトは証明書を作成し、それらをコンピューターの「CurrentUser\My certificate store」に格納し、XML ファイルのサムプリントを更新します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-457">The script will create the certificates, put them in the CurrentUser\My certificate store on the machine, and update the thumbprints in the XML file.</span></span>

    ```powershell
    # Create self-signed certs
    .\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    <span data-ttu-id="7f24a-458">証明書を再利用する必要があるため、証明書を生成する必要がない場合は、**generateSelfSignedCert** タグを **false** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-458">If you must reuse any certificates and therefore don't have to generate certificates for them, set the **generateSelfSignedCert** tag to **false**.</span></span>

3. <span data-ttu-id="7f24a-459">既に生成されている SSL 証明書を使用している場合は、証明書生成をスキップし、configTemplate.xml ファイルの拇印を更新します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-459">If you're using SSL certificates that were already generated, skip the Certificate generation and update the thumbprints in the configTemplate.xml file.</span></span> <span data-ttu-id="7f24a-460">証明書は CurrentUser\My ストアにインストールする必要があり、その秘密キーはエクスポート可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7f24a-460">The certificates need to be installed in the CurrentUser\My store and their private keys must be exportable.</span></span>

> [!WARNING]
> <span data-ttu-id="7f24a-461">存在する場合に特定するのが難しい先頭の印刷不可能な特殊文字のため、証明書マネージャーは拇印をコピーするために使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-461">Because of a leading not-printable special character, which is difficult to determine when present, the cert manager should not be used to copy thumbprints.</span></span> <span data-ttu-id="7f24a-462">非印刷可能な特殊文字が存在する場合、**X509 証明書が有効ではない**というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-462">If the not-printable special character is present, you will get **X509 certificate not valid** error.</span></span> <span data-ttu-id="7f24a-463">拇印を取得するには、PowerShell コマンドの結果を参照するか、PowerShell で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-463">To retrieve the thumbprints, see results from PowerShell commands or run the following commands in PowerShell.</span></span>
> ```powershell
> dir cert:\CurrentUser\My
> dir cert:\LocalMachine\My
> dir cert:\LocalMachine\Root
> ```

4. <span data-ttu-id="7f24a-464">各証明書の **ProtectTo** でユーザーまたはグループのセミコロンで区切られた一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-464">Specify a semi-colon separated list of users or groups in the **ProtectTo** tag for each certificate.</span></span> <span data-ttu-id="7f24a-465">**ProtectTo** タグで指定された Active Directory ユーザーとグループのみに、スクリプトを使用してエクスポートされる証明書をインポートするアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-465">Only Active directory users and groups specified in the **ProtectTo** tag will have permissions to import the certificates that are exported using the scripts.</span></span> <span data-ttu-id="7f24a-466">エクスポートした証明書を保護するため、スクリプトによりパスワードがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7f24a-466">Passwords are not supported by the script to protect the exported certificates</span></span>

5. <span data-ttu-id="7f24a-467">証明書を .pfx ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-467">Export the certificates into .pfx files.</span></span>

    ```powershell
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will be written to infrastructure\Certs folder.
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="setupvms"></a> <span data-ttu-id="7f24a-468">9. VM の設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-468">9. Setup VMs</span></span>
1. <span data-ttu-id="7f24a-469">各 VM で実行する必要があるスクリプトをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-469">Export the scripts that must be run on each VM.</span></span>

    ```powershell
    # Exports the script files to be execute on each VM into a directory VMs\<VMName>.
    .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. <span data-ttu-id="7f24a-470">次の Microsoft Windows Installers (MSIs) を全ての VMs でアクセス可能なファイル共有にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-470">Download the following Microsoft Windows Installers (MSIs) into a file share that is accessible by all VMs.</span></span>

| <span data-ttu-id="7f24a-471">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="7f24a-471">Component</span></span> | <span data-ttu-id="7f24a-472">リンクのダウンロード</span><span class="sxs-lookup"><span data-stu-id="7f24a-472">Download link</span></span> |
|-----------|---------------|
| <span data-ttu-id="7f24a-473">SNAC – ODBC ドライバー</span><span class="sxs-lookup"><span data-stu-id="7f24a-473">SNAC – ODBC driver</span></span> | <https://www.microsoft.com/en-us/download/details.aspx?id=53339> |
| <span data-ttu-id="7f24a-474">Microsoft SQL Server Management Studio 17.2</span><span class="sxs-lookup"><span data-stu-id="7f24a-474">Microsoft SQL Server Management Studio 17.2</span></span> | <https://go.microsoft.com/fwlink/?linkid=854085> |
| <span data-ttu-id="7f24a-475">Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="7f24a-475">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</span></span> | <https://support.microsoft.com/en-us/help/3179560> |
| <span data-ttu-id="7f24a-476">Microsoft Access データベース エンジン 2010 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="7f24a-476">Microsoft Access Database Engine 2010 Redistributable</span></span> | <https://www.microsoft.com/en-us/download/details.aspx?id=13255> |

#### <a name="follow-these-steps-for-each-vm"></a><span data-ttu-id="7f24a-477">各 VM について、これらのステップに従います。</span><span class="sxs-lookup"><span data-stu-id="7f24a-477">Follow these steps for each VM</span></span>

1. <span data-ttu-id="7f24a-478">各 infrastructure\VMs\<VMName> フォルダーのコンテンツを対応する VM にコピーし、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-478">Copy the contents of each infrastructure\VMs\<VMName> folder into the corresponding VM, and then run the following scripts.</span></span>

    ```powershell
    # Install pre-req software on the VMs.
    .\Configure-PreReqs.ps1 -MSIFilePath <path of the MSIs>
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="7f24a-479">再起動するように求められるたびにコンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-479">Restart the machine each time you're prompted to restart it.</span></span> <span data-ttu-id="7f24a-480">再起動した後、すべての前提条件がインストールされるまで、`.\Configure-PreReqs.ps1` スクリプトを再実行することを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-480">Make sure that you rerun the `.\Configure-PreReqs.ps1` script after each restart until all the prerequisites are installed.</span></span>

2. <span data-ttu-id="7f24a-481">VM セットアップを完了するため、存在する場合は、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-481">Run the following scripts, if they exist, in order to complete the VM setup.</span></span>

    ```powershell
    .\Add-GMSAOnVM.ps1
    .\Import-PfxFiles.ps1
    .\Set-CertificateAcls.ps1
    ```

3. <span data-ttu-id="7f24a-482">次のスクリプトを実行して VM のセットアップを検証します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-482">Run the following script to validate the VM setup.</span></span>

    ```powershell
    .\Test-D365FOConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="setupsfcluster"></a> <span data-ttu-id="7f24a-483">10. スタンドアロン Service Fabric クラスターの設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-483">10. Set up a standalone Service Fabric cluster</span></span>

1. <span data-ttu-id="7f24a-484">[Service Fabric スタンドアロン インストール パッケージ](http://go.microsoft.com/fwlink/?LinkId=730690) を使用中の Service Fabric ノードのいずれかにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-484">Download the [Service Fabric standalone installation package](http://go.microsoft.com/fwlink/?LinkId=730690) onto one of your Service Fabric nodes.</span></span> <span data-ttu-id="7f24a-485">ZIP ファイルをダウンロードした後、 ZIP ファイルを右クリックし**プロパティ**を選択してブロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-485">After the zip file is downloaded, unblock it by right-clicking the zip file and then selecting **Properties**.</span></span> <span data-ttu-id="7f24a-486">ダイアログ ボックスで、右下の **ブロック解除** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-486">In the dialog box, select the **Unblock** check box in the lower right.</span></span>

2. <span data-ttu-id="7f24a-487">ZIP ファイルを Service Fabric クラスター内のいずれかのノードにコピーし、解凍します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-487">Copy the zip file to one of the nodes in the Service Fabric cluster, and unzip it.</span></span> <span data-ttu-id="7f24a-488">**インフラストラクチャ**フォルダーが、このフォルダーにアクセスすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-488">Ensure the **infrastructure** folder has access to this folder.</span></span>

3. <span data-ttu-id="7f24a-489">**インフラストラクチャ** フォルダーに移動し、次のコマンドを実行して Service Fabric の ClusterConfig.json ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-489">Navigate to the **infrastructure** folder and execute the following command to generate the Service Fabric ClusterConfig.json file.</span></span>

    ```powershell
   .\New-SFClusterConfig.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -TemplateConfig <ServiceFabricStandaloneInstallerPath>\ClusterConfig.X509.MultiMachine.json
    ```

    <span data-ttu-id="7f24a-490">詳細については、[手順 1B: 複数のマシンでクラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)、[X.509 証明書を使用して Windows スタンドアロン クラスターを保護する](/azure/service-fabric/service-fabric-windows-cluster-x509-security)、および[Windows Server で実行されているスタンドアロン クラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-490">For more information, see, [Step 1B: Create a multi-machine cluster](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Secure a standalone cluster on Windows using X.509 certificates](/azure/service-fabric/service-fabric-windows-cluster-x509-security), and [Create a standalone cluster running on Windows Server](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).</span></span>

4. <span data-ttu-id="7f24a-491">生成された ClusterConfig.json ファイルを \<ServiceFabricStandaloneInstallerPath\> にコピーします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-491">Copy the generated ClusterConfig.json file to the \<ServiceFabricStandaloneInstallerPath\>.</span></span>

5. <span data-ttu-id="7f24a-492">上位の権限を使用して Windows PowerShell で \<ServiceFabricStandaloneInstallerPath\> に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-492">Navigate to the \<ServiceFabricStandaloneInstallerPath\> in Windows PowerShell by using elevated privileges.</span></span> <span data-ttu-id="7f24a-493">次のコマンドを実行して ClusterConfig をテストします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-493">Run the following command to test ClusterConfig.</span></span>

    ```powershell
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

6. <span data-ttu-id="7f24a-494">テストが成功した場合は、次のコマンドを実行してクラスターを展開します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-494">If the test is successful, run the following command to deploy the cluster.</span></span>

    ```powershell
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

7. <span data-ttu-id="7f24a-495">クラスターが作成された後は、任意のクライアント マシンで Service Fabric エクスプローラーを開き、インストールを検証します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-495">After the cluster is created, open the Service Fabric explorer on any client machine to validate the installation.</span></span>

    1. <span data-ttu-id="7f24a-496">まだインストールされていない場合、CurrentUser\\My に Service Fabric クライアント証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-496">Install the Service Fabric client certificate in CurrentUser\\My if it isn't already installed.</span></span>
    2. <span data-ttu-id="7f24a-497">**IE 設定** \> **互換モード** に移動し、**互換モードでイントラネット サイトを表示する** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-497">Go to **IE settings** \> **Compatibility Mode**, and clear the **Display Intranet sites in compatibility mode** check box.</span></span>
    3. <span data-ttu-id="7f24a-498">`https://sf.d365ffo.onprem.contoso.com:19080` に移動します。sf.d365ffo.onprem.contoso.com は、ゾーンで指定されている Service Fabric クラスターのホスト名です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-498">Go to `https://sf.d365ffo.onprem.contoso.com:19080`, where sf.d365ffo.onprem.contoso.com is the host name of the Service Fabric cluster that is specified in the zone.</span></span> <span data-ttu-id="7f24a-499">DNS 名前解決が設定されていない場合は、マシンの IP アドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-499">If DNS name resolution isn't configured, use the IP address of the machine.</span></span>
    4. <span data-ttu-id="7f24a-500">クライアントの証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-500">Select the client certificate.</span></span> <span data-ttu-id="7f24a-501">**Service Fabric エクスプローラー** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-501">The **Service Fabric explorer** page appears.</span></span>

### <a name="configurelcs"></a> <span data-ttu-id="7f24a-502">11. テナント用 LCS 接続のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f24a-502">11. Configure LCS connectivity for the tenant</span></span>

<span data-ttu-id="7f24a-503">Finance and Operations の展開とサービスは、オンプレミスのローカル エージェントを使用して LCS を通じて調整されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-503">Deployment and servicing of Finance and Operations is orchestrated through LCS by using an on-premises local agent.</span></span> <span data-ttu-id="7f24a-504">LCS から Finance and Operations テナントへの接続を確立するには、Azure AD テナント (たとえば、Contoso.onmicrosoft.com) の代わりに動作するローカル エージェントを可能にする証明書をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-504">To establish connectivity from LCS to the Finance and Operations tenant, you must configure a certificate that enables the local agent to act on behalf on your Azure AD tenant (for example, Contoso.onmicrosoft.com).</span></span>

<span data-ttu-id="7f24a-505">CA から取得したオンプレミス エージェントの証明書またはスクリプトを使用して生成した自己署名証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-505">Use the on-premises agent certificate that you acquired from a CA or the self-signed certificate that you generated by using scripts.</span></span>

<span data-ttu-id="7f24a-506">オンプレミス エージェント証明書は、テナントごとに複数のサンドボックス環境および実稼動環境で再利用できます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-506">The on-premises agent certificate can be reused across multiple sandbox and production environments per tenant.</span></span>

<span data-ttu-id="7f24a-507">グローバル管理者ディレクトリの役割を持つユーザー アカウントだけが、LCS を承認するための証明書を追加できます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-507">Only user accounts that have the Global Administrator directory role can add certificates to authorize LCS.</span></span> <span data-ttu-id="7f24a-508">既定では、組織の Microsoft Office 365 にサインアップする担当者が、ディレクトリのグローバル管理者です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-508">By default, the person who signs up for Microsoft Office 365 for your organization is the global administrator for the directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f24a-509">テナントごとに証明書を正確に 1 回構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-509">You must configure the certificate exactly one time per tenant.</span></span> <span data-ttu-id="7f24a-510">すべてのオンプレミス環境では、同じ証明書を使用して LCS に接続できます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-510">All on-premises environments can use the same certificate to connect with LCS.</span></span>

1. <span data-ttu-id="7f24a-511">Azure PowerShell の最新バージョンをクライアント マシンにダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-511">Download and install the latest version of Azure PowerShell on a client machine.</span></span> <span data-ttu-id="7f24a-512">詳細については、[Azure PowerShell のインストールおよびコンフィギュレーション](/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-512">For more information, see [Install and configure Azure PowerShell](/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).</span></span>
2. <span data-ttu-id="7f24a-513">[顧客の Azure ポータル](https://portal.azure.com) にサインインして、グローバル管理者ディレクトリの役割があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-513">Sign in to the [customer's Azure portal](https://portal.azure.com) to verify that you have the Global Administrator directory role.</span></span>
3. <span data-ttu-id="7f24a-514">$(DownloadPath)\\InfrastructureScripts から次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-514">Run the following script from $(DownloadPath)\\InfrastructureScripts.</span></span>
    ```powershell
    .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
    ```

### <a name="setupfile"></a> <span data-ttu-id="7f24a-515">12.ファイル ストレージの設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-515">12. Set up file storage</span></span>

<span data-ttu-id="7f24a-516">以下の SMB 3.0 ファイル共有を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-516">You must set up the following SMB 3.0 file shares:</span></span>

- <span data-ttu-id="7f24a-517">AOS にアップロードされるユーザー ドキュメントを格納するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\aos-storage)。</span><span class="sxs-lookup"><span data-stu-id="7f24a-517">A file share that stores user documents that are uploaded to AOS (for example, \\\\DAX7SQLAOFILE1\\aos-storage).</span></span>
- <span data-ttu-id="7f24a-518">デプロイメントを調整するための最新のビルド ファイルと構成ファイルを保存するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\agent)。</span><span class="sxs-lookup"><span data-stu-id="7f24a-518">A file share that stores the latest build and configuration files to orchestrate the deployment (for example, \\\\DAX7SQLAOFILE1\\agent).</span></span>

    > [!WARNING]
    > <span data-ttu-id="7f24a-519">共有に入れるファイルの最大パス長を超えないように、このファイル共有パスはできるだけ短くしておいてください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-519">Keep this file share path as short as possible to avoid exceeding the maximum path length on the files that will be put in the share.</span></span>

<span data-ttu-id="7f24a-520">SMB 3.0 を有効にする方法については、[SMB セキュリティの強化](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-520">For information about how to enable SMB 3.0, see [SMB Security Enhancements](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="7f24a-521">セキュリティで保護されたダイアレクト ネゴシエーションでは、SMB 2.0 または 3.0 から SMB 1.0 へのダウングレードを検出または防止できません。</span><span class="sxs-lookup"><span data-stu-id="7f24a-521">Secure dialect negotiation can't detect or prevent downgrades from SMB 2.0 or 3.0 to SMB 1.0.</span></span> <span data-ttu-id="7f24a-522">したがって、SMB 1.0 サーバーを無効にすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-522">Therefore, we strongly recommend that you disable the SMB 1.0 server.</span></span> <span data-ttu-id="7f24a-523">SMB 1.0 サーバーを無効にすることで、SMB 暗号化のすべての機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-523">By disabling the SMB 1.0 server, you can take advantage of the full capabilities of SMB encryption.</span></span>
> - <span data-ttu-id="7f24a-524">環境内の残りの部分でデータが保護されていることを保証するために、BitLocker ドライブ暗号化をすべてのマシンで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-524">To help ensure that your data is protected while it's at rest in your environment, BitLocker Drive Encryption must be enabled on every machine.</span></span> <span data-ttu-id="7f24a-525">BitLocker を有効にする方法については、[BitLocker: Windows Server 2012 以降で配置する方法](/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-525">For information about how to enable BitLocker, see [BitLocker: How to deploy on Windows Server 2012 and later](/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).</span></span>

1. <span data-ttu-id="7f24a-526">ファイル共有マシンで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-526">On the file share machine, run the following command.</span></span>

    ```powershell
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```

2. <span data-ttu-id="7f24a-527">\\\\DAX7SQLAOFILE1\\aos-storage ファイル共有を設定するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7f24a-527">Follow these steps to set up the \\\\DAX7SQLAOFILE1\\aos-storage file share:</span></span>

    1. <span data-ttu-id="7f24a-528">サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-528">In Server Manager, select **File and Storage Services** \> **Shares**.</span></span>
    2. <span data-ttu-id="7f24a-529">**タスク**\>**新しい共有** を選択し、新しい共有を作成します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-529">Select **Tasks** \> **New Share** to create a new share.</span></span> <span data-ttu-id="7f24a-530">共有に **aos-storage** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-530">Name the share **aos-storage**.</span></span>
    3. <span data-ttu-id="7f24a-531">OrchestratorType を除いて、Service Fabric クラスター内のすべてのマシンに対して**変更**許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-531">Grant **Modify** permissions for every machine in the Service Fabric cluster except OrchestratorType.</span></span>
    4. <span data-ttu-id="7f24a-532">AOS ドメイン ユーザー (contoso\\AXServiceUser) と gMSA ユーザー (contoso\\svc-AXSF$) に対して、**変更**アクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-532">Grant **Modify** permissions for the user AOS domain user (contoso\\AXServiceUser) and the gMSA user (contoso\\svc-AXSF$).</span></span>

3. <span data-ttu-id="7f24a-533">\\\\DAX7SQLAOFILE1\\ エージェント ファイル共有を設定するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7f24a-533">Follow these steps to set up the \\\\DAX7SQLAOFILE1\\agent file share:</span></span>

    1. <span data-ttu-id="7f24a-534">サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-534">In Server Manager, select **File and Storage Services** \> **Shares**.</span></span>
    2. <span data-ttu-id="7f24a-535">**タスク**\>**新しい共有** を選択し、新しい共有を作成します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-535">Select **Tasks** \> **New Share** to create a new share.</span></span> <span data-ttu-id="7f24a-536">共有に**エージェント**と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-536">Name the share **agent**.</span></span>
    3. <span data-ttu-id="7f24a-537">ローカル展開エージェント (contoso\\svc-LocalAgent$) の gMSA ユーザーに対して **フル コントロール** のアクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-537">Grant **Full-Control** permissions to the gMSA user for the local deployment agent (contoso\\svc-LocalAgent$).</span></span>

### <a name="setupsql"></a> <span data-ttu-id="7f24a-538">13. SQL Server の設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-538">13. Set up SQL Server</span></span>

1. <span data-ttu-id="7f24a-539">高可用性を備えた SQL Server 2016 SP1 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-539">Install SQL Server 2016 SP1 with high availability.</span></span> <span data-ttu-id="7f24a-540">(SQL Server の 1 つのインスタンスで十分なサンドボックス環境に配置している場合を除きます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-540">(Unless you're deploying in a sandbox environment, where one instance of SQL Server is sufficient.</span></span> <span data-ttu-id="7f24a-541">高可用性シナリオをテストするため、サンドボックス環境に高可用性の SQL Server をインストールできます。)</span><span class="sxs-lookup"><span data-stu-id="7f24a-541">You may want to install SQL Server with high availability in sandbox enviornments to test high availability scenarios.)</span></span>

    <span data-ttu-id="7f24a-542">高可用性を備えた SQL Server を、SAN (ストレージ エリア ネットワーク) を含む SQL クラスターまたは Always-On 構成のいずれかとしてインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-542">You can install SQL Server with high availability either as SQL clusters that include a Storage Area Network (SAN) or in an Always-On configuration.</span></span> <span data-ttu-id="7f24a-543">データベース エンジン、SSRS、フルテキスト検索、および管理ツールがインストール済みであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-543">Verify that the Database Engine, SSRS, Full-Text Search, and Management Tools are already installed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f24a-544">Always-On が [初期データ同期ページの選択 (可用性グループ ウィザードで常に使用する)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) で説明されているとおりに設定され、[セカンダリ データベースを手動で準備する](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs) の指示に従っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-544">Make sure that Always-On is set up as described in [Select Initial Data Synchronization Page (Always On Availability Group Wizards)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards), and follow the instructions in [To Prepare Secondary Databases Manually](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs).</span></span>

2. <span data-ttu-id="7f24a-545">ドメイン ユーザーとして SQL サービスを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-545">Run the SQL service as a domain user.</span></span>
3. <span data-ttu-id="7f24a-546">Finance and Operations を構成するために CA から SSL 証明書を取得します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-546">Get an SSL certificate from a CA to configure Finance and Operations.</span></span> <span data-ttu-id="7f24a-547">テストの目的で、自己署名証明書を作成して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-547">For testing purposes, you can create and use a self-signed certificate.</span></span>

    <span data-ttu-id="7f24a-548">**クラスター化された SQL インスタンスの自己署名証明書**</span><span class="sxs-lookup"><span data-stu-id="7f24a-548">**Self-signed certificate for a Clustered SQL instance**</span></span>

    ```powershell
    New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
    ```

    <span data-ttu-id="7f24a-549">**Always-On SQL インスタンスの自己署名証明書**</span><span class="sxs-lookup"><span data-stu-id="7f24a-549">**Self-signed certificate for an Always-On SQL instance**</span></span>

    <span data-ttu-id="7f24a-550">テスト証明書の**手動**作成。</span><span class="sxs-lookup"><span data-stu-id="7f24a-550">**Manual** creation of test certificates:</span></span>
    ```powershell
    # https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

    # Manually create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
    # Run script on each node
    $computerName = $env:COMPUTERNAME.ToLower()
    $domain = $env:USERDNSDOMAIN.ToLower()
    $listenerName = 'dax7sqlaosqla'
    $cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'
    ```

4. <span data-ttu-id="7f24a-551">SQL サーバーで SSL を構成するには、証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-551">Use the certificate(s) to configure SSL on SQL Server.</span></span> <span data-ttu-id="7f24a-552">[Microsoft 管理コンソールを使用して SQL Server のインスタンスに対する SSL 暗号化を有効にする方法](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7f24a-552">Follow the steps in [How to enable SSL encryption for an instance of SQL Server by using Microsoft Management Console](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console).</span></span>
5. <span data-ttu-id="7f24a-553">SQL クラスターの各ノードに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-553">For each node of the SQL cluster, follow these steps.</span></span> <span data-ttu-id="7f24a-554">非アクティブなノードで変更を加えて、変更が行われた後フェール オーバーするようにしてください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-554">Make sure that you make the changes on the non-active node, and that you fail over to it after changes are made.</span></span>

    1. <span data-ttu-id="7f24a-555">LocalMachine\\My に証明書をインポートします。Always-On を設定していない限り、証明書は既にノードに存在します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-555">Import the certificate into LocalMachine\\My, unless you are setting up Always-On, in which case the certificate already exists on the node.</span></span>
    2. <span data-ttu-id="7f24a-556">SQL サービスを実行するために使用されるサービス アカウントに証明書のアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-556">Grant certificate permissions to the service account that is used to run the SQL service.</span></span> <span data-ttu-id="7f24a-557">Microsoft 管理コンソール (MMC) で証明書 (**certlm.msc**) を右クリックし、**タスク** \> **秘密キーの管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-557">In Microsoft Management Console (MMC), right-click the certificate (**certlm.msc**), and then select **Tasks** \> **Manage Private Keys**.</span></span>
    3. <span data-ttu-id="7f24a-558">証明書の拇印を HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate に追加します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-558">Add the certificate thumbprint to HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.</span></span>
    4. <span data-ttu-id="7f24a-559">Microsoft SQL Server 構成マネージャーで、**ForceEncryption** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-559">In Microsoft SQL Server Configuration Manager, set **ForceEncryption** to **Yes**.</span></span>

6. <span data-ttu-id="7f24a-560">証明書の公開鍵 (.cer ファイル) をエクスポートし、各 Service Fabric ノードの信頼できるルートにインストールします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-560">Export the public key of the certificate (the .cer file), and install it in the trusted root of each Service Fabric node.</span></span>

### <a name="configuredb"></a> <span data-ttu-id="7f24a-561">14. データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f24a-561">14. Configure the databases</span></span>

1. <span data-ttu-id="7f24a-562">[LCS](https://lcs.dynamics.com/v2) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-562">Sign in to [LCS](https://lcs.dynamics.com/v2).</span></span>

2. <span data-ttu-id="7f24a-563">ダッシュボードで、**共有アセット ライブラリ**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-563">On the dashboard, select the **Shared asset library** tile.</span></span>

3. <span data-ttu-id="7f24a-564">**モデル**タブで、必要なリリースのデモ データを選択し、zip ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-564">On the **Model** tab, select the demo data for the release you want and download the zip file.</span></span>

| <span data-ttu-id="7f24a-565">リリース</span><span class="sxs-lookup"><span data-stu-id="7f24a-565">Release</span></span> | <span data-ttu-id="7f24a-566">デモ データ</span><span class="sxs-lookup"><span data-stu-id="7f24a-566">Demo Data</span></span> |
|-------|------|
| <span data-ttu-id="7f24a-567">オンプレミスの一般提供 (GA) リリース</span><span class="sxs-lookup"><span data-stu-id="7f24a-567">On-premises General Availability (GA) release</span></span> | <span data-ttu-id="7f24a-568">Dynamics 365 for Operations (オンプレミス) - デモ データ</span><span class="sxs-lookup"><span data-stu-id="7f24a-568">Dynamics 365 for Operations (on-premises) - Demo data</span></span> |
| <span data-ttu-id="7f24a-569">オンプレミスのプラットフォーム更新プログラム 2017 年 11 月 11 日リリース</span><span class="sxs-lookup"><span data-stu-id="7f24a-569">On-premises Platform Update 11 Nov 2017 release</span></span> | <span data-ttu-id="7f24a-570">Dynamics 365 for Operations、Enterprise Edition (オンプレミス) - 更新プログラム 11 デモ データ</span><span class="sxs-lookup"><span data-stu-id="7f24a-570">Dynamics 365 for Operations, Enterprise edition (on-premises) - Update 11 Demo data</span></span> |

4. <span data-ttu-id="7f24a-571">zip ファイルには空のデモデータ .bak ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f24a-571">The zip file contains empty and demo data .bak files.</span></span> <span data-ttu-id="7f24a-572">必要に応じて、.bak ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-572">Select .bak file, based on your requirements.</span></span> <span data-ttu-id="7f24a-573">たとえば、デモ データが必要な場合は、AxBootstrapDB_Demodata.bak ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-573">For example, if you require demo data, download the AxBootstrapDB_Demodata.bak file.</span></span>

5. <span data-ttu-id="7f24a-574">infrastructure\ConfigTempate.xml のデータベース セクションが、次のように正しく構成されているか確認します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-574">Ensure the database section in the infrastructure\ConfigTempate.xml is configured correctly with the following:</span></span>
    1. <span data-ttu-id="7f24a-575">データベース名。</span><span class="sxs-lookup"><span data-stu-id="7f24a-575">The database name.</span></span>
    2. <span data-ttu-id="7f24a-576">db ファイルとログ設定。</span><span class="sxs-lookup"><span data-stu-id="7f24a-576">The db file and log settings.</span></span> <span data-ttu-id="7f24a-577">dbの設定は、指定された既定値以上にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-577">The db settings should not be lower than the defaults specified.</span></span>
    3. <span data-ttu-id="7f24a-578">LCS 共有アセット ライブラリからダウンロードされるバックアップ ファイルへのパス。</span><span class="sxs-lookup"><span data-stu-id="7f24a-578">The path to the backup file downloaded from LCS Shared Asset library.</span></span> <span data-ttu-id="7f24a-579">Finance and Operations データベースの既定の名前は AXDB です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-579">The default name for the Finance and Operations database is AXDB.</span></span>

   > [!WARNING]
   > 1. <span data-ttu-id="7f24a-580">SQL サービスを実行しているユーザーとスクリプトを実行しているユーザーは、バックアップ ファイルが格納されているフォルダーまたは共有に対して READ アクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-580">The user running the SQL service and the user running the scripts should have READ access on the folder or share where the backup file is located.</span></span>
   > 
   > 2. <span data-ttu-id="7f24a-581">同じ名前のデータベースが存在する場合は、データベースが再利用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-581">If a database with the same name exists, the database will be reused.</span></span>

6. <span data-ttu-id="7f24a-582">**インフラストラクチャ**フォルダーを SQL Server マシンにコピーし、権限を昇格した PowerShell ウィンドウでそのフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-582">Copy the **infrastructure** folder to the SQL Server machine and navigate to it in a PowerShell window with elevate privileges.</span></span>

#### <a name="configure-the-orchestratordata-database"></a><span data-ttu-id="7f24a-583">OrchestratorData データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f24a-583">Configure the OrchestratorData database</span></span>

1. <span data-ttu-id="7f24a-584">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-584">Execute the following script.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
   ```

   <span data-ttu-id="7f24a-585">スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="7f24a-585">The script will do the following:</span></span>
  
   - <span data-ttu-id="7f24a-586">**OrchestratorData** という名前の空のデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-586">Create an empty database named **OrchestratorData**.</span></span> <span data-ttu-id="7f24a-587">このデータベースは、オンプレミスのローカル エージェントによって配置を調整するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-587">This database is used by the on-premises local agent to orchestrate deployments.</span></span>
   - <span data-ttu-id="7f24a-588">データベースにローカル エージェント gMSA (svc-LocalAgent$) **db\_owner** アクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-588">Grant the local agent gMSA (svc-LocalAgent$) **db\_owner** permissions on the database.</span></span>

#### <a name="configure-the-finance-and-operations-database"></a><span data-ttu-id="7f24a-589">Finance and Operations データベースの構成</span><span class="sxs-lookup"><span data-stu-id="7f24a-589">Configure the Finance and Operations database</span></span>

1. <span data-ttu-id="7f24a-590">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-590">Execute the following scripts.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
   .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
   ```

   <span data-ttu-id="7f24a-591">**Initialize-Database.ps1** スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="7f24a-591">The **Initialize-Database.ps1** script will do the following:</span></span>

   1. <span data-ttu-id="7f24a-592">指定されたバックアップ ファイルからデータベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-592">Restore the database from the specified backup file.</span></span>
   2. <span data-ttu-id="7f24a-593">SQL 認証が有効になっている新しいユーザーを作成します (axdbadmin)。</span><span class="sxs-lookup"><span data-stu-id="7f24a-593">Create a new user that has SQL authentication enabled (axdbadmin).</span></span>
   3. <span data-ttu-id="7f24a-594">AXDB の次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-594">Map users to database roles based on the following table for AXDB.</span></span>

      | <span data-ttu-id="7f24a-595">ユーザー</span><span class="sxs-lookup"><span data-stu-id="7f24a-595">User</span></span>            | <span data-ttu-id="7f24a-596">種類</span><span class="sxs-lookup"><span data-stu-id="7f24a-596">Type</span></span>    | <span data-ttu-id="7f24a-597">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="7f24a-597">Database role</span></span> |
      |-----------------|---------|---------------|
      | <span data-ttu-id="7f24a-598">svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="7f24a-598">svc-AXSF$</span></span>       | <span data-ttu-id="7f24a-599">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-599">gMSA</span></span>    | <span data-ttu-id="7f24a-600">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7f24a-600">db\_owner</span></span>     |
      | <span data-ttu-id="7f24a-601">svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="7f24a-601">svc-LocalAgent$</span></span> | <span data-ttu-id="7f24a-602">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-602">gMSA</span></span>    | <span data-ttu-id="7f24a-603">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7f24a-603">db\_owner</span></span>     |
      | <span data-ttu-id="7f24a-604">svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="7f24a-604">svc-FRPS$</span></span>       | <span data-ttu-id="7f24a-605">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-605">gMSA</span></span>    | <span data-ttu-id="7f24a-606">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7f24a-606">db\_owner</span></span>     |
      | <span data-ttu-id="7f24a-607">svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="7f24a-607">svc-FRAS$</span></span>       | <span data-ttu-id="7f24a-608">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-608">gMSA</span></span>    | <span data-ttu-id="7f24a-609">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7f24a-609">db\_owner</span></span>     |
      | <span data-ttu-id="7f24a-610">axdbadmin</span><span class="sxs-lookup"><span data-stu-id="7f24a-610">axdbadmin</span></span>       | <span data-ttu-id="7f24a-611">SqlUser</span><span class="sxs-lookup"><span data-stu-id="7f24a-611">SqlUser</span></span> | <span data-ttu-id="7f24a-612">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7f24a-612">db\_owner</span></span>     |


   4. <span data-ttu-id="7f24a-613">TempDB の次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-613">Map users to database roles based on the following table for TempDB.</span></span>

      | <span data-ttu-id="7f24a-614">ユーザー</span><span class="sxs-lookup"><span data-stu-id="7f24a-614">User</span></span>            | <span data-ttu-id="7f24a-615">種類</span><span class="sxs-lookup"><span data-stu-id="7f24a-615">Type</span></span>    | <span data-ttu-id="7f24a-616">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="7f24a-616">Database role</span></span> |
      |-----------------|---------|---------------|
      | <span data-ttu-id="7f24a-617">svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="7f24a-617">svc-AXSF$</span></span>       | <span data-ttu-id="7f24a-618">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-618">gMSA</span></span>    | <span data-ttu-id="7f24a-619">db_datareader, db_datawriter, db_ddladmin</span><span class="sxs-lookup"><span data-stu-id="7f24a-619">db_datareader, db_datawriter, db_ddladmin</span></span>     |
      | <span data-ttu-id="7f24a-620">axdbadmin</span><span class="sxs-lookup"><span data-stu-id="7f24a-620">axdbadmin</span></span>       | <span data-ttu-id="7f24a-621">SqlUser</span><span class="sxs-lookup"><span data-stu-id="7f24a-621">SqlUser</span></span> | <span data-ttu-id="7f24a-622">db_datareader, db_datawriter, db_ddladmin</span><span class="sxs-lookup"><span data-stu-id="7f24a-622">db_datareader, db_datawriter, db_ddladmin</span></span>     |

   <span data-ttu-id="7f24a-623">**Configure-Database.ps1** スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="7f24a-623">The **Configure-Database.ps1** script will do the following:</span></span>

    1. <span data-ttu-id="7f24a-624">READ_COMMITTED_SNAPSHOT ON を設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-624">Set READ_COMMITTED_SNAPSHOT ON</span></span>
    2. <span data-ttu-id="7f24a-625">ALLOW_SNAPSHOT_ISOLATION ON を設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-625">Set ALLOW_SNAPSHOT_ISOLATION ON</span></span>
    3. <span data-ttu-id="7f24a-626">指定したデータベース ファイルとログの設定を設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-626">Set the specified database file and log settings</span></span>
    4. <span data-ttu-id="7f24a-627">サーバー状態の表示を axdbadmin に付与</span><span class="sxs-lookup"><span data-stu-id="7f24a-627">GRANT VIEW SERVER STATE TO axdbadmin</span></span>
    5. <span data-ttu-id="7f24a-628">サーバー状態の表示を [contoso\svc AXSF$] に付与</span><span class="sxs-lookup"><span data-stu-id="7f24a-628">GRANT VIEW SERVER STATE TO [contoso\svc-AXSF$]</span></span>

2. <span data-ttu-id="7f24a-629">データベース ユーザーをリセットするには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-629">Run the following command to reset the database users.</span></span>

    ```powershell
    .\Reset-DatabaseUsers.ps1 -DatabaseServer '<FQDN of the SQL server>' -DatabaseName '<AX database name>'
    ```

#### <a name="configure-the-financial-reporting-database"></a><span data-ttu-id="7f24a-630">財務レポート データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f24a-630">Configure the Financial Reporting database</span></span>

1. <span data-ttu-id="7f24a-631">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-631">Execute the following script.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName MR
   ```

   <span data-ttu-id="7f24a-632">スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="7f24a-632">The script will do the following:</span></span>
   1. <span data-ttu-id="7f24a-633">**FinancialReporting** という名前の空のデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-633">Create an empty database named **FinancialReporting**.</span></span>
   2. <span data-ttu-id="7f24a-634">次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-634">Map the users to database roles based on the following table.</span></span>

      | <span data-ttu-id="7f24a-635">ユーザー</span><span class="sxs-lookup"><span data-stu-id="7f24a-635">User</span></span>            | <span data-ttu-id="7f24a-636">種類</span><span class="sxs-lookup"><span data-stu-id="7f24a-636">Type</span></span> | <span data-ttu-id="7f24a-637">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="7f24a-637">Database role</span></span> |
      |-----------------|------|---------------|
      | <span data-ttu-id="7f24a-638">svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="7f24a-638">svc-LocalAgent$</span></span> | <span data-ttu-id="7f24a-639">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-639">gMSA</span></span> | <span data-ttu-id="7f24a-640">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7f24a-640">db\_owner</span></span>     |
      | <span data-ttu-id="7f24a-641">svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="7f24a-641">svc-FRPS$</span></span>       | <span data-ttu-id="7f24a-642">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-642">gMSA</span></span> | <span data-ttu-id="7f24a-643">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7f24a-643">db\_owner</span></span>     |
      | <span data-ttu-id="7f24a-644">svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="7f24a-644">svc-FRAS$</span></span>       | <span data-ttu-id="7f24a-645">gMSA</span><span class="sxs-lookup"><span data-stu-id="7f24a-645">gMSA</span></span> | <span data-ttu-id="7f24a-646">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7f24a-646">db\_owner</span></span>     |

### <a name="encryptcred"></a> <span data-ttu-id="7f24a-647">15. 資格情報の暗号化</span><span class="sxs-lookup"><span data-stu-id="7f24a-647">15. Encrypt credentials</span></span>

1. <span data-ttu-id="7f24a-648">任意のクライアント マシンで、LocalMachine\\My certificate store に暗号化証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-648">On any client machine, install the encipherment certificate in the LocalMachine\\My certificate store.</span></span>
2. <span data-ttu-id="7f24a-649">現在のユーザーにこの証明書の秘密キーへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-649">Grant the current user read access to the private key of this certificate.</span></span>
3. <span data-ttu-id="7f24a-650">次のようにして、Credentials.json ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-650">Create the Credentials.json file, as shown here.</span></span>

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

    - <span data-ttu-id="7f24a-651">**AccountPassword** は、AOS ドメインユーザー (contoso\\axserviceuser) の暗号化されたドメイン ユーザー パスワードです。</span><span class="sxs-lookup"><span data-stu-id="7f24a-651">**AccountPassword** is the encrypted domain user password for the AOS domain user (contoso\\axserviceuser).</span></span>
    - <span data-ttu-id="7f24a-652">**SqlUser** は、Finance and Operations データベース (AXDB) にアクセスできる暗号化された SQL ユーザー (axdbadmin) で、**SqlPassword** は暗号化された SQL パスワードです。</span><span class="sxs-lookup"><span data-stu-id="7f24a-652">**SqlUser** is the encrypted SQL user (axdbadmin) that has access to the Finance and Operations database (AXDB), and **SqlPassword** is the encrypted SQL password.</span></span>

4. <span data-ttu-id="7f24a-653">.json ファイルを SMB ファイル共有、\\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json にコピーします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-653">Copy the .json file to the SMB file share, \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.</span></span>
5. <span data-ttu-id="7f24a-654">暗号化された値で Credentials.json ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-654">Update the Credentials.json file with encrypted values.</span></span>

    ```powershell
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | Set-Clipboard
    ```

### <a name="setupssis"></a> <span data-ttu-id="7f24a-655">16. SSIS の設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-655">16. Set up SSIS</span></span>

<span data-ttu-id="7f24a-656">データ管理と統合ワークロードを有効にするには、各 AOS 仮想マシンに SSIS をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-656">To enable Data management and Integration workloads, SSIS must be installed on each of the AOS virtual machines.</span></span> <span data-ttu-id="7f24a-657">各 AOS 仮想マシン上で、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-657">Complete the following steps on each AOS virtual machine.</span></span>

1. <span data-ttu-id="7f24a-658">マシンに SSIS インストールへのアクセス許可があることを確認し、SSIS セットアップ ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-658">Verify that the machine has access to the SSIS installation and open the SSIS Setup Wizard.</span></span>
2. <span data-ttu-id="7f24a-659">**機能の選択**ウィンドウの**機能**ウィンドウで、**Integration Services** および **SQL クライアント接続 SDK** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-659">In the **Feature Selection** window, in the **Features** pane, select the **Integration Services** and **SQL Client Connectivity SDK** check boxes.</span></span>
3. <span data-ttu-id="7f24a-660">セットアップを完了し、インストールが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-660">Complete the setup and verify that the installation was successful.</span></span>

<span data-ttu-id="7f24a-661">詳細については、[統合サービスのインストール](https://docs.microsoft.com/en-us/sql/integration-services/install-windows/install-integration-services) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-661">For more information, see [Install integration services](https://docs.microsoft.com/en-us/sql/integration-services/install-windows/install-integration-services).</span></span>

### <a name="setupssrs"></a> <span data-ttu-id="7f24a-662">17. SSRS の設定</span><span class="sxs-lookup"><span data-stu-id="7f24a-662">17. Set up SSRS</span></span>

1. <span data-ttu-id="7f24a-663">開始する前に、このトピックの冒頭に記載されている前提条件がインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-663">Before you begin, make sure that the prerequisites that are listed at the beginning of this topic are installed.</span></span>
2. <span data-ttu-id="7f24a-664">[オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション](../analytics/configure-ssrs-on-premises.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7f24a-664">Follow the steps in [Configure SQL Server Reporting Services for an on-premises deployment](../analytics/configure-ssrs-on-premises.md).</span></span>

### <a name="configureadfs"></a><span data-ttu-id="7f24a-665">18. AD FS のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f24a-665">18. Configure AD FS</span></span>

<span data-ttu-id="7f24a-666">この手順を完了する前に、AD FS を Windows Server 2016 に展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-666">Before you can complete this procedure, AD FS must be deployed on Windows Server 2016.</span></span> <span data-ttu-id="7f24a-667">AD FS を展開する方法については、[Windows Server 2016 配置ガイドおよび 2012 R2 AD FS 配置ガイド](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-667">For information about how to deploy AD FS, see [Deployment Guide Windows Server 2016 and 2012 R2 AD FS Deployment Guide](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).</span></span>

<span data-ttu-id="7f24a-668">Finance and Operations では、AD FS の既定で標準のコンフィギュレーション以外の追加のコンフィギュレーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-668">Finance and Operations requires additional configuration beyond the default out-of-box configuration of AD FS.</span></span> <span data-ttu-id="7f24a-669">以下の手順では、Windows PowerShell は AD FS ロール サービスがインストールされているマシン上で実行されます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-669">For the following steps, Windows PowerShell runs on a machine where the AD FS role service is installed.</span></span> <span data-ttu-id="7f24a-670">ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-670">The user account must have enough permissions to administer AD FS.</span></span> <span data-ttu-id="7f24a-671">たとえば、ユーザーには、ドメイン管理者アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-671">For example, the user must have a domain administrator account.</span></span>

1. <span data-ttu-id="7f24a-672">AD FS 識別子を構成して、AD FS トークン発行者と一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-672">Configure the AD FS identifier so that it matches the AD FS token issuer.</span></span>

    ```powershell
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. <span data-ttu-id="7f24a-673">混在環境用に AD FS を構成していない限り、イントラネット認証接続用に Windows 統合認証 (WIA) を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-673">You should disable Windows Integrated Authentication (WIA) for intranet authentication connections, unless you've configured AD FS for mixed environments.</span></span> <span data-ttu-id="7f24a-674">WIA を AD FS で使用できるように構成する方法の詳細については、[AD FS で Windows 統合認証 (WIA) を使用するようにブラウザを構成する](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-674">For more information about how to configure WIA so that it can be used with AD FS, see [Configure browsers to use Windows Integrated Authentication (WIA) with AD FS](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).</span></span>

    ```powershell
    Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
    ```

3. <span data-ttu-id="7f24a-675">サインインの場合、ユーザーの電子メール アドレスは許容される認証入力でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7f24a-675">For sign-in, the user's email address must be an acceptable authentication input.</span></span>

    ```powershell
    Add-Type -AssemblyName System.Net
    $fqdn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
    $domainName = $fqdn.Substring($fqdn.IndexOf('.')+1)
    Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
    ```

<span data-ttu-id="7f24a-676">AD FS が認証を交換するために Finance and Operations を信頼するためには、AD FS アプリケーション グループの下の AD FS にさまざまなアプリケーション エントリを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-676">In order for AD FS to trust Finance and Operations for the exchange of authentication, various application entries must be registered in AD FS under an AD FS application group.</span></span> <span data-ttu-id="7f24a-677">設定プロセスをスピードアップし、エラーを減らすために、次のスクリプトを使用して登録します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-677">To speed up the setup process and help reduce errors, you can use the following script for registration.</span></span> <span data-ttu-id="7f24a-678">Publish-ADFSApplicationGroup.ps1 スクリプトと D365FO-OP ディレクトリを、AD FS ロール サービスがインストールされているマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-678">Copy the Publish-ADFSApplicationGroup.ps1 script and D365FO-OP directory to a machine where the AD FS role service is installed.</span></span> <span data-ttu-id="7f24a-679">次に、AD FS を管理するための十分なアクセス許可を持つユーザー アカウントを使用してスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-679">Then run the script by using a user account that has enough permissions to administer AD FS.</span></span> <span data-ttu-id="7f24a-680">(たとえば、管理者アカウントを使用します。)</span><span class="sxs-lookup"><span data-stu-id="7f24a-680">(For example, use an administrator account.)</span></span>

<span data-ttu-id="7f24a-681">スクリプトの使用方法の詳細については、スクリプトに記載されているドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-681">For more information about how to use the script, see the documentation that is listed in the script.</span></span> <span data-ttu-id="7f24a-682">後の手順の LCS でこの情報が必要となるため、出力に指定されているクライアント ID を書き留めておいてください。</span><span class="sxs-lookup"><span data-stu-id="7f24a-682">Make a note of the client IDs that are specified in the output, because you will need this information in LCS in a later step.</span></span> <span data-ttu-id="7f24a-683">クライアント ID を紛失した場合、AD FS がインストールされているコンピューターにログインし、**サーバー マネージャー** \> **ツール** \> **AD FS の管理** \> **アプリケーション グループ** \> **Microsoft Dynamics 365 for Operations On-premises** を開き、ネイティブ アプリケーションでクライアント ID を見つけます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-683">Should you lose the client IDs, log in to the machine which has AD FS installed, open **Server Manager** \> **Tools** \> **AD FS Management** \> **Application Groups** \> **Microsoft Dynamics 365 for Operations On-premises** and find the client IDs under the native applications.</span></span>

```powershell
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
```

![アプリケーション グループのプロパティ](./media/OPSetup_05_ApplicatioGroupProperties.png)

<span data-ttu-id="7f24a-685">最後に、**AOSNodeType** タイプの Service Fabric ノード上の AD FS OpenID コンフィギュレーション URL にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-685">Finally, make sure that you can access the AD FS OpenID Configuration URL on a Service Fabric node of the **AOSNodeType** type.</span></span> <span data-ttu-id="7f24a-686">このチェックを行うには、Web ブラウザーで `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` を開きます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-686">To perform this check, try to open `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` in a web browser.</span></span> <span data-ttu-id="7f24a-687">サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていません。</span><span class="sxs-lookup"><span data-stu-id="7f24a-687">If you receive a message that states that the site isn't secure, you haven't added your AD FS SSL certificate to the Trusted Root Certification Authorities store.</span></span> <span data-ttu-id="7f24a-688">この手順については、「AD FS 展開ガイド」で説明されています。</span><span class="sxs-lookup"><span data-stu-id="7f24a-688">This step is described in the AD FS deployment guide.</span></span>

<span data-ttu-id="7f24a-689">URL に正常にアクセスすると、AD FS コンフィギュレーションを含む JavaScript Object Notation (JSON) ファイルが返され、AD FS URL が信頼されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-689">If you successfully access the URL, a JavaScript Object Notation (JSON) file is returned that contains your AD FS configuration, and you will see that your AD FS URL is trusted.</span></span>

<span data-ttu-id="7f24a-690">これで、インフラストラクチャの設定を完了しました。</span><span class="sxs-lookup"><span data-stu-id="7f24a-690">You've now completed the setup of the infrastructure.</span></span> <span data-ttu-id="7f24a-691">次のセクションでは、[LCS](https://lcs.dynamics.com) にアクセスしてコネクタを設定し、Finance and Operations 環境を配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-691">The following sections describe how to navigate to [LCS](https://lcs.dynamics.com) to set up your connector and deploy your Finance and Operations environment.</span></span>

### <a name="configureconnector"></a> <span data-ttu-id="7f24a-692">19. コネクタのコンフィギュレーションと、オンプレミスのローカル エージェントのインストール</span><span class="sxs-lookup"><span data-stu-id="7f24a-692">19. Configure a connector and install an on-premises local agent</span></span>

1. <span data-ttu-id="7f24a-693">[LCS](https://lcs.dynamics.com/) にサインインし、オンプレミスの実装プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f24a-693">Sign in to [LCS](https://lcs.dynamics.com/), and open the on-premises implementation project.</span></span>
2. <span data-ttu-id="7f24a-694">ハンバーガー メニューで、**プロジェクト設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-694">On the hamburger menu, select **Project settings**.</span></span>

    ![プロジェクト設定コマンド](./media/OPSetup_06_ProjectSettings.png)

3. <span data-ttu-id="7f24a-696">**オンプレミス コネクタ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-696">Select **On-premises connectors**.</span></span>
4. <span data-ttu-id="7f24a-697">新しいコネクタを作成するには、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-697">Select **Add** to create a new connector.</span></span>
5. <span data-ttu-id="7f24a-698">**ホスト インフラストラクチャ設定** タブで、エージェント インストーラーをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-698">On the **Setup host infrastructure** tab, download the agent installer.</span></span>

    ![[ホスト インフラストラクチャ設定] タブで、エージェント インストーラー ボタンをダウンロードする](./media/OPSetup_07_DownloadAgentInstaller.png)
6. <span data-ttu-id="7f24a-700">zip ファイルがブロックされていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-700">Verify that the zip file is unblocked.</span></span> <span data-ttu-id="7f24a-701">ファイルを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-701">Right-click the file, and then select **Properties**.</span></span> <span data-ttu-id="7f24a-702">ダイアログ ボックスで**ブロック解除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-702">In the dialog box, select **Unblock**.</span></span>
7. <span data-ttu-id="7f24a-703">**OrchestratorType** タイプの Service Fabric ノードの 1 つでエージェント インストーラーを解凍します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-703">Unzip the agent installer on one of the Service Fabric nodes of the **OrchestratorType** type.</span></span>
8. <span data-ttu-id="7f24a-704">**構成エージェント** タブで、コンフィギュレーションの設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-704">On the **Configure agent** tab, enter the configuration settings.</span></span>
9. <span data-ttu-id="7f24a-705">コンフィギュレーションを保存し、**コンフィギュレーションのダウンロード** を選択して、localagent-config.json コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-705">Save the configuration, and then select **Download configurations** to download the localagent-config.json configuration file.</span></span>

    ![[エージェントの設定] タブの [コンフィギュレーションのダウンロード] ボタン](./media/OPSetup_08_DownloadConfigurations.png)

10. <span data-ttu-id="7f24a-707">localagent-config.json ファイルを、エージェント インストーラー パッケージが配置されているマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-707">Copy the localagent-config.json file to the machine where the agent installer package is located.</span></span>
11. <span data-ttu-id="7f24a-708">**コマンド プロンプト** ウィンドウで、エージェント インストーラーを含むフォルダーに移動して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-708">In a **Command Prompt** window, run the following command by navigating to the folder that contains the agent installer.</span></span>

    ```powershell
    LocalAgentCLI.exe Install <path of config.json>
    ```

    > [!NOTE]
    > <span data-ttu-id="7f24a-709">このコマンドを実行するユーザーは、OrchestratorData データベースに対して **db\_owner** のアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-709">The user who runs this command must have **db\_owner** permissions on the OrchestratorData database.</span></span>

12. <span data-ttu-id="7f24a-710">ローカル エージェントが正常にインストールされると、LCS のオンプレミス コネクタに戻るようにします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-710">After the local agent is successfully installed, navigate back to your on-premises connector in LCS.</span></span>
13. <span data-ttu-id="7f24a-711">**設定の検証**タブで、**メッセージ エージェント**を選択して、ローカル エージェントへの LCS 接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="7f24a-711">On the **Validate setup** tab, select **Message agent** to test for LCS connectivity to your local agent.</span></span> <span data-ttu-id="7f24a-712">接続が正常に確立されると、ページは下図のようになります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-712">When a connection is successfully established, the page will resemble the following illustration.</span></span>

    ![エージェントの検証](./media/ValidateAgent.PNG)

### <a name="deploy"></a> <span data-ttu-id="7f24a-714">20. LCS から Finance and Operations (オンプレミス) 環境を配置する</span><span class="sxs-lookup"><span data-stu-id="7f24a-714">20. Deploy your Finance and Operations (on-premises) environment from LCS</span></span>

1. <span data-ttu-id="7f24a-715">LCS で、オンプレミス プロジェクトに移動し、**環境** > **サンドボックス**に移動してから**構成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-715">In LCS, navigate to your on-premises project, go to **Environment** > **Sandbox**, and then select **Configure**.</span></span>
2. <span data-ttu-id="7f24a-716">新しい展開では、環境のトポロジを選択し、展開を開始するウィザードを完了します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-716">For new deployments, select your environment topology, and then complete the wizard to start your deployment.</span></span>
3. <span data-ttu-id="7f24a-717">既存の展開がある場合は、「[設置環境を再配置](redeploy-on-prem.md)」というトピックを参照します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-717">If you have an existing deployment, see the topic [Redeploy an on-premises environment](redeploy-on-prem.md).</span></span>
4. <span data-ttu-id="7f24a-718">ローカル エージェントは配置要求を受け取り、配置を開始し、環境の準備ができたら LCS に再度通知します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-718">The local agent will pick up the deployment request, start the deployment, and communicate back to LCS when the environment is ready.</span></span>

<span data-ttu-id="7f24a-719">展開に失敗した場合、LCS のお客様の環境では、**再設定**ボタンは利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="7f24a-719">If the deployment fails, the **Reconfigure** button will become available for your environment in LCS.</span></span> <span data-ttu-id="7f24a-720">基になる問題を修正し、**再コンフィギュレーション**をクリックして、任意のコンフィギュレーションの変更を更新し、**配置**をクリックして配置を再試行します。</span><span class="sxs-lookup"><span data-stu-id="7f24a-720">Fix the underlying issue, click **Reconfigure**, update any configuration changes, and click **Deploy** to retry the deployment.</span></span>

### <a name="connect"></a> <span data-ttu-id="7f24a-721">22. Finance and Operations (オンプレミス) 環境に接続する</span><span class="sxs-lookup"><span data-stu-id="7f24a-721">21. Connect to your Finance and Operations (on-premises) environment</span></span>

<span data-ttu-id="7f24a-722">ブラウザーで、https://[yourD365FOdomain]/namespaces/AXSF に移動し、そこでは yourD365FOdomain がこのドキュメントの[ドメイン名と DNS ゾーンの計画](#plandomain)セクションで定義したドメイン名です。</span><span class="sxs-lookup"><span data-stu-id="7f24a-722">In your browser, navigate to https://[yourD365FOdomain]/namespaces/AXSF, where yourD365FOdomain is the domain name that you defined in the [Plan your domain name and DNS zones](#plandomain) section of this document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f24a-723">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="7f24a-723">Additional resources</span></span>
- [<span data-ttu-id="7f24a-724">オンプレミス配置への更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="7f24a-724">Apply updates to an on-premises deployment</span></span>](apply-updates-on-premises.md)
- [<span data-ttu-id="7f24a-725">オンプレミス配置の再配置</span><span class="sxs-lookup"><span data-stu-id="7f24a-725">Redeploy an on-premises deployment</span></span>](redeploy-on-prem.md)

