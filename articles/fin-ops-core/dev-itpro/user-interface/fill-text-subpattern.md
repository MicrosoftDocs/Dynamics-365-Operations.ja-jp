---
title: テキスト入力のサブパターン
description: この記事では、テキスト入力のサブパターンについて説明します。 このサブパターンは、1 つの String コントロールまたは StaticText コントロールをコンテナーの全幅まで広げる必要があるときに使用されます。これにより、ユーザーはより多くの情報を入力する領域を獲得します。
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
ms.custom: 12414
ms.assetid: 60279057-6aea-428f-b75c-313ec041c0c0
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91feabff07cc87bebd34ff6ee72c1f14b5f10b69
ms.sourcegitcommit: 17fe0218e8e3f2f4c57c73c0c438a6ebf1ef32a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/01/2020
ms.locfileid: "3329891"
---
# <a name="fill-text-subpattern"></a><span data-ttu-id="f6200-104">テキスト入力のサブパターン</span><span class="sxs-lookup"><span data-stu-id="f6200-104">Fill Text subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6200-105">この記事では、テキスト入力のサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f6200-105">This article provides information about the Fill Text subpattern.</span></span> <span data-ttu-id="f6200-106">このサブパターンは、1 つの String コントロールまたは StaticText コントロールをコンテナーの全幅まで広げる必要があるときに使用されます。これにより、ユーザーはより多くの情報を入力する領域を獲得します。</span><span class="sxs-lookup"><span data-stu-id="f6200-106">This subpattern is used when a single String or StaticText control must stretch to the full width of the container, so that users have more space to enter information.</span></span>

<a name="usage"></a><span data-ttu-id="f6200-107">用途</span><span class="sxs-lookup"><span data-stu-id="f6200-107">Usage</span></span>
-----

<span data-ttu-id="f6200-108">テキスト入力は、コンテナーの幅を最大限に拡大する単一の文字列または StaticText コントロールを必要とする場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f6200-108">Fill Text is used when you need a single String or StaticText control to stretch to the full width of the container.</span></span> <span data-ttu-id="f6200-109">このサブパターンは、通常、ユーザーが情報を入力するために更なる領域を必要とする複数行文字列コントロールに使用されます。</span><span class="sxs-lookup"><span data-stu-id="f6200-109">This subpattern is typically used for multi-line string controls that require more space for users to enter information.</span></span>

## <a name="wireframe"></a><span data-ttu-id="f6200-110">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="f6200-110">Wireframe</span></span>

<span data-ttu-id="f6200-111">[![テキスト入力のサブパターンのワイヤーフレーム](./media/filltext1.png)](./media/filltext1.png)</span><span class="sxs-lookup"><span data-stu-id="f6200-111">[![Fill Text sub-pattern wireframe](./media/filltext1.png)](./media/filltext1.png)</span></span>

## <a name="model"></a><span data-ttu-id="f6200-112">モデル</span><span class="sxs-lookup"><span data-stu-id="f6200-112">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="f6200-113">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="f6200-113">High-level structure</span></span>

<span data-ttu-id="f6200-114">[Container]</span><span class="sxs-lookup"><span data-stu-id="f6200-114">[Container]</span></span>

<span data-ttu-id="f6200-115">文字列 | StaticText</span><span class="sxs-lookup"><span data-stu-id="f6200-115">String | StaticText</span></span>

### <a name="core-components"></a><span data-ttu-id="f6200-116">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f6200-116">Core components</span></span>

-   <span data-ttu-id="f6200-117">テキスト入力のサブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="f6200-117">Apply the Fill Text subpattern to the container control.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="f6200-118">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="f6200-118">Related container patterns</span></span>

-   [<span data-ttu-id="f6200-119">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="f6200-119">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="f6200-120">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="f6200-120">UX guidelines</span></span>
<span data-ttu-id="f6200-121">None</span><span class="sxs-lookup"><span data-stu-id="f6200-121">None</span></span>

## <a name="examples"></a><span data-ttu-id="f6200-122">例</span><span class="sxs-lookup"><span data-stu-id="f6200-122">Examples</span></span>
<span data-ttu-id="f6200-123">フォーム: **FmRental (Notes)**</span><span class="sxs-lookup"><span data-stu-id="f6200-123">Form: **FmRental (Notes)**</span></span> 

<span data-ttu-id="f6200-124">[![テキスト入力のサブパターンの例](./media/filltext2.png)](./media/filltext2.png)</span><span class="sxs-lookup"><span data-stu-id="f6200-124">[![Fill Text sub-pattern example](./media/filltext2.png)](./media/filltext2.png)</span></span>

## <a name="resources"></a><span data-ttu-id="f6200-125">リソース</span><span class="sxs-lookup"><span data-stu-id="f6200-125">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="f6200-126">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="f6200-126">Typically used by patterns</span></span>

-   [<span data-ttu-id="f6200-127">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="f6200-127">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="f6200-128">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="f6200-128">Details Transaction</span></span>](details-transaction-form-pattern.md)
-   [<span data-ttu-id="f6200-129">簡易詳細</span><span class="sxs-lookup"><span data-stu-id="f6200-129">Simple Details</span></span>](simple-details-form-pattern.md)
-   [<span data-ttu-id="f6200-130">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="f6200-130">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="f6200-131">目次</span><span class="sxs-lookup"><span data-stu-id="f6200-131">Table Of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="f6200-132">ウィザード</span><span class="sxs-lookup"><span data-stu-id="f6200-132">Wizard</span></span>](wizard-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="f6200-133">付録</span><span class="sxs-lookup"><span data-stu-id="f6200-133">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="f6200-134">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="f6200-134">Frequently asked questions</span></span>

<span data-ttu-id="f6200-135">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="f6200-135">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="f6200-136">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="f6200-136">Open issues</span></span>

-   <span data-ttu-id="f6200-137">パターンは、現在、コントロールの **HeightMode** プロパティを **SizeToAvailable** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f6200-137">The pattern currently sets the **HeightMode** property of the control to **SizeToAvailable**.</span></span> <span data-ttu-id="f6200-138">これは、パターンが **SizeToAvailable** コンテナーで使用されている場合、非常に大きい文字列コントロールを生成します。</span><span class="sxs-lookup"><span data-stu-id="f6200-138">This can produce very tall string controls if the pattern is used in a **SizeToAvailable** container.</span></span> <span data-ttu-id="f6200-139">このコントロールで **SizeToContent** 高さを使用するか、またはプロパティをまったく設定せずに、代わりに、開発者に適切なコントロールの高さを決定させるかを調査しています。</span><span class="sxs-lookup"><span data-stu-id="f6200-139">We’re investigating whether this control should use **SizeToContent** height, or whether it should not set the property at all and should instead let the developer decide the appropriate control height.</span></span>




