---
title: Azure Pipelines を使用した資産のダウンロード
description: このトピックでは、Azure Pipelines を使用して、Microsoft Dynamics Lifecycle Services (LCS) で資産をアセット ライブラリからダウンロードする方法について説明します。
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
ms.custom: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 455306c8ffff387386c67a8c03fc02344635550d
ms.sourcegitcommit: 9b23eff7adfe4043419f5b18e8df1d3a91b28c27
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2020
ms.locfileid: "3815648"
---
# <a name="download-assets-by-using-azure-pipelines"></a><span data-ttu-id="16cc3-103">Azure Pipelines を使用した資産のダウンロード</span><span class="sxs-lookup"><span data-stu-id="16cc3-103">Download assets by using Azure Pipelines</span></span>

<span data-ttu-id="16cc3-104">Azure DevOps の **Lifecycle Services (LCS) 資産のダウンロード** タスクを使用して、Microsoft Dynamics Lifecycle Services (LCS) で資産をアセット ライブラリから自動的にダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="16cc3-104">You can automate the download of assets from the Asset library in Microsoft Dynamics Lifecycle Services (LCS) by using the **Deploy Lifecycle Services (LCS) Asset Download** task in Azure DevOps.</span></span>

<span data-ttu-id="16cc3-105">このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を持っていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="16cc3-105">This topic assumes that you have a working knowledge of [Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started).</span></span>

> [!NOTE]
> <span data-ttu-id="16cc3-106">これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="16cc3-106">Before you can add these steps to a pipeline, the [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) extension for Azure DevOps must be enabled and installed in the Azure DevOps account.</span></span> <span data-ttu-id="16cc3-107">組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16cc3-107">For more information about how to install an extension for an organization, see [Install extensions](https://docs.microsoft.com/azure/devops/marketplace/install-extension).</span></span>

## <a name="add-the-task-to-a-pipeline"></a><span data-ttu-id="16cc3-108">パイプラインへのタスクの追加</span><span class="sxs-lookup"><span data-stu-id="16cc3-108">Add the task to a pipeline</span></span>

<span data-ttu-id="16cc3-109">YML または Classic パイプラインのビルドにタスクを追加するには、**Dynamics Lifecycle Services (LCS) アセット ダウンロード** のタスク リストを検索します。</span><span class="sxs-lookup"><span data-stu-id="16cc3-109">To add the task to the build of your YML or Classic pipeline, search the task list for **Dynamics Lifecycle Services (LCS) Asset Download**.</span></span>

<span data-ttu-id="16cc3-110">次のテーブルに、このタスクで使用可能なオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="16cc3-110">The following table describes the options that are available for this task.</span></span>

