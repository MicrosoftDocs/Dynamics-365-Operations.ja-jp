---
title: メンテナンス ダウンタイム
description: このトピックでは、資産管理におけるメンテナンス ダウンタイムについて説明します。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a831d56116c57b640993162473e74e5ce181f09c
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875747"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="3edc1-103">メンテナンス ダウンタイム</span><span class="sxs-lookup"><span data-stu-id="3edc1-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3edc1-104">メンテナンス ダウンタイムは、特定の期間、特定の資産に対してメンテナンス ジョブを実行するために必要な能力の概要を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-104">Maintenance downtime is used to get an overview of the capacity required to carry out maintenance jobs on specific assets during a specific period.</span></span> <span data-ttu-id="3edc1-105">たとえば、生産サイト 02 の生産 Hall 29-A の生産ライン 10 に対して、メンテナンス ダウンタイム登録を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-105">For example, you can create a maintenance downtime registration for Production line 10 in Production Hall 29-A on production site 02.</span></span> <span data-ttu-id="3edc1-106">メンテナンス ダウンタイムの登録には、メンテナンスによる停止に関係する資産が生産を行えなくなる期間を示す開始時刻と終了時刻が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-106">The maintenance downtime registration has a start and end time indicating the period in which the assets related to the maintenance stop are not available for production.</span></span>

<span data-ttu-id="3edc1-107">**メンテナンス ダウンタイム アクティビティ**は、指定された期間における関連資産のメンテナンス スケジュール明細行と作業指示書のメンテナンス作業の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-107">**Maintenance downtime activities** is an overview of maintenance schedule lines and work order maintenance jobs on related assets during a specified period.</span></span> <span data-ttu-id="3edc1-108">作業指示書のメンテナンス作業に関連する明細行すべてには、メンテナンスによる停止期間内の開始予定日が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-108">The lines related to work order maintenance jobs all have an expected start date within the maintenance stop period.</span></span> <span data-ttu-id="3edc1-109">有用な情報を抽出し、計画されたメンテナンス作業を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-109">You can extract useful information and make adjustments to planned maintenance jobs:</span></span>

- <span data-ttu-id="3edc1-110">生産施設 (資産) に必要なシャットダウン期間の概要を取得します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-110">Get an overview of required shut-down periods of production equipment (assets).</span></span>  
- <span data-ttu-id="3edc1-111">電気技師 Smith の能力負荷、また、計画されたメンテナンス作業を実行するのに必要な他のメンテナンス作業者グループのような、コンピテンシー (担当メンテナンス作業者グループまたはメンテナンス作業者) によりグループ化され、計画されているメンテナンス (時間) の概要を取得します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-111">Get an overview of planned maintenance (hours), grouped by competencies (responsible maintenance worker groups or maintenance workers), for example capacity load on electricians, smiths, or other maintenance work groups required to do the planned maintenance jobs.</span></span>  
- <span data-ttu-id="3edc1-112">明細行の開始予定時刻および終了予定時刻を変更したり、または他のメンテナンス作業者を選択してメンテナンス作業者およびメンテナンス作業者グループのワークフローを最適化するなど、資産に関連したメンテナンス スケジュールの明細行、またはメンテナンス作業に対して調整を行います。</span><span class="sxs-lookup"><span data-stu-id="3edc1-112">Make adjustments to maintenance schedule lines or work order maintenance jobs related to the assets, for example, change expected start and end times on a line, or select other maintenance workers to optimize the workflow for maintenance workers and maintenance worker groups.</span></span>

<span data-ttu-id="3edc1-113">メンテナンス ダウンタイムの登録時に資産が選択されている場合、有効な作業指示書に関連するすべての未処理のメンテナンス スケジュール明細行と作業指示書のメンテナンス作業がメンテナンス ダウンタイムの登録に含められます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-113">When assets have been selected on a maintenance downtime registration, all open maintenance schedule lines and work order maintenance jobs relating to active work orders are included in the maintenance downtime registration.</span></span>

## <a name="maintenance-downtime-activities"></a><span data-ttu-id="3edc1-114">メンテナンス ダウンタイム活動</span><span class="sxs-lookup"><span data-stu-id="3edc1-114">Maintenance downtime activities</span></span>

<span data-ttu-id="3edc1-115">**資産管理** > **共通** > **メンテナンス ダウンタイム アクティビティ** > **すべてのメンテナンス ダウンタイム アクティビティ**をクリックして、すべてのすべてのメンテナンス ダウンタイム アクティビティのリストを開き、アクティビティに関連した情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-115">Click **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** to open a list of all maintenance downtime activities and see some of the information related to the activities.</span></span> <span data-ttu-id="3edc1-116">**メンテナンス ダウンタイム アクティビティ**列のリンクをクリックして、詳細表示を開きます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-116">Click on a link in the **Maintenance downtime activities** column to open the details view.</span></span>

