---
title: "Retail と Finance and Operations のビルド システムのマージ"
description: "この記事では、Azure DevOps を使用して Dynamics 365 for Finance and Operations、および Dynamics 365 for Retail のビルド システムをマージするステップについて説明します。"
author: andreash1
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: andreash
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d22fe0c9a38026350c839d1d7d35835bfc77d995
ms.openlocfilehash: fdffc29c346a7a1f4c9530b0a6653de816f9322b
ms.contentlocale: ja-jp
ms.lasthandoff: 09/17/2018

---

# <a name="merge-the-build-systems-for-retail-and-finance-and-operations"></a><span data-ttu-id="833f7-103">Retail および Finance and Operations 用ビルド システムのマージ</span><span class="sxs-lookup"><span data-stu-id="833f7-103">Merge the build systems for Retail and Finance and Operations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="833f7-104">この記事では、Dynamics 365 for Finance and Operations、および Dynamics 365 for Retail のビルド システムをマージするステップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="833f7-104">This article describes the steps for merging the build systems for both Dynamics 365 for Finance and Operations, and Dynamics 365 for Retail.</span></span> <span data-ttu-id="833f7-105">Lifecycle Services (LCS) に統合されたビルド エクスペリエンスは、コードのアップグレードと新しいプロジェクトの両方をサポートします。</span><span class="sxs-lookup"><span data-stu-id="833f7-105">The Lifecycle Services (LCS)-integrated build experience supports both code upgrades and new projects.</span></span> <span data-ttu-id="833f7-106">Retail SDK は、自己完結型の MSBuild ベースのビルド システムです。</span><span class="sxs-lookup"><span data-stu-id="833f7-106">The Retail SDK is a self-contained MSBuild-based build system.</span></span> <span data-ttu-id="833f7-107">多くのカスタマイザーは、Microsoft Dynamics 365 for Finance and Operations および Retail の両方のコンポーネントに生産的な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="833f7-107">Many customizers want to make productive changes in both Microsoft Dynamics 365 for Finance and Operations and Retail components.</span></span> <span data-ttu-id="833f7-108">この記事では、Azure DevOps を使用して両方のビルド システムをマージするための手動のステップを概説します。</span><span class="sxs-lookup"><span data-stu-id="833f7-108">This article outlines the manual steps for merging both build systems using Azure DevOps.</span></span> 

## <a name="enable-the-build-system"></a><span data-ttu-id="833f7-109">ビルド システムの有効化</span><span class="sxs-lookup"><span data-stu-id="833f7-109">Enable the build system</span></span>

