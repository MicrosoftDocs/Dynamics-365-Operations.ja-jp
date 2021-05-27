---
title: 現物入庫済み購買注文は在庫決算レポートに表示されない
description: 現物入庫済み購買注文が、オープン数量チェック在庫決算レポートに表示されません。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026677"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="d05f4-103">現物入庫済み購買注文は在庫決算レポートに表示されない</span><span class="sxs-lookup"><span data-stu-id="d05f4-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="d05f4-104">KB 番号: 4612595</span><span class="sxs-lookup"><span data-stu-id="d05f4-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="d05f4-105">現象</span><span class="sxs-lookup"><span data-stu-id="d05f4-105">Symptoms</span></span>

<span data-ttu-id="d05f4-106">現物入庫済み購買注文が、**オープン数量チェック** 在庫決算レポートに表示されません。</span><span class="sxs-lookup"><span data-stu-id="d05f4-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="d05f4-107">解像度</span><span class="sxs-lookup"><span data-stu-id="d05f4-107">Resolution</span></span>

<span data-ttu-id="d05f4-108">**オープン数量チェック** レポートには、選択した決算日現在で現物入庫済みの在庫入庫に対して決済できない出庫トランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d05f4-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="d05f4-109">レポートでは現物入庫を含めるオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d05f4-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="d05f4-110">この場合、決済できない出庫トランザクションに対処できる場合は、現物入庫が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d05f4-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="d05f4-111">詳細については、[在庫原価計算の実行の準備](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d05f4-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>
