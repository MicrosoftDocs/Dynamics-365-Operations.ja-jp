---
title: Azure での Retail Essentials 開発/テスト環境の配置
description: このトピックでは、Microsoft Azure に Retail essentials 開発環境またはテスト環境を配置する方法について説明します。
author: aamirallaqaband
manager: AnnBe
ms.date: 01/05/2018
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 13261
ms.assetid: 00e58780-7373-4c53-b3af-1e9d3d4eebff
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 42b10719b68da13e0c5400c068f89757e05ac836
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128651"
---
# <a name="deploy-retail-essentials-devtest-environments-on-azure"></a><span data-ttu-id="33ff1-103">Azure での Retail Essentials 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="33ff1-103">Deploy Retail essentials dev/test environments on Azure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33ff1-104">このトピックでは、Microsoft Azure に Retail essentials 開発環境またはテスト環境を配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-104">This topic explains how to deploy a Retail essentials dev/test environment on Microsoft Azure.</span></span> <span data-ttu-id="33ff1-105">環境を配置するには、Microsoft Dynamics Lifecycle Services でクラウド ホスト環境ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-105">To deploy the environment, you’ll use the cloud-hosted environments tool in Microsoft Dynamics Lifecycle Services.</span></span>

<a name="prerequisites"></a><span data-ttu-id="33ff1-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="33ff1-106">Prerequisites</span></span>
-------------

<span data-ttu-id="33ff1-107">このトピックの手順を実行する前に、次の条件が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-107">Before you complete the procedures in this topic, make sure that the following prerequisites are in place.</span></span>

| <span data-ttu-id="33ff1-108">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="33ff1-108">Category</span></span>       | <span data-ttu-id="33ff1-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="33ff1-109">Prerequisite</span></span>                                                                                                                                                    |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ff1-110">必要なタスク</span><span class="sxs-lookup"><span data-stu-id="33ff1-110">Required tasks</span></span> | [<span data-ttu-id="33ff1-111">Azure で AX 2012 R3 の配置を計画する</span><span class="sxs-lookup"><span data-stu-id="33ff1-111">Plan AX 2012 R3 deployments on Azure</span></span>](plan-2012-r3-deployment-azure.md) |

