---
title: カレンダーに問題がある場合は、出荷を確認できない
description: カレンダーに問題がある場合は、出荷を確認できない
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938506"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>カレンダーに問題がある場合は、出荷を確認できない

エラーコード: TRX2716

## <a name="symptoms"></a>現象

出荷を確認しようとすると、次のエラー メッセージが表示されます。

> カレンダー タイプ %1 では、予定 %2 をチェックイン/チェックアウトする必要があります。

したがって、積荷の出荷を確認できません。

## <a name="cause"></a>原因

積荷の有効な予定が存在します。 たとえば、ドライバーのチェックインを必要とするルールがあります。 そのため、積荷の状態は、現在出荷確認に失敗しています。

## <a name="resolution"></a>解像度

積荷にリンクされている有効な予定に関する問題を調査および修正する必要があります。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を選択します。
1. アクション ペインで、**輸送** タブの **予定** グループで、**予定のスケジューリング** を選択します。
1. 次の手順のいずれかを実行します。

    - 予定に対してドライバーのチェックイン/チェックアウトが完了済であることを確認します。
    - 予定を完了またはキャンセルします。
    - 関連する予定ルールで **ドライバーのチェックイン必須** オプションを無効にします。
