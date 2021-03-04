---
title: バージョン コントロール、メタデータ検索、およびナビゲーション
description: このチュートリアルでは、Azure DevOps をコンフィギュレーションして、モデルのソース管理を有効にします。
author: RobinARH
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 23401
ms.assetid: 46ed0115-6f8b-4757-b8d2-d4ccb76c733d
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39c4949a920bf373d70c9e38ea5558a6d4f0a36c
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093590"
---
# <a name="version-control-metadata-search-and-navigation"></a><span data-ttu-id="0d844-103">バージョン コントロール、メタデータ検索、およびナビゲーション</span><span class="sxs-lookup"><span data-stu-id="0d844-103">Version control, metadata search, and navigation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d844-104">このチュートリアルでは、Microsoft Azure DevOps をコンフィギュレーションして、モデルのソース管理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="0d844-104">This tutorial will walk you through configuring Microsoft Azure DevOps to enable source control on your models.</span></span> <span data-ttu-id="0d844-105">これは、TODO タスクの作成および整理、メタデータおよびソース コードの検索、関連するモデル要素間の移動、モデルからのプロジェクトの作成を行う機能など、開発ツールでのその他の生産性機能について把握することにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0d844-105">It will also help you learn about other productivity features in the development tools, including the ability to create and organize TODO task, search metadata and source code, navigate between related model elements, and create a project from a model.</span></span>

## <a name="configure-your-azure-devops-organization-and-project"></a><span data-ttu-id="0d844-106">Azure DevOps 組織およびプロジェクトをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="0d844-106">Configure your Azure DevOps organization and project</span></span>

<span data-ttu-id="0d844-107">このセクションでは、Azure DevOps で新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="0d844-107">In this section, you'll create a new project in Azure DevOps.</span></span> <span data-ttu-id="0d844-108">このプロジェクトはモデルのソース コードをホストします。</span><span class="sxs-lookup"><span data-stu-id="0d844-108">This project will host the source code of your model.</span></span> <span data-ttu-id="0d844-109">例として、フリート管理モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d844-109">You'll use the Fleet Management model as an example.</span></span> <span data-ttu-id="0d844-110">Azure DevOps 組織をお持ちでない場合は、作成します。</span><span class="sxs-lookup"><span data-stu-id="0d844-110">If you don't have a Azure DevOps organization, you'll create one.</span></span>

### <a name="sign-up-to-azure-devops-create-an-account-and-create-a-new-project"></a><span data-ttu-id="0d844-111">Azure DevOps への登録、アカウントの作成、および新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="0d844-111">Sign up to Azure DevOps, create an account, and create a new project</span></span>

<span data-ttu-id="0d844-112"><https://www.visualstudio.com/> に移動して Azure DevOps にサインアップします。</span><span class="sxs-lookup"><span data-stu-id="0d844-112">Navigate to <https://www.visualstudio.com/> to sign up for Azure DevOps.</span></span> <span data-ttu-id="0d844-113">**サインアップ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-113">Click **Sign up**.</span></span> <span data-ttu-id="0d844-114">Azure DevOps アカウントを既に持っている場合は、このトピックの後半の「Azure DevOps プロジェクトの作成」セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="0d844-114">If you already have an account in Azure DevOps, go to the Create a Azure DevOps project section later in this topic.</span></span>

1. <span data-ttu-id="0d844-115">Microsoft アカウントでサインインします。</span><span class="sxs-lookup"><span data-stu-id="0d844-115">Sign in with your Microsoft account.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d844-116">組織のアカウント (Microsoft 365 ドメイン) を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="0d844-116">You can also use an organizational account (Microsoft 365 domain).</span></span>

2. <span data-ttu-id="0d844-117">Azure DevOps 組織を作成し、アカウントの URL を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-117">Create a Azure DevOps organization, and select a URL for your account.</span></span> <span data-ttu-id="0d844-118">Visual Studio でソース管理を設定するときに、開発用コンピューターから接続する URL を使用します。</span><span class="sxs-lookup"><span data-stu-id="0d844-118">You'll use this URL to connect from your development computer when you're configuring source control in Visual Studio.</span></span> <span data-ttu-id="0d844-119">次の図は、アカウント URL の例です。</span><span class="sxs-lookup"><span data-stu-id="0d844-119">The following image is an example of the account URL.</span></span>

    ![アカウントの URL を選択する](./media/accounturl_usingdevotools.png)

    <span data-ttu-id="0d844-121">アカウントが作成されると、アカウントのメイン ページに進むように指示され、そこで最初のプロジェクトの作成を求められます。</span><span class="sxs-lookup"><span data-stu-id="0d844-121">When the account is created, you're directed to your account main page where you're prompted to create your first project.</span></span>
3. <span data-ttu-id="0d844-122">デモ **フリート管理** プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="0d844-122">Create a demo **Fleet Management** project.</span></span>

    ![最初のプロジェクトを作成する](./media/firstproject_usingdevotools.png)

### <a name="create-a-azure-devops-team-project"></a><span data-ttu-id="0d844-124">Azure DevOps チーム プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="0d844-124">Create a Azure DevOps team project</span></span>

<span data-ttu-id="0d844-125">Azure DevOps 組織を既に持っている場合は、Internet Explorer を使用してアカウントに移動します。</span><span class="sxs-lookup"><span data-stu-id="0d844-125">If you already have a Azure DevOps organization, go to your account using Internet Explorer.</span></span> <span data-ttu-id="0d844-126">このトピックでは、説明のために URL の例として **.visualstudio.com** を使用します。</span><span class="sxs-lookup"><span data-stu-id="0d844-126">This topic uses **.visualstudio.com** as the example URL for illustration purposes.</span></span>

1. <span data-ttu-id="0d844-127"><https://www.visualstudio.com/> に移動します。</span><span class="sxs-lookup"><span data-stu-id="0d844-127">Go to <https://www.visualstudio.com/>.</span></span>
2. <span data-ttu-id="0d844-128">**最近使用したプロジェクトとチーム** で **新規** をクリックして新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="0d844-128">Under **Recent projects & teams**, click **New** to create a new project.</span></span>

   ![新しいプロジェクトの作成](./media/clicknew_usingdevotools.png)

