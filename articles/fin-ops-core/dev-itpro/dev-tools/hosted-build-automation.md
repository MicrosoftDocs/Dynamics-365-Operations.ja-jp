---
title: Microsoft ホステッド エージェントと Azure Pipelines を使用するビルドの自動化
description: このトピックでは、Microsoft Azure DevOps でエージェントにおける X++ のビルド プロセスを自動化する方法について説明します。
author: jorisdg
manager: AnnBe
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 26731
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-03-05
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fd9d82e28f122bd9a761cbba6a4953244d250cc
ms.sourcegitcommit: 0efa93f11847a2b75d13cd0a49e716c76130ec44
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2020
ms.locfileid: "4409497"
---
# <a name="build-automation-that-uses-microsoft-hosted-agents-and-azure-pipelines"></a><span data-ttu-id="99832-103">Microsoft ホステッド エージェントと Azure Pipelines を使用するビルドの自動化</span><span class="sxs-lookup"><span data-stu-id="99832-103">Build automation that uses Microsoft-hosted agents and Azure Pipelines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99832-104">Microsoft Windows で実行される任意のビルド エージェントで、X++ コードのビルドと配置可能なパッケージの作成プロセスを自動化できます。</span><span class="sxs-lookup"><span data-stu-id="99832-104">You can automate the process of building X++ code and creating deployable packages on any build agent that run on Microsoft Windows.</span></span> <span data-ttu-id="99832-105">これらのエージェントには、[Microsoft-ホステッド エージェント](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted)が含まれています。</span><span class="sxs-lookup"><span data-stu-id="99832-105">These agents include [Microsoft-hosted agents](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted).</span></span> <span data-ttu-id="99832-106">この方法は、ビルド バーチャル マシン (VM) の配置の設定、保守、およびコストを回避するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="99832-106">This approach helps you avoid the setup, maintenance, and cost of deploying build virtual machines (VMs).</span></span> <span data-ttu-id="99832-107">また、ビルド エージェントの既存の設定を再利用して、他の .NET ビルド自動化を実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="99832-107">It also lets you reuse the existing setup of build agents to run other .NET build automation.</span></span>

> [!NOTE]
> <span data-ttu-id="99832-108">この機能は、コンパイルとパッケージングに限定されています。</span><span class="sxs-lookup"><span data-stu-id="99832-108">This feature is limited to compilation and packaging.</span></span> <span data-ttu-id="99832-109">このランタイムを必要とする X++ 単体テスト (SysTest)、データベースの同期、またはその他の機能 (Application Object Server \[AOS \]) やそのコンポーネントはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="99832-109">There is no support for X++ unit testing (SysTest), database synchronization, or other features that require the runtime (Application Object Server \[AOS\]) or its components.</span></span>

## <a name="prerequisites-for-building-x-code"></a><span data-ttu-id="99832-110">X++ コードをビルドするための前提条件</span><span class="sxs-lookup"><span data-stu-id="99832-110">Prerequisites for building X++ code</span></span>

### <a name="build-projects"></a><span data-ttu-id="99832-111">プロジェクトのビルド</span><span class="sxs-lookup"><span data-stu-id="99832-111">Build projects</span></span>

<span data-ttu-id="99832-112">Azure DevOps での X++ のビルドに .NET ツールを使用するには、Microsoft Build Engine (MSBuild) とカスタム X++ のターゲットが使用されます。</span><span class="sxs-lookup"><span data-stu-id="99832-112">To use .NET tools for building X++ in Azure DevOps, the Microsoft Build Engine (MSBuild) and custom X++ targets are used.</span></span> <span data-ttu-id="99832-113">X++ ソース コード レポジトリには、ビルドする各パッケージの X++ プロジェクトが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-113">Your X++ source code repository must contain an X++ project for each package that you have to build.</span></span> <span data-ttu-id="99832-114">オプションで、ソリューション ファイルを使用して、C# プロジェクトの依存関係を含むプロジェクトをグループ化したり、明示的なビルド順序を指定したりできます。</span><span class="sxs-lookup"><span data-stu-id="99832-114">You can optionally use a solution file to group the projects, including C# project dependencies, and provide an explicit build order.</span></span> <span data-ttu-id="99832-115">リポジトリにプロジェクトがまだ含まれていない場合は、Visual Studio にプロジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="99832-115">If the repository doesn't already contain a project, you can create a project in Visual Studio.</span></span>

