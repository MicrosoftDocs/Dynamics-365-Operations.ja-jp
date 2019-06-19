---
title: 分析コード式ビルダーのサブパターン
description: この記事では、分析コード式ビルダー コントロールを使用するコンテナー コントロールに適用される分析コード式ビルダーのサブパターンについて説明します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 29451
ms.assetid: 6ab0f75d-3168-4dfe-b2ce-d17d3861216e
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b09476da4fa764df3bac30d0097648d8b7ad6ce
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555608"
---
# <a name="dimension-expression-builder-subpattern"></a><span data-ttu-id="5de05-103">分析コード式ビルダーのサブパターン</span><span class="sxs-lookup"><span data-stu-id="5de05-103">Dimension Expression Builder subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5de05-104">この記事では、分析コード式ビルダー コントロールを使用するコンテナー コントロールに適用される分析コード式ビルダーのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5de05-104">This article describes the Dimension Expression Builder subpattern, which is applied to container controls that use the Dimension Expression Builder control.</span></span>  

<a name="usage"></a><span data-ttu-id="5de05-105">用途</span><span class="sxs-lookup"><span data-stu-id="5de05-105">Usage</span></span>
-----

<span data-ttu-id="5de05-106">分析コード式ビルダー パターンは、分析コード式ビルダー コントロールを使用するグループまたはタブ ページがあるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="5de05-106">The Dimension Expression Builder pattern is used when you have a group or tab page that uses the Dimension Expression Builder control.</span></span>

## <a name="wireframe"></a><span data-ttu-id="5de05-107">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="5de05-107">Wireframe</span></span>
<span data-ttu-id="5de05-108">[![dimensionExpressionBuilderWireframe](./media/dimensionexpressionbuilderwireframe.png)](./media/dimensionexpressionbuilderwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="5de05-108">[![dimensionExpressionBuilderWireframe](./media/dimensionexpressionbuilderwireframe.png)](./media/dimensionexpressionbuilderwireframe.png)</span></span>

## <a name="model"></a><span data-ttu-id="5de05-109">モデル</span><span class="sxs-lookup"><span data-stu-id="5de05-109">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="5de05-110">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="5de05-110">High-level structure</span></span>

<span data-ttu-id="5de05-111">TabPage | Group</span><span class="sxs-lookup"><span data-stu-id="5de05-111">TabPage | Group</span></span>

<span data-ttu-id="5de05-112">*TopFieldGroup (グループ) \[オプション\]* – **注記:** フィールド サブパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5de05-112">*TopFieldGroup (Group) \[Optional\]* – **Note:** A field subpattern is used.</span></span>

<span data-ttu-id="5de05-113">*DEBGroup (グループ)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="5de05-113">*DEBGroup (Group) \[0..N\]*</span></span>

<span data-ttu-id="5de05-114">分析コード式ビルダー</span><span class="sxs-lookup"><span data-stu-id="5de05-114">Dimension Expression Builder</span></span>

<span data-ttu-id="5de05-115">*分析コード式ビルダー \[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="5de05-115">*Dimension Expression Builder \[0..N\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="5de05-116">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="5de05-116">Core components</span></span>

-   <span data-ttu-id="5de05-117">分析コード式ビルダーのサブパターンを TabPage またはグループ コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="5de05-117">Apply the Dimension Expression Builder subpattern to the TabPage or Group control.</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="5de05-118">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="5de05-118">UX guidelines</span></span>
<span data-ttu-id="5de05-119">None</span><span class="sxs-lookup"><span data-stu-id="5de05-119">None</span></span>

## <a name="examples"></a><span data-ttu-id="5de05-120">例</span><span class="sxs-lookup"><span data-stu-id="5de05-120">Examples</span></span>
<span data-ttu-id="5de05-121">フォーム: **BudgetControlConfiguration (RulesDetailsCriteriaFastTabPage)** (**予算作成** &gt; **設定** &gt; **予算管理** &gt; **予算管理コンフィギュレーション**) [![dimensionExpressionBuilderExample](./media/dimensionexpressionbuilderexample.png)](./media/dimensionexpressionbuilderexample.png)</span><span class="sxs-lookup"><span data-stu-id="5de05-121">Form: **BudgetControlConfiguration (RulesDetailsCriteriaFastTabPage)** (**Budgeting** &gt; **Setup** &gt; **Budget control** &gt; **Budget control configuration**) [![dimensionExpressionBuilderExample](./media/dimensionexpressionbuilderexample.png)](./media/dimensionexpressionbuilderexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="5de05-122">付録</span><span class="sxs-lookup"><span data-stu-id="5de05-122">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="5de05-123">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="5de05-123">Frequently asked questions</span></span>

<span data-ttu-id="5de05-124">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="5de05-124">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="5de05-125">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="5de05-125">Open issues</span></span>

<span data-ttu-id="5de05-126">None</span><span class="sxs-lookup"><span data-stu-id="5de05-126">None</span></span>



