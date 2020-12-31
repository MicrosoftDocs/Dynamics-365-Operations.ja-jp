---
title: 最新のプラットフォーム更新プログラムを環境へ適用
description: このトピックでは、最新のプラットフォーム更新プログラムを Finance and Operations 環境に適用する方法について説明します。
author: tariqbell
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 253274
ms.assetid: a70a4f28-9269-4b35-bc29-1edba0b92d83
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 408aa89dd979a18410ee612ab0e0697037875d76
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686628"
---
# <a name="apply-the-latest-platform-update-to-environments"></a><span data-ttu-id="4eb93-103">最新のプラットフォーム更新プログラムの環境への適用</span><span class="sxs-lookup"><span data-stu-id="4eb93-103">Apply the latest platform update to environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4eb93-104">このトピックでは、最新のプラットフォーム リリースを Finance and Operations 環境に適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-104">This topic explains how to apply the latest platform release to your Finance and Operations environment.</span></span>

## <a name="overview"></a><span data-ttu-id="4eb93-105">概要</span><span class="sxs-lookup"><span data-stu-id="4eb93-105">Overview</span></span>

<span data-ttu-id="4eb93-106">Finance and Operations では、プラットフォームは次のコンポーネントで構成されています:</span><span class="sxs-lookup"><span data-stu-id="4eb93-106">In Finance and Operations, the platform consists of the following components:</span></span>

-   <span data-ttu-id="4eb93-107">Application Object Server (AOS)、データ管理フレームワーク、レポートおよびビジネス インテリジェンス (BI) フレームワーク、開発ツール、および分析サービスなどのバイナリ。</span><span class="sxs-lookup"><span data-stu-id="4eb93-107">Binaries such as Application Object Server (AOS), the data management framework, the reporting and business intelligence (BI) framework, development tools, and analytics services.</span></span>
-   <span data-ttu-id="4eb93-108">次のアプリケーション オブジェクト ツリー (AOT) パッケージ。</span><span class="sxs-lookup"><span data-stu-id="4eb93-108">The following Application Object Tree (AOT) packages:</span></span>
    -   <span data-ttu-id="4eb93-109">アプリケーション プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="4eb93-109">Application Platform</span></span>
    -   <span data-ttu-id="4eb93-110">アプリケーション基準</span><span class="sxs-lookup"><span data-stu-id="4eb93-110">Application Foundation</span></span>
    -   <span data-ttu-id="4eb93-111">Test Essentials</span><span class="sxs-lookup"><span data-stu-id="4eb93-111">Test Essentials</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4eb93-112">最新のプラットフォームに移行するためには、Finance and Operations の実装で、プラットフォームに属する AOT パッケージのカスタマイズ (オーバーレイヤー) を行うことは **できません**。</span><span class="sxs-lookup"><span data-stu-id="4eb93-112">To move to the latest platform, your Finance and Operations implementation **cannot** have any customizations (overlayering) of any of the AOT packages that belong to the platform.</span></span> <span data-ttu-id="4eb93-113">この制限は、プラットフォーム更新 3 で導入されたため、プラットフォームにシームレスに継続的な更新を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4eb93-113">This restriction was introduced in Platform update 3, so that seamless continuous updates can be made to the platform.</span></span> 

## <a name="overall-flow"></a><span data-ttu-id="4eb93-114">全体的な流れ</span><span class="sxs-lookup"><span data-stu-id="4eb93-114">Overall flow</span></span>
<span data-ttu-id="4eb93-115">次の図は、プラットフォームを最新の更新プログラムにアップグレードするための全体的なプロセスを示しています。</span><span class="sxs-lookup"><span data-stu-id="4eb93-115">The following illustration shows the overall process for upgrading the platform to the latest update.</span></span>

<span data-ttu-id="4eb93-116">[![プラットフォームのカスタマイズがない実装のアップグレード プロセス](./media/flownocustomisations.jpg)](./media/flownocustomisations.jpg)</span><span class="sxs-lookup"><span data-stu-id="4eb93-116">[![Upgrade process for implementations that have no customization of the platform](./media/flownocustomisations.jpg)](./media/flownocustomisations.jpg)</span></span>

