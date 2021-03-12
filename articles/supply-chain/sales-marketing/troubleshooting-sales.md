---
title: 販売注文に関するトラブルシューティング
description: このトピックでは、販売注文と作業する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c9a5b7a5e8cac7f8816233dd2d7ff1a7f84ea480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974788"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="6b663-103">販売注文に関するトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="6b663-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="6b663-104">このトピックでは、販売注文と作業する際に発生する可能性がある問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6b663-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="6b663-105">販売注文ヘッダーの場所を変更しても、税金情報は更新されません。</span><span class="sxs-lookup"><span data-stu-id="6b663-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6b663-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="6b663-106">Issue description</span></span>

<span data-ttu-id="6b663-107">販売注文ヘッダーまたは明細行レベルで、サイト、倉庫、または配送先の住所が変更された場合、明細行のケースの税金情報は自動的に更新されません。</span><span class="sxs-lookup"><span data-stu-id="6b663-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6b663-108">問題の解決</span><span class="sxs-lookup"><span data-stu-id="6b663-108">Issue resolution</span></span>

<span data-ttu-id="6b663-109">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="6b663-109">This behavior is by design.</span></span> <span data-ttu-id="6b663-110">この問題が発生するのは、明細行レベルで配送先住所、サイト、および倉庫が自動的に変更されないためです。</span><span class="sxs-lookup"><span data-stu-id="6b663-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="6b663-111">手動でそれらをを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b663-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="6b663-112">同じ期間または重複する期間に対して 2 つの売買契約がある場合は、常に同じ契約明細行が選択されます。</span><span class="sxs-lookup"><span data-stu-id="6b663-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6b663-113">問題の説明</span><span class="sxs-lookup"><span data-stu-id="6b663-113">Issue description</span></span>

<span data-ttu-id="6b663-114">2 つの売買契約が同じ期間または重複する期間に対して定義されている場合は、それらの品目を含む販売注文明細行を作成するたびに同じ売買契約が選択されるように見えます。</span><span class="sxs-lookup"><span data-stu-id="6b663-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6b663-115">問題の解決</span><span class="sxs-lookup"><span data-stu-id="6b663-115">Issue resolution</span></span>

<span data-ttu-id="6b663-116">特定の日付に対して複数の売買契約がある場合は、最低価格の売買契約が常に選択されます。</span><span class="sxs-lookup"><span data-stu-id="6b663-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="6b663-117">詳細については、[Microsoft Dynamics AX 2012 の売買契約](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90) のホワイトペーパーをダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="6b663-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="6b663-118">需要を満たすために注文書を販売注文にリンクすることはできますか。</span><span class="sxs-lookup"><span data-stu-id="6b663-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="6b663-119">販売注文からの発注書を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="6b663-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="6b663-120">詳細については、[販売注文から発注書を作成する](tasks/create-purchase-order-sales-order.md) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="6b663-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="6b663-121">返品注文または販売注文をキャンセルまたは削除できません。</span><span class="sxs-lookup"><span data-stu-id="6b663-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="6b663-122">*作成済* 状態の販売注文および返品注文のみをキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="6b663-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="6b663-123">詳細については、[返品注文のキャンセル](../service-management/cancel-return-order.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b663-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="6b663-124">販売注文をキャンセルしようとすると、"予約に依存する作業が作成されているため、"引当を削除できません" というエラーを受信します。</span><span class="sxs-lookup"><span data-stu-id="6b663-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="6b663-125">エラーコード: WAX4661</span><span class="sxs-lookup"><span data-stu-id="6b663-125">Error code: WAX4661</span></span>

<span data-ttu-id="6b663-126">作業が販売注文に関連付けられている場合、その作業がキャンセルされて取り消されるまで、販売注文をキャンセルすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6b663-126">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="6b663-127">この要件は、販売注文に関連付けられている作業が終了されている場合にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="6b663-127">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="6b663-128">この問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6b663-128">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="6b663-129">作業をキャンセルし、在庫を目的の場所に戻します。</span><span class="sxs-lookup"><span data-stu-id="6b663-129">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="6b663-130">販売注文の該当する負荷に移動し、読み込み行の **ピッキング済数量の削減** またはアクション ペインでの **作業の取消し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b663-130">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="6b663-131">この時点で、職場のステータスは *キャンセル済* になり、新しい在庫移動作業が自動的に作成および処理されて、在庫が取消時点で説明した保管場所に戻されます。</span><span class="sxs-lookup"><span data-stu-id="6b663-131">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="6b663-132">負荷を削除します。</span><span class="sxs-lookup"><span data-stu-id="6b663-132">Delete the load.</span></span> <span data-ttu-id="6b663-133">また、出荷も削除されます。</span><span class="sxs-lookup"><span data-stu-id="6b663-133">The shipment is also deleted.</span></span>
3. <span data-ttu-id="6b663-134">これで、販売注文に移動してキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="6b663-134">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="6b663-135">販売注文にリンクされている会社間発注書をキャンセルできません。</span><span class="sxs-lookup"><span data-stu-id="6b663-135">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6b663-136">問題の説明</span><span class="sxs-lookup"><span data-stu-id="6b663-136">Issue description</span></span>

