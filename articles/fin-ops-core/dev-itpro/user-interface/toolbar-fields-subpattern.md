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
ms.openlocfilehash: 8483c28d3b5b1fda719a7798bacfa01be942eb98
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183029"
---
# <a name="toolbar-and-fields-subpattern"></a><span data-ttu-id="bf200-105">ツールバーおよびフィールドのサブパターン</span><span class="sxs-lookup"><span data-stu-id="bf200-105">Toolbar and Fields subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf200-106">この記事では、ツールバーおよびフィールドのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bf200-106">This article provides information about the Toolbar and Fields subpattern.</span></span> <span data-ttu-id="bf200-107">このコンテナー パターンは、データ フィールドのサブパターンの上にアクションを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf200-107">This container pattern is used to show actions above a subpattern of data fields.</span></span> <span data-ttu-id="bf200-108">ツールバーに含まれるアクションは 10 個未満にしてください。</span><span class="sxs-lookup"><span data-stu-id="bf200-108">The toolbar should contain fewer than 10 actions.</span></span>

<a name="usage"></a><span data-ttu-id="bf200-109">用途</span><span class="sxs-lookup"><span data-stu-id="bf200-109">Usage</span></span>
-----

<span data-ttu-id="bf200-110">このコンテナー パターンは、データ フィールドのサブパターンの上にアクションを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf200-110">This container pattern is used to show actions above a subpattern of data fields.</span></span> <span data-ttu-id="bf200-111">ツールバーに含まれるアクションは 10 個未満にしてください。</span><span class="sxs-lookup"><span data-stu-id="bf200-111">The toolbar should contain fewer than 10 actions.</span></span>

## <a name="wireframe"></a><span data-ttu-id="bf200-112">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="bf200-112">Wireframe</span></span>

<span data-ttu-id="bf200-113">[![ToolbarFields(1)](./media/toolbarfields1.png)](./media/toolbarfields1.png)</span><span class="sxs-lookup"><span data-stu-id="bf200-113">[![ToolbarFields(1)](./media/toolbarfields1.png)](./media/toolbarfields1.png)</span></span>

## <a name="model"></a><span data-ttu-id="bf200-114">モデル</span><span class="sxs-lookup"><span data-stu-id="bf200-114">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="bf200-115">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="bf200-115">High-level structure</span></span>

- <span data-ttu-id="bf200-116">\[コンテナ\]</span><span class="sxs-lookup"><span data-stu-id="bf200-116">\[Container\]</span></span>

    - <span data-ttu-id="bf200-117">ツールバー (ActionPane、スタイル=ストライプ)</span><span class="sxs-lookup"><span data-stu-id="bf200-117">Toolbar (ActionPane, Style=Strip)</span></span>
    - <span data-ttu-id="bf200-118">ContentGroup (グループ) – **注記:** フィールドのサブパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf200-118">ContentGroup (Group) – **Note:** A fields subpattern is used.</span></span>

### <a name="core-components"></a><span data-ttu-id="bf200-119">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="bf200-119">Core components</span></span>

-   <span data-ttu-id="bf200-120">ToolbarFields サブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="bf200-120">Apply the ToolbarFields subpattern to the container control.</span></span>
-   <span data-ttu-id="bf200-121">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="bf200-121">Address BP Warnings:</span></span>
    -   <span data-ttu-id="bf200-122">繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。</span><span class="sxs-lookup"><span data-stu-id="bf200-122">No additional BP checks are required beyond the AX6.3 BP checks that were carried forward.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="bf200-123">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="bf200-123">Related patterns</span></span>

