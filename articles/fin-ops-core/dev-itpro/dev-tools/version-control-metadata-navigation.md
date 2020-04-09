---
title: バージョン コントロール、メタデータ検索、およびナビゲーション
description: このチュートリアルでは、Azure DevOps (以前の名称は Visual Studio Online) を設定して、モデルのソース管理を有効にします。 これは、"仕事" のタスクの作成および整理、メタデータおよびソース コードの検索、関連するモデル要素間の移動、モデルからのプロジェクトの作成を行う機能など、開発ツールでのその他の生産性機能について把握することにも役立ちます。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 23401
ms.assetid: 46ed0115-6f8b-4757-b8d2-d4ccb76c733d
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e43b6e93f1b0b25b0657d1dfe0b7c54cc4f637c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154145"
---
# <a name="version-control-metadata-search-and-navigation"></a><span data-ttu-id="279b9-104">バージョン コントロール、メタデータ検索、およびナビゲーション</span><span class="sxs-lookup"><span data-stu-id="279b9-104">Version control, metadata search, and navigation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="279b9-105">このチュートリアルでは、Azure DevOps (以前の名称は Visual Studio Online) を設定して、モデルのソース管理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="279b9-105">This tutorial will walk you through configuring Azure DevOps (previously known as Visual Studio Online) to enable source control on your models.</span></span> <span data-ttu-id="279b9-106">これは、"仕事" のタスクの作成および整理、メタデータおよびソース コードの検索、関連するモデル要素間の移動、モデルからのプロジェクトの作成を行う機能など、開発ツールでのその他の生産性機能について把握することにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="279b9-106">It’ll also help you learn about other productivity features in the development tools, including the ability to create and organize TODO task, search metadata and source code, navigate between related model elements, and create a project from a model.</span></span>

## <a name="configure-your-azure-devops-account-and-project"></a><span data-ttu-id="279b9-107">Azure DevOps アカウントおよびプロジェクトをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="279b9-107">Configure your Azure DevOps account and project</span></span>

<span data-ttu-id="279b9-108">このセクションでは、Azure DevOps で新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="279b9-108">In this section, you'll create a new project in Azure DevOps.</span></span> <span data-ttu-id="279b9-109">このプロジェクトはモデルのソース コードをホストします。</span><span class="sxs-lookup"><span data-stu-id="279b9-109">This project will host the source code of your model.</span></span> <span data-ttu-id="279b9-110">例として、フリート管理モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="279b9-110">You'll use the Fleet Management model as an example.</span></span> <span data-ttu-id="279b9-111">Azure DevOps アカウントをお持ちでない場合は、作成します。</span><span class="sxs-lookup"><span data-stu-id="279b9-111">If you don't have a Azure DevOps account, you'll create one.</span></span>

### <a name="sign-up-to-azure-devops-create-an-account-and-create-a-new-project"></a><span data-ttu-id="279b9-112">Azure DevOps への登録、アカウントの作成、および新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="279b9-112">Sign up to Azure DevOps, create an account, and create a new project</span></span>

<span data-ttu-id="279b9-113"><https://www.visualstudio.com/> に移動して Azure DevOps にサインアップします。</span><span class="sxs-lookup"><span data-stu-id="279b9-113">Navigate to <https://www.visualstudio.com/> to sign up for Azure DevOps.</span></span> <span data-ttu-id="279b9-114">**サインアップ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-114">Click **Sign up**.</span></span> <span data-ttu-id="279b9-115">Azure DevOps アカウントを既に持っている場合は、このトピックの後半の「Azure DevOps プロジェクトの作成」セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="279b9-115">If you already have an account in Azure DevOps, go to the Create a Azure DevOps project section later in this topic.</span></span> 

1.  <span data-ttu-id="279b9-116">Microsoft アカウントでサインインします。</span><span class="sxs-lookup"><span data-stu-id="279b9-116">Sign in with your Microsoft account.</span></span>

    > [!NOTE]
    > <span data-ttu-id="279b9-117">組織のアカウント (Microsoft Office 365 ドメイン) を使用することも可能です。</span><span class="sxs-lookup"><span data-stu-id="279b9-117">You can also use an organizational account (Microsoft Office 365 domain).</span></span>

