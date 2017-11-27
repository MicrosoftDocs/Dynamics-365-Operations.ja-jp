---
title: "原価バージョン"
description: "この記事は、原価バージョン、その管理方法、そこに含めることができるデータのタイプについての情報を提供します。 原価バージョンの主な目的は、品目、原価カテゴリ、間接原価の計算式に関する原価レコードを保持することです。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 54532
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cb8e8193b3312a63042a44cb082a33a196cbc1be
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="costing-versions"></a><span data-ttu-id="3f476-104">原価バージョン</span><span class="sxs-lookup"><span data-stu-id="3f476-104">Costing versions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3f476-105">この記事は、原価バージョン、その管理方法、そこに含めることができるデータのタイプについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="3f476-105">This article provides information about costing versions, how to maintain them, and the types of data that you can include in them.</span></span> <span data-ttu-id="3f476-106">原価バージョンの主な目的は、品目、原価カテゴリ、間接原価の計算式に関する原価レコードを保持することです。</span><span class="sxs-lookup"><span data-stu-id="3f476-106">The primary purpose of a costing version is to contain cost records about items, cost categories, and calculation formulas for indirect costs.</span></span>

<span data-ttu-id="3f476-107">原価バージョンは、内部に保持しているデータに応じて 1 つ以上の目的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="3f476-107">A costing version can serve one or more purposes, depending on the data that the costing version contains.</span></span> <span data-ttu-id="3f476-108">原価バージョンの主な目的は、品目、原価カテゴリ、間接原価の計算式に関する原価レコードを保持することです。</span><span class="sxs-lookup"><span data-stu-id="3f476-108">The primary purpose of a costing version is to contain cost records about items, cost categories, and calculation formulas for indirect costs.</span></span> <span data-ttu-id="3f476-109">原価バージョンには、割り当てられた原価タイプに基づいて、一連の標準原価レコードまたは予定原価レコードを格納することができます。</span><span class="sxs-lookup"><span data-stu-id="3f476-109">A costing version can contain a set of standard cost records or a set of planned cost records that are based on the costing type that is assigned to the costing version.</span></span>

## <a name="costing-versions-for-standard-or-planned-costs"></a><span data-ttu-id="3f476-110">標準または予定原価用の原価バージョン</span><span class="sxs-lookup"><span data-stu-id="3f476-110">Costing versions for standard or planned costs</span></span>
### <a name="standard-costs"></a><span data-ttu-id="3f476-111">標準原価</span><span class="sxs-lookup"><span data-stu-id="3f476-111">Standard costs</span></span>

<span data-ttu-id="3f476-112">標準原価 − 原価バージョンは、品目に対する標準原価在庫モデルをサポートできます。この場合、原価バージョンには品目および製造プロセスに関する一連の標準原価レコードが格納されます。</span><span class="sxs-lookup"><span data-stu-id="3f476-112">A costing version can support a standard cost inventory model for items, where the costing version contains a set of standard cost records about items and manufacturing processes.</span></span> <span data-ttu-id="3f476-113">製造プロセスに関する原価データは、工順の原価カテゴリおよび製造間接費の計算式で表されます。</span><span class="sxs-lookup"><span data-stu-id="3f476-113">Cost data about manufacturing processes is expressed in terms of the cost categories for routing operations and the calculation formulas for manufacturing overheads.</span></span>

### <a name="planned-costs"></a><span data-ttu-id="3f476-114">予定原価</span><span class="sxs-lookup"><span data-stu-id="3f476-114">Planned costs</span></span>

<span data-ttu-id="3f476-115">予定原価 − 原価バージョンに、品目および製造プロセスに関する一連の予定原価レコードを格納できます。</span><span class="sxs-lookup"><span data-stu-id="3f476-115">A costing version can contain a set of planned cost records about items and manufacturing processes.</span></span> <span data-ttu-id="3f476-116">予定原価の原価バージョンは、多くの場合、原価計算シミュレーション (購入材料や製造プロセスの原価変更が、製造された品目の原価計算に及ぼす影響のシミュレーションなど) に使われます。</span><span class="sxs-lookup"><span data-stu-id="3f476-116">A costing version that contains planned costs is often used to support cost calculation simulations, such as simulations of the effect that cost changes to purchased materials or manufacturing processes has on the calculated costs of manufactured items.</span></span> <span data-ttu-id="3f476-117">品目の予定原価の原価レコードを使用して、品目原価の初期値に指定することにより、実績原価在庫モデルをサポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3f476-117">The item cost records for planned costs can also be used to support an actual cost inventory model by providing the initial values for item costs.</span></span> <span data-ttu-id="3f476-118">これらの値には、製造品目の予定原価の計算が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f476-118">These values include the calculation of planned costs for manufactured items.</span></span>

