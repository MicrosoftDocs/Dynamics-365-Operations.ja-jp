---
title: 注文の分割時に開始された検査指示の数量が更新されない
description: 検査指示を作成してそれを分割しようとすると、注文数量が分割された残りの数量に更新されません。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026690"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="090b5-103">注文の分割時に開始された検査指示の数量が更新されない</span><span class="sxs-lookup"><span data-stu-id="090b5-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="090b5-104">KB 番号: 4613113</span><span class="sxs-lookup"><span data-stu-id="090b5-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="090b5-105">現象</span><span class="sxs-lookup"><span data-stu-id="090b5-105">Symptoms</span></span>

<span data-ttu-id="090b5-106">検査指示を作成してそれを分割しようとすると、注文数量が分割後の残り数量に更新されません。</span><span class="sxs-lookup"><span data-stu-id="090b5-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="090b5-107">解像度</span><span class="sxs-lookup"><span data-stu-id="090b5-107">Resolution</span></span>

<span data-ttu-id="090b5-108">検査指示で作成された元の数量を確実に追跡できるように、システムは検査指示から元の数量を変更しません。</span><span class="sxs-lookup"><span data-stu-id="090b5-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="090b5-109">ただし、検査指示から分割される数量はシステムによって追跡されます。</span><span class="sxs-lookup"><span data-stu-id="090b5-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="090b5-110">この追跡を行うには、`QuantityThatHasSplitIntoOtherQuarantineOrders` という名前の付いたデータベース フィールドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="090b5-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="090b5-111">ただし、このフィールドはユーザー インターフェイス (UI) に表示されません。</span><span class="sxs-lookup"><span data-stu-id="090b5-111">However, this field isn't visible in the user interface (UI).</span></span>