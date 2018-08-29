---
title: "エンティティ ストア モデルの更新プログラムをスケジュール"
description: "このトピックでは、システム管理者が組み込まれているツールを使用して、トランザクションのデータベースで使用可能な最新の更新を使用してデータ モデルが更新される頻度を管理する方法について説明します。"
author: tjvass
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-31
ms.dyn365.ops.version: Platform update 16
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8c47ad7789d96abec106cd33b4816a9b6ca5eaff
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="schedule-updates-of-entity-store-models"></a><span data-ttu-id="bc2fb-103">エンティティ ストア モデルの更新プログラムをスケジュール</span><span class="sxs-lookup"><span data-stu-id="bc2fb-103">Schedule updates of entity store models</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/pre-release.md)] 

## <a name="refreshing-models"></a><span data-ttu-id="bc2fb-104">モデルの更新</span><span class="sxs-lookup"><span data-stu-id="bc2fb-104">Refreshing models</span></span>
<span data-ttu-id="bc2fb-105">システム管理者は組み込まれているツールを使用して、トランザクションのデータベースで使用可能な最新の更新を使用してデータ モデルが更新される頻度を管理します。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-105">System administrators use built-in tools to manage the frequency at which data models are refreshed with the latest updates available in the transactional database.</span></span> <span data-ttu-id="bc2fb-106">Microsoft Dynamics 365 for Finance and Operations は、モデルを最新の状態に維持するために使用される完全な同期および差分同期の両方の戦略をサポートします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-106">Microsoft Dynamics 365 for Finance and Operations supports both a full and incremental synchronization strategy that can be used to keep models up to date.</span></span>

- <span data-ttu-id="bc2fb-107">**完全同期** - エンティティ ストア内の既存データを削除し、バックグラウンド プロセス中にモデル全体を実現します。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-107">**Full synchronization** - Existing data in the entity store is deleted and the entire model is materialized during the background process.</span></span>

- <span data-ttu-id="bc2fb-108">**差分更新** - オブジェクトの削除を含む、トランザクション データベースの更新は、エンティティ ストア モデルと同期されます。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-108">**Incremental refresh** - Updates to the transactional database, including object deletes, are synchronized with the entity store models.</span></span>
    
<span data-ttu-id="bc2fb-109">配置の固有のニーズに基づくエンティティ ストア モデルの更新スケジュールを管理するのはシステム管理者の責任です。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-109">It is the responsibility of the system administrator to manage the entity store model refresh schedule based on the unique needs of the deployment.</span></span> <span data-ttu-id="bc2fb-110">組み込みツールでは、モデルの実行時の分析に基づく詳細なメッセージが提供されます。 それはモデル全体が Finance and Operationsトランザクションのデータベースで利用できる最新の更新プログラムで同期していることを確認するのに完全同期が必要なケースを識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-110">The built-in tooling provides detailed messaging based on run-time analysis of the models to help identify cases where a full-synchronization is required to ensure the entire model is synchronized with the latest updates available in the Finance and Operations transactional database.</span></span>

## <a name="administrator-tasks"></a><span data-ttu-id="bc2fb-111">管理者タスク</span><span class="sxs-lookup"><span data-stu-id="bc2fb-111">Administrator tasks</span></span>
<span data-ttu-id="bc2fb-112">このセクションでは、組み込み管理ツールを使用して、エンティティ ストア モデルの管理に関連付けられている活動について説明します。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-112">This section describes the activities associated with managing entity store models using the built-in administration tools.</span></span>

### <a name="perform-a-full-synchronization"></a><span data-ttu-id="bc2fb-113">完全同期の実行</span><span class="sxs-lookup"><span data-stu-id="bc2fb-113">Perform a full synchronization</span></span>
<span data-ttu-id="bc2fb-114">環境をオンラインにした後に最初にするのは、アプリケーションに必要なモデルを識別することです。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-114">The first thing you'll want to do after bringing the environment online is identify the models which are required by the application.</span></span> <span data-ttu-id="bc2fb-115">未使用のモデルの更新に時間を浪費してしまうため、すべてのモデルが必要であると想定するのは正しくありません。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-115">It's incorrect to assume that all of the models are necessary, as this can waste time updating unused models.</span></span> <span data-ttu-id="bc2fb-116">アプリケーション スイートで最初から用意されている利用可能なソリューションをよく理解するため、Finance and Operations で [Power BI コンテンツ](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/power-bi-home-page) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-116">See [Power BI content](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/power-bi-home-page) in Finance and Operations to familiarize yourself with the out-of-box solutions available in the application suite.</span></span>

