---
title: 在庫原価計算
description: 受入トランザクションと払出トランザクションを決済するプロセスの一環で、行った調整を総勘定元帳に反映して更新するように選択することもできます。
author: AndersGirke
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4cad461c6ff4ef6badeeba868eef45165cf5d33
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431939"
---
# <a name="inventory-close"></a><span data-ttu-id="951ec-103">在庫原価計算</span><span class="sxs-lookup"><span data-stu-id="951ec-103">Inventory close</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="951ec-104">受入トランザクションと払出トランザクションを決済するプロセスの一環で、行った調整を総勘定元帳に反映して更新するように選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="951ec-104">As part of the process to settle issue transactions with receipt transactions, you can also choose to have the general ledger updated to reflect the adjustments that have been made.</span></span>

<span data-ttu-id="951ec-105">在庫原価計算プロセスでは、品目の品目モデル グループで選択した在庫評価方法に基づいて、払出トランザクションを受入トランザクションへと決済します。</span><span class="sxs-lookup"><span data-stu-id="951ec-105">The inventory close process settles issue transactions to receipt transactions, based on the inventory valuation method that is selected in the item’s item model group.</span></span> <span data-ttu-id="951ec-106">決済プロセスの一部として、実施された調整を反映するために総勘定元帳を更新するように指定できます。</span><span class="sxs-lookup"><span data-stu-id="951ec-106">As part of the settlement process, you can specify that the general ledger should be updated, so that it reflects the adjustments that have been made.</span></span> <span data-ttu-id="951ec-107">ただし、在庫決算または再計算が実行されるまで、払出トランザクションは計算された移動平均原価価格で転記されます。</span><span class="sxs-lookup"><span data-stu-id="951ec-107">However, until inventory close or recalculation has been run, issue transactions are posted at the calculated running average cost price.</span></span> 

<span data-ttu-id="951ec-108">在庫決算後は、完了した在庫決算プロセスを取り消さないかぎり、設定した在庫決算日よりも前の期間に転記することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="951ec-108">After inventory close, you can no longer post in periods that are before the inventory closing date that you set, unless you reverse a completed inventory close process.</span></span> <span data-ttu-id="951ec-109">たとえば、在庫決算が 1 月 31 日に終了する期間で実行される場合、1 月 31 日より前の日付ではトランザクションを転記できません。</span><span class="sxs-lookup"><span data-stu-id="951ec-109">For example, if inventory close is run for the period that ends on January 31, you can't post transactions that have a date that is earlier than January 31.</span></span> 

<span data-ttu-id="951ec-110">在庫中の品目は、品目、またはサービスの 2 つの在庫タイプに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="951ec-110">Items in inventory are assigned to one of two inventory types: item or service.</span></span> <span data-ttu-id="951ec-111">在庫決算は両方のタイプに対して同じ処理を行います。</span><span class="sxs-lookup"><span data-stu-id="951ec-111">Inventory close performs the same functions for both types.</span></span> <span data-ttu-id="951ec-112">ただし、サービス品目の在庫決算でも出庫を入庫に対して決済します。</span><span class="sxs-lookup"><span data-stu-id="951ec-112">However, for service items, inventory close still settles issues to receipts.</span></span> 

<span data-ttu-id="951ec-113">在庫決算プロセスの実行頻度は会社によって異なります。</span><span class="sxs-lookup"><span data-stu-id="951ec-113">How often the inventory close process is run varies by company.</span></span> <span data-ttu-id="951ec-114">ただし、在庫決算を実行すべき頻度を判断するにはトランザクション量が便利です。</span><span class="sxs-lookup"><span data-stu-id="951ec-114">However, transaction volume should help determine how often you decide to run inventory close.</span></span> <span data-ttu-id="951ec-115">一般に、多くの会社では、月末の決算および調整手順の一部として在庫決算を実行します。</span><span class="sxs-lookup"><span data-stu-id="951ec-115">In general, most companies run inventory close as part of their month-end close and reconciliation procedures.</span></span>

