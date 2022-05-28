---
title: 仕訳帳からの関連する会社間伝票の表示
description: 一般仕訳帳から会社間トランザクションを転記する時、関連する伝票ウィンドウは相殺会社からの伝票を表示します。
author: aprilolson
ms.date: 05/5/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, SysDataAreaSelectLookup, LedgerTransVoucher, LedgerTransRelatedVouchers
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a2f226c9b784a687296157b995bebb761aae27b
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717281"
---
# <a name="view-related-intercompany-voucher-from-journal"></a>仕訳帳からの関連する会社間伝票の表示

[!include [banner](../../includes/banner.md)]

一般仕訳帳から会社間トランザクションを転記する時、関連する伝票ウィンドウは相殺会社からの伝票を表示します。


## <a name="post-an-intercompany-journal"></a>会社間仕訳帳の転記
1. **一般仕訳帳** に移動して **新規** をクリックします。
2. 一覧で、選択された行をマークします。
3. **名前** フィールドで、会社間の仕訳帳名を入力または選択します。
4. 一覧で **明細** をクリックして、選択した行をマークします。
5. **勘定** フィールドで、目的の値を指定します。
6. **説明** フィールドで、値を入力または選択します。
7. ページを閉じます。
8. **借方** フィールドに数値を入力します。
9. **相殺会社** フィールドで、相殺会社を入力または選択します。
10. **相殺勘定** フィールドで、任意の値を指定します。
11. **転記** をクリックします。

## <a name="view-related-intercompany-voucher"></a>関連する会社間伝票の表示
1. **伝票** をクリックします。
2. 下のリストで **関連する伝票** をクリックして選択した行をマークします。
3. **伝票** をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
