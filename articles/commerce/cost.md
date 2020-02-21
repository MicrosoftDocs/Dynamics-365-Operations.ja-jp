---
title: 配分済み注文の管理 (DOM) の原価コンフィギュレーション
description: このトピックでは、Dynamics 365 Commerce の配分済み注文の管理 (DOM) 機能の原価コンフィギュレーションについて説明します。
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004231"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="2cf49-103">配分済み注文の管理 (DOM) の原価コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2cf49-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2cf49-104">組織は、注文のフルフィルメントに最適な場所を決定するために、複数の原価コンポーネントを考慮します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="2cf49-105">これらの原価コンポーネントには、出荷コスト、取扱コスト、梱包コストなどがあります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="2cf49-106">これらの原価の組み合わせを計算して、フルフィルメント場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="2cf49-107">Dynamics 365 Commerce の配分済み注文の管理 (DOM) の最初のイテレーションで、注文をフルフィルメント場所に割り当てることが最適化されている場合、このイテレーションでは距離のみが考慮されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="2cf49-108">距離は原価に関連付けることができますが、原価と同じではありません。</span><span class="sxs-lookup"><span data-stu-id="2cf49-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="2cf49-109">たとえば、翌日配送方式では、同じ距離に対して、3 日間配送または 7 日間配送の場合より費用が多くかかります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="2cf49-110">原価コンフィギュレーション機能を使用すると、小売業者は、注文明細行のフルフィルメントに最適な場所を決定するために計算および考慮する追加の原価コンポーネントを定義および構成することができます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="2cf49-111">原価コンポーネントが構成されると、DOM ソルバーはこれらの原価定義のみを使用して、注文のフルフィルメントに最適な場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="2cf49-112">DOM ソルバーは距離コンポーネントをコストと見なしません。</span><span class="sxs-lookup"><span data-stu-id="2cf49-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="2cf49-113">ただし、原価コンポーネントが構成されていない場合、DOM ソルバーは距離コンポーネントをコストとして使用し、注文のフルフィルメントに最適な場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="2cf49-114">原価コンポーネントの設定</span><span class="sxs-lookup"><span data-stu-id="2cf49-114">Set up cost components</span></span>

<span data-ttu-id="2cf49-115">システムでは、**出荷** と **その他** の 2 つの主要な原価コンポーネント タイプを定義できます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="2cf49-116">両方の原価コンポーネント タイプは、次の表に示すように、複数の計算基準をサポートします。</span><span class="sxs-lookup"><span data-stu-id="2cf49-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2cf49-117">原価コンポーネント タイプ</span><span class="sxs-lookup"><span data-stu-id="2cf49-117">Cost component type</span></span></th>
<th><span data-ttu-id="2cf49-118">計算基準</span><span class="sxs-lookup"><span data-stu-id="2cf49-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2cf49-119">出荷</span><span class="sxs-lookup"><span data-stu-id="2cf49-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="2cf49-120">簡易</span><span class="sxs-lookup"><span data-stu-id="2cf49-120">Simple</span></span></li>
<li><span data-ttu-id="2cf49-121">階層化</span><span class="sxs-lookup"><span data-stu-id="2cf49-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="2cf49-122">その他</span><span class="sxs-lookup"><span data-stu-id="2cf49-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="2cf49-123">販売注文</span><span class="sxs-lookup"><span data-stu-id="2cf49-123">Sales order</span></span></li>
<li><span data-ttu-id="2cf49-124">販売明細行</span><span class="sxs-lookup"><span data-stu-id="2cf49-124">Sales line</span></span></li>
<li><span data-ttu-id="2cf49-125">保管場所</span><span class="sxs-lookup"><span data-stu-id="2cf49-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="2cf49-126">出荷原価コンポーネント タイプ</span><span class="sxs-lookup"><span data-stu-id="2cf49-126">Shipping cost component type</span></span>