## <a name="inventory-recalculation-and-the-general-ledger"></a><span data-ttu-id="951ec-116">在庫再計算と総勘定元帳</span><span class="sxs-lookup"><span data-stu-id="951ec-116">Inventory recalculation and the general ledger</span></span>
<span data-ttu-id="951ec-117">月内またはその他の在庫期間中に在庫調整およびその一般会計が必要な場合は、在庫決算ではなく、在庫再計算を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="951ec-117">If adjustments to inventory and the general ledger are required during a month or other inventory period, you can run inventory recalculation instead of inventory close.</span></span> <span data-ttu-id="951ec-118">在庫再計算では在庫トランザクションの調整を行いますが、決済は行いません。</span><span class="sxs-lookup"><span data-stu-id="951ec-118">Inventory recalculation makes adjustments but doesn't make settlements to inventory transactions.</span></span> 

<span data-ttu-id="951ec-119">在庫再計算時、手持在庫が調整され、在庫トランザクションが調整され、在庫再計算および在庫決算が実行されます。</span><span class="sxs-lookup"><span data-stu-id="951ec-119">During inventory recalculation, on-hand inventory is adjusted, inventory transactions are adjusted, and inventory recalculations and inventory closes are run.</span></span> <span data-ttu-id="951ec-120">これらのタスクは、元の在庫トランザクションにリンクされている勘定科目に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="951ec-120">These tasks affect any ledger account that is linked to the original inventory transaction.</span></span> 

<span data-ttu-id="951ec-121">**例**</span><span class="sxs-lookup"><span data-stu-id="951ec-121">**Example**</span></span> 

<span data-ttu-id="951ec-122">販売注文から発注書を作成すると、元の販売注文に使用される一般会計勘定が更新されます。</span><span class="sxs-lookup"><span data-stu-id="951ec-122">When you create a purchase order from a sales order, the general ledger accounts that are used for the original sales order are updated.</span></span> <span data-ttu-id="951ec-123">この品目に割り当てられた品目グループの勘定科目が、販売注文が転記された後に変更されていて、在庫再計算で調整量が作成されている場合でも、調整量は元の勘定科目に転記されます。</span><span class="sxs-lookup"><span data-stu-id="951ec-123">Even if the ledger accounts for the item group that is assigned to the item were changed after the sales order was posted, and an inventory recalculation created an adjustment amount, the adjustment amount is posted to the original ledger accounts.</span></span> <span data-ttu-id="951ec-124">調整済金額は品目に割り当てられた新しい勘定科目には転記されません。</span><span class="sxs-lookup"><span data-stu-id="951ec-124">The adjusted amount isn’t posted to the new ledger accounts that are assigned to the item.</span></span> 

<span data-ttu-id="951ec-125">更新が完了したら、これらのタスクの 1 つのせいで転記された元帳伝票を確認できます。</span><span class="sxs-lookup"><span data-stu-id="951ec-125">After the update is completed, you can review the ledger voucher that is posted because of one of these tasks.</span></span>

1.  <span data-ttu-id="951ec-126">**決算と調整** ページの **概要** タブで、確認する更新を選択します。</span><span class="sxs-lookup"><span data-stu-id="951ec-126">On the **Closing and adjustment** page, on the **Overview** tab, select the update to review.</span></span>
2.  <span data-ttu-id="951ec-127">**詳細** をクリックし、**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="951ec-127">Click **Details**, and then select **Voucher**.</span></span>

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a><span data-ttu-id="951ec-128">総勘定元帳に対する在庫決算プロセスの影響</span><span class="sxs-lookup"><span data-stu-id="951ec-128">Effects of the inventory close process on the general ledger</span></span>
<span data-ttu-id="951ec-129">**決算と調整** ページで実行できる作業のうち、いくつかの作業を行うと、総勘定元帳が更新されます。</span><span class="sxs-lookup"><span data-stu-id="951ec-129">Several of the tasks that you can perform on the **Closing and adjustment** page cause an update to general ledger.</span></span> <span data-ttu-id="951ec-130">たとえば、手持在庫での調整、在庫トランザクション調整、在庫再計算の実行、在庫決算の実行により総勘定元帳が更新されます。</span><span class="sxs-lookup"><span data-stu-id="951ec-130">For example, the general ledger is updated when you make inventory on-hand adjustments, make inventory transaction adjustments, run inventory recalculation, and run inventory close.</span></span> 

