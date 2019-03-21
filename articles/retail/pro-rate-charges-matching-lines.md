---
title: ヘッダーの諸費用を一致する販売明細行に比例配分する
description: このトピックでは、高度な自動請求機能を使用して、自動請求を小売チャネル注文に計算および適用するための追加の機能について説明します。
author: hhaines
manager: annbe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d225f1ed3922f72c33e77fc3c488db8d1f2bc8d5
ms.sourcegitcommit: 0bd0215d0735ed47b1b8af93a80bcdbf7ca2cc49
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/08/2019
ms.locfileid: "790224"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a><span data-ttu-id="ba148-103">ヘッダーの諸費用を一致する販売明細行に比例配分する</span><span class="sxs-lookup"><span data-stu-id="ba148-103">Prorate header charges to matching sales lines</span></span>

[!include [banner](includes/preview-banner.md)]

[!include [banner](includes/banner.md)]

<span data-ttu-id="ba148-104">このトピックでは、ヘッダー レベルの自動請求をグループ化して、小売販売明細行に比例配分する機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="ba148-104">This topic describes the functionality for grouping header-level auto-charges and prorating them to retail sales lines.</span></span> <span data-ttu-id="ba148-105">この機能は、Microsoft Dynamics 365 for Retail バージョン 10.0.1 の販売時点管理 (POS) で作成されたトランザクションと、Microsoft Dynamics 365 for Retail バージョン 10.0.2 のコール センターで作成された販売で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba148-105">This functionality is available for transactions that are created at the point of sale (POS) in Microsoft Dynamics 365 for Retail version 10.0.1 and sales that are created in a call center in Microsoft Dynamics 365 for Retail version 10.0.2.</span></span>

<span data-ttu-id="ba148-106">この機能は、[高度な自動請求](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) 機能が**小売パラメーター**ページのオプションを使用して有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba148-106">This functionality is available only if the [advanced auto-charges](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) feature is turned on by using the option on the **Retail parameters** page.</span></span> <span data-ttu-id="ba148-107">さらに、自動請求の拡張された計算方法は、小売チャネル (POS、コール センター、および Dynamics E コマース プラットフォーム) で作成した小売販売注文にのみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="ba148-107">Additionally, the enhanced calculation method for auto-charges can be applied only to retail sales orders that are created through retail channels (the POS, a call center, and the Dynamics e-Commerce platform).</span></span>

<span data-ttu-id="ba148-108">この新しい機能により、ヘッダー レベルの自動請求が計算され小売販売トランザクションに適用されるという点で組織はさらに柔軟になります。</span><span class="sxs-lookup"><span data-stu-id="ba148-108">This new functionality gives organizations more flexibility in the way that header-level auto-charges are calculated and applied to retail sales transactions.</span></span>

<span data-ttu-id="ba148-109">バージョン 10.0.1 よりも前の Microsoft Dynamics 365 for Retail のバージョンでは、特定の荷渡方法リレーションを持つヘッダーレベルの自動請求は、販売注文ヘッダーで定義されている荷渡方法と一致する場合にのみ計算されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-109">In versions of Microsoft Dynamics 365 for Retail that are earlier than version 10.0.1, header-level auto-charges that have a specific mode of delivery relation are calculated only when there is a match with the mode of delivery that is defined on the sales order header.</span></span>

<span data-ttu-id="ba148-110">たとえば、ヘッダー レベルの自動請求は荷渡方法 **99** および荷渡方法 **11** に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-110">For example, header-level auto-charges are defined for mode of delivery **99** and mode of delivery **11**.</span></span> <span data-ttu-id="ba148-111">販売注文が作成されると、荷渡方法 **99** は、注文ヘッダーで定義されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-111">A sales order is created, and mode of delivery **99** is defined on the order header.</span></span> <span data-ttu-id="ba148-112">ただし、一部の販売注文明細行は荷渡方法 **11** を使用して出荷されるように設定されています。</span><span class="sxs-lookup"><span data-stu-id="ba148-112">However, some of the sale lines are set up so that they're shipped by using mode of delivery **11**.</span></span> <span data-ttu-id="ba148-113">この場合、荷渡方法 **99** に関連付けられているヘッダー レベルの請求金額のみが考慮され、販売注文に適用されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-113">In this case, only the header-level charges that are linked to mode of delivery **99** are considered and applied to the sales order.</span></span>

