---
title: 勘定科目間でのトランザクションの決済
description: この手順は、勘定科目間でトランザクションを決済する方法、また元帳決済をキャンセルする方法を示します。
author: aprilolson
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a871e379826626edbad2434b11281fce5e29e14e
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717309"
---
# <a name="settle-transactions-between-ledger-accounts"></a>勘定科目間でのトランザクションの決済

[!include [banner](../../includes/banner.md)]

この手順は、勘定科目間でトランザクションを決済する方法、また元帳決済をキャンセルする方法を示します。 この手順では、デモ データの会社 USMF を使用します。


## <a name="settle-transaction-between-ledger-accounts"></a>勘定科目間でのトランザクションの決済
1. **一般会計 > 定期処理タスク > 元帳決済** の順に移動します。
2. 一覧で、決済するトランザクションを見つけます。
   > [!NOTE]
   > 残額は 0 にする必要があります。  
3. **含む** をクリックします。
4. **承認** をクリックします。

## <a name="cancel-a-ledger-settlement"></a>元帳決済のキャンセル

1. **一般会計 > 照会およびレポート > 試算表** の順に移動します。
2. **パラメーター** をクリックして、ドロップ ダイアログを開きます。
3. **更新** をクリックします。
4. 一覧で、トランザクションが決済した勘定を見つけます。
5. **すべてのトランザクション** をクリックします。
6. フィルターを使用すると、一覧内のトランザクションを簡単に見つけることができます。
7. **元帳決済** をクリックします。
8. 一覧で、選択された行をマークします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
