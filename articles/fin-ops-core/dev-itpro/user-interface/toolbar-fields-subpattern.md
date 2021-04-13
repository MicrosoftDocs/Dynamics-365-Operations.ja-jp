---
title: ツールバーおよびフィールドのサブパターン
description: この記事では、ツールバーおよびフィールドのサブパターンについて説明します。 このコンテナー パターンは、データ フィールドのサブパターンの上にアクションを表示するために使用されます。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 15911
ms.assetid: c5d6aa38-1f5f-41e5-9d90-11766d34a947
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1be83f13945c258580f56e48c1916ec12a88518f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749579"
---
# <a name="toolbar-and-fields-subpattern"></a><span data-ttu-id="f3d86-104">ツールバーおよびフィールドのサブパターン</span><span class="sxs-lookup"><span data-stu-id="f3d86-104">Toolbar and Fields subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3d86-105">この記事では、ツールバーおよびフィールドのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f3d86-105">This article provides information about the Toolbar and Fields subpattern.</span></span> <span data-ttu-id="f3d86-106">このコンテナー パターンは、データ フィールドのサブパターンの上にアクションを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3d86-106">This container pattern is used to show actions above a subpattern of data fields.</span></span> <span data-ttu-id="f3d86-107">ツールバーに含まれるアクションは 10 個未満にしてください。</span><span class="sxs-lookup"><span data-stu-id="f3d86-107">The toolbar should contain fewer than 10 actions.</span></span>

<a name="usage"></a><span data-ttu-id="f3d86-108">用途</span><span class="sxs-lookup"><span data-stu-id="f3d86-108">Usage</span></span>
-----

<span data-ttu-id="f3d86-109">このコンテナー パターンは、データ フィールドのサブパターンの上にアクションを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3d86-109">This container pattern is used to show actions above a subpattern of data fields.</span></span> <span data-ttu-id="f3d86-110">ツールバーに含まれるアクションは 10 個未満にしてください。</span><span class="sxs-lookup"><span data-stu-id="f3d86-110">The toolbar should contain fewer than 10 actions.</span></span>

## <a name="wireframe"></a><span data-ttu-id="f3d86-111">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="f3d86-111">Wireframe</span></span>

<span data-ttu-id="f3d86-112">[![ツール バーおよびフィールドのサブパターンのワイヤーフレーム](./media/toolbarfields1.png)](./media/toolbarfields1.png)</span><span class="sxs-lookup"><span data-stu-id="f3d86-112">[![Wireframe for Toolbar and Fields subpattern](./media/toolbarfields1.png)](./media/toolbarfields1.png)</span></span>

## <a name="model"></a><span data-ttu-id="f3d86-113">モデル</span><span class="sxs-lookup"><span data-stu-id="f3d86-113">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="f3d86-114">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="f3d86-114">High-level structure</span></span>

- <span data-ttu-id="f3d86-115">\[コンテナー\]</span><span class="sxs-lookup"><span data-stu-id="f3d86-115">\[Container\]</span></span>

    - <span data-ttu-id="f3d86-116">ツールバー (ActionPane、スタイル=ストライプ)</span><span class="sxs-lookup"><span data-stu-id="f3d86-116">Toolbar (ActionPane, Style=Strip)</span></span>
    - <span data-ttu-id="f3d86-117">ContentGroup (グループ) – **注記:** フィールドのサブパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3d86-117">ContentGroup (Group) – **Note:** A fields subpattern is used.</span></span>

### <a name="core-components"></a><span data-ttu-id="f3d86-118">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f3d86-118">Core components</span></span>

-   <span data-ttu-id="f3d86-119">ToolbarFields サブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="f3d86-119">Apply the ToolbarFields subpattern to the container control.</span></span>
-   <span data-ttu-id="f3d86-120">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="f3d86-120">Address BP Warnings:</span></span>
    -   <span data-ttu-id="f3d86-121">繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。</span><span class="sxs-lookup"><span data-stu-id="f3d86-121">No additional BP checks are required beyond the AX6.3 BP checks that were carried forward.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="f3d86-122">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="f3d86-122">Related patterns</span></span>

