---
title: 自動クリーンアップ タスクを使用したパフォーマンスの最適化
description: この記事では、バッチジョブ履歴をクリーンアップすることにより、Microsoft Dynamics 365 Human Resources での一部のパフォーマンスに関する問題を解決する方法について説明します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6a9e94e282aa8f101b42c1378ef21c6c1fe0477e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053494"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="bfd3c-103">自動クリーンアップ タスクを使用したパフォーマンスの最適化</span><span class="sxs-lookup"><span data-stu-id="bfd3c-103">Optimize performance with auto cleanup tasks</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bfd3c-104">**問題点**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-104">**Issue**</span></span>

<span data-ttu-id="bfd3c-105">Microsoft Dynamics 365 Human Resources では、バッチ ジョブ履歴が大きくなりすぎると、パフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="bfd3c-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-106">**Cause**</span></span>

<span data-ttu-id="bfd3c-107">頻繁に実行されるバッチ ジョブにより、バッチ ジョブ履歴の持続不可能な増加につながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="bfd3c-108">これにより、パフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-108">This can cause performance issues.</span></span> 

<span data-ttu-id="bfd3c-109">**解像度**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-109">**Resolution**</span></span>

<span data-ttu-id="bfd3c-110">バッチ ジョブ履歴をクリーンアップする自動タスクをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="bfd3c-111">タスクを毎週実行するよう設定することをお勧めしますが、環境によっては、クリーンアップの実行頻度を増減する必要がある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="bfd3c-112">次の手順には推奨設定が含まれていますが、必要に応じてこれらを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="bfd3c-113">人事管理では、**システム管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="bfd3c-114">**検索** バーで、**バッチ ジョブ履歴のクリーンアップ** を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![バッチ ジョブ履歴のクリーンアップを検索する](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="bfd3c-116">**履歴の範囲 (日数)** で、**30** と入力します。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-116">In **History limit (days)**, enter **30**.</span></span>

   ![履歴の範囲を 30 に設定](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="bfd3c-118">**バックグラウンドで実行** を選択してから、**再実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![再実行の設定](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="bfd3c-120">**再実行の定義** で、**開始日** および **開始時刻** を時間外または週末に実行するよう設定してから、**終了日なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![再実行の開始日時の定義](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="bfd3c-122">**再実行のパターン** で、**日数** を選択し、**指定した間隔で繰り返す** を **7** に設定します。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![クリーンアップを週単位で繰り返すよう設定する](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="bfd3c-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-124">Select **OK**.</span></span>

8. <span data-ttu-id="bfd3c-125">必要に応じて、**バックグラウンドで実行** でその他のパラメータを変更してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd3c-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]