<span data-ttu-id="833f7-110">開始するには、すべてのステップを実行して、完全な連続ビルド システムを稼働させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="833f7-110">To get started, you must follow all the steps to get a full continuous build system up and running.</span></span> <span data-ttu-id="833f7-111">詳細については、[継続的ビルドとテストの自動化を使用した開発者トポロジの展開](../../../dev-itpro/perf-test/continuous-build-test-automation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="833f7-111">For information, see [Developer topology deployment with continuous build and test automation](../../../dev-itpro/perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="833f7-112">配置した後、ビルド定義とビルド ステップを作成します。</span><span class="sxs-lookup"><span data-stu-id="833f7-112">After deployment, you create the build definition and build steps.</span></span> <span data-ttu-id="833f7-113">それをよく理解してエラーなしでビルドできるように、少なくとも 1 回はビルドしてください。</span><span class="sxs-lookup"><span data-stu-id="833f7-113">Build at least one time, so that you become familiar with it and are sure that you can build without errors.</span></span> <span data-ttu-id="833f7-114">その後、次の手順に移ります。</span><span class="sxs-lookup"><span data-stu-id="833f7-114">Then move to the next step.</span></span>

## <a name="prepare-the-retail-sdk"></a><span data-ttu-id="833f7-115">Retail SDK を準備します。</span><span class="sxs-lookup"><span data-stu-id="833f7-115">Prepare the Retail SDK</span></span>
### <a name="getting-the-retail-sdk"></a><span data-ttu-id="833f7-116">Retail SDK の取得</span><span class="sxs-lookup"><span data-stu-id="833f7-116">Getting the Retail SDK</span></span>
<span data-ttu-id="833f7-117">同じ Microsoft Azure DevOps プロジェクトで Retail ソフトウェア開発キット (SDK) がない場合は、ここで追加します。</span><span class="sxs-lookup"><span data-stu-id="833f7-117">If you don't already have the Retail software development kit (SDK) in the same Microsoft Azure DevOps project, add it now.</span></span> <span data-ttu-id="833f7-118">どの開発者トポロジまたはビルド トポロジでも、Retail SDK が存在します。</span><span class="sxs-lookup"><span data-stu-id="833f7-118">You will find the Retail SDK in any developer or build topology.</span></span> <span data-ttu-id="833f7-119">[Retail SDK の概要](retail-sdk-overview.md) の分岐ドキュメントに従います。</span><span class="sxs-lookup"><span data-stu-id="833f7-119">Follow the branching documentation in [Retail SDK overview](retail-sdk-overview.md).</span></span> <span data-ttu-id="833f7-120">この時点で、Retail SDK ミラーと Retail SDK カスタマイズ分岐を作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="833f7-120">We recommend that you create your Retail SDK mirror and your Retail SDK customization branch at this time.</span></span> <span data-ttu-id="833f7-121">Retail SDK カスタマイズ分岐が準備できた後、Retail と同じ Azure DevOps プロジェクトで送信され開始できます。</span><span class="sxs-lookup"><span data-stu-id="833f7-121">After your Retail SDK customization branch is ready, and it has been submitted in the same Azure DevOps project as Retail, you can start.</span></span>

## <a name="add-a-repository-mapping-for-the-retail-sdk"></a><span data-ttu-id="833f7-122">Retail SDK のレポジトリ マッピングを追加します。</span><span class="sxs-lookup"><span data-stu-id="833f7-122">Add a repository mapping for the Retail SDK</span></span>
<span data-ttu-id="833f7-123">Retail SDK の場所が含まれるように、ビルド定義を編集します。</span><span class="sxs-lookup"><span data-stu-id="833f7-123">Edit the build definition so that it includes the location of the Retail SDK.</span></span> <span data-ttu-id="833f7-124">(つまり、マップを追加します。) [![Retail SDK のリポジトリ マッピングを追加](./media/build-map-addition.png)](./media/build-map-addition.png)</span><span class="sxs-lookup"><span data-stu-id="833f7-124">(In other words, add a map.) [![Adding a repository mapping for the Retail SDK](./media/build-map-addition.png)](./media/build-map-addition.png)</span></span>

## <a name="add-a-new-build-step-to-build-the-retail-sdk"></a><span data-ttu-id="833f7-125">Retail SDKを構築するための新しいビルド ステップの追加</span><span class="sxs-lookup"><span data-stu-id="833f7-125">Add a new build step to build the Retail SDK</span></span>
<span data-ttu-id="833f7-126">次のスクリーン ショットに示すように、ビルド パイプラインの先頭に新しいステップを追加します。</span><span class="sxs-lookup"><span data-stu-id="833f7-126">Add a new step at the beginning of the build pipeline, as shown in the following screen shot.</span></span> <span data-ttu-id="833f7-127">[![小売 SDK を構築するための新しいビルド ステップの追加](./media/new-build-step-1024x527.png)](./media/new-build-step.png)</span><span class="sxs-lookup"><span data-stu-id="833f7-127">[![Adding a new build step to build the Retail SDK](./media/new-build-step-1024x527.png)](./media/new-build-step.png)</span></span>

## <a name="add-a-copy-step-for-binaries-from-the-retail-sdk-to-the-retail--build"></a><span data-ttu-id="833f7-128">Retail SDK から Retail ビルドにバイナリのコピー ステップの追加</span><span class="sxs-lookup"><span data-stu-id="833f7-128">Add a copy step for binaries from the Retail SDK to the Retail  build</span></span>
<span data-ttu-id="833f7-129">このビルド ステップでは、Microsoft がファイル/バイナリを共有する場合、Microsoft は Retail bin フォルダに最新の構築済みRetail バイナリをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="833f7-129">This build step enables Microsoft to copy the latest built Retail binaries to the Retail bin folder, if Microsoft shares files/binaries.</span></span> <span data-ttu-id="833f7-130">前のセクションで説明したように、Retail SDK のビルド ステップを追加した直後にこのステップを完了することを確認します。</span><span class="sxs-lookup"><span data-stu-id="833f7-130">Make sure that you complete this step immediately after you add a build step for the Retail SDK, as described in the previous section.</span></span> <span data-ttu-id="833f7-131">[![小売 SDK から小売ビルドの Dynamics 365 へのバイナリのコピー ステップの追加](./media/binary-drop-to-ax.png)](./media/binary-drop-to-ax.png)</span><span class="sxs-lookup"><span data-stu-id="833f7-131">[![Adding a copy step for binaries from the Retail SDK to the Dynamics 365 for Retail build](./media/binary-drop-to-ax.png)](./media/binary-drop-to-ax.png)</span></span>

## <a name="add-a-copy-step-for-all-retail-packages"></a><span data-ttu-id="833f7-132">すべての Retail パッケージのコピー ステップの追加</span><span class="sxs-lookup"><span data-stu-id="833f7-132">Add a copy step for all Retail packages</span></span>
<span data-ttu-id="833f7-133">このステップが「PowerShell: パッケージの生成」ステップ後に発生することを確認します (以下の図を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="833f7-133">Make sure that this step occurs after the “PowerShell: Generate packages” step (see image below).</span></span> <span data-ttu-id="833f7-134">その引数を次に示します。</span><span class="sxs-lookup"><span data-stu-id="833f7-134">Here are the arguments.</span></span>

    -BuildPackagePath "$(Agent.BuildDirectory)\Packages" -BuildVersion "$(Build.BuildNumber)"

<span data-ttu-id="833f7-135">[![すべての小売パッケージのコピー ステップの追加](./media/package-drop-1024x473.png)](./media/package-drop.png)</span><span class="sxs-lookup"><span data-stu-id="833f7-135">[![Adding a copy step for all Retail packages](./media/package-drop-1024x473.png)](./media/package-drop.png)</span></span>

## <a name="optional-referencing-a-retail-dll-from-retail"></a><span data-ttu-id="833f7-136">オプション: Retail から Retail DLL を参照します。</span><span class="sxs-lookup"><span data-stu-id="833f7-136">Optional: Referencing a Retail DLL from Retail</span></span>
<span data-ttu-id="833f7-137">構築済み Retail バイナリを小売パッケージに追加する必要がある場合にのみ、このタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="833f7-137">You must complete this task only if you must add built Retail binaries to the Retail package.</span></span> <span data-ttu-id="833f7-138">この場合、これら 3 つの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="833f7-138">In this case, you must follow these three steps:</span></span>

1.  <span data-ttu-id="833f7-139">小売プロジェクトでは通常の AXReference を使用します。</span><span class="sxs-lookup"><span data-stu-id="833f7-139">Use a normal AXReference in your Retail project.</span></span>
2.  <span data-ttu-id="833f7-140">Azure DevOps に、対応する AXReference フォルダーとその中の XML ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="833f7-140">Add the corresponding AXReference folder and the XML file inside it to Azure DevOps.</span></span>
3.  <span data-ttu-id="833f7-141">Copy-RetailBinaries.ps1 ファイルを適切なファイル コマンドで更新し、バイナリ ファイルを Retail SDK から Retail bin フォルダーに取得します。</span><span class="sxs-lookup"><span data-stu-id="833f7-141">Update the Copy-RetailBinaries.ps1 file with the appropriate file commands to get the binary file from the Retail SDK to the Retail bin folder.</span></span> <span data-ttu-id="833f7-142">Microsoft Windows PowerShell ファイルには、ApplicationSuite bin フォルダーに PricingEngine.dll ファイルをコピーするサンプルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="833f7-142">The Microsoft Windows PowerShell file includes a sample that copies the PricingEngine.dll file into the ApplicationSuite bin folder.</span></span> <span data-ttu-id="833f7-143">ビルドしているモジュールによっては、ファイルとフォルダーが異なる場所にあるように変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="833f7-143">Depending on the modules that you're building, the files and folders must be changed so that they are in a different location.</span></span>

