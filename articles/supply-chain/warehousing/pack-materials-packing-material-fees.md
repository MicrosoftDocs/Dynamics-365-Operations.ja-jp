---
title: 梱包材および費用
description: このトピックでは、特定の期間にリサイクル会社に支払われる梱包材費用についての情報を提供します。
author: MarkusFogelberg
manager: tfehr
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1061f336701461df7a2cf78661788e4c6100c84d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215703"
---
# <a name="packing-materials-and-fees"></a><span data-ttu-id="b2363-103">梱包材および費用</span><span class="sxs-lookup"><span data-stu-id="b2363-103">Packing materials and fees</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2363-104">梱包材費用は、特定の間隔でリサイクル会社に支払われます。</span><span class="sxs-lookup"><span data-stu-id="b2363-104">Packing material fees are paid to a recycling company at specific intervals.</span></span> <span data-ttu-id="b2363-105">梱包単位を構成する各材料について、重量単位あたりの金額が支払われます。</span><span class="sxs-lookup"><span data-stu-id="b2363-105">An amount is paid, per unit of weight, for each material that a packing unit consists of.</span></span> <span data-ttu-id="b2363-106">梱包材費用は計算および報告されますが、所轄官庁に支払う必要がある税とは見なされないため、元帳トランザクションは転記されません。</span><span class="sxs-lookup"><span data-stu-id="b2363-106">Although packing material fees are calculated and reported, no ledger transactions are posted, because the fees aren't considered taxes that must be paid to an authority.</span></span>

<span data-ttu-id="b2363-107">梱包材の重量および費用は、販売注文明細行および購買注文明細行で計算されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-107">Packing material weights and fees are calculated for sales order lines and purchase order lines.</span></span>

<span data-ttu-id="b2363-108">1 つの品目、品目のグループ (梱包グループ)、またはすべての品目に対して、梱包単位を 1 つ以上定義できます。</span><span class="sxs-lookup"><span data-stu-id="b2363-108">You can define one or more packing units for a single item, a group of items (packing group), or all items.</span></span> <span data-ttu-id="b2363-109">梱包単位は、梱包材と、梱包材重量、および梱包単位に含まれる品目数から構成されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-109">A packing unit consists of the packing materials, their weights, and the number of items that are included in the packing unit.</span></span> <span data-ttu-id="b2363-110">梱包材コードが、定義された梱包材の各タイプに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b2363-110">A packing material code is assigned to each type of packing material that is defined.</span></span> <span data-ttu-id="b2363-111">梱包材コードに基づいて、特定の期間の価格を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b2363-111">Based on the packing material code, you can specify a price for a specific period.</span></span> <span data-ttu-id="b2363-112">梱包材費用はこの情報に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-112">The packing material fee is calculated based on this information.</span></span>

> [!NOTE]
> <span data-ttu-id="b2363-113">梱包材費用を支払っていない会社でも、この機能を使用して、梱包材の重量の統計を計算できます。</span><span class="sxs-lookup"><span data-stu-id="b2363-113">Even if your company doesn't pay packing material fees, you can use the functionality to calculate statistics for the weights of packing materials.</span></span>

## <a name="set-up-packing-material-allocation"></a><a name="allocations"></a><span data-ttu-id="b2363-114">梱包材の配賦の設定</span><span class="sxs-lookup"><span data-stu-id="b2363-114">Set up packing material allocation</span></span>

<span data-ttu-id="b2363-115">梱包材重量、梱包材費用、またはその両方を計算する前に、計算を有効にして、どの材料および費用ををどの品目に適用するかを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2363-115">Before you can calculate packing material weights, packing material fees, or both, you must turn on the calculation and define which materials and fees apply to which items.</span></span>

