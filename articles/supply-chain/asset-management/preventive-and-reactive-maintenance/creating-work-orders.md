---
title: 作業指示書の作成
description: このトピックでは、資産管理で作業指示書を作成する方法について説明します。
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3982232e5008d6f8c283d6cecfaf2fa6e66150a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836737"
---
# <a name="creating-work-orders"></a><span data-ttu-id="11333-103">作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="11333-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11333-104">予防的メンテナンス ジョブをスケジュールした後の次の手順は、そのジョブの作業指示書を作成することです。</span><span class="sxs-lookup"><span data-stu-id="11333-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="11333-105">この手順は、メンテナンス スケジュールのいずれかを使用して完了できます。</span><span class="sxs-lookup"><span data-stu-id="11333-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="11333-106">メンテナンス スケジュールのスケジュールされたジョブには、次の表に示すように、異なる参照タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="11333-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="11333-107">参照タイプ</span><span class="sxs-lookup"><span data-stu-id="11333-107">Reference type</span></span> | <span data-ttu-id="11333-108">説明</span><span class="sxs-lookup"><span data-stu-id="11333-108">Description</span></span> |
|---|---|
| <span data-ttu-id="11333-109">メンテナンス計画</span><span class="sxs-lookup"><span data-stu-id="11333-109">Maintenance plans</span></span> | <span data-ttu-id="11333-110">*時間* または *カウンター* のメンテナンス計画タイプに基づく予防的メンテナンス ジョブ。</span><span class="sxs-lookup"><span data-stu-id="11333-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="11333-111">メンテナンス ラウンド</span><span class="sxs-lookup"><span data-stu-id="11333-111">Maintenance rounds</span></span> | <span data-ttu-id="11333-112">同様のタイプのメンテナンスを必要とする複数の資産を含む予防的メンテナンス ジョブ。</span><span class="sxs-lookup"><span data-stu-id="11333-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="11333-113">メンテナンス要求</span><span class="sxs-lookup"><span data-stu-id="11333-113">Maintenance request</span></span> | <span data-ttu-id="11333-114">資産のメンテナンスまたは修理のために手動で作成された要求。</span><span class="sxs-lookup"><span data-stu-id="11333-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="11333-115">この要求は作業指示書に変換できます。</span><span class="sxs-lookup"><span data-stu-id="11333-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="11333-116">メンテナンス スケジュールに基づく作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="11333-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="11333-117">メンテナンス スケジュールに基づく作業指示書を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="11333-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="11333-118">作業指示書のスケジュール項目の選択方法に応じて、次のいずれかのページを開きます:</span><span class="sxs-lookup"><span data-stu-id="11333-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="11333-119">すべてのメンテナンス スケジュール (**資産管理 \> 管理スケジュール \> すべてのメンテナンス スケジュール**)</span><span class="sxs-lookup"><span data-stu-id="11333-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="11333-120">メンテナンス スケジュール明細行を開く (**資産管理 \> 管理スケジュール \> メンテナンス スケジュール明細行を開く**)</span><span class="sxs-lookup"><span data-stu-id="11333-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="11333-121">メンテナンス スケジュール プールを開く (**資産管理 \> 管理スケジュール \> メンテナンス スケジュール プールを開く**)</span><span class="sxs-lookup"><span data-stu-id="11333-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="11333-122">グリッドで作業指示書を作成するスケジュール済みメンテナンス ジョブごとに、チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="11333-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="11333-123">アクション ペインで、**作業指示書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11333-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="11333-124">**作業指示書の作成** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="11333-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="11333-125">**メンテナンス予測時間** フィールドには、選択した明細行に対する予測時間数の合計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="11333-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![作業指示書の作成ダイアログ ボックス](media/18-preventive-maintenance.png)

1. <span data-ttu-id="11333-127">**パラメーター** セクションで、作成する作業指示書の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="11333-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="11333-128">次のオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="11333-128">Select one of the following options:</span></span>

    - <span data-ttu-id="11333-129">**明細行ごとに 1 つの作業指示書** – メンテナンス スケジュール明細行ごとに 1 つの作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="11333-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="11333-130">**1 つの作業指示書** – このオプションを選択すると使用可能になるその他のオプションの設定に従って、グループ化された作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="11333-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="11333-131">**作業指示書タイプ** フィールドで、作成したすべての作業指示書に使用する作業指示書タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="11333-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="11333-132">**OK** を選択して、設定に従って作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="11333-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="11333-133">メンテナンス計画の実行中に自動的に作成される作業指示書明細行のグループ化</span><span class="sxs-lookup"><span data-stu-id="11333-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