3. <span data-ttu-id="0d844-130">**プロジェクト名** フィールドに、**フリート管理** と入力し、**説明** を入力してから **プロジェクトの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-130">In the **Project name** field, enter **Fleet Management**, enter a **Description**, and then click **Create project**.</span></span>

### <a name="create-the-recommended-folder-structure-in-your-team-project"></a><span data-ttu-id="0d844-131">チーム プロジェクトで推奨するフォルダー構造を作成する</span><span class="sxs-lookup"><span data-stu-id="0d844-131">Create the recommended folder structure in your team project</span></span>

<span data-ttu-id="0d844-132">Lifecycle Services (LCS) 自動化コードのアップグレード ツールを使用して以前のバージョンからコードを移行した場合、以下のフォルダ構造は、Azure DevOps チーム プロジェクトで自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="0d844-132">If you have migrated your code from a previous version using the Lifecycle Services (LCS) automated code upgrade tool, the following folder structure is automatically created in your Azure DevOps team project.</span></span>

![既定のフォルダー構造](./media/vsofolders1.png)

<span data-ttu-id="0d844-134">**メタデータ** フォルダーには、パッケージとモデルによって整理されたソース XML ファイルがあり、**プロジェクト** フォルダーには Visual Studio プロジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0d844-134">The **Metadata** folder contains your source XML files organized by packages and models and the **Projects** folder contains Visual Studio projects.</span></span> <span data-ttu-id="0d844-135">コードを移行せず、最初から開始している場合、開発を開始する前に、チーム プロジェクト内のサーバーに類似したフォルダ構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="0d844-135">If you are not migrating code and are starting from scratch, create a similar folder structure on the server in your team project before you start development.</span></span>

### <a name="configure-visual-studio-to-connect-to-your-team-project"></a><span data-ttu-id="0d844-136">Visual Studio をコンフィギュレーションしてチーム プロジェクトに接続する</span><span class="sxs-lookup"><span data-stu-id="0d844-136">Configure Visual Studio to connect to your team project</span></span>

1. <span data-ttu-id="0d844-137">Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="0d844-137">Start Visual Studio.</span></span> <span data-ttu-id="0d844-138">マシンに管理者としてログインしている場合は、Visual Studio を管理者として起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d844-138">If you are logged into the machine as an administrator, then you must start Visual Studio as an administrator.</span></span>
2. <span data-ttu-id="0d844-139">**ツール &gt; オプション &gt; ソース管理 &gt; プラグインの選択** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-139">Click **Tools &gt; Options &gt; Source Control &gt; Plug-in Selection**.</span></span>
3. <span data-ttu-id="0d844-140">現在のソース管理プラグイン フィールドで **Visual Studio Team Foundation Server** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-140">In the Current source control plug-in field, select **Visual Studio Team Foundation Server**.</span></span>
4. <span data-ttu-id="0d844-141">**チーム &gt; Team Foundation Server に接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-141">Select **Team &gt; Connect to Team Foundation Server**.</span></span>
5. <span data-ttu-id="0d844-142">**チーム エクスプローラー** で、**チーム プロジェクトの選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-142">In **Team Explorer**, click **Select Team Projects**.</span></span>
6. <span data-ttu-id="0d844-143">**Team Foundation Server の選択** ドロップダウン リストで、フリート管理プロジェクトをホストする **Azure DevOps 組織** を選択するか、メニューにない場合は **サーバー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-143">In the **Select a Team Foundation Server** drop-down list, select the **Azure DevOps organization** that hosts the Fleet Management project, or click **Servers** if it isn't in the menu.</span></span>
    1. <span data-ttu-id="0d844-144">**Team Foundation Server の追加および削除** ダイアログ ボックスが開いたとき、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-144">When the **Add/Remove Team Foundation Server** dialog opens, click **Add**.</span></span>
    2. <span data-ttu-id="0d844-145">Azure DevOps 組織の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d844-145">Enter the URL of your Azure DevOps organization.</span></span>
    3. <span data-ttu-id="0d844-146">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-146">Click **OK**.</span></span>
    4. <span data-ttu-id="0d844-147">メッセージが表示されたら、Microsoft アカウントのユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="0d844-147">If prompted, enter your Microsoft Account username and password.</span></span>

7. <span data-ttu-id="0d844-148">**チーム プロジェクト** で **フリート管理** チェック ボックスをオンにし、**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-148">Select the **Fleet Management** check box under **Team projects**, and then click **Connect**.</span></span>

    ![Team Foundation Serverに 接続する](./media/connecttfsserver_usingdevotools.png)

### <a name="map-your-azure-devops-project-to-your-local-model-store-and-projects-folder"></a><span data-ttu-id="0d844-150">Azure DevOps プロジェクトをローカルのモデル ストアとプロジェクト フォルダーにマップ</span><span class="sxs-lookup"><span data-stu-id="0d844-150">Map your Azure DevOps project to your local model store and projects folder</span></span>

<span data-ttu-id="0d844-151">モデル ストアのルート フォルダーには、アプリケーションの一部であるすべてのパッケージとモデルのソース ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0d844-151">Your model store root folder contains source files of all packages and models that are part of your application.</span></span> <span data-ttu-id="0d844-152">展開中には、複数のパッケージにまたがる複数のモデルのソース ファイルを使用するでしょう。</span><span class="sxs-lookup"><span data-stu-id="0d844-152">During deployment, you'll probably use source files from more than one model across more than one package.</span></span> <span data-ttu-id="0d844-153">モデル ストアのルート フォルダーを Azure DevOps のチーム プロジェクト メタデータ フォルダーにマップすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0d844-153">We recommend that you map your model store root folder to the Azure DevOps team project metadata folder.</span></span>