1. <span data-ttu-id="b2363-116">**在庫管理 \> 設定 \> 在庫および倉庫管理パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2363-116">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="b2363-117">**一般**タブの**梱包材** セクションで、**梱包材費用の計算**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="b2363-117">On the **General** tab, in the **Packing material** section, set the **Calculate packing material fees** option to **Yes**.</span></span>
1. <span data-ttu-id="b2363-118">**在庫管理 \> 設定 \> 梱包材 \> 梱包グループ**の順に移動して、使用するすべての梱包グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="b2363-118">Go to **Inventory management \> Setup \> Packing material \> Packing groups**, and create all the packing groups that you use.</span></span> <span data-ttu-id="b2363-119">梱包グループ内のすべての品目は、同じ梱包材配賦を使用します。</span><span class="sxs-lookup"><span data-stu-id="b2363-119">All the items in a packing group will use the same packing material allocation.</span></span> <span data-ttu-id="b2363-120">梱包グループを使用しない場合は、このステップを省略できます。</span><span class="sxs-lookup"><span data-stu-id="b2363-120">If you don't use packing groups, you can skip this step.</span></span>

    > [!TIP]
    > <span data-ttu-id="b2363-121">梱包グループを作成したら、必要に応じて各製品にグループを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b2363-121">After you've created your packing groups, can assign a group to each product as you require.</span></span> <span data-ttu-id="b2363-122">**製品情報管理 \> 製品 \> リリース済製品**の順に移動して、製品を選択してから、**在庫の管理**クイック タブの**梱包グループ** フィールドで、適切な梱包グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2363-122">Go to **Product information management \> Products \> Released products**, select a product, and then, on the **Manage inventory** FastTab, in the **Packing group** field, select the appropriate packing group.</span></span>

