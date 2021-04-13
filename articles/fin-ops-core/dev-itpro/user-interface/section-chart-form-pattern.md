---
title: セクション グラフのフォーム パターン
description: このトピックでは、セクション グラフのフォーム パターンに関する情報を提供します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29271
ms.assetid: 049887b5-6277-4902-96ec-a81a3d2348c3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da931ce1d6740ac498f7e742c66a38f40875e338
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750246"
---
# <a name="section-chart-form-pattern"></a><span data-ttu-id="2f35a-103">セクション グラフのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="2f35a-103">Section Chart form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f35a-104">このトピックでは、セクション グラフのフォーム パターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="2f35a-104">This topic provides information about the Section Chart form pattern.</span></span> <span data-ttu-id="2f35a-105">このパターンは主に、作業ワークスペース パターンと組み合わせて使用されます。特に、チャート コントロールを含むフォームに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2f35a-105">This pattern is primarily used in conjunction with the Operational Workspace pattern, and specifically on forms that contain a chart control.</span></span>

<a name="usage"></a><span data-ttu-id="2f35a-106">用途</span><span class="sxs-lookup"><span data-stu-id="2f35a-106">Usage</span></span>
-----

<span data-ttu-id="2f35a-107">セクション グラフ フォーム パターンは、主に運用ワークスペース パターンと組み合わせて使用することを意図しています。</span><span class="sxs-lookup"><span data-stu-id="2f35a-107">The Section Chart form pattern is intended to be used primarily in conjunction with the Operational Workspace pattern.</span></span> <span data-ttu-id="2f35a-108">具体的には、グラフ セクションまたは集計セクションに、グラフが含まれるフォームをポイントするフォーム パーツ コントロールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2f35a-108">Specifically, the chart section or summary section contains Form Part Controls that point to forms that contain charts.</span></span> <span data-ttu-id="2f35a-109">これらの参照されるフォームは、セクション グラフ パターンを使用することを意図しています。</span><span class="sxs-lookup"><span data-stu-id="2f35a-109">These referenced forms are intended to use the Section Chart pattern.</span></span>

## <a name="wireframe"></a><span data-ttu-id="2f35a-110">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="2f35a-110">Wireframe</span></span>
<span data-ttu-id="2f35a-111">[![セクション グラフのフォーム パターンのワイヤーフレーム](./media/sectionchartwireframe1.png)](./media/sectionchartwireframe1.png)</span><span class="sxs-lookup"><span data-stu-id="2f35a-111">[![Wireframe for Section Chart form pattern](./media/sectionchartwireframe1.png)](./media/sectionchartwireframe1.png)</span></span>

## <a name="pattern-changes-for-finance-and-operations"></a><span data-ttu-id="2f35a-112">Finance and Operations 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="2f35a-112">Pattern changes for Finance and Operations</span></span>
<span data-ttu-id="2f35a-113">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="2f35a-113">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="2f35a-114">モデル</span><span class="sxs-lookup"><span data-stu-id="2f35a-114">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="2f35a-115">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="2f35a-115">High-level structure</span></span>

- <span data-ttu-id="2f35a-116">フォーム デザイン</span><span class="sxs-lookup"><span data-stu-id="2f35a-116">Form Design</span></span>

    - <span data-ttu-id="2f35a-117">*HeaderGroup (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f35a-117">*HeaderGroup (Group) \[Optional\]* – This uses one of the [Filters and Toolbar](filters-toolbar-subpattern.md) subpatterns.</span></span>
    - <span data-ttu-id="2f35a-118">グラフ</span><span class="sxs-lookup"><span data-stu-id="2f35a-118">Chart</span></span>

### <a name="core-components"></a><span data-ttu-id="2f35a-119">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="2f35a-119">Core components</span></span>

<span data-ttu-id="2f35a-120">セクション グラフ パターンを適切なフォーム/コンテナーに適用します。</span><span class="sxs-lookup"><span data-stu-id="2f35a-120">Apply the Section Chart pattern to the appropriate form/container.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="2f35a-121">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="2f35a-121">Related container patterns</span></span>

-   [<span data-ttu-id="2f35a-122">ワークスペース</span><span class="sxs-lookup"><span data-stu-id="2f35a-122">Workspace</span></span>](workspace-form-pattern.md)
-   [<span data-ttu-id="2f35a-123">セクション積み上げグラフ</span><span class="sxs-lookup"><span data-stu-id="2f35a-123">Section stacked chart</span></span>](section-stacked-chart-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="2f35a-124">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="2f35a-124">UX guidelines</span></span>
<span data-ttu-id="2f35a-125">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="2f35a-125">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="2f35a-126">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="2f35a-126">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="2f35a-127">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="2f35a-127">Open the form in the browser, and walk through these steps.</span></span> <span data-ttu-id="2f35a-128">None</span><span class="sxs-lookup"><span data-stu-id="2f35a-128">None</span></span>

## <a name="examples"></a><span data-ttu-id="2f35a-129">例</span><span class="sxs-lookup"><span data-stu-id="2f35a-129">Examples</span></span>
<span data-ttu-id="2f35a-130">フォーム: **FmBiChartPart\_VehicleByModel** (**すべてのワークスペース** &gt; **予約管理** (**統計** セクションを参照してください)</span><span class="sxs-lookup"><span data-stu-id="2f35a-130">Form: **FmBiChartPart\_VehicleByModel** (**All workspaces** &gt; **Reservation Management** (see the **Statistics** section)</span></span> 

<span data-ttu-id="2f35a-131">[![セクション グラフのフォーム パターンの例](./media/sectionchartexample.png)](./media/sectionchartexample.png)</span><span class="sxs-lookup"><span data-stu-id="2f35a-131">[![Example of Section Chart form pattern](./media/sectionchartexample.png)](./media/sectionchartexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="2f35a-132">付録</span><span class="sxs-lookup"><span data-stu-id="2f35a-132">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="2f35a-133">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="2f35a-133">Frequently asked questions</span></span>

<span data-ttu-id="2f35a-134">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="2f35a-134">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="2f35a-135">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="2f35a-135">Open issues</span></span>

<span data-ttu-id="2f35a-136">None</span><span class="sxs-lookup"><span data-stu-id="2f35a-136">None</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]