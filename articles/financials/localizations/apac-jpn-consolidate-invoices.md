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
ms.search.scope: Core, Operations
ms.custom: 10314
ms.assetid: bd7255d9-0b0e-4372-8563-eaa559adbf24
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8041d91e72560e832ed6a0ee4b1507c7a02a364
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850724"
---
# <a name="consolidated-invoices-for-japan"></a><span data-ttu-id="10533-104">日本向け月次締め請求書</span><span class="sxs-lookup"><span data-stu-id="10533-104">Consolidated invoices for Japan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10533-105">日本では、支払の請求書は毎月統合されます。</span><span class="sxs-lookup"><span data-stu-id="10533-105">In Japan, invoices are consolidated each month for payment.</span></span> <span data-ttu-id="10533-106">この記事は、月次締め請求書に関する情報を提供し、請求金額および期日の計算方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="10533-106">This article provides information about consolidated invoices, and explains how the invoice amount and due date are calculated.</span></span>

<span data-ttu-id="10533-107">複数の仕入先請求書、発注書、購買返品および仕入仕訳帳を支払の仕入先の月次締め請求書に統合できます。</span><span class="sxs-lookup"><span data-stu-id="10533-107">You can consolidate several vendor invoices, purchase orders, purchase returns, and purchase journals into a consolidated vendor invoice for payment.</span></span> <span data-ttu-id="10533-108">個別の仕入先トランザクションの支払を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="10533-108">You don't have to issue payments for the separate vendor transactions.</span></span> <span data-ttu-id="10533-109">また、顧客請求書、販売注文、返品、および売上仕訳帳を顧客の月次締め請求書に統合して、顧客に送信できます。</span><span class="sxs-lookup"><span data-stu-id="10533-109">You can also consolidate customer invoices, sales orders, sales returns, and sales journals into a customer consolidated invoice that you can send to the customer.</span></span>

<span data-ttu-id="10533-110">同じ日に顧客または仕入先の複数の月次締め請求書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="10533-110">You can create two or more consolidated invoices on the same day for a customer or a vendor.</span></span> <span data-ttu-id="10533-111">顧客または仕入先の月次締め請求書を作成した後、仕入先に支払うか、顧客から支払を受け取り、支払金額の月次締め請求書を決済できます。</span><span class="sxs-lookup"><span data-stu-id="10533-111">After you create a consolidated invoice for a customer or a vendor, you can pay the vendor or receive payment from the customer, and settle the consolidated invoice for the amount of the payment.</span></span>

<span data-ttu-id="10533-112">次の計算が月次締め請求書に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="10533-112">The following calculations are performed for a consolidated invoice:</span></span>

-   <span data-ttu-id="10533-113">請求金額</span><span class="sxs-lookup"><span data-stu-id="10533-113">Invoice amount</span></span>
-   <span data-ttu-id="10533-114">期日</span><span class="sxs-lookup"><span data-stu-id="10533-114">Due date</span></span>

## <a name="calculating-the-invoice-amount-for-a-consolidated-invoice"></a><span data-ttu-id="10533-115">月次締め請求書の請求金額の計算</span><span class="sxs-lookup"><span data-stu-id="10533-115">Calculating the invoice amount for a consolidated invoice</span></span>
<span data-ttu-id="10533-116">**月次締め請求書**ページで月次締め請求書を作成および確認した後、次の金額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="10533-116">After you create and confirm a consolidated invoice on the **Consolidated invoice** page, the following amounts are calculated:</span></span>

-   <span data-ttu-id="10533-117">**前回の請求金額** – 前の連結期間の合計請求金額。</span><span class="sxs-lookup"><span data-stu-id="10533-117">**Previous invoice amount** – The total invoice amount for the previous consolidation period.</span></span>
-   <span data-ttu-id="10533-118">**以前に支払済の金額** – 前の連結期間に支払われた合計金額。</span><span class="sxs-lookup"><span data-stu-id="10533-118">**Previously paid amount** – The total amount that was paid for the previous consolidation period.</span></span>
-   <span data-ttu-id="10533-119">**調整金額** – 前回の連結期間に支払われた調整金額。</span><span class="sxs-lookup"><span data-stu-id="10533-119">**Adjustment amount** – The adjustment amount for the previous consolidation period.</span></span> <span data-ttu-id="10533-120">調整金額には現金割引、銀行手数料が含まれます。</span><span class="sxs-lookup"><span data-stu-id="10533-120">The adjustment amount includes cash discounts and bank charges.</span></span>
-   <span data-ttu-id="10533-121">**未払い金額** – 現在の連結期間の合計未払い金額。</span><span class="sxs-lookup"><span data-stu-id="10533-121">**Outstanding amount** – The total outstanding amount for the current consolidation period.</span></span> <span data-ttu-id="10533-122">未払い金額は次の式を使用して計算されます。前回の請求金額 - 支払高 - 調整金額</span><span class="sxs-lookup"><span data-stu-id="10533-122">The outstanding amount is calculated by using the following formula: Previous invoice amount – Paid amount – Adjustment amount</span></span>
-   <span data-ttu-id="10533-123">**締め期間中の請求金額** – 現在の月次締め請求書の合計請求金額。</span><span class="sxs-lookup"><span data-stu-id="10533-123">**Invoice amount during consolidation period** – The total invoice amount for the current consolidated invoice.</span></span> <span data-ttu-id="10533-124">この金額には売上税が含まれています。</span><span class="sxs-lookup"><span data-stu-id="10533-124">This amount includes the sales tax.</span></span>
-   <span data-ttu-id="10533-125">**合計請求金額** – 現在の請求書の新しい合計請求金額。</span><span class="sxs-lookup"><span data-stu-id="10533-125">**Total invoice amount** – The new total invoice amount for the current invoice.</span></span> <span data-ttu-id="10533-126">この金額は次の式を使用して計算されます。未払い金額 + 締め期間中の請求金額</span><span class="sxs-lookup"><span data-stu-id="10533-126">This amount is calculated by using the following formula: Outstanding amount + Invoice amount during consolidation period</span></span>

