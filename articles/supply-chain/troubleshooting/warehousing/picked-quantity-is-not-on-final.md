---
title: 品目がピッキングされていないため、出荷を確認できない
description: 品目がピッキングされていないため、出荷を確認できない
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938504"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="75b1c-103">品目がピッキングされていないため、出荷を確認できない</span><span class="sxs-lookup"><span data-stu-id="75b1c-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="75b1c-104">エラー コード: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="75b1c-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="75b1c-105">現象</span><span class="sxs-lookup"><span data-stu-id="75b1c-105">Symptoms</span></span>

<span data-ttu-id="75b1c-106">出荷を確認しようとすると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="75b1c-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="75b1c-107">積荷 %1 に必要な一部の品目がまだピッキングされておらず、最終出荷場所に移動されていません。</span><span class="sxs-lookup"><span data-stu-id="75b1c-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="75b1c-108">したがって、積荷の出荷を確認できません。</span><span class="sxs-lookup"><span data-stu-id="75b1c-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="75b1c-109">原因</span><span class="sxs-lookup"><span data-stu-id="75b1c-109">Cause</span></span>

<span data-ttu-id="75b1c-110">次のいずれかの条件が存在する可能性があるため、現在の状態では積荷または出荷を確認できません:</span><span class="sxs-lookup"><span data-stu-id="75b1c-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="75b1c-111">関連する作業がまだ選択されていないので、最終的な出荷場所に移動されていません。</span><span class="sxs-lookup"><span data-stu-id="75b1c-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="75b1c-112">作業のピッキング済数量が、積荷明細行で作成された作業数量と一致しません。</span><span class="sxs-lookup"><span data-stu-id="75b1c-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="75b1c-113">解像度</span><span class="sxs-lookup"><span data-stu-id="75b1c-113">Resolution</span></span>

<span data-ttu-id="75b1c-114">積荷または出荷用の関連する販売注文または移動オーダーを確認します。</span><span class="sxs-lookup"><span data-stu-id="75b1c-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="75b1c-115">関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="75b1c-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="75b1c-116">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="75b1c-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="75b1c-117">発送が確認できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="75b1c-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="75b1c-118">**積荷明細行** クイックタブで、積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="75b1c-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="75b1c-119">**作業作成数量** フィールドの値を記録します。</span><span class="sxs-lookup"><span data-stu-id="75b1c-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="75b1c-120">アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。</span><span class="sxs-lookup"><span data-stu-id="75b1c-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="75b1c-121">作業が最後の出荷場所で完了し、作業のピッキング済数量が積荷明細行で作成された作業数量と一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="75b1c-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="75b1c-122">すべての積荷明細行に対してこの手順を繰り返して、すべての基準が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="75b1c-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
