---
title: "移動平均原価価格"
description: "在庫原価計算プロセスでは、品目の品目モデル グループで選択した在庫評価方法に基づいて、払出トランザクションを受入トランザクションへと決済します。 ただし、在庫決算を実行する前に、システムは、払出トランザクションの転記時に通常使用される移動平均原価価格を計算します。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: aeb23f78d9bec93cf92214470e9ace3cd88b92c3
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="running-average-cost-price"></a><span data-ttu-id="47fc4-104">移動平均原価価格</span><span class="sxs-lookup"><span data-stu-id="47fc4-104">Running average cost price</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="47fc4-105">在庫原価計算プロセスでは、品目の品目モデル グループで選択した在庫評価方法に基づいて、払出トランザクションを受入トランザクションへと決済します。</span><span class="sxs-lookup"><span data-stu-id="47fc4-105">The inventory close process settles issue transactions to receipt transactions, based on the inventory valuation method that is selected in the item’s item model group.</span></span> <span data-ttu-id="47fc4-106">ただし、在庫決算を実行する前に、システムは、払出トランザクションの転記時に通常使用される移動平均原価価格を計算します。</span><span class="sxs-lookup"><span data-stu-id="47fc4-106">However, before inventory close is run, the system calculates a running average cost price that is typically used when issue transactions are posted.</span></span>

<span data-ttu-id="47fc4-107">システムは、次の式を使用して、品目に対するこの移動平均原価価格を見積もります。</span><span class="sxs-lookup"><span data-stu-id="47fc4-107">The system estimates this running average cost price for an item by using the following formula:</span></span> 

<span data-ttu-id="47fc4-108">見積価格 = (現物金額 + 財務金額) ÷ (現物数量 + 財務数量)</span><span class="sxs-lookup"><span data-stu-id="47fc4-108">Estimated price = (Physical amount + Financial amount) ÷ (Physical quantity + Financial quantity)</span></span>

## <a name="using-the-running-average-cost-price"></a><span data-ttu-id="47fc4-109">移動平均原価価格の使用</span><span class="sxs-lookup"><span data-stu-id="47fc4-109">Using the running average cost price</span></span>
<span data-ttu-id="47fc4-110">次の表では、システムが在庫トランザクションの転記に、移動平均原価価格を使用する場合と、品目マスタ レコードで定義されている原価価格を代わりに使用する場合を示します。</span><span class="sxs-lookup"><span data-stu-id="47fc4-110">The following table shows when the system posts inventory transactions by using the running average cost price, and when it uses the cost price that is defined on the item master record instead.</span></span>

| <span data-ttu-id="47fc4-111">条件</span><span class="sxs-lookup"><span data-stu-id="47fc4-111">Condition</span></span>                                               | <span data-ttu-id="47fc4-112">システムは見積もられた移動平均原価価格を使用</span><span class="sxs-lookup"><span data-stu-id="47fc4-112">The system uses the estimated running average cost price</span></span> | <span data-ttu-id="47fc4-113">システムは品目マスターで定義されている原価価格を使用</span><span class="sxs-lookup"><span data-stu-id="47fc4-113">The system uses the cost price that is defined on the item master</span></span> |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="47fc4-114">分子\* と分母\*\* が両方とも正です。</span><span class="sxs-lookup"><span data-stu-id="47fc4-114">Both the numerator\* and denominator\*\* are positive.</span></span>  | <span data-ttu-id="47fc4-115">有</span><span class="sxs-lookup"><span data-stu-id="47fc4-115">Yes</span></span>                                                      | <span data-ttu-id="47fc4-116">無</span><span class="sxs-lookup"><span data-stu-id="47fc4-116">No</span></span>                                                                |
| <span data-ttu-id="47fc4-117">分子\* と分母\*\* のどちらか一方または両方が負です。</span><span class="sxs-lookup"><span data-stu-id="47fc4-117">The numerator\*, denominator\*\*, or both are negative.</span></span> | <span data-ttu-id="47fc4-118">無</span><span class="sxs-lookup"><span data-stu-id="47fc4-118">No</span></span>                                                       | <span data-ttu-id="47fc4-119">有</span><span class="sxs-lookup"><span data-stu-id="47fc4-119">Yes</span></span>                                                               |
| <span data-ttu-id="47fc4-120">分母\*\* が 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="47fc4-120">The denominator\*\* is 0 (zero).</span></span>                        | <span data-ttu-id="47fc4-121">無</span><span class="sxs-lookup"><span data-stu-id="47fc4-121">No</span></span>                                                       | <span data-ttu-id="47fc4-122">有</span><span class="sxs-lookup"><span data-stu-id="47fc4-122">Yes</span></span>                                                               |

<span data-ttu-id="47fc4-123">\* 分子 = (現物金額 + 財務金額) \*\* 分母 = (現物数量 + 財務数量)</span><span class="sxs-lookup"><span data-stu-id="47fc4-123">\* Numerator = (Physical amount + Financial amount) \*\* Denominator = (Physical quantity + Financial quantity)</span></span> 

