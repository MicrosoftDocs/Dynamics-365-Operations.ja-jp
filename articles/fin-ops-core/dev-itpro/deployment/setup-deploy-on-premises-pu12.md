---
title: オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 から 40)
description: このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) プラットフォーム更新プログラム 12 から 40 を計画、設定、展開する方法について説明します。
author: PeterRFriis
ms.date: 06/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2017-11-30
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 6d99a0b22a13530546e3a87cfaed0f183eb2a8cb
ms.sourcegitcommit: d49b27df81bd30537b504a8679462b71210f4462
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2021
ms.locfileid: "6277403"
---
# <a name="set-up-and-deploy-on-premises-environments-platform-updates-12-through-40"></a><span data-ttu-id="9a0cf-103">オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 から 40)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-103">Set up and deploy on-premises environments (Platform updates 12 through 40)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a0cf-104">このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) プラットフォーム更新プログラム 12 から 40 を計画、設定、展開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-104">This topic provides information about how to plan, set up, and deploy Dynamics 365 Finance + Operations (on-premises) with Platform update 12-40.</span></span>

<span data-ttu-id="9a0cf-105">[ローカル ビジネス データ Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13595809&view=all) が利用可能です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-105">The [Local Business Data Yammer group](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13595809&view=all) is available.</span></span> <span data-ttu-id="9a0cf-106">オンプレミス展開に関する質問またはフィードバックをそこに投稿することができます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-106">You can post questions or feedback you may have about the on-premises deployment there.</span></span>

<span data-ttu-id="9a0cf-107">このトピックの内容に関する質問やフィードバックがある場合は、このページ下の **コメント** セクションに転記してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-107">If you have questions or feedback about the content in this topic, please post them in the **Comments** section at the bottom of this page.</span></span>

## <a name="finance--operations-components"></a><span data-ttu-id="9a0cf-108">Finance + Operations のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-108">Finance + Operations components</span></span>

<span data-ttu-id="9a0cf-109">Finance + Operations アプリケーションは、次の 3 つの主要なコンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-109">The Finance + Operations application consists of three main components:</span></span>

- <span data-ttu-id="9a0cf-110">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-110">Application Object Server (AOS)</span></span>
- <span data-ttu-id="9a0cf-111">ビジネス インテリジェンス (BI)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-111">Business Intelligence (BI)</span></span>
- <span data-ttu-id="9a0cf-112">財務レポート/管理レポーター</span><span class="sxs-lookup"><span data-stu-id="9a0cf-112">Financial Reporting/Management Reporter</span></span>

<span data-ttu-id="9a0cf-113">これらのコンポーネントは、次のシステム ソフトウェアによって異なります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-113">These components depend on the following system software:</span></span>

- <span data-ttu-id="9a0cf-114">Microsoft Windows Server 2016 (英語 OS のインストールのみがサポートされます)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-114">Microsoft Windows Server 2016 (only English OS installations are supported)</span></span>
- <span data-ttu-id="9a0cf-115">Microsoft SQL Server 2016 SP1 および SP2 (プラットフォーム更新プログラム 33 から) には次の機能があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-115">Microsoft SQL Server 2016 SP1 and SP2 (from Platform update 33), which has the following features:</span></span>
  - <span data-ttu-id="9a0cf-116">フルテキスト インデックス検索が有効にされている。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-116">Full-text index search is enabled.</span></span>
  - <span data-ttu-id="9a0cf-117">SQL Server Reporting Services (SSRS) - これは BI 仮想マシンに配置されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-117">SQL Server Reporting Services (SSRS) - This is deployed on BI virtual machines.</span></span>
  - <span data-ttu-id="9a0cf-118">SQL Server Integration Services (SSIS) - これは AOS 仮想マシンに配置されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-118">SQL Server Integration Services (SSIS) - This is deployed on AOS virtual machines.</span></span>

    > [!WARNING]
    > <span data-ttu-id="9a0cf-119">完全なテキスト検索を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-119">Full Text Search must be enabled.</span></span>

