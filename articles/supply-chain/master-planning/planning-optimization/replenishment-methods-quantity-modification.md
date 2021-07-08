---
title: 補充方法と数量変更
description: このトピックでは、計画最適化における補充方法に関する情報を提供します。 また、製品の複数の注文数量が結果にどのように影響するかについても説明します。
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261699"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="95f20-104">補充方法と数量変更</span><span class="sxs-lookup"><span data-stu-id="95f20-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95f20-105">このトピックでは、計画最適化における補充方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="95f20-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="95f20-106">また、製品の複数の注文数量が結果にどのように影響するかについても説明します。</span><span class="sxs-lookup"><span data-stu-id="95f20-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="95f20-107">補充方法は、カバレッジ方法およびロットサイズ変更方法とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="95f20-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="95f20-108">補充コード</span><span class="sxs-lookup"><span data-stu-id="95f20-108">Coverage codes</span></span>

<span data-ttu-id="95f20-109">さまざまな補充方法を使用するように計画最適化をコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="95f20-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="95f20-110">補充方法は、製品の要件を計算するためにシステムが使用する技術です。</span><span class="sxs-lookup"><span data-stu-id="95f20-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="95f20-111">補充方法は、補充グループまたは製品のいずれかに対して設定できる補充コードによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="95f20-112">計画最適化で使用できる補充コードは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="95f20-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="95f20-113">**期間** – 補充方法では、ある期間のすべての需要を 1 つの製品の注文にまとめます。</span><span class="sxs-lookup"><span data-stu-id="95f20-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="95f20-114">この注文はその期間の初日に対して計画され、その数量が設定された期間における正味必要量となります。</span><span class="sxs-lookup"><span data-stu-id="95f20-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="95f20-115">この期間は、製品の最初の需要から始まり、定義された期間の長さを対象としています。</span><span class="sxs-lookup"><span data-stu-id="95f20-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="95f20-116">次の期間は、製品の次の要件から開始されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="95f20-117">*期間* 補充コードは多くの場合、予測できない在庫振出、季節影響を受ける製品、または高コスト製品に使用されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="95f20-118">次の図は、例を示します。</span><span class="sxs-lookup"><span data-stu-id="95f20-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="95f20-119">![期間補充コードの使用例](./media/coverage-code-period.png "期間補充コードの使用例")</span><span class="sxs-lookup"><span data-stu-id="95f20-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="95f20-120">**要求** – 補充方法では、製品の要求ごとに計画購買、移動、または製造オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="95f20-121">この方法は、断続的な需要がある高価な製品に使用されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="95f20-122">*要求* 補充コードは多くの場合、コンフィギュレーション可能な製品や受注生産シナリオで使用されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="95f20-123">次の図は、例を示します。</span><span class="sxs-lookup"><span data-stu-id="95f20-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="95f20-124">![要求補充コードの使用例](./media/coverage-code-requirement.png "要求補充コードの使用例")</span><span class="sxs-lookup"><span data-stu-id="95f20-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="95f20-125">**最小/最大**</span><span class="sxs-lookup"><span data-stu-id="95f20-125">**Min./Max.**</span></span> <span data-ttu-id="95f20-126">– 補充方法は、在庫レベルに基づきます。</span><span class="sxs-lookup"><span data-stu-id="95f20-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="95f20-127">予測手持在庫レベルが特定のしきい値を下回った場合に、在庫の補充を特定のレベルまで定義します。</span><span class="sxs-lookup"><span data-stu-id="95f20-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="95f20-128">補充数量は、最大レベルと予測手持在庫レベルの差額になります。</span><span class="sxs-lookup"><span data-stu-id="95f20-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="95f20-129">*最小/最大*</span><span class="sxs-lookup"><span data-stu-id="95f20-129">The *Min./Max.*</span></span> <span data-ttu-id="95f20-130">補充コードは多くの場合、予測可能な在庫振出、高ランナー、またはより安価な製品に使用されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="95f20-131">次の図は、例を示します。</span><span class="sxs-lookup"><span data-stu-id="95f20-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="95f20-132">![最小/最大補充コードの使用例](./media/coverage-code-min-max.png "最小/最大補充コードの使用例")</span><span class="sxs-lookup"><span data-stu-id="95f20-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="95f20-133">**手動** – 補充方法では、製品に対する購入、移動、または製造オーダーは提案されません。</span><span class="sxs-lookup"><span data-stu-id="95f20-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="95f20-134">代わりに、製品のプランナーが製品の補充に必要な注文の作成を担当します。</span><span class="sxs-lookup"><span data-stu-id="95f20-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="95f20-135">*手動* 補充コードは、多くの場合、システム生成された計画オーダーが不要な製品に使用されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="95f20-136">既定の注文設定からの注文数量の影響</span><span class="sxs-lookup"><span data-stu-id="95f20-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="95f20-137">リリース済製品の **既定の注文設定** ページで、**発注書**、**在庫**、および **販売注文** クイック タブで、次の各数量設定を指定できます。</span><span class="sxs-lookup"><span data-stu-id="95f20-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="95f20-138">(**在庫** クイック タブは、移動オーダーと製造オーダーの両方に使用されます。)</span><span class="sxs-lookup"><span data-stu-id="95f20-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="95f20-139">**複数** – 計画オーダーは、この数量の倍数です。</span><span class="sxs-lookup"><span data-stu-id="95f20-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="95f20-140">たとえば、**倍数** フィールドが *5* に設定されている場合、注文は 5、10、15、20 などの数量になります。</span><span class="sxs-lookup"><span data-stu-id="95f20-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="95f20-141">**最小注文数量** – 計画オーダーは、指定された値より少なくなることはありません。</span><span class="sxs-lookup"><span data-stu-id="95f20-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="95f20-142">たとえば、**最小注文数量** フィールドが *10* に設定されている場合、需要を満たすには 4 つだけ必要な場合でも、数量 10 の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="95f20-143">**最大注文数量** – 計画オーダーは、指定された値を超えることはありません。</span><span class="sxs-lookup"><span data-stu-id="95f20-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="95f20-144">需要が **最大注文数量** 値を超える場合は、それをカバーするため複数の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="95f20-145">たとえば、**最大注文数量** フィールドが *100* に設定され、需要が 450 の場合、数量 100 の計画オーダーが 4 つ、および数量 50 の計画オーダーが 1 つ作成されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="95f20-146">最小/最大を使用する補充例</span><span class="sxs-lookup"><span data-stu-id="95f20-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="95f20-147">補充コード</span><span class="sxs-lookup"><span data-stu-id="95f20-147">coverage code</span></span>

