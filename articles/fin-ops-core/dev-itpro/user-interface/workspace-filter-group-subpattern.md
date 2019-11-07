---
title: ワークスペース ページ フィルター グループのサブパターン
description: この記事では、ワークスペース ページ フィルター グループのサブパターンについて説明します。 このサブパターンは、ワークスペースがフォーム上で 1 つのワークスペース全体にかかわるフィルターを公開する必要があるとき、運用ワークスペース パターンの一部として使用されます。
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
ms.custom: 29231
ms.assetid: 90d5a70b-a99b-4e79-a52d-b4ef5a942607
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 646f97b91501044439df09159de1404636920fc7
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658796"
---
# <a name="workspace-page-filter-group-subpattern"></a><span data-ttu-id="63cdb-104">ワークスペース ページ フィルター グループのサブパターン</span><span class="sxs-lookup"><span data-stu-id="63cdb-104">Workspace Page Filter Group subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63cdb-105">この記事では、ワークスペース ページ フィルター グループのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="63cdb-105">This article provides information about the Workspace Page Filter Group subpattern.</span></span> <span data-ttu-id="63cdb-106">このサブパターンは、ワークスペースがフォーム上で 1 つのワークスペース全体にかかわるフィルターを公開する必要があるとき、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="63cdb-106">This subpattern is used as part of the Operational Workspace pattern when a workspace must expose a single workspace-wide filter on the form.</span></span>

<a name="usage"></a><span data-ttu-id="63cdb-107">用途</span><span class="sxs-lookup"><span data-stu-id="63cdb-107">Usage</span></span>
-----

<span data-ttu-id="63cdb-108">ワークスペース ページ フィルター グループのサブパターンは、特にワークスペースがフォーム上で 1 つのワークスペース全体にかかわるフィルターを公開する必要があるときに、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="63cdb-108">The Workspace Page Filter Group subpattern is used as part of the Operational Workspace pattern, specifically when a workspace must expose a single workspace-wide filter on the form.</span></span>

## <a name="wireframe"></a><span data-ttu-id="63cdb-109">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="63cdb-109">Wireframe</span></span>

<span data-ttu-id="63cdb-110">[![ワークスペース ページ フィルター グループのサブパターンのワイヤーフレーム](./media/workspacepagefiltergroupwireframe.png)](./media/workspacepagefiltergroupwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="63cdb-110">[![Wireframe for Workspace Page Filter Group subpattern](./media/workspacepagefiltergroupwireframe.png)](./media/workspacepagefiltergroupwireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="63cdb-111">Microsoft Dynamics AX 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="63cdb-111">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="63cdb-112">このパターンは、Microsoft Dynamics AX 2012 には存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="63cdb-112">This pattern didn't exist in Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="63cdb-113">モデル</span><span class="sxs-lookup"><span data-stu-id="63cdb-113">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="63cdb-114">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="63cdb-114">High-level structure</span></span>

- <span data-ttu-id="63cdb-115">グループ化</span><span class="sxs-lookup"><span data-stu-id="63cdb-115">Group</span></span>

    - <span data-ttu-id="63cdb-116">フィールド ($Field)</span><span class="sxs-lookup"><span data-stu-id="63cdb-116">Field ($Field)</span></span>

### <a name="core-components"></a><span data-ttu-id="63cdb-117">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="63cdb-117">Core components</span></span>

<span data-ttu-id="63cdb-118">ワークスペース ページ フィルター グループを (運用) ワークスペースの適切なグループに適用します。</span><span class="sxs-lookup"><span data-stu-id="63cdb-118">Apply Workspace Page Filter Group to the appropriate group in an (operational) workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="63cdb-119">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="63cdb-119">Related container patterns</span></span>

-   [<span data-ttu-id="63cdb-120">カスタム フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="63cdb-120">Custom Filter Group</span></span>](custom-filter-group-subpattern.md)
-   [<span data-ttu-id="63cdb-121">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="63cdb-121">Operational workspace</span></span>](workspace-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="63cdb-122">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="63cdb-122">UX guidelines</span></span>
<span data-ttu-id="63cdb-123">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="63cdb-123">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="63cdb-124">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="63cdb-124">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="63cdb-125">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="63cdb-125">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="63cdb-126">フィルター フィールドには、使用可能な値のリストを含むドロップダウンが必要です。</span><span class="sxs-lookup"><span data-stu-id="63cdb-126">The filter field should have a drop-down that contains the list of available values.</span></span>
-   <span data-ttu-id="63cdb-127">フィルター フィールドは、ターゲット ユーザーによって 1 日に複数回変更される予定です。</span><span class="sxs-lookup"><span data-stu-id="63cdb-127">The expectation is that the filter field will be modified multiple times per day by the target user.</span></span> <span data-ttu-id="63cdb-128">フィルター フィールドがより頻度が少ない回数で変更される場合、または主に静的である場合は、構成ダイアログ ボックスに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63cdb-128">If the filter field is modified less often or is primarily static, it should be put in a configuration dialog.</span></span>
-   <span data-ttu-id="63cdb-129">さらにフィルター フィールドが必要な場合は、コンフィギュレーション ダイアログ (最大で5つのフィルター フィールド) に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63cdb-129">If more filter fields are needed, they should be put in a configuration dialog (up to five filter fields).</span></span>

## <a name="examples"></a><span data-ttu-id="63cdb-130">例</span><span class="sxs-lookup"><span data-stu-id="63cdb-130">Examples</span></span>
<span data-ttu-id="63cdb-131">フォーム: **ReqCreatePlanWorkspace** (**すべてのワークスペース** &gt; **マスター プラン**)</span><span class="sxs-lookup"><span data-stu-id="63cdb-131">Form: **ReqCreatePlanWorkspace** (**All workspaces** &gt; **Master Planning**)</span></span> 

<span data-ttu-id="63cdb-132">[![ワークスペース ページ フィルター グループの例](./media/workspacepagefiltergroupexample.png)](./media/workspacepagefiltergroupexample.png)</span><span class="sxs-lookup"><span data-stu-id="63cdb-132">[![workspace Page Filter Group example](./media/workspacepagefiltergroupexample.png)](./media/workspacepagefiltergroupexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="63cdb-133">付録</span><span class="sxs-lookup"><span data-stu-id="63cdb-133">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="63cdb-134">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="63cdb-134">Frequently asked questions</span></span>

<span data-ttu-id="63cdb-135">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="63cdb-135">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="63cdb-136">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="63cdb-136">Open issues</span></span>

<span data-ttu-id="63cdb-137">None</span><span class="sxs-lookup"><span data-stu-id="63cdb-137">None</span></span>