1. <span data-ttu-id="0d844-154">Visual studio の **チーム エクスプローラー** で、このドキュメントで前に説明したようにチーム プロジェクトに接続します。</span><span class="sxs-lookup"><span data-stu-id="0d844-154">In Visual studio **Team Explorer**, connect to the team project as described earlier in this document.</span></span>
2. <span data-ttu-id="0d844-155">**ソース管理エクスプローラー** から **チーム エクスプローラー** を開きます。</span><span class="sxs-lookup"><span data-stu-id="0d844-155">Open **Source Control Explorer** from **Team Explorer**.</span></span>
3. <span data-ttu-id="0d844-156">チーム プロジェクトの **メタデータ** フォルダーを、ローカル ドライブのモデル ストアのルート フォルダー (通常は K:\\AOSService\\PackagesLocalDirectory) にマップします。例を以下の図に示します。</span><span class="sxs-lookup"><span data-stu-id="0d844-156">Map the **Metadata** folder of your team project to the root folder of the model store on your local drive (Typically K:\\AOSService\\PackagesLocalDirectory), an example is shown in the image below.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d844-157">マシンの構成によっては、モデル ストアが I:\\AosService\\PackagesLocalDirectory または別のドライブの配下にある場合があります。</span><span class="sxs-lookup"><span data-stu-id="0d844-157">Your model store may be located under I:\\AosService\\PackagesLocalDirectory or another drive, depending on your machine configuration.</span></span>

    ![ワークスペース マッピングの作成](./media/vsofolders21.png)

4. <span data-ttu-id="0d844-159">**マップ** をクリックし、次のダイアログ ボックスで、**No** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-159">Click **Map**, and on the next dialog, click **No**.</span></span>
5. <span data-ttu-id="0d844-160">同様に、**/Trunk/Main/Projects** サーバー フォルダーを、Visual Studio ソリューションとプロジェクト ファイルを保持する **ローカル プロジェクト フォルダー** にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="0d844-160">Similarly, map the **/Trunk/Main/Projects** server folder to the **local projects folder** that will hold your Visual Studio solution and project files.</span></span>

## <a name="scenario-1-open-the-fleet-management-solution-and-add-it-to-azure-devops-source-control"></a><span data-ttu-id="0d844-161">シナリオ 1: フリート管理ソリューションを開き、Azure DevOps ソース管理に追加する</span><span class="sxs-lookup"><span data-stu-id="0d844-161">Scenario 1: Open the fleet management solution and add it to Azure DevOps source control</span></span>

<span data-ttu-id="0d844-162">このセクションでは、Azure DevOps のソース管理にソリューションを追加するために必要なステップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0d844-162">This section describes the steps needed to add a solution to Azure DevOps source control.</span></span> <span data-ttu-id="0d844-163">このシナリオは、新しいモデルで開発を開始し、初めてソース管理に追加する場合に関係します。</span><span class="sxs-lookup"><span data-stu-id="0d844-163">This scenario is relevant when you have started development on a new model and you are adding it to source control for the first time.</span></span> <span data-ttu-id="0d844-164">コード移行シナリオまたは他の開発者により作成された新しいモデルを同期する場合は、以下のシナリオ 2 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d844-164">For code migration scenarios or in the case you are synchronizing new models that have been created by another developer, refer to scenario 2 below.</span></span>

### <a name="open-the-fleetmanagement-solution"></a><span data-ttu-id="0d844-165">FleetManagement ソリューションを開く</span><span class="sxs-lookup"><span data-stu-id="0d844-165">Open the FleetManagement solution</span></span>

> [!NOTE]
> <span data-ttu-id="0d844-166">このプロジェクトは単なる一例です。</span><span class="sxs-lookup"><span data-stu-id="0d844-166">This project is only an example.</span></span> <span data-ttu-id="0d844-167">任意のプロジェクト/ソリューションを開いて、ソリューションをソース管理に追加するプロセスについて学習することができます。</span><span class="sxs-lookup"><span data-stu-id="0d844-167">You can open any project/solution to learn about the process of adding a solution to source control.</span></span>

1. <span data-ttu-id="0d844-168">**ファイル** メニューで、**開く** をポイントし、**プロジェクト/ソリューション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-168">On the **File** menu, point to **Open**, and then click **Project/Solution**.</span></span>
2. <span data-ttu-id="0d844-169">デスクトップを参照し、**FleetManagement** フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="0d844-169">Browse to the desktop and open the **FleetManagement** folder.</span></span>
3. <span data-ttu-id="0d844-170">**FleetManagement** という名前のソリューション ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-170">Select the solution file named **FleetManagement**.</span></span> <span data-ttu-id="0d844-171">表示されるファイル タイプは Microsoft Visual Studio Solution です。</span><span class="sxs-lookup"><span data-stu-id="0d844-171">The file type listed is Microsoft Visual Studio Solution.</span></span> <span data-ttu-id="0d844-172">ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。</span><span class="sxs-lookup"><span data-stu-id="0d844-172">If the solution file is not on your computer, the steps to create it are listed in [Tutorial: Create a Fleet Management solution file out of the Fleet Management models in the AOT](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot).</span></span>
4. <span data-ttu-id="0d844-173">**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-173">Click **Open**.</span></span> <span data-ttu-id="0d844-174">ソリューションの読み込みには時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0d844-174">Loading the solution may take some time.</span></span>

### <a name="add-the-fleetmanagement-solution-to-source-control"></a><span data-ttu-id="0d844-175">ソース コントロールへの FleetManagement ソリューションの追加</span><span class="sxs-lookup"><span data-stu-id="0d844-175">Add the FleetManagement solution to source control</span></span>

1. <span data-ttu-id="0d844-176">**ソリューション エクスプローラー** で、フリート管理ソリューションを右クリックして、**ソリューションをソース管理に追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-176">In **Solution Explorer**, right-click the Fleet Management solution, and select **Add Solution to Source Control.**</span></span>
2. <span data-ttu-id="0d844-177">次のダイアログで、**Team Foundation バージョン管理** を選択し、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-177">On the next dialog, select **Team Foundation Version Control**, and then click **Next**.</span></span>
3. <span data-ttu-id="0d844-178">**チーム プロジェクト ロケーション** にて、以下画像のように **プロジェクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-178">In the **Team Project Location**, select **Projects**, as shown in this image.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d844-179">サーバープロジェクト フォルダ を FleetManagement ソリューションを含むローカルフォルダに既にマッピングしている場合は、手順2 と 3 を省略します。</span><span class="sxs-lookup"><span data-stu-id="0d844-179">If you have already mapped the server Projects folder to a local folder that contains the FleetManagement solution, steps 2 and 3 are omitted.</span></span>

    ![Team Foundation Server のフォルダー構造](./media/vsofolders31.png)

