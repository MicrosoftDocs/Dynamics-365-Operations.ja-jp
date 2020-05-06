---
title: Azure 上での AX 2012 R3の 配置計画
description: Microsoft Azure に Microsoft Dynamics AX 2012 R3 を展開する前に、いくつかの点を考慮し決定する必要があります。 この記事では、計画プロセスについて説明します。
author: kfend
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 4f5ea1ad7430c353e72c3232e472df6286b458b3
ms.sourcegitcommit: 990dd96d1dcd462928aa0029ff84a8185198e5de
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2020
ms.locfileid: "3287839"
---
# <a name="plan-ax-2012-r3-deployments-on-azure"></a><span data-ttu-id="42d60-104">Azure 上での AX 2012 R3の 配置計画</span><span class="sxs-lookup"><span data-stu-id="42d60-104">Plan AX 2012 R3 deployments on Azure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42d60-105">Microsoft Azure に Microsoft Dynamics AX 2012 R3 を展開する前に、いくつかの点を考慮し決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-105">Before you can deploy Microsoft Dynamics AX 2012 R3 on Microsoft Azure, there are several things you must consider and decisions you must make.</span></span> <span data-ttu-id="42d60-106">この記事では、計画プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="42d60-106">This article guides you through the planning process.</span></span> 

