---
title: Microsoft ホステッド エージェントと Azure Pipelines を使用するビルドの自動化
description: このトピックでは、Microsoft Azure DevOps でエージェントにおける X++ のビルド プロセスを自動化する方法について説明します。
author: jorisdg
ms.date: 03/05/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 26731
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-03-05
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 783433f16dbf5a09c568b7f43c4483a79cdb1290
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216703"
---
# <a name="build-automation-that-uses-microsoft-hosted-agents-and-azure-pipelines"></a><span data-ttu-id="acaaf-103">Microsoft ホステッド エージェントと Azure Pipelines を使用するビルドの自動化</span><span class="sxs-lookup"><span data-stu-id="acaaf-103">Build automation that uses Microsoft-hosted agents and Azure Pipelines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="acaaf-104">Microsoft Windows で実行される任意のビルド エージェントで、X++ コードのビルドと配置可能なパッケージの作成プロセスを自動化できます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-104">You can automate the process of building X++ code and creating deployable packages on any build agent that run on Microsoft Windows.</span></span> <span data-ttu-id="acaaf-105">これらのエージェントには、[Microsoft-ホステッド エージェント](/azure/devops/pipelines/agents/hosted)が含まれています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-105">These agents include [Microsoft-hosted agents](/azure/devops/pipelines/agents/hosted).</span></span> <span data-ttu-id="acaaf-106">この方法は、ビルド バーチャル マシン (VM) の配置の設定、保守、およびコストを回避するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-106">This approach helps you avoid the setup, maintenance, and cost of deploying build virtual machines (VMs).</span></span> <span data-ttu-id="acaaf-107">また、ビルド エージェントの既存の設定を再利用して、他の .NET ビルド自動化を実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-107">It also lets you reuse the existing setup of build agents to run other .NET build automation.</span></span>

> [!NOTE]
> <span data-ttu-id="acaaf-108">この機能は、コンパイルとパッケージングに限定されています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-108">This feature is limited to compilation and packaging.</span></span> <span data-ttu-id="acaaf-109">このランタイムを必要とする X++ 単体テスト (SysTest)、データベースの同期、またはその他の機能 (Application Object Server \[AOS \]) やそのコンポーネントはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="acaaf-109">There is no support for X++ unit testing (SysTest), database synchronization, or other features that require the runtime (Application Object Server \[AOS\]) or its components.</span></span>

## <a name="prerequisites-for-building-x-code"></a><span data-ttu-id="acaaf-110">X++ コードをビルドするための前提条件</span><span class="sxs-lookup"><span data-stu-id="acaaf-110">Prerequisites for building X++ code</span></span>

### <a name="build-projects"></a><span data-ttu-id="acaaf-111">プロジェクトのビルド</span><span class="sxs-lookup"><span data-stu-id="acaaf-111">Build projects</span></span>

<span data-ttu-id="acaaf-112">Azure DevOps での X++ のビルドに .NET ツールを使用するには、Microsoft Build Engine (MSBuild) とカスタム X++ のターゲットが使用されます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-112">To use .NET tools for building X++ in Azure DevOps, the Microsoft Build Engine (MSBuild) and custom X++ targets are used.</span></span> <span data-ttu-id="acaaf-113">X++ ソース コード レポジトリには、ビルドする各パッケージの X++ プロジェクトが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-113">Your X++ source code repository must contain an X++ project for each package that you have to build.</span></span> <span data-ttu-id="acaaf-114">オプションで、ソリューション ファイルを使用して、C# プロジェクトの依存関係を含むプロジェクトをグループ化したり、明示的なビルド順序を指定したりできます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-114">You can optionally use a solution file to group the projects, including C# project dependencies, and provide an explicit build order.</span></span> <span data-ttu-id="acaaf-115">リポジトリにプロジェクトがまだ含まれていない場合は、Visual Studio にプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-115">If the repository doesn't already contain a project, you can create a project in Visual Studio.</span></span>