-   [<span data-ttu-id="f3d86-123">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="f3d86-123">Toolbar and List</span></span>](toolbar-list-subpattern.md)

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="f3d86-124">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="f3d86-124">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="f3d86-125">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="f3d86-125">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="f3d86-126">表形式フィールド</span><span class="sxs-lookup"><span data-stu-id="f3d86-126">Tabular Fields</span></span>](tabular-fields-subpattern.md)
-   [<span data-ttu-id="f3d86-127">分析コード式ビルダー</span><span class="sxs-lookup"><span data-stu-id="f3d86-127">Dimension Expression Builder</span></span>](../financial/dimension-expression-builder-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="f3d86-128">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="f3d86-128">UX guidelines</span></span>
<span data-ttu-id="f3d86-129">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="f3d86-129">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="f3d86-130">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f3d86-130">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="f3d86-131">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d86-131">Open the form in the browser, and walk through these steps.</span></span> 

<span data-ttu-id="f3d86-132">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="f3d86-132">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="f3d86-133">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="f3d86-133">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="f3d86-134">**ツールバー** **ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="f3d86-134">**Toolbar** **guidelines:**</span></span>

-   <span data-ttu-id="f3d86-135">ツールバーのガイドラインは、Dynamics AX の [全般的なフォーム ガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="f3d86-135">Toolbar guidelines have been consolidated into the Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

## <a name="examples"></a><span data-ttu-id="f3d86-136">例</span><span class="sxs-lookup"><span data-stu-id="f3d86-136">Examples</span></span>
### <a name="toolbar-and-fields"></a><span data-ttu-id="f3d86-137">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="f3d86-137">Toolbar and Fields</span></span>

<span data-ttu-id="f3d86-138">フォーム: **HcmPosition** **(WorkerAssignmentTabPage)**</span><span class="sxs-lookup"><span data-stu-id="f3d86-138">Form: **HcmPosition** **(WorkerAssignmentTabPage)**</span></span> 

<span data-ttu-id="f3d86-139">[![ツール バーおよびフィールドのサブパターンの例](./media/toolbarfields2-1024x131.png)](./media/toolbarfields2.png)</span><span class="sxs-lookup"><span data-stu-id="f3d86-139">[![Example of Toolbar and Fields subpattern](./media/toolbarfields2-1024x131.png)](./media/toolbarfields2.png)</span></span>

## <a name="resources"></a><span data-ttu-id="f3d86-140">リソース</span><span class="sxs-lookup"><span data-stu-id="f3d86-140">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="f3d86-141">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="f3d86-141">Typically used by patterns</span></span>

-   [<span data-ttu-id="f3d86-142">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="f3d86-142">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="f3d86-143">目次</span><span class="sxs-lookup"><span data-stu-id="f3d86-143">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="f3d86-144">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="f3d86-144">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="f3d86-145">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="f3d86-145">Details Transaction</span></span>](details-transaction-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="f3d86-146">付録</span><span class="sxs-lookup"><span data-stu-id="f3d86-146">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="f3d86-147">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="f3d86-147">Frequently asked questions</span></span>

<span data-ttu-id="f3d86-148">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="f3d86-148">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="f3d86-149">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="f3d86-149">Open issues</span></span>

-   <span data-ttu-id="f3d86-150">**ShowMoreLess グループは、パターンの一部にすべきですか、独自のサブパターンにする必要がありますか。**</span><span class="sxs-lookup"><span data-stu-id="f3d86-150">**Should the ShowMoreLess group be part of the pattern, or should it be its own subpattern?**</span></span>
    -   <span data-ttu-id="f3d86-151">新しいパターンの追加を正当化するだけの十分な需要があるまで、**ShowMoreLess** グループをカスタム コンテナー パターンとして取り扱います。</span><span class="sxs-lookup"><span data-stu-id="f3d86-151">We will treat the **ShowMoreLess** group as a custom container pattern until there is enough demand to justify the addition of a new pattern.</span></span>

### <a name="microsoft-dynamics-ax-2012-content"></a><span data-ttu-id="f3d86-152">Microsoft Dynamics AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="f3d86-152">Microsoft Dynamics AX 2012 content</span></span>

<span data-ttu-id="f3d86-153">**HcmPosition**</span><span class="sxs-lookup"><span data-stu-id="f3d86-153">**HcmPosition**</span></span> 

![以前のバージョンのツール バーおよびフィールド](./media/toolbarfields3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]