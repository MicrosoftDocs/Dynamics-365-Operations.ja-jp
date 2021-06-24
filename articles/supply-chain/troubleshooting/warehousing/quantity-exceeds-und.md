---
title: 数量が過少配送率を超えているため、出荷を確認できない
description: 数量が過少配送率を超えているため、出荷を確認できない
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 625003731485329b93f5f9454ccece580c889613
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123822"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="9f078-103">数量が過少配送率を超えているため、出荷を確認できない</span><span class="sxs-lookup"><span data-stu-id="9f078-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="9f078-104">エラーコード: WAX1686</span><span class="sxs-lookup"><span data-stu-id="9f078-104">Error code: WAX1686</span></span>

## <a name="symptoms"></a><span data-ttu-id="9f078-105">現象</span><span class="sxs-lookup"><span data-stu-id="9f078-105">Symptoms</span></span>

<span data-ttu-id="9f078-106">出荷を確認しようとすると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9f078-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="9f078-107">品目 %2 の数量が過少配送に対して定義されている割合を超えているため、積荷 %1 の出荷を確認できませんでした。</span><span class="sxs-lookup"><span data-stu-id="9f078-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="9f078-108">したがって、積荷の出荷を確認できません。</span><span class="sxs-lookup"><span data-stu-id="9f078-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="9f078-109">原因</span><span class="sxs-lookup"><span data-stu-id="9f078-109">Cause</span></span>

<span data-ttu-id="9f078-110">積荷または出荷の数量は、一部ピッキング済になっています。</span><span class="sxs-lookup"><span data-stu-id="9f078-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="9f078-111">現在、数量が、許容される過少配送率を超える割合で、ピッキング済数量よりも少なくなっています。</span><span class="sxs-lookup"><span data-stu-id="9f078-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="9f078-112">解像度</span><span class="sxs-lookup"><span data-stu-id="9f078-112">Resolution</span></span>

<span data-ttu-id="9f078-113">この問題を解決するには、次のいずれかのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9f078-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="9f078-114">積荷明細行の数量を設定します。</span><span class="sxs-lookup"><span data-stu-id="9f078-114">Set the load line quantity.</span></span>
- <span data-ttu-id="9f078-115">過少配送率を設定します。</span><span class="sxs-lookup"><span data-stu-id="9f078-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="9f078-116">積荷明細行の数量を設定する</span><span class="sxs-lookup"><span data-stu-id="9f078-116">Set the load line quantity</span></span>

<span data-ttu-id="9f078-117">積荷明細行の数量を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9f078-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="9f078-118">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f078-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="9f078-119">発送が確認できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f078-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="9f078-120">**積荷明細行** クイック タブで、過少配送率を超える品目の積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f078-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="9f078-121">**明細行の詳細** クイックタブで、**注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f078-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="9f078-122">**数量** フィールドで、ピッキング済数量 (つまり、**作業作成数量** の値) に設定して、出荷確認が行われるようにします。</span><span class="sxs-lookup"><span data-stu-id="9f078-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="9f078-123">過少配送率の設定</span><span class="sxs-lookup"><span data-stu-id="9f078-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="9f078-124">過少配送率を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9f078-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="9f078-125">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f078-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="9f078-126">発送が確認できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f078-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="9f078-127">**積荷明細行** クイック タブで、過少配送率を超える品目の積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f078-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="9f078-128">**明細行の詳細** クイックタブで、**全般** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f078-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="9f078-129">**過少配送** フィールドで、積荷数量に対してピッキングされた数量に対応するよりも大きな割合に値を設定して、出荷確認を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f078-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
