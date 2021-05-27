---
title: 直接派生した会社注文は、レビュー中のワークフローによって処理されます
description: 直接派生した会社注文は、レビュー中のワークフローによって処理されます。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026685"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="5a9f3-103">直接派生した会社注文は、レビュー中のワークフローによって処理されます</span><span class="sxs-lookup"><span data-stu-id="5a9f3-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="5a9f3-104">KB 番号: 4612450</span><span class="sxs-lookup"><span data-stu-id="5a9f3-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="5a9f3-105">現象</span><span class="sxs-lookup"><span data-stu-id="5a9f3-105">Symptoms</span></span>

<span data-ttu-id="5a9f3-106">直接派生した会社注文は、*レビュー中* のワークフローによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="5a9f3-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="5a9f3-107">解像度</span><span class="sxs-lookup"><span data-stu-id="5a9f3-107">Resolution</span></span>

<span data-ttu-id="5a9f3-108">変更追跡が有効な場合、確定した派生オーダー (外注発注書) は、案件変更のトラッキングが有効になっている場合は、状態が *レビュー中* と表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a9f3-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="5a9f3-109">したがって、派生した発注書 (外注発注書) は、ワークフローにのみ送信されます。</span><span class="sxs-lookup"><span data-stu-id="5a9f3-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="5a9f3-110">発注書が固定された計画発注書の場合、発注書のステータスが *ドラフト* の間、計画エンジンが新しい計画オーダーを作成しない場合は、自動的に承認されます。</span><span class="sxs-lookup"><span data-stu-id="5a9f3-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
