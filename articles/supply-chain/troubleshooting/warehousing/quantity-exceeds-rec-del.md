---
title: 更新しようとしている数量が、入庫済/配送済の数量を超えています。
description: 梱包明細を生成すると、出庫積荷には販売注文に対して選択および保存された作業数量を超えた数量が含まれます。
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 25507a482b2db7c01f56679bf3e8454249de3a6b9965f9c359a2ebe2cc8445ce
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711690"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>更新しようとしている数量が、入庫済/配送済の数量を超えている場合

エラーコード: SYS7676

## <a name="symptoms"></a>現象

梱包明細を生成すると、出庫積荷には販売注文に対して選択および保存された作業数量を超えた数量が含まれます。

梱包明細を生成しようとすると、次のエラー メッセージが表示されます:

> 更新しようとした数量は受入/配送できる数量を超えています。

したがって、積荷の梱包明細を生成できません。

## <a name="cause"></a>原因

作業のピッキング済数量が、積荷明細行で作成された作業数量と一致しません。 たとえば、積荷明細行の数量、作成済作業の数量、またはピッキング済数量が正確ではない場合、この問題が発生する可能性があります。

## <a name="resolution"></a>解決策

積荷または出荷は現在、梱包明細の生成に失敗した状態になっています。 この問題を解決するには、次のいずれかのタスクを実行します。

- 積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。
- 積荷明細行の数量を調整します。
- すべてのピッキング登録を取り消し、ピッキングを再実行します。

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認する

次の手順を使用して積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が生成できない積荷を選択します。
1. **積荷明細行** クイックタブで、積荷明細行を選択します。
1. **作業作成数量** フィールドの値を記録します。
1. アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。
1. 作業が最後の出荷場所で完了し、作業のピッキング済数量が積荷明細行で作成された作業数量と一致していることを確認します。
1. すべての積荷明細行に対してこの手順を繰り返して、すべての基準が満たされていることを確認します。

### <a name="adjust-the-load-line-quantity"></a>積荷明細行の数量を調整する

次の手順を使用して、積荷明細行の数量を調整します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 梱包明細が生成できない積荷を選択します。
1. アクション ウィンドウの、 **出荷と入荷** タブの、 **取消** グループで、 **出荷確定の取消** を選択します。
1.  **積荷明細行** タブで、問題の原因となる品目の積荷明細行を選択します。
1. **ピッキング済数量の削減** を選択して、選択した数量を調整します。
1. **ピッキング済数量の削減** フィールドが積荷明細行の調整を反映するように設定します。

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>すべてのピッキング登録を取り消し、ピッキングを再実行する

ピッキングの登録を使用して作業なしで積荷明細行をクローズした場合、積荷明細行の数量とピッキング済数量の間に不一致が発生する場合があります。 この場合は、手動ピッキング登録を取り消す必要があります。また Warehouse Management モバイル アプリを使用してピッキングを完了する必要があります。

ピッキング登録を取り消すには、次の手順を使用します。

1. **売掛金勘定 \> 注文 \> すべての注文** の順に移動します。
1. 積荷の梱包明細を転記できない販売注文を選択します。
1.  **販売注文明細行** タブで、ピッキング登録が実行された販売注文明細行を選択します。
1. **明細行の更新 \> ピッキング** を選択して、品目のピッキングを解除します。