<span data-ttu-id="ba148-114">Dynamics 365 for Retail のヘッダー レベルの請求金額には、注文金額に基づいた[階層型費用のコンフィギュレーション](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) を定義することのできる追加の機能があります。</span><span class="sxs-lookup"><span data-stu-id="ba148-114">In Dynamics 365 for Retail, the header-level charges have an additional feature that lets you define a [tiered charge configuration](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) that is based on the order value.</span></span> <span data-ttu-id="ba148-115">たとえば、注文金額が $50.00 から $200.00 である場合、組織は $5.00 の配送料を請求する場合があります。</span><span class="sxs-lookup"><span data-stu-id="ba148-115">For example, if the order value is between $50.00 and $200.00, an organization might want to charge a freight charge of $5.00.</span></span> <span data-ttu-id="ba148-116">しかし、注文金額が $200.01 から $500.00 である場合は、配送料を $4.00 にするかもしれません。</span><span class="sxs-lookup"><span data-stu-id="ba148-116">However, if the order value is between $200.01 and $500.00, the freight charge might be $4.00.</span></span>

<span data-ttu-id="ba148-117">一部の組織は、ヘッダー レベルの請求金額で提供される階層型費用の計算の利点を求めています。</span><span class="sxs-lookup"><span data-stu-id="ba148-117">Some organizations want the benefits of the tiered charge calculation that is provided with header-level charges.</span></span> <span data-ttu-id="ba148-118">ただし、さまざまな荷渡方法が関係するシナリオの場合、計算される請求金額が各販売明細行で定義されている荷渡方法との一致に基づいていることを確認する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="ba148-118">However, in scenarios that involve mixed modes of delivery, they also want to make sure that the charges that are calculated are based on a match with the mode of delivery that is defined on each sales line.</span></span>

<span data-ttu-id="ba148-119">これで、請求金額の計算時に注文のすべての荷渡方法が考慮されるようにヘッダー レベルの自動請求をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="ba148-119">You can now configure header-level auto-charges so that all modes of delivery on the order are considered when charges are calculated.</span></span> <span data-ttu-id="ba148-120">この機能には、ヘッダー レベルの請求金額を計算するためのより複雑な計算ロジックが必要です。</span><span class="sxs-lookup"><span data-stu-id="ba148-120">This functionality requires a more complex calculation logic to calculate the header-level charges.</span></span> <span data-ttu-id="ba148-121">ロジックは、同じ荷渡方法を使用して出荷されるすべての品目をグループ化し、ヘッダー レベルの自動請求を計算するときにそのグループを品目の計算グループとして扱います。</span><span class="sxs-lookup"><span data-stu-id="ba148-121">The logic groups together all the items that are shipped by using the same mode of delivery, and it treats that group as the calculation group for the items when it calculates the header-level auto-charges.</span></span> <span data-ttu-id="ba148-122">同じ荷渡方法がある品目の場合は、自動請求は品目の合計販売値に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-122">For items that have the same mode of delivery, auto-charges are calculated based on the combined sales value of the items.</span></span> <span data-ttu-id="ba148-123">この方法で、適切な自動請求層が決定されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-123">In this way, the appropriate auto-charge tier is determined.</span></span>

<span data-ttu-id="ba148-124">同じ荷渡方法を使用して出荷された販売明細行に対して適切なヘッダー レベルの請求金額が取得された後、計算された請求金額は販売明細行レベルまで比例配分されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-124">After the appropriate header-level charges are obtained for the sales lines that are shipped by using the same mode of delivery, the calculated charges are prorated down to the sales line level.</span></span> <span data-ttu-id="ba148-125">これらの請求は明細行レベルであり、ヘッダー レベルでは維持されないため、品目とそれに対して計算された請求金額の値との間に、より具体的なリンクが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-125">Because these charges are at the line level and not kept at the header level, a more specific link is made between the item and the charge value that calculated for it.</span></span> <span data-ttu-id="ba148-126">この動作は、一部の商品のみが返品されたときに、組織が全額ではなく一部の料金のみを返金することを希望する部分返品シナリオで役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ba148-126">This behavior can be useful in partial return scenarios, where an organization wants to refund only part of the charge instead of the whole charge when only some items are returned.</span></span>

