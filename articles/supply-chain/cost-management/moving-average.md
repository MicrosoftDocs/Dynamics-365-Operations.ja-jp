---
title: 移動平均
description: 移動平均は、平均原則に基づく永久原価法であり、購買原価が変化するとき、在庫払出の原価は変化しません。 差額は資本化され、比例計算に基づきます。 残りの金額が経費となります。
author: AndersGirke
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3616ade55b2055a30af8ebc2da7e2ade41973543
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809713"
---
# <a name="moving-average"></a><span data-ttu-id="a32d6-105">移動平均</span><span class="sxs-lookup"><span data-stu-id="a32d6-105">Moving average</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a32d6-106">移動平均は、平均原則に基づく永久原価法であり、購買原価が変化するとき、在庫払出の原価は変化しません。</span><span class="sxs-lookup"><span data-stu-id="a32d6-106">Moving average is a perpetual costing method based on the average principle, where the costs on inventory issues do not change when the purchase cost does.</span></span> <span data-ttu-id="a32d6-107">差額は資本化され、比例計算に基づきます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-107">The difference is capitalized and is based on a proportional calculation.</span></span> <span data-ttu-id="a32d6-108">残りの金額が経費となります。</span><span class="sxs-lookup"><span data-stu-id="a32d6-108">The amount that remains is expensed.</span></span>

<span data-ttu-id="a32d6-109">移動平均を使用する場合、在庫の決済および在庫のマーキングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a32d6-109">When you use moving average, inventory settlements and inventory marking are not supported.</span></span> <span data-ttu-id="a32d6-110">在庫原価計算は、在庫モデル グループとして移動平均がある製品には影響を与えず、トランザクション間で決済を生成しません</span><span class="sxs-lookup"><span data-stu-id="a32d6-110">Inventory close does not affect products that have moving average as the inventory model group, and it does not generate any settlements between the transactions.</span></span>

<span data-ttu-id="a32d6-111">次に、移動平均原価を原価計算方法として使用するときの前提条件を示します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-111">The following are prerequisites when you use moving average cost as a costing method.</span></span>

1. <span data-ttu-id="a32d6-112">**品目モデル グループ** ページで、**在庫モデル** フィールドで、**移動平均** がオンになっている品目モデル グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-112">On the **Item model groups** page, set up an item model group that has **Moving average** selected in the **Inventory model** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a32d6-113">既定では、**移動平均** を選択した場合、**現物在庫の転記** フィールドと **資産在庫の転記** フィールドも選択されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-113">By default, when **Moving average** is selected, the **Post physical inventory** and **Post financial inventory** fields are also selected.</span></span>

1. <span data-ttu-id="a32d6-114">**転記** ページで、**移動平均の価格差** に勘定を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-114">On the **Posting** page, assign accounts to the **Price difference for moving average**.</span></span> <span data-ttu-id="a32d6-115">原価を比例して経費処理する場合は、**移動平均の価格差異** の勘定が使用できます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-115">You use the **Price difference for moving average** account when cost has to be proportionally expensed.</span></span> <span data-ttu-id="a32d6-116">これは、次の 2 つのシナリオで発生します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-116">This occurs in following two scenarios:</span></span>
    - <span data-ttu-id="a32d6-117">これが起きるのは、購買入庫と仕入請求書の原価に差異があるためであり、また元の在庫数量と現在の手持在庫数量に差異があるためです。</span><span class="sxs-lookup"><span data-stu-id="a32d6-117">There is a difference in cost between a purchase receipt and the purchase invoice because there is a difference between the original inventory quantity and the current on-hand quantity.</span></span>
    - <span data-ttu-id="a32d6-118">トランザクションによって、在庫がマイナスからゼロになり、トランザクション原価と現在の移動平均原価との間に差異が生じます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-118">The transactions bring the inventory from negative to zero, and there is a difference between the transaction cost and the current moving average cost.</span></span>

1. <span data-ttu-id="a32d6-119">**転記** ページの **在庫** タブで、勘定を **移動平均の原価の再評価**  の勘定に割り当てます。生産に対して移動平均原価を新しいユニット単位で調節する場合は、**移動平均の原価の再評価** の勘定を使用します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-119">On the **Posting** page, assign accounts to the **Cost revaluation for moving average** accounts on the **Inventory** tab. You use the **Cost revaluation for moving average** account when you want to adjust the moving average cost for a product to a new unit price.</span></span>

