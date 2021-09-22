---
title: 在庫評価方法が標準原価または移動平均である場合の更新の競合
description: 在庫評価方法が標準原価または移動平均である場合に更新の競合が発生する
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476906"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>在庫評価方法が標準原価または移動平均である場合に更新の競合が発生する

## <a name="symptoms"></a>現象

在庫仕訳帳、発注請求書、販売注文請求書などのドキュメントを、スケーラビリティとパフォーマンスに関して並列で転記すると、更新の競合に関するエラー メッセージが表示され、一部のドキュメントが転記されない場合があります。 この問題は、在庫評価方法が *標準原価* または *移動平均* である場合に発生します。 これらの方法はどちらも永続的な原価計算の方法です。 つまり、最終的な原価は転記時に決定されます。

*移動平均法* を使用している場合、エラー メッセージは次のような例です。

> 比例経費計算後の在庫値 xx.xx が予期されません

*標準コスト* を使用している場合、エラー メッセージは次のような例です。

> 更新後の標準原価が資産在庫金額と一致しません。 値 = xx.xx, Qty = yy.yy、標準コスト = zz.zz

## <a name="workaround"></a>回避策

Microsoft が問題を修正するソリューションをリリースするまで、次の説明を使用してエラーを回避または減らしてください。

- 失敗したドキュメントを再転記します。
- 明細行の少ないドキュメントを作成します。
- 標準コストでは小数の値を避けます。 **価格数量** フィールドが *1* に設定された標準コストを定義してください。 *1* より大きい **価格数量** 値を指定する必要がある場合は、単位標準原価の小数点以下の桁数を最小限にしてください。 (小数点以下 2 桁以下が理想的です)。たとえば、**価格** = *10* や **価格数量** = *3* などの標準原価設定は 、3.333333 (小数点以下の値が繰り返される) 単位標準原価を生成するので定義しないようにします。
- 大多数のドキュメントでは、製品在庫分析コードと資産在庫分析コードの同じ組み合わせを保持する複数の明細行を保持しないようにします。
- 並列処理の程度を減らします。 (この場合、更新の競合や再試行の回数が少なくなるので、システムが高速化される可能性があります)。
