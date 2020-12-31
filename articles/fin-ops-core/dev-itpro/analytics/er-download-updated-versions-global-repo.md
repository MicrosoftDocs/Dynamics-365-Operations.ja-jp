---
title: ER コンフィギュレーションの更新バージョンのインポート
description: このトピックでは、コンフィギュレーション サービスのグローバル リポジトリから電子申告 (ER) コンフィギュレーションの更新済バージョンをインポートする方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 897663998c6c95ff6d7172de2abc4d4dd6ec5f12
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679513"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="461c1-103">ER コンフィギュレーションの更新バージョンのインポート</span><span class="sxs-lookup"><span data-stu-id="461c1-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="461c1-104">電子レポート (ER) [リポジトリ](general-electronic-reporting.md#Repository) は、[ER コンフィギュレーション](general-electronic-reporting.md#Configuration) を共有するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="461c1-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="461c1-105">異なるリポジトリから Microsoft Dynamics 365 Finance のインスタンスに ER コンフィギュレーションを[インポート](download-electronic-reporting-configuration-lcs.md) できます。</span><span class="sxs-lookup"><span data-stu-id="461c1-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="461c1-106">ER コンフィギュレーションをインポートする場合、[コンフィギュレーション プロバイダー](general-electronic-reporting.md#Provider) は、新しい[バージョン](general-electronic-reporting.md#component-versioning) のリポジトリを公開して共有できるようになります。</span><span class="sxs-lookup"><span data-stu-id="461c1-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="461c1-107">このトピックでは、コンフィギュレーション サービスのグローバル リポジトリから ER コンフィギュレーションの更新済バージョンをインポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="461c1-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="461c1-108">詳細については、[Microsoft Dynamics 365 for Finance and Operations - Regulatory services、コンフィギュレーション サービス](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="461c1-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="461c1-109">利用可能な更新済バージョンを確認する</span><span class="sxs-lookup"><span data-stu-id="461c1-109">Review the available updated versions</span></span>

1. <span data-ttu-id="461c1-110">次のロールの 1 つを使用して Finance にサイン インします:</span><span class="sxs-lookup"><span data-stu-id="461c1-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="461c1-111">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="461c1-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="461c1-112">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="461c1-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="461c1-113">システム管理者</span><span class="sxs-lookup"><span data-stu-id="461c1-113">System administrator</span></span>

2. <span data-ttu-id="461c1-114">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="461c1-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="461c1-115">**ローカライズ構成** ページの、**関連リンク** セクションで、**コンフィギュレーション バージョンの更新をインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="461c1-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![ローカライズ コンフィギュレーション ページ](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="461c1-117">**電子レポート コンフィギュレーション バージョンの更新をインポート** ダイアログ ボックスの **実行モード** フィールドで、**使用可能な更新のみ表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="461c1-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="461c1-118">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="461c1-118">Then select **OK**.</span></span> 

    ![実行モード フィールドを使用可能な更新のみに設定](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="461c1-120">受信したメッセージを確認します。</span><span class="sxs-lookup"><span data-stu-id="461c1-120">Review the messages that you receive.</span></span> <span data-ttu-id="461c1-121">これらのメッセージは、現在の Finance インスタンス ER コンフィギュレーションに関する次の情報を提供し、それがグローバル リポジトリのコンテンツとどのように比較されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="461c1-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="461c1-122">ER コンフィギュレーションの合計数</span><span class="sxs-lookup"><span data-stu-id="461c1-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="461c1-123">グローバル リポジトリに存在しない ER コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="461c1-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="461c1-124">現在の Finance インスタンスで最新バージョンが既に利用可能な ER コンフィギュレーション (これらの ER コンフィギュレーションの完全な一覧を表示するには、**メッセージの詳細** リンクを選択します。)</span><span class="sxs-lookup"><span data-stu-id="461c1-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![「次のコンフィギュレーションの最新バージョンは既にインポートされています」というメッセージおよびメッセージの詳細](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="461c1-126">最新バージョンがグローバル リポジトリで利用可能で、現在の Finance インスタンスにインポート可能な ER コンフィギュレーション (これらの ER コンフィギュレーションの完全な一覧を表示するには、**メッセージの詳細** リンクを選択します。)</span><span class="sxs-lookup"><span data-stu-id="461c1-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![「使用可能な更新」というメッセージおよびメッセージの詳細](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="461c1-128">利用可能な更新済バージョンをインポートする</span><span class="sxs-lookup"><span data-stu-id="461c1-128">Import available updated versions</span></span>

1. <span data-ttu-id="461c1-129">次のロールの 1 つを使用して Finance にサイン インします:</span><span class="sxs-lookup"><span data-stu-id="461c1-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="461c1-130">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="461c1-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="461c1-131">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="461c1-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="461c1-132">システム管理者</span><span class="sxs-lookup"><span data-stu-id="461c1-132">System administrator</span></span>

2. <span data-ttu-id="461c1-133">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="461c1-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="461c1-134">**ローカライズ構成** ページの、**関連リンク** セクションで、**コンフィギュレーション バージョンの更新をインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="461c1-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="461c1-135">**電子レポート コンフィギュレーションのバージョンをインポート** ダイアログ ボックスの **実行モード** フィールドで、**最新の更新プログラムをインポート** を選び、ER コンフィギュレーションの最新バージョンをグローバル リポジトリから現在の Finance インスタンスにインポートします。</span><span class="sxs-lookup"><span data-stu-id="461c1-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="461c1-136">インポートに対してバッチ ジョブをスケジュールするには、**バックグラウンドで実行** クイックタブで、**バッチ処理** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="461c1-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="461c1-137">定期的にインポートを繰り返したい場合は、必要な繰り返しをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="461c1-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![最新の更新プログラムをインポートするように設定された実行モード フィールド](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="461c1-139">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="461c1-139">Select **OK**.</span></span>
7. <span data-ttu-id="461c1-140">インポートされたコンフィギュレーション バージョンを調べるには、次の手順のいずれかを実行します:</span><span class="sxs-lookup"><span data-stu-id="461c1-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="461c1-141">バッチ ジョブを使用する代わりにインポートを対話的に実行する場合は、受信したメッセージを確認します。</span><span class="sxs-lookup"><span data-stu-id="461c1-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![対話型のインポート実行中に受信したメッセージ](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="461c1-143">バッチ モードでインポートを実行する場合は、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="461c1-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="461c1-144">**共通** \> **照会** \> **バッチ ジョブ** \> **私のバッチ ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="461c1-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="461c1-145">**電子レポート コンフィギュレーション バージョンのインポート** ジョブを検索および選択し、アクション ウィンドウの **バッチ ジョブ** タブで、**バッチ ジョブの履歴経歴** を選びジョブの履歴を表示します。</span><span class="sxs-lookup"><span data-stu-id="461c1-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="461c1-146">**バッチ ジョブの履歴** ページで **ログ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="461c1-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="461c1-147">次に、受信したメッセージで、**メッセージの詳細** リンクを選びジョブ ログを表示します。</span><span class="sxs-lookup"><span data-stu-id="461c1-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![ジョブ ログ](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="461c1-149">定期的なバッチ ジョブのスケジュールを設定して、更新されたバージョンの ER コンフィギュレーションを運用環境にインポートすることをお勧めします。この場合、インポートされたバージョンをすぐに使用できます。</span><span class="sxs-lookup"><span data-stu-id="461c1-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="461c1-150">代わりに、ER コンフィギュレーションのバージョンをサンドボックス環境に配置するには、この方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="461c1-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="461c1-151">これにより、運用環境に配置する前に、サンドボックス環境で評価することができます。</span><span class="sxs-lookup"><span data-stu-id="461c1-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="461c1-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="461c1-152">Additional resources</span></span>

- [<span data-ttu-id="461c1-153">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="461c1-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="461c1-154">ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする</span><span class="sxs-lookup"><span data-stu-id="461c1-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