<span data-ttu-id="42d60-107">Azure 上の AX 2012 R3 の配備は、Microsoft が次のシナリオでサポートしています。</span><span class="sxs-lookup"><span data-stu-id="42d60-107">Deployments of AX 2012 R3 on Azure are supported by Microsoft in the following scenarios:</span></span> 
- <span data-ttu-id="42d60-108">配置は、Microsoft Dynamics Lifecycle Services (LCS) を通じて実行されています。</span><span class="sxs-lookup"><span data-stu-id="42d60-108">The deployment has been performed through Microsoft Dynamics Lifecycle Services (LCS).</span></span> 
- <span data-ttu-id="42d60-109">以下のガイダンスに厳密に従って実施された顧客またはパートナー主導配置。</span><span class="sxs-lookup"><span data-stu-id="42d60-109">Customer or partner-driven deployments that have been performed strictly adhering to the following guidance:</span></span> 
   - <span data-ttu-id="42d60-110">SQL は、(SQL クラスタリング/Always On を使用して) 可用性トポロジに配置されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-110">SQL is deployed in a High Availability topology (using SQL Clustering/Always On).</span></span>
   - <span data-ttu-id="42d60-111">Azure に配置するために、[Azure 仮想マシンでの SQL Server のパフォーマンス ベスト プラクティス](/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)を使用して、SQL のベスト プラクティスに従っています。</span><span class="sxs-lookup"><span data-stu-id="42d60-111">SQL best practices have been followed for deployment in Azure, using the [Performance best practices for SQL Server in Azure Virtual Machines](/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance).</span></span> 
   - <span data-ttu-id="42d60-112">[SQL サーバーおよび記憶域の設定のコンフィギュレーション (TechNet)](https://technet.microsoft.com/library/dd309734.aspx) によって指定された AX 2012 の SQL Server コンフィギュレーションのベスト プラクティスに従っています。</span><span class="sxs-lookup"><span data-stu-id="42d60-112">Best practices for SQL Server configuration for AX 2012 have been followed, as specified in [Configure SQL Server and storage settings (TechNet)](https://technet.microsoft.com/library/dd309734.aspx).</span></span> 
   - <span data-ttu-id="42d60-113">[Lifecycle Services (LCS) のシステム診断](system-diagnostics-lcs.md) で指定されているように、システム診断ツールがインストールされ、ベスト プラクティスに従います。</span><span class="sxs-lookup"><span data-stu-id="42d60-113">The System diagnostic tool is installed and best practices are followed, as specified in [System diagnostics in Lifecycle Services (LCS)](system-diagnostics-lcs.md)</span></span> 

> [!NOTE]
> <span data-ttu-id="42d60-114">Azure 環境でサポートされていない AX 2012 R3 に問題があり、LCS 経由で Azure に展開された、またはローカルに展開された AX 2012 R3 環境で同じ問題を再現することができる場合、Microsoft がサポートを提供できます。</span><span class="sxs-lookup"><span data-stu-id="42d60-114">If you have an issue in an unsupported AX 2012 R3 on Azure environment, and can reproduce the same issue in an AX 2012 R3 environment that was either deployed to Azure through LCS, or deployed locally, Microsoft can provide support.</span></span>
> 
> <span data-ttu-id="42d60-115">AX 2012 R3 は、オンプレミスでも配置できます。</span><span class="sxs-lookup"><span data-stu-id="42d60-115">AX 2012 R3 can also be deployed on-premises.</span></span> <span data-ttu-id="42d60-116">詳細については、[Microsoft Dynamics AX 2012 のインストール](https://technet.microsoft.com/library/dd362138.aspx) のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-116">For details, see the topic [Install Microsoft Dynamics AX 2012](https://technet.microsoft.com/library/dd362138.aspx).</span></span>

## <a name="verify-that-you-can-log-on-to-lifecycle-services"></a><span data-ttu-id="42d60-117">Lifecycle Services にログオンできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="42d60-117">Verify that you can log on to Lifecycle Services</span></span>
<span data-ttu-id="42d60-118">Lifecycle Services (LCS) は、顧客およびパートナーが Microsoft Dynamics AX プロジェクトの管理に使用できるクラウドベースの共同ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="42d60-118">Lifecycle Services (LCS) is a cloud-based collaborative workspace that customers and partners can use to manage Microsoft Dynamics AX projects.</span></span> <span data-ttu-id="42d60-119">Azure 上に AX 2012 R3 を配置するには、Lifecycle Services Web サイトで利用できるクラウド ホスト環境ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="42d60-119">You’ll use the Cloud-hosted environments tool, available on the Lifecycle Services website, to deploy AX 2012 R3 on Azure.</span></span> <span data-ttu-id="42d60-120">Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="42d60-120">Lifecycle Services is available to customers and partners as part of their support plans.</span></span> <span data-ttu-id="42d60-121">CustomerSource または PartnerSource の資格情報でアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-121">You can access it with your CustomerSource or PartnerSource credentials.</span></span> [<span data-ttu-id="42d60-122">Lifecycle Services にログオンできることを確認する</span><span class="sxs-lookup"><span data-stu-id="42d60-122">Verify that you can log on to Lifecycle Services</span></span>](https://lcs.dynamics.com/)

## <a name="purchase-an-azure-subscription"></a><span data-ttu-id="42d60-123">Azure サブスクリプションの購買</span><span class="sxs-lookup"><span data-stu-id="42d60-123">Purchase an Azure subscription</span></span>
<span data-ttu-id="42d60-124">Azure を使用するには、サブスクリプションを購入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-124">To use Azure, you must purchase a subscription.</span></span> <span data-ttu-id="42d60-125">サブスクリプション プランおよび価格決定の詳細については、[Azure 価格決定](https://azure.microsoft.com/pricing/) ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-125">For information about subscription plans and pricing details, see the [Azure pricing](https://azure.microsoft.com/pricing/) page.</span></span> <span data-ttu-id="42d60-126">その後、そのページの指示に従ってサブスクリプションを購入します。</span><span class="sxs-lookup"><span data-stu-id="42d60-126">Then follow the instructions on that page to purchase a subscription.</span></span> <span data-ttu-id="42d60-127">サブスクリプションは、Azure に配備する AX 2012 R3 環境をサポートするのに十分な大きさでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="42d60-127">The subscription must be large enough to support the AX 2012 R3 environment that you want to deploy on Azure.</span></span> <span data-ttu-id="42d60-128">次のテーブルは、Azure に配置できる AX 2012 R3 環境のタイプと、各環境を既定のコンフィギュレーションで配置するために必要なコアの数を示しています。</span><span class="sxs-lookup"><span data-stu-id="42d60-128">The following table lists the types of AX 2012 R3 environments that you can deploy on Azure, and the number of cores required to deploy each environment in its default configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="42d60-129">環境を配置するときに、配置される仮想マシンの数とサイズを変更できることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-129">Keep in mind that when you deploy an environment, you can change the number and size of the virtual machines that are deployed.</span></span> <span data-ttu-id="42d60-130">ただし、次のテーブルでは、その*既定*コンフィギュレーションで各環境を配置するために必要なコアの数を一覧にします。</span><span class="sxs-lookup"><span data-stu-id="42d60-130">However, this table lists the number of cores required to deploy each environment in its *default* configuration.</span></span>

<span data-ttu-id="42d60-131">**環境タイプ:** - デモ</span><span class="sxs-lookup"><span data-stu-id="42d60-131">**Environment type:** - Demo</span></span>


| <span data-ttu-id="42d60-132">環境名</span><span class="sxs-lookup"><span data-stu-id="42d60-132">Environment name</span></span>       | <span data-ttu-id="42d60-133">既定の構成で環境を配置するコアの数</span><span class="sxs-lookup"><span data-stu-id="42d60-133">Number of cores to deploy the environment in its default configuration</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="42d60-134">AX 2012 R3 デモ</span><span class="sxs-lookup"><span data-stu-id="42d60-134">AX 2012 R3 demo</span></span>        | <span data-ttu-id="42d60-135">8 コア</span><span class="sxs-lookup"><span data-stu-id="42d60-135">8 cores</span></span>                                                                |
| <span data-ttu-id="42d60-136">AX 2012 R3 CU8 デモ</span><span class="sxs-lookup"><span data-stu-id="42d60-136">AX 2012 R3 CU8 demo</span></span>    | <span data-ttu-id="42d60-137">8 コア</span><span class="sxs-lookup"><span data-stu-id="42d60-137">8 cores</span></span>                                                                |
| <span data-ttu-id="42d60-138">Retail Essentials デモ</span><span class="sxs-lookup"><span data-stu-id="42d60-138">Retail essentials demo</span></span> | <span data-ttu-id="42d60-139">8 コア</span><span class="sxs-lookup"><span data-stu-id="42d60-139">8 cores</span></span>                                                                |


<span data-ttu-id="42d60-140">**環境タイプ:** - 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="42d60-140">**Environment type:** - Dev/test</span></span>


| <span data-ttu-id="42d60-141">環境名</span><span class="sxs-lookup"><span data-stu-id="42d60-141">Environment name</span></span>                   | <span data-ttu-id="42d60-142">既定の構成で環境を配置するコアの数</span><span class="sxs-lookup"><span data-stu-id="42d60-142">Number of cores to deploy the environment in its default configuration</span></span> |
|------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="42d60-143">開発</span><span class="sxs-lookup"><span data-stu-id="42d60-143">Development</span></span>                        | <span data-ttu-id="42d60-144">9 コア</span><span class="sxs-lookup"><span data-stu-id="42d60-144">9 cores</span></span>                                                                |
| <span data-ttu-id="42d60-145">共有 SQL Server による開発</span><span class="sxs-lookup"><span data-stu-id="42d60-145">Development with shared SQL Server</span></span> | <span data-ttu-id="42d60-146">14 コア</span><span class="sxs-lookup"><span data-stu-id="42d60-146">14 cores</span></span>                                                               |
| <span data-ttu-id="42d60-147">テスト</span><span class="sxs-lookup"><span data-stu-id="42d60-147">Test</span></span>                               | <span data-ttu-id="42d60-148">13 コア</span><span class="sxs-lookup"><span data-stu-id="42d60-148">13 cores</span></span>                                                               |
| <span data-ttu-id="42d60-149">Retail Essentials 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="42d60-149">Retail essentials dev/test</span></span>         | <span data-ttu-id="42d60-150">4 コア</span><span class="sxs-lookup"><span data-stu-id="42d60-150">4 cores</span></span>                                                                |
| <span data-ttu-id="42d60-151">Retail E-commerce 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="42d60-151">Retail e-commerce dev/test</span></span>         | <span data-ttu-id="42d60-152">4 コア</span><span class="sxs-lookup"><span data-stu-id="42d60-152">4 cores</span></span>                                                                |
| <span data-ttu-id="42d60-153">Retail Mobility 開発/テスト</span><span class="sxs-lookup"><span data-stu-id="42d60-153">Retail mobility dev/test</span></span>           | <span data-ttu-id="42d60-154">4 コア</span><span class="sxs-lookup"><span data-stu-id="42d60-154">4 cores</span></span>                                                                |


<span data-ttu-id="42d60-155">**環境タイプ:** - 高可用性</span><span class="sxs-lookup"><span data-stu-id="42d60-155">**Environment type:** - High availability</span></span>


| <span data-ttu-id="42d60-156">環境名</span><span class="sxs-lookup"><span data-stu-id="42d60-156">Environment name</span></span>              | <span data-ttu-id="42d60-157">既定の構成で環境を配置するコアの数</span><span class="sxs-lookup"><span data-stu-id="42d60-157">Number of cores to deploy the environment in its default configuration</span></span> |
|-------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="42d60-158">高可用性環境</span><span class="sxs-lookup"><span data-stu-id="42d60-158">High availability environment</span></span> | <span data-ttu-id="42d60-159">45 コア</span><span class="sxs-lookup"><span data-stu-id="42d60-159">45 cores</span></span>                                                               |


<span data-ttu-id="42d60-160">Azure のサブスクリプションを既に持っている場合、次に注意します。</span><span class="sxs-lookup"><span data-stu-id="42d60-160">If you already have an Azure subscription, note the following:</span></span>

-   <span data-ttu-id="42d60-161">**定期売買のサイズを表示する:** Azure 管理ポータルで、定期売買のサイズを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-161">**To view the size of your subscription:** You can view the size of your subscription in the Azure management portal.</span></span> <span data-ttu-id="42d60-162">これを行うには、[[Azure管理ポータル](https://manage.windowsazure.com/)] にログオンし、**設定**&gt;**使用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d60-162">To do so, log on to the [Azure management portal](https://manage.windowsazure.com/), and then click **Settings** &gt; **Usage**.</span></span>
-   <span data-ttu-id="42d60-163">**定期購読のサイズを増やす:** 定期売買のサイズを増やすには、Azure サポート チームにてサポート チケットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-163">**To increase the size of your subscription:** To increase the size of your subscription, you’ll need to create a support ticket with the Azure support team.</span></span> <span data-ttu-id="42d60-164">これを行うには、[[Azure サポート オプション](https://azure.microsoft.com/support/options/)] ページに移動し、**サポートを受ける** をクリックしてサポート チケットを作成します。</span><span class="sxs-lookup"><span data-stu-id="42d60-164">To do so, go to the [Azure support options](https://azure.microsoft.com/support/options/) page, and then click **Get Support** to create the support ticket.</span></span> <span data-ttu-id="42d60-165">サポート チケットを作成するとき、チケットが課金サポートに対応していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="42d60-165">When creating the support ticket, be sure to indicate that the ticket is for billing support.</span></span>

> [!NOTE]
> <span data-ttu-id="42d60-166">クラウド ソリューション プロバイダー (CSP) プログラムは、Azure Resource Manager (ARM) 要件のため Lifecycle Services によって現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="42d60-166">The Cloud Solution Provider (CSP) program is currently not supported with Lifecycle Services due to the Azure Resource Manager (ARM) requirement.</span></span>

## <a name="purchase-and-azure-support-plan"></a><span data-ttu-id="42d60-167">発注書および Azure サポート計画</span><span class="sxs-lookup"><span data-stu-id="42d60-167">Purchase and Azure support plan</span></span>
<span data-ttu-id="42d60-168">Azure サポート計画では Azure の技術および課金サポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="42d60-168">Azure support plans provide technical and billing support for Azure.</span></span> <span data-ttu-id="42d60-169">Azure サポート プランは、Azure 展開のサポーの適切なレベルを選択できる柔軟なサポート オプションを提供しています。</span><span class="sxs-lookup"><span data-stu-id="42d60-169">The Azure support plans offer flexible support options that will allow you to select the right level of support for your Azure deployment.</span></span> <span data-ttu-id="42d60-170">サポート オプションには、Azure サブスクリプションに含まれているサポート サービスから、無料のサポート サービスまでさまざまです。</span><span class="sxs-lookup"><span data-stu-id="42d60-170">The support options range from support services included with your Azure subscription at no charge to premier support services.</span></span> <span data-ttu-id="42d60-171">利用可能なサポート プランについて学び、プランを購入するには、[[Azure サポート計画](https://www.windowsazure.com/support/plans/)] ページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="42d60-171">To learn about the available support plans and to purchase a plan, see the [Azure support plans](https://www.windowsazure.com/support/plans/) page.</span></span>

## <a name="become-familiar-with-the-azure-management-portal"></a><span data-ttu-id="42d60-172">Azure 管理ポータルを使いこなせるようになります</span><span class="sxs-lookup"><span data-stu-id="42d60-172">Become familiar with the Azure management portal</span></span>
<span data-ttu-id="42d60-173">Azure 管理ポータルは、開発者および IT プロフェッショナルに、その Azure コンポーネントをプロビジョニング、構成、監視、および管理する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="42d60-173">The Azure management portal provides developers and IT professionals the ability to provision, configure, monitor, and manage their Azure components.</span></span> <span data-ttu-id="42d60-174">今後使用するために、管理ポータルについてよく理解しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="42d60-174">It’s important to become familiar with the management portal because you’ll use it to:</span></span>

-   <span data-ttu-id="42d60-175">管理証明書をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="42d60-175">Upload a management certificate.</span></span> <span data-ttu-id="42d60-176">(管理証明書を使用すると、Lifecycle Services はユーザーに代わって Azure に AX 2012 R3 環境を配置できます。)</span><span class="sxs-lookup"><span data-stu-id="42d60-176">(The management certificate enables Lifecycle Services to deploy AX 2012 R3 environments on Azure on your behalf.)</span></span>
-   <span data-ttu-id="42d60-177">仮想マシンに接続します。</span><span class="sxs-lookup"><span data-stu-id="42d60-177">Connect to virtual machines.</span></span>
-   <span data-ttu-id="42d60-178">AX 2012 R3 環境の正常性および状態を監視します。</span><span class="sxs-lookup"><span data-stu-id="42d60-178">Monitor the health and status of your AX 2012 R3 environment.</span></span>

<span data-ttu-id="42d60-179">Azure サブスクリプションを購入した後、 [ここ](https://manage.windowsazure.com/?whr=live.com) をクリックして管理ポータルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="42d60-179">After you purchase an Azure subscription, you can access the management portal by clicking [here](https://manage.windowsazure.com/?whr=live.com).</span></span> <span data-ttu-id="42d60-180">次の図は、管理ポータルを示しています。</span><span class="sxs-lookup"><span data-stu-id="42d60-180">The following image shows the management portal.</span></span> <span data-ttu-id="42d60-181">[![PlanYouAXR3DeploymentonAzure1](./media/planyouaxr3deploymentonazure1.jpg)](./media/planyouaxr3deploymentonazure1.jpg)</span><span class="sxs-lookup"><span data-stu-id="42d60-181">[![PlanYouAXR3DeploymentonAzure1](./media/planyouaxr3deploymentonazure1.jpg)](./media/planyouaxr3deploymentonazure1.jpg)</span></span>  

## <a name="become-familiar-with-the-azure-vm-agent"></a><span data-ttu-id="42d60-182">Azure VM エージェントを使いこなせるようになります</span><span class="sxs-lookup"><span data-stu-id="42d60-182">Become familiar with the Azure VM agent</span></span>
<span data-ttu-id="42d60-183">Azure VM エージェントは、Lifecycle Services を通じて展開されたすべての VM で自動的に配置されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-183">The Azure VM Agent is now automatically deployed with every VM deployed via Lifecycle Services.</span></span> <span data-ttu-id="42d60-184">Azure VM エージェントは、Azure 仮想マシン拡張 (VM 拡張) インストール、コンフィギュレーション、管理、実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-184">The Azure VM Agent is used to install, configure, manage and run Azure Virtual Machine Extensions (VM Extensions).</span></span> <span data-ttu-id="42d60-185">VM 拡張機能は、VM を監視および管理するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="42d60-185">VM extensions can help you monitor and manage your VMs.</span></span>

## <a name="consider-cloud-services-resource-requirements"></a><span data-ttu-id="42d60-186">クラウド サービスのリソース要件を検討する</span><span class="sxs-lookup"><span data-stu-id="42d60-186">Consider Cloud Services resource requirements</span></span>
<span data-ttu-id="42d60-187">トポロジが配置されると、配置システムは選択された仮想マシン (VM) の SKU を検査します。</span><span class="sxs-lookup"><span data-stu-id="42d60-187">When a topology is deployed, the deployment system will inspect the virtual machine (VM) SKUs that were selected.</span></span> <span data-ttu-id="42d60-188">Azure がこれらの VM を VM が使用可能である適切なクラスターに配置していることを確認するために、VM SKU の各レベルに独自の Azure クラウド サービスが必要です。</span><span class="sxs-lookup"><span data-stu-id="42d60-188">In order to ensure that Azure deploys these VMs to the proper clusters where the VMs are available, each level of VM SKU must have its own Azure Cloud Service.</span></span> <span data-ttu-id="42d60-189">VM SKU の内訳は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="42d60-189">The VM SKU breakdown is as follows:</span></span>

|         |                                 |
|---------|---------------------------------|
| <span data-ttu-id="42d60-190">**最小在庫管理単位**</span><span class="sxs-lookup"><span data-stu-id="42d60-190">**SKU**</span></span> | <span data-ttu-id="42d60-191">**サイズ**</span><span class="sxs-lookup"><span data-stu-id="42d60-191">**Size**</span></span>                        |
| <span data-ttu-id="42d60-192">A</span><span class="sxs-lookup"><span data-stu-id="42d60-192">A</span></span>       | <span data-ttu-id="42d60-193">標準 A の \[A0-A4\]</span><span class="sxs-lookup"><span data-stu-id="42d60-193">Standard A’s \[A0-A4\]</span></span>          |
| <span data-ttu-id="42d60-194">午前</span><span class="sxs-lookup"><span data-stu-id="42d60-194">AM</span></span>      | <span data-ttu-id="42d60-195">標準 A の \[A5-A7\]</span><span class="sxs-lookup"><span data-stu-id="42d60-195">Standard A's \[A5-A7\]</span></span>          |
| <span data-ttu-id="42d60-196">AL</span><span class="sxs-lookup"><span data-stu-id="42d60-196">AL</span></span>      | <span data-ttu-id="42d60-197">標準 A の (大) \[A8-A11\]</span><span class="sxs-lookup"><span data-stu-id="42d60-197">Standard A’s (large) \[A8-A11\]</span></span> |
| <span data-ttu-id="42d60-198">D</span><span class="sxs-lookup"><span data-stu-id="42d60-198">D</span></span>       | <span data-ttu-id="42d60-199">標準 D の\[すべての D シリーズ\]</span><span class="sxs-lookup"><span data-stu-id="42d60-199">Standard D’s \[all D series\]</span></span>   |
| <span data-ttu-id="42d60-200">DS</span><span class="sxs-lookup"><span data-stu-id="42d60-200">DS</span></span>      | <span data-ttu-id="42d60-201">標準 DS の\[すべての DS シリーズ\]</span><span class="sxs-lookup"><span data-stu-id="42d60-201">Standard DS’s \[all DS series\]</span></span> |
| <span data-ttu-id="42d60-202">G</span><span class="sxs-lookup"><span data-stu-id="42d60-202">G</span></span>       | <span data-ttu-id="42d60-203">標準 G の\[すべての G シリーズ\]</span><span class="sxs-lookup"><span data-stu-id="42d60-203">Standard G’s \[all G series\]</span></span>   |

<span data-ttu-id="42d60-204">次の名前付けスキームを含むクラウド サービスが作成されます: Version-Topology-EnvironmentName-SKU-GUID</span><span class="sxs-lookup"><span data-stu-id="42d60-204">A Cloud Service will be created with the following naming scheme: Version-Topology-EnvironmentName-SKU-GUID</span></span> 

<span data-ttu-id="42d60-205">必要に応じて、配置のためのクラウド サービス リソース要件を検討し、Azure サポートから Azure サブスクリプションの追加クラウド サービス キャパシティを要求してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-205">Please consider the Cloud Services resource requirements for your deployments and request additional Cloud Services capacity in your Azure Subscription from Azure Support if necessary.</span></span>

## <a name="plan-for-storage-accounts"></a><span data-ttu-id="42d60-206">ストレージ アカウントの計画</span><span class="sxs-lookup"><span data-stu-id="42d60-206">Plan for storage accounts</span></span>
<span data-ttu-id="42d60-207">Lifecycle Services で作成された各プロジェクトについては、1 つまたは複数の個別のストレージ アカウントが Azure 定期売買で作成されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-207">For each project created in Lifecycle Services, one or more distinct storage accounts will be created in the Azure subscription.</span></span> <span data-ttu-id="42d60-208">ストレージ アカウントは、プロジェクトを Azure サブスクリプションに接続すると作成されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-208">A storage account is created when you connect your project to your Azure subscription.</span></span> <span data-ttu-id="42d60-209">このストレージ アカウントは、ローカル冗長ストレージ (LRS) アカウントであり、展開に必要なスクリプトと VHD を格納するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-209">This storage account is a Locally Redundant Storage (LRS) account, and is used to house scripts and VHDs which are required for deployments.</span></span> <span data-ttu-id="42d60-210">最初の Premium ストレージ有効トポロジがプロジェクトから配置されると、各プロジェクトが作成され Premium ストレージ アカウントが追加されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-210">An additional Premium storage account is created for each project when the first Premium storage-enabled topology is deployed from the project.</span></span> <span data-ttu-id="42d60-211">ストレージ アカウントは、配置が同じ Azure サブスクリプションに行われる場合でも、Lifecycle Services プロジェクト間で共有されません。</span><span class="sxs-lookup"><span data-stu-id="42d60-211">Storage accounts are not shared across Lifecycle Services projects, even if the deployments are to the same Azure subscription.</span></span> <span data-ttu-id="42d60-212">Premium ストレージ アカウントが作成されると、それもまた LRS として作成されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-212">When a Premium storage account is created, it too is created as LRS.</span></span> <span data-ttu-id="42d60-213">ストレージの詳細については、[ここ](https://azure.microsoft.com/pricing/details/storage) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="42d60-213">For more information about storage, click [here](https://azure.microsoft.com/pricing/details/storage).</span></span> <span data-ttu-id="42d60-214">同じ Lifecycle Services (LCS) プロジェクトと Azure コネクタに展開されるトポロジと環境の数を検討します。</span><span class="sxs-lookup"><span data-stu-id="42d60-214">Consider which topologies and the number of environments that will be deployed into the same Lifecycle Services (LCS) project and Azure Connector.</span></span> <span data-ttu-id="42d60-215">Premium ストレージ アカウントとは別に、既定では、LCS プロジェクトおよび Azure コネクタごとにストレージ アカウントが 1 つ存在します。</span><span class="sxs-lookup"><span data-stu-id="42d60-215">Premium storage account aside, by default there is 1 storage account for each LCS project and Azure Connector.</span></span> <span data-ttu-id="42d60-216">Azure Storage には[限度](https://azure.microsoft.com/documentation/articles/azure-subscription-service-limits/#storage-limits)があるので注意してください。具体的には、標準ストレージ アカウントあたり 20,000 IOPS (秒単位の入力/出力オペレーション) です。</span><span class="sxs-lookup"><span data-stu-id="42d60-216">Be aware that Azure storage has [limits](https://azure.microsoft.com/documentation/articles/azure-subscription-service-limits/#storage-limits), specifically 20,000 IOPS (input/output operations per second) per standard storage account.</span></span> <span data-ttu-id="42d60-217">VHD あたり 500 IOPS と組み合わせると、調整が発生する前に約 40 個の***利用効率が高い*** VHDが残されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-217">Combined with 500 IOPS per VHD, that leaves roughly 40 ***highly utilized*** VHDs before throttling occurs.</span></span> <span data-ttu-id="42d60-218">これを軽減するには、複数の Azure コネクタや複数の LCS プロジェクトを活用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="42d60-218">To mitigate this, we recommend that you leverage multiple Azure Connectors and/or multiple LCS projects.</span></span> <span data-ttu-id="42d60-219">たとえば、1 つの LCS プロジェクトで製造環境を、別で開発/テスト環境を検討します。</span><span class="sxs-lookup"><span data-stu-id="42d60-219">For example, consider having production environments in one LCS project, and Dev/Test environments in another.</span></span> 

> [!NOTE]
> <span data-ttu-id="42d60-220">インストール VHD など、LCS が配置するすべての VHD が高度に使用されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="42d60-220">Not all VHDs that LCS deploys will be highly utilized, such as the installation VHD.</span></span>

## <a name="plan-your-sql-server-configuration"></a><span data-ttu-id="42d60-221">SQL Server 構成の計画</span><span class="sxs-lookup"><span data-stu-id="42d60-221">Plan your SQL Server configuration</span></span>
<span data-ttu-id="42d60-222">Azure Premium Storage は、Azure 仮想マシン (VM) 上で実行される I/O 集約型ワークロードに対して高パフォーマンス、待機時間が短いディスク サポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="42d60-222">Azure Premium Storage delivers high-performance, low-latency disk support for I/O intensive workloads running on Azure virtual machines (VMs).</span></span> <span data-ttu-id="42d60-223">Premium Storage では、アプリケーションは VM ごとに 32 TB までのストレージを持つことができ、VM ごとに 50,000 IOPS を達成し、読み取り操作での待機時間は非常に短くなります。</span><span class="sxs-lookup"><span data-stu-id="42d60-223">With Premium Storage, your applications can have up to 32 TB of storage per VM, achieve 50,000 IOPS per VM, and have extremely low latencies for read operations.</span></span> <span data-ttu-id="42d60-224">Premium Storage は、生産能力で使用される AX 2012 R3 配置に必要です。</span><span class="sxs-lookup"><span data-stu-id="42d60-224">Premium Storage is required for AX 2012 R3 deployments that will be used in a production capacity.</span></span> <span data-ttu-id="42d60-225">Azure DS シリーズ VM が選択されている場合、高可用性配置では Premium Storage が既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="42d60-225">Premium Storage is enabled by default for High Availability deployments when Azure DS-series VMs are selected.</span></span> <span data-ttu-id="42d60-226">Premium Storage は、現時点では DS シリーズ VM 上でのみ提供されています。</span><span class="sxs-lookup"><span data-stu-id="42d60-226">Premium Storage is only offered on DS-series VMs at this time.</span></span> <span data-ttu-id="42d60-227">他のすべての記憶域ニーズに非 Premium ストレージが使用されているとき、SQL Server AlwaysOn データベース サーバーだけで Premium Storage が有効になります。</span><span class="sxs-lookup"><span data-stu-id="42d60-227">Premium Storage is enabled exclusively for the SQL Server AlwaysOn database servers, while non-Premium storage is used for all other storage needs.</span></span> <span data-ttu-id="42d60-228">SQL Server AlwaysOn 可用性セットが作成されると、Lifecycle Services は、選択された DS シリーズ VM でサポートされているすべてのディスク スロットに対してディスクをアタッチします。</span><span class="sxs-lookup"><span data-stu-id="42d60-228">When a SQL Server AlwaysOn availability set is created, Lifecycle Services will attach a disk for every disk slot supported by the DS-series VM selected.</span></span> <span data-ttu-id="42d60-229">VM ディスク能力の詳細については、[ここ](https://msdn.microsoft.com/library/azure/dn197896.aspx) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d60-229">For more information about VM disk capacity, click [here](https://msdn.microsoft.com/library/azure/dn197896.aspx).</span></span> <span data-ttu-id="42d60-230">異なる VM サイズには、スループットと IOPS の最大値が変化します。</span><span class="sxs-lookup"><span data-stu-id="42d60-230">Different VM sizes will come with varying maximums for throughput and IOPS.</span></span> <span data-ttu-id="42d60-231">結果として、 SQL Server の構成を計画しているときは、ビジネスに最も効率的でコスト効果の良いソリューションを展開するために、これらの制限に精通してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-231">As a result, when you are planning your SQL Server configuration, please be familiar with these limitations to ensure that you are deploying the most efficient and cost effective solution for your business.</span></span> <span data-ttu-id="42d60-232">[Premium Storage: Azure 仮想マシン ワークロード向け高性能ストレージ](https://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/)に関するページ (特に、**Premium Storage の使用時の調整**に関するセッション) にあるガイドラインに従ってください。</span><span class="sxs-lookup"><span data-stu-id="42d60-232">Please follow the guidance found in [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/), particularly the section, **Throttling when using Premium Storage**.</span></span> <span data-ttu-id="42d60-233">SQL Server AlwaysOn 可用性セットは、Lifecycle Services を通じて自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-233">The SQL Server AlwaysOn availability set is created automatically through Lifecycle Services.</span></span> <span data-ttu-id="42d60-234">生産システムで使用するための高可用性トポロジを配置する前に、データおよびパフォーマンスのニーズを考慮することが重要です。</span><span class="sxs-lookup"><span data-stu-id="42d60-234">It is important to consider your data and performance needs before deploying a High Availability topology for use with a production system.</span></span> <span data-ttu-id="42d60-235">Azure Premium Storage については、[こちら](https://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="42d60-235">Please refer to Azure Premium Storage information [here](https://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/).</span></span> <span data-ttu-id="42d60-236">Premium Storage で配置を計画すると、高可用性トポロジには、原価とパフォーマンスの目標を達成するためのコンフィギュレーション オプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-236">Once you have planned your deployment with Premium Storage, the High Availability topology provides configuration options to help you achieve your cost and performance objectives.</span></span> <span data-ttu-id="42d60-237">高可用性のトポロジの詳細設定では、次の SQL Server 構成オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-237">Under Advanced Settings for the High Availability topology, the following SQL Server configuration options appear:</span></span>

-   <span data-ttu-id="42d60-238">**SQL Server イメージ コンフィギュレーションのカスタマイズ** - このオプションを使用すると、カスタム SQL Server Enterprise イメージまたは Azure Gallery SQL Server Enterprise イメージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="42d60-238">**Customize the SQL Server image configuration** – This option allows the use of a custom SQL Server Enterprise image or an Azure Gallery SQL Server Enterprise image.</span></span>
    -   <span data-ttu-id="42d60-239">カスタム SQL Server イメージ (既定) - このイメージには、SQL Server Enterprise 2014の試用版が含まれています。</span><span class="sxs-lookup"><span data-stu-id="42d60-239">Custom SQL Server image (default) – This image contains a trial edition of SQL Server Enterprise 2014.</span></span> <span data-ttu-id="42d60-240">評価版ライセンスは 3〜6 か月間有効です。</span><span class="sxs-lookup"><span data-stu-id="42d60-240">The trial license is enabled for 3-6 months.</span></span> <span data-ttu-id="42d60-241">既存の EA/etc. ライセンスを使用する場合は、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="42d60-241">Use this option if you want to use an existing EA/etc. license.</span></span>
    -   <span data-ttu-id="42d60-242">ギャラリー SQL Server イメージ – このイメージには SQL Server Enterprise 2014 が含まれており、消費に基づく Azure 価格決定を使用します。</span><span class="sxs-lookup"><span data-stu-id="42d60-242">Gallery SQL Server image – This image contains SQL Server Enterprise 2014 and uses consumption-based Azure pricing.</span></span> <span data-ttu-id="42d60-243">詳細については、[Azure 仮想マシンの価格決定](https://azure.microsoft.com/pricing/details/virtual-machines/#sql-server)ページと [Azure 仮想マシンの SQL Server](https://msdn.microsoft.com/library/azure/jj823132.aspx) で確認できます。</span><span class="sxs-lookup"><span data-stu-id="42d60-243">More information can be found on the [Azure Virtual Machines Pricing](https://azure.microsoft.com/pricing/details/virtual-machines/#sql-server) page and the [SQL Server in Azure Virtual Machines](https://msdn.microsoft.com/library/azure/jj823132.aspx)</span></span>
-   <span data-ttu-id="42d60-244">**SQL Server のストレージ領域コンフィギュレーションのカスタマイズ** - SQL Server VM に関連付けられるディスクの数とサイズを指定できます。</span><span class="sxs-lookup"><span data-stu-id="42d60-244">**Customize the SQL Server storage space configuration** – You can specify the number and size of the disks that will be attached to the SQL Server VMs.</span></span>

<span data-ttu-id="42d60-245">SQL Server 内でストレージ領域の作成に使用する必要があるディスクの数を指定する場合は、次の点に留意してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-245">Keep the following points in mind when specifying the number of disks that should be used to create the storage space within SQL Server:</span></span>

-   <span data-ttu-id="42d60-246">データベース サーバーのために選択されている VM サイズで、その VM SKU でサポートされるディスクの数が決まります。</span><span class="sxs-lookup"><span data-stu-id="42d60-246">The VM size that is selected for the database server dictates how many disks are supported by that VM SKU.</span></span> <span data-ttu-id="42d60-247">各 VM でサポートされているディスクの数に関する情報は、[ここ](https://msdn.microsoft.com/library/azure/dn197896.aspx)で確認できます。</span><span class="sxs-lookup"><span data-stu-id="42d60-247">Information about the number of disks that are supported by each VM can be found [here](https://msdn.microsoft.com/library/azure/dn197896.aspx).</span></span>
-   <span data-ttu-id="42d60-248">VM で使用可能なディスク スロットの 1 つは、Lifecycle Services 配置サービスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-248">One of the available disk slots on the VM will be used by the Lifecycle Services deployment service.</span></span> <span data-ttu-id="42d60-249">これは、VM の最大ディスク数 (マイナス1) が、使用可能なスロットを満たすことを意味します。</span><span class="sxs-lookup"><span data-stu-id="42d60-249">This means the VM’s maximum number of disks—minus 1—equals the available slots to fill.</span></span>
-   <span data-ttu-id="42d60-250">この設定を空白のままにすると、配置サービスによって VM でサポートされている最大までディスクを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-250">Leaving this setting blank will allow the deployment service to attach disks up to the maximum supported by the VM.</span></span> <span data-ttu-id="42d60-251">最大のディスクが使用される運用配置の場合にお勧めします。</span><span class="sxs-lookup"><span data-stu-id="42d60-251">It is recommended for production deployments that the maximum disks be used.</span></span>

<span data-ttu-id="42d60-252">VM に関連付けられている各ディスクのサイズ (GB 単位) を指定する場合、次の点に留意してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-252">Keep the following points in mind when specifying the size (in GB) of each disk attached to the VM:</span></span>

-   <span data-ttu-id="42d60-253">100 GB – 1024 GB 値を許可します。</span><span class="sxs-lookup"><span data-stu-id="42d60-253">Allowed values are 100 GB – 1024 GB.</span></span>
-   <span data-ttu-id="42d60-254">既定値は 128 GB です。</span><span class="sxs-lookup"><span data-stu-id="42d60-254">Default is 128 GB.</span></span>
-   <span data-ttu-id="42d60-255">使用されるディスクのサイズは、使用される Premium Storage 階層を決定します。</span><span class="sxs-lookup"><span data-stu-id="42d60-255">The size of the disk used dictates the Premium Storage tier used.</span></span>
-   <span data-ttu-id="42d60-256">Premium Storage 層は、原価、ディスクあたりの IPOPS、および展開されるシステムのスループットを示しています。</span><span class="sxs-lookup"><span data-stu-id="42d60-256">The Premium Storage tier dictates cost, IOPS per disk, and throughput of the system being deployed.</span></span> <span data-ttu-id="42d60-257">詳細については、[ここ](https://azure.microsoft.com/pricing/details/storage/) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="42d60-257">For more information, click [here](https://azure.microsoft.com/pricing/details/storage/).</span></span>
-   <span data-ttu-id="42d60-258">すべてのディスクは 64k クラスター サイズにフォーマットします。</span><span class="sxs-lookup"><span data-stu-id="42d60-258">All disks are formatted to 64k cluster size.</span></span> <span data-ttu-id="42d60-259">これにより、パフォーマンスが最大 20％ 向上します。</span><span class="sxs-lookup"><span data-stu-id="42d60-259">This results in up to a 20% increase in performance.</span></span> 

<span data-ttu-id="42d60-260">TempDB とログは、パフォーマンスの向上のために記憶域上に配置されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-260">TempDB and logs are deployed onto storage spaces as to benefit from the performance gains.</span></span> <span data-ttu-id="42d60-261">そのストレージ領域にコンフィギュレーションされているディスクの数に対して、1 つの仮想ディスクが作成されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-261">One virtual disk is created over the number of disks configured for the storage space.</span></span> <span data-ttu-id="42d60-262">次に、仮想ディスクは次のようにパーティション化されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-262">The virtual disk is then partitioned as follows:</span></span>

-   <span data-ttu-id="42d60-263">SQL データ = プールの合計サイズの 1/2</span><span class="sxs-lookup"><span data-stu-id="42d60-263">SQL data = 1/2 of the total size of pool</span></span>
-   <span data-ttu-id="42d60-264">SQL ログ = 合計サイズの 1/4</span><span class="sxs-lookup"><span data-stu-id="42d60-264">SQL logs = 1/4 of the total size</span></span>
-   <span data-ttu-id="42d60-265">SQL Temp db = 合計サイズの 1/8</span><span class="sxs-lookup"><span data-stu-id="42d60-265">SQL Temp db = 1/8 of the total size</span></span>
-   <span data-ttu-id="42d60-266">SQL バックアップ = 合計サイズの残り 1/8</span><span class="sxs-lookup"><span data-stu-id="42d60-266">SQL backup = remaining 1/8 of the total size</span></span>

<span data-ttu-id="42d60-267">他の考慮事項を念頭に置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-267">Other considerations to keep in mind:</span></span>

-   <span data-ttu-id="42d60-268">配置を計画するときは、対象とする Azure 領域で Premium Storage を使用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="42d60-268">When planning your deployment, ensure that Premium Storage is available in the Azure region you are targeting.</span></span> <span data-ttu-id="42d60-269">詳細については、[ここ](https://azure.microsoft.com/services/preview/) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="42d60-269">For more information, click [here](https://azure.microsoft.com/services/preview/).</span></span>
-   <span data-ttu-id="42d60-270">会社のネットワークと Azure の間で VPN/Express ルート接続 (または計画) がある場合、Premium ストレージ アカウントをサポートしている Azure 地域でこれが行われていることが確認します。</span><span class="sxs-lookup"><span data-stu-id="42d60-270">If you have a VPN/Express Route connection (or plan to) between your corporate network and Azure, please ensure this is done for an Azure region that supports Premium Storage.</span></span>
-   <span data-ttu-id="42d60-271">使用に関する制限について理解するためには [Azure Premium Storage ドキュメント](https://azure.microsoft.com/documentation/services/storage/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-271">Consult the [Azure Premium Storage documentation](https://azure.microsoft.com/documentation/services/storage/) to understand limitations of use.</span></span>
-   <span data-ttu-id="42d60-272">可用性トポロジーで非 Premium ストレージ VM がデプロイされている場合は、上記のすべての SQL Server のコンフィギュレーションを適用できますが、Premium ストレージのメリットは適用されません。</span><span class="sxs-lookup"><span data-stu-id="42d60-272">If non-Premium Storage VMs are deployed with the High Availability topologies, all of the above SQL Server configuration settings are applicable; however, Premium Storage benefits will not apply.</span></span>
-   <span data-ttu-id="42d60-273">配置ために Lifecycle Services プロジェクトを設定するとき、Premium Storage をサポートする地域を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-273">When setting up your Lifecycle Services project for deployment, you must select a region that supports Premium Storage.</span></span>

<span data-ttu-id="42d60-274">展開サービスにより実装される SQL Server ベスト プラクティスには、SQL Server チームにより推奨されるベスト プラクティスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="42d60-274">SQL Server best practices implemented by the deployment service include those recommended by the SQL Server team.</span></span> <span data-ttu-id="42d60-275">詳細については、[ここ](https://blogs.technet.com/b/dataplatforminsider/archive/2014/09/12/new-vm-images-optimized-for-transactional-and-dw-workloads-in-azure-vm-gallery.aspx) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="42d60-275">For more information, click [here](https://blogs.technet.com/b/dataplatforminsider/archive/2014/09/12/new-vm-images-optimized-for-transactional-and-dw-workloads-in-azure-vm-gallery.aspx).</span></span> <span data-ttu-id="42d60-276">さらに、次の項目が実行されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-276">In addition, the following items are done:</span></span>

-   <span data-ttu-id="42d60-277">複数の一時ファイル (CPU コアごとに 1 つ)。</span><span class="sxs-lookup"><span data-stu-id="42d60-277">Multiple temp files (one per CPU core).</span></span>
-   <span data-ttu-id="42d60-278">SQL Server の最大メモリを使用可能なコンピューター RAM の 90% に設定します。</span><span class="sxs-lookup"><span data-stu-id="42d60-278">Set max memory for SQL Server to 90% of available machine RAM.</span></span>
-   <span data-ttu-id="42d60-279">並列処理の最大限度を設定します。</span><span class="sxs-lookup"><span data-stu-id="42d60-279">Set max degree of parallelism.</span></span>
-   <span data-ttu-id="42d60-280">トレース フラグの有効  -T1204、 -T1222。</span><span class="sxs-lookup"><span data-stu-id="42d60-280">Enabled trace flags  -T1204, -T1222.</span></span>

## <a name="estimate-costs-and-understand-the-azure-billing-process"></a><span data-ttu-id="42d60-281">減価を見積もり、Azure 請求プロセスに同意</span><span class="sxs-lookup"><span data-stu-id="42d60-281">Estimate costs and understand the Azure billing process</span></span>
<span data-ttu-id="42d60-282">Azure での AX 2012 R3 の展開コストを見積もるには、[Azure 価格計算ツール](https://azure.microsoft.com/pricing/calculator/)を使用します。</span><span class="sxs-lookup"><span data-stu-id="42d60-282">To help estimate the cost of your AX 2012 R3 deployment on Azure, use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/).</span></span> <span data-ttu-id="42d60-283">Azure に AX 2012 R3 を配置する前に、Azure 請求プロセスについて理解することも重要です。</span><span class="sxs-lookup"><span data-stu-id="42d60-283">It’s also important to understand the Azure billing process before you deploy AX 2012 R3 on Azure.</span></span> <span data-ttu-id="42d60-284">サンプル請求書、および現在の請求期間に対する毎日の使用データをダウンロードする方法に関する情報にリンクする Azure 請求プロセスの概要については、[請求書を理解する](https://azure.microsoft.com/support/understand-your-bill/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-284">For an overview of the Azure billing process, links to sample invoices, and information about how to download daily usage data for the current billing period, see [Understand your bill](https://azure.microsoft.com/support/understand-your-bill/).</span></span> 

> [!NOTE]
> <span data-ttu-id="42d60-285">使用されていないときに Azure 上に配置されている AX 2012 R3 環境をシャット ダウンすることができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-285">Keep in mind, you can shut down an AX 2012 R3 environment that has been deployed on Azure when it’s not in use.</span></span> <span data-ttu-id="42d60-286">たとえば、コスト削減のため週末に環境をシャット ダウンする場合があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-286">For example, you may want to shut down an environment on the weekends to reduce costs.</span></span> <span data-ttu-id="42d60-287">環境をシャット ダウンすると、その環境はまだ存在します。ただし、その環境内の仮想マシンはシャット ダウンされます。</span><span class="sxs-lookup"><span data-stu-id="42d60-287">When you shut down an environment, the environment still exists; however, the virtual machines in the environment are shut down.</span></span> <span data-ttu-id="42d60-288">仮想マシンが実行されていないときは、それに対して課金されません。</span><span class="sxs-lookup"><span data-stu-id="42d60-288">You won’t be charged for the virtual machines when they’re not running.</span></span> <span data-ttu-id="42d60-289">詳細については、「環境をシャット ダウンする方法とは」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-289">For more information, see “How do I shut down an environment?”</span></span> <span data-ttu-id="42d60-290">[Azure 上の AX 2012 R3 配置の管理](manage-2012-r3-deployment-azure.md) という記事の中です。</span><span class="sxs-lookup"><span data-stu-id="42d60-290">in the [Manage AX 2012 R3 deployments on Azure](manage-2012-r3-deployment-azure.md) article.</span></span>

## <a name="consider-legal-and-regulatory-requirements"></a><span data-ttu-id="42d60-291">法的および規制要件を考慮する</span><span class="sxs-lookup"><span data-stu-id="42d60-291">Consider legal and regulatory requirements</span></span>
<span data-ttu-id="42d60-292">Microsoft は、複数の地域や税務署にわたる一般的な運用方法と機能で Azure サービスを実行します。</span><span class="sxs-lookup"><span data-stu-id="42d60-292">Microsoft runs Azure services with common operational practices and features across multiple geographies and jurisdictions.</span></span> <span data-ttu-id="42d60-293">ただし、Microsoft サービスがユーザーの規制の必要を満たしているかどうかを判断するのは、最終的にはユーザー次第となります。</span><span class="sxs-lookup"><span data-stu-id="42d60-293">However, it is ultimately up to you to determine if Microsoft services satisfy your regulatory needs.</span></span> <span data-ttu-id="42d60-294">最新の情報を提供するために、[Azure セキュリティ センター](https://azure.microsoft.com/support/trust-center/) はセキュリティ、プライバシー、コンプライアンスに関する以下の情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="42d60-294">To help provide you with up-to-date information, the [Azure trust center](https://azure.microsoft.com/support/trust-center/) provides the following information about security, privacy, and compliance.</span></span>

-   <span data-ttu-id="42d60-295">**セキュリティ:** [Azure セキュリティ ページ](https://www.windowsazure.com/support/trust-center/security/) は地理的に分散されているデータ センター内に安全な環境を提供するために Microsoft が取っている条項の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="42d60-295">**Security:** The [Azure security page](https://www.windowsazure.com/support/trust-center/security/) provides an overview of the provisions Microsoft is taking to provide a secure environment within geographically dispersed datacenters.</span></span> <span data-ttu-id="42d60-296">セキュリティ関連リソースの広範なリストの中で、[情報の要求についての標準応答: セキュリティおよびプライバシー](https://www.microsoft.com/download/details.aspx?id=26647) ホワイト ペーパーがどのように Azure の提案されたプリンシパルを満たし、国際標準化機構 (ISO) 27001:2005 および ISO 27002 にマップされているかを概説します。</span><span class="sxs-lookup"><span data-stu-id="42d60-296">Among the extensive list of security-related resources, the [Standard Response to Request for Information: Security and Privacy](https://www.microsoft.com/download/details.aspx?id=26647) white paper outlines how Azure meets the suggested principals and mapped them to the International Standards Organization (ISO) 27001:2005 and ISO 27002.</span></span>
-   <span data-ttu-id="42d60-297">**プライバシー:** [Azure プライバシー ページ](https://www.windowsazure.com/support/trust-center/privacy/) は、Azure 環境のプライバシーに関する取り組みを説明する複数のリソースへのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="42d60-297">**Privacy:** The [Azure privacy page](https://www.windowsazure.com/support/trust-center/privacy/) includes links to multiple resources that describe privacy practices of the Azure environment.</span></span> <span data-ttu-id="42d60-298">[Azure のプライバシーに関する声明](https://www.windowsazure.com/support/legal/privacy-statement/)へのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="42d60-298">It includes a link to the [Azure privacy statement](https://www.windowsazure.com/support/legal/privacy-statement/).</span></span>
-   <span data-ttu-id="42d60-299">**コンプライアンス:** [Azure コンプライアンス ページ](https://www.windowsazure.com/support/trust-center/compliance/) は、独自の業界に適用される特定の法律および規制を順守し、シナリオを使用するためのリソースを提供します。</span><span class="sxs-lookup"><span data-stu-id="42d60-299">**Compliance:** The [Azure compliance page](https://www.windowsazure.com/support/trust-center/compliance/) provides resources to help you comply with the specific laws and regulations applicable to your unique industry and use scenario.</span></span>

## <a name="consider-licensing-requirements"></a><span data-ttu-id="42d60-300">ライセンス供与の要件の検討</span><span class="sxs-lookup"><span data-stu-id="42d60-300">Consider licensing requirements</span></span>
<span data-ttu-id="42d60-301">AX 2012 R3 仮想マシン環境のさまざまなコンポーネントのライセンス供与は、重要な考慮事項です。</span><span class="sxs-lookup"><span data-stu-id="42d60-301">Licensing the various components of the AX 2012 R3 virtual machine environment is an important consideration.</span></span> <span data-ttu-id="42d60-302">Azure での展開は、 Azure に固有な特別なライセンス条項であるか、およびそれらの条項がソリューションの全体的な適合性を備えているかを評価します。</span><span class="sxs-lookup"><span data-stu-id="42d60-302">For deployments on Azure, you will want to evaluate the special licensing terms specific to Azure and the impact that these terms have on the overall suitability of the solution.</span></span> <span data-ttu-id="42d60-303">ライセンス供与の要件は、Azure に配置する AX 2012 R3 仮想マシン環境の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="42d60-303">Licensing requirements vary based on the type of AX 2012 R3 virtual machine environment that you deploy on Azure.</span></span> <span data-ttu-id="42d60-304">次のテーブルに詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="42d60-304">The following table provides more information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42d60-305"><strong>環境のタイプ</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-305"><strong>Type of environment</strong></span></span></td>
<td><span data-ttu-id="42d60-306"><strong>ライセンス要件</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-306"><strong>Licensing requirements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-307">デモ</span><span class="sxs-lookup"><span data-stu-id="42d60-307">Demo</span></span></td>
<td><span data-ttu-id="42d60-308">仮想マシン環境に含まれるソフトウェアは、ソフトウェア ライセンス条項の項目に従って、時間制限付きで使用許諾されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-308">The software that is included in the virtual machine environment is time-bound and licensed according to the terms in the Software License Terms.</span></span>
<ul>
<li><span data-ttu-id="42d60-309"><a href="https://go.microsoft.com/fwlink/?LinkId=397371">AX 2013 R3 デモ環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="42d60-309"><a href="https://go.microsoft.com/fwlink/?LinkId=397371">Software License Terms for the AX 2013 R3 demo environment</a></span></span></li>
<li><span data-ttu-id="42d60-310"><a href="https://go.microsoft.com/fwlink/?LinkId=397371">AX 2013 R3 CU8 デモ環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="42d60-310"><a href="https://go.microsoft.com/fwlink/?LinkId=397371">Software License Terms for the AX 2013 R3 CU8 demo environment</a></span></span></li>
<li><span data-ttu-id="42d60-311"><a href="https://go.microsoft.com/fwlink/?LinkId=397371">5. Retail Essentials デモ環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="42d60-311"><a href="https://go.microsoft.com/fwlink/?LinkId=397371">Software License Terms for the Retail essentials demo environment</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d60-312">開発/テストおよび高可用性</span><span class="sxs-lookup"><span data-stu-id="42d60-312">Dev/test and high availability</span></span></td>
<td><span data-ttu-id="42d60-313">仮想マシン環境を含めすべてのソフトウェアには適切なライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="42d60-313">All software included in the virtual machine environment must be properly licensed.</span></span> <span data-ttu-id="42d60-314">パートナーとマイクロソフトの担当者共に、ライセンスのニーズを十分に調査してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-314">Please investigate your licensing needs thoroughly with your partner and your Microsoft representative.</span></span> <span data-ttu-id="42d60-315">仮想マシン環境に含まれる個々のソフトウェアの条件を調査する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-315">You will need to investigate the terms for each piece of software that is included in the virtual machine environment.</span></span> <span data-ttu-id="42d60-316">仮想マシン環境に含まれるソフトウェアの完全な一覧については、ソフトウェア ライセンス条項を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-316">For the complete list of software that is included in the virtual machine environment, review the Software License Terms.</span></span>
<ul>
<li><span data-ttu-id="42d60-317"><a href="https://go.microsoft.com/fwlink/?LinkId=397363">開発環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="42d60-317"><a href="https://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the development environment</a></span></span></li>
<li><span data-ttu-id="42d60-318"><a href="https://go.microsoft.com/fwlink/?LinkId=397363">共有の SQL Server 環境による開発用のソフトウェア ライセンス条件</a></span><span class="sxs-lookup"><span data-stu-id="42d60-318"><a href="https://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the development with shared SQL Server environment</a></span></span></li>
<li><span data-ttu-id="42d60-319"><a href="https://go.microsoft.com/fwlink/?LinkId=397363">テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="42d60-319"><a href="https://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the test environment</a></span></span></li>
<li><span data-ttu-id="42d60-320"><a href="https://go.microsoft.com/fwlink/?LinkID=507496&amp;amp;clcid=0x409">5. Retail Essentials 開発/テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="42d60-320"><a href="https://go.microsoft.com/fwlink/?LinkID=507496&amp;amp;clcid=0x409">Software License Terms for the Retail essentials dev/test environment</a></span></span></li>
<li><span data-ttu-id="42d60-321"><a href="https://go.microsoft.com/fwlink/?LinkID=507494">5. Retail E-commerce 開発/テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="42d60-321"><a href="https://go.microsoft.com/fwlink/?LinkID=507494">Software License Terms for the Retail e-commerce dev/test environment</a></span></span></li>
<li><span data-ttu-id="42d60-322"><a href="https://go.microsoft.com/fwlink/?LinkID=507496">5. Retail Mobility 開発/テスト環境のソフトウェア ライセンス条項</a></span><span class="sxs-lookup"><span data-stu-id="42d60-322"><a href="https://go.microsoft.com/fwlink/?LinkID=507496">Software License Terms for the Retail mobility dev/test environment</a></span></span></li>
<li><span data-ttu-id="42d60-323"><a href="https://go.microsoft.com/fwlink/?LinkId=397363">高可用性環境のソフトウェア ライセンス条項</a> </span><span class="sxs-lookup"><span data-stu-id="42d60-323"><a href="https://go.microsoft.com/fwlink/?LinkId=397363">Software License Terms for the high availability environment</a> </span></span></li>
</ul>
<p><span data-ttu-id="42d60-324">ライセンス条項と要件を確認する際には、Azure に配置するために特に適用される条項、および使用目的に適用される条項に特に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-324">When reviewing the licensing terms and requirements, you need to pay special attention to any terms that apply specifically to deploying on Azure, as well as terms that apply to your intended use.</span></span> <span data-ttu-id="42d60-325">たとえば、Microsoft Office は Azure に固有の条件を持ちますが、これらの条件は、開発またはテスト目的で Office を配置するか、または生産目的で Office を配置するかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="42d60-325">For example, Microsoft Office has terms that are specific to Azure; but those terms vary depending on whether you deploy Office for development or test purposes, or whether you deploy Office for production purposes.</span></span></p>
<p><span data-ttu-id="42d60-326">開始するうえで役立ついくつかのリソースを以下のリンクに示します。</span><span class="sxs-lookup"><span data-stu-id="42d60-326">Some resources to help you get started are linked to below.</span></span> <span data-ttu-id="42d60-327">以下にリンクされているリソースのほとんどに、複数の製品およびシナリオの詳細な情報へのリンクが含まれています。ただし、追加の情報を確認しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-327">Most of the resources that are linked to below contain links to in-depth information for several products and scenarios; however, you may need to review additional information, as well.</span></span> <span data-ttu-id="42d60-328">この情報は、ライセンスを取得した製品の承認済みの使用に関するガイドに役立つ情報です。 同意ではありません。</span><span class="sxs-lookup"><span data-stu-id="42d60-328">This information is provided to help guide your authorized use of products you license; it is not your agreement.</span></span> <span data-ttu-id="42d60-329">ボリューム ライセンス契約にもとづいてライセンスされている製品の使用は、その契約の条件によって支配されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-329">Your use of products licensed under your volume license agreement is governed by the terms and conditions of that agreement.</span></span> <span data-ttu-id="42d60-330">ここにリンクされている情報と契約に矛盾がある場合、契約の使用条件が有効となります。</span><span class="sxs-lookup"><span data-stu-id="42d60-330">In the case of any conflict between information linked here and your agreement, the terms and conditions of your agreement control.</span></span></p>
<ul>
<li><span data-ttu-id="42d60-331"><strong>仮想マシン ライセンスによく寄せられる質問</strong> Azure 仮想マシンのライセンスに関するよくある質問は、<a href="https://www.windowsazure.com/pricing/licensing-faq/">このページ</a>で回答されています。</span><span class="sxs-lookup"><span data-stu-id="42d60-331"><strong>Virtual machines licensing FAQ</strong> Common questions regarding licensing on Azure virtual machines are answered on <a href="https://www.windowsazure.com/pricing/licensing-faq/">this page</a>.</span></span></li>
<li><span data-ttu-id="42d60-332"><strong>Microsoft 製品の使用権限と製品リスト</strong>ビジネス上の意思決定を効果的にし、IT 購入価値を最大化するために、<a href="https://go.microsoft.com/fwlink/?LinkId=397363">このページ</a>で、Microsoft ボリューム ライセンス製品のライセンスモデル、プログラム、シナリオ、および使用条件について詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="42d60-332"><strong>Microsoft Product Use Rights and Product List</strong> Learn more about Microsoft Volume Licensing product licensing models, programs, scenarios, and terms and conditions to help you make effective business decisions and maximize the value of your IT purchases on <a href="https://go.microsoft.com/fwlink/?LinkId=397363">this page</a>.</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="42d60-333"><strong>Azure プログラムのソフトウェア保証によるライセンス モビリティ</strong>ソフトウェア保証によるライセンス モビリティにより、Microsoft ボリューム ライセンスの顧客は、Azure でアクティブなソフトウェア保証を使用して、適格なサーバー アプリケーションを配置する柔軟性を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-333"><strong>License Mobility through Software Assurance on Azure program</strong> License Mobility through Software Assurance gives Microsoft volume licensing customers the flexibility to deploy eligible server applications with active Software Assurance on Azure.</span></span> <span data-ttu-id="42d60-334">このソフトウェア保証給付金では、新しいライセンスを購入する必要がなく、関連するモビリティ費用がかかりません。</span><span class="sxs-lookup"><span data-stu-id="42d60-334">With this Software Assurance benefit, there is no need to purchase new licenses and no associated mobility fees.</span></span> <span data-ttu-id="42d60-335">これにより、既存のライセンスを Azure クラウド プラットフォームに簡単に展開できます。</span><span class="sxs-lookup"><span data-stu-id="42d60-335">This enables you to easily deploy existing licenses on the Azure cloud platform.</span></span> <span data-ttu-id="42d60-336">詳細については、<a href="https://www.windowsazure.com/pricing/license-mobility/">このページ</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-336">For more information, see <a href="https://www.windowsazure.com/pricing/license-mobility/">this page</a>.</span></span> <span data-ttu-id="42d60-337">開発、テスト、および SharePoint の高可用性トポロジ トライアル版用に、Visual Studio、SQL Server および Office が提供されています。</span><span class="sxs-lookup"><span data-stu-id="42d60-337">For Development, Test, and High Availability topologies trial versions of SharePoint, Visual Studio, SQL Server, and Office are provided.</span></span> <span data-ttu-id="42d60-338">評価の範囲は 30〜180 日間です。</span><span class="sxs-lookup"><span data-stu-id="42d60-338">The trials range from 30-180 days.</span></span> <span data-ttu-id="42d60-339">それに応じてライセンスを適用してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-339">Please apply licenses accordingly.</span></span></li>
<li><span data-ttu-id="42d60-340"><strong>Microsoft Dynamics AX ボリューム ライセンス バイヤー ガイド</strong> Microsoft Dynamics AX を使用したキー ライセンス オプションの概要については、<a href="https://go.microsoft.com/fwlink/?LinkId=397363">このページ</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-340"><strong>Microsoft Dynamics AX volume licensing buyer’s guide</strong> For an overview of key licensing options with Microsoft Dynamics AX, see <a href="https://go.microsoft.com/fwlink/?LinkId=397363">this page</a>.</span></span></li>
<li><span data-ttu-id="42d60-341"><strong>企業向け Microsoft 365 アプリの共有コンピュータの有効化</strong> 共有コンピューターの有効化により、複数のユーザーがアクセスする組織内のコンピュータに企業向け Microsoft 365 アプリを配置できます。</span><span class="sxs-lookup"><span data-stu-id="42d60-341"><strong>Shared computer activation for Microsoft 365 Apps for enterprise</strong> Shared computer activation lets you to deploy Microsoft 365 Apps for enterprise to a computer in your organization that is accessed by multiple users.</span></span> <span data-ttu-id="42d60-342">詳細については、<a href="https://technet.microsoft.com/library/dn782860(v=office.15).aspx">このページ</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-342">For more information, see <a href="https://technet.microsoft.com/library/dn782860(v=office.15).aspx">this page</a>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="select-the-ax-2012-r3-environment-that-you-want-to-deploy"></a><span data-ttu-id="42d60-343">配置する AX 2012 R3 環境を選択</span><span class="sxs-lookup"><span data-stu-id="42d60-343">Select the AX 2012 R3 environment that you want to deploy</span></span>
<span data-ttu-id="42d60-344">Azure 上に AX 2012 R3 環境を配置するには、Lifecycle Services のクラウド ホスト環境ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="42d60-344">You’ll use the Cloud-hosted environments tool in Lifecycle Services to deploy AX 2012 R3 environments on Azure.</span></span> <span data-ttu-id="42d60-345">クラウド ホスト環境ツールを使用して配置するとき、デモまたは開発/テスト環境などの、Azure 上に配置する環境のタイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-345">When you use the Cloud-hosted environments tool to deploy, you’ll need to select the type of environment that you want to deploy on Azure, such as a demo or development/test environment.</span></span> <span data-ttu-id="42d60-346">この選択に基づいて、クラウド ホスト環境ツールは Azure での仮想マシンの適切な数を提供します。</span><span class="sxs-lookup"><span data-stu-id="42d60-346">Based on your selection, the Cloud-hosted environments tool provisions the appropriate number of virtual machines on Azure.</span></span> <span data-ttu-id="42d60-347">これらの仮想マシンには、AX 2012 R3 コンポーネント (およびそれらの必要物すべて) がインストール済みです。</span><span class="sxs-lookup"><span data-stu-id="42d60-347">These virtual machines have AX 2012 R3 components—and all of their prerequisites—already installed on them.</span></span> <span data-ttu-id="42d60-348">次のセクションでは、Azure に配置できる AX 2012 R3 環境について説明します。</span><span class="sxs-lookup"><span data-stu-id="42d60-348">The following sections describe the AX 2012 R3 environments that you can deploy on Azure.</span></span>

-   <span data-ttu-id="42d60-349">AX 2012 R3 および AX 2012 R3 CU8 デモ環境</span><span class="sxs-lookup"><span data-stu-id="42d60-349">AX 2012 R3 and AX 2012 R3 CU8 demo environments</span></span>
-   <span data-ttu-id="42d60-350">Retail Essentials デモ環境</span><span class="sxs-lookup"><span data-stu-id="42d60-350">Retail essentials demo environment</span></span>
-   <span data-ttu-id="42d60-351">開発環境</span><span class="sxs-lookup"><span data-stu-id="42d60-351">Development environments</span></span>
-   <span data-ttu-id="42d60-352">テスト環境</span><span class="sxs-lookup"><span data-stu-id="42d60-352">Test environment</span></span>
-   <span data-ttu-id="42d60-353">Retail Essentials 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="42d60-353">Retail essentials dev/test environment</span></span>
-   <span data-ttu-id="42d60-354">Retail E-commerce 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="42d60-354">Retail e-commerce dev/test environment</span></span>
-   <span data-ttu-id="42d60-355">Retail mobility 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="42d60-355">Retail mobility dev/test environment</span></span>
-   <span data-ttu-id="42d60-356">高可用性環境</span><span class="sxs-lookup"><span data-stu-id="42d60-356">High availability environment</span></span>

> [!NOTE]
> <span data-ttu-id="42d60-357">このような環境では、SQL Server は SQL\_Latin1\_General\_CP1\_CI\_AS の照合順序を使用するよう構成されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-357">In these environments, SQL Server is configured to use the SQL\_Latin1\_General\_CP1\_CI\_AS collation.</span></span>

## <a name="ax-2012-r3-and-ax-2012-r3-cu8-demo-environments"></a><span data-ttu-id="42d60-358">AX 2012 R3 および AX 2012 R3 CU8 デモ環境</span><span class="sxs-lookup"><span data-stu-id="42d60-358">AX 2012 R3 and AX 2012 R3 CU8 demo environments</span></span>
<span data-ttu-id="42d60-359">2 つの AX 2012 R3 デモ環境があります。1 方の環境には累積更新プログラム 8 があり、もう 1 つ方にはありません。</span><span class="sxs-lookup"><span data-stu-id="42d60-359">There are two AX 2012 R3 demo environments: one environment includes Cumulative Update 8, and the other does not.</span></span> <span data-ttu-id="42d60-360">次のテーブルは、それぞれの環境に関する詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="42d60-360">The following table lists details about each environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="42d60-361">各環境に含まれる仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="42d60-361">The virtual machine included in each environment is a single-instance virtual machine.</span></span> <span data-ttu-id="42d60-362">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](https://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="42d60-362">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](https://azure.microsoft.com/support/legal/sla/).</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42d60-363"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-363"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="42d60-364"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-364"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="42d60-365"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-365"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="42d60-366"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-366"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-367">1</span><span class="sxs-lookup"><span data-stu-id="42d60-367">1</span></span></td>
<td><span data-ttu-id="42d60-368">デモ マシン</span><span class="sxs-lookup"><span data-stu-id="42d60-368">Demo machine</span></span></td>
<td><span data-ttu-id="42d60-369"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-369"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-370"><strong>既定名:</strong> DEMO-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-370"><strong>Default name:</strong> DEMO-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-371">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="42d60-371">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="42d60-372">Active Directory</span><span class="sxs-lookup"><span data-stu-id="42d60-372">Active Directory</span></span></li>
<li><span data-ttu-id="42d60-373">ドメイン名サービス (DNS)</span><span class="sxs-lookup"><span data-stu-id="42d60-373">Domain Name Services (DNS)</span></span></li>
<li><span data-ttu-id="42d60-374">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="42d60-374">Internet Information Services (IIS)</span></span></li>
<li><span data-ttu-id="42d60-375">リモート デスクトップ サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-375">Remote Desktop Services</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-376">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="42d60-376">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="42d60-377">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-377">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-378">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-378">Database Engine Services</span></span></li>
<li><span data-ttu-id="42d60-379">レポート サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-379">Reporting Services</span></span></li>
<li><span data-ttu-id="42d60-380">分析サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-380">Analysis Services</span></span></li>
<li><span data-ttu-id="42d60-381">Management Studio</span><span class="sxs-lookup"><span data-stu-id="42d60-381">Management Studio</span></span></li>
<li><span data-ttu-id="42d60-382">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="42d60-382">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-383">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="42d60-383">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="42d60-384">Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="42d60-384">Microsoft Office 2013</span></span></li>
<li><span data-ttu-id="42d60-385">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-385">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-386">データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-386">Databases</span></span></li>
<li><span data-ttu-id="42d60-387">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-387">Server components:</span></span>
<ul>
<li><span data-ttu-id="42d60-388">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="42d60-388">Application Object Server (AOS)</span></span></li>
<li><span data-ttu-id="42d60-389">Web サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-389">Web server components:</span></span>
<ul>
<li><span data-ttu-id="42d60-390">エンタープライズ ポータル (EP)</span><span class="sxs-lookup"><span data-stu-id="42d60-390">Enterprise Portal (EP)</span></span></li>
<li><span data-ttu-id="42d60-391">エンタープライズ検索</span><span class="sxs-lookup"><span data-stu-id="42d60-391">Enterprise Search</span></span></li>
<li><span data-ttu-id="42d60-392">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-392">Help Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="42d60-393">ビジネス インテリジェンス コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-393">Business intelligence components:</span></span>
<ul>
<li><span data-ttu-id="42d60-394">Reporting Services 拡張機能</span><span class="sxs-lookup"><span data-stu-id="42d60-394">Reporting Services extensions</span></span></li>
<li><span data-ttu-id="42d60-395">Analysis Services の構成</span><span class="sxs-lookup"><span data-stu-id="42d60-395">Analysis Services configuration</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-396">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-396">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="42d60-397">Management Reporter サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="42d60-397">Management Reporter server components</span></span></li>
<li><span data-ttu-id="42d60-398">Management Reporter レポート デザイナー</span><span class="sxs-lookup"><span data-stu-id="42d60-398">Management Reporter Report Designer</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-399">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-399">Client components:</span></span>
<ul>
<li><span data-ttu-id="42d60-400">クライアント</span><span class="sxs-lookup"><span data-stu-id="42d60-400">Client</span></span></li>
<li><span data-ttu-id="42d60-401">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="42d60-401">Office add-ins</span></span></li>
<li><span data-ttu-id="42d60-402">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="42d60-402">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-403">開発者ツール:</span><span class="sxs-lookup"><span data-stu-id="42d60-403">Developer tools:</span></span>
<ul>
<li><span data-ttu-id="42d60-404">デバッガー</span><span class="sxs-lookup"><span data-stu-id="42d60-404">Debugger</span></span></li>
<li><span data-ttu-id="42d60-405">Visual Studio ツール</span><span class="sxs-lookup"><span data-stu-id="42d60-405">Visual Studio Tools</span></span></li>
<li><span data-ttu-id="42d60-406">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="42d60-406">Trace Parser</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-407">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-407">Integration components:</span></span>
<ul>
<li><span data-ttu-id="42d60-408">IIS 上の Web サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-408">Web services on IIS</span></span></li>
<li><span data-ttu-id="42d60-409">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="42d60-409">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-410">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="42d60-410">Management utilities</span></span></li>
<li><span data-ttu-id="42d60-411">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-411">Retail components:</span></span>
<ul>
<li><span data-ttu-id="42d60-412">Retail POS</span><span class="sxs-lookup"><span data-stu-id="42d60-412">Retail POS</span></span></li>
<li><span data-ttu-id="42d60-413">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="42d60-413">Retail Headquarters</span></span></li>
<li><span data-ttu-id="42d60-414">Commerce Data Exchange コンポーネント</span><span class="sxs-lookup"><span data-stu-id="42d60-414">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="42d60-415">Synch Service</span><span class="sxs-lookup"><span data-stu-id="42d60-415">Synch Service</span></span></li>
<li><span data-ttu-id="42d60-416">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="42d60-416">Real-time Service</span></span></li>
<li><span data-ttu-id="42d60-417">Async Server</span><span class="sxs-lookup"><span data-stu-id="42d60-417">Async Server</span></span></li>
<li><span data-ttu-id="42d60-418">Async Client</span><span class="sxs-lookup"><span data-stu-id="42d60-418">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-419">Retail チャンネル コンフィギュレーション ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="42d60-419">Retail Channel Configuration Utility</span></span></li>
<li><span data-ttu-id="42d60-420">Retail SDK</span><span class="sxs-lookup"><span data-stu-id="42d60-420">Retail SDK</span></span></li>
<li><span data-ttu-id="42d60-421">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="42d60-421">Retail online channel</span></span></li>
<li><span data-ttu-id="42d60-422">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-422">Retail Server</span></span></li>
<li><span data-ttu-id="42d60-423">Retail 一括配置ツールキット</span><span class="sxs-lookup"><span data-stu-id="42d60-423">Retail Mass Deployment Toolkit</span></span></li>
<li><span data-ttu-id="42d60-424">小売チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-424">Retail channel database</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-425">RapidStart Connector</span><span class="sxs-lookup"><span data-stu-id="42d60-425">RapidStart Connector</span></span></li>
<li><span data-ttu-id="42d60-426">データのインポート/エクスポート フレームワーク コンポーネント。</span><span class="sxs-lookup"><span data-stu-id="42d60-426">Data Import/Export Framework components:</span></span>
<ul>
<li><span data-ttu-id="42d60-427">データのインポート/エクスポート フレームワーク (DIXF) サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-427">Data Import/Export Framework (DIXF) service</span></span></li>
<li><span data-ttu-id="42d60-428">AOS コンポーネント</span><span class="sxs-lookup"><span data-stu-id="42d60-428">AOS component</span></span></li>
<li><span data-ttu-id="42d60-429">クライアント コンポーネント</span><span class="sxs-lookup"><span data-stu-id="42d60-429">Client component</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-430">倉庫モバイル デバイス ポータル</span><span class="sxs-lookup"><span data-stu-id="42d60-430">Warehouse Mobile Devices Portal</span></span></li>
<li><span data-ttu-id="42d60-431">Microsoft Dynamics Connector</span><span class="sxs-lookup"><span data-stu-id="42d60-431">Connector for Microsoft Dynamics</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-essentials-demo-environment"></a><span data-ttu-id="42d60-432">Retail Essentials デモ環境</span><span class="sxs-lookup"><span data-stu-id="42d60-432">Retail Essentials demo environment</span></span>
<span data-ttu-id="42d60-433">この環境を配置して、Retail Essentials をデモしてください。</span><span class="sxs-lookup"><span data-stu-id="42d60-433">Deploy this environment to demo Retail essentials.</span></span> <span data-ttu-id="42d60-434">Retail Essentials は、Microsoft Dynamics AX の小売中心のコンフィギュレーション オプションです。</span><span class="sxs-lookup"><span data-stu-id="42d60-434">Retail essentials is a retail-centric configuration option for Microsoft Dynamics AX.</span></span> <span data-ttu-id="42d60-435">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="42d60-435">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="42d60-436">この仮想マシンには、Windows Server と、Retail Essentials をデモンストレーションするために必要なソフトウェアとサンプル データが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="42d60-436">This virtual machine has Windows Server—and the software and sample data that you’ll need to demo Retail essentials—already installed on it.</span></span> <span data-ttu-id="42d60-437">次のテーブルは、既定の Retail Essentials デモ環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="42d60-437">The following table lists details about the default Retail essentials demo environment.</span></span> <span data-ttu-id="42d60-438">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-438">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="42d60-439">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="42d60-439">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="42d60-440">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](https://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="42d60-440">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](https://azure.microsoft.com/support/legal/sla/).</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42d60-441"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-441"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="42d60-442"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-442"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="42d60-443"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-443"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="42d60-444"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-444"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-445">1</span><span class="sxs-lookup"><span data-stu-id="42d60-445">1</span></span></td>
<td><span data-ttu-id="42d60-446">Retail Essentials デモ コンピューター</span><span class="sxs-lookup"><span data-stu-id="42d60-446">Retail essentials demo machine</span></span></td>
<td><span data-ttu-id="42d60-447"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-447"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-448"><strong>既定名:</strong> DEMO-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-448"><strong>Default name:</strong> DEMO-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-449">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="42d60-449">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="42d60-450">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-450">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-451">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-451">Database Engine Services</span></span></li>
<li><span data-ttu-id="42d60-452">Management Studio</span><span class="sxs-lookup"><span data-stu-id="42d60-452">Management Studio</span></span></li>
<li><span data-ttu-id="42d60-453">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="42d60-453">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-454">AX 2012 R3 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-454">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-455">データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-455">Databases</span></span></li>
<li><span data-ttu-id="42d60-456">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-456">Server components:</span></span>
<ul>
<li><span data-ttu-id="42d60-457">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="42d60-457">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-458">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-458">Client components:</span></span>
<ul>
<li><span data-ttu-id="42d60-459">クライアント</span><span class="sxs-lookup"><span data-stu-id="42d60-459">Client</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-460">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-460">Integration components:</span></span>
<ul>
<li><span data-ttu-id="42d60-461">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="42d60-461">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-462">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-462">Retail components:</span></span>
<ul>
<li><span data-ttu-id="42d60-463">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="42d60-463">Retail Headquarters</span></span></li>
<li><span data-ttu-id="42d60-464">Commerce Data Exchange コンポーネント</span><span class="sxs-lookup"><span data-stu-id="42d60-464">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="42d60-465">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="42d60-465">Real-time Service</span></span></li>
<li><span data-ttu-id="42d60-466">Async Server</span><span class="sxs-lookup"><span data-stu-id="42d60-466">Async Server</span></span></li>
<li><span data-ttu-id="42d60-467">Async Client</span><span class="sxs-lookup"><span data-stu-id="42d60-467">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-468">小売チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-468">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="development-environments"></a><span data-ttu-id="42d60-469">開発環境</span><span class="sxs-lookup"><span data-stu-id="42d60-469">Development environments</span></span>
<span data-ttu-id="42d60-470">多くの開発者の開発努力を迅速に開始する必要がある場合は、これらの開発環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="42d60-470">Deploy these development environments when you need to quickly jumpstart a development effort for one to many developers.</span></span> <span data-ttu-id="42d60-471">各開発者の開発用仮想マシン (VM) を数日ではなく数時間で展開します。</span><span class="sxs-lookup"><span data-stu-id="42d60-471">Deploy a development virtual machine (VM) for each of your developers in a matter of hours instead of days.</span></span> <span data-ttu-id="42d60-472">開発環境には、テスト環境と同じドメインおよび仮想ネットワーク カスタマイズすべてが用意されています。</span><span class="sxs-lookup"><span data-stu-id="42d60-472">With a development environment, you have all the same domain and virtual network customizations that you have with the Test environment.</span></span> <span data-ttu-id="42d60-473">開発者シナリオには 2 つのトポロジ オプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="42d60-473">Two topology options are provided for developer scenarios:</span></span>

-   <span data-ttu-id="42d60-474">開発。Active Directory と共に展開されたオールインワンの VM を含みます。</span><span class="sxs-lookup"><span data-stu-id="42d60-474">Development: Includes all-in-one VMs deployed with Active Directory.</span></span>
-   <span data-ttu-id="42d60-475">共有 SQL Server による開発。Active Directory と共に展開されたオールインワンの VM を含みます。</span><span class="sxs-lookup"><span data-stu-id="42d60-475">Development with shared SQL Server: Includes all-in-one VMs deployed with Active Directory.</span></span> <span data-ttu-id="42d60-476">各開発 VM インスタンスのデータベースは、共有 SQL Server インスタンスに配置されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-476">The database for each development VM instance will be deployed to a shared SQL Server instance.</span></span>

<span data-ttu-id="42d60-477">それらの BI 開発の実行については、目的に対する 1 つのインスタンスを配置することができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-477">For those doing BI development you can deploy one instance for the purpose.</span></span> <span data-ttu-id="42d60-478">その他のすべてのインスタンスは BI で配置されません。</span><span class="sxs-lookup"><span data-stu-id="42d60-478">All other instances will not deploy with BI.</span></span> <span data-ttu-id="42d60-479">提供されている開発用 VM には、すべての AX 2012 R3 コンポーネントが Visual Studio 2013 および AX 2012 R3 開発ツールとともにインストールされています。</span><span class="sxs-lookup"><span data-stu-id="42d60-479">The development VMs provided have all the AX 2012 R3 components installed with Visual Studio 2013 and AX 2012 R3 development tools.</span></span> <span data-ttu-id="42d60-480">VM は、展開時に Active Directory ドメインに結合されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-480">The VMs are joined to the Active Directory domain at deployment time.</span></span> <span data-ttu-id="42d60-481">カスタマイズ オプションとして Active Directory ドメインを指定する場合は、VM はそのドメインに参加します。</span><span class="sxs-lookup"><span data-stu-id="42d60-481">If you provided an Active Directory domain as a customization option, then the VMs will join to that domain.</span></span> <span data-ttu-id="42d60-482">開発 VM は、AX 2012 R3 チェックリストの時点まで配置され、すべてのソフトウェアがインストールされていることがテスト環境にリストされます。</span><span class="sxs-lookup"><span data-stu-id="42d60-482">Development VMs will be deployed up to the point of the AX 2012 R3 checklist, and have all the software installed that is listed in the Test environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="42d60-483">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="42d60-483">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="42d60-484">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](https://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="42d60-484">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](https://azure.microsoft.com/support/legal/sla/).</span></span>

## <a name="test-environment"></a><span data-ttu-id="42d60-485">テスト環境</span><span class="sxs-lookup"><span data-stu-id="42d60-485">Test environment</span></span>
<span data-ttu-id="42d60-486">この環境には、既定で数台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="42d60-486">This environment includes several virtual machines, by default.</span></span> <span data-ttu-id="42d60-487">これらの仮想マシンには、Windows Server と、AX 2012 R3 のテストに必要なすべてのソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="42d60-487">These virtual machines have Windows Server—and the software that you’ll need for AX 2012 R3 testing purposes—already installed on them.</span></span> <span data-ttu-id="42d60-488">次のテーブルは、既定のテスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="42d60-488">The following table lists details about the default test environment.</span></span> <span data-ttu-id="42d60-489">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-489">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="42d60-490">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="42d60-490">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="42d60-491">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](https://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="42d60-491">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](https://azure.microsoft.com/support/legal/sla/).</span></span> <span data-ttu-id="42d60-492">データのインポート/エクスポート フレームワーク (DIXF) コンポーネントは既定ではインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="42d60-492">Data Import/Export Framework (DIXF) components are not installed by default.</span></span> <span data-ttu-id="42d60-493">DIXF を使用する場合は、独自の SQL Server インストール メディアを使用して、SQL Server マシンに SQL Server Integration Services (SSIS) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-493">If you want to use DIXF, you must use your own SQL Server installation media to install SQL Server Integration Services (SSIS) on the SQL Server machine.</span></span> <span data-ttu-id="42d60-494">SSIS をインストールした後は、Dynamics AX CD (VM 内の接続されたドライブで利用可能) を使用し、DIXF コンポーネントを AOS およびクライアント マシンにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="42d60-494">After you install SSIS, you can use the Dynamics AX CD (available on a connected drive within the VMs) to install the DIXF components on the AOS and then client machines.</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42d60-495"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-495"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="42d60-496"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-496"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="42d60-497"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-497"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="42d60-498"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-498"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-499">1</span><span class="sxs-lookup"><span data-stu-id="42d60-499">1</span></span></td>
<td><span data-ttu-id="42d60-500">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="42d60-500">Domain controller</span></span></td>
<td><span data-ttu-id="42d60-501"><strong>サイズ:</strong> D1: 基本的な計算層 (1 コア、3.5 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-501"><strong>Size:</strong> D1: Basic compute tier (1 core, 3.5 GB memory)</span></span></br><span data-ttu-id="42d60-502"><strong>既定名:</strong> AD-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-502"><strong>Default name:</strong> AD-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-503">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="42d60-503">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="42d60-504">Active Directory</span><span class="sxs-lookup"><span data-stu-id="42d60-504">Active Directory</span></span></li>
<li><span data-ttu-id="42d60-505">ドメイン名サービス (DNS)</span><span class="sxs-lookup"><span data-stu-id="42d60-505">Domain Name Services (DNS)</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d60-506">1</span><span class="sxs-lookup"><span data-stu-id="42d60-506">1</span></span></td>
<td><span data-ttu-id="42d60-507">AOS サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-507">AOS server</span></span></td>
<td><span data-ttu-id="42d60-508"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-508"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-509"><strong>既定名:</strong> AOS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-509"><strong>Default name:</strong> AOS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-510">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="42d60-510">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="42d60-511">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="42d60-511">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-512">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="42d60-512">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="42d60-513">Microsoft Project Server</span><span class="sxs-lookup"><span data-stu-id="42d60-513">Microsoft Project Server</span></span></li>
<li><span data-ttu-id="42d60-514">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-514">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-515">Management Studio</span><span class="sxs-lookup"><span data-stu-id="42d60-515">Management Studio</span></span></li>
<li><span data-ttu-id="42d60-516">ネイティブ クライアント</span><span class="sxs-lookup"><span data-stu-id="42d60-516">Native Client</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-517">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-517">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-518">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-518">Server components:</span></span>
<ul>
<li><span data-ttu-id="42d60-519">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="42d60-519">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-520">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-520">Client components:</span></span>
<ul>
<li><span data-ttu-id="42d60-521">クライアント</span><span class="sxs-lookup"><span data-stu-id="42d60-521">Client</span></span></li>
<li><span data-ttu-id="42d60-522">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="42d60-522">Office add-ins</span></span></li>
<li><span data-ttu-id="42d60-523">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="42d60-523">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-524">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-524">Integration components:</span></span>
<ul>
<li><span data-ttu-id="42d60-525">IIS 上の Web サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-525">Web services on IIS</span></span></li>
<li><span data-ttu-id="42d60-526">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="42d60-526">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-527">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="42d60-527">Management utilities</span></span></li>
<li><span data-ttu-id="42d60-528">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-528">Retail components:</span></span>
<ul>
<li><span data-ttu-id="42d60-529">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="42d60-529">Retail Headquarters</span></span></li>
<li><span data-ttu-id="42d60-530">Commerce Data Exchange コンポーネント</span><span class="sxs-lookup"><span data-stu-id="42d60-530">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="42d60-531">Synch Service</span><span class="sxs-lookup"><span data-stu-id="42d60-531">Synch Service</span></span></li>
<li><span data-ttu-id="42d60-532">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="42d60-532">Real-time Service</span></span></li>
<li><span data-ttu-id="42d60-533">Async Server</span><span class="sxs-lookup"><span data-stu-id="42d60-533">Async Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="42d60-534">RapidStart Connector</span><span class="sxs-lookup"><span data-stu-id="42d60-534">RapidStart Connector</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-535">1</span><span class="sxs-lookup"><span data-stu-id="42d60-535">1</span></span></td>
<td><span data-ttu-id="42d60-536">データベース サーバー/BIサーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-536">Database server/BI server</span></span></td>
<td><span data-ttu-id="42d60-537"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-537"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-538"><strong>既定名:</strong> SQL-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-538"><strong>Default name:</strong> SQL-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-539">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="42d60-539">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="42d60-540">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-540">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-541">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-541">Database Engine Services</span></span></li>
<li><span data-ttu-id="42d60-542">レポート サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-542">Reporting Services</span></span></li>
<li><span data-ttu-id="42d60-543">分析サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-543">Analysis Services</span></span></li>
<li><span data-ttu-id="42d60-544">Management Studio</span><span class="sxs-lookup"><span data-stu-id="42d60-544">Management Studio</span></span></li>
</ul></li>
</ul><span data-ttu-id="42d60-545">
    <strong>注記:</strong> Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="42d60-545">
    <strong>Note: </strong> Reporting Services is configured to run in Native mode.</span></span> <span data-ttu-id="42d60-546">電源表示を使用するには、追加の構成手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-546">To use Power View, you’ll need to complete additional configuration steps.</span></span> <span data-ttu-id="42d60-547">詳細については、<a href="https://technet.microsoft.com/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-547">For more information, see the prerequisites listed in <a href="https://technet.microsoft.com/library/jj933492.aspx">Create a report by using Power View to connect to a cube</a>.</span></span>
<ul>
<li><span data-ttu-id="42d60-548">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-548">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-549">データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-549">Databases</span></span></li>
<li><span data-ttu-id="42d60-550">ビジネス インテリジェンス コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-550">Business intelligence components:</span></span>
<ul>
<li><span data-ttu-id="42d60-551">Reporting Services 拡張機能</span><span class="sxs-lookup"><span data-stu-id="42d60-551">Reporting Services extensions</span></span></li>
<li><span data-ttu-id="42d60-552">Analysis Services の構成</span><span class="sxs-lookup"><span data-stu-id="42d60-552">Analysis Services configuration</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d60-553">0</span><span class="sxs-lookup"><span data-stu-id="42d60-553">0</span></span></td>
<td><span data-ttu-id="42d60-554">エンタープライズ ポータル サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-554">Enterprise Portal server</span></span></td>
<td><span data-ttu-id="42d60-555"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-555"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-556"><strong>既定名:</strong> EP-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-556"><strong>Default name:</strong> EP-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-557">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="42d60-557">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="42d60-558">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="42d60-558">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-559">Microsoft SQL Server 2012 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-559">Microsoft SQL Server 2012 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-560">フル テキスト検索</span><span class="sxs-lookup"><span data-stu-id="42d60-560">Full-text Search</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-561">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="42d60-561">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="42d60-562">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-562">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-563">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-563">Server components:</span></span>
<ul>
<li><span data-ttu-id="42d60-564">Web サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-564">Web server components:</span></span>
<ul>
<li><span data-ttu-id="42d60-565">エンタープライズ ポータル (EP)</span><span class="sxs-lookup"><span data-stu-id="42d60-565">Enterprise Portal (EP)</span></span></li>
<li><span data-ttu-id="42d60-566">エンタープライズ検索</span><span class="sxs-lookup"><span data-stu-id="42d60-566">Enterprise Search</span></span></li>
<li><span data-ttu-id="42d60-567">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-567">Help Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="42d60-568">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-568">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="42d60-569">Management Reporter サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="42d60-569">Management Reporter server components</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-570">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-570">Retail components:</span></span>
<ul>
<li><span data-ttu-id="42d60-571">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-571">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="42d60-572">Async Client</span><span class="sxs-lookup"><span data-stu-id="42d60-572">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-573">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-573">Retail Server</span></span></li>
<li><span data-ttu-id="42d60-574">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="42d60-574">Retail Online Channel</span></span></li>
<li><span data-ttu-id="42d60-575">Retail チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-575">Retail Channel Database</span></span></li>
<li><span data-ttu-id="42d60-576">Retail チャンネル コンフィギュレーション ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="42d60-576">Retail Channel Configuration Utility</span></span></li>
<li><span data-ttu-id="42d60-577">Retail ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="42d60-577">Retail Hardware Station</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-578">倉庫モバイル デバイス ポータル</span><span class="sxs-lookup"><span data-stu-id="42d60-578">Warehouse Mobile Devices Portal</span></span></li>
<li><span data-ttu-id="42d60-579">Microsoft Dynamics Connector</span><span class="sxs-lookup"><span data-stu-id="42d60-579">Connector for Microsoft Dynamics</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-580">1</span><span class="sxs-lookup"><span data-stu-id="42d60-580">1</span></span></td>
<td><span data-ttu-id="42d60-581">クライアント コンピューター</span><span class="sxs-lookup"><span data-stu-id="42d60-581">Client computer</span></span></td>
<td><span data-ttu-id="42d60-582"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-582"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-583"><strong>既定名:</strong> CLI-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-583"><strong>Default name:</strong> CLI-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-584">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="42d60-584">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="42d60-585">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="42d60-585">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="42d60-586">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-586">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-587">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="42d60-587">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-588">Microsoft SharePoint Server 2013 クライアント コンポーネント SDK</span><span class="sxs-lookup"><span data-stu-id="42d60-588">Microsoft SharePoint Server 2013 Client Components SDK</span></span></li>
<li><span data-ttu-id="42d60-589">企業向け Microsoft 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="42d60-589">Microsoft 365 Apps for enterprise</span></span></li>
<li><span data-ttu-id="42d60-590">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-590">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-591">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-591">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="42d60-592">Management Reporter レポート デザイナー</span><span class="sxs-lookup"><span data-stu-id="42d60-592">Management Reporter Report Designer</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-593">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-593">Client components:</span></span>
<ul>
<li><span data-ttu-id="42d60-594">クライアント</span><span class="sxs-lookup"><span data-stu-id="42d60-594">Client</span></span></li>
<li><span data-ttu-id="42d60-595">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="42d60-595">Office add-ins</span></span></li>
<li><span data-ttu-id="42d60-596">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="42d60-596">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-597">開発者ツール:</span><span class="sxs-lookup"><span data-stu-id="42d60-597">Developer tools:</span></span>
<ul>
<li><span data-ttu-id="42d60-598">デバッガー</span><span class="sxs-lookup"><span data-stu-id="42d60-598">Debugger</span></span></li>
<li><span data-ttu-id="42d60-599">Visual Studio ツール</span><span class="sxs-lookup"><span data-stu-id="42d60-599">Visual Studio Tools</span></span></li>
<li><span data-ttu-id="42d60-600">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="42d60-600">Trace Parser</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-601">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="42d60-601">Management utilities</span></span></li>
<li><span data-ttu-id="42d60-602">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-602">Retail components:</span></span>
<ul>
<li><span data-ttu-id="42d60-603">Retail POS</span><span class="sxs-lookup"><span data-stu-id="42d60-603">Retail POS</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d60-604">0</span><span class="sxs-lookup"><span data-stu-id="42d60-604">0</span></span></td>
<td><span data-ttu-id="42d60-605">リモート デスクトップ サービス サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-605">Remote Desktop Services server</span></span></td>
<td><span data-ttu-id="42d60-606"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-606"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-607"><strong>既定名:</strong> RDS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-607"><strong>Default name:</strong> RDS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-608">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="42d60-608">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="42d60-609">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="42d60-609">Internet Information Services (IIS)</span></span></li>
<li><span data-ttu-id="42d60-610">リモート デスクトップ サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-610">Remote Desktop Services</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-611">Microsoft SQL Server 2012 ネイティブ クライアント</span><span class="sxs-lookup"><span data-stu-id="42d60-611">Microsoft SQL Server 2012 Native Client</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-essentials-devtest-environment"></a><span data-ttu-id="42d60-612">Retail Essentials 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="42d60-612">Retail Essentials dev/test environment</span></span>
<span data-ttu-id="42d60-613">この環境を配置して、Retail essentials の機能を開発またはテストします。</span><span class="sxs-lookup"><span data-stu-id="42d60-613">Deploy this environment to develop or test features for Retail essentials.</span></span> <span data-ttu-id="42d60-614">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="42d60-614">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="42d60-615">この仮想マシンには、Windows Server と、Retail Essentials の開発とテストで必要となるソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="42d60-615">This virtual machine has Windows Server—and the software that you’ll need for Retail essentials development and testing purposes—already installed on it.</span></span> <span data-ttu-id="42d60-616">次のテーブルは、既定の Retail Essentials 開発/テスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="42d60-616">The following table lists details about the default Retail essentials dev/test environment.</span></span> <span data-ttu-id="42d60-617">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-617">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="42d60-618">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="42d60-618">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="42d60-619">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](https://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="42d60-619">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](https://azure.microsoft.com/support/legal/sla/).</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42d60-620"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-620"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="42d60-621"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-621"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="42d60-622"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-622"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="42d60-623"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-623"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-624">1</span><span class="sxs-lookup"><span data-stu-id="42d60-624">1</span></span></td>
<td><span data-ttu-id="42d60-625">Retail Essentials サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-625">Retail essentials server</span></span></td>
<td><span data-ttu-id="42d60-626"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-626"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-627"><strong>既定名:</strong> ESSEN-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-627"><strong>Default name:</strong> ESSEN-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-628">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="42d60-628">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="42d60-629">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-629">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-630">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-630">Database Engine Services</span></span></li>
<li><span data-ttu-id="42d60-631">Management Studio</span><span class="sxs-lookup"><span data-stu-id="42d60-631">Management Studio</span></span></li>
<li><span data-ttu-id="42d60-632">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="42d60-632">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-633">AX 2012 R3 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-633">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-634">データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-634">Databases</span></span></li>
<li><span data-ttu-id="42d60-635">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-635">Server components:</span></span>
<ul>
<li><span data-ttu-id="42d60-636">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="42d60-636">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-637">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-637">Client components:</span></span>
<ul>
<li><span data-ttu-id="42d60-638">クライアント</span><span class="sxs-lookup"><span data-stu-id="42d60-638">Client</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-639">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-639">Integration components:</span></span>
<ul>
<li><span data-ttu-id="42d60-640">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="42d60-640">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-641">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-641">Retail components:</span></span>
<ul>
<li><span data-ttu-id="42d60-642">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="42d60-642">Retail Headquarters</span></span></li>
<li><span data-ttu-id="42d60-643">Commerce Data Exchange コンポーネント</span><span class="sxs-lookup"><span data-stu-id="42d60-643">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="42d60-644">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="42d60-644">Real-time Service</span></span></li>
<li><span data-ttu-id="42d60-645">Async Server</span><span class="sxs-lookup"><span data-stu-id="42d60-645">Async Server</span></span></li>
<li><span data-ttu-id="42d60-646">Async Client</span><span class="sxs-lookup"><span data-stu-id="42d60-646">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-647">小売チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-647">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="retail-ecommerce-devtest-environment"></a><span data-ttu-id="42d60-648">Retail E-commerce 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="42d60-648">Retail ecommerce dev/test environment</span></span>
<span data-ttu-id="42d60-649">この環境を配置して、AX 2012 R3 と完全に統合されたオンライン販売チャネルを作成し、テストします。</span><span class="sxs-lookup"><span data-stu-id="42d60-649">Deploy this environment to create and test an online sales channel that is fully integrated with AX 2012 R3.</span></span> <span data-ttu-id="42d60-650">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="42d60-650">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="42d60-651">この仮想マシンには、Windows Server と、小売電子商取引に必要なソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="42d60-651">This virtual machine has Windows Server—and the software that you’ll need for Retail e-commerce—already installed on it.</span></span> <span data-ttu-id="42d60-652">次のテーブルは、既定の Retail E-commerce 開発/テスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="42d60-652">The following table lists details about the default Retail e-commerce dev/test environment.</span></span> <span data-ttu-id="42d60-653">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-653">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="42d60-654">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="42d60-654">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="42d60-655">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](https://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="42d60-655">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](https://azure.microsoft.com/support/legal/sla/).</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42d60-656"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-656"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="42d60-657"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-657"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="42d60-658"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-658"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="42d60-659"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-659"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-660">1</span><span class="sxs-lookup"><span data-stu-id="42d60-660">1</span></span></td>
<td><span data-ttu-id="42d60-661">Retail E-commerce サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-661">Retail e-commerce server</span></span></td>
<td><span data-ttu-id="42d60-662"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-662"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-663"><strong>既定名:</strong> E-COM-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-663"><strong>Default name:</strong> E-COM-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-664">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="42d60-664">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="42d60-665">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="42d60-665">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="42d60-666">AX 2012 R3 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-666">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-667">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-667">Retail components:</span></span>
<ul>
<li><span data-ttu-id="42d60-668">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-668">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="42d60-669">Async Client</span><span class="sxs-lookup"><span data-stu-id="42d60-669">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-670">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="42d60-670">Retail online channel</span></span></li>
<li><span data-ttu-id="42d60-671">小売チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-671">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="retail-mobility-devtest-environment"></a><span data-ttu-id="42d60-672">Retail mobility 開発/テスト環境</span><span class="sxs-lookup"><span data-stu-id="42d60-672">Retail mobility dev/test environment</span></span>
<span data-ttu-id="42d60-673">この環境を配置することで、販売スタッフが販売トランザクションを処理し、顧客注文を入力し、店舗内のどこでもモバイル デバイスを使用して日々の操作と在庫管理を実行できます。</span><span class="sxs-lookup"><span data-stu-id="42d60-673">Deploy this environment to enable your sales staff to process sales transactions, enter customer orders, and perform daily operations and inventory management with mobile devices anywhere in a store.</span></span> <span data-ttu-id="42d60-674">この環境には、既定で 1 台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="42d60-674">This environment includes one virtual machine, by default.</span></span> <span data-ttu-id="42d60-675">この仮想マシンには、Windows Server と、Retail mobilityに必要なソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="42d60-675">This virtual machine has Windows Server—and the software that you’ll need for Retail mobility—already installed on it.</span></span> <span data-ttu-id="42d60-676">次のテーブルは、既定の Retail Mobility 開発/テスト環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="42d60-676">The following table lists details about the default Retail mobility dev/test environment.</span></span> <span data-ttu-id="42d60-677">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-677">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 
> [!NOTE]
> <span data-ttu-id="42d60-678">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</span><span class="sxs-lookup"><span data-stu-id="42d60-678">The virtual machines in this environment are single-instance virtual machines.</span></span> <span data-ttu-id="42d60-679">シングル インスタンス仮想マシンは、Azure [サービス レベル アグリーメント](https://azure.microsoft.com/support/legal/sla/)の対象となりません。</span><span class="sxs-lookup"><span data-stu-id="42d60-679">Single-instance virtual machines are not covered by an Azure [Service Level Agreement](https://azure.microsoft.com/support/legal/sla/).</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42d60-680"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-680"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="42d60-681"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-681"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="42d60-682"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-682"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="42d60-683"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-683"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-684">1</span><span class="sxs-lookup"><span data-stu-id="42d60-684">1</span></span></td>
<td><span data-ttu-id="42d60-685">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-685">Retail server</span></span></td>
<td><span data-ttu-id="42d60-686"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-686"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-687"><strong>既定名:</strong> MOBIL-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-687"><strong>Default name:</strong> MOBIL-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-688">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="42d60-688">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="42d60-689">AX 2012 R3 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-689">AX 2012 R3 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-690">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-690">Retail components:</span></span>
<ul>
<li><span data-ttu-id="42d60-691">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-691">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="42d60-692">Async Client</span><span class="sxs-lookup"><span data-stu-id="42d60-692">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-693">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-693">Retail Server</span></span></li>
<li><span data-ttu-id="42d60-694">小売チャネル データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-694">Retail channel database</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="high-availability-environment"></a><span data-ttu-id="42d60-695">高可用性環境</span><span class="sxs-lookup"><span data-stu-id="42d60-695">High availability environment</span></span>
<span data-ttu-id="42d60-696">この環境を配置して、高可用性のためにコンフィギュレーションできる環境で AX 2012 R3 を使用します。</span><span class="sxs-lookup"><span data-stu-id="42d60-696">Deploy this environment to use AX 2012 R3 in an environment that can be configured for high availability.</span></span> <span data-ttu-id="42d60-697">この環境には、数台の仮想マシンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="42d60-697">This environment includes several virtual machines.</span></span> <span data-ttu-id="42d60-698">これらの仮想マシンには、Windows Server と、AX 2012 R3 を使用するために必要なソフトウェアが既にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="42d60-698">These virtual machines have Windows Server—and the software that you’ll need to use AX 2012 R3—already installed on them.</span></span> <span data-ttu-id="42d60-699">次のテーブルは、既定の高可用性環境の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="42d60-699">The following table lists details about the default high availability environment.</span></span> <span data-ttu-id="42d60-700">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="42d60-700">When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</span></span> 

> [!NOTE]
> <span data-ttu-id="42d60-701">Azure Premium Storage は高可用性環境が必要です。</span><span class="sxs-lookup"><span data-stu-id="42d60-701">Azure Premium Storage is required for high availability environments.</span></span> <span data-ttu-id="42d60-702">詳細については、 [Azure での高可用性環境の配置](deploy-high-availability-environment-azure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-702">For more information, see [Deploy high-availability environments on Azure](deploy-high-availability-environment-azure.md).</span></span> <span data-ttu-id="42d60-703">この環境の仮想マシンは、Azure [サービス レベル アグリーメント](https://azure.microsoft.com/support/legal/sla/)の対象となります。</span><span class="sxs-lookup"><span data-stu-id="42d60-703">The virtual machines in this environment are covered by an Azure [Service Level Agreement](https://azure.microsoft.com/support/legal/sla/).</span></span> <span data-ttu-id="42d60-704">データのインポート/エクスポート フレームワーク (DIXF) コンポーネントは既定ではインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="42d60-704">Data Import/Export Framework (DIXF) components are not installed by default.</span></span> <span data-ttu-id="42d60-705">DIXF を使用する場合は、独自の SQL Server インストール メディアを使用して、SQL Server マシンに SQL Server Integration Services (SSIS) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-705">If you want to use DIXF, you must use your own SQL Server installation media to install SQL Server Integration Services (SSIS) on the SQL Server machine.</span></span> <span data-ttu-id="42d60-706">SSIS をインストールした後は、Dynamics AX CD (VM 内の接続されたドライブで利用可能) を使用し、DIXF コンポーネントを AOS およびクライアント マシンにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="42d60-706">After you install SSIS, you can use the Dynamics AX CD (available on a connected drive within the VMs) to install the DIXF components on the AOS and then client machines.</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42d60-707"><strong>既定で配置される仮想マシンの数</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-707"><strong>Number of virtual machines deployed by default</strong></span></span></td>
<td><span data-ttu-id="42d60-708"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-708"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="42d60-709"><strong>サイズと名前</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-709"><strong>Size and name</strong></span></span></td>
<td><span data-ttu-id="42d60-710"><strong>ソフトウェア インストール済み</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-710"><strong>Software installed</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-711">3 <strong>注記:</strong> 3 つのドメイン コントローラがこの環境に配置されています。</span><span class="sxs-lookup"><span data-stu-id="42d60-711">3<strong>Note: </strong>Three domain controllers are deployed in this environment.</span></span> <span data-ttu-id="42d60-712">1 つのドメイン コントローラーが失敗すると、Azure の<a href="https://azure.microsoft.com/support/legal/sla/">サービス レベル同意書</a>に準拠するために、2 つのオンライン ドメイン コントローラーを残しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-712">If one domain controller fails, you must be left with two, online domain controllers in order to meet Azure’s <a href="https://azure.microsoft.com/support/legal/sla/">Service Level Agreement</a>.</span></span></td>
<td><span data-ttu-id="42d60-713">ドメイン コントローラー</span><span class="sxs-lookup"><span data-stu-id="42d60-713">Domain controller</span></span></td>
<td><span data-ttu-id="42d60-714"><strong>サイズ:</strong> D1: 基本的な計算層 (1 コア、3.5 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-714"><strong>Size:</strong> D1: Basic compute tier (1 core, 3.5 GB memory)</span></span></br><span data-ttu-id="42d60-715"><strong>既定名:</strong> AD-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-715"><strong>Default name:</strong> AD-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-716">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="42d60-716">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="42d60-717">Active Directory</span><span class="sxs-lookup"><span data-stu-id="42d60-717">Active Directory</span></span></li>
<li><span data-ttu-id="42d60-718">ドメイン名サービス (DNS)</span><span class="sxs-lookup"><span data-stu-id="42d60-718">Domain Name Services (DNS)</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d60-719">2</span><span class="sxs-lookup"><span data-stu-id="42d60-719">2</span></span></td>
<td><span data-ttu-id="42d60-720">AOS サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-720">AOS server</span></span></td>
<td><span data-ttu-id="42d60-721"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-721"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-722"><strong>既定名:</strong> AOS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-722"><strong>Default name:</strong> AOS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-723">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="42d60-723">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="42d60-724">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="42d60-724">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-725">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="42d60-725">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="42d60-726">Microsoft Project Server</span><span class="sxs-lookup"><span data-stu-id="42d60-726">Microsoft Project Server</span></span></li>
<li><span data-ttu-id="42d60-727">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-727">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-728">Management Studio</span><span class="sxs-lookup"><span data-stu-id="42d60-728">Management Studio</span></span></li>
<li><span data-ttu-id="42d60-729">ネイティブ クライアント</span><span class="sxs-lookup"><span data-stu-id="42d60-729">Native Client</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-730">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-730">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-731">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-731">Server components:</span></span>
<ul>
<li><span data-ttu-id="42d60-732">Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="42d60-732">Application Object Server (AOS)</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-733">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-733">Client components:</span></span>
<ul>
<li><span data-ttu-id="42d60-734">クライアント</span><span class="sxs-lookup"><span data-stu-id="42d60-734">Client</span></span></li>
<li><span data-ttu-id="42d60-735">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="42d60-735">Office add-ins</span></span></li>
<li><span data-ttu-id="42d60-736">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="42d60-736">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-737">統合コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-737">Integration components:</span></span>
<ul>
<li><span data-ttu-id="42d60-738">IIS 上の Web サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-738">Web services on IIS</span></span></li>
<li><span data-ttu-id="42d60-739">.NET Business Connector</span><span class="sxs-lookup"><span data-stu-id="42d60-739">.NET Business Connector</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-740">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="42d60-740">Management utilities</span></span></li>
<li><span data-ttu-id="42d60-741">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-741">Retail components:</span></span>
<ul>
<li><span data-ttu-id="42d60-742">Retail Headquarters</span><span class="sxs-lookup"><span data-stu-id="42d60-742">Retail Headquarters</span></span></li>
<li><span data-ttu-id="42d60-743">Commerce Data Exchange コンポーネント</span><span class="sxs-lookup"><span data-stu-id="42d60-743">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="42d60-744">Synch Service</span><span class="sxs-lookup"><span data-stu-id="42d60-744">Synch Service</span></span></li>
<li><span data-ttu-id="42d60-745">Real-time Service</span><span class="sxs-lookup"><span data-stu-id="42d60-745">Real-time Service</span></span></li>
<li><span data-ttu-id="42d60-746">Async Server</span><span class="sxs-lookup"><span data-stu-id="42d60-746">Async Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="42d60-747">RapidStart Connector</span><span class="sxs-lookup"><span data-stu-id="42d60-747">RapidStart Connector</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-748">2</span><span class="sxs-lookup"><span data-stu-id="42d60-748">2</span></span></td>
<td><span data-ttu-id="42d60-749">データベース サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-749">Database server</span></span></td>
<td><span data-ttu-id="42d60-750"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-750"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-751"><strong>既定名:</strong> SQL-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-751"><strong>Default name:</strong> SQL-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-752">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="42d60-752">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="42d60-753">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-753">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-754">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-754">Database Engine Services</span></span></li>
<li><span data-ttu-id="42d60-755">Management Studio</span><span class="sxs-lookup"><span data-stu-id="42d60-755">Management Studio</span></span></li>
</ul></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42d60-756"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-756"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-757">クォーラム サーバーも配置されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-757">A Quorum server is also deployed.</span></span> <span data-ttu-id="42d60-758">この仮想マシンは、AlwaysOn 可用性グループのリスナーです。</span><span class="sxs-lookup"><span data-stu-id="42d60-758">This virtual machine is a listener for the AlwaysOn availability group.</span></span> <span data-ttu-id="42d60-759">この仮想マシンは、o    [高可用性 VM] ボックスの一覧には表示されませんが、高可用性環境で展開されます。o    QRM -&lt;GUID&gt; という名前です。</span><span class="sxs-lookup"><span data-stu-id="42d60-759">This virtual machine:o    Is not represented in the High Availability VM list, but it is deployed with High Availability environments.o    Is named QRM-&lt;GUID&gt;.</span></span> <span data-ttu-id="42d60-760">この名前はカスタマイズできません。o    A2 仮想マシンです。o    Windows Server 2012 R2 のギャラリー画像を実行します。o    配置後には、この VM は、高可用性環境に VM を追加するときに「データベース サーバー」として表示されます。</span><span class="sxs-lookup"><span data-stu-id="42d60-760">This name can’t be customized.o    Is an A2 virtual machine.o    Runs a gallery image of Windows Server 2012 R2.o    Post deployment, this VM appears as a “Database Server” when adding VMs to the High Availability environment.</span></span> <span data-ttu-id="42d60-761">ここで参照されている 3 番目の VM は、明示的に SQL Server ではない A2 Quorum Server です。</span><span class="sxs-lookup"><span data-stu-id="42d60-761">The 3rd VM referenced here is the A2 Quorum Server which is explicitly not a SQL Server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d60-762"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-762"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-763">Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="42d60-763">Reporting Services is configured to run in Native mode.</span></span> <span data-ttu-id="42d60-764">電源表示を使用するには、追加の構成手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-764">To use Power View, you’ll need to complete additional configuration steps.</span></span> <span data-ttu-id="42d60-765">詳細については、<a href="https://technet.microsoft.com/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-765">For more information, see the prerequisites listed in <a href="https://technet.microsoft.com/library/jj933492.aspx">Create a report by using Power View to connect to a cube</a>.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="42d60-766">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-766">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-767">データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-767">Databases</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d60-768">2</span><span class="sxs-lookup"><span data-stu-id="42d60-768">2</span></span></td>
<td><span data-ttu-id="42d60-769">ビジネス インテリジェンス (BI) サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-769">Business intelligence (BI) server</span></span></td>
<td><span data-ttu-id="42d60-770"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-770"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-771"><strong>既定名:</strong> BI-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-771"><strong>Default name:</strong> BI-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-772">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="42d60-772">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="42d60-773">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-773">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-774">データベース エンジン サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-774">Database Engine Services</span></span></li>
<li><span data-ttu-id="42d60-775">レポート サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-775">Reporting Services</span></span></li>
<li><span data-ttu-id="42d60-776">分析サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-776">Analysis Services</span></span></li>
<li><span data-ttu-id="42d60-777">Management Studio</span><span class="sxs-lookup"><span data-stu-id="42d60-777">Management Studio</span></span></li>
</ul></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="42d60-778"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="42d60-778"><strong>Note</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-779">Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="42d60-779">Reporting Services is configured to run in Native mode.</span></span> <span data-ttu-id="42d60-780">電源表示を使用するには、追加の構成手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d60-780">To use Power View, you’ll need to complete additional configuration steps.</span></span> <span data-ttu-id="42d60-781">詳細については、<a href="https://technet.microsoft.com/library/jj933492.aspx">キューブに接続するための Power View を使用したレポートの作成</a>に一覧表示された前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42d60-781">For more information, see the prerequisites listed in <a href="https://technet.microsoft.com/library/jj933492.aspx">Create a report by using Power View to connect to a cube</a>.</span></span></td>
</tr>
</tbody>
</table>
<ul>
<li><span data-ttu-id="42d60-782">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-782">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-783">ビジネス インテリジェンス コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-783">Business intelligence components:</span></span>
<ul>
<li><span data-ttu-id="42d60-784">Reporting Services 拡張機能</span><span class="sxs-lookup"><span data-stu-id="42d60-784">Reporting Services extensions</span></span></li>
<li><span data-ttu-id="42d60-785">Analysis Services の構成</span><span class="sxs-lookup"><span data-stu-id="42d60-785">Analysis Services configuration</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-786">0</span><span class="sxs-lookup"><span data-stu-id="42d60-786">0</span></span></td>
<td><span data-ttu-id="42d60-787">エンタープライズ ポータル サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-787">Enterprise Portal server</span></span></td>
<td><span data-ttu-id="42d60-788"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-788"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-789"><strong>既定名:</strong> EP-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-789"><strong>Default name:</strong> EP-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-790">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="42d60-790">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="42d60-791">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="42d60-791">Internet Information Services (IIS)</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-792">Microsoft SQL Server 2012 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-792">Microsoft SQL Server 2012 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-793">フル テキスト検索</span><span class="sxs-lookup"><span data-stu-id="42d60-793">Full-text Search</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-794">Microsoft SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="42d60-794">Microsoft SharePoint Server 2013</span></span></li>
<li><span data-ttu-id="42d60-795">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-795">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-796">サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-796">Server components:</span></span>
<ul>
<li><span data-ttu-id="42d60-797">Web サーバー コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-797">Web server components:</span></span>
<ul>
<li><span data-ttu-id="42d60-798">エンタープライズ ポータル (EP)</span><span class="sxs-lookup"><span data-stu-id="42d60-798">Enterprise Portal (EP)</span></span></li>
<li><span data-ttu-id="42d60-799">エンタープライズ検索</span><span class="sxs-lookup"><span data-stu-id="42d60-799">Enterprise Search</span></span></li>
<li><span data-ttu-id="42d60-800">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-800">Help Server</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="42d60-801">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-801">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="42d60-802">Management Reporter サーバー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="42d60-802">Management Reporter server components</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-803">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-803">Retail components:</span></span>
<ul>
<li><span data-ttu-id="42d60-804">Commerce Data Exchange コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-804">Commerce Data Exchange components:</span></span>
<ul>
<li><span data-ttu-id="42d60-805">Async Client</span><span class="sxs-lookup"><span data-stu-id="42d60-805">Async Client</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-806">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-806">Retail Server</span></span></li>
<li><span data-ttu-id="42d60-807">小売オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="42d60-807">Retail Online Channel</span></span></li>
<li><span data-ttu-id="42d60-808">Retail チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="42d60-808">Retail Channel Database</span></span></li>
<li><span data-ttu-id="42d60-809">Retail チャンネル コンフィギュレーション ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="42d60-809">Retail Channel Configuration Utility</span></span></li>
<li><span data-ttu-id="42d60-810">Retail ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="42d60-810">Retail Hardware Station</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-811">倉庫モバイル デバイス ポータル</span><span class="sxs-lookup"><span data-stu-id="42d60-811">Warehouse Mobile Devices Portal</span></span></li>
<li><span data-ttu-id="42d60-812">Microsoft Dynamics Connector</span><span class="sxs-lookup"><span data-stu-id="42d60-812">Connector for Microsoft Dynamics</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="42d60-813">2</span><span class="sxs-lookup"><span data-stu-id="42d60-813">2</span></span></td>
<td><span data-ttu-id="42d60-814">クライアント コンピューター</span><span class="sxs-lookup"><span data-stu-id="42d60-814">Client computer</span></span></td>
<td><span data-ttu-id="42d60-815"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-815"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-816"><strong>既定名:</strong> CLI-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-816"><strong>Default name:</strong> CLI-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-817">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="42d60-817">Windows Server 2012 R2</span></span></li>
<li><span data-ttu-id="42d60-818">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="42d60-818">Microsoft Visual Studio 2013</span></span></li>
<li><span data-ttu-id="42d60-819">Microsoft SQL Server 2014 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-819">Microsoft SQL Server 2014 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-820">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="42d60-820">Developer tools</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-821">Microsoft SharePoint Server 2013 クライアント コンポーネント SDK</span><span class="sxs-lookup"><span data-stu-id="42d60-821">Microsoft SharePoint Server 2013 Client Components SDK</span></span></li>
<li><span data-ttu-id="42d60-822">企業向け Microsoft 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="42d60-822">Microsoft 365 Apps for enterprise</span></span></li>
<li><span data-ttu-id="42d60-823">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-823">AX 2012 R3 or AX 2012 R3 CU8 components:</span></span>
<ul>
<li><span data-ttu-id="42d60-824">Management Reporter コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-824">Management Reporter components:</span></span>
<ul>
<li><span data-ttu-id="42d60-825">Management Reporter レポート デザイナー</span><span class="sxs-lookup"><span data-stu-id="42d60-825">Management Reporter Report Designer</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-826">クライアント コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-826">Client components:</span></span>
<ul>
<li><span data-ttu-id="42d60-827">クライアント</span><span class="sxs-lookup"><span data-stu-id="42d60-827">Client</span></span></li>
<li><span data-ttu-id="42d60-828">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="42d60-828">Office add-ins</span></span></li>
<li><span data-ttu-id="42d60-829">リモート デスクトップ サービス統合</span><span class="sxs-lookup"><span data-stu-id="42d60-829">Remote Desktop Services integration</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-830">開発者ツール:</span><span class="sxs-lookup"><span data-stu-id="42d60-830">Developer tools:</span></span>
<ul>
<li><span data-ttu-id="42d60-831">デバッガー</span><span class="sxs-lookup"><span data-stu-id="42d60-831">Debugger</span></span></li>
<li><span data-ttu-id="42d60-832">Visual Studio ツール</span><span class="sxs-lookup"><span data-stu-id="42d60-832">Visual Studio Tools</span></span></li>
<li><span data-ttu-id="42d60-833">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="42d60-833">Trace Parser</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-834">管理ユーティリティ</span><span class="sxs-lookup"><span data-stu-id="42d60-834">Management utilities</span></span></li>
<li><span data-ttu-id="42d60-835">小売コンポーネント:</span><span class="sxs-lookup"><span data-stu-id="42d60-835">Retail components:</span></span>
<ul>
<li><span data-ttu-id="42d60-836">Retail POS</span><span class="sxs-lookup"><span data-stu-id="42d60-836">Retail POS</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="42d60-837">2</span><span class="sxs-lookup"><span data-stu-id="42d60-837">2</span></span></td>
<td><span data-ttu-id="42d60-838">リモート デスクトップ サービス サーバー</span><span class="sxs-lookup"><span data-stu-id="42d60-838">Remote Desktop Services server</span></span></td>
<td><span data-ttu-id="42d60-839"><strong>サイズ:</strong> D3: 標準計算層 (4 コア、14 GB メモリ)</span><span class="sxs-lookup"><span data-stu-id="42d60-839"><strong>Size:</strong> D3: Standard compute tier (4 cores, 14 GB memory)</span></span></br><span data-ttu-id="42d60-840"><strong>既定名:</strong> RDS-&lt;GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="42d60-840"><strong>Default name:</strong> RDS-&lt;GUID&gt;</span></span></td>
<td><ul>
<li><span data-ttu-id="42d60-841">次を含む Windows Server2012 R2:</span><span class="sxs-lookup"><span data-stu-id="42d60-841">Windows Server 2012 R2, including:</span></span>
<ul>
<li><span data-ttu-id="42d60-842">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="42d60-842">Internet Information Services (IIS)</span></span></li>
<li><span data-ttu-id="42d60-843">リモート デスクトップ サービス</span><span class="sxs-lookup"><span data-stu-id="42d60-843">Remote Desktop Services</span></span></li>
</ul></li>
<li><span data-ttu-id="42d60-844">Microsoft SQL Server 2012 ネイティブ クライアント</span><span class="sxs-lookup"><span data-stu-id="42d60-844">Microsoft SQL Server 2012 Native Client</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="next-steps"></a><span data-ttu-id="42d60-845">次のステップ</span><span class="sxs-lookup"><span data-stu-id="42d60-845">Next steps</span></span>
- [<span data-ttu-id="42d60-846">Azure に AX 2012 R3 または AX 2012 R3 CU8 デモ環境を配置する</span><span class="sxs-lookup"><span data-stu-id="42d60-846">Deploy AX 2012 R3 or AX 2012 R3 CU8 demo environments on Azure</span></span>](deploy-ax-2012-r3-ax-2012-r3-cu8-demo-environment-azure.md) 
- [<span data-ttu-id="42d60-847">Azure での Retail Essentials デモ環境の配置</span><span class="sxs-lookup"><span data-stu-id="42d60-847">Deploy a Retail essentials demo environment on Azure</span></span>](deploy-retail-essentials-demo-environment-azure.md) 
- [<span data-ttu-id="42d60-848">Azure での開発環境の配置</span><span class="sxs-lookup"><span data-stu-id="42d60-848">Deploy development environments on Azure</span></span>](deploy-development-environment-azure.md) 
- [<span data-ttu-id="42d60-849">Azure でのテスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="42d60-849">Deploy test environments on Azure</span></span>](deploy-test-environment-azure.md) 
- [<span data-ttu-id="42d60-850">Azure での Retail Essentials 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="42d60-850">Deploy Retail essentials dev/test environments on Azure</span></span>](deploy-retail-essentials-devtest-environment-azure.md) 
- [<span data-ttu-id="42d60-851">Azure での Retail E-commerce 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="42d60-851">Deploy Retail e-Commerce dev/test environments on Azure</span></span>](deploy-retail-ecommerce-devtest-environment-azure.md) 
- [<span data-ttu-id="42d60-852">Azure での Retail Mobility 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="42d60-852">Deploy Retail mobility dev/test environments on Azure</span></span>](deploy-retail-mobility-devtest-environment-azure.md) 
- [<span data-ttu-id="42d60-853">Azure での高可用性環境の配置</span><span class="sxs-lookup"><span data-stu-id="42d60-853">Deploy high-availability environments on Azure</span></span>](deploy-high-availability-environment-azure.md)
