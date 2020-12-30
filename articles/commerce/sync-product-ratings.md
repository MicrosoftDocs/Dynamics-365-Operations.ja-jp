---
title: Dynamics 365 Commerce の製品評価の同期
description: このトピックでは、Microsoft Dynamics 365 Commerce で製品評価を同期する方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: dec87b548f3a218e1f833b752305f373e893b14c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413820"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="4f6c2-103">Dynamics 365 Commerce の製品評価の同期</span><span class="sxs-lookup"><span data-stu-id="4f6c2-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f6c2-104">このトピックでは、Microsoft Dynamics 365 Commerce で製品評価を同期する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4f6c2-105">概要</span><span class="sxs-lookup"><span data-stu-id="4f6c2-105">Overview</span></span>

<span data-ttu-id="4f6c2-106">販売時点管理 (POS) およびコール センターなどのオムニチャネルで製品評価を使用するには、評価およびレビュー サービスからの製品評価をコマース チャネル データベースにインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="4f6c2-107">製品評価をオムニチャネルで使用可能にした場合、顧客が販売担当者との対話を間接的に行うのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="4f6c2-108">このトピックでは、次のタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="4f6c2-109">**製品評価の同期ジョブ** をバッチ ジョブとしてコンフィギュレーションして、**評価およびレビュー サービス** から製品評価を同期します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="4f6c2-110">製品評価の同期のバッチ ジョブが正常に行われたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="4f6c2-111">POS で製品評価を使用可能にします。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="4f6c2-112">製品評価を同期するバッチ ジョブをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="4f6c2-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f6c2-113">開始する前に、バージョン 10.0.6 またはそれ以降の Dynamics 365 Commerce がインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="4f6c2-114">コマース スケジューラの初期化</span><span class="sxs-lookup"><span data-stu-id="4f6c2-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="4f6c2-115">コマース スケジューラを初期化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="4f6c2-116">**Retail とコマース \> バックオフィスの設定 \> コマース スケジューラ \> コマース スケジューラの初期化** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="4f6c2-117">または、"コマース スケジューラの初期化" を検索します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="4f6c2-118">**コマース スケジューラの初期化** ダイアログ ボックスで、**既存のコンフィギュレーションの削除** オプションが **いいえ** に設定されていることを確認し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="4f6c2-119">RetailProductRating サブジョブの検証</span><span class="sxs-lookup"><span data-stu-id="4f6c2-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="4f6c2-120">**RetailProductRating** サブジョブが存在していることを検証するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="4f6c2-121">**Retail とコマース \> バックオフィスの設定 \> コマース スケジューラ \> スケジューラ サブジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="4f6c2-122">または、「スケジューラ サブジョブ」を検索します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="4f6c2-123">サブジョブ リストで、**RetailProductRating** サブジョブを検索します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="4f6c2-124">次の図は、コマースのサブジョブの詳細ページの例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![RetailProductRating サブジョブの詳細](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="4f6c2-126">**RetailProductRating** サブジョブを検索できない場合、コマース スケジューラを初期化する前に、**同期製品の評価** ジョブおよび **1040 CDX** ジョブが既に実行されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="4f6c2-127">この場合、次の手順に従って **完全データ同期** ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="4f6c2-128">**Retail とコマース \> バックオフィスの設定 \> コマース スケジューラ \> チャネル データベース** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="4f6c2-129">または、「チャネル データベース」を検索します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="4f6c2-130">同期するチャネル データベースを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="4f6c2-131">アクション ウィンドウで、**完全なデータの同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="4f6c2-132">**配送スケジュールの選択** ドロップダウン ダイアログ ボックスで、**1040 - 製品** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="4f6c2-133">前の手順を繰り返して、**RetailProductRating** サブジョブが作成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="4f6c2-134">製品評価のインポート</span><span class="sxs-lookup"><span data-stu-id="4f6c2-134">Import product ratings</span></span>

<span data-ttu-id="4f6c2-135">評価およびレビュー サービスから製品評価をコマースにインポートするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="4f6c2-136">**Retail とコマース \> 本社の設定 \> コマース スケジューラ \> 製品評価の同期ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="4f6c2-137">または、「製品評価の同期ジョブ」を検索します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="4f6c2-138">**製品評価のプル** ダイアログ ボックスの **バックグラウンドで実行** クイック タブで、**定期的なアイテム** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="4f6c2-139">**定期的なアイテムの定義** ダイアログ ボックスで、定期的なアイテムのパターンを設定します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="4f6c2-140">(提案される値は 2 時間です) 1 時間未満の定期的なアイテムをスケジュールしないでください。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="4f6c2-141">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-141">Select **OK**.</span></span>
1. <span data-ttu-id="4f6c2-142">**バッチ処理** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="4f6c2-143">この設定によりログを監査して、バッチ ジョブの実行状況を確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="4f6c2-144">バッチ ジョブをスケジュールするには、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="4f6c2-145">次の図は、コマースのバッチ ジョブ コンフィギュレーションの例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![製品評価の同期バッチ ジョブのコンフィギュレーション](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="4f6c2-147">製品評価の同期のバッチ ジョブが正常に行われたことの確認</span><span class="sxs-lookup"><span data-stu-id="4f6c2-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="4f6c2-148">**製品評価の同期** バッチ ジョブが正常に行われたことを確認するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="4f6c2-149">**Retail とコマース \> システム管理者 \> 照会\> バッチ ジョブ** に移動するか、またはコマース専用の最小在庫管理単位 (SKU) を使用している場合、代わりに **Retail とコマース \> 照会およびレポート \> バッチ ジョブ** を使用します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="4f6c2-150">または、「バッチ ジョブ」を検索します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="4f6c2-151">バッチ ジョブの詳細を表示するには、バッチ ジョブ リストの **ジョブの説明** の列で、「製品評価をプル」を含む説明を検索します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="4f6c2-152">ジョブ ID を選択して、開始予定日/時刻および定期的なアイテムのテキストなどのバッチ ジョブの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="4f6c2-153">次の図は、バッチ ジョブが 2 時間間隔で実行するようにスケジュールされている場合の、コマースでのバッチ ジョブの詳細の例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![製品評価の同期バッチ ジョブの詳細](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="4f6c2-155">POS で製品評価を使用可能にする</span><span class="sxs-lookup"><span data-stu-id="4f6c2-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="4f6c2-156">Dynamics 365 Commerce の評価およびレビュー ソリューションは、オムニチャネル ソリューションです。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="4f6c2-157">ただし、既定では、製品の評価は POS に表示されません。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="4f6c2-158">販売担当者が店舗の顧客に評価とレビューを表示するには、POS で製品評価を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="4f6c2-159">POS で製品の評価を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="4f6c2-160">**Retail とコマース \> コマースの設定 \> パラメーター \> コマース パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="4f6c2-161">または、"コマース パラメーター" を検索します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="4f6c2-162">**コンフィギュレーション パラメーター** タブで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="4f6c2-163">**RatingsAndReviews.EnableProductRatingsForRetailStores** などの名前を入力し、値を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="4f6c2-164">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-164">Select **Save**.</span></span>
1. <span data-ttu-id="4f6c2-165">**Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="4f6c2-166">また、「配送スケジュール」を検索します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="4f6c2-167">ジョブ リストで、**1110** (**グローバル構成**) を選択し、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="4f6c2-168">ジョブが正常に実行された後、製品の評価が POS に表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="4f6c2-169">次の図は、POS で製品評価を有効にするためのコマース パラメーターのコンフィギュレーションの例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![POS での製品評価のコマース パラメーターのコンフィギュレーション](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="4f6c2-171">以下の図は、POS の製品評価の例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-171">The following illustration shows an example of product ratings at the POS.</span></span>

![POS での製品評価](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="4f6c2-173">次の図は、コール センター チャネルの製品評価の例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="4f6c2-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![コール センター チャネルの製品評価](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="4f6c2-175">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4f6c2-175">Additional resources</span></span>

[<span data-ttu-id="4f6c2-176">評価とレビューの概要</span><span class="sxs-lookup"><span data-stu-id="4f6c2-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="4f6c2-177">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="4f6c2-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="4f6c2-178">評価とレビューの管理</span><span class="sxs-lookup"><span data-stu-id="4f6c2-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="4f6c2-179">評価とレビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="4f6c2-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
