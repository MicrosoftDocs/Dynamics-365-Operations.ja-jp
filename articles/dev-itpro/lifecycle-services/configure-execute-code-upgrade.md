---
title: "Lifecycle Services (LCS) で、コード アップグレード サービスを構成する"
description: "このトピックでは、Lifecycle Services (LCS) の <strong>コード アップグレード</strong> タイルを構成して、ソリューションを最新バージョンの Finance and Operations に移行する方法について説明します。"
author: tariqbell
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 265594
ms.assetid: 964b5a15-9b9c-434c-a4c2-e14406ebfaeb
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fcef08f348ec6bf0ff903c6f3a255763ba7b5808
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="configure-the-code-upgrade-service-in-lifecycle-services-lcs"></a><span data-ttu-id="84408-103">Lifecycle Services (LCS) で、コード アップグレード サービスを構成する</span><span class="sxs-lookup"><span data-stu-id="84408-103">Configure the code upgrade service in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84408-104">このトピックでは、Lifecycle Services (LCS) の <strong>コード アップグレード</strong> タイルを構成して、ソリューションを最新バージョンの Dynamics 365 for Finance and Operations に移行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="84408-104">This topic explains how to configure the <strong>Code upgrade </strong>tile in Lifecycle Services (LCS) to migrate your solution to the latest version of Dynamics 365 for Finance and Operations.</span></span>

<a name="overview"></a><span data-ttu-id="84408-105">概要</span><span class="sxs-lookup"><span data-stu-id="84408-105">Overview</span></span>
--------

<span data-ttu-id="84408-106">コードのアップグレード ツールは、Visual Studio Team Services (VSTS) に接続し、トランク\\メインブランチを検索し、リリース\\\<バージョン番号\>という名前の新しいブランチに分岐してから、コードのアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="84408-106">The code upgrade tool operates by connecting to Visual Studio Team Services (VSTS), locating your Trunk\\Main branch, branching to a new branch which will be named as Releases\\\<version number\>, and then performing the code upgrade there.</span></span> <span data-ttu-id="84408-107">このプロセスが完了した後、Finance and Operations 開発環境を、リリース \\\<バージョン番号\> 下の新しいブランチに同期させ、競合を解決できます。</span><span class="sxs-lookup"><span data-stu-id="84408-107">After this process is complete you can synchronize your Finance and Operations developer environment to this new branch under Releases\\\<version number\> and resolve conflicts.</span></span> <span data-ttu-id="84408-108">アップグレード後のコードをコンパイルしてテストしたとき、新しいブランチを Visual Studio のソース管理エクスプ ローラーを使用して Trunk\\Main にマージすると、プロセスが完了します。</span><span class="sxs-lookup"><span data-stu-id="84408-108">When you have compiled and tested your upgraded code you can merge the new branch back into Trunk\\Main, using source control explorer in Visual Studio and the process is complete.</span></span>

