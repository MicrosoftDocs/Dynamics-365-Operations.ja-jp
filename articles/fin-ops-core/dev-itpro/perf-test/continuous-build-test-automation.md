---
title: 継続的なビルドおよびテストの自動化環境の配置と使用
description: このトピックでは、継続的なビルドとテストの自動化をサポートする開発者トポロジを配置する方法について説明します。
author: RobinARH
ms.date: 01/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 13171
ms.assetid: ''
ms.search.region: Global
ms.author: shailesn
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83d827a8506eab97f6accc6fe0a52b42b42ebae9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752934"
---
# <a name="deploy-and-use-a-continuous-build-and-test-automation-environment"></a><span data-ttu-id="76648-103">継続的なビルドおよびテストの自動化環境の配置と使用</span><span class="sxs-lookup"><span data-stu-id="76648-103">Deploy and use a continuous build and test automation environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76648-104">このトピックでは継続的なビルドとテストの自動化をサポートする環境を配置して使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="76648-104">This topic describes how to deploy and use an environment that supports continuous build and test automation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="76648-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="76648-105">Prerequisites</span></span>

<span data-ttu-id="76648-106">仮想マシン (VM) のクラウド配置には Microsoft Azure DevOps サブスクリプションが必要です。</span><span class="sxs-lookup"><span data-stu-id="76648-106">Cloud deployment of virtual machines (VMs) requires a Microsoft Azure DevOps subscription.</span></span>

## <a name="workflow"></a><span data-ttu-id="76648-107">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="76648-107">Workflow</span></span>

<span data-ttu-id="76648-108">Microsoft Dynamics Lifecycle Services (LCS) で Azure DevOps サブスクリプションを構成した後、LCS を使用して開発者 VM やビルド / テスト VM を配置できます。</span><span class="sxs-lookup"><span data-stu-id="76648-108">After you configure an Azure DevOps subscription in Microsoft Dynamics Lifecycle Services (LCS), you can use LCS to deploy developer VMs or build/test VMs.</span></span> <span data-ttu-id="76648-109">LCS は開発 VM を構成し、それは Azure DevOps プロジェクトにマップされます。</span><span class="sxs-lookup"><span data-stu-id="76648-109">LCS configures a developer VM that can be mapped to an Azure DevOps project.</span></span> <span data-ttu-id="76648-110">LCS は、ビルド VM も構成します。ビルド VM は、自動的に Azure DevOps プロジェクトにマップされ、Azure DevOps プロジェクトのモジュールを構成するビルド エージェント / コントローラーを持ち、妥当性確認のための外部エンドポイントを持つ自動化テストを実行します。</span><span class="sxs-lookup"><span data-stu-id="76648-110">LCS also configures a build VM that is automatically mapped to an Azure DevOps project and has a build agent/controller that builds modules from the Azure DevOps project and runs automated tests that have an external endpoint for validation.</span></span> <span data-ttu-id="76648-111">次の図は通常のワークフローを示します。</span><span class="sxs-lookup"><span data-stu-id="76648-111">The following illustration shows a typical workflow.</span></span>

![LCS、Azure DevOps、および VM の関係](./media/deploy-build-test.png)

<span data-ttu-id="76648-113">このワークフローには、Azure の開発者 VM とビルド / テスト VM の LCS 配置が含まれています。</span><span class="sxs-lookup"><span data-stu-id="76648-113">This workflow includes an LCS deployment of a developer VM and a build/test VM in Azure.</span></span>

