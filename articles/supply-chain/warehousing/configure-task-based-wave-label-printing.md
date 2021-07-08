---
title: ウェーブ中にウェーブ ラベルの印刷をスケジュールする
description: このトピックでは、タスク ベースのウェーブ ラベル印刷用の機能を設定および使用する方法について説明します。
author: MSFTGarm
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-obaranov
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 32842c32599b3ca5d84cc9f715a1453d55e176dc
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301889"
---
# <a name="schedule-wave-label-printing-during-wave"></a><span data-ttu-id="859df-103">ウェーブ中にウェーブ ラベルの印刷をスケジュールする</span><span class="sxs-lookup"><span data-stu-id="859df-103">Schedule wave label printing during wave</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="859df-104">ウェーブ プロセスの一部として *ウェーブ ラベル印刷に基づくタスク* 機能を使用すると効率が向上、また、ウェーブ ラベルを作成するシステムと個別作業を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="859df-104">Use the *Task based wave label printing* feature as part of your waving process to help improve efficiency, and to have the system create wave labels and work in separate tasks.</span></span>

<span data-ttu-id="859df-105">ウェーブ ラベルの印刷を構成するプロセスは複雑で、正確なコンフィギュレーションとマスター データに依存します。</span><span class="sxs-lookup"><span data-stu-id="859df-105">The process of configuring wave label printing is complex and relies on accurate configuration and master data.</span></span> <span data-ttu-id="859df-106">これは、複数のウェーブ レコードの生成が失敗することは珍しくなく、失敗した場合でも、ウェーブ処理の全体がロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="859df-106">It isn't uncommon for the generation of wave label records to fail, and when it does, the whole wave processing is rolled back.</span></span> <span data-ttu-id="859df-107">*ウェーブ ラベル印刷に基づくタスク* 機能を使用すると、ウェーブ ラベルを誤って印刷するたびに作業と作業明細行を再作成する必要が無いようにします。</span><span class="sxs-lookup"><span data-stu-id="859df-107">The *Task based wave label printing* feature helps you avoid having to re-create work and work lines every time that a wave label is incorrectly printed.</span></span>

<span data-ttu-id="859df-108">*ウェーブ ラベルの印刷に基づくタスク* 機能を使うと、システムは最初に作業と作業明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="859df-108">When you use the *Task based wave label printing* feature, the system first creates work and work lines.</span></span> <span data-ttu-id="859df-109">次に、ウェーブ ラベルを作成して印刷します。</span><span class="sxs-lookup"><span data-stu-id="859df-109">It then creates and prints wave labels.</span></span> <span data-ttu-id="859df-110">最後に、ウェーブ ラベルが正しく作成された場合は、ピッキング用の作業とウェーブがリリースされます。</span><span class="sxs-lookup"><span data-stu-id="859df-110">Finally, if the wave labels are correctly created, it releases the work and wave for picking.</span></span>

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a><span data-ttu-id="859df-111">機能管理でのタスク ベースのウェーブ ラベル印刷機能の有効</span><span class="sxs-lookup"><span data-stu-id="859df-111">Turn on the Task based wave label printing feature in feature management</span></span>

