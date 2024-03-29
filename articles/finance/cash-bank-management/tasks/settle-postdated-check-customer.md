---
title: 顧客からの先日付小切手の決済
description: 先日付小切手は、銀行で精算された後に決済できます。
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e61ac6d6785dd0383d5e5dcaca4cc55bf6deb52
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780018"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>顧客からの先日付小切手の決済

[!include [banner](../../includes/banner.md)]

先日付小切手は、銀行で精算された後に決済できます。 この財務トランザクションによって、先日付小切手のつなぎ勘定トランザクションも精算されます。 

こちらを始める前に、次のタスクを完了する必要があります。

1) 先日付小切手の設定

2) 顧客の先日付小切手の登録および転記 



このタスク ガイドのロールは会計登録者です。



この手順では、USMF というデモ会社を使用します。

1. **貸方転記および取立 > 照会およびレポート > 支払 > 顧客の先日付小切手** の順に移動します。
2. **決済** をクリックします。
3. **清算項目の決済** をクリックします。
    * 小切手トランザクションの顧客 ID を決済します。  
4. ページを閉じます。
5. **総勘定元帳 > 仕訳入力 > 一般仕訳帳** の順に移動します。
6. **表示** フィールドで、オプションを選択します。
7. **作成ユーザーのみ表示** チェック ボックスをオンまたはオフにします。
8. 一覧で、目的のレコードを見つけ、選択します。
9. **行** をクリックします。
10. **伝票** をクリックします。
11. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
