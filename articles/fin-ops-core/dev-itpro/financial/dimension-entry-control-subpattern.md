---
title: 分析コード エントリ コントロールのサブパターン
description: この記事では、分析コード エントリ コントロールのサブパターンについて説明します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 15951
ms.assetid: 6baee22e-2a86-428c-b9e2-178581c57830
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c546e4639ae0310a66974c47add598d80f0043a4
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130779"
---
# <a name="dimension-entry-control-subpattern"></a><span data-ttu-id="33a4d-103">分析コード エントリ コントロールのサブパターン</span><span class="sxs-lookup"><span data-stu-id="33a4d-103">Dimension Entry Control subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33a4d-104">この記事では、分析コード エントリ コントロールのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="33a4d-104">This article provides information about the Dimension Entry Control subpattern.</span></span> <span data-ttu-id="33a4d-105">このサブパターンは、分析コード エントリ コントロール (DEC) を使用するグループまたはタブ ページがあるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="33a4d-105">This subpattern is used when you have a group or tab page that uses the Dimension Entry control (DEC).</span></span> 

## <a name="usage"></a><span data-ttu-id="33a4d-106">用途</span><span class="sxs-lookup"><span data-stu-id="33a4d-106">Usage</span></span>

<span data-ttu-id="33a4d-107">分析コード エントリ コントロール パターンは、分析コード エントリ コントロール (DEC) を使用するグループまたはタブ ページがあるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="33a4d-107">The Dimension Entry Control pattern is used when you have a group or tab page that uses the Dimension Entry control (DEC).</span></span>

## <a name="wireframe"></a><span data-ttu-id="33a4d-108">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="33a4d-108">Wireframe</span></span>

![分析コード エントリ コントロールのサブパターンのワイヤーフレーム](media/decwireframe.png)

## <a name="model"></a><span data-ttu-id="33a4d-110">モデル</span><span class="sxs-lookup"><span data-stu-id="33a4d-110">Model</span></span>

### <a name="high-level-structure"></a><span data-ttu-id="33a4d-111">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="33a4d-111">High-level structure</span></span>

<span data-ttu-id="33a4d-112">TabPage | Group *TopFieldGroup (グループ) \[オプション\]* – **注:** フィールド サブパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="33a4d-112">TabPage | Group *TopFieldGroup (Group) \[Optional\]* – **Note:** A field subpattern is used.</span></span>

<span data-ttu-id="33a4d-113">*DECGroup (グループ) \[0..N\]* 分析コード エントリ コントロール *分析コード エントリ コントロール \[0..N\]* *BottomFieldGroup (グループ) \[オプション\]* – **注記:** フィールド サブパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="33a4d-113">*DECGroup (Group) \[0..N\]* Dimension Entry Control *Dimension Entry Control \[0..N\]* *BottomFieldGroup (Group) \[Optional\]* – **Note:** A field subpattern is used.</span></span>

### <a name="core-components"></a><span data-ttu-id="33a4d-114">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="33a4d-114">Core components</span></span>

- <span data-ttu-id="33a4d-115">分析コード エントリ コントロールのサブパターンを TabPage コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="33a4d-115">Apply the Dimension Entry Control subpattern to the TabPage control.</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="33a4d-116">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="33a4d-116">UX guidelines</span></span>

<span data-ttu-id="33a4d-117">なし。</span><span class="sxs-lookup"><span data-stu-id="33a4d-117">None.</span></span>

## <a name="examples"></a><span data-ttu-id="33a4d-118">例</span><span class="sxs-lookup"><span data-stu-id="33a4d-118">Examples</span></span>

<span data-ttu-id="33a4d-119">フォーム: **CustTable (TabFinancialDimensions)**</span><span class="sxs-lookup"><span data-stu-id="33a4d-119">Form: **CustTable (TabFinancialDimensions)**</span></span>

![TabFinancialDimensions を使用した CustTable の例](media/decexample.png)

## <a name="appendix"></a><span data-ttu-id="33a4d-121">付録</span><span class="sxs-lookup"><span data-stu-id="33a4d-121">Appendix</span></span>

### <a name="frequently-asked-questions"></a><span data-ttu-id="33a4d-122">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="33a4d-122">Frequently asked questions</span></span>

<span data-ttu-id="33a4d-123">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="33a4d-123">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="33a4d-124">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="33a4d-124">Open issues</span></span>

<span data-ttu-id="33a4d-125">なし。</span><span class="sxs-lookup"><span data-stu-id="33a4d-125">None.</span></span>
