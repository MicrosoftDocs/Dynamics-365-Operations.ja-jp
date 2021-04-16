---
title: 承認仕訳帳を使用した買掛金勘定への請求書データの入力
description: このトピックでは、仕入帳を使用して請求書を作成した後、承認仕訳帳を使用して経費勘定を更新する方法について説明します。
author: abruer
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d01c04fcf707109cd7bc6f056846506914e96dec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838888"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>承認仕訳帳を使用した買掛金勘定への請求書データの入力

[!include [banner](../../includes/banner.md)]

このトピックでは、仕入帳を使用して請求書を作成した後、承認仕訳帳を使用して経費勘定を更新する方法について説明します。

## <a name="create-and-post-and-invoice"></a>請求書の作成と転記
1. ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 請求書 > 仕入帳** の順に移動します。
2. **新規** を選択します。
3. 使用する仕入帳の名前を選択します。
4. 登録を開いて経費明細行を入力するには、**明細行** を選択します。
5. 仕入先を選択してください。 たとえば、`US-104` を入力または選択します。
6. **請求書** フィールドに値を入力します。
7. **説明** フィールドで、値を入力します。
8. **貸方** フィールドに、数値を入力します。
9. **承認者** フィールドで、ドロップダウン メニューから承認者を選択します。
10. **投稿** を選択します。

## <a name="approve-an-invoice"></a>請求書の承認
1. ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 請求書 > 請求書の承認** の順に移動します。
2. **新規** を選択します。
3. 使用する請求書承認仕訳帳の名前を選択します。
4. **明細行** を選択すると、承認する請求書を選択できるページが表示されます。
5. **伝票の検索** を選択すると、承認待ちの請求書をすべて表示します。
6. 作成した請求書をマークし、**選択** をクリックします。 上の手順で選択した伝票は、選択後にこのリストに移動されます。  
7. **OK** を選択します。
8. 請求書に経費勘定を追加するには、**勘定番号** フィールドを選択します。
9. 勘定番号を入力し、Tab キーでこのフィールドから移動します。 たとえば、「`600120`」を入力します。
10. **投稿** を選択します。
11. 転記されたエントリを表示するには、**伝票** をクリックします。 承認保留中の請求書の勘定は、取消されて実際の経費勘定に置き換えられます。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]