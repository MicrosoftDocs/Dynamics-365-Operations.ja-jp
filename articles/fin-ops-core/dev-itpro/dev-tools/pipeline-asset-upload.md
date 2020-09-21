---
title: Azure Pipelines を使用した資産のアップロード
description: このトピックでは、Azure Pipelines を使用して、LCS アセット ライブラリへ資産をアップロードする方法について説明します。
author: jorisdg
manager: AnnBe
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 26731
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4996bcc8da49f188bbd7bffef66b6c58b6c139e9
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2020
ms.locfileid: "3765091"
---
# <a name="upload-assets-by-using-azure-pipelines"></a><span data-ttu-id="5ec94-103">Azure Pipelines を使用した資産のアップロード</span><span class="sxs-lookup"><span data-stu-id="5ec94-103">Upload assets by using Azure Pipelines</span></span>

<span data-ttu-id="5ec94-104">Azure DevOps の **Lifecycle Services (LCS) 資産のアップロード** タスクを使用して、**Lifecycle Services アセット ライブラリ** へ資産を自動的にアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="5ec94-104">You can automate uploading assets to the **Lifecycle Services Asset Library** by using the **Deploy Lifecycle Services (LCS) Asset Upload** task in Azure DevOps.</span></span> <span data-ttu-id="5ec94-105">このタスクは **リリース** パイプラインでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ec94-105">The task is only available in **Releases** pipelines.</span></span>

<span data-ttu-id="5ec94-106">このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started?view=azure-devops) の実用的な知識を持っていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="5ec94-106">This topic assumes you have a working knowledge of [Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started?view=azure-devops).</span></span>

> [!NOTE]
> <span data-ttu-id="5ec94-107">これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ec94-107">Before you can add these steps to a pipeline, the [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) extension for Azure DevOps must be enabled and installed in the Azure DevOps account.</span></span> <span data-ttu-id="5ec94-108">組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension?view=azure-devops&tabs=browser)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ec94-108">For more information about how to install an extension for an organization, see [Install extensions](https://docs.microsoft.com/azure/devops/marketplace/install-extension?view=azure-devops&tabs=browser).</span></span>

## <a name="add-the-task-to-a-pipeline"></a><span data-ttu-id="5ec94-109">パイプラインへのタスクの追加</span><span class="sxs-lookup"><span data-stu-id="5ec94-109">Add the task to a pipeline</span></span>

<span data-ttu-id="5ec94-110">YML または Classic パイプラインのビルドにタスクを追加するには、**Dynamics Lifecycle Services (LCS) 資産 アップロード** のタスク リストを検索します。</span><span class="sxs-lookup"><span data-stu-id="5ec94-110">To add the task to the build of your YML or Classic pipeline, search the task list for **Dynamics Lifecycle Services (LCS) Asset Upload**.</span></span>

<span data-ttu-id="5ec94-111">次のテーブルに、このタスクで使用可能なオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="5ec94-111">The following table describes the options that are available for this task.</span></span>

| <span data-ttu-id="5ec94-112">入力名</span><span class="sxs-lookup"><span data-stu-id="5ec94-112">Input name</span></span> | <span data-ttu-id="5ec94-113">必須</span><span class="sxs-lookup"><span data-stu-id="5ec94-113">Mandatory</span></span> | <span data-ttu-id="5ec94-114">説明</span><span class="sxs-lookup"><span data-stu-id="5ec94-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5ec94-115">LCS 接続</span><span class="sxs-lookup"><span data-stu-id="5ec94-115">LCS Connection</span></span> | <span data-ttu-id="5ec94-116">有</span><span class="sxs-lookup"><span data-stu-id="5ec94-116">Yes</span></span> | <span data-ttu-id="5ec94-117">Dynamics Lifecycle Services (LCS) へのサービス接続を選択または作成します。</span><span class="sxs-lookup"><span data-stu-id="5ec94-117">Select or create a service connection to Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5ec94-118">詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ec94-118">For more information, see [Creating an LCS connection in Azure Pipelines](pipeline-lcs-connection.md).</span></span> |
| <span data-ttu-id="5ec94-119">LCS プロジェクト ID</span><span class="sxs-lookup"><span data-stu-id="5ec94-119">LCS Project ID</span></span> | <span data-ttu-id="5ec94-120">有</span><span class="sxs-lookup"><span data-stu-id="5ec94-120">Yes</span></span> | <span data-ttu-id="5ec94-121">配置する両方の試算と、ターゲット環境を含む、LCS のプロジェクトを識別するプロジェクト ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec94-121">Enter the project ID identifying the project in LCS that contains both the asset to be deployed, and the target environment.</span></span> <span data-ttu-id="5ec94-122">プロジェクト ID は、プロジェクトのダッシュボードの URL の末尾に記載できます。</span><span class="sxs-lookup"><span data-stu-id="5ec94-122">YOu can find the project ID at the end of the URL of your project's dashboard.</span></span> |
| <span data-ttu-id="5ec94-123">資産 タイプ</span><span class="sxs-lookup"><span data-stu-id="5ec94-123">Type of asset</span></span> | <span data-ttu-id="5ec94-124">有</span><span class="sxs-lookup"><span data-stu-id="5ec94-124">Yes</span></span> | <span data-ttu-id="5ec94-125">アップロードする資産のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec94-125">Select the type of asset you wish to upload.</span></span> |
| <span data-ttu-id="5ec94-126">アップロードするファイル</span><span class="sxs-lookup"><span data-stu-id="5ec94-126">File to upload</span></span> | <span data-ttu-id="5ec94-127">有</span><span class="sxs-lookup"><span data-stu-id="5ec94-127">Yes</span></span> | <span data-ttu-id="5ec94-128">LCS **アセット ライブラリ** にアップロードするファイルへのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec94-128">Enter the path to the file to upload into the LCS **Asset Library**.</span></span> |
| <span data-ttu-id="5ec94-129">LCS 資産の名前</span><span class="sxs-lookup"><span data-stu-id="5ec94-129">LCS Asset Name</span></span> | <span data-ttu-id="5ec94-130">第        条</span><span class="sxs-lookup"><span data-stu-id="5ec94-130">No</span></span> | <span data-ttu-id="5ec94-131">**アセット ライブラリ** に表示する、資産の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec94-131">Enter a name for the asset to be shown in the **Asset Library**.</span></span> <span data-ttu-id="5ec94-132">名前が指定されていない場合は、ファイル名が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ec94-132">If no name is specified, the file name will be used.</span></span> |
| <span data-ttu-id="5ec94-133">LCS の説明</span><span class="sxs-lookup"><span data-stu-id="5ec94-133">LCS Description</span></span> | <span data-ttu-id="5ec94-134">第        条</span><span class="sxs-lookup"><span data-stu-id="5ec94-134">No</span></span> | <span data-ttu-id="5ec94-135">アセット の詳細に表示する、資産の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec94-135">Enter a description for the asset to be shown in the asset details.</span></span> |
| <span data-ttu-id="5ec94-136">検証を待機する</span><span class="sxs-lookup"><span data-stu-id="5ec94-136">Wait for Validation</span></span> | <span data-ttu-id="5ec94-137">第        条</span><span class="sxs-lookup"><span data-stu-id="5ec94-137">No</span></span> | <span data-ttu-id="5ec94-138">検証が必要な資産タイプの場合、このチェック ボックスをオンにすると、タスクは、資産の検証が成功または失敗するまで待機するようになります。</span><span class="sxs-lookup"><span data-stu-id="5ec94-138">For asset types that require validation, this checkbox instructs the task to wait until the validation of the asset has either succeeded or failed.</span></span> |
