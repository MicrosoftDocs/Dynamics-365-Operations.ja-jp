---
title: 個別製造のトラブルシューティング
description: このトピックでは、個別製造を操作する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b0073cb2c3e3d6b9218caf20c394c8c0ca67b796
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966208"
---
# <a name="troubleshoot-discrete-manufacturing"></a><span data-ttu-id="3350c-103">個別製造のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="3350c-103">Troubleshoot discrete manufacturing</span></span>

<span data-ttu-id="3350c-104">このトピックでは、個別製造を操作する際に発生する可能性がある問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3350c-104">This topic describes how to fix issues that you might encounter while you work with discrete manufacturing.</span></span>

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a><span data-ttu-id="3350c-105">エラー メッセージ "倉庫管理プロセスは現在使用中です。</span><span class="sxs-lookup"><span data-stu-id="3350c-105">I receive the following error message: "Warehouse management processes are currently being used.</span></span> <span data-ttu-id="3350c-106">作業明細行がまだ登録されていない場合は、作成した作業をキャンセルし、すべての貨物または出荷明細行をキャンセルして、ピッキングまたは出荷プロセスを続行することができます" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-106">If work lines are not yet registered, you can cancel the created work and any load or shipment lines, and then continue with the picking or shipping process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3350c-107">問題の説明</span><span class="sxs-lookup"><span data-stu-id="3350c-107">Issue description</span></span>

<span data-ttu-id="3350c-108">この問題は、明細行の引当またはリリースを実行しようとしたときに、在庫トランザクションのステータスが *ピッキング済* になっている (材料がピッキングされていることを示す) 場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="3350c-108">This issue occurs if you try to reserve or release work for a line, but the inventory transaction has a status of *Picked*, which indicates that the material has been picked.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3350c-109">問題の解決</span><span class="sxs-lookup"><span data-stu-id="3350c-109">Issue resolution</span></span>

<span data-ttu-id="3350c-110">この問題を解決するには、次のいずれかの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3350c-110">To fix this issue, follow one of these steps.</span></span>

- <span data-ttu-id="3350c-111">製造オーダーのステータスを *見積済* または *リリース済* に変更します。</span><span class="sxs-lookup"><span data-stu-id="3350c-111">Change the status of the production order back to *Estimated* or *Released*.</span></span>
- <span data-ttu-id="3350c-112">関連する製造オーダーの詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="3350c-112">Open the details page for the relevant production order.</span></span> <span data-ttu-id="3350c-113">アクション ウィンドウの **倉庫** タブの **停止** グループで、**停止してピッキング解除** を選択し、ピッキング済トランザクションをすべてピッキング解除します。</span><span class="sxs-lookup"><span data-stu-id="3350c-113">On the Action Pane, on the **Warehouse** tab, in the **Stop** group, select **Stop and unpick** to unpick all picked transactions.</span></span> <span data-ttu-id="3350c-114">次に、**停止の削除** を選択して、製造オーダーを処理します。</span><span class="sxs-lookup"><span data-stu-id="3350c-114">Then select **Remove stop** to process the production order.</span></span>

<span data-ttu-id="3350c-115">*ピッキング解除* と *停止* の機能について、次で説明します。</span><span class="sxs-lookup"><span data-stu-id="3350c-115">Here is an explanation of the *Unpick* and *Stop* functions:</span></span>

