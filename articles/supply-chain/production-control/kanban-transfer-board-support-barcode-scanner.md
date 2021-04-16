---
title: バーコード スキャナー用かんばん転送ボードのサポート
description: かんばん転送ボードは、かんばん作業を選択、開始、完了、および空にするためのウィジェット バーコード スキャナーのスキャナー入力をサポートします。
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a7073fb5d77e2d11569e86b92433864371f0e1d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825870"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="90985-103">バーコード スキャナー用かんばん転送ボードのサポート</span><span class="sxs-lookup"><span data-stu-id="90985-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90985-104">かんばん転送ボードは、かんばん作業を選択、開始、完了、および空にするためのウィジェット バーコード スキャナーのスキャナー入力をサポートします。</span><span class="sxs-lookup"><span data-stu-id="90985-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="90985-105">登録モード</span><span class="sxs-lookup"><span data-stu-id="90985-105">Registration modes</span></span>
------------------

<span data-ttu-id="90985-106">**スキャナーの登録** クイック タブで登録モードを選択すると、登録モードを選択できます。これは、[かんばんカード番号] フィールドでかんばんカード番号をスキャンまたは手動入力するときのアクションを制御します。</span><span class="sxs-lookup"><span data-stu-id="90985-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="90985-107">登録モードの設定</span><span class="sxs-lookup"><span data-stu-id="90985-107">Set registration mode</span></span> | <span data-ttu-id="90985-108">説明</span><span class="sxs-lookup"><span data-stu-id="90985-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90985-109">開始日</span><span class="sxs-lookup"><span data-stu-id="90985-109">Start</span></span>                 | <span data-ttu-id="90985-110">かんばん転送ジョブを進行中として登録します。</span><span class="sxs-lookup"><span data-stu-id="90985-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="90985-111">完了</span><span class="sxs-lookup"><span data-stu-id="90985-111">Complete</span></span>              | <span data-ttu-id="90985-112">かんばん転送ジョブを完了として登録します。</span><span class="sxs-lookup"><span data-stu-id="90985-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="90985-113">空</span><span class="sxs-lookup"><span data-stu-id="90985-113">Empty</span></span>                 | <span data-ttu-id="90985-114">かんばんカードで参照される材料取り扱い単位を空として登録します。</span><span class="sxs-lookup"><span data-stu-id="90985-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="90985-115">選択</span><span class="sxs-lookup"><span data-stu-id="90985-115">Select</span></span>                | <span data-ttu-id="90985-116">かんばんカード番号を登録すると、自動的にかんばんリストに参照されるジョブが選択されます。</span><span class="sxs-lookup"><span data-stu-id="90985-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="90985-117">[選択] の登録モード</span><span class="sxs-lookup"><span data-stu-id="90985-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="90985-118">ジョブを選択するのにバーコードを使用する場合、かんばんボードの表示モードを変更します。</span><span class="sxs-lookup"><span data-stu-id="90985-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="90985-119">このモードでは、次の要件が適用されます。</span><span class="sxs-lookup"><span data-stu-id="90985-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="90985-120">スキャンしたかんばん作業のみを表示します。</span><span class="sxs-lookup"><span data-stu-id="90985-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="90985-121">選択したジョブの詳細は、**詳細** クイック タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="90985-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="90985-122">**メッセージ** クイック タブでは、選択したジョブに対してのみメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="90985-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="90985-123">[アクション ウィンドウ] で使用できる機能を使用してジョブのステータスを変更できます。</span><span class="sxs-lookup"><span data-stu-id="90985-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="90985-124">今回、かんばん転送ボードは 1 つのジョブのみを継続して表示します。</span><span class="sxs-lookup"><span data-stu-id="90985-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="90985-125">ジョブのリストの情報を手動で更新するには、アクション ペインの **更新** (Shift+F5) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="90985-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="90985-126">情報を更新すると、ジョブのフィルターの完全な結果が再び表示されます。</span><span class="sxs-lookup"><span data-stu-id="90985-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="90985-127">ジョブ状態と実行可能なアクション</span><span class="sxs-lookup"><span data-stu-id="90985-127">Job status and possible actions</span></span>
<span data-ttu-id="90985-128">選択したジョブのステータスおよびイベントのかんばんにペギングされたジョブのステータスによって、このジョブをさらに処理するかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="90985-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="90985-129">次の表に、これらのステータスやタスクに関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="90985-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="90985-130">ジョブに使用できるステータス、またはジョブによって参照される材料取り扱い単位のステータス。</span><span class="sxs-lookup"><span data-stu-id="90985-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="90985-131">ジョブに対して実行できる各タスク。</span><span class="sxs-lookup"><span data-stu-id="90985-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90985-132">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="90985-132">Job type</span></span></th>
<th><span data-ttu-id="90985-133">ジョブ ステータスまたは材料取り扱い単位ステータス</span><span class="sxs-lookup"><span data-stu-id="90985-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="90985-134">ピッキング リストの更新</span><span class="sxs-lookup"><span data-stu-id="90985-134">Update picking list</span></span></th>
<th><span data-ttu-id="90985-135">開始日</span><span class="sxs-lookup"><span data-stu-id="90985-135">Start</span></span></th>
<th><span data-ttu-id="90985-136">登録の更新</span><span class="sxs-lookup"><span data-stu-id="90985-136">Update registration</span></span></th>
<th><span data-ttu-id="90985-137">完了</span><span class="sxs-lookup"><span data-stu-id="90985-137">Complete</span></span></th>
<th><span data-ttu-id="90985-138">空</span><span class="sxs-lookup"><span data-stu-id="90985-138">Empty</span></span></th>
<th><span data-ttu-id="90985-139">イベントのかんばんを作成</span><span class="sxs-lookup"><span data-stu-id="90985-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90985-140">移動</span><span class="sxs-lookup"><span data-stu-id="90985-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="90985-141">未定</span><span class="sxs-lookup"><span data-stu-id="90985-141">Not planned</span></span></li>
<li><span data-ttu-id="90985-142">ペギングにしたジョブがない、またはペギングにしたジョブが [完了]</span><span class="sxs-lookup"><span data-stu-id="90985-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="90985-143">有</span><span class="sxs-lookup"><span data-stu-id="90985-143">Yes</span></span></td>
<td><span data-ttu-id="90985-144">有</span><span class="sxs-lookup"><span data-stu-id="90985-144">Yes</span></span></td>
<td><span data-ttu-id="90985-145">有</span><span class="sxs-lookup"><span data-stu-id="90985-145">Yes</span></span></td>
<td><span data-ttu-id="90985-146">有</span><span class="sxs-lookup"><span data-stu-id="90985-146">Yes</span></span></td>
<td><span data-ttu-id="90985-147">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-147">No</span></span></td>
<td><span data-ttu-id="90985-148">有</span><span class="sxs-lookup"><span data-stu-id="90985-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90985-149">移動</span><span class="sxs-lookup"><span data-stu-id="90985-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="90985-150">未定</span><span class="sxs-lookup"><span data-stu-id="90985-150">Not planned</span></span></li>
<li><span data-ttu-id="90985-151">ペギングにされたジョブが [完了] ではない</span><span class="sxs-lookup"><span data-stu-id="90985-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="90985-152">有</span><span class="sxs-lookup"><span data-stu-id="90985-152">Yes</span></span></td>
<td><span data-ttu-id="90985-153">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-153">No</span></span></td>
<td><span data-ttu-id="90985-154">有</span><span class="sxs-lookup"><span data-stu-id="90985-154">Yes</span></span></td>
<td><span data-ttu-id="90985-155">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-155">No</span></span></td>
<td><span data-ttu-id="90985-156">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-156">No</span></span></td>
<td><span data-ttu-id="90985-157">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90985-158">移動</span><span class="sxs-lookup"><span data-stu-id="90985-158">Transfer</span></span></td>
<td><span data-ttu-id="90985-159">処理中</span><span class="sxs-lookup"><span data-stu-id="90985-159">In progress</span></span></td>
<td><span data-ttu-id="90985-160">有</span><span class="sxs-lookup"><span data-stu-id="90985-160">Yes</span></span></td>
<td><span data-ttu-id="90985-161">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-161">No</span></span></td>
<td><span data-ttu-id="90985-162">有</span><span class="sxs-lookup"><span data-stu-id="90985-162">Yes</span></span></td>
<td><span data-ttu-id="90985-163">有</span><span class="sxs-lookup"><span data-stu-id="90985-163">Yes</span></span></td>
<td><span data-ttu-id="90985-164">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-164">No</span></span></td>
<td><span data-ttu-id="90985-165">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90985-166">移動</span><span class="sxs-lookup"><span data-stu-id="90985-166">Transfer</span></span></td>
<td><span data-ttu-id="90985-167">完了</span><span class="sxs-lookup"><span data-stu-id="90985-167">Completed</span></span></td>
<td><span data-ttu-id="90985-168">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-168">No</span></span></td>
<td><span data-ttu-id="90985-169">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-169">No</span></span></td>
<td><span data-ttu-id="90985-170">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-170">No</span></span></td>
<td><span data-ttu-id="90985-171">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-171">No</span></span></td>
<td><span data-ttu-id="90985-172">有</span><span class="sxs-lookup"><span data-stu-id="90985-172">Yes</span></span></td>
<td><span data-ttu-id="90985-173">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90985-174">転送または処理中</span><span class="sxs-lookup"><span data-stu-id="90985-174">Transfer or process</span></span></td>
<td><span data-ttu-id="90985-175">空</span><span class="sxs-lookup"><span data-stu-id="90985-175">Empty</span></span></td>
<td><span data-ttu-id="90985-176">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-176">No</span></span></td>
<td><span data-ttu-id="90985-177">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-177">No</span></span></td>
<td><span data-ttu-id="90985-178">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-178">No</span></span></td>
<td><span data-ttu-id="90985-179">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-179">No</span></span></td>
<td><span data-ttu-id="90985-180">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-180">No</span></span></td>
<td><span data-ttu-id="90985-181">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90985-182">転送または処理中</span><span class="sxs-lookup"><span data-stu-id="90985-182">Transfer or process</span></span></td>
<td><span data-ttu-id="90985-183">かんばんカードがない</span><span class="sxs-lookup"><span data-stu-id="90985-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="90985-184">いいえ</span><span class="sxs-lookup"><span data-stu-id="90985-184">No</span></span></td>
<td><span data-ttu-id="90985-185">いいえ</span><span class="sxs-lookup"><span data-stu-id="90985-185">No</span></span></td>
<td><span data-ttu-id="90985-186">いいえ</span><span class="sxs-lookup"><span data-stu-id="90985-186">No</span></span></td>
<td><span data-ttu-id="90985-187">いいえ</span><span class="sxs-lookup"><span data-stu-id="90985-187">No</span></span></td>
<td><span data-ttu-id="90985-188">いいえ</span><span class="sxs-lookup"><span data-stu-id="90985-188">No</span></span></td>
<td><span data-ttu-id="90985-189">いいえ</span><span class="sxs-lookup"><span data-stu-id="90985-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90985-190">転送または処理中</span><span class="sxs-lookup"><span data-stu-id="90985-190">Transfer or process</span></span></td>
<td><span data-ttu-id="90985-191">かんばんカードはあるが、かんばんに割り当てられていない</span><span class="sxs-lookup"><span data-stu-id="90985-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="90985-192">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-192">No</span></span></td>
<td><span data-ttu-id="90985-193">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-193">No</span></span></td>
<td><span data-ttu-id="90985-194">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-194">No</span></span></td>
<td><span data-ttu-id="90985-195">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-195">No</span></span></td>
<td><span data-ttu-id="90985-196">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-196">No</span></span></td>
<td><span data-ttu-id="90985-197">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90985-198">処理</span><span class="sxs-lookup"><span data-stu-id="90985-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="90985-199">未定</span><span class="sxs-lookup"><span data-stu-id="90985-199">Not planned</span></span></li>
<li><span data-ttu-id="90985-200">準備済</span><span class="sxs-lookup"><span data-stu-id="90985-200">Prepared</span></span></li>
<li><span data-ttu-id="90985-201">処理中</span><span class="sxs-lookup"><span data-stu-id="90985-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="90985-202">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-202">No</span></span></td>
<td><span data-ttu-id="90985-203">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-203">No</span></span></td>
<td><span data-ttu-id="90985-204">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-204">No</span></span></td>
<td><span data-ttu-id="90985-205">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-205">No</span></span></td>
<td><span data-ttu-id="90985-206">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-206">No</span></span></td>
<td><span data-ttu-id="90985-207">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90985-208">処理</span><span class="sxs-lookup"><span data-stu-id="90985-208">Process</span></span></td>
<td><span data-ttu-id="90985-209">完了</span><span class="sxs-lookup"><span data-stu-id="90985-209">Completed</span></span></td>
<td><span data-ttu-id="90985-210">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-210">No</span></span></td>
<td><span data-ttu-id="90985-211">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-211">No</span></span></td>
<td><span data-ttu-id="90985-212">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-212">No</span></span></td>
<td><span data-ttu-id="90985-213">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-213">No</span></span></td>
<td><span data-ttu-id="90985-214">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-214">No</span></span></td>
<td><span data-ttu-id="90985-215">第        条</span><span class="sxs-lookup"><span data-stu-id="90985-215">No</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]