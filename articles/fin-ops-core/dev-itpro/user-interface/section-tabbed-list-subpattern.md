---
title: セクション タブ付きリストのサブパターン
description: この記事では、セクション タブ付きリストのサブパターンに関する情報を提供します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29291
ms.assetid: 3f8b00ff-54f0-4e32-bd7f-b94a74785537
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0acd4f6a91c8a3cc3edfea14ac7a153a8c1d638f
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092444"
---
# <a name="section-tabbed-list-subpattern"></a><span data-ttu-id="7aa54-103">セクション タブ付きリストのサブパターン</span><span class="sxs-lookup"><span data-stu-id="7aa54-103">Section Tabbed List subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7aa54-104">この記事では、セクション タブ付きリストのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="7aa54-104">This article provides information about the Section Tabbed List subpattern.</span></span> <span data-ttu-id="7aa54-105">このサブパターンは、それぞれにデータのフィルタ処理されたリストを含む垂直タブセットが入ったパノラマ セクション専用の、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="7aa54-105">This subpattern is used as part of the Operational Workspace pattern, specifically for a panorama section that contains a set of vertical tabs, each of which contains a filtered list of data.</span></span>

<a name="usage"></a><span data-ttu-id="7aa54-106">用途</span><span class="sxs-lookup"><span data-stu-id="7aa54-106">Usage</span></span>
-----

<span data-ttu-id="7aa54-107">セクション タブ付きリストのサブパターンは、それぞれにデータのフィルタ処理されたリストを含む垂直タブセットが入ったパノラマ セクション専用の、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="7aa54-107">The Section Tabbed List subpattern is used as part of the Operational Workspace pattern, specifically for a panorama section that contains a set of vertical tabs, each of which contains a filtered list of data.</span></span>

## <a name="wireframe"></a><span data-ttu-id="7aa54-108">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="7aa54-108">Wireframe</span></span>
<span data-ttu-id="7aa54-109">[![セクション タブ付きリストのワイヤーフレーム](./media/sectiontabbedlistwireframe.png)](./media/sectiontabbedlistwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="7aa54-109">[![Section Tabbed List wireframe](./media/sectiontabbedlistwireframe.png)](./media/sectiontabbedlistwireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="7aa54-110">Microsoft Dynamics AX 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="7aa54-110">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="7aa54-111">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="7aa54-111">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="7aa54-112">モデル</span><span class="sxs-lookup"><span data-stu-id="7aa54-112">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="7aa54-113">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="7aa54-113">High-level structure</span></span>

- <span data-ttu-id="7aa54-114">TabPage</span><span class="sxs-lookup"><span data-stu-id="7aa54-114">TabPage</span></span>
- <span data-ttu-id="7aa54-115">TabbedList (タブ) (Style=VerticalTabs)</span><span class="sxs-lookup"><span data-stu-id="7aa54-115">TabbedList (Tab) (Style=VerticalTabs)</span></span>

    - <span data-ttu-id="7aa54-116">*TabbedListPage (TabPage)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="7aa54-116">*TabbedListPage (TabPage) \[0..N\]*</span></span>

        - <span data-ttu-id="7aa54-117">TargetForm (FormPart)</span><span class="sxs-lookup"><span data-stu-id="7aa54-117">TargetForm (FormPart)</span></span>

<span data-ttu-id="7aa54-118">各フォーム パーツでは、セクションの内容を含むフォームを指します。</span><span class="sxs-lookup"><span data-stu-id="7aa54-118">Each Form Part points to a form that contains the content for the section.</span></span> <span data-ttu-id="7aa54-119">これらのフォームはそれぞれ、Form Part Section List フォーム パターンの 1 つを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7aa54-119">Each of these forms should use one of the Form Part Section List form patterns.</span></span>

### <a name="core-components"></a><span data-ttu-id="7aa54-120">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="7aa54-120">Core components</span></span>

<span data-ttu-id="7aa54-121">セクション タブ付きリストをワークスペース内の適切なタブ ページに適用します。</span><span class="sxs-lookup"><span data-stu-id="7aa54-121">Apply Section Tabbed List to the appropriate tab page in the workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="7aa54-122">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="7aa54-122">Related container patterns</span></span>

-   [<span data-ttu-id="7aa54-123">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="7aa54-123">Operational Workspace</span></span>](workspace-form-pattern.md)
-   [<span data-ttu-id="7aa54-124">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="7aa54-124">Form Part Section List</span></span>](section-list-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="7aa54-125">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="7aa54-125">UX guidelines</span></span>
<span data-ttu-id="7aa54-126">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="7aa54-126">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="7aa54-127">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="7aa54-127">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="7aa54-128">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="7aa54-128">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="7aa54-129">少なくとも 1 つのリストはタブ付きリストのセクション内に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7aa54-129">At least one list should be present in the tabbed list section.</span></span>
-   <span data-ttu-id="7aa54-130">各フォーム パーツ コントロールでは、いずれかの[フォーム パーツ セクション リスト](section-list-form-pattern.md)パターンを使用するフォームを指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7aa54-130">Each Form Part Control should point to a form that uses one of the [Form Part Section List](section-list-form-pattern.md) patterns.</span></span>

## <a name="examples"></a><span data-ttu-id="7aa54-131">例</span><span class="sxs-lookup"><span data-stu-id="7aa54-131">Examples</span></span>
<span data-ttu-id="7aa54-132">フォーム: **PurchOrderMaintainWorkspace** (**すべてのワークスペース** &gt; **発注書の準備**)</span><span class="sxs-lookup"><span data-stu-id="7aa54-132">Form: **PurchOrderMaintainWorkspace** (**All workspaces** &gt; **Purchase order preparation**)</span></span> 

<span data-ttu-id="7aa54-133">[![タブ付きリストのセクションの例](./media/tabbedlistsectionexample.png)](./media/tabbedlistsectionexample.png)</span><span class="sxs-lookup"><span data-stu-id="7aa54-133">[![Tabbed List Section example](./media/tabbedlistsectionexample.png)](./media/tabbedlistsectionexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="7aa54-134">付録</span><span class="sxs-lookup"><span data-stu-id="7aa54-134">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="7aa54-135">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="7aa54-135">Frequently asked questions</span></span>

<span data-ttu-id="7aa54-136">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="7aa54-136">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="7aa54-137">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="7aa54-137">Open issues</span></span>

<span data-ttu-id="7aa54-138">None</span><span class="sxs-lookup"><span data-stu-id="7aa54-138">None</span></span>
