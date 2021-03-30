---
title: 貨物使用率のスケジュール設定
description: このトピックでは、倉庫の負荷を設定およびスケジュールする方法について説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f88dc44b036f6d5535f7e83693a387149f94f37d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239257"
---
# <a name="schedule-load-utilization"></a><span data-ttu-id="3721f-103">貨物使用率のスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="3721f-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3721f-104">選択した場所のタイプに負荷の稼働をスケジューリングすることも、現在および将来の負荷の稼働をプロジェクト化することもできます。</span><span class="sxs-lookup"><span data-stu-id="3721f-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="3721f-105">1 つ以上のサイトの負荷、負荷単位 (ゾーンまたは倉庫)、またはゾーンと倉庫の組み合わせの負荷をプロジェクト化できます。</span><span class="sxs-lookup"><span data-stu-id="3721f-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="3721f-106">倉庫またはサイトの負荷のスケジュールおよび表示</span><span class="sxs-lookup"><span data-stu-id="3721f-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="3721f-107">サイト、倉庫またはゾーンの負荷をスケジュールするには、空間使用率の設定を作成し、それをマスター プランに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="3721f-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="3721f-108">空間使用率の設定で、**バルク場所** および **ピッキング場所の** などの、使用する場所のタイプは、空間使用率を予測する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="3721f-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="3721f-109">**ゾーン** などの保管負荷モードも指定します。</span><span class="sxs-lookup"><span data-stu-id="3721f-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="3721f-110">将来の空間使用率の予測は、関連するマスター プランで計算される情報に基づいています。</span><span class="sxs-lookup"><span data-stu-id="3721f-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="3721f-111">マスター プランにより、生産および工程のための着信および送信オーダーのリソース計画が予測されます。</span><span class="sxs-lookup"><span data-stu-id="3721f-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="3721f-112">使用可能な空間の予想は、空間使用率の設定および選択したマスター プラン間のリレーションに基づいています。</span><span class="sxs-lookup"><span data-stu-id="3721f-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="3721f-113">空間使用率の設定で選択した保管負荷モードを使用して、各倉庫またはゾーンのために負荷を予測するかどうか、または予測に倉庫およびゾーン両方に関する情報を含むかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3721f-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="3721f-114">ブロックされた場所を負荷の使用の計算から除くかどうかも指定します。</span><span class="sxs-lookup"><span data-stu-id="3721f-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="3721f-115">**倉庫貨物使用率** レポートを生成することによって、空間使用率をプロジェクト化できます。</span><span class="sxs-lookup"><span data-stu-id="3721f-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="3721f-116">このレポートを生成するとき、負荷の使用を各サイトで、サイト全域で、またはゾーンや倉庫などの選択した負荷単位で予測するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3721f-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="3721f-117">倉庫用の空間使用率の設定を作成</span><span class="sxs-lookup"><span data-stu-id="3721f-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="3721f-118">**在庫管理** \> **設定** \> **倉庫の監視** \> **空間使用率** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="3721f-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="3721f-119">**新規** を選択して、空間使用率の設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="3721f-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="3721f-120">新しい設定の ID と名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="3721f-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="3721f-121">**保管負荷モード** フィールドで、空間使用率の概要が倉庫、ゾーン、または倉庫とゾーンによる情報を表示すべきかを選択します。</span><span class="sxs-lookup"><span data-stu-id="3721f-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="3721f-122">**ブロックされた場所の除外** オプションを **はい** に設定して、ブロックされた在庫場所を利用可能領域の計算から除外します。</span><span class="sxs-lookup"><span data-stu-id="3721f-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="3721f-123">**在庫場所** ページの **その他** クイック タブの、**ブロックされた入力** または **ブロックされた出力** フィールドで、場所のブロックの原因を指定して、入出力の在庫場所をブロックすることができます。</span><span class="sxs-lookup"><span data-stu-id="3721f-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="3721f-124">**場所タイプ** クイック タブで、空間使用率の計算に含める場所のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="3721f-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="3721f-125">プロジェクションに 1 つ以上の場所タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3721f-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="3721f-126">設定するマスター プランに空間使用率を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="3721f-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="3721f-127">**在庫管理** \> **定期処理** \> **貨物使用率のスケジュール設定** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="3721f-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="3721f-128">**マスター プラン** フィールドで、マスター プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="3721f-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="3721f-129">**日数** フィールドで、現在および将来のワークロードの予想に含める日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3721f-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="3721f-130">**空間使用率** フィールドで、現在および将来のワークロードの予想に使用する空間使用率の設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="3721f-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="3721f-131">負荷の使用の予想を指定し、情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="3721f-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="3721f-132">**在庫管理** \> **照会およびレポート** \> **現物在庫レポート** \> **倉庫貨物使用率** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="3721f-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="3721f-133">**表示方法** フィールドで、空間使用率の予想レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3721f-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="3721f-134">**サイト**– 各サイトの空間使用率を予測します。</span><span class="sxs-lookup"><span data-stu-id="3721f-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="3721f-135">この予測は、たとえば倉庫間の空間使用率のバランスを取るために、サイトのすべての倉庫を表示する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="3721f-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="3721f-136">**負荷単位**– ゾーンまたは倉庫の空間使用率を予測します。</span><span class="sxs-lookup"><span data-stu-id="3721f-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="3721f-137">空間使用率の設定を作成すると、**空間使用率** ページの **保管負荷モード** フィールドで選択した値に基づいて、使用可能領域が予想されます。</span><span class="sxs-lookup"><span data-stu-id="3721f-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="3721f-138">前の手順で選択した値に応じて、これらの手順のいずれかに従います。</span><span class="sxs-lookup"><span data-stu-id="3721f-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="3721f-139">**表示方法** フィールドで **サイト** を選択した場合、**サイト** フィールドが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="3721f-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="3721f-140">予想に含める 1 つ以上のサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="3721f-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="3721f-141">**表示方法** フィールドで **負荷単位** を選択した場合、**負荷単位** フィールドが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="3721f-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="3721f-142">負荷単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="3721f-142">Select the load unit.</span></span>

4. <span data-ttu-id="3721f-143">**負荷タイプ** フィールドで、**量** または **重量** を選択し、空間を予測する倉庫の作業単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="3721f-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="3721f-144">**空間使用率の設定** フィールドで、予測の基になるべき空間使用率の設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="3721f-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]