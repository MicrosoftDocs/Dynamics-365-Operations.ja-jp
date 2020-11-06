---
title: 倉庫作業の繰延処理
description: このトピックでは、Dynamics 365 Supply Chain Management で倉庫作業の繰延処理を使用可能にする機能について説明します。
author: josaw1
manager: tfehr
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc8321c55bc867db065af0cddf356fb497a956e8
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016704"
---
# <a name="deferred-processing-of-warehouse-work"></a><span data-ttu-id="eab85-103">倉庫作業の繰延処理</span><span class="sxs-lookup"><span data-stu-id="eab85-103">Deferred processing of warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eab85-104">このトピックでは、Dynamics 365 Supply Chain Management で倉庫作業の繰延処理を使用可能にする機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="eab85-104">This topic describes the functionality that makes deferred processing of put operations for warehouse work available in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="eab85-105">繰延処理機能では、プット工程がバックグラウンドで処理されている間でも、倉庫作業者は他の作業を続行できます。</span><span class="sxs-lookup"><span data-stu-id="eab85-105">The deferred processing functionality lets warehouse workers continue to do other work while the put operation is processed in the background.</span></span> <span data-ttu-id="eab85-106">繰延処理では、多くの作業明細行を処理する必要があり、作業者がその作業を非同期に処理できるようにする場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="eab85-106">Deferred processing is useful when many work lines must be processed and the worker can let that work be processed asynchronously.</span></span> <span data-ttu-id="eab85-107">また、サーバーの処理時間がアドホックまたは予定外で増加する場合、さらに増加した処理時間がユーザーの生産性に影響を与える可能性がある場合にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="eab85-107">It's also useful when the server can have ad-hoc or unplanned increases in processing time, and the increased processing time might affect the user's productivity.</span></span>

