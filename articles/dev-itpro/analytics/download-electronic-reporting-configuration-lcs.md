---
title: "Lifecycle Services の電子申告コンフィギュレーションのダウンロード"
description: "このトピックは、Microsoft Dynamics Lifecycle Services (LCS) から電子申告 (ER) のコンフィギュレーションをダウンロードする方法を説明します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a4411b25285128c849a715fdc7a2f5fe51580a3b
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="0cc26-103">Lifecycle Services の電子申告コンフィギュレーションのダウンロード</span><span class="sxs-lookup"><span data-stu-id="0cc26-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0cc26-104">このトピックは、Microsoft Dynamics Lifecycle Services (LCS) から電子申告 (ER) のコンフィギュレーションをダウンロードする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="0cc26-105">このチュートリアル ガイドは Microsoft Dynamics Lifecycle Services (LCS) から Electronic reporting (ER) コンフィギュレーションの最新バージョンをダウンロードするプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1.  <span data-ttu-id="0cc26-106">次のロールの 1 つを使用して Dynamics 365 for Finance and Operations にサインインします。</span><span class="sxs-lookup"><span data-stu-id="0cc26-106">Sign in to Finance and Operations by using one of the following roles:</span></span>
    -   <span data-ttu-id="0cc26-107">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="0cc26-107">Electronic reporting developer</span></span>
    -   <span data-ttu-id="0cc26-108">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="0cc26-108">Electronic reporting functional consultant</span></span>
    -   <span data-ttu-id="0cc26-109">システム管理者</span><span class="sxs-lookup"><span data-stu-id="0cc26-109">System administrator</span></span>

2.  <span data-ttu-id="0cc26-110">[**組織管理**] &gt; [**電子申告**] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3.  <span data-ttu-id="0cc26-111">[**コンフィギュレーション プロバイダー**] セクションで、[**Microsoft**] タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4.  <span data-ttu-id="0cc26-112">[**Microsoft**] タイルで [**リポジトリ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0cc26-112">On the **Microsoft** tile, click **Repositories**.</span></span> <span data-ttu-id="0cc26-113">[![MS オープン MS リポジトリ リスト用 LCS からの ER 更新](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="0cc26-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>
5.  <span data-ttu-id="0cc26-114">**コンフィギュレーション リポジトリ** ページのグリッドで、**LCS** タイプの既存のリポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="0cc26-115">このリポジトリがグリッドに表示されない場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0cc26-115">If this repository doesn't appear in the grid, follow these steps:</span></span>
    1.  <span data-ttu-id="0cc26-116">[**追加**] をクリックして新しいリポジトリを追加します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-116">Click **Add** to add a new repository.</span></span>
    2.  <span data-ttu-id="0cc26-117">リポジトリ タイプとして、[**LCS**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-117">Select **LCS** as the repository type.</span></span>
    3.  <span data-ttu-id="0cc26-118">[**リポジトリの作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0cc26-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="0cc26-119">メッセージが表示されたら、承認の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="0cc26-119">If prompted, follow the authorization instructions.</span></span>
    5.  <span data-ttu-id="0cc26-120">リポジトリの名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-120">Enter a name and description for the repository.</span></span>
    6.  <span data-ttu-id="0cc26-121">[**OK**] をクリックして、新しいリポジトリ エントリを確認します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-121">Click **OK** to confirm the new repository entry.</span></span>
    7.  <span data-ttu-id="0cc26-122">グリッドで、[**LCS**] タイプの新しいリポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-122">In the grid, select the new repository of the **LCS** type.</span></span>

6.  <span data-ttu-id="0cc26-123">[**開く**] をクリックして、選択したリポジトリの ER コンフィギュレーションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span> <span data-ttu-id="0cc26-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="0cc26-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>
7.  <span data-ttu-id="0cc26-125">左ウィンドウのコンフィギュレーション ツリーで必要な ER コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8.  <span data-ttu-id="0cc26-126">[**バージョン**] クイック タブで、選択した ER コンフィギュレーションの必要なバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="0cc26-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9.  <span data-ttu-id="0cc26-127">[**インポート**] をクリックして、LCS から現在の Finance and Operations インスタンスに選択したバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0cc26-127">Click **Import** to download the selected version from LCS to the current Finance and Operations instance.</span></span> <span data-ttu-id="0cc26-128">**注:** [**インポート**] ボタンは、現在の Finance and Operations インスタンスにある ER コンフィギュレーション バージョンでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="0cc26-128">**Note:** The **Import** button is unavailable for ER configuration versions that are already present in the current Finance and Operations instance.</span></span> <span data-ttu-id="0cc26-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="0cc26-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

<span data-ttu-id="0cc26-130">**注:** ER の設定に応じて、コンフィギュレーションはインポートされた後に検証されます。</span><span class="sxs-lookup"><span data-stu-id="0cc26-130">**Note:** Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="0cc26-131">不整合の問題が検出されると、通知を受け取る場合があります。</span><span class="sxs-lookup"><span data-stu-id="0cc26-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="0cc26-132">インポートしたコンフィギュレーションのバージョンを使用する前に、それらの問題を解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0cc26-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="0cc26-133">詳細については、このトピックの関連記事の一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0cc26-133">For more information, see the list of related articles for this topic.</span></span>

<a name="see-also"></a><span data-ttu-id="0cc26-134">参照</span><span class="sxs-lookup"><span data-stu-id="0cc26-134">See also</span></span>
--------

[<span data-ttu-id="0cc26-135">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="0cc26-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)