<span data-ttu-id="2cf49-127">このセクションでは、**出荷** 原価コンポーネント タイプと出荷コストの計算基準の各組み合わせを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="2cf49-128">また、DOM ソルバーで各組み合わせがどのように使用されるかについても説明します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="2cf49-129">原価コンポーネント タイプ = 出荷と計算基準 = 簡易</span><span class="sxs-lookup"><span data-stu-id="2cf49-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="2cf49-130">**出荷** 原価コンポーネント タイプと計算基準 **簡易** の組み合わせを使用する場合、荷渡方法の出荷コストは均一料金または距離に基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="2cf49-131">この組み合わせに対して、次のフィールドを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="2cf49-132">**原価係数** – 原価係数の固有識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="2cf49-133">**説明** – 原価係数の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="2cf49-134">**開始日** および **終了日** – これらのフィールドを使用して、特定の日付範囲の原価係数を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="2cf49-135">これらのフィールドを空白のままにすると、原価係数は無期限に有効になります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="2cf49-136">**有効** – 原価係数が有効かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="2cf49-137">DOM は、フルフィルメント プロファイルに関連付けられている有効な原価係数のみを考慮します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="2cf49-138">**会社** – 原価係数をコンフィギュレーションする対象の法人を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="2cf49-139">計算基準のすべての明細行は、同じ法人に対して設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="2cf49-140">**荷渡方法** – 原価をコンフィギュレーションする対象の荷渡方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="2cf49-141">**計算タイプ** – 特定の荷渡方法に対して原価を計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="2cf49-142">次の 2 つの計算タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="2cf49-143">**固定** – 荷渡方法に均一料金が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="2cf49-144">この計算タイプを選択した場合は、**原価** フィールドによって均一料金が定義されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="2cf49-145">**距離単位ごと** – 荷渡方法に対するコストは、**原価** フィールドで指定された原価価値に配送先住所と保管場所の間の距離を乗じて計算されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="2cf49-146">**原価** – 荷渡方法の原価を計算するために、**計算タイプ** フィールドと組み合わせて使用される原価価値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="2cf49-147">原価コンポーネント タイプ = 出荷と計算基準 = 階層化</span><span class="sxs-lookup"><span data-stu-id="2cf49-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="2cf49-148">**出荷** 原価コンポーネント タイプと計算基準 **階層化** の組み合わせを使用する場合、荷渡方法の出荷費用は均一料金または距離に基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="2cf49-149">ただし、この組み合わせでは、距離は階層化された距離の範囲に基づきます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="2cf49-150">この組み合わせに対して、次のフィールドを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="2cf49-151">**原価係数** – 原価係数の固有識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="2cf49-152">**説明** – 原価係数の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="2cf49-153">**既定の原価** – 配送先住所と保管場所の間の距離が荷渡方法の階層化された距離の範囲に含まれない場合、荷渡方法に使用される原価を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="2cf49-154">**開始日** および **終了日** – これらのフィールドを使用して、特定の日付範囲の原価係数を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="2cf49-155">これらのフィールドを空白のままにすると、原価係数は無期限に有効になります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="2cf49-156">**有効** – 原価係数が有効かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="2cf49-157">DOM は、フルフィルメント プロファイルに関連付けられている有効な原価係数のみを考慮します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="2cf49-158">**会社** – 原価係数をコンフィギュレーションする対象の法人を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="2cf49-159">計算基準のすべての明細行は、同じ法人に対して設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="2cf49-160">**荷渡方法** – 原価をコンフィギュレーションする対象の荷渡方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="2cf49-161">**距離タイプ** – 階層化された距離定義が空路の距離であるか、陸路の距離であるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="2cf49-162">**距離単位** – 階層化された距離を測定する単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="2cf49-163">**開始距離** – 階層化された距離の開始範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="2cf49-164">**終了距離** – 階層化された距離の終了範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="2cf49-165">**計算タイプ** – 特定の荷渡方法と階層化された距離に対してコストを計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="2cf49-166">次の 2 つの計算タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="2cf49-167">**固定** – 荷渡方法に均一料金が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="2cf49-168">この計算タイプを選択した場合は、**原価** フィールドによって均一料金が定義されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="2cf49-169">**距離単位ごと** – 荷渡方法と階層化された距離に対するコストは、**原価** フィールドで指定された原価価値に配送先住所と保管場所の間の距離を乗じて計算されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="2cf49-170">**原価** – 荷渡方法の原価を計算するために、**計算タイプ** フィールドと組み合わせて使用される原価価値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="2cf49-171">階層化された距離を定義すると、欠落または重複する距離がないことが検証されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="2cf49-172">荷渡方法に使用される距離タイプは、階層化されたすべての距離にわたって同一である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="2cf49-173">その他原価コンポーネント タイプ</span><span class="sxs-lookup"><span data-stu-id="2cf49-173">Other cost component type</span></span>

