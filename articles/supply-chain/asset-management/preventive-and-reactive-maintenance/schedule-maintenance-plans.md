---
title: メンテナンス計画のスケジュール
description: このトピックでは、資産管理におけるメンテナンス計画のスケジュールについて説明します。
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9c215417eacb8a0e1ec0a8324fe35fc053089afb
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016909"
---
# <a name="schedule-maintenance-plans"></a><span data-ttu-id="62678-103">メンテナンス計画のスケジュール</span><span class="sxs-lookup"><span data-stu-id="62678-103">Schedule maintenance plans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="62678-104">予防的メンテナンスのスケジューリングは、資産に設定されたメンテナンス計画に基づいて、資産にカレンダー エントリを生成します。</span><span class="sxs-lookup"><span data-stu-id="62678-104">Preventive maintenance scheduling generates calendar entries on assets, based on the maintenance plans set up on the assets.</span></span> <span data-ttu-id="62678-105">選択したメンテナンス計画、資産タイプ、および資産に基づいてカレンダー エントリをスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="62678-105">You can schedule calendar entries based on selected maintenance plans, asset types, and assets.</span></span>

1. <span data-ttu-id="62678-106">**資産管理** > **定期処理** > **予防的メンテナンス** > **メンテナンス計画のスケジュール** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62678-106">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance plans**.</span></span>

2. <span data-ttu-id="62678-107">**期間** と **期間頻度** のフィールドで時間間隔を選択できます。</span><span class="sxs-lookup"><span data-stu-id="62678-107">You can select a time interval in the **Period** and **Period frequency** fields.</span></span>

>[!NOTE]
><span data-ttu-id="62678-108">**期間** および **期間頻度** のフィールドには、作成したメンテナンス計画 (時間ベースまたはカウンターベース) に基づいて、メンテナンス スケジュール行をどれだけ先に作成するかが示されます。</span><span class="sxs-lookup"><span data-stu-id="62678-108">The **Period** and **Period frequencey** fields indicate how far ahead in time you want maintenance schedule lines to be created, based on the maintenance plans you have created (time-based or counter-based).</span></span> <span data-ttu-id="62678-109">次の図では、メンテナンス スケジュール行 (= ワーク オーダー提案) が現在の日付および 3 か月後から作成されます。</span><span class="sxs-lookup"><span data-stu-id="62678-109">In the figure below, maintenance schedule lines (= work order proposals) are created from the current date and three months onwards.</span></span>

3. <span data-ttu-id="62678-110">メンテナンス計画行に従ってワークー オーダーを自動的に作成する場合は、**行で指定されている場合は自動作成** のトグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="62678-110">Select "Yes" on the **Auto create if specified in the line** toggle button if work orders should automatically be created according to the maintenance plan line.</span></span>

>[!NOTE]
><span data-ttu-id="62678-111">このトグル ボタンが 「はい」に設定されている場合、*また*、**メンテナンス計画** のメンテナンス計画行で **自動作成** チェック ボックスも選択されている場合、ワーク オーダーはメンテナンス計画行に基づいて作成され、「ワーク オーダー作成済」ステータスのメンテナンス計画行も作成されます。</span><span class="sxs-lookup"><span data-stu-id="62678-111">If this toggle button is set to "Yes", *and* the **Auto create** check box is also selected on maintenance plan lines in **Maintenance plans**, work orders are created based on the maintenance plan lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="62678-112">オプションを 1 つだけ選択した場合 (このダイアログの **行で指定されている場合は自動作成** トグル ボタン、または **メンテナンス計画** フォームの **自動作成** チェック ボックス)、メンテナンス スケジュール行が「作成済」ステータスで作成されます。</span><span class="sxs-lookup"><span data-stu-id="62678-112">If only one option is selected (**Auto create if specified in the line** toggle button in this dialog or **Auto create** check box in **Maintenance plans** form), only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="62678-113">その場合、ワーク オーダーは作成されません。</span><span class="sxs-lookup"><span data-stu-id="62678-113">In that case, no work orders are created.</span></span>

