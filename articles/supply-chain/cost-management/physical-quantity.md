---
title: 在庫オブジェクトの値
description: この記事は、在庫オブジェクトの値の計算方法についての情報を提供します。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e92c7889b11208c4d2b48eb279a104a7c226f904
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "319135"
---
# <a name="inventory-object-values"></a><span data-ttu-id="1c445-103">在庫オブジェクトの値</span><span class="sxs-lookup"><span data-stu-id="1c445-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c445-104">この記事は、在庫オブジェクトの値の計算方法についての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="1c445-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="1c445-105">**現物数量** という名前の新しい機能は、特定の在庫オブジェクトの値を表示できます。</span><span class="sxs-lookup"><span data-stu-id="1c445-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="1c445-106">原価オブジェクトは、在庫会計が実行されるエンティティ レベルを表します。</span><span class="sxs-lookup"><span data-stu-id="1c445-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="1c445-107">原価オブジェクトの詳細については、「[原価オブジェクト](cost-object.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c445-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="1c445-108">特定の在庫オブジェクトの値を表示するには、**原価のオブジェクト** ページで **現物数量** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c445-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="1c445-109">在庫オブジェクトの値がどのように計算されるかは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1c445-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="1c445-110">在庫オブジェクト . 値 = コスト オブジェクト . 平均単位コスト × 在庫オブジェクト . 数量</span><span class="sxs-lookup"><span data-stu-id="1c445-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="1c445-111">次の例では、在庫オブジェクトとコスト オブジェクトの値の計算方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1c445-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="1c445-112">2 つの製品受領書イベントは、品目 A に登録されます。</span><span class="sxs-lookup"><span data-stu-id="1c445-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="1c445-113">製品受領書 1 : 数量 = 100 個、金額 = $1,000.00、サイト = 1、倉庫 =11、バッチ番号。</span><span class="sxs-lookup"><span data-stu-id="1c445-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="1c445-114">= B1</span><span class="sxs-lookup"><span data-stu-id="1c445-114">= B1</span></span>
-   <span data-ttu-id="1c445-115">製品受領書 2 : 数量 = 50 個、金額 = $800.00、サイト = 1、倉庫 =11、バッチ番号。</span><span class="sxs-lookup"><span data-stu-id="1c445-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="1c445-116">= B2</span><span class="sxs-lookup"><span data-stu-id="1c445-116">= B2</span></span>

