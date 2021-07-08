---
title: セクション Power BI のサブパターン
description: この記事では、セクション PowerBI サブパターンに関する情報を提供します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29431
ms.assetid: 3e760372-e5ee-49d6-b715-c638294345de
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: daedefc3491b18bde9a3838a09ce4bfed59b8710
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189294"
---
# <a name="section-power-bi-subpattern"></a><span data-ttu-id="69384-103">セクション Power BI のサブパターン</span><span class="sxs-lookup"><span data-stu-id="69384-103">Section Power BI subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69384-104">この記事では、セクション PowerBI サブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="69384-104">This article provides information about the Section PowerBI subpattern.</span></span> <span data-ttu-id="69384-105">このサブパターンは、PowerBI コントロールを含むパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="69384-105">This subpattern is used as part of the Operational Workspace pattern, specifically for the panorama section that contains a PowerBI control.</span></span>

## <a name="usage"></a><span data-ttu-id="69384-106">用途</span><span class="sxs-lookup"><span data-stu-id="69384-106">Usage</span></span>

<span data-ttu-id="69384-107">セクション PowerBI サブパターンは、PowerBI コントロールを含むパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="69384-107">The Section PowerBI subpattern is used as part of the Operational Workspace pattern, specifically for the panorama section that contains the PowerBI control.</span></span>

## <a name="wireframe"></a><span data-ttu-id="69384-108">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="69384-108">Wireframe</span></span>
<span data-ttu-id="69384-109">[![Section PowerBI のワイヤーフレーム](./media/sectionpowerbiwireframe.png)](./media/sectionpowerbiwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="69384-109">[![Section PowerBI wireframe](./media/sectionpowerbiwireframe.png)](./media/sectionpowerbiwireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="69384-110">Microsoft Dynamics AX 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="69384-110">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="69384-111">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="69384-111">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="69384-112">モデル</span><span class="sxs-lookup"><span data-stu-id="69384-112">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="69384-113">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="69384-113">High-level structure</span></span>

<span data-ttu-id="69384-114">TabPage PowerBI (PowerBI)</span><span class="sxs-lookup"><span data-stu-id="69384-114">TabPage PowerBI (PowerBI)</span></span>

### <a name="core-components"></a><span data-ttu-id="69384-115">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="69384-115">Core components</span></span>

<span data-ttu-id="69384-116">セクション PowerBI をワークスペース内の適切なタブ ページに適用します。</span><span class="sxs-lookup"><span data-stu-id="69384-116">Apply Section PowerBI to the appropriate tab page in the workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="69384-117">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="69384-117">Related container patterns</span></span>

-   [<span data-ttu-id="69384-118">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="69384-118">Operational workspace</span></span>](workspace-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="69384-119">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="69384-119">UX guidelines</span></span>
<span data-ttu-id="69384-120">None</span><span class="sxs-lookup"><span data-stu-id="69384-120">None</span></span>

## <a name="examples"></a><span data-ttu-id="69384-121">例</span><span class="sxs-lookup"><span data-stu-id="69384-121">Examples</span></span>
<span data-ttu-id="69384-122">フォーム: **FmClerkWorkspace** (**すべてのワークスペース** &gt; **予約管理**) フォームが表示できる前に、PowerBI がコンフィギュレーションされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="69384-122">Form: **FmClerkWorkspace** (**All workspaces** &gt; **Reservation Management**) PowerBI must be configured before the form can appear.</span></span> <span data-ttu-id="69384-123">(PowerBI のコンフィギュレーション方法については、付録を参照してください。)</span><span class="sxs-lookup"><span data-stu-id="69384-123">(For information about how to configure PowerBI, see the Appendix.)</span></span>

## <a name="appendix"></a><span data-ttu-id="69384-124">付録</span><span class="sxs-lookup"><span data-stu-id="69384-124">Appendix</span></span>
### <a name="related-articles"></a><span data-ttu-id="69384-125">関連記事</span><span class="sxs-lookup"><span data-stu-id="69384-125">Related articles</span></span>

-   [<span data-ttu-id="69384-126">ワークスペース用に Power BI 統合を構成する</span><span class="sxs-lookup"><span data-stu-id="69384-126">Configure Power BI integration for workspaces</span></span>](../analytics/configure-power-bi-integration.md)
-   [<span data-ttu-id="69384-127">Power BI 統合を通して利用可能な機能とサービス</span><span class="sxs-lookup"><span data-stu-id="69384-127">Features and services available through Power BI integration</span></span>](../analytics/power-bi-integration.md)

### <a name="frequently-asked-questions"></a><span data-ttu-id="69384-128">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="69384-128">Frequently asked questions</span></span>

<span data-ttu-id="69384-129">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="69384-129">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

-   <span data-ttu-id="69384-130">**ワークスペースとの統合のために PowerBI をどのようにコンフィギュレーションしますか。**</span><span class="sxs-lookup"><span data-stu-id="69384-130">**How do I configure PowerBI for integration with my workspace?**</span></span>
    -   <span data-ttu-id="69384-131">[ワークスペースの Power BI 統合の構成](../analytics/configure-power-bi-integration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="69384-131">See the [Configure Power BI integration for workspaces](../analytics/configure-power-bi-integration.md) article.</span></span>

### <a name="open-issues"></a><span data-ttu-id="69384-132">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="69384-132">Open issues</span></span>

<span data-ttu-id="69384-133">なし</span><span class="sxs-lookup"><span data-stu-id="69384-133">None</span></span>





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]