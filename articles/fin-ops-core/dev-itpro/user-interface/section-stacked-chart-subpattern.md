---
title: セクション積み上げグラフのサブパターン
description: この記事では、セクション積み上げグラフのサブパターンに関する情報を提供します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29251
ms.assetid: 58fea559-4d50-46f3-9a88-4cca1d882d04
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8f316f174a7048370679431bde65b003ec231bb
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092367"
---
# <a name="section-stacked-chart-subpattern"></a><span data-ttu-id="22772-103">セクション積み上げグラフのサブパターン</span><span class="sxs-lookup"><span data-stu-id="22772-103">Section Stacked Chart subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22772-104">この記事では、セクション積み上げグラフのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="22772-104">This article provides information about the Section Stacked Chart subpattern.</span></span> <span data-ttu-id="22772-105">このサブパターンは、パノラマ セクションに 1 つまたは 2 つのグラフが含まれているとき、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="22772-105">This subpattern is used as part of the Operational Workspace pattern when a panorama section contains one or two charts.</span></span>  

<a name="usage"></a><span data-ttu-id="22772-106">用途</span><span class="sxs-lookup"><span data-stu-id="22772-106">Usage</span></span>
-----

<span data-ttu-id="22772-107">セクション積み上げグラフのサブパターンは、1 つ以上のグラフを含むパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="22772-107">The Section Stacked Chart subpattern is used as part of the Operational Workspace pattern, specifically for a panorama section that contains one or two charts.</span></span>

## <a name="wireframe"></a><span data-ttu-id="22772-108">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="22772-108">Wireframe</span></span>
<span data-ttu-id="22772-109">[![セクション積み上げグラフのワイヤーフレーム](./media/sectionstackedchartwireframe.png)](./media/sectionstackedchartwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="22772-109">[![Wireframe for Section Stacked Chart](./media/sectionstackedchartwireframe.png)](./media/sectionstackedchartwireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="22772-110">Microsoft Dynamics AX 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="22772-110">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="22772-111">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="22772-111">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="22772-112">モデル</span><span class="sxs-lookup"><span data-stu-id="22772-112">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="22772-113">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="22772-113">High-level structure</span></span>

- <span data-ttu-id="22772-114">TabPage</span><span class="sxs-lookup"><span data-stu-id="22772-114">TabPage</span></span>

    - <span data-ttu-id="22772-115">*ChartPart (FormPart)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="22772-115">*ChartPart (FormPart) \[0..N\]*</span></span>

<span data-ttu-id="22772-116">各フォーム パーツでは、単一のグラフを含むフォームを指します。</span><span class="sxs-lookup"><span data-stu-id="22772-116">Each Form Part points to a form that contains a single chart.</span></span> <span data-ttu-id="22772-117">これらのフォームはそれぞれ、[セクション グラフ](section-chart-form-pattern.md)フォーム パターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22772-117">Each of these forms should use the [Section Chart](section-chart-form-pattern.md) form pattern.</span></span>

### <a name="core-components"></a><span data-ttu-id="22772-118">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="22772-118">Core components</span></span>

<span data-ttu-id="22772-119">セクション積み上げグラフをワークスペース内の適切なタブ ページに適用します。</span><span class="sxs-lookup"><span data-stu-id="22772-119">Apply Section Stacked Chart to the appropriate tab page in the workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="22772-120">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="22772-120">Related container patterns</span></span>

-   [<span data-ttu-id="22772-121">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="22772-121">Operational workspace</span></span>](workspace-form-pattern.md)
-   [<span data-ttu-id="22772-122">セクション グラフ</span><span class="sxs-lookup"><span data-stu-id="22772-122">Section Chart</span></span>](section-chart-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="22772-123">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="22772-123">UX guidelines</span></span>
<span data-ttu-id="22772-124">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="22772-124">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="22772-125">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="22772-125">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="22772-126">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="22772-126">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="22772-127">このセクションには、グラフを 2 つ以下にしてください。</span><span class="sxs-lookup"><span data-stu-id="22772-127">There should be no more than two charts in this section.</span></span>
-   <span data-ttu-id="22772-128">各フォーム パーツ コントロールでは、[セクション グラフ](section-chart-form-pattern.md)パターンを使用するフォームを指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="22772-128">Each Form Part Control should point to a form that uses the [Section Chart](section-chart-form-pattern.md) pattern.</span></span>

## <a name="examples"></a><span data-ttu-id="22772-129">例</span><span class="sxs-lookup"><span data-stu-id="22772-129">Examples</span></span>
<span data-ttu-id="22772-130">フォーム: **FmClerkWorkspace** (**すべてのワークスペース** &gt; **予約管理**)</span><span class="sxs-lookup"><span data-stu-id="22772-130">Form: **FmClerkWorkspace** (**All workspaces** &gt; **Reservation Management**)</span></span> 

<span data-ttu-id="22772-131">[![セクション積み上げグラフの例](./media/sectionstackedchartexample.png)](./media/sectionstackedchartexample.png)</span><span class="sxs-lookup"><span data-stu-id="22772-131">[![Section Stacked Chart example](./media/sectionstackedchartexample.png)](./media/sectionstackedchartexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="22772-132">付録</span><span class="sxs-lookup"><span data-stu-id="22772-132">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="22772-133">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="22772-133">Frequently asked questions</span></span>

<span data-ttu-id="22772-134">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="22772-134">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="22772-135">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="22772-135">Open issues</span></span>

<span data-ttu-id="22772-136">None</span><span class="sxs-lookup"><span data-stu-id="22772-136">None</span></span>