1. <span data-ttu-id="b2363-123">**在庫管理 \> 設定 \> 梱包材 \> 梱包材コード**の順に移動して、使用する梱包材のタイプを定義し、出荷の準備時に梱包材を消費する単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2363-123">Go to **Inventory management \> Setup \> Packing material \> Packing material codes**, define each type of packing material that you use, and specify the unit that the packing material is consumed in when you prepare shipments.</span></span>
1. <span data-ttu-id="b2363-124">**在庫管理 \> 設定 \> 梱包材 \> 梱包材費用**の順に移動して、先ほど定義した梱包材のタイプごとに費用を設定します。</span><span class="sxs-lookup"><span data-stu-id="b2363-124">Go to **Inventory management \> Setup \> Packing material \> Packing material fees**, and set a fee for each type of packing material that you just defined.</span></span> <span data-ttu-id="b2363-125">費用は、消費される単位あたりの価格に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-125">Fees are calculated based on the price per unit that is consumed.</span></span>
1. <span data-ttu-id="b2363-126">梱包材を品目に配賦するには、**在庫管理 \> 設定 \> 梱包材 \> 梱包材の配賦**の順に移動して、配賦を作成します。</span><span class="sxs-lookup"><span data-stu-id="b2363-126">To allocate packing materials to items, go to **Inventory management \> Setup \> Packing material \> Packaging material allocation**, and create allocations.</span></span> <span data-ttu-id="b2363-127">必要な数の配賦を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="b2363-127">You can create as many allocations as you require.</span></span> <span data-ttu-id="b2363-128">配賦の詳細度に応じて、個々の品目、品目のグループ (梱包グループ)、またはすべての品目の梱包材を配賦することができます。</span><span class="sxs-lookup"><span data-stu-id="b2363-128">You can allocate packing materials for individual items, groups of items (packing groups), or all items, depending on how detailed your allocations should be.</span></span>

    <span data-ttu-id="b2363-129">作成するそれぞれの配賦で、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b2363-129">For each allocation that you create, follow these steps.</span></span>

    1. <span data-ttu-id="b2363-130">**一般**クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="b2363-130">On the **General** FastTab, set the following fields:</span></span>

        - <span data-ttu-id="b2363-131">**品目コード** – 配賦の範囲を選択します:</span><span class="sxs-lookup"><span data-stu-id="b2363-131">**Item code** – Select the scope of the allocation:</span></span>

            - <span data-ttu-id="b2363-132">**テーブル** – 1 つの特定の品目に配賦を作成します。</span><span class="sxs-lookup"><span data-stu-id="b2363-132">**Table** – Create an allocation for a single specific item.</span></span>
            - <span data-ttu-id="b2363-133">**グループ** – **梱包グループ** ページで定義されている梱包グループに属しているすべての品目の配賦を作成します。</span><span class="sxs-lookup"><span data-stu-id="b2363-133">**Group** – Create an allocation for all the items the belong to a packing group that is defined on the **Packing groups** page.</span></span>
            - <span data-ttu-id="b2363-134">**すべて** – すべての品目に対して配賦を作成します。</span><span class="sxs-lookup"><span data-stu-id="b2363-134">**All** – Create an allocation for all items.</span></span>

            > [!NOTE]
            > <span data-ttu-id="b2363-135">通常は、すべての配賦を同じレベル (**テーブル**、**グループ**、または**すべて**) に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2363-135">Usually, you should make all your allocations at the same level (**Table**, **Group**, or **All**).</span></span> <span data-ttu-id="b2363-136">複数のレベルを使用する場合は、各品目に対して最も具体的に一致する配賦が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-136">If you use more than one level, the most specific matching allocation will be used for each item.</span></span> <span data-ttu-id="b2363-137">(**テーブル** レベルは**グループ** レベルより優先され、両方のレベルが**すべて**レベルよりも優先されます。)</span><span class="sxs-lookup"><span data-stu-id="b2363-137">(The **Table** level takes precedence over the **Group** level, and both those levels take precedence over the **All** level.)</span></span>

        - <span data-ttu-id="b2363-138">**商品関係** – 1 つの品目に配賦する場合は、その品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2363-138">**Item relation** – If you're allocating for a single item, select the item.</span></span> <span data-ttu-id="b2363-139">品目のグループに対して配賦する場合は、梱包グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2363-139">If you're allocating for a group of items, select the packing group.</span></span> <span data-ttu-id="b2363-140">すべての品目に対して配賦する場合は、このフィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="b2363-140">If you're allocating for all items, leave this field blank.</span></span>
        - <span data-ttu-id="b2363-141">**構成**、**サイズ**、**色**、および**スタイル** – 配賦する品目をさらに定義するには、必要に応じてこれらの分析コードの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2363-141">**Configuration**, **Size**, **Color**, and **Style** – Enter values for these dimensions as you require, to further define the item that you're allocating for.</span></span>
        - <span data-ttu-id="b2363-142">**梱包単位** – 梱包材が使用されるときに、品目が梱包される単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2363-142">**Packing unit** – Select the unit that the item is packaged in when the packing material is used.</span></span> <span data-ttu-id="b2363-143">この単位は、品目が購買されて保管される単位とは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b2363-143">This unit might differ from the unit that the item is purchased and stored in.</span></span>
        - <span data-ttu-id="b2363-144">**梱包単位係数** – 在庫単位から梱包単位に換算するために使用される換算率を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2363-144">**Packing unit factor** – Enter the conversion factor that is used to convert from the inventory unit to the packing unit.</span></span> <span data-ttu-id="b2363-145">(換算では、数式*梱包単位* = *品目単位* × *梱包単位係数*が使用されます。)</span><span class="sxs-lookup"><span data-stu-id="b2363-145">(The conversion uses the formula *Packing units* = *Item units* × *Packing unit factor*.)</span></span>

    1. <span data-ttu-id="b2363-146">**梱包材**クイック タブで、現在の配賦に必要な梱包材ごとに明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="b2363-146">On the **Packing material** FastTab, add a line for each piece of packing material that is required for the current allocation.</span></span> <span data-ttu-id="b2363-147">各明細行で、(**梱包材コード** ページで定義されている) 材料のタイプと、現在の品目の出荷単位ごとに消費される材料の量を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2363-147">On each line, specify the type of material (as defined on the **Packing material codes** page) and the amount of it that is consumed for each shipped unit of the current item.</span></span>

