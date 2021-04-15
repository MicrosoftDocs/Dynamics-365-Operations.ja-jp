---
title: 価格、割引、契約、リベートのトラブルシューティング
description: このトピックでは、価格、割引、契約、およびリベートの処理中に発生する可能性がある問題を修正する方法について説明します。
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 12bc3cbccb1577c278489f640299510b3ced17e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811089"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="8a409-103">価格、割引、契約、リベートのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="8a409-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="8a409-104">このトピックでは、価格、割引、契約、およびリベートの処理中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8a409-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="8a409-105">発注書が作成された後、購買契約書を発注書の明細行にリンクできません。</span><span class="sxs-lookup"><span data-stu-id="8a409-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="8a409-106">購買契約書は、発注書が作成された後、発注書に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a409-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="8a409-107">それ以外の場合、発注書の明細行を購買契約書の明細行に関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="8a409-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="8a409-108">「手動または外部ドキュメントで入力した価格と割引を更新します」というメッセージが表示されるのは、どのチェックがトリガーになっていますか?</span><span class="sxs-lookup"><span data-stu-id="8a409-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="8a409-109">出荷日を変更すると、「手動または外部ドキュメントで入力した価格と割引を更新します」 というメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="8a409-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="8a409-110">このメッセージは、出荷日が変更された場合、別の取引または販売契約が発生し、価格が変更される可能性があるために表示されます。</span><span class="sxs-lookup"><span data-stu-id="8a409-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="8a409-111">出荷日を変更は、倉庫のスケジュールやその他の関連情報にも影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8a409-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="8a409-112">このメッセージは、日付またはその他のパラメーターが変更されるたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="8a409-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="8a409-113">メッセージの目的は、これらの変更によって発生する可能性がある価格の変更を確実に把握することです。</span><span class="sxs-lookup"><span data-stu-id="8a409-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="8a409-114">メッセージは、売買契約評価 (TAE) プロンプトです。</span><span class="sxs-lookup"><span data-stu-id="8a409-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="8a409-115">詳細な詳細については、[売買契約評価ポリシー](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a409-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="8a409-116">発注受入には、すべての費用は含まれません。</span><span class="sxs-lookup"><span data-stu-id="8a409-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="8a409-117">問題を再現する</span><span class="sxs-lookup"><span data-stu-id="8a409-117">Reproduce the issue</span></span>

<span data-ttu-id="8a409-118">この問題を再現する一つの方法は次のプロシージャです。</span><span class="sxs-lookup"><span data-stu-id="8a409-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="8a409-119">**調達パラメーター** ページの **配送** タブで、**製品受領時に費用を生成** オプションが *はい* に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8a409-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="8a409-120">費用を含む発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="8a409-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="8a409-121">発注書を確認します。</span><span class="sxs-lookup"><span data-stu-id="8a409-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="8a409-122">発注書を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="8a409-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="8a409-123">受入合計を確認し、予想される合計と比較します。</span><span class="sxs-lookup"><span data-stu-id="8a409-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="8a409-124">すべての費用が発注受入に含まれているわけではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8a409-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8a409-125">問題の解決</span><span class="sxs-lookup"><span data-stu-id="8a409-125">Issue resolution</span></span>

<span data-ttu-id="8a409-126">解決策は、雑費が設定されている方法によって異なります。</span><span class="sxs-lookup"><span data-stu-id="8a409-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="8a409-127">要件に合わせて雑費を設定する方法については、次のブログ記事を参照してください: [製品受領時に雑費を計上する](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)。</span><span class="sxs-lookup"><span data-stu-id="8a409-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="8a409-128">売買契約価格および割引は、データ管理を介してインポートされた販売注文または発注書の明細行には適用されません。</span><span class="sxs-lookup"><span data-stu-id="8a409-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8a409-129">問題の説明</span><span class="sxs-lookup"><span data-stu-id="8a409-129">Issue description</span></span>

<span data-ttu-id="8a409-130">販売注文または発注書の明細行に適用可能な売買契約は、データ管理を介してインポートされた明細行には適用されません。</span><span class="sxs-lookup"><span data-stu-id="8a409-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="8a409-131">ただし、手動で作成された販売注文または発注書の明細行には、同じ売買契約が適用されます。</span><span class="sxs-lookup"><span data-stu-id="8a409-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="8a409-132">問題の理由</span><span class="sxs-lookup"><span data-stu-id="8a409-132">Reason for the issue</span></span>

<span data-ttu-id="8a409-133">データ管理を介してインポートされた発注書の明細行に価格情報が既に含まれている場合、それらの明細行に対する売買契約は再評価されません。</span><span class="sxs-lookup"><span data-stu-id="8a409-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="8a409-134">たとえば、**行割引の割合** または価格と割引のいずれかの値が、明細行に設定されている場合、その明細行に対して売買契約は検索されません。</span><span class="sxs-lookup"><span data-stu-id="8a409-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="8a409-135">問題の回避策</span><span class="sxs-lookup"><span data-stu-id="8a409-135">Issue workaround</span></span>

<span data-ttu-id="8a409-136">この動作は予期されるものであり、販売注文と発注書の両方で類似しています。</span><span class="sxs-lookup"><span data-stu-id="8a409-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="8a409-137">回避策として、価格情報を設定せずに発注書の明細行をインポートします。</span><span class="sxs-lookup"><span data-stu-id="8a409-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="8a409-138">その結果、売買契約が適用され、定義された売買契約に基づいて発注書の明細行が更新されます。</span><span class="sxs-lookup"><span data-stu-id="8a409-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="8a409-139">仕入先リベートは、請求書に基づいて累計されません。</span><span class="sxs-lookup"><span data-stu-id="8a409-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8a409-140">問題の説明</span><span class="sxs-lookup"><span data-stu-id="8a409-140">Issue description</span></span>

<span data-ttu-id="8a409-141">転記された請求書の支払期日が異なる場合、それらの請求書は、それらから生成される仕入先リベートには反映されません。</span><span class="sxs-lookup"><span data-stu-id="8a409-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8a409-142">問題の解決</span><span class="sxs-lookup"><span data-stu-id="8a409-142">Issue resolution</span></span>

<span data-ttu-id="8a409-143">仕様では、仕入先リベートの計算時に期日が考慮されません。</span><span class="sxs-lookup"><span data-stu-id="8a409-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="8a409-144">実際の仕入先リベートに関して、期日と請求書との関係がより明確になるようにシステムをカスタマイズすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="8a409-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="8a409-145">発注書の単価は、単位換算に基づいて計算されません。</span><span class="sxs-lookup"><span data-stu-id="8a409-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8a409-146">問題の説明</span><span class="sxs-lookup"><span data-stu-id="8a409-146">Issue description</span></span>

<span data-ttu-id="8a409-147">発注書の単位が変更された場合、売買契約価格は単位換算定義に従って再計算されません。</span><span class="sxs-lookup"><span data-stu-id="8a409-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8a409-148">問題の解決</span><span class="sxs-lookup"><span data-stu-id="8a409-148">Issue resolution</span></span>

<span data-ttu-id="8a409-149">価格は常に売買契約 (または販売契約書や品目価格などのシステム内のその他の価格設定) から取得され、単位に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="8a409-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="8a409-150">注文明細行で単位が変更されると、システムは新しい単位の価格を検索し、その価格を適用します。</span><span class="sxs-lookup"><span data-stu-id="8a409-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="8a409-151">単位の価格が見つからない場合は、システムは価格を適用しません。</span><span class="sxs-lookup"><span data-stu-id="8a409-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="8a409-152">単位換算を使用して、価格を別の単位に再計算することはできません。</span><span class="sxs-lookup"><span data-stu-id="8a409-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="8a409-153">理論的には、10 個入りの 1 箱の価格は、1 箱の価格の 10 倍と等しくない場合があります。</span><span class="sxs-lookup"><span data-stu-id="8a409-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="8a409-154">問題の回避策</span><span class="sxs-lookup"><span data-stu-id="8a409-154">Issue workaround</span></span>

<span data-ttu-id="8a409-155">この問題を回避する 1 つの方法は、品目の注文明細行で使用されると予想される単位の売買契約があることを確認することです。</span><span class="sxs-lookup"><span data-stu-id="8a409-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="8a409-156">通貨換算の問題は、売買契約で発生します。</span><span class="sxs-lookup"><span data-stu-id="8a409-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="8a409-157">通貨が発注書で異なる場合、売買契約価格が通貨に従って再計算されません。</span><span class="sxs-lookup"><span data-stu-id="8a409-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="8a409-158">*一般通貨* 機能を使用すると、価格と割引を 1 つの通貨でのみ定義できます。</span><span class="sxs-lookup"><span data-stu-id="8a409-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="8a409-159">その後、必要に応じて、他の通貨に換算できます。</span><span class="sxs-lookup"><span data-stu-id="8a409-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="8a409-160">さらに、換算が完了すると、機能によって自動的にスマート丸めが適用されます。</span><span class="sxs-lookup"><span data-stu-id="8a409-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="8a409-161">行ビュー モードで購買契約ページを開くと、明細行の概要に価格単位フィールドを追加してページをカスタマイズできません。</span><span class="sxs-lookup"><span data-stu-id="8a409-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="8a409-162">契約フレームワーク内の一部の共有フィールドは、個人用設定に含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="8a409-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="8a409-163">この制限は、実装されるデータ モデルが原因で発生します。</span><span class="sxs-lookup"><span data-stu-id="8a409-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="8a409-164">したがって、**価格単位** フィールドをカスタマイズすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8a409-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="8a409-165">購買契約書の上限は、購買要求に対して有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="8a409-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8a409-166">問題の説明</span><span class="sxs-lookup"><span data-stu-id="8a409-166">Issue description</span></span>

<span data-ttu-id="8a409-167">購買要求が購買契約書にリンクされている場合、購買要求に対して購買契約書の上限は有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="8a409-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="8a409-168">既定の価格情報は正しく入力されていますが、購買要求で購買契約書の上限を超えて注文することができます。</span><span class="sxs-lookup"><span data-stu-id="8a409-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8a409-169">問題の解決</span><span class="sxs-lookup"><span data-stu-id="8a409-169">Issue resolution</span></span>

<span data-ttu-id="8a409-170">この動作は予期されています。</span><span class="sxs-lookup"><span data-stu-id="8a409-170">This behavior is expected.</span></span> <span data-ttu-id="8a409-171">要求が常に承認されるとは限らないため、購買契約書に数量または金額を予約しないでください。</span><span class="sxs-lookup"><span data-stu-id="8a409-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="8a409-172">したがって、購買契約書の上限には達しません。</span><span class="sxs-lookup"><span data-stu-id="8a409-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="8a409-173">売買契約は、却下された RFQ から作成できます。</span><span class="sxs-lookup"><span data-stu-id="8a409-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="8a409-174">したがって、RFQ 明細行が受理されていない場合でも、システムは売買契約仕訳帳の作成を妨げません。</span><span class="sxs-lookup"><span data-stu-id="8a409-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="8a409-175">承認されたかまたは却下されたかに関係なく、見積依頼 (RFQ) に対するすべての返信は、売買契約を作成できます。</span><span class="sxs-lookup"><span data-stu-id="8a409-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="8a409-176">詳細については、[見積依頼 (RFQ) の概要](request-quotations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a409-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]