<span data-ttu-id="47fc4-124">**注記:** 品目に対して **現物価格を含める** オプションが選択されていない場合、システムは現物金額と現物数量の両方に 0 (ゼロ) を使用します。</span><span class="sxs-lookup"><span data-stu-id="47fc4-124">**Note:** If the **Include physical value** option isn't selected for an item, the system uses 0 (zero) for both the physical amount and the physical quantity.</span></span> <span data-ttu-id="47fc4-125">このオプションの詳細については、「[現物価格を含める](include-physical-value.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47fc4-125">For information about this option, see [Include physical value](include-physical-value.md).</span></span>

## <a name="avoiding-pricing-amplification"></a><span data-ttu-id="47fc4-126">価格決定増幅の回避</span><span class="sxs-lookup"><span data-stu-id="47fc4-126">Avoiding pricing amplification</span></span>
<span data-ttu-id="47fc4-127">あまりないことですが、システムが、価格の基になる入庫が十分な数になる前に複数の払出の価格を決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="47fc4-127">On rare occasions, the system prices several issues before it has enough receipts to base the price on.</span></span> <span data-ttu-id="47fc4-128">このシナリオは、移動平均原価価格の見積を過剰に高くします。</span><span class="sxs-lookup"><span data-stu-id="47fc4-128">This scenario can cause estimates of the running average cost price to be overly inflated.</span></span> <span data-ttu-id="47fc4-129">ただし、この価格決定増幅を回避する方法、または問題が発生した場合にその影響を減らす方法があります。</span><span class="sxs-lookup"><span data-stu-id="47fc4-129">However, there are steps that you can take to avoid pricing amplification, or to reduce its impact when it does occur.</span></span> <span data-ttu-id="47fc4-130">**シナリオ** 次のトランザクションは、[**現物価格を含める**] オプションを選択した品目に対して発生します。</span><span class="sxs-lookup"><span data-stu-id="47fc4-130">**Scenario** The following transactions occur for an item that you've selected the **Include physical value** option for:</span></span>

1.  <span data-ttu-id="47fc4-131">USD 100.00 で 100 個を財務で入庫します。</span><span class="sxs-lookup"><span data-stu-id="47fc4-131">You financially receive a quantity of 100 at USD 100.00.</span></span>
2.  <span data-ttu-id="47fc4-132">200 個を財務で払い出します。</span><span class="sxs-lookup"><span data-stu-id="47fc4-132">You financially issue a quantity of 200.</span></span>
3.  <span data-ttu-id="47fc4-133">USD 202.00 で 101 個を現物で入庫します。</span><span class="sxs-lookup"><span data-stu-id="47fc4-133">You physically receive a quantity of 101 at USD 202.00.</span></span>

<span data-ttu-id="47fc4-134">品目に対して見積もられた移動平均原価価格を調べる際には、原価価格を USD 1.51 と予想します。</span><span class="sxs-lookup"><span data-stu-id="47fc4-134">When you examine the estimated running average cost price for the item, you expect a cost price of USD 1.51.</span></span> <span data-ttu-id="47fc4-135">代わりに、次の式に基づいて USD 102.00 と見積もられた移動平均を見つけます。見積価格 = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 この価格決定増幅が発生するのは、ステップ 2 で 200 個の品目を財務的に払い出すときに、システムが、対応する入庫がある前に品目の価格を 100 に決定する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="47fc4-135">Instead, you find an estimated running average of USD 102.00, which is based on the following formula: Estimated price = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 This pricing amplification occurs because, when 200 items are issued financially in step 2, the system must price 100 of the items before it has any corresponding receipts.</span></span> <span data-ttu-id="47fc4-136">この条件によってマイナス在庫が発生します。</span><span class="sxs-lookup"><span data-stu-id="47fc4-136">This situation causes negative inventory.</span></span> <span data-ttu-id="47fc4-137">システムは単価を USD 1.00 と見積もり、これは予想した値です。</span><span class="sxs-lookup"><span data-stu-id="47fc4-137">The system then estimates a unit price of USD 1.00, as we might expect.</span></span> <span data-ttu-id="47fc4-138">しかし、対応する 100 個の入荷があり、その単価はそれぞれ USD 2.00 です。</span><span class="sxs-lookup"><span data-stu-id="47fc4-138">However, when the corresponding 100 receipts arrive, they are at a unit price of USD 2.00 each.</span></span> 

