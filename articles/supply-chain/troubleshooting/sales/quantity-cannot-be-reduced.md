---
title: 販売注文がキャンセルされたとき、数量を削減できない
description: 販売注文がキャンセルされたとき、数量を削減できません。
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230839"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="b20bf-103">販売注文がキャンセルされたとき、数量を削減できない</span><span class="sxs-lookup"><span data-stu-id="b20bf-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="b20bf-104">エラーコード: SYS138831</span><span class="sxs-lookup"><span data-stu-id="b20bf-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="b20bf-105">現象</span><span class="sxs-lookup"><span data-stu-id="b20bf-105">Symptoms</span></span>

<span data-ttu-id="b20bf-106">システムは次のエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-106">The system shows the following error message:</span></span>

> <span data-ttu-id="b20bf-107">数量を減らすことができません。</span><span class="sxs-lookup"><span data-stu-id="b20bf-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="b20bf-108">数量またはその一部が出荷注文または製造オーダーによって参照されたり、他のトランザクションに対してマークされている可能性があるため、注文中の在庫トランザクションの数が少なすぎます。</span><span class="sxs-lookup"><span data-stu-id="b20bf-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="b20bf-109">原因</span><span class="sxs-lookup"><span data-stu-id="b20bf-109">Cause</span></span>

<span data-ttu-id="b20bf-110">作業が販売注文に関連付けられている場合、その作業がキャンセルされて取り消されるまで、販売注文をキャンセルすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b20bf-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="b20bf-111">この要件は、販売注文に関連付けられている作業が終了されている場合にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="b20bf-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="b20bf-112">解決策</span><span class="sxs-lookup"><span data-stu-id="b20bf-112">Resolution</span></span>

<span data-ttu-id="b20bf-113">この問題を解決するには、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="b20bf-114">オープン作業をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="b20bf-114">Cancel open work.</span></span>
1. <span data-ttu-id="b20bf-115">負荷を削除します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-115">Delete the load.</span></span>
1. <span data-ttu-id="b20bf-116">ピッキング済み数量を削減します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="b20bf-117">オープン作業をキャンセルする</span><span class="sxs-lookup"><span data-stu-id="b20bf-117">Cancel open work</span></span>

<span data-ttu-id="b20bf-118">オープン作業をキャンセルするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b20bf-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="b20bf-119">**倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="b20bf-120">**作業 ID** フィールドで、キャンセルする作業の ID を指定します。現在、**作業状態** の値は、*未処理*、*進行中*、*キャンセル済*、*結合済*、または *終了済* です。</span><span class="sxs-lookup"><span data-stu-id="b20bf-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="b20bf-121">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-121">Select **OK**.</span></span>
1. <span data-ttu-id="b20bf-122">**はい** を選択して、作業をキャンセルすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="b20bf-123">積荷を削除する</span><span class="sxs-lookup"><span data-stu-id="b20bf-123">Delete the load</span></span>

<span data-ttu-id="b20bf-124">積荷を削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b20bf-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="b20bf-125">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b20bf-126">関連する販売注文を開きます。</span><span class="sxs-lookup"><span data-stu-id="b20bf-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="b20bf-127">**販売注文明細行** クイック タブで、**倉庫 \> 作業の詳細s** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="b20bf-128">**作業** ページで、[アクション ペイン] の **作業** タブの **作業** グループで、**作業のキャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="b20bf-129">**作業ステータス** フィールドが *キャンセル済* に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="b20bf-130">**作業** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b20bf-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="b20bf-131">販売注文の詳細ページの **販売注文明細行** クイック タブで、**倉庫 \> 積荷の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="b20bf-132">アクション ウィンドウで **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="b20bf-133">**はい** を選択して、積荷を削除することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="b20bf-134">**積荷** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b20bf-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="b20bf-135">ピッキング済み数量を減らす</span><span class="sxs-lookup"><span data-stu-id="b20bf-135">Reduce the picked quantity</span></span>

<span data-ttu-id="b20bf-136">すべての作業をキャンセルした後は、次の手順に従って、選択した数量を減らします。</span><span class="sxs-lookup"><span data-stu-id="b20bf-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="b20bf-137">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b20bf-138">関連する販売注文を開きます。</span><span class="sxs-lookup"><span data-stu-id="b20bf-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="b20bf-139">**販売注文明細行** クイック タブで、ツール バーから **行の更新\>ピッキング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="b20bf-140">**ピッキング** ページの **トランザクション** セクションで、**出庫ステータス** フィールドが *ピッキング済* に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="b20bf-141">**トランザクション** セクションで、ツール バーから **ピッキング ラインの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="b20bf-142">**ピッキング ライン** セクションで、ツール バーから **すべてのピッキングを確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="b20bf-143">**ピッキング** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b20bf-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="b20bf-144">販売注文明細ページの [アクション ペイン] の **販売注文** タブで、**メンテナンス** グループの **キャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="b20bf-145">**はい** を選択して、販売注文をキャンセルすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b20bf-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
