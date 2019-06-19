---
title: コード移行中の Azure DevOps マッピングのコンフィギュレーション
description: このチュートリアルでは、LCS コードのアップグレード サービスが完了した後、開発ボックスを Azure DevOps プロジェクトにマップする方法を示します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 25951
ms.assetid: 60b8c895-0d5d-4d6b-8e32-e9c2f688ca69
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0713fc3868acff11f2fabf59a492ed6bfa86fd7d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558021"
---
# <a name="configure-the-azure-devops-mapping-during-code-migration"></a><span data-ttu-id="506f6-103">コード移行中の Azure DevOps マッピングのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="506f6-103">Configure the Azure DevOps mapping during code migration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="506f6-104">このチュートリアルでは、LCS コードのアップグレード サービスが完了した後、開発ボックスを Azure DevOps プロジェクトにマップする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="506f6-104">This tutorial shows how to map your development box to the Azure DevOps project after the LCS code upgrade service has completed.</span></span> 

<span data-ttu-id="506f6-105">LCS コードのアップグレード サービスでは、Azure DevOps (旧 Visual Studio Online) にアップグレードされたコードが自動的に確認されます。</span><span class="sxs-lookup"><span data-stu-id="506f6-105">The LCS code upgrade service automatically checks your upgraded code into Azure DevOps (formerly called Visual Studio Online).</span></span> <span data-ttu-id="506f6-106">次に、 開発ボックスを、Azure DevOps プロジェクト内のアップグレード フォルダー/ブランチにマップする必要があります (アップグレード フォルダー/ブランチの名前は移行するバージョンによって異なります)。</span><span class="sxs-lookup"><span data-stu-id="506f6-106">You will then need to map your development box to the upgrade folder/branch in your Azure DevOps project (The name of the upgrade folder/branch depends on the version you migrated to).</span></span> <span data-ttu-id="506f6-107">アップグレードされたフォルダー内には、3 つのフォルダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="506f6-107">Within your upgraded folder, you will find three folders:</span></span>

-   <span data-ttu-id="506f6-108">輸出</span><span class="sxs-lookup"><span data-stu-id="506f6-108">Export</span></span>
-   <span data-ttu-id="506f6-109">メタデータ</span><span class="sxs-lookup"><span data-stu-id="506f6-109">Metadata</span></span>
-   <span data-ttu-id="506f6-110">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="506f6-110">Projects</span></span>

## <a name="key-concepts"></a><span data-ttu-id="506f6-111">重要な概念</span><span class="sxs-lookup"><span data-stu-id="506f6-111">Key concepts</span></span>
-   <span data-ttu-id="506f6-112">**Export** は、Microsoft Dynamics AX 2012 からのエクスポート後、XML ファイルを含んでいるプロジェクトです。</span><span class="sxs-lookup"><span data-stu-id="506f6-112">**Export** is the project that contains the XML files after exporting from Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="506f6-113">これはアップグレード前の XML 形式のメタデータです。</span><span class="sxs-lookup"><span data-stu-id="506f6-113">This is your metadata in XML format before it is upgraded.</span></span> <span data-ttu-id="506f6-114">これは、Dynamics AX 2012 からアップグレードする場合にのみ関係があります。</span><span class="sxs-lookup"><span data-stu-id="506f6-114">This is only relevant if you are upgrading from Dynamics AX 2012.</span></span>
-   <span data-ttu-id="506f6-115">**Metadata** は、Microsoft Dynamics 365 for Finance and Operations の最新バージョン上のアップグレード後のコード (メタデータ XML ファイル) です。</span><span class="sxs-lookup"><span data-stu-id="506f6-115">**Metadata** is your upgraded code (metadata XML file) on the latest version of Microsoft Dynamics 365 for Finance and Operations.</span></span>
-   <span data-ttu-id="506f6-116">**プロジェクト**は、アップグレード中に使用できる 2 つのソリューションです。</span><span class="sxs-lookup"><span data-stu-id="506f6-116">**Projects** are two solutions that you can use during upgrade.</span></span> <span data-ttu-id="506f6-117">1 つのソリューションである CodeMergeSolution は、競合し、また解決する必要がある要素を伴うプロジェクトを含むソリューションです。</span><span class="sxs-lookup"><span data-stu-id="506f6-117">One solution, CodeMergeSolution, is the solution that contains projects with the elements that have conflicts and need to be resolved.</span></span> <span data-ttu-id="506f6-118">もう 1 つのソリューション、UpgradedSolution には、アップグレードされたモデルごとに 1 つのプロジェクトのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="506f6-118">The other solution, UpgradedSolution, contains a collection of projects, one for each upgraded model.</span></span> <span data-ttu-id="506f6-119">たとえば、Azure DevOps で、以下の構造のようなものを表示します。</span><span class="sxs-lookup"><span data-stu-id="506f6-119">For example, in Azure DevOps, you should see something like the following structure.</span></span> <span data-ttu-id="506f6-120">[![プロジェクト](./media/filestructure_configuringyourvsosolution.png)](./media/filestructure_configuringyourvsosolution.png)</span><span class="sxs-lookup"><span data-stu-id="506f6-120">[![Project](./media/filestructure_configuringyourvsosolution.png)](./media/filestructure_configuringyourvsosolution.png)</span></span>

