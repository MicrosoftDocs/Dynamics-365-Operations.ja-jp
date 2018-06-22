---
title: "Dynamics AX プラットフォームの 2016 年 8 月リリースへのアップグレード"
description: "このトピックでは、Microsoft Dynamics AX プラットフォームを Dynamics AX の 2016 年 8 月リリースにアップグレードする方法について説明します。"
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 125753
ms.assetid: 99af5334-d30e-4160-9504-881777e9d4ea
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 23bf98df09ca77ed1939541507f433638226f4ed
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="upgrade-the-dynamics-ax-platform-to-the-august-2016-release"></a><span data-ttu-id="10f42-103">Dynamics AX プラットフォームの 2016 年 8 月リリースへのアップグレード</span><span class="sxs-lookup"><span data-stu-id="10f42-103">Upgrade the Dynamics AX platform to the August 2016 release</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10f42-104">このトピックでは、Microsoft Dynamics AX プラットフォームを Dynamics AX の 2016 年 8 月リリースにアップグレードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="10f42-104">This topic explains how to upgrade your Microsoft Dynamics AX platform to the August 2016 release of Dynamics AX.</span></span>

<a name="overview"></a><span data-ttu-id="10f42-105">概要</span><span class="sxs-lookup"><span data-stu-id="10f42-105">Overview</span></span>
--------

<span data-ttu-id="10f42-106">**重要:** このトピックは、2016 年 8 月よりも前の、Microsoft Dynamics AX のリリースにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="10f42-106">**Important:** This topic applies only to Microsoft Dynamics AX releases prior to August 2016.</span></span> <span data-ttu-id="10f42-107">Microsoft Dynamics 365 for Finance and Operations 更新プログラムで、このトピックを参照してください: [Finance and Operations を最新のプラットフォーム更新プログラムに更新](../migration-upgrade/upgrade-latest-platform-update.md)</span><span class="sxs-lookup"><span data-stu-id="10f42-107">For Microsoft Dynamics 365 for Finance and Operations updates, see the topic: [Upgrade Finance and Operations to the latest platform update](../migration-upgrade/upgrade-latest-platform-update.md).</span></span> <span data-ttu-id="10f42-108">Microsoft Dynamics AX プラットフォームは、次のコンポーネントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="10f42-108">The Microsoft Dynamics AX platform consists of the following components:</span></span>

-   <span data-ttu-id="10f42-109">Application Object Server (AOS)、データ管理フレームワーク、レポートおよびビジネス インテリジェンス (BI) フレームワーク、開発ツール、および分析サービスなどの Dynamics AX プラットフォーム バイナリ</span><span class="sxs-lookup"><span data-stu-id="10f42-109">Dynamics AX platform binaries such as Application Object Server (AOS), the data management framework, the reporting and business intelligence (BI) framework, development tools, and analytics services</span></span>
-   <span data-ttu-id="10f42-110">次のアプリケーション オブジェクト ツリー (AOT) パッケージ。</span><span class="sxs-lookup"><span data-stu-id="10f42-110">The following Application Object Tree (AOT) packages:</span></span>
    -   <span data-ttu-id="10f42-111">アプリケーション プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="10f42-111">Application Platform</span></span>
    -   <span data-ttu-id="10f42-112">アプリケーション基準</span><span class="sxs-lookup"><span data-stu-id="10f42-112">Application Foundation</span></span>
    -   <span data-ttu-id="10f42-113">ディレクトリ</span><span class="sxs-lookup"><span data-stu-id="10f42-113">Directory</span></span>
    -   <span data-ttu-id="10f42-114">TestEssentials</span><span class="sxs-lookup"><span data-stu-id="10f42-114">TestEssentials</span></span>

<span data-ttu-id="10f42-115">**重要:** Dynamics AX のプラットフォームを新しいリリースに更新する場合は、Dynamics AX の実装はプラットフォームに属するどの AOT パッケージにもカスタマイズ (オーバーレイ) を行なうべきではありません。</span><span class="sxs-lookup"><span data-stu-id="10f42-115">**Important:** If you want to update the Dynamics AX platform to a new release, your Dynamics AX implementation should not have any customizations (overlayering) of any of the AOT packages that belong to the platform.</span></span> <span data-ttu-id="10f42-116">プラットフォーム パッケージをカスタマイズ**する**場合 (ソリューションに 1 つ以上のプラットフォーム パッケージに属しているモデルが含まれている場合) は、このトピックの最後に記載されている回避策を完了し、カスタマイズされたプラットフォーム パッケージがある Dynamics AX の実装のために図示され、説明されている総合プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="10f42-116">If you **do** customize platform packages (that is, if your solution contains models that belong to one or more of the platform packages), complete the workaround that is described at the end of this topic, and the overall process that is illustrated and described for Dynamics AX implementations that have customized platform packages.</span></span>