<span data-ttu-id="951ec-131">このような作業によって更新される勘定科目は、元の在庫トランザクションにリンクされている科目です。</span><span class="sxs-lookup"><span data-stu-id="951ec-131">The ledger accounts that are updated because of these tasks are linked to the original inventory transaction.</span></span> <span data-ttu-id="951ec-132">たとえば、販売注文が発注書に対して決算されると、元の販売注文に対して使用されている一般会計勘定が調整されます。</span><span class="sxs-lookup"><span data-stu-id="951ec-132">For example, if a sales order is settled to a purchase order, the general ledger accounts that were used for the original sales order are adjusted.</span></span> <span data-ttu-id="951ec-133">この動作は、販売注文の転記後に、この品目に割り当てられた品目グループの勘定科目が変更された場合も同様に発生します。</span><span class="sxs-lookup"><span data-stu-id="951ec-133">This behavior occurs even if the ledger accounts for the item group that is assigned to the item have changed since the sales order was posted.</span></span> <span data-ttu-id="951ec-134">在庫決済によって決済金額が作成された後でも、決済金額は、品目に割り当てられた新しい勘定科目ではなく、元の勘定科目に転記されます。</span><span class="sxs-lookup"><span data-stu-id="951ec-134">After inventory close creates a settlement amount, the settlement amount is still posted to the original ledger accounts, not to the new ledger accounts that are assigned to the item.</span></span> <span data-ttu-id="951ec-135">在庫決算を取り消すと、総勘定元帳も更新される場合があります。</span><span class="sxs-lookup"><span data-stu-id="951ec-135">The general ledger might also be updated if you reverse an inventory close.</span></span> 

> [!NOTE] 
> - <span data-ttu-id="951ec-136">在庫決算は、すべての在庫モデルについて、月末決算手続きにおける必須ステップです。</span><span class="sxs-lookup"><span data-stu-id="951ec-136">Inventory close is a required step in the month-end closing procedure for all inventory models.</span></span> <span data-ttu-id="951ec-137">これには、標準原価と移動平均原価が含まれます。</span><span class="sxs-lookup"><span data-stu-id="951ec-137">This includes Standard and Moving Average Costing.</span></span> <span data-ttu-id="951ec-138">期末日時点で在庫決算が行われていないと、決算期間を閉じることができません。</span><span class="sxs-lookup"><span data-stu-id="951ec-138">You will not be able to close the financial period until an inventory close has been performed as of the period end date.</span></span>
> - <span data-ttu-id="951ec-139">決算手続きを実行する前に、更新中に決済できない品目のリストを表示できます。</span><span class="sxs-lookup"><span data-stu-id="951ec-139">Before you run the closing procedure, you can view a list of items that can't be settled during the update.</span></span>
> - <span data-ttu-id="951ec-140">コンピューター リソースの配分を均等にするために、在庫決算はピーク時以外に実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="951ec-140">We recommend that you run inventory close during off-peak hours, to distribute computing resources more evenly.</span></span>

## <a name="the-inventory-close-log"></a><span data-ttu-id="951ec-141"> 在庫原価計算ログ</span><span class="sxs-lookup"><span data-stu-id="951ec-141">The inventory close log</span></span>
<span data-ttu-id="951ec-142">在庫原価計算プロセスが完了した後、トランザクションを完全に決済できなかったという理由で単位原価価格が間違っている可能性があることを、メッセージ センターのメッセージが通知する場合があります。</span><span class="sxs-lookup"><span data-stu-id="951ec-142">After the inventory close process has been completed, a message in the message center might inform you that a unit cost price might be incorrect because a transaction could not be fully settled.</span></span> 

<span data-ttu-id="951ec-143">このメッセージが表示される前に、システムが品目番号と該当するトランザクションを報告します。</span><span class="sxs-lookup"><span data-stu-id="951ec-143">Before this message is shown, the system reports the item number and the affected transaction.</span></span> <span data-ttu-id="951ec-144">メッセージは、このトランザクションに使用された原価金額が、在庫原価計算のゆえに、更新されなかったことを通知します。</span><span class="sxs-lookup"><span data-stu-id="951ec-144">The message informs you that the cost amount that is used for this transaction wasn't updated because of the inventory close.</span></span> <span data-ttu-id="951ec-145">このメッセージは、払出タイプのトランザクションが決済できない場合に表示されます。</span><span class="sxs-lookup"><span data-stu-id="951ec-145">This message appears when a transaction of the issue type can't be settled.</span></span> 