4. <span data-ttu-id="0d844-181">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-181">Click OK.</span></span>
5. <span data-ttu-id="0d844-182">**チーム エクスプ ローラー &gt; 保留中の変更** に移動し、**チェックイン** をクリックして、ソリューションおよびモデル要素が Azure DevOps ソース管理にチェックインするようにします。</span><span class="sxs-lookup"><span data-stu-id="0d844-182">Go to **Team Explorer &gt; Pending changes**, and then click **Check-in** to check-in your solution and its model element to the Azure DevOps source control.</span></span>

### <a name="add-the-model-descriptor-file-to-source-control"></a><span data-ttu-id="0d844-183">ソース コントロールへのモデル記述子ファイルの追加</span><span class="sxs-lookup"><span data-stu-id="0d844-183">Add the model descriptor file to source control</span></span>

<span data-ttu-id="0d844-184">すべての Visual Studio プロジェクトはモデルに属しています。</span><span class="sxs-lookup"><span data-stu-id="0d844-184">All Visual Studio projects belong to models.</span></span> <span data-ttu-id="0d844-185">モデルは、通常 Visual Studio プロジェクトよりも大きなスコープ内にあるソース コードの配布と配置の単位です。</span><span class="sxs-lookup"><span data-stu-id="0d844-185">Models are source code distribution and deployment units that are typically larger in scope than a Visual Studio project.</span></span> <span data-ttu-id="0d844-186">前のセクションでは、ソース管理にフリート管理ソリューションの要素のファイルを追加しました。</span><span class="sxs-lookup"><span data-stu-id="0d844-186">In the previous section, you added element files of the fleet management solution to source control.</span></span> <span data-ttu-id="0d844-187">フリート管理モデルの要素をソース管理に追加したのは初めてのため、モデル記述子ファイルをチェックインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d844-187">Because this was the first time that you added elements of the Fleet Management models to source control, you'll also need to check-in the model descriptor file.</span></span>

