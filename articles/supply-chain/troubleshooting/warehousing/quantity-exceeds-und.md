---
title: 数量が過少配送率を超えているため、出荷を確認できない
description: 数量が過少配送率を超えているため、出荷を確認できない
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a6a5b1140d1bc5d09a1bc582fb1d2ac9446fae0920cbb9957797dbdea4c684e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760325"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>数量が過少配送率を超えているため、出荷を確認できない

エラーコード: WAX1686

## <a name="symptoms"></a>現象

出荷を確認しようとすると、次のエラー メッセージが表示されます。

> 品目 %2 の数量が過少配送に対して定義されている割合を超えているため、積荷 %1 の出荷を確認できませんでした。

したがって、積荷の出荷を確認できません。

## <a name="cause"></a>原因

積荷または出荷の数量は、一部ピッキング済になっています。 現在、数量が、許容される過少配送率を超える割合で、ピッキング済数量よりも少なくなっています。

## <a name="resolution"></a>解像度

この問題を解決するには、次のいずれかのタスクを実行します。

- 積荷明細行の数量を設定します。
- 過少配送率を設定します。

### <a name="set-the-load-line-quantity"></a>積荷明細行の数量を設定する

積荷明細行の数量を設定するには、次の手順に従います。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を選択します。
1. **積荷明細行** クイック タブで、過少配送率を超える品目の積荷明細行を選択します。
1. **明細行の詳細** クイックタブで、**注文** を選択します。
1. **数量** フィールドで、ピッキング済数量 (つまり、**作業作成数量** の値) に設定して、出荷確認が行われるようにします。

### <a name="set-the-underdelivery-percentage"></a>過少配送率の設定

過少配送率を設定するには、次の手順に従います。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 発送が確認できない積荷を選択します。
1. **積荷明細行** クイック タブで、過少配送率を超える品目の積荷明細行を選択します。
1. **明細行の詳細** クイックタブで、**全般** を選択します。
1. **過少配送** フィールドで、積荷数量に対してピッキングされた数量に対応するよりも大きな割合に値を設定して、出荷確認を行う必要があります。