<span data-ttu-id="95f20-148">**既定の注文設定** ページの **複数** フィールドで値を指定しない場合、および *最小/最大*</span><span class="sxs-lookup"><span data-stu-id="95f20-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="95f20-149">補充方法を使用している場合、計画の最適化では、予測手持在庫レベルが特定のしきい値を下回った場合に、在庫を特定のレベルまで補充します。</span><span class="sxs-lookup"><span data-stu-id="95f20-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="95f20-150">製品に対して複数の数量を定義する場合、*最小/最大*</span><span class="sxs-lookup"><span data-stu-id="95f20-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="95f20-151">補充方法ではその動作が変更され、**複数** 値が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="95f20-152">つまり、計画の最適化では、予測手持在庫レベルが定義された最小レベルよりも小さい場合でも、定義された最大レベルまで在庫を補充します。</span><span class="sxs-lookup"><span data-stu-id="95f20-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="95f20-153">ただし、補充数量は **複数** 値の倍数である必要があります。</span><span class="sxs-lookup"><span data-stu-id="95f20-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="95f20-154">補充数量 (最大レベルと予測手持在庫レベルの差) が定義された複数の数量の倍数ではない場合、計画の最適化では、予測手持在庫レベルと共に最大レベルを下回る最初の可能な値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="95f20-155">合計が最小レベルよりも小さい場合は、計画の最適化では、予測手持在庫レベルと共に最大レベルを上回る最初の可能な値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="95f20-156">次のサブセクションでは、製品の複数の注文数量が *最小/最大*</span><span class="sxs-lookup"><span data-stu-id="95f20-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="95f20-157">補充方法の結果にどのように影響するかを示す例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="95f20-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="95f20-158">例 1</span><span class="sxs-lookup"><span data-stu-id="95f20-158">Example 1</span></span>