<span data-ttu-id="47fc4-139">**メモ:** 払出の結果として在庫は負になりますが、払出価格の計算時には在庫は正です。</span><span class="sxs-lookup"><span data-stu-id="47fc4-139">**Note:** Although the issues create negative inventory, inventory is positive when the issue price is calculated.</span></span> <span data-ttu-id="47fc4-140">このため、品目マスタの価格ではなく、移動平均原価価格が使用されます。</span><span class="sxs-lookup"><span data-stu-id="47fc4-140">Therefore, the running average cost price is used instead of the price on the item master.</span></span> <span data-ttu-id="47fc4-141">この時点で、システムには USD 100.00 の在庫金額相殺があります。</span><span class="sxs-lookup"><span data-stu-id="47fc4-141">At this point, the system has an inventory value offset of USD 100.00.</span></span> <span data-ttu-id="47fc4-142">それぞれの単位相殺は USD 1.00 である 100 個に対する相殺が累積しますが、最終的に在庫は 1 個になります。</span><span class="sxs-lookup"><span data-stu-id="47fc4-142">Although that offset was built up over 100 pieces, where there was a unit offset of USD 1.00 each, we now have only one piece in inventory.</span></span> <span data-ttu-id="47fc4-143">そのため、その相殺の USD 100.00 が、このただ 1 個に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="47fc4-143">Therefore, the offset of USD 100.00 is allocated to this one piece.</span></span> <span data-ttu-id="47fc4-144">結果は、過剰に高い見積もり原価価格になります。</span><span class="sxs-lookup"><span data-stu-id="47fc4-144">The result is the overly inflated estimated cost price.</span></span> 

<span data-ttu-id="47fc4-145">**メモ:** 比較のため、シナリオのステップ 2 と 3 が逆になったとすると、200 個の品目が単価 USD 1.51 で払い出され、1 個が単価 USD 1.51 で残ることを確認します。</span><span class="sxs-lookup"><span data-stu-id="47fc4-145">**Note:** For comparison, notice that if steps 2 and 3 are reversed in the scenario, 200 items will be issued at a unit price of USD 1.51, and one piece will remain at a unit price of USD 1.51.</span></span> <span data-ttu-id="47fc4-146">この価格決定増幅シナリオは、負の在庫が関係するときに発生する可能性があるので、次の場合には防ぐのが困難です。</span><span class="sxs-lookup"><span data-stu-id="47fc4-146">Because this pricing amplification scenario can occur when negative inventory is involved, it's difficult to avoid in the following cases:</span></span>

-   <span data-ttu-id="47fc4-147">手持の金額と数量で払出価格を見積もる必要があります。</span><span class="sxs-lookup"><span data-stu-id="47fc4-147">You must estimate issue prices on the on-hand value and quantity.</span></span>
-   <span data-ttu-id="47fc4-148">手持の金額と数量を払出と入庫で調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47fc4-148">You must adjust the on-hand value and quantity on issues and receipts.</span></span>
-   <span data-ttu-id="47fc4-149">ビジネス モデルで、手持より多い個数の発送または価格決定が許可されています。</span><span class="sxs-lookup"><span data-stu-id="47fc4-149">Your business model allows you to send out, or price, more pieces than you have.</span></span>
-   <span data-ttu-id="47fc4-150">送信されたすべての入庫金額と数量を受け入れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="47fc4-150">You must accept any receipt value and quantity that are submitted to you.</span></span>

<span data-ttu-id="47fc4-151">ただし、ビジネス モデルが以下の方法を許している場合は、価格決定増幅シナリオの可能性がある負の数量を避けるのに有効です。</span><span class="sxs-lookup"><span data-stu-id="47fc4-151">However, if your business model allows for the following practices, they can help you avoid the negative quantities that make the pricing amplification scenario possible:</span></span>

-   <span data-ttu-id="47fc4-152">品目に [**現物価格を含める**] オプションを選択している場合、[**品目モデル グループ**] ページの [**現物マイナス在庫**] チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="47fc4-152">If you select the **Include physical value** option for an item, clear the **Physical negative inventory** check box on the **Item model groups** page.</span></span>
-   <span data-ttu-id="47fc4-153">品目に [**現物価格を含める**] オプションを選択して*いない*場合、[**品目モデル グループ**] ページの [**財務マイナス在庫**] オプションをオフにします。</span><span class="sxs-lookup"><span data-stu-id="47fc4-153">If you do *not* select the **Include physical value** option for an item, clear the **Financial negative inventory** option on the **Item model groups** page.</span></span>

<span data-ttu-id="47fc4-154">また、現物在庫金額の最大相殺は、現物トランザクションの数および現物価格と財務価格の差によって制限されることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="47fc4-154">Additionally, consider that the maximum offset in your physical inventory value is limited by the number of physical transactions, and the difference between physical and financial prices.</span></span> <span data-ttu-id="47fc4-155">すべての現物トランザクションが最終的に財務的に更新されれば、現物金額が非常に高くなることはありません。</span><span class="sxs-lookup"><span data-stu-id="47fc4-155">Provided that all physical transactions are eventually updated financially, the physical value can't rise to extreme levels.</span></span> <span data-ttu-id="47fc4-156">最後に、累積された相殺がただ 1 つではなく、いくつかの手持に対して分配されると、増幅の影響は大幅に減少することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="47fc4-156">Finally, note that the amplification effect decreases significantly when the accumulated offset is spread out over several on-hand pieces instead of just one.</span></span>




