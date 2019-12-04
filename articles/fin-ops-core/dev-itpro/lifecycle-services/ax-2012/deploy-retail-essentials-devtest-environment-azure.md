---
title: Azure での Retail Essentials 開発/テスト環境の配置
description: このトピックでは、Microsoft Azure に Retail essentials 開発環境またはテスト環境を配置する方法について説明します。 環境を配置するには、Microsoft Dynamics Lifecycle Services でクラウド ホスト環境ツールを使用します。
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
ms.custom: 13261
ms.assetid: 00e58780-7373-4c53-b3af-1e9d3d4eebff
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 741001c5801604bf72ac18f0fec4be47d6c08f05
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812065"
---
# <a name="deploy-retail-essentials-devtest-environments-on-azure"></a><span data-ttu-id="92873-104">Azure での Retail Essentials 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="92873-104">Deploy Retail essentials dev/test environments on Azure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="92873-105">このトピックでは、Microsoft Azure に Retail essentials 開発環境またはテスト環境を配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="92873-105">This topic explains how to deploy a Retail essentials dev/test environment on Microsoft Azure.</span></span> <span data-ttu-id="92873-106">環境を配置するには、Microsoft Dynamics Lifecycle Services でクラウド ホスト環境ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="92873-106">To deploy the environment, you’ll use the cloud-hosted environments tool in Microsoft Dynamics Lifecycle Services.</span></span>

<a name="prerequisites"></a><span data-ttu-id="92873-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="92873-107">Prerequisites</span></span>
-------------

<span data-ttu-id="92873-108">このトピックの手順を実行する前に、次の条件が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="92873-108">Before you complete the procedures in this topic, make sure that the following prerequisites are in place.</span></span>

| <span data-ttu-id="92873-109">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="92873-109">Category</span></span>       | <span data-ttu-id="92873-110">前提条件</span><span class="sxs-lookup"><span data-stu-id="92873-110">Prerequisite</span></span>                                                                                                                                                    |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92873-111">必要なタスク</span><span class="sxs-lookup"><span data-stu-id="92873-111">Required tasks</span></span> | [<span data-ttu-id="92873-112">Azure で AX 2012 R3 の配置を計画する</span><span class="sxs-lookup"><span data-stu-id="92873-112">Plan AX 2012 R3 deployments on Azure</span></span>](plan-2012-r3-deployment-azure.md) |