## <a name="overall-flow"></a><span data-ttu-id="10f42-117">全体的な流れ</span><span class="sxs-lookup"><span data-stu-id="10f42-117">Overall flow</span></span>
<span data-ttu-id="10f42-118">次の図は、Dynamics AX プラットフォームを最新の更新プログラムにアップグレードする 2 つのシナリオの異なるプロセス全体を示しています。</span><span class="sxs-lookup"><span data-stu-id="10f42-118">The following illustrations show the different overall process for two scenarios for upgrading the Dynamics AX platform to the latest update.</span></span>

### <a name="dynamics-ax-implementations-that-have-no-customization-of-the-platform"></a><span data-ttu-id="10f42-119">プラットフォームのカスタマイズがない実装の Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="10f42-119">Dynamics AX implementations that have no customization of the platform</span></span>

<span data-ttu-id="10f42-120">[![プラットフォームのカスタマイズがない実装のアップグレード プロセス](./media/flownocustomisations.jpg)](./media/flownocustomisations.jpg)</span><span class="sxs-lookup"><span data-stu-id="10f42-120">[![Upgrade process for implementations that have no customization of the platform](./media/flownocustomisations.jpg)](./media/flownocustomisations.jpg)</span></span>

### <a name="dynamics-ax-implementations-that-have-customized-platform-packages"></a><span data-ttu-id="10f42-121">プラットフォーム パッケージをカスタマイズした実装の Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="10f42-121">Dynamics AX implementations that have customized platform packages</span></span>

<span data-ttu-id="10f42-122">[![プラットフォーム パッケージをカスタマイズした実装のアップグレード プロセス](./media/flowwithcustomisations.jpg)](./media/flowwithcustomisations.jpg)</span><span class="sxs-lookup"><span data-stu-id="10f42-122">[![Upgrade process for implementations that have customized platform packages](./media/flowwithcustomisations.jpg)](./media/flowwithcustomisations.jpg)</span></span>

## <a name="import-the-platform-update-package"></a><span data-ttu-id="10f42-123">プラットフォーム更新プログラム パッケージのインポート</span><span class="sxs-lookup"><span data-stu-id="10f42-123">Import the platform update package</span></span>
<span data-ttu-id="10f42-124">プラットフォーム更新プログラム パッケージは、Microsoft によってリリースされ、Microsoft Lifecycle Services (LCS) の共有資産ライブラリからインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="10f42-124">Platform update packages are released by Microsoft and can be imported from the Shared Asset Library in Microsoft Lifecycle Services (LCS).</span></span> <span data-ttu-id="10f42-125">このパッケージの名前は、**Dynamics AX platform  2016 年 8 月リリース (更新プログラム 2)** です。</span><span class="sxs-lookup"><span data-stu-id="10f42-125">The package is named **Dynamics AX platform August 2016 release (Update 2).**</span></span> <span data-ttu-id="10f42-126">まだ済んでいない場合、次の手順に従って、**Dynamics AX プラットフォーム 2016 年 8 月リリース (更新プログラム 2)** パッケージをプロジェクトの資産ライブラリにインポートします。</span><span class="sxs-lookup"><span data-stu-id="10f42-126">If you haven't done so yet, import the **Dynamics AX platform August 2016 release (Update 2)** package to your project's asset library by following these steps:</span></span>

1. <span data-ttu-id="10f42-127">LCS プロジェクトの資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="10f42-127">Go to your LCS project's asset library.</span></span>
2. <span data-ttu-id="10f42-128">ソフトウェア配置可能パッケージ タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="10f42-128">Select the Software Deployable Package tab.</span></span>
3. <span data-ttu-id="10f42-129"><strong>インポートをクリックし、Dynamics AX プラットフォーム 2016 年 8 月リリース (更新プログラム 2) 共有パッケージ**を選択します**</strong>。[![importupgradepackage](./media/importupgradepackage.png)](./media/importupgradepackage.png)</span><span class="sxs-lookup"><span data-stu-id="10f42-129">Click <strong>Import **then select the **Dynamics AX platform August 2016 release (Update 2)</strong> shared package.[![importupgradepackage](./media/importupgradepackage.png)](./media/importupgradepackage.png)</span></span>

