---
title: "セクション関連リンクのサブパターン"
description: "この記事では、関連リンクのサブパターンに関する情報を提供します。 このサブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 29331
ms.assetid: 984d7c6b-cf0a-4056-88f3-c32c92ca3401
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d797b366325b77046d8322df69981df3bce90e29
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="section-related-links-subpattern"></a><span data-ttu-id="2c3ad-104">セクション関連リンクのサブパターン</span><span class="sxs-lookup"><span data-stu-id="2c3ad-104">Section Related Links subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c3ad-105">この記事では、関連リンクのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="2c3ad-105">This article provides information about the Section Related Links subpattern.</span></span> <span data-ttu-id="2c3ad-106">このサブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="2c3ad-106">This subpattern is used as part of the Operational Workspace pattern, specifically for the last panorama section that contains a set of links to other forms.</span></span>

<a name="usage"></a><span data-ttu-id="2c3ad-107">用途</span><span class="sxs-lookup"><span data-stu-id="2c3ad-107">Usage</span></span>
-----

<span data-ttu-id="2c3ad-108">セクション関連リンク サブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="2c3ad-108">The Section Related Links subpattern is used as part of the Operational Workspace pattern, specifically for the last panorama section that contains a set of links to other forms.</span></span>

## <a name="wireframe"></a><span data-ttu-id="2c3ad-109">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="2c3ad-109">Wireframe</span></span>
<span data-ttu-id="2c3ad-110">[![sectionRelatedLinksWireframe](./media/sectionrelatedlinkswireframe.png)](./media/sectionrelatedlinkswireframe.png)</span><span class="sxs-lookup"><span data-stu-id="2c3ad-110">[![sectionRelatedLinksWireframe](./media/sectionrelatedlinkswireframe.png)](./media/sectionrelatedlinkswireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="2c3ad-111">Microsoft Dynamics AX のパータン変更</span><span class="sxs-lookup"><span data-stu-id="2c3ad-111">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="2c3ad-112">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="2c3ad-112">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="2c3ad-113">モデル</span><span class="sxs-lookup"><span data-stu-id="2c3ad-113">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="2c3ad-114">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="2c3ad-114">High-level structure</span></span>

- <span data-ttu-id="2c3ad-115">TabPage</span><span class="sxs-lookup"><span data-stu-id="2c3ad-115">TabPage</span></span>

    - <span data-ttu-id="2c3ad-116">*LinkButton ($ ボタン)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="2c3ad-116">*LinkButton ($Button) \[0..N\]*</span></span>
    - <span data-ttu-id="2c3ad-117">*ButtonGroup (グループ)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="2c3ad-117">*ButtonGroup (Group) \[0..N\]*</span></span>

- <span data-ttu-id="2c3ad-118">LinkButton ($Button) \[1..N\]</span><span class="sxs-lookup"><span data-stu-id="2c3ad-118">LinkButton ($Button) \[1..N\]</span></span>

### <a name="core-components"></a><span data-ttu-id="2c3ad-119">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="2c3ad-119">Core components</span></span>

<span data-ttu-id="2c3ad-120">セクション関連リンクを運用ワークスペース内の適切なタブ ページに適用します。</span><span class="sxs-lookup"><span data-stu-id="2c3ad-120">Apply Section Related Links to the appropriate tab page in the Operational Workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="2c3ad-121">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="2c3ad-121">Related container patterns</span></span>

-   [<span data-ttu-id="2c3ad-122">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="2c3ad-122">Operational Workspace</span></span>](workspace-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="2c3ad-123">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="2c3ad-123">UX guidelines</span></span>
<span data-ttu-id="2c3ad-124">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="2c3ad-124">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="2c3ad-125">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="2c3ad-125">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="2c3ad-126">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="2c3ad-126">Open the form in the browser, and walk through these steps.</span></span> <span data-ttu-id="2c3ad-127">None</span><span class="sxs-lookup"><span data-stu-id="2c3ad-127">None</span></span>

## <a name="examples"></a><span data-ttu-id="2c3ad-128">例</span><span class="sxs-lookup"><span data-stu-id="2c3ad-128">Examples</span></span>
<span data-ttu-id="2c3ad-129">フォーム: **PurchOrderProcessReceiptsWorkspace** (**すべてのワークスペース** &gt; **発注書入庫とフォローアップ** (**リンク**セクションを参照してください)</span><span class="sxs-lookup"><span data-stu-id="2c3ad-129">Form: **PurchOrderProcessReceiptsWorkspace** (**All workspaces** &gt; **Purchase order receipt and follow-up** (see the **Links** section)</span></span> 

<span data-ttu-id="2c3ad-130">[![sectionRelatedLinksExample](./media/sectionrelatedlinksexample.png)](./media/sectionrelatedlinksexample.png)</span><span class="sxs-lookup"><span data-stu-id="2c3ad-130">[![sectionRelatedLinksExample](./media/sectionrelatedlinksexample.png)](./media/sectionrelatedlinksexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="2c3ad-131">付録</span><span class="sxs-lookup"><span data-stu-id="2c3ad-131">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="2c3ad-132">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="2c3ad-132">Frequently asked questions</span></span>

<span data-ttu-id="2c3ad-133">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="2c3ad-133">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="2c3ad-134">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="2c3ad-134">Open issues</span></span>

<span data-ttu-id="2c3ad-135">None</span><span class="sxs-lookup"><span data-stu-id="2c3ad-135">None</span></span>

