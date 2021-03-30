---
title: 代替配送先
description: 受注管理者は、代替配送処理ページを使用して、代替注文処理オプションを検出できます。
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 783307ea5cc764f4a04d069dfd7d614a4f63dd2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229258"
---
# <a name="delivery-alternatives"></a><span data-ttu-id="02781-103">代替配送先</span><span class="sxs-lookup"><span data-stu-id="02781-103">Delivery alternatives</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02781-104">受注管理者は、**代替配送処理** ページを使用して、代替注文処理オプションを検出できます。</span><span class="sxs-lookup"><span data-stu-id="02781-104">Sales order takers can use the **Delivery alternatives** page to discover alternative order fulfillment options.</span></span>

<span data-ttu-id="02781-105">**代替配送処理** ページ レイアウトには、すべての代替オプションの詳細な概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="02781-105">The **Delivery alternatives** page layout gives an overview of all alternative options.</span></span> <span data-ttu-id="02781-106">また、受注管理者は既存の会社の情報だけではなく、フルフィルメント案件も確認できます。</span><span class="sxs-lookup"><span data-stu-id="02781-106">It also lets order takers look beyond the current company for fulfillment opportunities.</span></span> <span data-ttu-id="02781-107">会社間の営業案件および外部仕入先の営業案件の両方を表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="02781-107">They can now view both intercompany opportunities and opportunities from external vendors.</span></span> <span data-ttu-id="02781-108">配送日ごとにオプションを並べ替えることで、受注管理者は、代替配送処理におけるインテリジェント リストを表示できます。</span><span class="sxs-lookup"><span data-stu-id="02781-108">By sorting the options by delivery date, sales order takers can view an intelligent list of delivery alternatives.</span></span> <span data-ttu-id="02781-109">さらに、パラメーターでは、提示された出荷を効率的に管理するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="02781-109">In addition, parameters help them better manage the suggested deliveries.</span></span> <span data-ttu-id="02781-110">配送時間は、出荷日に影響する可能性があるため、受注管理者は、配送業者が提供しているさまざまな配送選択を参照できます。</span><span class="sxs-lookup"><span data-stu-id="02781-110">Because transport time can affect delivery dates, sales order takers can explore the various transportation choices that carriers offer.</span></span> <span data-ttu-id="02781-111">各提案には詳細な情報が表示されているため、受注管理者は **代替配送処理** ページからの情報に基づいて、決定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="02781-111">Because detailed information is shown for each suggestion, order takers can make informed decisions directly from the **Delivery alternatives** page.</span></span>

## <a name="open-the-delivery-alternatives-page"></a><span data-ttu-id="02781-112">代替配送処理ページを開く</span><span class="sxs-lookup"><span data-stu-id="02781-112">Open the Delivery alternatives page</span></span>

<span data-ttu-id="02781-113">販売注文明細行の **代替配送処理** ページを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="02781-113">You can open the **Delivery alternatives** page from the sales order line.</span></span>

1. <span data-ttu-id="02781-114">**製品と供給 \> 代替配送処理** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="02781-114">Select **Products and supply \> Delivery alternatives**.</span></span>
1. <span data-ttu-id="02781-115">**行の詳細 \> 配送 \> 代替配送処理** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="02781-115">Select **Line details \> Delivery \> Delivery alternatives.**</span></span>

<span data-ttu-id="02781-116">**販売注文の処理と照会** ワークスペースを開いて、**注文とお気に入り \> 遅延注文明細行 \> 代替配送処理** の順に選択して、**代替配送処理** ページを開くこともできます **注:** 両方の条件を満たせる場合にのみ、**代替配送処理** ページを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="02781-116">You can also open the **Delivery alternatives** page by opening the **Sales order processing and inquiry** workspace, and then selecting **Orders and favorites \> Delayed order lines \> Delivery alternatives** **Note:** You can open the **Delivery alternatives** page only if both the following conditions are met:</span></span>

- <span data-ttu-id="02781-117">販売明細行の必須情報すべてが入力されます。</span><span class="sxs-lookup"><span data-stu-id="02781-117">All mandatory sales line information is filled in.</span></span>
- <span data-ttu-id="02781-118">**配送日の管理** フィールドには、**なし** 以外の値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="02781-118">The **Delivery date control** field is set to a value other than **None**.</span></span>

## <a name="delivery-date-control-methods"></a><span data-ttu-id="02781-119">配送日管理方法</span><span class="sxs-lookup"><span data-stu-id="02781-119">Delivery date control methods</span></span>