<span data-ttu-id="2cf49-174">このセクションでは、**その他** 原価コンポーネント タイプと出荷以外のコストのその他の原価タイプの各組み合わせを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="2cf49-175">また、DOM ソルバーで各組み合わせがどのように使用されるかについても説明します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="2cf49-176">原価コンポーネント タイプ = その他とその他の原価タイプ = 販売注文</span><span class="sxs-lookup"><span data-stu-id="2cf49-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="2cf49-177">**その他** 原価コンポーネント タイプとその他の原価タイプ **販売注文** の組み合わせは、販売注文レベルでの出荷以外のコストを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="2cf49-178">この組み合わせに対して、次のフィールドを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="2cf49-179">**原価係数** – 原価係数の固有識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="2cf49-180">**説明** – 原価係数の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="2cf49-181">**開始日** および **終了日** – これらのフィールドを使用して、特定の日付範囲の原価係数を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="2cf49-182">これらのフィールドを空白のままにすると、原価係数は無期限に有効になります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="2cf49-183">**有効** – 原価係数が有効かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="2cf49-184">DOM は、フルフィルメント プロファイルに関連付けられている有効な原価係数のみを考慮します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="2cf49-185">**原価** – 販売注文レベルでの出荷以外のコストの原価価値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="2cf49-186">原価コンポーネント タイプ = その他とその他の原価タイプ = 販売明細行</span><span class="sxs-lookup"><span data-stu-id="2cf49-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="2cf49-187">**その他** 原価コンポーネント タイプとその他の原価タイプ **販売明細行** の組み合わせは、販売注文明細行レベルでの出荷以外のコストを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="2cf49-188">この組み合わせに対して、次のフィールドを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="2cf49-189">**原価係数** – 原価係数の固有識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="2cf49-190">**説明** – 原価係数の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="2cf49-191">**開始日** および **終了日** – これらのフィールドを使用して、特定の日付範囲の原価係数を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="2cf49-192">これらのフィールドを空白のままにすると、原価係数は無期限に有効になります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="2cf49-193">**有効** – 原価係数が有効かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="2cf49-194">DOM は、フルフィルメント プロファイルに関連付けられている有効な原価係数のみを考慮します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="2cf49-195">**原価** – 販売注文明細行レベルでの出荷以外のコストの原価価値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="2cf49-196">原価コンポーネント タイプ = その他とその他の原価タイプ = 保管場所</span><span class="sxs-lookup"><span data-stu-id="2cf49-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="2cf49-197">**その他** 原価コンポーネント タイプとその他の原価タイプ **保管場所** の組み合わせは、保管場所のグループまたは個々の場所に対する出荷以外のコストを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="2cf49-198">この組み合わせに対して、次のフィールドを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="2cf49-199">**原価係数** – 原価係数の固有識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="2cf49-200">**説明** – 原価係数の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="2cf49-201">**開始日** および **終了日** – これらのフィールドを使用して、特定の日付範囲の原価係数を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="2cf49-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="2cf49-202">これらのフィールドを空白のままにすると、原価係数は無期限に有効になります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="2cf49-203">**有効** – 原価係数が有効かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="2cf49-204">DOM は、フルフィルメント プロファイルに関連付けられている有効な原価係数のみを考慮します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="2cf49-205">**フルフィルメント グループ** – 出荷以外のコストを定義する対象の保管場所のグループを指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="2cf49-206">**フルフィルメント場所** – 出荷以外のコストを定義する対象の保管場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2cf49-207">場所に基づく計算基準では、同じ明細行で、フルフィルメント グループとフルフィルメント場所を指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="2cf49-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="2cf49-208">**原価** – フルフィルメント グループ レベルまたはフルフィルメント場所レベルで、出荷以外のコストの原価価値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2cf49-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2cf49-209">DOM でこれらの原価を実行時に考慮するには、関連するフルフィルメント プロファイルに原価係数を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cf49-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