- <span data-ttu-id="3350c-116">**ピッキング解除**: この機能は、部品表 (BOM) 明細行と、ステータスが *ピッキング済* から *注文中* になっているフォーミュラ明細行の在庫トランザクション ステータスを反転します。</span><span class="sxs-lookup"><span data-stu-id="3350c-116">**Unpick** – This function reverses the status of inventory transactions for bill of materials (BOM) lines and formula lines that have a status from *Picked* through *On order*.</span></span> <span data-ttu-id="3350c-117">未処理の材料ピッキングの作業が完了すると、明細行のステータスが *ピッキング済* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-117">When work for raw material picking is completed, the status of the lines is set to *Picked*.</span></span> <span data-ttu-id="3350c-118">このステータスにより、製造オーダーが *作成済* ステータスにリセットされなくなります。</span><span class="sxs-lookup"><span data-stu-id="3350c-118">This status prevents the production order from being reset to *Created* status.</span></span> <span data-ttu-id="3350c-119">この場合、*ピッキング解除* 機能を使用して、トランザクションを *ピッキング済* ステータスから元に戻してから、製造オーダーを *作成済* ステータスにリセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="3350c-119">In this case, you can use the *Unpick* function to revert the transactions from *Picked* status and then reset the production order to *Created* status.</span></span>
- <span data-ttu-id="3350c-120">**停止**: この機能は、注文のステータスが更新されないようにするために製造オーダーに **停止済み** フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="3350c-120">**Stop** – This function sets a **Stopped** flag on the production order to prevent any status update on the order.</span></span> <span data-ttu-id="3350c-121">**停止済み** フラグは、製造オーダーの詳細ページの **倉庫** クイックタブにあります。</span><span class="sxs-lookup"><span data-stu-id="3350c-121">You can find the **Stopped** flag on the **Warehouse** FastTab of the production order details page.</span></span>

> [!NOTE]
>
> - <span data-ttu-id="3350c-122">このボタンは、倉庫プロセスに対して有効になっている品目に対して製造オーダーが作成された場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-122">The buttons are visible only when the production order is created for items that are enabled for warehouse processes.</span></span>
> - <span data-ttu-id="3350c-123">**停止** グループは、製造オーダーの詳細ページのアクション ウィンドウの **倉庫** タブにのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-123">The **Stop** group is visible only on the **Warehouse** tab on the Action Pane of the production order details page.</span></span> <span data-ttu-id="3350c-124">**製造オーダー** リスト ページの **倉庫** クイックタブには表示されません。</span><span class="sxs-lookup"><span data-stu-id="3350c-124">It isn't visible on the **Warehouse** FastTab of the **Production orders** list page.</span></span>

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a><span data-ttu-id="3350c-125">グローバル アドレス帳で作業者名を変更しても、一致するリソース名が更新されません。</span><span class="sxs-lookup"><span data-stu-id="3350c-125">The matching resource name isn't updated after I change a worker name in the global address book.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3350c-126">問題の説明</span><span class="sxs-lookup"><span data-stu-id="3350c-126">Issue description</span></span>

<span data-ttu-id="3350c-127">グローバル アドレス帳の作業者の名前を変更した場合、リソース グループ マスター内の一致するリソース名は更新されません。</span><span class="sxs-lookup"><span data-stu-id="3350c-127">If you change a worker name in the global address book, the matching resource name isn't updated in the resource group master.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3350c-128">問題の解決</span><span class="sxs-lookup"><span data-stu-id="3350c-128">Issue resolution</span></span>

<span data-ttu-id="3350c-129">このシナリオは、現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3350c-129">This scenario isn't currently supported.</span></span> <span data-ttu-id="3350c-130">問題を修正するには、リソース名を手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3350c-130">To fix the issue, you must manually update the resource name.</span></span>

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a><span data-ttu-id="3350c-131">新しい製造オーダーを作成すると、"部品表と工順の有効なバージョンを挿入しますか?" というメッセージが表示されません。</span><span class="sxs-lookup"><span data-stu-id="3350c-131">When I create a new production order, I don't receive the following message: "Insert the active version of bill of material and route?"</span></span>

### <a name="issue-description"></a><span data-ttu-id="3350c-132">問題の説明</span><span class="sxs-lookup"><span data-stu-id="3350c-132">Issue description</span></span>