<span data-ttu-id="02781-120">配送日管理方法により、配送日の設定方法、代替配送処理の計算方法、および表示される情報が指定されます。</span><span class="sxs-lookup"><span data-stu-id="02781-120">The delivery date control method determines how the system establishes delivery dates, how delivery alternatives are calculated, and what information is shown.</span></span> <span data-ttu-id="02781-121">配送日管理ではカレンダーを考慮に入れます。</span><span class="sxs-lookup"><span data-stu-id="02781-121">Note that delivery date control takes calendars into consideration.</span></span> <span data-ttu-id="02781-122">したがって、提案された入庫日は倉庫カレンダー、輸送カレンダー、仕入先カレンダー、および顧客カレンダーに影響される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="02781-122">Therefore, the following calendars can affect the suggested receipt date: Warehouse calendar, Transport calendar, Vendor calendar, and Customer calendar.</span></span> <span data-ttu-id="02781-123">次の表では、配送日管理の各方法が説明されています。</span><span class="sxs-lookup"><span data-stu-id="02781-123">The following table describes each method for delivery date control.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02781-124"><strong>方法</strong></span><span class="sxs-lookup"><span data-stu-id="02781-124"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="02781-125"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="02781-125"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02781-126"><strong>None</strong></span><span class="sxs-lookup"><span data-stu-id="02781-126"><strong>None</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="02781-127">販売明細行の代替配送処理はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="02781-127">Delivery alternatives for sales lines aren't supported.</span></span> <span data-ttu-id="02781-128">このオプションは、配送日管理を無効にします。</span><span class="sxs-lookup"><span data-stu-id="02781-128">This option turns off delivery date control.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02781-129"><strong>販売リード タイム</strong></span><span class="sxs-lookup"><span data-stu-id="02781-129"><strong>Sales lead time</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="02781-130">代替配送処理は、事前に定義された販売リード タイムに基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="02781-130">Delivery alternatives are calculated based on the predefined sales lead time.</span></span> <span data-ttu-id="02781-131">配送日数は、荷渡方法に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="02781-131">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="02781-132">代替配送処理には、手持在庫および供給/需要注文がある倉庫が含まれます。</span><span class="sxs-lookup"><span data-stu-id="02781-132">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02781-133"><strong>ATP</strong></span><span class="sxs-lookup"><span data-stu-id="02781-133"><strong>ATP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="02781-134">納期回答可能在庫 (ATP) ロジックに基づいて代替配送処理が計算されます。</span><span class="sxs-lookup"><span data-stu-id="02781-134">Delivery alternatives are calculated based on available to promise (ATP) logic.</span></span> <span data-ttu-id="02781-135">現在の使用可能性および将来的に予想される使用可能性が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="02781-135">The current availability and expected future availability are considered.</span></span> <span data-ttu-id="02781-136">配送日数は、荷渡方法に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="02781-136">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="02781-137">代替配送処理には、手持在庫および供給/需要注文がある倉庫が含まれます。</span><span class="sxs-lookup"><span data-stu-id="02781-137">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02781-138"><strong>ATP + 払出安全日数</strong></span><span class="sxs-lookup"><span data-stu-id="02781-138"><strong>ATP + Issue margin</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="02781-139">代替配送処理は、ATP メソッドを使用する場合に計算されますが、払出安全日数が計算に含められます。</span><span class="sxs-lookup"><span data-stu-id="02781-139">Delivery alternatives are calculated as for the ATP method, but the issue margin is included in the calculation.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02781-140"><strong>CTP</strong></span><span class="sxs-lookup"><span data-stu-id="02781-140"><strong>CTP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="02781-141">納期回答可能在庫 (CTP) ロジックに基づいて代替配送処理が計算されます。</span><span class="sxs-lookup"><span data-stu-id="02781-141">Delivery alternatives are calculated based on the capable to promise (CTP) logic.</span></span> <span data-ttu-id="02781-142">MRP 展開は、使用可能性を確認するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="02781-142">MRP explosion is used to determine availability.</span></span> <span data-ttu-id="02781-143">少なくとも、CTP は納期を販売リードタイムに相殺することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="02781-143">Note that, at a minimum, CTP offsets delivery dates to the sales lead time.</span></span> <span data-ttu-id="02781-144">配送日数は、荷渡方法に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="02781-144">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="02781-145">代替配送処理には、次の倉庫に対する提案が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02781-145">Delivery alternatives include suggestions for the following warehouses:</span></span>
<ul>
<li><span data-ttu-id="02781-146">現在の倉庫</span><span class="sxs-lookup"><span data-stu-id="02781-146">Current warehouse</span></span></li>
<li><span data-ttu-id="02781-147">既定の倉庫</span><span class="sxs-lookup"><span data-stu-id="02781-147">Default warehouse</span></span></li>
<li><span data-ttu-id="02781-148">使用可能な手持在庫があるすべての倉庫</span><span class="sxs-lookup"><span data-stu-id="02781-148">All warehouses that have available on-hand inventory</span></span></li>
<li><span data-ttu-id="02781-149">供給の注文があるすべての倉庫</span><span class="sxs-lookup"><span data-stu-id="02781-149">All warehouses that have supply orders</span></span></li>
<li><span data-ttu-id="02781-150">有効な部品表 (BOM) バージョンがあるすべての倉庫</span><span class="sxs-lookup"><span data-stu-id="02781-150">All warehouses that have active bill of materials (BOM) versions</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a><span data-ttu-id="02781-151">代替配送処理に関する情報の表示</span><span class="sxs-lookup"><span data-stu-id="02781-151">View information about delivery alternatives</span></span>

