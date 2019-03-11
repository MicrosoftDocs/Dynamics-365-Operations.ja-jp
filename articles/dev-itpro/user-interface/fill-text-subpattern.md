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
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 12414
ms.assetid: 60279057-6aea-428f-b75c-313ec041c0c0
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6625e628ac4c0bdd551acb8b6f7e4fd57e0c057
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369970"
---
# <a name="fill-text-subpattern"></a><span data-ttu-id="699f1-104">テキスト入力のサブパターン</span><span class="sxs-lookup"><span data-stu-id="699f1-104">Fill Text subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="699f1-105">この記事では、テキスト入力のサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="699f1-105">This article provides information about the Fill Text subpattern.</span></span> <span data-ttu-id="699f1-106">このサブパターンは、1 つの String コントロールまたは StaticText コントロールをコンテナーの全幅まで広げる必要があるときに使用されます。これにより、ユーザーはより多くの情報を入力する領域を獲得します。</span><span class="sxs-lookup"><span data-stu-id="699f1-106">This subpattern is used when a single String or StaticText control must stretch to the full width of the container, so that users have more space to enter information.</span></span>

<a name="usage"></a><span data-ttu-id="699f1-107">用途</span><span class="sxs-lookup"><span data-stu-id="699f1-107">Usage</span></span>
-----

<span data-ttu-id="699f1-108">テキスト入力は、コンテナーの幅を最大限に拡大する単一の文字列または StaticText コントロールを必要とする場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="699f1-108">Fill Text is used when you need a single String or StaticText control to stretch to the full width of the container.</span></span> <span data-ttu-id="699f1-109">このサブパターンは、通常、ユーザーが情報を入力するために更なる領域を必要とする複数行文字列コントロールに使用されます。</span><span class="sxs-lookup"><span data-stu-id="699f1-109">This subpattern is typically used for multi-line string controls that require more space for users to enter information.</span></span>

## <a name="wireframe"></a><span data-ttu-id="699f1-110">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="699f1-110">Wireframe</span></span>

<span data-ttu-id="699f1-111">[![テキスト入力のサブパターンのワイヤーフレーム](./media/filltext1.png)](./media/filltext1.png)</span><span class="sxs-lookup"><span data-stu-id="699f1-111">[![Fill Text sub-pattern wireframe](./media/filltext1.png)](./media/filltext1.png)</span></span>

## <a name="model"></a><span data-ttu-id="699f1-112">モデル</span><span class="sxs-lookup"><span data-stu-id="699f1-112">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="699f1-113">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="699f1-113">High-level structure</span></span>

<span data-ttu-id="699f1-114">[Container]</span><span class="sxs-lookup"><span data-stu-id="699f1-114">[Container]</span></span>

<span data-ttu-id="699f1-115">文字列 | StaticText</span><span class="sxs-lookup"><span data-stu-id="699f1-115">String | StaticText</span></span>

### <a name="core-components"></a><span data-ttu-id="699f1-116">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="699f1-116">Core components</span></span>

-   <span data-ttu-id="699f1-117">テキスト入力のサブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="699f1-117">Apply the Fill Text subpattern to the container control.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="699f1-118">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="699f1-118">Related container patterns</span></span>

-   [<span data-ttu-id="699f1-119">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="699f1-119">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="699f1-120">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="699f1-120">UX guidelines</span></span>
<span data-ttu-id="699f1-121">None</span><span class="sxs-lookup"><span data-stu-id="699f1-121">None</span></span>

## <a name="examples"></a><span data-ttu-id="699f1-122">例</span><span class="sxs-lookup"><span data-stu-id="699f1-122">Examples</span></span>
<span data-ttu-id="699f1-123">フォーム: **FmRental (Notes)**</span><span class="sxs-lookup"><span data-stu-id="699f1-123">Form: **FmRental (Notes)**</span></span> 

<span data-ttu-id="699f1-124">[![テキスト入力のサブパターンの例](./media/filltext2.png)](./media/filltext2.png)</span><span class="sxs-lookup"><span data-stu-id="699f1-124">[![Fill Text sub-pattern example](./media/filltext2.png)](./media/filltext2.png)</span></span>

## <a name="resources"></a><span data-ttu-id="699f1-125">リソース</span><span class="sxs-lookup"><span data-stu-id="699f1-125">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="699f1-126">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="699f1-126">Typically used by patterns</span></span>

-   [<span data-ttu-id="699f1-127">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="699f1-127">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="699f1-128">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="699f1-128">Details Transaction</span></span>](details-transaction-form-pattern.md)
-   [<span data-ttu-id="699f1-129">簡易詳細</span><span class="sxs-lookup"><span data-stu-id="699f1-129">Simple Details</span></span>](simple-details-form-pattern.md)
-   [<span data-ttu-id="699f1-130">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="699f1-130">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="699f1-131">目次</span><span class="sxs-lookup"><span data-stu-id="699f1-131">Table Of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="699f1-132">ウィザード</span><span class="sxs-lookup"><span data-stu-id="699f1-132">Wizard</span></span>](wizard-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="699f1-133">付録</span><span class="sxs-lookup"><span data-stu-id="699f1-133">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="699f1-134">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="699f1-134">Frequently asked questions</span></span>

<span data-ttu-id="699f1-135">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="699f1-135">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="699f1-136">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="699f1-136">Open issues</span></span>

-   <span data-ttu-id="699f1-137">パターンは、現在、コントロールの **HeightMode** プロパティを **SizeToAvailable** に設定します。</span><span class="sxs-lookup"><span data-stu-id="699f1-137">The pattern currently sets the **HeightMode** property of the control to **SizeToAvailable**.</span></span> <span data-ttu-id="699f1-138">これは、パターンが **SizeToAvailable** コンテナーで使用されている場合、非常に大きい文字列コントロールを生成します。</span><span class="sxs-lookup"><span data-stu-id="699f1-138">This can produce very tall string controls if the pattern is used in a **SizeToAvailable** container.</span></span> <span data-ttu-id="699f1-139">このコントロールで **SizeToContent** 高さを使用するか、またはプロパティをまったく設定せずに、代わりに、開発者に適切なコントロールの高さを決定させるかを調査しています。</span><span class="sxs-lookup"><span data-stu-id="699f1-139">We’re investigating whether this control should use **SizeToContent** height, or whether it should not set the property at all and should instead let the developer decide the appropriate control height.</span></span>




