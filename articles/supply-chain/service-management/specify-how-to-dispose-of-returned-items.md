---
title: 返品品目の廃棄方法の指定
description: 返品品目の廃棄方法を指定します。
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eaeb2589329809e57ac01aba85067e94c15477c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817488"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="080ea-103">返品品目の廃棄方法の指定</span><span class="sxs-lookup"><span data-stu-id="080ea-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="080ea-104">返品注文を処理する場合、製品が返品されている理由を識別する返品理由コードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="080ea-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="080ea-105">返品製品自体に何が実行されたかを特定する廃棄コード、および処分アクションも指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="080ea-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="080ea-106">廃棄コードは、返品注文の作成、品目到着の登録または品目到着の梱包明細の更新、および検査指示の終了時に適用できます。</span><span class="sxs-lookup"><span data-stu-id="080ea-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="080ea-107">業務プロセスをサポートするため、任意の必要な廃棄コードを定義できます。</span><span class="sxs-lookup"><span data-stu-id="080ea-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="080ea-108">次の表に、返品品目の廃棄を割り当てるために一般的に使用されるコードを示します。</span><span class="sxs-lookup"><span data-stu-id="080ea-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="080ea-109">廃棄タイプ</span><span class="sxs-lookup"><span data-stu-id="080ea-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="080ea-110">一般的なコード</span><span class="sxs-lookup"><span data-stu-id="080ea-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="080ea-111">説明</span><span class="sxs-lookup"><span data-stu-id="080ea-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="080ea-112">処分</span><span class="sxs-lookup"><span data-stu-id="080ea-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="080ea-113">SC</span><span class="sxs-lookup"><span data-stu-id="080ea-113">SC</span></span></p></td>
<td><p><span data-ttu-id="080ea-114">解体/廃棄</span><span class="sxs-lookup"><span data-stu-id="080ea-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="080ea-115">処分</span><span class="sxs-lookup"><span data-stu-id="080ea-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="080ea-116">DC</span><span class="sxs-lookup"><span data-stu-id="080ea-116">DC</span></span></p></td>
<td><p><span data-ttu-id="080ea-117">慈善活動に寄贈</span><span class="sxs-lookup"><span data-stu-id="080ea-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="080ea-118">処分</span><span class="sxs-lookup"><span data-stu-id="080ea-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="080ea-119">TD</span><span class="sxs-lookup"><span data-stu-id="080ea-119">TD</span></span></p></td>
<td><p><span data-ttu-id="080ea-120">サード パーティによる廃棄</span><span class="sxs-lookup"><span data-stu-id="080ea-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="080ea-121">処分</span><span class="sxs-lookup"><span data-stu-id="080ea-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="080ea-122">SL</span><span class="sxs-lookup"><span data-stu-id="080ea-122">SL</span></span></p></td>
<td><p><span data-ttu-id="080ea-123">回収</span><span class="sxs-lookup"><span data-stu-id="080ea-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="080ea-124">処分</span><span class="sxs-lookup"><span data-stu-id="080ea-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="080ea-125">TS</span><span class="sxs-lookup"><span data-stu-id="080ea-125">TS</span></span></p></td>
<td><p><span data-ttu-id="080ea-126">サード パーティへの売却 (二次市場)</span><span class="sxs-lookup"><span data-stu-id="080ea-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="080ea-127">修復/変更</span><span class="sxs-lookup"><span data-stu-id="080ea-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="080ea-128">RW</span><span class="sxs-lookup"><span data-stu-id="080ea-128">RW</span></span></p></td>
<td><p><span data-ttu-id="080ea-129">再加工</span><span class="sxs-lookup"><span data-stu-id="080ea-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="080ea-130">修復/変更</span><span class="sxs-lookup"><span data-stu-id="080ea-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="080ea-131">RF</span><span class="sxs-lookup"><span data-stu-id="080ea-131">RF</span></span></p></td>
<td><p><span data-ttu-id="080ea-132">再製品化/修繕</span><span class="sxs-lookup"><span data-stu-id="080ea-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="080ea-133">修復/変更</span><span class="sxs-lookup"><span data-stu-id="080ea-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="080ea-134">MD</span><span class="sxs-lookup"><span data-stu-id="080ea-134">MD</span></span></p></td>
<td><p><span data-ttu-id="080ea-135">変更</span><span class="sxs-lookup"><span data-stu-id="080ea-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="080ea-136">修復/変更</span><span class="sxs-lookup"><span data-stu-id="080ea-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="080ea-137">RP</span><span class="sxs-lookup"><span data-stu-id="080ea-137">RP</span></span></p></td>
<td><p><span data-ttu-id="080ea-138">修復</span><span class="sxs-lookup"><span data-stu-id="080ea-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="080ea-139">修復/変更</span><span class="sxs-lookup"><span data-stu-id="080ea-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="080ea-140">RV</span><span class="sxs-lookup"><span data-stu-id="080ea-140">RV</span></span></p></td>
<td><p><span data-ttu-id="080ea-141">仕入先に返品</span><span class="sxs-lookup"><span data-stu-id="080ea-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="080ea-142">その他</span><span class="sxs-lookup"><span data-stu-id="080ea-142">Other</span></span></p></td>
<td><p><span data-ttu-id="080ea-143">AI</span><span class="sxs-lookup"><span data-stu-id="080ea-143">AI</span></span></p></td>
<td><p><span data-ttu-id="080ea-144">現状のまま使用</span><span class="sxs-lookup"><span data-stu-id="080ea-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="080ea-145">その他</span><span class="sxs-lookup"><span data-stu-id="080ea-145">Other</span></span></p></td>
<td><p><span data-ttu-id="080ea-146">RS</span><span class="sxs-lookup"><span data-stu-id="080ea-146">RS</span></span></p></td>
<td><p><span data-ttu-id="080ea-147">再販売</span><span class="sxs-lookup"><span data-stu-id="080ea-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="080ea-148">その他</span><span class="sxs-lookup"><span data-stu-id="080ea-148">Other</span></span></p></td>
<td><p><span data-ttu-id="080ea-149">前</span><span class="sxs-lookup"><span data-stu-id="080ea-149">EX</span></span></p></td>
<td><p><span data-ttu-id="080ea-150">交換</span><span class="sxs-lookup"><span data-stu-id="080ea-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="080ea-151">その他</span><span class="sxs-lookup"><span data-stu-id="080ea-151">Other</span></span></p></td>
<td><p><span data-ttu-id="080ea-152">Ms.</span><span class="sxs-lookup"><span data-stu-id="080ea-152">MS</span></span></p></td>
<td><p><span data-ttu-id="080ea-153">雑費</span><span class="sxs-lookup"><span data-stu-id="080ea-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="080ea-154">定義した各廃棄コードごとに、処分アクションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="080ea-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="080ea-155">処分アクションにより、廃棄コードの物理的および財務的意味が決まります。</span><span class="sxs-lookup"><span data-stu-id="080ea-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="080ea-156">たとえば、交換品目を顧客に送る必要がある場合、処分アクションにより、返品品目の物理的な処理や返品品目の財務上の影響などが決まります。</span><span class="sxs-lookup"><span data-stu-id="080ea-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="080ea-157">業務のニーズに応じて廃棄コードの数を任意に定義できますが、6 種類の定義済の処分アクションのみ選択できます。</span><span class="sxs-lookup"><span data-stu-id="080ea-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="080ea-158">次の表に、処分アクションとその定義を示します。</span><span class="sxs-lookup"><span data-stu-id="080ea-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="080ea-159">処分アクション</span><span class="sxs-lookup"><span data-stu-id="080ea-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="080ea-160">説明</span><span class="sxs-lookup"><span data-stu-id="080ea-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="080ea-161"><strong>クレジット</strong></span><span class="sxs-lookup"><span data-stu-id="080ea-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="080ea-162">品目を在庫に返品し、顧客に対して貸方転記します。</span><span class="sxs-lookup"><span data-stu-id="080ea-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="080ea-163"><strong>貸方のみ</strong></span><span class="sxs-lookup"><span data-stu-id="080ea-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="080ea-164">品目の返品を要求または期待せずに、顧客に対して貸方転記します。</span><span class="sxs-lookup"><span data-stu-id="080ea-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="080ea-165"><strong>仕損</strong></span><span class="sxs-lookup"><span data-stu-id="080ea-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="080ea-166">品目を処分して、顧客に対して貸方転記します。</span><span class="sxs-lookup"><span data-stu-id="080ea-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="080ea-167"><strong>置換と貸方転記</strong></span><span class="sxs-lookup"><span data-stu-id="080ea-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="080ea-168">品目を在庫に戻して、交換注文を作成し、顧客に対して貸方転記します。</span><span class="sxs-lookup"><span data-stu-id="080ea-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="080ea-169"><strong>置換と仕損</strong></span><span class="sxs-lookup"><span data-stu-id="080ea-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="080ea-170">品目の処分し、交換注文を作成し、顧客に対して貸方転記します。</span><span class="sxs-lookup"><span data-stu-id="080ea-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="080ea-171"><strong>顧客に戻る</strong></span><span class="sxs-lookup"><span data-stu-id="080ea-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="080ea-172">品目の返品を拒否して、顧客に返送します。</span><span class="sxs-lookup"><span data-stu-id="080ea-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="080ea-173">検査指示の廃棄コードの選択</span><span class="sxs-lookup"><span data-stu-id="080ea-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="080ea-174">**在庫管理** \> **定期処理** \> **品質管理** \> **検査指示** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="080ea-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="080ea-175">既存の検査指示に対して、**概要** タブの **廃棄コード** フィールドからアクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="080ea-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="080ea-176">参照</span><span class="sxs-lookup"><span data-stu-id="080ea-176">See also</span></span>

<span data-ttu-id="080ea-177">[検査指示 (フォーム)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="080ea-177">[Quarantine order (form)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="080ea-178">[廃棄コード (フォーム)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="080ea-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]