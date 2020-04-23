---
title: 計画の最適化の概要
description: このトピックでは、計画の最適化機能の概要を示します。
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f88ee8067fdd816ba6890ee28bafe8fa4d3b3ac5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208734"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="bb3eb-103">計画の最適化の概要</span><span class="sxs-lookup"><span data-stu-id="bb3eb-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="bb3eb-104">Microsoft Dynamics 365 Supply Chain Management の計画の最適化アドインを使用すると、マスター プランの計算を、Dynamics 365 Supply Chain Management および関連する SQL データベース以外で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="bb3eb-105">計画の最適化機能に関連する利点として、マスター プランの実行時にパフォーマンスが向上し、SQL データベースへの影響が最小限に抑えられます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="bb3eb-106">迅速なプランニングを営業時間中に実行できるため、プランナーは要求またはパラメータの変更にすぐに対応できます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="bb3eb-107">計画の最適化を使用するには、計画の最適化アドインを Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトからインストールし、Supply Chain Management の計画の最適化機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="bb3eb-108">詳細については、[計画の最適化を開始する](get-started.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="bb3eb-109">次の図は、営業時間内に計画の最適化を実行する利点を示しています。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![営業時間内に計画の最適化を実行する利点](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="bb3eb-111">パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="bb3eb-111">Improved performance</span></span>

<span data-ttu-id="bb3eb-112">長時間実行されるマスター プランに関連するシナリオでは、計画の最適化を使用できます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="bb3eb-113">非常に大量のデータを含む非常に高速な計算に特化して設計されています。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="bb3eb-114">ハイパースケーラブルなマルチテナント サービスとして構築されているため、複数のインスタンスは同時に連携して計画を計算することができます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="bb3eb-115">さらに、計画サービスはマスター プランの負荷をシステムから除去し、サーバーの負荷を最小限に抑えるデータ ストリームと連携して機能します。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="bb3eb-116">計画の最適化は、次の目標を達成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="bb3eb-117">短い実行時間で計画のパフォーマンスを向上させること。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="bb3eb-118">マスター プランの実行中に他のプロセスへの影響を軽減すること。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="bb3eb-119">より頻繁に計画を実行すること。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-119">Do more frequent planning runs.</span></span> <span data-ttu-id="bb3eb-120">(日常の実行は制限されません。)</span><span class="sxs-lookup"><span data-stu-id="bb3eb-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="bb3eb-121">将来のビジネス成長によって計画のシステムが過負荷にならないこと。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="bb3eb-122">アーキテクチャとデータ フロー</span><span class="sxs-lookup"><span data-stu-id="bb3eb-122">Architecture and data flow</span></span>

<span data-ttu-id="bb3eb-123">LCS から計画の最適化アドインをインストールすると、計画の最適化サービスへの安全な接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="bb3eb-124">このサービスは、関連する Supply Chain Management インスタンスと同じデータ センターの国または地域にあります。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="bb3eb-125">計画の最適化が設定されたら、マスター プランの実行時に、マスター データおよびトランザクション データが Supply Chain Management から計画の最適化サービスに送信されます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="bb3eb-126">計画の最適化アドインをアンインストールすると、計画の最適化サービスに関連するすべてのデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="bb3eb-127">再生成実行のための高レベル データ フロー</span><span class="sxs-lookup"><span data-stu-id="bb3eb-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="bb3eb-128">Supply Chain Management クライアントは、計画の最適化から計画の実行を要求するためのシグナルを送信します。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="bb3eb-129">計画の最適化は、統合コネクタを介して必要なデータを要求します。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="bb3eb-130">SQL データベースはコネクタを介して、設定、マスター、およびトランザクションのデータについて要求された情報を、計画の最適化に送信します。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="bb3eb-131">コネクタは、Supply Chain Management と計画の最適化サービス間で情報を変換します。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="bb3eb-132">計画の最適化サービスでは、計画に関連するデータがメモリに保持され、必要な計算が行われます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="bb3eb-133">計画の結果は、コネクタを介して Supply Chain Management データベースに送信されます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="bb3eb-134">この結果には、計画オーダーやペギング情報などの情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="bb3eb-135">計画の最適化では、計画の実行が完了したことを示すシグナルが、Supply Chain Management に送信されます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="bb3eb-136">また、関連するメッセージおよび警告を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="bb3eb-137">次の図はデータ フローを示します。</span><span class="sxs-lookup"><span data-stu-id="bb3eb-137">The following illustration shows the data flow.</span></span>

![再生成実行のためのデータ フロー](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="bb3eb-139">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="bb3eb-139">Related resources</span></span>

[<span data-ttu-id="bb3eb-140">計画の最適化を開始する</span><span class="sxs-lookup"><span data-stu-id="bb3eb-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="bb3eb-141">計画の最適化フィット分析</span><span class="sxs-lookup"><span data-stu-id="bb3eb-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="bb3eb-142">計画の履歴と計画ログの表示</span><span class="sxs-lookup"><span data-stu-id="bb3eb-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="bb3eb-143">プランへのフィルターの適用</span><span class="sxs-lookup"><span data-stu-id="bb3eb-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="bb3eb-144">計画ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="bb3eb-144">Cancel a planning job</span></span>](cancel-planning-job.md)