## <a name="how-to-apply-the-platform-upgrade-package"></a><span data-ttu-id="10f42-130">プラットフォーム更新プログラムパッケージを適用する方法</span><span class="sxs-lookup"><span data-stu-id="10f42-130">How to apply the platform upgrade package</span></span>
<span data-ttu-id="10f42-131">プロセスの観点では、プラットフォーム更新プログラム パッケージは、バイナリ修正プログラムの展開可能なパッケージに似ています。</span><span class="sxs-lookup"><span data-stu-id="10f42-131">From a process perspective, a platform upgrade package is similar to a binary hotfix deployable package.</span></span>

-   <span data-ttu-id="10f42-132">パッケージを開発環境またはビルド環境に適用するには、次のセクションの指示に従います。</span><span class="sxs-lookup"><span data-stu-id="10f42-132">To apply the package to your development or build environment, follow the instructions in the sections below.</span></span>
-   <span data-ttu-id="10f42-133">パッケージをデモ、第 2 層サンド ボックス、または実稼働環境に適用するには、[[展開可能パッケージの適用](../deployment/apply-deployable-package-system.md)] のトピックのバイナリ修正プログラムの指示に従います。</span><span class="sxs-lookup"><span data-stu-id="10f42-133">To apply the package to your demo, sandbox tier-2, or production environments, follow the instructions for a binary hotfix in the topic [Apply a Deployable package](../deployment/apply-deployable-package-system.md).</span></span>

## <a name="apply-the-platform-update-package-on-your-development-environment"></a><span data-ttu-id="10f42-134">開発環境にプラットフォーム更新プログラム パッケージを適用する</span><span class="sxs-lookup"><span data-stu-id="10f42-134">Apply the platform update package on your development environment</span></span>
### <a name="delete-any-platform-metadata-hotfixes-from-your-vsts-project"></a><span data-ttu-id="10f42-135">VSTS プロジェクトからプラットフォーム メタデータの修正プログラムを削除する</span><span class="sxs-lookup"><span data-stu-id="10f42-135">Delete any platform metadata hotfixes from your VSTS project</span></span>

<span data-ttu-id="10f42-136">新しいプラットフォーム更新プログラムをインストールする前に、Visual Studio Team Services (VSTS) ソース コントロール プロジェクトをクリーンアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="10f42-136">Before you install the new platform update, you need to clean up your Visual Studio Team Services (VSTS) source control project.</span></span> <span data-ttu-id="10f42-137">既存のプラットフォームにインストールされているすべての X++ またはメタデータの修正プログラムを削除します。</span><span class="sxs-lookup"><span data-stu-id="10f42-137">Remove any X++ or metadata hotfixes you have installed on your existing platform.</span></span> <span data-ttu-id="10f42-138">次の Microsoft モデルのいずれかの VSTS プロジェクトでチェックされている X++ またはメタデータの修正プログラムがある場合は、Visual Studio のソース管理エクスプローラーを使用してプロジェクトから削除します。</span><span class="sxs-lookup"><span data-stu-id="10f42-138">If you have any X++ or metadata hotfixes that are checked in your VSTS project for any of the following Microsoft models, delete them from your project using the Visual Studio Source Control Explorer.</span></span>

-   <span data-ttu-id="10f42-139">アプリケーション プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="10f42-139">Application Platform</span></span>
-   <span data-ttu-id="10f42-140">アプリケーション基準</span><span class="sxs-lookup"><span data-stu-id="10f42-140">Application Foundation</span></span>
-   <span data-ttu-id="10f42-141">ディレクトリ</span><span class="sxs-lookup"><span data-stu-id="10f42-141">Directory</span></span>
-   <span data-ttu-id="10f42-142">TestEssentials</span><span class="sxs-lookup"><span data-stu-id="10f42-142">TestEssentials</span></span>

<span data-ttu-id="10f42-143">これらの修正プログラムは、Microsoft モデルでこれらのモデルのチェックイン履歴を参照することにより見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="10f42-143">You can find these hotfixes by browsing the check-in history of these models Microsoft models.</span></span> <span data-ttu-id="10f42-144">たとえば、ソース管理エクスプローラーを使用して、フォルダー *TrunkMainMetadataApplicationFoundationApplicationFoundation* のチェックイン履歴を参照し、この Microsoft モデルでチェックされたすべての XML ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="10f42-144">For example, use Source Control Explorer to browse the check-in history of the folder *TrunkMainMetadataApplicationFoundationApplicationFoundation* and delete all XML files that have been checked in this Microsoft model.</span></span> <span data-ttu-id="10f42-145">[![CheckInHistory](./media/checkinhistory.png)](./media/checkinhistory.png)</span><span class="sxs-lookup"><span data-stu-id="10f42-145">[![CheckInHistory](./media/checkinhistory.png)](./media/checkinhistory.png)</span></span>

