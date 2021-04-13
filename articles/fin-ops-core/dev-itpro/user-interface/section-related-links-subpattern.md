---
title: セクション関連リンクのサブパターン
description: この記事では、関連リンクのサブパターンに関する情報を提供します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29331
ms.assetid: 984d7c6b-cf0a-4056-88f3-c32c92ca3401
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f36c2930d090b9c5bfe9b7aaf68436fe640f3fd2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754844"
---
# <a name="section-related-links-subpattern"></a><span data-ttu-id="d0bae-103">セクション関連リンクのサブパターン</span><span class="sxs-lookup"><span data-stu-id="d0bae-103">Section Related Links subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0bae-104">この記事では、関連リンクのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d0bae-104">This article provides information about the Section Related Links subpattern.</span></span> <span data-ttu-id="d0bae-105">このサブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="d0bae-105">This subpattern is used as part of the Operational Workspace pattern, specifically for the last panorama section that contains a set of links to other forms.</span></span>

<a name="usage"></a><span data-ttu-id="d0bae-106">用途</span><span class="sxs-lookup"><span data-stu-id="d0bae-106">Usage</span></span>
-----

<span data-ttu-id="d0bae-107">セクション関連リンク サブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="d0bae-107">The Section Related Links subpattern is used as part of the Operational Workspace pattern, specifically for the last panorama section that contains a set of links to other forms.</span></span>

## <a name="wireframe"></a><span data-ttu-id="d0bae-108">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="d0bae-108">Wireframe</span></span>
<span data-ttu-id="d0bae-109">[![セクション関連リンクのワイヤーフレーム](./media/sectionrelatedlinkswireframe.png)](./media/sectionrelatedlinkswireframe.png)</span><span class="sxs-lookup"><span data-stu-id="d0bae-109">[![Section Related Links wireframe](./media/sectionrelatedlinkswireframe.png)](./media/sectionrelatedlinkswireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="d0bae-110">Microsoft Dynamics AX 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="d0bae-110">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="d0bae-111">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="d0bae-111">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="d0bae-112">モデル</span><span class="sxs-lookup"><span data-stu-id="d0bae-112">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="d0bae-113">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="d0bae-113">High-level structure</span></span>

- <span data-ttu-id="d0bae-114">TabPage</span><span class="sxs-lookup"><span data-stu-id="d0bae-114">TabPage</span></span>

    - <span data-ttu-id="d0bae-115">*LinkButton ($ ボタン)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="d0bae-115">*LinkButton ($Button) \[0..N\]*</span></span>
    - <span data-ttu-id="d0bae-116">*ButtonGroup (グループ)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="d0bae-116">*ButtonGroup (Group) \[0..N\]*</span></span>

- <span data-ttu-id="d0bae-117">LinkButton ($Button) \[1..N\]</span><span class="sxs-lookup"><span data-stu-id="d0bae-117">LinkButton ($Button) \[1..N\]</span></span>

### <a name="core-components"></a><span data-ttu-id="d0bae-118">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d0bae-118">Core components</span></span>

<span data-ttu-id="d0bae-119">セクション関連リンクを運用ワークスペース内の適切なタブ ページに適用します。</span><span class="sxs-lookup"><span data-stu-id="d0bae-119">Apply Section Related Links to the appropriate tab page in the Operational Workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="d0bae-120">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="d0bae-120">Related container patterns</span></span>

-   [<span data-ttu-id="d0bae-121">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="d0bae-121">Operational Workspace</span></span>](workspace-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="d0bae-122">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="d0bae-122">UX guidelines</span></span>
<span data-ttu-id="d0bae-123">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="d0bae-123">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="d0bae-124">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="d0bae-124">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="d0bae-125">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="d0bae-125">Open the form in the browser, and walk through these steps.</span></span> <span data-ttu-id="d0bae-126">None</span><span class="sxs-lookup"><span data-stu-id="d0bae-126">None</span></span>

## <a name="examples"></a><span data-ttu-id="d0bae-127">例</span><span class="sxs-lookup"><span data-stu-id="d0bae-127">Examples</span></span>
<span data-ttu-id="d0bae-128">フォーム: **PurchOrderProcessReceiptsWorkspace** (**すべてのワークスペース** &gt; **発注書入庫とフォローアップ** (**リンク** セクションを参照してください)</span><span class="sxs-lookup"><span data-stu-id="d0bae-128">Form: **PurchOrderProcessReceiptsWorkspace** (**All workspaces** &gt; **Purchase order receipt and follow-up** (see the **Links** section)</span></span> 

<span data-ttu-id="d0bae-129">[![セクション関連リンクの例](./media/sectionrelatedlinksexample.png)](./media/sectionrelatedlinksexample.png)</span><span class="sxs-lookup"><span data-stu-id="d0bae-129">[![Section Related Links example](./media/sectionrelatedlinksexample.png)](./media/sectionrelatedlinksexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="d0bae-130">付録</span><span class="sxs-lookup"><span data-stu-id="d0bae-130">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="d0bae-131">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="d0bae-131">Frequently asked questions</span></span>

<span data-ttu-id="d0bae-132">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="d0bae-132">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="d0bae-133">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="d0bae-133">Open issues</span></span>

<span data-ttu-id="d0bae-134">None</span><span class="sxs-lookup"><span data-stu-id="d0bae-134">None</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]