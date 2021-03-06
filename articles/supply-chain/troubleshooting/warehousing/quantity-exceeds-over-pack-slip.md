---
title: 梱包明細の生成中に数量が超過配送率を超えている場合
description: 梱包明細を生成すると、出庫積荷に超過配送率を超える数量が含まれます。
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
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249130"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>梱包明細の生成中に数量が超過配送率を超えている場合

エラーコード: SYS24920

## <a name="symptoms"></a>現象

梱包明細を生成すると、出庫積荷に超過配送率を超える数量が含まれます。

梱包明細を生成しようとすると、次のエラー メッセージが表示されます:

> ラインの出荷超過が %1 パーセントですが、出荷超過は %2 パーセントしか許可されません。

したがって、積荷の梱包明細を生成できません。

## <a name="cause"></a>原因

積荷または出荷の選択された数量が注文済数量を超え、過剰配送率の範囲内ではありません。

## <a name="resolution"></a>解決策

積荷または出荷は現在、梱包明細の生成に失敗した状態になっています。 この問題を解決するには、次のいずれかのタスクを実行します。

- 積荷明細行の数量を調整します。
- 超過配送率を調整します。
- 取り消して、調整します。

### <a name="adjust-the-load-line-quantity"></a>積荷明細行の数量を調整する

次の手順を使用して、積荷明細行の数量を調整します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 梱包明細が生成できない積荷を選択します。
1. アクション ウィンドウの、 **出荷と入荷** タブの、 **取消** グループで、 **出荷確定の取消** を選択します。
1.  **積荷明細行** タブで、超過配送率を超える品目の積荷明細行を選択します。
1. **ピッキング済数量の削減** を選択して、選択した数量を調整します。
1.  **明細行の詳細** タブで、**注文** を選択します。
1. **数量** フィールドをピッキング済数量 (つまり、**作業作成数量** フィールドの値) に設定して、梱包明細の生成が続行されるようにします。

### <a name="adjust-the-over-delivery-percentage"></a>超過配送率を調整する

次の手順を使用して、過剰配送率を調整します。

1. **売掛金勘定 \> 注文 \> すべての注文** の順に移動します。
1. 積荷の梱包明細を転記できない販売注文を選択します。
1.  **販売注文明細行** タブで、超過配送率を超える品目の販売注文明細行を選択します。
1.  **明細行の詳細** タブで、**配送** を選択します。
1. **超過配送** フィールドを、積荷数量に対してピッキングされた数量に対応するよりも大きな割合に設定して、梱包明細の生成が続行されるようにします。

### <a name="reverse-and-make-adjustments"></a>取り消して、調整する

積荷 (梱包明細、出荷確定、作業など) に対して転記されたすべてを取り消し、販売注文の調整を実行し、倉庫への注文を再リリースして、出荷手順を完了します。

次の手順を使用して、梱包明細をキャンセルします。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. アクション ウィンドウの、 **出荷と入荷** タブの、 **取消** グループで、 **梱包明細のキャンセル** を選択します。

次の手順を使用して、出荷確定を取り消します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. アクション ウィンドウの、 **出荷と入荷** タブの、 **取消** グループで、 **出荷確定の取消** を選択します。

次の手順を使用して、作業を取り消します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. アクション ウィンドウの **積荷** タブの、 **作業** グループで、 **作業の取消** を選択します。
