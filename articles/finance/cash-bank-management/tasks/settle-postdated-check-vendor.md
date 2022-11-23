---
title: 仕入先の先日付小切手の決済
description: 銀行が期限切れの小切手をクリアして、その小切手トランザクションを精算してしまったときに、仕入先へ発行した先日付小切手を決済します。
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e3816a2f1c95d568a173cb07daad0473703da9c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779504"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>仕入先の先日付小切手の決済

[!include [banner](../../includes/banner.md)]

銀行が期限切れの小切手をクリアして、その小切手トランザクションを精算してしまったときに、仕入先へ発行した先日付小切手を決済します。 

これを始める前に、次の手順を完了します。

1) 先日付小切手の設定

2) 仕入先の先日付小切手の登録および転記



この手順のロールは会計登録者です。 この手順では、USMF というデモ会社を使用します。

1. **買掛金勘定 > 支払 > 仕入先の先日付小切手** へ移動します。
2. **決済** をクリックします。
3. **清算項目の決済** をクリックします。
    * 小切手トランザクションのための仕入先を決済します。  
4. ページを閉じます。
5. **総勘定元帳 > 仕訳入力 > 一般仕訳帳** の順に移動します。
6. **表示** フィールドで **すべて** を選択します。
7. **作成ユーザーのみ表示** チェック ボックスをオンまたはオフにします。
8. 一覧で、選択された行をマークします。
9. **行** をクリックします。
10. **伝票** をクリックします。
11. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
