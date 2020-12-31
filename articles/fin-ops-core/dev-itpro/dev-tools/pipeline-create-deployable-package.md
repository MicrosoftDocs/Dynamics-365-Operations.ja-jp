---
title: Azure Pipelines に配置可能なパッケージの作成
description: このトピックでは、Microsoft Azure DevOps でビルドの自動化を実行するときに、ソフトウェア配置可能なパッケージを作成する方法について説明します。
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
ms.openlocfilehash: 119185a6e80376cdf90d384a71c61fdf1e1d6d5e
ms.sourcegitcommit: 2186155e4662ae5010a190c0ede458ef6cf91f24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2020
ms.locfileid: "4409511"
---
# <a name="create-deployable-packages-in-azure-pipelines"></a><span data-ttu-id="92f55-103">Azure Pipelines に配置可能なパッケージの作成</span><span class="sxs-lookup"><span data-stu-id="92f55-103">Create deployable packages in Azure Pipelines</span></span>

<span data-ttu-id="92f55-104">カスタマイズを環境に配置する場合は、配置可能なパッケージが Microsoft Dynamics Lifecycle Services (LCS) に必要です。</span><span class="sxs-lookup"><span data-stu-id="92f55-104">If you want to deploy customizations to an environment, a deployable package is required in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="92f55-105">このパッケージは、ビルド プロセスまたはリリース プロセス中に Azure Pipelines を使用して作成できます。</span><span class="sxs-lookup"><span data-stu-id="92f55-105">You can create this package by using Azure Pipelines during a build or release process.</span></span>

<span data-ttu-id="92f55-106">このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を前提としています。</span><span class="sxs-lookup"><span data-stu-id="92f55-106">This topic assumes a working knowledge of [Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started).</span></span>