<span data-ttu-id="951ec-146">在庫原価計算プロセスの間、システムは、指定された決算日までの払出数が入庫よりも多いかどうかを確認するために、各財務分析コードをチェックします。</span><span class="sxs-lookup"><span data-stu-id="951ec-146">During the inventory close process, the system checks each financial dimension to see whether there are more issues than receipts up to the specified closing date.</span></span> <span data-ttu-id="951ec-147">仕入先請求書がまだ受け取ってないゆえに、または高度なレベルの生産に含まれる部品表 (BOM) コンポーネントが財務上転記されていないゆえに、発注書の在庫トランザクションが財務上完全に転記されていないとき、このタイプの不均衡が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="951ec-147">This type of imbalance can occur when an inventory transaction from a purchase order isn't fully posted financially, either because the vendor invoice hasn't been received, or because bill of materials (BOM) components that are included in a production on a higher level aren't financially posted.</span></span> <span data-ttu-id="951ec-148">(副生産が原価計算されていない。) この場合は、十分な入庫情報が得られないので、それ以降の在庫原価計算では、すべての払出が適切な原価価格に調整されません。</span><span class="sxs-lookup"><span data-stu-id="951ec-148">(The sub-production isn't cost-calculated.) In this case, the subsequent close won't adjust all issues to the correct cost price, because not enough receipt information is available.</span></span> 

<span data-ttu-id="951ec-149">決算手続きを実行するごとに、システムによって警告が含まれたログが保存され、表示できるかどうか示されます。</span><span class="sxs-lookup"><span data-stu-id="951ec-149">For each run of the closing procedure, the system indicates whether a log that contains the warnings is stored and can be viewed.</span></span> 

<span data-ttu-id="951ec-150">メッセージでの警告が多数表示される場合は、次のアクションを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="951ec-150">If you receive many warnings in the message, we recommend that you perform the following actions:</span></span>

-   <span data-ttu-id="951ec-151">入庫を財務上更新する。</span><span class="sxs-lookup"><span data-stu-id="951ec-151">Update receipts financially.</span></span>
-   <span data-ttu-id="951ec-152">決算日を繰り上げる。</span><span class="sxs-lookup"><span data-stu-id="951ec-152">Advance the closing date.</span></span>
-   <span data-ttu-id="951ec-153">業務手順を再評価する。</span><span class="sxs-lookup"><span data-stu-id="951ec-153">Reevaluate the business procedures.</span></span>

<span data-ttu-id="951ec-154">状況によっては、警告についてどうにもできない場合があります。</span><span class="sxs-lookup"><span data-stu-id="951ec-154">In some circumstances, you might not be able to do anything about the warnings.</span></span> <span data-ttu-id="951ec-155">たとえば、マークされた発注書の財務日付が決算日の後になっている場合にマーキングを使用すると、決算日は変更できません。</span><span class="sxs-lookup"><span data-stu-id="951ec-155">For example, if marking is used, and the marked purchase order has a financial date that is after the closing date, the closing date can't be changed.</span></span>

## <a name="reversing-a-completed-inventory-close"></a><span data-ttu-id="951ec-156">完了した在庫決算の取消</span><span class="sxs-lookup"><span data-stu-id="951ec-156">Reversing a completed inventory close</span></span>
<span data-ttu-id="951ec-157">決済を調整前の状態に戻すために、完了した在庫決算を取り消す必要が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="951ec-157">Occasionally, you might have to reverse a completed inventory close to return settlements to the state that they had before adjustments were made.</span></span> <span data-ttu-id="951ec-158">完了した在庫決算を取り消すと、在庫が再び開き、在庫決算に含まれる期間の転記ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="951ec-158">When you reverse a completed inventory close, inventory is reopened to enable posting in the period that the inventory close covers.</span></span> <span data-ttu-id="951ec-159">総勘定元帳でも関連する変更が行われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="951ec-159">Related changes might also be made in the general ledger.</span></span> <span data-ttu-id="951ec-160">調整が終了してから、作業している期間に対して在庫決算を再び実行します。</span><span class="sxs-lookup"><span data-stu-id="951ec-160">After you've finished making adjustments, you can run inventory close again for the period that you're working with.</span></span> 

> [!NOTE] 
> <span data-ttu-id="951ec-161">終了済みの最終の在庫期間のみを再オープンすることができます。</span><span class="sxs-lookup"><span data-stu-id="951ec-161">Only the last inventory period that was closed can be reopened.</span></span> <span data-ttu-id="951ec-162">初期の在庫決算を取り消すには、最新の決算から在庫原価計算プロシージャを個別に取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="951ec-162">To reverse an earlier inventory close, you must reverse each subsequent inventory close one at a time, starting with the most recent close.</span></span>

