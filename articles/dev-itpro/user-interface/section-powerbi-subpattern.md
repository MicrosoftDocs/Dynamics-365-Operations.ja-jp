---
title: セクション Power BI のサブパターン
description: この記事では、セクション PowerBI サブパターンに関する情報を提供します。 このサブパターンは、PowerBI コントロールを含むパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。
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
ms.custom: 29431
ms.assetid: 3e760372-e5ee-49d6-b715-c638294345de
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e3a563426bdb63f01b0873a778bb9f3ba9c6023
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851115"
---
# <a name="section-power-bi-subpattern"></a><span data-ttu-id="87487-104">セクション Power BI のサブパターン</span><span class="sxs-lookup"><span data-stu-id="87487-104">Section Power BI subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87487-105">この記事では、セクション PowerBI サブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="87487-105">This article provides information about the Section PowerBI subpattern.</span></span> <span data-ttu-id="87487-106">このサブパターンは、PowerBI コントロールを含むパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="87487-106">This subpattern is used as part of the Operational Workspace pattern, specifically for the panorama section that contains a PowerBI control.</span></span>

<a name="usage"></a><span data-ttu-id="87487-107">用途</span><span class="sxs-lookup"><span data-stu-id="87487-107">Usage</span></span>
-----

<span data-ttu-id="87487-108">セクション PowerBI サブパターンは、PowerBI コントロールを含むパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="87487-108">The Section PowerBI subpattern is used as part of the Operational Workspace pattern, specifically for the panorama section that contains the PowerBI control.</span></span>

## <a name="wireframe"></a><span data-ttu-id="87487-109">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="87487-109">Wireframe</span></span>
<span data-ttu-id="87487-110">[![sectionPowerBIWireframe](./media/sectionpowerbiwireframe.png)](./media/sectionpowerbiwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="87487-110">[![sectionPowerBIWireframe](./media/sectionpowerbiwireframe.png)](./media/sectionpowerbiwireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="87487-111">Microsoft Dynamics AX 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="87487-111">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="87487-112">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="87487-112">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="87487-113">モデル</span><span class="sxs-lookup"><span data-stu-id="87487-113">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="87487-114">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="87487-114">High-level structure</span></span>

<span data-ttu-id="87487-115">TabPage PowerBI (PowerBI)</span><span class="sxs-lookup"><span data-stu-id="87487-115">TabPage PowerBI (PowerBI)</span></span>

### <a name="core-components"></a><span data-ttu-id="87487-116">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="87487-116">Core components</span></span>

<span data-ttu-id="87487-117">セクション PowerBI をワークスペース内の適切なタブ ページに適用します。</span><span class="sxs-lookup"><span data-stu-id="87487-117">Apply Section PowerBI to the appropriate tab page in the workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="87487-118">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="87487-118">Related container patterns</span></span>

-   [<span data-ttu-id="87487-119">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="87487-119">Operational workspace</span></span>](workspace-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="87487-120">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="87487-120">UX guidelines</span></span>
<span data-ttu-id="87487-121">None</span><span class="sxs-lookup"><span data-stu-id="87487-121">None</span></span>

## <a name="examples"></a><span data-ttu-id="87487-122">例</span><span class="sxs-lookup"><span data-stu-id="87487-122">Examples</span></span>
<span data-ttu-id="87487-123">フォーム: **FmClerkWorkspace** (**すべてのワークスペース** &gt; **予約管理**) フォームが表示できる前に、Power BI がコンフィギュレーションされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="87487-123">Form: **FmClerkWorkspace** (**All workspaces** &gt; **Reservation Management**) PowerBI must be configured before the form can appear.</span></span> <span data-ttu-id="87487-124">(PowerBI のコンフィギュレーション方法については、付録を参照してください。)</span><span class="sxs-lookup"><span data-stu-id="87487-124">(For information about how to configure PowerBI, see the Appendix.)</span></span>

## <a name="appendix"></a><span data-ttu-id="87487-125">付録</span><span class="sxs-lookup"><span data-stu-id="87487-125">Appendix</span></span>
### <a name="related-articles"></a><span data-ttu-id="87487-126">関連記事</span><span class="sxs-lookup"><span data-stu-id="87487-126">Related articles</span></span>

-   [<span data-ttu-id="87487-127">ワークスペースの PowerBI 統合の構成</span><span class="sxs-lookup"><span data-stu-id="87487-127">Configuring PowerBI integration for workspaces</span></span>](../analytics/configure-power-bi-integration.md)
-   [<span data-ttu-id="87487-128">Dynamics AX での Power BI 統合</span><span class="sxs-lookup"><span data-stu-id="87487-128">Power BI Integration in Dynamics AX</span></span>](../analytics/power-bi-integration.md)

### <a name="frequently-asked-questions"></a><span data-ttu-id="87487-129">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="87487-129">Frequently asked questions</span></span>

<span data-ttu-id="87487-130">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="87487-130">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

-   <span data-ttu-id="87487-131">**ワークスペースとの統合のために PowerBI をどのようにコンフィギュレーションしますか。**</span><span class="sxs-lookup"><span data-stu-id="87487-131">**How do I configure PowerBI for integration with my workspace?**</span></span>
    -   <span data-ttu-id="87487-132">[ワークスペースの PowerBI 統合のコンフィギュレーション](../analytics/configure-power-bi-integration.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87487-132">See the [Configuring PowerBI integration for workspaces](../analytics/configure-power-bi-integration.md) article.</span></span>

### <a name="open-issues"></a><span data-ttu-id="87487-133">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="87487-133">Open issues</span></span>

<span data-ttu-id="87487-134">None</span><span class="sxs-lookup"><span data-stu-id="87487-134">None</span></span>