> [!Important]
> <span data-ttu-id="bc2fb-117">**ProjecCostRevenueAnalysis** および **VendPaymentBIMeasure** エンティティ ストア モデルの両方に対する同期を**無効にする**ことを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-117">We strongly recommend that you **disable** synchronization for both the **ProjecCostRevenueAnalysis** and **VendPaymentBIMeasure** entity store models.</span></span> <span data-ttu-id="bc2fb-118">これらのアプリケーション モデルの両方に、同期プロセス中のパフォーマンス低下のフラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-118">Both of these application models have been flagged for poor performance during the synchronization process.</span></span> <span data-ttu-id="bc2fb-119">次の手順を使用して、アプリケーションで使用されるモデルのエンティティ格納の完全同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-119">Use the following steps to perform a full-synchronization of the entity store for the models used by the application.</span></span>

1. <span data-ttu-id="bc2fb-120">**エンティティ格納**ページに移動します (**システム管理** > **設定** > **エンティティ格納**)。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-120">Go to the **Entity Store** page (**System administration** > **Setup** > **Entity Store**).</span></span>
2. <span data-ttu-id="bc2fb-121">アプリケーションでアクセスできるすべての領域に関連するエンティティ ストア モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-121">Select the entity store models related to all areas accessible in the application.</span></span>
3. <span data-ttu-id="bc2fb-122">ページ上部の**更新**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-122">Click **Refresh** at the top of the page.</span></span>
4. <span data-ttu-id="bc2fb-123">**更新のコンフィギュレーション**ダイアログ ボックスで、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-123">Click **OK** in the **Configure refresh** dialog box.</span></span>
    
<span data-ttu-id="bc2fb-124">このプロセスは、アプリケーションの展開のサイズと幅に応じて 1 時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-124">This process may take up to an hour depending on the size and breadth of the application deployment.</span></span> <span data-ttu-id="bc2fb-125">バッチ ジョブ領域にアクセスし、**測定の配置**のような記述を持つジョブを検索することによって、バック グラウンド同期プロセスのステータスを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-125">You can track the status of the background synchronization process by visiting the batch jobs area and searching for jobs with a description like **Deploy measurement**.</span></span> <span data-ttu-id="bc2fb-126">プロセスが完了したら、埋め込み解析ワークスペースとレポート、および PowerBI.com でホストされているレポートにエンティティ ストア モデルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-126">When the process is complete, you can begin to use the entity store model for embedded analytical workspaces and reports, as well as reports hosted on PowerBI.com.</span></span>

### <a name="start-the-incremental-refresh-processing-engine"></a><span data-ttu-id="bc2fb-127">差分更新の処理エンジンを開始</span><span class="sxs-lookup"><span data-stu-id="bc2fb-127">Start the incremental refresh processing engine</span></span>
<span data-ttu-id="bc2fb-128">最初の全同期プロセスを実行すると、モデルの更新スケジュールの調整を開始する準備ができ、レポートおよび埋め込み分析のユーザーの相互作用を収容できます。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-128">After performing the initial full-synchronization process, you're ready to begin adjusting the model refresh schedule to accommodate users' interactions with reports and embedded analytics.</span></span> <span data-ttu-id="bc2fb-129">差分更新エンジンが、システムのバッチ ジョブを使用してバック グラウンドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-129">The incremental refresh engine runs in the background using a system batch job.</span></span> <span data-ttu-id="bc2fb-130">システム管理者は、差分更新オプションを使用するプロセスを開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-130">System administrators must start the process to utilize the incremental refresh option.</span></span> <span data-ttu-id="bc2fb-131">次の手順を使用して、モデルの差分更新エンジンを有効にします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-131">Use the following steps to turn on the incremental refresh engine for models.</span></span>

1. <span data-ttu-id="bc2fb-132">**変更に基づく警告**ページに移動します (**システム管理** > **設定** > **警告** > **変更に基づく警告**)。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-132">Go to the **Change based alerts** page (**System administration** > **Setup** > **Alerts** > **Change based alerts**).</span></span>
2. <span data-ttu-id="bc2fb-133">バッチ ジョブのオプションを展開するには、**バックグラウンドで実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-133">Click **Run in the background** to expand the batch job options.</span></span>
3. <span data-ttu-id="bc2fb-134">**バッチ処理**オプションを **True** に設定してバック グラウンド処理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-134">Set the **Batch processing** option to **True** to enable the background processing.</span></span>
4. <span data-ttu-id="bc2fb-135">処理の頻度を確立するには、**再実行**テキストをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-135">Click **Recurrence** text to establish the processing frequency.</span></span>
5. <span data-ttu-id="bc2fb-136">**終了日なし**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-136">Select the **No end date** option.</span></span>
6. <span data-ttu-id="bc2fb-137">**定期的なアイテムのパターン**で、処理の頻度を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-137">Under **Recurrence pattern**, select the processing frequency.</span></span>

