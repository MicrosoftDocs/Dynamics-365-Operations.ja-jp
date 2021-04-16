---
title: メンテナンス スケジュール
description: このトピックでは、資産管理におけるメンテナンス スケジュールについて説明します。
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f7bed45ccf151a2667dcc8dddd5c0586a594ca58
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839586"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="85657-103">メンテナンス スケジュール</span><span class="sxs-lookup"><span data-stu-id="85657-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="85657-104">メンテナンス スケジュールには、すべての予定された予防的メンテナンス計画、メンテナンス要求、および実行されるメンテナンス ラウンドのリストが含まれています。一部のスケジュール明細行は、作業指示書に変換されていることがあります。</span><span class="sxs-lookup"><span data-stu-id="85657-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="85657-105">メンテナンス スケジュールの 4 つのビューは、表示するメンテナンス スケジュールの明細行に応じて少し異なります。</span><span class="sxs-lookup"><span data-stu-id="85657-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="85657-106">メニュー項目</span><span class="sxs-lookup"><span data-stu-id="85657-106">Menu item</span></span>                  | <span data-ttu-id="85657-107">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="85657-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85657-108">すべてのメンテナンス スケジュール</span><span class="sxs-lookup"><span data-stu-id="85657-108">All maintenance schedule</span></span>       | <span data-ttu-id="85657-109">すべてのメンテナンス スケジュール明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="85657-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="85657-110">自分の資産スケジュール</span><span class="sxs-lookup"><span data-stu-id="85657-110">My asset schedule</span></span>        | <span data-ttu-id="85657-111">このリストには、作業者として関連付けられている ([メンテナンス作業者と作業者グループ](../setup-for-objects/workers-and-worker-groups.md) で設定) 機能の場所にインストールされている資産を含む、すべてのメンテナンス スケジュールの明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="85657-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="85657-112">メンテナンス スケジュール明細行を開く</span><span class="sxs-lookup"><span data-stu-id="85657-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="85657-113">このリストには、ステータスが「作成済」であるメンテナンス スケジュールの明細行 (つまり、作業指示書に変換されていないかまたは破棄済み) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="85657-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="85657-114">メンテナンス スケジュール プールを開く</span><span class="sxs-lookup"><span data-stu-id="85657-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="85657-115">このリストには、作業指示書プールに関連するメンテナンス スケジュールの明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="85657-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="85657-116">メンテナンス スケジュールの明細行が複数の作業指示書プールに含まれている場合 ([作業指示書プール](../work-orders/work-order-pools.md) を参照)、**未処理のメンテナンス スケジュール プール** の各プールに 1 つのレコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="85657-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="85657-117">これは、作業指示書プールに対するフィルター処理オプションを最適化するために行われます。</span><span class="sxs-lookup"><span data-stu-id="85657-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="85657-118">メンテナンス スケジュールを開く。</span><span class="sxs-lookup"><span data-stu-id="85657-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="85657-119">**資産管理** > **共通** > **メンテナンス スケジュール** > **すべてのメンテナンス スケジュール** または **未処理のメンテナンス スケジュール明細行** または **未処理のメンテナンス スケジュール プール** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="85657-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="85657-120">メンテナンス スケジュールを更新するには、**メンテナンス計画** または **メンテナンス ラウンド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85657-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="85657-121">選択し、**編集** をクリックすることにより、メンテナンス スケジュールの明細行を編集することができます。</span><span class="sxs-lookup"><span data-stu-id="85657-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="85657-122">たとえば、サービス レベルまたはジョブの担当作業者を簡単に更新できます。</span><span class="sxs-lookup"><span data-stu-id="85657-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="85657-123">まだ作業指示書に関連付けられていないメンテナンス スケジュールの明細行のみを編集できます。</span><span class="sxs-lookup"><span data-stu-id="85657-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="85657-124">リスト ページで選択し **削除** をクリックすることにより、メンテナンス スケジュールの明細行を削除することができます。</span><span class="sxs-lookup"><span data-stu-id="85657-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="85657-125">リスト ページで選択し **破棄** をクリックすることにより、メンテナンス スケジュールの明細行を破棄することができます。</span><span class="sxs-lookup"><span data-stu-id="85657-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="85657-126">たとえば、この機能は資産に 2,000 km のメンテナンス計画と 10,000 km のメンテナンス計画がある場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="85657-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="85657-127">次に、10,000 km、20,000 km、30,000 km などと一致する場合、2,000 km のメンテナンス計画から作成された明細行を廃棄することができます。</span><span class="sxs-lookup"><span data-stu-id="85657-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="85657-128">メンテナンス計画に関連付けられているメンテナンス スケジュールの明細行を廃棄した場合、そのメンテナンス計画がスケジュールされている場合でも、その明細行が再度表示されることはありません。</span><span class="sxs-lookup"><span data-stu-id="85657-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="85657-129">**すべてのメンテナンス スケジュール** のメンテナンス スケジュール明細行の番号を選択し、**作業指示書プール** をクリックすることにより、選択した明細行すべてを同じ作業指示書プールに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="85657-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="85657-130">**すべてのメンテナンス スケジュール**、**未処理のメンテナンス スケジュール明細行**、または **未処理のメンテナンス スケジュール プール** のメンテナンス スケジュールの番号を選択し、**スケジュールの調整** をクリックすることにより、複数の明細行に対して同じ調整を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="85657-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="85657-131">選択したメンテナンス スケジュールの明細行に関連付けられている開始予定日と終了予定日、サービス レベル、および担当メンテナンス作業者グループまたは担当メンテナンス作業者を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="85657-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="85657-132">メンテナンス スケジュールの明細行が作業指示書に関連付けられている場合、作業指示書 ID が **作業指示書** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="85657-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="85657-133">**すべての資産** の詳細表示 > **資産メンテナンス計画** のクイックタブで、資産のメンテナンス計画を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="85657-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="85657-134">後で、**全資産** の資産に関連付けられているメンテナンス計画明細行を削除すると、そのメンテナンス計画に基づいて作成された、「作成済」のステータスを持つすべてのメンテナンス スケジュール明細行も自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="85657-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="85657-135">[資産の作成](../objects/create-an-object.md) も参照してください。</span><span class="sxs-lookup"><span data-stu-id="85657-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="85657-136">次の図は、**すべてのメンテナンス スケジュール** のリスト ページを示しています。</span><span class="sxs-lookup"><span data-stu-id="85657-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![図 1](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]