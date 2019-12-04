---
title: 開発環境でのメタデータの修正プログラムのインストール
description: このトピックでは、開発環境にアプリケーション メタデータの修正プログラムをインストールする方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 09/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 79822
ms.assetid: 9b132253-1748-4b71-b128-c4b9d3a311ae
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143886e342e1c901a7cf2b87ef6deec7dc1515fe
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812047"
---
# <a name="install-metadata-hotfixes-in-development-environments"></a><span data-ttu-id="c0f5a-103">開発環境でのメタデータの修正プログラムのインストール</span><span class="sxs-lookup"><span data-stu-id="c0f5a-103">Install metadata hotfixes in development environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0f5a-104">このトピックでは、開発環境にアプリケーション メタデータの修正プログラムをインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-104">This topic will guide you through installing an Application Metadata hotfix on your development environment.</span></span>

<span data-ttu-id="c0f5a-105">メタデータ修正プログラムのパッケージには、開発環境でのモデル要素 (XML ファイル) への変更 (メタデータまたは X++ ソース コード) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-105">A metadata hotfix package contains changes (metadata or X++ source code) to model elements (XML files) in your development environment.</span></span> <span data-ttu-id="c0f5a-106">修正プログラムは、新しいモデルの要素を含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-106">A hotfix can also contain new model elements.</span></span> <span data-ttu-id="c0f5a-107">メタデータ修正プログラムのパッケージは、SCDP ファイルの形式です。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-107">A metadata hotfix package is in the form of an SCDP file.</span></span> <span data-ttu-id="c0f5a-108">この記事では、メタデータ修正プログラム パッケージのインストール プロセスについて説明し、同じプロジェクトで作業している他の開発者とパッケージを共有する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-108">This article describes the process for installing a metadata hotfix package and explains how to share the package with other developers who are working on the same project.</span></span>

## <a name="overall-flow"></a><span data-ttu-id="c0f5a-109">全体的な流れ</span><span class="sxs-lookup"><span data-stu-id="c0f5a-109">Overall flow</span></span>
<span data-ttu-id="c0f5a-110">次の図は、全体的なフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-110">The following diagram shows the overall flow.</span></span> 

<span data-ttu-id="c0f5a-111">[![メタデータ修正プログラムのパッケージをインストールするためのプロセス](./media/configureinstallhotfix-1.png)](./media/configureinstallhotfix-1.png)</span><span class="sxs-lookup"><span data-stu-id="c0f5a-111">[![Process for installing a metadata hotfix package](./media/configureinstallhotfix-1.png)](./media/configureinstallhotfix-1.png)</span></span>

