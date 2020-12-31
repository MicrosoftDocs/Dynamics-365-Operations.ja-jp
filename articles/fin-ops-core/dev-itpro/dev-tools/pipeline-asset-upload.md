---
title: Azure Pipelines を使用した資産のアップロード
description: このトピックでは、Azure Pipelines を使用して、Microsoft Dynamics Lifecycle Services (LCS) で資産をアセット ライブラリにアップロードする方法について説明します。
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
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d9f75a98f79dca532f062b6b1eaed65ad29ae7e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408723"
---
# <a name="upload-assets-by-using-azure-pipelines"></a><span data-ttu-id="351b6-103">Azure Pipelines を使用した資産のアップロード</span><span class="sxs-lookup"><span data-stu-id="351b6-103">Upload assets by using Azure Pipelines</span></span>

<span data-ttu-id="351b6-104">Azure DevOps の **Lifecycle Services (LCS) 資産のアップロード** タスクを使用して、 Microsoft Dynamics Lifecycle Services (LCS) で資産をアセット ライブラリに自動的にアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="351b6-104">You can automate the upload of assets to the Asset library in Microsoft Dynamics Lifecycle Services (LCS) by using the **Deploy Lifecycle Services (LCS) Asset Upload** task in Azure DevOps.</span></span> <span data-ttu-id="351b6-105">このタスク **リリース** パイプラインでのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="351b6-105">This task is available only in **Releases** pipelines.</span></span>

<span data-ttu-id="351b6-106">このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を持っていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="351b6-106">This topic assumes you have a working knowledge of [Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started).</span></span>

> [!NOTE]
> <span data-ttu-id="351b6-107">これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="351b6-107">Before you can add these steps to a pipeline, the [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) extension for Azure DevOps must be enabled and installed in the Azure DevOps account.</span></span> <span data-ttu-id="351b6-108">組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="351b6-108">For more information about how to install an extension for an organization, see [Install extensions](https://docs.microsoft.com/azure/devops/marketplace/install-extension).</span></span>

## <a name="add-the-task-to-a-pipeline"></a><span data-ttu-id="351b6-109">パイプラインへのタスクの追加</span><span class="sxs-lookup"><span data-stu-id="351b6-109">Add the task to a pipeline</span></span>

<span data-ttu-id="351b6-110">YML または Classic パイプラインのビルドにタスクを追加するには、**Dynamics Lifecycle Services (LCS) 資産 アップロード** のタスク リストを検索します。</span><span class="sxs-lookup"><span data-stu-id="351b6-110">To add the task to the build of your YML or Classic pipeline, search the task list for **Dynamics Lifecycle Services (LCS) Asset Upload**.</span></span>

<span data-ttu-id="351b6-111">次のテーブルに、このタスクで使用可能なオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="351b6-111">The following table describes the options that are available for this task.</span></span>

| <span data-ttu-id="351b6-112">入力名</span><span class="sxs-lookup"><span data-stu-id="351b6-112">Input name</span></span> | <span data-ttu-id="351b6-113">必須</span><span class="sxs-lookup"><span data-stu-id="351b6-113">Mandatory</span></span> | <span data-ttu-id="351b6-114">説明</span><span class="sxs-lookup"><span data-stu-id="351b6-114">Description</span></span> |
|---|---|---|
| <span data-ttu-id="351b6-115">LCS 接続</span><span class="sxs-lookup"><span data-stu-id="351b6-115">LCS Connection</span></span> | <span data-ttu-id="351b6-116">あり</span><span class="sxs-lookup"><span data-stu-id="351b6-116">Yes</span></span> | <span data-ttu-id="351b6-117">LCS へのサービス接続を選択または作成します。</span><span class="sxs-lookup"><span data-stu-id="351b6-117">Select or create a service connection to LCS.</span></span> <span data-ttu-id="351b6-118">詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="351b6-118">For more information, see [Create an LCS connection in Azure Pipelines](pipeline-lcs-connection.md).</span></span> |
| <span data-ttu-id="351b6-119">LCS プロジェクト ID</span><span class="sxs-lookup"><span data-stu-id="351b6-119">LCS Project ID</span></span> | <span data-ttu-id="351b6-120">あり</span><span class="sxs-lookup"><span data-stu-id="351b6-120">Yes</span></span> | <span data-ttu-id="351b6-121">配置する資産およびターゲット環境の両方を含むプロジェクトの ID を LCS に入力します。</span><span class="sxs-lookup"><span data-stu-id="351b6-121">Enter the ID of the project in LCS that contains both the asset to deploy and the target environment.</span></span> <span data-ttu-id="351b6-122">プロジェクト ID は、プロジェクトのダッシュボードの URL の末尾に記載できます。</span><span class="sxs-lookup"><span data-stu-id="351b6-122">You can find the project ID at the end of the URL of your project's dashboard.</span></span> |
| <span data-ttu-id="351b6-123">資産 タイプ</span><span class="sxs-lookup"><span data-stu-id="351b6-123">Type of asset</span></span> | <span data-ttu-id="351b6-124">あり</span><span class="sxs-lookup"><span data-stu-id="351b6-124">Yes</span></span> | <span data-ttu-id="351b6-125">アップロードする資産のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="351b6-125">Select the type of asset to upload.</span></span> |
| <span data-ttu-id="351b6-126">アップロードするファイル</span><span class="sxs-lookup"><span data-stu-id="351b6-126">File to upload</span></span> | <span data-ttu-id="351b6-127">あり</span><span class="sxs-lookup"><span data-stu-id="351b6-127">Yes</span></span> | <span data-ttu-id="351b6-128">LCS アセット ライブラリにアップロードしたいファイルへのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="351b6-128">Enter the path of the file that you want to upload into the Asset library in LCS.</span></span> |
| <span data-ttu-id="351b6-129">LCS 資産の名前</span><span class="sxs-lookup"><span data-stu-id="351b6-129">LCS Asset Name</span></span> | <span data-ttu-id="351b6-130">なし</span><span class="sxs-lookup"><span data-stu-id="351b6-130">No</span></span> | <span data-ttu-id="351b6-131">アセット ライブラリに表示する、資産の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="351b6-131">Enter the name to show for the asset in the Asset library.</span></span> <span data-ttu-id="351b6-132">ここで名前を入力しない場合は、ファイル名が使用されます。</span><span class="sxs-lookup"><span data-stu-id="351b6-132">If you don't enter a name here, the file name will be used.</span></span> |
| <span data-ttu-id="351b6-133">LCS の説明</span><span class="sxs-lookup"><span data-stu-id="351b6-133">LCS Description</span></span> | <span data-ttu-id="351b6-134">なし</span><span class="sxs-lookup"><span data-stu-id="351b6-134">No</span></span> | <span data-ttu-id="351b6-135">資産の詳細に資産を表示する説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="351b6-135">Enter the description to show for the asset in the asset details.</span></span> |
| <span data-ttu-id="351b6-136">検証を待機する</span><span class="sxs-lookup"><span data-stu-id="351b6-136">Wait for Validation</span></span> | <span data-ttu-id="351b6-137">なし</span><span class="sxs-lookup"><span data-stu-id="351b6-137">No</span></span> | <span data-ttu-id="351b6-138">検証が必要な資産タイプの場合、このチェック ボックスを使用して、アセットの検証が成功または失敗するまで待機するようにタスクに指示します。</span><span class="sxs-lookup"><span data-stu-id="351b6-138">For asset types that require validation, use this check box to instruct the task to wait until validation of the asset has either succeeded or failed.</span></span> |
