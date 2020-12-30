---
title: 倉庫のコンフィギュレーションの概要
description: この記事は、倉庫をコンフィギュレーションする方法について説明します。 これには、倉庫レイアウトおよび倉庫プロセスを有効にする方法に関する情報が含まれます。
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 11554
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8cd436f1b8324335cc39ce54344db834dddebc9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431825"
---
# <a name="warehouse-configuration-overview"></a><span data-ttu-id="6388f-104">倉庫のコンフィギュレーションの概要</span><span class="sxs-lookup"><span data-stu-id="6388f-104">Warehouse configuration overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6388f-105">この記事は、倉庫をコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6388f-105">This article explains how to configure a warehouse.</span></span> <span data-ttu-id="6388f-106">これには、倉庫レイアウトおよび倉庫プロセスを有効にする方法に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6388f-106">It includes information about how to enable a warehouse layout and warehouse processes.</span></span>

> [!NOTE]
> <span data-ttu-id="6388f-107">この記事は、**倉庫管理** モジュールの機能が対象です (詳細な倉庫保管)。</span><span class="sxs-lookup"><span data-stu-id="6388f-107">This article applies to features in the **Warehouse management** module (advanced warehousing).</span></span> <span data-ttu-id="6388f-108">**在庫管理** モジュールの倉庫機能は対象外です。</span><span class="sxs-lookup"><span data-stu-id="6388f-108">It doesn't apply to warehouse features in the **Inventory management** module.</span></span>

## <a name="warehouse-layout"></a><span data-ttu-id="6388f-109">倉庫レイアウト</span><span class="sxs-lookup"><span data-stu-id="6388f-109">Warehouse layout</span></span>
<span data-ttu-id="6388f-110">Supply Chain Management の倉庫管理システムは、最適な倉庫効率を達成できるよう、変化するニーズを満たす倉庫レイアウトを定義する柔軟な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="6388f-110">The Warehouse management system in Supply Chain Management gives you flexible ways to define your warehouse layout to meet changing needs, so that you can achieve optimal warehouse efficiency.</span></span>

-   <span data-ttu-id="6388f-111">商品を最適に配置するために、優先順位が高い保管エリアと優先順位の低い保管エリアを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-111">You can establish high-priority and low-priority storages areas for optimum placement of goods.</span></span>
-   <span data-ttu-id="6388f-112">品目の温度条件や回転率など、さまざまな倉庫のニーズに対応するため、倉庫をゾーンに分割できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-112">You can divide your warehouse into zones to accommodate various storage needs, such as temperature requirements, or various turnover rates for items.</span></span>
-   <span data-ttu-id="6388f-113">すべてのレベルに倉庫の場所を指定できます (たとえば、サイト、倉庫、通路、ラック、棚、および在庫置場の位置)。</span><span class="sxs-lookup"><span data-stu-id="6388f-113">You can specify warehouse locations on any level (for example, site, warehouse, aisle, rack, shelf, and bin position).</span></span>
-   <span data-ttu-id="6388f-114">物理的能力制約の設定を使用して場所をグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-114">You can group locations by using physical capacity constraint settings.</span></span>
-   <span data-ttu-id="6388f-115">クエリ定義したルールに基づいて品目の保管、ピッキング方法を制御できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-115">You can control how items are stored and picked, based on query-defined rules.</span></span>

<span data-ttu-id="6388f-116">Supply Chain Management で倉庫管理を使用するには、倉庫を作成し、詳細またはより特別な倉庫管理の活動に対して有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6388f-116">To use warehouse management in Supply Chain Management, you must create a warehouse and enable it for more advanced or specialized warehouse management activities.</span></span> <span data-ttu-id="6388f-117">**倉庫** ページで、**倉庫管理プロセスの使用** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6388f-117">On the **Warehouses** page, select the **Use warehouse management processes** option.</span></span>

