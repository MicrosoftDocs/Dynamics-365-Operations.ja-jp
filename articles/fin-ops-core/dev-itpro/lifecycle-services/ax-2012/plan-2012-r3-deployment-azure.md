---
title: Azure 上での AX 2012 R3の 配置計画
description: Microsoft Azure に Microsoft Dynamics AX 2012 R3 を展開する前に、いくつかの点を考慮し決定する必要があります。 この記事では、計画プロセスについて説明します。
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 18591
ms.assetid: 84e597d7-6ad3-4322-8ac3-6b6151dd24f6
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 624f7ec6c93928077cb4cd2b1ec42f7a96debd68
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183239"
---
# <a name="plan-ax-2012-r3-deployments-on-azure"></a><span data-ttu-id="421bc-104">Azure 上での AX 2012 R3の 配置計画</span><span class="sxs-lookup"><span data-stu-id="421bc-104">Plan AX 2012 R3 deployments on Azure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="421bc-105">Microsoft Azure に Microsoft Dynamics AX 2012 R3 を展開する前に、いくつかの点を考慮し決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-105">Before you can deploy Microsoft Dynamics AX 2012 R3 on Microsoft Azure, there are several things you must consider and decisions you must make.</span></span> <span data-ttu-id="421bc-106">この記事では、計画プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="421bc-106">This article guides you through the planning process.</span></span> 

