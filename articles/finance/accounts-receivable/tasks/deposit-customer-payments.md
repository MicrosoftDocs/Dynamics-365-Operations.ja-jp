---
title: 顧客支払の預金
description: 顧客支払を預金します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7357683e46df04c3dedd7e22607748512c9de94a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220254"
---
# <a name="deposit-customer-payments"></a>顧客支払の預金

[!include [banner](../../includes/banner.md)]

顧客支払を預金します。 このタスクでは、USMF というデモ会社を使用します。

1. **ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 支払 > 支払仕訳** の順に移動します。
2. **新規** を選択します。
3. **名前** フィールドで、ドロップダウン メニューの **CustPay** を選択します。
4. **明細行** を選択します。
5. **口座** フィールドで、支払を記録している顧客を選択します。
6. **貸方** フィールドに支払金額を入力します。 金額を空白にし、支払済み請求書を選択してシステムに計算させることができます。  
7. **支払参照** フィールドに値を入力します。 支払の参照は、入力する支払の小切手番号にすることができます。 預金伝票に支払を含めるためには、支払参照が必要となります。  
8. [預金伝票の使用] ボックスをマークします。 支払額を預金残高に含める場合、この設定を「はい」に変更します。  
9. **新規** を選択します。
10. **口座** フィールドで、次回に支払う顧客を選択します。
11. **貸方** フィールドに支払金額を入力します。
12. **支払参照** フィールドに値を入力します。
13. **預金伝票の使用** ボックスをマークします。
14. **投稿** を選択します。 預金伝票を生成する前に、支払は転記されなければなりません。 これは、預金伝票が生成された後に支払が変更しないようにするためです。  
15. **機能** を選択します。
16. **預金伝票** を選択します。
17. **OK** を選択します。 最初のページは預金伝票を作成するために使用されます。  
18. **OK** を選択します。 2 番目の手順は、預金伝票を印刷することですが、この手順は必須ではありません。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]