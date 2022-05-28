---
title: 元帳発生トランザクションの作成
description: このタスク ガイドでは、発生主義スキーマに基づく元帳計上トランザクションの生成について説明します。
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9aa546bea140fe29a97e4cda7a85f632b8cf3b0
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716610"
---
# <a name="create-ledger-accrual-transactions"></a>元帳発生トランザクションの作成

[!include [banner](../../includes/banner.md)]

このタスク ガイドでは、発生主義スキーマに基づく元帳計上トランザクションの生成について説明します。

1. **総勘定元帳 > 仕訳入力 > 一般仕訳帳** の順に移動します。
2. 一覧で、目的の仕訳帳を検索し選択するか、新しい仕訳帳を作成します。
3. クリックして、**仕訳帳バッチ番号** フィールドのリンク先を表示します。
4. 一覧で、選択された行をマークします。
5. **勘定** フィールドで、目的の値を指定します。
    * この例では、保険の経費を定義します。 これは定期的経費の金額になります。  
6. **説明** フィールドで、値を入力します。
7. **借方** フィールドに数値を入力します。
8. **相殺勘定** フィールドで、任意の値を指定します。
9. **機能** をクリックします。
10. **元帳計上** をクリックします。
11. **発生主義スキーマ ID** フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。
12. 一覧で、適用する発生主義スキーマを検索し選択します。
13. 一覧で、選択された行のリンクをクリックします。
14. **開始日** フィールドに日付を入力します。
15. **トランザクション** をクリックします。
16. ページを閉じます。
17. **OK** をクリックします。
18. **転記** をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
