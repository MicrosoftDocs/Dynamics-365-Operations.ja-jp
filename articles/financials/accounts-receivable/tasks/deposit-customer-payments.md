--- 
title: "顧客支払の預金"
description: "顧客支払を預金します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dbf21bd5df70cd80e4fe3f2f5d699aa82b62423b
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="deposit-customer-payments"></a>顧客支払の預金

[!include [task guide banner](../../includes/task-guide-banner.md)]

顧客支払を預金します。 このタスクでは、USMF というデモ会社を使用します。

1. [売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 支払仕訳帳を選択します。 
5. [行] をクリックします。
6. [口座] フィールドで、支払を記録している顧客を選択します。
7. [貸方] フィールドに支払金額を入力します。
    * 金額を空白にし、支払済み請求書を選択してシステムに計算させることができます。  
8. [支払参照] フィールドに値を入力します。
    * 支払の参照は、入力する支払の小切手番号にすることができます。 預金伝票に支払を含めるためには、支払参照が必要となります。  
9. [預金伝票の使用] ボックスをマークします。
    * 支払額を預金残高に含める場合、この設定を「はい」に変更します。  
10. [新規] をクリックします。
11. [口座] フィールドで、次回に支払う顧客を選択します。
12. [貸方] フィールドに支払金額を入力します。
13. [支払参照] フィールドに値を入力します。
14. [預金伝票の使用] ボックスをマークします。
15. [転記] をクリックします。
    * 預金伝票を生成する前に、支払は転記されなければなりません。 これは、預金伝票が生成された後に支払が変更しないようにするためです。  
16. [機能] をクリックします。
17. [預金伝票] をクリックします。
18. [OK] をクリックします。
    * 最初のページは預金伝票を作成するために使用されます。  
19. [OK] をクリックします。
    * 2 番目の手順は、預金伝票を印刷することですが、この手順は必須ではありません。  