<span data-ttu-id="eab85-108">バックグラウンド処理は、SysOperation フレームワークを使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="eab85-108">Background processing is achieved by using the SysOperation framework.</span></span> <span data-ttu-id="eab85-109">詳細については、[SysOperation フレームワークの概要](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eab85-109">For more information, see [SysOperation Framework Overview](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview).</span></span>

## <a name="configuring-the-work-processing-policies"></a><span data-ttu-id="eab85-110">作業処理ポリシーの構成</span><span class="sxs-lookup"><span data-stu-id="eab85-110">Configuring the work processing policies</span></span>

<span data-ttu-id="eab85-111">繰延処理を使用するには、作業処理ポリシーを構成して使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eab85-111">To use deferred processing, you must configure and use a work processing policy.</span></span>

<span data-ttu-id="eab85-112">ポリシーは、 **作業処理ポリシー** ページで構成されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-112">Policies are configured on the **Work processing policies** page.</span></span> <span data-ttu-id="eab85-113">次の表では、ページのフィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="eab85-113">The following table describes the fields on that page.</span></span>

| <span data-ttu-id="eab85-114">フィールド</span><span class="sxs-lookup"><span data-stu-id="eab85-114">Field</span></span>                           | <span data-ttu-id="eab85-115">説明</span><span class="sxs-lookup"><span data-stu-id="eab85-115">Description</span></span> |
|---------------------------------|-------------|
| <span data-ttu-id="eab85-116">作業処理ポリシー名</span><span class="sxs-lookup"><span data-stu-id="eab85-116">Work processing policy name</span></span>     | <span data-ttu-id="eab85-117">作業処理ポリシーの名前。</span><span class="sxs-lookup"><span data-stu-id="eab85-117">The name of the work processing policy.</span></span> |
| <span data-ttu-id="eab85-118">ワーク オーダー タイプ</span><span class="sxs-lookup"><span data-stu-id="eab85-118">Work order type</span></span>                 | <span data-ttu-id="eab85-119">ポリシーが適用される作業指示書タイプ。</span><span class="sxs-lookup"><span data-stu-id="eab85-119">The work order type that the policy is applied to.</span></span> |
| <span data-ttu-id="eab85-120">操作</span><span class="sxs-lookup"><span data-stu-id="eab85-120">Operation</span></span>                       | <span data-ttu-id="eab85-121">ポリシーを使用して処理される操作。</span><span class="sxs-lookup"><span data-stu-id="eab85-121">The operation that is processed by using the policy.</span></span> |
| <span data-ttu-id="eab85-122">作業処理方法</span><span class="sxs-lookup"><span data-stu-id="eab85-122">Work processing method</span></span>          | <span data-ttu-id="eab85-123">作業明細行の処理に使用されるメソッド。</span><span class="sxs-lookup"><span data-stu-id="eab85-123">The method that is used to process the work line.</span></span> <span data-ttu-id="eab85-124">メソッドが **即時** に設定されている場合、動作は明細行の処理に作業処理ポリシーが使用されていない場合の動作に似ています。</span><span class="sxs-lookup"><span data-stu-id="eab85-124">If the method is set to **Immediate** , the behavior resembles the behavior when no work processing policies are used to process the line.</span></span> <span data-ttu-id="eab85-125">メソッドが **繰延** に設定されている場合は、バッチ フレームワークを使用する繰延処理が使用されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-125">If the method is set to **Deferred** , deferred processing that uses the batch framework is used.</span></span> |
| <span data-ttu-id="eab85-126">繰延処理のしきい値</span><span class="sxs-lookup"><span data-stu-id="eab85-126">Deferred processing threshold</span></span>   | <span data-ttu-id="eab85-127">**0** (ゼロ) の値は、しきい値がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="eab85-127">A value of **0** (zero) indicates that there is no threshold.</span></span> <span data-ttu-id="eab85-128">この場合、繰延処理を使用できる場合は、それが使用されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-128">In this case, deferred processing is used if it can be used.</span></span> <span data-ttu-id="eab85-129">特定のしきい値の計算がしきい値を下回っている場合は、即時メソッドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-129">If the specific threshold calculation is below the threshold, the Immediate method is used.</span></span> <span data-ttu-id="eab85-130">それ以外の場合は、繰延メソッドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-130">Otherwise, the Deferred method is used if it can be used.</span></span> <span data-ttu-id="eab85-131">販売と移動に関連する作業では、しきい値は作業に対して処理されている関連したソース積荷明細行の数として計算されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-131">For sales and transfer-related work, the threshold is calculated as the number of associated source load lines that are being processed for the work.</span></span> <span data-ttu-id="eab85-132">補充作業では、しきい値は作業によって補充されている作業明細行の数として計算されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-132">For replenishment work, the threshold is calculated as the number of work lines that are being replenished by the work.</span></span> <span data-ttu-id="eab85-133">しきい値を設定することによって、たとえば販売に対する **5** 、初期ソース積荷明細行が 5 未満の小さな作業は繰延処理を使用しませんが、大きな作業では使用されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-133">By setting a threshold of, for example, **5** for sales, smaller works that have fewer than five initial source load lines won't use deferred processing, but larger works will use it.</span></span> <span data-ttu-id="eab85-134">しきい値は、作業処理メソッドが **繰延** に設定されている場合にのみ影響があります。</span><span class="sxs-lookup"><span data-stu-id="eab85-134">The threshold has an effect only if the work processing method is set to **Deferred**.</span></span> |
| <span data-ttu-id="eab85-135">遅延処理バッチ グループ</span><span class="sxs-lookup"><span data-stu-id="eab85-135">Deferred processing batch group</span></span> |<span data-ttu-id="eab85-136">処理に使用されるバッチ グループ。</span><span class="sxs-lookup"><span data-stu-id="eab85-136">The batch group that is used for processing.</span></span> |

<span data-ttu-id="eab85-137">繰延プット処理では、販売注文、移動オーダーの出庫、および補充の各作業指示タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="eab85-137">For deferred put-processing, the following work order types are supported: sales order, transfer order issue, and replenishment.</span></span>

## <a name="assigning-the-work-creation-policy"></a><span data-ttu-id="eab85-138">作業作成ポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="eab85-138">Assigning the work creation policy</span></span>

<span data-ttu-id="eab85-139">作業作成ポリシーは、倉庫管理パラメーターで割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="eab85-139">The work creation policy can be assigned in the warehouse management parameters.</span></span> <span data-ttu-id="eab85-140">また、個々の倉庫のレベルで割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="eab85-140">It can also be assigned at the level of individual warehouses.</span></span> <span data-ttu-id="eab85-141">ポリシーが倉庫に割り当てられている場合、その倉庫に対して作成された作業にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-141">If the policy is assigned to a warehouse, it's applied only to work that is created for that warehouse.</span></span> <span data-ttu-id="eab85-142">倉庫レベルにポリシーが割り当てられていない場合、倉庫管理パラメータからのポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-142">If no policy is assigned at the warehouse level, the policy from the warehouse management parameters is applied.</span></span>

## <a name="viewing-the-deferred-put-processing-tasks"></a><span data-ttu-id="eab85-143">繰延プット処理タスクの表示</span><span class="sxs-lookup"><span data-stu-id="eab85-143">Viewing the deferred put processing tasks</span></span>

<span data-ttu-id="eab85-144">繰延プット処理タスクは、 **繰延プット処理タスク** ページで表示できます。</span><span class="sxs-lookup"><span data-stu-id="eab85-144">You can view deferred put processing tasks on the **Deferred put processing tasks** page.</span></span>

<span data-ttu-id="eab85-145">既定では、 **完了済** タスクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-145">By default, the **Completed** tasks are shown.</span></span>

| <span data-ttu-id="eab85-146">フィールド</span><span class="sxs-lookup"><span data-stu-id="eab85-146">Field</span></span>            | <span data-ttu-id="eab85-147">説明</span><span class="sxs-lookup"><span data-stu-id="eab85-147">Description</span></span> |
|------------------|-------------|
| <span data-ttu-id="eab85-148">ステータス</span><span class="sxs-lookup"><span data-stu-id="eab85-148">Status</span></span>           | <span data-ttu-id="eab85-149">タスクの状態。</span><span class="sxs-lookup"><span data-stu-id="eab85-149">The status of the task.</span></span> |
| <span data-ttu-id="eab85-150">バッチ ジョブの状態</span><span class="sxs-lookup"><span data-stu-id="eab85-150">Batch job status</span></span> | <span data-ttu-id="eab85-151">関連するバッチ ジョブの状態。</span><span class="sxs-lookup"><span data-stu-id="eab85-151">The status of the related batch job.</span></span> <span data-ttu-id="eab85-152">バッチ ジョブが処理されている場合、バッチ履歴にはバッチ ジョブのログおよび情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="eab85-152">If the batch job has been processed, the batch history contains the log and information from the batch job.</span></span> |

<span data-ttu-id="eab85-153">状態の説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="eab85-153">Here is an explanation of the possible statuses:</span></span>

- <span data-ttu-id="eab85-154">**待機中** – 関連するバッチ ジョブは、バッチ サーバー上の処理を待機しています。</span><span class="sxs-lookup"><span data-stu-id="eab85-154">**Awaiting** – The related batch job is awaiting processing on the batch server.</span></span>
- <span data-ttu-id="eab85-155">**失敗** – 処理に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="eab85-155">**Failed** – The processing failed.</span></span> <span data-ttu-id="eab85-156">タスクは、 **繰延プットの処理** アクションを使用して再処理したり、または **繰延プットのキャンセル** アクションを使用してキャンセルすることもできます。</span><span class="sxs-lookup"><span data-stu-id="eab85-156">The task can be reprocessed by using the **Process deferred put** action, or it can be canceled by using the **Cancel deferred put** action.</span></span>
- <span data-ttu-id="eab85-157">**完了済** – ジョブが完了しました。</span><span class="sxs-lookup"><span data-stu-id="eab85-157">**Completed** – The job was completed.</span></span>

## <a name="impact-on-closed-work-dates"></a><span data-ttu-id="eab85-158">作業完了日への影響</span><span class="sxs-lookup"><span data-stu-id="eab85-158">Impact on closed work dates</span></span>

<span data-ttu-id="eab85-159">繰延プット処理を使用すると、作業完了日は、繰延プット処理タスクの作成日時として設定されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-159">When deferred put processing is used, the closed work date is set as the created date/time of the deferred put processing tasks.</span></span> <span data-ttu-id="eab85-160">プット工程が完了したときの最善の見積もりであるため、作業完了日が使用されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-160">The closed work date is used because it's the best estimate for when the put operation was completed.</span></span>

## <a name="reprocessing-a-failed-task"></a><span data-ttu-id="eab85-161">失敗したタスクの再処理</span><span class="sxs-lookup"><span data-stu-id="eab85-161">Reprocessing a failed task</span></span>

<span data-ttu-id="eab85-162">失敗したタスクを再処理するには、ページでタスクを選択してから、 **繰延プット処理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eab85-162">You can reprocess a failed task by selecting it on the page and then selecting **Process deferred put**.</span></span> <span data-ttu-id="eab85-163">再処理は、ユーザーがモバイル デバイスからプット アウェイを、まるで即時処理するよう設定されていたかのように完了する状況に対応します。</span><span class="sxs-lookup"><span data-stu-id="eab85-163">Reprocessing corresponds to a situation where the user completes the put-away from the mobile device as if it was set for immediate processing.</span></span>

## <a name="canceling-failed-tasks"></a><span data-ttu-id="eab85-164">失敗したタスクのキャンセル</span><span class="sxs-lookup"><span data-stu-id="eab85-164">Canceling failed tasks</span></span>

<span data-ttu-id="eab85-165">失敗したタスクのみをキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="eab85-165">Only failed tasks can be canceled.</span></span> <span data-ttu-id="eab85-166">タスクをキャンセルすると、新しいユーザーにタスクを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="eab85-166">When you cancel a task, you can assign it to a new user.</span></span> <span data-ttu-id="eab85-167">または、作業を処理したユーザーにタスクを割り当て続けることができます。</span><span class="sxs-lookup"><span data-stu-id="eab85-167">Alternatively, the task can remain assigned to the user who processed the work.</span></span> <span data-ttu-id="eab85-168">キャンセルは、ちょうど最後のピッキング ステップが完了し、作業を片付ける必要があるかのように、作業がモバイル デバイスに戻される状況に対応します。</span><span class="sxs-lookup"><span data-stu-id="eab85-168">Cancellation corresponds to a situation where the work is brought back to the mobile device as if the last pick step was just completed and the work must be put away.</span></span> <span data-ttu-id="eab85-169">ただし、ユーザーは作業が "異なる" と判断できます。それは作業にプット アウェイ ステップのみがあり、その場所は作業を処理した最初のユーザーが最終的なプット場所として持っていた場所に対応するからです。</span><span class="sxs-lookup"><span data-stu-id="eab85-169">However, the user will be able to determine that the work is "different," because it will have only a put-away step, and the location will correspond to the location that the first user who processed the work had as a final put location.</span></span>

<span data-ttu-id="eab85-170">タスクがキャンセルれると、繰延プット処理のブロック理由によって作業がブロックされなくなります。</span><span class="sxs-lookup"><span data-stu-id="eab85-170">When a task is canceled, the work is no longer blocked by the deferred put processing blocking reason.</span></span> <span data-ttu-id="eab85-171">モバイル デバイスを使用して再処理することができます。</span><span class="sxs-lookup"><span data-stu-id="eab85-171">It can be reprocessed by using the mobile device.</span></span>

<span data-ttu-id="eab85-172">タスク レコードは、タスクがキャンセルされると削除されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-172">The task record is deleted when the task canceled.</span></span>

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a><span data-ttu-id="eab85-173">繰延処理ポリシーをスキップするモバイル デバイス メニューの構成</span><span class="sxs-lookup"><span data-stu-id="eab85-173">Configuring the mobile device menu to skip the deferred processing policy</span></span>

<span data-ttu-id="eab85-174">繰延処理ポリシーが使用されないように、モバイル デバイスのメニュー項目を構成できます。</span><span class="sxs-lookup"><span data-stu-id="eab85-174">You can configure the mobile device menu item so that the deferred processing policy isn't used.</span></span> <span data-ttu-id="eab85-175">繰延処理ポリシーが使用されていない場合、作業はそのまま処理されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-175">The work is then processed as it is when no deferred processing policy is used.</span></span> <span data-ttu-id="eab85-176">この機能により、監修者は繰延プットが使用されていない特定のメニュー項目を使用できます。</span><span class="sxs-lookup"><span data-stu-id="eab85-176">This functionality lets a supervisor use a specific menu item where deferred put isn't used.</span></span> <span data-ttu-id="eab85-177">構成するには、 **繰延プット処理ポリシー** フィールドを、 **設定の上書きおよび同期的なプット処理** に設定します。</span><span class="sxs-lookup"><span data-stu-id="eab85-177">To configure it, set the **Deferred put processing policy** field to **Override settings and process put synchronously**.</span></span> 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a><span data-ttu-id="eab85-178">繰延プット処理が適用されない場合の制限</span><span class="sxs-lookup"><span data-stu-id="eab85-178">Restrictions when the deferred put processing isn't applied</span></span>

<span data-ttu-id="eab85-179">ポリシーが構成されていても、繰延プット処理が適用されないいくつかのシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="eab85-179">There are several scenarios where deferred put processing isn't applied even though the policy is configured.</span></span> <span data-ttu-id="eab85-180">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="eab85-180">Here are some examples:</span></span>

- <span data-ttu-id="eab85-181">作業の手動完了が使用されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-181">Manual work completion is used.</span></span>
- <span data-ttu-id="eab85-182">作業は、自動完了を使用して完了します。</span><span class="sxs-lookup"><span data-stu-id="eab85-182">The work is completed by using auto-completion.</span></span>
- <span data-ttu-id="eab85-183">監査テンプレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-183">Audit templates are used.</span></span>


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a><span data-ttu-id="eab85-184">出庫作業監視ワークスペースからの繰延処理タスクの監視</span><span class="sxs-lookup"><span data-stu-id="eab85-184">Monitoring the deferred processing tasks from the Outbound work monitoring workspace</span></span>

<span data-ttu-id="eab85-185">**出庫作業監視** ワークスペースには、繰延プット処理タスクの監視に役立つ 2 つのタイルがあります。</span><span class="sxs-lookup"><span data-stu-id="eab85-185">The **Outbound work monitoring** workspace has two tiles that help you monitor deferred put processing tasks:</span></span>

- <span data-ttu-id="eab85-186">**失敗した繰延プット処理タスク** – このタイルには、失敗したタスクの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-186">**Failed deferred put processing tasks** – This tile shows the number of failed tasks.</span></span> <span data-ttu-id="eab85-187">失敗したタスクがある場合、タスクは自動的に再処理されないため、倉庫マネージャーはタスクを再処理するかキャンセルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eab85-187">If there are failed tasks, the warehouse manager must either reprocess them or cancel them, because they won't be reprocessed automatically.</span></span>
- <span data-ttu-id="eab85-188">**繰延プット処理タスクの待機中** – このタイルには、10 分を超えて **待機中** 状態にあるタスクの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eab85-188">**Awaiting deferred put processing tasks** – This tile shows the number of tasks that have been in the **Awaiting** status for more than 10 minutes.</span></span> <span data-ttu-id="eab85-189">タイルに番号が表示される場合は、バッチ処理中に問題が発生したことを示している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eab85-189">If the tile shows a number, it might indicate that an issue occurred during batch processing.</span></span> <span data-ttu-id="eab85-190">**待機中** タスクを手動で処理できます。</span><span class="sxs-lookup"><span data-stu-id="eab85-190">You can manually process the **Awaiting** tasks.</span></span> <span data-ttu-id="eab85-191">タスクのバッチ ジョブが後で処理される場合、それは既に処理されているため、失敗します。</span><span class="sxs-lookup"><span data-stu-id="eab85-191">If the batch job for a task is processed later, it will just fail, because it has already been processed.</span></span> <span data-ttu-id="eab85-192">影響はありません。</span><span class="sxs-lookup"><span data-stu-id="eab85-192">There will be no impact.</span></span>

## <a name="deleting-completed-tasks"></a><span data-ttu-id="eab85-193">完了済みのタスクの削除</span><span class="sxs-lookup"><span data-stu-id="eab85-193">Deleting completed tasks</span></span>

<span data-ttu-id="eab85-194">完了した繰延プット処理タスクは、それらを選択してページ上で削除することで削除できます。</span><span class="sxs-lookup"><span data-stu-id="eab85-194">You can delete deferred put processing tasks that have been completed by selecting them and deleting them on the page.</span></span>
