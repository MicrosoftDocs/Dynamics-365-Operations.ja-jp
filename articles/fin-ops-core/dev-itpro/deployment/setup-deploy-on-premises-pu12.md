---
title: オンプレミス環境の設定と配置 (Platform update 12 以降)
description: このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) プラットフォーム更新プログラム 12 以降を計画、設定、展開する方法について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-11-30
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 93ba63f9e92ca546c3417480d21aee100ecb4d02
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627576"
---
# <a name="set-up-and-deploy-on-premises-environments-platform-update-12-and-later"></a><span data-ttu-id="17e3d-103">オンプレミス環境の設定と配置 (Platform update 12 以降)</span><span class="sxs-lookup"><span data-stu-id="17e3d-103">Set up and deploy on-premises environments (Platform update 12 and later)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17e3d-104">このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) プラットフォーム更新プログラム 12 以降を計画、設定、展開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-104">This topic provides information about how to plan, set up, and deploy Dynamics 365 Finance + Operations (on-premises) with Platform update 12 and later.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17e3d-105">このトピックは、プラットフォーム更新プログラム 12 以降にオンプレミス環境を展開する場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-105">This topic applies only to deploying on-premises environments on Platform update 12 and later.</span></span> <span data-ttu-id="17e3d-106">プラットフォーム更新プログラム 8 および 11 のインストールへの配置方法については、[オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 8 および 11)](setup-deploy-on-premises-pu8-pu11.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-106">For information about deploying to Platform update 8 or Platform update 11 installations, see [Set up and deploy on-premises environments (Platform updates 8 and 11)](setup-deploy-on-premises-pu8-pu11.md).</span></span> 

<span data-ttu-id="17e3d-107">[ローカル ビジネス データ Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13595809&view=all) が利用可能です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-107">The [Local Business Data Yammer group](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13595809&view=all) is available.</span></span> <span data-ttu-id="17e3d-108">オンプレミス展開に関する質問またはフィードバックをそこに投稿することができます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-108">You can post questions or feedback you may have about the on-premises deployment there.</span></span>

<span data-ttu-id="17e3d-109">このトピックの内容に関する質問やフィードバックがある場合は、このページ下の**コメント**セクションに転記してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-109">If you have questions or feedback about the content in this topic, please post them in the **Comments** section at the bottom of this page.</span></span>

## <a name="finance--operations-components"></a><span data-ttu-id="17e3d-110">Finance + Operations のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="17e3d-110">Finance + Operations components</span></span>

<span data-ttu-id="17e3d-111">Finance + Operations アプリケーションは、次の 3 つの主要なコンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="17e3d-111">The Finance + Operations application consists of three main components:</span></span>

- <span data-ttu-id="17e3d-112">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="17e3d-112">Application Object Server (AOS)</span></span>
- <span data-ttu-id="17e3d-113">ビジネス インテリジェンス (BI)</span><span class="sxs-lookup"><span data-stu-id="17e3d-113">Business Intelligence (BI)</span></span>
- <span data-ttu-id="17e3d-114">財務レポート/管理レポーター</span><span class="sxs-lookup"><span data-stu-id="17e3d-114">Financial Reporting/Management Reporter</span></span>

<span data-ttu-id="17e3d-115">これらのコンポーネントは、次のシステム ソフトウェアによって異なります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-115">These components depend on the following system software:</span></span>

- <span data-ttu-id="17e3d-116">Microsoft Windows Server 2016 (英語 OS のインストールのみがサポートされます)</span><span class="sxs-lookup"><span data-stu-id="17e3d-116">Microsoft Windows Server 2016 (only English OS installations are supported)</span></span>
- <span data-ttu-id="17e3d-117">以下の特徴を有する Microsoft SQL Server2016 SP1:</span><span class="sxs-lookup"><span data-stu-id="17e3d-117">Microsoft SQL Server 2016 SP1, which has the following features:</span></span>
  - <span data-ttu-id="17e3d-118">フルテキスト インデックス検索が有効にされている。</span><span class="sxs-lookup"><span data-stu-id="17e3d-118">Full-text index search is enabled.</span></span>
  - <span data-ttu-id="17e3d-119">SQL Server Reporting Services (SSRS) - これは BI 仮想マシンに配置されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-119">SQL Server Reporting Services (SSRS) - This is deployed on BI virtual machines.</span></span>
  - <span data-ttu-id="17e3d-120">SQL Server Integration Services (SSIS) - これは AOS 仮想マシンに配置されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-120">SQL Server Integration Services (SSIS) - This is deployed on AOS virtual machines.</span></span>

    > [!WARNING]
    > <span data-ttu-id="17e3d-121">完全なテキスト検索を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-121">Full Text Search must be enabled.</span></span>