<span data-ttu-id="3350c-133">新しい製造オーダーを作成する場合は、品目番号を入力すると、**サイト** および **倉庫** フィールドが、完成品目の **既定の注文設定** ページで定義されている既定のサイトと倉庫に自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-133">When you create a new production order, after you enter the item number, the **Site** and **Warehouse** fields are automatically set to the default site and warehouse that are defined on the **Default order settings** page for the finished goods item.</span></span> <span data-ttu-id="3350c-134">さらに、有効な BOM 番号と工順番号が自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-134">Additionally, the active BOM number and route number are automatically entered.</span></span> <span data-ttu-id="3350c-135">これらの値の入力を求める次のメッセージは表示されません。</span><span class="sxs-lookup"><span data-stu-id="3350c-135">You don't receive the following message that prompts you for those values:</span></span>

> <span data-ttu-id="3350c-136">部品表および工順の有効なバージョンを挿入しますか?</span><span class="sxs-lookup"><span data-stu-id="3350c-136">Insert active version for bill of material and route?</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3350c-137">問題の解決</span><span class="sxs-lookup"><span data-stu-id="3350c-137">Issue resolution</span></span>

<span data-ttu-id="3350c-138">**既定の注文設定** ページでサイトと倉庫が定義されている製品を選択した場合、BOM と工順の番号を挿入するように求められることはありません。</span><span class="sxs-lookup"><span data-stu-id="3350c-138">You aren't prompted to insert BOM and route numbers if you select a product that a site and warehouse are defined for on the **Default order settings** page.</span></span> <span data-ttu-id="3350c-139">選択した製品に対してこれらの値が定義されていない場合にのみ、プロンプトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-139">You're prompted only if those values aren't defined for the selected product.</span></span>

## <a name="production-orders-arent-shown-on-the-marking-page"></a><span data-ttu-id="3350c-140">[マーキング] ページに製造オーダーは表示されません。</span><span class="sxs-lookup"><span data-stu-id="3350c-140">Production orders aren't shown on the Marking page.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3350c-141">問題の説明</span><span class="sxs-lookup"><span data-stu-id="3350c-141">Issue description</span></span>

<span data-ttu-id="3350c-142">**マーキング** ページには、一部の製造オーダーが表示されません。</span><span class="sxs-lookup"><span data-stu-id="3350c-142">Some production orders aren't shown on the **Marking** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3350c-143">問題の解決</span><span class="sxs-lookup"><span data-stu-id="3350c-143">Issue resolution</span></span>

<span data-ttu-id="3350c-144">次の構成を持つ製品をマーキングに使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="3350c-144">Products that have the following configuration aren't available for marking.</span></span> <span data-ttu-id="3350c-145">したがって、これらは **マーキング** ページに表示されません。</span><span class="sxs-lookup"><span data-stu-id="3350c-145">Therefore, they won't be shown on the **Marking** page:</span></span>

- <span data-ttu-id="3350c-146">製品は、*CW* タイプの製品として定義されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-146">The products are defined as products of the *catch weight* type.</span></span>
- <span data-ttu-id="3350c-147">これらは、高度な倉庫プロセスに対して有効になっています。</span><span class="sxs-lookup"><span data-stu-id="3350c-147">They are enabled for the advanced warehouse processes.</span></span>
- <span data-ttu-id="3350c-148">これらは、*標準原価* 原則によって制御されるように構成されています。</span><span class="sxs-lookup"><span data-stu-id="3350c-148">They are configured to be controlled by the *Standard cost* principle.</span></span>

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a><span data-ttu-id="3350c-149">製造オーダーを終了しようとすると、エラー メッセージ " BOM consumptionCost 値の計算は、在庫からの払出時には負である必要があります" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-149">When I try to end a production order, I receive the following error message: "Calculating BOM consumptionCost value must be negative upon issue from inventory."</span></span>

