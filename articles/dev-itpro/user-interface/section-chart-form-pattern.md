---
title: セクション グラフのフォーム パターン
description: この記事では、セクション グラフのフォーム パターンに関する情報を提供します。 このパターンは主に、作業ワークスペース パターンと組み合わせて使用されます。特に、チャート コントロールを含むフォームに使用されます。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 29271
ms.assetid: 049887b5-6277-4902-96ec-a81a3d2348c3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 654fc486251d818aee5894fc70d80a5d3cdee766
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537479"
---
# <a name="section-chart-form-pattern"></a><span data-ttu-id="ff3a7-104">セクション グラフのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="ff3a7-104">Section Chart form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff3a7-105">この記事では、セクション グラフのフォーム パターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-105">This article provides information about the Section Chart form pattern.</span></span> <span data-ttu-id="ff3a7-106">このパターンは主に、作業ワークスペース パターンと組み合わせて使用されます。特に、チャート コントロールを含むフォームに使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-106">This pattern is primarily used in conjunction with the Operational Workspace pattern, and specifically on forms that contain a chart control.</span></span>

<a name="usage"></a><span data-ttu-id="ff3a7-107">用途</span><span class="sxs-lookup"><span data-stu-id="ff3a7-107">Usage</span></span>
-----

<span data-ttu-id="ff3a7-108">セクション グラフ フォーム パターンは、主に運用ワークスペース パターンと組み合わせて使用することを意図しています。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-108">The Section Chart form pattern is intended to be used primarily in conjunction with the Operational Workspace pattern.</span></span> <span data-ttu-id="ff3a7-109">具体的には、グラフ セクションまたは集計セクションに、グラフが含まれるフォームをポイントするフォーム パーツ コントロールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-109">Specifically, the chart section or summary section contains Form Part Controls that point to forms that contain charts.</span></span> <span data-ttu-id="ff3a7-110">これらの参照されるフォームは、セクション グラフ パターンを使用することを意図しています。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-110">These referenced forms are intended to use the Section Chart pattern.</span></span>

## <a name="wireframe"></a><span data-ttu-id="ff3a7-111">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="ff3a7-111">Wireframe</span></span>
<span data-ttu-id="ff3a7-112">[![sectionChartWireframe](./media/sectionchartwireframe1.png)](./media/sectionchartwireframe1.png)</span><span class="sxs-lookup"><span data-stu-id="ff3a7-112">[![sectionChartWireframe](./media/sectionchartwireframe1.png)](./media/sectionchartwireframe1.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="ff3a7-113">Microsoft Dynamics 365 for Finance and Operations 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="ff3a7-113">Pattern changes for Microsoft Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="ff3a7-114">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-114">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="ff3a7-115">モデル</span><span class="sxs-lookup"><span data-stu-id="ff3a7-115">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="ff3a7-116">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="ff3a7-116">High-level structure</span></span>

- <span data-ttu-id="ff3a7-117">フォーム デザイン</span><span class="sxs-lookup"><span data-stu-id="ff3a7-117">Form Design</span></span>

    - <span data-ttu-id="ff3a7-118">*HeaderGroup (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-118">*HeaderGroup (Group) \[Optional\]* – This uses one of the [Filters and Toolbar](filters-toolbar-subpattern.md) subpatterns.</span></span>
    - <span data-ttu-id="ff3a7-119">グラフ</span><span class="sxs-lookup"><span data-stu-id="ff3a7-119">Chart</span></span>

### <a name="core-components"></a><span data-ttu-id="ff3a7-120">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ff3a7-120">Core components</span></span>

<span data-ttu-id="ff3a7-121">セクション グラフ パターンを適切なフォーム/コンテナーに適用します。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-121">Apply the Section Chart pattern to the appropriate form/container.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="ff3a7-122">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="ff3a7-122">Related container patterns</span></span>

-   [<span data-ttu-id="ff3a7-123">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="ff3a7-123">Operational workspace</span></span>](workspace-form-pattern.md)
-   [<span data-ttu-id="ff3a7-124">セクション積み上げグラフ</span><span class="sxs-lookup"><span data-stu-id="ff3a7-124">Section stacked chart</span></span>](section-stacked-chart-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="ff3a7-125">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="ff3a7-125">UX guidelines</span></span>
<span data-ttu-id="ff3a7-126">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-126">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="ff3a7-127">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-127">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="ff3a7-128">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-128">Open the form in the browser, and walk through these steps.</span></span> <span data-ttu-id="ff3a7-129">None</span><span class="sxs-lookup"><span data-stu-id="ff3a7-129">None</span></span>

## <a name="examples"></a><span data-ttu-id="ff3a7-130">例</span><span class="sxs-lookup"><span data-stu-id="ff3a7-130">Examples</span></span>
<span data-ttu-id="ff3a7-131">フォーム: **FmBiChartPart\_VehicleByModel** (**すべてのワークスペース** &gt; **予約管理** (**統計**セクションを参照してください)</span><span class="sxs-lookup"><span data-stu-id="ff3a7-131">Form: **FmBiChartPart\_VehicleByModel** (**All workspaces** &gt; **Reservation Management** (see the **Statistics** section)</span></span> 

<span data-ttu-id="ff3a7-132">[![sectionChartExample](./media/sectionchartexample.png)](./media/sectionchartexample.png)</span><span class="sxs-lookup"><span data-stu-id="ff3a7-132">[![sectionChartExample](./media/sectionchartexample.png)](./media/sectionchartexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="ff3a7-133">付録</span><span class="sxs-lookup"><span data-stu-id="ff3a7-133">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="ff3a7-134">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ff3a7-134">Frequently asked questions</span></span>

<span data-ttu-id="ff3a7-135">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="ff3a7-135">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="ff3a7-136">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="ff3a7-136">Open issues</span></span>

<span data-ttu-id="ff3a7-137">None</span><span class="sxs-lookup"><span data-stu-id="ff3a7-137">None</span></span>