+ <span data-ttu-id="76648-114">LCS は Azure で開発およびビルド / テスト環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="76648-114">LCS creates developer and the build/test environments in Azure.</span></span> <span data-ttu-id="76648-115">ビルド / テスト環境を作成するためには、LCS は Azure DevOps プロジェクトのソース コードがどこにあるか特定できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="76648-115">To create a build/test environment, LCS must be able to determine where the source code for the Azure DevOps project is.</span></span>
+ <span data-ttu-id="76648-116">開発者は開発者 VM のソース コードで作業し、その作業は Azure DevOps プロジェクトに同期されます。</span><span class="sxs-lookup"><span data-stu-id="76648-116">The developer works on source code on the developer VM, and the work is synced to the Azure DevOps project.</span></span>
+ <span data-ttu-id="76648-117">ビルド プロセスによって、コードが Azure DevOps からビルド / テスト VM に同期され、配置可能なパッケージが作成され、サンドボックスおよび実稼動環境に適用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="76648-117">The build process synchronizes the code from Azure DevOps onto the build/test VM and produces deployable packages that you can apply to sandbox and production environments.</span></span> <span data-ttu-id="76648-118">ソース コードは、開発 VM からビルド / テスト VM への直接フローを持ちません。</span><span class="sxs-lookup"><span data-stu-id="76648-118">The source code doesn't flow directly from the development VM to the build/test VM.</span></span> <span data-ttu-id="76648-119">これらは Azure DevOps を通して同期されます。</span><span class="sxs-lookup"><span data-stu-id="76648-119">They are synced through Azure DevOps.</span></span>

