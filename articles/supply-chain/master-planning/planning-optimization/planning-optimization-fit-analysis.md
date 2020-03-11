---
title: 計画の最適化フィット分析
description: このトピックでは、計画の最適化機能の能力に対して、現在の設定およびデータを検証する方法について説明します。
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
ms.openlocfilehash: 25f3b39d0e6e88eb3f042ab93773e9724528ab0f
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076181"
---
# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="e549f-103">計画の最適化フィット分析</span><span class="sxs-lookup"><span data-stu-id="e549f-103">Planning Optimization fit analysis</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e549f-104">現在の設定およびデータと計画の最適化機能との互換性を確認するには、**マスター プラン** \> **設定** \> **計画の最適化フィット分析**の順に移動してから、**分析の実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e549f-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="e549f-105">分析で不整合が見つかった場合は、同じページに一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="e549f-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="e549f-106">(分析を実行するには数分かかります。)</span><span class="sxs-lookup"><span data-stu-id="e549f-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="e549f-107">不整合が見つかった場合でも、計画の最適化を引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="e549f-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="e549f-108">フィット分析の結果は、計画サービスが現在の設定を遵守しない箇所を示しているだけです。</span><span class="sxs-lookup"><span data-stu-id="e549f-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="e549f-109">つまり、一部のプロセスが無視される、またはサポートされない可能性がある場所を示します。</span><span class="sxs-lookup"><span data-stu-id="e549f-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="e549f-110">分析結果: 例 1</span><span class="sxs-lookup"><span data-stu-id="e549f-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="e549f-111">**機能:** 生産</span><span class="sxs-lookup"><span data-stu-id="e549f-111">**Feature:** Production</span></span>
- <span data-ttu-id="e549f-112">**問題:** BOM レベルがゼロより大きい品目: 56</span><span class="sxs-lookup"><span data-stu-id="e549f-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="e549f-113">**説明:** フィット分析で、生産の部品表 (BOM) 設定がある 56 品目が見つかりました。</span><span class="sxs-lookup"><span data-stu-id="e549f-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="e549f-114">計画の最適化の現在のバージョンは生産をサポートしていないため、計画の最適化では計画製造オーダーではなく計画発注書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="e549f-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="e549f-115">また、影響を受ける品目を一覧表示する警告も表示されます。</span><span class="sxs-lookup"><span data-stu-id="e549f-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="e549f-116">分析結果: 例 2</span><span class="sxs-lookup"><span data-stu-id="e549f-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="e549f-117">**機能:** アクション</span><span class="sxs-lookup"><span data-stu-id="e549f-117">**Feature:** Actions</span></span>
- <span data-ttu-id="e549f-118">**問題:** アクション計算が有効な補充グループ: 6</span><span class="sxs-lookup"><span data-stu-id="e549f-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="e549f-119">**説明:** フィット分析で、アクション計算が有効になっている 6 つの補充グループが見つかりました。</span><span class="sxs-lookup"><span data-stu-id="e549f-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="e549f-120">計画の最適化の現在のバージョンではアクションがサポートされていないため、マスター プラン中にアクションが生成されることはありません。</span><span class="sxs-lookup"><span data-stu-id="e549f-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="e549f-121">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="e549f-121">Related resources</span></span>

[<span data-ttu-id="e549f-122">計画の最適化の概要</span><span class="sxs-lookup"><span data-stu-id="e549f-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="e549f-123">計画の最適化を開始する</span><span class="sxs-lookup"><span data-stu-id="e549f-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="e549f-124">計画の履歴と計画ログの表示</span><span class="sxs-lookup"><span data-stu-id="e549f-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="e549f-125">プランへのフィルターの適用</span><span class="sxs-lookup"><span data-stu-id="e549f-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="e549f-126">計画ジョブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="e549f-126">Cancel a planning job</span></span>](cancel-planning-job.md)
