---
title: Azure でのテスト環境の配置
description: このトピックでは、Microsoft Azure でのテスト環境の配置方法について説明します。
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
ms.custom: 13281
ms.assetid: 861f276d-adeb-4591-b53f-beafd1b77999
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 49ff03d11c75e79be97f3813be2617c3ae8d64d9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183252"
---
# <a name="deploy-test-environments-on-azure"></a><span data-ttu-id="96581-103">Azure でのテスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="96581-103">Deploy test environments on Azure</span></span>

[!include [banner](../../includes/banner.md)]

<a name="prerequisites"></a><span data-ttu-id="96581-104">必要条件</span><span class="sxs-lookup"><span data-stu-id="96581-104">Prerequisites</span></span>
-------------

<span data-ttu-id="96581-105">この記事の手順を実行する前に、次の条件が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="96581-105">Before you complete the procedures in this article, make sure that the following prerequisites are in place.</span></span>

|                |                                                                                                                                                                 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96581-106">**カテゴリ**</span><span class="sxs-lookup"><span data-stu-id="96581-106">**Category**</span></span>   | <span data-ttu-id="96581-107">**前提条件**</span><span class="sxs-lookup"><span data-stu-id="96581-107">**Prerequisite**</span></span>                                                                                                                                                |
| <span data-ttu-id="96581-108">必要なタスク</span><span class="sxs-lookup"><span data-stu-id="96581-108">Required tasks</span></span> | [<span data-ttu-id="96581-109">Azure 上での Microsoft Dynamics AX 2012 R3 の配置計画</span><span class="sxs-lookup"><span data-stu-id="96581-109">Plan your Microsoft Dynamics AX 2012 R3 deployment on Azure</span></span>](plan-2012-r3-deployment-azure.md) |