<span data-ttu-id="1c445-117">次の表に、原価オブジェクトの計算結果を示します。</span><span class="sxs-lookup"><span data-stu-id="1c445-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="1c445-118">**原価オブジェクト** ページの結果を表示できます。</span><span class="sxs-lookup"><span data-stu-id="1c445-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c445-119">オブジェクト タイプ</span><span class="sxs-lookup"><span data-stu-id="1c445-119">Object type</span></span></th>
<th><span data-ttu-id="1c445-120">品目番号</span><span class="sxs-lookup"><span data-stu-id="1c445-120">Item number</span></span></th>
<th><span data-ttu-id="1c445-121">サービス拠点</span><span class="sxs-lookup"><span data-stu-id="1c445-121">Site</span></span></th>
<th><span data-ttu-id="1c445-122">件数</span><span class="sxs-lookup"><span data-stu-id="1c445-122">Quantity</span></span></th>
<th><span data-ttu-id="1c445-123">在庫単位</span><span class="sxs-lookup"><span data-stu-id="1c445-123">Inventory unit</span></span></th>
<th><span data-ttu-id="1c445-124">値</span><span class="sxs-lookup"><span data-stu-id="1c445-124">Value</span></span></th>
<th><span data-ttu-id="1c445-125">平均単位原価</span><span class="sxs-lookup"><span data-stu-id="1c445-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c445-126">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="1c445-126">Cost object</span></span></td>
<td><span data-ttu-id="1c445-127">A</span><span class="sxs-lookup"><span data-stu-id="1c445-127">A</span></span></td>
<td><span data-ttu-id="1c445-128">1</span><span class="sxs-lookup"><span data-stu-id="1c445-128">1</span></span></td>
<td><span data-ttu-id="1c445-129">150</span><span class="sxs-lookup"><span data-stu-id="1c445-129">150</span></span></td>
<td><span data-ttu-id="1c445-130">個数</span><span class="sxs-lookup"><span data-stu-id="1c445-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="1c445-131">$1800.00</span><span class="sxs-lookup"><span data-stu-id="1c445-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="1c445-132">$12.00</span><span class="sxs-lookup"><span data-stu-id="1c445-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1c445-133">次の表に、在庫オブジェクトの計算結果を示します。</span><span class="sxs-lookup"><span data-stu-id="1c445-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="1c445-134">**原価オブジェクト** ページの **現物数量** をクリックすることにより、結果を表示できます。</span><span class="sxs-lookup"><span data-stu-id="1c445-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c445-135">オブジェクト タイプ</span><span class="sxs-lookup"><span data-stu-id="1c445-135">Object type</span></span></th>
<th><span data-ttu-id="1c445-136">品目番号</span><span class="sxs-lookup"><span data-stu-id="1c445-136">Item number</span></span></th>
<th><span data-ttu-id="1c445-137">サービス拠点</span><span class="sxs-lookup"><span data-stu-id="1c445-137">Site</span></span></th>
<th><span data-ttu-id="1c445-138">倉庫</span><span class="sxs-lookup"><span data-stu-id="1c445-138">Warehouse</span></span></th>
<th><span data-ttu-id="1c445-139">バッチ番号</span><span class="sxs-lookup"><span data-stu-id="1c445-139">Batch No.</span></span></th>
<th><span data-ttu-id="1c445-140">件数</span><span class="sxs-lookup"><span data-stu-id="1c445-140">Quantity</span></span></th>
<th><span data-ttu-id="1c445-141">在庫単位</span><span class="sxs-lookup"><span data-stu-id="1c445-141">Inventory unit</span></span></th>
<th><span data-ttu-id="1c445-142">値</span><span class="sxs-lookup"><span data-stu-id="1c445-142">Value</span></span></th>
<th><span data-ttu-id="1c445-143">平均単位原価</span><span class="sxs-lookup"><span data-stu-id="1c445-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c445-144">在庫オブジェクト</span><span class="sxs-lookup"><span data-stu-id="1c445-144">Inventory object</span></span></td>
<td><span data-ttu-id="1c445-145">A</span><span class="sxs-lookup"><span data-stu-id="1c445-145">A</span></span></td>
<td><span data-ttu-id="1c445-146">1</span><span class="sxs-lookup"><span data-stu-id="1c445-146">1</span></span></td>
<td><span data-ttu-id="1c445-147">11</span><span class="sxs-lookup"><span data-stu-id="1c445-147">11</span></span></td>
<td><span data-ttu-id="1c445-148">B1</span><span class="sxs-lookup"><span data-stu-id="1c445-148">B1</span></span></td>
<td><span data-ttu-id="1c445-149">100</span><span class="sxs-lookup"><span data-stu-id="1c445-149">100</span></span></td>
<td><span data-ttu-id="1c445-150">個数</span><span class="sxs-lookup"><span data-stu-id="1c445-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="1c445-151">$1200.00</span><span class="sxs-lookup"><span data-stu-id="1c445-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="1c445-152">$12.00</span><span class="sxs-lookup"><span data-stu-id="1c445-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c445-153">在庫オブジェクト</span><span class="sxs-lookup"><span data-stu-id="1c445-153">Inventory object</span></span></td>
<td><span data-ttu-id="1c445-154">A</span><span class="sxs-lookup"><span data-stu-id="1c445-154">A</span></span></td>
<td><span data-ttu-id="1c445-155">1</span><span class="sxs-lookup"><span data-stu-id="1c445-155">1</span></span></td>
<td><span data-ttu-id="1c445-156">11</span><span class="sxs-lookup"><span data-stu-id="1c445-156">11</span></span></td>
<td><span data-ttu-id="1c445-157">B2</span><span class="sxs-lookup"><span data-stu-id="1c445-157">B2</span></span></td>
<td><span data-ttu-id="1c445-158">50</span><span class="sxs-lookup"><span data-stu-id="1c445-158">50</span></span></td>
<td><span data-ttu-id="1c445-159">個数</span><span class="sxs-lookup"><span data-stu-id="1c445-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="1c445-160">$600.00</span><span class="sxs-lookup"><span data-stu-id="1c445-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="1c445-161">$12.00</span><span class="sxs-lookup"><span data-stu-id="1c445-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="1c445-162">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="1c445-162">Additional resources</span></span>
--------

[<span data-ttu-id="1c445-163">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="1c445-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="1c445-164">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="1c445-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="1c445-165">新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="1c445-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