2.  <span data-ttu-id="279b9-118">Azure DevOps アカウントを作成し、アカウントの URL を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-118">Create a Azure DevOps account, and select a URL for your account.</span></span> <span data-ttu-id="279b9-119">これは、Visual Studio でソース管理を設定するときに、開発用コンピューターから接続する URL です。</span><span class="sxs-lookup"><span data-stu-id="279b9-119">This is the URL that you'll connect to from your development computer when you're configuring source control in Visual Studio.</span></span> <span data-ttu-id="279b9-120">次は、アカウント URLの例です。</span><span class="sxs-lookup"><span data-stu-id="279b9-120">The following is an example of the account URL.</span></span> 

    <span data-ttu-id="279b9-121">[![AccountURL\_UsingDevoTools](./media/accounturl_usingdevotools.png)](./media/accounturl_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-121">[![AccountURL\_UsingDevoTools](./media/accounturl_usingdevotools.png)](./media/accounturl_usingdevotools.png)</span></span> 

    <span data-ttu-id="279b9-122">アカウントが作成されると、アカウントのメイン ページに進むように指示され、そこで最初のプロジェクトの作成を求められます。</span><span class="sxs-lookup"><span data-stu-id="279b9-122">When the account is created, you're directed to your account main page where you're prompted to create your first project.</span></span>
3.  <span data-ttu-id="279b9-123">デモ**フリート管理**プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="279b9-123">Create a demo **Fleet Management** project.</span></span> 

    <span data-ttu-id="279b9-124">[![FirstProject\_UsingDevoTools](./media/firstproject_usingdevotools.png)](./media/firstproject_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-124">[![FirstProject\_UsingDevoTools](./media/firstproject_usingdevotools.png)](./media/firstproject_usingdevotools.png)</span></span>

### <a name="create-a-azure-devops-team-project"></a><span data-ttu-id="279b9-125">Azure DevOps チーム プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="279b9-125">Create a Azure DevOps team project</span></span>

<span data-ttu-id="279b9-126">Azure DevOps アカウントを既に持っている場合は、Internet Explorer を使用してアカウントに移動します。</span><span class="sxs-lookup"><span data-stu-id="279b9-126">If you already have a Azure DevOps account, go to your account using Internet Explorer.</span></span> <span data-ttu-id="279b9-127">このトピックでは、説明のために URL の例として **.visualstudio.com** を使用します。</span><span class="sxs-lookup"><span data-stu-id="279b9-127">This topic uses **.visualstudio.com** as the example URL for illustration purposes.</span></span>

1. <span data-ttu-id="279b9-128"><https://www.visualstudio.com/> に移動します。</span><span class="sxs-lookup"><span data-stu-id="279b9-128">Go to <https://www.visualstudio.com/>.</span></span>
2. <span data-ttu-id="279b9-129">**最近使用したプロジェクトとチーム** で **新規** をクリックして新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="279b9-129">Under **Recent projects & teams**, click **New** to create a new project.</span></span> 

   <span data-ttu-id="279b9-130">[![ClickNew\_UsingDevoTools](./media/clicknew_usingdevotools.png)](./media/clicknew_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-130">[![ClickNew\_UsingDevoTools](./media/clicknew_usingdevotools.png)](./media/clicknew_usingdevotools.png)</span></span>

3. <span data-ttu-id="279b9-131">**プロジェクト名**フィールドに、**フリート管理**と入力し、**説明**を入力してから**プロジェクトの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-131">In the **Project name** field, enter **Fleet Management**, enter a **Description**, and then click **Create project**.</span></span>

### <a name="create-the-recommended-folder-structure-in-your-team-project"></a><span data-ttu-id="279b9-132">チーム プロジェクトで推奨するフォルダー構造を作成する</span><span class="sxs-lookup"><span data-stu-id="279b9-132">Create the recommended folder structure in your team project</span></span>

<span data-ttu-id="279b9-133">Lifecycle Services (LCS) 自動化コードのアップグレード ツールを使用して以前のバージョンからコードを移行した場合、以下のフォルダ構造は、Azure DevOps チーム プロジェクトで自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="279b9-133">If you have migrated your code from a previous version using the Lifecycle Services (LCS) automated code upgrade tool, the following folder structure is automatically created in your Azure DevOps team project.</span></span> 

<span data-ttu-id="279b9-134">[![VSOfolders](./media/vsofolders1.png)](./media/vsofolders1.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-134">[![VSOfolders](./media/vsofolders1.png)](./media/vsofolders1.png)</span></span>

<span data-ttu-id="279b9-135">**メタデータ**フォルダーには、パッケージとモデルによって整理されたソース XML ファイルがあり、**プロジェクト**フォルダーには Visual Studio プロジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="279b9-135">The **Metadata** folder contains your source XML files organized by packages and models and the **Projects** folder contains Visual Studio projects.</span></span> <span data-ttu-id="279b9-136">コードを移行せず、最初から開始している場合、開発を開始する前に、チーム プロジェクト内のサーバーに類似したフォルダ構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="279b9-136">If you are not migrating code and are starting from scratch, create a similar folder structure on the server in your team project before you start development.</span></span>

### <a name="configure-visual-studio-to-connect-to-your-team-project"></a><span data-ttu-id="279b9-137">Visual Studio をコンフィギュレーションしてチーム プロジェクトに接続する</span><span class="sxs-lookup"><span data-stu-id="279b9-137">Configure Visual Studio to connect to your team project</span></span>

1.  <span data-ttu-id="279b9-138">管理ユーザーとしてログインしている場合は、Visual Studio を管理者として起動します。</span><span class="sxs-lookup"><span data-stu-id="279b9-138">When logged in as an administrative user, start Visual Studio as Administrator.</span></span>
2.  <span data-ttu-id="279b9-139">**ツール &gt; オプション &gt; ソース管理 &gt; プラグインの選択** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-139">Click **Tools &gt; Options &gt; Source Control &gt; Plug-in Selection**.</span></span>
3.  <span data-ttu-id="279b9-140">現在のソース管理プラグイン フィールドで **Visual studio Team Foundation Server** を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-140">In the Current source control plug-in field, select **Visual studio Team Foundation Server**.</span></span>
4.  <span data-ttu-id="279b9-141">**チーム &gt; Team Foundation Server に接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-141">Select **Team &gt; Connect to Team Foundation Server**.</span></span>
5.  <span data-ttu-id="279b9-142">**チーム エクスプローラー**で、**チーム プロジェクトの選択**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-142">In **Team Explorer**, click **Select Team Projects**.</span></span>
6.  <span data-ttu-id="279b9-143">**Team Foundation Server の選択**ドロップダウン リストで、フリート管理プロジェクトをホストする **Azure DevOps アカウント**を選択するか、メニューにない場合は**サーバー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-143">In the **Select a Team Foundation Server** drop-down list, select the **Azure DevOps account** that hosts the Fleet Management project, or click **Servers** if it isn't in the menu.</span></span>
    1.  <span data-ttu-id="279b9-144">**Team Foundation Server の追加および削除** ダイアログ ボックスが開いたとき、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-144">When the **Add/Remove Team Foundation Server** dialog opens, click **Add**.</span></span>
    2.  <span data-ttu-id="279b9-145">Azure DevOps アカウントの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="279b9-145">Enter the URL of your Azure DevOps account.</span></span>
    3.  <span data-ttu-id="279b9-146">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-146">Click **OK**.</span></span>
    4.  <span data-ttu-id="279b9-147">メッセージが表示されたら、Microsoft アカウントのユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="279b9-147">If prompted, enter your Microsoft Account username and password.</span></span>

7.  <span data-ttu-id="279b9-148">**チーム プロジェクト** で **フリート管理** チェック ボックスをオンにし、**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-148">Select the **Fleet Management** check box under **Team projects**, and then click **Connect**.</span></span> 

    <span data-ttu-id="279b9-149">[![ConnectTFSServer\_UsingDevoTools](./media/connecttfsserver_usingdevotools.png)](./media/connecttfsserver_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-149">[![ConnectTFSServer\_UsingDevoTools](./media/connecttfsserver_usingdevotools.png)](./media/connecttfsserver_usingdevotools.png)</span></span>

### <a name="map-your-azure-devops-project-to-your-local-model-store-and-projects-folder"></a><span data-ttu-id="279b9-150">Azure DevOps プロジェクトをローカルのモデル ストアとプロジェクト フォルダーにマップ</span><span class="sxs-lookup"><span data-stu-id="279b9-150">Map your Azure DevOps project to your local model store and projects folder</span></span>

<span data-ttu-id="279b9-151">モデル ストアのルート フォルダーには、アプリケーションの一部であるすべてのパッケージとモデルのソース ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="279b9-151">Your model store root folder contains source files of all packages and models that are part of your application.</span></span> <span data-ttu-id="279b9-152">展開中には、複数のパッケージにまたがる複数のモデルのソース ファイルを使用するでしょう。</span><span class="sxs-lookup"><span data-stu-id="279b9-152">During deployment, you'll probably use source files from more than one model across more than one package.</span></span> <span data-ttu-id="279b9-153">このため、モデル ストアのルート フォルダーを Azure DevOps のチーム プロジェクト メタデータ フォルダーにマップすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="279b9-153">Because of this, we recommend that you map your model store root folder to the Azure DevOps team project metadata folder.</span></span>

1. <span data-ttu-id="279b9-154">Visual studio の**チーム エクスプローラー**で、このドキュメントで前に説明したようにチーム プロジェクトに接続します。</span><span class="sxs-lookup"><span data-stu-id="279b9-154">In Visual studio **Team Explorer**, connect to the team project as described earlier in this document.</span></span>
2. <span data-ttu-id="279b9-155">**ソース管理エクスプローラー**から**チーム エクスプローラー**を開きます。</span><span class="sxs-lookup"><span data-stu-id="279b9-155">Open **Source Control Explorer** from **Team Explorer**.</span></span>
3. <span data-ttu-id="279b9-156">チーム プロジェクトの **メタデータ** フォルダーを、ローカル ドライブのモデル ストアのルート フォルダー (通常は K:\\AOSService\\PackagesLocalDirectory) にマップします。例を以下の図に示します。</span><span class="sxs-lookup"><span data-stu-id="279b9-156">Map the **Metadata** folder of your team project to the root folder of the model store on your local drive (Typically K:\\AOSService\\PackagesLocalDirectory), an example is shown in the image below.</span></span>

    > [!NOTE]
    > <span data-ttu-id="279b9-157">マシンの構成によっては、モデル ストアが I:\\AosService\\PackagesLocalDirectory または別のドライブの配下にある場合があります。</span><span class="sxs-lookup"><span data-stu-id="279b9-157">Your model store may be located under I:\\AosService\\PackagesLocalDirectory or another drive, depending on your machine configuration.</span></span>

    <span data-ttu-id="279b9-158">[![VSOfolders2](./media/vsofolders21.png)](./media/vsofolders21.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-158">[![VSOfolders2](./media/vsofolders21.png)](./media/vsofolders21.png)</span></span>

4. <span data-ttu-id="279b9-159">**マップ**をクリックし、次のダイアログ ボックスで、**No** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-159">Click **Map**, and on the next dialog, click **No**.</span></span>
5. <span data-ttu-id="279b9-160">同様に、**/Trunk/Main/Projects** サーバー フォルダーを、Visual Studio ソリューションとプロジェクト ファイルを保持する **ローカル プロジェクト フォルダー** にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="279b9-160">Similarly, map the **/Trunk/Main/Projects** server folder to the **local projects folder** that will hold your Visual Studio solution and project files.</span></span>

## <a name="scenario-1-open-the-fleet-management-solution-and-add-it-to-azure-devops-source-control"></a><span data-ttu-id="279b9-161">シナリオ 1: フリート管理ソリューションを開き、Azure DevOps ソース管理に追加する</span><span class="sxs-lookup"><span data-stu-id="279b9-161">Scenario 1: Open the fleet management solution and add it to Azure DevOps source control</span></span>
<span data-ttu-id="279b9-162">このセクションでは、Azure DevOps のソース管理にソリューションを追加するために必要なステップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="279b9-162">This section describes the steps needed to add a solution to Azure DevOps source control.</span></span> <span data-ttu-id="279b9-163">このシナリオは、新しいモデルで開発を開始し、初めてソース管理に追加する場合に関係します。</span><span class="sxs-lookup"><span data-stu-id="279b9-163">This scenario is relevant when you have started development on a new model and you are adding it to source control for the first time.</span></span> <span data-ttu-id="279b9-164">コード移行シナリオまたは他の開発者により作成された新しいモデルを同期する場合は、以下のシナリオ 2 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="279b9-164">For code migration scenarios or in the case you are synchronizing new models that have been created by another developer, refer to scenario 2 below.</span></span>

### <a name="open-the-fleetmanagement-solution"></a><span data-ttu-id="279b9-165">FleetManagement ソリューションを開く</span><span class="sxs-lookup"><span data-stu-id="279b9-165">Open the FleetManagement solution</span></span>

> [!NOTE]
> <span data-ttu-id="279b9-166">これはほんの一例に過ぎません。</span><span class="sxs-lookup"><span data-stu-id="279b9-166">This is only an example.</span></span> <span data-ttu-id="279b9-167">任意のプロジェクト/ソリューションを開いて、ソリューションをソース管理に追加するプロセスについて学習することができます。</span><span class="sxs-lookup"><span data-stu-id="279b9-167">You can open any project/solution to learn about the process of adding a solution to source control.</span></span>

1.  <span data-ttu-id="279b9-168">**ファイル**メニューで、**開く**をポイントし、**プロジェクト/ソリューション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-168">On the **File** menu, point to **Open**, and then click **Project/Solution**.</span></span>
2.  <span data-ttu-id="279b9-169">デスクトップを参照し、**FleetManagement** フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="279b9-169">Browse to the desktop and open the **FleetManagement** folder.</span></span>
3.  <span data-ttu-id="279b9-170">**FleetManagement** という名前のソリューション ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-170">Select the solution file named **FleetManagement**.</span></span> <span data-ttu-id="279b9-171">表示されるファイル タイプは Microsoft Visual Studio Solution です。</span><span class="sxs-lookup"><span data-stu-id="279b9-171">The file type listed is Microsoft Visual Studio Solution.</span></span> <span data-ttu-id="279b9-172">ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。</span><span class="sxs-lookup"><span data-stu-id="279b9-172">If the solution file is not on your computer, the steps to create it are listed in [Tutorial: Create a Fleet Management solution file out of the Fleet Management models in the AOT](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot).</span></span>
4.  <span data-ttu-id="279b9-173">**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-173">Click **Open**.</span></span> <span data-ttu-id="279b9-174">ソリューションの読み込みには時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="279b9-174">Loading the solution may take some time.</span></span>

### <a name="add-the-fleetmanagement-solution-to-source-control"></a><span data-ttu-id="279b9-175">ソース コントロールへの FleetManagement ソリューションの追加</span><span class="sxs-lookup"><span data-stu-id="279b9-175">Add the FleetManagement solution to source control</span></span>

1.  <span data-ttu-id="279b9-176">**ソリューション エクスプローラー**で、フリート管理ソリューションを右クリックして、**ソリューションをソース管理に追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-176">In **Solution Explorer**, right-click the Fleet Management solution, and select **Add Solution to Source Control.**</span></span>
2.  <span data-ttu-id="279b9-177">次のダイアログで、**Team Foundation バージョン管理**を選択し、**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-177">On the next dialog, select **Team Foundation Version Control**, and then click **Next**.</span></span>
3.  <span data-ttu-id="279b9-178">**チーム プロジェクト ロケーション**にて、以下画像のように **プロジェクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-178">In the **Team Project Location**, select **Projects**, as shown in this image.</span></span>

    > [!NOTE]
    > <span data-ttu-id="279b9-179">サーバープロジェクト フォルダ を FleetManagement ソリューションを含むローカルフォルダに既にマッピングしている場合は、手順2 と 3 を省略します。</span><span class="sxs-lookup"><span data-stu-id="279b9-179">If you have already mapped the server Projects folder to a local folder that contains the FleetManagement solution, steps 2 and 3 are omitted.</span></span>

    <span data-ttu-id="279b9-180">[![VSOfolders3](./media/vsofolders31.png)](./media/vsofolders31.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-180">[![VSOfolders3](./media/vsofolders31.png)](./media/vsofolders31.png)</span></span>

4.  <span data-ttu-id="279b9-181">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-181">Click OK.</span></span>
5.  <span data-ttu-id="279b9-182">**チーム エクスプ ローラー &gt; 保留中の変更**に移動し、**チェックイン**をクリックして、ソリューションおよびモデル要素が Azure DevOps ソース管理にチェックインするようにします。</span><span class="sxs-lookup"><span data-stu-id="279b9-182">Go to **Team Explorer &gt; Pending changes**, and then click **Check-in** to check-in your solution and its model element to the Azure DevOps source control.</span></span>

### <a name="add-the-model-descriptor-file-to-source-control"></a><span data-ttu-id="279b9-183">ソース コントロールへのモデル記述子ファイルの追加</span><span class="sxs-lookup"><span data-stu-id="279b9-183">Add the model descriptor file to source control</span></span>

<span data-ttu-id="279b9-184">すべての Visual Studio プロジェクトはモデルに属しています。</span><span class="sxs-lookup"><span data-stu-id="279b9-184">All Visual Studio projects belong to models.</span></span> <span data-ttu-id="279b9-185">モデルは、通常 Visual Studio プロジェクトよりも大きなスコープ内にあるソース コードの配布と配置の単位です。</span><span class="sxs-lookup"><span data-stu-id="279b9-185">Models are source code distribution and deployment units that are typically larger in scope than a Visual Studio project.</span></span> <span data-ttu-id="279b9-186">前のセクションでは、ソース管理にフリート管理ソリューションの要素のファイルを追加しました。</span><span class="sxs-lookup"><span data-stu-id="279b9-186">In the previous section, you added element files of the fleet management solution to source control.</span></span> <span data-ttu-id="279b9-187">フリート管理モデルの要素をソース管理に追加したのは初めてのため、モデル記述子ファイルをチェックインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="279b9-187">Because this was the first time that you added elements of the Fleet Management models to source control, you'll also need to check-in the model descriptor file.</span></span>

1.  <span data-ttu-id="279b9-188">Visual Studio の**チーム エクスプローラー**で、**ソース管理エクスプローラー**を開いてから、メタデータ フォルダー (たとえば、**\Trunk\Main\Metadata**) を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-188">In Visual Studio, in **Team Explorer**, open **Source Control Explorer**, and then right-click on the metadata folder (for example, **\Trunk\Main\Metadata**).</span></span>
2.  <span data-ttu-id="279b9-189">**ソース管理エクスプローラー** ツール バーで、**フォルダーへの項目の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-189">In the **Source Control Explorer** toolbar, click **Add Item to Folder**.</span></span>
3.  <span data-ttu-id="279b9-190">モデル記述子ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-190">Select your model descriptor file.</span></span> <span data-ttu-id="279b9-191">モデル記述子ファイルは、モデルの XML ファイルのマニフェストです。</span><span class="sxs-lookup"><span data-stu-id="279b9-191">The model descriptor file is the XML file manifest of your model.</span></span> <span data-ttu-id="279b9-192">これは、モデルが属するパッケージの**記述子**フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="279b9-192">It's located in the **Descriptor** folder of the package that the model belongs to.</span></span> <span data-ttu-id="279b9-193">次の図は、フリート管理モデルのモデル記述子ファイルが存在する場所の例を示しています (c:\\packages\\FleetManagement\\Descriptor\\FleetManagement.xml)。</span><span class="sxs-lookup"><span data-stu-id="279b9-193">The following image shows an example of where the model descriptor file of the Fleet Management model exists (c:\\packages\\FleetManagement\\Descriptor\\FleetManagement.xml).</span></span>

    > [!NOTE]
    > <span data-ttu-id="279b9-194">マシンの構成によっては、モデル ストアが、I:\AosService\PackagesLocalDirectory、c:\AosService\PackagesLocalDirectory、または別のドライブの配下にある場合があります。</span><span class="sxs-lookup"><span data-stu-id="279b9-194">Your model store may be located under I:\AosService\PackagesLocalDirectory or c:\AosService\PackagesLocalDirectory or another drive, depending on your machine configuration.</span></span>

    <span data-ttu-id="279b9-195">[![AddSourceControl\_UsingDevoTools](./media/addsourcecontrol_usingdevotools.png)](./media/addsourcecontrol_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-195">[![AddSourceControl\_UsingDevoTools](./media/addsourcecontrol_usingdevotools.png)](./media/addsourcecontrol_usingdevotools.png)</span></span>

4.  <span data-ttu-id="279b9-196">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-196">Click **Finish**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="279b9-197">ソリューションに 2 つのモデルの要素が含まれていたため、ソース管理に追加のモデル記述子ファイルを追加する必要があります: K:\\AOSService\\PackagesLocalDirectory\\FleetManagementExtension\\Descriptor\\FleetManagementExtension.xml</span><span class="sxs-lookup"><span data-stu-id="279b9-197">Because your solution contained elements from two models, you'll need to add an additional model descriptor file to source control: K:\\AOSService\\PackagesLocalDirectory\\FleetManagementExtension\\Descriptor\\FleetManagementExtension.xml</span></span>

5.  <span data-ttu-id="279b9-198">保留中の品目をチェックインします。</span><span class="sxs-lookup"><span data-stu-id="279b9-198">Check-in your pending items.</span></span> <span data-ttu-id="279b9-199">これで、Azure DevOps の最新のクラウド ベースのソース コントロール システムとその他の多くのアプリケーション ライフ サイクルの機能を使用して、項目のフリート管理アプリケーションの開発の準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="279b9-199">Your item is now ready for development of the fleet management application using a state-of-the-art, cloud-based source control system and many other application lifecycle features of Azure DevOps.</span></span>

### <a name="experiment-with-source-control"></a><span data-ttu-id="279b9-200">ソース管理を試す</span><span class="sxs-lookup"><span data-stu-id="279b9-200">Experiment with source control</span></span>

<span data-ttu-id="279b9-201">このセクションでは、**FMRental** テーブルにマイナーな変更を加え、変更内容をソース コード リポジトリ内の最新バージョンと比較します。</span><span class="sxs-lookup"><span data-stu-id="279b9-201">In this section, you'll make minor changes to the **FMRental** table and compare your changes with the latest version in your source code repository.</span></span>

1.  <span data-ttu-id="279b9-202">**ソリューション エクスプローラー**で、**移行されたフリート管理 &gt; データ モデル &gt; テーブル &gt; FMRental** とクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-202">In **Solution Explorer**, click **Fleet Management Migrated &gt; Data model &gt; Tables &gt; FMRental**.</span></span>
2.  <span data-ttu-id="279b9-203">デザイナーを開けるには、**FMRental** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-203">Double-click **FMRental** to open the designer.</span></span>
3.  <span data-ttu-id="279b9-204">**フィールド** ノードを右クリックし、**新規 &gt; 整数** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-204">Right-click the **Fields** node, and then click **New &gt; Integer**.</span></span> 

    <span data-ttu-id="279b9-205">[![NewInteger\_UsingDevoTools](./media/newinteger_usingdevotools.png)](./media/newinteger_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-205">[![NewInteger\_UsingDevoTools](./media/newinteger_usingdevotools.png)](./media/newinteger_usingdevotools.png)</span></span>

4.  <span data-ttu-id="279b9-206">**メソッド** を右クリックして、新しいメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="279b9-206">Right-click **Methods**, and add a new method.</span></span>
5.  <span data-ttu-id="279b9-207">X++ コード エディターで、新たなメソッドにコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="279b9-207">In the X++ code editor, enter a comment in the new method.</span></span>
6.  <span data-ttu-id="279b9-208">既存メソッドにコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="279b9-208">Enter a comment in any existing method.</span></span>
7.  <span data-ttu-id="279b9-209">**FMRental** を保存します。</span><span class="sxs-lookup"><span data-stu-id="279b9-209">Save the **FMRental**.</span></span>
8.  <span data-ttu-id="279b9-210">**チーム エクスプローラー**で、**FMRental.xml** を右クリックして**最新バージョンと比較**を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-210">In **Team Explorer**, right-click **FMRental.xml**, and select **Compare with Latest Version**.</span></span> 

    <span data-ttu-id="279b9-211">[![CompareVersions\_UsingDevoTools](./media/compareversions_usingdevotools.png)](./media/compareversions_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-211">[![CompareVersions\_UsingDevoTools](./media/compareversions_usingdevotools.png)](./media/compareversions_usingdevotools.png)</span></span>

9.  <span data-ttu-id="279b9-212">**比較 (差異)** ウィンドウの違いを参照してください。</span><span class="sxs-lookup"><span data-stu-id="279b9-212">Browse through the differences in the **comparison (Diff)** window.</span></span>
10. <span data-ttu-id="279b9-213">**ソリューション エクスプローラー**で **FMRental** テーブルを右クリックし、**ソース管理 &gt; 元に戻す &gt; 保留中の変更**を選択して変更を元に戻します。</span><span class="sxs-lookup"><span data-stu-id="279b9-213">In **Solution Explorer**, right-click on the **FMRental** table, and select **Source control &gt; Undo &gt; Pending Changes** to revert your changes.</span></span> 

    <span data-ttu-id="279b9-214">[![Undo\_UsingDevoTools](./media/undo_usingdevotools.png)](./media/undo_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-214">[![Undo\_UsingDevoTools](./media/undo_usingdevotools.png)](./media/undo_usingdevotools.png)</span></span>

11. <span data-ttu-id="279b9-215">次のダイアログで取り消しを確認し、**差異**ウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="279b9-215">Confirm the undo on the next dialog and close the **diff** window.</span></span>

## <a name="scenario-2-synchronize-models-from-source-control"></a><span data-ttu-id="279b9-216">シナリオ 2: ソース管理からモデルを同期する</span><span class="sxs-lookup"><span data-stu-id="279b9-216">Scenario 2: Synchronize models from source control</span></span>
<span data-ttu-id="279b9-217">このセクションでは、Azure DevOps プロジェクトから既存のモデルおよびモデル要素を同期します。</span><span class="sxs-lookup"><span data-stu-id="279b9-217">In this section, you will synchronize existing models and model elements from your Azure DevOps project.</span></span> <span data-ttu-id="279b9-218">これは以下の場合に関連します。1) 以前のバージョンのコードを LCS 経由で移行した。2) 別の開発者が新しいモデルまたは新しいモデル要素をチェックインし、それらを開発環境と同期させたい。</span><span class="sxs-lookup"><span data-stu-id="279b9-218">This is relevant in the following cases: 1) You have migrated your code from a previous version via LCS, or 2) another developer has checked-in a new model or new model elements and you would like to synchronize them to your development environment.</span></span>

1.  <span data-ttu-id="279b9-219">ソース管理エクスプローラーで、メタデータを右クリックして**最新バージョンの取得**を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-219">In Source Control Explorer, right-click on Metadata and select **Get Latest Version**.</span></span> <span data-ttu-id="279b9-220">これにより、ローカル パッケージ フォルダーと最新のコードが同期されます。</span><span class="sxs-lookup"><span data-stu-id="279b9-220">This will synchronize you local packages folder with the latest code.</span></span>
2.  <span data-ttu-id="279b9-221">別の方法として、**詳細**メニューを使用して固有のビルド バージョンまたは変更セットを同期することができます。</span><span class="sxs-lookup"><span data-stu-id="279b9-221">Alternatively you can use the **Advanced** menu to synchronize specific build version or change sets.</span></span>

    ![getlatest](./media/getlatest.png)

3.  <span data-ttu-id="279b9-223">同期が完了し、新しいモデルを環境に同期させる場合は、Visual Studio からメタデータを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="279b9-223">Once synchronization is complete, and if this leads to synchronizing new models to your environment, you need to refresh your metadata from Visual Studio.</span></span>
4.  <span data-ttu-id="279b9-224">**Dynamics 365 &gt; モデル管理 &gt; モデルの更新**の順に移動します</span><span class="sxs-lookup"><span data-stu-id="279b9-224">Go to **Dynamics 365 &gt; Model Management &gt; Refresh models**</span></span>

## <a name="organize-todo-tasks-in-a-project"></a><span data-ttu-id="279b9-225">プロジェクト内の TODO タスクの整理</span><span class="sxs-lookup"><span data-stu-id="279b9-225">Organize TODO tasks in a project</span></span>
<span data-ttu-id="279b9-226">このセクションでは、X++コードに埋め込まれたタスク (TODO コメント) から Visual Studio プロジェクトを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="279b9-226">This section describes how you can create a Visual Studio project out of tasks (TODO comments) embedded in your X++ code.</span></span>

1.  <span data-ttu-id="279b9-227">**ソリューション エクスプローラー**で、**移行されたフリート管理 &gt; コード &gt; クラス &gt; FMDataHelper** をクリックしてから、**FMDataHelper** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-227">In **Solution Explorer**, click **Fleet Management Migrated &gt; Code &gt; Classes &gt; FMDataHelper**, and then double-click **FMDataHelper**.</span></span> <span data-ttu-id="279b9-228">これにより、X++ コード エディターが開きます。</span><span class="sxs-lookup"><span data-stu-id="279b9-228">This will open the X++ code editor.</span></span>
2.  <span data-ttu-id="279b9-229">任意のメソッド内に、TODO コメント (//TODO: my comment) を入力します。</span><span class="sxs-lookup"><span data-stu-id="279b9-229">Enter a TODO comment (//TODO: my comment) inside any method.</span></span> 

    <span data-ttu-id="279b9-230">[![Code\_UsingDevoTools](./media/code_usingdevotools.png)](./media/code_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-230">[![Code\_UsingDevoTools](./media/code_usingdevotools.png)](./media/code_usingdevotools.png)</span></span>

3.  <span data-ttu-id="279b9-231">他のフリート管理のクラスやテーブルを開き、さらに TODO コメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="279b9-231">Open other Fleet Management classes or tables and add more TODO comments.</span></span>
4.  <span data-ttu-id="279b9-232">**FleetManagement Migrated** プロジェクトをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="279b9-232">Rebuild the **FleetManagement Migrated** project.</span></span>
5.  <span data-ttu-id="279b9-233">**表示 &gt; タスク一覧**をクリックし、Visual Studio **タスク一覧**ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="279b9-233">Click **View &gt; Task List**, to open the Visual Studio **Task List** window.</span></span> 

    <span data-ttu-id="279b9-234">[![TaskList\_UsingDevoTools](./media/tasklist_usingdevotools.png)](./media/tasklist_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-234">[![TaskList\_UsingDevoTools](./media/tasklist_usingdevotools.png)](./media/tasklist_usingdevotools.png)</span></span>

6.  <span data-ttu-id="279b9-235">ドロップダウン リストから **コメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-235">Select **Comments** from the drop-down list.</span></span> 

    <span data-ttu-id="279b9-236">[![TaskListComments\_UsingDevoTools](./media/tasklistcomments_usingdevotools.png)](./media/tasklistcomments_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-236">[![TaskListComments\_UsingDevoTools](./media/tasklistcomments_usingdevotools.png)](./media/tasklistcomments_usingdevotools.png)</span></span>

7.  <span data-ttu-id="279b9-237">すべての作業項目を選択して右クリックし、**新しいプロジェクトに追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-237">Select all TODO items, right-click, and select **Add to new project**.</span></span> 

    <span data-ttu-id="279b9-238">[![AddNewProject\_UsingDevoTools](./media/addnewproject_usingdevotools.png)](./media/addnewproject_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-238">[![AddNewProject\_UsingDevoTools](./media/addnewproject_usingdevotools.png)](./media/addnewproject_usingdevotools.png)</span></span>

8.  <span data-ttu-id="279b9-239">これにより、**新規プロジェクト** ダイアログが開き、すべての TODO を含む新しいプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="279b9-239">This will open the **New project** dialog and enable you to create a new project that contains all of your TODOs.</span></span>
9.  <span data-ttu-id="279b9-240">このプロジェクトを作業プロジェクトとして保存し、TODO リストを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="279b9-240">You can save this project as a working project to manage your TODO list.</span></span>
10. <span data-ttu-id="279b9-241">完了したら、**チーム エクスプ ローラー** ですべての保留中の変更を元に戻します。</span><span class="sxs-lookup"><span data-stu-id="279b9-241">When you're finished, undo all of your pending changes in **Team Explorer**.</span></span> 

    <span data-ttu-id="279b9-242">[![UndoAll\_UsingDevoTools](./media/undoall_usingdevotools.png)](./media/undoall_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-242">[![UndoAll\_UsingDevoTools](./media/undoall_usingdevotools.png)](./media/undoall_usingdevotools.png)</span></span>

11. <span data-ttu-id="279b9-243">FleetManagement ソリューションを閉じるには、**ファイル &gt; ソリューションを閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-243">Click **File &gt; Close Solution**, to close the FleetManagement solution.</span></span>

## <a name="use-metadata-search-and-navigation-tools-to-find-elements-and-create-projects"></a><span data-ttu-id="279b9-244">メタデータ検索とナビゲーション ツールを使用して要素を検索し、プロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="279b9-244">Use metadata search and navigation tools to find elements and create projects</span></span>
<span data-ttu-id="279b9-245">このセクションでは、アプリケーション全体でメタデータ ベースの検索を実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="279b9-245">This section demonstrates how you can perform meta-data based searches throughout your application.</span></span>

### <a name="use-the-metadata-search-window"></a><span data-ttu-id="279b9-246">[メタデータ検索] ウィンドウの使用</span><span class="sxs-lookup"><span data-stu-id="279b9-246">Use the Metadata search window</span></span>

1. <span data-ttu-id="279b9-247">**Dynamics 365 &gt; メタデータの検索**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-247">Click **Dynamics 365 &gt; Metadata search**.</span></span>
2. <span data-ttu-id="279b9-248">**メタデータ検索**ウィンドウの**検索**フィールドに、次のテキストを入力して会社間クエリを含むアプリケーション スイート モデルのすべてのテーブル挿入メソッドを検索します。</span><span class="sxs-lookup"><span data-stu-id="279b9-248">In the **Metadata search** window, in the **Search** field, enter the following text to find all of the table insert methods in the Application Suite model that contain a cross-company query.</span></span> <span data-ttu-id="279b9-249">*type:table,method name:insert code:"crosscompany" model:"Application Suite"*</span><span class="sxs-lookup"><span data-stu-id="279b9-249">*type:table,method name:insert code:"crosscompany" model:"Application Suite"*</span></span>
3. <span data-ttu-id="279b9-250">検索が完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="279b9-250">Wait for the search to complete.</span></span> <span data-ttu-id="279b9-251">これにはしばらく時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="279b9-251">It may take a while.</span></span> 

   <span data-ttu-id="279b9-252">[</span><span class="sxs-lookup"><span data-stu-id="279b9-252">[</span></span>![MetadataSearchResults\_UsingDevoTools](./media/metadatasearchresults_usingdevotools.png)<span data-ttu-id="279b9-254">]    (./media/metadatasearchresults_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-254">]    (./media/metadatasearchresults_usingdevotools.png)</span></span>

4. <span data-ttu-id="279b9-255">リスト内の結果をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-255">Double-click a result in the list.</span></span> <span data-ttu-id="279b9-256">コード エディターが開き、検索条件に一致する行にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="279b9-256">The code editor will open and place the cursor at the line that matches your search criteria.</span></span>
5. <span data-ttu-id="279b9-257">Ctrl キーを押しながら複数選択することで結果リストで複数の要素を選択し、右クリックして **新しいプロジェクトに追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-257">Select several elements in the results list by holding down the Ctrl key for multiple selections, right-click, and then select **Add to new project**.</span></span> <span data-ttu-id="279b9-258">これにより、選択した要素を含む新しいソリューションとプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="279b9-258">This will let you to create a new solution and project containing the selected elements.</span></span>

### <a name="try-other-search-examples"></a><span data-ttu-id="279b9-259">他の検索例を試す</span><span class="sxs-lookup"><span data-stu-id="279b9-259">Try other search examples</span></span>

<span data-ttu-id="279b9-260">**Tip**: 検索結果を操作する前に、検索が完了するのを待つ必要はありません。</span><span class="sxs-lookup"><span data-stu-id="279b9-260">**Tip**: You don't need to wait for the search to complete before you interact with search results.</span></span> <span data-ttu-id="279b9-261">いつでも結果をダブルクリックして、検索条件に一致するメタデータまたはソース コードを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="279b9-261">You can double-click results at any time to view the metadata or source code that matches your search criteria.</span></span> <span data-ttu-id="279b9-262">推奨される検索例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="279b9-262">The following are some suggested search examples:</span></span>

-   <span data-ttu-id="279b9-263">モデル アプリケーション スイートのビュー モードおよび自動幅モードで定義された、垂直タブのコントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="279b9-263">Find vertical tab controls defined in view mode and auto-width mode in the model Application Suite.</span></span> <span data-ttu-id="279b9-264">*type:form,formtabcontrol property:arrangeMethod=Vertical,ViewEditMode=view,WidthMode=Auto model:"Application Suite"*</span><span class="sxs-lookup"><span data-stu-id="279b9-264">*type:form,formtabcontrol property:arrangeMethod=Vertical,ViewEditMode=view,WidthMode=Auto model:"Application Suite"*</span></span>
-   <span data-ttu-id="279b9-265">プロパティ heightmode = 列で、編集できないフォームですべてのグリッド コントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="279b9-265">Find all grid controls in forms that aren't editable and with the property heightmode = column.</span></span> <span data-ttu-id="279b9-266">*type:form,formgridcontrol:allowedit=no,heightmode=column*</span><span class="sxs-lookup"><span data-stu-id="279b9-266">*type:form,formgridcontrol:allowedit=no,heightmode=column*</span></span>
-   <span data-ttu-id="279b9-267">アプリケーション スイート モデル内のすべての SimpleListDetail フォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="279b9-267">Find all SimpleListDetail forms in the Application Suite model.</span></span> <span data-ttu-id="279b9-268">*type:formdesign property:style=simplelistdetail model:"Applicaiton Suite"*</span><span class="sxs-lookup"><span data-stu-id="279b9-268">*type:formdesign property:style=simplelistdetail model:"Applicaiton Suite"*</span></span>
-   <span data-ttu-id="279b9-269">キーワード xpNum を含むインデックス フィールド名を持つすべてのテーブルを検索します。</span><span class="sxs-lookup"><span data-stu-id="279b9-269">Find all tables that have an index field name that contains the keyword xpNum.</span></span> <span data-ttu-id="279b9-270">*type:table,tableindexfield anem: xpNum*</span><span class="sxs-lookup"><span data-stu-id="279b9-270">*type:table,tableindexfield anem: xpNum*</span></span>
-   <span data-ttu-id="279b9-271">以前の検索条件にアクセスするには、検索バーのドロップダウン メニューを使用します。</span><span class="sxs-lookup"><span data-stu-id="279b9-271">Use the search bar drop-down menu to access previous searches.</span></span> 

    <span data-ttu-id="279b9-272">[![AccessPrevious\_UsingDevoTools](./media/accessprevious_usingdevotools.png)](./media/accessprevious_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-272">[![AccessPrevious\_UsingDevoTools](./media/accessprevious_usingdevotools.png)](./media/accessprevious_usingdevotools.png)</span></span>

## <a name="navigate-to-related-elements"></a><span data-ttu-id="279b9-273">関連する要素への移動</span><span class="sxs-lookup"><span data-stu-id="279b9-273">Navigate to related elements</span></span>
<span data-ttu-id="279b9-274">このセクションでは、**アプリケーション エクスプローラー**または**ソリューション エクスプローラー**で関連要素を見つけることなく、ある要素から関連要素に移動する機能を紹介します。</span><span class="sxs-lookup"><span data-stu-id="279b9-274">This section highlights a feature that enables you to move from one element to a related element without having to find the related elements in **Application Explorer** or **Solution Explorer**.</span></span>

1.  <span data-ttu-id="279b9-275">**アプリケーション エクスプローラー**を開き、**モデル ビュー**に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="279b9-275">Open **Application Explorer**, and switch the view to **Model View**.</span></span> 

    <span data-ttu-id="279b9-276">[![ModelView\_UsingDevoTool](./media/modelview_usingdevotool1.png)](./media/modelview_usingdevotool1.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-276">[![ModelView\_UsingDevoTool](./media/modelview_usingdevotool1.png)](./media/modelview_usingdevotool1.png)</span></span>

2.  <span data-ttu-id="279b9-277">**フリート管理** モデルで、**ユーザー インターフェイス&gt;メニュー項目&gt;メニュー項目を表示&gt;FMCustomer** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-277">Under the **Fleet Management** model, click **User Interface &gt; Menu items &gt; Display Menu Items &gt; FMCustomer**.</span></span> 

    <span data-ttu-id="279b9-278">[![FMCustomerISV\_UsingDevoTools](./media/fmcustomerisv_usingdevotools.png)](./media/fmcustomerisv_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-278">[![FMCustomerISV\_UsingDevoTools](./media/fmcustomerisv_usingdevotools.png)](./media/fmcustomerisv_usingdevotools.png)</span></span>

3.  <span data-ttu-id="279b9-279">**FMCustomer** を右クリックし、**デザイナーを開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-279">Right-click **FMCustomer**, and then select **Open designer**.</span></span>
4.  <span data-ttu-id="279b9-280">**FMCustomer** メニュー項目デザイナーでルート ノードを右クリックし、**フォーム FMCustomer に移動する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-280">In the **FMCustomer** menu item designer, right-click the root node, and then select **Go to Form FMCustomer**.</span></span> 

    <span data-ttu-id="279b9-281">[![GoFormFMCustomer\_UsingDevoTools](./media/goformfmcustomer_usingdevotools.png)](./media/goformfmcustomer_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-281">[![GoFormFMCustomer\_UsingDevoTools](./media/goformfmcustomer_usingdevotools.png)](./media/goformfmcustomer_usingdevotools.png)</span></span> 

    <span data-ttu-id="279b9-282">**FMCustomer** フォーム デザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="279b9-282">The **FMCustomer** form designer will open.</span></span>
5.  <span data-ttu-id="279b9-283">**FMCustomer** フォームのデザイナーで、**データ ソース**を展開して、**FMCustomer** を右クリックしてから**テーブル FMCustomer へ移動**を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-283">In the designer of the **FMCustomer** form, expand **Data sources**, right-click **FMCustomer**, and then select **Go to Table FMCustomer**</span></span> 

    <span data-ttu-id="279b9-284">[![GoTableFMCustomer\_UsingDevoTools](./media/gotablefmcustomer_usingdevotools.png)](./media/gotablefmcustomer_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="279b9-284">[![GoTableFMCustomer\_UsingDevoTools](./media/gotablefmcustomer_usingdevotools.png)](./media/gotablefmcustomer_usingdevotools.png)</span></span>

    <span data-ttu-id="279b9-285">**FMCustomer** テーブル デザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="279b9-285">The **FMCustomer** table designer will open.</span></span>
6.  <span data-ttu-id="279b9-286">同じ方法を使用すると、テーブル フィールドが参照する EDT 要素に移動できます。</span><span class="sxs-lookup"><span data-stu-id="279b9-286">Using the same methodology, you can navigate to the EDT element that a table field references.</span></span> <span data-ttu-id="279b9-287">**ヒント**: コンテキスト メニューを開くのではなく F9 キーを押します。</span><span class="sxs-lookup"><span data-stu-id="279b9-287">**Tip**: Press F9 instead of opening the context menu.</span></span> <span data-ttu-id="279b9-288">F9 キーを押すと、参照要素のデザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="279b9-288">F9 will open the designer of the referenced element.</span></span> <span data-ttu-id="279b9-289">**ヒント**: 現在のプロジェクトに要素を追加するには、ドキュメント タブを右クリックし、**プロジェクトへの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-289">**Tip**: You can add an element to the current project by right-clicking on the document tab and selecting **Add to project**.</span></span>

![Addtoproject\_UsingDevoTools](./media/addtoproject_usingdevotools.png)

<a name="use-application-explorer-to-create-a-project-from-a-model"></a><span data-ttu-id="279b9-291">アプリケーション エクスプローラーを使用してモデルからプロジェクトを作成</span><span class="sxs-lookup"><span data-stu-id="279b9-291">Use Application Explorer to create a project from a model</span></span>
---------------------------------------------------------

<span data-ttu-id="279b9-292">アプリケーション エクスプ ローラーを使用して、モデルのすべてまたは一部の要素を検索し、検索結果からプロジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="279b9-292">You can use Application Explorer to search for all or some elements of a model and create a project out of the search results.</span></span>

1.  <span data-ttu-id="279b9-293">要素のタイプでプロジェクトを整理するためのオプションがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="279b9-293">Make sure the option to organize a project by element type is on.</span></span> <span data-ttu-id="279b9-294">**Dynamics 365** &gt; **オプション** &gt; **プロジェクト**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="279b9-294">Go to **Dynamics 365** &gt; **Options** &gt; **Projects**.</span></span>
2.  <span data-ttu-id="279b9-295">アプリケーション エクスプローラーに移動し、目的のモデル内の要素を検索します。</span><span class="sxs-lookup"><span data-stu-id="279b9-295">Go to Application Explorer and search for elements in the desired model.</span></span> <span data-ttu-id="279b9-296">たとえば、*モデル:「フリート管理」*を入力し、**入力**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="279b9-296">For example, enter\* model:"fleet management"\* and click **Enter**.</span></span>

    <span data-ttu-id="279b9-297">[![AppExplorerModelSearch](./media/appexplorermodelsearch.jpg)](./media/appexplorermodelsearch.jpg)</span><span class="sxs-lookup"><span data-stu-id="279b9-297">[![AppExplorerModelSearch](./media/appexplorermodelsearch.jpg)](./media/appexplorermodelsearch.jpg)</span></span>

3.  <span data-ttu-id="279b9-298">検索が完了したら、AOT ルート ノードを右クリックし、\*検索結果を新規プロジェクトに追加しますを選択します。</span><span class="sxs-lookup"><span data-stu-id="279b9-298">When the search is complete, right-click the AOT root node and select \*Add search results to new project.</span></span>

    <span data-ttu-id="279b9-299">[![AddSearchResultsToNewProject](./media/addsearchresultstonewproject.jpg)](./media/addsearchresultstonewproject.jpg)\*</span><span class="sxs-lookup"><span data-stu-id="279b9-299">[![AddSearchResultsToNewProject](./media/addsearchresultstonewproject.jpg)](./media/addsearchresultstonewproject.jpg)\*</span></span>

4.  <span data-ttu-id="279b9-300">新しいプロジェクト ダイアログ ボックスでプロジェクトのプロパティを指定し、**OK** をクリックしてプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="279b9-300">Specify your project properties in the new project dialog and click **OK** to create the project.</span></span>

<span data-ttu-id="279b9-301">**ヒント:** 検索結果からプロジェクトを作成するには、すべての結果が同じモデル内にある限り、任意のタイプ、名前、またはその他のフィルタを検索に追加できます。</span><span class="sxs-lookup"><span data-stu-id="279b9-301">**Tip:** To create a project from search results, you can add any type, name, or other filters to your search as long as all results are in the same model.</span></span> <span data-ttu-id="279b9-302">例: *モデル:「フリート管理」 タイプ:テーブル名:^FM* は、文字 FM で始まる名前を持つフリート管理モデルで、すべてのテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="279b9-302">For example: *model:"Fleet Management" type:Table name:^FM* will return all tables in the Fleet Management model with a name starting with the letters FM.</span></span>