1. <span data-ttu-id="a32d6-120">**リリースされた製品** ページで、移動平均品目モデル グループを製品に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-120">On the **Released products** page, assign the moving average item model group to the product.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a32d6-121">在庫クローズプロセスは、会計期間のみを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-121">The inventory close process only closes the accounting period.</span></span> <span data-ttu-id="a32d6-122">これは、品目モデル グループとして割り当てられた移動平均がある製品には影響しません。</span><span class="sxs-lookup"><span data-stu-id="a32d6-122">It does not affect products that have moving average assigned to them as an item model group.</span></span>

## <a name="convert-to-the-moving-average-costing-method"></a><span data-ttu-id="a32d6-123">移動平均原価計算方法への換算</span><span class="sxs-lookup"><span data-stu-id="a32d6-123">Convert to the moving average costing method</span></span>

<span data-ttu-id="a32d6-124">製品は、移動平均在庫評価方法を使用するように変換できます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-124">Products can be converted to use the moving average inventory valuation method.</span></span> <span data-ttu-id="a32d6-125">このタイプの変換は、通常、現年度の最後の月を締めた後の年度の最後に行われます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-125">This type of conversion is usually done at the end of the year, after the last month of the current year is closed.</span></span> <span data-ttu-id="a32d6-126">これには、製品の現在の価格モデルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-126">It is done by using the product’s current costing model.</span></span> <span data-ttu-id="a32d6-127">在庫原価計算方法を、平均原価または標準原価に基づく原価計算方法から移動平均に基づくメソッドへ変更できます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-127">You can change your inventory costing method from a costing method that is based on average cost or standard cost to a method that is based on moving average.</span></span>

<span data-ttu-id="a32d6-128">原価計算方法を標準原価計算方法から移動平均方法に変更する場合、次の作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a32d6-128">If you are changing your costing method from a standard costing method to a moving average method, you have to complete the following tasks:</span></span>

1. <span data-ttu-id="a32d6-129">在庫数量と値が 0 (ゼロ) になるように調整します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-129">Make adjustments to get inventory quantities and values down to 0 (zero).</span></span>
1. <span data-ttu-id="a32d6-130">在庫金額と数量が 0 (ゼロ) の後に、品目モデル グループを移動平均に変更します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-130">After the inventory value and quantity are 0 (zero), change the item model group to moving average.</span></span>
1. <span data-ttu-id="a32d6-131">数量と価格が在庫に戻るように調整します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-131">Make adjustments to get the quantity and value back into inventory.</span></span>

<span data-ttu-id="a32d6-132">在庫原価計算方法を、移動平均方法から、先入れ先出し (FIFO) 方法、後入れ先出し (LIFO)、または加重平均方法には変更できません。</span><span class="sxs-lookup"><span data-stu-id="a32d6-132">You cannot change your inventory costing method from a moving average method to a First in, First out (FIFO) method, a Last in, First out (LIFO) method, or a weighted average method.</span></span>

> [!NOTE]
> <span data-ttu-id="a32d6-133">標準原価から移動加重平均への換算は、手動プロセスです。</span><span class="sxs-lookup"><span data-stu-id="a32d6-133">Converting from standard cost to moving weighted average is a manual process.</span></span>

<span data-ttu-id="a32d6-134">次の例では、移動平均原価計算方法を使用した効果について説明します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-134">The following examples illustrate the effect of using the moving average costing method.</span></span> <span data-ttu-id="a32d6-135">コンフィギュレーションには次の 4 つがあります。</span><span class="sxs-lookup"><span data-stu-id="a32d6-135">There are four configurations:</span></span>

- <span data-ttu-id="a32d6-136">発注書と比例して経理処理する原価との差異</span><span class="sxs-lookup"><span data-stu-id="a32d6-136">Purchase order and proportionally expensed cost difference</span></span>
- <span data-ttu-id="a32d6-137">移動平均の製品および在庫調整</span><span class="sxs-lookup"><span data-stu-id="a32d6-137">Moving average product and inventory adjustment</span></span>
- <span data-ttu-id="a32d6-138">生産での移動平均</span><span class="sxs-lookup"><span data-stu-id="a32d6-138">Moving average with production</span></span>
- <span data-ttu-id="a32d6-139">前の日付のトランザクションでの移動平均</span><span class="sxs-lookup"><span data-stu-id="a32d6-139">Moving average with a backdated transaction</span></span>

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a><span data-ttu-id="a32d6-140">発注書と比例して経理処理する原価との差異</span><span class="sxs-lookup"><span data-stu-id="a32d6-140">Purchase order and proportionally expensed cost difference</span></span>

