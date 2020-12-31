---
title: 仕入先支払の計算済割引より大幅な割引を行う
description: この記事は、請求書で最初に使用できた割引を超えた金額の現金割引を行うシナリオについて説明します。 このシナリオは、組織が請求書の減額した金額を支払う契約を仕入先とした場合に発生することがあります。
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b84b3d6ef1a86d8174823345a5ee9181c701c151
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445027"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="e6445-104">仕入先支払の計算済割引より大幅な割引を行う</span><span class="sxs-lookup"><span data-stu-id="e6445-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6445-105">この記事は、請求書で最初に使用できた割引を超えた金額の現金割引を行うシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e6445-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="e6445-106">このシナリオは、組織が請求書の減額した金額を支払う契約を仕入先とした場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="e6445-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="e6445-107">請求書が 7 日以内に支払われた場合に、仕入先 3051 が Fabrikam に 4 パーセントの現金割引を提供します。</span><span class="sxs-lookup"><span data-stu-id="e6445-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="e6445-108">6 月 29 日に、April は 1,000.00 ドルの請求書を入力します。</span><span class="sxs-lookup"><span data-stu-id="e6445-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="e6445-109">仕入先は、April が請求書に対して既定の 40.00 ドルの割引の代わりに 60.00 ドルの割引を受けるようにします。</span><span class="sxs-lookup"><span data-stu-id="e6445-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="e6445-110">April は、買掛金勘定支払仕訳帳を使用して 1 回限りの支払を記録します。</span><span class="sxs-lookup"><span data-stu-id="e6445-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="e6445-111">彼女は支払の仕入先を入力し、**トランザクションの決済** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="e6445-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="e6445-112">さらに、請求書にマークしたり、**現金割引金額** フィールドの値を **-60.00** に変更したりします。</span><span class="sxs-lookup"><span data-stu-id="e6445-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="e6445-113">マーク</span><span class="sxs-lookup"><span data-stu-id="e6445-113">Mark</span></span>     | <span data-ttu-id="e6445-114">現金割引の使用</span><span class="sxs-lookup"><span data-stu-id="e6445-114">Use cash discount</span></span> | <span data-ttu-id="e6445-115">伝票番号</span><span class="sxs-lookup"><span data-stu-id="e6445-115">Voucher</span></span>   | <span data-ttu-id="e6445-116">口座</span><span class="sxs-lookup"><span data-stu-id="e6445-116">Account</span></span> | <span data-ttu-id="e6445-117">日</span><span class="sxs-lookup"><span data-stu-id="e6445-117">Date</span></span>      | <span data-ttu-id="e6445-118">期日</span><span class="sxs-lookup"><span data-stu-id="e6445-118">Due date</span></span>  | <span data-ttu-id="e6445-119">請求書</span><span class="sxs-lookup"><span data-stu-id="e6445-119">Invoice</span></span> | <span data-ttu-id="e6445-120">トランザクション通貨の金額</span><span class="sxs-lookup"><span data-stu-id="e6445-120">Amount in transaction currency</span></span> | <span data-ttu-id="e6445-121">通貨</span><span class="sxs-lookup"><span data-stu-id="e6445-121">Currency</span></span> | <span data-ttu-id="e6445-122">決済金額</span><span class="sxs-lookup"><span data-stu-id="e6445-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="e6445-123">選択済</span><span class="sxs-lookup"><span data-stu-id="e6445-123">Selected</span></span> | <span data-ttu-id="e6445-124">標準</span><span class="sxs-lookup"><span data-stu-id="e6445-124">Normal</span></span>            | <span data-ttu-id="e6445-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="e6445-125">Inv-10040</span></span> | <span data-ttu-id="e6445-126">3051</span><span class="sxs-lookup"><span data-stu-id="e6445-126">3051</span></span>    | <span data-ttu-id="e6445-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="e6445-127">6/29/2015</span></span> | <span data-ttu-id="e6445-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="e6445-128">7/29/2015</span></span> | <span data-ttu-id="e6445-129">10040</span><span class="sxs-lookup"><span data-stu-id="e6445-129">10040</span></span>   | <span data-ttu-id="e6445-130">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e6445-130">1,000.00</span></span>                       | <span data-ttu-id="e6445-131">USD</span><span class="sxs-lookup"><span data-stu-id="e6445-131">USD</span></span>      | <span data-ttu-id="e6445-132">940.00</span><span class="sxs-lookup"><span data-stu-id="e6445-132">940.00</span></span>           |

<span data-ttu-id="e6445-133">割引の情報は **トランザクションの決済** ページの下部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6445-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="e6445-134">現金割引日</span><span class="sxs-lookup"><span data-stu-id="e6445-134">Cash discount date</span></span>           | <span data-ttu-id="e6445-135">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="e6445-135">7/12/2015</span></span> |
| <span data-ttu-id="e6445-136">現金割引金額</span><span class="sxs-lookup"><span data-stu-id="e6445-136">Cash discount amount</span></span>         | <span data-ttu-id="e6445-137">60.00</span><span class="sxs-lookup"><span data-stu-id="e6445-137">60.00</span></span>     |
| <span data-ttu-id="e6445-138">現金割引の使用</span><span class="sxs-lookup"><span data-stu-id="e6445-138">Use cash discount</span></span>            | <span data-ttu-id="e6445-139">標準</span><span class="sxs-lookup"><span data-stu-id="e6445-139">Normal</span></span>    |
| <span data-ttu-id="e6445-140">適用される現金割引</span><span class="sxs-lookup"><span data-stu-id="e6445-140">Cash discount taken</span></span>          | <span data-ttu-id="e6445-141">0.00</span><span class="sxs-lookup"><span data-stu-id="e6445-141">0.00</span></span>      |
| <span data-ttu-id="e6445-142">適用する現金割引金額</span><span class="sxs-lookup"><span data-stu-id="e6445-142">Cash discount amount to take</span></span> | <span data-ttu-id="e6445-143">60.00</span><span class="sxs-lookup"><span data-stu-id="e6445-143">60.00</span></span>     |

<span data-ttu-id="e6445-144">April は支払仕訳帳を転記します。</span><span class="sxs-lookup"><span data-stu-id="e6445-144">April posts the payment journal.</span></span> <span data-ttu-id="e6445-145">940.00 ドルの支払と 60.00 ドルの割引で請求書を完済します。</span><span class="sxs-lookup"><span data-stu-id="e6445-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