1. <span data-ttu-id="0d844-188">Visual Studio の **チーム エクスプローラー** で、**ソース管理エクスプローラー** を開いてから、メタデータ フォルダー (たとえば、**\Trunk\Main\Metadata**) を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-188">In Visual Studio, in **Team Explorer**, open **Source Control Explorer**, and then right-click on the metadata folder (for example, **\Trunk\Main\Metadata**).</span></span>
2. <span data-ttu-id="0d844-189">**ソース管理エクスプローラー** ツール バーで、**フォルダーへの項目の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-189">In the **Source Control Explorer** toolbar, click **Add Item to Folder**.</span></span>
3. <span data-ttu-id="0d844-190">モデル記述子ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-190">Select your model descriptor file.</span></span> <span data-ttu-id="0d844-191">モデル記述子ファイルは、モデルの XML ファイルのマニフェストです。</span><span class="sxs-lookup"><span data-stu-id="0d844-191">The model descriptor file is the XML file manifest of your model.</span></span> <span data-ttu-id="0d844-192">これは、モデルが属するパッケージの **記述子** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0d844-192">It's located in the **Descriptor** folder of the package that the model belongs to.</span></span> <span data-ttu-id="0d844-193">次の図は、フリート管理モデルのモデル記述子ファイルが存在する場所の例を示しています (c:\\packages\\FleetManagement\\Descriptor\\FleetManagement.xml)。</span><span class="sxs-lookup"><span data-stu-id="0d844-193">The following image shows an example of where the model descriptor file of the Fleet Management model exists (c:\\packages\\FleetManagement\\Descriptor\\FleetManagement.xml).</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d844-194">マシンの構成によっては、モデル ストアが、I:\AosService\PackagesLocalDirectory、c:\AosService\PackagesLocalDirectory、または別のドライブの配下にある場合があります。</span><span class="sxs-lookup"><span data-stu-id="0d844-194">Your model store may be located under I:\AosService\PackagesLocalDirectory or c:\AosService\PackagesLocalDirectory or another drive, depending on your machine configuration.</span></span>

    <span data-ttu-id="0d844-195">[![ソース コントロールへの FleetManagement.xml の追加](./media/addsourcecontrol_usingdevotools.png)](./media/addsourcecontrol_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-195">[![Adding FleetManagement.xml to source control](./media/addsourcecontrol_usingdevotools.png)](./media/addsourcecontrol_usingdevotools.png)</span></span>

4. <span data-ttu-id="0d844-196">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-196">Click **Finish**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d844-197">ソリューションに 2 つのモデルの要素が含まれていたため、ソース管理に追加のモデル記述子ファイルを追加する必要があります: K:\\AOSService\\PackagesLocalDirectory\\FleetManagementExtension\\Descriptor\\FleetManagementExtension.xml</span><span class="sxs-lookup"><span data-stu-id="0d844-197">Because your solution contained elements from two models, you'll need to add an additional model descriptor file to source control: K:\\AOSService\\PackagesLocalDirectory\\FleetManagementExtension\\Descriptor\\FleetManagementExtension.xml</span></span>

5. <span data-ttu-id="0d844-198">保留中の品目をチェックインします。</span><span class="sxs-lookup"><span data-stu-id="0d844-198">Check-in your pending items.</span></span> <span data-ttu-id="0d844-199">これで、Azure DevOps の最新のクラウド ベースのソース コントロール システムとその他の多くのアプリケーション ライフ サイクルの機能を使用して、品目のフリート管理アプリケーションの開発をする準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="0d844-199">Your item is now ready for development of the fleet management application using a state-of-the-art, cloud-based source control system, and many other application lifecycle features of Azure DevOps.</span></span>

### <a name="experiment-with-source-control"></a><span data-ttu-id="0d844-200">ソース管理を試す</span><span class="sxs-lookup"><span data-stu-id="0d844-200">Experiment with source control</span></span>

<span data-ttu-id="0d844-201">このセクションでは、**FMRental** テーブルにマイナーな変更を加え、変更内容をソース コード リポジトリ内の最新バージョンと比較します。</span><span class="sxs-lookup"><span data-stu-id="0d844-201">In this section, you'll make minor changes to the **FMRental** table and compare your changes with the latest version in your source code repository.</span></span>

1. <span data-ttu-id="0d844-202">**ソリューション エクスプローラー** で、**移行されたフリート管理 &gt; データ モデル &gt; テーブル &gt; FMRental** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-202">In **Solution Explorer**, select **Fleet Management Migrated &gt; Data model &gt; Tables &gt; FMRental**.</span></span>
2. <span data-ttu-id="0d844-203">デザイナーを開けるには、**FMRental** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-203">Double-click **FMRental** to open the designer.</span></span>
3. <span data-ttu-id="0d844-204">**フィールド** ノードを右クリックし、**新規 &gt; 整数** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-204">Right-click the **Fields** node, and then click **New &gt; Integer**.</span></span>

    <span data-ttu-id="0d844-205">[![新しい整数の追加](./media/newinteger_usingdevotools.png)](./media/newinteger_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-205">[![Add new integer](./media/newinteger_usingdevotools.png)](./media/newinteger_usingdevotools.png)</span></span>

4. <span data-ttu-id="0d844-206">**メソッド** を右クリックして、新しいメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="0d844-206">Right-click **Methods**, and add a new method.</span></span>
5. <span data-ttu-id="0d844-207">X++ コード エディターで、新たなメソッドにコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="0d844-207">In the X++ code editor, enter a comment in the new method.</span></span>
6. <span data-ttu-id="0d844-208">既存メソッドにコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="0d844-208">Enter a comment in any existing method.</span></span>
7. <span data-ttu-id="0d844-209">**FMRental** を保存します。</span><span class="sxs-lookup"><span data-stu-id="0d844-209">Save the **FMRental**.</span></span>
8. <span data-ttu-id="0d844-210">**チーム エクスプローラー** で、**FMRental.xml** を右クリックして **最新バージョンと比較** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-210">In **Team Explorer**, right-click **FMRental.xml**, and select **Compare with Latest Version**.</span></span>

    <span data-ttu-id="0d844-211">[![バージョン間の比較](./media/compareversions_usingdevotools.png)](./media/compareversions_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-211">[![Compare versions](./media/compareversions_usingdevotools.png)](./media/compareversions_usingdevotools.png)</span></span>

9. <span data-ttu-id="0d844-212">**比較 (差異)** ウィンドウの違いを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d844-212">Browse through the differences in the **comparison (Diff)** window.</span></span>
10. <span data-ttu-id="0d844-213">**ソリューション エクスプローラー** で **FMRental** テーブルを右クリックし、**ソース管理 &gt; 元に戻す &gt; 保留中の変更** を選択して変更を元に戻します。</span><span class="sxs-lookup"><span data-stu-id="0d844-213">In **Solution Explorer**, right-click on the **FMRental** table, and select **Source control &gt; Undo &gt; Pending Changes** to revert your changes.</span></span>

    <span data-ttu-id="0d844-214">[![保留中の変更を元に戻す](./media/undo_usingdevotools.png)](./media/undo_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-214">[![Undo pending changes](./media/undo_usingdevotools.png)](./media/undo_usingdevotools.png)</span></span>

11. <span data-ttu-id="0d844-215">次のダイアログで取り消しを確認し、**差異** ウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0d844-215">Confirm the undo on the next dialog and close the **diff** window.</span></span>

## <a name="scenario-2-synchronize-models-from-source-control"></a><span data-ttu-id="0d844-216">シナリオ 2: ソース管理からモデルを同期する</span><span class="sxs-lookup"><span data-stu-id="0d844-216">Scenario 2: Synchronize models from source control</span></span>

<span data-ttu-id="0d844-217">このセクションでは、Azure DevOps プロジェクトから既存のモデルおよびモデル要素を同期します。</span><span class="sxs-lookup"><span data-stu-id="0d844-217">In this section, you will synchronize existing models and model elements from your Azure DevOps project.</span></span> <span data-ttu-id="0d844-218">同期は以下の場合に関連します。1) 以前のバージョンのコードを LCS 経由で移行した。2) 別の開発者が新しいモデルまたは新しいモデル要素をチェックインし、それらを開発環境と同期させたい。</span><span class="sxs-lookup"><span data-stu-id="0d844-218">Synchronization is relevant in the following cases: 1) You have migrated your code from a previous version via LCS, or 2) another developer has checked-in a new model or new model elements and you would like to synchronize them to your development environment.</span></span>

1. <span data-ttu-id="0d844-219">ソース管理エクスプローラーで、メタデータを右クリックして **最新バージョンの取得** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-219">In Source Control Explorer, right-click on Metadata and select **Get Latest Version**.</span></span> <span data-ttu-id="0d844-220">最新バージョンを取得することにより、ローカル パッケージ フォルダーと最新のコードが同期されます。</span><span class="sxs-lookup"><span data-stu-id="0d844-220">Getting the latest version will synchronize you local packages folder with the latest code.</span></span>
2. <span data-ttu-id="0d844-221">別の方法として、**詳細** メニューを使用して固有のビルド バージョンまたは変更セットを同期することができます。</span><span class="sxs-lookup"><span data-stu-id="0d844-221">Alternatively you can use the **Advanced** menu to synchronize specific build version or change sets.</span></span>

    ![最新バージョンの取得](./media/getlatest.png)

3. <span data-ttu-id="0d844-223">同期が完了し、新しいモデルを環境に同期させる場合は、Visual Studio からメタデータを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d844-223">Once synchronization is complete, and if the synchronization leads to synchronizing new models to your environment, you need to refresh your metadata from Visual Studio.</span></span>
4. <span data-ttu-id="0d844-224">**Dynamics 365 &gt; モデル管理 &gt; モデルの更新** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0d844-224">Go to **Dynamics 365 &gt; Model Management &gt; Refresh models**.</span></span>

