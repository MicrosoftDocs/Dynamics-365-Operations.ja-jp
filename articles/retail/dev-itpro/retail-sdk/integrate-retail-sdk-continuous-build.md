---
title: Retail and Finance 用ビルド システムのマージ
description: このトピックでは、Azure DevOps を使用して Dynamics 365 Retail および Dynamics 365 Finance の両方のビルド システムをマージするためのステップを説明します。
author: andreash1
manager: AnnBe
ms.date: 02/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: andreash
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3bfb92daa628108ce038769410a41360058bba56
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570597"
---
# <a name="merge-the-build-systems-for-retail-and-finance"></a><span data-ttu-id="fc710-103">Retail and Finance 用ビルド システムのマージ</span><span class="sxs-lookup"><span data-stu-id="fc710-103">Merge the build systems for Retail and Finance</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="fc710-104">このトピックでは、Dynamics 365 Retail および Dynamics 365 Finance のビルド システムをマージするためのステップを説明します。</span><span class="sxs-lookup"><span data-stu-id="fc710-104">This topic describes the steps for merging the build systems for Dynamics 365 Retail and Dynamics 365 Finance.</span></span> <span data-ttu-id="fc710-105">Lifecycle Services (LCS) に統合されたビルド エクスペリエンスは、コードのアップグレードと新しいプロジェクトの両方をサポートします。</span><span class="sxs-lookup"><span data-stu-id="fc710-105">The Lifecycle Services (LCS)-integrated build experience supports both code upgrades and new projects.</span></span> <span data-ttu-id="fc710-106">Retail SDK は、自己完結型の MSBuild ベースのビルド システムです。</span><span class="sxs-lookup"><span data-stu-id="fc710-106">The Retail SDK is a self-contained MSBuild-based build system.</span></span> <span data-ttu-id="fc710-107">多くのカスタマイザーは、両方の Microsoft Finance and Retail のコンポーネントに生産的な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="fc710-107">Many customizers want to make productive changes in both Microsoft Finance and Retail components.</span></span> <span data-ttu-id="fc710-108">このトピックでは、Azure DevOps を使用して両方のビルド システムをマージするための手動のステップを概説します。</span><span class="sxs-lookup"><span data-stu-id="fc710-108">This topic outlines the manual steps for merging both build systems using Azure DevOps.</span></span> 


## <a name="enable-the-build-system"></a><span data-ttu-id="fc710-109">ビルド システムの有効化</span><span class="sxs-lookup"><span data-stu-id="fc710-109">Enable the build system</span></span>

