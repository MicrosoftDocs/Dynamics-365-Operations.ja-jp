---
title: 手動在庫移動の繰延処理
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management で手動在庫移動の繰延処理を使用する方法について説明します。
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 54a202b7e6728bc83022851c901d3c5db17510bf
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956724"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a><span data-ttu-id="4d5c8-103">手動在庫移動の繰延処理</span><span class="sxs-lookup"><span data-stu-id="4d5c8-103">Deferred processing of manual inventory movement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d5c8-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management で手動在庫移動の繰延処理を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-104">This topic describes how to use deferred processing of manual inventory movement in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="4d5c8-105">繰延処理では、プット工程がバックグラウンドで処理されている間でも、倉庫作業者は他の作業を続行できます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-105">Deferred processing lets warehouse workers continue to do other work while a put operation is processed in the background.</span></span> <span data-ttu-id="4d5c8-106">繰延処理は、サーバーの処理時間が一時的または予定外で増加する場合、さらに増加した処理時間が作業者の生産性に影響を与える可能性がある場合にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-106">Deferred processing is useful when the server can have occasional or unplanned increases in processing time, and the increased processing time might affect worker productivity.</span></span> <span data-ttu-id="4d5c8-107">*在庫移動* 作業タイプが、この機能でサポートされる一連の作業タイプに追加されました。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-107">The *Inventory movement* work type has now been added to the set of work types that this feature supports.</span></span>

<span data-ttu-id="4d5c8-108">バックグラウンド処理は、[倉庫アプリのイベント処理機能](warehouse-app-events.md) を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-108">Background processing is achieved by using the [Process warehouse app events feature](warehouse-app-events.md).</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="4d5c8-109">システムでこの機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="4d5c8-109">Turn on this feature for your system</span></span>

<span data-ttu-id="4d5c8-110">この機能を使用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で次の機能をオンにします。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span> <span data-ttu-id="4d5c8-111">次の順序でオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-111">You must turn them on in this order:</span></span>

1. <span data-ttu-id="4d5c8-112">組織全体の作業のブロック</span><span class="sxs-lookup"><span data-stu-id="4d5c8-112">Organization-wide work blocking</span></span>
1. <span data-ttu-id="4d5c8-113">倉庫アプリ イベントの処理</span><span class="sxs-lookup"><span data-stu-id="4d5c8-113">Process warehouse app events</span></span>
1. <span data-ttu-id="4d5c8-114">遅延プット オペレーション</span><span class="sxs-lookup"><span data-stu-id="4d5c8-114">Deferred put operations</span></span>
1. <span data-ttu-id="4d5c8-115">手動在庫移動操作の遅延処理</span><span class="sxs-lookup"><span data-stu-id="4d5c8-115">Deferred processing of manual inventory movement operation</span></span>

## <a name="configure-the-work-processing-policies"></a><span data-ttu-id="4d5c8-116">作業処理ポリシーの構成</span><span class="sxs-lookup"><span data-stu-id="4d5c8-116">Configure the work processing policies</span></span>

<span data-ttu-id="4d5c8-117">繰延処理を使用するには、作業処理ポリシーを設定して使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-117">To use deferred processing, you must set up and use a work processing policy.</span></span> <span data-ttu-id="4d5c8-118">繰延プット処理では、[倉庫作業の繰延処理機能](deferred-put.md)は、*販売注文*、*移動オーダーの出庫*、および *補充* の作業タイプをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-118">For deferred put processing, the [Deferred processing of warehouse work feature](deferred-put.md) supports the following work types: *Sales order*, *Transfer order issue*, and *Replenishment*.</span></span> <span data-ttu-id="4d5c8-119">*手動在庫移動の繰延処理操作* 機能によって、新しい作業タイプ *在庫移動* が追加されます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-119">The *Deferred processing of manual inventory movement operation* features adds a new work type: *Inventory movement*.</span></span>

