---
title: キャンセルされた製品受領書では、トランザクションのステータスは登録済に更新されません
description: 入庫積荷の製品受領書をキャンセルした後、システムによって在庫トランザクション のステータスが入庫済から注文済に自動的に更新されます。
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eae703ce0b2c981518b18c4badd4f90031b902ece62f3ca0837427b306d618b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731106"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>キャンセルされた製品受領書では、トランザクションのステータスは登録済に更新されません

## <a name="symptoms"></a>現象

入庫積荷で **製品受領書をキャンセル** アクションを実行した後、システムによって在庫トランザクションのステータスが *入庫済* から *注文済* に自動的に更新されます。

## <a name="resolution"></a>解決策

梱包明細が出庫積荷に対してキャンセルされた場合、在庫トランザクションのステータスは *選択済* のままです。 ただし、入庫負荷からの製品入庫がキャンセルされた場合、在庫トランザクションのステータスは *登録済* に復元されません。 したがって、入庫積荷からの製品受領書がキャンセルされた後に、倉庫作業者は負荷の品目数量を再登録する必要があります。

詳細については、[入庫積荷に到着する品目数量の登録](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving) を参照してください。
