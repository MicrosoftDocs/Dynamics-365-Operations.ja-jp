---
title: 在庫トランザクションをアーカイブする
description: このトピックでは、システムのパフォーマンスを向上させるために在庫トランザクション データをアーカイブする方法について説明します。
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: bacc27c1a9066892c51110d28ba9a2ad26bebe77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839298"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="67dfb-103">在庫トランザクションをアーカイブする</span><span class="sxs-lookup"><span data-stu-id="67dfb-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="67dfb-104">時間の経過と共に、在庫トランザクション テーブル (`InventTrans`) は拡大し、データベース容量を消費します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="67dfb-105">したがって、テーブルに対して実行されるクエリの速度は徐々に低下します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="67dfb-106">このトピックでは、システム パフォーマンスを向上させるために、*在庫トランザクション アーカイブ* 機能を使用して在庫トランザクションに関するデータをアーカイブする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="67dfb-107">選択した決算済元帳期間にアーカイブできるのは、財務更新済の在庫トランザクションのみです。</span><span class="sxs-lookup"><span data-stu-id="67dfb-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="67dfb-108">アーカイブするには、財務更新済の出荷在庫トランザクションの払出ステータスが *売却済* で、入庫在庫トランザクションの受入ステータスが *購買済* である必要があります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="67dfb-109">在庫トランザクションをアーカイブすると、関連のすべてのトランザクションが `InventTransArchive` テーブルに移動されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="67dfb-110">在庫払出トランザクションと在庫受入トランザクションは、品目ID (`itemId`) と在庫分析コード ID (`inventDimId`) の組み合わせに基づいて個別にアーカイブされ、集計された払出トランザクションと受入トランザクションに転記されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="67dfb-111">`itemId` と `inventDimId` の組み合わせに払出トランザクションまたは受入トランザクションが 1 つだけ含まれている場合、トランザクションはアーカイブされません。</span><span class="sxs-lookup"><span data-stu-id="67dfb-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="67dfb-112">システムで機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="67dfb-112">Turn on the feature in your system</span></span>

<span data-ttu-id="67dfb-113">このトピックで説明する機能がシステムにまだ含まれていない場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、*在庫トランザクション アーカイブ* 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="67dfb-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="67dfb-114">在庫トランザクションをアーカイブする前に考慮する点</span><span class="sxs-lookup"><span data-stu-id="67dfb-114">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="67dfb-115">在庫トランザクションをアーカイブする前に、次の業務シナリオを考慮する必要があります。これらは操作の影響を受けるためです。</span><span class="sxs-lookup"><span data-stu-id="67dfb-115">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="67dfb-116">発注書明細行などの関連ドキュメントから在庫トランザクションを監査する場合、在庫トランザクションはアーカイブ済として表示されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-116">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="67dfb-117">アーカイブされたトランザクションを確認するには、**在庫管理 \> 定期処理タスク \> クリーンアップ \> 在庫トランザクション アーカイブ** の順に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-117">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="67dfb-118">アーカイブされた期間の在庫決算はキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-118">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="67dfb-119">在庫決算をキャンセルするには、まず関連する期間の在庫トランザクション アーカイブを取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-119">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="67dfb-120">アーカイブされた期間に対して標準原価換算は行えません。</span><span class="sxs-lookup"><span data-stu-id="67dfb-120">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="67dfb-121">標準原価換算を行うには、まず関連する期間の在庫トランザクション アーカイブを取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-121">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="67dfb-122">在庫トランザクションをアーカイブすると、在庫トランザクションから取得された在庫レポートが影響を受ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-122">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="67dfb-123">これらのレポートには、在庫エイジング レポートおよび在庫金額レポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-123">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="67dfb-124">在庫予測は、アーカイブされた期間の期間中に実行されると影響を受ける場合があります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-124">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="67dfb-125">必要条件</span><span class="sxs-lookup"><span data-stu-id="67dfb-125">Prerequisites</span></span>

<span data-ttu-id="67dfb-126">在庫トランザクションは、次の条件が満たされた期間にのみアーカイブできます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-126">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="67dfb-127">元帳期間は決済されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-127">The ledger period must be closed.</span></span>
- <span data-ttu-id="67dfb-128">在庫決算は、アーカイブの終了日以降に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-128">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="67dfb-129">期間は、アーカイブの開始日の 1 年以上前の日付である必要があります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-129">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="67dfb-130">既存の在庫再計算が作成されていない必要があります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-130">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="67dfb-131">在庫トランザクションをアーカイブする</span><span class="sxs-lookup"><span data-stu-id="67dfb-131">Archive inventory transactions</span></span>

