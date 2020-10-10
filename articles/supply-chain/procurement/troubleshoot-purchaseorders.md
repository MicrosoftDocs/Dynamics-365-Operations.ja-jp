---
title: 発注書のトラブルシューティング
description: このトピックでは、発注書と作業する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: e55974f65577170880e60095f1ba74ea7366e592
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834386"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="156e7-103">発注書のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="156e7-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="156e7-104">このトピックでは、発注書と作業する際に発生する可能性がある問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="156e7-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="156e7-105">行番号が完全に配布された後にのみアクションを完了できます。</span><span class="sxs-lookup"><span data-stu-id="156e7-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="156e7-106">この問題は、発注書の配分に不整合があるために発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="156e7-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="156e7-107">この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="156e7-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="156e7-108">詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="156e7-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="156e7-109">データ管理を通して発注書をインポートした場合、発注書明細行番号は、システム パラメータで定義されている増分に従いません。</span><span class="sxs-lookup"><span data-stu-id="156e7-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="156e7-110">問題の説明</span><span class="sxs-lookup"><span data-stu-id="156e7-110">Issue description</span></span>

<span data-ttu-id="156e7-111">既定では、*発注書明細行 V2*  データ エンティティを通じてインポートされた発注書明細行の自動生成された行番号は、システム パラメータで指定されたシステム行番号の増分を使用しません。</span><span class="sxs-lookup"><span data-stu-id="156e7-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="156e7-112">ユーザー インターフェイス (UI) を通じて発注書を手動で作成し、明細行を追加すると、行番号が正しく増加します。</span><span class="sxs-lookup"><span data-stu-id="156e7-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="156e7-113">ただし、データ管理フレームワーク (DMF) を使用すると、正しく増加しません。</span><span class="sxs-lookup"><span data-stu-id="156e7-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="156e7-114">この問題が発生するのは、DMF で明細行をインポートしたときに、インポートされたエンティティで行番号が割り当てられていない場合に、DMF メソッドを使用してそれを割り当てるためです。</span><span class="sxs-lookup"><span data-stu-id="156e7-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="156e7-115">このメソッドでは、常に行番号が 1 ずつ増加します。</span><span class="sxs-lookup"><span data-stu-id="156e7-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="156e7-116">問題の回避策</span><span class="sxs-lookup"><span data-stu-id="156e7-116">Issue workaround</span></span>

<span data-ttu-id="156e7-117">発注書明細行をインポートするときに、目的の行番号が [データエンティティの行番号] フィールドに既に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="156e7-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="156e7-118">この場合、DMF は行番号を上書きしません。</span><span class="sxs-lookup"><span data-stu-id="156e7-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="156e7-119">既定の税グループと既定の現金割引が請求元仕入先に入力されていません。</span><span class="sxs-lookup"><span data-stu-id="156e7-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="156e7-120">顧客 ID とは異なる請求元仕入先を使用している場合、既定の税グループと既定の現金割引は、発注書が作成されるときに請求先/元 ID から入力されません。</span><span class="sxs-lookup"><span data-stu-id="156e7-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="156e7-121">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="156e7-121">This behavior is by design.</span></span> <span data-ttu-id="156e7-122">税グループ、現金割引、およびその他の価格情報の既定値は、請求先/元 ID ではなく顧客 ID に基づいています。</span><span class="sxs-lookup"><span data-stu-id="156e7-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="156e7-123">発注書の確認に "オブジェクト参照が設定されていません" というエラーが表示されるか、仕入先請求書の転記中に "呼び出しのターゲットが例外をスローしました" という例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="156e7-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="156e7-124">この問題は、発注書の配分に不整合があるために発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="156e7-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="156e7-125">この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="156e7-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="156e7-126">詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="156e7-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="156e7-127">1 つ以上の勘定配布が、過剰配布されているか、配布中であるかのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="156e7-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="156e7-128">問題の説明</span><span class="sxs-lookup"><span data-stu-id="156e7-128">Issue description</span></span>

<span data-ttu-id="156e7-129">"1 つ以上の勘定配布が過剰配分されているか、配分中である" というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="156e7-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="156e7-130">問題の解決</span><span class="sxs-lookup"><span data-stu-id="156e7-130">Issue resolution</span></span>

