---
title: 数量がゼロであるため、出荷を確認できない
description: 数量がゼロであるため、出荷を確認できない
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938503"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="beb6f-103">数量がゼロであるため、出荷を確認できない</span><span class="sxs-lookup"><span data-stu-id="beb6f-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="beb6f-104">エラー コード: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="beb6f-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="beb6f-105">現象</span><span class="sxs-lookup"><span data-stu-id="beb6f-105">Symptoms</span></span>

<span data-ttu-id="beb6f-106">出荷を確認しようとすると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="beb6f-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="beb6f-107">品目 %1 および出荷 %2 の積荷明細行は、配送不足の設定が原因で数量が 0 に更新されており、この品目の数量は出荷できません。</span><span class="sxs-lookup"><span data-stu-id="beb6f-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="beb6f-108">したがって、積荷の出荷を確認できません。</span><span class="sxs-lookup"><span data-stu-id="beb6f-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="beb6f-109">原因</span><span class="sxs-lookup"><span data-stu-id="beb6f-109">Cause</span></span>

<span data-ttu-id="beb6f-110">システムでは、ピッキング済数量、積荷明細行数量、および過少配送率に基づいて、ピッキング済数量が予想制限内かどうかが評価されます。</span><span class="sxs-lookup"><span data-stu-id="beb6f-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="beb6f-111">積荷明細行のピッキング済数量が 0 (ゼロ) である場合は、出荷を確認できません。</span><span class="sxs-lookup"><span data-stu-id="beb6f-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="beb6f-112">たとえば、作業がキャンセルされ、積荷明細行の過少配送率が 100% の場合、この問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="beb6f-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="beb6f-113">解像度</span><span class="sxs-lookup"><span data-stu-id="beb6f-113">Resolution</span></span>

<span data-ttu-id="beb6f-114">過少配送率と数量がピッキング済作業と一致するよう、積荷明細行を確認します。</span><span class="sxs-lookup"><span data-stu-id="beb6f-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="beb6f-115">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="beb6f-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="beb6f-116">発送が確認できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="beb6f-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="beb6f-117">**積荷明細行** クイック タブで、過少配送率を超える品目の積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="beb6f-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="beb6f-118">必要に応じて、**過少配送** フィールドまたは **数量** フィールドの値を調整します。</span><span class="sxs-lookup"><span data-stu-id="beb6f-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="beb6f-119">それでも問題が解決しない場合は、利用可能な数量が積荷または出荷に一致するまで、関連する販売注文または移動オーダーに対してピッキング作業を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="beb6f-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
