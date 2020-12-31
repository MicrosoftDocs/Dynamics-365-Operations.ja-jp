---
title: Azure Pipelines にある配置可能なパッケージへのライセンス ファイルの追加
description: このトピックでは、Microsoft Azure DevOps でビルドの自動化を実行するときに、既存のソフトウェア配置可能なパッケージにライセンス ファイルを追加する方法について説明します。
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
ms.openlocfilehash: 169fd55df3c3d737456dfc22f2a8e52102275108
ms.sourcegitcommit: 2186155e4662ae5010a190c0ede458ef6cf91f24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2020
ms.locfileid: "4409510"
---
# <a name="add-license-files-to-a-deployable-package-in-azure-pipelines"></a><span data-ttu-id="39394-103">Azure Pipelines にある配置可能なパッケージへのライセンス ファイルの追加</span><span class="sxs-lookup"><span data-stu-id="39394-103">Add license files to a deployable package in Azure Pipelines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39394-104">配置可能パッケージを使用して環境を更新する場合は、独立系ソフトウェアベンダー (ISV) またはパートナー X++ のソリューションに対してライセンスが必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="39394-104">When you update an environment by using a deployable package, a license might be required for independent software vendor (ISV) or partner X++ solutions.</span></span> <span data-ttu-id="39394-105">ISV は、リリースまたはビルド パイプラインのライセンスを自動的に追加するパイプラインを作成できます。</span><span class="sxs-lookup"><span data-stu-id="39394-105">ISVs can create pipelines to automatically include licenses in release or build pipelines.</span></span> <span data-ttu-id="39394-106">ユーザーは、独自のパイプラインを作成して、ISV 配置可能なパッケージとライセンス ファイルを結合することができます。</span><span class="sxs-lookup"><span data-stu-id="39394-106">Customers can create their own pipelines to combine the ISV deployable package and the license file.</span></span>

<span data-ttu-id="39394-107">このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を前提としています。</span><span class="sxs-lookup"><span data-stu-id="39394-107">This topic assumes a working knowledge of [Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started).</span></span>

> [!NOTE]
> <span data-ttu-id="39394-108">これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="39394-108">Before you can add these steps to a pipeline, the [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) extension for Azure DevOps must be enabled and installed in the Azure DevOps account.</span></span> <span data-ttu-id="39394-109">組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39394-109">For more information about how to install an extension for an organization, see [Install extensions](https://docs.microsoft.com/azure/devops/marketplace/install-extension).</span></span>

## <a name="adding-the-task-to-a-pipeline"></a><span data-ttu-id="39394-110">パイプラインへのタスクの追加</span><span class="sxs-lookup"><span data-stu-id="39394-110">Adding the task to a pipeline</span></span>

<span data-ttu-id="39394-111">YML または Classic パイプラインのビルドにタスクを追加するには、**配置可能なパッケージへのライセンスの追加** のタスク リストを検索します。</span><span class="sxs-lookup"><span data-stu-id="39394-111">To add the task to your build for the YML or Classic pipeline, search the task list for **Add Licenses to Deployable Package**.</span></span> <span data-ttu-id="39394-112">次のテーブルに、このタスクで使用可能なオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="39394-112">The following table describes the options that are available for this task.</span></span>

| <span data-ttu-id="39394-113">入力名</span><span class="sxs-lookup"><span data-stu-id="39394-113">Input name</span></span> | <span data-ttu-id="39394-114">必須</span><span class="sxs-lookup"><span data-stu-id="39394-114">Mandatory</span></span> | <span data-ttu-id="39394-115">説明</span><span class="sxs-lookup"><span data-stu-id="39394-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="39394-116">パッケージに追加するライセンス ファイルの検索パターン</span><span class="sxs-lookup"><span data-stu-id="39394-116">Search pattern for license files to add to the package</span></span> | <span data-ttu-id="39394-117">有</span><span class="sxs-lookup"><span data-stu-id="39394-117">Yes</span></span> | <span data-ttu-id="39394-118">ビルド エージェントのライセンス ファイルの一覧、またはビルド エージェントのファイルの検索パターン。</span><span class="sxs-lookup"><span data-stu-id="39394-118">A list of license files on the build agent, or a search pattern for files on the build agent.</span></span> <span data-ttu-id="39394-119">ライセンス ファイルをビルド エージェントで使用できるようにするには、それらをソース管理に追加します。</span><span class="sxs-lookup"><span data-stu-id="39394-119">To make the license files available on the build agent, you can add them to source control.</span></span> <span data-ttu-id="39394-120">また、パイプラインの前の手順でダウンロードまたは生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="39394-120">Alternatively, they can be downloaded or generated in an earlier step of the pipeline.</span></span> <span data-ttu-id="39394-121">詳細については、[ファイルの一致パターン リファレンス](https://docs.microsoft.com/azure/devops/pipelines/tasks/file-matching-patterns)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39394-121">For more information, see [File matching patterns reference](https://docs.microsoft.com/azure/devops/pipelines/tasks/file-matching-patterns).</span></span> |
| <span data-ttu-id="39394-122">更新する配置可能なパッケージのファイル名とパス</span><span class="sxs-lookup"><span data-stu-id="39394-122">Filename and path of the deployable package to update</span></span> | <span data-ttu-id="39394-123">有</span><span class="sxs-lookup"><span data-stu-id="39394-123">Yes</span></span> | <span data-ttu-id="39394-124">ライセンス ファイルを追加する既存の配置可能パッケージ zip ファイルのパスおよびファイル名。</span><span class="sxs-lookup"><span data-stu-id="39394-124">The path and file name of an existing deployable package zip file that the license files should be added to.</span></span> |
