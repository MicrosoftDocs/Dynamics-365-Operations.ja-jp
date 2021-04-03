---
title: 製品受領書と請求書に関するトラブルシューティング
description: このトピックでは、製品受領書と請求の処理中に発生する可能性がある問題を修正する方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 5fd8ced95c6017c128b77b80047761715b92fc2c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260554"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="9d800-103">製品受領書と請求書に関するトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="9d800-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="9d800-104">このトピックでは、製品受領書と請求の処理中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9d800-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="9d800-105">カテゴリ ベースの品目を持つ購買注文明細行に対して複数の請求書を転記することはできません。</span><span class="sxs-lookup"><span data-stu-id="9d800-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="9d800-106">請求書を転記する場合は、数量が必須です。</span><span class="sxs-lookup"><span data-stu-id="9d800-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="9d800-107">したがって、明細行の全数量が一部の金額でしか請求されていない場合は、別の請求書で残額を請求することはできません。</span><span class="sxs-lookup"><span data-stu-id="9d800-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="9d800-108">発注書の確認に "オブジェクト参照が設定されていません" というエラーが表示されるか、仕入先請求書の転記中に "呼び出しのターゲットが例外をスローしました" という例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="9d800-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="9d800-109">この問題は、発注書の配分に不整合があるために発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="9d800-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="9d800-110">この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9d800-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="9d800-111">詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d800-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="9d800-112">複数の製品受領書を 1 つの発注書にまとめることはできません。</span><span class="sxs-lookup"><span data-stu-id="9d800-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="9d800-113">複数の製品受領書を 1 つの発注書にまとめることはできません。異なる製品受領書明細行の会計日付が異なる場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="9d800-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="9d800-114">Microsoft Dynamics 365 Supply Chain Management の以前のバージョンでは、このような場合に懸念許されていました。</span><span class="sxs-lookup"><span data-stu-id="9d800-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="9d800-115">ただし、このプラクティスではエラーが発生しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="9d800-115">However, the practice is prone to error.</span></span> <span data-ttu-id="9d800-116">作成された発注書明細行の会計日と、その発注書明細行の作成元である製品受領書明細行の会計日とは異なるものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d800-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="9d800-117">(発注書明細行の会計日は、発注書ヘッダーの会計日と一致します。) したがって、複数の製品受領書を1つの発注書に連結することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="9d800-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="9d800-118">たとえば、予算引当や債務など、会計日が使用されます。</span><span class="sxs-lookup"><span data-stu-id="9d800-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="9d800-119">したがって、この品目は、製品受領書から発注書への移行時に保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d800-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="9d800-120">製品受領書がキャンセルされると、トランザクションを中断された勘定科目に転記できます。</span><span class="sxs-lookup"><span data-stu-id="9d800-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9d800-121">問題の説明</span><span class="sxs-lookup"><span data-stu-id="9d800-121">Issue description</span></span>

<span data-ttu-id="9d800-122">製品受領書がキャンセルされると、主勘定が中断された場合でも、保留中の勘定科目にトランザクションを転記することができます。</span><span class="sxs-lookup"><span data-stu-id="9d800-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="9d800-123">問題を再現する</span><span class="sxs-lookup"><span data-stu-id="9d800-123">Reproduce the issue</span></span>

<span data-ttu-id="9d800-124">この問題を再現する一つの方法は次のプロシージャです。</span><span class="sxs-lookup"><span data-stu-id="9d800-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="9d800-125">**買掛金勘定パラメーター** ページの **一般** タブで、**元帳の製品受領書の転記** オプションが *はい* に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9d800-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="9d800-126">発注書を作成し、製品に対して *1000* の数量を持つ注文明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="9d800-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="9d800-127">発注書を確認します。</span><span class="sxs-lookup"><span data-stu-id="9d800-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="9d800-128">製品受領書を転記し、伝票を確認します。</span><span class="sxs-lookup"><span data-stu-id="9d800-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="9d800-129">関連する主勘定 *200140* と *140200* を中断します。</span><span class="sxs-lookup"><span data-stu-id="9d800-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="9d800-130">転記された製品受領書をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="9d800-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="9d800-131">トランザクションが保留中の勘定に転記される可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9d800-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9d800-132">問題の解決</span><span class="sxs-lookup"><span data-stu-id="9d800-132">Issue resolution</span></span>