## <a name="entering-costs"></a><span data-ttu-id="3f476-119">コスト入力</span><span class="sxs-lookup"><span data-stu-id="3f476-119">Entering costs</span></span>
<span data-ttu-id="3f476-120">原価バージョンにおける原価レコードのデータを管理するには、購入した品目およびサイト間で移動した品目の原価を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f476-120">Data maintenance for cost records in a costing version involves entering costs for purchased items and for items that are transferred between sites.</span></span> <span data-ttu-id="3f476-121">その他に製造環境のデータ管理では、工順に関連付けられた原価カテゴリの原価の入力、製造間接費を反映する間接原価の計算式の入力、および製造品目の原価計算を行います。</span><span class="sxs-lookup"><span data-stu-id="3f476-121">Additional data maintenance for manufacturers involves entering costs for cost categories that are associated with routing operations, entering calculation formulas for the indirect costs that reflect manufacturing overhead, and calculating costs for manufactured items.</span></span> 

<span data-ttu-id="3f476-122">原価バージョンにおける品目原価データは、各品目の 1 つまたは複数の原価レコードで構成されます。</span><span class="sxs-lookup"><span data-stu-id="3f476-122">The item cost data in a costing version consists of one or more cost records for each item.</span></span> <span data-ttu-id="3f476-123">品目の原価レコードを初期入力すると、ステータスは [**保留中**] であり、発効日が設定されています。</span><span class="sxs-lookup"><span data-stu-id="3f476-123">When an item cost record is first entered, it has **Pending** status and an intended effective date.</span></span> <span data-ttu-id="3f476-124">品目の原価レコードを有効にすると、ステータスは [**有効**] に更新され、発効日は有効化した日に更新されます。</span><span class="sxs-lookup"><span data-stu-id="3f476-124">When you activate the item cost record, the status is updated to **Active**, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="3f476-125">各品目原価レコードで、反映されるサイト、発効日、またはステータスが異なっている場合があります。</span><span class="sxs-lookup"><span data-stu-id="3f476-125">Different item cost records can reflect different sites, effective dates, or statuses.</span></span> <span data-ttu-id="3f476-126">未来の日付の製造完了品目の原価を計算する場合は、ステータスが [**保留中**] または [**有効**] であるかに関係なく、BOM の計算には、該当する発効日の原価レコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="3f476-126">When you calculate costs for manufactured items for a future date, the bill of materials (BOM) calculation uses cost records that have the relevant effective date, regardless of whether the status is **Pending** or **Active**.</span></span> <span data-ttu-id="3f476-127">品目の現在の有効な原価レコードを使用して、製造オーダー原価を見積もり、標準原価在庫モデルで在庫トランザクションを評価します。</span><span class="sxs-lookup"><span data-stu-id="3f476-127">An item's current active cost record is used to estimate production order costs and to value inventory transactions under a standard costing inventory model.</span></span> <span data-ttu-id="3f476-128">原価カテゴリの原価レコードおよび間接原価の計算式の管理は、品目原価レコードの管理と類似しています。</span><span class="sxs-lookup"><span data-stu-id="3f476-128">The maintenance of cost records for cost categories and indirect cost calculation formulas resembles the maintenance of item cost records.</span></span> 

<span data-ttu-id="3f476-129">原価バージョンに対する 2 つのブロック ポリシーで、保留原価を保持するかどうか、および保留原価を有効にするかどうかが決定されます。</span><span class="sxs-lookup"><span data-stu-id="3f476-129">Two blocking policies for a costing version determine whether pending costs can be maintained and whether the pending cost can be activated.</span></span> <span data-ttu-id="3f476-130">原価バージョンにおける原価レコードのデータ管理を許可または禁止するには、ブロック ポリシーを使用します。</span><span class="sxs-lookup"><span data-stu-id="3f476-130">Use the blocking policies to permit data maintenance, and then use them to prevent data maintenance for cost records in a costing version.</span></span> 

<span data-ttu-id="3f476-131">原価バージョンには、BOM の計算に使用する品目の販売価格や購買価格に関するデータも格納できます。</span><span class="sxs-lookup"><span data-stu-id="3f476-131">A costing version can also contain data about item sales prices or purchase prices for BOM calculation purposes.</span></span>

## <a name="item-sales-prices-for-bom-calculations"></a><span data-ttu-id="3f476-132">BOM 計算の品目の販売価格</span><span class="sxs-lookup"><span data-stu-id="3f476-132">Item sales prices for BOM calculations</span></span>
<span data-ttu-id="3f476-133">販売価格に関するデータを含める主な理由は、製造品目の計算済販売価格を保有することです。</span><span class="sxs-lookup"><span data-stu-id="3f476-133">The main reason for including data about sales prices is to retain a manufactured item’s calculated sales price.</span></span> <span data-ttu-id="3f476-134">計算済販売価格を分析し、コンポーネント、工順工程、および間接費がコストと販売価格に寄与する方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="3f476-134">The calculated sales price can then be analyzed to determine how components, routing operations, and overhead contribute to the cost and sales price.</span></span> 

