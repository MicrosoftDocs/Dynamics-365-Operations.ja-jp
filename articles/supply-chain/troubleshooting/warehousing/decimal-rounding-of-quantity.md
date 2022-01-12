---
title: 物理的な更新数量の 10 進数の丸めが正しくありません
description: 梱包明細を生成すると、出庫積荷に単位で定義された小数点以下の精度と一致しない数量が含まれます。
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a9e0475aab452daa9e1a6f012e17a59e611010da
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920476"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>物理的な更新数量の 10 進数の丸めが正しくありません

エラーコード: SYS19589

## <a name="symptoms"></a>現象

梱包明細を生成すると、出庫積荷に単位で定義された小数点以下の精度と一致しない数量が含まれます。

梱包明細を生成しようとすると、次のエラー メッセージが表示されます:

> 単位 %1 の更新現物数量の小数の丸めが正しくありません。

したがって、積荷の梱包明細を生成できません。

## <a name="cause"></a>原因

システムでは、出荷数量の 10 進数の丸めが出荷単位に定義されている小数点以下の精度に対応するかどうかが評価されます。 システムにより出荷数量を指定した 10 進数の桁数に丸めたときに、丸め出荷数量が実際の出荷数量と一致しない場合は、梱包明細を生成できません。 たとえば、販売数量が 1.75 キログラム (kg) で、小数点以下の精度が *1* に設定されている場合にこの問題が発生する可能性があります。

## <a name="resolution"></a>解決策

積荷または出荷は現在、梱包明細の生成に失敗した状態になっています。 この問題を解決するには、次のいずれかのタスクを実行します。

- 負荷行を確認し、10 進数および他の丸め問題なしに数量を正しく変換できるように調整します。
- 積荷明細行を確認し、単位の小数点以下の精度に合わせて単位と数量を調整します。

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>負荷行を確認し、10 進数および他の丸め問題なしに数量を正しく変換できるように調整する

次の手順を使用して負荷行を確認し、10 進数および他の丸め問題なしに数量を正しく変換できるように調整します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 梱包明細が生成できない積荷を選択します。
1. アクション ペインの、**出荷と入荷** タブの、**取消** グループで、**出荷確定の取消** を選択します。
1. **積荷明細行** タブで、問題の原因となる品目の積荷明細行を選択します。
1. **ピッキング済数量の削減** を選択して、選択した数量を調整します。
1. **明細行の詳細** タブで、**注文** を選択します。
1. **数量** フィールドをピッキング済数量 (つまり、**作業作成数量** フィールドの値) に設定して、梱包明細の生成が続行されるようにします。

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>積荷明細行を確認し、単位の小数点以下の精度に合わせて単位と数量を調整する

次の手順を使用して積荷明細行を確認し、単位の小数点以下の精度に合わせて単位と数量を調整します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 梱包明細が生成できない積荷を選択します。
1. **積荷明細行** クイックタブで、問題の原因となる品目の積荷明細行を選択します。 **数量** および **単位** フィールドの値を記録します。
1. **組織管理 \> 単位 \> 単位** に移動します。
1. 梱包明細が生成できない単位を選択します。
1. 必要に応じて **小数点以下の精度** フィールドの値を調整します。