> [!NOTE]
> <span data-ttu-id="acaaf-116">既存の X++ プロジェクト (rnrproj) を使用する場合は、プラットフォーム更新プログラム 27 以降の Visual Studio ツールを使用して、それを作成するか、または開いて保存しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-116">When you use an existing X++ project (rnrproj), make sure that you created it, or opened and saved it, by using Visual Studio tools on Platform update 27 or later.</span></span>
>
> <span data-ttu-id="acaaf-117">1 つのパッケージには複数のモデルを含めることができますが、常に完全にビルドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-117">Although a package can contain multiple models, it must always be built in its entirety.</span></span> <span data-ttu-id="acaaf-118">したがって、パッケージ全体をビルドするために必要なプロジェクトは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="acaaf-118">Therefore, only one project for just one of the models is required to build the whole package.</span></span> <span data-ttu-id="acaaf-119">また、プロジェクトにはオブジェクトを含める必要はありませんが、プロジェクトに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-119">Additionally, although the project doesn't have to contain any objects, it can contain them.</span></span>

### <a name="nuget-packages"></a><span data-ttu-id="acaaf-120">NuGet パッケージ</span><span class="sxs-lookup"><span data-stu-id="acaaf-120">NuGet packages</span></span>

<span data-ttu-id="acaaf-121">X++ コードをビルドするには、X++ コンパイラ (xppc.exe) などの基本的な開発者ツールを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-121">To build X++ code, the basic developer tools such as the X++ compiler (xppc.exe) are required.</span></span> <span data-ttu-id="acaaf-122">また、アプリケーション プラットフォームやアプリケーション スイートなどの参照先パッケージは、コンパイルされた形式で使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-122">Additionally, any referenced packages, such as the Application Platform or Application Suite, must be available in a compiled format.</span></span> <span data-ttu-id="acaaf-123">このプロセスを有効にするために、Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリには、X++ ビルドを実行するために必要な NuGet パッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-123">To enable this process, the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) provides NuGet packages that are required to do an X++ build.</span></span>

<span data-ttu-id="acaaf-124">次のパッケージは、共有アセット ライブラリからダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-124">The following packages can be downloaded from the Shared asset library:</span></span>

- <span data-ttu-id="acaaf-125">**Microsoft.Dynamics.AX.Platform.CompilerPackage** – このパッケージには、ビルドを実行するために必要な X++コンパイラおよび関連ツールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-125">**Microsoft.Dynamics.AX.Platform.CompilerPackage** – This package contains the X++ compiler and related tools that are required to do a build.</span></span>
- <span data-ttu-id="acaaf-126">**Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp** – このパッケージには、アプリケーション プラットフォームおよび関連モジュールのコンパイル済み X++ コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-126">**Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp** – This package contains the compiled X++ code for the Application Platform and related modules.</span></span> <span data-ttu-id="acaaf-127">このコードは、ビルドに対して最適化されています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-127">This code is optimized for building.</span></span>
- <span data-ttu-id="acaaf-128">**Microsoft.Dynamics.AX.Application.DevALM.BuildXpp** – このパッケージには、アプリケーションおよび関連モジュールのコンパイル済み X++ コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-128">**Microsoft.Dynamics.AX.Application.DevALM.BuildXpp** – This package contains the compiled X++ code for the Application and related modules.</span></span> <span data-ttu-id="acaaf-129">このコードは、ビルドに対して最適化されています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-129">This code is optimized for building.</span></span>

<span data-ttu-id="acaaf-130">バージョン 10.0.18 から、アプリケーション スイート パッケージは 2 つのパッケージに分割され、共有アセット ライブラリからダウンロードする追加のパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-130">Starting from version 10.0.18, the Application Suite package has been split into two packages and there is an additional package to download from the Shared asset library.</span></span>

- <span data-ttu-id="acaaf-131">**Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp** – このパッケージには、アプリケーション スイート モジュールのコンパイル済み X++ コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-131">**Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp** - This package contains the compiled X++ code for the Application Suite module.</span></span> <span data-ttu-id="acaaf-132">このコードは、ビルドに対して最適化されています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-132">This code is optimized for building.</span></span>

<span data-ttu-id="acaaf-133">これらのパッケージを LCS からダウンロードし、ビルドを実行する Azure DevOps 組織内の Azure コンポーネント フィードに追加し ます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-133">Download these packages from LCS, and add them to an Azure Artifacts feed in the Azure DevOps organization where the builds will run.</span></span> <span data-ttu-id="acaaf-134">Azure コンポーネントを作成し、NuGet パッケージを追加する方法の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="acaaf-134">For more information about how to create an Azure Artifacts feed and add NuGet packages, see these topics:</span></span>

