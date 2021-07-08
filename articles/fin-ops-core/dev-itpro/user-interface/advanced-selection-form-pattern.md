---
title: 高度な選択のフォーム パターン
description: この記事では、高度な選択のフォーム パターンに関する情報を提供します。これにより、ユーザーが大規模で広範なリストから品目をフィルタ処理して選択できます。
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29171
ms.assetid: c3c5eea7-f771-41ea-9976-8d0e1f3d3f25
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2093c74e302015b553cda92725a1c10b9abbab83
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189798"
---
# <a name="advanced-selection-form-pattern"></a><span data-ttu-id="c51d0-103">高度な選択のフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="c51d0-103">Advanced selection form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c51d0-104">この記事では、高度な選択フォーム パターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c51d0-104">This article provides information about the Advanced Selection form pattern.</span></span> <span data-ttu-id="c51d0-105">このダイアログ フォーム パターンを使用すると、ユーザーは大規模な全体のリストから項目をフィルターして選択できます。</span><span class="sxs-lookup"><span data-stu-id="c51d0-105">This Dialog form pattern lets users filter and select items from a large, wide list.</span></span> <span data-ttu-id="c51d0-106">リスト パネルのパターンと同様に、このパターンは主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c51d0-106">Like the List Panel pattern, this pattern should be used when the primary user task is to select a set of items.</span></span>

## <a name="usage"></a><span data-ttu-id="c51d0-107">用途</span><span class="sxs-lookup"><span data-stu-id="c51d0-107">Usage</span></span>

<span data-ttu-id="c51d0-108">高度な選択フォーム パターンは、主要なユーザー タスクが項目のセットを選択するときに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c51d0-108">The Advanced Selection form pattern should be used when the primary user task is to select a set of items.</span></span> <span data-ttu-id="c51d0-109">このタスクは、通常、複数選択リストによって達成されます。</span><span class="sxs-lookup"><span data-stu-id="c51d0-109">This task is usually accomplished through a multi-select list.</span></span> <span data-ttu-id="c51d0-110">ただし、多くのシナリオでは、ユーザーは連続していない品目を選択する必要があり、同時に、選択する品目の一覧を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c51d0-110">However, in many scenarios, users must select items that aren't contiguous and, at the same time, must see the set of items that they are selecting.</span></span> <span data-ttu-id="c51d0-111">このパターンは、ユーザーが 1 つのリスト内の項目を選択して別のリストに追加する点において、リスト パネルのパターンと似ています。</span><span class="sxs-lookup"><span data-stu-id="c51d0-111">This pattern resembles the List panel pattern, in that the user selects items in one list and adds them to another.</span></span> <span data-ttu-id="c51d0-112">ただし、このパターンにはカスタム フィルターおよび上部の「広い」リストがあり、およびページの画面「不動産」のほとんどを使用します (通常、大きなダイアログ)。</span><span class="sxs-lookup"><span data-stu-id="c51d0-112">However, this pattern allows for custom filters and a “wide” list on top, and uses most of the screen "real estate" of the page (typically, it's a Large dialog).</span></span> <span data-ttu-id="c51d0-113">大規模かつ広範囲のリストでフィルター処理および選択しなければならない場合にこのパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="c51d0-113">Use this pattern when a user must be able to filter and select in a large, wide list.</span></span>

## <a name="wireframe"></a><span data-ttu-id="c51d0-114">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="c51d0-114">Wireframe</span></span>

<span data-ttu-id="c51d0-115">[![高度な選択パターン ワイヤーフレーム](./media/advancedselection1.png)](./media/advancedselection1.png)</span><span class="sxs-lookup"><span data-stu-id="c51d0-115">[![Advanced Selection pattern wireframe](./media/advancedselection1.png)](./media/advancedselection1.png)</span></span>

### <a name="related-patterns"></a><span data-ttu-id="c51d0-116">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="c51d0-116">Related patterns</span></span>

-   [<span data-ttu-id="c51d0-117">リスト パネルのサブパターン</span><span class="sxs-lookup"><span data-stu-id="c51d0-117">List Panel subpattern</span></span>](list-panel-subpattern.md)
-   [<span data-ttu-id="c51d0-118">ダイアログのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="c51d0-118">Dialog form pattern</span></span>](dialog-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="c51d0-119">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="c51d0-119">UX guidelines</span></span>
<span data-ttu-id="c51d0-120">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="c51d0-120">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="c51d0-121">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="c51d0-121">This checklist doesn’t include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="c51d0-122">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="c51d0-122">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="c51d0-123">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="c51d0-123">**Standard form guidelines:**</span></span>
    -   <span data-ttu-id="c51d0-124">標準フォーム ガイドラインは、[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="c51d0-124">Standard form guidelines have been consolidated into the [General form guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="c51d0-125">**高度な選択のガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="c51d0-125">**Advanced selection guidelines:**</span></span>
    -   <span data-ttu-id="c51d0-126">既定では、クイック フィルターは名前または説明列を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c51d0-126">By default, the Quick filter should use the name or description column.</span></span>
    -   <span data-ttu-id="c51d0-127">リストには最大 15 の列を表示できます。</span><span class="sxs-lookup"><span data-stu-id="c51d0-127">The list can display up to 15 columns.</span></span> <span data-ttu-id="c51d0-128">**注記:** このガイドラインは Microsoft Dynamics AX 2012 から緩和されています。</span><span class="sxs-lookup"><span data-stu-id="c51d0-128">**Note:** This guidelines has been relaxed since Microsoft Dynamics AX 2012.</span></span>
    -   <span data-ttu-id="c51d0-129">主な指示は、ユーザーに何をする必要があるかを指示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c51d0-129">The main instruction should instruct users what they need to do.</span></span>
    -   <span data-ttu-id="c51d0-130">データが存在しないとき、グリッドは新しいレコードを自動的に追加できません。</span><span class="sxs-lookup"><span data-stu-id="c51d0-130">When there is no data, the grid should not automatically add a new record.</span></span>

## <a name="example"></a><span data-ttu-id="c51d0-131">例</span><span class="sxs-lookup"><span data-stu-id="c51d0-131">Example</span></span>
<span data-ttu-id="c51d0-132">フォーム: **ProcCategoryAddVendor** (**調達** &gt; **調達カテゴリ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c51d0-132">Form: **ProcCategoryAddVendor** (Click **Procurement and sourcing** &gt; **Procurement categories**.</span></span> <span data-ttu-id="c51d0-133">**仕入先** クイック タブで、**追加** をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="c51d0-133">On the **Vendors** FastTab, click **Add**.)</span></span> 

> <span data-ttu-id="c51d0-134">[注記] ごのフォームでは、このパターンが利用できません。ここで表示している画像では、一般的な拡張選択フォームパターンの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c51d0-134">[NOTE] This form no longer utilizes this pattern; however, the image shows an example of what a typical Advanced selection form pattern looks like.</span></span>

<span data-ttu-id="c51d0-135">[![高度な選択の例](./media/advancedselectionexample.png)](./media/advancedselectionexample.png)</span><span class="sxs-lookup"><span data-stu-id="c51d0-135">[![Example of advanced selection](./media/advancedselectionexample.png)](./media/advancedselectionexample.png)</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]