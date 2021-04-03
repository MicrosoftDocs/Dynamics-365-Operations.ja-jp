---
title: 日本向け月次締め請求書
description: 日本では、支払の請求書は毎月統合されます。 この記事は、月次締め請求書に関する情報を提供し、請求金額および期日の計算方法を説明します。
author: yijialuan
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustConsInvoice_JP, VendConsInvoice_JP
audience: Application User
ms.reviewer: kfend
ms.custom: 10314
ms.assetid: bd7255d9-0b0e-4372-8563-eaa559adbf24
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7045af0c9dcf96424469d76ae2b332433c02db62
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258194"
---
# <a name="consolidated-invoices-for-japan"></a><span data-ttu-id="6ee6d-104">日本向け月次締め請求書</span><span class="sxs-lookup"><span data-stu-id="6ee6d-104">Consolidated invoices for Japan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ee6d-105">日本では、支払の請求書は毎月統合されます。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-105">In Japan, invoices are consolidated each month for payment.</span></span> <span data-ttu-id="6ee6d-106">この記事は、月次締め請求書に関する情報を提供し、請求金額および期日の計算方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-106">This article provides information about consolidated invoices, and explains how the invoice amount and due date are calculated.</span></span>

<span data-ttu-id="6ee6d-107">複数の仕入先請求書、発注書、購買返品および仕入仕訳帳を支払の仕入先の月次締め請求書に統合できます。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-107">You can consolidate several vendor invoices, purchase orders, purchase returns, and purchase journals into a consolidated vendor invoice for payment.</span></span> <span data-ttu-id="6ee6d-108">個別の仕入先トランザクションの支払を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-108">You don't have to issue payments for the separate vendor transactions.</span></span> <span data-ttu-id="6ee6d-109">また、顧客請求書、販売注文、返品、および売上仕訳帳を顧客の月次締め請求書に統合して、顧客に送信できます。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-109">You can also consolidate customer invoices, sales orders, sales returns, and sales journals into a customer consolidated invoice that you can send to the customer.</span></span>

<span data-ttu-id="6ee6d-110">同じ日に顧客または仕入先の複数の月次締め請求書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-110">You can create two or more consolidated invoices on the same day for a customer or a vendor.</span></span> <span data-ttu-id="6ee6d-111">顧客または仕入先の月次締め請求書を作成した後、仕入先に支払うか、顧客から支払を受け取り、支払金額の月次締め請求書を決済できます。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-111">After you create a consolidated invoice for a customer or a vendor, you can pay the vendor or receive payment from the customer, and settle the consolidated invoice for the amount of the payment.</span></span>

<span data-ttu-id="6ee6d-112">次の計算が月次締め請求書に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-112">The following calculations are performed for a consolidated invoice:</span></span>

-   <span data-ttu-id="6ee6d-113">請求金額</span><span class="sxs-lookup"><span data-stu-id="6ee6d-113">Invoice amount</span></span>
-   <span data-ttu-id="6ee6d-114">期日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-114">Due date</span></span>

## <a name="calculating-the-invoice-amount-for-a-consolidated-invoice"></a><span data-ttu-id="6ee6d-115">月次締め請求書の請求金額の計算</span><span class="sxs-lookup"><span data-stu-id="6ee6d-115">Calculating the invoice amount for a consolidated invoice</span></span>
<span data-ttu-id="6ee6d-116">**月次締め請求書** ページで月次締め請求書を作成および確認した後、次の金額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-116">After you create and confirm a consolidated invoice on the **Consolidated invoice** page, the following amounts are calculated:</span></span>

-   <span data-ttu-id="6ee6d-117">**前回の請求金額** – 前の連結期間の合計請求金額。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-117">**Previous invoice amount** – The total invoice amount for the previous consolidation period.</span></span>
-   <span data-ttu-id="6ee6d-118">**以前に支払済の金額** – 前の連結期間に支払われた合計金額。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-118">**Previously paid amount** – The total amount that was paid for the previous consolidation period.</span></span>
-   <span data-ttu-id="6ee6d-119">**調整金額** – 前回の連結期間に支払われた調整金額。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-119">**Adjustment amount** – The adjustment amount for the previous consolidation period.</span></span> <span data-ttu-id="6ee6d-120">調整金額には現金割引、銀行手数料が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-120">The adjustment amount includes cash discounts and bank charges.</span></span>
-   <span data-ttu-id="6ee6d-121">**未払い金額** – 現在の連結期間の合計未払い金額。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-121">**Outstanding amount** – The total outstanding amount for the current consolidation period.</span></span> <span data-ttu-id="6ee6d-122">未払い金額は次の式を使用して計算されます。前回の請求金額 - 支払高 - 調整金額</span><span class="sxs-lookup"><span data-stu-id="6ee6d-122">The outstanding amount is calculated by using the following formula: Previous invoice amount – Paid amount – Adjustment amount</span></span>
-   <span data-ttu-id="6ee6d-123">**締め期間中の請求金額** – 現在の月次締め請求書の合計請求金額。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-123">**Invoice amount during consolidation period** – The total invoice amount for the current consolidated invoice.</span></span> <span data-ttu-id="6ee6d-124">この金額には売上税が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-124">This amount includes the sales tax.</span></span>
-   <span data-ttu-id="6ee6d-125">**合計請求金額** – 現在の請求書の新しい合計請求金額。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-125">**Total invoice amount** – The new total invoice amount for the current invoice.</span></span> <span data-ttu-id="6ee6d-126">この金額は次の式を使用して計算されます。未払い金額 + 締め期間中の請求金額</span><span class="sxs-lookup"><span data-stu-id="6ee6d-126">This amount is calculated by using the following formula: Outstanding amount + Invoice amount during consolidation period</span></span>

