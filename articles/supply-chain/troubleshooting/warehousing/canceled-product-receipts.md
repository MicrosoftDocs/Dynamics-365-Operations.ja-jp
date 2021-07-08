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
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294117"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="f931d-103">キャンセルされた製品受領書では、トランザクションのステータスは登録済に更新されません</span><span class="sxs-lookup"><span data-stu-id="f931d-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="f931d-104">現象</span><span class="sxs-lookup"><span data-stu-id="f931d-104">Symptoms</span></span>

<span data-ttu-id="f931d-105">入庫積荷で **製品受領書をキャンセル** アクションを実行した後、システムによって在庫トランザクションのステータスが *入庫済* から *注文済* に自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="f931d-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="f931d-106">解決策</span><span class="sxs-lookup"><span data-stu-id="f931d-106">Resolution</span></span>

<span data-ttu-id="f931d-107">梱包明細が出庫積荷に対してキャンセルされた場合、在庫トランザクションのステータスは *選択済* のままです。</span><span class="sxs-lookup"><span data-stu-id="f931d-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="f931d-108">ただし、入庫負荷からの製品入庫がキャンセルされた場合、在庫トランザクションのステータスは *登録済* に復元されません。</span><span class="sxs-lookup"><span data-stu-id="f931d-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="f931d-109">したがって、入庫積荷からの製品受領書がキャンセルされた後に、倉庫作業者は負荷の品目数量を再登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f931d-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="f931d-110">詳細については、[入庫積荷に到着する品目数量の登録](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f931d-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