<span data-ttu-id="76648-120">カスタム テスト コードの記述またはビルド インフラストラクチャと統合するための自動テスト コードを生成する方法の詳細は、[テストと検証](testing-validation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76648-120">For information about how to write custom test code or generate automated test code to integrate with the build infrastructure, see [Testing and validations](testing-validation.md).</span></span>

## <a name="set-up-azure-devops"></a><span data-ttu-id="76648-121">Azure DevOps の設定</span><span class="sxs-lookup"><span data-stu-id="76648-121">Set up Azure DevOps</span></span>

### <a name="choose-a-plan"></a><span data-ttu-id="76648-122">計画を選択</span><span class="sxs-lookup"><span data-stu-id="76648-122">Choose a plan</span></span>

<span data-ttu-id="76648-123">最初のステップは組織に [Azure DevOps プランを選ぶ](https://www.visualstudio.com/products/visual-studio-team-services-feature-matrix-vs) ことです。</span><span class="sxs-lookup"><span data-stu-id="76648-123">The first step is to [choose an Azure DevOps plan](https://www.visualstudio.com/products/visual-studio-team-services-feature-matrix-vs) for your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="76648-124">TFVC はサポートされている唯一のソース管理リポジトリです。</span><span class="sxs-lookup"><span data-stu-id="76648-124">TFVC is the only source control repository that is supported.</span></span> <span data-ttu-id="76648-125">Git はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="76648-125">Git isn't supported.</span></span>

### <a name="set-up-azure-devops"></a><span data-ttu-id="76648-126">Azure DevOps の設定</span><span class="sxs-lookup"><span data-stu-id="76648-126">Set up Azure DevOps</span></span>

<span data-ttu-id="76648-127">Azure DevOps をセットアップするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="76648-127">To set up Azure DevOps, follow these steps.</span></span>

1. <span data-ttu-id="76648-128">[個人用アクセス トークンの作成](../lifecycle-services/synchronize-bpm-vsts.md#lcs-project-settings-set-up-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="76648-128">[Create a personal access token](../lifecycle-services/synchronize-bpm-vsts.md#lcs-project-settings-set-up-azure-devops).</span></span> <span data-ttu-id="76648-129">トークンはすべての LCS バックグラウンド アクションに使用されます。</span><span class="sxs-lookup"><span data-stu-id="76648-129">The token is used for all LCS background actions.</span></span> <span data-ttu-id="76648-130">これらのアクションにはアップグレードと配置が含まれます。</span><span class="sxs-lookup"><span data-stu-id="76648-130">These actions include upgrade and deployment.</span></span> <span data-ttu-id="76648-131">ユーザーが LCS からアクションを起動すると、LCS はこれらのユーザーが Azure DevOps に追加されることを期待しています。</span><span class="sxs-lookup"><span data-stu-id="76648-131">When users initiate actions from LCS, LCS expects that those users will be added to Azure DevOps.</span></span> <span data-ttu-id="76648-132">ユーザーは彼らのために Azure DevOps への LCS アクセスを認可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76648-132">The users must authorize LCS access to Azure DevOps on their behalf.</span></span>
1. <span data-ttu-id="76648-133">[LCS の構成](../lifecycle-services/synchronize-bpm-vsts.md#lcs-project-settings-set-up-azure-devops)。</span><span class="sxs-lookup"><span data-stu-id="76648-133">[Configure LCS](../lifecycle-services/synchronize-bpm-vsts.md#lcs-project-settings-set-up-azure-devops).</span></span>

<span data-ttu-id="76648-134">LCS の Azure DevOps へのアクセスを承認するまで、「設定が完了していません」 というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="76648-134">Until you authorize LCS access to Azure DevOps, you will see a "setup is not complete" message in action center.</span></span>

### <a name="suspend-current-builds"></a><span data-ttu-id="76648-135">現在のビルドの中断</span><span class="sxs-lookup"><span data-stu-id="76648-135">Suspend current builds</span></span>

<span data-ttu-id="76648-136">既にビルド定義を持つ既存の Azure DevOps プロジェクトにビルド環境を展開している場合、ビルドをキューに入れるアクティブなトリガーがないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="76648-136">If you're deploying a build environment on an existing Azure DevOps project that already has a build definition, make sure that you don't have any active triggers to queue the build.</span></span> <span data-ttu-id="76648-137">また、ビルド プールに対して、スケジュールされたりキューに格納されたビルドがないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="76648-137">Additionally, make sure that no builds are scheduled or queued against the build pool.</span></span>

## <a name="deploy-developer-and-buildtest-environments-from-lcs"></a><span data-ttu-id="76648-138">LCS 開発およびビルド / テスト環境の展開</span><span class="sxs-lookup"><span data-stu-id="76648-138">Deploy Developer and Build/Test environments from LCS</span></span>
<span data-ttu-id="76648-139">LCS では、開発およびビルド / テスト環境を展開するオプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="76648-139">LCS provides an option to deploy Development and Build/Test environments.</span></span> <span data-ttu-id="76648-140">このオプションでは、Azure DevOps プロジェクトに接続されたクラウド内に、開発者を配置して VM をビルドすることができます。</span><span class="sxs-lookup"><span data-stu-id="76648-140">With this option, you can deploy developer and build VMs in the cloud that are connected to your Azure DevOps project.</span></span>

### <a name="azure-devops-credential-setup-and-linking-to-lcs-project"></a><span data-ttu-id="76648-141">Azure DevOps 資格情報の設定と LCS プロジェクトへのリンク</span><span class="sxs-lookup"><span data-stu-id="76648-141">Azure DevOps credential setup and linking to LCS project</span></span>
<span data-ttu-id="76648-142">まだ完了していない場合は、ビルド環境を配置する前に、最初にLCS プロジェクトを設定してから Azure DevOps プロジェクトに接続してください。</span><span class="sxs-lookup"><span data-stu-id="76648-142">If you have not already done so, you need to first setup your LCS project to connect to your Azure DevOps project before you deploy a build environment.</span></span>

1. <span data-ttu-id="76648-143">[https://lcs.dynamics.com/](https://lcs.dynamics.com/)で LCS ポータルにログインして、Azure DevOps および LCS プロジェクトに接続します。</span><span class="sxs-lookup"><span data-stu-id="76648-143">Login to the LCS portal to connect to Azure DevOps and your LCS project at [https://lcs.dynamics.com/](https://lcs.dynamics.com/).</span></span>
2. <span data-ttu-id="76648-144">作業しているプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="76648-144">Select a project that you are working on.</span></span>
3. <span data-ttu-id="76648-145">**プロジェクト設定** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="76648-145">Click the **Project Settings** tile.</span></span>
4. <span data-ttu-id="76648-146">**Azure DevOps** を選択し、モジュール プロジェクトのソース コードが保管されている Azure DevOps URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="76648-146">Select **Azure DevOps** and enter the Azure DevOps URL where the source code for your module project is located.</span></span>
5. <span data-ttu-id="76648-147">Azure DevOps リンクを指定して、承認し、**既定のプロジェクトを選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="76648-147">Specify the Azure DevOps link, authorize, and then click **Choose default project**.</span></span>
   > [!NOTE]
   > <span data-ttu-id="76648-148">現在のところ、VSTF をソース コントロールとしてサポートしていますが、Git をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="76648-148">We currently support VSTF as source control and do not support Git.</span></span> 

### <a name="check-in-migrated-or-new-module-code-into-azure-devops"></a><span data-ttu-id="76648-149">Azure DevOps に移行または新しいモジュールコードをチェックイン</span><span class="sxs-lookup"><span data-stu-id="76648-149">Check-in migrated or new module code into Azure DevOps</span></span>

<span data-ttu-id="76648-150">コードの移行プロセスまたは開発活動の一環として、モデル ソース ファイルと関連するテスト モデル ソース ファイルを Azure DevOps にチェックインすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="76648-150">As part of code Migration process or development activities, we expect you to check-in your model source files and the associated test model source files into Azure DevOps.</span></span> <span data-ttu-id="76648-151">LCS 移行サービスを使用してコードを移行した場合、自動的に行われます。</span><span class="sxs-lookup"><span data-stu-id="76648-151">If you have migrated your code using the LCS migration service, this is automatically done for you.</span></span> <span data-ttu-id="76648-152">Azure DevOps にコードをチェックインせずに直接チェックインする場合は、Azure DevOps フォルダ構造の特定のガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="76648-152">If you have not checked in any code into Azure DevOps and work on direct check-in, you must follow certain guidelines for the Azure DevOps folder structure.</span></span> <span data-ttu-id="76648-153">これは、適切なビルド定義の設定に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="76648-153">This will help with setting up correct build definition.</span></span> <span data-ttu-id="76648-154">すべてのモジュールをルート フォルダー **メタデータ** に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76648-154">All modules should be added to root folder **Metadata**.</span></span> <span data-ttu-id="76648-155">各モジュールにはフォルダーが 2 つ必要です。</span><span class="sxs-lookup"><span data-stu-id="76648-155">Under each module, there should be two folders.</span></span> <span data-ttu-id="76648-156">1 つのフォルダーには、すべてのモデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="76648-156">One folder contains all models.</span></span> <span data-ttu-id="76648-157">他のフォルダーには、そのモジュールの記述子 XML が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="76648-157">The other folder should contain descriptor XML for that module.</span></span> 

![Azure DevOps フォルダー構造](media/build-trunk-main-metadata.png)

### <a name="deploy-a-build-environment"></a><span data-ttu-id="76648-159">ビルド環境の展開</span><span class="sxs-lookup"><span data-stu-id="76648-159">Deploy a Build environment</span></span>

<span data-ttu-id="76648-160">「[開発環境の展開およびアクセス](../dev-tools/access-instances.md)」のトピックでは、開発環境の展開方法が説明されています。</span><span class="sxs-lookup"><span data-stu-id="76648-160">The topic [Deploy and access development environments](../dev-tools/access-instances.md) describes how to deploy developer environments.</span></span> <span data-ttu-id="76648-161">同様のフローを使用して、ビルド環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="76648-161">Use the same flow to deploy a build environment.</span></span> <span data-ttu-id="76648-162">展開またはコンフィギュレーション ウィザードを実行する際に、**トポロジを選択してください** というメッセージが表示されたら、**ビルドおよびテスト** トポロジを選択してから **DevTest** を選択します。</span><span class="sxs-lookup"><span data-stu-id="76648-162">As you are going through the deployment or configuration wizard, when prompted to **Select a Topology**, select **DevTest** then select a **Build and Test** topology.</span></span>

<span data-ttu-id="76648-163">展開ウィザードの一部として、ビルド エージェント名およびビルド エージェント プールを構成できます。</span><span class="sxs-lookup"><span data-stu-id="76648-163">As part of the deployment wizard, you can configure the build agent name and build agent pool.</span></span>

<span data-ttu-id="76648-164">**詳細設定** をクリックし、**Azure DevOps** を選択します</span><span class="sxs-lookup"><span data-stu-id="76648-164">Click **Advanced settings**, select **Azure DevOps**</span></span>
   1.  <span data-ttu-id="76648-165">ビルド エージェント名: Azure DevOps ビルド エージェントのフレンドリ名</span><span class="sxs-lookup"><span data-stu-id="76648-165">Build Agent Name: Friendly name for build agent on Azure DevOps</span></span>
   2.  <span data-ttu-id="76648-166">ビルド エージェント プール: ビルド マシンの配置に使用するビルド エージェント プール名を指定します。</span><span class="sxs-lookup"><span data-stu-id="76648-166">Build Agent Pool: specify build agent pool name which should be used for build machine deployment.</span></span> <span data-ttu-id="76648-167">Azure DevOps に少なくとも 1 つのエージェント プールが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="76648-167">Make sure Azure DevOps contains at least one agent pool.</span></span> <span data-ttu-id="76648-168">既定では、既定のプールがあります。</span><span class="sxs-lookup"><span data-stu-id="76648-168">By default, there will be the default pool.</span></span> <span data-ttu-id="76648-169">既定のプールを削除した場合は、ビルド配置は失敗します。</span><span class="sxs-lookup"><span data-stu-id="76648-169">If you have deleted the default pool then build deployment will fail.</span></span>
   3.  <span data-ttu-id="76648-170">分岐名: ビルド VM の既定のソース コード同期場所になる Azure DevOps ソース コード ブランチを指定します。</span><span class="sxs-lookup"><span data-stu-id="76648-170">Branch Name: Specify your Azure DevOps source code branch which will be default source code sync location for the build VM.</span></span> <span data-ttu-id="76648-171">既定の分岐は、「メイン」です。</span><span class="sxs-lookup"><span data-stu-id="76648-171">Default branch is "Main".</span></span>

   
## <a name="test-integration-with-the-build"></a><span data-ttu-id="76648-172">ビルドとのテスト統合</span><span class="sxs-lookup"><span data-stu-id="76648-172">Test integration with the build</span></span>
<span data-ttu-id="76648-173">テストと検証のためのビルド プロセスの一部としてテストを統合するには、2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="76648-173">There are two ways to integrate test as part of build process for testing and validation:</span></span>

-   <span data-ttu-id="76648-174">単位とコンポーネントのレベル テストに基づく SysTest フレームワーク。</span><span class="sxs-lookup"><span data-stu-id="76648-174">SysTest framework based unit and component level tests.</span></span>
-   <span data-ttu-id="76648-175">自動化されたテストの実行の XML を記録するタスク レコーダーから、コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="76648-175">Generate code from Task Recorder recording XML for automated test execution.</span></span>

<span data-ttu-id="76648-176">これらの2つの方法の詳細については、 [テストと検証](testing-validation.md) の記事で説明しています。</span><span class="sxs-lookup"><span data-stu-id="76648-176">The details of these two approaches are mentioned in the [Testing and validation](testing-validation.md) article.</span></span> <span data-ttu-id="76648-177">テストおよび検証の手順については、この資料を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76648-177">Review this article for testing and validation strategy.</span></span>

## <a name="use-the-build-vm-environment"></a><span data-ttu-id="76648-178">ビルド VM 環境の使用</span><span class="sxs-lookup"><span data-stu-id="76648-178">Use the Build VM environment</span></span>
<span data-ttu-id="76648-179">LCS を通じて開発者トポロジにビルド VM が配置されると、それは事前に構成され、ビルドを開始する準備ができます。</span><span class="sxs-lookup"><span data-stu-id="76648-179">When a Build VM is deployed in Developer topology through LCS, it is pre-configured and ready to start a build.</span></span> <span data-ttu-id="76648-180">Visual Studio IDE または Azure DevOps インターフェイスから、いつでも既定の構成を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="76648-180">You can change the default configuration at any time from the Visual Studio IDE or the Azure DevOps interface.</span></span> <span data-ttu-id="76648-181">ビルド VM では、簡単なビルドのセットアップのために、モジュール ソース コードがビルド コンピューターに同期されます。</span><span class="sxs-lookup"><span data-stu-id="76648-181">On a Build VM, the module source code is synchronized to the build machine for easy build setup.</span></span> <span data-ttu-id="76648-182">ビルド マシンは、ビルド エージェント、ビルド コントローラー、ビルド プロセス テンプレート、ビルド定義のデフォルト設定で自動構成されています。</span><span class="sxs-lookup"><span data-stu-id="76648-182">The build machine is also auto-configured with default settings for build agent, build controller, build process template, and build definition.</span></span> <span data-ttu-id="76648-183">ビルドに成功したら、ビルド定義と統合されているテストが実行されます。</span><span class="sxs-lookup"><span data-stu-id="76648-183">Tests that are integrated with build definition are executed after the build is successful.</span></span>

### <a name="review-a-pre-configured-customizable-build-environment"></a><span data-ttu-id="76648-184">定義済みのカスタマイズ可能なビルド環境を確認</span><span class="sxs-lookup"><span data-stu-id="76648-184">Review a pre-configured customizable build environment</span></span>

<span data-ttu-id="76648-185">ビルド VM には、**Azure DevOps** の一部としてリリースされた vNext ビルド エージェントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="76648-185">The build VM contains the vNext build agent which was released as part of **Azure DevOps**.</span></span> <span data-ttu-id="76648-186">ビルド VM を配置するときは、既定では Azure DevOps プロジェクトと接続して同期するようにビルド エージェントが構成されます。</span><span class="sxs-lookup"><span data-stu-id="76648-186">When you deploy the Build VM, the build agent is configured by default to connect and sync with the Azure DevOps project.</span></span> <span data-ttu-id="76648-187">ビルド VM 構成の一部として、以下に示すようにデフォルトのビルド定義も作成および構成されます。</span><span class="sxs-lookup"><span data-stu-id="76648-187">As a part of the Build VM configuration, the default build definition is also created and configured, as shown below.</span></span> 

<span data-ttu-id="76648-188">[![既定のビルド定義](./media/build1-1024x488.jpg)](./media/build1.jpg)</span><span class="sxs-lookup"><span data-stu-id="76648-188">[![Default build definition](./media/build1-1024x488.jpg)](./media/build1.jpg)</span></span> 

<span data-ttu-id="76648-189">既定のビルド定義には、以下で説明するように、特定の操作を実行する複数のタスクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="76648-189">Default build definition contains multiple tasks to perform specific operation, as described below.</span></span>

1.  <span data-ttu-id="76648-190">ビルドに渡す事前定義済の変数パラメータをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="76648-190">Configure the predefined variables parameters that will be passed to the build.</span></span> <span data-ttu-id="76648-191">ビルド実行ごとにクリーンなデータベースを設定するには、**DatabaseBackupToRestore** 変数のデータベース バックアップ ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="76648-191">To set up a clean database for every build execution, provide the name of the database backup file for the **DatabaseBackupToRestore** variable.</span></span> <span data-ttu-id="76648-192">パッケージ フォルダーは、すべてのビルド時にクリーン パッケージ フォルダーのコピーで復元されます。</span><span class="sxs-lookup"><span data-stu-id="76648-192">The packages folder is restored at every build with a copy of a clean package folder.</span></span>

    <span data-ttu-id="76648-193">[![定義済み変数ウィンドウ一覧](./media/build2-1024x678.jpg)](./media/build2.jpg)</span><span class="sxs-lookup"><span data-stu-id="76648-193">[![List of predefined variables pane](./media/build2-1024x678.jpg)](./media/build2.jpg)</span></span>

2.  <span data-ttu-id="76648-194">以下のように、「トランク/メイン」ブランチにあるすべてのモジュールを検出して構築するためにソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="76648-194">Build the solution to discover and build all modules under "Trunk/Main" branch as shown below.</span></span>

    <span data-ttu-id="76648-195">[![ソリューション ウィンドウ を ビルド します。](./media/build3-1024x456.jpg)](./media/build3.jpg)</span><span class="sxs-lookup"><span data-stu-id="76648-195">[![Build the solution pane](./media/build3-1024x456.jpg)](./media/build3.jpg)</span></span>

3.  <span data-ttu-id="76648-196">「レポートの展開」タスクを使用して、レポートを生成し、ビルド VM に展開します。</span><span class="sxs-lookup"><span data-stu-id="76648-196">Use "Deploy Report" task to generate reports and deploy on build VM.</span></span>
4.  <span data-ttu-id="76648-197">「データベース同期」タスクを使用して、データベースをビルド VM 上のローカル SQL に同期させます。</span><span class="sxs-lookup"><span data-stu-id="76648-197">Use "Database Sync" task to synchronize the database to local SQL on build VM.</span></span>
5.  <span data-ttu-id="76648-198">ビルドが成功した後、サンドボックス/ステージング環境を更新するために使用できる配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="76648-198">After the build is successful, create a deployable package that can be used to update sandbox/ staging environment.</span></span>

    <span data-ttu-id="76648-199">[![パッケージ ウィンドウ を生成します](./media/build4-1024x462.jpg)](./media/build4.jpg)</span><span class="sxs-lookup"><span data-stu-id="76648-199">[![Generate packages pane](./media/build4-1024x462.jpg)](./media/build4.jpg)</span></span>

6.  <span data-ttu-id="76648-200">「ビルド コンポーネントのコピーと発行」は、配置可能パッケージを Azure DevOps コンポーネントの場所にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="76648-200">"Copy and publish build artifacts" uploads the deployable package to Azure DevOps artifacts location.</span></span>

    <span data-ttu-id="76648-201">[![成果物ウィンドウを公開する](./media/build5-1024x439.jpg)](./media/build5.jpg)</span><span class="sxs-lookup"><span data-stu-id="76648-201">[![Publish Artifact pane](./media/build5-1024x439.jpg)](./media/build5.jpg)</span></span>

7.  <span data-ttu-id="76648-202">テストの実行については、3 つの既定のタスク「テスト設定」、「テストの実行」、および「テストの終了」があります。</span><span class="sxs-lookup"><span data-stu-id="76648-202">For test execution, there are three default tasks "Test Setup", "Execute Test" and "Test End".</span></span>

    <span data-ttu-id="76648-203">[![テスト実行ウィンドウ](./media/build7-1024x457.jpg)](./media/build7.jpg)</span><span class="sxs-lookup"><span data-stu-id="76648-203">[![Execute Tests pane](./media/build7-1024x457.jpg)](./media/build7.jpg)</span></span>

8.  <span data-ttu-id="76648-204">既定のビルドでは毎日午後 5 時に開始される予定です。</span><span class="sxs-lookup"><span data-stu-id="76648-204">The default build is scheduled to trigger start every day at 5 P.M.</span></span> <span data-ttu-id="76648-205">チームの必要性に従って、各チェックインでトリガーを「継続」に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="76648-205">You can change trigger as per your team's need to "Continuous" for each check-in.</span></span>

    <span data-ttu-id="76648-206">[![既定のビルド スケジュール](./media/build8-1024x491.jpg)](./media/build8.jpg)</span><span class="sxs-lookup"><span data-stu-id="76648-206">[![Default build schedule](./media/build8-1024x491.jpg)](./media/build8.jpg)</span></span>

<span data-ttu-id="76648-207">既定の構成に変更を加えて、そのビルド VM がビルドをトリガーできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="76648-207">You can make changes to the default configuration, and the build VM will be ready to trigger a build.</span></span>

## <a name="start-a-build-and-verify-the-build-and-test-execution-results"></a><span data-ttu-id="76648-208">ビルドを開始し、ビルドとテストの実行結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="76648-208">Start a build and verify the build and test execution results</span></span>
<span data-ttu-id="76648-209">既定のビルド構成を確認した後、Visual Studio IDE または Azure DevOps Web インターフェイスからビルドを手動でトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="76648-209">After you review the default build configuration, you can manually trigger a build from Visual Studio IDE or Azure DevOps web interface.</span></span>

1.  <span data-ttu-id="76648-210">ブラウザーを開き、Azure DevOps URL に接続します。</span><span class="sxs-lookup"><span data-stu-id="76648-210">Open your browser and connect to the Azure DevOps URL.</span></span>
2.  <span data-ttu-id="76648-211">資格情報を使用してをログインします。</span><span class="sxs-lookup"><span data-stu-id="76648-211">Login using your credentials.</span></span>
3.  <span data-ttu-id="76648-212">ホーム ページの **最近のプロジェクトとソリューション** で、プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="76648-212">On the home page, under **Recent projects and solutions**, select a project.</span></span>
4.  <span data-ttu-id="76648-213">上部リンク オプションから、**ビルド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="76648-213">From top links options, select **BUILD**.</span></span>
5.  <span data-ttu-id="76648-214">左側のパネルで、既定のビルド定義インスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="76648-214">On the left panel, select the default build definition instance.</span></span>
6.  <span data-ttu-id="76648-215">右クリックし、**キュー ビルド** を選択して Azure DevOps ソース管理に既にチェックインしているモジュールおよびテスト モジュールのビルドをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="76648-215">Right-click and select **Queue Build** to trigger a build for your module and test module that is already checked into the Azure DevOps source control.</span></span>

<span data-ttu-id="76648-216">次の例に示すように、ビルドの成功または失敗が表示されます。</span><span class="sxs-lookup"><span data-stu-id="76648-216">Success or failure for the build will display, as shown by the following examples.</span></span> <span data-ttu-id="76648-217">すべてのビルドを表示します。</span><span class="sxs-lookup"><span data-stu-id="76648-217">View all builds.</span></span> 

<span data-ttu-id="76648-218">[![ビルドの成功または失敗を表示](./media/build9-1024x443.jpg)](./media/build9.jpg)</span><span class="sxs-lookup"><span data-stu-id="76648-218">[![Display of build success or failure](./media/build9-1024x443.jpg)](./media/build9.jpg)</span></span> 

<span data-ttu-id="76648-219">特定の完了したビルドとビューの成功/失敗の詳細を選択します。</span><span class="sxs-lookup"><span data-stu-id="76648-219">Select specific completed build and view success/ failure details.</span></span> 

<span data-ttu-id="76648-220">[![ビルドの成功または失敗の詳細を表示する](./media/build10-1024x446.jpg)](./media/build10.jpg) テストのリンクをクリックすると、テストの実行の失敗が表示されます。</span><span class="sxs-lookup"><span data-stu-id="76648-220">[![View details of build success or failure](./media/build10-1024x446.jpg)](./media/build10.jpg) Click on Test link to visualize test execution failure.</span></span> 

<span data-ttu-id="76648-221">[![テスト実行エラーの可視化](./media/build11-1024x455.jpg)](./media/build11.jpg)</span><span class="sxs-lookup"><span data-stu-id="76648-221">[![Visualize test execution failure](./media/build11-1024x455.jpg)](./media/build11.jpg)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]