### <a name="zone-groups-zones-location-types-and-locations"></a><span data-ttu-id="6388f-118">ゾーン グループ、ゾーン、場所のタイプと場所</span><span class="sxs-lookup"><span data-stu-id="6388f-118">Zone groups, zones, location types, and locations</span></span>

<span data-ttu-id="6388f-119">倉庫レイアウトを有効にするプロセスの一部として、倉庫ゾーン グループ、およびゾーン、場所プロファイル、場所タイプと場所を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6388f-119">As part of the process for enabling a warehouse layout, you must define warehouse zone groups, and zones, location profiles, location types, and locations.</span></span>

-   <span data-ttu-id="6388f-120">**ゾーン グループ** – 倉庫内のゾーンの論理的または物理的グループ。</span><span class="sxs-lookup"><span data-stu-id="6388f-120">**Zone groups** – A logical or physical grouping of zones within a warehouse.</span></span>
-   <span data-ttu-id="6388f-121">**ゾーン** – 倉庫内の場所の論理的または物理的グループ。</span><span class="sxs-lookup"><span data-stu-id="6388f-121">**Zones** – A logical or physical grouping of locations within a warehouse.</span></span>
-   <span data-ttu-id="6388f-122">**場所プロファイル** –同じ倉庫場所プロセスのポリシーを持つ論理的または物理的グループ (たとえば、異なる品目番号の組み合わせが保管でき、同じ物理的能力制約が適用されます)。</span><span class="sxs-lookup"><span data-stu-id="6388f-122">**Location profiles** – A logical or physical grouping of locations that have the same warehouse location process policies (for example, a mix of different item numbers can be stored there, and the same physical capacity constraints apply).</span></span>
-   <span data-ttu-id="6388f-123">**場所タイプ** – 倉庫の場所の論理的または物理的グループ。</span><span class="sxs-lookup"><span data-stu-id="6388f-123">**Locations types** – A logical or physical grouping of the warehouse locations.</span></span> <span data-ttu-id="6388f-124">たとえば、すべてのステージング場所の場所タイプを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-124">For example, you can create a location type for all staging locations.</span></span> <span data-ttu-id="6388f-125">**倉庫管理パラメーター** ページの必須の設定は、ステージング場所のタイプおよび最終出荷場所タイプを定義するプロセスをドライブします。</span><span class="sxs-lookup"><span data-stu-id="6388f-125">Mandatory settings on the **Warehouse management parameters** page drive the process of defining staging location types and the final shipping location type.</span></span>
-   <span data-ttu-id="6388f-126">**場所** – 場所情報の最下位レベル。</span><span class="sxs-lookup"><span data-stu-id="6388f-126">**Locations** – The lowest level of location information.</span></span> <span data-ttu-id="6388f-127">場所は、手持在庫が倉庫のどこに格納され、どこでピッキングされるかの追跡に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6388f-127">Locations are used to track where the on-hand inventory is stored and picked in a warehouse.</span></span>

