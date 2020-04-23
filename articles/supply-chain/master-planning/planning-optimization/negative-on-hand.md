---
title: マイナスの手持在庫数量を使用した計画
description: このトピックでは、計画の最適化を使用する場合のマイナスの手持在庫の処理方法について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8803b0b90f22711b844442d16f717ab87dabf041
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209861"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="ff31b-103">マイナスの手持在庫数量を使用した計画</span><span class="sxs-lookup"><span data-stu-id="ff31b-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff31b-104">システムによってマイナスの集計手持在庫数量が表示される場合、計画エンジンは過剰な供給を回避するため、数量を 0 (ゼロ) として扱います。</span><span class="sxs-lookup"><span data-stu-id="ff31b-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="ff31b-105">この機能の動作は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ff31b-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="ff31b-106">計画の最適化機能では、最下位レベルの補充分析コードの手持在庫数量が集計されます。</span><span class="sxs-lookup"><span data-stu-id="ff31b-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="ff31b-107">(たとえば、*場所*が補充分析コードではない場合、計画の最適化では手持在庫数量が*倉庫*レベルで集計されます。)</span><span class="sxs-lookup"><span data-stu-id="ff31b-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="ff31b-108">最下位レベルの補充分析コードの集計手持在庫数量がマイナスの場合、システムでは手持在庫数量が実際に 0 (ゼロ) であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="ff31b-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff31b-109">計画システムは、入力データと同じ精度でしか設定できません。</span><span class="sxs-lookup"><span data-stu-id="ff31b-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="ff31b-110">入力データが誤っている場合、マイナスの手持在庫レコードによって、Microsoft Dynamics 365 Supply Chain Management の在庫情報が実際の世界と同期されていないことが示されます。</span><span class="sxs-lookup"><span data-stu-id="ff31b-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="ff31b-111">したがって、計画結果には欠陥があります。</span><span class="sxs-lookup"><span data-stu-id="ff31b-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="ff31b-112">正確な計画の結果を得るには、マイナスの手持在庫数量を表示するレコードの数を最小限にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff31b-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="ff31b-113">例 1</span><span class="sxs-lookup"><span data-stu-id="ff31b-113">Example 1</span></span>

