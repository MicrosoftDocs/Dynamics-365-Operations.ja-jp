---
title: "倉庫管理における作業が関連付けられている在庫の移動"
description: "このトピックでは、モバイル デバイスからピース ピッキングの確認を設定して適用する方法について説明します。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7b330d6aa8e972d3c35bb7783ec0a39f09775011
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="dc9d6-103">倉庫管理における作業が関連付けられている在庫の移動</span><span class="sxs-lookup"><span data-stu-id="dc9d6-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dc9d6-104">在庫移動を使用すると、引当済の在庫を移動することが許可されている倉庫作業者を指定できます。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="dc9d6-105">これにより、作業者が既に作成されているピッキング作業に対して新しいピッキング場所を選択できないように規制している倉庫内での柔軟性が実現します。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="dc9d6-106">また、倉庫マネージャーは、経験の浅い従業員がどの機能を管理するかを制御できます。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="dc9d6-107">倉庫作業者の日常的な工程を管理する柔軟性は、このような場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="dc9d6-108">シナリオ 1</span><span class="sxs-lookup"><span data-stu-id="dc9d6-108">Scenario 1</span></span>
<span data-ttu-id="dc9d6-109">会社は比較的小さな入庫エリアを所有しており、待機中のパレットとボックスで混雑しています。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="dc9d6-110">当日は大量の出荷が予定されているため、入荷係はパレットの一部を二次受信ステージング エリアに移動させて入庫エリアをクリアすることを決定します。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="dc9d6-111">シナリオ 2</span><span class="sxs-lookup"><span data-stu-id="dc9d6-111">Scenario 2</span></span>
<span data-ttu-id="dc9d6-112">経験のある倉庫作業員は、倉庫内の機会に気づいて、3 つの近隣の場所に少ない数量でそれぞれに分割するのではなく、1 つの場所に統合できます。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="dc9d6-113">作業者は、これらの場所からそれぞれを同じ場所およびナンバープレート上に物品を移動することによって数量を集約したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="dc9d6-114">シナリオ 3</span><span class="sxs-lookup"><span data-stu-id="dc9d6-114">Scenario 3</span></span>
<span data-ttu-id="dc9d6-115">パレットは BAYDOOR01 の近くにある STAGE01 などのステージング場所で出荷を待機しています。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="dc9d6-116">計画の変更によりトラックは BAYDOOR04 に到着する予定です。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="dc9d6-117">出荷係はこれを認識しており、トラックが STAGE01 から積み込まれるのを待つ必要がないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="dc9d6-118">出荷係は、STAGE01 から新しい目的地に近い STAGE04 へその品目を移動することを指定します。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="dc9d6-119">現在の制限</span><span class="sxs-lookup"><span data-stu-id="dc9d6-119">Current limitations</span></span>

<span data-ttu-id="dc9d6-120">移動ができる作業引当は、販売注文、移動オーダーの出庫、移動オーダーの入庫、発注書、および補充作業に限定されます。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="dc9d6-121">移動する品目は、作業明細行が分割されないように制限されています。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="dc9d6-122">これは、Loc1 から 100 個ある品目 A の作業ラインがある場合、そこから 30 個ある品目 A のみを別の場所に移動することはできないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="dc9d6-123">これにより、場所が異なるため、既存の作業明細行は 30 と 70 に分割されるようになります。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="dc9d6-124">ステージング シナリオでは、商品を移動させるライセンス プレート、または商品を移動するライセンス プレートは、ワーク オーダーのターゲット LP として設定され、LP 全体の移動のみが許可されるため、ターゲット LP は分割されません。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="dc9d6-125">アド ホック振替のみが現在サポートされています。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="dc9d6-126">テンプレート モバイル デバイスのメニュー項目で、移動により引当済の在庫を移動できなくなることを意味します。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="dc9d6-127">個々の作業者の引当済の在庫を移動するためのアクセス許可を設定します。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="dc9d6-128">引当済の在庫移動を許可されている作業者については、[**倉庫管理**] > [**設定**] > [**作業者**] の順に移動して、[**関連付けられている作業で在庫移動を許可する**] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="dc9d6-129">バックポート済み</span><span class="sxs-lookup"><span data-stu-id="dc9d6-129">Backported</span></span>

<span data-ttu-id="dc9d6-130">この機能も Microsoft Dynamics AX 2012 R3 にバックポートされているため、CU12 の一部として利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="dc9d6-131">KB 番号 3192548 を通じて個別にダウンロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="dc9d6-131">It can also be downloaded individually through KB number 3192548.</span></span> 