## <a name="scenarios"></a><span data-ttu-id="ba148-127">シナリオ</span><span class="sxs-lookup"><span data-stu-id="ba148-127">Scenarios</span></span>

<span data-ttu-id="ba148-128">次の 2 つのサンプルシナリオでは、新しい機能が使用されている場合と使用されていない場合の両方で、これらの請求金額がどのように計算されるかについての概要を説明しています。</span><span class="sxs-lookup"><span data-stu-id="ba148-128">The following two sample scenarios outline how these charges are calculated both when the new functionality is used and when it isn't used.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="ba148-129">シナリオ 1</span><span class="sxs-lookup"><span data-stu-id="ba148-129">Scenario 1</span></span>

<span data-ttu-id="ba148-130">このシナリオは、自動請求の設定で**一致する販売明細行への比例配分**オプションが**いいえ**に設定されているときの動作についての概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="ba148-130">This scenario outlines the behavior when the **Pro-rate to matching sales lines** option is set to **No** in the auto-charge setup.</span></span> <span data-ttu-id="ba148-131">(この動作は、バージョン 10.0.1 より前の小売バージョンでのヘッダー レベルの請求金額の動作に相当します)。</span><span class="sxs-lookup"><span data-stu-id="ba148-131">(The behavior is equivalent to the behavior of header-level charges in Retail versions that are earlier than version 10.0.1.)</span></span>

<span data-ttu-id="ba148-132">このシナリオでは、組織には、荷渡方法リレーション **99** および荷渡方法リレーション **11** の定義されているヘッダー レベルの請求金額があります。</span><span class="sxs-lookup"><span data-stu-id="ba148-132">In this scenario, the organization has defined header-level charges for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="ba148-133">荷渡方法 **21** には自動請求はコンフィギュレーションされません。</span><span class="sxs-lookup"><span data-stu-id="ba148-133">No auto-charges are configured for mode of delivery **21**.</span></span>

![一致する明細行の比例配分がオフになっているときの荷渡方法 99 の自動請求](media/99_disabled.png)

![一致する明細行の比例配分がオフになっているときの荷渡方法 11 の自動請求](media/11_disabled.png)

<span data-ttu-id="ba148-136">コール センターで販売注文が作成されると、荷渡方法は **99** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-136">A sales order is created in the call center, and the mode of delivery is set to **99**.</span></span> <span data-ttu-id="ba148-137">この注文には、5 つの品目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ba148-137">This order contains five items.</span></span> <span data-ttu-id="ba148-138">次のテーブルが示すように、2 つの注文明細行が荷渡方法 **99** を使用するようにコンフィギュレーションされ、2 つの明細行が荷渡方法 **11** を使用するようにコンフィギュレーションされ、1 つの明細行が荷渡方法 **21** を使用するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="ba148-138">Two order lines have been configured to use mode of delivery **99**, two lines have been configured to use mode of delivery **11**, and one line has been configured to use mode of delivery **21**, as shown in the following table.</span></span>

