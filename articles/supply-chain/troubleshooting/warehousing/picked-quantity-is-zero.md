---
title: 数量がゼロであるため、出荷を確認できない
description: 数量がゼロであるため、出荷を確認できない
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938503"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>数量がゼロであるため、出荷を確認できない

エラー コード: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>現象

出荷を確認しようとすると、次のエラー メッセージが表示されます。

> 品目 %1 および出荷 %2 の積荷明細行は、配送不足の設定が原因で数量が 0 に更新されており、この品目の数量は出荷できません。

したがって、積荷の出荷を確認できません。

## <a name="cause"></a>原因

システムでは、ピッキング済数量、積荷明細行数量、および過少配送率に基づいて、ピッキング済数量が予想制限内かどうかが評価されます。 積荷明細行のピッキング済数量が 0 (ゼロ) である場合は、出荷を確認できません。 たとえば、作業がキャンセルされ、積荷明細行の過少配送率が 100% の場合、この問題が発生する可能性があります。

## <a name="resolution"></a>解像度

過少配送率と数量がピッキング済作業と一致するよう、積荷明細行を確認します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を選択します。
1. **積荷明細行** クイック タブで、過少配送率を超える品目の積荷明細行を選択します。
1. 必要に応じて、**過少配送** フィールドまたは **数量** フィールドの値を調整します。

> [!TIP]
> それでも問題が解決しない場合は、利用可能な数量が積荷または出荷に一致するまで、関連する販売注文または移動オーダーに対してピッキング作業を完了する必要があります。
