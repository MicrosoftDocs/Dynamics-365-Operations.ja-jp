---
title: セクション タイルのサブパターン
description: この記事では、セクション タイルのサブパターンに関する情報を提供します。 このサブパターンは、タイル、グラフ、および単一カードのセットを含む最初のパノラマ セクション (概要セクション) 専用の、運用ワークスペース パターンの一部として使用されます。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 29311
ms.assetid: 196e714a-ecfc-42b3-a7f5-84e29fb271bb
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e5a9cf358bd3b751680be0953cbe866c7c39ffe
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658827"
---
# <a name="section-tiles-subpattern"></a><span data-ttu-id="aa01f-104">セクション タイルのサブパターン</span><span class="sxs-lookup"><span data-stu-id="aa01f-104">Section Tiles subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa01f-105">この記事では、セクション タイルのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="aa01f-105">This article provides information about the Section Tiles subpattern.</span></span> <span data-ttu-id="aa01f-106">このサブパターンは、タイル、グラフ、および単一カードのセットを含む最初のパノラマ セクション (概要セクション) 専用の、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa01f-106">This subpattern is used as part of the Operational Workspace pattern, specifically for the first panorama section (the Summary section) that contains a set of tiles, charts, and singleton cards.</span></span> 

<a name="usage"></a><span data-ttu-id="aa01f-107">用途</span><span class="sxs-lookup"><span data-stu-id="aa01f-107">Usage</span></span>
-----

<span data-ttu-id="aa01f-108">セクション タイル サブパターンは、タイル、グラフ、および単一カードのセットを含む最初のパノラマ セクション (**概要** セクション) 専用の、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa01f-108">The Section Tiles subpattern is used as part of the Operational Workspace pattern, specifically for the first panorama section (the **Summary** section) that contains a set of tiles, charts, and singleton cards.</span></span>

## <a name="wireframe"></a><span data-ttu-id="aa01f-109">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="aa01f-109">Wireframe</span></span>
<span data-ttu-id="aa01f-110">[![セクション タイルのワイヤーフレーム](./media/sectiontileswireframe.png)](./media/sectiontileswireframe.png)</span><span class="sxs-lookup"><span data-stu-id="aa01f-110">[![Wireframe for Section Tiles](./media/sectiontileswireframe.png)](./media/sectiontileswireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="aa01f-111">Microsoft Dynamics AX 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="aa01f-111">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="aa01f-112">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="aa01f-112">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="aa01f-113">モデル</span><span class="sxs-lookup"><span data-stu-id="aa01f-113">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="aa01f-114">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="aa01f-114">High-level structure</span></span>

- <span data-ttu-id="aa01f-115">TabPage</span><span class="sxs-lookup"><span data-stu-id="aa01f-115">TabPage</span></span>

    - <span data-ttu-id="aa01f-116">*TileButton (TileButton)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="aa01f-116">*TileButton (TileButton) \[0..N\]*</span></span>
    - <span data-ttu-id="aa01f-117">*TargetForm (FormPart)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="aa01f-117">*TargetForm (FormPart) \[0..N\]*</span></span>

<span data-ttu-id="aa01f-118">フォーム パーツは、グラフまたは単一のカードをワークスペースの **集計** セクションに埋め込むために使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa01f-118">The Form Parts are used to embed Charts or singleton Cards into the **Summary** section of the workspace.</span></span> <span data-ttu-id="aa01f-119">グラフを表す各フォームでは、[セクション チャート](section-chart-form-pattern.md)フォーム パターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa01f-119">Each form that represents a Chart should use the [Section Chart](section-chart-form-pattern.md) form pattern.</span></span>

### <a name="core-components"></a><span data-ttu-id="aa01f-120">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="aa01f-120">Core components</span></span>

<span data-ttu-id="aa01f-121">セクション タイルを運用ワークスペース内の最初のタブ ページに適用します。</span><span class="sxs-lookup"><span data-stu-id="aa01f-121">Apply Section Tiles to the first tab page in the Operational Workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="aa01f-122">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="aa01f-122">Related container patterns</span></span>

-   [<span data-ttu-id="aa01f-123">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="aa01f-123">Operational Workspace</span></span>](workspace-form-pattern.md)
-   [<span data-ttu-id="aa01f-124">セクション グラフ</span><span class="sxs-lookup"><span data-stu-id="aa01f-124">Section Chart</span></span>](section-chart-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="aa01f-125">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="aa01f-125">UX guidelines</span></span>
<span data-ttu-id="aa01f-126">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="aa01f-126">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="aa01f-127">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="aa01f-127">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="aa01f-128">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="aa01f-128">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="aa01f-129">**集計** セクションは、「集計」という名前にするか、"Summary" という語を修飾するバリアントにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa01f-129">The **Summary** section should be named "Summary" or a variant that qualifies the word “Summary.”</span></span>
-   <span data-ttu-id="aa01f-130">ワークスペースの 2 つのタイルに、同じ記号がある必要はありません。</span><span class="sxs-lookup"><span data-stu-id="aa01f-130">No two tiles in the workspace should have the same symbol.</span></span>
-   <span data-ttu-id="aa01f-131">最大 1 つの「新しい」タイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="aa01f-131">There should be a maximum of one "New" tile.</span></span>
-   <span data-ttu-id="aa01f-132">グラフのサイズは、タイル サイズの倍数に対応する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa01f-132">Chart sizes should correspond to multiples of tile sizes.</span></span>
    -   <span data-ttu-id="aa01f-133">使用可能なサイズには縦 1 タイル × 横 2 タイル、2 × 2、2 × 3、2 × 4、2 × 6、4 × 4、4 × 6 および 4 × 8 が含まれます。</span><span class="sxs-lookup"><span data-stu-id="aa01f-133">Available sizes include 1 tile tall × 2 tiles wide, 2 × 2, 2 × 3, 2 × 4, 2 × 6, 4 × 4, 4 × 6, and 4 × 8.</span></span>

## <a name="examples"></a><span data-ttu-id="aa01f-134">例</span><span class="sxs-lookup"><span data-stu-id="aa01f-134">Examples</span></span>
<span data-ttu-id="aa01f-135">フォーム: **PurchOrderMaintainWorkspace** (**すべてのワークスペース** &gt; **発注書の準備** (**集計**セクションを参照してください)</span><span class="sxs-lookup"><span data-stu-id="aa01f-135">Form: **PurchOrderMaintainWorkspace** (**All workspaces** &gt; **Purchase order preparation** (see the **Summary** section)</span></span>

<span data-ttu-id="aa01f-136">[![セクション タイルの例](./media/sectiontilesexample.png)](./media/sectiontilesexample.png)</span><span class="sxs-lookup"><span data-stu-id="aa01f-136">[![Section Tiles example](./media/sectiontilesexample.png)](./media/sectiontilesexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="aa01f-137">付録</span><span class="sxs-lookup"><span data-stu-id="aa01f-137">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="aa01f-138">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="aa01f-138">Frequently asked questions</span></span>

<span data-ttu-id="aa01f-139">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="aa01f-139">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="aa01f-140">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="aa01f-140">Open issues</span></span>

<span data-ttu-id="aa01f-141">None</span><span class="sxs-lookup"><span data-stu-id="aa01f-141">None</span></span>
