---
title: 数量が超過配送率を超えているため、出荷を確認できない
description: 数量が超過配送率を超えているため、出荷を確認できない
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
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938507"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a>数量が超過配送率を超えているため、出荷を確認できない

エラーコード: WAX1687

## <a name="symptoms"></a>現象

出荷を確認しようとすると、次のエラー メッセージが表示されます。

> 品目 %2 の数量が超過配送に対して定義されている割合を超えているため、積荷 %1 の出荷を確認できませんでした。

したがって、積荷の出荷を確認できません。

## <a name="cause"></a>原因

積荷または出荷の数量は、一部ピッキング済になっています。 現在、数量が、許容される超過配送率を超える割合で、ピッキング済数量を超えています。

## <a name="resolution"></a>解像度

この問題を解決するには、次のいずれかのタスクを実行します。

- 積荷明細行の数量を設定します。
- 超過配送率を設定します。

### <a name="set-the-load-line-quantity"></a>積荷明細行の数量を設定する

積荷明細行の数量を設定するには、次の手順に従います。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を選択します。
1. **積荷明細行** クイック タブで、超過配送率を超える品目の積荷明細行を選択します。
1. **明細行の詳細** クイックタブで、**注文** を選択します。
1. **数量** フィールドで、ピッキング済数量 (つまり、**作業作成数量** の値) に設定して、出荷確認が行われるようにします。

### <a name="set-the-overdelivery-percentage"></a>超過配送率を設定する

過少配送率を設定するには、次の手順に従います。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を選択します。
1. **積荷明細行** クイック タブで、超過配送率を超える品目の積荷明細行を選択します。
1. **明細行の詳細** クイックタブで、**全般** を選択します。
1. **超過配送** フィールドで、積荷数量に対してピッキングされた数量に対応するよりも大きな割合に値を設定して、出荷確認を行う必要があります。