<span data-ttu-id="3350c-150">この問題は、リリース 10.0.15 で修正されました。</span><span class="sxs-lookup"><span data-stu-id="3350c-150">This issue was fixed in release 10.0.15.</span></span>

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a><span data-ttu-id="3350c-151">製造オーダーのステータスが "完了報告済" から "終了" に変更された場合、エラー メッセージ "更新が競合しています。</span><span class="sxs-lookup"><span data-stu-id="3350c-151">When the status of a production order is changed from Reported as finished to End, I receive the following error messages: "Update conflict.</span></span> <span data-ttu-id="3350c-152">更新後に、標準原価が資産在庫金額と一致していません" および "関数 InventCostMovement.checkVariance で重大なエラーが発生しました" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-152">The standard cost does not match with the financial inventory value after the update" and "A critical error has occurred in function InventCostMovement.checkVariance."</span></span>

<span data-ttu-id="3350c-153">この問題は、基になるデータが別のプロセスによって変更されたために発生します。</span><span class="sxs-lookup"><span data-stu-id="3350c-153">This issue occurs because the underlying data was changed by another process.</span></span> <span data-ttu-id="3350c-154">このプロセスでは、最大 5 回までデータを更新しようとします。</span><span class="sxs-lookup"><span data-stu-id="3350c-154">The process will try to update the data up to five times.</span></span> <span data-ttu-id="3350c-155">5 回試行しても競合が発生する場合は、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-155">If the conflict still exists after five attempts, you will receive the following error messages:</span></span>

> <span data-ttu-id="3350c-156">更新が競合しています。</span><span class="sxs-lookup"><span data-stu-id="3350c-156">Update conflict.</span></span> <span data-ttu-id="3350c-157">更新後の標準原価が資産在庫金額と一致しません。</span><span class="sxs-lookup"><span data-stu-id="3350c-157">The standard cost does not match with the financial inventory value after the update.</span></span>

> <span data-ttu-id="3350c-158">関数 InventCostMovement.checkVariance で重大なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="3350c-158">A critical error has occurred in function InventCostMovement.checkVariance.</span></span>

<span data-ttu-id="3350c-159">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="3350c-159">This behavior is by design.</span></span> <span data-ttu-id="3350c-160">この問題を回避するには、バッチ ジョブを再開します。</span><span class="sxs-lookup"><span data-stu-id="3350c-160">To mitigate the issue, resume the batch job.</span></span> <span data-ttu-id="3350c-161">実行が完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3350c-161">It should finish running.</span></span>

<span data-ttu-id="3350c-162">バッチ ジョブが再開後に一貫して失敗する場合は、元帳の既定の通貨の丸め精度が、InventSum テーブルの値に適用される丸めに準拠していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="3350c-162">If the batch job consistently fails after you resume it, verify that the rounding precision for the ledger's default currency is compliant with the rounding that is applied to values in the InventSum table.</span></span> <span data-ttu-id="3350c-163">丸めの精度が準拠していない値に変更された場合は、通常、それを対応する値に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3350c-163">If the rounding precision has been changed to a non-compliant value, you probably must change it back to a compliant value.</span></span> <span data-ttu-id="3350c-164">**ModifiedDateTime** を探します。</span><span class="sxs-lookup"><span data-stu-id="3350c-164">Look for **ModifiedDateTime**.</span></span> <span data-ttu-id="3350c-165">この場合、値は、通常、丸めの精度が最近変更されたことを示しています。</span><span class="sxs-lookup"><span data-stu-id="3350c-165">In this case, the value will typically show that the rounding precision was recently changed.</span></span>

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a><span data-ttu-id="3350c-166">倉庫にリリースすると、エラー メッセージ "品目 RM を完全に引当できませんでした。</span><span class="sxs-lookup"><span data-stu-id="3350c-166">When I release to a warehouse, I receive the following error message: "Item RM could not be fully reserved.</span></span> <span data-ttu-id="3350c-167">数量がすべて使用可能であることを確認するか、BOM 明細行の [引当] フィールドが [手動] または [開始] に設定されている場合は、品目を手動で引当します。</span><span class="sxs-lookup"><span data-stu-id="3350c-167">Ensure that the full quantity is available, or reserve the items manually if the Reservation field on the BOM line is set to Manual or Started.</span></span> <span data-ttu-id="3350c-168">一部の材料を引き当てることができないため、注文を倉庫にリリースできませんでした" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-168">Could not release the order to warehouse because some materials could not be reserved."</span></span> <span data-ttu-id="3350c-169">ただし、ステータスは [リリース済] に更新されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-169">However, the status is updated to Released.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3350c-170">問題の説明</span><span class="sxs-lookup"><span data-stu-id="3350c-170">Issue description</span></span>

