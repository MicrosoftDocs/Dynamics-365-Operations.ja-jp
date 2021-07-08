---
title: ワークスペース ページ フィルター グループのサブパターン
description: この記事では、ワークスペース ページ フィルター グループのサブパターンについて説明します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29231
ms.assetid: 90d5a70b-a99b-4e79-a52d-b4ef5a942607
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b86690bb57ae2059303047eff7b624c0808f4f9
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189730"
---
# <a name="workspace-page-filter-group-subpattern"></a><span data-ttu-id="bce4f-103">ワークスペース ページ フィルター グループのサブパターン</span><span class="sxs-lookup"><span data-stu-id="bce4f-103">Workspace Page Filter Group subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bce4f-104">この記事では、ワークスペース ページ フィルター グループのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bce4f-104">This article provides information about the Workspace Page Filter Group subpattern.</span></span> <span data-ttu-id="bce4f-105">このサブパターンは、ワークスペースがフォーム上で 1 つのワークスペース全体にかかわるフィルターを公開する必要があるとき、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="bce4f-105">This subpattern is used as part of the Operational Workspace pattern when a workspace must expose a single workspace-wide filter on the form.</span></span>

## <a name="usage"></a><span data-ttu-id="bce4f-106">用途</span><span class="sxs-lookup"><span data-stu-id="bce4f-106">Usage</span></span>

<span data-ttu-id="bce4f-107">ワークスペース ページ フィルター グループのサブパターンは、特にワークスペースがフォーム上で 1 つのワークスペース全体にかかわるフィルターを公開する必要があるときに、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="bce4f-107">The Workspace Page Filter Group subpattern is used as part of the Operational Workspace pattern, specifically when a workspace must expose a single workspace-wide filter on the form.</span></span>

## <a name="wireframe"></a><span data-ttu-id="bce4f-108">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="bce4f-108">Wireframe</span></span>

<span data-ttu-id="bce4f-109">[![ワークスペース ページ フィルター グループのサブパターンのワイヤーフレーム](./media/workspacepagefiltergroupwireframe.png)](./media/workspacepagefiltergroupwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="bce4f-109">[![Wireframe for Workspace Page Filter Group subpattern](./media/workspacepagefiltergroupwireframe.png)](./media/workspacepagefiltergroupwireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="bce4f-110">Microsoft Dynamics AX 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="bce4f-110">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="bce4f-111">このパターンは、Microsoft Dynamics AX 2012 には存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="bce4f-111">This pattern didn't exist in Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="bce4f-112">モデル</span><span class="sxs-lookup"><span data-stu-id="bce4f-112">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="bce4f-113">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="bce4f-113">High-level structure</span></span>

- <span data-ttu-id="bce4f-114">グループ化</span><span class="sxs-lookup"><span data-stu-id="bce4f-114">Group</span></span>

    - <span data-ttu-id="bce4f-115">フィールド ($Field)</span><span class="sxs-lookup"><span data-stu-id="bce4f-115">Field ($Field)</span></span>

### <a name="core-components"></a><span data-ttu-id="bce4f-116">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="bce4f-116">Core components</span></span>

<span data-ttu-id="bce4f-117">ワークスペース ページ フィルター グループを (運用) ワークスペースの適切なグループに適用します。</span><span class="sxs-lookup"><span data-stu-id="bce4f-117">Apply Workspace Page Filter Group to the appropriate group in an (operational) workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="bce4f-118">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="bce4f-118">Related container patterns</span></span>

-   [<span data-ttu-id="bce4f-119">カスタム フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="bce4f-119">Custom Filter Group</span></span>](custom-filter-group-subpattern.md)
-   [<span data-ttu-id="bce4f-120">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="bce4f-120">Operational workspace</span></span>](workspace-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="bce4f-121">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="bce4f-121">UX guidelines</span></span>
<span data-ttu-id="bce4f-122">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="bce4f-122">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="bce4f-123">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="bce4f-123">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="bce4f-124">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="bce4f-124">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="bce4f-125">フィルター フィールドには、使用可能な値のリストを含むドロップダウンが必要です。</span><span class="sxs-lookup"><span data-stu-id="bce4f-125">The filter field should have a drop-down that contains the list of available values.</span></span>
-   <span data-ttu-id="bce4f-126">フィルター フィールドは、ターゲット ユーザーによって 1 日に複数回変更される予定です。</span><span class="sxs-lookup"><span data-stu-id="bce4f-126">The expectation is that the filter field will be modified multiple times per day by the target user.</span></span> <span data-ttu-id="bce4f-127">フィルター フィールドがより頻度が少ない回数で変更される場合、または主に静的である場合は、構成ダイアログ ボックスに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bce4f-127">If the filter field is modified less often or is primarily static, it should be put in a configuration dialog.</span></span>
-   <span data-ttu-id="bce4f-128">さらにフィルター フィールドが必要な場合は、コンフィギュレーション ダイアログ (最大で5つのフィルター フィールド) に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bce4f-128">If more filter fields are needed, they should be put in a configuration dialog (up to five filter fields).</span></span>

## <a name="examples"></a><span data-ttu-id="bce4f-129">例</span><span class="sxs-lookup"><span data-stu-id="bce4f-129">Examples</span></span>
<span data-ttu-id="bce4f-130">フォーム: **ReqCreatePlanWorkspace** (**すべてのワークスペース** &gt; **マスター プラン**)</span><span class="sxs-lookup"><span data-stu-id="bce4f-130">Form: **ReqCreatePlanWorkspace** (**All workspaces** &gt; **Master Planning**)</span></span> 

<span data-ttu-id="bce4f-131">[![ワークスペース ページ フィルター グループの例](./media/workspacepagefiltergroupexample.png)](./media/workspacepagefiltergroupexample.png)</span><span class="sxs-lookup"><span data-stu-id="bce4f-131">[![workspace Page Filter Group example](./media/workspacepagefiltergroupexample.png)](./media/workspacepagefiltergroupexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="bce4f-132">付録</span><span class="sxs-lookup"><span data-stu-id="bce4f-132">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="bce4f-133">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="bce4f-133">Frequently asked questions</span></span>

<span data-ttu-id="bce4f-134">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="bce4f-134">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="bce4f-135">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="bce4f-135">Open issues</span></span>

<span data-ttu-id="bce4f-136">None</span><span class="sxs-lookup"><span data-stu-id="bce4f-136">None</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]