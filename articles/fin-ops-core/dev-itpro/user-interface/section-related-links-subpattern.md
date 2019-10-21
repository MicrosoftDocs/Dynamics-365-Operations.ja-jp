---
title: セクション関連リンクのサブパターン
description: この記事では、関連リンクのサブパターンに関する情報を提供します。 このサブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。
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
ms.custom: 29331
ms.assetid: 984d7c6b-cf0a-4056-88f3-c32c92ca3401
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb9868795661c1ed80b60aae1486eedc3bc5f2b0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191762"
---
# <a name="section-related-links-subpattern"></a><span data-ttu-id="594af-104">セクション関連リンクのサブパターン</span><span class="sxs-lookup"><span data-stu-id="594af-104">Section Related Links subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="594af-105">この記事では、関連リンクのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="594af-105">This article provides information about the Section Related Links subpattern.</span></span> <span data-ttu-id="594af-106">このサブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="594af-106">This subpattern is used as part of the Operational Workspace pattern, specifically for the last panorama section that contains a set of links to other forms.</span></span>

<a name="usage"></a><span data-ttu-id="594af-107">用途</span><span class="sxs-lookup"><span data-stu-id="594af-107">Usage</span></span>
-----

<span data-ttu-id="594af-108">セクション関連リンク サブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="594af-108">The Section Related Links subpattern is used as part of the Operational Workspace pattern, specifically for the last panorama section that contains a set of links to other forms.</span></span>

## <a name="wireframe"></a><span data-ttu-id="594af-109">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="594af-109">Wireframe</span></span>
<span data-ttu-id="594af-110">[![sectionRelatedLinksWireframe](./media/sectionrelatedlinkswireframe.png)](./media/sectionrelatedlinkswireframe.png)</span><span class="sxs-lookup"><span data-stu-id="594af-110">[![sectionRelatedLinksWireframe](./media/sectionrelatedlinkswireframe.png)](./media/sectionrelatedlinkswireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="594af-111">Microsoft Dynamics AX 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="594af-111">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="594af-112">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="594af-112">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="594af-113">モデル</span><span class="sxs-lookup"><span data-stu-id="594af-113">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="594af-114">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="594af-114">High-level structure</span></span>

- <span data-ttu-id="594af-115">TabPage</span><span class="sxs-lookup"><span data-stu-id="594af-115">TabPage</span></span>

    - <span data-ttu-id="594af-116">*LinkButton ($ ボタン)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="594af-116">*LinkButton ($Button) \[0..N\]*</span></span>
    - <span data-ttu-id="594af-117">*ButtonGroup (グループ)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="594af-117">*ButtonGroup (Group) \[0..N\]*</span></span>

- <span data-ttu-id="594af-118">LinkButton ($Button) \[1..N\]</span><span class="sxs-lookup"><span data-stu-id="594af-118">LinkButton ($Button) \[1..N\]</span></span>

### <a name="core-components"></a><span data-ttu-id="594af-119">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="594af-119">Core components</span></span>

<span data-ttu-id="594af-120">セクション関連リンクを運用ワークスペース内の適切なタブ ページに適用します。</span><span class="sxs-lookup"><span data-stu-id="594af-120">Apply Section Related Links to the appropriate tab page in the Operational Workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="594af-121">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="594af-121">Related container patterns</span></span>

-   [<span data-ttu-id="594af-122">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="594af-122">Operational Workspace</span></span>](workspace-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="594af-123">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="594af-123">UX guidelines</span></span>
<span data-ttu-id="594af-124">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="594af-124">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="594af-125">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="594af-125">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="594af-126">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="594af-126">Open the form in the browser, and walk through these steps.</span></span> <span data-ttu-id="594af-127">None</span><span class="sxs-lookup"><span data-stu-id="594af-127">None</span></span>

## <a name="examples"></a><span data-ttu-id="594af-128">例</span><span class="sxs-lookup"><span data-stu-id="594af-128">Examples</span></span>
<span data-ttu-id="594af-129">フォーム: **PurchOrderProcessReceiptsWorkspace** (**すべてのワークスペース** &gt; **発注書入庫とフォローアップ** (**リンク**セクションを参照してください)</span><span class="sxs-lookup"><span data-stu-id="594af-129">Form: **PurchOrderProcessReceiptsWorkspace** (**All workspaces** &gt; **Purchase order receipt and follow-up** (see the **Links** section)</span></span> 

<span data-ttu-id="594af-130">[![sectionRelatedLinksExample](./media/sectionrelatedlinksexample.png)](./media/sectionrelatedlinksexample.png)</span><span class="sxs-lookup"><span data-stu-id="594af-130">[![sectionRelatedLinksExample](./media/sectionrelatedlinksexample.png)](./media/sectionrelatedlinksexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="594af-131">付録</span><span class="sxs-lookup"><span data-stu-id="594af-131">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="594af-132">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="594af-132">Frequently asked questions</span></span>

<span data-ttu-id="594af-133">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="594af-133">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="594af-134">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="594af-134">Open issues</span></span>

<span data-ttu-id="594af-135">None</span><span class="sxs-lookup"><span data-stu-id="594af-135">None</span></span>
