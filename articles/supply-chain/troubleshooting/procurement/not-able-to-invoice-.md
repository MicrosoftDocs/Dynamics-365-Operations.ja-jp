---
title: 顧客向けの販売注文は請求できません
description: '[請求書の自動転記] オプションを有効した後に、元の販売注文と元の直納発注書の請求は行えなくなりました。'
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026673"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="d149d-103">顧客向けの販売注文は請求できません</span><span class="sxs-lookup"><span data-stu-id="d149d-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="d149d-104">KB 番号: 4611793</span><span class="sxs-lookup"><span data-stu-id="d149d-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="d149d-105">現象</span><span class="sxs-lookup"><span data-stu-id="d149d-105">Symptoms</span></span>

<span data-ttu-id="d149d-106">仕入れ先の **会社間** ページで **請求書の自動転記** オプションを有効した後に、元の販売注文と元の直納発注書の請求は行えなくなりました。</span><span class="sxs-lookup"><span data-stu-id="d149d-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="d149d-107">解像度</span><span class="sxs-lookup"><span data-stu-id="d149d-107">Resolution</span></span>

<span data-ttu-id="d149d-108">会社間および直納注文の請求に関する同期動作は、[パラメーターを設定して会社間の注文を転記する](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order) で説明があるように、パラメータによって制御、強制されています。</span><span class="sxs-lookup"><span data-stu-id="d149d-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="d149d-109">これらのパラメータを設定した後、最初に会社間の販売注文を請求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d149d-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="d149d-110">そうすると、元の販売注文と発注書が同期されます。</span><span class="sxs-lookup"><span data-stu-id="d149d-110">The original sales orders and purchase orders will then be synchronized.</span></span>
