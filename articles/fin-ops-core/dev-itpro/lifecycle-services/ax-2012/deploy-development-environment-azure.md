---
title: Azure での開発環境の配置
description: このトピックでは、Microsoft Azure での開発環境の展開方法について説明します。
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 17591
ms.assetid: eaef3391-e5fe-43f9-98d9-db9fb6951363
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: c36db050438fec57495f59b0c16911add6710130
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983610"
---
# <a name="deploy-development-environments-on-azure"></a><span data-ttu-id="aef41-103">Azure での開発環境の配置</span><span class="sxs-lookup"><span data-stu-id="aef41-103">Deploy development environments on Azure</span></span>

[!include [banner](../../includes/banner.md)]

<a name="prerequisites"></a><span data-ttu-id="aef41-104">必要条件</span><span class="sxs-lookup"><span data-stu-id="aef41-104">Prerequisites</span></span>
-------------

<span data-ttu-id="aef41-105">このトピックの手順を実行する前に、次の条件が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="aef41-105">Before you complete the procedures in this topic, make sure that the following prerequisites are in place.</span></span>

|                |                                                                                                                                                                 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef41-106">**カテゴリ**</span><span class="sxs-lookup"><span data-stu-id="aef41-106">**Category**</span></span>   | <span data-ttu-id="aef41-107">**前提条件**</span><span class="sxs-lookup"><span data-stu-id="aef41-107">**Prerequisite**</span></span>                                                                                                                                                |
| <span data-ttu-id="aef41-108">必要なタスク</span><span class="sxs-lookup"><span data-stu-id="aef41-108">Required tasks</span></span> | [<span data-ttu-id="aef41-109">Azure で AX 2012 R3 の配置を計画する</span><span class="sxs-lookup"><span data-stu-id="aef41-109">Plan AX 2012 R3 deployments on Azure</span></span>](plan-2012-r3-deployment-azure.md) |

