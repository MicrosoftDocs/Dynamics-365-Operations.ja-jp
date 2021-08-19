---
title: 顧客が保留中であるため出荷を確認できない
description: 顧客が保留中であるため出荷を確認できません。
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
ms.openlocfilehash: 82b28e7cfd8c88e453cdd09398f5a92f605eab15a17d33defa0b9729a53c05b6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012185"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>顧客が保留中であるため出荷を確認できない

エラー コード: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>現象

出荷を確認しようとすると、次のエラー メッセージが表示されます。

> 顧客が %2 に対して保留中であるため、出荷 %1 を確認できません。

したがって、積荷の出荷を確認できません。

## <a name="cause"></a>原因

負荷または出荷の顧客アカウントは保留中です。 したがって、顧客のステータスによって出荷の確認が防止されます。

## <a name="resolution"></a>解決策

顧客アカウントのブロックを解除するには、次の手順に従います。

1. **売掛金勘定 \> 顧客 \> すべての顧客** の順に移動します。
1. 出荷を確認できない顧客アカウントを開きます。
1. **与信および回収** クイック タブで、**請求と出荷の保留中** フィールドを *いいえ* に設定します。
1. 負荷がブロックされているすべての顧客に対してこの手順を繰り返します。
