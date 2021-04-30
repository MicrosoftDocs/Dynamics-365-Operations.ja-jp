---
title: ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする
description: このトピックでは、コンフィギュレーション サービスのグローバル リポジトリから電子申告 (ER) コンフィギュレーションをダウンロードする方法について説明します。
author: NickSelin
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 6f74602cafe3f0848a9e03f17300ca6242fe1545
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893983"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="34f27-103">ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする</span><span class="sxs-lookup"><span data-stu-id="34f27-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34f27-104">このトピックでは、コンフィギュレーション サービスのグローバル リポジトリから [電子申告 (ER) コンフィギュレーション](general-electronic-reporting.md#Configuration) をダウンロードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="34f27-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="34f27-105">詳細については、[Microsoft Dynamics 365 for Finance and Operations - Regulatory services、コンフィギュレーション サービス](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="34f27-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="34f27-106">コンフィギュレーション リポジトリを開く</span><span class="sxs-lookup"><span data-stu-id="34f27-106">Open configurations repository</span></span>

1. <span data-ttu-id="34f27-107">次のロールの 1 つを使用して Dynamics 365 Finance アプリケーションにサインインします:</span><span class="sxs-lookup"><span data-stu-id="34f27-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="34f27-108">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="34f27-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="34f27-109">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="34f27-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="34f27-110">システム管理者</span><span class="sxs-lookup"><span data-stu-id="34f27-110">System administrator</span></span>

2. <span data-ttu-id="34f27-111">**組織管理 > ワークスペース > 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="34f27-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="34f27-112">**コンフィギュレーション プロバイダー** セクションで、**Microsoft** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="34f27-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="34f27-113">**Microsoft** タイルで **リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f27-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![電子申告ワークスペース](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="34f27-115">**コンフィギュレーション リポジトリ** ページのグリッドで、**グローバル** タイプの既存のリポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="34f27-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="34f27-116">このリポジトリがグリッドに表示されない場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="34f27-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="34f27-117">**追加** を選択して新しいリポジトリを追加します。</span><span class="sxs-lookup"><span data-stu-id="34f27-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="34f27-118">リポジトリ タイプとして **グローバル** を選択し、**リポジトリの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f27-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="34f27-119">メッセージが表示されたら、承認の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="34f27-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="34f27-120">リポジトリの名前と説明を入力し、**OK** を選択して、新しいリポジトリのエントリを確認します。</span><span class="sxs-lookup"><span data-stu-id="34f27-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="34f27-121">グリッドで、**グローバル** タイプの新しいリポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="34f27-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="34f27-122">**開く** を選択して、選択したリポジトリの ER コンフィギュレーションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="34f27-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![コンフィギュレーション レポジトリ ページ](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="34f27-124">単一のコンフィギュレーションをインポートする</span><span class="sxs-lookup"><span data-stu-id="34f27-124">Import a single configuration</span></span>

1. <span data-ttu-id="34f27-125">**コンフィギュレーション リポジトリ** ページの コンフィギュレーション ツリーで、必要な ER コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="34f27-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="34f27-126">**バージョン** クイック タブで、選択した ER コンフィギュレーションの必要なバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="34f27-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="34f27-127">**インポート** を選択して、グローバル リポジトリから現在の Finance インスタンスに選択したバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="34f27-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="34f27-128">**インポート** ボタンは、現在の Finance インスタンスにある ER コンフィギュレーション バージョンでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="34f27-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![レポジトリ ページのコンフィギュレーション](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="34f27-130">フィルター処理されたコンフィギュレーションをインポートする</span><span class="sxs-lookup"><span data-stu-id="34f27-130">Import filtered configurations</span></span>

1. <span data-ttu-id="34f27-131">**コンフィギュレーション リポジトリ** ページの コンフィギュレーション ツリーで、**フィルター** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="34f27-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="34f27-132">**タグ** グリッドで、必要なタグを追加します。</span><span class="sxs-lookup"><span data-stu-id="34f27-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="34f27-133">**国/地域の適用性** フィールドで、適切な国/地域コードを選択し、**フィルターの適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f27-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="34f27-134">**コンフィギュレーション** クイック タブには、指定した選択条件を満たすコンフィギュレーションがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="34f27-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="34f27-135">**コンフィギュレーション** クイック タブで、**インポート** を選択し、フィルタ処理されたコンフィギュレーションをグローバル リポジトリから現在のインスタンスにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="34f27-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="34f27-136">**コンフィギュレーション** クイック タブで、**フィルタのリセット** を選択し、指定された選択条件をクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="34f27-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![レポジトリ ページのコンフィギュレーション](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="34f27-138">ER の設定に応じて、コンフィギュレーションはインポートされた後に検証されます。</span><span class="sxs-lookup"><span data-stu-id="34f27-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="34f27-139">不整合の問題が検出されると、通知を受け取る場合があります。</span><span class="sxs-lookup"><span data-stu-id="34f27-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="34f27-140">インポートしたコンフィギュレーションのバージョンを使用する前に、問題を解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34f27-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="34f27-141">詳細については、このトピックの関連リソースの一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="34f27-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="34f27-142">ER コンフィギュレーションは、他のコンフィギュレーションに依存するようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="34f27-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="34f27-143">したがって、選択したコンフィギュレーションに加えて、他のコンフィギュレーションが自動的にインポートされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="34f27-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="34f27-144">コンフィギュレーションの依存関係の詳細については、[他のコンポーネントに対する ER コンフィギュレーションの依存関係を定義する](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="34f27-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34f27-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="34f27-145">Additional resources</span></span>

[<span data-ttu-id="34f27-146">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="34f27-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]