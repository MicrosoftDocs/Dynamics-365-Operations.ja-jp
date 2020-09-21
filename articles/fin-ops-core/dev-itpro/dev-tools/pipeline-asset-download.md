---
title: Azure パイプラインを使用した資産のダウンロード
description: このトピックでは、Azure パイプラインを使用して、LCS アセット ライブラリから資産をダウンロードする方法について説明します。
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
ms.openlocfilehash: 2d974d546188ef26e736ed28b711884b7135cbc2
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2020
ms.locfileid: "3765090"
---
# <a name="download-assets-by-using-azure-pipelines"></a><span data-ttu-id="65ac4-103">Azure パイプラインを使用した資産のダウンロード</span><span class="sxs-lookup"><span data-stu-id="65ac4-103">Download assets by using Azure Pipelines</span></span>

<span data-ttu-id="65ac4-104">Azure DevOps の **Lifecycle Services (LCS) 資産のダウンロード** タスクを使用して、**Lifecycle Services アセット ライブラリ** から資産をダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="65ac4-104">You can automate downloading assets from the **Lifecycle Services Asset Library** by using the **Deploy Lifecycle Services (LCS) Asset Download** task in Azure DevOps.</span></span>

<span data-ttu-id="65ac4-105">このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を持っていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="65ac4-105">This topic assumes that you have a working knowledge of [Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started).</span></span>

> [!NOTE]
> <span data-ttu-id="65ac4-106">これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="65ac4-106">Before you can add these steps to a pipeline, the [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) extension for Azure DevOps must be enabled and installed in the Azure DevOps account.</span></span> <span data-ttu-id="65ac4-107">組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension?view=azure-devops&tabs=browser)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65ac4-107">For more information about how to install an extension for an organization, see [Install extensions](https://docs.microsoft.com/azure/devops/marketplace/install-extension?view=azure-devops&tabs=browser).</span></span>

## <a name="add-the-task-to-a-pipeline"></a><span data-ttu-id="65ac4-108">パイプラインへのタスクの追加</span><span class="sxs-lookup"><span data-stu-id="65ac4-108">Add the task to a pipeline</span></span>

<span data-ttu-id="65ac4-109">YML または Classic パイプラインのビルドにタスクを追加するには、**Dynamics Lifecycle Services (LCS) アセット ダウンロード** のタスク リストを検索します。</span><span class="sxs-lookup"><span data-stu-id="65ac4-109">To add the task to the build of your YML or Classic pipeline, search the task list for **Dynamics Lifecycle Services (LCS) Asset Download**.</span></span>

<span data-ttu-id="65ac4-110">次のテーブルに、このタスクで使用可能なオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="65ac4-110">The following table describes the options that are available for this task.</span></span>

