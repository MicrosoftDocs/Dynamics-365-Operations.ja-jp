--- 
title: "勘定科目間でのトランザクションの決済"
description: "この手順は、勘定科目間でトランザクションを決済する方法、また元帳決済をキャンセルする方法を示します。"
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97a28069f8d560c98099a667852c932ba7658996
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="settle-transactions-between-ledger-accounts"></a>勘定科目間でのトランザクションの決済

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順は、勘定科目間でトランザクションを決済する方法、また元帳決済をキャンセルする方法を示します。 この手順では、デモ データの会社 USMF を使用します。


## <a name="settle-transaction-between-ledger-accounts"></a>勘定科目間でのトランザクションの決済
1. [総勘定元帳] > [定期処理タスク] > [元帳決済] の順に移動します。
2. 一覧で、決済するトランザクションを見つけます。
    * 残額は 0 にする必要があります。  
3. [含む] をクリックします。
4. [承認] をクリックします。

## <a name="cancel-a-ledger-settlement"></a>元帳決済のキャンセル
1. ページを閉じます。
2. [総勘定元帳] > [照会およびレポート] > [試算表] の順に移動します。
3. [パラメーター] をクリックして、ドロップ ダイアログを開きます。
4. [更新] をクリックします。
5. 一覧で、トランザクションが決済した勘定を見つけます。
6. [すべてのトランザクション] をクリックします。
7. フィルターを使用すると、一覧内のトランザクションを簡単に見つけることができます。
8. [元帳決済] をクリックします。
9. 一覧で、選択された行をマークします。