<span data-ttu-id="ff31b-114">倉庫 13 は、次の方法で構成されています。</span><span class="sxs-lookup"><span data-stu-id="ff31b-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="ff31b-115">**補充コード:** 最小/最大。</span><span class="sxs-lookup"><span data-stu-id="ff31b-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="ff31b-116">**最小:** 15 個</span><span class="sxs-lookup"><span data-stu-id="ff31b-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="ff31b-117">**最大:** 25 個。</span><span class="sxs-lookup"><span data-stu-id="ff31b-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="ff31b-118">最下位レベルの補充分析コードは*倉庫*で、次の手持在庫数量は*場所*レベルで記録されます。</span><span class="sxs-lookup"><span data-stu-id="ff31b-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="ff31b-119">**サイト 1、倉庫 13、場所 1:** 20 個。</span><span class="sxs-lookup"><span data-stu-id="ff31b-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="ff31b-120">**サイト 1、倉庫 13、場所 2:** &minus;8 個。</span><span class="sxs-lookup"><span data-stu-id="ff31b-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="ff31b-121">したがって、倉庫 13 の集計手持在庫数量は 12 個です。</span><span class="sxs-lookup"><span data-stu-id="ff31b-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="ff31b-122">(= 20 個。</span><span class="sxs-lookup"><span data-stu-id="ff31b-122">(= 20 pcs.</span></span> <span data-ttu-id="ff31b-123">&minus; 8 個)。</span><span class="sxs-lookup"><span data-stu-id="ff31b-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="ff31b-124">この場合、計画エンジンでは 12 個の集計手持数量が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff31b-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="ff31b-125">倉庫 13 に対して。</span><span class="sxs-lookup"><span data-stu-id="ff31b-125">for warehouse 13.</span></span>

<span data-ttu-id="ff31b-126">結果は 13 個の計画オーダーです。</span><span class="sxs-lookup"><span data-stu-id="ff31b-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="ff31b-127">(= 25 個。</span><span class="sxs-lookup"><span data-stu-id="ff31b-127">(= 25 pcs.</span></span> <span data-ttu-id="ff31b-128">&minus; 12 個) 12 個から倉庫 13 に補充する場合に行います。</span><span class="sxs-lookup"><span data-stu-id="ff31b-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="ff31b-129">25 個へ。</span><span class="sxs-lookup"><span data-stu-id="ff31b-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="ff31b-130">例 2</span><span class="sxs-lookup"><span data-stu-id="ff31b-130">Example 2</span></span>

<span data-ttu-id="ff31b-131">倉庫 13 は、次の方法で構成されています。</span><span class="sxs-lookup"><span data-stu-id="ff31b-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="ff31b-132">**補充コード:** 最小/最大。</span><span class="sxs-lookup"><span data-stu-id="ff31b-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="ff31b-133">**最小:** 15 個。</span><span class="sxs-lookup"><span data-stu-id="ff31b-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="ff31b-134">**最大:** 25 個。</span><span class="sxs-lookup"><span data-stu-id="ff31b-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="ff31b-135">最下位レベルの補充分析コードは*倉庫*で、次の手持在庫数量は*場所*レベルで記録されます。</span><span class="sxs-lookup"><span data-stu-id="ff31b-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="ff31b-136">**サイト 1、倉庫 13、場所 1:** 4 個。</span><span class="sxs-lookup"><span data-stu-id="ff31b-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="ff31b-137">**サイト 1、倉庫 13、場所 2:** &minus;8 個。</span><span class="sxs-lookup"><span data-stu-id="ff31b-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="ff31b-138">したがって、倉庫 13 の集計手持在庫数量は &minus;4 個です。</span><span class="sxs-lookup"><span data-stu-id="ff31b-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="ff31b-139">(= 4 個。</span><span class="sxs-lookup"><span data-stu-id="ff31b-139">(= 4 pcs.</span></span> <span data-ttu-id="ff31b-140">&minus; 8 個)。</span><span class="sxs-lookup"><span data-stu-id="ff31b-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="ff31b-141">つまり、0 (ゼロ) 以下です。</span><span class="sxs-lookup"><span data-stu-id="ff31b-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="ff31b-142">この場合、計画エンジンは、倉庫 13 の手持在庫数量が 0 個であるとみなします。</span><span class="sxs-lookup"><span data-stu-id="ff31b-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="ff31b-143">&minus;4 個の代わりに。</span><span class="sxs-lookup"><span data-stu-id="ff31b-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="ff31b-144">結果は 25 個の計画オーダーです。</span><span class="sxs-lookup"><span data-stu-id="ff31b-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="ff31b-145">(= 25 個。</span><span class="sxs-lookup"><span data-stu-id="ff31b-145">(= 25 pcs.</span></span> <span data-ttu-id="ff31b-146">&minus; 0 個) 0 個から倉庫 13 に補充する場合に行います。</span><span class="sxs-lookup"><span data-stu-id="ff31b-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="ff31b-147">25 個へ。</span><span class="sxs-lookup"><span data-stu-id="ff31b-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="ff31b-148">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="ff31b-148">Related resources</span></span>

[<span data-ttu-id="ff31b-149">計画最適化の概要</span><span class="sxs-lookup"><span data-stu-id="ff31b-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="ff31b-150">計画最適化の開始</span><span class="sxs-lookup"><span data-stu-id="ff31b-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="ff31b-151">計画の最適化フィット分析</span><span class="sxs-lookup"><span data-stu-id="ff31b-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="ff31b-152">計画の履歴と計画ログの表示</span><span class="sxs-lookup"><span data-stu-id="ff31b-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="ff31b-153">計画ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="ff31b-153">Cancel a planning job</span></span>](cancel-planning-job.md)
