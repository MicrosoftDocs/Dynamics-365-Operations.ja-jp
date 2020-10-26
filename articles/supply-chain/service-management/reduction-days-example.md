---
title: 下方修正日数の例
description: 下方修正日数の例です。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87c46cd7ee7410e1c7cb88868cd19f5075482f8c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975659"
---
# <a name="reduction-days-example"></a><span data-ttu-id="d8425-103">下方修正日数の例</span><span class="sxs-lookup"><span data-stu-id="d8425-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d8425-104">次の表に示すように、顧客のメンテナンス定期売買の定期売買トランザクションを作成しました。</span><span class="sxs-lookup"><span data-stu-id="d8425-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8425-105">開始日</span><span class="sxs-lookup"><span data-stu-id="d8425-105">From date</span></span></p></th>
<th><p><span data-ttu-id="d8425-106">終了日</span><span class="sxs-lookup"><span data-stu-id="d8425-106">To date</span></span></p></th>
<th><p><span data-ttu-id="d8425-107">定期売買</span><span class="sxs-lookup"><span data-stu-id="d8425-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d8425-108">定期売買タイプ</span><span class="sxs-lookup"><span data-stu-id="d8425-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="d8425-109">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="d8425-109">Project</span></span></p></th>
<th><p><span data-ttu-id="d8425-110">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="d8425-110">Category</span></span></p></th>
<th><p><span data-ttu-id="d8425-111">販売通貨</span><span class="sxs-lookup"><span data-stu-id="d8425-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d8425-112">販売価格</span><span class="sxs-lookup"><span data-stu-id="d8425-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8425-113">2011 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="d8425-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="d8425-114">2011 年 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d8425-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="d8425-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="d8425-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="d8425-116"><strong>通常</strong></span><span class="sxs-lookup"><span data-stu-id="d8425-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="d8425-117">9013</span><span class="sxs-lookup"><span data-stu-id="d8425-117">9013</span></span></p></td>
<td><p><span data-ttu-id="d8425-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="d8425-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d8425-119">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="d8425-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="d8425-120">200.00</span><span class="sxs-lookup"><span data-stu-id="d8425-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d8425-121">顧客から、2 日間 (3 月 10 日と 3 月 11 日) のサービスは不要だという報告が出されます。</span><span class="sxs-lookup"><span data-stu-id="d8425-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="d8425-122">そこで、これら 2 日分の定期売買を削減することに合意します。</span><span class="sxs-lookup"><span data-stu-id="d8425-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="d8425-123">**下方修正日数**タイプの新しいトランザクションを、次の表に示すように作成します。</span><span class="sxs-lookup"><span data-stu-id="d8425-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8425-124">自</span><span class="sxs-lookup"><span data-stu-id="d8425-124">From date</span></span></p></th>
<th><p><span data-ttu-id="d8425-125">至</span><span class="sxs-lookup"><span data-stu-id="d8425-125">To date</span></span></p></th>
<th><p><span data-ttu-id="d8425-126">定期売買</span><span class="sxs-lookup"><span data-stu-id="d8425-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d8425-127">定期売買タイプ</span><span class="sxs-lookup"><span data-stu-id="d8425-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="d8425-128">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="d8425-128">Project</span></span></p></th>
<th><p><span data-ttu-id="d8425-129">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="d8425-129">Category</span></span></p></th>
<th><p><span data-ttu-id="d8425-130">販売通貨</span><span class="sxs-lookup"><span data-stu-id="d8425-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d8425-131">販売価格</span><span class="sxs-lookup"><span data-stu-id="d8425-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8425-132">2011 年 3 月 10 日</span><span class="sxs-lookup"><span data-stu-id="d8425-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="d8425-133">2011 年 3 月 11 日</span><span class="sxs-lookup"><span data-stu-id="d8425-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="d8425-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="d8425-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="d8425-135"><strong>下方修正日数</strong></span><span class="sxs-lookup"><span data-stu-id="d8425-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="d8425-136">9013</span><span class="sxs-lookup"><span data-stu-id="d8425-136">9013</span></span></p></td>
<td><p><span data-ttu-id="d8425-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="d8425-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d8425-138">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="d8425-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="d8425-139">-12.90</span><span class="sxs-lookup"><span data-stu-id="d8425-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d8425-140">20011 年 3 月のトランザクションが請求されるとき、販売価格 EUR 200 から EUR 12.90 が減算されます。</span><span class="sxs-lookup"><span data-stu-id="d8425-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="d8425-141">したがって定期売買トランザクションの請求可能金額は EUR 187.10 となり、2 つのトランザクションは合計 EUR 187.10 で請求されます。</span><span class="sxs-lookup"><span data-stu-id="d8425-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8425-142">参照</span><span class="sxs-lookup"><span data-stu-id="d8425-142">See also</span></span>

[<span data-ttu-id="d8425-143">定期売買手数料の日数の引き下げ</span><span class="sxs-lookup"><span data-stu-id="d8425-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