## <a name="download-the-hotfix-from-lcs"></a><span data-ttu-id="c0f5a-112">修正プログラムを LCS からダウンロード</span><span class="sxs-lookup"><span data-stu-id="c0f5a-112">Download the hotfix from LCS</span></span>
<span data-ttu-id="c0f5a-113">修正プログラムをダウンロードする方法の詳細については、 [Lifecycle Services (LCS) から更新プログラムのダウンロード](download-hotfix-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-113">For instructions about how to download a hotfix, see [Download updates from Lifecycle Services (LCS)](download-hotfix-lcs.md).</span></span> <span data-ttu-id="c0f5a-114">ZIP ファイルをダウンロードした後は、そこから SCDP メタデータの修正プログラム パッケージを抽出し、ローカル フォルダーに保存できます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-114">After you download the zip file, extract the SCDP metadata hotfix package from it, and put it in a local folder.</span></span>

## <a name="install-the-hotfix"></a><span data-ttu-id="c0f5a-115">修正プログラムのインストール</span><span class="sxs-lookup"><span data-stu-id="c0f5a-115">Install the hotfix</span></span>
### <a name="before-you-begin"></a><span data-ttu-id="c0f5a-116">準備</span><span class="sxs-lookup"><span data-stu-id="c0f5a-116">Before you begin</span></span>

-   <span data-ttu-id="c0f5a-117">このトピックでは、あなたのパッケージ フォルダが c:\\AOSService\\PackagesLocalDirectory\\Bin にあることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-117">This topic assumes that your packages folder is located at c:\\AOSService\\PackagesLocalDirectory\\Bin.</span></span> <span data-ttu-id="c0f5a-118">いくつかの仮想マシン (Vm) では、c:\\Packages, i:\\AOSService\\PackagesLocalDirectory\\Bin または k:\\AOSService\\PackagesLocalDirectory\\Bin に表示されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-118">On some virtual machines (VMs), it might be located at c:\\Packages, i:\\AOSService\\PackagesLocalDirectory\\Bin, or k:\\AOSService\\PackagesLocalDirectory\\Bin.</span></span>
-   <span data-ttu-id="c0f5a-119">Microsoft Azure DevOps または別のソース管理システムを使用していない場合は、(メタデータ ストアとも呼ばれる) パッケージ フォルダーのバックアップを作成します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-119">If you're not using Microsoft Azure DevOps or another source control system, create a backup of your packages folder (which is also known as the metadata store).</span></span> <span data-ttu-id="c0f5a-120">Azure DevOps を使用していないときに、開発を実行することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-120">We don't recommend that you do development unless you use Azure DevOps.</span></span>
-   <span data-ttu-id="c0f5a-121">Azure DevOps または Microsoft Team Foundation Server (TFS) バージョン コントロールがない場合、現在のワークスペースの**保留中の変更**一覧にファイルがないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-121">If you have Azure DevOps or Microsoft Team Foundation Server (TFS) version control, make sure that there are no files in the **Pending Changes** list of your current workspace.</span></span> <span data-ttu-id="c0f5a-122">保留中の変更がある場合は、メタデータの修正プログラムをインストールする前に、それらを送信するかまたは棚に置くことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-122">If you have pending changes, we recommend that you submit them or shelve them before you install the metadata hotfix.</span></span>

### <a name="install-the-metadata-hotfix-package"></a><span data-ttu-id="c0f5a-123">メタデータ修正プログラム パッケージのインストール</span><span class="sxs-lookup"><span data-stu-id="c0f5a-123">Install the metadata hotfix package</span></span>

<span data-ttu-id="c0f5a-124">メタデータ修正プログラムのインストールを起動するには、コマンド プロンプトから SCDPBundleInstall.exe ユーティリティを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-124">To invoke the installation of the metadata hotfix, you can call the SCDPBundleInstall.exe utility from a command prompt.</span></span> <span data-ttu-id="c0f5a-125">SCDPBundleInstall.exe は、パッケージの bin フォルダーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-125">SCDPBundleInstall.exe is located in your packages bin folder.</span></span>

#### <a name="without-version-control-not-recommended"></a><span data-ttu-id="c0f5a-126">バージョン コントロールなし (非推奨)</span><span class="sxs-lookup"><span data-stu-id="c0f5a-126">Without version control (not recommended)</span></span>

<span data-ttu-id="c0f5a-127">ソース管理の Azure DevOps または TFS を使用していない場合は、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-127">If you're not using Azure DevOps or TFS for source control, use the following command.</span></span>

    SCDPBundleInstall.exe -install -packagepath=<scdp file containing the hotfix> -metadatastorepath=<metadata packages root folder>

#### <a name="with-version-control-recommended"></a><span data-ttu-id="c0f5a-128">バージョン管理の使用 (推奨)</span><span class="sxs-lookup"><span data-stu-id="c0f5a-128">With version control (recommended)</span></span>

<span data-ttu-id="c0f5a-129">ソース管理に Azure DevOps または TFS を使用している場合は、次の手順を実行します。以下のコマンドを使用して、修正プログラム パッケージのインストールを**準備**します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-129">If you're using Azure DevOps or TFS for source control, follow the steps below: **Prepare** the installation of the hotfix package using the command below.</span></span> <span data-ttu-id="c0f5a-130">この手順は、プラットフォーム更新プログラム 2 (2016 年 8 月) よりも古いプラットフォームを使用している場合は利用できません)</span><span class="sxs-lookup"><span data-stu-id="c0f5a-130">This step is not available if you are using a platform that is older than Platform update 2 (August 2016))</span></span>

    SCDPBundleInstall.exe -prepare -packagepath=<scdp file containing the hotfixes> -metadatastorepath=<metadata packages root folder> -tfsworkspacepath=<path of local workspace folder> -tfsprojecturi=<URI of the Azure DevOps or TFS project collection>

<span data-ttu-id="c0f5a-131">これにより、環境内のすべての既存ファイルの変更セットが作成され、修正プログラム パッケージによって変更されます。この場合、prepare コマンドによって修正プログラムはインストールされません。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-131">This will create a changeset of all the existing files on your environment that will be modified by the hotfix package, the prepare command will not install the hotfixes.</span></span> <span data-ttu-id="c0f5a-132">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-132">Here is an example.</span></span>

    SCDPBundleInstall.exe -prepare -packagepath=c:\temp\hotfixbundle1234.axscdppkg -metadatastorepath= c:\AOSService\PackagesLocalDirectory -tfsworkspacepath= c:\AOSService\PackagesLocalDirectory -tfsprojecturi=https://myaccount.visualstudio.com/defaultcollection

<span data-ttu-id="c0f5a-133">保留中の変更を**チェックイン**して、バージョン管理システムでこれらのファイルのバックアップを作成します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-133">**Check-in** your pending changes to create a backup of these files in your version control system.</span></span> <span data-ttu-id="c0f5a-134">これにより、必要に応じて修正プログラムをロールバックすることができます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-134">This will enable rolling back the hotfixes if needed.</span></span> <span data-ttu-id="c0f5a-135">次のコマンドを使用して修正プログラムを**インストール**します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-135">**Install** the hotfix package using the command below.</span></span>

    SCDPBundleInstall.exe -install -packagepath=<scdp file containing the hotfixes> -metadatastorepath=<metadata packages root folder> -tfsworkspacepath=<path of local workspace folder> -tfsprojecturi=<URI of the Azure DevOps or TFS project collection>

<span data-ttu-id="c0f5a-136">プラットフォーム更新プログラム 2 (2016 年 8 月) よりも古いプラットフォームを使用している場合は、**-install** オプションを指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-136">If you are using a platform that is older than Platform update 2 (August 2016), you do not need to specify the **-install** option.</span></span> <span data-ttu-id="c0f5a-137">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-137">Here is an example.</span></span>

    SCDPBundleInstall.exe -install -packagepath=c:\temp\hotfixbundle1234.axscdppkg -metadatastorepath= c:\AOSService\PackagesLocalDirectory -tfsworkspacepath= c:\AOSService\PackagesLocalDirectory -tfsprojecturi=https://myaccount.visualstudio.com/defaultcollection

<span data-ttu-id="c0f5a-138">Azure DevOps/TFS パラメーターを使用して、パッケージによって修正されたファイルを、チーム エクスプ ローラー内の保留中の変更の一覧に追加できます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-138">Azure DevOps/TFS parameters let you add the files that are modified by the package to your list of pending changes in Team Explorer.</span></span>

### <a name="required-parameters"></a><span data-ttu-id="c0f5a-139">必須パラメーター</span><span class="sxs-lookup"><span data-stu-id="c0f5a-139">Required parameters</span></span>

    /packagepath=[Path of the local scdp file containing the hotfixes downloaded from Lifecycle Service (LCS)]

    /metadatastorepath=[Path of the local metadata store folder, such as c:\AOSService\PackagesLocalDirectory]

### <a name="tfs-parameters"></a><span data-ttu-id="c0f5a-140">TFS パラメーター</span><span class="sxs-lookup"><span data-stu-id="c0f5a-140">TFS parameters</span></span>

<span data-ttu-id="c0f5a-141">ソース管理に Azure DevOps または TFS を使用している場合は、次の 2 つのパラメーターを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-141">If you're using Azure DevOps or TFS for source control, you should specify the following two parameters.</span></span>

    /tfsprojecturi=[URI of the TFS Project to connect to]

    /tfsworkspacepath=[Path of the local workspace, usually equal to the metadatastorepath]

<span data-ttu-id="c0f5a-142">インストール コマンドが呼び出されると、パッケージのインストール プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-142">After the install command is invoked, the package installation process begins.</span></span> <span data-ttu-id="c0f5a-143">インストール プロセスの一環として、メタデータ ストア フォルダ内の一部の XML ファイルはそれ自体の修正で加えられた変更を反映するように更新されます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-143">As part of the installation process, some XML files in your metadata store folder will be updated to reflect the changes that were made in the fix itself.</span></span> <span data-ttu-id="c0f5a-144">Azure DevOps または TFS を使用している場合、これらのファイルがチーム エクスプローラーの**保留中の変更**ウィンドウに含まれた変更のリストに追加されます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-144">If you’re using Azure DevOps or TFS, these files will be added to the list of included changes in the **Pending Changes** window in Team Explorer.</span></span> 

<span data-ttu-id="c0f5a-145">[![保留中の変更ウィンドウに含まれている変更の一覧](./media/configureinstallhotfix-2.png)](./media/configureinstallhotfix-2.png)</span><span class="sxs-lookup"><span data-stu-id="c0f5a-145">[![List of included changes in the Pending Changes window](./media/configureinstallhotfix-2.png)](./media/configureinstallhotfix-2.png)</span></span>

## <a name="resolve-conflicts-that-are-generated-by-the-installation-of-the-hotfix"></a><span data-ttu-id="c0f5a-146">修正プログラムのインストールによって生成された競合を解決</span><span class="sxs-lookup"><span data-stu-id="c0f5a-146">Resolve conflicts that are generated by the installation of the hotfix</span></span>
<span data-ttu-id="c0f5a-147">場合によっては、メタデータ修正プログラム パッケージに、上位モデルでカスタマイズされていたオブジェクトへの変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-147">Sometimes, a metadata hotfix package contains changes to objects that have been customized in higher-layer models.</span></span> <span data-ttu-id="c0f5a-148">この場合、インストール プロセスは修正プログラムのインストール後に解決する必要がある競合を自動的に生成します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-148">In this case, the installation process automatically generates conflicts that must be resolved after the hotfix has been installed.</span></span> <span data-ttu-id="c0f5a-149">開発ツールを使用すると、競合しているすべての品目をグループ化するプロジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-149">The development tools let you create a project that groups all items that have conflicts.</span></span> <span data-ttu-id="c0f5a-150">たとえば、VendTable フォームをカスタマイズするアプリケーション スイート パッケージに VAR レイヤー モデルがあり、SYS レイヤ モデルで VendTable フォームを変更する修正プログラムをインストールする場合、VAR レイヤ モデルで競合が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-150">For example, if you have a VAR layer model in the Application Suite package that customizes the VendTable form, and you install a hotfix that modifies the VendTable form in the Sys layer model, conflicts might occur in your VAR layer model.</span></span>

1.  <span data-ttu-id="c0f5a-151">**Dynamics 365** &gt; **アドイン** &gt; **競合からプロジェクトを作成する**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-151">Click **Dynamics 365** &gt; **Addins** &gt; **Create project from conflicts**.</span></span>
2.  <span data-ttu-id="c0f5a-152">ダイアログ ボックスで、モデルを選択して競合を確認します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-152">In the dialog box, select a model to check for conflicts.</span></span>
3.  <span data-ttu-id="c0f5a-153">**プロジェクトの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-153">Click **Create project**.</span></span> <span data-ttu-id="c0f5a-154">修正プログラムが適用された後に競合していることが見つかった選択しているモデルの要素のみを含むプロジェクトが生成されます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-154">A project is generated that contains only those elements in the selected model that were found to have conflicts after the hotfix was applied.</span></span>
4.  <span data-ttu-id="c0f5a-155">競合する要素のデザイナーを開いて、表示されたツールを使って競合を表示し、解決します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-155">Open the designer for the conflicting element to view conflicts, and resolve them by using the tools that are provided.</span></span>

<!--The Office Mix at <https://mix.office.com/watch/1rl75ei2cs6d7> provides an introduction to the conflict resolution tools in the development environment.-->

## <a name="build-and-test-on-a-local-vm"></a><span data-ttu-id="c0f5a-156">ローカル VM のビルドおよびテスト</span><span class="sxs-lookup"><span data-stu-id="c0f5a-156">Build and test on a local VM</span></span>
<span data-ttu-id="c0f5a-157">修正プログラムの影響を受けるすべてのモデルをビルドし、アプリケーションをテストします。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-157">Build all models that are affected by the hotfix, and test your application.</span></span>

## <a name="check-pending-changes-in-to-version-control"></a><span data-ttu-id="c0f5a-158">バージョン管理の保留中の変更のチェック</span><span class="sxs-lookup"><span data-stu-id="c0f5a-158">Check pending changes in to version control</span></span>
<span data-ttu-id="c0f5a-159">この更新プログラムに関連するすべての変更で問題がなければ、Microsoft Visual Studio のチーム エクスプローラーを使用して、保留中の変更を Azure DevOps にチェックインします。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-159">When you're satisfied with all changes that are related to this update, check in your pending changes to Azure DevOps by using Team Explorer in Microsoft Visual Studio.</span></span> <span data-ttu-id="c0f5a-160">**コメント**フィールドにコメントを入力し、**チェック イン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-160">Enter a comment in the **Comment** field, and then click **Check In**.</span></span> <span data-ttu-id="c0f5a-161">ソース コード リポジトリには、変更の履歴が維持されます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-161">A history of the changes is preserved in your source code repository.</span></span> 

> [!NOTE]
> <span data-ttu-id="c0f5a-162">ビルドとテストの自動化にビルド環境を使用する場合、ビルドの自動化プロセスは、Azure DevOps プロジェクトにあるメタデータの修正プログラム ファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-162">If you use a build environment for build and test automation, the build automation process can build metadata hotfix files are in your Azure DevOps project.</span></span> <span data-ttu-id="c0f5a-163">それが属しているモデルの記述子ファイルがバージョン管理にチェックインする場合にのみ、修正プログラムを構築できます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-163">A hotfix can be built only if the descriptor file of the model that it belongs to is checked in to version control.</span></span> <span data-ttu-id="c0f5a-164">たとえば、修正プログラムのインストール プロセスがディレクトリ モデル (このファイルは保留中の変更の一覧に表示されます) が属しているファイルを変更した場合、ディレクトリ モデル (c:\\AOSService\\PackagesLocalDirectory\\ディレクトリ\\記述子\\Directory.xml) の記述子ファイルが既に Azure DevOps プロジェクトにチェックインされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-164">For example, if the hotfix installation process modified a file that belongs to the Directory model (this file will appear in your list of pending changes), make sure that the descriptor file of the Directory model (c:\\AOSService\\PackagesLocalDirectory\\Directory\\Descriptor\\Directory.xml) is already checked in to your Azure DevOps project.</span></span> <span data-ttu-id="c0f5a-165">チェックインされていない場合は、ソース管理エクスプローラーを使用してチェックインする前に、追加保留中の変更の一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-165">If it isn't checked in, manually add it to your list of pending changes before you check in by using Source Control Explorer.</span></span> 

<span data-ttu-id="c0f5a-166">[![保留中の変更のリストに記述子ファイルを手動で追加します](./media/configureinstallhotfix-8.png)](./media/configureinstallhotfix-8.png)</span><span class="sxs-lookup"><span data-stu-id="c0f5a-166">[![Manually adding the descriptor file to the list of pending changes](./media/configureinstallhotfix-8.png)](./media/configureinstallhotfix-8.png)</span></span>

## <a name="synchronize-other-development-vms"></a><span data-ttu-id="c0f5a-167">その他の開発 VM を同期</span><span class="sxs-lookup"><span data-stu-id="c0f5a-167">Synchronize other development VMs</span></span>
<span data-ttu-id="c0f5a-168">この記事で記載されているように、修正プログラムが開発 VM でインストールされた後、再インストール、競合の解決、同じ Azure DevOps プロジェクトに接続されている他の開発 VMでの検証をする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-168">After a hotfix has been installed on a development VM as described in this article, you don't have to reinstall, resolve conflicts, and validate on other development VMs that are connected to the same Azure DevOps project.</span></span> <span data-ttu-id="c0f5a-169">同じ Azure DevOps プロジェクトに接続されている開発者とテスターは、ローカル VM に変更を同期させてビルドするだけで済みます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-169">Developers and testers who are connected to the same Azure DevOps project can just synchronize the changes into their local VM and then build.</span></span>

## <a name="deploy"></a><span data-ttu-id="c0f5a-170">配置</span><span class="sxs-lookup"><span data-stu-id="c0f5a-170">Deploy</span></span>
<span data-ttu-id="c0f5a-171">開発環境にメタデータの修正プログラムを適用した後、競合を解決し、変更を検証したら、配置可能パッケージを作成しテスト環境またはサンドボックス環境に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-171">After you’ve applied a metadata hotfix to your development environment, resolved conflicts, and validated your changes, you must create a deployable package and apply your changes to your test or sandbox environment.</span></span> <span data-ttu-id="c0f5a-172">ビルドとテストの自動化にビルド インスタンスを使用すると、ビルド プロセスによって配置可能なパッケージが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-172">If you use a build instance for build and test automation, the build process will automatically create the deployable package for you.</span></span> <span data-ttu-id="c0f5a-173">詳細については、[配置可能パッケージの作成](../deployment/create-apply-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0f5a-173">For more information, see [Create deployable packages of models](../deployment/create-apply-deployable-package.md).</span></span>