<span data-ttu-id="95f20-159">製品のコンフィギュレーションは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="95f20-159">A product has the following configuration:</span></span>

- <span data-ttu-id="95f20-160">**補充コード:** *最小/最大*</span><span class="sxs-lookup"><span data-stu-id="95f20-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="95f20-161">**最小:** *15*</span><span class="sxs-lookup"><span data-stu-id="95f20-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="95f20-162">**最大:** *22*</span><span class="sxs-lookup"><span data-stu-id="95f20-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="95f20-163">**倍数:** *0*</span><span class="sxs-lookup"><span data-stu-id="95f20-163">**Multiple:** *0*</span></span>

<span data-ttu-id="95f20-164">製品の手持在庫が 10 個で、その他の需要または供給はありません。</span><span class="sxs-lookup"><span data-stu-id="95f20-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="95f20-165">マスター プランを実行すると、在庫を最大数量まで補充するために 12 個の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="95f20-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="95f20-166">例 2</span><span class="sxs-lookup"><span data-stu-id="95f20-166">Example 2</span></span>

<span data-ttu-id="95f20-167">製品のコンフィギュレーションは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="95f20-167">A product has the following configuration:</span></span>

- <span data-ttu-id="95f20-168">**補充コード:** *最小/最大*</span><span class="sxs-lookup"><span data-stu-id="95f20-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="95f20-169">**最小:** *15*</span><span class="sxs-lookup"><span data-stu-id="95f20-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="95f20-170">**最大:** *22*</span><span class="sxs-lookup"><span data-stu-id="95f20-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="95f20-171">**倍数:** *5*</span><span class="sxs-lookup"><span data-stu-id="95f20-171">**Multiple:** *5*</span></span>

<span data-ttu-id="95f20-172">製品の手持在庫が 10 個で、その他の需要または供給はありません。</span><span class="sxs-lookup"><span data-stu-id="95f20-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="95f20-173">マスター プランを実行すると、10 個の計画オーダーが作成されます (15 個の補充と 10 個の手持在庫が最大数量を超えるためです)。</span><span class="sxs-lookup"><span data-stu-id="95f20-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="95f20-174">例 3</span><span class="sxs-lookup"><span data-stu-id="95f20-174">Example 3</span></span>

<span data-ttu-id="95f20-175">製品のコンフィギュレーションは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="95f20-175">A product has the following configuration:</span></span>

- <span data-ttu-id="95f20-176">**補充コード:** *最小/最大*</span><span class="sxs-lookup"><span data-stu-id="95f20-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="95f20-177">**最小:** *21*</span><span class="sxs-lookup"><span data-stu-id="95f20-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="95f20-178">**最大:** *24*</span><span class="sxs-lookup"><span data-stu-id="95f20-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="95f20-179">**倍数:** *5*</span><span class="sxs-lookup"><span data-stu-id="95f20-179">**Multiple:** *5*</span></span>

<span data-ttu-id="95f20-180">製品の手持在庫が 10 個で、その他の需要または供給はありません。</span><span class="sxs-lookup"><span data-stu-id="95f20-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="95f20-181">マスター プランを実行すると、15 個の計画オーダーが作成されます (10 個の補充と 10 個の手持在庫が最小数量を下回るためです)。</span><span class="sxs-lookup"><span data-stu-id="95f20-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
