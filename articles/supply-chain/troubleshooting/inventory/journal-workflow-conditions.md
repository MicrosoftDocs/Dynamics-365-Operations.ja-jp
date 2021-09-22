---
title: 在庫仕訳帳ワークフロー条件は、行レベルではなく仕訳帳レベルに適用される
description: 在庫仕訳帳ワークフロー条件は、行レベルではなく仕訳帳レベルにのみ適用されます。
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476875"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>在庫仕訳帳ワークフロー条件は、行レベルではなく仕訳帳レベルに適用される

## <a name="symptoms"></a>現象

たとえば、原価金額に対して在庫仕訳帳のワークフロー条件を設定しようとする場合に、この問題が発生する可能性があります。 この条件を設定して、原価金額が 100 未満の場合にのみ手順 1 が実行されます。 その後他の条件を設定して、原価金額が 100 以上の場合にのみ手順 2 が実行されます。 その後、ワークフローを実行するとワークフロー履歴に表示される行は 1 行のみです。送信された値に関係なく、常に最初の条件が *真* として評価されます。

## <a name="workaround"></a>回避策

現在のリリースでは、在庫ワークフロー条件は、行レベルではなく仕訳帳レベルでのみ適用されます。 この動作は仕様です。 条件基準は、仕訳帳レベルの属性に対してだけ設定することをお勧めします。
