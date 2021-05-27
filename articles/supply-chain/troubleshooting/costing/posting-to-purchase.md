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
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>金額が 0 の購買見越計上がゼロ価値製品入庫に対して転記される

KB 番号: 4612588

## <a name="symptoms"></a>現象

値が 0 の製品入庫が転記される場合、金額が 0 (ゼロ) の購買見越計上への転記が作成されます。

## <a name="resolution"></a>解像度

既定では、*購買見越計上* タイプの元帳転記の場合、サブ元帳トランザクションの `IsTransferredIndetail` フィールドは常に *集計* に設定されます。 したがって、金額が0 (ゼロ) の場合でも、関連する伝票エントリが作成されます。

金額が0 (ゼロ) の場合にこの転記タイプをスキップするには、次の例に示すように、`subledgerJournalizer.markDoNotTransferEntries` メソッドを拡張して `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` を含むようにします。

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