<span data-ttu-id="a32d6-141">移動平均では、製品の原価は購買入庫によって決まります。</span><span class="sxs-lookup"><span data-stu-id="a32d6-141">With moving average, the product’s cost is determined by the purchase receipt.</span></span> <span data-ttu-id="a32d6-142">仕入請求書を転記するとき、購買入庫と仕入請求書の原価に違いがある場合、差額は在庫の現在の製品に合わせて調整され、残りの金額が経費として処理されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-142">When the purchase invoice is posted, if there is a difference in cost between the purchase receipt and the purchase invoice, the difference is proportionally adjusted to the current products in stock, and any remaining amount is expensed.</span></span>

<span data-ttu-id="a32d6-143">この例では、発注書が作成され、ある原価で入庫され、仕入請求書は異なる原価で転記されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-143">In this example, a purchase order is created and received at one cost, and the purchase invoice is posted with a different cost.</span></span>

1. <span data-ttu-id="a32d6-144">数量 2、単価 10.00 の発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-144">Create a purchase order for a quantity of 2 and a unit price of 10.00.</span></span>
1. <span data-ttu-id="a32d6-145">その製品の購買入庫を作成します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-145">Create a purchase receipt of the product.</span></span>
1. <span data-ttu-id="a32d6-146">数量 1、単価 10.00 の販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-146">Create a sales order for a quantity of 1 and a unit price of 10.00.</span></span>
1. <span data-ttu-id="a32d6-147">数量 2、単価 12.00 の発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-147">Create a purchase invoice for a quantity of 2 and a unit price of 12.00.</span></span>

<span data-ttu-id="a32d6-148">単価 2.00 の差額は、仕入請求書の転記時に、[移動平均の価格差異] 勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-148">The difference in unit price, 2.00, is posted to the Price difference for moving average account when the purchase invoice is posted.</span></span> <span data-ttu-id="a32d6-149">その理由は、2 つの製品を 20.00 の原価で購入したことによります。</span><span class="sxs-lookup"><span data-stu-id="a32d6-149">The reason is that two products were purchased for a cost of 20.00.</span></span> <span data-ttu-id="a32d6-150">製品の 1 つは、単価 10.00 で販売されました。</span><span class="sxs-lookup"><span data-stu-id="a32d6-150">One of the products was sold for a unit price of 10.00.</span></span> <span data-ttu-id="a32d6-151">仕入請求書は、数量 2 が単価 12.00 で転記されました。</span><span class="sxs-lookup"><span data-stu-id="a32d6-151">The purchase invoice was posted at a unit price of 12.00 with a quantity of 2.</span></span> <span data-ttu-id="a32d6-152">製品の単価は 14.00 で転記することはできません。</span><span class="sxs-lookup"><span data-stu-id="a32d6-152">The unit price of the product cannot be posted at 14.00.</span></span>

## <a name="moving-average-product-and-inventory-adjustment"></a><span data-ttu-id="a32d6-153">移動平均の製品および在庫調整</span><span class="sxs-lookup"><span data-stu-id="a32d6-153">Moving average product and inventory adjustment</span></span>

<span data-ttu-id="a32d6-154">製品の移動平均原価を調整する必要がある場合、在庫調整は今日の日付に許可されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-154">If you need to adjust the moving average cost of a product, inventory adjustments are allowed as of today’s date.</span></span> <span data-ttu-id="a32d6-155">在庫調整の日付をさかのぼって、製品の移動平均原価を訂正することができません。</span><span class="sxs-lookup"><span data-stu-id="a32d6-155">You cannot backdate an inventory adjustment to correct the moving average cost of a product.</span></span> <span data-ttu-id="a32d6-156">後続のトランザクションによる原価フローを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="a32d6-156">You cannot have the cost flow through subsequent transactions.</span></span>

