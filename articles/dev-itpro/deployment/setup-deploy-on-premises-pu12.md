---
title: "オンプレミス環境の設定と配置 (Platform update 12 以降)"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 12 以降 にオンプレミス環境を計画、設定、展開する方法について説明します。"
author: sarvanisathish
manager: AnnBe
ms.date: 11/02/2018
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
ms.search.validFrom: 2017-11-30
ms.dyn365.ops.version: Platform update 12
ms.translationtype: HT
ms.sourcegitcommit: b8fb8c963e2bba2e6fe7cb31e71a38232f1e8a54
ms.openlocfilehash: 23d636cebd9da60c3cf05a322d1bbe56cb99c5bb
ms.contentlocale: ja-jp
ms.lasthandoff: 11/02/2018

---

# <a name="set-up-and-deploy-on-premises-environments-platform-update-12-and-later"></a><span data-ttu-id="7bf0f-103">オンプレミス環境の設定と配置 (Platform update 12 以降)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-103">Set up and deploy on-premises environments (Platform update 12 and later)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bf0f-104">このトピックでは、展開を計画し、インフラストラクチャを設定し、Microsoft Dynamics 365 for Finance and Operations (オンプレミス) プラットフォーム更新プログラム 12 以降を展開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-104">This topic describes how to plan your deployment, set up the infrastructure, and deploy Microsoft Dynamics 365 for Finance and Operations (on-premises) with Platform update 12 and later.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bf0f-105">このトピックは、プラットフォーム更新プログラム 12 以降にオンプレミス環境を展開する場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-105">This topic applies only to deploying on-premises environments on Platform update 12 and later.</span></span> <span data-ttu-id="7bf0f-106">プラットフォーム更新プログラム 8 および 11 のインストールへの配置方法については、[オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 8 および 11)](setup-deploy-on-premises-pu8-pu11.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-106">For information about deploying to Platform update 8 or Platform update 11 installations, see [Set up and deploy on-premises environments (Platform updates 8 and 11)](setup-deploy-on-premises-pu8-pu11.md).</span></span> 

<span data-ttu-id="7bf0f-107">[ローカル ビジネス データ Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13595809&view=all)が利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-107">The [Local Business Data Yammer group](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13595809&view=all) is now available.</span></span> <span data-ttu-id="7bf0f-108">オンプレミス展開に関する質問またはフィードバックをそこに投稿することができます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-108">You can post questions or feedback you may have about the on-premises deployment there.</span></span>

<span data-ttu-id="7bf0f-109">このトピックの内容に関する質問やフィードバックがある場合は、このページ下の**コメント**セクションに転記してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-109">If you have questions or feedback about the content in this topic, please post them in the **Comments** section at the bottom of this page.</span></span>

## <a name="finance-and-operations-components"></a><span data-ttu-id="7bf0f-110">Finance and Operations のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-110">Finance and Operations components</span></span>

<span data-ttu-id="7bf0f-111">Finance and Operations アプリケーションは、次の 3 つの主要なコンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-111">The Finance and Operations application consists of three main components:</span></span>

- <span data-ttu-id="7bf0f-112">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-112">Application Object Server (AOS)</span></span>
- <span data-ttu-id="7bf0f-113">ビジネス インテリジェンス (BI)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-113">Business Intelligence (BI)</span></span>
- <span data-ttu-id="7bf0f-114">財務レポート/管理レポーター</span><span class="sxs-lookup"><span data-stu-id="7bf0f-114">Financial Reporting/Management Reporter</span></span>

<span data-ttu-id="7bf0f-115">これらのコンポーネントは、次のシステム ソフトウェアによって異なります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-115">These components depend on the following system software:</span></span>

- <span data-ttu-id="7bf0f-116">Microsoft Windows Server 2016 (英語 OS のインストールのみがサポートされます)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-116">Microsoft Windows Server 2016 (only English OS installations are supported)</span></span>
- <span data-ttu-id="7bf0f-117">以下の特徴を有する Microsoft SQL Server 2016 SP1:</span><span class="sxs-lookup"><span data-stu-id="7bf0f-117">Microsoft SQL Server 2016 SP1, which has the following features:</span></span>
  - <span data-ttu-id="7bf0f-118">フルテキスト インデックス検索が有効にされている。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-118">Full-text index search is enabled.</span></span>
  - <span data-ttu-id="7bf0f-119">SQL Server Reporting Services (SSRS) - これは BI 仮想マシンに配置されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-119">SQL Server Reporting Services (SSRS) - This is deployed on BI virtual machines.</span></span>
  - <span data-ttu-id="7bf0f-120">SQL Server Integration Services (SSIS) - これは AOS 仮想マシンに配置されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-120">SQL Server Integration Services (SSIS) - This is deployed on AOS virtual machines.</span></span>

    > [!WARNING]
    > <span data-ttu-id="7bf0f-121">完全なテキスト検索を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-121">Full Text Search must be enabled.</span></span>