<span data-ttu-id="156e7-131">この問題は、発注書の配分に不整合があるために発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="156e7-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="156e7-132">この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="156e7-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="156e7-133">詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="156e7-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="156e7-134">自分が作成した発注書のみを表示できますか?</span><span class="sxs-lookup"><span data-stu-id="156e7-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="156e7-135">この機能は現在使用できません。</span><span class="sxs-lookup"><span data-stu-id="156e7-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="156e7-136">発注書の登録済在庫に対して、在庫を予約したりトランザクションを作成したりすることはできますか ?</span><span class="sxs-lookup"><span data-stu-id="156e7-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="156e7-137">問題の説明</span><span class="sxs-lookup"><span data-stu-id="156e7-137">Issue description</span></span>

<span data-ttu-id="156e7-138">品目が発注書の *登録済* 状態にある場合でも 、在庫を引当てることができます。</span><span class="sxs-lookup"><span data-stu-id="156e7-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="156e7-139">つまり、登録済みの在庫に対してトランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="156e7-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="156e7-140">問題を再現する</span><span class="sxs-lookup"><span data-stu-id="156e7-140">Reproduce the issue</span></span>

<span data-ttu-id="156e7-141">この問題を再現する一つの方法は次のプロシージャです。</span><span class="sxs-lookup"><span data-stu-id="156e7-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="156e7-142">発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="156e7-142">Create a purchase order.</span></span>
2. <span data-ttu-id="156e7-143">発注書明細行を登録します。</span><span class="sxs-lookup"><span data-stu-id="156e7-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="156e7-144">登録済みの在庫に対して引当またはトランザクションを生成できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="156e7-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="156e7-145">問題の解決</span><span class="sxs-lookup"><span data-stu-id="156e7-145">Issue resolution</span></span>

<span data-ttu-id="156e7-146">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="156e7-146">This behavior is by design.</span></span> <span data-ttu-id="156e7-147">これは、登録された品目が倉庫または在庫に現物到着しており、引当に使用できるようになっていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="156e7-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="156e7-148">購買注文には、法人の言語設定は反映されません。</span><span class="sxs-lookup"><span data-stu-id="156e7-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="156e7-149">問題の説明</span><span class="sxs-lookup"><span data-stu-id="156e7-149">Issue description</span></span>

<span data-ttu-id="156e7-150">発注書上の製品名は、発注書が作成された法人に対して設定されている言語ではなく、システム言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="156e7-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="156e7-151">問題を再現する</span><span class="sxs-lookup"><span data-stu-id="156e7-151">Reproduce the issue</span></span>

<span data-ttu-id="156e7-152">この問題を再現する一つの方法は次のプロシージャです。</span><span class="sxs-lookup"><span data-stu-id="156e7-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="156e7-153">システム言語を *EN-US* (米国英語) に設定します。</span><span class="sxs-lookup"><span data-stu-id="156e7-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="156e7-154">製品名の翻訳に、*EN-US* と *DE* (ドイツ語) 言語が維持される製品があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="156e7-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="156e7-155">法人の言語を *"DE"* に変更します。</span><span class="sxs-lookup"><span data-stu-id="156e7-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="156e7-156">言語として *DE* が設定されている法人では、製品を含む発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="156e7-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="156e7-157">製品名が米国英語 (システム言語) で表示されたままになっていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="156e7-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="156e7-158">問題の解決</span><span class="sxs-lookup"><span data-stu-id="156e7-158">Issue resolution</span></span>

<span data-ttu-id="156e7-159">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="156e7-159">This behavior is by design.</span></span> <span data-ttu-id="156e7-160">発注書では、製品は常にシステム言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="156e7-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="156e7-161">発注書の言語は、確認仕訳帳が作成されたときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="156e7-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="156e7-162">製品エンティティ別の承認済仕入先リストでは、有効日を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="156e7-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="156e7-163">問題の説明</span><span class="sxs-lookup"><span data-stu-id="156e7-163">Issue description</span></span>