## <a name="organize-todo-tasks-in-a-project"></a><span data-ttu-id="0d844-225">プロジェクト内の TODO タスクの整理</span><span class="sxs-lookup"><span data-stu-id="0d844-225">Organize TODO tasks in a project</span></span>

<span data-ttu-id="0d844-226">このセクションでは、X++コードに埋め込まれたタスク (TODO コメント) から Visual Studio プロジェクトを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d844-226">This section describes how you can create a Visual Studio project out of tasks (TODO comments) embedded in your X++ code.</span></span>

1. <span data-ttu-id="0d844-227">**ソリューション エクスプローラー** で、**移行されたフリート管理 &gt; コード &gt; クラス &gt; FMDataHelper** を選択してから、**FMDataHelper** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-227">In **Solution Explorer**, select **Fleet Management Migrated &gt; Code &gt; Classes &gt; FMDataHelper**, and then double-click **FMDataHelper**.</span></span> <span data-ttu-id="0d844-228">X++ コード エディターが開きます。</span><span class="sxs-lookup"><span data-stu-id="0d844-228">The X++ code editor opens.</span></span>
2. <span data-ttu-id="0d844-229">任意のメソッド内に、TODO コメント (//TODO: my comment) を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d844-229">Enter a TODO comment (//TODO: my comment) inside any method.</span></span>

    <span data-ttu-id="0d844-230">[![TODO コメントの例](./media/code_usingdevotools.png)](./media/code_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-230">[![Example of TODO comments](./media/code_usingdevotools.png)](./media/code_usingdevotools.png)</span></span>

3. <span data-ttu-id="0d844-231">他のフリート管理のクラスやテーブルを開き、さらに TODO コメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="0d844-231">Open other Fleet Management classes or tables and add more TODO comments.</span></span>
4. <span data-ttu-id="0d844-232">**FleetManagement Migrated** プロジェクトをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="0d844-232">Rebuild the **FleetManagement Migrated** project.</span></span>
5. <span data-ttu-id="0d844-233">**表示 &gt; タスク一覧** を選択し、Visual Studio **タスク一覧** ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="0d844-233">Select **View &gt; Task List**, to open the Visual Studio **Task List** window.</span></span>

    <span data-ttu-id="0d844-234">[![タスク一覧を開く](./media/tasklist_usingdevotools.png)](./media/tasklist_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-234">[![Opening the Task List](./media/tasklist_usingdevotools.png)](./media/tasklist_usingdevotools.png)</span></span>

6. <span data-ttu-id="0d844-235">ドロップダウン リストから **コメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-235">Select **Comments** from the drop-down list.</span></span>

    <span data-ttu-id="0d844-236">[![コメントの表示](./media/tasklistcomments_usingdevotools.png)](./media/tasklistcomments_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-236">[![Viewing comments](./media/tasklistcomments_usingdevotools.png)](./media/tasklistcomments_usingdevotools.png)</span></span>

7. <span data-ttu-id="0d844-237">すべての作業項目を選択して右クリックし、**新しいプロジェクトに追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-237">Select all TODO items, right-click, and select **Add to new project**.</span></span>

    <span data-ttu-id="0d844-238">[![TODO コメントの選択](./media/addnewproject_usingdevotools.png)](./media/addnewproject_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-238">[![Selecting TODO comments](./media/addnewproject_usingdevotools.png)](./media/addnewproject_usingdevotools.png)</span></span>

8. <span data-ttu-id="0d844-239">品目を追加することにより、**新規プロジェクト** ダイアログが開き、すべての TODO を含む新しいプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0d844-239">Adding the items will open the **New project** dialog and enable you to create a new project that contains all of your TODOs.</span></span>
9. <span data-ttu-id="0d844-240">このプロジェクトを作業プロジェクトとして保存し、TODO リストを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="0d844-240">You can save this project as a working project to manage your TODO list.</span></span>
10. <span data-ttu-id="0d844-241">完了したら、**チーム エクスプ ローラー** ですべての保留中の変更を元に戻します。</span><span class="sxs-lookup"><span data-stu-id="0d844-241">When you're finished, undo all of your pending changes in **Team Explorer**.</span></span>

    <span data-ttu-id="0d844-242">[![すべての変更を元に戻す](./media/undoall_usingdevotools.png)](./media/undoall_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-242">[![Undoing all the changes](./media/undoall_usingdevotools.png)](./media/undoall_usingdevotools.png)</span></span>

11. <span data-ttu-id="0d844-243">FleetManagement ソリューションを閉じるには、**ファイル &gt; ソリューションを閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-243">Click **File &gt; Close Solution**, to close the FleetManagement solution.</span></span>

## <a name="use-metadata-search-and-navigation-tools-to-find-elements-and-create-projects"></a><span data-ttu-id="0d844-244">メタデータ検索とナビゲーション ツールを使用して要素を検索し、プロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="0d844-244">Use metadata search and navigation tools to find elements and create projects</span></span>

<span data-ttu-id="0d844-245">このセクションでは、アプリケーション全体でメタデータ ベースの検索を実行する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0d844-245">This section demonstrates how you can perform meta-data based searches throughout your application.</span></span>

### <a name="use-the-metadata-search-window"></a><span data-ttu-id="0d844-246">[メタデータ検索] ウィンドウの使用</span><span class="sxs-lookup"><span data-stu-id="0d844-246">Use the Metadata search window</span></span>

1. <span data-ttu-id="0d844-247">**Dynamics 365 &gt; メタデータの検索** とクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-247">Click **Dynamics 365 &gt; Metadata search**.</span></span>
2. <span data-ttu-id="0d844-248">**メタデータ検索** ウィンドウの **検索** フィールドに、次のテキストを入力して会社間クエリを含むアプリケーション スイート モデルのすべてのテーブル挿入メソッドを検索します。</span><span class="sxs-lookup"><span data-stu-id="0d844-248">In the **Metadata search** window, in the **Search** field, enter the following text to find all of the table insert methods in the Application Suite model that contain a cross-company query.</span></span> <span data-ttu-id="0d844-249">`type:table,method name:insert code:"crosscompany" model:"Application Suite"`。</span><span class="sxs-lookup"><span data-stu-id="0d844-249">`type:table,method name:insert code:"crosscompany" model:"Application Suite"`.</span></span>
3. <span data-ttu-id="0d844-250">検索が完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="0d844-250">Wait for the search to complete.</span></span> <span data-ttu-id="0d844-251">これにはしばらく時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0d844-251">It may take a while.</span></span>

   ![メタデータの検索結果](./media/metadatasearchresults_usingdevotools.png)

4. <span data-ttu-id="0d844-253">リスト内の結果をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-253">Double-click a result in the list.</span></span> <span data-ttu-id="0d844-254">コード エディターが開き、検索条件に一致する行にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="0d844-254">The code editor will open and place the cursor at the line that matches your search criteria.</span></span>
5. <span data-ttu-id="0d844-255">Ctrl キーを押しながら複数選択することで結果リストで複数の要素を選択し、右クリックして **新しいプロジェクトに追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-255">Select several elements in the results list by holding down the Ctrl key for multiple selections, right-click, and then select **Add to new project**.</span></span> <span data-ttu-id="0d844-256">要素を追加することにより、選択した要素を含む新しいソリューションとプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0d844-256">Adding the elements will let you to create a new solution and project containing the selected elements.</span></span>

### <a name="try-other-search-examples"></a><span data-ttu-id="0d844-257">他の検索例を試す</span><span class="sxs-lookup"><span data-stu-id="0d844-257">Try other search examples</span></span>

<span data-ttu-id="0d844-258">検索結果を操作する前に、検索が完了するのを待つ必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0d844-258">You don't need to wait for the search to complete before you interact with search results.</span></span> <span data-ttu-id="0d844-259">いつでも結果をダブルクリックして、検索条件に一致するメタデータまたはソース コードを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0d844-259">You can double-click results at any time to view the metadata or source code that matches your search criteria.</span></span> <span data-ttu-id="0d844-260">推奨される検索例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0d844-260">The following are some suggested search examples:</span></span>

- <span data-ttu-id="0d844-261">モデル アプリケーション スイートの表示モードおよび自動幅モードで定義された、垂直タブのコントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="0d844-261">Find vertical tab controls defined in view mode and autowidth mode in the model Application Suite.</span></span> 

    `type:form,formtabcontrol property:arrangeMethod=Vertical,ViewEditMode=view,WidthMode=Auto model:"Application Suite"`

- <span data-ttu-id="0d844-262">プロパティ heightmode = 列で、編集できないフォームですべてのグリッド コントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="0d844-262">Find all grid controls in forms that aren't editable and with the property heightmode = column.</span></span>

    `type:form,formgridcontrol:allowedit=no,heightmode=column`

- <span data-ttu-id="0d844-263">アプリケーション スイート モデル内のすべての SimpleListDetail フォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="0d844-263">Find all SimpleListDetail forms in the Application Suite model.</span></span>

    `type:formdesign property:style=simplelistdetail model:"Application Suite"`

- <span data-ttu-id="0d844-264">キーワード xpNum を含むインデックス フィールド名を持つすべてのテーブルを検索します。</span><span class="sxs-lookup"><span data-stu-id="0d844-264">Find all tables that have an index field name that contains the keyword xpNum.</span></span>

    `type:table,tableindexfield anem: xpNum*`

- <span data-ttu-id="0d844-265">以前の検索条件にアクセスするには、検索バーのドロップダウン メニューを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d844-265">Use the search bar drop-down menu to access previous searches.</span></span>

    <span data-ttu-id="0d844-266">[![ドロップダウン メニューの使用](./media/accessprevious_usingdevotools.png)](./media/accessprevious_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-266">[![Using the drop-down menu](./media/accessprevious_usingdevotools.png)](./media/accessprevious_usingdevotools.png)</span></span>

## <a name="navigate-to-related-elements"></a><span data-ttu-id="0d844-267">関連する要素への移動</span><span class="sxs-lookup"><span data-stu-id="0d844-267">Navigate to related elements</span></span>

<span data-ttu-id="0d844-268">このセクションでは、**アプリケーション エクスプローラー** または **ソリューション エクスプローラー** で関連要素を見つけることなく、ある要素から関連要素に移動する機能を紹介します。</span><span class="sxs-lookup"><span data-stu-id="0d844-268">This section highlights a feature that enables you to move from one element to a related element without having to find the related elements in **Application Explorer** or **Solution Explorer**.</span></span>

1. <span data-ttu-id="0d844-269">**アプリケーション エクスプローラー** を開き、**モデル ビュー** に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0d844-269">Open **Application Explorer**, and switch the view to **Model View**.</span></span>

    <span data-ttu-id="0d844-270">[![モデル ビューでアプリケーション エクスプローラーを開く](./media/modelview_usingdevotool1.png)](./media/modelview_usingdevotool1.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-270">[![Opening Application Explorer in Model View](./media/modelview_usingdevotool1.png)](./media/modelview_usingdevotool1.png)</span></span>

2. <span data-ttu-id="0d844-271">**フリート管理** モデルで、**ユーザー インターフェイス&gt;メニュー項目&gt;メニュー項目を表示&gt;FMCustomer** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-271">Under the **Fleet Management** model, click **User Interface &gt; Menu items &gt; Display Menu Items &gt; FMCustomer**.</span></span>

    <span data-ttu-id="0d844-272">[![アプリケーション エクスプローラーで FMCustomer を選択する](./media/fmcustomerisv_usingdevotools.png)](./media/fmcustomerisv_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-272">[![Selecting FMCustomer in Application Explorer](./media/fmcustomerisv_usingdevotools.png)](./media/fmcustomerisv_usingdevotools.png)</span></span>

3. <span data-ttu-id="0d844-273">**FMCustomer** を右クリックし、**デザイナーを開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-273">Right-click **FMCustomer**, and then select **Open designer**.</span></span>
4. <span data-ttu-id="0d844-274">**FMCustomer** メニュー項目デザイナーでルート ノードを右クリックし、**フォーム FMCustomer に移動する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-274">In the **FMCustomer** menu item designer, right-click the root node, and then select **Go to Form FMCustomer**.</span></span>

    <span data-ttu-id="0d844-275">[![アプリケーション エクスプローラーを使用したフォームへの移動](./media/goformfmcustomer_usingdevotools.png)](./media/goformfmcustomer_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-275">[![Navigating to a form using Application Explorer](./media/goformfmcustomer_usingdevotools.png)](./media/goformfmcustomer_usingdevotools.png)</span></span>

    <span data-ttu-id="0d844-276">**FMCustomer** フォーム デザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="0d844-276">The **FMCustomer** form designer will open.</span></span>

5. <span data-ttu-id="0d844-277">**FMCustomer** フォームのデザイナーで、**データ ソース** を展開して、**FMCustomer** を右クリックしてから **テーブル FMCustomer へ移動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-277">In the designer of the **FMCustomer** form, expand **Data sources**, right-click **FMCustomer**, and then select **Go to Table FMCustomer**</span></span>

    <span data-ttu-id="0d844-278">[![アプリケーション エクスプローラーを使用したテーブルへの移動](./media/gotablefmcustomer_usingdevotools.png)](./media/gotablefmcustomer_usingdevotools.png)</span><span class="sxs-lookup"><span data-stu-id="0d844-278">[![Navigating to a table using Application Explorer](./media/gotablefmcustomer_usingdevotools.png)](./media/gotablefmcustomer_usingdevotools.png)</span></span>

    <span data-ttu-id="0d844-279">**FMCustomer** テーブル デザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="0d844-279">The **FMCustomer** table designer will open.</span></span>

6. <span data-ttu-id="0d844-280">同じ方法を使用すると、テーブル フィールドが参照する EDT 要素に移動できます。</span><span class="sxs-lookup"><span data-stu-id="0d844-280">Using the same methodology, you can navigate to the EDT element that a table field references.</span></span> <span data-ttu-id="0d844-281">**ヒント**: コンテキスト メニューを開くのではなく F9 キーを押します。</span><span class="sxs-lookup"><span data-stu-id="0d844-281">**Tip**: Press F9 instead of opening the context menu.</span></span> <span data-ttu-id="0d844-282">F9 キーを押すと、参照要素のデザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="0d844-282">F9 will open the designer of the referenced element.</span></span> <span data-ttu-id="0d844-283">**ヒント**: 現在のプロジェクトに要素を追加するには、ドキュメント タブを右クリックし、**プロジェクトへの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-283">**Tip**: You can add an element to the current project by right-clicking on the document tab and selecting **Add to project**.</span></span>

    ![プロジェクトへの追加を使用する](./media/addtoproject_usingdevotools.png)

## <a name="use-application-explorer-to-create-a-project-from-a-model"></a><span data-ttu-id="0d844-285">アプリケーション エクスプローラーを使用してモデルからプロジェクトを作成</span><span class="sxs-lookup"><span data-stu-id="0d844-285">Use Application Explorer to create a project from a model</span></span>

<span data-ttu-id="0d844-286">アプリケーション エクスプ ローラーを使用して、モデルのすべてまたは一部の要素を検索し、検索結果からプロジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="0d844-286">You can use Application Explorer to search for all or some elements of a model and create a project out of the search results.</span></span>

1. <span data-ttu-id="0d844-287">要素のタイプでプロジェクトを整理するためのオプションがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0d844-287">Make sure the option to organize a project by element type is on.</span></span> <span data-ttu-id="0d844-288">**Dynamics 365** \> **オプション** \> **プロジェクト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0d844-288">Go to **Dynamics 365** \> **Options** \> **Projects**.</span></span>
2. <span data-ttu-id="0d844-289">アプリケーション エクスプローラーに移動し、目的のモデル内の要素を検索します。</span><span class="sxs-lookup"><span data-stu-id="0d844-289">Go to Application Explorer and search for elements in the desired model.</span></span> <span data-ttu-id="0d844-290">たとえば、*モデル: "フリート管理"* を入力し、**入力** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d844-290">For example, enter *model:"fleet management"* and click **Enter**.</span></span>

    <span data-ttu-id="0d844-291">[![アプリケーション エクスプローラーでモデルを検索する](./media/appexplorermodelsearch.jpg)](./media/appexplorermodelsearch.jpg)</span><span class="sxs-lookup"><span data-stu-id="0d844-291">[![Searching for model in Application Explorer](./media/appexplorermodelsearch.jpg)](./media/appexplorermodelsearch.jpg)</span></span>

3. <span data-ttu-id="0d844-292">検索が完了したら、AOT ルート ノードを右クリックし、**新しいプロジェクトへの検索結果の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d844-292">When the search is complete, right-click the AOT root node and select **Add search results to new project.**</span></span>

    <span data-ttu-id="0d844-293">[![新しいモデルに品目を追加する](./media/addsearchresultstonewproject.jpg)](./media/addsearchresultstonewproject.jpg)</span><span class="sxs-lookup"><span data-stu-id="0d844-293">[![Add item to a new model](./media/addsearchresultstonewproject.jpg)](./media/addsearchresultstonewproject.jpg)</span></span>

4. <span data-ttu-id="0d844-294">新しいプロジェクト ダイアログ ボックスでプロジェクトのプロパティを指定し、**OK** をクリックしてプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="0d844-294">Specify your project properties in the new project dialog and click **OK** to create the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="0d844-295">検索結果からプロジェクトを作成するには、すべての結果が同じモデル内にある限り、任意のタイプ、名前、またはその他のフィルタを検索に追加できます。</span><span class="sxs-lookup"><span data-stu-id="0d844-295">To create a project from search results, you can add any type, name, or other filters to your search as long as all results are in the same model.</span></span> <span data-ttu-id="0d844-296">例: *モデル:「フリート管理」 タイプ:テーブル名:^FM* は、文字 FM で始まる名前を持つフリート管理モデルで、すべてのテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="0d844-296">For example: *model:"Fleet Management" type:Table name:^FM* will return all tables in the Fleet Management model with a name starting with the letters FM.</span></span>