<span data-ttu-id="4d5c8-120">作業処理ポリシーを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-120">To set up a work processing policy, follow these steps.</span></span>

1. <span data-ttu-id="4d5c8-121">**倉庫管理\>設定\>作業\>作業処理ポリシー** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-121">Go to **Warehouse management \> Setup \> Work \> Work processing policies**.</span></span>
1. <span data-ttu-id="4d5c8-122">一覧で既存のポリシーを選択するか、アクション ペインで **新規** を選択して新しいポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-122">Either select an existing policy in the list, or create a new policy by selecting **New** on the Action Pane.</span></span> <span data-ttu-id="4d5c8-123">各ポリシーのヘッダーには次のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-123">The header of every policy has the following fields:</span></span>

    - <span data-ttu-id="4d5c8-124">**作業処理ポリシー名** – 作業処理ポリシーの名前。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-124">**Work processing policy name** – The name of the work processing policy.</span></span>
    - <span data-ttu-id="4d5c8-125">**説明** – 作業処理ポリシーの説明。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-125">**Description** – A description of the work processing policy.</span></span>

1. <span data-ttu-id="4d5c8-126">**処理ルール** クイック タブで、ポリシーが適用するルールのコレクションを設定します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-126">On the **Processing rules** FastTab, set up the collection of rules that the policy will apply.</span></span> <span data-ttu-id="4d5c8-127">ツールバーのボタンを使用して、必要に応じてルールを追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-127">Use the buttons on the toolbar to add or remove rules as you require.</span></span> <span data-ttu-id="4d5c8-128">ルールごとに、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-128">For each rule, set the following fields:</span></span>

    - <span data-ttu-id="4d5c8-129">**作業指示書タイプ** – ポリシーが適用される作業タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-129">**Work order type** – Select the work type that the policy applies to.</span></span>
    - <span data-ttu-id="4d5c8-130">**工程** – ポリシーを処理するために使用する工程を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-130">**Operation** – Select the operation that the policy is used to process.</span></span> <span data-ttu-id="4d5c8-131">**作業指示書タイプ** フィールドで *在庫移動* を選択した場合は、ピック工程とプット工程の両方が 1 つのイベントとして処理されるので、このフィールドを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-131">If you selected *Inventory movement* in the **Work order type** field, you don't have to set this field, because both pick operations and put operations are processed as a single event.</span></span>
    - <span data-ttu-id="4d5c8-132">**作業処理方法** – 作業明細行の処理に使用する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-132">**Work processing method** – Select the method that is used to process the work line.</span></span> <span data-ttu-id="4d5c8-133">*即時* を選択した場合、動作は明細行の処理に作業処理ポリシーが使用されていない場合の動作に似ています。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-133">If you select *Immediate*, the behavior resembles the behavior when no work processing policies are used to process the line.</span></span> <span data-ttu-id="4d5c8-134">*繰延* を選択した場合、システムは、バッチ フレームワークを使用する繰延処理を適用します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-134">If you select *Deferred*, the system will apply deferred processing that uses the batch framework.</span></span>
    - <span data-ttu-id="4d5c8-135">**繰延処理のしきい値** – このフィールドを *0* (ゼロ) に設定した場合は、しきい値はありません。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-135">**Deferred processing threshold** – If you set this field to *0* (zero), there is no threshold.</span></span> <span data-ttu-id="4d5c8-136">この場合、可能ならば *繰延* 処理方法が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-136">In this case, the *Deferred* processing method is used if possible.</span></span> <span data-ttu-id="4d5c8-137">特定のしきい値の計算がしきい値を下回っている場合は、*即時メソッド* が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-137">If the specific threshold calculation is below the threshold, the *Immediate* method is used.</span></span> <span data-ttu-id="4d5c8-138">それ以外の場合は、可能ならば *繰延* メソッドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-138">Otherwise, the *Deferred* method is used if possible.</span></span> <span data-ttu-id="4d5c8-139">販売と移動に関連する作業では、しきい値は作業に対して処理されている関連したソース積荷明細行の数として計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-139">For sales and transfer-related work, the threshold is calculated as the number of associated source load lines that are being processed for the work.</span></span> <span data-ttu-id="4d5c8-140">補充作業では、しきい値は作業によって補充されている作業明細行の数として計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-140">For replenishment work, the threshold is calculated as the number of work lines that are being replenished by the work.</span></span> <span data-ttu-id="4d5c8-141">たとえば販売に対するしきい値を *5* に設定することによって、初期ソース積荷明細行が 5 未満の小さな作業は繰延処理を使用せず、大きな作業では使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-141">By setting a threshold of, for example, *5* for sales, you ensure that smaller works that have fewer than five initial source load lines won't use deferred processing, but larger works will use it.</span></span> <span data-ttu-id="4d5c8-142">しきい値は、**作業処理メソッド** フィールドが *繰延* に設定されている場合にのみ影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-142">The threshold has an effect only if the **Work processing method** field is set to *Deferred*.</span></span>
    - <span data-ttu-id="4d5c8-143">**遅延処理バッチ グループ** – 処理に使用するバッチ グループを指定します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-143">**Deferred processing batch group** – Specify the batch group that is used for processing.</span></span> <span data-ttu-id="4d5c8-144">**作業指示書タイプ** フィールドで *在庫移動* を選択した場合は、**倉庫アプリ イベントの処理** ダイアログ ボックスでバッチ グループが選択されているので、このフィールドを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-144">If you selected *Inventory movement* in the **Work order type** field, you don't have to set this field, because the batch group is selected in the **Process warehouse app events** dialog box.</span></span>

