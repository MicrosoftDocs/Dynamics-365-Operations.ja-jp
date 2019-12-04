---
title: プランへのフィルターの適用
description: このトピックでは、計画の最適化機能の使用する場合、計画でフィルターを使用する方法について説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ff9c9f875368fcc4dd62b9c188d489e20a5c7960
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773999"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="1029f-103">プランへのフィルターの適用</span><span class="sxs-lookup"><span data-stu-id="1029f-103">Apply filters to a plan</span></span>

<span data-ttu-id="1029f-104">計画の最適化機能を使用する場合、計画にフィルターを適用できます。</span><span class="sxs-lookup"><span data-stu-id="1029f-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="1029f-105">計画フィルターは、常にマスター プランの実行中に適用されます。</span><span class="sxs-lookup"><span data-stu-id="1029f-105">The plan filter will always be applied during a master planning run.</span></span> <span data-ttu-id="1029f-106">計画フィルターは、計画を特定の品目のグループに制限し、結果のマスター プランの一部としてその他の品目が含まれないようにするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1029f-106">A plan filter is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="1029f-107">計画フィルターが適用され、マスター プランの実行中にランタイム フィルターも適用される場合、計画の実行には 2 つのフィルターの共通部分のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1029f-107">If a plan filter is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="1029f-108">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="1029f-108">Example scenario</span></span>

<span data-ttu-id="1029f-109">計画フィルターには品目 A、B、および C が含まれるよう設定されています。その後マスター プランの実行は同じ計画に対して実行されますが、異なるランタイム フィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="1029f-109">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="1029f-110">**品目 D を含むランタイム フィルター:** 計画フィルターおよびランタイム フィルター間に共通部分がないため、品目は計画されていません。</span><span class="sxs-lookup"><span data-stu-id="1029f-110">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="1029f-111">**品目 A および D を含むランタイム フィルター:** 品目 D は計画フィルターの一部ではないため、プランの実行では品目 A のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1029f-111">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="1029f-112">**品目 B を含むランタイム フィルター:** プランの実行には品目 B のみが含まれ、品目 A の以前の計画出力が保持されます。</span><span class="sxs-lookup"><span data-stu-id="1029f-112">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="1029f-113">**すべての品目を含むランタイム フィルター (空白フィルター):** プランの実行には項目 A、B、および C が含まれており、品目 A および B の計画出力は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="1029f-113">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="1029f-114">**マスター プラン パラメーター** ページで**現在の動的マスター プラン**として選択される計画には、計画フィルターを設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="1029f-114">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="1029f-115">そうしないと、動的マスター プラン機能は、フィルター処理された品目に制限されます。</span><span class="sxs-lookup"><span data-stu-id="1029f-115">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="1029f-116">たとえば、計画フィルターの一部でない品目に対して正味必要量が更新されると、結果は生成されません。</span><span class="sxs-lookup"><span data-stu-id="1029f-116">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="1029f-117">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="1029f-117">Related resources</span></span>

[<span data-ttu-id="1029f-118">計画の最適化の概要</span><span class="sxs-lookup"><span data-stu-id="1029f-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="1029f-119">計画の最適化を開始する</span><span class="sxs-lookup"><span data-stu-id="1029f-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="1029f-120">計画の最適化フィット分析</span><span class="sxs-lookup"><span data-stu-id="1029f-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="1029f-121">計画の履歴と計画ログの表示</span><span class="sxs-lookup"><span data-stu-id="1029f-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="1029f-122">計画ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="1029f-122">Cancel a planning job</span></span>](cancel-planning-job.md)