| <span data-ttu-id="65ac4-111">入力名</span><span class="sxs-lookup"><span data-stu-id="65ac4-111">Input name</span></span> | <span data-ttu-id="65ac4-112">必須</span><span class="sxs-lookup"><span data-stu-id="65ac4-112">Mandatory</span></span> | <span data-ttu-id="65ac4-113">説明</span><span class="sxs-lookup"><span data-stu-id="65ac4-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="65ac4-114">LCS 接続</span><span class="sxs-lookup"><span data-stu-id="65ac4-114">LCS Connection</span></span> | <span data-ttu-id="65ac4-115">有</span><span class="sxs-lookup"><span data-stu-id="65ac4-115">Yes</span></span> | <span data-ttu-id="65ac4-116">Dynamics Lifecycle Services (LCS) へのサービス接続を選択または作成します。</span><span class="sxs-lookup"><span data-stu-id="65ac4-116">Select or create a service connection to Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="65ac4-117">詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65ac4-117">For more information, see [Creating an LCS connection in Azure Pipelines](pipeline-lcs-connection.md).</span></span> |
| <span data-ttu-id="65ac4-118">LCS プロジェクト ID</span><span class="sxs-lookup"><span data-stu-id="65ac4-118">LCS Project ID</span></span> | <span data-ttu-id="65ac4-119">有</span><span class="sxs-lookup"><span data-stu-id="65ac4-119">Yes</span></span> | <span data-ttu-id="65ac4-120">配置する両方の試算と、ターゲット環境を含む、LCS のプロジェクトを識別するプロジェクト ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="65ac4-120">Enter the project ID identifying the project in LCS that contains both the asset to be deployed, and the target environment.</span></span> <span data-ttu-id="65ac4-121">プロジェクト ID は、プロジェクトのダッシュボードの URL の末尾に記載できます。</span><span class="sxs-lookup"><span data-stu-id="65ac4-121">You can find the project ID at the end of the URL of your project's dashboard.</span></span> |
| <span data-ttu-id="65ac4-122">ダウンロード先のパス</span><span class="sxs-lookup"><span data-stu-id="65ac4-122">Path to download to</span></span> | <span data-ttu-id="65ac4-123">有</span><span class="sxs-lookup"><span data-stu-id="65ac4-123">Yes</span></span> | <span data-ttu-id="65ac4-124">資産のダウンロード先のパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="65ac4-124">Enter the path to download the asset into.</span></span> |
| <span data-ttu-id="65ac4-125">検索パターン</span><span class="sxs-lookup"><span data-stu-id="65ac4-125">Search Pattern</span></span> | <span data-ttu-id="65ac4-126">有</span><span class="sxs-lookup"><span data-stu-id="65ac4-126">Yes</span></span> | <span data-ttu-id="65ac4-127">**アセット ライブラリ** で資産を検索する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ac4-127">Select how to find the assets in the **Asset Library**.</span></span> |

<span data-ttu-id="65ac4-128">選択した **検索パターン** のタイプに応じて、次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="65ac4-128">Depending on the type of **Search Pattern** that you selected, the following options are available.</span></span>

* <span data-ttu-id="65ac4-129">**資産 ID (GUID)** を選択する場合は、**LCS ファイル資産 ID**  フィールドに GUID を入力するか、資産 ID の GUID またはセミコロンで区切られた一覧を指定します。</span><span class="sxs-lookup"><span data-stu-id="65ac4-129">When selecting **Asset ID (guid)**, provide a GUID or a semi-colon separated list of GUIDs of asset IDs in the **LCS File Asset Id(s)** field.</span></span>
* <span data-ttu-id="65ac4-130">**名前** を選択する場合は、**LCS ファイル資産タイプ** ドロップダウン リストから資産タイプを選択し、**LCS ファイル資産名** フィールドで検索する名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="65ac4-130">When selecting **Name**, select the asset type from the **LCS File Asset Type** dropdown, and a name to search for in the **LCS File Asset Name** field.</span></span> <span data-ttu-id="65ac4-131">**MyPackage\*** など、アスタリスク (\*) 記号を使用して名前にワイルドカードを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="65ac4-131">You can use a wildcard in the name using the asterisk (\*) symbol, for example **MyPackage\***.</span></span>

<span data-ttu-id="65ac4-132">ダウンロードが正常に行われた後、ファイルパスの一覧を出力変数と共に取得できます。</span><span class="sxs-lookup"><span data-stu-id="65ac4-132">After a successful download, a list of the file paths can be captured with an output variable.</span></span> <span data-ttu-id="65ac4-133">複数のファイルが存在する場合は、セミコロンで区切られたファイルパスの一覧が出力変数に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="65ac4-133">If there are multiple files, a semi-colon separated list of file paths is assigned to the output variable.</span></span> <span data-ttu-id="65ac4-134">**Azure DevOps** の出力変数の詳細については、[タスクからの出力変数を使用する](https://docs.microsoft.com/azure/devops/pipelines/process/variables?view=azure-devops&tabs=yaml%2Cbatch#use-output-variables-from-tasks) を参照してください</span><span class="sxs-lookup"><span data-stu-id="65ac4-134">For more information about output variables in **Azure DevOps**, see [Use output variables from tasks](https://docs.microsoft.com/azure/devops/pipelines/process/variables?view=azure-devops&tabs=yaml%2Cbatch#use-output-variables-from-tasks)</span></span>