- [<span data-ttu-id="acaaf-135">Azure DevOps サービスおよび TFS の NuGet パッケージの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="acaaf-135">Get started with NuGet packages in Azure DevOps Services and TFS</span></span>](/azure/devops/artifacts/get-started-nuget)
- [<span data-ttu-id="acaaf-136">フィードの作成</span><span class="sxs-lookup"><span data-stu-id="acaaf-136">Create a feed</span></span>](/azure/devops/artifacts/get-started-nuget#create-a-feed)
- [<span data-ttu-id="acaaf-137">独自の NuGet パッケージの作成と公開</span><span class="sxs-lookup"><span data-stu-id="acaaf-137">Create and publish your own NuGet package</span></span>](/azure/devops/artifacts/get-started-nuget#create-and-publish-your-own-nuget-package)

> [!NOTE]
> <span data-ttu-id="acaaf-138">無料の Azure DevOps 組織には、Azure コンポーネントの限られたストレージしかありません。</span><span class="sxs-lookup"><span data-stu-id="acaaf-138">Free Azure DevOps organizations have limited storage for Azure Artifacts.</span></span> <span data-ttu-id="acaaf-139">ストレージ容量を解放するために、古いバージョンと使用していないバージョンを削除することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="acaaf-139">Consider deleting old and unused versions to free up storage capacity.</span></span> <span data-ttu-id="acaaf-140">詳細については、[Azure コンポーネントのサインアップ](/azure/devops/artifacts/start-using-azure-artifacts#billing-and-free-monthly-usage) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="acaaf-140">For more information, see [Sign up for Azure Artifacts](/azure/devops/artifacts/start-using-azure-artifacts#billing-and-free-monthly-usage).</span></span>

<span data-ttu-id="acaaf-141">ビルド中に使用する必要があるパッケージを特定するには、ビルド時に nuget.exe ファイルと packages.config ファイルを用意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-141">To identify which packages should be used during the build, and where they can be found, you must provide a nuget.config file and a packages.config file during the build.</span></span> <span data-ttu-id="acaaf-142">これらのファイルを作成し、ソース管理リポジトリに追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="acaaf-142">We recommend that you create these files and add them to the source control repository.</span></span> <span data-ttu-id="acaaf-143">これらのファイルのパスは NuGet コマンドの明示的な入力であるため、ソース管理内の任意の場所にファイルを格納でき ます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-143">The files can be stored anywhere in source control, because the paths of these files are explicit inputs for the NuGet command.</span></span>

<span data-ttu-id="acaaf-144">nuget.exe ファイルには、パッケージが格納されているソース フィードを持つ NuGet が含まれています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-144">The nuget.config file provides NuGet with the source feed where the packages can be found.</span></span> <span data-ttu-id="acaaf-145">packages.config ファイルでは、パッケージとそのバージョンが指定されています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-145">The packages.config file specifies the packages and their versions.</span></span> <span data-ttu-id="acaaf-146">新しいバージョンに対してビルドする場合は、packages.config ファイルのバージョンを更新するだけで済みます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-146">To build against a newer version, you just have to update the versions in the packages.config file.</span></span> <span data-ttu-id="acaaf-147">サンプルの nuget.config ファイルを含む詳細については、[Azure Pipelines でのパッケージ管理 NuGet パッケージの復元](/azure/devops/pipelines/packages/nuget-restore)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="acaaf-147">For more information, including a sample nuget.config file, see [Restore Package Management NuGet packages in Azure Pipelines](/azure/devops/pipelines/packages/nuget-restore).</span></span>

<span data-ttu-id="acaaf-148">次の例は、一般的な X++ ビルドに必要な 3 つの主要なパッケージのための、**packages.config** ファイルを示しています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-148">The following example shows a **packages.config** file for the three main packages that are required for a typical X++ build.</span></span> <span data-ttu-id="acaaf-149">一覧のバージョンを実際のバージョンの NuGet パッケージに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-149">You must substitute the listed version with the actual versions of your NuGet packages.</span></span>

+ <span data-ttu-id="acaaf-150">バージョン 10.0.17 以前の場合は、次の packages.config レイアウトを使用します。</span><span class="sxs-lookup"><span data-stu-id="acaaf-150">For version 10.0.17 or earlier, use the following packages.config layout:</span></span>

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <packages>
        <package id="Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp" version="7.0.5644.16778" targetFramework="net40" />
        <package id="Microsoft.Dynamics.AX.Application.DevALM.BuildXpp" version="10.0.464.13" targetFramework="net40" />
        <package id="Microsoft.Dynamics.AX.Platform.CompilerPackage" version="7.0.5644.16778" targetFramework="net40" />
    </packages>
    ```

+ <span data-ttu-id="acaaf-151">バージョン 10.0.18 以降の場合は、次の packages.config レイアウトを使用します。</span><span class="sxs-lookup"><span data-stu-id="acaaf-151">For version 10.0.18 or later, use the following packages.config layout:</span></span>

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <packages>
        <package id="Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp" version="7.0.5968.16973" targetFramework="net40" />
        <package id="Microsoft.Dynamics.AX.Application.DevALM.BuildXpp" version="10.0.793.16" targetFramework="net40" />
        <package id="Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp" version="10.0.793.16" targetFramework="net40" />
        <package id="Microsoft.Dynamics.AX.Platform.CompilerPackage" version="7.0.5968.16973" targetFramework="net40" />
    </packages>
    ```

## <a name="creating-the-pipeline"></a><span data-ttu-id="acaaf-152">パイプラインの作成</span><span class="sxs-lookup"><span data-stu-id="acaaf-152">Creating the pipeline</span></span>

<span data-ttu-id="acaaf-153">Azure DevOps は、ビルドを自動化するために使用できるパイプラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="acaaf-153">Azure DevOps provides pipelines that can be used to automate builds.</span></span> <span data-ttu-id="acaaf-154">パイプラインには、YML と Classic の 2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-154">There are two types of pipelines: YML and Classic.</span></span> <span data-ttu-id="acaaf-155">YML パイプラインは、Git ソース管理リポジトリを使用している場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-155">YML pipelines are available only when you use Git source control repositories.</span></span> <span data-ttu-id="acaaf-156">Classic パイプラインを使用して、Team Foundation バージョン管理 (TFVC) リポジトリをビルドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-156">Classic pipelines must be used to build Team Foundation Version Control (TFVC) repositories.</span></span> <span data-ttu-id="acaaf-157">詳細については、 [Azure Pipelines](/azure/devops/pipelines/get-started/pipelines-get-started) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="acaaf-157">For more information, see [Azure Pipelines](/azure/devops/pipelines/get-started/pipelines-get-started).</span></span>

<span data-ttu-id="acaaf-158">このセクションでは、パイプラインで X++ コードを作成するために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="acaaf-158">This section describes the steps that are required in a pipeline to build X++ code.</span></span> <span data-ttu-id="acaaf-159">[Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub リポジトリでは、既存の Azure DevOps プロジェクトにインポートできるサンプル パイプラインを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-159">In the [Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub repository, you can find a sample pipeline that can be imported into an existing Azure DevOps project.</span></span>

### <a name="creating-a-basic-build-pipeline"></a><span data-ttu-id="acaaf-160">基本的なビルド パイプラインの作成</span><span class="sxs-lookup"><span data-stu-id="acaaf-160">Creating a basic build pipeline</span></span>

<span data-ttu-id="acaaf-161">X++ をコンパイルするための基本パイプラインには、2 つの手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="acaaf-161">A basic pipeline for compiling X++ requires only two steps:</span></span>

1. <span data-ttu-id="acaaf-162">NuGet パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="acaaf-162">Install the NuGet packages.</span></span>
2. <span data-ttu-id="acaaf-163">ソリューションまたはプロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="acaaf-163">Build the solution or projects.</span></span>

<span data-ttu-id="acaaf-164">抽出された NuGet パッケージの使用を容易にするために、**NuGet インストール** オプションを使用して、**-ExcludeVersion** [NuGet コマンドライン オプション](/nuget/reference/cli-reference/cli-ref-install#options)を指定することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="acaaf-164">To simplify use of the extracted NuGet packages, consider using the **NuGet install** option and specifying the **-ExcludeVersion** [NuGet command-line option](/nuget/reference/cli-reference/cli-ref-install#options).</span></span> <span data-ttu-id="acaaf-165">このようにして、パッケージのバージョンに関係なく、抽出されたパッケージ パスをビルドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-165">In that way, the extracted package paths can be used in the build, regardless of the version of the packages.</span></span> <span data-ttu-id="acaaf-166">**NuGet インストーラー** タスクを使用し、**インストールの種類** フィールドを **インストール** に設定します。</span><span class="sxs-lookup"><span data-stu-id="acaaf-166">Use the **NuGet Installer** task, and set the **Installation type** field to **Install**.</span></span> <span data-ttu-id="acaaf-167">最後に、前の手順で作成した packages.config ファイルと nuget.config ファイルのパスを指定します。</span><span class="sxs-lookup"><span data-stu-id="acaaf-167">Finally, specify the path of the packages.config and nuget.config files that you created earlier.</span></span>

<span data-ttu-id="acaaf-168">次の NuGet 引数の例では、パッケージ バージョンに対してサブフォルダーが作成されないようにし、NuGet パッケージを **$(Pipeline.Workspace)\\NuGets** に展開します。</span><span class="sxs-lookup"><span data-stu-id="acaaf-168">The following example of NuGet arguments will prevent a subfolder from being created for the package versions and will extract the NuGet packages into **$(Pipeline.Workspace)\\NuGets**.</span></span>

`-ExcludeVersion -OutputDirectory "$(Pipeline.Workspace)\NuGets"`

<span data-ttu-id="acaaf-169">MSBuild を使用して X++ をビルドするには、いくつかの引数を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-169">To build X++ by using MSBuild, you must supply several arguments.</span></span> <span data-ttu-id="acaaf-170">ソリューションをビルドするパイプライン ステップでは、これらの引数を **MSBuild 引数** フィールドで指定できます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-170">In the pipeline step that builds the solution, you can specify these arguments in the **MSBuild Arguments** field.</span></span>

| <span data-ttu-id="acaaf-171">引数</span><span class="sxs-lookup"><span data-stu-id="acaaf-171">Argument</span></span> | <span data-ttu-id="acaaf-172">説明</span><span class="sxs-lookup"><span data-stu-id="acaaf-172">Description</span></span> |
| --- | --- |
| <span data-ttu-id="acaaf-173">/p:BuildTasksDirectory</span><span class="sxs-lookup"><span data-stu-id="acaaf-173">/p:BuildTasksDirectory</span></span> | <span data-ttu-id="acaaf-174">抽出されたコンパイラ ツール NuGet パッケージのパス (DevAlm フォルダー内のサブフォルダを含む)。</span><span class="sxs-lookup"><span data-stu-id="acaaf-174">The path of the extracted Compiler Tools NuGet package, including the subfolders in the DevAlm folder.</span></span> |
| <span data-ttu-id="acaaf-175">/p:MetadataDirectory</span><span class="sxs-lookup"><span data-stu-id="acaaf-175">/p:MetadataDirectory</span></span> | <span data-ttu-id="acaaf-176">X++ ソース コードのパス。</span><span class="sxs-lookup"><span data-stu-id="acaaf-176">The path of the X++ source code.</span></span> |
| <span data-ttu-id="acaaf-177">/p:FrameworkDirectory</span><span class="sxs-lookup"><span data-stu-id="acaaf-177">/p:FrameworkDirectory</span></span> | <span data-ttu-id="acaaf-178">抽出されたコンパイラ ツール NuGet パッケージのパス。</span><span class="sxs-lookup"><span data-stu-id="acaaf-178">The path of the extracted Compiler Tools NuGet package.</span></span> |
| <span data-ttu-id="acaaf-179">/p:ReferenceFolder</span><span class="sxs-lookup"><span data-stu-id="acaaf-179">/p:ReferenceFolder</span></span> | <span data-ttu-id="acaaf-180">コンパイルで参照され、必須である X++ パッケージのバイナリを含むパスのセミコロン区切りのリスト (アプリケーション プラットフォームやアプリケーション スイートなど)。</span><span class="sxs-lookup"><span data-stu-id="acaaf-180">A semicolon-separated list of paths that contain binaries of X++ packages that are referenced and required for compilation (for example, Application Platform and Application Suite).</span></span> <span data-ttu-id="acaaf-181">コンパイルするコードに互いを参照する複数のパッケージがある場合は、出力ディレクトリもここに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-181">If the code that will be compiled has multiple packages that reference each other, the output directory should also be included here.</span></span> |
| <span data-ttu-id="acaaf-182">/p:ReferencePath</span><span class="sxs-lookup"><span data-stu-id="acaaf-182">/p:ReferencePath</span></span> | <span data-ttu-id="acaaf-183">コンパイル時に参照され、必須である X++ 以外のすべてのバイナリを含むパスのセミコロン区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="acaaf-183">A semicolon-separated list of paths that contain any non-X++ binaries that are referenced and required for compilation.</span></span> <span data-ttu-id="acaaf-184">必要な参照が含まれている場合があるため、抽出したコンパイラ ツール NuGet パッケージの場所を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-184">You should include the location of the extracted Compiler Tools NuGet package, because it might contain required references.</span></span> |
| <span data-ttu-id="acaaf-185">/p:OutputDirectory</span><span class="sxs-lookup"><span data-stu-id="acaaf-185">/p:OutputDirectory</span></span> | <span data-ttu-id="acaaf-186">コンパイラがフォルダーとバイナリを作成するパス。</span><span class="sxs-lookup"><span data-stu-id="acaaf-186">The path where the compiler will create folders and binaries.</span></span> |

<span data-ttu-id="acaaf-187">次の MSBuild 引数の例では、NuGet パッケージが **$(Pipeline.Workspace)\\NuGets** にインストールされており、X++ のソース コードが **$(Build.SourcesDirectory)\\Metadata** 内にあり、コンパイラの出力を **$(Build.BinariesDirectory)** にする必要があることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-187">The following example of MSBuild arguments assumes that the NuGet packages are installed in **$(Pipeline.Workspace)\\NuGets**, the X++ source code is in **$(Build.SourcesDirectory)\\Metadata**, and the output of the compiler should go in **$(Build.BinariesDirectory)**.</span></span>

+ <span data-ttu-id="acaaf-188">バージョン 10.0.17 以前の場合は、次の引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="acaaf-188">For version 10.0.17 or earlier, use the following arguments:</span></span>

    ```dos
    /p:BuildTasksDirectory="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage\DevAlm"
    /p:MetadataDirectory="$(Build.SourcesDirectory)\Metadata"
    /p:FrameworkDirectory="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage"
    /p:ReferenceFolder="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp\ref\net40;$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Application.DevALM.BuildXpp\ref\net40;$(Build.SourcesDirectory)\Metadata;$(Build.BinariesDirectory)"
    /p:ReferencePath="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage" /p:OutputDirectory="$(Build.BinariesDirectory)"
    ```
    
+ <span data-ttu-id="acaaf-189">バージョン 10.0.18 以降の場合は、次の引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="acaaf-189">For version 10.0.18 or newer, use the following arguments:</span></span>

    ```dos
    /p:BuildTasksDirectory="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage\DevAlm"
    /p:MetadataDirectory="$(Build.SourcesDirectory)\Metadata"
    /p:FrameworkDirectory="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage"
    /p:ReferenceFolder="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp\ref\net40;$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Application.DevALM.BuildXpp\ref\net40;$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp\ref\net40;$(Build.SourcesDirectory)\Metadata;$(Build.BinariesDirectory)"
    /p:ReferencePath="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage" /p:OutputDirectory="$(Build.BinariesDirectory)"
    ```

<span data-ttu-id="acaaf-190">パイプライン サンプルでは、NuGet パッケージ名とパスの変数を使用して、これらのコマンドを簡略化しています。</span><span class="sxs-lookup"><span data-stu-id="acaaf-190">In the pipeline samples, variables for NuGet package names and paths are used to simplify these commands.</span></span>

### <a name="creating-a-full-pipeline-that-includes-packaging"></a><span data-ttu-id="acaaf-191">パッケージを含む完全なパイプラインの作成</span><span class="sxs-lookup"><span data-stu-id="acaaf-191">Creating a full pipeline that includes packaging</span></span>

<span data-ttu-id="acaaf-192">利便性のため、パイプラインにはバージョン管理手順とパッケージ手順が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-192">To be useful, the pipeline should include a versioning step and a packaging step.</span></span> <span data-ttu-id="acaaf-193">これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) 拡張機能が有効になっていて、Azure DevOps 組織で Azure DevOps が有効化およびインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-193">Before you can add these steps to a pipeline, the [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) extension for Azure DevOps must be enabled and installed in the Azure DevOps organization.</span></span> <span data-ttu-id="acaaf-194">組織に拡張機能をインストールする方法の詳細については、[Azure DevOps のドキュメント](/azure/devops/marketplace/install-extension)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="acaaf-194">For information about how to install an extension for an organization, see the [Azure DevOps documentation](/azure/devops/marketplace/install-extension).</span></span>

<span data-ttu-id="acaaf-195">パイプライン全体は、少なくとも次の手順で構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-195">A full pipeline should consist of at least the following steps:</span></span>

1. <span data-ttu-id="acaaf-196">NuGet パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="acaaf-196">Install the NuGet packages.</span></span>
2. <span data-ttu-id="acaaf-197">[モデルバージョンを更新](pipeline-model-version.md)します。</span><span class="sxs-lookup"><span data-stu-id="acaaf-197">[Update the model versions](pipeline-model-version.md).</span></span>
3. <span data-ttu-id="acaaf-198">ソリューションまたはプロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="acaaf-198">Build the solution or projects.</span></span>
4. <span data-ttu-id="acaaf-199">エージェントに NuGet 3.3.0 またはそれ以前のバージョンをインストールします。</span><span class="sxs-lookup"><span data-stu-id="acaaf-199">Install NuGet 3.3.0 or earlier on the agent.</span></span> <span data-ttu-id="acaaf-200">(配置可能なパッケージを作成するステップでは、この手順が必要です)。</span><span class="sxs-lookup"><span data-stu-id="acaaf-200">(This step is required for the step that creates the deployable package.)</span></span>
5. <span data-ttu-id="acaaf-201">[配置可能パッケージを作成します](pipeline-create-deployable-package.md)。</span><span class="sxs-lookup"><span data-stu-id="acaaf-201">[Create the deployable package](pipeline-create-deployable-package.md).</span></span>
6. <span data-ttu-id="acaaf-202">配置可能パッケージ コンポーネントをビルド出力として発行します。</span><span class="sxs-lookup"><span data-stu-id="acaaf-202">Publish the deployable package artifact as the build output.</span></span>

<span data-ttu-id="acaaf-203">配置可能パッケージを作成するには、ビルド エージェントですぐに NuGet を使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-203">For the deployable package to be created, NuGet must be readily available on the build agent.</span></span> <span data-ttu-id="acaaf-204">したがって、パッケージを作成するステップの前に、Azure DevOps の **NuGetツール インストーラー** タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-204">Therefore, the **NuGet tool installer** task in Azure DevOps must be run before the step that creates the package.</span></span>

> [!NOTE]
> <span data-ttu-id="acaaf-205">ソース コード リポジトリに ISVs のようなサード パーティのバイナリ パッケージが含まれる場合は、パッケージ ステップに明示的に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="acaaf-205">If your source code repository includes binary packages from third parties like ISVs, you have to explicitly add those to the packaging step.</span></span> <span data-ttu-id="acaaf-206">詳細については、[Azure Pipelines での配置可能パッケージの作成](pipeline-create-deployable-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="acaaf-206">For more information, see [Create deployable packages in Azure Pipelines](pipeline-create-deployable-package.md).</span></span>

> [!NOTE]
> <span data-ttu-id="acaaf-207">NuGet バージョン 3.4 以降のセマンティック バージョニング機能のために、タスクによってバージョン 3.3.0 またはそれ以前のバージョンがインストールされることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="acaaf-207">Because of semantic versioning features in NuGet version 3.4 and later, make sure that the task installs version 3.3.0 or earlier.</span></span> <span data-ttu-id="acaaf-208">現在、配置可能パッケージの生成はセマンティック バージョニングをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="acaaf-208">Currently, deployable package generation doesn't support semantic versioning.</span></span>

### <a name="sample-pipeline-for-x-developers"></a><span data-ttu-id="acaaf-209">X++ 開発者のためのサンプル パイプライン</span><span class="sxs-lookup"><span data-stu-id="acaaf-209">Sample pipeline for X++ developers</span></span>

<span data-ttu-id="acaaf-210">[Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub リポジトリでは、既存の Azure DevOps プロジェクトにインポートできるサンプル パイプラインを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="acaaf-210">In the [Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub repository, you can find a sample pipeline that can be imported into an existing Azure DevOps project.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