### <a name="install-the-deployable-package"></a><span data-ttu-id="10f42-146">配置可能パッケージのインストール</span><span class="sxs-lookup"><span data-stu-id="10f42-146">Install the deployable package</span></span>

1.  <span data-ttu-id="10f42-147">プラットフォーム更新パッケージ (AXPlatformUpdate.zip) を使用中の仮想マシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="10f42-147">Copy the platform update package (AXPlatformUpdate.zip) to your virtual machine.</span></span>
2.  <span data-ttu-id="10f42-148">コンテンツをローカル ディレクトリに解凍します。</span><span class="sxs-lookup"><span data-stu-id="10f42-148">Unzip the contents to a local directory.</span></span>
3.  <span data-ttu-id="10f42-149">アップグレードする環境のタイプに応じて、AOSService スクリプトの下の PlatformUpdatePackages.Config ファイルを開き、MetaPackage 値を変更します。</span><span class="sxs-lookup"><span data-stu-id="10f42-149">Depending on the type of environment that you're upgrading, open the PlatformUpdatePackages.Config file under AOSServiceScripts, and change the MetaPackage value:</span></span>
    -   <span data-ttu-id="10f42-150">開発をアップグレードする場合、またはソース コードが含まれているデモ環境をアップグレードする場合は、**MetaPackage** 値を **dynamicsax-meta-platform-development** に変更します。</span><span class="sxs-lookup"><span data-stu-id="10f42-150">If you're upgrading a development or demo environment that contains source code, change the **MetaPackage** value to **dynamicsax-meta-platform-development**.</span></span>
    -   <span data-ttu-id="10f42-151">レベル 2 のサンド ボックスやソース コードが含まれていない他の環境を含むランタイム環境をアップグレードする場合は、既定値の **dynamicsax-meta-platform-runtime** は正しい値になります。</span><span class="sxs-lookup"><span data-stu-id="10f42-151">If you're upgrading a runtime environment, such as a Tier-2 sandbox or other environment that doesn't contain source code, the default value, **dynamicsax-meta-platform-runtime**, is correct.</span></span>