<span data-ttu-id="3350c-171">製造オーダーがリリースされるときに、すべての BOM 明細行品目が物理的に使用可能ではない場合、**倉庫にリリース** ポリシーが製造オーダーで *完全引当を要求* に設定されていると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-171">If not all BOM line items are physically available when a production order is released, and the **Release to warehouse** policy is set to *Require full reservation* on the production order, you will receive the following error message:</span></span>

> <span data-ttu-id="3350c-172">品目 RM を完全に引当することはできません。</span><span class="sxs-lookup"><span data-stu-id="3350c-172">Item RM could not be fully reserved.</span></span> <span data-ttu-id="3350c-173">数量がすべて使用可能であることを確認するか、BOM 明細行の [引当] フィールドが [手動] または [開始] に設定されている場合は、品目を手動で引当します。</span><span class="sxs-lookup"><span data-stu-id="3350c-173">Ensure that the full quantity is available, or reserve the items manually if the Reservation field on the BOM line is set to Manual or Started.</span></span> <span data-ttu-id="3350c-174">注文を倉庫にリリースできませんでした。一部の材料を引き当てることができませんでした。</span><span class="sxs-lookup"><span data-stu-id="3350c-174">Could not release the order to warehouse because some materials could not be reserved.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3350c-175">問題の解決</span><span class="sxs-lookup"><span data-stu-id="3350c-175">Issue resolution</span></span>

<span data-ttu-id="3350c-176">この動作は仕様であり、期待どおりに機能しています。</span><span class="sxs-lookup"><span data-stu-id="3350c-176">This behavior is by design and is working as expected.</span></span>

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a><span data-ttu-id="3350c-177">製造オーダーを終了して完了と報告しようとすると、エラー メッセージ "生産に対して完了報告済みの適正数量の合計は %1 です。</span><span class="sxs-lookup"><span data-stu-id="3350c-177">When I try to end a production order and report as finished, I receive the following error message: "Total good quantity reported as finished for the production will be %1.</span></span> <span data-ttu-id="3350c-178">最後の工程に対するフィードバックは合計で 0.00 です" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-178">Feedback for the last operation is 0.00 in total."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3350c-179">問題の説明</span><span class="sxs-lookup"><span data-stu-id="3350c-179">Issue description</span></span>

<span data-ttu-id="3350c-180">レポートを完了仕訳帳として製造オーダーに転記しようとすると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-180">When you try to post a report as finished journal on a production order, you receive the following error message:</span></span>

> <span data-ttu-id="3350c-181">生産完了が報告された良品数量の合計が %1 になります。</span><span class="sxs-lookup"><span data-stu-id="3350c-181">Total good quantity reported as finished for the production will be %1.</span></span> <span data-ttu-id="3350c-182">最後の工程に対するフィードバックは合計で 0.00 です。</span><span class="sxs-lookup"><span data-stu-id="3350c-182">Feedback for the last operation is 0.00 in total.</span></span>

### <a name="possible-cause"></a><span data-ttu-id="3350c-183">考えられる原因</span><span class="sxs-lookup"><span data-stu-id="3350c-183">Possible cause</span></span>

