---
title: 倉庫管理における作業が関連付けられている在庫の移動
description: 在庫移動を使用すると、引当済の在庫を移動することが許可されている倉庫作業者を指定できます。
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6477a91b3c65e8be5ab527eaff12c92ae7918b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808753"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="94abe-103">倉庫管理における作業が関連付けられている在庫の移動</span><span class="sxs-lookup"><span data-stu-id="94abe-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94abe-104">在庫移動を使用すると、引当済の在庫を移動することが許可されている倉庫作業者を指定できます。</span><span class="sxs-lookup"><span data-stu-id="94abe-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="94abe-105">これにより、作業者が既に作成されているピッキング作業に対して新しいピッキング場所を選択できないように規制している倉庫内での柔軟性が実現します。</span><span class="sxs-lookup"><span data-stu-id="94abe-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="94abe-106">また、倉庫マネージャーは、経験の浅い従業員がどの機能を管理するかを制御できます。</span><span class="sxs-lookup"><span data-stu-id="94abe-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="94abe-107">倉庫作業者の日常的な工程を管理する柔軟性は、このような場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="94abe-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="94abe-108">シナリオ 1</span><span class="sxs-lookup"><span data-stu-id="94abe-108">Scenario 1</span></span>

<span data-ttu-id="94abe-109">会社は比較的小さな入庫エリアを所有しており、待機中のパレットとボックスで混雑しています。</span><span class="sxs-lookup"><span data-stu-id="94abe-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="94abe-110">当日は大量の出荷が予定されているため、入荷係はパレットの一部を二次受信ステージング エリアに移動させて入庫エリアをクリアすることを決定します。</span><span class="sxs-lookup"><span data-stu-id="94abe-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="94abe-111">シナリオ 2</span><span class="sxs-lookup"><span data-stu-id="94abe-111">Scenario 2</span></span>

<span data-ttu-id="94abe-112">経験豊富な倉庫作業員は、倉庫内の商品を近くの3箇所に分けて少量ずつ置くのではなく、1箇所にまとめる機会に気付きました。</span><span class="sxs-lookup"><span data-stu-id="94abe-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across three nearby locations with little quantity on each.</span></span> <span data-ttu-id="94abe-113">作業者は、これらの場所からそれぞれを同じ場所およびナンバープレート上に物品を移動することによって数量を集約したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="94abe-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="94abe-114">シナリオ 3</span><span class="sxs-lookup"><span data-stu-id="94abe-114">Scenario 3</span></span>

<span data-ttu-id="94abe-115">パレットは BAYDOOR01 の近くにある STAGE01 などのステージング場所で出荷を待機しています。</span><span class="sxs-lookup"><span data-stu-id="94abe-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="94abe-116">計画の変更によりトラックは BAYDOOR04 に到着する予定です。</span><span class="sxs-lookup"><span data-stu-id="94abe-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="94abe-117">出荷係はこれを認識しており、トラックが STAGE01 から積み込まれるのを待つ必要がないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94abe-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="94abe-118">出荷係は、STAGE01 から新しい目的地に近い STAGE04 へその品目を移動することを指定します。</span><span class="sxs-lookup"><span data-stu-id="94abe-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="94abe-119">現在の制限</span><span class="sxs-lookup"><span data-stu-id="94abe-119">Current limitations</span></span>

<span data-ttu-id="94abe-120">移動ができる作業引当は、販売注文、移動オーダーの出庫、移動オーダーの入庫、発注書、および補充作業に限定されます。</span><span class="sxs-lookup"><span data-stu-id="94abe-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="94abe-121">移動する品目は、作業明細行が分割されないように制限されています。</span><span class="sxs-lookup"><span data-stu-id="94abe-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="94abe-122">これは、Loc1 から 100 個ある品目 A の作業ラインがある場合、そこから 30 個ある品目 A のみを別の場所に移動することはできないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="94abe-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="94abe-123">これにより、場所が異なるため、既存の作業明細行は 30 と 70 に分割されるようになります。</span><span class="sxs-lookup"><span data-stu-id="94abe-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="94abe-124">ステージング シナリオでは、商品を移動させるライセンス プレート、または商品を移動するライセンス プレートは、ワーク オーダーのターゲット LP として設定され、LP 全体の移動のみが許可されるため、ターゲット LP は分割されません。</span><span class="sxs-lookup"><span data-stu-id="94abe-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>

<span data-ttu-id="94abe-125">アド ホック振替のみが現在サポートされています。</span><span class="sxs-lookup"><span data-stu-id="94abe-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="94abe-126">テンプレート モバイル デバイスのメニュー項目で、移動により引当済の在庫を移動できなくなることを意味します。</span><span class="sxs-lookup"><span data-stu-id="94abe-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="94abe-127">個々の作業者の引当済の在庫を移動するためのアクセス許可を設定します。</span><span class="sxs-lookup"><span data-stu-id="94abe-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="94abe-128">引当済の在庫の移動を許可されている作業者については、**倉庫管理 \> 設定 \> 作業者** の **作業に関連した在庫の移動を許可する** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="94abe-128">For the worker who is allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management \> Setup \> Worker**.</span></span>  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