## <a name="calculating-the-due-date-for-a-consolidated-invoice"></a><span data-ttu-id="10533-127">月次締め請求書の期日の計算</span><span class="sxs-lookup"><span data-stu-id="10533-127">Calculating the due date for a consolidated invoice</span></span>
<span data-ttu-id="10533-128">請求書は、仕入先または顧客ごとに指定した月次締め日に基づいて、毎月統合されます。</span><span class="sxs-lookup"><span data-stu-id="10533-128">Invoices are consolidated each month, based on the consolidation day that you specify for each vendor or customer.</span></span> <span data-ttu-id="10533-129">月次締め日は、請求書を締め処理する日と期間、および支払期日を決定します。</span><span class="sxs-lookup"><span data-stu-id="10533-129">The consolidation day determines the day and period that invoices are consolidated for, and the date that payment is due.</span></span> <span data-ttu-id="10533-130">月の最終日が指定した月次締め日よりも前の日付になる場合、請求書は月の最後の営業日に締め処理されます。</span><span class="sxs-lookup"><span data-stu-id="10533-130">If the last day of the month falls on a date that is earlier than the consolidation day that you specify, the invoices are consolidated on the last business day of the month.</span></span> <span data-ttu-id="10533-131">したがって、月次締め日に対して 31 を指定し、現在の月が 31 日未満の場合は、請求書はその月の最後の営業日に締め処理されます。</span><span class="sxs-lookup"><span data-stu-id="10533-131">Therefore, if you specify 31 for the consolidation day, but the current month has fewer than 31 days, the invoices are consolidated on the last business day of that month.</span></span> <span data-ttu-id="10533-132">たとえば、2012 年 6 月の請求書は 2012 年 6 月 29 日に締め処理されます。その日が月の最後の営業日であるためです。</span><span class="sxs-lookup"><span data-stu-id="10533-132">For example, the invoices for June 2012 are consolidated on June 29, 2012, because that is the last business day of the month.</span></span> <span data-ttu-id="10533-133">さまざまな日に生成される請求書の支払期日の計算方法を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="10533-133">The following table shows how the payment due date is calculated for invoices that are generated on different days.</span></span> <span data-ttu-id="10533-134">月次締め日は 10 で、支払期日は月末です。</span><span class="sxs-lookup"><span data-stu-id="10533-134">The consolidation day is 10, and the payment date is the end of the month.</span></span>

| <span data-ttu-id="10533-135">請求書番号</span><span class="sxs-lookup"><span data-stu-id="10533-135">Invoice number</span></span> | <span data-ttu-id="10533-136">請求日</span><span class="sxs-lookup"><span data-stu-id="10533-136">Invoice date</span></span> | <span data-ttu-id="10533-137">月次締め日</span><span class="sxs-lookup"><span data-stu-id="10533-137">Consolidation day</span></span> | <span data-ttu-id="10533-138">期日</span><span class="sxs-lookup"><span data-stu-id="10533-138">Due date</span></span>      |
|----------------|--------------|-------------------|---------------|
| <span data-ttu-id="10533-139">請求書 001</span><span class="sxs-lookup"><span data-stu-id="10533-139">INV001</span></span>         | <span data-ttu-id="10533-140">2012 年 5 月 4 日</span><span class="sxs-lookup"><span data-stu-id="10533-140">May 4, 2012</span></span>  | <span data-ttu-id="10533-141">2012 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="10533-141">May 10, 2012</span></span>      | <span data-ttu-id="10533-142">2012 年 6 月 29 日</span><span class="sxs-lookup"><span data-stu-id="10533-142">June 29, 2012</span></span> |
| <span data-ttu-id="10533-143">請求書 002</span><span class="sxs-lookup"><span data-stu-id="10533-143">INV002</span></span>         | <span data-ttu-id="10533-144">2012 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="10533-144">May 10, 2012</span></span> | <span data-ttu-id="10533-145">2012 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="10533-145">May 10, 2012</span></span>      | <span data-ttu-id="10533-146">2012 年 6 月 29 日</span><span class="sxs-lookup"><span data-stu-id="10533-146">June 29, 2012</span></span> |
| <span data-ttu-id="10533-147">請求書 003</span><span class="sxs-lookup"><span data-stu-id="10533-147">INV003</span></span>         | <span data-ttu-id="10533-148">2012 年 5 月 18 日</span><span class="sxs-lookup"><span data-stu-id="10533-148">May 18, 2012</span></span> | <span data-ttu-id="10533-149">2012 年 6 月 10 日</span><span class="sxs-lookup"><span data-stu-id="10533-149">June 10, 2012</span></span>     | <span data-ttu-id="10533-150">2012 年 7 月 31 日</span><span class="sxs-lookup"><span data-stu-id="10533-150">July 31, 2012</span></span> |
| <span data-ttu-id="10533-151">請求書 004</span><span class="sxs-lookup"><span data-stu-id="10533-151">INV004</span></span>         | <span data-ttu-id="10533-152">2012 年 6 月 8 日</span><span class="sxs-lookup"><span data-stu-id="10533-152">June 8, 2012</span></span> | <span data-ttu-id="10533-153">2012 年 6 月 10 日</span><span class="sxs-lookup"><span data-stu-id="10533-153">June 10, 2012</span></span>     | <span data-ttu-id="10533-154">2012 年 7 月 31 日</span><span class="sxs-lookup"><span data-stu-id="10533-154">July 31, 2012</span></span> |