## <a name="packing-units-on-sales-order-lines"></a><span data-ttu-id="b2363-148">販売注文明細行の梱包単位</span><span class="sxs-lookup"><span data-stu-id="b2363-148">Packing units on sales order lines</span></span>

<span data-ttu-id="b2363-149">[梱包材費用の計算を有効にして配賦を設定](#allocations) した後、販売注文に追加される各品目に梱包単位が指定されているかどうかがシステムによって確認されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-149">After you've [turned on the calculation for packing material fees and set up your allocations](#allocations), the system verifies that packing units are specified for each item that is added to a sales order.</span></span> <span data-ttu-id="b2363-150">その後、必要な費用が計算されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-150">It then calculates any fees that are required.</span></span> <span data-ttu-id="b2363-151">品目が販売注文に追加されると、次のいずれかの手順が実行されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-151">When an item is added to a sales order, one of the following steps occurs:</span></span>

- <span data-ttu-id="b2363-152">**梱包配賦が品目に適用される場合:** 販売注文明細行が、指定された梱包単位と梱包単位数量でシステムによって更新されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-152">**If a packing allocation applies to the item:** The system updates the sales order line with the specified packing unit and the packing unit quantity.</span></span> <span data-ttu-id="b2363-153">(梱包単位数量は、数式*梱包単位数量* = *注文済数量* ÷ *選択された梱包単位に含まれる品目の数*で計算されます。)</span><span class="sxs-lookup"><span data-stu-id="b2363-153">(The packing unit quantity is calculated by using the formula *Packing unit quantity* = *Ordered quantity* ÷ *Number of items in the selected packing unit*.)</span></span>
- <span data-ttu-id="b2363-154">**梱包配賦が品目に適用されない場合:** 梱包単位および梱包単位数量を手動で販売注文明細行に入力できます。</span><span class="sxs-lookup"><span data-stu-id="b2363-154">**If no packing allocation applies to the item:** You can manually enter a packing unit and a packing unit quantity on the sales order line.</span></span>

<span data-ttu-id="b2363-155">販売注文明細行を転記する際に、梱包単位および梱包単位数量を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="b2363-155">You can also change the packing unit and the packing unit quantity when you post the sales order line.</span></span> <span data-ttu-id="b2363-156">この機能が関係してくるのは、販売注文明細行の一部のみを出荷または請求する場合です。</span><span class="sxs-lookup"><span data-stu-id="b2363-156">This capability is relevant if the sales order line is only partly delivered or partly invoiced.</span></span>

<span data-ttu-id="b2363-157">販売注文の請求時に、システムによって梱包材トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-157">When you invoice the sales order, the system creates packing material transactions.</span></span> <span data-ttu-id="b2363-158">梱包材トランザクションには、販売注文明細行の梱包材重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b2363-158">Packing material transactions contain the weights of the packing materials for the sales line.</span></span> <span data-ttu-id="b2363-159">このトランザクションは、請求した後に変更できます。</span><span class="sxs-lookup"><span data-stu-id="b2363-159">You can modify the transactions after you invoice them.</span></span> <span data-ttu-id="b2363-160">これにより、新しいトランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="b2363-160">You can then create new transactions.</span></span>

## <a name="packing-units-on-purchase-order-lines"></a><span data-ttu-id="b2363-161">購買注文明細行の梱包単位</span><span class="sxs-lookup"><span data-stu-id="b2363-161">Packing units on purchase order lines</span></span>

<span data-ttu-id="b2363-162">システムは、購買注文明細行の梱包材トランザクションを作成しません。</span><span class="sxs-lookup"><span data-stu-id="b2363-162">The system doesn't create packing material transactions for purchase order lines.</span></span> <span data-ttu-id="b2363-163">代わりに、**梱包材の購買トランザクションの作成**ページで、請求済購買注文明細行に対するトランザクションを手動で作成します。</span><span class="sxs-lookup"><span data-stu-id="b2363-163">Instead, you manually create transactions for invoiced purchase order lines on the **Packing material transactions** page.</span></span>

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a><span data-ttu-id="b2363-164">梱包材費用が請求される顧客のライセンス番号を設定する</span><span class="sxs-lookup"><span data-stu-id="b2363-164">Set up license numbers for customers that are charged packing material fees</span></span>

<span data-ttu-id="b2363-165">特定の顧客の販売注文に、各注文に対して使用される梱包材の請求金額を含める場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b2363-165">If the sales orders for a specific customer should include charges for the packing materials that are used for each order, follow these steps.</span></span>

1. <span data-ttu-id="b2363-166">**売掛金勘定 \> 顧客 \> すべての顧客**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2363-166">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="b2363-167">梱包材に対して請求する顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2363-167">Select the customer that should be charged for packing materials.</span></span>
1. <span data-ttu-id="b2363-168">**請求書と出荷**クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="b2363-168">On the **Invoice and delivery** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="b2363-169">**売上税**セクションの**梱包税ライセンス番号**フィールドに、会社のライセンス番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2363-169">In the **Sales tax** section, in the **Packing duty license number** field, enter the company's license number.</span></span>
    - <span data-ttu-id="b2363-170">**梱包材費用**セクションの**ライセンス番号**フィールドに、会社のライセンス番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2363-170">In the **Packing material fee** section, in the **License number** field, enter the company's license number.</span></span>

<span data-ttu-id="b2363-171">これで、梱包材を使用する 1 つ以上の品目を含む販売注文を作成および請求すると、請求書に梱包材費用が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-171">Now, when you create and invoice a sales order that includes one or more items that use packing materials, the invoice will show the packing material fees.</span></span>

<span data-ttu-id="b2363-172">梱包材費用を支払う必要がない顧客の場合は、これらの同じ手順に従いますが、**梱包税ライセンス番号**フィールドおよび**ライセンス番号**フィールドからライセンス番号を削除します。</span><span class="sxs-lookup"><span data-stu-id="b2363-172">For customers that should not pay packing material fees, follow these same steps, but clear the license numbers from the **Packing duty license number** and **License number** fields.</span></span> <span data-ttu-id="b2363-173">梱包材費用を支払わない顧客の請求書には、梱包材の重量が表示されますが、費用は表示されません。</span><span class="sxs-lookup"><span data-stu-id="b2363-173">Invoices for customers that don't pay packing material fees show the weights of the packing materials, but they don't show the fees.</span></span>

<span data-ttu-id="b2363-174">特定の期間に会社が支払う梱包材費用をすべて表示するレポートを生成するには、**在庫管理 \> 照会およびレポート \> 梱包材レポート \> 梱包材費用の計算**の順に移動して、日付の範囲を指定してから **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2363-174">To generate a report that shows all the packing material fees that your company will owe for a specific period, go to **Inventory management \> Inquiries and reports \> Packing material reports \> Packing material fee calculation**, specify a range of dates, and then select **OK**.</span></span>

## <a name="print-packing-material-weights-on-invoices"></a><span data-ttu-id="b2363-175">請求書への梱包材重量の印刷</span><span class="sxs-lookup"><span data-stu-id="b2363-175">Print packing material weights on invoices</span></span>

<span data-ttu-id="b2363-176">請求書に梱包材重量を印刷し、だれが関連する費用を支払うかを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="b2363-176">You can print packing material weights on an invoice and indicate who pays the related fees.</span></span> <span data-ttu-id="b2363-177">重量は、梱包コードごとに集計されます。</span><span class="sxs-lookup"><span data-stu-id="b2363-177">The weights are summarized by packaging code.</span></span>

1. <span data-ttu-id="b2363-178">**売掛金勘定 \> 設定 \> 売掛金勘定パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2363-178">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
1. <span data-ttu-id="b2363-179">**更新**タブの**請求書**クイック タブで、**梱包材重量の印刷**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="b2363-179">On the **Updates** tab, on the **Invoice** FastTab, set the **Print packing material weight** option to **Yes**.</span></span>
