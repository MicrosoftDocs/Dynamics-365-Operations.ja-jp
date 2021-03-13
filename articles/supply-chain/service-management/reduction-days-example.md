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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 509d1a9e2abd79938376209d8feab1b935394833
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010525"
---
# <a name="reduction-days-example"></a><span data-ttu-id="be148-103">下方修正日数の例</span><span class="sxs-lookup"><span data-stu-id="be148-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="be148-104">次の表に示すように、顧客のメンテナンス定期売買の定期売買トランザクションを作成しました。</span><span class="sxs-lookup"><span data-stu-id="be148-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="be148-105">開始日</span><span class="sxs-lookup"><span data-stu-id="be148-105">From date</span></span></p></th>
<th><p><span data-ttu-id="be148-106">終了日</span><span class="sxs-lookup"><span data-stu-id="be148-106">To date</span></span></p></th>
<th><p><span data-ttu-id="be148-107">定期売買</span><span class="sxs-lookup"><span data-stu-id="be148-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="be148-108">定期売買タイプ</span><span class="sxs-lookup"><span data-stu-id="be148-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="be148-109">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="be148-109">Project</span></span></p></th>
<th><p><span data-ttu-id="be148-110">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="be148-110">Category</span></span></p></th>
<th><p><span data-ttu-id="be148-111">販売通貨</span><span class="sxs-lookup"><span data-stu-id="be148-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="be148-112">販売価格</span><span class="sxs-lookup"><span data-stu-id="be148-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be148-113">2011 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="be148-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="be148-114">2011 年 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="be148-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="be148-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="be148-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="be148-116"><strong>通常</strong></span><span class="sxs-lookup"><span data-stu-id="be148-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="be148-117">9013</span><span class="sxs-lookup"><span data-stu-id="be148-117">9013</span></span></p></td>
<td><p><span data-ttu-id="be148-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="be148-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="be148-119">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="be148-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="be148-120">200.00</span><span class="sxs-lookup"><span data-stu-id="be148-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be148-121">顧客から、2 日間 (3 月 10 日と 3 月 11 日) のサービスは不要だという報告が出されます。</span><span class="sxs-lookup"><span data-stu-id="be148-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="be148-122">そこで、これら 2 日分の定期売買を削減することに合意します。</span><span class="sxs-lookup"><span data-stu-id="be148-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="be148-123">**下方修正日数** タイプの新しいトランザクションを、次の表に示すように作成します。</span><span class="sxs-lookup"><span data-stu-id="be148-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="be148-124">自</span><span class="sxs-lookup"><span data-stu-id="be148-124">From date</span></span></p></th>
<th><p><span data-ttu-id="be148-125">至</span><span class="sxs-lookup"><span data-stu-id="be148-125">To date</span></span></p></th>
<th><p><span data-ttu-id="be148-126">定期売買</span><span class="sxs-lookup"><span data-stu-id="be148-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="be148-127">定期売買タイプ</span><span class="sxs-lookup"><span data-stu-id="be148-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="be148-128">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="be148-128">Project</span></span></p></th>
<th><p><span data-ttu-id="be148-129">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="be148-129">Category</span></span></p></th>
<th><p><span data-ttu-id="be148-130">販売通貨</span><span class="sxs-lookup"><span data-stu-id="be148-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="be148-131">販売価格</span><span class="sxs-lookup"><span data-stu-id="be148-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be148-132">2011 年 3 月 10 日</span><span class="sxs-lookup"><span data-stu-id="be148-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="be148-133">2011 年 3 月 11 日</span><span class="sxs-lookup"><span data-stu-id="be148-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="be148-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="be148-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="be148-135"><strong>下方修正日数</strong></span><span class="sxs-lookup"><span data-stu-id="be148-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="be148-136">9013</span><span class="sxs-lookup"><span data-stu-id="be148-136">9013</span></span></p></td>
<td><p><span data-ttu-id="be148-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="be148-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="be148-138">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="be148-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="be148-139">-12.90</span><span class="sxs-lookup"><span data-stu-id="be148-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be148-140">20011 年 3 月のトランザクションが請求されるとき、販売価格 EUR 200 から EUR 12.90 が減算されます。</span><span class="sxs-lookup"><span data-stu-id="be148-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="be148-141">したがって定期売買トランザクションの請求可能金額は EUR 187.10 となり、2 つのトランザクションは合計 EUR 187.10 で請求されます。</span><span class="sxs-lookup"><span data-stu-id="be148-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="be148-142">参照</span><span class="sxs-lookup"><span data-stu-id="be148-142">See also</span></span>

[<span data-ttu-id="be148-143">定期売買手数料の日数の引き下げ</span><span class="sxs-lookup"><span data-stu-id="be148-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