<span data-ttu-id="fc710-110">開始するには、すべてのステップを実行して、完全な連続ビルド システムを稼働させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc710-110">To get started, you must follow all the steps to get a full continuous build system up and running.</span></span> <span data-ttu-id="fc710-111">詳細については、[継続的ビルドとテストの自動化を使用した開発者トポロジの展開](../../../dev-itpro/perf-test/continuous-build-test-automation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc710-111">For information, see [Developer topology deployment with continuous build and test automation](../../../dev-itpro/perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="fc710-112">配置した後、ビルド定義とビルド ステップを作成します。</span><span class="sxs-lookup"><span data-stu-id="fc710-112">After deployment, you create the build definition and build steps.</span></span> <span data-ttu-id="fc710-113">それをよく理解してエラーなしでビルドできるように、少なくとも 1 回はビルドしてください。</span><span class="sxs-lookup"><span data-stu-id="fc710-113">Build at least one time, so that you become familiar with it and are sure that you can build without errors.</span></span> <span data-ttu-id="fc710-114">その後、次の手順に移ります。</span><span class="sxs-lookup"><span data-stu-id="fc710-114">Then move to the next step.</span></span>

## <a name="prepare-the-retail-sdk"></a><span data-ttu-id="fc710-115">Retail SDK を準備します。</span><span class="sxs-lookup"><span data-stu-id="fc710-115">Prepare the Retail SDK</span></span>

### <a name="getting-the-retail-sdk"></a><span data-ttu-id="fc710-116">Retail SDK の取得</span><span class="sxs-lookup"><span data-stu-id="fc710-116">Getting the Retail SDK</span></span>

<span data-ttu-id="fc710-117">同じ Microsoft Azure DevOps プロジェクトで Retail ソフトウェア開発キット (SDK) がない場合は、ここで追加します。</span><span class="sxs-lookup"><span data-stu-id="fc710-117">If you don't already have the Retail software development kit (SDK) in the same Microsoft Azure DevOps project, add it now.</span></span> <span data-ttu-id="fc710-118">どの開発者トポロジまたはビルド トポロジでも、Retail SDK が存在します。</span><span class="sxs-lookup"><span data-stu-id="fc710-118">You will find the Retail SDK in any developer or build topology.</span></span> <span data-ttu-id="fc710-119">[Retail SDK の概要](retail-sdk-overview.md) の分岐ドキュメントに従います。</span><span class="sxs-lookup"><span data-stu-id="fc710-119">Follow the branching documentation in [Retail SDK overview](retail-sdk-overview.md).</span></span> <span data-ttu-id="fc710-120">この時点で、Retail SDK ミラーと Retail SDK カスタマイズ分岐を作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fc710-120">We recommend that you create your Retail SDK mirror and your Retail SDK customization branch at this time.</span></span> <span data-ttu-id="fc710-121">Retail SDK カスタマイズ分岐が準備できた後、Retail と同じ Azure DevOps プロジェクトで送信され開始できます。</span><span class="sxs-lookup"><span data-stu-id="fc710-121">After your Retail SDK customization branch is ready, and it has been submitted in the same Azure DevOps project as Retail, you can start.</span></span>

## <a name="install-nugetexe"></a><span data-ttu-id="fc710-122">NuGet.exe のインストール</span><span class="sxs-lookup"><span data-stu-id="fc710-122">Install NuGet.exe</span></span> 

<span data-ttu-id="fc710-123">ファイルの結合およびSDKのサイズを最小限に抑えるため、いくつかの依存関係パッケージおよび参照を NuGet パッケージに移動します。</span><span class="sxs-lookup"><span data-stu-id="fc710-123">Some of the dependency packages and references have moved to NuGet packages to minimize the file merge and the size of the SDK.</span></span> <span data-ttu-id="fc710-124">これらは NuGet.org からダウンロードできます。Retail SDK を作成すると、これらの依存関係は自動的に packages.config ファイルに基づいて NuGet.org から収集されます。</span><span class="sxs-lookup"><span data-stu-id="fc710-124">These are available for download from the NuGet.org. When you build the Retail SDK these dependencies are automatically pulled from the NuGet.org based on the packages.config file.</span></span> <span data-ttu-id="fc710-125">このためには、「[NuGet コマンド ライン インターフェイス](https://docs.microsoft.com/nuget/tools/nuget-exe-cli-reference#installing-nugetexe)」をインストールし、 NuGet.org から nuget.exe をダウンロードした後、nuget を Windows パスに追加する必要があります。次の手順は、Windows パスに nuget を追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fc710-125">For this to work, you need to install the [NuGet command line interface](https://docs.microsoft.com/nuget/tools/nuget-exe-cli-reference#installing-nugetexe) and add the nuget to the Windows path after downloading nuget.exe from NuGet.org. The following steps show how to add the nuget to the Windows path:</span></span>

1. <span data-ttu-id="fc710-126">Windows メニューを開き、 **Path**と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc710-126">Open the Windows menu and type **Path**.</span></span> <span data-ttu-id="fc710-127">**システム環境変数を編集**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="fc710-127">The **Edit the system environment variables** will be available.</span></span> 
2. <span data-ttu-id="fc710-128">メニューの右下の**環境変数**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc710-128">In that menu, click **Environment variables** on the lower right.</span></span>
3. <span data-ttu-id="fc710-129">次のウィンドウで、**システム変数**の**パス**を選択し、**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc710-129">In the next window, under **System variables**, select **Path** and click **Edit**.</span></span>
4. <span data-ttu-id="fc710-130">nuget.exe ファイルを保存するフォルダーのエントリを追加するか、既に登録されているフォルダーに nuget.exe ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="fc710-130">Add an entry for the folder where you would like to store the nuget.exe file or store the nuget.exe file in a folder that is already listed.</span></span>

## <a name="add-a-repository-mapping-for-the-retail-sdk"></a><span data-ttu-id="fc710-131">Retail SDK のレポジトリ マッピングを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc710-131">Add a repository mapping for the Retail SDK</span></span>

<span data-ttu-id="fc710-132">Retail SDK の場所が含まれるように、ビルド定義を編集します。</span><span class="sxs-lookup"><span data-stu-id="fc710-132">Edit the build definition so that it includes the location of the Retail SDK.</span></span> <span data-ttu-id="fc710-133">(言い換えれば、マップを追加します。)</span><span class="sxs-lookup"><span data-stu-id="fc710-133">(In other words, add a map.)</span></span>

<span data-ttu-id="fc710-134">[![Retail SDK に対するレポジトリ マッピングの追加](./media/build-map-addition.png)](./media/build-map-addition.png)</span><span class="sxs-lookup"><span data-stu-id="fc710-134">[![Adding a repository mapping for the Retail SDK](./media/build-map-addition.png)](./media/build-map-addition.png)</span></span>

## <a name="add-a-new-build-step-to-build-the-retail-sdk"></a><span data-ttu-id="fc710-135">Retail SDKを構築するための新しいビルド ステップの追加</span><span class="sxs-lookup"><span data-stu-id="fc710-135">Add a new build step to build the Retail SDK</span></span>

<span data-ttu-id="fc710-136">次のスクリーン ショットに示すように、ビルド パイプラインの先頭に新しいステップを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc710-136">Add a new step at the beginning of the build pipeline, as shown in the following screen shot.</span></span>

<span data-ttu-id="fc710-137">[![小売 SDK を構築するための新しいビルド ステップの追加](./media/new-build-step-1024x527.png)](./media/new-build-step.png)</span><span class="sxs-lookup"><span data-stu-id="fc710-137">[![Adding a new build step to build the Retail SDK](./media/new-build-step-1024x527.png)](./media/new-build-step.png)</span></span>

## <a name="add-a-copy-step-for-binaries-from-the-retail-sdk-to-the-retail-build"></a><span data-ttu-id="fc710-138">Retail SDK から Retail ビルドへのバイナリのコピー ステップの追加</span><span class="sxs-lookup"><span data-stu-id="fc710-138">Add a copy step for binaries from the Retail SDK to the Retail build</span></span>

<span data-ttu-id="fc710-139">このビルド ステップでは、Microsoft がファイル/バイナリを共有する場合、Microsoft は Retail bin フォルダに最新の構築済み Retail バイナリをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="fc710-139">This build step enables Microsoft to copy the latest built Retail binaries to the Retail bin folder, if Microsoft shares files/binaries.</span></span> <span data-ttu-id="fc710-140">前のセクションで説明したように、Retail SDK のビルド ステップを追加した直後にこのステップを完了することを確認します。</span><span class="sxs-lookup"><span data-stu-id="fc710-140">Make sure that you complete this step immediately after you add a build step for the Retail SDK, as described in the previous section.</span></span>

<span data-ttu-id="fc710-141">[![Retail SDK から Retail ビルドへのバイナリのコピー ステップの追加](./media/binary-drop-to-ax.png)](./media/binary-drop-to-ax.png)</span><span class="sxs-lookup"><span data-stu-id="fc710-141">[![Adding a copy step for binaries from the Retail SDK to the Retail build](./media/binary-drop-to-ax.png)](./media/binary-drop-to-ax.png)</span></span>

## <a name="add-a-copy-step-for-all-retail-packages"></a><span data-ttu-id="fc710-142">すべての Retail パッケージのコピー ステップの追加</span><span class="sxs-lookup"><span data-stu-id="fc710-142">Add a copy step for all Retail packages</span></span>

<span data-ttu-id="fc710-143">このステップが "PowerShell: パッケージの生成" ステップ後に発生することを確認します (以下の図を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="fc710-143">Make sure that this step occurs after the "PowerShell: Generate packages" step (see image below).</span></span> <span data-ttu-id="fc710-144">その引数を次に示します。</span><span class="sxs-lookup"><span data-stu-id="fc710-144">Here are the arguments.</span></span>

```
-BuildPackagePath "$(Agent.BuildDirectory)\Packages" -BuildVersion "$(Build.BuildNumber)"
```

<span data-ttu-id="fc710-145">[![すべての小売パッケージのコピー ステップの追加](./media/package-drop-1024x473.png)](./media/package-drop.png)</span><span class="sxs-lookup"><span data-stu-id="fc710-145">[![Adding a copy step for all Retail packages](./media/package-drop-1024x473.png)](./media/package-drop.png)</span></span>

## <a name="optional-referencing-a-retail-dll-from-retail"></a><span data-ttu-id="fc710-146">オプション: Retail から Retail DLL を参照します。</span><span class="sxs-lookup"><span data-stu-id="fc710-146">Optional: Referencing a Retail DLL from Retail</span></span>

<span data-ttu-id="fc710-147">構築済み Retail バイナリを小売パッケージに追加する必要がある場合にのみ、このタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc710-147">You must complete this task only if you must add built Retail binaries to the Retail package.</span></span> <span data-ttu-id="fc710-148">この場合、これら 3 つの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc710-148">In this case, you must follow these three steps:</span></span>

1. <span data-ttu-id="fc710-149">小売プロジェクトでは通常の AXReference を使用します。</span><span class="sxs-lookup"><span data-stu-id="fc710-149">Use a normal AXReference in your Retail project.</span></span>
2. <span data-ttu-id="fc710-150">Azure DevOps に、対応する AXReference フォルダーとその中の XML ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc710-150">Add the corresponding AXReference folder and the XML file inside it to Azure DevOps.</span></span>
3. <span data-ttu-id="fc710-151">Copy-RetailBinaries.ps1 ファイルを適切なファイル コマンドで更新し、バイナリ ファイルを Retail SDK から Retail bin フォルダーに取得します。</span><span class="sxs-lookup"><span data-stu-id="fc710-151">Update the Copy-RetailBinaries.ps1 file with the appropriate file commands to get the binary file from the Retail SDK to the Retail bin folder.</span></span> <span data-ttu-id="fc710-152">Microsoft Windows PowerShell ファイルには、ApplicationSuite bin フォルダーに PricingEngine.dll ファイルをコピーするサンプルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fc710-152">The Microsoft Windows PowerShell file includes a sample that copies the PricingEngine.dll file into the ApplicationSuite bin folder.</span></span> <span data-ttu-id="fc710-153">ビルドしているモジュールによっては、ファイルとフォルダーが異なる場所にあるように変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc710-153">Depending on the modules that you're building, the files and folders must be changed so that they are in a different location.</span></span>
