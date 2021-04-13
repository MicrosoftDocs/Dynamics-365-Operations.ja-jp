---
title: テキスト入力のサブパターン
description: この記事では、テキスト入力のサブパターンについて説明します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 12414
ms.assetid: 60279057-6aea-428f-b75c-313ec041c0c0
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c8794770aa5f119df7923bd3e40f867eccfa12c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748763"
---
# <a name="fill-text-subpattern"></a><span data-ttu-id="074a9-103">テキスト入力のサブパターン</span><span class="sxs-lookup"><span data-stu-id="074a9-103">Fill Text subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="074a9-104">この記事では、テキスト入力のサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="074a9-104">This article provides information about the Fill Text subpattern.</span></span> <span data-ttu-id="074a9-105">このサブパターンは、1 つの String コントロールまたは StaticText コントロールをコンテナーの全幅まで広げる必要があるときに使用されます。これにより、ユーザーはより多くの情報を入力する領域を獲得します。</span><span class="sxs-lookup"><span data-stu-id="074a9-105">This subpattern is used when a single String or StaticText control must stretch to the full width of the container, so that users have more space to enter information.</span></span>

<a name="usage"></a><span data-ttu-id="074a9-106">用途</span><span class="sxs-lookup"><span data-stu-id="074a9-106">Usage</span></span>
-----

<span data-ttu-id="074a9-107">テキスト入力は、コンテナーの幅を最大限に拡大する単一の文字列または StaticText コントロールを必要とする場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="074a9-107">Fill Text is used when you need a single String or StaticText control to stretch to the full width of the container.</span></span> <span data-ttu-id="074a9-108">このサブパターンは、通常、ユーザーが情報を入力するために更なる領域を必要とする複数行文字列コントロールに使用されます。</span><span class="sxs-lookup"><span data-stu-id="074a9-108">This subpattern is typically used for multi-line string controls that require more space for users to enter information.</span></span>

## <a name="wireframe"></a><span data-ttu-id="074a9-109">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="074a9-109">Wireframe</span></span>

<span data-ttu-id="074a9-110">[![テキスト入力のサブパターンのワイヤーフレーム](./media/filltext1.png)](./media/filltext1.png)</span><span class="sxs-lookup"><span data-stu-id="074a9-110">[![Fill Text sub-pattern wireframe](./media/filltext1.png)](./media/filltext1.png)</span></span>

## <a name="model"></a><span data-ttu-id="074a9-111">モデル</span><span class="sxs-lookup"><span data-stu-id="074a9-111">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="074a9-112">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="074a9-112">High-level structure</span></span>

<span data-ttu-id="074a9-113">[Container]</span><span class="sxs-lookup"><span data-stu-id="074a9-113">[Container]</span></span>

<span data-ttu-id="074a9-114">文字列 | StaticText</span><span class="sxs-lookup"><span data-stu-id="074a9-114">String | StaticText</span></span>

### <a name="core-components"></a><span data-ttu-id="074a9-115">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="074a9-115">Core components</span></span>

-   <span data-ttu-id="074a9-116">テキスト入力のサブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="074a9-116">Apply the Fill Text subpattern to the container control.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="074a9-117">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="074a9-117">Related container patterns</span></span>

-   [<span data-ttu-id="074a9-118">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="074a9-118">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="074a9-119">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="074a9-119">UX guidelines</span></span>
<span data-ttu-id="074a9-120">None</span><span class="sxs-lookup"><span data-stu-id="074a9-120">None</span></span>

## <a name="examples"></a><span data-ttu-id="074a9-121">例</span><span class="sxs-lookup"><span data-stu-id="074a9-121">Examples</span></span>
<span data-ttu-id="074a9-122">フォーム: **FmRental (Notes)**</span><span class="sxs-lookup"><span data-stu-id="074a9-122">Form: **FmRental (Notes)**</span></span> 

<span data-ttu-id="074a9-123">[![テキスト入力のサブパターンの例](./media/filltext2.png)](./media/filltext2.png)</span><span class="sxs-lookup"><span data-stu-id="074a9-123">[![Fill Text sub-pattern example](./media/filltext2.png)](./media/filltext2.png)</span></span>

## <a name="resources"></a><span data-ttu-id="074a9-124">リソース</span><span class="sxs-lookup"><span data-stu-id="074a9-124">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="074a9-125">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="074a9-125">Typically used by patterns</span></span>

-   [<span data-ttu-id="074a9-126">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="074a9-126">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="074a9-127">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="074a9-127">Details Transaction</span></span>](details-transaction-form-pattern.md)
-   [<span data-ttu-id="074a9-128">簡易詳細</span><span class="sxs-lookup"><span data-stu-id="074a9-128">Simple Details</span></span>](simple-details-form-pattern.md)
-   [<span data-ttu-id="074a9-129">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="074a9-129">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="074a9-130">目次</span><span class="sxs-lookup"><span data-stu-id="074a9-130">Table Of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="074a9-131">ウィザード</span><span class="sxs-lookup"><span data-stu-id="074a9-131">Wizard</span></span>](wizard-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="074a9-132">付録</span><span class="sxs-lookup"><span data-stu-id="074a9-132">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="074a9-133">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="074a9-133">Frequently asked questions</span></span>

<span data-ttu-id="074a9-134">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="074a9-134">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="074a9-135">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="074a9-135">Open issues</span></span>

-   <span data-ttu-id="074a9-136">パターンは、現在、コントロールの **HeightMode** プロパティを **SizeToAvailable** に設定します。</span><span class="sxs-lookup"><span data-stu-id="074a9-136">The pattern currently sets the **HeightMode** property of the control to **SizeToAvailable**.</span></span> <span data-ttu-id="074a9-137">これは、パターンが **SizeToAvailable** コンテナーで使用されている場合、非常に大きい文字列コントロールを生成します。</span><span class="sxs-lookup"><span data-stu-id="074a9-137">This can produce very tall string controls if the pattern is used in a **SizeToAvailable** container.</span></span> <span data-ttu-id="074a9-138">このコントロールで **SizeToContent** 高さを使用するか、またはプロパティをまったく設定せずに、代わりに、開発者に適切なコントロールの高さを決定させるかを調査しています。</span><span class="sxs-lookup"><span data-stu-id="074a9-138">We’re investigating whether this control should use **SizeToContent** height, or whether it should not set the property at all and should instead let the developer decide the appropriate control height.</span></span>






[!INCLUDE[footer-include](../../../includes/footer-banner.md)]