<span data-ttu-id="a32d6-157">この例では、移動平均原価は製品に合わせて調整されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-157">In this example, the moving average cost is adjusted for a product.</span></span>

1. <span data-ttu-id="a32d6-158">移動平均原価の調整の対象となる製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-158">Select the product that you want to adjust the moving average cost for.</span></span> 

 > [!NOTE]
 > <span data-ttu-id="a32d6-159">**移動平均の再評価** ページでは、製品に対して使用可能な在庫を確認できます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-159">The **Revaluation for moving average** page examines the inventory available for a product.</span></span> <span data-ttu-id="a32d6-160">選択した製品は、転記数量が 1、転記価格が 12.00、転記された単位原価が 12.00、そして単位原価が 12.00 です。</span><span class="sxs-lookup"><span data-stu-id="a32d6-160">The product selected has a posted quantity of 1, a posted a value of 12.00, a posted unit cost of 12.00, and a unit cost of 12.00.</span></span>
    
1. <span data-ttu-id="a32d6-161">ここで、**単位原価** フィールドを 16.00 に更新します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-161">Update the **Unit cost** field to 16.00.</span></span> <span data-ttu-id="a32d6-162">システムは残りのフィールドを計算します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-162">The system calculates the remaining fields.</span></span>
1. <span data-ttu-id="a32d6-163">調整が転記されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-163">The adjustment is posted.</span></span>

> [!NOTE]
> <span data-ttu-id="a32d6-164">移動平均原価は、今日の日付でのみ調整できます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-164">You can only adjust the moving average cost as of today’s date.</span></span>

<span data-ttu-id="a32d6-165">**伝票の決済** ページで、移動平均の原価の再評価の勘定に転記された 4.00 の調整を確認できます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-165">On the **Settlements for voucher** page, you can see an adjustment of 4.00 posted to the Cost revaluation for moving average account.</span></span>

## <a name="moving-average-with-production"></a><span data-ttu-id="a32d6-166">生産での移動平均</span><span class="sxs-lookup"><span data-stu-id="a32d6-166">Moving average with production</span></span>

<span data-ttu-id="a32d6-167">移動平均で、生産された品目がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-167">Moving average supports produced items.</span></span> <span data-ttu-id="a32d6-168">運用環境で移動平均の使用を計画する場合は、**生産管理パラメーター** ページの **見積原価価格の使用** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a32d6-168">If you plan to use moving average in a production environment, select **Use estimated cost price** on the **Production control parameters** page.</span></span> <span data-ttu-id="a32d6-169">すなわち、見積時に計算された原価価格が、実際の BOM 計算原価価格の代わりに使用されるということです。</span><span class="sxs-lookup"><span data-stu-id="a32d6-169">This means that the cost price that is calculated during estimation is used instead of the actual BOM calculation cost price.</span></span>

## <a name="moving-average-with-a-backdated-transaction"></a><span data-ttu-id="a32d6-170">前の日付のトランザクションでの移動平均</span><span class="sxs-lookup"><span data-stu-id="a32d6-170">Moving average with a backdated transaction</span></span>

<span data-ttu-id="a32d6-171">さかのぼった日付のトランザクションが現在の移動平均原価に割り当てられ、製品の現物の数量が更新されますが、製品の移動平均原価には影響しません。</span><span class="sxs-lookup"><span data-stu-id="a32d6-171">Backdated transactions are assigned the current moving average cost, and the product’s physical quantity is updated, but the product’s moving average cost is not affected.</span></span> <span data-ttu-id="a32d6-172">この移動平均の例では、移動平均の製品に対してさかのぼったトランザクションが転記されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-172">In this moving average example, a backdated transaction for a moving average product is posted.</span></span>

1. <span data-ttu-id="a32d6-173">数量 1、原価 20.00 の移動平均製品の在庫調整を作成します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-173">Create an inventory adjustment for the moving average product for a quantity of 1 and a cost of 20.00.</span></span>
1. <span data-ttu-id="a32d6-174">製品の在庫トランザクション履歴は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="a32d6-174">The inventory transaction history for the product would resemble the following:</span></span>
    - <span data-ttu-id="a32d6-175">在庫トランザクションは 1、原価は 16.00、転記日付は 1 月 15 日、トランザクションの日付は 1 月 15 日。</span><span class="sxs-lookup"><span data-stu-id="a32d6-175">An inventory transaction of 1, a cost of 16.00, a posting date of January 15, and a transaction date of January 15.</span></span>
    - <span data-ttu-id="a32d6-176">在庫調整は 1、原価は 20.00、転記日付は 1 月 1 日、トランザクションの日付は 1 月 15 日。</span><span class="sxs-lookup"><span data-stu-id="a32d6-176">An inventory adjustment of 1, a cost of 20.00, a posting date of January 1, and a transaction date of January 15.</span></span>