<span data-ttu-id="67dfb-132">在庫トランザクションをアーカイブするには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="67dfb-132">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="67dfb-133">**在庫管理** \> **定期処理タスク** \> **クリーンアップ** \> **在庫トランザクション アーカイブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-133">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="67dfb-134">**在庫トランザクション アーカイブ** ページが表示され、アーカイブされているプロセス レコードの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-134">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="67dfb-135">![在庫トランザクション アーカイブ ページ](media/archive-inventory-empty.png "在庫トランザクション アーカイブ ページ")</span><span class="sxs-lookup"><span data-stu-id="67dfb-135">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="67dfb-136">アクション ウィンドウで、**在庫トランザクション アーカイブ** を選択して、在庫トランザクション アーカイブを作成します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-136">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="67dfb-137">**在庫トランザクション アーカイブ** ダイアログ ボックスの **パラメーター** クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-137">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="67dfb-138">**元帳の決算済期間の開始日** – アーカイブに含める最も早いトランザクションの日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-138">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="67dfb-139">**元帳の決算済期間の終了日** – アーカイブに含める最も遅いトランザクションの日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-139">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="67dfb-140">![在庫トランザクション ダイアログ ボックス](media/archive-inventory-dates.png "在庫トランザクション ダイアログ ボックス")</span><span class="sxs-lookup"><span data-stu-id="67dfb-140">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="67dfb-141">[前提条件](#prerequisites) を満たす期間のみを選択できます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-141">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="67dfb-142">**バックグラウンドで実行** クイック タブで、必要に応じてバッチ処理の詳細を設定します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-142">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="67dfb-143">Microsoft Dynamics 365 Supply Chain Management のバッチ ジョブの通常の手順に従います 。</span><span class="sxs-lookup"><span data-stu-id="67dfb-143">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="67dfb-144">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-144">Select **OK**.</span></span>
1. <span data-ttu-id="67dfb-145">続行を確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-145">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="67dfb-146">メッセージを慎重に読み、続行する場合は **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-146">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="67dfb-147">在庫トランザクション アーカイブ ジョブがバッチ キューに追加されたというメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-147">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="67dfb-148">選択した期間の在庫トランザクションのアーカイブがジョブによって開始されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-148">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="67dfb-149">アーカイブされた在庫トランザクションの表示</span><span class="sxs-lookup"><span data-stu-id="67dfb-149">View archived inventory transactions</span></span>

<span data-ttu-id="67dfb-150">**在庫トランザクション アーカイブ** ページには、完全なアーカイブ履歴が表示されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-150">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="67dfb-151">グリッドの各行には、アーカイブが作成された日付、作成したユーザー、ステータスなどの情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-151">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="67dfb-152">![在庫トランザクション アーカイブの履歴をアーカイブする](media/archive-inventory-full.png "在庫トランザクション アーカイブの履歴をアーカイブする")</span><span class="sxs-lookup"><span data-stu-id="67dfb-152">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="67dfb-153">ページの上部にあるドロップダウン リストで、次のいずれかの値を選択して、グリッドに表示されるアーカイブをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-153">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="67dfb-154">**有効** – 有効なアーカイブのみ表示し、取り消されたアーカイブは表示しません。</span><span class="sxs-lookup"><span data-stu-id="67dfb-154">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="67dfb-155">**すべて** – 有効なアーカイブと取り消されたアーカイブの両方を表示します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-155">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="67dfb-156">グリッド内のアーカイブごとに、次の情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-156">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="67dfb-157">**有効** – チェック マークは、アーカイブが有効かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-157">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="67dfb-158">**開始日** – アーカイブに含まれる最も古いトランザクションの日付。</span><span class="sxs-lookup"><span data-stu-id="67dfb-158">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="67dfb-159">**終了日** – アーカイブに含まれる最も新しいトランザクションの日付。</span><span class="sxs-lookup"><span data-stu-id="67dfb-159">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="67dfb-160">**スケジュール作成者** – アーカイブを作成したユーザー アカウント。</span><span class="sxs-lookup"><span data-stu-id="67dfb-160">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="67dfb-161">**実行日** – アーカイブが作成された日時。</span><span class="sxs-lookup"><span data-stu-id="67dfb-161">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="67dfb-162">**取り消し** – チェック マークは、アーカイブが取り消し済かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-162">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="67dfb-163">**現在の更新の停止** – チェック マークは、アーカイブが進行中で、一時停止中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-163">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="67dfb-164">**状態** – アーカイブの処理ステータス。</span><span class="sxs-lookup"><span data-stu-id="67dfb-164">**State** – The processing status of the archive.</span></span> <span data-ttu-id="67dfb-165">このフィールドの値は、*待機中*、*進行中*、および *完了済* です。</span><span class="sxs-lookup"><span data-stu-id="67dfb-165">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="67dfb-166">グリッドの上にあるツール バーには、選択したアーカイブを操作する場合に使用できる次のボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-166">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="67dfb-167">**アーカイブされたトランザクション** – 選択したアーカイブの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-167">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="67dfb-168">**アーカイブされたトランザクション** ページには、アーカイブ内のすべてのトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-168">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="67dfb-169">![アーカイブされたトランザクション ページ](media/archive-inventory-transactions.png "アーカイブされたトランザクション ページ")</span><span class="sxs-lookup"><span data-stu-id="67dfb-169">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="67dfb-170">**アーカイブされたトランザクション** ページで特定のトランザクションに関する詳細情報を表示するには、グリッドで特定のトランザクションを選択し、アクション ウィンドウで **アーカイブされたトランザクションの詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-170">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="67dfb-171">表示される **アーカイブされたトランザクションの詳細** ページには、元帳転記、関連する補助元帳参照、財務分析コードなどの情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-171">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="67dfb-172">**アーカイブの一時停止** – 現在処理されている選択したアーカイブを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-172">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="67dfb-173">一時停止は、アーカイブ タスクが生成された後にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-173">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="67dfb-174">そのため、一時停止が有効になる前に、短い遅延が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="67dfb-174">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="67dfb-175">アーカイブが一時停止されている場合は、**現在の更新の停止** フィールドにチェック マークが表示されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-175">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="67dfb-176">**アーカイブの再開** – 現在一時停止されている選択したアーカイブを再開します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-176">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="67dfb-177">**取り消し** – 選択したアーカイブを取り消します。</span><span class="sxs-lookup"><span data-stu-id="67dfb-177">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="67dfb-178">アーカイブを取り消しできるのは、アーカイブの **状態** フィールドが *完了* に設定されている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="67dfb-178">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="67dfb-179">アーカイブが取り消されている場合は、**取り消し** フィールドにチェック マークが表示されます。</span><span class="sxs-lookup"><span data-stu-id="67dfb-179">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
