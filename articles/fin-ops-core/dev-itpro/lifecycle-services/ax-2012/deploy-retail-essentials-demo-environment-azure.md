---
title: Azure での Retail Essentials デモ環境の配置
description: このトピックでは、Microsoft Azure にRetail essentials デモを配置する方法について説明します。
author: aamirallaqaband
manager: AnnBe
ms.date: 01/05/2018
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 13352
ms.assetid: be08d43a-f05e-4580-ac75-52710d06a1d7
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 872d0c3804b80d960207ca045b18682c89625dfa
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983748"
---
# <a name="deploy-retail-essentials-demo-environments-on-azure"></a><span data-ttu-id="f4150-103">Azure での Retail Essentials デモ環境の配置</span><span class="sxs-lookup"><span data-stu-id="f4150-103">Deploy Retail essentials demo environments on Azure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4150-104">このトピックでは、Microsoft Azure にRetail essentials デモを配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f4150-104">This topic explains how to deploy a Retail essentials demo environment on Microsoft Azure.</span></span> <span data-ttu-id="f4150-105">環境を展開するには、Microsoft Dynamics Lifecycle Services でクラウド ホスト環境ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="f4150-105">To deploy the environment, you’ll use the Cloud-hosted environments tool in Microsoft Dynamics Lifecycle Services.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f4150-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="f4150-106">Prerequisites</span></span>
<span data-ttu-id="f4150-107">この記事の手順を実行する前に、次の条件が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4150-107">Before you complete the procedures in this article, make sure that the following prerequisites are in place.</span></span>

| <span data-ttu-id="f4150-108">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="f4150-108">Category</span></span>       | <span data-ttu-id="f4150-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="f4150-109">Prerequisite</span></span>                                                                                                                                            |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4150-110">必要なタスク</span><span class="sxs-lookup"><span data-stu-id="f4150-110">Required tasks</span></span> | [<span data-ttu-id="f4150-111">Azure で AX 2012 R3 の配置を計画する</span><span class="sxs-lookup"><span data-stu-id="f4150-111">Plan AX 2012 R3 deployments on Azure</span></span>](plan-2012-r3-deployment-azure.md) |

