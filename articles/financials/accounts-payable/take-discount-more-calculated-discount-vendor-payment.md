---
title: "仕入先支払の計算済割引より大幅な割引を行う"
description: "この記事は、請求書で最初に使用できた割引を超えた金額の現金割引を行うシナリオについて説明します。 このシナリオは、組織が請求書の減額した金額を支払う契約を仕入先とした場合に発生することがあります。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 757a917311a9c0f1226a452e9fb59e05018f1635
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="4f8f7-104">仕入先支払の計算済割引より大幅な割引を行う</span><span class="sxs-lookup"><span data-stu-id="4f8f7-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="4f8f7-105">この記事は、請求書で最初に使用できた割引を超えた金額の現金割引を行うシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4f8f7-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="4f8f7-106">このシナリオは、組織が請求書の減額した金額を支払う契約を仕入先とした場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="4f8f7-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="4f8f7-107">請求書が 7 日以内に支払われた場合に、仕入先 3051 が Fabrikam に 4 パーセントの現金割引を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f8f7-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="4f8f7-108">6 月 29 日に、April は 1,000.00 ドルの請求書を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f8f7-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="4f8f7-109">仕入先は、April が請求書に対して既定の 40.00 ドルの割引の代わりに 60.00 ドルの割引を受けるようにします。</span><span class="sxs-lookup"><span data-stu-id="4f8f7-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="4f8f7-110">April は、買掛金勘定支払仕訳帳を使用して 1 回限りの支払を記録します。</span><span class="sxs-lookup"><span data-stu-id="4f8f7-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="4f8f7-111">彼女は支払の仕入先を入力し、[**トランザクションの決済**] ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="4f8f7-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="4f8f7-112">さらに、請求書にマークしたり、[**現金割引金額**] フィールドの値を **-60.00** に変更したりします。</span><span class="sxs-lookup"><span data-stu-id="4f8f7-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="4f8f7-113">マーク</span><span class="sxs-lookup"><span data-stu-id="4f8f7-113">Mark</span></span>     | <span data-ttu-id="4f8f7-114">現金割引の使用</span><span class="sxs-lookup"><span data-stu-id="4f8f7-114">Use cash discount</span></span> | <span data-ttu-id="4f8f7-115">伝票番号</span><span class="sxs-lookup"><span data-stu-id="4f8f7-115">Voucher</span></span>   | <span data-ttu-id="4f8f7-116">口座</span><span class="sxs-lookup"><span data-stu-id="4f8f7-116">Account</span></span> | <span data-ttu-id="4f8f7-117">日</span><span class="sxs-lookup"><span data-stu-id="4f8f7-117">Date</span></span>      | <span data-ttu-id="4f8f7-118">期日</span><span class="sxs-lookup"><span data-stu-id="4f8f7-118">Due date</span></span>  | <span data-ttu-id="4f8f7-119">請求書</span><span class="sxs-lookup"><span data-stu-id="4f8f7-119">Invoice</span></span> | <span data-ttu-id="4f8f7-120">トランザクション通貨の金額</span><span class="sxs-lookup"><span data-stu-id="4f8f7-120">Amount in transaction currency</span></span> | <span data-ttu-id="4f8f7-121">通貨</span><span class="sxs-lookup"><span data-stu-id="4f8f7-121">Currency</span></span> | <span data-ttu-id="4f8f7-122">決済金額</span><span class="sxs-lookup"><span data-stu-id="4f8f7-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="4f8f7-123">選択済</span><span class="sxs-lookup"><span data-stu-id="4f8f7-123">Selected</span></span> | <span data-ttu-id="4f8f7-124">標準</span><span class="sxs-lookup"><span data-stu-id="4f8f7-124">Normal</span></span>            | <span data-ttu-id="4f8f7-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="4f8f7-125">Inv-10040</span></span> | <span data-ttu-id="4f8f7-126">3051</span><span class="sxs-lookup"><span data-stu-id="4f8f7-126">3051</span></span>    | <span data-ttu-id="4f8f7-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="4f8f7-127">6/29/2015</span></span> | <span data-ttu-id="4f8f7-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="4f8f7-128">7/29/2015</span></span> | <span data-ttu-id="4f8f7-129">10040</span><span class="sxs-lookup"><span data-stu-id="4f8f7-129">10040</span></span>   | <span data-ttu-id="4f8f7-130">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4f8f7-130">1,000.00</span></span>                       | <span data-ttu-id="4f8f7-131">USD</span><span class="sxs-lookup"><span data-stu-id="4f8f7-131">USD</span></span>      | <span data-ttu-id="4f8f7-132">940.00</span><span class="sxs-lookup"><span data-stu-id="4f8f7-132">940.00</span></span>           |

<span data-ttu-id="4f8f7-133">割引の情報は [**トランザクションの決済**] ページの下部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="4f8f7-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="4f8f7-134">現金割引日</span><span class="sxs-lookup"><span data-stu-id="4f8f7-134">Cash discount date</span></span>           | <span data-ttu-id="4f8f7-135">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="4f8f7-135">7/12/2015</span></span> |
| <span data-ttu-id="4f8f7-136">現金割引金額</span><span class="sxs-lookup"><span data-stu-id="4f8f7-136">Cash discount amount</span></span>         | <span data-ttu-id="4f8f7-137">60.00</span><span class="sxs-lookup"><span data-stu-id="4f8f7-137">60.00</span></span>     |
| <span data-ttu-id="4f8f7-138">現金割引の使用</span><span class="sxs-lookup"><span data-stu-id="4f8f7-138">Use cash discount</span></span>            | <span data-ttu-id="4f8f7-139">標準</span><span class="sxs-lookup"><span data-stu-id="4f8f7-139">Normal</span></span>    |
| <span data-ttu-id="4f8f7-140">適用される現金割引</span><span class="sxs-lookup"><span data-stu-id="4f8f7-140">Cash discount taken</span></span>          | <span data-ttu-id="4f8f7-141">0.00</span><span class="sxs-lookup"><span data-stu-id="4f8f7-141">0.00</span></span>      |
| <span data-ttu-id="4f8f7-142">適用する現金割引金額</span><span class="sxs-lookup"><span data-stu-id="4f8f7-142">Cash discount amount to take</span></span> | <span data-ttu-id="4f8f7-143">60.00</span><span class="sxs-lookup"><span data-stu-id="4f8f7-143">60.00</span></span>     |

<span data-ttu-id="4f8f7-144">April は支払仕訳帳を転記します。</span><span class="sxs-lookup"><span data-stu-id="4f8f7-144">April posts the payment journal.</span></span> <span data-ttu-id="4f8f7-145">940.00 ドルの支払と 60.00 ドルの割引で請求書を完済します。</span><span class="sxs-lookup"><span data-stu-id="4f8f7-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>