| <span data-ttu-id="16cc3-111">入力名</span><span class="sxs-lookup"><span data-stu-id="16cc3-111">Input name</span></span> | <span data-ttu-id="16cc3-112">必須</span><span class="sxs-lookup"><span data-stu-id="16cc3-112">Mandatory</span></span> | <span data-ttu-id="16cc3-113">説明</span><span class="sxs-lookup"><span data-stu-id="16cc3-113">Description</span></span> |
|---|---|---|
| <span data-ttu-id="16cc3-114">LCS 接続</span><span class="sxs-lookup"><span data-stu-id="16cc3-114">LCS Connection</span></span> | <span data-ttu-id="16cc3-115">あり</span><span class="sxs-lookup"><span data-stu-id="16cc3-115">Yes</span></span> | <span data-ttu-id="16cc3-116">LCS へのサービス接続を選択または作成します。</span><span class="sxs-lookup"><span data-stu-id="16cc3-116">Select or create a service connection to LCS.</span></span> <span data-ttu-id="16cc3-117">詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16cc3-117">For more information, see [Create an LCS connection in Azure Pipelines](pipeline-lcs-connection.md).</span></span> |
| <span data-ttu-id="16cc3-118">LCS プロジェクト ID</span><span class="sxs-lookup"><span data-stu-id="16cc3-118">LCS Project ID</span></span> | <span data-ttu-id="16cc3-119">あり</span><span class="sxs-lookup"><span data-stu-id="16cc3-119">Yes</span></span> | <span data-ttu-id="16cc3-120">配置する資産およびターゲット環境の両方を含むプロジェクトの ID を LCS に入力します。</span><span class="sxs-lookup"><span data-stu-id="16cc3-120">Enter the ID of the project in LCS that contains both the asset to deploy and the target environment.</span></span> <span data-ttu-id="16cc3-121">プロジェクト ID は、プロジェクトのダッシュボードの URL の末尾に記載できます。</span><span class="sxs-lookup"><span data-stu-id="16cc3-121">You can find the project ID at the end of the URL of your project's dashboard.</span></span> |
| <span data-ttu-id="16cc3-122">ダウンロード先のパス</span><span class="sxs-lookup"><span data-stu-id="16cc3-122">Path to download to</span></span> | <span data-ttu-id="16cc3-123">あり</span><span class="sxs-lookup"><span data-stu-id="16cc3-123">Yes</span></span> | <span data-ttu-id="16cc3-124">資産のダウンロード先のパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="16cc3-124">Enter the path to download the asset to.</span></span> |
| <span data-ttu-id="16cc3-125">検索パターン</span><span class="sxs-lookup"><span data-stu-id="16cc3-125">Search Pattern</span></span> | <span data-ttu-id="16cc3-126">あり</span><span class="sxs-lookup"><span data-stu-id="16cc3-126">Yes</span></span> | <span data-ttu-id="16cc3-127">LCS の資産ライブラリで資産を検索するために使用する検索パターンのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="16cc3-127">Select the type of search pattern that should be used to find the asset in the Asset library in LCS.</span></span> <span data-ttu-id="16cc3-128">選択した値に応じて、次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="16cc3-128">Depending on the value that you select, the following options are available:</span></span><ul><li><span data-ttu-id="16cc3-129">**資産 ID (guid)** – この値を選択する場合は、**LCS ファイル資産 ID** フィールドに、資産 ID を入力するか、またはセミコロンで区切られた資産 ID の一覧を入力します。</span><span class="sxs-lookup"><span data-stu-id="16cc3-129">**Asset ID (guid)** – If you select this value, in the **LCS File Asset Id(s)** field, enter the asset ID or a semicolon-separated list of asset IDs.</span></span> <span data-ttu-id="16cc3-130">資産 ID は、グローバル一意識別子 (GUID) です。</span><span class="sxs-lookup"><span data-stu-id="16cc3-130">Asset IDs are globally unique identifiers (GUIDs).</span></span></li><li><span data-ttu-id="16cc3-131">**名前** – この値を選択した場合は、**LCS ファイル資産タイプ** フィールドで資産タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="16cc3-131">**Name** – If you select this value, in the **LCS File Asset Type** field, select the asset type.</span></span> <span data-ttu-id="16cc3-132">次に、**LCS ファイル資産名**フィールドで、検索する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="16cc3-132">Then, in the **LCS File Asset Name** field, specify the name to search for.</span></span> <span data-ttu-id="16cc3-133">アスタリスク (\*) を名前でワイルドカード文字として使用できます。</span><span class="sxs-lookup"><span data-stu-id="16cc3-133">You can use an asterisk (\*) as a wildcard character in the name.</span></span> <span data-ttu-id="16cc3-134">たとえば、**MyPackage\*** と入力します。</span><span class="sxs-lookup"><span data-stu-id="16cc3-134">For example, you might enter **MyPackage\***.</span></span></li></ul> |

<span data-ttu-id="16cc3-135">ダウンロードが正常に行われた後、ファイル パスの一覧を出力変数と共に取得できます。</span><span class="sxs-lookup"><span data-stu-id="16cc3-135">After a successful download, an output variable can be used to capture a list of the file paths.</span></span> <span data-ttu-id="16cc3-136">複数のファイルが存在する場合は、セミコロンで区切られたファイル パスの一覧が出力変数に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="16cc3-136">If there are multiple files, a semicolon-separated list of file paths is assigned to the output variable.</span></span> <span data-ttu-id="16cc3-137">Azure DevOps の出力変数の詳細については、[タスクからの出力変数を使用する を参照してください](https://docs.microsoft.com/azure/devops/pipelines/process/variables#use-output-variables-from-tasks) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16cc3-137">For more information about output variables in Azure DevOps, see [Use output variables from tasks](https://docs.microsoft.com/azure/devops/pipelines/process/variables#use-output-variables-from-tasks).</span></span>