4. <span data-ttu-id="62678-114">メンテナンス計画 (時間またはカウンター)、資産、資産タイプ、機能的な場所、および機能的な場所タイプに基づいて、カレンダー エントリを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="62678-114">It is possible to generate calendar entries based on maintenance plans (time or counter), assets, asset types, functional locations, and functional location types.</span></span> <span data-ttu-id="62678-115">**フィルター** ボタンをクリックして、必要に応じて選択を行います。</span><span class="sxs-lookup"><span data-stu-id="62678-115">Click the **Filter** button and make your selections, if required.</span></span>

- <span data-ttu-id="62678-116">機能的な場所のメンテナンス計画のスケジュールについて : メンテナンス計画をスケジュールした後に、**すべての機能的な場所** > **メンテナンス計画** クイック タブで、資産タイプ、メーカー、およびモデルのメンテナンス計画の設定を更新する場合は、その機能的な場所に関連する既存のメンテナンス スケジュール エントリは自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="62678-116">Regarding scheduling of maintenance plans on functional locations: If you update the setup of asset types, manufacturers, and models on maintenance plans in **All functional locations** > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="62678-117">機能的な場所の更新されたメンテナンス計画設定に対応する新しいカレンダー エントリを作成するには、その機能的な場所に対する新しいメンテナンス計画スケジュールを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62678-117">In order to create new calendar entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> <span data-ttu-id="62678-118">機能的な場所の資産タイプ、メーカー、およびモデルの設定については、[機能的な場所の作成](../functional-locations/create-functional-locations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62678-118">Read more about the setup of asset types, manufacturers, and models on functional locations in [Create functional locations](../functional-locations/create-functional-locations.md).</span></span>

><span data-ttu-id="62678-119">*例* : 特定の機能的な場所のメンテナンス計画を作成すると、メンテナンス計画をスケジュールする際に、その機能的な場所に設定された資産が常に含まれます。</span><span class="sxs-lookup"><span data-stu-id="62678-119">*Example:* You want to create a maintenance plan for a specific functional location, meaning all assets set up on that functional location at any given time will be included when you schedule the maintenance plan.</span></span> <span data-ttu-id="62678-120">この場合、メンテナンス計画を作成し、特定の機能的な場所を選択しますが、メンテナンス計画に資産を追加することはしません。</span><span class="sxs-lookup"><span data-stu-id="62678-120">In that case, you create a maintenance plan and select the specific functional location, but you do NOT add any assets in the maintenance plan.</span></span> <span data-ttu-id="62678-121">その結果、そのメンテナンス計画をスケジュールすると、その時点で機能的な場所に関連付けられているすべての資産のメンテナンス スケジュール行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="62678-121">The result is that when you schedule that maintenance plan, maintenance schedule lines will be created for all the assets related to the functional location at that time.</span></span>