<span data-ttu-id="156e7-164">たとえば、ある製品には承認済仕入先があり、有効日は 2018 年 1 月 11 日 (*01/11/2018*)、有効期限は *なし* となっています。</span><span class="sxs-lookup"><span data-stu-id="156e7-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="156e7-165">有効日を 2018 年 1 月 10 日 (*01/10/2018*) または 2018 年 1 月 12 日 (*01/12/2018*) に変更しようとすると、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="156e7-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="156e7-166">承認済サプライヤー リスト (PdsApproveVendorList) にレコードを作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="156e7-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="156e7-167">'有効期限' の値は、'有効' 値以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="156e7-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="156e7-168">問題の解決</span><span class="sxs-lookup"><span data-stu-id="156e7-168">Issue resolution</span></span>

<span data-ttu-id="156e7-169">仕入先の承認期間のみ延長できます。</span><span class="sxs-lookup"><span data-stu-id="156e7-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="156e7-170">次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="156e7-170">The following rules apply:</span></span>

- <span data-ttu-id="156e7-171">有効日を、品目の仕入先の既存のレコード (期間) よりも前に変更するには、新しい期間の有効期限を既存のレコードの有効期限のすべての日付より前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="156e7-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="156e7-172">既存の期間より後の日付に有効期限を変更するには、既存のレコードの有効日が最新の有効期限の後にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="156e7-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="156e7-173">仕入先が承認する合計期間を減らすには、既存のレコードを削除または変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="156e7-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="156e7-174">または、インポート中に **切り捨て** スイッチを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="156e7-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="156e7-175">このスイッチは、品目ごとに承認済仕入先のテーブル内の既存のレコードをすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="156e7-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="156e7-176">レコードに有効日が *01/11/2018*、有効期限が *なし* となっている問題の説明で説明されているシナリオでは、有効期限が常にあるという、問題の説明で説明されているシナリオについては、有効日が *01/10/2018* で有効期限が *なし* となっている新規レコードをインポートできます。</span><span class="sxs-lookup"><span data-stu-id="156e7-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="156e7-177">ただし、データ管理を通じて有効日が *01/12/2018* に更新されるように期間を短縮することはできません。</span><span class="sxs-lookup"><span data-stu-id="156e7-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="156e7-178">この変更は UI を通じて行なわなければなりません。</span><span class="sxs-lookup"><span data-stu-id="156e7-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a><span data-ttu-id="156e7-179">発注書ヘッダーの配送先住所を変更した後、配送先名は同期されません。</span><span class="sxs-lookup"><span data-stu-id="156e7-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="156e7-180">問題の説明</span><span class="sxs-lookup"><span data-stu-id="156e7-180">Issue description</span></span>

<span data-ttu-id="156e7-181">発注書のヘッダーの住所が配送先住所ではない住所に更新されます。</span><span class="sxs-lookup"><span data-stu-id="156e7-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="156e7-182">住所は発注書上で更新されますが、更新された住所に基づいて配送先名が更新されることはありません。</span><span class="sxs-lookup"><span data-stu-id="156e7-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="156e7-183">問題の解決</span><span class="sxs-lookup"><span data-stu-id="156e7-183">Issue resolution</span></span>

<span data-ttu-id="156e7-184">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="156e7-184">This behavior is by design.</span></span> <span data-ttu-id="156e7-185">選択された住所は配送先住所として分類される必要があります。</span><span class="sxs-lookup"><span data-stu-id="156e7-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="156e7-186">それ以外の場合、選択した住所に基づいて配送先名が更新されることはありません。</span><span class="sxs-lookup"><span data-stu-id="156e7-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="156e7-187">発注書をキャンセルしたユーザーを見つけることができますか ?</span><span class="sxs-lookup"><span data-stu-id="156e7-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="156e7-188">この情報は、発注書が変更管理の対象となる場合にのみ追跡されます。</span><span class="sxs-lookup"><span data-stu-id="156e7-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="156e7-189">変更管理を使用すると、変更 (キャンセル) を送信したユーザーと、変更を承認したユーザーを確認できます。</span><span class="sxs-lookup"><span data-stu-id="156e7-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