> [!NOTE]
> <span data-ttu-id="99832-116">既存の X++ プロジェクト (rnrproj) を使用する場合は、プラットフォーム更新プログラム 27 以降の Visual Studio ツールを使用して、それを作成するか、または開いて保存しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-116">When you use an existing X++ project (rnrproj), make sure that you created it, or opened and saved it, by using Visual Studio tools on Platform update 27 or later.</span></span>
>
> <span data-ttu-id="99832-117">1 つのパッケージには複数のモデルを含めることができますが、常に完全にビルドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-117">Although a package can contain multiple models, it must always be built in its entirety.</span></span> <span data-ttu-id="99832-118">したがって、パッケージ全体をビルドするために必要なプロジェクトは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="99832-118">Therefore, only one project for just one of the models is required to build the whole package.</span></span> <span data-ttu-id="99832-119">また、プロジェクトにはオブジェクトを含める必要はありませんが、プロジェクトに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="99832-119">Additionally, although the project doesn't have to contain any objects, it can contain them.</span></span>

### <a name="nuget-packages"></a><span data-ttu-id="99832-120">NuGet パッケージ</span><span class="sxs-lookup"><span data-stu-id="99832-120">NuGet packages</span></span>

<span data-ttu-id="99832-121">X++ コードをビルドするには、X++ コンパイラ (xppc.exe) などの基本的な開発者ツールを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-121">To build X++ code, the basic developer tools such as the X++ compiler (xppc.exe) are required.</span></span> <span data-ttu-id="99832-122">また、アプリケーション プラットフォームやアプリケーション スイートなどの参照先パッケージは、コンパイルされた形式で使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-122">Additionally, any referenced packages, such as the Application Platform or Application Suite, must be available in a compiled format.</span></span> <span data-ttu-id="99832-123">このプロセスを有効にするために、Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリには、X++ ビルドを実行するために必要な NuGet パッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="99832-123">To enable this process, the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) provides NuGet packages that are required to do an X++ build.</span></span>

<span data-ttu-id="99832-124">次のパッケージは、共有アセット ライブラリからダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="99832-124">The following packages can be downloaded from the Shared asset library:</span></span>

- <span data-ttu-id="99832-125">**Microsoft.Dynamics.AX.Platform.CompilerPackage** – このパッケージには、ビルドを実行するために必要な X++コンパイラおよび関連ツールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="99832-125">**Microsoft.Dynamics.AX.Platform.CompilerPackage** – This package contains the X++ compiler and related tools that are required to do a build.</span></span>
- <span data-ttu-id="99832-126">**Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp** – このパッケージには、アプリケーション プラットフォームおよび関連モジュールのコンパイル済み X++ コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="99832-126">**Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp** – This package contains the compiled X++ code for the Application Platform and related modules.</span></span> <span data-ttu-id="99832-127">このコードは、ビルドに対して最適化されています。</span><span class="sxs-lookup"><span data-stu-id="99832-127">This code is optimized for building.</span></span>
- <span data-ttu-id="99832-128">**Microsoft.Dynamics.AX.Application.DevALM.BuildXpp** – このパッケージには、アプリケーション スイートおよび関連モジュールのコンパイル済み X++ コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="99832-128">**Microsoft.Dynamics.AX.Application.DevALM.BuildXpp** – This package contains the compiled X++ code for the Application Suite and related modules.</span></span> <span data-ttu-id="99832-129">このコードは、ビルドに対して最適化されています。</span><span class="sxs-lookup"><span data-stu-id="99832-129">This code optimized for building.</span></span>

<span data-ttu-id="99832-130">これらのパッケージを LCS からダウンロードし、ビルドを実行する Azure DevOps 組織内の Azure コンポーネント フィードに追加し ます。</span><span class="sxs-lookup"><span data-stu-id="99832-130">Download these packages from LCS, and add them to an Azure Artifacts feed in the Azure DevOps organization where the builds will run.</span></span> <span data-ttu-id="99832-131">Azure コンポーネントを作成し、NuGet パッケージを追加する方法の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="99832-131">For more information about how to create an Azure Artifacts feed and add NuGet packages, see these topics:</span></span>