| <span data-ttu-id="ba148-139">項目</span><span class="sxs-lookup"><span data-stu-id="ba148-139">Item</span></span>  | <span data-ttu-id="ba148-140">明細行の数量</span><span class="sxs-lookup"><span data-stu-id="ba148-140">Line quantity</span></span> | <span data-ttu-id="ba148-141">荷渡方法</span><span class="sxs-lookup"><span data-stu-id="ba148-141">Delivery mode</span></span> | <span data-ttu-id="ba148-142">単位あたりの価格</span><span class="sxs-lookup"><span data-stu-id="ba148-142">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="ba148-143">81331</span><span class="sxs-lookup"><span data-stu-id="ba148-143">81331</span></span> | <span data-ttu-id="ba148-144">1</span><span class="sxs-lookup"><span data-stu-id="ba148-144">1</span></span>             | <span data-ttu-id="ba148-145">11</span><span class="sxs-lookup"><span data-stu-id="ba148-145">11</span></span>            | <span data-ttu-id="ba148-146">10 ドル</span><span class="sxs-lookup"><span data-stu-id="ba148-146">$10</span></span>            |
| <span data-ttu-id="ba148-147">81332</span><span class="sxs-lookup"><span data-stu-id="ba148-147">81332</span></span> | <span data-ttu-id="ba148-148">1</span><span class="sxs-lookup"><span data-stu-id="ba148-148">1</span></span>             | <span data-ttu-id="ba148-149">99</span><span class="sxs-lookup"><span data-stu-id="ba148-149">99</span></span>            | <span data-ttu-id="ba148-150">$50</span><span class="sxs-lookup"><span data-stu-id="ba148-150">$50</span></span>            |
| <span data-ttu-id="ba148-151">81333</span><span class="sxs-lookup"><span data-stu-id="ba148-151">81333</span></span> | <span data-ttu-id="ba148-152">2</span><span class="sxs-lookup"><span data-stu-id="ba148-152">2</span></span>             | <span data-ttu-id="ba148-153">11</span><span class="sxs-lookup"><span data-stu-id="ba148-153">11</span></span>            | <span data-ttu-id="ba148-154">$30</span><span class="sxs-lookup"><span data-stu-id="ba148-154">$30</span></span>            |
| <span data-ttu-id="ba148-155">81334</span><span class="sxs-lookup"><span data-stu-id="ba148-155">81334</span></span> | <span data-ttu-id="ba148-156">3</span><span class="sxs-lookup"><span data-stu-id="ba148-156">3</span></span>             | <span data-ttu-id="ba148-157">99</span><span class="sxs-lookup"><span data-stu-id="ba148-157">99</span></span>            | <span data-ttu-id="ba148-158">10 ドル</span><span class="sxs-lookup"><span data-stu-id="ba148-158">$10</span></span>            |
| <span data-ttu-id="ba148-159">81334</span><span class="sxs-lookup"><span data-stu-id="ba148-159">81334</span></span> | <span data-ttu-id="ba148-160">3</span><span class="sxs-lookup"><span data-stu-id="ba148-160">3</span></span>             | <span data-ttu-id="ba148-161">21</span><span class="sxs-lookup"><span data-stu-id="ba148-161">21</span></span>            | <span data-ttu-id="ba148-162">$5</span><span class="sxs-lookup"><span data-stu-id="ba148-162">$5</span></span>             |

<span data-ttu-id="ba148-163">このシナリオでは、注文全体が荷渡方法 **99** の自動請求に対して評価されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-163">In this scenario, the whole order is evaluated against the auto-charge table for mode of delivery **99**.</span></span> <span data-ttu-id="ba148-164">すべての販売明細行の完全な合計は、自動請求のコンフィギュレーションの一致する階層を決定するために使用され、この請求金額は注文ヘッダー レベルで適用されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-164">The full total of all sales lines is used to determine a matching tier in the auto-charge configuration, and this charge is applied at the order header level.</span></span> <span data-ttu-id="ba148-165">この例では、注文の合計は $165.00 で、$15.00 の配送料は注文ヘッダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-165">In this example, the order total is $165.00, and the $15.00 freight charge is applied to the order header.</span></span> <span data-ttu-id="ba148-166">荷渡方法 **11** にコンフィギュレーションされている自動請求は、参照または適用されることはありません。</span><span class="sxs-lookup"><span data-stu-id="ba148-166">Auto-charges that are configured for mode of delivery **11** are never referenced or applied.</span></span>

<span data-ttu-id="ba148-167">このシナリオでは、顧客が注文の一部の品目を返品し、[請求金額コードが払戻されるようにコンフィギュレーションされている](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2) 場合、一部の品目のみが返品された場合でも、ヘッダー レベルの合計請求金額が体系的に払戻に適用されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-167">In this scenario, if a customer returns some of the items on the order, and if the [charge code has been configured so that it will be refunded](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), the total header-level charge is systematically applied to the refund, even if only some of the items are returned.</span></span>