<span data-ttu-id="4eb93-117">既にプラットフォーム更新プログラム 4 以降で実行している場合は、最新のリリースに更新することが単純なサービス工程となります。</span><span class="sxs-lookup"><span data-stu-id="4eb93-117">If you are already running on Platform update 4 or later, updating to the latest release is a simple servicing operation.</span></span> <span data-ttu-id="4eb93-118">プラットフォーム更新プログラム パッケージが LCS アセット ライブラリに含まれた後、フローに従って LCS 環境ページから更新を適用します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-118">After the platform update package is in your LCS asset library, follow the flow to apply an update from the LCS environment page.</span></span> <span data-ttu-id="4eb93-119">**メンテナンス** で **更新プログラムの適用** を選択してから、プラットフォーム更新プログラム パッケージを選択します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-119">Select **Apply updates** under **Maintain**, then select the platform update package.</span></span>

<span data-ttu-id="4eb93-120">[![更新プログラムの適用](./media/applyupdates.jpg)](./media/applyupdates.jpg)</span><span class="sxs-lookup"><span data-stu-id="4eb93-120">[![Apply updates](./media/applyupdates.jpg)](./media/applyupdates.jpg)</span></span>

<span data-ttu-id="4eb93-121">次のセクションでは **最新のプラットフォーム パッケージを取得して、LCS を通じて配置された環境に適用する** 方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-121">Learn how to **get the latest platform package and apply it to an environment deployed through LCS** in the next section.</span></span>

## <a name="apply-the-latest-platform-update-package"></a><span data-ttu-id="4eb93-122">最新のプラットフォーム更新プログラム パッケージを適用</span><span class="sxs-lookup"><span data-stu-id="4eb93-122">Apply the latest platform update package</span></span>
<span data-ttu-id="4eb93-123">LCS で、環境ページから最新のプラットフォーム更新パッケージを入手するには、2つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="4eb93-123">There are two ways to get the latest platform update package in LCS from your environment page.</span></span>
- <span data-ttu-id="4eb93-124">**プラットフォーム バイナリ更新プログラム** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4eb93-124">Click the **Platform binary updates** tile</span></span> 
- <span data-ttu-id="4eb93-125">**すべてのバイナリ更新プログラム** タイルをクリックすると、アプリケーションとプラットフォームのバイナリ アップデートのパッケージの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4eb93-125">Click the **All Binary Updates** tile to see a list of combined package of application and platform binary updates.</span></span> <span data-ttu-id="4eb93-126">(現在のプラットフォーム更新プログラム 4 では、LCS のバイナリ更新プログラムに、最新のプラットフォームへのアップグレードが含まれています)。</span><span class="sxs-lookup"><span data-stu-id="4eb93-126">(As of Platform update 4, binary updates from LCS include an upgrade to the latest platform).</span></span>

> [!NOTE]
> <span data-ttu-id="4eb93-127">LCS の環境ページのタイルは、現在のバージョンと環境の状態に基づいて、環境に適用される更新のみを表示します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-127">Tiles on an environment's page in LCS show only the updates that are applicable to your environment based on the current version and state of the environment.</span></span>

<span data-ttu-id="4eb93-128">上記に示されたように、2 つのタイルのいずれかをクリックして、最新のプラットフォーム更新プログラム パッケージを取得します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-128">Get the latest platform update package by clicking on one of the two tiles as mentioned above.</span></span> <span data-ttu-id="4eb93-129">プラットフォームに含まれる修正を確認した後に、**パッケージの保存** をクリックして、プロジェクト アセット ライブラリにパッケージを保存します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-129">After reviewing the fixes included in the platform, click **Save Package** to save the package to the project asset library.</span></span>

<span data-ttu-id="4eb93-130">プロセスの観点では、プラットフォーム更新プログラム パッケージの展開は、バイナリ修正プログラムの展開可能なパッケージに似ています。</span><span class="sxs-lookup"><span data-stu-id="4eb93-130">From a process perspective, deploying a platform upgrade package resembles a binary hotfix deployable package.</span></span>

-   <span data-ttu-id="4eb93-131">クラウド開発、ビルド、デモ、第 2 層サンド ボックス、または実稼働環境にプラットフォーム更新パッケージを適用するには、LCS から直接更新します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-131">To apply a platform update package to your cloud development, build, demo, tier-2 sandbox, or production environment, update directly from LCS.</span></span>

    <span data-ttu-id="4eb93-132">[![更新プログラムの適用](./media/applyupdates.jpg)](./media/applyupdates.jpg)</span><span class="sxs-lookup"><span data-stu-id="4eb93-132">[![Apply updates](./media/applyupdates.jpg)](./media/applyupdates.jpg)</span></span>