<span data-ttu-id="421bc-107">Azure 上の AX 2012 R3 の配備は、Microsoft が次のシナリオでサポートしています。</span><span class="sxs-lookup"><span data-stu-id="421bc-107">Deployments of AX 2012 R3 on Azure are supported by Microsoft in the following scenarios:</span></span> 
- <span data-ttu-id="421bc-108">配置は、Microsoft Dynamics Lifecycle Services (LCS) を通じて実行されています。</span><span class="sxs-lookup"><span data-stu-id="421bc-108">The deployment has been performed through Microsoft Dynamics Lifecycle Services (LCS).</span></span> 
- <span data-ttu-id="421bc-109">以下のガイダンスに厳密に従って実施された顧客またはパートナー主導配置。</span><span class="sxs-lookup"><span data-stu-id="421bc-109">Customer or partner-driven deployments that have been performed strictly adhering to the following guidance:</span></span> 
   - <span data-ttu-id="421bc-110">SQL は、(SQL クラスタリング/Always On を使用して) 可用性トポロジに配置されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-110">SQL is deployed in a High Availability topology (using SQL Clustering/Always On).</span></span>
   - <span data-ttu-id="421bc-111">Azure に配置するために、[Azure 仮想マシンでの SQL Server のパフォーマンス ベスト プラクティス](/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)を使用して、SQL のベスト プラクティスに従っています。</span><span class="sxs-lookup"><span data-stu-id="421bc-111">SQL best practices have been followed for deployment in Azure, using the [Performance best practices for SQL Server in Azure Virtual Machines](/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance).</span></span> 
   - <span data-ttu-id="421bc-112">[SQL サーバーおよび記憶域の設定のコンフィギュレーション (TechNet)](https://technet.microsoft.com/library/dd309734.aspx) によって指定された AX 2012 の SQL Server コンフィギュレーションのベスト プラクティスに従っています。</span><span class="sxs-lookup"><span data-stu-id="421bc-112">Best practices for SQL Server configuration for AX 2012 have been followed, as specified in [Configure SQL Server and storage settings (TechNet)](https://technet.microsoft.com/library/dd309734.aspx).</span></span> 
   - <span data-ttu-id="421bc-113">[システム診断](system-diagnostics-lcs.md)で指定されているように、システム診断ツールがインストールされ、ベスト プラクティスに従います。</span><span class="sxs-lookup"><span data-stu-id="421bc-113">The System diagnostic tool is installed and best practices are followed, as specified in [System diagnostics](system-diagnostics-lcs.md)</span></span> 

> [!NOTE]
> <span data-ttu-id="421bc-114">Azure 環境でサポートされていない AX 2012 R3 に問題があり、LCS 経由で Azure に展開された、またはローカルに展開された AX 2012 R3 環境で同じ問題を再現することができる場合、Microsoft がサポートを提供できます。</span><span class="sxs-lookup"><span data-stu-id="421bc-114">If you have an issue in an unsupported AX 2012 R3 on Azure environment, and can reproduce the same issue in an AX 2012 R3 environment that was either deployed to Azure through LCS, or deployed locally, Microsoft can provide support.</span></span>
> 
> <span data-ttu-id="421bc-115">AX 2012 R3 は、オンプレミスでも配置できます。</span><span class="sxs-lookup"><span data-stu-id="421bc-115">AX 2012 R3 can also be deployed on-premises.</span></span> <span data-ttu-id="421bc-116">詳細については、[Microsoft Dynamics AX 2012 のインストール](https://technet.microsoft.com/library/dd362138.aspx) のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-116">For details, see the topic [Install Microsoft Dynamics AX 2012](https://technet.microsoft.com/library/dd362138.aspx).</span></span>

## <a name="verify-that-you-can-log-on-to-lifecycle-services"></a><span data-ttu-id="421bc-117">Lifecycle Services にログオンできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="421bc-117">Verify that you can log on to Lifecycle Services</span></span>
<span data-ttu-id="421bc-118">Lifecycle Services (LCS) は、顧客およびパートナーが Microsoft Dynamics AX プロジェクトの管理に使用できるクラウドベースの共同ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="421bc-118">Lifecycle Services (LCS) is a cloud-based collaborative workspace that customers and partners can use to manage Microsoft Dynamics AX projects.</span></span> <span data-ttu-id="421bc-119">Azure 上に AX 2012 R3 を配置するには、Lifecycle Services Web サイトで利用できるクラウド ホスト環境ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="421bc-119">You’ll use the Cloud-hosted environments tool, available on the Lifecycle Services website, to deploy AX 2012 R3 on Azure.</span></span> <span data-ttu-id="421bc-120">Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="421bc-120">Lifecycle Services is available to customers and partners as part of their support plans.</span></span> <span data-ttu-id="421bc-121">CustomerSource または PartnerSource の資格情報でアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="421bc-121">You can access it with your CustomerSource or PartnerSource credentials.</span></span> [<span data-ttu-id="421bc-122">Lifecycle Services にログオンできることを確認する</span><span class="sxs-lookup"><span data-stu-id="421bc-122">Verify that you can log on to Lifecycle Services</span></span>](https://lcs.dynamics.com/)

## <a name="purchase-an-azure-subscription"></a><span data-ttu-id="421bc-123">Azure サブスクリプションの購買</span><span class="sxs-lookup"><span data-stu-id="421bc-123">Purchase an Azure subscription</span></span>
<span data-ttu-id="421bc-124">Azure を使用するには、サブスクリプションを購入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-124">To use Azure, you must purchase a subscription.</span></span> <span data-ttu-id="421bc-125">サブスクリプション プランおよび価格決定の詳細については、[Azure 価格決定](https://azure.microsoft.com/pricing/) ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-125">For information about subscription plans and pricing details, see the [Azure pricing](https://azure.microsoft.com/pricing/) page.</span></span> <span data-ttu-id="421bc-126">その後、そのページの指示に従ってサブスクリプションを購入します。</span><span class="sxs-lookup"><span data-stu-id="421bc-126">Then follow the instructions on that page to purchase a subscription.</span></span> <span data-ttu-id="421bc-127">サブスクリプションは、Azure に配備する AX 2012 R3 環境をサポートするのに十分な大きさでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="421bc-127">The subscription must be large enough to support the AX 2012 R3 environment that you want to deploy on Azure.</span></span> <span data-ttu-id="421bc-128">次のテーブルは、Azure に配置できる AX 2012 R3 環境のタイプと、各環境を既定のコンフィギュレーションで配置するために必要なコアの数を示しています。</span><span class="sxs-lookup"><span data-stu-id="421bc-128">The following table lists the types of AX 2012 R3 environments that you can deploy on Azure, and the number of cores required to deploy each environment in its default configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="421bc-129">環境を配置するときに、配置される仮想マシンの数とサイズを変更できることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-129">Keep in mind that when you deploy an environment, you can change the number and size of the virtual machines that are deployed.</span></span> <span data-ttu-id="421bc-130">ただし、次のテーブルでは、その*既定*コンフィギュレーションで各環境を配置するために必要なコアの数を一覧にします。</span><span class="sxs-lookup"><span data-stu-id="421bc-130">However, this table lists the number of cores required to deploy each environment in its *default* configuration.</span></span>

<span data-ttu-id="421bc-131">**環境タイプ:** - デモ</span><span class="sxs-lookup"><span data-stu-id="421bc-131">**Environment type:** - Demo</span></span>


| <span data-ttu-id="421bc-132">環境名</span><span class="sxs-lookup"><span data-stu-id="421bc-132">Environment name</span></span>       | <span data-ttu-id="421bc-133">既定の構成で環境を配置するコアの数</span><span class="sxs-lookup"><span data-stu-id="421bc-133">Number of cores to deploy the environment in its default configuration</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="421bc-134">AX 2012 R3 デモ</span><span class="sxs-lookup"><span data-stu-id="421bc-134">AX 2012 R3 demo</span></span>        | <span data-ttu-id="421bc-135">8 コア</span><span class="sxs-lookup"><span data-stu-id="421bc-135">8 cores</span></span>                                                                |
| <span data-ttu-id="421bc-136">AX 2012 R3 CU8 デモ</span><span class="sxs-lookup"><span data-stu-id="421bc-136">AX 2012 R3 CU8 demo</span></span>    | <span data-ttu-id="421bc-137">8 コア</span><span class="sxs-lookup"><span data-stu-id="421bc-137">8 cores</span></span>                                                                |
| <span data-ttu-id="421bc-138">Retail Essentials デモ</span><span class="sxs-lookup"><span data-stu-id="421bc-138">Retail essentials demo</span></span> | <span data-ttu-id="421bc-139">8 コア</span><span class="sxs-lookup"><span data-stu-id="421bc-139">8 cores</span></span>                                                                |


<span data-ttu-id="421bc-140">**環境タイプ:** - 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="421bc-140">**Environment type:** - Dev/test</span></span>


| <span data-ttu-id="421bc-141">環境名</span><span class="sxs-lookup"><span data-stu-id="421bc-141">Environment name</span></span>                   | <span data-ttu-id="421bc-142">既定の構成で環境を配置するコアの数</span><span class="sxs-lookup"><span data-stu-id="421bc-142">Number of cores to deploy the environment in its default configuration</span></span> |
|------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="421bc-143">開発</span><span class="sxs-lookup"><span data-stu-id="421bc-143">Development</span></span>                        | <span data-ttu-id="421bc-144">9 コア</span><span class="sxs-lookup"><span data-stu-id="421bc-144">9 cores</span></span>                                                                |
| <span data-ttu-id="421bc-145">共有 SQL Server による開発</span><span class="sxs-lookup"><span data-stu-id="421bc-145">Development with shared SQL Server</span></span> | <span data-ttu-id="421bc-146">14 コア</span><span class="sxs-lookup"><span data-stu-id="421bc-146">14 cores</span></span>                                                               |
| <span data-ttu-id="421bc-147">テスト</span><span class="sxs-lookup"><span data-stu-id="421bc-147">Test</span></span>                               | <span data-ttu-id="421bc-148">13 コア</span><span class="sxs-lookup"><span data-stu-id="421bc-148">13 cores</span></span>                                                               |
| <span data-ttu-id="421bc-149">Retail Essentials 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="421bc-149">Retail essentials dev/test</span></span>         | <span data-ttu-id="421bc-150">4 コア</span><span class="sxs-lookup"><span data-stu-id="421bc-150">4 cores</span></span>                                                                |
| <span data-ttu-id="421bc-151">Retail E-commerce 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="421bc-151">Retail e-commerce dev/test</span></span>         | <span data-ttu-id="421bc-152">4 コア</span><span class="sxs-lookup"><span data-stu-id="421bc-152">4 cores</span></span>                                                                |
| <span data-ttu-id="421bc-153">Retail Mobility 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="421bc-153">Retail mobility dev/test</span></span>           | <span data-ttu-id="421bc-154">4 コア</span><span class="sxs-lookup"><span data-stu-id="421bc-154">4 cores</span></span>                                                                |


<span data-ttu-id="421bc-155">**環境タイプ:** - 高可用性</span><span class="sxs-lookup"><span data-stu-id="421bc-155">**Environment type:** - High availability</span></span>


| <span data-ttu-id="421bc-156">環境名</span><span class="sxs-lookup"><span data-stu-id="421bc-156">Environment name</span></span>              | <span data-ttu-id="421bc-157">既定の構成で環境を配置するコアの数</span><span class="sxs-lookup"><span data-stu-id="421bc-157">Number of cores to deploy the environment in its default configuration</span></span> |
|-------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="421bc-158">高可用性環境</span><span class="sxs-lookup"><span data-stu-id="421bc-158">High availability environment</span></span> | <span data-ttu-id="421bc-159">45 コア</span><span class="sxs-lookup"><span data-stu-id="421bc-159">45 cores</span></span>                                                               |


<span data-ttu-id="421bc-160">Azure のサブスクリプションを既に持っている場合、次に注意します。</span><span class="sxs-lookup"><span data-stu-id="421bc-160">If you already have an Azure subscription, note the following:</span></span>

-   <span data-ttu-id="421bc-161">**定期売買のサイズを表示する:** Azure 管理ポータルで、定期売買のサイズを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="421bc-161">**To view the size of your subscription:** You can view the size of your subscription in the Azure management portal.</span></span> <span data-ttu-id="421bc-162">これを行うには、[[Azure管理ポータル](https://manage.windowsazure.com/)] にログオンし、**設定**&gt;**使用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="421bc-162">To do so, log on to the [Azure management portal](https://manage.windowsazure.com/), and then click **Settings** &gt; **Usage**.</span></span>
-   <span data-ttu-id="421bc-163">**定期購読のサイズを増やす:** 定期売買のサイズを増やすには、Azure サポート チームにてサポート チケットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-163">**To increase the size of your subscription:** To increase the size of your subscription, you’ll need to create a support ticket with the Azure support team.</span></span> <span data-ttu-id="421bc-164">これを行うには、[[Azure サポート オプション](http://azure.microsoft.com/support/options/)] ページに移動し、**サポートを受ける** をクリックしてサポート チケットを作成します。</span><span class="sxs-lookup"><span data-stu-id="421bc-164">To do so, go to the [Azure support options](http://azure.microsoft.com/support/options/) page, and then click **Get Support** to create the support ticket.</span></span> <span data-ttu-id="421bc-165">サポート チケットを作成するとき、チケットが課金サポートに対応していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="421bc-165">When creating the support ticket, be sure to indicate that the ticket is for billing support.</span></span>

> [!NOTE]
> <span data-ttu-id="421bc-166">クラウド ソリューション プロバイダー (CSP) プログラムは、Azure Resource Manager (ARM) 要件のため Lifecycle Services によって現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="421bc-166">The Cloud Solution Provider (CSP) program is currently not supported with Lifecycle Services due to the Azure Resource Manager (ARM) requirement.</span></span>

## <a name="purchase-and-azure-support-plan"></a><span data-ttu-id="421bc-167">発注書および Azure サポート計画</span><span class="sxs-lookup"><span data-stu-id="421bc-167">Purchase and Azure support plan</span></span>
<span data-ttu-id="421bc-168">Azure サポート計画では Azure の技術および課金サポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="421bc-168">Azure support plans provide technical and billing support for Azure.</span></span> <span data-ttu-id="421bc-169">Azure サポート プランは、Azure 展開のサポーの適切なレベルを選択できる柔軟なサポート オプションを提供しています。</span><span class="sxs-lookup"><span data-stu-id="421bc-169">The Azure support plans offer flexible support options that will allow you to select the right level of support for your Azure deployment.</span></span> <span data-ttu-id="421bc-170">サポート オプションには、Azure サブスクリプションに含まれているサポート サービスから、無料のサポート サービスまでさまざまです。</span><span class="sxs-lookup"><span data-stu-id="421bc-170">The support options range from support services included with your Azure subscription at no charge to premier support services.</span></span> <span data-ttu-id="421bc-171">利用可能なサポート プランについて学び、プランを購入するには、[[Azure サポート計画](http://www.windowsazure.com/support/plans/)] ページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="421bc-171">To learn about the available support plans and to purchase a plan, see the [Azure support plans](http://www.windowsazure.com/support/plans/) page.</span></span>

## <a name="become-familiar-with-the-azure-management-portal"></a><span data-ttu-id="421bc-172">Azure 管理ポータルを使いこなせるようになります</span><span class="sxs-lookup"><span data-stu-id="421bc-172">Become familiar with the Azure management portal</span></span>
<span data-ttu-id="421bc-173">Azure 管理ポータルは、開発者および IT プロフェッショナルに、その Azure コンポーネントをプロビジョニング、構成、監視、および管理する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="421bc-173">The Azure management portal provides developers and IT professionals the ability to provision, configure, monitor, and manage their Azure components.</span></span> <span data-ttu-id="421bc-174">今後使用するために、管理ポータルについてよく理解しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="421bc-174">It’s important to become familiar with the management portal because you’ll use it to:</span></span>

-   <span data-ttu-id="421bc-175">管理証明書をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="421bc-175">Upload a management certificate.</span></span> <span data-ttu-id="421bc-176">(管理証明書を使用すると、Lifecycle Services はユーザーに代わって Azure に AX 2012 R3 環境を配置できます。)</span><span class="sxs-lookup"><span data-stu-id="421bc-176">(The management certificate enables Lifecycle Services to deploy AX 2012 R3 environments on Azure on your behalf.)</span></span>
-   <span data-ttu-id="421bc-177">仮想マシンに接続します。</span><span class="sxs-lookup"><span data-stu-id="421bc-177">Connect to virtual machines.</span></span>
-   <span data-ttu-id="421bc-178">AX 2012 R3 環境の正常性および状態を監視します。</span><span class="sxs-lookup"><span data-stu-id="421bc-178">Monitor the health and status of your AX 2012 R3 environment.</span></span>

<span data-ttu-id="421bc-179">Azure サブスクリプションを購入した後、[ここ。](https://manage.windowsazure.com/?whr=live.com) をクリックして管理ポータルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="421bc-179">After you purchase an Azure subscription, you can access the management portal by clicking [here.](https://manage.windowsazure.com/?whr=live.com)</span></span> <span data-ttu-id="421bc-180">次の図は、管理ポータルを示しています。</span><span class="sxs-lookup"><span data-stu-id="421bc-180">The following image shows the management portal.</span></span> <span data-ttu-id="421bc-181">[![PlanYouAXR3DeploymentonAzure1](./media/planyouaxr3deploymentonazure1.jpg)](./media/planyouaxr3deploymentonazure1.jpg)</span><span class="sxs-lookup"><span data-stu-id="421bc-181">[![PlanYouAXR3DeploymentonAzure1](./media/planyouaxr3deploymentonazure1.jpg)](./media/planyouaxr3deploymentonazure1.jpg)</span></span>  

## <a name="become-familiar-with-the-azure-vm-agent"></a><span data-ttu-id="421bc-182">Azure VM エージェントを使いこなせるようになります</span><span class="sxs-lookup"><span data-stu-id="421bc-182">Become familiar with the Azure VM agent</span></span>
<span data-ttu-id="421bc-183">Azure VM エージェントは、Lifecycle Services を通じて展開されたすべての VM で自動的に配置されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-183">The Azure VM Agent is now automatically deployed with every VM deployed via Lifecycle Services.</span></span> <span data-ttu-id="421bc-184">Azure VM エージェントは、Azure 仮想マシン拡張 (VM 拡張) インストール、コンフィギュレーション、管理、実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-184">The Azure VM Agent is used to install, configure, manage and run Azure Virtual Machine Extensions (VM Extensions).</span></span> <span data-ttu-id="421bc-185">VM 拡張機能は、VM を監視および管理するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="421bc-185">VM extensions can help you monitor and manage your VMs.</span></span>

## <a name="consider-cloud-services-resource-requirements"></a><span data-ttu-id="421bc-186">クラウド サービスのリソース要件を検討する</span><span class="sxs-lookup"><span data-stu-id="421bc-186">Consider Cloud Services resource requirements</span></span>
<span data-ttu-id="421bc-187">トポロジが配置されると、配置システムは選択された仮想マシン (VM) の SKU を検査します。</span><span class="sxs-lookup"><span data-stu-id="421bc-187">When a topology is deployed, the deployment system will inspect the virtual machine (VM) SKUs that were selected.</span></span> <span data-ttu-id="421bc-188">Azure がこれらの VM を VM が使用可能である適切なクラスターに配置していることを確認するために、VM SKU の各レベルに独自の Azure クラウド サービスが必要です。</span><span class="sxs-lookup"><span data-stu-id="421bc-188">In order to ensure that Azure deploys these VMs to the proper clusters where the VMs are available, each level of VM SKU must have its own Azure Cloud Service.</span></span> <span data-ttu-id="421bc-189">VM SKU の内訳は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="421bc-189">The VM SKU breakdown is as follows:</span></span>

|         |                                 |
|---------|---------------------------------|
| <span data-ttu-id="421bc-190">**最小在庫管理単位**</span><span class="sxs-lookup"><span data-stu-id="421bc-190">**SKU**</span></span> | <span data-ttu-id="421bc-191">**サイズ**</span><span class="sxs-lookup"><span data-stu-id="421bc-191">**Size**</span></span>                        |
| <span data-ttu-id="421bc-192">A</span><span class="sxs-lookup"><span data-stu-id="421bc-192">A</span></span>       | <span data-ttu-id="421bc-193">標準 A の \[A0-A4\]</span><span class="sxs-lookup"><span data-stu-id="421bc-193">Standard A’s \[A0-A4\]</span></span>          |
| <span data-ttu-id="421bc-194">午前</span><span class="sxs-lookup"><span data-stu-id="421bc-194">AM</span></span>      | <span data-ttu-id="421bc-195">標準 A の \[A5-A7\]</span><span class="sxs-lookup"><span data-stu-id="421bc-195">Standard A's \[A5-A7\]</span></span>          |
| <span data-ttu-id="421bc-196">AL</span><span class="sxs-lookup"><span data-stu-id="421bc-196">AL</span></span>      | <span data-ttu-id="421bc-197">標準 A の (大) \[A8-A11\]</span><span class="sxs-lookup"><span data-stu-id="421bc-197">Standard A’s (large) \[A8-A11\]</span></span> |
| <span data-ttu-id="421bc-198">D</span><span class="sxs-lookup"><span data-stu-id="421bc-198">D</span></span>       | <span data-ttu-id="421bc-199">標準 D の\[すべての D シリーズ\]</span><span class="sxs-lookup"><span data-stu-id="421bc-199">Standard D’s \[all D series\]</span></span>   |
| <span data-ttu-id="421bc-200">DS</span><span class="sxs-lookup"><span data-stu-id="421bc-200">DS</span></span>      | <span data-ttu-id="421bc-201">標準 DS の\[すべての DS シリーズ\]</span><span class="sxs-lookup"><span data-stu-id="421bc-201">Standard DS’s \[all DS series\]</span></span> |
| <span data-ttu-id="421bc-202">G</span><span class="sxs-lookup"><span data-stu-id="421bc-202">G</span></span>       | <span data-ttu-id="421bc-203">標準 G の\[すべての G シリーズ\]</span><span class="sxs-lookup"><span data-stu-id="421bc-203">Standard G’s \[all G series\]</span></span>   |

<span data-ttu-id="421bc-204">Version-Topology-EnvironmentName-SKU-GUID という名前付けスキームを含むクラウド サービスが作成されます。必要に応じて、配置のためのクラウド サービス リソース要件を検討し、Azure サポートから Azure サブスクリプションの追加クラウド サービス能力を要求してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-204">A Cloud Service will be created with the following naming scheme: Version-Topology-EnvironmentName-SKU-GUID Please consider the Cloud Services resource requirements for your deployments and request additional Cloud Services capacity in your Azure Subscription from Azure Support if necessary.</span></span>

## <a name="plan-for-storage-accounts"></a><span data-ttu-id="421bc-205">ストレージ アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="421bc-205">Plan for storage accounts</span></span>
<span data-ttu-id="421bc-206">Lifecycle Services で作成された各プロジェクトについては、1 つまたは複数の個別のストレージ アカウントが Azure 定期売買で作成されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-206">For each project created in Lifecycle Services, one or more distinct storage accounts will be created in the Azure subscription.</span></span> <span data-ttu-id="421bc-207">ストレージ アカウントは、プロジェクトを Azure サブスクリプションに接続すると作成されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-207">A storage account is created when you connect your project to your Azure subscription.</span></span> <span data-ttu-id="421bc-208">このストレージ アカウントは、ローカル冗長ストレージ (LRS) アカウントであり、展開に必要なスクリプトと VHD を格納するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-208">This storage account is a Locally Redundant Storage (LRS) account, and is used to house scripts and VHDs which are required for deployments.</span></span> <span data-ttu-id="421bc-209">最初の Premium ストレージ有効トポロジがプロジェクトから配置されると、各プロジェクトが作成され Premium ストレージ アカウントが追加されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-209">An additional Premium storage account is created for each project when the first Premium storage-enabled topology is deployed from the project.</span></span> <span data-ttu-id="421bc-210">ストレージ アカウントは、配置が同じ Azure サブスクリプションに行われる場合でも、Lifecycle Services プロジェクト間で共有されません。</span><span class="sxs-lookup"><span data-stu-id="421bc-210">Storage accounts are not shared across Lifecycle Services projects, even if the deployments are to the same Azure subscription.</span></span> <span data-ttu-id="421bc-211">Premium ストレージ アカウントが作成されると、それもまた LRS として作成されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-211">When a Premium storage account is created, it too is created as LRS.</span></span> <span data-ttu-id="421bc-212">ストレージの詳細については、[ここ](http://azure.microsoft.com/pricing/details/storage) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="421bc-212">For more information about storage, click [here](http://azure.microsoft.com/pricing/details/storage).</span></span> <span data-ttu-id="421bc-213">同じ Lifecycle Services (LCS) プロジェクトと Azure コネクタに展開されるトポロジと環境の数を検討します。</span><span class="sxs-lookup"><span data-stu-id="421bc-213">Consider which topologies and the number of environments that will be deployed into the same Lifecycle Services (LCS) project and Azure Connector.</span></span> <span data-ttu-id="421bc-214">Premium ストレージ アカウントとは別に、既定では、LCS プロジェクトおよび Azure コネクタごとにストレージ アカウントが 1 つ存在します。</span><span class="sxs-lookup"><span data-stu-id="421bc-214">Premium storage account aside, by default there is 1 storage account for each LCS project and Azure Connector.</span></span> <span data-ttu-id="421bc-215">Azure Storage には[限度](https://azure.microsoft.com/documentation/articles/azure-subscription-service-limits/#storage-limits)があるので注意してください。具体的には、標準ストレージ アカウントあたり 20,000 IOPS (秒単位の入力/出力オペレーション) です。</span><span class="sxs-lookup"><span data-stu-id="421bc-215">Be aware that Azure storage has [limits](https://azure.microsoft.com/documentation/articles/azure-subscription-service-limits/#storage-limits), specifically 20,000 IOPS (input/output operations per second) per standard storage account.</span></span> <span data-ttu-id="421bc-216">VHD あたり 500 IOPS と組み合わせると、調整が発生する前に約 40 個の***利用効率が高い*** VHDが残されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-216">Combined with 500 IOPS per VHD, that leaves roughly 40 ***highly utilized*** VHDs before throttling occurs.</span></span> <span data-ttu-id="421bc-217">これを軽減するには、複数の Azure コネクタや複数の LCS プロジェクトを活用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="421bc-217">To mitigate this, we recommend that you leverage multiple Azure Connectors and/or multiple LCS projects.</span></span> <span data-ttu-id="421bc-218">たとえば、1 つの LCS プロジェクトで製造環境を、別で開発/テスト環境を検討します。</span><span class="sxs-lookup"><span data-stu-id="421bc-218">For example, consider having production environments in one LCS project, and Dev/Test environments in another.</span></span> 

> [!NOTE]
> <span data-ttu-id="421bc-219">インストール VHD など、LCS が配置するすべての VHD が高度に使用されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="421bc-219">Not all VHDs that LCS deploys will be highly utilized, such as the installation VHD.</span></span>

## <a name="plan-your-sql-server-configuration"></a><span data-ttu-id="421bc-220">SQL Server 構成の計画</span><span class="sxs-lookup"><span data-stu-id="421bc-220">Plan your SQL Server configuration</span></span>
<span data-ttu-id="421bc-221">Azure Premium Storage は、Azure 仮想マシン (VM) 上で実行される I/O 集約型ワークロードに対して高パフォーマンス、待機時間が短いディスク サポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="421bc-221">Azure Premium Storage delivers high-performance, low-latency disk support for I/O intensive workloads running on Azure virtual machines (VMs).</span></span> <span data-ttu-id="421bc-222">Premium Storage では、アプリケーションは VM ごとに 32 TB までのストレージを持つことができ、VM ごとに 50,000 IOPS を達成し、読み取り操作での待機時間は非常に短くなります。</span><span class="sxs-lookup"><span data-stu-id="421bc-222">With Premium Storage, your applications can have up to 32 TB of storage per VM, achieve 50,000 IOPS per VM, and have extremely low latencies for read operations.</span></span> <span data-ttu-id="421bc-223">Premium Storage は、生産能力で使用される AX 2012 R3 配置に必要です。</span><span class="sxs-lookup"><span data-stu-id="421bc-223">Premium Storage is required for AX 2012 R3 deployments that will be used in a production capacity.</span></span> <span data-ttu-id="421bc-224">Azure DS シリーズ VM が選択されている場合、高可用性配置では Premium Storage が既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="421bc-224">Premium Storage is enabled by default for High Availability deployments when Azure DS-series VMs are selected.</span></span> <span data-ttu-id="421bc-225">Premium Storage は、現時点では DS シリーズ VM 上でのみ提供されています。</span><span class="sxs-lookup"><span data-stu-id="421bc-225">Premium Storage is only offered on DS-series VMs at this time.</span></span> <span data-ttu-id="421bc-226">他のすべての記憶域ニーズに非 Premium ストレージが使用されているとき、SQL Server AlwaysOn データベース サーバーだけで Premium Storage が有効になります。</span><span class="sxs-lookup"><span data-stu-id="421bc-226">Premium Storage is enabled exclusively for the SQL Server AlwaysOn database servers, while non-Premium storage is used for all other storage needs.</span></span> <span data-ttu-id="421bc-227">SQL Server AlwaysOn 可用性セットが作成されると、Lifecycle Services は、選択された DS シリーズ VM でサポートされているすべてのディスク スロットに対してディスクをアタッチします。</span><span class="sxs-lookup"><span data-stu-id="421bc-227">When a SQL Server AlwaysOn availability set is created, Lifecycle Services will attach a disk for every disk slot supported by the DS-series VM selected.</span></span> <span data-ttu-id="421bc-228">VM ディスク能力の詳細については、[ここ](https://msdn.microsoft.com/library/azure/dn197896.aspx) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="421bc-228">For more information about VM disk capacity, click [here](https://msdn.microsoft.com/library/azure/dn197896.aspx).</span></span> <span data-ttu-id="421bc-229">異なる VM サイズには、スループットと IOPS の最大値が変化します。</span><span class="sxs-lookup"><span data-stu-id="421bc-229">Different VM sizes will come with varying maximums for throughput and IOPS.</span></span> <span data-ttu-id="421bc-230">結果として、 SQL Server の構成を計画しているときは、ビジネスに最も効率的でコスト効果の良いソリューションを展開するために、これらの制限に精通してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-230">As a result, when you are planning your SQL Server configuration, please be familiar with these limitations to ensure that you are deploying the most efficient and cost effective solution for your business.</span></span> <span data-ttu-id="421bc-231">[Premium Storage: Azure 仮想マシン ワークロード向け高性能ストレージ](https://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/)に関するページ (特に、**Premium Storage の使用時の調整**に関するセッション) にあるガイドラインに従ってください。</span><span class="sxs-lookup"><span data-stu-id="421bc-231">Please follow the guidance found in [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/), particularly the section, **Throttling when using Premium Storage**.</span></span> <span data-ttu-id="421bc-232">SQL Server AlwaysOn 可用性セットは、Lifecycle Services を通じて自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-232">The SQL Server AlwaysOn availability set is created automatically through Lifecycle Services.</span></span> <span data-ttu-id="421bc-233">生産システムで使用するための高可用性トポロジを配置する前に、データおよびパフォーマンスのニーズを考慮することが重要です。</span><span class="sxs-lookup"><span data-stu-id="421bc-233">It is important to consider your data and performance needs before deploying a High Availability topology for use with a production system.</span></span> <span data-ttu-id="421bc-234">Azure Premium Storage については、[こちら](http://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="421bc-234">Please refer to Azure Premium Storage information [here](http://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/).</span></span> <span data-ttu-id="421bc-235">Premium Storage で配置を計画すると、高可用性トポロジには、原価とパフォーマンスの目標を達成するためのコンフィギュレーション オプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-235">Once you have planned your deployment with Premium Storage, the High Availability topology provides configuration options to help you achieve your cost and performance objectives.</span></span> <span data-ttu-id="421bc-236">高可用性のトポロジの詳細設定では、次の SQL Server 構成オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-236">Under Advanced Settings for the High Availability topology, the following SQL Server configuration options appear:</span></span>

-   <span data-ttu-id="421bc-237">**SQL Server イメージ コンフィギュレーションのカスタマイズ** - このオプションを使用すると、カスタム SQL Server Enterprise イメージまたは Azure Gallery SQL Server Enterprise イメージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="421bc-237">**Customize the SQL Server image configuration** – This option allows the use of a custom SQL Server Enterprise image or an Azure Gallery SQL Server Enterprise image.</span></span>
    -   <span data-ttu-id="421bc-238">カスタム SQL Server イメージ (既定) - このイメージには、SQL Server Enterprise 2014の試用版が含まれています。</span><span class="sxs-lookup"><span data-stu-id="421bc-238">Custom SQL Server image (default) – This image contains a trial edition of SQL Server Enterprise 2014.</span></span> <span data-ttu-id="421bc-239">評価版ライセンスは 3〜6 か月間有効です。</span><span class="sxs-lookup"><span data-stu-id="421bc-239">The trial license is enabled for 3-6 months.</span></span> <span data-ttu-id="421bc-240">既存の EA/etc. ライセンスを使用する場合は、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="421bc-240">Use this option if you want to use an existing EA/etc. license.</span></span>
    -   <span data-ttu-id="421bc-241">ギャラリー SQL Server イメージ – このイメージには SQL Server Enterprise 2014 が含まれており、消費に基づく Azure 価格決定を使用します。</span><span class="sxs-lookup"><span data-stu-id="421bc-241">Gallery SQL Server image – This image contains SQL Server Enterprise 2014 and uses consumption-based Azure pricing.</span></span> <span data-ttu-id="421bc-242">詳細については、[Azure 仮想マシンの価格決定](https://azure.microsoft.com/pricing/details/virtual-machines/#sql-server)ページと [Azure 仮想マシンの SQL Server](https://msdn.microsoft.com/library/azure/jj823132.aspx) で確認できます。</span><span class="sxs-lookup"><span data-stu-id="421bc-242">More information can be found on the [Azure Virtual Machines Pricing](https://azure.microsoft.com/pricing/details/virtual-machines/#sql-server) page and the [SQL Server in Azure Virtual Machines](https://msdn.microsoft.com/library/azure/jj823132.aspx)</span></span>
-   <span data-ttu-id="421bc-243">**SQL Server のストレージ領域コンフィギュレーションのカスタマイズ** - SQL Server VM に関連付けられるディスクの数とサイズを指定できます。</span><span class="sxs-lookup"><span data-stu-id="421bc-243">**Customize the SQL Server storage space configuration** – You can specify the number and size of the disks that will be attached to the SQL Server VMs.</span></span>

<span data-ttu-id="421bc-244">SQL Server 内でストレージ領域の作成に使用する必要があるディスクの数を指定する場合は、次の点に留意してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-244">Keep the following points in mind when specifying the number of disks that should be used to create the storage space within SQL Server:</span></span>

-   <span data-ttu-id="421bc-245">データベース サーバーのために選択されている VM サイズで、その VM SKU でサポートされるディスクの数が決まります。</span><span class="sxs-lookup"><span data-stu-id="421bc-245">The VM size that is selected for the database server dictates how many disks are supported by that VM SKU.</span></span> <span data-ttu-id="421bc-246">各 VM でサポートされているディスクの数に関する情報は、[ここ](https://msdn.microsoft.com/library/azure/dn197896.aspx)で確認できます。</span><span class="sxs-lookup"><span data-stu-id="421bc-246">Information about the number of disks that are supported by each VM can be found [here](https://msdn.microsoft.com/library/azure/dn197896.aspx).</span></span>
-   <span data-ttu-id="421bc-247">VM で使用可能なディスク スロットの 1 つは、Lifecycle Services 配置サービスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-247">One of the available disk slots on the VM will be used by the Lifecycle Services deployment service.</span></span> <span data-ttu-id="421bc-248">これは、VM の最大ディスク数 (マイナス1) が、使用可能なスロットを満たすことを意味します。</span><span class="sxs-lookup"><span data-stu-id="421bc-248">This means the VM’s maximum number of disks—minus 1—equals the available slots to fill.</span></span>
-   <span data-ttu-id="421bc-249">この設定を空白のままにすると、配置サービスによって VM でサポートされている最大までディスクを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="421bc-249">Leaving this setting blank will allow the deployment service to attach disks up to the maximum supported by the VM.</span></span> <span data-ttu-id="421bc-250">最大のディスクが使用される運用配置の場合にお勧めします。</span><span class="sxs-lookup"><span data-stu-id="421bc-250">It is recommended for production deployments that the maximum disks be used.</span></span>

<span data-ttu-id="421bc-251">VM に関連付けられている各ディスクのサイズ (GB 単位) を指定する場合、次の点に留意してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-251">Keep the following points in mind when specifying the size (in GB) of each disk attached to the VM:</span></span>

-   <span data-ttu-id="421bc-252">100 GB – 1024 GB 値を許可します。</span><span class="sxs-lookup"><span data-stu-id="421bc-252">Allowed values are 100 GB – 1024 GB.</span></span>
-   <span data-ttu-id="421bc-253">既定値は 128 GB です。</span><span class="sxs-lookup"><span data-stu-id="421bc-253">Default is 128 GB.</span></span>
-   <span data-ttu-id="421bc-254">使用されるディスクのサイズは、使用される Premium Storage 階層を決定します。</span><span class="sxs-lookup"><span data-stu-id="421bc-254">The size of the disk used dictates the Premium Storage tier used.</span></span>
-   <span data-ttu-id="421bc-255">Premium Storage 層は、原価、ディスクあたりの IPOPS、および展開されるシステムのスループットを示しています。</span><span class="sxs-lookup"><span data-stu-id="421bc-255">The Premium Storage tier dictates cost, IOPS per disk, and throughput of the system being deployed.</span></span> <span data-ttu-id="421bc-256">詳細については、[ここ](http://azure.microsoft.com/pricing/details/storage/) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="421bc-256">For more information, click [here](http://azure.microsoft.com/pricing/details/storage/).</span></span>
-   <span data-ttu-id="421bc-257">すべてのディスクは 64k クラスター サイズにフォーマットします。</span><span class="sxs-lookup"><span data-stu-id="421bc-257">All disks are formatted to 64k cluster size.</span></span> <span data-ttu-id="421bc-258">これにより、パフォーマンスが最大 20％ 向上します。</span><span class="sxs-lookup"><span data-stu-id="421bc-258">This results in up to a 20% increase in performance.</span></span> 

<span data-ttu-id="421bc-259">TempDB とログは、パフォーマンスの向上のために記憶域上に配置されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-259">TempDB and logs are deployed onto storage spaces as to benefit from the performance gains.</span></span> <span data-ttu-id="421bc-260">そのストレージ領域にコンフィギュレーションされているディスクの数に対して、1 つの仮想ディスクが作成されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-260">One virtual disk is created over the number of disks configured for the storage space.</span></span> <span data-ttu-id="421bc-261">次に、仮想ディスクは次のようにパーティション化されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-261">The virtual disk is then partitioned as follows:</span></span>

-   <span data-ttu-id="421bc-262">SQL データ = プールの合計サイズの 1/2</span><span class="sxs-lookup"><span data-stu-id="421bc-262">SQL data = 1/2 of the total size of pool</span></span>
-   <span data-ttu-id="421bc-263">SQL ログ = 合計サイズの 1/4</span><span class="sxs-lookup"><span data-stu-id="421bc-263">SQL logs = 1/4 of the total size</span></span>
-   <span data-ttu-id="421bc-264">SQL Temp db = 合計サイズの 1/8</span><span class="sxs-lookup"><span data-stu-id="421bc-264">SQL Temp db = 1/8 of the total size</span></span>
-   <span data-ttu-id="421bc-265">SQL バックアップ = 合計サイズの残り 1/8</span><span class="sxs-lookup"><span data-stu-id="421bc-265">SQL backup = remaining 1/8 of the total size</span></span>

<span data-ttu-id="421bc-266">他の考慮事項を念頭に置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-266">Other considerations to keep in mind:</span></span>

-   <span data-ttu-id="421bc-267">配置を計画するときは、対象とする Azure 領域で Premium Storage を使用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="421bc-267">When planning your deployment, ensure that Premium Storage is available in the Azure region you are targeting.</span></span> <span data-ttu-id="421bc-268">詳細については、[ここ](http://azure.microsoft.com/services/preview/) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="421bc-268">For more information, click [here](http://azure.microsoft.com/services/preview/).</span></span>
-   <span data-ttu-id="421bc-269">会社のネットワークと Azure の間で VPN/Express ルート接続 (または計画) がある場合、Premium ストレージ アカウントをサポートしている Azure 地域でこれが行われていることが確認します。</span><span class="sxs-lookup"><span data-stu-id="421bc-269">If you have a VPN/Express Route connection (or plan to) between your corporate network and Azure, please ensure this is done for an Azure region that supports Premium Storage.</span></span>
-   <span data-ttu-id="421bc-270">使用に関する制限について理解するためには [Azure Premium Storage ドキュメント](http://azure.microsoft.com/documentation/services/storage/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-270">Consult the [Azure Premium Storage documentation](http://azure.microsoft.com/documentation/services/storage/) to understand limitations of use.</span></span>
-   <span data-ttu-id="421bc-271">可用性トポロジーで非 Premium ストレージ VM がデプロイされている場合は、上記のすべての SQL Server のコンフィギュレーションを適用できますが、Premium ストレージのメリットは適用されません。</span><span class="sxs-lookup"><span data-stu-id="421bc-271">If non-Premium Storage VMs are deployed with the High Availability topologies, all of the above SQL Server configuration settings are applicable; however, Premium Storage benefits will not apply.</span></span>
-   <span data-ttu-id="421bc-272">配置ために Lifecycle Services プロジェクトを設定するとき、Premium Storage をサポートする地域を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-272">When setting up your Lifecycle Services project for deployment, you must select a region that supports Premium Storage.</span></span>

<span data-ttu-id="421bc-273">展開サービスにより実装される SQL Server ベスト プラクティスには、SQL Server チームにより推奨されるベスト プラクティスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="421bc-273">SQL Server best practices implemented by the deployment service include those recommended by the SQL Server team.</span></span> <span data-ttu-id="421bc-274">詳細については、[ここ](http://blogs.technet.com/b/dataplatforminsider/archive/2014/09/12/new-vm-images-optimized-for-transactional-and-dw-workloads-in-azure-vm-gallery.aspx) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="421bc-274">For more information, click [here](http://blogs.technet.com/b/dataplatforminsider/archive/2014/09/12/new-vm-images-optimized-for-transactional-and-dw-workloads-in-azure-vm-gallery.aspx).</span></span> <span data-ttu-id="421bc-275">さらに、次の項目が実行されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-275">In addition, the following items are done:</span></span>

-   <span data-ttu-id="421bc-276">複数の一時ファイル (CPU コアごとに 1 つ)。</span><span class="sxs-lookup"><span data-stu-id="421bc-276">Multiple temp files (one per CPU core).</span></span>
-   <span data-ttu-id="421bc-277">SQL Server の最大メモリを使用可能なコンピューター RAM の 90% に設定します。</span><span class="sxs-lookup"><span data-stu-id="421bc-277">Set max memory for SQL Server to 90% of available machine RAM.</span></span>
-   <span data-ttu-id="421bc-278">並列処理の最大限度を設定します。</span><span class="sxs-lookup"><span data-stu-id="421bc-278">Set max degree of parallelism.</span></span>
-   <span data-ttu-id="421bc-279">トレース フラグの有効  -T1204、 -T1222。</span><span class="sxs-lookup"><span data-stu-id="421bc-279">Enabled trace flags  -T1204, -T1222.</span></span>

## <a name="estimate-costs-and-understand-the-azure-billing-process"></a><span data-ttu-id="421bc-280">減価を見積もり、Azure 請求プロセスに同意</span><span class="sxs-lookup"><span data-stu-id="421bc-280">Estimate costs and understand the Azure billing process</span></span>
<span data-ttu-id="421bc-281">Azure での AX 2012 R3 の展開コストを見積もるには、[Azure 価格計算ツール](http://azure.microsoft.com/pricing/calculator/)を使用します。</span><span class="sxs-lookup"><span data-stu-id="421bc-281">To help estimate the cost of your AX 2012 R3 deployment on Azure, use the [Azure pricing calculator](http://azure.microsoft.com/pricing/calculator/).</span></span> <span data-ttu-id="421bc-282">Azure に AX 2012 R3 を配置する前に、Azure 請求プロセスについて理解することも重要です。</span><span class="sxs-lookup"><span data-stu-id="421bc-282">It’s also important to understand the Azure billing process before you deploy AX 2012 R3 on Azure.</span></span> <span data-ttu-id="421bc-283">サンプル請求書、および現在の請求期間に対する毎日の使用データをダウンロードする方法に関する情報にリンクする Azure 請求プロセスの概要については、[請求書を理解する](http://azure.microsoft.com/support/understand-your-bill/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-283">For an overview of the Azure billing process, links to sample invoices, and information about how to download daily usage data for the current billing period, see [Understand your bill](http://azure.microsoft.com/support/understand-your-bill/).</span></span> <span data-ttu-id="421bc-284">**注記:** 使用されていないときに Azure 上に配置されている AX 2012 R3 環境をシャット ダウンすることができることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-284">\*\*Note: \*\*Keep in mind, you can shut down an AX 2012 R3 environment that has been deployed on Azure when it’s not in use.</span></span> <span data-ttu-id="421bc-285">たとえば、コスト削減のため週末に環境をシャット ダウンする場合があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-285">For example, you may want to shut down an environment on the weekends to reduce costs.</span></span> <span data-ttu-id="421bc-286">環境をシャット ダウンすると、その環境はまだ存在します。ただし、その環境内の仮想マシンはシャット ダウンされます。</span><span class="sxs-lookup"><span data-stu-id="421bc-286">When you shut down an environment, the environment still exists; however, the virtual machines in the environment are shut down.</span></span> <span data-ttu-id="421bc-287">仮想マシンが実行されていないときは、それに対して課金されません。</span><span class="sxs-lookup"><span data-stu-id="421bc-287">You won’t be charged for the virtual machines when they’re not running.</span></span> <span data-ttu-id="421bc-288">詳細については、「環境をシャット ダウンする方法とは」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-288">For more information, see “How do I shut down an environment?”</span></span> <span data-ttu-id="421bc-289">[Azure での Microsoft Dynamics AX 2012 R3 配置の管理](manage-2012-r3-deployment-azure.md)という記事の中です。</span><span class="sxs-lookup"><span data-stu-id="421bc-289">in the [Manage your Microsoft Dynamics AX 2012 R3 deployment on Azure](manage-2012-r3-deployment-azure.md) article.</span></span>

## <a name="consider-legal-and-regulatory-requirements"></a><span data-ttu-id="421bc-290">法的および規制要件を考慮する</span><span class="sxs-lookup"><span data-stu-id="421bc-290">Consider legal and regulatory requirements</span></span>
<span data-ttu-id="421bc-291">Microsoft は、複数の地域や税務署にわたる一般的な運用方法と機能で Azure サービスを実行します。</span><span class="sxs-lookup"><span data-stu-id="421bc-291">Microsoft runs Azure services with common operational practices and features across multiple geographies and jurisdictions.</span></span> <span data-ttu-id="421bc-292">ただし、Microsoft サービスがユーザーの規制の必要を満たしているかどうかを判断するのは、最終的にはユーザー次第となります。</span><span class="sxs-lookup"><span data-stu-id="421bc-292">However, it is ultimately up to you to determine if Microsoft services satisfy your regulatory needs.</span></span> <span data-ttu-id="421bc-293">最新の情報を提供するために、[Azure セキュリティ センター](http://azure.microsoft.com/support/trust-center/) はセキュリティ、プライバシー、コンプライアンスに関する以下の情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="421bc-293">To help provide you with up-to-date information, the [Azure trust center](http://azure.microsoft.com/support/trust-center/) provides the following information about security, privacy, and compliance.</span></span>

-   <span data-ttu-id="421bc-294">**セキュリティ**、[Azure セキュリティ ページ](http://www.windowsazure.com/support/trust-center/security/) は地理的に分散されているデータ センター内に安全な環境を提供するために Microsoft が取っている条項の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="421bc-294">**Security** The [Azure security page](http://www.windowsazure.com/support/trust-center/security/) provides an overview of the provisions Microsoft is taking to provide a secure environment within geographically dispersed datacenters.</span></span> <span data-ttu-id="421bc-295">セキュリティ関連リソースの広範なリストの中で、[情報の要求についての標準応答: セキュリティおよびプライバシー](https://www.microsoft.com/download/details.aspx?id=26647) ホワイト ペーパーがどのように Azure の提案されたプリンシパルを満たし、国際標準化機構 (ISO) 27001:2005 および ISO 27002 にマップされているかを概説します。</span><span class="sxs-lookup"><span data-stu-id="421bc-295">Among the extensive list of security-related resources, the [Standard Response to Request for Information: Security and Privacy](https://www.microsoft.com/download/details.aspx?id=26647) white paper outlines how Azure meets the suggested principals and mapped them to the International Standards Organization (ISO) 27001:2005 and ISO 27002.</span></span>
-   <span data-ttu-id="421bc-296">**プライバシー** [Azure プライバシー ページ](http://www.windowsazure.com/support/trust-center/privacy/) Azure 環境のプライバシーに関する取り組みを説明する複数のリソースへのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="421bc-296">**Privacy** The [Azure privacy page](http://www.windowsazure.com/support/trust-center/privacy/) includes links to multiple resources that describe privacy practices of the Azure environment.</span></span> <span data-ttu-id="421bc-297">[Azure のプライバシーに関する声明](http://www.windowsazure.com/support/legal/privacy-statement/)へのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="421bc-297">It includes a link to the [Azure privacy statement](http://www.windowsazure.com/support/legal/privacy-statement/).</span></span>
-   <span data-ttu-id="421bc-298">**コンプライアンス** [Azure コンプライアンス ページ](http://www.windowsazure.com/support/trust-center/compliance/)は、独自の業界に適用される特定の法律および規制を順守し、シナリオを使用するためのリソースを提供します。</span><span class="sxs-lookup"><span data-stu-id="421bc-298">**Compliance** The [Azure compliance page](http://www.windowsazure.com/support/trust-center/compliance/) provides resources to help you comply with the specific laws and regulations applicable to your unique industry and use scenario.</span></span>

## <a name="consider-licensing-requirements"></a><span data-ttu-id="421bc-299">ライセンス供与の要件の検討</span><span class="sxs-lookup"><span data-stu-id="421bc-299">Consider licensing requirements</span></span>
<span data-ttu-id="421bc-300">AX 2012 R3 仮想マシン環境のさまざまなコンポーネントのライセンス供与は、重要な考慮事項です。</span><span class="sxs-lookup"><span data-stu-id="421bc-300">Licensing the various components of the AX 2012 R3 virtual machine environment is an important consideration.</span></span> <span data-ttu-id="421bc-301">Azure での展開は、 Azure に固有な特別なライセンス条項であるか、およびそれらの条項がソリューションの全体的な適合性を備えているかを評価します。</span><span class="sxs-lookup"><span data-stu-id="421bc-301">For deployments on Azure, you will want to evaluate the special licensing terms specific to Azure and the impact that these terms have on the overall suitability of the solution.</span></span> <span data-ttu-id="421bc-302">ライセンス供与の要件は、Azure に配置する AX 2012 R3 仮想マシン環境の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="421bc-302">Licensing requirements vary based on the type of AX 2012 R3 virtual machine environment that you deploy on Azure.</span></span> <span data-ttu-id="421bc-303">次のテーブルに詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="421bc-303">The following table provides more information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="421bc-304"><strong>環境のタイプ</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-304"><strong>Type of environment</strong></span></span></td>
<td><span data-ttu-id="421bc-305"><strong>ライセンス要件</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-305"><strong>Licensing requirements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-306">デモ</span><span class="sxs-lookup"><span data-stu-id="421bc-306">Demo</span></span></td>
<td><span data-ttu-id="421bc-307">仮想マシン環境に含まれるソフトウェアは、ソフトウェア ライセンス条項の項目に従って、時間制限付きで使用許諾されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-307">The software that is included in the virtual machine environment is time-bound and licensed according to the terms in the Software License Terms.</span></span>
<ul>
<li><span data-ttu-id="421bc-308"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">AX 2013 R3 デモ環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="421bc-308"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">Software License Terms for the AX 2013 R3 demo environment</a></span></span></li>
<li><span data-ttu-id="421bc-309"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">AX 2013 R3 CU8 デモ環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="421bc-309"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">Software License Terms for the AX 2013 R3 CU8 demo environment</a></span></span></li>
<li><span data-ttu-id="421bc-310"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">5. Retail Essentials デモ環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="421bc-310"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">Software License Terms for the Retail essentials demo environment</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="421bc-311">開発/テストおよび高可用性</span><span class="sxs-lookup"><span data-stu-id="421bc-311">Dev/test and high availability</span></span></td>
<td><span data-ttu-id="421bc-312">仮想マシン環境を含めすべてのソフトウェアには適切なライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="421bc-312">All software included in the virtual machine environment must be properly licensed.</span></span> <span data-ttu-id="421bc-313">パートナーとマイクロソフトの担当者共に、ライセンスのニーズを十分に調査してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-313">Please investigate your licensing needs thoroughly with your partner and your Microsoft representative.</span></span> <span data-ttu-id="421bc-314">仮想マシン環境に含まれる個々のソフトウェアの条件を調査する必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-314">You will need to investigate the terms for each piece of software that is included in the virtual machine environment.</span></span> <span data-ttu-id="421bc-315">仮想マシン環境に含まれるソフトウェアの完全な一覧については、ソフトウェア ライセンス条項を参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-315">For the complete list of software that is included in the virtual machine environment, review the Software License Terms.</span></span>
<ul>
<li><span data-ttu-id="421bc-316"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">開発環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="421bc-316"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the development environment</a></span></span></li>
<li><span data-ttu-id="421bc-317"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">共有の SQL Server 環境による開発用のソフトウェア ライセンス条件</a></span><span class="sxs-lookup"><span data-stu-id="421bc-317"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the development with shared SQL Server environment</a></span></span></li>
<li><span data-ttu-id="421bc-318"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="421bc-318"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the test environment</a></span></span></li>
<li><span data-ttu-id="421bc-319"><a href="http://go.microsoft.com/fwlink/?LinkID=507496&amp;amp;clcid=0x409">5. Retail Essentials 開発/テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="421bc-319"><a href="http://go.microsoft.com/fwlink/?LinkID=507496&amp;amp;clcid=0x409">Software License Terms for the Retail essentials dev/test environment</a></span></span></li>
<li><span data-ttu-id="421bc-320"><a href="http://go.microsoft.com/fwlink/?LinkID=507494">5. Retail E-commerce 開発/テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="421bc-320"><a href="http://go.microsoft.com/fwlink/?LinkID=507494">Software License Terms for the Retail e-commerce dev/test environment</a></span></span></li>
<li><span data-ttu-id="421bc-321"><a href="http://go.microsoft.com/fwlink/?LinkID=507496">5. Retail Mobility 開発/テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="421bc-321"><a href="http://go.microsoft.com/fwlink/?LinkID=507496">Software License Terms for the Retail mobility dev/test environment</a></span></span></li>
<li><span data-ttu-id="421bc-322"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">高可用性環境のソフトウェア ライセンス条項</a>ライセンス条項と要件を確認する際には、Azure に配置するために特に適用される条項、および使用目的に適用される条項に特に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-322"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the high availability environment</a> When reviewing the licensing terms and requirements, you need to pay special attention to any terms that apply specifically to deploying on Azure, as well as terms that apply to your intended use.</span></span> <span data-ttu-id="421bc-323">たとえば、Microsoft Office は Azure に固有の条件を持ちますが、これらの条件は、開発またはテスト目的で Office を配置するか、または生産目的で Office を配置するかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="421bc-323">For example, Microsoft Office has terms that are specific to Azure; but those terms vary depending on whether you deploy Office for development or test purposes, or whether you deploy Office for production purposes.</span></span></li>
</ul>
<span data-ttu-id="421bc-324">開始するうえで役立ついくつかのリソースを以下のリンクに示します。</span><span class="sxs-lookup"><span data-stu-id="421bc-324">Some resources to help you get started are linked to below.</span></span> <span data-ttu-id="421bc-325">以下にリンクされているリソースのほとんどに、複数の製品およびシナリオの詳細な情報へのリンクが含まれています。ただし、追加の情報を確認しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-325">Most of the resources that are linked to below contain links to in-depth information for several products and scenarios; however, you may need to review additional information, as well.</span></span> <span data-ttu-id="421bc-326">この情報は、ライセンスを取得した製品の承認済みの使用に関するガイドに役立つ情報です。 同意ではありません。</span><span class="sxs-lookup"><span data-stu-id="421bc-326">This information is provided to help guide your authorized use of products you license; it is not your agreement.</span></span> <span data-ttu-id="421bc-327">ボリューム ライセンス契約にもとづいてライセンスされている製品の使用は、その契約の条件によって支配されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-327">Your use of products licensed under your volume license agreement is governed by the terms and conditions of that agreement.</span></span> <span data-ttu-id="421bc-328">ここにリンクされている情報と契約に矛盾がある場合、契約の使用条件が有効となります。</span><span class="sxs-lookup"><span data-stu-id="421bc-328">In the case of any conflict between information linked here and your agreement, the terms and conditions of your agreement control.</span></span>
<ul>
<li><span data-ttu-id="421bc-329"><strong>仮想マシン ライセンスによく寄せられる質問</strong> Azure 仮想マシンのライセンスに関するよくある質問は、<a href="http://www.windowsazure.com/pricing/licensing-faq/">このページ</a>で回答されています。</span><span class="sxs-lookup"><span data-stu-id="421bc-329"><strong>Virtual machines licensing FAQ</strong> Common questions regarding licensing on Azure virtual machines are answered on <a href="http://www.windowsazure.com/pricing/licensing-faq/">this page</a>.</span></span></li>
<li><span data-ttu-id="421bc-330"><strong>Microsoft 製品の使用権限と製品リスト</strong>ビジネス上の意思決定を効果的にし、IT 購入価値を最大化するために、<a href="http://go.microsoft.com/fwlink/?LinkId=397363">このページ</a>で、Microsoft ボリューム ライセンス製品のライセンスモデル、プログラム、シナリオ、および使用条件について詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="421bc-330"><strong>Microsoft Product Use Rights and Product List</strong> Learn more about Microsoft Volume Licensing product licensing models, programs, scenarios, and terms and conditions to help you make effective business decisions and maximize the value of your IT purchases on <a href="http://go.microsoft.com/fwlink/?LinkId=397363">this page</a>.</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="421bc-331"><strong>Azure プログラムのソフトウェア保証によるライセンス モビリティ</strong>ソフトウェア保証によるライセンス モビリティにより、Microsoft ボリューム ライセンスの顧客は、Azure でアクティブなソフトウェア保証を使用して、適格なサーバー アプリケーションを配置する柔軟性を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="421bc-331"><strong>License Mobility through Software Assurance on Azure program</strong> License Mobility through Software Assurance gives Microsoft volume licensing customers the flexibility to deploy eligible server applications with active Software Assurance on Azure.</span></span> <span data-ttu-id="421bc-332">このソフトウェア保証給付金では、新しいライセンスを購入する必要がなく、関連するモビリティ費用がかかりません。</span><span class="sxs-lookup"><span data-stu-id="421bc-332">With this Software Assurance benefit, there is no need to purchase new licenses and no associated mobility fees.</span></span> <span data-ttu-id="421bc-333">これにより、既存のライセンスを Azure クラウド プラットフォームに簡単に展開できます。</span><span class="sxs-lookup"><span data-stu-id="421bc-333">This enables you to easily deploy existing licenses on the Azure cloud platform.</span></span> <span data-ttu-id="421bc-334">詳細については、<a href="http://www.windowsazure.com/pricing/license-mobility/">このページ</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-334">For more information, see <a href="http://www.windowsazure.com/pricing/license-mobility/">this page</a>.</span></span> <span data-ttu-id="421bc-335">開発、テスト、および SharePoint の高可用性トポロジ トライアル版用に、Visual Studio、SQL Server および Office が提供されています。</span><span class="sxs-lookup"><span data-stu-id="421bc-335">For Development, Test, and High Availability topologies trial versions of SharePoint, Visual Studio, SQL Server, and Office are provided.</span></span> <span data-ttu-id="421bc-336">評価の範囲は 30〜180 日間です。</span><span class="sxs-lookup"><span data-stu-id="421bc-336">The trials range from 30-180 days.</span></span> <span data-ttu-id="421bc-337">それに応じてライセンスを適用してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-337">Please apply licenses accordingly.</span></span></li>
<li><span data-ttu-id="421bc-338"><strong>Microsoft Dynamics AX ボリューム ライセンス バイヤー ガイド</strong> Microsoft Dynamics AX を使用したキー ライセンス オプションの概要については、<a href="http://go.microsoft.com/fwlink/?LinkId=397363">このページ</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-338"><strong>Microsoft Dynamics AX volume licensing buyer’s guide</strong> For an overview of key licensing options with Microsoft Dynamics AX, see <a href="http://go.microsoft.com/fwlink/?LinkId=397363">this page</a>.</span></span></li>
<li><span data-ttu-id="421bc-339"><strong>Office 365 ProPlus の共有コンピュータの有効化</strong> 共有コンピューターの有効化により、複数のユーザーがアクセスする組織内のコンピュータに Office 365 ProPlus を配置できます。</span><span class="sxs-lookup"><span data-stu-id="421bc-339"><strong>Shared computer activation for Office 365 ProPlus</strong> Shared computer activation lets you to deploy Office 365 ProPlus to a computer in your organization that is accessed by multiple users.</span></span> <span data-ttu-id="421bc-340">詳細については、<a href="https://technet.microsoft.com/library/dn782860(v=office.15).aspx">このページ</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-340">For more information, see <a href="https://technet.microsoft.com/library/dn782860(v=office.15).aspx">this page</a>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="select-the-ax-2012-r3-environment-that-you-want-to-deploy"></a><span data-ttu-id="421bc-341">配置する AX 2012 R3 環境を選択</span><span class="sxs-lookup"><span data-stu-id="421bc-341">Select the AX 2012 R3 environment that you want to deploy</span></span>
<span data-ttu-id="421bc-342">Azure 上に AX 2012 R3 環境を配置するには、Lifecycle Services のクラウド ホスト環境ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="421bc-342">You’ll use the Cloud-hosted environments tool in Lifecycle Services to deploy AX 2012 R3 environments on Azure.</span></span> <span data-ttu-id="421bc-343">クラウド ホスト環境ツールを使用して配置するとき、デモまたは開発/テスト環境などの、Azure 上に配置する環境のタイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-343">When you use the Cloud-hosted environments tool to deploy, you’ll need to select the type of environment that you want to deploy on Azure, such as a demo or development/test environment.</span></span> <span data-ttu-id="421bc-344">この選択に基づいて、クラウド ホスト環境ツールは Azure での仮想マシンの適切な数を提供します。</span><span class="sxs-lookup"><span data-stu-id="421bc-344">Based on your selection, the Cloud-hosted environments tool provisions the appropriate number of virtual machines on Azure.</span></span> <span data-ttu-id="421bc-345">これらの仮想マシンには、AX 2012 R3 コンポーネント (およびそれらの必要物すべて) がインストール済みです。</span><span class="sxs-lookup"><span data-stu-id="421bc-345">These virtual machines have AX 2012 R3 components—and all of their prerequisites—already installed on them.</span></span> <span data-ttu-id="421bc-346">次のセクションでは、Azure に配置できる AX 2012 R3 環境について説明します。</span><span class="sxs-lookup"><span data-stu-id="421bc-346">The following sections describe the AX 2012 R3 environments that you can deploy on Azure.</span></span>

-   <span data-ttu-id="421bc-347">AX 2012 R3 および AX 2012 R3 CU8 デモ環境</span><span class="sxs-lookup"><span data-stu-id="421bc-347">AX 2012 R3 and AX 2012 R3 CU8 demo environments</span></span>
-   <span data-ttu-id="421bc-348">Retail Essentials デモ環境</span><span class="sxs-lookup"><span data-stu-id="421bc-348">Retail essentials demo environment</span></span>
-   <span data-ttu-id="421bc-349">開発環境</span><span class="sxs-lookup"><span data-stu-id="421bc-349">Development environments</span></span>
-   <span data-ttu-id="421bc-350">テスト環境</span><span class="sxs-lookup"><span data-stu-id="421bc-350">Test environment</span></span>
-   <span data-ttu-id="421bc-351">Retail Essentials 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="421bc-351">Retail essentials dev/test environment</span></span>
-   <span data-ttu-id="421bc-352">Retail E-commerce 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="421bc-352">Retail e-commerce dev/test environment</span></span>
-   <span data-ttu-id="421bc-353">Retail mobility 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="421bc-353">Retail mobility dev/test environment</span></span>
-   <span data-ttu-id="421bc-354">高可用性環境</span><span class="sxs-lookup"><span data-stu-id="421bc-354">High availability environment</span></span>

> [!NOTE]
> <span data-ttu-id="421bc-355">このような環境では、SQL Server は SQL\_Latin1\_General\_CP1\_CI\_AS の照合順序を使用するよう構成されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-355">In these environments, SQL Server is configured to use the SQL\_Latin1\_General\_CP1\_CI\_AS collation.</span></span>

## <a name="ax-2012-r3-and-ax-2012-r3-cu8-demo-environments"></a><span data-ttu-id="421bc-356">AX 2012 R3 および AX 2012 R3 CU8 デモ環境</span><span class="sxs-lookup"><span data-stu-id="421bc-356">AX 2012 R3 and AX 2012 R3 CU8 demo environments</span></span>
<span data-ttu-id="421bc-357">2 つの AX 2012 R3 デモ環境があります。1 方の環境には累積更新プログラム 8 があり、もう 1 つ方にはありません。</span><span class="sxs-lookup"><span data-stu-id="421bc-357">There are two AX 2012 R3 demo environments: one environment includes Cumulative Update 8, and the other does not.</span></span> <span data-ttu-id="421bc-358">次のテーブルは、それぞれの環境に関する詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="421bc-358">The following table lists details about each environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="421bc-359">各環境に含まれる仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="421bc-359">The virtual machine included in each environment is a single-instance virtual machine.</span></span> <span data-ttu-id="421bc-360">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="421bc-360">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/support/legal/sla/).</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="421bc-361"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-361"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="421bc-362"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-362"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="421bc-363"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-363"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="421bc-364"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-364"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-365">1</span><span class="sxs-lookup"><span data-stu-id="421bc-365">1</span></span></td>
<td><span data-ttu-id="421bc-366">デモ マシン</span><span class="sxs-lookup"><span data-stu-id="421bc-366">Demo machine</span></span></td>
<td><span data-ttu-id="421bc-367"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>DEMO-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-367"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> DEMO-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-368">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="421bc-368">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="421bc-369">Active Directory</span><span class="sxs-lookup"><span data-stu-id="421bc-369">Active Directory</span></span></li>
<li><span data-ttu-id="421bc-370">ドメイン名サービス (DNS)</span><span class="sxs-lookup"><span data-stu-id="421bc-370">Domain Name Services (DNS)</span></span></li>
<li><span data-ttu-id="421bc-371">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="421bc-371">Internet Information Services (IIS)</span></span></li>
<li><span data-ttu-id="421bc-372">リモート デスクトップ サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-372">Remote Desktop Services</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-373">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="421bc-373">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="421bc-374">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-374">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-375">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-375">Database Engine Services</span></span></li>
<li><span data-ttu-id="421bc-376">レポート サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-376">Reporting Services</span></span></li>
<li><span data-ttu-id="421bc-377">分析サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-377">Analysis Services</span></span></li>
<li><span data-ttu-id="421bc-378">Management Studio</span><span class="sxs-lookup"><span data-stu-id="421bc-378">Management Studio</span></span></li>
<li><span data-ttu-id="421bc-379">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="421bc-379">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-380">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="421bc-380">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="421bc-381">Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="421bc-381">Microsoft Office 2013</span></span></li>
<li><span data-ttu-id="421bc-382">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-382">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-383">データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-383">Databases</span></span></li>
<li><span data-ttu-id="421bc-384">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-384">Server components:</span></span>
<ul>
<li><span data-ttu-id="421bc-385">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="421bc-385">Application Object Server (AOS)</span></span></li>
<li><span data-ttu-id="421bc-386">Web サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-386">Web server components:</span></span>
<ul>
<li><span data-ttu-id="421bc-387">エンタープライズ ポータル (EP)</span><span class="sxs-lookup"><span data-stu-id="421bc-387">Enterprise Portal (EP)</span></span></li>
<li><span data-ttu-id="421bc-388">エンタープライズ検索</span><span class="sxs-lookup"><span data-stu-id="421bc-388">Enterprise Search</span></span></li>
<li><span data-ttu-id="421bc-389">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-389">Help Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="421bc-390">ビジネス インテリジェンス コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-390">Business intelligence components:</span></span>
<ul>
<li><span data-ttu-id="421bc-391">Reporting Services 拡張機能</span><span class="sxs-lookup"><span data-stu-id="421bc-391">Reporting Services extensions</span></span></li>
<li><span data-ttu-id="421bc-392">Analysis Services の構成</span><span class="sxs-lookup"><span data-stu-id="421bc-392">Analysis Services configuration</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-393">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-393">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="421bc-394">Management Reporter サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="421bc-394">Management Reporter server components</span></span></li>
<li><span data-ttu-id="421bc-395">Management Reporter レポート デザイナー</span><span class="sxs-lookup"><span data-stu-id="421bc-395">Management Reporter Report Designer</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-396">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-396">Client components:</span></span>
<ul>
<li><span data-ttu-id="421bc-397">クライアント</span><span class="sxs-lookup"><span data-stu-id="421bc-397">Client</span></span></li>
<li><span data-ttu-id="421bc-398">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="421bc-398">Office add-ins</span></span></li>
<li><span data-ttu-id="421bc-399">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="421bc-399">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-400">開発者ツール:</span><span class="sxs-lookup"><span data-stu-id="421bc-400">Developer tools:</span></span>
<ul>
<li><span data-ttu-id="421bc-401">デバッガー</span><span class="sxs-lookup"><span data-stu-id="421bc-401">Debugger</span></span></li>
<li><span data-ttu-id="421bc-402">Visual Studio ツール</span><span class="sxs-lookup"><span data-stu-id="421bc-402">Visual Studio Tools</span></span></li>
<li><span data-ttu-id="421bc-403">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="421bc-403">Trace Parser</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-404">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-404">Integration components:</span></span>
<ul>
<li><span data-ttu-id="421bc-405">IIS 上の Web サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-405">Web services on IIS</span></span></li>
<li><span data-ttu-id="421bc-406">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="421bc-406">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-407">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="421bc-407">Management utilities</span></span></li>
<li><span data-ttu-id="421bc-408">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-408">Retail components:</span></span>
<ul>
<li><span data-ttu-id="421bc-409">Retail POS</span><span class="sxs-lookup"><span data-stu-id="421bc-409">Retail POS</span></span></li>
<li><span data-ttu-id="421bc-410">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="421bc-410">Retail Headquarters</span></span></li>
<li><span data-ttu-id="421bc-411">Commerce Data Exchange コンポーネント</span><span class="sxs-lookup"><span data-stu-id="421bc-411">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="421bc-412">Synch Service</span><span class="sxs-lookup"><span data-stu-id="421bc-412">Synch Service</span></span></li>
<li><span data-ttu-id="421bc-413">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="421bc-413">Real-time Service</span></span></li>
<li><span data-ttu-id="421bc-414">Async Server</span><span class="sxs-lookup"><span data-stu-id="421bc-414">Async Server</span></span></li>
<li><span data-ttu-id="421bc-415">Async Client</span><span class="sxs-lookup"><span data-stu-id="421bc-415">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-416">Retail チャンネル コンフィギュレーション ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="421bc-416">Retail Channel Configuration Utility</span></span></li>
<li><span data-ttu-id="421bc-417">Retail SDK</span><span class="sxs-lookup"><span data-stu-id="421bc-417">Retail SDK</span></span></li>
<li><span data-ttu-id="421bc-418">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="421bc-418">Retail online channel</span></span></li>
<li><span data-ttu-id="421bc-419">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-419">Retail Server</span></span></li>
<li><span data-ttu-id="421bc-420">Retail 一括配置ツールキット</span><span class="sxs-lookup"><span data-stu-id="421bc-420">Retail Mass Deployment Toolkit</span></span></li>
<li><span data-ttu-id="421bc-421">小売チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-421">Retail channel database</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-422">RapidStart Connector</span><span class="sxs-lookup"><span data-stu-id="421bc-422">RapidStart Connector</span></span></li>
<li><span data-ttu-id="421bc-423">データのインポート/エクスポート フレームワーク コンポーネント。</span><span class="sxs-lookup"><span data-stu-id="421bc-423">Data Import/Export Framework components:</span></span>
<ul>
<li><span data-ttu-id="421bc-424">データのインポート/エクスポート フレームワーク (DIXF) サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-424">Data Import/Export Framework (DIXF) service</span></span></li>
<li><span data-ttu-id="421bc-425">AOS コンポーネント</span><span class="sxs-lookup"><span data-stu-id="421bc-425">AOS component</span></span></li>
<li><span data-ttu-id="421bc-426">クライアント コンポーネント</span><span class="sxs-lookup"><span data-stu-id="421bc-426">Client component</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-427">倉庫モバイル デバイス ポータル</span><span class="sxs-lookup"><span data-stu-id="421bc-427">Warehouse Mobile Devices Portal</span></span></li>
<li><span data-ttu-id="421bc-428">Microsoft Dynamics Connector</span><span class="sxs-lookup"><span data-stu-id="421bc-428">Connector for Microsoft Dynamics</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-essentials-demo-environment"></a><span data-ttu-id="421bc-429">Retail Essentials デモ環境</span><span class="sxs-lookup"><span data-stu-id="421bc-429">Retail Essentials demo environment</span></span>
<span data-ttu-id="421bc-430">この環境を配置して、Retail Essentials をデモしてください。</span><span class="sxs-lookup"><span data-stu-id="421bc-430">Deploy this environment to demo Retail essentials.</span></span> <span data-ttu-id="421bc-431">Retail Essentials は、Microsoft Dynamics AX の小売中心のコンフィギュレーション オプションです。</span><span class="sxs-lookup"><span data-stu-id="421bc-431">Retail essentials is a retail-centric configuration option for Microsoft Dynamics AX.</span></span> <span data-ttu-id="421bc-432">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="421bc-432">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="421bc-433">この仮想マシンには、Windows Server と、Retail Essentials をデモンストレーションするために必要なソフトウェアとサンプル データが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="421bc-433">This virtual machine has Windows Server—and the software and sample data that you’ll need to demo Retail essentials—already installed on it.</span></span> <span data-ttu-id="421bc-434">次のテーブルは、既定の Retail Essentials デモ環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="421bc-434">The following table lists details about the default Retail essentials demo environment.</span></span> <span data-ttu-id="421bc-435">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="421bc-435">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="421bc-436">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="421bc-436">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="421bc-437">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="421bc-437">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/support/legal/sla/).</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="421bc-438"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-438"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="421bc-439"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-439"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="421bc-440"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-440"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="421bc-441"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-441"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-442">1</span><span class="sxs-lookup"><span data-stu-id="421bc-442">1</span></span></td>
<td><span data-ttu-id="421bc-443">Retail Essentials デモ コンピューター</span><span class="sxs-lookup"><span data-stu-id="421bc-443">Retail essentials demo machine</span></span></td>
<td><span data-ttu-id="421bc-444"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>DEMO-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-444"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> DEMO-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-445">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="421bc-445">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="421bc-446">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-446">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-447">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-447">Database Engine Services</span></span></li>
<li><span data-ttu-id="421bc-448">Management Studio</span><span class="sxs-lookup"><span data-stu-id="421bc-448">Management Studio</span></span></li>
<li><span data-ttu-id="421bc-449">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="421bc-449">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-450">AX 2012 R3 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-450">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-451">データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-451">Databases</span></span></li>
<li><span data-ttu-id="421bc-452">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-452">Server components:</span></span>
<ul>
<li><span data-ttu-id="421bc-453">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="421bc-453">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-454">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-454">Client components:</span></span>
<ul>
<li><span data-ttu-id="421bc-455">クライアント</span><span class="sxs-lookup"><span data-stu-id="421bc-455">Client</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-456">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-456">Integration components:</span></span>
<ul>
<li><span data-ttu-id="421bc-457">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="421bc-457">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-458">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-458">Retail components:</span></span>
<ul>
<li><span data-ttu-id="421bc-459">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="421bc-459">Retail Headquarters</span></span></li>
<li><span data-ttu-id="421bc-460">Commerce Data Exchange コンポーネント</span><span class="sxs-lookup"><span data-stu-id="421bc-460">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="421bc-461">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="421bc-461">Real-time Service</span></span></li>
<li><span data-ttu-id="421bc-462">Async Server</span><span class="sxs-lookup"><span data-stu-id="421bc-462">Async Server</span></span></li>
<li><span data-ttu-id="421bc-463">Async Client</span><span class="sxs-lookup"><span data-stu-id="421bc-463">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-464">小売チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-464">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="development-environments"></a><span data-ttu-id="421bc-465">開発環境</span><span class="sxs-lookup"><span data-stu-id="421bc-465">Development environments</span></span>
<span data-ttu-id="421bc-466">多くの開発者の開発努力を迅速に開始する必要がある場合は、これらの開発環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="421bc-466">Deploy these development environments when you need to quickly jumpstart a development effort for one to many developers.</span></span> <span data-ttu-id="421bc-467">各開発者の開発用仮想マシン (VM) を数日ではなく数時間で展開します。</span><span class="sxs-lookup"><span data-stu-id="421bc-467">Deploy a development virtual machine (VM) for each of your developers in a matter of hours instead of days.</span></span> <span data-ttu-id="421bc-468">開発環境には、テスト環境と同じドメインおよび仮想ネットワーク カスタマイズすべてが用意されています。</span><span class="sxs-lookup"><span data-stu-id="421bc-468">With a development environment, you have all the same domain and virtual network customizations that you have with the Test environment.</span></span> <span data-ttu-id="421bc-469">開発者シナリオには 2 つのトポロジ オプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="421bc-469">Two topology options are provided for developer scenarios:</span></span>

-   <span data-ttu-id="421bc-470">開発。Active Directory と共に展開されたオールインワンの VM を含みます。</span><span class="sxs-lookup"><span data-stu-id="421bc-470">Development: Includes all-in-one VMs deployed with Active Directory.</span></span>
-   <span data-ttu-id="421bc-471">共有 SQL Server による開発。Active Directory と共に展開されたオールインワンの VM を含みます。</span><span class="sxs-lookup"><span data-stu-id="421bc-471">Development with shared SQL Server: Includes all-in-one VMs deployed with Active Directory.</span></span> <span data-ttu-id="421bc-472">各開発 VM インスタンスのデータベースは、共有 SQL Server インスタンスに配置されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-472">The database for each development VM instance will be deployed to a shared SQL Server instance.</span></span>

<span data-ttu-id="421bc-473">それらの BI 開発の実行については、目的に対する 1 つのインスタンスを配置することができます。</span><span class="sxs-lookup"><span data-stu-id="421bc-473">For those doing BI development you can deploy one instance for the purpose.</span></span> <span data-ttu-id="421bc-474">その他のすべてのインスタンスは BI で配置されません。</span><span class="sxs-lookup"><span data-stu-id="421bc-474">All other instances will not deploy with BI.</span></span> <span data-ttu-id="421bc-475">提供されている開発用 VM には、すべての AX 2012 R3 コンポーネントが Visual Studio 2013 および AX 2012 R3 開発ツールとともにインストールされています。</span><span class="sxs-lookup"><span data-stu-id="421bc-475">The development VMs provided have all the AX 2012 R3 components installed with Visual Studio 2013 and AX 2012 R3 development tools.</span></span> <span data-ttu-id="421bc-476">VM は、展開時に Active Directory ドメインに結合されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-476">The VMs are joined to the Active Directory domain at deployment time.</span></span> <span data-ttu-id="421bc-477">カスタマイズ オプションとして Active Directory ドメインを指定する場合は、VM はそのドメインに参加します。</span><span class="sxs-lookup"><span data-stu-id="421bc-477">If you provided an Active Directory domain as a customization option, then the VMs will join to that domain.</span></span> <span data-ttu-id="421bc-478">開発 VM は、AX 2012 R3 チェックリストの時点まで配置され、すべてのソフトウェアがインストールされていることがテスト環境にリストされます。</span><span class="sxs-lookup"><span data-stu-id="421bc-478">Development VMs will be deployed up to the point of the AX 2012 R3 checklist, and have all the software installed that is listed in the Test environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="421bc-479">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="421bc-479">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="421bc-480">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="421bc-480">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/support/legal/sla/).</span></span>

## <a name="test-environment"></a><span data-ttu-id="421bc-481">テスト環境</span><span class="sxs-lookup"><span data-stu-id="421bc-481">Test environment</span></span>
<span data-ttu-id="421bc-482">この環境には、既定で数台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="421bc-482">This environment includes several virtual machines, by default.</span></span> <span data-ttu-id="421bc-483">これらの仮想マシンには、Windows Server と、AX 2012 R3 のテストに必要なすべてのソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="421bc-483">These virtual machines have Windows Server—and the software that you’ll need for AX 2012 R3 testing purposes—already installed on them.</span></span> <span data-ttu-id="421bc-484">次のテーブルは、既定のテスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="421bc-484">The following table lists details about the default test environment.</span></span> <span data-ttu-id="421bc-485">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="421bc-485">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="421bc-486">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="421bc-486">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="421bc-487">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="421bc-487">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/support/legal/sla/).</span></span> <span data-ttu-id="421bc-488">データのインポート/エクスポート フレームワーク (DIXF) コンポーネントは既定ではインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="421bc-488">Data Import/Export Framework (DIXF) components are not installed by default.</span></span> <span data-ttu-id="421bc-489">DIXF を使用する場合は、独自の SQL Server インストール メディアを使用して、SQL Server マシンに SQL Server Integration Services (SSIS) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-489">If you want to use DIXF, you must use your own SQL Server installation media to install SQL Server Integration Services (SSIS) on the SQL Server machine.</span></span> <span data-ttu-id="421bc-490">SSIS をインストールした後は、Dynamics AX CD (VM 内の接続されたドライブで利用可能) を使用し、DIXF コンポーネントを AOS およびクライアント マシンにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="421bc-490">After you install SSIS, you can use the Dynamics AX CD (available on a connected drive within the VMs) to install the DIXF components on the AOS and then client machines.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="421bc-491"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-491"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="421bc-492"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-492"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="421bc-493"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-493"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="421bc-494"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-494"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-495">1</span><span class="sxs-lookup"><span data-stu-id="421bc-495">1</span></span></td>
<td><span data-ttu-id="421bc-496">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="421bc-496">Domain controller</span></span></td>
<td><span data-ttu-id="421bc-497"><strong>サイズ:</strong>D1: 基本的な計算層 (1 コア、3.5 GB メモリ) <strong>既定名:</strong>AD-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-497"><strong>Size:</strong> D1: Basic compute tier (1 core, 3.5 GB memory)<strong>Default name:</strong> AD-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-498">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="421bc-498">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="421bc-499">Active Directory</span><span class="sxs-lookup"><span data-stu-id="421bc-499">Active Directory</span></span></li>
<li><span data-ttu-id="421bc-500">ドメイン名サービス (DNS)</span><span class="sxs-lookup"><span data-stu-id="421bc-500">Domain Name Services (DNS)</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="421bc-501">1</span><span class="sxs-lookup"><span data-stu-id="421bc-501">1</span></span></td>
<td><span data-ttu-id="421bc-502">AOS サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-502">AOS server</span></span></td>
<td><span data-ttu-id="421bc-503"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>AOS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-503"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> AOS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-504">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="421bc-504">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="421bc-505">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="421bc-505">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-506">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="421bc-506">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="421bc-507">Microsoft Project Server</span><span class="sxs-lookup"><span data-stu-id="421bc-507">Microsoft Project Server</span></span></li>
<li><span data-ttu-id="421bc-508">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-508">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-509">Management Studio</span><span class="sxs-lookup"><span data-stu-id="421bc-509">Management Studio</span></span></li>
<li><span data-ttu-id="421bc-510">ネイティブ クライアント</span><span class="sxs-lookup"><span data-stu-id="421bc-510">Native Client</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-511">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-511">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-512">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-512">Server components:</span></span>
<ul>
<li><span data-ttu-id="421bc-513">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="421bc-513">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-514">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-514">Client components:</span></span>
<ul>
<li><span data-ttu-id="421bc-515">クライアント</span><span class="sxs-lookup"><span data-stu-id="421bc-515">Client</span></span></li>
<li><span data-ttu-id="421bc-516">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="421bc-516">Office add-ins</span></span></li>
<li><span data-ttu-id="421bc-517">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="421bc-517">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-518">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-518">Integration components:</span></span>
<ul>
<li><span data-ttu-id="421bc-519">IIS 上の Web サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-519">Web services on IIS</span></span></li>
<li><span data-ttu-id="421bc-520">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="421bc-520">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-521">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="421bc-521">Management utilities</span></span></li>
<li><span data-ttu-id="421bc-522">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-522">Retail components:</span></span>
<ul>
<li><span data-ttu-id="421bc-523">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="421bc-523">Retail Headquarters</span></span></li>
<li><span data-ttu-id="421bc-524">Commerce Data Exchange コンポーネント</span><span class="sxs-lookup"><span data-stu-id="421bc-524">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="421bc-525">Synch Service</span><span class="sxs-lookup"><span data-stu-id="421bc-525">Synch Service</span></span></li>
<li><span data-ttu-id="421bc-526">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="421bc-526">Real-time Service</span></span></li>
<li><span data-ttu-id="421bc-527">Async Server</span><span class="sxs-lookup"><span data-stu-id="421bc-527">Async Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="421bc-528">RapidStart Connector</span><span class="sxs-lookup"><span data-stu-id="421bc-528">RapidStart Connector</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-529">1</span><span class="sxs-lookup"><span data-stu-id="421bc-529">1</span></span></td>
<td><span data-ttu-id="421bc-530">データベース サーバー/BIサーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-530">Database server/BI server</span></span></td>
<td><span data-ttu-id="421bc-531"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>SQL-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-531"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> SQL-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-532">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="421bc-532">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="421bc-533">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-533">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-534">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-534">Database Engine Services</span></span></li>
<li><span data-ttu-id="421bc-535">レポート サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-535">Reporting Services</span></span></li>
<li><span data-ttu-id="421bc-536">分析サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-536">Analysis Services</span></span></li>
<li><span data-ttu-id="421bc-537">Management Studio</span><span class="sxs-lookup"><span data-stu-id="421bc-537">Management Studio</span></span></li>
</ul></li>
</ul><span data-ttu-id="421bc-538">
    <strong>注記:</strong> Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="421bc-538">
    <strong>Note: </strong> Reporting Services is configured to run in Native mode.</span></span> <span data-ttu-id="421bc-539">電源表示を使用するには、追加の構成手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-539">To use Power View, you’ll need to complete additional configuration steps.</span></span> <span data-ttu-id="421bc-540">詳細については、<a href="https://technet.microsoft.com/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-540">For more information, see the prerequisites listed in <a href="https://technet.microsoft.com/library/jj933492.aspx">Create a report by using Power View to connect to a cube</a>.</span></span>
<ul>
<li><span data-ttu-id="421bc-541">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-541">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-542">データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-542">Databases</span></span></li>
<li><span data-ttu-id="421bc-543">ビジネス インテリジェンス コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-543">Business intelligence components:</span></span>
<ul>
<li><span data-ttu-id="421bc-544">Reporting Services 拡張機能</span><span class="sxs-lookup"><span data-stu-id="421bc-544">Reporting Services extensions</span></span></li>
<li><span data-ttu-id="421bc-545">Analysis Services の構成</span><span class="sxs-lookup"><span data-stu-id="421bc-545">Analysis Services configuration</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="421bc-546">0</span><span class="sxs-lookup"><span data-stu-id="421bc-546">0</span></span></td>
<td><span data-ttu-id="421bc-547">エンタープライズ ポータル サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-547">Enterprise Portal server</span></span></td>
<td><span data-ttu-id="421bc-548"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>EP-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-548"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> EP-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-549">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="421bc-549">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="421bc-550">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="421bc-550">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-551">Microsoft SQL Server 2012 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-551">Microsoft SQL Server 2012 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-552">フル テキスト検索</span><span class="sxs-lookup"><span data-stu-id="421bc-552">Full-text Search</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-553">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="421bc-553">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="421bc-554">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-554">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-555">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-555">Server components:</span></span>
<ul>
<li><span data-ttu-id="421bc-556">Web サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-556">Web server components:</span></span>
<ul>
<li><span data-ttu-id="421bc-557">エンタープライズ ポータル (EP)</span><span class="sxs-lookup"><span data-stu-id="421bc-557">Enterprise Portal (EP)</span></span></li>
<li><span data-ttu-id="421bc-558">エンタープライズ検索</span><span class="sxs-lookup"><span data-stu-id="421bc-558">Enterprise Search</span></span></li>
<li><span data-ttu-id="421bc-559">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-559">Help Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="421bc-560">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-560">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="421bc-561">Management Reporter サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="421bc-561">Management Reporter server components</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-562">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-562">Retail components:</span></span>
<ul>
<li><span data-ttu-id="421bc-563">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-563">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="421bc-564">Async Client</span><span class="sxs-lookup"><span data-stu-id="421bc-564">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-565">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-565">Retail Server</span></span></li>
<li><span data-ttu-id="421bc-566">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="421bc-566">Retail Online Channel</span></span></li>
<li><span data-ttu-id="421bc-567">Retail チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-567">Retail Channel Database</span></span></li>
<li><span data-ttu-id="421bc-568">Retail チャンネル コンフィギュレーション ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="421bc-568">Retail Channel Configuration Utility</span></span></li>
<li><span data-ttu-id="421bc-569">Retail ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="421bc-569">Retail Hardware Station</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-570">倉庫モバイル デバイス ポータル</span><span class="sxs-lookup"><span data-stu-id="421bc-570">Warehouse Mobile Devices Portal</span></span></li>
<li><span data-ttu-id="421bc-571">Microsoft Dynamics Connector</span><span class="sxs-lookup"><span data-stu-id="421bc-571">Connector for Microsoft Dynamics</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-572">1</span><span class="sxs-lookup"><span data-stu-id="421bc-572">1</span></span></td>
<td><span data-ttu-id="421bc-573">クライアント コンピューター</span><span class="sxs-lookup"><span data-stu-id="421bc-573">Client computer</span></span></td>
<td><span data-ttu-id="421bc-574"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>CLI-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-574"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> CLI-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-575">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="421bc-575">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="421bc-576">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="421bc-576">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="421bc-577">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-577">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-578">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="421bc-578">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-579">Microsoft SharePoint Server 2013 クライアント コンポーネント SDK</span><span class="sxs-lookup"><span data-stu-id="421bc-579">Microsoft SharePoint Server 2013 Client Components SDK</span></span></li>
<li><span data-ttu-id="421bc-580">Microsoft Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="421bc-580">Microsoft Office 365 ProPlus</span></span></li>
<li><span data-ttu-id="421bc-581">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-581">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-582">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-582">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="421bc-583">Management Reporter レポート デザイナー</span><span class="sxs-lookup"><span data-stu-id="421bc-583">Management Reporter Report Designer</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-584">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-584">Client components:</span></span>
<ul>
<li><span data-ttu-id="421bc-585">クライアント</span><span class="sxs-lookup"><span data-stu-id="421bc-585">Client</span></span></li>
<li><span data-ttu-id="421bc-586">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="421bc-586">Office add-ins</span></span></li>
<li><span data-ttu-id="421bc-587">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="421bc-587">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-588">開発者ツール:</span><span class="sxs-lookup"><span data-stu-id="421bc-588">Developer tools:</span></span>
<ul>
<li><span data-ttu-id="421bc-589">デバッガー</span><span class="sxs-lookup"><span data-stu-id="421bc-589">Debugger</span></span></li>
<li><span data-ttu-id="421bc-590">Visual Studio ツール</span><span class="sxs-lookup"><span data-stu-id="421bc-590">Visual Studio Tools</span></span></li>
<li><span data-ttu-id="421bc-591">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="421bc-591">Trace Parser</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-592">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="421bc-592">Management utilities</span></span></li>
<li><span data-ttu-id="421bc-593">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-593">Retail components:</span></span>
<ul>
<li><span data-ttu-id="421bc-594">Retail POS</span><span class="sxs-lookup"><span data-stu-id="421bc-594">Retail POS</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="421bc-595">0</span><span class="sxs-lookup"><span data-stu-id="421bc-595">0</span></span></td>
<td><span data-ttu-id="421bc-596">リモート デスクトップ サービス サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-596">Remote Desktop Services server</span></span></td>
<td><span data-ttu-id="421bc-597"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>RDS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-597"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> RDS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-598">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="421bc-598">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="421bc-599">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="421bc-599">Internet Information Services (IIS)</span></span></li>
<li><span data-ttu-id="421bc-600">リモート デスクトップ サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-600">Remote Desktop Services</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-601">Microsoft SQL Server 2012 ネイティブ クライアント</span><span class="sxs-lookup"><span data-stu-id="421bc-601">Microsoft SQL Server 2012 Native Client</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-essentials-devtest-environment"></a><span data-ttu-id="421bc-602">Retail Essentials 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="421bc-602">Retail Essentials dev/test environment</span></span>
<span data-ttu-id="421bc-603">この環境を配置して、Retail essentials の機能を開発またはテストします。</span><span class="sxs-lookup"><span data-stu-id="421bc-603">Deploy this environment to develop or test features for Retail essentials.</span></span> <span data-ttu-id="421bc-604">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="421bc-604">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="421bc-605">この仮想マシンには、Windows Server と、Retail Essentials の開発とテストで必要となるソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="421bc-605">This virtual machine has Windows Server—and the software that you’ll need for Retail essentials development and testing purposes—already installed on it.</span></span> <span data-ttu-id="421bc-606">次のテーブルは、既定の Retail Essentials 開発/テスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="421bc-606">The following table lists details about the default Retail essentials dev/test environment.</span></span> <span data-ttu-id="421bc-607">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="421bc-607">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="421bc-608">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="421bc-608">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="421bc-609">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="421bc-609">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/support/legal/sla/).</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="421bc-610"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-610"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="421bc-611"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-611"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="421bc-612"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-612"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="421bc-613"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-613"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-614">1</span><span class="sxs-lookup"><span data-stu-id="421bc-614">1</span></span></td>
<td><span data-ttu-id="421bc-615">Retail Essentials サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-615">Retail essentials server</span></span></td>
<td><span data-ttu-id="421bc-616"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>ESSEN-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-616"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> ESSEN-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-617">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="421bc-617">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="421bc-618">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-618">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-619">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-619">Database Engine Services</span></span></li>
<li><span data-ttu-id="421bc-620">Management Studio</span><span class="sxs-lookup"><span data-stu-id="421bc-620">Management Studio</span></span></li>
<li><span data-ttu-id="421bc-621">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="421bc-621">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-622">AX 2012 R3 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-622">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-623">データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-623">Databases</span></span></li>
<li><span data-ttu-id="421bc-624">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-624">Server components:</span></span>
<ul>
<li><span data-ttu-id="421bc-625">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="421bc-625">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-626">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-626">Client components:</span></span>
<ul>
<li><span data-ttu-id="421bc-627">クライアント</span><span class="sxs-lookup"><span data-stu-id="421bc-627">Client</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-628">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-628">Integration components:</span></span>
<ul>
<li><span data-ttu-id="421bc-629">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="421bc-629">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-630">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-630">Retail components:</span></span>
<ul>
<li><span data-ttu-id="421bc-631">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="421bc-631">Retail Headquarters</span></span></li>
<li><span data-ttu-id="421bc-632">Commerce Data Exchange コンポーネント</span><span class="sxs-lookup"><span data-stu-id="421bc-632">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="421bc-633">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="421bc-633">Real-time Service</span></span></li>
<li><span data-ttu-id="421bc-634">Async Server</span><span class="sxs-lookup"><span data-stu-id="421bc-634">Async Server</span></span></li>
<li><span data-ttu-id="421bc-635">Async Client</span><span class="sxs-lookup"><span data-stu-id="421bc-635">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-636">小売チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-636">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-ecommerce-devtest-environment"></a><span data-ttu-id="421bc-637">Retail E-commerce 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="421bc-637">Retail ecommerce dev/test environment</span></span>
<span data-ttu-id="421bc-638">この環境を配置して、AX 2012 R3 と完全に統合されたオンライン販売チャネルを作成し、テストします。</span><span class="sxs-lookup"><span data-stu-id="421bc-638">Deploy this environment to create and test an online sales channel that is fully integrated with AX 2012 R3.</span></span> <span data-ttu-id="421bc-639">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="421bc-639">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="421bc-640">この仮想マシンには、Windows Server と、小売電子商取引に必要なソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="421bc-640">This virtual machine has Windows Server—and the software that you’ll need for Retail e-commerce—already installed on it.</span></span> <span data-ttu-id="421bc-641">次のテーブルは、既定の Retail E-commerce 開発/テスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="421bc-641">The following table lists details about the default Retail e-commerce dev/test environment.</span></span> <span data-ttu-id="421bc-642">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="421bc-642">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="421bc-643">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="421bc-643">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="421bc-644">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="421bc-644">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/support/legal/sla/).</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="421bc-645"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-645"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="421bc-646"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-646"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="421bc-647"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-647"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="421bc-648"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-648"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-649">1</span><span class="sxs-lookup"><span data-stu-id="421bc-649">1</span></span></td>
<td><span data-ttu-id="421bc-650">Retail E-commerce サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-650">Retail e-commerce server</span></span></td>
<td><span data-ttu-id="421bc-651"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>E-COM-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-651"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> E-COM-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-652">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="421bc-652">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="421bc-653">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="421bc-653">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="421bc-654">AX 2012 R3 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-654">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-655">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-655">Retail components:</span></span>
<ul>
<li><span data-ttu-id="421bc-656">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-656">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="421bc-657">Async Client</span><span class="sxs-lookup"><span data-stu-id="421bc-657">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-658">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="421bc-658">Retail online channel</span></span></li>
<li><span data-ttu-id="421bc-659">小売チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-659">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="retail-mobility-devtest-environment"></a><span data-ttu-id="421bc-660">Retail mobility 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="421bc-660">Retail mobility dev/test environment</span></span>
<span data-ttu-id="421bc-661">この環境を配置することで、販売スタッフが販売トランザクションを処理し、顧客注文を入力し、店舗内のどこでもモバイル デバイスを使用して日々の操作と在庫管理を実行できます。</span><span class="sxs-lookup"><span data-stu-id="421bc-661">Deploy this environment to enable your sales staff to process sales transactions, enter customer orders, and perform daily operations and inventory management with mobile devices anywhere in a store.</span></span> <span data-ttu-id="421bc-662">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="421bc-662">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="421bc-663">この仮想マシンには、Windows Server と、Retail mobilityに必要なソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="421bc-663">This virtual machine has Windows Server—and the software that you’ll need for Retail mobility—already installed on it.</span></span> <span data-ttu-id="421bc-664">次のテーブルは、既定の Retail Mobility 開発/テスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="421bc-664">The following table lists details about the default Retail mobility dev/test environment.</span></span> <span data-ttu-id="421bc-665">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="421bc-665">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 
> [!NOTE]
> <span data-ttu-id="421bc-666">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="421bc-666">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="421bc-667">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="421bc-667">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/support/legal/sla/).</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="421bc-668"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-668"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="421bc-669"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-669"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="421bc-670"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-670"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="421bc-671"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-671"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-672">1</span><span class="sxs-lookup"><span data-stu-id="421bc-672">1</span></span></td>
<td><span data-ttu-id="421bc-673">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-673">Retail server</span></span></td>
<td><span data-ttu-id="421bc-674"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>MOBIL-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-674"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> MOBIL-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-675">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="421bc-675">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="421bc-676">AX 2012 R3 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-676">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-677">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-677">Retail components:</span></span>
<ul>
<li><span data-ttu-id="421bc-678">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-678">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="421bc-679">Async Client</span><span class="sxs-lookup"><span data-stu-id="421bc-679">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-680">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-680">Retail Server</span></span></li>
<li><span data-ttu-id="421bc-681">小売チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-681">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="high-availability-environment"></a><span data-ttu-id="421bc-682">高可用性環境</span><span class="sxs-lookup"><span data-stu-id="421bc-682">High availability environment</span></span>
<span data-ttu-id="421bc-683">この環境を配置して、高可用性のためにコンフィギュレーションできる環境で AX 2012 R3 を使用します。</span><span class="sxs-lookup"><span data-stu-id="421bc-683">Deploy this environment to use AX 2012 R3 in an environment that can be configured for high availability.</span></span> <span data-ttu-id="421bc-684">この環境には、数台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="421bc-684">This environment includes several virtual machines.</span></span> <span data-ttu-id="421bc-685">これらの仮想マシンには、Windows Server と、AX 2012 R3 を使用するために必要なソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="421bc-685">These virtual machines have Windows Server—and the software that you’ll need to use AX 2012 R3—already installed on them.</span></span> <span data-ttu-id="421bc-686">次のテーブルは、既定の高可用性環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="421bc-686">The following table lists details about the default high availability environment.</span></span> <span data-ttu-id="421bc-687">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="421bc-687">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="421bc-688">Azure Premium Storage は高可用性環境が必要です。</span><span class="sxs-lookup"><span data-stu-id="421bc-688">Azure Premium Storage is required for high availability environments.</span></span> <span data-ttu-id="421bc-689">詳細については、[Azure での高可用性環境の配置](deploy-high-availability-environment-azure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-689">For more information, see [Deploy a high availability environment on Azure](deploy-high-availability-environment-azure.md).</span></span> <span data-ttu-id="421bc-690">この環境の仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/support/legal/sla/)の対象となります。</span><span class="sxs-lookup"><span data-stu-id="421bc-690">The virtual machines in this environment are covered by an Azure [Service Level Agreement](http://azure.microsoft.com/support/legal/sla/).</span></span> <span data-ttu-id="421bc-691">データのインポート/エクスポート フレームワーク (DIXF) コンポーネントは既定ではインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="421bc-691">Data Import/Export Framework (DIXF) components are not installed by default.</span></span> <span data-ttu-id="421bc-692">DIXF を使用する場合は、独自の SQL Server インストール メディアを使用して、SQL Server マシンに SQL Server Integration Services (SSIS) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-692">If you want to use DIXF, you must use your own SQL Server installation media to install SQL Server Integration Services (SSIS) on the SQL Server machine.</span></span> <span data-ttu-id="421bc-693">SSIS をインストールした後は、Dynamics AX CD (VM 内の接続されたドライブで利用可能) を使用し、DIXF コンポーネントを AOS およびクライアント マシンにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="421bc-693">After you install SSIS, you can use the Dynamics AX CD (available on a connected drive within the VMs) to install the DIXF components on the AOS and then client machines.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="421bc-694"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-694"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="421bc-695"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-695"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="421bc-696"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-696"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="421bc-697"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-697"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-698">3 <strong>注記:</strong> 3 つのドメイン コントローラがこの環境に配置されています。</span><span class="sxs-lookup"><span data-stu-id="421bc-698">3<strong>Note: </strong>Three domain controllers are deployed in this environment.</span></span> <span data-ttu-id="421bc-699">1 つのドメイン コントローラーが失敗すると、Azure の<a href="http://azure.microsoft.com/support/legal/sla/">サービス レベル同意書</a>に準拠するために、2 つのオンライン ドメイン コントローラーを残しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-699">If one domain controller fails, you must be left with two, online domain controllers in order to meet Azure’s <a href="http://azure.microsoft.com/support/legal/sla/">Service Level Agreement</a>.</span></span></td>
<td><span data-ttu-id="421bc-700">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="421bc-700">Domain controller</span></span></td>
<td><span data-ttu-id="421bc-701"><strong>サイズ:</strong>D1: 基本的な計算層 (1 コア、3.5 GB メモリ) <strong>既定名:</strong>AD-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-701"><strong>Size:</strong> D1: Basic compute tier (1 core, 3.5 GB memory)<strong>Default name:</strong> AD-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-702">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="421bc-702">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="421bc-703">Active Directory</span><span class="sxs-lookup"><span data-stu-id="421bc-703">Active Directory</span></span></li>
<li><span data-ttu-id="421bc-704">ドメイン名サービス (DNS)</span><span class="sxs-lookup"><span data-stu-id="421bc-704">Domain Name Services (DNS)</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="421bc-705">2</span><span class="sxs-lookup"><span data-stu-id="421bc-705">2</span></span></td>
<td><span data-ttu-id="421bc-706">AOS サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-706">AOS server</span></span></td>
<td><span data-ttu-id="421bc-707"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>AOS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-707"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> AOS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-708">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="421bc-708">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="421bc-709">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="421bc-709">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-710">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="421bc-710">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="421bc-711">Microsoft Project Server</span><span class="sxs-lookup"><span data-stu-id="421bc-711">Microsoft Project Server</span></span></li>
<li><span data-ttu-id="421bc-712">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-712">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-713">Management Studio</span><span class="sxs-lookup"><span data-stu-id="421bc-713">Management Studio</span></span></li>
<li><span data-ttu-id="421bc-714">ネイティブ クライアント</span><span class="sxs-lookup"><span data-stu-id="421bc-714">Native Client</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-715">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-715">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-716">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-716">Server components:</span></span>
<ul>
<li><span data-ttu-id="421bc-717">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="421bc-717">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-718">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-718">Client components:</span></span>
<ul>
<li><span data-ttu-id="421bc-719">クライアント</span><span class="sxs-lookup"><span data-stu-id="421bc-719">Client</span></span></li>
<li><span data-ttu-id="421bc-720">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="421bc-720">Office add-ins</span></span></li>
<li><span data-ttu-id="421bc-721">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="421bc-721">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-722">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-722">Integration components:</span></span>
<ul>
<li><span data-ttu-id="421bc-723">IIS 上の Web サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-723">Web services on IIS</span></span></li>
<li><span data-ttu-id="421bc-724">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="421bc-724">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-725">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="421bc-725">Management utilities</span></span></li>
<li><span data-ttu-id="421bc-726">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-726">Retail components:</span></span>
<ul>
<li><span data-ttu-id="421bc-727">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="421bc-727">Retail Headquarters</span></span></li>
<li><span data-ttu-id="421bc-728">Commerce Data Exchange コンポーネント</span><span class="sxs-lookup"><span data-stu-id="421bc-728">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="421bc-729">Synch Service</span><span class="sxs-lookup"><span data-stu-id="421bc-729">Synch Service</span></span></li>
<li><span data-ttu-id="421bc-730">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="421bc-730">Real-time Service</span></span></li>
<li><span data-ttu-id="421bc-731">Async Server</span><span class="sxs-lookup"><span data-stu-id="421bc-731">Async Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="421bc-732">RapidStart Connector</span><span class="sxs-lookup"><span data-stu-id="421bc-732">RapidStart Connector</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-733">2</span><span class="sxs-lookup"><span data-stu-id="421bc-733">2</span></span></td>
<td><span data-ttu-id="421bc-734">データベース サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-734">Database server</span></span></td>
<td><span data-ttu-id="421bc-735"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>SQL-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-735"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> SQL-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-736">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="421bc-736">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="421bc-737">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-737">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-738">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-738">Database Engine Services</span></span></li>
<li><span data-ttu-id="421bc-739">Management Studio</span><span class="sxs-lookup"><span data-stu-id="421bc-739">Management Studio</span></span></li>
</ul></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="421bc-740"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-740"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-741">クォーラム サーバーも配置されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-741">A Quorum server is also deployed.</span></span> <span data-ttu-id="421bc-742">この仮想マシンは、AlwaysOn 可用性グループのリスナーです。</span><span class="sxs-lookup"><span data-stu-id="421bc-742">This virtual machine is a listener for the AlwaysOn availability group.</span></span> <span data-ttu-id="421bc-743">この仮想マシンは、o    [高可用性 VM] ボックスの一覧には表示されませんが、高可用性環境で展開されます。o    QRM -&lt;GUID&gt; という名前です。</span><span class="sxs-lookup"><span data-stu-id="421bc-743">This virtual machine:o    Is not represented in the High Availability VM list, but it is deployed with High Availability environments.o    Is named QRM-&lt;GUID&gt;.</span></span> <span data-ttu-id="421bc-744">この名前はカスタマイズできません。o    A2 仮想マシンです。o    Windows Server 2012 R2 のギャラリー画像を実行します。o    配置後には、この VM は、高可用性環境に VM を追加するときに「データベース サーバー」として表示されます。</span><span class="sxs-lookup"><span data-stu-id="421bc-744">This name can’t be customized.o    Is an A2 virtual machine.o    Runs a gallery image of Windows Server 2012 R2.o    Post deployment, this VM appears as a “Database Server” when adding VMs to the High Availability environment.</span></span> <span data-ttu-id="421bc-745">ここで参照されている 3 番目の VM は、明示的に SQL Server ではない A2 Quorum Server です。</span><span class="sxs-lookup"><span data-stu-id="421bc-745">The 3rd VM referenced here is the A2 Quorum Server which is explicitly not a SQL Server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="421bc-746"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-746"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-747">Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="421bc-747">Reporting Services is configured to run in Native mode.</span></span> <span data-ttu-id="421bc-748">電源表示を使用するには、追加の構成手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-748">To use Power View, you’ll need to complete additional configuration steps.</span></span> <span data-ttu-id="421bc-749">詳細については、<a href="https://technet.microsoft.com/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-749">For more information, see the prerequisites listed in <a href="https://technet.microsoft.com/library/jj933492.aspx">Create a report by using Power View to connect to a cube</a>.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="421bc-750">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-750">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-751">データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-751">Databases</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="421bc-752">2</span><span class="sxs-lookup"><span data-stu-id="421bc-752">2</span></span></td>
<td><span data-ttu-id="421bc-753">ビジネス インテリジェンス (BI) サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-753">Business intelligence (BI) server</span></span></td>
<td><span data-ttu-id="421bc-754"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>BI-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-754"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> BI-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-755">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="421bc-755">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="421bc-756">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-756">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-757">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-757">Database Engine Services</span></span></li>
<li><span data-ttu-id="421bc-758">レポート サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-758">Reporting Services</span></span></li>
<li><span data-ttu-id="421bc-759">分析サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-759">Analysis Services</span></span></li>
<li><span data-ttu-id="421bc-760">Management Studio</span><span class="sxs-lookup"><span data-stu-id="421bc-760">Management Studio</span></span></li>
</ul></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="421bc-761"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="421bc-761"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-762">Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="421bc-762">Reporting Services is configured to run in Native mode.</span></span> <span data-ttu-id="421bc-763">電源表示を使用するには、追加の構成手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="421bc-763">To use Power View, you’ll need to complete additional configuration steps.</span></span> <span data-ttu-id="421bc-764">詳細については、<a href="https://technet.microsoft.com/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="421bc-764">For more information, see the prerequisites listed in <a href="https://technet.microsoft.com/library/jj933492.aspx">Create a report by using Power View to connect to a cube</a>.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="421bc-765">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-765">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-766">ビジネス インテリジェンス コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-766">Business intelligence components:</span></span>
<ul>
<li><span data-ttu-id="421bc-767">Reporting Services 拡張機能</span><span class="sxs-lookup"><span data-stu-id="421bc-767">Reporting Services extensions</span></span></li>
<li><span data-ttu-id="421bc-768">Analysis Services の構成</span><span class="sxs-lookup"><span data-stu-id="421bc-768">Analysis Services configuration</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-769">0</span><span class="sxs-lookup"><span data-stu-id="421bc-769">0</span></span></td>
<td><span data-ttu-id="421bc-770">エンタープライズ ポータル サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-770">Enterprise Portal server</span></span></td>
<td><span data-ttu-id="421bc-771"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>EP-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-771"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> EP-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-772">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="421bc-772">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="421bc-773">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="421bc-773">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-774">Microsoft SQL Server 2012 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-774">Microsoft SQL Server 2012 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-775">フル テキスト検索</span><span class="sxs-lookup"><span data-stu-id="421bc-775">Full-text Search</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-776">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="421bc-776">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="421bc-777">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-777">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-778">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-778">Server components:</span></span>
<ul>
<li><span data-ttu-id="421bc-779">Web サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-779">Web server components:</span></span>
<ul>
<li><span data-ttu-id="421bc-780">エンタープライズ ポータル (EP)</span><span class="sxs-lookup"><span data-stu-id="421bc-780">Enterprise Portal (EP)</span></span></li>
<li><span data-ttu-id="421bc-781">エンタープライズ検索</span><span class="sxs-lookup"><span data-stu-id="421bc-781">Enterprise Search</span></span></li>
<li><span data-ttu-id="421bc-782">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-782">Help Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="421bc-783">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-783">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="421bc-784">Management Reporter サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="421bc-784">Management Reporter server components</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-785">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-785">Retail components:</span></span>
<ul>
<li><span data-ttu-id="421bc-786">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-786">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="421bc-787">Async Client</span><span class="sxs-lookup"><span data-stu-id="421bc-787">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-788">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-788">Retail Server</span></span></li>
<li><span data-ttu-id="421bc-789">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="421bc-789">Retail Online Channel</span></span></li>
<li><span data-ttu-id="421bc-790">Retail チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="421bc-790">Retail Channel Database</span></span></li>
<li><span data-ttu-id="421bc-791">Retail チャンネル コンフィギュレーション ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="421bc-791">Retail Channel Configuration Utility</span></span></li>
<li><span data-ttu-id="421bc-792">Retail ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="421bc-792">Retail Hardware Station</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-793">倉庫モバイル デバイス ポータル</span><span class="sxs-lookup"><span data-stu-id="421bc-793">Warehouse Mobile Devices Portal</span></span></li>
<li><span data-ttu-id="421bc-794">Microsoft Dynamics Connector</span><span class="sxs-lookup"><span data-stu-id="421bc-794">Connector for Microsoft Dynamics</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="421bc-795">2</span><span class="sxs-lookup"><span data-stu-id="421bc-795">2</span></span></td>
<td><span data-ttu-id="421bc-796">クライアント コンピューター</span><span class="sxs-lookup"><span data-stu-id="421bc-796">Client computer</span></span></td>
<td><span data-ttu-id="421bc-797"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>CLI-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-797"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> CLI-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-798">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="421bc-798">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="421bc-799">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="421bc-799">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="421bc-800">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-800">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-801">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="421bc-801">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-802">Microsoft SharePoint Server 2013 クライアント コンポーネント SDK</span><span class="sxs-lookup"><span data-stu-id="421bc-802">Microsoft SharePoint Server 2013 Client Components SDK</span></span></li>
<li><span data-ttu-id="421bc-803">Microsoft Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="421bc-803">Microsoft Office 365 ProPlus</span></span></li>
<li><span data-ttu-id="421bc-804">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-804">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="421bc-805">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-805">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="421bc-806">Management Reporter レポート デザイナー</span><span class="sxs-lookup"><span data-stu-id="421bc-806">Management Reporter Report Designer</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-807">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-807">Client components:</span></span>
<ul>
<li><span data-ttu-id="421bc-808">クライアント</span><span class="sxs-lookup"><span data-stu-id="421bc-808">Client</span></span></li>
<li><span data-ttu-id="421bc-809">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="421bc-809">Office add-ins</span></span></li>
<li><span data-ttu-id="421bc-810">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="421bc-810">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-811">開発者ツール:</span><span class="sxs-lookup"><span data-stu-id="421bc-811">Developer tools:</span></span>
<ul>
<li><span data-ttu-id="421bc-812">デバッガー</span><span class="sxs-lookup"><span data-stu-id="421bc-812">Debugger</span></span></li>
<li><span data-ttu-id="421bc-813">Visual Studio ツール</span><span class="sxs-lookup"><span data-stu-id="421bc-813">Visual Studio Tools</span></span></li>
<li><span data-ttu-id="421bc-814">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="421bc-814">Trace Parser</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-815">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="421bc-815">Management utilities</span></span></li>
<li><span data-ttu-id="421bc-816">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="421bc-816">Retail components:</span></span>
<ul>
<li><span data-ttu-id="421bc-817">Retail POS</span><span class="sxs-lookup"><span data-stu-id="421bc-817">Retail POS</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="421bc-818">2</span><span class="sxs-lookup"><span data-stu-id="421bc-818">2</span></span></td>
<td><span data-ttu-id="421bc-819">リモート デスクトップ サービス サーバー</span><span class="sxs-lookup"><span data-stu-id="421bc-819">Remote Desktop Services server</span></span></td>
<td><span data-ttu-id="421bc-820"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>RDS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="421bc-820"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> RDS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="421bc-821">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="421bc-821">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="421bc-822">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="421bc-822">Internet Information Services (IIS)</span></span></li>
<li><span data-ttu-id="421bc-823">リモート デスクトップ サービス</span><span class="sxs-lookup"><span data-stu-id="421bc-823">Remote Desktop Services</span></span></li>
</ul></li>
<li><span data-ttu-id="421bc-824">Microsoft SQL Server 2012 ネイティブ クライアント</span><span class="sxs-lookup"><span data-stu-id="421bc-824">Microsoft SQL Server 2012 Native Client</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="next-steps"></a><span data-ttu-id="421bc-825">次のステップ</span><span class="sxs-lookup"><span data-stu-id="421bc-825">Next steps</span></span>
- [<span data-ttu-id="421bc-826">Azure に AX 2012 R3 または AX 2012 R3 CU8 デモ環境を配置します</span><span class="sxs-lookup"><span data-stu-id="421bc-826">Deploy an AX 2012 R3 or AX 2012 R3 CU8 demo environment on Azure</span></span>](deploy-ax-2012-r3-ax-2012-r3-cu8-demo-environment-azure.md) 
- [<span data-ttu-id="421bc-827">Azure での Retail Essentials デモ環境の配置</span><span class="sxs-lookup"><span data-stu-id="421bc-827">Deploy a Retail essentials demo environment on Azure</span></span>](deploy-retail-essentials-demo-environment-azure.md) 
- [<span data-ttu-id="421bc-828">Azure での開発環境の配置</span><span class="sxs-lookup"><span data-stu-id="421bc-828">Deploy a development environment on Azure</span></span>](deploy-development-environment-azure.md) 
- [<span data-ttu-id="421bc-829">Azure でのテスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="421bc-829">Deploy a test environment on Azure</span></span>](deploy-test-environment-azure.md) 
- [<span data-ttu-id="421bc-830">Azure での Retail Essentials 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="421bc-830">Deploy a Retail essentials dev/test environment on Azure</span></span>](deploy-retail-essentials-devtest-environment-azure.md) 
- [<span data-ttu-id="421bc-831">Azure での Retail E-commerce 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="421bc-831">Deploy a Retail e-commerce dev/test environment on Azure</span></span>](deploy-retail-ecommerce-devtest-environment-azure.md) 
- [<span data-ttu-id="421bc-832">Azure での Retail Mobility 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="421bc-832">Deploy a Retail mobility dev/test environment on Azure</span></span>](deploy-retail-mobility-devtest-environment-azure.md) 
- [<span data-ttu-id="421bc-833">Azure に高可用性環境を配置する</span><span class="sxs-lookup"><span data-stu-id="421bc-833">Deploy a high availability environment on Azure</span></span>](deploy-high-availability-environment-azure.md)