<span data-ttu-id="6388f-128">自分の倉庫レイアウトを定義するために作成するエンティティは、、倉庫内で作業注文をドライブするための作業テンプレートで設定するクエリで使用されます。</span><span class="sxs-lookup"><span data-stu-id="6388f-128">The entities that you create to define your warehouse layout are used in the queries that you set up in work templates to drive work orders in the warehouse.</span></span> <span data-ttu-id="6388f-129">したがって、ゾーンや場所タイプなど定義するとき、倉庫のさまざまな領域が異なるプロセスにどのように使用されるかを検討してください。</span><span class="sxs-lookup"><span data-stu-id="6388f-129">Therefore, when you define the zones, location types, and so on, consider how different areas in the warehouse are used for different processes.</span></span> <span data-ttu-id="6388f-130">また、特定の領域の物理的特性などの要素を検討してください。</span><span class="sxs-lookup"><span data-stu-id="6388f-130">Additionally, consider factors such as the physical characteristics of a particular area.</span></span> <span data-ttu-id="6388f-131">たとえば、特定のタイプのフォークリフトのみ使用できる領域がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="6388f-131">For example, there might be areas where you can use only a certain type of forklift truck.</span></span> <span data-ttu-id="6388f-132">または、会社が同じ施設内に製造と完成製品の両方がある場合、Supply Chain Management での 1 つの倉庫を作成し、ゾーン グループを作成して 2 つの工程を分割するのが望ましい場合があります。</span><span class="sxs-lookup"><span data-stu-id="6388f-132">Or, if your company has both production and finished goods within the same facility, you might want to create a single warehouse in Supply Chain Management but then separate the two operations by creating two zone groups.</span></span> <span data-ttu-id="6388f-133">テンプレートのクエリで使用するときに識別することが容易になるように、エンティティに内容を示す名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6388f-133">Give your entities descriptive names, so that it's easy to identify them when you use them in template queries.</span></span>

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a><span data-ttu-id="6388f-134">場所別在庫限度、場所プロファイルと固定のピッキング場所</span><span class="sxs-lookup"><span data-stu-id="6388f-134">Location stocking limits, location profiles, and fixed picking locations</span></span>

<span data-ttu-id="6388f-135">保管量 (場所別在庫限度および場所プロファイル) を決定するため、また最適な倉庫プロセスを達成するために倉庫の物理的なレイアウトを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6388f-135">You must consider the physical layout of the warehouse, both to determine storage capacities (location stocking limits and location profiles) and as part of your attempts to achieve optimal warehouse processes.</span></span> 

<span data-ttu-id="6388f-136">場所別在庫限度は、在庫を配送する物理的能力がない場所に在庫の配置を要求する作業が作成されないことを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="6388f-136">Location stocking limits help guarantee that work isn't created to request that inventory be put in a location that doesn't have the physical capacity to carry the inventory.</span></span> <span data-ttu-id="6388f-137">たとえば、倉庫内の場所が、場所ごとに 1 つのパレットのみ保持できる場合は場所別在庫限度を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="6388f-137">For example, if some locations within a warehouse can hold only one pallet per location, location stocking limits can be enabled.</span></span> <span data-ttu-id="6388f-138">場所プロファイルのグループでは、**数量** 値は **1** に設定でき、**単位** 値は **PL** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-138">The **Quantity** value can be set to **1**, and the **Unit** value can be set to **PL** within a specific location profile grouping.</span></span> 

<span data-ttu-id="6388f-139">場所の能力制約を制御するためにより高度な計算が必要な場合、場所プロファイルの設定を使用できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-139">If more advanced calculations are required to control the location capacity constraints, the location profile settings can be used.</span></span> <span data-ttu-id="6388f-140">この場合、能力計算を実行すると、重量および容積が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="6388f-140">In this case, the weight and volume are considered when capacity calculations are done.</span></span> 

<span data-ttu-id="6388f-141">最適な出荷プロセスを達成するには、固定のピッキング場所または梱包場所を使用するかどうか評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6388f-141">To achieve optimal outbound processes, you should evaluate whether to use fixed picking locations and/or packing locations.</span></span> <span data-ttu-id="6388f-142">多くの場合、最小/最大の補充がバルク領域から固定のピッキング場所への補充プロセスに使用され、複数の固定のピッキング場所は同じ倉庫内および製品バリアントに対して有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6388f-142">Often, minimum/maximum replenishment is used for replenishment processes from a bulk area to the fixed picking locations, and multiple fixed picking locations can be enabled within the same warehouse and for product variants.</span></span> <span data-ttu-id="6388f-143">ウェーブ/積荷補充プロセスで使用される専用の要求補充のオーバーフローの場所を有効にして達成できる柔軟性を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="6388f-143">Consider the flexibility that can you achieve by enabling dedicated demand replenishment overflow locations that are used only for wave/load replenishment processing.</span></span>