<span data-ttu-id="02781-152">このセクションでは **代替配送処理** ページの各クイックタブで使用可能な代替配送処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="02781-152">This section describes the information about delivery alternatives that is available on each FastTab of the **Delivery alternatives** page.</span></span>

### <a name="the-product-fasttab"></a><span data-ttu-id="02781-153">製品クイックタブ</span><span class="sxs-lookup"><span data-stu-id="02781-153">The Product FastTab</span></span>

<span data-ttu-id="02781-154">このクイックタブでは、製品の概要と現在の販売明細行の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="02781-154">This FastTab shows a summary of the product and details of the current sales line.</span></span>

### <a name="the-delivery-alternatives-fasttab"></a><span data-ttu-id="02781-155">代替配送処理クイックタブ</span><span class="sxs-lookup"><span data-stu-id="02781-155">The Delivery alternatives FastTab</span></span>

<span data-ttu-id="02781-156">このクイックタブには、受領日で並べ替えられた代替配送処理が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="02781-156">This FastTab shows a list of delivery alternatives that is sorted by receipt date.</span></span> <span data-ttu-id="02781-157">リストの上では、提案のベースとなるオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="02781-157">Above the list, you can select which options to base the suggestions on.</span></span> <span data-ttu-id="02781-158">配送日数を指定する荷渡方法を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="02781-158">You can also select the mode of delivery, which determines the transport days.</span></span> <span data-ttu-id="02781-159">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="02781-159">The following options are available:</span></span>

