---
title: メンテナンス ラウンド
description: このトピックでは、資産管理におけるメンテナンス ラウンドについて説明します。
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a3a64593a2155d35e78b0d854c7367fa65d1c5c8
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018549"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="c752f-103">メンテナンス ラウンド</span><span class="sxs-lookup"><span data-stu-id="c752f-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c752f-104">**資産管理** で、定期的に同様のタスクを実行する必要があるさまざまな資産に対してメンテナンス ラウンドを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="c752f-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="c752f-105">たとえば、同じ間隔内で複数の機械に実行する必要がある潤滑ジョブまたは安全検査ジョブがあります。</span><span class="sxs-lookup"><span data-stu-id="c752f-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="c752f-106">最初のステップは、同じフォームのメンテナンス ジョブを必要とする資産を含む、メンテナンス ラウンドを作成することです。</span><span class="sxs-lookup"><span data-stu-id="c752f-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="c752f-107">次に、メンテナンス ラウンドをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="c752f-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="c752f-108">メンテナンス ラウンド スケジュールを完了すると、**すべてのメンテナンス スケジュール** および **未処理のメンテナンス スケジュール明細行** のラウンドに関連するすべてのジョブ レコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c752f-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="c752f-109">また、ラウンド ベースの作業手順書の作成時に、メンテナンス ラウンドが機能の場所にインストールされている資産上で完了するように機能の場所に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="c752f-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="c752f-110">機能の場所のメンテナンス ラウンドの設定に関する詳細については、[機能の場所の作成](../functional-locations/create-functional-locations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c752f-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="c752f-111">メンテナンス ラウンドの設定</span><span class="sxs-lookup"><span data-stu-id="c752f-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="c752f-112">**資産管理** > **設定** > **予防的メンテナンス** > **メンテナンス ラウンド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c752f-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="c752f-113">**新規** をクリックして、新しいメンテナンス レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="c752f-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="c752f-114">そして、**メンテナンス ラウンド** フィールドに「ID」、**名前** フィールドにメンテナンス ラウンドの名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="c752f-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="c752f-115">**開始日** フィールドのラウンドの開始日を選択します。</span><span class="sxs-lookup"><span data-stu-id="c752f-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="c752f-116">**日数内に完了** および **時間内に完了** フィールドで、予定終了日を日数または時間数で挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="c752f-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="c752f-117">メンテナンス スケジュール明細行が作成される時に計算される開始日に関連して、予定終了日が計算されます。</span><span class="sxs-lookup"><span data-stu-id="c752f-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="c752f-118">たとえば、**日数内に完了** フィールドに「7」を挿入することにより、関連付けられている作業が開始日から 1 週間以内に完了するように指定することができます。</span><span class="sxs-lookup"><span data-stu-id="c752f-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="c752f-119">このメンテナンス ラウンドから作成されたメンテナンス スケジュールの明細行から作業手順書を自動的に作成する場合は、**自動作成** トグル ボタンをオンにします。</span><span class="sxs-lookup"><span data-stu-id="c752f-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="c752f-120">**作業指示書タイプ** フィールドで、このメンテナンス ラウンドから作成された作業指示書で使用する作業指示書タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c752f-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="c752f-121">**サービス レベル** フィールドで、このメンテナンス ラウンドから作成された作業指示書で使用する作業指示書サービス レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c752f-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="c752f-122">**資産明細行** クイック タブで **追加** をクリックしてメンテナンス ラウンドに資産を追加します。</span><span class="sxs-lookup"><span data-stu-id="c752f-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="c752f-123">メンテナンス ラウンドの資産の順序を示すために、**行番号** フィールドに行番号が自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="c752f-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="c752f-124">**資産** フィールドで、資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="c752f-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="c752f-125">**メンテナンス作業タイプ** フィールドで、資産のメンテナンス作業タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c752f-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="c752f-126">必要に応じて、メンテナンス作業タイプに関連する **メンテナンス作業タイプ バリアント** および **取引** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c752f-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="c752f-127">**期間タイプ** フィールドで、日、週などの定期的なアイテムを選択します。</span><span class="sxs-lookup"><span data-stu-id="c752f-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="c752f-128">**期間の頻度** フィールドに、メンテナンス ラウンドを繰り返す回数を挿入します。</span><span class="sxs-lookup"><span data-stu-id="c752f-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="c752f-129">例: **期間の頻度** フィールドで「日」を選択し、このフィールドに数値「7」を挿入した場合、予防的メンテナンス スケジューリングの間、週に一回、新しいメンテナンス ラウンドの明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="c752f-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="c752f-130">**開始日** フィールドで、メンテナンス ラウンドに含められる資産の開始日を選択します。</span><span class="sxs-lookup"><span data-stu-id="c752f-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="c752f-131">この日付は、メンテナンス ラウンドで設定された開始日とは異なることがあります。</span><span class="sxs-lookup"><span data-stu-id="c752f-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="c752f-132">ステップ 9-16 を繰り返して、より多くの資産をメンテナンス ラウンドに追加します。</span><span class="sxs-lookup"><span data-stu-id="c752f-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="c752f-133">**機能の場所の明細行** クイック タブで **追加** をクリックしてメンテナンス ラウンドに機能の場所を追加します。</span><span class="sxs-lookup"><span data-stu-id="c752f-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="c752f-134">上の関連フィールドの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c752f-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="c752f-135">資産明細行の作成時に同じフィールドが使用可能ですが、必要に応じて、機能の場所の **メーカー** および **モデル** を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="c752f-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="c752f-136">明細行で機能の場所を選択するだけで、**資産タイプ**、**メーカー**、**モデル**、**メンテナンス作業タイプ**、**メンテナンス作業タイプ バリアント** および **取引** では選択されていない場合、メンテナンス スケジューリングの時点でその機能の場所に関連しているすべての資産が、メンテナンス ラウンドに含まれます。</span><span class="sxs-lookup"><span data-stu-id="c752f-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="c752f-137">**プール** クイック タブで、**追加** をクリックして、メンテナンス ラウンドに含める作業指示書プールを選択します。</span><span class="sxs-lookup"><span data-stu-id="c752f-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="c752f-138">複数の作業指示書プールを 1 つのメンテナンス サイクルに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="c752f-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="c752f-139">設定の保存。</span><span class="sxs-lookup"><span data-stu-id="c752f-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="c752f-140">**ヘッダー** クイック タブの **詳細** グループに位置する **資産** および **明細行** フィールドに、選択したメンテナンス ラウンドに関連する資産および明細行の合計数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c752f-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="c752f-141">次の図は、3 つの資産を含むメンテナンス ラウンドの例を表示します。</span><span class="sxs-lookup"><span data-stu-id="c752f-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![図 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="c752f-143">メンテナンス ラウンドのスケジュール</span><span class="sxs-lookup"><span data-stu-id="c752f-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="c752f-144">メンテナンス ラウンドを設定したら、スケジュール作業を実行して、メンテナンス ラウンドに関連するすべての作業をスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="c752f-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="c752f-145">**資産管理** > **定期処理** > **予防的メンテナンス** > **メンテナンス ラウンドのスケジュール**、**資産管理** > **共通** > **メンテナンス スケジュール** > **すべてのメンテナンス スケジュール**、**未処理のメンテナンス スケジュール明細行**、または **処理のメンテナンス スケジュール プール** > リストからメンテナンス スケジュール明細行を選択 > **メンテナンス ラウンド** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c752f-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="c752f-146">**期間** フィールドで、スケジューリング ジョブに使用する期間タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c752f-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="c752f-147">**期間の頻度** フィールドに、スケジューリング ジョブに含める期間の数を挿入します。</span><span class="sxs-lookup"><span data-stu-id="c752f-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="c752f-148">スケジューリングの開始は現在の日付です。</span><span class="sxs-lookup"><span data-stu-id="c752f-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="c752f-149">メンテナンス ラウンドに基づいて作業指示書が自動的に作成されるようにするには、**自動作成** トグル ボタンをオンにします。</span><span class="sxs-lookup"><span data-stu-id="c752f-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="c752f-150">このトグル ボタンが「オン」に設定されている場合、また、**メンテナンス ラウンド** フォームのメンテナンス ラウンドで **自動作成** トグル ボタン「オン」に設定されている場合、ワーク オーダーはメンテナンス ラウンド明細行に基づいて作成され、「ワーク オーダー作成済」ステータスのメンテナンス計画行も作成されます。</span><span class="sxs-lookup"><span data-stu-id="c752f-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="c752f-151">このドロップダウンまたは **メンテナンス ラウンド** で、**自動作成** トグル ボタンの 1 つだけが「オン」に設定されている場合、メンテナンス スケジュール明細行のみが「作成済」のステータスで作成されます。</span><span class="sxs-lookup"><span data-stu-id="c752f-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="c752f-152">その場合、ワーク オーダーは作成されません。</span><span class="sxs-lookup"><span data-stu-id="c752f-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="c752f-153">必要に応じて、スケジュール ジョブに対して特定のラウンドまたは別の開始日を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="c752f-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="c752f-154">**フィルター** をクリックし、含めるラウンドを追加します。</span><span class="sxs-lookup"><span data-stu-id="c752f-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="c752f-155">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c752f-155">Click **OK**.</span></span>

7. <span data-ttu-id="c752f-156">**資産管理** > **共通** > **メンテナンス スケジュール** > **すべてのメンテナンス スケジュール** または **未処理のメンテナンス スケジュール明細行** でメンテナンス ラウンド作業を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="c752f-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="c752f-157">スケジュールされたラウンドが作業指示書プールに関連付けられている場合は、**未処理のメンテナンス スケジュール プール** でメンテナンス スケジュールの明細行も表示されます。</span><span class="sxs-lookup"><span data-stu-id="c752f-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="c752f-158">ラウンドから作成されたメンテナンス スケジュールの明細行の参照タイプは「メンテナンス ラウンド」になります。</span><span class="sxs-lookup"><span data-stu-id="c752f-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="c752f-159">以下の 2 つの図では、**メンテナンス ラウンドのスケジュール** ダイアログのスケジュール ジョブと、そのスケジュールジョブに基ずく **全てのメンテナンス スケジュール** で作成されたメンテナンス スケジュールの明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="c752f-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![図 2](media/14-preventive-maintenance.png)

![図 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="c752f-162">仕入先保証の対象となる資産に作業指示書を手動で作成した場合、ユーザーに保証を確認するためのダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c752f-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="c752f-163">次に、作業指示書の作成をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="c752f-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="c752f-164">自動的に作成される作業指示書については、保証関係のチェックは省略されます。</span><span class="sxs-lookup"><span data-stu-id="c752f-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="c752f-165">**バックグラウンドで実行** クイック タブでバッチ ジョブを設定し、定期的にラウンドをスケジュールすることができます。</span><span class="sxs-lookup"><span data-stu-id="c752f-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="c752f-166">ラウンドが複数の作業指示書プールに含まれている場合 ([作業指示書プール](../work-orders/work-order-pools.md) を参照)、**未処理のメンテナンス スケジュール プール** の各プールに 1 つのレコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c752f-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="c752f-167">これは、作業指示書プールに対するフィルター処理オプションを最適化するために行われます。</span><span class="sxs-lookup"><span data-stu-id="c752f-167">This is done to optimize the filtering options for work order pools.</span></span>