- <span data-ttu-id="17e3d-122">SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="17e3d-122">SQL Server Management Studio</span></span>
- <span data-ttu-id="17e3d-123">スタンドアロン Microsoft Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="17e3d-123">Standalone Microsoft Azure Service Fabric</span></span>
- <span data-ttu-id="17e3d-124">Microsoft Windows PowerShell 5.0 以降</span><span class="sxs-lookup"><span data-stu-id="17e3d-124">Microsoft Windows PowerShell 5.0 or later</span></span>
- <span data-ttu-id="17e3d-125">Windows Server 2016 での Active Directory Federation Services (AD FS)</span><span class="sxs-lookup"><span data-stu-id="17e3d-125">Active Directory Federation Services (AD FS) on Windows Server 2016</span></span>
- <span data-ttu-id="17e3d-126">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="17e3d-126">Domain controller</span></span>

  > [!WARNING]
  > <span data-ttu-id="17e3d-127">ドメイン コントローラは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-127">The domain controller must be Microsoft Windows Server 2012 R2 or later and must have a domain functional level of 2012 R2 or more.</span></span>    <span data-ttu-id="17e3d-128">ドメイン機能レベルの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-128">For more information about domain functional levels, see the following topics:</span></span>
  >   - <span data-ttu-id="17e3d-129">[Active Directory 機能レベルとは](https://technet.microsoft.com/library/cc787290(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="17e3d-129">[What Are Active Directory Functional Levels](https://technet.microsoft.com/library/cc787290(v=ws.10).aspx)</span></span>
  >   - <span data-ttu-id="17e3d-130">[Active Directory ドメイン サービス機能のレベルを理解する](https://technet.microsoft.com/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="17e3d-130">[Understanding Active Directory Domain Services Functional Levels](https://technet.microsoft.com/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="17e3d-131">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="17e3d-131">Lifecycle Services</span></span>

<span data-ttu-id="17e3d-132">Finance + Operations のビットは、Microsoft Dynamics Lifecycle Services (LCS) を通じて配布されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-132">Finance + Operations bits are distributed through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="17e3d-133">配置する前に、[エンタープライズ契約](https://www.microsoft.com/Licensing/licensing-programs/enterprise.aspx) チャンネルを通じてライセンス キーを購入し、LCS でオンプレミス プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-133">Before you can deploy, you must purchase license keys through the [Enterprise Agreements](https://www.microsoft.com/Licensing/licensing-programs/enterprise.aspx) channel and set up an on-premises project in LCS.</span></span> <span data-ttu-id="17e3d-134">LCS からのみ配置を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-134">Deployments can be initiated only through LCS.</span></span> <span data-ttu-id="17e3d-135">LCS でオンプレミス プロジェクトを設定する方法の詳細については、[Lifecycle Services でのオンプレミス プロジェクトの作成](../lifecycle-services/lbd-create-lcs-on-prem-project.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-135">For more information about how to set up on-premises projects in LCS, see [Create an on-premises project in Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).</span></span>

## <a name="authentication"></a><span data-ttu-id="17e3d-136">認証</span><span class="sxs-lookup"><span data-stu-id="17e3d-136">Authentication</span></span>

<span data-ttu-id="17e3d-137">オンプレミス アプリケーションは AD FS で動作します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-137">The on-premises application works with AD FS.</span></span> <span data-ttu-id="17e3d-138">LCS と対話するには、Azure Active Directory (AAD) も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-138">To interact with LCS, you must also configure Azure Active Directory (AAD).</span></span> <span data-ttu-id="17e3d-139">配置を完了し、LCS ローカル エージェントを構成するには、AAD が必要です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-139">To complete the deployment and configure the LCS Local agent, you will need AAD.</span></span> <span data-ttu-id="17e3d-140">AAD テナントがまだない場合は、AAD によって提供されるオプションのいずれかを使用して無料のものを取得できます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-140">If you do not already have an AAD tenant, you can get one for free by using one of the options provided by AAD.</span></span> <span data-ttu-id="17e3d-141">詳細については、[Azure Active Directory テナントを取得する方法](https://docs.microsoft.com/azure/active-directory/develop/active-directory-howto-tenant) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-141">For more information, see [How to get an Azure Active Directory tenant](https://docs.microsoft.com/azure/active-directory/develop/active-directory-howto-tenant).</span></span>

## <a name="standalone-service-fabric"></a><span data-ttu-id="17e3d-142">Standalone Service Fabric</span><span class="sxs-lookup"><span data-stu-id="17e3d-142">Standalone Service Fabric</span></span>

<span data-ttu-id="17e3d-143">Finance + Operations は スタンドアロン Service Fabric を使用します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-143">Finance + Operations uses standalone Service Fabric.</span></span> <span data-ttu-id="17e3d-144">詳細については、[Service Fabric ドキュメント](/azure/service-fabric/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-144">For more information, see the [Service Fabric documentation](/azure/service-fabric/).</span></span>

<span data-ttu-id="17e3d-145">Finance + Operations の設定は、Service Fabric (SF) 内に一連のアプリケーションを配置します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-145">Setup of Finance + Operations will deploy a set of applications inside Service Fabric (SF).</span></span> <span data-ttu-id="17e3d-146">展開中に、クラスター内の各ノードは、次のいずれかのノード タイプを持つように構成によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-146">During deployment, each node in the cluster will be defined via configuration to have one of the following node types:</span></span>

- <span data-ttu-id="17e3d-147">**AOSNodeType** - アプリケーション オブジェクト サーバー (ビジネス ロジック) をホストします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-147">**AOSNodeType** - Hosts the application object server (business logic).</span></span>
- <span data-ttu-id="17e3d-148">**OrchestratorType** - Service Fabric のプライマリ ノードとして機能し、配置およびサービスロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-148">**OrchestratorType** - Functions as Service Fabric primary nodes, and hosts deployment- and servicing logic.</span></span>
- <span data-ttu-id="17e3d-149">**ReportServerType** - SSRS およびレポート ロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-149">**ReportServerType** - Hosts SSRS and reporting logic.</span></span>
- <span data-ttu-id="17e3d-150">**MRType** - 管理レポート ロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-150">**MRType** - Hosts management reporting logic.</span></span>

## <a name="infrastructure"></a><span data-ttu-id="17e3d-151">インフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="17e3d-151">Infrastructure</span></span>

<span data-ttu-id="17e3d-152">Finance + Operations には、非 Microsoft 仮想化プラットフォーム (具体的には VMWare) での操作に関する Microsoft の標準サポート ポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-152">Finance + Operations falls under Microsoft’s standard support policy regarding operation on non-Microsoft virtualization platforms – specifically VMWare.</span></span> <span data-ttu-id="17e3d-153">詳細については、[Microsoft ソフトウェアのサポート ポリシー](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-153">For more information, read [Support policy for Microsoft software](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw).</span></span> <span data-ttu-id="17e3d-154">つまり、この環境では製品をサポートしますが、問題の調査を依頼された場合、仮想化プラットフォームのない状態または Microsoft 仮想化プラットフォームで問題を再現するようまずお客様に依頼する場合があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-154">In short, we support our products in this environment, but if we are asked to investigate an issue, we may ask the customer to first reproduce the problem without the virtualization platform or on the Microsoft virtualization platform.</span></span>

<span data-ttu-id="17e3d-155">VMWare を使用している場合は、次の Web ページに記載されている修正プログラムを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-155">If you are using VMWare, you must implement the fixes that are documented on the following web pages:</span></span>
- [<span data-ttu-id="17e3d-156">仮想マシンをハードウェア バージョン 11 にアップグレード後、ネットワーク依存ワークロードのパフォーマンスが低下する (2129176)</span><span class="sxs-lookup"><span data-stu-id="17e3d-156">After upgrading a virtual machine to hardware version 11, network dependent workloads experience performance degradation (2129176)</span></span>](https://kb.vmware.com/s/article/2129176)
- [<span data-ttu-id="17e3d-157">vmxnet3 仮想アダプターのいくつかの問題</span><span class="sxs-lookup"><span data-stu-id="17e3d-157">Several issues with vmxnet3 virtual adapter</span></span>](https://vinfrastructure.it/2016/05/several-issues-vmxnet3-virtual-adapter)

 > [!WARNING]
 > <span data-ttu-id="17e3d-158">Dynamics 365 Finance + Operations (オンプレミス) は、Azure を含む、任意のパブリック クラウド インフラストラクチャでサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="17e3d-158">Dynamics 365 Finance + Operations (on-premises) is not supported on any public cloud infrastructure, including Azure.</span></span>

<span data-ttu-id="17e3d-159">ハードウェア構成には、次のコンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-159">The hardware configuration includes the following components:</span></span>

- <span data-ttu-id="17e3d-160">Windows Server 2016 仮想マシン (VM) に基づく Standalone Service Fabric Cluster</span><span class="sxs-lookup"><span data-stu-id="17e3d-160">Standalone Service Fabric cluster that is based on Windows Server 2016 virtual machines (VMs)</span></span>
- <span data-ttu-id="17e3d-161">Microsoft SQL Server (Clustered SQL と Always-On の両方がサポートされています)</span><span class="sxs-lookup"><span data-stu-id="17e3d-161">Microsoft SQL Server (both Clustered SQL and Always-On are supported)</span></span>
- <span data-ttu-id="17e3d-162">認証のための AD FS</span><span class="sxs-lookup"><span data-stu-id="17e3d-162">AD FS for authentication</span></span>
- <span data-ttu-id="17e3d-163">ストレージ用の Server Message Block (SMB) バージョン 3 のファイル共有</span><span class="sxs-lookup"><span data-stu-id="17e3d-163">Server Message Block (SMB) version 3 file share for storage</span></span>
- <span data-ttu-id="17e3d-164">オプション: Microsoft Office Server 2017</span><span class="sxs-lookup"><span data-stu-id="17e3d-164">Optional: Microsoft Office Server 2017</span></span>

<span data-ttu-id="17e3d-165">詳細については、[システム要件](../../fin-ops/get-started/system-requirements-on-prem.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-165">For more information, see [System requirements](../../fin-ops/get-started/system-requirements-on-prem.md).</span></span>

### <a name="hardware-layout"></a><span data-ttu-id="17e3d-166">ハードウェア レイアウト</span><span class="sxs-lookup"><span data-stu-id="17e3d-166">Hardware layout</span></span>

<span data-ttu-id="17e3d-167">[オンプレミス環境のハードウェア サイジング](../../fin-ops/get-started/hardware-sizing-on-premises-environments.md) で推奨されるサイジングに基づいて、インフラストラクチャと Service Fabric クラスターを計画します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-167">Plan your infrastructure and Service Fabric cluster based on the recommended sizing in [Hardware sizing for on-premises environments](../../fin-ops/get-started/hardware-sizing-on-premises-environments.md).</span></span> <span data-ttu-id="17e3d-168">Service Fabric クラスターを計画する方法の詳細については、[Service Fabric のスタンドアロン クラスター展開の計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-168">For more information about how to plan the Service Fabric cluster, see [Plan and prepare your Service Fabric standalone cluster deployment](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

<span data-ttu-id="17e3d-169">次のテーブルは、ハードウェア レイアウトの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="17e3d-169">The following table shows an example of a hardware layout.</span></span> <span data-ttu-id="17e3d-170">この例は、設定を説明するためにこのトピック全体で使用されています。</span><span class="sxs-lookup"><span data-stu-id="17e3d-170">This example is used throughout this topic to illustrate the setup.</span></span> <span data-ttu-id="17e3d-171">次の手順で指定されているマシン名と IP アドレスを、ご使用の環境のマシンの名前と IP アドレスに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-171">You will need to replace the machine names and IP addresses given in the following instructions with the names and IP addresses for the machines in your environment.</span></span>

> [!NOTE]
> <span data-ttu-id="17e3d-172">Service Fabric クラスターのプライマリ ノードには、少なくとも 3 つのノードが必要です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-172">The Primary node of the Service Fabric cluster must have at least three nodes.</span></span> <span data-ttu-id="17e3d-173">この例では **OrchestratorType** を主要なノード タイプとして指定します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-173">In this example, **OrchestratorType** is designated as the Primary node type.</span></span>

| <span data-ttu-id="17e3d-174">マシンの目的</span><span class="sxs-lookup"><span data-stu-id="17e3d-174">Machine purpose</span></span>          | <span data-ttu-id="17e3d-175">SF ノード タイプ</span><span class="sxs-lookup"><span data-stu-id="17e3d-175">SF Node type</span></span>     | <span data-ttu-id="17e3d-176">コンピューター名</span><span class="sxs-lookup"><span data-stu-id="17e3d-176">Machine name</span></span>    | <span data-ttu-id="17e3d-177">IP アドレス</span><span class="sxs-lookup"><span data-stu-id="17e3d-177">IP address</span></span>    |
|--------------------------|------------------|-----------------|---------------|
| <span data-ttu-id="17e3d-178">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="17e3d-178">Domain controller</span></span>        |                  | <span data-ttu-id="17e3d-179">DAX7SQLAODC1</span><span class="sxs-lookup"><span data-stu-id="17e3d-179">DAX7SQLAODC1</span></span>    | <span data-ttu-id="17e3d-180">10.179.108.2</span><span class="sxs-lookup"><span data-stu-id="17e3d-180">10.179.108.2</span></span>  |
| <span data-ttu-id="17e3d-181">AD FS</span><span class="sxs-lookup"><span data-stu-id="17e3d-181">AD FS</span></span>                    |                  | <span data-ttu-id="17e3d-182">DAX7SQLAOADFS1</span><span class="sxs-lookup"><span data-stu-id="17e3d-182">DAX7SQLAOADFS1</span></span>  | <span data-ttu-id="17e3d-183">10.179.108.3</span><span class="sxs-lookup"><span data-stu-id="17e3d-183">10.179.108.3</span></span>  |
| <span data-ttu-id="17e3d-184">ファイル サーバー</span><span class="sxs-lookup"><span data-stu-id="17e3d-184">File server</span></span>              |                  | <span data-ttu-id="17e3d-185">DAX7SQLAOFILE1</span><span class="sxs-lookup"><span data-stu-id="17e3d-185">DAX7SQLAOFILE1</span></span>  | <span data-ttu-id="17e3d-186">10.179.108.4</span><span class="sxs-lookup"><span data-stu-id="17e3d-186">10.179.108.4</span></span>  |
| <span data-ttu-id="17e3d-187">SQL Always-On クラスター</span><span class="sxs-lookup"><span data-stu-id="17e3d-187">SQL Always-On cluster</span></span>    |                  | <span data-ttu-id="17e3d-188">DAX7SQLAOSQLA01</span><span class="sxs-lookup"><span data-stu-id="17e3d-188">DAX7SQLAOSQLA01</span></span> | <span data-ttu-id="17e3d-189">10.179.108.5</span><span class="sxs-lookup"><span data-stu-id="17e3d-189">10.179.108.5</span></span>  |
|                          |                  | <span data-ttu-id="17e3d-190">DAX7SQLAOSQLA02</span><span class="sxs-lookup"><span data-stu-id="17e3d-190">DAX7SQLAOSQLA02</span></span> | <span data-ttu-id="17e3d-191">10.179.108.6</span><span class="sxs-lookup"><span data-stu-id="17e3d-191">10.179.108.6</span></span>  |
|                          |                  | <span data-ttu-id="17e3d-192">DAX7SQLAOSQLA</span><span class="sxs-lookup"><span data-stu-id="17e3d-192">DAX7SQLAOSQLA</span></span>   | <span data-ttu-id="17e3d-193">10.179.108.9</span><span class="sxs-lookup"><span data-stu-id="17e3d-193">10.179.108.9</span></span>  |
| <span data-ttu-id="17e3d-194">クライアント</span><span class="sxs-lookup"><span data-stu-id="17e3d-194">Client</span></span>                   |                  | <span data-ttu-id="17e3d-195">SQLAOCLIENT1</span><span class="sxs-lookup"><span data-stu-id="17e3d-195">SQLAOCLIENT1</span></span>    | <span data-ttu-id="17e3d-196">10.179.108.11</span><span class="sxs-lookup"><span data-stu-id="17e3d-196">10.179.108.11</span></span> |
| <span data-ttu-id="17e3d-197">AOS 1</span><span class="sxs-lookup"><span data-stu-id="17e3d-197">AOS 1</span></span>                    | <span data-ttu-id="17e3d-198">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="17e3d-198">AOSNodeType</span></span>      | <span data-ttu-id="17e3d-199">SQLAOSF1AOS1</span><span class="sxs-lookup"><span data-stu-id="17e3d-199">SQLAOSF1AOS1</span></span>    | <span data-ttu-id="17e3d-200">10.179.108.12</span><span class="sxs-lookup"><span data-stu-id="17e3d-200">10.179.108.12</span></span> |
| <span data-ttu-id="17e3d-201">AOS 2</span><span class="sxs-lookup"><span data-stu-id="17e3d-201">AOS 2</span></span>                    | <span data-ttu-id="17e3d-202">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="17e3d-202">AOSNodeType</span></span>      | <span data-ttu-id="17e3d-203">SQLAOSF1AOS2</span><span class="sxs-lookup"><span data-stu-id="17e3d-203">SQLAOSF1AOS2</span></span>    | <span data-ttu-id="17e3d-204">10.179.108.13</span><span class="sxs-lookup"><span data-stu-id="17e3d-204">10.179.108.13</span></span> |
| <span data-ttu-id="17e3d-205">AOS 3</span><span class="sxs-lookup"><span data-stu-id="17e3d-205">AOS 3</span></span>                    | <span data-ttu-id="17e3d-206">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="17e3d-206">AOSNodeType</span></span>      | <span data-ttu-id="17e3d-207">SQLAOSF1AOS3</span><span class="sxs-lookup"><span data-stu-id="17e3d-207">SQLAOSF1AOS3</span></span>    | <span data-ttu-id="17e3d-208">10.179.108.14</span><span class="sxs-lookup"><span data-stu-id="17e3d-208">10.179.108.14</span></span> |
| <span data-ttu-id="17e3d-209">オーケストレータ 1</span><span class="sxs-lookup"><span data-stu-id="17e3d-209">Orchestrator 1</span></span>           | <span data-ttu-id="17e3d-210">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="17e3d-210">OrchestratorType</span></span> | <span data-ttu-id="17e3d-211">SQLAOSF1ORCH1</span><span class="sxs-lookup"><span data-stu-id="17e3d-211">SQLAOSF1ORCH1</span></span>   | <span data-ttu-id="17e3d-212">10.179.108.15</span><span class="sxs-lookup"><span data-stu-id="17e3d-212">10.179.108.15</span></span> |
| <span data-ttu-id="17e3d-213">オーケストレータ 2</span><span class="sxs-lookup"><span data-stu-id="17e3d-213">Orchestrator 2</span></span>           | <span data-ttu-id="17e3d-214">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="17e3d-214">OrchestratorType</span></span> | <span data-ttu-id="17e3d-215">SQLAOSF1ORCH2</span><span class="sxs-lookup"><span data-stu-id="17e3d-215">SQLAOSF1ORCH2</span></span>   | <span data-ttu-id="17e3d-216">10.179.108.16</span><span class="sxs-lookup"><span data-stu-id="17e3d-216">10.179.108.16</span></span> |
| <span data-ttu-id="17e3d-217">オーケストレータ 3</span><span class="sxs-lookup"><span data-stu-id="17e3d-217">Orchestrator 3</span></span>           | <span data-ttu-id="17e3d-218">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="17e3d-218">OrchestratorType</span></span> | <span data-ttu-id="17e3d-219">SQLAOSF1ORCH3</span><span class="sxs-lookup"><span data-stu-id="17e3d-219">SQLAOSF1ORCH3</span></span>   | <span data-ttu-id="17e3d-220">10.179.108.17</span><span class="sxs-lookup"><span data-stu-id="17e3d-220">10.179.108.17</span></span> |
| <span data-ttu-id="17e3d-221">Management Reporter ノード</span><span class="sxs-lookup"><span data-stu-id="17e3d-221">Management Reporter node</span></span> | <span data-ttu-id="17e3d-222">MRType</span><span class="sxs-lookup"><span data-stu-id="17e3d-222">MRType</span></span>           | <span data-ttu-id="17e3d-223">SQLAOSMR1</span><span class="sxs-lookup"><span data-stu-id="17e3d-223">SQLAOSMR1</span></span>       | <span data-ttu-id="17e3d-224">10.179.108.18</span><span class="sxs-lookup"><span data-stu-id="17e3d-224">10.179.108.18</span></span> |
| <span data-ttu-id="17e3d-225">SSRS ノード</span><span class="sxs-lookup"><span data-stu-id="17e3d-225">SSRS node</span></span>                | <span data-ttu-id="17e3d-226">ReportServerType</span><span class="sxs-lookup"><span data-stu-id="17e3d-226">ReportServerType</span></span> | <span data-ttu-id="17e3d-227">SQLAOSFBIN1</span><span class="sxs-lookup"><span data-stu-id="17e3d-227">SQLAOSFBIN1</span></span>     | <span data-ttu-id="17e3d-228">10.179.108.10</span><span class="sxs-lookup"><span data-stu-id="17e3d-228">10.179.108.10</span></span> |

## <a name="setup"></a><span data-ttu-id="17e3d-229">段取り</span><span class="sxs-lookup"><span data-stu-id="17e3d-229">Setup</span></span>

### <a name="prerequisites"></a><span data-ttu-id="17e3d-230">前提条件</span><span class="sxs-lookup"><span data-stu-id="17e3d-230">Prerequisites</span></span>

<span data-ttu-id="17e3d-231">セットアップを開始する前に、次の前提条件が満たされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-231">Before you start the setup, the following prerequisites must be in place.</span></span> <span data-ttu-id="17e3d-232">これらの前提条件の設定は、このドキュメントの範囲外です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-232">The setup of these prerequisites is out of scope for this document.</span></span>

- <span data-ttu-id="17e3d-233">Active Directory Domain Services (AD DS) は、ネットワークにインストールして構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-233">Active Directory Domain Services (AD DS) must be installed and configured in your network.</span></span>
- <span data-ttu-id="17e3d-234">AD FS は、展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-234">AD FS must be deployed.</span></span>
- <span data-ttu-id="17e3d-235">SQL Server 2016 SP1 は SSRS コンピューターにインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-235">SQL Server 2016 SP1 must be installed on the SSRS machines.</span></span>
- <span data-ttu-id="17e3d-236">SQL Server Reporting Services 2016 は、SSRS コンピューターに**ネイティブ** モードでインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-236">SQL Server Reporting Services 2016 must be installed in **Native** mode on the SSRS machines.</span></span>

<span data-ttu-id="17e3d-237">次の必須ソフトウェアは、LCS からダウンロードされたインフラストラクチャ セットアップ スクリプトによって VM にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-237">The following prerequisite software is installed on the VMs by the infrastructure setup scripts downloaded from LCS.</span></span>

| <span data-ttu-id="17e3d-238">ノード タイプ</span><span class="sxs-lookup"><span data-stu-id="17e3d-238">Node type</span></span> | <span data-ttu-id="17e3d-239">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="17e3d-239">Component</span></span> | <span data-ttu-id="17e3d-240">詳細情報</span><span class="sxs-lookup"><span data-stu-id="17e3d-240">Details</span></span> |
|-----------|-----------|---------|
| <span data-ttu-id="17e3d-241">AOS</span><span class="sxs-lookup"><span data-stu-id="17e3d-241">AOS</span></span>       | <span data-ttu-id="17e3d-242">SNAC – ODBC ドライバー 13</span><span class="sxs-lookup"><span data-stu-id="17e3d-242">SNAC – ODBC driver 13</span></span> | <https://www.microsoft.com/download/details.aspx?id=53339> |
| <span data-ttu-id="17e3d-243">AOS</span><span class="sxs-lookup"><span data-stu-id="17e3d-243">AOS</span></span>       | <span data-ttu-id="17e3d-244">SNAC – ODBC ドライバー 17</span><span class="sxs-lookup"><span data-stu-id="17e3d-244">SNAC – ODBC driver 17</span></span> | <span data-ttu-id="17e3d-245">このドライバーは、PU15 以上へのアップグレードに必要です。<https://www.microsoft.com/download/details.aspx?id=56567></span><span class="sxs-lookup"><span data-stu-id="17e3d-245">This driver is needed for upgrading to PU15 or higher: <https://www.microsoft.com/download/details.aspx?id=56567></span></span> |
| <span data-ttu-id="17e3d-246">AOS</span><span class="sxs-lookup"><span data-stu-id="17e3d-246">AOS</span></span>       | <span data-ttu-id="17e3d-247">Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="17e3d-247">The Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="17e3d-248">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="17e3d-248">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="17e3d-249">AOS</span><span class="sxs-lookup"><span data-stu-id="17e3d-249">AOS</span></span>       | <span data-ttu-id="17e3d-250">Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="17e3d-250">The Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="17e3d-251">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="17e3d-251">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="17e3d-252">AOS</span><span class="sxs-lookup"><span data-stu-id="17e3d-252">AOS</span></span>       | <span data-ttu-id="17e3d-253">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="17e3d-253">Internet Information Services (IIS)</span></span> | <span data-ttu-id="17e3d-254">**Windows の機能:** WAS、WAS-Process-Model、WAS-NET-Environment、WAS-Config-APIs、Web-Server、Web-WebServer、Web-Security、Web-Filtering、Web-App-Dev、Web-Net-Ext、Web-Mgmt-Tools、Web-Mgmt-Console</span><span class="sxs-lookup"><span data-stu-id="17e3d-254">**Windows features:** WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs, Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console</span></span> |
| <span data-ttu-id="17e3d-255">AOS</span><span class="sxs-lookup"><span data-stu-id="17e3d-255">AOS</span></span>       | <span data-ttu-id="17e3d-256">SQL Server Management Studio 17.2</span><span class="sxs-lookup"><span data-stu-id="17e3d-256">SQL Server Management Studio 17.2</span></span> | <https://go.microsoft.com/fwlink/?linkid=854085> |
| <span data-ttu-id="17e3d-257">AOS</span><span class="sxs-lookup"><span data-stu-id="17e3d-257">AOS</span></span>       | <span data-ttu-id="17e3d-258">Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="17e3d-258">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</span></span> | <https://support.microsoft.com/help/3179560> |
| <span data-ttu-id="17e3d-259">AOS</span><span class="sxs-lookup"><span data-stu-id="17e3d-259">AOS</span></span>       | <span data-ttu-id="17e3d-260">Microsoft Visual Studio 2017 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="17e3d-260">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2017</span></span> | <span data-ttu-id="17e3d-261"><https://lcs.dynamics.com/V2/SharedAssetLibrary>> モデル > "VC ++ 17 再頒布可能"</span><span class="sxs-lookup"><span data-stu-id="17e3d-261"><https://lcs.dynamics.com/V2/SharedAssetLibrary> > Models > "VC++ 17 Redistributables"</span></span> |
| <span data-ttu-id="17e3d-262">AOS</span><span class="sxs-lookup"><span data-stu-id="17e3d-262">AOS</span></span>       | <span data-ttu-id="17e3d-263">Microsoft Access データベース エンジン 2010 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="17e3d-263">Microsoft Access Database Engine 2010 Redistributable</span></span> | <https://www.microsoft.com/download/details.aspx?id=13255> |
| <span data-ttu-id="17e3d-264">BI</span><span class="sxs-lookup"><span data-stu-id="17e3d-264">BI</span></span>        | <span data-ttu-id="17e3d-265">.NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="17e3d-265">.NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="17e3d-266">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="17e3d-266">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="17e3d-267">BI</span><span class="sxs-lookup"><span data-stu-id="17e3d-267">BI</span></span>        | <span data-ttu-id="17e3d-268">.NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="17e3d-268">.NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="17e3d-269">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="17e3d-269">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="17e3d-270">BI</span><span class="sxs-lookup"><span data-stu-id="17e3d-270">BI</span></span>        | <span data-ttu-id="17e3d-271">SQL Server Management Studio 17.2</span><span class="sxs-lookup"><span data-stu-id="17e3d-271">SQL Server Management Studio 17.2</span></span> | <https://go.microsoft.com/fwlink/?linkid=854085> |
| <span data-ttu-id="17e3d-272">MR</span><span class="sxs-lookup"><span data-stu-id="17e3d-272">MR</span></span>        | <span data-ttu-id="17e3d-273">.NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="17e3d-273">.NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="17e3d-274">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="17e3d-274">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="17e3d-275">MR</span><span class="sxs-lookup"><span data-stu-id="17e3d-275">MR</span></span>        | <span data-ttu-id="17e3d-276">.NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="17e3d-276">.NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="17e3d-277">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="17e3d-277">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="17e3d-278">MR</span><span class="sxs-lookup"><span data-stu-id="17e3d-278">MR</span></span>        | <span data-ttu-id="17e3d-279">Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="17e3d-279">Visual C++ Redistributable Packages for Visual Studio 2013</span></span> | <https://support.microsoft.com/help/3179560> |
| <span data-ttu-id="17e3d-280">ORCH</span><span class="sxs-lookup"><span data-stu-id="17e3d-280">ORCH</span></span>      | <span data-ttu-id="17e3d-281">Microsoft .NET Framework version 4.0–4.8 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="17e3d-281">The Microsoft .NET Framework version 4.0–4.8 (CLR 4.0)</span></span> | <https://dotnet.microsoft.com/download/thank-you/net48-offline> |

### <a name="overview"></a><span data-ttu-id="17e3d-282">概要</span><span class="sxs-lookup"><span data-stu-id="17e3d-282">Overview</span></span>

<span data-ttu-id="17e3d-283">Finance + Operations のインフラストラクチャを設定するには、以下の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-283">The following steps must be completed to set up the infrastructure for Finance + Operations.</span></span> <span data-ttu-id="17e3d-284">開始する前にすべての手順を読むと、セットアップを計画しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-284">Reading all the steps before you begin will make it easier to plan your setup.</span></span>

1. [<span data-ttu-id="17e3d-285">ドメイン名と DNS ゾーンの計画</span><span class="sxs-lookup"><span data-stu-id="17e3d-285">Plan your domain name and DNS zones</span></span>](#plandomain)
2. [<span data-ttu-id="17e3d-286">証明書の計画と取得</span><span class="sxs-lookup"><span data-stu-id="17e3d-286">Plan and acquire your certificates</span></span>](#plancert)
3. [<span data-ttu-id="17e3d-287">ユーザーとサービス アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="17e3d-287">Plan your users and service accounts</span></span>](#plansvcacct)
4. [<span data-ttu-id="17e3d-288">DNS ゾーンの作成と A レコードの追加</span><span class="sxs-lookup"><span data-stu-id="17e3d-288">Create DNS zones, and add A records</span></span>](#createdns)
5. [<span data-ttu-id="17e3d-289">VM のドメインへの参加</span><span class="sxs-lookup"><span data-stu-id="17e3d-289">Join VMs to the domain</span></span>](#joindomain)
6. [<span data-ttu-id="17e3d-290">LCS からセットアップ スクリプトのダウンロード</span><span class="sxs-lookup"><span data-stu-id="17e3d-290">Download setup scripts from LCS</span></span>](#downloadscripts)
7. [<span data-ttu-id="17e3d-291">コンフィギュレーションの記述</span><span class="sxs-lookup"><span data-stu-id="17e3d-291">Describe your configuration</span></span>](#describeconfig)
8. [<span data-ttu-id="17e3d-292">証明書の構成</span><span class="sxs-lookup"><span data-stu-id="17e3d-292">Configure certificates</span></span>](#configurecert)
9. [<span data-ttu-id="17e3d-293">VM を設定する</span><span class="sxs-lookup"><span data-stu-id="17e3d-293">Setup VMs</span></span>](#setupvms)
10. [<span data-ttu-id="17e3d-294">スタンドアロン Service Fabric クラスターの設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-294">Set up a standalone Service Fabric cluster</span></span>](#setupsfcluster)
11. [<span data-ttu-id="17e3d-295">テナント用 LCS 接続の構成</span><span class="sxs-lookup"><span data-stu-id="17e3d-295">Configure LCS connectivity for the tenant</span></span>](#configurelcs)
12. [<span data-ttu-id="17e3d-296">ファイル ストレージの設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-296">Set up file storage</span></span>](#setupfile)
13. [<span data-ttu-id="17e3d-297">SQL Server の設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-297">Set up SQL Server</span></span>](#setupsql)
14. [<span data-ttu-id="17e3d-298">データベースを構成する</span><span class="sxs-lookup"><span data-stu-id="17e3d-298">Configure the databases</span></span>](#configuredb)
15. [<span data-ttu-id="17e3d-299">資格情報の暗号化</span><span class="sxs-lookup"><span data-stu-id="17e3d-299">Encrypt credentials</span></span>](#encryptcred)
16. [<span data-ttu-id="17e3d-300">資産除去債務 (SSIS) の設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-300">Set up SSIS</span></span>](#setupssis)
17. [<span data-ttu-id="17e3d-301">資産除去債務 (SSRS) の設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-301">Set up SSRS</span></span>](#setupssrs)
18. [<span data-ttu-id="17e3d-302">AD FS のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="17e3d-302">Configure AD FS</span></span>](#configureadfs)
19. [<span data-ttu-id="17e3d-303">コネクタを構成し、オンプレミスのローカル エージェントをインストールする</span><span class="sxs-lookup"><span data-stu-id="17e3d-303">Configure a connector and install an on-premises local agent</span></span>](#configureconnector)
20. [<span data-ttu-id="17e3d-304">リモート処理が使用されたら、CredSSP を終了処理する</span><span class="sxs-lookup"><span data-stu-id="17e3d-304">Tear down CredSSP, if remoting was used</span></span>](#teardowncredssp)
21. [<span data-ttu-id="17e3d-305">LCS から Finance + Operations 環境を配置する</span><span class="sxs-lookup"><span data-stu-id="17e3d-305">Deploy your Finance + Operations environment from LCS</span></span>](#deploy)
22. [<span data-ttu-id="17e3d-306">Finance + Operations 環境への接続</span><span class="sxs-lookup"><span data-stu-id="17e3d-306">Connect to your Finance + Operations environment</span></span>](#connect)

### <a name="plandomain"></a> <span data-ttu-id="17e3d-307">1. ドメイン名と DNS ゾーンの計画</span><span class="sxs-lookup"><span data-stu-id="17e3d-307">1. Plan your domain name and DNS zones</span></span>

<span data-ttu-id="17e3d-308">AOS のプロダクション インストールには、公的に登録されたドメイン名を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-308">We recommend that you use a publicly registered domain name for your production installation of AOS.</span></span> <span data-ttu-id="17e3d-309">このようにして、外部アクセスが必要な場合は、ネットワークの外部からインストールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-309">In that way, the installation can be accessed outside the network, if outside access is required.</span></span>

<span data-ttu-id="17e3d-310">たとえば、会社のドメインが contoso.com の場合、Finance + Operations は d365ffo.onprem.contoso.com であり、ホスト名は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-310">For example, if your company's domain is contoso.com, your zone for Finance + Operations might be d365ffo.onprem.contoso.com, and the host names might be as follows:</span></span>

- <span data-ttu-id="17e3d-311">AOS の機械の場合 ax.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-311">ax.d365ffo.onprem.contoso.com for AOS machines</span></span>
- <span data-ttu-id="17e3d-312">Service Fabric クラスターの場合 sf.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-312">sf.d365ffo.onprem.contoso.com for the Service Fabric cluster</span></span>

### <a name="plancert"></a> <span data-ttu-id="17e3d-313">2. 証明書の計画と取得</span><span class="sxs-lookup"><span data-stu-id="17e3d-313">2. Plan and acquire your certificates</span></span>

<span data-ttu-id="17e3d-314">Service Fabric クラスターと展開されているすべてのアプリケーションを保護するには、Secure Sockets Layer (SSL) 証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-314">Secure Sockets Layer (SSL) certificates are required in order to secure a Service Fabric cluster and all the applications that are deployed.</span></span> <span data-ttu-id="17e3d-315">プロダクションとサンドボックスのワークロードについては、[DigiCert](https://www.digicert.com/ssl-certificate/)、[Comodo](https://ssl.comodo.com/)、[Symantec](https://www.websecurity.symantec.com/ssl-certificate)、[GoDaddy](https://www.godaddy.com/web-security/ssl-certificate)、または [GlobalSign](https://www.globalsign.com/en/ssl/) などの認証局から証明書を取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-315">For your production and sandbox workloads, we recommend that you acquire certificates from a certificate authority (CA) such as [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate), or [GlobalSign](https://www.globalsign.com/en/ssl/).</span></span> <span data-ttu-id="17e3d-316">ドメインが [Active Directory 証明書サービス](https://technet.microsoft.com/library/cc772393(v=ws.10).aspx) (AD CS) で設定されている場合は、AD CS を介して証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-316">If your domain is set up with [Active Directory Certificate Services](https://technet.microsoft.com/library/cc772393(v=ws.10).aspx) (AD CS), you can create the certificates through AD CS.</span></span> <span data-ttu-id="17e3d-317">証明書ごとに、プライベート キーが作成されたキーの交換を含める必要があり、個人情報交換 (.pfx) ファイルにエクスポート可能な必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-317">Each certificate must contain a private key that was created for key exchange, and it must be exportable to a Personal Information Exchange (.pfx) file.</span></span>

<span data-ttu-id="17e3d-318">自己署名証明書は、テスト目的でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-318">Self-signed certificates can be used only for testing purposes.</span></span> <span data-ttu-id="17e3d-319">便宜上、LCS で提供されるセットアップ スクリプトには、自己署名証明書を生成およびエクスポートするスクリプトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-319">For convenience, the setup scripts provided in LCS include scripts that generate and export self-signed certificates.</span></span> <span data-ttu-id="17e3d-320">自己署名スクリプトを使用している場合は、後の手順で作成スクリプトを実行するように指示されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-320">If you are using self-signed scripts, you will be instructed to run the creation scripts in later steps.</span></span> <span data-ttu-id="17e3d-321">先に述べたように、これらの証明書はテスト目的でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-321">As we've mentioned, these certificates can be used for testing purposes only.</span></span>

<span data-ttu-id="17e3d-322">証明書の推奨設定は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="17e3d-322">Recommended settings for certificates are:</span></span>
- <span data-ttu-id="17e3d-323">署名アルゴリズム: sha256RSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-323">Signature algorithm: sha256RSA</span></span>
- <span data-ttu-id="17e3d-324">署名ハッシュ アルゴリズム: sha256</span><span class="sxs-lookup"><span data-stu-id="17e3d-324">Signature hash algorithm: sha256</span></span>
- <span data-ttu-id="17e3d-325">公開キー: RSA (2048 ビット)</span><span class="sxs-lookup"><span data-stu-id="17e3d-325">Public key: RSA (2048 bits)</span></span>
- <span data-ttu-id="17e3d-326">Thumbprint アルゴリズム: sha1</span><span class="sxs-lookup"><span data-stu-id="17e3d-326">Thumbprint algorithm: sha1</span></span>

| <span data-ttu-id="17e3d-327">目的</span><span class="sxs-lookup"><span data-stu-id="17e3d-327">Purpose</span></span>                                      | <span data-ttu-id="17e3d-328">説明</span><span class="sxs-lookup"><span data-stu-id="17e3d-328">Explanation</span></span> | <span data-ttu-id="17e3d-329">追加条件</span><span class="sxs-lookup"><span data-stu-id="17e3d-329">Additional requirements</span></span> |
|----------------------------------------------|-------------|-------------------------|
| <span data-ttu-id="17e3d-330">SQL Server SSL 証明書</span><span class="sxs-lookup"><span data-stu-id="17e3d-330">SQL Server SSL certificate</span></span>                   | <span data-ttu-id="17e3d-331">この証明書は、ネットワーク上の SQL Server インスタンスとクライアント アプリケーションの間で転送されるデータを暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-331">This certificate is used to encrypt data that is transmitted across a network between an instance of SQL Server and a client application.</span></span> | <p><span data-ttu-id="17e3d-332">証明書の場合、ドメイン名は SQL Server のインスタンスまたはリスナーの完全修飾ドメイン名 (FQDN) と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-332">The domain name of the certificate should match the fully qualified domain name (FQDN) of the SQL Server instance or listener.</span></span> <span data-ttu-id="17e3d-333">たとえば、SQL のリスナーが DAX7SQLAOSQLA のコンピューターにホストされている場合、証明書の DNS 名は、DAX7SQLAOSQLA.contoso.com です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-333">For example, if the SQL listener is hosted on the machine DAX7SQLAOSQLA, the certificate's DNS name is DAX7SQLAOSQLA.contoso.com.</span></span></p> <p><span data-ttu-id="17e3d-334">CN: DAX7SQLAOSQLA.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-334">CN: DAX7SQLAOSQLA.contoso.com</span></span> <br> <span data-ttu-id="17e3d-335">DNS 名: DAX7SQLAOSQLA.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-335">DNS Name: DAX7SQLAOSQLA.contoso.com</span></span></p> |
| <span data-ttu-id="17e3d-336">Service Fabric Server 証明書</span><span class="sxs-lookup"><span data-stu-id="17e3d-336">Service Fabric Server certificate</span></span>            | <p><span data-ttu-id="17e3d-337">この証明書を使用して、Service Fabric ノード間のノードからノードの通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-337">This certificate is used to help secure the node-to-node communication between the Service Fabric nodes.</span></span></p> <p> <span data-ttu-id="17e3d-338">この証明書は、クラスターに接続するクライアントに提示されるサーバー証明書としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-338">This certificate is also used as the Server certificate that is presented to the client that connects to the cluster.</span></span></p> | <p><span data-ttu-id="17e3d-339">この証明書には、ドメインの SSL ワイルド カード証明書も使用できます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-339">For this certificate you can also use SSL wild card certificate of your domain.</span></span> <span data-ttu-id="17e3d-340">たとえば、\*.contoso.com です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-340">For example, \*.contoso.com.</span></span> <span data-ttu-id="17e3d-341">これについて下の表で詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-341">This is explained in more details below the table.</span></span> <span data-ttu-id="17e3d-342">それ以外の場合は、次の値を使用します:</span><span class="sxs-lookup"><span data-stu-id="17e3d-342">Otherwise, use the following values:</span></span></p> <p><span data-ttu-id="17e3d-343">CN: sf.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-343">CN: sf.d365ffo.onprem.contoso.com</span></span> <br> <span data-ttu-id="17e3d-344">DNS 名: sf.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-344">DNS Name: sf.d365ffo.onprem.contoso.com</span></span></p> |
| <span data-ttu-id="17e3d-345">Service Fabric Client 証明書</span><span class="sxs-lookup"><span data-stu-id="17e3d-345">Service Fabric Client certificate</span></span>            | <span data-ttu-id="17e3d-346">この証明書は、クライアントによって Service Fabric クラスターを表示および管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-346">This certificate is used by clients to view and manage the Service Fabric cluster.</span></span> | <span data-ttu-id="17e3d-347">CN: client.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-347">CN: client.d365ffo.onprem.contoso.com</span></span> <br> <span data-ttu-id="17e3d-348">DNS 名: client.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-348">DNS Name: client.d365ffo.onprem.contoso.com</span></span> |
| <span data-ttu-id="17e3d-349">証明書の暗号化</span><span class="sxs-lookup"><span data-stu-id="17e3d-349">Encipherment Certificate</span></span>                     | <span data-ttu-id="17e3d-350">この証明書は、SQL Server パスワードとユーザー アカウントのパスワードなどの重要な情報を暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-350">This certificate is used to encrypt sensitive information such as the SQL Server password and user account passwords.</span></span> | <p> <span data-ttu-id="17e3d-351">証明書は、プロバイダー **Microsoft Enhanced Cryptographic Provider v1.0** を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-351">The certificate must be created by using the provider **Microsoft Enhanced Cryptographic Provider v1.0**.</span></span> </p><p><span data-ttu-id="17e3d-352">証明書キーの使用にはデータ暗号化 (10) が含まれている必要があり、サーバー認証またはクライアント認証は含めないでください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-352">The certificate key usage must include Data Encipherment (10) and should not include Server authentication or Client authentication.</span></span></p><p><span data-ttu-id="17e3d-353">詳細については、[Service Fabric アプリケーションでの機密情報の管理](/azure/service-fabric/service-fabric-application-secret-management) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-353">For more information, see [Managing secrets in Service Fabric applications](/azure/service-fabric/service-fabric-application-secret-management).</span></span></p> <p> <span data-ttu-id="17e3d-354">CN: axdataenciphermentcert</span><span class="sxs-lookup"><span data-stu-id="17e3d-354">CN: axdataenciphermentcert</span></span> <br> <span data-ttu-id="17e3d-355">DNS 名: axdataenciphermentcert</span><span class="sxs-lookup"><span data-stu-id="17e3d-355">DNS Name: axdataenciphermentcert</span></span> </p> |
| <span data-ttu-id="17e3d-356">AOS SSL 証明書</span><span class="sxs-lookup"><span data-stu-id="17e3d-356">AOS SSL Certificate</span></span>                          | <p><span data-ttu-id="17e3d-357">この証明書は、AOS Web サイトに接続するクライアントに提示されるサーバー証明書としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-357">This certificate is used as the Server certificate that is presented to the client for the AOS website.</span></span> <span data-ttu-id="17e3d-358">また、WCF (Windows Communication Foundation) / SOAP (Simple Object Access Protocol) 証明書を有効にするためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-358">It's also used to enable Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP) certificates.</span></span></p> | <p><span data-ttu-id="17e3d-359">Service Fabric サーバー証明書として使用するのと同じワイルドカード証明書を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-359">You can use the same wild card certificate that you used as the Service Fabric Server certificate.</span></span> <span data-ttu-id="17e3d-360">それ以外の場合は、次の値を使用します:</span><span class="sxs-lookup"><span data-stu-id="17e3d-360">Otherwise, use the following values:</span></span></p> <p> <span data-ttu-id="17e3d-361">CN: ax.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-361">CN: ax.d365ffo.onprem.contoso.com</span></span> <br> <span data-ttu-id="17e3d-362">DNS 名: ax.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-362">DNS Name: ax.d365ffo.onprem.contoso.com</span></span> </p> |
| <span data-ttu-id="17e3d-363">セッション認証証明書</span><span class="sxs-lookup"><span data-stu-id="17e3d-363">Session Authentication certificate</span></span>           | <span data-ttu-id="17e3d-364">この証明書は、AOS がユーザーのセッション情報を保護するために使用します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-364">This certificate is used by AOS to help secure a user's session information.</span></span> | <p> <span data-ttu-id="17e3d-365">この証明書は、LCS からの展開時に使用されるファイル共有証明書です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-365">This certificate is also the File Share certificate that will be used at the time of deployment from LCS.</span></span></p> <p> <span data-ttu-id="17e3d-366">CN: SessionAuthentication</span><span class="sxs-lookup"><span data-stu-id="17e3d-366">CN: SessionAuthentication</span></span> <br> <span data-ttu-id="17e3d-367">DNS 名: SessionAuthentication</span><span class="sxs-lookup"><span data-stu-id="17e3d-367">DNS Name: SessionAuthentication</span></span> </p> |
| <span data-ttu-id="17e3d-368">データの暗号化証明書</span><span class="sxs-lookup"><span data-stu-id="17e3d-368">Data Encryption certificate</span></span>                  | <span data-ttu-id="17e3d-369">これらの証明書は、機密情報を暗号化するために AOS によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-369">This certificate is used by the AOS to encrypt sensitive information.</span></span>  | <p><span data-ttu-id="17e3d-370">これはプロバイダー **Microsoft Enhanced RSA および AES Cryptographic Provider** を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-370">This must be created using the provider **Microsoft Enhanced RSA and AES Cryptographic Provider**.</span></span> </p> <p> <span data-ttu-id="17e3d-371">CN: DataEncryption</span><span class="sxs-lookup"><span data-stu-id="17e3d-371">CN: DataEncryption</span></span> <br> <span data-ttu-id="17e3d-372">DNS 名: DataEncryption</span><span class="sxs-lookup"><span data-stu-id="17e3d-372">DNS Name: DataEncryption</span></span> </p> |
| <span data-ttu-id="17e3d-373">データ署名の証明書</span><span class="sxs-lookup"><span data-stu-id="17e3d-373">Data Signing certificate</span></span>                     | <span data-ttu-id="17e3d-374">これらの証明書は、機密情報を暗号化するために AOS によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-374">This certificate is used by the AOS to encrypt sensitive information.</span></span>  | <p> <span data-ttu-id="17e3d-375">これは、データ暗号化証明書とは別のもので、プロバイダー**Microsoft の拡張された RSA および AES 暗号化プロバイダー**を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-375">This is separate from the Data Encryption certificate and must be created using the provider **Microsoft Enhanced RSA and AES Cryptographic Provider**.</span></span> </p> <p> <span data-ttu-id="17e3d-376">CN: DataSigning</span><span class="sxs-lookup"><span data-stu-id="17e3d-376">CN: DataSigning</span></span> <br> <span data-ttu-id="17e3d-377">DNS 名: DataSigning</span><span class="sxs-lookup"><span data-stu-id="17e3d-377">DNS Name: DataSigning</span></span> </p> |
| <span data-ttu-id="17e3d-378">財務報告クライアント証明書</span><span class="sxs-lookup"><span data-stu-id="17e3d-378">Financial Reporting client certificate</span></span>       | <span data-ttu-id="17e3d-379">この証明書は、財務報告サービスと AOS 間の通信を保護するのに役立ちます。   この証明書を使用して、財務報告サービスと AOS 間の通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-379">This certificate is used to help secure the communication between the Financial Reporting services and the AOS.</span></span> | <p><span data-ttu-id="17e3d-380">CN: FinancialReporting</span><span class="sxs-lookup"><span data-stu-id="17e3d-380">CN: FinancialReporting</span></span> <br> <span data-ttu-id="17e3d-381">DNS 名: FinancialReporting</span><span class="sxs-lookup"><span data-stu-id="17e3d-381">DNS Name: FinancialReporting</span></span> </p>  |
| <span data-ttu-id="17e3d-382">報告証明書</span><span class="sxs-lookup"><span data-stu-id="17e3d-382">Reporting certificate</span></span>                        | <span data-ttu-id="17e3d-383">この証明書を使用して、SSRS と AOS 間の通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-383">This certificate is used to help secure the communication between SSRS and the AOS.</span></span>| <p> <span data-ttu-id="17e3d-384">**財務報告クライアント証明書を再利用しないでください。**</span><span class="sxs-lookup"><span data-stu-id="17e3d-384">**Do not reuse the Financial Reporting Client certificate.**</span></span> </p> <p> <span data-ttu-id="17e3d-385">CN: ReportingService</span><span class="sxs-lookup"><span data-stu-id="17e3d-385">CN: ReportingService</span></span> <br> <span data-ttu-id="17e3d-386">DNS 名: ReportingService</span><span class="sxs-lookup"><span data-stu-id="17e3d-386">DNS Name: ReportingService</span></span> </p> |
| <span data-ttu-id="17e3d-387">オンプレミス ローカル エージェント証明書</span><span class="sxs-lookup"><span data-stu-id="17e3d-387">On-Premises local agent certificate</span></span>           | <p><span data-ttu-id="17e3d-388">この証明書は、オンプレミスと LCS でホストされているローカル エージェント間の通信を保護するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-388">This certificate is used to help secure the communication between a local agent that is hosted on-premises and on LCS.</span></span></p><p><span data-ttu-id="17e3d-389">この証明書を使用すると、Azure AD テナントに代わってローカル エージェントが動作し、LCS と通信して配置を編成および監視することができます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-389">This certificate enables the local agent to act on behalf of your Azure AD tenant, and to communicate with LCS to orchestrate and monitor deployments.</span></span></p><p><span data-ttu-id="17e3d-390">**注記:** テナントにはオンプレミス ローカル エージェント証明書が 1 つだけ必要です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-390">**Note:** Only 1 on-premises local agent certificate is needed for a tenant.</span></span></p> | <p> <span data-ttu-id="17e3d-391">CN: OnPremLocalAgent</span><span class="sxs-lookup"><span data-stu-id="17e3d-391">CN: OnPremLocalAgent</span></span> <br> <span data-ttu-id="17e3d-392">DNS 名: OnPremLocalAgent</span><span class="sxs-lookup"><span data-stu-id="17e3d-392">DNS Name: OnPremLocalAgent</span></span> </p> |

<span data-ttu-id="17e3d-393">ドメインの SSL ワイルド カード証明書を使用して、Service Fabric サーバー証明書と AOS SSL 証明書を結合できます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-393">SSL wild card certificate of your domain can be used to combine Service Fabric Server certificate and AOS SSL certificate.</span></span>

<span data-ttu-id="17e3d-394">以下は、AOS SSL 証明書と組み合わせた Service Fabric Server 証明書の例です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-394">The following is an example of a Service Fabric Server certificate combined with an AOS SSL certificate.</span></span>

#### <a name="subject-name"></a><span data-ttu-id="17e3d-395">件名</span><span class="sxs-lookup"><span data-stu-id="17e3d-395">Subject name</span></span>

```
CN = *.d365ffo.onprem.contoso.com
```

#### <a name="subject-alternative-names"></a><span data-ttu-id="17e3d-396">件名の代替名</span><span class="sxs-lookup"><span data-stu-id="17e3d-396">Subject alternative names</span></span>

```
DNS Name=ax.d365ffo.onprem.contoso.com
DNS Name=sf.d365ffo.onprem.contoso.com
DNS Name=*.d365ffo.onprem.contoso.com
```

> [!NOTE]
> <span data-ttu-id="17e3d-397">ワイルド カード証明書は、発行先となるドメインの最初のレベル サブドメインのみをセキュリティ保護できるようにします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-397">The wild card certificate allows you to secure only the first-level subdomain of the domain to which it is issued.</span></span>

### <a name="plansvcacct"></a> <span data-ttu-id="17e3d-398">3. ユーザーとサービス アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="17e3d-398">3. Plan your users and service accounts</span></span>

<span data-ttu-id="17e3d-399">Finance + Operations を機能させるために、いくつかのユーザー アカウントまたはサービス アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-399">You must create several user or service accounts for Finance + Operations to work.</span></span> <span data-ttu-id="17e3d-400">サービス アカウントの管理グループ (gMSAs)、ドメイン アカウント、および SQL アカウントの組み合わせを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-400">You must create a combination of group managed service accounts (gMSAs), domain accounts, and SQL accounts.</span></span> <span data-ttu-id="17e3d-401">次の表は、このトピックで使用されるユーザー アカウント、その目的、および名前の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="17e3d-401">The following table shows the user accounts, their purpose, and example names that will be used in this topic.</span></span>

| <span data-ttu-id="17e3d-402">ユーザー アカウント</span><span class="sxs-lookup"><span data-stu-id="17e3d-402">User account</span></span>                                            | <span data-ttu-id="17e3d-403">種類</span><span class="sxs-lookup"><span data-stu-id="17e3d-403">Type</span></span>           | <span data-ttu-id="17e3d-404">目的</span><span class="sxs-lookup"><span data-stu-id="17e3d-404">Purpose</span></span> | <span data-ttu-id="17e3d-405">ユーザー名</span><span class="sxs-lookup"><span data-stu-id="17e3d-405">User name</span></span> |
|---------------------------------------------------------|----------------|---------|-----------|
| <span data-ttu-id="17e3d-406">財務レポート アプリケーション サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="17e3d-406">Financial Reporting Application Service Account</span></span>         | <span data-ttu-id="17e3d-407">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-407">gMSA</span></span>           |         | <span data-ttu-id="17e3d-408">Contoso\\svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="17e3d-408">Contoso\\svc-FRAS$</span></span> |
| <span data-ttu-id="17e3d-409">財務レポート プロセス サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="17e3d-409">Financial Reporting Process Service Account</span></span>             | <span data-ttu-id="17e3d-410">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-410">gMSA</span></span>           |         | <span data-ttu-id="17e3d-411">Contoso\\svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="17e3d-411">Contoso\\svc-FRPS$</span></span> |
| <span data-ttu-id="17e3d-412">財務レポート クリック ワンス デザイナー サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="17e3d-412">Financial Reporting Click Once Designer Service Account</span></span> | <span data-ttu-id="17e3d-413">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-413">gMSA</span></span>           |         | <span data-ttu-id="17e3d-414">Contoso\\svc-FRCO$</span><span class="sxs-lookup"><span data-stu-id="17e3d-414">Contoso\\svc-FRCO$</span></span> |
| <span data-ttu-id="17e3d-415">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="17e3d-415">AOS Service Account</span></span>                                     | <span data-ttu-id="17e3d-416">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-416">gMSA</span></span>           | <span data-ttu-id="17e3d-417">このユーザーは、将来校正するために作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-417">This user should be created for future proofing.</span></span> <span data-ttu-id="17e3d-418">今後のリリースでは、AOS を gMSA と連携させる予定です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-418">We plan to enable AOS to work with the gMSA in upcoming releases.</span></span> <span data-ttu-id="17e3d-419">このユーザーを設定時に作成することで、gMSA へのシームレスな移行を確実にすることができます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-419">By creating this user at the time of setup, you will help to ensure a seamless transition to the gMSA.</span></span> | <span data-ttu-id="17e3d-420">Contoso\\svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="17e3d-420">Contoso\\svc-AXSF$</span></span> |
| <span data-ttu-id="17e3d-421">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="17e3d-421">AOS Service Account</span></span>                                     | <span data-ttu-id="17e3d-422">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="17e3d-422">Domain account</span></span> | <span data-ttu-id="17e3d-423">AOS は、一般提供 (GA) リリースでこのユーザーを使用します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-423">AOS uses this user in the general availability (GA) release.</span></span> | <span data-ttu-id="17e3d-424">Contoso\\AXServiceUser</span><span class="sxs-lookup"><span data-stu-id="17e3d-424">Contoso\\AXServiceUser</span></span> |
| <span data-ttu-id="17e3d-425">AOS SQL DB 管理者ユーザー</span><span class="sxs-lookup"><span data-stu-id="17e3d-425">AOS SQL DB Admin user</span></span>                                   | <span data-ttu-id="17e3d-426">SQL ユーザー</span><span class="sxs-lookup"><span data-stu-id="17e3d-426">SQL user</span></span>       | <span data-ttu-id="17e3d-427">Finance + Operations は、このユーザーを使用して SQL\* を認証します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-427">Finance + Operations uses this user to authenticate with SQL\*.</span></span> <span data-ttu-id="17e3d-428">このユーザーも、今後のリリースで gMSA ユーザーに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-428">This user will also be replaced by the gMSA user in upcoming releases.</span></span> | <span data-ttu-id="17e3d-429">AXDBAdmin</span><span class="sxs-lookup"><span data-stu-id="17e3d-429">AXDBAdmin</span></span> |
| <span data-ttu-id="17e3d-430">ローカル配置エージェント サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="17e3d-430">Local Deployment Agent Service Account</span></span>                  | <span data-ttu-id="17e3d-431">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-431">gMSA</span></span>           | <span data-ttu-id="17e3d-432">このアカウントは、ローカル エージェントによって、さまざまなノードでの展開を調整するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-432">This account is used by the local agent to orchestrate the deployment on various nodes.</span></span> | <span data-ttu-id="17e3d-433">Contoso\\Svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="17e3d-433">Contoso\\Svc-LocalAgent$</span></span> |

<span data-ttu-id="17e3d-434">\* SQL 認証の SQL ユーザー名とパスワードは、暗号化されてファイル共有に格納されているため、保護されています。</span><span class="sxs-lookup"><span data-stu-id="17e3d-434">\* The SQL user name and password for SQL authentication are secured because they are encrypted and stored in the file share.</span></span>

### <a name="createdns"></a> <span data-ttu-id="17e3d-435">4. DNS ゾーンの作成とレコードの追加</span><span class="sxs-lookup"><span data-stu-id="17e3d-435">4. Create DNS zones and add A records</span></span>

<span data-ttu-id="17e3d-436">DNS は AD DS と統合されており、ネットワーク内のリソースを整理、管理、検索することができます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-436">DNS is integrated with AD DS, and lets you organize, manage, and find resources in a network.</span></span> <span data-ttu-id="17e3d-437">次の指示では、AOS ホスト名と Service Fabric クラスターの DNS 前方参照ゾーンと A レコードを作成する手順を示します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-437">The following instructions provide steps to create a DNS forward lookup zone and A records for the AOS host name and Service Fabric cluster.</span></span> <span data-ttu-id="17e3d-438">この設定例では、DNS ゾーン名は d365ffo.onprem.contoso.com で、A レコード/ホスト名は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="17e3d-438">In this example setup, the DNS zone name is d365ffo.onprem.contoso.com, and the A records/host names are as follows:</span></span>

- <span data-ttu-id="17e3d-439">AOS の機械の場合 **ax**.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-439">**ax**.d365ffo.onprem.contoso.com for AOS machines</span></span>
- <span data-ttu-id="17e3d-440">Service Fabric クラスターの場合 **sf**.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="17e3d-440">**sf**.d365ffo.onprem.contoso.com for the Service Fabric cluster</span></span>

#### <a name="add-a-dns-zone"></a><span data-ttu-id="17e3d-441">DNS ゾーンの追加</span><span class="sxs-lookup"><span data-stu-id="17e3d-441">Add a DNS zone</span></span>

<span data-ttu-id="17e3d-442">DNS ゾーンを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-442">Use the following procedure to add a DNS zone.</span></span>

1. <span data-ttu-id="17e3d-443">ドメイン コントローラー コンピューターにログインして **スタート** を選択し、**dnsmgmt.msc** と入力して **dnsmgmt (DNS)** アプリケーションを選択することにより DNS マネージャーを起動します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-443">Sign in to the domain controller machine, select **Start**, and start DNS Manager by typing **dnsmgmt.msc** and selecting the **dnsmgmt (DNS)** application.</span></span>
2. <span data-ttu-id="17e3d-444">コンソール ツリーでドメイン コントローラー名を右クリックし、**新しいゾーン** \> **次へ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-444">Right-click the domain controller name in the console tree, and then select **New Zone** \> **Next**.</span></span>
3. <span data-ttu-id="17e3d-445">**プライマリ ゾーン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-445">Select **Primary Zone**.</span></span>
4. <span data-ttu-id="17e3d-446">**Active Directory にゾーンを保存 (DNS サーバーが書き込み可能なドメイン コントローラーの場合にのみ使用可能)** のチェック ボックスが選択されたままの状態で、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-446">Leave the **Store the zone in Active Directory (available only if the DNS Server is a writeable domain controller** check box selected, and then select **Next**.</span></span>
5. <span data-ttu-id="17e3d-447">**このドメイン (Contoso.com) のドメイン コントローラーで実行されているすべての DNS サーバーに対して** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-447">Select **To all DNS Servers running on Domain Controllers in this domain: Contoso.com**, and then select **Next**.</span></span>
6. <span data-ttu-id="17e3d-448">**前方参照ゾーン** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-448">Select **Forward Lookup Zone**, and then select **Next**.</span></span>
7. <span data-ttu-id="17e3d-449">設定するゾーン名を入力し、**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-449">Enter the zone name for your setup, and then select **Next**.</span></span> <span data-ttu-id="17e3d-450">たとえば、**d365ffo.onprem.contoso.com** と入力します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-450">For example, enter **d365ffo.onprem.contoso.com**.</span></span>
8. <span data-ttu-id="17e3d-451">**動的更新を許可しない** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-451">Select **Do not allow dynamic updates**, and then select **Next**.</span></span>
9. <span data-ttu-id="17e3d-452">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-452">Select **Finish**.</span></span>

#### <a name="set-up-an-a-record-for-aos"></a><span data-ttu-id="17e3d-453">AOS の A レコードを設定する</span><span class="sxs-lookup"><span data-stu-id="17e3d-453">Set up an A record for AOS</span></span>

<span data-ttu-id="17e3d-454">新しい DNS ゾーンで、**AOSNodeType** タイプの Service Fabric クラスター ノード**ごと**に、**ax.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-454">In the new DNS zone, create one A record that is named **ax.d365ffo.onprem.contoso.com** for **each** Service Fabric cluster node of the **AOSNodeType** type.</span></span> <span data-ttu-id="17e3d-455">他のノード タイプの A レコードは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-455">Don't create A records for the other node types.</span></span>

1. <span data-ttu-id="17e3d-456">DNS マネージャーの**前方参照ゾーン**フォルダーで、新しく作成したゾーンを検索します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-456">Find the newly created zone under the **Forward Lookup Zones** folder in DNS Manager.</span></span>
2. <span data-ttu-id="17e3d-457">新しいゾーンを右クリックして、**新しいホスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-457">Right-click the new zone, and then select **New Host**.</span></span>
3. <span data-ttu-id="17e3d-458">Service Fabric ノードの 名前および IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-458">Enter the name and IP address of the Service Fabric node.</span></span> <span data-ttu-id="17e3d-459">(たとえば、**ax** を名前として入力し、**10.179.108.12** を IP アドレスとして入力します。) **ホストの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-459">(For example, enter **ax** as the name and enter **10.179.108.12** as the IP address.) Select **Add Host**.</span></span>
4. <span data-ttu-id="17e3d-460">どのチェック ボックスもオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-460">Do not select either check box.</span></span>
5. <span data-ttu-id="17e3d-461">各 AOS ノードで手順 1 ～ 4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-461">Repeat steps 1-4 for each AOS node.</span></span>

#### <a name="set-up-an-a-record-for-the-orchestrator"></a><span data-ttu-id="17e3d-462">Orchestrator の A レコードを設定する</span><span class="sxs-lookup"><span data-stu-id="17e3d-462">Set up an A record for the orchestrator</span></span>

<span data-ttu-id="17e3d-463">新しい DNS ゾーンで、**OrchestratorType** タイプの Service Fabric クラスター ノード**ごと**に、**sf.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-463">In the new DNS zone, create an A record that is named **sf.d365ffo.onprem.contoso.com** for **each** Service Fabric cluster node of the **OrchestratorType** type.</span></span> <span data-ttu-id="17e3d-464">他のノード タイプの A レコードは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-464">Don't create A records for the other node types.</span></span>

1. <span data-ttu-id="17e3d-465">新しいゾーンを右クリックして、**新しいホスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-465">Right-click the new zone, and then select **New Host**.</span></span>
2. <span data-ttu-id="17e3d-466">Service Fabric ノードの 名前および IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-466">Enter the name and IP address of the Service Fabric node.</span></span> <span data-ttu-id="17e3d-467">(たとえば、**sf** を名前としてを入力し、**10.179.108.15** を IP アドレスとして入力します。) **ホストの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-467">(For example, enter **sf** as the name and enter **10.179.108.15** as the IP address.) Select **Add Host**.</span></span>
3. <span data-ttu-id="17e3d-468">どのチェック ボックスもオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-468">Do not select either check box.</span></span>
4. <span data-ttu-id="17e3d-469">各オーケストレータ ノードを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-469">Repeat for each Orchestrator node.</span></span>

### <a name="joindomain"></a> <span data-ttu-id="17e3d-470">5. VM のドメインへの参加</span><span class="sxs-lookup"><span data-stu-id="17e3d-470">5. Join VMs to the domain</span></span>

<span data-ttu-id="17e3d-471">各 VM をドメインに参加させるには、[コンピューターをドメインに参加させる](https://docs.microsoft.com/windows-server/identity/ad-fs/deployment/join-a-computer-to-a-domain)のドキュメントの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-471">Join each VM to the domain by completing the steps in the [Join a Computer to a Domain](https://docs.microsoft.com/windows-server/identity/ad-fs/deployment/join-a-computer-to-a-domain) document.</span></span> <span data-ttu-id="17e3d-472">または、次の Windows PowerShell スクリプトを使用します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-472">Alternatively, use the following Windows PowerShell script.</span></span>

```powershell
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
```

> [!IMPORTANT]
> <span data-ttu-id="17e3d-473">ドメインにそれらを結合させた後、VM を再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-473">You must restart the VMs after you join them to the domain.</span></span>

### <a name="downloadscripts"></a> <span data-ttu-id="17e3d-474">6. LCS からのセットアップ スクリプトのダウンロード</span><span class="sxs-lookup"><span data-stu-id="17e3d-474">6. Download setup scripts from LCS</span></span>

<span data-ttu-id="17e3d-475">セットアップ エクスペリエンスを向上させるためのスクリプトをいくつか紹介しています。</span><span class="sxs-lookup"><span data-stu-id="17e3d-475">We have provided several scripts to help improve the setup experience.</span></span> <span data-ttu-id="17e3d-476">LCS からセットアップ スクリプトをダウンロードするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="17e3d-476">Follow these steps to download the setup scripts from LCS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17e3d-477">スクリプトは、オンプレミス インフラストラクチャと同じドメイン内のコンピューターから実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-477">The scripts must be executed from a computer in the same domain that the on-premises infrastructure is in.</span></span>

1. <span data-ttu-id="17e3d-478">[LCS](https://lcs.dynamics.com/v2) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-478">Sign in to [LCS](https://lcs.dynamics.com/v2).</span></span>
2. <span data-ttu-id="17e3d-479">ダッシュボードで、**共有アセット ライブラリ**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-479">On the dashboard, select the **Shared asset library** tile.</span></span>
3. <span data-ttu-id="17e3d-480">**モデル**タブの、グリッドで、**Dynamics 365 for Operations オンプレミス - 配置スクリプト**行を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-480">On the **Model** tab, in the grid, select the **Dynamics 365 for Operations on-premises - Deployment scripts** row.</span></span>
4. <span data-ttu-id="17e3d-481">**バージョン** を選択し、スクリプトの zip ファイルの最新版をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-481">Select **Versions**, and then download the latest version of the zip file for the scripts.</span></span>
   >[!Note] 
   > <span data-ttu-id="17e3d-482">プラットフォーム更新プログラム 8 またはプラットフォーム更新プログラム 11 の以前のバージョンが必要な場合は、バージョン 1 をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-482">If you need the older version for Platform update 8 or Platform update 11, download version 1.</span></span>
5. <span data-ttu-id="17e3d-483">zip ファイルを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-483">Right-click the zip file, and then select **Properties**.</span></span> <span data-ttu-id="17e3d-484">ダイアログ ボックスで、**ブロック解除**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-484">In the dialog box, select the **Unblock** check box.</span></span>
6. <span data-ttu-id="17e3d-485">ZIP ファイルをスクリプトの実行に使用するマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-485">Copy the zip file to the machine that will be used to execute the scripts.</span></span>
7. <span data-ttu-id="17e3d-486">**infrastructure** という名前のフォルダーにファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-486">Unzip the files into a folder that is named **infrastructure**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17e3d-487">このフォルダーの ConfigTemplate.xml ファイルにすべての編集を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-487">Ensure all edits are made to the ConfigTemplate.xml file in this folder.</span></span>

### <a name="describeconfig"></a> <span data-ttu-id="17e3d-488">7. コンフィギュレーションの記述</span><span class="sxs-lookup"><span data-stu-id="17e3d-488">7. Describe your configuration</span></span>

<span data-ttu-id="17e3d-489">インフラストラクチャの設定 スクリプトは、次のコンフィギュレーション ファイルを使用して設定を実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-489">The infrastructure setup scripts use the following configuration files to drive the setup.</span></span>
- <span data-ttu-id="17e3d-490">infrastructure\ConfigTemplate.xml</span><span class="sxs-lookup"><span data-stu-id="17e3d-490">infrastructure\ConfigTemplate.xml</span></span>
- <span data-ttu-id="17e3d-491">infrastructure\D365FO-OP\NodeTopologyDefinition.xml</span><span class="sxs-lookup"><span data-stu-id="17e3d-491">infrastructure\D365FO-OP\NodeTopologyDefinition.xml</span></span>
- <span data-ttu-id="17e3d-492">infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml</span><span class="sxs-lookup"><span data-stu-id="17e3d-492">infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml</span></span>

>[!NOTE]
><span data-ttu-id="17e3d-493">セットアップ スクリプトが正しく機能するには、環境に基づいてコンフィギュレーション ファイルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-493">Configuration files must be updated based on your environment for the setup scripts to work correctly.</span></span> <span data-ttu-id="17e3d-494">これらのファイルは、設定に基づいて適切なコンピューター名、IP アドレス、サービス アカウントおよびドメインで更新してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-494">Be sure to update these files with the proper computer names, IP addresses, service accounts, and domain based on your setup.</span></span>

<span data-ttu-id="17e3d-495">**infrastructure\ConfigTemplate.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-495">**infrastructure\ConfigTemplate.xml** describes:</span></span>
- <span data-ttu-id="17e3d-496">アプリケーションが動作するために必要なサービス アカウント</span><span class="sxs-lookup"><span data-stu-id="17e3d-496">Service Accounts that are needed for the application to operate</span></span>
- <span data-ttu-id="17e3d-497">通信を保護するために必要な証明書</span><span class="sxs-lookup"><span data-stu-id="17e3d-497">Certificates necessary for securing communications</span></span>
- <span data-ttu-id="17e3d-498">データベース コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="17e3d-498">Database configuration</span></span>
- <span data-ttu-id="17e3d-499">Service Fabric クラスター構成</span><span class="sxs-lookup"><span data-stu-id="17e3d-499">Service Fabric cluster configuration</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="17e3d-500">Service Fabric クラスタをコンフィギュレーションする際に OrchestratorType の 3 つのフォールト ドメインがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-500">Make sure that there are three fault domains for OrchestratorType when you configure Service Fabric cluster.</span></span> <span data-ttu-id="17e3d-501">Service Fabric クラスタをコンフィギュレーションする際、単一のマシンにノードの 1 つのタイプのみが配置されるよう確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-501">Make sure that no more than one type of node is deployed in a single machine when you configure Service Fabric cluster.</span></span>

<span data-ttu-id="17e3d-502">各 Service Fabric ノード タイプについて、**infrastructure\D365FO-OP\NodeTopologyDefinition.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-502">For each Service Fabric node type, **infrastructure\D365FO-OP\NodeTopologyDefinition.xml** describes:</span></span>

- <span data-ttu-id="17e3d-503">各ノード タイプとアプリケーション、ドメインとサービス アカウント、および証明書間のマッピング。</span><span class="sxs-lookup"><span data-stu-id="17e3d-503">The mapping between each node type and the application, domain and service accounts, and certificates.</span></span>
- <span data-ttu-id="17e3d-504">UAC を有効にするかどうか。</span><span class="sxs-lookup"><span data-stu-id="17e3d-504">Whether to enable the UAC.</span></span>
- <span data-ttu-id="17e3d-505">Windows の機能とシステム ソフトウェアの前提条件。</span><span class="sxs-lookup"><span data-stu-id="17e3d-505">Prerequisites for Windows features and system software.</span></span>
- <span data-ttu-id="17e3d-506">厳密な名前の検証を有効にするかどうか。</span><span class="sxs-lookup"><span data-stu-id="17e3d-506">Whether strong name validation should be enabled.</span></span>
- <span data-ttu-id="17e3d-507">ファイアウォール ポートのリストを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-507">List of firewall ports to be opened.</span></span>

<span data-ttu-id="17e3d-508">各データベースについて、**infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-508">For each database, **infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml** describes:</span></span>

- <span data-ttu-id="17e3d-509">データベース設定。</span><span class="sxs-lookup"><span data-stu-id="17e3d-509">The database settings.</span></span>
- <span data-ttu-id="17e3d-510">ユーザーとロール間のマッピング。</span><span class="sxs-lookup"><span data-stu-id="17e3d-510">The mappings between users and roles.</span></span>

#### <a name="create-gmsa-and-domain-user-accounts"></a><span data-ttu-id="17e3d-511">gMSA およびドメイン ユーザー アカウントを作成する</span><span class="sxs-lookup"><span data-stu-id="17e3d-511">Create gMSA and domain user accounts</span></span>

1. <span data-ttu-id="17e3d-512">**インフラストラクチャ** フォルダーに展開したインフラストラクチャ スクリプトがあるマシンに移動します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-512">Navigate to the machine that has the unzipped infrastructure scripts in the **infrastructure** folder.</span></span>
2. <span data-ttu-id="17e3d-513">**インフラストラクチャ**フォルダーをドメイン コントローラー マシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-513">Copy the **infrastructure** folder to the domain controller machine.</span></span>
3. <span data-ttu-id="17e3d-514">管理者特権モードで Windows PowerShell を起動し、ディレクトリを **infrastructure** フォルダーに変更して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-514">Start Windows PowerShell in elevated mode, change the directory to the **infrastructure** folder, and run the following commands.</span></span>
    > [!IMPORTANT]
    > <span data-ttu-id="17e3d-515">次のスクリプトは、ドメイン ユーザー AxServiceUser を作成しません。</span><span class="sxs-lookup"><span data-stu-id="17e3d-515">The following script doesn't create a domain user AxServiceUser for you.</span></span> <span data-ttu-id="17e3d-516">ユーザーが作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-516">You must create it yourself.</span></span>

    ```powershell
    Import-Module .\D365FO-OP\D365FO-OP.psd1
    New-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```
    


4. <span data-ttu-id="17e3d-517">AOS サービス アカウントの **Contoso\svc-AXSF$** および **Contoso\AXServiceUser** をすべての AOS マシンのローカル 管理者グループへ追加します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-517">Add the AOS Service Accounts, **Contoso\svc-AXSF$** and **Contoso\AXServiceUser** to the local administrators group for all AOS machines.</span></span> <span data-ttu-id="17e3d-518">詳細については、「[ローカル グループへのメンバーの追加](https://technet.microsoft.com/library/cc772524(v=ws.11).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-518">For more information, see [Add a member to local group](https://technet.microsoft.com/library/cc772524(v=ws.11).aspx).</span></span>

5. <span data-ttu-id="17e3d-519">アカウントまたはマシンを変更する必要がある場合は、元の **インフラストラクチャ** フォルダーの ConfigTemplate.xml ファイルを更新し、このマシンにコピーしてから次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-519">If you must make changes to accounts or machines, update the ConfigTemplate.xml file in the original **infrastructure** folder, copy it to this machine and then run the following script.</span></span>

    ```powershell
    Update-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="configurecert"></a> <span data-ttu-id="17e3d-520">8. 証明書のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="17e3d-520">8. Configure certificates</span></span>

1. <span data-ttu-id="17e3d-521">**インフラストラクチャ** フォルダーがあるマシンに移動します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-521">Navigate to the machine that has the **infrastructure** folder.</span></span>
2. <span data-ttu-id="17e3d-522">自己署名証明書を生成する必要がある場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-522">If you must generate self-signed certificates, run the following command.</span></span> <span data-ttu-id="17e3d-523">スクリプトは証明書を作成し、それらをコンピューターの「CurrentUser\My certificate store」に格納し、XML ファイルのサムプリントを更新します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-523">The script will create the certificates, put them in the CurrentUser\My certificate store on the machine, and update the thumbprints in the XML file.</span></span>

    ```powershell
    # Create self-signed certs
    .\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    <span data-ttu-id="17e3d-524">証明書を再利用する必要があるため、証明書を生成する必要がない場合は、**generateSelfSignedCert** タグを **false** に設定します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-524">If you must reuse any certificates and therefore don't have to generate certificates for them, set the **generateSelfSignedCert** tag to **false**.</span></span>

3. <span data-ttu-id="17e3d-525">既に生成されている SSL 証明書を使用している場合は、証明書生成をスキップし、configTemplate.xml ファイルの拇印を更新します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-525">If you're using SSL certificates that were already generated, skip the Certificate generation and update the thumbprints in the configTemplate.xml file.</span></span> <span data-ttu-id="17e3d-526">証明書は CurrentUser\My ストアにインストールする必要があり、その秘密キーはエクスポート可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="17e3d-526">The certificates need to be installed in the CurrentUser\My store and their private keys must be exportable.</span></span>

> [!WARNING]
> <span data-ttu-id="17e3d-527">存在する場合に特定するのが難しい先頭の印刷不可能な特殊文字のため、証明書マネージャーは拇印をコピーするために使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-527">Because of a leading not-printable special character, which is difficult to determine when present, the cert manager should not be used to copy thumbprints.</span></span> <span data-ttu-id="17e3d-528">印刷できない特殊文字がある場合、**X509 証明書が無効です**というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-528">If the not-printable special character is present, you will get the error, **X509 certificate not valid**.</span></span> <span data-ttu-id="17e3d-529">拇印を取得するには、PowerShell コマンドの結果を参照するか、PowerShell で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-529">To retrieve the thumbprints, see results from PowerShell commands or run the following commands in PowerShell.</span></span>
> ```powershell
> dir cert:\CurrentUser\My
> dir cert:\LocalMachine\My
> dir cert:\LocalMachine\Root
> ```

4. <span data-ttu-id="17e3d-530">各証明書の **ProtectTo** でユーザーまたはグループのセミコロンで区切られた一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-530">Specify a semi-colon separated list of users or groups in the **ProtectTo** tag for each certificate.</span></span> <span data-ttu-id="17e3d-531">**ProtectTo** タグで指定された Active Directory ユーザーとグループのみに、スクリプトを使用してエクスポートされる証明書をインポートするアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-531">Only Active directory users and groups specified in the **ProtectTo** tag will have permissions to import the certificates that are exported using the scripts.</span></span> <span data-ttu-id="17e3d-532">エクスポートした証明書を保護するため、スクリプトによりパスワードがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="17e3d-532">Passwords are not supported by the script to protect the exported certificates</span></span>

5. <span data-ttu-id="17e3d-533">証明書を .pfx ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-533">Export the certificates into .pfx files.</span></span>

    ```powershell
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will be written to infrastructure\Certs folder.
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="setupvms"></a> <span data-ttu-id="17e3d-534">9. VM の設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-534">9. Setup VMs</span></span>
1. <span data-ttu-id="17e3d-535">各 VM で実行する必要があるスクリプトをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-535">Export the scripts that must be run on each VM.</span></span>

    ```powershell
    # Exports the script files to be execute on each VM into a directory VMs\<VMName>.
    .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. <span data-ttu-id="17e3d-536">次の Microsoft Windows Installers (MSI) を全ての VM でアクセス可能なファイル共有にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-536">Download the following Microsoft Windows Installers (MSIs) into a file share that is accessible by all VMs.</span></span>

| <span data-ttu-id="17e3d-537">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="17e3d-537">Component</span></span> | <span data-ttu-id="17e3d-538">リンクのダウンロード</span><span class="sxs-lookup"><span data-stu-id="17e3d-538">Download link</span></span> |
|-----------|---------------|
| <span data-ttu-id="17e3d-539">SNAC – ODBC ドライバー 13</span><span class="sxs-lookup"><span data-stu-id="17e3d-539">SNAC – ODBC driver 13</span></span> | <https://www.microsoft.com/download/details.aspx?id=53339> |
| <span data-ttu-id="17e3d-540">SNAC – ODBC ドライバー 17</span><span class="sxs-lookup"><span data-stu-id="17e3d-540">SNAC – ODBC driver 17</span></span> | <https://www.microsoft.com/download/details.aspx?id=56567> |
| <span data-ttu-id="17e3d-541">Microsoft SQL ServerManagement Studio 17.5</span><span class="sxs-lookup"><span data-stu-id="17e3d-541">Microsoft SQL Server Management Studio 17.5</span></span> | <https://docs.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms> |
| <span data-ttu-id="17e3d-542">Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="17e3d-542">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</span></span> | <https://support.microsoft.com/help/3179560> |
| <span data-ttu-id="17e3d-543">Microsoft Access データベース エンジン 2010 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="17e3d-543">Microsoft Access Database Engine 2010 Redistributable</span></span> | <https://www.microsoft.com/download/details.aspx?id=13255> |

> [!IMPORTANT]
> <span data-ttu-id="17e3d-544">Microsoft SQL Server Management Studio の設定が、対象となるコンピューターのオペレーティング システムと同じ言語であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-544">Make sure the Microsoft SQL Server Management Studio setup is in the same language as the operating system of the target machine.</span></span>
> <span data-ttu-id="17e3d-545">NodeTopologyDefinition.xml で定義されているインストーラー ファイルが指定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-545">Ensure the installer files are named as defined in NodeTopologyDefinition.xml.</span></span>
> <span data-ttu-id="17e3d-546">msodbcsql.ms SSMS-Setup-\*.exe vcredist_x64.exe AccessDatabaseEngine_x64.exe</span><span class="sxs-lookup"><span data-stu-id="17e3d-546">msodbcsql.ms SSMS-Setup-\*.exe vcredist_x64.exe AccessDatabaseEngine_x64.exe</span></span>

#### <a name="follow-these-steps-for-each-vm-or-use-remoting-from-a-single-machine"></a><span data-ttu-id="17e3d-547">各 VM についてこれらのステップに従うか、または単一のコンピューターからリモート処理を使用します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-547">Follow these steps for each VM, or use remoting from a single machine</span></span>

> [!NOTE]
> <span data-ttu-id="17e3d-548">次のセクションでは、複数の VM での実行が必要です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-548">The following section requires execution on multiple VMs.</span></span> <span data-ttu-id="17e3d-549">このプロセスは、指定されたリモート処理スクリプトを使用して、1 台のマシン (`.\Export-Scripts.ps1` を実行するのと同じマシンなど) から必要なスクリプトを実行するオプションを提供することで、簡単に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-549">This process can be eased by using the supplied remoting scripts, which provide the option of running the necessary scripts from a single machine, such as the same machine used to execute `.\Export-Scripts.ps1`.</span></span> <span data-ttu-id="17e3d-550">利用可能な場合、リモート処理スクリプトは、PowerShell セクションの「`# If Remoting`」コメントの後に宣言されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-550">The remoting scripts, when available, are declared after a "`# If Remoting`" comment in the PowerShell sections.</span></span> <span data-ttu-id="17e3d-551">リモート処理スクリプトを使用するときは、セクションの残りのスクリプトを実行する必要はありません。そのような例については、セクションの本文を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-551">When the remoting scripts are used, you may not need to execute the remaining scripts in a section, please see the section text for cases such as that.</span></span> <span data-ttu-id="17e3d-552">リモート処理では、[WinRM](https://msdn.microsoft.com/library/aa384426(v=vs.85).aspx) が使用され、特定のケースでは [CredSSP](https://msdn.microsoft.com/library/windows/desktop/bb931352(v=vs.85).aspx) が有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-552">Remoting uses [WinRM](https://msdn.microsoft.com/library/aa384426(v=vs.85).aspx) and requires [CredSSP](https://msdn.microsoft.com/library/windows/desktop/bb931352(v=vs.85).aspx) to be enabled in certain cases.</span></span> <span data-ttu-id="17e3d-553">CredSSP の有効化と無効化は、実行ごとにリモート処理モジュールによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-553">The enabling and disabling of CredSSP is handled by the remoting module on a per-execution basis.</span></span> <span data-ttu-id="17e3d-554">資格情報の盗難の形でのセキュリティ リスクをもたらすため、CredSSP が使用されていない場合に有効のままにすることはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="17e3d-554">Keeping CredSSP enabled when it is not in use is not advised, as it introduces security risks in the shape of credential theft.</span></span> <span data-ttu-id="17e3d-555">設定が完了した場合、[CredSSP を終了処理する](#teardowncredssp) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-555">See the [Tear down CredSSP](#teardowncredssp) section when you are finished setting up.</span></span>

1. <span data-ttu-id="17e3d-556">各 infrastructure\VMs\<VMName> フォルダーのコンテンツを対応する VM にコピーし (リモート処理スクリプトが使用されている場合は、コンテンツをターゲット VM に自動的にコピーします)、次のスクリプトを管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-556">Copy the contents of each infrastructure\VMs\<VMName> folder into the corresponding VM (if remoting scripts are used, they will automatically copy the content to the target VMs), and then run the following scripts as an Administrator.</span></span>

    ```powershell
    # Install pre-req software on the VMs.

    # If Remoting, execute
    # .\Configure-PreReqs-AllVMs.ps1 -MSIFilePath <share folder path of the MSIs> -ConfigurationFilePath .\ConfigTemplate.xml

    .\Configure-PreReqs.ps1 -MSIFilePath <path of the MSIs>
    ```

    > [!IMPORTANT]
    > 1. <span data-ttu-id="17e3d-557">再起動するように求められるたびにコンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-557">Each time you are prompted, restart the machine.</span></span> <span data-ttu-id="17e3d-558">再起動した後、すべての前提条件がインストールされるまで、`.\Configure-PreReqs.ps1` スクリプトを再実行することを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-558">Make sure that you rerun the `.\Configure-PreReqs.ps1` script after each restart until all of the prerequisites are installed.</span></span> <span data-ttu-id="17e3d-559">リモート処理の場合、すべてのマシンがオンラインに戻ったときに AllVM スクリプトを再実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-559">In the case of remoting, rerun the AllVMs script when all of the machines are back online.</span></span>
    > 2. <span data-ttu-id="17e3d-560">リモート処理スクリプトを使用するときに、現在のユーザーが MSI の共有フォルダーにアクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-560">When you use the remoting script, ensure that the current user has access to the share folder of MSIs.</span></span>
    > 3. <span data-ttu-id="17e3d-561">リモート処理スクリプトを使用するときに、ユーザーが AOSNoteType、MRType、および ReportServerType タイプのマシンにアクセスしていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-561">When you use the remoting script, ensure no user is accessing the AOSNoteType, MRType, and ReportServerType type machines.</span></span> <span data-ttu-id="17e3d-562">それ以外の場合は、コンピューターにログオンしているユーザーが原因で、リモート処理スクリプトはコンピュータの再起動に失敗します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-562">Otherwise, the remoting script will fail to restart the computer because of the users being logged on to the computer.</span></span>

2. <span data-ttu-id="17e3d-563">VM セットアップを完了するため、存在する場合は、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-563">Run the following scripts, if they exist, to complete the VM setup.</span></span>

    ```powershell
    # If Remoting, only execute
    # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    .\Add-GMSAOnVM.ps1
    .\Import-PfxFiles.ps1
    .\Set-CertificateAcls.ps1
    ```

3. <span data-ttu-id="17e3d-564">次のスクリプトを実行して VM のセットアップを検証します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-564">Run the following script to validate the VM setup.</span></span>

    ```powershell
    # If Remoting, execute
    # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    .\Test-D365FOConfiguration.ps1 
    ```

> [!IMPORTANT]
> <span data-ttu-id="17e3d-565">リモート処理を使用していた場合は、設定が完了するとクリーンアップ手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-565">If remoting was used, be sure to execute the clean up steps when the setup is complete.</span></span> <span data-ttu-id="17e3d-566">[20. Tear down CredSSP](#teardowncredssp) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-566">See the [20. Tear down CredSSP](#teardowncredssp) section.</span></span>

### <a name="setupsfcluster"></a> <span data-ttu-id="17e3d-567">10. スタンドアロン Service Fabric クラスターの設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-567">10. Set up a standalone Service Fabric cluster</span></span>

1. <span data-ttu-id="17e3d-568">[Service Fabric スタンドアロン インストール パッケージ](https://go.microsoft.com/fwlink/?LinkId=730690) を使用中の Service Fabric ノードのいずれかにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-568">Download the [Service Fabric standalone installation package](https://go.microsoft.com/fwlink/?LinkId=730690) onto one of your Service Fabric nodes.</span></span> <span data-ttu-id="17e3d-569">ZIP ファイルをダウンロードした後、 ZIP ファイルを右クリックし**プロパティ**を選択してブロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-569">After the zip file is downloaded, unblock it by right-clicking the zip file and then selecting **Properties**.</span></span> <span data-ttu-id="17e3d-570">ダイアログ ボックスで、右下の **ブロック解除** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-570">In the dialog box, select the **Unblock** check box in the lower right.</span></span>

2. <span data-ttu-id="17e3d-571">ZIP ファイルを Service Fabric クラスター内のいずれかのノードにコピーし、解凍します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-571">Copy the zip file to one of the nodes in the Service Fabric cluster, and unzip it.</span></span> <span data-ttu-id="17e3d-572">**インフラストラクチャ**フォルダーが、このフォルダーにアクセスすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-572">Ensure the **infrastructure** folder has access to this folder.</span></span>

3. <span data-ttu-id="17e3d-573">**インフラストラクチャ** フォルダーに移動し、次のコマンドを実行して Service Fabric Cluster の ClusterConfig.json ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-573">Navigate to the **infrastructure** folder and execute the following command to generate the Service Fabric ClusterConfig.json file.</span></span>

    ```powershell
   .\New-SFClusterConfig.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -TemplateConfig <ServiceFabricStandaloneInstallerPath>\ClusterConfig.X509.MultiMachine.json
    ```
4. <span data-ttu-id="17e3d-574">クラスター コンフィギュレーションへの追加の変更は、環境に基づいて必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-574">Additional modifications to your cluster configuration may be necessary based on your environment.</span></span> <span data-ttu-id="17e3d-575">詳細については、[手順 1B: 複数のマシンでクラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)、[X.509 証明書を使用して Windows スタンドアロン クラスターを保護する](/azure/service-fabric/service-fabric-windows-cluster-x509-security)、および[Windows Server で実行されているスタンドアロン クラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-575">For more information, see, [Step 1B: Create a multi-machine cluster](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Secure a standalone cluster on Windows using X.509 certificates](/azure/service-fabric/service-fabric-windows-cluster-x509-security), and [Create a standalone cluster running on Windows Server](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).</span></span>

5. <span data-ttu-id="17e3d-576">生成された ClusterConfig.json ファイルを \<ServiceFabricStandaloneInstallerPath\> にコピーします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-576">Copy the generated ClusterConfig.json file to the \<ServiceFabricStandaloneInstallerPath\>.</span></span>

6. <span data-ttu-id="17e3d-577">上位の権限を使用して Windows PowerShell で \<ServiceFabricStandaloneInstallerPath\> に移動します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-577">Navigate to the \<ServiceFabricStandaloneInstallerPath\> in Windows PowerShell by using elevated privileges.</span></span> <span data-ttu-id="17e3d-578">次のコマンドを実行して ClusterConfig をテストします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-578">Run the following command to test ClusterConfig.</span></span>

    ```powershell
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

7. <span data-ttu-id="17e3d-579">テストが成功した場合は、次のコマンドを実行してクラスターを展開します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-579">If the test is successful, run the following command to deploy the cluster.</span></span>

    ```powershell
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

8. <span data-ttu-id="17e3d-580">クラスターが作成された後は、任意のクライアント マシンで Service Fabric エクスプローラーを開き、インストールを検証します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-580">After the cluster is created, open the Service Fabric explorer on any client machine to validate the installation.</span></span>

    1. <span data-ttu-id="17e3d-581">まだインストールされていない場合、CurrentUser\\My に Service Fabric クライアント証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-581">Install the Service Fabric client certificate in CurrentUser\\My if it isn't already installed.</span></span>
    2. <span data-ttu-id="17e3d-582">**IE 設定** \> **互換モード** に移動し、**互換モードでイントラネット サイトを表示する** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-582">Go to **IE settings** \> **Compatibility Mode**, and clear the **Display Intranet sites in compatibility mode** check box.</span></span>
    3. <span data-ttu-id="17e3d-583">`https://sf.d365ffo.onprem.contoso.com:19080` に移動します。sf.d365ffo.onprem.contoso.com は、ゾーンで指定されている Service Fabric クラスターのホスト名です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-583">Go to `https://sf.d365ffo.onprem.contoso.com:19080`, where sf.d365ffo.onprem.contoso.com is the host name of the Service Fabric cluster that is specified in the zone.</span></span> <span data-ttu-id="17e3d-584">DNS 名前解決が設定されていない場合は、マシンの IP アドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-584">If DNS name resolution isn't configured, use the IP address of the machine.</span></span>
    4. <span data-ttu-id="17e3d-585">クライアントの証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-585">Select the client certificate.</span></span> <span data-ttu-id="17e3d-586">**Service Fabric エクスプローラー** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-586">The **Service Fabric explorer** page appears.</span></span>
    5. <span data-ttu-id="17e3d-587">すべてのノードが緑で表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-587">Verify that all nodes are appear as green.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="17e3d-588">クライアント マシンが Windows Server 2016 のようなサーバー コンピューターである場合は、**Service Fabric エクスプローラー**ページにアクセスするときに IE のセキュリティ強化の構成をオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-588">If your client machine is a server machine like Windows Server 2016, you must turn off the IE Enhanced Security Configuration when you access the **Service Fabric explorer** page.</span></span>
    > <span data-ttu-id="17e3d-589">ウィルス対策ソフトウェアがインストールされている場合は、[Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) ドキュメントのガイダンスに従って除外を設定してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-589">If any antivirus software is installed, ensure you set exclusion following the guidance in the [Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) documentation.</span></span>

### <a name="configurelcs"></a> <span data-ttu-id="17e3d-590">11. テナント用 LCS 接続のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="17e3d-590">11. Configure LCS connectivity for the tenant</span></span>

<span data-ttu-id="17e3d-591">Finance + Operations の展開とサービスは、オンプレミスのローカル エージェントを使用して LCS を通じて調整されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-591">Deployment and servicing of Finance + Operations is orchestrated through LCS by using an on-premises local agent.</span></span> <span data-ttu-id="17e3d-592">LCS から Finance + Operations テナントへの接続を確立するには、Azure AD テナント (たとえば、Contoso.onmicrosoft.com) の代わりに動作するローカル エージェントを可能にする証明書をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-592">To establish connectivity from LCS to the Finance + Operations tenant, you must configure a certificate that enables the local agent to act on behalf on your Azure AD tenant (for example, Contoso.onmicrosoft.com).</span></span>

<span data-ttu-id="17e3d-593">証明機関から取得したオンプレミス エージェントの証明書またはスクリプトを使用して生成した自己署名証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-593">Use the on-premises agent certificate that you acquired from a certificate authority or the self-signed certificate that you generated by using scripts.</span></span>

<span data-ttu-id="17e3d-594">オンプレミス エージェント証明書は、テナントごとに複数のサンドボックス環境および実稼動環境で再利用できます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-594">The on-premises agent certificate can be reused across multiple sandbox and production environments per tenant.</span></span>

<span data-ttu-id="17e3d-595">グローバル管理者ディレクトリの役割を持つユーザー アカウントだけが、LCS を承認するための証明書を追加できます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-595">Only user accounts that have the Global Administrator directory role can add certificates to authorize LCS.</span></span> <span data-ttu-id="17e3d-596">既定では、組織の Microsoft Office 365 にサインアップする担当者が、ディレクトリのグローバル管理者です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-596">By default, the person who signs up for Microsoft Office 365 for your organization is the global administrator for the directory.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="17e3d-597">テナントごとに証明書を正確に 1 回構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-597">You must configure the certificate exactly one time per tenant.</span></span> <span data-ttu-id="17e3d-598">すべてのオンプレミス環境では、同じ証明書を使用して LCS に接続できます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-598">All on-premises environments can use the same certificate to connect with LCS.</span></span>
   > <span data-ttu-id="17e3d-599">Windows Server 2016 などのサーバー コンピューターでこれを実行する場合は、IE セキュリティ強化の構成を一時的にオフに必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-599">If you run this in a server machine like Windows Server 2016, you must turn off the IE Enhanced Security Configuration temporarily.</span></span> <span data-ttu-id="17e3d-600">そうしないと、Azure ログイン ウィンドウのコンテンツはブロックされます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-600">If you don't, the Azure login window content will be blocked.</span></span>

1. <span data-ttu-id="17e3d-601">Azure PowerShell の最新バージョンをクライアント マシンにダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-601">Download and install the latest version of Azure PowerShell on a client machine.</span></span> <span data-ttu-id="17e3d-602">詳細については [Azure PowerShell サービス管理モジュールのインストール](https://docs.microsoft.com/powershell/azure/servicemanagement/install-azure-ps?view=azuresmps-4.0.0) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-602">For more information, see [Installing the Azure PowerShell Service Management module](https://docs.microsoft.com/powershell/azure/servicemanagement/install-azure-ps?view=azuresmps-4.0.0).</span></span>
2. <span data-ttu-id="17e3d-603">[顧客の Azure ポータル](https://portal.azure.com) にサインインして、グローバル管理者ディレクトリの役割があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-603">Sign in to the [customer's Azure portal](https://portal.azure.com) to verify that you have the Global Administrator directory role.</span></span>
3. <span data-ttu-id="17e3d-604">**インフラストラクチャ**フォルダから次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-604">Run the following script from the **Infrastructure** folder.</span></span>
    ```powershell
    Install-Module AzureRM
    Import-Module AzureRM
    .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
    ```

### <a name="setupfile"></a> <span data-ttu-id="17e3d-605">12.ファイル ストレージの設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-605">12. Set up file storage</span></span>

<span data-ttu-id="17e3d-606">以下の SMB 3.0 ファイル共有を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-606">You must set up the following SMB 3.0 file shares:</span></span>

- <span data-ttu-id="17e3d-607">AOS にアップロードされるユーザー ドキュメントを格納するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\aos-storage)。</span><span class="sxs-lookup"><span data-stu-id="17e3d-607">A file share that stores user documents that are uploaded to AOS (for example, \\\\DAX7SQLAOFILE1\\aos-storage).</span></span>
- <span data-ttu-id="17e3d-608">デプロイメントを調整するための最新のビルド ファイルと構成ファイルを保存するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\agent)。</span><span class="sxs-lookup"><span data-stu-id="17e3d-608">A file share that stores the latest build and configuration files to orchestrate the deployment (for example, \\\\DAX7SQLAOFILE1\\agent).</span></span>

    > [!WARNING]
    > <span data-ttu-id="17e3d-609">共有に入れるファイルの最大パス長を超えないように、このファイル共有パスはできるだけ短くしておいてください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-609">Keep this file share path as short as possible to avoid exceeding the maximum path length on the files that will be put in the share.</span></span>

<span data-ttu-id="17e3d-610">SMB 3.0 を有効にする方法については、[SMB セキュリティの強化](https://technet.microsoft.com/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-610">For information about how to enable SMB 3.0, see [SMB Security Enhancements](https://technet.microsoft.com/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="17e3d-611">セキュリティで保護されたダイアレクト ネゴシエーションでは、SMB 2.0 または 3.0 から SMB 1.0 へのダウングレードを検出または防止できません。</span><span class="sxs-lookup"><span data-stu-id="17e3d-611">Secure dialect negotiation can't detect or prevent downgrades from SMB 2.0 or 3.0 to SMB 1.0.</span></span> <span data-ttu-id="17e3d-612">したがって、SMB 1.0 サーバーを無効にすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-612">Therefore, we strongly recommend that you disable the SMB 1.0 server.</span></span> <span data-ttu-id="17e3d-613">SMB 1.0 サーバーを無効にすることで、SMB 暗号化のすべての機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-613">By disabling the SMB 1.0 server, you can take advantage of the full capabilities of SMB encryption.</span></span>
> - <span data-ttu-id="17e3d-614">環境内の残りの部分でデータが保護されていることを保証するために、BitLocker ドライブ暗号化をすべてのマシンで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-614">To help ensure that your data is protected while it's at rest in your environment, BitLocker Drive Encryption must be enabled on every machine.</span></span> <span data-ttu-id="17e3d-615">BitLocker を有効にする方法については、[BitLocker: Windows Server 2012 以降で配置する方法](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-615">For information about how to enable BitLocker, see [BitLocker: How to deploy on Windows Server 2012 and later](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server).</span></span>

1. <span data-ttu-id="17e3d-616">ファイル共有マシンで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-616">On the file share machine, run the following command.</span></span>

    ```powershell
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```

2. <span data-ttu-id="17e3d-617">\\\\DAX7SQLAOFILE1\\aos-storage ファイル共有を設定するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="17e3d-617">Follow these steps to set up the \\\\DAX7SQLAOFILE1\\aos-storage file share:</span></span>

   1. <span data-ttu-id="17e3d-618">サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-618">In Server Manager, select **File and Storage Services** \> **Shares**.</span></span>
   2. <span data-ttu-id="17e3d-619">**タスク**\>**新しい共有** を選択し、新しい共有を作成します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-619">Select **Tasks** \> **New Share** to create a new share.</span></span> <span data-ttu-id="17e3d-620">共有に **aos-storage** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-620">Name the share **aos-storage**.</span></span>
   3. <span data-ttu-id="17e3d-621">**共有のキャッシュを許可**を選択したままにします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-621">Leave **Allow caching of share** selected.</span></span>
   4. <span data-ttu-id="17e3d-622">**データ アクセスを暗号化**を確認してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-622">Check **Encrypt data access**.</span></span>
   5. <span data-ttu-id="17e3d-623">OrchestratorType を除いて、Service Fabric クラスター内のすべてのマシンに対して**変更**許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-623">Grant **Modify** permissions for every machine in the Service Fabric cluster except OrchestratorType.</span></span>
   6. <span data-ttu-id="17e3d-624">AOS ドメイン ユーザー (contoso\\AXServiceUser) と gMSA ユーザー (contoso\\svc-AXSF$) に対して、**変更**アクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-624">Grant **Modify** permissions for the user AOS domain user (contoso\\AXServiceUser) and the gMSA user (contoso\\svc-AXSF$).</span></span>

      >[!NOTE]
      > <span data-ttu-id="17e3d-625">マシンを追加するために**オブジェクト タイプ**の下の**コンピューター**を、またはサービス アカウントを追加するために**オブジェクト タイプ**下の**サービス アカウント**を有効にする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-625">You may need to enable **Computers** under **Object Types** to add machines or enable **Service Accounts** under **Object Types** to add service accounts.</span></span>

3. <span data-ttu-id="17e3d-626">\\\\DAX7SQLAOFILE1\\ エージェント ファイル共有を設定するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="17e3d-626">Follow these steps to set up the \\\\DAX7SQLAOFILE1\\agent file share:</span></span>

    1. <span data-ttu-id="17e3d-627">サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-627">In Server Manager, select **File and Storage Services** \> **Shares**.</span></span>
    2. <span data-ttu-id="17e3d-628">**タスク**\>**新しい共有** を選択し、新しい共有を作成します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-628">Select **Tasks** \> **New Share** to create a new share.</span></span> <span data-ttu-id="17e3d-629">共有に**エージェント**と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-629">Name the share **agent**.</span></span>
    3. <span data-ttu-id="17e3d-630">ローカル展開エージェント (contoso\\svc-LocalAgent$) の gMSA ユーザーに対して **フル コントロール** のアクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-630">Grant **Full-Control** permissions to the gMSA user for the local deployment agent (contoso\\svc-LocalAgent$).</span></span>

    ```PowerShell
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

### <a name="setupsql"></a> <span data-ttu-id="17e3d-631">13. SQL Server の設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-631">13. Set up SQL Server</span></span>

1. <span data-ttu-id="17e3d-632">高可用性を備えた SQL Server 2016 SP1 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-632">Install SQL Server 2016 SP1 with high availability.</span></span> <span data-ttu-id="17e3d-633">(SQL Server の 1 つのインスタンスで十分なサンドボックス環境に配置している場合を除きます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-633">(Unless you're deploying in a sandbox environment, where one instance of SQL Server is sufficient.</span></span> <span data-ttu-id="17e3d-634">高可用性シナリオをテストするため、サンドボックス環境に高可用性の SQL Server をインストールできます。)</span><span class="sxs-lookup"><span data-stu-id="17e3d-634">You may want to install SQL Server with high availability in sandbox environments to test high-availability scenarios.)</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="17e3d-635">[SQL Server および Windows 認証モード](https://docs.microsoft.com/sql/database-engine/configure-windows/change-server-authentication-mode) を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-635">You must enable the [SQL Server and Windows Authentication mode](https://docs.microsoft.com/sql/database-engine/configure-windows/change-server-authentication-mode).</span></span>

    <span data-ttu-id="17e3d-636">高可用性を備えた SQL Server を、SAN (ストレージ エリア ネットワーク) を含む SQL クラスターまたは Always-On 構成のいずれかとしてインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-636">You can install SQL Server with high availability either as SQL clusters that include a Storage Area Network (SAN) or in an Always-On configuration.</span></span> <span data-ttu-id="17e3d-637">データベース エンジン、SSRS、フルテキスト検索、および管理ツールがインストール済みであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-637">Verify that the Database Engine, SSRS, Full-Text Search, and Management Tools are already installed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="17e3d-638">Always-On が [初期データ同期ページの選択 (可用性グループ ウィザードで常に使用する)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) で説明されているとおりに設定され、[セカンダリ データベースを手動で準備する](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs) の指示に従っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-638">Make sure that Always-On is set up as described in [Select Initial Data Synchronization Page (Always On Availability Group Wizards)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards), and follow the instructions in [To Prepare Secondary Databases Manually](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs).</span></span>

2. <span data-ttu-id="17e3d-639">ドメイン ユーザーとして SQL サービスを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-639">Run the SQL service as a domain user.</span></span>
3. <span data-ttu-id="17e3d-640">Finance + Operations を構成するために証明機関から SSL 証明書を取得します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-640">Get an SSL certificate from a certificate authority to configure Finance + Operations.</span></span> <span data-ttu-id="17e3d-641">テストの目的で、自己署名証明書を作成して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-641">For testing purposes, you can create and use a self-signed certificate.</span></span> <span data-ttu-id="17e3d-642">次の例にあるコンピューター名とドメイン名を置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-642">You will need to replace the computer name and domain name in the following example.</span></span>

    <span data-ttu-id="17e3d-643">**クラスター化された SQL インスタンスの自己署名証明書**</span><span class="sxs-lookup"><span data-stu-id="17e3d-643">**Self-signed certificate for a Clustered SQL instance**</span></span>

    ```powershell
    New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contoso.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contoso.com"
    ```

    <span data-ttu-id="17e3d-644">**Always-On SQL インスタンスの自己署名証明書**</span><span class="sxs-lookup"><span data-stu-id="17e3d-644">**Self-signed certificate for an Always-On SQL instance**</span></span>

    <span data-ttu-id="17e3d-645">Always-On のテスト証明書を設定する場合は、以下の**リモート**スクリプトを使用できます。これは、**マニュアル**スクリプトおよび手順 **4.**、**5.**、**6.** と同じ方法で実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-645">If setting up testing certificates for Always-On, you can use the following **remoting** script, which will perform the same as the following **manual** script and steps **4.**, **5.**, and **6.**.</span></span>

    ```powershell
    .\Create-SQLTestCert-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml `
        -SqlMachineNames DAX7SQLAOSQLA01, DAX7SQLAOSQLA02 `
        -SqlListenerName dax7sqlaosqla
    ```

    <span data-ttu-id="17e3d-646">テスト証明書の**手動**作成。</span><span class="sxs-lookup"><span data-stu-id="17e3d-646">**Manual** creation of test certificates.</span></span>
    ```powershell
    # https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

    # Manually create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
    # Run script on each node
    $computerName = $env:COMPUTERNAME.ToLower()
    $domain = $env:USERDNSDOMAIN.ToLower()
    $listenerName = 'dax7sqlaosqla'
    $cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'
    ```

4. <span data-ttu-id="17e3d-647">SQL サーバーで SSL を構成するには、証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-647">Use the certificate(s) to configure SSL on SQL Server.</span></span> <span data-ttu-id="17e3d-648">[Microsoft 管理コンソールを使用して SQL Server のインスタンスに対する SSL 暗号化を有効にする方法](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="17e3d-648">Follow the steps in [How to enable SSL encryption for an instance of SQL Server by using Microsoft Management Console](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console).</span></span>
5. <span data-ttu-id="17e3d-649">SQL クラスターの各ノードに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-649">For each node of the SQL cluster, follow these steps.</span></span> <span data-ttu-id="17e3d-650">非アクティブなノードで変更を加えて、変更が行われた後フェール オーバーするようにしてください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-650">Make sure that you make the changes on the non-active node, and that you fail over to it after changes are made.</span></span>

    1. <span data-ttu-id="17e3d-651">LocalMachine\\My に証明書をインポートします。Always-On を設定していない限り、証明書は既にノードに存在します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-651">Import the certificate into LocalMachine\\My, unless you are setting up Always-On, in which case the certificate already exists on the node.</span></span>
    2. <span data-ttu-id="17e3d-652">SQL サービスを実行するために使用されるサービス アカウントに証明書のアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-652">Grant certificate permissions to the service account that is used to run the SQL service.</span></span> <span data-ttu-id="17e3d-653">Microsoft 管理コンソール (MMC) で証明書 (**certlm.msc**) を右クリックし、**タスク** \> **秘密キーの管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-653">In Microsoft Management Console (MMC), right-click the certificate (**certlm.msc**), and then select **Tasks** \> **Manage Private Keys**.</span></span>
    3. <span data-ttu-id="17e3d-654">証明書の拇印を HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate に追加します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-654">Add the certificate thumbprint to HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.</span></span> <span data-ttu-id="17e3d-655">たとえば、SQL Server 2016 SP1: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\MSSQL13.MSSQLSERVER\\MSSQLServer\\SuperSocketNetLib\\Certificate</span><span class="sxs-lookup"><span data-stu-id="17e3d-655">For example, with SQL Server 2016 SP1: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\MSSQL13.MSSQLSERVER\\MSSQLServer\\SuperSocketNetLib\\Certificate</span></span>
        1. <span data-ttu-id="17e3d-656">スタート メニューから、**regedit** をタイプし、**regedit** を選択してレジストリ エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-656">From the start menu, type **regedit**, then select **regedit** to open the registry editor.</span></span>
        2. <span data-ttu-id="17e3d-657">証明書に移動し、**変更**を右クリックしてから、証明書の拇印に値を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-657">Navigate to the certificate, right-click **Modify**, then replace the value with the certificate thumbprint.</span></span>
    4. <span data-ttu-id="17e3d-658">Microsoft SQL Server 構成マネージャーで、**ForceEncryption** を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-658">In Microsoft SQL Server Configuration Manager, set **ForceEncryption** to **Yes**.</span></span>
        1. <span data-ttu-id="17e3d-659">**SQL Server 構成マネージャー**で、**SQL Server ネットワークの構成**を展開し、**サーバーのインスタンスのプロトコル**を右クリックしてから、**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-659">In **SQL Server Configuration Manager**, expand **SQL Server Network Configuration**, right-click **Protocols for [server instance]**, and then select **Properties**.</span></span>
        2. <span data-ttu-id="17e3d-660">**インスタンス名プロパティのプロトコル**ダイアログ ボックスの**証明書**タブで、**証明書**ボックスのドロップダウン メニューから目的の証明書を選択して、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-660">In the **Protocols for [instance name] Properties** dialog box, on the **Certificate** tab, select the desired certificate from the drop-down menu for the **Certificate** box, and then click **OK**.</span></span>
        3. <span data-ttu-id="17e3d-661">**フラグ**タブの **ForceEncryption** ボックスで、**はい**を選択してから、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-661">On the **Flags** tab, in the **ForceEncryption** box, select **Yes**, and then click **OK**</span></span>
        4. <span data-ttu-id="17e3d-662">SQL Server サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-662">Restart the SQL Server service.</span></span>

6. <span data-ttu-id="17e3d-663">証明書の公開鍵 (.cer ファイル) をエクスポートし、各 Service Fabric ノードの信頼できるルートにインストールします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-663">Export the public key of the certificate (the .cer file), and install it in the trusted root of each Service Fabric node.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17e3d-664">リモート処理を使用していた場合は、設定が完了するとクリーンアップ手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-664">If remoting was used, be sure to execute the clean up steps when the setup is complete.</span></span> <span data-ttu-id="17e3d-665">詳細については、[20. CredSSP を終章処理する](#teardowncredssp) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-665">See the [20. Tear down CredSSP](#teardowncredssp) section for more information.</span></span>

### <a name="configuredb"></a> <span data-ttu-id="17e3d-666">14. データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="17e3d-666">14. Configure the databases</span></span>

1. <span data-ttu-id="17e3d-667">[LCS](https://lcs.dynamics.com/v2) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-667">Sign in to [LCS](https://lcs.dynamics.com/v2).</span></span>

2. <span data-ttu-id="17e3d-668">ダッシュボードで、**共有アセット ライブラリ**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-668">On the dashboard, select the **Shared asset library** tile.</span></span>

3. <span data-ttu-id="17e3d-669">**モデル**タブで、必要なリリースのデモ データを選択し、zip ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-669">On the **Model** tab, select the demo data for the release that you want and download the zip file.</span></span>

| <span data-ttu-id="17e3d-670">リリース</span><span class="sxs-lookup"><span data-stu-id="17e3d-670">Release</span></span> | <span data-ttu-id="17e3d-671">デモ データ</span><span class="sxs-lookup"><span data-stu-id="17e3d-671">Demo data</span></span> |
|-------|------|
| <span data-ttu-id="17e3d-672">オンプレミスの一般提供 (GA) リリース</span><span class="sxs-lookup"><span data-stu-id="17e3d-672">On-premises General Availability (GA) release</span></span> | <span data-ttu-id="17e3d-673">Dynamics 365 for Operations オンプレミス - デモ データ</span><span class="sxs-lookup"><span data-stu-id="17e3d-673">Dynamics 365 for Operations on-premises - Demo data</span></span> |
| <span data-ttu-id="17e3d-674">オンプレミスのプラットフォーム更新プログラム 2017 年 11 月 11 日リリース</span><span class="sxs-lookup"><span data-stu-id="17e3d-674">On-premises Platform Update 11 Nov 2017 release</span></span> | <span data-ttu-id="17e3d-675">Dynamics 365 for Operations オンプレミス Enterprise Edition - 更新プログラム 11 デモ データ</span><span class="sxs-lookup"><span data-stu-id="17e3d-675">Dynamics 365 for Operations on-premises, Enterprise edition - Update 11 Demo data</span></span> |
| <span data-ttu-id="17e3d-676">オンプレミスのプラットフォーム更新プログラム 2018 年 3 月 12 日リリース</span><span class="sxs-lookup"><span data-stu-id="17e3d-676">On-premises Platform Update 12 Mar 2018 release</span></span> | <span data-ttu-id="17e3d-677">Dynamics 365 for Operations オンプレミス Enterprise Edition - 更新プログラム 12 デモ データ</span><span class="sxs-lookup"><span data-stu-id="17e3d-677">Dynamics 365 for Operations on-premises, Enterprise edition - Update 12 Demo data</span></span> |

4. <span data-ttu-id="17e3d-678">zip ファイルには空のデモデータ .bak ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="17e3d-678">The zip file contains empty and demo data .bak files.</span></span> <span data-ttu-id="17e3d-679">必要に応じて、.bak ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-679">Select the .bak file, based on your requirements.</span></span> <span data-ttu-id="17e3d-680">たとえば、デモ データが必要な場合は、AxBootstrapDB_Demodata.bak ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-680">For example, if you require demo data, download the AxBootstrapDB_Demodata.bak file.</span></span>

5. <span data-ttu-id="17e3d-681">infrastructure\ConfigTempate.xml のデータベース セクションが、次のように正しく構成されているか確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-681">Ensure the database section in the infrastructure\ConfigTempate.xml is configured correctly with the following:</span></span>
    1. <span data-ttu-id="17e3d-682">データベース名。</span><span class="sxs-lookup"><span data-stu-id="17e3d-682">The database name.</span></span>
    2. <span data-ttu-id="17e3d-683">db ファイルとログ設定。</span><span class="sxs-lookup"><span data-stu-id="17e3d-683">The db file and log settings.</span></span> <span data-ttu-id="17e3d-684">dbの設定は、指定された既定値以上にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-684">The db settings should not be lower than the defaults specified.</span></span>
    3. <span data-ttu-id="17e3d-685">LCS 共有アセット ライブラリからダウンロードされるバックアップ ファイルへのパス。</span><span class="sxs-lookup"><span data-stu-id="17e3d-685">The path to the backup file downloaded from LCS Shared Asset library.</span></span> <span data-ttu-id="17e3d-686">Finance + Operations データベースの既定の名前は AXDB です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-686">The default name for the Finance + Operations database is AXDB.</span></span>

   > [!WARNING]
   > - <span data-ttu-id="17e3d-687">SQL サービスを実行しているユーザーとスクリプトを実行しているユーザーは、バックアップ ファイルが格納されているフォルダーまたは共有に対して READ アクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-687">The user running the SQL service and the user running the scripts should have READ access on the folder or share where the backup file is located.</span></span>
   > 
   > - <span data-ttu-id="17e3d-688">同じ名前のデータベースが存在する場合は、データベースが再利用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-688">If a database with the same name exists, the database will be reused.</span></span>

6. <span data-ttu-id="17e3d-689">**インフラストラクチャ**フォルダーを SQL Server マシンにコピーし、権限を昇格した PowerShell ウィンドウでそのフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-689">Copy the **infrastructure** folder to the SQL Server machine and navigate to it in a PowerShell window with elevate privileges.</span></span>

#### <a name="configure-the-orchestratordata-database"></a><span data-ttu-id="17e3d-690">OrchestratorData データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="17e3d-690">Configure the OrchestratorData database</span></span>

1. <span data-ttu-id="17e3d-691">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-691">Execute the following script.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
   ```

   <span data-ttu-id="17e3d-692">スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="17e3d-692">The script will do the following:</span></span>
  
   - <span data-ttu-id="17e3d-693">**OrchestratorData** という名前の空のデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-693">Create an empty database named **OrchestratorData**.</span></span> <span data-ttu-id="17e3d-694">このデータベースは、オンプレミスのローカル エージェントによって配置を調整するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-694">This database is used by the on-premises local agent to orchestrate deployments.</span></span>
   - <span data-ttu-id="17e3d-695">データベースにローカル エージェント gMSA (svc-LocalAgent$) **db\_owner** アクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-695">Grant the local agent gMSA (svc-LocalAgent$) **db\_owner** permissions on the database.</span></span>

#### <a name="configure-the-finance--operations-database"></a><span data-ttu-id="17e3d-696">Finance + Operations データベースの構成</span><span class="sxs-lookup"><span data-stu-id="17e3d-696">Configure the Finance + Operations database</span></span>

1. <span data-ttu-id="17e3d-697">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-697">Execute the following scripts.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
   .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
   ```

   <span data-ttu-id="17e3d-698">**Initialize-Database.ps1** スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="17e3d-698">The **Initialize-Database.ps1** script will do the following:</span></span>

   1. <span data-ttu-id="17e3d-699">指定されたバックアップ ファイルからデータベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-699">Restore the database from the specified backup file.</span></span>
   2. <span data-ttu-id="17e3d-700">SQL 認証が有効になっている新しいユーザーを作成します (axdbadmin)。</span><span class="sxs-lookup"><span data-stu-id="17e3d-700">Create a new user that has SQL authentication enabled (axdbadmin).</span></span>
   3. <span data-ttu-id="17e3d-701">AXDB の次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-701">Map users to database roles based on the following table for AXDB.</span></span>

      | <span data-ttu-id="17e3d-702">ユーザー</span><span class="sxs-lookup"><span data-stu-id="17e3d-702">User</span></span>            | <span data-ttu-id="17e3d-703">種類</span><span class="sxs-lookup"><span data-stu-id="17e3d-703">Type</span></span>    | <span data-ttu-id="17e3d-704">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="17e3d-704">Database role</span></span> |
      |-----------------|---------|---------------|
      | <span data-ttu-id="17e3d-705">svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="17e3d-705">svc-AXSF$</span></span>       | <span data-ttu-id="17e3d-706">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-706">gMSA</span></span>    | <span data-ttu-id="17e3d-707">db\_owner</span><span class="sxs-lookup"><span data-stu-id="17e3d-707">db\_owner</span></span>     |
      | <span data-ttu-id="17e3d-708">svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="17e3d-708">svc-LocalAgent$</span></span> | <span data-ttu-id="17e3d-709">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-709">gMSA</span></span>    | <span data-ttu-id="17e3d-710">db\_owner</span><span class="sxs-lookup"><span data-stu-id="17e3d-710">db\_owner</span></span>     |
      | <span data-ttu-id="17e3d-711">svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="17e3d-711">svc-FRPS$</span></span>       | <span data-ttu-id="17e3d-712">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-712">gMSA</span></span>    | <span data-ttu-id="17e3d-713">db\_owner</span><span class="sxs-lookup"><span data-stu-id="17e3d-713">db\_owner</span></span>     |
      | <span data-ttu-id="17e3d-714">svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="17e3d-714">svc-FRAS$</span></span>       | <span data-ttu-id="17e3d-715">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-715">gMSA</span></span>    | <span data-ttu-id="17e3d-716">db\_owner</span><span class="sxs-lookup"><span data-stu-id="17e3d-716">db\_owner</span></span>     |
      | <span data-ttu-id="17e3d-717">axdbadmin</span><span class="sxs-lookup"><span data-stu-id="17e3d-717">axdbadmin</span></span>       | <span data-ttu-id="17e3d-718">SqlUser</span><span class="sxs-lookup"><span data-stu-id="17e3d-718">SqlUser</span></span> | <span data-ttu-id="17e3d-719">db\_owner</span><span class="sxs-lookup"><span data-stu-id="17e3d-719">db\_owner</span></span>     |


   4. <span data-ttu-id="17e3d-720">TempDB の次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-720">Map users to database roles based on the following table for TempDB.</span></span>

      | <span data-ttu-id="17e3d-721">ユーザー</span><span class="sxs-lookup"><span data-stu-id="17e3d-721">User</span></span>            | <span data-ttu-id="17e3d-722">種類</span><span class="sxs-lookup"><span data-stu-id="17e3d-722">Type</span></span>    | <span data-ttu-id="17e3d-723">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="17e3d-723">Database role</span></span> |
      |-----------------|---------|---------------|
      | <span data-ttu-id="17e3d-724">svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="17e3d-724">svc-AXSF$</span></span>       | <span data-ttu-id="17e3d-725">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-725">gMSA</span></span>    | <span data-ttu-id="17e3d-726">db_datareader, db_datawriter, db_ddladmin</span><span class="sxs-lookup"><span data-stu-id="17e3d-726">db_datareader, db_datawriter, db_ddladmin</span></span>     |
      | <span data-ttu-id="17e3d-727">axdbadmin</span><span class="sxs-lookup"><span data-stu-id="17e3d-727">axdbadmin</span></span>       | <span data-ttu-id="17e3d-728">SqlUser</span><span class="sxs-lookup"><span data-stu-id="17e3d-728">SqlUser</span></span> | <span data-ttu-id="17e3d-729">db_datareader, db_datawriter, db_ddladmin</span><span class="sxs-lookup"><span data-stu-id="17e3d-729">db_datareader, db_datawriter, db_ddladmin</span></span>     |

   <span data-ttu-id="17e3d-730">**Configure-Database.ps1** スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="17e3d-730">The **Configure-Database.ps1** script will do the following:</span></span>

    1. <span data-ttu-id="17e3d-731">READ_COMMITTED_SNAPSHOT ON を設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-731">Set READ_COMMITTED_SNAPSHOT ON</span></span>
    2. <span data-ttu-id="17e3d-732">ALLOW_SNAPSHOT_ISOLATION ON を設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-732">Set ALLOW_SNAPSHOT_ISOLATION ON</span></span>
    3. <span data-ttu-id="17e3d-733">指定したデータベース ファイルとログの設定を設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-733">Set the specified database file and log settings</span></span>
    4. <span data-ttu-id="17e3d-734">サーバー状態の表示を axdbadmin に付与</span><span class="sxs-lookup"><span data-stu-id="17e3d-734">GRANT VIEW SERVER STATE TO axdbadmin</span></span>
    5. <span data-ttu-id="17e3d-735">サーバー状態の表示を [contoso\svc AXSF$] に付与</span><span class="sxs-lookup"><span data-stu-id="17e3d-735">GRANT VIEW SERVER STATE TO [contoso\svc-AXSF$]</span></span>

2. <span data-ttu-id="17e3d-736">データベース ユーザーをリセットするには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-736">Run the following command to reset the database users.</span></span>

    ```powershell
    .\Reset-DatabaseUsers.ps1 -DatabaseServer '<FQDN of the SQL server>' -DatabaseName '<AX database name>'
    ```

#### <a name="configure-the-financial-reporting-database"></a><span data-ttu-id="17e3d-737">財務レポート データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="17e3d-737">Configure the Financial Reporting database</span></span>

1. <span data-ttu-id="17e3d-738">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-738">Execute the following script.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName MR
   ```

   <span data-ttu-id="17e3d-739">スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="17e3d-739">The script will do the following:</span></span>
   1. <span data-ttu-id="17e3d-740">**FinancialReporting** という名前の空のデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-740">Create an empty database named **FinancialReporting**.</span></span>
   2. <span data-ttu-id="17e3d-741">次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-741">Map the users to database roles based on the following table.</span></span>

      | <span data-ttu-id="17e3d-742">ユーザー</span><span class="sxs-lookup"><span data-stu-id="17e3d-742">User</span></span>            | <span data-ttu-id="17e3d-743">種類</span><span class="sxs-lookup"><span data-stu-id="17e3d-743">Type</span></span> | <span data-ttu-id="17e3d-744">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="17e3d-744">Database role</span></span> |
      |-----------------|------|---------------|
      | <span data-ttu-id="17e3d-745">svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="17e3d-745">svc-LocalAgent$</span></span> | <span data-ttu-id="17e3d-746">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-746">gMSA</span></span> | <span data-ttu-id="17e3d-747">db\_owner</span><span class="sxs-lookup"><span data-stu-id="17e3d-747">db\_owner</span></span>     |
      | <span data-ttu-id="17e3d-748">svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="17e3d-748">svc-FRPS$</span></span>       | <span data-ttu-id="17e3d-749">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-749">gMSA</span></span> | <span data-ttu-id="17e3d-750">db\_owner</span><span class="sxs-lookup"><span data-stu-id="17e3d-750">db\_owner</span></span>     |
      | <span data-ttu-id="17e3d-751">svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="17e3d-751">svc-FRAS$</span></span>       | <span data-ttu-id="17e3d-752">gMSA</span><span class="sxs-lookup"><span data-stu-id="17e3d-752">gMSA</span></span> | <span data-ttu-id="17e3d-753">db\_owner</span><span class="sxs-lookup"><span data-stu-id="17e3d-753">db\_owner</span></span>     |

### <a name="encryptcred"></a> <span data-ttu-id="17e3d-754">15. 資格情報の暗号化</span><span class="sxs-lookup"><span data-stu-id="17e3d-754">15. Encrypt credentials</span></span>

1. <span data-ttu-id="17e3d-755">任意のクライアント マシンで、LocalMachine\\My certificate store に暗号化証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-755">On any client machine, install the encipherment certificate in the LocalMachine\\My certificate store.</span></span>
2. <span data-ttu-id="17e3d-756">現在のユーザーにこの証明書の秘密キーへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-756">Grant the current user read access to the private key of this certificate.</span></span>
3. <span data-ttu-id="17e3d-757">次のようにして、Credentials.json ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-757">Create the Credentials.json file, as shown here.</span></span>

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

    - <span data-ttu-id="17e3d-758">**AccountPassword** は、AOS ドメインユーザー (contoso\\axserviceuser) の暗号化されたドメイン ユーザー パスワードです。</span><span class="sxs-lookup"><span data-stu-id="17e3d-758">**AccountPassword** is the encrypted domain user password for the AOS domain user (contoso\\axserviceuser).</span></span>
    - <span data-ttu-id="17e3d-759">**SqlUser** は、Finance + Operations データベース (AXDB) にアクセスできる暗号化された SQL ユーザー (axdbadmin) で、**SqlPassword** は暗号化された SQL パスワードです。</span><span class="sxs-lookup"><span data-stu-id="17e3d-759">**SqlUser** is the encrypted SQL user (axdbadmin) that has access to the Finance + Operations database (AXDB), and **SqlPassword** is the encrypted SQL password.</span></span>

4. <span data-ttu-id="17e3d-760">.json ファイルを SMB ファイル共有、\\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json にコピーします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-760">Copy the .json file to the SMB file share, \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.</span></span>
5. <span data-ttu-id="17e3d-761">暗号化された値で Credentials.json ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-761">Update the Credentials.json file with encrypted values.</span></span>

    ```powershell
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | Set-Clipboard
    ```
    > [!IMPORTANT]
    > <span data-ttu-id="17e3d-762">*Invoke-ServiceFabricEncryptText* を起動する前に、[Microsoft Azure Service Fabric SDK](https://docs.microsoft.com/azure/service-fabric/service-fabric-get-started#sdk-installation-only) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-762">Before you can invoke *Invoke-ServiceFabricEncryptText*, you need to install [Microsoft Azure Service Fabric SDK](https://docs.microsoft.com/azure/service-fabric/service-fabric-get-started#sdk-installation-only).</span></span>
    > <span data-ttu-id="17e3d-763">Azure Service Fabric SDK をインストールした後で、"Invoke-ServiceFabricEncryptText は認識されないコマンドです" というエラーが発生した場合は、コンピューターを再起動して再試行してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-763">If you encounter the following error, "Invoke-ServiceFabricEncryptText is not recognized command" after you install the Azure Service Fabric SDK, restart the computer and retry.</span></span>

### <a name="setupssis"></a> <span data-ttu-id="17e3d-764">16. SSIS の設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-764">16. Set up SSIS</span></span>

<span data-ttu-id="17e3d-765">データ管理と統合ワークロードを有効にするには、各 AOS 仮想マシンに SSIS をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-765">To enable Data management and Integration workloads, SSIS must be installed on each of the AOS virtual machines.</span></span> <span data-ttu-id="17e3d-766">各 AOS 仮想マシン上で、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-766">Complete the following steps on each AOS virtual machine.</span></span>

1. <span data-ttu-id="17e3d-767">マシンに SSIS インストールへのアクセス許可があることを確認し、SSIS セットアップ ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-767">Verify that the machine has access to the SSIS installation and open the SSIS Setup Wizard.</span></span>
2. <span data-ttu-id="17e3d-768">**機能の選択**ウィンドウの**機能**ウィンドウで、**Integration Services** および **SQL クライアント接続 SDK** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-768">In the **Feature Selection** window, in the **Features** pane, select the **Integration Services** and **SQL Client Connectivity SDK** check boxes.</span></span>
3. <span data-ttu-id="17e3d-769">セットアップを完了し、インストールが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-769">Complete the setup and verify that the installation was successful.</span></span>

<span data-ttu-id="17e3d-770">詳細については、[統合サービスのインストール](https://docs.microsoft.com/sql/integration-services/install-windows/install-integration-services) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-770">For more information, see [Install integration services](https://docs.microsoft.com/sql/integration-services/install-windows/install-integration-services).</span></span>

### <a name="setupssrs"></a> <span data-ttu-id="17e3d-771">17. SSRS の設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-771">17. Set up SSRS</span></span>

1. <span data-ttu-id="17e3d-772">開始する前に、このトピックの冒頭に記載されている前提条件がインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-772">Before you begin, make sure that the prerequisites that are listed at the beginning of this topic are installed.</span></span>
2. <span data-ttu-id="17e3d-773">[オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション](../analytics/configure-ssrs-on-premises.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="17e3d-773">Follow the steps in [Configure SQL Server Reporting Services for an on-premises deployment](../analytics/configure-ssrs-on-premises.md).</span></span>
    > [!IMPORTANT]
    > <span data-ttu-id="17e3d-774">SSRS のインストール時にデータベース エンジンをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-774">You must install then database engine when you install SSRS.</span></span>

### <a name="configureadfs"></a><span data-ttu-id="17e3d-775">18. AD FS のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="17e3d-775">18. Configure AD FS</span></span>

<span data-ttu-id="17e3d-776">この手順を完了する前に、AD FS を Windows Server 2016 に展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-776">Before you can complete this procedure, AD FS must be deployed on Windows Server 2016.</span></span> <span data-ttu-id="17e3d-777">AD FS を展開する方法については、[Windows Server 2016 配置ガイドおよび 2012 R2 AD FS 配置ガイド](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-777">For information about how to deploy AD FS, see [Deployment Guide Windows Server 2016 and 2012 R2 AD FS Deployment Guide](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).</span></span>

<span data-ttu-id="17e3d-778">Finance + Operations では、AD FS の既定で標準のコンフィギュレーション以外の追加のコンフィギュレーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-778">Finance + Operations requires additional configuration beyond the default out-of-box configuration of AD FS.</span></span> <span data-ttu-id="17e3d-779">以下の Windows PowerShell コマンドを、AD FS ロール サービスがインストールされているマシン上で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-779">The following Windows PowerShell commands must be run on the machine where the AD FS role service is installed.</span></span> <span data-ttu-id="17e3d-780">ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-780">The user account must have enough permissions to administer AD FS.</span></span> <span data-ttu-id="17e3d-781">たとえば、ユーザーには、ドメイン管理者アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-781">For example, the user must have a domain administrator account.</span></span> <span data-ttu-id="17e3d-782">複雑な AD FS シナリオでは、ドメイン管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-782">For complex AD FS scenarios, consult your domain administrator.</span></span>

1. <span data-ttu-id="17e3d-783">AD FS 識別子を構成して、AD FS トークン発行者と一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-783">Configure the AD FS identifier so that it matches the AD FS token issuer.</span></span>

   <span data-ttu-id="17e3d-784">このコマンドは、Finance + Operations クライアントの**ユーザー** ページ (**システム管理 > ユーザー > ユーザー**) で**ユーザーをインポート** オプションを使用した新しいユーザーの追加に関連しています。</span><span class="sxs-lookup"><span data-stu-id="17e3d-784">This command is related to adding new users using the **Import users** option on the **Users** page (**System administration > Users > Users**) in the Finance + Operations client.</span></span>

    ```PowerShell
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. <span data-ttu-id="17e3d-785">混在環境用に AD FS を構成していない限り、イントラネット認証接続用に Windows 統合認証 (WIA) を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-785">You should disable Windows Integrated Authentication (WIA) for intranet authentication connections, unless you've configured AD FS for mixed environments.</span></span> <span data-ttu-id="17e3d-786">WIA を AD FS で使用できるように構成する方法の詳細については、[AD FS で Windows 統合認証 (WIA) を使用するようにブラウザを構成する](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-786">For more information about how to configure WIA so that it can be used with AD FS, see [Configure browsers to use Windows Integrated Authentication (WIA) with AD FS](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).</span></span>

   <span data-ttu-id="17e3d-787">このコマンドは、Finance + Operations クライアントへのログイン時のフォーム認証の使用に関連しています。</span><span class="sxs-lookup"><span data-stu-id="17e3d-787">This command is related to using forms authentication upon signing into the Finance + Operations client.</span></span> <span data-ttu-id="17e3d-788">シングル サインオンなど、追加の設定が必要な他のオプションが使用可能な場合があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-788">Other options, such as single sign-on, may be available which require additional setup.</span></span>

    ```powershell
    Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
    ```

3. <span data-ttu-id="17e3d-789">サインインの場合、ユーザーの電子メール アドレスは許容される認証入力でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="17e3d-789">For sign-in, the user's email address must be an acceptable authentication input.</span></span>

   <span data-ttu-id="17e3d-790">このコマンドは、電子メール要求の設定に関連しています。</span><span class="sxs-lookup"><span data-stu-id="17e3d-790">This command is related to setting up email claims.</span></span> <span data-ttu-id="17e3d-791">変換ルールなど、追加の設定が必要な他のオプションが使用可能な場合があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-791">Other options, such as transformation rules, may be available which require additional setup.</span></span>

    ```powershell
    Add-Type -AssemblyName System.Net
    $fqdn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
    $domainName = $fqdn.Substring($fqdn.IndexOf('.')+1)
    Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
    ```

<span data-ttu-id="17e3d-792">AD FS が認証を交換するために Finance + Operations を信頼するためには、AD FS アプリケーション グループの下の AD FS にさまざまなアプリケーション エントリを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-792">In order for AD FS to trust Finance + Operations for the exchange of authentication, various application entries must be registered in AD FS under an AD FS application group.</span></span> <span data-ttu-id="17e3d-793">設定プロセスをスピードアップし、エラーを減らすために、次のスクリプトを使用して登録します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-793">To speed up the setup process and help reduce errors, you can use the following script for registration.</span></span> <span data-ttu-id="17e3d-794">Publish-ADFSApplicationGroup.ps1 スクリプトと D365FO-OP ディレクトリを、AD FS ロール サービスがインストールされているマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-794">Copy the Publish-ADFSApplicationGroup.ps1 script and D365FO-OP directory to a machine where the AD FS role service is installed.</span></span> <span data-ttu-id="17e3d-795">次に、AD FS を管理するための十分なアクセス許可を持つユーザー アカウントを使用してスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-795">Then run the script by using a user account that has enough permissions to administer AD FS.</span></span> <span data-ttu-id="17e3d-796">(たとえば、管理者アカウントを使用します。)</span><span class="sxs-lookup"><span data-stu-id="17e3d-796">(For example, use an administrator account.)</span></span>

<span data-ttu-id="17e3d-797">スクリプトの使用方法の詳細については、スクリプトに記載されているドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-797">For more information about how to use the script, see the documentation that is listed in the script.</span></span> <span data-ttu-id="17e3d-798">後の手順の LCS でこの情報が必要となるため、出力に指定されているクライアント ID を書き留めておいてください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-798">Make a note of the client IDs that are specified in the output, because you will need this information in LCS in a later step.</span></span> <span data-ttu-id="17e3d-799">クライアント ID を紛失した場合、AD FS がインストールされているコンピューターにログインし、**サーバー マネージャー** \> **ツール** \> **AD FS の管理** \> **アプリケーション グループ** \> **Microsoft Dynamics 365 for Operations On-premises**を開き、ネイティブ アプリケーションでクライアント ID を見つけます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-799">Should you lose the client IDs, log in to the machine which has AD FS installed, open **Server Manager** \> **Tools** \> **AD FS Management** \> **Application Groups** \> **Microsoft Dynamics 365 for Operations On-premises** and find the client IDs under the native applications.</span></span>

```powershell
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
```

![アプリケーション グループのプロパティ](./media/OPSetup_05_ApplicatioGroupProperties.png)

<span data-ttu-id="17e3d-801">最後に、**AOSNodeType** タイプの Service Fabric ノード上の AD FS OpenID コンフィギュレーション URL にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-801">Finally, make sure that you can access the AD FS OpenID Configuration URL on a Service Fabric node of the **AOSNodeType** type.</span></span> <span data-ttu-id="17e3d-802">このチェックを行うには、Web ブラウザーで `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` を開きます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-802">To perform this check, try to open `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` in a web browser.</span></span> <span data-ttu-id="17e3d-803">サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていません。</span><span class="sxs-lookup"><span data-stu-id="17e3d-803">If you receive a message that states that the site isn't secure, you haven't added your AD FS SSL certificate to the Trusted Root Certification Authorities store.</span></span> <span data-ttu-id="17e3d-804">このステップについては、「AD FS 展開ガイド」で説明されています。リモーティングを使用している場合は、次のスクリプトを使用して、Service Fabric クラスター内のすべてのノードに証明書をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-804">This step is described in the AD FS deployment guide, and if you are using remoting, you can use the following script to install the certificate on all nodes in the Service Fabric cluster:</span></span>

```powershell
# If remoting, execute
.\Install-ADFSCert-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

<span data-ttu-id="17e3d-805">URL に正常にアクセスすると、AD FS コンフィギュレーションを含む JavaScript Object Notation (JSON) ファイルが返され、AD FS URL が信頼されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-805">If you successfully access the URL, a JavaScript Object Notation (JSON) file is returned that contains your AD FS configuration, and you will see that your AD FS URL is trusted.</span></span>

<span data-ttu-id="17e3d-806">これで、インフラストラクチャの設定を完了しました。</span><span class="sxs-lookup"><span data-stu-id="17e3d-806">You've now completed the setup of the infrastructure.</span></span> <span data-ttu-id="17e3d-807">次のセクションでは、[LCS](https://lcs.dynamics.com) にアクセスしてコネクタを設定し、Finance + Operations 環境を配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-807">The following sections describe how to navigate to [LCS](https://lcs.dynamics.com) to set up your connector and deploy your Finance + Operations environment.</span></span>

### <a name="configureconnector"></a> <span data-ttu-id="17e3d-808">19. コネクタのコンフィギュレーションと、オンプレミスのローカル エージェントのインストール</span><span class="sxs-lookup"><span data-stu-id="17e3d-808">19. Configure a connector and install an on-premises local agent</span></span>

1. <span data-ttu-id="17e3d-809">[LCS](https://lcs.dynamics.com/) にサインインし、オンプレミスの実装プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-809">Sign in to [LCS](https://lcs.dynamics.com/), and open the on-premises implementation project.</span></span>
2. <span data-ttu-id="17e3d-810">ハンバーガー メニューで、**プロジェクト設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-810">On the hamburger menu, select **Project settings**.</span></span>

    ![プロジェクト設定コマンド](./media/OPSetup_06_ProjectSettings.png)

3. <span data-ttu-id="17e3d-812">**オンプレミス コネクタ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-812">Select **On-premises connectors**.</span></span>
4. <span data-ttu-id="17e3d-813">新しいコネクタを作成するには、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-813">Select **Add** to create a new connector.</span></span> 
5. <span data-ttu-id="17e3d-814">**ホスト インフラストラクチャ設定** タブで、エージェント インストーラーをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-814">On the **Setup host infrastructure** tab, download the agent installer.</span></span>

    ![[ホスト インフラストラクチャ設定] タブで、エージェント インストーラー ボタンをダウンロードする](./media/OPSetup_07_DownloadAgentInstaller.png)
6. <span data-ttu-id="17e3d-816">zip ファイルがブロックされていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-816">Verify that the zip file is unblocked.</span></span> <span data-ttu-id="17e3d-817">ファイルを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-817">Right-click the file, and then select **Properties**.</span></span> <span data-ttu-id="17e3d-818">ダイアログ ボックスで**ブロック解除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-818">In the dialog box, select **Unblock**.</span></span>
7. <span data-ttu-id="17e3d-819">**OrchestratorType** タイプの Service Fabric ノードの 1 つでエージェント インストーラーを解凍します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-819">Unzip the agent installer on one of the Service Fabric nodes of the **OrchestratorType** type.</span></span>
8. <span data-ttu-id="17e3d-820">**構成エージェント** タブで、コンフィギュレーションの設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-820">On the **Configure agent** tab, enter the configuration settings.</span></span> <span data-ttu-id="17e3d-821">必要な値を取得するには、そのマシンと構成ファイルにアクセスできる任意のマシンで次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-821">Execute the following script on any machine with access to it and the configuration file, to get the needed values.</span></span>

    ```powershell
    .\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

9. <span data-ttu-id="17e3d-822">コンフィギュレーションを保存し、**コンフィギュレーションのダウンロード** を選択して、localagent-config.json コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-822">Save the configuration, and then select **Download configurations** to download the localagent-config.json configuration file.</span></span>

    ![[エージェントの設定] タブの [コンフィギュレーションのダウンロード] ボタン](./media/OPSetup_08_DownloadConfigurations.png)

10. <span data-ttu-id="17e3d-824">localagent-config.json ファイルを、エージェント インストーラー パッケージが配置されているマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-824">Copy the localagent-config.json file to the machine where the agent installer package is located.</span></span>
11. <span data-ttu-id="17e3d-825">**コマンド プロンプト** ウィンドウで、エージェント インストーラーを含むフォルダーに移動して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-825">In a **Command Prompt** window, run the following command by navigating to the folder that contains the agent installer.</span></span>

    ```powershell
    LocalAgentCLI.exe Install <path of config.json>
    ```

    > [!NOTE]
    > <span data-ttu-id="17e3d-826">このコマンドを実行するユーザーは、OrchestratorData データベースに対して **db\_owner** のアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-826">The user who runs this command must have **db\_owner** permissions on the OrchestratorData database.</span></span>

12. <span data-ttu-id="17e3d-827">ローカル エージェントが正常にインストールされると、LCS のオンプレミス コネクタに戻るようにします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-827">After the local agent is successfully installed, navigate back to your on-premises connector in LCS.</span></span>
13. <span data-ttu-id="17e3d-828">**設定の検証**タブで、**メッセージ エージェント**を選択して、ローカル エージェントへの LCS 接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-828">On the **Validate setup** tab, select **Message agent** to test for LCS connectivity to your local agent.</span></span> <span data-ttu-id="17e3d-829">接続が正常に確立されると、ページは下図のようになります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-829">When a connection is successfully established, the page will resemble the following illustration.</span></span>

    ![エージェントの検証](./media/ValidateAgent.PNG)

### <a name="teardowncredssp"></a> <span data-ttu-id="17e3d-831">20. リモート処理が使用された場合、CredSSP を終了処理する</span><span class="sxs-lookup"><span data-stu-id="17e3d-831">20. Tear down CredSSP, if remoting was used</span></span>

<span data-ttu-id="17e3d-832">セットアップ中にリモート処理スクリプトのいずれかが使用された場合は、セットアップ プロセスの中断時または完了時に、次のスクリプトを実行してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-832">If any of the remoting scripts were used during setup, be sure to execute the following script when there are breaks in the setup process, or the setup has finished.</span></span>

```powershell
.\Disable-CredSSP-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

<span data-ttu-id="17e3d-833">前のリモート PowerShell ウィンドウが誤って終了し、CredSSP が有効にまったままである場合、スクリプトにより、コンフィギュレーション ファイルで指定されたすべてのコンピューター上で無効にされます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-833">If the previous remoting PowerShell window was accidentally closed and CredSSP was left enabled, the script will disable it on all the machines specified in the configuration file.</span></span>

### <a name="deploy"></a> <span data-ttu-id="17e3d-834">21. LCS から Finance + Operations 環境を配置する</span><span class="sxs-lookup"><span data-stu-id="17e3d-834">21. Deploy your Finance + Operations environment from LCS</span></span>

1. <span data-ttu-id="17e3d-835">LCS で、オンプレミス プロジェクトに移動し、**環境** > **サンドボックス**に移動してから**構成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-835">In LCS, navigate to your on-premises project, go to **Environment** > **Sandbox**, and then select **Configure**.</span></span> <span data-ttu-id="17e3d-836">必要な値を取得するには、ADFS および DNS サーバー設定にアクセスする必要があるプライマリ ドメイン コントローラ VM で次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-836">Execute the following script on the primary domain controller VM, which must have access to ADFS and the DNS server settings, to get the needed values.</span></span>

    ```powershell
    .\Get-DeploymentSettings.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. <span data-ttu-id="17e3d-837">新しい展開では、環境のトポロジを選択し、展開を開始するウィザードを完了します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-837">For new deployments, select your environment topology, and then complete the wizard to start your deployment.</span></span>

![配置](./media/Deploy.png)

3. <span data-ttu-id="17e3d-839">既存のプラットフォーム更新プログラム 8 またはプラットフォーム更新プログラム 11 を展開する場合:</span><span class="sxs-lookup"><span data-stu-id="17e3d-839">If you have an existing Platform update 8 or Platform update 11 deployment:</span></span> 
    - <span data-ttu-id="17e3d-840">ローカル エージェントを更新します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-840">Update the local agent.</span></span> <span data-ttu-id="17e3d-841">詳細については、[ローカル エージェントの更新](../lifecycle-services/update-local-agent.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-841">See [Update your local agent](../lifecycle-services/update-local-agent.md) for more details.</span></span>
    - <span data-ttu-id="17e3d-842">LCS からローカル エージェントを検証します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-842">Validate the local agent from LCS.</span></span>
    - <span data-ttu-id="17e3d-843">[環境の再構成](../lifecycle-services/reconfigure-environment.md) の手順を実行しながらプラットフォーム更新プログラム 12 を導入します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-843">Deploy Platform update 12 while going through the steps in [Reconfigure your environment](../lifecycle-services/reconfigure-environment.md).</span></span>
4. <span data-ttu-id="17e3d-844">LCS は準備フェーズ中に環境の Service Fabric アプリケーション パッケージを組み立てます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-844">LCS will assemble the Service Fabric application packages for your environment during the preparation phase.</span></span> <span data-ttu-id="17e3d-845">配置を開始するローカル エージェントにメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-845">It then sends a message to the local agent to start deployment.</span></span> <span data-ttu-id="17e3d-846">下記のように、**準備中** ステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-846">You will notice the **Preparing** status as below.</span></span>

![準備中](./media/Preparing.png)

<span data-ttu-id="17e3d-848">以下に示すような環境の詳細ページに移動するには、**完全な詳細**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17e3d-848">Click **Full details** to take you to the environment details page, as shown below.</span></span>

![Details_Preparing](./media/Details_Preparing.png)

5. <span data-ttu-id="17e3d-850">ローカル エージェントは配置要求を受け取り、配置を開始し、環境の準備ができたら LCS に再度通知します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-850">The local agent will now pick up the deployment request, start the deployment, and communicate back to LCS when the environment is ready.</span></span> <span data-ttu-id="17e3d-851">表示されているとおりに、配置の開始がしたときに、ステータスは**配置**に変更します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-851">When deployment starts, the status will change to **Deploying**, as shown.</span></span>

![配置しています](./media/Deploying.png)

![Details_Deploying](./media/Details_Deploying.png)

<span data-ttu-id="17e3d-854">展開に失敗した場合、LCS のお客様の環境では、**再設定**ボタンは次のように利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-854">If the deployment fails, the **Reconfigure** button will become available for your environment in LCS, as shown below.</span></span> <span data-ttu-id="17e3d-855">基になる問題を修正し、**再コンフィギュレーション**をクリックして、任意のコンフィギュレーションの変更を更新し、**配置**をクリックして配置を再試行します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-855">Fix the underlying issue, click **Reconfigure**, update any configuration changes, and click **Deploy** to retry the deployment.</span></span>

![失敗](./media/Failed.png)

<span data-ttu-id="17e3d-857">再構成する方法の詳細については、[環境の再構成](../lifecycle-services/reconfigure-environment.md) トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-857">See the [Reconfigure your environment](../lifecycle-services/reconfigure-environment.md) topic for details about how to reconfigure.</span></span> <span data-ttu-id="17e3d-858">次の図は、正常な配置を示します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-858">The following graphic shows a successful deployment.</span></span>
<span data-ttu-id="17e3d-859">![配置済み](./media/Deployed.png)</span><span class="sxs-lookup"><span data-stu-id="17e3d-859">![Deployed](./media/Deployed.png)</span></span>

### <a name="connect"></a> <span data-ttu-id="17e3d-860">22. Finance + Operations 環境への接続</span><span class="sxs-lookup"><span data-stu-id="17e3d-860">22. Connect to your Finance + Operations environment</span></span>
<span data-ttu-id="17e3d-861">ブラウザーで、https://[yourD365FOdomain]/namespaces/AXSF に移動し、そこでは yourD365FOdomain がこのトピックの[ドメイン名と DNS ゾーンの計画](#plandomain) セクションで定義したドメイン名です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-861">In your browser, navigate to https://[yourD365FOdomain]/namespaces/AXSF, where yourD365FOdomain is the domain name that you defined in the [Plan your domain name and DNS zones](#plandomain) section of this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17e3d-862">追加リソース</span><span class="sxs-lookup"><span data-stu-id="17e3d-862">Additional resources</span></span>
- [<span data-ttu-id="17e3d-863">オンプレミス配置への更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="17e3d-863">Apply updates to an on-premises deployment</span></span>](apply-updates-on-premises.md)
- [<span data-ttu-id="17e3d-864">オンプレミス配置の再配置</span><span class="sxs-lookup"><span data-stu-id="17e3d-864">Redeploy an on-premises deployment</span></span>](redeploy-on-prem.md)
- [<span data-ttu-id="17e3d-865">ドキュメント管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="17e3d-865">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
- [<span data-ttu-id="17e3d-866">電子申告 (ER) コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="17e3d-866">Import Electronic reporting (ER) configurations</span></span>](../analytics/electronic-reporting-import-ger-configurations.md)
- [<span data-ttu-id="17e3d-867">オンプレミス配置でのドキュメントの生成、発行、印刷</span><span class="sxs-lookup"><span data-stu-id="17e3d-867">Document generation, publishing, and printing in on-premises deployments</span></span>](../analytics/printing-capabilities-on-premises.md)
- [<span data-ttu-id="17e3d-868">オンプレミス環境用リバース プロキシの構成</span><span class="sxs-lookup"><span data-stu-id="17e3d-868">Configure reverse proxies for on-premises environments</span></span>](onprem-reverseproxy.md)
- [<span data-ttu-id="17e3d-869">テクニカル サポートの設定</span><span class="sxs-lookup"><span data-stu-id="17e3d-869">Set up technical support</span></span>](../lifecycle-services/support-experience.md)
- [<span data-ttu-id="17e3d-870">クライアントのインターネット接続</span><span class="sxs-lookup"><span data-stu-id="17e3d-870">Client internet connectivity</span></span>](../user-interface/client-disconnected.md)

## <a name="known-issues"></a><span data-ttu-id="17e3d-871">既知の問題</span><span class="sxs-lookup"><span data-stu-id="17e3d-871">Known issues</span></span>

### <a name="error-key-does-not-exist-when-running-the-new-d365fogmsaaccounts-cmdlet"></a><span data-ttu-id="17e3d-872">New-D365FOGMSAAccounts cmdlet を実行した際のエラー、「キーが存在しません」</span><span class="sxs-lookup"><span data-stu-id="17e3d-872">Error "Key does not exist" when running the New-D365FOGMSAAccounts cmdlet</span></span>
<span data-ttu-id="17e3d-873">ドメインでグループ管理サービス アカウント パスワードを初めて作成し生成する場合は、最初に**キー配分サービス KDS ルート キー**を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-873">If this is your first time creating and generating group Managed Service Account passwords in your domain, you need to first create the **Key Distribution Services KDS Root Key**.</span></span> <span data-ttu-id="17e3d-874">詳細については、[キー配分サービス KDS ルート キーの作成](https://docs.microsoft.com/windows-server/security/group-managed-service-accounts/create-the-key-distribution-services-kds-root-key)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17e3d-874">For more information, see [Create the Key Distribution Services KDS Root Key](https://docs.microsoft.com/windows-server/security/group-managed-service-accounts/create-the-key-distribution-services-kds-root-key).</span></span>

### <a name="error-the-winrm-client-cannot-process-the-request-when-running-the-remoting-script-configure-prereqs-allvms-cmdlet"></a><span data-ttu-id="17e3d-875">リモート処理スクリプト Configure-Prereqs-AllVms cmdlet を実行した際のエラー、「WinRM クライアントは要求を処理できません」</span><span class="sxs-lookup"><span data-stu-id="17e3d-875">Error "The WinRM client cannot process the request" when running the remoting script Configure-Prereqs-AllVms cmdlet</span></span>
<span data-ttu-id="17e3d-876">Service Fabric Cluster のすべてのマシンでコンピューター ポリシー**新しい資格情報委任を許可**を有効にするには、エラー メッセージの指示に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-876">You need to follow the instructions in the error message to enable the computer policy **Allow delegation fresh credentials** in all machines of Service Fabric cluster.</span></span>

### <a name="error-not-process-argument-transformation-on-parameter-test-cannot-convert-value-systemstring-to-type-systemmanagementautomationswitchparameter-when-running-the-config-prereqs-allvms-cmdlet"></a><span data-ttu-id="17e3d-877">エラー、「'テスト'パラメータでの引数変換を処理できません」</span><span class="sxs-lookup"><span data-stu-id="17e3d-877">Error "Not process argument transformation on parameter 'Test'.</span></span> <span data-ttu-id="17e3d-878">Config-Prereqs-AllVms cmdlet 実行時、値 "System.String" を、タイプ "System.Management.Automation.SwitchParameter" に変換することはできません</span><span class="sxs-lookup"><span data-stu-id="17e3d-878">Cannot convert value "System.String" to type "System.Management.Automation.SwitchParameter" when running the Config-Prereqs-AllVms cmdlet</span></span>
<span data-ttu-id="17e3d-879">このエラーを回避するには、**インフラストラクチャ** フォルダーにある Config-Prereqs-AllVms.ps1 の 56 行目の「-Test:$Test」を削除します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-879">To work around this error, remove "-Test:$Test" in line 56 of Config-Prereqs-AllVms.ps1, which is found under the **Infrastructure** folder.</span></span>

### <a name="error-not-process-argument-transformation-on-parameter-test-cannot-convert-value-systemstring-to-type-systemmanagementautomationswitchparameter-when-running-the-complete-prereqs-allvms-cmdlet"></a><span data-ttu-id="17e3d-880">エラー、「'テスト'パラメータでの引数変換を処理できません」</span><span class="sxs-lookup"><span data-stu-id="17e3d-880">Error "Not process argument transformation on parameter 'Test'.</span></span> <span data-ttu-id="17e3d-881">Complete-Prereqs-AllVms cmdlet 実行時、値 "System.String" を、タイプ "System.Management.Automation.SwitchParameter" に変換することはできません</span><span class="sxs-lookup"><span data-stu-id="17e3d-881">Cannot convert value "System.String" to type "System.Management.Automation.SwitchParameter" when running the Complete-Prereqs-AllVms cmdlet</span></span>
<span data-ttu-id="17e3d-882">このエラーを回避するには、**インフラストラクチャ** フォルダーにある Complete-Prereqs-AllVms.ps1 の 56、61、66 行目の「-Test:$Test」を削除します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-882">To work around this error, remove "-Test:$Test" in line 56, 61 and 66 of Complete-Prereqs-AllVms.ps1 which is found under the **Infrastructure** folder.</span></span>

### <a name="error-install-windowsfeature-the-request-to-add-or-remove-features-on-the-specified-server-failed-when-running-configure-prereqs-on-mrtype-and-reportservertyoe-servers"></a><span data-ttu-id="17e3d-883">MRType および ReportServerTyoe サーバーで Configure-Prereqs を実行した際のエラー、「Install-WindowsFeature: 指定されたサーバーへの機能の追加または削除の要求に失敗しました」</span><span class="sxs-lookup"><span data-stu-id="17e3d-883">Error "Install-WindowsFeature: The request to add or remove features on the specified server failed" when running Configure-Prereqs on MRType and ReportServerTyoe servers</span></span>
<span data-ttu-id="17e3d-884">.NET Framework 3.5 には、MRType および ReportServerType サーバーが必要です。</span><span class="sxs-lookup"><span data-stu-id="17e3d-884">.NET Framework 3.5 is required in MRType and ReportServerType servers.</span></span> <span data-ttu-id="17e3d-885">ただし、既定では .NET Framework 3.5 ソース ファイルは Windows Server 2016 インストールに含まれていません。</span><span class="sxs-lookup"><span data-stu-id="17e3d-885">By default however, .NET Framework 3.5 source files aren't included in your Windows Server 2016 installation.</span></span> <span data-ttu-id="17e3d-886">このエラーを回避するには、サーバー マネージャーによって新機能を手動で追加するときに**ソース** オプションを使用してインストールし、ソース ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-886">To work around this error, install it and specify the source files using the **source** option when you manually add new features by server manager.</span></span>

### <a name="error-msis7628-scope-names-should-be-a-valid-scope-description-name-in-ad-fs-configuration-when-running-the-publish-adfsapplicationgroup-cmdlet"></a><span data-ttu-id="17e3d-887">Publish-ADFSApplicationGroup cmdlet を実行した際のエラー、「MSIS7628: スコープ名は AD FS コンフィギュレーションで有効なスコープ説明でなければなりません」</span><span class="sxs-lookup"><span data-stu-id="17e3d-887">Error "MSIS7628: Scope names should be a valid Scope description name in AD FS configuration" when running the Publish-ADFSApplicationGroup cmdlet</span></span>
<span data-ttu-id="17e3d-888">このエラーは D365FO-OP-ADFSApplicationGroup で必要とされる OpenID スコープ **allatclaims** が原因で表示されます。ただし、一部の Windows Server 2016 インストールでは表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="17e3d-888">This error occurs because of an OpenID scope **allatclaims** that is required by the D365FO-OP-ADFSApplicationGroup, but it might be missing in some Windows Server 2016 installation.</span></span> <span data-ttu-id="17e3d-889">このエラーを回避するには、AD FS Management\Service\Scope Descriptions を使用してスコープの説明 **allatclaims** を追加します。</span><span class="sxs-lookup"><span data-stu-id="17e3d-889">To work around this error, add the scope description **allatclaims** through AD FS Management\Service\Scope Descriptions.</span></span>

### <a name="error-admin0077-access-control-policy-does-not-exist-permit-everyone-when-running-the-publish-adfsapplicationgroup-cmdlet"></a><span data-ttu-id="17e3d-890">Publish-ADFSApplicationGroup cmdletを実行した際のエラー、「ADMIN0077: アクセス制御ポリシーが存在しません: すべてのユーザーを許可」</span><span class="sxs-lookup"><span data-stu-id="17e3d-890">Error "ADMIN0077: Access control policy does not exist: Permit everyone" when running the Publish-ADFSApplicationGroup cmdlet</span></span>
<span data-ttu-id="17e3d-891">英語以外のバージョンの Windows Server 2016 と共に AD FS をインストールすると、すべてのユーザーのアクセス許可のアクセス許可ポリシーがローカル言語で作成されます。</span><span class="sxs-lookup"><span data-stu-id="17e3d-891">When your AD FS is installed with a non-English version of Windows Server 2016, the permit everyone access control policy is created with your local language.</span></span> <span data-ttu-id="17e3d-892">AccessControlPolicyName パラメーターを指定することによりコマンドレットを呼び出します: .\Publish-ADFSApplicationGroup.ps1 - HostUrl 'https://ax.d365ffo.onprem.contoso.com' - AccessControlPolicyName '<Permit everyone access control policy in your language>'。</span><span class="sxs-lookup"><span data-stu-id="17e3d-892">Invoke the cmdlet by specifying AccessControlPolicyName parameter as: .\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com' -AccessControlPolicyName '<Permit everyone access control policy in your language>'.</span></span> 
