---
title: 仕入先請求書の消費税の計算と調整
description: この記事では、Dynamics 365 Finance で、仕入先請求書の売上税を調整する方法について説明します。
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a1093631688351d065d6b55bc65055b6f92d256
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868376"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>仕入先請求書の消費税の計算と調整

[!include [banner](../../includes/banner.md)]

この記事では、仕入先請求書の売上税を調整する方法について説明します。 オリジナルの元伝票が計算と異なる税額を表示している場合、転記前にこれらの金額を調整できます。 このタスクでは、USMF というデモ会社を使用します。

1. **買掛金勘定 > 請求書 > 請求仕訳帳** の順に移動します。
2. **新規** を選択します。
3. 新しい行の **名前** フィールドで、ドロップダウン メニューのオプションを選択します。
4. アクション ウィンドウで、**明細行** を選択します。
5. **勘定** フィールドで、目的の値を指定します。
6. **請求書** フィールドに値を入力します。
7. **貸方** フィールドに、数値を入力します。
8. **相殺勘定** フィールドで、任意の値を指定します。
9. **売上税** を選択します。
10. **実際の売上税の合計金額** フィールドに、数値を入力します。
11. **調整** タブで、売上税コードごとに売上税金額を調整できます。
12. **計算上の金額から実績をリセット** を選択します。
13. **OK** を選択します。
14. **保存** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