<span data-ttu-id="3350c-184">この問題は、前回の工程で転記された数量が正しくなかった場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="3350c-184">This issue occurs if the quantities that were posted in the last operations were incorrect.</span></span> <span data-ttu-id="3350c-185">たとえば、生産が開始されているが、開始する必要のある数量が割り当てられていない場合、工順カード仕訳帳は明細行なしで転記されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-185">For example, if production is started, but the quantity that must be started isn't allocated, the route card journal will be posted without any lines.</span></span> <span data-ttu-id="3350c-186">状況を確認するには、製造オーダーを開き、アクション ウィンドウの **表示** タブで、**工順カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3350c-186">To confirm the situation, open the production order, and then, on the Action Pane, on the **View** tab, select **Route card**.</span></span>

### <a name="workaround"></a><span data-ttu-id="3350c-187">回避策</span><span class="sxs-lookup"><span data-stu-id="3350c-187">Workaround</span></span>

<span data-ttu-id="3350c-188">仕訳帳が正しく転記されなかった工程に対して追加の仕訳帳を転記することにより、この問題を解決できます。</span><span class="sxs-lookup"><span data-stu-id="3350c-188">You can fix this issue by posting additional journals for the operations that the journals weren't correctly posted for.</span></span> <span data-ttu-id="3350c-189">製造オーダーを再開し、追加の仕訳帳を転記する場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="3350c-189">Restart the production order, and select to post the additional journals.</span></span> <span data-ttu-id="3350c-190">このアクションでは製造オーダーは開始されませんが、仕訳帳は転記されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-190">This action won't start the production order, but it will post the journals.</span></span> <span data-ttu-id="3350c-191">その後、工順カードに転記済の数量が表示され、製造オーダーを正常に終了することができます。</span><span class="sxs-lookup"><span data-stu-id="3350c-191">The route card should then show the quantities that were posted, and you should be able to end the production orders successfully.</span></span>

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a><span data-ttu-id="3350c-192">エラーの数量を報告しているが、時間または材料の数量を報告していないときに、製造オーダーを完了として報告することはできますか。</span><span class="sxs-lookup"><span data-stu-id="3350c-192">Can I report a production order as finished while I report the error quantity, but not while I report the time or material quantity?</span></span>

<span data-ttu-id="3350c-193">正常数量も報告しなければ、製造オーダーのエラー数量を報告することはできません。</span><span class="sxs-lookup"><span data-stu-id="3350c-193">You can't report the error quantity on a production order unless you also report the good quantity.</span></span> <span data-ttu-id="3350c-194">このシナリオはサポートされ **ません**。</span><span class="sxs-lookup"><span data-stu-id="3350c-194">This scenario is **not** supported.</span></span> <span data-ttu-id="3350c-195">製造オーダーを終了しようとすると、完了レポートの更新が最終的に失敗し、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3350c-195">The report as finished update will eventually fail when you try to end the production order, and you will receive the following error message:</span></span>

> <span data-ttu-id="3350c-196">完了レポートの数量がありません。</span><span class="sxs-lookup"><span data-stu-id="3350c-196">Missing report as finished quantity.</span></span>

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a><span data-ttu-id="3350c-197">消費された商品のシリアル番号に対して、完成品のシリアル番号を追跡できますか。</span><span class="sxs-lookup"><span data-stu-id="3350c-197">Can I trace the serial numbers of finished goods against the serial numbers of consumed goods?</span></span>

<span data-ttu-id="3350c-198">完成品のシリアル番号を、製造オーダーが完成品を作成するために消費する材料のシリアル番号に対して追跡することはできません。</span><span class="sxs-lookup"><span data-stu-id="3350c-198">You can't trace the serial numbers of finished goods against the serial numbers of material that a production order consumes to make those finished goods.</span></span> <span data-ttu-id="3350c-199">このシナリオは、現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3350c-199">This scenario isn't currently supported.</span></span> <span data-ttu-id="3350c-200">この回避策として、数量 1 の製造オーダーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="3350c-200">The workaround is to create production orders for a quantity of 1.</span></span>
