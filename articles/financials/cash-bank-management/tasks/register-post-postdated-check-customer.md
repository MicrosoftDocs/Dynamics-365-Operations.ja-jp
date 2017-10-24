--- 
title: "顧客の先日付小切手の登録および転記"
description: "顧客から受け取った先日付小切手の詳細を登録できます。"
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1610036815349f625a67d5dd67260114d42fff97
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a>顧客の先日付小切手の登録および転記

[!include[task guide banner](../../includes/task-guide-banner.md)]

顧客から受け取った先日付小切手の詳細を登録できます。 先日付小切手を転記して財務トランザクションを生成することもできます。   顧客から受け取った先日付小切手を登録および転記する前に、次のタスクを完了します。• [現金および銀行管理] ページで、先日付小切手を設定する • 先日小切手用の支払方法を設定する。この手順のロールは会計登録者です。 この手順では、USMF というデモ会社を使用します。

1. [売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [明細行] をクリックします。
5. 一覧で、選択された行をマークします。
6. [勘定] フィールドで、任意の値を指定します。
7. [貸方] フィールドに数値を入力します。
    * 先日付小切手に指定された金額を入力します。  
8. [支払] タブをクリックします。
9. [支払方法] フィールドに値を入力します。
    * 先日付小切手に対する支払方法を選択します。  
10. [先日付小切手] タブをクリックします。
11. [振出日] フィールドに、日付を入力します。
    * 先日付小切手が支払期限になる日付を入力します。  
12. [発行銀行支店] フィールドに、値を入力します。
    * 先日付小切手の銀行詳細を入力します。  
13. [小切手番号] フィールドに値を入力します。
14. [発行銀行名] フィールドに、値を入力します。
    * 先日付小切手の銀行詳細を入力します。  
15. [転記] をクリックします。
16. ページを閉じます。


