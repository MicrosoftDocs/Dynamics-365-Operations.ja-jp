---
title: "Azure での Dynamics AX 2012 R3 配置の計画"
description: "Microsoft Azure に Microsoft Dynamics AX 2012 R3 を展開する前に、いくつかの点を考慮し決定する必要があります。 この記事では、計画プロセスについて説明します。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18591
ms.assetid: 84e597d7-6ad3-4322-8ac3-6b6151dd24f6
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 905084f3fdd0a18bdd4de2729fd4c6589e4bc9ea
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="plan-your-dynamics-ax-2012-r3-deployment-on-azure"></a><span data-ttu-id="fee39-104">Azure での Dynamics AX 2012 R3 配置の計画</span><span class="sxs-lookup"><span data-stu-id="fee39-104">Plan your Dynamics AX 2012 R3 deployment on Azure</span></span>

[!INCLUDE [banner](../../includes/banner.md)]

<span data-ttu-id="fee39-105">Microsoft Azure に Microsoft Dynamics AX 2012 R3 を展開する前に、いくつかの点を考慮し決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-105">Before you can deploy Microsoft Dynamics AX 2012 R3 on Microsoft Azure, there are several things you must consider and decisions you must make.</span></span> <span data-ttu-id="fee39-106">この記事では、計画プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fee39-106">This article guides you through the planning process.</span></span> 