- <span data-ttu-id="02781-160">**その他の製品バリアントを含める**: このオプションは、製品バリアントがある製品に対して使用可能です。</span><span class="sxs-lookup"><span data-stu-id="02781-160">**Include other product variants** - This option is available for products that have product variants.</span></span> <span data-ttu-id="02781-161">その製品の他のバリアントの代替配送処理が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02781-161">It will include delivery alternatives for other variants of the product.</span></span> <span data-ttu-id="02781-162">このオプションは、CTP には使用できません。</span><span class="sxs-lookup"><span data-stu-id="02781-162">This option isn't available for CTP.</span></span>
- <span data-ttu-id="02781-163">**部分的な数量を含める場合**: 既定では、販売明細行の全数量を満たす提案のみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="02781-163">**Include partial quantity** - By default, only suggestions that fulfill the full quantity of the sales line are included.</span></span> <span data-ttu-id="02781-164">このオプションを選択すると、注文明細行を一部のみ満たすための提案を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="02781-164">Select this option to include suggestions that only partially fulfill the order line.</span></span> <span data-ttu-id="02781-165">このオプションは、顧客がより早い納期を要求し、部分配送を受け入れる場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="02781-165">This option is useful when the customer requests an earlier delivery date and accepts partial delivery.</span></span>
- <span data-ttu-id="02781-166">**後の日付を含める**: 既定では、販売明細行の現在の日付よりも良い (より早い) 提案のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="02781-166">**Include later dates** - By default, only suggestions that are better (earlier) than the current dates on the sales line are shown.</span></span> <span data-ttu-id="02781-167">後の日付を含める場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="02781-167">Select this option to include later dates.</span></span> <span data-ttu-id="02781-168">このオプションは、日付以外のパラメーターが優先される状況で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="02781-168">This option can be useful in situations where parameters other than the date have priority.</span></span> <span data-ttu-id="02781-169">たとえば、特定の仕入先と倉庫が推奨されることができます。</span><span class="sxs-lookup"><span data-stu-id="02781-169">For example, a specific vendor or warehouse might be preferred.</span></span>
- <span data-ttu-id="02781-170">**荷渡方法** - 配送時間と原価を最適化できる推奨されている荷渡方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="02781-170">**Mode of delivery** - Select the preferred mode of delivery to optimize transport time and cost.</span></span> <span data-ttu-id="02781-171">推奨される代替配送処理への影響がすぐに表示されます。</span><span class="sxs-lookup"><span data-stu-id="02781-171">You will immediately see the effect on the suggested delivery alternatives.</span></span> <span data-ttu-id="02781-172">したがって、代替オプションを簡単に比較できるようになります。</span><span class="sxs-lookup"><span data-stu-id="02781-172">Therefore, it's easy to compare the alternatives.</span></span>
- <span data-ttu-id="02781-173">**調達を含める** - 調達を選択すると、推奨される代替配送処理には、外部仕入先とその他の企業 (会社間) の両方から調達するオプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="02781-173">**Include procurement** - When procurement is selected, the suggested delivery alternatives include options to procure from both external vendors and other companies in the enterprise (intercompany).</span></span> <span data-ttu-id="02781-174">**調達を含める** オプションは、ATP および ATP + 払出安全日数のサポート利益幅の配送日管理でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="02781-174">The **Include procurement** option is supported for ATP and ATP + Issue margin delivery date control.</span></span> <span data-ttu-id="02781-175">製品の既定仕入先と製品の承認済み仕入先すべてからの調達オプションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="02781-175">Procurement options from the default purchase vendor for the product and all approved vendors for the product are included.</span></span>
- <span data-ttu-id="02781-176">外部仕入先の場合は、調達リード タイムに基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="02781-176">For external vendors, the calculation is based on the purchase lead time.</span></span>
- <span data-ttu-id="02781-177">会社間の場合は、調達会社の配送日管理に基づいて、調達会社からの入手可能なものが考慮されます。</span><span class="sxs-lookup"><span data-stu-id="02781-177">For intercompany, the calculation considers what is available from the sourcing company, based on delivery date control in the sourcing company.</span></span>
- <span data-ttu-id="02781-178">**配送タイプ** (調達に関連)</span><span class="sxs-lookup"><span data-stu-id="02781-178">**Delivery type** (Relevant for procurement)</span></span>
  - <span data-ttu-id="02781-179">**在庫** - 製品は販売明細行上にあるサイト/倉庫へ調達倉庫から出荷されます。</span><span class="sxs-lookup"><span data-stu-id="02781-179">**Stock** - Products are shipped from the sourcing warehouse to the site/warehouse on the sales line.</span></span> <span data-ttu-id="02781-180">その倉庫から顧客へ出荷されます。</span><span class="sxs-lookup"><span data-stu-id="02781-180">They are then shipped from that warehouse to the customer.</span></span>
  - <span data-ttu-id="02781-181">**直納** - 製品は調達倉庫から顧客に直接出荷されます。</span><span class="sxs-lookup"><span data-stu-id="02781-181">**Direct delivery** - Products are shipped directly from the sourcing warehouse to the customer.</span></span>

### <a name="the-availability-information-fasttab"></a><span data-ttu-id="02781-182">在庫情報クイック タブ</span><span class="sxs-lookup"><span data-stu-id="02781-182">The Availability information FastTab</span></span>

<span data-ttu-id="02781-183">このクイックタブの情報は選択した代替配送明細行に関連しています。</span><span class="sxs-lookup"><span data-stu-id="02781-183">Information on this FastTab is related to the delivery alternative line that is selected.</span></span> <span data-ttu-id="02781-184">販売注文明細行の配送日の管理によって、次の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="02781-184">The following information is shown, depending on the delivery date control for the sales line:</span></span>

- <span data-ttu-id="02781-185">**販売リード タイム**</span><span class="sxs-lookup"><span data-stu-id="02781-185">**Sales lead time**</span></span>
  - <span data-ttu-id="02781-186">**現在利用可能** - 現在現物手持在庫、現物引当済在庫、利用可能な現物在庫を表示します。</span><span class="sxs-lookup"><span data-stu-id="02781-186">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="02781-187">**パラメーター** - 在庫単位と販売リード タイムを表示します。</span><span class="sxs-lookup"><span data-stu-id="02781-187">**Parameters** - Show the inventory unit and sales lead time.</span></span>