1. <span data-ttu-id="a32d6-177">調整を転記します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-177">Post the adjustment.</span></span>

<span data-ttu-id="a32d6-178">**在庫トランザクション** ページで、製品の現在の移動平均が 16.00 のままで、4.00 が経費として処理されたことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-178">On the **Inventory transactions** page, you can see that 4.00 is expensed as the current moving average for the product is 16.00.</span></span> <span data-ttu-id="a32d6-179">過去の日付で転記することが可能ですが、原価の差額は経費として処理され、移動平均原価には影響しません。</span><span class="sxs-lookup"><span data-stu-id="a32d6-179">You can post in the past, but the difference in cost is expensed, so the moving average cost is not affected.</span></span>

## <a name="negative-inventory-balances"></a><span data-ttu-id="a32d6-180">マイナス在庫残高</span><span class="sxs-lookup"><span data-stu-id="a32d6-180">Negative inventory balances</span></span>

<span data-ttu-id="a32d6-181">トランザクションは、トランザクションが負、ゼロ、または正の後の新しい手持在庫の数量に応じて異なる方法で処理されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-181">Transactions are handled differently depending on whether the new on-hand quantity after the transaction is negative, zero, or positive.</span></span>

### <a name="new-balance-is-negative-or-zero"></a><span data-ttu-id="a32d6-182">新しい残高は負またはゼロです</span><span class="sxs-lookup"><span data-stu-id="a32d6-182">New balance is negative or zero</span></span>

<span data-ttu-id="a32d6-183">新しい手持在庫数量が負であるかゼロである場合、トランザクションは現在の平均原価で原価計算されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-183">If the new on-hand quantity is negative or zero, the transaction is costed at the current average costs.</span></span> <span data-ttu-id="a32d6-184">購買価格と現在の平均原価との間に差異がある場合は、**移動平均の価格差** に転記されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-184">If there is a difference between the purchase price and the current average costs, it's posted to **Price difference for moving average**.</span></span>

### <a name="new-balance-is-positive"></a><span data-ttu-id="a32d6-185">新しい残高は正です</span><span class="sxs-lookup"><span data-stu-id="a32d6-185">New balance is positive</span></span>

<span data-ttu-id="a32d6-186">トランザクション後に新しい手持在庫数量が正の場合は、次の表に示すように、トランザクションは 2 つの部分に分割され、別の方法で原価が計算されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-186">If the new on-hand quantity is positive after the transaction, the transaction is split into two parts and costed differently, as summarized in the following table.</span></span>

| <span data-ttu-id="a32d6-187">パート</span><span class="sxs-lookup"><span data-stu-id="a32d6-187">Part</span></span> | <span data-ttu-id="a32d6-188">説明</span><span class="sxs-lookup"><span data-stu-id="a32d6-188">Description</span></span> |
|---|---|
| <span data-ttu-id="a32d6-189">マイナスから 0 の数量</span><span class="sxs-lookup"><span data-stu-id="a32d6-189">Quantity from negative to zero</span></span> | <span data-ttu-id="a32d6-190">在庫では、品目の現在の移動平均原価ではなく、手持在庫残高をマイナスからゼロまで増やす入庫数量のトランザクション原価ではなく、品目の現在の移動平均原価が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-190">Inventory uses the current moving average cost of the item rather than the transaction cost for that portion of the receipt quantity that increases the on-hand balance from negative to zero.</span></span> <span data-ttu-id="a32d6-191">取引コストと現在の移動平均原価との間に差異がある場合は、**移動平均の価格差** に転記されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-191">The difference between the transaction cost and the current moving average cost is posted to **Price difference for moving average**.</span></span> |
| <span data-ttu-id="a32d6-192">ゼロから正の数量</span><span class="sxs-lookup"><span data-stu-id="a32d6-192">Quantity from zero to positive</span></span> | <span data-ttu-id="a32d6-193">在庫では、入庫数量のその部分に対してトランザクション原価が使用され、手持在庫の残高がゼロから正に増加します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-193">Inventory uses the transaction cost for that portion of the receipt quantity that increases the on-hand balance from zero to positive.</span></span>                                                  |