### <a name="location-setup-wizard"></a><span data-ttu-id="6388f-144">場所設定ウィザード</span><span class="sxs-lookup"><span data-stu-id="6388f-144">Location setup wizard</span></span>

<span data-ttu-id="6388f-145">倉庫内の場所をすばやく作成するには、**場所設定** ウィザードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-145">To quickly create the locations within a warehouse, you can use the **Location setup** wizard.</span></span> <span data-ttu-id="6388f-146">このプロセスの一部として、場所の名前の形式を簡単に維持できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-146">As part of this process, you can easily maintain the format of the location names.</span></span>

## <a name="warehouse-processes"></a><span data-ttu-id="6388f-147">倉庫プロセス</span><span class="sxs-lookup"><span data-stu-id="6388f-147">Warehouse processes</span></span>
<span data-ttu-id="6388f-148">倉庫のコンフィギュレーションの一部として、業務要件に基づいて倉庫プロセスを有効にすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="6388f-148">As part of the configuration of the warehouse, it's important that you enable warehouse processes according to business requirements.</span></span> <span data-ttu-id="6388f-149">コンフィギュレーションする必要がある最も重要なコンポーネントは、ウェーブ テンプレート、作業テンプレート、作業プールと場所のディレクティブです。</span><span class="sxs-lookup"><span data-stu-id="6388f-149">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="6388f-150">ウェーブ テンプレート</span><span class="sxs-lookup"><span data-stu-id="6388f-150">Wave templates</span></span>

<span data-ttu-id="6388f-151">ウェーブ テンプレートは、出荷の"倉庫にリリース" プロセスを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="6388f-151">Wave templates help enable the outbound "Release to warehouse" process.</span></span> <span data-ttu-id="6388f-152">注文明細行がリリース (元伝票から直接、またはバッチ ジョブのプロセスから、または既に作成されている積荷から) された時点で、ウェーブ テンプレートの機能が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6388f-152">As soon as order lines are released (either directly from source documents, via batch job processes, or via loads that have already been created), the wave template functionality is used.</span></span> 

<span data-ttu-id="6388f-153">3 つのタイプのウェーブ テンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-153">You can create three types of wave templates:</span></span> 
-   <span data-ttu-id="6388f-154">**出荷**</span><span class="sxs-lookup"><span data-stu-id="6388f-154">**Shipping**</span></span>
-   <span data-ttu-id="6388f-155">**製造オーダー**</span><span class="sxs-lookup"><span data-stu-id="6388f-155">**Production order**</span></span>
-   <span data-ttu-id="6388f-156">**かんばん**</span><span class="sxs-lookup"><span data-stu-id="6388f-156">**Kanban**</span></span> 