<span data-ttu-id="6b663-137">販売注文にリンクされている会社間発注書をキャンセルしようとすると、"残余更新数量が変更されたため、数量を減らすことができません。" というエラーメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="6b663-137">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6b663-138">問題の解決</span><span class="sxs-lookup"><span data-stu-id="6b663-138">Issue resolution</span></span>

<span data-ttu-id="6b663-139">この問題は、Microsoft Dynamics 365 Supply Chain Management バージョン10.0.13 で修正されました。</span><span class="sxs-lookup"><span data-stu-id="6b663-139">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="6b663-140">このバージョン以降のバージョンでは、販売注文にリンクされている会社間発注書をキャンセルできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6b663-140">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="6b663-141">削除された請求済販売注文を元に戻すことはできますか ?</span><span class="sxs-lookup"><span data-stu-id="6b663-141">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="6b663-142">問題の説明</span><span class="sxs-lookup"><span data-stu-id="6b663-142">Issue description</span></span>

<span data-ttu-id="6b663-143">請求済の販売注文が誤って削除されました。これを復元するか、その詳細を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b663-143">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6b663-144">問題の解決</span><span class="sxs-lookup"><span data-stu-id="6b663-144">Issue resolution</span></span>

<span data-ttu-id="6b663-145">削除された販売注文が既に請求されている場合は、**顧客アカウント \> トランザクション \> 元のドキュメント \> 詳細の表示** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b663-145">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="6b663-146">目的の請求書を検索し、その詳細を表示するために選択します。</span><span class="sxs-lookup"><span data-stu-id="6b663-146">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="6b663-147">この詳細には、販売注文の参照が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6b663-147">These details include the sales order reference.</span></span> <span data-ttu-id="6b663-148">また、このページから販売注文の詳細にアクセスできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b663-148">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="6b663-149">販売注文ヘッダーの期限が SalesOrderHeaderV2Entity データ エンティティに見つかりません。</span><span class="sxs-lookup"><span data-stu-id="6b663-149">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="6b663-150">[期日] フィールドは、*SalesOrderHeaderV2Entity* エンティティに存在しません。</span><span class="sxs-lookup"><span data-stu-id="6b663-150">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="6b663-151">孤立した販売注文レコードを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b663-151">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="6b663-152">孤立した販売注文レコードをクリーンアップするには、次のいずれかの場所に移動して、*販売注文の削除* の定期処理ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="6b663-152">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="6b663-153">販売とマーケティング \> 定期的なタスク \> クリーンアップ \> 半日注文の削除</span><span class="sxs-lookup"><span data-stu-id="6b663-153">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="6b663-154">小売りおよびコマース \>小売業およびコマース IT \> クリーンアップ \> 販売注文の削除</span><span class="sxs-lookup"><span data-stu-id="6b663-154">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="6b663-155">既に転記されている請求書のコミッションを計算する方法はありますか。</span><span class="sxs-lookup"><span data-stu-id="6b663-155">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="6b663-156">Supply Chain Management は、転記された請求書のコミッションの計算は現在サポートしていません。</span><span class="sxs-lookup"><span data-stu-id="6b663-156">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="6b663-157">バンドル品目は、会社間プロセスではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6b663-157">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="6b663-158">このバンドル品目は、発注書に対しては使用できません。なぜなら、このバンドル品目の販売注文明細行を確認すると、数量が *0* (ゼロ) になり、ステータスが *キャンセル済* であることがわかります。</span><span class="sxs-lookup"><span data-stu-id="6b663-158">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Canceled*.</span></span> <span data-ttu-id="6b663-159">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="6b663-159">This behavior is by design.</span></span> <span data-ttu-id="6b663-160">この販売注文では、バンドル品目のコンポーネントのみが購入されます。</span><span class="sxs-lookup"><span data-stu-id="6b663-160">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="6b663-161">バンドル品目自体は購入されません。</span><span class="sxs-lookup"><span data-stu-id="6b663-161">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="6b663-162">バンドルを購入する必要がある場合、この機能は実際には収益認識シナリオのために設計されているため、バンドル品目としてマークする必要があるかどうかを検討します。</span><span class="sxs-lookup"><span data-stu-id="6b663-162">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is designed for revenue recognition scenarios.</span></span> <span data-ttu-id="6b663-163">バンドル品目についての詳細情報は、[バンドル](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b663-163">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
