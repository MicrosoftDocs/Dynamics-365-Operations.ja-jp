---
title: ツールバーおよびフィールドのサブパターン
description: この記事では、ツールバーおよびフィールドのサブパターンについて説明します。 このコンテナー パターンは、データ フィールドのサブパターンの上にアクションを表示するために使用されます。 ツールバーに含まれるアクションは 10 個未満にしてください。
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
ms.custom: 15911
ms.assetid: c5d6aa38-1f5f-41e5-9d90-11766d34a947
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a94273fcb9b0ce46929b04c55f6b917352368ee
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658799"
---
# <a name="toolbar-and-fields-subpattern"></a><span data-ttu-id="35074-105">ツールバーおよびフィールドのサブパターン</span><span class="sxs-lookup"><span data-stu-id="35074-105">Toolbar and Fields subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35074-106">この記事では、ツールバーおよびフィールドのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="35074-106">This article provides information about the Toolbar and Fields subpattern.</span></span> <span data-ttu-id="35074-107">このコンテナー パターンは、データ フィールドのサブパターンの上にアクションを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="35074-107">This container pattern is used to show actions above a subpattern of data fields.</span></span> <span data-ttu-id="35074-108">ツールバーに含まれるアクションは 10 個未満にしてください。</span><span class="sxs-lookup"><span data-stu-id="35074-108">The toolbar should contain fewer than 10 actions.</span></span>

<a name="usage"></a><span data-ttu-id="35074-109">用途</span><span class="sxs-lookup"><span data-stu-id="35074-109">Usage</span></span>
-----

<span data-ttu-id="35074-110">このコンテナー パターンは、データ フィールドのサブパターンの上にアクションを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="35074-110">This container pattern is used to show actions above a subpattern of data fields.</span></span> <span data-ttu-id="35074-111">ツールバーに含まれるアクションは 10 個未満にしてください。</span><span class="sxs-lookup"><span data-stu-id="35074-111">The toolbar should contain fewer than 10 actions.</span></span>

## <a name="wireframe"></a><span data-ttu-id="35074-112">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="35074-112">Wireframe</span></span>

<span data-ttu-id="35074-113">[![ツール バーおよびフィールドのサブパターンのワイヤーフレーム](./media/toolbarfields1.png)](./media/toolbarfields1.png)</span><span class="sxs-lookup"><span data-stu-id="35074-113">[![Wireframe for Toolbar and Fields subpattern](./media/toolbarfields1.png)](./media/toolbarfields1.png)</span></span>

## <a name="model"></a><span data-ttu-id="35074-114">モデル</span><span class="sxs-lookup"><span data-stu-id="35074-114">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="35074-115">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="35074-115">High-level structure</span></span>

- <span data-ttu-id="35074-116">\[コンテナー\]</span><span class="sxs-lookup"><span data-stu-id="35074-116">\[Container\]</span></span>

    - <span data-ttu-id="35074-117">ツールバー (ActionPane、スタイル=ストライプ)</span><span class="sxs-lookup"><span data-stu-id="35074-117">Toolbar (ActionPane, Style=Strip)</span></span>
    - <span data-ttu-id="35074-118">ContentGroup (グループ) – **注記:** フィールドのサブパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="35074-118">ContentGroup (Group) – **Note:** A fields subpattern is used.</span></span>

### <a name="core-components"></a><span data-ttu-id="35074-119">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="35074-119">Core components</span></span>

-   <span data-ttu-id="35074-120">ToolbarFields サブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="35074-120">Apply the ToolbarFields subpattern to the container control.</span></span>
-   <span data-ttu-id="35074-121">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="35074-121">Address BP Warnings:</span></span>
    -   <span data-ttu-id="35074-122">繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。</span><span class="sxs-lookup"><span data-stu-id="35074-122">No additional BP checks are required beyond the AX6.3 BP checks that were carried forward.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="35074-123">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="35074-123">Related patterns</span></span>