- <span data-ttu-id="02781-188">**ATP および ATP + 払出安全日数**</span><span class="sxs-lookup"><span data-stu-id="02781-188">**ATP and ATP + Issue margin**</span></span>
  - <span data-ttu-id="02781-189">**現在利用可能** - 現在現物手持在庫、現物引当済在庫、利用可能な現物在庫を表示します。</span><span class="sxs-lookup"><span data-stu-id="02781-189">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="02781-190">**パラメーター** - 在庫単位と販売リード タイムを表示します。</span><span class="sxs-lookup"><span data-stu-id="02781-190">**Parameters** - Show the inventory unit and sales lead time.</span></span>
  - <span data-ttu-id="02781-191">**将来の使用可能性** - 選択したサイトおよび **代替配送処理** の倉庫における現在および未来の使用可能性がグラフで表示されます。</span><span class="sxs-lookup"><span data-stu-id="02781-191">**Future availability** - Show a graphical representation of current and future availability for the selected site and warehouse under **Delivery alternatives**.</span></span> <span data-ttu-id="02781-192">グラフ列を選択して、製品の未来の使用可能性に関する詳細情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="02781-192">You can select the chart columns to see more detailed information about the future availability of the product.</span></span> <span data-ttu-id="02781-193">スライダーには、ATP タイム フェンス内に関連する需要および供給注文が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="02781-193">The slider shows a list of relevant demand and supply orders within the ATP time fence.</span></span>

- <span data-ttu-id="02781-194">**CTP**</span><span class="sxs-lookup"><span data-stu-id="02781-194">**CTP**</span></span>
  - <span data-ttu-id="02781-195">**現在利用可能** - 現在現物手持在庫、現物引当済在庫、利用可能な現物在庫を表示します。</span><span class="sxs-lookup"><span data-stu-id="02781-195">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="02781-196">**パラメーター** - 在庫単位と販売リード タイムを表示します。</span><span class="sxs-lookup"><span data-stu-id="02781-196">**Parameters** - Show the inventory unit and sales lead time.</span></span>
  - <span data-ttu-id="02781-197">**展開** - 選択した代替配送処理の供給展開を表示します。</span><span class="sxs-lookup"><span data-stu-id="02781-197">**Explosion** - Show a supply explosion of the selected delivery alternative.</span></span> <span data-ttu-id="02781-198">**設定** でフィールドを変更し、展開に表示される分析コードを変更します。</span><span class="sxs-lookup"><span data-stu-id="02781-198">You can use **Setup** to change the fields and inventory dimensions that are shown in the explosion.</span></span>

### <a name="the-impact-of-selected-alternative-fasttab"></a><span data-ttu-id="02781-199">選択した代替の影響クイックタブ</span><span class="sxs-lookup"><span data-stu-id="02781-199">The Impact of selected alternative FastTab</span></span>

<span data-ttu-id="02781-200">このクイックタブには、選択した代替配送処理の影響が強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="02781-200">This FastTab highlights the impact of the selected delivery alternative.</span></span> <span data-ttu-id="02781-201">**OK** を選択すると、販売明細行は、選択した列の強調表示された値で更新されます。</span><span class="sxs-lookup"><span data-stu-id="02781-201">If you select **OK**, the sales line is updated with the highlighted values in the SELECTED columns.</span></span> <span data-ttu-id="02781-202">選択された代替配送処理の数量が販売注文明細行の数量より少ない場合は、配送スケジュールが作成されると、注文明細行が 2 つの行に分割されます。選択した数量と残余数量それぞれに 1 つの明細行が生成されます。</span><span class="sxs-lookup"><span data-stu-id="02781-202">Note that, if the quantity on the selected delivery alternative is less than quantity on the sales line, a delivery schedule is created, and the order line is split into two lines: one line for the selected quantity and one line for the remaining quantity.</span></span> <span data-ttu-id="02781-203">業務行を更新してスケジュール明細行と一致させ、価格設定に影響を与えることもできます。</span><span class="sxs-lookup"><span data-stu-id="02781-203">You can also update the commercial line so that it matches the schedule lines and affects the pricing.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="02781-204">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="02781-204">Additional resources</span></span>

[<span data-ttu-id="02781-205">注文納期日</span><span class="sxs-lookup"><span data-stu-id="02781-205">Order promising</span></span>](delivery-dates-available-promise-calculations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]