<span data-ttu-id="fee39-107">Azure 上の AX 2012 R3 の配備は、Microsoft が次のシナリオでサポートしています。</span><span class="sxs-lookup"><span data-stu-id="fee39-107">Deployments of AX 2012 R3 on Azure are supported by Microsoft in the following scenarios:</span></span> 
- <span data-ttu-id="fee39-108">配置は、Microsoft Dynamics Lifecycle Services (LCS) を通じて実行されています。</span><span class="sxs-lookup"><span data-stu-id="fee39-108">The deployment has been performed through Microsoft Dynamics Lifecycle Services (LCS).</span></span> 
- <span data-ttu-id="fee39-109">以下のガイダンスに厳密に従って実施された顧客またはパートナー主導配置。</span><span class="sxs-lookup"><span data-stu-id="fee39-109">Customer or partner-driven deployments that have been performed strictly adhering to the following guidance:</span></span> 
   - <span data-ttu-id="fee39-110">SQL は、(SQL クラスタリング/Always On を使用して) 可用性トポロジに配置されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-110">SQL is deployed in a High Availability topology (using SQL Clustering/Always On).</span></span>
   - <span data-ttu-id="fee39-111">Azure に配置するために、[Azure 仮想マシンでの SQL Server のパフォーマンス ベスト プラクティス](/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)を使用して、SQL のベスト プラクティスに従っています。</span><span class="sxs-lookup"><span data-stu-id="fee39-111">SQL best practices have been followed for deployment in Azure, using the [Performance best practices for SQL Server in Azure Virtual Machines](/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance).</span></span> 
   - <span data-ttu-id="fee39-112">[SQL サーバーおよび記憶域の設定のコンフィギュレーション (TechNet)](https://technet.microsoft.com/en-us/library/dd309734.aspx) によって指定された AX 2012 の SQL Server コンフィギュレーションのベスト プラクティスに従っています。</span><span class="sxs-lookup"><span data-stu-id="fee39-112">Best practices for SQL Server configuration for AX 2012 have been followed, as specified in [Configure SQL Server and storage settings (TechNet)](https://technet.microsoft.com/en-us/library/dd309734.aspx).</span></span> 
   - <span data-ttu-id="fee39-113">[システム診断](system-diagnostics-lcs.md)で指定されているように、システム診断ツールがインストールされ、ベスト プラクティスに従います。</span><span class="sxs-lookup"><span data-stu-id="fee39-113">The System diagnostic tool is installed and best practices are followed, as specified in [System diagnostics](system-diagnostics-lcs.md)</span></span> 

> [!NOTE]
> <span data-ttu-id="fee39-114">Azure 環境でサポートされていない AX 2012 R3 に問題があり、LCS 経由で Azure に展開された、またはローカルに展開された AX 2012 R3 環境で同じ問題を再現することができる場合、Microsoft がサポートを提供できます。</span><span class="sxs-lookup"><span data-stu-id="fee39-114">If you have an issue in an unsupported AX 2012 R3 on Azure environment, and can reproduce the same issue in an AX 2012 R3 environment that was either deployed to Azure through LCS, or deployed locally, Microsoft can provide support.</span></span>
> 
> <span data-ttu-id="fee39-115">AX 2012 R3 は、オンプレミスでも配置できます。</span><span class="sxs-lookup"><span data-stu-id="fee39-115">AX 2012 R3 can also be deployed on-premises.</span></span> <span data-ttu-id="fee39-116">詳細については、トピックの [Microsoft Dynamics AX 2012 のインストール](https://technet.microsoft.com/en-us/library/dd362138.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-116">For details, see the topic [Install Microsoft Dynamics AX 2012](https://technet.microsoft.com/en-us/library/dd362138.aspx).</span></span>

## <a name="verify-that-you-can-log-on-to-lifecycle-services"></a><span data-ttu-id="fee39-117">Lifecycle Services にログオンできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fee39-117">Verify that you can log on to Lifecycle Services</span></span>
<span data-ttu-id="fee39-118">Lifecycle Services (LCS) は、顧客およびパートナーが Microsoft Dynamics AX のプロジェクトの管理に使用できるクラウドベースの共同ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="fee39-118">Lifecycle Services (LCS) is a cloud-based collaborative workspace that customers and partners can use to manage Microsoft Dynamics AX projects.</span></span> <span data-ttu-id="fee39-119">Azure 上に AX 2012 R3 を配置するには、Lifecycle Services Web サイトで利用できるクラウド ホスト環境ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="fee39-119">You’ll use the Cloud-hosted environments tool, available on the Lifecycle Services website, to deploy AX 2012 R3 on Azure.</span></span> <span data-ttu-id="fee39-120">Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="fee39-120">Lifecycle Services is available to customers and partners as part of their support plans.</span></span> <span data-ttu-id="fee39-121">CustomerSource または PartnerSource の資格情報でアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="fee39-121">You can access it with your CustomerSource or PartnerSource credentials.</span></span> [<span data-ttu-id="fee39-122">Lifecycle Services にログオンできることを確認する</span><span class="sxs-lookup"><span data-stu-id="fee39-122">Verify that you can log on to Lifecycle Services</span></span>](https://lcs.dynamics.com/)

## <a name="purchase-an-azure-subscription"></a><span data-ttu-id="fee39-123">Azure サブスクリプションの購買</span><span class="sxs-lookup"><span data-stu-id="fee39-123">Purchase an Azure subscription</span></span>
<span data-ttu-id="fee39-124">Azure を使用するには、サブスクリプションを購入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-124">To use Azure, you must purchase a subscription.</span></span> <span data-ttu-id="fee39-125">サブスクリプション プランおよび価格決定の詳細については、[Azure 価格決定](https://azure.microsoft.com/en-us/pricing/) ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-125">For information about subscription plans and pricing details, see the [Azure pricing](https://azure.microsoft.com/en-us/pricing/) page.</span></span> <span data-ttu-id="fee39-126">その後、そのページの指示に従ってサブスクリプションを購入します。</span><span class="sxs-lookup"><span data-stu-id="fee39-126">Then follow the instructions on that page to purchase a subscription.</span></span> <span data-ttu-id="fee39-127">サブスクリプションは、Azure に配備する AX 2012 R3 環境をサポートするのに十分な大きさでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="fee39-127">The subscription must be large enough to support the AX 2012 R3 environment that you want to deploy on Azure.</span></span> <span data-ttu-id="fee39-128">次のテーブルは、Azure に配置できる AX 2012 R3 環境のタイプと、各環境を既定のコンフィギュレーションで配置するために必要なコアの数を示しています。</span><span class="sxs-lookup"><span data-stu-id="fee39-128">The following table lists the types of AX 2012 R3 environments that you can deploy on Azure, and the number of cores required to deploy each environment in its default configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="fee39-129">環境を配置するときに、配置される仮想マシンの数とサイズを変更できることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-129">Keep in mind that when you deploy an environment, you can change the number and size of the virtual machines that are deployed.</span></span> <span data-ttu-id="fee39-130">ただし、次のテーブルでは、その*既定*コンフィギュレーションで各環境を配置するために必要なコアの数を一覧にします。</span><span class="sxs-lookup"><span data-stu-id="fee39-130">However, this table lists the number of cores required to deploy each environment in its *default* configuration.</span></span>

<span data-ttu-id="fee39-131">**環境タイプ:** - デモ</span><span class="sxs-lookup"><span data-stu-id="fee39-131">**Environment type:** - Demo</span></span>


| <span data-ttu-id="fee39-132">環境名</span><span class="sxs-lookup"><span data-stu-id="fee39-132">Environment name</span></span>       | <span data-ttu-id="fee39-133">既定の構成で環境を配置するコアの数</span><span class="sxs-lookup"><span data-stu-id="fee39-133">Number of cores to deploy the environment in its default configuration</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="fee39-134">AX 2012 R3 デモ</span><span class="sxs-lookup"><span data-stu-id="fee39-134">AX 2012 R3 demo</span></span>        | <span data-ttu-id="fee39-135">8 コア</span><span class="sxs-lookup"><span data-stu-id="fee39-135">8 cores</span></span>                                                                |
| <span data-ttu-id="fee39-136">AX 2012 R3 CU8 デモ</span><span class="sxs-lookup"><span data-stu-id="fee39-136">AX 2012 R3 CU8 demo</span></span>    | <span data-ttu-id="fee39-137">8 コア</span><span class="sxs-lookup"><span data-stu-id="fee39-137">8 cores</span></span>                                                                |
| <span data-ttu-id="fee39-138">Retail Essentials デモ</span><span class="sxs-lookup"><span data-stu-id="fee39-138">Retail essentials demo</span></span> | <span data-ttu-id="fee39-139">8 コア</span><span class="sxs-lookup"><span data-stu-id="fee39-139">8 cores</span></span>                                                                |


<span data-ttu-id="fee39-140">**環境タイプ:** - 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="fee39-140">**Environment type:** - Dev/test</span></span>


| <span data-ttu-id="fee39-141">環境名</span><span class="sxs-lookup"><span data-stu-id="fee39-141">Environment name</span></span>                   | <span data-ttu-id="fee39-142">既定の構成で環境を配置するコアの数</span><span class="sxs-lookup"><span data-stu-id="fee39-142">Number of cores to deploy the environment in its default configuration</span></span> |
|------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="fee39-143">開発</span><span class="sxs-lookup"><span data-stu-id="fee39-143">Development</span></span>                        | <span data-ttu-id="fee39-144">9 コア</span><span class="sxs-lookup"><span data-stu-id="fee39-144">9 cores</span></span>                                                                |
| <span data-ttu-id="fee39-145">共有 SQL Server による開発</span><span class="sxs-lookup"><span data-stu-id="fee39-145">Development with shared SQL Server</span></span> | <span data-ttu-id="fee39-146">14 コア</span><span class="sxs-lookup"><span data-stu-id="fee39-146">14 cores</span></span>                                                               |
| <span data-ttu-id="fee39-147">テスト</span><span class="sxs-lookup"><span data-stu-id="fee39-147">Test</span></span>                               | <span data-ttu-id="fee39-148">13 コア</span><span class="sxs-lookup"><span data-stu-id="fee39-148">13 cores</span></span>                                                               |
| <span data-ttu-id="fee39-149">Retail Essentials 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="fee39-149">Retail essentials dev/test</span></span>         | <span data-ttu-id="fee39-150">4 コア</span><span class="sxs-lookup"><span data-stu-id="fee39-150">4 cores</span></span>                                                                |
| <span data-ttu-id="fee39-151">Retail E-commerce 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="fee39-151">Retail e-commerce dev/test</span></span>         | <span data-ttu-id="fee39-152">4 コア</span><span class="sxs-lookup"><span data-stu-id="fee39-152">4 cores</span></span>                                                                |
| <span data-ttu-id="fee39-153">Retail Mobility 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="fee39-153">Retail mobility dev/test</span></span>           | <span data-ttu-id="fee39-154">4 コア</span><span class="sxs-lookup"><span data-stu-id="fee39-154">4 cores</span></span>                                                                |


<span data-ttu-id="fee39-155">**環境タイプ:** - 高可用性</span><span class="sxs-lookup"><span data-stu-id="fee39-155">**Environment type:** - High availability</span></span>


| <span data-ttu-id="fee39-156">環境名</span><span class="sxs-lookup"><span data-stu-id="fee39-156">Environment name</span></span>              | <span data-ttu-id="fee39-157">既定の構成で環境を配置するコアの数</span><span class="sxs-lookup"><span data-stu-id="fee39-157">Number of cores to deploy the environment in its default configuration</span></span> |
|-------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="fee39-158">高可用性環境</span><span class="sxs-lookup"><span data-stu-id="fee39-158">High availability environment</span></span> | <span data-ttu-id="fee39-159">45 コア</span><span class="sxs-lookup"><span data-stu-id="fee39-159">45 cores</span></span>                                                               |


<span data-ttu-id="fee39-160">Azure のサブスクリプションを既に持っている場合、次に注意します。</span><span class="sxs-lookup"><span data-stu-id="fee39-160">If you already have an Azure subscription, note the following:</span></span>

-   <span data-ttu-id="fee39-161">**定期売買のサイズを表示する:** Azure 管理ポータルで、定期売買のサイズを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="fee39-161">**To view the size of your subscription:** You can view the size of your subscription in the Azure management portal.</span></span> <span data-ttu-id="fee39-162">これを行うには、[[Azure管理ポータル](https://manage.windowsazure.com/)] にログオンし、**設定**&gt;**使用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fee39-162">To do so, log on to the [Azure management portal](https://manage.windowsazure.com/), and then click **Settings** &gt; **Usage**.</span></span>
-   <span data-ttu-id="fee39-163">**定期購読のサイズを増やす:** 定期売買のサイズを増やすには、Azure サポート チームにてサポート チケットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-163">**To increase the size of your subscription:** To increase the size of your subscription, you’ll need to create a support ticket with the Azure support team.</span></span> <span data-ttu-id="fee39-164">これを行うには、[[Azure サポート オプション](http://azure.microsoft.com/en-us/support/options/)] ページに移動し、**サポートを受ける** をクリックしてサポート チケットを作成します。</span><span class="sxs-lookup"><span data-stu-id="fee39-164">To do so, go to the [Azure support options](http://azure.microsoft.com/en-us/support/options/) page, and then click **Get Support** to create the support ticket.</span></span> <span data-ttu-id="fee39-165">サポート チケットを作成するとき、チケットが課金サポートに対応していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fee39-165">When creating the support ticket, be sure to indicate that the ticket is for billing support.</span></span>

> [!NOTE]
> <span data-ttu-id="fee39-166">クラウド ソリューション プロバイダー (CSP) プログラムは、Azure Resource Manager (ARM) 要件のため Lifecycle Services によって現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="fee39-166">The Cloud Solution Provider (CSP) program is currently not supported with Lifecycle Services due to the Azure Resource Manager (ARM) requirement.</span></span>

## <a name="purchase-and-azure-support-plan"></a><span data-ttu-id="fee39-167">発注書および Azure サポート計画</span><span class="sxs-lookup"><span data-stu-id="fee39-167">Purchase and Azure support plan</span></span>
<span data-ttu-id="fee39-168">Azure サポート計画では Azure の技術および課金サポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="fee39-168">Azure support plans provide technical and billing support for Azure.</span></span> <span data-ttu-id="fee39-169">Azure サポート プランは、Azure 展開のサポーの適切なレベルを選択できる柔軟なサポート オプションを提供しています。</span><span class="sxs-lookup"><span data-stu-id="fee39-169">The Azure support plans offer flexible support options that will allow you to select the right level of support for your Azure deployment.</span></span> <span data-ttu-id="fee39-170">サポート オプションには、Azure サブスクリプションに含まれているサポート サービスから、無料のサポート サービスまでさまざまです。</span><span class="sxs-lookup"><span data-stu-id="fee39-170">The support options range from support services included with your Azure subscription at no charge to premier support services.</span></span> <span data-ttu-id="fee39-171">利用可能なサポート プランについて学び、プランを購入するには、[[Azure サポート計画](http://www.windowsazure.com/en-us/support/plans/)] ページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="fee39-171">To learn about the available support plans and to purchase a plan, see the [Azure support plans](http://www.windowsazure.com/en-us/support/plans/) page.</span></span>

## <a name="become-familiar-with-the-azure-management-portal"></a><span data-ttu-id="fee39-172">Azure 管理ポータルを使いこなせるようになります</span><span class="sxs-lookup"><span data-stu-id="fee39-172">Become familiar with the Azure management portal</span></span>
<span data-ttu-id="fee39-173">Azure 管理ポータルは、開発者および IT プロフェッショナルに、その Azure コンポーネントをプロビジョニング、構成、監視、および管理する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="fee39-173">The Azure management portal provides developers and IT professionals the ability to provision, configure, monitor, and manage their Azure components.</span></span> <span data-ttu-id="fee39-174">今後使用するために、管理ポータルについてよく理解しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="fee39-174">It’s important to become familiar with the management portal because you’ll use it to:</span></span>

-   <span data-ttu-id="fee39-175">管理証明書をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="fee39-175">Upload a management certificate.</span></span> <span data-ttu-id="fee39-176">(管理証明書を使用すると、Lifecycle Services はユーザーに代わって Azure に AX 2012 R3 環境を配置できます。)</span><span class="sxs-lookup"><span data-stu-id="fee39-176">(The management certificate enables Lifecycle Services to deploy AX 2012 R3 environments on Azure on your behalf.)</span></span>
-   <span data-ttu-id="fee39-177">仮想マシンに接続します。</span><span class="sxs-lookup"><span data-stu-id="fee39-177">Connect to virtual machines.</span></span>
-   <span data-ttu-id="fee39-178">AX 2012 R3 環境の正常性および状態を監視します。</span><span class="sxs-lookup"><span data-stu-id="fee39-178">Monitor the health and status of your AX 2012 R3 environment.</span></span>

<span data-ttu-id="fee39-179">Azure サブスクリプションを購入した後、[ここ。](https://manage.windowsazure.com/?whr=live.com) をクリックして管理ポータルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="fee39-179">After you purchase an Azure subscription, you can access the management portal by clicking [here.](https://manage.windowsazure.com/?whr=live.com)</span></span> <span data-ttu-id="fee39-180">次の図は、管理ポータルを示しています。</span><span class="sxs-lookup"><span data-stu-id="fee39-180">The following image shows the management portal.</span></span> <span data-ttu-id="fee39-181">[![PlanYouAXR3DeploymentonAzure1](./media/planyouaxr3deploymentonazure1.jpg)](./media/planyouaxr3deploymentonazure1.jpg)</span><span class="sxs-lookup"><span data-stu-id="fee39-181">[![PlanYouAXR3DeploymentonAzure1](./media/planyouaxr3deploymentonazure1.jpg)](./media/planyouaxr3deploymentonazure1.jpg)</span></span>  

## <a name="become-familiar-with-the-azure-vm-agent"></a><span data-ttu-id="fee39-182">Azure VM エージェントを使いこなせるようになります</span><span class="sxs-lookup"><span data-stu-id="fee39-182">Become familiar with the Azure VM agent</span></span>
<span data-ttu-id="fee39-183">Azure VM エージェントは、Lifecycle Services を通じて展開されたすべての VM で自動的に配置されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-183">The Azure VM Agent is now automatically deployed with every VM deployed via Lifecycle Services.</span></span> <span data-ttu-id="fee39-184">Azure VM エージェントは、Azure 仮想マシン拡張 (VM 拡張) インストール、コンフィギュレーション、管理、実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-184">The Azure VM Agent is used to install, configure, manage and run Azure Virtual Machine Extensions (VM Extensions).</span></span> <span data-ttu-id="fee39-185">VM 拡張機能は、VM を監視および管理するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="fee39-185">VM extensions can help you monitor and manage your VMs.</span></span>

## <a name="consider-cloud-services-resource-requirements"></a><span data-ttu-id="fee39-186">クラウド サービスのリソース要件を検討する</span><span class="sxs-lookup"><span data-stu-id="fee39-186">Consider Cloud Services resource requirements</span></span>
<span data-ttu-id="fee39-187">トポロジが配置されると、配置システムは選択された仮想マシン (VM) の SKU を検査します。</span><span class="sxs-lookup"><span data-stu-id="fee39-187">When a topology is deployed, the deployment system will inspect the virtual machine (VM) SKUs that were selected.</span></span> <span data-ttu-id="fee39-188">Azure がこれらの VM を VM が使用可能である適切なクラスターに配置していることを確認するために、VM SKU の各レベルに独自の Azure クラウド サービスが必要です。</span><span class="sxs-lookup"><span data-stu-id="fee39-188">In order to ensure that Azure deploys these VMs to the proper clusters where the VMs are available, each level of VM SKU must have its own Azure Cloud Service.</span></span> <span data-ttu-id="fee39-189">VM SKU の内訳は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fee39-189">The VM SKU breakdown is as follows:</span></span>

|         |                                 |
|---------|---------------------------------|
| <span data-ttu-id="fee39-190">**最小在庫管理単位**</span><span class="sxs-lookup"><span data-stu-id="fee39-190">**SKU**</span></span> | <span data-ttu-id="fee39-191">**サイズ**</span><span class="sxs-lookup"><span data-stu-id="fee39-191">**Size**</span></span>                        |
| <span data-ttu-id="fee39-192">A</span><span class="sxs-lookup"><span data-stu-id="fee39-192">A</span></span>       | <span data-ttu-id="fee39-193">標準 A の \[A0-A4\]</span><span class="sxs-lookup"><span data-stu-id="fee39-193">Standard A’s \[A0-A4\]</span></span>          |
| <span data-ttu-id="fee39-194">午前</span><span class="sxs-lookup"><span data-stu-id="fee39-194">AM</span></span>      | <span data-ttu-id="fee39-195">標準 A の \[A5-A7\]</span><span class="sxs-lookup"><span data-stu-id="fee39-195">Standard A's \[A5-A7\]</span></span>          |
| <span data-ttu-id="fee39-196">AL</span><span class="sxs-lookup"><span data-stu-id="fee39-196">AL</span></span>      | <span data-ttu-id="fee39-197">標準 A の (大) \[A8-A11\]</span><span class="sxs-lookup"><span data-stu-id="fee39-197">Standard A’s (large) \[A8-A11\]</span></span> |
| <span data-ttu-id="fee39-198">D</span><span class="sxs-lookup"><span data-stu-id="fee39-198">D</span></span>       | <span data-ttu-id="fee39-199">標準 D の\[すべての D シリーズ\]</span><span class="sxs-lookup"><span data-stu-id="fee39-199">Standard D’s \[all D series\]</span></span>   |
| <span data-ttu-id="fee39-200">DS</span><span class="sxs-lookup"><span data-stu-id="fee39-200">DS</span></span>      | <span data-ttu-id="fee39-201">標準 DS の\[すべての DS シリーズ\]</span><span class="sxs-lookup"><span data-stu-id="fee39-201">Standard DS’s \[all DS series\]</span></span> |
| <span data-ttu-id="fee39-202">G</span><span class="sxs-lookup"><span data-stu-id="fee39-202">G</span></span>       | <span data-ttu-id="fee39-203">標準 G の\[すべての G シリーズ\]</span><span class="sxs-lookup"><span data-stu-id="fee39-203">Standard G’s \[all G series\]</span></span>   |

<span data-ttu-id="fee39-204">Version-Topology-EnvironmentName-SKU-GUID という名前付けスキームを含むクラウド サービスが作成されます。必要に応じて、配置のためのクラウド サービス リソース要件を検討し、Azure サポートから Azure サブスクリプションの追加クラウド サービス能力を要求してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-204">A Cloud Service will be created with the following naming scheme: Version-Topology-EnvironmentName-SKU-GUID Please consider the Cloud Services resource requirements for your deployments and request additional Cloud Services capacity in your Azure Subscription from Azure Support if necessary.</span></span>

## <a name="plan-for-storage-accounts"></a><span data-ttu-id="fee39-205">ストレージ アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="fee39-205">Plan for storage accounts</span></span>
<span data-ttu-id="fee39-206">Lifecycle Services で作成された各プロジェクトについては、1 つまたは複数の個別のストレージ アカウントが Azure 定期売買で作成されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-206">For each project created in Lifecycle Services, one or more distinct storage accounts will be created in the Azure subscription.</span></span> <span data-ttu-id="fee39-207">ストレージ アカウントは、プロジェクトを Azure サブスクリプションに接続すると作成されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-207">A storage account is created when you connect your project to your Azure subscription.</span></span> <span data-ttu-id="fee39-208">このストレージ アカウントは、ローカル冗長ストレージ (LRS) アカウントであり、展開に必要なスクリプトと VHD を格納するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-208">This storage account is a Locally Redundant Storage (LRS) account, and is used to house scripts and VHDs which are required for deployments.</span></span> <span data-ttu-id="fee39-209">最初の Premium ストレージ有効トポロジがプロジェクトから配置されると、各プロジェクトが作成され Premium ストレージ アカウントが追加されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-209">An additional Premium storage account is created for each project when the first Premium storage-enabled topology is deployed from the project.</span></span> <span data-ttu-id="fee39-210">ストレージ アカウントは、配置が同じ Azure サブスクリプションに行われる場合でも、Lifecycle Services プロジェクト間で共有されません。</span><span class="sxs-lookup"><span data-stu-id="fee39-210">Storage accounts are not shared across Lifecycle Services projects, even if the deployments are to the same Azure subscription.</span></span> <span data-ttu-id="fee39-211">Premium ストレージ アカウントが作成されると、それもまた LRS として作成されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-211">When a Premium storage account is created, it too is created as LRS.</span></span> <span data-ttu-id="fee39-212">ストレージの詳細については、[ここ](http://azure.microsoft.com/en-us/pricing/details/storage) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="fee39-212">For more information about storage, click [here](http://azure.microsoft.com/en-us/pricing/details/storage).</span></span> <span data-ttu-id="fee39-213">同じ Lifecycle Services (LCS) プロジェクトと Azure コネクタに展開されるトポロジと環境の数を検討します。</span><span class="sxs-lookup"><span data-stu-id="fee39-213">Consider which topologies and the number of environments that will be deployed into the same Lifecycle Services (LCS) project and Azure Connector.</span></span> <span data-ttu-id="fee39-214">Premium ストレージ アカウントとは別に、既定では、LCS プロジェクトおよび Azure コネクタごとにストレージ アカウントが 1 つ存在します。</span><span class="sxs-lookup"><span data-stu-id="fee39-214">Premium storage account aside, by default there is 1 storage account for each LCS project and Azure Connector.</span></span> <span data-ttu-id="fee39-215">Azure Storage には[限度](https://azure.microsoft.com/en-us/documentation/articles/azure-subscription-service-limits/#storage-limits)があるので注意してください。具体的には、標準ストレージ アカウントあたり 20,000 IOPS (秒単位の入力/出力オペレーション) です。</span><span class="sxs-lookup"><span data-stu-id="fee39-215">Be aware that Azure storage has [limits](https://azure.microsoft.com/en-us/documentation/articles/azure-subscription-service-limits/#storage-limits), specifically 20,000 IOPS (input/output operations per second) per standard storage account.</span></span> <span data-ttu-id="fee39-216">VHD あたり 500 IOPS と組み合わせると、調整が発生する前に約 40 個の***利用効率が高い*** VHDが残されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-216">Combined with 500 IOPS per VHD, that leaves roughly 40 ***highly utilized*** VHDs before throttling occurs.</span></span> <span data-ttu-id="fee39-217">これを軽減するには、複数の Azure コネクタや複数の LCS プロジェクトを活用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fee39-217">To mitigate this, we recommend that you leverage multiple Azure Connectors and/or multiple LCS projects.</span></span> <span data-ttu-id="fee39-218">たとえば、1 つの LCS プロジェクトで製造環境を、別で開発/テスト環境を検討します。</span><span class="sxs-lookup"><span data-stu-id="fee39-218">For example, consider having production environments in one LCS project, and Dev/Test environments in another.</span></span> 

> [!NOTE]
> <span data-ttu-id="fee39-219">インストール VHD など、LCS が配置するすべての VHD が高度に使用されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="fee39-219">Not all VHDs that LCS deploys will be highly utilized, such as the installation VHD.</span></span>

## <a name="plan-your-sql-server-configuration"></a><span data-ttu-id="fee39-220">SQL Server 構成の計画</span><span class="sxs-lookup"><span data-stu-id="fee39-220">Plan your SQL Server configuration</span></span>
<span data-ttu-id="fee39-221">Azure Premium Storage は、Azure 仮想マシン (VM) 上で実行される I/O 集約型ワークロードに対して高パフォーマンス、待機時間が短いディスク サポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="fee39-221">Azure Premium Storage delivers high-performance, low-latency disk support for I/O intensive workloads running on Azure virtual machines (VMs).</span></span> <span data-ttu-id="fee39-222">Premium Storage では、アプリケーションは VM ごとに 32 TB までのストレージを持つことができ、VM ごとに 50,000 IOPS を達成し、読み取り操作での待機時間は非常に短くなります。</span><span class="sxs-lookup"><span data-stu-id="fee39-222">With Premium Storage, your applications can have up to 32 TB of storage per VM, achieve 50,000 IOPS per VM, and have extremely low latencies for read operations.</span></span> <span data-ttu-id="fee39-223">Premium Storage は、生産能力で使用される AX 2012 R3 配置に必要です。</span><span class="sxs-lookup"><span data-stu-id="fee39-223">Premium Storage is required for AX 2012 R3 deployments that will be used in a production capacity.</span></span> <span data-ttu-id="fee39-224">Azure DS シリーズ VM が選択されている場合、高可用性配置では Premium Storage が既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="fee39-224">Premium Storage is enabled by default for High Availability deployments when Azure DS-series VMs are selected.</span></span> <span data-ttu-id="fee39-225">Premium Storage は、現時点では DS シリーズ VM 上でのみ提供されています。</span><span class="sxs-lookup"><span data-stu-id="fee39-225">Premium Storage is only offered on DS-series VMs at this time.</span></span> <span data-ttu-id="fee39-226">他のすべての記憶域ニーズに非 Premium ストレージが使用されているとき、SQL Server AlwaysOn データベース サーバーだけで Premium Storage が有効になります。</span><span class="sxs-lookup"><span data-stu-id="fee39-226">Premium Storage is enabled exclusively for the SQL Server AlwaysOn database servers, while non-Premium storage is used for all other storage needs.</span></span> <span data-ttu-id="fee39-227">SQL Server AlwaysOn 可用性セットが作成されると、Lifecycle Services は、選択された DS シリーズ VM でサポートされているすべてのディスク スロットに対してディスクをアタッチします。</span><span class="sxs-lookup"><span data-stu-id="fee39-227">When a SQL Server AlwaysOn availability set is created, Lifecycle Services will attach a disk for every disk slot supported by the DS-series VM selected.</span></span> <span data-ttu-id="fee39-228">VM ディスク能力の詳細については、[ここ](https://msdn.microsoft.com/en-us/library/azure/dn197896.aspx) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fee39-228">For more information about VM disk capacity, click [here](https://msdn.microsoft.com/en-us/library/azure/dn197896.aspx).</span></span> <span data-ttu-id="fee39-229">異なる VM サイズには、スループットと IOPS の最大値が変化します。</span><span class="sxs-lookup"><span data-stu-id="fee39-229">Different VM sizes will come with varying maximums for throughput and IOPS.</span></span> <span data-ttu-id="fee39-230">結果として、 SQL Server の構成を計画しているときは、ビジネスに最も効率的でコスト効果の良いソリューションを展開するために、これらの制限に精通してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-230">As a result, when you are planning your SQL Server configuration, please be familiar with these limitations to ensure that you are deploying the most efficient and cost effective solution for your business.</span></span> <span data-ttu-id="fee39-231">[Premium Storage: Azure 仮想マシン ワークロード向け高性能ストレージ](https://azure.microsoft.com/en-us/documentation/articles/storage-premium-storage-preview-portal/)に関するページ (特に、**Premium Storage の使用時の調整**に関するセッション) にあるガイドラインに従ってください。</span><span class="sxs-lookup"><span data-stu-id="fee39-231">Please follow the guidance found in [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://azure.microsoft.com/en-us/documentation/articles/storage-premium-storage-preview-portal/), particularly the section, **Throttling when using Premium Storage**.</span></span> <span data-ttu-id="fee39-232">SQL Server AlwaysOn 可用性セットは、Lifecycle Services を通じて自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-232">The SQL Server AlwaysOn availability set is created automatically through Lifecycle Services.</span></span> <span data-ttu-id="fee39-233">生産システムで使用するための高可用性トポロジを配置する前に、データおよびパフォーマンスのニーズを考慮することが重要です。</span><span class="sxs-lookup"><span data-stu-id="fee39-233">It is important to consider your data and performance needs before deploying a High Availability topology for use with a production system.</span></span> <span data-ttu-id="fee39-234">Azure Premium Storage については、[こちら](http://azure.microsoft.com/en-us/documentation/articles/storage-premium-storage-preview-portal/)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="fee39-234">Please refer to Azure Premium Storage information [here](http://azure.microsoft.com/en-us/documentation/articles/storage-premium-storage-preview-portal/).</span></span> <span data-ttu-id="fee39-235">Premium Storage で配置を計画すると、高可用性トポロジには、原価とパフォーマンスの目標を達成するためのコンフィギュレーション オプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-235">Once you have planned your deployment with Premium Storage, the High Availability topology provides configuration options to help you achieve your cost and performance objectives.</span></span> <span data-ttu-id="fee39-236">高可用性のトポロジの詳細設定では、次の SQL Server 構成オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-236">Under Advanced Settings for the High Availability topology, the following SQL Server configuration options appear:</span></span>

-   <span data-ttu-id="fee39-237">**SQL Server イメージ コンフィギュレーションのカスタマイズ** - このオプションを使用すると、カスタム SQL Server Enterprise イメージまたは Azure Gallery SQL Server Enterprise イメージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fee39-237">**Customize the SQL Server image configuration** – This option allows the use of a custom SQL Server Enterprise image or an Azure Gallery SQL Server Enterprise image.</span></span>
    -   <span data-ttu-id="fee39-238">カスタム SQL Server イメージ (既定) - このイメージには、SQL Server Enterprise 2014の試用版が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fee39-238">Custom SQL Server image (default) – This image contains a trial edition of SQL Server Enterprise 2014.</span></span> <span data-ttu-id="fee39-239">評価版ライセンスは 3〜6 か月間有効です。</span><span class="sxs-lookup"><span data-stu-id="fee39-239">The trial license is enabled for 3-6 months.</span></span> <span data-ttu-id="fee39-240">既存の EA/etc. ライセンスを使用する場合は、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="fee39-240">Use this option if you want to use an existing EA/etc. license.</span></span>
    -   <span data-ttu-id="fee39-241">ギャラリー SQL Server イメージ – このイメージには SQL Server Enterprise 2014 が含まれており、消費に基づく Azure 価格決定を使用します。</span><span class="sxs-lookup"><span data-stu-id="fee39-241">Gallery SQL Server image – This image contains SQL Server Enterprise 2014 and uses consumption-based Azure pricing.</span></span> <span data-ttu-id="fee39-242">詳細については、[Azure 仮想マシンの価格決定](https://azure.microsoft.com/en-us/pricing/details/virtual-machines/#sql-server)ページと [Azure 仮想マシンの SQL Server](https://msdn.microsoft.com/library/azure/jj823132.aspx) で確認できます。</span><span class="sxs-lookup"><span data-stu-id="fee39-242">More information can be found on the [Azure Virtual Machines Pricing](https://azure.microsoft.com/en-us/pricing/details/virtual-machines/#sql-server) page and the [SQL Server in Azure Virtual Machines](https://msdn.microsoft.com/library/azure/jj823132.aspx)</span></span>
-   <span data-ttu-id="fee39-243">**SQL Server のストレージ領域コンフィギュレーションのカスタマイズ** - SQL Server VM に関連付けられるディスクの数とサイズを指定できます。</span><span class="sxs-lookup"><span data-stu-id="fee39-243">**Customize the SQL Server storage space configuration** – You can specify the number and size of the disks that will be attached to the SQL Server VMs.</span></span>

<span data-ttu-id="fee39-244">SQL Server 内でストレージ領域の作成に使用する必要があるディスクの数を指定する場合は、次の点に留意してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-244">Keep the following points in mind when specifying the number of disks that should be used to create the storage space within SQL Server:</span></span>

-   <span data-ttu-id="fee39-245">データベース サーバーのために選択されている VM サイズで、その VM SKU でサポートされるディスクの数が決まります。</span><span class="sxs-lookup"><span data-stu-id="fee39-245">The VM size that is selected for the database server dictates how many disks are supported by that VM SKU.</span></span> <span data-ttu-id="fee39-246">各 VM でサポートされているディスクの数に関する情報は、[ここ](https://msdn.microsoft.com/en-us/library/azure/dn197896.aspx)で確認できます。</span><span class="sxs-lookup"><span data-stu-id="fee39-246">Information about the number of disks that are supported by each VM can be found [here](https://msdn.microsoft.com/en-us/library/azure/dn197896.aspx).</span></span>
-   <span data-ttu-id="fee39-247">VM で使用可能なディスク スロットの 1 つは、Lifecycle Services 配置サービスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-247">One of the available disk slots on the VM will be used by the Lifecycle Services deployment service.</span></span> <span data-ttu-id="fee39-248">これは、VM の最大ディスク数 (マイナス1) が、使用可能なスロットを満たすことを意味します。</span><span class="sxs-lookup"><span data-stu-id="fee39-248">This means the VM’s maximum number of disks—minus 1—equals the available slots to fill.</span></span>
-   <span data-ttu-id="fee39-249">この設定を空白のままにすると、配置サービスによって VM でサポートされている最大までディスクを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="fee39-249">Leaving this setting blank will allow the deployment service to attach disks up to the maximum supported by the VM.</span></span> <span data-ttu-id="fee39-250">最大のディスクが使用される運用配置の場合にお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fee39-250">It is recommended for production deployments that the maximum disks be used.</span></span>

<span data-ttu-id="fee39-251">VM に関連付けられている各ディスクのサイズ (GB 単位) を指定する場合、次の点に留意してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-251">Keep the following points in mind when specifying the size (in GB) of each disk attached to the VM:</span></span>

-   <span data-ttu-id="fee39-252">100 GB – 1024 GB 値を許可します。</span><span class="sxs-lookup"><span data-stu-id="fee39-252">Allowed values are 100 GB – 1024 GB.</span></span>
-   <span data-ttu-id="fee39-253">既定値は 128 GB です。</span><span class="sxs-lookup"><span data-stu-id="fee39-253">Default is 128 GB.</span></span>
-   <span data-ttu-id="fee39-254">使用されるディスクのサイズは、使用される Premium Storage 階層を決定します。</span><span class="sxs-lookup"><span data-stu-id="fee39-254">The size of the disk used dictates the Premium Storage tier used.</span></span>
-   <span data-ttu-id="fee39-255">Premium Storage 層は、原価、ディスクあたりの IPOPS、および展開されるシステムのスループットを示しています。</span><span class="sxs-lookup"><span data-stu-id="fee39-255">The Premium Storage tier dictates cost, IOPS per disk, and throughput of the system being deployed.</span></span> <span data-ttu-id="fee39-256">詳細については、[ここ](http://azure.microsoft.com/en-us/pricing/details/storage/) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="fee39-256">For more information, click [here](http://azure.microsoft.com/en-us/pricing/details/storage/).</span></span>
-   <span data-ttu-id="fee39-257">すべてのディスクは 64k クラスター サイズにフォーマットします。</span><span class="sxs-lookup"><span data-stu-id="fee39-257">All disks are formatted to 64k cluster size.</span></span> <span data-ttu-id="fee39-258">これにより、パフォーマンスが最大 20％ 向上します。</span><span class="sxs-lookup"><span data-stu-id="fee39-258">This results in up to a 20% increase in performance.</span></span> <span data-ttu-id="fee39-259">詳細については、[ここ](http://tk.azurewebsites.net/2012/08/) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="fee39-259">For more information, click [here](http://tk.azurewebsites.net/2012/08/).</span></span>

<span data-ttu-id="fee39-260">TempDB とログは、パフォーマンスの向上のために記憶域上に配置されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-260">TempDB and logs are deployed onto storage spaces as to benefit from the performance gains.</span></span> <span data-ttu-id="fee39-261">そのストレージ領域にコンフィギュレーションされているディスクの数に対して、1 つの仮想ディスクが作成されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-261">One virtual disk is created over the number of disks configured for the storage space.</span></span> <span data-ttu-id="fee39-262">次に、仮想ディスクは次のようにパーティション化されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-262">The virtual disk is then partitioned as follows:</span></span>

-   <span data-ttu-id="fee39-263">SQL データ = プールの合計サイズの 1/2</span><span class="sxs-lookup"><span data-stu-id="fee39-263">SQL data = 1/2 of the total size of pool</span></span>
-   <span data-ttu-id="fee39-264">SQL ログ = 合計サイズの 1/4</span><span class="sxs-lookup"><span data-stu-id="fee39-264">SQL logs = 1/4 of the total size</span></span>
-   <span data-ttu-id="fee39-265">SQL Temp db = 合計サイズの 1/8</span><span class="sxs-lookup"><span data-stu-id="fee39-265">SQL Temp db = 1/8 of the total size</span></span>
-   <span data-ttu-id="fee39-266">SQL バックアップ = 合計サイズの残り 1/8</span><span class="sxs-lookup"><span data-stu-id="fee39-266">SQL backup = remaining 1/8 of the total size</span></span>

<span data-ttu-id="fee39-267">他の考慮事項を念頭に置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-267">Other considerations to keep in mind:</span></span>

-   <span data-ttu-id="fee39-268">配置を計画するときは、対象とする Azure 領域で Premium Storage を使用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fee39-268">When planning your deployment, ensure that Premium Storage is available in the Azure region you are targeting.</span></span> <span data-ttu-id="fee39-269">詳細については、[ここ](http://azure.microsoft.com/en-us/services/preview/) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="fee39-269">For more information, click [here](http://azure.microsoft.com/en-us/services/preview/).</span></span>
-   <span data-ttu-id="fee39-270">会社のネットワークと Azure の間で VPN/Express ルート接続 (または計画) がある場合、Premium ストレージ アカウントをサポートしている Azure 地域でこれが行われていることが確認します。</span><span class="sxs-lookup"><span data-stu-id="fee39-270">If you have a VPN/Express Route connection (or plan to) between your corporate network and Azure, please ensure this is done for an Azure region that supports Premium Storage.</span></span>
-   <span data-ttu-id="fee39-271">使用に関する制限について理解するためには [Azure Premium Storage ドキュメント](http://azure.microsoft.com/en-us/documentation/services/storage/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-271">Consult the [Azure Premium Storage documentation](http://azure.microsoft.com/en-us/documentation/services/storage/) to understand limitations of use.</span></span>
-   <span data-ttu-id="fee39-272">可用性トポロジーで非 Premium ストレージ VM がデプロイされている場合は、上記のすべての SQL Server のコンフィギュレーションを適用できますが、Premium ストレージのメリットは適用されません。</span><span class="sxs-lookup"><span data-stu-id="fee39-272">If non-Premium Storage VMs are deployed with the High Availability topologies, all of the above SQL Server configuration settings are applicable; however, Premium Storage benefits will not apply.</span></span>
-   <span data-ttu-id="fee39-273">配置ために Lifecycle Services プロジェクトを設定するとき、Premium Storage をサポートする地域を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-273">When setting up your Lifecycle Services project for deployment, you must select a region that supports Premium Storage.</span></span>

<span data-ttu-id="fee39-274">展開サービスにより実装される SQL Server ベスト プラクティスには、SQL Server チームにより推奨されるベスト プラクティスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fee39-274">SQL Server best practices implemented by the deployment service include those recommended by the SQL Server team.</span></span> <span data-ttu-id="fee39-275">詳細については、[ここ](http://blogs.technet.com/b/dataplatforminsider/archive/2014/09/12/new-vm-images-optimized-for-transactional-and-dw-workloads-in-azure-vm-gallery.aspx) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="fee39-275">For more information, click [here](http://blogs.technet.com/b/dataplatforminsider/archive/2014/09/12/new-vm-images-optimized-for-transactional-and-dw-workloads-in-azure-vm-gallery.aspx).</span></span> <span data-ttu-id="fee39-276">さらに、次の項目が実行されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-276">In addition, the following items are done:</span></span>

-   <span data-ttu-id="fee39-277">複数の一時ファイル (CPU コアごとに 1 つ)。</span><span class="sxs-lookup"><span data-stu-id="fee39-277">Multiple temp files (one per CPU core).</span></span>
-   <span data-ttu-id="fee39-278">SQL Server の最大メモリを使用可能なコンピューター RAM の 90% に設定します。</span><span class="sxs-lookup"><span data-stu-id="fee39-278">Set max memory for SQL Server to 90% of available machine RAM.</span></span>
-   <span data-ttu-id="fee39-279">並列処理の最大限度を設定します。</span><span class="sxs-lookup"><span data-stu-id="fee39-279">Set max degree of parallelism.</span></span>
-   <span data-ttu-id="fee39-280">トレース フラグの有効  -T1204、 -T1222。</span><span class="sxs-lookup"><span data-stu-id="fee39-280">Enabled trace flags  -T1204, -T1222.</span></span>

## <a name="estimate-costs-and-understand-the-azure-billing-process"></a><span data-ttu-id="fee39-281">減価を見積もり、Azure 請求プロセスに同意</span><span class="sxs-lookup"><span data-stu-id="fee39-281">Estimate costs and understand the Azure billing process</span></span>
<span data-ttu-id="fee39-282">Azure での AX 2012 R3 の展開コストを見積もるには、[[Azure 価格計算ツール](http://azure.microsoft.com/en-us/pricing/calculator/)] を使用します。</span><span class="sxs-lookup"><span data-stu-id="fee39-282">To help estimate the cost of your AX 2012 R3 deployment on Azure, use the [Azure pricing calculator](http://azure.microsoft.com/en-us/pricing/calculator/).</span></span> <span data-ttu-id="fee39-283">Azure に AX 2012 R3 を配置する前に、Azure 請求プロセスについて理解することも重要です。</span><span class="sxs-lookup"><span data-stu-id="fee39-283">It’s also important to understand the Azure billing process before you deploy AX 2012 R3 on Azure.</span></span> <span data-ttu-id="fee39-284">サンプル請求書、および現在の請求期間に対する毎日の使用データをダウンロードする方法に関する情報にリンクする Azure 請求プロセスの概要については、[請求書を理解する](http://azure.microsoft.com/en-us/support/understand-your-bill/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-284">For an overview of the Azure billing process, links to sample invoices, and information about how to download daily usage data for the current billing period, see [Understand your bill](http://azure.microsoft.com/en-us/support/understand-your-bill/).</span></span> <span data-ttu-id="fee39-285">**注記:** 使用されていないときに Azure 上に配置されている AX 2012 R3 環境をシャット ダウンすることができることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-285">**Note: **Keep in mind, you can shut down an AX 2012 R3 environment that has been deployed on Azure when it’s not in use.</span></span> <span data-ttu-id="fee39-286">たとえば、コスト削減のため週末に環境をシャット ダウンする場合があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-286">For example, you may want to shut down an environment on the weekends to reduce costs.</span></span> <span data-ttu-id="fee39-287">環境をシャット ダウンすると、その環境はまだ存在します。ただし、その環境内の仮想マシンはシャット ダウンされます。</span><span class="sxs-lookup"><span data-stu-id="fee39-287">When you shut down an environment, the environment still exists; however, the virtual machines in the environment are shut down.</span></span> <span data-ttu-id="fee39-288">仮想マシンが実行されていないときは、それに対して課金されません。</span><span class="sxs-lookup"><span data-stu-id="fee39-288">You won’t be charged for the virtual machines when they’re not running.</span></span> <span data-ttu-id="fee39-289">詳細については、「環境をシャット ダウンする方法とは」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-289">For more information, see “How do I shut down an environment?”</span></span> <span data-ttu-id="fee39-290">[Azure 上の Microsoft Dynamics AX 2012 R3 配置の管理](manage-2012-r3-deployment-azure.md) の記事にあります。</span><span class="sxs-lookup"><span data-stu-id="fee39-290">in the [Manage your Microsoft Dynamics AX 2012 R3 deployment on Azure](manage-2012-r3-deployment-azure.md) article.</span></span>

## <a name="consider-legal-and-regulatory-requirements"></a><span data-ttu-id="fee39-291">法的および規制要件を考慮する</span><span class="sxs-lookup"><span data-stu-id="fee39-291">Consider legal and regulatory requirements</span></span>
<span data-ttu-id="fee39-292">Microsoft は、複数の地域や税務署にわたる一般的な運用方法と機能で Azure サービスを実行します。</span><span class="sxs-lookup"><span data-stu-id="fee39-292">Microsoft runs Azure services with common operational practices and features across multiple geographies and jurisdictions.</span></span> <span data-ttu-id="fee39-293">ただし、Microsoft サービスがユーザーの規制の必要を満たしているかどうかを判断するのは、最終的にはユーザー次第となります。</span><span class="sxs-lookup"><span data-stu-id="fee39-293">However, it is ultimately up to you to determine if Microsoft services satisfy your regulatory needs.</span></span> <span data-ttu-id="fee39-294">最新の情報を提供するために、[Azure セキュリティ センター](http://azure.microsoft.com/en-us/support/trust-center/) はセキュリティ、プライバシー、コンプライアンスに関する以下の情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="fee39-294">To help provide you with up-to-date information, the [Azure trust center](http://azure.microsoft.com/en-us/support/trust-center/) provides the following information about security, privacy, and compliance.</span></span>

-   <span data-ttu-id="fee39-295">**セキュリティ**、[Azure セキュリティ ページ](http://www.windowsazure.com/en-us/support/trust-center/security/) は地理的に分散されているデータ センター内に安全な環境を提供するために Microsoft が取っている条項の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="fee39-295">**Security** The [Azure security page](http://www.windowsazure.com/en-us/support/trust-center/security/) provides an overview of the provisions Microsoft is taking to provide a secure environment within geographically dispersed datacenters.</span></span> <span data-ttu-id="fee39-296">セキュリティ関連リソースの広範なリストの中で、[情報の要求についての標準応答: セキュリティおよびプライバシー](https://www.microsoft.com/en-us/download/details.aspx?id=26647) ホワイト ペーパーがどのように Azure の提案されたプリンシパルを満たし、国際標準化機構 (ISO) 27001:2005 および ISO 27002 にマップされているかを概説します。</span><span class="sxs-lookup"><span data-stu-id="fee39-296">Among the extensive list of security-related resources, the [Standard Response to Request for Information: Security and Privacy](https://www.microsoft.com/en-us/download/details.aspx?id=26647) white paper outlines how Azure meets the suggested principals and mapped them to the International Standards Organization (ISO) 27001:2005 and ISO 27002.</span></span>
-   <span data-ttu-id="fee39-297">**プライバシー** [Azure プライバシー ページ](http://www.windowsazure.com/en-us/support/trust-center/privacy/) Azure 環境のプライバシーに関する取り組みを説明する複数のリソースへのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fee39-297">**Privacy** The [Azure privacy page](http://www.windowsazure.com/en-us/support/trust-center/privacy/) includes links to multiple resources that describe privacy practices of the Azure environment.</span></span> <span data-ttu-id="fee39-298">[Azure のプライバシーに関する声明](http://www.windowsazure.com/en-us/support/legal/privacy-statement/)へのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fee39-298">It includes a link to the [Azure privacy statement](http://www.windowsazure.com/en-us/support/legal/privacy-statement/).</span></span>
-   <span data-ttu-id="fee39-299">**コンプライアンス** [Azure コンプライアンス ページ](http://www.windowsazure.com/en-us/support/trust-center/compliance/)は、独自の業界に適用される特定の法律および規制を順守し、シナリオを使用するためのリソースを提供します。</span><span class="sxs-lookup"><span data-stu-id="fee39-299">**Compliance** The [Azure compliance page](http://www.windowsazure.com/en-us/support/trust-center/compliance/) provides resources to help you comply with the specific laws and regulations applicable to your unique industry and use scenario.</span></span>

## <a name="consider-licensing-requirements"></a><span data-ttu-id="fee39-300">ライセンス供与の要件の検討</span><span class="sxs-lookup"><span data-stu-id="fee39-300">Consider licensing requirements</span></span>
<span data-ttu-id="fee39-301">AX 2012 R3 仮想マシン環境のさまざまなコンポーネントのライセンス供与は、重要な考慮事項です。</span><span class="sxs-lookup"><span data-stu-id="fee39-301">Licensing the various components of the AX 2012 R3 virtual machine environment is an important consideration.</span></span> <span data-ttu-id="fee39-302">Azure での展開は、 Azure に固有な特別なライセンス条項であるか、およびそれらの条項がソリューションの全体的な適合性を備えているかを評価します。</span><span class="sxs-lookup"><span data-stu-id="fee39-302">For deployments on Azure, you will want to evaluate the special licensing terms specific to Azure and the impact that these terms have on the overall suitability of the solution.</span></span> <span data-ttu-id="fee39-303">ライセンス供与の要件は、Azure に配置する AX 2012 R3 仮想マシン環境の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="fee39-303">Licensing requirements vary based on the type of AX 2012 R3 virtual machine environment that you deploy on Azure.</span></span> <span data-ttu-id="fee39-304">次のテーブルに詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="fee39-304">The following table provides more information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fee39-305"><strong>環境のタイプ</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-305"><strong>Type of environment</strong></span></span></td>
<td><span data-ttu-id="fee39-306"><strong>ライセンス要件</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-306"><strong>Licensing requirements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-307">デモ</span><span class="sxs-lookup"><span data-stu-id="fee39-307">Demo</span></span></td>
<td><span data-ttu-id="fee39-308">仮想マシン環境に含まれるソフトウェアは、ソフトウェア ライセンス条項の項目に従って、時間制限付きで使用許諾されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-308">The software that is included in the virtual machine environment is time-bound and licensed according to the terms in the Software License Terms.</span></span>
<ul>
<li><span data-ttu-id="fee39-309"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">AX 2013 R3 デモ環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="fee39-309"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">Software License Terms for the AX 2013 R3 demo environment</a></span></span></li>
<li><span data-ttu-id="fee39-310"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">AX 2013 R3 CU8 デモ環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="fee39-310"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">Software License Terms for the AX 2013 R3 CU8 demo environment</a></span></span></li>
<li><span data-ttu-id="fee39-311"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">5. Retail Essentials デモ環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="fee39-311"><a href="http://go.microsoft.com/fwlink/?LinkId=397371">Software License Terms for the Retail essentials demo environment</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fee39-312">開発/テストおよび高可用性</span><span class="sxs-lookup"><span data-stu-id="fee39-312">Dev/test and high availability</span></span></td>
<td><span data-ttu-id="fee39-313">仮想マシン環境を含めすべてのソフトウェアには適切なライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="fee39-313">All software included in the virtual machine environment must be properly licensed.</span></span> <span data-ttu-id="fee39-314">パートナーとマイクロソフトの担当者共に、ライセンスのニーズを十分に調査してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-314">Please investigate your licensing needs thoroughly with your partner and your Microsoft representative.</span></span> <span data-ttu-id="fee39-315">仮想マシン環境に含まれる個々のソフトウェアの条件を調査する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-315">You will need to investigate the terms for each piece of software that is included in the virtual machine environment.</span></span> <span data-ttu-id="fee39-316">仮想マシン環境に含まれるソフトウェアの完全な一覧については、ソフトウェア ライセンス条項を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-316">For the complete list of software that is included in the virtual machine environment, review the Software License Terms.</span></span>
<ul>
<li><span data-ttu-id="fee39-317"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">開発環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="fee39-317"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the development environment</a></span></span></li>
<li><span data-ttu-id="fee39-318"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">共有の SQL Server 環境による開発用のソフトウェア ライセンス条件</a></span><span class="sxs-lookup"><span data-stu-id="fee39-318"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the development with shared SQL Server environment</a></span></span></li>
<li><span data-ttu-id="fee39-319"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="fee39-319"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the test environment</a></span></span></li>
<li><span data-ttu-id="fee39-320"><a href="http://go.microsoft.com/fwlink/?LinkID=507496&amp;amp;clcid=0x409">5. Retail Essentials 開発/テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="fee39-320"><a href="http://go.microsoft.com/fwlink/?LinkID=507496&amp;amp;clcid=0x409">Software License Terms for the Retail essentials dev/test environment</a></span></span></li>
<li><span data-ttu-id="fee39-321"><a href="http://go.microsoft.com/fwlink/?LinkID=507494">5. Retail E-commerce 開発/テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="fee39-321"><a href="http://go.microsoft.com/fwlink/?LinkID=507494">Software License Terms for the Retail e-commerce dev/test environment</a></span></span></li>
<li><span data-ttu-id="fee39-322"><a href="http://go.microsoft.com/fwlink/?LinkID=507496">5. Retail Mobility 開発/テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="fee39-322"><a href="http://go.microsoft.com/fwlink/?LinkID=507496">Software License Terms for the Retail mobility dev/test environment</a></span></span></li>
<li><span data-ttu-id="fee39-323"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">高可用性環境のソフトウェア ライセンス条項</a>ライセンス条項と要件を確認する際には、Azure に配置するために特に適用される条項、および使用目的に適用される条項に特に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-323"><a href="http://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the high availability environment</a> When reviewing the licensing terms and requirements, you need to pay special attention to any terms that apply specifically to deploying on Azure, as well as terms that apply to your intended use.</span></span> <span data-ttu-id="fee39-324">たとえば、Microsoft Office は Azure に固有の条件を持ちますが、これらの条件は、開発またはテスト目的で Office を配置するか、または生産目的で Office を配置するかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="fee39-324">For example, Microsoft Office has terms that are specific to Azure; but those terms vary depending on whether you deploy Office for development or test purposes, or whether you deploy Office for production purposes.</span></span></li>
</ul>
<span data-ttu-id="fee39-325">開始するうえで役立ついくつかのリソースを以下のリンクに示します。</span><span class="sxs-lookup"><span data-stu-id="fee39-325">Some resources to help you get started are linked to below.</span></span> <span data-ttu-id="fee39-326">以下にリンクされているリソースのほとんどに、複数の製品およびシナリオの詳細な情報へのリンクが含まれています。ただし、追加の情報を確認しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-326">Most of the resources that are linked to below contain links to in-depth information for several products and scenarios; however, you may need to review additional information, as well.</span></span> <span data-ttu-id="fee39-327">この情報は、ライセンスを取得した製品の承認済みの使用に関するガイドに役立つ情報です。 同意ではありません。</span><span class="sxs-lookup"><span data-stu-id="fee39-327">This information is provided to help guide your authorized use of products you license; it is not your agreement.</span></span> <span data-ttu-id="fee39-328">ボリューム ライセンス契約にもとづいてライセンスされている製品の使用は、その契約の条件によって支配されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-328">Your use of products licensed under your volume license agreement is governed by the terms and conditions of that agreement.</span></span> <span data-ttu-id="fee39-329">ここにリンクされている情報と契約に矛盾がある場合、契約の使用条件が有効となります。</span><span class="sxs-lookup"><span data-stu-id="fee39-329">In the case of any conflict between information linked here and your agreement, the terms and conditions of your agreement control.</span></span>
<ul>
<li><span data-ttu-id="fee39-330"><strong>仮想マシン ライセンスによく寄せられる質問</strong> Azure 仮想マシンのライセンスに関するよくある質問は、<a href="http://www.windowsazure.com/en-us/pricing/licensing-faq/">このページ</a>で回答されています。</span><span class="sxs-lookup"><span data-stu-id="fee39-330"><strong>Virtual machines licensing FAQ</strong> Common questions regarding licensing on Azure virtual machines are answered on <a href="http://www.windowsazure.com/en-us/pricing/licensing-faq/">this page</a>.</span></span></li>
<li><span data-ttu-id="fee39-331"><strong>Microsoft 製品の使用権限と製品リスト</strong>ビジネス上の意思決定を効果的にし、IT 購入価値を最大化するために、<a href="http://go.microsoft.com/fwlink/?LinkId=397363">このページ</a>で、Microsoft ボリューム ライセンス製品のライセンスモデル、プログラム、シナリオ、および使用条件について詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="fee39-331"><strong>Microsoft Product Use Rights and Product List</strong> Learn more about Microsoft Volume Licensing product licensing models, programs, scenarios, and terms and conditions to help you make effective business decisions and maximize the value of your IT purchases on <a href="http://go.microsoft.com/fwlink/?LinkId=397363">this page</a>.</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="fee39-332"><strong>Azure プログラムのソフトウェア保証によるライセンス モビリティ</strong>ソフトウェア保証によるライセンス モビリティにより、Microsoft ボリューム ライセンスの顧客は、Azure でアクティブなソフトウェア保証を使用して、適格なサーバー アプリケーションを配置する柔軟性を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="fee39-332"><strong>License Mobility through Software Assurance on Azure program</strong> License Mobility through Software Assurance gives Microsoft volume licensing customers the flexibility to deploy eligible server applications with active Software Assurance on Azure.</span></span> <span data-ttu-id="fee39-333">このソフトウェア保証給付金では、新しいライセンスを購入する必要がなく、関連するモビリティ費用がかかりません。</span><span class="sxs-lookup"><span data-stu-id="fee39-333">With this Software Assurance benefit, there is no need to purchase new licenses and no associated mobility fees.</span></span> <span data-ttu-id="fee39-334">これにより、既存のライセンスを Azure クラウド プラットフォームに簡単に展開できます。</span><span class="sxs-lookup"><span data-stu-id="fee39-334">This enables you to easily deploy existing licenses on the Azure cloud platform.</span></span> <span data-ttu-id="fee39-335">詳細については、<a href="http://www.windowsazure.com/en-us/pricing/license-mobility/">このページ</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-335">For more information, see <a href="http://www.windowsazure.com/en-us/pricing/license-mobility/">this page</a>.</span></span> <span data-ttu-id="fee39-336">開発、テスト、および SharePoint の高可用性トポロジ トライアル版用に、Visual Studio、SQL Server および Office が提供されています。</span><span class="sxs-lookup"><span data-stu-id="fee39-336">For Development, Test, and High Availability topologies trial versions of SharePoint, Visual Studio, SQL Server, and Office are provided.</span></span> <span data-ttu-id="fee39-337">評価の範囲は 30〜180 日間です。</span><span class="sxs-lookup"><span data-stu-id="fee39-337">The trials range from 30-180 days.</span></span> <span data-ttu-id="fee39-338">それに応じてライセンスを適用してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-338">Please apply licenses accordingly.</span></span></li>
<li><span data-ttu-id="fee39-339"><strong>Microsoft Dynamics AX ボリューム ライセンス バイヤー ガイド </strong>Microsoft Dynamics AX を使用したキー ライセンス オプションの概要については、<a href="http://go.microsoft.com/fwlink/?LinkId=397363">このページ</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-339"><strong>Microsoft Dynamics AX volume licensing buyer’s guide</strong> For an overview of key licensing options with Microsoft Dynamics AX, see <a href="http://go.microsoft.com/fwlink/?LinkId=397363">this page</a>.</span></span></li>
<li><span data-ttu-id="fee39-340"><strong>Office 365 ProPlus の共有コンピュータの有効化</strong>共有コンピューターの有効化により、複数のユーザーがアクセスする組織内のコンピュータに Office 365 ProPlus を配置できます。</span><span class="sxs-lookup"><span data-stu-id="fee39-340"><strong>Shared computer activation for Office 365 ProPlus</strong> Shared computer activation lets you to deploy Office 365 ProPlus to a computer in your organization that is accessed by multiple users.</span></span> <span data-ttu-id="fee39-341">詳細については、<a href="https://technet.microsoft.com/en-us/library/dn782860(v=office.15).aspx">このページ</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-341">For more information, see <a href="https://technet.microsoft.com/en-us/library/dn782860(v=office.15).aspx">this page</a>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="select-the-ax-2012-r3-environment-that-you-want-to-deploy"></a><span data-ttu-id="fee39-342">配置する AX 2012 R3 環境を選択</span><span class="sxs-lookup"><span data-stu-id="fee39-342">Select the AX 2012 R3 environment that you want to deploy</span></span>
<span data-ttu-id="fee39-343">Azure 上に AX 2012 R3 環境を配置するには、Lifecycle Services のクラウド ホスト環境ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="fee39-343">You’ll use the Cloud-hosted environments tool in Lifecycle Services to deploy AX 2012 R3 environments on Azure.</span></span> <span data-ttu-id="fee39-344">クラウド ホスト環境ツールを使用して配置するとき、デモまたは開発/テスト環境などの、Azure 上に配置する環境のタイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-344">When you use the Cloud-hosted environments tool to deploy, you’ll need to select the type of environment that you want to deploy on Azure, such as a demo or development/test environment.</span></span> <span data-ttu-id="fee39-345">この選択に基づいて、クラウド ホスト環境ツールは Azure での仮想マシンの適切な数を提供します。</span><span class="sxs-lookup"><span data-stu-id="fee39-345">Based on your selection, the Cloud-hosted environments tool provisions the appropriate number of virtual machines on Azure.</span></span> <span data-ttu-id="fee39-346">これらの仮想マシンには、AX 2012 R3 コンポーネント (およびそれらの必要物すべて) がインストール済みです。</span><span class="sxs-lookup"><span data-stu-id="fee39-346">These virtual machines have AX 2012 R3 components—and all of their prerequisites—already installed on them.</span></span> <span data-ttu-id="fee39-347">次のセクションでは、Azure に配置できる AX 2012 R3 環境について説明します。</span><span class="sxs-lookup"><span data-stu-id="fee39-347">The following sections describe the AX 2012 R3 environments that you can deploy on Azure.</span></span>

-   <span data-ttu-id="fee39-348">AX 2012 R3 および AX 2012 R3 CU8 デモ環境</span><span class="sxs-lookup"><span data-stu-id="fee39-348">AX 2012 R3 and AX 2012 R3 CU8 demo environments</span></span>
-   <span data-ttu-id="fee39-349">Retail Essentials デモ環境</span><span class="sxs-lookup"><span data-stu-id="fee39-349">Retail essentials demo environment</span></span>
-   <span data-ttu-id="fee39-350">開発環境</span><span class="sxs-lookup"><span data-stu-id="fee39-350">Development environments</span></span>
-   <span data-ttu-id="fee39-351">テスト環境</span><span class="sxs-lookup"><span data-stu-id="fee39-351">Test environment</span></span>
-   <span data-ttu-id="fee39-352">Retail Essentials 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="fee39-352">Retail essentials dev/test environment</span></span>
-   <span data-ttu-id="fee39-353">Retail E-commerce 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="fee39-353">Retail e-commerce dev/test environment</span></span>
-   <span data-ttu-id="fee39-354">Retail mobility 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="fee39-354">Retail mobility dev/test environment</span></span>
-   <span data-ttu-id="fee39-355">高可用性環境</span><span class="sxs-lookup"><span data-stu-id="fee39-355">High availability environment</span></span>

> [!NOTE]
> <span data-ttu-id="fee39-356">このような環境では、SQL Server は SQL\_Latin1\_General\_CP1\_CI\_AS の照合順序を使用するよう構成されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-356">In these environments, SQL Server is configured to use the SQL\_Latin1\_General\_CP1\_CI\_AS collation.</span></span>

## <a name="ax-2012-r3-and-ax-2012-r3-cu8-demo-environments"></a><span data-ttu-id="fee39-357">AX 2012 R3 および AX 2012 R3 CU8 デモ環境</span><span class="sxs-lookup"><span data-stu-id="fee39-357">AX 2012 R3 and AX 2012 R3 CU8 demo environments</span></span>
<span data-ttu-id="fee39-358">2 つの AX 2012 R3 デモ環境があります。1 方の環境には累積更新プログラム 8 があり、もう 1 つ方にはありません。</span><span class="sxs-lookup"><span data-stu-id="fee39-358">There are two AX 2012 R3 demo environments: one environment includes Cumulative Update 8, and the other does not.</span></span> <span data-ttu-id="fee39-359">次のテーブルは、それぞれの環境に関する詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="fee39-359">The following table lists details about each environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="fee39-360">各環境に含まれる仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="fee39-360">The virtual machine included in each environment is a single-instance virtual machine.</span></span> <span data-ttu-id="fee39-361">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="fee39-361">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/en-us/support/legal/sla/).</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fee39-362"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-362"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="fee39-363"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-363"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="fee39-364"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-364"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="fee39-365"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-365"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-366">1</span><span class="sxs-lookup"><span data-stu-id="fee39-366">1</span></span></td>
<td><span data-ttu-id="fee39-367">デモ マシン</span><span class="sxs-lookup"><span data-stu-id="fee39-367">Demo machine</span></span></td>
<td><span data-ttu-id="fee39-368"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>DEMO-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-368"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> DEMO-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-369">Windows Server 2012 R2、以下を含む:</span><span class="sxs-lookup"><span data-stu-id="fee39-369">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="fee39-370">Active Directory</span><span class="sxs-lookup"><span data-stu-id="fee39-370">Active Directory</span></span></li>
<li><span data-ttu-id="fee39-371">ドメイン名サービス (DNS)</span><span class="sxs-lookup"><span data-stu-id="fee39-371">Domain Name Services (DNS)</span></span></li>
<li><span data-ttu-id="fee39-372">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="fee39-372">Internet Information Services (IIS)</span></span></li>
<li><span data-ttu-id="fee39-373">リモート デスクトップ サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-373">Remote Desktop Services</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-374">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="fee39-374">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="fee39-375">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-375">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-376">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-376">Database Engine Services</span></span></li>
<li><span data-ttu-id="fee39-377">レポート サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-377">Reporting Services</span></span></li>
<li><span data-ttu-id="fee39-378">分析サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-378">Analysis Services</span></span></li>
<li><span data-ttu-id="fee39-379">Management Studio</span><span class="sxs-lookup"><span data-stu-id="fee39-379">Management Studio</span></span></li>
<li><span data-ttu-id="fee39-380">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="fee39-380">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-381">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="fee39-381">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="fee39-382">Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="fee39-382">Microsoft Office 2013</span></span></li>
<li><span data-ttu-id="fee39-383">AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-383">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-384">データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-384">Databases</span></span></li>
<li><span data-ttu-id="fee39-385">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-385">Server components:</span></span>
<ul>
<li><span data-ttu-id="fee39-386">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="fee39-386">Application Object Server (AOS)</span></span></li>
<li><span data-ttu-id="fee39-387">Web サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-387">Web server components:</span></span>
<ul>
<li><span data-ttu-id="fee39-388">エンタープライズ ポータル (EP)</span><span class="sxs-lookup"><span data-stu-id="fee39-388">Enterprise Portal (EP)</span></span></li>
<li><span data-ttu-id="fee39-389">エンタープライズ検索</span><span class="sxs-lookup"><span data-stu-id="fee39-389">Enterprise Search</span></span></li>
<li><span data-ttu-id="fee39-390">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-390">Help Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="fee39-391">ビジネス インテリジェンス コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-391">Business intelligence components:</span></span>
<ul>
<li><span data-ttu-id="fee39-392">Reporting Services 拡張機能</span><span class="sxs-lookup"><span data-stu-id="fee39-392">Reporting Services extensions</span></span></li>
<li><span data-ttu-id="fee39-393">Analysis Services の構成</span><span class="sxs-lookup"><span data-stu-id="fee39-393">Analysis Services configuration</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-394">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-394">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="fee39-395">Management Reporter サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="fee39-395">Management Reporter server components</span></span></li>
<li><span data-ttu-id="fee39-396">Management Reporter レポート デザイナー</span><span class="sxs-lookup"><span data-stu-id="fee39-396">Management Reporter Report Designer</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-397">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-397">Client components:</span></span>
<ul>
<li><span data-ttu-id="fee39-398">クライアント</span><span class="sxs-lookup"><span data-stu-id="fee39-398">Client</span></span></li>
<li><span data-ttu-id="fee39-399">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="fee39-399">Office add-ins</span></span></li>
<li><span data-ttu-id="fee39-400">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="fee39-400">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-401">開発者ツール:</span><span class="sxs-lookup"><span data-stu-id="fee39-401">Developer tools:</span></span>
<ul>
<li><span data-ttu-id="fee39-402">デバッガー</span><span class="sxs-lookup"><span data-stu-id="fee39-402">Debugger</span></span></li>
<li><span data-ttu-id="fee39-403">Visual Studio Tools</span><span class="sxs-lookup"><span data-stu-id="fee39-403">Visual Studio Tools</span></span></li>
<li><span data-ttu-id="fee39-404">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="fee39-404">Trace Parser</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-405">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-405">Integration components:</span></span>
<ul>
<li><span data-ttu-id="fee39-406">IIS 上の Web サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-406">Web services on IIS</span></span></li>
<li><span data-ttu-id="fee39-407">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="fee39-407">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-408">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="fee39-408">Management utilities</span></span></li>
<li><span data-ttu-id="fee39-409">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-409">Retail components:</span></span>
<ul>
<li><span data-ttu-id="fee39-410">Retail POS</span><span class="sxs-lookup"><span data-stu-id="fee39-410">Retail POS</span></span></li>
<li><span data-ttu-id="fee39-411">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="fee39-411">Retail Headquarters</span></span></li>
<li><span data-ttu-id="fee39-412">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-412">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="fee39-413">Synch Service</span><span class="sxs-lookup"><span data-stu-id="fee39-413">Synch Service</span></span></li>
<li><span data-ttu-id="fee39-414">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="fee39-414">Real-time Service</span></span></li>
<li><span data-ttu-id="fee39-415">Async Server</span><span class="sxs-lookup"><span data-stu-id="fee39-415">Async Server</span></span></li>
<li><span data-ttu-id="fee39-416">Async Client</span><span class="sxs-lookup"><span data-stu-id="fee39-416">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-417">Retail チャンネル コンフィギュレーション ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="fee39-417">Retail Channel Configuration Utility</span></span></li>
<li><span data-ttu-id="fee39-418">Retail SDK</span><span class="sxs-lookup"><span data-stu-id="fee39-418">Retail SDK</span></span></li>
<li><span data-ttu-id="fee39-419">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="fee39-419">Retail online channel</span></span></li>
<li><span data-ttu-id="fee39-420">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-420">Retail Server</span></span></li>
<li><span data-ttu-id="fee39-421">Retail 一括配置ツールキット</span><span class="sxs-lookup"><span data-stu-id="fee39-421">Retail Mass Deployment Toolkit</span></span></li>
<li><span data-ttu-id="fee39-422">Retail チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-422">Retail channel database</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-423">RapidStart Connector</span><span class="sxs-lookup"><span data-stu-id="fee39-423">RapidStart Connector</span></span></li>
<li><span data-ttu-id="fee39-424">データのインポート/エクスポート フレームワーク コンポーネント。</span><span class="sxs-lookup"><span data-stu-id="fee39-424">Data Import/Export Framework components:</span></span>
<ul>
<li><span data-ttu-id="fee39-425">データのインポート/エクスポート フレームワーク (DIXF) サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-425">Data Import/Export Framework (DIXF) service</span></span></li>
<li><span data-ttu-id="fee39-426">AOS コンポーネント</span><span class="sxs-lookup"><span data-stu-id="fee39-426">AOS component</span></span></li>
<li><span data-ttu-id="fee39-427">クライアント コンポーネント</span><span class="sxs-lookup"><span data-stu-id="fee39-427">Client component</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-428">倉庫モバイル デバイス ポータル</span><span class="sxs-lookup"><span data-stu-id="fee39-428">Warehouse Mobile Devices Portal</span></span></li>
<li><span data-ttu-id="fee39-429">Microsoft Dynamics Connector</span><span class="sxs-lookup"><span data-stu-id="fee39-429">Connector for Microsoft Dynamics</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-essentials-demo-environment"></a><span data-ttu-id="fee39-430">Retail Essentials デモ環境</span><span class="sxs-lookup"><span data-stu-id="fee39-430">Retail Essentials demo environment</span></span>
<span data-ttu-id="fee39-431">この環境を配置して、Retail Essentials をデモしてください。</span><span class="sxs-lookup"><span data-stu-id="fee39-431">Deploy this environment to demo Retail essentials.</span></span> <span data-ttu-id="fee39-432">Retail Essentials は、Microsoft Dynamics AX の小売中心のコンフィギュレーション オプションです。</span><span class="sxs-lookup"><span data-stu-id="fee39-432">Retail essentials is a retail-centric configuration option for Microsoft Dynamics AX.</span></span> <span data-ttu-id="fee39-433">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fee39-433">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="fee39-434">この仮想マシンには、Windows Server と、Retail Essentials をデモンストレーションするために必要なソフトウェアとサンプル データが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="fee39-434">This virtual machine has Windows Server—and the software and sample data that you’ll need to demo Retail essentials—already installed on it.</span></span> <span data-ttu-id="fee39-435">次のテーブルは、既定の Retail Essentials デモ環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="fee39-435">The following table lists details about the default Retail essentials demo environment.</span></span> <span data-ttu-id="fee39-436">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="fee39-436">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="fee39-437">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="fee39-437">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="fee39-438">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="fee39-438">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/en-us/support/legal/sla/).</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fee39-439"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-439"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="fee39-440"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-440"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="fee39-441"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-441"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="fee39-442"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-442"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-443">1</span><span class="sxs-lookup"><span data-stu-id="fee39-443">1</span></span></td>
<td><span data-ttu-id="fee39-444">Retail Essentials デモ コンピューター</span><span class="sxs-lookup"><span data-stu-id="fee39-444">Retail essentials demo machine</span></span></td>
<td><span data-ttu-id="fee39-445"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>DEMO-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-445"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> DEMO-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-446">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fee39-446">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="fee39-447">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-447">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-448">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-448">Database Engine Services</span></span></li>
<li><span data-ttu-id="fee39-449">Management Studio</span><span class="sxs-lookup"><span data-stu-id="fee39-449">Management Studio</span></span></li>
<li><span data-ttu-id="fee39-450">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="fee39-450">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-451">AX 2012 R3 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-451">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-452">データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-452">Databases</span></span></li>
<li><span data-ttu-id="fee39-453">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-453">Server components:</span></span>
<ul>
<li><span data-ttu-id="fee39-454">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="fee39-454">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-455">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-455">Client components:</span></span>
<ul>
<li><span data-ttu-id="fee39-456">クライアント</span><span class="sxs-lookup"><span data-stu-id="fee39-456">Client</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-457">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-457">Integration components:</span></span>
<ul>
<li><span data-ttu-id="fee39-458">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="fee39-458">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-459">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-459">Retail components:</span></span>
<ul>
<li><span data-ttu-id="fee39-460">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="fee39-460">Retail Headquarters</span></span></li>
<li><span data-ttu-id="fee39-461">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-461">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="fee39-462">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="fee39-462">Real-time Service</span></span></li>
<li><span data-ttu-id="fee39-463">Async Server</span><span class="sxs-lookup"><span data-stu-id="fee39-463">Async Server</span></span></li>
<li><span data-ttu-id="fee39-464">Async Client</span><span class="sxs-lookup"><span data-stu-id="fee39-464">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-465">Retail チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-465">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="development-environments"></a><span data-ttu-id="fee39-466">開発環境</span><span class="sxs-lookup"><span data-stu-id="fee39-466">Development environments</span></span>
<span data-ttu-id="fee39-467">多くの開発者の開発努力を迅速に開始する必要がある場合は、これらの開発環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="fee39-467">Deploy these development environments when you need to quickly jumpstart a development effort for one to many developers.</span></span> <span data-ttu-id="fee39-468">各開発者の開発用仮想マシン (VM) を数日ではなく数時間で展開します。</span><span class="sxs-lookup"><span data-stu-id="fee39-468">Deploy a development virtual machine (VM) for each of your developers in a matter of hours instead of days.</span></span> <span data-ttu-id="fee39-469">開発環境には、テスト環境と同じドメインおよび仮想ネットワーク カスタマイズすべてが用意されています。</span><span class="sxs-lookup"><span data-stu-id="fee39-469">With a development environment, you have all the same domain and virtual network customizations that you have with the Test environment.</span></span> <span data-ttu-id="fee39-470">開発者シナリオには 2 つのトポロジ オプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="fee39-470">Two topology options are provided for developer scenarios:</span></span>

-   <span data-ttu-id="fee39-471">開発。Active Directory と共に展開されたオールインワンの VM を含みます。</span><span class="sxs-lookup"><span data-stu-id="fee39-471">Development: Includes all-in-one VMs deployed with Active Directory.</span></span>
-   <span data-ttu-id="fee39-472">共有 SQL Server による開発。Active Directory と共に展開されたオールインワンの VM を含みます。</span><span class="sxs-lookup"><span data-stu-id="fee39-472">Development with shared SQL Server: Includes all-in-one VMs deployed with Active Directory.</span></span> <span data-ttu-id="fee39-473">各開発 VM インスタンスのデータベースは、共有 SQL Server インスタンスに配置されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-473">The database for each development VM instance will be deployed to a shared SQL Server instance.</span></span>

<span data-ttu-id="fee39-474">それらの BI 開発の実行については、目的に対する 1 つのインスタンスを配置することができます。</span><span class="sxs-lookup"><span data-stu-id="fee39-474">For those doing BI development you can deploy one instance for the purpose.</span></span> <span data-ttu-id="fee39-475">その他のすべてのインスタンスは BI で配置されません。</span><span class="sxs-lookup"><span data-stu-id="fee39-475">All other instances will not deploy with BI.</span></span> <span data-ttu-id="fee39-476">提供されている開発用 VM には、すべての AX 2012 R3 コンポーネントが Visual Studio 2013 および AX 2012 R3 開発ツールとともにインストールされています。</span><span class="sxs-lookup"><span data-stu-id="fee39-476">The development VMs provided have all the AX 2012 R3 components installed with Visual Studio 2013 and AX 2012 R3 development tools.</span></span> <span data-ttu-id="fee39-477">VM は、展開時に Active Directory ドメインに結合されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-477">The VMs are joined to the Active Directory domain at deployment time.</span></span> <span data-ttu-id="fee39-478">カスタマイズ オプションとして Active Directory ドメインを指定する場合は、VM はそのドメインに参加します。</span><span class="sxs-lookup"><span data-stu-id="fee39-478">If you provided an Active Directory domain as a customization option, then the VMs will join to that domain.</span></span> <span data-ttu-id="fee39-479">開発 VM は、AX 2012 R3 チェックリストの時点まで配置され、すべてのソフトウェアがインストールされていることがテスト環境にリストされます。</span><span class="sxs-lookup"><span data-stu-id="fee39-479">Development VMs will be deployed up to the point of the AX 2012 R3 checklist, and have all the software installed that is listed in the Test environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="fee39-480">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="fee39-480">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="fee39-481">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="fee39-481">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/en-us/support/legal/sla/).</span></span>

## <a name="test-environment"></a><span data-ttu-id="fee39-482">テスト環境</span><span class="sxs-lookup"><span data-stu-id="fee39-482">Test environment</span></span>
<span data-ttu-id="fee39-483">この環境には、既定で数台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fee39-483">This environment includes several virtual machines, by default.</span></span> <span data-ttu-id="fee39-484">これらの仮想マシンには、すでにインストールされている Windows Server および AX 2012 R3 のテストに必要なソフトウェアがあります。</span><span class="sxs-lookup"><span data-stu-id="fee39-484">These virtual machines have Windows Server—and the software that you’ll need for AX 2012 R3 testing purposes—already installed on them.</span></span> <span data-ttu-id="fee39-485">次のテーブルは、既定のテスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="fee39-485">The following table lists details about the default test environment.</span></span> <span data-ttu-id="fee39-486">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="fee39-486">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="fee39-487">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="fee39-487">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="fee39-488">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="fee39-488">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/en-us/support/legal/sla/).</span></span> <span data-ttu-id="fee39-489">データのインポート/エクスポート フレームワーク (DIXF) コンポーネントは既定ではインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="fee39-489">Data Import/Export Framework (DIXF) components are not installed by default.</span></span> <span data-ttu-id="fee39-490">DIXF を使用する場合は、独自の SQL Server インストール メディアを使用して、SQL Server マシンに SQL Server Integration Services (SSIS) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-490">If you want to use DIXF, you must use your own SQL Server installation media to install SQL Server Integration Services (SSIS) on the SQL Server machine.</span></span> <span data-ttu-id="fee39-491">SSIS をインストールした後は、Dynamics AX CD (VM 内の接続されたドライブで利用可能) を使用し、DIXF コンポーネントを AOS およびクライアント マシンにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="fee39-491">After you install SSIS, you can use the Dynamics AX CD (available on a connected drive within the VMs) to install the DIXF components on the AOS and then client machines.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fee39-492"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-492"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="fee39-493"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-493"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="fee39-494"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-494"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="fee39-495"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-495"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-496">1</span><span class="sxs-lookup"><span data-stu-id="fee39-496">1</span></span></td>
<td><span data-ttu-id="fee39-497">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="fee39-497">Domain controller</span></span></td>
<td><span data-ttu-id="fee39-498"><strong>サイズ:</strong>D1: 基本的な計算層 (1 コア、3.5 GB メモリ) <strong>既定名:</strong>AD-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-498"><strong>Size:</strong> D1: Basic compute tier (1 core, 3.5 GB memory)<strong>Default name:</strong> AD-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-499">Windows Server 2012 R2、以下を含む:</span><span class="sxs-lookup"><span data-stu-id="fee39-499">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="fee39-500">Active Directory</span><span class="sxs-lookup"><span data-stu-id="fee39-500">Active Directory</span></span></li>
<li><span data-ttu-id="fee39-501">ドメイン名サービス (DNS)</span><span class="sxs-lookup"><span data-stu-id="fee39-501">Domain Name Services (DNS)</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fee39-502">1</span><span class="sxs-lookup"><span data-stu-id="fee39-502">1</span></span></td>
<td><span data-ttu-id="fee39-503">AOS サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-503">AOS server</span></span></td>
<td><span data-ttu-id="fee39-504"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>AOS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-504"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> AOS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-505">Windows Server 2012 R2、以下を含む:</span><span class="sxs-lookup"><span data-stu-id="fee39-505">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="fee39-506">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="fee39-506">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-507">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="fee39-507">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="fee39-508">Microsoft Project Server</span><span class="sxs-lookup"><span data-stu-id="fee39-508">Microsoft Project Server</span></span></li>
<li><span data-ttu-id="fee39-509">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-509">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-510">Management Studio</span><span class="sxs-lookup"><span data-stu-id="fee39-510">Management Studio</span></span></li>
<li><span data-ttu-id="fee39-511">ネイティブ クライアント</span><span class="sxs-lookup"><span data-stu-id="fee39-511">Native Client</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-512">AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-512">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-513">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-513">Server components:</span></span>
<ul>
<li><span data-ttu-id="fee39-514">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="fee39-514">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-515">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-515">Client components:</span></span>
<ul>
<li><span data-ttu-id="fee39-516">クライアント</span><span class="sxs-lookup"><span data-stu-id="fee39-516">Client</span></span></li>
<li><span data-ttu-id="fee39-517">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="fee39-517">Office add-ins</span></span></li>
<li><span data-ttu-id="fee39-518">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="fee39-518">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-519">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-519">Integration components:</span></span>
<ul>
<li><span data-ttu-id="fee39-520">IIS 上の Web サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-520">Web services on IIS</span></span></li>
<li><span data-ttu-id="fee39-521">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="fee39-521">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-522">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="fee39-522">Management utilities</span></span></li>
<li><span data-ttu-id="fee39-523">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-523">Retail components:</span></span>
<ul>
<li><span data-ttu-id="fee39-524">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="fee39-524">Retail Headquarters</span></span></li>
<li><span data-ttu-id="fee39-525">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-525">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="fee39-526">Synch Service</span><span class="sxs-lookup"><span data-stu-id="fee39-526">Synch Service</span></span></li>
<li><span data-ttu-id="fee39-527">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="fee39-527">Real-time Service</span></span></li>
<li><span data-ttu-id="fee39-528">Async Server</span><span class="sxs-lookup"><span data-stu-id="fee39-528">Async Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="fee39-529">RapidStart Connector</span><span class="sxs-lookup"><span data-stu-id="fee39-529">RapidStart Connector</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-530">1</span><span class="sxs-lookup"><span data-stu-id="fee39-530">1</span></span></td>
<td><span data-ttu-id="fee39-531">データベース サーバー/BIサーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-531">Database server/BI server</span></span></td>
<td><span data-ttu-id="fee39-532"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>SQL-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-532"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> SQL-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-533">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fee39-533">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="fee39-534">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-534">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-535">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-535">Database Engine Services</span></span></li>
<li><span data-ttu-id="fee39-536">レポート サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-536">Reporting Services</span></span></li>
<li><span data-ttu-id="fee39-537">分析サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-537">Analysis Services</span></span></li>
<li><span data-ttu-id="fee39-538">Management Studio</span><span class="sxs-lookup"><span data-stu-id="fee39-538">Management Studio</span></span></li>
</ul></li>
</ul><span data-ttu-id="fee39-539">
    <strong>注記:</strong> Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="fee39-539">
    <strong>Note: </strong> Reporting Services is configured to run in Native mode.</span></span> <span data-ttu-id="fee39-540">電源表示を使用するには、追加の構成手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-540">To use Power View, you’ll need to complete additional configuration steps.</span></span> <span data-ttu-id="fee39-541">詳細については、<a href="https://technet.microsoft.com/en-us/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-541">For more information, see the prerequisites listed in <a href="https://technet.microsoft.com/en-us/library/jj933492.aspx">Create a report by using Power View to connect to a cube</a>.</span></span>
<ul>
<li><span data-ttu-id="fee39-542">AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-542">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-543">データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-543">Databases</span></span></li>
<li><span data-ttu-id="fee39-544">ビジネス インテリジェンス コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-544">Business intelligence components:</span></span>
<ul>
<li><span data-ttu-id="fee39-545">Reporting Services 拡張機能</span><span class="sxs-lookup"><span data-stu-id="fee39-545">Reporting Services extensions</span></span></li>
<li><span data-ttu-id="fee39-546">Analysis Services の構成</span><span class="sxs-lookup"><span data-stu-id="fee39-546">Analysis Services configuration</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fee39-547">0</span><span class="sxs-lookup"><span data-stu-id="fee39-547">0</span></span></td>
<td><span data-ttu-id="fee39-548">エンタープライズ ポータル サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-548">Enterprise Portal server</span></span></td>
<td><span data-ttu-id="fee39-549"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>EP-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-549"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> EP-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-550">Windows Server 2012 R2、以下を含む:</span><span class="sxs-lookup"><span data-stu-id="fee39-550">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="fee39-551">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="fee39-551">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-552">Microsoft SQL Server 2012 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-552">Microsoft SQL Server 2012 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-553">フル テキスト検索</span><span class="sxs-lookup"><span data-stu-id="fee39-553">Full-text Search</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-554">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="fee39-554">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="fee39-555">AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-555">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-556">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-556">Server components:</span></span>
<ul>
<li><span data-ttu-id="fee39-557">Web サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-557">Web server components:</span></span>
<ul>
<li><span data-ttu-id="fee39-558">エンタープライズ ポータル (EP)</span><span class="sxs-lookup"><span data-stu-id="fee39-558">Enterprise Portal (EP)</span></span></li>
<li><span data-ttu-id="fee39-559">エンタープライズ検索</span><span class="sxs-lookup"><span data-stu-id="fee39-559">Enterprise Search</span></span></li>
<li><span data-ttu-id="fee39-560">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-560">Help Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="fee39-561">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-561">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="fee39-562">Management Reporter サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="fee39-562">Management Reporter server components</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-563">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-563">Retail components:</span></span>
<ul>
<li><span data-ttu-id="fee39-564">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-564">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="fee39-565">Async Client</span><span class="sxs-lookup"><span data-stu-id="fee39-565">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-566">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-566">Retail Server</span></span></li>
<li><span data-ttu-id="fee39-567">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="fee39-567">Retail Online Channel</span></span></li>
<li><span data-ttu-id="fee39-568">Retail チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-568">Retail Channel Database</span></span></li>
<li><span data-ttu-id="fee39-569">Retail チャンネル コンフィギュレーション ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="fee39-569">Retail Channel Configuration Utility</span></span></li>
<li><span data-ttu-id="fee39-570">Retail ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="fee39-570">Retail Hardware Station</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-571">倉庫モバイル デバイス ポータル</span><span class="sxs-lookup"><span data-stu-id="fee39-571">Warehouse Mobile Devices Portal</span></span></li>
<li><span data-ttu-id="fee39-572">Microsoft Dynamics Connector</span><span class="sxs-lookup"><span data-stu-id="fee39-572">Connector for Microsoft Dynamics</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-573">1</span><span class="sxs-lookup"><span data-stu-id="fee39-573">1</span></span></td>
<td><span data-ttu-id="fee39-574">クライアント コンピューター</span><span class="sxs-lookup"><span data-stu-id="fee39-574">Client computer</span></span></td>
<td><span data-ttu-id="fee39-575"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>CLI-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-575"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> CLI-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-576">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fee39-576">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="fee39-577">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="fee39-577">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="fee39-578">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-578">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-579">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="fee39-579">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-580">Microsoft SharePoint Server 2013 クライアント コンポーネント SDK</span><span class="sxs-lookup"><span data-stu-id="fee39-580">Microsoft SharePoint Server 2013 Client Components SDK</span></span></li>
<li><span data-ttu-id="fee39-581">Microsoft Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="fee39-581">Microsoft Office 365 ProPlus</span></span></li>
<li><span data-ttu-id="fee39-582">AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-582">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-583">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-583">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="fee39-584">Management Reporter レポート デザイナー</span><span class="sxs-lookup"><span data-stu-id="fee39-584">Management Reporter Report Designer</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-585">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-585">Client components:</span></span>
<ul>
<li><span data-ttu-id="fee39-586">クライアント</span><span class="sxs-lookup"><span data-stu-id="fee39-586">Client</span></span></li>
<li><span data-ttu-id="fee39-587">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="fee39-587">Office add-ins</span></span></li>
<li><span data-ttu-id="fee39-588">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="fee39-588">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-589">開発者ツール:</span><span class="sxs-lookup"><span data-stu-id="fee39-589">Developer tools:</span></span>
<ul>
<li><span data-ttu-id="fee39-590">デバッガー</span><span class="sxs-lookup"><span data-stu-id="fee39-590">Debugger</span></span></li>
<li><span data-ttu-id="fee39-591">Visual Studio Tools</span><span class="sxs-lookup"><span data-stu-id="fee39-591">Visual Studio Tools</span></span></li>
<li><span data-ttu-id="fee39-592">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="fee39-592">Trace Parser</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-593">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="fee39-593">Management utilities</span></span></li>
<li><span data-ttu-id="fee39-594">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-594">Retail components:</span></span>
<ul>
<li><span data-ttu-id="fee39-595">Retail POS</span><span class="sxs-lookup"><span data-stu-id="fee39-595">Retail POS</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fee39-596">0</span><span class="sxs-lookup"><span data-stu-id="fee39-596">0</span></span></td>
<td><span data-ttu-id="fee39-597">リモート デスクトップ サービス サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-597">Remote Desktop Services server</span></span></td>
<td><span data-ttu-id="fee39-598"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>RDS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-598"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> RDS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-599">Windows Server 2012 R2、以下を含む:</span><span class="sxs-lookup"><span data-stu-id="fee39-599">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="fee39-600">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="fee39-600">Internet Information Services (IIS)</span></span></li>
<li><span data-ttu-id="fee39-601">リモート デスクトップ サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-601">Remote Desktop Services</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-602">Microsoft SQL Server 2012 Native Client</span><span class="sxs-lookup"><span data-stu-id="fee39-602">Microsoft SQL Server 2012 Native Client</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-essentials-devtest-environment"></a><span data-ttu-id="fee39-603">Retail Essentials 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="fee39-603">Retail Essentials dev/test environment</span></span>
<span data-ttu-id="fee39-604">この環境を配置して、Retail essentials の機能を開発またはテストします。</span><span class="sxs-lookup"><span data-stu-id="fee39-604">Deploy this environment to develop or test features for Retail essentials.</span></span> <span data-ttu-id="fee39-605">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fee39-605">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="fee39-606">この仮想マシンには、Windows Server と、Retail Essentials の開発とテストの目的で必要となるソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="fee39-606">This virtual machine has Windows Server—and the software that you’ll need for Retail essentials development and testing purposes—already installed on it.</span></span> <span data-ttu-id="fee39-607">次のテーブルは、既定の Retail Essentials 開発/テスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="fee39-607">The following table lists details about the default Retail essentials dev/test environment.</span></span> <span data-ttu-id="fee39-608">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="fee39-608">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="fee39-609">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="fee39-609">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="fee39-610">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="fee39-610">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/en-us/support/legal/sla/).</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fee39-611"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-611"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="fee39-612"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-612"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="fee39-613"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-613"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="fee39-614"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-614"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-615">1</span><span class="sxs-lookup"><span data-stu-id="fee39-615">1</span></span></td>
<td><span data-ttu-id="fee39-616">Retail Essentials サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-616">Retail essentials server</span></span></td>
<td><span data-ttu-id="fee39-617"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>ESSEN-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-617"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> ESSEN-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-618">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fee39-618">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="fee39-619">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-619">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-620">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-620">Database Engine Services</span></span></li>
<li><span data-ttu-id="fee39-621">Management Studio</span><span class="sxs-lookup"><span data-stu-id="fee39-621">Management Studio</span></span></li>
<li><span data-ttu-id="fee39-622">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="fee39-622">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-623">AX 2012 R3 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-623">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-624">データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-624">Databases</span></span></li>
<li><span data-ttu-id="fee39-625">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-625">Server components:</span></span>
<ul>
<li><span data-ttu-id="fee39-626">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="fee39-626">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-627">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-627">Client components:</span></span>
<ul>
<li><span data-ttu-id="fee39-628">クライアント</span><span class="sxs-lookup"><span data-stu-id="fee39-628">Client</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-629">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-629">Integration components:</span></span>
<ul>
<li><span data-ttu-id="fee39-630">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="fee39-630">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-631">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-631">Retail components:</span></span>
<ul>
<li><span data-ttu-id="fee39-632">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="fee39-632">Retail Headquarters</span></span></li>
<li><span data-ttu-id="fee39-633">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-633">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="fee39-634">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="fee39-634">Real-time Service</span></span></li>
<li><span data-ttu-id="fee39-635">Async Server</span><span class="sxs-lookup"><span data-stu-id="fee39-635">Async Server</span></span></li>
<li><span data-ttu-id="fee39-636">Async Client</span><span class="sxs-lookup"><span data-stu-id="fee39-636">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-637">Retail チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-637">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-ecommerce-devtest-environment"></a><span data-ttu-id="fee39-638">Retail E-commerce 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="fee39-638">Retail ecommerce dev/test environment</span></span>
<span data-ttu-id="fee39-639">この環境を導入して、AX 2012 R3 と完全に統合されたオンライン販売チャネルを作成し、テストします。</span><span class="sxs-lookup"><span data-stu-id="fee39-639">Deploy this environment to create and test an online sales channel that is fully integrated with AX 2012 R3.</span></span> <span data-ttu-id="fee39-640">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fee39-640">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="fee39-641">この仮想マシンには、Windows Server と、小売電子商取引に必要なソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="fee39-641">This virtual machine has Windows Server—and the software that you’ll need for Retail e-commerce—already installed on it.</span></span> <span data-ttu-id="fee39-642">次のテーブルは、既定の Retail E-commerce 開発/テスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="fee39-642">The following table lists details about the default Retail e-commerce dev/test environment.</span></span> <span data-ttu-id="fee39-643">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="fee39-643">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="fee39-644">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="fee39-644">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="fee39-645">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="fee39-645">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/en-us/support/legal/sla/).</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fee39-646"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-646"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="fee39-647"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-647"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="fee39-648"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-648"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="fee39-649"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-649"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-650">1</span><span class="sxs-lookup"><span data-stu-id="fee39-650">1</span></span></td>
<td><span data-ttu-id="fee39-651">Retail E-commerce サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-651">Retail e-commerce server</span></span></td>
<td><span data-ttu-id="fee39-652"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>E-COM-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-652"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> E-COM-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-653">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fee39-653">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="fee39-654">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="fee39-654">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="fee39-655">AX 2012 R3 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-655">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-656">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-656">Retail components:</span></span>
<ul>
<li><span data-ttu-id="fee39-657">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-657">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="fee39-658">Async Client</span><span class="sxs-lookup"><span data-stu-id="fee39-658">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-659">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="fee39-659">Retail online channel</span></span></li>
<li><span data-ttu-id="fee39-660">Retail チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-660">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="retail-mobility-devtest-environment"></a><span data-ttu-id="fee39-661">Retail mobility 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="fee39-661">Retail mobility dev/test environment</span></span>
<span data-ttu-id="fee39-662">この環境を配置することで、販売スタッフが販売トランザクションを処理し、顧客注文を入力し、店舗内のどこでもモバイル デバイスを使用して日々の操作と在庫管理を実行できます。</span><span class="sxs-lookup"><span data-stu-id="fee39-662">Deploy this environment to enable your sales staff to process sales transactions, enter customer orders, and perform daily operations and inventory management with mobile devices anywhere in a store.</span></span> <span data-ttu-id="fee39-663">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fee39-663">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="fee39-664">この仮想マシンには、Windows Server と、小売モビリティに必要なソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="fee39-664">This virtual machine has Windows Server—and the software that you’ll need for Retail mobility—already installed on it.</span></span> <span data-ttu-id="fee39-665">次のテーブルは、既定の Retail Mobility 開発/テスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="fee39-665">The following table lists details about the default Retail mobility dev/test environment.</span></span> <span data-ttu-id="fee39-666">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="fee39-666">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 
> [!NOTE]
> <span data-ttu-id="fee39-667">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="fee39-667">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="fee39-668">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="fee39-668">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](http://azure.microsoft.com/en-us/support/legal/sla/).</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fee39-669"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-669"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="fee39-670"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-670"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="fee39-671"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-671"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="fee39-672"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-672"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-673">1</span><span class="sxs-lookup"><span data-stu-id="fee39-673">1</span></span></td>
<td><span data-ttu-id="fee39-674">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-674">Retail server</span></span></td>
<td><span data-ttu-id="fee39-675"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>MOBIL-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-675"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> MOBIL-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-676">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fee39-676">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="fee39-677">AX 2012 R3 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-677">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-678">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-678">Retail components:</span></span>
<ul>
<li><span data-ttu-id="fee39-679">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-679">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="fee39-680">Async Client</span><span class="sxs-lookup"><span data-stu-id="fee39-680">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-681">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-681">Retail Server</span></span></li>
<li><span data-ttu-id="fee39-682">Retail チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-682">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="high-availability-environment"></a><span data-ttu-id="fee39-683">高可用性環境</span><span class="sxs-lookup"><span data-stu-id="fee39-683">High availability environment</span></span>
<span data-ttu-id="fee39-684">この環境を配置して、高可用性のために構成できる環境で AX 2012 R3 を使用します。</span><span class="sxs-lookup"><span data-stu-id="fee39-684">Deploy this environment to use AX 2012 R3 in an environment that can be configured for high availability.</span></span> <span data-ttu-id="fee39-685">この環境には、数台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fee39-685">This environment includes several virtual machines.</span></span> <span data-ttu-id="fee39-686">これらの仮想マシンには、すでにインストールされている Windows Server および AX 2012 R3 を使用するために必要なソフトウェアがあります。</span><span class="sxs-lookup"><span data-stu-id="fee39-686">These virtual machines have Windows Server—and the software that you’ll need to use AX 2012 R3—already installed on them.</span></span> <span data-ttu-id="fee39-687">次のテーブルは、既定の高可用性環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="fee39-687">The following table lists details about the default high availability environment.</span></span> <span data-ttu-id="fee39-688">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="fee39-688">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="fee39-689">Azure Premium Storage は高可用性環境が必要です。</span><span class="sxs-lookup"><span data-stu-id="fee39-689">Azure Premium Storage is required for high availability environments.</span></span> <span data-ttu-id="fee39-690">詳細については、[Azure での高可用性環境の配置](deploy-high-availability-environment-azure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-690">For more information, see [Deploy a high availability environment on Azure](deploy-high-availability-environment-azure.md).</span></span> <span data-ttu-id="fee39-691">この環境の仮想マシンは、Azure [サービス レベル アグリーメント](http://azure.microsoft.com/en-us/support/legal/sla/)の対象となります。</span><span class="sxs-lookup"><span data-stu-id="fee39-691">The virtual machines in this environment are covered by an Azure [Service Level Agreement](http://azure.microsoft.com/en-us/support/legal/sla/).</span></span> <span data-ttu-id="fee39-692">データのインポート/エクスポート フレームワーク (DIXF) コンポーネントは既定ではインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="fee39-692">Data Import/Export Framework (DIXF) components are not installed by default.</span></span> <span data-ttu-id="fee39-693">DIXF を使用する場合は、独自の SQL Server インストール メディアを使用して、SQL Server マシンに SQL Server Integration Services (SSIS) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-693">If you want to use DIXF, you must use your own SQL Server installation media to install SQL Server Integration Services (SSIS) on the SQL Server machine.</span></span> <span data-ttu-id="fee39-694">SSIS をインストールした後は、Dynamics AX CD (VM 内の接続されたドライブで利用可能) を使用し、DIXF コンポーネントを AOS およびクライアント マシンにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="fee39-694">After you install SSIS, you can use the Dynamics AX CD (available on a connected drive within the VMs) to install the DIXF components on the AOS and then client machines.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fee39-695"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-695"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="fee39-696"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-696"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="fee39-697"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-697"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="fee39-698"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-698"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-699">3 <strong>注記:</strong> 3 つのドメイン コントローラがこの環境に配置されています。</span><span class="sxs-lookup"><span data-stu-id="fee39-699">3<strong>Note: </strong>Three domain controllers are deployed in this environment.</span></span> <span data-ttu-id="fee39-700">1 つのドメイン コントローラーが失敗すると、Azure の<a href="http://azure.microsoft.com/en-us/support/legal/sla/">サービス レベル同意書</a>に準拠するために、2 つのオンライン ドメイン コントローラーを残しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-700">If one domain controller fails, you must be left with two, online domain controllers in order to meet Azure’s <a href="http://azure.microsoft.com/en-us/support/legal/sla/">Service Level Agreement</a>.</span></span></td>
<td><span data-ttu-id="fee39-701">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="fee39-701">Domain controller</span></span></td>
<td><span data-ttu-id="fee39-702"><strong>サイズ:</strong>D1: 基本的な計算層 (1 コア、3.5 GB メモリ) <strong>既定名:</strong>AD-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-702"><strong>Size:</strong> D1: Basic compute tier (1 core, 3.5 GB memory)<strong>Default name:</strong> AD-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-703">Windows Server 2012 R2、以下を含む:</span><span class="sxs-lookup"><span data-stu-id="fee39-703">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="fee39-704">Active Directory</span><span class="sxs-lookup"><span data-stu-id="fee39-704">Active Directory</span></span></li>
<li><span data-ttu-id="fee39-705">ドメイン名サービス (DNS)</span><span class="sxs-lookup"><span data-stu-id="fee39-705">Domain Name Services (DNS)</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fee39-706">2</span><span class="sxs-lookup"><span data-stu-id="fee39-706">2</span></span></td>
<td><span data-ttu-id="fee39-707">AOS サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-707">AOS server</span></span></td>
<td><span data-ttu-id="fee39-708"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>AOS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-708"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> AOS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-709">Windows Server 2012 R2、以下を含む:</span><span class="sxs-lookup"><span data-stu-id="fee39-709">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="fee39-710">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="fee39-710">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-711">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="fee39-711">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="fee39-712">Microsoft Project Server</span><span class="sxs-lookup"><span data-stu-id="fee39-712">Microsoft Project Server</span></span></li>
<li><span data-ttu-id="fee39-713">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-713">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-714">Management Studio</span><span class="sxs-lookup"><span data-stu-id="fee39-714">Management Studio</span></span></li>
<li><span data-ttu-id="fee39-715">ネイティブ クライアント</span><span class="sxs-lookup"><span data-stu-id="fee39-715">Native Client</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-716">AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-716">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-717">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-717">Server components:</span></span>
<ul>
<li><span data-ttu-id="fee39-718">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="fee39-718">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-719">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-719">Client components:</span></span>
<ul>
<li><span data-ttu-id="fee39-720">クライアント</span><span class="sxs-lookup"><span data-stu-id="fee39-720">Client</span></span></li>
<li><span data-ttu-id="fee39-721">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="fee39-721">Office add-ins</span></span></li>
<li><span data-ttu-id="fee39-722">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="fee39-722">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-723">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-723">Integration components:</span></span>
<ul>
<li><span data-ttu-id="fee39-724">IIS 上の Web サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-724">Web services on IIS</span></span></li>
<li><span data-ttu-id="fee39-725">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="fee39-725">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-726">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="fee39-726">Management utilities</span></span></li>
<li><span data-ttu-id="fee39-727">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-727">Retail components:</span></span>
<ul>
<li><span data-ttu-id="fee39-728">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="fee39-728">Retail Headquarters</span></span></li>
<li><span data-ttu-id="fee39-729">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-729">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="fee39-730">Synch Service</span><span class="sxs-lookup"><span data-stu-id="fee39-730">Synch Service</span></span></li>
<li><span data-ttu-id="fee39-731">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="fee39-731">Real-time Service</span></span></li>
<li><span data-ttu-id="fee39-732">Async Server</span><span class="sxs-lookup"><span data-stu-id="fee39-732">Async Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="fee39-733">RapidStart Connector</span><span class="sxs-lookup"><span data-stu-id="fee39-733">RapidStart Connector</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-734">2</span><span class="sxs-lookup"><span data-stu-id="fee39-734">2</span></span></td>
<td><span data-ttu-id="fee39-735">データベース サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-735">Database server</span></span></td>
<td><span data-ttu-id="fee39-736"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>SQL-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-736"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> SQL-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-737">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fee39-737">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="fee39-738">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-738">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-739">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-739">Database Engine Services</span></span></li>
<li><span data-ttu-id="fee39-740">Management Studio</span><span class="sxs-lookup"><span data-stu-id="fee39-740">Management Studio</span></span></li>
</ul></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fee39-741"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-741"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-742">クォーラム サーバーも配置されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-742">A Quorum server is also deployed.</span></span> <span data-ttu-id="fee39-743">この仮想マシンは、AlwaysOn 可用性グループのリスナーです。</span><span class="sxs-lookup"><span data-stu-id="fee39-743">This virtual machine is a listener for the AlwaysOn availability group.</span></span> <span data-ttu-id="fee39-744">この仮想マシンは、o    [高可用性 VM] ボックスの一覧には表示されませんが、高可用性環境で展開されます。o    QRM -&lt;GUID&gt; という名前です。</span><span class="sxs-lookup"><span data-stu-id="fee39-744">This virtual machine:o    Is not represented in the High Availability VM list, but it is deployed with High Availability environments.o    Is named QRM-&lt;GUID&gt;.</span></span> <span data-ttu-id="fee39-745">この名前は customized.o にはできません    A2 仮想マシン.o です    Windows Server 2012 R2.o 配置後のギャラリー 画像を実行します。この VM は、高可用性環境に VM を追加するときに「データベース サーバー」として表示されます。</span><span class="sxs-lookup"><span data-stu-id="fee39-745">This name can’t be customized.o    Is an A2 virtual machine.o    Runs a gallery image of Windows Server 2012 R2.o    Post deployment, this VM appears as a “Database Server” when adding VMs to the High Availability environment.</span></span> <span data-ttu-id="fee39-746">ここで参照されている 3 番目の VM は、明示的に SQL Server ではない A2 Quorum Server です。</span><span class="sxs-lookup"><span data-stu-id="fee39-746">The 3rd VM referenced here is the A2 Quorum Server which is explicitly not a SQL Server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fee39-747"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-747"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-748">Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="fee39-748">Reporting Services is configured to run in Native mode.</span></span> <span data-ttu-id="fee39-749">電源表示を使用するには、追加の構成手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-749">To use Power View, you’ll need to complete additional configuration steps.</span></span> <span data-ttu-id="fee39-750">詳細については、<a href="https://technet.microsoft.com/en-us/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-750">For more information, see the prerequisites listed in <a href="https://technet.microsoft.com/en-us/library/jj933492.aspx">Create a report by using Power View to connect to a cube</a>.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="fee39-751">AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-751">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-752">データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-752">Databases</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fee39-753">2</span><span class="sxs-lookup"><span data-stu-id="fee39-753">2</span></span></td>
<td><span data-ttu-id="fee39-754">ビジネス インテリジェンス (BI) サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-754">Business intelligence (BI) server</span></span></td>
<td><span data-ttu-id="fee39-755"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>BI-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-755"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> BI-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-756">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fee39-756">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="fee39-757">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-757">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-758">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-758">Database Engine Services</span></span></li>
<li><span data-ttu-id="fee39-759">レポート サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-759">Reporting Services</span></span></li>
<li><span data-ttu-id="fee39-760">分析サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-760">Analysis Services</span></span></li>
<li><span data-ttu-id="fee39-761">Management Studio</span><span class="sxs-lookup"><span data-stu-id="fee39-761">Management Studio</span></span></li>
</ul></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fee39-762"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="fee39-762"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-763">Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="fee39-763">Reporting Services is configured to run in Native mode.</span></span> <span data-ttu-id="fee39-764">電源表示を使用するには、追加の構成手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fee39-764">To use Power View, you’ll need to complete additional configuration steps.</span></span> <span data-ttu-id="fee39-765">詳細については、<a href="https://technet.microsoft.com/en-us/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fee39-765">For more information, see the prerequisites listed in <a href="https://technet.microsoft.com/en-us/library/jj933492.aspx">Create a report by using Power View to connect to a cube</a>.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="fee39-766">AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-766">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-767">ビジネス インテリジェンス コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-767">Business intelligence components:</span></span>
<ul>
<li><span data-ttu-id="fee39-768">Reporting Services 拡張機能</span><span class="sxs-lookup"><span data-stu-id="fee39-768">Reporting Services extensions</span></span></li>
<li><span data-ttu-id="fee39-769">Analysis Services の構成</span><span class="sxs-lookup"><span data-stu-id="fee39-769">Analysis Services configuration</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-770">0</span><span class="sxs-lookup"><span data-stu-id="fee39-770">0</span></span></td>
<td><span data-ttu-id="fee39-771">エンタープライズ ポータル サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-771">Enterprise Portal server</span></span></td>
<td><span data-ttu-id="fee39-772"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>EP-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-772"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> EP-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-773">Windows Server 2012 R2、以下を含む:</span><span class="sxs-lookup"><span data-stu-id="fee39-773">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="fee39-774">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="fee39-774">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-775">Microsoft SQL Server 2012 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-775">Microsoft SQL Server 2012 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-776">フル テキスト検索</span><span class="sxs-lookup"><span data-stu-id="fee39-776">Full-text Search</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-777">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="fee39-777">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="fee39-778">AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-778">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-779">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-779">Server components:</span></span>
<ul>
<li><span data-ttu-id="fee39-780">Web サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-780">Web server components:</span></span>
<ul>
<li><span data-ttu-id="fee39-781">エンタープライズ ポータル (EP)</span><span class="sxs-lookup"><span data-stu-id="fee39-781">Enterprise Portal (EP)</span></span></li>
<li><span data-ttu-id="fee39-782">エンタープライズ検索</span><span class="sxs-lookup"><span data-stu-id="fee39-782">Enterprise Search</span></span></li>
<li><span data-ttu-id="fee39-783">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-783">Help Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="fee39-784">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-784">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="fee39-785">Management Reporter サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="fee39-785">Management Reporter server components</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-786">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-786">Retail components:</span></span>
<ul>
<li><span data-ttu-id="fee39-787">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-787">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="fee39-788">Async Client</span><span class="sxs-lookup"><span data-stu-id="fee39-788">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-789">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-789">Retail Server</span></span></li>
<li><span data-ttu-id="fee39-790">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="fee39-790">Retail Online Channel</span></span></li>
<li><span data-ttu-id="fee39-791">Retail チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="fee39-791">Retail Channel Database</span></span></li>
<li><span data-ttu-id="fee39-792">Retail チャンネル コンフィギュレーション ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="fee39-792">Retail Channel Configuration Utility</span></span></li>
<li><span data-ttu-id="fee39-793">Retail ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="fee39-793">Retail Hardware Station</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-794">倉庫モバイル デバイス ポータル</span><span class="sxs-lookup"><span data-stu-id="fee39-794">Warehouse Mobile Devices Portal</span></span></li>
<li><span data-ttu-id="fee39-795">Microsoft Dynamics Connector</span><span class="sxs-lookup"><span data-stu-id="fee39-795">Connector for Microsoft Dynamics</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fee39-796">2</span><span class="sxs-lookup"><span data-stu-id="fee39-796">2</span></span></td>
<td><span data-ttu-id="fee39-797">クライアント コンピューター</span><span class="sxs-lookup"><span data-stu-id="fee39-797">Client computer</span></span></td>
<td><span data-ttu-id="fee39-798"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>CLI-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-798"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> CLI-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-799">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fee39-799">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="fee39-800">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="fee39-800">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="fee39-801">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-801">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-802">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="fee39-802">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-803">Microsoft SharePoint Server 2013 クライアント コンポーネント SDK</span><span class="sxs-lookup"><span data-stu-id="fee39-803">Microsoft SharePoint Server 2013 Client Components SDK</span></span></li>
<li><span data-ttu-id="fee39-804">Microsoft Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="fee39-804">Microsoft Office 365 ProPlus</span></span></li>
<li><span data-ttu-id="fee39-805">AX 2012 R3 または AX 2012 R3 CU8 コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-805">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="fee39-806">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-806">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="fee39-807">Management Reporter レポート デザイナー</span><span class="sxs-lookup"><span data-stu-id="fee39-807">Management Reporter Report Designer</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-808">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-808">Client components:</span></span>
<ul>
<li><span data-ttu-id="fee39-809">クライアント</span><span class="sxs-lookup"><span data-stu-id="fee39-809">Client</span></span></li>
<li><span data-ttu-id="fee39-810">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="fee39-810">Office add-ins</span></span></li>
<li><span data-ttu-id="fee39-811">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="fee39-811">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-812">開発者ツール:</span><span class="sxs-lookup"><span data-stu-id="fee39-812">Developer tools:</span></span>
<ul>
<li><span data-ttu-id="fee39-813">デバッガー</span><span class="sxs-lookup"><span data-stu-id="fee39-813">Debugger</span></span></li>
<li><span data-ttu-id="fee39-814">Visual Studio Tools</span><span class="sxs-lookup"><span data-stu-id="fee39-814">Visual Studio Tools</span></span></li>
<li><span data-ttu-id="fee39-815">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="fee39-815">Trace Parser</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-816">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="fee39-816">Management utilities</span></span></li>
<li><span data-ttu-id="fee39-817">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="fee39-817">Retail components:</span></span>
<ul>
<li><span data-ttu-id="fee39-818">Retail POS</span><span class="sxs-lookup"><span data-stu-id="fee39-818">Retail POS</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fee39-819">2</span><span class="sxs-lookup"><span data-stu-id="fee39-819">2</span></span></td>
<td><span data-ttu-id="fee39-820">リモート デスクトップ サービス サーバー</span><span class="sxs-lookup"><span data-stu-id="fee39-820">Remote Desktop Services server</span></span></td>
<td><span data-ttu-id="fee39-821"><strong>サイズ:</strong>D3: 標準計算層 (4 コア、14 GB メモリ) <strong>既定名:</strong>RDS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="fee39-821"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)<strong>Default name:</strong> RDS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="fee39-822">Windows Server 2012 R2、以下を含む:</span><span class="sxs-lookup"><span data-stu-id="fee39-822">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="fee39-823">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="fee39-823">Internet Information Services (IIS)</span></span></li>
<li><span data-ttu-id="fee39-824">リモート デスクトップ サービス</span><span class="sxs-lookup"><span data-stu-id="fee39-824">Remote Desktop Services</span></span></li>
</ul></li>
<li><span data-ttu-id="fee39-825">Microsoft SQL Server 2012 Native Client</span><span class="sxs-lookup"><span data-stu-id="fee39-825">Microsoft SQL Server 2012 Native Client</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="next-steps"></a><span data-ttu-id="fee39-826">次のステップ</span><span class="sxs-lookup"><span data-stu-id="fee39-826">Next steps</span></span>
- [<span data-ttu-id="fee39-827">Azure に AX 2012 R3 または AX 2012 R3 CU8 デモ環境を配置する</span><span class="sxs-lookup"><span data-stu-id="fee39-827">Deploy an AX 2012 R3 or AX 2012 R3 CU8 demo environment on Azure</span></span>](deploy-ax-2012-r3-ax-2012-r3-cu8-demo-environment-azure.md) 
- [<span data-ttu-id="fee39-828">Azure での Retail Essentials デモ環境の配置</span><span class="sxs-lookup"><span data-stu-id="fee39-828">Deploy a Retail essentials demo environment on Azure</span></span>](deploy-retail-essentials-demo-environment-azure.md) 
- [<span data-ttu-id="fee39-829">Azure での開発環境の配置</span><span class="sxs-lookup"><span data-stu-id="fee39-829">Deploy a development environment on Azure</span></span>](deploy-development-environment-azure.md) 
- [<span data-ttu-id="fee39-830">Azure でのテスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="fee39-830">Deploy a test environment on Azure</span></span>](deploy-test-environment-azure.md) 
- [<span data-ttu-id="fee39-831">Azure での Retail Essentials 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="fee39-831">Deploy a Retail essentials dev/test environment on Azure</span></span>](deploy-retail-essentials-devtest-environment-azure.md) 
- [<span data-ttu-id="fee39-832">Azure での Retail E-commerce 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="fee39-832">Deploy a Retail e-commerce dev/test environment on Azure</span></span>](deploy-retail-ecommerce-devtest-environment-azure.md) 
- [<span data-ttu-id="fee39-833">Azure での Retail Mobility 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="fee39-833">Deploy a Retail mobility dev/test environment on Azure</span></span>](deploy-retail-mobility-devtest-environment-azure.md) 
- [<span data-ttu-id="fee39-834">Azure に高可用性環境を配置する</span><span class="sxs-lookup"><span data-stu-id="fee39-834">Deploy a high availability environment on Azure</span></span>](deploy-high-availability-environment-azure.md)