> [!Note]
> <span data-ttu-id="bc2fb-138">**10 分**の繰り返しパターンから始め、必要に応じて更新することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-138">We recommend that you start with a recurring pattern of **10 minutes** and refine as needed.</span></span> <span data-ttu-id="bc2fb-139">差分処理が完了しない頻度を選択しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-139">Try to avoid selecting a frequency that doesn't allow for an incremental process to complete.</span></span>

<span data-ttu-id="bc2fb-140">差分更新の処理エンジンの頻度を管理するために使用されるダイアログ ボックスのスクリーン ショットです。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-140">Here's a screenshot of the dialog box that is used to manage the frequency of the incremental refresh processing engine.</span></span>

![定期的なアイテムのダイアログの定義](media/Schedule-incremental-refresh.png)

<span data-ttu-id="bc2fb-142">処理エンジンが初期化された後、差分更新の一部のモデルを有効化する開始準備が整います。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-142">After the processing engine is initialized, you're ready to begin enabling select models for incremental refresh.</span></span>

#### <a name="activate-the-incremental-refresh-option-for-selected-models"></a><span data-ttu-id="bc2fb-143">選択したモデルの差分更新オプションを有効化</span><span class="sxs-lookup"><span data-stu-id="bc2fb-143">Activate the incremental refresh option for selected models</span></span>
<span data-ttu-id="bc2fb-144">最初の全同期プロセスを実行すると、モデルの更新スケジュールの調整を開始する準備ができ、レポートおよび埋め込み分析のユーザーの相互作用をよりよく収容できます。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-144">After performing the initial full-synchronization process, you're ready to begin adjusting the model refresh schedule to better accommodate users' interactions with reports and embedded analytics.</span></span> <span data-ttu-id="bc2fb-145">1 日に 1 回よりも頻繁に更新する必要のあるデータが含まれているモデルでは、差分更新オプションを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-145">You'll want to enable the incremental refresh option for models that contain data that must be refreshed more often than once a day.</span></span> <span data-ttu-id="bc2fb-146">まず、完全同期をトリガーするために使用される、既定の待機時間設定を保持することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-146">For starters, it's best to keep the default latency settings used to trigger a full-synchronization.</span></span> <span data-ttu-id="bc2fb-147">次の手順を使用して、特定のエンティティ格納モデルの差分更新オプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-147">Use the following steps to turn on the incremental refresh option for a given entity store model.</span></span>

1. <span data-ttu-id="bc2fb-148">**エンティティ格納**ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-148">Go to the **Entity Store** page.</span></span>
2. <span data-ttu-id="bc2fb-149">アプリケーションでアクセスできるすべての領域に関連するエンティティ ストア モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-149">Select the entity store models related to all areas accessible in the application.</span></span>
3. <span data-ttu-id="bc2fb-150">ページ上部の**編集**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-150">Click the **Edit** button at the top of the page.</span></span>
4. <span data-ttu-id="bc2fb-151">**差分更新**列でチェック ボックスをオンにして差分更新オプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-151">Select the check box in the **Incremental updates** column to enable the incremental refresh option.</span></span>

> [!Note]
> <span data-ttu-id="bc2fb-152">差分更新オプションは、すべてのアプリケーション エンティティ ストア モデルで使用**できません**。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-152">The incremental refresh option is **not** available for all application entity store models.</span></span> <span data-ttu-id="bc2fb-153">拡張機能は、差分更新プロセスでサポートされている集計モデル パターンを展開するプラットフォームの更新プログラムの一部として配信されています。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-153">Enhancements are being delivered as part of platform updates to expand the aggregate model patterns supported by the incremental refresh process.</span></span> <span data-ttu-id="bc2fb-154">警告アイコンはモデルの横に配置され、依然として完全同期が必要です。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-154">An alert icon is placed next to models the still require a full synchronization.</span></span> <span data-ttu-id="bc2fb-155">ほぼリアルタイムな結果を提供するのに使用される任意のモデルの待機時間を短くします。</span><span class="sxs-lookup"><span data-stu-id="bc2fb-155">Provide a lower latency for any models that are used to deliver near real-time results.</span></span>

