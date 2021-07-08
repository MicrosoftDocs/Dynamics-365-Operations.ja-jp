---
title: 梱包明細の生成中に数量が過少配送率を超えている場合
description: 梱包明細を生成すると、出庫積荷に過少配送率を超える数量が含まれます。
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249128"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="ffd4e-103">梱包明細の生成中に数量が過少配送率を超えている場合</span><span class="sxs-lookup"><span data-stu-id="ffd4e-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="ffd4e-104">エラーコード: SYS24921</span><span class="sxs-lookup"><span data-stu-id="ffd4e-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="ffd4e-105">現象</span><span class="sxs-lookup"><span data-stu-id="ffd4e-105">Symptoms</span></span>

<span data-ttu-id="ffd4e-106">梱包明細を生成すると、出庫積荷に過少配送率を超える数量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="ffd4e-107">梱包明細を生成しようとすると、次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="ffd4e-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="ffd4e-108">ラインの部分納品率は %1 パーセントですが、部分納品許可率は %2 パーセントだけです。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="ffd4e-109">したがって、積荷の梱包明細を生成できません。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="ffd4e-110">原因</span><span class="sxs-lookup"><span data-stu-id="ffd4e-110">Cause</span></span>

<span data-ttu-id="ffd4e-111">積荷または出荷の選択された数量が注文済数量を下回り、過少配送率の範囲内ではありません。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="ffd4e-112">解決策</span><span class="sxs-lookup"><span data-stu-id="ffd4e-112">Resolution</span></span>

<span data-ttu-id="ffd4e-113">積荷または出荷は現在、梱包明細の生成に失敗した状態になっています。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="ffd4e-114">この問題を解決するには、次のいずれかのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="ffd4e-115">過少配送率を調整します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="ffd4e-116">取り消して、調整します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="ffd4e-117">過少配送率を調整する</span><span class="sxs-lookup"><span data-stu-id="ffd4e-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="ffd4e-118">次の手順を使用して、過少配送率を調整します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="ffd4e-119">**売掛金勘定 \> 注文 \> すべての注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="ffd4e-120">積荷の梱包明細を転記できない販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="ffd4e-121"> *\*販売注文明細行** タブで、過少配送率を超える品目の販売注文明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="ffd4e-122"> *\*明細行の詳細** タブで、*\*配送** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="ffd4e-123">**過少配送** フィールドを、積荷数量に対してピッキングされた数量に対応するよりも大きな割合に設定して、梱包明細の生成が続行されるようにします。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="ffd4e-124">取り消して、調整する</span><span class="sxs-lookup"><span data-stu-id="ffd4e-124">Reverse and make adjustments</span></span>

<span data-ttu-id="ffd4e-125">積荷 (梱包明細、出荷確定、作業など) に対して転記されたすべてを取り消し、販売注文の調整を実行し、倉庫への注文を再リリースして、出荷手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="ffd4e-126">次の手順を使用して、梱包明細をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="ffd4e-127">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="ffd4e-128">アクション ウィンドウの、 **出荷と入荷** タブの、 **取消** グループで、 **梱包明細のキャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="ffd4e-129">次の手順を使用して、出荷確定を取り消します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="ffd4e-130">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="ffd4e-131">アクション ウィンドウの、 **出荷と入荷** タブの、 **取消** グループで、 **出荷確定の取消** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="ffd4e-132">次の手順を使用して、作業を取り消します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="ffd4e-133">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="ffd4e-134">アクション ウィンドウの **積荷** タブの、 **作業** グループで、 **作業の取消** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffd4e-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
