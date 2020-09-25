---
title: プロジェクト リソースのスケジューリング パフォーマンス
description: このトピックでは、多数のプロジェクトのリソース スケジューリングのパフォーマンスを向上させる方法について説明します。
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760599"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="8f926-103">プロジェクト リソースのスケジューリング パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="8f926-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="8f926-104">リソースのスケジューリングに関連するパフォーマンスの問題は、プロジェクトの数が数千に達したときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8f926-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="8f926-105">リソースのスケジューリングのパフォーマンスを改善するために、ユーザーがリソースの可用性フォームを起動するのにかかる時間を節約することができる機能があります。</span><span class="sxs-lookup"><span data-stu-id="8f926-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="8f926-106">具体的には、リソースのキャパシティのロールアップ同期プロセスを削除し、**ResProjectResource** テーブルを使用して、リソースの検索を高速化します。</span><span class="sxs-lookup"><span data-stu-id="8f926-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="8f926-107">**Resrollup** テーブルは使用されなくなりますので注意してください。</span><span class="sxs-lookup"><span data-stu-id="8f926-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f926-108">リソース キャパシティのロールアップの同期プロセス、または **ResProjectResource** テーブルのいずれかに依存関係がある場合は、この機能を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="8f926-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="8f926-109">リソース スケジューリングのパフォーマンス向上の有効化</span><span class="sxs-lookup"><span data-stu-id="8f926-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="8f926-110">リソース スケジューリングのパフォーマンス向上を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8f926-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="8f926-111">**機能の管理** > **すべて** に移動して、機能一覧で **プロジェクト リソース スケジューリングのパフォーマンス向上を有効にする** を見つけます。</span><span class="sxs-lookup"><span data-stu-id="8f926-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="8f926-112">**直ちに有効化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f926-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="8f926-113">一覧にこの機能が見つからない場合は、**更新の確認** を選択して一覧を最新の情報に更新してください。</span><span class="sxs-lookup"><span data-stu-id="8f926-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="8f926-114">ブラウザーを更新した後、**プロジェクト管理および会計** > **定期処理** > **プロジェクト リソース** > **リソース カレンダーのキャパシティをすべての会社に対して同期** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8f926-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="8f926-115">以前のデータを削除する場合は、**既存のキャパシティ レコードの削除** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8f926-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="8f926-116">増分データを生成する場合は、**いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8f926-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="8f926-117">**期間コード** フィールドで、データを生成する期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f926-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="8f926-118">期間コードを選択した場合は、開始日と終了日を定義する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8f926-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="8f926-119">**期間コード** フィールドを空白のままにした場合は、データを生成するための特定の開始日と終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f926-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="8f926-120">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f926-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="8f926-121">これにより、自分の環境内のすべての会社にわたって一般データが **ResCalendarCapacity** テーブルに配布されるので、バッチ ジョブは 1 つの法人でのみ実行される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f926-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="8f926-122">このバッチ ジョブにあるデータは、関連付けられているカレンダーを介してリソースのキャパシティを計算するために必要です。</span><span class="sxs-lookup"><span data-stu-id="8f926-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="8f926-123">**プロジェクト管理および会計** > **定期処理** > **プロジェクトリソース** > **すべての会社間でプロジェクト リソースを設定** に移動してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f926-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="8f926-124">これは、**ResProjectResource**、**ResCalendarDateTimeRange**、および **ResEffectiveDateTimeRange** の各テーブルの一般データのデータ アップグレード スクリプトです。</span><span class="sxs-lookup"><span data-stu-id="8f926-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="8f926-125">**PSAPRojSchedRole activity** フィールドの値も更新されます。</span><span class="sxs-lookup"><span data-stu-id="8f926-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="8f926-126">この機能が実行されていない場合は、リソースのスケジューリングの操作を実行しようとすると警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f926-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="8f926-127">リソース スケジューリングのパフォーマンス向上をオフにする</span><span class="sxs-lookup"><span data-stu-id="8f926-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="8f926-128">**機能の管理** > **すべて** に移動して、**プロジェクト リソース スケジューリングのパフォーマンス向上を有効にする** を見つけます。</span><span class="sxs-lookup"><span data-stu-id="8f926-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="8f926-129">機能を選択し、**無効** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f926-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="8f926-130">ブラウザーを更新します。</span><span class="sxs-lookup"><span data-stu-id="8f926-130">Refresh your browser.</span></span>
4. <span data-ttu-id="8f926-131">**プロジェクト管理と会計** > **定期処理** > **キャパシティ同期** > **リソース キャパシティのロールアップを同期** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8f926-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="8f926-132">**キャパシティ ロールアップ同期** ページで、以前のデータを削除する場合は、**既存の容量レコードを削除する** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8f926-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="8f926-133">増分データを生成する場合は、**いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8f926-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="8f926-134">**期間コード** フィールドで、データを生成する期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f926-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="8f926-135">期間コードを選択した場合は、開始日と終了日を定義する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8f926-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="8f926-136">**期間コード** フィールドを空白のままにした場合は、データを生成するための特定の開始日と終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f926-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="8f926-137">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f926-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="8f926-138">これにより、自分の環境内のすべての会社にわたって一般データが **ResRollup** テーブルに配布されるので、バッチ ジョブは 1 つの法人でのみ実行される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f926-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="8f926-139">このバッチジョブは、すべての **リソースの可用性** ビューに対して必要です。</span><span class="sxs-lookup"><span data-stu-id="8f926-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="8f926-140">このバッチ ジョブを実行しない場合、その **ResRollup** データがその場で生成されます。これには時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="8f926-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