## <a name="inventory-value-report"></a><span data-ttu-id="a32d6-194">在庫金額レポート</span><span class="sxs-lookup"><span data-stu-id="a32d6-194">Inventory value report</span></span>

<span data-ttu-id="a32d6-195">この移動平均の例では、製品の現在の移動平均の計算をサポートするために、在庫金額のレポートが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-195">In this moving average example, the inventory value report is printed to support the current moving average calculation for a product.</span></span> <span data-ttu-id="a32d6-196">[在庫金額] レポートは、トランザクションを古い順に印刷して、原価とともに、製品の移動平均原価計算をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-196">The Inventory value report can print the transactions in chronological order, together with the cost to support the moving average cost calculation of a product.</span></span> <span data-ttu-id="a32d6-197">レポートは、製品の移動平均原価を表示します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-197">The report displays the moving average cost for the product.</span></span> <span data-ttu-id="a32d6-198">**在庫金額のレポート** ダイアログ ボックスで、日付範囲を使用すると、**トランザクション時間** や **転記日付** でレポートを並び替えることができます。</span><span class="sxs-lookup"><span data-stu-id="a32d6-198">In the **Inventory value reports** dialog box, a date interval allows you to select the **Transaction time** or the **Posting date** to sort the report by.</span></span> <span data-ttu-id="a32d6-199">**転記日付** オプションは、従来から使用されているレポートの印刷方法です。</span><span class="sxs-lookup"><span data-stu-id="a32d6-199">The **Posting date** option is how the report is traditionally printed.</span></span> <span data-ttu-id="a32d6-200">**トランザクションが時刻** オプションは、トランザクションが報告され、製品の移動平均原価が更新される実際の日付です。</span><span class="sxs-lookup"><span data-stu-id="a32d6-200">The **Transaction time** option is the actual date that the transaction is reported and the moving average cost for the product is updated.</span></span> <span data-ttu-id="a32d6-201">移動平均原価計算を経時的に表示する場合は、**トランザクション時刻で並べ替え** オプションを使用して、[在庫金額レポート] を印刷します。</span><span class="sxs-lookup"><span data-stu-id="a32d6-201">You can print the Inventory value report by using the **Transaction time sorting** option if you want to see the moving average cost calculation over time.</span></span> <span data-ttu-id="a32d6-202">次の表は、**トランザクション時刻で並べ替え** オプションを使用してレポートを印刷した製品のトランザクションを表示しています。</span><span class="sxs-lookup"><span data-stu-id="a32d6-202">The following table displays the transactions for the product that the report is printed for when the **Transaction time sorting** option is used.</span></span>