<span data-ttu-id="9d800-133">製品受領書がキャンセルされると、トランザクションが保留中の勘定に転記される場合があります。なぜなら、この動作では、正しい転記が許可されるからです。</span><span class="sxs-lookup"><span data-stu-id="9d800-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="9d800-134">製品受領書で財務伝票が生成されていない場合でも、製品受領伝票番号が消費されます。</span><span class="sxs-lookup"><span data-stu-id="9d800-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="9d800-135">品目モデルグループで **製品受領書の未収負債** オプションが *いいえ* に設定されている場合、一般会計への転記は行われません。</span><span class="sxs-lookup"><span data-stu-id="9d800-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="9d800-136">ただし、補助元帳で会計を目的として現物イベントが記録され、そのイベントに伝票番号が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="9d800-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="9d800-137">この伝票番号は、在庫トランザクションで参照される伝票番号です。</span><span class="sxs-lookup"><span data-stu-id="9d800-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="9d800-138">[製品受領時に雑費を転記する](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/) のブログ記事に説明されている通り、**製品受領時に負債を見越計上** オプションを *はい* に設定することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="9d800-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="9d800-139">元帳設定の [勘定への転記] の設定が有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="9d800-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9d800-140">問題の説明</span><span class="sxs-lookup"><span data-stu-id="9d800-140">Issue description</span></span>

<span data-ttu-id="9d800-141">この問題は、**買掛金勘定パラメータ** ページの **請求書** タブで、**元帳の掛売勘定に転記** オプションを *はい* に設定された時に発注書が請求されるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="9d800-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="9d800-142">問題を再現する</span><span class="sxs-lookup"><span data-stu-id="9d800-142">Reproduce the issue</span></span>

<span data-ttu-id="9d800-143">この問題を再現する一つの方法は次のプロシージャです。</span><span class="sxs-lookup"><span data-stu-id="9d800-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="9d800-144">**買掛金勘定 \> 設定 \> 買掛金勘定パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9d800-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="9d800-145">**請求書** タブで、**元帳の掛売勘定に転記** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="9d800-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="9d800-146">**在庫管理 \> 設定 \> 転記 \> 転記** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9d800-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="9d800-147">**発注書** タブで、製品の購買経費のすべての明細行が削除されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9d800-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="9d800-148">**買掛金勘定 \> 発注書 \> すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9d800-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="9d800-149">発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="9d800-149">Create a purchase order.</span></span> <span data-ttu-id="9d800-150">**仕入先勘定** フィールドで、*1001 Acme 事務用品* を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d800-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="9d800-151">以下の設定で注文書明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="9d800-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="9d800-152">**品目番号:** *D0011 レーザー プロジェクター*</span><span class="sxs-lookup"><span data-stu-id="9d800-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="9d800-153">**サイト:** *1*</span><span class="sxs-lookup"><span data-stu-id="9d800-153">**Site:** *1*</span></span>
    - <span data-ttu-id="9d800-154">**倉庫:** *11*</span><span class="sxs-lookup"><span data-stu-id="9d800-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="9d800-155">**数量:** *4*</span><span class="sxs-lookup"><span data-stu-id="9d800-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="9d800-156">アクション ペインで、**購入** タブの **アクション** グループで、**確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d800-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="9d800-157">アクション ペインの、**受領** タブの **一般** グループで、**製品受領書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d800-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="9d800-158">**製品受領書の転記** ダイアログボックスの **製品受領書** フィールドに任意の番号を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d800-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="9d800-159">アクション ペインの、**請求書** タブで、**生成** グループから **請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d800-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="9d800-160">**番号** フィールドに、請求書番号として任意の数を入力します。</span><span class="sxs-lookup"><span data-stu-id="9d800-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="9d800-161">照合状態を更新して、転記します。</span><span class="sxs-lookup"><span data-stu-id="9d800-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="9d800-162">発注書から請求書を生成すると、"製品タイプの取引タイプに対する仕入先の勘定番号が存在しません。" というエラーが表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9d800-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9d800-163">問題の解決</span><span class="sxs-lookup"><span data-stu-id="9d800-163">Issue resolution</span></span>

<span data-ttu-id="9d800-164">これは、請求書および請求書グループのパラメータ設定によって異なります。</span><span class="sxs-lookup"><span data-stu-id="9d800-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="9d800-165">詳細については、[発注書と在庫の変動に関する会計転記](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d800-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]