### <a name="scenario-2"></a><span data-ttu-id="ba148-168">シナリオ 2</span><span class="sxs-lookup"><span data-stu-id="ba148-168">Scenario 2</span></span>

<span data-ttu-id="ba148-169">このシナリオでは、ヘッダー レベルの請求金額は荷渡方法リレーション **99** および荷渡方法リレーション **11** に定義されています。</span><span class="sxs-lookup"><span data-stu-id="ba148-169">In this scenario, header-level charges are defined for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="ba148-170">ただし、これらの自動請求テーブルでは**一致する販売明細行への比例配分**オプションが**はい**に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ba148-170">However, the **Pro-rate to matching sales lines** option is set to **Yes** for these auto-charge tables.</span></span>

![一致する明細行の比例配分がオンになっているときの荷渡方法 99 の自動請求](media/99_enabled.png)

![一致する明細行の比例配分がオンになっているときの荷渡方法 11 の自動請求](media/11_enabled.png)

<span data-ttu-id="ba148-173">このシナリオでは、5 つの明細行を含む同じ販売注文を使用します。</span><span class="sxs-lookup"><span data-stu-id="ba148-173">This scenario uses the same sales order that contains five lines.</span></span> <span data-ttu-id="ba148-174">注文ヘッダーの荷渡方法は **99** に設定されていますが、販売注文の各品目の荷渡方法は次のテーブルに示すようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="ba148-174">The mode of delivery on the order header is set to **99**, but the mode of delivery for each item on the sales order is configured as shown in the following table.</span></span>

| <span data-ttu-id="ba148-175">項目</span><span class="sxs-lookup"><span data-stu-id="ba148-175">Item</span></span>  | <span data-ttu-id="ba148-176">明細行の数量</span><span class="sxs-lookup"><span data-stu-id="ba148-176">Line quantity</span></span> | <span data-ttu-id="ba148-177">荷渡方法</span><span class="sxs-lookup"><span data-stu-id="ba148-177">Delivery mode</span></span> | <span data-ttu-id="ba148-178">単位あたりの価格</span><span class="sxs-lookup"><span data-stu-id="ba148-178">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="ba148-179">81331</span><span class="sxs-lookup"><span data-stu-id="ba148-179">81331</span></span> | <span data-ttu-id="ba148-180">1</span><span class="sxs-lookup"><span data-stu-id="ba148-180">1</span></span>             | <span data-ttu-id="ba148-181">11</span><span class="sxs-lookup"><span data-stu-id="ba148-181">11</span></span>            | <span data-ttu-id="ba148-182">10 ドル</span><span class="sxs-lookup"><span data-stu-id="ba148-182">$10</span></span>            |
| <span data-ttu-id="ba148-183">81332</span><span class="sxs-lookup"><span data-stu-id="ba148-183">81332</span></span> | <span data-ttu-id="ba148-184">1</span><span class="sxs-lookup"><span data-stu-id="ba148-184">1</span></span>             | <span data-ttu-id="ba148-185">99</span><span class="sxs-lookup"><span data-stu-id="ba148-185">99</span></span>            | <span data-ttu-id="ba148-186">$50</span><span class="sxs-lookup"><span data-stu-id="ba148-186">$50</span></span>            |
| <span data-ttu-id="ba148-187">81333</span><span class="sxs-lookup"><span data-stu-id="ba148-187">81333</span></span> | <span data-ttu-id="ba148-188">2</span><span class="sxs-lookup"><span data-stu-id="ba148-188">2</span></span>             | <span data-ttu-id="ba148-189">11</span><span class="sxs-lookup"><span data-stu-id="ba148-189">11</span></span>            | <span data-ttu-id="ba148-190">$30</span><span class="sxs-lookup"><span data-stu-id="ba148-190">$30</span></span>            |
| <span data-ttu-id="ba148-191">81334</span><span class="sxs-lookup"><span data-stu-id="ba148-191">81334</span></span> | <span data-ttu-id="ba148-192">3</span><span class="sxs-lookup"><span data-stu-id="ba148-192">3</span></span>             | <span data-ttu-id="ba148-193">99</span><span class="sxs-lookup"><span data-stu-id="ba148-193">99</span></span>            | <span data-ttu-id="ba148-194">10 ドル</span><span class="sxs-lookup"><span data-stu-id="ba148-194">$10</span></span>            |
| <span data-ttu-id="ba148-195">81334</span><span class="sxs-lookup"><span data-stu-id="ba148-195">81334</span></span> | <span data-ttu-id="ba148-196">3</span><span class="sxs-lookup"><span data-stu-id="ba148-196">3</span></span>             | <span data-ttu-id="ba148-197">21</span><span class="sxs-lookup"><span data-stu-id="ba148-197">21</span></span>            | <span data-ttu-id="ba148-198">$5</span><span class="sxs-lookup"><span data-stu-id="ba148-198">$5</span></span>             |