<span data-ttu-id="11333-134">この機能を使用すると、システムがメンテナンス計画に基づいて作業指示書が自動的に生成されるように設定されている場合に、1 つの作業指示書に作業指示書明細行をグループ化するためのルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="11333-134">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="11333-135">以前は、自動生成された作業指示書には、1 行しか含めることができませんでした。</span><span class="sxs-lookup"><span data-stu-id="11333-135">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="11333-136">ただし、作業指示書を資産、資産タイプ、または機能の場所などによってグループ化できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="11333-136">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="11333-137">(このトピックの前のセクションで説明したように、手動生成された作業指示書は、この方法で既にグループ化されている場合があります。)</span><span class="sxs-lookup"><span data-stu-id="11333-137">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="11333-138">自動生成された作業指示書のグループ化の有効化</span><span class="sxs-lookup"><span data-stu-id="11333-138">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="11333-139">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="11333-139">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="11333-140">管理者は、[機能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="11333-140">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="11333-141">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="11333-141">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="11333-142">**モジュール:** *資産管理*</span><span class="sxs-lookup"><span data-stu-id="11333-142">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="11333-143">**機能名 :** *メンテナンス計画の実行中に作業指示書をグループ化するルールの適用*</span><span class="sxs-lookup"><span data-stu-id="11333-143">**Feature name:** *Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="11333-144">自動生成された作業指示書のグループ化の設定</span><span class="sxs-lookup"><span data-stu-id="11333-144">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="11333-145">自動生成された作業指示書のグループ化を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="11333-145">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="11333-146">**資産管理 \> 設定 \> 予防的メンテナンス \> メンテナンス計画** に移動します。</span><span class="sxs-lookup"><span data-stu-id="11333-146">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="11333-147">グループ化された作業指示書を生成する計画ごとに、次の手順に従います:</span><span class="sxs-lookup"><span data-stu-id="11333-147">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="11333-148">一覧ペインで、計画を選択します。</span><span class="sxs-lookup"><span data-stu-id="11333-148">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="11333-149">**明細行** クイックタブで、すべての行で **自動作成** チェック ボックスが選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="11333-149">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="11333-150">**資産管理 \> 定期 \> 予防的メンテナンス \> メンテナンス計画のスケジュール** に移動します。</span><span class="sxs-lookup"><span data-stu-id="11333-150">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="11333-151">**メンテナンス計画のスケジュール** ダイアログ ボックスにある **期間** セクションで、計画の期間 (作業を生成するためにスケジュール済みメンテナンス ジョブを検索する際の今後の展望) を指定します。</span><span class="sxs-lookup"><span data-stu-id="11333-151">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="11333-152">**作業指示書をスケジュールから自動的に作成** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="11333-152">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="11333-153">**作業指示書** セクションで、次のいずれかのオプションを選択します:</span><span class="sxs-lookup"><span data-stu-id="11333-153">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="11333-154">**明細行ごとに 1 つの作業指示書** – メンテナンス スケジュール明細行ごとに 1 つの作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="11333-154">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="11333-155">(このオプションは、*メンテナンス計画の実行中に作業指示書をグループ化するルールの適用* 機能がオフの場合に、使用できるのと同じ機能を提供します。)</span><span class="sxs-lookup"><span data-stu-id="11333-155">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="11333-156">**1 つの作業指示書** – このオプションを選択すると使用可能になるその他のオプションの設定に従って、グループ化された作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="11333-156">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="11333-157">一部のメンテナンス計画の実行時にのみオプションを適用する場合は、**対象に含めるレコード** クイックタブで Microsoft Dynamics 365 Supply Chain Management の他のバッチ ジョブと同様に、必要に応じてフィルターを追加します。</span><span class="sxs-lookup"><span data-stu-id="11333-157">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="11333-158">**バックグラウンドで実行** クイックタブで、Supply Chain Management の他のバッチ ジョブと同様に、必要に応じてバッチとスケジューリング オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="11333-158">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="11333-159">**OK** を選択して、選択したメンテナンス計画を実行および/またはスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="11333-159">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]