## <a name="map-azure-devops-to-your-development-box"></a><span data-ttu-id="506f6-121">Azure DevOps の開発ボックスへのマップ</span><span class="sxs-lookup"><span data-stu-id="506f6-121">Map Azure DevOps to your development box</span></span>
1.  <span data-ttu-id="506f6-122">Visual Studio で、**チーム エクスプローラー &gt; チーム プロジェクトの選択 &gt; サーバー &gt; 追加**と進んでアカウントに接続します。</span><span class="sxs-lookup"><span data-stu-id="506f6-122">In Visual Studio, connect to your account by going to **Team explorer &gt; Select Team Projects &gt; Servers &gt; Add.**</span></span>
2.  <span data-ttu-id="506f6-123">チーム プロジェクトに URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="506f6-123">Enter the URL to your team project.</span></span> <span data-ttu-id="506f6-124">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="506f6-124">Click **Close**.</span></span>
3.  <span data-ttu-id="506f6-125">Azure DevOps アカウントが表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="506f6-125">Make sure the Azure DevOps account shows up.</span></span> <span data-ttu-id="506f6-126">右側で、作業するプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="506f6-126">On the right, choose the project that you want to work on.</span></span> <span data-ttu-id="506f6-127">**接続** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="506f6-127">Click **Connect**.</span></span>
4.  <span data-ttu-id="506f6-128">ここで、ワークスペースを Azure DevOps フォルダーにマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="506f6-128">Now you need to map your workspace to the Azure DevOps folders.</span></span> <span data-ttu-id="506f6-129">**ソース コード エクスプ ローラ**に移動し、このマッピングを行います。</span><span class="sxs-lookup"><span data-stu-id="506f6-129">Go to the **Source Code Explorer** and do this mapping:</span></span>
    1.  <span data-ttu-id="506f6-130">プロジェクト &gt; C:\\Users\\&lt;username&gt;\\Documents\\Visual Studio 2015\\Projects</span><span class="sxs-lookup"><span data-stu-id="506f6-130">Projects &gt; C:\\Users\\&lt;username&gt;\\Documents\\Visual Studio 2015\\Projects</span></span>
    2.  <span data-ttu-id="506f6-131">メタデータ &gt; C:\\AOSService\\PackagesLocalDirectory</span><span class="sxs-lookup"><span data-stu-id="506f6-131">Metadata &gt; C:\\AOSService\\PackagesLocalDirectory</span></span>
        -   <span data-ttu-id="506f6-132">クラウド VMs で、このフォルダーは I:\\または J:\\ ドライブに保管</span><span class="sxs-lookup"><span data-stu-id="506f6-132">On cloud VMs, this folder is located on the I:\\ or J:\\ drive</span></span>
        -   <span data-ttu-id="506f6-133">以前のバージョンで、このフォルダーは C:\\パッケージ</span><span class="sxs-lookup"><span data-stu-id="506f6-133">On earlier versions, this folder is C:\\packages</span></span>
        -   <span data-ttu-id="506f6-134">**重要**:</span><span class="sxs-lookup"><span data-stu-id="506f6-134">**Important**:</span></span>
            -   <span data-ttu-id="506f6-135">Dynamics AX 2012 R3 またはそれ以前のバージョンから移行する場合は、**メイン**分岐の下のメタデータ フォルダにマッピングします。</span><span class="sxs-lookup"><span data-stu-id="506f6-135">If you are migrating from Dynamics AX 2012 R3 or earlier, you will be mapping to the metadata folder under the **Main** branch.</span></span>
            -   <span data-ttu-id="506f6-136">新しい Dynamics AX (Finance and Operations) の 2 つのバージョン間で移行する場合は、いずれかの**リリース**の分岐の下のメタデータ フォルダーにマッピングします。</span><span class="sxs-lookup"><span data-stu-id="506f6-136">If you are migrating between 2 versions of the new Dynamics AX (Finance and Operations), you will be mapping to the metadata folder under one of the **Releases** branch.</span></span>

<span data-ttu-id="506f6-137">[![vstsmapping](./media/vstsmapping.png)](./media/vstsmapping.png) これらのフォルダーをマップしたら、ローカル ボックスにコードを同期させることができます。</span><span class="sxs-lookup"><span data-stu-id="506f6-137">[![vstsmapping](./media/vstsmapping.png)](./media/vstsmapping.png) Once you have mapped these folders, you can synchronize the code to your local box.</span></span> <span data-ttu-id="506f6-138">メタデータを右クリックし、**最新バージョンを取得** を選択します。</span><span class="sxs-lookup"><span data-stu-id="506f6-138">Right-click on Metadata and select **Get latest**.</span></span> <span data-ttu-id="506f6-139">同様に、プロジェクト フォルダーを同期します。</span><span class="sxs-lookup"><span data-stu-id="506f6-139">Similarly synchronize the Projects folder.</span></span> <span data-ttu-id="506f6-140">メタデータ フォルダーを同期した後、**Finance and Operations** &gt; **モデル管理** &gt; **モデルの更新** から Visual Studio でモデルを更新します。</span><span class="sxs-lookup"><span data-stu-id="506f6-140">After synchronizing the metadata folder, refresh your models in Visual Studio from **Finance and Operations** &gt; **Model Management** &gt; **Refresh Models**.</span></span> <span data-ttu-id="506f6-141">[![VSRefreshModels](./media/vsrefreshmodels.png)](./media/vsrefreshmodels.png) これで、プロジェクトを立ち上げ、競合を解決し、コードの移行を構築、テスト、および実行する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="506f6-141">[![VSRefreshModels](./media/vsrefreshmodels.png)](./media/vsrefreshmodels.png) You are now ready to open your projects, resolve conflicts, build, test and complete your code migration.</span></span>



