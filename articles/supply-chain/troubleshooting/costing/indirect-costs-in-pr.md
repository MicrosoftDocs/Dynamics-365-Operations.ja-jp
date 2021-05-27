---
title: プロセス レポートの間接原価には削除された製造オーダーが含まれます
description: プロセス レポートの間接原価には、部分的に処理され、後で削除された製造オーダーに関する情報が表示されます。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026678"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="f2599-103">プロセス レポートの間接原価には削除された製造オーダーが含まれます</span><span class="sxs-lookup"><span data-stu-id="f2599-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="f2599-104">KB 番号: 4612748</span><span class="sxs-lookup"><span data-stu-id="f2599-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="f2599-105">現象</span><span class="sxs-lookup"><span data-stu-id="f2599-105">Symptoms</span></span>

<span data-ttu-id="f2599-106">**プロセス レポートの間接原価** には、部分的に処理され、後で削除された製造オーダーに関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2599-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="f2599-107">解像度</span><span class="sxs-lookup"><span data-stu-id="f2599-107">Resolution</span></span>

<span data-ttu-id="f2599-108">製造オーダーを取り消す場合は、その製造オーダーのすべてのトランザクションも取り消します。</span><span class="sxs-lookup"><span data-stu-id="f2599-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="f2599-109">製造オーダーを削除すると、補助元帳テーブルと総勘定元帳に関連付いたすべてのトランザクションが保持されます。</span><span class="sxs-lookup"><span data-stu-id="f2599-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="f2599-110">レポートには、補助元帳テーブルのトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2599-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="f2599-111">特定の製造オーダーの場合、正味値は 0.00 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2599-111">For the specific production order, the net value should be 0.00.</span></span>