<span data-ttu-id="ba148-199">自動請求のコンフィギュレーションは一致する販売明細行に比例配分するように設定されているため、システムは次の計算手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ba148-199">Because the auto-charge configuration is set to prorate to matching sales lines, the system performs the following calculation steps.</span></span>

1. <span data-ttu-id="ba148-200">同じ荷渡方法があるすべての品目はグループ化され、システムはグループ内の品目の製品の合計値を計算します。</span><span class="sxs-lookup"><span data-stu-id="ba148-200">All items that have the same mode of delivery are grouped together, and the system calculates the total product value of the items in the group.</span></span>

    <span data-ttu-id="ba148-201">**荷渡方法 11**</span><span class="sxs-lookup"><span data-stu-id="ba148-201">**Delivery mode 11**</span></span>

    - <span data-ttu-id="ba148-202">品目 81331、数量 1 = $10</span><span class="sxs-lookup"><span data-stu-id="ba148-202">Item 81331, quantity 1 = $10</span></span>
    - <span data-ttu-id="ba148-203">品目 81333、数量 2 = 正味 $60 (単位あたり $30)</span><span class="sxs-lookup"><span data-stu-id="ba148-203">Item 81333, quantity 2 = $60 net ($30 per unit)</span></span>
    - <span data-ttu-id="ba148-204">**荷渡方法 11 の製品の合計値 = $70**</span><span class="sxs-lookup"><span data-stu-id="ba148-204">**Total product value for delivery mode 11 = $70**</span></span>

    <span data-ttu-id="ba148-205">**荷渡方法 99**</span><span class="sxs-lookup"><span data-stu-id="ba148-205">**Delivery mode 99**</span></span>

    - <span data-ttu-id="ba148-206">品目 81332、数量 1 = $50</span><span class="sxs-lookup"><span data-stu-id="ba148-206">Item 81332, quantity 1 = $50</span></span>
    - <span data-ttu-id="ba148-207">品目 81334、数量 3 = 正味 $30</span><span class="sxs-lookup"><span data-stu-id="ba148-207">Item 81334, quantity 3 = $30 net</span></span>
    - <span data-ttu-id="ba148-208">**荷渡方法 99 の製品の合計値 = $80**</span><span class="sxs-lookup"><span data-stu-id="ba148-208">**Total product value for delivery mode 99 = $80**</span></span>

    <span data-ttu-id="ba148-209">**荷渡方法 21**</span><span class="sxs-lookup"><span data-stu-id="ba148-209">**Delivery mode 21**</span></span>

    - <span data-ttu-id="ba148-210">品目 81334、数量 3 = 正味 $15</span><span class="sxs-lookup"><span data-stu-id="ba148-210">Item 81334, quantity 3 = $15 net</span></span>
    - <span data-ttu-id="ba148-211">**荷渡方法 21 の製品の合計値 = $15**</span><span class="sxs-lookup"><span data-stu-id="ba148-211">**Total product value for delivery mode 21 = $15**</span></span>

