---
title: 分析コード エントリ コントロールのサブパターン
description: この記事では、分析コード エントリ コントロールのサブパターンについて説明します。 このサブパターンは、分析コード エントリ コントロール (DEC) を使用するグループまたはタブ ページがあるときに使用されます。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 15951
ms.assetid: 6baee22e-2a86-428c-b9e2-178581c57830
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6fd435f4eb19427b55b0776dbde8bbbd31b0d722
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191570"
---
# <a name="dimension-entry-control-subpattern"></a><span data-ttu-id="07d28-104">分析コード エントリ コントロールのサブパターン</span><span class="sxs-lookup"><span data-stu-id="07d28-104">Dimension Entry Control subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07d28-105">この記事では、分析コード エントリ コントロールのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="07d28-105">This article provides information about the Dimension Entry Control subpattern.</span></span> <span data-ttu-id="07d28-106">このサブパターンは、分析コード エントリ コントロール (DEC) を使用するグループまたはタブ ページがあるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="07d28-106">This subpattern is used when you have a group or tab page that uses the Dimension Entry control (DEC).</span></span> 

<a name="usage"></a><span data-ttu-id="07d28-107">用途</span><span class="sxs-lookup"><span data-stu-id="07d28-107">Usage</span></span>
-----

<span data-ttu-id="07d28-108">分析コード エントリ コントロール パターンは、分析コード エントリ コントロール (DEC) を使用するグループまたはタブ ページがあるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="07d28-108">The Dimension Entry Control pattern is used when you have a group or tab page that uses the Dimension Entry control (DEC).</span></span>

## <a name="wireframe"></a><span data-ttu-id="07d28-109">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="07d28-109">Wireframe</span></span>
<span data-ttu-id="07d28-110">[![decWireframe](./media/decwireframe.png)](./media/decwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="07d28-110">[![decWireframe](./media/decwireframe.png)](./media/decwireframe.png)</span></span>  

## <a name="model"></a><span data-ttu-id="07d28-111">モデル</span><span class="sxs-lookup"><span data-stu-id="07d28-111">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="07d28-112">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="07d28-112">High-level structure</span></span>

<span data-ttu-id="07d28-113">TabPage | Group *TopFieldGroup (グループ) \[オプション\]* – **注:** フィールド サブパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07d28-113">TabPage | Group *TopFieldGroup (Group) \[Optional\]* – **Note:** A field subpattern is used.</span></span> <span data-ttu-id="07d28-114">*DECGroup (グループ) \[0..N\]* 分析コード エントリ コントロール *分析コード エントリ コントロール \[0..N\]* *BottomFieldGroup (グループ) \[オプション\]* – **注記:** フィールド サブパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="07d28-114">*DECGroup (Group) \[0..N\]* Dimension Entry Control *Dimension Entry Control \[0..N\]* *BottomFieldGroup (Group) \[Optional\]* – **Note:** A field subpattern is used.</span></span>

### <a name="core-components"></a><span data-ttu-id="07d28-115">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="07d28-115">Core components</span></span>

-   <span data-ttu-id="07d28-116">分析コード エントリ コントロールのサブパターンを TabPage コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="07d28-116">Apply the Dimension Entry Control subpattern to the TabPage control.</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="07d28-117">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="07d28-117">UX guidelines</span></span>
<span data-ttu-id="07d28-118">なし。</span><span class="sxs-lookup"><span data-stu-id="07d28-118">None.</span></span>

## <a name="examples"></a><span data-ttu-id="07d28-119">例</span><span class="sxs-lookup"><span data-stu-id="07d28-119">Examples</span></span>
<span data-ttu-id="07d28-120">フォーム: **CustTable (TabFinancialDimensions)** [![decExample](./media/decexample.png)](./media/decexample.png)</span><span class="sxs-lookup"><span data-stu-id="07d28-120">Form: **CustTable (TabFinancialDimensions)** [![decExample](./media/decexample.png)](./media/decexample.png)</span></span>    

## <a name="appendix"></a><span data-ttu-id="07d28-121">付録</span><span class="sxs-lookup"><span data-stu-id="07d28-121">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="07d28-122">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="07d28-122">Frequently asked questions</span></span>

<span data-ttu-id="07d28-123">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="07d28-123">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="07d28-124">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="07d28-124">Open issues</span></span>

<span data-ttu-id="07d28-125">なし。</span><span class="sxs-lookup"><span data-stu-id="07d28-125">None.</span></span>



