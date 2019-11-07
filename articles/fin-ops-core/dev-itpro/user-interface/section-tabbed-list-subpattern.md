---
title: セクション タブ付きリストのサブパターン
description: この記事では、セクション タブ付きリストのサブパターンに関する情報を提供します。 このサブパターンは、それぞれにデータのフィルタ処理されたリストを含む垂直タブセットが入ったパノラマ セクション専用の、運用ワークスペース パターンの一部として使用されます。
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
ms.custom: 29291
ms.assetid: 3f8b00ff-54f0-4e32-bd7f-b94a74785537
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3855a2d9f7cbcee8c11ef4eb5a720378d4bacb6
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658826"
---
# <a name="section-tabbed-list-subpattern"></a><span data-ttu-id="123d8-104">セクション タブ付きリストのサブパターン</span><span class="sxs-lookup"><span data-stu-id="123d8-104">Section Tabbed List subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="123d8-105">この記事では、セクション タブ付きリストのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="123d8-105">This article provides information about the Section Tabbed List subpattern.</span></span> <span data-ttu-id="123d8-106">このサブパターンは、それぞれにデータのフィルタ処理されたリストを含む垂直タブセットが入ったパノラマ セクション専用の、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="123d8-106">This subpattern is used as part of the Operational Workspace pattern, specifically for a panorama section that contains a set of vertical tabs, each of which contains a filtered list of data.</span></span>

<a name="usage"></a><span data-ttu-id="123d8-107">用途</span><span class="sxs-lookup"><span data-stu-id="123d8-107">Usage</span></span>
-----

<span data-ttu-id="123d8-108">セクション タブ付きリストのサブパターンは、それぞれにデータのフィルタ処理されたリストを含む垂直タブセットが入ったパノラマ セクション専用の、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="123d8-108">The Section Tabbed List subpattern is used as part of the Operational Workspace pattern, specifically for a panorama section that contains a set of vertical tabs, each of which contains a filtered list of data.</span></span>

## <a name="wireframe"></a><span data-ttu-id="123d8-109">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="123d8-109">Wireframe</span></span>
<span data-ttu-id="123d8-110">[![セクション タブ付きリストのワイヤーフレーム](./media/sectiontabbedlistwireframe.png)](./media/sectiontabbedlistwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="123d8-110">[![Section Tabbed List wireframe](./media/sectiontabbedlistwireframe.png)](./media/sectiontabbedlistwireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="123d8-111">Microsoft Dynamics AX 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="123d8-111">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="123d8-112">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="123d8-112">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="123d8-113">モデル</span><span class="sxs-lookup"><span data-stu-id="123d8-113">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="123d8-114">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="123d8-114">High-level structure</span></span>

- <span data-ttu-id="123d8-115">TabPage</span><span class="sxs-lookup"><span data-stu-id="123d8-115">TabPage</span></span>
- <span data-ttu-id="123d8-116">TabbedList (タブ) (Style=VerticalTabs)</span><span class="sxs-lookup"><span data-stu-id="123d8-116">TabbedList (Tab) (Style=VerticalTabs)</span></span>

    - <span data-ttu-id="123d8-117">*TabbedListPage (TabPage)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="123d8-117">*TabbedListPage (TabPage) \[0..N\]*</span></span>

        - <span data-ttu-id="123d8-118">TargetForm (FormPart)</span><span class="sxs-lookup"><span data-stu-id="123d8-118">TargetForm (FormPart)</span></span>

<span data-ttu-id="123d8-119">各フォーム パーツでは、セクションの内容を含むフォームを指します。</span><span class="sxs-lookup"><span data-stu-id="123d8-119">Each Form Part points to a form that contains the content for the section.</span></span> <span data-ttu-id="123d8-120">これらのフォームはそれぞれ、Form Part Section List フォーム パターンの 1 つを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="123d8-120">Each of these forms should use one of the Form Part Section List form patterns.</span></span>

### <a name="core-components"></a><span data-ttu-id="123d8-121">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="123d8-121">Core components</span></span>

<span data-ttu-id="123d8-122">セクション タブ付きリストをワークスペース内の適切なタブ ページに適用します。</span><span class="sxs-lookup"><span data-stu-id="123d8-122">Apply Section Tabbed List to the appropriate tab page in the workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="123d8-123">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="123d8-123">Related container patterns</span></span>

-   [<span data-ttu-id="123d8-124">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="123d8-124">Operational Workspace</span></span>](workspace-form-pattern.md)
-   [<span data-ttu-id="123d8-125">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="123d8-125">Form Part Section List</span></span>](section-list-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="123d8-126">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="123d8-126">UX guidelines</span></span>
<span data-ttu-id="123d8-127">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="123d8-127">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="123d8-128">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="123d8-128">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="123d8-129">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="123d8-129">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="123d8-130">少なくとも 1 つのリストはタブ付きリストのセクション内に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="123d8-130">At least one list should be present in the tabbed list section.</span></span>
-   <span data-ttu-id="123d8-131">各フォーム パーツ コントロールでは、いずれかの[フォーム パーツ セクション リスト](section-list-form-pattern.md)パターンを使用するフォームを指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="123d8-131">Each Form Part Control should point to a form that uses one of the [Form Part Section List](section-list-form-pattern.md) patterns.</span></span>

## <a name="examples"></a><span data-ttu-id="123d8-132">例</span><span class="sxs-lookup"><span data-stu-id="123d8-132">Examples</span></span>
<span data-ttu-id="123d8-133">フォーム: **PurchOrderMaintainWorkspace** (**すべてのワークスペース** &gt; **発注書の準備**)</span><span class="sxs-lookup"><span data-stu-id="123d8-133">Form: **PurchOrderMaintainWorkspace** (**All workspaces** &gt; **Purchase order preparation**)</span></span> 

<span data-ttu-id="123d8-134">[![タブ付きリストのセクションの例](./media/tabbedlistsectionexample.png)](./media/tabbedlistsectionexample.png)</span><span class="sxs-lookup"><span data-stu-id="123d8-134">[![Tabbed List Section example](./media/tabbedlistsectionexample.png)](./media/tabbedlistsectionexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="123d8-135">付録</span><span class="sxs-lookup"><span data-stu-id="123d8-135">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="123d8-136">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="123d8-136">Frequently asked questions</span></span>

<span data-ttu-id="123d8-137">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="123d8-137">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="123d8-138">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="123d8-138">Open issues</span></span>

<span data-ttu-id="123d8-139">None</span><span class="sxs-lookup"><span data-stu-id="123d8-139">None</span></span>