- <span data-ttu-id="7bf0f-122">SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="7bf0f-122">SQL Server Management Studio</span></span>
- <span data-ttu-id="7bf0f-123">Standalone Microsoft Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7bf0f-123">Standalone Microsoft Azure Service Fabric</span></span>
- <span data-ttu-id="7bf0f-124">Microsoft Windows PowerShell 5.0 以降</span><span class="sxs-lookup"><span data-stu-id="7bf0f-124">Microsoft Windows PowerShell 5.0 or later</span></span>
- <span data-ttu-id="7bf0f-125">Windows Server 2016 での Active Directory Federation Services (AD FS)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-125">Active Directory Federation Services (AD FS) on Windows Server 2016</span></span>
- <span data-ttu-id="7bf0f-126">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="7bf0f-126">Domain controller</span></span>

  > [!WARNING]
  > <span data-ttu-id="7bf0f-127">ドメイン コントローラは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-127">The domain controller must be Microsoft Windows Server 2012 R2 or later and must have a domain functional level of 2012 R2 or more.</span></span>    <span data-ttu-id="7bf0f-128">ドメイン機能レベルの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-128">For more information about domain functional levels, see the following topics:</span></span>
  >   - <span data-ttu-id="7bf0f-129">[Active Directory 機能レベルとは](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-129">[What Are Active Directory Functional Levels](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)</span></span>
  >   - <span data-ttu-id="7bf0f-130">[Active Directory ドメイン サービス機能のレベルを理解する](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-130">[Understanding Active Directory Domain Services Functional Levels](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="7bf0f-131">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="7bf0f-131">Lifecycle Services</span></span>

<span data-ttu-id="7bf0f-132">Finance and Operations のビットは、Microsoft Dynamics Lifecycle Services (LCS) を通じて配布されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-132">Finance and Operations bits are distributed through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="7bf0f-133">配置する前に、[エンタープライズ契約](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) チャンネルを通じてライセンス キーを購入し、LCS でオンプレミス プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-133">Before you can deploy, you must purchase license keys through the [Enterprise Agreements](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) channel and set up an on-premises project in LCS.</span></span> <span data-ttu-id="7bf0f-134">LCS からのみ配置を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-134">Deployments can be initiated only through LCS.</span></span> <span data-ttu-id="7bf0f-135">LCS でオンプレミス プロジェクトを設定する方法の詳細については、[Lifecycle Services でのオンプレミス プロジェクトの作成](../lifecycle-services/lbd-create-lcs-on-prem-project.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-135">For more information about how to set up on-premises projects in LCS, see [Create an on-premises project in Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).</span></span>

## <a name="authentication"></a><span data-ttu-id="7bf0f-136">認証</span><span class="sxs-lookup"><span data-stu-id="7bf0f-136">Authentication</span></span>

<span data-ttu-id="7bf0f-137">オンプレミス アプリケーションは AD FS で動作します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-137">The on-premises application works with AD FS.</span></span> <span data-ttu-id="7bf0f-138">LCS と対話するには、Azure Active Directory (AAD) も設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-138">To interact with LCS, you must also configure Azure Active Directory (AAD).</span></span> <span data-ttu-id="7bf0f-139">配置を完了し、LCS ローカル エージェントを構成するには、AAD が必要です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-139">To complete the deployment and configure the LCS Local agent, you will need AAD.</span></span> <span data-ttu-id="7bf0f-140">AAD テナントがまだない場合は、AAD によって提供されるオプションのいずれかを使用して無料のものを取得できます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-140">If you do not already have an AAD tenant, you can get one for free by using one of the options provided by AAD.</span></span> <span data-ttu-id="7bf0f-141">詳細については、[Azure Active Directory テナントを取得する方法](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-howto-tenant) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-141">For more information, see [How to get an Azure Active Directory tenant](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-howto-tenant).</span></span>

## <a name="standalone-service-fabric"></a><span data-ttu-id="7bf0f-142">Standalone Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7bf0f-142">Standalone Service Fabric</span></span>

<span data-ttu-id="7bf0f-143">Finance and Operations は スタンドアロン Service Fabric を使用します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-143">Finance and Operations uses standalone Service Fabric.</span></span> <span data-ttu-id="7bf0f-144">詳細については、[Service Fabric ドキュメント](/azure/service-fabric/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-144">For more information, see the [Service Fabric documentation](/azure/service-fabric/).</span></span>

<span data-ttu-id="7bf0f-145">Finance and Operations の設定は、Service Fabric (SF) 内に一連のアプリケーションを配置します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-145">Setup of Finance and Operations will deploy a set of applications inside Service Fabric (SF).</span></span> <span data-ttu-id="7bf0f-146">展開中に、クラスター内の各ノードは、次のいずれかのノード タイプを持つように構成によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-146">During deployment, each node in the cluster will be defined via configuration to have one of the following node types:</span></span>

- <span data-ttu-id="7bf0f-147">**AOSNodeType** - アプリケーション オブジェクト サーバー (ビジネス ロジック) をホストします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-147">**AOSNodeType** - Hosts the application object server (business logic).</span></span>
- <span data-ttu-id="7bf0f-148">**OrchestratorType** - Service Fabric のプライマリ ノードとして機能し、配置およびサービスロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-148">**OrchestratorType** - Functions as Service Fabric primary nodes, and hosts deployment- and servicing logic.</span></span>
- <span data-ttu-id="7bf0f-149">**ReportServerType** - SSRS およびレポート ロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-149">**ReportServerType** - Hosts SSRS and reporting logic.</span></span>
- <span data-ttu-id="7bf0f-150">**MRType** - 管理レポート ロジックをホストします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-150">**MRType** - Hosts management reporting logic.</span></span>

## <a name="infrastructure"></a><span data-ttu-id="7bf0f-151">インフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-151">Infrastructure</span></span>

<span data-ttu-id="7bf0f-152">Finance and Operations には、非 Microsoft 仮想化プラットフォーム (具体的には VMWare) での操作に関する Microsoft の標準サポート ポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-152">Finance and Operations falls under Microsoft’s standard support policy regarding operation on non-Microsoft virtualization platforms – specifically VMWare.</span></span> <span data-ttu-id="7bf0f-153">詳細については、[Microsoft ソフトウェアのサポート ポリシー](https://support.microsoft.com/en-us/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-153">For more information, read [Support policy for Microsoft software](https://support.microsoft.com/en-us/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw).</span></span> <span data-ttu-id="7bf0f-154">つまり、この環境では製品をサポートしますが、問題の調査を依頼された場合、仮想化プラットフォームのない状態または Microsoft 仮想化プラットフォームで問題を再現するようまずお客様に依頼する場合があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-154">In short, we support our products in this environment, but if we are asked to investigate an issue, we may ask the customer to first reproduce the problem without the virtualization platform or on the Microsoft virtualization platform.</span></span>

<span data-ttu-id="7bf0f-155">VMWare を使用している場合は、次の Web ページに記載されている修正プログラムを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-155">If you are using VMWare, you must implement the fixes that are documented on the following web pages:</span></span>
- [<span data-ttu-id="7bf0f-156">仮想マシンをハードウェア バージョン 11 にアップグレード後、ネットワーク依存ワークロードのパフォーマンスが低下する (2129176)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-156">After upgrading a virtual machine to hardware version 11, network dependent workloads experience performance degradation (2129176)</span></span>](https://kb.vmware.com/s/article/2129176)
- [<span data-ttu-id="7bf0f-157">vmxnet3 仮想アダプターのいくつかの問題</span><span class="sxs-lookup"><span data-stu-id="7bf0f-157">Several issues with vmxnet3 virtual adapter</span></span>](https://vinfrastructure.it/2016/05/several-issues-vmxnet3-virtual-adapter)

 > [!WARNING]
 > <span data-ttu-id="7bf0f-158">Azure を含む、任意のパブリック クラウド インフラストラクチャでサポートされていない、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-158">On-premises deployments of Microsoft Dynamics 365 for Finance and Operations are not supported on any public cloud infrastructure, including Azure.</span></span>

<span data-ttu-id="7bf0f-159">ハードウェア構成には、次のコンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-159">The hardware configuration includes the following components:</span></span>

- <span data-ttu-id="7bf0f-160">Windows Server 2016 仮想マシン (VM) に基づく Standalone Service Fabric クラスター</span><span class="sxs-lookup"><span data-stu-id="7bf0f-160">Standalone Service Fabric cluster that is based on Windows Server 2016 virtual machines (VMs)</span></span>
- <span data-ttu-id="7bf0f-161">Microsoft SQL Server (Clustered SQL と Always-On の両方がサポートされています)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-161">Microsoft SQL Server (both Clustered SQL and Always-On are supported)</span></span>
- <span data-ttu-id="7bf0f-162">認証のための AD FS</span><span class="sxs-lookup"><span data-stu-id="7bf0f-162">AD FS for authentication</span></span>
- <span data-ttu-id="7bf0f-163">ストレージ用の Server Message Block (SMB) バージョン 3 のファイル共有</span><span class="sxs-lookup"><span data-stu-id="7bf0f-163">Server Message Block (SMB) version 3 file share for storage</span></span>
- <span data-ttu-id="7bf0f-164">オプション: Microsoft Office Server 2017</span><span class="sxs-lookup"><span data-stu-id="7bf0f-164">Optional: Microsoft Office Server 2017</span></span>

<span data-ttu-id="7bf0f-165">詳細については、[システム要件](../../fin-and-ops/get-started/system-requirements-on-prem.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-165">For more information, see [System requirements](../../fin-and-ops/get-started/system-requirements-on-prem.md).</span></span>

### <a name="hardware-layout"></a><span data-ttu-id="7bf0f-166">ハードウェア レイアウト</span><span class="sxs-lookup"><span data-stu-id="7bf0f-166">Hardware layout</span></span>

<span data-ttu-id="7bf0f-167">[オンプレミス環境のハードウェア サイジング](../../fin-and-ops/get-started/hardware-sizing-on-premises-environments.md) で推奨されるサイジングに基づいて、インフラストラクチャと Service Fabric クラスターを計画します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-167">Plan your infrastructure and Service Fabric cluster based on the recommended sizing in [Hardware sizing for on-premises environments](../../fin-and-ops/get-started/hardware-sizing-on-premises-environments.md).</span></span> <span data-ttu-id="7bf0f-168">Service Fabric クラスターを計画する方法の詳細については、[Service Fabric のスタンドアロン クラスター展開の計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-168">For more information about how to plan the Service Fabric cluster, see [Plan and prepare your Service Fabric standalone cluster deployment](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

<span data-ttu-id="7bf0f-169">次のテーブルは、ハードウェア レイアウトの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-169">The following table shows an example of a hardware layout.</span></span> <span data-ttu-id="7bf0f-170">この例は、設定を説明するためにこのトピック全体で使用されています。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-170">This example is used throughout this topic to illustrate the setup.</span></span> <span data-ttu-id="7bf0f-171">次の手順で指定されているマシン名と IP アドレスを、ご使用の環境のマシンの名前と IP アドレスに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-171">You will need to replace the machine names and IP addresses given in the following instructions with the names and IP addresses for the machines in your environment.</span></span>

> [!NOTE]
> <span data-ttu-id="7bf0f-172">Service Fabric クラスターのプライマリ ノードには、少なくとも 3 つのノードが必要です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-172">The Primary node of the Service Fabric cluster must have at least three nodes.</span></span> <span data-ttu-id="7bf0f-173">この例では **OrchestratorType** を主要なノード タイプとして指定します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-173">In this example, **OrchestratorType** is designated as the Primary node type.</span></span>

| <span data-ttu-id="7bf0f-174">マシンの目的</span><span class="sxs-lookup"><span data-stu-id="7bf0f-174">Machine purpose</span></span>          | <span data-ttu-id="7bf0f-175">SF ノード タイプ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-175">SF Node type</span></span>     | <span data-ttu-id="7bf0f-176">コンピューター名</span><span class="sxs-lookup"><span data-stu-id="7bf0f-176">Machine name</span></span>    | <span data-ttu-id="7bf0f-177">IP アドレス</span><span class="sxs-lookup"><span data-stu-id="7bf0f-177">IP address</span></span>    |
|--------------------------|------------------|-----------------|---------------|
| <span data-ttu-id="7bf0f-178">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="7bf0f-178">Domain controller</span></span>        |                  | <span data-ttu-id="7bf0f-179">DAX7SQLAODC1</span><span class="sxs-lookup"><span data-stu-id="7bf0f-179">DAX7SQLAODC1</span></span>    | <span data-ttu-id="7bf0f-180">10.179.108.2</span><span class="sxs-lookup"><span data-stu-id="7bf0f-180">10.179.108.2</span></span>  |
| <span data-ttu-id="7bf0f-181">AD FS</span><span class="sxs-lookup"><span data-stu-id="7bf0f-181">AD FS</span></span>                    |                  | <span data-ttu-id="7bf0f-182">DAX7SQLAOADFS1</span><span class="sxs-lookup"><span data-stu-id="7bf0f-182">DAX7SQLAOADFS1</span></span>  | <span data-ttu-id="7bf0f-183">10.179.108.3</span><span class="sxs-lookup"><span data-stu-id="7bf0f-183">10.179.108.3</span></span>  |
| <span data-ttu-id="7bf0f-184">ファイル サーバー</span><span class="sxs-lookup"><span data-stu-id="7bf0f-184">File server</span></span>              |                  | <span data-ttu-id="7bf0f-185">DAX7SQLAOFILE1</span><span class="sxs-lookup"><span data-stu-id="7bf0f-185">DAX7SQLAOFILE1</span></span>  | <span data-ttu-id="7bf0f-186">10.179.108.4</span><span class="sxs-lookup"><span data-stu-id="7bf0f-186">10.179.108.4</span></span>  |
| <span data-ttu-id="7bf0f-187">SQL Always-On クラスター</span><span class="sxs-lookup"><span data-stu-id="7bf0f-187">SQL Always-On cluster</span></span>    |                  | <span data-ttu-id="7bf0f-188">DAX7SQLAOSQLA01</span><span class="sxs-lookup"><span data-stu-id="7bf0f-188">DAX7SQLAOSQLA01</span></span> | <span data-ttu-id="7bf0f-189">10.179.108.5</span><span class="sxs-lookup"><span data-stu-id="7bf0f-189">10.179.108.5</span></span>  |
|                          |                  | <span data-ttu-id="7bf0f-190">DAX7SQLAOSQLA02</span><span class="sxs-lookup"><span data-stu-id="7bf0f-190">DAX7SQLAOSQLA02</span></span> | <span data-ttu-id="7bf0f-191">10.179.108.6</span><span class="sxs-lookup"><span data-stu-id="7bf0f-191">10.179.108.6</span></span>  |
|                          |                  | <span data-ttu-id="7bf0f-192">DAX7SQLAOSQLA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-192">DAX7SQLAOSQLA</span></span>   | <span data-ttu-id="7bf0f-193">10.179.108.9</span><span class="sxs-lookup"><span data-stu-id="7bf0f-193">10.179.108.9</span></span>  |
| <span data-ttu-id="7bf0f-194">クライアント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-194">Client</span></span>                   |                  | <span data-ttu-id="7bf0f-195">SQLAOCLIENT1</span><span class="sxs-lookup"><span data-stu-id="7bf0f-195">SQLAOCLIENT1</span></span>    | <span data-ttu-id="7bf0f-196">10.179.108.11</span><span class="sxs-lookup"><span data-stu-id="7bf0f-196">10.179.108.11</span></span> |
| <span data-ttu-id="7bf0f-197">AOS 1</span><span class="sxs-lookup"><span data-stu-id="7bf0f-197">AOS 1</span></span>                    | <span data-ttu-id="7bf0f-198">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="7bf0f-198">AOSNodeType</span></span>      | <span data-ttu-id="7bf0f-199">SQLAOSF1AOS1</span><span class="sxs-lookup"><span data-stu-id="7bf0f-199">SQLAOSF1AOS1</span></span>    | <span data-ttu-id="7bf0f-200">10.179.108.12</span><span class="sxs-lookup"><span data-stu-id="7bf0f-200">10.179.108.12</span></span> |
| <span data-ttu-id="7bf0f-201">AOS 2</span><span class="sxs-lookup"><span data-stu-id="7bf0f-201">AOS 2</span></span>                    | <span data-ttu-id="7bf0f-202">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="7bf0f-202">AOSNodeType</span></span>      | <span data-ttu-id="7bf0f-203">SQLAOSF1AOS2</span><span class="sxs-lookup"><span data-stu-id="7bf0f-203">SQLAOSF1AOS2</span></span>    | <span data-ttu-id="7bf0f-204">10.179.108.13</span><span class="sxs-lookup"><span data-stu-id="7bf0f-204">10.179.108.13</span></span> |
| <span data-ttu-id="7bf0f-205">AOS 3</span><span class="sxs-lookup"><span data-stu-id="7bf0f-205">AOS 3</span></span>                    | <span data-ttu-id="7bf0f-206">AOSNodeType</span><span class="sxs-lookup"><span data-stu-id="7bf0f-206">AOSNodeType</span></span>      | <span data-ttu-id="7bf0f-207">SQLAOSF1AOS3</span><span class="sxs-lookup"><span data-stu-id="7bf0f-207">SQLAOSF1AOS3</span></span>    | <span data-ttu-id="7bf0f-208">10.179.108.14</span><span class="sxs-lookup"><span data-stu-id="7bf0f-208">10.179.108.14</span></span> |
| <span data-ttu-id="7bf0f-209">オーケストレータ 1</span><span class="sxs-lookup"><span data-stu-id="7bf0f-209">Orchestrator 1</span></span>           | <span data-ttu-id="7bf0f-210">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="7bf0f-210">OrchestratorType</span></span> | <span data-ttu-id="7bf0f-211">SQLAOSF1ORCH1</span><span class="sxs-lookup"><span data-stu-id="7bf0f-211">SQLAOSF1ORCH1</span></span>   | <span data-ttu-id="7bf0f-212">10.179.108.15</span><span class="sxs-lookup"><span data-stu-id="7bf0f-212">10.179.108.15</span></span> |
| <span data-ttu-id="7bf0f-213">オーケストレータ 2</span><span class="sxs-lookup"><span data-stu-id="7bf0f-213">Orchestrator 2</span></span>           | <span data-ttu-id="7bf0f-214">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="7bf0f-214">OrchestratorType</span></span> | <span data-ttu-id="7bf0f-215">SQLAOSF1ORCH2</span><span class="sxs-lookup"><span data-stu-id="7bf0f-215">SQLAOSF1ORCH2</span></span>   | <span data-ttu-id="7bf0f-216">10.179.108.16</span><span class="sxs-lookup"><span data-stu-id="7bf0f-216">10.179.108.16</span></span> |
| <span data-ttu-id="7bf0f-217">オーケストレータ 3</span><span class="sxs-lookup"><span data-stu-id="7bf0f-217">Orchestrator 3</span></span>           | <span data-ttu-id="7bf0f-218">OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="7bf0f-218">OrchestratorType</span></span> | <span data-ttu-id="7bf0f-219">SQLAOSF1ORCH3</span><span class="sxs-lookup"><span data-stu-id="7bf0f-219">SQLAOSF1ORCH3</span></span>   | <span data-ttu-id="7bf0f-220">10.179.108.17</span><span class="sxs-lookup"><span data-stu-id="7bf0f-220">10.179.108.17</span></span> |
| <span data-ttu-id="7bf0f-221">Management Reporter ノード</span><span class="sxs-lookup"><span data-stu-id="7bf0f-221">Management Reporter node</span></span> | <span data-ttu-id="7bf0f-222">MRType</span><span class="sxs-lookup"><span data-stu-id="7bf0f-222">MRType</span></span>           | <span data-ttu-id="7bf0f-223">SQLAOSMR1</span><span class="sxs-lookup"><span data-stu-id="7bf0f-223">SQLAOSMR1</span></span>       | <span data-ttu-id="7bf0f-224">10.179.108.18</span><span class="sxs-lookup"><span data-stu-id="7bf0f-224">10.179.108.18</span></span> |
| <span data-ttu-id="7bf0f-225">SSRS ノード</span><span class="sxs-lookup"><span data-stu-id="7bf0f-225">SSRS node</span></span>                | <span data-ttu-id="7bf0f-226">ReportServerType</span><span class="sxs-lookup"><span data-stu-id="7bf0f-226">ReportServerType</span></span> | <span data-ttu-id="7bf0f-227">SQLAOSFBIN1</span><span class="sxs-lookup"><span data-stu-id="7bf0f-227">SQLAOSFBIN1</span></span>     | <span data-ttu-id="7bf0f-228">10.179.108.10</span><span class="sxs-lookup"><span data-stu-id="7bf0f-228">10.179.108.10</span></span> |

## <a name="setup"></a><span data-ttu-id="7bf0f-229">段取り</span><span class="sxs-lookup"><span data-stu-id="7bf0f-229">Setup</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7bf0f-230">前提条件</span><span class="sxs-lookup"><span data-stu-id="7bf0f-230">Prerequisites</span></span>

<span data-ttu-id="7bf0f-231">セットアップを開始する前に、次の前提条件が満たされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-231">Before you start the setup, the following prerequisites must be in place.</span></span> <span data-ttu-id="7bf0f-232">これらの前提条件の設定は、このドキュメントの範囲外です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-232">The setup of these prerequisites is out of scope for this document.</span></span>

- <span data-ttu-id="7bf0f-233">Active Directory Domain Services (AD DS) は、ネットワークにインストールして構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-233">Active Directory Domain Services (AD DS) must be installed and configured in your network.</span></span>
- <span data-ttu-id="7bf0f-234">AD FS は、展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-234">AD FS must be deployed.</span></span>
- <span data-ttu-id="7bf0f-235">SQL Server 2016 SP1 は SSRS コンピューターにインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-235">SQL Server 2016 SP1 must be installed on the SSRS machines.</span></span>
- <span data-ttu-id="7bf0f-236">SQL Server Reporting Services 2016 は、SSRS コンピューターに**ネイティブ** モードでインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-236">SQL Server Reporting Services 2016 must be installed in **Native** mode on the SSRS machines.</span></span>

<span data-ttu-id="7bf0f-237">次の必須ソフトウェアは、LCS からダウンロードされたインフラストラクチャ セットアップ スクリプトによって VM にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-237">The following prerequisite software is installed on the VMs by the infrastructure setup scripts downloaded from LCS.</span></span>

| <span data-ttu-id="7bf0f-238">ノード タイプ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-238">Node type</span></span> | <span data-ttu-id="7bf0f-239">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-239">Component</span></span> | <span data-ttu-id="7bf0f-240">詳細情報</span><span class="sxs-lookup"><span data-stu-id="7bf0f-240">Details</span></span> |
|-----------|-----------|---------|
| <span data-ttu-id="7bf0f-241">AOS</span><span class="sxs-lookup"><span data-stu-id="7bf0f-241">AOS</span></span>       | <span data-ttu-id="7bf0f-242">SNAC – ODBC ドライバー 13</span><span class="sxs-lookup"><span data-stu-id="7bf0f-242">SNAC – ODBC driver 13</span></span> | <https://www.microsoft.com/en-us/download/details.aspx?id=53339> |
| <span data-ttu-id="7bf0f-243">AOS</span><span class="sxs-lookup"><span data-stu-id="7bf0f-243">AOS</span></span>       | <span data-ttu-id="7bf0f-244">SNAC – ODBC ドライバー 17</span><span class="sxs-lookup"><span data-stu-id="7bf0f-244">SNAC – ODBC driver 17</span></span> | <span data-ttu-id="7bf0f-245">このドライバーは、PU15 以上へのアップグレードに必要です。<https://www.microsoft.com/en-us/download/details.aspx?id=56567></span><span class="sxs-lookup"><span data-stu-id="7bf0f-245">This driver is needed for upgrading to PU15 or higher: <https://www.microsoft.com/en-us/download/details.aspx?id=56567></span></span> |
| <span data-ttu-id="7bf0f-246">AOS</span><span class="sxs-lookup"><span data-stu-id="7bf0f-246">AOS</span></span>       | <span data-ttu-id="7bf0f-247">Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-247">The Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="7bf0f-248">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-248">**Windows Features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="7bf0f-249">AOS</span><span class="sxs-lookup"><span data-stu-id="7bf0f-249">AOS</span></span>       | <span data-ttu-id="7bf0f-250">Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-250">The Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="7bf0f-251">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="7bf0f-251">**Windows Features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="7bf0f-252">AOS</span><span class="sxs-lookup"><span data-stu-id="7bf0f-252">AOS</span></span>       | <span data-ttu-id="7bf0f-253">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-253">Internet Information Services (IIS)</span></span> | <span data-ttu-id="7bf0f-254">**Windows の機能:** WAS、WAS-Process-Model、WAS-NET-Environment、WAS-Config-APIs、Web-Server、Web-WebServer、Web-Security、Web-Filtering、Web-App-Dev、Web-Net-Ext、Web-Mgmt-Tools、Web-Mgmt-Console</span><span class="sxs-lookup"><span data-stu-id="7bf0f-254">**Windows Features:** WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs, Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console</span></span> |
| <span data-ttu-id="7bf0f-255">AOS</span><span class="sxs-lookup"><span data-stu-id="7bf0f-255">AOS</span></span>       | <span data-ttu-id="7bf0f-256">SQL Server Management Studio 17.2</span><span class="sxs-lookup"><span data-stu-id="7bf0f-256">SQL Server Management Studio 17.2</span></span> | <https://go.microsoft.com/fwlink/?linkid=854085> |
| <span data-ttu-id="7bf0f-257">AOS</span><span class="sxs-lookup"><span data-stu-id="7bf0f-257">AOS</span></span>       | <span data-ttu-id="7bf0f-258">Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-258">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</span></span> | <https://support.microsoft.com/en-us/help/3179560> |
| <span data-ttu-id="7bf0f-259">AOS</span><span class="sxs-lookup"><span data-stu-id="7bf0f-259">AOS</span></span>       | <span data-ttu-id="7bf0f-260">Microsoft Access データベース エンジン 2010 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-260">Microsoft Access Database Engine 2010 Redistributable</span></span> | <https://www.microsoft.com/en-us/download/details.aspx?id=13255> |
| <span data-ttu-id="7bf0f-261">BI</span><span class="sxs-lookup"><span data-stu-id="7bf0f-261">BI</span></span>        | <span data-ttu-id="7bf0f-262">.NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-262">.NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="7bf0f-263">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-263">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="7bf0f-264">BI</span><span class="sxs-lookup"><span data-stu-id="7bf0f-264">BI</span></span>        | <span data-ttu-id="7bf0f-265">.NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-265">.NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="7bf0f-266">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="7bf0f-266">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="7bf0f-267">BI</span><span class="sxs-lookup"><span data-stu-id="7bf0f-267">BI</span></span>        | <span data-ttu-id="7bf0f-268">SQL Server Management Studio 17.2</span><span class="sxs-lookup"><span data-stu-id="7bf0f-268">SQL Server Management Studio 17.2</span></span> | <https://go.microsoft.com/fwlink/?linkid=854085> |
| <span data-ttu-id="7bf0f-269">MR</span><span class="sxs-lookup"><span data-stu-id="7bf0f-269">MR</span></span>        | <span data-ttu-id="7bf0f-270">.NET Framework version 2.0–3.5 (CLR 2.0)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-270">.NET Framework version 2.0–3.5 (CLR 2.0)</span></span> | <span data-ttu-id="7bf0f-271">**Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-271">**Windows features:** NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</span></span> |
| <span data-ttu-id="7bf0f-272">MR</span><span class="sxs-lookup"><span data-stu-id="7bf0f-272">MR</span></span>        | <span data-ttu-id="7bf0f-273">.NET Framework version 4.0–4.6 (CLR 4.0)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-273">.NET Framework version 4.0–4.6 (CLR 4.0)</span></span> | <span data-ttu-id="7bf0f-274">**Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</span><span class="sxs-lookup"><span data-stu-id="7bf0f-274">**Windows features:** NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</span></span> |
| <span data-ttu-id="7bf0f-275">MR</span><span class="sxs-lookup"><span data-stu-id="7bf0f-275">MR</span></span>        | <span data-ttu-id="7bf0f-276">Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-276">Visual C++ Redistributable Packages for Visual Studio 2013</span></span> | <https://support.microsoft.com/en-us/help/3179560> |

### <a name="overview"></a><span data-ttu-id="7bf0f-277">概要</span><span class="sxs-lookup"><span data-stu-id="7bf0f-277">Overview</span></span>

<span data-ttu-id="7bf0f-278">Finance and Operations のインフラストラクチャを設定するには、以下の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-278">The following steps must be completed to set up the infrastructure for Finance and Operations.</span></span> <span data-ttu-id="7bf0f-279">開始する前にすべての手順を読むと、セットアップを計画しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-279">Reading all the steps before you begin will make it easier to plan your setup.</span></span>

1. [<span data-ttu-id="7bf0f-280">ドメイン名と DNS ゾーンの計画</span><span class="sxs-lookup"><span data-stu-id="7bf0f-280">Plan your domain name and DNS zones</span></span>](#plandomain)
2. [<span data-ttu-id="7bf0f-281">証明書の計画と取得</span><span class="sxs-lookup"><span data-stu-id="7bf0f-281">Plan and acquire your certificates</span></span>](#plancert)
3. [<span data-ttu-id="7bf0f-282">ユーザーとサービス アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="7bf0f-282">Plan your users and service accounts</span></span>](#plansvcacct)
4. [<span data-ttu-id="7bf0f-283">DNS ゾーンの作成と A レコードの追加</span><span class="sxs-lookup"><span data-stu-id="7bf0f-283">Create DNS zones, and add A records</span></span>](#createdns)
5. [<span data-ttu-id="7bf0f-284">VM のドメインへの参加</span><span class="sxs-lookup"><span data-stu-id="7bf0f-284">Join VMs to the domain</span></span>](#joindomain)
6. [<span data-ttu-id="7bf0f-285">LCS からセットアップ スクリプトのダウンロード</span><span class="sxs-lookup"><span data-stu-id="7bf0f-285">Download setup scripts from LCS</span></span>](#downloadscripts)
7. [<span data-ttu-id="7bf0f-286">コンフィギュレーションの記述</span><span class="sxs-lookup"><span data-stu-id="7bf0f-286">Describe your configuration</span></span>](#describeconfig)
8. [<span data-ttu-id="7bf0f-287">証明書の構成</span><span class="sxs-lookup"><span data-stu-id="7bf0f-287">Configure certificates</span></span>](#configurecert)
9. [<span data-ttu-id="7bf0f-288">VM を設定する</span><span class="sxs-lookup"><span data-stu-id="7bf0f-288">Setup VMs</span></span>](#setupvms)
10. [<span data-ttu-id="7bf0f-289">スタンドアロン Service Fabric クラスターの設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-289">Set up a standalone Service Fabric cluster</span></span>](#setupsfcluster)
11. [<span data-ttu-id="7bf0f-290">テナント用 LCS 接続の構成</span><span class="sxs-lookup"><span data-stu-id="7bf0f-290">Configure LCS connectivity for the tenant</span></span>](#configurelcs)
12. [<span data-ttu-id="7bf0f-291">ファイル ストレージの設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-291">Set up file storage</span></span>](#setupfile)
13. [<span data-ttu-id="7bf0f-292">SQL Server の設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-292">Set up SQL Server</span></span>](#setupsql)
14. [<span data-ttu-id="7bf0f-293">データベースを構成する</span><span class="sxs-lookup"><span data-stu-id="7bf0f-293">Configure the databases</span></span>](#configuredb)
15. [<span data-ttu-id="7bf0f-294">資格情報の暗号化</span><span class="sxs-lookup"><span data-stu-id="7bf0f-294">Encrypt credentials</span></span>](#encryptcred)
16. [<span data-ttu-id="7bf0f-295">資産除去債務 (SSIS) の設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-295">Set up SSIS</span></span>](#setupssis)
17. [<span data-ttu-id="7bf0f-296">資産除去債務 (SSRS) の設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-296">Set up SSRS</span></span>](#setupssrs)
18. [<span data-ttu-id="7bf0f-297">AD FS のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7bf0f-297">Configure AD FS</span></span>](#configureadfs)
19. [<span data-ttu-id="7bf0f-298">コネクタを構成し、オンプレミスのローカル エージェントをインストールする</span><span class="sxs-lookup"><span data-stu-id="7bf0f-298">Configure a connector and install an on-premises local agent</span></span>](#configureconnector)
20. [<span data-ttu-id="7bf0f-299">リモート処理が使用されたら、CredSSP を終了処理する</span><span class="sxs-lookup"><span data-stu-id="7bf0f-299">Tear down CredSSP, if remoting was used</span></span>](#teardowncredssp)
21. [<span data-ttu-id="7bf0f-300">LCS から Finance and Operations (オンプレミス) 環境を配置する</span><span class="sxs-lookup"><span data-stu-id="7bf0f-300">Deploy your Finance and Operations (on-premises) environment from LCS</span></span>](#deploy)
22. [<span data-ttu-id="7bf0f-301">Finance and Operations (オンプレミス) 環境に接続する</span><span class="sxs-lookup"><span data-stu-id="7bf0f-301">Connect to your Finance and Operations (on-premises) environment</span></span>](#connect)

### <a name="plandomain"></a> <span data-ttu-id="7bf0f-302">1. ドメイン名と DNS ゾーンの計画</span><span class="sxs-lookup"><span data-stu-id="7bf0f-302">1. Plan your domain name and DNS zones</span></span>

<span data-ttu-id="7bf0f-303">AOS のプロダクション インストールには、公的に登録されたドメイン名を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-303">We recommend that you use a publicly registered domain name for your production installation of AOS.</span></span> <span data-ttu-id="7bf0f-304">このようにして、外部アクセスが必要な場合は、ネットワークの外部からインストールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-304">In that way, the installation can be accessed outside the network, if outside access is required.</span></span>

<span data-ttu-id="7bf0f-305">たとえば、会社のドメインが contoso.com の場合、Finance and Operations (オンプレミス) は d365ffo.onprem.contoso.com であり、ホスト名は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-305">For example, if your company's domain is contoso.com, your zone for Finance and Operations (on-premises) might be d365ffo.onprem.contoso.com, and the host names might be as follows:</span></span>

- <span data-ttu-id="7bf0f-306">AOS の機械の場合 ax.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7bf0f-306">ax.d365ffo.onprem.contoso.com for AOS machines</span></span>
- <span data-ttu-id="7bf0f-307">Service Fabric クラスターの場合 sf.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7bf0f-307">sf.d365ffo.onprem.contoso.com for the Service Fabric cluster</span></span>

### <a name="plancert"></a> <span data-ttu-id="7bf0f-308">2. 証明書の計画と取得</span><span class="sxs-lookup"><span data-stu-id="7bf0f-308">2. Plan and acquire your certificates</span></span>

<span data-ttu-id="7bf0f-309">Service Fabric クラスターと展開されているすべてのアプリケーションを保護するには、Secure Sockets Layer (SSL) 証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-309">Secure Sockets Layer (SSL) certificates are required in order to secure a Service Fabric cluster and all the applications that are deployed.</span></span> <span data-ttu-id="7bf0f-310">プロダクションとサンドボックスのワークロードについては、[DigiCert](https://www.digicert.com/ssl-certificate/)、[Comodo](https://ssl.comodo.com/)、[Symantec](https://www.websecurity.symantec.com/ssl-certificate)、[GoDaddy](https://www.godaddy.com/web-security/ssl-certificate)、または [GlobalSign](https://www.globalsign.com/en/ssl/) などの認証局から証明書を取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-310">For your production and sandbox workloads, we recommend that you acquire certificates from a certificate authority (CA) such as [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate), or [GlobalSign](https://www.globalsign.com/en/ssl/).</span></span> <span data-ttu-id="7bf0f-311">ドメインが [Active Directory 証明書サービス](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS) で設定されている場合は、AD CS を介して証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-311">If your domain is set up with [Active Directory Certificate Services](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS), you can create the certificates through AD CS.</span></span> <span data-ttu-id="7bf0f-312">証明書ごとに、プライベート キーが作成されたキーの交換を含める必要があり、個人情報交換 (.pfx) ファイルにエクスポート可能な必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-312">Each certificate must contain a private key that was created for key exchange, and it must be exportable to a Personal Information Exchange (.pfx) file.</span></span>

<span data-ttu-id="7bf0f-313">自己署名証明書は、テスト目的でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-313">Self-signed certificates can be used only for testing purposes.</span></span> <span data-ttu-id="7bf0f-314">便宜上、LCS で提供されるセットアップ スクリプトには、自己署名証明書を生成およびエクスポートするスクリプトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-314">For convenience, the setup scripts provided in LCS include scripts that generate and export self-signed certificates.</span></span> <span data-ttu-id="7bf0f-315">自己署名スクリプトを使用している場合は、後の手順で作成スクリプトを実行するように指示されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-315">If you are using self-signed scripts, you will be instructed to run the creation scripts in later steps.</span></span> <span data-ttu-id="7bf0f-316">先に述べたように、これらの証明書はテスト目的でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-316">As we've mentioned, these certificates can be used for testing purposes only.</span></span>

| <span data-ttu-id="7bf0f-317">目的</span><span class="sxs-lookup"><span data-stu-id="7bf0f-317">Purpose</span></span>                                      | <span data-ttu-id="7bf0f-318">説明</span><span class="sxs-lookup"><span data-stu-id="7bf0f-318">Explanation</span></span> | <span data-ttu-id="7bf0f-319">追加条件</span><span class="sxs-lookup"><span data-stu-id="7bf0f-319">Additional requirements</span></span> |
|----------------------------------------------|-------------|-------------------------|
| <span data-ttu-id="7bf0f-320">SQL Server SSL 証明書</span><span class="sxs-lookup"><span data-stu-id="7bf0f-320">SQL Server SSL certificate</span></span>                   | <span data-ttu-id="7bf0f-321">この証明書は、ネットワーク上の SQL Server インスタンスとクライアント アプリケーションの間で転送されるデータを暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-321">This certificate is used to encrypt data that is transmitted across a network between an instance of SQL Server and a client application.</span></span> | <span data-ttu-id="7bf0f-322">証明書の場合、ドメイン名は、SQL Server のインスタンスまたはリスナーの完全修飾ドメイン名 (FQDN) と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-322">The domain name of the certificate should match the fully-qualified domain name (FQDN) of the SQL Server instance or listener.</span></span> <span data-ttu-id="7bf0f-323">たとえば、SQL のリスナーが DAX7SQLAOSQLA のコンピューターにホストされている場合、証明書の DNS 名は、DAX7SQLAOSQLA.contoso.com です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-323">For example, if the SQL listener is hosted on the machine DAX7SQLAOSQLA, the certificate's DNS name is DAX7SQLAOSQLA.contoso.com.</span></span> |
| <span data-ttu-id="7bf0f-324">Service Fabric Server 証明書</span><span class="sxs-lookup"><span data-stu-id="7bf0f-324">Service Fabric Server certificate</span></span>            | <p><span data-ttu-id="7bf0f-325">この証明書を使用して、Service Fabric ノード間のノードからノードの通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-325">This certificate is used to help secure the node-to-node communication between the Service Fabric nodes.</span></span></p> <p> <span data-ttu-id="7bf0f-326">この証明書は、クラスターに接続するクライアントに提示されるサーバー証明書としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-326">This certificate is also used as the Server certificate that is presented to the client that connects to the cluster.</span></span></p> | <span data-ttu-id="7bf0f-327">ドメインの SSL ワイルドカード証明書を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-327">You can use the SSL wild card certificate of your domain.</span></span> <span data-ttu-id="7bf0f-328">たとえば、\*.contoso.com です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-328">For example, \*.contoso.com.</span></span> <span data-ttu-id="7bf0f-329">**注記:** ワイルド カード証明書は、発行先となるドメインの最初のレベル サブドメインのみをセキュリティ保護できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-329">**Note:** The wild card certificate allows you to secure only the first level subdomain of the domain to which it is issued.</span></span><p><span data-ttu-id="7bf0f-330">この例では、Service Fabric ドメインが sf.d365ffo.onprem.contoso.com であるため、証明書にサブジェクト代替名 (SAN) としてこれを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-330">In this example, because your service fabric domain is sf.d365ffo.onprem.contoso.com, you must include this as a Subject Alternative Name (SAN) in the certificate.</span></span> <span data-ttu-id="7bf0f-331">証明機関と連携して、追加の SAN を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-331">You will need to work with your certificate authority to acquire the additional SANs.</span></span></p> |
| <span data-ttu-id="7bf0f-332">Service Fabric Client 証明書</span><span class="sxs-lookup"><span data-stu-id="7bf0f-332">Service Fabric Client certificate</span></span>            | <span data-ttu-id="7bf0f-333">この証明書は、クライアントによって Service Fabric クラスターを表示および管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-333">This certificate is used by clients to view and manage the Service Fabric cluster.</span></span> | |
| <span data-ttu-id="7bf0f-334">証明書の暗号化</span><span class="sxs-lookup"><span data-stu-id="7bf0f-334">Encipherment Certificate</span></span>                     | <span data-ttu-id="7bf0f-335">この証明書は、SQL Server パスワードとユーザー アカウントのパスワードなどの重要な情報を暗号化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-335">This certificate is used to encrypt sensitive information such as the SQL Server password and user account passwords.</span></span>  | <p> <span data-ttu-id="7bf0f-336">証明書は、プロバイダー **Microsoft Enhanced Cryptographic Provider v1.0** を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-336">The certificate must be created by using the provider **Microsoft Enhanced Cryptographic Provider v1.0**.</span></span> </p><p><span data-ttu-id="7bf0f-337">証明書キーの使用にはデータ暗号化 (10) が含まれている必要があり、サーバー認証またはクライアント認証は含めないでください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-337">The certificate key usage must include Data Encipherment (10) and should not include Server authentication or Client authentication.</span></span></p><p><span data-ttu-id="7bf0f-338">詳細については、[Service Fabric アプリケーションでの機密情報の管理](/azure/service-fabric/service-fabric-application-secret-management) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-338">For more information, see [Managing secrets in Service Fabric applications](/azure/service-fabric/service-fabric-application-secret-management).</span></span></p> |
| <span data-ttu-id="7bf0f-339">AOS SSL 証明書</span><span class="sxs-lookup"><span data-stu-id="7bf0f-339">AOS SSL Certificate</span></span>                          | <p><span data-ttu-id="7bf0f-340">この証明書は、AOS Web サイトに接続するクライアントに提示されるサーバー証明書としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-340">This certificate is used as the Server certificate that is presented to the client for the AOS website.</span></span> <span data-ttu-id="7bf0f-341">また、WCF (Windows Communication Foundation) / SOAP (Simple Object Access Protocol) 証明書を有効にするためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-341">It's also used to enable Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP) certificates.</span></span></p><p><span data-ttu-id="7bf0f-342">Service Fabric サーバー証明書として使用するのと同じワイルドカード証明書を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-342">You can use the same wild card certificate that you used as the Service Fabric Server certificate.</span></span></p> | <p><span data-ttu-id="7bf0f-343">この例では、ドメイン名 ax.d365ffo.onprem.contoso.com を、Service Fabric Server 証明書としてサブジェクト代替名 (SAN) に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-343">In this example, the domain name ax.d365ffo.onprem.contoso.com must be added to the Subject Alternative Name (SAN) as in the Service  Fabric Server certificate.</span></span></p> |
| <span data-ttu-id="7bf0f-344">セッション認証証明書</span><span class="sxs-lookup"><span data-stu-id="7bf0f-344">Session Authentication certificate</span></span>           | <span data-ttu-id="7bf0f-345">この証明書は、AOS がユーザーのセッション情報を保護するために使用します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-345">This certificate is used by AOS to help secure a user's session information.</span></span> | <span data-ttu-id="7bf0f-346">この証明書は、LCS からの展開時に使用されるファイル共有証明書です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-346">This certificate is also the File Share certificate that will used at the time of deployment from LCS.</span></span> |
| <span data-ttu-id="7bf0f-347">データの暗号化証明書</span><span class="sxs-lookup"><span data-stu-id="7bf0f-347">Data Encryption certificate</span></span>                  | <span data-ttu-id="7bf0f-348">これらの証明書は、機密情報を暗号化するために AOS によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-348">This certificate is used by the AOS to encrypt sensitive information.</span></span>  | <span data-ttu-id="7bf0f-349">これはプロバイダー **Microsoft Enhanced RSA および AES Cryptographic Provider** を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-349">This must be created using the provider **Microsoft Enhanced RSA and AES Cryptographic Provider**.</span></span> |
| <span data-ttu-id="7bf0f-350">データ署名の証明書</span><span class="sxs-lookup"><span data-stu-id="7bf0f-350">Data Signing certificate</span></span>                     | <span data-ttu-id="7bf0f-351">これらの証明書は、機密情報を暗号化するために AOS によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-351">This certificate is used by AOS to encrypt sensitive information.</span></span>  | <span data-ttu-id="7bf0f-352">これは、データ暗号化証明書とは別のもので、プロバイダー**Microsoft の拡張された RSA および AES 暗号化プロバイダー**を使用して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-352">This is separate from the Data Encryption certificate and must be created using the provider **Microsoft Enhanced RSA and AES Cryptographic Provider**.</span></span> |
| <span data-ttu-id="7bf0f-353">財務報告クライアント証明書</span><span class="sxs-lookup"><span data-stu-id="7bf0f-353">Financial Reporting client certificate</span></span>       | <span data-ttu-id="7bf0f-354">この証明書は、財務報告サービスと AOS 間の通信を保護するのに役立ちます。   この証明書を使用して、財務報告サービスと AOS 間の通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-354">This certificate is used to help secure the communication between the Financial Reporting services and the AOS.</span></span> |  |
| <span data-ttu-id="7bf0f-355">報告証明書</span><span class="sxs-lookup"><span data-stu-id="7bf0f-355">Reporting certificate</span></span>                        | <span data-ttu-id="7bf0f-356">この証明書を使用して、SSRS と AOS 間の通信を保護します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-356">This certificate is used to help secure the communication between SSRS and the AOS.</span></span>| <span data-ttu-id="7bf0f-357">**財務報告クライアント証明書を再利用しないでください。**</span><span class="sxs-lookup"><span data-stu-id="7bf0f-357">**Do not reuse the Financial Reporting Client certificate.**</span></span> |
| <span data-ttu-id="7bf0f-358">オンプレミス ローカル エージェント証明書</span><span class="sxs-lookup"><span data-stu-id="7bf0f-358">On-Premise local agent certificate</span></span>           | <p><span data-ttu-id="7bf0f-359">この証明書は、オンプレミスと LCS でホストされているローカル エージェント間の通信を保護するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-359">This certificate is used to help secure the communication between a local agent that is hosted on-premises and on LCS.</span></span></p><p><span data-ttu-id="7bf0f-360">この証明書を使用すると、Azure AD テナントに代わってローカル エージェントが動作し、LCS と通信して配置を編成および監視することができます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-360">This certificate enables the local agent to act on behalf of your Azure AD tenant, and to communicate with LCS to orchestrate and monitor deployments.</span></span></p><p><span data-ttu-id="7bf0f-361">**注記:** テナントにはオンプレミス ローカル エージェント証明書が 1 つだけ必要です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-361">**Note:** Only 1 on-premise local agent certificate is needed for a tenant.</span></span></p> | |

<span data-ttu-id="7bf0f-362">以下は、AOS SSL 証明書と組み合わせた Service Fabric Server 証明書の例です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-362">The following is an example of a Service Fabric Server certificate combined with an AOS SSL certificate.</span></span>

#### <a name="subject-name"></a><span data-ttu-id="7bf0f-363">件名</span><span class="sxs-lookup"><span data-stu-id="7bf0f-363">Subject name</span></span>

```
CN = *.d365ffo.onprem.contoso.com
```

#### <a name="subject-alternative-names"></a><span data-ttu-id="7bf0f-364">件名の代替名</span><span class="sxs-lookup"><span data-stu-id="7bf0f-364">Subject alternative names</span></span>

```
DNS Name=ax.d365ffo.onprem.contoso.com
DNS Name=sf.d365ffo.onprem.contoso.com
DNS Name=*.d365ffo.onprem.contoso.com
```

### <a name="plansvcacct"></a> <span data-ttu-id="7bf0f-365">3. ユーザーとサービス アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="7bf0f-365">3. Plan your users and service accounts</span></span>

<span data-ttu-id="7bf0f-366">Finance and Operations (オンプレミス) を機能させるために、いくつかのユーザー アカウントまたはサービス アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-366">You must create several user or service accounts for Finance and Operations (on-premises) to work.</span></span> <span data-ttu-id="7bf0f-367">サービス アカウントの管理グループ (gMSAs)、ドメイン アカウント、および SQL アカウントの組み合わせを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-367">You must create a combination of group managed service accounts (gMSAs), domain accounts, and SQL accounts.</span></span> <span data-ttu-id="7bf0f-368">次の表は、このトピックで使用されるユーザー アカウント、その目的、および名前の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-368">The following table shows the user accounts, their purpose, and example names that will be used in this topic.</span></span>

| <span data-ttu-id="7bf0f-369">ユーザー アカウント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-369">User account</span></span>                                            | <span data-ttu-id="7bf0f-370">種類</span><span class="sxs-lookup"><span data-stu-id="7bf0f-370">Type</span></span>           | <span data-ttu-id="7bf0f-371">目的</span><span class="sxs-lookup"><span data-stu-id="7bf0f-371">Purpose</span></span> | <span data-ttu-id="7bf0f-372">ユーザー名</span><span class="sxs-lookup"><span data-stu-id="7bf0f-372">User name</span></span> |
|---------------------------------------------------------|----------------|---------|-----------|
| <span data-ttu-id="7bf0f-373">財務レポート アプリケーション サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-373">Financial Reporting Application Service Account</span></span>         | <span data-ttu-id="7bf0f-374">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-374">gMSA</span></span>           |         | <span data-ttu-id="7bf0f-375">Contoso\\svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-375">Contoso\\svc-FRAS$</span></span> |
| <span data-ttu-id="7bf0f-376">財務レポート プロセス サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-376">Financial Reporting Process Service Account</span></span>             | <span data-ttu-id="7bf0f-377">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-377">gMSA</span></span>           |         | <span data-ttu-id="7bf0f-378">Contoso\\svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-378">Contoso\\svc-FRPS$</span></span> |
| <span data-ttu-id="7bf0f-379">財務レポート クリック ワンス デザイナー サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-379">Financial Reporting Click Once Designer Service Account</span></span> | <span data-ttu-id="7bf0f-380">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-380">gMSA</span></span>           |         | <span data-ttu-id="7bf0f-381">Contoso\\svc-FRCO$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-381">Contoso\\svc-FRCO$</span></span> |
| <span data-ttu-id="7bf0f-382">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-382">AOS Service Account</span></span>                                     | <span data-ttu-id="7bf0f-383">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-383">gMSA</span></span>           | <span data-ttu-id="7bf0f-384">このユーザーは、将来校正するために作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-384">This user should be created for future-proofing.</span></span> <span data-ttu-id="7bf0f-385">今後のリリースでは、AOS を gMSA と連携させる予定です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-385">We plan to enable AOS to work with the gMSA in upcoming releases.</span></span> <span data-ttu-id="7bf0f-386">このユーザーを設定時に作成することで、gMSA へのシームレスな移行を確実にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-386">By creating this user at the time of setup, you will help to ensure a seamless transition to the gMSA.</span></span> | <span data-ttu-id="7bf0f-387">Contoso\\svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-387">Contoso\\svc-AXSF$</span></span> |
| <span data-ttu-id="7bf0f-388">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-388">AOS Service Account</span></span>                                     | <span data-ttu-id="7bf0f-389">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-389">Domain account</span></span> | <span data-ttu-id="7bf0f-390">AOS は、一般提供 (GA) リリースでこのユーザーを使用します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-390">AOS uses this user in the general availability (GA) release.</span></span> | <span data-ttu-id="7bf0f-391">Contoso\\AXServiceUser</span><span class="sxs-lookup"><span data-stu-id="7bf0f-391">Contoso\\AXServiceUser</span></span> |
| <span data-ttu-id="7bf0f-392">AOS SQL DB 管理者ユーザー</span><span class="sxs-lookup"><span data-stu-id="7bf0f-392">AOS SQL DB Admin user</span></span>                                   | <span data-ttu-id="7bf0f-393">SQL ユーザー</span><span class="sxs-lookup"><span data-stu-id="7bf0f-393">SQL user</span></span>       | <span data-ttu-id="7bf0f-394">Finance and Operations は、このユーザーを使用して SQL\* を認証します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-394">Finance and Operations uses this user to authenticate with SQL\*.</span></span> <span data-ttu-id="7bf0f-395">このユーザーも、今後のリリースで gMSA ユーザーに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-395">This user will also be replaced by the gMSA user in upcoming releases.</span></span> | <span data-ttu-id="7bf0f-396">AXDBAdmin</span><span class="sxs-lookup"><span data-stu-id="7bf0f-396">AXDBAdmin</span></span> |
| <span data-ttu-id="7bf0f-397">ローカル配置エージェント サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-397">Local Deployment Agent Service Account</span></span>                  | <span data-ttu-id="7bf0f-398">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-398">gMSA</span></span>           | <span data-ttu-id="7bf0f-399">このアカウントは、ローカル エージェントによって、さまざまなノードでの展開を調整するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-399">This account is used by the local agent to orchestrate the deployment on various nodes.</span></span> | <span data-ttu-id="7bf0f-400">Contoso\\Svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-400">Contoso\\Svc-LocalAgent$</span></span> |

<span data-ttu-id="7bf0f-401">\* SQL 認証の SQL ユーザー名とパスワードは、暗号化されてファイル共有に格納されているため、保護されています。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-401">\* The SQL user name and password for SQL authentication are secured because they are encrypted and stored in the file share.</span></span>

### <a name="createdns"></a> <span data-ttu-id="7bf0f-402">4. DNS ゾーンの作成とレコードの追加</span><span class="sxs-lookup"><span data-stu-id="7bf0f-402">4. Create DNS zones and add A records</span></span>

<span data-ttu-id="7bf0f-403">DNS は AD DS と統合されており、ネットワーク内のリソースを整理、管理、検索することができます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-403">DNS is integrated with AD DS, and lets you organize, manage, and find resources in a network.</span></span> <span data-ttu-id="7bf0f-404">次の指示では、AOS ホスト名と Service Fabric クラスターの DNS 前方参照ゾーンと A レコードを作成する手順を示します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-404">The following instructions provide steps to create a DNS forward lookup zone and A records for the AOS host name and Service Fabric cluster.</span></span> <span data-ttu-id="7bf0f-405">この設定例では、DNS ゾーン名は d365ffo.onprem.contoso.com で、A レコード/ホスト名は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-405">In this example setup, the DNS zone name is d365ffo.onprem.contoso.com, and the A records/host names are as follows:</span></span>

- <span data-ttu-id="7bf0f-406">AOS の機械の場合 **ax**.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7bf0f-406">**ax**.d365ffo.onprem.contoso.com for AOS machines</span></span>
- <span data-ttu-id="7bf0f-407">Service Fabric クラスターの場合 **sf**.d365ffo.onprem.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7bf0f-407">**sf**.d365ffo.onprem.contoso.com for the Service Fabric cluster</span></span>

#### <a name="add-a-dns-zone"></a><span data-ttu-id="7bf0f-408">DNS ゾーンの追加</span><span class="sxs-lookup"><span data-stu-id="7bf0f-408">Add a DNS zone</span></span>

<span data-ttu-id="7bf0f-409">DNS ゾーンを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-409">Use the following procedure to add a DNS zone.</span></span>

1. <span data-ttu-id="7bf0f-410">ドメイン コントローラー コンピューターにログインして **スタート** を選択し、**dnsmgmt.msc** と入力して **dnsmgmt (DNS)** アプリケーションを選択することにより DNS マネージャーを起動します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-410">Sign in to the domain controller machine, select **Start**, and start DNS Manager by typing **dnsmgmt.msc** and selecting the **dnsmgmt (DNS)** application.</span></span>
2. <span data-ttu-id="7bf0f-411">コンソール ツリーでドメイン コントローラー名を右クリックし、**新しいゾーン** \> **次へ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-411">Right-click the domain controller name in the console tree, and then select **New Zone** \> **Next**.</span></span>
3. <span data-ttu-id="7bf0f-412">**プライマリ ゾーン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-412">Select **Primary Zone**.</span></span>
4. <span data-ttu-id="7bf0f-413">**Active Directory にゾーンを保存 (DNS サーバーが書き込み可能なドメイン コントローラーの場合にのみ使用可能)** のチェック ボックスが選択されたままの状態で、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-413">Leave the **Store the zone in Active Directory (available only if the DNS Server is a writeable domain controller** check box selected, and then select **Next**.</span></span>
5. <span data-ttu-id="7bf0f-414">**このドメイン (Contoso.com) のドメイン コントローラーで実行されているすべての DNS サーバーに対して** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-414">Select **To all DNS Servers running on Domain Controllers in this domain: Contoso.com**, and then select **Next**.</span></span>
6. <span data-ttu-id="7bf0f-415">**前方参照ゾーン** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-415">Select **Forward Lookup Zone**, and then select **Next**.</span></span>
7. <span data-ttu-id="7bf0f-416">設定するゾーン名を入力し、**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-416">Enter the zone name for your setup, and then select **Next**.</span></span> <span data-ttu-id="7bf0f-417">たとえば、**d365ffo.onprem.contoso.com** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-417">For example, enter **d365ffo.onprem.contoso.com**.</span></span>
8. <span data-ttu-id="7bf0f-418">**動的更新を許可しない** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-418">Select **Do not allow dynamic updates**, and then select **Next**.</span></span>
9. <span data-ttu-id="7bf0f-419">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-419">Select **Finish**.</span></span>

#### <a name="set-up-an-a-record-for-aos"></a><span data-ttu-id="7bf0f-420">AOS の A レコードを設定する</span><span class="sxs-lookup"><span data-stu-id="7bf0f-420">Set up an A record for AOS</span></span>

<span data-ttu-id="7bf0f-421">新しい DNS ゾーンで、**AOSNodeType** タイプの Service Fabric クラスター ノード**ごと**に、**ax.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-421">In the new DNS zone, create one A record that is named **ax.d365ffo.onprem.contoso.com** for **each** Service Fabric cluster node of the **AOSNodeType** type.</span></span> <span data-ttu-id="7bf0f-422">他のノード タイプの A レコードは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-422">Don't create A records for the other node types.</span></span>

1. <span data-ttu-id="7bf0f-423">DNS マネージャーの**前方参照ゾーン**フォルダーで、新しく作成したゾーンを検索します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-423">Find the newly created zone under the **Forward Lookup Zones** folder in DNS Manager.</span></span>
2. <span data-ttu-id="7bf0f-424">新しいゾーンを右クリックして、**新しいホスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-424">Right-click the new zone, and then select **New Host**.</span></span>
3. <span data-ttu-id="7bf0f-425">Service Fabric ノードの 名前および IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-425">Enter the name and IP address of the Service Fabric node.</span></span> <span data-ttu-id="7bf0f-426">(たとえば、**ax** を名前として入力し、**10.179.108.12** を IP アドレスとして入力します。) **ホストの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-426">(For example, enter **ax** as the name and enter **10.179.108.12** as the IP address.) Select **Add Host**.</span></span>
4. <span data-ttu-id="7bf0f-427">どのチェック ボックスもオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-427">Do not select either check box.</span></span>
5. <span data-ttu-id="7bf0f-428">各 AOS ノードで手順 1 ～ 4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-428">Repeat steps 1-4 for each AOS node.</span></span>

#### <a name="set-up-an-a-record-for-the-orchestrator"></a><span data-ttu-id="7bf0f-429">Orchestrator の A レコードを設定する</span><span class="sxs-lookup"><span data-stu-id="7bf0f-429">Set up an A record for the orchestrator</span></span>

<span data-ttu-id="7bf0f-430">新しい DNS ゾーンで、**OrchestratorType** タイプの Service Fabric クラスター ノード**ごと**に、**sf.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-430">In the new DNS zone, create an A record that is named **sf.d365ffo.onprem.contoso.com** for **each** Service Fabric cluster node of the **OrchestratorType** type.</span></span> <span data-ttu-id="7bf0f-431">他のノード タイプの A レコードは作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-431">Don't create A records for the other node types.</span></span>

1. <span data-ttu-id="7bf0f-432">新しいゾーンを右クリックして、**新しいホスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-432">Right-click the new zone, and then select **New Host**.</span></span>
2. <span data-ttu-id="7bf0f-433">Service Fabric ノードの 名前および IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-433">Enter the name and IP address of the Service Fabric node.</span></span> <span data-ttu-id="7bf0f-434">(たとえば、**sf** を名前としてを入力し、**10.179.108.15** を IP アドレスとして入力します。) **ホストの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-434">(For example, enter **sf** as the name and enter **10.179.108.15** as the IP address.) Select **Add Host**.</span></span>
3. <span data-ttu-id="7bf0f-435">どのチェック ボックスもオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-435">Do not select either check box.</span></span>
4. <span data-ttu-id="7bf0f-436">各オーケストレータ ノードを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-436">Repeat for each Orchestrator node.</span></span>

### <a name="joindomain"></a> <span data-ttu-id="7bf0f-437">5. VM のドメインへの参加</span><span class="sxs-lookup"><span data-stu-id="7bf0f-437">5. Join VMs to the domain</span></span>

<span data-ttu-id="7bf0f-438">各 VM をドメインに参加させるには、[コンピューターをドメインに参加させる](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/join-a-computer-to-a-domain)のドキュメントの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-438">Join each VM to the domain by completing the steps in the [Join a Computer to a Domain](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/join-a-computer-to-a-domain) document.</span></span> <span data-ttu-id="7bf0f-439">または、次の Windows PowerShell スクリプトを使用します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-439">Alternatively, use the following Windows PowerShell script.</span></span>

```powershell
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
```

> [!IMPORTANT]
> <span data-ttu-id="7bf0f-440">ドメインにそれらを結合させた後、VM を再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-440">You must restart the VMs after you join them to the domain.</span></span>

### <a name="downloadscripts"></a> <span data-ttu-id="7bf0f-441">6. LCS からのセットアップ スクリプトのダウンロード</span><span class="sxs-lookup"><span data-stu-id="7bf0f-441">6. Download setup scripts from LCS</span></span>

<span data-ttu-id="7bf0f-442">セットアップ エクスペリエンスを向上させるためのスクリプトをいくつか紹介しています。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-442">We have provided several scripts to help improve the setup experience.</span></span> <span data-ttu-id="7bf0f-443">LCS からセットアップ スクリプトをダウンロードするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-443">Follow these steps to download the setup scripts from LCS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bf0f-444">スクリプトは、オンプレミス インフラストラクチャと同じドメイン内のコンピューターから実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-444">The scripts must be executed from a computer in the same domain that the on-premises infrastructure is in.</span></span>

1. <span data-ttu-id="7bf0f-445">[LCS](https://lcs.dynamics.com/v2) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-445">Sign in to [LCS](https://lcs.dynamics.com/v2).</span></span>
2. <span data-ttu-id="7bf0f-446">ダッシュボードで、**共有アセット ライブラリ**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-446">On the dashboard, select the **Shared asset library** tile.</span></span>
3. <span data-ttu-id="7bf0f-447">**モデル**タブの、グリッドで、**Dynamics 365 for Operations オンプレミス - 配置スクリプト**行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-447">On the **Model** tab, in the grid, select the **Dynamics 365 for Operations on-premises - Deployment scripts** row.</span></span>
4. <span data-ttu-id="7bf0f-448">**バージョン** を選択し、スクリプトの zip ファイルの最新版をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-448">Select **Versions**, and then download the latest version of the zip file for the scripts.</span></span>
   >[!Note] 
   > <span data-ttu-id="7bf0f-449">プラットフォーム更新プログラム 8 またはプラットフォーム更新プログラム 11 の以前のバージョンが必要な場合は、バージョン 1 をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-449">If you need the older version for Platform update 8 or Platform update 11, download version 1.</span></span>
5. <span data-ttu-id="7bf0f-450">zip ファイルを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-450">Right-click the zip file, and then select **Properties**.</span></span> <span data-ttu-id="7bf0f-451">ダイアログ ボックスで、**ブロック解除**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-451">In the dialog box, select the **Unblock** check box.</span></span>
6. <span data-ttu-id="7bf0f-452">ZIP ファイルをスクリプトの実行に使用するマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-452">Copy the zip file to the machine that will be used to execute the scripts.</span></span>
7. <span data-ttu-id="7bf0f-453">**infrastructure** という名前のフォルダーにファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-453">Unzip the files into a folder that is named **infrastructure**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bf0f-454">このフォルダーの ConfigTemplate.xml ファイルにすべての編集を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-454">Ensure all edits are made to the ConfigTemplate.xml file in this folder.</span></span>

### <a name="describeconfig"></a> <span data-ttu-id="7bf0f-455">7. コンフィギュレーションの記述</span><span class="sxs-lookup"><span data-stu-id="7bf0f-455">7. Describe your configuration</span></span>

<span data-ttu-id="7bf0f-456">インフラストラクチャの設定 スクリプトは、次のコンフィギュレーション ファイルを使用して設定を実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-456">The infrastructure setup scripts use the following configuration files to drive the setup.</span></span>
- <span data-ttu-id="7bf0f-457">infrastructure\ConfigTemplate.xml</span><span class="sxs-lookup"><span data-stu-id="7bf0f-457">infrastructure\ConfigTemplate.xml</span></span>
- <span data-ttu-id="7bf0f-458">infrastructure\D365FO-OP\NodeTopologyDefintion.xml</span><span class="sxs-lookup"><span data-stu-id="7bf0f-458">infrastructure\D365FO-OP\NodeTopologyDefintion.xml</span></span>
- <span data-ttu-id="7bf0f-459">infrastructure\D365FO-OP\DatabaseTopologyDefintion.xml</span><span class="sxs-lookup"><span data-stu-id="7bf0f-459">infrastructure\D365FO-OP\DatabaseTopologyDefintion.xml</span></span>

>[!NOTE]
><span data-ttu-id="7bf0f-460">セットアップ スクリプトが正しく機能するには、環境に基づいてコンフィギュレーション ファイルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-460">Configuration files must be updated based on your environment for the setup scripts to work correctly.</span></span> <span data-ttu-id="7bf0f-461">これらのファイルは、設定に基づいて適切なコンピューター名、IP アドレス、サービス アカウントおよびドメインで更新してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-461">Be sure to update these files with the proper computer names, IP addresses, service accounts, and domain based on your setup.</span></span>

<span data-ttu-id="7bf0f-462">**infrastructure\ConfigTemplate.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-462">**infrastructure\ConfigTemplate.xml** describes:</span></span>
- <span data-ttu-id="7bf0f-463">アプリケーションが動作するために必要なサービス アカウント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-463">Service Accounts that are needed for the application to operate</span></span>
- <span data-ttu-id="7bf0f-464">通信を保護するために必要な証明書</span><span class="sxs-lookup"><span data-stu-id="7bf0f-464">Certificates necessary for securing communications</span></span>
- <span data-ttu-id="7bf0f-465">データベース コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7bf0f-465">Database configuration</span></span>
- <span data-ttu-id="7bf0f-466">Service Fabric クラスター構成</span><span class="sxs-lookup"><span data-stu-id="7bf0f-466">Service Fabric cluster configuration</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7bf0f-467">Service Fabric クラスタをコンフィギュレーションする際に OrchestratorType の 3 つのフォールト ドメインがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-467">Make sure that there are three fault domains for OrchestratorType when you configure Service Fabric cluster.</span></span> <span data-ttu-id="7bf0f-468">Service Fabric クラスタをコンフィギュレーションする際、単一のマシンにノードの 1 つのタイプのみが配置されるよう確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-468">Make sure that no more than one type of node is deployed in a single machine when you configure Service Fabric cluster.</span></span>

<span data-ttu-id="7bf0f-469">各 Service Fabric ノード タイプについて、**infrastructure\D365FO-OP\NodeTopologyDefinition.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-469">For each Service Fabric node type, **infrastructure\D365FO-OP\NodeTopologyDefinition.xml** describes:</span></span>

- <span data-ttu-id="7bf0f-470">各ノード タイプとアプリケーション、ドメインとサービス アカウント、および証明書間のマッピング。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-470">The mapping between each node type and the application, domain and service accounts, and certificates.</span></span>
- <span data-ttu-id="7bf0f-471">UAC を有効にするかどうか。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-471">Whether to enable the UAC.</span></span>
- <span data-ttu-id="7bf0f-472">Windows の機能とシステム ソフトウェアの前提条件。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-472">Prerequisites for Windows features and system software.</span></span>
- <span data-ttu-id="7bf0f-473">厳密な名前の検証を有効にするかどうか。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-473">Whether strong name validation should be enabled.</span></span>
- <span data-ttu-id="7bf0f-474">ファイアウォール ポートのリストを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-474">List of firewall ports to be opened.</span></span>

<span data-ttu-id="7bf0f-475">各データベースについて、**infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml** で説明します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-475">For each database, **infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml** describes:</span></span>

- <span data-ttu-id="7bf0f-476">データベース設定。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-476">The database settings.</span></span>
- <span data-ttu-id="7bf0f-477">ユーザーとロール間のマッピング。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-477">The mappings between users and roles.</span></span>

#### <a name="create-gmsa-and-domain-user-accounts"></a><span data-ttu-id="7bf0f-478">gMSA およびドメイン ユーザー アカウントを作成する</span><span class="sxs-lookup"><span data-stu-id="7bf0f-478">Create gMSA and domain user accounts</span></span>

1. <span data-ttu-id="7bf0f-479">**インフラストラクチャ** フォルダーに展開したインフラストラクチャ スクリプトがあるマシンに移動します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-479">Navigate to the machine that has the unzipped infrastructure scripts in the **infrastructure** folder.</span></span>
2. <span data-ttu-id="7bf0f-480">**インフラストラクチャ**フォルダーをドメイン コントローラー マシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-480">Copy the **infrastructure** folder to the domain controller machine.</span></span>
3. <span data-ttu-id="7bf0f-481">管理者特権モードで Windows PowerShell を起動し、ディレクトリを **infrastructure** フォルダーに変更して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-481">Start Windows PowerShell in elevated mode, change the directory to the **infrastructure** folder, and run the following commands.</span></span>
    > [!IMPORTANT]
    > <span data-ttu-id="7bf0f-482">次のスクリプトは、ドメイン ユーザー AxServiceUser を作成しません。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-482">The following script doesn't create a domain user AxServiceUser for you.</span></span> <span data-ttu-id="7bf0f-483">ユーザーが作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-483">You must create it yourself.</span></span>

    ```powershell
    Import-Module .\D365FO-OP\D365FO-OP.psd1
    New-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```
    


4. <span data-ttu-id="7bf0f-484">AOS サービス アカウントの **Contoso\svc-AXSF$** および **Contoso\AXServiceUser** をすべての AOS マシンのローカル 管理者グループへ追加します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-484">Add the AOS Service Accounts, **Contoso\svc-AXSF$** and **Contoso\AXServiceUser** to the local administrators group for all AOS machines.</span></span> <span data-ttu-id="7bf0f-485">詳細については、「[ローカル グループへのメンバーの追加](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-485">For more information, see [Add a member to local group](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx).</span></span>

5. <span data-ttu-id="7bf0f-486">アカウントまたはマシンを変更する必要がある場合は、元の **インフラストラクチャ** フォルダーの ConfigTemplate.xml ファイルを更新し、このマシンにコピーしてから次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-486">If you must make changes to accounts or machines, update the ConfigTemplate.xml file in the original **infrastructure** folder, copy it to this machine and then run the following script.</span></span>

    ```powershell
    Update-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="configurecert"></a> <span data-ttu-id="7bf0f-487">8. 証明書のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7bf0f-487">8. Configure certificates</span></span>

1. <span data-ttu-id="7bf0f-488">**インフラストラクチャ** フォルダーがあるマシンに移動します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-488">Navigate to the machine that has the **infrastructure** folder.</span></span>
2. <span data-ttu-id="7bf0f-489">自己署名証明書を生成する必要がある場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-489">If you must generate self-signed certificates, run the following command.</span></span> <span data-ttu-id="7bf0f-490">スクリプトは証明書を作成し、それらをコンピューターの「CurrentUser\My certificate store」に格納し、XML ファイルのサムプリントを更新します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-490">The script will create the certificates, put them in the CurrentUser\My certificate store on the machine, and update the thumbprints in the XML file.</span></span>

    ```powershell
    # Create self-signed certs
    .\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    <span data-ttu-id="7bf0f-491">証明書を再利用する必要があるため、証明書を生成する必要がない場合は、**generateSelfSignedCert** タグを **false** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-491">If you must reuse any certificates and therefore don't have to generate certificates for them, set the **generateSelfSignedCert** tag to **false**.</span></span>

3. <span data-ttu-id="7bf0f-492">既に生成されている SSL 証明書を使用している場合は、証明書生成をスキップし、configTemplate.xml ファイルの拇印を更新します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-492">If you're using SSL certificates that were already generated, skip the Certificate generation and update the thumbprints in the configTemplate.xml file.</span></span> <span data-ttu-id="7bf0f-493">証明書は CurrentUser\My ストアにインストールする必要があり、その秘密キーはエクスポート可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-493">The certificates need to be installed in the CurrentUser\My store and their private keys must be exportable.</span></span>

> [!WARNING]
> <span data-ttu-id="7bf0f-494">存在する場合に特定するのが難しい先頭の印刷不可能な特殊文字のため、証明書マネージャーは拇印をコピーするために使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-494">Because of a leading not-printable special character, which is difficult to determine when present, the cert manager should not be used to copy thumbprints.</span></span> <span data-ttu-id="7bf0f-495">印刷できない特殊文字がある場合、**X509 証明書が無効です**というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-495">If the not-printable special character is present, you will get the error, **X509 certificate not valid**.</span></span> <span data-ttu-id="7bf0f-496">拇印を取得するには、PowerShell コマンドの結果を参照するか、PowerShell で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-496">To retrieve the thumbprints, see results from PowerShell commands or run the following commands in PowerShell.</span></span>
> ```powershell
> dir cert:\CurrentUser\My
> dir cert:\LocalMachine\My
> dir cert:\LocalMachine\Root
> ```

4. <span data-ttu-id="7bf0f-497">各証明書の **ProtectTo** でユーザーまたはグループのセミコロンで区切られた一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-497">Specify a semi-colon separated list of users or groups in the **ProtectTo** tag for each certificate.</span></span> <span data-ttu-id="7bf0f-498">**ProtectTo** タグで指定された Active Directory ユーザーとグループのみに、スクリプトを使用してエクスポートされる証明書をインポートするアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-498">Only Active directory users and groups specified in the **ProtectTo** tag will have permissions to import the certificates that are exported using the scripts.</span></span> <span data-ttu-id="7bf0f-499">エクスポートした証明書を保護するため、スクリプトによりパスワードがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-499">Passwords are not supported by the script to protect the exported certificates</span></span>

5. <span data-ttu-id="7bf0f-500">証明書を .pfx ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-500">Export the certificates into .pfx files.</span></span>

    ```powershell
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will be written to infrastructure\Certs folder.
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="setupvms"></a> <span data-ttu-id="7bf0f-501">9. VM の設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-501">9. Setup VMs</span></span>
1. <span data-ttu-id="7bf0f-502">各 VM で実行する必要があるスクリプトをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-502">Export the scripts that must be run on each VM.</span></span>

    ```powershell
    # Exports the script files to be execute on each VM into a directory VMs\<VMName>.
    .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. <span data-ttu-id="7bf0f-503">次の Microsoft Windows Installers (MSIs) を全ての VMs でアクセス可能なファイル共有にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-503">Download the following Microsoft Windows Installers (MSIs) into a file share that is accessible by all VMs.</span></span>

| <span data-ttu-id="7bf0f-504">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="7bf0f-504">Component</span></span> | <span data-ttu-id="7bf0f-505">リンクのダウンロード</span><span class="sxs-lookup"><span data-stu-id="7bf0f-505">Download link</span></span> |
|-----------|---------------|
| <span data-ttu-id="7bf0f-506">SNAC – ODBC ドライバー 13</span><span class="sxs-lookup"><span data-stu-id="7bf0f-506">SNAC – ODBC driver 13</span></span> | <https://www.microsoft.com/en-us/download/details.aspx?id=53339> |
| <span data-ttu-id="7bf0f-507">SNAC – ODBC ドライバー 17</span><span class="sxs-lookup"><span data-stu-id="7bf0f-507">SNAC – ODBC driver 17</span></span> | <https://www.microsoft.com/en-us/download/details.aspx?id=56567> |
| <span data-ttu-id="7bf0f-508">Microsoft SQL Server Management Studio 17.5</span><span class="sxs-lookup"><span data-stu-id="7bf0f-508">Microsoft SQL Server Management Studio 17.5</span></span> | <https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms> |
| <span data-ttu-id="7bf0f-509">Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-509">Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</span></span> | <https://support.microsoft.com/en-us/help/3179560> |
| <span data-ttu-id="7bf0f-510">Microsoft Access データベース エンジン 2010 再頒布可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-510">Microsoft Access Database Engine 2010 Redistributable</span></span> | <https://www.microsoft.com/en-us/download/details.aspx?id=13255> |

> [!IMPORTANT]
> <span data-ttu-id="7bf0f-511">Microsoft SQL Server Management Studio の設定が、対象となるコンピューターのオペレーティング システムと同じ言語であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-511">Make sure the Microsoft SQL Server Management Studio setup is in the same language as the operating system of the target machine.</span></span>
> <span data-ttu-id="7bf0f-512">NodeTopologyDefinition.xml で定義されているインストーラー ファイルが指定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-512">Ensure the installer files are named as defined in NodeTopologyDefinition.xml.</span></span>
> <span data-ttu-id="7bf0f-513">msodbcsql.ms SSMS-Setup-\*.exe vcredist_x64.exe AccessDatabaseEngine_x64.exe</span><span class="sxs-lookup"><span data-stu-id="7bf0f-513">msodbcsql.ms SSMS-Setup-\*.exe vcredist_x64.exe AccessDatabaseEngine_x64.exe</span></span>

#### <a name="follow-these-steps-for-each-vm-or-use-remoting-from-a-single-machine"></a><span data-ttu-id="7bf0f-514">各 VM についてこれらのステップに従うか、または単一のコンピューターからリモート処理を使用します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-514">Follow these steps for each VM, or use remoting from a single machine</span></span>

> [!NOTE]
> <span data-ttu-id="7bf0f-515">次のセクションでは、複数の VM での実行が必要です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-515">The following section requires execution on multiple VMs.</span></span> <span data-ttu-id="7bf0f-516">このプロセスは、指定されたリモート処理スクリプトを使用して、1 台のマシン (`.\Export-Scripts.ps1` を実行するのと同じマシンなど) から必要なスクリプトを実行するオプションを提供することで、簡単に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-516">This process can be eased by using the supplied remoting scripts, which provide the option of running the necessary scripts from a single machine, such as the same machine used to execute `.\Export-Scripts.ps1`.</span></span> <span data-ttu-id="7bf0f-517">利用可能な場合、リモート処理スクリプトは、PowerShell セクションの「`# If Remoting`」コメントの後に宣言されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-517">The remoting scripts, when available, are declared after a "`# If Remoting`" comment in the PowerShell sections.</span></span> <span data-ttu-id="7bf0f-518">リモート処理スクリプトを使用するときは、セクションの残りのスクリプトを実行する必要はありません。そのような例については、セクションの本文を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-518">When the remoting scripts are used, you may not need to execute the remaining scripts in a section, please see the section text for cases such as that.</span></span> <span data-ttu-id="7bf0f-519">リモート処理では、[WinRM](https://msdn.microsoft.com/en-us/library/aa384426(v=vs.85).aspx) が使用され、特定のケースでは [CredSSP](https://msdn.microsoft.com/en-us/library/windows/desktop/bb931352(v=vs.85).aspx) が有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-519">Remoting uses [WinRM](https://msdn.microsoft.com/en-us/library/aa384426(v=vs.85).aspx) and requires [CredSSP](https://msdn.microsoft.com/en-us/library/windows/desktop/bb931352(v=vs.85).aspx) to be enabled in certain cases.</span></span> <span data-ttu-id="7bf0f-520">CredSSP の有効化と無効化は、実行ごとにリモート処理モジュールによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-520">The enabling and disabling of CredSSP is handled by the remoting module on a per-execution basis.</span></span> <span data-ttu-id="7bf0f-521">資格情報の盗難の形でのセキュリティ リスクをもたらすため、CredSSP が使用されていない場合に有効のままにすることはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-521">Keeping CredSSP enabled when it is not in use is not advised, as it introduces security risks in the shape of credential theft.</span></span> <span data-ttu-id="7bf0f-522">設定が完了した場合、[CredSSP を終了処理する](#teardowncredssp) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-522">See the [Tear down CredSSP](#teardowncredssp) section when you are finished setting up.</span></span>

1. <span data-ttu-id="7bf0f-523">各 infrastructure\VMs\<VMName> フォルダーのコンテンツを対応する VM にコピーし (リモート処理スクリプトが使用されている場合は、コンテンツをターゲット VM に自動的にコピーします)、次のスクリプトを管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-523">Copy the contents of each infrastructure\VMs\<VMName> folder into the corresponding VM (if remoting scripts are used, they will automatically copy the content to the target VMs), and then run the following scripts as an Administrator.</span></span>

    ```powershell
    # Install pre-req software on the VMs.

    # If Remoting, execute
    # .\Configure-PreReqs-AllVMs.ps1 -MSIFilePath <share folder path of the MSIs> -ConfigurationFilePath .\ConfigTemplate.xml

    .\Configure-PreReqs.ps1 -MSIFilePath <path of the MSIs>
    ```

    > [!IMPORTANT]
    > 1. <span data-ttu-id="7bf0f-524">再起動するように求められるたびにコンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-524">Each time you are prompted, restart the machine.</span></span> <span data-ttu-id="7bf0f-525">再起動した後、すべての前提条件がインストールされるまで、`.\Configure-PreReqs.ps1` スクリプトを再実行することを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-525">Make sure that you rerun the `.\Configure-PreReqs.ps1` script after each restart until all of the prerequisites are installed.</span></span> <span data-ttu-id="7bf0f-526">リモート処理の場合、すべてのマシンがオンラインに戻ったときに AllVM スクリプトを再実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-526">In the case of remoting, rerun the AllVMs script when all of the machines are back online.</span></span>
    > 2. <span data-ttu-id="7bf0f-527">リモート処理スクリプトを使用するときに、現在のユーザーが MSI の共有フォルダーにアクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-527">When you use the remoting script, ensure that the current user has access to the share folder of MSIs.</span></span>
    > 3. <span data-ttu-id="7bf0f-528">リモート処理スクリプトを使用するときに、ユーザーが AOSNoteType、MRType、および ReportServerType タイプのマシンにアクセスしていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-528">When you use the remoting script, ensure no user is accessing the AOSNoteType, MRType, and ReportServerType type machines.</span></span> <span data-ttu-id="7bf0f-529">それ以外の場合は、コンピューターにログオンしているユーザーが原因で、リモート処理スクリプトはコンピュータの再起動に失敗します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-529">Otherwise, the remoting script will fail to restart the computer because of the users being logged on to the computer.</span></span>

2. <span data-ttu-id="7bf0f-530">VM セットアップを完了するため、存在する場合は、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-530">Run the following scripts, if they exist, to complete the VM setup.</span></span>

    ```powershell
    # If Remoting, only execute
    # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    .\Add-GMSAOnVM.ps1
    .\Import-PfxFiles.ps1
    .\Set-CertificateAcls.ps1
    ```

3. <span data-ttu-id="7bf0f-531">次のスクリプトを実行して VM のセットアップを検証します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-531">Run the following script to validate the VM setup.</span></span>

    ```powershell
    # If Remoting, execute
    # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    .\Test-D365FOConfiguration.ps1 
    ```

> [!IMPORTANT]
> <span data-ttu-id="7bf0f-532">リモート処理を使用していた場合は、設定が完了するとクリーンアップ手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-532">If remoting was used, be sure to execute the clean up steps when the setup is complete.</span></span> <span data-ttu-id="7bf0f-533">[20. Tear down CredSSP](#teardowncredssp) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-533">See the [20. Tear down CredSSP](#teardowncredssp) section.</span></span>

### <a name="setupsfcluster"></a> <span data-ttu-id="7bf0f-534">10. スタンドアロン Service Fabric クラスターの設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-534">10. Set up a standalone Service Fabric cluster</span></span>

1. <span data-ttu-id="7bf0f-535">[Service Fabric スタンドアロン インストール パッケージ](http://go.microsoft.com/fwlink/?LinkId=730690) を使用中の Service Fabric ノードのいずれかにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-535">Download the [Service Fabric standalone installation package](http://go.microsoft.com/fwlink/?LinkId=730690) onto one of your Service Fabric nodes.</span></span> <span data-ttu-id="7bf0f-536">ZIP ファイルをダウンロードした後、 ZIP ファイルを右クリックし**プロパティ**を選択してブロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-536">After the zip file is downloaded, unblock it by right-clicking the zip file and then selecting **Properties**.</span></span> <span data-ttu-id="7bf0f-537">ダイアログ ボックスで、右下の **ブロック解除** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-537">In the dialog box, select the **Unblock** check box in the lower right.</span></span>

2. <span data-ttu-id="7bf0f-538">ZIP ファイルを Service Fabric クラスター内のいずれかのノードにコピーし、解凍します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-538">Copy the zip file to one of the nodes in the Service Fabric cluster, and unzip it.</span></span> <span data-ttu-id="7bf0f-539">**インフラストラクチャ**フォルダーが、このフォルダーにアクセスすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-539">Ensure the **infrastructure** folder has access to this folder.</span></span>

3. <span data-ttu-id="7bf0f-540">**インフラストラクチャ** フォルダーに移動し、次のコマンドを実行して Service Fabric の ClusterConfig.json ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-540">Navigate to the **infrastructure** folder and execute the following command to generate the Service Fabric ClusterConfig.json file.</span></span>

    ```powershell
   .\New-SFClusterConfig.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -TemplateConfig <ServiceFabricStandaloneInstallerPath>\ClusterConfig.X509.MultiMachine.json
    ```
4. <span data-ttu-id="7bf0f-541">クラスター コンフィギュレーションへの追加の変更は、環境に基づいて必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-541">Additional modifications to your cluster configuration may be necessary based on your environment.</span></span> <span data-ttu-id="7bf0f-542">詳細については、[手順 1B: 複数のマシンでクラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)、[X.509 証明書を使用して Windows スタンドアロン クラスターを保護する](/azure/service-fabric/service-fabric-windows-cluster-x509-security)、および[Windows Server で実行されているスタンドアロン クラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-542">For more information, see, [Step 1B: Create a multi-machine cluster](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Secure a standalone cluster on Windows using X.509 certificates](/azure/service-fabric/service-fabric-windows-cluster-x509-security), and [Create a standalone cluster running on Windows Server](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).</span></span>

5. <span data-ttu-id="7bf0f-543">生成された ClusterConfig.json ファイルを \<ServiceFabricStandaloneInstallerPath\> にコピーします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-543">Copy the generated ClusterConfig.json file to the \<ServiceFabricStandaloneInstallerPath\>.</span></span>

6. <span data-ttu-id="7bf0f-544">上位の権限を使用して Windows PowerShell で \<ServiceFabricStandaloneInstallerPath\> に移動します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-544">Navigate to the \<ServiceFabricStandaloneInstallerPath\> in Windows PowerShell by using elevated privileges.</span></span> <span data-ttu-id="7bf0f-545">次のコマンドを実行して ClusterConfig をテストします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-545">Run the following command to test ClusterConfig.</span></span>

    ```powershell
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

7. <span data-ttu-id="7bf0f-546">テストが成功した場合は、次のコマンドを実行してクラスターを展開します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-546">If the test is successful, run the following command to deploy the cluster.</span></span>

    ```powershell
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

8. <span data-ttu-id="7bf0f-547">クラスターが作成された後は、任意のクライアント マシンで Service Fabric エクスプローラーを開き、インストールを検証します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-547">After the cluster is created, open the Service Fabric explorer on any client machine to validate the installation.</span></span>

    1. <span data-ttu-id="7bf0f-548">まだインストールされていない場合、CurrentUser\\My に Service Fabric クライアント証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-548">Install the Service Fabric client certificate in CurrentUser\\My if it isn't already installed.</span></span>
    2. <span data-ttu-id="7bf0f-549">**IE 設定** \> **互換モード** に移動し、**互換モードでイントラネット サイトを表示する** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-549">Go to **IE settings** \> **Compatibility Mode**, and clear the **Display Intranet sites in compatibility mode** check box.</span></span>
    3. <span data-ttu-id="7bf0f-550">`https://sf.d365ffo.onprem.contoso.com:19080` に移動します。sf.d365ffo.onprem.contoso.com は、ゾーンで指定されている Service Fabric クラスターのホスト名です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-550">Go to `https://sf.d365ffo.onprem.contoso.com:19080`, where sf.d365ffo.onprem.contoso.com is the host name of the Service Fabric cluster that is specified in the zone.</span></span> <span data-ttu-id="7bf0f-551">DNS 名前解決が設定されていない場合は、マシンの IP アドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-551">If DNS name resolution isn't configured, use the IP address of the machine.</span></span>
    4. <span data-ttu-id="7bf0f-552">クライアントの証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-552">Select the client certificate.</span></span> <span data-ttu-id="7bf0f-553">**Service Fabric エクスプローラー** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-553">The **Service Fabric explorer** page appears.</span></span>
    5. <span data-ttu-id="7bf0f-554">すべてのノードが緑で表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-554">Verify that all nodes are appear as green.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="7bf0f-555">クライアント マシンが Windows Server 2016 のようなサーバー コンピューターである場合は、**Service Fabric エクスプローラー**ページにアクセスするときに IE のセキュリティ強化の構成をオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-555">If your client machine is a server machine like Windows Server 2016, you must turn off the IE Enhanced Security Configuration when you access the **Service Fabric explorer** page.</span></span>
    > <span data-ttu-id="7bf0f-556">ウィルス対策ソフトウェアがインストールされている場合は、[Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) ドキュメントのガイダンスに従って除外を設定してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-556">If any antivirus software is installed, ensure you set exclusion following the guidance in the [Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) documentation.</span></span>

### <a name="configurelcs"></a> <span data-ttu-id="7bf0f-557">11. テナント用 LCS 接続のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7bf0f-557">11. Configure LCS connectivity for the tenant</span></span>

<span data-ttu-id="7bf0f-558">Finance and Operations の展開とサービスは、オンプレミスのローカル エージェントを使用して LCS を通じて調整されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-558">Deployment and servicing of Finance and Operations is orchestrated through LCS by using an on-premises local agent.</span></span> <span data-ttu-id="7bf0f-559">LCS から Finance and Operations テナントへの接続を確立するには、Azure AD テナント (たとえば、Contoso.onmicrosoft.com) の代わりに動作するローカル エージェントを可能にする証明書をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-559">To establish connectivity from LCS to the Finance and Operations tenant, you must configure a certificate that enables the local agent to act on behalf on your Azure AD tenant (for example, Contoso.onmicrosoft.com).</span></span>

<span data-ttu-id="7bf0f-560">証明機関から取得したオンプレミス エージェントの証明書またはスクリプトを使用して生成した自己署名証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-560">Use the on-premises agent certificate that you acquired from a certificate authority or the self-signed certificate that you generated by using scripts.</span></span>

<span data-ttu-id="7bf0f-561">オンプレミス エージェント証明書は、テナントごとに複数のサンドボックス環境および実稼動環境で再利用できます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-561">The on-premises agent certificate can be reused across multiple sandbox and production environments per tenant.</span></span>

<span data-ttu-id="7bf0f-562">グローバル管理者ディレクトリの役割を持つユーザー アカウントだけが、LCS を承認するための証明書を追加できます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-562">Only user accounts that have the Global Administrator directory role can add certificates to authorize LCS.</span></span> <span data-ttu-id="7bf0f-563">既定では、組織の Microsoft Office 365 にサインアップする担当者が、ディレクトリのグローバル管理者です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-563">By default, the person who signs up for Microsoft Office 365 for your organization is the global administrator for the directory.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="7bf0f-564">テナントごとに証明書を正確に 1 回構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-564">You must configure the certificate exactly one time per tenant.</span></span> <span data-ttu-id="7bf0f-565">すべてのオンプレミス環境では、同じ証明書を使用して LCS に接続できます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-565">All on-premises environments can use the same certificate to connect with LCS.</span></span>
   > <span data-ttu-id="7bf0f-566">Windows Server 2016 などのサーバー コンピューターでこれを実行する場合は、IE セキュリティ強化の構成を一時的にオフに必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-566">If you run this in a server machine like Windows Server 2016, you must turn off the IE Enhanced Security Configuration temporarily.</span></span> <span data-ttu-id="7bf0f-567">そうしないと、Azure ログイン ウィンドウのコンテンツはブロックされます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-567">If you don't, the Azure login window content will be blocked.</span></span>

1. <span data-ttu-id="7bf0f-568">Azure PowerShell の最新バージョンをクライアント マシンにダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-568">Download and install the latest version of Azure PowerShell on a client machine.</span></span> <span data-ttu-id="7bf0f-569">詳細については、[Azure PowerShell のインストールおよびコンフィギュレーション](/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-569">For more information, see [Install and configure Azure PowerShell](/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).</span></span>
2. <span data-ttu-id="7bf0f-570">[顧客の Azure ポータル](https://portal.azure.com) にサインインして、グローバル管理者ディレクトリの役割があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-570">Sign in to the [customer's Azure portal](https://portal.azure.com) to verify that you have the Global Administrator directory role.</span></span>
3. <span data-ttu-id="7bf0f-571">**インフラストラクチャ**フォルダから次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-571">Run the following script from the **Infrastructure** folder.</span></span>
    ```powershell
    .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
    ```

### <a name="setupfile"></a> <span data-ttu-id="7bf0f-572">12.ファイル ストレージの設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-572">12. Set up file storage</span></span>

<span data-ttu-id="7bf0f-573">以下の SMB 3.0 ファイル共有を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-573">You must set up the following SMB 3.0 file shares:</span></span>

- <span data-ttu-id="7bf0f-574">AOS にアップロードされるユーザー ドキュメントを格納するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\aos-storage)。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-574">A file share that stores user documents that are uploaded to AOS (for example, \\\\DAX7SQLAOFILE1\\aos-storage).</span></span>
- <span data-ttu-id="7bf0f-575">デプロイメントを調整するための最新のビルド ファイルと構成ファイルを保存するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\agent)。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-575">A file share that stores the latest build and configuration files to orchestrate the deployment (for example, \\\\DAX7SQLAOFILE1\\agent).</span></span>

    > [!WARNING]
    > <span data-ttu-id="7bf0f-576">共有に入れるファイルの最大パス長を超えないように、このファイル共有パスはできるだけ短くしておいてください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-576">Keep this file share path as short as possible to avoid exceeding the maximum path length on the files that will be put in the share.</span></span>

<span data-ttu-id="7bf0f-577">SMB 3.0 を有効にする方法については、[SMB セキュリティの強化](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-577">For information about how to enable SMB 3.0, see [SMB Security Enhancements](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="7bf0f-578">セキュリティで保護されたダイアレクト ネゴシエーションでは、SMB 2.0 または 3.0 から SMB 1.0 へのダウングレードを検出または防止できません。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-578">Secure dialect negotiation can't detect or prevent downgrades from SMB 2.0 or 3.0 to SMB 1.0.</span></span> <span data-ttu-id="7bf0f-579">したがって、SMB 1.0 サーバーを無効にすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-579">Therefore, we strongly recommend that you disable the SMB 1.0 server.</span></span> <span data-ttu-id="7bf0f-580">SMB 1.0 サーバーを無効にすることで、SMB 暗号化のすべての機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-580">By disabling the SMB 1.0 server, you can take advantage of the full capabilities of SMB encryption.</span></span>
> - <span data-ttu-id="7bf0f-581">環境内の残りの部分でデータが保護されていることを保証するために、BitLocker ドライブ暗号化をすべてのマシンで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-581">To help ensure that your data is protected while it's at rest in your environment, BitLocker Drive Encryption must be enabled on every machine.</span></span> <span data-ttu-id="7bf0f-582">BitLocker を有効にする方法については、[BitLocker: Windows Server 2012 以降で配置する方法](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-582">For information about how to enable BitLocker, see [BitLocker: How to deploy on Windows Server 2012 and later](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server).</span></span>

1. <span data-ttu-id="7bf0f-583">ファイル共有マシンで、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-583">On the file share machine, run the following command.</span></span>

    ```powershell
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```

2. <span data-ttu-id="7bf0f-584">\\\\DAX7SQLAOFILE1\\aos-storage ファイル共有を設定するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-584">Follow these steps to set up the \\\\DAX7SQLAOFILE1\\aos-storage file share:</span></span>

   1. <span data-ttu-id="7bf0f-585">サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-585">In Server Manager, select **File and Storage Services** \> **Shares**.</span></span>
   2. <span data-ttu-id="7bf0f-586">**タスク**\>**新しい共有** を選択し、新しい共有を作成します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-586">Select **Tasks** \> **New Share** to create a new share.</span></span> <span data-ttu-id="7bf0f-587">共有に **aos-storage** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-587">Name the share **aos-storage**.</span></span>
   3. <span data-ttu-id="7bf0f-588">**共有のキャッシュを許可**を選択したままにします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-588">Leave **Allow caching of share** selected.</span></span>
   4. <span data-ttu-id="7bf0f-589">**データ アクセスを暗号化**を確認してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-589">Check **Encrypt data access**.</span></span>
   5. <span data-ttu-id="7bf0f-590">OrchestratorType を除いて、Service Fabric クラスター内のすべてのマシンに対して**変更**許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-590">Grant **Modify** permissions for every machine in the Service Fabric cluster except OrchestratorType.</span></span>
   6. <span data-ttu-id="7bf0f-591">AOS ドメイン ユーザー (contoso\\AXServiceUser) と gMSA ユーザー (contoso\\svc-AXSF$) に対して、**変更**アクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-591">Grant **Modify** permissions for the user AOS domain user (contoso\\AXServiceUser) and the gMSA user (contoso\\svc-AXSF$).</span></span>

      >[!NOTE]
      > <span data-ttu-id="7bf0f-592">マシンを追加するために**オブジェクト タイプ**の下の**コンピューター**を、またはサービス アカウントを追加するために**オブジェクト タイプ**下の**サービス アカウント**を有効にする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-592">You may need to enable **Computers** under **Object Types** to add machines or enable **Service Accounts** under **Object Types** to add service accounts.</span></span>

3. <span data-ttu-id="7bf0f-593">\\\\DAX7SQLAOFILE1\\ エージェント ファイル共有を設定するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-593">Follow these steps to set up the \\\\DAX7SQLAOFILE1\\agent file share:</span></span>

    1. <span data-ttu-id="7bf0f-594">サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-594">In Server Manager, select **File and Storage Services** \> **Shares**.</span></span>
    2. <span data-ttu-id="7bf0f-595">**タスク**\>**新しい共有** を選択し、新しい共有を作成します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-595">Select **Tasks** \> **New Share** to create a new share.</span></span> <span data-ttu-id="7bf0f-596">共有に**エージェント**と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-596">Name the share **agent**.</span></span>
    3. <span data-ttu-id="7bf0f-597">ローカル展開エージェント (contoso\\svc-LocalAgent$) の gMSA ユーザーに対して **フル コントロール** のアクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-597">Grant **Full-Control** permissions to the gMSA user for the local deployment agent (contoso\\svc-LocalAgent$).</span></span>

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

### <a name="setupsql"></a> <span data-ttu-id="7bf0f-598">13. SQL Server の設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-598">13. Set up SQL Server</span></span>

1. <span data-ttu-id="7bf0f-599">高可用性を備えた SQL Server 2016 SP1 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-599">Install SQL Server 2016 SP1 with high availability.</span></span> <span data-ttu-id="7bf0f-600">(SQL Server の 1 つのインスタンスで十分なサンドボックス環境に配置している場合を除きます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-600">(Unless you're deploying in a sandbox environment, where one instance of SQL Server is sufficient.</span></span> <span data-ttu-id="7bf0f-601">高可用性シナリオをテストするため、サンドボックス環境に高可用性の SQL Server をインストールできます。)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-601">You may want to install SQL Server with high availability in sandbox environments to test high-availability scenarios.)</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7bf0f-602">[SQL Server および Windows 認証モード](https://docs.microsoft.com/en-us/sql/database-engine/configure-windows/change-server-authentication-mode) を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-602">You must enable the [SQL Server and Windows Authentication mode](https://docs.microsoft.com/en-us/sql/database-engine/configure-windows/change-server-authentication-mode).</span></span>

    <span data-ttu-id="7bf0f-603">高可用性を備えた SQL Server を、SAN (ストレージ エリア ネットワーク) を含む SQL クラスターまたは Always-On 構成のいずれかとしてインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-603">You can install SQL Server with high availability either as SQL clusters that include a Storage Area Network (SAN) or in an Always-On configuration.</span></span> <span data-ttu-id="7bf0f-604">データベース エンジン、SSRS、フルテキスト検索、および管理ツールがインストール済みであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-604">Verify that the Database Engine, SSRS, Full-Text Search, and Management Tools are already installed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7bf0f-605">Always-On が [初期データ同期ページの選択 (可用性グループ ウィザードで常に使用する)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) で説明されているとおりに設定され、[セカンダリ データベースを手動で準備する](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs) の指示に従っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-605">Make sure that Always-On is set up as described in [Select Initial Data Synchronization Page (Always On Availability Group Wizards)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards), and follow the instructions in [To Prepare Secondary Databases Manually](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs).</span></span>

2. <span data-ttu-id="7bf0f-606">ドメイン ユーザーとして SQL サービスを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-606">Run the SQL service as a domain user.</span></span>
3. <span data-ttu-id="7bf0f-607">Finance and Operations を構成するために証明機関から SSL 証明書を取得します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-607">Get an SSL certificate from a certificate authority to configure Finance and Operations.</span></span> <span data-ttu-id="7bf0f-608">テストの目的で、自己署名証明書を作成して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-608">For testing purposes, you can create and use a self-signed certificate.</span></span> <span data-ttu-id="7bf0f-609">次の例にあるコンピューター名とドメイン名を置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-609">You will need to replace the computer name and domain name in the following example.</span></span>

    <span data-ttu-id="7bf0f-610">**クラスター化された SQL インスタンスの自己署名証明書**</span><span class="sxs-lookup"><span data-stu-id="7bf0f-610">**Self-signed certificate for a Clustered SQL instance**</span></span>

    ```powershell
    New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contoso.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contoso.com"
    ```

    <span data-ttu-id="7bf0f-611">**Always-On SQL インスタンスの自己署名証明書**</span><span class="sxs-lookup"><span data-stu-id="7bf0f-611">**Self-signed certificate for an Always-On SQL instance**</span></span>

    <span data-ttu-id="7bf0f-612">Always-On のテスト証明書を設定する場合は、以下の**リモート**スクリプトを使用できます。これは、**マニュアル**スクリプトおよび手順 **4.**、**5.**、**6.** と同じ方法で実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-612">If setting up testing certificates for Always-On, you can use the following **remoting** script, which will perform the same as the following **manual** script and steps **4.**, **5.**, and **6.**.</span></span>

    ```powershell
    .\Create-SQLTestCert-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml `
        -SqlMachineNames DAX7SQLAOSQLA01, DAX7SQLAOSQLA02 `
        -SqlListenerName dax7sqlaosqla
    ```

    <span data-ttu-id="7bf0f-613">テスト証明書の**手動**作成。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-613">**Manual** creation of test certificates.</span></span>
    ```powershell
    # https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

    # Manually create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
    # Run script on each node
    $computerName = $env:COMPUTERNAME.ToLower()
    $domain = $env:USERDNSDOMAIN.ToLower()
    $listenerName = 'dax7sqlaosqla'
    $cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'
    ```

4. <span data-ttu-id="7bf0f-614">SQL サーバーで SSL を構成するには、証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-614">Use the certificate(s) to configure SSL on SQL Server.</span></span> <span data-ttu-id="7bf0f-615">[Microsoft 管理コンソールを使用して SQL Server のインスタンスに対する SSL 暗号化を有効にする方法](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-615">Follow the steps in [How to enable SSL encryption for an instance of SQL Server by using Microsoft Management Console](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console).</span></span>
5. <span data-ttu-id="7bf0f-616">SQL クラスターの各ノードに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-616">For each node of the SQL cluster, follow these steps.</span></span> <span data-ttu-id="7bf0f-617">非アクティブなノードで変更を加えて、変更が行われた後フェール オーバーするようにしてください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-617">Make sure that you make the changes on the non-active node, and that you fail over to it after changes are made.</span></span>

    1. <span data-ttu-id="7bf0f-618">LocalMachine\\My に証明書をインポートします。Always-On を設定していない限り、証明書は既にノードに存在します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-618">Import the certificate into LocalMachine\\My, unless you are setting up Always-On, in which case the certificate already exists on the node.</span></span>
    2. <span data-ttu-id="7bf0f-619">SQL サービスを実行するために使用されるサービス アカウントに証明書のアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-619">Grant certificate permissions to the service account that is used to run the SQL service.</span></span> <span data-ttu-id="7bf0f-620">Microsoft 管理コンソール (MMC) で証明書 (**certlm.msc**) を右クリックし、**タスク** \> **秘密キーの管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-620">In Microsoft Management Console (MMC), right-click the certificate (**certlm.msc**), and then select **Tasks** \> **Manage Private Keys**.</span></span>
    3. <span data-ttu-id="7bf0f-621">証明書の拇印を HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate に追加します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-621">Add the certificate thumbprint to HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.</span></span> <span data-ttu-id="7bf0f-622">たとえば、SQL Server 2016 SP1: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\MSSQL13.MSSQLSERVER\\MSSQLServer\\SuperSocketNetLib\\Certificate</span><span class="sxs-lookup"><span data-stu-id="7bf0f-622">For example, with SQL Server 2016 SP1: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\MSSQL13.MSSQLSERVER\\MSSQLServer\\SuperSocketNetLib\\Certificate</span></span>
        1. <span data-ttu-id="7bf0f-623">スタート メニューから、**regedit** をタイプし、**regedit** を選択してレジストリ エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-623">From the start menu, type **regedit**, then select **regedit** to open the registry editor.</span></span>
        2. <span data-ttu-id="7bf0f-624">証明書に移動し、**変更**を右クリックしてから、証明書の拇印に値を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-624">Navigate to the certificate, right-click **Modify**, then replace the value with the certificate thumbprint.</span></span>
    4. <span data-ttu-id="7bf0f-625">Microsoft SQL Server 構成マネージャーで、**ForceEncryption** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-625">In Microsoft SQL Server Configuration Manager, set **ForceEncryption** to **Yes**.</span></span>
        1. <span data-ttu-id="7bf0f-626">**SQL Server 構成マネージャー**で、**SQL Server ネットワークの構成**を展開し、**サーバーのインスタンスのプロトコル**を右クリックしてから、**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-626">In **SQL Server Configuration Manager**, expand **SQL Server Network Configuration**, right-click **Protocols for [server instance]**, and then select **Properties**.</span></span>
        2. <span data-ttu-id="7bf0f-627">**インスタンス名プロパティのプロトコル**ダイアログ ボックスの**証明書**タブで、**証明書**ボックスのドロップダウン メニューから目的の証明書を選択して、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-627">In the **Protocols for [instance name] Properties** dialog box, on the **Certificate** tab, select the desired certificate from the drop-down menu for the **Certificate** box, and then click **OK**.</span></span>
        3. <span data-ttu-id="7bf0f-628">**フラグ**タブの **ForceEncryption** ボックスで、**はい**を選択してから、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-628">On the **Flags** tab, in the **ForceEncryption** box, select **Yes**, and then click **OK**</span></span>
        4. <span data-ttu-id="7bf0f-629">SQL Server サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-629">Restart the SQL Server service.</span></span>

6. <span data-ttu-id="7bf0f-630">証明書の公開鍵 (.cer ファイル) をエクスポートし、各 Service Fabric ノードの信頼できるルートにインストールします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-630">Export the public key of the certificate (the .cer file), and install it in the trusted root of each Service Fabric node.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bf0f-631">リモート処理を使用していた場合は、設定が完了するとクリーンアップ手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-631">If remoting was used, be sure to execute the clean up steps when the setup is complete.</span></span> <span data-ttu-id="7bf0f-632">詳細については、[20. CredSSP を終章処理する](#teardowncredssp) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-632">See the [20. Tear down CredSSP](#teardowncredssp) section for more information.</span></span>

### <a name="configuredb"></a> <span data-ttu-id="7bf0f-633">14. データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7bf0f-633">14. Configure the databases</span></span>

1. <span data-ttu-id="7bf0f-634">[LCS](https://lcs.dynamics.com/v2) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-634">Sign in to [LCS](https://lcs.dynamics.com/v2).</span></span>

2. <span data-ttu-id="7bf0f-635">ダッシュボードで、**共有アセット ライブラリ**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-635">On the dashboard, select the **Shared asset library** tile.</span></span>

3. <span data-ttu-id="7bf0f-636">**モデル**タブで、必要なリリースのデモ データを選択し、zip ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-636">On the **Model** tab, select the demo data for the release that you want and download the zip file.</span></span>

| <span data-ttu-id="7bf0f-637">リリース</span><span class="sxs-lookup"><span data-stu-id="7bf0f-637">Release</span></span> | <span data-ttu-id="7bf0f-638">デモ データ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-638">Demo data</span></span> |
|-------|------|
| <span data-ttu-id="7bf0f-639">オンプレミスの一般提供 (GA) リリース</span><span class="sxs-lookup"><span data-stu-id="7bf0f-639">On-premises General Availability (GA) release</span></span> | <span data-ttu-id="7bf0f-640">Dynamics 365 for Operations オンプレミス - デモ データ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-640">Dynamics 365 for Operations on-premises - Demo data</span></span> |
| <span data-ttu-id="7bf0f-641">オンプレミスのプラットフォーム更新プログラム 2017 年 11 月 11 日リリース</span><span class="sxs-lookup"><span data-stu-id="7bf0f-641">On-premises Platform Update 11 Nov 2017 release</span></span> | <span data-ttu-id="7bf0f-642">Dynamics 365 for Operations オンプレミス Enterprise Edition - 更新プログラム 11 デモ データ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-642">Dynamics 365 for Operations on-premises, Enterprise edition - Update 11 Demo data</span></span> |
| <span data-ttu-id="7bf0f-643">オンプレミスのプラットフォーム更新プログラム 2018 年 3 月 12 日リリース</span><span class="sxs-lookup"><span data-stu-id="7bf0f-643">On-premises Platform Update 12 Mar 2018 release</span></span> | <span data-ttu-id="7bf0f-644">Dynamics 365 for Operations オンプレミス、Enterprise Edition - 更新プログラム 12 デモ データ</span><span class="sxs-lookup"><span data-stu-id="7bf0f-644">Dynamics 365 for Operations on-premises, Enterprise edition - Update 12 Demo data</span></span> |

4. <span data-ttu-id="7bf0f-645">zip ファイルには空のデモデータ .bak ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-645">The zip file contains empty and demo data .bak files.</span></span> <span data-ttu-id="7bf0f-646">必要に応じて、.bak ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-646">Select the .bak file, based on your requirements.</span></span> <span data-ttu-id="7bf0f-647">たとえば、デモ データが必要な場合は、AxBootstrapDB_Demodata.bak ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-647">For example, if you require demo data, download the AxBootstrapDB_Demodata.bak file.</span></span>

5. <span data-ttu-id="7bf0f-648">infrastructure\ConfigTempate.xml のデータベース セクションが、次のように正しく構成されているか確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-648">Ensure the database section in the infrastructure\ConfigTempate.xml is configured correctly with the following:</span></span>
    1. <span data-ttu-id="7bf0f-649">データベース名。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-649">The database name.</span></span>
    2. <span data-ttu-id="7bf0f-650">db ファイルとログ設定。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-650">The db file and log settings.</span></span> <span data-ttu-id="7bf0f-651">dbの設定は、指定された既定値以上にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-651">The db settings should not be lower than the defaults specified.</span></span>
    3. <span data-ttu-id="7bf0f-652">LCS 共有アセット ライブラリからダウンロードされるバックアップ ファイルへのパス。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-652">The path to the backup file downloaded from LCS Shared Asset library.</span></span> <span data-ttu-id="7bf0f-653">Finance and Operations データベースの既定の名前は AXDB です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-653">The default name for the Finance and Operations database is AXDB.</span></span>

   > [!WARNING]
   > - <span data-ttu-id="7bf0f-654">SQL サービスを実行しているユーザーとスクリプトを実行しているユーザーは、バックアップ ファイルが格納されているフォルダーまたは共有に対して READ アクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-654">The user running the SQL service and the user running the scripts should have READ access on the folder or share where the backup file is located.</span></span>
   > 
   > - <span data-ttu-id="7bf0f-655">同じ名前のデータベースが存在する場合は、データベースが再利用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-655">If a database with the same name exists, the database will be reused.</span></span>

6. <span data-ttu-id="7bf0f-656">**インフラストラクチャ**フォルダーを SQL Server マシンにコピーし、権限を昇格した PowerShell ウィンドウでそのフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-656">Copy the **infrastructure** folder to the SQL Server machine and navigate to it in a PowerShell window with elevate privileges.</span></span>

#### <a name="configure-the-orchestratordata-database"></a><span data-ttu-id="7bf0f-657">OrchestratorData データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7bf0f-657">Configure the OrchestratorData database</span></span>

1. <span data-ttu-id="7bf0f-658">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-658">Execute the following script.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
   ```

   <span data-ttu-id="7bf0f-659">スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-659">The script will do the following:</span></span>
  
   - <span data-ttu-id="7bf0f-660">**OrchestratorData** という名前の空のデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-660">Create an empty database named **OrchestratorData**.</span></span> <span data-ttu-id="7bf0f-661">このデータベースは、オンプレミスのローカル エージェントによって配置を調整するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-661">This database is used by the on-premises local agent to orchestrate deployments.</span></span>
   - <span data-ttu-id="7bf0f-662">データベースにローカル エージェント gMSA (svc-LocalAgent$) **db\_owner** アクセス許可を与えます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-662">Grant the local agent gMSA (svc-LocalAgent$) **db\_owner** permissions on the database.</span></span>

#### <a name="configure-the-finance-and-operations-database"></a><span data-ttu-id="7bf0f-663">Finance and Operations データベースの構成</span><span class="sxs-lookup"><span data-stu-id="7bf0f-663">Configure the Finance and Operations database</span></span>

1. <span data-ttu-id="7bf0f-664">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-664">Execute the following scripts.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
   .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
   ```

   <span data-ttu-id="7bf0f-665">**Initialize-Database.ps1** スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-665">The **Initialize-Database.ps1** script will do the following:</span></span>

   1. <span data-ttu-id="7bf0f-666">指定されたバックアップ ファイルからデータベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-666">Restore the database from the specified backup file.</span></span>
   2. <span data-ttu-id="7bf0f-667">SQL 認証が有効になっている新しいユーザーを作成します (axdbadmin)。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-667">Create a new user that has SQL authentication enabled (axdbadmin).</span></span>
   3. <span data-ttu-id="7bf0f-668">AXDB の次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-668">Map users to database roles based on the following table for AXDB.</span></span>

      | <span data-ttu-id="7bf0f-669">ユーザー</span><span class="sxs-lookup"><span data-stu-id="7bf0f-669">User</span></span>            | <span data-ttu-id="7bf0f-670">種類</span><span class="sxs-lookup"><span data-stu-id="7bf0f-670">Type</span></span>    | <span data-ttu-id="7bf0f-671">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="7bf0f-671">Database role</span></span> |
      |-----------------|---------|---------------|
      | <span data-ttu-id="7bf0f-672">svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-672">svc-AXSF$</span></span>       | <span data-ttu-id="7bf0f-673">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-673">gMSA</span></span>    | <span data-ttu-id="7bf0f-674">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7bf0f-674">db\_owner</span></span>     |
      | <span data-ttu-id="7bf0f-675">svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-675">svc-LocalAgent$</span></span> | <span data-ttu-id="7bf0f-676">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-676">gMSA</span></span>    | <span data-ttu-id="7bf0f-677">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7bf0f-677">db\_owner</span></span>     |
      | <span data-ttu-id="7bf0f-678">svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-678">svc-FRPS$</span></span>       | <span data-ttu-id="7bf0f-679">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-679">gMSA</span></span>    | <span data-ttu-id="7bf0f-680">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7bf0f-680">db\_owner</span></span>     |
      | <span data-ttu-id="7bf0f-681">svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-681">svc-FRAS$</span></span>       | <span data-ttu-id="7bf0f-682">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-682">gMSA</span></span>    | <span data-ttu-id="7bf0f-683">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7bf0f-683">db\_owner</span></span>     |
      | <span data-ttu-id="7bf0f-684">axdbadmin</span><span class="sxs-lookup"><span data-stu-id="7bf0f-684">axdbadmin</span></span>       | <span data-ttu-id="7bf0f-685">SqlUser</span><span class="sxs-lookup"><span data-stu-id="7bf0f-685">SqlUser</span></span> | <span data-ttu-id="7bf0f-686">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7bf0f-686">db\_owner</span></span>     |


   4. <span data-ttu-id="7bf0f-687">TempDB の次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-687">Map users to database roles based on the following table for TempDB.</span></span>

      | <span data-ttu-id="7bf0f-688">ユーザー</span><span class="sxs-lookup"><span data-stu-id="7bf0f-688">User</span></span>            | <span data-ttu-id="7bf0f-689">種類</span><span class="sxs-lookup"><span data-stu-id="7bf0f-689">Type</span></span>    | <span data-ttu-id="7bf0f-690">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="7bf0f-690">Database role</span></span> |
      |-----------------|---------|---------------|
      | <span data-ttu-id="7bf0f-691">svc-AXSF$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-691">svc-AXSF$</span></span>       | <span data-ttu-id="7bf0f-692">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-692">gMSA</span></span>    | <span data-ttu-id="7bf0f-693">db_datareader, db_datawriter, db_ddladmin</span><span class="sxs-lookup"><span data-stu-id="7bf0f-693">db_datareader, db_datawriter, db_ddladmin</span></span>     |
      | <span data-ttu-id="7bf0f-694">axdbadmin</span><span class="sxs-lookup"><span data-stu-id="7bf0f-694">axdbadmin</span></span>       | <span data-ttu-id="7bf0f-695">SqlUser</span><span class="sxs-lookup"><span data-stu-id="7bf0f-695">SqlUser</span></span> | <span data-ttu-id="7bf0f-696">db_datareader, db_datawriter, db_ddladmin</span><span class="sxs-lookup"><span data-stu-id="7bf0f-696">db_datareader, db_datawriter, db_ddladmin</span></span>     |

   <span data-ttu-id="7bf0f-697">**Configure-Database.ps1** スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-697">The **Configure-Database.ps1** script will do the following:</span></span>

    1. <span data-ttu-id="7bf0f-698">READ_COMMITTED_SNAPSHOT ON を設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-698">Set READ_COMMITTED_SNAPSHOT ON</span></span>
    2. <span data-ttu-id="7bf0f-699">ALLOW_SNAPSHOT_ISOLATION ON を設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-699">Set ALLOW_SNAPSHOT_ISOLATION ON</span></span>
    3. <span data-ttu-id="7bf0f-700">指定したデータベース ファイルとログの設定を設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-700">Set the specified database file and log settings</span></span>
    4. <span data-ttu-id="7bf0f-701">サーバー状態の表示を axdbadmin に付与</span><span class="sxs-lookup"><span data-stu-id="7bf0f-701">GRANT VIEW SERVER STATE TO axdbadmin</span></span>
    5. <span data-ttu-id="7bf0f-702">サーバー状態の表示を [contoso\svc AXSF$] に付与</span><span class="sxs-lookup"><span data-stu-id="7bf0f-702">GRANT VIEW SERVER STATE TO [contoso\svc-AXSF$]</span></span>

2. <span data-ttu-id="7bf0f-703">データベース ユーザーをリセットするには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-703">Run the following command to reset the database users.</span></span>

    ```powershell
    .\Reset-DatabaseUsers.ps1 -DatabaseServer '<FQDN of the SQL server>' -DatabaseName '<AX database name>'
    ```

#### <a name="configure-the-financial-reporting-database"></a><span data-ttu-id="7bf0f-704">財務レポート データベースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7bf0f-704">Configure the Financial Reporting database</span></span>

1. <span data-ttu-id="7bf0f-705">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-705">Execute the following script.</span></span>

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName MR
   ```

   <span data-ttu-id="7bf0f-706">スクリプトは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-706">The script will do the following:</span></span>
   1. <span data-ttu-id="7bf0f-707">**FinancialReporting** という名前の空のデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-707">Create an empty database named **FinancialReporting**.</span></span>
   2. <span data-ttu-id="7bf0f-708">次の表に基づくデータベース ロールにユーザーをマップします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-708">Map the users to database roles based on the following table.</span></span>

      | <span data-ttu-id="7bf0f-709">ユーザー</span><span class="sxs-lookup"><span data-stu-id="7bf0f-709">User</span></span>            | <span data-ttu-id="7bf0f-710">種類</span><span class="sxs-lookup"><span data-stu-id="7bf0f-710">Type</span></span> | <span data-ttu-id="7bf0f-711">データベース ロール</span><span class="sxs-lookup"><span data-stu-id="7bf0f-711">Database role</span></span> |
      |-----------------|------|---------------|
      | <span data-ttu-id="7bf0f-712">svc-LocalAgent$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-712">svc-LocalAgent$</span></span> | <span data-ttu-id="7bf0f-713">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-713">gMSA</span></span> | <span data-ttu-id="7bf0f-714">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7bf0f-714">db\_owner</span></span>     |
      | <span data-ttu-id="7bf0f-715">svc-FRPS$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-715">svc-FRPS$</span></span>       | <span data-ttu-id="7bf0f-716">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-716">gMSA</span></span> | <span data-ttu-id="7bf0f-717">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7bf0f-717">db\_owner</span></span>     |
      | <span data-ttu-id="7bf0f-718">svc-FRAS$</span><span class="sxs-lookup"><span data-stu-id="7bf0f-718">svc-FRAS$</span></span>       | <span data-ttu-id="7bf0f-719">gMSA</span><span class="sxs-lookup"><span data-stu-id="7bf0f-719">gMSA</span></span> | <span data-ttu-id="7bf0f-720">db\_owner</span><span class="sxs-lookup"><span data-stu-id="7bf0f-720">db\_owner</span></span>     |

### <a name="encryptcred"></a> <span data-ttu-id="7bf0f-721">15. 資格情報の暗号化</span><span class="sxs-lookup"><span data-stu-id="7bf0f-721">15. Encrypt credentials</span></span>

1. <span data-ttu-id="7bf0f-722">任意のクライアント マシンで、LocalMachine\\My certificate store に暗号化証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-722">On any client machine, install the encipherment certificate in the LocalMachine\\My certificate store.</span></span>
2. <span data-ttu-id="7bf0f-723">現在のユーザーにこの証明書の秘密キーへの読み取りアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-723">Grant the current user read access to the private key of this certificate.</span></span>
3. <span data-ttu-id="7bf0f-724">次のようにして、Credentials.json ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-724">Create the Credentials.json file, as shown here.</span></span>

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

    - <span data-ttu-id="7bf0f-725">**AccountPassword** は、AOS ドメインユーザー (contoso\\axserviceuser) の暗号化されたドメイン ユーザー パスワードです。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-725">**AccountPassword** is the encrypted domain user password for the AOS domain user (contoso\\axserviceuser).</span></span>
    - <span data-ttu-id="7bf0f-726">**SqlUser** は、Finance and Operations データベース (AXDB) にアクセスできる暗号化された SQL ユーザー (axdbadmin) で、**SqlPassword** は暗号化された SQL パスワードです。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-726">**SqlUser** is the encrypted SQL user (axdbadmin) that has access to the Finance and Operations database (AXDB), and **SqlPassword** is the encrypted SQL password.</span></span>

4. <span data-ttu-id="7bf0f-727">.json ファイルを SMB ファイル共有、\\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json にコピーします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-727">Copy the .json file to the SMB file share, \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.</span></span>
5. <span data-ttu-id="7bf0f-728">暗号化された値で Credentials.json ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-728">Update the Credentials.json file with encrypted values.</span></span>

    ```powershell
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | Set-Clipboard
    ```
    > [!IMPORTANT]
    > <span data-ttu-id="7bf0f-729">*Invoke-ServiceFabricEncryptText* を呼び出す前に、[Microsoft Azure Service Fabric SDK](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-get-started#sdk-installation-only) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-729">Before you can invoke *Invoke-ServiceFabricEncryptText*, you need to install [Microsoft Azure Service Fabric SDK](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-get-started#sdk-installation-only).</span></span>
    > <span data-ttu-id="7bf0f-730">Azure Service Fabric SDK をインストールした後、「Invoke-ServiceFabricEncryptText は認識されないコマンドです」というエラーが発生した場合は、コンピューターを再起動して再試行してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-730">If you encounter the following error, "Invoke-ServiceFabricEncryptText is not recognized command" after you install the Azure Service Fabric SDK, restart the computer and retry.</span></span>

### <a name="setupssis"></a> <span data-ttu-id="7bf0f-731">16. SSIS の設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-731">16. Set up SSIS</span></span>

<span data-ttu-id="7bf0f-732">データ管理と統合ワークロードを有効にするには、各 AOS 仮想マシンに SSIS をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-732">To enable Data management and Integration workloads, SSIS must be installed on each of the AOS virtual machines.</span></span> <span data-ttu-id="7bf0f-733">各 AOS 仮想マシン上で、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-733">Complete the following steps on each AOS virtual machine.</span></span>

1. <span data-ttu-id="7bf0f-734">マシンに SSIS インストールへのアクセス許可があることを確認し、SSIS セットアップ ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-734">Verify that the machine has access to the SSIS installation and open the SSIS Setup Wizard.</span></span>
2. <span data-ttu-id="7bf0f-735">**機能の選択**ウィンドウの**機能**ウィンドウで、**Integration Services** および **SQL クライアント接続 SDK** のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-735">In the **Feature Selection** window, in the **Features** pane, select the **Integration Services** and **SQL Client Connectivity SDK** check boxes.</span></span>
3. <span data-ttu-id="7bf0f-736">セットアップを完了し、インストールが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-736">Complete the setup and verify that the installation was successful.</span></span>

<span data-ttu-id="7bf0f-737">詳細については、[統合サービスのインストール](https://docs.microsoft.com/en-us/sql/integration-services/install-windows/install-integration-services) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-737">For more information, see [Install integration services](https://docs.microsoft.com/en-us/sql/integration-services/install-windows/install-integration-services).</span></span>

### <a name="setupssrs"></a> <span data-ttu-id="7bf0f-738">17. SSRS の設定</span><span class="sxs-lookup"><span data-stu-id="7bf0f-738">17. Set up SSRS</span></span>

1. <span data-ttu-id="7bf0f-739">開始する前に、このトピックの冒頭に記載されている前提条件がインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-739">Before you begin, make sure that the prerequisites that are listed at the beginning of this topic are installed.</span></span>
2. <span data-ttu-id="7bf0f-740">[オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション](../analytics/configure-ssrs-on-premises.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-740">Follow the steps in [Configure SQL Server Reporting Services for an on-premises deployment](../analytics/configure-ssrs-on-premises.md).</span></span>
    > [!IMPORTANT]
    > <span data-ttu-id="7bf0f-741">SSRS のインストール時にデータベース エンジンをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-741">You must install then database engine when you install SSRS.</span></span>

### <a name="configureadfs"></a><span data-ttu-id="7bf0f-742">18. AD FS のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7bf0f-742">18. Configure AD FS</span></span>

<span data-ttu-id="7bf0f-743">この手順を完了する前に、AD FS を Windows Server 2016 に展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-743">Before you can complete this procedure, AD FS must be deployed on Windows Server 2016.</span></span> <span data-ttu-id="7bf0f-744">AD FS を展開する方法については、[Windows Server 2016 配置ガイドおよび 2012 R2 AD FS 配置ガイド](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-744">For information about how to deploy AD FS, see [Deployment Guide Windows Server 2016 and 2012 R2 AD FS Deployment Guide](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).</span></span>

<span data-ttu-id="7bf0f-745">Finance and Operations では、AD FS の既定で標準のコンフィギュレーション以外の追加のコンフィギュレーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-745">Finance and Operations requires additional configuration beyond the default out-of-box configuration of AD FS.</span></span> <span data-ttu-id="7bf0f-746">以下の Windows PowerShell コマンドを、AD FS ロール サービスがインストールされているマシン上で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-746">The following Windows PowerShell commands must be run on the machine where the AD FS role service is installed.</span></span> <span data-ttu-id="7bf0f-747">ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-747">The user account must have enough permissions to administer AD FS.</span></span> <span data-ttu-id="7bf0f-748">たとえば、ユーザーには、ドメイン管理者アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-748">For example, the user must have a domain administrator account.</span></span> <span data-ttu-id="7bf0f-749">複雑な AD FS シナリオでは、ドメイン管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-749">For complex AD FS scenarios, consult your domain administrator.</span></span>

1. <span data-ttu-id="7bf0f-750">AD FS 識別子を構成して、AD FS トークン発行者と一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-750">Configure the AD FS identifier so that it matches the AD FS token issuer.</span></span>

   <span data-ttu-id="7bf0f-751">このコマンドは、Finance and Operations クライアントの **ユーザー** ページ (**システム管理 > ユーザー > ユーザー**) で **ユーザーをインポート** オプションを使用した新しいユーザーの追加に関連しています。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-751">This command is related to adding new users using the **Import users** option on the **Users** page (**System administration > Users > Users**) in the Finance and Operations client.</span></span>

    ```PowerShell
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. <span data-ttu-id="7bf0f-752">混在環境用に AD FS を構成していない限り、イントラネット認証接続用に Windows 統合認証 (WIA) を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-752">You should disable Windows Integrated Authentication (WIA) for intranet authentication connections, unless you've configured AD FS for mixed environments.</span></span> <span data-ttu-id="7bf0f-753">WIA を AD FS で使用できるように構成する方法の詳細については、[AD FS で Windows 統合認証 (WIA) を使用するようにブラウザを構成する](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-753">For more information about how to configure WIA so that it can be used with AD FS, see [Configure browsers to use Windows Integrated Authentication (WIA) with AD FS](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).</span></span>

   <span data-ttu-id="7bf0f-754">このコマンドは、Finance and Operations クライアントへのログイン時のフォーム認証の使用に関連しています。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-754">This command is related to using forms authentication upon signing into the Finance and Operations client.</span></span> <span data-ttu-id="7bf0f-755">シングル サインオンなど、追加の設定が必要な他のオプションが使用可能な場合があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-755">Other options, such as single sign-on, may be available which require additional setup.</span></span>

    ```powershell
    Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
    ```

3. <span data-ttu-id="7bf0f-756">サインインの場合、ユーザーの電子メール アドレスは許容される認証入力でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-756">For sign-in, the user's email address must be an acceptable authentication input.</span></span>

   <span data-ttu-id="7bf0f-757">このコマンドは、電子メール要求の設定に関連しています。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-757">This command is related to setting up email claims.</span></span> <span data-ttu-id="7bf0f-758">変換ルールなど、追加の設定が必要な他のオプションが使用可能な場合があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-758">Other options, such as transformation rules, may be available which require additional setup.</span></span>

    ```powershell
    Add-Type -AssemblyName System.Net
    $fqdn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
    $domainName = $fqdn.Substring($fqdn.IndexOf('.')+1)
    Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
    ```

<span data-ttu-id="7bf0f-759">AD FS が認証を交換するために Finance and Operations を信頼するためには、AD FS アプリケーション グループの下の AD FS にさまざまなアプリケーション エントリを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-759">In order for AD FS to trust Finance and Operations for the exchange of authentication, various application entries must be registered in AD FS under an AD FS application group.</span></span> <span data-ttu-id="7bf0f-760">設定プロセスをスピードアップし、エラーを減らすために、次のスクリプトを使用して登録します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-760">To speed up the setup process and help reduce errors, you can use the following script for registration.</span></span> <span data-ttu-id="7bf0f-761">Publish-ADFSApplicationGroup.ps1 スクリプトと D365FO-OP ディレクトリを、AD FS ロール サービスがインストールされているマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-761">Copy the Publish-ADFSApplicationGroup.ps1 script and D365FO-OP directory to a machine where the AD FS role service is installed.</span></span> <span data-ttu-id="7bf0f-762">次に、AD FS を管理するための十分なアクセス許可を持つユーザー アカウントを使用してスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-762">Then run the script by using a user account that has enough permissions to administer AD FS.</span></span> <span data-ttu-id="7bf0f-763">(たとえば、管理者アカウントを使用します。)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-763">(For example, use an administrator account.)</span></span>

<span data-ttu-id="7bf0f-764">スクリプトの使用方法の詳細については、スクリプトに記載されているドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-764">For more information about how to use the script, see the documentation that is listed in the script.</span></span> <span data-ttu-id="7bf0f-765">後の手順の LCS でこの情報が必要となるため、出力に指定されているクライアント ID を書き留めておいてください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-765">Make a note of the client IDs that are specified in the output, because you will need this information in LCS in a later step.</span></span> <span data-ttu-id="7bf0f-766">クライアント ID を紛失した場合、AD FS がインストールされているコンピューターにログインし、**サーバー マネージャー** \> **ツール** \> **AD FS の管理** \> **アプリケーション グループ** \> **Microsoft Dynamics 365 for Operations On-premises** を開き、ネイティブ アプリケーションでクライアント ID を見つけます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-766">Should you lose the client IDs, log in to the machine which has AD FS installed, open **Server Manager** \> **Tools** \> **AD FS Management** \> **Application Groups** \> **Microsoft Dynamics 365 for Operations On-premises** and find the client IDs under the native applications.</span></span>

```powershell
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
```

![アプリケーション グループのプロパティ](./media/OPSetup_05_ApplicatioGroupProperties.png)

<span data-ttu-id="7bf0f-768">最後に、**AOSNodeType** タイプの Service Fabric ノード上の AD FS OpenID コンフィギュレーション URL にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-768">Finally, make sure that you can access the AD FS OpenID Configuration URL on a Service Fabric node of the **AOSNodeType** type.</span></span> <span data-ttu-id="7bf0f-769">このチェックを行うには、Web ブラウザーで `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` を開きます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-769">To perform this check, try to open `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` in a web browser.</span></span> <span data-ttu-id="7bf0f-770">サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていません。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-770">If you receive a message that states that the site isn't secure, you haven't added your AD FS SSL certificate to the Trusted Root Certification Authorities store.</span></span> <span data-ttu-id="7bf0f-771">このステップについては、「AD FS 展開ガイド」で説明されています。リモーティングを使用している場合は、次のスクリプトを使用して、Service Fabric クラスター内のすべてのノードに証明書をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-771">This step is described in the AD FS deployment guide, and if you are using remoting, you can use the following script to install the certificate on all nodes in the Service Fabric cluster:</span></span>

```powershell
# If remoting, execute
.\Install-ADFSCert-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

<span data-ttu-id="7bf0f-772">URL に正常にアクセスすると、AD FS コンフィギュレーションを含む JavaScript Object Notation (JSON) ファイルが返され、AD FS URL が信頼されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-772">If you successfully access the URL, a JavaScript Object Notation (JSON) file is returned that contains your AD FS configuration, and you will see that your AD FS URL is trusted.</span></span>

<span data-ttu-id="7bf0f-773">これで、インフラストラクチャの設定を完了しました。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-773">You've now completed the setup of the infrastructure.</span></span> <span data-ttu-id="7bf0f-774">次のセクションでは、[LCS](https://lcs.dynamics.com) にアクセスしてコネクタを設定し、Finance and Operations 環境を配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-774">The following sections describe how to navigate to [LCS](https://lcs.dynamics.com) to set up your connector and deploy your Finance and Operations environment.</span></span>

### <a name="configureconnector"></a> <span data-ttu-id="7bf0f-775">19. コネクタのコンフィギュレーションと、オンプレミスのローカル エージェントのインストール</span><span class="sxs-lookup"><span data-stu-id="7bf0f-775">19. Configure a connector and install an on-premises local agent</span></span>

1. <span data-ttu-id="7bf0f-776">[LCS](https://lcs.dynamics.com/) にサインインし、オンプレミスの実装プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-776">Sign in to [LCS](https://lcs.dynamics.com/), and open the on-premises implementation project.</span></span>
2. <span data-ttu-id="7bf0f-777">ハンバーガー メニューで、**プロジェクト設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-777">On the hamburger menu, select **Project settings**.</span></span>

    ![プロジェクト設定コマンド](./media/OPSetup_06_ProjectSettings.png)

3. <span data-ttu-id="7bf0f-779">**オンプレミス コネクタ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-779">Select **On-premises connectors**.</span></span>
4. <span data-ttu-id="7bf0f-780">新しいコネクタを作成するには、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-780">Select **Add** to create a new connector.</span></span> 
5. <span data-ttu-id="7bf0f-781">**ホスト インフラストラクチャ設定** タブで、エージェント インストーラーをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-781">On the **Setup host infrastructure** tab, download the agent installer.</span></span>

    ![[ホスト インフラストラクチャ設定] タブで、エージェント インストーラー ボタンをダウンロードする](./media/OPSetup_07_DownloadAgentInstaller.png)
6. <span data-ttu-id="7bf0f-783">zip ファイルがブロックされていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-783">Verify that the zip file is unblocked.</span></span> <span data-ttu-id="7bf0f-784">ファイルを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-784">Right-click the file, and then select **Properties**.</span></span> <span data-ttu-id="7bf0f-785">ダイアログ ボックスで**ブロック解除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-785">In the dialog box, select **Unblock**.</span></span>
7. <span data-ttu-id="7bf0f-786">**OrchestratorType** タイプの Service Fabric ノードの 1 つでエージェント インストーラーを解凍します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-786">Unzip the agent installer on one of the Service Fabric nodes of the **OrchestratorType** type.</span></span>
8. <span data-ttu-id="7bf0f-787">**構成エージェント** タブで、コンフィギュレーションの設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-787">On the **Configure agent** tab, enter the configuration settings.</span></span> <span data-ttu-id="7bf0f-788">必要な値を取得するには、そのマシンと構成ファイルにアクセスできる任意のマシンで次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-788">Execute the following script on any machine with access to it and the configuration file, to get the needed values.</span></span>

    ```powershell
    .\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

9. <span data-ttu-id="7bf0f-789">コンフィギュレーションを保存し、**コンフィギュレーションのダウンロード** を選択して、localagent-config.json コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-789">Save the configuration, and then select **Download configurations** to download the localagent-config.json configuration file.</span></span>

    ![[エージェントの設定] タブの [コンフィギュレーションのダウンロード] ボタン](./media/OPSetup_08_DownloadConfigurations.png)

10. <span data-ttu-id="7bf0f-791">localagent-config.json ファイルを、エージェント インストーラー パッケージが配置されているマシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-791">Copy the localagent-config.json file to the machine where the agent installer package is located.</span></span>
11. <span data-ttu-id="7bf0f-792">**コマンド プロンプト** ウィンドウで、エージェント インストーラーを含むフォルダーに移動して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-792">In a **Command Prompt** window, run the following command by navigating to the folder that contains the agent installer.</span></span>

    ```powershell
    LocalAgentCLI.exe Install <path of config.json>
    ```

    > [!NOTE]
    > <span data-ttu-id="7bf0f-793">このコマンドを実行するユーザーは、OrchestratorData データベースに対して **db\_owner** のアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-793">The user who runs this command must have **db\_owner** permissions on the OrchestratorData database.</span></span>

12. <span data-ttu-id="7bf0f-794">ローカル エージェントが正常にインストールされると、LCS のオンプレミス コネクタに戻るようにします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-794">After the local agent is successfully installed, navigate back to your on-premises connector in LCS.</span></span>
13. <span data-ttu-id="7bf0f-795">**設定の検証**タブで、**メッセージ エージェント**を選択して、ローカル エージェントへの LCS 接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-795">On the **Validate setup** tab, select **Message agent** to test for LCS connectivity to your local agent.</span></span> <span data-ttu-id="7bf0f-796">接続が正常に確立されると、ページは下図のようになります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-796">When a connection is successfully established, the page will resemble the following illustration.</span></span>

    ![エージェントの検証](./media/ValidateAgent.PNG)

### <a name="teardowncredssp"></a> <span data-ttu-id="7bf0f-798">20. リモート処理が使用された場合、CredSSP を終了処理する</span><span class="sxs-lookup"><span data-stu-id="7bf0f-798">20. Tear down CredSSP, if remoting was used</span></span>

<span data-ttu-id="7bf0f-799">セットアップ中にリモート処理スクリプトのいずれかが使用された場合は、セットアップ プロセスの中断時または完了時に、次のスクリプトを実行してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-799">If any of the remoting scripts were used during setup, be sure to execute the following script when there are breaks in the setup process, or the setup has finished.</span></span>

```powershell
.\Disable-CredSSP-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

<span data-ttu-id="7bf0f-800">前のリモート PowerShell ウィンドウが誤って終了し、CredSSP が有効にまったままである場合、スクリプトにより、コンフィギュレーション ファイルで指定されたすべてのコンピューター上で無効にされます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-800">If the previous remoting PowerShell window was accidentally closed and CredSSP was left enabled, the script will disable it on all the machines specified in the configuration file.</span></span>

### <a name="deploy"></a> <span data-ttu-id="7bf0f-801">21. LCS から Finance and Operations (オンプレミス) 環境を配置する</span><span class="sxs-lookup"><span data-stu-id="7bf0f-801">21. Deploy your Finance and Operations (on-premises) environment from LCS</span></span>

1. <span data-ttu-id="7bf0f-802">LCS で、オンプレミス プロジェクトに移動し、**環境** > **サンドボックス**に移動してから**構成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-802">In LCS, navigate to your on-premises project, go to **Environment** > **Sandbox**, and then select **Configure**.</span></span> <span data-ttu-id="7bf0f-803">必要な値を取得するには、ADFS および DNS サーバー設定にアクセスする必要があるプライマリ ドメイン コントローラ VM で次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-803">Execute the following script on the primary domain controller VM, which must have access to ADFS and the DNS server settings, to get the needed values.</span></span>

    ```powershell
    .\Get-DeploymentSettings.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. <span data-ttu-id="7bf0f-804">新しい展開では、環境のトポロジを選択し、展開を開始するウィザードを完了します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-804">For new deployments, select your environment topology, and then complete the wizard to start your deployment.</span></span>

![配置](./media/Deploy.png)

3. <span data-ttu-id="7bf0f-806">既存のプラットフォーム更新プログラム 8 またはプラットフォーム更新プログラム 11 を展開する場合:</span><span class="sxs-lookup"><span data-stu-id="7bf0f-806">If you have an existing Platform update 8 or Platform update 11 deployment:</span></span> 
    - <span data-ttu-id="7bf0f-807">ローカル エージェントを更新します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-807">Update the local agent.</span></span> <span data-ttu-id="7bf0f-808">詳細については、[ローカル エージェントの更新](../lifecycle-services/update-local-agent.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-808">See [Update your local agent](../lifecycle-services/update-local-agent.md) for more details.</span></span>
    - <span data-ttu-id="7bf0f-809">LCS からローカル エージェントを検証します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-809">Validate the local agent from LCS.</span></span>
    - <span data-ttu-id="7bf0f-810">[環境の再構成](../lifecycle-services/reconfigure-environment.md) の手順を実行しながらプラットフォーム更新プログラム 12 を導入します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-810">Deploy Platform update 12 while going through the steps in [Reconfigure your environment](../lifecycle-services/reconfigure-environment.md).</span></span>
4. <span data-ttu-id="7bf0f-811">LCS は準備フェーズ中に環境の Service Fabric アプリケーション パッケージを組み立てます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-811">LCS will assemble the Service Fabric application packages for your environment during the preparation phase.</span></span> <span data-ttu-id="7bf0f-812">配置を開始するローカル エージェントにメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-812">It then sends a message to the local agent to start deployment.</span></span> <span data-ttu-id="7bf0f-813">下記のように、**準備中** ステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-813">You will notice the **Preparing** status as below.</span></span>

![準備中](./media/Preparing.png)

<span data-ttu-id="7bf0f-815">以下に示すような環境の詳細ページに移動するには、**完全な詳細**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-815">Click **Full details** to take you to the environment details page, as shown below.</span></span>

![Details_Preparing](./media/Details_Preparing.png)

5. <span data-ttu-id="7bf0f-817">ローカル エージェントは配置要求を受け取り、配置を開始し、環境の準備ができたら LCS に再度通知します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-817">The local agent will now pick up the deployment request, start the deployment, and communicate back to LCS when the environment is ready.</span></span> <span data-ttu-id="7bf0f-818">表示されているとおりに、配置の開始がしたときに、ステータスは**配置**に変更します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-818">When deployment starts, the status will change to **Deploying**, as shown.</span></span>

![配置しています](./media/Deploying.png)

![Details_Deploying](./media/Details_Deploying.png)

<span data-ttu-id="7bf0f-821">展開に失敗した場合、LCS のお客様の環境では、**再設定**ボタンは次のように利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-821">If the deployment fails, the **Reconfigure** button will become available for your environment in LCS, as shown below.</span></span> <span data-ttu-id="7bf0f-822">基になる問題を修正し、**再コンフィギュレーション**をクリックして、任意のコンフィギュレーションの変更を更新し、**配置**をクリックして配置を再試行します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-822">Fix the underlying issue, click **Reconfigure**, update any configuration changes, and click **Deploy** to retry the deployment.</span></span>

![失敗](./media/Failed.png)

<span data-ttu-id="7bf0f-824">再構成する方法の詳細については、[環境の再構成](../lifecycle-services/reconfigure-environment.md) トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-824">See the [Reconfigure your environment](../lifecycle-services/reconfigure-environment.md) topic for details about how to reconfigure.</span></span> <span data-ttu-id="7bf0f-825">次の図は、正常な配置を示します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-825">The following graphic shows a successful deployment.</span></span>
<span data-ttu-id="7bf0f-826">![配置済み](./media/Deployed.png)</span><span class="sxs-lookup"><span data-stu-id="7bf0f-826">![Deployed](./media/Deployed.png)</span></span>

### <a name="connect"></a> <span data-ttu-id="7bf0f-827">22. Finance and Operations (オンプレミス) 環境に接続する</span><span class="sxs-lookup"><span data-stu-id="7bf0f-827">22. Connect to your Finance and Operations (on-premises) environment</span></span>
<span data-ttu-id="7bf0f-828">ブラウザーで、https://[yourD365FOdomain]/namespaces/AXSF に移動し、そこでは yourD365FOdomain がこのトピックの [ドメイン名と DNS ゾーンの計画](#plandomain) セクションで定義したドメイン名です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-828">In your browser, navigate to https://[yourD365FOdomain]/namespaces/AXSF, where yourD365FOdomain is the domain name that you defined in the [Plan your domain name and DNS zones](#plandomain) section of this topic.</span></span>

## <a name="known-issues"></a><span data-ttu-id="7bf0f-829">既知の問題</span><span class="sxs-lookup"><span data-stu-id="7bf0f-829">Known issues</span></span>

### <a name="error-key-does-not-exist-when-running-the-new-d365fogmsaaccounts-cmdlet"></a><span data-ttu-id="7bf0f-830">New-D365FOGMSAAccounts cmdlet を実行した際のエラー、「キーが存在しません」</span><span class="sxs-lookup"><span data-stu-id="7bf0f-830">Error "Key does not exist" when running the New-D365FOGMSAAccounts cmdlet</span></span>
<span data-ttu-id="7bf0f-831">ドメインでグループ管理サービス アカウント パスワードを初めて作成し生成する場合は、最初に**キー配分サービス KDS ルート キー**を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-831">If this is your first time creating and generating group Managed Service Account passwords in your domain, you need to first create the **Key Distribution Services KDS Root Key**.</span></span> <span data-ttu-id="7bf0f-832">詳細については、[キー配分サービス KDS ルート キーの作成](https://docs.microsoft.com/en-us/windows-server/security/group-managed-service-accounts/create-the-key-distribution-services-kds-root-key)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-832">For more information, see [Create the Key Distribution Services KDS Root Key](https://docs.microsoft.com/en-us/windows-server/security/group-managed-service-accounts/create-the-key-distribution-services-kds-root-key).</span></span>

### <a name="error-the-winrm-client-cannot-process-the-request-when-running-the-remoting-script-configure-prereqs-allvms-cmdlet"></a><span data-ttu-id="7bf0f-833">リモート処理スクリプト Configure-Prereqs-AllVms cmdlet を実行した際のエラー、「WinRM クライアントは要求を処理できません」</span><span class="sxs-lookup"><span data-stu-id="7bf0f-833">Error "The WinRM client cannot process the request" when running the remoting script Configure-Prereqs-AllVms cmdlet</span></span>
<span data-ttu-id="7bf0f-834">Service Fabirc クラスターのすべてのマシンでコンピューター ポリシー**新しい資格情報委任を許可**を有効にするには、エラー メッセージの指示に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-834">You need to follow the instructions in the error message to enable the computer policy **Allow delegation fresh credentials** in all machines of Service Fabirc cluster.</span></span>

### <a name="error-not-process-argument-transformation-on-parameter-test-cannot-convert-value-systemstring-to-type-systemmanagementautomationswitchparameter-when-running-the-config-prereqs-allvms-cmdlet"></a><span data-ttu-id="7bf0f-835">エラー、「'テスト'パラメータでの引数変換を処理できません」</span><span class="sxs-lookup"><span data-stu-id="7bf0f-835">Error "Not process argument transformation on parameter 'Test'.</span></span> <span data-ttu-id="7bf0f-836">Config-Prereqs-AllVms cmdlet 実行時、値 "System.String" を、タイプ "System.Management.Automation.SwitchParameter" に変換することはできません</span><span class="sxs-lookup"><span data-stu-id="7bf0f-836">Cannot convert value "System.String" to type "System.Management.Automation.SwitchParameter" when running the Config-Prereqs-AllVms cmdlet</span></span>
<span data-ttu-id="7bf0f-837">このエラーを回避するには、**インフラストラクチャ** フォルダーにある Config-Prereqs-AllVms.ps1 の 56 行目の「-Test:$Test」を削除します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-837">To work around this error, remove "-Test:$Test" in line 56 of Config-Prereqs-AllVms.ps1, which is found under the **Infrastructure** folder.</span></span>

### <a name="error-not-process-argument-transformation-on-parameter-test-cannot-convert-value-systemstring-to-type-systemmanagementautomationswitchparameter-when-running-the-complete-prereqs-allvms-cmdlet"></a><span data-ttu-id="7bf0f-838">エラー、「'テスト'パラメータでの引数変換を処理できません」</span><span class="sxs-lookup"><span data-stu-id="7bf0f-838">Error "Not process argument transformation on parameter 'Test'.</span></span> <span data-ttu-id="7bf0f-839">Complete-Prereqs-AllVms cmdlet 実行時、値 "System.String" を、タイプ "System.Management.Automation.SwitchParameter" に変換することはできません</span><span class="sxs-lookup"><span data-stu-id="7bf0f-839">Cannot convert value "System.String" to type "System.Management.Automation.SwitchParameter" when running the Complete-Prereqs-AllVms cmdlet</span></span>
<span data-ttu-id="7bf0f-840">このエラーを回避するには、**インフラストラクチャ** フォルダーにある Complete-Prereqs-AllVms.ps1 の 56、61、66 行目の「-Test:$Test」を削除します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-840">To work around this error, remove "-Test:$Test" in line 56, 61 and 66 of Complete-Prereqs-AllVms.ps1 which is found under the **Infrastructure** folder.</span></span>

### <a name="error-install-windowsfeature-the-request-to-add-or-remove-features-on-the-specified-server-failed-when-running-configure-prereqs-on-mrtype-and-reportservertyoe-servers"></a><span data-ttu-id="7bf0f-841">MRType および ReportServerTyoe サーバーで Configure-Prereqs を実行した際のエラー、「Install-WindowsFeature: 指定されたサーバーへの機能の追加または削除の要求に失敗しました」</span><span class="sxs-lookup"><span data-stu-id="7bf0f-841">Error "Install-WindowsFeature: The request to add or remove features on the specified server failed" when running Configure-Prereqs on MRType and ReportServerTyoe servers</span></span>
<span data-ttu-id="7bf0f-842">.NET Framework 3.5 には、MRType および ReportServerType サーバーが必要です。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-842">.NET Framework 3.5 is required in MRType and ReportServerType servers.</span></span> <span data-ttu-id="7bf0f-843">ただし、既定では .NET Framework 3.5 ソース ファイルは Windows Server 2016 インストールに含まれていません。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-843">By default however, .NET Framework 3.5 source files aren't included in your Windows Server 2016 installation.</span></span> <span data-ttu-id="7bf0f-844">このエラーを回避するには、サーバー マネージャーによって新機能を手動で追加するときに**ソース** オプションを使用してインストールし、ソース ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-844">To work around this error, install it and specify the source files using the **source** option when you manually add new features by server manager.</span></span>

### <a name="error-msis7628-scope-names-should-be-a-valid-scope-description-name-in-ad-fs-configuration-when-running-the-publish-adfsapplicationgroup-cmdlet"></a><span data-ttu-id="7bf0f-845">Publish-ADFSApplicationGroup cmdlet を実行した際のエラー、「MSIS7628: スコープ名は AD FS コンフィギュレーションで有効なスコープ説明でなければなりません」</span><span class="sxs-lookup"><span data-stu-id="7bf0f-845">Error "MSIS7628: Scope names should be a valid Scope description name in AD FS configuration" when running the Publish-ADFSApplicationGroup cmdlet</span></span>
<span data-ttu-id="7bf0f-846">このエラーは D365FO-OP-ADFSApplicationGroup で必要とされる OpenID スコープ **allatclaims** が原因で表示されます。ただし、一部の Windows Server 2016 インストールでは表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-846">This error occurs because of an OpenID scope **allatclaims** that is required by the D365FO-OP-ADFSApplicationGroup, but it might be missing in some Windows Server 2016 installation.</span></span> <span data-ttu-id="7bf0f-847">このエラーを回避するには、AD FS Management\Service\Scope Descriptions を使用してスコープの説明 **allatclaims** を追加します。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-847">To work around this error, add the scope description **allatclaims** through AD FS Management\Service\Scope Descriptions.</span></span>

### <a name="error-admin0077-access-control-policy-does-not-exist-permit-everyone-when-running-the-publish-adfsapplicationgroup-cmdlet"></a><span data-ttu-id="7bf0f-848">Publish-ADFSApplicationGroup cmdletを実行した際のエラー、「ADMIN0077: アクセス制御ポリシーが存在しません: すべてのユーザーを許可」</span><span class="sxs-lookup"><span data-stu-id="7bf0f-848">Error "ADMIN0077: Access control policy does not exist: Permit everyone" when running the Publish-ADFSApplicationGroup cmdlet</span></span>
<span data-ttu-id="7bf0f-849">英語以外のバージョンの Windows Server 2016 と共に AD FS をインストールすると、すべてのユーザーのアクセス許可のアクセス許可ポリシーがローカル言語で作成されます。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-849">When your AD FS is installed with a non-English version of Windows Server 2016, the permit everyone access control policy is created with your local language.</span></span> <span data-ttu-id="7bf0f-850">AccessControlPolicyName パラメーターを指定することによりコマンドレットを呼び出します: .\Publish-ADFSApplicationGroup.ps1 - HostUrl 'https://ax.d365ffo.onprem.contoso.com' - AccessControlPolicyName '<Permit everyone access control policy in your language>'。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-850">Invoke the cmdlet by specifying AccessControlPolicyName parameter as: .\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com' -AccessControlPolicyName '<Permit everyone access control policy in your language>'.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="7bf0f-851">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="7bf0f-851">Additional resources</span></span>
- [<span data-ttu-id="7bf0f-852">オンプレミス配置への更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="7bf0f-852">Apply updates to an on-premises deployment</span></span>](apply-updates-on-premises.md)
- [<span data-ttu-id="7bf0f-853">オンプレミス配置の再配置</span><span class="sxs-lookup"><span data-stu-id="7bf0f-853">Redeploy an on-premises deployment</span></span>](redeploy-on-prem.md)