<span data-ttu-id="6388f-157">パラメーターはシステムが出荷作業プロセスをどの程度自動的に処理するかの定義にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="6388f-157">Parameters are used to define how far the system should automatically go in the outbound work processing.</span></span> <span data-ttu-id="6388f-158">ウェーブ テンプレートはウェーブ テンプレートの順序と、テンプレートに指定された基準に基づいて選択されます。</span><span class="sxs-lookup"><span data-stu-id="6388f-158">A wave template is selected based on the wave template sequence and criteria that are specified in the template.</span></span> <span data-ttu-id="6388f-159">テンプレートが順序の上部に表示されている場合、テンプレートの基準が先にチェックされます。</span><span class="sxs-lookup"><span data-stu-id="6388f-159">If a template is listed at the top of the sequence, the criteria in that template are checked first.</span></span> <span data-ttu-id="6388f-160">基準を満たすことができれば、ウェーブ テンプレートが処理されます。</span><span class="sxs-lookup"><span data-stu-id="6388f-160">If the criteria can be met, the wave template is processed.</span></span> <span data-ttu-id="6388f-161">それ以外の場合は、次のテンプレートの基準がチェックなどが行われます。</span><span class="sxs-lookup"><span data-stu-id="6388f-161">Otherwise, the criteria in the next template are checked, and so on.</span></span> <span data-ttu-id="6388f-162">したがって、最も限定的な基準を持つテンプレートを、最初に処理されるようにウェーブ テンプレートの順序リストの先頭に設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6388f-162">Therefore, it's a good idea to put the template that has the most specific criteria at the top of the wave template sequence list, so that it's processed first.</span></span> <span data-ttu-id="6388f-163">たとえば、特定の配送業者のすべての作業を今日処理するため、一時的に他の配送業者の作業の処理を遅らせるとします。</span><span class="sxs-lookup"><span data-stu-id="6388f-163">For example, you want to process all the work for a specific carrier today and temporarily delay processing of the work for other carriers.</span></span> <span data-ttu-id="6388f-164">この場合、その配送業者の作業を選択するウェーブ テンプレートは、他のテンプレートより上の順序に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6388f-164">In this case, the wave template that selects work for that carrier should be listed higher in the sequence than other templates.</span></span> <span data-ttu-id="6388f-165">それ以外の場合は、その配送業者の作業の完了前に、他の配送業者の作業が処理されることがあります。</span><span class="sxs-lookup"><span data-stu-id="6388f-165">Otherwise, the work for other carriers might be processed before the work for that carrier is completed.</span></span> 

<span data-ttu-id="6388f-166">各ウェーブ テンプレートにウェーブのプロセス方法を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6388f-166">You must specify the wave process methods in each wave template.</span></span> <span data-ttu-id="6388f-167">使用できる方法は、ウェーブ テンプレート タイプによって変わります。</span><span class="sxs-lookup"><span data-stu-id="6388f-167">The methods that are available vary, depending on the wave template type.</span></span>

### <a name="work-templates"></a><span data-ttu-id="6388f-168">作業テンプレート</span><span class="sxs-lookup"><span data-stu-id="6388f-168">Work templates</span></span>

<span data-ttu-id="6388f-169">作業テンプレートの定義は、倉庫管理作業プロセスの定義において重要な役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="6388f-169">Work template definitions play an important role in the definition of warehouse management work processes.</span></span> <span data-ttu-id="6388f-170">どの作業が実行されるか、および作業方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="6388f-170">They define what work is performed, and how the work is done.</span></span> <span data-ttu-id="6388f-171">テンプレートは、作業がどこで実行するかを決定する場所のディレクティブにリンクするディレクティブ コードを含むことができます。</span><span class="sxs-lookup"><span data-stu-id="6388f-171">Templates can also contain a directive code that links to a location directive to determine where work is performed.</span></span> <span data-ttu-id="6388f-172">作業テンプレートには、作業の基準を指定するクエリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6388f-172">Work templates include a query that specifies the criteria for the work.</span></span> <span data-ttu-id="6388f-173">各テンプレートは、少なくとも 1 つのピッキング工程と、手持在庫をある場所から別の場所に移動させる基本的な作業をドライブする 1 つのプット工程を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6388f-173">Each template must include at least one Pick operation and one Put operation to drive the basic work operation of transferring on-hand inventory from one location to another.</span></span> 

<span data-ttu-id="6388f-174">複数の作業者が倉庫工程の一部を処理できるようにするに、在庫に *ステージング* 概念を使用して、さまざまな作業のクラスに作業実行を分割する場合があります。</span><span class="sxs-lookup"><span data-stu-id="6388f-174">If multiple workers must be able to process work for some of your warehouse operations, you might want to use the concept of *staging* for the inventory and separate the work execution into different work classes.</span></span>

### <a name="work-pools"></a><span data-ttu-id="6388f-175">作業プール</span><span class="sxs-lookup"><span data-stu-id="6388f-175">Work pools</span></span>

