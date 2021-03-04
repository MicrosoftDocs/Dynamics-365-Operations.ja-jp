---
title: Lifecycle Services (LCS) で、コード アップグレード サービスを構成する
description: このトピックでは、コード アップグレード タイルを構成して、ソリューションを最新バージョンの Finance and Operations アプリに移行する方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 265594
ms.assetid: 964b5a15-9b9c-434c-a4c2-e14406ebfaeb
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a4470bd84c3766dabe03eae4b494a277aa66677
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128867"
---
# <a name="configure-the-code-upgrade-service-in-lifecycle-services-lcs"></a><span data-ttu-id="adf1c-103">Lifecycle Services (LCS) で、コード アップグレード サービスを構成する</span><span class="sxs-lookup"><span data-stu-id="adf1c-103">Configure the code upgrade service in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adf1c-104">このトピックでは、Lifecycle Services (LCS) の<strong>コード アップグレード</strong> タイルを構成して、ソリューションを最新バージョンの Dynamics 365 Finance and Operations アプリに移行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-104">This topic explains how to configure the <strong>Code upgrade </strong>tile in Lifecycle Services (LCS) to migrate your solution to the latest version of the Dynamics 365 Finance and Operations apps.</span></span>

<a name="overview"></a><span data-ttu-id="adf1c-105">概要</span><span class="sxs-lookup"><span data-stu-id="adf1c-105">Overview</span></span>
--------


<span data-ttu-id="adf1c-106">コードのアップグレード ツールは、Azure DevOps プロジェクトに接続し、トランク\\メイン ブランチを検索し、リリース\\\<version number\> という名前の新しいブランチに分岐してから、コードのアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-106">The code upgrade tool operates by connecting to your Azure DevOps project, locating your Trunk\\Main branch, branching to a new branch that will be named as Releases\\\<version number\>, and then performing the code upgrade there.</span></span> <span data-ttu-id="adf1c-107">このプロセスが完了した後、開発環境を、リリース\\\<version number\> の下の新しいブランチに同期させ、競合を解決できます。</span><span class="sxs-lookup"><span data-stu-id="adf1c-107">After this process is complete, you can synchronize your developer environment to this new branch under Releases\\\<version number\> and resolve conflicts.</span></span> <span data-ttu-id="adf1c-108">アップグレード後のコードをコンパイルしてテストしたとき、新しいブランチを Visual Studio のソース管理エクスプ ローラーを使用して Trunk\\Main にマージすると、プロセスが完了します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-108">When you have compiled and tested your upgraded code you can merge the new branch back into Trunk\\Main, using source control explorer in Visual Studio and the process is complete.</span></span>


