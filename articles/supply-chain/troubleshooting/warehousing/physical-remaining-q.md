---
title: 単位の残余現物数量がゼロではない
description: 梱包明細を生成するとき、提供されたデータの在庫数量はゼロではありませんが、販売数量はゼロになります。
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
ms.openlocfilehash: d767fdce861ccb481a3fe289480a51a7534dc207
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920227"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>単位の残余現物数量がゼロではない

エラーコード: SYS19591

## <a name="symptoms"></a>現象

梱包明細を生成するとき、提供されたデータの在庫数量はゼロではありませんが、販売数量はゼロになります。

梱包明細を生成しようとすると、次のエラー メッセージが表示されます:

> 単位 %1 の残余現物数量はゼロ以外でなければなりません。

したがって、積荷の梱包明細を生成できません。

## <a name="cause"></a>原因

システムは、在庫単位の残余現物数量と出荷単位の残余現物数量を評価します。 システムにおいて出荷単位の残余現物数量が 0 (ゼロ) であるが、在庫単位の残余現物数量が 0 でない場合、梱包明細を生成することはできません。 たとえば、品目の販売単位と在庫単位が異なり、単位間の変換が正確でない場合、この問題が発生することがあります。

## <a name="resolution"></a>解決策

積荷または出荷は現在、梱包明細の生成に失敗した状態になっています。 この問題を解決するには、次のいずれかのタスクを実行します。

- 積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。
- 積荷明細行を確認し、丸め問題なしに数量を正しく変換できるように調整します。
- 積荷明細行を確認し、単位の小数点以下の精度に合わせて単位と数量を調整します。
- 在庫単位が販売単位よりも少ないことを確認してください。

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認する

次の手順を使用して積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を選択します。
1. **積荷明細行** クイックタブで、積荷明細行を選択します。
1. **作業作成数量** フィールドの値を記録します。
1. アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。
1. 作業が最後の出荷場所で完了し、作業のピッキング済数量が積荷明細行で作成された作業数量と一致していることを確認します。
1. すべての積荷明細行に対してこの手順を繰り返して、すべての基準が満たされていることを確認します。

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>積荷明細行を確認し、丸め問題なしに数量を正しく変換できるように調整する

次の手順を使用して積荷明細行を確認し、丸め問題なしに数量を正しく変換できるように調整します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 梱包明細が生成できない積荷を選択します。
1. アクション ペインの、**出荷と入荷** タブの、**取消** グループで、**出荷確定の取消** を選択します。
1. **積荷明細行** タブで、超過配送を超える品目の積荷明細行を選択します。
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

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>在庫単位が販売単位よりも少ないことを確認する

在庫単位が販売単位よりも少ないことを確認してください。 必要に応じて、品目の単位を再構成する必要があります。
