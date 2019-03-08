---
title: 在庫場所
description: 在庫場所は、品目の保存場所、および WMS I 倉庫で品目がピッキングされる場所を特定するために基本倉庫 (WMS I) で使用されます。
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 789272e1ee02c7f5dbab4e325cefe56425a3d1a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "350806"
---
# <a name="inventory-locations"></a><span data-ttu-id="c62fe-103">在庫場所</span><span class="sxs-lookup"><span data-stu-id="c62fe-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c62fe-104">在庫場所は、品目の保存場所、および WMS I 倉庫で品目がピッキングされる場所を特定するために基本倉庫 (WMS I) で使用されます。</span><span class="sxs-lookup"><span data-stu-id="c62fe-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="c62fe-105">このトピックは、在庫管理モジュールの機能に適用されます。</span><span class="sxs-lookup"><span data-stu-id="c62fe-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="c62fe-106">これは、倉庫管理モジュールの機能には適用されません。</span><span class="sxs-lookup"><span data-stu-id="c62fe-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="c62fe-107">場所という用語は、品目が保管され、取得元となる場所を意味します。</span><span class="sxs-lookup"><span data-stu-id="c62fe-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="c62fe-108">各在庫場所に対し、品目の挿入先も指定できます。</span><span class="sxs-lookup"><span data-stu-id="c62fe-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="c62fe-109">既定では、どちらも同じです。</span><span class="sxs-lookup"><span data-stu-id="c62fe-109">By default, they are the same.</span></span> <span data-ttu-id="c62fe-110">通常、品目の挿入と取り出しが行われるのは在庫場所の同じ側ですが、常にそうであるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="c62fe-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="c62fe-111">たとえば、常用保管ラックに格納される品目は、一方の通路から挿入されて、別の通路から取り出されます。</span><span class="sxs-lookup"><span data-stu-id="c62fe-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="c62fe-112">主な入力は、倉庫、通路、ラック、棚、および在庫置場などの座標によって決まる場所の名前で指定されます。</span><span class="sxs-lookup"><span data-stu-id="c62fe-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="c62fe-113">この名前または ID は、手動で入力することも、[在庫場所] ページの保管場所の座標から生成することもできます。たとえば、通路 1、ラック 2、棚 3、在庫置場 4 という座標の場合、ID は 01-02-03-4 になります。</span><span class="sxs-lookup"><span data-stu-id="c62fe-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="c62fe-114">在庫場所のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c62fe-114">Location properties</span></span>

<span data-ttu-id="c62fe-115">在庫場所には次のような特性があります。</span><span class="sxs-lookup"><span data-stu-id="c62fe-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="c62fe-116">サイズ (高さ、幅、奥行き、およびこれらによる体積)</span><span class="sxs-lookup"><span data-stu-id="c62fe-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="c62fe-117">倉庫、通路、ラック、棚、在庫置場の位置</span><span class="sxs-lookup"><span data-stu-id="c62fe-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="c62fe-118">場所タイプ (バルク場所、ピッキング場所、入荷ドック、出荷ドック、生産入力の場所、検査場所、かんばんスーパーマーケット)</span><span class="sxs-lookup"><span data-stu-id="c62fe-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="c62fe-119">オンライン システムでチェック テキストを使用すると、オペレータが特定の品目に対して正しい在庫場所を選択したかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c62fe-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="c62fe-120">このチェック テキストは手動で作成することも、既定で作成されるようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c62fe-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="c62fe-121">並べ替えコード</span><span class="sxs-lookup"><span data-stu-id="c62fe-121">Sort codes</span></span>
<span data-ttu-id="c62fe-122">並べ替えコードは、在庫からの品目のピッキングに必要な情報 (バルク オーダーなど) を示すもので、このコードを使用してピッキング ラインの処理を最適化できます。</span><span class="sxs-lookup"><span data-stu-id="c62fe-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="c62fe-123">並べ替えコードは、通路やその他の座標にで指定できるほか、場所に対して手動で割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="c62fe-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="c62fe-124">ブロックされた在庫場所</span><span class="sxs-lookup"><span data-stu-id="c62fe-124">Blocked locations</span></span>
<span data-ttu-id="c62fe-125">たとえば、修理などのために、在庫場所が一時的にブロックされていることを示す必要が生じることがあります。</span><span class="sxs-lookup"><span data-stu-id="c62fe-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="c62fe-126">他には、入力または出力のいずれか一方のみがブロックされていることを表示したい場合もあります。</span><span class="sxs-lookup"><span data-stu-id="c62fe-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="c62fe-127">ツリー構造</span><span class="sxs-lookup"><span data-stu-id="c62fe-127">Tree structure</span></span>

<span data-ttu-id="c62fe-128">[在庫場所] ページでは、倉庫のレイアウトを、在庫場所の座標に基づいて、設定した形式でツリー構造で表示できます。</span><span class="sxs-lookup"><span data-stu-id="c62fe-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="c62fe-129">倉庫フォームで在庫場所を管理</span><span class="sxs-lookup"><span data-stu-id="c62fe-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="c62fe-130">1 つの倉庫から別の倉庫に場所をコピーし、ウィザードによって場所を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="c62fe-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="c62fe-131">ウィザードを実行する前に、[倉庫] ページで既定の場所の名前を定義してあることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c62fe-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="c62fe-132">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="c62fe-132">Additional resources</span></span>
--------

[<span data-ttu-id="c62fe-133">新しい倉庫レイアウトの作成 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="c62fe-133">Create a new warehouse layout (Task guide)</span></span>](tasks/create-new-warehouse-layout.md)