- <span data-ttu-id="62678-122">**資産タイプ** の資産タイプ、メーカー、モデルに変更を加えた場合、それらの変更は更新された資産タイプを使用する新しい資産にのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="62678-122">If you make changes to asset types, manufacturers and models in **Asset types**, those changes only affect new assets that use the updated asset type.</span></span> <span data-ttu-id="62678-123">資産タイプ設定の詳細については、[資産タイプ](../setup-for-objects/object-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62678-123">Read more about asset type setup in [Asset types](../setup-for-objects/object-types.md).</span></span>  

5. <span data-ttu-id="62678-124">**OK** をクリックして、資産のメンテナンス スケジュール エントリの生成を開始します。</span><span class="sxs-lookup"><span data-stu-id="62678-124">Click **OK** to start the generation of maintenance schedule entries on assets.</span></span> <span data-ttu-id="62678-125">生成されたエントリは、**すべてのメンテナンス スケジュール** リストのページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="62678-125">The generated entries will be shown in the **All maintenance schedule** list page.</span></span> <span data-ttu-id="62678-126">次の図は、**メンテナンス計画のスケジュール** ダイアログの例を示します。</span><span class="sxs-lookup"><span data-stu-id="62678-126">The following illustration shows an example of the **Schedule maintenance plans** dialog.</span></span>

![図 1](media/09-preventive-maintenance.png)

- <span data-ttu-id="62678-128">**メンテナンス計画のスケジュール** ダイアログでは、**バックグラウンドで実行** クイック タブでバッチ ジョブを設定して、定期的にカレンダー エントリを自動的に生成することができます。</span><span class="sxs-lookup"><span data-stu-id="62678-128">In the **Schedule maintenance plans** dialog, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.</span></span>  
- <span data-ttu-id="62678-129">予防的メンテナンスをスケジュールすると、開始日がシステム日付と時刻よりも前のメンテナンス スケジュール行は作成されません。</span><span class="sxs-lookup"><span data-stu-id="62678-129">When you schedule preventive maintenance, maintenance schedule lines with expected start date and time earlier than the system date and time will not be created.</span></span>  

<span data-ttu-id="62678-130">次の図は、時間ベースのメンテナンス計画の計算を図解したものです。</span><span class="sxs-lookup"><span data-stu-id="62678-130">The figure below provides a graphic illustration of a time-based maintenance plan calculation.</span></span>  

![図 2](media/10-preventive-maintenance.jpg)

<span data-ttu-id="62678-132">カウンターベースのメンテナンス計画について : 次の図では、2 つの異なるカウンター登録サイクルが示されています。</span><span class="sxs-lookup"><span data-stu-id="62678-132">Regarding counter-based maintenance plans: In the figures below, two different counter registration cycles are shown.</span></span> <span data-ttu-id="62678-133">これらは、資産 V0001 に対して設定されたメンテナンス計画に基づいており、毎月約 2,000 km を走る資産 (自動車) を想定しています。</span><span class="sxs-lookup"><span data-stu-id="62678-133">They are based on a maintenance plan set up for asset "V0001", expecting the asset (a car) to run approx. 2,000 km every month.</span></span>

<span data-ttu-id="62678-134">最初の例では、予想される 2,000 km に毎月達することはありません。</span><span class="sxs-lookup"><span data-stu-id="62678-134">In the first example, the expected 2,000 km are not reached every month.</span></span> <span data-ttu-id="62678-135">カウンターベースのメンテナンス計画によれば、しきい値は 2,000 km です。つまり、メンテナンス計画のスケジューリングを実行した場合、毎回 2,000 km のしきい値に達するたびに、メンテナンス スケジュール行を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62678-135">According to the counter-based maintenance plan, the threshold is 2,000 km, meaning when you run a maintenance plan scheduling, a maintenance schedule line should be created each time the 2,000-kilometer threshold is reached.</span></span> <span data-ttu-id="62678-136">例 1 には、4 つの登録行がありますが、2,000 キロメートルしきい値に達するのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="62678-136">In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once.</span></span> <span data-ttu-id="62678-137">したがって、たとえば 3 か月の期間、この資産のメンテナンス計画のスケジュールを実行すると、1 つのメンテナンス スケジュール行のみが作成されます。</span><span class="sxs-lookup"><span data-stu-id="62678-137">This means that when you run schedule maintenance plans this asset, for example for a 3-month period, only one maintenance schedule line will be created.</span></span>

<span data-ttu-id="62678-138">次の図では、2,000 km 以上が毎月登録されています。</span><span class="sxs-lookup"><span data-stu-id="62678-138">In the next figure, 2,000 km or more are registered every month.</span></span> <span data-ttu-id="62678-139">したがって、3 か月の期間、この資産のメンテナンス計画をスケジュールすると、3 つのメンテナンス行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="62678-139">Therefore, three maintenance lines would be created if you schedule maintenance plans for this asset for a 3-month period.</span></span> 

<span data-ttu-id="62678-140">これらの例は、資産に対してなされたすべてのカウンター登録が、資産の消耗を示す傾向を示していることを説明しています。</span><span class="sxs-lookup"><span data-stu-id="62678-140">The examples described here show that all counter registrations made on an asset show a trend describing wear and tear on the asset.</span></span> <span data-ttu-id="62678-141">その傾向は、メンテナンス計画のスケジューリング時に計算基準として使用されます。</span><span class="sxs-lookup"><span data-stu-id="62678-141">That trend is used as calculation basis at the time of maintenance plan scheduling.</span></span>

![図 3](media/11-preventive-maintenance.png)

![図 4](media/12-preventive-maintenance.png)