<span data-ttu-id="3f476-135">販売価格に関するデータを含める 2 番目の理由は、コンポーネント品目の販売価格レコードを定義することです。</span><span class="sxs-lookup"><span data-stu-id="3f476-135">A secondary reason for including data about sales prices is to define the sales price records for component items.</span></span> <span data-ttu-id="3f476-136">これらのレコードは、製造された品目の販売価格を計算するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="3f476-136">These records can then be used to calculate the sales price of manufactured items.</span></span> <span data-ttu-id="3f476-137">最初に BOM 計算グループに埋め込まれている販売価格モデルを定義し、BOM 計算グループを購入品目に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3f476-137">You first define the sales price model that is embedded in a BOM calculation group, and assign the BOM calculation group to purchased items.</span></span> <span data-ttu-id="3f476-138">次に、予定原価を使用する BOM 計算を実行するとき、BOM 計算グループの原価価格モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3f476-138">Then, when you perform BOM calculations that use planned costs, you select the cost price model of the BOM calculation group.</span></span> 

<span data-ttu-id="3f476-139">そうしない場合、レコードが手動で入力されたか計算されたかにかかわらず、品目の販売価格レコードは照会情報としてのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f476-139">Otherwise, the sales price records for items are used only as reference information, regardless of whether the records are manually entered or calculated.</span></span> <span data-ttu-id="3f476-140">品目の販売価格レコードを有効化すると、品目の基準販売価格を更新できます。</span><span class="sxs-lookup"><span data-stu-id="3f476-140">By activating an item’s sales price record, you can update the item’s base sales price.</span></span> <span data-ttu-id="3f476-141">ただし、基準販売価格はサイト固有ではなく、手動で上書きできます。</span><span class="sxs-lookup"><span data-stu-id="3f476-141">However, the base sales price isn't site-specific and can be manually overridden.</span></span> <span data-ttu-id="3f476-142">品目の基準販売価格は、販売注文および販売見積に対する既定の販売価格として使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f476-142">The item’s base sales price is used as a default sales price on sales orders and sales quotations.</span></span>

## <a name="item-purchase-prices-for-bom-calculations"></a><span data-ttu-id="3f476-143">BOM 計算の品目の購買価格</span><span class="sxs-lookup"><span data-stu-id="3f476-143">Item purchase prices for BOM calculations</span></span>
<span data-ttu-id="3f476-144">購買価格のデータを有効にする主な理由は、コンポーネント品目の購買価格レコードを定義するためです。これらのレコードを使用して製造品目のコストを計算できるようになります。</span><span class="sxs-lookup"><span data-stu-id="3f476-144">The main reason for enabling purchase price data is to define purchase price records for component items, so that these records can be used to calculate the costs of manufactured items.</span></span> <span data-ttu-id="3f476-145">品目購買価格レコードは手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f476-145">The item purchase price records must be manually entered.</span></span> 

<span data-ttu-id="3f476-146">購買価格の内容を有効にするには、最初に、品目の購買価格のコスト価格モデルを含む BOM 計算グループを定義し、購入品目に BOM 計算グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3f476-146">To enable purchase price content, you first define a BOM calculation group that contains a cost price model for the item’s purchase price, and assign the BOM calculation group to purchased items.</span></span> <span data-ttu-id="3f476-147">計画コストを使用した BOM 計算を実行して製造品目の販売価格を計算するとき、BOM 計算グループにコスト価格モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="3f476-147">You then use a cost price model for the BOM calculation group when you perform BOM calculations that use planned costs to calculate the sales price of manufactured items.</span></span> 

<span data-ttu-id="3f476-148">品目の購買価格レコードは、参照情報としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f476-148">The purchase price records for items are also used as reference information.</span></span> <span data-ttu-id="3f476-149">品目の購買価格レコードの状態を [**保留中**] から [**有効**] に変更すると、品目の基準購買価格を更新できます。</span><span class="sxs-lookup"><span data-stu-id="3f476-149">By changing the status of an item’s purchase price record from **Pending** to **Active**, you can update the item’s base purchase price.</span></span> <span data-ttu-id="3f476-150">ただし、基準購買価格はサイト固有ではなく、手動で上書きできます。</span><span class="sxs-lookup"><span data-stu-id="3f476-150">However, the base purchase price isn't site-specific and can be manually overridden.</span></span> <span data-ttu-id="3f476-151">品目の基準購買価格は、発注書の既定の購買価格として使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f476-151">The item's base purchase price is used as a default purchase price on purchase orders.</span></span>