| <span data-ttu-id="a32d6-203">トランザクションの時刻</span><span class="sxs-lookup"><span data-stu-id="a32d6-203">Transaction time</span></span> | <span data-ttu-id="a32d6-204">日</span><span class="sxs-lookup"><span data-stu-id="a32d6-204">Date</span></span>         | <span data-ttu-id="a32d6-205">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="a32d6-205">Transaction type</span></span>           | <span data-ttu-id="a32d6-206">梱包明細から</span><span class="sxs-lookup"><span data-stu-id="a32d6-206">Quantity</span></span> | <span data-ttu-id="a32d6-207">金額</span><span class="sxs-lookup"><span data-stu-id="a32d6-207">Amount</span></span> | <span data-ttu-id="a32d6-208">平均単位原価</span><span class="sxs-lookup"><span data-stu-id="a32d6-208">Average unit cost</span></span> |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | <span data-ttu-id="a32d6-209">10 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-209">October 1</span></span>    | <span data-ttu-id="a32d6-210">期首残高</span><span class="sxs-lookup"><span data-stu-id="a32d6-210">Beginning balance</span></span>          | <span data-ttu-id="a32d6-211">0</span><span class="sxs-lookup"><span data-stu-id="a32d6-211">0</span></span>        | <span data-ttu-id="a32d6-212">0.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-212">0.00</span></span>   | <span data-ttu-id="a32d6-213">0.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-213">0.00</span></span>              |
| <span data-ttu-id="a32d6-214">10 月 8 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-214">October 8</span></span>        | <span data-ttu-id="a32d6-215">9 月 28 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-215">September 28</span></span> | <span data-ttu-id="a32d6-216">さかのぼった日付の入庫</span><span class="sxs-lookup"><span data-stu-id="a32d6-216">Backdated receipt</span></span>          | <span data-ttu-id="a32d6-217">1</span><span class="sxs-lookup"><span data-stu-id="a32d6-217">1</span></span>        | <span data-ttu-id="a32d6-218">16.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-218">16.00</span></span>  | <span data-ttu-id="a32d6-219">16.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-219">16.00</span></span>             |
| <span data-ttu-id="a32d6-220">10 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-220">October 3</span></span>        | <span data-ttu-id="a32d6-221">10 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-221">October 3</span></span>    | <span data-ttu-id="a32d6-222">購買入庫</span><span class="sxs-lookup"><span data-stu-id="a32d6-222">Purchase receipt</span></span>           | <span data-ttu-id="a32d6-223">2</span><span class="sxs-lookup"><span data-stu-id="a32d6-223">2</span></span>        | <span data-ttu-id="a32d6-224">20.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-224">20.00</span></span>  | <span data-ttu-id="a32d6-225">12.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-225">12.00</span></span>             |
| <span data-ttu-id="a32d6-226">10 月 5 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-226">October 5</span></span>        | <span data-ttu-id="a32d6-227">10 月 5 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-227">October 5</span></span>    | <span data-ttu-id="a32d6-228">販売注文</span><span class="sxs-lookup"><span data-stu-id="a32d6-228">Sales order</span></span>                | <span data-ttu-id="a32d6-229">-1</span><span class="sxs-lookup"><span data-stu-id="a32d6-229">-1</span></span>       | <span data-ttu-id="a32d6-230">-10.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-230">-10.00</span></span> | <span data-ttu-id="a32d6-231">13.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-231">13.00</span></span>             |
| <span data-ttu-id="a32d6-232">10 月 7 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-232">October 7</span></span>        | <span data-ttu-id="a32d6-233">10 月 7 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-233">October 7</span></span>    | <span data-ttu-id="a32d6-234">仕入請求書</span><span class="sxs-lookup"><span data-stu-id="a32d6-234">Purchase invoice</span></span>           |          | <span data-ttu-id="a32d6-235">2.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-235">2.00</span></span>   | <span data-ttu-id="a32d6-236">14.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-236">14.00</span></span>             |
| <span data-ttu-id="a32d6-237">10 月 8 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-237">October 8</span></span>        | <span data-ttu-id="a32d6-238">10 月 8 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-238">October 8</span></span>    | <span data-ttu-id="a32d6-239">移動平均の再評価</span><span class="sxs-lookup"><span data-stu-id="a32d6-239">Moving average revaluation</span></span> |          | <span data-ttu-id="a32d6-240">4.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-240">4.00</span></span>   | <span data-ttu-id="a32d6-241">16.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-241">16.00</span></span>             |
|                  | <span data-ttu-id="a32d6-242">10 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a32d6-242">October 31</span></span>   | <span data-ttu-id="a32d6-243">小計</span><span class="sxs-lookup"><span data-stu-id="a32d6-243">Total</span></span>                      | <span data-ttu-id="a32d6-244">2</span><span class="sxs-lookup"><span data-stu-id="a32d6-244">2</span></span>        | <span data-ttu-id="a32d6-245">32.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-245">32.00</span></span>  | <span data-ttu-id="a32d6-246">16.00</span><span class="sxs-lookup"><span data-stu-id="a32d6-246">16.00</span></span>             |

> [!NOTE]
> <span data-ttu-id="a32d6-247">**トランザクション時間で並べ替え** オプション使用して、一般会計と在庫を一致させることはできません。</span><span class="sxs-lookup"><span data-stu-id="a32d6-247">You cannot reconcile the general ledger with inventory by using the **Transaction time sorting** option.</span></span> <span data-ttu-id="a32d6-248">レポートは、**転記日付** オプションを使用して印刷する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a32d6-248">The report must be printed by using the **Posting date** option.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]