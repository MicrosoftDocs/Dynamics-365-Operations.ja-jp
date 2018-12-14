---
title: "継続的ビルドとテストの自動化をサポートするトポロジの配置"
description: "このトピックでは、継続的なビルドとテストの自動化をサポートする開発者トポロジを配置する方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 02/22/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 13171
ms.assetid: 
ms.search.region: Global
ms.author: shailesn
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cda5df9bec24bf8fc63ab3a5b2f3de9f84a03923
ms.openlocfilehash: 860cf388ce7bc1f3848bd40e6cb146ff71c7b051
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="deploy-topologies-that-support-continuous-build-and-test-automation"></a><span data-ttu-id="5002a-103">継続的ビルドとテストの自動化をサポートするトポロジの配置</span><span class="sxs-lookup"><span data-stu-id="5002a-103">Deploy topologies that support continuous build and test automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5002a-104">このトピックでは、継続的なビルドとテストの自動化をサポートする開発者トポロジを配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5002a-104">This topic describes how to deploy a developer topology that supports continuous build and test automation.</span></span>

<span data-ttu-id="5002a-105">前提条件: これには、クラウド VM 展開用の Azure DevOps アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="5002a-105">Prerequisite: This requires a Azure DevOps account for cloud VM deployment.</span></span>

