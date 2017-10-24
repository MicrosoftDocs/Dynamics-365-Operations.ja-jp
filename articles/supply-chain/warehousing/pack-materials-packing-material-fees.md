---
title: "梱包材および費用"
description: "梱包材費用は、一定の間隔でリサイクル会社に支払われます。 梱包単位を構成する各材料について、重量単位あたりの金額が支払われます。 梱包材費用は計算および報告されますが、所轄官庁に支払う必要がある税とは見なされないため、元帳トランザクションは転記されません。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d7cd7b3d60e9c265a766695b53d8d27ee2a8d0a
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="packing-materials-and-fees"></a><span data-ttu-id="d35d2-105">梱包材および費用</span><span class="sxs-lookup"><span data-stu-id="d35d2-105">Packing materials and fees</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d35d2-106">梱包材費用は、一定の間隔でリサイクル会社に支払われます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-106">Packing material fees are paid to a recycling company at certain intervals.</span></span> <span data-ttu-id="d35d2-107">梱包単位を構成する各材料について、重量単位あたりの金額が支払われます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-107">An amount is paid, per unit of weight, for each material that a packing unit consists of.</span></span> <span data-ttu-id="d35d2-108">梱包材費用は計算および報告されますが、所轄官庁に支払う必要がある税とは見なされないため、元帳トランザクションは転記されません。</span><span class="sxs-lookup"><span data-stu-id="d35d2-108">Packing material fees are calculated and reported, but no ledger transactions are posted because the fees are not regarded as taxes to be paid to an authority.</span></span>

<span data-ttu-id="d35d2-109">梱包材の重量および費用は、販売注文明細行と購買注文明細行の両方で計算されます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-109">Packing material weights and fees are calculated for sales order lines and for purchase order lines.</span></span>

<span data-ttu-id="d35d2-110">1 つの品目、品目の梱包グループ、またはすべての品目に対して、梱包単位を 1 つ以上定義できます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-110">You can define one or more packing units for an item, for a packing group of items, or for all items.</span></span> <span data-ttu-id="d35d2-111">梱包単位は、梱包材と、梱包材重量、および梱包単位に含まれる品目数から構成されます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-111">A packing unit consists of the packing materials, their weights, and the number of items that are included in the packing unit.</span></span> <span data-ttu-id="d35d2-112">梱包材コードが、定義された梱包材の各タイプに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-112">A packing material code is assigned to each type of packing material that is defined.</span></span> <span data-ttu-id="d35d2-113">梱包材コードに基づいて、指定した期間の価格を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-113">Based on the packing material code, you can specify a price for a specified period.</span></span> <span data-ttu-id="d35d2-114">梱包材費用はこの情報に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-114">The packing material fee is calculated based on this information.</span></span>

| <span data-ttu-id="d35d2-115">**メモ**</span><span class="sxs-lookup"><span data-stu-id="d35d2-115">**Note**</span></span>                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d35d2-116">梱包材費用を支払っていない会社でも、この機能を使用して、梱包材の重量の統計を計算できます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-116">Even if your company does not pay packing material fees, you can use the functionality to calculate statistics for the weights of packing materials.</span></span> |

## <a name="setup-requirements-for-packing-material-fees"></a><span data-ttu-id="d35d2-117">梱包材費用の要件の設定</span><span class="sxs-lookup"><span data-stu-id="d35d2-117">Setup requirements for packing material fees</span></span>
<span data-ttu-id="d35d2-118">梱包材重量、梱包材費用、またはその両方を計算する前に、次の基本データを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d35d2-118">Before you calculate packing material weights or packing material fees, or both, you must create the following base data:</span></span>

-   <span data-ttu-id="d35d2-119">梱包グループ – 品目に割り当てる梱包グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="d35d2-119">Packing groups – Create packing groups to assign to items.</span></span>
-   <span data-ttu-id="d35d2-120">梱包材コード – 定義された梱包材のタイプごとの梱包材コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="d35d2-120">Packing material codes – Create packing material codes for each type of packing material that is defined.</span></span>
-   <span data-ttu-id="d35d2-121">梱包単位 – 1 つの品目、梱包グループ、またはすべての品目の梱包単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="d35d2-121">Packing units – Specify a packing unit for an item, for a packing group, or for all items.</span></span> <span data-ttu-id="d35d2-122">各梱包単位について、含める梱包材を定義し、重量を割り当て、[梱包単位係数] フィールドに、在庫単位から換算率を入力します。</span><span class="sxs-lookup"><span data-stu-id="d35d2-122">For each packing unit, define which packing materials to include, assign weights, and, in the Packing unit factor field, enter the conversion factor from the inventory unit.</span></span>
-   <span data-ttu-id="d35d2-123">梱包材費用 – 梱包材コードごとの梱包材費用を指定します。</span><span class="sxs-lookup"><span data-stu-id="d35d2-123">Packing material fees – Specify packing material fees per packing material code.</span></span> <span data-ttu-id="d35d2-124">各梱包材タイプについて、有効期間、材料あたりの価格、通貨、および単位を定義します。</span><span class="sxs-lookup"><span data-stu-id="d35d2-124">For each type of material, define the period of validity, the price per material, the currency, and the unit.</span></span>