-   [<span data-ttu-id="35074-124">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="35074-124">Toolbar and List</span></span>](toolbar-list-subpattern.md)

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="35074-125">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="35074-125">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="35074-126">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="35074-126">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="35074-127">表形式フィールド</span><span class="sxs-lookup"><span data-stu-id="35074-127">Tabular Fields</span></span>](tabular-fields-subpattern.md)
-   [<span data-ttu-id="35074-128">分析コード式ビルダー</span><span class="sxs-lookup"><span data-stu-id="35074-128">Dimension Expression Builder</span></span>](../financial/dimension-expression-builder-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="35074-129">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="35074-129">UX guidelines</span></span>
<span data-ttu-id="35074-130">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="35074-130">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="35074-131">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="35074-131">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="35074-132">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="35074-132">Open the form in the browser, and walk through these steps.</span></span> 

<span data-ttu-id="35074-133">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="35074-133">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="35074-134">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="35074-134">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="35074-135">**ツールバー** **ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="35074-135">**Toolbar** **guidelines:**</span></span>

-   <span data-ttu-id="35074-136">ツールバーのガイドラインは、Dynamics AX の [全般的なフォーム ガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="35074-136">Toolbar guidelines have been consolidated into the Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

## <a name="examples"></a><span data-ttu-id="35074-137">例</span><span class="sxs-lookup"><span data-stu-id="35074-137">Examples</span></span>
### <a name="toolbar-and-fields"></a><span data-ttu-id="35074-138">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="35074-138">Toolbar and Fields</span></span>

<span data-ttu-id="35074-139">フォーム: **HcmPosition** **(WorkerAssignmentTabPage)**</span><span class="sxs-lookup"><span data-stu-id="35074-139">Form: **HcmPosition** **(WorkerAssignmentTabPage)**</span></span> 

<span data-ttu-id="35074-140">[![ツール バーおよびフィールドのサブパターンの例](./media/toolbarfields2-1024x131.png)](./media/toolbarfields2.png)</span><span class="sxs-lookup"><span data-stu-id="35074-140">[![Example of Toolbar and Fields subpattern](./media/toolbarfields2-1024x131.png)](./media/toolbarfields2.png)</span></span>

## <a name="resources"></a><span data-ttu-id="35074-141">リソース</span><span class="sxs-lookup"><span data-stu-id="35074-141">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="35074-142">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="35074-142">Typically used by patterns</span></span>

-   [<span data-ttu-id="35074-143">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="35074-143">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="35074-144">目次</span><span class="sxs-lookup"><span data-stu-id="35074-144">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="35074-145">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="35074-145">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="35074-146">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="35074-146">Details Transaction</span></span>](details-transaction-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="35074-147">付録</span><span class="sxs-lookup"><span data-stu-id="35074-147">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="35074-148">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="35074-148">Frequently asked questions</span></span>

<span data-ttu-id="35074-149">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="35074-149">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="35074-150">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="35074-150">Open issues</span></span>

-   <span data-ttu-id="35074-151">**ShowMoreLess グループは、パターンの一部にすべきですか、独自のサブパターンにする必要がありますか。**</span><span class="sxs-lookup"><span data-stu-id="35074-151">**Should the ShowMoreLess group be part of the pattern, or should it be its own subpattern?**</span></span>
    -   <span data-ttu-id="35074-152">新しいパターンの追加を正当化するだけの十分な需要があるまで、**ShowMoreLess** グループをカスタム コンテナー パターンとして取り扱います。</span><span class="sxs-lookup"><span data-stu-id="35074-152">We will treat the **ShowMoreLess** group as a custom container pattern until there is enough demand to justify the addition of a new pattern.</span></span>

### <a name="microsoft-dynamics-ax-2012-content"></a><span data-ttu-id="35074-153">Microsoft Dynamics AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="35074-153">Microsoft Dynamics AX 2012 content</span></span>

<span data-ttu-id="35074-154">**HcmPosition**</span><span class="sxs-lookup"><span data-stu-id="35074-154">**HcmPosition**</span></span> 

![以前のバージョンのツール バーおよびフィールド](./media/toolbarfields3.png)