## <a name="workflow"></a><span data-ttu-id="5002a-106">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="5002a-106">Workflow</span></span>
<span data-ttu-id="5002a-107">Lifecycle Services (LCS) で Azure DevOps サブスクリプションを設定した後、開発者トポロジの配置をトリガーして開発者およびビルド VM の設定をすることができます。</span><span class="sxs-lookup"><span data-stu-id="5002a-107">After you have configured a Azure DevOps subscription in Lifecycle Services (LCS), you can trigger Developer Topology Deployment to set up Developer and Build VMs.</span></span> <span data-ttu-id="5002a-108">この配置では、開発者用 VM は Azure DevOps プロジェクトに対して開発するためにワークスペース マッピングで構成されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-108">In this deployment, the Developer VM is configured with workspace mapping to develop against a Azure DevOps project.</span></span> <span data-ttu-id="5002a-109">ビルド VM は、モジュール Azure DevOps プロジェクトを構築し、検証用の外部エンドポイントを使用して自動テストを実行するために、ビルド エージェント/コントローラーを使用して自動構成されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-109">The Build VM is auto-configured with the build agent/controller to build modules  Azure DevOps project and to execute automated tests with external endpoint for validation.</span></span> <span data-ttu-id="5002a-110">カスタム テスト コードの記述またはビルド インフラストラクチャと統合する自動テスト コードを生成する方法については、[テストと検証](testing-validation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5002a-110">For more information on writing custom test code or generating automated test code to integrate with build infrastructure, see [Testing and validations](testing-validation.md).</span></span> <span data-ttu-id="5002a-111">一般的なワークフローまたは使用シナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="5002a-111">A typical workflow or usage scenario is shown below.</span></span> 

<span data-ttu-id="5002a-112">[![build12](./media/build12-1024x693.jpg)](./media/build12.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-112">[![build12](./media/build12-1024x693.jpg)](./media/build12.jpg)</span></span>

## <a name="set-up-azure-devops"></a><span data-ttu-id="5002a-113">Azure DevOps の設定</span><span class="sxs-lookup"><span data-stu-id="5002a-113">Set up Azure DevOps</span></span>
<span data-ttu-id="5002a-114">組織の必要な Azure DevOps 機能を比較します。<https://www.visualstudio.com/products/visual-studio-team-services-feature-matrix-vs></span><span class="sxs-lookup"><span data-stu-id="5002a-114">Compare Azure DevOps features required for your organization: <https://www.visualstudio.com/products/visual-studio-team-services-feature-matrix-vs></span></span>

-   <span data-ttu-id="5002a-115">**TFVC vs GIT**: 現在 TFVC がサポートされているのはソース管理リポジトリのみで、Git はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5002a-115">**TFVC vs GIT**: Currently TFVC is the only supported source control repository, Git is not supported.</span></span>
-   <span data-ttu-id="5002a-116">**現在のビルドの中断:** 既にビルド定義が作成されている既存の Azure DevOps プロジェクトにビルド エージェントを展開している場合、ビルドをキューに入れるための有効なトリガーがないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5002a-116">**Suspend current builds:** If you are deploying the build agent on an existing Azure DevOps project which already has build definition created, please ensure you do not have any active triggers to queue the build.</span></span> <span data-ttu-id="5002a-117">また、ビルド プールに対して、スケジュールされた/キューに格納されたビルドがないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5002a-117">Additionally, make sure there are no builds scheduled / queued against the build pool.</span></span> 

    <span data-ttu-id="5002a-118">[![BuildTriggers](./media/buildtriggers.jpg)](./media/buildtriggers.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-118">[![BuildTriggers](./media/buildtriggers.jpg)](./media/buildtriggers.jpg)</span></span>

-   <span data-ttu-id="5002a-119">**無料の Azure DevOps アカウントには、ビルド エージェントが 1 つだけ用意されています**。</span><span class="sxs-lookup"><span data-stu-id="5002a-119">**Free Azure DevOps accounts provide only one build pipeline**.</span></span> <span data-ttu-id="5002a-120">社内の Visual Studio Enterprise サブスクライバーにはそれぞれ、追加のパイプラインが付与されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-120">For each Visual Studio Enterprise subscriber in your organization you're granted an additional pipeline.</span></span> 


<span data-ttu-id="5002a-121">現在許可されているよりも多くのビルド パイプラインを使用するには、Azure DevOps アカウントを Azure 請求で設定します。[アカウントの請求を設定する](https://docs.microsoft.com/en-us/azure/devops/organizations/billing/set-up-billing-for-your-organization-vs?view=vsts)</span><span class="sxs-lookup"><span data-stu-id="5002a-121">To use more build pipelines than you're currently granted, set up your Azure DevOps account with Azure billing: [Set up billing for your account](https://docs.microsoft.com/en-us/azure/devops/organizations/billing/set-up-billing-for-your-organization-vs?view=vsts)</span></span> 

<span data-ttu-id="5002a-122">[![VSTS1](./media/vsts1-300x155.jpg)](./media/vsts1.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-122">[![VSTS1](./media/vsts1-300x155.jpg)](./media/vsts1.jpg)</span></span>

-   <span data-ttu-id="5002a-123">Azure サブスクリプションを使用してアカウントにリンクした後、Azure 管理ポータルの指示に従い、より多くの同時パイプラインを購入します [VSTS の同時パイプライン](https://docs.microsoft.com/en-us/azure/devops/pipelines/licensing/concurrent-jobs-vsts?branch=master&view=vsts)</span><span class="sxs-lookup"><span data-stu-id="5002a-123">After your account is linked with the Azure subscription, follow the instructions in the Azure management portal to purchase more concurrent pipelines - [Concurrent pipelines in VSTS](https://docs.microsoft.com/en-us/azure/devops/pipelines/licensing/concurrent-jobs-vsts?branch=master&view=vsts)</span></span> 


<span data-ttu-id="5002a-124">[![VSTS2](./media/vsts2-300x151.jpg)](./media/vsts2.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-124">[![VSTS2](./media/vsts2-300x151.jpg)](./media/vsts2.jpg)</span></span> 

> [!NOTE]
> <span data-ttu-id="5002a-125">支払済オプションで、「プライベート エージェント」を増やしてください。</span><span class="sxs-lookup"><span data-stu-id="5002a-125">Make sure you increase “Private Agents” under PAID option.</span></span> 

<span data-ttu-id="5002a-126">[![VSTS3](./media/vsts3-300x191.jpg)](./media/vsts3.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-126">[![VSTS3](./media/vsts3-300x191.jpg)](./media/vsts3.jpg)</span></span>

-   <span data-ttu-id="5002a-127">**ビルド エージェント プールのロールとアクセス許可:**<https://msdn.microsoft.com/library/vs/alm/build/agents/admin#agent-pools></span><span class="sxs-lookup"><span data-stu-id="5002a-127">**Build Agent Pool role and permissions:** <https://msdn.microsoft.com/library/vs/alm/build/agents/admin#agent-pools></span></span>

<span data-ttu-id="5002a-128">ビルド エージェントが追加されたら、ユーザー (LCS から VM を配置構築) を「エージェント プール管理者」ロールにします。</span><span class="sxs-lookup"><span data-stu-id="5002a-128">Once build agents are added, add user (who will be deploying build VM from LCS) to “Agent Pool Administrators” role.</span></span> 

<span data-ttu-id="5002a-129">[![VSTS4](./media/vsts4.jpg)](./media/vsts4.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-129">[![VSTS4](./media/vsts4.jpg)](./media/vsts4.jpg)</span></span>

-   <span data-ttu-id="5002a-130">**管理エージェント:** 複数のエージェントがコンフィギュレーションされていて、1 つを削除する場合は、エージェントを選択し、ステータス列の右側にある削除ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="5002a-130">**Manage agent:** If you have multiple agents configured and want to delete one, select the agent and use the delete button to the right of the status column.</span></span>

    <span data-ttu-id="5002a-131">[![build14](./media/build14.jpg)](./media/build14.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-131">[![build14](./media/build14.jpg)](./media/build14.jpg)</span></span>

-   <span data-ttu-id="5002a-132">**既定のプールの削除:** 何らかの理由でデフォルト プールを削除した場合は、「既定」という名前の新しいプールを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="5002a-132">**Deleting Default Pool:** If for some reason you have deleted the default pool, please do not create a new pool with the name "Default".</span></span> <span data-ttu-id="5002a-133">代わりに、別の名前で新しい管理グループを作成し、配置の際に LCS の「詳細設定」のカスタマイズから管理グループ名を渡します。</span><span class="sxs-lookup"><span data-stu-id="5002a-133">Instead create a new pool with the different name and pass the pool name from the "Advanced Settings" customization from LCS during deployment.</span></span>
-   <span data-ttu-id="5002a-134">**個人用アクセス トークン:** このトークンは、アップグレードおよび配置を含む Lifecycle Services (LCS) のバックグラウンド アクションで使用されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-134">**Personal access token:** This token is used for all Lifecycle Services (LCS) background actions, including upgrade and deployment.</span></span> <span data-ttu-id="5002a-135">ユーザーが LCS からアクションを起動すると、LCS はユーザーが Azure DevOps に追加されることを期待しています。</span><span class="sxs-lookup"><span data-stu-id="5002a-135">When a user initiates actions from LCS, LCS expects that users will be added to Azure DevOps.</span></span> <span data-ttu-id="5002a-136">ユーザーは、ユーザーの代わりに Azure DevOps への LCS アクセスを認可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5002a-136">The user must authorize LCS access to Azure DevOps on behalf of the user.</span></span> <span data-ttu-id="5002a-137">プロジェクトのユーザーが Azure DevOps で承認されるまで、アクション センターに以下のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-137">Until the projects users authorize with Azure DevOps, you will see the below message in action center:</span></span> 

<span data-ttu-id="5002a-138">[![LCS の VSTS 設定\_5 月 27 日](./media/vsts-setup-in-lcs_may27-300x216.jpg)](./media/vsts-setup-in-lcs_may27.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-138">[![VSTS setup in LCS\_May27](./media/vsts-setup-in-lcs_may27-300x216.jpg)](./media/vsts-setup-in-lcs_may27.jpg)</span></span>

## <a name="deploy-developer-topology-from-lcs"></a><span data-ttu-id="5002a-139">LCS から開発者トポロジを配置する</span><span class="sxs-lookup"><span data-stu-id="5002a-139">Deploy Developer topology from LCS</span></span>
<span data-ttu-id="5002a-140">LCS では、開発トポロジ環境を配置するオプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-140">LCS provides an option to deploy a Development topology environment.</span></span> <span data-ttu-id="5002a-141">このオプションでは、Azure DevOps プロジェクトに接続されたクラウド内に、開発者を配置して VM をビルドすることができます。</span><span class="sxs-lookup"><span data-stu-id="5002a-141">With this option, you can deploy developer and build VMs in the cloud that are connected to your Azure DevOps project.</span></span>

### <a name="azure-devops-credential-setup-and-linking-to-lcs-project"></a><span data-ttu-id="5002a-142">Azure DevOps 資格情報の設定と LCS プロジェクトへのリンク</span><span class="sxs-lookup"><span data-stu-id="5002a-142">Azure DevOps credential setup and linking to LCS project</span></span>

1. <span data-ttu-id="5002a-143">[https://lcs.dynamics.com/](https://lcs.dynamics.com/)で LCS ポータルにログインして、Azure DevOps および LCS プロジェクトに接続します。</span><span class="sxs-lookup"><span data-stu-id="5002a-143">Login to the LCS portal to connect to Azure DevOps and your LCS project at [https://lcs.dynamics.com/](https://lcs.dynamics.com/).</span></span>
2. <span data-ttu-id="5002a-144">作業しているプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="5002a-144">Select a project that you are working on.</span></span>
3. <span data-ttu-id="5002a-145">**プロジェクト設定**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5002a-145">Click the **Project Settings** tile.</span></span>
4. <span data-ttu-id="5002a-146">**Azure DevOps** を選択し、モジュール プロジェクトのソース コードが保管されている Azure DevOps URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="5002a-146">Select **Azure DevOps** and enter the Azure DevOps URL where the source code for your module project is located.</span></span>
5. <span data-ttu-id="5002a-147">Azure DevOps リンクを指定して、承認し、**既定のプロジェクトを選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5002a-147">Specify the Azure DevOps link, authorize, and then click **Choose default project**.</span></span>
   > [!NOTE]
   > <span data-ttu-id="5002a-148">現在のところ、VSTF をソース コントロールとしてサポートしていますが、Git をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="5002a-148">We currently support VSTF as source control and do not support Git.</span></span> 

<span data-ttu-id="5002a-149">[![VSTS](./media/vsts-1024x792.jpg)](./media/vsts.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-149">[![VSTS](./media/vsts-1024x792.jpg)](./media/vsts.jpg)</span></span>

### <a name="check-in-migrated-or-new-module-code-into-azure-devops"></a><span data-ttu-id="5002a-150">Azure DevOps に移行または新しいモジュールコードをチェックイン</span><span class="sxs-lookup"><span data-stu-id="5002a-150">Check-in migrated or new module code into Azure DevOps</span></span>

<span data-ttu-id="5002a-151">コードの移行プロセスまたは開発活動の一環として、モデル ソース ファイルと関連するテスト モデル ソース ファイルを Azure DevOps にチェックインすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5002a-151">As part of code Migration process or development activities, we expect you to check-in your model source files and the associated test model source files into Azure DevOps.</span></span> <span data-ttu-id="5002a-152">LCS 移行サービスを使用してコードを移行した場合、自動的に行われます。</span><span class="sxs-lookup"><span data-stu-id="5002a-152">If you have migrated your code using the LCS migration service, this is automatically done for you.</span></span> <span data-ttu-id="5002a-153">Azure DevOps にコードをチェックインせずに直接チェックインする場合は、Azure DevOps フォルダ構造の特定のガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5002a-153">If you have not checked in any code into Azure DevOps and work on direct check-in, you must follow certain guidelines for the Azure DevOps folder structure.</span></span> <span data-ttu-id="5002a-154">これは、適切なビルド定義の設定に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5002a-154">This will help with setting up correct build definition.</span></span> <span data-ttu-id="5002a-155">すべてのモジュールをルート フォルダー**メタデータ**に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5002a-155">All modules should be added to root folder **Metadata**.</span></span> <span data-ttu-id="5002a-156">各モジュールにはフォルダーが 2 つ必要です。</span><span class="sxs-lookup"><span data-stu-id="5002a-156">Under each module, there should be two folders.</span></span> <span data-ttu-id="5002a-157">1 つのフォルダーには、すべてのモデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5002a-157">One folder contains all models.</span></span> <span data-ttu-id="5002a-158">他のフォルダーには、そのモジュールの記述子 XML が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5002a-158">The other folder should contain descriptor XML for that module.</span></span> 

![VSTS フォルダー構造](media/build-trunk-main-metadata.png)

### <a name="deploy-developer-topology-developer-and-build-vm"></a><span data-ttu-id="5002a-160">開発者トポロジの配置 (開発者とビルド VM)</span><span class="sxs-lookup"><span data-stu-id="5002a-160">Deploy developer topology (Developer and Build VM)</span></span>

1. <span data-ttu-id="5002a-161">LCS ポータルで、Azure DevOps に接続されているプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="5002a-161">In the LCS portal, select the project that is connected to Azure DevOps.</span></span>
2. <span data-ttu-id="5002a-162">**環境**ウィンドウで、**+** をクリックして新しい環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="5002a-162">In the **Environments** pane, click **+** to deploy a new environment.</span></span>

   ![Azure の設定](media/azure-settings.png)

3. <span data-ttu-id="5002a-164">**環境のトポロジの選択**ウィンドウで、**Azure** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5002a-164">In the **Select environment topology** pane, select **Azure**.</span></span>

   ![環境のトポロジの選択](media/select-environment-topology.png)

4. <span data-ttu-id="5002a-166">DEV/TEST 環境の展開に進みます。</span><span class="sxs-lookup"><span data-stu-id="5002a-166">Proceed to deploy a DEV/TEST environment.</span></span>
   -   <span data-ttu-id="5002a-167">LCS プロジェクトのタイプによっては、以下に説明する配置ステップの一部が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="5002a-167">Depending on your LCS project type, some deployment steps described below may vary.</span></span>

5. <span data-ttu-id="5002a-168">**環境の配置**ウィンドウで、配置のための環境名を入力し、**開発者** VM のインスタンスの番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="5002a-168">On the **Deploy environment** pane, enter the environment name for the deployment, and select the number of instances for **Developer** VMs.</span></span>
   > [!NOTE]
   > <span data-ttu-id="5002a-169">1 つのビルド VM および 1 つの開発者向け VM のみを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="5002a-169">You can only deploy one Build VM and one Developer VM.</span></span> <span data-ttu-id="5002a-170">開発者 VM を導入しない場合、インスタンスの数をゼロに設定します。</span><span class="sxs-lookup"><span data-stu-id="5002a-170">If you don’t want to deploy a Developer VM, then set instances count to zero.</span></span> 

   <span data-ttu-id="5002a-171">複数の開発者 VM が必要な場合、開発者 VM ごとに新しい環境を展開します。</span><span class="sxs-lookup"><span data-stu-id="5002a-171">If you want multiple Developer VMs then deploy new environment per developer VM.</span></span>

   <span data-ttu-id="5002a-172">[![配置](./media/deploy-1024x669.jpg)](./media/deploy.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-172">[![Deploy](./media/deploy-1024x669.jpg)](./media/deploy.jpg)</span></span>

6. <span data-ttu-id="5002a-173">**詳細設定** をクリックし、**Azure DevOps** を選択します</span><span class="sxs-lookup"><span data-stu-id="5002a-173">Click **Advanced settings**, select **Azure DevOps**</span></span>
   1.  <span data-ttu-id="5002a-174">ビルド エージェント名: Azure DevOps ビルド エージェントのフレンドリ名</span><span class="sxs-lookup"><span data-stu-id="5002a-174">Build Agent Name: Friendly name for build agent on Azure DevOps</span></span>
   2.  <span data-ttu-id="5002a-175">ビルド エージェント プール: ビルド マシンの配置に使用するビルド エージェント プール名を指定します。</span><span class="sxs-lookup"><span data-stu-id="5002a-175">Build Agent Pool: specify build agent pool name which should be used for build machine deployment.</span></span> <span data-ttu-id="5002a-176">Azure DevOps に少なくとも 1 つのエージェント プールが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5002a-176">Make sure Azure DevOps contains at least one agent pool.</span></span> <span data-ttu-id="5002a-177">既定では、既定のプールがあります。</span><span class="sxs-lookup"><span data-stu-id="5002a-177">By default, there will be the default pool.</span></span> <span data-ttu-id="5002a-178">既定のプールを削除した場合は、ビルド配置は失敗します。</span><span class="sxs-lookup"><span data-stu-id="5002a-178">If you have deleted the default pool then build deployment will fail.</span></span>
   3.  <span data-ttu-id="5002a-179">分岐名: ビルド VM の既定のソース コード同期場所になる Azure DevOps ソース コード ブランチを指定します。</span><span class="sxs-lookup"><span data-stu-id="5002a-179">Branch Name: Specify your Azure DevOps source code branch which will be default source code sync location for the build VM.</span></span> <span data-ttu-id="5002a-180">既定の分岐は、「メイン」です。</span><span class="sxs-lookup"><span data-stu-id="5002a-180">Default branch is "Main".</span></span>

   ![設定](media/settings.jpg)

7. <span data-ttu-id="5002a-182">設定が確認されたら、**次へ**をクリックして展開を開始します。</span><span class="sxs-lookup"><span data-stu-id="5002a-182">After the settings are verified, click **Next** to start the deployment.</span></span> <span data-ttu-id="5002a-183">展開の進捗状況は **環境** の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-183">You can see progress of deployment under **Environments**.</span></span>
8. <span data-ttu-id="5002a-184">配置が完了したら、リモート デスクトップを使用して、開発者とビルド VMを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="5002a-184">After the deployment is complete, you can use Remote Desktop to view Developer and Build VM.</span></span>

## <a name="use-a-developer-vm-environment"></a><span data-ttu-id="5002a-185">開発者 VM 環境の使用</span><span class="sxs-lookup"><span data-stu-id="5002a-185">Use a Developer VM environment</span></span>
<span data-ttu-id="5002a-186">開発者 VM が配置されると、ソース管理 (Azure DevOps) からのコードの同期に使用されるワークスペースで開発者 VM が自動構成されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-186">When a Developer VM gets deployed, it’s auto-configured with a workspace that will be used to synchronize your code from source control (Azure DevOps).</span></span> <span data-ttu-id="5002a-187">この開発者 VM には Microsoft Dynamics 365 for Finance and Operations が配置されているため、テスト VM として使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="5002a-187">As this Developer VM has Microsoft Dynamics 365 for Finance and Operations deployed on it, it can also be used as a test VM.</span></span>

### <a name="configure-visual-studio-to-connect-to-azure-devops"></a><span data-ttu-id="5002a-188">Azure DevOps に接続するように Visual Studio をコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="5002a-188">Configure Visual Studio to connect to Azure DevOps</span></span>

<span data-ttu-id="5002a-189">開発者 VM で初めて Visual Studio を開くときは、自分の資格情報を使用して Azure DevOps に接続します。</span><span class="sxs-lookup"><span data-stu-id="5002a-189">When you open Visual Studio the first time on a Developer VM, connect to Azure DevOps using your credentials.</span></span>

1.  <span data-ttu-id="5002a-190">**チーム エクスプローラー**を開き、**チーム プロジェクトの選択**を開きます。</span><span class="sxs-lookup"><span data-stu-id="5002a-190">Open **Team explorer** and click **Select Team projects**.</span></span>
2.  <span data-ttu-id="5002a-191">Azure DevOps URL を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5002a-191">Enter the Azure DevOps URL and click **OK**.</span></span> <span data-ttu-id="5002a-192">Azure DevOps ユーザー名とパスワードを求められます。</span><span class="sxs-lookup"><span data-stu-id="5002a-192">You will be prompted for your Azure DevOps username and password.</span></span>
3.  <span data-ttu-id="5002a-193">Azure DevOps にログインした後、開発に使用する**既定のワークスペース**。</span><span class="sxs-lookup"><span data-stu-id="5002a-193">After you are logged into the Azure DevOps, your **Default workspace** that you will use for your development.</span></span>

    ![ワークスペースの管理](media/manage-workspaces.png)

## <a name="test-integration-with-the-build"></a><span data-ttu-id="5002a-195">ビルドとのテスト統合</span><span class="sxs-lookup"><span data-stu-id="5002a-195">Test integration with the build</span></span>
<span data-ttu-id="5002a-196">テストと検証のためのビルド プロセスの一部としてテストを統合するには、2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="5002a-196">There are two ways to integrate test as part of build process for testing and validation:</span></span>

-   <span data-ttu-id="5002a-197">単位とコンポーネントのレベル テストに基づく SysTest フレームワーク。</span><span class="sxs-lookup"><span data-stu-id="5002a-197">SysTest framework based unit and component level tests.</span></span>
-   <span data-ttu-id="5002a-198">自動化されたテストの実行の XML を記録するタスク レコーダーから、コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="5002a-198">Generate code from Task Recorder recording XML for automated test execution.</span></span>

<span data-ttu-id="5002a-199">これら 2 つの方法の詳細については、[テストと検証](testing-validation.md) を参照してください。テストおよび検証の戦略についてはこの記事を確認してください。</span><span class="sxs-lookup"><span data-stu-id="5002a-199">The details of these two approaches are mentioned in the [Testing and validation. ](testing-validation.md)Review this article for testing and validation strategy.</span></span>

## <a name="use-the-build-vm-environment"></a><span data-ttu-id="5002a-200">ビルド VM 環境の使用</span><span class="sxs-lookup"><span data-stu-id="5002a-200">Use the Build VM environment</span></span>
<span data-ttu-id="5002a-201">LCS を通じて開発者トポロジにビルド VM が配置されると、それは事前に構成され、ビルドを開始する準備ができます。</span><span class="sxs-lookup"><span data-stu-id="5002a-201">When a Build VM is deployed in Developer topology through LCS, it is pre-configured and ready to start a build.</span></span> <span data-ttu-id="5002a-202">Visual Studio IDE または Azure DevOps インターフェイスから、いつでも既定の構成を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="5002a-202">You can change the default configuration at any time from the Visual Studio IDE or the Azure DevOps interface.</span></span> <span data-ttu-id="5002a-203">ビルド VM では、簡単なビルドのセットアップのために、モジュール ソース コードがビルド コンピューターに同期されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-203">On a Build VM, the module source code is synchronized to the build machine for easy build setup.</span></span> <span data-ttu-id="5002a-204">ビルド マシンは、ビルド エージェント、ビルド コントローラー、ビルド プロセス テンプレート、ビルド定義のデフォルト設定で自動構成されています。</span><span class="sxs-lookup"><span data-stu-id="5002a-204">The build machine is also auto-configured with default settings for build agent, build controller, build process template, and build definition.</span></span> <span data-ttu-id="5002a-205">ビルドに成功したら、ビルド定義と統合されているテストが実行されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-205">Tests that are integrated with build definition are executed after the build is successful.</span></span>

### <a name="review-a-pre-configured-customizable-build-environment"></a><span data-ttu-id="5002a-206">定義済みのカスタマイズ可能なビルド環境を確認</span><span class="sxs-lookup"><span data-stu-id="5002a-206">Review a pre-configured customizable build environment</span></span>

<span data-ttu-id="5002a-207">ビルド VM には、TFS 2015 の一部としてリリースされた vNext ビルド エージェントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5002a-207">The build VM contains the vNext build agent which was released as part of TFS 2015.</span></span> <span data-ttu-id="5002a-208">ビルド VM を配置するときは、既定では Azure DevOps プロジェクトと接続して同期するようにビルド エージェントが構成されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-208">When you deploy the Build VM, the build agent is configured by default to connect and sync with the Azure DevOps project.</span></span> <span data-ttu-id="5002a-209">ビルド VM 構成の一部として、以下に示すようにデフォルトのビルド定義も作成および構成されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-209">As a part of the Build VM configuration, the default build definition is also created and configured, as shown below.</span></span> 

<span data-ttu-id="5002a-210">[![Build1](./media/build1-1024x488.jpg)](./media/build1.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-210">[![Build1](./media/build1-1024x488.jpg)](./media/build1.jpg)</span></span> 

<span data-ttu-id="5002a-211">既定のビルド定義には、以下で説明するように、特定の操作を実行する複数のタスクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5002a-211">Default build definition contains multiple tasks to perform specific operation, as described below.</span></span>

1.  <span data-ttu-id="5002a-212">ビルドに渡す事前定義済の変数パラメータをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="5002a-212">Configure the predefined variables parameters that will be passed to the build.</span></span> <span data-ttu-id="5002a-213">ビルド実行ごとにクリーンなデータベースを設定するには、**DatabaseBackupToRestore**変数のデータベース バックアップ ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="5002a-213">To set up a clean database for every build execution, provide the name of the database backup file for the **DatabaseBackupToRestore** variable.</span></span> <span data-ttu-id="5002a-214">パッケージ フォルダーは、すべてのビルド時にクリーン パッケージ フォルダーのコピーで復元されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-214">The packages folder is restored at every build with a copy of a clean package folder.</span></span>

    <span data-ttu-id="5002a-215">[![build2](./media/build2-1024x678.jpg)](./media/build2.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-215">[![build2](./media/build2-1024x678.jpg)](./media/build2.jpg)</span></span>

2.  <span data-ttu-id="5002a-216">以下のように、「トランク/メイン」ブランチにあるすべてのモジュールを検出して構築するためにソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="5002a-216">Build the solution to discover and build all modules under "Trunk/Main" branch as shown below.</span></span>

    <span data-ttu-id="5002a-217">[![Build3](./media/build3-1024x456.jpg)](./media/build3.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-217">[![Build3](./media/build3-1024x456.jpg)](./media/build3.jpg)</span></span>

3.  <span data-ttu-id="5002a-218">「レポートの展開」タスクを使用して、レポートを生成し、ビルド VM に展開します。</span><span class="sxs-lookup"><span data-stu-id="5002a-218">Use "Deploy Report" task to generate reports and deploy on build VM.</span></span>
4.  <span data-ttu-id="5002a-219">「データベース同期」タスクを使用して、データベースをビルド VM 上のローカル SQL に同期させます。</span><span class="sxs-lookup"><span data-stu-id="5002a-219">Use "Database Sync" task to synchronize the database to local SQL on build VM.</span></span>
5.  <span data-ttu-id="5002a-220">ビルドが成功した後、サンドボックス/ステージング環境を更新するために使用できる配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="5002a-220">After the build is successful, create a deployable package that can be used to update sandbox/ staging environment.</span></span>

    <span data-ttu-id="5002a-221">[![Build4](./media/build4-1024x462.jpg)](./media/build4.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-221">[![Build4](./media/build4-1024x462.jpg)](./media/build4.jpg)</span></span>

6.  <span data-ttu-id="5002a-222">「ビルド コンポーネントのコピーと発行」は、配置可能パッケージを Azure DevOps コンポーネントの場所にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="5002a-222">"Copy and publish build artifacts" uploads the deployable package to Azure DevOps artifacts location.</span></span>

    <span data-ttu-id="5002a-223">[![build5](./media/build5-1024x439.jpg)](./media/build5.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-223">[![build5](./media/build5-1024x439.jpg)](./media/build5.jpg)</span></span>

7.  <span data-ttu-id="5002a-224">テストの実行については、3 つの既定のタスク「テスト設定」、「テストの実行」、および「テストの終了」があります。</span><span class="sxs-lookup"><span data-stu-id="5002a-224">For test execution, there are three default tasks "Test Setup", "Execute Test" and "Test End".</span></span>

    <span data-ttu-id="5002a-225">[![build7](./media/build7-1024x457.jpg)](./media/build7.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-225">[![build7](./media/build7-1024x457.jpg)](./media/build7.jpg)</span></span>

8.  <span data-ttu-id="5002a-226">既定のビルドでは毎日午後 5 時に開始される予定です。</span><span class="sxs-lookup"><span data-stu-id="5002a-226">The default build is scheduled to trigger start every day at 5 P.M.</span></span> <span data-ttu-id="5002a-227">チームの必要性に従って、各チェックインでトリガーを「継続」に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="5002a-227">You can change trigger as per your team's need to "Continuous" for each check-in.</span></span>

    <span data-ttu-id="5002a-228">[![build8](./media/build8-1024x491.jpg)](./media/build8.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-228">[![build8](./media/build8-1024x491.jpg)](./media/build8.jpg)</span></span>

<span data-ttu-id="5002a-229">既定の構成に変更を加えて、そのビルド VM がビルドをトリガーできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="5002a-229">You can make changes to the default configuration, and the build VM will be ready to trigger a build.</span></span>

## <a name="start-a-build-and-verify-the-build-and-test-execution-results"></a><span data-ttu-id="5002a-230">ビルドを開始し、ビルドとテストの実行結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="5002a-230">Start a build and verify the build and test execution results</span></span>
<span data-ttu-id="5002a-231">既定のビルド構成を確認した後は、Visual Studio IDE または Azure DevOps Web インターフェイスからビルドを手動でトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="5002a-231">After you review the default build configuration, you can manually trigger a build from Visual Studio IDE or Azure DevOps web interface.</span></span>

1.  <span data-ttu-id="5002a-232">ブラウザーを開き、Azure DevOps URL に接続します。</span><span class="sxs-lookup"><span data-stu-id="5002a-232">Open your browser and connect to the Azure DevOps URL.</span></span>
2.  <span data-ttu-id="5002a-233">資格情報を使用してをログインします。</span><span class="sxs-lookup"><span data-stu-id="5002a-233">Login using your credentials.</span></span>
3.  <span data-ttu-id="5002a-234">ホーム ページの**最近のプロジェクトとソリューション**で、プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="5002a-234">On the home page, under **Recent projects and solutions**, select a project.</span></span>
4.  <span data-ttu-id="5002a-235">上部リンク オプションから、**ビルド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5002a-235">From top links options, select **BUILD**.</span></span>
5.  <span data-ttu-id="5002a-236">左側のパネルで、既定のビルド定義インスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="5002a-236">On the left panel, select the default build definition instance.</span></span>
6.  <span data-ttu-id="5002a-237">右クリックし、**キュー ビルド** を選択して Azure DevOps ソース管理に既にチェックインしているモジュールおよびテスト モジュールのビルドをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="5002a-237">Right-click and select **Queue Build** to trigger a build for your module and test module that is already checked into the Azure DevOps source control.</span></span>

<span data-ttu-id="5002a-238">[![image045](./media/image045.png)](./media/image045.png)</span><span class="sxs-lookup"><span data-stu-id="5002a-238">[![image045](./media/image045.png)](./media/image045.png)</span></span> 

<span data-ttu-id="5002a-239">次の例に示すように、ビルドの成功または失敗が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5002a-239">Success or failure for the build will display, as shown by the following examples.</span></span> <span data-ttu-id="5002a-240">すべてのビルドを表示します。</span><span class="sxs-lookup"><span data-stu-id="5002a-240">View all builds.</span></span> 

<span data-ttu-id="5002a-241">[![build9](./media/build9-1024x443.jpg)](./media/build9.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-241">[![build9](./media/build9-1024x443.jpg)](./media/build9.jpg)</span></span> 

<span data-ttu-id="5002a-242">特定の完了したビルドとビューの成功/失敗の詳細を選択します。</span><span class="sxs-lookup"><span data-stu-id="5002a-242">Select specific completed build and view success/ failure details.</span></span> 

<span data-ttu-id="5002a-243">[![build10](./media/build10-1024x446.jpg)](./media/build10.jpg) テストリンクをクリックして、テスト実行の失敗を視覚化します。</span><span class="sxs-lookup"><span data-stu-id="5002a-243">[![build10](./media/build10-1024x446.jpg)](./media/build10.jpg) Click on Test link to visualize test execution failure.</span></span> 

<span data-ttu-id="5002a-244">[![build11](./media/build11-1024x455.jpg)](./media/build11.jpg)</span><span class="sxs-lookup"><span data-stu-id="5002a-244">[![build11](./media/build11-1024x455.jpg)](./media/build11.jpg)</span></span>

