---
title: 数時間後にバッチ ジョブのスケジュールを設定して、パフォーマンスを最適化する
description: このトピックでは、数時間後の実行時間が長いバッチ ジョブのスケジュールを設定して、Microsoft Dynamics 365 Human Resources でのパフォーマンスに関する問題を解決する方法について説明します。
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 92dd281ed718be5c7ebd843d015c108ee121f30a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794928"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="c3615-103">数時間後にバッチ ジョブのスケジュールを設定して、パフォーマンスを最適化する</span><span class="sxs-lookup"><span data-stu-id="c3615-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="c3615-104">問題</span><span class="sxs-lookup"><span data-stu-id="c3615-104">Issue</span></span>

<span data-ttu-id="c3615-105">Microsoft Dynamics 365 Human Resources は、通常の営業時間中に実行時間の長いバッチジョブを実行する場合、パフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c3615-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="c3615-106">解像度</span><span class="sxs-lookup"><span data-stu-id="c3615-106">Resolution</span></span>

<span data-ttu-id="c3615-107">次のバッチ ジョブを業務時間外にスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="c3615-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="c3615-108">また、頻繁に実行されるバッチ ジョブの頻度を確認することもお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c3615-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="c3615-109">可能な場合は、バッチ ジョブの繰り返しを減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="c3615-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="c3615-110">多くの場合、既定の頻度で十分です。</span><span class="sxs-lookup"><span data-stu-id="c3615-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="c3615-111">次のバッチ ジョブは、深夜またはそれより後の時間に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3615-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="c3615-112">これらの定期的なバッチ ジョブのタイム ゾーンを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c3615-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="c3615-113">一部のバッチ ジョブは、太平洋標準時 (PST) を使用している場合があります。</span><span class="sxs-lookup"><span data-stu-id="c3615-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="c3615-114">バッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="c3615-114">Batch job</span></span> | <span data-ttu-id="c3615-115">既定の発生</span><span class="sxs-lookup"><span data-stu-id="c3615-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="c3615-116">バッチ ジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="c3615-116">Batch job history cleanup</span></span> | <span data-ttu-id="c3615-117">月ごとに 1 回</span><span class="sxs-lookup"><span data-stu-id="c3615-117">1 time per month</span></span> |
| <span data-ttu-id="c3615-118">ステージング クリーンアップのエクスポート</span><span class="sxs-lookup"><span data-stu-id="c3615-118">Export staging cleanup</span></span> | <span data-ttu-id="c3615-119">1 日に 1 回</span><span class="sxs-lookup"><span data-stu-id="c3615-119">1 time per day</span></span> |
| <span data-ttu-id="c3615-120">Common Data Service の統合で要求の同期が達成されませんでした</span><span class="sxs-lookup"><span data-stu-id="c3615-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="c3615-121">1 日に 1 回</span><span class="sxs-lookup"><span data-stu-id="c3615-121">1 time per day</span></span> |
| <span data-ttu-id="c3615-122">業務時間外に定期的に実行する必要があるデータベース圧縮システム ジョブ</span><span class="sxs-lookup"><span data-stu-id="c3615-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="c3615-123">1 日に 1 回</span><span class="sxs-lookup"><span data-stu-id="c3615-123">1 time per day</span></span> |
| <span data-ttu-id="c3615-124">業務時間外に定期的に実行する必要があるデータベース インデックス リビルド システム ジョブ</span><span class="sxs-lookup"><span data-stu-id="c3615-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="c3615-125">1 日に 1 回</span><span class="sxs-lookup"><span data-stu-id="c3615-125">1 time per day</span></span> |

1. <span data-ttu-id="c3615-126">人事管理では、**システム管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3615-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="c3615-127">**検索** バーで、上記のバッチ ジョブのいずれかを検索します。</span><span class="sxs-lookup"><span data-stu-id="c3615-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="c3615-128">**バックグラウンドで実行** を選択して、**再実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3615-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![再実行の設定](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="c3615-130">**再実行の定義** で、**開始日** および **開始時刻** を時間外または週末に発生するよう設定します。</span><span class="sxs-lookup"><span data-stu-id="c3615-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="c3615-131">**終了日なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3615-131">Select **No end date**.</span></span> 

   ![再実行の開始日時の定義](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="c3615-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3615-133">Select **OK**.</span></span>

6. <span data-ttu-id="c3615-134">必要に応じて、**バックグラウンドで実行** でその他のパラメータを変更してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3615-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3615-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c3615-135">Additional resources</span></span>

[<span data-ttu-id="c3615-136">自動クリーンアップ タスクを使用したパフォーマンスの最適化</span><span class="sxs-lookup"><span data-stu-id="c3615-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]