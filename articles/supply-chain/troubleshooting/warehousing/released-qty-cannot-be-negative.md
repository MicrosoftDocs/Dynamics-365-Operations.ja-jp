---
title: リリース済数量がマイナスなので、積荷明細行を更新できない
description: この問題は、積荷明細行を更新または削除すると、マイナスのリリース済数量が発生する場合に起こります。
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728462"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>リリース済数量がマイナスなので、積荷明細行を更新できない

エラー コード: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>現象

この問題は、積荷明細行を更新または削除すると、マイナスのリリース済数量が発生する場合に起こります。 この場合、積荷明細行を更新または削除しようとする場合は、次のエラー メッセージが表示されます。

> 品目 %1、ロット %2 のリリース済数量を負の値にすることはできません。

したがって、積荷明細行を更新または削除できません。

## <a name="cause"></a>原因

積荷明細行を更新または削除すると、システムは関連する販売明細行のリリース済数量が更新します (*whsSalesLine.ReleaseQty*)。 システムはリリース済数量を評価し、更新後に明細行のリリース済数量がマイナスになることが判明した場合、明細行を更新または削除することはできません。 この検証は、積荷明細行の削除、出荷の削除、積荷明細行の数量の変更、ピッキング済数量の削減、ショート ピッキングなどのさまざまなアクションを通じて、積荷明細行の数量または測定単位のいずれかを更新しようとするたびに行われます。

この問題の最も一般的な根本原因は、オープンな積荷明細行に使用される単位換算の変更です。 たとえば、販売注文がリリースされた場合の単位換算は、*50 Ea = 1 PL* でした。 ただし、関連する積荷の出荷が終了する前は、単位換算が *100 Ea = 1 PL* に変更されました。

## <a name="resolution"></a>解決策

解決策は、単位換算の変更を元に戻し、積荷明細行を更新または削除してから、変換を再実装することです。 問題が修正されるまで、問題の原因となった品目を含む他の積荷が処理されないようにする必要があります。 それ以外の場合は、既に開いている他の積荷に対して新しい換算が使用される可能性があります。

この問題を解決するには、次のタスクを実行します。

1. 積荷明細行に対して使用された単位換算を確認します。
2. 品目の現在の単位換算を確認し、積荷明細行の更新または削除できるように調整します。
3. 積荷明細行を更新または削除し、単位換算調整を元に戻します。

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>積荷明細行に対して使用された単位換算を確認する

次の手順に従って、積荷明細行を確認し、積荷明細行に対して使用された単位換算をメモします。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 削除または更新できない積荷明細行を含む積荷を選択します。
1. アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。
1. 上部グリッドで、関連する作業 ID を選択します。
1. ページの下部にある **一般** タブで、**在庫作業数量の値** と **作業数量の値** との間の換算率を計算します。 レートの値をメモします。
1. すべての関連作業の ID に対してこの手順を繰り返して、同じ換算が使用されたことを確認します。

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>品目の現在の単位換算を確認し、調整を行う

次の手順を使用して製品の単位換算を確認し、単位変換が積荷明細行と一致するように調整します。

1. **製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。
1. 関連する製品を起動し、**リリース済製品の詳細** ページに移動します。
1. アクション ウィンドウ、**製品** タブの、**設定** グループで、**単位換算** を選択します。
1. 単位間の換算を選択し、前のセクションで検出した換算を使用して調整します。

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>積荷明細行を更新または削除し、単位換算調整を元に戻す

必要に応じて積荷明細行を処理し、単位換算を元に戻すには、次の手順に従います。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 削除または更新できない積荷明細行を含む積荷を開きます。
1. **積荷明細行** クイックタブで、積荷明細行を選択します。
1. 必要に応じて必要なアクションを続行します。 (たとえば、積荷明細行を削除したり、数量を変更したりします。)
1. **製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。
1. 関連する製品を起動し、**リリース済製品の詳細** ページに移動します。
1. アクション ウィンドウ、**製品** タブの、**設定** グループで、**単位換算** を選択します。
1. 単位間の換算を選択し、前のセクションで作成した調整を元に戻します。