2. <span data-ttu-id="ba148-212">システムは、品目のグループごとの顧客および荷渡方法に一致するヘッダー レベルの自動請求のコンフィギュレーションを検索します。</span><span class="sxs-lookup"><span data-stu-id="ba148-212">The system looks for the configuration for header-level auto-charges that matches the customer and mode of delivery settings for each group of items.</span></span> <span data-ttu-id="ba148-213">コンフィギュレーションが見つかった場合、システムは、荷渡方法グループの品目の製品の合計値に基づいて、適用されるべき請求金額を見つけるために階層型のコンフィギュレーション内を検索します。</span><span class="sxs-lookup"><span data-stu-id="ba148-213">If the configuration is found, the system looks in the tiered configuration to find the charge that should be applied, based on the total product value of items in the mode of delivery group.</span></span>

    <span data-ttu-id="ba148-214">**荷渡方法 11**</span><span class="sxs-lookup"><span data-stu-id="ba148-214">**Delivery mode 11**</span></span>

    - <span data-ttu-id="ba148-215">小売製品の合計値 = $70</span><span class="sxs-lookup"><span data-stu-id="ba148-215">Total retail product value = $70</span></span>
    - <span data-ttu-id="ba148-216">**請求金額の値 = $7**</span><span class="sxs-lookup"><span data-stu-id="ba148-216">**Charge value = $7**</span></span>

    <span data-ttu-id="ba148-217">**荷渡方法 99**</span><span class="sxs-lookup"><span data-stu-id="ba148-217">**Delivery mode 99**</span></span>

    - <span data-ttu-id="ba148-218">小売製品の合計値 = $80</span><span class="sxs-lookup"><span data-stu-id="ba148-218">Total retail product value = $80</span></span>
    - <span data-ttu-id="ba148-219">**請求金額の値 = $15**</span><span class="sxs-lookup"><span data-stu-id="ba148-219">**Charge value = $15**</span></span>

    <span data-ttu-id="ba148-220">**荷渡方法 21**</span><span class="sxs-lookup"><span data-stu-id="ba148-220">**Delivery mode 21**</span></span>

    - <span data-ttu-id="ba148-221">小売製品の合計値 = $15</span><span class="sxs-lookup"><span data-stu-id="ba148-221">Total retail product value = $15</span></span>
    - <span data-ttu-id="ba148-222">**請求金額の値 = $0** (この顧客および荷渡方法の組み合わせには、自動請求はコンフィギュレーションされていません)。</span><span class="sxs-lookup"><span data-stu-id="ba148-222">**Charge value = $0** (No auto-charges have been configured for this combination of a customer and a mode of delivery.)</span></span>

    ![荷渡方法 11 の請求金額は強調表示された層に分類される](media/step2mode11.png)

    ![荷渡方法 99 の請求金額は強調表示された層に分類される](media/step2mode99.png)