- <span data-ttu-id="9a0cf-120">SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="9a0cf-120">SQL Server Management Studio</span></span>
- <span data-ttu-id="9a0cf-121">スタンドアロン Microsoft Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9a0cf-121">Standalone Microsoft Azure Service Fabric</span></span>
- <span data-ttu-id="9a0cf-122">Microsoft Windows PowerShell 5.0 以降</span><span class="sxs-lookup"><span data-stu-id="9a0cf-122">Microsoft Windows PowerShell 5.0 or later</span></span>
- <span data-ttu-id="9a0cf-123">Windows Server 2016 での Active Directory Federation Services (AD FS)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-123">Active Directory Federation Services (AD FS) on Windows Server 2016</span></span>
- <span data-ttu-id="9a0cf-124">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="9a0cf-124">Domain controller</span></span>

  > [!WARNING]
  > <span data-ttu-id="9a0cf-125">ドメイン コントローラは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-125">The domain controller must be Microsoft Windows Server 2012 R2 or later and must have a domain functional level of 2012 R2 or more.</span></span>    <span data-ttu-id="9a0cf-126">ドメイン機能レベルの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-126">For more information about domain functional levels, see the following topics:</span></span>
  >   - <span data-ttu-id="9a0cf-127">[Active Directory 機能レベルとは](/previous-versions/windows/it-pro/windows-server-2003/cc787290(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="9a0cf-127">[What Are Active Directory Functional Levels](/previous-versions/windows/it-pro/windows-server-2003/cc787290(v=ws.10))</span></span>
  >   - <span data-ttu-id="9a0cf-128">[Active Directory ドメイン サービス機能のレベルを理解する](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="9a0cf-128">[Understanding Active Directory Domain Services Functional Levels](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))</span></span>
  >   - [<span data-ttu-id="9a0cf-129">双方向の完全な信頼</span><span class="sxs-lookup"><span data-stu-id="9a0cf-129">Full 2-way trust</span></span>](../../fin-ops/get-started/system-requirements-on-prem.md#full-2-way-trust)


## <a name="lifecycle-services"></a><span data-ttu-id="9a0cf-130">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="9a0cf-130">Lifecycle Services</span></span>

<span data-ttu-id="9a0cf-131">Finance + Operations のビットは、Microsoft Dynamics Lifecycle Services (LCS) を通じて配布されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-131">Finance + Operations bits are distributed through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9a0cf-132">配置する前に、[エンタープライズ契約](https://www.microsoft.com/Licensing/licensing-programs/enterprise.aspx) チャンネルを通じてライセンス キーを購入し、LCS でオンプレミス プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-132">Before you can deploy, you must purchase license keys through the [Enterprise Agreements](https://www.microsoft.com/Licensing/licensing-programs/enterprise.aspx) channel and set up an on-premises project in LCS.</span></span> <span data-ttu-id="9a0cf-133">LCS からのみ配置を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-133">Deployments can be initiated only through LCS.</span></span> <span data-ttu-id="9a0cf-134">LCS でオンプレミス プロジェクトを設定する方法の詳細については、[Lifecycle Services (LCS) でのオンプレミス プロジェクトの設定](../lifecycle-services/lbd-create-lcs-on-prem-project.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-134">For more information about how to set up on-premises projects in LCS, see [Set up on-premises projects in Lifecycle Services (LCS)](../lifecycle-services/lbd-create-lcs-on-prem-project.md).</span></span>

## <a name="authentication"></a><span data-ttu-id="9a0cf-135">認証</span><span class="sxs-lookup"><span data-stu-id="9a0cf-135">Authentication</span></span>

<span data-ttu-id="9a0cf-136">オンプレミス アプリケーションは AD FS で動作します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-136">The on-premises application works with AD FS.</span></span> <span data-ttu-id="9a0cf-137">LCS と対話するには、Azure Active Directory (AAD) も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-137">To interact with LCS, you must also configure Azure Active Directory (AAD).</span></span> <span data-ttu-id="9a0cf-138">配置を完了し、LCS ローカル エージェントを構成するには、AAD が必要です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-138">To complete the deployment and configure the LCS Local agent, you will need AAD.</span></span> <span data-ttu-id="9a0cf-139">AAD テナントがまだない場合は、AAD によって提供されるオプションのいずれかを使用して無料のものを取得できます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-139">If you do not already have an AAD tenant, you can get one for free by using one of the options provided by AAD.</span></span> <span data-ttu-id="9a0cf-140">詳細については、[Azure Active Directory テナントを取得する方法](/azure/active-directory/develop/active-directory-howto-tenant) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-140">For more information, see [How to get an Azure Active Directory tenant](/azure/active-directory/develop/active-directory-howto-tenant).</span></span>

## <a name="standalone-service-fabric"></a><span data-ttu-id="9a0cf-141">Standalone Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9a0cf-141">Standalone Service Fabric</span></span>

<span data-ttu-id="9a0cf-142">Finance + Operations は スタンドアロン Service Fabric を使用します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-142">Finance + Operations uses standalone Service Fabric.</span></span> <span data-ttu-id="9a0cf-143">詳細については、[Service Fabric ドキュメント](/azure/service-fabric/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-143">For more information, see the [Service Fabric documentation](/azure/service-fabric/).</span></span>

<span data-ttu-id="9a0cf-144">Finance + Operations の設定は、Service Fabric (SF) 内に一連のアプリケーションを配置します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-144">Setup of Finance + Operations will deploy a set of applications inside Service Fabric (SF).</span></span> <span data-ttu-id="9a0cf-145">展開中に、クラスター内の各ノードは、次のいずれかのノード タイプを持つように構成によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-145">During deployment, each node in the cluster will be defined via configuration to have one of the following node types:</span></span>

- <span data-ttu-id="9a0cf-146">**AOSNodeType** - アプリケーション オブジェクト サーバー (ビジネス ロジック) をホストします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-146">**AOSNodeType** - Hosts the application object server (business logic).</span></span>
- <span data-ttu-id="9a0cf-147">**OrchestratorType** - Service Fabric のプライマリ ノードとして機能し、配置およびサービスロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-147">**OrchestratorType** - Functions as Service Fabric primary nodes, and hosts deployment- and servicing logic.</span></span>
- <span data-ttu-id="9a0cf-148">**ReportServerType** - SSRS およびレポート ロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-148">**ReportServerType** - Hosts SSRS and reporting logic.</span></span>
- <span data-ttu-id="9a0cf-149">**MRType** - 管理レポート ロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-149">**MRType** - Hosts management reporting logic.</span></span>

## <a name="infrastructure"></a><span data-ttu-id="9a0cf-150">インフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-150">Infrastructure</span></span>

<span data-ttu-id="9a0cf-151">Finance + Operations には、非 Microsoft 仮想化プラットフォーム (特に VMWare) での操作に関する Microsoft の標準サポート ポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-151">Finance + Operations falls under the standard Microsoft support policy about operation on non-Microsoft virtualization platforms, specifically VMware.</span></span> <span data-ttu-id="9a0cf-152">詳細については、[Microsoft ソフトウェアのサポート ポリシー](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-152">For more information, see [Support policy for Microsoft software](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw).</span></span> <span data-ttu-id="9a0cf-153">要するに、私たちはこの環境で当社製品をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-153">In short, we support our products in this environment.</span></span> <span data-ttu-id="9a0cf-154">ただし、問題の調査を依頼された場合、仮想化プラットフォームのない状態または Microsoft 仮想化プラットフォームで問題を再現するようまず顧客に依頼する場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-154">However, if we are asked to investigate an issue, we might first ask the customer to reproduce the issue without the virtualization platform or on the Microsoft virtualization platform.</span></span>

<span data-ttu-id="9a0cf-155">VMWare を使用している場合は、次の Web ページに記載されている修正プログラムを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-155">If you are using VMWare, you must implement the fixes that are documented on the following web pages:</span></span>
- [<span data-ttu-id="9a0cf-156">仮想マシンをハードウェア バージョン 11 にアップグレード後、ネットワーク依存ワークロードのパフォーマンスが低下する (2129176)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-156">After upgrading a virtual machine to hardware version 11, network dependent workloads experience performance degradation (2129176)</span></span>](https://kb.vmware.com/s/article/2129176)
- [<span data-ttu-id="9a0cf-157">vmxnet3 仮想アダプターのいくつかの問題</span><span class="sxs-lookup"><span data-stu-id="9a0cf-157">Several issues with vmxnet3 virtual adapter</span></span>](https://vinfrastructure.it/2016/05/several-issues-vmxnet3-virtual-adapter)

> [!IMPORTANT]
> <span data-ttu-id="9a0cf-158">Dynamics 365 Finance + Operations (オンプレミス) は、Microsoft Azure クラウド サービス を含む、任意のパブリック クラウド インフラストラクチャではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-158">Dynamics 365 Finance + Operations (on-premises) is not supported on any public cloud infrastructure, including Microsoft Azure Cloud services.</span></span> <span data-ttu-id="9a0cf-159">ただし、[Microsoft Azure Stack Hub](https://azure.microsoft.com/products/azure-stack/hub/) での実行はサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-159">However, it is supported to run on [Microsoft Azure Stack Hub](https://azure.microsoft.com/products/azure-stack/hub/) services.</span></span>

<span data-ttu-id="9a0cf-160">ハードウェア構成には、次のコンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-160">The hardware configuration includes the following components:</span></span>

- <span data-ttu-id="9a0cf-161">Windows Server 2016 仮想マシン (VM) に基づく スタンドアロン Service Fabric Cluster</span><span class="sxs-lookup"><span data-stu-id="9a0cf-161">Standalone Service Fabric cluster that is based on Windows Server 2016 virtual machines (VMs)</span></span>
- <span data-ttu-id="9a0cf-162">Microsoft SQL Server (Clustered SQL と Always-On の両方がサポートされています)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-162">Microsoft SQL Server (both Clustered SQL and Always-On are supported)</span></span>
- <span data-ttu-id="9a0cf-163">認証のための AD FS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-163">AD FS for authentication</span></span>
- <span data-ttu-id="9a0cf-164">ストレージ用の Server Message Block (SMB) バージョン 3 のファイル共有</span><span class="sxs-lookup"><span data-stu-id="9a0cf-164">Server Message Block (SMB) version 3 file share for storage</span></span>
- <span data-ttu-id="9a0cf-165">オプション: Microsoft Office Server 2017</span><span class="sxs-lookup"><span data-stu-id="9a0cf-165">Optional: Microsoft Office Server 2017</span></span>

<span data-ttu-id="9a0cf-166">詳細については、[オンプレミス展開のシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-166">For more information, see [System requirements for on-premises deployments](../../fin-ops/get-started/system-requirements-on-prem.md).</span></span>

### <a name="hardware-layout"></a><span data-ttu-id="9a0cf-167">ハードウェア レイアウト</span><span class="sxs-lookup"><span data-stu-id="9a0cf-167">Hardware layout</span></span>

<span data-ttu-id="9a0cf-168">[オンプレミス環境のハードウェア サイジング要件](../../fin-ops/get-started/hardware-sizing-on-premises-environments.md) で推奨されるサイジングに基づいて、インフラストラクチャと Service Fabric Cluster を計画します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-168">Plan your infrastructure and Service Fabric cluster based on the recommended sizing in [Hardware sizing requirements for on-premises environments](../../fin-ops/get-started/hardware-sizing-on-premises-environments.md).</span></span> <span data-ttu-id="9a0cf-169">Service Fabric クラスターを計画する方法の詳細については、[Service Fabric のスタンドアロン クラスター展開の計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-169">For more information about how to plan the Service Fabric cluster, see [Plan and prepare your Service Fabric standalone cluster deployment](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

<span data-ttu-id="9a0cf-170">次のテーブルは、ハードウェア レイアウトの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-170">The following table shows an example of a hardware layout.</span></span> <span data-ttu-id="9a0cf-171">この例は、設定を説明するためにこのトピック全体で使用されています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-171">This example is used throughout this topic to illustrate the setup.</span></span> <span data-ttu-id="9a0cf-172">次の手順で指定されているマシン名と IP アドレスを、ご使用の環境のマシンの名前と IP アドレスに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-172">You will need to replace the machine names and IP addresses given in the following instructions with the names and IP addresses for the machines in your environment.</span></span>

> [!NOTE]
> <span data-ttu-id="9a0cf-173">Service Fabric クラスターのプライマリ ノードには、少なくとも 3 つのノードが必要です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-173">The Primary node of the Service Fabric cluster must have at least three nodes.</span></span> <span data-ttu-id="9a0cf-174">この例では **OrchestratorType** を主要なノード タイプとして指定します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-174">In this example, **OrchestratorType** is designated as the Primary node type.</span></span>

| <span data-ttu-id="9a0cf-175">マシンの目的</span><span class="sxs-lookup"><span data-stu-id="9a0cf-175">Machine purpose</span></span>          | <span data-ttu-id="9a0cf-176">SF ノード タイプ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-176">SF Node type</span></span>     | <span data-ttu-id="9a0cf-177">コンピューター名</span><span class="sxs-lookup"><span data-stu-id="9a0cf-177">Machine name</span></span>    | <span data-ttu-id="9a0cf-178">IP アドレス</span><span class="sxs-lookup"><span data-stu-id="9a0cf-178">IP address</span></span>    |
|--------------------------|------------------|-----------------|---------------|
| <span data-ttu-id="9a0cf-179">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="9a0cf-179">Domain controller</span></span>        |                  | <span data-ttu-id="9a0cf-180">DAX7SQLAODC1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-180">DAX7SQLAODC1</span></span>    | <span data-ttu-id="9a0cf-181">10.179.108.2</span><span class="sxs-lookup"><span data-stu-id="9a0cf-181">10.179.108.2</span></span>  |
| <span data-ttu-id="9a0cf-182">AD FS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-182">AD FS</span></span>                    |                  | <span data-ttu-id="9a0cf-183">DAX7SQLAOADFS1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-183">DAX7SQLAOADFS1</span></span>  | <span data-ttu-id="9a0cf-184">10.179.108.3</span><span class="sxs-lookup"><span data-stu-id="9a0cf-184">10.179.108.3</span></span>  |
| <span data-ttu-id="9a0cf-185">ファイル サーバー</span><span class="sxs-lookup"><span data-stu-id="9a0cf-185">File server</span></span>              |                  | <span data-ttu-id="9a0cf-186">DAX7SQLAOFILE1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-186">DAX7SQLAOFILE1</span></span>  | <span data-ttu-id="9a0cf-187">10.179.108.4</span><span class="sxs-lookup"><span data-stu-id="9a0cf-187">10.179.108.4</span></span>  |
| <span data-ttu-id="9a0cf-188">SQL Always-On クラスター</span><span class="sxs-lookup"><span data-stu-id="9a0cf-188">SQL Always-On cluster</span></span>    |                  | <span data-ttu-id="9a0cf-189">DAX7SQLAOSQLA01</span><span class="sxs-lookup"><span data-stu-id="9a0cf-189">DAX7SQLAOSQLA01</span></span> | <span data-ttu-id="9a0cf-190">10.179.108.5</span><span class="sxs-lookup"><span data-stu-id="9a0cf-190">10.179.108.5</span></span>  |
|                          |                  | <span data-ttu-id="9a0cf-191">DAX7SQLAOSQLA02</span><span class="sxs-lookup"><span data-stu-id="9a0cf-191">DAX7SQLAOSQLA02</span></span> | <span data-ttu-id="9a0cf-192">10.179.108.6</span><span class="sxs-lookup"><span data-stu-id="9a0cf-192">10.179.108.6</span></span>  |
|                          |                  | <span data-ttu-id="9a0cf-193">DAX7SQLAOSQLA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-193">DAX7SQLAOSQLA</span></span>   | <span data-ttu-id="9a0cf-194">10.179.108.9</span><span class="sxs-lookup"><span data-stu-id="9a0cf-194">10.179.108.9</span></span>  |
| <span data-ttu-id="9a0cf-195">クライアント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-195">Client</span></span>                   |                  | <span data-ttu-id="9a0cf-196">SQLAOCLIENT1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-196">SQLAOCLIENT1</span></span>    | <span data-ttu-id="9a0cf-197">10.179.108.11</span><span class="sxs-lookup"><span data-stu-id="9a0cf-197">10.179.108.11</span></span> |
| <span data-ttu-id="9a0cf-198">AOS 1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-198">AOS 1</span></span>                    | <span data-ttu-id="9a0cf-199">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="9a0cf-199">AOSNodeType</span></span>      | <span data-ttu-id="9a0cf-200">SQLAOSF1AOS1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-200">SQLAOSF1AOS1</span></span>    | <span data-ttu-id="9a0cf-201">10.179.108.12</span><span class="sxs-lookup"><span data-stu-id="9a0cf-201">10.179.108.12</span></span> |
| <span data-ttu-id="9a0cf-202">AOS 2</span><span class="sxs-lookup"><span data-stu-id="9a0cf-202">AOS 2</span></span>                    | <span data-ttu-id="9a0cf-203">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="9a0cf-203">AOSNodeType</span></span>      | <span data-ttu-id="9a0cf-204">SQLAOSF1AOS2</span><span class="sxs-lookup"><span data-stu-id="9a0cf-204">SQLAOSF1AOS2</span></span>    | <span data-ttu-id="9a0cf-205">10.179.108.13</span><span class="sxs-lookup"><span data-stu-id="9a0cf-205">10.179.108.13</span></span> |
| <span data-ttu-id="9a0cf-206">AOS 3</span><span class="sxs-lookup"><span data-stu-id="9a0cf-206">AOS 3</span></span>                    | <span data-ttu-id="9a0cf-207">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="9a0cf-207">AOSNodeType</span></span>      | <span data-ttu-id="9a0cf-208">SQLAOSF1AOS3</span><span class="sxs-lookup"><span data-stu-id="9a0cf-208">SQLAOSF1AOS3</span></span>    | <span data-ttu-id="9a0cf-209">10.179.108.14</span><span class="sxs-lookup"><span data-stu-id="9a0cf-209">10.179.108.14</span></span> |
| <span data-ttu-id="9a0cf-210">オーケストレータ 1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-210">Orchestrator 1</span></span>           | <span data-ttu-id="9a0cf-211">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="9a0cf-211">OrchestratorType</span></span> | <span data-ttu-id="9a0cf-212">SQLAOSF1ORCH1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-212">SQLAOSF1ORCH1</span></span>   | <span data-ttu-id="9a0cf-213">10.179.108.15</span><span class="sxs-lookup"><span data-stu-id="9a0cf-213">10.179.108.15</span></span> |
| <span data-ttu-id="9a0cf-214">オーケストレータ 2</span><span class="sxs-lookup"><span data-stu-id="9a0cf-214">Orchestrator 2</span></span>           | <span data-ttu-id="9a0cf-215">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="9a0cf-215">OrchestratorType</span></span> | <span data-ttu-id="9a0cf-216">SQLAOSF1ORCH2</span><span class="sxs-lookup"><span data-stu-id="9a0cf-216">SQLAOSF1ORCH2</span></span>   | <span data-ttu-id="9a0cf-217">10.179.108.16</span><span class="sxs-lookup"><span data-stu-id="9a0cf-217">10.179.108.16</span></span> |
| <span data-ttu-id="9a0cf-218">オーケストレータ 3</span><span class="sxs-lookup"><span data-stu-id="9a0cf-218">Orchestrator 3</span></span>           | <span data-ttu-id="9a0cf-219">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="9a0cf-219">OrchestratorType</span></span> | <span data-ttu-id="9a0cf-220">SQLAOSF1ORCH3</span><span class="sxs-lookup"><span data-stu-id="9a0cf-220">SQLAOSF1ORCH3</span></span>   | <span data-ttu-id="9a0cf-221">10.179.108.17</span><span class="sxs-lookup"><span data-stu-id="9a0cf-221">10.179.108.17</span></span> |
| <span data-ttu-id="9a0cf-222">Management Reporter ノード</span><span class="sxs-lookup"><span data-stu-id="9a0cf-222">Management Reporter node</span></span> | <span data-ttu-id="9a0cf-223">MRType</span><span class="sxs-lookup"><span data-stu-id="9a0cf-223">MRType</span></span>           | <span data-ttu-id="9a0cf-224">SQLAOSMR1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-224">SQLAOSMR1</span></span>       | <span data-ttu-id="9a0cf-225">10.179.108.18</span><span class="sxs-lookup"><span data-stu-id="9a0cf-225">10.179.108.18</span></span> |
| <span data-ttu-id="9a0cf-226">SSRS ノード</span><span class="sxs-lookup"><span data-stu-id="9a0cf-226">SSRS node</span></span>                | <span data-ttu-id="9a0cf-227">ReportServerType</span><span class="sxs-lookup"><span data-stu-id="9a0cf-227">ReportServerType</span></span> | <span data-ttu-id="9a0cf-228">SQLAOSFBIN1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-228">SQLAOSFBIN1</span></span>     | <span data-ttu-id="9a0cf-229">10.179.108.10</span><span class="sxs-lookup"><span data-stu-id="9a0cf-229">10.179.108.10</span></span> |

## <a name="setup"></a><span data-ttu-id="9a0cf-230">段取り</span><span class="sxs-lookup"><span data-stu-id="9a0cf-230">Setup</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9a0cf-231">前提条件</span><span class="sxs-lookup"><span data-stu-id="9a0cf-231">Prerequisites</span></span>

<span data-ttu-id="9a0cf-232">セットアップを開始する前に、次の前提条件が満たされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-232">Before you start the setup, the following prerequisites must be in place.</span></span> <span data-ttu-id="9a0cf-233">これらの前提条件の設定は、このドキュメントの範囲外です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-233">The setup of these prerequisites is out of scope for this document.</span></span>

- <span data-ttu-id="9a0cf-234">Active Directory Domain Services (AD DS) は、ネットワークにインストールして構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-234">Active Directory Domain Services (AD DS) must be installed and configured in your network.</span></span>
- <span data-ttu-id="9a0cf-235">AD FS は、展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-235">AD FS must be deployed.</span></span>
- <span data-ttu-id="9a0cf-236">SQL Server 2016 SP2 は SSRS コンピューターにインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-236">SQL Server 2016 SP2 must be installed on the SSRS machines.</span></span>
- <span data-ttu-id="9a0cf-237">SQL Server Reporting Services 2016 は、SSRS コンピューターに **ネイティブ** モードでインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-237">SQL Server Reporting Services 2016 must be installed in **Native** mode on the SSRS machines.</span></span>

<span data-ttu-id="9a0cf-238">次の必須ソフトウェアは、LCS からダウンロードされたインフラストラクチャ セットアップ スクリプトによって VM にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-238">The following prerequisite software is installed on the VMs by the infrastructure setup scripts downloaded from LCS.</span></span>

| <span data-ttu-id="9a0cf-239">ノード タイプ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-239">Node type</span></span> | <span data-ttu-id="9a0cf-240">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-240">Component</span></span> | <span data-ttu-id="9a0cf-241">細目</span><span class="sxs-lookup"><span data-stu-id="9a0cf-241">Details</span></span> |
|-----------|-----------|---------|
| <span data-ttu-id="9a0cf-242">AOS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-242">AOS</span></span>       | <span data-ttu-id="9a0cf-243">SNAC – ODBC ドライバー 13</span><span class="sxs-lookup"><span data-stu-id="9a0cf-243">SNAC – ODBC driver 13</span></span> | [<span data-ttu-id="9a0cf-244">ODBC ドライバー 13.1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-244">ODBC driver 13.1</span></span>](/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows#131) |
| <span data-ttu-id="9a0cf-245">AOS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-245">AOS</span></span>       | <span data-ttu-id="9a0cf-246">SNAC – ODBC ドライバー 17</span><span class="sxs-lookup"><span data-stu-id="9a0cf-246">SNAC – ODBC driver 17</span></span> | <span data-ttu-id="9a0cf-247">このドライバーは、PU15 以上へのアップグレードに必要です。<https://aka.ms/downloadmsodbcsql></span><span class="sxs-lookup"><span data-stu-id="9a0cf-247">This driver is needed for upgrading to PU15 or higher: <https://aka.ms/downloadmsodbcsql></span></span> |
| <span data-ttu-id="9a0cf-248">AOS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-248">AOS</span></span>       | <span data-ttu-id="9a0cf-249">Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-249">The Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="9a0cf-250">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-250">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="9a0cf-251">AOS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-251">AOS</span></span>       | <span data-ttu-id="9a0cf-252">Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-252">The Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="9a0cf-253">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="9a0cf-253">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="9a0cf-254">AOS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-254">AOS</span></span>       | <span data-ttu-id="9a0cf-255">Microsoft .NET Framework version 4.7.2 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-255">The Microsoft .NET Framework version 4.7.2 (CLR 4.0)</span></span> | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| <span data-ttu-id="9a0cf-256">AOS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-256">AOS</span></span>       | <span data-ttu-id="9a0cf-257">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-257">Internet Information Services (IIS)</span></span> | <span data-ttu-id="9a0cf-258">**Windows の機能:** WAS、WAS-Process-Model、WAS-NET-Environment、WAS-Config-APIs、Web-Server、Web-WebServer、Web-Security、Web-Filtering、Web-App-Dev、Web-Net-Ext、Web-Mgmt-Tools、Web-Mgmt-Console</span><span class="sxs-lookup"><span data-stu-id="9a0cf-258">**Windows features:** WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs, Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console</span></span> |
| <span data-ttu-id="9a0cf-259">AOS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-259">AOS</span></span>       | <span data-ttu-id="9a0cf-260">SQL Server Management Studio 17.2</span><span class="sxs-lookup"><span data-stu-id="9a0cf-260">SQL Server Management Studio 17.2</span></span> | <https://go.microsoft.com/fwlink/?linkid=854085> |
| <span data-ttu-id="9a0cf-261">AOS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-261">AOS</span></span>       | <span data-ttu-id="9a0cf-262">Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-262">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</span></span> | <https://support.microsoft.com/help/3179560> |
| <span data-ttu-id="9a0cf-263">AOS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-263">AOS</span></span>       | <span data-ttu-id="9a0cf-264">Microsoft Visual Studio 2017 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-264">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2017</span></span> | <span data-ttu-id="9a0cf-265"><https://lcs.dynamics.com/V2/SharedAssetLibrary>> モデル > "VC ++ 17 再頒布可能"</span><span class="sxs-lookup"><span data-stu-id="9a0cf-265"><https://lcs.dynamics.com/V2/SharedAssetLibrary> > Models > "VC++ 17 Redistributables"</span></span> |
| <span data-ttu-id="9a0cf-266">AOS</span><span class="sxs-lookup"><span data-stu-id="9a0cf-266">AOS</span></span>       | <span data-ttu-id="9a0cf-267">Microsoft Access データベース エンジン 2010 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-267">Microsoft Access Database Engine 2010 Redistributable</span></span> | <https://www.microsoft.com/download/details.aspx?id=13255> |
| <span data-ttu-id="9a0cf-268">BI</span><span class="sxs-lookup"><span data-stu-id="9a0cf-268">BI</span></span>        | <span data-ttu-id="9a0cf-269">.NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-269">.NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="9a0cf-270">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-270">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="9a0cf-271">BI</span><span class="sxs-lookup"><span data-stu-id="9a0cf-271">BI</span></span>        | <span data-ttu-id="9a0cf-272">.NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-272">.NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="9a0cf-273">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="9a0cf-273">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="9a0cf-274">BI</span><span class="sxs-lookup"><span data-stu-id="9a0cf-274">BI</span></span>        | <span data-ttu-id="9a0cf-275">Microsoft .NET Framework version 4.7.2 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-275">The Microsoft .NET Framework version 4.7.2 (CLR 4.0)</span></span> | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| <span data-ttu-id="9a0cf-276">BI</span><span class="sxs-lookup"><span data-stu-id="9a0cf-276">BI</span></span>        | <span data-ttu-id="9a0cf-277">SQL Server Management Studio 17.2</span><span class="sxs-lookup"><span data-stu-id="9a0cf-277">SQL Server Management Studio 17.2</span></span> | <https://go.microsoft.com/fwlink/?linkid=854085> |
| <span data-ttu-id="9a0cf-278">MR</span><span class="sxs-lookup"><span data-stu-id="9a0cf-278">MR</span></span>        | <span data-ttu-id="9a0cf-279">.NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-279">.NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="9a0cf-280">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-280">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="9a0cf-281">MR</span><span class="sxs-lookup"><span data-stu-id="9a0cf-281">MR</span></span>        | <span data-ttu-id="9a0cf-282">.NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-282">.NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="9a0cf-283">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="9a0cf-283">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="9a0cf-284">MR</span><span class="sxs-lookup"><span data-stu-id="9a0cf-284">MR</span></span>        | <span data-ttu-id="9a0cf-285">Microsoft .NET Framework version 4.7.2 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-285">The Microsoft .NET Framework version 4.7.2 (CLR 4.0)</span></span> | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| <span data-ttu-id="9a0cf-286">MR</span><span class="sxs-lookup"><span data-stu-id="9a0cf-286">MR</span></span>        | <span data-ttu-id="9a0cf-287">Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-287">Visual C++ Redistributable Packages for Visual Studio 2013</span></span> | <https://support.microsoft.com/help/3179560> |
| <span data-ttu-id="9a0cf-288">ORCH</span><span class="sxs-lookup"><span data-stu-id="9a0cf-288">ORCH</span></span>      | <span data-ttu-id="9a0cf-289">Microsoft .NET Framework version 4.0–4.8 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-289">The Microsoft .NET Framework version 4.0–4.8 (CLR 4.0)</span></span> | <https://dotnet.microsoft.com/download/thank-you/net48-offline> |

### <a name="overview"></a><span data-ttu-id="9a0cf-290">概要</span><span class="sxs-lookup"><span data-stu-id="9a0cf-290">Overview</span></span>

<span data-ttu-id="9a0cf-291">Finance + Operations のインフラストラクチャを設定するには、以下の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-291">The following steps must be completed to set up the infrastructure for Finance + Operations.</span></span> <span data-ttu-id="9a0cf-292">開始する前にすべての手順を読むと、セットアップを計画しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-292">Reading all the steps before you begin will make it easier to plan your setup.</span></span>

1. [<span data-ttu-id="9a0cf-293">ドメイン名と DNS ゾーンの計画</span><span class="sxs-lookup"><span data-stu-id="9a0cf-293">Plan your domain name and DNS zones</span></span>](#plandomain)
2. [<span data-ttu-id="9a0cf-294">証明書の計画と取得</span><span class="sxs-lookup"><span data-stu-id="9a0cf-294">Plan and acquire your certificates</span></span>](#plancert)
3. [<span data-ttu-id="9a0cf-295">ユーザーとサービス アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="9a0cf-295">Plan your users and service accounts</span></span>](#plansvcacct)
4. [<span data-ttu-id="9a0cf-296">DNS ゾーンの作成と A レコードの追加</span><span class="sxs-lookup"><span data-stu-id="9a0cf-296">Create DNS zones, and add A records</span></span>](#createdns)
5. [<span data-ttu-id="9a0cf-297">VM のドメインへの参加</span><span class="sxs-lookup"><span data-stu-id="9a0cf-297">Join VMs to the domain</span></span>](#joindomain)
6. [<span data-ttu-id="9a0cf-298">LCS からセットアップ スクリプトのダウンロード</span><span class="sxs-lookup"><span data-stu-id="9a0cf-298">Download setup scripts from LCS</span></span>](#downloadscripts)
7. [<span data-ttu-id="9a0cf-299">コンフィギュレーションの記述</span><span class="sxs-lookup"><span data-stu-id="9a0cf-299">Describe your configuration</span></span>](#describeconfig)
8. [<span data-ttu-id="9a0cf-300">証明書の構成</span><span class="sxs-lookup"><span data-stu-id="9a0cf-300">Configure certificates</span></span>](#configurecert)
9. [<span data-ttu-id="9a0cf-301">VM を設定する</span><span class="sxs-lookup"><span data-stu-id="9a0cf-301">Setup VMs</span></span>](#setupvms)
10. [<span data-ttu-id="9a0cf-302">スタンドアロン Service Fabric クラスターの設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-302">Set up a standalone Service Fabric cluster</span></span>](#setupsfcluster)
11. [<span data-ttu-id="9a0cf-303">テナント用 LCS 接続の構成</span><span class="sxs-lookup"><span data-stu-id="9a0cf-303">Configure LCS connectivity for the tenant</span></span>](#configurelcs)
12. [<span data-ttu-id="9a0cf-304">ファイル ストレージの設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-304">Set up file storage</span></span>](#setupfile)
13. [<span data-ttu-id="9a0cf-305">SQL Server の設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-305">Set up SQL Server</span></span>](#setupsql)
14. [<span data-ttu-id="9a0cf-306">データベースを構成する</span><span class="sxs-lookup"><span data-stu-id="9a0cf-306">Configure the databases</span></span>](#configuredb)
15. [<span data-ttu-id="9a0cf-307">資格情報の暗号化</span><span class="sxs-lookup"><span data-stu-id="9a0cf-307">Encrypt credentials</span></span>](#encryptcred)
16. [<span data-ttu-id="9a0cf-308">資産除去債務 (SSIS) の設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-308">Set up SSIS</span></span>](#setupssis)
17. [<span data-ttu-id="9a0cf-309">資産除去債務 (SSRS) の設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-309">Set up SSRS</span></span>](#setupssrs)
18. [<span data-ttu-id="9a0cf-310">AD FS のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9a0cf-310">Configure AD FS</span></span>](#configureadfs)
19. [<span data-ttu-id="9a0cf-311">コネクタを構成し、オンプレミスのローカル エージェントをインストールする</span><span class="sxs-lookup"><span data-stu-id="9a0cf-311">Configure a connector and install an on-premises local agent</span></span>](#configureconnector)
20. [<span data-ttu-id="9a0cf-312">リモート処理が使用されたら、CredSSP を終了処理する</span><span class="sxs-lookup"><span data-stu-id="9a0cf-312">Tear down CredSSP, if remoting was used</span></span>](#teardowncredssp)
21. [<span data-ttu-id="9a0cf-313">LCS から Finance + Operations 環境を配置する</span><span class="sxs-lookup"><span data-stu-id="9a0cf-313">Deploy your Finance + Operations environment from LCS</span></span>](#deploy)
22. [<span data-ttu-id="9a0cf-314">Finance + Operations 環境への接続</span><span class="sxs-lookup"><span data-stu-id="9a0cf-314">Connect to your Finance + Operations environment</span></span>](#connect)

### <a name="1-plan-your-domain-name-and-dns-zones"></a><a name="plandomain"></a> <span data-ttu-id="9a0cf-315">1. ドメイン名と DNS ゾーンの計画</span><span class="sxs-lookup"><span data-stu-id="9a0cf-315">1. Plan your domain name and DNS zones</span></span>

<span data-ttu-id="9a0cf-316">AOS のプロダクション インストールには、公的に登録されたドメイン名を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-316">We recommend that you use a publicly registered domain name for your production installation of AOS.</span></span> <span data-ttu-id="9a0cf-317">このようにして、外部アクセスが必要な場合は、ネットワークの外部からインストールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-317">In that way, the installation can be accessed outside the network, if outside access is required.</span></span>

<span data-ttu-id="9a0cf-318">たとえば、会社のドメインが contoso.com の場合、Finance + Operations は d365ffo.onprem.contoso.com であり、ホスト名は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-318">For example, if your company's domain is contoso.com, your zone for Finance + Operations might be d365ffo.onprem.contoso.com, and the host names might be as follows:</span></span>

- <span data-ttu-id="9a0cf-319">AOS の機械の場合 ax.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-319">ax.d365ffo.onprem.contoso.com for AOS machines</span></span>
- <span data-ttu-id="9a0cf-320">Service Fabric クラスターの場合 sf.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-320">sf.d365ffo.onprem.contoso.com for the Service Fabric cluster</span></span>

### <a name="2-plan-and-acquire-your-certificates"></a><a name="plancert"></a> <span data-ttu-id="9a0cf-321">2. 証明書の計画と取得</span><span class="sxs-lookup"><span data-stu-id="9a0cf-321">2. Plan and acquire your certificates</span></span>

<span data-ttu-id="9a0cf-322">Service Fabric クラスターと展開されているすべてのアプリケーションを保護するには、Secure Sockets Layer (SSL) 証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-322">Secure Sockets Layer (SSL) certificates are required in order to secure a Service Fabric cluster and all the applications that are deployed.</span></span> <span data-ttu-id="9a0cf-323">プロダクションとサンドボックスのワークロードについては、[DigiCert](https://www.digicert.com/ssl-certificate/)、[Comodo](https://ssl.comodo.com/)、[Symantec](https://www.websecurity.symantec.com/ssl-certificate)、[GoDaddy](https://www.godaddy.com/web-security/ssl-certificate)、または [GlobalSign](https://www.globalsign.com/en/ssl/) などの認証局から証明書を取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-323">For your production and sandbox workloads, we recommend that you acquire certificates from a certificate authority (CA) such as [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate), or [GlobalSign](https://www.globalsign.com/en/ssl/).</span></span> <span data-ttu-id="9a0cf-324">ドメインが [Active Directory 証明書サービス](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772393(v=ws.10)) (AD CS) で設定されている場合は、AD CS を介して証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-324">If your domain is set up with [Active Directory Certificate Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772393(v=ws.10)) (AD CS), you can create the certificates through AD CS.</span></span> <span data-ttu-id="9a0cf-325">証明書ごとに、プライベート キーが作成されたキーの交換を含める必要があり、個人情報交換 (.pfx) ファイルにエクスポート可能な必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-325">Each certificate must contain a private key that was created for key exchange, and it must be exportable to a Personal Information Exchange (.pfx) file.</span></span>

<span data-ttu-id="9a0cf-326">自己署名証明書は、テスト目的でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-326">Self-signed certificates can be used only for testing purposes.</span></span> <span data-ttu-id="9a0cf-327">便宜上、LCS で提供されるセットアップ スクリプトには、自己署名証明書を生成およびエクスポートするスクリプトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-327">For convenience, the setup scripts provided in LCS include scripts that generate and export self-signed certificates.</span></span> <span data-ttu-id="9a0cf-328">自己署名スクリプトを使用している場合は、後の手順で作成スクリプトを実行するように指示されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-328">If you are using self-signed scripts, you will be instructed to run the creation scripts in later steps.</span></span> <span data-ttu-id="9a0cf-329">先に述べたように、これらの証明書はテスト目的でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-329">As we've mentioned, these certificates can be used for testing purposes only.</span></span>

<span data-ttu-id="9a0cf-330">証明書の推奨設定は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="9a0cf-330">Recommended settings for certificates are:</span></span>
- <span data-ttu-id="9a0cf-331">署名アルゴリズム: sha256RSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-331">Signature algorithm: sha256RSA</span></span>
- <span data-ttu-id="9a0cf-332">署名ハッシュ アルゴリズム: sha256</span><span class="sxs-lookup"><span data-stu-id="9a0cf-332">Signature hash algorithm: sha256</span></span>
- <span data-ttu-id="9a0cf-333">公開キー: RSA (2048 ビット)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-333">Public key: RSA (2048 bits)</span></span>
- <span data-ttu-id="9a0cf-334">Thumbprint アルゴリズム: sha1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-334">Thumbprint algorithm: sha1</span></span>

| <span data-ttu-id="9a0cf-335">目的</span><span class="sxs-lookup"><span data-stu-id="9a0cf-335">Purpose</span></span>                                      | <span data-ttu-id="9a0cf-336">説明</span><span class="sxs-lookup"><span data-stu-id="9a0cf-336">Explanation</span></span> | <span data-ttu-id="9a0cf-337">追加条件</span><span class="sxs-lookup"><span data-stu-id="9a0cf-337">Additional requirements</span></span> |
|----------------------------------------------|-------------|-------------------------|
| <span data-ttu-id="9a0cf-338">SQL Server SSL 証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-338">SQL Server SSL certificate</span></span>                   | <span data-ttu-id="9a0cf-339">この証明書は、ネットワーク上の SQL Server インスタンスとクライアント アプリケーションの間で転送されるデータを暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-339">This certificate is used to encrypt data that is transmitted across a network between an instance of SQL Server and a client application.</span></span> | <p><span data-ttu-id="9a0cf-340">証明書の場合、ドメイン名は SQL Server のインスタンスまたはリスナーの完全修飾ドメイン名 (FQDN) と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-340">The domain name of the certificate should match the fully qualified domain name (FQDN) of the SQL Server instance or listener.</span></span> <span data-ttu-id="9a0cf-341">たとえば、SQL のリスナーが DAX7SQLAOSQLA のコンピューターにホストされている場合、証明書の DNS 名は、DAX7SQLAOSQLA.contoso.com です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-341">For example, if the SQL listener is hosted on the machine DAX7SQLAOSQLA, the certificate's DNS name is DAX7SQLAOSQLA.contoso.com.</span></span></p> <p><span data-ttu-id="9a0cf-342">CN: DAX7SQLAOSQLA.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-342">CN: DAX7SQLAOSQLA.contoso.com</span></span> <br> <span data-ttu-id="9a0cf-343">DNS 名: DAX7SQLAOSQLA.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-343">DNS Name: DAX7SQLAOSQLA.contoso.com</span></span></p> |
| <span data-ttu-id="9a0cf-344">Service Fabric Server 証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-344">Service Fabric Server certificate</span></span>            | <p><span data-ttu-id="9a0cf-345">この証明書を使用して、Service Fabric ノード間のノードからノードの通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-345">This certificate is used to help secure the node-to-node communication between the Service Fabric nodes.</span></span></p> <p> <span data-ttu-id="9a0cf-346">この証明書は、クラスターに接続するクライアントに提示されるサーバー証明書としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-346">This certificate is also used as the Server certificate that is presented to the client that connects to the cluster.</span></span></p> | <p><span data-ttu-id="9a0cf-347">この証明書には、ドメインの SSL ワイルド カード証明書も使用できます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-347">For this certificate you can also use SSL wild card certificate of your domain.</span></span> <span data-ttu-id="9a0cf-348">たとえば、\*.contoso.com です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-348">For example, \*.contoso.com.</span></span> <span data-ttu-id="9a0cf-349">これについて下の表で詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-349">This is explained in more details below the table.</span></span> <span data-ttu-id="9a0cf-350">それ以外の場合は、次の値を使用します:</span><span class="sxs-lookup"><span data-stu-id="9a0cf-350">Otherwise, use the following values:</span></span></p> <p><span data-ttu-id="9a0cf-351">CN: sf.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-351">CN: sf.d365ffo.onprem.contoso.com</span></span> <br> <span data-ttu-id="9a0cf-352">DNS 名: sf.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-352">DNS Name: sf.d365ffo.onprem.contoso.com</span></span></p> |
| <span data-ttu-id="9a0cf-353">Service Fabric Client 証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-353">Service Fabric Client certificate</span></span>            | <span data-ttu-id="9a0cf-354">この証明書は、クライアントによって Service Fabric クラスターを表示および管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-354">This certificate is used by clients to view and manage the Service Fabric cluster.</span></span> | <span data-ttu-id="9a0cf-355">CN: client.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-355">CN: client.d365ffo.onprem.contoso.com</span></span> <br> <span data-ttu-id="9a0cf-356">DNS 名: client.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-356">DNS Name: client.d365ffo.onprem.contoso.com</span></span> |
| <span data-ttu-id="9a0cf-357">証明書の暗号化</span><span class="sxs-lookup"><span data-stu-id="9a0cf-357">Encipherment Certificate</span></span>                     | <span data-ttu-id="9a0cf-358">この証明書は、SQL Server パスワードとユーザー アカウントのパスワードなどの重要な情報を暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-358">This certificate is used to encrypt sensitive information such as the SQL Server password and user account passwords.</span></span> | <p> <span data-ttu-id="9a0cf-359">証明書は、プロバイダー **Microsoft Enhanced Cryptographic Provider v1.0** を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-359">The certificate must be created by using the provider **Microsoft Enhanced Cryptographic Provider v1.0**.</span></span> </p><p><span data-ttu-id="9a0cf-360">証明書キーの使用にはデータ暗号化 (10) が含まれている必要があり、サーバー認証またはクライアント認証は含めないでください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-360">The certificate key usage must include Data Encipherment (10) and should not include Server authentication or Client authentication.</span></span></p><p><span data-ttu-id="9a0cf-361">詳細については、[Service Fabric アプリケーションでの機密情報の管理](/azure/service-fabric/service-fabric-application-secret-management) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-361">For more information, see [Managing secrets in Service Fabric applications](/azure/service-fabric/service-fabric-application-secret-management).</span></span></p> <p> <span data-ttu-id="9a0cf-362">CN: axdataenciphermentcert</span><span class="sxs-lookup"><span data-stu-id="9a0cf-362">CN: axdataenciphermentcert</span></span> <br> <span data-ttu-id="9a0cf-363">DNS 名: axdataenciphermentcert</span><span class="sxs-lookup"><span data-stu-id="9a0cf-363">DNS Name: axdataenciphermentcert</span></span> </p> |
| <span data-ttu-id="9a0cf-364">AOS SSL 証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-364">AOS SSL Certificate</span></span>                          | <p><span data-ttu-id="9a0cf-365">この証明書は、AOS Web サイトに接続するクライアントに提示されるサーバー証明書としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-365">This certificate is used as the Server certificate that is presented to the client for the AOS website.</span></span> <span data-ttu-id="9a0cf-366">また、WCF (Windows Communication Foundation) / SOAP (Simple Object Access Protocol) 証明書を有効にするためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-366">It's also used to enable Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP) certificates.</span></span></p> | <p><span data-ttu-id="9a0cf-367">Service Fabric サーバー証明書として使用するのと同じワイルドカード証明書を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-367">You can use the same wild card certificate that you used as the Service Fabric Server certificate.</span></span> <span data-ttu-id="9a0cf-368">それ以外の場合は、次の値を使用します:</span><span class="sxs-lookup"><span data-stu-id="9a0cf-368">Otherwise, use the following values:</span></span></p> <p> <span data-ttu-id="9a0cf-369">CN: ax.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-369">CN: ax.d365ffo.onprem.contoso.com</span></span> <br> <span data-ttu-id="9a0cf-370">DNS 名: ax.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-370">DNS Name: ax.d365ffo.onprem.contoso.com</span></span> </p> |
| <span data-ttu-id="9a0cf-371">セッション認証証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-371">Session Authentication certificate</span></span>           | <span data-ttu-id="9a0cf-372">この証明書は、AOS がユーザーのセッション情報を保護するために使用します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-372">This certificate is used by AOS to help secure a user's session information.</span></span> | <p> <span data-ttu-id="9a0cf-373">この証明書は、LCS からの展開時に使用されるファイル共有証明書です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-373">This certificate is also the File Share certificate that will be used at the time of deployment from LCS.</span></span></p> <p> <span data-ttu-id="9a0cf-374">CN: SessionAuthentication</span><span class="sxs-lookup"><span data-stu-id="9a0cf-374">CN: SessionAuthentication</span></span> <br> <span data-ttu-id="9a0cf-375">DNS 名: SessionAuthentication</span><span class="sxs-lookup"><span data-stu-id="9a0cf-375">DNS Name: SessionAuthentication</span></span> </p> |
| <span data-ttu-id="9a0cf-376">データの暗号化証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-376">Data Encryption certificate</span></span>                  | <span data-ttu-id="9a0cf-377">これらの証明書は、機密情報を暗号化するために AOS によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-377">This certificate is used by the AOS to encrypt sensitive information.</span></span>  | <p><span data-ttu-id="9a0cf-378">これはプロバイダー **Microsoft Enhanced RSA および AES Cryptographic Provider** を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-378">This must be created using the provider **Microsoft Enhanced RSA and AES Cryptographic Provider**.</span></span> </p> <p> <span data-ttu-id="9a0cf-379">CN: DataEncryption</span><span class="sxs-lookup"><span data-stu-id="9a0cf-379">CN: DataEncryption</span></span> <br> <span data-ttu-id="9a0cf-380">DNS 名: DataEncryption</span><span class="sxs-lookup"><span data-stu-id="9a0cf-380">DNS Name: DataEncryption</span></span> </p> |
| <span data-ttu-id="9a0cf-381">データ署名の証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-381">Data Signing certificate</span></span>                     | <span data-ttu-id="9a0cf-382">これらの証明書は、機密情報を暗号化するために AOS によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-382">This certificate is used by the AOS to encrypt sensitive information.</span></span>  | <p> <span data-ttu-id="9a0cf-383">これは、データ暗号化証明書とは別のもので、プロバイダー **Microsoft の拡張された RSA および AES 暗号化プロバイダー** を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-383">This is separate from the Data Encryption certificate and must be created using the provider **Microsoft Enhanced RSA and AES Cryptographic Provider**.</span></span> </p> <p> <span data-ttu-id="9a0cf-384">CN: DataSigning</span><span class="sxs-lookup"><span data-stu-id="9a0cf-384">CN: DataSigning</span></span> <br> <span data-ttu-id="9a0cf-385">DNS 名: DataSigning</span><span class="sxs-lookup"><span data-stu-id="9a0cf-385">DNS Name: DataSigning</span></span> </p> |
| <span data-ttu-id="9a0cf-386">財務報告クライアント証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-386">Financial Reporting client certificate</span></span>       | <span data-ttu-id="9a0cf-387">この証明書は、財務報告サービスと AOS 間の通信を保護するのに役立ちます。   この証明書を使用して、財務報告サービスと AOS 間の通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-387">This certificate is used to help secure the communication between the Financial Reporting services and the AOS.</span></span> | <p><span data-ttu-id="9a0cf-388">CN: FinancialReporting</span><span class="sxs-lookup"><span data-stu-id="9a0cf-388">CN: FinancialReporting</span></span> <br> <span data-ttu-id="9a0cf-389">DNS 名: FinancialReporting</span><span class="sxs-lookup"><span data-stu-id="9a0cf-389">DNS Name: FinancialReporting</span></span> </p>  |
| <span data-ttu-id="9a0cf-390">報告証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-390">Reporting certificate</span></span>                        | <span data-ttu-id="9a0cf-391">この証明書を使用して、SSRS と AOS 間の通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-391">This certificate is used to help secure the communication between SSRS and the AOS.</span></span>| <p> <span data-ttu-id="9a0cf-392">**財務報告クライアント証明書を再利用しないでください。**</span><span class="sxs-lookup"><span data-stu-id="9a0cf-392">**Do not reuse the Financial Reporting Client certificate.**</span></span> </p> <p> <span data-ttu-id="9a0cf-393">CN: ReportingService</span><span class="sxs-lookup"><span data-stu-id="9a0cf-393">CN: ReportingService</span></span> <br> <span data-ttu-id="9a0cf-394">DNS 名: ReportingService</span><span class="sxs-lookup"><span data-stu-id="9a0cf-394">DNS Name: ReportingService</span></span> </p> |
| <span data-ttu-id="9a0cf-395">オンプレミス ローカル エージェント証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-395">On-Premises local agent certificate</span></span>           | <p><span data-ttu-id="9a0cf-396">この証明書は、オンプレミスと LCS でホストされているローカル エージェント間の通信を保護するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-396">This certificate is used to help secure the communication between a local agent that is hosted on-premises and on LCS.</span></span></p><p><span data-ttu-id="9a0cf-397">この証明書を使用すると、Azure AD テナントに代わってローカル エージェントが動作し、LCS と通信して配置を編成および監視することができます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-397">This certificate enables the local agent to act on behalf of your Azure AD tenant, and to communicate with LCS to orchestrate and monitor deployments.</span></span></p><p><span data-ttu-id="9a0cf-398">**注記:** テナントにはオンプレミス ローカル エージェント証明書が 1 つだけ必要です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-398">**Note:** Only 1 on-premises local agent certificate is needed for a tenant.</span></span></p> | <p> <span data-ttu-id="9a0cf-399">CN: OnPremLocalAgent</span><span class="sxs-lookup"><span data-stu-id="9a0cf-399">CN: OnPremLocalAgent</span></span> <br> <span data-ttu-id="9a0cf-400">DNS 名: OnPremLocalAgent</span><span class="sxs-lookup"><span data-stu-id="9a0cf-400">DNS Name: OnPremLocalAgent</span></span> </p> |

<span data-ttu-id="9a0cf-401">ドメインの SSL ワイルド カード証明書を使用して、Service Fabric サーバー証明書と AOS SSL 証明書を結合できます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-401">SSL wild card certificate of your domain can be used to combine Service Fabric Server certificate and AOS SSL certificate.</span></span>

<span data-ttu-id="9a0cf-402">以下は、AOS SSL 証明書と組み合わせた Service Fabric Server 証明書の例です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-402">The following is an example of a Service Fabric Server certificate combined with an AOS SSL certificate.</span></span>

#### <a name="subject-name"></a><span data-ttu-id="9a0cf-403">件名</span><span class="sxs-lookup"><span data-stu-id="9a0cf-403">Subject name</span></span>

```Text
CN = *.d365ffo.onprem.contoso.com
```

#### <a name="subject-alternative-names"></a><span data-ttu-id="9a0cf-404">件名の代替名</span><span class="sxs-lookup"><span data-stu-id="9a0cf-404">Subject alternative names</span></span>

```Text
DNS Name=ax.d365ffo.onprem.contoso.com
DNS Name=sf.d365ffo.onprem.contoso.com
DNS Name=*.d365ffo.onprem.contoso.com
```

> [!NOTE]
> <span data-ttu-id="9a0cf-405">ワイルド カード証明書は、発行先となるドメインの最初のレベル サブドメインのみをセキュリティ保護できるようにします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-405">The wild card certificate allows you to secure only the first-level subdomain of the domain to which it is issued.</span></span>

### <a name="3-plan-your-users-and-service-accounts"></a><a name="plansvcacct"></a> <span data-ttu-id="9a0cf-406">3. ユーザーとサービス アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="9a0cf-406">3. Plan your users and service accounts</span></span>

<span data-ttu-id="9a0cf-407">Finance + Operations を機能させるために、いくつかのユーザー アカウントまたはサービス アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-407">You must create several user or service accounts for Finance + Operations to work.</span></span> <span data-ttu-id="9a0cf-408">サービス アカウントの管理グループ (gMSAs)、ドメイン アカウント、および SQL アカウントの組み合わせを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-408">You must create a combination of group managed service accounts (gMSAs), domain accounts, and SQL accounts.</span></span> <span data-ttu-id="9a0cf-409">次の表は、このトピックで使用されるユーザー アカウント、その目的、および名前の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-409">The following table shows the user accounts, their purpose, and example names that will be used in this topic.</span></span>

| <span data-ttu-id="9a0cf-410">ユーザー アカウント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-410">User account</span></span>                                            | <span data-ttu-id="9a0cf-411">種類</span><span class="sxs-lookup"><span data-stu-id="9a0cf-411">Type</span></span>           | <span data-ttu-id="9a0cf-412">目的</span><span class="sxs-lookup"><span data-stu-id="9a0cf-412">Purpose</span></span> | <span data-ttu-id="9a0cf-413">ユーザー名</span><span class="sxs-lookup"><span data-stu-id="9a0cf-413">User name</span></span> |
|---------------------------------------------------------|----------------|---------|-----------|
| <span data-ttu-id="9a0cf-414">財務レポート アプリケーション サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-414">Financial Reporting Application Service Account</span></span>         | <span data-ttu-id="9a0cf-415">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-415">gMSA</span></span>           |         | <span data-ttu-id="9a0cf-416">Contoso\\svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-416">Contoso\\svc-FRAS$</span></span> |
| <span data-ttu-id="9a0cf-417">財務レポート プロセス サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-417">Financial Reporting Process Service Account</span></span>             | <span data-ttu-id="9a0cf-418">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-418">gMSA</span></span>           |         | <span data-ttu-id="9a0cf-419">Contoso\\svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-419">Contoso\\svc-FRPS$</span></span> |
| <span data-ttu-id="9a0cf-420">財務レポート クリック ワンス デザイナー サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-420">Financial Reporting Click Once Designer Service Account</span></span> | <span data-ttu-id="9a0cf-421">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-421">gMSA</span></span>           |         | <span data-ttu-id="9a0cf-422">Contoso\\svc-FRCO$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-422">Contoso\\svc-FRCO$</span></span> |
| <span data-ttu-id="9a0cf-423">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-423">AOS Service Account</span></span>                                     | <span data-ttu-id="9a0cf-424">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-424">gMSA</span></span>           | <span data-ttu-id="9a0cf-425">このユーザーは、将来校正するために作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-425">This user should be created for future proofing.</span></span> <span data-ttu-id="9a0cf-426">今後のリリースでは、AOS を gMSA と連携させる予定です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-426">We plan to enable AOS to work with the gMSA in upcoming releases.</span></span> <span data-ttu-id="9a0cf-427">このユーザーを設定時に作成することで、gMSA へのシームレスな移行を確実にすることができます。\*</span><span class="sxs-lookup"><span data-stu-id="9a0cf-427">By creating this user at the time of setup, you will help to ensure a seamless transition to the gMSA.\*</span></span> | <span data-ttu-id="9a0cf-428">Contoso\\svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-428">Contoso\\svc-AXSF$</span></span> |
| <span data-ttu-id="9a0cf-429">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-429">AOS Service Account</span></span>                                     | <span data-ttu-id="9a0cf-430">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-430">Domain account</span></span> | <span data-ttu-id="9a0cf-431">AOS は、一般提供 (GA) リリースでこのユーザーを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-431">AOS uses this user in the general availability (GA) release.</span></span> | <span data-ttu-id="9a0cf-432">Contoso\\ AXServiceUser</span><span class="sxs-lookup"><span data-stu-id="9a0cf-432">Contoso\\AXServiceUser</span></span> |
| <span data-ttu-id="9a0cf-433">AOS SQL DB 管理者ユーザー</span><span class="sxs-lookup"><span data-stu-id="9a0cf-433">AOS SQL DB Admin user</span></span>                                   | <span data-ttu-id="9a0cf-434">SQL ユーザー</span><span class="sxs-lookup"><span data-stu-id="9a0cf-434">SQL user</span></span>       | <span data-ttu-id="9a0cf-435">Finance + Operations は、このユーザーを使用して SQL\*\* を認証します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-435">Finance + Operations uses this user to authenticate with SQL\*\*.</span></span> <span data-ttu-id="9a0cf-436">このユーザーは、今後のリリース \*\*\* で gMSA ユーザーにも置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-436">This user will also be replaced by the gMSA user in upcoming releases\*\*\*.</span></span> | <span data-ttu-id="9a0cf-437">AXDBAdmin</span><span class="sxs-lookup"><span data-stu-id="9a0cf-437">AXDBAdmin</span></span> |
| <span data-ttu-id="9a0cf-438">ローカル配置エージェント サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-438">Local Deployment Agent Service Account</span></span>                  | <span data-ttu-id="9a0cf-439">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-439">gMSA</span></span>           | <span data-ttu-id="9a0cf-440">このアカウントは、ローカル エージェントによって、さまざまなノードでの展開を調整するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-440">This account is used by the local agent to orchestrate the deployment on various nodes.</span></span> | <span data-ttu-id="9a0cf-441">Contoso\\Svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-441">Contoso\\Svc-LocalAgent$</span></span> |

<span data-ttu-id="9a0cf-442">\* これらのアカウントでは、地域の設定を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-442">\* These accounts should not have their regional settings changed.</span></span> <span data-ttu-id="9a0cf-443">既定の EN-US リージョン設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-443">They should have the default EN-US region settings.</span></span> 

<span data-ttu-id="9a0cf-444">\*\* SQL ユーザーのパスワードに特殊文字が含まれている場合、展開中に問題が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-444">\*\* If the password of the SQL user contains special characters, you might encounter issues during deployment.</span></span>

<span data-ttu-id="9a0cf-445">\*\*\* SQL 認証で使用する SQL ユーザ名とパスワードは暗号化されてファイル共有に保存されているため、安全性が確保されています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-445">\*\*\* The SQL user name and password for SQL authentication are secured because they are encrypted and stored in the file share.</span></span>

### <a name="4-create-dns-zones-and-add-a-records"></a><a name="createdns"></a> <span data-ttu-id="9a0cf-446">4. DNS ゾーンの作成とレコードの追加</span><span class="sxs-lookup"><span data-stu-id="9a0cf-446">4. Create DNS zones and add A records</span></span>

<span data-ttu-id="9a0cf-447">DNS は AD DS と統合されており、ネットワーク内のリソースを整理、管理、検索することができます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-447">DNS is integrated with AD DS, and lets you organize, manage, and find resources in a network.</span></span> <span data-ttu-id="9a0cf-448">次の指示では、AOS ホスト名と Service Fabric クラスターの DNS 前方参照ゾーンと A レコードを作成する手順を示します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-448">The following instructions provide steps to create a DNS forward lookup zone and A records for the AOS host name and Service Fabric cluster.</span></span> <span data-ttu-id="9a0cf-449">この設定例では、DNS ゾーン名は d365ffo.onprem.contoso.com で、A レコード/ホスト名は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-449">In this example setup, the DNS zone name is d365ffo.onprem.contoso.com, and the A records/host names are as follows:</span></span>

- <span data-ttu-id="9a0cf-450">AOS の機械の場合 **ax**.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-450">**ax**.d365ffo.onprem.contoso.com for AOS machines</span></span>
- <span data-ttu-id="9a0cf-451">Service Fabric クラスターの場合 **sf**.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a0cf-451">**sf**.d365ffo.onprem.contoso.com for the Service Fabric cluster</span></span>

#### <a name="add-a-dns-zone"></a><span data-ttu-id="9a0cf-452">DNS ゾーンの追加</span><span class="sxs-lookup"><span data-stu-id="9a0cf-452">Add a DNS zone</span></span>

<span data-ttu-id="9a0cf-453">DNS ゾーンを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-453">Use the following procedure to add a DNS zone.</span></span>

1. <span data-ttu-id="9a0cf-454">ドメイン コントローラー コンピューターにログインして **スタート** を選択し、**dnsmgmt.msc** と入力して **dnsmgmt (DNS)** アプリケーションを選択することにより DNS マネージャーを起動します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-454">Sign in to the domain controller machine, select **Start**, and start DNS Manager by typing **dnsmgmt.msc** and selecting the **dnsmgmt (DNS)** application.</span></span>
2. <span data-ttu-id="9a0cf-455">コンソール ツリーでドメイン コントローラー名を右クリックし、**新しいゾーン** \> **次へ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-455">Right-click the domain controller name in the console tree, and then select **New Zone** \> **Next**.</span></span>
3. <span data-ttu-id="9a0cf-456">**プライマリ ゾーン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-456">Select **Primary Zone**.</span></span>
4. <span data-ttu-id="9a0cf-457">**Active Directory にゾーンを保存 (DNS サーバーが書き込み可能なドメイン コントローラーの場合にのみ使用可能)** のチェック ボックスが選択されたままの状態で、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-457">Leave the **Store the zone in Active Directory (available only if the DNS Server is a writeable domain controller** check box selected, and then select **Next**.</span></span>
5. <span data-ttu-id="9a0cf-458">**このドメインのドメイン コントローラーで実行されているすべての DNS サーバーに対して : Contoso.com** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-458">Select **To all DNS Servers running on Domain Controllers in this domain: Contoso.com**, and then select **Next**.</span></span>
6. <span data-ttu-id="9a0cf-459">**前方参照ゾーン** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-459">Select **Forward Lookup Zone**, and then select **Next**.</span></span>
7. <span data-ttu-id="9a0cf-460">設定するゾーン名を入力し、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-460">Enter the zone name for your setup, and then select **Next**.</span></span> <span data-ttu-id="9a0cf-461">たとえば、**d365ffo.onprem.contoso.com** と入力します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-461">For example, enter **d365ffo.onprem.contoso.com**.</span></span>
8. <span data-ttu-id="9a0cf-462">**動的更新を許可しない** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-462">Select **Do not allow dynamic updates**, and then select **Next**.</span></span>
9. <span data-ttu-id="9a0cf-463">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-463">Select **Finish**.</span></span>

#### <a name="set-up-an-a-record-for-aos"></a><span data-ttu-id="9a0cf-464">AOS の A レコードを設定する</span><span class="sxs-lookup"><span data-stu-id="9a0cf-464">Set up an A record for AOS</span></span>

<span data-ttu-id="9a0cf-465">新しい DNS ゾーンで、**AOSNodeType** タイプの Service Fabric クラスター ノード **ごと** に、**ax.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-465">In the new DNS zone, create one A record that is named **ax.d365ffo.onprem.contoso.com** for **each** Service Fabric cluster node of the **AOSNodeType** type.</span></span> <span data-ttu-id="9a0cf-466">他のノード タイプの A レコードは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-466">Don't create A records for the other node types.</span></span>

1. <span data-ttu-id="9a0cf-467">DNS マネージャーの **前方参照ゾーン** フォルダーで、新しく作成したゾーンを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-467">Find the newly created zone under the **Forward Lookup Zones** folder in DNS Manager.</span></span>
2. <span data-ttu-id="9a0cf-468">新しいゾーンを右クリックして、**新しいホスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-468">Right-click the new zone, and then select **New Host**.</span></span>
3. <span data-ttu-id="9a0cf-469">Service Fabric ノードの 名前および IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-469">Enter the name and IP address of the Service Fabric node.</span></span> <span data-ttu-id="9a0cf-470">(たとえば、**ax** を名前として入力し、**10.179.108.12** を IP アドレスとして入力します。) **ホストの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-470">(For example, enter **ax** as the name and enter **10.179.108.12** as the IP address.) Select **Add Host**.</span></span>
4. <span data-ttu-id="9a0cf-471">どのチェック ボックスもオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-471">Do not select either check box.</span></span>
5. <span data-ttu-id="9a0cf-472">各 AOS ノードで手順 1 ～ 4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-472">Repeat steps 1-4 for each AOS node.</span></span>

#### <a name="set-up-an-a-record-for-the-orchestrator"></a><span data-ttu-id="9a0cf-473">Orchestrator の A レコードを設定する</span><span class="sxs-lookup"><span data-stu-id="9a0cf-473">Set up an A record for the orchestrator</span></span>

<span data-ttu-id="9a0cf-474">新しい DNS ゾーンで、**OrchestratorType** タイプの Service Fabric クラスター ノード **ごと** に、**sf.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-474">In the new DNS zone, create an A record that is named **sf.d365ffo.onprem.contoso.com** for **each** Service Fabric cluster node of the **OrchestratorType** type.</span></span> <span data-ttu-id="9a0cf-475">他のノード タイプの A レコードは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-475">Don't create A records for the other node types.</span></span>

1. <span data-ttu-id="9a0cf-476">新しいゾーンを右クリックして、**新しいホスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-476">Right-click the new zone, and then select **New Host**.</span></span>
2. <span data-ttu-id="9a0cf-477">Service Fabric ノードの 名前および IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-477">Enter the name and IP address of the Service Fabric node.</span></span> <span data-ttu-id="9a0cf-478">(たとえば、**sf** を名前としてを入力し、**10.179.108.15** を IP アドレスとして入力します。) **ホストの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-478">(For example, enter **sf** as the name and enter **10.179.108.15** as the IP address.) Select **Add Host**.</span></span>
3. <span data-ttu-id="9a0cf-479">どのチェック ボックスもオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-479">Do not select either check box.</span></span>
4. <span data-ttu-id="9a0cf-480">各オーケストレータ ノードを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-480">Repeat for each Orchestrator node.</span></span>

### <a name="5-join-vms-to-the-domain"></a><a name="joindomain"></a> <span data-ttu-id="9a0cf-481">5. VM のドメインへの参加</span><span class="sxs-lookup"><span data-stu-id="9a0cf-481">5. Join VMs to the domain</span></span>

<span data-ttu-id="9a0cf-482">各 VM をドメインに参加させるには、[コンピューターをドメインに参加させる](/windows-server/identity/ad-fs/deployment/join-a-computer-to-a-domain)のドキュメントの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-482">Join each VM to the domain by completing the steps in the [Join a Computer to a Domain](/windows-server/identity/ad-fs/deployment/join-a-computer-to-a-domain) document.</span></span> <span data-ttu-id="9a0cf-483">または、次の Windows PowerShell スクリプトを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-483">Alternatively, use the following Windows PowerShell script.</span></span>

```powershell
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
```

> [!IMPORTANT]
> <span data-ttu-id="9a0cf-484">ドメインにそれらを結合させた後、VM を再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-484">You must restart the VMs after you join them to the domain.</span></span>

### <a name="6-download-setup-scripts-from-lcs"></a><a name="downloadscripts"></a> <span data-ttu-id="9a0cf-485">6. LCS からのセットアップ スクリプトのダウンロード</span><span class="sxs-lookup"><span data-stu-id="9a0cf-485">6. Download setup scripts from LCS</span></span>

<span data-ttu-id="9a0cf-486">セットアップ エクスペリエンスを向上させるためのスクリプトをいくつか紹介しています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-486">We have provided several scripts to help improve the setup experience.</span></span> <span data-ttu-id="9a0cf-487">LCS からセットアップ スクリプトをダウンロードするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-487">Follow these steps to download the setup scripts from LCS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a0cf-488">スクリプトは、オンプレミス インフラストラクチャと同じドメイン内のコンピューターから実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-488">The scripts must be executed from a computer in the same domain that the on-premises infrastructure is in.</span></span>

1. <span data-ttu-id="9a0cf-489">[LCS](https://lcs.dynamics.com/v2) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-489">Sign in to [LCS](https://lcs.dynamics.com/v2).</span></span>
2. <span data-ttu-id="9a0cf-490">ダッシュボードで、**共有アセット ライブラリ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-490">On the dashboard, select the **Shared asset library** tile.</span></span>
3. <span data-ttu-id="9a0cf-491">**モデル** タブの、グリッドで、**Dynamics 365 for Operations オンプレミス - 配置スクリプト** 行を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-491">On the **Model** tab, in the grid, select the **Dynamics 365 for Operations on-premises - Deployment scripts** row.</span></span>
4. <span data-ttu-id="9a0cf-492">**バージョン** を選択し、スクリプトの zip ファイルの最新版をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-492">Select **Versions**, and then download the latest version of the zip file for the scripts.</span></span>
   >[!Note] 
   > <span data-ttu-id="9a0cf-493">プラットフォーム更新プログラム 8 またはプラットフォーム更新プログラム 11 の以前のバージョンが必要な場合は、バージョン 1 をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-493">If you need the older version for Platform update 8 or Platform update 11, download version 1.</span></span>
5. <span data-ttu-id="9a0cf-494">zip ファイルを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-494">Right-click the zip file, and then select **Properties**.</span></span> <span data-ttu-id="9a0cf-495">ダイアログ ボックスで、**ブロック解除** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-495">In the dialog box, select the **Unblock** check box.</span></span>
6. <span data-ttu-id="9a0cf-496">ZIP ファイルをスクリプトの実行に使用するマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-496">Copy the zip file to the machine that will be used to execute the scripts.</span></span>
7. <span data-ttu-id="9a0cf-497">**infrastructure** という名前のフォルダーにファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-497">Unzip the files into a folder that is named **infrastructure**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a0cf-498">このフォルダーの ConfigTemplate.xml ファイルにすべての編集を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-498">Ensure all edits are made to the ConfigTemplate.xml file in this folder.</span></span>

### <a name="7-describe-your-configuration"></a><a name="describeconfig"></a> <span data-ttu-id="9a0cf-499">7. コンフィギュレーションの記述</span><span class="sxs-lookup"><span data-stu-id="9a0cf-499">7. Describe your configuration</span></span>

<span data-ttu-id="9a0cf-500">インフラストラクチャの設定 スクリプトは、次のコンフィギュレーション ファイルを使用して設定を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-500">The infrastructure setup scripts use the following configuration files to drive the setup.</span></span>
- <span data-ttu-id="9a0cf-501">infrastructure\ConfigTemplate.xml</span><span class="sxs-lookup"><span data-stu-id="9a0cf-501">infrastructure\ConfigTemplate.xml</span></span>
- <span data-ttu-id="9a0cf-502">infrastructure\D365FO-OP\NodeTopologyDefinition.xml</span><span class="sxs-lookup"><span data-stu-id="9a0cf-502">infrastructure\D365FO-OP\NodeTopologyDefinition.xml</span></span>
- <span data-ttu-id="9a0cf-503">infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml</span><span class="sxs-lookup"><span data-stu-id="9a0cf-503">infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml</span></span>

>[!NOTE]
><span data-ttu-id="9a0cf-504">セットアップ スクリプトが正しく機能するには、環境に基づいてコンフィギュレーション ファイルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-504">Configuration files must be updated based on your environment for the setup scripts to work correctly.</span></span> <span data-ttu-id="9a0cf-505">これらのファイルは、設定に基づいて適切なコンピューター名、IP アドレス、サービス アカウントおよびドメインで更新してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-505">Be sure to update these files with the proper computer names, IP addresses, service accounts, and domain based on your setup.</span></span>

<span data-ttu-id="9a0cf-506">**infrastructure\ConfigTemplate.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-506">**infrastructure\ConfigTemplate.xml** describes:</span></span>
- <span data-ttu-id="9a0cf-507">アプリケーションが動作するために必要なサービス アカウント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-507">Service Accounts that are needed for the application to operate</span></span>
- <span data-ttu-id="9a0cf-508">通信を保護するために必要な証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-508">Certificates necessary for securing communications</span></span>
- <span data-ttu-id="9a0cf-509">データベース コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9a0cf-509">Database configuration</span></span>
- <span data-ttu-id="9a0cf-510">Service Fabric クラスター構成</span><span class="sxs-lookup"><span data-stu-id="9a0cf-510">Service Fabric cluster configuration</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="9a0cf-511">Service Fabric クラスタをコンフィギュレーションする際に OrchestratorType の 3 つのフォールト ドメインがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-511">Make sure that there are three fault domains for OrchestratorType when you configure Service Fabric cluster.</span></span> <span data-ttu-id="9a0cf-512">Service Fabric クラスタをコンフィギュレーションする際、単一のマシンにノードの 1 つのタイプのみが配置されるよう確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-512">Make sure that no more than one type of node is deployed in a single machine when you configure Service Fabric cluster.</span></span>

<span data-ttu-id="9a0cf-513">各 Service Fabric ノード タイプについて、**infrastructure\D365FO-OP\NodeTopologyDefinition.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-513">For each Service Fabric node type, **infrastructure\D365FO-OP\NodeTopologyDefinition.xml** describes:</span></span>

- <span data-ttu-id="9a0cf-514">各ノード タイプとアプリケーション、ドメインとサービス アカウント、および証明書間のマッピング。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-514">The mapping between each node type and the application, domain and service accounts, and certificates.</span></span>
- <span data-ttu-id="9a0cf-515">UAC を有効にするかどうか。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-515">Whether to enable the UAC.</span></span>
- <span data-ttu-id="9a0cf-516">Windows の機能とシステム ソフトウェアの前提条件。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-516">Prerequisites for Windows features and system software.</span></span>
- <span data-ttu-id="9a0cf-517">厳密な名前の検証を有効にするかどうか。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-517">Whether strong name validation should be enabled.</span></span>
- <span data-ttu-id="9a0cf-518">ファイアウォール ポートのリストを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-518">List of firewall ports to be opened.</span></span>

<span data-ttu-id="9a0cf-519">各データベースについて、**infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-519">For each database, **infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml** describes:</span></span>

- <span data-ttu-id="9a0cf-520">データベース設定。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-520">The database settings.</span></span>
- <span data-ttu-id="9a0cf-521">ユーザーとロール間のマッピング。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-521">The mappings between users and roles.</span></span>

#### <a name="create-gmsa-and-domain-user-accounts"></a><span data-ttu-id="9a0cf-522">gMSA およびドメイン ユーザー アカウントを作成する</span><span class="sxs-lookup"><span data-stu-id="9a0cf-522">Create gMSA and domain user accounts</span></span>

1. <span data-ttu-id="9a0cf-523">**インフラストラクチャ** フォルダーに展開したインフラストラクチャ スクリプトがあるマシンに移動します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-523">Navigate to the machine that has the unzipped infrastructure scripts in the **infrastructure** folder.</span></span>
2. <span data-ttu-id="9a0cf-524">**インフラストラクチャ** フォルダーをドメイン コントローラー マシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-524">Copy the **infrastructure** folder to the domain controller machine.</span></span>
3. <span data-ttu-id="9a0cf-525">管理者特権モードで Windows PowerShell を起動し、ディレクトリを **infrastructure** フォルダーに変更して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-525">Start Windows PowerShell in elevated mode, change the directory to the **infrastructure** folder, and run the following commands.</span></span>
    > [!IMPORTANT]
    > <span data-ttu-id="9a0cf-526">次のスクリプトは、ドメイン ユーザー AxServiceUser を作成しません。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-526">The following script doesn't create a domain user AxServiceUser for you.</span></span> <span data-ttu-id="9a0cf-527">ユーザーが作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-527">You must create it yourself.</span></span>

    ```powershell
    Import-Module .\D365FO-OP\D365FO-OP.psd1
    New-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```
    


4. <span data-ttu-id="9a0cf-528">AOS サービス アカウントの **Contoso\svc-AXSF$** および **Contoso\AXServiceUser** をすべての AOS マシンのローカル管理者グループへ追加します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-528">Add the AOS Service Accounts, **Contoso\svc-AXSF$** and **Contoso\AXServiceUser** to the local administrators group for all AOS machines.</span></span> <span data-ttu-id="9a0cf-529">詳細については、「[ローカル グループへのメンバーの追加](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772524(v=ws.11))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-529">For more information, see [Add a member to local group](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772524(v=ws.11)).</span></span>

5. <span data-ttu-id="9a0cf-530">アカウントまたはマシンを変更する必要がある場合は、元の **インフラストラクチャ** フォルダーの ConfigTemplate.xml ファイルを更新し、このマシンにコピーしてから次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-530">If you must make changes to accounts or machines, update the ConfigTemplate.xml file in the original **infrastructure** folder, copy it to this machine and then run the following script.</span></span>

    ```powershell
    Update-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="8-configure-certificates"></a><a name="configurecert"></a> <span data-ttu-id="9a0cf-531">8. 証明書のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9a0cf-531">8. Configure certificates</span></span>

1. <span data-ttu-id="9a0cf-532">**インフラストラクチャ** フォルダーがあるマシンに移動します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-532">Navigate to the machine that has the **infrastructure** folder.</span></span>
2. <span data-ttu-id="9a0cf-533">証明書を生成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-533">Generate certificates:</span></span> 
    1. <span data-ttu-id="9a0cf-534">自己署名証明書を生成する必要がある場合は、次の設定を行います。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-534">If you must generate self-signed certificates:</span></span>
        1. <span data-ttu-id="9a0cf-535">**generateSelfSignedCert** の属性を **true** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-535">Set the **generateSelfSignedCert** attribute to **true**.</span></span> <span data-ttu-id="9a0cf-536">生成する必要がある証明書にのみこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-536">Only set this for the certificates that you need to generate.</span></span> 
        1. <span data-ttu-id="9a0cf-537">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-537">Run the following command.</span></span> <span data-ttu-id="9a0cf-538">スクリプトによって証明書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-538">The script will create the certificates.</span></span> <span data-ttu-id="9a0cf-539">証明書をコンピューターの CurrentUser\My certificate store に格納し、XML ファイルのサムプリントを更新します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-539">Put the certificates in the CurrentUser\My certificate store on the machine, and update the thumbprints in the XML file.</span></span>

        ```powershell
        # Create self-signed certs
        .\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        ```
    1. <span data-ttu-id="9a0cf-540">Active Directory 証明書サービス (AD CS) 証明書を生成する場合は、次の方法で作成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-540">If you want to generate Active Directory Certificate Services (AD CS) certificates:</span></span>
        1. <span data-ttu-id="9a0cf-541">生成したくない証明書の **generateADCSCert** 属性を **false** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-541">Set the **generateADCSCert** attribute to **false** for the certificates that you don't want generated.</span></span>
        1. <span data-ttu-id="9a0cf-542">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-542">Run the following commands.</span></span> <span data-ttu-id="9a0cf-543">スクリプトは、AD CS で証明書テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-543">The script will create the certificate templates in AD CS.</span></span> <span data-ttu-id="9a0cf-544">テンプレートから証明書を生成し、コンピューターの CurrentUser\My certificate store に格納し、XML ファイルのサムプリントを更新します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-544">Generate the certificates from the templates, place the certificates in the CurrentUser\My certificate store on the machine, and update the thumbprints in the XML file.</span></span>

        ```powershell
        .\New-ADCSCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -CreateTemplates
        .\New-ADCSCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        ```

        > [!NOTE] 
        > <span data-ttu-id="9a0cf-545">AD CS スクリプトは、ドメイン コントローラーまたはリモート サーバー管理ツールがインストールされている Windows Server で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-545">The AD CS scripts need to run on a Domain Controller, or a Windows Server with Remote Server Admin Tools installed.</span></span>

3. <span data-ttu-id="9a0cf-546">既に生成されている SSL 証明書を使用している場合は、証明書生成をスキップし、configTemplate.xml ファイルのサムプリントを更新します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-546">If you're using SSL certificates that were already generated, skip the certificate generation and update the thumbprints in the configTemplate.xml file.</span></span> <span data-ttu-id="9a0cf-547">証明書は CurrentUser\My ストアにインストールする必要があり、その秘密キーはエクスポート可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-547">The certificates need to be installed in the CurrentUser\My store and their private keys must be exportable.</span></span>

    > [!WARNING]
    > <span data-ttu-id="9a0cf-548">存在する場合に特定するのが難しい先頭の印刷不可能な特殊文字のため、証明書マネージャーは拇印をコピーするために使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-548">Because of a leading not-printable special character, which is difficult to determine when present, the cert manager should not be used to copy thumbprints.</span></span> <span data-ttu-id="9a0cf-549">印刷できない特殊文字がある場合、**X509 証明書が無効です** というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-549">If the not-printable special character is present, you will get the error, **X509 certificate not valid**.</span></span> <span data-ttu-id="9a0cf-550">拇印を取得するには、PowerShell コマンドの結果を参照するか、PowerShell で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-550">To retrieve the thumbprints, see results from PowerShell commands or run the following commands in PowerShell.</span></span>
    > ```powershell
    > dir cert:\CurrentUser\My
    > dir cert:\LocalMachine\My
    > dir cert:\LocalMachine\Root
    > ```

4. <span data-ttu-id="9a0cf-551">各証明書の **ProtectTo** でユーザーまたはグループのセミコロンで区切られた一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-551">Specify a semi-colon separated list of users or groups in the **ProtectTo** tag for each certificate.</span></span> <span data-ttu-id="9a0cf-552">**ProtectTo** タグで指定された Active Directory ユーザーとグループのみに、スクリプトを使用してエクスポートされる証明書をインポートするアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-552">Only Active directory users and groups specified in the **ProtectTo** tag will have permissions to import the certificates that are exported using the scripts.</span></span> <span data-ttu-id="9a0cf-553">エクスポートした証明書を保護するため、スクリプトによりパスワードがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-553">Passwords are not supported by the script to protect the exported certificates</span></span>

5. <span data-ttu-id="9a0cf-554">証明書を .pfx ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-554">Export the certificates into .pfx files.</span></span> <span data-ttu-id="9a0cf-555">エクスポートの一環として、このスクリプトは、証明書に正しい暗号化プロバイダが設定されているかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-555">As part of the export, this script will check that your certificates have the correct cryptographic provider set.</span></span> 

    ```powershell
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will be written to infrastructure\Certs folder.
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="9-setup-vms"></a><a name="setupvms"></a> <span data-ttu-id="9a0cf-556">9. VM の設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-556">9. Setup VMs</span></span>
1. <span data-ttu-id="9a0cf-557">各 VM で実行する必要があるスクリプトをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-557">Export the scripts that must be run on each VM.</span></span>

    ```powershell
    # Exports the script files to be execute on each VM into a directory VMs\<VMName>.
    .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. <span data-ttu-id="9a0cf-558">次の Microsoft Windows Installers (MSI) を全ての VM でアクセス可能なファイル共有にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-558">Download the following Microsoft Windows Installers (MSIs) into a file share that is accessible by all VMs.</span></span>

    | <span data-ttu-id="9a0cf-559">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="9a0cf-559">Component</span></span> | <span data-ttu-id="9a0cf-560">リンクのダウンロード</span><span class="sxs-lookup"><span data-stu-id="9a0cf-560">Download link</span></span> | <span data-ttu-id="9a0cf-561">必要なファイル名</span><span class="sxs-lookup"><span data-stu-id="9a0cf-561">Expected file name</span></span> |
    |-----------|---------------|--------------------|
    | <span data-ttu-id="9a0cf-562">SNAC – ODBC ドライバー 13</span><span class="sxs-lookup"><span data-stu-id="9a0cf-562">SNAC – ODBC driver 13</span></span> | [<span data-ttu-id="9a0cf-563">ODBC ドライバー 13.1</span><span class="sxs-lookup"><span data-stu-id="9a0cf-563">ODBC driver 13.1</span></span>](/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows#131) | <span data-ttu-id="9a0cf-564">Msodbcsql .msi</span><span class="sxs-lookup"><span data-stu-id="9a0cf-564">msodbcsql.msi</span></span> |
    | <span data-ttu-id="9a0cf-565">SNAC – ODBC ドライバー 17</span><span class="sxs-lookup"><span data-stu-id="9a0cf-565">SNAC – ODBC driver 17</span></span> | <https://aka.ms/downloadmsodbcsql> | <span data-ttu-id="9a0cf-566">msodbcsql\_17.msi</span><span class="sxs-lookup"><span data-stu-id="9a0cf-566">msodbcsql\_17.msi</span></span> |
    | <span data-ttu-id="9a0cf-567">Microsoft SQL ServerManagement Studio 17.5</span><span class="sxs-lookup"><span data-stu-id="9a0cf-567">Microsoft SQL Server Management Studio 17.5</span></span> | [<span data-ttu-id="9a0cf-568">SSMS 17.5</span><span class="sxs-lookup"><span data-stu-id="9a0cf-568">SSMS 17.5</span></span>](/sql/ssms/download-sql-server-management-studio-ssms) | <span data-ttu-id="9a0cf-569">SSMS-Setup-\*.exe</span><span class="sxs-lookup"><span data-stu-id="9a0cf-569">SSMS-Setup-\*.exe</span></span> |
    | <span data-ttu-id="9a0cf-570">Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-570">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</span></span> | <https://support.microsoft.com/help/3179560> | <span data-ttu-id="9a0cf-571">vcredist\_x64.exe</span><span class="sxs-lookup"><span data-stu-id="9a0cf-571">vcredist\_x64.exe</span></span> |
    | <span data-ttu-id="9a0cf-572">Microsoft Visual Studio 2017 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-572">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2017</span></span> | <span data-ttu-id="9a0cf-573"><https://lcs.dynamics.com/V2/SharedAssetLibrary>に移動して、資産タイプとして **モデル** を選択して、**VC++ 17 再配布可能ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-573">Go to <https://lcs.dynamics.com/V2/SharedAssetLibrary>, select **Model** as the asset type, and then select **VC++ 17 Redistributables**.</span></span> | <span data-ttu-id="9a0cf-574">vc\_redist.x64\_14\_16\_27024.exe</span><span class="sxs-lookup"><span data-stu-id="9a0cf-574">vc\_redist.x64\_14\_16\_27024.exe</span></span> |
    | <span data-ttu-id="9a0cf-575">Microsoft Access データベース エンジン 2010 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-575">Microsoft Access Database Engine 2010 Redistributable</span></span> | <https://www.microsoft.com/download/details.aspx?id=13255> | <span data-ttu-id="9a0cf-576">AccessDatabaseEngine\_x64.exe</span><span class="sxs-lookup"><span data-stu-id="9a0cf-576">AccessDatabaseEngine\_x64.exe</span></span> |
    | <span data-ttu-id="9a0cf-577">Microsoft .NET Framework version 4.8 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-577">The Microsoft .NET Framework version 4.8 (CLR 4.0)</span></span> | <https://dotnet.microsoft.com/download/thank-you/net48-offline> | <span data-ttu-id="9a0cf-578">ndp48-x86-x64-allos-enu.exe</span><span class="sxs-lookup"><span data-stu-id="9a0cf-578">ndp48-x86-x64-allos-enu.exe</span></span> |
    | <span data-ttu-id="9a0cf-579">Microsoft .NET Framework version 4.7.2 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-579">The Microsoft .NET Framework version 4.7.2 (CLR 4.0)</span></span> | <https://dotnet.microsoft.com/download/thank-you/net472-offline> | <span data-ttu-id="9a0cf-580">ndp472-x86-x64-allos-enu.exe</span><span class="sxs-lookup"><span data-stu-id="9a0cf-580">ndp472-x86-x64-allos-enu.exe</span></span> |

> [!IMPORTANT]
> - <span data-ttu-id="9a0cf-581">Microsoft SQL Server Management Studio の設定が、対象となるコンピューターのオペレーティング システムと同じ言語であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-581">Make sure the Microsoft SQL Server Management Studio setup is in the same language as the operating system of the target machine.</span></span>
> - <span data-ttu-id="9a0cf-582">前の表の **"必要なファイル名"** 列に指定されている名前がインストーラ ファイルに設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-582">Make sure that the installer files have the names that are specified in the **"Expected file name"** column of the preceding table.</span></span>
> - <span data-ttu-id="9a0cf-583">**"必要なファイル名"** が異なる場合は、一部のダウンロードの名前を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-583">You may need to rename some of the downloads if the **"Expected file name"** is different.</span></span> <span data-ttu-id="9a0cf-584">これを行わないと、"Configure-PreReqs.ps1" スクリプトを実行するときにエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-584">Failure to do so will result in errors when running the "Configure-PreReqs.ps1" script.</span></span>  
> - <span data-ttu-id="9a0cf-585">**VC++ 17 再配布可能ファイル** をダウンロードする場合、実行可能ファイルが zip ファイル内に含まれます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-585">When you download **VC++ 17 Redistributables**, the executable file is inside the zip file.</span></span>

#### <a name="follow-these-steps-for-each-vm-or-use-remoting-from-a-single-machine"></a><span data-ttu-id="9a0cf-586">各 VM についてこれらのステップに従うか、または単一のコンピューターからリモート処理を使用します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-586">Follow these steps for each VM, or use remoting from a single machine</span></span>

> [!NOTE]
> <span data-ttu-id="9a0cf-587">次のセクションでは、複数の VM での実行が必要です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-587">The following section requires execution on multiple VMs.</span></span> <span data-ttu-id="9a0cf-588">このプロセスは、指定されたリモート処理スクリプトを使用して、1 台のマシン (`.\Export-Scripts.ps1` を実行するのと同じマシンなど) から必要なスクリプトを実行するオプションを提供することで、簡単に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-588">This process can be eased by using the supplied remoting scripts, which provide the option of running the necessary scripts from a single machine, such as the same machine used to execute `.\Export-Scripts.ps1`.</span></span> <span data-ttu-id="9a0cf-589">利用可能な場合、リモート処理スクリプトは、PowerShell セクションの「`# If Remoting`」コメントの後に宣言されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-589">The remoting scripts, when available, are declared after a "`# If Remoting`" comment in the PowerShell sections.</span></span> <span data-ttu-id="9a0cf-590">リモート処理スクリプトを使用するときは、セクションの残りのスクリプトを実行する必要はありません。そのような例については、セクションの本文を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-590">When the remoting scripts are used, you may not need to execute the remaining scripts in a section, please see the section text for cases such as that.</span></span> <span data-ttu-id="9a0cf-591">リモート処理では、[WinRM](/windows/win32/winrm/portal) が使用され、特定のケースでは [CredSSP](/windows/win32/secauthn/credential-security-support-provider) が有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-591">Remoting uses [WinRM](/windows/win32/winrm/portal) and requires [CredSSP](/windows/win32/secauthn/credential-security-support-provider) to be enabled in certain cases.</span></span> <span data-ttu-id="9a0cf-592">CredSSP の有効化と無効化は、実行ごとにリモート処理モジュールによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-592">The enabling and disabling of CredSSP is handled by the remoting module on a per-execution basis.</span></span> <span data-ttu-id="9a0cf-593">資格情報の盗難の形でのセキュリティ リスクをもたらすため、CredSSP が使用されていない場合に有効のままにすることはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-593">Keeping CredSSP enabled when it is not in use is not advised, as it introduces security risks in the shape of credential theft.</span></span> <span data-ttu-id="9a0cf-594">設定が完了した場合、[CredSSP を終了処理する](#teardowncredssp) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-594">See the [Tear down CredSSP](#teardowncredssp) section when you are finished setting up.</span></span>

1. <span data-ttu-id="9a0cf-595">各 infrastructure\VMs\<VMName>  フォルダーのコンテンツを対応する VM にコピーし (リモート処理スクリプトが使用されている場合は、自動的にターゲット VM にコンテンツをコピーします)、次のスクリプトを管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-595">Copy the contents of each infrastructure\VMs\<VMName> folder into the corresponding VM (if remoting scripts are used, they will automatically copy the content to the target VMs), and then run the following scripts as an Administrator.</span></span>

    ```powershell
    # Install pre-req software on the VMs.

    # If Remoting, execute
    # .\Configure-PreReqs-AllVMs.ps1 -MSIFilePath <share folder path of the MSIs> -ConfigurationFilePath .\ConfigTemplate.xml

    .\Configure-PreReqs.ps1 -MSIFilePath <path of the MSIs>
    ```

    > [!IMPORTANT]
    > 1. <span data-ttu-id="9a0cf-596">再起動するように求められるたびにコンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-596">Each time you are prompted, restart the machine.</span></span> <span data-ttu-id="9a0cf-597">再起動した後、すべての前提条件がインストールされるまで、`.\Configure-PreReqs.ps1` スクリプトを再実行することを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-597">Make sure that you rerun the `.\Configure-PreReqs.ps1` script after each restart until all of the prerequisites are installed.</span></span> <span data-ttu-id="9a0cf-598">リモート処理の場合、すべてのマシンがオンラインに戻ったときに AllVM スクリプトを再実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-598">In the case of remoting, rerun the AllVMs script when all of the machines are back online.</span></span>
    > 2. <span data-ttu-id="9a0cf-599">リモート処理スクリプトを使用するときに、現在のユーザーが MSI の共有フォルダーにアクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-599">When you use the remoting script, ensure that the current user has access to the share folder of MSIs.</span></span>
    > 3. <span data-ttu-id="9a0cf-600">リモート処理スクリプトを使用するときに、ユーザーが AOSNoteType、MRType、および ReportServerType タイプのマシンにアクセスしていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-600">When you use the remoting script, ensure no user is accessing the AOSNoteType, MRType, and ReportServerType type machines.</span></span> <span data-ttu-id="9a0cf-601">それ以外の場合は、コンピューターにログオンしているユーザーが原因で、リモート処理スクリプトはコンピュータの再起動に失敗します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-601">Otherwise, the remoting script will fail to restart the computer because of the users being logged on to the computer.</span></span>

2. <span data-ttu-id="9a0cf-602">VM セットアップを完了するため、存在する場合は、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-602">Run the following scripts, if they exist, to complete the VM setup.</span></span>

    ```powershell
    # If Remoting, only execute
    # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    # Note: Script "Add-GMSAOnVM.ps1" is not present on BI node 
    .\Add-GMSAOnVM.ps1
    .\Import-PfxFiles.ps1
    .\Set-CertificateAcls.ps1
    ```

3. <span data-ttu-id="9a0cf-603">次のスクリプトを実行して VM のセットアップを検証します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-603">Run the following script to validate the VM setup.</span></span>

    ```powershell
    # If Remoting, execute
    # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    .\Test-D365FOConfiguration.ps1 
    ```

> [!IMPORTANT]
> <span data-ttu-id="9a0cf-604">リモート処理を使用していた場合は、設定が完了するとクリーンアップ手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-604">If remoting was used, be sure to execute the clean up steps when the setup is complete.</span></span> <span data-ttu-id="9a0cf-605">[20. Tear down CredSSP](#teardowncredssp) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-605">See the [20. Tear down CredSSP](#teardowncredssp) section.</span></span>

### <a name="10-set-up-a-standalone-service-fabric-cluster"></a><a name="setupsfcluster"></a> <span data-ttu-id="9a0cf-606">10. スタンドアロン Service Fabric クラスターの設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-606">10. Set up a standalone Service Fabric cluster</span></span>

1. <span data-ttu-id="9a0cf-607">[Service Fabric スタンドアロン インストール パッケージ](https://go.microsoft.com/fwlink/?LinkId=730690) を使用中の Service Fabric ノードのいずれかにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-607">Download the [Service Fabric standalone installation package](https://go.microsoft.com/fwlink/?LinkId=730690) onto one of your Service Fabric nodes.</span></span> <span data-ttu-id="9a0cf-608">ZIP ファイルをダウンロードした後、 ZIP ファイルを右クリックし **プロパティ** を選択してブロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-608">After the zip file is downloaded, unblock it by right-clicking the zip file and then selecting **Properties**.</span></span> <span data-ttu-id="9a0cf-609">ダイアログ ボックスで、右下の **ブロック解除** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-609">In the dialog box, select the **Unblock** check box in the lower right.</span></span>

2. <span data-ttu-id="9a0cf-610">ZIP ファイルを Service Fabric クラスター内のいずれかのノードにコピーし、解凍します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-610">Copy the zip file to one of the nodes in the Service Fabric cluster, and unzip it.</span></span> <span data-ttu-id="9a0cf-611">**インフラストラクチャ** フォルダーが、このフォルダーにアクセスすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-611">Ensure the **infrastructure** folder has access to this folder.</span></span>

3. <span data-ttu-id="9a0cf-612">**インフラストラクチャ** フォルダーに移動し、次のコマンドを実行して Service Fabric Cluster の ClusterConfig.json ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-612">Navigate to the **infrastructure** folder and execute the following command to generate the Service Fabric ClusterConfig.json file.</span></span>

    ```powershell
   .\New-SFClusterConfig.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -TemplateConfig <ServiceFabricStandaloneInstallerPath>\ClusterConfig.X509.MultiMachine.json
    ```
4. <span data-ttu-id="9a0cf-613">クラスター コンフィギュレーションへの追加の変更は、環境に基づいて必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-613">Additional modifications to your cluster configuration may be necessary based on your environment.</span></span> <span data-ttu-id="9a0cf-614">詳細については、[手順 1B: 複数のマシンでクラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)、[X.509 証明書を使用して Windows スタンドアロン クラスターを保護する](/azure/service-fabric/service-fabric-windows-cluster-x509-security)、および[Windows Server で実行されているスタンドアロン クラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-614">For more information, see, [Step 1B: Create a multi-machine cluster](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Secure a standalone cluster on Windows using X.509 certificates](/azure/service-fabric/service-fabric-windows-cluster-x509-security), and [Create a standalone cluster running on Windows Server](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).</span></span>

5. <span data-ttu-id="9a0cf-615">生成された ClusterConfig.json ファイルを \<ServiceFabricStandaloneInstallerPath\> にコピーします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-615">Copy the generated ClusterConfig.json file to the \<ServiceFabricStandaloneInstallerPath\>.</span></span>

6. <span data-ttu-id="9a0cf-616">上位の権限を使用して Windows PowerShell で  \<ServiceFabricStandaloneInstallerPath\>  にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-616">Navigate to the \<ServiceFabricStandaloneInstallerPath\> in Windows PowerShell by using elevated privileges.</span></span> <span data-ttu-id="9a0cf-617">次のコマンドを実行して ClusterConfig をテストします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-617">Run the following command to test ClusterConfig.</span></span>

    ```powershell
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

7. <span data-ttu-id="9a0cf-618">テストが成功した場合は、次のコマンドを実行してクラスターを展開します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-618">If the test is successful, run the following command to deploy the cluster.</span></span>

    ```powershell
    # If using offline (internet-disconnected) install
    # .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json -FabricRuntimePackagePath <Path to MicrosoftAzureServiceFabric.cab download>
    
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

8. <span data-ttu-id="9a0cf-619">クラスターが作成された後は、任意のクライアント マシンで Service Fabric エクスプローラーを開き、インストールを検証します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-619">After the cluster is created, open the Service Fabric explorer on any client machine to validate the installation.</span></span>

    1. <span data-ttu-id="9a0cf-620">まだインストールされていない場合、CurrentUser\\My に Service Fabric クライアント証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-620">Install the Service Fabric client certificate in CurrentUser\\My if it isn't already installed.</span></span>
    2. <span data-ttu-id="9a0cf-621">**IE 設定** \> **互換モード** に移動し、**互換モードでイントラネット サイトを表示する** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-621">Go to **IE settings** \> **Compatibility Mode**, and clear the **Display Intranet sites in compatibility mode** check box.</span></span>
    3. <span data-ttu-id="9a0cf-622">`https://sf.d365ffo.onprem.contoso.com:19080` に移動します。sf.d365ffo.onprem.contoso.com は、ゾーンで指定されている Service Fabric クラスターのホスト名です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-622">Go to `https://sf.d365ffo.onprem.contoso.com:19080`, where sf.d365ffo.onprem.contoso.com is the host name of the Service Fabric cluster that is specified in the zone.</span></span> <span data-ttu-id="9a0cf-623">DNS 名前解決が設定されていない場合は、マシンの IP アドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-623">If DNS name resolution isn't configured, use the IP address of the machine.</span></span>
    4. <span data-ttu-id="9a0cf-624">クライアントの証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-624">Select the client certificate.</span></span> <span data-ttu-id="9a0cf-625">**Service Fabric エクスプローラー** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-625">The **Service Fabric explorer** page appears.</span></span>
    5. <span data-ttu-id="9a0cf-626">すべてのノードが緑で表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-626">Verify that all nodes are appear as green.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="9a0cf-627">クライアント マシンが Windows Server 2016 のようなサーバー コンピューターである場合は、**Service Fabric エクスプローラー** ページにアクセスするときに IE のセキュリティ強化の構成をオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-627">If your client machine is a server machine like Windows Server 2016, you must turn off the IE Enhanced Security Configuration when you access the **Service Fabric explorer** page.</span></span>
    > <span data-ttu-id="9a0cf-628">ウィルス対策ソフトウェアがインストールされている場合は、[Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) ドキュメントのガイダンスに従って除外を設定してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-628">If any antivirus software is installed, ensure you set exclusion following the guidance in the [Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) documentation.</span></span>

### <a name="11-configure-lcs-connectivity-for-the-tenant"></a><a name="configurelcs"></a> <span data-ttu-id="9a0cf-629">11. テナント用 LCS 接続のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9a0cf-629">11. Configure LCS connectivity for the tenant</span></span>

<span data-ttu-id="9a0cf-630">Finance + Operations の展開とサービスは、オンプレミスのローカル エージェントを使用して LCS を通じて調整されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-630">Deployment and servicing of Finance + Operations is orchestrated through LCS by using an on-premises local agent.</span></span> <span data-ttu-id="9a0cf-631">LCS から Finance + Operations テナントへの接続を確立するには、Azure AD テナント (たとえば、Contoso.onmicrosoft.com) の代わりに動作するローカル エージェントを可能にする認定資格を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-631">To establish connectivity from LCS to the Finance + Operations tenant, you must configure a certificate that enables the local agent to act on behalf on your Azure AD tenant (for example, Contoso.onmicrosoft.com).</span></span>

<span data-ttu-id="9a0cf-632">証明機関から取得したオンプレミス エージェントの証明書またはスクリプトを使用して生成した自己署名証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-632">Use the on-premises agent certificate that you acquired from a certificate authority or the self-signed certificate that you generated by using scripts.</span></span>

<span data-ttu-id="9a0cf-633">オンプレミス エージェント証明書は、テナントごとに複数のサンドボックス環境および実稼動環境で再利用できます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-633">The on-premises agent certificate can be reused across multiple sandbox and production environments per tenant.</span></span>

<span data-ttu-id="9a0cf-634">グローバル管理者ディレクトリの役割を持つユーザー アカウントだけが、LCS を承認するための証明書を追加できます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-634">Only user accounts that have the Global Administrator directory role can add certificates to authorize LCS.</span></span> <span data-ttu-id="9a0cf-635">既定では、組織の Microsoft 365 にサインアップする担当者がディレクトリのグローバル管理者です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-635">By default, the person who signs up for Microsoft 365 for your organization is the global administrator for the directory.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="9a0cf-636">テナントごとに証明書を正確に **1** 回構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-636">You must configure the certificate exactly **one** time per tenant.</span></span> <span data-ttu-id="9a0cf-637">同じ環境のすべてのオンプレミス環境では、同じ証明書を使用して LCS に接続できます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-637">All on-premises environments under the same tenant must use the same certificate to connect with LCS.</span></span>
> - <span data-ttu-id="9a0cf-638">Windows Server 2016 などのサーバー コンピューターでこれを実行する場合は、IE セキュリティ強化の構成を一時的にオフに必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-638">If you run this in a server machine like Windows Server 2016, you must turn off the IE Enhanced Security Configuration temporarily.</span></span> <span data-ttu-id="9a0cf-639">そうしないと、Azure ログイン ウィンドウのコンテンツはブロックされます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-639">If you don't, the Azure login window content will be blocked.</span></span>

1. <span data-ttu-id="9a0cf-640">[顧客の Azure ポータル](https://portal.azure.com) にサインインして、グローバル管理者ディレクトリの役割があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-640">Sign in to the [customer's Azure portal](https://portal.azure.com) to verify that you have the Global Administrator directory role.</span></span>

2. <span data-ttu-id="9a0cf-641">次のスクリプトを **インフラストラクチャ** フォルダーから実行して、証明書が既に登録されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-641">Determine whether the certificate is already registered by running the following script from the **Infrastructure** folder.</span></span>

    ```powershell
    # If you have issues downloading the Azure PowerShell Az module, run the following:
    # [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    
    Install-Module Az
    Import-Module Az
    .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint' -Test
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="9a0cf-642">既に AzureRM をインストールしている場合は、PowerShell 5.1 の既存の AzureRM インストールと互換性がない可能性があるのため、削除してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-642">If you previously installed AzureRM, please remove it as it may not be compatible with any existing AzureRM installs in PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="9a0cf-643">詳細については、[Azure PowerShell を AzureRM から Az に移行する](/powershell/azure/migrate-from-azurerm-to-az) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-643">For more information, [Migrate Azure PowerShell from AzureRM to Az](/powershell/azure/migrate-from-azurerm-to-az).</span></span>

3. <span data-ttu-id="9a0cf-644">証明書が登録されていないことをスクリプトが示している場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-644">If the script indicates that the certificate isn't registered, run the following command.</span></span>

    ```powershell
    .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint'
    ```

> [!NOTE]
> <span data-ttu-id="9a0cf-645">ログイン アカウントに関連付けられた複数のテナントがある場合、コンテキストが正しいテナントに設定されていることを確認するために、テナント ID をパラメーターとして渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-645">If you have multiple tenants associated with the login account, you can pass the tenant ID as a parameter to ensure that the context is set to the correct tenant.</span></span>

> ```powershell
> .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint' -TenantId 'xxxx-xxxx-xxxx-xxxx'
> ```

### <a name="12-set-up-file-storage"></a><a name="setupfile"></a> <span data-ttu-id="9a0cf-646">12.ファイル ストレージの設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-646">12. Set up file storage</span></span>

<span data-ttu-id="9a0cf-647">以下の SMB 3.0 ファイル共有を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-647">You must set up the following SMB 3.0 file shares:</span></span>

- <span data-ttu-id="9a0cf-648">AOS にアップロードされるユーザー ドキュメントを格納するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\aos-storage)。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-648">A file share that stores user documents that are uploaded to AOS (for example, \\\\DAX7SQLAOFILE1\\aos-storage).</span></span>
- <span data-ttu-id="9a0cf-649">デプロイメントを調整するための最新のビルド ファイルと構成ファイルを保存するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\agent)。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-649">A file share that stores the latest build and configuration files to orchestrate the deployment (for example, \\\\DAX7SQLAOFILE1\\agent).</span></span>

    > [!WARNING]
    > <span data-ttu-id="9a0cf-650">共有に入れるファイルの最大パス長を超えないように、このファイル共有パスはできるだけ短くしておいてください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-650">Keep this file share path as short as possible to avoid exceeding the maximum path length on the files that will be put in the share.</span></span>

<span data-ttu-id="9a0cf-651">SMB 3.0 を有効にする方法については、[SMB セキュリティの強化](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn551363(v=ws.11)#BKMK_disablesmb1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-651">For information about how to enable SMB 3.0, see [SMB Security Enhancements](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn551363(v=ws.11)#BKMK_disablesmb1).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="9a0cf-652">セキュリティで保護されたダイアレクト ネゴシエーションでは、SMB 2.0 または 3.0 から SMB 1.0 へのダウングレードを検出または防止できません。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-652">Secure dialect negotiation can't detect or prevent downgrades from SMB 2.0 or 3.0 to SMB 1.0.</span></span> <span data-ttu-id="9a0cf-653">したがって、SMB 1.0 サーバーを無効にすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-653">Therefore, we strongly recommend that you disable the SMB 1.0 server.</span></span> <span data-ttu-id="9a0cf-654">SMB 1.0 サーバーを無効にすることで、SMB 暗号化のすべての機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-654">By disabling the SMB 1.0 server, you can take advantage of the full capabilities of SMB encryption.</span></span>
> - <span data-ttu-id="9a0cf-655">環境内の残りの部分でデータが保護されていることを保証するために、BitLocker ドライブ暗号化をすべてのマシンで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-655">To help ensure that your data is protected while it's at rest in your environment, BitLocker Drive Encryption must be enabled on every machine.</span></span> <span data-ttu-id="9a0cf-656">BitLocker を有効にする方法については、[BitLocker: Windows Server 2012 以降で配置する方法](/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-656">For information about how to enable BitLocker, see [BitLocker: How to deploy on Windows Server 2012 and later](/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server).</span></span>

1. <span data-ttu-id="9a0cf-657">ファイル共有マシンで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-657">On the file share machine, run the following command.</span></span>

    ```powershell
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```

2. <span data-ttu-id="9a0cf-658">\\\\DAX7SQLAOFILE1\\aos-storage ファイル共有を設定するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-658">Follow these steps to set up the \\\\DAX7SQLAOFILE1\\aos-storage file share:</span></span>

   1. <span data-ttu-id="9a0cf-659">サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-659">In Server Manager, select **File and Storage Services** \> **Shares**.</span></span>
   2. <span data-ttu-id="9a0cf-660">**タスク**\>**新しい共有** を選択し、新しい共有を作成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-660">Select **Tasks** \> **New Share** to create a new share.</span></span> <span data-ttu-id="9a0cf-661">共有に **aos-storage** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-661">Name the share **aos-storage**.</span></span>
   3. <span data-ttu-id="9a0cf-662">**共有のキャッシュを許可** を選択したままにします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-662">Leave **Allow caching of share** selected.</span></span>
   4. <span data-ttu-id="9a0cf-663">**データ アクセスを暗号化** を確認してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-663">Check **Encrypt data access**.</span></span>
   5. <span data-ttu-id="9a0cf-664">OrchestratorType を除いて、Service Fabric クラスター内のすべてのマシンに対して **変更** 許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-664">Grant **Modify** permissions for every machine in the Service Fabric cluster except OrchestratorType.</span></span>
   6. <span data-ttu-id="9a0cf-665">AOS ドメイン ユーザー (contoso\\AXServiceUser) と gMSA ユーザー (contoso\\svc-AXSF$) に対して、**変更** アクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-665">Grant **Modify** permissions for the user AOS domain user (contoso\\AXServiceUser) and the gMSA user (contoso\\svc-AXSF$).</span></span>

      >[!NOTE]
      > <span data-ttu-id="9a0cf-666">マシンを追加するために **オブジェクト タイプ** の下の **コンピューター** を、またはサービス アカウントを追加するために **オブジェクト タイプ** 下の **サービス アカウント** を有効にする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-666">You may need to enable **Computers** under **Object Types** to add machines or enable **Service Accounts** under **Object Types** to add service accounts.</span></span>

3. <span data-ttu-id="9a0cf-667">\\\\DAX7SQLAOFILE1\\ エージェント ファイル共有を設定するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-667">Follow these steps to set up the \\\\DAX7SQLAOFILE1\\agent file share:</span></span>

    1. <span data-ttu-id="9a0cf-668">サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-668">In Server Manager, select **File and Storage Services** \> **Shares**.</span></span>
    2. <span data-ttu-id="9a0cf-669">**タスク**\>**新しい共有** を選択し、新しい共有を作成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-669">Select **Tasks** \> **New Share** to create a new share.</span></span> <span data-ttu-id="9a0cf-670">共有に **エージェント** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-670">Name the share **agent**.</span></span>
    3. <span data-ttu-id="9a0cf-671">ローカル展開エージェント (contoso\\svc-LocalAgent$) の gMSA ユーザーに対して **フル コントロール** のアクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-671">Grant **Full-Control** permissions to the gMSA user for the local deployment agent (contoso\\svc-LocalAgent$).</span></span>

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

### <a name="13-set-up-sql-server"></a><a name="setupsql"></a> <span data-ttu-id="9a0cf-672">13. SQL Server の設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-672">13. Set up SQL Server</span></span>

1. <span data-ttu-id="9a0cf-673">高可用性を備えた SQL Server 2016 SP2 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-673">Install SQL Server 2016 SP2 with high availability.</span></span> <span data-ttu-id="9a0cf-674">(SQL Server の 1 つのインスタンスで十分なサンドボックス環境に配置している場合を除きます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-674">(Unless you're deploying in a sandbox environment, where one instance of SQL Server is sufficient.</span></span> <span data-ttu-id="9a0cf-675">高可用性シナリオをテストするため、サンドボックス環境に高可用性の SQL Server をインストールできます。)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-675">You may want to install SQL Server with high availability in sandbox environments to test high-availability scenarios.)</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="9a0cf-676">[SQL Server および Windows 認証モード](/sql/database-engine/configure-windows/change-server-authentication-mode) を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-676">You must enable the [SQL Server and Windows Authentication mode](/sql/database-engine/configure-windows/change-server-authentication-mode).</span></span>

    <span data-ttu-id="9a0cf-677">高可用性を備えた SQL Server を、SAN (ストレージ エリア ネットワーク) を含む SQL クラスターまたは Always-On 構成のいずれかとしてインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-677">You can install SQL Server with high availability either as SQL clusters that include a Storage Area Network (SAN) or in an Always-On configuration.</span></span> <span data-ttu-id="9a0cf-678">データベース エンジン、SSRS、フルテキスト検索、および管理ツールがインストール済みであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-678">Verify that the Database Engine, SSRS, Full-Text Search, and Management Tools are already installed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a0cf-679">Always-On が [初期データ同期ページの選択 (可用性グループ ウィザードで常に使用する)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) で説明されているとおりに設定され、[セカンダリ データベースを手動で準備する](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs) の指示に従っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-679">Make sure that Always-On is set up as described in [Select Initial Data Synchronization Page (Always On Availability Group Wizards)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards), and follow the instructions in [To Prepare Secondary Databases Manually](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs).</span></span>

2. <span data-ttu-id="9a0cf-680">ドメイン ユーザーまたはグループ管理サービス アカウントとして SQL サービスを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-680">Run the SQL service as a domain user or a group-managed service account.</span></span>
3. <span data-ttu-id="9a0cf-681">Finance + Operations 向けに SQL Server を構成するために証明機関から SSL 証明書を取得します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-681">Get an SSL certificate from a certificate authority to configure SQL Server for Finance + Operations.</span></span> <span data-ttu-id="9a0cf-682">テストの目的で、自己署名証明書または AD CS 証明書を作成して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-682">For testing purposes, you can create and use a self-signed certificate or an AD CS certificate.</span></span> <span data-ttu-id="9a0cf-683">次の例にあるコンピューター名とドメイン名を置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-683">You will need to replace the computer name and domain name in the following examples.</span></span>

    <span data-ttu-id="9a0cf-684">**Always-On SQL インスタンスの証明書**</span><span class="sxs-lookup"><span data-stu-id="9a0cf-684">**Certificates for an Always-On SQL instance**</span></span>

    <span data-ttu-id="9a0cf-685">Always-On 用の証明書のテストを設定する場合は、次の **リモート処理** スクリプトを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-685">If you are setting up testing certificates for Always-On, use the following **remoting** script.</span></span> <span data-ttu-id="9a0cf-686">これにより、次の **手動** スクリプトが実行され、手順 **a ～ e** が実行されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-686">This will perform the same as the following **manual** script and steps **a-e**.</span></span>

    1. <span data-ttu-id="9a0cf-687">自己署名証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-687">Self-signed certificate</span></span>

        ```powershell
        .\New-SelfSigned-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser
        ```

    1. <span data-ttu-id="9a0cf-688">AD CS 証明書</span><span class="sxs-lookup"><span data-stu-id="9a0cf-688">AD CS certificate</span></span>

        ```powershell
        .\New-ADCS-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser
        ```

    <span data-ttu-id="9a0cf-689">**SQL Server を使用した Always-On SQL または Windows Serverフェールオーバー クラスタリングの手動自己署名ステップ**</span><span class="sxs-lookup"><span data-stu-id="9a0cf-689">**Manual self-signed steps for an Always-On SQL instance or Windows Server Failover Clustering with SQL Server**</span></span> 
        
    <span data-ttu-id="9a0cf-690">SQL クラスターの各ノードに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-690">For each node of the SQL cluster, follow these steps.</span></span> 

    1. <span data-ttu-id="9a0cf-691">次の PowerShell スクリプトを、SQL Server Always-On レプリカごとに実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-691">Run the following PowerShell script on each of the SQL Server Always-On replicas.</span></span>

    ```powershell
    # Manually create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
    # Run script on each node
    $computerName = $env:COMPUTERNAME.ToLower()
    $domain = $env:USERDNSDOMAIN.ToLower()
    $listenerName = 'dax7sqlaosqla'
    $cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider' -CertStoreLocation "cert:\LocalMachine\My" -KeyAlgorithm "RSA" -HashAlgorithm "sha256" -KeyLength 2048
    ```

    2. <span data-ttu-id="9a0cf-692">SQL サービスを実行するために使用されるアカウントに証明書のアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-692">Grant certificate permissions to the account that is used to run the SQL service.</span></span> 
        1. <span data-ttu-id="9a0cf-693">\[コンピューター証明書の管理\] (**certlm.msc**) を開きます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-693">Open Manage Computer Certificates (**certlm.msc**).</span></span>
        2. <span data-ttu-id="9a0cf-694">作成した証明書を右クリックし、**タスク** \> **プライベート キーの管理** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-694">Right-click the certificate created, and then select **Tasks** \> **Manage Private Keys**.</span></span>
        3. <span data-ttu-id="9a0cf-695">SQL Server サービス アカウントを追加し、読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-695">Add in the SQL Server service account and grant Read access.</span></span>
    3. <span data-ttu-id="9a0cf-696">Microsoft SQL Server Configuration Manager で **ForceEncryption** と新しい **証明書** を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-696">Enable **ForceEncryption** and the new **Certificate** in Microsoft SQL Server Configuration Manager.</span></span>
        1. <span data-ttu-id="9a0cf-697">**SQL Server 構成マネージャー** で、**SQL Server ネットワークの構成** を展開し、**サーバーのインスタンスのプロトコル** を右クリックしてから、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-697">In **SQL Server Configuration Manager**, expand **SQL Server Network Configuration**, right-click **Protocols for [server instance]**, and then select **Properties**.</span></span>
        2. <span data-ttu-id="9a0cf-698">**プロトコル** ダイアログ ボックスの **証明書** タブで、**証明書** ボックスのドロップダウン メニューから目的の証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-698">In the **Properties** dialog box, on the **Certificate** tab, select the desired certificate from the drop-down menu for the **Certificate** box.</span></span>
        3. <span data-ttu-id="9a0cf-699">**プロパティ** ダイアログ ボックスの **フラグ** タブにある **ForceEncryption** ボックスで、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-699">In the **Properties** dialog box, on the **Flags** tab, in the **ForceEncryption** box, select **Yes**.</span></span>
        4. <span data-ttu-id="9a0cf-700">**OK** を選択して保存します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-700">Select **OK** to save.</span></span>
    4. <span data-ttu-id="9a0cf-701">各 SQL クラスター ノードから証明書 (.cer ファイル) をエクスポートし、各 Service Fabric ノードの信頼できるルートにインストールします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-701">Export the certificate (.cer file) from each SQL cluster node, and install it in the trusted root of each Service Fabric node.</span></span> <span data-ttu-id="9a0cf-702">Always-On クラスターには少なくとも 2 つの証明書がありますが、追加のレプリカがある場合はそれ以上の証明書が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-702">You will have a minimum of 2 certificates for the Always-On cluster, but there may be more if you have additional replicas.</span></span> 
    5. <span data-ttu-id="9a0cf-703">SQL Server サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-703">Restart the SQL Server service.</span></span>
   > [!NOTE] 
   > <span data-ttu-id="9a0cf-704">詳細は、[Microsoft 管理コンソールを使用して SQL Server のインスタンスに対する SSL 暗号化を有効にする方法](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-704">For more information, see [How to enable SSL encryption for an instance of SQL Server by using Microsoft Management Console](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console).</span></span>



> [!IMPORTANT]
> <span data-ttu-id="9a0cf-705">リモート処理を使用していた場合は、設定が完了するとクリーンアップ手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-705">If remoting was used, be sure to execute the clean up steps when the setup is complete.</span></span> <span data-ttu-id="9a0cf-706">詳細については、[20. CredSSP を終章処理する](#teardowncredssp) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-706">See the [20. Tear down CredSSP](#teardowncredssp) section for more information.</span></span>

### <a name="14-configure-the-databases"></a><a name="configuredb"></a> <span data-ttu-id="9a0cf-707">14. データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9a0cf-707">14. Configure the databases</span></span>

1. <span data-ttu-id="9a0cf-708">[LCS](https://lcs.dynamics.com/v2) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-708">Sign in to [LCS](https://lcs.dynamics.com/v2).</span></span>

2. <span data-ttu-id="9a0cf-709">ダッシュボードで、**共有アセット ライブラリ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-709">On the dashboard, select the **Shared asset library** tile.</span></span>

3. <span data-ttu-id="9a0cf-710">**モデル** タブで、必要なリリースのデモ データを選択し、zip ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-710">On the **Model** tab, select the demo data for the release that you want and download the zip file.</span></span>

    | <span data-ttu-id="9a0cf-711">リリース</span><span class="sxs-lookup"><span data-stu-id="9a0cf-711">Release</span></span> | <span data-ttu-id="9a0cf-712">デモ データ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-712">Demo data</span></span> |
    |-------|------|
    | <span data-ttu-id="9a0cf-713">オンプレミスの一般提供 (GA) リリース</span><span class="sxs-lookup"><span data-stu-id="9a0cf-713">On-premises General Availability (GA) release</span></span> | <span data-ttu-id="9a0cf-714">Dynamics 365 for Operations オンプレミス - デモ データ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-714">Dynamics 365 for Operations on-premises - Demo data</span></span> |
    | <span data-ttu-id="9a0cf-715">オンプレミスのプラットフォーム更新プログラム 2017 年 11 月 11 日リリース</span><span class="sxs-lookup"><span data-stu-id="9a0cf-715">On-premises Platform Update 11 Nov 2017 release</span></span> | <span data-ttu-id="9a0cf-716">Dynamics 365 for Operations オンプレミス Enterprise Edition - 更新プログラム 11 デモ データ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-716">Dynamics 365 for Operations on-premises, Enterprise edition - Update 11 Demo data</span></span> |
    | <span data-ttu-id="9a0cf-717">オンプレミスのプラットフォーム更新プログラム 2018 年 3 月 12 日リリース</span><span class="sxs-lookup"><span data-stu-id="9a0cf-717">On-premises Platform Update 12 Mar 2018 release</span></span> | <span data-ttu-id="9a0cf-718">Dynamics 365 for Operations オンプレミス Enterprise Edition - 更新プログラム 12 デモ データ</span><span class="sxs-lookup"><span data-stu-id="9a0cf-718">Dynamics 365 for Operations on-premises, Enterprise edition - Update 12 Demo data</span></span> |

4. <span data-ttu-id="9a0cf-719">zip ファイルには空のデモデータ .bak ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-719">The zip file contains empty and demo data .bak files.</span></span> <span data-ttu-id="9a0cf-720">必要に応じて、.bak ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-720">Select the .bak file, based on your requirements.</span></span> <span data-ttu-id="9a0cf-721">たとえば、デモ データが必要な場合は、AxBootstrapDB_Demodata.bak ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-721">For example, if you require demo data, download the AxBootstrapDB_Demodata.bak file.</span></span>

5. <span data-ttu-id="9a0cf-722">infrastructure\ConfigTempate.xml のデータベース セクションが、次のように正しく構成されているか確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-722">Ensure the database section in the infrastructure\ConfigTempate.xml is configured correctly with the following:</span></span>
    1. <span data-ttu-id="9a0cf-723">データベース名。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-723">The database name.</span></span>
    2. <span data-ttu-id="9a0cf-724">db ファイルとログ設定。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-724">The db file and log settings.</span></span> <span data-ttu-id="9a0cf-725">dbの設定は、指定された既定値以上にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-725">The db settings should not be lower than the defaults specified.</span></span>
    3. <span data-ttu-id="9a0cf-726">LCS 共有アセット ライブラリからダウンロードされるバックアップ ファイルへのパス。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-726">The path to the backup file downloaded from LCS Shared Asset library.</span></span> <span data-ttu-id="9a0cf-727">Finance + Operations データベースの既定の名前は AXDB です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-727">The default name for the Finance + Operations database is AXDB.</span></span>

   > [!WARNING]
   > - <span data-ttu-id="9a0cf-728">SQL サービスを実行しているユーザーとスクリプトを実行しているユーザーは、バックアップ ファイルが格納されているフォルダーまたは共有に対して READ アクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-728">The user running the SQL service and the user running the scripts should have READ access on the folder or share where the backup file is located.</span></span>
   > 
   > - <span data-ttu-id="9a0cf-729">同じ名前のデータベースが存在する場合は、データベースが再利用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-729">If a database with the same name exists, the database will be reused.</span></span>

6. <span data-ttu-id="9a0cf-730">**インフラストラクチャ** フォルダーを SQL Server マシンにコピーし、権限を昇格した PowerShell ウィンドウでそのフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-730">Copy the **infrastructure** folder to the SQL Server machine and navigate to it in a PowerShell window with elevate privileges.</span></span>

#### <a name="configure-the-orchestratordata-database"></a><span data-ttu-id="9a0cf-731">OrchestratorData データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9a0cf-731">Configure the OrchestratorData database</span></span>

1. <span data-ttu-id="9a0cf-732">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-732">Execute the following script.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
   ```

   <span data-ttu-id="9a0cf-733">スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-733">The script will do the following:</span></span>
  
   - <span data-ttu-id="9a0cf-734">**OrchestratorData** という名前の空のデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-734">Create an empty database named **OrchestratorData**.</span></span> <span data-ttu-id="9a0cf-735">このデータベースは、オンプレミスのローカル エージェントによって配置を調整するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-735">This database is used by the on-premises local agent to orchestrate deployments.</span></span>
   - <span data-ttu-id="9a0cf-736">データベースにローカル エージェント gMSA (svc-LocalAgent$) **db\_owner** アクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-736">Grant the local agent gMSA (svc-LocalAgent$) **db\_owner** permissions on the database.</span></span>

#### <a name="configure-the-finance--operations-database"></a><span data-ttu-id="9a0cf-737">Finance + Operations データベースの構成</span><span class="sxs-lookup"><span data-stu-id="9a0cf-737">Configure the Finance + Operations database</span></span>

1. <span data-ttu-id="9a0cf-738">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-738">Execute the following scripts.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
   .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
   ```

   <span data-ttu-id="9a0cf-739">**Initialize-Database.ps1** スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-739">The **Initialize-Database.ps1** script will do the following:</span></span>

   1. <span data-ttu-id="9a0cf-740">指定されたバックアップ ファイルからデータベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-740">Restore the database from the specified backup file.</span></span>
   2. <span data-ttu-id="9a0cf-741">SQL 認証が有効になっている新しいユーザーを作成します (axdbadmin)。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-741">Create a new user that has SQL authentication enabled (axdbadmin).</span></span>
   3. <span data-ttu-id="9a0cf-742">AXDB の次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-742">Map users to database roles based on the following table for AXDB.</span></span>

      | <span data-ttu-id="9a0cf-743">ユーザー</span><span class="sxs-lookup"><span data-stu-id="9a0cf-743">User</span></span>            | <span data-ttu-id="9a0cf-744">種類</span><span class="sxs-lookup"><span data-stu-id="9a0cf-744">Type</span></span>    | <span data-ttu-id="9a0cf-745">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="9a0cf-745">Database role</span></span> |
      |-----------------|---------|---------------|
      | <span data-ttu-id="9a0cf-746">svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-746">svc-AXSF$</span></span>       | <span data-ttu-id="9a0cf-747">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-747">gMSA</span></span>    | <span data-ttu-id="9a0cf-748">db\_owner</span><span class="sxs-lookup"><span data-stu-id="9a0cf-748">db\_owner</span></span>     |
      | <span data-ttu-id="9a0cf-749">svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-749">svc-LocalAgent$</span></span> | <span data-ttu-id="9a0cf-750">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-750">gMSA</span></span>    | <span data-ttu-id="9a0cf-751">db\_owner</span><span class="sxs-lookup"><span data-stu-id="9a0cf-751">db\_owner</span></span>     |
      | <span data-ttu-id="9a0cf-752">svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-752">svc-FRPS$</span></span>       | <span data-ttu-id="9a0cf-753">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-753">gMSA</span></span>    | <span data-ttu-id="9a0cf-754">db\_owner</span><span class="sxs-lookup"><span data-stu-id="9a0cf-754">db\_owner</span></span>     |
      | <span data-ttu-id="9a0cf-755">svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-755">svc-FRAS$</span></span>       | <span data-ttu-id="9a0cf-756">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-756">gMSA</span></span>    | <span data-ttu-id="9a0cf-757">db\_owner</span><span class="sxs-lookup"><span data-stu-id="9a0cf-757">db\_owner</span></span>     |
      | <span data-ttu-id="9a0cf-758">axdbadmin</span><span class="sxs-lookup"><span data-stu-id="9a0cf-758">axdbadmin</span></span>       | <span data-ttu-id="9a0cf-759">SqlUser</span><span class="sxs-lookup"><span data-stu-id="9a0cf-759">SqlUser</span></span> | <span data-ttu-id="9a0cf-760">db\_owner</span><span class="sxs-lookup"><span data-stu-id="9a0cf-760">db\_owner</span></span>     |


   4. <span data-ttu-id="9a0cf-761">TempDB の次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-761">Map users to database roles based on the following table for TempDB.</span></span>

      | <span data-ttu-id="9a0cf-762">ユーザー</span><span class="sxs-lookup"><span data-stu-id="9a0cf-762">User</span></span>            | <span data-ttu-id="9a0cf-763">種類</span><span class="sxs-lookup"><span data-stu-id="9a0cf-763">Type</span></span>    | <span data-ttu-id="9a0cf-764">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="9a0cf-764">Database role</span></span> |
      |-----------------|---------|---------------|
      | <span data-ttu-id="9a0cf-765">svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-765">svc-AXSF$</span></span>       | <span data-ttu-id="9a0cf-766">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-766">gMSA</span></span>    | <span data-ttu-id="9a0cf-767">db_datareader, db_datawriter, db_ddladmin</span><span class="sxs-lookup"><span data-stu-id="9a0cf-767">db_datareader, db_datawriter, db_ddladmin</span></span>     |
      | <span data-ttu-id="9a0cf-768">axdbadmin</span><span class="sxs-lookup"><span data-stu-id="9a0cf-768">axdbadmin</span></span>       | <span data-ttu-id="9a0cf-769">SqlUser</span><span class="sxs-lookup"><span data-stu-id="9a0cf-769">SqlUser</span></span> | <span data-ttu-id="9a0cf-770">db_datareader, db_datawriter, db_ddladmin</span><span class="sxs-lookup"><span data-stu-id="9a0cf-770">db_datareader, db_datawriter, db_ddladmin</span></span>     |

   <span data-ttu-id="9a0cf-771">**Configure-Database.ps1** スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-771">The **Configure-Database.ps1** script will do the following:</span></span>

    1. <span data-ttu-id="9a0cf-772">READ_COMMITTED_SNAPSHOT ON を設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-772">Set READ_COMMITTED_SNAPSHOT ON</span></span>
    2. <span data-ttu-id="9a0cf-773">ALLOW_SNAPSHOT_ISOLATION ON を設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-773">Set ALLOW_SNAPSHOT_ISOLATION ON</span></span>
    3. <span data-ttu-id="9a0cf-774">指定したデータベース ファイルとログの設定を設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-774">Set the specified database file and log settings</span></span>
    4. <span data-ttu-id="9a0cf-775">サーバー状態の表示を axdbadmin に付与</span><span class="sxs-lookup"><span data-stu-id="9a0cf-775">GRANT VIEW SERVER STATE TO axdbadmin</span></span>
    5. <span data-ttu-id="9a0cf-776">イベント セッション変更の権限を axdbadmin に付与</span><span class="sxs-lookup"><span data-stu-id="9a0cf-776">GRANT ALTER ANY EVENT SESSION TO axdbadmin</span></span>
    6. <span data-ttu-id="9a0cf-777">サーバー状態の表示を [contoso\svc AXSF$] に付与</span><span class="sxs-lookup"><span data-stu-id="9a0cf-777">GRANT VIEW SERVER STATE TO [contoso\svc-AXSF$]</span></span>
    7. <span data-ttu-id="9a0cf-778">イベント セッションの変更権限を [contoso\svc-AXSF$] に付与</span><span class="sxs-lookup"><span data-stu-id="9a0cf-778">GRANT ALTER ANY EVENT SESSION TO [contoso\svc-AXSF$]</span></span>

2. <span data-ttu-id="9a0cf-779">データベース ユーザーをリセットするには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-779">Run the following command to reset the database users.</span></span>

    ```powershell
    .\Reset-DatabaseUsers.ps1 -DatabaseServer '<FQDN of the SQL server>' -DatabaseName '<AX database name>'
    ```

#### <a name="configure-the-financial-reporting-database"></a><span data-ttu-id="9a0cf-780">財務レポート データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9a0cf-780">Configure the Financial Reporting database</span></span>

1. <span data-ttu-id="9a0cf-781">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-781">Execute the following script.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName MR
   ```

   <span data-ttu-id="9a0cf-782">スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-782">The script will do the following:</span></span>
   1. <span data-ttu-id="9a0cf-783">**FinancialReporting** という名前の空のデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-783">Create an empty database named **FinancialReporting**.</span></span>
   2. <span data-ttu-id="9a0cf-784">次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-784">Map the users to database roles based on the following table.</span></span>

      | <span data-ttu-id="9a0cf-785">ユーザー</span><span class="sxs-lookup"><span data-stu-id="9a0cf-785">User</span></span>            | <span data-ttu-id="9a0cf-786">種類</span><span class="sxs-lookup"><span data-stu-id="9a0cf-786">Type</span></span> | <span data-ttu-id="9a0cf-787">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="9a0cf-787">Database role</span></span> |
      |-----------------|------|---------------|
      | <span data-ttu-id="9a0cf-788">svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-788">svc-LocalAgent$</span></span> | <span data-ttu-id="9a0cf-789">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-789">gMSA</span></span> | <span data-ttu-id="9a0cf-790">db\_owner</span><span class="sxs-lookup"><span data-stu-id="9a0cf-790">db\_owner</span></span>     |
      | <span data-ttu-id="9a0cf-791">svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-791">svc-FRPS$</span></span>       | <span data-ttu-id="9a0cf-792">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-792">gMSA</span></span> | <span data-ttu-id="9a0cf-793">db\_owner</span><span class="sxs-lookup"><span data-stu-id="9a0cf-793">db\_owner</span></span>     |
      | <span data-ttu-id="9a0cf-794">svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="9a0cf-794">svc-FRAS$</span></span>       | <span data-ttu-id="9a0cf-795">gMSA</span><span class="sxs-lookup"><span data-stu-id="9a0cf-795">gMSA</span></span> | <span data-ttu-id="9a0cf-796">db\_owner</span><span class="sxs-lookup"><span data-stu-id="9a0cf-796">db\_owner</span></span>     |

### <a name="15-encrypt-credentials"></a><a name="encryptcred"></a> <span data-ttu-id="9a0cf-797">15. 資格情報の暗号化</span><span class="sxs-lookup"><span data-stu-id="9a0cf-797">15. Encrypt credentials</span></span>

1. <span data-ttu-id="9a0cf-798">任意のクライアント マシンで、LocalMachine\\My certificate store に暗号化証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-798">On any client machine, install the encipherment certificate in the LocalMachine\\My certificate store.</span></span>
2. <span data-ttu-id="9a0cf-799">現在のユーザーにこの証明書の秘密キーへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-799">Grant the current user read access to the private key of this certificate.</span></span>
3. <span data-ttu-id="9a0cf-800">次のようにして、Credentials.json ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-800">Create the Credentials.json file, as shown here.</span></span>

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

    - <span data-ttu-id="9a0cf-801">**AccountPassword** は、AOS ドメインユーザー (contoso\\axserviceuser) の暗号化されたドメイン ユーザー パスワードです。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-801">**AccountPassword** is the encrypted domain user password for the AOS domain user (contoso\\axserviceuser).</span></span>
    - <span data-ttu-id="9a0cf-802">**SqlUser** は、Finance + Operations データベース (AXDB) にアクセスできる暗号化された SQL ユーザー (axdbadmin) で、**SqlPassword** は暗号化された SQL パスワードです。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-802">**SqlUser** is the encrypted SQL user (axdbadmin) that has access to the Finance + Operations database (AXDB), and **SqlPassword** is the encrypted SQL password.</span></span>

4. <span data-ttu-id="9a0cf-803">.json ファイルを SMB ファイル共有、\\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json にコピーします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-803">Copy the .json file to the SMB file share, \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.</span></span>
5. <span data-ttu-id="9a0cf-804">暗号化された値で Credentials.json ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-804">Update the Credentials.json file with encrypted values.</span></span>

    ```powershell
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | Set-Clipboard
    ```
    > [!IMPORTANT]
    > <span data-ttu-id="9a0cf-805">*Invoke-ServiceFabricEncryptText* を起動する前に、[Microsoft Azure Service Fabric SDK](/azure/service-fabric/service-fabric-get-started#sdk-installation-only) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-805">Before you can invoke *Invoke-ServiceFabricEncryptText*, you need to install [Microsoft Azure Service Fabric SDK](/azure/service-fabric/service-fabric-get-started#sdk-installation-only).</span></span>
    > <span data-ttu-id="9a0cf-806">Azure Service Fabric SDK をインストールした後で、"Invoke-ServiceFabricEncryptText は認識されないコマンドです" というエラーが発生した場合は、コンピューターを再起動して再試行してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-806">If you encounter the following error, "Invoke-ServiceFabricEncryptText is not recognized command" after you install the Azure Service Fabric SDK, restart the computer and retry.</span></span>

    > [!WARNING]
    > <span data-ttu-id="9a0cf-807">すべての **ServiceFabricEncryptText** コマンドの起動が完了したら、Windows PowerShell の履歴を削除することを忘れないでください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-807">After you've finished invoking all **Invoke-ServiceFabricEncryptText** commands, remember to delete the Windows PowerShell history.</span></span> <span data-ttu-id="9a0cf-808">それ以外の場合は、暗号化されていない資格情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-808">Otherwise, your non-encrypted credentials will be visible.</span></span>

### <a name="16-set-up-ssis"></a><a name="setupssis"></a> <span data-ttu-id="9a0cf-809">16. SSIS の設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-809">16. Set up SSIS</span></span>

<span data-ttu-id="9a0cf-810">データ管理と統合ワークロードを有効にするには、各 AOS 仮想マシンに SSIS をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-810">To enable Data management and Integration workloads, SSIS must be installed on each of the AOS virtual machines.</span></span> <span data-ttu-id="9a0cf-811">各 AOS 仮想マシン上で、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-811">Complete the following steps on each AOS virtual machine.</span></span>

1. <span data-ttu-id="9a0cf-812">マシンに SSIS インストールへのアクセス許可があることを確認し、SSIS セットアップ ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-812">Verify that the machine has access to the SSIS installation and open the SSIS Setup Wizard.</span></span>
2. <span data-ttu-id="9a0cf-813">**機能の選択** ウィンドウの **機能** ウィンドウで、**Integration Services** および **SQL クライアント接続 SDK** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-813">In the **Feature Selection** window, in the **Features** pane, select the **Integration Services** and **SQL Client Connectivity SDK** check boxes.</span></span>
3. <span data-ttu-id="9a0cf-814">セットアップを完了し、インストールが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-814">Complete the setup and verify that the installation was successful.</span></span>

<span data-ttu-id="9a0cf-815">詳細については、[統合サービスのインストール](/sql/integration-services/install-windows/install-integration-services) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-815">For more information, see [Install integration services](/sql/integration-services/install-windows/install-integration-services).</span></span>

### <a name="17-set-up-ssrs"></a><a name="setupssrs"></a> <span data-ttu-id="9a0cf-816">17. SSRS の設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-816">17. Set up SSRS</span></span>

1. <span data-ttu-id="9a0cf-817">開始する前に、このトピックの冒頭に記載されている前提条件がインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-817">Before you begin, make sure that the prerequisites that are listed at the beginning of this topic are installed.</span></span>
2. <span data-ttu-id="9a0cf-818">[オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション](../analytics/configure-ssrs-on-premises.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-818">Follow the steps in [Configure SQL Server Reporting Services for on-premises deployments](../analytics/configure-ssrs-on-premises.md).</span></span>
    > [!IMPORTANT]
    > <span data-ttu-id="9a0cf-819">SSRS のインストール時にデータベース エンジンをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-819">You must install then database engine when you install SSRS.</span></span>

### <a name="18-configure-ad-fs"></a><a name="configureadfs"></a><span data-ttu-id="9a0cf-820">18. AD FS のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9a0cf-820">18. Configure AD FS</span></span>

<span data-ttu-id="9a0cf-821">この手順を完了する前に、AD FS を Windows Server 2016 に展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-821">Before you can complete this procedure, AD FS must be deployed on Windows Server 2016.</span></span> <span data-ttu-id="9a0cf-822">AD FS を展開する方法については、[Windows Server 2016 配置ガイドおよび 2012 R2 AD FS 配置ガイド](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-822">For information about how to deploy AD FS, see [Deployment Guide Windows Server 2016 and 2012 R2 AD FS Deployment Guide](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).</span></span>

<span data-ttu-id="9a0cf-823">Finance + Operations では、AD FS の既定で標準のコンフィギュレーション以外の追加のコンフィギュレーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-823">Finance + Operations requires additional configuration beyond the default out-of-box configuration of AD FS.</span></span> <span data-ttu-id="9a0cf-824">以下の Windows PowerShell コマンドを、AD FS ロール サービスがインストールされているマシン上で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-824">The following Windows PowerShell commands must be run on the machine where the AD FS role service is installed.</span></span> <span data-ttu-id="9a0cf-825">ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-825">The user account must have enough permissions to administer AD FS.</span></span> <span data-ttu-id="9a0cf-826">たとえば、ユーザーには、ドメイン管理者アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-826">For example, the user must have a domain administrator account.</span></span> <span data-ttu-id="9a0cf-827">複雑な AD FS シナリオでは、ドメイン管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-827">For complex AD FS scenarios, consult your domain administrator.</span></span>

1. <span data-ttu-id="9a0cf-828">AD FS 識別子を構成して、AD FS トークン発行者と一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-828">Configure the AD FS identifier so that it matches the AD FS token issuer.</span></span>

   <span data-ttu-id="9a0cf-829">このコマンドは、Finance + Operations クライアントの **ユーザー** ページ (**システム管理 > ユーザー > ユーザー**) で **ユーザーをインポート** オプションを使用した新しいユーザーの追加に関連しています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-829">This command is related to adding new users using the **Import users** option on the **Users** page (**System administration > Users > Users**) in the Finance + Operations client.</span></span>

    ```PowerShell
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. <span data-ttu-id="9a0cf-830">混在環境用に AD FS を構成していない限り、イントラネット認証接続用に Windows 統合認証 (WIA) を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-830">You should disable Windows Integrated Authentication (WIA) for intranet authentication connections, unless you've configured AD FS for mixed environments.</span></span> <span data-ttu-id="9a0cf-831">WIA を AD FS で使用できるように構成する方法の詳細については、[AD FS で Windows 統合認証 (WIA) を使用するようにブラウザを構成する](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-831">For more information about how to configure WIA so that it can be used with AD FS, see [Configure browsers to use Windows Integrated Authentication (WIA) with AD FS](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).</span></span>

   <span data-ttu-id="9a0cf-832">このコマンドは、Finance + Operations クライアントへのログイン時のフォーム認証の使用に関連しています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-832">This command is related to using forms authentication upon signing into the Finance + Operations client.</span></span> <span data-ttu-id="9a0cf-833">シングル サインインなどの他のオプションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-833">Other options, such as single sign-on, are not supported.</span></span>

    ```powershell
    Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
    ```

3. <span data-ttu-id="9a0cf-834">サインインの場合、ユーザーの電子メール アドレスは許容される認証入力でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-834">For sign-in, the user's email address must be an acceptable authentication input.</span></span>

   <span data-ttu-id="9a0cf-835">このコマンドは、電子メール要求の設定に関連しています。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-835">This command is related to setting up email claims.</span></span> <span data-ttu-id="9a0cf-836">変換ルールなど、追加の設定が必要な他のオプションが使用可能な場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-836">Other options, such as transformation rules, may be available which require additional setup.</span></span>

    ```powershell
    Add-Type -AssemblyName System.Net
    $fqdn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
    $domainName = $fqdn.Substring($fqdn.IndexOf('.')+1)
    Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
    ```

<span data-ttu-id="9a0cf-837">AD FS が認証を交換するために Finance + Operations を信頼するためには、AD FS アプリケーション グループの下の AD FS にさまざまなアプリケーション エントリを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-837">In order for AD FS to trust Finance + Operations for the exchange of authentication, various application entries must be registered in AD FS under an AD FS application group.</span></span> <span data-ttu-id="9a0cf-838">設定プロセスをスピードアップし、エラーを減らすために、次のスクリプトを使用して登録します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-838">To speed up the setup process and help reduce errors, you can use the following script for registration.</span></span> <span data-ttu-id="9a0cf-839">Publish-ADFSApplicationGroup.ps1 スクリプトと D365FO-OP ディレクトリを、AD FS ロール サービスがインストールされているマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-839">Copy the Publish-ADFSApplicationGroup.ps1 script and D365FO-OP directory to a machine where the AD FS role service is installed.</span></span> <span data-ttu-id="9a0cf-840">次に、AD FS を管理するための十分なアクセス許可を持つユーザー アカウントを使用してスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-840">Then run the script by using a user account that has enough permissions to administer AD FS.</span></span> <span data-ttu-id="9a0cf-841">(たとえば、管理者アカウントを使用します。)</span><span class="sxs-lookup"><span data-stu-id="9a0cf-841">(For example, use an administrator account.)</span></span>

<span data-ttu-id="9a0cf-842">スクリプトの使用方法の詳細については、スクリプトに記載されているドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-842">For more information about how to use the script, see the documentation that is listed in the script.</span></span> <span data-ttu-id="9a0cf-843">後の手順の LCS でこの情報が必要となるため、出力に指定されているクライアント ID を書き留めておいてください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-843">Make a note of the client IDs that are specified in the output, because you will need this information in LCS in a later step.</span></span> <span data-ttu-id="9a0cf-844">クライアント ID を紛失した場合、AD FS がインストールされているコンピューターにログインし、**サーバー マネージャー** \> **ツール** \> **AD FS の管理** \> **アプリケーション グループ** \> **Microsoft Dynamics 365 for Operations On-premises** を開き、ネイティブ アプリケーションでクライアント ID を見つけます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-844">Should you lose the client IDs, log in to the machine which has AD FS installed, open **Server Manager** \> **Tools** \> **AD FS Management** \> **Application Groups** \> **Microsoft Dynamics 365 for Operations On-premises** and find the client IDs under the native applications.</span></span>

> [!NOTE]
> <span data-ttu-id="9a0cf-845">以前に構成した AD FS サーバーを別の環境で再利用する方法については、[複数の環境に同じ AD FS インスタンスを再使用する](./onprem-reuseadfs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-845">If you want to reuse your previously configured AD FS server for additional environments, see [Reuse the same AD FS instance for multiple environments](./onprem-reuseadfs.md).</span></span>

```powershell
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
```

![アプリケーション グループのプロパティ](./media/OPSetup_05_ApplicatioGroupProperties.png)

<span data-ttu-id="9a0cf-847">最後に、**AOSNodeType** タイプの Service Fabric ノード上の AD FS OpenID コンフィギュレーション URL にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-847">Finally, make sure that you can access the AD FS OpenID Configuration URL on a Service Fabric node of the **AOSNodeType** type.</span></span> <span data-ttu-id="9a0cf-848">このチェックを行うには、Web ブラウザーで `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` を開きます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-848">To perform this check, try to open `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` in a web browser.</span></span> <span data-ttu-id="9a0cf-849">サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていません。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-849">If you receive a message that states that the site isn't secure, you haven't added your AD FS SSL certificate to the Trusted Root Certification Authorities store.</span></span> <span data-ttu-id="9a0cf-850">このステップについては、「AD FS 展開ガイド」で説明されています。リモーティングを使用している場合は、次のスクリプトを使用して、Service Fabric クラスター内のすべてのノードに証明書をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-850">This step is described in the AD FS deployment guide, and if you are using remoting, you can use the following script to install the certificate on all nodes in the Service Fabric cluster:</span></span>

```powershell
# If remoting, execute
.\Install-ADFSCert-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

<span data-ttu-id="9a0cf-851">URL に正常にアクセスすると、AD FS コンフィギュレーションを含む JavaScript Object Notation (JSON) ファイルが返され、AD FS URL が信頼されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-851">If you successfully access the URL, a JavaScript Object Notation (JSON) file is returned that contains your AD FS configuration, and you will see that your AD FS URL is trusted.</span></span>

<span data-ttu-id="9a0cf-852">これで、インフラストラクチャの設定を完了しました。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-852">You've now completed the setup of the infrastructure.</span></span> <span data-ttu-id="9a0cf-853">次のセクションでは、[LCS](https://lcs.dynamics.com) にアクセスしてコネクタを設定し、Finance + Operations 環境を配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-853">The following sections describe how to navigate to [LCS](https://lcs.dynamics.com) to set up your connector and deploy your Finance + Operations environment.</span></span>

### <a name="19-configure-a-connector-and-install-an-on-premises-local-agent"></a><a name="configureconnector"></a> <span data-ttu-id="9a0cf-854">19. コネクタのコンフィギュレーションと、オンプレミスのローカル エージェントのインストール</span><span class="sxs-lookup"><span data-stu-id="9a0cf-854">19. Configure a connector and install an on-premises local agent</span></span>

1. <span data-ttu-id="9a0cf-855">[LCS](https://lcs.dynamics.com/) にサインインし、オンプレミスの実装プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-855">Sign in to [LCS](https://lcs.dynamics.com/), and open the on-premises implementation project.</span></span>
2. <span data-ttu-id="9a0cf-856">ハンバーガー メニューで、**プロジェクト設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-856">On the hamburger menu, select **Project settings**.</span></span>

    ![プロジェクト設定コマンド](./media/OPSetup_06_ProjectSettings.png)

3. <span data-ttu-id="9a0cf-858">**オンプレミス コネクタ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-858">Select **On-premises connectors**.</span></span>
4. <span data-ttu-id="9a0cf-859">新しいコネクタを作成するには、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-859">Select **Add** to create a new connector.</span></span> 
5. <span data-ttu-id="9a0cf-860">**ホスト インフラストラクチャ設定** タブで、エージェント インストーラーをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-860">On the **Setup host infrastructure** tab, download the agent installer.</span></span>

    ![[ホスト インフラストラクチャ設定] タブで、エージェント インストーラー ボタンをダウンロードする](./media/OPSetup_07_DownloadAgentInstaller.png)
    
6. <span data-ttu-id="9a0cf-862">zip ファイルがブロックされていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-862">Verify that the zip file is unblocked.</span></span> <span data-ttu-id="9a0cf-863">ファイルを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-863">Right-click the file, and then select **Properties**.</span></span> <span data-ttu-id="9a0cf-864">ダイアログ ボックスで **ブロック解除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-864">In the dialog box, select **Unblock**.</span></span>
7. <span data-ttu-id="9a0cf-865">**OrchestratorType** タイプの Service Fabric ノードの 1 つでエージェント インストーラーを解凍します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-865">Unzip the agent installer on one of the Service Fabric nodes of the **OrchestratorType** type.</span></span>
8. <span data-ttu-id="9a0cf-866">**構成エージェント** タブで、コンフィギュレーションの設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-866">On the **Configure agent** tab, enter the configuration settings.</span></span> <span data-ttu-id="9a0cf-867">必要な値を取得するには、そのマシンと構成ファイルにアクセスできる任意のマシンで次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-867">Execute the following script on any machine with access to it and the configuration file, to get the needed values.</span></span>

    ```powershell
    .\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

9. <span data-ttu-id="9a0cf-868">コンフィギュレーションを保存し、**コンフィギュレーションのダウンロード** を選択して、localagent-config.json コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-868">Save the configuration, and then select **Download configurations** to download the localagent-config.json configuration file.</span></span>

    ![[エージェントの設定] タブの [コンフィギュレーションのダウンロード] ボタン](./media/OPSetup_08_DownloadConfigurations.png)

10. <span data-ttu-id="9a0cf-870">localagent-config.json ファイルを、エージェント インストーラー パッケージが配置されているマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-870">Copy the localagent-config.json file to the machine where the agent installer package is located.</span></span>
11. <span data-ttu-id="9a0cf-871">**コマンド プロンプト** ウィンドウで、エージェント インストーラーを含むフォルダーに移動して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-871">In a **Command Prompt** window, run the following command by navigating to the folder that contains the agent installer.</span></span>

    ```powershell
    LocalAgentCLI.exe Install <path of config.json>
    ```

    > [!NOTE]
    > <span data-ttu-id="9a0cf-872">このコマンドを実行するユーザーは、OrchestratorData データベースに対して **db\_owner** のアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-872">The user who runs this command must have **db\_owner** permissions on the OrchestratorData database.</span></span>

12. <span data-ttu-id="9a0cf-873">ローカル エージェントが正常にインストールされると、LCS のオンプレミス コネクタに戻るようにします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-873">After the local agent is successfully installed, navigate back to your on-premises connector in LCS.</span></span>
13. <span data-ttu-id="9a0cf-874">**設定の検証** タブで、**メッセージ エージェント** を選択して、ローカル エージェントへの LCS 接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-874">On the **Validate setup** tab, select **Message agent** to test for LCS connectivity to your local agent.</span></span> <span data-ttu-id="9a0cf-875">接続が正常に確立されると、ページは下図のようになります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-875">When a connection is successfully established, the page will resemble the following illustration.</span></span>

    ![エージェントの検証](./media/ValidateAgent.PNG)

### <a name="20-tear-down-credssp-if-remoting-was-used"></a><a name="teardowncredssp"></a> <span data-ttu-id="9a0cf-877">20. リモート処理が使用された場合、CredSSP を終了処理する</span><span class="sxs-lookup"><span data-stu-id="9a0cf-877">20. Tear down CredSSP, if remoting was used</span></span>

<span data-ttu-id="9a0cf-878">セットアップ中にリモート処理スクリプトのいずれかが使用された場合は、セットアップ プロセスの中断時または完了時に、次のスクリプトを実行してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-878">If any of the remoting scripts were used during setup, be sure to execute the following script when there are breaks in the setup process, or the setup has finished.</span></span>

```powershell
.\Disable-CredSSP-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

<span data-ttu-id="9a0cf-879">前のリモート PowerShell ウィンドウが誤って終了し、CredSSP が有効にまったままである場合、スクリプトにより、コンフィギュレーション ファイルで指定されたすべてのコンピューター上で無効にされます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-879">If the previous remoting PowerShell window was accidentally closed and CredSSP was left enabled, the script will disable it on all the machines specified in the configuration file.</span></span>

### <a name="21-deploy-your-finance--operations-environment-from-lcs"></a><a name="deploy"></a> <span data-ttu-id="9a0cf-880">21. LCS から Finance + Operations 環境を配置する</span><span class="sxs-lookup"><span data-stu-id="9a0cf-880">21. Deploy your Finance + Operations environment from LCS</span></span>

1. <span data-ttu-id="9a0cf-881">LCS で、オンプレミス プロジェクトに移動し、**環境** > **サンドボックス** に移動してから **構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-881">In LCS, navigate to your on-premises project, go to **Environment** > **Sandbox**, and then select **Configure**.</span></span> <span data-ttu-id="9a0cf-882">必要な値を取得するには、ADFS および DNS サーバー設定にアクセスする必要があるプライマリ ドメイン コントローラ VM で次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-882">Execute the following script on the primary domain controller VM, which must have access to ADFS and the DNS server settings, to get the needed values.</span></span>

    ```powershell
    .\Get-DeploymentSettings.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. <span data-ttu-id="9a0cf-883">新しい展開では、環境のトポロジを選択し、展開を開始するウィザードを完了します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-883">For new deployments, select your environment topology, and then complete the wizard to start your deployment.</span></span>

    ![環境の配置](./media/Deploy.png)

3. <span data-ttu-id="9a0cf-885">既存のプラットフォーム更新プログラム 8 またはプラットフォーム更新プログラム 11 を展開する場合:</span><span class="sxs-lookup"><span data-stu-id="9a0cf-885">If you have an existing Platform update 8 or Platform update 11 deployment:</span></span> 
    - <span data-ttu-id="9a0cf-886">ローカル エージェントを更新します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-886">Update the local agent.</span></span> <span data-ttu-id="9a0cf-887">詳細については、[ローカル エージェントの更新](../lifecycle-services/update-local-agent.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-887">See [Update the local agent](../lifecycle-services/update-local-agent.md) for more details.</span></span>
    - <span data-ttu-id="9a0cf-888">LCS からローカル エージェントを検証します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-888">Validate the local agent from LCS.</span></span>
    - <span data-ttu-id="9a0cf-889">[環境を再構成して新しいプラットフォームまたはトポロジを採用する](../lifecycle-services/reconfigure-environment.md) の手順を実行している間に、プラットフォーム更新 12 を配置します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-889">Deploy Platform update 12 while going through the steps in [Reconfigure environments to take a new platform or topology](../lifecycle-services/reconfigure-environment.md).</span></span>
4. <span data-ttu-id="9a0cf-890">LCS は準備フェーズ中に環境の Service Fabric アプリケーション パッケージを組み立てます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-890">LCS will assemble the Service Fabric application packages for your environment during the preparation phase.</span></span> <span data-ttu-id="9a0cf-891">配置を開始するローカル エージェントにメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-891">It then sends a message to the local agent to start deployment.</span></span> <span data-ttu-id="9a0cf-892">下記のように、**準備中** ステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-892">You will notice the **Preparing** status as below.</span></span>

    ![準備フェーズ](./media/Preparing.png)

    <span data-ttu-id="9a0cf-894">以下に示すような環境の詳細ページに移動するには、**完全な詳細** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-894">Click **Full details** to take you to the environment details page, as shown below.</span></span>

    ![環境の詳細ページ](./media/Details_Preparing.png)

5. <span data-ttu-id="9a0cf-896">ローカル エージェントは配置要求を受け取り、配置を開始し、環境の準備ができたら LCS に再度通知します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-896">The local agent will now pick up the deployment request, start the deployment, and communicate back to LCS when the environment is ready.</span></span> <span data-ttu-id="9a0cf-897">表示されているとおりに、配置の開始がしたときに、ステータスは **配置** に変更します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-897">When deployment starts, the status will change to **Deploying**, as shown.</span></span>

    ![ステータスを展開に変更する](./media/Deploying.png)

    ![環境を展開する](./media/Details_Deploying.png)

    <span data-ttu-id="9a0cf-900">展開に失敗した場合、LCS のお客様の環境では、**再設定** ボタンは次のように利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-900">If the deployment fails, the **Reconfigure** button will become available for your environment in LCS, as shown below.</span></span> <span data-ttu-id="9a0cf-901">基になる問題を修正し、**再コンフィギュレーション** をクリックして、任意のコンフィギュレーションの変更を更新し、**配置** をクリックして配置を再試行します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-901">Fix the underlying issue, click **Reconfigure**, update any configuration changes, and click **Deploy** to retry the deployment.</span></span>

    ![再構成ボタンが使用可能になる](./media/Failed.png)

    <span data-ttu-id="9a0cf-903">再構成の方法の詳細については、[環境を再構成して、新しいプラットフォームまたはトポロジを採用する](../lifecycle-services/reconfigure-environment.md) のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-903">See the [Reconfigure environments to take a new platform or topology](../lifecycle-services/reconfigure-environment.md) topic for details about how to reconfigure.</span></span> <span data-ttu-id="9a0cf-904">次の図は、正常な配置を示します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-904">The following graphic shows a successful deployment.</span></span>

    ![環境が正常に配置された](./media/Deployed.png)

### <a name="22-connect-to-your-finance--operations-environment"></a><a name="connect"></a> <span data-ttu-id="9a0cf-906">22. Finance + Operations 環境への接続</span><span class="sxs-lookup"><span data-stu-id="9a0cf-906">22. Connect to your Finance + Operations environment</span></span>
<span data-ttu-id="9a0cf-907">ブラウザーで、https://[yourD365FOdomain]/namespaces/AXSF に移動し、そこでは yourD365FOdomain がこのトピックの[ドメイン名と DNS ゾーンの計画](#plandomain) セクションで定義したドメイン名です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-907">In your browser, navigate to https://[yourD365FOdomain]/namespaces/AXSF, where yourD365FOdomain is the domain name that you defined in the [Plan your domain name and DNS zones](#plandomain) section of this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a0cf-908">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9a0cf-908">Additional resources</span></span>
- [<span data-ttu-id="9a0cf-909">オンプレミス配置への更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="9a0cf-909">Apply updates to on-premises deployments</span></span>](apply-updates-on-premises.md)
- [<span data-ttu-id="9a0cf-910">オンプレミス環境の再配置</span><span class="sxs-lookup"><span data-stu-id="9a0cf-910">Redeploy on-premises environments</span></span>](redeploy-on-prem.md)
- [<span data-ttu-id="9a0cf-911">ドキュメント管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9a0cf-911">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
- [<span data-ttu-id="9a0cf-912">電子申告 (ER) コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="9a0cf-912">Import Electronic reporting (ER) configurations</span></span>](../analytics/electronic-reporting-import-ger-configurations.md)
- [<span data-ttu-id="9a0cf-913">オンプレミス配置でのドキュメントの生成、発行、印刷</span><span class="sxs-lookup"><span data-stu-id="9a0cf-913">Document generation, publishing, and printing in on-premises deployments</span></span>](../analytics/printing-capabilities-on-premises.md)
- [<span data-ttu-id="9a0cf-914">オンプレミス環境用プロキシの構成</span><span class="sxs-lookup"><span data-stu-id="9a0cf-914">Configure proxies for on-premises environments</span></span>](onprem-reverseproxy.md)
- [<span data-ttu-id="9a0cf-915">Finance and Operations アプリのテクニカル サポートの設定</span><span class="sxs-lookup"><span data-stu-id="9a0cf-915">Set up technical support for Finance and Operations apps</span></span>](../lifecycle-services/support-experience.md)
- [<span data-ttu-id="9a0cf-916">クライアントのインターネット接続</span><span class="sxs-lookup"><span data-stu-id="9a0cf-916">Client internet connectivity</span></span>](../user-interface/client-disconnected.md)

## <a name="known-issues"></a><span data-ttu-id="9a0cf-917">既知の問題</span><span class="sxs-lookup"><span data-stu-id="9a0cf-917">Known issues</span></span>

### <a name="error-key-does-not-exist-when-running-the-new-d365fogmsaaccounts-cmdlet"></a><span data-ttu-id="9a0cf-918">New-D365FOGMSAAccounts cmdlet を実行した際のエラー、「キーが存在しません」</span><span class="sxs-lookup"><span data-stu-id="9a0cf-918">Error "Key does not exist" when running the New-D365FOGMSAAccounts cmdlet</span></span>
<span data-ttu-id="9a0cf-919">ドメインでグループ管理サービス アカウント パスワードを初めて作成し生成する場合は、最初に **キー配分サービス KDS ルート キー** を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-919">If this is your first time creating and generating group Managed Service Account passwords in your domain, you need to first create the **Key Distribution Services KDS Root Key**.</span></span> <span data-ttu-id="9a0cf-920">詳細については、[キー配分サービス KDS ルート キーの作成](/windows-server/security/group-managed-service-accounts/create-the-key-distribution-services-kds-root-key)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-920">For more information, see [Create the Key Distribution Services KDS Root Key](/windows-server/security/group-managed-service-accounts/create-the-key-distribution-services-kds-root-key).</span></span>

### <a name="error-the-winrm-client-cannot-process-the-request-when-running-the-remoting-script-configure-prereqs-allvms-cmdlet"></a><span data-ttu-id="9a0cf-921">リモート処理スクリプト Configure-Prereqs-AllVms cmdlet を実行した際のエラー、「WinRM クライアントは要求を処理できません」</span><span class="sxs-lookup"><span data-stu-id="9a0cf-921">Error "The WinRM client cannot process the request" when running the remoting script Configure-Prereqs-AllVms cmdlet</span></span>
<span data-ttu-id="9a0cf-922">Service Fabric Cluster のすべてのマシンでコンピューター ポリシー **新しい資格情報委任を許可** を有効にするには、エラー メッセージの指示に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-922">You need to follow the instructions in the error message to enable the computer policy **Allow delegation fresh credentials** in all machines of Service Fabric cluster.</span></span>

### <a name="error-not-process-argument-transformation-on-parameter-test-cannot-convert-value-systemstring-to-type-systemmanagementautomationswitchparameter-when-running-the-config-prereqs-allvms-cmdlet"></a><span data-ttu-id="9a0cf-923">エラー、「'テスト'パラメータでの引数変換を処理できません」</span><span class="sxs-lookup"><span data-stu-id="9a0cf-923">Error "Not process argument transformation on parameter 'Test'.</span></span> <span data-ttu-id="9a0cf-924">Config-Prereqs-AllVms cmdlet 実行時、値 "System.String" を、タイプ "System.Management.Automation.SwitchParameter" に変換することはできません</span><span class="sxs-lookup"><span data-stu-id="9a0cf-924">Cannot convert value "System.String" to type "System.Management.Automation.SwitchParameter" when running the Config-Prereqs-AllVms cmdlet</span></span>
<span data-ttu-id="9a0cf-925">このエラーを回避するには、**インフラストラクチャ** フォルダーにある Config-Prereqs-AllVms.ps1 の 56 行目の「-Test:$Test」を削除します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-925">To work around this error, remove "-Test:$Test" in line 56 of Config-Prereqs-AllVms.ps1, which is found under the **Infrastructure** folder.</span></span>

### <a name="error-not-process-argument-transformation-on-parameter-test-cannot-convert-value-systemstring-to-type-systemmanagementautomationswitchparameter-when-running-the-complete-prereqs-allvms-cmdlet"></a><span data-ttu-id="9a0cf-926">エラー、「'テスト'パラメータでの引数変換を処理できません」</span><span class="sxs-lookup"><span data-stu-id="9a0cf-926">Error "Not process argument transformation on parameter 'Test'.</span></span> <span data-ttu-id="9a0cf-927">Complete-Prereqs-AllVms cmdlet 実行時、値 "System.String" を、タイプ "System.Management.Automation.SwitchParameter" に変換することはできません</span><span class="sxs-lookup"><span data-stu-id="9a0cf-927">Cannot convert value "System.String" to type "System.Management.Automation.SwitchParameter" when running the Complete-Prereqs-AllVms cmdlet</span></span>
<span data-ttu-id="9a0cf-928">このエラーを回避するには、**インフラストラクチャ** フォルダーにある Complete-Prereqs-AllVms.ps1 の 56、61、66 行目の「-Test:$Test」を削除します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-928">To work around this error, remove "-Test:$Test" in line 56, 61 and 66 of Complete-Prereqs-AllVms.ps1 which is found under the **Infrastructure** folder.</span></span>

### <a name="error-install-windowsfeature-the-request-to-add-or-remove-features-on-the-specified-server-failed-when-running-configure-prereqs-on-mrtype-and-reportservertyoe-servers"></a><span data-ttu-id="9a0cf-929">MRType および ReportServerTyoe サーバーで Configure-Prereqs を実行した際のエラー、「Install-WindowsFeature: 指定されたサーバーへの機能の追加または削除の要求に失敗しました」</span><span class="sxs-lookup"><span data-stu-id="9a0cf-929">Error "Install-WindowsFeature: The request to add or remove features on the specified server failed" when running Configure-Prereqs on MRType and ReportServerTyoe servers</span></span>
<span data-ttu-id="9a0cf-930">.NET Framework 3.5 には、MRType および ReportServerType サーバーが必要です。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-930">.NET Framework 3.5 is required in MRType and ReportServerType servers.</span></span> <span data-ttu-id="9a0cf-931">ただし、既定では .NET Framework 3.5 ソース ファイルは Windows Server 2016 インストールに含まれていません。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-931">By default, however, .NET Framework 3.5 source files aren't included in your Windows Server 2016 installation.</span></span> <span data-ttu-id="9a0cf-932">このエラーを回避するには、サーバー マネージャーによって新機能を手動で追加するときに **ソース** オプションを使用してインストールし、ソース ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-932">To work around this error, install it and specify the source files using the **source** option when you manually add new features by server manager.</span></span>

### <a name="error-msis7628-scope-names-should-be-a-valid-scope-description-name-in-ad-fs-configuration-when-running-the-publish-adfsapplicationgroup-cmdlet"></a><span data-ttu-id="9a0cf-933">Publish-ADFSApplicationGroup cmdlet を実行した際のエラー、「MSIS7628: スコープ名は AD FS コンフィギュレーションで有効なスコープ説明でなければなりません」</span><span class="sxs-lookup"><span data-stu-id="9a0cf-933">Error "MSIS7628: Scope names should be a valid Scope description name in AD FS configuration" when running the Publish-ADFSApplicationGroup cmdlet</span></span>
<span data-ttu-id="9a0cf-934">このエラーは D365FO-OP-ADFSApplicationGroup で必要とされる OpenID スコープ **allatclaims** が原因で表示されます。ただし、一部の Windows Server 2016 インストールでは表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-934">This error occurs because of an OpenID scope **allatclaims** that is required by the D365FO-OP-ADFSApplicationGroup, but it might be missing in some Windows Server 2016 installation.</span></span> <span data-ttu-id="9a0cf-935">このエラーを回避するには、AD FS Management\Service\Scope Descriptions を使用してスコープの説明 **allatclaims** を追加します。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-935">To work around this error, add the scope description **allatclaims** through AD FS Management\Service\Scope Descriptions.</span></span>

### <a name="error-admin0077-access-control-policy-does-not-exist-permit-everyone-when-running-the-publish-adfsapplicationgroup-cmdlet"></a><span data-ttu-id="9a0cf-936">Publish-ADFSApplicationGroup cmdletを実行した際のエラー、「ADMIN0077: アクセス制御ポリシーが存在しません: すべてのユーザーを許可」</span><span class="sxs-lookup"><span data-stu-id="9a0cf-936">Error "ADMIN0077: Access control policy does not exist: Permit everyone" when running the Publish-ADFSApplicationGroup cmdlet</span></span>
<span data-ttu-id="9a0cf-937">英語以外のバージョンの Windows Server 2016 と共に AD FS をインストールすると、すべてのユーザーのアクセス許可のアクセス許可ポリシーがローカル言語で作成されます。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-937">When your AD FS is installed with a non-English version of Windows Server 2016, the permit everyone access control policy is created with your local language.</span></span> <span data-ttu-id="9a0cf-938">AccessControlPolicyName パラメーターを指定することによりコマンドレットを呼び出します: .\Publish-ADFSApplicationGroup.ps1 - HostUrl 'https://ax.d365ffo.onprem.contoso.com' - AccessControlPolicyName '<Permit everyone access control policy in your language>'。</span><span class="sxs-lookup"><span data-stu-id="9a0cf-938">Invoke the cmdlet by specifying AccessControlPolicyName parameter as: .\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com' -AccessControlPolicyName '<Permit everyone access control policy in your language>'.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