<span data-ttu-id="4eb93-133">詳細については、[クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md) で、バイナリ修正プログラムを適用するための指示に従って下さい。</span><span class="sxs-lookup"><span data-stu-id="4eb93-133">For more details, follow the instructions for applying a binary hotfix in [Apply updates to cloud environments](../deployment/apply-deployable-package-system.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4eb93-134">**ドキュメント管理用のファイルの移行**: プラットフォーム更新プログラム 6 以降にアップグレードした後、管理者は **ドキュメント管理パラメーター** ページの **ファイルの移行** ボタンをクリックして、アップグレード プロセスを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4eb93-134">**Migrate files for Document management**: After upgrading to Platform update 6 or later, an administrator needs to click the **Migrate Files** button on the **Document management parameters** page to finish the upgrade process.</span></span> <span data-ttu-id="4eb93-135">これにより、データベースに格納されている添付ファイルが BLOB ストレージに移行されます。</span><span class="sxs-lookup"><span data-stu-id="4eb93-135">This will migrate any attachments stored in the database to blob storage.</span></span> <span data-ttu-id="4eb93-136">移行はバッチ プロセスとして実行され、データベースから Azure Blob Storage に移動されるファイルの数とサイズに応じて、時間がかかる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4eb93-136">The migration will run as a batch process and could take a long time, depending on the number and size of the files being moved from the database into Azure blob storage.</span></span> <span data-ttu-id="4eb93-137">移行プロセスの実行中に、ユーザーは引き続き添付ファイルを使用できるため、移行には、ユーザーが気づくほどの影響はありません。</span><span class="sxs-lookup"><span data-stu-id="4eb93-137">The attachments will continue to be available to users while the migration process is running, so there should be no noticeable effects from the migration.</span></span> <span data-ttu-id="4eb93-138">バッチ処理がまだ実行されているかどうかを確認するには、**バッチ ジョブ** ページで **データベースに格納されたファイルをブロブ ストレージに移行する** プロセスを探します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-138">To check if the batch process is still running, look for the **Migrate files stored in the database to blob storage** process on the **Batch jobs** page.</span></span>

## <a name="apply-a-platform-update-to-environments-that-are-not-connected-to-lcs"></a><span data-ttu-id="4eb93-139">LCS に接続されていない環境にプラットフォーム更新プログラムを適用します</span><span class="sxs-lookup"><span data-stu-id="4eb93-139">Apply a platform update to environments that are not connected to LCS</span></span>
<span data-ttu-id="4eb93-140">このセクションでは、プラットフォーム更新パッケージを *ローカル開発環境* (LCS に接続されていないもの) に適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-140">This section describes how to apply a platform update package to a *local development environment* (one that that is not connected to LCS).</span></span>

### <a name="how-to-get-the-platform-update-package"></a><span data-ttu-id="4eb93-141">プラットフォーム更新プログラム パッケージを取得する方法</span><span class="sxs-lookup"><span data-stu-id="4eb93-141">How to get the platform update package</span></span>
<span data-ttu-id="4eb93-142">プラットフォーム更新プログラム パッケージは、Microsoft によってリリースされ、Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリからインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="4eb93-142">Platform update packages are released by Microsoft and can be imported from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="4eb93-143">パッケージ名の先頭に **Dynamics 365 Unified Operations プラットフォーム更新** が付きます。</span><span class="sxs-lookup"><span data-stu-id="4eb93-143">The package name is prefixed with **Dynamics 365 Unified Operations Platform Update**.</span></span> <span data-ttu-id="4eb93-144">プラットフォーム更新プログラムのパッケージをインポートするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-144">Use these steps to import the platform update package:</span></span>

1.  <span data-ttu-id="4eb93-145">LCS プロジェクトの資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-145">Go to your LCS project's Asset library.</span></span>
2.  <span data-ttu-id="4eb93-146">**ソフトウェア配置可能パッケージ** タブで、**インポート** をクリックし、プラットフォーム更新プログラム パッケージへの参照を作成します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-146">On the **Software deployable package** tab, click **Import** to create a reference to the platform update package.</span></span> 

    <span data-ttu-id="4eb93-147">[![ボタンのインポート](./media/importupgradepackage.png)](./media/importupgradepackage.png)</span><span class="sxs-lookup"><span data-stu-id="4eb93-147">[![Import button](./media/importupgradepackage.png)](./media/importupgradepackage.png)</span></span>

3.  <span data-ttu-id="4eb93-148">目的のプラットフォーム更新プログラム パッケージを選択します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-148">Select the desired platform update package.</span></span>

> [!NOTE]
> <span data-ttu-id="4eb93-149">共有アセット ライブラリのパッケージは、目的のプラットフォーム リリースの最新ビルド (ホットフィックス付き) に対応していない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4eb93-149">The package in the Shared Asset library may not correspond to the latest build (with hotfixes) of the desired platform release.</span></span> <span data-ttu-id="4eb93-150">最新のビルドを保証するには、この記事の前半で説明した LCS 環境ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-150">To guarrantee the latest build, use the LCS environment page as described earlier in this article.</span></span>

### <a name="apply-the-platform-update-package-to-your-development-environment"></a><span data-ttu-id="4eb93-151">開発環境にプラットフォーム更新プログラム パッケージを適用</span><span class="sxs-lookup"><span data-stu-id="4eb93-151">Apply the platform update package to your development environment</span></span>
> [!NOTE]
> <span data-ttu-id="4eb93-152">これらの手順は、LCS から直接更新できない環境にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4eb93-152">These instructions apply only to environments that cannot be updated directly from LCS.</span></span>

### <a name="install-the-deployable-package"></a><span data-ttu-id="4eb93-153">配置可能パッケージのインストール</span><span class="sxs-lookup"><span data-stu-id="4eb93-153">Install the deployable package</span></span>

1.  <span data-ttu-id="4eb93-154">プラットフォーム更新パッケージ (AXPlatformUpdate.zip) を使用中の仮想マシン (VM) にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="4eb93-154">Download the platform update package (AXPlatformUpdate.zip) to your virtual machine (VM).</span></span>
2.  <span data-ttu-id="4eb93-155">コンテンツをローカル ディレクトリに解凍します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-155">Unzip the contents to a local directory.</span></span>
3.  <span data-ttu-id="4eb93-156">アップグレードする環境のタイプに応じて、\\AOSService\\ スクリプトの下の PlatformUpdatePackages.Config ファイルを開き、**MetaPackage** 値を変更します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-156">Depending on the type of environment that you're upgrading, open the PlatformUpdatePackages.Config file under \\AOSService\\Scripts, and change the **MetaPackage** value.</span></span>
    -   <span data-ttu-id="4eb93-157">開発をアップグレードする場合、またはソース コードが含まれているデモ環境をアップグレードする場合は、**MetaPackage** 値を **dynamicsax-meta-platform-development** に変更します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-157">If you're upgrading a development or demo environment that contains source code, change the **MetaPackage** value to **dynamicsax-meta-platform-development**.</span></span>
    -   <span data-ttu-id="4eb93-158">レベル 2 のサンド ボックスやソース コードが含まれていない別の環境を含むランタイム環境をアップグレードする場合は、既定値の **dynamicsax-meta-platform-runtime** は正しい値になります。</span><span class="sxs-lookup"><span data-stu-id="4eb93-158">If you're upgrading a runtime environment, such as a tier-2 sandbox environment or another environment that doesn't contain source code, the default value, **dynamicsax-meta-platform-runtime**, is correct.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4eb93-159">プラットフォーム更新プログラム 4 以降にアップグレードするときは、手順 3 は適用されません。</span><span class="sxs-lookup"><span data-stu-id="4eb93-159">Step 3 is not applicable when upgrading to Platform update 4 or later.</span></span>

4.  <span data-ttu-id="4eb93-160">配置可能パッケージをインストールする指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="4eb93-160">Follow the instructions for installing a deployable package.</span></span> <span data-ttu-id="4eb93-161">[コマンド ラインからの配置可能なパッケージのインストール](../deployment/install-deployable-package.md)</span><span class="sxs-lookup"><span data-stu-id="4eb93-161">See [Install deployable packages from the command line](../deployment/install-deployable-package.md).</span></span>
5.  <span data-ttu-id="4eb93-162">開発環境で作業している場合、アプリケーションのコードをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="4eb93-162">If you're working in a development environment, rebuild your application’s code.</span></span>

#### <a name="example"></a><span data-ttu-id="4eb93-163">例</span><span class="sxs-lookup"><span data-stu-id="4eb93-163">Example</span></span>

```powershell
AXUpdateInstaller.exe generate -runbookid="OneBoxDev" -topologyfile="DefaultTopologyData.xml" -servicemodelfile="DefaultServiceModelData.xml" -runbookfile="OneBoxDev-runbook.xml"

    AXUpdateInstaller.exe import -runbookfile=OneBoxDev-runbook.xml

    AXUpdateInstaller.exe execute -runbookid=OneBoxDev
```

### <a name="install-the-visual-studio-development-tools-platform-update-3-or-earlier"></a><span data-ttu-id="4eb93-164">Visual Studio 開発ツール (プラットフォーム更新プログラム 3 またはそれ以前) をインストールする</span><span class="sxs-lookup"><span data-stu-id="4eb93-164">Install the Visual Studio development tools (Platform update 3 or earlier)</span></span>

> [!NOTE]
> <span data-ttu-id="4eb93-165">プラットフォーム更新プログラム 4 以降を更新する場合にこのセクションをスキップすると、開発ツールは配置可能パッケージのインストールの一部として自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="4eb93-165">Skip this section if you are updating to Platform update 4 or later, development tools are automatically installed as part of installing the deployable package.</span></span>

<span data-ttu-id="4eb93-166">[Visual Studio 開発ツールの更新](../dev-tools/update-development-tools.md) の説明に従って、Visual Studio 開発ツールを更新します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-166">Update the Visual Studio development tools as described in [Update the Visual Studio development tools](../dev-tools/update-development-tools.md).</span></span>

### <a name="regenerate-form-adaptor-models"></a><span data-ttu-id="4eb93-167">フォーム アダプタ モデルの再生成</span><span class="sxs-lookup"><span data-stu-id="4eb93-167">Regenerate form adaptor models</span></span>

<span data-ttu-id="4eb93-168">フォーム アダプター モデルは、テストの自動化に必要です。</span><span class="sxs-lookup"><span data-stu-id="4eb93-168">Form adaptor models are required for test automation.</span></span> <span data-ttu-id="4eb93-169">新たに更新されたプラットフォーム モデルに基づいて、プラットフォーム フォーム アダプターのモデルを再生成します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-169">Regenerate the platform form adaptor models, based on the newly updated platform models.</span></span> <span data-ttu-id="4eb93-170">フォーム アダプター モデルを生成するには、xppfagen.exe ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-170">Use the xppfagen.exe tool to generate the form adaptor models.</span></span> <span data-ttu-id="4eb93-171">このツールは、パッケージの bin フォルダー (通常は、j:\\AosService\\PackagesLocalDirectory\\bin) にあります。</span><span class="sxs-lookup"><span data-stu-id="4eb93-171">This tool is located in the package's bin folder (typically, j:\\AosService\\PackagesLocalDirectory\\bin).</span></span> <span data-ttu-id="4eb93-172">プラットフォームのフォーム アダプター モデルの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-172">Here is a list of the platform form adaptor models:</span></span>

-   <span data-ttu-id="4eb93-173">ApplicationPlatformFormAdaptor</span><span class="sxs-lookup"><span data-stu-id="4eb93-173">ApplicationPlatformFormAdaptor</span></span>
-   <span data-ttu-id="4eb93-174">ApplicationFoundationFormAdaptor</span><span class="sxs-lookup"><span data-stu-id="4eb93-174">ApplicationFoundationFormAdaptor</span></span>
-   <span data-ttu-id="4eb93-175">DirectoryFormAdaptor</span><span class="sxs-lookup"><span data-stu-id="4eb93-175">DirectoryFormAdaptor</span></span>

<span data-ttu-id="4eb93-176">次の例は、フォーム アダプター モデルを生成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="4eb93-176">The following examples show how to generate the form adaptor models.</span></span>

```powershell
xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="ApplicationPlatformFormAdaptor" -xmllog="c:\temp\log1.xml"

xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="ApplicationFoundationFormAdaptor" -xmllog="c:\temp\log2.xml"

xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="DirectoryFormAdaptor" -xmllog="c:\temp\log3.xml"
```

### <a name="install-the-data-management-service-platform-update-3-or-earlier"></a><span data-ttu-id="4eb93-177">データ管理サービス (プラットフォーム更新プログラム 3 またはそれ以前) をインストールします</span><span class="sxs-lookup"><span data-stu-id="4eb93-177">Install the Data Management service (Platform update 3 or earlier)</span></span>

> [!NOTE]
> <span data-ttu-id="4eb93-178">プラットフォーム更新プログラム 4 以降を更新する場合にこのセクションをスキップすると、データ管理サービスは配置可能パッケージのインストールの一部として自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="4eb93-178">Skip this section if you are updating to Platform update 4 or newer, the data management service is automatically installed as part of installing the deployable package.</span></span>

<span data-ttu-id="4eb93-179">配置可能なパッケージのインストール後、以下の手順に従って、新しい Data Management サービスをインストールします。</span><span class="sxs-lookup"><span data-stu-id="4eb93-179">After the deployable package is installed, follow these instructions to install the new Data Management service.</span></span> <span data-ttu-id="4eb93-180">管理者として **コマンド プロンプト** ウィンドウを開き、.\\DIXFService\\Scripts フォルダーから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-180">Open a **Command Prompt** window as an administrator, and run the following commands from the .\\DIXFService\\Scripts folder.</span></span>

```Console
msiExec.exe /uninstall {5C74B12A-8583-4B4F-B5F5-8E526507A3E0} /passive /qn /quiet
```

<span data-ttu-id="4eb93-181">Microsoft SQL Server の統合サービス 2016 (13.0) に接続している場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-181">If you're connected to Microsoft SQL Server Integration Services 2016 (13.0), run the following command.</span></span>

```Console
msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin\2012" SERVICEACCOUNT="NT AUTHORITY\NetworkService" /qb /lv DIXF_log.txt
```

<span data-ttu-id="4eb93-182">Microsoft SQL Server の統合サービスの早期リリースに接続している場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-182">If you're connected to an earlier release of Microsoft SQL Server Integration Services, run the following command.</span></span>

```Console
msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin" SERVICEACCOUNT="NT AUTHORITY\NetworkService" /qb /lv DIXF_log.txt
```

## <a name="apply-the-platform-update-package-on-a-build-environment-platform-update-6-or-earlier"></a><span data-ttu-id="4eb93-183">ビルド環境 (プラットフォーム アップデート 6 またはそれ以前) にプラットフォーム更新プログラムのパッケージを適用</span><span class="sxs-lookup"><span data-stu-id="4eb93-183">Apply the platform update package on a build environment (Platform update 6 or earlier)</span></span>

> [!NOTE]
> <span data-ttu-id="4eb93-184">プラットフォーム更新プログラム 7 以降を更新する場合はこのセクションをスキップします。</span><span class="sxs-lookup"><span data-stu-id="4eb93-184">Skip this section if you are updating to Platform update 7 or newer.</span></span> <span data-ttu-id="4eb93-185">これは、ビルド環境のための前提条件ステップでした。</span><span class="sxs-lookup"><span data-stu-id="4eb93-185">This was a prerequesite step for build environments.</span></span>

<span data-ttu-id="4eb93-186">1 つ以上のビルドに対してビルド マシンが使用されているときは、VM を新しいプラットフォーム更新プログラムにアップグレードする前に、メタデータ バックアップ フォルダーからメタデータ パッケージ フォルダーを復元する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4eb93-186">If the build machine has been used for one or more builds, you should restore the metadata packages folder from the metadata backup folder before you upgrade the VM to a newer platform update.</span></span> <span data-ttu-id="4eb93-187">その後、メタデータのバックアップを削除してください。</span><span class="sxs-lookup"><span data-stu-id="4eb93-187">You should then delete the metadata backup.</span></span> <span data-ttu-id="4eb93-188">これらの手順は、プラットフォームの更新がクリーンな環境に確実に適用されるようにします。</span><span class="sxs-lookup"><span data-stu-id="4eb93-188">These steps help ensure that the platform update will be applied on a clean environment.</span></span> <span data-ttu-id="4eb93-189">次のビルド プロセスはメタデータ バックアップが存在しないことを検出し、新しいメタデータ バックアップが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="4eb93-189">The next build process will then detect that no metadata backup exists and will automatically create a new one.</span></span> <span data-ttu-id="4eb93-190">この新しいメタデータ バックアップには、更新されたプラットフォームが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4eb93-190">This new metadata backup will include the updated platform.</span></span> <span data-ttu-id="4eb93-191">完全なメタデータ バックアップが存在するかどうかを確認するには、I:\\DynamicsBackup\\Packages (またはダウンロード可能な仮想ハード ディスク \[VHD\] 上の C:\\DynamicsBackup\\Packages) で、BackupComplete.txt ファイルを探してください。</span><span class="sxs-lookup"><span data-stu-id="4eb93-191">To determine whether a complete metadata backup exists, look for a BackupComplete.txt file in I:\\DynamicsBackup\\Packages (or C:\\DynamicsBackup\\Packages on a downloadable virtual hard disk \[VHD\]).</span></span> <span data-ttu-id="4eb93-192">このファイルが存在する場合、メタデータ バックアップが存在し、ファイルにはその作成日時を示すタイムスタンプが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4eb93-192">If this file is present, a metadata backup exists, and the file will contain a timestamp that indicates when it was created.</span></span> <span data-ttu-id="4eb93-193">展開のメタデータ パッケージ フォルダーをメタデータ バックアップから復元するには、上位の Windows PowerShell **コマンド プロンプト** ウィンドウを開き、以下のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-193">To restore the deployment's metadata packages folder from the metadata backup, open an elevated Windows PowerShell **Command Prompt** window, and run the following command.</span></span> <span data-ttu-id="4eb93-194">このコマンドは、ビルド プロセスの最初のステップで使用したのと同じスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-194">This command will run the same script that is used in the first step of the build process.</span></span>

```powershell
if (Test-Path -Path "I:\DynamicsBackup\Packages\BackupComplete.txt") { C:\DynamicsSDK\PrepareForBuild.ps1 }
```

<span data-ttu-id="4eb93-195">完全なメタデータ バックアップが存在しない場合、コマンドは新しいバックアップを作成します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-195">If a complete metadata backup doesn't exist, the command will create a new backup.</span></span> <span data-ttu-id="4eb93-196">このコマンドも ファイルをメタデータ バックアップから展開のメタデータ パッケージ フォルダーに復元する前に、Finance and Operations 配置サービスおよびインターネット インフォメーション サービス (IIS) を停止します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-196">This command will also stop the Finance and Operations deployment services and Internet Information Services (IIS) before it restores the files from the metadata backup to the deployment's metadata packages folder.</span></span> <span data-ttu-id="4eb93-197">次の例のような出力が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4eb93-197">You should see output that resembles the following example.</span></span> 

```powershell
6:17:52 PM: Preparing build environment...* <em>6:17:53 PM: Updating Dynamics SDK registry key with specified values...</em> <em>6:17:53 PM: Updating Dynamics SDK registry key with values from AOS web config...</em> <em>6:17:53 PM: Stopping Finance and Operations deployment...</em> <em>6:18:06 PM: **A backup already exists at: I:\\DynamicsBackup\\Packages. No new backup will be created</em><em>.</em> <em>6:18:06 PM: **Restoring metadata packages from backup...</em>** <em>6:22:56 PM: **Metadata packages successfully restored from backup</em><em>.</em> <em>6:22:57 PM: Preparing build environment complete.</em> <em>6:22:57 PM: Script completed with exit code: 0</em> 
```

<span data-ttu-id="4eb93-198">メタデータ バックアップが復元された後、ビルド プロセスでは検出されないようにメタデータ バックアップ フォルダー (DynamicsBackup\\Packages) を削除します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-198">After the metadata backup has been restored, delete (or rename) the metadata backup folder (DynamicsBackup\\Packages), so that it will no longer be found by the build process.</span></span>

### <a name="apply-the-platform-update-package"></a><span data-ttu-id="4eb93-199">プラットフォーム更新プログラム パッケージを適用</span><span class="sxs-lookup"><span data-stu-id="4eb93-199">Apply the platform update package</span></span>

<span data-ttu-id="4eb93-200">更新プログラムのビルド環境を準備した後、他の環境で使用する同じメソッドでプラットフォームの更新プログラム パッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="4eb93-200">After you've prepared your build environment for this update, apply the platform update package by using the same method that you use on other environments.</span></span>

<a name="additional-resources"></a><span data-ttu-id="4eb93-201">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4eb93-201">Additional resources</span></span>
--------

[<span data-ttu-id="4eb93-202">Finance and Operationsで最新の更新プログラムに移行するためのプロセス</span><span class="sxs-lookup"><span data-stu-id="4eb93-202">Process for moving to the latest update of Finance and Operations</span></span>](upgrade-latest-update.md)
