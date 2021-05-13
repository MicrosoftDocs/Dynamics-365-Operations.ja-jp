---
title: 品目がピッキングされていないため、出荷を確認できない
description: 品目がピッキングされていないため、出荷を確認できない
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938504"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>品目がピッキングされていないため、出荷を確認できない

エラー コード: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>現象

出荷を確認しようとすると、次のエラー メッセージが表示されます。

> 積荷 %1 に必要な一部の品目がまだピッキングされておらず、最終出荷場所に移動されていません。

したがって、積荷の出荷を確認できません。

## <a name="cause"></a>原因

次のいずれかの条件が存在する可能性があるため、現在の状態では積荷または出荷を確認できません:

- 関連する作業がまだ選択されていないので、最終的な出荷場所に移動されていません。
- 作業のピッキング済数量が、積荷明細行で作成された作業数量と一致しません。

## <a name="resolution"></a>解像度

積荷または出荷用の関連する販売注文または移動オーダーを確認します。 関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を選択します。
1. **積荷明細行** クイックタブで、積荷明細行を選択します。
1. **作業作成数量** フィールドの値を記録します。
1. アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。
1. 作業が最後の出荷場所で完了し、作業のピッキング済数量が積荷明細行で作成された作業数量と一致していることを確認します。
1. すべての積荷明細行に対してこの手順を繰り返して、すべての基準が満たされていることを確認します。