<span data-ttu-id="adf1c-109">Dynamics 365 for Finance and Operations バージョン 8.0 およびそれ以降では、Microsoft モデルをオーバーレイしてカスタマイズすることはできません。</span><span class="sxs-lookup"><span data-stu-id="adf1c-109">Dynamics 365 for Finance and Operations version 8.0 and newer, does not allow customization via overlayering of Microsoft models.</span></span> <span data-ttu-id="adf1c-110">アップグレードする前に、カスタマイズを拡張機能にリファクターする計画が必要です。</span><span class="sxs-lookup"><span data-stu-id="adf1c-110">Before you upgrade, you must have a plan to refactor your customizations into extensions.</span></span> <span data-ttu-id="adf1c-111">詳細については [拡張機能のホーム ページ](../extensibility/extensibility-home-page.md) および [モデルの制限を緩和して、オーバレイを拡張機能にリファクタリングする](../extensibility/refactoring-over-layering.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adf1c-111">For more information, see the [Extensibility home page](../extensibility/extensibility-home-page.md) and [Relax model restrictions to refactor overlayering into extensions](../extensibility/refactoring-over-layering.md).</span></span>

## <a name="process"></a><span data-ttu-id="adf1c-112">処理</span><span class="sxs-lookup"><span data-stu-id="adf1c-112">Process</span></span>
### <a name="create-the-trunkmain-folder-structure"></a><span data-ttu-id="adf1c-113">トランク\\メイン フォルダー構造を作成する</span><span class="sxs-lookup"><span data-stu-id="adf1c-113">Create the Trunk\\Main folder structure</span></span>

<span data-ttu-id="adf1c-114">ソース コードを識別するコード アップグレード サービスについては、Azure DevOps プロジェクトには Team Foundation バージョン管理 (TFVC) コード リポジトリが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="adf1c-114">For the code upgrade service to recognize your source code, your Azure DevOps project must contain a Team Foundation Version Control (TFVC) code repository.</span></span> <span data-ttu-id="adf1c-115">さらに、コード リポジトリ フォルダー構造は、次の厳密なパターンに準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="adf1c-115">In addition, the code repository folder structure must conform to the following strict pattern.</span></span> 

 - <span data-ttu-id="adf1c-116">コードおよびメタデータ: /<DevOps project name>/Trunk/Main/Metadata</span><span class="sxs-lookup"><span data-stu-id="adf1c-116">For code and metadata: /<DevOps project name>/Trunk/Main/Metadata</span></span>
 - <span data-ttu-id="adf1c-117">Visual Studio プロジェクトおよびソリューション ファイル: /<DevOps project name>/Trunk/Main/Projects</span><span class="sxs-lookup"><span data-stu-id="adf1c-117">For Visual Studio project and solution files: /<DevOps project name>/Trunk/Main/Projects</span></span>
 
 <span data-ttu-id="adf1c-118">新しいフォルダーは、Azure DevOps Web インターフェイスの **リポジトリ** で直接作成できます。</span><span class="sxs-lookup"><span data-stu-id="adf1c-118">You can create new folders directly in the Azure DevOps web interface under **Repos**.</span></span>
 
 
> [!NOTE]
> - <span data-ttu-id="adf1c-119">フォルダー名は大文字と小文字を区別していて、つまり、メインおよびメインでない、またはコードのアップグレード サービスはフォルダーを認識しません。</span><span class="sxs-lookup"><span data-stu-id="adf1c-119">Folder names are case sensitive, that is, you must use Main and not MAIN, or the code upgrade service will not recognize the folder.</span></span>
> - <span data-ttu-id="adf1c-120">Azure DevOps プロジェクトは、既定で Git バージョン管理を使用します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-120">Azure DevOps projects use Git version control by default.</span></span> <span data-ttu-id="adf1c-121">TFVC リポジトリを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="adf1c-121">You will need to add a TFVC repository.</span></span>
>     1. <span data-ttu-id="adf1c-122">プロジェクト設定へ移動し、リポジトリに移動します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-122">Go to Project settings, then Repositories.</span></span>
>     2. <span data-ttu-id="adf1c-123">[新しいリポジトリ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-123">Select New repository.</span></span>
>     3. <span data-ttu-id="adf1c-124">[種類] フィールドで [TFVC] を選択し、[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="adf1c-124">In the Type field, select TFVC, and then click Create.</span></span>


### <a name="create-a-personal-access-token"></a><span data-ttu-id="adf1c-125">個人用アクセス トークンを作成する</span><span class="sxs-lookup"><span data-stu-id="adf1c-125">Create a personal access token</span></span>

<span data-ttu-id="adf1c-126">Azure DevOps プロジェクトに接続するために、LCS は個人用アクセス トークンを使用して認証されます。</span><span class="sxs-lookup"><span data-stu-id="adf1c-126">To connect to an Azure DevOps project, LCS is authenticated using a personal access token.</span></span> <span data-ttu-id="adf1c-127">Azure DevOps で個人用アクセス トークンを作成するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="adf1c-127">Use the following steps to create a personal access token in Azure DevOps.</span></span> <span data-ttu-id="adf1c-128">LCS プロジェクトを Azure DevOps プロジェクトへ接続できるように構成する場合、このセクションを省略できます。</span><span class="sxs-lookup"><span data-stu-id="adf1c-128">If you have already configured your LCS project to connect to your Azure DevOps project, you can skip this section.</span></span>

1. <span data-ttu-id="adf1c-129">visualstudio.com にログインし、Azure DevOps プロジェクトを見つけます。</span><span class="sxs-lookup"><span data-stu-id="adf1c-129">Sign in to visualstudio.com and locate your Azure DevOps project.</span></span>
2. <span data-ttu-id="adf1c-130">右上隅で、名前をポイントするとメニューが表示され、**セキュリティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-130">In the top-right corner, hover over your name, a menu appears, select **Security**.</span></span>
3. <span data-ttu-id="adf1c-131">**追加** を選択して、新しい個人用アクセス トークンを作成し、名前を付けて、トークンが使用できる期間を入力します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-131">Select **Add** to create a new personal access token, give it a name, and then enter the amount of time that you want the token to last for.</span></span> <span data-ttu-id="adf1c-132">**トークンの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-132">Select **Create Token**.</span></span> 

   <span data-ttu-id="adf1c-133">[![コード アップグレードのトークンの作成](./media/codeupgrademaketoken.png)](./media/codeupgrademaketoken.png)</span><span class="sxs-lookup"><span data-stu-id="adf1c-133">[![Code upgrade create token](./media/codeupgrademaketoken.png)](./media/codeupgrademaketoken.png)</span></span>

4. <span data-ttu-id="adf1c-134">トークンをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="adf1c-134">Copy the token to your clipboard.</span></span> <span data-ttu-id="adf1c-135">このステップが完了したら、トークンの詳細情報を見つけることはできません。したがって、このページから移動する前に、かならずトークンをコピーしてください。</span><span class="sxs-lookup"><span data-stu-id="adf1c-135">You will not be able to find the token details after this step is completed, so be sure that you have copied the token before navigating away from this page.</span></span>

### <a name="configure-your-lifecycle-services-project-to-connect-to-azure-devops"></a><span data-ttu-id="adf1c-136">Lifecycle Services プロジェクトをコンフィギュレーションして Azure DevOps に接続する</span><span class="sxs-lookup"><span data-stu-id="adf1c-136">Configure your Lifecycle Services project to connect to Azure DevOps</span></span>

1. <span data-ttu-id="adf1c-137">LCS プロジェクトで、**プロジェクト設定** タイルに移動し、**Visual Studio Team Services** を選択してから、**Visual Studio Team Services の設定** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-137">In your LCS project, go to the **Project settings** tile, select **Visual Studio Team Services**, and then select the **Setup Visual Studio Team Services** button.</span></span> <span data-ttu-id="adf1c-138">この構成は多くの LCS ツールで必要になります。すでに Azure DevOps プロジェクトに接続するように LCS を設定している場合は、このセクションをスキップできます。</span><span class="sxs-lookup"><span data-stu-id="adf1c-138">This configuration is needed by many LCS tools, if you have already configured LCS to connect to your Azure DevOps project, you can skip this section.</span></span> 


   <span data-ttu-id="adf1c-139">[![LCS VSTS の設定](./media/lcs_vsts_setup.png)](./media/lcs_vsts_setup.png)</span><span class="sxs-lookup"><span data-stu-id="adf1c-139">[![LCS VSTS setup](./media/lcs_vsts_setup.png)](./media/lcs_vsts_setup.png)</span></span>

2. <span data-ttu-id="adf1c-140">Azure DevOps 組織のルート URL および以前に作成したアクセス トークンを入力し、**続行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-140">Enter the root URL for your Azure DevOps organization and the access token created earlier, and then select **Continue**.</span></span>

   <span data-ttu-id="adf1c-141">[![LCS トークン](./media/lcstoken.png)](./media/lcstoken.png)</span><span class="sxs-lookup"><span data-stu-id="adf1c-141">[![LCS token](./media/lcstoken.png)](./media/lcstoken.png)</span></span>

3. <span data-ttu-id="adf1c-142">接続する Azure DevOps 組織内のプロジェクトを選択し、**続行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-142">Select the project within your Azure DevOps organization that you want to connect to, and select **Continue**.</span></span> 
   
   <span data-ttu-id="adf1c-143">[![LCS がプロジェクトを選択](./media/lcs_selectproject.png)](./media/lcs_selectproject.png)</span><span class="sxs-lookup"><span data-stu-id="adf1c-143">[![LCS select project](./media/lcs_selectproject.png)](./media/lcs_selectproject.png)</span></span>

4. <span data-ttu-id="adf1c-144">**確認および保存** ページで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-144">On the **Review and save** page, select **Save**.</span></span>

### <a name="create-an-ax7version-file"></a><span data-ttu-id="adf1c-145">ax7.version ファイルを作成します</span><span class="sxs-lookup"><span data-stu-id="adf1c-145">Create an ax7.version file</span></span>

> [!NOTE]
> <span data-ttu-id="adf1c-146">AX 2012 から移行する場合は、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="adf1c-146">If you are migrating from AX 2012, you can skip this step.</span></span>

<span data-ttu-id="adf1c-147">LCS のコードのアップグレード タイルは、移行元のバージョンを自動的に検出します。ソース管理のメイン フォルダの ax7.version ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="adf1c-147">The code upgrade tile in LCS automatically finds the version that you are migrating from, by reading the ax7.version file under the Main folder in your source control.</span></span> <span data-ttu-id="adf1c-148">以下に示すように、Visual Studio または Azure DevOps Web ポータルを通じて、このファイルを手動で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="adf1c-148">You must create this file manually, either in Visual Studio or through the Azure DevOps web portal, as shown below.</span></span> <span data-ttu-id="adf1c-149">Dynamics AX 2012 R3 またはそれ以前のバージョンからコードを移行する場合、このファイルは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="adf1c-149">This file is not needed if you are migrating your code from Dynamics AX 2012 R3 or an earlier version.</span></span> <span data-ttu-id="adf1c-150">ここに入力するバージョン番号は、アプリケーションのバージョン (プラットフォームのバージョンではない) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="adf1c-150">The version number entered here must be the application version (not the platform version).</span></span> <span data-ttu-id="adf1c-151">このファイルに無効なバージョン番号を入力するとしてのコード アップグレードの実行に失敗する可能性があるため、ここには必ず正しいバージョン番号を入力してください。</span><span class="sxs-lookup"><span data-stu-id="adf1c-151">Take care to enter the correct version number here as entering an incorrect version number in this file may cause your code upgrade run to fail.</span></span>

<span data-ttu-id="adf1c-152">[![ax7 バージョン ファイル](./media/ax7_versionfile.png)](./media/ax7_versionfile.png)</span><span class="sxs-lookup"><span data-stu-id="adf1c-152">[![ax7 version file](./media/ax7_versionfile.png)](./media/ax7_versionfile.png)</span></span> 

<span data-ttu-id="adf1c-153">どのアプリケーション バージョンを持っているか識別する方法の詳細については、[Microsoft Dynamics AX ビルド番号の概要](https://blogs.msdn.microsoft.com/axsupport/2012/03/29/overview-of-microsoft-dynamics-ax-build-numbers/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adf1c-153">For more information about how to identify which application version you have, see [Overview of Microsoft Dynamics AX build numbers](https://blogs.msdn.microsoft.com/axsupport/2012/03/29/overview-of-microsoft-dynamics-ax-build-numbers/).</span></span>

### <a name="execute-the-code-upgrade-tile"></a><span data-ttu-id="adf1c-154">コード アップグレード タイルを実行</span><span class="sxs-lookup"><span data-stu-id="adf1c-154">Execute the code upgrade tile</span></span>

1. <span data-ttu-id="adf1c-155">LCS プロジェクトで、**コードのアップグレード** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-155">In your LCS project, select the **Code upgrade** tile.</span></span> 

   <span data-ttu-id="adf1c-156">[![コード アップグレード タイル](./media/codeupgradetile.png)](./media/codeupgradetile.png)</span><span class="sxs-lookup"><span data-stu-id="adf1c-156">[![Code upgrade tile](./media/codeupgradetile.png)](./media/codeupgradetile.png)</span></span>

2. <span data-ttu-id="adf1c-157">画面の左下隅で、**追加** を選択してから名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-157">In the bottom-left corner of the screen, select **Add**, and then enter a name and description.</span></span> <span data-ttu-id="adf1c-158">アップグレード元のバージョンとして Microsoft Dynamics AX 7 を選択し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-158">Select the version you are upgrading from as Microsoft Dynamics AX 7, and then select **Create**.</span></span>
   -   <span data-ttu-id="adf1c-159">Dynamics AX 2012 R3 からコードをアップグレードする場合は、アップグレード元のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-159">If you are upgrading your code from Dynamics AX 2012 R3, select the version you are upgrading from.</span></span> <span data-ttu-id="adf1c-160">圧縮バージョンの Dynamics AX 2012 R3 モデル ストア ファイルをアップロードするように要求されます。</span><span class="sxs-lookup"><span data-stu-id="adf1c-160">You will be prompted to upload a zipped version of your Dynamics AX 2012 R3 model store file.</span></span>
   -   <span data-ttu-id="adf1c-161">**見積のみ** チェック ボックスがオンになっている場合、ツールはレポートのみを生成し、チェックインや Azure DevOps の新しいコード分岐の作成を行いません。</span><span class="sxs-lookup"><span data-stu-id="adf1c-161">If the **Estimation Only** check box is selected, the tool only generates a report and does not check in or create a new code branch in Azure DevOps for you.</span></span> <span data-ttu-id="adf1c-162">実際のアップグレードをコミットする前に、アップグレードに必要な作業の潜在的なサイズを評価する場合、このオプションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="adf1c-162">You should use this option if you want to evaluate the potential size of the work involved in upgrading before you commit to the actual upgrade.</span></span>

   <span data-ttu-id="adf1c-163">[![新規コード ブランチ](./media/codeupgrade_new.png)](./media/codeupgrade_new.png)</span><span class="sxs-lookup"><span data-stu-id="adf1c-163">[![New code branch](./media/codeupgrade_new.png)](./media/codeupgrade_new.png)</span></span>

3. <span data-ttu-id="adf1c-164">右下にある **コードの分析** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-164">Select **Analyze code** in the bottom-right corner.</span></span> <span data-ttu-id="adf1c-165">コードのアップグレード プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="adf1c-165">The code upgrade process will start.</span></span> <span data-ttu-id="adf1c-166">このプロセスには、大規模なソリューションが完了するまでに通常 40 分かかります。</span><span class="sxs-lookup"><span data-stu-id="adf1c-166">This process typically takes 40 minutes for a large solution to complete.</span></span> <span data-ttu-id="adf1c-167">完了したら、LCS の **コードのアップグレード** タイルに戻り、結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-167">When complete, return to the **Code upgrade** tile in LCS to view the results.</span></span>
4. <span data-ttu-id="adf1c-168">コードのアップグレード サービスは、新しいブランチを作成し、アップグレードされたコードを Azure DevOps プロジェクトにチェックインします。</span><span class="sxs-lookup"><span data-stu-id="adf1c-168">The code upgrade service creates a new branch and checks in the upgraded code to your Azure DevOps project.</span></span> <span data-ttu-id="adf1c-169">アップグレード プロセスが完了した後、コードは **リリース** フォルダ下の新しいブランチに存在します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-169">After the upgrade process is complete, your code will exist in a new branch under the **Releases** folder.</span></span> <span data-ttu-id="adf1c-170">分岐名の後には、アップグレードの日時が付いています。</span><span class="sxs-lookup"><span data-stu-id="adf1c-170">The branch name is suffixed with the date and time of the upgrade.</span></span> 

   <span data-ttu-id="adf1c-171">[![コード アップグレード ブランチ](./media/codeupgradebranch-300x192.png)](./media/codeupgradebranch.png)</span><span class="sxs-lookup"><span data-stu-id="adf1c-171">[![Code upgrade branch](./media/codeupgradebranch-300x192.png)](./media/codeupgradebranch.png)</span></span>

### <a name="merge-releases-back-into-trunkmain"></a><span data-ttu-id="adf1c-172">リリースを Trunk\\Main にマージ</span><span class="sxs-lookup"><span data-stu-id="adf1c-172">Merge Releases back into Trunk\\Main</span></span>

<span data-ttu-id="adf1c-173">リリース\\\<version number\> のアップグレードされたコードが正常にコンパイルされ、コード移行とテストを完了したら、このブランチをトランク\\メインにマージする準備が整います。</span><span class="sxs-lookup"><span data-stu-id="adf1c-173">Once the upgraded code in Releases\\\<version number\> compiles successfully and you have completed your code migration and testing, you are ready to merge this branch back into Trunk\\Main.</span></span> <span data-ttu-id="adf1c-174">マージするには、Visual Studio の開発環境で、ソース管理エクスプローラー ウィンドウを開き、**リリース\\\<version number\>** のブランチを右クリックし、コンテキスト メニューで **分岐とマージ** に進み、サブ メニューで **マージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adf1c-174">To merge, on your development environment in Visual Studio, open the Source control explorer pane then right-click on the **Releases\\\<version number\>** branch, and in the context menu go to **Branching and Merging**, and then on the submenu select **Merge**.</span></span>

<span data-ttu-id="adf1c-175">[![リリース ブランチのマージ](./media/MergeReleasesBranch.PNG)](./media/MergeReleasesBranch.PNG)</span><span class="sxs-lookup"><span data-stu-id="adf1c-175">[![Merge release branch](./media/MergeReleasesBranch.PNG)](./media/MergeReleasesBranch.PNG)</span></span>

<span data-ttu-id="adf1c-176">[ソース管理マージ ウィザード](https://www.visualstudio.com/docs/tfvc/merge-folders-files#sourcecontrolwizard) が開かれ、リリース\\\<version number\> ブランチを トランク\\メインにマージする手順が示されます。</span><span class="sxs-lookup"><span data-stu-id="adf1c-176">The [Source Control Merge Wizard](https://www.visualstudio.com/docs/tfvc/merge-folders-files#sourcecontrolwizard) opens, which guides you through merging the Releases\\\<version number\> branch back into Trunk\\Main.</span></span>

