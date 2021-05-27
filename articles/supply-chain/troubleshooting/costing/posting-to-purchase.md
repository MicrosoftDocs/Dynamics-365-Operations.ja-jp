---
title: 金額が 0 の購買見越計上がゼロ価値製品入庫に対して転記される
description: 値が 0 の製品入庫が転記される場合、金額が 0 (ゼロ) の購買見越計上への転記が作成されます。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026693"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="0ec76-103">金額が 0 の購買見越計上がゼロ価値製品入庫に対して転記される</span><span class="sxs-lookup"><span data-stu-id="0ec76-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="0ec76-104">KB 番号: 4612588</span><span class="sxs-lookup"><span data-stu-id="0ec76-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="0ec76-105">現象</span><span class="sxs-lookup"><span data-stu-id="0ec76-105">Symptoms</span></span>

<span data-ttu-id="0ec76-106">値が 0 の製品入庫が転記される場合、金額が 0 (ゼロ) の購買見越計上への転記が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0ec76-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="0ec76-107">解像度</span><span class="sxs-lookup"><span data-stu-id="0ec76-107">Resolution</span></span>

<span data-ttu-id="0ec76-108">既定では、*購買見越計上* タイプの元帳転記の場合、サブ元帳トランザクションの `IsTransferredIndetail` フィールドは常に *集計* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0ec76-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="0ec76-109">したがって、金額が0 (ゼロ) の場合でも、関連する伝票エントリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0ec76-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="0ec76-110">金額が0 (ゼロ) の場合にこの転記タイプをスキップするには、次の例に示すように、`subledgerJournalizer.markDoNotTransferEntries` メソッドを拡張して `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` を含むようにします。</span><span class="sxs-lookup"><span data-stu-id="0ec76-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