-   [<span data-ttu-id="bf200-124">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="bf200-124">Toolbar and List</span></span>](toolbar-list-subpattern.md)

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="bf200-125">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="bf200-125">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="bf200-126">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="bf200-126">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="bf200-127">表形式フィールド</span><span class="sxs-lookup"><span data-stu-id="bf200-127">Tabular Fields</span></span>](tabular-fields-subpattern.md)
-   [<span data-ttu-id="bf200-128">分析コード式ビルダー</span><span class="sxs-lookup"><span data-stu-id="bf200-128">Dimension Expression Builder</span></span>](../financial/dimension-expression-builder-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="bf200-129">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="bf200-129">UX guidelines</span></span>
<span data-ttu-id="bf200-130">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="bf200-130">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="bf200-131">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="bf200-131">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="bf200-132">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="bf200-132">Open the form in the browser, and walk through these steps.</span></span> 

<span data-ttu-id="bf200-133">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="bf200-133">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="bf200-134">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="bf200-134">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="bf200-135">**ツールバー** **ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="bf200-135">**Toolbar** **guidelines:**</span></span>

-   <span data-ttu-id="bf200-136">ツールバーのガイドラインは、Dynamics AX の [全般的なフォーム ガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="bf200-136">Toolbar guidelines have been consolidated into the Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

## <a name="examples"></a><span data-ttu-id="bf200-137">例</span><span class="sxs-lookup"><span data-stu-id="bf200-137">Examples</span></span>
### <a name="toolbar-and-fields"></a><span data-ttu-id="bf200-138">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="bf200-138">Toolbar and Fields</span></span>

<span data-ttu-id="bf200-139">フォーム: **HcmPosition** **(WorkerAssignmentTabPage)**</span><span class="sxs-lookup"><span data-stu-id="bf200-139">Form: **HcmPosition** **(WorkerAssignmentTabPage)**</span></span> 

<span data-ttu-id="bf200-140">[![ToolbarFields(2)](./media/toolbarfields2-1024x131.png)](./media/toolbarfields2.png)</span><span class="sxs-lookup"><span data-stu-id="bf200-140">[![ToolbarFields(2)](./media/toolbarfields2-1024x131.png)](./media/toolbarfields2.png)</span></span>

## <a name="resources"></a><span data-ttu-id="bf200-141">リソース</span><span class="sxs-lookup"><span data-stu-id="bf200-141">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="bf200-142">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="bf200-142">Typically used by patterns</span></span>

-   [<span data-ttu-id="bf200-143">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="bf200-143">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="bf200-144">目次</span><span class="sxs-lookup"><span data-stu-id="bf200-144">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="bf200-145">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="bf200-145">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="bf200-146">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="bf200-146">Details Transaction</span></span>](details-transaction-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="bf200-147">付録</span><span class="sxs-lookup"><span data-stu-id="bf200-147">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="bf200-148">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="bf200-148">Frequently asked questions</span></span>

<span data-ttu-id="bf200-149">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="bf200-149">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="bf200-150">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="bf200-150">Open issues</span></span>

-   <span data-ttu-id="bf200-151">**ShowMoreLess グループは、パターンの一部にすべきですか、独自のサブパターンにする必要がありますか。**</span><span class="sxs-lookup"><span data-stu-id="bf200-151">**Should the ShowMoreLess group be part of the pattern, or should it be its own subpattern?**</span></span>
    -   <span data-ttu-id="bf200-152">新しいパターンの追加を正当化するだけの十分な需要があるまで、**ShowMoreLess** グループをカスタム コンテナー パターンとして取り扱います。</span><span class="sxs-lookup"><span data-stu-id="bf200-152">We will treat the **ShowMoreLess** group as a custom container pattern until there is enough demand to justify the addition of a new pattern.</span></span>

### <a name="microsoft-dynamics-ax-2012-content"></a><span data-ttu-id="bf200-153">Microsoft Dynamics AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="bf200-153">Microsoft Dynamics AX 2012 content</span></span>

<span data-ttu-id="bf200-154">**HcmPosition**</span><span class="sxs-lookup"><span data-stu-id="bf200-154">**HcmPosition**</span></span> 

![ToolbarFields(3)](./media/toolbarfields3.png)