## <a name="assign-the-work-creation-policy"></a><span data-ttu-id="4d5c8-145">作業作成ポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="4d5c8-145">Assign the work creation policy</span></span>

<span data-ttu-id="4d5c8-146">作業作成ポリシーの割り当て方法の詳細については、[倉庫作業の繰延処理](deferred-put.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-146">For details about how to assign a work creation policy, see [Deferred processing of warehouse work](deferred-put.md).</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="4d5c8-147">倉庫アプリのイベントを処理するためのバッチ ジョブを設定する</span><span class="sxs-lookup"><span data-stu-id="4d5c8-147">Set up a batch job to process warehouse app events</span></span>

<span data-ttu-id="4d5c8-148">*手動在庫移動の繰延処理操作* プロセスを使用するには、スケジュールされたバッチ ジョブを設定します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-148">To use the *Deferred processing of manual inventory movement operation* process, set up a scheduled batch job.</span></span>

1. <span data-ttu-id="4d5c8-149">**倉庫管理 \> 定期タスク \> 倉庫アプリのイベント処理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-149">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="4d5c8-150">**倉庫アプリ イベントの処理** ダイアログ ボックスの、**バックグラウンドで実行する** クイック タブで、**バッチ処理** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-150">In the **Process warehouse app events** dialog box, on the **Run in background** FastTab, set the **Batch processing** option to *Yes*.</span></span>
1. <span data-ttu-id="4d5c8-151">**反復** を選択し、業務の要件を満たす実行スケジュールを設定します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-151">Select **Recurrence**, and set up a run schedule that meets the requirements of your business.</span></span>
1. <span data-ttu-id="4d5c8-152">それぞれのダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-152">Select **OK** in each dialog box.</span></span>

## <a name="inquire-about-the-warehouse-app-events"></a><span data-ttu-id="4d5c8-153">倉庫アプリのイベントの照会</span><span class="sxs-lookup"><span data-stu-id="4d5c8-153">Inquire about the warehouse app events</span></span>

<span data-ttu-id="4d5c8-154">倉庫アプリによって生成されたイベント キューとイベント メッセージを表示するには、**倉庫管理\>照会およびレポート\>モバイル デバイスのログ\>倉庫アプリのイベント** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-154">You can view the event queue and event messages that the warehouse app generates by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

<span data-ttu-id="4d5c8-155">*在庫移動* イベント メッセージは、初めて作成されるとき *キューに設定* の状態になります。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-155">The *Inventory movement* event messages will have a status of *Queued* when they are first created.</span></span> <span data-ttu-id="4d5c8-156">この状態は、**倉庫アプリ イベントの処理** バッチ ジョブがイベント メッセージを取得および処理することを示しています。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-156">This status indicates that the **Process warehouse app events** batch job will pick up the event messages and process them.</span></span> <span data-ttu-id="4d5c8-157">状態が *完了* に更新されると、すべての関連するイベントがキューから削除されます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-157">When the status is updated to *Completed*, all the related events are deleted from the queue.</span></span>

<span data-ttu-id="4d5c8-158">すべての *在庫移動* イベントは、イベント タイプおよび倉庫ごとに 1 つのコレクションに累計されます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-158">All the *Inventory movement* events are accumulated under one collection per event type and warehouse.</span></span>

<span data-ttu-id="4d5c8-159">バッチ ジョブは、**倉庫アプリ イベントの処理** ダイアログ ボックスで設定された反復に従って、倉庫アプリ イベントを処理します。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-159">The batch job will process the warehouse app events according to the recurrence that is set up in the **Process warehouse app events** dialog box.</span></span> <span data-ttu-id="4d5c8-160">したがって、メッセージが処理されるまで、**識別子** フィールドをクリックすることで倉庫 ID を検索できます。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-160">Therefore, until a message is processed, you can find the warehouse ID by looking in the **Identifier** field.</span></span>

<span data-ttu-id="4d5c8-161">メッセージの詳細には、移動の詳細が含まれます (「移動元」 および 「移動先」 の場所など)。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-161">The details of the message contain the details of the movement (for example, the "from" and "to" locations).</span></span>

<span data-ttu-id="4d5c8-162">詳細については、[倉庫アプリのイベント処理](warehouse-app-events.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-162">For more information, see [Warehouse app event processing](warehouse-app-events.md).</span></span>

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a><span data-ttu-id="4d5c8-163">繰延処理ポリシーをスキップするモバイル デバイス メニューの構成</span><span class="sxs-lookup"><span data-stu-id="4d5c8-163">Configure the mobile device menu to skip the deferred processing policy</span></span>

<span data-ttu-id="4d5c8-164">延期処理ポリシーをスキップするモバイル デバイス メニューを構成する方法の詳細については、[倉庫作業の繰延処理](deferred-put.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-164">For details about how to configure the mobile device menu to skip the deferred processing policy, see [Deferred processing of warehouse work](deferred-put.md).</span></span>

## <a name="impact-on-closed-work-dates"></a><span data-ttu-id="4d5c8-165">作業完了日への影響</span><span class="sxs-lookup"><span data-stu-id="4d5c8-165">Impact on closed work dates</span></span>

<span data-ttu-id="4d5c8-166">作業完了日への影響の詳細については、[倉庫作業の繰延処理](deferred-put.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d5c8-166">For details about the impact on closed work dates, see [Deferred processing of warehouse work](deferred-put.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d5c8-167">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4d5c8-167">Additional resources</span></span>

- [<span data-ttu-id="4d5c8-168">倉庫作業の繰延処理</span><span class="sxs-lookup"><span data-stu-id="4d5c8-168">Deferred processing of warehouse work</span></span>](deferred-put.md)
- [<span data-ttu-id="4d5c8-169">倉庫アプリのイベント処理</span><span class="sxs-lookup"><span data-stu-id="4d5c8-169">Warehouse app event processing</span></span>](warehouse-app-events.md)
- [<span data-ttu-id="4d5c8-170">倉庫作業用のモバイル デバイスの設定</span><span class="sxs-lookup"><span data-stu-id="4d5c8-170">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