![図 1](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-registration"></a><span data-ttu-id="3edc1-118">メンテナンス ダウンタイムの登録の作成</span><span class="sxs-lookup"><span data-stu-id="3edc1-118">Create a maintenance downtime registration</span></span>

1. <span data-ttu-id="3edc1-119">**資産管理** > **共通** > **メンテナンス ダウンタイム アクティビティ** > **すべてのメンテナンス ダウンタイム アクティビティ**または**効なメンテナンス ダウンタイム アクティビティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3edc1-119">Click **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** or **Active maintenance downtime activities**.</span></span>

2. <span data-ttu-id="3edc1-120">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3edc1-120">Click **New**.</span></span>

3. <span data-ttu-id="3edc1-121">**メンテナンス ダウンタイム アクティビティ** フィールドに ID を挿入し、**名前**フィールドに名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-121">Insert an ID in the **Maintenance downtime activities** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="3edc1-122">メンテナンス停止の期間を**開始日時**および**終了日時**フィールドに挿入します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-122">Insert the period for the maintenance stop in the **Start date/time** and **End date/time** fields.</span></span>

5. <span data-ttu-id="3edc1-123">**メンテナンス ダウンタイム アクティビティ資産** クイック タブ > で**明細行の追加**をクリックし、一度に一つずつ、メンテナンス ダウンタイム アクティビティに資産を追加します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-123">On the **Maintenance downtime activities assets** FastTab> click **Add line** to add assets, one at a time, to the maintenance downtime activity.</span></span>

6. <span data-ttu-id="3edc1-124">すべての資産が追加されたら、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3edc1-124">Click **Save** when all assets have been added.</span></span>

7. <span data-ttu-id="3edc1-125">選択した資産に関連する作業指示書のメンテナンス作業および未処理のメンテナンス スケジュール明細行が、**結果としての作業指示書のメンテナンス作業**および**メンテナンス スケジュール明細行**クイック タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-125">The work order maintenance jobs and open maintenance schedule lines related to the selected assets are shown on the **Resulting work order maintenance jobs** and **Maintenance schedule lines** FastTabs.</span></span> <span data-ttu-id="3edc1-126">**一般**クイック タブ > **作業指示書**グループ > **メンテナンス予測時間**フィールドおよび**一般**クイック タブ > **メンテナンス スケジュール** グループ > **メンテナンス予測時間**フィールドに、作業指示書のメンテナンス作業およびメンテナンス スケジュール明細行に対して予測される時間の合計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-126">On the **General** FastTab > **Work orders** group > **Maintenance forecast hours** field and **General** FastTab > **Maintenance schedule** group > **Maintenance forecast hours** field , you see the total number of hours forecasted for work order maintenance jobs and maintenance schedule lines.</span></span>

![図 2](media/20-preventive-maintenance.png)

>[!NOTE]
><span data-ttu-id="3edc1-128">選択した資産に関連する作業指示書メンテナンス ジョブおよびメンテナンス スケジュール明細行は、メンテナンス ダウンタイム アクティビティを作成した後に新しい作業指示書または明細行が作成された場合に、自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-128">The work order maintenance jobs and maintenance schedule lines related to the selected assets are automatically updated if new work orders or maintenance schedule lines are created after you created the maintenance downtime activity.</span></span> <span data-ttu-id="3edc1-129">たとえば、関連する資産のメンテナンス計画またはメンテナンス ラウンドを、メンテナンス ダウンタイム アクティビティが作成された 2 日後にスケジュールした場合、メンテナンス ダウンタイム アクティビティに新しいメンテナンス スケジュールの明細行が自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-129">For example, if you schedule maintenance plans or maintenance rounds on the related assets two days after the maintenance downtime activity was created, new maintenance schedule lines are automatically added to the maintenance downtime activity.</span></span>

8. <span data-ttu-id="3edc1-130">**すべてのメンテナンス ダウンタイム アクティビティ** > **メンテナンス ダウンタイム アクティビティ** > のリストからメンテナンス ダウンタイム アクティビティを選択し、**最大能力負荷**をクリックして**最大能力負荷の計算**ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-130">In **All maintenance downtime activities** > **Maintenance downtime activities** > select a mainteance downtime activity in the list and click **Capacity load** to open the **Calculate capacity load** dialog.</span></span> <span data-ttu-id="3edc1-131">このダイアログを使用して、日付、資産、資産タイプ、およびメンテナンス作業タイプなどの最大能力負荷の概要を取得します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-131">Use this dialog to get an overview of capacity load on, for example, dates, assets, asset types, and maintenance job types.</span></span> <span data-ttu-id="3edc1-132">ダイアログに表示されている日付は、**メンテナンス ダウンタイム アクティビティ**で選択された開始日と終了日です。</span><span class="sxs-lookup"><span data-stu-id="3edc1-132">Note that the dates shown in the dialog are the start and end dates selected in **Maintenance downtime activities**.</span></span> <span data-ttu-id="3edc1-133">この計算には、メンテナンス ダウンタイム アクティビティに関連する資産が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3edc1-133">This calculation includes the assets related to the maintenance downtime activity.</span></span>

9. <span data-ttu-id="3edc1-134">必要に応じて**最大能力負荷の計算**ダイアログで開始時刻と終了時刻を編集し、作業指示書とメンテナンス スケジュールを計算に含めるかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-134">In the **Calculate capacity load** dialog, edit start and end times if required, and select if you want to include work orders and maintenance schedules in the calculation.</span></span> <span data-ttu-id="3edc1-135">**レベル** フィールドを使用すると、機能的な場所に関する最大能力負荷の計算の詳細度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-135">You can use the **Level** field to indicate how detailed you want the capacity load calculation to be regarding functional locations.</span></span> <span data-ttu-id="3edc1-136">たとえば、フィールドに「1」の番号を挿入し、複数レベルの機能的な場所構造がある場合、機能的な場所に対するすべての資産がメンテナンス ダウンタイム アクティビティで選択され、最上位レベルに表示されます。したがって明細行の時間は、下位レベルにある機能的な場所から追加される場合があります。</span><span class="sxs-lookup"><span data-stu-id="3edc1-136">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location, which are selected on the maintenance downtime activity, will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="3edc1-137">**レベル** フィールドに数値「0」を挿入すると、関連するすべての機能的な場所レベルに関する、すべての最大能力負荷明細行を示す詳細な結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-137">If you insert the number "0" in the **Level** field, you will see a detailed result showing all capacity load lines on all the functional location levels to which they are related.</span></span>

10. <span data-ttu-id="3edc1-138">**OK** をクリックして、計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-138">Click **OK** to start the calculation.</span></span> <span data-ttu-id="3edc1-139">時間の合計数が、**最大能力負荷**の概要に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-139">The total number of hours is shown in the **Capacity load** overview.</span></span> <span data-ttu-id="3edc1-140">**最大能力負荷**タブ > **グループ化**アクション ウィンドウ グループで、該当するボタンをクリックして、予測時間の配賦の詳細な概要を取得します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-140">On the **Capacity load** tab > the **Group by...** action pane groups, click the relevant buttons to get a more detailed overview of the allocation of forecasted hours.</span></span>

![図 3](media/21-preventive-maintenance.png)

11. <span data-ttu-id="3edc1-142">最大能力負荷の概要を取得した後、作業指示書のメンテナンス作業またはメンテナンス スケジュール明細行に対して調整を行う場合、**メンテナンス ダウンタイム アクティビティ**の詳細表示に戻り、**結果としての作業指示書のメンテナンス作業**および**メンテナンス スケジュール明細行**クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-142">After you get an overview of the capacity load, if you want to make adjustments on work order maintenance jobs or maintenance schedule lines, return to the **Maintenance downtime activites** details view and select the lines you want to adjust on the **Resulting work order maintenance jobs** and **Maintenance schedule lines** FastTabs.</span></span>

12. <span data-ttu-id="3edc1-143">**調整**ボタンをクリックして、選択した作業指示書メンテナンス作業またはメンテナンス スケジュール明細行の開始予定日、終了予定日、サービス レベル、またはメンテナンス担当作業者を更新します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-143">Click the **Adjust** button and update expected start/end dates, service level, or responsible maintenance workers for the selected work order maintenance jobs or maintenance schedule lines.</span></span>

13. <span data-ttu-id="3edc1-144">必要な調整を行ったら、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3edc1-144">Click **OK** when you have made the required adjustments.</span></span> 

>[!NOTE]
><span data-ttu-id="3edc1-145">調整を行った後のメンテナンス ダウンタイム期間に含まれていない作業指示書メンテナンス作業およびメンテナンス スケジュールの明細行は、**メンテナンス ダウンタイム アクティビティ**から自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-145">Work order maintenance jobs and maintenance schedule lines that are not included in the maintenance downtime period after you have made adjustments are automatically removed from **Maintenance downtime activities**.</span></span>

14. <span data-ttu-id="3edc1-146">**すべてのメンテナンス ダウンタイム アクティビティ** > **メンテナンス ダウンタイム アクティビティ** > のリストからメンテナンス ダウンタイム アクティビティを選択し、**品目予測**をクリックして**品目予測の計算**ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-146">In **All maintenance downtime activities** > **Maintenance downtime activities** > select a maintenance downtime activity in the list and click **Item forecast** to open the **Calculate item forecast** dialog.</span></span> <span data-ttu-id="3edc1-147">このダイアログを使用して、品目 (予備部品やその他必要な品目) の予測を計算し、日付、資産、資産タイプ、メンテナンス ジョブ タイプなどによってグループ化して概要を取得します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-147">Use this dialog to calculate forecasts for items (spare parts and other required items) and group them to get an overview, for example, by date, asset, asset type, and maintenance job type.</span></span> <span data-ttu-id="3edc1-148">ダイアログに表示されている日付は、**メンテナンス ダウンタイム アクティビティ**で選択された開始日と終了日です。</span><span class="sxs-lookup"><span data-stu-id="3edc1-148">Note that the dates shown in the dialog are the start and end dates selected in **Maintenance downtime activities**.</span></span> <span data-ttu-id="3edc1-149">この計算には、予備部品やメンテナンス ダウンタイム アクティビティで選択された資産に関連する品目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-149">This calculation includes spare parts and items related to the assets that are selected on the maintenance downtime activity.</span></span>

15. <span data-ttu-id="3edc1-150">必要に応じて**品目予測の計算**ダイアログで開始時刻と終了時刻を編集し、作業指示書とメンテナンス スケジュールを計算に含めるかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-150">In the **Calculate item forecast** dialog, edit start and end times if required, and select if you want to include work orders and maintenance schedules in the calculation.</span></span> <span data-ttu-id="3edc1-151">**レベル** フィールドを使用すると、機能的な場所に関する最大能力負荷の計算の詳細度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-151">You can use the **Level** field to indicate how detailed you want the capacity load calculation to be regarding functional locations.</span></span> <span data-ttu-id="3edc1-152">たとえば、フィールドに「1」の番号を挿入し、複数レベルの機能的な場所構造がある場合、機能的な場所に対するすべての資産がメンテナンス ダウンタイム アクティビティで選択され、最上位レベルに表示されます。したがって明細行の時間は、下位レベルにある機能的な場所から追加される場合があります。</span><span class="sxs-lookup"><span data-stu-id="3edc1-152">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location, which are selected on the maintenance downtime activity, will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="3edc1-153">**レベル** フィールドに数値「0」を挿入すると、関連するすべての機能的な場所レベルに関する、すべての最大能力負荷明細行を示す詳細な結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-153">If you insert the number "0" in the **Level** field, you will see a detailed result showing all capacity load lines on all the functional location levels to which they are related.</span></span>

16. <span data-ttu-id="3edc1-154">**OK** をクリックして、計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-154">Click **OK** to start the calculation.</span></span> <span data-ttu-id="3edc1-155">品目予測の合計数は、**品目予測**の概要に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-155">The total number of item forecasts is shown in the  **Item forecast** overview.</span></span> <span data-ttu-id="3edc1-156">**品目予測**タブ > **グループ化**アクション ウィンドウ グループで、該当するボタンをクリックして、予測品目の配賦の詳細な概要を取得します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-156">On the **Item forecast** tab > the **Group by...** action pane groups, click the relevant buttons to get a more detailed overview of the allocation of forecasted items.</span></span>

![図 4](media/22-preventive-maintenance.png)

- <span data-ttu-id="3edc1-158">あるメンテナンス ダウンタイム アクティビティから別のアクティビティに資産をコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="3edc1-158">You can copy assets from one maintenance downtime activity to another.</span></span> <span data-ttu-id="3edc1-159">**すべてのメンテナンス ダウンタイム アクティビティ**で**メンテナンス ダウンタイム アクティビティのコピー** ボタンを選択します。**メンテナンス ダウンタイム アクティビティのコピー元**および**メンテナンス ダウンタイム アクティビティのコピー先**フィールドを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3edc1-159">In **All maintenance downtime activities**, select the **Copy maintenance downtime activities** button, and make your selections in the **From maintenance downtime activities** and **To maintenance downtime activities** fields, and click **OK**.</span></span>
- <span data-ttu-id="3edc1-160">**すべてのメンテナンス ダウンタイム アクティビティ**で、**メンテナンス スケジュール明細行**ボタンまたは**有効な作業指示書**ボタンをクリックして関連するリストを開き、選択したメンテナンス ダウンタイム アクティビティに関連する明細行を表示します。</span><span class="sxs-lookup"><span data-stu-id="3edc1-160">In **All maintenance downtime activities**, click the **Maintenance schedule lines** button or the **Active work orders** button to open the related lists and view the lines related to the selected maintenance downtime activity.</span></span>

