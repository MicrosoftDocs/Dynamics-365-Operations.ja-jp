---
title: 行き詰まったバッチ ジョブのリセット
description: このトピックでは、行き詰ったバッチ ジョブの問題の解決方法について説明します。
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d0b12908993070a41d21ac57d6fb504fc6e3b06a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053518"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="8feed-103">行き詰まったバッチ ジョブのリセット</span><span class="sxs-lookup"><span data-stu-id="8feed-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="8feed-104">出庫</span><span class="sxs-lookup"><span data-stu-id="8feed-104">Issue</span></span>

<span data-ttu-id="8feed-105">Microsoft Dynamics 365 Human Resources では、**実行中** または **キャンセル中** のいずれかの状態で処理が行き詰まり、バッチ ジョブ処理が完了しないという問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8feed-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="8feed-106">解像度</span><span class="sxs-lookup"><span data-stu-id="8feed-106">Resolution</span></span>

<span data-ttu-id="8feed-107">バッチ ジョブが **実行中** または **キャンセル中** の状態で処理されなくなった場合は、ジョブを強制的にキャンセルすることでステータス をリセットできます。</span><span class="sxs-lookup"><span data-stu-id="8feed-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="8feed-108">キャンセルした後は、バッチ ジョブを **待機中** ステータスに設定してリセットできます。</span><span class="sxs-lookup"><span data-stu-id="8feed-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="8feed-109">その後、次回スケジュールされたバッチ実行で実行するために、再度取得されます。</span><span class="sxs-lookup"><span data-stu-id="8feed-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="8feed-110">**システム管理** ワークスペースで 、**リンク** ページ を選択し、**バッチ ジョブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8feed-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="8feed-111">**バッチ ジョブ** リスト ページで、リセットする必要があるジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8feed-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="8feed-112">アクション リボンで、**強制キャンセル** を選択し、アクションを確定します。</span><span class="sxs-lookup"><span data-stu-id="8feed-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="8feed-113">**強制キャンセル** アクションは、選択したバッチ ジョブのステータスが **実行中** または **キャンセル中** であり、ジョブに対してバッチの実行またはキャンセルのプロセスが実行されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8feed-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="8feed-114">アクション リボンで、**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8feed-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="8feed-115">**新しいステータスの選択** ページで、**待機中** を選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8feed-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![新しいバッチ ジョブ ステータスの選択](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="8feed-117">参照</span><span class="sxs-lookup"><span data-stu-id="8feed-117">See also</span></span>

[<span data-ttu-id="8feed-118">時間後にバッチ ジョブのスケジュールを設定してパフォーマンスを最適化する</span><span class="sxs-lookup"><span data-stu-id="8feed-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="8feed-119">自動クリーンアップ タスクを使用したパフォーマンスの最適化</span><span class="sxs-lookup"><span data-stu-id="8feed-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
