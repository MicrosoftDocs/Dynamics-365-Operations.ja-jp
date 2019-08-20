---
title: 顧客からの先日付小切手の決済
description: 先日付小切手は、銀行で精算された後に決済できます。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 635a1c50390bca59cd1c9ba0cf0421c510b2998c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841852"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>顧客からの先日付小切手の決済

[!include [task guide banner](../../includes/task-guide-banner.md)]

先日付小切手は、銀行で精算された後に決済できます。 この財務トランザクションによって、先日付小切手のつなぎ勘定トランザクションも精算されます。 

こちらを始める前に、次のタスクを完了する必要があります。

1) 先日付小切手の設定

2) 顧客の先日付小切手の登録および転記 



このタスク ガイドのロールは会計登録者です。



この手順では、USMF というデモ会社を使用します。

1. [貸方転記および取立] > [照会およびレポート] > [支払] > [顧客の先日付小切手] の順に移動します。
2. [決済] をクリックします。
3. [清算項目の決済] をクリックします。
    * 小切手トランザクションの顧客 ID を決済します。  
4. ページを閉じます。
5. [総勘定元帳] > [総勘定元帳] > [仕訳入力] > [一般仕訳帳] の順に移動します。
6. [表示] フィールドで、オプションを選択します。
7. [作成ユーザーのみ表示] チェック ボックスをオンまたはオフにします。
8. 一覧で、目的のレコードを見つけ、選択します。
9. [行] をクリックします。
10. [伝票] をクリックします。
11. ページを閉じます。