## <a name="1-log-on-to-lifecycle-services"></a><span data-ttu-id="aef41-110">1. ライフサイクル サービスにログオンする</span><span class="sxs-lookup"><span data-stu-id="aef41-110">1. Log on to Lifecycle Services</span></span>
<span data-ttu-id="aef41-111">Microsoft Dynamics Lifecycle Services は、顧客およびパートナーが Microsoft Dynamics AX の管理に使用できるクラウドベースの共同ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="aef41-111">Microsoft Dynamics Lifecycle Services provides a cloud-based collaborative workspace that customers and partners can use to manage Microsoft Dynamics AX projects.</span></span> <span data-ttu-id="aef41-112">Azure に AX 2012 R3 を配置するには、この Web サイトを使用します。</span><span class="sxs-lookup"><span data-stu-id="aef41-112">You’ll use this website to deploy AX 2012 R3 on Azure.</span></span> <span data-ttu-id="aef41-113">Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="aef41-113">Lifecycle Services is available to customers and partners as part of their support plans.</span></span> <span data-ttu-id="aef41-114">CustomerSource または PartnerSource の資格情報でアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="aef41-114">You can access it with your CustomerSource or PartnerSource credentials.</span></span> [<span data-ttu-id="aef41-115">Lifecycle Services にログオン</span><span class="sxs-lookup"><span data-stu-id="aef41-115">Log on to Lifecycle Services</span></span>](https://lcs.dynamics.com/en/)

## <a name="2-create-a-project"></a><span data-ttu-id="aef41-116">2. プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="aef41-116">2. Create a project</span></span>
<span data-ttu-id="aef41-117">Lifecycle Services にログインした後、既存のプロジェクトを開くか、または新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="aef41-117">After you log in to Lifecycle Services, open an existing project, or create a new project.</span></span> <span data-ttu-id="aef41-118">プロジェクトは、Lifecycle Services でのエクスペリエンスの主な開催者です。</span><span class="sxs-lookup"><span data-stu-id="aef41-118">Projects are the key organizer of your experience in Lifecycle Services.</span></span> <span data-ttu-id="aef41-119">プロジェクトに関連する手法は、既定でプロジェクトに含まれるフェーズとタスクを決定します。</span><span class="sxs-lookup"><span data-stu-id="aef41-119">The methodology associated with a project determines which phases and tasks are included in the project by default.</span></span>

## <a name="3-connect-the-project-to-your-azure-subscription"></a><span data-ttu-id="aef41-120">3. Azure サブスクリプションにプロジェクトを接続する</span><span class="sxs-lookup"><span data-stu-id="aef41-120">3. Connect the project to your Azure subscription</span></span>
<span data-ttu-id="aef41-121">Azure サブスクリプションに Lifecycle Services プロジェクトを接続します。</span><span class="sxs-lookup"><span data-stu-id="aef41-121">Connect the Lifecycle Services project to your Azure subscription.</span></span> <span data-ttu-id="aef41-122">これにより、Lifecycle Services は AX 2012 R3 環境をサブスクリプションに展開できます。</span><span class="sxs-lookup"><span data-stu-id="aef41-122">This will enable Lifecycle Services to deploy an AX 2012 R3 environment to the subscription.</span></span> <span data-ttu-id="aef41-123">Azure サブスクリプションにプロジェクトを接続するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="aef41-123">To connect the project to your Azure subscription, complete the following procedure.</span></span> <span data-ttu-id="aef41-124">プロジェクトは 1 つの Azure サブスクリプションにだけ接続できることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-124">Keep in mind that a project can be connected to only one Azure subscription.</span></span> <span data-ttu-id="aef41-125">複数の Azure サブスクリプションがある場合、この手順を実行する前にどのサブスクリプションを使用するかを必ず識別します。</span><span class="sxs-lookup"><span data-stu-id="aef41-125">If you have multiple Azure subscriptions, be sure to identify which subscription you want to use before you complete this procedure.</span></span>

1.  <span data-ttu-id="aef41-126">**クラウド ホスト環境**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-126">Click **Cloud-hosted environments**.</span></span> <span data-ttu-id="aef41-127">**クラウド ホスト環境** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-127">The **Cloud-hosted environments** page is displayed.</span></span>
2.  <span data-ttu-id="aef41-128">**Microsoft Azure 設定**パネルが画面の横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-128">The **Microsoft Azure setup** panel is displayed on the side of the screen.</span></span> <span data-ttu-id="aef41-129">表示されない場合は、**Microsoft Azure 設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-129">If it is not displayed, click **Microsoft Azure settings**.</span></span>
3.  <span data-ttu-id="aef41-130">Azure サブスクリプション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="aef41-130">Enter your Azure subscription ID.</span></span> <span data-ttu-id="aef41-131">サブスクリプション ID を検索する必要がある場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="aef41-131">If you need to find your subscription ID, complete the following steps:</span></span>
    1.  <span data-ttu-id="aef41-132">ブラウザの別のインスタンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="aef41-132">Open another instance of your browser.</span></span>
    2.  <span data-ttu-id="aef41-133">**Azure 管理ポータル**にログオンします。</span><span class="sxs-lookup"><span data-stu-id="aef41-133">Log on to the **Azure management portal**.</span></span>
    3.  <span data-ttu-id="aef41-134">左のナビゲーション ウィンドウで、**設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-134">In the navigation pane on the left, click **Settings**.</span></span> <span data-ttu-id="aef41-135">(設定リンクを表示するには、ナビゲーションペインの一番下までスクロールしなければならない場合があります。) **Settings** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-135">(You may have to scroll to the bottom of the navigation pane to see the Settings link.) The **Settings** page is displayed.</span></span>
    4.  <span data-ttu-id="aef41-136">サブスクリプション ID をコピーして、Lifecycle Services の **Azure サブスクリプション ID** フィールドに貼り付けます (現在別のブラウザー インスタンスに表示されています)。</span><span class="sxs-lookup"><span data-stu-id="aef41-136">Copy your subscription ID, and then paste it into the **Azure subscription ID** field in Lifecycle Services (which is currently displayed in another browser instance).</span></span>

4.  <span data-ttu-id="aef41-137">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-137">Click **Next**.</span></span>
5.  <span data-ttu-id="aef41-138">**ダウンロード**をクリックして管理証明書をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="aef41-138">Click **Download** to download a management certificate.</span></span> <span data-ttu-id="aef41-139">この管理証明書により、Lifecycle Services はお客様の代わりに Azure と通信できます。</span><span class="sxs-lookup"><span data-stu-id="aef41-139">This management certificate enables Lifecycle Services to communicate with Azure on your behalf.</span></span> <span data-ttu-id="aef41-140">既定では、管理証明書はコンピューターのダウンロード フォルダーに保存され、LifecycleServicesDeployment.cer という名前が付きます。</span><span class="sxs-lookup"><span data-stu-id="aef41-140">By default, the management certificate is saved to the Downloads folder on your computer and is named LifecycleServicesDeployment.cer.</span></span>
6.  <span data-ttu-id="aef41-141">管理証明書を Azure にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="aef41-141">Upload the management certificate to Azure.</span></span> <span data-ttu-id="aef41-142">そのためには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="aef41-142">To do so, complete the following steps:</span></span>
    1.  <span data-ttu-id="aef41-143">ブラウザの別のインスタンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="aef41-143">Open another instance of your browser.</span></span> <span data-ttu-id="aef41-144">(または、手順 3 で開いた可能性のあるブラウザインスタンスに移動します。)</span><span class="sxs-lookup"><span data-stu-id="aef41-144">(Or, go to the browser instance that you may have opened in step 3.)</span></span>
    2.  <span data-ttu-id="aef41-145">**Azure 管理ポータル**にログオンします。</span><span class="sxs-lookup"><span data-stu-id="aef41-145">Log on to the **Azure management portal**.</span></span>
    3.  <span data-ttu-id="aef41-146">左のナビゲーション ウィンドウで、**設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-146">In the navigation pane on the left, click **Settings**.</span></span> <span data-ttu-id="aef41-147">**設定** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-147">The **Settings** page is displayed.</span></span>
    4.  <span data-ttu-id="aef41-148">**管理証明書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-148">Click **Management certificates**.</span></span>
    5.  <span data-ttu-id="aef41-149">ページの下部にある**アップロード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-149">Click **Upload** at the bottom of the page.</span></span>
    6.  <span data-ttu-id="aef41-150">**管理証明書をアップロード** ウィンドウで、手順 5 でダウンロードした管理証明書を参照します。</span><span class="sxs-lookup"><span data-stu-id="aef41-150">In the **Upload a management certificate** window, browse to the management certificate that you downloaded in step 5.</span></span> <span data-ttu-id="aef41-151">その後、チェック マークをクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-151">Then click the check mark.</span></span>

7.  <span data-ttu-id="aef41-152">Lifecycle Services で **Microsoft Azure 設定**パネルを表示するブラウザーに戻ります。</span><span class="sxs-lookup"><span data-stu-id="aef41-152">Go back to the browser that displays the **Microsoft Azure setup** panel in Lifecycle Services.</span></span> <span data-ttu-id="aef41-153">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-153">Click **Next**.</span></span>
8.  <span data-ttu-id="aef41-154">最も近い地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="aef41-154">Select the region that is closest to you.</span></span> <span data-ttu-id="aef41-155">AX 2012 R3 環境は、この領域のデータ センターに配置されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-155">The AX 2012 R3 environment will be deployed to a datacenter in this region.</span></span>
9.  <span data-ttu-id="aef41-156">**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-156">Click **Connect**.</span></span> <span data-ttu-id="aef41-157">これで、プロジェクトが指定された Azure サブスクリプションに接続できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="aef41-157">The project is now connected to the Azure subscription that you specified.</span></span> <span data-ttu-id="aef41-158">プロジェクトを間違った Azure サブスクリプション (複数の Azure サブスクリプションがあると仮定した場合) に接続していることが分かった場合、プロジェクトを削除し、新しいプロジェクトを作成し、新しいプロジェクトを適切な Azure サブスクリプションに接続させるためのこの手順を繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-158">If you discover that you connected the project to the wrong Azure subscription (that is, assuming you have multiple Azure subscriptions), you’ll need to delete the project, create a new project, and then repeat this procedure to connect the new project to the appropriate Azure subscription.</span></span>

## <a name="4-connect-your-corporate-network-to-the-azure-virtual-network"></a><span data-ttu-id="aef41-159">4. 会社のネットワークを Azure 仮想ネットワークに接続する</span><span class="sxs-lookup"><span data-stu-id="aef41-159">4. Connect your corporate network to the Azure virtual network</span></span>
<span data-ttu-id="aef41-160">次のセクションでは、企業ユーザーが AX 2012 R3 にアクセスできるように、Azure 仮想ネットワークとドメインを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aef41-160">The following sections provide information about how to configure the Azure virtual network and domain so that your corporate users can access AX 2012 R3.</span></span> <span data-ttu-id="aef41-161">企業の資格情報を使用してこれらのシステムにログインする必要がある場合、環境を配置する前に接続を設定することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="aef41-161">It is recommended that if you require login to these systems using corporate credentials that you set up the connectivity before you deploy the environment.</span></span> <span data-ttu-id="aef41-162">これには、Azure のネットワーク機能を使用して企業ネットワークを 1 つ以上の Azure 仮想ネットワークに拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-162">This will require using Azure networking capabilities to extend you corporate network to one or more Azure virtual networks.</span></span> <span data-ttu-id="aef41-163">さらに、Azure 仮想ネットワークに Active Directory を配置する必要があり、これは会社の Active Directory に対する信頼のために設定されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-163">It will additionally require you to deploy an Active Directory into the Azure virtual network, which will be set up for trust to your corporate Active Directory.</span></span> <span data-ttu-id="aef41-164">この Active Directory は、Azure 仮想ネットワーク内の VM 関連リソースを管理するために適用されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-164">This Active Directory will be used to manage VM-related resources in the Azure virtual network.</span></span> <span data-ttu-id="aef41-165">この Active Directory はシングルサインオンには使用されません。社内ディレクトリを同期するように設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="aef41-165">This Active Directory will not be used for single sign-on, and should not be set up to sync the corporate directory.</span></span> <span data-ttu-id="aef41-166">シングル サインオン機能は、ドメインの信頼関係を通じて提供されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-166">Single sign-on capabilities will be provided through the domain trust.</span></span>

### <a name="create-a-site-to-site-vpn-connection"></a><span data-ttu-id="aef41-167">サイト間 VPN 接続を作成する</span><span class="sxs-lookup"><span data-stu-id="aef41-167">Create a site-to-site VPN connection</span></span>

<span data-ttu-id="aef41-168">企業ユーザーが Azure 仮想ネットワーク内の仮想マシンのリソースにアクセスできるようにするには、Azure 仮想ネットワークとオンプレミス社内ネットワークの間にサイト間 VPN 接続を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-168">To enable corporate users to access resources on the virtual machines in the Azure virtual network, you’ll need to create a site-to-site VPN connection between the Azure virtual network and your on-premises, corporate network.</span></span> <span data-ttu-id="aef41-169">これを行う方法の詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-169">For information about how to do this, see:</span></span>

-   [<span data-ttu-id="aef41-170">仮想ネットワークの概要</span><span class="sxs-lookup"><span data-stu-id="aef41-170">Virtual network overview</span></span>](https://msdn.microsoft.com/library/windowsazure/jj156007.aspx)
-   [<span data-ttu-id="aef41-171">仮想ネットワークのコンフィギュレーション タスク</span><span class="sxs-lookup"><span data-stu-id="aef41-171">Virtual network configuration tasks</span></span>](https://msdn.microsoft.com/library/jj156206.aspx)
-   [<span data-ttu-id="aef41-172">テスト用にシミュレーションしたハイブリッド クラウド環境を設定する</span><span class="sxs-lookup"><span data-stu-id="aef41-172">Set up a simulated hybrid cloud environment for testing</span></span>](https://azure.microsoft.com/documentation/articles/virtual-networks-setup-simulated-hybrid-cloud-environment-testing/)
-   [<span data-ttu-id="aef41-173">Windows Server 2012 ルーティングおよびリモート アクセスサービス (RRAS) を使用した Azure 仮想ネットワークのサイト間 VPN</span><span class="sxs-lookup"><span data-stu-id="aef41-173">Site-to-site VPN in Azure virtual network using Windows Server 2012 Routing and Remote Access Service (RRAS)</span></span>](https://msdn.microsoft.com/library/dn636917.aspx)
-   [<span data-ttu-id="aef41-174">管理ポータルに仮想ネットワーク ゲートウェイを構成する</span><span class="sxs-lookup"><span data-stu-id="aef41-174">Configure a virtual network gateway in the management portal</span></span>](https://msdn.microsoft.com/library/azure/jj156210.aspx)

### <a name="create-an-active-directory-in-azure"></a><span data-ttu-id="aef41-175">Azure の Active Directory アカウントの作成</span><span class="sxs-lookup"><span data-stu-id="aef41-175">Create an active directory in Azure</span></span>

<span data-ttu-id="aef41-176">Active Directory は Azure 仮想ネットワークに必須です。</span><span class="sxs-lookup"><span data-stu-id="aef41-176">An Active Directory is required in the Azure virtual network.</span></span> <span data-ttu-id="aef41-177">Active Directory は Azure 仮想ネットワークに配置できます。</span><span class="sxs-lookup"><span data-stu-id="aef41-177">An Active Directory can be deployed to the Azure virtual network.</span></span> <span data-ttu-id="aef41-178">[Azure 仮想マシンに Windows Server Active Directory を展開するためのガイドライン](https://msdn.microsoft.com/library/azure/jj156090.aspx)に従ってください。</span><span class="sxs-lookup"><span data-stu-id="aef41-178">Please follow [Guidelines for Deploying Windows Server Active Directory on Azure Virtual Machines](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span> <span data-ttu-id="aef41-179">Active Directory フェデレーション サービスは現在 AX 2012 R3 でサポートされていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-179">Please note that Active Directory Federation Services is not presently supported with AX 2012 R3.</span></span> <span data-ttu-id="aef41-180">Active Directory を提供する場合は、LCS 展開サービスで使用できる範囲で次のサービス アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-180">If you are providing the Active Directory, you will need to create the following service accounts within it that can be used by LCS deployment services when you deploy the environment.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aef41-181"><strong>勘定</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-181"><strong>Account</strong></span></span></td>
<td><span data-ttu-id="aef41-182"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-182"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aef41-183">&lt;DomainName&gt;AXServiceUser</span><span class="sxs-lookup"><span data-stu-id="aef41-183">&lt;DomainName&gt;AXServiceUser</span></span></td>
<td><span data-ttu-id="aef41-184">AX 2012 R3 サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="aef41-184">AX 2012 R3 service account</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aef41-185">&lt;DomainName&gt;AOSServiceUser</span><span class="sxs-lookup"><span data-stu-id="aef41-185">&lt;DomainName&gt;AOSServiceUser</span></span></td>
<td><span data-ttu-id="aef41-186">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="aef41-186">AOS service account</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aef41-187">&lt;DomainName&gt;BCProxyUser</span><span class="sxs-lookup"><span data-stu-id="aef41-187">&lt;DomainName&gt;BCProxyUser</span></span></td>
<td><span data-ttu-id="aef41-188">Business Connector プロキシ アカウント</span><span class="sxs-lookup"><span data-stu-id="aef41-188">Business Connector proxy account</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aef41-189">&lt;DomainName&gt;SPServiceUser</span><span class="sxs-lookup"><span data-stu-id="aef41-189">&lt;DomainName&gt;SPServiceUser</span></span></td>
<td><span data-ttu-id="aef41-190">SharePoint サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="aef41-190">SharePoint service account</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aef41-191">&lt;DomainName&gt;SqlServiceUser</span><span class="sxs-lookup"><span data-stu-id="aef41-191">&lt;DomainName&gt;SqlServiceUser</span></span></td>
<td><span data-ttu-id="aef41-192">SQL Server サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="aef41-192">SQL Server service account</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aef41-193">&lt;DomainName&gt;DynamicsInstallUser</span><span class="sxs-lookup"><span data-stu-id="aef41-193">&lt;DomainName&gt;DynamicsInstallUser</span></span></td>
<td><span data-ttu-id="aef41-194">AX 2012 R3 インストール アカウント</span><span class="sxs-lookup"><span data-stu-id="aef41-194">AX 2012 R3 installation account</span></span> 

<span data-ttu-id="aef41-195">**注記:** このアカウントは、コンピューターをドメインに参加させるためのアクセス許可を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-195">**Note:** This account must have permission to join computers to the domain.</span></span> <span data-ttu-id="aef41-196">このアカウントにアクセス許可を与えるには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="aef41-196">To give this account permission, complete the following steps:</span></span>
<ol>
<li><span data-ttu-id="aef41-197"><strong>開始</strong>をクリックし、dsa.msc 型で<strong>実行</strong>をクリックし、 <strong>OK</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-197">Click <strong>Start</strong>, click <strong>Run</strong>, type dsa.msc, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="aef41-198">作業ウィンドウで、ドメイン ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="aef41-198">In the task pane, expand the domain node.</span></span></li>
<li><span data-ttu-id="aef41-199">変更する組織単位を検索し、右クリックしてから<strong>デリゲート コントロール</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-199">Locate and right-click the organizational unit that you want to modify, and then click <strong>Delegate Control</strong>.</span></span></li>
<li><span data-ttu-id="aef41-200"><strong>コントロールのデリゲート</strong> ウィザードで、<strong>次へ</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-200">In the <strong>Delegation of Control</strong> Wizard, click <strong>Next</strong>.</span></span></li>
<li><span data-ttu-id="aef41-201">特定のユーザーまたは特定のグループを一覧に追加するには、<strong>追加</strong>をクリックし、次に <strong>次へ</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-201">Click <strong>Add</strong> to add a specific user or a specific group to the list, and then click <strong>Next</strong>.</span></span></li>
<li><span data-ttu-id="aef41-202"><strong>委任するタスク</strong> ページで、<strong>委任するカスタム タスクを作成</strong>をクリックしてから、<strong>次へ</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-202">In the <strong>Tasks to Delegate</strong> page, click <strong>Create a custom task to delegate</strong>, and then click <strong>Next</strong>.</span></span></li>
<li><span data-ttu-id="aef41-203"><strong>フォルダ内の次のオブジェクトのみ</strong>をクリックし、一覧から<strong>コンピューター オブジェクト</strong> チェック ボックスをクリックして選択します。</span><span class="sxs-lookup"><span data-stu-id="aef41-203">Click <strong>Only the following objects in the folder</strong>, and then from the list, click to select the <strong>Computer objects</strong> check box.</span></span> <span data-ttu-id="aef41-204">その後、リスト下部で <strong>このフォルダーの選択したオブジェクトを作成する</strong> および <strong>このフォルダーの選択したオブジェクトを削除する</strong> の各チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="aef41-204">Then, select the check boxes below the list, <strong>Create selected objects in this folder</strong> and <strong>Delete selected objects in this folder</strong>.</span></span></li>
<li><span data-ttu-id="aef41-205"><strong>次へ</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-205">Click <strong>Next</strong>.</span></span></li>
<li><span data-ttu-id="aef41-206"><strong>アクセス許可</strong>リストで、次のチェック ボックスをクリックしてオンにします。</span><span class="sxs-lookup"><span data-stu-id="aef41-206">In the <strong>Permissions</strong> list, click to select the following check boxes:</span></span>
<ul>
<li><span data-ttu-id="aef41-207"><strong>パスワードのリセット</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-207"><strong>Reset Password</strong></span></span></li>
<li><span data-ttu-id="aef41-208"><strong>アカウントの制限の読み取りと書き込み</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-208"><strong>Read and write Account Restrictions</strong></span></span></li>
<li><span data-ttu-id="aef41-209"><strong>DNS ホスト名への検証済みの書き込み</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-209"><strong>Validated write to DNS host name</strong></span></span></li>
<li><span data-ttu-id="aef41-210"><strong>サービス プリンシパル名への検証済みの書き込み</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-210"><strong>Validated write to service principal name</strong></span></span></li>
</ul></li>
<li><span data-ttu-id="aef41-211"><strong>次へ</strong>をクリックし、<strong>完了</strong>の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-211">Click <strong>Next</strong>, and then click <strong>Finish</strong>.</span></span></li>
<li><span data-ttu-id="aef41-212"><strong>Active Directory ユーザーおよびコンピューター MMC スナップイン</strong>を閉じます。</span><span class="sxs-lookup"><span data-stu-id="aef41-212">Close the <strong>Active Directory Users and Computers MMC snap-in</strong>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

<span data-ttu-id="aef41-213">環境を配置するとき、これらのアカウントのパスワードを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-213">You will need to provide the passwords for these accounts when you deploy the environment.</span></span>

### <a name="create-a-domain-trust"></a><span data-ttu-id="aef41-214">ドメイン信頼の作成</span><span class="sxs-lookup"><span data-stu-id="aef41-214">Create a domain trust</span></span>

<span data-ttu-id="aef41-215">企業ユーザーが Azure ドメイン内の仮想マシンのリソースにアクセスできるようにするには、ドメイン間で Active Directory のトラストを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-215">To enable corporate users to access resources on the virtual machines in your Azure domain, you must create an Active Directory trust between the domains.</span></span> <span data-ttu-id="aef41-216">信託の作成方法の詳細については、「[フォレスト信託の作成](https://technet.microsoft.com/library/cc754626.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-216">For information about how to create a trust, see [Create a Forest Trust](https://technet.microsoft.com/library/cc754626.aspx).</span></span> <span data-ttu-id="aef41-217">このプロセスは、2 つのオンプレミス ドメイン間で信頼関係を作成する場合と同じプロセスです。</span><span class="sxs-lookup"><span data-stu-id="aef41-217">This process is the same process you would use to create a trust between two on-premises domains.</span></span>

### <a name="give-the-administrators-group-the-right-to-log-on-as-a-batch-job"></a><span data-ttu-id="aef41-218">バッチ ジョブとしてログオンする権限を管理者グループに付与します</span><span class="sxs-lookup"><span data-stu-id="aef41-218">Give the Administrators group the right to log on as a batch job</span></span>

<span data-ttu-id="aef41-219">Active Directory ドメイン コントローラーにログインし、次の手順を完了して、ビルトイン Administrator グループにバッチ ジョブとしてログオンする権利を付与します。</span><span class="sxs-lookup"><span data-stu-id="aef41-219">Log in to the Active Directory domain controller and complete the following steps to give the built-in Administrators group the right to log on as a batch job.</span></span>

1.  <span data-ttu-id="aef41-220">**開始**、**すべてのプログラム**の順にクリックし、**管理ツール**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-220">Click **Start**, click **All Programs**, and then click **Administrative Tools**.</span></span>
2.  <span data-ttu-id="aef41-221">**管理ツール** メニューで、**グループ ポリシーの管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="aef41-221">In the **Administrative Tools** menu, select **Group Policy Management**.</span></span>
3.  <span data-ttu-id="aef41-222">**グループ ポリシー管理**コンソール ツリーで、**フォレスト: &lt;ServerName&gt;** をクリックしてから、**ドメイン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-222">In the **Group Policy Management** console tree, click **Forest: &lt;ServerName&gt;**, and then click **Domains**.</span></span>
4.  <span data-ttu-id="aef41-223">サーバーの名前をクリックし、**ドメイン コントローラー**を展開します。**既定のドメイン コント ローラー ポリシー**を右クリックし、**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-223">Click the name of your server, expand **Domain Controllers**, right-click **Default Domain Controllers Policy**, and then click **Edit**.</span></span>
5.  <span data-ttu-id="aef41-224">**グループ ポリシー管理エディター**で、**既定のドメイン コントローラ ポリシー &lt; ServerName &gt; ポリシー**とクリックし、**コンピューターの構成**を展開してから**ポリシー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-224">In the **Group Policy Management Editor**, click **Default Domain Controllers Policy &lt;ServerName&gt; Policy**, expand **Computer Configuration**, and then click **Policies**.</span></span>
6.  <span data-ttu-id="aef41-225">**ポリシー** ツリーで、**Windows 設定**を展開してから**セキュリティの設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-225">In the **Policies** tree, expand **Windows Setting**, and then click **Security Settings**.</span></span>
7.  <span data-ttu-id="aef41-226">**セキュリティの設定**ツリーで、**ローカル ポリシー**を展開してから**ユーザーの権限の割り当て**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-226">In the **Security Settings** tree, expand **Local Policies**, and then click **User Rights Assignment**.</span></span>
8.  <span data-ttu-id="aef41-227">結果ウィンドウで、スクロールして**バッチ ジョブとしてログオン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-227">In the results pane, scroll to and then click **Log on as a batch job**.</span></span>
9.  <span data-ttu-id="aef41-228">**バッチ ジョブとしてログオン プロパティ** ダイアログ ボックスで、**ユーザーまたはグループの追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-228">In the **Log on as a batch job Properties** dialog box, click **Add User or Group**.</span></span>
10. <span data-ttu-id="aef41-229">**ユーザーまたはグループの追加**ダイアログ ボックスで、**参照**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-229">In the **Add User or Group** dialog box, click **Browse**.</span></span>
11. <span data-ttu-id="aef41-230">**ユーザー、コンピュータ、またはグループの選択**ダイアログ ボックスで、管理者と入力します。</span><span class="sxs-lookup"><span data-stu-id="aef41-230">In the **Select Users, Computers, or Groups** dialog box, type Administrators.</span></span>
12. <span data-ttu-id="aef41-231">**名前の確認**をクリックして、あらかじめ登録された Administrator アカウントが表示されていることを確認し、**OK** を 3 回クリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-231">Click **Check Names** to verify that the built-in Administrators account appears, and then click **OK** three times.</span></span>

### <a name="change-the-default-organizational-unit"></a><span data-ttu-id="aef41-232">既定の組織単位の変更</span><span class="sxs-lookup"><span data-stu-id="aef41-232">Change the default organizational unit</span></span>

<span data-ttu-id="aef41-233">仮想マシンをカスタム組織単位 (デフォルトの組織単位と比較して) の Active Directory に追加する場合は、展開を開始する前に Active Directory 内の既定の組織単位を変更できます。</span><span class="sxs-lookup"><span data-stu-id="aef41-233">If you want virtual machines to be added to Active Directory in a custom organizational unit—versus the default organizational unit—you can change the default organizational unit in your Active Directory prior to starting deployment.</span></span> <span data-ttu-id="aef41-234">詳細については、[ここ](http://pc-addicts.com/server-2012-change-default-ou/) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="aef41-234">For more information, click [here](http://pc-addicts.com/server-2012-change-default-ou/).</span></span>

## <a name="5-deploy-a-development-environment-on-azure"></a><span data-ttu-id="aef41-235">5. Azure での開発環境の配置</span><span class="sxs-lookup"><span data-stu-id="aef41-235">5. Deploy a development environment on Azure</span></span>
<span data-ttu-id="aef41-236">Azure に開発環境を配置するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="aef41-236">Complete the following procedure to deploy a development environment on Azure.</span></span>

1. <span data-ttu-id="aef41-237">**クラウド ホスト環境**ページで、追加 (+) アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-237">On the **Cloud-hosted environments** page, click the Add (+) icon.</span></span>
2. <span data-ttu-id="aef41-238">**環境のトポロジの選択**パネルで、**開発/テスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="aef41-238">In the **Select environment topology** panel, select **Dev/test**.</span></span>
3. <span data-ttu-id="aef41-239">**開発**または**共有 SQL Serverによる開発**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-239">Click **Development** or **Development with shared SQL Server**.</span></span>
4. <span data-ttu-id="aef41-240">**環境名**フィールドに、配置される環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="aef41-240">In the **Environment name** field, enter a name for the environment that will be deployed.</span></span>
5. <span data-ttu-id="aef41-241">**詳細設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-241">Click **Advanced settings**.</span></span>
6. <span data-ttu-id="aef41-242">ドメイン設定をカスタマイズするには、**ドメイン設定をカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-242">To customize domain settings, click **Customize domain settings**.</span></span> <span data-ttu-id="aef41-243">情報を入力するには、次の表を使用してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-243">Then use the following table to enter information.</span></span>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td><span data-ttu-id="aef41-244"><strong>以下を行う場合:</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-244"><strong>If you want to:</strong></span></span></td>
   <td><span data-ttu-id="aef41-245"><strong>手順</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-245"><strong>Do this:</strong></span></span></td>
   </tr>
   <tr class="even">
   <td><span data-ttu-id="aef41-246">Azure で環境用に新しいドメインを作成する</span><span class="sxs-lookup"><span data-stu-id="aef41-246">Create a new domain in Azure for the environment</span></span></td>
   <td><ol>
   <li><span data-ttu-id="aef41-247"><strong>新規ドメイン</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-247">Click <strong>New domain</strong>.</span></span></li>
   <li><span data-ttu-id="aef41-248">ドメイン名を入力します。</span><span class="sxs-lookup"><span data-stu-id="aef41-248">Enter a name for the domain.</span></span> <span data-ttu-id="aef41-249">既定では、ドメインは <em>contoso.com</em> と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="aef41-249">By default, the domain is named <em>contoso.com</em>.</span></span></li>
   </ol></td>
   </tr>
   <tr class="odd">
   <td><span data-ttu-id="aef41-250">Azure の既存のドメインへの環境の追加</span><span class="sxs-lookup"><span data-stu-id="aef41-250">Add the environment to an existing domain in Azure</span></span></td>
   <td><ol>
   <li><span data-ttu-id="aef41-251"><strong>既存のドメイン</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-251">Click <strong>Existing domain</strong>.</span></span></li>
   <li><span data-ttu-id="aef41-252">ドメイン名を入力します。</span><span class="sxs-lookup"><span data-stu-id="aef41-252">Enter the name of the domain.</span></span> <span data-ttu-id="aef41-253">たとえば、<em>contoso.com</em>。</span><span class="sxs-lookup"><span data-stu-id="aef41-253">For example, <em>contoso.com</em>.</span></span></li>
   </ol></td>
   </tr>
   </tbody>
   </table>

7. <span data-ttu-id="aef41-254">ドメインで作成されるサービス アカウントをカスタマイズするには、**サービス アカウントをカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-254">To customize the service accounts that will be created in the domain, click **Customize service accounts**.</span></span> <span data-ttu-id="aef41-255">展開の **詳細設定** オプションを通じてサービス アカウントやサービス アカウントのパスワードを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="aef41-255">Service accounts and/or service account passwords may be specified through the **Advanced Settings** option for a deployment.</span></span> <span data-ttu-id="aef41-256">どちらもが指定されていない場合は、既定の勘定が使用され、ランダムなパスワードが選択されています。</span><span class="sxs-lookup"><span data-stu-id="aef41-256">If neither is provided, default accounts are used and random passwords are selected.</span></span> <span data-ttu-id="aef41-257">次の機能は、企業のアカウントの命名規則とパスワードの規則を管理する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="aef41-257">Use these features when you want to maintain account naming and password rules for your corporation.</span></span> <span data-ttu-id="aef41-258">アカウントとパスワードのルール:</span><span class="sxs-lookup"><span data-stu-id="aef41-258">Account and password rules:</span></span>
   - <span data-ttu-id="aef41-259">有効なサービス名は、特殊文字を含まない 20 文字未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-259">A valid service name must be less than 20 characters with no special characters.</span></span>
   - <span data-ttu-id="aef41-260">有効なパスワードは 8 文字以上で、大文字、小文字、数字、および次の文字のうち少なくとも 1 つが含まれます: \['@", "!', '=', '\*'\] 次のような一般的なパスワードは使用できません: pass@word1</span><span class="sxs-lookup"><span data-stu-id="aef41-260">A valid password must be more than 8 characters and contain uppercase letters, lowercase letters, numbers, and at least one of the following characters: \['@", "!', '=', '\*'\] You can’t use common passwords, such as: pass@word1</span></span>

8. <span data-ttu-id="aef41-261">使用を希望する AX 2012 R3 のバージョンを選択するには、**サポートされているバージョン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-261">To select the version of AX 2012 R3 that you want use, click **Supported version**.</span></span> <span data-ttu-id="aef41-262">既定では、この環境の AX 2012 R3 CU8 バージョンが配置されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-262">By default, the AX 2012 R3 CU8 version of this environment will be deployed.</span></span> <span data-ttu-id="aef41-263">CU8 バージョンを使用しない場合は、**Dynamics ERP 2012 R3 RTM** をリストから選択します。</span><span class="sxs-lookup"><span data-stu-id="aef41-263">If you don’t want to use the CU8 version, select **Dynamics ERP 2012 R3 RTM** from the list.</span></span>
9. <span data-ttu-id="aef41-264">仮想マシン名をカスタマイズするには、**仮想マシン名をカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-264">To customize virtual machine names, click **Customize virtual machine names**.</span></span> <span data-ttu-id="aef41-265">一般的な IT 名前付けガイドラインをサポートするために、仮想マシンに名前を付ける機能がほとんどの配置トポロジの**詳細設定**に用意されています。</span><span class="sxs-lookup"><span data-stu-id="aef41-265">In order to support common IT naming guidelines, the ability to name virtual machines is provided through the **Advanced settings** option on most deployment topologies.</span></span> <span data-ttu-id="aef41-266">名前を定義することに加えて、各仮想マシン タイプに開始インデックスを選択できます。</span><span class="sxs-lookup"><span data-stu-id="aef41-266">In addition to defining the name, a starting index can be selected for each virtual machine type.</span></span> <span data-ttu-id="aef41-267">インデックスは、配置される仮想マシン タイプのインスタンスごとに増加します。</span><span class="sxs-lookup"><span data-stu-id="aef41-267">The index is incremented for each instance of the virtual machine type that is deployed.</span></span> <span data-ttu-id="aef41-268">仮想マシン名は 13 文字またはそれ以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-268">Virtual machine names must be 13 characters or less.</span></span> <span data-ttu-id="aef41-269">インデックスはマシン名とハイフン (-) で区切られ、その後に最大 2 桁のインデックスが続きます。</span><span class="sxs-lookup"><span data-stu-id="aef41-269">The index is separated from the machine name by a hyphen (-), followed by the index that supports a maximum of 2 digits.</span></span> <span data-ttu-id="aef41-270">例: ACustomVMName-99。仮想マシン インスタンスが最初の展開後に環境へ追加されると、展開サービスは中断した仮想マシン名のインクリメントを開始します。</span><span class="sxs-lookup"><span data-stu-id="aef41-270">Example: ACustomVMName-99 When virtual machine instances are added to an environment after the initial deployment, the deployment service will start incrementing the virtual machine name where it left off.</span></span> <span data-ttu-id="aef41-271">たとえば、2 で始まるインデックスを持つ 4 つの AOS 仮想マシンを展開する場合、最後の AOS インスタンス名は AOS-6 になります。</span><span class="sxs-lookup"><span data-stu-id="aef41-271">For example, if you deployed four AOS virtual machines with a starting index of 2, then the last AOS instance name will be AOS-6.</span></span> <span data-ttu-id="aef41-272">もう 2 つ AOS インスタンスを追加する場合は、AOS-7 と AOS 8 になります。</span><span class="sxs-lookup"><span data-stu-id="aef41-272">If you add two more AOS instances, they will be AOS-7 and AOS-8.</span></span> <span data-ttu-id="aef41-273">展開内の仮想マシン タイプの 1 つがカスタマイズされている場合は、すべての仮想マシン名をカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-273">If one of the virtual machine types in your deployment is customized, then all of the virtual machine names must be customized.</span></span> <span data-ttu-id="aef41-274">これは、仮想マシン名が誤って紛失してしまったため、長期的な展開が発生しないようにするためです。</span><span class="sxs-lookup"><span data-stu-id="aef41-274">This is done to ensure that a long deployment does not occur because a virtual machine name was accidentally missed.</span></span>
10. <span data-ttu-id="aef41-275">仮想ネットワークの設定をカスタマイズするには、<strong>仮想ネットワークをカスタマイズする</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-275">To customize virtual network settings, click <strong>Customize virtual network</strong>.</span></span> <span data-ttu-id="aef41-276">情報を入力するには、次の表を使用してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-276">Then use the following table to enter information.</span></span>
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="aef41-277"><strong>以下を行う場合:</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-277"><strong>If you want to:</strong></span></span></td>
    <td><span data-ttu-id="aef41-278"><strong>手順</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-278"><strong>Do this:</strong></span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="aef41-279">Azure で環境用に新しい仮想ネットワークを作成する</span><span class="sxs-lookup"><span data-stu-id="aef41-279">Create a new virtual network in Azure for the environment</span></span></td>
    <td><ol>
    <li><span data-ttu-id="aef41-280"><strong>新しい仮想ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-280">Click <strong>New virtual network</strong>.</span></span></li>
    <li><span data-ttu-id="aef41-281">仮想ネットワーク名を入力します。</span><span class="sxs-lookup"><span data-stu-id="aef41-281">Enter a name for the virtual network.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="aef41-282">Azure の既存の仮想ネットワークへの環境の追加</span><span class="sxs-lookup"><span data-stu-id="aef41-282">Add the environment to an existing virtual network in Azure</span></span></td>
    <td><ol>
    <li><span data-ttu-id="aef41-283"><strong>既存の仮想ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-283">Click <strong>Existing virtual network</strong>.</span></span></li>
    <li><span data-ttu-id="aef41-284">使用する既存の仮想ネットワークの名前を選択してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-284">Select the name of the existing virtual network that you want to use.</span></span></li>
    <li><span data-ttu-id="aef41-285"><strong>アドレス空間</strong> フィールドには、適切な値が自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-285">The <strong>Address space</strong> field will automatically display the appropriate value.</span></span> <span data-ttu-id="aef41-286">提供された値を選択します。</span><span class="sxs-lookup"><span data-stu-id="aef41-286">Select the provided value.</span></span></li>
    <li><span data-ttu-id="aef41-287"><strong>アプリケーション サブネット名</strong> フィールドには、使用可能なオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-287">The <strong>Application subnet name</strong> field will display available options.</span></span> <span data-ttu-id="aef41-288">Lifecycle Servicesによって以前に展開した広告に配置する場合は、選択した <em>APPNET</em> 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="aef41-288">If you are deploying to an AD that was previously deployed through Lifecycle Services, select the <em>APPNET</em> value.</span></span></li>
    <li><span data-ttu-id="aef41-289">Active Directory サブネットを入力する必要があり、ターゲットとする AD の Azure 管理ポータルにある Active Directory サブネット IP/範囲と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-289">The Active Directory subnet must be entered and match the Active Directory subnet IP/Range found in the Azure management portal for the AD you desire to target.</span></span>
    <ol>
    <li><span data-ttu-id="aef41-290"><a href="https://manage.windowsazure.com/">Azure 管理ポータル</a>にログオンします。</span><span class="sxs-lookup"><span data-stu-id="aef41-290">Log on to the <a href="https://manage.windowsazure.com/">Azure management portal</a>.</span></span></li>
    <li><span data-ttu-id="aef41-291">左のナビゲーション ウィンドウで、<strong>ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-291">In the navigation pane on the left, click <strong>Networks</strong>.</span></span></li>
    <li><span data-ttu-id="aef41-292">使用する仮想ネットワークの名前をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-292">Click the name of the virtual network that you’re going to use.</span></span></li>
    <li><span data-ttu-id="aef41-293"><strong>構成</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-293">Click <strong>Configure</strong>.</span></span> <span data-ttu-id="aef41-294">仮想ネットワークに関する詳細は、ページに記載されています。</span><span class="sxs-lookup"><span data-stu-id="aef41-294">Details about the virtual network are listed on the page.</span></span></li>
    </ol></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

11. <span data-ttu-id="aef41-295">**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-295">Click **Done.**</span></span> <span data-ttu-id="aef41-296">**環境の展開** パネルが再表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-296">The **Deploy environment** panel is redisplayed.</span></span>
12. <span data-ttu-id="aef41-297">配置される仮想マシンの数とサイズが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-297">The number and size of each virtual machine that will be deployed is listed.</span></span> <span data-ttu-id="aef41-298">必要に応じて、仮想マシンの数とサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="aef41-298">Change the number and size of the virtual machines, as needed.</span></span>
    -   <span data-ttu-id="aef41-299">この環境で各仮想マシンにインストールされているソフトウェアの詳細については、 [Azure 上での AX 2012 R3の 配置計画](plan-2012-r3-deployment-azure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-299">For information about the software installed on each virtual machine in this environment, see [Plan AX 2012 R3 deployments on Azure](plan-2012-r3-deployment-azure.md).</span></span>
    -   <span data-ttu-id="aef41-300">仮想マシンに関するサイズおよび価格決定の詳細については、[仮想マシンの価格決定の詳細](https://azure.microsoft.com/pricing/details/virtual-machines/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-300">For sizing and pricing details about virtual machines, see [Virtual machines pricing details](https://azure.microsoft.com/pricing/details/virtual-machines/).</span></span>

13. <span data-ttu-id="aef41-301">ライセンスの条項を確認するには、**ソフトウェア ライセンス条項**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-301">Click **Software License Terms** to review the licensing terms and conditions.</span></span> <span data-ttu-id="aef41-302">次に、チェック ボックスを選択して、条件に同意することを示します。</span><span class="sxs-lookup"><span data-stu-id="aef41-302">Then select the check box to indicate that you agree to the terms.</span></span>
14. <span data-ttu-id="aef41-303">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef41-303">Click **Next**.</span></span>
15. <span data-ttu-id="aef41-304">**展開**をクリックして、環境を展開する準備が整ったことを確認します。</span><span class="sxs-lookup"><span data-stu-id="aef41-304">Click **Deploy** to confirm that you’re ready to deploy the environment.</span></span> <span data-ttu-id="aef41-305">配置には数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-305">The deployment may take a few hours to complete.</span></span> <span data-ttu-id="aef41-306">配置が完了すると、**クラウド ホスト環境** ページの **配置ステータス** 列に **配置済み** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-306">When the deployment is done, the **Deployment Status** column on the **Cloud-hosted environments** page will display **Deployed**.</span></span> <span data-ttu-id="aef41-307">(これを表示するにはブラウザーを更新する必要があります。) 配置が失敗すると、すぐエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-307">(You may need to refresh your browser to see this.) If the deployment fails, you may see an error message right away.</span></span> <span data-ttu-id="aef41-308">配置プロセスでエラーが後に発生する場合に、エラーの詳細がページの右側の詳細ペインに表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-308">If the error occurs later in the deployment process, error details will be displayed in the details pane on the right-side of the page.</span></span>

## <a name="6-prepare-ax-2012-r3-for-use"></a><span data-ttu-id="aef41-309">6. 使用する AX 2012 R3 の準備</span><span class="sxs-lookup"><span data-stu-id="aef41-309">6. Prepare AX 2012 R3 for use</span></span>
<span data-ttu-id="aef41-310">環境が Azure に配置されたので、使用するために AX 2012 R3 を設定し、コンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-310">Now that the environment has been deployed on Azure, you must set up and configure AX 2012 R3 for use.</span></span> <span data-ttu-id="aef41-311">詳細については、以降のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-311">See the following sections for more information.</span></span>

### <a name="log-on-to-the-aos-virtual-machine"></a><span data-ttu-id="aef41-312">AOS 仮想マシンへのログオン</span><span class="sxs-lookup"><span data-stu-id="aef41-312">Log on to the AOS virtual machine</span></span>

<span data-ttu-id="aef41-313">AOS-&lt;GUID&gt; 仮想マシンに &lt;DomainName&gt;DynamicsInstallUser アカウントを使用してログオンします。</span><span class="sxs-lookup"><span data-stu-id="aef41-313">Log on to the AOS-&lt;GUID&gt; virtual machine using the &lt;DomainName&gt;DynamicsInstallUser account.</span></span> <span data-ttu-id="aef41-314">手順については、「仮想マシンにどのようにログオンしますか?」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-314">For instructions, see the “How do I log on to a virtual machine?”</span></span> <span data-ttu-id="aef41-315">[Azure で AX 2012 R3 配置を管理する](manage-2012-r3-deployment-azure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-315">section of the [Manage AX 2012 R3 deployments on Azure](manage-2012-r3-deployment-azure.md) article.</span></span>

### <a name="compile-ax-2012-r3"></a><span data-ttu-id="aef41-316">AX 2012 R3 のコンパイル</span><span class="sxs-lookup"><span data-stu-id="aef41-316">Compile AX 2012 R3</span></span>

<span data-ttu-id="aef41-317">AxBuild.exe. を使用した AX 2012 R3 のコンパイル</span><span class="sxs-lookup"><span data-stu-id="aef41-317">Compile AX 2012 R3 by using AxBuild.exe.</span></span> <span data-ttu-id="aef41-318">手順については、[X++ から P コードへの AOS の並列コンパイルに対する AxBuild.exe](https://technet.microsoft.com/library/dn528954.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-318">For instructions, see [AxBuild.exe for Parallel Compile on AOS of X++ to p-code](https://technet.microsoft.com/library/dn528954.aspx).</span></span>

### <a name="initailize-ax-2012-r3"></a><span data-ttu-id="aef41-319">AX 2012 R3 の初期化</span><span class="sxs-lookup"><span data-stu-id="aef41-319">Initailize AX 2012 R3</span></span>

<span data-ttu-id="aef41-320">AX 2012 R3 クライアントを開いて、初期化チェックリストを完了します。</span><span class="sxs-lookup"><span data-stu-id="aef41-320">Open the AX 2012 R3 client and complete the initialization checklists.</span></span> <span data-ttu-id="aef41-321">手順については、[初期化チェックリスト](https://technet.microsoft.com/library/aa497061.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-321">For instructions, see [Initialization checklists](https://technet.microsoft.com/library/aa497061.aspx).</span></span>

### <a name="install-sample-data"></a><span data-ttu-id="aef41-322">サンプル データのインストール</span><span class="sxs-lookup"><span data-stu-id="aef41-322">Install sample data</span></span>

<span data-ttu-id="aef41-323">サンプル データを環境にインストールする場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="aef41-323">If you want sample data installed in your environment, complete the following steps.</span></span>

1.  <span data-ttu-id="aef41-324">SQL-&lt;GUID&gt; 仮想マシンにログオンします。</span><span class="sxs-lookup"><span data-stu-id="aef41-324">Log on to the SQL-&lt;GUID&gt; virtual machine.</span></span> <span data-ttu-id="aef41-325">DynamicsInstallUser アカウントを使用して仮想マシンにログオンします。</span><span class="sxs-lookup"><span data-stu-id="aef41-325">Log on to the virtual machine using the DynamicsInstallUser account.</span></span> <span data-ttu-id="aef41-326">手順については、「仮想マシンにどのようにログオンしますか?」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-326">For instructions, see the “How do I log on to a virtual machine?”</span></span> <span data-ttu-id="aef41-327">[Azure で AX 2012 R3 配置を管理する](manage-2012-r3-deployment-azure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-327">section of the [Manage AX 2012 R3 deployments on Azure](manage-2012-r3-deployment-azure.md) article.</span></span>
2.  <span data-ttu-id="aef41-328">仮想マシンで次の場所に移動します: F:TestTransferTool</span><span class="sxs-lookup"><span data-stu-id="aef41-328">Go to the following location on the virtual machine: F:TestTransferTool</span></span>
3.  <span data-ttu-id="aef41-329">テスト データ転送ツールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="aef41-329">Install the Test Data Transfer Tool.</span></span> <span data-ttu-id="aef41-330">手順については、 [テスト データ転送ツール (ベータ版) をインストールする](install-test-data-transfer-tool-beta.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-330">For instructions, see [Install the Test Data Transfer Tool (beta)](install-test-data-transfer-tool-beta.md).</span></span>
4.  <span data-ttu-id="aef41-331">コマンド プロンプトを開いて、次の場所にアクセスします: C:\Program Files (x86) \Microsoft Dynamics AX 2012 テスト データ確認転送ツール (ベータ)</span><span class="sxs-lookup"><span data-stu-id="aef41-331">Open a command prompt and navigate to the following location: C:\Program Files (x86)\Microsoft Dynamics AX 2012 Test Data Transfer Tool (Beta)</span></span>
5.  <span data-ttu-id="aef41-332">次のコマンドを実行します: dp.exe import F:DemoData MicrosoftDynamicsAx</span><span class="sxs-lookup"><span data-stu-id="aef41-332">Run the following command: dp.exe import F:DemoData MicrosoftDynamicsAx</span></span>

> [!NOTE]
> <span data-ttu-id="aef41-333">サンプル データには、AX 2012 R3 の試用版のライセンス キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="aef41-333">The sample data includes trial license keys for AX 2012 R3.</span></span> <span data-ttu-id="aef41-334">サンプル データをインストールしないように選択する場合は、開発またはテスト用の試用版ライセンス キーを [CustomerSource](https://mbs.microsoft.com/downloads/customer/AX/AXDemoTools/MicrosoftDynamicsAX2012R2v4DemoLicense.zip) または [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898#FileId=57028) からダウンロードすることができます</span><span class="sxs-lookup"><span data-stu-id="aef41-334">If you choose not to install the sample data, you can download trial license keys—for development or testing purposes—from [CustomerSource](https://mbs.microsoft.com/downloads/customer/AX/AXDemoTools/MicrosoftDynamicsAX2012R2v4DemoLicense.zip) or [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898#FileId=57028).</span></span>

### <a name="give-users-access"></a><span data-ttu-id="aef41-335">ユーザーのアクセス許可を付与します</span><span class="sxs-lookup"><span data-stu-id="aef41-335">Give users access</span></span>

<span data-ttu-id="aef41-336">ユーザが AX 2012 R3 にアクセスできるようにするには、以下のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="aef41-336">To enable your users to access AX 2012 R3, complete the following tasks:</span></span>

-   <span data-ttu-id="aef41-337">CLI- &lt;GUID&gt; 仮想マシンのリモート デスクトップ ユーザー グループに各ユーザーのドメイン アカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="aef41-337">Add each user’s domain account to the Remote Desktop Users group on the CLI-&lt;GUID&gt; virtual machine.</span></span>
-   <span data-ttu-id="aef41-338">ユーザーに AX 2012 R3 へのアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="aef41-338">Give users access to AX 2012 R3.</span></span> <span data-ttu-id="aef41-339">手順については、[Microsoft Dynamics AX で新しいユーザーを作成する](https://technet.microsoft.com/library/aa548139.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-339">For instructions, see [Create new users in Microsoft Dynamics AX](https://technet.microsoft.com/library/aa548139.aspx).</span></span>

> [!NOTE]
> <span data-ttu-id="aef41-340">VPN接続とドメインの信頼を作成しない場合でも、ユーザーに AX 2012 R3 へのアクセス権を与えることができます。</span><span class="sxs-lookup"><span data-stu-id="aef41-340">If you don’t want to create a VPN connection and a domain trust, you can still give users access to AX 2012 R3.</span></span> <span data-ttu-id="aef41-341">これを行うには、ドメイン コントローラとして機能する仮想マシンにログオンし、各ユーザーのドメイン アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-341">To do so, you’ll need to log on to the virtual machine that serves as the domain controller, and create domain accounts for each user.</span></span> <span data-ttu-id="aef41-342">その後、上記の 2 つのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef41-342">Then, you’ll need to complete the two tasks mentioned above.</span></span>

### <a name="set-up-and-configure-ax-2012-r3"></a><span data-ttu-id="aef41-343">AX 2012 R3 の設定およびコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="aef41-343">Set up and configure AX 2012 R3</span></span>

<span data-ttu-id="aef41-344">Azure 上で AX 2012 R3 を設定およびコンフィギュレーションする手順は、オンプレミス展開の設定およびコンフィギュレーションに使用される手順と同じです。</span><span class="sxs-lookup"><span data-stu-id="aef41-344">The procedures for setting up and configuring AX 2012 R3 on Azure are the same procedures used for setting up and configuring on-premises deployments.</span></span> <span data-ttu-id="aef41-345">詳細については、次のリソースを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-345">See the following resources for more information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aef41-346"><strong>タスク</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-346"><strong>Task</strong></span></span></td>
<td><span data-ttu-id="aef41-347"><strong>リソース</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-347"><strong>Resources</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aef41-348">TechNet の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-348">See the instructions on TechNet</span></span></td>
<td><ul>
<li><span data-ttu-id="aef41-349"><a href="https://technet.microsoft.com/library/gg732218.aspx">Microsoft Dynamics AX のシステム設定</a></span><span class="sxs-lookup"><span data-stu-id="aef41-349"><a href="https://technet.microsoft.com/library/gg732218.aspx">System setup for Microsoft Dynamics AX</a></span></span></li>
<li><span data-ttu-id="aef41-350"><a href="https://technet.microsoft.com/library/gg732158.aspx">Microsoft Dynamics AX クライアント</a></span><span class="sxs-lookup"><span data-stu-id="aef41-350"><a href="https://technet.microsoft.com/library/gg732158.aspx">The Microsoft Dynamics AX client</a></span></span></li>
<li><span data-ttu-id="aef41-351"><a href="https://technet.microsoft.com/library/gg731868.aspx">Application Object Server</a></span><span class="sxs-lookup"><span data-stu-id="aef41-351"><a href="https://technet.microsoft.com/library/gg731868.aspx">Application Object Servers</a></span></span></li>
<li><span data-ttu-id="aef41-352"><a href="https://technet.microsoft.com/library/ee873263.aspx">Microsoft Dynamics AX でのレポート</a></span><span class="sxs-lookup"><span data-stu-id="aef41-352"><a href="https://technet.microsoft.com/library/ee873263.aspx">Reporting in Microsoft Dynamics AX</a></span></span></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aef41-353"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-353"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aef41-354"><a href="https://technet.microsoft.com/library/dd309703.aspx">既定のレポートを展開</a>し、ユーザーに<a href="https://technet.microsoft.com/library/aa496432.aspx">アクセス権を付与</a>してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-354">Be sure to <a href="https://technet.microsoft.com/library/dd309703.aspx">deploy the default reports</a> and <a href="https://technet.microsoft.com/library/aa496432.aspx">grant users access</a> to them.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="aef41-355"><a href="https://www.microsoft.com/download/details.aspx?id=5916">Management Reporter 2012</a></span><span class="sxs-lookup"><span data-stu-id="aef41-355"><a href="https://www.microsoft.com/download/details.aspx?id=5916">Management Reporter 2012</a></span></span></li>
<li><span data-ttu-id="aef41-356"><a href="https://technet.microsoft.com/library/ee873272.aspx"> Microsoft Dynamics AX での分析</a></span><span class="sxs-lookup"><span data-stu-id="aef41-356"><a href="https://technet.microsoft.com/library/ee873272.aspx">Analytics in Microsoft Dynamics AX</a></span></span></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aef41-357"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-357"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aef41-358">AX 2012 R3 に含まれているキューブを処理するには、ExternalCommandTimeout 値を 7200 に増やすことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="aef41-358">To process the cubes that are included with AX 2012 R3, we recommend that you increase the ExternalCommandTimeout value to 7200.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="aef41-359"><a href="https://technet.microsoft.com/library/gg866975.aspx">ヘルプ サーバー</a></span><span class="sxs-lookup"><span data-stu-id="aef41-359"><a href="https://technet.microsoft.com/library/gg866975.aspx">Help server</a></span></span></li>
<li><span data-ttu-id="aef41-360"><a href="https://technet.microsoft.com/library/gg751374.aspx">エンタープライズ ポータルおよびロール センター</a></span><span class="sxs-lookup"><span data-stu-id="aef41-360"><a href="https://technet.microsoft.com/library/gg751374.aspx">Enterprise Portal and Role Centers</a></span></span></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aef41-361"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="aef41-361"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aef41-362">エンタープライズ ポータルはポート 81 で実行するように設定されているため、ファイアウォール設定でそのポートを除外してください。</span><span class="sxs-lookup"><span data-stu-id="aef41-362">Enterprise Portal is configured to run on port 81, so be sure to exclude that port in your firewall settings.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="aef41-363"><a href="https://technet.microsoft.com/library/gg731850.aspx">エンタープライズ検索</a></span><span class="sxs-lookup"><span data-stu-id="aef41-363"><a href="https://technet.microsoft.com/library/gg731850.aspx">Enterprise Search</a></span></span></li>
<li><span data-ttu-id="aef41-364"><a href="https://technet.microsoft.com/library/gg731810.aspx">サービス & アプリケーション統合フレームワーク (AIF)</a></span><span class="sxs-lookup"><span data-stu-id="aef41-364"><a href="https://technet.microsoft.com/library/gg731810.aspx">Services and Application Integration Framework (AIF)</a></span></span></li>
<li><span data-ttu-id="aef41-365"><a href="https://technet.microsoft.com/library/jj710398.aspx">Microsoft Dynamics AX Retail IT プロおよび開発者向け</a></span><span class="sxs-lookup"><span data-stu-id="aef41-365"><a href="https://technet.microsoft.com/library/jj710398.aspx">Microsoft Dynamics AX Retail for IT pros and developers</a></span></span></li>
<li><span data-ttu-id="aef41-366"><a href="https://technet.microsoft.com/library/aa834453.aspx">.NET Business Connector</a></span><span class="sxs-lookup"><span data-stu-id="aef41-366"><a href="https://technet.microsoft.com/library/aa834453.aspx">.NET Business Connector</a></span></span></li>
<li><span data-ttu-id="aef41-367"><a href="https://technet.microsoft.com/library/gg731779.aspx">セキュリティ</a></span><span class="sxs-lookup"><span data-stu-id="aef41-367"><a href="https://technet.microsoft.com/library/gg731779.aspx">Security</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aef41-368">印刷可能なガイドおよびホワイト ペーパーの表示</span><span class="sxs-lookup"><span data-stu-id="aef41-368">View printable guides and white papers</span></span></td>
<td><ul>
<li><span data-ttu-id="aef41-369"><a href="https://technet.microsoft.com/library/gg732268.aspx">印刷可能なガイド</a></span><span class="sxs-lookup"><span data-stu-id="aef41-369"><a href="https://technet.microsoft.com/library/gg732268.aspx">Printable guides</a></span></span></li>
<li><span data-ttu-id="aef41-370"><a href="https://technet.microsoft.com/library/gg188985.aspx">システム管理者向けのホワイト ペーパー</a></span><span class="sxs-lookup"><span data-stu-id="aef41-370"><a href="https://technet.microsoft.com/library/gg188985.aspx">White papers for system administrators</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aef41-371">Microsoft Dynamics AX ウェブ検索ツールの使用</span><span class="sxs-lookup"><span data-stu-id="aef41-371">Use the Microsoft Dynamics AX web search tool</span></span></td>
<td><ul>
<li><span data-ttu-id="aef41-372"><a href="https://go.microsoft.com/fwlink/?LinkID=212924">開発者用の Web 検索</a></span><span class="sxs-lookup"><span data-stu-id="aef41-372"><a href="https://go.microsoft.com/fwlink/?LinkID=212924">Web search for developers</a></span></span></li>
<li><span data-ttu-id="aef41-373"><a href="https://go.microsoft.com/fwlink/?LinkID=212925">システム管理者用の Web 検索</a></span><span class="sxs-lookup"><span data-stu-id="aef41-373"><a href="https://go.microsoft.com/fwlink/?LinkID=212925">Web search for system administrators</a></span></span></li>
<li><span data-ttu-id="aef41-374"><a href="https://go.microsoft.com/fwlink/?LinkID=212922">アプリケーション ユーザー用の Web 検索</a></span><span class="sxs-lookup"><span data-stu-id="aef41-374"><a href="https://go.microsoft.com/fwlink/?LinkID=212922">Web search for application users</a></span></span></li>
<li><span data-ttu-id="aef41-375"><a href="https://go.microsoft.com/fwlink/?LinkID=194311">結合された Web 検索</a></span><span class="sxs-lookup"><span data-stu-id="aef41-375"><a href="https://go.microsoft.com/fwlink/?LinkID=194311">Combined web search</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="7-learn-about-the-service-accounts-for-this-environment"></a><span data-ttu-id="aef41-376">7. この環境のサービス アカウントについて学ぶ</span><span class="sxs-lookup"><span data-stu-id="aef41-376">7. Learn about the service accounts for this environment</span></span>
<span data-ttu-id="aef41-377">次のセクションでは、環境を配置したときに作成されたサービス アカウントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="aef41-377">The following sections provide information about the service accounts that were created when you deployed the environment.</span></span>

### <a name="domain-accounts"></a><span data-ttu-id="aef41-378">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="aef41-378">Domain accounts</span></span>

<span data-ttu-id="aef41-379">次のテーブルに、環境を配置したときに作成されるドメインア カウントの既定の名前を示します。</span><span class="sxs-lookup"><span data-stu-id="aef41-379">The following table lists the default names of the domain accounts that are created when you deployed the environment.</span></span>

| <span data-ttu-id="aef41-380">環境</span><span class="sxs-lookup"><span data-stu-id="aef41-380">Environment</span></span>                     | <span data-ttu-id="aef41-381">説明</span><span class="sxs-lookup"><span data-stu-id="aef41-381">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef41-382"><DomainName>AOSServiceUser</span><span class="sxs-lookup"><span data-stu-id="aef41-382"><DomainName>AOSServiceUser</span></span>      | <span data-ttu-id="aef41-383">次のサービスを AOS-<GUID> 仮想マシンで実行するために使用されたアカウント: Microsoft Dynamics AX Object Server。</span><span class="sxs-lookup"><span data-stu-id="aef41-383">The account used to run the following services on AOS-<GUID> virtual machines: Microsoft Dynamics AX Object Server.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="aef41-384"><DomainName>SQLServiceUser</span><span class="sxs-lookup"><span data-stu-id="aef41-384"><DomainName>SQLServiceUser</span></span>      | <span data-ttu-id="aef41-385">次のサービスを SQL で実行するために使用されるアカウント -<GUID> 仮想マシン: SQL Server Analysis Services (MSSQLSERVER)。</span><span class="sxs-lookup"><span data-stu-id="aef41-385">The account used to run the following services on SQL-<GUID> virtual machines: SQL Server Analysis Services (MSSQLSERVER).</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="aef41-386"><DomainName>DynamicsInstallUser</span><span class="sxs-lookup"><span data-stu-id="aef41-386"><DomainName>DynamicsInstallUser</span></span> | <span data-ttu-id="aef41-387">AX 2012 R3 をインストールするために使用したアカウント。</span><span class="sxs-lookup"><span data-stu-id="aef41-387">The account used to install AX 2012 R3.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="aef41-388"><DomainName>SPServiceUser</span><span class="sxs-lookup"><span data-stu-id="aef41-388"><DomainName>SPServiceUser</span></span>       | <span data-ttu-id="aef41-389">次のサービスを EP-<GUID> 仮想マシンで実行するために使用されたアカウント: AppFabric Caching Service、SharePoint Search Host Controller、SharePoint Server Search 15、SharePoint Timer Service、および SharePoint User Code Host。</span><span class="sxs-lookup"><span data-stu-id="aef41-389">The account used to run the following services on EP-<GUID> virtual machines: AppFabric Caching Service, SharePoint Search Host Controller, SharePoint Server Search 15, SharePoint Timer Service, and SharePoint User Code Host.</span></span>                                                                                                                       |
| <span data-ttu-id="aef41-390"><DomainName>BCProxyUser</span><span class="sxs-lookup"><span data-stu-id="aef41-390"><DomainName>BCProxyUser</span></span>         | <span data-ttu-id="aef41-391">ビジネス コネクタ プロキシとして使用されるアカウント。</span><span class="sxs-lookup"><span data-stu-id="aef41-391">The account used as the Business Connector proxy.</span></span>                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="aef41-392"><DomainName>AXServiceUser</span><span class="sxs-lookup"><span data-stu-id="aef41-392"><DomainName>AXServiceUser</span></span>       | <span data-ttu-id="aef41-393">AOS<GUID> 仮想マシンで次のサービスを実行するためにアカウントが使用されます: Microsoft Dynamics AX Data Import/Export Framework Service および Microsoft Dynamics ERP RapidStart Connector。</span><span class="sxs-lookup"><span data-stu-id="aef41-393">The account used to run the following services on AOS-<GUID> virtual machines: Microsoft Dynamics AX Data Import/Export Framework Service and Microsoft Dynamics ERP RapidStart Connector.</span></span> <span data-ttu-id="aef41-394">アカウントは、次のサービスを CLI-<GUID> 仮想マシンで実行するためにも使用されます: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client。</span><span class="sxs-lookup"><span data-stu-id="aef41-394">The account is also used to run the following services on CLI-<GUID> virtual machines: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client.</span></span> |

> [!NOTE] 
> <span data-ttu-id="aef41-395">パスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) のクラウド ホスト環境ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-395">The passwords are displayed on the Cloud-hosted environments page in [Lifecycle Services](https://lifecycleservices.dynamics.com/en/).</span></span>

### <a name="local-administrator-accounts"></a><span data-ttu-id="aef41-396">ローカル管理者アカウント</span><span class="sxs-lookup"><span data-stu-id="aef41-396">Local administrator accounts</span></span>

<span data-ttu-id="aef41-397">配置した各仮想マシンには、ローカル Administrator アカウントがあります。</span><span class="sxs-lookup"><span data-stu-id="aef41-397">Each virtual machine that you deployed has a local administrator account.</span></span> <span data-ttu-id="aef41-398">このアカウントは builtinaxlocaladmin です。</span><span class="sxs-lookup"><span data-stu-id="aef41-398">This account is: builtinaxlocaladmin.</span></span> <span data-ttu-id="aef41-399">ローカル管理者アカウントのパスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) の クラウド ホスト 環境ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="aef41-399">The passwords for the local administrator accounts are displayed on the Cloud-hosted environments page in [Lifecycle Services](https://lifecycleservices.dynamics.com/en/).</span></span>