## <a name="1-log-on-to-lifecycle-services"></a><span data-ttu-id="33ff1-112">1. ライフサイクル サービスにログオンする</span><span class="sxs-lookup"><span data-stu-id="33ff1-112">1. Log on to Lifecycle Services</span></span>
<span data-ttu-id="33ff1-113">Microsoft Dynamics Lifecycle Services (LCS) は、顧客およびパートナーが Dynamics AX のプロジェクトの管理に使用できるクラウドベースの共同ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="33ff1-113">Microsoft Dynamics Lifecycle Services (LCS) provides a cloud-based collaborative workspace that customers and partners can use to manage Dynamics AX projects.</span></span> <span data-ttu-id="33ff1-114">Azure に Dynamics AX を配置するには、この Web サイトを使用します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-114">You’ll use this website to deploy Dynamics AX on Azure.</span></span> <span data-ttu-id="33ff1-115">Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-115">Lifecycle Services is available to customers and partners as part of their support plans.</span></span> <span data-ttu-id="33ff1-116">CustomerSource または PartnerSource の資格情報でアクセスすることができます。詳細については、[Lifecycle Services にログオン](https://lcs.dynamics.com/en/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-116">You can access it with your CustomerSource or PartnerSource credentials, for details see [Log on to Lifecycle Services](https://lcs.dynamics.com/en/).</span></span>

## <a name="2-create-a-project"></a><span data-ttu-id="33ff1-117">2. プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="33ff1-117">2. Create a project</span></span>
<span data-ttu-id="33ff1-118">LCS にログインした後、既存のプロジェクトを開くか、または新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-118">After you log in to LCS, open an existing project, or create a new project.</span></span> <span data-ttu-id="33ff1-119">プロジェクトは、LCS でのエクスペリエンスの主な開催者です。</span><span class="sxs-lookup"><span data-stu-id="33ff1-119">Projects are the key organizer of your experience in LCS.</span></span> <span data-ttu-id="33ff1-120">プロジェクトに関連する手法は、既定でプロジェクトに含まれるフェーズとタスクを決定します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-120">The methodology associated with a project determines which phases and tasks are included in the project by default.</span></span>

## <a name="3-connect-the-project-to-your-azure-subscription"></a><span data-ttu-id="33ff1-121">3. Azure サブスクリプションにプロジェクトを接続する</span><span class="sxs-lookup"><span data-stu-id="33ff1-121">3. Connect the project to your Azure subscription</span></span>
<span data-ttu-id="33ff1-122">Azure サブスクリプションに LCS プロジェクトを接続します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-122">Connect the LCS project to your Azure subscription.</span></span> <span data-ttu-id="33ff1-123">これにより、LCS は Dynamics AX 環境をサブスクリプションに展開できます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-123">This will enable LCS to deploy a Dynamics AX environment to the subscription.</span></span> <span data-ttu-id="33ff1-124">Azure サブスクリプションにプロジェクトを接続するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-124">To connect the project to your Azure subscription, complete the following procedure.</span></span>

1. <span data-ttu-id="33ff1-125">LCS プロジェクトで **環境** セクションに移動して、**Microsoft Azure 設定** をクリックしてから、**Azure コネクタ領域** で **追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-125">In your LCS project, go to the **Environments** section, click **Microsoft Azure settings**, and then click **Add** in the **Azure Connectors** area.</span></span> 
   >[!Note]
   > <span data-ttu-id="33ff1-126">**Microsoft Azure 設定** オプションは、**クラウド-ホスト環境タイル** をクリックしたときにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-126">The **Microsoft Azure settings** option is also available when you click the **Cloud-hosted environments** tile.</span></span>
2. <span data-ttu-id="33ff1-127">Azure への接続を識別する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-127">Enter a name to identify the connection to Azure.</span></span>
3. <span data-ttu-id="33ff1-128">Azure サブスクリプション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-128">Enter your Azure subscription ID.</span></span> <span data-ttu-id="33ff1-129">サブスクリプション ID を検索する必要がある場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-129">If you need to find your subscription ID, complete the following steps:</span></span>
   1.  <span data-ttu-id="33ff1-130">ブラウザの別のインスタンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-130">Open another instance of your browser.</span></span>
   2.  <span data-ttu-id="33ff1-131">[Azure ポータル](https://ms.portal.azure.com/)にログオンします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-131">Log on to the [Azure portal](https://ms.portal.azure.com/).</span></span>
   3.  <span data-ttu-id="33ff1-132">左のナビゲーション ウィンドウで、**サブスクリプション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-132">In the navigation pane on the left, click **Subscriptions**.</span></span> 

       > [!Note]
       > <span data-ttu-id="33ff1-133">下部の **その他のサービス** をクリックしてから **サブスクリプション** をクリックすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-133">You may need to click **More services** at the bottom, and then click **Subscriptions**.</span></span>

   4.  <span data-ttu-id="33ff1-134">サブスクリプション ID をコピーして、LCS の **Azure サブスクリプション ID** フィールドに貼り付けます (現在別のブラウザー インスタンスに表示されています)。</span><span class="sxs-lookup"><span data-stu-id="33ff1-134">Copy your subscription ID, and then paste it into the **Azure subscription ID** field in LCS (which is currently displayed in another browser instance).</span></span>

4. <span data-ttu-id="33ff1-135">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-135">Click **Next**.</span></span>
5. <span data-ttu-id="33ff1-136">**ダウンロード** をクリックして管理証明書をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-136">Click **Download** to download a management certificate.</span></span> <span data-ttu-id="33ff1-137">この管理証明書により、LCS はお客様の代わりに Azure と通信できます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-137">This management certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="33ff1-138">既定では、管理証明書はコンピューターの **ダウンロード** フォルダーに保存され、**LifecycleServicesDeployment.cer** という名前が付きます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-138">By default, the management certificate is saved to the **Downloads** folder on your computer and is named **LifecycleServicesDeployment.cer.**</span></span>
6. <span data-ttu-id="33ff1-139">管理証明書を Azure にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-139">Upload the management certificate to Azure.</span></span> <span data-ttu-id="33ff1-140">これを行うには、[[Azure 管理 API 管理証明書をアップロード](https://docs.microsoft.com/azure/azure-api-management-certs)] の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-140">To do so, see the instructions in [Upload an Azure Management API Management Certificate](https://docs.microsoft.com/azure/azure-api-management-certs).</span></span>

7. <span data-ttu-id="33ff1-141">LCS で **Microsoft Azure 設定** パネルを表示するブラウザーに戻ります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-141">Go back to the browser that displays the **Microsoft Azure setup** panel in LCS.</span></span> <span data-ttu-id="33ff1-142">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-142">Click **Next**.</span></span>
8. <span data-ttu-id="33ff1-143">地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-143">Select a region.</span></span> <span data-ttu-id="33ff1-144">AX 2012 R3 環境は、この領域のデータ センターに配置されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-144">The AX 2012 R3 environment will be deployed to a datacenter in this region.</span></span>
9. <span data-ttu-id="33ff1-145">**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-145">Click **Connect**.</span></span> <span data-ttu-id="33ff1-146">これで、プロジェクトが指定された Azure サブスクリプションに接続できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="33ff1-146">The project is now connected to the Azure subscription that you specified.</span></span> 

>[!Note]
> <span data-ttu-id="33ff1-147">証明書が期限切れになった場合は、新しいものを取得できます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-147">If the certificate expires, you can obtain a new one.</span></span> <span data-ttu-id="33ff1-148">そのためには次の作業を行います。</span><span class="sxs-lookup"><span data-stu-id="33ff1-148">To do so:</span></span>
> 1. <span data-ttu-id="33ff1-149">プロジェクトの設定の **Azure コネクタ** 領域で接続を選択し、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-149">Select the connection in the **Azure connectors** area of your project settings, and click **Edit**.</span></span>
> 2. <span data-ttu-id="33ff1-150">**Microsoft Azure 設定** パネルが画面の横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-150">The **Microsoft Azure setup** panel is displayed on the side of the screen.</span></span> <span data-ttu-id="33ff1-151">**ダウンロード** をクリックして新しい証明書をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-151">Click **Download** to download a new certificate.</span></span>
> 3. <span data-ttu-id="33ff1-152">上の手順の手順 6 ～ 9 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-152">Repeat steps 6-9 of the above procedure.</span></span>

## <a name="4-deploy-a-retail-essentials-devtest-environment-on-azure"></a><span data-ttu-id="33ff1-153">4. Azure での Retail Essentials 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="33ff1-153">4. Deploy a Retail essentials dev/test environment on Azure</span></span>
<span data-ttu-id="33ff1-154">Azure に Retail Essentials 開発/テスト環境を配置するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-154">Complete the following procedure to deploy a Retail essentials dev/test environment on Azure.</span></span>

1. <span data-ttu-id="33ff1-155">**クラウド ホスト環境** ページで、**追加** (**+**) アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-155">On the **Cloud-hosted environments** page, click the **Add** (**+**) icon.</span></span>
2. <span data-ttu-id="33ff1-156">**環境のトポロジの選択** パネルで、**開発/テスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-156">In the **Select environment topology** panel, select **Dev/Test**.</span></span>
3. <span data-ttu-id="33ff1-157">**Retail Essentials 開発/テスト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-157">Click **Retail essentials dev/test**.</span></span>
4. <span data-ttu-id="33ff1-158">**環境名** フィールドに、配置される環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-158">In the **Environment name** field, enter a name for the environment that will be deployed.</span></span>
5. <span data-ttu-id="33ff1-159">**詳細設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-159">Click **Advanced settings**.</span></span>
6. <span data-ttu-id="33ff1-160">ドメイン設定をカスタマイズするには、**ドメイン設定をカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-160">To customize domain settings, click **Customize domain settings**.</span></span> <span data-ttu-id="33ff1-161">情報を入力するには、次の表を使用してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-161">Use the following table to enter information.</span></span>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th><span data-ttu-id="33ff1-162">以下を行う場合</span><span class="sxs-lookup"><span data-stu-id="33ff1-162">If you want to</span></span></th>
   <th><span data-ttu-id="33ff1-163">操作</span><span class="sxs-lookup"><span data-stu-id="33ff1-163">Do this</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td><span data-ttu-id="33ff1-164">Azure で環境用に新しいドメインを作成する</span><span class="sxs-lookup"><span data-stu-id="33ff1-164">Create a new domain in Azure for the environment</span></span></td>
   <td><ol>
   <li><span data-ttu-id="33ff1-165"><strong>新規ドメイン</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-165">Click <strong>New domain</strong>.</span></span></li>
   <li><span data-ttu-id="33ff1-166">ドメイン名を入力します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-166">Enter a name for the domain.</span></span> <span data-ttu-id="33ff1-167">既定では、ドメインは <em>contoso.com</em> と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-167">By default, the domain is named <em>contoso.com</em>.</span></span></li>
   </ol></td>
   </tr>
   <tr class="even">
   <td><span data-ttu-id="33ff1-168">Azure の既存のドメインへの環境の追加</span><span class="sxs-lookup"><span data-stu-id="33ff1-168">Add the environment to an existing domain in Azure</span></span></td>
   <td><ol>
   <li><span data-ttu-id="33ff1-169"><strong>既存のドメイン</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-169">Click <strong>Existing domain</strong>.</span></span></li>
   <li><span data-ttu-id="33ff1-170">ドメイン名を入力します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-170">Enter the name of the domain.</span></span> <span data-ttu-id="33ff1-171">たとえば、<em>contoso.com</em>。</span><span class="sxs-lookup"><span data-stu-id="33ff1-171">For example, <em>contoso.com</em>.</span></span></li>
   </ol></td>
   </tr>
   </tbody>
   </table>

7. <span data-ttu-id="33ff1-172">ドメインで作成されるサービス アカウントをカスタマイズするには、**サービス アカウントをカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-172">To customize the service accounts that will be created in the domain, click **Customize service accounts**.</span></span> <span data-ttu-id="33ff1-173">展開の **詳細設定** オプションを通じてサービス アカウントやサービス アカウントのパスワードを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-173">Service accounts and/or service account passwords can be specified through the **Advanced Settings** option for a deployment.</span></span> <span data-ttu-id="33ff1-174">どちらもが指定されていない場合は、既定の勘定が使用され、ランダムなパスワードが選択されています。</span><span class="sxs-lookup"><span data-stu-id="33ff1-174">If neither is provided, default accounts are used and random passwords are selected.</span></span> <span data-ttu-id="33ff1-175">次の機能は、企業のアカウントの命名規則とパスワードの規則を管理する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-175">Use these features when you want to maintain account naming and password rules for your corporation.</span></span> <span data-ttu-id="33ff1-176">アカウントとパスワードのルール:</span><span class="sxs-lookup"><span data-stu-id="33ff1-176">Account and password rules:</span></span>
   - <span data-ttu-id="33ff1-177">有効なサービス名は、特殊文字を含まない 20 文字未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-177">A valid service name must be less than 20 characters with no special characters.</span></span>
   - <span data-ttu-id="33ff1-178">有効なパスワードは 8 文字以上で、大文字、小文字、数字、および次の文字のうち少なくとも 1 つが含まれます: \['@', '!', '=', '\*'\] 次のような一般的なパスワードは使用できません: pass@word1</span><span class="sxs-lookup"><span data-stu-id="33ff1-178">A valid password must be more than 8 characters and contain uppercase letters, lowercase letters, numbers, and at least one of the following characters: \['@', '!', '=', '\*'\] You can’t use common passwords, such as: pass@word1</span></span>

8. <span data-ttu-id="33ff1-179">使用を希望する AX 2012 R3 のバージョンを選択するには、**サポートされているバージョン** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-179">To select the version of AX 2012 R3 that you want use, click **Supported version**.</span></span> <span data-ttu-id="33ff1-180">既定では、この環境の AX 2012 R3 CU8 バージョンが配置されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-180">By default, the AX 2012 R3 CU8 version of this environment will be deployed.</span></span> <span data-ttu-id="33ff1-181">CU8 バージョンを使用しない場合は、**Dynamics ERP 2012 R3 RTM** をリストから選択します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-181">If you don’t want to use the CU8 version, select **Dynamics ERP 2012 R3 RTM** from the list.</span></span>
9. <span data-ttu-id="33ff1-182">仮想マシン名をカスタマイズするには、**仮想マシン名をカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-182">To customize virtual machine names, click **Customize virtual machine names**.</span></span> <span data-ttu-id="33ff1-183">一般的な IT 名前付けガイドラインをサポートするために、仮想マシンに名前を付ける機能がほとんどの配置トポロジの **詳細設定** に用意されています。</span><span class="sxs-lookup"><span data-stu-id="33ff1-183">In order to support common IT naming guidelines, the ability to name virtual machines is provided through the **Advanced settings** option on most deployment topologies.</span></span> <span data-ttu-id="33ff1-184">名前を定義することに加えて、各仮想マシン タイプに開始インデックスを選択できます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-184">In addition to defining the name, a starting index can be selected for each virtual machine type.</span></span> <span data-ttu-id="33ff1-185">インデックスは、配置される仮想マシン タイプのインスタンスごとに増加します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-185">The index is incremented for each instance of the virtual machine type that is deployed.</span></span> <span data-ttu-id="33ff1-186">仮想マシン名は 13 文字またはそれ以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-186">Virtual machine names must be 13 characters or less.</span></span> <span data-ttu-id="33ff1-187">インデックスはマシン名とハイフン (-) で区切られ、その後に最大 2 桁のインデックスが続きます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-187">The index is separated from the machine name by a hyphen (-), followed by the index that supports a maximum of 2 digits.</span></span> <span data-ttu-id="33ff1-188">例: ACustomVMName-99。</span><span class="sxs-lookup"><span data-stu-id="33ff1-188">Example: ACustomVMName-99.</span></span> <span data-ttu-id="33ff1-189">最初の展開後に、仮想マシンのインスタンスが環境に追加されるとき、配置サービスは、中断した場所で、仮想マシンの名前の増分を開始します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-189">When virtual machine instances are added to an environment after the initial deployment, the deployment service will start incrementing the virtual machine name where it left off.</span></span> <span data-ttu-id="33ff1-190">たとえば、2 で始まるインデックスを持つ 4 つの AOS 仮想マシンを展開する場合、最後の AOS インスタンス名は AOS-6 になります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-190">For example, if you deployed four AOS virtual machines with a starting index of 2, then the last AOS instance name will be AOS-6.</span></span> <span data-ttu-id="33ff1-191">もう 2 つ AOS インスタンスを追加する場合は、AOS-7 と AOS 8 になります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-191">If you add two more AOS instances, they will be AOS-7 and AOS-8.</span></span> <span data-ttu-id="33ff1-192">展開内の仮想マシン タイプの 1 つがカスタマイズされている場合は、すべての仮想マシン名をカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-192">If one of the virtual machine types in your deployment is customized, then all of the virtual machine names must be customized.</span></span> <span data-ttu-id="33ff1-193">これは、仮想マシン名が誤って紛失してしまったため、長期的な展開が発生しないようにするためです。</span><span class="sxs-lookup"><span data-stu-id="33ff1-193">This is done to ensure that a long deployment does not occur because a virtual machine name was accidentally missed.</span></span>
10. <span data-ttu-id="33ff1-194">仮想ネットワークの設定をカスタマイズするには、<strong>仮想ネットワークをカスタマイズする</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-194">To customize virtual network settings, click <strong>Customize virtual network</strong>.</span></span> <span data-ttu-id="33ff1-195">情報を入力するには、次の表を使用してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-195">Use the following table to enter information.</span></span>
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="33ff1-196">以下を行う場合</span><span class="sxs-lookup"><span data-stu-id="33ff1-196">If you want to</span></span></th>
    <th><span data-ttu-id="33ff1-197">操作</span><span class="sxs-lookup"><span data-stu-id="33ff1-197">Do this</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="33ff1-198">Azure で環境用に新しい仮想ネットワークを作成する</span><span class="sxs-lookup"><span data-stu-id="33ff1-198">Create a new virtual network in Azure for the environment</span></span></td>
    <td><ol>
    <li><span data-ttu-id="33ff1-199"><strong>新しい仮想ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-199">Click <strong>New virtual network</strong>.</span></span></li>
    <li><span data-ttu-id="33ff1-200">仮想ネットワーク名を入力します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-200">Enter a name for the virtual network.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="33ff1-201">Azure の既存の仮想ネットワークへの環境の追加</span><span class="sxs-lookup"><span data-stu-id="33ff1-201">Add the environment to an existing virtual network in Azure</span></span></td>
    <td><ol>
    <li><span data-ttu-id="33ff1-202"><strong>既存の仮想ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-202">Click <strong>Existing virtual network</strong>.</span></span></li>
    <li><span data-ttu-id="33ff1-203">使用する既存の仮想ネットワークの名前を選択してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-203">Select the name of the existing virtual network that you want to use.</span></span></li>
    <li><span data-ttu-id="33ff1-204"><strong>アドレス空間</strong> フィールドには、適切な値が自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-204">The <strong>Address space</strong> field will automatically display the appropriate value.</span></span> <span data-ttu-id="33ff1-205">提供された値を選択します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-205">Select the provided value.</span></span></li>
    <li><span data-ttu-id="33ff1-206"><strong>アプリケーション サブネット名</strong> フィールドには、使用可能なオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-206">The <strong>Application subnet name</strong> field will display available options.</span></span> <span data-ttu-id="33ff1-207">Lifecycle Servicesによって以前に展開した広告に配置する場合は、選択した <strong>APPNET</strong> 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-207">If you are deploying to an AD that was previously deployed through Lifecycle Services, select the <strong>APPNET</strong> value.</span></span></li>
    <li><span data-ttu-id="33ff1-208">Active Directory サブネットを入力する必要があり、ターゲットとする AD の Azure 管理ポータルにある Active Directory サブネット IP/範囲と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-208">The Active Directory subnet must be entered and match the Active Directory subnet IP/Range found in the Azure management portal for the AD you want to target.</span></span>
    <ol>
    <li><span data-ttu-id="33ff1-209"><a href="https://ms.portal.azure.com/">Azure ポータル</a>にログオンします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-209">Log on to the <a href="https://ms.portal.azure.com/">Azure portal</a>.</span></span></li>
    <li><span data-ttu-id="33ff1-210">左のナビゲーション ウィンドウで、 <strong>仮想ネットワーク</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-210">In the navigation pane on the left, click <strong>Virtual networks</strong>.</span></span></li>
    <li><span data-ttu-id="33ff1-211">使用する仮想ネットワークの名前をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-211">Click the name of the virtual network that you’re going to use.</span></span></li>
    <li><span data-ttu-id="33ff1-212"><strong>構成</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-212">Click <strong>Configure</strong>.</span></span> <span data-ttu-id="33ff1-213">仮想ネットワークに関する詳細は、ページに記載されています。</span><span class="sxs-lookup"><span data-stu-id="33ff1-213">Details about the virtual network are listed on the page.</span></span></li>
    </ol></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

11. <span data-ttu-id="33ff1-214">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-214">Click **Done**.</span></span> <span data-ttu-id="33ff1-215">**環境** **の展開** パネルが再表示されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-215">The **Deploy** **environment** panel is redisplayed.</span></span>
12. <span data-ttu-id="33ff1-216">配置される仮想マシンの数とサイズが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-216">The number and size of each virtual machine that will be deployed is listed.</span></span> <span data-ttu-id="33ff1-217">必要に応じて、仮想マシンの数とサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-217">Change the number and size of the virtual machines, as needed.</span></span>
    -   <span data-ttu-id="33ff1-218">この環境で各仮想マシンにインストールされているソフトウェアの詳細については、 [Azure 上での AX 2012 R3の 配置計画](plan-2012-r3-deployment-azure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-218">For information about the software installed on each virtual machine in this environment, see [Plan AX 2012 R3 deployments on Azure](plan-2012-r3-deployment-azure.md).</span></span>
    -   <span data-ttu-id="33ff1-219">仮想マシンに関するサイズおよび価格決定の詳細については、[仮想マシンの価格決定の詳細](https://azure.microsoft.com/pricing/details/virtual-machines/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-219">For sizing and pricing details about virtual machines, see [Virtual machines pricing details](https://azure.microsoft.com/pricing/details/virtual-machines/).</span></span>

13. <span data-ttu-id="33ff1-220">ライセンスの条項を確認するには、**ソフトウェア ライセンス条項** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-220">Click **Software License Terms** to review the licensing terms and conditions.</span></span> <span data-ttu-id="33ff1-221">次に、チェック ボックスを選択して、条件に同意することを示します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-221">Then select the check box to indicate that you agree to the terms.</span></span>
14. <span data-ttu-id="33ff1-222">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-222">Click **Next**.</span></span>
15. <span data-ttu-id="33ff1-223">**展開** をクリックして、環境を展開する準備が整ったことを確認します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-223">Click **Deploy** to confirm that you’re ready to deploy the environment.</span></span> <span data-ttu-id="33ff1-224">配置には数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-224">The deployment may take a few hours to complete.</span></span> <span data-ttu-id="33ff1-225">配置が完了すると、**クラウド ホスト環境** ページの **配置ステータス** 列に **配置済み** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-225">When the deployment is done, the **Deployment Status** column on the **Cloud-hosted environments** page will display **Deployed**.</span></span> <span data-ttu-id="33ff1-226">(これを表示するにはブラウザーを更新する必要があります。) 配置が失敗すると、すぐエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-226">(You may need to refresh your browser to see this.) If the deployment fails, you may see an error message right away.</span></span> <span data-ttu-id="33ff1-227">配置プロセスでエラーが後に発生する場合に、エラーの詳細がページの右側の詳細ペインに表示されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-227">If the error occurs later in the deployment process, error details will be displayed in the details pane on the right-side of the page.</span></span>

## <a name="5-prepare-the-environment-for-use"></a><span data-ttu-id="33ff1-228">5. 使用する環境を準備</span><span class="sxs-lookup"><span data-stu-id="33ff1-228">5. Prepare the environment for use</span></span>
<span data-ttu-id="33ff1-229">Retail Essentials 環境が Azure に配置されたので、これを設定して使用するためにコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-229">Now that the Retail essentials environment has been deployed on Azure, you must set it up and configure it for use.</span></span> <span data-ttu-id="33ff1-230">詳細については、以降のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-230">See the following sections for more information.</span></span>

### <a name="log-on-to-the-retails-essentials-virtual-machine"></a><span data-ttu-id="33ff1-231">Retail Essentials 仮想マシンにログオンします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-231">Log on to the Retails essentials virtual machine</span></span>

<span data-ttu-id="33ff1-232">ESSEN-&lt;GUID&gt; 仮想マシンに &lt;DomainName&gt;DynamicsInstallUser アカウントを使用してログオンします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-232">Log on to the ESSEN-&lt;GUID&gt; virtual machine using the &lt;DomainName&gt;DynamicsInstallUser account.</span></span> <span data-ttu-id="33ff1-233">手順については、「仮想マシンにどのようにログオンしますか?」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-233">For instructions, see the “How do I log on to a virtual machine?”</span></span> <span data-ttu-id="33ff1-234">トピック [Azure で AX 2012 R3 配置を管理する](manage-2012-r3-deployment-azure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-234">section of the [Manage AX 2012 R3 deployments on Azure](manage-2012-r3-deployment-azure.md) topic.</span></span>

### <a name="compile-dynamics-ax-2012-r3"></a><span data-ttu-id="33ff1-235">Dynamics AX 2012 R3 のコンパイル</span><span class="sxs-lookup"><span data-stu-id="33ff1-235">Compile Dynamics AX 2012 R3</span></span>

<span data-ttu-id="33ff1-236">Ax Build.exe. を使用した Dynamics AX 2012 R3 のコンパイル</span><span class="sxs-lookup"><span data-stu-id="33ff1-236">Compile Dynamics AX 2012 R3 by using AxBuild.exe.</span></span> <span data-ttu-id="33ff1-237">手順については、[X++ から P コードへの AOS の並列コンパイルに対する AxBuild.exe](https://technet.microsoft.com/library/dn528954.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-237">For instructions, see [AxBuild.exe for Parallel Compile on AOS of X++ to p-code](https://technet.microsoft.com/library/dn528954.aspx).</span></span>

### <a name="initialize-dynamics-ax-2012-r3"></a><span data-ttu-id="33ff1-238">Dynamics AX 2012 R3 の初期化</span><span class="sxs-lookup"><span data-stu-id="33ff1-238">Initialize Dynamics AX 2012 R3</span></span>

<span data-ttu-id="33ff1-239">Dynamics AX 2012 R3 クライアントを開いて、初期化チェックリストを完了します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-239">Open the Dynamics AX 2012 R3 client and complete the initialization checklists.</span></span> <span data-ttu-id="33ff1-240">手順については、[初期化チェックリスト](https://technet.microsoft.com/library/aa497061.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-240">For instructions, see [Initialization checklists](https://technet.microsoft.com/library/aa497061.aspx).</span></span>

### <a name="install-sample-data"></a><span data-ttu-id="33ff1-241">サンプル データのインストール</span><span class="sxs-lookup"><span data-stu-id="33ff1-241">Install sample data</span></span>

<span data-ttu-id="33ff1-242">サンプル データを環境にインストールする場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-242">If you want sample data installed in your environment, complete the following steps.</span></span>

1.  <span data-ttu-id="33ff1-243">次の場所に移動します: F:TestTransferTool</span><span class="sxs-lookup"><span data-stu-id="33ff1-243">Go to the following location:F:TestTransferTool</span></span>
2.  <span data-ttu-id="33ff1-244">テスト データ ツールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-244">Install the Test Data Tool.</span></span> <span data-ttu-id="33ff1-245">手順については、 [テスト データ転送ツール (ベータ版) をインストールする](install-test-data-transfer-tool-beta.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-245">For instructions, see [Install the Test Data Transfer Tool (beta)](install-test-data-transfer-tool-beta.md).</span></span>
3.  <span data-ttu-id="33ff1-246">コマンド プロンプトを開いて、次の場所に移動します: C:\Program Files (x86) \Microsoft Dynamics AX 2012 R3 Test Data Transfer Tool (Beta)</span><span class="sxs-lookup"><span data-stu-id="33ff1-246">Open a command prompt and navigate to the following location: C:\Program Files (x86)\Microsoft Dynamics AX 2012 R3 Test Data Transfer Tool (Beta)</span></span>
4.  <span data-ttu-id="33ff1-247">次のコマンドを実行します: dp.exe import F:DemoData MicrosoftDynamicsAx</span><span class="sxs-lookup"><span data-stu-id="33ff1-247">Run the following command: dp.exe import F:DemoData MicrosoftDynamicsAx</span></span>

> [!NOTE]
> <span data-ttu-id="33ff1-248">サンプル データには、Dynamics AX の試用版のライセンス キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="33ff1-248">The sample data includes trial license keys for Dynamics AX.</span></span> <span data-ttu-id="33ff1-249">サンプル データをインストールしないように選択する場合は、開発またはテスト用の試用版ライセンス キーを [CustomerSource](https://mbs.microsoft.com/downloads/customer/AX/AXDemoTools/MicrosoftDynamicsAX2012R2v4DemoLicense.zip) または [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898#FileId=57028) からダウンロードすることができます</span><span class="sxs-lookup"><span data-stu-id="33ff1-249">If you choose not to install the sample data, you can download trial license keys—for development or testing purposes—from [CustomerSource](https://mbs.microsoft.com/downloads/customer/AX/AXDemoTools/MicrosoftDynamicsAX2012R2v4DemoLicense.zip) or [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898#FileId=57028).</span></span>

### <a name="set-up-retail-essentials"></a><span data-ttu-id="33ff1-250">Retail Essentials の設定</span><span class="sxs-lookup"><span data-stu-id="33ff1-250">Set up Retail essentials</span></span>

<span data-ttu-id="33ff1-251">Dynamics AX クライアントを開いて、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-251">Open the Dynamics AX client and complete the following steps.</span></span>

1.  <span data-ttu-id="33ff1-252">**Retail essentials** エリア ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-252">Go to the **Retail essentials** area page.</span></span>
2.  <span data-ttu-id="33ff1-253">**チャネル &gt; 設定** **&gt; 小売パラメーター** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-253">Click **Channels &gt; Setup** **&gt; Retail parameters**.</span></span>
3.  <span data-ttu-id="33ff1-254">**小売パラメーター** フォームで、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-254">In the **Retail parameters** form, complete the following steps:</span></span>
    1.  <span data-ttu-id="33ff1-255">フォーム上部の **初期化** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-255">Click the **Initialize** button at the top of the form.</span></span>
    2.  <span data-ttu-id="33ff1-256">**はい** をクリックして、基本構成データを初期化することを確認します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-256">Click **Yes** to confirm that you want to initialize the base configuration data.</span></span> <span data-ttu-id="33ff1-257">初期化プロセスが完了すると、情報ログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-257">When the initialization process is complete, the Infolog is displayed.</span></span>
    3.  <span data-ttu-id="33ff1-258">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-258">Close the form.</span></span>

4.  <span data-ttu-id="33ff1-259">**データ同期 &gt; 設定 &gt; 小売用スケジューラのパラメーター** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-259">Click **Data synchronization &gt; Setup &gt; Retail scheduler parameters.**</span></span>
5.  <span data-ttu-id="33ff1-260">**小売用スケジューラ パラメーター** フォームで、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-260">In the **Retail scheduler parameters** form, complete the following steps:</span></span>
    1.  <span data-ttu-id="33ff1-261">**サーバー名** フィールドに、仮想マシンの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-261">In the **Server name** field, enter the name of the virtual machine.</span></span>
    2.  <span data-ttu-id="33ff1-262">フォーム上部の **メタデータの同期** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-262">Click the **Sync metadata** button at the top of the form.</span></span>
    3.  <span data-ttu-id="33ff1-263">**はい** をクリックしてメタデータを同期することを確認します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-263">Click **Yes** to confirm that you want to sync the metadata.</span></span> <span data-ttu-id="33ff1-264">このプロセスが完了すると、情報ログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-264">When the process is complete, the Infolog is displayed.</span></span>
    4.  <span data-ttu-id="33ff1-265">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-265">Close the form.</span></span>

6.  <span data-ttu-id="33ff1-266">**データ同期 &gt; 設定 &gt; チャネル統合 &gt; Real-time Service プロファイル** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-266">Click **Data synchronization &gt; Setup &gt; Channel integration &gt; Real-time service profiles.**</span></span>
7.  <span data-ttu-id="33ff1-267">**Commerce Data Exchange: Real-time Service** プロファイル フォームで、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-267">In the **Commerce Data Exchange: Real-time Service Profile** form, complete the following steps:</span></span>
    1.  <span data-ttu-id="33ff1-268">**サーバー名** フィールドに、仮想マシンの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-268">In the **Server name** field, enter the name of the virtual machine.</span></span>
    2.  <span data-ttu-id="33ff1-269">**共通名** フィールドに、証明書の共通名を入力します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-269">In the **Common name** field, enter the common name of the certificate.</span></span>
    3.  <span data-ttu-id="33ff1-270">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-270">Close the form.</span></span>

8.  <span data-ttu-id="33ff1-271">**データ同期 &gt; 設定 &gt; チャネル統合 &gt; 作業フォルダー** とクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-271">Click **Data synchronization &gt; Setup &gt; Channel integration &gt; Working folders.**</span></span>
9.  <span data-ttu-id="33ff1-272">**作業フォルダー** フォームで、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-272">In the **Working folders** form, complete the following steps.</span></span>
    1.  <span data-ttu-id="33ff1-273">**ダウンロード パス** フィールドの場所に注意してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-273">Note the location in the **Download path** field.</span></span> <span data-ttu-id="33ff1-274">通常は C:\DemoFiles\Retail\CDXDownload です。</span><span class="sxs-lookup"><span data-stu-id="33ff1-274">It is typically C:\DemoFiles\Retail\CDXDownload.</span></span> <span data-ttu-id="33ff1-275">C ドライブにこれらのフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-275">Create these folders on the C drive.</span></span>
    2.  <span data-ttu-id="33ff1-276">**アップロード パス** フィールドの場所に注意してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-276">Note the location in the **Upload path** field.</span></span> <span data-ttu-id="33ff1-277">通常は C:\DemoFiles\Retail\CDXUpload です。</span><span class="sxs-lookup"><span data-stu-id="33ff1-277">It is typically C:\DemoFiles\Retail\CDXUpload.</span></span> <span data-ttu-id="33ff1-278">C ドライブにこれらのフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-278">Create these folders on the C drive.</span></span>
    3.  <span data-ttu-id="33ff1-279">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-279">Close the form.</span></span>

10. <span data-ttu-id="33ff1-280">**データ同期 &gt; 設定 &gt; チャネル統合 &gt; チャネル データベース** とクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-280">Click **Data synchronization &gt; Setup &gt; Channel integration &gt; Channel database.**</span></span>
11. <span data-ttu-id="33ff1-281">**チャネル データベース** フォームで、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-281">In the **Channel database** form, complete the following steps:</span></span>
    1.  <span data-ttu-id="33ff1-282">**HoustonStore** レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-282">Select the **HoustonStore** record.</span></span>
    2.  <span data-ttu-id="33ff1-283">フォームの右側にあるウィンドウで、**Retail サーバー** セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-283">In the pane on the right side of the form, go to the **Retail Server** section.</span></span> <span data-ttu-id="33ff1-284">(表示するためにウィンドウの一番下までスクロールしなければならない場合があります。)</span><span class="sxs-lookup"><span data-stu-id="33ff1-284">(You may have to scroll to the bottom of the pane to see it.)</span></span>
    3.  <span data-ttu-id="33ff1-285">**サーバー名** フィールドに、仮想マシンの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-285">In the **Server name** field, enter the name of the virtual machine.</span></span>
    4.  <span data-ttu-id="33ff1-286">フォーム上部の **完全データ同期** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-286">Click the **Full data sync** button at the top of the form.</span></span> <span data-ttu-id="33ff1-287">次に、リストから 9999 配布スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-287">Then, select the 9999 distribution schedule from the list.</span></span> <span data-ttu-id="33ff1-288">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33ff1-288">Click **OK**.</span></span>
    5.  <span data-ttu-id="33ff1-289">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-289">Close the form.</span></span>

## <a name="6-enable-users-to-access-dynamics-ax-2012-r3-on-azure"></a><span data-ttu-id="33ff1-290">6. Azure で Dynamics AX 2012 R3 へのユーザーのアクセスを可能にする</span><span class="sxs-lookup"><span data-stu-id="33ff1-290">6. Enable users to access Dynamics AX 2012 R3 on Azure</span></span>
<span data-ttu-id="33ff1-291">次のセクションでは、企業ユーザーが Dynamics AX 2012 R3 にアクセスできるように、Azure 仮想ネットワークとドメインを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-291">The following sections provide information about how to configure the Azure virtual network and domain so that your corporate users can access Dynamics AX 2012 R3.</span></span>

### <a name="create-a-site-to-site-vpn-connection"></a><span data-ttu-id="33ff1-292">サイト間 VPN 接続を作成する</span><span class="sxs-lookup"><span data-stu-id="33ff1-292">Create a site-to-site VPN connection</span></span>

<span data-ttu-id="33ff1-293">企業ユーザーが Azure 仮想ネットワーク内の仮想マシンのリソースにアクセスできるようにするには、Azure 仮想ネットワークとオンプレミス社内ネットワークの間にサイト間 VPN 接続を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-293">To enable corporate users to access resources on the virtual machines in the Azure virtual network, you’ll need to create a site-to-site VPN connection between the Azure virtual network and your on-premises, corporate network.</span></span> <span data-ttu-id="33ff1-294">これを行う方法の詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-294">For information about how to do this, see:</span></span>

-   [<span data-ttu-id="33ff1-295">仮想ネットワークの概要</span><span class="sxs-lookup"><span data-stu-id="33ff1-295">Virtual network overview</span></span>](https://msdn.microsoft.com/library/windowsazure/jj156007.aspx)
-   [<span data-ttu-id="33ff1-296">仮想ネットワークのコンフィギュレーション タスク</span><span class="sxs-lookup"><span data-stu-id="33ff1-296">Virtual network configuration tasks</span></span>](https://msdn.microsoft.com/library/jj156206.aspx)
-   [<span data-ttu-id="33ff1-297">Windows Server 2012 ルーティングおよびリモート アクセスサービス (RRAS) を使用した Azure 仮想ネットワークのサイト間 VPN</span><span class="sxs-lookup"><span data-stu-id="33ff1-297">Site-to-site VPN in Azure virtual network using Windows Server 2012 Routing and Remote Access Service (RRAS)</span></span>](https://msdn.microsoft.com/library/dn636917.aspx)
-   [<span data-ttu-id="33ff1-298">管理ポータルに仮想ネットワーク ゲートウェイを構成する</span><span class="sxs-lookup"><span data-stu-id="33ff1-298">Configure a virtual network gateway in the management portal</span></span>](https://msdn.microsoft.com/library/azure/jj156210.aspx)

### <a name="create-a-domain-trust"></a><span data-ttu-id="33ff1-299">ドメイン信頼の作成</span><span class="sxs-lookup"><span data-stu-id="33ff1-299">Create a domain trust</span></span>

<span data-ttu-id="33ff1-300">企業ユーザーが Azure ドメイン内の仮想マシンのリソースにアクセスできるようにするには、ドメイン間で Active Directory のトラストを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-300">To enable corporate users to access resources on the virtual machines in your Azure domain, you must create an Active Directory trust between the domains.</span></span> <span data-ttu-id="33ff1-301">信託の作成方法の詳細については、「[フォレスト信託の作成](https://technet.microsoft.com/library/cc754626.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-301">For information about how to create a trust, see [Create a Forest Trust](https://technet.microsoft.com/library/cc754626.aspx).</span></span> <span data-ttu-id="33ff1-302">このプロセスは、2 つのオンプレミス ドメイン間で信頼関係を作成する場合と同じプロセスです。</span><span class="sxs-lookup"><span data-stu-id="33ff1-302">This process is the same process you would use to create a trust between two on-premises domains.</span></span>

### <a name="give-users-access"></a><span data-ttu-id="33ff1-303">ユーザーのアクセス許可を付与します</span><span class="sxs-lookup"><span data-stu-id="33ff1-303">Give users access</span></span>

<span data-ttu-id="33ff1-304">ユーザが Dynamics AX にアクセスできるようにするには、以下のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-304">To enable your users to access Dynamics AX, complete the following tasks:</span></span>

-   <span data-ttu-id="33ff1-305">CLI- &lt;GUID&gt; 仮想マシンのリモート デスクトップ ユーザー グループに各ユーザーのドメイン アカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-305">Add each user’s domain account to the Remote Desktop Users group on the CLI-&lt;GUID&gt; virtual machine.</span></span>
-   <span data-ttu-id="33ff1-306">ユーザーに Dynamics AX へのアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-306">Give users access to Dynamics AX.</span></span> <span data-ttu-id="33ff1-307">手順については、[Microsoft Dynamics AX で新しいユーザーを作成する](https://technet.microsoft.com/library/aa548139.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33ff1-307">For instructions, see [Create new users in Microsoft Dynamics AX](https://technet.microsoft.com/library/aa548139.aspx).</span></span>

> [!NOTE]
> <span data-ttu-id="33ff1-308">VPN 接続とドメイン信頼を作成しない場合でも、ユーザーに Dynamics AX へのアクセス権を付与することができます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-308">If you don’t want to create a VPN connection and a domain trust, you can still give users access to Dynamics AX.</span></span> <span data-ttu-id="33ff1-309">これを行うには、ドメイン コントローラとして機能する仮想マシンにログオンし、各ユーザーのドメイン アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-309">To do so, you’ll need to log on to the virtual machine that serves as the domain controller, and create domain accounts for each user.</span></span> <span data-ttu-id="33ff1-310">その後、上記の 2 つのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-310">Then, you’ll need to complete the two tasks mentioned above.</span></span>

## <a name="7-learn-more-about-the-service-accounts-for-this-environment"></a><span data-ttu-id="33ff1-311">7. この環境のサービス アカウントに関する詳細</span><span class="sxs-lookup"><span data-stu-id="33ff1-311">7. Learn more about the service accounts for this environment</span></span>
<span data-ttu-id="33ff1-312">次のセクションでは、環境を配置したときに作成されたサービス アカウントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-312">The following sections provide information about the service accounts that were created when you deployed the environment.</span></span>

### <a name="domain-accounts"></a><span data-ttu-id="33ff1-313">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="33ff1-313">Domain accounts</span></span>

<span data-ttu-id="33ff1-314">次のテーブルに、環境を配置したときに作成されたドメイン アカウントの既定の名前を示します。</span><span class="sxs-lookup"><span data-stu-id="33ff1-314">The following table lists the default names of the domain accounts that were created when you deployed the environment.</span></span>

| <span data-ttu-id="33ff1-315">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="33ff1-315">Domain account</span></span>                  | <span data-ttu-id="33ff1-316">説明</span><span class="sxs-lookup"><span data-stu-id="33ff1-316">Description</span></span>                                                                                                           |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ff1-317"><DomainName>AOSServiceUser</span><span class="sxs-lookup"><span data-stu-id="33ff1-317"><DomainName>AOSServiceUser</span></span>      | <span data-ttu-id="33ff1-318">次のサービスを実行するために使用されたアカウント: Microsoft Dynamics AX Object Server</span><span class="sxs-lookup"><span data-stu-id="33ff1-318">The account used to run the following services: Microsoft Dynamics AX Object Server</span></span>                                   |
| <span data-ttu-id="33ff1-319"><DomainName>SQLServiceUser</span><span class="sxs-lookup"><span data-stu-id="33ff1-319"><DomainName>SQLServiceUser</span></span>      | <span data-ttu-id="33ff1-320">次のサービスを実行するために使用されるアカウント: SQL Server Analysis Services (MSSQLSERVER)。</span><span class="sxs-lookup"><span data-stu-id="33ff1-320">The account used to run the following services: SQL Server Analysis Services (MSSQLSERVER)</span></span>                            |
| <span data-ttu-id="33ff1-321"><DomainName>DynamicsInstallUser</span><span class="sxs-lookup"><span data-stu-id="33ff1-321"><DomainName>DynamicsInstallUser</span></span> | <span data-ttu-id="33ff1-322">Dynamics AX をインストールするために使用したアカウント。</span><span class="sxs-lookup"><span data-stu-id="33ff1-322">The account used to install Dynamics AX.</span></span>                                                                              |
| <span data-ttu-id="33ff1-323"><DomainName>RetailServiceUser</span><span class="sxs-lookup"><span data-stu-id="33ff1-323"><DomainName>RetailServiceUser</span></span>   | <span data-ttu-id="33ff1-324">次のサービスの実行に使用したアカウント: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client。</span><span class="sxs-lookup"><span data-stu-id="33ff1-324">The account used to run the following services: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client.</span></span> |
| <span data-ttu-id="33ff1-325"><DomainName>BCProxyUser</span><span class="sxs-lookup"><span data-stu-id="33ff1-325"><DomainName>BCProxyUser</span></span>         | <span data-ttu-id="33ff1-326">ビジネス コネクタ プロキシとして使用されるアカウント。</span><span class="sxs-lookup"><span data-stu-id="33ff1-326">The account used as the Business Connector proxy.</span></span>                                                                     |

> [!NOTE]
> <span data-ttu-id="33ff1-327">パスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) の **クラウド ホスト 環境** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-327">The passwords are displayed on the **Cloud-hosted environments** page in [Lifecycle Services](https://lifecycleservices.dynamics.com/en/).</span></span>

### <a name="local-administrator-accounts"></a><span data-ttu-id="33ff1-328">ローカル管理者アカウント</span><span class="sxs-lookup"><span data-stu-id="33ff1-328">Local administrator accounts</span></span>

<span data-ttu-id="33ff1-329">配置した各仮想マシンには、ローカル Administrator アカウントがあります。</span><span class="sxs-lookup"><span data-stu-id="33ff1-329">Each virtual machine that you deployed has a local administrator account.</span></span> <span data-ttu-id="33ff1-330">このアカウントは builtinaxlocaladmin です。</span><span class="sxs-lookup"><span data-stu-id="33ff1-330">This account is: builtinaxlocaladmin.</span></span> <span data-ttu-id="33ff1-331">ローカル管理者アカウントのパスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) の **クラウド ホスト 環境** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="33ff1-331">The passwords for the local administrator accounts are displayed on the **Cloud-hosted environments** page in [Lifecycle Services](https://lifecycleservices.dynamics.com/en/).</span></span>



