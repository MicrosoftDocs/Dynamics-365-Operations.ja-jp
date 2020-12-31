---
title: Lifecycle Services の電子申告コンフィギュレーションのダウンロード
description: このトピックは、Microsoft Dynamics Lifecycle Services (LCS) から電子申告 (ER) のコンフィギュレーションをダウンロードする方法を説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 719b277fb828ea2085ea80bc4a36c2af3412f66b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683308"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="2719a-103">Lifecycle Services から電子申告コンフィギュレーションをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="2719a-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2719a-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) の [共有アセット ライブラリ](../lifecycle-services/asset-library.md) から最新バージョンの [電子申告 (ER) コンフィギュレーション](general-electronic-reporting.md#Configuration) をダウンロードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2719a-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="2719a-105">次のロールの 1 つを使用してアプリケーションにサインインします。</span><span class="sxs-lookup"><span data-stu-id="2719a-105">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="2719a-106">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="2719a-106">Electronic reporting developer</span></span>
    - <span data-ttu-id="2719a-107">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="2719a-107">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="2719a-108">システム管理者</span><span class="sxs-lookup"><span data-stu-id="2719a-108">System administrator</span></span>

2. <span data-ttu-id="2719a-109">**組織管理** &gt; **ワークスペース** &gt; **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2719a-109">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="2719a-110">**コンフィギュレーション プロバイダー** セクションで、**Microsoft** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="2719a-110">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="2719a-111">**Microsoft** タイルで **リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2719a-111">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="2719a-112">[ローカライズ コンフィギュレーション ページ の ![Microsoft タイル](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="2719a-112">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="2719a-113">**コンフィギュレーション リポジトリ** ページのグリッドで、**LCS** タイプの既存のリポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="2719a-113">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="2719a-114">このリポジトリがグリッドに表示されない場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2719a-114">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="2719a-115">**追加** を選択して、リポジトリを追加します。</span><span class="sxs-lookup"><span data-stu-id="2719a-115">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="2719a-116">リポジトリ タイプとして、**LCS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2719a-116">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="2719a-117">**レポジトリを作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2719a-117">Select **Create repository**.</span></span>
    4. <span data-ttu-id="2719a-118">認証についてのメッセージが表示された場合は、画面の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="2719a-118">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="2719a-119">リポジトリの名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2719a-119">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="2719a-120">**OK** を選択して、新しいリポジトリ エントリを確認します。</span><span class="sxs-lookup"><span data-stu-id="2719a-120">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="2719a-121">グリッドで、**LCS** タイプの新しいリポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="2719a-121">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="2719a-122">**開く** を選択して、選択したリポジトリの ER コンフィギュレーションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="2719a-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="2719a-123">[![コンフィギュレーション レポジトリ ページ](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="2719a-123">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="2719a-124">LCS の共有アセット ライブラリからコンフィギュレーションをダウンロードするのに、LCS リポジトリへのアクセスに問題がある場合は、代わりに [グローバル リポジトリ](er-download-configurations-global-repo.md) からコンフィギュレーションをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="2719a-124">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="2719a-125">左側ペインのコンフィギュレーション ツリーで必要な ER コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2719a-125">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="2719a-126">**バージョン** クイック タブで、選択した ER コンフィギュレーションの必要なバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="2719a-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="2719a-127">**インポート** を選択して、LCS から現在のインスタンスに選択したバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2719a-127">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2719a-128">**インポート** ボタンは、現在のインスタンスにある ER コンフィギュレーション バージョンでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="2719a-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="2719a-129">[![レポジトリ ページのコンフィギュレーション](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="2719a-129">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="2719a-130">ER の設定に応じて、コンフィギュレーションはインポートされた後に検証されます。</span><span class="sxs-lookup"><span data-stu-id="2719a-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="2719a-131">不整合の問題が検出されると、通知を受け取る場合があります。</span><span class="sxs-lookup"><span data-stu-id="2719a-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="2719a-132">インポートしたコンフィギュレーションのバージョンを使用する前に、それらの問題を解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2719a-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="2719a-133">詳細については、このトピックの関連トピックの一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2719a-133">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2719a-134">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2719a-134">Additional resources</span></span>

[<span data-ttu-id="2719a-135">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="2719a-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="2719a-136">ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする</span><span class="sxs-lookup"><span data-stu-id="2719a-136">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