<span data-ttu-id="6388f-176">作業プールは、作業をグループに整理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6388f-176">Work pools are used to organize work into groups.</span></span> <span data-ttu-id="6388f-177">たとえば、特定の倉庫の場所に発生する作業を分類する作業プールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-177">For example, you can create a work pool to classify work that occurs in a particular warehouse location.</span></span> <span data-ttu-id="6388f-178">棚卸以外のすべての作業タイプについて、作業プールを作業テンプレートに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6388f-178">For all work types except counting, you can assign a work pool to a work template.</span></span> <span data-ttu-id="6388f-179">循環棚卸の場合、次のページに作業プールを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6388f-179">For cycle counting, you can assign a work pool on the following pages:</span></span>

-   <span data-ttu-id="6388f-180">循環棚卸計画</span><span class="sxs-lookup"><span data-stu-id="6388f-180">Cycle count plans</span></span>
-   <span data-ttu-id="6388f-181">循環棚卸のしきい値</span><span class="sxs-lookup"><span data-stu-id="6388f-181">Cycle count thresholds</span></span>
-   <span data-ttu-id="6388f-182">場所別循環棚卸作業</span><span class="sxs-lookup"><span data-stu-id="6388f-182">Cycle count work by location</span></span>
-   <span data-ttu-id="6388f-183">品目別循環棚卸作業</span><span class="sxs-lookup"><span data-stu-id="6388f-183">Cycle count work by item</span></span>

<span data-ttu-id="6388f-184">作業テンプレートを使用して作業を作成するとき、作業プールが作業に自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6388f-184">When you use work templates to create work, the work pool is automatically assigned to the work.</span></span> 

<span data-ttu-id="6388f-185">作業プールIDは、関連するモバイル デバイスのメニュー項目でコンフィギュレーションされている場合、特定の倉庫の作業者に指示される作業のタイプを制限するのにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-185">Work pool IDs can also be used to limit the type of work that is directed to a particular warehouse worker, provided that this functionality is configured on the relevant mobile device menu item.</span></span>

### <a name="location-directives"></a><span data-ttu-id="6388f-186">場所のディレクティブ</span><span class="sxs-lookup"><span data-stu-id="6388f-186">Location directives</span></span>

<span data-ttu-id="6388f-187">名前が示すとおり、倉庫の適切な位置に作業トランザクションを指示するために場所のディレクティブが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6388f-187">As the name suggests, location directives are used to direct the work transactions to the appropriate locations in the warehouse.</span></span> <span data-ttu-id="6388f-188">つまり、どこでピッキングとプットされるかが定義されます。</span><span class="sxs-lookup"><span data-stu-id="6388f-188">In other words, they define where to pick and put.</span></span> 

<span data-ttu-id="6388f-189">場所ディレクティブの明細行と関連付けられるアクションの定義をすばやく、容易にするには、事前に定義された戦略の 1 つを使用します。</span><span class="sxs-lookup"><span data-stu-id="6388f-189">To make it easier and quicker to define the actions that are associated with each location directive line, use one of the predefined strategies.</span></span> <span data-ttu-id="6388f-190">たとえば、**作業を受け取らない空の場所** 戦略を使用して倉庫の空いている場所を検索したり、出荷販売ピッキングに対して **FEFO バッチ引当** 戦略を使用できます。</span><span class="sxs-lookup"><span data-stu-id="6388f-190">For example, you can use the **Empty location with no incoming work** strategy to search for free locations in a warehouse, or you can use **FEFO batch reservation** strategy for outbound sales picking.</span></span>

<a name="additional-resources"></a><span data-ttu-id="6388f-191">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6388f-191">Additional resources</span></span>
--------

[<span data-ttu-id="6388f-192">WMS に対応した倉庫の場所のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6388f-192">Configure locations in a WMS-enabled warehouse</span></span>](tasks/configure-locations-wms-enabled-warehouse.md)