## <a name="1-log-on-to-lifecycle-services"></a><span data-ttu-id="92873-113">1. ライフサイクル サービスにログオンする</span><span class="sxs-lookup"><span data-stu-id="92873-113">1. Log on to Lifecycle Services</span></span>
<span data-ttu-id="92873-114">Microsoft Dynamics Lifecycle Services (LCS) は、顧客およびパートナーが Dynamics AX のプロジェクトの管理に使用できるクラウドベースの共同ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="92873-114">Microsoft Dynamics Lifecycle Services (LCS) provides a cloud-based collaborative workspace that customers and partners can use to manage Dynamics AX projects.</span></span> <span data-ttu-id="92873-115">Azure に Dynamics AX を配置するには、この Web サイトを使用します。</span><span class="sxs-lookup"><span data-stu-id="92873-115">You’ll use this website to deploy Dynamics AX on Azure.</span></span> <span data-ttu-id="92873-116">Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="92873-116">Lifecycle Services is available to customers and partners as part of their support plans.</span></span> <span data-ttu-id="92873-117">CustomerSource または PartnerSource の資格情報でアクセスすることができます。詳細については、[Lifecycle Services にログオン](https://lcs.dynamics.com/en/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-117">You can access it with your CustomerSource or PartnerSource credentials, for details see [Log on to Lifecycle Services](https://lcs.dynamics.com/en/).</span></span>

## <a name="2-create-a-project"></a><span data-ttu-id="92873-118">2. プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="92873-118">2. Create a project</span></span>
<span data-ttu-id="92873-119">LCS にログインした後、既存のプロジェクトを開くか、または新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="92873-119">After you log in to LCS, open an existing project, or create a new project.</span></span> <span data-ttu-id="92873-120">プロジェクトは、LCS でのエクスペリエンスの主な開催者です。</span><span class="sxs-lookup"><span data-stu-id="92873-120">Projects are the key organizer of your experience in LCS.</span></span> <span data-ttu-id="92873-121">プロジェクトに関連する手法は、既定でプロジェクトに含まれるフェーズとタスクを決定します。</span><span class="sxs-lookup"><span data-stu-id="92873-121">The methodology associated with a project determines which phases and tasks are included in the project by default.</span></span>

## <a name="3-connect-the-project-to-your-azure-subscription"></a><span data-ttu-id="92873-122">3. Azure サブスクリプションにプロジェクトを接続する</span><span class="sxs-lookup"><span data-stu-id="92873-122">3. Connect the project to your Azure subscription</span></span>
<span data-ttu-id="92873-123">Azure サブスクリプションに LCS プロジェクトを接続します。</span><span class="sxs-lookup"><span data-stu-id="92873-123">Connect the LCS project to your Azure subscription.</span></span> <span data-ttu-id="92873-124">これにより、LCS は Dynamics AX 環境をサブスクリプションに展開できます。</span><span class="sxs-lookup"><span data-stu-id="92873-124">This will enable LCS to deploy a Dynamics AX environment to the subscription.</span></span> <span data-ttu-id="92873-125">Azure サブスクリプションにプロジェクトを接続するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="92873-125">To connect the project to your Azure subscription, complete the following procedure.</span></span>

1. <span data-ttu-id="92873-126">LCS プロジェクトで**環境**セクションに移動して、**Microsoft Azure 設定**をクリックしてから、**Azure コネクタ領域**で**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-126">In your LCS project, go to the **Environments** section, click **Microsoft Azure settings**, and then click **Add** in the **Azure Connectors** area.</span></span> 
   >[!Note]
   > <span data-ttu-id="92873-127">**Microsoft Azure 設定**オプションは、**クラウド-ホスト環境タイル**をクリックしたときにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="92873-127">The **Microsoft Azure settings** option is also available when you click the **Cloud-hosted environments** tile.</span></span>
2. <span data-ttu-id="92873-128">Azure への接続を識別する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="92873-128">Enter a name to identify the connection to Azure.</span></span>
3. <span data-ttu-id="92873-129">Azure サブスクリプション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="92873-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="92873-130">サブスクリプション ID を検索する必要がある場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="92873-130">If you need to find your subscription ID, complete the following steps:</span></span>
   1.  <span data-ttu-id="92873-131">ブラウザの別のインスタンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="92873-131">Open another instance of your browser.</span></span>
   2.  <span data-ttu-id="92873-132">[Azure ポータル](https://ms.portal.azure.com/)にログオンします。</span><span class="sxs-lookup"><span data-stu-id="92873-132">Log on to the [Azure portal](https://ms.portal.azure.com/).</span></span>
   3.  <span data-ttu-id="92873-133">左のナビゲーション ウィンドウで、**サブスクリプション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-133">In the navigation pane on the left, click **Subscriptions**.</span></span> 

       > [!Note]
       > <span data-ttu-id="92873-134">下部の **その他のサービス** をクリックしてから **サブスクリプション** をクリックすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="92873-134">You may need to click **More services** at the bottom, and then click **Subscriptions**.</span></span>

   4.  <span data-ttu-id="92873-135">サブスクリプション ID をコピーして、LCS の **Azure サブスクリプション ID** フィールドに貼り付けます (現在別のブラウザー インスタンスに表示されています)。</span><span class="sxs-lookup"><span data-stu-id="92873-135">Copy your subscription ID, and then paste it into the **Azure subscription ID** field in LCS (which is currently displayed in another browser instance).</span></span>

4. <span data-ttu-id="92873-136">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-136">Click **Next**.</span></span>
5. <span data-ttu-id="92873-137">**ダウンロード**をクリックして管理証明書をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="92873-137">Click **Download** to download a management certificate.</span></span> <span data-ttu-id="92873-138">この管理証明書により、LCS はお客様の代わりに Azure と通信できます。</span><span class="sxs-lookup"><span data-stu-id="92873-138">This management certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="92873-139">既定では、管理証明書はコンピューターの**ダウンロード** フォルダーに保存され、**LifecycleServicesDeployment.cer** という名前が付きます。</span><span class="sxs-lookup"><span data-stu-id="92873-139">By default, the management certificate is saved to the **Downloads** folder on your computer and is named **LifecycleServicesDeployment.cer.**</span></span>
6. <span data-ttu-id="92873-140">管理証明書を Azure にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="92873-140">Upload the management certificate to Azure.</span></span> <span data-ttu-id="92873-141">これを行うには、[[Azure 管理 API 管理証明書をアップロード](https://docs.microsoft.com/azure/azure-api-management-certs)] の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-141">To do so, see the instructions in [Upload an Azure Management API Management Certificate](https://docs.microsoft.com/azure/azure-api-management-certs).</span></span>

7. <span data-ttu-id="92873-142">LCS で **Microsoft Azure 設定**パネルを表示するブラウザーに戻ります。</span><span class="sxs-lookup"><span data-stu-id="92873-142">Go back to the browser that displays the **Microsoft Azure setup** panel in LCS.</span></span> <span data-ttu-id="92873-143">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-143">Click **Next**.</span></span>
8. <span data-ttu-id="92873-144">地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="92873-144">Select a region.</span></span> <span data-ttu-id="92873-145">AX 2012 R3 環境は、この領域のデータ センターに配置されます。</span><span class="sxs-lookup"><span data-stu-id="92873-145">The AX 2012 R3 environment will be deployed to a datacenter in this region.</span></span>
9. <span data-ttu-id="92873-146">**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-146">Click **Connect**.</span></span> <span data-ttu-id="92873-147">これで、プロジェクトが指定された Azure サブスクリプションに接続できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="92873-147">The project is now connected to the Azure subscription that you specified.</span></span> 

>[!Note]
> <span data-ttu-id="92873-148">証明書が期限切れになった場合は、新しいものを取得できます。</span><span class="sxs-lookup"><span data-stu-id="92873-148">If the certificate expires, you can obtain a new one.</span></span> <span data-ttu-id="92873-149">そのためには次の作業を行います。</span><span class="sxs-lookup"><span data-stu-id="92873-149">To do so:</span></span>
> 1. <span data-ttu-id="92873-150">プロジェクトの設定の **Azure コネクタ** 領域で接続を選択し、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-150">Select the connection in the **Azure connectors** area of your project settings, and click **Edit**.</span></span>
> 2. <span data-ttu-id="92873-151">**Microsoft Azure 設定**パネルが画面の横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="92873-151">The **Microsoft Azure setup** panel is displayed on the side of the screen.</span></span> <span data-ttu-id="92873-152">**ダウンロード**をクリックして新しい証明書をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="92873-152">Click **Download** to download a new certificate.</span></span>
> 3. <span data-ttu-id="92873-153">上の手順の手順 6 ～ 9 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="92873-153">Repeat steps 6-9 of the above procedure.</span></span>

## <a name="4-deploy-a-retail-essentials-devtest-environment-on-azure"></a><span data-ttu-id="92873-154">4. Azure での Retail Essentials 開発/テスト環境の配置</span><span class="sxs-lookup"><span data-stu-id="92873-154">4. Deploy a Retail essentials dev/test environment on Azure</span></span>
<span data-ttu-id="92873-155">Azure に Retail Essentials 開発/テスト環境を配置するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="92873-155">Complete the following procedure to deploy a Retail essentials dev/test environment on Azure.</span></span>

1. <span data-ttu-id="92873-156">**クラウド ホスト環境**ページで、**追加** (**+**) アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-156">On the **Cloud-hosted environments** page, click the **Add** (**+**) icon.</span></span>
2. <span data-ttu-id="92873-157">**環境のトポロジの選択**パネルで、**開発/テスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="92873-157">In the **Select environment topology** panel, select **Dev/Test**.</span></span>
3. <span data-ttu-id="92873-158">**Retail Essentials 開発/テスト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-158">Click **Retail essentials dev/test**.</span></span>
4. <span data-ttu-id="92873-159">**環境名**フィールドに、配置される環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="92873-159">In the **Environment name** field, enter a name for the environment that will be deployed.</span></span>
5. <span data-ttu-id="92873-160">**詳細設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-160">Click **Advanced settings**.</span></span>
6. <span data-ttu-id="92873-161">ドメイン設定をカスタマイズするには、**ドメイン設定をカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-161">To customize domain settings, click **Customize domain settings**.</span></span> <span data-ttu-id="92873-162">情報を入力するには、次の表を使用してください。</span><span class="sxs-lookup"><span data-stu-id="92873-162">Use the following table to enter information.</span></span>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th><span data-ttu-id="92873-163">以下を行う場合</span><span class="sxs-lookup"><span data-stu-id="92873-163">If you want to</span></span></th>
   <th><span data-ttu-id="92873-164">操作</span><span class="sxs-lookup"><span data-stu-id="92873-164">Do this</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td><span data-ttu-id="92873-165">Azure で環境用に新しいドメインを作成する</span><span class="sxs-lookup"><span data-stu-id="92873-165">Create a new domain in Azure for the environment</span></span></td>
   <td><ol>
   <li><span data-ttu-id="92873-166"><strong>新規ドメイン</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-166">Click <strong>New domain</strong>.</span></span></li>
   <li><span data-ttu-id="92873-167">ドメイン名を入力します。</span><span class="sxs-lookup"><span data-stu-id="92873-167">Enter a name for the domain.</span></span> <span data-ttu-id="92873-168">既定では、ドメインは <em>contoso.com</em> と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="92873-168">By default, the domain is named <em>contoso.com</em>.</span></span></li>
   </ol></td>
   </tr>
   <tr class="even">
   <td><span data-ttu-id="92873-169">Azure の既存のドメインへの環境の追加</span><span class="sxs-lookup"><span data-stu-id="92873-169">Add the environment to an existing domain in Azure</span></span></td>
   <td><ol>
   <li><span data-ttu-id="92873-170"><strong>既存のドメイン</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-170">Click <strong>Existing domain</strong>.</span></span></li>
   <li><span data-ttu-id="92873-171">ドメイン名を入力します。</span><span class="sxs-lookup"><span data-stu-id="92873-171">Enter the name of the domain.</span></span> <span data-ttu-id="92873-172">たとえば、<em>contoso.com</em>。</span><span class="sxs-lookup"><span data-stu-id="92873-172">For example, <em>contoso.com</em>.</span></span></li>
   </ol></td>
   </tr>
   </tbody>
   </table>

7. <span data-ttu-id="92873-173">ドメインで作成されるサービス アカウントをカスタマイズするには、**サービス アカウントをカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-173">To customize the service accounts that will be created in the domain, click **Customize service accounts**.</span></span> <span data-ttu-id="92873-174">展開の **詳細設定** オプションを通じてサービス アカウントやサービス アカウントのパスワードを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="92873-174">Service accounts and/or service account passwords can be specified through the **Advanced Settings** option for a deployment.</span></span> <span data-ttu-id="92873-175">どちらもが指定されていない場合は、既定の勘定が使用され、ランダムなパスワードが選択されています。</span><span class="sxs-lookup"><span data-stu-id="92873-175">If neither is provided, default accounts are used and random passwords are selected.</span></span> <span data-ttu-id="92873-176">次の機能は、企業のアカウントの命名規則とパスワードの規則を管理する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="92873-176">Use these features when you want to maintain account naming and password rules for your corporation.</span></span> <span data-ttu-id="92873-177">アカウントとパスワードのルール:</span><span class="sxs-lookup"><span data-stu-id="92873-177">Account and password rules:</span></span>
   - <span data-ttu-id="92873-178">有効なサービス名は、特殊文字を含まない 20 文字未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="92873-178">A valid service name must be less than 20 characters with no special characters.</span></span>
   - <span data-ttu-id="92873-179">有効なパスワードは 8 文字以上で、大文字、小文字、数字、および次の文字のうち少なくとも 1 つが含まれます: \['@', '!', '=', '\*'\] 次のような一般的なパスワードは使用できません: pass@word1</span><span class="sxs-lookup"><span data-stu-id="92873-179">A valid password must be more than 8 characters and contain uppercase letters, lowercase letters, numbers, and at least one of the following characters: \['@', '!', '=', '\*'\] You can’t use common passwords, such as: pass@word1</span></span>

8. <span data-ttu-id="92873-180">使用を希望する AX 2012 R3 のバージョンを選択するには、**サポートされているバージョン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-180">To select the version of AX 2012 R3 that you want use, click **Supported version**.</span></span> <span data-ttu-id="92873-181">既定では、この環境の AX 2012 R3 CU8 バージョンが配置されます。</span><span class="sxs-lookup"><span data-stu-id="92873-181">By default, the AX 2012 R3 CU8 version of this environment will be deployed.</span></span> <span data-ttu-id="92873-182">CU8 バージョンを使用しない場合は、**Dynamics ERP 2012 R3 RTM** をリストから選択します。</span><span class="sxs-lookup"><span data-stu-id="92873-182">If you don’t want to use the CU8 version, select **Dynamics ERP 2012 R3 RTM** from the list.</span></span>
9. <span data-ttu-id="92873-183">仮想マシン名をカスタマイズするには、**仮想マシン名をカスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-183">To customize virtual machine names, click **Customize virtual machine names**.</span></span> <span data-ttu-id="92873-184">一般的な IT 名前付けガイドラインをサポートするために、仮想マシンに名前を付ける機能がほとんどの配置トポロジの**詳細設定**に用意されています。</span><span class="sxs-lookup"><span data-stu-id="92873-184">In order to support common IT naming guidelines, the ability to name virtual machines is provided through the **Advanced settings** option on most deployment topologies.</span></span> <span data-ttu-id="92873-185">名前を定義することに加えて、各仮想マシン タイプに開始インデックスを選択できます。</span><span class="sxs-lookup"><span data-stu-id="92873-185">In addition to defining the name, a starting index can be selected for each virtual machine type.</span></span> <span data-ttu-id="92873-186">インデックスは、配置される仮想マシン タイプのインスタンスごとに増加します。</span><span class="sxs-lookup"><span data-stu-id="92873-186">The index is incremented for each instance of the virtual machine type that is deployed.</span></span> <span data-ttu-id="92873-187">仮想マシン名は 13 文字またはそれ以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92873-187">Virtual machine names must be 13 characters or less.</span></span> <span data-ttu-id="92873-188">インデックスはマシン名とハイフン (-) で区切られ、その後に最大 2 桁のインデックスが続きます。</span><span class="sxs-lookup"><span data-stu-id="92873-188">The index is separated from the machine name by a hyphen (-), followed by the index that supports a maximum of 2 digits.</span></span> <span data-ttu-id="92873-189">例: ACustomVMName-99。</span><span class="sxs-lookup"><span data-stu-id="92873-189">Example: ACustomVMName-99.</span></span> <span data-ttu-id="92873-190">最初の展開後に、仮想マシンのインスタンスが環境に追加されるとき、配置サービスは、中断した場所で、仮想マシンの名前の増分を開始します。</span><span class="sxs-lookup"><span data-stu-id="92873-190">When virtual machine instances are added to an environment after the initial deployment, the deployment service will start incrementing the virtual machine name where it left off.</span></span> <span data-ttu-id="92873-191">たとえば、2 で始まるインデックスを持つ 4 つの AOS 仮想マシンを展開する場合、最後の AOS インスタンス名は AOS-6 になります。</span><span class="sxs-lookup"><span data-stu-id="92873-191">For example, if you deployed four AOS virtual machines with a starting index of 2, then the last AOS instance name will be AOS-6.</span></span> <span data-ttu-id="92873-192">もう 2 つ AOS インスタンスを追加する場合は、AOS-7 と AOS 8 になります。</span><span class="sxs-lookup"><span data-stu-id="92873-192">If you add two more AOS instances, they will be AOS-7 and AOS-8.</span></span> <span data-ttu-id="92873-193">展開内の仮想マシン タイプの 1 つがカスタマイズされている場合は、すべての仮想マシン名をカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92873-193">If one of the virtual machine types in your deployment is customized, then all of the virtual machine names must be customized.</span></span> <span data-ttu-id="92873-194">これは、仮想マシン名が誤って紛失してしまったため、長期的な展開が発生しないようにするためです。</span><span class="sxs-lookup"><span data-stu-id="92873-194">This is done to ensure that a long deployment does not occur because a virtual machine name was accidentally missed.</span></span>
10. <span data-ttu-id="92873-195">仮想ネットワークの設定をカスタマイズするには、<strong>仮想ネットワークをカスタマイズする</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-195">To customize virtual network settings, click <strong>Customize virtual network</strong>.</span></span> <span data-ttu-id="92873-196">情報を入力するには、次の表を使用してください。</span><span class="sxs-lookup"><span data-stu-id="92873-196">Use the following table to enter information.</span></span>
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="92873-197">以下を行う場合</span><span class="sxs-lookup"><span data-stu-id="92873-197">If you want to</span></span></th>
    <th><span data-ttu-id="92873-198">操作</span><span class="sxs-lookup"><span data-stu-id="92873-198">Do this</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="92873-199">Azure で環境用に新しい仮想ネットワークを作成する</span><span class="sxs-lookup"><span data-stu-id="92873-199">Create a new virtual network in Azure for the environment</span></span></td>
    <td><ol>
    <li><span data-ttu-id="92873-200"><strong>新しい仮想ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-200">Click <strong>New virtual network</strong>.</span></span></li>
    <li><span data-ttu-id="92873-201">仮想ネットワーク名を入力します。</span><span class="sxs-lookup"><span data-stu-id="92873-201">Enter a name for the virtual network.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="92873-202">Azure の既存の仮想ネットワークへの環境の追加</span><span class="sxs-lookup"><span data-stu-id="92873-202">Add the environment to an existing virtual network in Azure</span></span></td>
    <td><ol>
    <li><span data-ttu-id="92873-203"><strong>既存の仮想ネットワーク</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-203">Click <strong>Existing virtual network</strong>.</span></span></li>
    <li><span data-ttu-id="92873-204">使用する既存の仮想ネットワークの名前を選択してください。</span><span class="sxs-lookup"><span data-stu-id="92873-204">Select the name of the existing virtual network that you want to use.</span></span></li>
    <li><span data-ttu-id="92873-205"><strong>アドレス空間</strong> フィールドには、適切な値が自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="92873-205">The <strong>Address space</strong> field will automatically display the appropriate value.</span></span> <span data-ttu-id="92873-206">提供された値を選択します。</span><span class="sxs-lookup"><span data-stu-id="92873-206">Select the provided value.</span></span></li>
    <li><span data-ttu-id="92873-207"><strong>アプリケーション サブネット名</strong> フィールドには、使用可能なオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="92873-207">The <strong>Application subnet name</strong> field will display available options.</span></span> <span data-ttu-id="92873-208">Lifecycle Servicesによって以前に展開した広告に配置する場合は、選択した <strong>APPNET</strong> 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="92873-208">If you are deploying to an AD that was previously deployed through Lifecycle Services, select the <strong>APPNET</strong> value.</span></span></li>
    <li><span data-ttu-id="92873-209">Active Directory サブネットを入力する必要があり、ターゲットとする AD の Azure 管理ポータルにある Active Directory サブネット IP/範囲と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="92873-209">The Active Directory subnet must be entered and match the Active Directory subnet IP/Range found in the Azure management portal for the AD you want to target.</span></span>
    <ol>
    <li><span data-ttu-id="92873-210"><a href="https://ms.portal.azure.com/">Azure ポータル</a>にログオンします。</span><span class="sxs-lookup"><span data-stu-id="92873-210">Log on to the <a href="https://ms.portal.azure.com/">Azure portal</a>.</span></span></li>
    <li><span data-ttu-id="92873-211">左のナビゲーション ウィンドウで、 <strong>仮想ネットワーク</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-211">In the navigation pane on the left, click <strong>Virtual networks</strong>.</span></span></li>
    <li><span data-ttu-id="92873-212">使用する仮想ネットワークの名前をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-212">Click the name of the virtual network that you’re going to use.</span></span></li>
    <li><span data-ttu-id="92873-213"><strong>構成</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-213">Click <strong>Configure</strong>.</span></span> <span data-ttu-id="92873-214">仮想ネットワークに関する詳細は、ページに記載されています。</span><span class="sxs-lookup"><span data-stu-id="92873-214">Details about the virtual network are listed on the page.</span></span></li>
    </ol></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

11. <span data-ttu-id="92873-215">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-215">Click **Done**.</span></span> <span data-ttu-id="92873-216">**環境** **の展開** パネルが再表示されます。</span><span class="sxs-lookup"><span data-stu-id="92873-216">The **Deploy** **environment** panel is redisplayed.</span></span>
12. <span data-ttu-id="92873-217">配置される仮想マシンの数とサイズが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="92873-217">The number and size of each virtual machine that will be deployed is listed.</span></span> <span data-ttu-id="92873-218">必要に応じて、仮想マシンの数とサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="92873-218">Change the number and size of the virtual machines, as needed.</span></span>
    -   <span data-ttu-id="92873-219">この環境で各仮想マシンにインストールされているソフトウェアの詳細については、 [Azure 上での AX 2012 R3の 配置計画](plan-2012-r3-deployment-azure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-219">For information about the software installed on each virtual machine in this environment, see [Plan AX 2012 R3 deployments on Azure](plan-2012-r3-deployment-azure.md).</span></span>
    -   <span data-ttu-id="92873-220">仮想マシンに関するサイズおよび価格決定の詳細については、[仮想マシンの価格決定の詳細](http://azure.microsoft.com/pricing/details/virtual-machines/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-220">For sizing and pricing details about virtual machines, see [Virtual machines pricing details](http://azure.microsoft.com/pricing/details/virtual-machines/).</span></span>

13. <span data-ttu-id="92873-221">ライセンスの条項を確認するには、**ソフトウェア ライセンス条項**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-221">Click **Software License Terms** to review the licensing terms and conditions.</span></span> <span data-ttu-id="92873-222">次に、チェック ボックスを選択して、条件に同意することを示します。</span><span class="sxs-lookup"><span data-stu-id="92873-222">Then select the check box to indicate that you agree to the terms.</span></span>
14. <span data-ttu-id="92873-223">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-223">Click **Next**.</span></span>
15. <span data-ttu-id="92873-224">**展開**をクリックして、環境を展開する準備が整ったことを確認します。</span><span class="sxs-lookup"><span data-stu-id="92873-224">Click **Deploy** to confirm that you’re ready to deploy the environment.</span></span> <span data-ttu-id="92873-225">配置には数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="92873-225">The deployment may take a few hours to complete.</span></span> <span data-ttu-id="92873-226">配置が完了すると、**クラウド ホスト環境** ページの **配置ステータス** 列に **配置済み** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="92873-226">When the deployment is done, the **Deployment Status** column on the **Cloud-hosted environments** page will display **Deployed**.</span></span> <span data-ttu-id="92873-227">(これを表示するにはブラウザーを更新する必要があります。) 配置が失敗すると、すぐエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="92873-227">(You may need to refresh your browser to see this.) If the deployment fails, you may see an error message right away.</span></span> <span data-ttu-id="92873-228">配置プロセスでエラーが後に発生する場合に、エラーの詳細がページの右側の詳細ペインに表示されます。</span><span class="sxs-lookup"><span data-stu-id="92873-228">If the error occurs later in the deployment process, error details will be displayed in the details pane on the right-side of the page.</span></span>

## <a name="5-prepare-the-environment-for-use"></a><span data-ttu-id="92873-229">5. 使用する環境を準備</span><span class="sxs-lookup"><span data-stu-id="92873-229">5. Prepare the environment for use</span></span>
<span data-ttu-id="92873-230">Retail Essentials 環境が Azure に配置されたので、これを設定して使用するためにコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92873-230">Now that the Retail essentials environment has been deployed on Azure, you must set it up and configure it for use.</span></span> <span data-ttu-id="92873-231">詳細については、以降のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-231">See the following sections for more information.</span></span>

### <a name="log-on-to-the-retails-essentials-virtual-machine"></a><span data-ttu-id="92873-232">Retail Essentials 仮想マシンにログオンします。</span><span class="sxs-lookup"><span data-stu-id="92873-232">Log on to the Retails essentials virtual machine</span></span>

<span data-ttu-id="92873-233">ESSEN-&lt;GUID&gt; 仮想マシンに &lt;DomainName&gt;DynamicsInstallUser アカウントを使用してログオンします。</span><span class="sxs-lookup"><span data-stu-id="92873-233">Log on to the ESSEN-&lt;GUID&gt; virtual machine using the &lt;DomainName&gt;DynamicsInstallUser account.</span></span> <span data-ttu-id="92873-234">手順については、「仮想マシンにどのようにログオンしますか?」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-234">For instructions, see the “How do I log on to a virtual machine?”</span></span> <span data-ttu-id="92873-235">トピック [Azure で AX 2012 R3 配置を管理する](manage-2012-r3-deployment-azure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-235">section of the [Manage AX 2012 R3 deployments on Azure](manage-2012-r3-deployment-azure.md) topic.</span></span>

### <a name="compile-dynamics-ax-2012-r3"></a><span data-ttu-id="92873-236">Dynamics AX 2012 R3 のコンパイル</span><span class="sxs-lookup"><span data-stu-id="92873-236">Compile Dynamics AX 2012 R3</span></span>

<span data-ttu-id="92873-237">Ax Build.exe. を使用した Dynamics AX 2012 R3 のコンパイル</span><span class="sxs-lookup"><span data-stu-id="92873-237">Compile Dynamics AX 2012 R3 by using AxBuild.exe.</span></span> <span data-ttu-id="92873-238">手順については、[X++ から P コードへの AOS の並列コンパイルに対する AxBuild.exe](https://technet.microsoft.com/library/dn528954.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-238">For instructions, see [AxBuild.exe for Parallel Compile on AOS of X++ to p-code](https://technet.microsoft.com/library/dn528954.aspx).</span></span>

### <a name="initialize-dynamics-ax-2012-r3"></a><span data-ttu-id="92873-239">Dynamics AX 2012 R3 の初期化</span><span class="sxs-lookup"><span data-stu-id="92873-239">Initialize Dynamics AX 2012 R3</span></span>

<span data-ttu-id="92873-240">Dynamics AX 2012 R3 クライアントを開いて、初期化チェックリストを完了します。</span><span class="sxs-lookup"><span data-stu-id="92873-240">Open the Dynamics AX 2012 R3 client and complete the initialization checklists.</span></span> <span data-ttu-id="92873-241">手順については、[初期化チェックリスト](https://technet.microsoft.com/library/aa497061.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-241">For instructions, see [Initialization checklists](https://technet.microsoft.com/library/aa497061.aspx).</span></span>

### <a name="install-sample-data"></a><span data-ttu-id="92873-242">サンプル データのインストール</span><span class="sxs-lookup"><span data-stu-id="92873-242">Install sample data</span></span>

<span data-ttu-id="92873-243">サンプル データを環境にインストールする場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="92873-243">If you want sample data installed in your environment, complete the following steps.</span></span>

1.  <span data-ttu-id="92873-244">次の場所に移動します: F:TestTransferTool</span><span class="sxs-lookup"><span data-stu-id="92873-244">Go to the following location:F:TestTransferTool</span></span>
2.  <span data-ttu-id="92873-245">テスト データ ツールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="92873-245">Install the Test Data Tool.</span></span> <span data-ttu-id="92873-246">手順については、 [テスト データ転送ツール (ベータ版) をインストールする](install-test-data-transfer-tool-beta.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-246">For instructions, see [Install the Test Data Transfer Tool (beta)](install-test-data-transfer-tool-beta.md).</span></span>
3.  <span data-ttu-id="92873-247">コマンド プロンプトを開いて、次の場所に移動します: C:\Program Files (x86) \Microsoft Dynamics AX 2012 R3 Test Data Transfer Tool (Beta)</span><span class="sxs-lookup"><span data-stu-id="92873-247">Open a command prompt and navigate to the following location: C:\Program Files (x86)\Microsoft Dynamics AX 2012 R3 Test Data Transfer Tool (Beta)</span></span>
4.  <span data-ttu-id="92873-248">次のコマンドを実行します: dp.exe import F:DemoData MicrosoftDynamicsAx</span><span class="sxs-lookup"><span data-stu-id="92873-248">Run the following command: dp.exe import F:DemoData MicrosoftDynamicsAx</span></span>

> [!NOTE]
> <span data-ttu-id="92873-249">サンプル データには、Dynamics AX の試用版のライセンス キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="92873-249">The sample data includes trial license keys for Dynamics AX.</span></span> <span data-ttu-id="92873-250">サンプル データをインストールしないように選択する場合は、開発またはテスト用の試用版ライセンス キーを [CustomerSource](https://mbs.microsoft.com/downloads/customer/AX/AXDemoTools/MicrosoftDynamicsAX2012R2v4DemoLicense.zip) または [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898#FileId=57028) からダウンロードすることができます</span><span class="sxs-lookup"><span data-stu-id="92873-250">If you choose not to install the sample data, you can download trial license keys—for development or testing purposes—from [CustomerSource](https://mbs.microsoft.com/downloads/customer/AX/AXDemoTools/MicrosoftDynamicsAX2012R2v4DemoLicense.zip) or [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898#FileId=57028).</span></span>

### <a name="set-up-retail-essentials"></a><span data-ttu-id="92873-251">Retail Essentials の設定</span><span class="sxs-lookup"><span data-stu-id="92873-251">Set up Retail essentials</span></span>

<span data-ttu-id="92873-252">Dynamics AX クライアントを開いて、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="92873-252">Open the Dynamics AX client and complete the following steps.</span></span>

1.  <span data-ttu-id="92873-253">**Retail essentials** エリア ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="92873-253">Go to the **Retail essentials** area page.</span></span>
2.  <span data-ttu-id="92873-254">**チャネル &gt; 設定** **&gt; 小売パラメーター**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-254">Click **Channels &gt; Setup** **&gt; Retail parameters**.</span></span>
3.  <span data-ttu-id="92873-255">**小売パラメーター** フォームで、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="92873-255">In the **Retail parameters** form, complete the following steps:</span></span>
    1.  <span data-ttu-id="92873-256">フォーム上部の**初期化**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-256">Click the **Initialize** button at the top of the form.</span></span>
    2.  <span data-ttu-id="92873-257">**はい**をクリックして、基本構成データを初期化することを確認します。</span><span class="sxs-lookup"><span data-stu-id="92873-257">Click **Yes** to confirm that you want to initialize the base configuration data.</span></span> <span data-ttu-id="92873-258">初期化プロセスが完了すると、情報ログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="92873-258">When the initialization process is complete, the Infolog is displayed.</span></span>
    3.  <span data-ttu-id="92873-259">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="92873-259">Close the form.</span></span>

4.  <span data-ttu-id="92873-260">**データ同期 &gt; 設定 &gt; 小売用スケジューラのパラメーター**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-260">Click **Data synchronization &gt; Setup &gt; Retail scheduler parameters.**</span></span>
5.  <span data-ttu-id="92873-261">**小売用スケジューラ パラメーター** フォームで、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="92873-261">In the **Retail scheduler parameters** form, complete the following steps:</span></span>
    1.  <span data-ttu-id="92873-262">**サーバー名**フィールドに、仮想マシンの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="92873-262">In the **Server name** field, enter the name of the virtual machine.</span></span>
    2.  <span data-ttu-id="92873-263">フォーム上部の**メタデータの同期**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-263">Click the **Sync metadata** button at the top of the form.</span></span>
    3.  <span data-ttu-id="92873-264">**はい**をクリックしてメタデータを同期することを確認します。</span><span class="sxs-lookup"><span data-stu-id="92873-264">Click **Yes** to confirm that you want to sync the metadata.</span></span> <span data-ttu-id="92873-265">このプロセスが完了すると、情報ログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="92873-265">When the process is complete, the Infolog is displayed.</span></span>
    4.  <span data-ttu-id="92873-266">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="92873-266">Close the form.</span></span>

6.  <span data-ttu-id="92873-267">**データ同期 &gt; 設定 &gt; チャネル統合 &gt; Real-time Service プロファイル**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-267">Click **Data synchronization &gt; Setup &gt; Channel integration &gt; Real-time service profiles.**</span></span>
7.  <span data-ttu-id="92873-268">**Commerce Data Exchange: Real-time Service** プロファイル フォームで、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="92873-268">In the **Commerce Data Exchange: Real-time Service Profile** form, complete the following steps:</span></span>
    1.  <span data-ttu-id="92873-269">**サーバー名**フィールドに、仮想マシンの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="92873-269">In the **Server name** field, enter the name of the virtual machine.</span></span>
    2.  <span data-ttu-id="92873-270">**共通名**フィールドに、証明書の共通名を入力します。</span><span class="sxs-lookup"><span data-stu-id="92873-270">In the **Common name** field, enter the common name of the certificate.</span></span>
    3.  <span data-ttu-id="92873-271">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="92873-271">Close the form.</span></span>

8.  <span data-ttu-id="92873-272">**データ同期 &gt; 設定 &gt; チャネル統合 &gt; 作業フォルダー**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-272">Click **Data synchronization &gt; Setup &gt; Channel integration &gt; Working folders.**</span></span>
9.  <span data-ttu-id="92873-273">**作業フォルダー** フォームで、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="92873-273">In the **Working folders** form, complete the following steps.</span></span>
    1.  <span data-ttu-id="92873-274">**ダウンロード パス** フィールドの場所に注意してください。</span><span class="sxs-lookup"><span data-stu-id="92873-274">Note the location in the **Download path** field.</span></span> <span data-ttu-id="92873-275">通常は C:\DemoFiles\Retail\CDXDownload です。</span><span class="sxs-lookup"><span data-stu-id="92873-275">It is typically C:\DemoFiles\Retail\CDXDownload.</span></span> <span data-ttu-id="92873-276">C ドライブにこれらのフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="92873-276">Create these folders on the C drive.</span></span>
    2.  <span data-ttu-id="92873-277">**アップロード パス** フィールドの場所に注意してください。</span><span class="sxs-lookup"><span data-stu-id="92873-277">Note the location in the **Upload path** field.</span></span> <span data-ttu-id="92873-278">通常は C:\DemoFiles\Retail\CDXUpload です。</span><span class="sxs-lookup"><span data-stu-id="92873-278">It is typically C:\DemoFiles\Retail\CDXUpload.</span></span> <span data-ttu-id="92873-279">C ドライブにこれらのフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="92873-279">Create these folders on the C drive.</span></span>
    3.  <span data-ttu-id="92873-280">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="92873-280">Close the form.</span></span>

10. <span data-ttu-id="92873-281">**データ同期 &gt; 設定 &gt; チャネル統合 &gt; チャネル データベース**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-281">Click **Data synchronization &gt; Setup &gt; Channel integration &gt; Channel database.**</span></span>
11. <span data-ttu-id="92873-282">**チャネル データベース** フォームで、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="92873-282">In the **Channel database** form, complete the following steps:</span></span>
    1.  <span data-ttu-id="92873-283">**HoustonStore** レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="92873-283">Select the **HoustonStore** record.</span></span>
    2.  <span data-ttu-id="92873-284">フォームの右側にあるウィンドウで、**Retail サーバー** セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="92873-284">In the pane on the right side of the form, go to the **Retail Server** section.</span></span> <span data-ttu-id="92873-285">(表示するためにウィンドウの一番下までスクロールしなければならない場合があります。)</span><span class="sxs-lookup"><span data-stu-id="92873-285">(You may have to scroll to the bottom of the pane to see it.)</span></span>
    3.  <span data-ttu-id="92873-286">**サーバー名**フィールドに、仮想マシンの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="92873-286">In the **Server name** field, enter the name of the virtual machine.</span></span>
    4.  <span data-ttu-id="92873-287">フォーム上部の**完全データ同期**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-287">Click the **Full data sync** button at the top of the form.</span></span> <span data-ttu-id="92873-288">次に、リストから 9999 配布スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="92873-288">Then, select the 9999 distribution schedule from the list.</span></span> <span data-ttu-id="92873-289">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92873-289">Click **OK**.</span></span>
    5.  <span data-ttu-id="92873-290">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="92873-290">Close the form.</span></span>

## <a name="6-enable-users-to-access-dynamics-ax-2012-r3-on-azure"></a><span data-ttu-id="92873-291">6. Azure で Dynamics AX 2012 R3 へのユーザーのアクセスを可能にする</span><span class="sxs-lookup"><span data-stu-id="92873-291">6. Enable users to access Dynamics AX 2012 R3 on Azure</span></span>
<span data-ttu-id="92873-292">次のセクションでは、企業ユーザーが Dynamics AX 2012 R3 にアクセスできるように、Azure 仮想ネットワークとドメインを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="92873-292">The following sections provide information about how to configure the Azure virtual network and domain so that your corporate users can access Dynamics AX 2012 R3.</span></span>

### <a name="create-a-site-to-site-vpn-connection"></a><span data-ttu-id="92873-293">サイト間 VPN 接続を作成する</span><span class="sxs-lookup"><span data-stu-id="92873-293">Create a site-to-site VPN connection</span></span>

<span data-ttu-id="92873-294">企業ユーザーが Azure 仮想ネットワーク内の仮想マシンのリソースにアクセスできるようにするには、Azure 仮想ネットワークとオンプレミス社内ネットワークの間にサイト間 VPN 接続を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92873-294">To enable corporate users to access resources on the virtual machines in the Azure virtual network, you’ll need to create a site-to-site VPN connection between the Azure virtual network and your on-premises, corporate network.</span></span> <span data-ttu-id="92873-295">これを行う方法の詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-295">For information about how to do this, see:</span></span>

-   [<span data-ttu-id="92873-296">仮想ネットワークの概要</span><span class="sxs-lookup"><span data-stu-id="92873-296">Virtual network overview</span></span>](https://msdn.microsoft.com/library/windowsazure/jj156007.aspx)
-   [<span data-ttu-id="92873-297">仮想ネットワークのコンフィギュレーション タスク</span><span class="sxs-lookup"><span data-stu-id="92873-297">Virtual network configuration tasks</span></span>](https://msdn.microsoft.com/library/jj156206.aspx)
-   [<span data-ttu-id="92873-298">Windows Server 2012 ルーティングおよびリモート アクセスサービス (RRAS) を使用した Azure 仮想ネットワークのサイト間 VPN</span><span class="sxs-lookup"><span data-stu-id="92873-298">Site-to-site VPN in Azure virtual network using Windows Server 2012 Routing and Remote Access Service (RRAS)</span></span>](https://msdn.microsoft.com/library/dn636917.aspx)
-   [<span data-ttu-id="92873-299">管理ポータルに仮想ネットワーク ゲートウェイを構成する</span><span class="sxs-lookup"><span data-stu-id="92873-299">Configure a virtual network gateway in the management portal</span></span>](https://msdn.microsoft.com/library/azure/jj156210.aspx)

### <a name="create-a-domain-trust"></a><span data-ttu-id="92873-300">ドメイン信頼の作成</span><span class="sxs-lookup"><span data-stu-id="92873-300">Create a domain trust</span></span>

<span data-ttu-id="92873-301">企業ユーザーが Azure ドメイン内の仮想マシンのリソースにアクセスできるようにするには、ドメイン間で Active Directory のトラストを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92873-301">To enable corporate users to access resources on the virtual machines in your Azure domain, you must create an Active Directory trust between the domains.</span></span> <span data-ttu-id="92873-302">信託の作成方法の詳細については、「[フォレスト信託の作成](https://technet.microsoft.com/library/cc754626.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-302">For information about how to create a trust, see [Create a Forest Trust](https://technet.microsoft.com/library/cc754626.aspx).</span></span> <span data-ttu-id="92873-303">このプロセスは、2 つのオンプレミス ドメイン間で信頼関係を作成する場合と同じプロセスです。</span><span class="sxs-lookup"><span data-stu-id="92873-303">This process is the same process you would use to create a trust between two on-premises domains.</span></span>

### <a name="give-users-access"></a><span data-ttu-id="92873-304">ユーザーのアクセス許可を付与します</span><span class="sxs-lookup"><span data-stu-id="92873-304">Give users access</span></span>

<span data-ttu-id="92873-305">ユーザが Dynamics AX にアクセスできるようにするには、以下のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="92873-305">To enable your users to access Dynamics AX, complete the following tasks:</span></span>

-   <span data-ttu-id="92873-306">CLI- &lt;GUID&gt; 仮想マシンのリモート デスクトップ ユーザー グループに各ユーザーのドメイン アカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="92873-306">Add each user’s domain account to the Remote Desktop Users group on the CLI-&lt;GUID&gt; virtual machine.</span></span>
-   <span data-ttu-id="92873-307">ユーザーに Dynamics AX へのアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="92873-307">Give users access to Dynamics AX.</span></span> <span data-ttu-id="92873-308">手順については、[Microsoft Dynamics AX で新しいユーザーを作成する](https://technet.microsoft.com/library/aa548139.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92873-308">For instructions, see [Create new users in Microsoft Dynamics AX](https://technet.microsoft.com/library/aa548139.aspx).</span></span>

> [!NOTE]
> <span data-ttu-id="92873-309">VPN 接続とドメイン信頼を作成しない場合でも、ユーザーに Dynamics AX へのアクセス権を付与することができます。</span><span class="sxs-lookup"><span data-stu-id="92873-309">If you don’t want to create a VPN connection and a domain trust, you can still give users access to Dynamics AX.</span></span> <span data-ttu-id="92873-310">これを行うには、ドメイン コントローラとして機能する仮想マシンにログオンし、各ユーザーのドメイン アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92873-310">To do so, you’ll need to log on to the virtual machine that serves as the domain controller, and create domain accounts for each user.</span></span> <span data-ttu-id="92873-311">その後、上記の 2 つのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92873-311">Then, you’ll need to complete the two tasks mentioned above.</span></span>

## <a name="7-learn-more-about-the-service-accounts-for-this-environment"></a><span data-ttu-id="92873-312">7. この環境のサービス アカウントに関する詳細</span><span class="sxs-lookup"><span data-stu-id="92873-312">7. Learn more about the service accounts for this environment</span></span>
<span data-ttu-id="92873-313">次のセクションでは、環境を配置したときに作成されたサービス アカウントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="92873-313">The following sections provide information about the service accounts that were created when you deployed the environment.</span></span>

### <a name="domain-accounts"></a><span data-ttu-id="92873-314">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="92873-314">Domain accounts</span></span>

<span data-ttu-id="92873-315">次のテーブルに、環境を配置したときに作成されたドメイン アカウントの既定の名前を示します。</span><span class="sxs-lookup"><span data-stu-id="92873-315">The following table lists the default names of the domain accounts that were created when you deployed the environment.</span></span>

| <span data-ttu-id="92873-316">ドメイン アカウント</span><span class="sxs-lookup"><span data-stu-id="92873-316">Domain account</span></span>                  | <span data-ttu-id="92873-317">説明</span><span class="sxs-lookup"><span data-stu-id="92873-317">Description</span></span>                                                                                                           |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92873-318"><DomainName>AOSServiceUser</span><span class="sxs-lookup"><span data-stu-id="92873-318"><DomainName>AOSServiceUser</span></span>      | <span data-ttu-id="92873-319">次のサービスを実行するために使用されたアカウント: Microsoft Dynamics AX Object Server</span><span class="sxs-lookup"><span data-stu-id="92873-319">The account used to run the following services: Microsoft Dynamics AX Object Server</span></span>                                   |
| <span data-ttu-id="92873-320"><DomainName>SQLServiceUser</span><span class="sxs-lookup"><span data-stu-id="92873-320"><DomainName>SQLServiceUser</span></span>      | <span data-ttu-id="92873-321">次のサービスを実行するために使用されるアカウント: SQL Server Analysis Services (MSSQLSERVER)。</span><span class="sxs-lookup"><span data-stu-id="92873-321">The account used to run the following services: SQL Server Analysis Services (MSSQLSERVER)</span></span>                            |
| <span data-ttu-id="92873-322"><DomainName>DynamicsInstallUser</span><span class="sxs-lookup"><span data-stu-id="92873-322"><DomainName>DynamicsInstallUser</span></span> | <span data-ttu-id="92873-323">Dynamics AX をインストールするために使用したアカウント。</span><span class="sxs-lookup"><span data-stu-id="92873-323">The account used to install Dynamics AX.</span></span>                                                                              |
| <span data-ttu-id="92873-324"><DomainName>RetailServiceUser</span><span class="sxs-lookup"><span data-stu-id="92873-324"><DomainName>RetailServiceUser</span></span>   | <span data-ttu-id="92873-325">次のサービスの実行に使用したアカウント: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client。</span><span class="sxs-lookup"><span data-stu-id="92873-325">The account used to run the following services: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client.</span></span> |
| <span data-ttu-id="92873-326"><DomainName>BCProxyUser</span><span class="sxs-lookup"><span data-stu-id="92873-326"><DomainName>BCProxyUser</span></span>         | <span data-ttu-id="92873-327">ビジネス コネクタ プロキシとして使用されるアカウント。</span><span class="sxs-lookup"><span data-stu-id="92873-327">The account used as the Business Connector proxy.</span></span>                                                                     |

> [!NOTE]
> <span data-ttu-id="92873-328">パスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) の **クラウド ホスト 環境** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="92873-328">The passwords are displayed on the **Cloud-hosted environments** page in [Lifecycle Services](https://lifecycleservices.dynamics.com/en/).</span></span>

### <a name="local-administrator-accounts"></a><span data-ttu-id="92873-329">ローカル管理者アカウント</span><span class="sxs-lookup"><span data-stu-id="92873-329">Local administrator accounts</span></span>

<span data-ttu-id="92873-330">配置した各仮想マシンには、ローカル Administrator アカウントがあります。</span><span class="sxs-lookup"><span data-stu-id="92873-330">Each virtual machine that you deployed has a local administrator account.</span></span> <span data-ttu-id="92873-331">このアカウントは builtinaxlocaladmin です。</span><span class="sxs-lookup"><span data-stu-id="92873-331">This account is: builtinaxlocaladmin.</span></span> <span data-ttu-id="92873-332">ローカル管理者アカウントのパスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) の **クラウド ホスト 環境** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="92873-332">The passwords for the local administrator accounts are displayed on the **Cloud-hosted environments** page in [Lifecycle Services](https://lifecycleservices.dynamics.com/en/).</span></span>



