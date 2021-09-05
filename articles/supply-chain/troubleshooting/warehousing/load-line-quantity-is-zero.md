---
title: 積荷明細行が数量がゼロであるため出荷を確認できない
description: 積荷明細行が数量がゼロであるため出荷を確認できません。
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 15aa7f5e72ff8f2c027b5b020a23328978aa02b0
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344237"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>積荷明細行が数量がゼロであるため出荷を確認できない

エラー コード: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>現象

出荷を確認しようとすると、次のエラー メッセージが表示されます。

> 積荷 %1 のすべての明細行の数量がゼロになっています。  
> 積荷 %1 の出荷を確認できませんでした。

したがって、積荷の出荷を確認できません。

## <a name="cause"></a>原因

システムでは、作成された作業 ID、積荷明細行の数量、および過少配送率に基づいて、積荷明細行を確認できるかどうかを評価します。 作業 ID がない場合、および過少配送率が 100% に設定されている場合は、出荷を確認できません。

たとえば、作業がキャンセルされ、積荷明細行の過少配送率が 100% の場合、この問題が発生する可能性があります。

## <a name="resolution"></a>解決策

積荷または出荷は現在、出荷確認に失敗した状態になっています。 この問題を解決するには、次のいずれかのタスクを実行します。

- 積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。
- 過少配送率と数量がピッキング済作業と一致するよう、積荷明細行を確認します。

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認する

次の手順を使用して積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を開きます。
1. **積荷明細行** クイックタブで、積荷明細行を選択します。
1. **作業作成数量** フィールドの値を記録します。
1. アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。
1. 作業が最後の出荷場所で完了し、作業のピッキング済数量が積荷明細行で作成された作業数量と一致していることを確認します。
1. 不一致が見つかった場合は、関連する作業をキャンセルし、場所のディレクティブを再構成して、負荷を再リリースします。 手順については、[品目がピッキングされていないために出荷を確認できない](picked-quantity-is-not-on-final.md) を参照してください。
1. すべての積荷明細行に対してこの手順を繰り返して、すべての基準が満たされていることを確認します。

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>過少配送率と数量がピッキング済作業と一致するよう、積荷明細行を確認する

以下の手順を使用して、過少配送率と数量がピッキング済作業と一致するよう、積荷明細行を確認します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を開きます。
1. **積荷明細行** クイック タブで、過少配送率を超える品目の積荷明細行を選択します。
1. 必要に応じて、**過少配送** フィールドまたは **数量** フィールドの値を調整します。

> [!TIP]
> それでも問題が解決しない場合は、利用可能な数量が積荷または出荷に一致するまで、関連する販売注文または移動オーダーに対してピッキング作業を完了する必要があります。
