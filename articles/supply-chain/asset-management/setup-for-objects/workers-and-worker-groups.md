---
title: メンテナンス作業者および作業者グループ
description: このトピックでは、資産管理のメンテナンス作業者および作業者グループについて説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6cf7e8e796032b348cff5a77c10b376dbbeef974
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214783"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="bd39b-103">メンテナンス作業者および作業者グループ</span><span class="sxs-lookup"><span data-stu-id="bd39b-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="bd39b-104">このトピックでは、資産管理のメンテナンス作業者および作業者グループについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="bd39b-105">資産管理では、メンテナンス作業者を機能的な場所に接続することができます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="bd39b-106">(機能的な場所の詳細については、[機能的な場所の作成](../functional-locations/create-functional-locations.md)を参照してください。) このメンテナンス機能は、たとえば、機能的な場所 01 にあるマシンでメンテナンス ジョブをスケジュールし、同じ場所からメンテナンス作業者を割り当ててジョブを実行する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="bd39b-107">また、メンテナンス作業者グループを作成し、メンテナンス作業者を関連付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="bd39b-108">この機能は、単純な作業指示書のスケジューリングを行い、作業指示書のメンテナンス作業者のグループをスケジュールする場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="bd39b-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="bd39b-109">メンテナンス作業者およびメンテナンス作業者グループを使用して、優先メンテナンス作業者およびメンテナンス担当作業者を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="bd39b-110">作業者の作成</span><span class="sxs-lookup"><span data-stu-id="bd39b-110">Create workers</span></span>

1. <span data-ttu-id="bd39b-111">**資産管理** \> **設定** \> **作業者** \> **作業者**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="bd39b-112">**新規**を選択すると、作業者を一覧に追加できます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="bd39b-113">**作業者**フィールドで、作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="bd39b-114">**有効**オプションを**はい**に設定し、作業指示書で作業者をスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="bd39b-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="bd39b-115">**一般**クイック タブでは、リソースが作業者に対して選択されている場合、**リソース** フィールドと**説明**フィールドは自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="bd39b-116">作業者をリソースとして設定し、**リソース** ページ (**組織管理** \> **リソース** \> **リソース**) でそのリソースにカレンダーを割り当てた場合、**カレンダー** フィールドも自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="bd39b-117">**グループ** クイック タブで、**追加**を選択し、作業者のメンテナンス作業者グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="bd39b-118">作業者は複数のグループに所属させることができます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="bd39b-119">標準設定では、グループを追加した日付から作業者のグループへの所属が有効になり、有効期限が切れることはありません。</span><span class="sxs-lookup"><span data-stu-id="bd39b-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="bd39b-120">この日付は、**有効**フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="bd39b-121">**有効**フィールドを表示するには、**表示** \> **すべて**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="bd39b-122">作業者のグループへの所属を特定の期間に限定する必要がある場合は、**有効**および**有効期限**フィールドを使用して期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="bd39b-123">**機能の場所**クイック タブで、**追加**を選択し、メンテナンス作業者の機能の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="bd39b-124">また、作業者の主要な機能の場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bd39b-125">作業者に機能の場所を追加すると、それらの機能の場所に関連するすべての有効な資産が、**個人用の有効な資産**および**個人用の有効な機能の場所**などのさまざまなメニュー項目に表示されます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="bd39b-126">また、新しい資産、メンテナンス要求、または作業指示書の作成時に表示される資産ルックアップにも表示されます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="bd39b-127">**詳細**クイック タブのフィールドには、選択したメンテナンス作業者が関連するメンテナンス作業者グループと機能の場所の数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="bd39b-128">作業者グループの作成</span><span class="sxs-lookup"><span data-stu-id="bd39b-128">Create worker groups</span></span>

1. <span data-ttu-id="bd39b-129">**資産管理** \> **設定** \> **作業者** \> **メンテナンス作業者グループ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="bd39b-130">**新規**を選択すると、作業者グループを一覧に追加できます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="bd39b-131">**メンテナンス作業者グループ** フィールドに、グループ ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="bd39b-132">**名前**フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="bd39b-133">**作業者**クイック タブで、**追加**を選択し、作業者グループのメンテナンス作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="bd39b-134">**有効**および**有効期限**フィールドに関する情報については、前の手順の手順 6 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd39b-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="bd39b-135">リソース グループを選択したメンテナンス作業者グループに関連づける場合は、**リソース グループからコピー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="bd39b-136">**グループ** フィールドで、カレンダーの設定をコピーするリソース グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="bd39b-137">次に、**作業者グループ** フィールドで、リソース グループのカレンダー設定をコピーする作業者グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="bd39b-138">このステップは、作業指示書のスケジューリング中に、メンテナンス作業者がリソース (ワーク センター) に関連するカレンダーを使用する場合にのみ関連します。</span><span class="sxs-lookup"><span data-stu-id="bd39b-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="bd39b-139">**詳細**クイック タブのフィールドには、選択したメンテナンス作業者グループに設定されたメンテナンス作業者グループの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bd39b-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>