4.  <span data-ttu-id="10f42-152">配置可能パッケージをインストールする標準指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="10f42-152">Follow the standard instructions for installing a deployable package.</span></span> <span data-ttu-id="10f42-153">[配置可能パッケージの適用](../deployment/apply-deployable-package-system.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="10f42-153">See [Apply a deployable package](../deployment/apply-deployable-package-system.md).</span></span>
5.  <span data-ttu-id="10f42-154">開発環境で作業している場合、アプリケーションのコードをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="10f42-154">If you're working in a development environment, rebuild your application’s code.</span></span>

<span data-ttu-id="10f42-155">**重要:** 開発環境で最初に検証することなく、実行環境でこの更新を適用しないでください。</span><span class="sxs-lookup"><span data-stu-id="10f42-155">**Important:** Do not apply this update in a runtime environment unless you have validated it in a development environment first.</span></span>

#### <a name="example-for-a-one-box-development-or-demo-environment"></a><span data-ttu-id="10f42-156">1 つのボックス (開発またはデモ) 環境の例</span><span class="sxs-lookup"><span data-stu-id="10f42-156">Example for a one-box (development or demo) environment</span></span>

    AXUpdateInstaller.exe generate -runbookid="OneBoxDev" -topologyfile="DefaultTopologyData.xml" -servicemodelfile="DefaultServiceModelData.xml" -runbookfile="OneBoxDev-runbook.xml"

    AXUpdateInstaller.exe import -runbookfile=OneBoxDev-runbook.xml

    AXUpdateInstaller.exe execute -runbookid=OneBoxDev

### <a name="install-the-visual-studio-development-tools"></a><span data-ttu-id="10f42-157">Visual Studio 開発ツールのインストール</span><span class="sxs-lookup"><span data-stu-id="10f42-157">Install the Visual Studio development tools</span></span>

<span data-ttu-id="10f42-158">[[Dynamics AXのVisual Studio 開発ツールの更新](../dev-tools/update-development-tools.md)] の説明に従って、Microsoft Visual Studio 開発ツールを更新します。</span><span class="sxs-lookup"><span data-stu-id="10f42-158">Update the Microsoft Visual Studio development tools as described in [Updating the Dynamics AX Visual Studio development tools](../dev-tools/update-development-tools.md).</span></span>

### <a name="regenerate-form-adaptor-models"></a><span data-ttu-id="10f42-159">フォーム アダプタ モデルの再生成</span><span class="sxs-lookup"><span data-stu-id="10f42-159">Regenerate form adaptor models</span></span>

<span data-ttu-id="10f42-160">フォーム アダプター モデルは、テストの自動化に必要です。</span><span class="sxs-lookup"><span data-stu-id="10f42-160">Form adaptor models are required for test automation.</span></span> <span data-ttu-id="10f42-161">新たに更新されたプラットフォーム モデルに基づいて、プラットフォーム フォーム アダプターのモデルを再生成します。</span><span class="sxs-lookup"><span data-stu-id="10f42-161">Regenerate the platform form adaptor models, based on the newly updated platform models.</span></span> <span data-ttu-id="10f42-162">フォーム アダプター モデルを生成するには、xppfagen.exe ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="10f42-162">Use the xppfagen.exe tool to generate the form adaptor models.</span></span> <span data-ttu-id="10f42-163">このツールは、パッケージの bin フォルダー (通常は、j:AosServicePackagesLocalDirectorybin) に配置されています。</span><span class="sxs-lookup"><span data-stu-id="10f42-163">This tool is located in the package's bin folder (typically, j:AosServicePackagesLocalDirectorybin).</span></span> <span data-ttu-id="10f42-164">プラットフォームのフォーム アダプター モデルの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="10f42-164">Here is a list of the platform form adaptor models:</span></span>

-   <span data-ttu-id="10f42-165">ApplicationPlatformFormAdaptor</span><span class="sxs-lookup"><span data-stu-id="10f42-165">ApplicationPlatformFormAdaptor</span></span>
-   <span data-ttu-id="10f42-166">ApplicationFoundationFormAdaptor</span><span class="sxs-lookup"><span data-stu-id="10f42-166">ApplicationFoundationFormAdaptor</span></span>
-   <span data-ttu-id="10f42-167">DirectoryFormAdaptor</span><span class="sxs-lookup"><span data-stu-id="10f42-167">DirectoryFormAdaptor</span></span>

<span data-ttu-id="10f42-168">次の例は、フォーム アダプター モデルを生成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="10f42-168">The following examples show how to generate the form adaptor models.</span></span>

    xppfagen.exe -metadata=j:AosServicePackagesLocalDirectory -model="ApplicationPlatformFormAdaptor" -xmllog="c:\temp\log1.xml"

    xppfagen.exe -metadata=j:AosServicePackagesLocalDirectory -model="ApplicationFoundationFormAdaptor" -xmllog="c:\temp\log2.xml"

    xppfagen.exe -metadata=j:AosServicePackagesLocalDirectory -model="DirectoryFormAdaptor" -xmllog="c:\temp\log3.xml"

### <a name="install-the-new-data-management-service"></a><span data-ttu-id="10f42-169">新しいデータ管理サービスのインストール</span><span class="sxs-lookup"><span data-stu-id="10f42-169">Install the new Data Management service</span></span>

<span data-ttu-id="10f42-170">配置可能なパッケージのインストール後、以下の手順に従って、新しい Data Management サービスをインストールします。</span><span class="sxs-lookup"><span data-stu-id="10f42-170">After the deployable package is installed, follow these instructions to install the new Data Management service.</span></span> <span data-ttu-id="10f42-171">管理者としてコマンド プロンプト ウィンドウを開き、.DIXFServiceScripts フォルダーから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="10f42-171">Open a Command Prompt window as an administrator, and run the following commands from the .DIXFServiceScripts folder.</span></span>

    msiExec.exe /uninstall {5C74B12A-8583-4B4F-B5F5-8E526507A3E0} /passive /qn /quiet

<span data-ttu-id="10f42-172">Microsoft SQL Server の統合サービス 2016 (13.0) に接続している場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="10f42-172">If you're connected to Microsoft SQL Server Integration Services 2016 (13.0), run the following command.</span></span>

    msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin2012" SERVICEACCOUNT="NT AUTHORITYNetworkService" /qb /lv DIXF_log.txt

<span data-ttu-id="10f42-173">Microsoft SQL Server の統合サービスの早期リリースに接続している場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="10f42-173">If you're connected to an earlier release of Microsoft SQL Server Integration Services, run the following command.</span></span>

    msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin" SERVICEACCOUNT="NT AUTHORITYNetworkService" /qb /lv DIXF_log.txt

## <a name="apply-the-platform-update-package-on-a-build-environment"></a><span data-ttu-id="10f42-174">ビルド環境にプラットフォーム更新プログラム パッケージを適用</span><span class="sxs-lookup"><span data-stu-id="10f42-174">Apply the platform update package on a build environment</span></span>
<span data-ttu-id="10f42-175">ビルド環境のプラットフォーム アップグレード パッケージを適用するには、開発環境に適用する同じ手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="10f42-175">Applying the platform upgrade package on a build environment requires the same procedure as applying it on a development environment.</span></span> <span data-ttu-id="10f42-176">ただし、次のように最新のプラットフォームにアップグレードする前に、まず、ビルド環境を準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10f42-176">However, you need to prepare your build environment first before you upgrade it to the latest platform as described next.</span></span>

### <a name="prepare-your-build-environment"></a><span data-ttu-id="10f42-177">ビルド環境を準備</span><span class="sxs-lookup"><span data-stu-id="10f42-177">Prepare your build environment</span></span>

<span data-ttu-id="10f42-178">1 つ以上のビルドに対してビルド マシンが使用されているときは、VM を新しい Dynamics AX プラットフォームにアップグレードする前に、メタデータ バックアップ フォルダーからメタデータ パッケージ フォルダーを復元する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10f42-178">When the build machine has been used for one or more builds, you should restore the metadata packages folder from the metadata backup folder before upgrading the VM to a newer Dynamics AX platform.</span></span> <span data-ttu-id="10f42-179">その後、メタデータのバックアップを削除してください。</span><span class="sxs-lookup"><span data-stu-id="10f42-179">You should then delete the metadata backup.</span></span> <span data-ttu-id="10f42-180">これにより、プラットフォームの更新がクリーンな環境で確実に適用され、次のビルド プロセスでメタデータのバックアップが存在しないことが検出され、新しいプラットフォームが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="10f42-180">This will ensure that the platform update will be applied on a clean environment, and the next build process will detect that no metadata backup exists and automatically create a new one, which will include the updated platform.</span></span> <span data-ttu-id="10f42-181">完全なメタデータ バックアップが存在するかどうかを確認するには、I:\Dynamics\BackupPackages (または、ダウンロード可能な VHD の C:\Dynamics\BackupPackages) で BackupComplete.txt ファイルを探してください。</span><span class="sxs-lookup"><span data-stu-id="10f42-181">To find out if a complete metadata backup exists, please look for a BackupComplete.txt file in I:\Dynamics\BackupPackages" (or C:\Dynamics\BackupPackages on a downloadable VHD).</span></span> <span data-ttu-id="10f42-182">このファイルの存在は、メタデータ バックアップが存在することを示し、そのファイルにはそれが作成された日時のタイムスタンプが含まれています。</span><span class="sxs-lookup"><span data-stu-id="10f42-182">The presence of this file indicates that a metadata backup exists and the file will contain a timestamp of when it was created.</span></span> <span data-ttu-id="10f42-183">展開のメタデータ パッケージ フォルダーをメタデータ バックアップから復元するには、昇格した PowerShell コマンド プロンプトを開き、以下のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="10f42-183">To restore the deployment's metadata packages folder from the metadata backup open an elevated PowerShell command prompt and run the below command.</span></span> <span data-ttu-id="10f42-184">これにより、ビルド プロセスの最初のステップで使用したのと同じスクリプトが実行されます。</span><span class="sxs-lookup"><span data-stu-id="10f42-184">This will exercise the same script as used in the first step of the build process.</span></span>

    if (Test-Path -Path "I:\Dynamics\BackupPackages\BackupComplete.txt") { C:\Dynamics\SDK\PrepareForBuild.ps1 }

<span data-ttu-id="10f42-185">注記: バックアップが存在しない場合は新しいバックアップを作成するため、完全なメタデータ バックアップが存在する場合にのみ、上記のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="10f42-185">Note: Execute the above command only if a complete metadata backup exists, as it will create a new backup if it does not.</span></span> <span data-ttu-id="10f42-186">このコマンドは、ファイルをメタデータ バックアップから展開のメタデータ パッケージ フォルダーに復元する前に、Dynamics AX 展開サービスと IIS を停止します。</span><span class="sxs-lookup"><span data-stu-id="10f42-186">This command will stop the Dynamics AX deployment services and IIS before restoring the files from the metadata backup to the deployment's metadata packages folder.</span></span> <span data-ttu-id="10f42-187">このように出力が表示されます: <em>午後 6 時 17 分 52 秒: ビルド定義環境を準備しています...</em> <em>午後 6 時 17 分 53 秒: 指定された値で Dynamics SDK のレジストリ キーを更新しています...</em> <em>午後 6 時 17 分 53 秒: AOS の web config からの値で Dynamics SDK レジストリ キーを更新しています...</em> <em>午後 6 時 17 分 53秒: Dynamics AX の配置を停止しています...</em> <em>午後 6 時 18 分 06 秒: ** バックアップが次の場所に既に存在します: I: DynamicsBackupPackages。新しいバックアップは作成されません</em><em>。</em></span><span class="sxs-lookup"><span data-stu-id="10f42-187">You should see output like this: <em>6:17:52 PM: Preparing build environment...</em> <em>6:17:53 PM: Updating Dynamics SDK registry key with specified values...</em> <em>6:17:53 PM: Updating Dynamics SDK registry key with values from AOS web config...</em> <em>6:17:53 PM: Stopping Dynamics AX deployment...</em> <em>6:18:06 PM: **A backup already exists at: I:DynamicsBackupPackages. No new backup will be created</em><em>.</em></span></span> <span data-ttu-id="10f42-188"><em>午後 6 時 18 分 6 秒: **メタデータ パッケージをバックアップから復元する</em>** <em>午後 6 時 22 分 56 秒: **メタデータ パッケージを正常にバックアップから復元しました</em><em>。</em></span><span class="sxs-lookup"><span data-stu-id="10f42-188"><em>6:18:06 PM: **Restoring metadata packages from backup...</em>** <em>6:22:56 PM: **Metadata packages successfully restored from backup</em><em>.</em></span></span> <span data-ttu-id="10f42-189"><em>午後 6 時 22 分 57: ビルド環境の準備が完了しました。</em></span><span class="sxs-lookup"><span data-stu-id="10f42-189"><em>6:22:57 PM: Preparing build environment complete.</em></span></span> <span data-ttu-id="10f42-190"><em>午後 6 時 22 分 57 秒: 終了コード 0 でスクリプトが完了</em>メタデータ バックアップが復元されると、<strong>メタデータ バックアップ フォルダーを削除 (または名前を変更) し (<em>DynamicsBackupPackages</em>)</strong>、ビルド プロセスでは検出されなくなります。</span><span class="sxs-lookup"><span data-stu-id="10f42-190"><em>6:22:57 PM: Script completed with exit code: 0</em> Once the metadata backup has been restored, <strong>delete (or rename) the metadata backup folder (<em>DynamicsBackupPackages</em>)</strong> so it will no longer be found by the build process.</span></span>

### <a name="apply-the-platform-update-package"></a><span data-ttu-id="10f42-191">プラットフォーム更新プログラム パッケージを適用</span><span class="sxs-lookup"><span data-stu-id="10f42-191">Apply the platform update package</span></span>

<span data-ttu-id="10f42-192">この更新のビルド環境を準備したら、[上記の](#apply-the-platform-update-package-on-your-development-environment)説明のように、開発環境に適用するのと同じ方法でプラットフォーム更新プログラム パッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="10f42-192">Once you have prepared your build environment for this update, apply the platform update package the same way you apply it on a development environment as describe [above](#apply-the-platform-update-package-on-your-development-environment).</span></span>

## <a name="features-that-arent-supported"></a><span data-ttu-id="10f42-193">サポートされていない機能</span><span class="sxs-lookup"><span data-stu-id="10f42-193">Features that aren't supported</span></span>
<span data-ttu-id="10f42-194">**Dynamics AX プラットフォーム 2016 年 8 月リリース (更新プログラム 2)** には、次の機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="10f42-194">**Dynamics AX platform August 2016 release (Update 2)** includes the following features:</span></span>

-   <span data-ttu-id="10f42-195">新しいエンティティ格納機能</span><span class="sxs-lookup"><span data-stu-id="10f42-195">The new Entity Store feature</span></span>
-   <span data-ttu-id="10f42-196">DirectQuery 付き Microsoft Power BI</span><span class="sxs-lookup"><span data-stu-id="10f42-196">Microsoft Power BI with DirectQuery</span></span>
-   <span data-ttu-id="10f42-197">Microsoft Cortana Analytics for Retail</span><span class="sxs-lookup"><span data-stu-id="10f42-197">Microsoft Cortana Analytics for Retail</span></span>

<span data-ttu-id="10f42-198">ただし、このトピックに記載されているプロセスを使用して更新する場合、2016 年 2 月のリリースを使用して当初展開された Dynamics AX のインスタンスにはこれらの機能がありません。</span><span class="sxs-lookup"><span data-stu-id="10f42-198">However, an instance of Dynamics AX that was originally deployed by using the February 2016 release won't have these features if you update by using the process that is described in this topic.</span></span> <span data-ttu-id="10f42-199">これらの機能を有効にするには、元の展開は更新プログラム 1 (2016年5月) の展開でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="10f42-199">To enable these features, you original deployment must be an Update 1 (May 2016) deployment.</span></span>

## <a name="optional-if-your-application-overlays-platform-models"></a><span data-ttu-id="10f42-200">オプション: アプリケーション オーバーレイ プラットフォーム モデルの場合</span><span class="sxs-lookup"><span data-stu-id="10f42-200">Optional: If your application overlays platform models</span></span>
<span data-ttu-id="10f42-201">開発インスタンスにプラットフォーム更新プログラム パッケージを適用する前に、ソリューションに次のいずれかのパッケージに属するモデルが含まれている場合は次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="10f42-201">Before you apply the platform update package on your development instance, follow these steps if your solution contains models that belong to one of the following packages:</span></span>

-   <span data-ttu-id="10f42-202">アプリケーション プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="10f42-202">Application Platform</span></span>
-   <span data-ttu-id="10f42-203">アプリケーション基準</span><span class="sxs-lookup"><span data-stu-id="10f42-203">Application Foundation</span></span>
-   <span data-ttu-id="10f42-204">ディレクトリ</span><span class="sxs-lookup"><span data-stu-id="10f42-204">Directory</span></span>
-   <span data-ttu-id="10f42-205">TestEssentials</span><span class="sxs-lookup"><span data-stu-id="10f42-205">TestEssentials</span></span>

1.  <span data-ttu-id="10f42-206">Visual Studio で、Microsoft Visual Studio Team Services (VSTS) のバージョン管理プロジェクトに対するすべての保留中の変更をチェックインします。</span><span class="sxs-lookup"><span data-stu-id="10f42-206">In Visual Studio, check in all pending changes to your Microsoft Visual Studio Team Services (VSTS) version control project.</span></span>
2.  <span data-ttu-id="10f42-207">Visual Studio を終了します。</span><span class="sxs-lookup"><span data-stu-id="10f42-207">Exit Visual Studio.</span></span>
3.  <span data-ttu-id="10f42-208">このトピックの前半で説明した、プラットフォーム更新プログラム配置可能パッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="10f42-208">Apply the platform update deployable package as described earlier in this topic.</span></span>
4.  <span data-ttu-id="10f42-209">Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="10f42-209">Start Visual Studio.</span></span>
5.  <span data-ttu-id="10f42-210">プラットフォーム モデルをオーバーレイするモデルの潜在的な競合を解決します。</span><span class="sxs-lookup"><span data-stu-id="10f42-210">Resolve potential conflicts in your models that overlay platform models.</span></span> <span data-ttu-id="10f42-211">**ヒント:** 競合アドインの作成プロジェクトを使用して、モデル内のすべての競合からプロジェクトを作成できます。[![競合からプロジェクトを作成](./media/projectforconflicts.jpg)](./media/projectforconflicts.jpg)</span><span class="sxs-lookup"><span data-stu-id="10f42-211">**Tip:** You can use the Create project from conflicts add-in to create a project from all conflicts in a model.[![Create project from conflicts ](./media/projectforconflicts.jpg)](./media/projectforconflicts.jpg)</span></span>
6.  <span data-ttu-id="10f42-212">アプリケーションをリビルドして検証します。</span><span class="sxs-lookup"><span data-stu-id="10f42-212">Rebuild and validate your application.</span></span>
7.  <span data-ttu-id="10f42-213">カスタマイズしたプラットフォーム パッケージからカスタム配置可能パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="10f42-213">Create a custom deployable package from your customized platform package.</span></span> <span data-ttu-id="10f42-214">このパッケージは、検証のためにサンドボックス/実稼働前の環境に適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10f42-214">This package should be applied to your sandbox/pre-production environment for validation.</span></span>


<a name="additional-resources"></a><span data-ttu-id="10f42-215">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="10f42-215">Additional resources</span></span>
--------

[<span data-ttu-id="10f42-216">最新の Dynamics AX 更新プログラムにアップグレードするためのプロセス</span><span class="sxs-lookup"><span data-stu-id="10f42-216">Process for upgrading to the latest Dynamics AX update</span></span>](../migration-upgrade/upgrade-latest-update.md)