## <a name="1-log-on-to-lifecycle-services"></a><span data-ttu-id="f4150-112">1. ライフサイクル サービスにログオンする</span><span class="sxs-lookup"><span data-stu-id="f4150-112">1. Log on to Lifecycle Services</span></span>
<span data-ttu-id="f4150-113">Microsoft Dynamics Lifecycle Services は、顧客およびパートナーが Microsoft Dynamics AX の管理に使用できるクラウドベースの共同ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="f4150-113">Microsoft Dynamics Lifecycle Services provides a cloud-based collaborative workspace that customers and partners can use to manage Microsoft Dynamics AX projects.</span></span> <span data-ttu-id="f4150-114">Azure に Dynamics AX を配置するには、この Web サイトを使用します。</span><span class="sxs-lookup"><span data-stu-id="f4150-114">You’ll use this website to deploy Dynamics AX on Azure.</span></span> <span data-ttu-id="f4150-115">Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="f4150-115">Lifecycle Services is available to customers and partners as part of their support plans.</span></span> <span data-ttu-id="f4150-116">CustomerSource または PartnerSource の資格情報でアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="f4150-116">You can access it with your CustomerSource or PartnerSource credentials.</span></span> [<span data-ttu-id="f4150-117">Lifecycle Services にログオン</span><span class="sxs-lookup"><span data-stu-id="f4150-117">Log on to Lifecycle Services</span></span>](https://lcs.dynamics.com/)

## <a name="2-create-a-project"></a><span data-ttu-id="f4150-118">2. プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="f4150-118">2. Create a project</span></span>
<span data-ttu-id="f4150-119">Lifecycle Services にログインした後、既存のプロジェクトを開くか、または新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f4150-119">After you log in to Lifecycle Services, open an existing project, or create a new project.</span></span> <span data-ttu-id="f4150-120">プロジェクトは、Lifecycle Services でのエクスペリエンスの主な開催者です。</span><span class="sxs-lookup"><span data-stu-id="f4150-120">Projects are the key organizer of your experience in Lifecycle Services.</span></span> <span data-ttu-id="f4150-121">プロジェクトに関連する手法は、既定でプロジェクトに含まれるフェーズとタスクを決定します。</span><span class="sxs-lookup"><span data-stu-id="f4150-121">The methodology associated with a project determines which phases and tasks are included in the project by default.</span></span>

## <a name="3-connect-the-project-to-your-azure-subscription"></a><span data-ttu-id="f4150-122">3. Azure サブスクリプションにプロジェクトを接続する</span><span class="sxs-lookup"><span data-stu-id="f4150-122">3. Connect the project to your Azure subscription</span></span>
<span data-ttu-id="f4150-123">Azure サブスクリプションに Lifecycle Services プロジェクトを接続します。</span><span class="sxs-lookup"><span data-stu-id="f4150-123">Connect the Lifecycle Services project to your Azure subscription.</span></span> <span data-ttu-id="f4150-124">これにより、Lifecycle Services は Dynamics AX 環境をサブスクリプションに配置できます。</span><span class="sxs-lookup"><span data-stu-id="f4150-124">This will enable Lifecycle Services to deploy a Dynamics AX environment to the subscription.</span></span> <span data-ttu-id="f4150-125">Azure サブスクリプションにプロジェクトを接続するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f4150-125">To connect the project to your Azure subscription, complete the following procedure.</span></span>

1. <span data-ttu-id="f4150-126">LCS プロジェクトで**環境**セクションに移動して、**Microsoft Azure 設定**をクリックしてから、**Azure コネクタ領域**で**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-126">In your LCS project, go to the **Environments** section, click **Microsoft Azure settings**, and then click **Add** in the **Azure Connectors** area.</span></span> 
   >[!Note]
   > <span data-ttu-id="f4150-127">**Microsoft Azure 設定**オプションは、**クラウド-ホスト環境タイル**をクリックしたときにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="f4150-127">The **Microsoft Azure settings** option is also available when you click the **Cloud-hosted environments** tile.</span></span>
2. <span data-ttu-id="f4150-128">Azure への接続を識別する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4150-128">Enter a name to identify the connection to Azure.</span></span>
3. <span data-ttu-id="f4150-129">Azure サブスクリプション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4150-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="f4150-130">サブスクリプション ID を検索する必要がある場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f4150-130">If you need to find your subscription ID, complete the following steps:</span></span>
   1.  <span data-ttu-id="f4150-131">ブラウザの別のインスタンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="f4150-131">Open another instance of your browser.</span></span>
   2.  <span data-ttu-id="f4150-132">[Azure ポータル](https://ms.portal.azure.com/)にログオンします。</span><span class="sxs-lookup"><span data-stu-id="f4150-132">Log on to the [Azure portal](https://ms.portal.azure.com/).</span></span>
   3.  <span data-ttu-id="f4150-133">左のナビゲーション ウィンドウで、**サブスクリプション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-133">In the navigation pane on the left, click **Subscriptions**.</span></span>

       > [!Note]
       > <span data-ttu-id="f4150-134">下部の **その他のサービス** をクリックしてから **サブスクリプション** をクリックすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="f4150-134">You may need to click **More services** at the bottom, and then click **Subscriptions**.</span></span>

   4.  <span data-ttu-id="f4150-135">サブスクリプション ID をコピーして、Lifecycle Services の **Azure サブスクリプション ID** フィールドに貼り付けます (現在別のブラウザー インスタンスに表示されています)。</span><span class="sxs-lookup"><span data-stu-id="f4150-135">Copy your subscription ID, and then paste it into the **Azure subscription ID** field in Lifecycle Services (which is currently displayed in another browser instance).</span></span>

4. <span data-ttu-id="f4150-136">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-136">Click **Next**.</span></span>
5. <span data-ttu-id="f4150-137">**ダウンロード**をクリックして管理証明書をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="f4150-137">Click **Download** to download a management certificate.</span></span> <span data-ttu-id="f4150-138">この管理証明書により、Lifecycle Services はお客様の代わりに Azure と通信できます。</span><span class="sxs-lookup"><span data-stu-id="f4150-138">This management certificate enables Lifecycle Services to communicate with Azure on your behalf.</span></span> <span data-ttu-id="f4150-139">既定では、管理証明書はコンピューターの**ダウンロード** フォルダーに保存され、**LifecycleServicesDeployment.cer** という名前が付きます。</span><span class="sxs-lookup"><span data-stu-id="f4150-139">By default, the management certificate is saved to the **Downloads** folder on your computer and is named **LifecycleServicesDeployment.cer.**</span></span>
6. <span data-ttu-id="f4150-140">管理証明書を Azure にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="f4150-140">Upload the management certificate to Azure.</span></span> <span data-ttu-id="f4150-141">これを行うには、[[Azure 管理 API 管理証明書をアップロード](https://docs.microsoft.com/azure/azure-api-management-certs)] の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4150-141">To do so, see the instructions in [Upload an Azure Management API Management Certificate](https://docs.microsoft.com/azure/azure-api-management-certs).</span></span>

7. <span data-ttu-id="f4150-142">Lifecycle Services で **Microsoft Azure 設定**パネルを表示するブラウザーに戻ります。</span><span class="sxs-lookup"><span data-stu-id="f4150-142">Go back to the browser that displays the **Microsoft Azure setup** panel in Lifecycle Services.</span></span> <span data-ttu-id="f4150-143">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-143">Click **Next**.</span></span>
8. <span data-ttu-id="f4150-144">地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4150-144">Select a region.</span></span> <span data-ttu-id="f4150-145">AX 2012 R3 環境は、この領域のデータ センターに配置されます。</span><span class="sxs-lookup"><span data-stu-id="f4150-145">The AX 2012 R3 environment will be deployed to a datacenter in this region.</span></span>
9. <span data-ttu-id="f4150-146">**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-146">Click **Connect**.</span></span> <span data-ttu-id="f4150-147">これで、プロジェクトが指定された Azure サブスクリプションに接続できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f4150-147">The project is now connected to the Azure subscription that you specified.</span></span> 

>[!Note]
> <span data-ttu-id="f4150-148">証明書が期限切れになった場合は、新しいものを取得できます。</span><span class="sxs-lookup"><span data-stu-id="f4150-148">If the certificate expires, you can obtain a new one.</span></span> <span data-ttu-id="f4150-149">そのためには次の作業を行います。</span><span class="sxs-lookup"><span data-stu-id="f4150-149">To do so:</span></span>
> 1. <span data-ttu-id="f4150-150">プロジェクトの設定の **Azure コネクタ** 領域で接続を選択し、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-150">Select the connection in the **Azure connectors** area of your project settings, and click **Edit**.</span></span>
> 2. <span data-ttu-id="f4150-151">**Microsoft Azure 設定**パネルが画面の横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4150-151">The **Microsoft Azure setup** panel is displayed on the side of the screen.</span></span> <span data-ttu-id="f4150-152">**ダウンロード**をクリックして新しい証明書をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="f4150-152">Click **Download** to download a new certificate.</span></span>
> 3. <span data-ttu-id="f4150-153">上の手順の手順 6 ～ 9 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="f4150-153">Repeat steps 6-9 of the above procedure.</span></span>

## <a name="4-deploy-a-retail-essentials-demo-environment-on-azure"></a><span data-ttu-id="f4150-154">4. Azure での Retail Essentials デモ環境の配置</span><span class="sxs-lookup"><span data-stu-id="f4150-154">4. Deploy a Retail essentials demo environment on Azure</span></span>
<span data-ttu-id="f4150-155">Azure に Retail Essentials デモ環境を配置するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="f4150-155">Complete the following procedure to deploy a Retail essentials demo environment on Azure.</span></span>

1.  <span data-ttu-id="f4150-156">**クラウド ホスト環境**ページで、**追加** (+) アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-156">On the **Cloud-hosted environments** page, click the **Add** (+) icon.</span></span>
2.  <span data-ttu-id="f4150-157">**環境のトポロジの選択**パネルで、**デモ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4150-157">In the **Select environment topology** panel, select **Demo**.</span></span>
3.  <span data-ttu-id="f4150-158">**Retail Essentials デモ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-158">Click **Retail essentials demo.**</span></span>
4.  <span data-ttu-id="f4150-159">**環境名**フィールドに、配置される環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4150-159">In the **Environment name** field, enter a name for the environment that will be deployed.</span></span>
5.  <span data-ttu-id="f4150-160">**詳細設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-160">Click **Advanced settings**.</span></span>
6.  <span data-ttu-id="f4150-161">仮想マシン名をカスタマイズするには、**仮想マシン名をカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-161">To customize virtual machine names, click **Customize virtual machine names**.</span></span> <span data-ttu-id="f4150-162">一般的な IT 名前付けガイドラインをサポートするために、仮想マシンに名前を付ける機能がほとんどの配置トポロジの**詳細設定**に用意されています。</span><span class="sxs-lookup"><span data-stu-id="f4150-162">In order to support common IT naming guidelines, the ability to name virtual machines is provided through the **Advanced settings** option on most deployment topologies.</span></span> <span data-ttu-id="f4150-163">名前を定義することに加えて、各仮想マシン タイプに開始インデックスを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f4150-163">In addition to defining the name, a starting index can be selected for each virtual machine type.</span></span> <span data-ttu-id="f4150-164">インデックスは、配置される仮想マシン タイプのインスタンスごとに増加します。</span><span class="sxs-lookup"><span data-stu-id="f4150-164">The index is incremented for each instance of the virtual machine type that is deployed.</span></span> <span data-ttu-id="f4150-165">仮想マシン名は 13 文字またはそれ以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4150-165">Virtual machine names must be 13 characters or less.</span></span> <span data-ttu-id="f4150-166">インデックスはマシン名とハイフン (-) で区切られ、その後に最大 2 桁のインデックスが続きます。</span><span class="sxs-lookup"><span data-stu-id="f4150-166">The index is separated from the machine name by a hyphen (-), followed by the index that supports a maximum of 2 digits.</span></span> <span data-ttu-id="f4150-167">例: ACustomVMName-99。</span><span class="sxs-lookup"><span data-stu-id="f4150-167">Example: ACustomVMName-99.</span></span> <span data-ttu-id="f4150-168">最初の展開後に、仮想マシンのインスタンスが環境に追加されるとき、配置サービスは、中断した場所で、仮想マシンの名前の増分を開始します。</span><span class="sxs-lookup"><span data-stu-id="f4150-168">When virtual machine instances are added to an environment after the initial deployment, the deployment service will start incrementing the virtual machine name where it left off.</span></span> <span data-ttu-id="f4150-169">たとえば、2 で始まるインデックスを持つ 4 つの AOS 仮想マシンを展開する場合、最後の AOS インスタンス名は AOS-6 になります。</span><span class="sxs-lookup"><span data-stu-id="f4150-169">For example, if you deployed four AOS virtual machines with a starting index of 2, then the last AOS instance name will be AOS-6.</span></span> <span data-ttu-id="f4150-170">もう 2 つ AOS インスタンスを追加する場合は、AOS-7 と AOS 8 になります。</span><span class="sxs-lookup"><span data-stu-id="f4150-170">If you add two more AOS instances, they will be AOS-7 and AOS-8.</span></span> <span data-ttu-id="f4150-171">展開内の仮想マシン タイプの 1 つがカスタマイズされている場合は、すべての仮想マシン名をカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4150-171">If one of the virtual machine types in your deployment is customized, then all of the virtual machine names must be customized.</span></span> <span data-ttu-id="f4150-172">これは、仮想マシン名が誤って紛失してしまったため、長期的な展開が発生しないようにするためです。</span><span class="sxs-lookup"><span data-stu-id="f4150-172">This is done to ensure that a long deployment does not occur because a virtual machine name was accidentally missed.</span></span>
7.  <span data-ttu-id="f4150-173">仮想ネットワークの設定をカスタマイズするには、**仮想ネットワークをカスタマイズする** 設定をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-173">To customize virtual network settings, click **Customize virtual network** settings.</span></span> <span data-ttu-id="f4150-174">情報を入力するには、次の表を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f4150-174">Then use the following table to enter information.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f4150-175">以下を行う場合:</span><span class="sxs-lookup"><span data-stu-id="f4150-175">If you want to:</span></span></th>
    <th><span data-ttu-id="f4150-176">手順</span><span class="sxs-lookup"><span data-stu-id="f4150-176">Do this:</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="f4150-177">Azure で環境用に新しい仮想ネットワークを作成する</span><span class="sxs-lookup"><span data-stu-id="f4150-177">Create a new virtual network in Azure for the environment</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f4150-178"><strong>新しい仮想ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-178">Click <strong>New virtual network</strong>.</span></span></li>
    <li><span data-ttu-id="f4150-179">仮想ネットワーク名を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4150-179">Enter a name for the virtual network.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f4150-180">Azure の既存の仮想ネットワークへの環境の追加</span><span class="sxs-lookup"><span data-stu-id="f4150-180">Add the environment to an existing virtual network in Azure</span></span></td>
    <td><ol>
    <li><span data-ttu-id="f4150-181"><strong>既存の仮想ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-181">Click <strong>Existing virtual network</strong>.</span></span></li>
    <li><span data-ttu-id="f4150-182">使用する既存の仮想ネットワークの名前を選択してください。</span><span class="sxs-lookup"><span data-stu-id="f4150-182">Select the name of the existing virtual network that you want to use.</span></span> <span data-ttu-id="f4150-183"><strong>アプリケーションのサブネット名</strong> および <strong>アドレス スペース</strong> フィールドには、選択した仮想ネットワークに基づいて適切な情報が自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4150-183">The <strong>Application subnet name</strong> and <strong>Address space</strong> fields will automatically display the appropriate information based on the virtual network that you selected.</span></span> <span data-ttu-id="f4150-184">これらのフィールドの情報を確認する場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="f4150-184">If you want to verify the information in these fields, do this:</span></span> <ol>
    <li><span data-ttu-id="f4150-185"><a href="https://ms.portal.azure.com/">Azure ポータル</a>にログオンします。</span><span class="sxs-lookup"><span data-stu-id="f4150-185">Log on to the <a href="https://ms.portal.azure.com/">Azure portal</a>.</span></span></li>
    <li><span data-ttu-id="f4150-186">左のナビゲーション ウィンドウで、 <strong>仮想ネットワーク</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-186">In the navigation pane on the left, click <strong>Virtual networks</strong>.</span></span></li>
    <li><span data-ttu-id="f4150-187">使用する仮想ネットワークの名前をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-187">Click the name of the virtual network that you’re going to use.</span></span></li>
    <li><span data-ttu-id="f4150-188"><strong>構成</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-188">Click <strong>Configure</strong>.</span></span> <span data-ttu-id="f4150-189">仮想ネットワークに関する詳細は、ページに記載されています。</span><span class="sxs-lookup"><span data-stu-id="f4150-189">Details about the virtual network are listed on the page.</span></span></li>
    <li><span data-ttu-id="f4150-190"><strong>完了</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-190">Click <strong>Done</strong>.</span></span> <span data-ttu-id="f4150-191"><strong>環境の展開</strong> パネルが再表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4150-191">The <strong>Deploy environment</strong> panel is redisplayed.</span></span></li>
    <li><span data-ttu-id="f4150-192">配置される仮想マシンの数とサイズが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4150-192">The number and size of each virtual machine that will be deployed is listed.</span></span> <span data-ttu-id="f4150-193">必要に応じて、仮想マシンの数とサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="f4150-193">Change the number and size of the virtual machines, as needed.</span></span></li>
    </ol></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

    -   <span data-ttu-id="f4150-194">この環境で各仮想マシンにインストールされているソフトウェアの詳細については、 [Azure 上での AX 2012 R3の 配置計画](plan-2012-r3-deployment-azure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4150-194">For information about the software installed on each virtual machine in this environment, see [Plan AX 2012 R3 deployments on Azure](plan-2012-r3-deployment-azure.md).</span></span>
    -   <span data-ttu-id="f4150-195">仮想マシンに関するサイズおよび価格決定の詳細については、[仮想マシンの価格決定の詳細](https://azure.microsoft.com/pricing/details/virtual-machines/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4150-195">For sizing and pricing details about virtual machines, see [Virtual machines pricing details](https://azure.microsoft.com/pricing/details/virtual-machines/).</span></span>

8.  <span data-ttu-id="f4150-196">ライセンスの条項を確認するには、**ソフトウェア ライセンス条項**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-196">Click **Software License Terms** to review the licensing terms and conditions.</span></span> <span data-ttu-id="f4150-197">次に、チェック ボックスを選択して、条件に同意することを示します。</span><span class="sxs-lookup"><span data-stu-id="f4150-197">Then select the check box to indicate that you agree to the terms.</span></span>
9.  <span data-ttu-id="f4150-198">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-198">Click **Next**.</span></span>
10. <span data-ttu-id="f4150-199">**展開**をクリックして、環境を展開する準備が整ったことを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4150-199">Click **Deploy** to confirm that you’re ready to deploy the environment.</span></span> <span data-ttu-id="f4150-200">配置には数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f4150-200">The deployment may take a few hours to complete.</span></span> <span data-ttu-id="f4150-201">配置が完了すると、**クラウド ホスト環境** ページの配置ステータス列に **配置済み** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4150-201">When the deployment is done, the Deployment Status column on the **Cloud-hosted environments** page will display **Deployed**.</span></span> <span data-ttu-id="f4150-202">(これを表示するにはブラウザーを更新する必要があります。) 配置が失敗すると、すぐエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="f4150-202">(You may need to refresh your browser to see this.)If the deployment fails, you may see an error message right away.</span></span> <span data-ttu-id="f4150-203">配置プロセスでエラーが後に発生する場合に、エラーの詳細がページの右側の詳細ペインに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4150-203">If the error occurs later in the deployment process, error details will be displayed in the details pane on the right-side of the page.</span></span>

## <a name="5-open-the-dynamics-ax-client"></a><span data-ttu-id="f4150-204">5. Dynamics AX クライアントを開く</span><span class="sxs-lookup"><span data-stu-id="f4150-204">5. Open the Dynamics AX client</span></span>
<span data-ttu-id="f4150-205">Dynamics AX クライアントがインストールされている仮想マシンに接続するには、以下の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="f4150-205">Complete the following procedure to connect to the virtual machine where the Dynamics AX client is installed.</span></span>

1.  <span data-ttu-id="f4150-206">**クラウド ホスト環境ページ**で、配置した Retail Essentials 環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4150-206">On the **Cloud-hosted environments page**, select the Retail essentials environment that you just deployed.</span></span>
2.  <span data-ttu-id="f4150-207">環境のプロパティを表示するためにページの右側にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="f4150-207">Scroll to the right side of the page to view the properties of the environment.</span></span>
3.  <span data-ttu-id="f4150-208">**DEMO-&lt;GUID&gt;** リンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4150-208">Click the **DEMO-&lt;GUID&gt;** link.</span></span>
4.  <span data-ttu-id="f4150-209">ページの下部にある**開く**をクリックして、.rdp ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f4150-209">At the bottom of the page, click **Open** to open the .rdp file.</span></span>
5.  <span data-ttu-id="f4150-210">資格情報を求めるメッセージが表示されたら、&lt;DomainName&gt; 管理者アカウントのユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f4150-210">When prompted for credentials, enter the user name and password for the &lt;DomainName&gt;Administrator account.</span></span> <span data-ttu-id="f4150-211">このアカウントのパスワードはこの環境の **クラウド ホスト環境** ページで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="f4150-211">You can find the password for this account on the **Cloud-hosted environments** page for this environment.</span></span>
6.  <span data-ttu-id="f4150-212">仮想マシンのデスクトップが表示されたとき、**Microsoft Dynamics AX** アイコンをクリックして、Microsoft Dynamics AX クライアントを開きます。</span><span class="sxs-lookup"><span data-stu-id="f4150-212">When the virtual machine’s desktop is displayed, click the **Microsoft Dynamics AX** icon to open the Microsoft Dynamics AX client.</span></span>