## <a name="packing-units-on-sales-order-lines"></a><span data-ttu-id="d35d2-125">販売注文明細行の梱包単位</span><span class="sxs-lookup"><span data-stu-id="d35d2-125">Packing units on sales order lines</span></span>
<span data-ttu-id="d35d2-126">販売注文明細行を作成する際には、システムは、品目の梱包単位が指定されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d35d2-126">When you create a sales order line, the system checks to see whether packing units are specified for the item.</span></span> <span data-ttu-id="d35d2-127">梱包単位が指定されている場合、販売注文明細行が、指定された梱包単位と梱包単位数量で更新されます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-127">If packing units are specified, the system updates the sales order line with the specified packing unit and the packing unit quantity.</span></span> <span data-ttu-id="d35d2-128">梱包単位数量は、選択された梱包単位に含まれる品目の数で分割された注文済数量に基づきます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-128">The packing unit quantity is based on the ordered quantity divided by the number of items in the selected packing unit.</span></span> <span data-ttu-id="d35d2-129">梱包単位が指定されていない場合は、梱包単位および梱包単位数量を手動で販売注文明細行に入力できます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-129">If a packing unit has not been specified, you can manually enter a packing unit and a packing unit quantity on the sales order line.</span></span> <span data-ttu-id="d35d2-130">販売注文明細行を転記する際に、梱包単位および梱包単位数量を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-130">You can also change the packing unit and the packing unit quantity when you post the sales order line.</span></span> <span data-ttu-id="d35d2-131">この変更が関係してくるのは、販売注文明細行の一部のみを出荷または請求する場合です。</span><span class="sxs-lookup"><span data-stu-id="d35d2-131">This is relevant if the sales order line is only partly delivered or partly invoiced.</span></span> <span data-ttu-id="d35d2-132">販売注文の請求時に、梱包材トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-132">When you invoice the sales order, packing material transactions are created.</span></span> <span data-ttu-id="d35d2-133">梱包材トランザクションには、販売注文明細行の梱包材重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-133">Packing material transactions contain the weights of the packing materials for the sales line.</span></span> <span data-ttu-id="d35d2-134">トランザクションの請求後にそのトランザクションを変更して、新しいトランザクションを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-134">You can also modify the transactions after you invoice them, and then create new transactions.</span></span>

## <a name="packing-units-on-purchase-order-lines"></a><span data-ttu-id="d35d2-135">購買注文明細行の梱包単位</span><span class="sxs-lookup"><span data-stu-id="d35d2-135">Packing units on purchase order lines</span></span>
<span data-ttu-id="d35d2-136">購買注文明細行の梱包材トランザクションは自動的には作成されません。</span><span class="sxs-lookup"><span data-stu-id="d35d2-136">Packing material transactions for a purchase order line are not created by the system.</span></span> <span data-ttu-id="d35d2-137">**梱包材の購買トランザクションの作成**ページで、請求済購買注文明細行に対するトランザクションを手動で作成します。</span><span class="sxs-lookup"><span data-stu-id="d35d2-137">You create transactions for invoiced purchase order lines manually in the **Packing material transactions** page.</span></span>

## <a name="set-up-customer-packagingmaterialfee-license-numbers"></a><span data-ttu-id="d35d2-138">顧客の梱包材費用ライセンス番号の設定</span><span class="sxs-lookup"><span data-stu-id="d35d2-138">Set up customer packagingmaterialfee license numbers</span></span>
<span data-ttu-id="d35d2-139">顧客が梱包材費用を支払う場合は、**顧客**ページで顧客の梱包材費用ライセンス番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="d35d2-139">If the customers pay the packaging material fees, specify the customers' packaging-material-fee license numbers in the **Customers** page.</span></span> <span data-ttu-id="d35d2-140">ライセンス番号が顧客に割り当てられている場合、販売注文が請求されるときに梱包材費用は自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-140">When a license number has been assigned to a customer, the packaging material fees are calculated automatically when sales orders are invoiced.</span></span> <span data-ttu-id="d35d2-141">請求後は、レポートの計算および印刷を行う必要がないため、**梱包材トランザクション** ページの [**手数料計算**] チェック ボックスがオフになります。</span><span class="sxs-lookup"><span data-stu-id="d35d2-141">After invoicing, the **Calculate fee** check box is cleared in the **Packing material transactions** page, because you do not have to calculate and print a report.</span></span> <span data-ttu-id="d35d2-142">梱包材重量を請求書に印刷し、顧客が費用を支払うことを顧客に通知するように選択できます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-142">You can print the packaging material weights on the invoice, and inform the customers that they pay the fees.</span></span> 

<span data-ttu-id="d35d2-143">法人が梱包材費用を支払う場合、顧客のライセンス番号を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="d35d2-143">If your company pays the packaging material fees, do not specify the customer license numbers.</span></span> <span data-ttu-id="d35d2-144">請求後は、**梱包材トランザクション** ページの [**手数料計算**] チェック ボックスが選択されます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-144">After invoicing, the **Calculate fee** check box is selected in the **Packing material transactions** page.</span></span> <span data-ttu-id="d35d2-145">これにより、レポートが作成されるときに費用が計算されることが示されます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-145">This indicates that the fees are calculated when a report is created.</span></span> <span data-ttu-id="d35d2-146">請求書に重量を印刷し、法人が費用を支払うことを示すように選択できます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-146">You can print the weights on the invoice, and indicate that your company pays the fees.</span></span>

## <a name="print-packaging-material-weights-on-invoices"></a><span data-ttu-id="d35d2-147">請求書への梱包材重量の印刷</span><span class="sxs-lookup"><span data-stu-id="d35d2-147">Print packaging material weights on invoices</span></span>
<span data-ttu-id="d35d2-148">請求書に、梱包材重量を印刷し、だれが梱包材費用を支払うかを示すように選択できます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-148">You can print the packaging material weights on the invoice, and indicate who pays the packaging material fees.</span></span> <span data-ttu-id="d35d2-149">重量は、梱包コードごとに集計されます。</span><span class="sxs-lookup"><span data-stu-id="d35d2-149">The weights are summarized by packaging code.</span></span>
 





