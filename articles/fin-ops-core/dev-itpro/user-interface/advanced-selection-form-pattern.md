---
title: 高度な選択のフォーム パターン
description: この記事では、高度な選択フォーム パターンに関する情報を提供します。 このダイアログ フォーム パターンを使用すると、ユーザーは大規模な全体のリストから項目をフィルターして選択できます。 リスト パネルのパターンと同様に、このパターンは主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。
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
ms.custom: 29171
ms.assetid: c3c5eea7-f771-41ea-9976-8d0e1f3d3f25
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d866be21deb82dffe9984b2230743aeb08d8262
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812032"
---
# <a name="advanced-selection-form-pattern"></a><span data-ttu-id="2e42e-105">高度な選択のフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="2e42e-105">Advanced selection form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e42e-106">この記事では、高度な選択フォーム パターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="2e42e-106">This article provides information about the Advanced Selection form pattern.</span></span> <span data-ttu-id="2e42e-107">このダイアログ フォーム パターンを使用すると、ユーザーは大規模な全体のリストから項目をフィルターして選択できます。</span><span class="sxs-lookup"><span data-stu-id="2e42e-107">This Dialog form pattern lets users filter and select items from a large, wide list.</span></span> <span data-ttu-id="2e42e-108">リスト パネルのパターンと同様に、このパターンは主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e42e-108">Like the List Panel pattern, this pattern should be used when the primary user task is to select a set of items.</span></span>

<a name="usage"></a><span data-ttu-id="2e42e-109">用途</span><span class="sxs-lookup"><span data-stu-id="2e42e-109">Usage</span></span>
-----

<span data-ttu-id="2e42e-110">高度な選択フォーム パターンは、主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e42e-110">The Advanced Selection form pattern should be used when the primary user task is to select a set of items.</span></span> <span data-ttu-id="2e42e-111">このタスクは、通常、複数選択リストによって達成されます。</span><span class="sxs-lookup"><span data-stu-id="2e42e-111">This task is usually accomplished through a multi-select list.</span></span> <span data-ttu-id="2e42e-112">ただし、多くのシナリオでは、ユーザーは連続していない品目を選択する必要があり、同時に、選択する品目の一覧を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e42e-112">However, in many scenarios, users must select items that aren't contiguous and, at the same time, must see the set of items that they are selecting.</span></span> <span data-ttu-id="2e42e-113">このパターンは、ユーザーが 1 つのリスト内の項目を選択して別のリストに追加する点において、リスト パネルのパターンと似ています。</span><span class="sxs-lookup"><span data-stu-id="2e42e-113">This pattern resembles the List panel pattern, in that the user selects items in one list and adds them to another.</span></span> <span data-ttu-id="2e42e-114">ただし、このパターンにはカスタム フィルターおよび上部の「広い」リストがあり、およびページの画面「不動産」のほとんどを使用します (通常、大きなダイアログ)。</span><span class="sxs-lookup"><span data-stu-id="2e42e-114">However, this pattern allows for custom filters and a “wide” list on top, and uses most of the screen "real estate" of the page (typically, it's a Large dialog).</span></span> <span data-ttu-id="2e42e-115">大規模かつ広範囲のリストでフィルター処理および選択しなければならない場合にこのパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="2e42e-115">Use this pattern when a user must be able to filter and select in a large, wide list.</span></span>

## <a name="wireframe"></a><span data-ttu-id="2e42e-116">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="2e42e-116">Wireframe</span></span>

<span data-ttu-id="2e42e-117">[![高度な選択パターン ワイヤーフレーム](./media/advancedselection1.png)](./media/advancedselection1.png)</span><span class="sxs-lookup"><span data-stu-id="2e42e-117">[![Advanced Selection pattern wireframe](./media/advancedselection1.png)](./media/advancedselection1.png)</span></span>

### <a name="related-patterns"></a><span data-ttu-id="2e42e-118">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="2e42e-118">Related patterns</span></span>

-   [<span data-ttu-id="2e42e-119">リスト パネルのサブパターン</span><span class="sxs-lookup"><span data-stu-id="2e42e-119">List Panel subpattern</span></span>](list-panel-subpattern.md)
-   [<span data-ttu-id="2e42e-120">ダイアログのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="2e42e-120">Dialog form pattern</span></span>](dialog-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="2e42e-121">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="2e42e-121">UX guidelines</span></span>
<span data-ttu-id="2e42e-122">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="2e42e-122">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="2e42e-123">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="2e42e-123">This checklist doesn’t include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="2e42e-124">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="2e42e-124">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="2e42e-125">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="2e42e-125">**Standard form guidelines:**</span></span>
    -   <span data-ttu-id="2e42e-126">標準フォーム ガイドラインは、[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="2e42e-126">Standard form guidelines have been consolidated into the [General form guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="2e42e-127">**高度な選択のガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="2e42e-127">**Advanced selection guidelines:**</span></span>
    -   <span data-ttu-id="2e42e-128">既定では、クイック フィルターは名前または説明列を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e42e-128">By default, the Quick filter should use the name or description column.</span></span>
    -   <span data-ttu-id="2e42e-129">リストには最大 15 の列を表示できます。</span><span class="sxs-lookup"><span data-stu-id="2e42e-129">The list can display up to 15 columns.</span></span> <span data-ttu-id="2e42e-130">**注記:** このガイドラインは Microsoft Dynamics AX 2012 から緩和されています。</span><span class="sxs-lookup"><span data-stu-id="2e42e-130">**Note:** This guidelines has been relaxed since Microsoft Dynamics AX 2012.</span></span>
    -   <span data-ttu-id="2e42e-131">主な指示は、ユーザーに何をする必要があるかを指示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e42e-131">The main instruction should instruct users what they need to do.</span></span>
    -   <span data-ttu-id="2e42e-132">データが存在しないとき、グリッドは新しいレコードを自動的に追加できません。</span><span class="sxs-lookup"><span data-stu-id="2e42e-132">When there is no data, the grid should not automatically add a new record.</span></span>

## <a name="example"></a><span data-ttu-id="2e42e-133">例</span><span class="sxs-lookup"><span data-stu-id="2e42e-133">Example</span></span>
<span data-ttu-id="2e42e-134">フォーム: **ProcCategoryAddVendor** (**調達** &gt; **調達カテゴリ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e42e-134">Form: **ProcCategoryAddVendor** (Click **Procurement and sourcing** &gt; **Procurement categories**.</span></span> <span data-ttu-id="2e42e-135">**仕入先**クイック タブで、**追加**をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="2e42e-135">On the **Vendors** FastTab, click **Add**.)</span></span> 

<span data-ttu-id="2e42e-136">[![高度な選択の例](./media/advancedselectionexample.png)](./media/advancedselectionexample.png)</span><span class="sxs-lookup"><span data-stu-id="2e42e-136">[![Example of advanced selection](./media/advancedselectionexample.png)](./media/advancedselectionexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="2e42e-137">付録</span><span class="sxs-lookup"><span data-stu-id="2e42e-137">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="2e42e-138">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="2e42e-138">Frequently asked questions</span></span>

<span data-ttu-id="2e42e-139">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="2e42e-139">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="2e42e-140">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="2e42e-140">Open issues</span></span>

<span data-ttu-id="2e42e-141">この時点ではなし</span><span class="sxs-lookup"><span data-stu-id="2e42e-141">None at this time</span></span>