<span data-ttu-id="859df-112">このトピックで説明する機能を使用するには、システムで機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="859df-112">To use the features that are described in this topic, they must be turned on for your system.</span></span> <span data-ttu-id="859df-113">[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ワークスペースを使用して、機能を次に示す順番で有効にします。</span><span class="sxs-lookup"><span data-stu-id="859df-113">Use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to turn on the features in the following order:</span></span>

1. <span data-ttu-id="859df-114">*ウェーブ ラベルの印刷* – この機能では、ウェーブ ラベルの印刷に対して、ラベルの印刷を簡単に行う方法を有効にする場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="859df-114">*Wave label printing* – This feature is required to enable the wave process method for wave label printing.</span></span>
1. <span data-ttu-id="859df-115">*組織全体の作業のブロック* - この機能ではスケジュールされた作業作成の手動と自動の両方の構成に必要です。</span><span class="sxs-lookup"><span data-stu-id="859df-115">*Organization-wide work blocking* – This feature is required for both manual and automatic configuration of scheduled work creation.</span></span>
1. <span data-ttu-id="859df-116">*ウェーブ ラベル印刷に基づくタスク* – この機能は、ウェーブ ラベルの印刷を別のトランザクション スコープに分割する必要があります。</span><span class="sxs-lookup"><span data-stu-id="859df-116">*Task based wave label printing* – This feature is required to split off wave label printing to a separate transaction scope.</span></span>

## <a name="manually-enable-the-new-wave-step-method"></a><span data-ttu-id="859df-117">新しいウェーブ ステップの方法を手動で有効にする</span><span class="sxs-lookup"><span data-stu-id="859df-117">Manually enable the new wave step method</span></span>

<span data-ttu-id="859df-118">最初に、新しいウェーブ ステップ メソッドを作成し、並列、非同期タスク処理を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="859df-118">You must first create the new wave step method and enable it for parallel, asynchronous task processing.</span></span>

1. <span data-ttu-id="859df-119"> *\*倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。</span><span class="sxs-lookup"><span data-stu-id="859df-119">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="859df-120">アクション ウィンドウで、**再生成の方法** を選択します。</span><span class="sxs-lookup"><span data-stu-id="859df-120">On the Action Pane, select **Regenerate method**.</span></span> <span data-ttu-id="859df-121">*waveLabelPrinting* は、出荷ウェーブ テンプレートで使用できるウェーブ プロセス方法の一覧に追加されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="859df-121">Notice that *waveLabelPrinting* is added to the list of wave process methods that you can use in your shipping wave templates.</span></span>
1. <span data-ttu-id="859df-122">**メソッド名** フィールドが *waveLabelPrinting* に設定されているレコードを選び、アクション ウィンドウで **タスク コンフィグレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="859df-122">Select the record where the **Method name** field is set to *waveLabelPrinting*, and then, on the Action Pane, select **Task configuration**.</span></span>
1. <span data-ttu-id="859df-123">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="859df-123">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="859df-124">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="859df-124">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="859df-125">**倉庫** – 作業作成処理をスケジュールするために使用する倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="859df-125">**Warehouse** – Select the warehouse that you will use to schedule work creation processing.</span></span> <span data-ttu-id="859df-126">(デモ データをテスト目的で使用している場合は、倉庫 *24* を選択できます。)</span><span class="sxs-lookup"><span data-stu-id="859df-126">(If you're using demo data for testing purposes, you can select warehouse *24*.)</span></span>
    - <span data-ttu-id="859df-127">**バッチ タスクの最大数** – バッチ タスクの最大数を指定します。</span><span class="sxs-lookup"><span data-stu-id="859df-127">**Maximum number of batch tasks** – Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="859df-128">ほとんどの場合、値は *8* から *16* です。</span><span class="sxs-lookup"><span data-stu-id="859df-128">In most cases, the value should be from *8* through *16*.</span></span> <span data-ttu-id="859df-129">ただし、最適な設定を試して、使用するシナリオを探すことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="859df-129">However, we recommend that you experiment to find the optimal setting for your scenarios.</span></span>
    - <span data-ttu-id="859df-130">**ウェーブを処理するバッチ グループ** – 専用のウェーブを処理するバッチ グループを選択して、バッチ キュー処理を最適化します。</span><span class="sxs-lookup"><span data-stu-id="859df-130">**Wave processing batch group** – Select a dedicated wave processing batch group to optimize batch queue processing.</span></span>

<span data-ttu-id="859df-131">*ウェーブ ラベル印刷* ウェーブ処理方法を使用するように、既存のウェーブ テンプレートを更新します。</span><span class="sxs-lookup"><span data-stu-id="859df-131">You can now update an existing wave template so that it uses the *Wave label printing* wave processing method.</span></span> <span data-ttu-id="859df-132">または、それを使用する新しいウェーブ テンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="859df-132">Alternatively, you can create a new wave template that uses it.</span></span>

1. <span data-ttu-id="859df-133"> *\*倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="859df-133">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="859df-134">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="859df-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="859df-135">リスト ウィンドウで、ウェーブ テンプレートを選択して更新します。</span><span class="sxs-lookup"><span data-stu-id="859df-135">In the list pane, select the wave template to update.</span></span> <span data-ttu-id="859df-136">(デモ データをテスト目的で使用している場合は、*24 出荷の既定* を選択できます。)</span><span class="sxs-lookup"><span data-stu-id="859df-136">(If you're using demo data for testing purposes, you can select *24 Shipping default*.)</span></span>
1. <span data-ttu-id="859df-137">**メソッド** クイックタブの **残りのメソッド** 列で、**名前** フィールドが *waveLabelPrinting* に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="859df-137">On the **Methods** FastTab, in the **Remaining methods** column, select the row where the **Name** field is set to *waveLabelPrinting*.</span></span>
1. <span data-ttu-id="859df-138">**追加** (右矢印ボタン) を選び、選択した行を **選択したメソッド** 行へ移動します。</span><span class="sxs-lookup"><span data-stu-id="859df-138">Select **add** (right arrow button) to move the selected row to the **Selected methods** column.</span></span>
1. <span data-ttu-id="859df-139">**ウェーブ ステップ コード** フィールドで、ウェーブ ラベル テンプレートとウェーブ テンプレートを接続するために使われるウェーブ ステップ コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="859df-139">In the **Wave step code** field, enter a wave step code that will be used to connect the wave template with a wave label template.</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="859df-140">ウェーブ タスク処理のしきい値データの設定</span><span class="sxs-lookup"><span data-stu-id="859df-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="859df-141">タスク ベースの処理を使用してウェーブ プロセスを初めて実行する際、システムは既定のウェーブ タスク処理のしきい値データを作成します。</span><span class="sxs-lookup"><span data-stu-id="859df-141">The first time that a wave process runs by using any task-based processing, the system creates default wave task processing threshold data.</span></span> <span data-ttu-id="859df-142">このデータは、ウェーブ処理が非同期に実行されタスク ベース化されるかどうかを制御するために使用され、これによりウェーブ ラベルを並行して処理および作成できます。</span><span class="sxs-lookup"><span data-stu-id="859df-142">This data is used to control whether wave processing will run asynchronously and be task-based, so that it can process and create wave labels in parallel.</span></span>

<span data-ttu-id="859df-143">既定データでは、最初に作業 ID の最小数に対して、しきい値 *1* が使用されます (`MinimumWorkThresholdForLabelPrinting`)。</span><span class="sxs-lookup"><span data-stu-id="859df-143">The default data initially uses a threshold value of *1* for the minimum number of work IDs (`MinimumWorkThresholdForLabelPrinting`).</span></span> <span data-ttu-id="859df-144">したがって、システムで複数の作業 ID を処理する場合、別のトランザクションでウェーブ ラベルのタスク ベース処理は使用されます。</span><span class="sxs-lookup"><span data-stu-id="859df-144">Therefore, when the system processes a wave that has more than one work ID, it will use task-based processing of wave labels in a separate transaction.</span></span> <span data-ttu-id="859df-145">テスト環境では、このデータを `WHSWaveTaskProcessingThresholdParameters` テーブルに手動で挿入または更新することができます。</span><span class="sxs-lookup"><span data-stu-id="859df-145">You can manually insert or update this data in the `WHSWaveTaskProcessingThresholdParameters` table in your test environments.</span></span> <span data-ttu-id="859df-146">運用環境で設定を変更するためには、Microsoft サポートに連絡してアップデートを依頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="859df-146">To change the setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a><span data-ttu-id="859df-147">タスクベースのウェーブ ラベル印刷を使用する場合のウェーブ処理ロジックの変更</span><span class="sxs-lookup"><span data-stu-id="859df-147">Changes to the wave processing logic when task-based wave label printing is used</span></span>

<span data-ttu-id="859df-148">ウェーブ ラベルの処理が開始される前の作業処理のしきい値を超えた場合は、タスク ベースの処理が開始されます。</span><span class="sxs-lookup"><span data-stu-id="859df-148">If the wave label processing exceeds the wave task processing threshold, task-based processing is initiated.</span></span> <span data-ttu-id="859df-149">ウェーブ テンプレートが適合する次のウェーブ処理では、ウェーブ ラベル印刷は作業作成後すぐにスタンドアロン *ttsbegin*/*ttscommit* トランザクションで実行されます。</span><span class="sxs-lookup"><span data-stu-id="859df-149">In the next wave processing that fits the wave template, wave label printing will run in a standalone *ttsbegin*/*ttscommit* transaction immediately after work creation.</span></span> <span data-ttu-id="859df-150">作業リリース (ブロックの解除) が自動的に実行するようにウェーブ テンプレートに対して構成されている場合、ウェーブ ラベル印刷のプロセスが正常に完了した後にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="859df-150">If work release (unblocking) is configured on the wave template to run automatically, it occurs only after the wave label printing process is successfully completed.</span></span>

<span data-ttu-id="859df-151">ウェーブ ラベル生成が失敗した場合 (たとえば、ウェーブ ラべル数量への作業数量の変換に失敗しエラーが発生した場合)、該当するトランザクションだけが失敗します。</span><span class="sxs-lookup"><span data-stu-id="859df-151">If wave label generation fails (for example, if conversion of the work quantity to the wave label quantity fails and throws an error), only the appropriate transaction fails.</span></span> <span data-ttu-id="859df-152">以前に作成された作業は凍結されたままです。</span><span class="sxs-lookup"><span data-stu-id="859df-152">The work that was previously created remains frozen.</span></span> <span data-ttu-id="859df-153">エラーを修正し、ウェーブ ラベルを印刷するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="859df-153">To correct errors and print the wave labels, follow these steps.</span></span>

1. <span data-ttu-id="859df-154">**倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="859df-154">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="859df-155">グリッドで関連ウェーブを選択します。</span><span class="sxs-lookup"><span data-stu-id="859df-155">Select the relevant wave in the grid.</span></span>
1. <span data-ttu-id="859df-156">アクション ペインにある **ウェーブ** タブの **印刷** グループで、**ウェーブ ラベル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="859df-156">On the Action Pane, on the **Wave** tab, in the **Print** group, select **Wave labels**.</span></span>
1. <span data-ttu-id="859df-157">画面に表示された指示に従って、印刷用のラベルを送信します。</span><span class="sxs-lookup"><span data-stu-id="859df-157">Follow the on-screen instructions to send the labels for printing.</span></span>
1. <span data-ttu-id="859df-158">アクション ウィンドウでの **ウェーブ** グループの **ウェーブ** タブで、**リリース** を選択し、手動で選択したウェーブの作業をリリースします。</span><span class="sxs-lookup"><span data-stu-id="859df-158">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Release** to manually release the work for the selected wave.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="859df-159">追加リソース</span><span class="sxs-lookup"><span data-stu-id="859df-159">Additional resources</span></span>

- [<span data-ttu-id="859df-160">ウェーブ ラベルの印刷</span><span class="sxs-lookup"><span data-stu-id="859df-160">Wave label printing</span></span>](configure-wave-label-printing.md)
- [<span data-ttu-id="859df-161">ウェーブ中の作業作成のスケジュール</span><span class="sxs-lookup"><span data-stu-id="859df-161">Schedule work creation during wave</span></span>](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
