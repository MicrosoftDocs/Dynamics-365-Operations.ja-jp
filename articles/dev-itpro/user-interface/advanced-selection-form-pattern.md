---
title: "高度な選択のフォーム パターン"
description: "この記事では、高度な選択フォーム パターンに関する情報を提供します。 このダイアログ フォーム パターンを使用すると、ユーザーは大規模な全体のリストから項目をフィルターして選択できます。 リスト パネルのパターンと同様に、このパターンは主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 29171
ms.assetid: c3c5eea7-f771-41ea-9976-8d0e1f3d3f25
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8a63f24353ba0c79bc718f047331edd25a0a74a4
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="advanced-selection-form-pattern"></a><span data-ttu-id="e5dcd-105">高度な選択のフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="e5dcd-105">Advanced selection form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5dcd-106">この記事では、高度な選択フォーム パターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-106">This article provides information about the Advanced Selection form pattern.</span></span> <span data-ttu-id="e5dcd-107">このダイアログ フォーム パターンを使用すると、ユーザーは大規模な全体のリストから項目をフィルターして選択できます。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-107">This Dialog form pattern lets users filter and select items from a large, wide list.</span></span> <span data-ttu-id="e5dcd-108">リスト パネルのパターンと同様に、このパターンは主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-108">Like the List Panel pattern, this pattern should be used when the primary user task is to select a set of items.</span></span>

<a name="usage"></a><span data-ttu-id="e5dcd-109">用途</span><span class="sxs-lookup"><span data-stu-id="e5dcd-109">Usage</span></span>
-----

<span data-ttu-id="e5dcd-110">高度な選択フォーム パターンは、主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-110">The Advanced Selection form pattern should be used when the primary user task is to select a set of items.</span></span> <span data-ttu-id="e5dcd-111">このタスクは、通常、複数選択リストによって達成されます。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-111">This task is usually accomplished through a multi-select list.</span></span> <span data-ttu-id="e5dcd-112">ただし、多くのシナリオでは、ユーザーは連続していない品目を選択する必要があり、同時に、選択する品目の一覧を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-112">However, in many scenarios, users must select items that aren't contiguous and, at the same time, must see the set of items that they are selecting.</span></span> <span data-ttu-id="e5dcd-113">このパターンは、ユーザーが 1 つのリスト内の項目を選択して別のリストに追加する点において、リスト パネルのパターンと似ています。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-113">This pattern resembles the List panel pattern, in that the user selects items in one list and adds them to another.</span></span> <span data-ttu-id="e5dcd-114">ただし、このパターンにはカスタム フィルターおよび上部の「広い」リストがあり、およびページの画面「不動産」のほとんどを使用します (通常、大きなダイアログ)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-114">However, this pattern allows for custom filters and a “wide” list on top, and uses most of the screen "real estate" of the page (typically, it's a Large dialog).</span></span> <span data-ttu-id="e5dcd-115">大規模かつ広範囲のリストでフィルター処理および選択しなければならない場合にこのパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-115">Use this pattern when a user must be able to filter and select in a large, wide list.</span></span>

## <a name="wireframe"></a><span data-ttu-id="e5dcd-116">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="e5dcd-116">Wireframe</span></span>

<span data-ttu-id="e5dcd-117">[![高度な選択パターン ワイヤーフレーム](./media/advancedselection1.png)](./media/advancedselection1.png)</span><span class="sxs-lookup"><span data-stu-id="e5dcd-117">[![Advanced Selection pattern wireframe](./media/advancedselection1.png)](./media/advancedselection1.png)</span></span>

### <a name="related-patterns"></a><span data-ttu-id="e5dcd-118">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="e5dcd-118">Related patterns</span></span>

-   [<span data-ttu-id="e5dcd-119">リスト パネル</span><span class="sxs-lookup"><span data-stu-id="e5dcd-119">List Panel</span></span>](list-panel-subpattern.md)
-   [<span data-ttu-id="e5dcd-120">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="e5dcd-120">Dialog</span></span>](dialog-form-pattern.md)

## <a name="pattern-changes"></a><span data-ttu-id="e5dcd-121">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="e5dcd-121">Pattern changes</span></span>
<span data-ttu-id="e5dcd-122">これは、Finance and Operations における新しいパターンです。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-122">This is a new pattern in Finance and Operations.</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="e5dcd-123">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="e5dcd-123">UX guidelines</span></span>
<span data-ttu-id="e5dcd-124">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-124">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="e5dcd-125">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-125">This checklist doesn’t include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="e5dcd-126">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-126">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="e5dcd-127">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="e5dcd-127">**Standard form guidelines:**</span></span>
    -   <span data-ttu-id="e5dcd-128">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-128">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="e5dcd-129">**高度な選択のガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="e5dcd-129">**Advanced selection guidelines:**</span></span>
    -   <span data-ttu-id="e5dcd-130">既定では、クイック フィルターは名前または説明列を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-130">By default, the Quick filter should use the name or description column.</span></span>
    -   <span data-ttu-id="e5dcd-131">リストには最大 15 の列を表示できます。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-131">The list can display up to 15 columns.</span></span> <span data-ttu-id="e5dcd-132">**注記:** このガイドラインは、Microsoft Dynamics AX 2012 以降に緩和されています。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-132">**Note:** This guidelines has been relaxed since Microsoft Dynamics AX 2012.</span></span>
    -   <span data-ttu-id="e5dcd-133">主な指示は、ユーザーに何をする必要があるかを指示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-133">The main instruction should instruct users what they need to do.</span></span>
    -   <span data-ttu-id="e5dcd-134">データが存在しないとき、グリッドは新しいレコードを自動的に追加できません。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-134">When there is no data, the grid should not automatically add a new record.</span></span>

## <a name="example"></a><span data-ttu-id="e5dcd-135">例</span><span class="sxs-lookup"><span data-stu-id="e5dcd-135">Example</span></span>
<span data-ttu-id="e5dcd-136">フォーム: **ProcCategoryAddVendor** (**調達** &gt; **調達カテゴリ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-136">Form: **ProcCategoryAddVendor** (Click **Procurement and sourcing** &gt; **Procurement categories**.</span></span> <span data-ttu-id="e5dcd-137">**仕入先**クイック タブで、**追加**をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-137">On the **Vendors** FastTab, click **Add**.)</span></span> 

<span data-ttu-id="e5dcd-138">[![advancedSelectionExample](./media/advancedselectionexample.png)](./media/advancedselectionexample.png)</span><span class="sxs-lookup"><span data-stu-id="e5dcd-138">[![advancedSelectionExample](./media/advancedselectionexample.png)](./media/advancedselectionexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="e5dcd-139">付録</span><span class="sxs-lookup"><span data-stu-id="e5dcd-139">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="e5dcd-140">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="e5dcd-140">Frequently asked questions</span></span>

<span data-ttu-id="e5dcd-141">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="e5dcd-141">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="e5dcd-142">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="e5dcd-142">Open issues</span></span>

<span data-ttu-id="e5dcd-143">この時点ではなし</span><span class="sxs-lookup"><span data-stu-id="e5dcd-143">None at this time</span></span>