3. <span data-ttu-id="ba148-225">システムは、グループの製品の合計値に対する明細行の比例値を考慮した比例配分ロジックに基づいて、各明細行に適用されるべき請求金額の値を計算します。</span><span class="sxs-lookup"><span data-stu-id="ba148-225">The system calculates the charge value that should be applied to each line, based on proration logic that considers the proportional value of the line in relation to the group's total product value.</span></span>

    <span data-ttu-id="ba148-226">**荷渡方法 11**</span><span class="sxs-lookup"><span data-stu-id="ba148-226">**Delivery mode 11**</span></span>

    - <span data-ttu-id="ba148-227">請求金額の値 = $7</span><span class="sxs-lookup"><span data-stu-id="ba148-227">Charge value = $7</span></span>
    - <span data-ttu-id="ba148-228">グループ製品の値 = $70</span><span class="sxs-lookup"><span data-stu-id="ba148-228">Group product value = $70</span></span>
    - <span data-ttu-id="ba148-229">明細行 1 の 値e = $10 (= グループ値の 14.2857 パーセント)</span><span class="sxs-lookup"><span data-stu-id="ba148-229">Line 1 value = $10 (= 14.2857 percent of the group value)</span></span>
    - <span data-ttu-id="ba148-230">明細行 3 の 値 = $60 (= グループ値の 85.7143 パーセント)</span><span class="sxs-lookup"><span data-stu-id="ba148-230">Line 3 value = $60 (= 85.7143 percent of the group value)</span></span>
    - <span data-ttu-id="ba148-231">**明細行 1 の明細行手数料 = $1**</span><span class="sxs-lookup"><span data-stu-id="ba148-231">**Line charge for line 1 = $1**</span></span>
    - <span data-ttu-id="ba148-232">**明細行 3 の明細行手数料 = $6**</span><span class="sxs-lookup"><span data-stu-id="ba148-232">**Line charge for line 3 = $6**</span></span>

    <span data-ttu-id="ba148-233">**荷渡方法 99**</span><span class="sxs-lookup"><span data-stu-id="ba148-233">**Delivery mode 99**</span></span>

    - <span data-ttu-id="ba148-234">請求金額の値 = $15</span><span class="sxs-lookup"><span data-stu-id="ba148-234">Charge value = $15</span></span>
    - <span data-ttu-id="ba148-235">グループ製品の値 = $80</span><span class="sxs-lookup"><span data-stu-id="ba148-235">Group product value = $80</span></span>
    - <span data-ttu-id="ba148-236">明細行 2 の 値 = $50 (= グループ値の 62.5 パーセント)</span><span class="sxs-lookup"><span data-stu-id="ba148-236">Line 2 value = $50 (= 62.5 percent of the group value)</span></span>
    - <span data-ttu-id="ba148-237">明細行 4 の 値 = $30 (= グループ値の 37.5 パーセント)</span><span class="sxs-lookup"><span data-stu-id="ba148-237">Line 4 value = $30 (= 37.5 percent of the group value)</span></span>
    - <span data-ttu-id="ba148-238">**明細行 2 の明細行手数料 = $9.38**</span><span class="sxs-lookup"><span data-stu-id="ba148-238">**Line charge for line 2 = $9.38**</span></span>
    - <span data-ttu-id="ba148-239">**明細行 4 の明細行手数料 = $5.62**</span><span class="sxs-lookup"><span data-stu-id="ba148-239">**Line charge for line 4 = $5.62**</span></span>

    <span data-ttu-id="ba148-240">**荷渡方法 21**</span><span class="sxs-lookup"><span data-stu-id="ba148-240">**Delivery mode 21**</span></span>

    - <span data-ttu-id="ba148-241">請求金額の値 = $0</span><span class="sxs-lookup"><span data-stu-id="ba148-241">Charge value = $0</span></span>
    - <span data-ttu-id="ba148-242">グループ製品の値 = $15</span><span class="sxs-lookup"><span data-stu-id="ba148-242">Group product value = $15</span></span>
    - <span data-ttu-id="ba148-243">明細行 5 の 値 = $15 (= グループ値の 100 パーセント)</span><span class="sxs-lookup"><span data-stu-id="ba148-243">Line 5 value = $15 (= 100 percent of the group value)</span></span>
    - <span data-ttu-id="ba148-244">**明細行 5 の明細行手数料 = $0**</span><span class="sxs-lookup"><span data-stu-id="ba148-244">**Line charge for line 5 = $0**</span></span>

<span data-ttu-id="ba148-245">したがって、この例では、品目 81334 には $5.62 の配送料が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="ba148-245">Therefore, for this example, item 81334 will be assigned a freight charge of $5.62.</span></span> <span data-ttu-id="ba148-246">販売明細行の**諸費用の管理**ページでこれらの請求金額を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ba148-246">You can view these charges on the **Maintain charges** page for the sales line.</span></span> <span data-ttu-id="ba148-247">次の図は、品目 81334 に対するこのページの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="ba148-247">The following illustration shows what this page looks like for item 81334.</span></span>

![品目 81334 の販売明細行の比例配分された請求金額](media/proratedlinecharge.png)

<span data-ttu-id="ba148-249">この計算メソッドが部分返品シナリオで使用される場合、請求金額コードが払戻可能な場合、その明細行に割り当てられた請求金額の一部のみが商品の返品時に返金されます。</span><span class="sxs-lookup"><span data-stu-id="ba148-249">When this method of calculation is used in a partial return scenario, if the charge code is refundable, only the part of the charge that is allocated to that line will be refunded when the item is returned.</span></span>