> [!NOTE]
> <span data-ttu-id="92f55-107">これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="92f55-107">Before you can add these steps to a pipeline, the [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) extension for Azure DevOps must be enabled and installed in the Azure DevOps account.</span></span> <span data-ttu-id="92f55-108">組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92f55-108">For more information about how to install an extension for an organization, see [Install extensions](https://docs.microsoft.com/azure/devops/marketplace/install-extension).</span></span>
>
> <span data-ttu-id="92f55-109">この Azure DevOps タスクを実行するには、エージェントで X++ コンパイラ ツールを使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="92f55-109">This Azure DevOps task requires that the X++ compiler tools be available on the agent.</span></span> <span data-ttu-id="92f55-110">このタスクをビルド バーチャル マシン (VM) エージェントで実行するか、コンパイラ ツール NuGetパッケージを使用してください。</span><span class="sxs-lookup"><span data-stu-id="92f55-110">Either run this task on a build virtual machine (VM) agent, or use the Compiler Tools NuGet package.</span></span> <span data-ttu-id="92f55-111">NuGet パッケージとパイプラインへのインストール方法の詳細については、[Microsoft がホストするエージェントと Azure Pipelines を使用したビルドの自動化](hosted-build-automation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92f55-111">For more information about the NuGet package and how to install it in a pipeline, see [Build automation using Microsoft-hosted agents and Azure Pipelines](hosted-build-automation.md).</span></span>

## <a name="add-the-task-to-a-pipeline"></a><span data-ttu-id="92f55-112">パイプラインへのタスクの追加</span><span class="sxs-lookup"><span data-stu-id="92f55-112">Add the task to a pipeline</span></span>

<span data-ttu-id="92f55-113">YML または Classic パイプラインのビルドにタスクを追加するには、**配置可能なパッケージの作成** のタスク リストを検索します。</span><span class="sxs-lookup"><span data-stu-id="92f55-113">To add the task to the build of your YML or Classic pipeline, search the task list for **Create Deployable Package**.</span></span> <span data-ttu-id="92f55-114">次のテーブルに、このタスクで使用可能なオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="92f55-114">The following table describes the options that are available for this task.</span></span>

| <span data-ttu-id="92f55-115">入力名</span><span class="sxs-lookup"><span data-stu-id="92f55-115">Input name</span></span> | <span data-ttu-id="92f55-116">必須</span><span class="sxs-lookup"><span data-stu-id="92f55-116">Mandatory</span></span> | <span data-ttu-id="92f55-117">説明</span><span class="sxs-lookup"><span data-stu-id="92f55-117">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="92f55-118">X++ ツール パス</span><span class="sxs-lookup"><span data-stu-id="92f55-118">X++ Tools Path</span></span> | <span data-ttu-id="92f55-119">有</span><span class="sxs-lookup"><span data-stu-id="92f55-119">Yes</span></span> | <span data-ttu-id="92f55-120">X++ ツールの場所のパス。</span><span class="sxs-lookup"><span data-stu-id="92f55-120">The path of the location of the X++ tools.</span></span> <span data-ttu-id="92f55-121">この場所は、ビルド VM 上の **PackagesLocalDirectory\\bin** フォルダーの場所か、コンパイラ ツール NuGet パッケージの抽出された NuGet ファイルの場所です。</span><span class="sxs-lookup"><span data-stu-id="92f55-121">This location is either the **PackagesLocalDirectory\\bin** folder location on a build VM, or the location of the extracted NuGet file of the Compiler Tools NuGet package.</span></span> |
| <span data-ttu-id="92f55-122">パッケージに対する X++ バイナリの場所</span><span class="sxs-lookup"><span data-stu-id="92f55-122">Location of the X++ binaries to package</span></span> | <span data-ttu-id="92f55-123">有</span><span class="sxs-lookup"><span data-stu-id="92f55-123">Yes</span></span> | <span data-ttu-id="92f55-124">配置可能パッケージに含める X++ パッケージ (モジュール) のすべてのバイナリが格納されているフォルダーのパス。</span><span class="sxs-lookup"><span data-stu-id="92f55-124">The path that contains the folders that contain all the binaries for the X++ packages (modules) that you want to include in the deployable package.</span></span> <span data-ttu-id="92f55-125">ビルド パイプラインでこのタスクを使用する場合、このフォルダーは通常、コンパイラの出力フォルダーと同じです。</span><span class="sxs-lookup"><span data-stu-id="92f55-125">If this task is used in a build pipeline, this folder is typically the same as the compiler output folder.</span></span> |
| <span data-ttu-id="92f55-126">パッケージ化するバイナリの検索パターン</span><span class="sxs-lookup"><span data-stu-id="92f55-126">Search pattern for binaries to package</span></span> | <span data-ttu-id="92f55-127">有</span><span class="sxs-lookup"><span data-stu-id="92f55-127">Yes</span></span> | <span data-ttu-id="92f55-128">**パッケージへの X++ バイナリの場所** オプションで指定されているパス内で、X++ パッケージ (モジュール) 名に一致する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="92f55-128">Provide a name matching pattern for X++ package (module) names inside the path that is specified in the **Location of the X++ binaries to package** option.</span></span> <span data-ttu-id="92f55-129">検索パターンの代わりに名前の一覧を指定したり、テスト パッケージが含まれていないように除外フィルターを指定したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="92f55-129">You can also specify a list of names instead of search patterns, or you can specify exclusion filters so that, for example, test packages aren't included.</span></span> <span data-ttu-id="92f55-130">詳細については、[ファイルの一致パターン リファレンス](https://docs.microsoft.com/azure/devops/pipelines/tasks/file-matching-patterns)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92f55-130">For more information, see [File matching patterns reference](https://docs.microsoft.com/azure/devops/pipelines/tasks/file-matching-patterns).</span></span> |
| <span data-ttu-id="92f55-131">配置可能なパッケージのファイル名とパス</span><span class="sxs-lookup"><span data-stu-id="92f55-131">Filename and path for the deployable package</span></span> | <span data-ttu-id="92f55-132">有</span><span class="sxs-lookup"><span data-stu-id="92f55-132">Yes</span></span> | <span data-ttu-id="92f55-133">配置可能なパッケージのパスとファイル名。</span><span class="sxs-lookup"><span data-stu-id="92f55-133">The path and file name of the deployable package.</span></span> <span data-ttu-id="92f55-134">出力ファイルは zip ファイルであり、ファイル名には通常、ファイルを識別しやすいようにするためのバージョン情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="92f55-134">The output file is a zip file, and the file name typically includes version information to make the file easy to identify.</span></span> |

## <a name="nuget-dependency"></a><span data-ttu-id="92f55-135">NuGet の依存関係</span><span class="sxs-lookup"><span data-stu-id="92f55-135">NuGet dependency</span></span>

<span data-ttu-id="92f55-136">ビルド VM でこのタスクを実行すると、NuGet が既に使用可能になっており、アクションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="92f55-136">When this task is run on the build VM, NuGet is already available, and no action is required.</span></span> <span data-ttu-id="92f55-137">ただし、このタスクをホストされたエージェントまたはその他のプライベート エージェントで実行する場合は、NuGet がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="92f55-137">However, when this task is run on hosted agents or other private agents, NuGet must be installed.</span></span> <span data-ttu-id="92f55-138">この場合、Azure DevOps には、パッケージを作成するタスクを実行する前に実行できる [NuGet ツール インストーラー タスク](https://docs.microsoft.com/azure/devops/pipelines/tasks/tool/nuget)があります。</span><span class="sxs-lookup"><span data-stu-id="92f55-138">In this case, Azure DevOps has the [NuGet Tool Installer task](https://docs.microsoft.com/azure/devops/pipelines/tasks/tool/nuget) that you can run before you run the task to create the package.</span></span>

> [!NOTE]
> <span data-ttu-id="92f55-139">NuGet バージョン 3.4 以降のセマンティック バージョニングが導入されたため、バージョン 3.3.0 またはそれ以前のバージョンをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92f55-139">Because of the introduction of semantic versioning in NuGet version 3.4 and later, you must install version 3.3.0 or earlier.</span></span>