## <a name="calculating-the-due-date-for-a-consolidated-invoice"></a><span data-ttu-id="6ee6d-127">月次締め請求書の期日の計算</span><span class="sxs-lookup"><span data-stu-id="6ee6d-127">Calculating the due date for a consolidated invoice</span></span>
<span data-ttu-id="6ee6d-128">請求書は、仕入先または顧客ごとに指定した月次締め日に基づいて、毎月統合されます。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-128">Invoices are consolidated each month, based on the consolidation day that you specify for each vendor or customer.</span></span> <span data-ttu-id="6ee6d-129">月次締め日は、請求書を締め処理する日と期間、および支払期日を決定します。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-129">The consolidation day determines the day and period that invoices are consolidated for, and the date that payment is due.</span></span> <span data-ttu-id="6ee6d-130">月の最終日が指定した月次締め日よりも前の日付になる場合、請求書は月の最後の営業日に締め処理されます。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-130">If the last day of the month falls on a date that is earlier than the consolidation day that you specify, the invoices are consolidated on the last business day of the month.</span></span> <span data-ttu-id="6ee6d-131">したがって、月次締め日に対して 31 を指定し、現在の月が 31 日未満の場合は、請求書はその月の最後の営業日に締め処理されます。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-131">Therefore, if you specify 31 for the consolidation day, but the current month has fewer than 31 days, the invoices are consolidated on the last business day of that month.</span></span> <span data-ttu-id="6ee6d-132">たとえば、2012 年 6 月の請求書は 2012 年 6 月 29 日に締め処理されます。その日が月の最後の営業日であるためです。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-132">For example, the invoices for June 2012 are consolidated on June 29, 2012, because that is the last business day of the month.</span></span> <span data-ttu-id="6ee6d-133">さまざまな日に生成される請求書の支払期日の計算方法を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-133">The following table shows how the payment due date is calculated for invoices that are generated on different days.</span></span> <span data-ttu-id="6ee6d-134">月次締め日は 10 で、支払期日は月末です。</span><span class="sxs-lookup"><span data-stu-id="6ee6d-134">The consolidation day is 10, and the payment date is the end of the month.</span></span>

| <span data-ttu-id="6ee6d-135">請求書番号</span><span class="sxs-lookup"><span data-stu-id="6ee6d-135">Invoice number</span></span> | <span data-ttu-id="6ee6d-136">請求日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-136">Invoice date</span></span> | <span data-ttu-id="6ee6d-137">月次締め日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-137">Consolidation day</span></span> | <span data-ttu-id="6ee6d-138">期日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-138">Due date</span></span>      |
|----------------|--------------|-------------------|---------------|
| <span data-ttu-id="6ee6d-139">請求書 001</span><span class="sxs-lookup"><span data-stu-id="6ee6d-139">INV001</span></span>         | <span data-ttu-id="6ee6d-140">2012 年 5 月 4 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-140">May 4, 2012</span></span>  | <span data-ttu-id="6ee6d-141">2012 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-141">May 10, 2012</span></span>      | <span data-ttu-id="6ee6d-142">2012 年 6 月 29 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-142">June 29, 2012</span></span> |
| <span data-ttu-id="6ee6d-143">請求書 002</span><span class="sxs-lookup"><span data-stu-id="6ee6d-143">INV002</span></span>         | <span data-ttu-id="6ee6d-144">2012 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-144">May 10, 2012</span></span> | <span data-ttu-id="6ee6d-145">2012 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-145">May 10, 2012</span></span>      | <span data-ttu-id="6ee6d-146">2012 年 6 月 29 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-146">June 29, 2012</span></span> |
| <span data-ttu-id="6ee6d-147">請求書 003</span><span class="sxs-lookup"><span data-stu-id="6ee6d-147">INV003</span></span>         | <span data-ttu-id="6ee6d-148">2012 年 5 月 18 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-148">May 18, 2012</span></span> | <span data-ttu-id="6ee6d-149">2012 年 6 月 10 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-149">June 10, 2012</span></span>     | <span data-ttu-id="6ee6d-150">2012 年 7 月 31 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-150">July 31, 2012</span></span> |
| <span data-ttu-id="6ee6d-151">請求書 004</span><span class="sxs-lookup"><span data-stu-id="6ee6d-151">INV004</span></span>         | <span data-ttu-id="6ee6d-152">2012 年 6 月 8 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-152">June 8, 2012</span></span> | <span data-ttu-id="6ee6d-153">2012 年 6 月 10 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-153">June 10, 2012</span></span>     | <span data-ttu-id="6ee6d-154">2012 年 7 月 31 日</span><span class="sxs-lookup"><span data-stu-id="6ee6d-154">July 31, 2012</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]