<span data-ttu-id="84408-109">Dynamics 365 for Finance and Operations 8.0 およびこれ以降のバージョンでは、Microsoft モデルのオーバーレイ経由でのカスタマイズは許可されていません。</span><span class="sxs-lookup"><span data-stu-id="84408-109">Dynamics 365 for Finance and Operations version 8.0 and newer, does not allow customization via overlayering of Microsoft models.</span></span> <span data-ttu-id="84408-110">アップグレードする前に、カスタマイズを拡張機能にリファクターする計画が必要です。</span><span class="sxs-lookup"><span data-stu-id="84408-110">Before you upgrade, you must have have a plan to refactor your customizations into extensions.</span></span> <span data-ttu-id="84408-111">詳細については、[拡張機能のホームページ](../extensibility/extensibility-home-page.md)および [8.0 環境でオーバーレイをリファクタリングする](../extensibility/refactoring-over-layering.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84408-111">For more information, see the [Extensibility homepage](../extensibility/extensibility-home-page.md) and [Refactor overlayering on 8.0 environments](../extensibility/refactoring-over-layering.md).</span></span>

## <a name="process"></a><span data-ttu-id="84408-112">プロセス</span><span class="sxs-lookup"><span data-stu-id="84408-112">Process</span></span>
### <a name="create-the-trunkmain-folder-structure"></a><span data-ttu-id="84408-113">トランク\\メイン フォルダー構造を作成する</span><span class="sxs-lookup"><span data-stu-id="84408-113">Create the Trunk\\Main folder structure</span></span>

<span data-ttu-id="84408-114">ソース コードを識別するコード アップグレード サービスについては、フォルダ構造は以下の厳密なパターンに準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="84408-114">For the code upgrade service to recognize your source code, the folder structure must conform to the following strict pattern.</span></span> <span data-ttu-id="84408-115">正しい構造は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="84408-115">The correct structure is:</span></span> 

 - <span data-ttu-id="84408-116">コード自体用: ..\\\<VSTS プロジェクト名 >\\トランク\\メイン\\メタデータ</span><span class="sxs-lookup"><span data-stu-id="84408-116">For code itself: ..\\\<VSTS project name>\\Trunk\\Main\\Metadata</span></span>
 - <span data-ttu-id="84408-117">Visual Studio プロジェクト用: ..\\\<VSTS プロジェクト名 >\\トランク\\メイン\\プロジェクト</span><span class="sxs-lookup"><span data-stu-id="84408-117">For Visual Studio projects: ..\\\<VSTS project name>\\Trunk\\Main\\Projects</span></span>
 
 <span data-ttu-id="84408-118">VSTS で新しいフォルダーを作成するには、ローカルでフォルダーを作成し、VSTS にチェックインします。</span><span class="sxs-lookup"><span data-stu-id="84408-118">To create new folders in VSTS, create the folders locally and then check them into VSTS.</span></span>
 
 > [!NOTE]
 > <span data-ttu-id="84408-119">フォルダー名は大文字と小文字を区別していて、つまり、メインおよびメインでない、またはコードのアップグレード サービスはフォルダーを認識しません。</span><span class="sxs-lookup"><span data-stu-id="84408-119">Folder names are case sensitive, that is, you must use Main and not MAIN, or the code upgrade service will not recognize the folder.</span></span> 


### <a name="to-create-a-personal-access-token"></a><span data-ttu-id="84408-120">個人用アクセス トークンを作成するには</span><span class="sxs-lookup"><span data-stu-id="84408-120">To create a personal access token</span></span>

<span data-ttu-id="84408-121">VSTS プロジェクトに接続するために、LCS は個人用アクセス トークンを使用して認証されます。</span><span class="sxs-lookup"><span data-stu-id="84408-121">To connect to a VSTS project, LCS is authenticated using a personal access token.</span></span> <span data-ttu-id="84408-122">VSTS で個人用アクセス トークンを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="84408-122">Use the following steps to create a personal access token in VSTS.</span></span> <span data-ttu-id="84408-123">LCS プロジェクトを VSTS プロジェクトへ接続できるように構成する場合、このセクションを省略できます。</span><span class="sxs-lookup"><span data-stu-id="84408-123">If you have already configured your LCS project to connect to your VSTS project, you can skip this section.</span></span>

1. <span data-ttu-id="84408-124">visualstudio.com にログインし、VSTS プロジェクトを見つけます。</span><span class="sxs-lookup"><span data-stu-id="84408-124">Sign in to visualstudio.com and locate your VSTS project.</span></span>
2. <span data-ttu-id="84408-125">右上隅で、名前をポイントするとメニューが表示され、**セキュリティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="84408-125">In the top right corner, hover over your name, a menu appears, select **Security**.</span></span>
3. <span data-ttu-id="84408-126">**追加**をクリックして、新しい個人用アクセス トークンを作成し、名前を付けて、トークンが使用できる期間を入力します。</span><span class="sxs-lookup"><span data-stu-id="84408-126">Click **Add** to create a new personal access token, give it a name, and then enter the amount of time that you want the token to last for.</span></span> <span data-ttu-id="84408-127">**トークンの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84408-127">Click **Create Token**.</span></span> 

   <span data-ttu-id="84408-128">[![コード アップグレードのトークンの作成](./media/codeupgrademaketoken.png)](./media/codeupgrademaketoken.png)</span><span class="sxs-lookup"><span data-stu-id="84408-128">[![Code upgrade create token](./media/codeupgrademaketoken.png)](./media/codeupgrademaketoken.png)</span></span>

4. <span data-ttu-id="84408-129">トークンをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="84408-129">Copy the token to your clipboard.</span></span> <span data-ttu-id="84408-130">このステップが完了したら、トークンの詳細情報を見つけることはできません。したがって、このページから移動する前に、かならずトークンをコピーしてください。</span><span class="sxs-lookup"><span data-stu-id="84408-130">You will not be able to find the token details after this step is completed, so be sure that you have copied the token before navigating away from this page.</span></span>

### <a name="configure-your-lifecycle-services-project-to-connect-to-vsts"></a><span data-ttu-id="84408-131">Lifecycle Services プロジェクトをコンフィギュレーションして VSTS に接続する</span><span class="sxs-lookup"><span data-stu-id="84408-131">Configure your Lifecycle Services project to connect to VSTS</span></span>

1. <span data-ttu-id="84408-132">LCS プロジェクトで、**プロジェクト設定**タイルに移動し、**Visual Studio Team Services** を選択してから、**Visual Studio Team Services の設定**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="84408-132">In your LCS project, go to the **Project settings** tile, select **Visual Studio Team Services**, and then select the **Setup Visual Studio Team Services** button.</span></span> <span data-ttu-id="84408-133">この構成は多くの LCS ツールで必要になります。すでに VSTS プロジェクトに接続するように LCS を設定している場合は、このセクションをスキップできます。</span><span class="sxs-lookup"><span data-stu-id="84408-133">This configuration is needed by many LCS tools, if you have already configured LCS to connect to your VSTS project, you can skip this section.</span></span> 

   <span data-ttu-id="84408-134">[![LCS VSTS の設定](./media/lcs_vsts_setup.png)](./media/lcs_vsts_setup.png)</span><span class="sxs-lookup"><span data-stu-id="84408-134">[![LCS VSTS setup](./media/lcs_vsts_setup.png)](./media/lcs_vsts_setup.png)</span></span>

2. <span data-ttu-id="84408-135">VSTS アカウントのルート URL および以前に作成したアクセス トークンを入力し、**続行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84408-135">Enter the root URL for your VSTS account and the access token created earlier, and then click **Continue**.</span></span>

   <span data-ttu-id="84408-136">[![LCS トークン](./media/lcstoken.png)](./media/lcstoken.png)</span><span class="sxs-lookup"><span data-stu-id="84408-136">[![LCS token](./media/lcstoken.png)](./media/lcstoken.png)</span></span>

3. <span data-ttu-id="84408-137">接続する VSTS アカウント内のプロジェクトを選択し、**続行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84408-137">Select the project within your VSTS account that you want to connect to, and select **Continue**.</span></span> 
   <span data-ttu-id="84408-138">[![LCS がプロジェクトを選択](./media/lcs_selectproject.png)](./media/lcs_selectproject.png)</span><span class="sxs-lookup"><span data-stu-id="84408-138">[![LCS select project](./media/lcs_selectproject.png)](./media/lcs_selectproject.png)</span></span>

4. <span data-ttu-id="84408-139">**確認および保存**ページで、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84408-139">On the **Review and save** page, click **Save**.</span></span>

### <a name="create-an-ax7version-file"></a><span data-ttu-id="84408-140">ax7.version ファイルを作成します</span><span class="sxs-lookup"><span data-stu-id="84408-140">Create an ax7.version file</span></span>

<span data-ttu-id="84408-141">LCS のコードのアップグレード タイルは、移行元の Finance and Operations のバージョンを自動的に検出します。ソース管理のメイン フォルダの ax7.version ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="84408-141">The code upgrade tile in LCS automatically finds the version of Finance and Operations that you are migrating from, by reading the ax7.version file under the Main folder in your source control.</span></span> <span data-ttu-id="84408-142">以下に示すように、Visual Studio または VSTS ポータルを通じて、このファイルを手動で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84408-142">You must create this file manually, either in Visual Studio or through the VSTS portal, as shown below.</span></span> <span data-ttu-id="84408-143">Dynamics AX 2012 R3 またはそれ以前のバージョンからコードを移行した場合、このファイルは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="84408-143">This file is not needed if you migrated your code from Dynamics AX 2012 R3 or an earlier version.</span></span> <span data-ttu-id="84408-144">ここに入力するバージョン番号は、アプリケーションのバージョン (プラットフォームのバージョンではない) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="84408-144">The version number entered here must be the application version (not the platform version).</span></span> <span data-ttu-id="84408-145">このファイルに無効なバージョン番号を入力するとしてのコード アップグレードの実行に失敗する可能性があるため、ここには必ず正しいバージョン番号を入力してください。</span><span class="sxs-lookup"><span data-stu-id="84408-145">Take care to enter the correct version number here as entering an incorrect version number in this file may cause your code upgrade run to fail.</span></span>

<span data-ttu-id="84408-146">[![ax7 バージョン ファイル](./media/ax7_versionfile.png)](./media/ax7_versionfile.png)</span><span class="sxs-lookup"><span data-stu-id="84408-146">[![ax7 version file](./media/ax7_versionfile.png)](./media/ax7_versionfile.png)</span></span> 

<span data-ttu-id="84408-147">どのアプリケーション バージョンを持っているか識別する方法の詳細については、[Microsoft Dynamics AX ビルド番号の概要](https://blogs.msdn.microsoft.com/axsupport/2012/03/29/overview-of-microsoft-dynamics-ax-build-numbers/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84408-147">For more information about how to identify which application version you have, see [Overview of Microsoft Dynamics AX build numbers](https://blogs.msdn.microsoft.com/axsupport/2012/03/29/overview-of-microsoft-dynamics-ax-build-numbers/).</span></span>

### <a name="execute-the-code-upgrade-tile"></a><span data-ttu-id="84408-148">コード アップグレード タイルを実行</span><span class="sxs-lookup"><span data-stu-id="84408-148">Execute the code upgrade tile</span></span>

1. <span data-ttu-id="84408-149">LCS プロジェクトで、**コードのアップグレード** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="84408-149">In your LCS project, select the **Code upgrade** tile.</span></span> 

   <span data-ttu-id="84408-150">[![コード アップグレード タイル](./media/codeupgradetile.png)](./media/codeupgradetile.png)</span><span class="sxs-lookup"><span data-stu-id="84408-150">[![Code upgrade tile](./media/codeupgradetile.png)](./media/codeupgradetile.png)</span></span>

2. <span data-ttu-id="84408-151">画面の左下隅で、**追加**をクリックしてから名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="84408-151">In the bottom left corner of the screen, click **Add**, and then enter a name and description.</span></span> <span data-ttu-id="84408-152">アップグレード元のバージョンとして Microsoft Dynamics AX 7 を選択し、**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84408-152">Select the version you are upgrading from as Microsoft Dynamics AX 7, and then click **Create**.</span></span>
   -   <span data-ttu-id="84408-153">Dynamics AX 2012 R3 からコードをアップグレードする場合、アップグレード元のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="84408-153">If you are upgrading your code from Dynamics AX 2012 R3, select the version you are upgrading from.</span></span> <span data-ttu-id="84408-154">圧縮バージョンの Dynamics AX 2012 R3 モデル ストア ファイルをアップロードするように要求されます。</span><span class="sxs-lookup"><span data-stu-id="84408-154">You will be prompted to upload a zipped version of your Dynamics AX 2012 R3 model store file.</span></span>
   -   <span data-ttu-id="84408-155">**見積のみ**チェック ボックスがオンになっている場合、ツールはレポートのみを生成し、チェックインや VSTS の新しいコード分岐の作成を行いません。</span><span class="sxs-lookup"><span data-stu-id="84408-155">If the **Estimation Only** check box is selected, the tool only generates a report and does not check in or create a new code branch in VSTS for you.</span></span> <span data-ttu-id="84408-156">実際のアップグレードをコミットする前に、アップグレードに必要な作業の潜在的なサイズを評価する場合、このオプションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84408-156">You should use this option if you want to evaluate the potential size of the work involved in upgrading before you commit to the actual upgrade.</span></span>

   <span data-ttu-id="84408-157">[![新規コード ブランチ](./media/codeupgrade_new.png)](./media/codeupgrade_new.png)</span><span class="sxs-lookup"><span data-stu-id="84408-157">[![New code branch](./media/codeupgrade_new.png)](./media/codeupgrade_new.png)</span></span>

3. <span data-ttu-id="84408-158">右下にある**コードの分析**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="84408-158">Click **Analyze code** in the bottom right corner.</span></span> <span data-ttu-id="84408-159">コードのアップグレード プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="84408-159">The code upgrade process will start.</span></span> <span data-ttu-id="84408-160">これは、大規模なソリューションが完了するまでに通常 40 分かかります。</span><span class="sxs-lookup"><span data-stu-id="84408-160">This typically takes 40 minutes for a large solution to complete.</span></span> <span data-ttu-id="84408-161">完了したら、LCS の **コードのアップグレード** タイルに戻り、結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="84408-161">When complete, return to the **Code upgrade** tile in LCS to view the results.</span></span>
4. <span data-ttu-id="84408-162">コードのアップグレード サービスは、新しいブランチを作成し、アップグレードされたコードを VSTS プロジェクトにチェックインします。</span><span class="sxs-lookup"><span data-stu-id="84408-162">The code upgrade service creates a new branch and checks in the upgraded code to your VSTS project.</span></span> <span data-ttu-id="84408-163">アップグレード プロセスが完了した後、コードは**リリース**フォルダ下の新しいブランチに存在します。</span><span class="sxs-lookup"><span data-stu-id="84408-163">After the upgrade process is complete, your code will exist in a new branch under the **Releases** folder.</span></span> <span data-ttu-id="84408-164">分岐名の後には、アップグレードの日時が付いています。</span><span class="sxs-lookup"><span data-stu-id="84408-164">The branch name is suffixed with the date and time of the upgrade.</span></span> 

   <span data-ttu-id="84408-165">[![コード アップグレード ブランチ](./media/codeupgradebranch-300x192.png)](./media/codeupgradebranch.png)</span><span class="sxs-lookup"><span data-stu-id="84408-165">[![Code upgrade branch](./media/codeupgradebranch-300x192.png)](./media/codeupgradebranch.png)</span></span>


### <a name="merge-releases-back-into-trunkmain"></a><span data-ttu-id="84408-166">リリースを Trunk\\Main にマージ</span><span class="sxs-lookup"><span data-stu-id="84408-166">Merge Releases back into Trunk\\Main</span></span>

<span data-ttu-id="84408-167">リリース\\\<バージョン番号\>のアップグレードされたコードが正常にコンパイルされ、テストに合格したら、このブランチをトランク\\メインにマージする準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="84408-167">Once the upgraded code in Releases\\\<version number\> compiles sucessfully and has passed your tests, then you are ready to merge this branch back into Trunk\\Main.</span></span> <span data-ttu-id="84408-168">これを行うには、Visual Studio の開発環境で、[ソース管理エクスプローラー] ウィンドウを開き、**リリース\\\<バージョン番号\>** 分岐を右クリックし、コンテキスト メニューで **分岐とマージ** に進み、サブ メニューで **マージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84408-168">To do this, on your development environment in Visual Studio open the Source control explorer pane then right-click on the **Releases\\\<version number\>** branch and in the context menu go to **Branching and Merging** and then on the sub-menu select **Merge**.</span></span>

<span data-ttu-id="84408-169">[![リリース ブランチのマージ](./media/MergeReleasesBranch.PNG)](./media/MergeReleasesBranch.PNG)</span><span class="sxs-lookup"><span data-stu-id="84408-169">[![Merge release branch](./media/MergeReleasesBranch.PNG)](./media/MergeReleasesBranch.PNG)</span></span>

<span data-ttu-id="84408-170">これにより、[[ソース管理マージ ウィザード](https://www.visualstudio.com/en-us/docs/tfvc/merge-folders-files#sourcecontrolwizard)] が開きます。これは、リリース\\\<のバージョン番号\>のブランチをトランク\\メインにマージする手順を案内します。</span><span class="sxs-lookup"><span data-stu-id="84408-170">This will open the [Source Control Merge Wizard](https://www.visualstudio.com/en-us/docs/tfvc/merge-folders-files#sourcecontrolwizard) which will guide you through merging the Releases\\\<version number\> branch back into Trunk\\Main.</span></span> 