## <a name="1-log-on-to-lifecycle-services"></a><span data-ttu-id="96581-110">1. ライフサイクル サービスにログオンする</span><span class="sxs-lookup"><span data-stu-id="96581-110">1. Log on to Lifecycle Services</span></span>
<span data-ttu-id="96581-111">Microsoft Dynamics Lifecycle Services は、顧客およびパートナーが Microsoft Dynamics AX の管理に使用できるクラウドベースの共同ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="96581-111">Microsoft Dynamics Lifecycle Services provides a cloud-based collaborative workspace that customers and partners can use to manage Microsoft Dynamics AX projects.</span></span> <span data-ttu-id="96581-112">Azure に AX 2012 R3 を配置するには、この Web サイトを使用します。</span><span class="sxs-lookup"><span data-stu-id="96581-112">You’ll use this website to deploy AX 2012 R3 on Azure.</span></span> <span data-ttu-id="96581-113">Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="96581-113">Lifecycle Services is available to customers and partners as part of their support plans.</span></span> <span data-ttu-id="96581-114">CustomerSource または PartnerSource の資格情報でアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="96581-114">You can access it with your CustomerSource or PartnerSource credentials.</span></span> [<span data-ttu-id="96581-115">Lifecycle Services にログオン</span><span class="sxs-lookup"><span data-stu-id="96581-115">Log on to Lifecycle Services</span></span>](https://lcs.dynamics.com/en/)

## <a name="2-create-a-project"></a><span data-ttu-id="96581-116">2. プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="96581-116">2. Create a project</span></span>
<span data-ttu-id="96581-117">Lifecycle Services にログインした後、既存のプロジェクトを開くか、または新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="96581-117">After you log in to Lifecycle Services, open an existing project, or create a new project.</span></span> <span data-ttu-id="96581-118">プロジェクトは、Lifecycle Services でのエクスペリエンスの主な開催者です。</span><span class="sxs-lookup"><span data-stu-id="96581-118">Projects are the key organizer of your experience in Lifecycle Services.</span></span> <span data-ttu-id="96581-119">プロジェクトに関連する手法は、既定でプロジェクトに含まれるフェーズとタスクを決定します。</span><span class="sxs-lookup"><span data-stu-id="96581-119">The methodology associated with a project determines which phases and tasks are included in the project by default.</span></span>

## <a name="3-connect-the-project-to-your-azure-subscription"></a><span data-ttu-id="96581-120">3. Azure サブスクリプションにプロジェクトを接続する</span><span class="sxs-lookup"><span data-stu-id="96581-120">3. Connect the project to your Azure subscription</span></span>
<span data-ttu-id="96581-121">Azure サブスクリプションに Lifecycle Services プロジェクトを接続します。</span><span class="sxs-lookup"><span data-stu-id="96581-121">Connect the Lifecycle Services project to your Azure subscription.</span></span> <span data-ttu-id="96581-122">これにより、Lifecycle Services は AX 2012 R3 環境をサブスクリプションに展開できます。</span><span class="sxs-lookup"><span data-stu-id="96581-122">This will enable Lifecycle Services to deploy an AX 2012 R3 environment to the subscription.</span></span> <span data-ttu-id="96581-123">Azure サブスクリプションにプロジェクトを接続するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="96581-123">To connect the project to your Azure subscription, complete the following procedure.</span></span> <span data-ttu-id="96581-124">プロジェクトは 1 つの Azure サブスクリプションにだけ接続できることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="96581-124">Keep in mind that a project can be connected to only one Azure subscription.</span></span> <span data-ttu-id="96581-125">複数の Azure サブスクリプションがある場合、この手順を実行する前にどのサブスクリプションを使用するかを必ず識別します。</span><span class="sxs-lookup"><span data-stu-id="96581-125">If you have multiple Azure subscriptions, be sure to identify which subscription you want to use before you complete this procedure.</span></span>

1.  <span data-ttu-id="96581-126">**クラウド ホスト環境**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-126">Click **Cloud-hosted environments**.</span></span> <span data-ttu-id="96581-127">**クラウド ホスト環境** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-127">The **Cloud-hosted environments** page is displayed.</span></span>
2.  <span data-ttu-id="96581-128">**Microsoft Azure 設定**パネルが画面の横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-128">The **Microsoft Azure setup** panel is displayed on the side of the screen.</span></span> <span data-ttu-id="96581-129">表示されない場合は、**Microsoft Azure 設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-129">If it is not displayed, click **Microsoft Azure settings**.</span></span>
3.  <span data-ttu-id="96581-130">Azure サブスクリプション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="96581-130">Enter your Azure subscription ID.</span></span> <span data-ttu-id="96581-131">サブスクリプション ID を検索する必要がある場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="96581-131">If you need to find your subscription ID, complete the following steps:</span></span>
    1.  <span data-ttu-id="96581-132">ブラウザの別のインスタンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="96581-132">Open another instance of your browser.</span></span>
    2.  <span data-ttu-id="96581-133">**Azure 管理ポータル**にログオンします。</span><span class="sxs-lookup"><span data-stu-id="96581-133">Log on to the **Azure management portal**.</span></span>
    3.  <span data-ttu-id="96581-134">左のナビゲーション ウィンドウで、**設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-134">In the navigation pane on the left, click **Settings**.</span></span> <span data-ttu-id="96581-135">(**設定**リンクを表示するには、ナビゲーションペインの一番下までスクロールしなければならない場合があります。) **設定**ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-135">(You may have to scroll to the bottom of the navigation pane to see the **Settings** link.) The **Settings** page is displayed.</span></span>
    4.  <span data-ttu-id="96581-136">サブスクリプション ID をコピーして、Lifecycle Services の **Azure サブスクリプション ID** フィールドに貼り付けます (現在別のブラウザー インスタンスに表示されています)。</span><span class="sxs-lookup"><span data-stu-id="96581-136">Copy your subscription ID, and then paste it into the **Azure subscription ID** field in Lifecycle Services (which is currently displayed in another browser instance).</span></span>

4.  <span data-ttu-id="96581-137">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-137">Click **Next**.</span></span>
5.  <span data-ttu-id="96581-138">**ダウンロード**をクリックして管理証明書をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="96581-138">Click **Download** to download a management certificate.</span></span> <span data-ttu-id="96581-139">この管理証明書により、Lifecycle Services はお客様の代わりに Azure と通信できます。</span><span class="sxs-lookup"><span data-stu-id="96581-139">This management certificate enables Lifecycle Services to communicate with Azure on your behalf.</span></span> <span data-ttu-id="96581-140">既定では、管理証明書はコンピューターのダウンロード フォルダーに保存され、LifecycleServicesDeployment.cer という名前が付きます。</span><span class="sxs-lookup"><span data-stu-id="96581-140">By default, the management certificate is saved to the Downloads folder on your computer and is named LifecycleServicesDeployment.cer.</span></span>
6.  <span data-ttu-id="96581-141">管理証明書を Azure にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="96581-141">Upload the management certificate to Azure.</span></span> <span data-ttu-id="96581-142">そのためには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="96581-142">To do so, complete the following steps:</span></span>
    1.  <span data-ttu-id="96581-143">ブラウザの別のインスタンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="96581-143">Open another instance of your browser.</span></span> <span data-ttu-id="96581-144">(または、手順 3 で開いた可能性のあるブラウザインスタンスに移動します。)</span><span class="sxs-lookup"><span data-stu-id="96581-144">(Or, go to the browser instance that you may have opened in step 3.)</span></span>
    2.  <span data-ttu-id="96581-145">**Azure 管理ポータル**にログオンします。</span><span class="sxs-lookup"><span data-stu-id="96581-145">Log on to the **Azure management portal**.</span></span>
    3.  <span data-ttu-id="96581-146">左のナビゲーション ウィンドウで、**設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-146">In the navigation pane on the left, click **Settings**.</span></span> <span data-ttu-id="96581-147">**設定** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-147">The **Settings** page is displayed.</span></span>
    4.  <span data-ttu-id="96581-148">**管理証明書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-148">Click **Management certificates**.</span></span>
    5.  <span data-ttu-id="96581-149">ページの下部にある**アップロード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-149">Click **Upload** at the bottom of the page.</span></span>
    6.  <span data-ttu-id="96581-150">**管理証明書をアップロード** ウィンドウで、手順 5 でダウンロードした管理証明書を参照します。</span><span class="sxs-lookup"><span data-stu-id="96581-150">In the **Upload a management certificate** window, browse to the management certificate that you downloaded in step 5.</span></span> <span data-ttu-id="96581-151">その後、チェック マークをクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-151">Then click the check mark.</span></span>

7.  <span data-ttu-id="96581-152">Lifecycle Services で **Microsoft Azure 設定**パネルを表示するブラウザーに戻ります。</span><span class="sxs-lookup"><span data-stu-id="96581-152">Go back to the browser that displays the **Microsoft Azure setup** panel in Lifecycle Services.</span></span> <span data-ttu-id="96581-153">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-153">Click **Next**.</span></span>
8.  <span data-ttu-id="96581-154">最も近い地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="96581-154">Select the region that is closest to you.</span></span> <span data-ttu-id="96581-155">AX 2012 R3 環境は、この領域のデータ センターに配置されます。</span><span class="sxs-lookup"><span data-stu-id="96581-155">The AX 2012 R3 environment will be deployed to a datacenter in this region.</span></span>
9.  <span data-ttu-id="96581-156">**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-156">Click **Connect**.</span></span> <span data-ttu-id="96581-157">これで、プロジェクトが指定された Azure サブスクリプションに接続できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="96581-157">The project is now connected to the Azure subscription that you specified.</span></span> <span data-ttu-id="96581-158">プロジェクトを間違った Azure サブスクリプション (複数の Azure サブスクリプションがあると仮定した場合) に接続していることが分かった場合、プロジェクトを削除し、新しいプロジェクトを作成し、新しいプロジェクトを適切な Azure サブスクリプションに接続させるためのこの手順を繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-158">If you discover that you connected the project to the wrong Azure subscription (that is, assuming you have multiple Azure subscriptions), you’ll need to delete the project, create a new project, and then repeat this procedure to connect the new project to the appropriate Azure subscription.</span></span>

## <a name="4-connect-your-corporate-network-to-the-azure-virtual-network"></a><span data-ttu-id="96581-159">4. 会社のネットワークを Azure 仮想ネットワークに接続する</span><span class="sxs-lookup"><span data-stu-id="96581-159">4. Connect your corporate network to the Azure virtual network</span></span>
<span data-ttu-id="96581-160">次のセクションでは、企業ユーザーが AX 2012 R3 にアクセスできるように、Azure 仮想ネットワークとドメインを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="96581-160">The following sections provide information about how to configure the Azure virtual network and domain so that your corporate users can access AX 2012 R3.</span></span> <span data-ttu-id="96581-161">企業の資格情報を使用してこれらのシステムにログインする必要がある場合、環境を配置する前に接続を設定することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="96581-161">It is recommended that if you require login to these systems using corporate credentials that you set up the connectivity before you deploy the environment.</span></span> <span data-ttu-id="96581-162">これには、Azure のネットワーク機能を使用して企業ネットワークを 1 つ以上の Azure 仮想ネットワークに拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-162">This will require using Azure networking capabilities to extend you corporate network to one or more Azure virtual networks.</span></span> <span data-ttu-id="96581-163">さらに、Azure 仮想ネットワークに Active Directory を配置する必要があり、これは会社の Active Directory に対する信頼のために設定されます。</span><span class="sxs-lookup"><span data-stu-id="96581-163">It will additionally require you to deploy an Active Directory into the Azure virtual network, which will be set up for trust to your corporate Active Directory.</span></span> <span data-ttu-id="96581-164">この Active Directory は、Azure 仮想ネットワーク内の VM 関連リソースを管理するために適用されます。</span><span class="sxs-lookup"><span data-stu-id="96581-164">This Active Directory will be used to manage VM-related resources in the Azure virtual network.</span></span> <span data-ttu-id="96581-165">この Active Directory はシングルサインオンには使用されません。社内ディレクトリを同期するように設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="96581-165">This Active Directory will not be used for single sign-on, and should not be set up to sync the corporate directory.</span></span> <span data-ttu-id="96581-166">シングル サインオン機能は、ドメインの信頼関係を通じて提供されます。</span><span class="sxs-lookup"><span data-stu-id="96581-166">Single sign-on capabilities will be provided through the domain trust.</span></span>

### <a name="create-a-site-to-site-vpn-connection"></a><span data-ttu-id="96581-167">サイト間 VPN 接続を作成する</span><span class="sxs-lookup"><span data-stu-id="96581-167">Create a site-to-site VPN connection</span></span>

<span data-ttu-id="96581-168">企業ユーザーが Azure 仮想ネットワーク内の仮想マシンのリソースにアクセスできるようにするには、Azure 仮想ネットワークとオンプレミス社内ネットワークの間にサイト間 VPN 接続を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-168">To enable corporate users to access resources on the virtual machines in the Azure virtual network, you’ll need to create a site-to-site VPN connection between the Azure virtual network and your on-premises, corporate network.</span></span> <span data-ttu-id="96581-169">これを行う方法の詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-169">For information about how to do this, see:</span></span>

-   [<span data-ttu-id="96581-170">仮想ネットワークの概要</span><span class="sxs-lookup"><span data-stu-id="96581-170">Virtual network overview</span></span>](https://msdn.microsoft.com/library/windowsazure/jj156007.aspx)
-   [<span data-ttu-id="96581-171">仮想ネットワークのコンフィギュレーション タスク</span><span class="sxs-lookup"><span data-stu-id="96581-171">Virtual network configuration tasks</span></span>](https://msdn.microsoft.com/library/jj156206.aspx)
-   [<span data-ttu-id="96581-172">テスト用にシミュレーションしたハイブリッド クラウド環境を設定する</span><span class="sxs-lookup"><span data-stu-id="96581-172">Set up a simulated hybrid cloud environment for testing</span></span>](http://azure.microsoft.com/documentation/articles/virtual-networks-setup-simulated-hybrid-cloud-environment-testing/)
-   [<span data-ttu-id="96581-173">Windows Server 2012 ルーティングおよびリモート アクセスサービス (RRAS) を使用した Azure 仮想ネットワークのサイト間 VPN</span><span class="sxs-lookup"><span data-stu-id="96581-173">Site-to-site VPN in Azure virtual network using Windows Server 2012 Routing and Remote Access Service (RRAS)</span></span>](https://msdn.microsoft.com/library/dn636917.aspx)
-   [<span data-ttu-id="96581-174">管理ポータルに仮想ネットワーク ゲートウェイを構成する</span><span class="sxs-lookup"><span data-stu-id="96581-174">Configure a virtual network gateway in the management portal</span></span>](https://msdn.microsoft.com/library/azure/jj156210.aspx)

### <a name="create-an-active-directory-account-in-azure"></a><span data-ttu-id="96581-175">Azure の Active Directory アカウントの作成</span><span class="sxs-lookup"><span data-stu-id="96581-175">Create an Active Directory account in Azure</span></span>

<span data-ttu-id="96581-176">Active Directory は Azure 仮想ネットワークに必須です。</span><span class="sxs-lookup"><span data-stu-id="96581-176">An Active Directory is required in the Azure virtual network.</span></span> <span data-ttu-id="96581-177">Active Directory は Azure 仮想ネットワークに配置できます。</span><span class="sxs-lookup"><span data-stu-id="96581-177">An Active Directory can be deployed to the Azure virtual network.</span></span> <span data-ttu-id="96581-178">[Azure 仮想マシンに Windows Server Active Directory を展開するためのガイドライン](https://msdn.microsoft.com/library/azure/jj156090.aspx)に従ってください。</span><span class="sxs-lookup"><span data-stu-id="96581-178">Please follow [Guidelines for Deploying Windows Server Active Directory on Azure Virtual Machines](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span> <span data-ttu-id="96581-179">Active Directory フェデレーション サービスは現在 AX 2012 R3 でサポートされていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="96581-179">Please note that Active Directory Federation Services is not presently supported with AX 2012 R3.</span></span> <span data-ttu-id="96581-180">Active Directory を提供する場合は、LCS 展開サービスで使用できる範囲で次のサービス アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-180">If you are providing the Active Directory, you will need to create the following service accounts within it that can be used by LCS deployment services when you deploy the environment.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96581-181"><strong>勘定</strong></span><span class="sxs-lookup"><span data-stu-id="96581-181"><strong>Account</strong></span></span></td>
<td><span data-ttu-id="96581-182"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="96581-182"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96581-183">&lt;DomainName&gt;AXServiceUser</span><span class="sxs-lookup"><span data-stu-id="96581-183">&lt;DomainName&gt;AXServiceUser</span></span></td>
<td><span data-ttu-id="96581-184">AX 2012 R3 サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="96581-184">AX 2012 R3 service account</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96581-185">&lt;DomainName&gt;AOSServiceUser</span><span class="sxs-lookup"><span data-stu-id="96581-185">&lt;DomainName&gt;AOSServiceUser</span></span></td>
<td><span data-ttu-id="96581-186">AOS サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="96581-186">AOS service account</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96581-187">&lt;DomainName&gt;BCProxyUser</span><span class="sxs-lookup"><span data-stu-id="96581-187">&lt;DomainName&gt;BCProxyUser</span></span></td>
<td><span data-ttu-id="96581-188">Business Connector プロキシ アカウント</span><span class="sxs-lookup"><span data-stu-id="96581-188">Business Connector proxy account</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96581-189">&lt;DomainName&gt;SPServiceUser</span><span class="sxs-lookup"><span data-stu-id="96581-189">&lt;DomainName&gt;SPServiceUser</span></span></td>
<td><span data-ttu-id="96581-190">SharePoint サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="96581-190">SharePoint service account</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96581-191">&lt;DomainName&gt;SqlServiceUser</span><span class="sxs-lookup"><span data-stu-id="96581-191">&lt;DomainName&gt;SqlServiceUser</span></span></td>
<td><span data-ttu-id="96581-192">SQL Server サービス アカウント</span><span class="sxs-lookup"><span data-stu-id="96581-192">SQL Server service account</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96581-193">&lt;DomainName&gt;DynamicsInstallUser</span><span class="sxs-lookup"><span data-stu-id="96581-193">&lt;DomainName&gt;DynamicsInstallUser</span></span></td>
<td><span data-ttu-id="96581-194">AX 2012 R3 インストール アカウント 注記: このアカウントは、コンピューターをドメインに参加させるためのアクセス許可を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-194">AX 2012 R3 installation account Note: This account must have permission to join computers to the domain.</span></span> <span data-ttu-id="96581-195">このアカウントにアクセス許可を与えるには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="96581-195">To give this account permission, complete the following steps:</span></span>
<ol>
<li><span data-ttu-id="96581-196"><strong>開始</strong>をクリックし、dsa.msc 型で<strong>実行</strong>をクリックし、 <strong>OK</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-196">Click <strong>Start</strong>, click <strong>Run</strong>, type dsa.msc, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="96581-197">作業ウィンドウで、ドメイン ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="96581-197">In the task pane, expand the domain node.</span></span></li>
<li><span data-ttu-id="96581-198">変更する組織単位を検索し、右クリックしてから<strong>デリゲート コントロール</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-198">Locate and right-click the organizational unit that you want to modify, and then click <strong>Delegate Control</strong>.</span></span></li>
<li><span data-ttu-id="96581-199"><strong>コントロールのデリゲート ウィザード</strong>で、<strong>次へ</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-199">In the <strong>Delegation of Control Wizard</strong>, click <strong>Next</strong>.</span></span></li>
<li><span data-ttu-id="96581-200">特定のユーザーまたは特定のグループを一覧に追加するには、<strong>追加</strong>をクリックし、次に <strong>次へ</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-200">Click <strong>Add</strong> to add a specific user or a specific group to the list, and then click <strong>Next</strong>.</span></span></li>
<li><span data-ttu-id="96581-201"><strong>委任するタスク</strong> ページで、<strong>委任するカスタム タスクを作成</strong>をクリックしてから、<strong>次へ</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-201">In the <strong>Tasks to Delegate</strong> page, click <strong>Create a custom task to delegate</strong>, and then click <strong>Next</strong>.</span></span></li>
<li><span data-ttu-id="96581-202"><strong>フォルダ内の次のオブジェクトのみ</strong>をクリックし、一覧から<strong>コンピューター オブジェクト</strong> チェック ボックスをクリックして選択します。</span><span class="sxs-lookup"><span data-stu-id="96581-202">Click <strong>Only the following objects in the folder</strong>, and then from the list, click to select the <strong>Computer objects</strong> check box.</span></span> <span data-ttu-id="96581-203">その後、リスト下部で <strong>このフォルダーの選択したオブジェクトを作成する</strong> および <strong>このフォルダーの選択したオブジェクトを削除する</strong> の各チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="96581-203">Then, select the check boxes below the list, <strong>Create selected objects in this folder</strong> and <strong>Delete selected objects in this folder</strong>.</span></span></li>
<li><span data-ttu-id="96581-204"><strong>次へ</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-204">Click <strong>Next</strong>.</span></span></li>
<li><span data-ttu-id="96581-205"><strong>アクセス許可</strong>リストで、次のチェック ボックスをクリックしてオンにします。</span><span class="sxs-lookup"><span data-stu-id="96581-205">In the <strong>Permissions</strong> list, click to select the following check boxes:</span></span>
<ul>
<li><span data-ttu-id="96581-206"><strong>パスワードのリセット</strong></span><span class="sxs-lookup"><span data-stu-id="96581-206"><strong>Reset Password</strong></span></span></li>
<li><span data-ttu-id="96581-207"><strong>アカウントの制限の読み取りと書き込み</strong></span><span class="sxs-lookup"><span data-stu-id="96581-207"><strong>Read and write Account Restrictions</strong></span></span></li>
<li><span data-ttu-id="96581-208"><strong>DNS ホスト名への検証済みの書き込み</strong></span><span class="sxs-lookup"><span data-stu-id="96581-208"><strong>Validated write to DNS host name</strong></span></span></li>
<li><span data-ttu-id="96581-209"><strong>サービス プリンシパル名への検証済みの書き込み</strong></span><span class="sxs-lookup"><span data-stu-id="96581-209"><strong>Validated write to service principal name</strong></span></span></li>
</ul></li>
<li><span data-ttu-id="96581-210"><strong>次へ</strong>をクリックし、<strong>完了</strong>の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-210">Click <strong>Next</strong>, and then click <strong>Finish</strong>.</span></span></li>
<li><span data-ttu-id="96581-211"><strong>Active Directory ユーザーおよびコンピューター MMC スナップイン</strong>を閉じます。</span><span class="sxs-lookup"><span data-stu-id="96581-211">Close the <strong>Active Directory Users and Computers MMC snap-in</strong>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96581-212">環境を配置するとき、これらのアカウントのパスワードを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-212">You will need to provide the passwords for these accounts when you deploy the environment.</span></span>

### <a name="create-a-domain-trust"></a><span data-ttu-id="96581-213">ドメイン信頼の作成</span><span class="sxs-lookup"><span data-stu-id="96581-213">Create a domain trust</span></span>

<span data-ttu-id="96581-214">企業ユーザーが Azure ドメイン内の仮想マシンのリソースにアクセスできるようにするには、ドメイン間で Active Directory のトラストを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-214">To enable corporate users to access resources on the virtual machines in your Azure domain, you must create an Active Directory trust between the domains.</span></span> <span data-ttu-id="96581-215">信託の作成方法の詳細については、「[フォレスト信託の作成](https://technet.microsoft.com/library/cc754626.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-215">For information about how to create a trust, see [Create a Forest Trust](https://technet.microsoft.com/library/cc754626.aspx).</span></span> <span data-ttu-id="96581-216">このプロセスは、2 つのオンプレミス ドメイン間で信頼関係を作成する場合と同じプロセスです。</span><span class="sxs-lookup"><span data-stu-id="96581-216">This process is the same process you would use to create a trust between two on-premises domains.</span></span>

### <a name="give-the-administrators-group-the-right-to-log-on-as-a-batch-job"></a><span data-ttu-id="96581-217">バッチ ジョブとしてログオンする権限を管理者グループに付与します</span><span class="sxs-lookup"><span data-stu-id="96581-217">Give the Administrators group the right to log on as a batch job</span></span>

<span data-ttu-id="96581-218">Active Directory ドメイン コントローラーにログインし、次の手順を完了して、ビルトイン Administrator グループにバッチ ジョブとしてログオンする権利を付与します。</span><span class="sxs-lookup"><span data-stu-id="96581-218">Log in to the Active Directory domain controller and complete the following steps to give the built-in Administrators group the right to log on as a batch job.</span></span>

1.  <span data-ttu-id="96581-219">**開始**、**すべてのプログラム**の順にクリックし、**管理ツール**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-219">Click **Start**, click **All Programs**, and then click **Administrative Tools**.</span></span>
2.  <span data-ttu-id="96581-220">**管理ツール** メニューで、**グループ ポリシーの管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="96581-220">In the **Administrative Tools** menu, select **Group Policy Management**.</span></span>
3.  <span data-ttu-id="96581-221">**グループ ポリシー管理**コンソール ツリーで、**フォレスト: &lt;ServerName&gt;** をクリックしてから、**ドメイン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-221">In the **Group Policy Management** console tree, click **Forest: &lt;ServerName&gt;**, and then click **Domains**.</span></span>
4.  <span data-ttu-id="96581-222">サーバーの名前をクリックし、**ドメイン コントローラー**を展開します。**既定のドメイン コント ローラー ポリシー**を右クリックし、**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-222">Click the name of your server, expand **Domain Controllers**, right-click **Default Domain Controllers Policy**, and then click **Edit**.</span></span>
5.  <span data-ttu-id="96581-223">**グループ ポリシー管理エディター**で、**既定のドメイン コントローラ ポリシー &lt; ServerName &gt; ポリシー**とクリックし、**コンピューターの構成**を展開してから**ポリシー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-223">In the **Group Policy Management Editor**, click **Default Domain Controllers Policy &lt;ServerName&gt; Policy**, expand **Computer Configuration**, and then click **Policies**.</span></span>
6.  <span data-ttu-id="96581-224">**ポリシー** ツリーで、**Windows 設定**を展開してから**セキュリティの設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-224">In the **Policies** tree, expand **Windows Setting**, and then click **Security Settings**.</span></span>
7.  <span data-ttu-id="96581-225">**セキュリティの設定**ツリーで、**ローカル ポリシー**を展開してから**ユーザーの権限の割り当て**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-225">In the **Security Settings** tree, expand **Local Policies**, and then click **User Rights Assignment**.</span></span>
8.  <span data-ttu-id="96581-226">結果ウィンドウで、スクロールして**バッチ ジョブとしてログオン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-226">In the results pane, scroll to and then click **Log on as a batch job**.</span></span>
9.  <span data-ttu-id="96581-227">**バッチ ジョブとしてログオン プロパティ** ダイアログ ボックスで、**ユーザーまたはグループの追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-227">In the **Log on as a batch job Properties** dialog box, click **Add User or Group**.</span></span>
10. <span data-ttu-id="96581-228">**ユーザーまたはグループの追加**ダイアログ ボックスで、**参照**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-228">In the **Add User or Group** dialog box, click **Browse**.</span></span>
11. <span data-ttu-id="96581-229">**ユーザー、コンピュータ、またはグループの選択**ダイアログ ボックスで、**管理者**と入力します。</span><span class="sxs-lookup"><span data-stu-id="96581-229">In the **Select Users, Computers, or Groups** dialog box, type **Administrators**.</span></span>
12. <span data-ttu-id="96581-230">**名前の確認**をクリックして、あらかじめ登録された Administrator アカウントが表示されていることを確認し、**OK** を 3 回クリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-230">Click **Check Names** to verify that the built-in Administrators account appears, and then click **OK** three times.</span></span>

### <a name="change-the-default-organizational-unit"></a><span data-ttu-id="96581-231">既定の組織単位の変更</span><span class="sxs-lookup"><span data-stu-id="96581-231">Change the default organizational unit</span></span>

<span data-ttu-id="96581-232">仮想マシンをカスタム組織単位 (デフォルトの組織単位と比較して) の Active Directory に追加する場合は、展開を開始する前に Active Directory 内の既定の組織単位を変更できます。</span><span class="sxs-lookup"><span data-stu-id="96581-232">If you want virtual machines to be added to Active Directory in a custom organizational unit—versus the default organizational unit—you can change the default organizational unit in your Active Directory prior to starting deployment.</span></span> <span data-ttu-id="96581-233">詳細については、[ここ](http://pc-addicts.com/server-2012-change-default-ou/) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="96581-233">For more information, click [here](http://pc-addicts.com/server-2012-change-default-ou/).</span></span>

## <a name="5-deploy-a-test-environment-on-azure"></a><span data-ttu-id="96581-234">5. Azure でのテスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="96581-234">5. Deploy a test environment on Azure</span></span>
<span data-ttu-id="96581-235">Azure にテスト環境を配置するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="96581-235">Complete the following procedure to deploy a test environment on Azure.</span></span>

1. <span data-ttu-id="96581-236">**クラウド ホスト環境**ページで、追加 (+) アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-236">On the **Cloud-hosted environments** page, click the Add (+) icon.</span></span>
2. <span data-ttu-id="96581-237">**環境のトポロジの選択**パネルで、**開発/テスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="96581-237">In the **Select environment topology** panel, select **Dev/test**.</span></span>
3. <span data-ttu-id="96581-238">**テスト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-238">Click **Test**.</span></span>
4. <span data-ttu-id="96581-239">**環境名**フィールドに、配置される環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="96581-239">In the **Environment name** field, enter a name for the environment that will be deployed.</span></span>
5. <span data-ttu-id="96581-240">**詳細設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-240">Click **Advanced settings**.</span></span>
6. <span data-ttu-id="96581-241">ドメイン設定をカスタマイズするには、**ドメイン設定をカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-241">To customize domain settings, click **Customize domain settings**.</span></span> <span data-ttu-id="96581-242">情報を入力するには、次の表を使用してください。</span><span class="sxs-lookup"><span data-stu-id="96581-242">Then use the following table to enter information.</span></span>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td><span data-ttu-id="96581-243"><strong>以下を行う場合:</strong></span><span class="sxs-lookup"><span data-stu-id="96581-243"><strong>If you want to:</strong></span></span></td>
   <td><span data-ttu-id="96581-244"><strong>手順</strong></span><span class="sxs-lookup"><span data-stu-id="96581-244"><strong>Do this:</strong></span></span></td>
   </tr>
   <tr class="even">
   <td><span data-ttu-id="96581-245">Azure で環境用に新しいドメインを作成する</span><span class="sxs-lookup"><span data-stu-id="96581-245">Create a new domain in Azure for the environment</span></span></td>
   <td><ol>
   <li><span data-ttu-id="96581-246"><strong>新規ドメイン</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-246">Click <strong>New domain</strong>.</span></span></li>
   <li><span data-ttu-id="96581-247">ドメイン名を入力します。</span><span class="sxs-lookup"><span data-stu-id="96581-247">Enter a name for the domain.</span></span> <span data-ttu-id="96581-248">既定では、ドメインは <em>contoso.com</em> と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="96581-248">By default, the domain is named <em>contoso.com</em>.</span></span></li>
   </ol></td>
   </tr>
   <tr class="odd">
   <td><span data-ttu-id="96581-249">Azure の既存のドメインへの環境の追加</span><span class="sxs-lookup"><span data-stu-id="96581-249">Add the environment to an existing domain in Azure</span></span></td>
   <td><ol>
   <li><span data-ttu-id="96581-250"><strong>既存のドメイン</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-250">Click <strong>Existing domain</strong>.</span></span></li>
   <li><span data-ttu-id="96581-251">ドメイン名を入力します。</span><span class="sxs-lookup"><span data-stu-id="96581-251">Enter the name of the domain.</span></span> <span data-ttu-id="96581-252">たとえば、<em>contoso.com</em>。</span><span class="sxs-lookup"><span data-stu-id="96581-252">For example, <em>contoso.com</em>.</span></span></li>
   </ol></td>
   </tr>
   </tbody>
   </table>

7. <span data-ttu-id="96581-253">ドメインで作成されるサービス アカウントをカスタマイズするには、**サービス アカウントをカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-253">To customize the service accounts that will be created in the domain, click **Customize service accounts**.</span></span> <span data-ttu-id="96581-254">展開の **詳細設定** オプションを通じてサービス アカウントやサービス アカウントのパスワードを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="96581-254">Service accounts and/or service account passwords may be specified through the **Advanced Settings** option for a deployment.</span></span> <span data-ttu-id="96581-255">どちらもが指定されていない場合は、既定の勘定が使用され、ランダムなパスワードが選択されています。</span><span class="sxs-lookup"><span data-stu-id="96581-255">If neither is provided, default accounts are used and random passwords are selected.</span></span> <span data-ttu-id="96581-256">次の機能は、企業のアカウントの命名規則とパスワードの規則を管理する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="96581-256">Use these features when you want to maintain account naming and password rules for your corporation.</span></span> <span data-ttu-id="96581-257">アカウントとパスワードのルール:</span><span class="sxs-lookup"><span data-stu-id="96581-257">Account and password rules:</span></span>
   - <span data-ttu-id="96581-258">有効なサービス名は、特殊文字を含まない 20 文字未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-258">A valid service name must be less than 20 characters with no special characters.</span></span>
   - <span data-ttu-id="96581-259">有効なパスワードは 8 文字以上で、大文字、小文字、数字、および次の文字のうち少なくとも 1 つが含まれます: \['@', '!', '=', '\*'\] 次のような一般的なパスワードは使用できません: pass@word1</span><span class="sxs-lookup"><span data-stu-id="96581-259">A valid password must be more than 8 characters and contain uppercase letters, lowercase letters, numbers, and at least one of the following characters: \['@', '!', '=', '\*'\] You can’t use common passwords, such as: pass@word1</span></span>

8. <span data-ttu-id="96581-260">使用を希望する AX 2012 R3 のバージョンを選択するには、**サポートされているバージョン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-260">To select the version of AX 2012 R3 that you want use, click **Supported version**.</span></span> <span data-ttu-id="96581-261">既定では、この環境の AX 2012 R3 CU8 バージョンが配置されます。</span><span class="sxs-lookup"><span data-stu-id="96581-261">By default, the AX 2012 R3 CU8 version of this environment will be deployed.</span></span> <span data-ttu-id="96581-262">CU8 バージョンを使用しない場合は、**Dynamics ERP 2012 R3 RTM** をリストから選択します。</span><span class="sxs-lookup"><span data-stu-id="96581-262">If you don’t want to use the CU8 version, select **Dynamics ERP 2012 R3 RTM** from the list.</span></span>
9. <span data-ttu-id="96581-263">仮想マシン名をカスタマイズするには、**仮想マシン名をカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-263">To customize virtual machine names, click **Customize virtual machine names**.</span></span> <span data-ttu-id="96581-264">一般的な IT 名前付けガイドラインをサポートするために、仮想マシンに名前を付ける機能がほとんどの配置トポロジの**詳細設定**に用意されています。</span><span class="sxs-lookup"><span data-stu-id="96581-264">In order to support common IT naming guidelines, the ability to name virtual machines is provided through the **Advanced settings** option on most deployment topologies.</span></span> <span data-ttu-id="96581-265">名前を定義することに加えて、各仮想マシン タイプに開始インデックスを選択できます。</span><span class="sxs-lookup"><span data-stu-id="96581-265">In addition to defining the name, a starting index can be selected for each virtual machine type.</span></span> <span data-ttu-id="96581-266">インデックスは、配置される仮想マシン タイプのインスタンスごとに増加します。</span><span class="sxs-lookup"><span data-stu-id="96581-266">The index is incremented for each instance of the virtual machine type that is deployed.</span></span> <span data-ttu-id="96581-267">仮想マシン名は 13 文字またはそれ以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-267">Virtual machine names must be 13 characters or less.</span></span> <span data-ttu-id="96581-268">インデックスはマシン名とハイフン (-) で区切られ、その後に最大 2 桁のインデックスが続きます。</span><span class="sxs-lookup"><span data-stu-id="96581-268">The index is separated from the machine name by a hyphen (-), followed by the index that supports a maximum of 2 digits.</span></span> <span data-ttu-id="96581-269">例: ACustomVMName-99。仮想マシン インスタンスが最初の展開後に環境へ追加されると、展開サービスは中断した仮想マシン名のインクリメントを開始します。</span><span class="sxs-lookup"><span data-stu-id="96581-269">Example: ACustomVMName-99 When virtual machine instances are added to an environment after the initial deployment, the deployment service will start incrementing the virtual machine name where it left off.</span></span> <span data-ttu-id="96581-270">たとえば、2 で始まるインデックスを持つ 4 つの AOS 仮想マシンを展開する場合、最後の AOS インスタンス名は AOS-6 になります。</span><span class="sxs-lookup"><span data-stu-id="96581-270">For example, if you deployed four AOS virtual machines with a starting index of 2, then the last AOS instance name will be AOS-6.</span></span> <span data-ttu-id="96581-271">もう 2 つ AOS インスタンスを追加する場合は、AOS-7 と AOS 8 になります。</span><span class="sxs-lookup"><span data-stu-id="96581-271">If you add two more AOS instances, they will be AOS-7 and AOS-8.</span></span> <span data-ttu-id="96581-272">展開内の仮想マシン タイプの 1 つがカスタマイズされている場合は、すべての仮想マシン名をカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-272">If one of the virtual machine types in your deployment is customized, then all of the virtual machine names must be customized.</span></span> <span data-ttu-id="96581-273">これは、仮想マシン名が誤って紛失してしまったため、長期的な展開が発生しないようにするためです。</span><span class="sxs-lookup"><span data-stu-id="96581-273">This is done to ensure that a long deployment does not occur because a virtual machine name was accidentally missed.</span></span>
10. <span data-ttu-id="96581-274">リモート デスクトップ サービスの仮想マシンを配置することを選択した場合、**リモート デスクトップ サービスをカスタマイズ**をクリックし、ユーザーが web 経由で AX 2012 R3 にアクセスする方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="96581-274">If you have selected to deploy a Remote Desktop Services virtual machine, click **Customize remote desktop services** to specify how your users will access AX 2012 R3 via the web.</span></span> <span data-ttu-id="96581-275">次のオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="96581-275">Select one of the following options:</span></span>
    -   <span data-ttu-id="96581-276">**リモート デスクトップ:** このオプションはユーザーの完全なリモート デスクトップへのログインを有効にします。</span><span class="sxs-lookup"><span data-stu-id="96581-276">**Remote Desktop:** This option enables users to login to a full remote desktop.</span></span>
    -   <span data-ttu-id="96581-277">**RemoteApp プログラム**: このオプションを使用すると、完全なデスクトップウィンドウを使用しなくても、ユーザは直接 AX 2012 R3 にログインできます。</span><span class="sxs-lookup"><span data-stu-id="96581-277">**RemoteApp Programs:** This option enables users to login in to AX 2012 R3 directly, without having the experience of a full desktop window.</span></span> <span data-ttu-id="96581-278">RemoteApp は既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="96581-278">RemoteApp is enabled by default.</span></span>

    <span data-ttu-id="96581-279">環境が配置されると、**クラウド ホスト環境**ページで次のリンクが使用できます:</span><span class="sxs-lookup"><span data-stu-id="96581-279">After the environment has been deployed, the following links are available to you on the **Cloud-hosted environments** page:</span></span>
    -   <span data-ttu-id="96581-280">**RDS Web アクセス証明書**: これは、RDS Web アクセス サイトへの安全なアクセスを許可するために提供される自己署名証明書です。</span><span class="sxs-lookup"><span data-stu-id="96581-280">**RDS Web Access certificate**: This is a self-signed certificate that is provided to allow secured access to the RDS Web Access site.</span></span> <span data-ttu-id="96581-281">リンクをクリックしてこの証明書を開き、RDS Web アクセス サイトにアクセスする前に、**ローカル コンピューター**&gt;**信頼済ルート証明機関**にインストールします。</span><span class="sxs-lookup"><span data-stu-id="96581-281">Click the link and open this certificate and install it into the **Local Machine** &gt; **Trusted Root Certification Authorities** node before attempting to access the RDS Web Access site.</span></span> <span data-ttu-id="96581-282">この環境を生産能力に配置する前に、RDS クラスターに自分の証明書をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="96581-282">It is recommended that before this environment be placed into a production capacity that you install your own certificate to the RDS cluster.</span></span>
    -   <span data-ttu-id="96581-283">**RDS Web アクセス**: これにより、ユーザはウェブ上で AX 2012 R3 環境にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="96581-283">**RDS Web Access**: This allows users to gain access to the AX 2012 R3 environment over the web.</span></span> <span data-ttu-id="96581-284">**リモート デスクトップ** オプションを選択すると、ユーザーは完全なリモート デスクトップにログインできます。</span><span class="sxs-lookup"><span data-stu-id="96581-284">If you chose the **Remote Desktop** option, users will be offered the ability to login to a full remote desktop.</span></span> <span data-ttu-id="96581-285">**RemoteApp プログラム** を選択すると、ユーザーが AX 2012 R3 に直接ログインできます。</span><span class="sxs-lookup"><span data-stu-id="96581-285">If you chose **RemoteApp Programs**, users will be able to log in directly to AX 2012 R3.</span></span>
    -   <span data-ttu-id="96581-286">**RDS ファーム アクセス**: これにより、ユーザは VPN 接続されたネットワークで AX 2012 R3 環境にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="96581-286">**RDS Farm Access**: This allows users to gain access to the AX 2012 R3 environment over a VPN connected network.</span></span> <span data-ttu-id="96581-287">この機能は、次の場合にのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="96581-287">This feature is only available if you have:</span></span>
        1.  <span data-ttu-id="96581-288">この AX の配置を VPN 接続されている会社のドメインに結合しました。</span><span class="sxs-lookup"><span data-stu-id="96581-288">Joined this AX deployment to a VPN connected corporate domain.</span></span>
        2.  <span data-ttu-id="96581-289">VPN 接続されたネットワークからの接続を受け入れるように RDS ゲートウェイをコンフィギュレーションしました。</span><span class="sxs-lookup"><span data-stu-id="96581-289">Configured the RDS Gateway to accept connections from the VPN connected network.</span></span>

    <span data-ttu-id="96581-290">**注記:** **RDS Web アクセス**および **RDS ファーム アクセス**の両方で、既存の Active Directory ドメインに配置を結合する際には、内部ロード バランサーの IP アドレスを使用して、AD/DNS に RDS ファームを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-290">**Note:** For both **RDS Web Access** and **RDS Farm Access**, when joining a deployment to an existing Active Directory domain you must add the RDS Farm to your AD/DNS with the IP address of the Internal Load Balancer.</span></span> <span data-ttu-id="96581-291">次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-291">See the following steps:</span></span>
    1.  <span data-ttu-id="96581-292">RDS ファームの名前を取得します。これは、LCS の RDS ファーム アクセス リンクから入手できます。</span><span class="sxs-lookup"><span data-stu-id="96581-292">Get the name of your RDS Farm: This can be obtained from the RDS Farm Access link in LCS.</span></span> <span data-ttu-id="96581-293">この場合、**RdsFarm0c0fa75** とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-293">In this case, it should be **RdsFarm0c0fa75**.</span></span>

        <span data-ttu-id="96581-294">[![MachineName](./media/machinename-300x165.png)](./media/machinename.png)</span><span class="sxs-lookup"><span data-stu-id="96581-294">[![MachineName](./media/machinename-300x165.png)](./media/machinename.png)</span></span>

    2.  <span data-ttu-id="96581-295">Azure ポータルでクラウド サービス ダッシュ ボードから内部ロード バランサの IP を取得します。</span><span class="sxs-lookup"><span data-stu-id="96581-295">Get the IP of the Internal Load Balancer from the Cloud Service dashboard in Azure Portal.</span></span> <span data-ttu-id="96581-296">ポート **3389** の横に内部 IP がある RDS マシンを検査します。</span><span class="sxs-lookup"><span data-stu-id="96581-296">Inspect the RDS machine that has an internal IP next to port **3389**.</span></span> <span data-ttu-id="96581-297">以下の例では、内部ロード バランサーの IP は 10.1.3.4 です。</span><span class="sxs-lookup"><span data-stu-id="96581-297">In the below example, the Internal Load Balancer IP is 10.1.3.4.</span></span>

        <span data-ttu-id="96581-298">[![IP アドレス](./media/ip-address-144x300.png)](./media/ip-address.png)</span><span class="sxs-lookup"><span data-stu-id="96581-298">[![IP address](./media/ip-address-144x300.png)](./media/ip-address.png)</span></span>

    3.  <span data-ttu-id="96581-299">上記で取得した情報を使用して、AD のコンピューターとして RDS フォームを追加します。</span><span class="sxs-lookup"><span data-stu-id="96581-299">Add the RDS Farm as a Computer in your AD, using the information obtained above.</span></span>

        <span data-ttu-id="96581-300">[![AddToAD](./media/addtoad-300x113.png)](./media/addtoad.png)</span><span class="sxs-lookup"><span data-stu-id="96581-300">[![AddToAD](./media/addtoad-300x113.png)](./media/addtoad.png)</span></span>

    <span data-ttu-id="96581-301">これらの手順を実行しないと、RD Web アクセスを実行する際に次のエラーが発生します。*リモート デスクトップには、コンピューター「RdsFarm0c0fa75.contoso.com」が見つかりません。これは、「RdsFarm0c0fa75.contoso.com」が指定されたネットワークに属していないことを意味する可能性があります。接続しようとしているコンピュータ名およびドメインを確認してください。*</span><span class="sxs-lookup"><span data-stu-id="96581-301">Failure to do these steps results in the following error when going through RD Web Access: *Remote Desktop can't find the computer "RdsFarm0c0fa75.contoso.com". This might mean that " RdsFarm0c0fa75.contoso.com" does not belong to the specified network. Verify the computer name and domain that you are trying to connect to.*</span></span>
11. <span data-ttu-id="96581-302">仮想ネットワークの設定をカスタマイズするには、<strong>仮想ネットワークをカスタマイズする</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-302">To customize virtual network settings, click <strong>Customize virtual network</strong>.</span></span> <span data-ttu-id="96581-303">情報を入力するには、次の表を使用してください。</span><span class="sxs-lookup"><span data-stu-id="96581-303">Then use the following table to enter information.</span></span>
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="96581-304"><strong>以下を行う場合:</strong></span><span class="sxs-lookup"><span data-stu-id="96581-304"><strong>If you want to:</strong></span></span></td>
    <td><span data-ttu-id="96581-305"><strong>手順</strong></span><span class="sxs-lookup"><span data-stu-id="96581-305"><strong>Do this:</strong></span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="96581-306">Azure で環境用に新しい仮想ネットワークを作成する</span><span class="sxs-lookup"><span data-stu-id="96581-306">Create a new virtual network in Azure for the environment</span></span></td>
    <td><ol>
    <li><span data-ttu-id="96581-307"><strong>新しい仮想ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-307">Click <strong>New virtual network</strong>.</span></span></li>
    <li><span data-ttu-id="96581-308">仮想ネットワーク名を入力します。</span><span class="sxs-lookup"><span data-stu-id="96581-308">Enter a name for the virtual network.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="96581-309">Azure の既存の仮想ネットワークへの環境の追加</span><span class="sxs-lookup"><span data-stu-id="96581-309">Add the environment to an existing virtual network in Azure</span></span></td>
    <td><ol>
    <li><span data-ttu-id="96581-310"><strong>既存の仮想ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-310">Click <strong>Existing virtual network</strong>.</span></span></li>
    <li><span data-ttu-id="96581-311">使用する既存の仮想ネットワークの名前を選択してください。</span><span class="sxs-lookup"><span data-stu-id="96581-311">Select the name of the existing virtual network that you want to use.</span></span></li>
    <li><span data-ttu-id="96581-312"><strong>アドレス空間</strong> フィールドには、適切な値が自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-312">The <strong>Address space</strong> field will automatically display the appropriate value.</span></span> <span data-ttu-id="96581-313">提供された値を選択します。</span><span class="sxs-lookup"><span data-stu-id="96581-313">Select the provided value.</span></span></li>
    <li><span data-ttu-id="96581-314"><strong>アプリケーション サブネット名</strong> フィールドには、使用可能なオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-314">The <strong>Application subnet name</strong> field will display available options.</span></span> <span data-ttu-id="96581-315">Lifecycle Services によって以前に展開した広告に配置する場合は、選択した <strong><em>APPNET</em></strong> 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="96581-315">If you are deploying to an AD that was previously deployed through Lifecycle Services, select the <strong><em>APPNET</em></strong> value.</span></span></li>
    <li><span data-ttu-id="96581-316">Active Directory サブネットを入力する必要があり、ターゲットとする AD の Azure 管理ポータルにある Active Directory サブネット IP/範囲と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-316">The Active Directory subnet must be entered and match the Active Directory subnet IP/Range found in the Azure management portal for the AD you desire to target.</span></span>
    <ol>
    <li><span data-ttu-id="96581-317"><a href="https://manage.windowsazure.com/"><span style="color: #0066cc">Azure 管理ポータル</span></a>へのログオン</span><span class="sxs-lookup"><span data-stu-id="96581-317">Log on to the <a href="https://manage.windowsazure.com/"><span style="color: #0066cc">Azure management portal</span></a></span></span></li>
    <li><span data-ttu-id="96581-318">左のナビゲーション ウィンドウで、<strong>ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-318">In the navigation pane on the left, click <strong>Networks</strong>.</span></span></li>
    <li><span data-ttu-id="96581-319">使用する仮想ネットワークの名前をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-319">Click the name of the virtual network that you’re going to use.</span></span></li>
    <li><span data-ttu-id="96581-320"><strong>構成</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-320">Click <strong>Configure</strong>.</span></span></li>
    </ol>
<span data-ttu-id="96581-321">仮想ネットワークに関する詳細は、ページに記載されています。</span><span class="sxs-lookup"><span data-stu-id="96581-321">Details about the virtual network are listed on the page.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

12. <span data-ttu-id="96581-322">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-322">Click **Done**.</span></span> <span data-ttu-id="96581-323">**環境の展開** パネルが再表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-323">The **Deploy environment** panel is redisplayed.</span></span>
13. <span data-ttu-id="96581-324">配置される仮想マシンの数とサイズが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-324">The number and size of each virtual machine that will be deployed is listed.</span></span> <span data-ttu-id="96581-325">必要に応じて、仮想マシンの数とサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="96581-325">Change the number and size of the virtual machines, as needed.</span></span>
    -   <span data-ttu-id="96581-326">この環境で各仮想マシンにインストールされているソフトウェアの詳細については、「[Azure での Microsoft Dynamics AX 2012 R3 配置の計画](plan-2012-r3-deployment-azure.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-326">For information about the software installed on each virtual machine in this environment, see [Plan your Microsoft Dynamics AX 2012 R3 deployment on Azure](plan-2012-r3-deployment-azure.md).</span></span>
    -   <span data-ttu-id="96581-327">仮想マシンに関するサイズおよび価格決定の詳細については、[仮想マシンの価格決定の詳細](http://azure.microsoft.com/pricing/details/virtual-machines/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-327">For sizing and pricing details about virtual machines, see [Virtual machines pricing details](http://azure.microsoft.com/pricing/details/virtual-machines/).</span></span>

14. <span data-ttu-id="96581-328">ライセンスの条項を確認するには、**ソフトウェア ライセンス条項**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-328">Click **Software License Terms** to review the licensing terms and conditions.</span></span> <span data-ttu-id="96581-329">次に、チェック ボックスを選択して、条件に同意することを示します。</span><span class="sxs-lookup"><span data-stu-id="96581-329">Then select the check box to indicate that you agree to the terms.</span></span>
15. <span data-ttu-id="96581-330">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-330">Click **Next**.</span></span>
16. <span data-ttu-id="96581-331">環境を展開する準備が整った**確認するための展開**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96581-331">Click **Deploy to confirm** that you’re ready to deploy the environment.</span></span> <span data-ttu-id="96581-332">配置には数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="96581-332">The deployment may take a few hours to complete.</span></span> <span data-ttu-id="96581-333">配置が完了すると、**クラウド ホスト環境** ページの **配置ステータス** 列に **配置済み** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-333">When the deployment is done, the **Deployment Status** column on the **Cloud-hosted environments** page will display **Deployed**.</span></span> <span data-ttu-id="96581-334">(これを表示するにはブラウザーを更新する必要があります。) 配置が失敗すると、すぐエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="96581-334">(You may need to refresh your browser to see this.) If the deployment fails, you may see an error message right away.</span></span> <span data-ttu-id="96581-335">配置プロセスでエラーが後に発生する場合に、エラーの詳細がページの右側の詳細ペインに表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-335">If the error occurs later in the deployment process, error details will be displayed in the details pane on the right-side of the page.</span></span>

## <a name="6-prepare-ax-2012-r3-for-use"></a><span data-ttu-id="96581-336">6. 使用する AX 2012 R3 の準備</span><span class="sxs-lookup"><span data-stu-id="96581-336">6. Prepare AX 2012 R3 for use</span></span>
<span data-ttu-id="96581-337">環境が Azure に配置されたので、使用するために AX 2012 R3 を設定し、コンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-337">Now that the environment has been deployed on Azure, you must set up and configure AX 2012 R3 for use.</span></span> <span data-ttu-id="96581-338">詳細については、以降のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-338">See the following sections for more information.</span></span>

### <a name="log-on-to-the-aos-virtual-machine"></a><span data-ttu-id="96581-339">AOS 仮想マシンへのログオン</span><span class="sxs-lookup"><span data-stu-id="96581-339">Log on to the AOS virtual machine</span></span>

<span data-ttu-id="96581-340">AOS-&lt;GUID&gt; 仮想マシンに &lt;DomainName&gt;DynamicsInstallUser アカウントを使用してログオンします。</span><span class="sxs-lookup"><span data-stu-id="96581-340">Log on to the AOS-&lt;GUID&gt; virtual machine using the &lt;DomainName&gt;DynamicsInstallUser account.</span></span> <span data-ttu-id="96581-341">手順については、「仮想マシンにどのようにログオンしますか?」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-341">For instructions, see the “How do I log on to a virtual machine?”</span></span> <span data-ttu-id="96581-342">[Azure での Microsoft Dynamics AX 2012 R3 配置の管理](manage-2012-r3-deployment-azure.md)という記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-342">section of the [Manage your Microsoft Dynamics AX 2012 R3 deployment on Azure](manage-2012-r3-deployment-azure.md) article.</span></span>

### <a name="compile-ax-2012-r3"></a><span data-ttu-id="96581-343">AX 2012 R3 のコンパイル</span><span class="sxs-lookup"><span data-stu-id="96581-343">Compile AX 2012 R3</span></span>

<span data-ttu-id="96581-344">AxBuild.exe. を使用した AX 2012 R3 のコンパイル</span><span class="sxs-lookup"><span data-stu-id="96581-344">Compile AX 2012 R3 by using AxBuild.exe.</span></span> <span data-ttu-id="96581-345">手順については、[X++ から P コードへの AOS の並列コンパイルに対する AxBuild.exe](https://technet.microsoft.com/library/dn528954.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-345">For instructions, see [AxBuild.exe for Parallel Compile on AOS of X++ to p-code](https://technet.microsoft.com/library/dn528954.aspx).</span></span>

### <a name="initialize-ax-2012-r3"></a><span data-ttu-id="96581-346">AX 2012 R3 の初期化</span><span class="sxs-lookup"><span data-stu-id="96581-346">Initialize AX 2012 R3</span></span>

<span data-ttu-id="96581-347">AX 2012 R3 クライアントを開いて、初期化チェックリストを完了します。</span><span class="sxs-lookup"><span data-stu-id="96581-347">Open the AX 2012 R3 client and complete the initialization checklists.</span></span> <span data-ttu-id="96581-348">手順については、[初期化チェックリスト](https://technet.microsoft.com/library/aa497061.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-348">For instructions, see [Initialization checklists](https://technet.microsoft.com/library/aa497061.aspx).</span></span>

### <a name="install-sample-data"></a><span data-ttu-id="96581-349">サンプル データのインストール</span><span class="sxs-lookup"><span data-stu-id="96581-349">Install sample data</span></span>

<span data-ttu-id="96581-350">サンプル データを環境にインストールする場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="96581-350">If you want sample data installed in your environment, complete the following steps.</span></span>

1.  <span data-ttu-id="96581-351">SQL-&lt;GUID&gt; 仮想マシンにログオンします。</span><span class="sxs-lookup"><span data-stu-id="96581-351">Log on to the SQL-&lt;GUID&gt; virtual machine.</span></span> <span data-ttu-id="96581-352">DynamicsInstallUser アカウントを使用して仮想マシンにログオンします。</span><span class="sxs-lookup"><span data-stu-id="96581-352">Log on to the virtual machine using the DynamicsInstallUser account.</span></span> <span data-ttu-id="96581-353">手順については、「仮想マシンにどのようにログオンしますか?」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-353">For instructions, see the “How do I log on to a virtual machine?”</span></span> <span data-ttu-id="96581-354">[Azure での Microsoft Dynamics AX 2012 R3 配置の管理](manage-2012-r3-deployment-azure.md)という記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-354">section of the [Manage your Microsoft Dynamics AX 2012 R3 deployment on Azure](manage-2012-r3-deployment-azure.md) article.</span></span>
2.  <span data-ttu-id="96581-355">仮想マシンで次の場所に移動します: F:TestTransferTool</span><span class="sxs-lookup"><span data-stu-id="96581-355">Go to the following location on the virtual machine: F:TestTransferTool</span></span>
3.  <span data-ttu-id="96581-356">テスト データ転送ツールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="96581-356">Install the Test Data Transfer Tool.</span></span> <span data-ttu-id="96581-357">手順については、[Microsoft Dynamics AX 用のテスト データ転送ツール (ベータ版) をインストールする](install-test-data-transfer-tool-beta.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-357">For instructions, see [Install the Test Data Transfer Tool (beta) for Microsoft Dynamics AX](install-test-data-transfer-tool-beta.md).</span></span>
4.  <span data-ttu-id="96581-358">コマンド プロンプトを開いて、次の場所にアクセスします: C:\Program Files (x86) \Microsoft Dynamics AX 2012 テスト データ確認転送ツール (ベータ)</span><span class="sxs-lookup"><span data-stu-id="96581-358">Open a command prompt and navigate to the following location: C:\Program Files (x86)\Microsoft Dynamics AX 2012 Test Data Transfer Tool (Beta)</span></span>
5.  <span data-ttu-id="96581-359">次のコマンドを実行します: dp.exe import F:DemoData MicrosoftDynamicsAx</span><span class="sxs-lookup"><span data-stu-id="96581-359">Run the following command: dp.exe import F:DemoData MicrosoftDynamicsAx</span></span>

<span data-ttu-id="96581-360">**注:** サンプル データには、AX 2012 R3 の試用版のライセンス キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="96581-360">\*\*Note: \*\*The sample data includes trial license keys for AX 2012 R3.</span></span> <span data-ttu-id="96581-361">サンプル データをインストールしないように選択する場合は、開発またはテスト用の試用版ライセンス キーを [CustomerSource](https://mbs.microsoft.com/downloads/customer/AX/AXDemoTools/MicrosoftDynamicsAX2012R2v4DemoLicense.zip) または [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898#FileId=57028) からダウンロードすることができます</span><span class="sxs-lookup"><span data-stu-id="96581-361">If you choose not to install the sample data, you can download trial license keys—for development or testing purposes—from [CustomerSource](https://mbs.microsoft.com/downloads/customer/AX/AXDemoTools/MicrosoftDynamicsAX2012R2v4DemoLicense.zip) or [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898#FileId=57028).</span></span>

### <a name="give-users-access"></a><span data-ttu-id="96581-362">ユーザーのアクセス許可を付与します</span><span class="sxs-lookup"><span data-stu-id="96581-362">Give users access</span></span>

<span data-ttu-id="96581-363">ユーザが AX 2012 R3 にアクセスできるようにするには、以下のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="96581-363">To enable your users to access AX 2012 R3, complete the following tasks:</span></span>

-   <span data-ttu-id="96581-364">CLI- &lt;GUID&gt; 仮想マシンのリモート デスクトップ ユーザー グループに各ユーザーのドメイン アカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="96581-364">Add each user’s domain account to the Remote Desktop Users group on the CLI-&lt;GUID&gt; virtual machine.</span></span>
-   <span data-ttu-id="96581-365">ユーザーに AX 2012 R3 へのアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="96581-365">Give users access to AX 2012 R3.</span></span> <span data-ttu-id="96581-366">手順については、[Microsoft Dynamics AX で新しいユーザーを作成する](https://technet.microsoft.com/library/aa548139.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-366">For instructions, see [Create new users in Microsoft Dynamics AX](https://technet.microsoft.com/library/aa548139.aspx).</span></span>

<span data-ttu-id="96581-367">**注:** VPN 接続とドメイン信頼を作成しない場合でも、ユーザーに AX 2012 R3 へのアクセス権を与えることができます。</span><span class="sxs-lookup"><span data-stu-id="96581-367">\*\*Note: \*\*If you don’t want to create a VPN connection and a domain trust, you can still give users access to AX 2012 R3.</span></span> <span data-ttu-id="96581-368">これを行うには、ドメイン コントローラとして機能する仮想マシンにログオンし、各ユーザーのドメイン アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-368">To do so, you’ll need to log on to the virtual machine that serves as the domain controller, and create domain accounts for each user.</span></span> <span data-ttu-id="96581-369">その後、上記の 2 つのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96581-369">Then, you’ll need to complete the two tasks mentioned above.</span></span>

### <a name="set-up-and-configure-ax-2012-r3"></a><span data-ttu-id="96581-370">AX 2012 R3 の設定およびコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="96581-370">Set up and configure AX 2012 R3</span></span>

<span data-ttu-id="96581-371">Azure 上で AX 2012 R3 を設定およびコンフィギュレーションする手順は、オンプレミス展開の設定およびコンフィギュレーションに使用される手順と同じです。</span><span class="sxs-lookup"><span data-stu-id="96581-371">The procedures for setting up and configuring AX 2012 R3 on Azure are the same procedures used for setting up and configuring on-premises deployments.</span></span> <span data-ttu-id="96581-372">詳細については、次のリソースを参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-372">See the following resources for more information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96581-373"><strong>タスク</strong></span><span class="sxs-lookup"><span data-stu-id="96581-373"><strong>Task</strong></span></span></td>
<td><span data-ttu-id="96581-374"><strong>リソース</strong></span><span class="sxs-lookup"><span data-stu-id="96581-374"><strong>Resources</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96581-375">TechNet の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96581-375">See the instructions on TechNet</span></span></td>
<td><ul>
<li><span data-ttu-id="96581-376"><a href="https://technet.microsoft.com/library/gg732218.aspx">Microsoft Dynamics AX のシステム設定</a></span><span class="sxs-lookup"><span data-stu-id="96581-376"><a href="https://technet.microsoft.com/library/gg732218.aspx">System setup for Microsoft Dynamics AX</a></span></span></li>
<li><span data-ttu-id="96581-377"><a href="https://technet.microsoft.com/library/gg732158.aspx">Microsoft Dynamics AX クライアント</a></span><span class="sxs-lookup"><span data-stu-id="96581-377"><a href="https://technet.microsoft.com/library/gg732158.aspx">The Microsoft Dynamics AX client</a></span></span></li>
<li><span data-ttu-id="96581-378"><a href="https://technet.microsoft.com/library/gg731868.aspx">Application Object Server</a></span><span class="sxs-lookup"><span data-stu-id="96581-378"><a href="https://technet.microsoft.com/library/gg731868.aspx">Application Object Servers</a></span></span></li>
<li><span data-ttu-id="96581-379"><a href="https://technet.microsoft.com/library/ee873263.aspx">Microsoft Dynamics AX でのレポート</a></span><span class="sxs-lookup"><span data-stu-id="96581-379"><a href="https://technet.microsoft.com/library/ee873263.aspx">Reporting in Microsoft Dynamics AX</a></span></span></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96581-380"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="96581-380"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96581-381"><a href="https://technet.microsoft.com/library/dd309703.aspx">既定のレポートを展開</a>し、ユーザーに<a href="https://technet.microsoft.com/library/aa496432.aspx">アクセス権を付与</a>してください。</span><span class="sxs-lookup"><span data-stu-id="96581-381">Be sure to <a href="https://technet.microsoft.com/library/dd309703.aspx">deploy the default reports</a> and <a href="https://technet.microsoft.com/library/aa496432.aspx">grant users access</a> to them.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="96581-382"><a href="https://www.microsoft.com/download/details.aspx?id=5916">Management Reporter 2012</a></span><span class="sxs-lookup"><span data-stu-id="96581-382"><a href="https://www.microsoft.com/download/details.aspx?id=5916">Management Reporter 2012</a></span></span></li>
<li><span data-ttu-id="96581-383"><a href="https://technet.microsoft.com/library/ee873272.aspx"> Microsoft Dynamics AX での分析</a></span><span class="sxs-lookup"><span data-stu-id="96581-383"><a href="https://technet.microsoft.com/library/ee873272.aspx">Analytics in Microsoft Dynamics AX</a></span></span></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96581-384"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="96581-384"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96581-385">AX 2012 R3 に含まれているキューブを処理するには、ExternalCommandTimeout 値を 7200 に増やすことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="96581-385">To process the cubes that are included with AX 2012 R3, we recommend that you increase the ExternalCommandTimeout value to 7200.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="96581-386"><a href="https://technet.microsoft.com/library/gg866975.aspx">ヘルプ サーバー</a></span><span class="sxs-lookup"><span data-stu-id="96581-386"><a href="https://technet.microsoft.com/library/gg866975.aspx">Help server</a></span></span></li>
<li><span data-ttu-id="96581-387"><a href="https://technet.microsoft.com/library/gg751374.aspx">エンタープライズ ポータルおよびロール センター</a></span><span class="sxs-lookup"><span data-stu-id="96581-387"><a href="https://technet.microsoft.com/library/gg751374.aspx">Enterprise Portal and Role Centers</a></span></span></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96581-388"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="96581-388"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96581-389">エンタープライズ ポータルはポート 81 で実行するように設定されているため、ファイアウォール設定でそのポートを除外してください。</span><span class="sxs-lookup"><span data-stu-id="96581-389">Enterprise Portal is configured to run on port 81, so be sure to exclude that port in your firewall settings.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="96581-390"><a href="https://technet.microsoft.com/library/gg731850.aspx">エンタープライズ検索</a></span><span class="sxs-lookup"><span data-stu-id="96581-390"><a href="https://technet.microsoft.com/library/gg731850.aspx">Enterprise Search</a></span></span></li>
<li><span data-ttu-id="96581-391"><a href="https://technet.microsoft.com/library/gg731810.aspx">サービス & アプリケーション統合フレームワーク (AIF)</a></span><span class="sxs-lookup"><span data-stu-id="96581-391"><a href="https://technet.microsoft.com/library/gg731810.aspx">Services and Application Integration Framework (AIF)</a></span></span></li>
<li><span data-ttu-id="96581-392"><a href="https://technet.microsoft.com/library/jj710398.aspx">Microsoft Dynamics AX Retail IT プロおよび開発者向け</a></span><span class="sxs-lookup"><span data-stu-id="96581-392"><a href="https://technet.microsoft.com/library/jj710398.aspx">Microsoft Dynamics AX Retail for IT pros and developers</a></span></span></li>
<li><span data-ttu-id="96581-393"><a href="https://technet.microsoft.com/library/aa834453.aspx">.NET Business Connector</a></span><span class="sxs-lookup"><span data-stu-id="96581-393"><a href="https://technet.microsoft.com/library/aa834453.aspx">.NET Business Connector</a></span></span></li>
<li><span data-ttu-id="96581-394"><a href="https://technet.microsoft.com/library/gg731779.aspx">セキュリティ</a></span><span class="sxs-lookup"><span data-stu-id="96581-394"><a href="https://technet.microsoft.com/library/gg731779.aspx">Security</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96581-395">印刷可能なガイドおよびホワイト ペーパーの表示</span><span class="sxs-lookup"><span data-stu-id="96581-395">View printable guides and white papers</span></span></td>
<td><ul>
<li><span data-ttu-id="96581-396"><a href="https://technet.microsoft.com/library/gg732268.aspx">印刷可能なガイド</a></span><span class="sxs-lookup"><span data-stu-id="96581-396"><a href="https://technet.microsoft.com/library/gg732268.aspx">Printable guides</a></span></span></li>
<li><span data-ttu-id="96581-397"><a href="https://technet.microsoft.com/library/gg188985.aspx">システム管理者向けのホワイト ペーパー</a></span><span class="sxs-lookup"><span data-stu-id="96581-397"><a href="https://technet.microsoft.com/library/gg188985.aspx">White papers for system administrators</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96581-398">Microsoft Dynamics AX ウェブ検索ツールの使用</span><span class="sxs-lookup"><span data-stu-id="96581-398">Use the Microsoft Dynamics AX web search tool</span></span></td>
<td><ul>
<li><span data-ttu-id="96581-399"><a href="http://go.microsoft.com/fwlink/?LinkID=212924">開発者用の Web 検索</a></span><span class="sxs-lookup"><span data-stu-id="96581-399"><a href="http://go.microsoft.com/fwlink/?LinkID=212924">Web search for developers</a></span></span></li>
<li><span data-ttu-id="96581-400"><a href="http://go.microsoft.com/fwlink/?LinkID=212925">システム管理者用の Web 検索</a></span><span class="sxs-lookup"><span data-stu-id="96581-400"><a href="http://go.microsoft.com/fwlink/?LinkID=212925">Web search for system administrators</a></span></span></li>
<li><span data-ttu-id="96581-401"><a href="http://go.microsoft.com/fwlink/?LinkID=212922">アプリケーション ユーザー用の Web 検索</a></span><span class="sxs-lookup"><span data-stu-id="96581-401"><a href="http://go.microsoft.com/fwlink/?LinkID=212922">Web search for application users</a></span></span></li>
<li><span data-ttu-id="96581-402"><a href="http://go.microsoft.com/fwlink/?LinkID=194311">結合された Web 検索</a></span><span class="sxs-lookup"><span data-stu-id="96581-402"><a href="http://go.microsoft.com/fwlink/?LinkID=194311">Combined web search</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="7-learn-more-about-the-service-accounts-for-this-environment"></a><span data-ttu-id="96581-403">7. この環境のサービス アカウントに関する詳細</span><span class="sxs-lookup"><span data-stu-id="96581-403">7. Learn more about the service accounts for this environment</span></span>
<span data-ttu-id="96581-404">次のセクションでは、環境を配置したときに作成されたサービス アカウントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="96581-404">The following sections provide information about the service accounts that were created when you deployed the environment.</span></span>

### <a name="domain-accounts"></a><span data-ttu-id="96581-405">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="96581-405">Domain accounts</span></span>

<span data-ttu-id="96581-406">次のテーブルに、環境を配置したときに作成されたドメイン アカウントの既定の名前を示します。</span><span class="sxs-lookup"><span data-stu-id="96581-406">The following table lists the default names of the domain accounts that were created when you deployed the environment.</span></span>

| <span data-ttu-id="96581-407">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="96581-407">Domain account</span></span>                  | <span data-ttu-id="96581-408">説明</span><span class="sxs-lookup"><span data-stu-id="96581-408">Description</span></span>                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96581-409"><DomainName>AOSServiceUser</span><span class="sxs-lookup"><span data-stu-id="96581-409"><DomainName>AOSServiceUser</span></span>      | <span data-ttu-id="96581-410">次のサービスを AOS-<GUID> 仮想マシンで実行するために使用されたアカウント: Microsoft Dynamics AX Object Server。</span><span class="sxs-lookup"><span data-stu-id="96581-410">The account used to run the following services on AOS-<GUID> virtual machines: Microsoft Dynamics AX Object Server.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="96581-411"><DomainName>SQLServiceUser</span><span class="sxs-lookup"><span data-stu-id="96581-411"><DomainName>SQLServiceUser</span></span>      | <span data-ttu-id="96581-412">次のサービスを SQL で実行するために使用されるアカウント -<GUID> 仮想マシン: SQL Server Analysis Services (MSSQLSERVER)。</span><span class="sxs-lookup"><span data-stu-id="96581-412">The account used to run the following services on SQL-<GUID> virtual machines: SQL Server Analysis Services (MSSQLSERVER)</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="96581-413"><DomainName>DynamicsInstallUser</span><span class="sxs-lookup"><span data-stu-id="96581-413"><DomainName>DynamicsInstallUser</span></span> | <span data-ttu-id="96581-414">AX 2012 R3 をインストールするために使用したアカウント。</span><span class="sxs-lookup"><span data-stu-id="96581-414">The account used to install AX 2012 R3.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="96581-415"><DomainName>SPServiceUser</span><span class="sxs-lookup"><span data-stu-id="96581-415"><DomainName>SPServiceUser</span></span>       | <span data-ttu-id="96581-416">次のサービスを EP-<GUID> 仮想マシンで実行するために使用したアカウント - : AppFabric、SharePoint Search Host Controller、SharePoint Server Search 15、SharePoint Timer Service、および SharePoint User Code Host。</span><span class="sxs-lookup"><span data-stu-id="96581-416">The account used to run the following services on EP-<GUID> virtual machines: AppFabric, SharePoint Search Host Controller, SharePoint Server Search 15, SharePoint Timer Service, and SharePoint User Code Host</span></span>                                                                                                                                         |
| <span data-ttu-id="96581-417"><DomainName>BCProxyUser</span><span class="sxs-lookup"><span data-stu-id="96581-417"><DomainName>BCProxyUser</span></span>         | <span data-ttu-id="96581-418">ビジネス コネクタ プロキシとして使用されるアカウント。</span><span class="sxs-lookup"><span data-stu-id="96581-418">The account used as the Business Connector proxy.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="96581-419"><DomainName>AXServiceUser</span><span class="sxs-lookup"><span data-stu-id="96581-419"><DomainName>AXServiceUser</span></span>       | <span data-ttu-id="96581-420">AOS<GUID> 仮想マシンで次のサービスを実行するためにアカウントが使用されます: Microsoft Dynamics AX Data Import/Export Framework Service および Microsoft Dynamics ERP RapidStart Connector。</span><span class="sxs-lookup"><span data-stu-id="96581-420">The account used to run the following services on AOS-<GUID> virtual machines: Microsoft Dynamics AX Data Import/Export Framework Services and Microsoft Dynamics ERP RapidStart Connector.</span></span> <span data-ttu-id="96581-421">アカウントは、次のサービスを CLI-<GUID> 仮想マシンで実行するためにも使用されます: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client。</span><span class="sxs-lookup"><span data-stu-id="96581-421">The account is also used to run the following services on CLI-<GUID> virtual machines: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client.</span></span> |

<span data-ttu-id="96581-422">**注記:** パスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) のクラウド ホスト 環境ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-422">**Note:** The passwords are displayed on the Cloud-hosted environments page in [Lifecycle Services](https://lifecycleservices.dynamics.com/en/).</span></span>



### <a name="local-administrator-accounts"></a><span data-ttu-id="96581-423">ローカル管理者アカウント</span><span class="sxs-lookup"><span data-stu-id="96581-423">Local administrator accounts</span></span>

<span data-ttu-id="96581-424">配置した各仮想マシンには、ローカル Administrator アカウントがあります。</span><span class="sxs-lookup"><span data-stu-id="96581-424">Each virtual machine that you deployed has a local administrator account.</span></span> <span data-ttu-id="96581-425">このアカウントは builtinaxlocaladmin です。</span><span class="sxs-lookup"><span data-stu-id="96581-425">This account is: builtinaxlocaladmin.</span></span> <span data-ttu-id="96581-426">ローカル管理者アカウントのパスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) の クラウド ホスト 環境ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="96581-426">The passwords for the local administrator accounts are displayed on the Cloud-hosted environments page in [Lifecycle Services](https://lifecycleservices.dynamics.com/en/).</span></span>