- [<span data-ttu-id="99832-132">Azure DevOps サービスおよび TFS の NuGet パッケージの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="99832-132">Get started with NuGet packages in Azure DevOps Services and TFS</span></span>](https://docs.microsoft.com/azure/devops/artifacts/get-started-nuget)
- [<span data-ttu-id="99832-133">フィードの作成</span><span class="sxs-lookup"><span data-stu-id="99832-133">Create a feed</span></span>](https://docs.microsoft.com/azure/devops/artifacts/get-started-nuget#create-a-feed)
- [<span data-ttu-id="99832-134">独自の NuGet パッケージの作成と公開</span><span class="sxs-lookup"><span data-stu-id="99832-134">Create and publish your own NuGet package</span></span>](https://docs.microsoft.com/azure/devops/artifacts/get-started-nuget#create-and-publish-your-own-nuget-package)

> [!NOTE]
> <span data-ttu-id="99832-135">無料の Azure DevOps 組織には、Azure コンポーネントの限られたストレージしかありません。</span><span class="sxs-lookup"><span data-stu-id="99832-135">Free Azure DevOps organizations have limited storage for Azure Artifacts.</span></span> <span data-ttu-id="99832-136">ストレージ容量を解放するために、古いバージョンと使用していないバージョンを削除することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="99832-136">Consider deleting old and unused versions to free up storage capacity.</span></span> <span data-ttu-id="99832-137">詳細については、[Azure コンポーネントのサインアップ](https://docs.microsoft.com/azure/devops/artifacts/start-using-azure-artifacts#billing-and-free-monthly-usage) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99832-137">For more information, see [Sign up for Azure Artifacts](https://docs.microsoft.com/azure/devops/artifacts/start-using-azure-artifacts#billing-and-free-monthly-usage).</span></span>

<span data-ttu-id="99832-138">ビルド中に使用する必要があるパッケージを特定するには、ビルド時に nuget.exe ファイルと packages.config ファイルを用意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-138">To identify which packages should be used during the build, and where they can be found, you must provide a nuget.config file and a packages.config file during the build.</span></span> <span data-ttu-id="99832-139">これらのファイルを作成し、ソース管理リポジトリに追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="99832-139">We recommend that you create these files and add them to the source control repository.</span></span> <span data-ttu-id="99832-140">これらのファイルのパスは NuGet コマンドの明示的な入力であるため、ソース管理内の任意の場所にファイルを格納でき ます。</span><span class="sxs-lookup"><span data-stu-id="99832-140">The files can be stored anywhere in source control, because the paths of these files are explicit inputs for the NuGet command.</span></span>

<span data-ttu-id="99832-141">nuget.exe ファイルには、パッケージが格納されているソース フィードを持つ NuGet が含まれています。</span><span class="sxs-lookup"><span data-stu-id="99832-141">The nuget.config file provides NuGet with the source feed where the packages can be found.</span></span> <span data-ttu-id="99832-142">packages.config ファイルでは、パッケージとそのバージョンが指定されています。</span><span class="sxs-lookup"><span data-stu-id="99832-142">The packages.config file specifies the packages and their versions.</span></span> <span data-ttu-id="99832-143">新しいバージョンに対してビルドする場合は、packages.config ファイルのバージョンを更新するだけで済みます。</span><span class="sxs-lookup"><span data-stu-id="99832-143">To build against a newer version, you just have to update the versions in the packages.config file.</span></span> <span data-ttu-id="99832-144">サンプルの nuget.config ファイルを含む詳細については、[Azure Pipelines でのパッケージ管理 NuGet パッケージの復元](https://docs.microsoft.com/azure/devops/pipelines/packages/nuget-restore)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99832-144">For more information, including a sample nuget.config file, see [Restore Package Management NuGet packages in Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/packages/nuget-restore).</span></span>

<span data-ttu-id="99832-145">次の例は、一般的な X++ ビルドに必要な 3 つの主要なパッケージのための、packages.config ファイルを示しています。</span><span class="sxs-lookup"><span data-stu-id="99832-145">The following example shows a packages.config file for the three main packages that are required for a typical X++ build.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<packages>
    <package id="Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp" version="7.0.5644.16778" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.Application.DevALM.BuildXpp" version="10.0.464.13" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.Platform.CompilerPackage" version="7.0.5644.16778" targetFramework="net40" />
</packages>
```

## <a name="creating-the-pipeline"></a><span data-ttu-id="99832-146">パイプラインの作成</span><span class="sxs-lookup"><span data-stu-id="99832-146">Creating the pipeline</span></span>

<span data-ttu-id="99832-147">Azure DevOps は、ビルドを自動化するために使用できるパイプラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="99832-147">Azure DevOps provides pipelines that can be used to automate builds.</span></span> <span data-ttu-id="99832-148">パイプラインには、YML と Classic の 2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="99832-148">There are two types of pipelines: YML and Classic.</span></span> <span data-ttu-id="99832-149">YML パイプラインは、Git ソース管理リポジトリを使用している場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="99832-149">YML pipelines are available only when you use Git source control repositories.</span></span> <span data-ttu-id="99832-150">Classic パイプラインを使用して、Team Foundation バージョン管理 (TFVC) リポジトリをビルドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-150">Classic pipelines must be used to build Team Foundation Version Control (TFVC) repositories.</span></span> <span data-ttu-id="99832-151">詳細については、 [Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99832-151">For more information, see [Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started).</span></span>

<span data-ttu-id="99832-152">このセクションでは、パイプラインで X++ コードを作成するために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="99832-152">This section describes the steps that are required in a pipeline to build X++ code.</span></span> <span data-ttu-id="99832-153">[Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub リポジトリでは、既存の Azure DevOps プロジェクトにインポートできるサンプル パイプラインを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="99832-153">In the [Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub repository, you can find a sample pipeline that can be imported into an existing Azure DevOps project.</span></span>

### <a name="creating-a-basic-build-pipeline"></a><span data-ttu-id="99832-154">基本的なビルド パイプラインの作成</span><span class="sxs-lookup"><span data-stu-id="99832-154">Creating a basic build pipeline</span></span>

<span data-ttu-id="99832-155">X++ をコンパイルするための基本パイプラインには、2 つの手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="99832-155">A basic pipeline for compiling X++ requires only two steps:</span></span>

1. <span data-ttu-id="99832-156">NuGet パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="99832-156">Install the NuGet packages.</span></span>
2. <span data-ttu-id="99832-157">ソリューションまたはプロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="99832-157">Build the solution or projects.</span></span>

<span data-ttu-id="99832-158">抽出された NuGet パッケージの使用を容易にするために、**NuGet インストール** オプションを使用して、**-ExcludeVersion** [NuGet コマンドライン オプション](https://docs.microsoft.com/nuget/reference/cli-reference/cli-ref-install#options)を指定することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="99832-158">To simplify use of the extracted NuGet packages, consider using the **NuGet install** option and specifying the **-ExcludeVersion** [NuGet command-line option](https://docs.microsoft.com/nuget/reference/cli-reference/cli-ref-install#options).</span></span> <span data-ttu-id="99832-159">このようにして、パッケージのバージョンに関係なく、抽出されたパッケージ パスをビルドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="99832-159">In that way, the extracted package paths can be used in the build, regardless of the version of the packages.</span></span> <span data-ttu-id="99832-160">**NuGet インストーラー** タスクを使用し、**インストールの種類** フィールドを **インストール** に設定します。</span><span class="sxs-lookup"><span data-stu-id="99832-160">Use the **NuGet Installer** task, and set the **Installation type** field to **Install**.</span></span> <span data-ttu-id="99832-161">最後に、前の手順で作成した packages.config ファイルと nuget.config ファイルのパスを指定します。</span><span class="sxs-lookup"><span data-stu-id="99832-161">Finally, specify the path of the packages.config and nuget.config files that you created earlier.</span></span>

<span data-ttu-id="99832-162">次の NuGet 引数の例では、パッケージ バージョンに対してサブフォルダーが作成されないようにし、NuGet パッケージを **$(Pipeline.Workspace)\\NuGets** に展開します。</span><span class="sxs-lookup"><span data-stu-id="99832-162">The following example of NuGet arguments will prevent a subfolder from being created for the package versions and will extract the NuGet packages into **$(Pipeline.Workspace)\\NuGets**.</span></span>

`-ExcludeVersion -OutputDirectory "$(Pipeline.Workspace)\NuGets"`

<span data-ttu-id="99832-163">MSBuild を使用して X++ をビルドするには、いくつかの引数を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-163">To build X++ by using MSBuild, you must supply several arguments.</span></span> <span data-ttu-id="99832-164">ソリューションをビルドするパイプライン ステップでは、これらの引数を **MSBuild 引数** フィールドで指定できます。</span><span class="sxs-lookup"><span data-stu-id="99832-164">In the pipeline step that builds the solution, you can specify these arguments in the **MSBuild Arguments** field.</span></span>

| <span data-ttu-id="99832-165">引数</span><span class="sxs-lookup"><span data-stu-id="99832-165">Argument</span></span> | <span data-ttu-id="99832-166">説明</span><span class="sxs-lookup"><span data-stu-id="99832-166">Description</span></span> |
| --- | --- |
| <span data-ttu-id="99832-167">/p:BuildTasksDirectory</span><span class="sxs-lookup"><span data-stu-id="99832-167">/p:BuildTasksDirectory</span></span> | <span data-ttu-id="99832-168">抽出されたコンパイラ ツール NuGet パッケージのパス (DevAlm フォルダー内のサブフォルダを含む)。</span><span class="sxs-lookup"><span data-stu-id="99832-168">The path of the extracted Compiler Tools NuGet package, including the subfolders in the DevAlm folder.</span></span> |
| <span data-ttu-id="99832-169">/p:MetadataDirectory</span><span class="sxs-lookup"><span data-stu-id="99832-169">/p:MetadataDirectory</span></span> | <span data-ttu-id="99832-170">X++ ソース コードのパス。</span><span class="sxs-lookup"><span data-stu-id="99832-170">The path of the X++ source code.</span></span> |
| <span data-ttu-id="99832-171">/p:FrameworkDirectory</span><span class="sxs-lookup"><span data-stu-id="99832-171">/p:FrameworkDirectory</span></span> | <span data-ttu-id="99832-172">抽出されたコンパイラ ツール NuGet パッケージのパス。</span><span class="sxs-lookup"><span data-stu-id="99832-172">The path of the extracted Compiler Tools NuGet package.</span></span> |
| <span data-ttu-id="99832-173">/p:ReferenceFolder</span><span class="sxs-lookup"><span data-stu-id="99832-173">/p:ReferenceFolder</span></span> | <span data-ttu-id="99832-174">コンパイルで参照され、必須である X++ パッケージのバイナリを含むパスのセミコロン区切りのリスト (アプリケーション プラットフォームやアプリケーション スイートなど)。</span><span class="sxs-lookup"><span data-stu-id="99832-174">A semicolon-separated list of paths that contain binaries of X++ packages that are referenced and required for compilation (for example, Application Platform and Application Suite).</span></span> <span data-ttu-id="99832-175">コンパイルするコードに互いを参照する複数のパッケージがある場合は、出力ディレクトリもここに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-175">If the code that will be compiled has multiple packages that reference each other, the output directory should also be included here.</span></span> |
| <span data-ttu-id="99832-176">/p:ReferencePath</span><span class="sxs-lookup"><span data-stu-id="99832-176">/p:ReferencePath</span></span> | <span data-ttu-id="99832-177">コンパイル時に参照され、必須である X++ 以外のすべてのバイナリを含むパスのセミコロン区切りのリスト。</span><span class="sxs-lookup"><span data-stu-id="99832-177">A semicolon-separated list of paths that contain any non-X++ binaries that are referenced and required for compilation.</span></span> <span data-ttu-id="99832-178">必要な参照が含まれている場合があるため、抽出したコンパイラ ツール NuGet パッケージの場所を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-178">You should include the location of the extracted Compiler Tools NuGet package, because it might contain required references.</span></span> |
| <span data-ttu-id="99832-179">/p:OutputDirectory</span><span class="sxs-lookup"><span data-stu-id="99832-179">/p:OutputDirectory</span></span> | <span data-ttu-id="99832-180">コンパイラがフォルダーとバイナリを作成するパス。</span><span class="sxs-lookup"><span data-stu-id="99832-180">The path where the compiler will create folders and binaries.</span></span> |

<span data-ttu-id="99832-181">次の MSBuild 引数の例では、NuGet パッケージが **$(Pipeline.Workspace)\\NuGets** にインストールされており、X++ のソース コードが **$(Build.SourcesDirectory)\\Metadata** 内にあり、コンパイラの出力を **$(Build.BinariesDirectory)** にする必要があることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="99832-181">The following example of MSBuild arguments assumes that the NuGet packages are installed in **$(Pipeline.Workspace)\\NuGets**, the X++ source code is in **$(Build.SourcesDirectory)\\Metadata**, and the output of the compiler should go in **$(Build.BinariesDirectory)**.</span></span>

```plaintext
/p:BuildTasksDirectory="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage\DevAlm"
/p:MetadataDirectory="$(Build.SourcesDirectory)\Metadata"
/p:FrameworkDirectory="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage"
/p:ReferenceFolder="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp\ref\net40;$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Application.DevALM.BuildXpp\ref\net40;$(Build.SourcesDirectory)\Metadata;$(Build.BinariesDirectory)"
/p:ReferencePath="$(Pipeline.Workspace)\NuGets\Microsoft.Dynamics.AX.Platform.CompilerPackage" /p:OutputDirectory="$(Build.BinariesDirectory)"
```

<span data-ttu-id="99832-182">パイプライン サンプルでは、NuGet パッケージ名とパスの変数を使用して、これらのコマンドを簡略化しています。</span><span class="sxs-lookup"><span data-stu-id="99832-182">In the pipeline samples, variables for NuGet package names and paths are used to simplify these commands.</span></span>

### <a name="creating-a-full-pipeline-that-includes-packaging"></a><span data-ttu-id="99832-183">パッケージを含む完全なパイプラインの作成</span><span class="sxs-lookup"><span data-stu-id="99832-183">Creating a full pipeline that includes packaging</span></span>

<span data-ttu-id="99832-184">利便性のため、パイプラインにはバージョン管理手順とパッケージ手順が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-184">To be useful, the pipeline should include a versioning step and a packaging step.</span></span> <span data-ttu-id="99832-185">これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-185">Before you can add these steps to a pipeline, the [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) extension for Azure DevOps must be enabled and installed in the Azure DevOps account.</span></span> <span data-ttu-id="99832-186">組織に拡張機能をインストールする方法の詳細については、[Azure DevOps のドキュメント](https://docs.microsoft.com/azure/devops/marketplace/install-extension)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99832-186">For information about how to install an extension for an organization, see the [Azure DevOps documentation](https://docs.microsoft.com/azure/devops/marketplace/install-extension).</span></span>

<span data-ttu-id="99832-187">パイプライン全体は、少なくとも次の手順で構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-187">A full pipeline should consist of at least the following steps:</span></span>

1. <span data-ttu-id="99832-188">NuGet パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="99832-188">Install the NuGet packages.</span></span>
2. <span data-ttu-id="99832-189">[モデルバージョンを更新](pipeline-model-version.md)します。</span><span class="sxs-lookup"><span data-stu-id="99832-189">[Update the model versions](pipeline-model-version.md).</span></span>
3. <span data-ttu-id="99832-190">ソリューションまたはプロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="99832-190">Build the solution or projects.</span></span>
4. <span data-ttu-id="99832-191">エージェントに NuGet 3.3.0 またはそれ以前のバージョンをインストールします。</span><span class="sxs-lookup"><span data-stu-id="99832-191">Install NuGet 3.3.0 or earlier on the agent.</span></span> <span data-ttu-id="99832-192">(配置可能なパッケージを作成するステップでは、この手順が必要です)。</span><span class="sxs-lookup"><span data-stu-id="99832-192">(This step is required for the step that creates the deployable package.)</span></span>
5. <span data-ttu-id="99832-193">[配置可能パッケージを作成します](pipeline-create-deployable-package.md)。</span><span class="sxs-lookup"><span data-stu-id="99832-193">[Create the deployable package](pipeline-create-deployable-package.md).</span></span>
6. <span data-ttu-id="99832-194">配置可能パッケージ コンポーネントをビルド出力として発行します。</span><span class="sxs-lookup"><span data-stu-id="99832-194">Publish the deployable package artifact as the build output.</span></span>

<span data-ttu-id="99832-195">配置可能パッケージを作成するには、ビルド エージェントですぐに NuGet を使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-195">For the deployable package to be created, NuGet must be readily available on the build agent.</span></span> <span data-ttu-id="99832-196">したがって、パッケージを作成するステップの前に、Azure DevOps の **NuGetツール インストーラー** タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99832-196">Therefore, the **NuGet tool installer** task in Azure DevOps must be run before the step that creates the package.</span></span>

> [!NOTE]
> <span data-ttu-id="99832-197">NuGet バージョン 3.4 以降のセマンティック バージョニング機能のために、タスクによってバージョン 3.3.0 またはそれ以前のバージョンがインストールされることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="99832-197">Because of semantic versioning features in NuGet version 3.4 and later, make sure that the task installs version 3.3.0 or earlier.</span></span> <span data-ttu-id="99832-198">現在、配置可能パッケージの生成はセマンティック バージョニングをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="99832-198">Currently, deployable package generation doesn't support semantic versioning.</span></span>

### <a name="sample-pipeline-for-x-developers"></a><span data-ttu-id="99832-199">X++ 開発者のためのサンプル パイプライン</span><span class="sxs-lookup"><span data-stu-id="99832-199">Sample pipeline for X++ developers</span></span>

<span data-ttu-id="99832-200">[Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub リポジトリでは、既存の Azure DevOps プロジェクトにインポートできるサンプル パイプラインを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="99832-200">In the [Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub repository, you can find a sample pipeline that can be imported into an existing Azure DevOps project.</span></span>
